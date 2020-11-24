---
title: 'Lync Server 2013: プライベート電話回線の計画'
description: 'Lync Server 2013: プライベート電話回線の計画'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for private telephone lines
ms:assetid: 9cc4f9e1-7b7a-4699-bd05-f16669ef2d21
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412728(v=OCS.15)
ms:contentKeyID: 48184909
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 120c1804bc3ce58e8746f68cbda9c66f02568ccb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400232"
---
# <a name="planning-for-private-telephone-lines-with-lync-server-2013"></a><span data-ttu-id="8ce89-103">Lync Server 2013 でのプライベート電話回線の計画</span><span class="sxs-lookup"><span data-stu-id="8ce89-103">Planning for private telephone lines with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8ce89-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8ce89-104">

<span> </span></span></span>

<span data-ttu-id="8ce89-105">_**最終更新日:** 2013-02-11_</span><span class="sxs-lookup"><span data-stu-id="8ce89-105">_**Topic Last Modified:** 2013-02-11_</span></span>

<span data-ttu-id="8ce89-106">Lync Server 2013 では、第2の私的な電話回線と、お客様の代表電話回線をユーザーに提供することができます。</span><span class="sxs-lookup"><span data-stu-id="8ce89-106">Lync Server 2013 introduces the ability to give users a second, private telephone line in addition to their primary telephone line.</span></span> <span data-ttu-id="8ce89-107">プライベート電話回線は、多くの場合、役員や直接受信できる非公開の電話番号が必要なユーザーに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="8ce89-107">Private telephone lines are often assigned to executives and others who want an unlisted telephone number at which they can be reached directly.</span></span>

<span data-ttu-id="8ce89-108">プライベート電話回線を構成するには、Lync Server 管理シェルを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8ce89-108">Private telephone lines can only be configured with the Lync Server Management Shell.</span></span> <span data-ttu-id="8ce89-109">Lync Server コントロールパネルでプライベート電話回線を構成することはできません。</span><span class="sxs-lookup"><span data-stu-id="8ce89-109">You cannot configure private telephone lines with the Lync Server Control Panel.</span></span> <span data-ttu-id="8ce89-110">プライベートな電話回線は、複数の展開ではなく、Lync Server の展開でのみ構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8ce89-110">Private telephone lines should be configured only in deployments of Lync Server and not in mixed deployments.</span></span>

<div>

## <a name="characteristics-of-private-telephone-lines"></a><span data-ttu-id="8ce89-111">プライベート電話回線の特徴</span><span class="sxs-lookup"><span data-stu-id="8ce89-111">Characteristics of Private Telephone Lines</span></span>

<span data-ttu-id="8ce89-112">セカンダリのプライベート電話回線の概念は基本的に単純なものですが、プライベート番号の特徴およびユーザーのプライマリ電話回線との類似点と相違点を理解することが重要です。</span><span class="sxs-lookup"><span data-stu-id="8ce89-112">Although the concept of a second, private telephone line is fundamentally simple, it is important to understand the characteristics of private lines and the ways in which they are similar to and different from users’ primary telephone lines.</span></span>

<div>

## <a name="general-characteristics-of-private-telephone-lines"></a><span data-ttu-id="8ce89-113">プライベート電話回線の一般的特徴</span><span class="sxs-lookup"><span data-stu-id="8ce89-113">General Characteristics of Private Telephone Lines</span></span>

  - <span data-ttu-id="8ce89-114">ユーザーに割り当てることができるプライベート電話回線は 1 つのみです。</span><span class="sxs-lookup"><span data-stu-id="8ce89-114">A user can have only one private telephone line.</span></span>

  - <span data-ttu-id="8ce89-115">プライベート電話回線が割り当てられたユーザーには、ボイス メール用メールボックスは 1 つのみ設定され、不在着信通知は 1 つの電子メール アドレスに通知されます。</span><span class="sxs-lookup"><span data-stu-id="8ce89-115">A user with a private telephone line has only one voice mailbox and receives missed call notifications at a single email address.</span></span>

  - <span data-ttu-id="8ce89-116">プライベート電話回線が割り当てられたユーザーに、2 番目の SIP アドレスは割り当てられません。また、セカンダリのプライベート電話回線によって、ユーザーにネットワーク上の 2 番目のプレゼンス (2 番目のインスタント メッセージング ID など) は付与されません。</span><span class="sxs-lookup"><span data-stu-id="8ce89-116">A user with a private telephone line does not have a second SIP address, and a second, private telephone line does not give a user a second presence on the network (such as a second instant messaging identity).</span></span>

  - <span data-ttu-id="8ce89-117">プライベート電話回線は、内部設置型展開でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="8ce89-117">Private telephone lines are available for on-premises deployments only.</span></span> <span data-ttu-id="8ce89-118">Lync Server のホスト型展開では使用できません。</span><span class="sxs-lookup"><span data-stu-id="8ce89-118">They are not available with hosted deployments of Lync Server.</span></span>

