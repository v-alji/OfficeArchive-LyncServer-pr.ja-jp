---
title: 'Lync Server 2013: リモート通話コントロールの計画'
description: 'Lync Server 2013: リモート通話コントロールの計画'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for remote call control
ms:assetid: 688a0328-1aa7-449f-b5f7-98c876112ed2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558658(v=OCS.15)
ms:contentKeyID: 48184371
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e3a089a806683098a948d235559bbcb16224bdde
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400209"
---
# <a name="planning-for-remote-call-control-in-lync-server-2013"></a><span data-ttu-id="b05a3-103">Lync Server 2013 でのリモート通話コントロールの計画</span><span class="sxs-lookup"><span data-stu-id="b05a3-103">Planning for remote call control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b05a3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b05a3-104">

<span> </span></span></span>

<span data-ttu-id="b05a3-105">_**最終更新日:** 2012-09-05_</span><span class="sxs-lookup"><span data-stu-id="b05a3-105">_**Topic Last Modified:** 2012-09-05_</span></span>

<span data-ttu-id="b05a3-106">Lync Server 2013 では、リモート通話コントロールのシナリオがサポートされているため、ユーザーは自分のデスクトップコンピューターで Lync 2013 を使用して、プライベート支店の exchange (PBX) 電話を制御することができます。</span><span class="sxs-lookup"><span data-stu-id="b05a3-106">In Lync Server 2013, support for remote call control scenarios enables users to control their private branch exchange (PBX) phones by using Lync 2013 on their desktop computers.</span></span> <span data-ttu-id="b05a3-107">このセクションでは、リモート通話コントロールの機能と、リモート通話コントロールを展開するための要件について説明します。</span><span class="sxs-lookup"><span data-stu-id="b05a3-107">This section describes remote call control features and requirements for deploying remote call control.</span></span>

<span data-ttu-id="b05a3-108">PBX と Lync Server 2013 を統合すると、リモート通話2013コントロールが有効になっているユーザーは、次のようにして、PBX 電話での通話を制御できるようになります。</span><span class="sxs-lookup"><span data-stu-id="b05a3-108">Integration between a PBX and Lync Server 2013 makes it possible for users enabled for remote call control to use the Lync 2013 user interface (UI) to control calls on their PBX phones in the following ways:</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b05a3-109">最終的には、ユーザーの PBX 携帯電話をホストしている PBX の機能によって、そのユーザーが使用できるリモート通話コントロール機能が決定されます。</span><span class="sxs-lookup"><span data-stu-id="b05a3-109">Ultimately, the capabilities of the PBX that hosts a user’s PBX phone determine the remote call control features that will be available to that user.</span></span>



</div>

  - <span data-ttu-id="b05a3-110">発信通話を行う</span><span class="sxs-lookup"><span data-stu-id="b05a3-110">Make an outgoing call</span></span>

  - <span data-ttu-id="b05a3-111">着信通話に応答する</span><span class="sxs-lookup"><span data-stu-id="b05a3-111">Answer an incoming call</span></span>

  - <span data-ttu-id="b05a3-112">インスタントメッセージで着信に応答する</span><span class="sxs-lookup"><span data-stu-id="b05a3-112">Answer an incoming call with an instant message</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="b05a3-113">つまり、発信者の電話番号は、組織のグローバルアドレス一覧 (GAL)、呼び出し元の Lync 連絡先リスト、またはフェデレーションパートナーの組織内のインスタントメッセージアドレスに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="b05a3-113">That is, when the caller’s phone number can be associated with an instant message address in your organization’s global address list (GAL), in the callee’s Lync Contacts list, or in a federated partner’s organization.</span></span>

    
    </div>

  - <span data-ttu-id="b05a3-114">通話の転送</span><span class="sxs-lookup"><span data-stu-id="b05a3-114">Transfer a call</span></span>

  - <span data-ttu-id="b05a3-115">着信通話を転送する</span><span class="sxs-lookup"><span data-stu-id="b05a3-115">Forward an incoming call</span></span>

  - <span data-ttu-id="b05a3-116">通話を保留にする</span><span class="sxs-lookup"><span data-stu-id="b05a3-116">Place calls on hold</span></span>

  - <span data-ttu-id="b05a3-117">複数の同時通話の切り替え</span><span class="sxs-lookup"><span data-stu-id="b05a3-117">Alternate between multiple concurrent calls</span></span>

  - <span data-ttu-id="b05a3-118">すでに通話中 (通話待ち) 中に2回目の通話に応答する</span><span class="sxs-lookup"><span data-stu-id="b05a3-118">Answer a second call while already in a call (that is, call waiting)</span></span>

  - <span data-ttu-id="b05a3-119">Dial dual トーン (DTMF) 数字</span><span class="sxs-lookup"><span data-stu-id="b05a3-119">Dial dual-tone multifrequency (DTMF) digits</span></span>

  - <span data-ttu-id="b05a3-120">[会話] ウィンドウで、Microsoft Office OneNote のノート作成プログラムにノートを入力する</span><span class="sxs-lookup"><span data-stu-id="b05a3-120">In the Conversation window, type notes in Microsoft Office OneNote note-taking program</span></span>

