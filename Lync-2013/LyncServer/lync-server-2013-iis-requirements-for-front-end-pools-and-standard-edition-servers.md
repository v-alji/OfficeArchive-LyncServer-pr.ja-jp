---
title: フロントエンド プールおよび Standard Edition サーバーの IIS 要件
description: フロントエンドプールと Standard Edition サーバーの IIS 要件。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IIS requirements for Front End pools and Standard Edition servers
ms:assetid: e8a6c7ac-b6d5-4c7e-abe9-d8ea5eedbc62
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399038(v=OCS.15)
ms:contentKeyID: 48185888
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f56452c7e47352333ac3ac5a51d649b0828a0ff9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427426"
---
# <a name="iis-requirements-for-front-end-pools-and-standard-edition-servers-in-lync-server-2013"></a><span data-ttu-id="e8f0d-103">Lync Server 2013 のフロントエンド プールおよび Standard Edition サーバーの IIS 要件</span><span class="sxs-lookup"><span data-stu-id="e8f0d-103">IIS requirements for Front End pools and Standard Edition servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e8f0d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e8f0d-104">

<span> </span></span></span>

<span data-ttu-id="e8f0d-105">_**最終更新日:** 2012-06-19_</span><span class="sxs-lookup"><span data-stu-id="e8f0d-105">_**Topic Last Modified:** 2012-06-19_</span></span>

<span data-ttu-id="e8f0d-106">Standard Edition サーバー、フロントエンドサーバー、およびディレクターの場合、Lync Server 2013 installer では、次の目的でインターネットインフォメーションサービス (IIS) で仮想ディレクトリが作成されます。</span><span class="sxs-lookup"><span data-stu-id="e8f0d-106">For Standard Edition servers and Front End Servers, and Directors, the Lync Server 2013 installer creates virtual directories in Internet Information Services (IIS) for the following purposes:</span></span>

  - <span data-ttu-id="e8f0d-107">ユーザーがアドレス帳サービスからファイルをダウンロードできるようにするには</span><span class="sxs-lookup"><span data-stu-id="e8f0d-107">To enable users to download files from the Address Book Service</span></span>

  - <span data-ttu-id="e8f0d-108">クライアントが更新プログラムを取得できるようにするには</span><span class="sxs-lookup"><span data-stu-id="e8f0d-108">To enable clients to obtain updates</span></span>

  - <span data-ttu-id="e8f0d-109">会議を有効にするには</span><span class="sxs-lookup"><span data-stu-id="e8f0d-109">To enable conferencing</span></span>

  - <span data-ttu-id="e8f0d-110">ユーザーが会議コンテンツをダウンロードできるようにするには</span><span class="sxs-lookup"><span data-stu-id="e8f0d-110">To enable users to download meeting content</span></span>

  - <span data-ttu-id="e8f0d-111">ユーザーが配布グループを展開できるようにするには</span><span class="sxs-lookup"><span data-stu-id="e8f0d-111">To enable users to expand distribution groups</span></span>

  - <span data-ttu-id="e8f0d-112">電話会議を有効にするには</span><span class="sxs-lookup"><span data-stu-id="e8f0d-112">To enable phone conferencing</span></span>

  - <span data-ttu-id="e8f0d-113">応答グループの機能を有効にするには</span><span class="sxs-lookup"><span data-stu-id="e8f0d-113">To enable response group features</span></span>

<span data-ttu-id="e8f0d-114">さらに、Lync Server 2010: 2011 年11月の累積更新プログラムでは、次の目的で IIS で仮想ディレクトリが作成されます。</span><span class="sxs-lookup"><span data-stu-id="e8f0d-114">In addition, the cumulative update for Lync Server 2010: November 2011 installer creates virtual directories in IIS for the following purposes:</span></span>

  - <span data-ttu-id="e8f0d-115">モバイルデバイスでのインスタントメッセージング (IM) やプレゼンスなどの機動性機能をサポートするフロントエンドサーバーまたは Standard Edition サーバーの場合</span><span class="sxs-lookup"><span data-stu-id="e8f0d-115">On Front End Servers or Standard Edition servers to support mobility functionality, such as instant messaging (IM) and presence, on mobile devices</span></span>

  - <span data-ttu-id="e8f0d-116">フロントエンドサーバーまたは標準エディションのサーバーおよびディレクターで、モバイルデバイスでモビリティリソースを自動的に検出できるようにする</span><span class="sxs-lookup"><span data-stu-id="e8f0d-116">On Front End Servers or Standard Edition servers and on Directors to enable mobile devices to automatically discover mobility resources</span></span>



