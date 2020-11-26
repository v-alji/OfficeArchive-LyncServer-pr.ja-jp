---
title: 'Lync Server 2013: 公開 SIP フェデレーション プロバイダーの作成または編集'
description: 'Lync Server 2013: パブリック SIP フェデレーションプロバイダーを作成または編集します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or edit public SIP federated providers
ms:assetid: 5321598c-1ab1-40e3-b739-4b2e6d0a3a3b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398349(v=OCS.15)
ms:contentKeyID: 48184167
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c0ef5850b5e8016e0bd90512db45c2917c16a104
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431877"
---
# <a name="create-or-edit-public-sip-federated-providers-in-lync-server-2013"></a><span data-ttu-id="45d27-103">Lync Server 2013 での公開 SIP フェデレーション プロバイダーの作成または編集</span><span class="sxs-lookup"><span data-stu-id="45d27-103">Create or edit public SIP federated providers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="45d27-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="45d27-104">

<span> </span></span></span>

<span data-ttu-id="45d27-105">_**最終更新日:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="45d27-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="45d27-106">パブリックインスタントメッセージング (IM) 接続を使うと、組織内のユーザーは IM を使用して、Windows Live Messenger、Yahoo、AOL など、パブリック IM サービスプロバイダーが提供する IM サービスのユーザーと通信でき \! ます。</span><span class="sxs-lookup"><span data-stu-id="45d27-106">Public instant messaging (IM) connectivity enables users in your organization to use IM to communicate with users of IM services provided by public IM service providers, including the Windows Live Messenger, Yahoo\!, and AOL.</span></span>

<span data-ttu-id="45d27-107">Lync Server 2013 には、America Online、Windows Live、Yahoo 用のパブリックプロバイダー構成があります。\!</span><span class="sxs-lookup"><span data-stu-id="45d27-107">Lync Server 2013 has public provider configurations for America Online, Windows Live and Yahoo\!</span></span> <span data-ttu-id="45d27-108">インスタントメッセージ (im)。</span><span class="sxs-lookup"><span data-stu-id="45d27-108">instant messaging.</span></span> <span data-ttu-id="45d27-109">各パブリックプロバイダーは、プロバイダーのエッジサーバーの完全修飾ドメイン名で構成され、既定の認証レベルでは、 **このプロバイダーを使用する連絡先リストのユーザーのみとの通信を許可** します。</span><span class="sxs-lookup"><span data-stu-id="45d27-109">Each public provider is configured with the provider’s Edge server fully qualified domain name, and the default verification level **Allow users to communicate only with people on their Contacts list who use this provider**.</span></span>

