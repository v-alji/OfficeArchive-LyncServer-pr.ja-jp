---
title: 'Lync Server 2013: ホスト型ボイス メール ポリシー'
description: 'Lync Server 2013: ホストされているボイスメールのポリシー。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hosted voice mail policies
ms:assetid: d62a35ed-cbe2-4f06-86b4-e192c18435c1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398932(v=OCS.15)
ms:contentKeyID: 48185506
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 57461f4ffd2c6f2cd733dd7ec2c945c9e7b801c2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427503"
---
# <a name="hosted-voice-mail-policies-in-lync-server-2013"></a><span data-ttu-id="86acd-103">Lync Server 2013 のホスト型ボイス メール ポリシー</span><span class="sxs-lookup"><span data-stu-id="86acd-103">Hosted voice mail policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="86acd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="86acd-104">

<span> </span></span></span>

<span data-ttu-id="86acd-105">_**最終更新日:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="86acd-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="86acd-106">ホストされた *ボイスメールポリシー* は、ホストされた Exchange サービス上にあるメールボックスを持つユーザーの呼び出しをルーティングする場所について、Lync Server 2013 Exum ルーティングアプリケーションに情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="86acd-106">A *hosted voice mail policy* provides information to the Lync Server 2013 ExUM Routing application about where to route calls for users whose mailboxes are located on a hosted Exchange service.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="86acd-107">ホストされたボイスメールポリシーは、Lync Server 2013 でのホストされた Exchange UM との統合にのみ必要です。</span><span class="sxs-lookup"><span data-stu-id="86acd-107">Hosted voice mail policies are required only for Lync Server 2013 integration with hosted Exchange UM.</span></span> <span data-ttu-id="86acd-108">オンプレミスの Exchange UM との統合には必要ありません。</span><span class="sxs-lookup"><span data-stu-id="86acd-108">They are not needed for integration with on-premises Exchange UM.</span></span>



</div>

<div>

## <a name="hosted-voice-mail-policy-scope"></a><span data-ttu-id="86acd-109">ホストされたボイスメールポリシーのスコープ</span><span class="sxs-lookup"><span data-stu-id="86acd-109">Hosted Voice Mail Policy Scope</span></span>

<span data-ttu-id="86acd-110">ホストされたボイスメールポリシーのスコープによって、ポリシーが適用される階層レベルが決まります。</span><span class="sxs-lookup"><span data-stu-id="86acd-110">Hosted voice mail policy scope determines the hierarchical level at which the policy applies.</span></span> <span data-ttu-id="86acd-111">以下のスコープレベルで、ホストされたボイスメールポリシーを構成できます。</span><span class="sxs-lookup"><span data-stu-id="86acd-111">You can configure hosted voice mail policies with the following scope levels:</span></span>

  - <span data-ttu-id="86acd-112">*グローバル* ポリシーは、Lync Server 2013 の展開におけるすべてのユーザーに影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="86acd-112">The *global* policy can potentially affect all users in the Lync Server 2013 deployment.</span></span> <span data-ttu-id="86acd-113">ホストされた Exchange UM アクセスが有効になっていて、ユーザーごとのポリシーが割り当てられていない場合や、サイトポリシーがユーザーのサイトに割り当てられていない場合は、グローバルポリシーが適用されます。</span><span class="sxs-lookup"><span data-stu-id="86acd-113">If a user is enabled for hosted Exchange UM access and has not been assigned a per-user policy, and if a site policy has not been assigned to the user’s site, the global policy applies.</span></span> <span data-ttu-id="86acd-114">グローバルポリシーは Lync Server 2013 と共にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="86acd-114">The global policy is installed with Lync Server 2013.</span></span> <span data-ttu-id="86acd-115">必要に応じて変更できますが、名前の変更や削除はできません。</span><span class="sxs-lookup"><span data-stu-id="86acd-115">You can modify it to meet your needs, but you cannot rename or delete it.</span></span>

  - <span data-ttu-id="86acd-116">*サイト* ポリシーは、ポリシーが定義されているサイトをホームにしているすべてのユーザーに影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="86acd-116">A *site* policy can affect all users that are homed on the site for which the policy is defined.</span></span> <span data-ttu-id="86acd-117">ユーザーがホストされた Exchange UM アクセス用に構成されていて、ユーザーごとのポリシーが割り当てられていない場合は、サイトポリシーが適用されます。</span><span class="sxs-lookup"><span data-stu-id="86acd-117">If a user is configured for hosted Exchange UM access and has not been assigned a per-user policy, the site policy applies.</span></span>

  - <span data-ttu-id="86acd-118">*ユーザーごと* のポリシーは、個々のユーザーまたはグループにのみ影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="86acd-118">A *per-user* policy can affect only individual users or groups.</span></span> <span data-ttu-id="86acd-119">ユーザーごとのポリシーを適用するには、個々のユーザー、グループ、連絡先オブジェクトにポリシーを明示的に割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="86acd-119">To enforce a per-user policy, you must explicitly assign the policy to individual users, groups, and contact objects.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="86acd-120">ほとんどの場合、ホストされるボイスメールのポリシーは1つだけ必要です。</span><span class="sxs-lookup"><span data-stu-id="86acd-120">In most cases, only one hosted voice mail policy is required.</span></span> <span data-ttu-id="86acd-121">多くの場合、すべてのニーズに合わせてグローバルポリシーを変更できます。</span><span class="sxs-lookup"><span data-stu-id="86acd-121">You can often modify the global policy to meet all your needs.</span></span> <span data-ttu-id="86acd-122">複数のホストされたボイスメールポリシーを展開する場合、そのようなすべてのポリシーにはユーザーごとのスコープがあります。</span><span class="sxs-lookup"><span data-stu-id="86acd-122">If you deploy multiple hosted voice mail policies, all such policies have per-user scope.</span></span>



