---
title: 'Lync Server 2013: Lync 2013 のグループポリシー設定'
description: 'Lync Server 2013: Lync 2013 のグループポリシー設定。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Group Policy settings for Lync 2013
ms:assetid: 5917a52b-dae0-4ec0-8548-a68dc20ab71c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204924(v=OCS.15)
ms:contentKeyID: 48184235
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5c6f2b26fc19653b0098ed4775df1f9c8146986c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427783"
---
# <a name="group-policy-settings-for-lync-2013"></a><span data-ttu-id="be5e2-103">Lync 2013 のグループポリシー設定</span><span class="sxs-lookup"><span data-stu-id="be5e2-103">Group Policy settings for Lync 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="be5e2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="be5e2-104">

<span> </span></span></span>

<span data-ttu-id="be5e2-105">_**最終更新日:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="be5e2-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="be5e2-106">以前のバージョンの Lync と Office Communicator では、スタンドアロンの Communicator 管理用テンプレートを使用してクライアントグループポリシー設定を構成できました。</span><span class="sxs-lookup"><span data-stu-id="be5e2-106">In previous versions of Lync and Office Communicator, a stand-alone Communicator.adm administrative template was available for configuring client Group Policy settings.</span></span> <span data-ttu-id="be5e2-107">Lync 2013 では、新しい管理用テンプレートファイル (admx および adml ファイル) が、Office グループポリシー管理用テンプレートと共に含まれています。</span><span class="sxs-lookup"><span data-stu-id="be5e2-107">For Lync 2013, new administrative template files (.admx and .adml files) are included along with the Office Group Policy Administrative Template.</span></span> <span data-ttu-id="be5e2-108">Lync 2013 の admx ファイルと adml ファイルを使用できるかどうかによって、テンプレートをダウンロードし、すべての Office プログラムと言語パックのグループポリシー設定を一元管理できます。</span><span class="sxs-lookup"><span data-stu-id="be5e2-108">The availability of Lync 2013 .admx and .adml files allows you to download templates and centrally manage Group Policy settings for all your Office programs and language packs.</span></span> <span data-ttu-id="be5e2-109">詳細については、Office 2013 ドキュメントの「Office 2013 管理用テンプレートファイル (ADMX、ADML)」を参照してください <https://go.microsoft.com/fwlink/p/?linkid=267516> 。</span><span class="sxs-lookup"><span data-stu-id="be5e2-109">For details, see “Office 2013 Administrative Template files (ADMX, ADML)” in the Office 2013 documentation at <https://go.microsoft.com/fwlink/p/?linkid=267516>.</span></span>

<div>

## <a name="client-bootstrapping-policies"></a><span data-ttu-id="be5e2-110">クライアントブートストラップポリシー</span><span class="sxs-lookup"><span data-stu-id="be5e2-110">Client Bootstrapping Policies</span></span>

<span data-ttu-id="be5e2-111">ユーザーが初めてサーバーにサインインする前に構成する必要があるクライアントブートストラップポリシーはいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="be5e2-111">There are several client bootstrapping policies that you should configure before users sign in to the server for the first time.</span></span> <span data-ttu-id="be5e2-112">これらのポリシーは、クライアントがサインインしてサーバーからインバンドのプロビジョニング設定を受信する前に有効になるため、グループポリシーを使って構成することができます。</span><span class="sxs-lookup"><span data-stu-id="be5e2-112">Because these policies take effect before the client signs in and begins receiving in-band provisioning settings from the server, you can use Group Policy to configure them.</span></span> <span data-ttu-id="be5e2-113">詳細については、展開ドキュメントの「 [Lync Server 2013 でのクライアントブートストラップポリシーの構成](lync-server-2013-configuring-client-bootstrapping-policies.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="be5e2-113">For more information, see [Configuring client bootstrapping policies in Lync Server 2013](lync-server-2013-configuring-client-bootstrapping-policies.md) in the Deployment documentation.</span></span>

<span data-ttu-id="be5e2-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="be5e2-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

