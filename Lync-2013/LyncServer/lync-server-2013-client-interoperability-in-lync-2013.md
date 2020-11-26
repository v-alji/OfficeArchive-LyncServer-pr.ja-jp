---
title: 'Lync Server 2013: Lync 2013 でのクライアント相互運用性'
description: 'Lync Server 2013: Lync 2013 でのクライアントの相互運用性。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Client interoperability in Lync 2013
ms:assetid: 0f126571-91a2-45d5-855c-1e4ddb45fc04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204672(v=OCS.15)
ms:contentKeyID: 48183417
ms.date: 03/04/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8ea6e90d9479f03dd6d946787e70a2b3cc078699
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434922"
---
# <a name="client-interoperability-in-lync-2013"></a><span data-ttu-id="9790f-103">Lync 2013 でのクライアント相互運用性</span><span class="sxs-lookup"><span data-stu-id="9790f-103">Client interoperability in Lync 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9790f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9790f-104">

<span> </span></span></span>

<span data-ttu-id="9790f-105">_**最終更新日:** 2016-03-04_</span><span class="sxs-lookup"><span data-stu-id="9790f-105">_**Topic Last Modified:** 2016-03-04_</span></span>

<span data-ttu-id="9790f-106">このトピックでは、Microsoft Lync Server 2013 クライアントが、以前のバージョンの Lync Server と Office Communications Server からクライアントとの共存と操作を行うことができるようにする機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="9790f-106">This topic discusses the ability of Microsoft Lync Server 2013 clients to coexist and interact with clients from earlier versions of Lync Server and Office Communications Server.</span></span>

<div>

## <a name="server-and-client-compatibility"></a><span data-ttu-id="9790f-107">サーバーとクライアントの互換性</span><span class="sxs-lookup"><span data-stu-id="9790f-107">Server and Client Compatibility</span></span>