</div>

</div>

<div>

## <a name="hosted-voice-mail-policy-attributes"></a><span data-ttu-id="86acd-123">ホストされたボイスメールポリシーの属性</span><span class="sxs-lookup"><span data-stu-id="86acd-123">Hosted Voice Mail Policy Attributes</span></span>

<span data-ttu-id="86acd-124">ボイスメールポリシーは、次の2つの属性を定義します。 Lync Server 2013 ExUM ルーティングアプリケーションは、ホストされた Exchange UM 実装に送信される INVITE メッセージの要求 URI に挿入します。</span><span class="sxs-lookup"><span data-stu-id="86acd-124">A voice mail policy defines two attributes that the Lync Server 2013 ExUM Routing application inserts in the request URI of an INVITE message that is sent to the hosted Exchange UM implementation:</span></span>

  - <span data-ttu-id="86acd-125">**Destination:** ホストされている Exchange UM サービスの完全修飾ドメイン名 (FQDN)。</span><span class="sxs-lookup"><span data-stu-id="86acd-125">**Destination:** The fully qualified domain name (FQDN) of the hosted Exchange UM service.</span></span> <span data-ttu-id="86acd-126">この値は、ルーティング目的でオンプレミスの Lync Server Edge サーバーによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="86acd-126">This value is used by the on-premises Lync Server Edge Server for routing purposes.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="86acd-127">Exchange Online の FQDN は exap.um.outlook.com です。</span><span class="sxs-lookup"><span data-stu-id="86acd-127">The FQDN for Exchange Online is exap.um.outlook.com.</span></span>

    
    </div>

  - <span data-ttu-id="86acd-128">**組織:** Lync Server 2013 ユーザーのメールボックスをホームとする、ホストされた Exchange UM サービス上のテナントの FQDN。</span><span class="sxs-lookup"><span data-stu-id="86acd-128">**Organization:** The FQDN of the tenant on the hosted Exchange UM service that homes your Lync Server 2013 users’ mailboxes.</span></span> <span data-ttu-id="86acd-129">ボイスメールのポリシーには、複数の組織を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="86acd-129">A voice mail policy can contain multiple organizations.</span></span> <span data-ttu-id="86acd-130">ポリシーに複数の組織が含まれている場合、この属性は、Lync Server 2013 ユーザーメールボックスのホームとなる Exchange Server テナントのコンマ区切りリストである必要があります。</span><span class="sxs-lookup"><span data-stu-id="86acd-130">If more than one organization is included in the policy, this attribute must be a comma-separated list of the Exchange Server tenants that home your Lync Server 2013 user mailboxes.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="86acd-131">ホストされた Exchange UM サービスのテナント管理者が、宛先と組織の属性設定に必要な値を提供します。</span><span class="sxs-lookup"><span data-stu-id="86acd-131">The tenant administrator of your hosted Exchange UM service will provide the necessary values for your Destination and Organization attribute settings.</span></span> <span data-ttu-id="86acd-132">ポリシーを構成するには、New-CsHostedVoicemailPolicy コマンドレットを実行するか、または Set-CsHostedVoicemailPolicy コマンドレットを使用して、存在するもの (グローバルポリシーなど) を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="86acd-132">To configure your policy, you must run the New-CsHostedVoicemailPolicy cmdlet or use the Set-CsHostedVoicemailPolicy cmdlet to modify one that exists (for example, the global policy).</span></span>



</div>

<span data-ttu-id="86acd-133">ホストされたボイスメールポリシーの管理について詳しくは、次のコマンドレットの Lync Server 管理シェルに関するドキュメントをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="86acd-133">For details about managing hosted voice mail policies, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - <span data-ttu-id="86acd-134">New-CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="86acd-134">New-CsHostedVoicemailPolicy</span></span>

  - <span data-ttu-id="86acd-135">Set-CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="86acd-135">Set-CsHostedVoicemailPolicy</span></span>

  - <span data-ttu-id="86acd-136">Get-CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="86acd-136">Get-CsHostedVoicemailPolicy</span></span>

</div>

<div>

## <a name="per-user-voice-mail-policy-assignment"></a><span data-ttu-id="86acd-137">Per-User ボイスメールポリシーの割り当て</span><span class="sxs-lookup"><span data-stu-id="86acd-137">Per-User Voice Mail Policy Assignment</span></span>

<span data-ttu-id="86acd-138">ホストされたボイスメールのポリシーがユーザーごとのスコープで定義されている場合は、明示的に割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="86acd-138">If your hosted voice mail policy is defined with per-user scope, you must explicitly assign it.</span></span> <span data-ttu-id="86acd-139">Grant-CsHostedVoicemailPolicy コマンドレットを実行して、個々のユーザーまたはグループにポリシーを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="86acd-139">You can run the Grant-CsHostedVoicemailPolicy cmdlet to assign the policy to individual users or groups.</span></span>

<span data-ttu-id="86acd-140">ユーザーごとにホストされるボイスメールのポリシーの割り当てまたは削除の詳細については、次のコマンドレットの Lync Server 管理シェルに関するドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="86acd-140">For details about assigning or removing a per-user hosted voice mail policy, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - <span data-ttu-id="86acd-141">Grant-CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="86acd-141">Grant-CsHostedVoicemailPolicy</span></span>

  - <span data-ttu-id="86acd-142">Remove-CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="86acd-142">Remove-CsHostedVoicemailPolicy</span></span>

<span data-ttu-id="86acd-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="86acd-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

