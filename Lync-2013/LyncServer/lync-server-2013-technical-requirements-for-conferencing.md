---
title: Lync Server 2013 の会議の技術要件
description: Lync Server 2013 会議のテクニカル要件。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical requirements for conferencing
ms:assetid: 3c0d89e1-53e6-46d7-bf8c-491260b292ea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425889(v=OCS.15)
ms:contentKeyID: 48183923
ms.date: 06/26/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0b3b787d84288d789cd0d824081439004f19327e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399225"
---
# <a name="technical-requirements-for-conferencing-in-lync-server-2013"></a><span data-ttu-id="6a6b1-103">Lync Server 2013 の会議の技術要件</span><span class="sxs-lookup"><span data-stu-id="6a6b1-103">Technical requirements for conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6a6b1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6a6b1-104">

<span> </span></span></span>

<span data-ttu-id="6a6b1-105">_**最終更新日:** 2014-06-25_</span><span class="sxs-lookup"><span data-stu-id="6a6b1-105">_**Topic Last Modified:** 2014-06-25_</span></span>

<span data-ttu-id="6a6b1-106">Lync Server 2013、ダイヤルイン会議、A/V 会議、インスタントメッセージング (IM) 会議、および web 会議機能は、常にフロントエンドサーバーで実行されます。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-106">For Lync Server 2013, dial-in conferencing, A/V conferencing, instant messaging (IM) conferencing and web conferencing capabilities always run on Front End Servers.</span></span>

<span data-ttu-id="6a6b1-107">このセクションでは、サポートされている collocation と共に、これらのサーバーのハードウェアとソフトウェアの要件について詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-107">This section details the hardware and software requirements for these servers, along with the supported collocation.</span></span>

<span data-ttu-id="6a6b1-108">ダイヤルイン会議は、さまざまなコンポーネントが含まれている機能です。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-108">Dial-in conferencing is a feature that includes a variety of components.</span></span> <span data-ttu-id="6a6b1-109">一部のコンポーネントは、ダイヤルイン会議に固有であり、一部はエンタープライズボイスコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-109">Some of the components are specific to dial-in conferencing and some are Enterprise Voice components.</span></span> <span data-ttu-id="6a6b1-110">このセクションでは、ダイヤルイン会議に固有のコンポーネントの要件について説明します。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-110">This section describes the requirements for the components that are specific to dial-in conferencing.</span></span> <span data-ttu-id="6a6b1-111">仲介サーバーと公衆交換電話網 (PSTN) ゲートウェイの要件の詳細については、「 [Lync server 2013 の仲介サーバーコンポーネント](lync-server-2013-mediation-server-component.md) 」および「計画ドキュメントの [lync Server 2013 の仲介サーバー用のコンポーネントとトポロジ](lync-server-2013-components-and-topologies-for-mediation-server.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-111">For details about Mediation Server and public switched telephone network (PSTN) gateway requirements, see [Mediation Server component in Lync Server 2013](lync-server-2013-mediation-server-component.md) and [Components and topologies for Mediation Server in Lync Server 2013](lync-server-2013-components-and-topologies-for-mediation-server.md) in the Planning documentation.</span></span>

<div>

## <a name="hardware-requirements"></a><span data-ttu-id="6a6b1-112">ハードウェア要件</span><span class="sxs-lookup"><span data-stu-id="6a6b1-112">Hardware Requirements</span></span>

<span data-ttu-id="6a6b1-113">Web 会議と A/V の会議はフロントエンドサーバーと連携しているため、サーバーハードウェア要件は、フロントエンドサーバーの場合と同じです。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-113">Because web conferencing and A/V conferencing are collocated with the Front End Server, the server hardware requirements are the same as for the Front End Servers.</span></span> <span data-ttu-id="6a6b1-114">ハードウェア要件の詳細については、サポートドキュメントの「 [サーバーハードウェアプラットフォーム (Lync server 2013 の場合](lync-server-2013-server-hardware-platforms.md) )」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-114">For details about hardware requirements, see [Server hardware platforms for Lync Server 2013](lync-server-2013-server-hardware-platforms.md) in the Supportability documentation.</span></span> <span data-ttu-id="6a6b1-115">ダイヤルイン会議に必要な次のコンポーネントについても、フロントエンドサーバーと同じハードウェア要件があります。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-115">The following components required for dial-in conferencing also have the same hardware requirements as Front End Servers:</span></span>

  - <span data-ttu-id="6a6b1-116">アプリケーション サービス</span><span class="sxs-lookup"><span data-stu-id="6a6b1-116">Application service</span></span>

  - <span data-ttu-id="6a6b1-117">会議アテンダント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="6a6b1-117">Conferencing Attendant application</span></span>

  - <span data-ttu-id="6a6b1-118">会議アナウンス アプリケーション</span><span class="sxs-lookup"><span data-stu-id="6a6b1-118">Conferencing Announcement application</span></span>