</div>

<div>

## <a name="how-private-telephone-lines-differ-from-primary-telephone-lines"></a><span data-ttu-id="8ce89-119">プライベート電話回線とプライマリ電話回線の相違点</span><span class="sxs-lookup"><span data-stu-id="8ce89-119">How Private Telephone Lines Differ from Primary Telephone Lines</span></span>

  - <span data-ttu-id="8ce89-120">プライベート電話回線の電話番号は、電話帳や Active Directory ドメイン サービスから得られる連絡先リストには表示されません。</span><span class="sxs-lookup"><span data-stu-id="8ce89-120">The telephone numbers for private telephone lines do not appear in the telephone directories or Contacts lists that are derived from Active Directory Domain Services.</span></span>

  - <span data-ttu-id="8ce89-121">プライベート電話回線では、着信の転送、チーム呼び出し、委任、チーム呼び出し、グループ通話ピックアップ、および応答グループ アプリケーションの機能は使用できません。</span><span class="sxs-lookup"><span data-stu-id="8ce89-121">None of the following features are available with a private telephone line: call forwarding, team call, delegation, team ring, Group Call Pickup, and Response Group application.</span></span>

  - <span data-ttu-id="8ce89-122">プライベート電話回線の呼び出しには特別な呼び出し音が設定され、呼び出しのシステム通知により、プライベート番号に着信通話があることがユーザーに通知されます。</span><span class="sxs-lookup"><span data-stu-id="8ce89-122">Calls to a private telephone line have a special ring, and the system notification for the call tells the user that the incoming call is on his or her private line.</span></span>

  - <span data-ttu-id="8ce89-p104">プライベート電話回線の呼び出しは、常に直接行われます。"応答不可" ルールには従いません。</span><span class="sxs-lookup"><span data-stu-id="8ce89-p104">Calls to the private telephone line always ring through. They do not follow "do not disturb" rules.</span></span>

  - <span data-ttu-id="8ce89-p105">プライベート電話回線は着信のみで、発信通話に使用することはできません。プライベート電話回線を割り当てられたユーザーが電話をかけた場合、その通話はユーザーのプライマリ電話回線から発信され、ユーザーの名前やプライマリ電話番号は通話先に対して非表示にはなりません。</span><span class="sxs-lookup"><span data-stu-id="8ce89-p105">Private telephone lines are inbound only and cannot be used to make outgoing calls. When a user with a private telephone line makes a call, the call originates from the user’s primary telephone line and does not hide the user’s name or the user’s primary telephone number from the person called.</span></span>

</div>

<div>

