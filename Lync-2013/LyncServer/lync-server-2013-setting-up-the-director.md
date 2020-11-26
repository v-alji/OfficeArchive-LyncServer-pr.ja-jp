---
title: 'Lync Server 2013: ディレクターの設定'
description: 'Lync Server 2013: ディレクターのセットアップ。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up the Director
ms:assetid: 408b76f7-6fdd-4e50-8a3e-e87db12c1394
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425915(v=OCS.15)
ms:contentKeyID: 48183951
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2b917000dec6d30fdec2963ff1e464fbb9a70805
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423905"
---
# <a name="setting-up-the-director-in-lync-server-2013"></a><span data-ttu-id="382ad-103">Lync Server 2013 でのディレクターの設定</span><span class="sxs-lookup"><span data-stu-id="382ad-103">Setting up the Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="382ad-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="382ad-104">

<span> </span></span></span>

<span data-ttu-id="382ad-105">_**最終更新日:** 2014-05-05_</span><span class="sxs-lookup"><span data-stu-id="382ad-105">_**Topic Last Modified:** 2014-05-05_</span></span>

<span data-ttu-id="382ad-106">エッジサーバーを展開して外部ユーザーのアクセスを有効にしている場合は、1つの選択肢としてディレクターを展開することができます。</span><span class="sxs-lookup"><span data-stu-id="382ad-106">If you’re enabling access for external users by deploying Edge Servers, one option is to deploy a Director.</span></span> <span data-ttu-id="382ad-107">ディレクターは、Microsoft Lync Server 2013 を実行しているサーバーで、ユーザー要求を認証しますが、ユーザーアカウントはホームになりません。</span><span class="sxs-lookup"><span data-stu-id="382ad-107">A Director is a server running Microsoft Lync Server 2013 that authenticates user requests, but doesn’t home any user accounts.</span></span> <span data-ttu-id="382ad-108">現時点では、これは必須ではありませんが、認証要求の合理化に役立てるために、パフォーマンスを心配していて、さらに便利です。</span><span class="sxs-lookup"><span data-stu-id="382ad-108">Now, this isn’t a requirement, but it is very helpful if you’re worried about performance and want to help streamline authentication requests.</span></span> <span data-ttu-id="382ad-109">組織にとってこの方法が適していると判断された場合は、ディレクターまたはディレクタープールをセットアップする手順は、Enterprise Edition のフロントエンドプールまたは Standard Edition サーバーの設定に似ています。</span><span class="sxs-lookup"><span data-stu-id="382ad-109">If you decide this is a good idea for your organization, the steps to set up a Director or a Director pool are similar to setting up either an Enterprise Edition Front End pool or Standard Edition server.</span></span> <span data-ttu-id="382ad-110">トポロジビルダーでディレクターを定義した後で、このセクションの手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="382ad-110">After you’ve defined your Director(s) in Topology Builder, you’ll need to perform the steps in this section.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="382ad-111">このセクション中</span><span class="sxs-lookup"><span data-stu-id="382ad-111">In This Section</span></span>

  - [<span data-ttu-id="382ad-112">Lync Server 2013 でのローカル構成ストアのインストール</span><span class="sxs-lookup"><span data-stu-id="382ad-112">Install the Local Configuration store in Lync Server 2013</span></span>](lync-server-2013-install-the-local-configuration-store.md)

  - [<span data-ttu-id="382ad-113">ディレクターでの Lync Server 2013 のインストール</span><span class="sxs-lookup"><span data-stu-id="382ad-113">Install Lync Server 2013 on the Director</span></span>](lync-server-2013-install-lync-server-on-the-director.md)

  - [<span data-ttu-id="382ad-114">Lync Server 2013 でのディレクターの証明書の構成</span><span class="sxs-lookup"><span data-stu-id="382ad-114">Configure certificates for the Director in Lync Server 2013</span></span>](lync-server-2013-configure-certificates-for-the-director.md)

  - [<span data-ttu-id="382ad-115">Lync Server 2013 でのディレクターのサービスの開始</span><span class="sxs-lookup"><span data-stu-id="382ad-115">Start services on the Director in Lync Server 2013</span></span>](lync-server-2013-start-services-on-the-director.md)

  - [<span data-ttu-id="382ad-116">Lync Server 2013 でのディレクターのテスト</span><span class="sxs-lookup"><span data-stu-id="382ad-116">Test the Director in Lync Server 2013</span></span>](lync-server-2013-test-the-director.md)

  - [<span data-ttu-id="382ad-117">Lync Server 2013 でのディレクターを使った自動クライアント サインインの構成</span><span class="sxs-lookup"><span data-stu-id="382ad-117">Configure Automatic Client Sign-In to use the Director in Lync Server 2013</span></span>](lync-server-2013-configure-automatic-client-sign-in-to-use-the-director.md)

<span data-ttu-id="382ad-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="382ad-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

