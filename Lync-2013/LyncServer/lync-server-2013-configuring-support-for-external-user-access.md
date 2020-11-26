---
title: 'Lync Server 2013: 外部ユーザー アクセスのサポートの構成'
description: 'Lync Server 2013: 外部ユーザーアクセスのサポートを構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring support for external user access
ms:assetid: f8424f8c-f965-4414-8485-30f07e10214a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413051(v=OCS.15)
ms:contentKeyID: 48185874
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d5a91f9b285a80ff6a0f3c58c2c12f88d72aac98
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432619"
---
# <a name="configuring-support-for-external-user-access-in-lync-server-2013"></a><span data-ttu-id="d5c23-103">Lync Server 2013 での外部ユーザー アクセスのサポートの構成</span><span class="sxs-lookup"><span data-stu-id="d5c23-103">Configuring support for external user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d5c23-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d5c23-104">

<span> </span></span></span>

<span data-ttu-id="d5c23-105">_**最終更新日:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="d5c23-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="d5c23-106">エッジサーバーまたはエッジプールの展開は、外部ユーザーをサポートするための最初の手順です。</span><span class="sxs-lookup"><span data-stu-id="d5c23-106">Deploying an Edge Server or Edge pool is the first step to supporting external users.</span></span> <span data-ttu-id="d5c23-107">エッジサーバーの展開の詳細については、展開ドキュメントの「 [Lync Server 2013 での外部ユーザーアクセスの展開](lync-server-2013-deploying-external-user-access.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5c23-107">For details about deploying Edge Servers, see [Deploying external user access in Lync Server 2013](lync-server-2013-deploying-external-user-access.md) in the Deployment documentation.</span></span> <span data-ttu-id="d5c23-108">ポリシーの構成について重要な考慮事項は、ポリシーの優先順位とポリシーの適用方法を理解することです。</span><span class="sxs-lookup"><span data-stu-id="d5c23-108">An important consideration for the configuration of policies is to understand the precedence of policies and how the policies are applied.</span></span> <span data-ttu-id="d5c23-109">1つのポリシーレベルで適用される Lync Server ポリシーの設定は、別のポリシーレベルで適用されている設定を上書きすることができます。</span><span class="sxs-lookup"><span data-stu-id="d5c23-109">Lync Server policy settings that are applied at one policy level can override settings that are applied at another policy level.</span></span> <span data-ttu-id="d5c23-110">Lync Server ポリシーの優先順位: ユーザーポリシー (ほとんどの影響) によってサイトポリシーが上書きされ、サイトポリシーがグローバルポリシーを上書きします (最も影響が少なくなります)。</span><span class="sxs-lookup"><span data-stu-id="d5c23-110">Lync Server policy precedence is: User policy (most influence) overrides a Site policy, and then a Site policy overrides a Global policy (least influence).</span></span> <span data-ttu-id="d5c23-111">つまり、ポリシー設定が、そのポリシーの影響を受けるオブジェクトに近いほど、オブジェクトに及ぼす影響は大きくなります。</span><span class="sxs-lookup"><span data-stu-id="d5c23-111">This means that the closer the policy setting is to the object that the policy is affecting, the more influence it has on the object.</span></span>

<span data-ttu-id="d5c23-112">エッジサーバーまたはエッジプールのセットアップが完了したら、提供する外部ユーザーアクセスの種類を有効にして、外部アクセスの設定を構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5c23-112">After completing the setup of an Edge Server or Edge pool, you must enable the types of external user access that you want to provide, and configure the settings for the external access.</span></span> <span data-ttu-id="d5c23-113">Lync server 2013 では、lync Server コントロールパネル、Lync Server 管理シェル、またはその両方を使用して、外部ユーザーのアクセスとポリシーを有効にし、構成することができます。</span><span class="sxs-lookup"><span data-stu-id="d5c23-113">In Lync Server 2013, you enable and configure external user access and policies using the Lync Server Control Panel, the Lync Server Management Shell or both, based on the task requirements.</span></span>

