---
title: 'Lync Server 2013: クライアント向けの新機能'
description: 'Lync Server 2013: クライアントの新機能'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: What's new for clients
ms:assetid: 5c144677-4d58-4fc3-8445-74b76c9fcf07
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204933(v=OCS.15)
ms:contentKeyID: 48184253
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 90c1b93666b556c7ce7c4f3d94bea583dbf9b1a1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398925"
---
# <a name="whats-new-for-clients-in-lync-server-2013"></a><span data-ttu-id="f7297-103">Lync Server 2013 のクライアント向けの新機能</span><span class="sxs-lookup"><span data-stu-id="f7297-103">What's new for clients in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f7297-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f7297-104">

<span> </span></span></span>

<span data-ttu-id="f7297-105">_**最終更新日:** 2013-02-19_</span><span class="sxs-lookup"><span data-stu-id="f7297-105">_**Topic Last Modified:** 2013-02-19_</span></span>

<span data-ttu-id="f7297-106">Microsoft Lync 2013 には、再設計されたユーザーインターフェイスと重要な新機能があります。</span><span class="sxs-lookup"><span data-stu-id="f7297-106">Microsoft Lync 2013 has a redesigned user interface and important new features.</span></span> <span data-ttu-id="f7297-107">管理者の場合は、Office のセットアッププログラムにクライアントが含まれており、Office を展開して組織内のクライアントをカスタマイズする方法がより効率的になりました。</span><span class="sxs-lookup"><span data-stu-id="f7297-107">For administrators, the client is now included with the Office setup program, providing a more streamlined approach to deploying Office and customizing clients in your organization.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f7297-108">Lync 2013 ユーザーインターフェイスの更新の表示方法については、「Lync 2013 の新機能」を参照してください <A href="https://go.microsoft.com/fwlink/?linkid=273885">https://go.microsoft.com/fwlink/?LinkId=273885</A> 。</span><span class="sxs-lookup"><span data-stu-id="f7297-108">For an illustrated view of Lync 2013 user interface updates, see “What’s New in Lync 2013” at <A href="https://go.microsoft.com/fwlink/?linkid=273885">https://go.microsoft.com/fwlink/?LinkId=273885</A>.</span></span>



</div>

<div>

## <a name="integration-with-office-setup"></a><span data-ttu-id="f7297-109">Office のセットアップとの統合</span><span class="sxs-lookup"><span data-stu-id="f7297-109">Integration with Office Setup</span></span>

<span data-ttu-id="f7297-110">Lync 2013 クライアントと Lync 2013 用のオンライン会議アドイン (Outlook メッセージングおよびコラボレーションクライアントでの会議管理をサポート) は、両方とも Office 2013 セットアッププログラムに含まれています。</span><span class="sxs-lookup"><span data-stu-id="f7297-110">The Lync 2013 client and the Online Meeting Add-in for Lync 2013—which supports meeting management from within the Outlook messaging and collaboration client—are now both included with the Office 2013 Setup program.</span></span>

<span data-ttu-id="f7297-111">以前のバージョンの Lync と Office Communicator では、Windows インストーラーのプロパティを使用して、Office のインストールをカスタマイズおよび制御することができます。</span><span class="sxs-lookup"><span data-stu-id="f7297-111">In previous versions of Lync and Office Communicator, you could use Windows Installer properties to customize and control the Office installation.</span></span> <span data-ttu-id="f7297-112">Lync 2013 は Office セットアップと統合されているため、Lync 2013 のセットアップをカスタマイズするには、次の方法を使用できます。</span><span class="sxs-lookup"><span data-stu-id="f7297-112">Because Lync 2013 is integrated with Office setup, you can use the following methods to customize Lync 2013 setup:</span></span>

  - <span data-ttu-id="f7297-113">Office カスタマイズ ツール (OCT) を使用する</span><span class="sxs-lookup"><span data-stu-id="f7297-113">Use the Office Customization Tool (OCT)</span></span>

  - <span data-ttu-id="f7297-114">Config.xml を使用してインストールタスクを実行する</span><span class="sxs-lookup"><span data-stu-id="f7297-114">Use the Config.xml to perform installation tasks</span></span>

  - <span data-ttu-id="f7297-115">セットアップ Command-Line オプションを使用する</span><span class="sxs-lookup"><span data-stu-id="f7297-115">Use Setup Command-Line Options</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f7297-116">Lync 2013 セットアッププログラムでは、以前のバージョンの Lync や Office Communicator はアンインストールされません。</span><span class="sxs-lookup"><span data-stu-id="f7297-116">The Lync 2013 setup program does not uninstall previous versions of Lync or Office Communicator.</span></span> <span data-ttu-id="f7297-117">Lync 2013 クライアントは、他の Lync または Office Communicator クライアントと並行してインストールされます。</span><span class="sxs-lookup"><span data-stu-id="f7297-117">The Lync 2013 client installs side-by-side with other Lync or Office Communicator clients</span></span>



</div>

