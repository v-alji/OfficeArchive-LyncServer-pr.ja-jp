---
title: 'Lync Server 2013: ホスト型ボイス メールに対するユーザーの有効化'
description: 'Lync Server 2013: ホストされているボイスメールのユーザーを有効にします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable users for hosted voice mail
ms:assetid: fa559f8f-ef99-43a1-b580-9e998b95efb8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413062(v=OCS.15)
ms:contentKeyID: 48185919
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3853a70d433c09029a02f2ca6256b5988defdcb2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437470"
---
# <a name="enable-users-for-hosted-voice-mail-in-lync-server-2013"></a><span data-ttu-id="bfced-103">Lync Server 2013 でのホスト型ボイス メールに対するユーザーの有効化</span><span class="sxs-lookup"><span data-stu-id="bfced-103">Enable users for hosted voice mail in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bfced-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bfced-104">

<span> </span></span></span>

<span data-ttu-id="bfced-105">_**最終更新日:** 2012-09-24_</span><span class="sxs-lookup"><span data-stu-id="bfced-105">_**Topic Last Modified:** 2012-09-24_</span></span>

<span data-ttu-id="bfced-106">手順に従って、ホストされている Exchange ユニファイドメッセージング (UM) サービスで Lync Server 2013 ユーザーのボイスメールを有効にします。</span><span class="sxs-lookup"><span data-stu-id="bfced-106">Follow the procedure to enable Lync Server 2013 users for voice mail on a hosted Exchange Unified Messaging (UM) service.</span></span>

<span data-ttu-id="bfced-107">詳細については、計画ドキュメントの「 [Lync Server 2013 でのホスト型 Exchange ユーザーの管理](lync-server-2013-hosted-exchange-user-management.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bfced-107">For details, see [Hosted Exchange user management in Lync Server 2013](lync-server-2013-hosted-exchange-user-management.md) in the Planning documentation.</span></span>

<span data-ttu-id="bfced-108">[Set-CsUser](https://docs.microsoft.com/powershell/module/skype/Set-CsUser)コマンドレットの詳細については、「Lync Server 管理シェルのドキュメント」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bfced-108">For details about the [Set-CsUser](https://docs.microsoft.com/powershell/module/skype/Set-CsUser) cmdlet, see the Lync Server Management Shell documentation.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="bfced-109">ホストされたボイスメールに対して Lync Server 2013 ユーザーを有効にする前に、ユーザーアカウントに適用されるホスト型ボイスメールのポリシーを展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bfced-109">Before a Lync Server 2013 user can be enabled for hosted voice mail, a hosted voice mail policy that applies to their user account must be deployed.</span></span> <span data-ttu-id="bfced-110">詳細については、「 <A href="lync-server-2013-hosted-voice-mail-policies.md">Lync Server 2013 のホスト型ボイスメールポリシー</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bfced-110">For details, see <A href="lync-server-2013-hosted-voice-mail-policies.md">Hosted voice mail policies in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-enable-users-for-hosted-voice-mail"></a><span data-ttu-id="bfced-111">ユーザーがホストされたボイスメールを有効にするには</span><span class="sxs-lookup"><span data-stu-id="bfced-111">To enable users for hosted voice mail</span></span>

1.  <span data-ttu-id="bfced-112">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfced-112">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="bfced-113">Set-CsUser コマンドレットを実行して、ホストされたボイスメールのユーザーアカウントを構成します。</span><span class="sxs-lookup"><span data-stu-id="bfced-113">Run the Set-CsUser cmdlet to configure the user account for hosted voice mail.</span></span> <span data-ttu-id="bfced-114">たとえば、以下を実行します。</span><span class="sxs-lookup"><span data-stu-id="bfced-114">For example, run:</span></span>
    
        Set-CsUser -HostedVoiceMail $True -Identity "contoso\kenmyer"
    
    <span data-ttu-id="bfced-115">上述の例では、次のパラメーターが設定されます。</span><span class="sxs-lookup"><span data-stu-id="bfced-115">The preceding example sets the following parameters:</span></span>
    
      - <span data-ttu-id="bfced-116">**HostedVoiceMail** を使用すると、ユーザーのボイスメール通話を、ホスティングされている Exchange UM にルーティングすることができます。</span><span class="sxs-lookup"><span data-stu-id="bfced-116">**HostedVoiceMail** enables a user’s voice mail calls to be routed to hosted Exchange UM.</span></span> <span data-ttu-id="bfced-117">また、Microsoft Lync 2013 には、"ボイスメールの呼び出し" インジケーターが表示されるように通知されます。</span><span class="sxs-lookup"><span data-stu-id="bfced-117">It also signals Microsoft Lync 2013 to light up the “call voice mail” indicator.</span></span>
    
      - <span data-ttu-id="bfced-118">**Id** は、変更するユーザーアカウントを指定します。</span><span class="sxs-lookup"><span data-stu-id="bfced-118">**Identity** specifies the user account to be modified.</span></span> <span data-ttu-id="bfced-119">Id 値は、次の形式のいずれかを使用して指定できます。</span><span class="sxs-lookup"><span data-stu-id="bfced-119">The Identity value can be specified using any of the following formats:</span></span>
        
          - <span data-ttu-id="bfced-120">ユーザーの SIP アドレス</span><span class="sxs-lookup"><span data-stu-id="bfced-120">The user's SIP address</span></span>
        
          - <span data-ttu-id="bfced-121">ユーザーの Active Directory ユーザープリンシパル名</span><span class="sxs-lookup"><span data-stu-id="bfced-121">The user's Active Directory User-Principal-Name</span></span>
        
          - <span data-ttu-id="bfced-122">ユーザーのドメイン \\ ログオン名 (たとえば、contoso \\ kenmyer)</span><span class="sxs-lookup"><span data-stu-id="bfced-122">The user's domain\\logon name (for example, contoso\\kenmyer)</span></span>
        
          - <span data-ttu-id="bfced-123">ユーザーの Active Directory ドメインサービス Display-Name (Ken Myer など)。</span><span class="sxs-lookup"><span data-stu-id="bfced-123">The user's Active Directory Domain Services Display-Name (for example, Ken Myer).</span></span> <span data-ttu-id="bfced-124">Display-Name を Id 値として使用する場合は、アスタリスク ( \* ) ワイルドカード文字を使用できます。</span><span class="sxs-lookup"><span data-stu-id="bfced-124">If using the Display-Name as the Identity value, you can use the asterisk (\*) wildcard character.</span></span> <span data-ttu-id="bfced-125">たとえば、"smith" という Id を指定すると、" \* smith" という文字列で終わる Display-Name を持つすべてのユーザーが返されます。</span><span class="sxs-lookup"><span data-stu-id="bfced-125">For example, the Identity "\* Smith" returns all the users who have a Display-Name that ends with the string value "Smith".</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="bfced-126">SAM アカウント名はフォレスト内で必ずしも一意ではないため、ユーザーの Active Directory SAM アカウント名を Id 値として使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="bfced-126">The user’s Active Directory SAM-Account-Name cannot be used as the Identity value because the SAM-Account-Name is not necessarily unique in the forest.</span></span>

        
        <span data-ttu-id="bfced-127"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bfced-127"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

