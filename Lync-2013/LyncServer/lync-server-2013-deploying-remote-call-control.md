---
title: 'Lync Server 2013: リモート通話コントロールの展開'
description: 'Lync Server 2013: リモート通話コントロールを展開しています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying remote call control
ms:assetid: 763037f7-7a2a-49ae-acc3-9781b0bff7e0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558664(v=OCS.15)
ms:contentKeyID: 48184536
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4cc5e79f3ee44c354baf435585d304574d6a980c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429784"
---
# <a name="deploying-remote-call-control-in-lync-server-2013"></a><span data-ttu-id="0cb28-103">Lync Server 2013 でのリモート通話コントロールの展開</span><span class="sxs-lookup"><span data-stu-id="0cb28-103">Deploying remote call control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0cb28-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0cb28-104">

<span> </span></span></span>

<span data-ttu-id="0cb28-105">_**最終更新日:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="0cb28-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="0cb28-106">このセクションでは、組織内のユーザーにリモート通話コントロール機能を展開するプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="0cb28-106">This section guides you through the process of deploying remote call control functionality to users in your organization.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="0cb28-107">リモートユーザーは、組織のファイアウォールの外側にいるリモート通話コントロール機能を使用できますが、外部アクセスシナリオの展開について詳しくは、このドキュメントの範囲外です。</span><span class="sxs-lookup"><span data-stu-id="0cb28-107">Although remote call control features are available to remote users while they are outside of your organization’s firewall, details about deploying external access scenarios are beyond the scope of this documentation.</span></span> <span data-ttu-id="0cb28-108">外部ユーザーアクセスの展開の詳細については、展開ドキュメントの「 <A href="lync-server-2013-deploying-external-user-access.md">Lync Server 2013 での外部ユーザーアクセスの展開</A> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0cb28-108">For details about deploying external user access, see <A href="lync-server-2013-deploying-external-user-access.md">Deploying external user access in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="0cb28-109">このセクション中</span><span class="sxs-lookup"><span data-stu-id="0cb28-109">In This Section</span></span>

  - [<span data-ttu-id="0cb28-110">SIP/CSTA ゲートウェイにルーティングするための Lync Server 2013 の構成</span><span class="sxs-lookup"><span data-stu-id="0cb28-110">Configuring Lync Server 2013 to route to a SIP/CSTA gateway</span></span>](lync-server-2013-configuring-lync-server-to-route-to-a-sip-csta-gateway.md)

  - [<span data-ttu-id="0cb28-111">Lync Server 2013 でのリモート通話コントロールの静的ルートの構成</span><span class="sxs-lookup"><span data-stu-id="0cb28-111">Configure a static route for remote call control in Lync Server 2013</span></span>](lync-server-2013-configure-a-static-route-for-remote-call-control.md)

  - [<span data-ttu-id="0cb28-112">Lync Server 2013 でリモート通話コントロールの信頼済みアプリケーション エントリを構成する</span><span class="sxs-lookup"><span data-stu-id="0cb28-112">Configure a trusted application entry for remote call control in Lync Server 2013</span></span>](lync-server-2013-configure-a-trusted-application-entry-for-remote-call-control.md)

  - <span data-ttu-id="0cb28-113">[Lync Server 2013 で SIP/CSTA ゲートウェイの IP アドレスを定義](lync-server-2013-define-a-sip-csta-gateway-ip-address.md) する (ゲートウェイが TCP を使用するように構成されている場合のみ)</span><span class="sxs-lookup"><span data-stu-id="0cb28-113">[Define a SIP/CSTA gateway IP address in Lync Server 2013](lync-server-2013-define-a-sip-csta-gateway-ip-address.md) (only if the gateway is configured to use TCP)</span></span>

  - [<span data-ttu-id="0cb28-114">Lync Server 2013 でのリモート通話コントロールの Lync ユーザーの有効化</span><span class="sxs-lookup"><span data-stu-id="0cb28-114">Enable Lync users for remote call control in Lync Server 2013</span></span>](lync-server-2013-enable-lync-users-for-remote-call-control.md)

  - [<span data-ttu-id="0cb28-115">Lync Server 2013 でのリモート通話コントロールと電話番号正規化</span><span class="sxs-lookup"><span data-stu-id="0cb28-115">Remote call control and phone number normalization in Lync Server 2013</span></span>](lync-server-2013-remote-call-control-and-phone-number-normalization.md)

  - <span data-ttu-id="0cb28-116">[Lync Server 2013 で従来の承認済みホストを削除する (オプション)](lync-server-2013-remove-a-legacy-authorized-host-optional.md) (リモート通話コントロールで以前に有効にしたユーザーを移行する場合のみ)</span><span class="sxs-lookup"><span data-stu-id="0cb28-116">[Remove a legacy authorized host in Lync Server 2013 (optional)](lync-server-2013-remove-a-legacy-authorized-host-optional.md) (only if you are migrating users previously enabled for remote call control)</span></span>

</div>

<div>

## <a name="related-sections"></a><span data-ttu-id="0cb28-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="0cb28-117">Related Sections</span></span>

[<span data-ttu-id="0cb28-118">Lync Server 2013 でのリモート通話コントロールの計画</span><span class="sxs-lookup"><span data-stu-id="0cb28-118">Planning for remote call control in Lync Server 2013</span></span>](lync-server-2013-planning-for-remote-call-control.md)

<span data-ttu-id="0cb28-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0cb28-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