<span data-ttu-id="9790f-108">次の表は、クライアントバージョンとサーバーバージョンのサポートされる組み合わせを示しています。</span><span class="sxs-lookup"><span data-stu-id="9790f-108">The following table shows the supported combinations of client versions and server versions.</span></span> <span data-ttu-id="9790f-109">次の表は、クライアントが指定したサーバーに接続しようとしたときにサインインがサポートされるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="9790f-109">This table indicates whether sign-in is supported when the client attempts to connect to the server indicated.</span></span> <span data-ttu-id="9790f-110">Lync Server 2013 では、以前のクライアントバージョンがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="9790f-110">Lync Server 2013 supports the previous client version.</span></span> <span data-ttu-id="9790f-111">また、以前のリリースとは異なり、Lync Server 2010 では新しい Lync 2013 クライアントがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="9790f-111">Also, unlike previous releases, Lync Server 2010 supports the new Lync 2013 clients.</span></span> <span data-ttu-id="9790f-112">これにより、Lync Server 2010 からアップグレードしている組織は、Lync Server のアップグレードに関係なく、新しいクライアントを展開することができます。</span><span class="sxs-lookup"><span data-stu-id="9790f-112">This allows organizations who are upgrading from Lync Server 2010 to roll out new clients independent of Lync Server upgrades.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9790f-113">クライアント</span><span class="sxs-lookup"><span data-stu-id="9790f-113">Client</span></span></th>
<th><span data-ttu-id="9790f-114">Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9790f-114">Lync Server 2013</span></span></th>
<th><span data-ttu-id="9790f-115">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="9790f-115">Lync Server 2010</span></span></th>
<th><span data-ttu-id="9790f-116">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="9790f-116">Office Communications Server 2007 R2</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9790f-117">Lync 2013</span><span class="sxs-lookup"><span data-stu-id="9790f-117">Lync 2013</span></span></p></td>
<td><p><span data-ttu-id="9790f-118">サポート</span><span class="sxs-lookup"><span data-stu-id="9790f-118">Supported</span></span></p></td>
<td><p><span data-ttu-id="9790f-119">Supported5</span><span class="sxs-lookup"><span data-stu-id="9790f-119">Supported5</span></span></p></td>
<td><p><span data-ttu-id="9790f-120">非サポート</span><span class="sxs-lookup"><span data-stu-id="9790f-120">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9790f-121">Lync 2013 Basic</span><span class="sxs-lookup"><span data-stu-id="9790f-121">Lync 2013 Basic</span></span></p></td>
<td><p><span data-ttu-id="9790f-122">サポート</span><span class="sxs-lookup"><span data-stu-id="9790f-122">Supported</span></span></p></td>
<td><p><span data-ttu-id="9790f-123">サポート対象</span><span class="sxs-lookup"><span data-stu-id="9790f-123">Supported</span></span></p></td>
<td><p><span data-ttu-id="9790f-124">サポート対象外</span><span class="sxs-lookup"><span data-stu-id="9790f-124">Not Supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9790f-125">Lync Web App 2013</span><span class="sxs-lookup"><span data-stu-id="9790f-125">Lync Web App 2013</span></span></p></td>
<td><p><span data-ttu-id="9790f-126">サポート対象</span><span class="sxs-lookup"><span data-stu-id="9790f-126">Supported</span></span></p></td>
<td><p><span data-ttu-id="9790f-127">サポート対象外</span><span class="sxs-lookup"><span data-stu-id="9790f-127">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="9790f-128">サポート対象外</span><span class="sxs-lookup"><span data-stu-id="9790f-128">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9790f-129">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="9790f-129">Lync 2010</span></span></p></td>
<td><p><span data-ttu-id="9790f-130">サポート</span><span class="sxs-lookup"><span data-stu-id="9790f-130">Supported</span></span></p></td>
<td><p><span data-ttu-id="9790f-131">サポート対象</span><span class="sxs-lookup"><span data-stu-id="9790f-131">Supported</span></span></p></td>
<td><p><span data-ttu-id="9790f-132">サポート対象外</span><span class="sxs-lookup"><span data-stu-id="9790f-132">Not Supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9790f-133">Lync 2010 Attendant</span><span class="sxs-lookup"><span data-stu-id="9790f-133">Lync 2010 Attendant</span></span></p></td>
<td><p><span data-ttu-id="9790f-134">サポート</span><span class="sxs-lookup"><span data-stu-id="9790f-134">Supported</span></span></p></td>
<td><p><span data-ttu-id="9790f-135">サポート対象</span><span class="sxs-lookup"><span data-stu-id="9790f-135">Supported</span></span></p></td>
<td><p><span data-ttu-id="9790f-136">サポート対象外</span><span class="sxs-lookup"><span data-stu-id="9790f-136">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9790f-137">Lync 2010 グループ チャット</span><span class="sxs-lookup"><span data-stu-id="9790f-137">Lync 2010 Group Chat</span></span></p></td>
<td><p><span data-ttu-id="9790f-138">Supported1</span><span class="sxs-lookup"><span data-stu-id="9790f-138">Supported1</span></span></p></td>
<td><p><span data-ttu-id="9790f-139">Supported2</span><span class="sxs-lookup"><span data-stu-id="9790f-139">Supported2</span></span></p></td>
<td><p><span data-ttu-id="9790f-140">該当なし</span><span class="sxs-lookup"><span data-stu-id="9790f-140">Not Applicable</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9790f-141">Lync Web App 2010</span><span class="sxs-lookup"><span data-stu-id="9790f-141">Lync Web App 2010</span></span></p></td>
<td><p><span data-ttu-id="9790f-142">非サポート</span><span class="sxs-lookup"><span data-stu-id="9790f-142">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="9790f-143">サポート対象</span><span class="sxs-lookup"><span data-stu-id="9790f-143">Supported</span></span></p></td>
<td><p><span data-ttu-id="9790f-144">サポート対象外</span><span class="sxs-lookup"><span data-stu-id="9790f-144">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9790f-145">Lync 2010 Attendee</span><span class="sxs-lookup"><span data-stu-id="9790f-145">Lync 2010 Attendee</span></span></p></td>
<td><p><span data-ttu-id="9790f-146">Supported3 しない</span><span class="sxs-lookup"><span data-stu-id="9790f-146">Not Supported3</span></span></p></td>
<td><p><span data-ttu-id="9790f-147">サポート対象</span><span class="sxs-lookup"><span data-stu-id="9790f-147">Supported</span></span></p></td>
<td><p><span data-ttu-id="9790f-148">サポート対象外</span><span class="sxs-lookup"><span data-stu-id="9790f-148">Not Supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9790f-149">Office Communicator 2007 R2</span><span class="sxs-lookup"><span data-stu-id="9790f-149">Office Communicator 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="9790f-150">Interoperable4</span><span class="sxs-lookup"><span data-stu-id="9790f-150">Interoperable4</span></span></p></td>
<td><p><span data-ttu-id="9790f-151">サポート</span><span class="sxs-lookup"><span data-stu-id="9790f-151">Supported</span></span></p></td>
<td><p><span data-ttu-id="9790f-152">サポート</span><span class="sxs-lookup"><span data-stu-id="9790f-152">Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9790f-153">Microsoft Office Communications Server 2007 R2 Attendant</span><span class="sxs-lookup"><span data-stu-id="9790f-153">Microsoft Office Communications Server 2007 R2 Attendant</span></span></p></td>
<td><p><span data-ttu-id="9790f-154">非サポート</span><span class="sxs-lookup"><span data-stu-id="9790f-154">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="9790f-155">サポート</span><span class="sxs-lookup"><span data-stu-id="9790f-155">Supported</span></span></p></td>
<td><p><span data-ttu-id="9790f-156">サポート</span><span class="sxs-lookup"><span data-stu-id="9790f-156">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9790f-157">Office Communicator 2007</span><span class="sxs-lookup"><span data-stu-id="9790f-157">Office Communicator 2007</span></span></p></td>
<td><p><span data-ttu-id="9790f-158">非サポート</span><span class="sxs-lookup"><span data-stu-id="9790f-158">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="9790f-159">サポート</span><span class="sxs-lookup"><span data-stu-id="9790f-159">Supported</span></span></p></td>
<td><p><span data-ttu-id="9790f-160">サポート</span><span class="sxs-lookup"><span data-stu-id="9790f-160">Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9790f-161">Office Live Meeting 2007</span><span class="sxs-lookup"><span data-stu-id="9790f-161">Office Live Meeting 2007</span></span></p></td>
<td><p><span data-ttu-id="9790f-162">非サポート</span><span class="sxs-lookup"><span data-stu-id="9790f-162">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="9790f-163">サポート</span><span class="sxs-lookup"><span data-stu-id="9790f-163">Supported</span></span></p></td>
<td><p><span data-ttu-id="9790f-164">サポート</span><span class="sxs-lookup"><span data-stu-id="9790f-164">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9790f-165">Lync Windows ストア アプリ</span><span class="sxs-lookup"><span data-stu-id="9790f-165">Lync Windows Store app</span></span></p></td>
<td><p><span data-ttu-id="9790f-166">サポート</span><span class="sxs-lookup"><span data-stu-id="9790f-166">Supported</span></span></p></td>
<td><p><span data-ttu-id="9790f-167">サポート対象</span><span class="sxs-lookup"><span data-stu-id="9790f-167">Supported</span></span></p></td>
<td><p><span data-ttu-id="9790f-168">サポート対象外</span><span class="sxs-lookup"><span data-stu-id="9790f-168">Not Supported</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9790f-169">1For については、「 [Lync server 2010、グループチャット、または Office Communications Server 2007 R2 グループチャットから Lync server 2013、常設チャットサーバーへの移行](migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9790f-169">1For details, see [Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server](migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server.md).</span></span>

