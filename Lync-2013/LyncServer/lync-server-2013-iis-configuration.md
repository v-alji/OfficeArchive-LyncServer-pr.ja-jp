---
title: 'Lync Server 2013: IIS 構成'
description: 'Lync Server 2013: IIS の構成。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IIS configuration
ms:assetid: b458babf-bf64-43f0-8a8e-612f5096b63c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412871(v=OCS.15)
ms:contentKeyID: 48185169
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 901aca7bf5ff8824b54e93754569a6ef5defc10e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427433"
---
# <a name="iis-configuration-in-lync-server-2013"></a><span data-ttu-id="b3653-103">Lync Server 2013 の IIS 構成</span><span class="sxs-lookup"><span data-stu-id="b3653-103">IIS configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b3653-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b3653-104">

<span> </span></span></span>

<span data-ttu-id="b3653-105">_**最終更新日:** 2014-02-17_</span><span class="sxs-lookup"><span data-stu-id="b3653-105">_**Topic Last Modified:** 2014-02-17_</span></span>

<span data-ttu-id="b3653-106">この手順を完了するには、ローカル管理者とドメインユーザーとして、サーバーに少なくともログオンしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3653-106">To successfully complete this procedure, you should be logged on to the server minimally as a local administrator and a domain user.</span></span>

<span data-ttu-id="b3653-107">Lync Server 2013、Standard Edition、または第1のフロントエンドサーバー用のフロントエンドサーバーをプールに構成してインストールする前に、サーバーの役割とインターネットインフォメーションサービス (IIS) 用の Web サービスをインストールして構成します。</span><span class="sxs-lookup"><span data-stu-id="b3653-107">Before you configure and install the Front End Server for Lync Server 2013, Standard Edition or the first Front End Server in a pool, you install and configure the server role and Web Services for Internet Information Services (IIS).</span></span>

<div class=" ">


> [!IMPORTANT]  
> <span data-ttu-id="b3653-108">組織で IIS およびすべての Web サービスをシステムドライブ以外のドライブに配置する必要がある場合は、Lync Server 2013 管理ツールを初めてインストールするときに、[セットアップ] ダイアログボックスで Lync Server 2013 ファイルのインストール場所のパスを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="b3653-108">If your organization requires that you locate IIS and all Web Services on a drive other than the system drive, you can change the installation location path for the Lync Server 2013 files in the Setup dialog box when you initially install the Lync Server 2013 Administrative tools.</span></span> <span data-ttu-id="b3653-109">IIS をインストールする前に、管理ツールをインストールします。</span><span class="sxs-lookup"><span data-stu-id="b3653-109">You install the Administrative tools before installing IIS.</span></span> <span data-ttu-id="b3653-110">OCSCore.msi を含むこのパスにセットアップファイルをインストールした場合は、Lync Server の他の2013ファイルもこのドライブに展開されます。</span><span class="sxs-lookup"><span data-stu-id="b3653-110">If you install the Setup files to this path, including OCSCore.msi, the rest of the Lync Server 2013 files will be deployed to this drive as well.</span></span> <span data-ttu-id="b3653-111">Dtails については、「 <A href="lync-server-2013-install-lync-server-administrative-tools.md">Lync Server 2013 管理ツールをインストール</A>する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3653-111">For dtails, see <A href="lync-server-2013-install-lync-server-administrative-tools.md">Install Lync Server 2013 administrative tools</A>.</span></span> <span data-ttu-id="b3653-112">IIS をインストールするときに、Windows Server Manager によって展開された INETPUB を再配置する方法の詳細については、を参照してください <A href="https://go.microsoft.com/fwlink/p/?linkid=216888">https://go.microsoft.com/fwlink/p/?linkId=216888</A> 。</span><span class="sxs-lookup"><span data-stu-id="b3653-112">For details about how to relocate the INETPUB deployed by Windows Server Manager when installing IIS, see <A href="https://go.microsoft.com/fwlink/p/?linkid=216888">https://go.microsoft.com/fwlink/p/?linkId=216888</A>.</span></span>



</div>

