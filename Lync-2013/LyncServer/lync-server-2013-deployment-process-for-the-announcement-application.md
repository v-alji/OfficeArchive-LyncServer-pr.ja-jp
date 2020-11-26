---
title: 'Lync Server 2013: アナウンスメントアプリケーションの展開プロセス'
description: 'Lync Server 2013: アナウンスメントアプリケーションの展開プロセス。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment process for the Announcement application
ms:assetid: 72c66249-c4ce-48ce-b1b9-90ebf77d7805
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398545(v=OCS.15)
ms:contentKeyID: 48184500
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 559977c32f63fae312164b5b0c36698fa13afb09
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429644"
---
# <a name="deployment-process-for-the-announcement-application-in-lync-server-2013"></a><span data-ttu-id="68144-103">Lync Server 2013 のアナウンスメントアプリケーションの展開プロセス</span><span class="sxs-lookup"><span data-stu-id="68144-103">Deployment process for the Announcement application in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="68144-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="68144-104">

<span> </span></span></span>

<span data-ttu-id="68144-105">_**最終更新日:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="68144-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="68144-106">このセクションでは、アナウンスメントアプリケーションの展開に関連する手順の概要を説明します。</span><span class="sxs-lookup"><span data-stu-id="68144-106">This section provides an overview of the steps involved in deploying the Announcement application.</span></span> <span data-ttu-id="68144-107">お知らせを構成する前に、エンタープライズボイスを展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="68144-107">You must deploy Enterprise Voice before you configure announcements.</span></span> <span data-ttu-id="68144-108">[エンタープライズ Voip] を展開すると、アナウンスメントアプリケーションで必要なコンポーネントがインストールされて有効になります。</span><span class="sxs-lookup"><span data-stu-id="68144-108">The components required by the Announcement application are installed and enabled when you deploy Enterprise Voice.</span></span>

### <a name="announcement-deployment-process"></a><span data-ttu-id="68144-109">アナウンスの展開プロセス</span><span class="sxs-lookup"><span data-stu-id="68144-109">Announcement Deployment Process</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="68144-110">フェーズ</span><span class="sxs-lookup"><span data-stu-id="68144-110">Phase</span></span></th>
<th><span data-ttu-id="68144-111">手順</span><span class="sxs-lookup"><span data-stu-id="68144-111">Steps</span></span></th>
<th><span data-ttu-id="68144-112">役割</span><span class="sxs-lookup"><span data-stu-id="68144-112">Roles</span></span></th>
<th><span data-ttu-id="68144-113">「展開」のドキュメント</span><span class="sxs-lookup"><span data-stu-id="68144-113">Deployment documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="68144-114">アナウンス設定の構成</span><span class="sxs-lookup"><span data-stu-id="68144-114">Configure Announcement settings</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="68144-115">オーディオ ファイルをレコーディングして読み込むか、音声合成 (TTS) を使用して、アナウンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="68144-115">Create the announcement by recording and uploading audio files or by using text-to-speech (TTS).</span></span></p></li>
<li><p><span data-ttu-id="68144-116">割り当てられていない番号の表で、割り当てられていない番号の範囲を構成して、適切なアナウンスに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="68144-116">Configure the unassigned number ranges in the unassigned number table and associate them with the appropriate announcement.</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="68144-117">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="68144-117">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="68144-118">CsVoiceAdministrator</span><span class="sxs-lookup"><span data-stu-id="68144-118">CsVoiceAdministrator</span></span></p>
<p><span data-ttu-id="68144-119">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="68144-119">CsServerAdministrator</span></span></p>
<p><span data-ttu-id="68144-120">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="68144-120">CsAdministrator</span></span></p>
<p><span data-ttu-id="68144-121">CsViewOnlyAdministrator</span><span class="sxs-lookup"><span data-stu-id="68144-121">CsViewOnlyAdministrator</span></span></p></td>
<td><p><span data-ttu-id="68144-122"><a href="lync-server-2013-create-an-announcement.md">Lync Server 2013 でお知らせを作成する</a></span><span class="sxs-lookup"><span data-stu-id="68144-122"><a href="lync-server-2013-create-an-announcement.md">Create an announcement in Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="68144-123"><a href="lync-server-2013-configure-the-unassigned-number-table.md">Lync Server 2013 での割り当てられていない番号の表の構成</a></span><span class="sxs-lookup"><span data-stu-id="68144-123"><a href="lync-server-2013-configure-the-unassigned-number-table.md">Configure the unassigned number table in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="68144-124">アナウンスの展開の確認</span><span class="sxs-lookup"><span data-stu-id="68144-124">Verify your Announcement deployment</span></span></p></td>
<td><p><span data-ttu-id="68144-125">アナウンスを聞いてテストし、構成が予想どおりに動作することを確認します。</span><span class="sxs-lookup"><span data-stu-id="68144-125">Test by listening to announcements to verify that your configuration works as expected.</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="68144-126"><a href="lync-server-2013-optional-verify-announcement-deployment.md">省略Lync Server 2013 でのアナウンスメントの展開を確認する</a></span><span class="sxs-lookup"><span data-stu-id="68144-126"><a href="lync-server-2013-optional-verify-announcement-deployment.md">(Optional) Verify Announcement deployment in Lync Server 2013</a></span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="68144-127">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="68144-127">


</div>

<span> </span>

</div>

</div>

</span></span></div>

