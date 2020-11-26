---
title: 中央集中ログサービスの構成設定を管理する
description: 一元的なログサービスの構成設定を管理する。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing the Centralized Logging Service configuration settings
ms:assetid: f455c3aa-0061-413d-bdfb-a3e78f82723d
ms:mtpsurl: https://technet.microsoft.com/library/JJ721938(v=OCS.15)
ms:contentKeyID: 49733875
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e25294e096b8368aa06a11e4ad851fe5d1a84c0f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425900"
---
# <a name="managing-the-centralized-logging-service-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="91b1a-103">Lync Server 2013 で中央集中ログサービスの構成設定を管理する</span><span class="sxs-lookup"><span data-stu-id="91b1a-103">Managing the Centralized Logging Service configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="91b1a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="91b1a-104">

<span> </span></span></span>

<span data-ttu-id="91b1a-105">_**最終更新日:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="91b1a-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="91b1a-106">一元化されたログサービスは、一元管理サービスコントローラー (CLSController) によって作成および使用される設定とパラメーターによって制御および構成され、個々のコンピューターの集中ログサービスエージェント (Clscontroller) にコマンドを送信します。</span><span class="sxs-lookup"><span data-stu-id="91b1a-106">The Centralized Logging Service is controlled and configured by settings and parameters that are created and used by the Centralized Logging Service Controller (CLSController) to send commands to the individual computer’s Centralized Logging Service Agent (CLSAgent).</span></span> <span data-ttu-id="91b1a-107">エージェントは、送信されたコマンドを処理し、開始コマンドの場合は、提供された構成情報に従って、シナリオ、プロバイダー、ログサイズ、トレースの継続時間、フラグの構成を使ってトレースログの収集を開始します。</span><span class="sxs-lookup"><span data-stu-id="91b1a-107">The agent processes the commands that are sent to it and (in the case of a Start command) uses the configuration of the scenarios, providers, log size, trace duration, and flags to begin collecting trace logs according to the configuration information provided.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="91b1a-108">一元管理のログサービス用に一覧表示されているすべての Windows PowerShell コマンドレットは、Lync Server 2013 オンプレミスの展開で使用することを目的としていません。</span><span class="sxs-lookup"><span data-stu-id="91b1a-108">Not all Windows PowerShell cmdlets listed for the Centralized Logging Service are intended for use with Lync Server 2013 on-premises deployments.</span></span> <span data-ttu-id="91b1a-109">機能しているように見えても、次のコマンドレットは Lync Server 2013 オンプレミスの展開で機能するように設計されていません。</span><span class="sxs-lookup"><span data-stu-id="91b1a-109">Although they may appear to work, the following cmdlets are not designed to function with Lync Server 2013 on-premises deployments:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="91b1a-110"><STRONG>Csclsregion コマンドレット:</STRONG> <A href="https://technet.microsoft.com/library/JJ204879(v=OCS.15)">Get-csclsregion</A>、 <A href="https://technet.microsoft.com/library/JJ204746(v=OCS.15)">Set-csclsregion</A>、 <A href="https://technet.microsoft.com/library/JJ204658(v=OCS.15)">New-</A>CsClsRegion、および削除された <A href="https://technet.microsoft.com/library/JJ204971(v=OCS.15)">csclsregion</A>。</span><span class="sxs-lookup"><span data-stu-id="91b1a-110"><STRONG>CsClsRegion cmdlets:</STRONG> <A href="https://technet.microsoft.com/library/JJ204879(v=OCS.15)">Get-CsClsRegion</A>, <A href="https://technet.microsoft.com/library/JJ204746(v=OCS.15)">Set-CsClsRegion</A>, <A href="https://technet.microsoft.com/library/JJ204658(v=OCS.15)">New-CsClsRegion</A>, and <A href="https://technet.microsoft.com/library/JJ204971(v=OCS.15)">Remove-CsClsRegion</A>.</span></span></P>
> <LI>
> <P><span data-ttu-id="91b1a-111"><STRONG>Csclssearchterm コマンドレット:</STRONG> <A href="https://technet.microsoft.com/library/JJ205061(v=OCS.15)">取得-csclssearchterm</A> と <A href="https://technet.microsoft.com/library/JJ204911(v=OCS.15)">Set-csclssearchterm</A>。</span><span class="sxs-lookup"><span data-stu-id="91b1a-111"><STRONG>CsClsSearchTerm cmdlets:</STRONG> <A href="https://technet.microsoft.com/library/JJ205061(v=OCS.15)">Get-CsClsSearchTerm</A> and <A href="https://technet.microsoft.com/library/JJ204911(v=OCS.15)">Set-CsClsSearchTerm</A>.</span></span></P>
> <LI>
> <P><span data-ttu-id="91b1a-112"><STRONG>CsClsSecurityGroup コマンドレット:</STRONG> <A href="https://technet.microsoft.com/library/JJ205285(v=OCS.15)">CsClsSecurityGroup</A>、 <A href="https://technet.microsoft.com/library/JJ204700(v=OCS.15)">Set-CsClsSecurityGroup</A>、 <A href="https://technet.microsoft.com/library/JJ205359(v=OCS.15)">New-CsClsSecurityGroup</A>、および <A href="https://technet.microsoft.com/library/JJ204958(v=OCS.15)">CsClsSecurityGroup を削除</A>します。</span><span class="sxs-lookup"><span data-stu-id="91b1a-112"><STRONG>CsClsSecurityGroup cmdlets:</STRONG> <A href="https://technet.microsoft.com/library/JJ205285(v=OCS.15)">Get-CsClsSecurityGroup</A>, <A href="https://technet.microsoft.com/library/JJ204700(v=OCS.15)">Set-CsClsSecurityGroup</A>, <A href="https://technet.microsoft.com/library/JJ205359(v=OCS.15)">New-CsClsSecurityGroup</A>, and <A href="https://technet.microsoft.com/library/JJ204958(v=OCS.15)">Remove-CsClsSecurityGroup</A>.</span></span></P></LI></UL><span data-ttu-id="91b1a-113">これらのコマンドレットで定義された設定によって、悪影響を及ぼすことはありませんが、Microsoft 365 で使用するように設計されており、オンプレミスの展開で期待される結果を得られません。</span><span class="sxs-lookup"><span data-stu-id="91b1a-113">The settings defined in these cmdlets will not hinder or cause any adverse behavior, but they are designed for use with Microsoft 365 and will not yield the expected results in on-premises deployments.</span></span> <span data-ttu-id="91b1a-114">これは、内部設置型展開ではこれらのコマンドレットが役に立たないという意味ではありませんが、その用途はより高度なトピックであるため、このドキュメントでは扱われません。</span><span class="sxs-lookup"><span data-stu-id="91b1a-114">This is not to say that there is no use for these cmdlets in on-premises deployments, but their use is a more advanced topic that is not covered in this documentation.</span></span>