<span data-ttu-id="b3653-113">次の表は、必要な IIS 7.5 の役割サービスを示しています。</span><span class="sxs-lookup"><span data-stu-id="b3653-113">The following table indicates the required IIS 7.5 role services.</span></span>

### <a name="iis-75-role-services"></a><span data-ttu-id="b3653-114">IIS 7.5 の役割サービス</span><span class="sxs-lookup"><span data-stu-id="b3653-114">IIS 7.5 Role Services</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b3653-115">ロール見出し</span><span class="sxs-lookup"><span data-stu-id="b3653-115">Role Heading</span></span></th>
<th><span data-ttu-id="b3653-116">役割サービス</span><span class="sxs-lookup"><span data-stu-id="b3653-116">Role Service</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b3653-117">インストールされている一般的な HTTP 機能</span><span class="sxs-lookup"><span data-stu-id="b3653-117">Common HTTP features installed</span></span></p></td>
<td><p><span data-ttu-id="b3653-118">静的なコンテンツ</span><span class="sxs-lookup"><span data-stu-id="b3653-118">Static content</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3653-119">インストールされている一般的な HTTP 機能</span><span class="sxs-lookup"><span data-stu-id="b3653-119">Common HTTP features installed</span></span></p></td>
<td><p><span data-ttu-id="b3653-120">既定のドキュメント</span><span class="sxs-lookup"><span data-stu-id="b3653-120">Default document</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3653-121">インストールされている一般的な HTTP 機能</span><span class="sxs-lookup"><span data-stu-id="b3653-121">Common HTTP features installed</span></span></p></td>
<td><p><span data-ttu-id="b3653-122">HTTP エラー</span><span class="sxs-lookup"><span data-stu-id="b3653-122">HTTP errors</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3653-123">アプリケーション開発</span><span class="sxs-lookup"><span data-stu-id="b3653-123">Application development</span></span></p></td>
<td><p><span data-ttu-id="b3653-124">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="b3653-124">ASP.NET</span></span></p>
<p><span data-ttu-id="b3653-125">Windows Server 2012 にも、.ASP 4.5 が必要です。</span><span class="sxs-lookup"><span data-stu-id="b3653-125">Windows Server 2012 also requires ASP.NET4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3653-126">アプリケーション開発</span><span class="sxs-lookup"><span data-stu-id="b3653-126">Application development</span></span></p></td>
<td><p><span data-ttu-id="b3653-127">.NET の拡張性</span><span class="sxs-lookup"><span data-stu-id="b3653-127">.NET extensibility</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3653-128">アプリケーション開発</span><span class="sxs-lookup"><span data-stu-id="b3653-128">Application development</span></span></p></td>
<td><p><span data-ttu-id="b3653-129">Internet Server API (ISAPI) の拡張機能</span><span class="sxs-lookup"><span data-stu-id="b3653-129">Internet Server API (ISAPI) extensions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3653-130">アプリケーション開発</span><span class="sxs-lookup"><span data-stu-id="b3653-130">Application development</span></span></p></td>
<td><p><span data-ttu-id="b3653-131">ISAPI フィルター</span><span class="sxs-lookup"><span data-stu-id="b3653-131">ISAPI filters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3653-132">正常性と診断</span><span class="sxs-lookup"><span data-stu-id="b3653-132">Health and diagnostics</span></span></p></td>
<td><p><span data-ttu-id="b3653-133">HTTP ログ</span><span class="sxs-lookup"><span data-stu-id="b3653-133">HTTP logging</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3653-134">正常性と診断</span><span class="sxs-lookup"><span data-stu-id="b3653-134">Health and diagnostics</span></span></p></td>
<td><p><span data-ttu-id="b3653-135">ログツール</span><span class="sxs-lookup"><span data-stu-id="b3653-135">Logging tools</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3653-136">正常性と診断</span><span class="sxs-lookup"><span data-stu-id="b3653-136">Health and diagnostics</span></span></p></td>
<td><p><span data-ttu-id="b3653-137">トレース</span><span class="sxs-lookup"><span data-stu-id="b3653-137">Tracing</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3653-138">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="b3653-138">Security</span></span></p></td>
<td><p><span data-ttu-id="b3653-139">匿名認証 (既定でインストールされ、有効になっている)</span><span class="sxs-lookup"><span data-stu-id="b3653-139">Anonymous authentication (installed and enabled by default)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3653-140">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="b3653-140">Security</span></span></p></td>
<td><p><span data-ttu-id="b3653-141">Windows 認証</span><span class="sxs-lookup"><span data-stu-id="b3653-141">Windows authentication</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3653-142">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="b3653-142">Security</span></span></p></td>
<td><p><span data-ttu-id="b3653-143">クライアント証明書のマッピング認証</span><span class="sxs-lookup"><span data-stu-id="b3653-143">Client Certificate Mapping authentication</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3653-144">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="b3653-144">Security</span></span></p></td>
<td><p><span data-ttu-id="b3653-145">フィルターを要求する</span><span class="sxs-lookup"><span data-stu-id="b3653-145">Request filtering</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3653-146">パフォーマンス</span><span class="sxs-lookup"><span data-stu-id="b3653-146">Performance</span></span></p></td>
<td><p><span data-ttu-id="b3653-147">静的なコンテンツの圧縮</span><span class="sxs-lookup"><span data-stu-id="b3653-147">Static content compression</span></span></p>
<p><span data-ttu-id="b3653-148">動的なコンテンツの圧縮</span><span class="sxs-lookup"><span data-stu-id="b3653-148">Dynamic content compression</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3653-149">管理ツール</span><span class="sxs-lookup"><span data-stu-id="b3653-149">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="b3653-150">IIS 管理コンソール</span><span class="sxs-lookup"><span data-stu-id="b3653-150">IIS Management Console</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3653-151">管理ツール</span><span class="sxs-lookup"><span data-stu-id="b3653-151">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="b3653-152">IIS 管理スクリプトおよびツール</span><span class="sxs-lookup"><span data-stu-id="b3653-152">IIS Management Scripts and Tools</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b3653-153">Windows Server 2008 R2 SP1 x64 オペレーティングシステムでは、Windows PowerShell 2.0 を使うことができます。</span><span class="sxs-lookup"><span data-stu-id="b3653-153">On the Windows Server 2008 R2 SP1 x64 operating system, you can use Windows PowerShell 2.0.</span></span> <span data-ttu-id="b3653-154">最初に ServerManager モジュールをインポートし、次に IIS 7.5 の役割と役割サービスをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3653-154">You must first import the ServerManager module, and then install the IIS 7.5 role and role services.</span></span>

   ```PowerShell
    Import-Module ServerManager
   ```

   ```PowerShell
    Add-WindowsFeature Web-Server, Web-Static-Content, Web-Default-Doc, Web-Scripting-Tools, Web-Windows-Auth, Web-Asp-Net, Web-Log-Libraries, Web-Http-Tracing, Web-Stat-Compression, Web-Dyn-Compression, Web-ISAPI-Ext, Web-ISAPI-Filter, Web-Http-Errors, Web-Http-Logging, Web-Net-Ext, Web-Client-Auth, Web-Filtering, Web-Mgmt-Console
   ```

