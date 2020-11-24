---
title: 'Lync Server 2013: IIS の構成'
description: 'Lync Server 2013: IIS を構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure IIS
ms:assetid: bc4ae8cc-ec0c-42f1-9034-058930e530d6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412918(v=OCS.15)
ms:contentKeyID: 48185248
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cdd08e47d05f2e32f14178eaaa3a100f8c445dda
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399368"
---
# <a name="configure-iis-for-lync-server-2013"></a><span data-ttu-id="80561-103">Lync Server 2013 での IIS の構成</span><span class="sxs-lookup"><span data-stu-id="80561-103">Configure IIS for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="80561-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="80561-104">

<span> </span></span></span>

<span data-ttu-id="80561-105">_**最終更新日:** 2011-12-16_</span><span class="sxs-lookup"><span data-stu-id="80561-105">_**Topic Last Modified:** 2011-12-16_</span></span>

<span data-ttu-id="80561-106">Lync server 2013 用のインターネットインフォメーションサービス (IIS) を構成するには、Lync Server 2013 で必要な Web サービスをサポートする適切なコンポーネントをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="80561-106">Configuring Internet Information Services (IIS) for Lync Server 2013 involves installing the correct components to support the Web Services needed by Lync Server 2013.</span></span> <span data-ttu-id="80561-107">IIS のインストールの詳細については、「 [Lync Server 2013 の iis 構成](lync-server-2013-iis-configuration.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="80561-107">For details about installing IIS, see [IIS configuration in Lync Server 2013](lync-server-2013-iis-configuration.md).</span></span> <span data-ttu-id="80561-108">サービスに移行する前に、サーバーでセキュリティ構成ウィザードを実行するポリシーを持っている場合、またはメンテナンスの一般的な部分として、サーバー上でセキュリティ構成ウィザードを実行する前に、「 [サーバーを再アクティブ化](lync-server-2013-re-activate-server-after-security-configuration-wizard-closes-ports-in-iis.md) する」を参照してください。このウィザードを実行したときに、Lync SERVER 2013 iis の構成でポートが閉じられる</span><span class="sxs-lookup"><span data-stu-id="80561-108">If you have a policy to run the Security Configuration Wizard on servers before putting them into service or as a typical part of your maintenance, see [Re-activate server after Security Configuration Wizard closes ports in IIS](lync-server-2013-re-activate-server-after-security-configuration-wizard-closes-ports-in-iis.md) for information about a side effect of running the wizard that will close ports on a Lync Server 2013 IIS configuration.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="80561-109">このセクション中</span><span class="sxs-lookup"><span data-stu-id="80561-109">In This Section</span></span>

  - [<span data-ttu-id="80561-110">Lync Server 2013 の IIS 構成</span><span class="sxs-lookup"><span data-stu-id="80561-110">IIS configuration in Lync Server 2013</span></span>](lync-server-2013-iis-configuration.md)

  - [<span data-ttu-id="80561-111">セキュリティ構成ウィザードで IIS のポートを閉じた後にサーバーを再アクティブ化する</span><span class="sxs-lookup"><span data-stu-id="80561-111">Re-activate server after Security Configuration Wizard closes ports in IIS</span></span>](lync-server-2013-re-activate-server-after-security-configuration-wizard-closes-ports-in-iis.md)

<span data-ttu-id="80561-112"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="80561-112"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