## <a name="how-private-telephone-lines-are-similar-to-primary-telephone-lines"></a><span data-ttu-id="8ce89-127">プライベート電話回線とプライマリ電話回線の類似点</span><span class="sxs-lookup"><span data-stu-id="8ce89-127">How Private Telephone Lines Are Similar to Primary Telephone Lines</span></span>

  - <span data-ttu-id="8ce89-128">プライベート電話回線の呼び出しで応答のなかったものは、プライマリ電話回線のものと同じボイス メール用受信ボックス (ボイス メールが有効になっている場合) にルーティングされます。</span><span class="sxs-lookup"><span data-stu-id="8ce89-128">Unanswered calls to a private telephone line are routed to the same voice mail inbox as for the primary telephone line (if voice mail is enabled).</span></span>

  - <span data-ttu-id="8ce89-129">コール パークとコール ピックアップは、ユーザーのプライマリ電話回線の場合とまったく同じ方法で、プライベート電話回線で機能します。</span><span class="sxs-lookup"><span data-stu-id="8ce89-129">Call park and call pickup work with private telephone lines in exactly the same manner as they do with the user’s primary telephone line.</span></span>

  - <span data-ttu-id="8ce89-130">ユーザーのプライマリ電話回線で同時呼び出しが有効になっている場合、プライベート電話回線でも有効になります。</span><span class="sxs-lookup"><span data-stu-id="8ce89-130">When simultaneous ringing is enabled on a user’s primary telephone line, it is also enabled on the private telephone line.</span></span>

  - <span data-ttu-id="8ce89-131">プライベート電話回線の電話番号は、ユーザーのプライマリ電話回線の電話番号と同じ方法で詳細な通話の記録に記録されますが、プライベート電話番号であることが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8ce89-131">The telephone number for a private telephone line is recorded in the call detail record in the same manner as the telephone number for a user’s primary telephone line, but with an indication that it is a private telephone number.</span></span>

  - <span data-ttu-id="8ce89-132">ユーザーがプライベート電話回線で通話に応答した場合、その通話はユーザーのプライマリ電話回線の通話と同じように処理されます。</span><span class="sxs-lookup"><span data-stu-id="8ce89-132">After a user answers a call on a private telephone line, the call is treated the same as a call on the user’s primary telephone line.</span></span> <span data-ttu-id="8ce89-133">たとえば、プライベート電話回線で通話を受信したユーザーが通話を転送したり、会議通話に他のユーザーを招待したりすると、ユーザーの名前が Lync 2013 に表示され、ユーザーのプライマリ電話回線の電話番号が発信者番号認識に表示されます。</span><span class="sxs-lookup"><span data-stu-id="8ce89-133">For example, if a user who receives a call on a private telephone line forwards the call or invites others to a conference call, the user’s name appears in Lync 2013, and the telephone number for the user’s primary telephone line appears in caller ID.</span></span>

  - <span data-ttu-id="8ce89-134">ユーザーは、プライマリ電話回線と同じ方法で、プライベート電話回線からの通話を切り替える (応答する前に、携帯電話や自宅の電話などの別の宛先に通話をリダイレクトする) ことができます。</span><span class="sxs-lookup"><span data-stu-id="8ce89-134">A user can deflect a call (redirect the call to another destination, such as a mobile phone or home phone, before answering) from the private telephone line in the same manner as with a primary telephone line.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="8ce89-135">プライベート番号の呼び出しが別の電話番号にルーティングされた場合、その別の電話番号でプライベート電話回線の電話番号を使用できるようになり、その番号のログを表示できます。</span><span class="sxs-lookup"><span data-stu-id="8ce89-135">When a call to a private line is routed to an alternate telephone number, the telephone number for the private telephone line is made available to the alternate telephone number and can be displayed in the logs for that number.</span></span>

    
    </div>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="8ce89-136">会議からプライベート電話回線への呼び出しでは、着信システム通知に<EM>プライベート番号</EM>表示は行われません。</span><span class="sxs-lookup"><span data-stu-id="8ce89-136">Calls from a conference to the private telephone line will not have a <EM>private-line</EM> indication in the incoming system notification.</span></span>

    
    </div>

</div>

</div>

<div>

## <a name="administering-private-telephone-lines"></a><span data-ttu-id="8ce89-137">プライベート電話回線の管理</span><span class="sxs-lookup"><span data-stu-id="8ce89-137">Administering Private Telephone Lines</span></span>

<span data-ttu-id="8ce89-p107">プライベート電話回線の作成および管理の技術的な側面に加えて、プライベート電話回線用の回線管理手順を設定する必要があります。これには、組織内のプライベート番号の対象ユーザー向けのポリシーの指定、それらのユーザーとその電話番号の一覧の作成および管理、役員のプライベート電話帳の作成、ユーザー トレーニングの調整、関連する作業などがあります。</span><span class="sxs-lookup"><span data-stu-id="8ce89-p107">In addition to the technical aspects of creating and managing private telephone lines, you will need to establish administrative procedures for them. This includes determining policies for who in the organization is eligible for a private line, creating and maintaining lists of people and their telephone lines, possibly creating a private telephone directory for executives, arranging for user training, and related tasks.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8ce89-p108">プライベート電話回線は、Active Directory にユーザー オブジェクトの msRTCSIP-PrivateLine 属性として格納されます。既定では、Authenticated Users グループのメンバーは、この属性に対して読み取りアクセスを持ちます。</span><span class="sxs-lookup"><span data-stu-id="8ce89-p108">The private telephone line is stored in Active Directory as an msRTCSIP-PrivateLine attribute on the user object. By default any member of the Authenticated Users group has read access to this attribute.</span></span>



