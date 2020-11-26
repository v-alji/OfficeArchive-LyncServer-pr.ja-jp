---
title: 'Lync Server 2013: 会議の移行に関する考慮事項'
description: 'Lync Server 2013: 会議の移行に関する考慮事項'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migration considerations for meetings
ms:assetid: a9807d58-99a3-4cff-b4c6-74950d106a2b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412800(v=OCS.15)
ms:contentKeyID: 61097556
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e238405acf7bc2a96fd2efd4cca761c1f1f258fd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425585"
---
# <a name="migration-considerations-for-meetings-in-lync-server-2013"></a><span data-ttu-id="ce861-103">Lync Server 2013 での会議の移行に関する考慮事項</span><span class="sxs-lookup"><span data-stu-id="ce861-103">Migration considerations for meetings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ce861-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ce861-104">

<span> </span></span></span>

<span data-ttu-id="ce861-105">_**最終更新日:** 2014-02-10_</span><span class="sxs-lookup"><span data-stu-id="ce861-105">_**Topic Last Modified:** 2014-02-10_</span></span>

<span data-ttu-id="ce861-106">このセクションでは、次のトピックについて説明します。</span><span class="sxs-lookup"><span data-stu-id="ce861-106">The following topics are discussed in this section:</span></span>

  - <span data-ttu-id="ce861-107">Microsoft Lync Server 2013 での会議の変更点</span><span class="sxs-lookup"><span data-stu-id="ce861-107">Changes to meetings in Microsoft Lync Server 2013</span></span>

  - <span data-ttu-id="ce861-108">会議のニーズに基づいてユーザーを移行する</span><span class="sxs-lookup"><span data-stu-id="ce861-108">Migrating users based on their conferencing needs</span></span>

  - <span data-ttu-id="ce861-109">既存の会議と会議コンテンツの移行</span><span class="sxs-lookup"><span data-stu-id="ce861-109">Migrating existing meetings and meeting content</span></span>

  - <span data-ttu-id="ce861-110">Lync Server 2010 の移行中のユーザーエクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="ce861-110">User experience during Lync Server 2010 migration</span></span>

  - <span data-ttu-id="ce861-111">Office Communications Server 2007 R2 の移行中のユーザーエクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="ce861-111">User Experience during Office Communications Server 2007 R2 migration</span></span>

  - <span data-ttu-id="ce861-112">Microsoft Lync 2013 以前のバージョンのサーバーの会議との互換性</span><span class="sxs-lookup"><span data-stu-id="ce861-112">Microsoft Lync 2013 compatibility with meetings on earlier server versions</span></span>

<div>

## <a name="changes-to-meetings-in-lync-server-2013"></a><span data-ttu-id="ce861-113">Lync Server 2013 での会議の変更点</span><span class="sxs-lookup"><span data-stu-id="ce861-113">Changes to Meetings in Lync Server 2013</span></span>

