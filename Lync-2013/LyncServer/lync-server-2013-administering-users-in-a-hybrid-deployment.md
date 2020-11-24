---
title: 'Lync Server 2013: ハイブリッド展開でユーザーを管理する'
description: 'Lync Server 2013: ハイブリッド展開でユーザーを管理します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Administering users in a hybrid deployment
ms:assetid: 6924ed7b-30a9-4be7-b952-90655625f2c8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204967(v=OCS.15)
ms:contentKeyID: 48184381
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7f1d7684a9f56eb013574a985ded0313378621c2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398007"
---
# <a name="administering-users-in-a-hybrid-lync-server-2013-deployment"></a><span data-ttu-id="b020b-103">ハイブリッド Lync Server 2013 展開でユーザーを管理する</span><span class="sxs-lookup"><span data-stu-id="b020b-103">Administering users in a hybrid Lync Server 2013 deployment</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b020b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b020b-104">

<span> </span></span></span>

<span data-ttu-id="b020b-105">_**最終更新日:** 2014-05-29_</span><span class="sxs-lookup"><span data-stu-id="b020b-105">_**Topic Last Modified:** 2014-05-29_</span></span>

<span data-ttu-id="b020b-106">Microsoft 365 管理センターで使用可能なユーザー管理機能を使って、Lync Online に移行したユーザーのユーザー設定とポリシーを管理できます。</span><span class="sxs-lookup"><span data-stu-id="b020b-106">You can manage user settings and policies for users migrated to Lync Online by using the User Management features available in the Microsoft 365 admin center.</span></span> <span data-ttu-id="b020b-107">管理タスクを実行するには、テナント管理者アカウントを使用してサインインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b020b-107">You must sign in by using your tenant administrator account to perform administration tasks.</span></span>

<div>

## <a name="moving-users-back-to-on-premises"></a><span data-ttu-id="b020b-108">ユーザーをオンプレミスに戻す</span><span class="sxs-lookup"><span data-stu-id="b020b-108">Moving Users Back to On-premises</span></span>

<div class="">


> [!IMPORTANT]  
> <span data-ttu-id="b020b-109">このセクションは、Lync をオンプレミスで作成して有効にし、オンプレミスの展開から Lync Online に移行したユーザーにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="b020b-109">This section applies only to users that were created and enabled for Lync on-premises and then moved from an on-premises deployment to Lync Online.</span></span> <span data-ttu-id="b020b-110">Lync Online で作成されたユーザーを移動する場合 (オンプレミスの展開で Lync に対して有効にしていない場合) は、「lync <A href="lync-server-2013-moving-users-from-lync-online-to-lync-on-premises.md">Online のユーザーを Lync Server 2013 で社内の lync に移動</A>する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b020b-110">If you want to move users that were created in Lync Online (and not ever enabled for Lync in an on-premises deployment) see, <A href="lync-server-2013-moving-users-from-lync-online-to-lync-on-premises.md">Moving users from Lync Online to Lync on-premises in Lync Server 2013</A>.</span></span>



</div>

  - <span data-ttu-id="b020b-111">Lync Online からオンプレミスの Lync にユーザーを戻すには、次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="b020b-111">Run the following cmdlets to move a user from Lync Online back to Lync on-premises:</span></span>
    
       ```PowerShell
        $cred=Get-Credential
       ```
    
       ```PowerShell
        Move-CsUser -Identity username@contoso.com -Target localpool.contoso.com -Credential $cred -HostedMigrationOverrideUrl <URL>
       ```

<span data-ttu-id="b020b-112">**HostedMigrationOverrideUrl** パラメーターの URL には、ホスティング型移行サービスが実行されているプールへの URL を次の形式で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b020b-112">The format of the URL specified for the **HostedMigrationOverrideUrl** parameter must be the URL to the pool where the Hosted Migration service is running, in the following format:</span></span>

<span data-ttu-id="b020b-113"> Https:// \<Pool FQDN\> /HostedMigration/hostedmigrationService.svc.</span><span class="sxs-lookup"><span data-stu-id="b020b-113">Https://\<Pool FQDN\>/HostedMigration/hostedmigrationService.svc.</span></span> <span data-ttu-id="b020b-114">ホスティング型移行サービスの URL は、Microsoft 365 または Office 365 の組織アカウントの Lync Online コントロールパネルの URL を表示することで確認できます。</span><span class="sxs-lookup"><span data-stu-id="b020b-114">You can determine the URL to the Hosted Migration Service by viewing the URL for the Lync Online Control Panel for your Microsoft 365 or Office 365 organization account.</span></span>

<span data-ttu-id="b020b-115">**Microsoft 365 または Office 365 組織のホスティング型移行サービスの URL を確認するには**</span><span class="sxs-lookup"><span data-stu-id="b020b-115">**To determine the Hosted Migration Service URL for your Microsoft 365 or Office 365 organization**</span></span>

1.  <span data-ttu-id="b020b-116">組織に管理者としてログインします。</span><span class="sxs-lookup"><span data-stu-id="b020b-116">Log in to your organization as an administrator.</span></span>

2.  <span data-ttu-id="b020b-117">**Lync 管理センター** を開きます。</span><span class="sxs-lookup"><span data-stu-id="b020b-117">Open the **Lync admin center**.</span></span>

3.  <span data-ttu-id="b020b-118">**Lync 管理センター** が表示されたら、アドレスバーの URL を選択して **lync.com** にコピーします。</span><span class="sxs-lookup"><span data-stu-id="b020b-118">With the **Lync admin center** displayed, select and copy the URL in the address bar up to **lync.com**.</span></span> <span data-ttu-id="b020b-119">URL は、次のような書式です。</span><span class="sxs-lookup"><span data-stu-id="b020b-119">An example URL looks similar to the following:</span></span>
    
    `https://webdir0a.online.lync.com/lscp/?language=en-US&tenantID=`

4.  <span data-ttu-id="b020b-120">URL の **webdir** を **admin** に置き換えると、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="b020b-120">Replace **webdir** in the URL with **admin**, resulting in the following:</span></span>
    
    `https://admin0a.online.lync.com`

5.  <span data-ttu-id="b020b-121">URL に以下の文字列を付加します。**/HostedMigration/hostedmigrationservice.svc**</span><span class="sxs-lookup"><span data-stu-id="b020b-121">Append the following string to the URL: **/HostedMigration/hostedmigrationservice.svc**.</span></span>
    
    <span data-ttu-id="b020b-122">以上の手順によって、**HostedMigrationOverrideUrl** の値を持った URL は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="b020b-122">The resulting URL, which is the value of the **HostedMigrationOverrideUrl**, should look like the following:</span></span>
    
    `https://admin0a.online.lync.com/HostedMigration/hostedmigrationservice.svc`

<span data-ttu-id="b020b-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b020b-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