<span data-ttu-id="d5c23-114">外部ユーザーのアクセスをサポートするには、次の両方の操作を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5c23-114">To support external user access, you must do both of the following:</span></span>

  - <span data-ttu-id="d5c23-115">**組織のサポートを有効にする**   展開で外部ユーザーアクセスのサポートを有効にするには、サポートする各種類の外部アクセスを有効にします。</span><span class="sxs-lookup"><span data-stu-id="d5c23-115">**Enable support for your organization**   To enable support for external user access in your deployment, you enable each type of external access that you want to support.</span></span> <span data-ttu-id="d5c23-116">外部ユーザーアクセスのサポートを有効または無効にするには、Lync Server コントロールパネルの [**フェデレーションと外部アクセス**] グループの [**外部アクセスポリシー** ] ページで、または lync server 管理シェルと関連付けられたコマンドレットを使用して、グローバル設定を編集するか、サイトまたはユーザーポリシーを作成して構成します。</span><span class="sxs-lookup"><span data-stu-id="d5c23-116">You enable and disable support for external user access by editing the global settings or creating and configuring a site or user policy on the **External Access Policy** page in the **Federation and External Access** group of the Lync Server Control Panel or by using the Lync Server Management Shell and associated cmdlets.</span></span> <span data-ttu-id="d5c23-117">**外部アクセスポリシー** を管理するためのコマンドレットについては、「 [Lync Server 2013 の「フェデレーション」と「外部アクセスコマンドレット](https://docs.microsoft.com/powershell/module/skype/)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="d5c23-117">Cmdlets for managing the **External Access Policy** are found in the topic [Federation and external access cmdlets in Lync Server 2013](https://docs.microsoft.com/powershell/module/skype/).</span></span> <span data-ttu-id="d5c23-118">外部アクセスのサポートを有効にすると、Lync Server アクセスエッジサービスを実行しているサーバーが外部ユーザーとサーバーとの通信をサポートすることになります。</span><span class="sxs-lookup"><span data-stu-id="d5c23-118">Enabling support for external access specifies that your servers running the Lync Server Access Edge service support communications with external users and servers.</span></span> <span data-ttu-id="d5c23-119">外部ユーザーのアクセスが無効になっているか、ポリシーがまだサポートされていない場合、内部および外部ユーザーは通信できません。</span><span class="sxs-lookup"><span data-stu-id="d5c23-119">Internal and external users cannot communicate while external user access is disabled or if policies have not yet been configured to support it.</span></span>

  - <span data-ttu-id="d5c23-120">**1 つまたは複数のポリシーを構成して割り当てる**   外部ユーザーのアクセスをサポートするには、次のような要件に対応するようにポリシーを構成します。</span><span class="sxs-lookup"><span data-stu-id="d5c23-120">**Configure and assign one or more policies**   To support external user access, you configure policies to address requirements that include:</span></span>
    
      - <span data-ttu-id="d5c23-121">**外部アクセスポリシー**   サイトまたはユーザーのスコープで作成された (グローバルポリシーは既定で存在し、有効な設定はありません)。</span><span class="sxs-lookup"><span data-stu-id="d5c23-121">**External access policies**   Created with either a site or user scope (a global policy exists by default and has no enabled settings).</span></span> <span data-ttu-id="d5c23-122">フェデレーションされたユーザーアクセス (選択した場合はフェデレーションされた XMPP ドメイン)、リモートユーザーのユーザーアクセス、サポートされているパブリック IM サービスプロバイダーを含む、1つ以上の種類の外部ユーザーアクセスの使用を制御するポリシーを作成して構成します。</span><span class="sxs-lookup"><span data-stu-id="d5c23-122">You create and configure policies to control the use of one or more types of external user access, including, federated user access (including, if selected, federated XMPP domains)remote users user access, and supported public IM service providers.</span></span> <span data-ttu-id="d5c23-123">Lync Server コントロールパネルで、[**フェデレーション] と [外部アクセス**] グループの [**外部アクセスポリシー** ] ページで、グローバルポリシーまたは1つ以上の管理者が作成したサイトとユーザーポリシーを使用して、外部ポリシーを構成します。</span><span class="sxs-lookup"><span data-stu-id="d5c23-123">You configure external policies in Lync Server Control Panel using the global policy or one or more administratively created site and user policies, on the **External Access Policy** page in the **Federation and External Access** group.</span></span> <span data-ttu-id="d5c23-124">グローバルポリシーは削除できません。</span><span class="sxs-lookup"><span data-stu-id="d5c23-124">The global policy cannot be deleted.</span></span> <span data-ttu-id="d5c23-125">特定のサイトまたはユーザーに対して外部ユーザーのアクセスを制限するために使用するサイトとユーザーのポリシーを作成して構成します。</span><span class="sxs-lookup"><span data-stu-id="d5c23-125">You create and configure any site and user policies that you want to use to limit external user access for specific sites or users.</span></span> <span data-ttu-id="d5c23-126">グローバルポリシーとサイトポリシーが自動的に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="d5c23-126">Global and site policies are automatically assigned.</span></span> <span data-ttu-id="d5c23-127">ユーザーポリシーを作成して構成した場合は **、ユーザーのページの** Lync Server コントロールパネルにある [ユーザーの構成] ページを使用して、そのポリシーを特定のユーザーに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5c23-127">If you create and configure a user policy, you must then assign it to the specific users by using the user configuration page in the Lync Server Control Panel on the **Users** page.</span></span> <span data-ttu-id="d5c23-128">このポリシーを適用するユーザー (複数可) を見つけて、ポリシーを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="d5c23-128">Find the user or users that you want this policy to apply to and assign the policy.</span></span> <span data-ttu-id="d5c23-129">を選択します。</span><span class="sxs-lookup"><span data-stu-id="d5c23-129">to whom you want it to apply.</span></span> <span data-ttu-id="d5c23-130">構成済みのユーザーポリシーをユーザーに割り当てる方法については、「 [Lync Server 2013 で lync を有効にしたユーザーに外部ユーザーアクセスポリシーを割り当てる](lync-server-2013-assign-an-external-user-access-policy-to-a-lync-enabled-user.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5c23-130">To assign a configured user policy to a user, see [Assign an external user access policy to a Lync enabled user in Lync Server 2013](lync-server-2013-assign-an-external-user-access-policy-to-a-lync-enabled-user.md).</span></span> <span data-ttu-id="d5c23-131">各外部ユーザーアクセスポリシーは、リモートユーザーアクセス、SIP フェデレーションユーザーアクセス、XMPP フェデレーションユーザーアクセス、パブリック IM 接続をサポートできます。</span><span class="sxs-lookup"><span data-stu-id="d5c23-131">Each external user access policy can support one or more of the following: remote user access, SIP federated user access, XMPP federated user access and public IM connectivity.</span></span>
    
      - <span data-ttu-id="d5c23-132">**会議のポリシー**   組織内の会議を管理するためのポリシーを作成して構成します。組織内のユーザーは、ホストされている会議に匿名ユーザーを招待することができます。</span><span class="sxs-lookup"><span data-stu-id="d5c23-132">**Conferencing policies**   You create and configure policies to control conferencing in your organization, including which users in your organization can invite anonymous users to conferences that they host.</span></span> <span data-ttu-id="d5c23-133">Lync Server コントロールパネルの [ **会議** ] ページには、実際の会議の設定を制御するグローバル、サイト、ユーザーのスコープのポリシー設定があります。</span><span class="sxs-lookup"><span data-stu-id="d5c23-133">On the Lync Server Control Panel **Conferencing** page are policy settings at the global, site and user scope that control settings for the actual conferences.</span></span> <span data-ttu-id="d5c23-134">詳細については、「 [Lync Server 2013 での会議と会議の管理](lync-server-2013-managing-meetings-and-conferences.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5c23-134">For details, see [Managing meetings and conferences in Lync Server 2013](lync-server-2013-managing-meetings-and-conferences.md).</span></span> <span data-ttu-id="d5c23-135">[ **アクセスエッジの構成** ] ページで、会議、リモートユーザー、フェデレーションユーザーの匿名ユーザーを有効にします。</span><span class="sxs-lookup"><span data-stu-id="d5c23-135">You enable anonymous users for conferencing, remote users and federated users on the **Access Edge Configuration** page.</span></span> <span data-ttu-id="d5c23-136">**アクセスエッジ構成** のポリシーは、スコープ内でグローバルになります。</span><span class="sxs-lookup"><span data-stu-id="d5c23-136">The policy on the **Access Edge Configuration** is global in scope.</span></span> <span data-ttu-id="d5c23-137">サイトまたはユーザーのポリシーを定義するオプションはありません。</span><span class="sxs-lookup"><span data-stu-id="d5c23-137">There are no options to define a site or user policy.</span></span> <span data-ttu-id="d5c23-138">スコープは、グローバル、サイト、またはユーザーのポリシー設定を使用して、[ **外部アクセスポリシー** ] ページで制御されます。</span><span class="sxs-lookup"><span data-stu-id="d5c23-138">The scope is controlled on the **External Access Policy** page through the use of global, site, or user policy settings.</span></span>
        
        <span data-ttu-id="d5c23-139">たとえば、リモートユーザーとの会議の作成、招待、管理をユーザーに許可する場合は、[**外部アクセスポリシー** ] グローバル、サイト、またはユーザーのポリシーで **リモートユーザー** との通信を有効にするように設定し、[**アクセスエッジの構成**] ページで **リモートユーザーとの通信を有効** にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5c23-139">For example, if you want to allow users to create, invite and manage conferencing with remote users, you must set **Enable communications with remote users** on the **External Access Policy** global, site or user policy, and **Enable Communications with remote users** on the **Access Edge Configuration** page.</span></span> <span data-ttu-id="d5c23-140">同様に、匿名ユーザーやフェデレーションパートナーとの間に、定義されたリレーションシップが設定されている会議を許可するには (たとえば、構成されたフェデレーション SIP ドメインとプロバイダーは、電話会議をサポートしていません)、**パブリックユーザーとの通信を有効に** し、**外部アクセスポリシー** のグローバル、サイト、またはユーザーのポリシーで **フェデレーション**</span><span class="sxs-lookup"><span data-stu-id="d5c23-140">Similarly, to allow conferencing with anonymous users or federated partners that you have a defined relationship with (such as configured federated SIP domains and providers – XMPP federation does not support conferencing), you set **Enable communications with public users** and **Enable communications with federated users** in the **External Access Policy** global, site or user policy.</span></span> <span data-ttu-id="d5c23-141">次に、[無料グローバルポリシーの設定] を選択して、[**アクセスエッジ構成**] ページで、[**匿名ユーザーの会議へのアクセスを有効に** し、**フェデレーションとパブリック IM 接続を有効** にします。</span><span class="sxs-lookup"><span data-stu-id="d5c23-141">You then select complimentary global policy settings **Enable anonymous user access to conferences** and **Enable federated and public IM connectivity** on the **Access Edge Configuration** page.</span></span>

<span data-ttu-id="d5c23-142">外部ユーザーアクセスを制御するために使用するポリシーなど、組織の外部ユーザーアクセスを有効にしていない場合でも、外部ユーザーアクセスの設定を構成できます。</span><span class="sxs-lookup"><span data-stu-id="d5c23-142">You can configure external user access settings, including any policies that you want to use to control external user access, even if you have not enabled external user access for your organization.</span></span> <span data-ttu-id="d5c23-143">ただし、構成したポリシーとその他の設定は、組織で外部ユーザーのアクセスが有効になっている場合にのみ有効になります。</span><span class="sxs-lookup"><span data-stu-id="d5c23-143">However, the policies and other settings that you configure are in effect only when you have external user access enabled for your organization.</span></span> <span data-ttu-id="d5c23-144">外部ユーザーのアクセスが無効になっている場合、または外部ユーザーのアクセスポリシーがサポートされていない場合、外部ユーザーは組織のユーザーと通信できません。</span><span class="sxs-lookup"><span data-stu-id="d5c23-144">External users cannot communicate with users of your organization when external user access is disabled or if no external user access policies are configured to support it.</span></span>

<span data-ttu-id="d5c23-145">エッジの展開では、外部ユーザーの種類 (会議 ID によって認証された匿名ユーザーを除く) と、会議を作成して参加者を招待したときに匿名の参加者に送信されるパスキーを認証し、edge サポートの構成方法に基づいてアクセスを制御します。</span><span class="sxs-lookup"><span data-stu-id="d5c23-145">Your edge deployment authenticates the types of external users (except for anonymous users, who are authenticated by the conference ID and a passkey that is sent to the anonymous participant when you create the conference and invite participants) and controls access based on how you configure your edge support.</span></span> <span data-ttu-id="d5c23-146">通信を制御するために、1つまたは複数のポリシーを構成し、展開の内外のユーザーとの通信方法を定義する設定を構成することができます。</span><span class="sxs-lookup"><span data-stu-id="d5c23-146">In order to control communications, you can configure one or more policies and configure settings that define how users inside and outside your deployment communicate with each other.</span></span> <span data-ttu-id="d5c23-147">ポリシーと設定には、外部ユーザーアクセスの既定のグローバルポリシーに加えて、特定のサイトまたはユーザーに対して1つ以上の種類の外部ユーザーアクセスを有効にするために作成および構成できるサイトとユーザーのポリシーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d5c23-147">The policies and settings include the default global policy for external user access, in addition to site and user policies that you can create and configure to enable one or more types of external user access for specific sites or users.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="d5c23-148">このセクション中</span><span class="sxs-lookup"><span data-stu-id="d5c23-148">In This Section</span></span>

  - [<span data-ttu-id="d5c23-149">Lync Server 2013 でのリモート ユーザー アクセスを制御するポリシーの構成</span><span class="sxs-lookup"><span data-stu-id="d5c23-149">Configure policies to control remote user access in Lync Server 2013</span></span>](lync-server-2013-configure-policies-to-control-remote-user-access.md)

  - [<span data-ttu-id="d5c23-150">Lync Server 2013 でのリモート ユーザー アクセスの有効化または無効化</span><span class="sxs-lookup"><span data-stu-id="d5c23-150">Enable or disable remote user access in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-remote-user-access.md)

  - [<span data-ttu-id="d5c23-151">Lync Server 2013 匿名ユーザー アクセスの有効化または無効化</span><span class="sxs-lookup"><span data-stu-id="d5c23-151">Enable or disable anonymous user access in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-anonymous-user-access.md)

  - [<span data-ttu-id="d5c23-152">Lync Server 2013 での匿名ユーザー サポートのための会議ポリシーの割り当て</span><span class="sxs-lookup"><span data-stu-id="d5c23-152">Assign conferencing policies to support anonymous users in Lync Server 2013</span></span>](lync-server-2013-assign-conferencing-policies-to-support-anonymous-users.md)

<span data-ttu-id="d5c23-153"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d5c23-153"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

