---
title: 'Lync Server 2013: 内部サーバーに対する証明書要件'
description: 'Lync Server 2013: 内部サーバーの証明書の要件。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate requirements for internal servers
ms:assetid: 0444cdbd-538c-43b1-b9a1-9d7d6cf818d6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398094(v=OCS.15)
ms:contentKeyID: 48183270
ms.date: 02/17/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dc1a627dd762c849b848087a96e00e19d320ef01
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435356"
---
# <a name="certificate-requirements-for-internal-servers-in-lync-server-2013"></a><span data-ttu-id="d03bc-103">Lync Server 2013 の内部サーバーに対する証明書要件</span><span class="sxs-lookup"><span data-stu-id="d03bc-103">Certificate requirements for internal servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d03bc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d03bc-104">

<span> </span></span></span>

<span data-ttu-id="d03bc-105">_**最終更新日:** 2017-02-17_</span><span class="sxs-lookup"><span data-stu-id="d03bc-105">_**Topic Last Modified:** 2017-02-17_</span></span>

<span data-ttu-id="d03bc-106">Lync Server を実行していて、証明書を必要とする内部サーバーには、Standard Edition Server、Enterprise Edition フロントエンドサーバー、仲介サーバー、およびディレクターが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d03bc-106">Internal servers that are running Lync Server and that require certificates include Standard Edition server, Enterprise Edition Front End Server, Mediation Server, and Director.</span></span> <span data-ttu-id="d03bc-107">次の表は、これらのサーバーの証明書要件を示しています。</span><span class="sxs-lookup"><span data-stu-id="d03bc-107">The following table shows the certificate requirements for these servers.</span></span> <span data-ttu-id="d03bc-108">Lync Server 証明書ウィザードを使って、これらの証明書を要求することができます。</span><span class="sxs-lookup"><span data-stu-id="d03bc-108">You can use the Lync Server certificate wizard to request these certificates.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="d03bc-109">ワイルドカード証明書は、フロントエンドプール、フロントエンドサーバー、またはディレクターの単純な Url に関連付けられたサブジェクトの別名でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="d03bc-109">Wildcard certificates are supported for the subject alternative names associated with the simple URLs on the Front End pool, Front End Server, or Director.</span></span> <span data-ttu-id="d03bc-110">ワイルドカード証明書のサポートについて詳しくは、「 <A href="lync-server-2013-wildcard-certificate-support.md">Lync Server 2013 でのワイルドカード証明書のサポート</A>」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="d03bc-110">For details about wildcard certificate support, see <A href="lync-server-2013-wildcard-certificate-support.md">Wildcard certificate support in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="d03bc-111">内部サーバーでは社内のエンタープライズ証明機関 (CA) を使うことをお勧めしますが、パブリック CA を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="d03bc-111">Although an internal enterprise certification authority (CA) is recommended for internal servers, you can also use a public CA.</span></span> <span data-ttu-id="d03bc-112">統合通信 (UC) 証明書の特定の要件に準拠し、Microsoft と提携して Lync Server の証明書ウィザードで動作することを確認するパブリック Ca の一覧については、「Microsoft サポート技術情報929395」、「Exchange Server および通信サーバーのユニファイドコミュニケーション証明書パートナー」を参照してください [https://go.microsoft.com/fwlink/p/?linkId=202834](https://go.microsoft.com/fwlink/p/?linkid=202834) 。</span><span class="sxs-lookup"><span data-stu-id="d03bc-112">For a list of public CAs that provide certificates that comply with specific requirements for unified communications (UC) certificates and have partnered with Microsoft to ensure they work with the Lync Server Certificate Wizard, see article Microsoft Knowledge Base 929395, "Unified Communications Certificate Partners for Exchange Server and for Communications Server," at [https://go.microsoft.com/fwlink/p/?linkId=202834](https://go.microsoft.com/fwlink/p/?linkid=202834).</span></span>

