---
title: 'Lync Server 2013: Lync Server ハイブリッド環境を準備および展開する手順'
description: 'Lync Server 2013: Lync Server ハイブリッド環境の準備と展開の手順を説明します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Steps to prepare and deploy Lync Server 2013 hybrid environment
ms:assetid: a50d4f7b-63f4-4663-af63-56ca87e4e3e7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205157(v=OCS.15)
ms:contentKeyID: 48185060
ms.date: 12/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ffb791a8a45b2220d8987c8d688f346447747c00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398127"
---
# <a name="steps-to-prepare-and-deploy-lync-server-2013-hybrid-environment"></a><span data-ttu-id="93793-103">Lync Server 2013 ハイブリッド環境を準備および展開する手順</span><span class="sxs-lookup"><span data-stu-id="93793-103">Steps to prepare and deploy Lync Server 2013 hybrid environment</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="93793-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="93793-104">

<span> </span></span></span>

<span data-ttu-id="93793-105">_**最終更新日:** 2016-12-08_</span><span class="sxs-lookup"><span data-stu-id="93793-105">_**Topic Last Modified:** 2016-12-08_</span></span>

<span data-ttu-id="93793-106">次の表に、Skype for Business Online と Microsoft Office 365 でのハイブリッド展開の環境を準備するために必要な手順を示します。</span><span class="sxs-lookup"><span data-stu-id="93793-106">The following table lists the steps required to prepare your environment for a hybrid deployment with Skype for Business Online and Microsoft Office 365.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93793-107">完了状態</span><span class="sxs-lookup"><span data-stu-id="93793-107">Completed?</span></span></th>
<th><span data-ttu-id="93793-108">ステップ</span><span class="sxs-lookup"><span data-stu-id="93793-108">Step</span></span></th>
<th><span data-ttu-id="93793-109">説明</span><span class="sxs-lookup"><span data-stu-id="93793-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="93793-110">Office 365 のテナントアカウントを作成して、Lync Online を有効にする</span><span class="sxs-lookup"><span data-stu-id="93793-110">Create a tenant account for Office 365 and enable Lync Online</span></span></p></td>
<td><p><span data-ttu-id="93793-111">Office <a href="https://go.microsoft.com/fwlink/p/?linkid=254980">365</a>での office 365 と Lync Online について説明します。</span><span class="sxs-lookup"><span data-stu-id="93793-111">Learn about Office 365 and Lync Online at <a href="https://go.microsoft.com/fwlink/p/?linkid=254980">Office 365</a>.</span></span></p>
<p><span data-ttu-id="93793-112">環境の Office 365 の準備が整っていることを確認するには、 <a href="https://go.microsoft.com/fwlink/p/?linkid=401408">システム要件</a>を参照してください。</span><span class="sxs-lookup"><span data-stu-id="93793-112">To make sure that your environment is ready for Office 365, see the <a href="https://go.microsoft.com/fwlink/p/?linkid=401408">System Requirements</a>.</span></span></p>
<p><span data-ttu-id="93793-113">Office 365 のセットアップの詳細については、「 <a href="https://go.microsoft.com/fwlink/p/?linkid=254982">office 365 の使用を開始</a> する」および「 <a href="https://go.microsoft.com/fwlink/p/?linkid=254979">office 365</a>をセットアップする」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="93793-113">For details about setting up Office 365, see <a href="https://go.microsoft.com/fwlink/p/?linkid=254982">Getting Started with Office 365</a> and <a href="https://go.microsoft.com/fwlink/p/?linkid=254979">Set Up Office 365</a>.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="93793-114">ドメインを追加して所有権を確認する</span><span class="sxs-lookup"><span data-stu-id="93793-114">Add your domain and verify ownership</span></span></p></td>
<td><p><span data-ttu-id="93793-115">ドメインは、「<em>バニティ ドメイン</em>」とも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="93793-115">Your domain is sometimes also referred to as your <em>vanity domain</em>.</span></span> <span data-ttu-id="93793-116">Office 365 組織にドメインを追加してから、Office 365 でドメインを検証するための手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="93793-116">You must add your domain to your Office 365 organization, and then follow the steps to validate the domain with Office 365.</span></span> <span data-ttu-id="93793-117">この検証は、ドメインの所有者が自分であることを確認するために必要な手順です。</span><span class="sxs-lookup"><span data-stu-id="93793-117">This is to confirm that you are the owner of the domain.</span></span></p>
<p><span data-ttu-id="93793-118">Office 365 組織にドメインを追加するには、「 <a href="https://go.microsoft.com/fwlink/p/?linkid=254983">office 365 にドメインを追加</a>する」に記載されている手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="93793-118">To add your domain to your Office 365 organization, follow the steps described at <a href="https://go.microsoft.com/fwlink/p/?linkid=254983">Add your domain to Office 365</a>.</span></span></p>
<p><span data-ttu-id="93793-119">「 &quot; Office 365 サービスの DNS レコードを編集する」など、トピックの各セクションのすべての手順を実行します。&quot;</span><span class="sxs-lookup"><span data-stu-id="93793-119">Complete all of the steps in each section in the topic, including &quot;Edit DNS records for your Office 365 services.&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="93793-120">環境の準備状況を確認する</span><span class="sxs-lookup"><span data-stu-id="93793-120">Verify environment readiness</span></span></p></td>
<td><p><span data-ttu-id="93793-121">Office 365 セットアップアシスタントを使用して、Office 365 を展開することができます。</span><span class="sxs-lookup"><span data-stu-id="93793-121">You can use the Office 365 Setup Assistant to help you deploy Office 365.</span></span> <span data-ttu-id="93793-122">詳細については、「 <a href="https://go.microsoft.com/fwlink/p/?linkid=254985">セットアップアシスタントを使用して Office 365 の準備を確認する」を</a>参照してください。</span><span class="sxs-lookup"><span data-stu-id="93793-122">For more information, see <a href="https://go.microsoft.com/fwlink/p/?linkid=254985">Use Setup Assistant to determine Office 365 readiness</a>.</span></span></p>
<p><span data-ttu-id="93793-123">このツールの使用と Office 365 の展開の詳細については、「 <a href="https://go.microsoft.com/fwlink/p/?linkid=257337">office 365 展開ガイド</a>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="93793-123">For details about using the tool and deploying Office 365, see <a href="https://go.microsoft.com/fwlink/p/?linkid=257337">Office 365 deployment guide</a>.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="93793-124">Active Directory の同期を準備する</span><span class="sxs-lookup"><span data-stu-id="93793-124">Prepare for Active Directory synchronization</span></span></p></td>
<td><p><span data-ttu-id="93793-125">Active Directory の同期によって、オンプレミスの Active Directory が Office 365 と継続的に同期されます。</span><span class="sxs-lookup"><span data-stu-id="93793-125">Active Directory synchronization keeps your on-premises Active Directory continuously synchronized with Office 365.</span></span> <span data-ttu-id="93793-126">これにより、各ユーザー アカウントおよびグループの同期バージョンを作成できるだけでなく、ローカルの Microsoft Exchange Server 環境から Microsoft Exchange Online へのグローバル アドレス一覧 (GAL) の同期を実行できるようになります。</span><span class="sxs-lookup"><span data-stu-id="93793-126">This lets you create synchronized versions of each user account and group, and also enables global address list (GAL) synchronization from your local Microsoft Exchange Server environment to Microsoft Exchange Online.</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="93793-127">ユーザーが Lync Online に移行されていない場合でも、組織内のすべての Lync ユーザーの AD アカウントを、オンプレミスとオンラインの Lync 展開の間で同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93793-127">You need to synchronize the AD accounts for all Lync users in your organization between your on-premises and online Lync deployments, even if users are not moved to Lync Online.</span></span> <span data-ttu-id="93793-128">すべてのユーザーを同期しない場合、組織のオンプレミス展開のユーザーとオンライン ユーザーとの間の通信が正常に動作しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="93793-128">If you do not synchronize all users, communication between on-premises and online users in your organization may not work as expected.</span></span>