<span data-ttu-id="45d27-110">既定の設定では、どのパブリックプロバイダーも有効になっていません。</span><span class="sxs-lookup"><span data-stu-id="45d27-110">As a default setting, none of the public providers are enabled.</span></span> <span data-ttu-id="45d27-111">パブリックプロバイダーを有効にする前に、ライセンス契約とプロビジョニング作業を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="45d27-111">You should complete license agreement and provisioning work before enabling the public providers.</span></span> <span data-ttu-id="45d27-112">ライセンスとプロビジョニングの作業を完了する前に、プロバイダーを有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="45d27-112">You can enable the provider before completing the licensing and provisioning work.</span></span> <span data-ttu-id="45d27-113">ユーザーは、前提条件となる作業が完了するまで、これらのプロバイダーの連絡先と通信できません。</span><span class="sxs-lookup"><span data-stu-id="45d27-113">Users will not be able to communicate with contacts on those providers until the pre-requisite work is completed.</span></span> <span data-ttu-id="45d27-114">パブリックプロバイダーのライセンスとプロビジョニングの詳細については、「 [Lync Server 2013 でパブリックユーザーアクセスを制御するためのポリシーを構成する](lync-server-2013-configure-policies-to-control-public-user-access.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="45d27-114">For details on licensing and provisioning of public providers, see [Configure policies to control public user access in Lync Server 2013](lync-server-2013-configure-policies-to-control-public-user-access.md).</span></span>

<span data-ttu-id="45d27-115">パブリックプロバイダーを作成または編集するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="45d27-115">Use the following procedure to create or edit Public providers:</span></span>

<div>

## <a name="to-create-or-edit-public-providers"></a><span data-ttu-id="45d27-116">パブリックプロバイダーを作成または編集するには</span><span class="sxs-lookup"><span data-stu-id="45d27-116">To create or edit public providers</span></span>

1.  <span data-ttu-id="45d27-117">RTCUniversalServerAdmins グループ (または同等のユーザー権限を持つグループ) のメンバーであるユーザー アカウントまたは CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="45d27-117">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="45d27-118">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="45d27-118">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="45d27-119">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="45d27-119">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="45d27-120">左側のナビゲーションバーで、[ **フェデレーションと外部アクセス**] をクリックし、[ **SIP フェデレーションプロバイダー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="45d27-120">In the left navigation bar, click **Federation and External Access**, and then click **SIP Federated Providers**.</span></span>

4.  <span data-ttu-id="45d27-121">新しいパブリックプロバイダーを作成する必要がある場合は、[ **新規** ] をクリックし、[ **パブリックプロバイダー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="45d27-121">If you need to create a new Public provider, click **New** and then click **Public provider**.</span></span>

5.  <span data-ttu-id="45d27-122">パブリックプロバイダーの一覧からエントリを編集する必要がある場合は、パブリックプロバイダーを選択し、[ **編集**] をクリックして、[ **詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="45d27-122">If you need to edit an entry from the list of Public providers, select a public provider, click **Edit**, then click **Show details**.</span></span>

6.  <span data-ttu-id="45d27-123">[ **SIP フェデレーションプロバイダーの編集** ] ページでは、次の設定を入力または編集できます。</span><span class="sxs-lookup"><span data-stu-id="45d27-123">On the **Edit SIP Federated Provider** page, you can type or edit the following settings:</span></span>
    
      - <span data-ttu-id="45d27-124">**このプロバイダーとの通信を有効にする**   この設定を選択すると、このプロバイダーのユーザーとの IM が有効になります。</span><span class="sxs-lookup"><span data-stu-id="45d27-124">**Enable communications with this provider**   Selecting this setting enables IM with this provider’s users.</span></span>
    
      - <span data-ttu-id="45d27-125">**プロバイダー名:**   必要なプロパティ。 SIP フェデレーションプロバイダーの一覧に反映されるプロバイダーの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="45d27-125">**Provider name:**   A required property, type the name of the provider as it will be reflected in the listing of SIP Federated Providers.</span></span>
    
      - <span data-ttu-id="45d27-126">**Access Edge サービス (FQDN):**   必要なプロパティ。構成しているプロバイダーのアクセスエッジサービスの完全修飾ドメイン名を入力します。</span><span class="sxs-lookup"><span data-stu-id="45d27-126">**Access Edge service (FQDN):**   A required property, type the fully qualified domain name of the Access Edge service of the provider that you are configuring.</span></span> <span data-ttu-id="45d27-127">この情報は既定の項目として提供され、パブリックプロバイダーがアクセスエッジサービスの FQDN に変更を加えた場合にのみ変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="45d27-127">This information is provided as a default item, and should only be changed if the public provider makes a change to the FQDN of the Access Edge service at the public provider.</span></span>
    
      - <span data-ttu-id="45d27-128">**既定の確認レベル:**   既定の設定では、ユーザーが連絡先リストに登録されているユーザー **との通信を許可すること** によって、このプロバイダーを使用している場合は、連絡先リストに登録されている連絡先への通信が制限されます。</span><span class="sxs-lookup"><span data-stu-id="45d27-128">**Default verification level:**   The default setting, **Allow users to communicate with people on their Contacts list who use this provider** will limit communication to contacts that you have accepted and are in your contact list.</span></span>
        
        <span data-ttu-id="45d27-129">[ **このプロバイダーを使用するすべてのユーザーとの通信を許可する** ] を選択すると、連絡先への招待を受信して受け付けるために必要な制限が解除されます。</span><span class="sxs-lookup"><span data-stu-id="45d27-129">Selecting **Allow users to communicate with everyone using this provider** removes the restriction that you must have received and accepted a contact invite.</span></span> <span data-ttu-id="45d27-130">この設定では、パブリックプロバイダーのネットワークから連絡できるユーザーを制限することはできません。</span><span class="sxs-lookup"><span data-stu-id="45d27-130">This setting does not limit who can contact you from the public provider’s network.</span></span>

7.  <span data-ttu-id="45d27-131">設定の構成が完了したら、[ **確定** ] をクリックするか、[ **キャンセル** ] をクリックして変更を破棄します。</span><span class="sxs-lookup"><span data-stu-id="45d27-131">When you are done configuring the settings, click **Commit** to save, or click **Cancel** to discard your changes.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="45d27-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="45d27-132">See Also</span></span>


[<span data-ttu-id="45d27-133">Lync Server 2013 でのパブリック ユーザー アクセスを制御するポリシーの構成</span><span class="sxs-lookup"><span data-stu-id="45d27-133">Configure policies to control public user access in Lync Server 2013</span></span>](lync-server-2013-configure-policies-to-control-public-user-access.md)  
[<span data-ttu-id="45d27-134">Lync Server 2013 でのフェデレーションおよびパブリック IM 接続の有効化または無効化</span><span class="sxs-lookup"><span data-stu-id="45d27-134">Enable or disable federation and public IM connectivity in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md)  
  

<span data-ttu-id="45d27-135"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="45d27-135"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