<span data-ttu-id="ce861-114">**Lync Server 2013 の機能。**</span><span class="sxs-lookup"><span data-stu-id="ce861-114">**Lync Server 2013 features.**</span></span>   <span data-ttu-id="ce861-115">Lync Server 2013 には、アカウントを Lync Server 2013 に移行した後でユーザーが利用できる新しい会議機能が用意されています。また、lync 2013 クライアントでサインインします。</span><span class="sxs-lookup"><span data-stu-id="ce861-115">Lync Server 2013 provides new conferencing features that become available to users after their accounts are moved to Lync Server 2013 and they sign in with the Lync 2013 client.</span></span> <span data-ttu-id="ce861-116">新しい機能については、「 [Lync server 2013 の新しい会議機能](lync-server-2013-new-conferencing-features.md) 」と「 [lync server 2013 でのクライアントの新](lync-server-2013-what-s-new-for-clients.md)機能」で説明しています。</span><span class="sxs-lookup"><span data-stu-id="ce861-116">New features are outlined in [New conferencing features in Lync Server 2013](lync-server-2013-new-conferencing-features.md) and [What's new for clients in Lync Server 2013](lync-server-2013-what-s-new-for-clients.md).</span></span>

<span data-ttu-id="ce861-117">**会議の URL。**</span><span class="sxs-lookup"><span data-stu-id="ce861-117">**Meeting URL.**</span></span>   <span data-ttu-id="ce861-118">Lync Server 2010 の場合と同様に、Lync Server 2013 で新しくスケジュールされた会議には、https://の URL プレフィックスと、既存の会議がユーザーアカウントと共に移行されます。</span><span class="sxs-lookup"><span data-stu-id="ce861-118">As in Lync Server 2010, all newly scheduled meetings in Lync Server 2013 have a URL prefix of https:// and existing meetings migrate along with user accounts.</span></span> <span data-ttu-id="ce861-119">ただし、Lync Server 2013 は、Office Communications Server 2007 R2 会議通話 (conf://URL プレフィックス) または web 会議 (meet://URL プレフィックス) をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="ce861-119">However, Lync Server 2013 does not support the Office Communications Server 2007 R2 conference call (conf:// URL prefix) or web conference (meet:// URL prefix).</span></span> <span data-ttu-id="ce861-120">詳細については、このトピックの後半の「Office Communications Server 2007 R2 から会議を移行する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ce861-120">See “Migrating Meetings from Office Communications Server 2007 R2” later in this topic for more information.</span></span>

<span data-ttu-id="ce861-121">**クライアントのサポート。**</span><span class="sxs-lookup"><span data-stu-id="ce861-121">**Client support.**</span></span>   <span data-ttu-id="ce861-122">Lync server 2010 とは異なり、Lync Server 2013 では、会議用の Office Communicator クライアントはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="ce861-122">Unlike Lync Server 2010, Lync Server 2013 does not support Office Communicator clients for conferencing.</span></span> <span data-ttu-id="ce861-123">Lync 2013 用のオンライン会議アドインによってスケジュールされた会議に、次のクライアントを使用して会議に参加することはできません。</span><span class="sxs-lookup"><span data-stu-id="ce861-123">You cannot use the following clients to join meetings scheduled through the Online Meeting Add-in for Lync 2013:</span></span>

  - <span data-ttu-id="ce861-124">Office Communicator 2007 R2</span><span class="sxs-lookup"><span data-stu-id="ce861-124">Office Communicator 2007 R2</span></span>

  - <span data-ttu-id="ce861-125">Microsoft Office Communications Server 2007 R2 Attendant</span><span class="sxs-lookup"><span data-stu-id="ce861-125">Microsoft Office Communications Server 2007 R2 Attendant</span></span>

  - <span data-ttu-id="ce861-126">Office Communicator 2007</span><span class="sxs-lookup"><span data-stu-id="ce861-126">Office Communicator 2007</span></span>

  - <span data-ttu-id="ce861-127">Office Live Meeting 2007</span><span class="sxs-lookup"><span data-stu-id="ce861-127">Office Live Meeting 2007</span></span>

<span data-ttu-id="ce861-128">Office Communicator 2007 R2 ユーザーは、移行中に Lync Web App 2013 を使って Lync Server 2013 会議に参加してから、顧客がアップグレードされるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ce861-128">During migration, Office Communicator 2007 R2 users should use Lync Web App 2013 to join Lync Server 2013 meetings until their clients are upgraded.</span></span> <span data-ttu-id="ce861-129">Office Communicator 2007 R2 ユーザーは、プレゼンスおよび IM 機能については、引き続き Lync Server 2013 に対して既存のクライアントを使用できますが、会議機能はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="ce861-129">Note that Office Communicator 2007 R2 users can continue to use their existing client against Lync Server 2013 for presence and IM features, but conferencing features are not supported.</span></span>

<div>


</div>

</div>

<div>

## <a name="migrating-users-based-on-their-conferencing-needs"></a><span data-ttu-id="ce861-130">会議のニーズに基づいてユーザーを移行する</span><span class="sxs-lookup"><span data-stu-id="ce861-130">Migrating Users Based on Their Conferencing Needs</span></span>

<span data-ttu-id="ce861-131">**会議の開催者の頻度。**</span><span class="sxs-lookup"><span data-stu-id="ce861-131">**Frequent meeting organizers.**</span></span>   <span data-ttu-id="ce861-132">Lync server [2013 の新しい会議機能](lync-server-2013-new-conferencing-features.md) で示されている新しい lync server 2013 および lync 2013 の機能を利用できるように、また、 [lync server 2013 でのクライアントの新](lync-server-2013-what-s-new-for-clients.md)機能を活用できるように、プロセスの早い段階で会議の開催者を頻繁に移行することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="ce861-132">Consider migrating frequent meeting organizers early in the process so that they can take advantage of the new Lync Server 2013 and Lync 2013 features outlined in [New conferencing features in Lync Server 2013](lync-server-2013-new-conferencing-features.md) and [What's new for clients in Lync Server 2013](lync-server-2013-what-s-new-for-clients.md).</span></span>

<span data-ttu-id="ce861-133">**Live Meeting ユーザー。**</span><span class="sxs-lookup"><span data-stu-id="ce861-133">**Live Meeting users.**</span></span>   <span data-ttu-id="ce861-134">Office Communications Server 2007 R2 から移行する場合、Live Meeting 固有の web 会議機能 (特に大規模な会議や休憩室のサポート) が必要なユーザーがいる場合は、次のオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="ce861-134">If you are migrating from Office Communications Server 2007 R2 and you have users who need web conferencing features specific to Live Meeting—particularly support for large meetings and break-out rooms—you have the following options:</span></span>

  - <span data-ttu-id="ce861-135">組織で利用できる場合は、Live Meeting サービスを使用するように開催者に通知します。</span><span class="sxs-lookup"><span data-stu-id="ce861-135">Advise organizers to use the Live Meeting service, if available in your organization.</span></span>

  - <span data-ttu-id="ce861-136">サーバーベースの Live Meeting web 会議のスケジュールを維持できるように、以前のバージョンの Office Communications Server の開催者をホームにしておきます。</span><span class="sxs-lookup"><span data-stu-id="ce861-136">Leave the organizers homed on the earlier version of Office Communications Server, so they can continue to schedule server-based Live Meeting web conferences.</span></span>

</div>

<div>

## <a name="migrating-existing-meetings-and-meeting-content"></a><span data-ttu-id="ce861-137">既存の会議と会議コンテンツの移行</span><span class="sxs-lookup"><span data-stu-id="ce861-137">Migrating Existing Meetings and Meeting Content</span></span>

<div>

## <a name="migrating-meetings-from-lync-server-2010"></a><span data-ttu-id="ce861-138">Lync Server 2010 から会議を移行する</span><span class="sxs-lookup"><span data-stu-id="ce861-138">Migrating Meetings from Lync Server 2010</span></span>

<span data-ttu-id="ce861-139">Lync Server 2010 から Lync Server 2013 にユーザーを移動すると、次の情報がユーザーのアカウントと共に移動します。</span><span class="sxs-lookup"><span data-stu-id="ce861-139">When you move a user from Lync Server 2010 to Lync Server 2013, the following information moves with the user’s account:</span></span>

  - <span data-ttu-id="ce861-140">ユーザーが既にスケジュールした会議。</span><span class="sxs-lookup"><span data-stu-id="ce861-140">Meetings already scheduled by the user.</span></span> <span data-ttu-id="ce861-141">これには、会議ディレクトリと会議データが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ce861-141">This includes conferencing directories and conferencing data.</span></span>

  - <span data-ttu-id="ce861-142">ユーザーの暗証番号 (PIN)。</span><span class="sxs-lookup"><span data-stu-id="ce861-142">The user’s personal identification number (PIN).</span></span> <span data-ttu-id="ce861-143">ユーザーの現在の PIN は、有効期限が切れるか、ユーザーが新しい PIN を要求するまで、引き続き動作します。</span><span class="sxs-lookup"><span data-stu-id="ce861-143">The user’s current PIN continues to work until it expires or the user requests a new PIN.</span></span>

<span data-ttu-id="ce861-144">ただし、次のユーザーアカウント情報は新しいサーバーに移動されません。</span><span class="sxs-lookup"><span data-stu-id="ce861-144">However, the following user account information does not move to the new server:</span></span>

  - <span data-ttu-id="ce861-145">会議コンテンツ (PowerPoint プレゼンテーション、ホワイトボードコンテンツ、投票データなど)</span><span class="sxs-lookup"><span data-stu-id="ce861-145">Meeting content, for example PowerPoint presentations, whiteboard content, and poll data</span></span>

<span data-ttu-id="ce861-146">会議で共有されているコンテンツを移動するには、Move-CsUser コマンドレットの MoveMeetingContent パラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="ce861-146">To move the content that has been shared in meetings, use the MoveMeetingContent parameter of the Move-CsUser cmdlet.</span></span> <span data-ttu-id="ce861-147">このコマンドレットの使い方の詳細については、「Lync Server 2013 コマンドレットのドキュメントでの [移動-CsUser](https://docs.microsoft.com/powershell/module/skype/Move-CsUser) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ce861-147">For details about using this cmdlet, see [Move-CsUser](https://docs.microsoft.com/powershell/module/skype/Move-CsUser) in the Lync Server 2013 cmdlets documentation.</span></span>

</div>

<div>

## <a name="migrating-meetings-from-office-communications-server-2007-r2"></a><span data-ttu-id="ce861-148">Office Communications Server 2007 R2 から会議を移行する</span><span class="sxs-lookup"><span data-stu-id="ce861-148">Migrating Meetings from Office Communications Server 2007 R2</span></span>

<span data-ttu-id="ce861-149">Office Communications Server 2007 R2 会議は、会議通話 (conf://URL プレフィックス) または web 会議 (meet://URL プレフィックス) のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="ce861-149">Office Communications Server 2007 R2 meetings are either conference calls (conf:// URL prefix) or web conferences (meet:// URL prefix).</span></span> <span data-ttu-id="ce861-150">Lync Server 2013 では、これらの以前の conf://と meet://の会議はサポートされておらず、ユーザーアカウントと共に移行されることはありません。</span><span class="sxs-lookup"><span data-stu-id="ce861-150">Lync Server 2013 does not support these earlier conf:// and meet:// conferences, and they are not migrated along with the user account.</span></span> <span data-ttu-id="ce861-151">移行後は、スケジュールしたオンライン会議のリンクを更新するようにユーザーに指示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ce861-151">After migration, you should instruct users to update the links for any online meetings they have scheduled.</span></span> <span data-ttu-id="ce861-152">この操作を行うには、スケジュールされた会議出席依頼を開き、会議の URL を更新し、参加者に招待状を再送信して、Lync 2013 クライアントをインストールします。</span><span class="sxs-lookup"><span data-stu-id="ce861-152">They can do this after installing the Lync 2013 client by opening a scheduled meeting invitation—which updates the meeting URL—and resending the invitation to participants.</span></span>

</div>

</div>

<div>

## <a name="user-experience-during-lync-server-2010-migration"></a><span data-ttu-id="ce861-153">Lync Server 2010 の移行中のユーザーエクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="ce861-153">User Experience during Lync Server 2010 Migration</span></span>

<span data-ttu-id="ce861-154">このセクションでは、Lync 2010 から移行する場合のユーザーの会議エクスペリエンスの概要について説明します。</span><span class="sxs-lookup"><span data-stu-id="ce861-154">This section provides a summary of users’ conferencing experience when migrating from Lync 2010.</span></span> <span data-ttu-id="ce861-155">Lync Server 2013 クライアントで、以前のクライアントとサーバーのバージョンを共存して操作する方法の詳細については、「 [lync 2013 でのクライアントの相互運用性](lync-server-2013-client-interoperability-in-lync-2013.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ce861-155">For more details about how Lync Server 2013 clients can coexist and interact with previous client and server versions, see [Client interoperability in Lync 2013](lync-server-2013-client-interoperability-in-lync-2013.md).</span></span>

<div>

## <a name="joining-lync-server-2010-meetings-with-a-lync-2013-client"></a><span data-ttu-id="ce861-156">Lync 2013 クライアントを使って Lync Server 2010 会議に参加する</span><span class="sxs-lookup"><span data-stu-id="ce861-156">Joining Lync Server 2010 Meetings with a Lync 2013 Client</span></span>

<span data-ttu-id="ce861-157">Lync Server 2010 からの移行中に、ユーザーが lync 2013 クライアントを使って Lync Server 2010 会議に参加すると、共存期間が延長される場合があります。</span><span class="sxs-lookup"><span data-stu-id="ce861-157">During migration from Lync Server 2010, there may be a period of coexistence when users join Lync Server 2010 meetings with a Lync 2013 client.</span></span> <span data-ttu-id="ce861-158">これらのユーザーは、次の例外を除き、Lync 2013 クライアント機能にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="ce861-158">These users have access to Lync 2013 client features with the following exceptions:</span></span>

  - <span data-ttu-id="ce861-159">[会議] ウィンドウの [連絡先] アイコンをポイントしてアクセスできる **参加者** の管理オプションでは、[ **会議 IM** を使わない] オプションは機能しません。</span><span class="sxs-lookup"><span data-stu-id="ce861-159">In the **Participants** management options, which are accessible by pointing to the people icon in the meeting window, the **No Meeting IM** option does not function.</span></span>

  - <span data-ttu-id="ce861-160">ギャラリービューは、ビデオ会議では機能しません。</span><span class="sxs-lookup"><span data-stu-id="ce861-160">Gallery View does not function in video conferences.</span></span> <span data-ttu-id="ce861-161">ユーザーは、すべてのスピーカーではなく、アクティブなスピーカーのみを表示します。</span><span class="sxs-lookup"><span data-stu-id="ce861-161">The user sees only the active speaker instead of all speakers.</span></span> <span data-ttu-id="ce861-162">[ **レイアウトの選択** ] オプションの一覧で、 **ギャラリービュー** を使用できない</span><span class="sxs-lookup"><span data-stu-id="ce861-162">In the list of **Pick a Layout** options, **Gallery View** is unavailable</span></span>

  - <span data-ttu-id="ce861-163">参加者リストは、ビデオ会議の既定で表示されます。</span><span class="sxs-lookup"><span data-stu-id="ce861-163">The participant list displays by default in video conferences.</span></span>

  - <span data-ttu-id="ce861-164">[参加者] リストでユーザーを右クリックすると、[ **ビデオスポットライトをロック** する] と [ **ギャラリーに参加するための Pin** ] オプションは使用できません。</span><span class="sxs-lookup"><span data-stu-id="ce861-164">When right-clicking a user in the participants list, the **Lock the Video Spotlight** and **Pin to Gallery** participant management options are unavailable.</span></span>

</div>

</div>

<div>

## <a name="user-experience-during-office-communications-server-2007-r2-migration"></a><span data-ttu-id="ce861-165">Office Communications Server 2007 R2 の移行中のユーザーエクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="ce861-165">User Experience during Office Communications Server 2007 R2 Migration</span></span>

<span data-ttu-id="ce861-166">このセクションでは、Lync 2013 がインストールされている前と後の両方で、Office Communications Server 2007 R2 から移行するユーザーの会議エクスペリエンスの概要について説明します。</span><span class="sxs-lookup"><span data-stu-id="ce861-166">This section provides a summary of users’ conferencing experience when migrating from Office Communications Server 2007 R2, both before and after Lync 2013 is installed.</span></span> <span data-ttu-id="ce861-167">Lync Server 2013 クライアントで、以前のクライアントとサーバーのバージョンを共存して操作する方法の詳細については、「 [lync 2013 でのクライアントの相互運用性](lync-server-2013-client-interoperability-in-lync-2013.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ce861-167">For more details about how Lync Server 2013 clients can coexist and interact with previous client and server versions, see [Client interoperability in Lync 2013](lync-server-2013-client-interoperability-in-lync-2013.md).</span></span>

<div>

## <a name="after-user-account-is-migrated-before-lync-2013-is-installed"></a><span data-ttu-id="ce861-168">ユーザーアカウントが移行された後、Lync 2013 がインストールされる前</span><span class="sxs-lookup"><span data-stu-id="ce861-168">After User Account is Migrated, Before Lync 2013 Is Installed</span></span>

<span data-ttu-id="ce861-169">ユーザーが Lync Server 2013 サーバーに移行された後、新しいクライアントがインストールされる前に、Office Communicator 2007 R2 ユーザーは、プレゼンスおよび IM 機能のために、Lync Server 2013 に対して既存のクライアントを引き続き使用できますが、会議機能はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="ce861-169">After a user is migrated to the Lync Server 2013 server, but before new clients are installed, Office Communicator 2007 R2 users can continue to use their existing client against Lync Server 2013 for presence and IM features, but conferencing features are not supported.</span></span>

</div>

<div>

## <a name="after-user-account-is-migrated-after-lync-2013-is-installed"></a><span data-ttu-id="ce861-170">ユーザーアカウントが移行された後、Lync 2013 をインストールした後</span><span class="sxs-lookup"><span data-stu-id="ce861-170">After User Account is Migrated, After Lync 2013 Is Installed</span></span>

<span data-ttu-id="ce861-171">移行したユーザーが Lync 2013 をインストールすると、Lync 2013 用のオンライン会議アドインもインストールされます。</span><span class="sxs-lookup"><span data-stu-id="ce861-171">When a migrated user installs Lync 2013, the Online Meeting Add-in for Lync 2013 is installed too.</span></span> <span data-ttu-id="ce861-172">これには、次のような効果があります。</span><span class="sxs-lookup"><span data-stu-id="ce861-172">This has the following effects:</span></span>

  - <span data-ttu-id="ce861-173">以降のスケジュールされた会議では、新しい会議の形式が使用されます。これにより、従来の meet://Live Meeting のアドレスではなく、https://の住所が使用されます。</span><span class="sxs-lookup"><span data-stu-id="ce861-173">All subsequently scheduled meetings use the new meeting format, which uses an https:// address instead of the legacy meet:// Live Meeting address.</span></span>

  - <span data-ttu-id="ce861-174">Lync 2013 の IT 管理展開では、管理者は Microsoft Office Outlook 用の会議アドインをアンインストールすることができます。これは、Live Meeting server とサービスベースの会議をスケジュールするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ce861-174">In an IT-managed deployment of Lync 2013, the administrator has the option of uninstalling the Conferencing Add-in for Microsoft Office Outlook, which is used to schedule Live Meeting server and service-based meetings.</span></span> <span data-ttu-id="ce861-175">ただし、Live Meeting サービス会議を継続してスケジュールする必要があるユーザーがいる場合があります。</span><span class="sxs-lookup"><span data-stu-id="ce861-175">However, you may have users who need to continue to schedule Live Meeting service meetings.</span></span> <span data-ttu-id="ce861-176">この場合は、両方のアドインを共存させることができます。</span><span class="sxs-lookup"><span data-stu-id="ce861-176">In this case, you can allow both add-ins to coexist.</span></span>

</div>

<div>

## <a name="meetings-with-federated-organizations-that-use-previous-clients"></a><span data-ttu-id="ce861-177">以前のクライアントを使用するフェデレーション組織との会議</span><span class="sxs-lookup"><span data-stu-id="ce861-177">Meetings with Federated Organizations that Use Previous Clients</span></span>

<span data-ttu-id="ce861-178">Microsoft Office Communicator 2007 を使用しているフェデレーション組織のユーザーは、会議が開催者によってロックされている場合、組織内の Lync Server 2013 会議に参加することはできません。</span><span class="sxs-lookup"><span data-stu-id="ce861-178">Users in federated organizations who are using Microsoft Office Communicator 2007 cannot join Lync Server 2013 meetings in your organization if those meetings are locked by the organizer.</span></span> <span data-ttu-id="ce861-179">会議の出席者が新しい https://会議の URL を使って会議に参加するときに、lync Web App を使うことができるように、Lync Server 2013 でこれらの会議のスケジュールを再設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ce861-179">You have to reschedule these meetings in Lync Server 2013 so when federated participants join the meeting by using the new https:// meeting URL, they can use Lync Web App.</span></span>

<span data-ttu-id="ce861-180"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ce861-180"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

