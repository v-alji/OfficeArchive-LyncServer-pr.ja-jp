---
title: 'Lync Server 2013: モバイルクライアントの展開プロセス'
description: 'Lync Server 2013: モバイルクライアント展開プロセス。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Mobile client deployment process
ms:assetid: 6498235b-2fa9-421d-bfa0-0ccc09508dbd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690982(v=OCS.15)
ms:contentKeyID: 51541484
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4fa4e9e1d272915e06009df5c06480309ce104e0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425564"
---
# <a name="mobile-client-deployment-process-in-lync-server-2013"></a><span data-ttu-id="a86b4-103">Lync Server 2013 でのモバイルクライアントの展開プロセス</span><span class="sxs-lookup"><span data-stu-id="a86b4-103">Mobile client deployment process in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a86b4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a86b4-104">

<span> </span></span></span>

<span data-ttu-id="a86b4-105">_**トピックの最終更新日:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="a86b4-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="a86b4-106">Microsoft Lync Server 2013 の展開が完了したら、ユーザーは、特定のデバイスで使い慣れたモバイル市場から Lync 2013 アプリをインストールできます。</span><span class="sxs-lookup"><span data-stu-id="a86b4-106">After a deployment of Microsoft Lync Server 2013 has been completed, users can install the Lync 2013 app from the mobile marketplace that they are accustomed to using for their specific device.</span></span>

<div>