<div class=" ">


> [!NOTE]  
> <span data-ttu-id="b3653-155">匿名認証は、既定で IIS server の役割と共にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="b3653-155">Anonymous authentication is installed by default with the IIS server role.</span></span> <span data-ttu-id="b3653-156">匿名認証は、IIS のインストール後に管理できます。</span><span class="sxs-lookup"><span data-stu-id="b3653-156">You can manage anonymous authentication after the installation of IIS.</span></span> <span data-ttu-id="b3653-157">詳細については、の「匿名認証 (IIS 7) を有効にする」を参照してください <A href="https://go.microsoft.com/fwlink/p/?linkid=203935">https://go.microsoft.com/fwlink/p/?linkId=203935</A> 。</span><span class="sxs-lookup"><span data-stu-id="b3653-157">For details, see “Enable Anonymous Authentication (IIS 7)” at <A href="https://go.microsoft.com/fwlink/p/?linkid=203935">https://go.microsoft.com/fwlink/p/?linkId=203935</A>.</span></span>



</div>

<span data-ttu-id="b3653-158">次の表は、Windows Server 2012 および Windows Server 2012 R2 に必要な IIS 8.0 と IIS 8.5 の役割サービスを示しています。</span><span class="sxs-lookup"><span data-stu-id="b3653-158">The following table indicates the required IIS 8.0 and IIS 8.5 role services for Windows Server 2012 and Windows Server 2012 R2.</span></span>

