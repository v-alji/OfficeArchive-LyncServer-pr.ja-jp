---
title: Lync Server 2013 電話会議
description: Lync Server 2013 会議。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conferencing
ms:assetid: 6129b7e0-9abd-488e-a54e-86094eb9df7a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg417161(v=OCS.15)
ms:contentKeyID: 48184274
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7d4a5f1ca1edc6246aace56c8a4bfa5b5215c4bc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434257"
---
# <a name="conferencing-in-lync-server-2013"></a><span data-ttu-id="3850e-103">Lync Server 2013 電話会議</span><span class="sxs-lookup"><span data-stu-id="3850e-103">Conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3850e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3850e-104">

<span> </span></span></span>

<span data-ttu-id="3850e-105">_**最終更新日:** 2012-09-11_</span><span class="sxs-lookup"><span data-stu-id="3850e-105">_**Topic Last Modified:** 2012-09-11_</span></span>

<span data-ttu-id="3850e-106">Lync Server 2013 の統合会議を使用すると、ユーザーはリアルタイムで共同作業、情報の共有、作業の調整を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="3850e-106">With unified conferencing in Lync Server 2013, users can collaborate, share information, and coordinate their efforts in real time.</span></span> <span data-ttu-id="3850e-107">すべてのユーザーが、突然のコラボレーション、予約された会議、会議ツールを使用できます。</span><span class="sxs-lookup"><span data-stu-id="3850e-107">All your users can use the full breadth of spontaneous collaboration, scheduled meetings, and meeting tools.</span></span> <span data-ttu-id="3850e-108">音声およびビデオ会議機能は、インターネット接続があればどこからでも使うことができます。また、コンピューターに接続していないユーザーは、公衆交換電話網 (PSTN) を使ってダイヤルインして電話会議に参加することができます。</span><span class="sxs-lookup"><span data-stu-id="3850e-108">Voice and video conferencing capabilities can be used from any location with an Internet connection, and users away from a computer can participate in audio conferences by dialing in with a public switched telephone network (PSTN) phone.</span></span>

<span data-ttu-id="3850e-109">Outlook に統合された会議ツールを使用すると、開催者は1回のクリックで会議のスケジュールを設定したり、一時的な会議を開始したりできます。また、出席者が参加できるようになります。</span><span class="sxs-lookup"><span data-stu-id="3850e-109">Meeting tools integrated into Outlook enable organizers to schedule a meeting or start an impromptu conference with a single click, and also make it just as easy for attendees to join.</span></span> <span data-ttu-id="3850e-110">Web クライアントは、デスクトップ版の Lync を実行していない参加者に、豊富な会議機能を拡張します。</span><span class="sxs-lookup"><span data-stu-id="3850e-110">A web client extends rich conference features to participants who are not running the desktop version of Lync.</span></span>

<div>

## <a name="audio-and-video-conferencing"></a><span data-ttu-id="3850e-111">音声ビデオ会議</span><span class="sxs-lookup"><span data-stu-id="3850e-111">Audio and Video Conferencing</span></span>

<span data-ttu-id="3850e-112">Lync Server は、PSTN ダイヤルインサービスなどの従来のオーディオブリッジサービス (タッチトーン通話制御コマンドを含む) のユーザーに使い慣れたユーザーエクスペリエンスを提供します。</span><span class="sxs-lookup"><span data-stu-id="3850e-112">Lync Server provides a user experience that is familiar to users of traditional audio bridge services including PSTN dial-in services with touch-tone call control commands.</span></span> <span data-ttu-id="3850e-113">同時に、統合された統合コミュニケーションプラットフォームでのみ利用できる強力なスケジューリング、参加、管理機能が組み込まれています。</span><span class="sxs-lookup"><span data-stu-id="3850e-113">At the same time, it incorporates powerful scheduling, joining, and management features available only with an integrated unified communications platform.</span></span>

<span data-ttu-id="3850e-114">1回のクリックで、ユーザーは Outlook から会議をスケジュールできます。</span><span class="sxs-lookup"><span data-stu-id="3850e-114">With a single click, users can schedule a meeting from Outlook.</span></span> <span data-ttu-id="3850e-115">会議の時間、場所、出席者などの詳細情報は、使い慣れた Outlook テンプレートに従います。</span><span class="sxs-lookup"><span data-stu-id="3850e-115">Details, such as meeting time, location, and attendees, follow the familiar Outlook template.</span></span> <span data-ttu-id="3850e-116">さらに、ダイヤルイン番号、会議 Id、暗証番号 (PIN) リマインダーなどの会議通話固有の情報が自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="3850e-116">Additionally, conference call-specific information, such as dial-in number, meeting IDs, and personal identification number (PIN) reminders, are automatically populated.</span></span>

