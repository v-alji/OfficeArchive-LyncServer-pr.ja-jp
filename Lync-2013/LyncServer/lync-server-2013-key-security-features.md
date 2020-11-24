---
title: 'Lync Server 2013: セキュリティの主要機能'
description: 'Lync Server 2013: 主なセキュリティ機能'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Key security features in Lync Server 2013
ms:assetid: bf2a3b8f-73c6-47e1-8c9e-ca1dc1a502bf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn342829(v=OCS.15)
ms:contentKeyID: 56107266
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 689cf2ac54eacd24bb4d31b451836edcf676521b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398750"
---
# <a name="key-security-features-in-lync-server-2013"></a><span data-ttu-id="b7460-103">Lync Server 2013 の主要なセキュリティ機能</span><span class="sxs-lookup"><span data-stu-id="b7460-103">Key security features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b7460-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b7460-104">

<span> </span></span></span>

<span data-ttu-id="b7460-105">_**最終更新日:** 2013-07-18_</span><span class="sxs-lookup"><span data-stu-id="b7460-105">_**Topic Last Modified:** 2013-07-18_</span></span>

<span data-ttu-id="b7460-106">Lync Server 2013 には、サーバー間認証、役割ベースのアクセス制御、構成データの一元ストレージなど、いくつかのセキュリティ機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b7460-106">Lync Server 2013 includes several security features, including server-to-server authentication, role-based access control, and centralized storage of configuration data.</span></span>

<span data-ttu-id="b7460-107">この記事では、Lync Server 2013 セキュリティの概要について説明します。</span><span class="sxs-lookup"><span data-stu-id="b7460-107">This article provides a high level overview of Lync Server 2013 security.</span></span>

<div>

## <a name="key-security-features-in-lync-server-2013"></a><span data-ttu-id="b7460-108">Lync Server 2013 の主要なセキュリティ機能</span><span class="sxs-lookup"><span data-stu-id="b7460-108">Key Security Features in Lync Server 2013</span></span>

<span data-ttu-id="b7460-109">セキュリティは非常に広い範囲に及ぶトピックです。</span><span class="sxs-lookup"><span data-stu-id="b7460-109">Security is a very broad topic.</span></span> <span data-ttu-id="b7460-110">Lync Server 2013 のすべての機能、および Lync エコシステムを構成するデータベース、サービス、ハードウェアにセキュリティが設定されます。</span><span class="sxs-lookup"><span data-stu-id="b7460-110">Security reaches across every feature of Lync Server 2013 as well as databases, services, and hardware that make up a Lync ecosystem.</span></span> <span data-ttu-id="b7460-111">この記事では、特にセキュリティのために設計された Lync Server 2013 の一部の機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="b7460-111">This article outlines some of the features in Lync Server 2013 in particular that are designed for security.</span></span>

<div>

## <a name="planning-and-design-tools"></a><span data-ttu-id="b7460-112">計画ツールと設計ツール</span><span class="sxs-lookup"><span data-stu-id="b7460-112">Planning and Design Tools</span></span>

<span data-ttu-id="b7460-113">Lync Server 2013 には、計画と設計を容易にするためのツールが2つ用意されています。 Lync Server コンポーネントの構成が間違っている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b7460-113">Lync Server 2013 provides two tools to facilitate planning and design and to reduce the chance of misconfiguring Lync Server components.</span></span>

  - <span data-ttu-id="b7460-114">**トポロジ計画ツール** は、トポロジ設計プロセスの大部分を自動化します。</span><span class="sxs-lookup"><span data-stu-id="b7460-114">**Topology Planning Tool** automates much of the topology design process.</span></span> <span data-ttu-id="b7460-115">計画ツールからトポロジビルダーに結果をエクスポートすることができます。これは、Lync Server 2013 を実行している各サーバーをインストールするために必要なツールです。</span><span class="sxs-lookup"><span data-stu-id="b7460-115">You can export the results from the Planning Tool to Topology Builder, which is the tool that is required to install each server running Lync Server 2013.</span></span>

  - <span data-ttu-id="b7460-116">**トポロジ ビルダー** は、すべての構成情報を中央管理ストアに格納します。</span><span class="sxs-lookup"><span data-stu-id="b7460-116">**Topology Builder** stores all configuration information in the Central Management store.</span></span>

