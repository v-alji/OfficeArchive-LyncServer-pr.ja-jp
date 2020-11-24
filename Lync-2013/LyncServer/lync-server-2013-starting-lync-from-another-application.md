---
title: 'Lync Server 2013: 別のアプリケーションから Lync を起動する'
description: 'Lync Server 2013: 別のアプリケーションから Lync を起動しています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Starting Lync from another application
ms:assetid: 573b30b1-6590-4b24-8e96-a41be57cb0ef
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398376(v=OCS.15)
ms:contentKeyID: 48184184
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fd64b8b9f335638b54a0bf6473b5d159c97a0e7f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398132"
---
# <a name="starting-lync-from-another-application"></a><span data-ttu-id="500c2-103">別のアプリケーションから Lync を起動する</span><span class="sxs-lookup"><span data-stu-id="500c2-103">Starting Lync from another application</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="500c2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="500c2-104">

<span> </span></span></span>

<span data-ttu-id="500c2-105">_**トピックの最終更新日:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="500c2-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="500c2-106">コマンドラインパラメーターを使用して、Lync 2013 のクイック起動を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="500c2-106">You can use command-line parameters to quick-start Lync 2013.</span></span> <span data-ttu-id="500c2-107">たとえば、ユーザーが別のアプリケーションで電話番号をクリックした場合、アプリケーションは Lync 2013 のインスタンスを起動し、その番号への通話を開始することができます。</span><span class="sxs-lookup"><span data-stu-id="500c2-107">For example, if a user clicks a phone number in another application, the application can start an instance of Lync 2013 and initiate a call to that number.</span></span>

<span data-ttu-id="500c2-108">Lync 2013 では、連絡先名のセミコロンで区切られたリストを、マルチパーティ会議でも認識できます。</span><span class="sxs-lookup"><span data-stu-id="500c2-108">Lync 2013 can also recognize a semicolon-delimited list of contact names for multiparty conferencing.</span></span>

<span data-ttu-id="500c2-109">Lync 2013 が起動時に自動的にサインインするように構成されている場合は、コマンドラインパラメーターを使用して Lync 2013 を起動すると、Lync メインウィンドウが開きます。</span><span class="sxs-lookup"><span data-stu-id="500c2-109">If Lync 2013 is configured to automatically sign in when started, then starting Lync 2013 with command-line parameters will open the Lync main window.</span></span> <span data-ttu-id="500c2-110">Lync が起動時に自動的にサインインするように構成されていない場合は、サインインウィンドウが開きます。</span><span class="sxs-lookup"><span data-stu-id="500c2-110">If Lync is not configured to automatically sign in when started, the sign-in window opens.</span></span>

<span data-ttu-id="500c2-111">次の表は、使用できるパラメーターを示しています。</span><span class="sxs-lookup"><span data-stu-id="500c2-111">The following table shows the available parameters.</span></span>

