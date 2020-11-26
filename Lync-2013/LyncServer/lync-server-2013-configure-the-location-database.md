---
title: 'Lync Server 2013: 場所データベースを構成する'
description: 'Lync Server 2013: 場所データベースを構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure the location database
ms:assetid: 8544be31-6958-47ef-b926-fdc80d56191c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398679(v=OCS.15)
ms:contentKeyID: 48184704
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 877c83976ca0db9abc3a9e57d4a1cf5adaa1291a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433613"
---
# <a name="configure-the-location-database-in-lync-server-2013"></a><span data-ttu-id="2acbf-103">Configure the location database in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2acbf-103">Configure the location database in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2acbf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2acbf-104">

<span> </span></span></span>

<span data-ttu-id="2acbf-105">_**最終更新日:** 2012-09-17_</span><span class="sxs-lookup"><span data-stu-id="2acbf-105">_**Topic Last Modified:** 2012-09-17_</span></span>

<span data-ttu-id="2acbf-106">クライアントがネットワーク内の各自の場所を自動検出できるようにするには、まず場所データベースを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2acbf-106">To enable clients to automatically detect their location within a network, you first need to configure the location database.</span></span> <span data-ttu-id="2acbf-107">場所のデータベースを構成せず、場所のポリシーで **必要な場所** が **[はい]** または [ **免責**] に設定されている場合は、場所を手動で入力するように求められます。</span><span class="sxs-lookup"><span data-stu-id="2acbf-107">If you do not configure a location database, and **Location Required** in the location policy is set to **Yes** or **Disclaimer**, the user will be prompted to manually enter a location.</span></span>

<span data-ttu-id="2acbf-108">場所データベースを構成するには、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="2acbf-108">To configure the location database, you will perform the following tasks:</span></span>

1.  <span data-ttu-id="2acbf-109">ネットワーク要素と場所のマッピングをデータベースに設定します。</span><span class="sxs-lookup"><span data-stu-id="2acbf-109">Populate the database with a mapping of network elements to locations.</span></span> <span data-ttu-id="2acbf-110">緊急対応の場所識別番号 (ELIN) ゲートウェイを使用する場合は、フィールドに ELIN を含める必要があり \<CompanyName\> ます。</span><span class="sxs-lookup"><span data-stu-id="2acbf-110">If you use an Emergency Location Identification Number (ELIN) gateway, you need to include the ELIN in the \<CompanyName\> field.</span></span>

2.  <span data-ttu-id="2acbf-111">E9-1-1 サービス プロバイダーで保持されている主要道路住所案内 (MSAG) と照らし合わせて住所を確認します。</span><span class="sxs-lookup"><span data-stu-id="2acbf-111">Validate the addresses against the master street address guide (MSAG) that is maintained by the E9-1-1 service provider.</span></span>

3.  <span data-ttu-id="2acbf-112">更新したデータベースを公開します。</span><span class="sxs-lookup"><span data-stu-id="2acbf-112">Publish the updated database.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="2acbf-113">または、場所データベースの配置で使用できるセカンダリの場所ソースデータベースを定義することもできます。</span><span class="sxs-lookup"><span data-stu-id="2acbf-113">Alternately, you can define a secondary location source database that can be used in placed of the location database.</span></span> <span data-ttu-id="2acbf-114">詳細については、「 <A href="lync-server-2013-configure-a-secondary-location-information-service.md">Lync Server 2013 でセカンダリ場所情報サービスを構成する</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2acbf-114">For details, see <A href="lync-server-2013-configure-a-secondary-location-information-service.md">Configure a secondary Location Information service in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="2acbf-115">このセクション中</span><span class="sxs-lookup"><span data-stu-id="2acbf-115">In This Section</span></span>

  - [<span data-ttu-id="2acbf-116">Lync Server 2013 で位置情報データベースを設定する</span><span class="sxs-lookup"><span data-stu-id="2acbf-116">Populate the location database in Lync Server 2013</span></span>](lync-server-2013-populate-the-location-database.md)

  - [<span data-ttu-id="2acbf-117">Lync Server 2013 で住所を検証する</span><span class="sxs-lookup"><span data-stu-id="2acbf-117">Validate addresses in Lync Server 2013</span></span>](lync-server-2013-validate-addresses.md)

  - [<span data-ttu-id="2acbf-118">Lync Server 2013 からロケーションデータベースを発行する</span><span class="sxs-lookup"><span data-stu-id="2acbf-118">Publish the location database from Lync Server 2013</span></span>](lync-server-2013-publish-the-location-database.md)

<span data-ttu-id="2acbf-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2acbf-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