<span data-ttu-id="9790f-170">2In Lync Server 2010 では、グループチャット機能は、Lync Server 2010 用のサードパーティの信頼済みアプリケーションであるグループチャットサーバーで利用できました。</span><span class="sxs-lookup"><span data-stu-id="9790f-170">2In Microsoft Lync Server 2010, group chat functionality was available with Group Chat Server, a third-party trusted application for Lync Server 2010.</span></span> <span data-ttu-id="9790f-171">Lync 2013 クライアントは、Lync Server 2010、グループチャットとは互換性がありません。</span><span class="sxs-lookup"><span data-stu-id="9790f-171">Lync 2013 clients are not compatible with Lync Server 2010, Group Chat.</span></span>

<span data-ttu-id="9790f-172">3Lync Web App 2013 は、コンピューターの音声やビデオなどの完全な会議エクスペリエンスを提供するようになりました。 Lync 2010 の出席者に代わるものと見なされます。</span><span class="sxs-lookup"><span data-stu-id="9790f-172">3Lync Web App 2013 now provides a full in-meeting experience, including computer audio and video, and is considered the replacement for Lync 2010 Attendee.</span></span> <span data-ttu-id="9790f-173">Lync 2010 出席者は、サポートされていないブラウザー (Internet Explorer 6 または Internet Explorer 7) と Windows XP を使用している場合にのみ Lync Server 2013 に接続します。</span><span class="sxs-lookup"><span data-stu-id="9790f-173">Lync 2010 Attendee will connect to Lync Server 2013 only when you are using an unsupported browser (Internet Explorer 6 or Internet Explorer 7) and Windows XP.</span></span>

<span data-ttu-id="9790f-174">4 Office Communicator 2007 R2 のプレゼンス機能と IM 機能は Lync Server 2013 と互換性がありますが、会議機能は使用できません。</span><span class="sxs-lookup"><span data-stu-id="9790f-174">4The presence and IM features in Office Communicator 2007 R2 are compatible with Lync Server 2013, but conferencing features are not.</span></span> <span data-ttu-id="9790f-175">Office Communications Server 2007 R2 からの移行中、Office Communicator 2007 R2 はプレゼンスと IM の相互運用性に適していますが、ユーザーは Lync Web App 2013 を使って Lync Server 2013 会議に参加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9790f-175">During migration from Office Communications Server 2007 R2, Office Communicator 2007 R2 is suitable for presence and IM interoperability, but users should use Lync Web App 2013 to join Lync Server 2013 meetings.</span></span>

<span data-ttu-id="9790f-176">5制限事項については、このトピックで後述する「lync Server 2010 会議での Lync 2013 クライアントの会議機能のサポート」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9790f-176">5 For limitations, see "Conferencing Feature Support for Lync 2013 Clients in Lync Server 2010 Meetings" later in this topic.</span></span>

</div>

<div>

## <a name="interoperability-among-clients"></a><span data-ttu-id="9790f-177">クライアント間の相互運用性</span><span class="sxs-lookup"><span data-stu-id="9790f-177">Interoperability among Clients</span></span>

<span data-ttu-id="9790f-178">Lync Server 2013 リリースでは、さまざまなクライアントバージョンがピアツーピアと会議の両方のシナリオでシームレスに対話できます。</span><span class="sxs-lookup"><span data-stu-id="9790f-178">With the Lync Server 2013 release, various client versions can interact seamlessly in both peer-to-peer and conferencing scenarios.</span></span> <span data-ttu-id="9790f-179">このセクションでは、ユーザーがさまざまなバージョンのクライアントとサーバーを使用している他のユーザーと対話する場合の、使用可能な機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="9790f-179">This section discusses feature availability when users interact with other users who are using different versions of clients and servers.</span></span>

<div>

## <a name="peer-to-peer-feature-support"></a><span data-ttu-id="9790f-180">ピアツーピア機能のサポート</span><span class="sxs-lookup"><span data-stu-id="9790f-180">Peer-to-Peer Feature Support</span></span>