</div>

<div>

## <a name="assigning-telephone-numbers"></a><span data-ttu-id="8ce89-142">電話番号の割り当て</span><span class="sxs-lookup"><span data-stu-id="8ce89-142">Assigning Telephone Numbers</span></span>

<span data-ttu-id="8ce89-143">専用の電話回線を必要とする新しいユーザーのアカウントは、Lync Server コントロールパネルまたは Lync Server 管理シェルを使用して、プライベート電話回線のないアカウントと同じ方法で作成されます。</span><span class="sxs-lookup"><span data-stu-id="8ce89-143">Accounts for new users who need private telephone lines are created in the same manner as accounts without private telephone lines, using Lync Server Control Panel or Lync Server Management Shell.</span></span>

<span data-ttu-id="8ce89-144">Lync Server 管理シェルで **set-csuser** コマンドレットを使用して、ユーザーのプライベート電話回線に電話番号を割り当てます。たとえば、 **Set-Csuser-Identity "Sip:joe@contoso.com"-PrivateLine "Tel: + 14255551212"**。</span><span class="sxs-lookup"><span data-stu-id="8ce89-144">Use the **Set-CsUser** cmdlet in the Lync Server Management Shell to assign a telephone number to a private telephone line for a user, for example, **Set-CsUser -Identity "sip:joe@contoso.com" -PrivateLine "Tel:+14255551212"**.</span></span>

<span data-ttu-id="8ce89-145">プライベート電話回線の電話番号には、3 ~ 15 個の番号を使用できます。また、前に "TEL:" プレフィックスを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8ce89-145">Telephone numbers for private telephone lines can be between 3 and 15 numbers in length and must be preceded with the "TEL:" prefix.</span></span> <span data-ttu-id="8ce89-146">組織で市外局番や国/地域コードに Direct Inward Dialing を使用している場合、その市外局番や国/地域コードを指定できます。</span><span class="sxs-lookup"><span data-stu-id="8ce89-146">They can have any area code and any country/region code as long as your organization has direct inward dialing for that area code and country/region code.</span></span>

<span data-ttu-id="8ce89-147">コマンドレットと Lync Server Management Shell の詳細については、「 [Lync server 2013 管理シェル](lync-server-2013-lync-server-management-shell.md) のドキュメント」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8ce89-147">For details about cmdlets and Lync Server Management Shell, see the [Lync Server 2013 Management Shell](lync-server-2013-lync-server-management-shell.md) documentation.</span></span>

</div>

<div>

## <a name="private-telephone-lines-in-mixed-deployments"></a><span data-ttu-id="8ce89-148">混在環境におけるプライベート電話回線</span><span class="sxs-lookup"><span data-stu-id="8ce89-148">Private Telephone Lines in Mixed Deployments</span></span>

<span data-ttu-id="8ce89-149">専用の電話回線は、Lync Server の展開用にのみ構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8ce89-149">Private telephone lines should be configured only for deployments of Lync Server.</span></span> <span data-ttu-id="8ce89-150">Lync Server と Office 2007 Communications server 2007 R2 サーバーの両方が含まれている展開では、以前のバージョンのユーザーがプライベート電話回線に電話をかけようとしたときに、サーバーがプライベート電話回線で逆引き番号参照を実行できないため、通話のルーティングが失敗します。</span><span class="sxs-lookup"><span data-stu-id="8ce89-150">In a deployment in which there are both Lync Server and Office Communications Server 2007 or Office Communications Server 2007 R2 servers, when a user on earlier version attempts to call a private telephone line, routing of the call fails because the server cannot perform a reverse number lookup on a private telephone line.</span></span>

<span data-ttu-id="8ce89-151"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8ce89-151"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