<span data-ttu-id="3850e-117">Lync Server では、承認されたユーザーのみが通話に参加できるようにするために、参加者に対して複数レベルの認証を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="3850e-117">To help ensure that only the authorized people participate in a call, Lync Server provides multiple levels of authentication for participants.</span></span> <span data-ttu-id="3850e-118">Lync を使用して参加しているユーザーは、Active Directory ドメインサービスによって既に認証されていますが、PIN、パスコード、または会議 ID を入力する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="3850e-118">Users who join by using Lync are already authenticated by the Active Directory Domain Services and do not need to enter a PIN, pass code, or meeting ID.</span></span>

<span data-ttu-id="3850e-119">Lync では、ビデオを統合クライアントに組み込み、ビデオ通話やビデオ通話のスケジュール設定がシームレスで簡単になるように、ビデオ会議のユーザーエクスペリエンスを簡素化します。</span><span class="sxs-lookup"><span data-stu-id="3850e-119">Lync simplifies the video conferencing user experience by incorporating video into the unified client so that scheduling a meeting with video or escalating to video spontaneously is seamless and easy.</span></span>

<span data-ttu-id="3850e-120">Lync Server を使用すると、ワンクリックで標準の通話にビデオを簡単に追加することができます。</span><span class="sxs-lookup"><span data-stu-id="3850e-120">Lync Server makes it easy to add video to a standard phone call in just one click.</span></span> <span data-ttu-id="3850e-121">ビデオ通話または会議に複数の参加者がいる場合、各ユーザーは、同時に最大5人のユーザーからのビデオを表示できます。また、発表者は、誰でも見ることができるビデオソースを1つだけ選ぶことができます。</span><span class="sxs-lookup"><span data-stu-id="3850e-121">When there are multiple participants in a video call or a conference, each user can see video from up to five other users simultaneously, or a presenter can choose just one video source to be seen exclusively by everyone.</span></span>

<span data-ttu-id="3850e-122">高解像度ビデオ (解像度 1270 x 720、縦横比 16:9) と VGA ビデオ (解像度 640 x 480、縦横比 4:3) は、ハイエンドコンピューターで Lync を実行しているユーザー間のピアツーピア通話でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="3850e-122">High-definition video (resolution 1270 x 720; aspect ratio 16:9) and VGA video (resolution 640 x 480; aspect ratio 4:3) are supported for peer-to-peer calls between users running Lync on high-end computers.</span></span> <span data-ttu-id="3850e-123">1つの会話で各参加者によって表示される解像度は、各ユーザーの各ハードウェアのビデオ機能によって異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="3850e-123">The resolution viewed by each participant in a single conversation may differ, depending on the video capabilities of each user’s respective hardware.</span></span>

<span data-ttu-id="3850e-124">IT 管理者は、コンピューターの機能、ネットワークの帯域幅、カメラの存在の有無に応じて、高解像度または VGA ビデオを設定して、必要な解像度を実現するようにポリシーを設定できます。</span><span class="sxs-lookup"><span data-stu-id="3850e-124">IT administrators can set policies to restrict or disable high-definition or VGA video on clients, depending on computer capability, network bandwidth, and the presence of a camera able to deliver the required resolution.</span></span> <span data-ttu-id="3850e-125">これらのポリシーは、インバンドプロビジョニングによって適用されます。</span><span class="sxs-lookup"><span data-stu-id="3850e-125">These policies are enforced through in-band provisioning.</span></span>

</div>

<div>

## <a name="web-conferencing"></a><span data-ttu-id="3850e-126">Web 会議</span><span class="sxs-lookup"><span data-stu-id="3850e-126">Web conferencing</span></span>

<span data-ttu-id="3850e-127">Lync Server は、デスクトップ、アプリケーション、添付ファイル、ホワイトボード、投票、PowerPoint などの会議共有機能を、効率化された Lync に統合します。</span><span class="sxs-lookup"><span data-stu-id="3850e-127">Lync Server integrates conferencing sharing features such as desktop, application, attachment, whiteboard, poll and PowerPoint into the streamlined Lync.</span></span> <span data-ttu-id="3850e-128">音声会議やビデオ会議と組み合わせると、非常に簡単に使いやすくなります。</span><span class="sxs-lookup"><span data-stu-id="3850e-128">Combined with audio or video conferencing, the result is a highly immersive and collaborative session that is simple to facilitate.</span></span>