<div class=" ">


> [!NOTE]  
> <span data-ttu-id="b3653-159">Windows Server 2012 および Windows Server 2012 R2 の場合、Add-WindowsFeature コマンドレットは Install-WindowsFeature コマンドレットに置き換えられています。</span><span class="sxs-lookup"><span data-stu-id="b3653-159">For Windows Server 2012 and Windows Server 2012 R2, the Add-WindowsFeature cmdlet has been replaced by the Install-WindowsFeature cmdlet.</span></span> <span data-ttu-id="b3653-160">詳細については、「 <A href="https://go.microsoft.com/fwlink/p/?linkid=392274">Install-add-windowsfeature</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3653-160">For details, see <A href="https://go.microsoft.com/fwlink/p/?linkid=392274">Install-WindowsFeature</A>.</span></span>



</div>

### <a name="iis-80-and-iis-85-role-services"></a><span data-ttu-id="b3653-161">IIS 8.0 および IIS 8.5 の役割サービス</span><span class="sxs-lookup"><span data-stu-id="b3653-161">IIS 8.0 and IIS 8.5 Role Services</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b3653-162">ロール見出し</span><span class="sxs-lookup"><span data-stu-id="b3653-162">Role Heading</span></span></th>
<th><span data-ttu-id="b3653-163">役割サービス</span><span class="sxs-lookup"><span data-stu-id="b3653-163">Role Service</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b3653-164">Web サーバー (IIS)</span><span class="sxs-lookup"><span data-stu-id="b3653-164">Web Server (IIS)</span></span></p></td>
<td><p><span data-ttu-id="b3653-165">Web サーバー</span><span class="sxs-lookup"><span data-stu-id="b3653-165">Web Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3653-166">HTTP 共通機能</span><span class="sxs-lookup"><span data-stu-id="b3653-166">Common HTTP Features</span></span></p></td>
<td><p><span data-ttu-id="b3653-167">既定のドキュメント</span><span class="sxs-lookup"><span data-stu-id="b3653-167">Default Document</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3653-168">HTTP 共通機能</span><span class="sxs-lookup"><span data-stu-id="b3653-168">Common HTTP Features</span></span></p></td>
<td><p><span data-ttu-id="b3653-169">ディレクトリの参照</span><span class="sxs-lookup"><span data-stu-id="b3653-169">Directory Browsing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3653-170">HTTP 共通機能</span><span class="sxs-lookup"><span data-stu-id="b3653-170">Common HTTP Features</span></span></p></td>
<td><p><span data-ttu-id="b3653-171">HTTP エラー</span><span class="sxs-lookup"><span data-stu-id="b3653-171">HTTP Errors</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3653-172">HTTP 共通機能</span><span class="sxs-lookup"><span data-stu-id="b3653-172">Common HTTP Features</span></span></p></td>
<td><p><span data-ttu-id="b3653-173">静的なコンテンツ</span><span class="sxs-lookup"><span data-stu-id="b3653-173">Static content</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3653-174">HTTP 共通機能</span><span class="sxs-lookup"><span data-stu-id="b3653-174">Common HTTP Features</span></span></p></td>
<td><p><span data-ttu-id="b3653-175">HTTP リダイレクション</span><span class="sxs-lookup"><span data-stu-id="b3653-175">HTTP Redirection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3653-176">状態と診断</span><span class="sxs-lookup"><span data-stu-id="b3653-176">Health and Diagnostics</span></span></p></td>
<td><p><span data-ttu-id="b3653-177">HTTP ログ</span><span class="sxs-lookup"><span data-stu-id="b3653-177">HTTP Logging</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3653-178">状態と診断</span><span class="sxs-lookup"><span data-stu-id="b3653-178">Health and Diagnostics</span></span></p></td>
<td><p><span data-ttu-id="b3653-179">ログ ツール</span><span class="sxs-lookup"><span data-stu-id="b3653-179">Logging Tools</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3653-180">状態と診断</span><span class="sxs-lookup"><span data-stu-id="b3653-180">Health and Diagnostics</span></span></p></td>
<td><p><span data-ttu-id="b3653-181">要求監視</span><span class="sxs-lookup"><span data-stu-id="b3653-181">Request Monitor</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3653-182">状態と診断</span><span class="sxs-lookup"><span data-stu-id="b3653-182">Health and Diagnostics</span></span></p></td>
<td><p><span data-ttu-id="b3653-183">トレース</span><span class="sxs-lookup"><span data-stu-id="b3653-183">Tracing</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3653-184">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="b3653-184">Security</span></span></p></td>
<td><p><span data-ttu-id="b3653-185">要求のフィルタリング</span><span class="sxs-lookup"><span data-stu-id="b3653-185">Request Filtering</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3653-186">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="b3653-186">Security</span></span></p></td>
<td><p><span data-ttu-id="b3653-187">基本認証</span><span class="sxs-lookup"><span data-stu-id="b3653-187">Basic Authentication</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3653-188">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="b3653-188">Security</span></span></p></td>
<td><p><span data-ttu-id="b3653-189">クライアント証明書マッピング認証</span><span class="sxs-lookup"><span data-stu-id="b3653-189">Client Certificate Mapping Authentication</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3653-190">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="b3653-190">Security</span></span></p></td>
<td><p><span data-ttu-id="b3653-191">Windows 認証</span><span class="sxs-lookup"><span data-stu-id="b3653-191">Windows Authentication</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3653-192">アプリケーション開発</span><span class="sxs-lookup"><span data-stu-id="b3653-192">Application Development</span></span></p></td>
<td><p><span data-ttu-id="b3653-193">.Net 拡張機能3.5</span><span class="sxs-lookup"><span data-stu-id="b3653-193">.Net Extensibility 3.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3653-194">アプリケーション開発</span><span class="sxs-lookup"><span data-stu-id="b3653-194">Application Development</span></span></p></td>
<td><p><span data-ttu-id="b3653-195">.Net 拡張機能4.5</span><span class="sxs-lookup"><span data-stu-id="b3653-195">.Net Extensibility 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3653-196">アプリケーション開発</span><span class="sxs-lookup"><span data-stu-id="b3653-196">Application Development</span></span></p></td>
<td><p><span data-ttu-id="b3653-197">ASP.Net 3.5</span><span class="sxs-lookup"><span data-stu-id="b3653-197">ASP.Net 3.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3653-198">アプリケーション開発</span><span class="sxs-lookup"><span data-stu-id="b3653-198">Application Development</span></span></p></td>
<td><p><span data-ttu-id="b3653-199">ASP.Net 4.5</span><span class="sxs-lookup"><span data-stu-id="b3653-199">ASP.Net 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3653-200">アプリケーション開発</span><span class="sxs-lookup"><span data-stu-id="b3653-200">Application Development</span></span></p></td>
<td><p><span data-ttu-id="b3653-201">ISAPI 拡張機能</span><span class="sxs-lookup"><span data-stu-id="b3653-201">ISAPI Extensions</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3653-202">アプリケーション開発</span><span class="sxs-lookup"><span data-stu-id="b3653-202">Application Development</span></span></p></td>
<td><p><span data-ttu-id="b3653-203">ISAPI フィルター</span><span class="sxs-lookup"><span data-stu-id="b3653-203">ISAPI Filters</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3653-204">アプリケーション開発</span><span class="sxs-lookup"><span data-stu-id="b3653-204">Application Development</span></span></p></td>
<td><p><span data-ttu-id="b3653-205">サーバー側のインクルード</span><span class="sxs-lookup"><span data-stu-id="b3653-205">Server Side Includes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3653-206">管理ツール</span><span class="sxs-lookup"><span data-stu-id="b3653-206">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="b3653-207">IIS 管理コンソール</span><span class="sxs-lookup"><span data-stu-id="b3653-207">IIS Management Console</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3653-208">管理ツール</span><span class="sxs-lookup"><span data-stu-id="b3653-208">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="b3653-209">IIS 6 メタベースの互換性</span><span class="sxs-lookup"><span data-stu-id="b3653-209">IIS 6 Metabase compatibility</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3653-210">管理ツール</span><span class="sxs-lookup"><span data-stu-id="b3653-210">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="b3653-211">IIS 管理スクリプトおよびツール</span><span class="sxs-lookup"><span data-stu-id="b3653-211">IIS Management Scripts and Tools</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3653-212">.Net 3.5 Framework の機能</span><span class="sxs-lookup"><span data-stu-id="b3653-212">.Net 3.5 Framework Features</span></span></p></td>
<td><p><span data-ttu-id="b3653-213">.Net 3.5 フレームワーク</span><span class="sxs-lookup"><span data-stu-id="b3653-213">.Net 3.5 Framework</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3653-214">.Net 4.5 Framework の機能</span><span class="sxs-lookup"><span data-stu-id="b3653-214">.Net 4.5 Framework Features</span></span></p></td>
<td><p><span data-ttu-id="b3653-215">.Net Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="b3653-215">.Net Framework 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3653-216">.Net 4.5 Framework の機能</span><span class="sxs-lookup"><span data-stu-id="b3653-216">.Net 4.5 Framework Features</span></span></p></td>
<td><p><span data-ttu-id="b3653-217">ASP.Net 4.5</span><span class="sxs-lookup"><span data-stu-id="b3653-217">ASP.Net 4.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3653-218">.Net 4.5 Framework の機能</span><span class="sxs-lookup"><span data-stu-id="b3653-218">.Net 4.5 Framework Features</span></span></p></td>
<td><p><span data-ttu-id="b3653-219">HTTP アクティブ化</span><span class="sxs-lookup"><span data-stu-id="b3653-219">HTTP Activation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3653-220">.Net 4.5 Framework の機能</span><span class="sxs-lookup"><span data-stu-id="b3653-220">.Net 4.5 Framework Features</span></span></p></td>
<td><p><span data-ttu-id="b3653-221">TCP ポート共有</span><span class="sxs-lookup"><span data-stu-id="b3653-221">TCP Port Sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3653-222">バックグラウンドインテリジェント転送サービス</span><span class="sxs-lookup"><span data-stu-id="b3653-222">Background Intelligent Transfer Service</span></span></p></td>
<td><p><span data-ttu-id="b3653-223">IIS Server Extensions</span><span class="sxs-lookup"><span data-stu-id="b3653-223">IIS Server Extensions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3653-224">インクと手書きサービス</span><span class="sxs-lookup"><span data-stu-id="b3653-224">Ink and Handwriting Services</span></span></p></td>
<td><p><span data-ttu-id="b3653-225">インクと手書きサービス</span><span class="sxs-lookup"><span data-stu-id="b3653-225">Ink and Handwriting Services</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3653-226">メディア ファンデーション</span><span class="sxs-lookup"><span data-stu-id="b3653-226">Media Foundation</span></span></p></td>
<td><p><span data-ttu-id="b3653-227">メディア ファンデーション</span><span class="sxs-lookup"><span data-stu-id="b3653-227">Media Foundation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3653-228">ユーザーインターフェイスとインフラストラクチャ</span><span class="sxs-lookup"><span data-stu-id="b3653-228">User Interfaces and Infrastructure</span></span></p></td>
<td><p><span data-ttu-id="b3653-229">グラフィカル管理ツールとインフラストラクチャ</span><span class="sxs-lookup"><span data-stu-id="b3653-229">Graphical Management Tools and Infrastructure</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3653-230">ユーザーインターフェイスとインフラストラクチャ</span><span class="sxs-lookup"><span data-stu-id="b3653-230">User Interfaces and Infrastructure</span></span></p></td>
<td><p><span data-ttu-id="b3653-231">デスクトップエクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="b3653-231">Desktop Experience</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3653-232">ユーザーインターフェイスとインフラストラクチャ</span><span class="sxs-lookup"><span data-stu-id="b3653-232">User Interfaces and Infrastructure</span></span></p></td>
<td><p><span data-ttu-id="b3653-233">サーバーグラフィカルシェル</span><span class="sxs-lookup"><span data-stu-id="b3653-233">Server Graphical Shell</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3653-234">Windows Identity Foundation 3.5</span><span class="sxs-lookup"><span data-stu-id="b3653-234">Windows Identity Foundation 3.5</span></span></p></td>
<td><p><span data-ttu-id="b3653-235">Windows Identity Foundation 3.5</span><span class="sxs-lookup"><span data-stu-id="b3653-235">Windows Identity Foundation 3.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3653-236">Windows プロセスアクティブ化サービス</span><span class="sxs-lookup"><span data-stu-id="b3653-236">Windows Process Activation Service</span></span></p></td>
<td><p><span data-ttu-id="b3653-237">プロセスモデル</span><span class="sxs-lookup"><span data-stu-id="b3653-237">Process Model</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3653-238">Windows プロセスアクティブ化サービス</span><span class="sxs-lookup"><span data-stu-id="b3653-238">Windows Process Activation Service</span></span></p></td>
<td><p><span data-ttu-id="b3653-239">構成 Api</span><span class="sxs-lookup"><span data-stu-id="b3653-239">Configuration APIs</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b3653-240">Windows Server 2012 および Windows Server 2012 R2 では、Windows PowerShell 3.0 を使用して、IIS の要件をインストールできます。</span><span class="sxs-lookup"><span data-stu-id="b3653-240">In Windows Server 2012 and Windows Server 2012 R2, you can use Windows PowerShell 3.0 to install the IIS Requirements.</span></span> <span data-ttu-id="b3653-241">Windows PowerShell 3.0 で ServerManager モジュールを使用して、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="b3653-241">Using the ServerManager module in Windows PowerShell 3.0, type:</span></span>

   ```PowerShell
    Import-Module ServerManager
   ```

   ```PowerShell
    Add-WindowsFeature Web-Server, Web-Static-Content, Web-Default-Doc, Web-Http-Errors, Web-Asp-Net, Web-Net-Ext, Web-ISAPI-Ext, Web-ISAPI-Filter, Web-Http-Logging, Web-Log-Libraries, Web-Request-Monitor, Web-Http-Tracing, Web-Basic-Auth, Web-Windows-Auth, Web-Client-Auth, Web-Filtering, Web-Stat-Compression, Web-Dyn-Compression, NET-Framework-45-Core, NET-WCF-HTTP-Activation45, Web-Asp-Net45, Web-Mgmt-Tools, Web-Scripting-Tools, Web-Mgmt-Console, Web-Mgmt-Compat, Windows-Identity-Foundation, Server-Media-Foundation, BITS -Source D:\sources\sxs
   ```

