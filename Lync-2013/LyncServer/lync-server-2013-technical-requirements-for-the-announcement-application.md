---
title: 'Lync Server 2013: アナウンス アプリケーションの技術要件'
description: 'Lync Server 2013: お知らせアプリケーションの技術要件。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical requirements for the Announcement application
ms:assetid: fbd8c204-3765-4b22-a0c9-a781b5126366
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205413(v=OCS.15)
ms:contentKeyID: 48185944
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: adc5019408b79301bbcda3993ceb7d96ee4d9b7d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444309"
---
# <a name="technical-requirements-for-the-announcement-application-in-lync-server-2013"></a><span data-ttu-id="bc096-103">Lync Server 2013 のアナウンス アプリケーションの技術要件</span><span class="sxs-lookup"><span data-stu-id="bc096-103">Technical requirements for the Announcement application in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bc096-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bc096-104">

<span> </span></span></span>

<span data-ttu-id="bc096-105">_**最終更新日:** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="bc096-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="bc096-106">このセクションでは、アナウンスメントアプリケーションの次の技術上の要件について説明します。</span><span class="sxs-lookup"><span data-stu-id="bc096-106">This section describes the following technical requirements for the Announcement application:</span></span>

  - <span data-ttu-id="bc096-107">ハードウェアの要件</span><span class="sxs-lookup"><span data-stu-id="bc096-107">Hardware requirements</span></span>

  - <span data-ttu-id="bc096-108">ソフトウェア要件</span><span class="sxs-lookup"><span data-stu-id="bc096-108">Software requirements</span></span>

  - <span data-ttu-id="bc096-109">ポートの要件</span><span class="sxs-lookup"><span data-stu-id="bc096-109">Port requirements</span></span>

  - <span data-ttu-id="bc096-110">オーディオファイルの要件</span><span class="sxs-lookup"><span data-stu-id="bc096-110">Audio file requirements</span></span>

<div>

## <a name="hardware-requirements"></a><span data-ttu-id="bc096-111">ハードウェア要件</span><span class="sxs-lookup"><span data-stu-id="bc096-111">Hardware Requirements</span></span>

<span data-ttu-id="bc096-112">アナウンスメントアプリケーションには、フロントエンドサーバーと同じハードウェア要件があります。</span><span class="sxs-lookup"><span data-stu-id="bc096-112">The Announcement application has the same hardware requirements as Front End Servers.</span></span> <span data-ttu-id="bc096-113">ハードウェア要件の詳細については、サポートドキュメントの「 [サーバーハードウェアプラットフォーム (Lync server 2013 の場合](lync-server-2013-server-hardware-platforms.md) )」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bc096-113">For details about hardware requirements, see [Server hardware platforms for Lync Server 2013](lync-server-2013-server-hardware-platforms.md) in the Supportability documentation.</span></span>

</div>

<div>

## <a name="software-requirements"></a><span data-ttu-id="bc096-114">ソフトウェア要件</span><span class="sxs-lookup"><span data-stu-id="bc096-114">Software Requirements</span></span>

<span data-ttu-id="bc096-115">アナウンスメントアプリケーションには、フロントエンドサーバーと同じオペレーティングシステム要件とソフトウェアの前提条件があります。</span><span class="sxs-lookup"><span data-stu-id="bc096-115">The Announcement application has the same operating system requirements and software prerequisites as Front End Servers.</span></span> <span data-ttu-id="bc096-116">ソフトウェア要件の詳細については、サポートドキュメントの「 [Lync server 2013 でのサーバーとツールのオペレーティングシステムのサポート](lync-server-2013-server-and-tools-operating-system-support.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bc096-116">For details about software requirements, see [Server and tools operating system support in Lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md) in the Supportability documentation.</span></span>

<span data-ttu-id="bc096-117">アナウンスメントアプリケーションを実行するすべてのフロントエンドサーバーまたは標準エディションのサーバーには、windows server 2008 R2 を実行しているサーバー、または windows server 2012 R2 を実行して2012いるサーバー用の Microsoft メディアファンデーションがインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="bc096-117">All Front End Servers or Standard Edition servers that run the Announcement application must have the Windows Media Format Runtime installed for servers running Windows Server 2008 R2, or Microsoft Media Foundation for servers running Windows Server 2012 or Windows Server 2012 R2.</span></span> <span data-ttu-id="bc096-118">Windows Server 2008 R2 の場合、windows Media 形式ランタイムは Windows デスクトップエクスペリエンスの一部としてインストールされます。</span><span class="sxs-lookup"><span data-stu-id="bc096-118">For Windows Server 2008 R2, the Windows Media Format Runtime is installed as part of Windows Desktop Experience.</span></span> <span data-ttu-id="bc096-119">Windows media Format Runtime または Microsoft メディアファンデーションは、アナウンスメントアプリケーションがお知らせや音楽を再生するために Windows Media オーディオ (.wma) ファイルを使用する場合に必要です。</span><span class="sxs-lookup"><span data-stu-id="bc096-119">Windows Media Format Runtime or Microsoft Media Foundation is required for Windows Media Audio (.wma) files that the Announcement application plays for announcements and music.</span></span>

</div>

<div>

## <a name="port-requirements"></a><span data-ttu-id="bc096-120">ポートの要件</span><span class="sxs-lookup"><span data-stu-id="bc096-120">Port Requirements</span></span>

<span data-ttu-id="bc096-121">アナウンスメントアプリケーションでは、次のポートが使用されます。</span><span class="sxs-lookup"><span data-stu-id="bc096-121">The Announcement application uses the following port:</span></span>

  - <span data-ttu-id="bc096-122">**ポート 5071**   SIP リッスン要求のために使用</span><span class="sxs-lookup"><span data-stu-id="bc096-122">**Port 5071**   Used for SIP listening requests</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="bc096-123">このポートは既定の設定であり、<STRONG>Set-CsApplicationServer</STRONG> コマンドレットを使用して変更することができます。</span><span class="sxs-lookup"><span data-stu-id="bc096-123">This port is the default setting, which you can change by using the <STRONG>Set-CsApplicationServer</STRONG> cmdlet.</span></span> <span data-ttu-id="bc096-124">このコマンドレットの詳細については、「Lync Server 管理シェルのドキュメント」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bc096-124">For details about this cmdlet, see the Lync Server Management Shell documentation.</span></span>



</div>

</div>

<div>

## <a name="audio-file-requirements"></a><span data-ttu-id="bc096-125">オーディオ ファイルの要件</span><span class="sxs-lookup"><span data-stu-id="bc096-125">Audio File Requirements</span></span>

<span data-ttu-id="bc096-126">アナウンスメントアプリケーションは、音楽とお知らせのウェーブ (.wav) ファイル形式と Windows Media オーディオ (.wma) ファイル形式をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="bc096-126">The Announcement application supports Wave (.wav) file format and Windows Media audio (.wma) file format for music and announcements.</span></span> <span data-ttu-id="bc096-127">アナウンスメントアプリケーションのオーディオファイルの要件は、応答グループアプリケーションの場合と同じです。</span><span class="sxs-lookup"><span data-stu-id="bc096-127">Audio file requirements for the Announcement application are the same as for the Response Group application.</span></span> <span data-ttu-id="bc096-128">詳細については、「 [Lync Server 2013 の応答グループの技術要件](lync-server-2013-technical-requirements-for-response-group.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bc096-128">For details, see [Technical requirements for Response Group in Lync Server 2013](lync-server-2013-technical-requirements-for-response-group.md).</span></span>

<span data-ttu-id="bc096-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bc096-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