<span data-ttu-id="6a6b1-119">フロントエンドサーバーのハードウェア要件は、Lync Server 2013 のその他の多くのサーバーの役割と同じで、次の表で説明します。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-119">The hardware requirements for Front End Server are the same as for many other server roles in Lync Server 2013 are outlined in the following table.</span></span>

</div>

<div>

## <a name="software-requirements"></a><span data-ttu-id="6a6b1-120">ソフトウェア要件</span><span class="sxs-lookup"><span data-stu-id="6a6b1-120">Software Requirements</span></span>

<span data-ttu-id="6a6b1-121">Web 会議と A/V の会議はフロントエンドサーバーと連携しているため、サーバーソフトウェアの要件は、フロントエンドサーバーの場合と同じです。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-121">Because web conferencing and A/V conferencing are collocated with the Front End Server, the server software requirements are the same as for the Front End Servers.</span></span> <span data-ttu-id="6a6b1-122">ソフトウェア要件の詳細については、サポートドキュメントの「 [Lync server 2013 でのサーバーとツールのオペレーティングシステムのサポート](lync-server-2013-server-and-tools-operating-system-support.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-122">For details about software requirements, see [Server and tools operating system support in Lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md) in the Supportability documentation.</span></span>

<span data-ttu-id="6a6b1-123">Web 会議の場合は、Lync Server 2013 では、Office Web Apps と Office Web apps サーバー (旧 WAC Server) で PowerPoint プレゼンテーションを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-123">For web conferencing, Lync Server 2013 also requires Office Web Apps and the Office Web Apps Server (formerly known as WAC Server) to handle PowerPoint presentations.</span></span> <span data-ttu-id="6a6b1-124">詳細については、「 [Office Web Apps サーバーおよび Lync server 2013 との統合を構成する](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-124">For details, see [Configuring integration with Office Web Apps Server and Lync Server 2013](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md).</span></span>

<span data-ttu-id="6a6b1-125">ダイヤルイン会議、アプリケーションサービス、会議アテンダントアプリケーション、会議アナウンスメントアプリケーションには、フロントエンドサーバーと同じオペレーティングシステム要件があります。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-125">For dial-in conferencing, Application service, Conferencing Attendant application, and Conferencing Announcement application have the same operating system requirements as Front End Servers.</span></span> <span data-ttu-id="6a6b1-126">ソフトウェア要件の詳細については、サポートドキュメントの「 [Lync server 2013 でのサーバーとツールのオペレーティングシステムのサポート](lync-server-2013-server-and-tools-operating-system-support.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-126">For details about software requirements, see [Server and tools operating system support in Lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md) in the Supportability documentation.</span></span>

