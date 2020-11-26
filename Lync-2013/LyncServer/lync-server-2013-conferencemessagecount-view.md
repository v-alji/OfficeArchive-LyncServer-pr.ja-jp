---
title: 'Lync Server 2013: ConferenceMessageCount view'
description: 'Lync Server 2013: ConferenceMessageCount ビュー。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceMessageCount view
ms:assetid: 8ee3ee95-fb78-4d4e-bcdd-6ce5a0a23b44
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688129(v=OCS.15)
ms:contentKeyID: 49733727
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 212d6e1a346253809fb70806424350cc7fc0dfe2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434432"
---
# <a name="conferencemessagecount-view-in-lync-server-2013"></a><span data-ttu-id="a683b-103">Lync Server 2013 での ConferenceMessageCount の表示</span><span class="sxs-lookup"><span data-stu-id="a683b-103">ConferenceMessageCount view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a683b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a683b-104">

<span> </span></span></span>

<span data-ttu-id="a683b-105">_**最終更新日:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="a683b-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="a683b-106">ConferenceMessageCount ビューには、ユーザーが会議に送信したメッセージの数に関する情報が格納されます。</span><span class="sxs-lookup"><span data-stu-id="a683b-106">The ConferenceMessageCount view stores information about how many messages were sent by a user to a conference.</span></span> <span data-ttu-id="a683b-107">このビューは、Microsoft Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="a683b-107">This view was introduced in Microsoft Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a683b-108">ConferenceMessageCount ビューには、 <A href="lync-server-2013-conferencesessiondetails-view.md">Lync Server 2013 の ConferenceSessionDetails ビュー</A> のすべての列に加えて、以下の列も含まれています。</span><span class="sxs-lookup"><span data-stu-id="a683b-108">The ConferenceMessageCount view contains all of the columns in the <A href="lync-server-2013-conferencesessiondetails-view.md">ConferenceSessionDetails view in Lync Server 2013</A> in addition the columns listed below.</span></span>



</div>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a683b-109">列</span><span class="sxs-lookup"><span data-stu-id="a683b-109">Column</span></span></th>
<th><span data-ttu-id="a683b-110">データ型</span><span class="sxs-lookup"><span data-stu-id="a683b-110">Data Type</span></span></th>
<th><span data-ttu-id="a683b-111">詳細</span><span class="sxs-lookup"><span data-stu-id="a683b-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a683b-112"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="a683b-112"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="a683b-113">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="a683b-113">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="a683b-114">メッセージを送信したユーザーの URI。</span><span class="sxs-lookup"><span data-stu-id="a683b-114">URI of the user who sent the message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a683b-115"><strong>UserUriType</strong></span><span class="sxs-lookup"><span data-stu-id="a683b-115"><strong>UserUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="a683b-116">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="a683b-116">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="a683b-117">メッセージを送信したユーザーの URI の種類。</span><span class="sxs-lookup"><span data-stu-id="a683b-117">Type of URI of the user who sent the messages.</span></span> <span data-ttu-id="a683b-118">詳細については、「 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 の UriTypes テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a683b-118">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a683b-119"><strong>UserTenant</strong></span><span class="sxs-lookup"><span data-stu-id="a683b-119"><strong>UserTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="a683b-120">長さ</span><span class="sxs-lookup"><span data-stu-id="a683b-120">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="a683b-121">メッセージを送信したユーザーのテナント。</span><span class="sxs-lookup"><span data-stu-id="a683b-121">Tenant of user who sent the messages.</span></span> <span data-ttu-id="a683b-122">詳細については、「 <a href="lync-server-2013-tenants-table.md">Lync Server 2013 のテナントの一覧</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a683b-122">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a683b-123"><strong>UserMessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="a683b-123"><strong>UserMessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="a683b-124">smallint</span><span class="sxs-lookup"><span data-stu-id="a683b-124">smallint</span></span></p></td>
<td><p><span data-ttu-id="a683b-125">会議セッション中にユーザーによって送信されたメッセージの数です。</span><span class="sxs-lookup"><span data-stu-id="a683b-125">Number of messages sent by the user during the conference session.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a683b-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a683b-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