## <a name="lync-mobile-deployment-process"></a><span data-ttu-id="a86b4-107">Lync モバイル展開プロセス</span><span class="sxs-lookup"><span data-stu-id="a86b4-107">Lync Mobile Deployment Process</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a86b4-108">段階</span><span class="sxs-lookup"><span data-stu-id="a86b4-108">Phase</span></span></th>
<th><span data-ttu-id="a86b4-109">ステップ</span><span class="sxs-lookup"><span data-stu-id="a86b4-109">Steps</span></span></th>
<th><span data-ttu-id="a86b4-110">アクセス許可</span><span class="sxs-lookup"><span data-stu-id="a86b4-110">Permissions</span></span></th>
<th><span data-ttu-id="a86b4-111">ドキュメント</span><span class="sxs-lookup"><span data-stu-id="a86b4-111">Documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a86b4-112">セットアップ前のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="a86b4-112">Perform pre-setup tasks.</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="a86b4-113">Lync Server 2013 の展開を確認します。</span><span class="sxs-lookup"><span data-stu-id="a86b4-113">Verify Lync Server 2013 deployment.</span></span></p></li>
<li><p><span data-ttu-id="a86b4-114">証明書の要件を確認します。</span><span class="sxs-lookup"><span data-stu-id="a86b4-114">Verify certificate requirements.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="a86b4-115">Administrator</span><span class="sxs-lookup"><span data-stu-id="a86b4-115">Administrator</span></span></p></td>
<td><p><span data-ttu-id="a86b4-116">サーバー計画ドキュメントの<a href="lync-server-2013-planning-for-mobility.md">Lync server 2013 でのモビリティの計画</a>。</span><span class="sxs-lookup"><span data-stu-id="a86b4-116"><a href="lync-server-2013-planning-for-mobility.md">Planning for mobility in Lync Server 2013</a> in the server planning documentation.</span></span></p>
<p><span data-ttu-id="a86b4-117">サーバー展開ドキュメントの<a href="lync-server-2013-deploying-mobility.md">Lync server 2013</a>へのモビリティの展開。</span><span class="sxs-lookup"><span data-stu-id="a86b4-117"><a href="lync-server-2013-deploying-mobility.md">Deploying mobility in Lync Server 2013</a> in the server deployment documentation.</span></span></p>
<p><span data-ttu-id="a86b4-118">サーバー計画ドキュメントの<a href="lync-server-2013-certificate-infrastructure-requirements.md">Lync server 2013 の証明書インフラストラクチャの要件</a>。</span><span class="sxs-lookup"><span data-stu-id="a86b4-118"><a href="lync-server-2013-certificate-infrastructure-requirements.md">Certificate infrastructure requirements for Lync Server 2013</a> in the server planning documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a86b4-119">Lync アプリケーションをテストデバイスにインストールします。</span><span class="sxs-lookup"><span data-stu-id="a86b4-119">Install the Lync application on a test device.</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="a86b4-120">前提条件をインストールします。</span><span class="sxs-lookup"><span data-stu-id="a86b4-120">Install prerequisites.</span></span></p></li>
<li><p><span data-ttu-id="a86b4-121">モバイルデバイスに固有の marketplace からインストールします。</span><span class="sxs-lookup"><span data-stu-id="a86b4-121">Install from the marketplace specific to the mobile device.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="a86b4-122">Administrator</span><span class="sxs-lookup"><span data-stu-id="a86b4-122">Administrator</span></span></p></td>
<td><p><span data-ttu-id="a86b4-123"><a href="lync-server-2013-deploying-mobile-clients.md">Lync Server 2013 でモバイルクライアントを展開</a>するときのモバイルデバイス固有のインストール手順。</span><span class="sxs-lookup"><span data-stu-id="a86b4-123">Installation instructions specific to the mobile device in <a href="lync-server-2013-deploying-mobile-clients.md">Deploying mobile clients in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a86b4-124">クライアントを構成します。</span><span class="sxs-lookup"><span data-stu-id="a86b4-124">Configure the client.</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="a86b4-125">サインインの設定とサーバー情報を構成します。</span><span class="sxs-lookup"><span data-stu-id="a86b4-125">Configure sign-in settings and server information.</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="a86b4-126">Administrator</span><span class="sxs-lookup"><span data-stu-id="a86b4-126">Administrator</span></span></p></td>
<td><p><span data-ttu-id="a86b4-127"><a href="lync-server-2013-deploying-mobile-clients.md">Lync Server 2013 でモバイルクライアントを展開する</a></span><span class="sxs-lookup"><span data-stu-id="a86b4-127"><a href="lync-server-2013-deploying-mobile-clients.md">Deploying mobile clients in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a86b4-128">モバイルシナリオをテストする。</span><span class="sxs-lookup"><span data-stu-id="a86b4-128">Test mobile scenarios.</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="a86b4-129">インスタントメッセージング (IM) とプレゼンスをテストします。</span><span class="sxs-lookup"><span data-stu-id="a86b4-129">Test instant messaging (IM) and presence.</span></span></p></li>
<li><p><span data-ttu-id="a86b4-130">ダイヤルアウト会議をテストします。</span><span class="sxs-lookup"><span data-stu-id="a86b4-130">Test dial-out conferencing.</span></span></p></li>
<li><p><span data-ttu-id="a86b4-131">会社のディレクトリで連絡先を検索します。</span><span class="sxs-lookup"><span data-stu-id="a86b4-131">Search for a contact in the corporate directory.</span></span></p></li>
<li><p><span data-ttu-id="a86b4-132">プッシュ通知をテストします。</span><span class="sxs-lookup"><span data-stu-id="a86b4-132">Test push notifications.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="a86b4-133">Administrator</span><span class="sxs-lookup"><span data-stu-id="a86b4-133">Administrator</span></span></p></td>
<td><p><span data-ttu-id="a86b4-134"><a href="lync-server-2013-deploying-mobile-clients.md">Lync Server 2013 でモバイルクライアントを展開</a>するときのモバイルデバイス固有の確認手順。</span><span class="sxs-lookup"><span data-stu-id="a86b4-134">Verification instructions specific to the mobile device in <a href="lync-server-2013-deploying-mobile-clients.md">Deploying mobile clients in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a86b4-135">Lync アプリケーションを携帯電話にインストールします。</span><span class="sxs-lookup"><span data-stu-id="a86b4-135">Install the Lync application on mobile phones.</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="a86b4-136">前提条件をインストールします。</span><span class="sxs-lookup"><span data-stu-id="a86b4-136">Install prerequisites.</span></span></p></li>
<li><p><span data-ttu-id="a86b4-137">モバイルデバイスに固有の marketplace からインストールします。</span><span class="sxs-lookup"><span data-stu-id="a86b4-137">Install from the marketplace specific to the mobile device.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="a86b4-138">ユーザー</span><span class="sxs-lookup"><span data-stu-id="a86b4-138">User</span></span></p></td>
<td><p><span data-ttu-id="a86b4-139"><a href="lync-server-2013-deploying-mobile-clients.md">Lync Server 2013 でモバイルクライアントを展開</a>するときのモバイルデバイス固有のインストール手順。</span><span class="sxs-lookup"><span data-stu-id="a86b4-139">Installation instructions specific to the mobile device in <a href="lync-server-2013-deploying-mobile-clients.md">Deploying mobile clients in Lync Server 2013</a>.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a86b4-140">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a86b4-140">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

