---
title: 'Lync Server 2013: 音声のサポート'
description: Lync Server 2013 の音声サポート。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Voice support
ms:assetid: d151caa8-2ee4-4bfa-be53-428570aae1ea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398896(v=OCS.15)
ms:contentKeyID: 48185436
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b97b8e5ade1d97d458117adc04f161077abc9beb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443903"
---
# <a name="voice-support-in-lync-server-2013"></a><span data-ttu-id="b3f4e-103">Lync Server 2013 での音声のサポート</span><span class="sxs-lookup"><span data-stu-id="b3f4e-103">Voice support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b3f4e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b3f4e-104">

<span> </span></span></span>

<span data-ttu-id="b3f4e-105">_**最終更新日:** 2012-06-29_</span><span class="sxs-lookup"><span data-stu-id="b3f4e-105">_**Topic Last Modified:** 2012-06-29_</span></span>

<span data-ttu-id="b3f4e-106">展開にフロントエンドプールが含まれている場合は、Microsoft によって提供される VoIP (Voice over IP) ソリューションであるエンタープライズ Voip のサポートを展開できます。</span><span class="sxs-lookup"><span data-stu-id="b3f4e-106">If your deployment includes a Front End pool, you can deploy support for Enterprise Voice, the Voice over IP (VoIP) solution offered by Microsoft.</span></span> <span data-ttu-id="b3f4e-107">ボイスオーバー IP (VoIP) は、従来の PBX ベースのテレフォニーに代わるソフトウェアベースの製品です。</span><span class="sxs-lookup"><span data-stu-id="b3f4e-107">Voice over IP (VoIP) is a software-based alternative to traditional PBX-based telephony.</span></span> <span data-ttu-id="b3f4e-108">VoIP 通話のエクスペリエンスは従来のテレフォニーのエクスペリエンスと似ていますが、エンタープライズボイスには、より充実したコミュニケーションとコラボレーションを可能にする機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b3f4e-108">Although the VoIP call experience is similar to the traditional telephony experience, Enterprise Voice includes features that enable richer communication and collaboration.</span></span> <span data-ttu-id="b3f4e-109">たとえば、エンタープライズ Voip の展開を構成して、Lync 2013 および Lync Phone Edition のユーザーが、組織のアドレス帳の連絡先の拡張プレゼンス情報や位置情報を表示できるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="b3f4e-109">For example, your Enterprise Voice deployment can be configured to make it possible for Lync 2013 and Lync Phone Edition users to view enhanced presence information or location information for contacts in your organization’s address book.</span></span> <span data-ttu-id="b3f4e-110">Lync server 2013 の一部の機能は、他の Lync Server 2013 ワークロードと Exchange ユニファイドメッセージング (UM) との統合によって有効になります。</span><span class="sxs-lookup"><span data-stu-id="b3f4e-110">Some Lync Server 2013 features are enabled through integration with other Lync Server 2013 workloads and with Exchange Unified Messaging (UM).</span></span> <span data-ttu-id="b3f4e-111">エンタープライズ Voip で利用できる機能と展開を計画する方法の詳細については、計画ドキュメントの「 [Lync Server 2013 でのエンタープライズ voip の計画](lync-server-2013-planning-for-enterprise-voice.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3f4e-111">For details about the features and functionality available with Enterprise Voice and how to plan for deployment, see [Planning for Enterprise Voice in Lync Server 2013](lync-server-2013-planning-for-enterprise-voice.md) in the Planning documentation.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="b3f4e-112">このセクション中</span><span class="sxs-lookup"><span data-stu-id="b3f4e-112">In This Section</span></span>

  - [<span data-ttu-id="b3f4e-113">Lync Server 2013 での SIP トランキングのサポート</span><span class="sxs-lookup"><span data-stu-id="b3f4e-113">SIP trunking support in Lync Server 2013</span></span>](lync-server-2013-sip-trunking-support.md)

  - [<span data-ttu-id="b3f4e-114">Lync Server 2013 での直接 SIP 接続のサポート</span><span class="sxs-lookup"><span data-stu-id="b3f4e-114">Direct SIP connections support in Lync Server 2013</span></span>](lync-server-2013-direct-sip-connections-support.md)

  - [<span data-ttu-id="b3f4e-115">Lync Server 2013 での Exchange ユニファイド メッセージング (UM) のサポート</span><span class="sxs-lookup"><span data-stu-id="b3f4e-115">Exchange Unified Messaging (UM) support in Lync Server 2013</span></span>](lync-server-2013-exchange-unified-messaging-um-support.md)

  - [<span data-ttu-id="b3f4e-116">Lync Server 2013 での E9-1-1 のサポート</span><span class="sxs-lookup"><span data-stu-id="b3f4e-116">E9-1-1 support in Lync Server 2013</span></span>](lync-server-2013-e9-1-1-support.md)

<span data-ttu-id="b3f4e-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b3f4e-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