> [!NOTE]
> <span data-ttu-id="e8f0d-117">モバイル機能を導入する場合は、IIS 7.5 を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e8f0d-117">If you are deploying mobility, we recommend that you use IIS 7.5.</span></span> <span data-ttu-id="e8f0d-118">Lync Server Mobility Service installer は、パフォーマンスを向上させるためにいくつかの ASP.NET フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="e8f0d-118">The Lync Server Mobility Service installer sets some ASP.NET flags to improve performance.</span></span> <span data-ttu-id="e8f0d-119">既定では、Windows Server 2008 R2 に IIS 7.5 がインストールされ、モビリティサービスのインストーラーによって ASP.NET の設定が自動的に変更されます。</span><span class="sxs-lookup"><span data-stu-id="e8f0d-119">IIS 7.5 is installed by default on Windows Server 2008 R2, and the Mobility Service installer automatically changes the ASP.NET settings.</span></span> <span data-ttu-id="e8f0d-120">Windows Server 2008 で IIS 7.0 を使っている場合は、これらの設定を手動で変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8f0d-120">If you use IIS 7.0 on Windows Server 2008, you need to manually change these settings.</span></span>



<span data-ttu-id="e8f0d-121">Lync Server では、次の IIS モジュールをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8f0d-121">Lync Server requires the following IIS modules to be installed:</span></span>


> [!IMPORTANT]
> <span data-ttu-id="e8f0d-122">組織で IIS およびすべての Web サービスをシステムドライブ以外のドライブに配置する必要がある場合、[セットアップ] ダイアログボックスで Lync Server ファイルのインストール場所のパスを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="e8f0d-122">If your organization requires that you locate IIS and all Web Services on a drive other than the system drive, you can change the installation location path for the Lync Server files in the Setup dialog box.</span></span> <span data-ttu-id="e8f0d-123">このパス (OCSCore.msi を含む) にセットアップファイルをインストールすると、その他の Lync Server ファイルもこのドライブに展開されます。</span><span class="sxs-lookup"><span data-stu-id="e8f0d-123">If you install the Setup files to this path, including OCSCore.msi, the rest of the Lync Server files will be deployed to this drive as well.</span></span> <span data-ttu-id="e8f0d-124">IIS をインストールするときに、Windows Server Manager によって展開された INETPUB を再配置する方法の詳細については、を参照してください <A href="https://go.microsoft.com/fwlink/p/?linkid=216888">https://go.microsoft.com/fwlink/p/?linkId=216888</A> 。</span><span class="sxs-lookup"><span data-stu-id="e8f0d-124">For details about how to relocate the INETPUB deployed by Windows Server Manager when installing IIS, see <A href="https://go.microsoft.com/fwlink/p/?linkid=216888">https://go.microsoft.com/fwlink/p/?linkId=216888</A>.</span></span>


  - <span data-ttu-id="e8f0d-125">静的コンテンツ</span><span class="sxs-lookup"><span data-stu-id="e8f0d-125">Static Content</span></span>

  - <span data-ttu-id="e8f0d-126">既定のドキュメント</span><span class="sxs-lookup"><span data-stu-id="e8f0d-126">Default Document</span></span>

  - <span data-ttu-id="e8f0d-127">HTTP エラー</span><span class="sxs-lookup"><span data-stu-id="e8f0d-127">HTTP Errors</span></span>

  - <span data-ttu-id="e8f0d-128">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="e8f0d-128">ASP.NET</span></span>

  - <span data-ttu-id="e8f0d-129">.NET の拡張性</span><span class="sxs-lookup"><span data-stu-id="e8f0d-129">.NET Extensibility</span></span>

  - <span data-ttu-id="e8f0d-130">Internet Server API (ISAPI) の拡張機能</span><span class="sxs-lookup"><span data-stu-id="e8f0d-130">Internet Server API (ISAPI) Extensions</span></span>

  - <span data-ttu-id="e8f0d-131">ISAPI フィルター</span><span class="sxs-lookup"><span data-stu-id="e8f0d-131">ISAPI Filters</span></span>

  - <span data-ttu-id="e8f0d-132">HTTP ログ</span><span class="sxs-lookup"><span data-stu-id="e8f0d-132">HTTP Logging</span></span>

  - <span data-ttu-id="e8f0d-133">ログ ツール</span><span class="sxs-lookup"><span data-stu-id="e8f0d-133">Logging Tools</span></span>

  - <span data-ttu-id="e8f0d-134">トレース</span><span class="sxs-lookup"><span data-stu-id="e8f0d-134">Tracing</span></span>

  - <span data-ttu-id="e8f0d-135">Windows 認証</span><span class="sxs-lookup"><span data-stu-id="e8f0d-135">Windows Authentication</span></span>

  - <span data-ttu-id="e8f0d-136">要求のフィルタリング</span><span class="sxs-lookup"><span data-stu-id="e8f0d-136">Request Filtering</span></span>

  - <span data-ttu-id="e8f0d-137">静的コンテンツ圧縮</span><span class="sxs-lookup"><span data-stu-id="e8f0d-137">Static Content Compression</span></span>

  - <span data-ttu-id="e8f0d-138">動的コンテンツ圧縮</span><span class="sxs-lookup"><span data-stu-id="e8f0d-138">Dynamic Content Compression</span></span>

  - <span data-ttu-id="e8f0d-139">IIS 管理コンソール</span><span class="sxs-lookup"><span data-stu-id="e8f0d-139">IIS Management Console</span></span>

  - <span data-ttu-id="e8f0d-140">IIS 管理スクリプトおよびツール</span><span class="sxs-lookup"><span data-stu-id="e8f0d-140">IIS Management Scripts and Tools</span></span>

  - <span data-ttu-id="e8f0d-141">匿名認証 (IIS がインストールされている場合に既定でインストールされます)</span><span class="sxs-lookup"><span data-stu-id="e8f0d-141">Anonymous Authentication (installed by default when IIS is installed)</span></span>

  - <span data-ttu-id="e8f0d-142">クライアント証明書マッピング認証</span><span class="sxs-lookup"><span data-stu-id="e8f0d-142">Client Certificate Mapping Authentication</span></span>

