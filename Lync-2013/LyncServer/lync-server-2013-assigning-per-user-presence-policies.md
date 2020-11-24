---
title: 'Lync Server 2013: ユーザーごとのプレゼンスポリシーの割り当て'
description: 'Lync Server 2013: ユーザーごとのプレゼンスポリシーを割り当てます。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assigning per-user presence policies
ms:assetid: fd1097b7-248d-4b78-8c43-456b03257c18
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182614(v=OCS.15)
ms:contentKeyID: 48185955
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5c3d4b4bda0c4bb85065d546fdbb4b2578db0e3f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399974"
---
# <a name="assigning-per-user-presence-policies-in-lync-server-2013"></a><span data-ttu-id="45ca6-103">Lync Server 2013 でのユーザーごとのプレゼンスポリシーの割り当て</span><span class="sxs-lookup"><span data-stu-id="45ca6-103">Assigning per-user presence policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="45ca6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="45ca6-104">

<span> </span></span></span>

<span data-ttu-id="45ca6-105">_**最終更新日:** 2012-10-11_</span><span class="sxs-lookup"><span data-stu-id="45ca6-105">_**Topic Last Modified:** 2012-10-11_</span></span>

<span data-ttu-id="45ca6-106">プレゼンスポリシーは、プレゼンスに影響する制限と制限のセットです。</span><span class="sxs-lookup"><span data-stu-id="45ca6-106">A presence policy is a set of limits and restrictions that affect presence.</span></span> <span data-ttu-id="45ca6-107">次の表では、Lync Server 2013 で使用できるプレゼンスポリシーの設定について説明します。</span><span class="sxs-lookup"><span data-stu-id="45ca6-107">The following table describes the presence policy settings available in Lync Server 2013.</span></span>

### <a name="presence-policy-settings"></a><span data-ttu-id="45ca6-108">プレゼンスポリシーの設定</span><span class="sxs-lookup"><span data-stu-id="45ca6-108">Presence Policy Settings</span></span>

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
<th><span data-ttu-id="45ca6-109">XML 名</span><span class="sxs-lookup"><span data-stu-id="45ca6-109">XML name</span></span></th>
<th><span data-ttu-id="45ca6-110">表示名</span><span class="sxs-lookup"><span data-stu-id="45ca6-110">Display name</span></span></th>
<th><span data-ttu-id="45ca6-111">説明</span><span class="sxs-lookup"><span data-stu-id="45ca6-111">Description</span></span></th>
<th><span data-ttu-id="45ca6-112">型</span><span class="sxs-lookup"><span data-stu-id="45ca6-112">Type</span></span></th>
<th><span data-ttu-id="45ca6-113">値</span><span class="sxs-lookup"><span data-stu-id="45ca6-113">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45ca6-114">カテゴリのサブスクリプション</span><span class="sxs-lookup"><span data-stu-id="45ca6-114">CategorySubscriptions</span></span></p></td>
<td><p><span data-ttu-id="45ca6-115">サブスクライバーカテゴリのサブスクリプションの最大数</span><span class="sxs-lookup"><span data-stu-id="45ca6-115">Maximum Number of Subscriber Category Subscriptions</span></span></p></td>
<td><p><span data-ttu-id="45ca6-116">サブスクライバーカテゴリのサブスクリプションの数を制限します。</span><span class="sxs-lookup"><span data-stu-id="45ca6-116">Limits the number of subscriber category subscriptions.</span></span> <span data-ttu-id="45ca6-117">たとえば、ユーザーのプレゼンスをサブスクライブしている場合は、連絡先カード、予定表データ、メモ、サービス、状態カテゴリごとに、カテゴリサブスクリプションが取得されます。</span><span class="sxs-lookup"><span data-stu-id="45ca6-117">For example, when Communicator subscribes to a user’s presence, it obtains a category subscription for each of the contact card, calendar data, notes, services, and state categories.</span></span></p>
<p><span data-ttu-id="45ca6-118">0に設定すると、ユーザーまたは連絡先オブジェクトは、他のユーザーが購読できないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="45ca6-118">A setting of 0 means that the user or contact object cannot be subscribed to by others.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="45ca6-119">この設定は、高い数値に設定されている場合に、パフォーマンスに大きな影響を与える可能性があります。また、平均的なユーザーが多数のユーザーに対して自分のプレゼンスをサブスクライブしている場合があります。</span><span class="sxs-lookup"><span data-stu-id="45ca6-119">This setting can have a significant impact on performance if it is set to a high number, and the average user has a large number of users subscribing to his or her presence.</span></span>