<span data-ttu-id="6a6b1-127">会議アテンダントアプリケーションと会議アナウンスメントアプリケーションでは、Windows Media Format Runtime がフロントエンドサーバーにインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-127">Conferencing Attendant application and Conferencing Announcement application require that Windows Media Format Runtime is installed on Front End Servers.</span></span> <span data-ttu-id="6a6b1-128">Windows Media 形式ランタイムは、音楽の保留、記録された名前、およびプロンプトに使用される Windows Media audio (WMA) ファイルを再生するために必要です。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-128">The Windows Media Format Runtime is required to play Windows Media audio (WMA) files that are used for music on hold, recorded names, and prompts.</span></span> <span data-ttu-id="6a6b1-129">Windows Server 2012 と Windows Server 2012 R2 を除き、windows Media 形式ランタイムは、セットアップの実行時に Windows デスクトップエクスペリエンスの一部として自動的にインストールされますが、コンピューターの再起動が必要になる場合もあります。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-129">Except for Windows Server 2012 and Windows Server 2012 R2, the Windows Media Format Runtime is installed automatically as part of the Windows Desktop Experience when you run Setup, but you might need to restart the computer.</span></span> <span data-ttu-id="6a6b1-130">そのため、windows デスクトップエクスペリエンスの一部としてインストールすることをお勧めします。これには、セットアップを実行する前に Windows Media 形式ランタイムが含まれています。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-130">Therefore, we recommend that you install as part of the Windows Desktop Experience, which includes Windows Media Format Runtime before you run Setup.</span></span> <span data-ttu-id="6a6b1-131">Windows Server 2012 および Windows Server 2012 R2 には Microsoft メディアファンデーションが必要です。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-131">Windows Server 2012 and Windows Server 2012 R2 requires Microsoft Media Foundation.</span></span>

</div>

<div>

## <a name="port-requirements-for-dial-in-conferencing"></a><span data-ttu-id="6a6b1-132">ダイヤルイン会議のポート要件</span><span class="sxs-lookup"><span data-stu-id="6a6b1-132">Port Requirements for dial-in conferencing</span></span>

<span data-ttu-id="6a6b1-133">次の表では、ダイヤルイン会議で使用されるポートについて説明します。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-133">The following table describes the ports that are used by dial-in conferencing.</span></span> <span data-ttu-id="6a6b1-134">ロードバランサーを使用している場合は、プールで実行されるすべてのアプリケーションで使用されているポート用にロードバランサーが構成されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-134">If you use a load balancer, ensure that the load balancer is configured for the ports used by any applications that will run in the pool.</span></span>

<span data-ttu-id="6a6b1-135">これらのポートは既定の設定であり、**Set-CsApplicationServer** コマンドレットを使用して変更することができます。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-135">These ports are default settings that you can change by using the **Set-CsApplicationServer** cmdlet.</span></span> <span data-ttu-id="6a6b1-136">このコマンドレットの詳細については、「Lync Server 管理シェルのドキュメント」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-136">For details about this cmdlet, see the Lync Server Management Shell documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="6a6b1-137">プール内の同じアプリケーションのすべてのインスタンスは、同じ SIP リスニングポートを使用します。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-137">All instances of the same application in a pool use the same SIP listening port.</span></span>



</div>

### <a name="ports-used-by-dial-in-conferencing"></a><span data-ttu-id="6a6b1-138">ダイヤルイン会議で使用されるポート</span><span class="sxs-lookup"><span data-stu-id="6a6b1-138">Ports used by dial-in conferencing</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6a6b1-139">ポート番号</span><span class="sxs-lookup"><span data-stu-id="6a6b1-139">Port number</span></span></th>
<th><span data-ttu-id="6a6b1-140">説明</span><span class="sxs-lookup"><span data-stu-id="6a6b1-140">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6a6b1-141">5072</span><span class="sxs-lookup"><span data-stu-id="6a6b1-141">5072</span></span></p></td>
<td><p><span data-ttu-id="6a6b1-142">SIP リスニング要求用の会議アテンダントアプリケーションで使用</span><span class="sxs-lookup"><span data-stu-id="6a6b1-142">Used by Conferencing Attendant application for SIP listening requests</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a6b1-143">5073</span><span class="sxs-lookup"><span data-stu-id="6a6b1-143">5073</span></span></p></td>
<td><p><span data-ttu-id="6a6b1-144">SIP リスニング要求の会議アナウンスメントアプリケーションで使用</span><span class="sxs-lookup"><span data-stu-id="6a6b1-144">Used by Conferencing Announcement application for SIP listening requests</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="supported-clients-for-dial-in-conferencing"></a><span data-ttu-id="6a6b1-145">ダイヤルイン会議でサポートされているクライアント</span><span class="sxs-lookup"><span data-stu-id="6a6b1-145">Supported Clients for Dial-In Conferencing</span></span>

