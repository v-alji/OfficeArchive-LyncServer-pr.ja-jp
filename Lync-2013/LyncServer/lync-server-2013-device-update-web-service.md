---
title: 'Lync Server 2013: デバイス更新 Web サービス'
description: 'Lync Server 2013: デバイス更新 Web サービス。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Device Update Web service
ms:assetid: 036f473d-a131-431f-8051-76ccadc5cfba
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994015(v=OCS.15)
ms:contentKeyID: 51803921
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 45511d34ab99f295481472f2a3c14bf21da32ff6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429368"
---
# <a name="device-update-web-service-in-lync-server-2013"></a><span data-ttu-id="47afc-103">Lync Server 2013 のデバイス更新 Web サービス</span><span class="sxs-lookup"><span data-stu-id="47afc-103">Device Update Web service in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="47afc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="47afc-104">

<span> </span></span></span>

<span data-ttu-id="47afc-105">_**トピックの最終更新日:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="47afc-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="47afc-106">Lync Server には、Web サービスの役割の一部として自動的にインストールされるデバイス更新 Web サービスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="47afc-106">Lync Server includes the Device Update Web service, which is automatically installed as part of the Web Services role.</span></span> <span data-ttu-id="47afc-107">このサービスを利用すると、Microsoft から更新プログラムをダウンロードし、テストして、組織内の IP 電話に更新プログラムを展開することができます。</span><span class="sxs-lookup"><span data-stu-id="47afc-107">This service lets you download updates from Microsoft, test them, and then deploy the updates to IP phones in your organization.</span></span> <span data-ttu-id="47afc-108">また、デバイス更新 Web サービスを使って、デバイスを以前のバージョンのソフトウェアに戻すこともできます。</span><span class="sxs-lookup"><span data-stu-id="47afc-108">You can also use Device Update Web service to roll back devices to previous software versions.</span></span>

<span data-ttu-id="47afc-109">このセクションでは、デバイス更新プログラムのログ、ルール (Lync Phone Edition で、ハードウェアデバイスとのファームウェアバージョンの更新プログラムに関連付けられ *たルールを使用し* ます)、構成設定を使用して、デバイス更新 Web サービスを管理し、更新プログラムを展開する方法について詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="47afc-109">This section provides details about how to manage the Device Update Web service and deployed updates by using device update logs, rules (Lync Phone Edition uses *rules* to associate firmware version updates with hardware devices), and configuration settings.</span></span>

<span data-ttu-id="47afc-110">デバイス更新 Web サービスのプロセスと機能の詳細については、「Lync Server 2010 TechNet ライブラリでの [デバイスの更新](https://technet.microsoft.com/library/gg412864\(v=ocs.14\).aspx) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="47afc-110">For details about the Device Update Web service process and features, see [Updating Devices](https://technet.microsoft.com/library/gg412864\(v=ocs.14\).aspx) in the Lync Server 2010 TechNet Library.</span></span> <span data-ttu-id="47afc-111">(また、lync Phone Edition のすべてのコンポーネントなどのデバイス更新 Web サービスは、lync Server 2010 と同じように、Lync Server 2013 と同じように動作します)。</span><span class="sxs-lookup"><span data-stu-id="47afc-111">(Note that the Device Update Web service, like all Lync Phone Edition components, works the same way with Lync Server 2013 as it does with Lync Server 2010.)</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="47afc-112">このセクション中</span><span class="sxs-lookup"><span data-stu-id="47afc-112">In This Section</span></span>

  - [<span data-ttu-id="47afc-113">Lync Server 2013 のデバイスの更新ログとファイル</span><span class="sxs-lookup"><span data-stu-id="47afc-113">Device Update logs and files in Lync Server 2013</span></span>](lync-server-2013-device-update-logs-and-files.md)

  - [<span data-ttu-id="47afc-114">Lync Server 2013 のデバイス更新ルール</span><span class="sxs-lookup"><span data-stu-id="47afc-114">Device Update rules in Lync Server 2013</span></span>](lync-server-2013-device-update-rules.md)

  - [<span data-ttu-id="47afc-115">Lync Server 2013 のデバイス更新設定の設定</span><span class="sxs-lookup"><span data-stu-id="47afc-115">Device Update configuration settings in Lync Server 2013</span></span>](lync-server-2013-device-update-configuration-settings.md)

  - [<span data-ttu-id="47afc-116">Lync Server 2013 でのデバイスのソフトウェア更新プログラムの表示</span><span class="sxs-lookup"><span data-stu-id="47afc-116">View software updates for devices in Lync Server 2013</span></span>](lync-server-2013-view-software-updates-for-devices-in-your-organization.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="47afc-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="47afc-117">See Also</span></span>


<span data-ttu-id="47afc-118">[デバイスの管理とトラブルシューティングのためのツールとサービス](https://technet.microsoft.com/library/gg425800\(v=ocs.14\).aspx)</span><span class="sxs-lookup"><span data-stu-id="47afc-118">[Tools and Services for Managing and Troubleshooting Devices](https://technet.microsoft.com/library/gg425800\(v=ocs.14\).aspx)</span></span>  
  

<span data-ttu-id="47afc-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="47afc-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