<span data-ttu-id="d03bc-113">他のアプリケーションやサーバー (Exchange 2013 など) との通信には、他のアプリケーションや製品でサポートされている証明書が必要です。</span><span class="sxs-lookup"><span data-stu-id="d03bc-113">Communication with other applications and servers, such as Exchange 2013, requires a certificate that is supported by the other applications and products.</span></span> <span data-ttu-id="d03bc-114">2013リリース、Lync Server 2013、および Exchange 2013 および SharePoint Server を含むその他の Microsoft サーバー製品については、サーバー間の認証と承認のための Open Authorization (OAuth) プロトコルをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="d03bc-114">For the 2013 release, Lync Server 2013 and other Microsoft server products, including Exchange 2013 and SharePoint Server, support the Open Authorization (OAuth) protocol for server-to-server authentication and authorization.</span></span> <span data-ttu-id="d03bc-115">詳細については、展開ドキュメントまたは運用マニュアルの「 [Lync server 2013 でサーバー間認証 (OAuth) とパートナーアプリケーションを管理する](lync-server-2013-managing-server-to-server-authentication-oauth-and-partner-applications.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d03bc-115">For details, see [Managing server-to-server authentication (OAuth) and partner applications in Lync Server 2013](lync-server-2013-managing-server-to-server-authentication-oauth-and-partner-applications.md) in the Deployment documentation or the Operations documentation.</span></span>

<span data-ttu-id="d03bc-116">Windows 7 オペレーティングシステム、windows Server 2008 オペレーティングシステム、windows server 2008 R2 オペレーティングシステム、Windows Vista オペレーティングシステム、Microsoft Lync Phone Edition を実行しているクライアントからの接続の場合、Lync Server 2013 には、SHA-256 暗号化ハッシュ関数を使って署名された証明書のサポートが含まれます (ただし、必須ではありません)。</span><span class="sxs-lookup"><span data-stu-id="d03bc-116">For connections from clients running Windows 7 operating system, Windows Server 2008 operating system, Windows Server 2008 R2 operating system, Windows Vista operating system, and Microsoft Lync Phone Edition, Lync Server 2013 includes support for (but does not require) certificates signed using the SHA-256 cryptographic hash function.</span></span> <span data-ttu-id="d03bc-117">SHA-256 を使って外部アクセスをサポートするために、外部証明書は SHA-256 を使ってパブリック CA によって発行されます。</span><span class="sxs-lookup"><span data-stu-id="d03bc-117">To support external access using SHA-256, the external certificate is issued by a public CA using SHA-256.</span></span>

<span data-ttu-id="d03bc-118">次の表は、フロントエンドプールと Standard Edition サーバーのサーバーロールごとの証明書要件を示しています。</span><span class="sxs-lookup"><span data-stu-id="d03bc-118">The following tables show certificate requirements by server role for Front End pools and Standard Edition servers.</span></span> <span data-ttu-id="d03bc-119">これらはすべて、標準の web サーバー証明書、秘密キー、エクスポートできません。</span><span class="sxs-lookup"><span data-stu-id="d03bc-119">All these are standard web server certificates, private key, non-exportable.</span></span>

<span data-ttu-id="d03bc-120">証明書ウィザードを使用して証明書を要求するときに、サーバーの拡張キー使用法 (EKU) が自動的に構成されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d03bc-120">Note that server enhanced key usage (EKU) is automatically configured when you use the certificate wizard to request certificates.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="d03bc-121">各証明書のフレンドリ名は、コンピューターストア内で一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="d03bc-121">Each certificate Friendly Name must be unique in the computer store.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="d03bc-122">DNS で sipinternal.contoso.com または sipexternal.contoso.com を構成している場合は、証明書のサブジェクトの代替名にそれらを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d03bc-122">If you have configured sipinternal.contoso.com or sipexternal.contoso.com in your DNS, you will need to add them in the certificate’s Subject Alternative Name.</span></span>



</div>

### <a name="certificates-for-standard-edition-server"></a><span data-ttu-id="d03bc-123">Standard Edition Server 用の証明書</span><span class="sxs-lookup"><span data-stu-id="d03bc-123">Certificates for Standard Edition Server</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d03bc-124">証明書</span><span class="sxs-lookup"><span data-stu-id="d03bc-124">Certificate</span></span></th>
<th><span data-ttu-id="d03bc-125">サブジェクト名/共通名</span><span class="sxs-lookup"><span data-stu-id="d03bc-125">Subject name/ Common name</span></span></th>
<th><span data-ttu-id="d03bc-126">サブジェクトの別名</span><span class="sxs-lookup"><span data-stu-id="d03bc-126">Subject alternative name</span></span></th>
<th><span data-ttu-id="d03bc-127">例</span><span class="sxs-lookup"><span data-stu-id="d03bc-127">Example</span></span></th>
<th><span data-ttu-id="d03bc-128">コメント</span><span class="sxs-lookup"><span data-stu-id="d03bc-128">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d03bc-129">Default</span><span class="sxs-lookup"><span data-stu-id="d03bc-129">Default</span></span></p></td>
<td><p><span data-ttu-id="d03bc-130">プールの完全修飾ドメイン名 (FQDN)</span><span class="sxs-lookup"><span data-stu-id="d03bc-130">Fully qualified domain name (FQDN) of the pool</span></span></p></td>
<td><p><span data-ttu-id="d03bc-131">プールの FQDN とサーバーの FQDN</span><span class="sxs-lookup"><span data-stu-id="d03bc-131">FQDN of the pool and the FQDN of the server</span></span></p>
<p><span data-ttu-id="d03bc-132">SIP ドメインが複数あり、自動クライアント構成が有効な場合は、証明書ウィザードによって、サポートされている各 SIP ドメインの FQDN が検出され、追加されます。</span><span class="sxs-lookup"><span data-stu-id="d03bc-132">If you have multiple SIP domains and have enabled automatic client configuration, the certificate wizard detects and adds each supported SIP domain FQDNs.</span></span></p>
<p><span data-ttu-id="d03bc-133">このプールがクライアントの自動ログオン サーバーであり、グループ ポリシーで厳密なドメイン ネーム システム (DNS) マッチングが必要な場合は、sip.sipdomain のエントリ (所有する各 SIP ドメイン用) も必要となります。</span><span class="sxs-lookup"><span data-stu-id="d03bc-133">If this pool is the auto-logon server for clients and strict Domain Name System (DNS) matching is required in group policy, you also need entries for sip.sipdomain (for each SIP domain you have).</span></span></p></td>
<td><p><span data-ttu-id="d03bc-134">SN=se01.contoso.com; SAN=se01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d03bc-134">SN=se01.contoso.com; SAN=se01.contoso.com</span></span></p>
<p><span data-ttu-id="d03bc-135">このプールがクライアントの自動ログオン サーバーであり、グループ ポリシーで厳密な DNS マッチングが必要な場合は、SAN=sip.contoso.com、SAN=sip.fabrikam.com も必要です。</span><span class="sxs-lookup"><span data-stu-id="d03bc-135">If this pool is the auto-logon server for clients and strict DNS matching is required in group policy, you also need SAN=sip.contoso.com; SAN=sip.fabrikam.com</span></span></p></td>
<td><p><span data-ttu-id="d03bc-136">Standard Edition server では、サーバーの FQDN はプールの FQDN と同じです。</span><span class="sxs-lookup"><span data-stu-id="d03bc-136">On Standard Edition server, the server FQDN is the same as the pool FQDN.</span></span></p>
<p><span data-ttu-id="d03bc-137">このウィザードでは、セットアップ時に指定した SIP ドメインが検出され、サブジェクトの別名に自動的に追加されます。</span><span class="sxs-lookup"><span data-stu-id="d03bc-137">The wizard detects any SIP domains you specified during setup and automatically adds them to the subject alternative name.</span></span></p>
<p><span data-ttu-id="d03bc-138">また、この証明書はサーバー間認証でも使用できます。</span><span class="sxs-lookup"><span data-stu-id="d03bc-138">You can also use this certificate for Server-to-Server Authentication.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d03bc-139">内部 Web</span><span class="sxs-lookup"><span data-stu-id="d03bc-139">Web internal</span></span></p></td>
<td><p><span data-ttu-id="d03bc-140">サーバーの FQDN</span><span class="sxs-lookup"><span data-stu-id="d03bc-140">FQDN of the server</span></span></p></td>
<td><p><span data-ttu-id="d03bc-141">次のうちのすべて:</span><span class="sxs-lookup"><span data-stu-id="d03bc-141">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="d03bc-142">内部 Web FQDN (サーバーの FQDN と同じ)</span><span class="sxs-lookup"><span data-stu-id="d03bc-142">Internal web FQDN (which is the same as the FQDN of the server)</span></span></p></li>
<li><p><span data-ttu-id="d03bc-143">会議の簡易 URL</span><span class="sxs-lookup"><span data-stu-id="d03bc-143">Meet simple URLs</span></span></p></li>
<li><p><span data-ttu-id="d03bc-144">ダイヤルインの簡易 URL</span><span class="sxs-lookup"><span data-stu-id="d03bc-144">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="d03bc-145">管理の簡易 URL</span><span class="sxs-lookup"><span data-stu-id="d03bc-145">Admin simple URL</span></span></p></li>
<li><p><span data-ttu-id="d03bc-146">または、単純な Url のワイルドカードエントリ</span><span class="sxs-lookup"><span data-stu-id="d03bc-146">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="d03bc-147">SN=se01.contoso.com; SAN=se01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d03bc-147">SN=se01.contoso.com; SAN=se01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span></span></p>
<p><span data-ttu-id="d03bc-148">ワイルドカード証明書使用時:</span><span class="sxs-lookup"><span data-stu-id="d03bc-148">Using a wildcard certificate:</span></span></p>
<p><span data-ttu-id="d03bc-149">SN=se01.contoso.com; SAN=se01.contoso.com; SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d03bc-149">SN=se01.contoso.com; SAN=se01.contoso.com; SAN=\*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="d03bc-150">トポロジビルダーで内部 web FQDN を上書きすることはできません。</span><span class="sxs-lookup"><span data-stu-id="d03bc-150">You cannot override the Internal web FQDN in Topology Builder.</span></span></p>
<p><span data-ttu-id="d03bc-151">複数の条件を満たす単純な Url がある場合は、それらのすべてを対象の代替名として含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="d03bc-151">If you have multiple Meet simple URLs, you must include all of them as subject alternative names.</span></span></p>
<p><span data-ttu-id="d03bc-152">簡易 URL エントリではワイルドカード エントリがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="d03bc-152">Wildcard entries are supported for the simple URL entries.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d03bc-153">外部 Web</span><span class="sxs-lookup"><span data-stu-id="d03bc-153">Web external</span></span></p></td>
<td><p><span data-ttu-id="d03bc-154">サーバーの FQDN</span><span class="sxs-lookup"><span data-stu-id="d03bc-154">FQDN of the server</span></span></p></td>
<td><p><span data-ttu-id="d03bc-155">次のうちのすべて:</span><span class="sxs-lookup"><span data-stu-id="d03bc-155">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="d03bc-156">外部 Web FQDN</span><span class="sxs-lookup"><span data-stu-id="d03bc-156">External web FQDN</span></span></p></li>
<li><p><span data-ttu-id="d03bc-157">ダイヤルインの簡易 URL</span><span class="sxs-lookup"><span data-stu-id="d03bc-157">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="d03bc-158">SIP ドメインごとの会議の簡易 URL</span><span class="sxs-lookup"><span data-stu-id="d03bc-158">Meet simple URLs per SIP domain</span></span></p></li>
<li><p><span data-ttu-id="d03bc-159">または、単純な Url のワイルドカードエントリ</span><span class="sxs-lookup"><span data-stu-id="d03bc-159">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="d03bc-160">SN=se01.contoso.com; SAN=webcon01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d03bc-160">SN=se01.contoso.com; SAN=webcon01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span></span></p>
<p><span data-ttu-id="d03bc-161">ワイルドカード証明書使用時:</span><span class="sxs-lookup"><span data-stu-id="d03bc-161">Using a wildcard certificate:</span></span></p>
<p><span data-ttu-id="d03bc-162">SN=se01.contoso.com; SAN=webcon01.contoso.com; SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d03bc-162">SN=se01.contoso.com; SAN=webcon01.contoso.com; SAN=\*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="d03bc-163">複数の条件を満たす単純な Url がある場合は、それらのすべてを対象の代替名として含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="d03bc-163">If you have multiple Meet simple URLs, you must include all of them as subject alternative names.</span></span></p>
<p><span data-ttu-id="d03bc-164">簡易 URL エントリではワイルドカード エントリがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="d03bc-164">Wildcard entries are supported for the simple URL entries.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="certificates-for-front-end-server-in-a-front-end-pool"></a><span data-ttu-id="d03bc-165">フロントエンドプールのフロントエンドサーバー用の証明書</span><span class="sxs-lookup"><span data-stu-id="d03bc-165">Certificates for Front End Server in a Front End Pool</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d03bc-166">証明書</span><span class="sxs-lookup"><span data-stu-id="d03bc-166">Certificate</span></span></th>
<th><span data-ttu-id="d03bc-167">サブジェクト名/共通名</span><span class="sxs-lookup"><span data-stu-id="d03bc-167">Subject name/ Common name</span></span></th>
<th><span data-ttu-id="d03bc-168">サブジェクトの別名</span><span class="sxs-lookup"><span data-stu-id="d03bc-168">Subject alternative name</span></span></th>
<th><span data-ttu-id="d03bc-169">例</span><span class="sxs-lookup"><span data-stu-id="d03bc-169">Example</span></span></th>
<th><span data-ttu-id="d03bc-170">コメント</span><span class="sxs-lookup"><span data-stu-id="d03bc-170">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d03bc-171">Default</span><span class="sxs-lookup"><span data-stu-id="d03bc-171">Default</span></span></p></td>
<td><p><span data-ttu-id="d03bc-172">プールの FQDN</span><span class="sxs-lookup"><span data-stu-id="d03bc-172">FQDN of the pool</span></span></p></td>
<td><p><span data-ttu-id="d03bc-173">サーバーのプールと FQDN の FQDN。</span><span class="sxs-lookup"><span data-stu-id="d03bc-173">FQDN of the pool and FQDN of the server.</span></span></p>
<p><span data-ttu-id="d03bc-174">SIP ドメインが複数あり、自動クライアント構成が有効な場合は、証明書ウィザードによって、サポートされている各 SIP ドメインの FQDN が検出され、追加されます。</span><span class="sxs-lookup"><span data-stu-id="d03bc-174">If you have multiple SIP domains and have enabled automatic client configuration, the certificate wizard detects and adds each supported SIP domain FQDNs.</span></span></p>
<p><span data-ttu-id="d03bc-175">このプールがクライアント用の自動ログオンサーバーであり、かつ厳密な DNS 一致がグループポリシーで必要となる場合は、sipdomain (SIP ドメインごとに) を入力する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="d03bc-175">If this pool is the auto-logon server for clients and strict DNS matching is required in group policy, you also need entries for sip.sipdomain (for each SIP domain you have).</span></span></p></td>
<td><p><span data-ttu-id="d03bc-176">SN=eepool.contoso.com; SAN=eepool.contoso.com; SAN=ee01.contoso.com </span><span class="sxs-lookup"><span data-stu-id="d03bc-176">SN=eepool.contoso.com; SAN=eepool.contoso.com; SAN=ee01.contoso.com</span></span></p>
<p><span data-ttu-id="d03bc-177">このプールがクライアントの自動ログオン サーバーであり、グループ ポリシーで厳密な DNS マッチングが必要な場合は、SAN=sip.contoso.com、SAN=sip.fabrikam.com も必要です。</span><span class="sxs-lookup"><span data-stu-id="d03bc-177">If this pool is the auto-logon server for clients and strict DNS matching is required in group policy, you also need SAN=sip.contoso.com; SAN=sip.fabrikam.com</span></span></p></td>
<td><p><span data-ttu-id="d03bc-178">このウィザードでは、セットアップ時に指定した SIP ドメインが検出され、サブジェクトの別名に自動的に追加されます。</span><span class="sxs-lookup"><span data-stu-id="d03bc-178">The wizard detects any SIP domains you specified during setup and automatically adds them to the subject alternative name.</span></span></p>
<p><span data-ttu-id="d03bc-179">また、この証明書はサーバー間認証でも使用できます。</span><span class="sxs-lookup"><span data-stu-id="d03bc-179">You can also use this certificate for Server-to-Server Authentication.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d03bc-180">Web 内部</span><span class="sxs-lookup"><span data-stu-id="d03bc-180">Web Internal</span></span></p></td>
<td><p><span data-ttu-id="d03bc-181">プールの FQDN</span><span class="sxs-lookup"><span data-stu-id="d03bc-181">FQDN of the pool</span></span></p></td>
<td><p><span data-ttu-id="d03bc-182">次のうちのすべて:</span><span class="sxs-lookup"><span data-stu-id="d03bc-182">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="d03bc-183">内部 Web FQDN (サーバーの FQDN とは異なる)</span><span class="sxs-lookup"><span data-stu-id="d03bc-183">Internal web FQDN (which is NOT the same as the FQDN of the server)</span></span></p></li>
<li><p><span data-ttu-id="d03bc-184">サーバーの FQDN</span><span class="sxs-lookup"><span data-stu-id="d03bc-184">Server FQDN</span></span></p></li>
<li><p><span data-ttu-id="d03bc-185">Lync プールの FQDN</span><span class="sxs-lookup"><span data-stu-id="d03bc-185">Lync pool FQDN</span></span></p></li>
<li><p><span data-ttu-id="d03bc-186">会議の簡易 URL</span><span class="sxs-lookup"><span data-stu-id="d03bc-186">Meet simple URLs</span></span></p></li>
<li><p><span data-ttu-id="d03bc-187">ダイヤルインの簡易 URL</span><span class="sxs-lookup"><span data-stu-id="d03bc-187">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="d03bc-188">管理の簡易 URL</span><span class="sxs-lookup"><span data-stu-id="d03bc-188">Admin simple URL</span></span></p></li>
<li><p><span data-ttu-id="d03bc-189">または、単純な Url のワイルドカードエントリ</span><span class="sxs-lookup"><span data-stu-id="d03bc-189">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="d03bc-190">SN=ee01.contoso.com; SAN=ee01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d03bc-190">SN=ee01.contoso.com; SAN=ee01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span></span></p>
<p><span data-ttu-id="d03bc-191">ワイルドカード証明書使用時:</span><span class="sxs-lookup"><span data-stu-id="d03bc-191">Using a wildcard certificate:</span></span></p>
<p><span data-ttu-id="d03bc-192">SN=ee01.contoso.com; SAN=ee01.contoso.com; SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d03bc-192">SN=ee01.contoso.com; SAN=ee01.contoso.com; SAN=\*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="d03bc-193">複数の条件を満たす単純な Url がある場合は、それらのすべてを対象の代替名として含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="d03bc-193">If you have multiple Meet simple URLs, you must include all of them as subject alternative names.</span></span></p>
<p><span data-ttu-id="d03bc-194">簡易 URL エントリではワイルドカード エントリがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="d03bc-194">Wildcard entries are supported for the simple URL entries.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d03bc-195">外部 Web</span><span class="sxs-lookup"><span data-stu-id="d03bc-195">Web external</span></span></p></td>
<td><p><span data-ttu-id="d03bc-196">プールの FQDN</span><span class="sxs-lookup"><span data-stu-id="d03bc-196">FQDN of the pool</span></span></p></td>
<td><p><span data-ttu-id="d03bc-197">次のうちのすべて:</span><span class="sxs-lookup"><span data-stu-id="d03bc-197">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="d03bc-198">外部 Web FQDN</span><span class="sxs-lookup"><span data-stu-id="d03bc-198">External web FQDN</span></span></p></li>
<li><p><span data-ttu-id="d03bc-199">ダイヤルインの簡易 URL</span><span class="sxs-lookup"><span data-stu-id="d03bc-199">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="d03bc-200">管理の簡易 URL</span><span class="sxs-lookup"><span data-stu-id="d03bc-200">Admin simple URL</span></span></p></li>
<li><p><span data-ttu-id="d03bc-201">または、単純な Url のワイルドカードエントリ</span><span class="sxs-lookup"><span data-stu-id="d03bc-201">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="d03bc-202">SN=ee01.contoso.com; SAN=webcon01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d03bc-202">SN=ee01.contoso.com; SAN=webcon01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span></span></p>
<p><span data-ttu-id="d03bc-203">ワイルドカード証明書使用時:</span><span class="sxs-lookup"><span data-stu-id="d03bc-203">Using a wildcard certificate:</span></span></p>
<p><span data-ttu-id="d03bc-204">SN=ee01.contoso.com; SAN=webcon01.contoso.com; SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d03bc-204">SN=ee01.contoso.com; SAN=webcon01.contoso.com; SAN=\*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="d03bc-205">複数の条件を満たす単純な Url がある場合は、それらのすべてを対象の代替名として含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="d03bc-205">If you have multiple Meet simple URLs, you must include all of them as subject alternative names.</span></span></p>
<p><span data-ttu-id="d03bc-206">簡易 URL エントリではワイルドカード エントリがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="d03bc-206">Wildcard entries are supported for the simple URL entries.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="certificates-for-director"></a><span data-ttu-id="d03bc-207">ディレクター用の証明書</span><span class="sxs-lookup"><span data-stu-id="d03bc-207">Certificates for Director</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d03bc-208">証明書</span><span class="sxs-lookup"><span data-stu-id="d03bc-208">Certificate</span></span></th>
<th><span data-ttu-id="d03bc-209">サブジェクト名/共通名</span><span class="sxs-lookup"><span data-stu-id="d03bc-209">Subject name/ Common name</span></span></th>
<th><span data-ttu-id="d03bc-210">サブジェクトの別名</span><span class="sxs-lookup"><span data-stu-id="d03bc-210">Subject alternative name</span></span></th>
<th><span data-ttu-id="d03bc-211">例</span><span class="sxs-lookup"><span data-stu-id="d03bc-211">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d03bc-212">Default</span><span class="sxs-lookup"><span data-stu-id="d03bc-212">Default</span></span></p></td>
<td><p><span data-ttu-id="d03bc-213">ディレクタープールの FQDN</span><span class="sxs-lookup"><span data-stu-id="d03bc-213">FQDN of the Director pool</span></span></p></td>
<td><p><span data-ttu-id="d03bc-214">ディレクタープールの FQDN の fqdn。</span><span class="sxs-lookup"><span data-stu-id="d03bc-214">FQDN of the Director, FQDN of the Director pool</span></span></p>
<p><span data-ttu-id="d03bc-215">このプールがクライアント用の自動ログオンサーバーであり、かつ厳密な DNS 一致がグループポリシーで必要となる場合は、sipdomain (SIP ドメインごとに) を入力する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="d03bc-215">If this pool is the auto-logon server for clients and strict DNS matching is required in group policy, you also need entries for sip.sipdomain (for each SIP domain you have).</span></span></p></td>
<td><p><span data-ttu-id="d03bc-216">SN = dir-pool.contoso.com;SAN = dir-pool.contoso.com;SAN = dir01</span><span class="sxs-lookup"><span data-stu-id="d03bc-216">SN=dir-pool.contoso.com; SAN=dir-pool.contoso.com; SAN=dir01.contoso.com</span></span></p>
<p><span data-ttu-id="d03bc-217">このディレクタープールがクライアント用の自動ログオンサーバーであり、かつ厳密な DNS 一致がグループポリシーで必要な場合は、SAN = sip-pstn を使用する必要もあります。サン = sip-pstn</span><span class="sxs-lookup"><span data-stu-id="d03bc-217">If this Director pool is the auto-logon server for clients and strict DNS matching is required in group policy, you also need SAN=sip.contoso.com; SAN=sip.fabrikam.com</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d03bc-218">Web 内部</span><span class="sxs-lookup"><span data-stu-id="d03bc-218">Web Internal</span></span></p></td>
<td><p><span data-ttu-id="d03bc-219">サーバーの FQDN</span><span class="sxs-lookup"><span data-stu-id="d03bc-219">FQDN of the server</span></span></p></td>
<td><p><span data-ttu-id="d03bc-220">次のうちのすべて:</span><span class="sxs-lookup"><span data-stu-id="d03bc-220">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="d03bc-221">内部 Web FQDN (サーバーの FQDN と同じ)</span><span class="sxs-lookup"><span data-stu-id="d03bc-221">Internal web FQDN (which is the same as the FQDN of the server)</span></span></p></li>
<li><p><span data-ttu-id="d03bc-222">サーバーの FQDN</span><span class="sxs-lookup"><span data-stu-id="d03bc-222">Server FQDN</span></span></p></li>
<li><p><span data-ttu-id="d03bc-223">Lync プールの FQDN</span><span class="sxs-lookup"><span data-stu-id="d03bc-223">Lync pool FQDN</span></span></p></li>
<li><p><span data-ttu-id="d03bc-224">会議の簡易 URL</span><span class="sxs-lookup"><span data-stu-id="d03bc-224">Meet simple URLs</span></span></p></li>
<li><p><span data-ttu-id="d03bc-225">ダイヤルインの簡易 URL</span><span class="sxs-lookup"><span data-stu-id="d03bc-225">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="d03bc-226">管理の簡易 URL</span><span class="sxs-lookup"><span data-stu-id="d03bc-226">Admin simple URL</span></span></p></li>
<li><p><span data-ttu-id="d03bc-227">または、単純な Url のワイルドカードエントリ</span><span class="sxs-lookup"><span data-stu-id="d03bc-227">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="d03bc-228">SN=dir01.contoso.com; SAN=dir01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d03bc-228">SN=dir01.contoso.com; SAN=dir01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span></span></p>
<p><span data-ttu-id="d03bc-229">SN=dir01.contoso.com; SAN=dir01.contoso.com SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d03bc-229">SN=dir01.contoso.com; SAN=dir01.contoso.com SAN=\*.contoso.com</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d03bc-230">外部 Web</span><span class="sxs-lookup"><span data-stu-id="d03bc-230">Web external</span></span></p></td>
<td><p><span data-ttu-id="d03bc-231">サーバーの FQDN</span><span class="sxs-lookup"><span data-stu-id="d03bc-231">FQDN of the server</span></span></p></td>
<td><p><span data-ttu-id="d03bc-232">次のうちのすべて:</span><span class="sxs-lookup"><span data-stu-id="d03bc-232">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="d03bc-233">外部 Web FQDN</span><span class="sxs-lookup"><span data-stu-id="d03bc-233">External web FQDN</span></span></p></li>
<li><p><span data-ttu-id="d03bc-234">ダイヤルインの簡易 URL</span><span class="sxs-lookup"><span data-stu-id="d03bc-234">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="d03bc-235">管理の簡易 URL</span><span class="sxs-lookup"><span data-stu-id="d03bc-235">Admin simple URL</span></span></p></li>
<li><p><span data-ttu-id="d03bc-236">または、単純な Url のワイルドカードエントリ</span><span class="sxs-lookup"><span data-stu-id="d03bc-236">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="d03bc-237">ディレクターの外部 web FQDN は、フロントエンドプールまたはフロントエンドサーバーと異なっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="d03bc-237">The Director external web FQDN must be different from the Front End pool or Front End Server.</span></span></p>
<p><span data-ttu-id="d03bc-238">SN=dir01.contoso.com; SAN=directorwebcon01.contoso.com SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d03bc-238">SN=dir01.contoso.com; SAN=directorwebcon01.contoso.com SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span></span></p>
<p><span data-ttu-id="d03bc-239">SN=dir01.contoso.com; SAN=directorwebcon01.contoso.com SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="d03bc-239">SN=dir01.contoso.com; SAN=directorwebcon01.contoso.com SAN=\*.contoso.com</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d03bc-240">スタンドアロンの仲介サーバープールを使用している場合、それぞれの仲介サーバーには、次の表に示す証明書が必要です。</span><span class="sxs-lookup"><span data-stu-id="d03bc-240">If you have a stand-alone Mediation Server pool, the Mediation Servers in it each need the certificates listed in the following table.</span></span> <span data-ttu-id="d03bc-241">フロントエンドサーバーによって仲介サーバーがある場合は、このトピックの前半の「フロントエンドプールの証明書」の表に記載されている証明書を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d03bc-241">If you collocate Mediation Server with the Front End Servers, the certificates listed in the “Certificates for Front End Server in Front End Pool” table earlier in this topic are sufficient.</span></span>

### <a name="certificates-for-stand-alone-mediation-server"></a><span data-ttu-id="d03bc-242">スタンドアロンの仲介サーバー用の証明書</span><span class="sxs-lookup"><span data-stu-id="d03bc-242">Certificates for Stand-alone Mediation Server</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d03bc-243">証明書</span><span class="sxs-lookup"><span data-stu-id="d03bc-243">Certificate</span></span></th>
<th><span data-ttu-id="d03bc-244">サブジェクト名/共通名</span><span class="sxs-lookup"><span data-stu-id="d03bc-244">Subject name/ Common name</span></span></th>
<th><span data-ttu-id="d03bc-245">サブジェクトの別名</span><span class="sxs-lookup"><span data-stu-id="d03bc-245">Subject alternative name</span></span></th>
<th><span data-ttu-id="d03bc-246">例</span><span class="sxs-lookup"><span data-stu-id="d03bc-246">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d03bc-247">Default</span><span class="sxs-lookup"><span data-stu-id="d03bc-247">Default</span></span></p></td>
<td><p><span data-ttu-id="d03bc-248">プールの FQDN</span><span class="sxs-lookup"><span data-stu-id="d03bc-248">FQDN of the pool</span></span></p></td>
<td><p><span data-ttu-id="d03bc-249">プールの FQDN</span><span class="sxs-lookup"><span data-stu-id="d03bc-249">FQDN of the pool</span></span></p>
<p><span data-ttu-id="d03bc-250">プールメンバーサーバーの FQDN</span><span class="sxs-lookup"><span data-stu-id="d03bc-250">FQDN of pool member server</span></span></p></td>
<td><p><span data-ttu-id="d03bc-251">SN=medsvr-pool.contoso.net; SAN=medsvr-pool.contoso.net; SAN=medsvr01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="d03bc-251">SN=medsvr-pool.contoso.net; SAN=medsvr-pool.contoso.net; SAN=medsvr01.contoso.net</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="certificates-for-survivable-branch-appliance"></a><span data-ttu-id="d03bc-252">Survivable Branch Appliance 用の証明書</span><span class="sxs-lookup"><span data-stu-id="d03bc-252">Certificates for Survivable Branch Appliance</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d03bc-253">証明書</span><span class="sxs-lookup"><span data-stu-id="d03bc-253">Certificate</span></span></th>
<th><span data-ttu-id="d03bc-254">サブジェクト名/共通名</span><span class="sxs-lookup"><span data-stu-id="d03bc-254">Subject name/ Common name</span></span></th>
<th><span data-ttu-id="d03bc-255">サブジェクトの別名</span><span class="sxs-lookup"><span data-stu-id="d03bc-255">Subject alternative name</span></span></th>
<th><span data-ttu-id="d03bc-256">例</span><span class="sxs-lookup"><span data-stu-id="d03bc-256">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d03bc-257">Default</span><span class="sxs-lookup"><span data-stu-id="d03bc-257">Default</span></span></p></td>
<td><p><span data-ttu-id="d03bc-258">アプライアンスの FQDN</span><span class="sxs-lookup"><span data-stu-id="d03bc-258">FQDN of the appliance</span></span></p></td>
<td><p><span data-ttu-id="d03bc-259">SIP。 &lt;sipdomain &gt; (SIP ドメインごとに1つのエントリが必要)</span><span class="sxs-lookup"><span data-stu-id="d03bc-259">SIP.&lt;sipdomain&gt; (need one entry per SIP domain)</span></span></p></td>
<td><p><span data-ttu-id="d03bc-260">SN=sba01.contoso.net; SAN=sip.contoso.com; SAN=sip.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="d03bc-260">SN=sba01.contoso.net; SAN=sip.contoso.com; SAN=sip.fabrikam.com</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="d03bc-261">関連項目</span><span class="sxs-lookup"><span data-stu-id="d03bc-261">See Also</span></span>


[<span data-ttu-id="d03bc-262">Lync Server 2013 のワイルドカード証明書のサポート</span><span class="sxs-lookup"><span data-stu-id="d03bc-262">Wildcard certificate support in Lync Server 2013</span></span>](lync-server-2013-wildcard-certificate-support.md)  
  

<span data-ttu-id="d03bc-263"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d03bc-263"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