<div class=" ">


> [!IMPORTANT]  
> <span data-ttu-id="b3653-242">Windows Server 2012 での新機能は、Windows Server 2012 ソースメディアが存在する場所を定義する、– Source パラメーターです。</span><span class="sxs-lookup"><span data-stu-id="b3653-242">New with Windows Server 2012 is the –Source parameter that defines where the Windows Server 2012 source media can be found.</span></span> <span data-ttu-id="b3653-243">メディアは、DVD ドライブ (D:\Sources\Sxs など)、またはメディアファイルがコピーされたネットワーク共有 (Fileserver\windows2012\sources\Sxs など) として定義でき \\ ます。</span><span class="sxs-lookup"><span data-stu-id="b3653-243">The media can be defined as a DVD drive (for example, D:\Sources\Sxs), or to a network share that the media files have been copied (for example, \\fileserver\windows2012\sources\Sxs).</span></span>



</div>

<div>

## <a name="see-also"></a><span data-ttu-id="b3653-244">関連項目</span><span class="sxs-lookup"><span data-stu-id="b3653-244">See Also</span></span>


[<span data-ttu-id="b3653-245">Lync Server 2013 のフロントエンド プールおよび Standard Edition サーバーの IIS 要件</span><span class="sxs-lookup"><span data-stu-id="b3653-245">IIS requirements for Front End pools and Standard Edition servers in Lync Server 2013</span></span>](lync-server-2013-iis-requirements-for-front-end-pools-and-standard-edition-servers.md)  
  

<span data-ttu-id="b3653-246"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b3653-246"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

