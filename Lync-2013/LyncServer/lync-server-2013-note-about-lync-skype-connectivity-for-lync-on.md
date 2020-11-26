---
title: 'Lync Server 2013: Lync の Lync-Skype 接続についての注意'
description: 'Lync Server 2013: Lync の Lync-Skype 接続についてメモします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Note about Lync-Skype connectivity for Lync On
ms:assetid: 1d0f5c1a-74c6-468f-9877-ad2b1ddf355f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn440169(v=OCS.15)
ms:contentKeyID: 57793359
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3f7d9758f277f2f987677c2c0ffa0a4447ba31d1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424976"
---
# <a name="note-about-lync-skype-connectivity-in-lync-server-2013-for-lync-online-customers"></a><span data-ttu-id="1ac7f-103">Lync Online ユーザー向けの Lync Server 2013 での Lync-Skype 接続についての注意</span><span class="sxs-lookup"><span data-stu-id="1ac7f-103">Note about Lync-Skype connectivity in Lync Server 2013 for Lync Online customers</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1ac7f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1ac7f-104">

<span> </span></span></span>

<span data-ttu-id="1ac7f-105">_**最終更新日:** 2013-09-23_</span><span class="sxs-lookup"><span data-stu-id="1ac7f-105">_**Topic Last Modified:** 2013-09-23_</span></span>

<span data-ttu-id="1ac7f-106">このドキュメントは、Lync Server のオンプレミス管理者が Lync-Skype 接続をセットアップできるように作成されています。</span><span class="sxs-lookup"><span data-stu-id="1ac7f-106">This document was written to help Lync Server on-premise administrators set up Lync-Skype connectivity.</span></span>  <span data-ttu-id="1ac7f-107">Lync-Skype 接続は、Office 365 および Microsoft 365 の一部である、Lync Online の機能でもあります。</span><span class="sxs-lookup"><span data-stu-id="1ac7f-107">Lync-Skype connectivity is also a feature of Lync Online, which is part of Office 365 and Microsoft 365.</span></span> <span data-ttu-id="1ac7f-108">管理センター内の Lync 管理センターから Lync-Skype 接続機能を有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="1ac7f-108">You can enable the Lync-Skype connectivity feature from the Lync Administration Center within the admin center.</span></span>

<span data-ttu-id="1ac7f-109">Microsoft 365 中堅企業向け、Office 365 Enterprise、Microsoft 365 エデュケーション、および Office 365: Office 365 ポータルまたは Microsoft 365 管理センターにサインインして、 **Lync 管理センター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="1ac7f-109">For Microsoft 365 Midsize Business, Office 365 Enterprise, Microsoft 365 Education, and Office 365 for Government: Sign in to the Office 365 portal or Microsoft 365 admin center and navigate to the **Lync Administration Center**.</span></span> <span data-ttu-id="1ac7f-110">**外部通信** に移動します。</span><span class="sxs-lookup"><span data-stu-id="1ac7f-110">Go to **External Communications**.</span></span> <span data-ttu-id="1ac7f-111">[ **パブリック IM サービスプロバイダー**] で [ **有効にする**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1ac7f-111">Under **Public IM Service Providers**, click **Enable**.</span></span> <span data-ttu-id="1ac7f-112">個々のユーザーによる接続 Lync-Skype のアクセスを制御する場合は、個々のユーザーの外部通信設定を編集します。</span><span class="sxs-lookup"><span data-stu-id="1ac7f-112">If you want to control individual user access to Lync-Skype Connectivity, you can do so by editing individual users’ External Communications settings.</span></span>

<span data-ttu-id="1ac7f-113">Microsoft 365 Small Business Premium の場合: Microsoft 365 にサインインし、[ **管理サービス設定] の [ \> \> インスタントメッセージング、ミーティング、および会議**] に移動します。</span><span class="sxs-lookup"><span data-stu-id="1ac7f-113">For Microsoft 365 Small Business Premium: Sign in to Microsoft 365, and go to **Admin \> Service Settings \> Instant messaging, meetings and conferencing**.</span></span> <span data-ttu-id="1ac7f-114">外部通信を有効にします。</span><span class="sxs-lookup"><span data-stu-id="1ac7f-114">Turn on External communications.</span></span> <span data-ttu-id="1ac7f-115">[外部通信] スイッチは、Lync を使用する他の組織との Lync-Skype 接続と通信の両方を有効にします。</span><span class="sxs-lookup"><span data-stu-id="1ac7f-115">The External communications switch turns on both Lync-Skype connectivity and communications with other organizations that use Lync.</span></span> <span data-ttu-id="1ac7f-116">Lync Online の使用を開始した時点によっては、"オン" 状態の外部通信スイッチが、他の Lync 組織との通信がアクティブ化されていることだけが最初に表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="1ac7f-116">Depending on when you started using Lync Online, the External communications switch in an "on" state may initially indicate only that communications with other Lync organizations is activated.</span></span> <span data-ttu-id="1ac7f-117">Lync-Skype 接続を有効にするには、スイッチをオフにしてからもう一度オンに切り替えます。</span><span class="sxs-lookup"><span data-stu-id="1ac7f-117">To turn on Lync-Skype Connectivity, simply toggle the switch off and then back on again.</span></span>

<span data-ttu-id="1ac7f-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1ac7f-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