### <a name="lync-2013-command-line-parameters"></a><span data-ttu-id="500c2-112">Lync 2013 Command-Line のパラメーター</span><span class="sxs-lookup"><span data-stu-id="500c2-112">Lync 2013 Command-Line Parameters</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="500c2-113">補助</span><span class="sxs-lookup"><span data-stu-id="500c2-113">Extension</span></span></th>
<th><span data-ttu-id="500c2-114">データの書式設定</span><span class="sxs-lookup"><span data-stu-id="500c2-114">Format of Data</span></span></th>
<th><span data-ttu-id="500c2-115">アクション</span><span class="sxs-lookup"><span data-stu-id="500c2-115">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="500c2-116">tel</span><span class="sxs-lookup"><span data-stu-id="500c2-116">tel:</span></span></p></td>
<td><p><span data-ttu-id="500c2-117">tel URI</span><span class="sxs-lookup"><span data-stu-id="500c2-117">tel URI</span></span></p></td>
<td><p><span data-ttu-id="500c2-118">音声通話の会話ウィンドウが開きますが、指定された番号をダイヤルしません。</span><span class="sxs-lookup"><span data-stu-id="500c2-118">Opens the Conversation window for an audio call but does not dial the specified number.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="500c2-119">callto</span><span class="sxs-lookup"><span data-stu-id="500c2-119">callto:</span></span></p></td>
<td><p><span data-ttu-id="500c2-120">tel:、sip:、または?</span><span class="sxs-lookup"><span data-stu-id="500c2-120">tel:, sip:, or typeable tel URI</span></span></p></td>
<td><p><span data-ttu-id="500c2-121">音声通話の会話ウィンドウが開きますが、指定された番号をダイヤルしません。</span><span class="sxs-lookup"><span data-stu-id="500c2-121">Opens the Conversation window for an audio call but does not dial the specified number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="500c2-122">フェデレーション</span><span class="sxs-lookup"><span data-stu-id="500c2-122">sip:</span></span></p></td>
<td><p><span data-ttu-id="500c2-123">SIP URI</span><span class="sxs-lookup"><span data-stu-id="500c2-123">SIP URI</span></span></p></td>
<td><p><span data-ttu-id="500c2-124">参加者リストの指定した SIP uri (URL) を使用して、会話ウィンドウを開きます。</span><span class="sxs-lookup"><span data-stu-id="500c2-124">Opens the Conversation window with the specified SIP Uniform Resource Identifier (URI) in the participant list.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="500c2-125">Sip</span><span class="sxs-lookup"><span data-stu-id="500c2-125">Sips:</span></span></p></td>
<td><p><span data-ttu-id="500c2-126">SIP URI</span><span class="sxs-lookup"><span data-stu-id="500c2-126">SIP URI</span></span></p></td>
<td><p><span data-ttu-id="500c2-127">Lync 2013 がトランスポート層セキュリティ (TLS) プロトコルを使用するように構成されている場合、sip: とまったく同じ機能が使われます。</span><span class="sxs-lookup"><span data-stu-id="500c2-127">If Lync 2013 is configured to use the Transport Layer Security (TLS) protocol, functions exactly like sip:.</span></span> <span data-ttu-id="500c2-128">TLS が使用されていない場合は、より高いレベルのセキュリティが必要であることをユーザーに知らせるダイアログボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="500c2-128">If TLS is not being used, displays a dialog box informing the user that a higher level of security is required.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="500c2-129">会議</span><span class="sxs-lookup"><span data-stu-id="500c2-129">conf:</span></span></p></td>
<td><p><span data-ttu-id="500c2-130">参加する会議の SIP URI</span><span class="sxs-lookup"><span data-stu-id="500c2-130">SIP URI of conference to join</span></span></p></td>
<td><p><span data-ttu-id="500c2-131">URI が self の場合は、フォーカスがインスタンス化され、一覧のみのビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="500c2-131">If URI is self, instantiates the focus and brings up roster-only view.</span></span> <span data-ttu-id="500c2-132">そうしないと、[名簿] ビューが表示されますが、招待状は送信されません。</span><span class="sxs-lookup"><span data-stu-id="500c2-132">Otherwise, brings up roster view but does not send INVITE.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="500c2-133">im</span><span class="sxs-lookup"><span data-stu-id="500c2-133">im:</span></span></p></td>
<td><p><span data-ttu-id="500c2-134">SIP URI</span><span class="sxs-lookup"><span data-stu-id="500c2-134">SIP URI</span></span></p></td>
<td><p><span data-ttu-id="500c2-135">SIP URI でインスタントメッセージング (IM) 専用の会話ウィンドウを表示します。</span><span class="sxs-lookup"><span data-stu-id="500c2-135">Displays an instant messaging (IM)-only Conversation window with the SIP URI.</span></span> <span data-ttu-id="500c2-136">&lt;区切り記号を付けずに、山かっこ () 内で指定された複数の SIP uri &gt; を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="500c2-136">Accepts multiple SIP URIs specified inside angle brackets (&lt;&gt;) without any separator.</span></span></p>
<pre><code>im:&lt;sip:user1@host&gt;&lt;sip:user2@host&gt;</code></pre></td>
</tr>
</tbody>
</table>


<span data-ttu-id="500c2-137">次の表では、これらのコマンドラインパラメーターの例を示します。</span><span class="sxs-lookup"><span data-stu-id="500c2-137">The following table provides examples of these command-line parameters.</span></span>

### <a name="command-line-parameter-examples"></a><span data-ttu-id="500c2-138">Command-Line パラメーターの例</span><span class="sxs-lookup"><span data-stu-id="500c2-138">Command-Line Parameter Examples</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="500c2-139">Instance</span><span class="sxs-lookup"><span data-stu-id="500c2-139">Instance</span></span></th>
<th><span data-ttu-id="500c2-140">より</span><span class="sxs-lookup"><span data-stu-id="500c2-140">Results</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="500c2-141">Tel: + 14255550101</span><span class="sxs-lookup"><span data-stu-id="500c2-141">Tel:+14255550101</span></span></p></td>
<td><p><span data-ttu-id="500c2-142">+ 14255550101 で電話専用ビューを開きます。</span><span class="sxs-lookup"><span data-stu-id="500c2-142">Opens a phone-only view with +14255550101.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="500c2-143">Callto: tel: + 14255550101</span><span class="sxs-lookup"><span data-stu-id="500c2-143">Callto:tel:+ 14255550101</span></span></p></td>
<td><p><span data-ttu-id="500c2-144">+ 14255550101 で電話専用ビューを開きます。</span><span class="sxs-lookup"><span data-stu-id="500c2-144">Opens a phone-only view with +14255550101.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="500c2-145">Callto:sip:kazuto@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="500c2-145">Callto:sip:kazuto@litwareinc.com</span></span></p></td>
<td><p><span data-ttu-id="500c2-146">Kazuto@litwareinc.com で電話専用ビューを開きます。</span><span class="sxs-lookup"><span data-stu-id="500c2-146">Opens a phone-only view with kazuto@litwareinc.com.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="500c2-147">sip:kazuto@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="500c2-147">sip:kazuto@litwareinc.com</span></span></p></td>
<td><p><span data-ttu-id="500c2-148">Kazuto@litwareinc.com を使用して、会話ウィンドウを開きます。</span><span class="sxs-lookup"><span data-stu-id="500c2-148">Opens a Conversation window with kazuto@litwareinc.com.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="500c2-149">conf: sip:https://meet.contoso.com/kazuto/7322994</span><span class="sxs-lookup"><span data-stu-id="500c2-149">conf:sip:https://meet.contoso.com/kazuto/7322994</span></span></p></td>
<td><p><span data-ttu-id="500c2-150">会話ウィンドウが開き、会議の音声参加オプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="500c2-150">Opens a Conversation window and displays meeting audio join options.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="500c2-151">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="500c2-151">


</div>

<span> </span>

</div>

</div>

</span></span></div>

