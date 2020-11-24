---
title: 'Lync Server 2013: 一般的なエリア電話'
description: 'Lync Server 2013: 一般的なエリア電話。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Common area phones
ms:assetid: d63bb3de-154e-4347-9251-9fa94e7d593a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994076(v=OCS.15)
ms:contentKeyID: 51803987
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: af8a68f875bba1d43a91e5a252259841d7a6bbda
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400071"
---
# <a name="common-area-phones-in-lync-server-2013"></a><span data-ttu-id="b98bb-103">Lync Server 2013 の一般的なエリア電話</span><span class="sxs-lookup"><span data-stu-id="b98bb-103">Common area phones in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b98bb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b98bb-104">

<span> </span></span></span>

<span data-ttu-id="b98bb-105">_**トピックの最終更新日:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="b98bb-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="b98bb-106">一般的なエリア電話とは、個々のユーザーに関連付けられていない IP 電話のことです。</span><span class="sxs-lookup"><span data-stu-id="b98bb-106">Common area phones are IP phones that are not associated with an individual user.</span></span> <span data-ttu-id="b98bb-107">通常、一般的なエリアの電話は、他のユーザーのオフィスにいなくても、ロビー、cafeterias、従業員 lounges、会議室など、多数のユーザーが収集する可能性のある場所に配置されています。</span><span class="sxs-lookup"><span data-stu-id="b98bb-107">Instead of being located in someone’s office, common area phones are typically located in building lobbies, cafeterias, employee lounges, meeting rooms, and other locations where a large number of people are likely to gather.</span></span> <span data-ttu-id="b98bb-108">Lync Server の他の電話とは異なり、個々のユーザーに割り当てられている音声ポリシーとダイヤルプランを使うことによって管理されますが、一般的なエリア電話には個々のユーザーが割り当てられるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="b98bb-108">Unlike other phones in Lync Server, which are typically maintained by using voice policies and dial plans that are assigned to individual users, common area phones do not have individual users assigned to them.</span></span> <span data-ttu-id="b98bb-109">これは、他の電話とは異なる方法で管理する必要があることを意味します。</span><span class="sxs-lookup"><span data-stu-id="b98bb-109">This means that they must be managed differently than your other phones.</span></span>

<span data-ttu-id="b98bb-110">一般的なエリア電話を管理するために、ユーザーアカウントなどの一般的なエリアの携帯電話のための Active Directory ドメインサービスの連絡先オブジェクトを作成して、ポリシーや音声プランを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="b98bb-110">To manage common area phones, you create Active Directory Domain Services contact objects for all your common area phones that, like user accounts, can be assigned policies and voice plans.</span></span> <span data-ttu-id="b98bb-111">この方法により、共通のエリアの携帯電話を管理することができます。これらの電話は個々のユーザーに関連付けられているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="b98bb-111">This approach enables you to maintain control over common area phones, even though those phones are not associated with an individual user.</span></span>

<span data-ttu-id="b98bb-112">このセクションのトピックを使用して、一般的なエリア携帯電話の連絡先オブジェクトの作成、変更、削除、展開での一般的なエリア電話に関する構成情報の構成と表示を行う方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b98bb-112">Use the topics in this section to learn how to create contact objects for common area phones, modify and delete them, and configure and view configuration information about the common area phones in your deployment.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b98bb-113">一般的なエリア携帯電話には、Aastra 6721ip 共通エリア電話、HP 4110 IP 電話、Polycom CX500 IP 共通エリア電話の3つのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="b98bb-113">You have three options for common area phones: the Aastra 6721ip common area phone, the HP 4110 IP Phone, and the Polycom CX500 IP common area phone.</span></span> <span data-ttu-id="b98bb-114">Polycom CX3000 IP 会議電話は、別のバリエーションの一般的な市外電話です。</span><span class="sxs-lookup"><span data-stu-id="b98bb-114">The Polycom CX3000 IP conferencing phone is another variant common area phone.</span></span> <span data-ttu-id="b98bb-115">ただし、会議室での使用を目的としています。</span><span class="sxs-lookup"><span data-stu-id="b98bb-115">However, it is intended for use in conference rooms.</span></span> <span data-ttu-id="b98bb-116">一般的なエリア電話の詳細については、「 <A href="https://technet.microsoft.com/library/gg398958(v=ocs.14).aspx">新しいデバイスを選択</A>する」の「一般的な市外局番」のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b98bb-116">For details about common area phones, see the Common Area Phones section of <A href="https://technet.microsoft.com/library/gg398958(v=ocs.14).aspx">Choosing New Devices</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="b98bb-117">このセクション中</span><span class="sxs-lookup"><span data-stu-id="b98bb-117">In This Section</span></span>

  - [<span data-ttu-id="b98bb-118">Lync Server 2013 で一般的な市外局番情報を表示する</span><span class="sxs-lookup"><span data-stu-id="b98bb-118">View common area phone information in Lync Server 2013</span></span>](lync-server-2013-view-common-area-phone-information.md)

  - [<span data-ttu-id="b98bb-119">Lync Server 2013 で一般的なエリア電話の連絡先オブジェクトを作成または変更する</span><span class="sxs-lookup"><span data-stu-id="b98bb-119">Create or modify a common area phone Contact object in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-common-area-phone-contact-object.md)

  - [<span data-ttu-id="b98bb-120">Lync Server 2013 でホット desking を有効または無効にする</span><span class="sxs-lookup"><span data-stu-id="b98bb-120">Enable or disable hot desking in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-hot-desking.md)

  - [<span data-ttu-id="b98bb-121">Lync Server 2013 で一般的なエリア電話の連絡先オブジェクトを削除する</span><span class="sxs-lookup"><span data-stu-id="b98bb-121">Delete a common area phone Contact object in Lync Server 2013</span></span>](lync-server-2013-delete-a-common-area-phone-contact-object.md)

  - [<span data-ttu-id="b98bb-122">Lync Server 2013 で共通の市外局番にポリシーを割り当てる</span><span class="sxs-lookup"><span data-stu-id="b98bb-122">Assign policies in Lync Server 2013 to a common area phone</span></span>](lync-server-2013-assign-policies-to-a-common-area-phone.md)

<span data-ttu-id="b98bb-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b98bb-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