</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="91b1a-115">このセクション中</span><span class="sxs-lookup"><span data-stu-id="91b1a-115">In This Section</span></span>

<span data-ttu-id="91b1a-116">このセクションのトピックでは、一元管理サービスの構成オプション、パラメーター、設定を定義します。</span><span class="sxs-lookup"><span data-stu-id="91b1a-116">The topics in this section define the configuration options, parameters, and settings for the Centralized Logging Service.</span></span> <span data-ttu-id="91b1a-117">一元管理サービスを構成する方法、構成設定の取得方法、シナリオの作成方法、一元ログサービスのためのセキュリティグループの管理、検索などについては、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="91b1a-117">Information about how to configure the Centralized Logging Service, how to retrieve the configuration settings, creation of scenarios, management of security groups for Centralized Logging Service, searching, and more is contained in the following topics.</span></span>

  - [<span data-ttu-id="91b1a-118">Lync Server 2013 でのコンピューター、サイト、グローバルな集中ログサービスの構成の管理</span><span class="sxs-lookup"><span data-stu-id="91b1a-118">Managing computer, site and global Centralized Logging Service configuration in Lync Server 2013</span></span>](lync-server-2013-managing-computer-site-and-global-centralized-logging-service-configuration.md)

  - [<span data-ttu-id="91b1a-119">Lync Server 2013 での中央集中ログサービスのプロバイダーの構成</span><span class="sxs-lookup"><span data-stu-id="91b1a-119">Configuring providers for Centralized Logging Service in Lync Server 2013</span></span>](lync-server-2013-configuring-providers-for-centralized-logging-service.md)

  - [<span data-ttu-id="91b1a-120">Lync Server 2013 の一元ログサービスのシナリオを構成する</span><span class="sxs-lookup"><span data-stu-id="91b1a-120">Configuring scenarios for the Centralized Logging Service in Lync Server 2013</span></span>](lync-server-2013-configuring-scenarios-for-the-centralized-logging-service.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="91b1a-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="91b1a-121">See Also</span></span>


[<span data-ttu-id="91b1a-122">Lync Server 2013 の一元管理されたログサービスの概要</span><span class="sxs-lookup"><span data-stu-id="91b1a-122">Overview of the Centralized Logging Service in Lync Server 2013</span></span>](lync-server-2013-overview-of-the-centralized-logging-service.md)  
[<span data-ttu-id="91b1a-123">Lync Server 2013 の集中化されたログコマンドレット</span><span class="sxs-lookup"><span data-stu-id="91b1a-123">Centralized Logging cmdlets in Lync Server 2013</span></span>](lync-server-2013-centralized-logging-cmdlets.md)  
  

<span data-ttu-id="91b1a-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="91b1a-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