<span data-ttu-id="e8f0d-143">次の表は、内部アクセス用の仮想ディレクトリと、それらが参照するファイルシステムリソースの Uri を示しています。</span><span class="sxs-lookup"><span data-stu-id="e8f0d-143">The following table lists the URIs for the virtual directories for internal access and the file system resources to which they refer.</span></span>

### <a name="virtual-directories-for-internal-access"></a><span data-ttu-id="e8f0d-144">内部アクセス用の仮想ディレクトリ</span><span class="sxs-lookup"><span data-stu-id="e8f0d-144">Virtual Directories for Internal Access</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e8f0d-145">機能</span><span class="sxs-lookup"><span data-stu-id="e8f0d-145">Feature</span></span></th>
<th><span data-ttu-id="e8f0d-146">仮想ディレクトリの URI</span><span class="sxs-lookup"><span data-stu-id="e8f0d-146">Virtual directory URI</span></span></th>
<th><span data-ttu-id="e8f0d-147">参照先</span><span class="sxs-lookup"><span data-stu-id="e8f0d-147">Refers to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8f0d-148">アドレス帳サーバー</span><span class="sxs-lookup"><span data-stu-id="e8f0d-148">Address Book Server</span></span></p></td>
<td><p><span data-ttu-id="e8f0d-149"> https://の &lt; 内部 FQDN &gt; /ABS/int/Handler</span><span class="sxs-lookup"><span data-stu-id="e8f0d-149">https://&lt;Internal FQDN&gt;/ABS/int/Handler</span></span></p></td>
<td><p><span data-ttu-id="e8f0d-150">内部ユーザーのアドレス帳サーバーのダウンロードファイルの場所。</span><span class="sxs-lookup"><span data-stu-id="e8f0d-150">Location of Address Book Server download files for internal users.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8f0d-151">自動検出サービス</span><span class="sxs-lookup"><span data-stu-id="e8f0d-151">Autodiscover Service</span></span></p></td>
<td><p><span data-ttu-id="e8f0d-152"> https:// &lt; 内部 FQDN &gt; /自動検出</span><span class="sxs-lookup"><span data-stu-id="e8f0d-152">https://&lt;Internal FQDN&gt;/Autodiscover</span></span></p></td>
<td><p><span data-ttu-id="e8f0d-153">内部のモバイルデバイスユーザーのモビリティリソースを検索する、Lync Server 自動検出サービスの場所。</span><span class="sxs-lookup"><span data-stu-id="e8f0d-153">Location of the Lync Server Autodiscover Service that locates mobility resources for internal mobile device users.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8f0d-154">クライアントの更新</span><span class="sxs-lookup"><span data-stu-id="e8f0d-154">Client updates</span></span></p></td>
<td><p><span data-ttu-id="e8f0d-155"> http://の &lt; 内部 FQDN &gt; /AutoUpdate/Int</span><span class="sxs-lookup"><span data-stu-id="e8f0d-155">http://&lt;Internal FQDN&gt;/AutoUpdate/Int</span></span></p></td>
<td><p><span data-ttu-id="e8f0d-156">内部コンピューターベースのクライアントの更新ファイルの場所。</span><span class="sxs-lookup"><span data-stu-id="e8f0d-156">Location of update files for internal computer-based clients.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8f0d-157">会議</span><span class="sxs-lookup"><span data-stu-id="e8f0d-157">Conf</span></span></p></td>
<td><p><span data-ttu-id="e8f0d-158"> http:// &lt; 内部 FQDN &gt; /Conf/Int</span><span class="sxs-lookup"><span data-stu-id="e8f0d-158">http://&lt;Internal FQDN&gt;/Conf/Int</span></span></p></td>
<td><p><span data-ttu-id="e8f0d-159">内部ユーザーの会議リソースの場所。</span><span class="sxs-lookup"><span data-stu-id="e8f0d-159">Location of conferencing resources for internal users.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8f0d-160">デバイスの更新</span><span class="sxs-lookup"><span data-stu-id="e8f0d-160">Device updates</span></span></p></td>
<td><p><span data-ttu-id="e8f0d-161"> http://の &lt; 内部 FQDN &gt; /DeviceUpdateFiles_Int</span><span class="sxs-lookup"><span data-stu-id="e8f0d-161">http://&lt;Internal FQDN&gt;/DeviceUpdateFiles_Int</span></span></p></td>
<td><p><span data-ttu-id="e8f0d-162">内部 UC デバイスの統合通信 (UC) デバイス更新ファイルの場所。</span><span class="sxs-lookup"><span data-stu-id="e8f0d-162">Location of unified communications (UC) device update files for internal UC devices.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8f0d-163">会議</span><span class="sxs-lookup"><span data-stu-id="e8f0d-163">Meeting</span></span></p></td>
<td><p><span data-ttu-id="e8f0d-164"> http://の &lt; 内部 FQDN &gt; /etc/place/null</span><span class="sxs-lookup"><span data-stu-id="e8f0d-164">http://&lt;Internal FQDN&gt;/etc/place/null</span></span></p></td>
<td><p><span data-ttu-id="e8f0d-165">内部ユーザー向けの会議コンテンツの場所。</span><span class="sxs-lookup"><span data-stu-id="e8f0d-165">Location of meeting content for internal users.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8f0d-166">モバイルサービス</span><span class="sxs-lookup"><span data-stu-id="e8f0d-166">Mobility Service</span></span></p></td>
<td><p><span data-ttu-id="e8f0d-167"> https:// &lt; 内部 FQDN &gt; /mcx</span><span class="sxs-lookup"><span data-stu-id="e8f0d-167">https://&lt;Internal FQDN&gt;/Mcx</span></span></p></td>
<td><p><span data-ttu-id="e8f0d-168">内部モバイルデバイスユーザー向けのモビリティサービスリソースの場所。</span><span class="sxs-lookup"><span data-stu-id="e8f0d-168">Location of Mobility Service resources for internal mobile device users.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8f0d-169">グループの展開とアドレス帳 Web クエリサービス</span><span class="sxs-lookup"><span data-stu-id="e8f0d-169">Group Expansion and Address Book Web Query service</span></span></p></td>
<td><p><span data-ttu-id="e8f0d-170"> http://の &lt; 内部 FQDN または &gt; グループの無効化</span><span class="sxs-lookup"><span data-stu-id="e8f0d-170">http://&lt;Internal FQDN&gt;/GroupExpansion/int/service.asmx</span></span></p></td>
<td><p><span data-ttu-id="e8f0d-171">内部ユーザーに対してグループの拡張を可能にする Web サービスの場所。</span><span class="sxs-lookup"><span data-stu-id="e8f0d-171">Location of the Web service that enables group expansion for internal users.</span></span> <span data-ttu-id="e8f0d-172">また、内部の Lync Mobile Microsoft Lync 2010 モバイルクライアントにグローバルアドレス一覧の情報を提供するアドレス帳 Web クエリサービスの場所。</span><span class="sxs-lookup"><span data-stu-id="e8f0d-172">Also, the location of the Address Book Web Query service that provides global address list information to internal Lync Mobile Microsoft Lync 2010 Mobile clients.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8f0d-173">電話会議</span><span class="sxs-lookup"><span data-stu-id="e8f0d-173">Phone Conferencing</span></span></p></td>
<td><p><span data-ttu-id="e8f0d-174"> http://の &lt; 内部 FQDN &gt; /PhoneConferencing/Int</span><span class="sxs-lookup"><span data-stu-id="e8f0d-174">http://&lt;Internal FQDN&gt;/PhoneConferencing/Int</span></span></p></td>
<td><p><span data-ttu-id="e8f0d-175">内部ユーザー向けの電話会議データの場所。</span><span class="sxs-lookup"><span data-stu-id="e8f0d-175">Location of phone conferencing data for internal users.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8f0d-176">デバイスの更新</span><span class="sxs-lookup"><span data-stu-id="e8f0d-176">Device updates</span></span></p></td>
<td><p><span data-ttu-id="e8f0d-177"> http://の &lt; 内部 FQDN &gt; /RequestHandler</span><span class="sxs-lookup"><span data-stu-id="e8f0d-177">http://&lt;Internal FQDN&gt;/RequestHandler</span></span></p></td>
<td><p><span data-ttu-id="e8f0d-178">内部の UC デバイスでログをアップロードし、更新プログラムを確認できるようにする、デバイス更新 Web サービス要求ハンドラーの場所。</span><span class="sxs-lookup"><span data-stu-id="e8f0d-178">Location of the Device Update Web service Request Handler that enables internal UC devices to upload logs and check for updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8f0d-179">応答グループ アプリケーション</span><span class="sxs-lookup"><span data-stu-id="e8f0d-179">Response Group application</span></span></p></td>
<td><p><span data-ttu-id="e8f0d-180"> http://の &lt; 内部 FQDN &gt; /RgsConfig</span><span class="sxs-lookup"><span data-stu-id="e8f0d-180">http://&lt;Internal FQDN&gt;/RgsConfig</span></span></p>
<p><span data-ttu-id="e8f0d-181"> http://の &lt; 内部 FQDN &gt; /RgsClients</span><span class="sxs-lookup"><span data-stu-id="e8f0d-181">http://&lt;Internal FQDN&gt;/RgsClients</span></span></p></td>
<td><p><span data-ttu-id="e8f0d-182">応答グループ構成ツールの場所。</span><span class="sxs-lookup"><span data-stu-id="e8f0d-182">Location of Response Group Configuration Tool.</span></span></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> <span data-ttu-id="e8f0d-183">統合された構成のフロントエンドプールの場合は、プールにサーバーを追加する前に、IIS を展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8f0d-183">For Front End pools in a consolidated configuration, you must deploy IIS before you can add servers to the pool.</span></span>


<table>
<thead>
<tr class="header">
<th><img src="images/Gg398321.security(OCS.15).gif" title="証券" alt="security" /><span data-ttu-id="e8f0d-185">セキュリティメモ:</span><span class="sxs-lookup"><span data-stu-id="e8f0d-185">Security Note:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e8f0d-186">Iis 管理スナップインを使用して、IIS web コンポーネントサーバーで使用する証明書を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8f0d-186">You must use the IIS administrative snap-in to assign the certificate used by the IIS web component server.</span></span></td>
</tr>
</tbody>
</table><span data-ttu-id="e8f0d-187">



</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e8f0d-187">



</div>

<span> </span>

</div>

</div>

</span></span></div>