<span data-ttu-id="b7460-117">これらのツールについて詳しくは、「 [Lync Server 2013 の計画](lync-server-2013-planning.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="b7460-117">For details about these tools, see [Planning for Lync Server 2013](lync-server-2013-planning.md).</span></span>

</div>

<div>

## <a name="central-management-store"></a><span data-ttu-id="b7460-118">中央管理ストア</span><span class="sxs-lookup"><span data-stu-id="b7460-118">Central Management Store</span></span>

<span data-ttu-id="b7460-119">Lync Server 2013 では、サーバーとサービスに関する構成データは中央管理ストアに含まれています。</span><span class="sxs-lookup"><span data-stu-id="b7460-119">In Lync Server 2013, configuration data about servers and services is part of the Central Management store.</span></span> <span data-ttu-id="b7460-120">中央管理ストアでは、Lync Server の展開を定義、セットアップ、管理、管理、説明、操作するために必要なデータを schematized に保存します。</span><span class="sxs-lookup"><span data-stu-id="b7460-120">The Central Management store provides a robust, schematized storage of the data needed to define, set up, maintain, administer, describe, and operate a Lync Server deployment.</span></span> <span data-ttu-id="b7460-121">また、データを検証して構成の一貫性を保ちます。</span><span class="sxs-lookup"><span data-stu-id="b7460-121">It also validates the data to ensure configuration consistency.</span></span> <span data-ttu-id="b7460-122">構成データへの変更はすべて中央管理ストアでなされるので、"非同期" の問題を回避できます。</span><span class="sxs-lookup"><span data-stu-id="b7460-122">All changes to this configuration data happen at the Central Management store, eliminating “out-of-sync” issues.</span></span>

<span data-ttu-id="b7460-p104">データの読み取り専用コピーは、エッジ サーバーや存続可能ブランチ アプライアンスなど、トポロジ内のすべてのサーバーにレプリケートされます。レプリケーションは、既定では、ネットワーク サービスのコンテキストで実行されるサービスが管理し、権限とアクセス許可が抑えられてコンピューター上の一般ユーザーと同じになります。</span><span class="sxs-lookup"><span data-stu-id="b7460-p104">Read-only copies of the data are replicated to all servers in the topology, including Edge Servers and Survivable Branch Appliances. Replication is managed by a service that is, by default, run under the context of the Network service, reducing the rights and permissions to that of a simple user on the computer.</span></span>

</div>

<div>

## <a name="server-to-server-authentication"></a><span data-ttu-id="b7460-125">サーバー間認証</span><span class="sxs-lookup"><span data-stu-id="b7460-125">Server-to-Server Authentication</span></span>

<span data-ttu-id="b7460-126">Lync Server 2013 では、Open Authorization (OAuth) プロトコルを使用してサーバー間で認証を構成することができます。</span><span class="sxs-lookup"><span data-stu-id="b7460-126">In Lync Server 2013, authentication can be configured between servers by using the Open Authorization (OAuth) protocol.</span></span> <span data-ttu-id="b7460-127">たとえば、Exchange Server 2013 を実行しているサーバーに対して認証するように Lync Server 2013 を構成することができます。</span><span class="sxs-lookup"><span data-stu-id="b7460-127">For example, you can configure Lync Server 2013 to authenticate with a server that is running Exchange Server 2013.</span></span> <span data-ttu-id="b7460-128">OAuth プロトコルを使用すると、Lync server と Exchange server が相互に信頼することができます。</span><span class="sxs-lookup"><span data-stu-id="b7460-128">Using the OAuth protocol, the Lync server and the Exchange server can trust each other.</span></span> <span data-ttu-id="b7460-129">これにより、製品をシームレスな方法で統合することができます。</span><span class="sxs-lookup"><span data-stu-id="b7460-129">This provides the ability to integrate the products in a seamless manner.</span></span> <span data-ttu-id="b7460-130">詳細については、「 [Lync server 2013 でサーバー間認証 (OAuth) とパートナーアプリケーションを管理する](lync-server-2013-managing-server-to-server-authentication-oauth-and-partner-applications.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b7460-130">For details, see [Managing server-to-server authentication (OAuth) and partner applications in Lync Server 2013](lync-server-2013-managing-server-to-server-authentication-oauth-and-partner-applications.md)</span></span>

</div>

<div>

## <a name="windows-powershell-based-management-and-web-based-management-interface"></a><span data-ttu-id="b7460-131">Windows PowerShell ベースの管理と Web ベースの管理インターフェイス</span><span class="sxs-lookup"><span data-stu-id="b7460-131">Windows PowerShell-based management and Web-based Management Interface</span></span>

<span data-ttu-id="b7460-132">Lync Server 2013 は、Windows PowerShell コマンドラインインターフェイスに基づいて構築された強力な管理インターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="b7460-132">Lync Server 2013 provides a powerful management interface, built on the Windows PowerShell command-line interface.</span></span> <span data-ttu-id="b7460-133">このインターフェイスにはセキュリティを管理するためのコマンドレットが含まれているうえ、Windows PowerShell のセキュリティ機能が既定で有効になっており、ユーザーが簡単にまたは知らないうちにスクリプトを実行することができないようになっています。</span><span class="sxs-lookup"><span data-stu-id="b7460-133">It includes cmdlets for managing security, and Windows PowerShell security features are enabled by default so that users cannot easily or unknowingly run scripts.</span></span> <span data-ttu-id="b7460-134">つまり、セキュリティを最大限に高め、攻撃の手段を減らすように、ソフトウェアの既定値が自動的に設定されています。</span><span class="sxs-lookup"><span data-stu-id="b7460-134">This means that the software defaults are set to automatically help maximize security and reduce the avenues of attack.</span></span> <span data-ttu-id="b7460-135">Lync Server 2013 での Windows PowerShell 管理のサポートについて詳しくは、「 [Lync server 2013 管理シェル](lync-server-2013-lync-server-management-shell.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="b7460-135">For details about Windows PowerShell management support in Lync Server 2013, see [Lync Server 2013 Management Shell](lync-server-2013-lync-server-management-shell.md).</span></span>

</div>

<div>

## <a name="role-based-access-control-rbac"></a><span data-ttu-id="b7460-136">役割ベースのアクセス制御 (RBAC)</span><span class="sxs-lookup"><span data-stu-id="b7460-136">Role-Based Access Control (RBAC)</span></span>

<span data-ttu-id="b7460-137">Microsoft Lync Server 2013 では、役割ベースのアクセス制御 (RBAC) を利用して、セキュリティの高い標準を維持しながら管理タスクを委任できます。</span><span class="sxs-lookup"><span data-stu-id="b7460-137">Microsoft Lync Server 2013 provides role-based access control (RBAC) to enable you to delegate administrative tasks while maintaining high standards for security.</span></span> <span data-ttu-id="b7460-138">そのため、業務上必要な管理権限のみをユーザーに与える "最小限の特権" の原則に従って RBAC を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="b7460-138">You can use RBAC to follow the principle of "least privilege," in which users are given only the administrative rights that their jobs require.</span></span> <span data-ttu-id="b7460-139">Lync Server 2013 には、新しい役割を作成したり、既存の役割を変更したりする機能が導入されています。</span><span class="sxs-lookup"><span data-stu-id="b7460-139">Lync Server 2013 introduces the ability to create a new role and also the ability to modify an existing role.</span></span> <span data-ttu-id="b7460-140">詳細については、「 [Lync Server 2013 での役割ベースのアクセス制御の計画](lync-server-2013-planning-for-role-based-access-control.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b7460-140">For details, see [Planning for role-based access control in Lync Server 2013](lync-server-2013-planning-for-role-based-access-control.md).</span></span>

</div>

</div>

<div>

## <a name="network-address-translation-nat"></a><span data-ttu-id="b7460-141">ネットワーク アドレス変換 (NAT)</span><span class="sxs-lookup"><span data-stu-id="b7460-141">Network Address Translation (NAT)</span></span>

<span data-ttu-id="b7460-142">Lync Server 2013 は、エッジサーバーの内部インターフェイスでのネットワークアドレス変換 (NAT) の使用をサポートしていませんが、統合されたエッジサーバートポロジの1つとスケーリングの両方について、ネットワークアドレス変換 (NAT) を実行するルーターまたはファイアウォールでの外部インターフェイスの配置をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="b7460-142">Lync Server 2013 does not support the use of network address translation (NAT) on the internal interface of the Edge Server, but it does support placing the external interface of the Access Edge service, Web Conferencing Edge service, and A/V Edge service behind a router or firewall that performs network address translation (NAT) for both single and scaled consolidated Edge Server topologies.</span></span> <span data-ttu-id="b7460-143">ハードウェア ロード バランサーの背後にある複数のエッジ サーバーでは、NAT を使用できません。</span><span class="sxs-lookup"><span data-stu-id="b7460-143">Multiple Edge Servers behind a hardware load balancer cannot use NAT.</span></span> <span data-ttu-id="b7460-144">複数のエッジ サーバーの外部インターフェイスで NAT を使用する場合は、ドメイン ネーム システム (DNS) の負荷分散が必要です。</span><span class="sxs-lookup"><span data-stu-id="b7460-144">If multiple Edge Servers use NAT on their external interfaces, Domain Name System (DNS) load balancing is required.</span></span> <span data-ttu-id="b7460-145">DNS 負荷分散を使用すると、エッジ サーバー プール内のエッジ サーバーあたりのパブリック IP アドレスの数を削減できます。</span><span class="sxs-lookup"><span data-stu-id="b7460-145">In turn, using DNS load balancing allows you to reduce the number of public IP addresses per Edge Server in an Edge Server pool.</span></span> <span data-ttu-id="b7460-146">詳細については、「[Lync Server 2013 での外部ユーザーアクセスの計画](lync-server-2013-planning-for-external-user-access.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b7460-146">For details, see[Planning for external user access in Lync Server 2013](lync-server-2013-planning-for-external-user-access.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b7460-147">Microsoft Office Communications Server 2007 が展開されているエンタープライズとフェデレーションを行うときに、使用しているエンタープライズとフェデレーション先のエンタープライズとの間で音声ビデオを使用する必要がある場合、ポート要件は、展開されているエッジ サーバーのうち、古い方のバージョン用の要件になります。</span><span class="sxs-lookup"><span data-stu-id="b7460-147">If you federate with enterprises that have a Microsoft Office Communications Server 2007 deployment and you need to use audio/video between your enterprise and the federated enterprise, the port requirements will be those for the older version of the Edge Servers that are deployed.</span></span> <span data-ttu-id="b7460-148">たとえば、これらの古いバージョンに必要なポート範囲は、フェデレーションパートナーがそのエッジサーバーを Lync Server 2013 にアップグレードするまで両方のエンタープライズで開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="b7460-148">For example, the port ranges required for those older versions must be opened for both enterprises until the federated partner upgrades its Edge Servers to Lync Server 2013.</span></span> <span data-ttu-id="b7460-149">アップグレード後には、ポート要件を見直して、新しい構成に応じて削減できます。</span><span class="sxs-lookup"><span data-stu-id="b7460-149">At that time, the port requirements can be reviewed and reduced according to the new configuration.</span></span>



</div>

</div>

<div>

## <a name="simplified-certificates-for-edge-servers"></a><span data-ttu-id="b7460-150">エッジ サーバーの簡単化された証明書</span><span class="sxs-lookup"><span data-stu-id="b7460-150">Simplified Certificates for Edge Servers</span></span>

<span data-ttu-id="b7460-151">展開ウィザードは、サブジェクト名 (SN) やサブジェクト代替名 (SAN) を自動的に読む込むことができるので、安全ではない可能性のある不要なエントリを含める危険性が減少します。</span><span class="sxs-lookup"><span data-stu-id="b7460-151">The Deployment Wizard can automatically populate subject names (SNs) and subject alternative names (SANs), reducing the possibility of including unnecessary and potentially unsecure entries.</span></span>

</div>

<div>

## <a name="trustworthy-computing-security-development-lifecycle-sdl"></a><span data-ttu-id="b7460-152">信頼できるコンピューティングのセキュリティ開発ライフサイクル (SDL)</span><span class="sxs-lookup"><span data-stu-id="b7460-152">Trustworthy Computing Security Development Lifecycle (SDL)</span></span>

<span data-ttu-id="b7460-153">Lync Server 2013 は、「」で説明されている Microsoft の信頼できるコンピューティングセキュリティ開発ライフサイクル (SDL) に準拠して設計および開発されてい <https://go.microsoft.com/fwlink/?linkid=68761> ます。</span><span class="sxs-lookup"><span data-stu-id="b7460-153">Lync Server 2013 is designed and developed in compliance with the Microsoft Trustworthy Computing Security Development Lifecycle (SDL), which is described at <https://go.microsoft.com/fwlink/?linkid=68761>.</span></span>

  - <span data-ttu-id="b7460-154">**信頼できる設計**   より安全なユニファイドコミュニケーションシステムを作成するための最初の手順は、脅威モデルを設計し、設計された各機能をテストすることでした。</span><span class="sxs-lookup"><span data-stu-id="b7460-154">**Trustworthy by Design**   The first step in creating a more secure unified communications system was to design threat models and test each feature as it was designed.</span></span> <span data-ttu-id="b7460-155">Microsoft では加えて、設計動作以外でのテストも実施して、予期しない製品動作から生じるセキュリティ脆弱性を探しています。</span><span class="sxs-lookup"><span data-stu-id="b7460-155">In addition, Microsoft performs testing outside of the designed behavior in order to find security vulnerabilities resulting from unexpected product behavior.</span></span> <span data-ttu-id="b7460-156">コーディング プロセスとコーディング手法には、セキュリティに関連する複数の改善点が組み込まれていました。</span><span class="sxs-lookup"><span data-stu-id="b7460-156">Multiple security-related improvements were built into the coding process and practices.</span></span> <span data-ttu-id="b7460-157">ビルド時に使われるツールは、製品にコードが最終的にチェックインされる前にバッファ オーバーランなどの潜在的なセキュリティ上の脅威を検出します。</span><span class="sxs-lookup"><span data-stu-id="b7460-157">Build-time tools detect buffer overruns and other potential security threats before the code is checked in to the final product.</span></span> <span data-ttu-id="b7460-158">もちろん、あらゆる未知のセキュリティの脅威を防ぐように設計することは不可能です。</span><span class="sxs-lookup"><span data-stu-id="b7460-158">Of course, it is impossible to design against all unknown security threats.</span></span> <span data-ttu-id="b7460-159">完全なセキュリティを保証できるシステムはありません。</span><span class="sxs-lookup"><span data-stu-id="b7460-159">No system can guarantee complete security.</span></span> <span data-ttu-id="b7460-160">ただし、製品開発では、開発者がセキュリティで保護された設計原則を採用しているため、Lync Server 2013 には、アーキテクチャの基礎として業界標準のセキュリティ技術が組み込まれています。</span><span class="sxs-lookup"><span data-stu-id="b7460-160">However, because product development embraced secure design principles from the start, Lync Server 2013 incorporates industry standard security technologies as a fundamental part of its architecture.</span></span>

  - <span data-ttu-id="b7460-161">**既定で信頼できる**   場合  既定では、Lync Server 2013 のネットワーク通信が暗号化されています。</span><span class="sxs-lookup"><span data-stu-id="b7460-161">**Trustworthy by Default**   By default, network communications in Lync Server 2013 are encrypted.</span></span> <span data-ttu-id="b7460-162">すべてのサーバーでは、証明書と Kerberos 認証、TLS、セキュア Real-Time トランスポートプロトコル (SRTP)、およびその他の業界標準の暗号化手法 (128 ビット Advanced Encryption Standard (AES) 暗号化など) が使用されているため、ネットワーク上で実質的にすべての Lync Server データが保護されます。</span><span class="sxs-lookup"><span data-stu-id="b7460-162">Because all servers use certificates and Kerberos authentication, TLS, Secure Real-Time Transport Protocol (SRTP), and other industry-standard encryption techniques, including 128-bit Advanced Encryption Standard (AES) encryption, virtually all Lync Server data is protected on the network.</span></span> <span data-ttu-id="b7460-163">さらに、役割ベースのアクセス制御によって、Lync Server 2013 を実行しているサーバーを展開して、各サーバーの役割がサービスのみを実行し、そのサービスに関連するアクセス許可のみをサーバーの役割に対して適切であるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="b7460-163">In addition, role-based access control makes it possible to deploy servers running Lync Server 2013 so that each server role runs only the services, and has only the permissions related to those services, that are appropriate for the server role.</span></span>

  - <span data-ttu-id="b7460-164">**展開により信頼できる**   すべての Lync Server 2013 ドキュメントにはベストプラクティスと推奨事項が含まれており、展開に最適なセキュリティレベルを決定して構成し、既定以外のオプションをアクティブ化する場合のセキュリティリスクを評価するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="b7460-164">**Trustworthy by Deployment**   All Lync Server 2013 documentation includes best practices and recommendations to help you determine and configure the optimal security levels for your deployment and assess the security risks of activating non-default options.</span></span>

<span data-ttu-id="b7460-165"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b7460-165"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