</div>
<p><span data-ttu-id="93793-129">Active Directory 同期のために環境を準備するには、「 <a href="https://go.microsoft.com/fwlink/p/?linkid=254988">ディレクトリ同期のロードマップ</a>」で説明されている手順に従ってください。シングルサインオンの設定が含まれます。</span><span class="sxs-lookup"><span data-stu-id="93793-129">To prepare your environment for Active Directory synchronization, follow the steps described in <a href="https://go.microsoft.com/fwlink/p/?linkid=254988">Directory synchronization Roadmap</a>, including setting up single sign-on.</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="93793-130">Active Directory フェデレーションサービス (AD FS) 用の証明書を作成する</span><span class="sxs-lookup"><span data-stu-id="93793-130">Create certificates for Active Directory Federation Services (AD FS)</span></span></p></td>
<td><p><span data-ttu-id="93793-131">Office 365 との id フェデレーションに使用する証明書を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93793-131">You will need to create the certificates that are used for identity federation with Office 365.</span></span> <span data-ttu-id="93793-132">詳細については、「 <a href="https://go.microsoft.com/fwlink/p/?linkid=285376">チェックリスト: AD fs を使用してシングルサインオンを実装および管理する</a>」の「フェデレーションサーバー証明書の計画と展開」のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="93793-132">For more information, see the “Federation server certificates” section of the Plan for and deploy AD FS for use with single sign-on topic at <a href="https://go.microsoft.com/fwlink/p/?linkid=285376">Checklist: Use AD FS to implement and manage single sign-on</a>.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="93793-133">AD FS 用の証明書を割り当てる</span><span class="sxs-lookup"><span data-stu-id="93793-133">Assign certificates for AD FS</span></span></p></td>
<td><p><span data-ttu-id="93793-134">Office 365 との id フェデレーションで使用する証明書を作成したら、それをインストールして割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="93793-134">After you create the certificates that are used for identity federation with Office 365, you must install and assign them.</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="93793-135">パイロットユーザーを Skype for Business Online に移行する</span><span class="sxs-lookup"><span data-stu-id="93793-135">Move pilot users to Skype for Business Online</span></span></p></td>
<td><p><span data-ttu-id="93793-136">Skype for Business Online の環境を準備して構成するための手順を完了したら、パイロットユーザーを Lync Online に移行することができます。</span><span class="sxs-lookup"><span data-stu-id="93793-136">After you have completed the steps to prepare and configure your environment for Skype for Business Online, you can start moving pilot users to Lync Online.</span></span></p>
<p><span data-ttu-id="93793-137">「 <a href="lync-server-2013-move-users-to-lync-online.md">Lync Server 2013 でユーザーを Lync Online に移動する」を</a>参照してください。</span><span class="sxs-lookup"><span data-stu-id="93793-137">See <a href="lync-server-2013-move-users-to-lync-online.md">Move users to Lync Online in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="93793-138">ハイブリッド展開でユーザーを管理する</span><span class="sxs-lookup"><span data-stu-id="93793-138">Administering users in a hybrid deployment</span></span></p></td>
<td><p><span data-ttu-id="93793-139">ハイブリッド展開でユーザーを管理する方法の詳細については、「 <a href="lync-server-2013-administering-users-in-a-hybrid-deployment.md">ハイブリッド Lync Server 2013 展開でユーザーを管理</a>する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="93793-139">For details about how to administer users in a hybrid deployment, see <a href="lync-server-2013-administering-users-in-a-hybrid-deployment.md">Administering users in a hybrid Lync Server 2013 deployment</a>.</span></span></p></td>
</tr><span data-ttu-id="93793-140">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="93793-140">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