</div></td>
<td><p><span data-ttu-id="45ca6-120">整数型</span><span class="sxs-lookup"><span data-stu-id="45ca6-120">Integer</span></span></p></td>
<td><p><span data-ttu-id="45ca6-121">0-3000</span><span class="sxs-lookup"><span data-stu-id="45ca6-121">0-3000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45ca6-122">PromptedSubscribers</span><span class="sxs-lookup"><span data-stu-id="45ca6-122">PromptedSubscribers</span></span></p></td>
<td><p><span data-ttu-id="45ca6-123">キューに登録されているプレゼンス情報の通知の最大数</span><span class="sxs-lookup"><span data-stu-id="45ca6-123">Maximum Number of Queued Presence Subscription Alerts</span></span></p></td>
<td><p><span data-ttu-id="45ca6-124">プロンプトを表示するサブスクライバーテーブルのエントリ数を制限します。</span><span class="sxs-lookup"><span data-stu-id="45ca6-124">Limits the number of entries in the prompted subscribers table.</span></span> <span data-ttu-id="45ca6-125">この設定では、特定のユーザーに対してキューに入れることができるプロンプトの最大数を決定します。</span><span class="sxs-lookup"><span data-stu-id="45ca6-125">This setting determines the maximum number of prompts that can be queued for a given user.</span></span> <span data-ttu-id="45ca6-126">たとえば、ユーザー A がユーザー B のプレゼンスをサブスクライブしている場合、ユーザー B はユーザー A がユーザー B に登録されていることを知らせるメッセージを受け取り、ユーザー b の [プロンプトを表示するサブスクライバー] テーブルに確認メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="45ca6-126">For example, when user A subscribes to user B’s presence, user B receives a prompt that user A is now subscribed to user B, and an acknowledgement prompt is created in user B’s prompted subscribers table.</span></span> <span data-ttu-id="45ca6-127">ユーザー B がサブスクリプションを承認するか、承認すると、確認メッセージがユーザー B のプロンプトのサブスクライバーテーブルから削除されます。</span><span class="sxs-lookup"><span data-stu-id="45ca6-127">After user B accepts, or acknowledges, the subscription, the acknowledgement prompt is removed from user B’s prompted subscribers table.</span></span></p>
<p><span data-ttu-id="45ca6-128">0に設定すると、他のユーザーが自分のプレゼンスをサブスクライブしているときに、ユーザーにメッセージが表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="45ca6-128">A setting of 0 means that the user is not prompted when someone subscribes to his or her presence.</span></span></p></td>
<td><p><span data-ttu-id="45ca6-129">Integer または Token</span><span class="sxs-lookup"><span data-stu-id="45ca6-129">Integer or Token</span></span></p></td>
<td><p><span data-ttu-id="45ca6-130">0-500</span><span class="sxs-lookup"><span data-stu-id="45ca6-130">0-500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="45ca6-131">既定では、Lync Server を展開すると、既定の **ポリシー** と **サービス: Medium** プレゼンスポリシーがインストールされます。</span><span class="sxs-lookup"><span data-stu-id="45ca6-131">By default, the **Default Policy** and **Service: Medium** presence policies are installed when you deploy Lync Server.</span></span> <span data-ttu-id="45ca6-132">次の表では、2つのプレゼンスポリシーの固有の設定について説明します。</span><span class="sxs-lookup"><span data-stu-id="45ca6-132">The following table describes the specific settings of the two presence policies.</span></span>

### <a name="presence-policies"></a><span data-ttu-id="45ca6-133">プレゼンスポリシー</span><span class="sxs-lookup"><span data-stu-id="45ca6-133">Presence Policies</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="45ca6-134">ポリシー名</span><span class="sxs-lookup"><span data-stu-id="45ca6-134">Policy name</span></span></th>
<th><span data-ttu-id="45ca6-135">説明</span><span class="sxs-lookup"><span data-stu-id="45ca6-135">Description</span></span></th>
<th><span data-ttu-id="45ca6-136">カテゴリのサブスクリプション</span><span class="sxs-lookup"><span data-stu-id="45ca6-136">CategorySubscriptions</span></span></th>
<th><span data-ttu-id="45ca6-137">PromptedSubscribers</span><span class="sxs-lookup"><span data-stu-id="45ca6-137">PromptedSubscribers</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45ca6-138">既定のポリシー</span><span class="sxs-lookup"><span data-stu-id="45ca6-138">Default Policy</span></span></p></td>
<td><p><span data-ttu-id="45ca6-139">一般的なユーザー向けのポリシー。</span><span class="sxs-lookup"><span data-stu-id="45ca6-139">Policy for typical users.</span></span> <span data-ttu-id="45ca6-140">これは既定のプレゼンスポリシーです。</span><span class="sxs-lookup"><span data-stu-id="45ca6-140">This is the default presence policy.</span></span></p></td>
<td><p><span data-ttu-id="45ca6-141">1000</span><span class="sxs-lookup"><span data-stu-id="45ca6-141">1000</span></span></p></td>
<td><p><span data-ttu-id="45ca6-142">200</span><span class="sxs-lookup"><span data-stu-id="45ca6-142">200</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45ca6-143">サービス: 媒体</span><span class="sxs-lookup"><span data-stu-id="45ca6-143">Service: Medium</span></span></p></td>
<td><p><span data-ttu-id="45ca6-144">他のユーザーがオブジェクトのプレゼンスをサブスクライブする必要があるアプリケーションのポリシー。</span><span class="sxs-lookup"><span data-stu-id="45ca6-144">Policy for applications that require more users to subscribe to the object’s presence.</span></span></p></td>
<td><p><span data-ttu-id="45ca6-145">1000</span><span class="sxs-lookup"><span data-stu-id="45ca6-145">1000</span></span></p></td>
<td><p><span data-ttu-id="45ca6-146">0</span><span class="sxs-lookup"><span data-stu-id="45ca6-146">0</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="45ca6-147">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="45ca6-147">


</div>

<span> </span>

</div>

</div>

</span></span></div>