<span data-ttu-id="b05a3-121">さらに、ユーザーがリモート通話コントロールを有効にしている場合は、Lync 2013 によって次の通話情報がユーザーに提供されます。</span><span class="sxs-lookup"><span data-stu-id="b05a3-121">Additionally, when a user is enabled for remote call control, Lync 2013 provides the user with the following call information:</span></span>

  - <span data-ttu-id="b05a3-122">呼び出し元の電話番号が、リモート通話コントロール対応ユーザーの Microsoft Office Outlook メッセージングおよびコラボレーションクライアント、Lync 連絡先リスト、または組織の GAL の連絡先リストに存在する場合の、名前による発信者の識別。</span><span class="sxs-lookup"><span data-stu-id="b05a3-122">Identification of a caller by name when the caller’s phone number exists in the Contacts list of a remote call control-enabled user’s Microsoft Office Outlook messaging and collaboration client, Lync Contacts list, or your organization’s GAL.</span></span>

  - <span data-ttu-id="b05a3-123">Outlook の [会話履歴] フォルダーに保存されている、過去の着信と発信の通話。</span><span class="sxs-lookup"><span data-stu-id="b05a3-123">Past incoming and outgoing calls, which are saved in the Conversation History folder in Outlook.</span></span>

  - <span data-ttu-id="b05a3-124">不在着信通知。ユーザーの Outlook 受信トレイフォルダーに送信されますが、着信呼び出しの受信時に Lync が実行されている場合にのみ生成されます。</span><span class="sxs-lookup"><span data-stu-id="b05a3-124">Missed call notifications, which are sent to the user’s Outlook Inbox folder, but are generated only if Lync is running when the incoming call is received.</span></span>

<div>

## <a name="remote-call-control-and-enterprise-voice"></a><span data-ttu-id="b05a3-125">リモート通話コントロールとエンタープライズボイス</span><span class="sxs-lookup"><span data-stu-id="b05a3-125">Remote Call Control and Enterprise Voice</span></span>

<span data-ttu-id="b05a3-126">リモート通話コントロール機能はエンタープライズボイス機能とは異なりますが、どちらのユーザーも有効にすることはできませんが、エンタープライズボイスは、リモート通話コントロールが有効になっているユーザーが利用できる機能のサブセットを提供します。</span><span class="sxs-lookup"><span data-stu-id="b05a3-126">Although remote call control features are separate from Enterprise Voice features and users cannot be enabled for both, Enterprise Voice provides a subset of features that are also available to users who are enabled for remote call control.</span></span> <span data-ttu-id="b05a3-127">エンタープライズボイスが展開されている場合、リモート通話コントロールが有効になっているユーザーは、Lync を使って次のエンタープライズ Voip 機能にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="b05a3-127">If Enterprise Voice is deployed, users who are enabled for remote call control can use Lync to access the following Enterprise Voice features:</span></span>

  - <span data-ttu-id="b05a3-128">別の Lync クライアントに対して音声通話を発信および受信する</span><span class="sxs-lookup"><span data-stu-id="b05a3-128">Make and receive audio calls to another Lync client</span></span>

  - <span data-ttu-id="b05a3-129">エンタープライズ Voip が有効になっているユーザーによって作成された会議のオーディオ部分に参加する</span><span class="sxs-lookup"><span data-stu-id="b05a3-129">Join the audio portion of a conference created by a user who is enabled for Enterprise Voice</span></span>

</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="b05a3-130">このセクション中</span><span class="sxs-lookup"><span data-stu-id="b05a3-130">In This Section</span></span>

  - [<span data-ttu-id="b05a3-131">Lync Server 2013 のリモート通話コントロールの展開タスク</span><span class="sxs-lookup"><span data-stu-id="b05a3-131">Deployment tasks for remote call control in Lync Server 2013</span></span>](lync-server-2013-deployment-tasks-for-remote-call-control.md)

<span data-ttu-id="b05a3-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b05a3-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