<span data-ttu-id="6a6b1-146">次のクライアントを使用して、ダイヤルインアクセスをサポートするオンプレミスの会議をスケジュールすることができます。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-146">You can use the following client to schedule on-premises conferences that support dial-in access:</span></span>

  - <span data-ttu-id="6a6b1-147">Lync 2013 用のオンライン会議アドイン (Lync 2013 または出席者をインストールしたときに自動的にインストールされます)</span><span class="sxs-lookup"><span data-stu-id="6a6b1-147">Online Meeting Add-in for Lync 2013 (installed automatically when you install Lync 2013 or Attendee)</span></span>

</div>

<div>

## <a name="dial-in-conferencing-settings-page-requirements"></a><span data-ttu-id="6a6b1-148">ダイヤルイン会議の設定ページの要件</span><span class="sxs-lookup"><span data-stu-id="6a6b1-148">Dial-in Conferencing Settings page Requirements</span></span>

<span data-ttu-id="6a6b1-149">[ダイヤルイン会議の設定] ページでは、次の表に示すオペレーティングシステムと web ブラウザーの組み合わせがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-149">The Dial-in Conferencing Settings page supports the combinations of operating systems and web browsers described in the following table.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="6a6b1-150">32ビット版と64ビット版のオペレーティングシステムがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-150">32-bit and 64-bit versions of the operating systems are supported.</span></span>



</div>

### <a name="supported-operating-systems-and-web-browsers"></a><span data-ttu-id="6a6b1-151">サポートされているオペレーティング システムおよび Web ブラウザー</span><span class="sxs-lookup"><span data-stu-id="6a6b1-151">Supported Operating Systems and Web Browsers</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6a6b1-152">オペレーティング システム</span><span class="sxs-lookup"><span data-stu-id="6a6b1-152">Operating system</span></span></th>
<th><span data-ttu-id="6a6b1-153">Web ブラウザー</span><span class="sxs-lookup"><span data-stu-id="6a6b1-153">Web browser</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6a6b1-154">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6a6b1-154">Windows 7</span></span></p></td>
<td><p><span data-ttu-id="6a6b1-155">Internet Explorer 9</span><span class="sxs-lookup"><span data-stu-id="6a6b1-155">Internet Explorer 9</span></span></p>
<p><span data-ttu-id="6a6b1-156">Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="6a6b1-156">Internet Explorer 8</span></span></p>
<p><span data-ttu-id="6a6b1-157">Firefox</span><span class="sxs-lookup"><span data-stu-id="6a6b1-157">Firefox</span></span></p></td>
</tr>
<tr class="even">
<td> </td>
<td> </td>
</tr>
<tr class="odd">
<td> </td>
<td> </td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a6b1-158">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6a6b1-158">Windows Server 2008 R2</span></span></p></td>
<td><p><span data-ttu-id="6a6b1-159">Internet Explorer 9</span><span class="sxs-lookup"><span data-stu-id="6a6b1-159">Internet Explorer 9</span></span></p>
<p><span data-ttu-id="6a6b1-160">Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="6a6b1-160">Internet Explorer 8</span></span></p>
<p><span data-ttu-id="6a6b1-161">Internet Explorer 7</span><span class="sxs-lookup"><span data-stu-id="6a6b1-161">Internet Explorer 7</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a6b1-162">Mac OS</span><span class="sxs-lookup"><span data-stu-id="6a6b1-162">Mac OS</span></span></p></td>
<td><p><span data-ttu-id="6a6b1-163">Firefox</span><span class="sxs-lookup"><span data-stu-id="6a6b1-163">Firefox</span></span></p>
<p><span data-ttu-id="6a6b1-164">Safari</span><span class="sxs-lookup"><span data-stu-id="6a6b1-164">Safari</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="audio-file-requirements-for-dial-in-conferencing"></a><span data-ttu-id="6a6b1-165">ダイヤルイン会議のオーディオファイルの要件</span><span class="sxs-lookup"><span data-stu-id="6a6b1-165">Audio File Requirements for dial-in conferencing</span></span>