<span data-ttu-id="f7297-118">詳細については、「lync [Server 2013 での lync クライアントの展開](lync-server-2013-deploying-lync-clients.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f7297-118">For details, see [Deploying Lync clients in Lync Server 2013](lync-server-2013-deploying-lync-clients.md).</span></span>

</div>

<div>

## <a name="group-policy-deployment"></a><span data-ttu-id="f7297-119">グループポリシーの展開</span><span class="sxs-lookup"><span data-stu-id="f7297-119">Group Policy Deployment</span></span>

<span data-ttu-id="f7297-120">Lync 2013 は Office のセットアップに含まれるようになったため、Lync グループポリシー設定を展開するための方法が変更されました。</span><span class="sxs-lookup"><span data-stu-id="f7297-120">Because Lync 2013 is now included in Office setup, the method for deploying Lync Group Policy settings has changed.</span></span> <span data-ttu-id="f7297-121">以前のバージョンの Lync と Office Communicator では、Microsoft Communicator を使用してグループポリシー設定を定義できますが、Lync 2013 では、Lync ADMX および ADML 管理用テンプレートを使用して、Office グループポリシー管理用テンプレートと共に提供されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="f7297-121">In previous versions of Lync and Office Communicator, you could use the Communicator.adm to define Group Policy settings, whereas in Lync 2013 you can now use the Lync ADMX and ADML administrative templates that are provided along with the Office Group Policy Administrative Templates.</span></span>

<span data-ttu-id="f7297-122">詳細については、「 [Lync 2013 のグループポリシー設定](lync-server-2013-group-policy-settings-for-lync-2013.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f7297-122">For details, see [Group Policy settings for Lync 2013](lync-server-2013-group-policy-settings-for-lync-2013.md).</span></span>

</div>

<div>

## <a name="outlook-scheduling-add-in-updates"></a><span data-ttu-id="f7297-123">Outlook のスケジュールによるアドインの更新</span><span class="sxs-lookup"><span data-stu-id="f7297-123">Outlook Scheduling Add-in Updates</span></span>

<span data-ttu-id="f7297-124">Lync 2013 用のオンライン会議アドインには、会議出席依頼のカスタマイズと新しい会議のオプションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f7297-124">The Online Meeting Add-in for Lync 2013 includes meeting invite customization and new meeting options.</span></span>

  - <span data-ttu-id="f7297-125">管理者は、カスタムロゴ、サポート URL、法的免責事項 URL、またはカスタムフッターテキストを追加して、組織の会議出席依頼をカスタマイズすることができます。</span><span class="sxs-lookup"><span data-stu-id="f7297-125">Administrators can customize the organization’s meeting invitations by adding a custom logo, a support URL, a legal disclaimer URL, or custom footer text.</span></span> <span data-ttu-id="f7297-126">詳細については、「 [Lync Server 2013 でオンライン会議アドインをカスタマイズする](lync-server-2013-customizing-the-online-meeting-add-in.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f7297-126">For details, see [Customizing the Online Meeting Add-in in Lync Server 2013](lync-server-2013-customizing-the-online-meeting-add-in.md).</span></span>

  - <span data-ttu-id="f7297-127">新しい出席者のミュートコントロールを使うと、会議の開催者は、出席者の音声とビデオが既定でミュートになっている会議をスケジュールできます。</span><span class="sxs-lookup"><span data-stu-id="f7297-127">New attendee mute controls allow meeting organizers to schedule conferences that have attendee audio and video muted by default.</span></span>

</div>

<div>

## <a name="virtual-desktop-infrastructure-plug-in"></a><span data-ttu-id="f7297-128">仮想デスクトップインフラストラクチャプラグイン</span><span class="sxs-lookup"><span data-stu-id="f7297-128">Virtual Desktop Infrastructure Plug-in</span></span>

<span data-ttu-id="f7297-129">Lync 2013 クライアントは、仮想デスクトップインフラストラクチャ (VDI) 環境での音声とビデオをサポートするようになりました。</span><span class="sxs-lookup"><span data-stu-id="f7297-129">The Lync 2013 client now supports audio and video in a Virtual Desktop Infrastructure (VDI) environment.</span></span> <span data-ttu-id="f7297-130">ユーザーは、オーディオデバイスやビデオデバイス (ヘッドセットやカメラなど) をローカルコンピューター (たとえば、シンクライアントや転用コンピューター) に接続できます。</span><span class="sxs-lookup"><span data-stu-id="f7297-130">A user can connect an audio or video device (for example, a headset or a camera) to the local computer (for example, a thin client or repurposed computer).</span></span> <span data-ttu-id="f7297-131">ユーザーは、仮想マシンに接続して、仮想マシンで実行されている Lync 2013 クライアントにサインインし、クライアントがローカルで実行されている場合と同じように、リアルタイムの音声およびビデオ通信に参加できます。</span><span class="sxs-lookup"><span data-stu-id="f7297-131">The user can connect to the virtual machine, sign in to the Lync 2013 client that is running on the virtual machine, and participate in real-time audio and video communication as though the client is running locally.</span></span> <span data-ttu-id="f7297-132">仮想デスクトップ環境では、次の機能がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="f7297-132">The following features are supported in a virtual desktop environment:</span></span>

  - <span data-ttu-id="f7297-133">オーディオとビデオのデバイスの統合。以下を含む。</span><span class="sxs-lookup"><span data-stu-id="f7297-133">Device integration for audio and video, including the following:</span></span>
    
      - <span data-ttu-id="f7297-134">デバイスからコントロールを呼び出す</span><span class="sxs-lookup"><span data-stu-id="f7297-134">Call controls from the device</span></span>
    
      - <span data-ttu-id="f7297-135">デバイスでのプレゼンスの統合</span><span class="sxs-lookup"><span data-stu-id="f7297-135">Presence integration on the device</span></span>
    
      - <span data-ttu-id="f7297-136">複数の HID (ヒューマンインターフェイスデバイス) のサポート</span><span class="sxs-lookup"><span data-stu-id="f7297-136">Multiple HID (human interface device) support</span></span>

  - <span data-ttu-id="f7297-137">場所と緊急サービスのサポート。</span><span class="sxs-lookup"><span data-stu-id="f7297-137">Location and emergency services support.</span></span>

  - <span data-ttu-id="f7297-138">IM、音声、ビデオ、アプリケーション共有、デスクトップ共有、PowerPoint 共有、ホワイトボード、ファイル送信など、すべての Lync モダリティのサポート。</span><span class="sxs-lookup"><span data-stu-id="f7297-138">Support for all Lync modalities, including IM, audio, video, application sharing, desktop sharing, PowerPoint sharing, whiteboard, and file transfer.</span></span>

  - <span data-ttu-id="f7297-139">個人間の通話や電話会議での音声とビデオのサポート。</span><span class="sxs-lookup"><span data-stu-id="f7297-139">Audio and video support in person-to-person calls and conference calls.</span></span>

<span data-ttu-id="f7297-140">VDI プラグインの展開について詳しくは、「 [Lync Server 2013 での LYNC VDI プラグインの展開](lync-server-2013-deploying-the-lync-vdi-plug-in.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="f7297-140">For information about deploying the VDI plug-in, see [Deploying the Lync VDI plug-in in Lync Server 2013](lync-server-2013-deploying-the-lync-vdi-plug-in.md).</span></span>

</div>

<div>

## <a name="video-enhancements"></a><span data-ttu-id="f7297-141">ビデオの機能強化</span><span class="sxs-lookup"><span data-stu-id="f7297-141">Video Enhancements</span></span>

<span data-ttu-id="f7297-142">いくつかの新機能により、会議参加者のビデオエクスペリエンスが大幅に向上します。</span><span class="sxs-lookup"><span data-stu-id="f7297-142">Several new features significantly enhance the video experience for conference participants.</span></span>

  - <span data-ttu-id="f7297-143">ビデオは面の検出とスマートなフレーミングによって強化されているため、参加者のビデオはフレーム内で中央に配置されたままにすることができます。</span><span class="sxs-lookup"><span data-stu-id="f7297-143">Video is enhanced with face detection and smart framing, so that a participant’s video moves to help keep them centered in the frame.</span></span>

  - <span data-ttu-id="f7297-144">高解像度ビデオが、2パーティーの通話とマルチパーティの会議でサポートされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="f7297-144">High-definition video is now supported in two-party calls and multiparty conferences.</span></span> <span data-ttu-id="f7297-145">ユーザーは、HD 1080P の解像度を向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="f7297-145">Users can experience resolutions up to HD 1080P.</span></span>

  - <span data-ttu-id="f7297-146">参加者は、さまざまな会議のレイアウトから選ぶことができます。ギャラリービューには、すべての参加者の写真やビデオが表示されます。[スピーカービュー]: 会議の内容が表示され、現在の発表者のビデオまたは写真のみが表示されます。プレゼンテーションビューに会議コンテンツのみが表示されます。[コンパクト表示すると、会議のコントロールのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f7297-146">Participants can select from different meeting layouts: Gallery View shows all participants’ pictures or videos; Speaker View shows the meeting content and only the current speaker’s video or picture; Presentation View shows meeting content only; Compact View shows just the meeting controls.</span></span>

  - <span data-ttu-id="f7297-147">新しいギャラリー機能を使用すると、参加者は同時に複数のビデオフィードを表示できます。</span><span class="sxs-lookup"><span data-stu-id="f7297-147">With the new Gallery feature, participants can see multiple video feeds at the same time.</span></span> <span data-ttu-id="f7297-148">会議に5人以上の参加者がいる場合は、最もアクティブな参加者だけのビデオフィードが一番上の行に表示され、他の参加者の写真が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f7297-148">If the conference has more than five participants, video feeds of only the most active participants appear in the top row, and pictures appear for the other participants.</span></span>

  - <span data-ttu-id="f7297-149">参加者はビデオのピン留めを使用して、利用可能なビデオフィードを1つ以上選択して、いつでも表示することができます。</span><span class="sxs-lookup"><span data-stu-id="f7297-149">Participants can use video pinning to select one or more of the available video feeds to be visible at all times.</span></span>

  - <span data-ttu-id="f7297-150">発表者は、ビデオスポットライト機能を使用して、1人のビデオフィードを選択し、会議の参加者のみがその参加者に表示されるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="f7297-150">Presenters can use the Video Spotlight feature to select one person’s video feed so that every participant in the meeting sees that participant only.</span></span>

</div>

<div>

## <a name="chat-room-integration"></a><span data-ttu-id="f7297-151">チャットルームの統合</span><span class="sxs-lookup"><span data-stu-id="f7297-151">Chat Room Integration</span></span>

<span data-ttu-id="f7297-152">Lync 2013 では、以前に Lync 2010 グループチャットで提供されていた機能が統合されました。</span><span class="sxs-lookup"><span data-stu-id="f7297-152">Lync 2013 now integrates the features previously provided by Lync 2010 Group Chat.</span></span> <span data-ttu-id="f7297-153">別のグループチャットクライアントは必要なくなりました。</span><span class="sxs-lookup"><span data-stu-id="f7297-153">A separate group chat client is no longer required.</span></span>

  - <span data-ttu-id="f7297-154">Lync 2013 内で、ユーザーはチャットルームを検索したり、チャットルームを連絡先に追加したり、チャットルームのアクティビティを監視したり、メッセージを読んだり投稿したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="f7297-154">From within Lync 2013, users can search for chat rooms, add chat rooms to their contacts, monitor chat room activity, and read and post messages.</span></span>

  - <span data-ttu-id="f7297-155">ユーザーは、トピックフィードを作成して、チャットルームのいずれかのユーザーが特定のキーワードを含む投稿を追加した場合に通知されるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="f7297-155">Users can create topic feeds so that they’ll be notified if someone in one of their chat rooms adds a post containing specific keywords.</span></span>

  - <span data-ttu-id="f7297-156">[新しい **常設チャット** ] オプションページでは、ユーザーがメッセージをチャットルームに投稿したときに適用される通知アラートとサウンドを設定できます。</span><span class="sxs-lookup"><span data-stu-id="f7297-156">With the new **Persistent Chat** options page, users can set notification alerts and sounds that apply when people post messages to their chat rooms.</span></span>

</div>

<div>

## <a name="lync-web-app-updates"></a><span data-ttu-id="f7297-157">Lync Web App の更新プログラム</span><span class="sxs-lookup"><span data-stu-id="f7297-157">Lync Web App Updates</span></span>

<span data-ttu-id="f7297-158">Lync Web App は、Lync Server 2013 会議用の web ベースの会議クライアントです。</span><span class="sxs-lookup"><span data-stu-id="f7297-158">Lync Web App is the web-based conferencing client for Lync Server 2013 meetings.</span></span> <span data-ttu-id="f7297-159">このリリースでは、コンピューターの音声とビデオを Lync Web App に追加することで、Lync クライアントがローカルにインストールされていないすべてのユーザーに対して、会議中の完全な操作を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="f7297-159">In this release, the addition of computer audio and video to Lync Web App provides a complete in-meeting experience for anyone who doesn’t have a Lync client installed locally.</span></span> <span data-ttu-id="f7297-160">会議の参加者は、すべてのコラボレーション機能と共有機能、および発表者の会議コントロールにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="f7297-160">Meeting participants have access to all collaboration and sharing features and presenter meeting controls.</span></span>

<span data-ttu-id="f7297-161">ユーザーが会議に参加しようとしていて、ローカルにインストールされたクライアントがない場合、Lync Web App が開きます。</span><span class="sxs-lookup"><span data-stu-id="f7297-161">When a user tries to join a meeting but doesn’t have a locally installed client, Lync Web App opens.</span></span> <span data-ttu-id="f7297-162">会議への参加に追加のオプションを許可する場合は、[会議の参加] ページを構成できます。展開ドキュメントの「 [Lync Server 2013 で会議参加ページを構成する](lync-server-2013-configuring-the-meeting-join-page.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f7297-162">If you want to allow additional options for joining the meeting, you can configure the Meeting Join page; see [Configuring the meeting join page in Lync Server 2013](lync-server-2013-configuring-the-meeting-join-page.md) in the Deployment documentation.</span></span>

<span data-ttu-id="f7297-163">Lync Web App が強化されたため、Lync Server 2013 では、更新された出席者のバージョンは利用できません。</span><span class="sxs-lookup"><span data-stu-id="f7297-163">Because of the enhancements to Lync Web App, an updated version of Attendee isn’t available for Lync Server 2013.</span></span> <span data-ttu-id="f7297-164">Lync Web App は、組織外の参加者向けのクライアントです。</span><span class="sxs-lookup"><span data-stu-id="f7297-164">Lync Web App is the client of choice for participants outside your organization.</span></span> <span data-ttu-id="f7297-165">ローカルクライアントをインストールする必要はありませんが、オーディオ、ビデオ、共有機能については、プラグインを初めて使用するときにインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7297-165">No local client installation is required, although audio, video, and sharing features require a plug-in to be installed at first use.</span></span>

</div>

<div>

## <a name="lync-2013-for-mobile-clients-updates"></a><span data-ttu-id="f7297-166">Lync 2013 for Mobile クライアントの更新プログラム</span><span class="sxs-lookup"><span data-stu-id="f7297-166">Lync 2013 for Mobile Clients Updates</span></span>

<span data-ttu-id="f7297-167">Lync 2013 モバイルクライアントでは、拡張されたプレゼンス、連絡先、IM 機能に加えて、インターネットと携帯電話のデータ接続を介して音声通話とビデオ通話を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="f7297-167">In addition to enhanced presence, contacts, and IM capabilities, Lync 2013 mobile clients now provide voice and video calling over the Internet and cellular data connections.</span></span> <span data-ttu-id="f7297-168">予定表アイテムの会議リンクを1回タップするだけで、モバイルユーザーは Lync の音声とビデオ会議に参加できます。</span><span class="sxs-lookup"><span data-stu-id="f7297-168">With a single tap of the meeting link in a calendar item, mobile users can join Lync voice and video meetings.</span></span> <span data-ttu-id="f7297-169">Lync 2013 モバイルクライアントの詳細については、「 [Lync Server 2013 でモバイルクライアントを計画](lync-server-2013-planning-for-mobile-clients.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f7297-169">For more information about Lync 2013 mobile clients, see [Planning for mobile clients in Lync Server 2013](lync-server-2013-planning-for-mobile-clients.md).</span></span>

</div>

<div>

## <a name="lync-2013-user-interface-updates"></a><span data-ttu-id="f7297-170">Lync 2013 ユーザーインターフェイスの更新</span><span class="sxs-lookup"><span data-stu-id="f7297-170">Lync 2013 User Interface Updates</span></span>

<div>

## <a name="accessibility-updates"></a><span data-ttu-id="f7297-171">アクセシビリティの更新</span><span class="sxs-lookup"><span data-stu-id="f7297-171">Accessibility Updates</span></span>

<span data-ttu-id="f7297-172">Lync 2013 には、いくつかの新しいアクセシビリティ機能が組み込まれています。</span><span class="sxs-lookup"><span data-stu-id="f7297-172">Lync 2013 incorporates several new accessibility features.</span></span>

  - <span data-ttu-id="f7297-173">Lync 2013 では高 DPI の解像度がサポートされており、ユーザーはテキストやグラフィックスを125% と150% のドットを使用できるように拡大縮小することができます。</span><span class="sxs-lookup"><span data-stu-id="f7297-173">Lync 2013 supports high DPI resolution, enabling users to scale text and graphics for 125% and 150% dots per inch.</span></span>

  - <span data-ttu-id="f7297-174">Lync はハイコントラストをサポートしているため、Windows でハイコントラストテーマを使用すると、ユーザーインターフェイスは完全に機能します。</span><span class="sxs-lookup"><span data-stu-id="f7297-174">Lync provides high-contrast support so that the user interface remains fully functional when used with high contrast themes in Windows.</span></span>

  - <span data-ttu-id="f7297-175">Lync では、マウスを使わずに重要な機能にアクセスできるように、100を超えるキーボードショートカットが用意されています。</span><span class="sxs-lookup"><span data-stu-id="f7297-175">Lync offers more than 100 keyboard shortcuts so that users can access important functions without a mouse.</span></span> <span data-ttu-id="f7297-176">たとえば、ユーザーは Alt キーを押しながら C キーを押して通話を承諾したり、Alt + I キーを押して無視したりすることができます。これには、tab キーまたはフォーカスを設定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="f7297-176">For example, users can press Alt+C to accept a call, or Alt + I to ignore it, without having to tab or set the focus.</span></span> <span data-ttu-id="f7297-177">(Alt + Q) キーを押すと、通話が終了します (Ctrl + N)。 OneNote を起動し、(Alt + T) を押すと、[ツール] メニューが開きます。</span><span class="sxs-lookup"><span data-stu-id="f7297-177">Pressing (Alt+Q) ends a call, (Ctrl+N) starts OneNote, and (Alt+T) opens the Tools menu.</span></span>

  - <span data-ttu-id="f7297-178">Lync 2013 でのさまざまなスクリーンリーダーのサポートにより、スクリーンリーダーが有効になっているときに、通知、着信要求、インスタントメッセージはすべて音声で読み上げることができます。</span><span class="sxs-lookup"><span data-stu-id="f7297-178">Extensive screen reader support in Lync 2013 ensures that all notifications, incoming requests, and instant messages are read aloud when a screen reader is enabled.</span></span>

</div>

<div>

## <a name="presence-while-sharing"></a><span data-ttu-id="f7297-179">共有中のプレゼンス</span><span class="sxs-lookup"><span data-stu-id="f7297-179">Presence While Sharing</span></span>

<span data-ttu-id="f7297-180">Lync は、ユーザーが共有していることを検出すると、プレゼンス状態を表示するユーザーに自動的に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="f7297-180">When Lync detects that a user is sharing, Lync automatically assigns the user a Presenting presence status.</span></span> <span data-ttu-id="f7297-181">この状態では、送信者にワークグループのプライバシー関係が割り当てられていない限り、すべての着信がブロックされます。</span><span class="sxs-lookup"><span data-stu-id="f7297-181">This status blocks all incoming communications unless the sender is assigned the Workgroup privacy relationship.</span></span> <span data-ttu-id="f7297-182">ユーザーがセカンダリモニターでまったく共有機能を使用している場合、Lync では [プレゼンス状態の表示] は割り当てられません。</span><span class="sxs-lookup"><span data-stu-id="f7297-182">If the user is using the sharing feature entirely on a secondary monitor, Lync does not assign a Presenting presence status.</span></span>

</div>

<div>

## <a name="conversation-window-updates"></a><span data-ttu-id="f7297-183">スレッドウィンドウの更新</span><span class="sxs-lookup"><span data-stu-id="f7297-183">Conversation Window Updates</span></span>

<span data-ttu-id="f7297-184">再設計された会話ウィンドウで、重要な機能にすばやくアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="f7297-184">The redesigned Conversation window provides quicker access to important features.</span></span>

  - <span data-ttu-id="f7297-185">新しいタブ表示の会話機能を使用すると、ユーザーはすべての Im とチャットルームを1つの会話ウィンドウにまとめることができるようになります。</span><span class="sxs-lookup"><span data-stu-id="f7297-185">With the new tabbed conversations feature, users can now keep all their IMs and chat rooms in one Conversation window.</span></span> <span data-ttu-id="f7297-186">会話ウィンドウの左側にあるタブでは、ユーザーはアクティブなすべての会話の間を簡単に移動できます。</span><span class="sxs-lookup"><span data-stu-id="f7297-186">The tabs along the left side of the Conversation window let users navigate easily among all active conversations.</span></span>

  - <span data-ttu-id="f7297-187">ユーザーは個別の会話を別のウィンドウに表示して、ウィンドウのサイズを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="f7297-187">Users can pop out an individual conversation into a separate window, and then resize the window.</span></span> <span data-ttu-id="f7297-188">また、ウィンドウをポップして、メインの会話ウィンドウに戻すこともできます。</span><span class="sxs-lookup"><span data-stu-id="f7297-188">They can also pop the window back into the main Conversation window.</span></span>

  - <span data-ttu-id="f7297-189">Lync 2013 は、ユーザーがサインアウトして Lync にサインインしたときに、ユーザーの会話を再度開きます。</span><span class="sxs-lookup"><span data-stu-id="f7297-189">Lync 2013 reopens a user’s conversations when the user signs out and signs back in to Lync.</span></span>

  - <span data-ttu-id="f7297-190">ユーザーは、IM、ビデオ、プログラム共有、デスクトップ共有、または web 会議ツール (ホワイトボード、会議のメモ、共有ノートブック、添付ファイル) を任意の会話に簡単に追加することができます。</span><span class="sxs-lookup"><span data-stu-id="f7297-190">Users can quickly add IM, video, program sharing, desktop sharing, or web conferencing tools (whiteboard, meeting notes, shared notebooks, and attachments) to any conversation.</span></span>

  - <span data-ttu-id="f7297-191">ビデオまたはコンテンツが共有されている会議では、ユーザーは会議のビデオまたは共有コンテンツをポップアップ表示して、ウィンドウのサイズを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="f7297-191">In a meeting where video or content is being shared, users can pop out the meeting video or shared content, and then resize the window.</span></span>

</div>

<div>

## <a name="lync-main-window-updates"></a><span data-ttu-id="f7297-192">Lync メインウィンドウの更新プログラム</span><span class="sxs-lookup"><span data-stu-id="f7297-192">Lync Main Window Updates</span></span>

<span data-ttu-id="f7297-193">新しい合理化された外観では、 **現在の** 状況、メモフィールド、状態セレクター、 **位置情報の設定** セレクターなど、使い慣れた機能が保持されます。</span><span class="sxs-lookup"><span data-stu-id="f7297-193">The new streamlined look retains familiar features such as the **What’s happening today?** note field, the status selector, and the **Set Your Location** selector.</span></span>

  - <span data-ttu-id="f7297-194">チャットルームが有効になっていると、ユーザーはメインの Lync ページに新しい **チャットルーム** アイコンを表示します。</span><span class="sxs-lookup"><span data-stu-id="f7297-194">When chat rooms are enabled, users see a new **Chat Rooms** icon on the main Lync page.</span></span> <span data-ttu-id="f7297-195">[ **チャットルーム** ] アイコンを使用すると、ユーザーはチャットルームやフィルターにすばやくアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="f7297-195">With the **Chat Rooms** icon, users can quickly access their chat rooms and filters.</span></span>

  - <span data-ttu-id="f7297-196">ユーザーは、表示アイコンをクリックして、 **連絡先** ビュー、 **チャットルーム** ビュー、 **スレッド** ビュー、または **電話** 表示に切り替えることができます。</span><span class="sxs-lookup"><span data-stu-id="f7297-196">Users can click the view icons to switch to the **Contacts** view, **Chat Rooms** view, **Conversations** view, or **Phone** view.</span></span>

  - <span data-ttu-id="f7297-197">ユーザーが Exchange 2013 に移行されている場合は、高解像度の画像をアップロードできます。</span><span class="sxs-lookup"><span data-stu-id="f7297-197">If users have been migrated to Exchange 2013, they can upload a high resolution picture.</span></span>

</div>

<div>

## <a name="contacts-view-and-contact-card-updates"></a><span data-ttu-id="f7297-198">連絡先ビューと連絡先カードの更新</span><span class="sxs-lookup"><span data-stu-id="f7297-198">Contacts View and Contact Card Updates</span></span>

<span data-ttu-id="f7297-199">Lync 2013 を使用すると、ユーザーは [ **連絡先** ] ビューで連絡先やグループをさまざまな方法で表示できます。</span><span class="sxs-lookup"><span data-stu-id="f7297-199">Lync 2013 gives users different ways to view contacts and groups in their **Contacts** view.</span></span>

  - <span data-ttu-id="f7297-200">新しい統合連絡先ストアでは、ユーザーの Lync 連絡先が Exchange 2013 に移行された後、ユーザーは Lync 2013、Outlook、または Outlook Web App から連絡先にアクセスして管理することができます。また、そのお気に入りは同期されたままになります。</span><span class="sxs-lookup"><span data-stu-id="f7297-200">With the new unified contact store, after users' Lync contacts are migrated to Exchange 2013, the users can access and manage their contacts from Lync 2013, Outlook, or Outlook Web App, and their Favorites stay synchronized.</span></span> <span data-ttu-id="f7297-201">たとえば、ユーザーが Outlook のお気に入りに連絡先を追加すると、その連絡先は Lync 2013 の [お気に入り] グループに表示されます。</span><span class="sxs-lookup"><span data-stu-id="f7297-201">For example, if a user adds a contact to Favorites in Outlook, the contact appears in the Favorites group in Lync 2013.</span></span>

  - <span data-ttu-id="f7297-202">XMPP プロキシと XMPP ゲートウェイを追加して構成している場合、ユーザーは、インスタントメッセージ (im) とプレゼンス情報を取得するために、XMPP ベースのパートナーから連絡先を追加できます。</span><span class="sxs-lookup"><span data-stu-id="f7297-202">If you have added and configured the XMPP proxy and XMPP gateway, users can add contacts from XMPP-based partners for instant messaging and presence.</span></span>

  - <span data-ttu-id="f7297-203">**[組織外の連絡先を追加する」** 機能を使うと、組織外のユーザーを簡単に追加することができます。</span><span class="sxs-lookup"><span data-stu-id="f7297-203">A new **Add a Contact That’s Not in My Organization** feature gives users an easy way to add people who are external to the organization.</span></span>

  - <span data-ttu-id="f7297-204">新しい [ **お気に入り** ] グループを使用すると、ユーザーが最も頻繁にアクセスするユーザーのリストを作成できます。</span><span class="sxs-lookup"><span data-stu-id="f7297-204">A new **Favorites** group lets users build a list of people users contact most often for quicker access.</span></span>

  - <span data-ttu-id="f7297-205">ユーザーは、[新しい **連絡先リスト** のオプション] ページを使って、ユーザーが連絡先を並べ替えて表示する方法を選ぶことができます。</span><span class="sxs-lookup"><span data-stu-id="f7297-205">Users can use the new **Contacts List** options page to choose how users want to sort and display contacts.</span></span> <span data-ttu-id="f7297-206">ユーザーは、連絡先の画像や狭い1行のビューを表示する拡張された2行のビューを選ぶことができます。</span><span class="sxs-lookup"><span data-stu-id="f7297-206">Users can select an expanded, two-line view that shows contacts’ pictures, or a condensed one-line view.</span></span> <span data-ttu-id="f7297-207">ユーザーは、連絡先をアルファベット順または空き時間別に並べ替えることもできます。</span><span class="sxs-lookup"><span data-stu-id="f7297-207">Users can also sort contacts alphabetically or by availability.</span></span>

</div>

<div>

## <a name="conferencing-updates"></a><span data-ttu-id="f7297-208">会議の更新</span><span class="sxs-lookup"><span data-stu-id="f7297-208">Conferencing Updates</span></span>

<span data-ttu-id="f7297-209">Lync 2013 では、会議機能がいくつか強化されています。</span><span class="sxs-lookup"><span data-stu-id="f7297-209">Lync 2013 offers several enhancements to conferencing features.</span></span>

  - <span data-ttu-id="f7297-210">会議の種類によっては、ユーザーは会議のスケジュール時に参加者をミュートにし、ビデオ共有を許可またはブロックすることができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="f7297-210">Depending on the type of meeting, users can now mute the audience and allow or block video sharing when scheduling the meeting.</span></span> <span data-ttu-id="f7297-211">これらのオプションは、[ **会議のオプション** ] ページで利用でき、20人以上の参加者との大きな会議に適しています。</span><span class="sxs-lookup"><span data-stu-id="f7297-211">These options are available on the **Meeting Options** page and are recommended for large meetings with more than 20 participants.</span></span>

  - <span data-ttu-id="f7297-212">会議室での音声コントロールが使いやすくなりました。ユーザーは、ミュート、ミュート解除、デバイス変更などのオーディオオプションを制御できます。</span><span class="sxs-lookup"><span data-stu-id="f7297-212">Easy to use audio controls in the meeting room allow the user to control audio options, such as mute, unmute, change device, and so on.</span></span>

  - <span data-ttu-id="f7297-213">プログラムを共有する場合、複数のプログラムを操作する必要がある場合は、共有する複数のプログラムを選ぶことができます。</span><span class="sxs-lookup"><span data-stu-id="f7297-213">When sharing programs, users can select multiple programs to share if they need to work with more than one program.</span></span>

  - <span data-ttu-id="f7297-214">PowerPoint ファイルをアップロードして、ビデオクリップを含むプレゼンテーションをアップロードできるようになりました。スライド上でマウスをポイントすると、再生、一時停止、オーディオコントロールなどのビデオコントロールが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f7297-214">Users can now upload presentations that contain video clips by uploading the PowerPoint file, and pointing the mouse over the slide to display video controls, such as play, pause, and audio controls.</span></span>

  - <span data-ttu-id="f7297-215">会議中に、ユーザーは [その **他のオプション**(**...**)] メニューで [**この通話の結合**] を使って、開いている別の会話を会議に統合することができます。</span><span class="sxs-lookup"><span data-stu-id="f7297-215">While in a meeting, users can merge another open conversation into the meeting by using **Merge This Call Into** on the **More Options** (**…**) menu.</span></span>

  - <span data-ttu-id="f7297-216">参加者の名前を表示するには、[ **参加者の表示** ] ボタンの上にマウスを置いて、または [ **参加者リストの表示** ] をクリックして、会議にパネルをドッキングします。</span><span class="sxs-lookup"><span data-stu-id="f7297-216">To see the participants’ names, users can hover the mouse over the **View Participants** button, or click **Show Participant List** to dock the panel in the meeting.</span></span>

  - <span data-ttu-id="f7297-217">会議の種類に応じて、ユーザーはさまざまなコンテンツと参加者のビューから選ぶことができます。</span><span class="sxs-lookup"><span data-stu-id="f7297-217">Depending on the meeting type, users can select from several different content and participant views.</span></span>

  - <span data-ttu-id="f7297-218">会議のレコーディングは、Windows Media Player (MP4) で再生される形式で自動的に保存されます。</span><span class="sxs-lookup"><span data-stu-id="f7297-218">Meeting recordings are automatically saved in a format that plays in Windows Media Player (MP4).</span></span> <span data-ttu-id="f7297-219">他のユーザーと簡単にファイルを共有したり、レコーディングマネージャーの **発行** 機能を使用して、レコーディングを共有の場所に投稿したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="f7297-219">Users can easily share the file with anyone, or use the **Publish** feature in recording manager to post the recording on a shared location.</span></span>

  - <span data-ttu-id="f7297-220">OneNote では、新しい方法で会議での共同作業を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="f7297-220">OneNote enables new ways to collaborate in a meeting.</span></span> <span data-ttu-id="f7297-221">会議中に、ユーザーは、会議後に OneNote を使用して個人用にノートを取ったり、共有ノートブックを使用したり、会議の参加者とリアルタイムで共同編集を行ったりすることができます。</span><span class="sxs-lookup"><span data-stu-id="f7297-221">During a meeting, users can take notes with OneNote for personal use after the meeting, or use shared notebooks and co-edit with meeting participants in real time.</span></span> <span data-ttu-id="f7297-222">すべてのチームメンバーが共有ノートにアクセスして、情報の投稿、アイデアのブレインストーミング、ノートブックのページの仮想ホワイトボードとしての使用を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="f7297-222">All team members can access the shared notes to contribute information, brainstorm ideas, or use the notebook pages as a virtual whiteboard.</span></span> <span data-ttu-id="f7297-223">会議で共有されているユーザーとコンテンツは、ノートに自動的に追加されます。</span><span class="sxs-lookup"><span data-stu-id="f7297-223">People and content shared in the meeting are automatically added to the Notes.</span></span>

  - <span data-ttu-id="f7297-224">会議室の下部にある **[コンテンツを共有し、会議アクティビティをリード** します] を使用してコンテンツタイプを切り替えることができます。</span><span class="sxs-lookup"><span data-stu-id="f7297-224">Users can switch between content types using **Share content and lead meeting activities** at the bottom of the meeting room.</span></span> <span data-ttu-id="f7297-225">[プレゼンテーション用コンテンツの **管理** ] メニューを使用して、共有するコンテンツを選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="f7297-225">Users can also use the **Manage Presentable Content** menu to choose which content they want to share.</span></span>

</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f7297-226">関連項目</span><span class="sxs-lookup"><span data-stu-id="f7297-226">See Also</span></span>


[<span data-ttu-id="f7297-227">Lync Server 2013 でのクライアントの計画</span><span class="sxs-lookup"><span data-stu-id="f7297-227">Planning for clients in Lync Server 2013</span></span>](lync-server-2013-planning-for-clients.md)  
  

<span data-ttu-id="f7297-228"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f7297-228"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

