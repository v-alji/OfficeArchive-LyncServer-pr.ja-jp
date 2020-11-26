---
title: 'Lync Server 2013: 通話受付管理のベスト プラクティス'
description: 'Lync Server 2013: 通話受付制御のベストプラクティス'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Best practices for call admission control
ms:assetid: 97173cca-8175-4ae2-a247-eb7ef809da93
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398770(v=OCS.15)
ms:contentKeyID: 48184913
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 17c32af904dc7fb48a1a5d1903bd6ed1f81f4cb3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436070"
---
# <a name="best-practices-for-call-admission-control-in-lync-server-2013"></a><span data-ttu-id="e18f1-103">Lync Server 2013 の通話受付管理のベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="e18f1-103">Best practices for call admission control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e18f1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e18f1-104">

<span> </span></span></span>

<span data-ttu-id="e18f1-105">_**最終更新日:** 2012-09-22_</span><span class="sxs-lookup"><span data-stu-id="e18f1-105">_**Topic Last Modified:** 2012-09-22_</span></span>

<span data-ttu-id="e18f1-106">パフォーマンスを向上させて展開を容易にするには、通話受付制御を展開するときに、次のベストプラクティスを適用します。</span><span class="sxs-lookup"><span data-stu-id="e18f1-106">To enhance performance and facilitate deployment, apply the following best practices when you deploy call admission control:</span></span>

  - <span data-ttu-id="e18f1-107">Wan が、現在および予想されるメディアトラフィックに適切にプロビジョニングされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e18f1-107">Ensure that WANs are adequately provisioned for current and anticipated media traffic.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="e18f1-108">帯域幅の制限に合わせてバッファーを考慮することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e18f1-108">We recommend that you factor in a buffer to your bandwidth limits.</span></span> <span data-ttu-id="e18f1-109">使用される帯域幅の合計に影響を与える競合状態などのシナリオがあります。また、帯域幅の制限を超えた場合に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e18f1-109">There are scenarios such as race conditions that affect the total bandwidth used and can result in situations where the bandwidth limit is exceeded.</span></span> <span data-ttu-id="e18f1-110">たとえば、メディアトラフィックが帯域幅の上限に近づいている間に2つの呼び出しが開始された場合、一方の呼び出しが最初に開始されるために、一方の通話が拒否されることがあります。</span><span class="sxs-lookup"><span data-stu-id="e18f1-110">For example, if two calls try to start while media traffic is approaching a bandwidth limit, one of them may be denied because the other managed to start first.</span></span>

    
    </div>

  - <span data-ttu-id="e18f1-111">ネットワーク使用量と通話の詳細レコードを監視して、最適な CAC settings を選択し、ネットワークの使用量の変化に応じて CAC 設定を更新できるようにします。</span><span class="sxs-lookup"><span data-stu-id="e18f1-111">Monitor network usage and call detail records so that you can choose optimal CAC settings and update CAC settings as network usage changes.</span></span>

  - <span data-ttu-id="e18f1-112">CAC 帯域幅ポリシーを使用して QoS の設定を補完します。</span><span class="sxs-lookup"><span data-stu-id="e18f1-112">Use CAC bandwidth policies to complement QoS settings.</span></span>

  - <span data-ttu-id="e18f1-113">ブロックされた通話を PSTN に再ルーティングする場合は、PSTN の機能と容量を確認します。</span><span class="sxs-lookup"><span data-stu-id="e18f1-113">If you want to re-route blocked calls onto the PSTN, verify PSTN functionality and capacity.</span></span> <span data-ttu-id="e18f1-114">詳細については、「 [Lync Server 2013 での送信ボイスルーティングの計画](lync-server-2013-planning-outbound-voice-routing.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e18f1-114">For details, see [Planning outbound voice routing in Lync Server 2013](lync-server-2013-planning-outbound-voice-routing.md).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="e18f1-115">[キャパシティ] は、PSTN の潜在的な再ルーティングをサポートするために開く必要があるポートの数です。</span><span class="sxs-lookup"><span data-stu-id="e18f1-115">Capacity refers to the number of ports you need to open to support potential PSTN re-routing.</span></span>

    
    <span data-ttu-id="e18f1-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e18f1-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