<span data-ttu-id="6a6b1-166">Lync Server 2013 は、ダイヤルイン会議の音声メッセージや音楽のカスタマイズをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-166">Lync Server 2013 does not support customization of voice prompts and music for dial-in conferencing.</span></span> <span data-ttu-id="6a6b1-167">ただし、既定のオーディオファイルを変更する必要がある強力な業務上のニーズがある場合は、microsoft サポート技術情報の記事961177、「 [Microsoft Office Communications Server 2007 R2 のダイヤルイン電話会議の音声メッセージまたは音楽ファイルをカスタマイズする方法](https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=961177)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-167">However, if you have a strong business need that requires you to change the default audio files, see Microsoft Knowledge Base article 961177, [How to customize voice prompts or music files for dial-in audio conferencing in Microsoft Office Communications Server 2007 R2](https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=961177).</span></span>

<span data-ttu-id="6a6b1-168">また、 [Microsoft Lync Server 会議アテンダントのカスタム音声指示](https://go.microsoft.com/fwlink/p/?linkid=396880) 管理ユーティリティを使用して、電話の発信者が、ユーザー設定のメッセージを使って Lync 会議に参加するときに使用される既定の音声プロンプトを置き換えて、別の会議エントリの操作を行うこともできます。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-168">You can also use the [Microsoft Lync Server Conferencing Attendant Custom Voice Prompts](https://go.microsoft.com/fwlink/p/?linkid=396880) management utility, which enables administrators to replace the default voice prompts used when a phone caller joins a Lync meeting with custom prompts to provide a different meeting entry experience.</span></span> <span data-ttu-id="6a6b1-169">カスタム音声プロンプトは、Lync Server 2010 または Lync Server 2013 (Enterprise または Standard Edition) を実行しているサーバーにインストールできます。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-169">The custom voice prompts can be installed on a server that is running Lync Server 2010 or Lync Server 2013, either Enterprise or Standard Edition.</span></span>

<span data-ttu-id="6a6b1-170">会議アテンダントアプリケーションと会議アナウンスメントアプリケーションには、音楽の保留、記録された名前、およびオーディオプロンプトファイルの次の要件があります。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-170">Conferencing Attendant application and Conferencing Announcement application have the following requirements for music on hold, recorded name, and audio prompt files:</span></span>

  - <span data-ttu-id="6a6b1-171">Windows Media Audio (WMA) ファイル形式</span><span class="sxs-lookup"><span data-stu-id="6a6b1-171">Windows Media Audio (WMA) file format</span></span>

  - <span data-ttu-id="6a6b1-172">16 ビット モノラル</span><span class="sxs-lookup"><span data-stu-id="6a6b1-172">16-bit mono</span></span>

  - <span data-ttu-id="6a6b1-173">48 Kbps 2-pass CBR (固定ビット レート)</span><span class="sxs-lookup"><span data-stu-id="6a6b1-173">48 kbps 2-pass CBR (constant bit rate)</span></span>

  - <span data-ttu-id="6a6b1-174">-24DB の音声レベル</span><span class="sxs-lookup"><span data-stu-id="6a6b1-174">Speech level at -24DB</span></span>

</div>

<div>

## <a name="user-requirements-for-dial-in-conferencing"></a><span data-ttu-id="6a6b1-175">ダイヤルイン会議のユーザー要件</span><span class="sxs-lookup"><span data-stu-id="6a6b1-175">User Requirements for Dial-In Conferencing</span></span>

<span data-ttu-id="6a6b1-176">ダイヤルイン会議ユーザーは、そのアカウントに固有の電話番号または内線番号を割り当てておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-176">Dial-in conferencing users must have a unique phone number or extension assigned to their account.</span></span> <span data-ttu-id="6a6b1-177">この要件によりダイヤルイン会議中の認証が可能になります。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-177">This requirement supports authentication during dial-in conferencing.</span></span> <span data-ttu-id="6a6b1-178">エンタープライズユーザー (つまり、組織内で Active Directory ドメインサービスの資格情報と Lync Server アカウントを持っているユーザー) は、電話番号 (または内線番号) と個人識別番号 (PIN) を入力して、認証されたユーザーとして会議にダイヤルインします。</span><span class="sxs-lookup"><span data-stu-id="6a6b1-178">Enterprise users (that is, users who have Active Directory Domain Services credentials and Lync Server accounts within your organization) enter their phone number (or extension) and a personal identification number (PIN) to dial in to conferences as an authenticated user.</span></span>

<span data-ttu-id="6a6b1-179"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6a6b1-179"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