<span data-ttu-id="9790f-181">ピアツーピア機能は、異なるバージョンのサーバーを使用していて、異なるクライアントバージョンを使っているユーザーに対してサポートされています。</span><span class="sxs-lookup"><span data-stu-id="9790f-181">Peer-to-peer features are supported for users who are homed on different versions of the server and who are using different client versions.</span></span> <span data-ttu-id="9790f-182">エンドユーザーエクスペリエンスと利用可能な機能は、ユーザーのクライアントの機能と、ユーザーがサインインしているサーバーのバージョンによって一貫しています。</span><span class="sxs-lookup"><span data-stu-id="9790f-182">The end-user experience and available features are consistent with the capabilities of the user’s client and the version of the server the user is signed in to.</span></span> <span data-ttu-id="9790f-183">つまり、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="9790f-183">In other words:</span></span>

  - <span data-ttu-id="9790f-184">ユーザーが古いクライアントを使って Lync Server 2013 にサインインしている場合、ユーザーの使用経験は同じになります。</span><span class="sxs-lookup"><span data-stu-id="9790f-184">If a user is signed in to Lync Server 2013 with an older client, the user will have the same experience he or she is used to.</span></span> <span data-ttu-id="9790f-185">Lync Server 2013 で導入された新機能は、ユーザーのクライアントがアップグレードされるまで使用できません。</span><span class="sxs-lookup"><span data-stu-id="9790f-185">None of the new features introduced in Lync Server 2013 will be available until the user’s client is upgraded.</span></span> <span data-ttu-id="9790f-186">例としては、ビデオギャラリービュー、HD ビデオ、更新された PowerPoint 共有、すべての参加者の音声とビデオを会議の入力時にミュートするオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="9790f-186">Examples include video gallery view, HD video, updated PowerPoint sharing, and the option to mute all attendee audio and video upon meeting entry.</span></span> <span data-ttu-id="9790f-187">新しい機能については、「 [Lync server 2013 の新しい会議機能](lync-server-2013-new-conferencing-features.md) 」と「 [lync server 2013 でのクライアントの新](lync-server-2013-what-s-new-for-clients.md)機能」で説明しています。</span><span class="sxs-lookup"><span data-stu-id="9790f-187">The new features are outlined in [New conferencing features in Lync Server 2013](lync-server-2013-new-conferencing-features.md) and [What's new for clients in Lync Server 2013](lync-server-2013-what-s-new-for-clients.md).</span></span>

  - <span data-ttu-id="9790f-188">ユーザーが lync 2013 クライアントを使って Lync Server 2010 にサインインしている場合、lync server 2010 でサポートされていないすべての新機能は、ユーザーが Lync Server 2013 に移動されるまで使用できません。</span><span class="sxs-lookup"><span data-stu-id="9790f-188">If a user is signed in to Lync Server 2010 with a Lync 2013 client, any new features not supported by Lync Server 2010 will be unavailable until the user is moved to Lync Server 2013.</span></span>

<span data-ttu-id="9790f-189">次の表では、クライアントが Lync Server 2013 または Lync Server 2010 のいずれかにサインインしているピアツーピアセッションの機能の可用性を比較します。</span><span class="sxs-lookup"><span data-stu-id="9790f-189">The following table compares feature availability in peer-to-peer sessions where the client is signed in to either Lync Server 2013 or Lync Server 2010.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="9790f-190">Lync Web App と Lync 2010 の出席者は会議専用クライアントであり、この表には含まれていません。</span><span class="sxs-lookup"><span data-stu-id="9790f-190">Lync Web App and Lync 2010 Attendee are meeting-only clients and aren’t included in this table.</span></span>



</div>


<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9790f-191">クライアント</span><span class="sxs-lookup"><span data-stu-id="9790f-191">Client</span></span></th>
<th><span data-ttu-id="9790f-192">インスタントメッセージ (im)</span><span class="sxs-lookup"><span data-stu-id="9790f-192">Instant Messaging</span></span></th>
<th><span data-ttu-id="9790f-193">プレゼンス</span><span class="sxs-lookup"><span data-stu-id="9790f-193">Presence</span></span></th>
<th><span data-ttu-id="9790f-194">音声</span><span class="sxs-lookup"><span data-stu-id="9790f-194">Voice</span></span></th>
<th><span data-ttu-id="9790f-195">ビデオ</span><span class="sxs-lookup"><span data-stu-id="9790f-195">Video</span></span></th>
<th><span data-ttu-id="9790f-196">アプリケーション共有</span><span class="sxs-lookup"><span data-stu-id="9790f-196">Application Sharing</span></span></th>
<th><span data-ttu-id="9790f-197">ファイル送信</span><span class="sxs-lookup"><span data-stu-id="9790f-197">File Transfer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9790f-198">Lync 2013</span><span class="sxs-lookup"><span data-stu-id="9790f-198">Lync 2013</span></span></p></td>
<td><p><span data-ttu-id="9790f-199">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-199">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-200">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-200">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-201">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-201">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-202">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-202">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-203">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-203">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-204">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-204">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9790f-205">Lync 2013 Basic</span><span class="sxs-lookup"><span data-stu-id="9790f-205">Lync 2013 Basic</span></span></p></td>
<td><p><span data-ttu-id="9790f-206">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-206">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-207">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-207">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-208">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-208">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-209">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-209">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-210">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-210">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-211">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-211">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9790f-212">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="9790f-212">Lync 2010</span></span></p></td>
<td><p><span data-ttu-id="9790f-213">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-213">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-214">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-214">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-215">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-215">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-216">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-216">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-217">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-217">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-218">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-218">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9790f-219">Lync 2010 Attendant</span><span class="sxs-lookup"><span data-stu-id="9790f-219">Lync 2010 Attendant</span></span></p></td>
<td><p><span data-ttu-id="9790f-220">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-220">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-221">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-221">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-222">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-222">Yes</span></span></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9790f-223">Lync 2010 Mobile</span><span class="sxs-lookup"><span data-stu-id="9790f-223">Lync 2010 Mobile</span></span></p></td>
<td><p><span data-ttu-id="9790f-224">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-224">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-225">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-225">Yes</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9790f-226">Lync Phone Edition</span><span class="sxs-lookup"><span data-stu-id="9790f-226">Lync Phone Edition</span></span></p></td>
<td><p><span data-ttu-id="9790f-227">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-227">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-228">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-228">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-229">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-229">Yes</span></span></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9790f-230">Office Communicator 2007 R2</span><span class="sxs-lookup"><span data-stu-id="9790f-230">Office Communicator 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="9790f-231">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-231">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-232">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-232">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-233">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-233">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-234">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-234">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-235">はい1</span><span class="sxs-lookup"><span data-stu-id="9790f-235">Yes1</span></span></p></td>
<td><p><span data-ttu-id="9790f-236">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-236">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9790f-237">パブリック IM (AOL、Yahoo!)</span><span class="sxs-lookup"><span data-stu-id="9790f-237">Public IM (AOL, Yahoo!)</span></span></p></td>
<td><p><span data-ttu-id="9790f-238">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-238">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-239">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-239">Yes</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9790f-240">パブリック IM (MSN、Windows Live Messenger)</span><span class="sxs-lookup"><span data-stu-id="9790f-240">Public IM (MSN, Windows Live Messenger)</span></span></p></td>
<td><p><span data-ttu-id="9790f-241">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-241">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-242">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-242">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-243">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-243">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-244">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-244">Yes</span></span></p></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>


<div>


> [!IMPORTANT]  
> <UL>
> <LI>
> <P><span data-ttu-id="9790f-245">2012年9月1日以降、Microsoft Lync パブリック IM 接続ユーザーサブスクリプションライセンス (PIC USL) は、新規または更新契約の購入に使用できなくなりました。</span><span class="sxs-lookup"><span data-stu-id="9790f-245">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (PIC USL) is no longer available for the purchase for new or renewing agreements.</span></span> <span data-ttu-id="9790f-246">アクティブなライセンスを持っているお客様は、Yahoo! とのフェデレーションを継続できます。</span><span class="sxs-lookup"><span data-stu-id="9790f-246">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="9790f-247">サービスのシャットダウン日までメッセンジャーを終了します。</span><span class="sxs-lookup"><span data-stu-id="9790f-247">Messenger until the service shutdown date.</span></span> <span data-ttu-id="9790f-248">AOL および Yahoo! の2014年6月の終了日</span><span class="sxs-lookup"><span data-stu-id="9790f-248">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="9790f-249">が発表されました。</span><span class="sxs-lookup"><span data-stu-id="9790f-249">has been announced.</span></span> <span data-ttu-id="9790f-250">詳細については、「 <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Lync Server 2013 でのパブリックインスタントメッセンジャー接続のサポート</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9790f-250">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>..</span></span></P>
> <LI>
> <P><span data-ttu-id="9790f-251">PIC USL は、Lync Server または Office Communications Server が Yahoo! とのフェデレーションを行うために必要なユーザーごとの1か月間のサブスクリプションライセンスです。</span><span class="sxs-lookup"><span data-stu-id="9790f-251">The PIC USL is a per-user, per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="9790f-252">Messenger.</span><span class="sxs-lookup"><span data-stu-id="9790f-252">Messenger.</span></span> <span data-ttu-id="9790f-253">このサービスを提供するための Microsoft の機能は、Yahoo! からのサポートによって決定されましたが、その基となる契約は更新されません。</span><span class="sxs-lookup"><span data-stu-id="9790f-253">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which will not be renewed.</span></span></P>
> <LI>
> <P><span data-ttu-id="9790f-254">Lync は、組織間、および世界各地の個人と接続するための強力なツールです。</span><span class="sxs-lookup"><span data-stu-id="9790f-254">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="9790f-255">Windows Live Messenger とのフェデレーションには、Lync 標準 CAL 以外の追加のユーザー/デバイスライセンスは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="9790f-255">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="9790f-256">Skype federation はこのリストに追加されるため、Lync ユーザーは IM や音声を通じて数百人の何百万ものユーザーに連絡できます。</span><span class="sxs-lookup"><span data-stu-id="9790f-256">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people through IM and voice.</span></span></P></LI></UL>



</div>

<span data-ttu-id="9790f-257">1 Office Communicator 2007 R2 では、デスクトップ共有 (プログラムによる共有ではない) のみを使用できます。</span><span class="sxs-lookup"><span data-stu-id="9790f-257">1 In Office Communicator 2007 R2, only desktop sharing (and not program sharing) is available.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="9790f-258">Skype for Business 2015 クライアントのユーザーインターフェイスが適用されている場合、Office Communicator 2007 R2 と Skype for Business 2015 の間のデスクトップ共有を新しいクライアントから開始することはできません。</span><span class="sxs-lookup"><span data-stu-id="9790f-258">Desktop sharing between Office Communicator 2007 R2 and Skype for Business 2015 cannot be initiated from the newer client when the Skype for Business 2015 client user interface is enforced.</span></span>



</div>

</div>

<div>

## <a name="conferencing-feature-support-for-lync-2013-clients-in-lync-server-2010-meetings"></a><span data-ttu-id="9790f-259">Lync Server 2010 会議での Lync 2013 クライアントの会議機能のサポート</span><span class="sxs-lookup"><span data-stu-id="9790f-259">Conferencing Feature Support for Lync 2013 Clients in Lync Server 2010 Meetings</span></span>

<span data-ttu-id="9790f-260">Lync 2013 クライアントを使って Lync Server 2010 会議に参加している場合、lync 2013 クライアントの機能にアクセスできますが、次の例外があります。</span><span class="sxs-lookup"><span data-stu-id="9790f-260">When users join Lync Server 2010 meetings with a Lync 2013 client, they have access to Lync 2013 client features with the following exceptions:</span></span>

  - <span data-ttu-id="9790f-261">[会議] ウィンドウの [連絡先] アイコンをポイントしてアクセスできる **参加者** の管理オプションでは、[ **会議 IM** を使わない] オプションは機能しません。</span><span class="sxs-lookup"><span data-stu-id="9790f-261">In the **Participants** management options, which are accessible by pointing to the people icon in the meeting window, the **No Meeting IM** option does not function.</span></span>

  - <span data-ttu-id="9790f-262">ギャラリービューは、ビデオ会議では機能しません。</span><span class="sxs-lookup"><span data-stu-id="9790f-262">Gallery View does not function in video conferences.</span></span> <span data-ttu-id="9790f-263">ユーザーは、すべてのスピーカーではなく、アクティブなスピーカーのみを表示します。</span><span class="sxs-lookup"><span data-stu-id="9790f-263">The user sees only the active speaker instead of all speakers.</span></span> <span data-ttu-id="9790f-264">[ **レイアウトの選択** ] オプションの一覧で、 **ギャラリービュー** を使用できない</span><span class="sxs-lookup"><span data-stu-id="9790f-264">In the list of **Pick a Layout** options, **Gallery View** is unavailable</span></span>

  - <span data-ttu-id="9790f-265">参加者リストは、ビデオ会議の既定で表示されます。</span><span class="sxs-lookup"><span data-stu-id="9790f-265">The participant list displays by default in video conferences.</span></span>

  - <span data-ttu-id="9790f-266">[参加者] リストでユーザーを右クリックすると、[ **ビデオスポットライトをロック** する] と [ **ギャラリーに参加するための Pin** ] オプションは使用できません。</span><span class="sxs-lookup"><span data-stu-id="9790f-266">When right-clicking a user in the participants list, the **Lock the Video Spotlight** and **Pin to Gallery** participant management options are unavailable.</span></span>

</div>

<div>

## <a name="conferencing-feature-support-in-lync-server-2013-meetings"></a><span data-ttu-id="9790f-267">Lync Server 2013 会議での会議機能のサポート</span><span class="sxs-lookup"><span data-stu-id="9790f-267">Conferencing Feature Support in Lync Server 2013 Meetings</span></span>

<span data-ttu-id="9790f-268">Lync Server 2013 には、アカウントを Lync Server 2013 に移行した後でユーザーが利用できる新しい会議機能が用意されています。また、lync 2013 クライアントでサインインします。</span><span class="sxs-lookup"><span data-stu-id="9790f-268">Lync Server 2013 provides new conferencing features that become available to users after their accounts are moved to Lync Server 2013 and they sign in with the Lync 2013 client.</span></span> <span data-ttu-id="9790f-269">例としては、ビデオギャラリービュー、HD ビデオ、PowerPoint 共有、すべての出席者の音声とビデオを会議の入力時にミュートするオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="9790f-269">Examples include video gallery view, HD video, PowerPoint sharing, and the option to mute all attendee audio and video upon meeting entry.</span></span> <span data-ttu-id="9790f-270">新しい機能については、「 [Lync server 2013 の新しい会議機能](lync-server-2013-new-conferencing-features.md) 」と「 [lync server 2013 でのクライアントの新](lync-server-2013-what-s-new-for-clients.md)機能」で説明しています。</span><span class="sxs-lookup"><span data-stu-id="9790f-270">The new features are outlined in [New conferencing features in Lync Server 2013](lync-server-2013-new-conferencing-features.md) and [What's new for clients in Lync Server 2013](lync-server-2013-what-s-new-for-clients.md).</span></span>

<span data-ttu-id="9790f-271">Lync Server 2013 会議では、特定の会議機能が、さまざまなバージョンのサーバーを使用していて、異なるクライアントとクライアントバージョンを使っているユーザーがサポートしています。</span><span class="sxs-lookup"><span data-stu-id="9790f-271">In Lync Server 2013 meetings, certain conferencing features are supported for users who are homed on different versions of the server and who are using different clients and client versions.</span></span> <span data-ttu-id="9790f-272">クライアントが Lync Server 2013 会議に参加すると、ユーザーは次の表に示す機能にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="9790f-272">When clients join a Lync Server 2013 meeting, users have access to the features and capabilities shown in this table.</span></span>


<table style="width:100%;">
<colgroup>
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9790f-273">クライアント</span><span class="sxs-lookup"><span data-stu-id="9790f-273">Client</span></span></th>
<th><span data-ttu-id="9790f-274">ピアツーピア IM</span><span class="sxs-lookup"><span data-stu-id="9790f-274">Peer-to-peer IM</span></span></th>
<th><span data-ttu-id="9790f-275">音声</span><span class="sxs-lookup"><span data-stu-id="9790f-275">Voice</span></span></th>
<th><span data-ttu-id="9790f-276">ビデオ</span><span class="sxs-lookup"><span data-stu-id="9790f-276">Video</span></span></th>
<th><span data-ttu-id="9790f-277">アプリケーション共有</span><span class="sxs-lookup"><span data-stu-id="9790f-277">Application Sharing</span></span></th>
<th><span data-ttu-id="9790f-278">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="9790f-278">PowerPoint</span></span></th>
<th><span data-ttu-id="9790f-279">ファイル送信</span><span class="sxs-lookup"><span data-stu-id="9790f-279">File Transfer</span></span></th>
<th><span data-ttu-id="9790f-280">Whiteboard</span><span class="sxs-lookup"><span data-stu-id="9790f-280">Whiteboard</span></span></th>
<th><span data-ttu-id="9790f-281">ポーリング</span><span class="sxs-lookup"><span data-stu-id="9790f-281">Polling</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9790f-282">Lync 2013</span><span class="sxs-lookup"><span data-stu-id="9790f-282">Lync 2013</span></span></p></td>
<td><p><span data-ttu-id="9790f-283">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-283">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-284">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-284">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-285">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-285">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-286">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-286">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-287">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-287">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-288">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-288">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-289">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-289">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-290">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-290">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9790f-291">Lync 2013 Basic</span><span class="sxs-lookup"><span data-stu-id="9790f-291">Lync 2013 Basic</span></span></p></td>
<td><p><span data-ttu-id="9790f-292">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-292">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-293">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-293">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-294">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-294">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-295">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-295">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-296">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-296">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-297">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-297">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-298">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-298">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-299">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-299">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9790f-300">Lync Web App</span><span class="sxs-lookup"><span data-stu-id="9790f-300">Lync Web App</span></span></p></td>
<td><p><span data-ttu-id="9790f-301">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-301">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-302">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-302">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-303">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-303">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-304">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-304">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-305">はい2</span><span class="sxs-lookup"><span data-stu-id="9790f-305">Yes2</span></span></p></td>
<td><p><span data-ttu-id="9790f-306">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-306">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-307">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-307">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-308">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-308">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9790f-309">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="9790f-309">Lync 2010</span></span></p></td>
<td><p><span data-ttu-id="9790f-310">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-310">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-311">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-311">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-312">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-312">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-313">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-313">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-314">はい3</span><span class="sxs-lookup"><span data-stu-id="9790f-314">Yes3</span></span></p></td>
<td><p><span data-ttu-id="9790f-315">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-315">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-316">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-316">Yes</span></span></p></td>
<td><p><span data-ttu-id="9790f-317">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-317">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9790f-318">Office Communicator 2007 R2 4</span><span class="sxs-lookup"><span data-stu-id="9790f-318">Office Communicator 2007 R2 4</span></span></p></td>
<td><p><span data-ttu-id="9790f-319">はい</span><span class="sxs-lookup"><span data-stu-id="9790f-319">Yes</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9790f-320">1 Office Communicator 2007 R2 では、デスクトップ共有 (プログラムによる共有ではない) のみを使用できます。</span><span class="sxs-lookup"><span data-stu-id="9790f-320">1 In Office Communicator 2007 R2, only desktop sharing (and not program sharing) is available.</span></span>

<span data-ttu-id="9790f-321">2 Lync Server 2013 では、PowerPoint ファイルをアップロードするためのメカニズムが更新されています。</span><span class="sxs-lookup"><span data-stu-id="9790f-321">2 Lync Server 2013 uses an updated mechanism for uploading PowerPoint files.</span></span> <span data-ttu-id="9790f-322">Lync Server 2010 でスケジュールされていた会議に参加した lync Web App ユーザーは、PowerPoint プレゼンテーションを表示したり、移動したりすることはできますが、PowerPoint ファイルをアップロードすることはできません。</span><span class="sxs-lookup"><span data-stu-id="9790f-322">Lync Web App users who join a meeting that was originally scheduled on Lync Server 2010 can view and navigate PowerPoint presentations, but cannot upload PowerPoint files.</span></span>

<span data-ttu-id="9790f-323">3 lync Server 2013 で会議がスケジュールされていて、PowerPoint スライドが Lync 2013 クライアントによってアップロードされている場合、Lync 2010 ユーザーは、スライドへの表示のみのアクセス権を持っています。</span><span class="sxs-lookup"><span data-stu-id="9790f-323">3 If the meeting was scheduled on Lync Server 2013 and PowerPoint slides were uploaded by a Lync 2013 client, Lync 2010 users have view-only access to the slides.</span></span> <span data-ttu-id="9790f-324">これに対して、PowerPoint スライドが Lync 2010 ユーザーによってアップロードされた場合、Lync Server 2013 ユーザーは表示およびスライドにアクセスでき、Office Web Apps サーバーが構成されていれば、高解像度のディスプレイ、アニメーション、スライド切り替え、埋め込みビデオなどの新しい機能にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="9790f-324">Conversely, if the PowerPoint slides were uploaded by a Lync 2010 user, Lync Server 2013 users will be able to view and slides and, if Office Web Apps Server is configured, access new capabilities such as higher resolution display, animations, slide transitions, and embedded video.</span></span> <span data-ttu-id="9790f-325">詳細については、「 [Office Web Apps サーバーおよび Lync server 2013 との統合を構成する](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9790f-325">For more information, see [Configuring integration with Office Web Apps Server and Lync Server 2013](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md).</span></span>

<span data-ttu-id="9790f-326">4 Office Communicator 2007 R2 のプレゼンス機能と IM 機能は Lync Server 2013 と互換性がありますが、会議機能は使用できません。</span><span class="sxs-lookup"><span data-stu-id="9790f-326">4The presence and IM features in Office Communicator 2007 R2 are compatible with Lync Server 2013, but conferencing features are not.</span></span> <span data-ttu-id="9790f-327">Office Communications Server 2007 R2 からの移行中、Office Communicator 2007 R2 はプレゼンスと IM の相互運用性に適していますが、ユーザーは Lync Web App 2013 を使って Lync Server 2013 会議に参加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9790f-327">During migration from Office Communications Server 2007 R2, Office Communicator 2007 R2 is suitable for presence and IM interoperability, but users should use Lync Web App 2013 to join Lync Server 2013 meetings.</span></span>

</div>

</div>

<div>

## <a name="scheduling-add-in-support"></a><span data-ttu-id="9790f-328">アドインのサポートのスケジュール</span><span class="sxs-lookup"><span data-stu-id="9790f-328">Scheduling Add-in Support</span></span>

<span data-ttu-id="9790f-329">各種のスケジュールアドインに対するサーバーのサポートは、サーバーとクライアントのバージョンの互換性と一貫性があります。</span><span class="sxs-lookup"><span data-stu-id="9790f-329">Server support for the various scheduling add-ins is consistent with server and client version compatibility.</span></span> <span data-ttu-id="9790f-330">一般的に、次のスケジュールのアドインは Lync Server 2013 でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="9790f-330">In general, the following scheduling add-ins are supported on Lync Server 2013.</span></span> <span data-ttu-id="9790f-331">ただし、以前のバージョンのアドインでは、会議エントリにあるすべての出席者の音声とビデオをミュートするオプションなどの新しい Lync 2013 アドイン機能は提供されていません。</span><span class="sxs-lookup"><span data-stu-id="9790f-331">However, previous versions of add-ins do not provide new Lync 2013 add-in features, such as the option to mute all attendee audio and video upon meeting entry.</span></span>

  - <span data-ttu-id="9790f-332">**Lync 2013 用のオンライン会議アドイン**   Lync 2010 用のオンライン会議アドインと同じ機能が用意されており、出席者のミュートコントロールを追加しています。この機能を使うと、会議の開催者は、出席者の音声とビデオが既定でミュートになっている会議のスケジュールを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="9790f-332">**Online Meeting Add-in for Lync 2013**   Provides the same features as the Online Meeting Add-in for Lync 2010, with the addition of attendee mute controls, which allow meeting organizers to schedule conferences that have attendee audio and video muted by default.</span></span> <span data-ttu-id="9790f-333">管理者は、カスタムロゴ、サポート URL、法的免責事項 URL、またはカスタムフッターテキストを追加して、組織の会議出席依頼をカスタマイズすることもできます。</span><span class="sxs-lookup"><span data-stu-id="9790f-333">Administrators can also customize the organization’s meeting invitations by adding a custom logo, a support URL, a legal disclaimer URL, or custom footer text.</span></span>

  - <span data-ttu-id="9790f-334">**Lync 2010 用のオンライン会議アドイン**   Lync 会議のスケジュールを提供し、Office Live Meeting 会議のスケジュール機能を削除します。</span><span class="sxs-lookup"><span data-stu-id="9790f-334">**Online Meeting Add-in for Lync 2010**   Provides scheduling for Lync meetings and removes the capability to schedule Office Live Meeting conferences.</span></span>

  - <span data-ttu-id="9790f-335">**Office Communicator 2007 R2 会議アドイン**   Office Live Meeting 会議と Office Communicator 2007 R2 会議の両方のスケジュールを提供します。</span><span class="sxs-lookup"><span data-stu-id="9790f-335">**Office Communicator 2007 R2 Conferencing Add-in**   Provides scheduling for both Office Live Meeting conferences and Office Communicator 2007 R2 conferences.</span></span> 

<div>


> [!NOTE]  
> <span data-ttu-id="9790f-336">Lync Server 2013 で Live Meeting の会議をスケジュールすることはできません。</span><span class="sxs-lookup"><span data-stu-id="9790f-336">Live Meeting conferences cannot be scheduled on Lync Server 2013.</span></span>



</div>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9790f-337">クライアントのスケジュール</span><span class="sxs-lookup"><span data-stu-id="9790f-337">Scheduling Client</span></span></th>
<th><span data-ttu-id="9790f-338">Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9790f-338">Lync Server 2013</span></span></th>
<th><span data-ttu-id="9790f-339">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="9790f-339">Lync Server 2010</span></span></th>
<th><span data-ttu-id="9790f-340">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="9790f-340">Office Communications Server 2007 R2</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9790f-341">Lync 2013 用のオンライン会議アドイン (Office 2013、Outlook 2010、Outlook 2007 で使用可能)</span><span class="sxs-lookup"><span data-stu-id="9790f-341">Online Meeting Add-in for Lync 2013 (can be used with Office 2013, Outlook 2010, and Outlook 2007)</span></span></p></td>
<td><p><span data-ttu-id="9790f-342">サポート</span><span class="sxs-lookup"><span data-stu-id="9790f-342">Supported</span></span></p></td>
<td><p><span data-ttu-id="9790f-343">サポートされています (新しいアドイン機能は使用できません)</span><span class="sxs-lookup"><span data-stu-id="9790f-343">Supported (new add-in features not available)</span></span></p></td>
<td><p><span data-ttu-id="9790f-344">非サポート</span><span class="sxs-lookup"><span data-stu-id="9790f-344">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9790f-345">Lync 2013 Web Scheduler</span><span class="sxs-lookup"><span data-stu-id="9790f-345">Lync 2013 Web Scheduler</span></span></p></td>
<td><p><span data-ttu-id="9790f-346">サポート対象</span><span class="sxs-lookup"><span data-stu-id="9790f-346">Supported</span></span></p></td>
<td><p><span data-ttu-id="9790f-347">サポート対象外</span><span class="sxs-lookup"><span data-stu-id="9790f-347">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="9790f-348">サポート対象外</span><span class="sxs-lookup"><span data-stu-id="9790f-348">Not Supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9790f-349">Lync 2010 用オンライン ミーティング アドイン</span><span class="sxs-lookup"><span data-stu-id="9790f-349">Online Meeting Add-in for Lync 2010</span></span></p></td>
<td><p><span data-ttu-id="9790f-350">サポート</span><span class="sxs-lookup"><span data-stu-id="9790f-350">Supported</span></span></p></td>
<td><p><span data-ttu-id="9790f-351">サポート対象</span><span class="sxs-lookup"><span data-stu-id="9790f-351">Supported</span></span></p></td>
<td><p><span data-ttu-id="9790f-352">サポート対象外</span><span class="sxs-lookup"><span data-stu-id="9790f-352">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9790f-353">Office Communicator 2007 R2 会議アドイン</span><span class="sxs-lookup"><span data-stu-id="9790f-353">Office Communicator 2007 R2 Conferencing Add-in</span></span></p></td>
<td><p><span data-ttu-id="9790f-354">非サポート</span><span class="sxs-lookup"><span data-stu-id="9790f-354">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="9790f-355">サポート</span><span class="sxs-lookup"><span data-stu-id="9790f-355">Supported</span></span></p></td>
<td><p><span data-ttu-id="9790f-356">サポート</span><span class="sxs-lookup"><span data-stu-id="9790f-356">Supported</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="support-for-joining-meetings"></a><span data-ttu-id="9790f-357">会議への参加のサポート</span><span class="sxs-lookup"><span data-stu-id="9790f-357">Support for Joining Meetings</span></span>

<span data-ttu-id="9790f-358">Lync Server 2013 でサポートされているすべてのクライアントは、Lync 2013 会議に参加することができます。</span><span class="sxs-lookup"><span data-stu-id="9790f-358">All of the clients that Lync Server 2013 supports are allowed to join Lync 2013 meetings.</span></span> <span data-ttu-id="9790f-359">Lync Web App はサーバーの Web コンポーネントであるため、lync Web App を使って Lync Server 2013 会議に参加している場合は、新しいバージョンの Lync Web App が常に使用されます。</span><span class="sxs-lookup"><span data-stu-id="9790f-359">Because Lync Web App is a web component of the server, in cases where Lync Web App is used to join a Lync Server 2013 meeting, the newer version of Lync Web App is always used.</span></span>

<span data-ttu-id="9790f-360">Lync 2013 クライアントは、スケールダウン機能を使用して、Lync 2010 および Office Communications Server 2007 R2 でホストされている会議に参加できます。</span><span class="sxs-lookup"><span data-stu-id="9790f-360">Lync 2013 clients can join meetings hosted on Lync 2010 and Office Communications Server 2007 R2 with scaled-down functionality.</span></span> <span data-ttu-id="9790f-361">会議中機能は、会議がホストされているサーバーのバージョンによって制限されます。</span><span class="sxs-lookup"><span data-stu-id="9790f-361">In-meeting features are limited by the version of the server on which the meeting is hosted.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="9790f-362">関連項目</span><span class="sxs-lookup"><span data-stu-id="9790f-362">See Also</span></span>


[<span data-ttu-id="9790f-363">Lync Server 2013 の lync Windows ストアアプリの要件</span><span class="sxs-lookup"><span data-stu-id="9790f-363">Lync Windows Store app requirements for Lync Server 2013</span></span>](lync-server-2013-lync-windows-store-app-requirements.md)  
[<span data-ttu-id="9790f-364">Lync Server 2013 の新しい会議機能</span><span class="sxs-lookup"><span data-stu-id="9790f-364">New conferencing features in Lync Server 2013</span></span>](lync-server-2013-new-conferencing-features.md)  
[<span data-ttu-id="9790f-365">Lync Server 2013 のクライアント向けの新機能</span><span class="sxs-lookup"><span data-stu-id="9790f-365">What's new for clients in Lync Server 2013</span></span>](lync-server-2013-what-s-new-for-clients.md)  
  

<span data-ttu-id="9790f-366"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9790f-366"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

