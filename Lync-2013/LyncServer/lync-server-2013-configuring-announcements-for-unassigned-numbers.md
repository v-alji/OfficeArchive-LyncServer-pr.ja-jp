---
title: 'Lync Server 2013: 割り当てられていない番号用のアナウンスの構成'
description: 'Lync Server 2013: 未割り当ての番号のお知らせを構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring announcements for unassigned numbers
ms:assetid: 45633dd3-78de-4934-867e-33969fc25368
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425944(v=OCS.15)
ms:contentKeyID: 48184035
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 16ab636f0c6157118a00d5e46521555086c5e520
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399176"
---
# <a name="configuring-announcements-for-unassigned-numbers-in-lync-server-2013"></a><span data-ttu-id="b9b0e-103">Lync Server 2013 での、割り当てられていない番号用のアナウンスの構成</span><span class="sxs-lookup"><span data-stu-id="b9b0e-103">Configuring announcements for unassigned numbers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b9b0e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b9b0e-104">

<span> </span></span></span>

<span data-ttu-id="b9b0e-105">_**最終更新日:** 2012-09-11_</span><span class="sxs-lookup"><span data-stu-id="b9b0e-105">_**Topic Last Modified:** 2012-09-11_</span></span>

<span data-ttu-id="b9b0e-106">アナウンスメントアプリケーションは、割り当てられていない拡張子 (組織に対して有効であり、ユーザーまたは電話に割り当てられていない拡張機能) への呼び出しを構成できるエンタープライズ Voip 機能です。</span><span class="sxs-lookup"><span data-stu-id="b9b0e-106">The Announcement application is an Enterprise Voice feature that enables you to configure what happens to calls to unassigned extensions (extensions that are valid for your organization, but are not assigned to a person or a phone).</span></span> <span data-ttu-id="b9b0e-107">たとえば、割り当てられていない番号に通話があった場合にメッセージを再生したり、別の通話先に転送したり、その両方を行ったりするように構成できます。</span><span class="sxs-lookup"><span data-stu-id="b9b0e-107">For example, you can configure calls to unassigned numbers to play a message, or to be transferred to a different destination, or both.</span></span>

<span data-ttu-id="b9b0e-108">お知らせアプリケーションは、エンタープライズボイスの展開時に、フロントエンドサーバーまたは Standard Edition サーバー上の応答グループアプリケーションの機能としてインストールされます。</span><span class="sxs-lookup"><span data-stu-id="b9b0e-108">The Announcement application is installed as a feature of Response Group application on the Front End Server or Standard Edition server when you deploy Enterprise Voice.</span></span> <span data-ttu-id="b9b0e-109">オーディオ ファイルをアップロードするか音声合成 (TTS) を構成して、割り当てられていない番号の表を構成し、アナウンスを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9b0e-109">You need to configure Announcements by uploading your audio files or by configuring text-to-speech (TTS) and configuring the unassigned number table.</span></span>

<span data-ttu-id="b9b0e-110">このセクションでは、Lync Server のお知らせを構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b9b0e-110">This section guides you through the configuration of Lync Server Announcements.</span></span> <span data-ttu-id="b9b0e-111">ここでは、お知らせに関連する計画セクションを既に読んでいて、enterprise Edition サーバーまたはエンタープライズ Voip サーバーを展開していることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="b9b0e-111">It assumes that you have already read the planning sections related to Announcements and deployed an Enterprise Edition server or a Standard Edition server with Enterprise Voice.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="b9b0e-112">このセクション中</span><span class="sxs-lookup"><span data-stu-id="b9b0e-112">In This Section</span></span>

  - [<span data-ttu-id="b9b0e-113">Lync Server 2013 のアナウンスの構成の前提条件と役割</span><span class="sxs-lookup"><span data-stu-id="b9b0e-113">Announcement configuration prerequisites and roles in Lync Server 2013</span></span>](lync-server-2013-announcement-configuration-prerequisites-and-roles.md)

  - [<span data-ttu-id="b9b0e-114">Lync Server 2013 のアナウンスメントアプリケーションの展開プロセス</span><span class="sxs-lookup"><span data-stu-id="b9b0e-114">Deployment process for the Announcement application in Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-the-announcement-application.md)

  - [<span data-ttu-id="b9b0e-115">Lync Server 2013 でお知らせを作成する</span><span class="sxs-lookup"><span data-stu-id="b9b0e-115">Create an announcement in Lync Server 2013</span></span>](lync-server-2013-create-an-announcement.md)

  - [<span data-ttu-id="b9b0e-116">Lync Server 2013 での割り当てられていない番号の表の構成</span><span class="sxs-lookup"><span data-stu-id="b9b0e-116">Configure the unassigned number table in Lync Server 2013</span></span>](lync-server-2013-configure-the-unassigned-number-table.md)

  - [<span data-ttu-id="b9b0e-117">省略Lync Server 2013 でのアナウンスメントの展開を確認する</span><span class="sxs-lookup"><span data-stu-id="b9b0e-117">(Optional) Verify Announcement deployment in Lync Server 2013</span></span>](lync-server-2013-optional-verify-announcement-deployment.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="b9b0e-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="b9b0e-118">See Also</span></span>


[<span data-ttu-id="b9b0e-119">Lync Server 2013 の通話管理機能の計画</span><span class="sxs-lookup"><span data-stu-id="b9b0e-119">Planning for call management features in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-management-features.md)  
  

<span data-ttu-id="b9b0e-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b9b0e-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