<span data-ttu-id="3850e-129">Lync Server 2013 は、PowerPoint プレゼンテーションを表示または表示するユーザーエクスペリエンス全体を向上させるために、Office Web Apps を採用して PowerPoint プレゼンテーションを処理します。</span><span class="sxs-lookup"><span data-stu-id="3850e-129">To improve the overall experience of users presenting or viewing PowerPoint presentations, Lync Server 2013 employs Office Web Apps to handle PowerPoint presentations.</span></span> <span data-ttu-id="3850e-130">ユーザーは、Lync 会議のホワイトボードを使って、画像の共有やテキストのコピーと貼り付けを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="3850e-130">Users can share a picture or copy and paste text using a Whiteboard in the Lync meeting.</span></span> <span data-ttu-id="3850e-131">発表者は、Lync 会議で投票を実施して、出席者からのフィードバックを得ることができます。</span><span class="sxs-lookup"><span data-stu-id="3850e-131">Presenters can conduct polls in the Lync meeting to solicit feedback from the attendees.</span></span>

<span data-ttu-id="3850e-132">デスクトップ共有では、発表者はビジュアル、アプリケーション、web ページ、ドキュメント、ソフトウェア、またはデスクトップの一部を Lync から直接、リアルタイムでブロードキャストすることができます。</span><span class="sxs-lookup"><span data-stu-id="3850e-132">Desktop sharing enables presenters to broadcast any visuals, applications, webpages, documents, software, or part of their desktops to remote participants in real time, right from Lync.</span></span> <span data-ttu-id="3850e-133">参加者メンバーは、マウスの動きとキーボード入力を使ってフォローすることができます。</span><span class="sxs-lookup"><span data-stu-id="3850e-133">Audience members can follow along with mouse movements and keyboard input.</span></span> <span data-ttu-id="3850e-134">発表者は、画面全体を共有するか、一部のみを共有するかを選ぶことができます。</span><span class="sxs-lookup"><span data-stu-id="3850e-134">Presenters can choose to share the entire screen or only a portion.</span></span> <span data-ttu-id="3850e-135">デスクトップを共有することで、発表者は、任意の場所からインタラクティブな製品またはソフトウェアのデモで対象ユーザーに参加することができます。</span><span class="sxs-lookup"><span data-stu-id="3850e-135">By sharing their desktops, presenters are able to engage with their audiences in interactive product or software demos from any location.</span></span>

<span data-ttu-id="3850e-136">アプリケーション共有を有効にすると、発表者は、参加者のフィードバックやテキストに関する質問を失うことなく、デスクトップ上のソフトウェアの制御を共有することができます。</span><span class="sxs-lookup"><span data-stu-id="3850e-136">Application sharing enables presenters to share control of software on their desktops without losing sight of participant feedback or text questions.</span></span> <span data-ttu-id="3850e-137">発表者は、アプリケーションの制御を会議参加者に委任することもできます。</span><span class="sxs-lookup"><span data-stu-id="3850e-137">Presenters can also delegate control of the application to meeting participants.</span></span>

</div>

<div>

## <a name="dial-in-conferencing"></a><span data-ttu-id="3850e-138">ダイヤルイン会議</span><span class="sxs-lookup"><span data-stu-id="3850e-138">Dial-in Conferencing</span></span>

<span data-ttu-id="3850e-139">個人のコンピューターを使用していないユーザーの場合は、Lync Server の電話会議に参加するために使用できる方法がいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="3850e-139">For users that are not using a personal computer, there are several methods available for joining a Lync Server conference call.</span></span> <span data-ttu-id="3850e-140">PSTN ユーザーは、アクセス番号をダイヤルし、会議ブリッジにアクセスして、会議 ID を入力することができます。</span><span class="sxs-lookup"><span data-stu-id="3850e-140">A PSTN user can dial an access number, access the meeting bridge, and then enter the meeting ID.</span></span> <span data-ttu-id="3850e-141">セキュリティで保護された会議の場合は、ユーザーは PIN を入力して Active Directory に対して認証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3850e-141">For more secure meetings, the user can also be required to enter his or her PIN to authenticate against Active Directory.</span></span> <span data-ttu-id="3850e-142">Lync Server は、Microsoft パートナーによって提供されるスタンドアロンの IP 電話デバイスである Lync Phone Edition デバイスもサポートしています。</span><span class="sxs-lookup"><span data-stu-id="3850e-142">Lync Server also supports Lync Phone Edition devices, which are stand-alone IP phone devices provided by Microsoft partners.</span></span>

<span data-ttu-id="3850e-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3850e-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

