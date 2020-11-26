---
title: 'Lync Server 2013: SIP トランク構成設定をテストする'
description: 'Lync Server 2013: SIP トランク構成設定をテストします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test SIP trunk configuration settings
ms:assetid: c8712308-0e2d-4e39-8f90-d1a250487a94
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721880(v=OCS.15)
ms:contentKeyID: 49733814
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2d44fe2ef5123bec31fafaff2d811a501e5cca4a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444253"
---
# <a name="test-sip-trunk-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="9ad9d-103">Lync Server 2013 で SIP トランクの構成設定をテストする</span><span class="sxs-lookup"><span data-stu-id="9ad9d-103">Test SIP trunk configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9ad9d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9ad9d-104">

<span> </span></span></span>

<span data-ttu-id="9ad9d-105">_**最終更新日:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="9ad9d-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="9ad9d-106">SIP トランク構成設定は、仲介サーバーと公衆交換電話網 (PSTN) ゲートウェイ、IP パブリックブランチ交換 (PBX)、またはサービスプロバイダのセッションボーダーコントローラー (SBC) 間の関係と機能を定義します。</span><span class="sxs-lookup"><span data-stu-id="9ad9d-106">SIP trunk configuration settings define the relationship and capabilities between a Mediation Server and the public switched telephone network (PSTN) gateway, an IP-public branch exchange (PBX), or a Session Border Controller (SBC) at the service provider.</span></span> <span data-ttu-id="9ad9d-107">たとえば、次の設定ができます。</span><span class="sxs-lookup"><span data-stu-id="9ad9d-107">These settings do such things as specify:</span></span>

  - <span data-ttu-id="9ad9d-108">トランクでメディア バイパスを有効化するか。</span><span class="sxs-lookup"><span data-stu-id="9ad9d-108">Whether media bypass should be enabled on the trunks.</span></span>

  - <span data-ttu-id="9ad9d-109">リアルタイム伝送制御プロトコル (RTCP) パケットを送信する条件。</span><span class="sxs-lookup"><span data-stu-id="9ad9d-109">The conditions under which real-time transport control protocol (RTCP) packets are sent.</span></span>

  - <span data-ttu-id="9ad9d-110">各トランクで、セキュリティで保護されたリアルタイムプロトコル (SRTP) 暗号化が必要かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="9ad9d-110">Whether or not secure real-time protocol (SRTP) encryption is required on each trunk.</span></span>

<span data-ttu-id="9ad9d-111">Microsoft Lync Server 2013 をインストールすると、SIP トランク構成設定のグローバルコレクションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="9ad9d-111">When you install Microsoft Lync Server 2013, a global collection of SIP trunk configuration settings is created for you.</span></span> <span data-ttu-id="9ad9d-112">また、管理者はサイト スコープまたはサービス スコープ (PSTN ゲートウェイ サービスの場合のみ) でカスタム設定のコレクションを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="9ad9d-112">In addition, administrators can create custom setting collections at the site scope or at the service scope (for the PSTN gateway service, only).</span></span> <span data-ttu-id="9ad9d-113">管理者は、Test-CsTrunkConfiguration コマンドレットを使用して、ユーザーがダイヤルした番号をゲートウェイで処理可能な番号にトランクが変換できるかどうかも確認できます。</span><span class="sxs-lookup"><span data-stu-id="9ad9d-113">Administrators can also use the Test-CsTrunkConfiguration cmdlet to verify that a trunk can convert a number as dialed by a user to a number that can be handled by the gateway.</span></span>

<span data-ttu-id="9ad9d-114">トランク構成設定は、Windows PowerShell と [Test-CsTrunkConfiguration](https://docs.microsoft.com/powershell/module/skype/Test-CsTrunkConfiguration) コマンドレットを使用する方法でのみテストできます。</span><span class="sxs-lookup"><span data-stu-id="9ad9d-114">Trunk configuration settings can only be tested by using Windows PowerShell and the [Test-CsTrunkConfiguration](https://docs.microsoft.com/powershell/module/skype/Test-CsTrunkConfiguration) cmdlet.</span></span> <span data-ttu-id="9ad9d-115">このコマンドレットは、Lync Server 2013 管理シェルまたは Windows PowerShell のリモート セッションから実行できます。</span><span class="sxs-lookup"><span data-stu-id="9ad9d-115">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="9ad9d-116">リモートの Windows PowerShell を使用して Lync Server に接続する方法について詳しくは、Lync Server Windows PowerShell のブログ記事「Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell (クイックスタート: リモート PowerShell を使用した Microsoft Lync Server 2010 の管理)」を[https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876)で参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ad9d-116">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-test-sip-trunk-configuration-settings"></a><span data-ttu-id="9ad9d-117">SIP トランク構成設定をテストするには</span><span class="sxs-lookup"><span data-stu-id="9ad9d-117">To test SIP trunk configuration settings</span></span>

  - <span data-ttu-id="9ad9d-118">このコマンドを実行すると、ダイヤルされた番号 4255551212 がレドモンド サイトのトランク構成設定によって正しく変換できることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="9ad9d-118">This command verifies that the trunk configuration settings for the Redmond site can correctly convert the dialed number 4255551212.</span></span>
    
        $trunk = Get-CsTrunkConfiguration -Identity "site:Redmond"
        Test-CsTrunkConfiguration -DialedNumber 4255551212 -TrunkConfiguration $trunk

<span data-ttu-id="9ad9d-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9ad9d-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

