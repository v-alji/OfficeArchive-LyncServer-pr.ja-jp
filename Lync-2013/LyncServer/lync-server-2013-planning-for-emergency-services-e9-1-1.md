---
title: 'Lync Server 2013: 緊急サービス (E9-1-1) の計画'
description: 'Lync Server 2013: 緊急電話サービスの計画 (E9-1)。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for emergency services (E9-1-1)
ms:assetid: 0a76f97b-474a-4bc1-8cd3-28c7e2bb57b9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398154(v=OCS.15)
ms:contentKeyID: 48183363
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ba4113b2355db0b1aade0ab6766e8ba7a5972aee
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424605"
---
# <a name="planning-for-emergency-services-e9-1-1-in-lync-server-2013"></a><span data-ttu-id="ba514-103">Lync Server 2013 での緊急サービス (E9-1-1) の計画</span><span class="sxs-lookup"><span data-stu-id="ba514-103">Planning for emergency services (E9-1-1) in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ba514-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ba514-104">

<span> </span></span></span>

<span data-ttu-id="ba514-105">_**最終更新日:** 2012-10-17_</span><span class="sxs-lookup"><span data-stu-id="ba514-105">_**Topic Last Modified:** 2012-10-17_</span></span>

<span data-ttu-id="ba514-106">Lync Server 2013 は、エンタープライズ Voip 展開の一部として、米国内での拡張 9-1-1 (E9-1) サービスをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="ba514-106">Lync Server 2013 supports Enhanced 9-1-1 (E9-1-1) services within the United States as part of an Enterprise Voice deployment.</span></span> <span data-ttu-id="ba514-107">E9-1 は、オフィスビルやその他のマルチテナント機能からの通話について、市民 (つまり、番地) とその他の特定の位置情報 (床番号など) で構成される緊急返信の場所 (ERL) に関連9-1-1 付けられた緊急派遣の機能です。</span><span class="sxs-lookup"><span data-stu-id="ba514-107">E9-1-1 is an emergency dispatch feature that associates a 9-1-1 call with an Emergency Response Location (ERL) that consists of civic (that is, street) addresses and other more specific location information, such as floor numbers, for calls from office buildings and other multitenant facilities.</span></span> <span data-ttu-id="ba514-108">提供された ERL を使用することによって、公開された安全な応答ポイント (PSAP) は、応答が不正確またはあいまいな場所に誤って通知されるリスクを軽減することで、最初のレスポンダーを distress で直接ディスパッチすることができます。</span><span class="sxs-lookup"><span data-stu-id="ba514-108">By using the provided ERL, a Public Safety Answering Point (PSAP) can immediately dispatch first responders to the caller in distress with reduced risk of inadvertently directing the responder to an incorrect or ambiguous location.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ba514-109">Lync Server には、通話受付制御、緊急サービス (E9-1)、メディアバイパスという3つの高度なエンタープライズ音声機能があります。</span><span class="sxs-lookup"><span data-stu-id="ba514-109">Lync Server has three advanced Enterprise Voice features: call admission control, emergency services (E9-1-1), and media bypass.</span></span> <span data-ttu-id="ba514-110">これら3つの機能の計画情報の概要については、「 <A href="lync-server-2013-network-settings-for-the-advanced-enterprise-voice-features.md">Lync Server 2013 の高度なエンタープライズ voip 機能のネットワーク設定</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ba514-110">For an overview of planning information that is common to all three of these features, see <A href="lync-server-2013-network-settings-for-the-advanced-enterprise-voice-features.md">Network settings for the advanced Enterprise Voice features in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="ba514-111">このセクション中</span><span class="sxs-lookup"><span data-stu-id="ba514-111">In This Section</span></span>

  - [<span data-ttu-id="ba514-112">Lync Server 2013 の E9-1-1 の概要</span><span class="sxs-lookup"><span data-stu-id="ba514-112">Overview of E9-1-1 in Lync Server 2013</span></span>](lync-server-2013-overview-of-e9-1-1.md)

  - [<span data-ttu-id="ba514-113">Lync Server 2013 での緊急電話の要件の定義</span><span class="sxs-lookup"><span data-stu-id="ba514-113">Defining your requirements for emergency calls in Lync Server 2013</span></span>](lync-server-2013-defining-your-requirements-for-emergency-calls.md)

  - [<span data-ttu-id="ba514-114">Lync Server 2013 の E9-1 の展開チェックリスト</span><span class="sxs-lookup"><span data-stu-id="ba514-114">Deployment checklist for E9-1-1 in Lync Server 2013</span></span>](lync-server-2013-deployment-checklist-for-e9-1-1.md)

<span data-ttu-id="ba514-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ba514-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

