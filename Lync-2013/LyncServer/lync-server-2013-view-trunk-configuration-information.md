---
title: 'Lync Server 2013: トランク構成情報の表示'
description: 'Lync Server 2013: トランク構成情報を表示します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View trunk configuration information
ms:assetid: ebe10e14-08c2-4797-9254-9ed89516d5cd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721927(v=OCS.15)
ms:contentKeyID: 49733862
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1b4e1d3063d65f8c27ad231f063249748046f759
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444029"
---
# <a name="view-trunk-configuration-information-in-lync-server-2013"></a><span data-ttu-id="cb2db-103">Lync Server 2013 でのトランク構成情報の表示</span><span class="sxs-lookup"><span data-stu-id="cb2db-103">View trunk configuration information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cb2db-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cb2db-104">

<span> </span></span></span>

<span data-ttu-id="cb2db-105">_**最終更新日:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="cb2db-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="cb2db-106">SIP トランク構成設定は、仲介サーバーと公衆交換電話網 (PSTN) ゲートウェイ、IP パブリックブランチ交換 (PBX)、またはサービスプロバイダのセッションボーダーコントローラー (SBC) 間の関係と機能を定義します。</span><span class="sxs-lookup"><span data-stu-id="cb2db-106">SIP trunk configuration settings define the relationship and capabilities between a Mediation Server and the public switched telephone network (PSTN) gateway, an IP-public branch exchange (PBX), or a Session Border Controller (SBC) at the service provider.</span></span> <span data-ttu-id="cb2db-107">たとえば、次の設定ができます。</span><span class="sxs-lookup"><span data-stu-id="cb2db-107">These settings do such things as specify:</span></span>

  - <span data-ttu-id="cb2db-108">トランクでメディア バイパスを有効化するか。</span><span class="sxs-lookup"><span data-stu-id="cb2db-108">Whether media bypass should be enabled on the trunks.</span></span>

  - <span data-ttu-id="cb2db-109">リアルタイム伝送制御プロトコル (RTCP) パケットを送信する条件。</span><span class="sxs-lookup"><span data-stu-id="cb2db-109">The conditions under which real-time transport control protocol (RTCP) packets are sent.</span></span>

  - <span data-ttu-id="cb2db-110">各トランクで、セキュリティで保護されたリアルタイムプロトコル (SRTP) 暗号化が必要かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="cb2db-110">Whether or not secure real-time protocol (SRTP) encryption is required on each trunk.</span></span>

<span data-ttu-id="cb2db-111">Microsoft Lync Server 2013 をインストールすると、SIP トランク構成設定のグローバルコレクションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="cb2db-111">When you install Microsoft Lync Server 2013, a global collection of SIP trunk configuration settings is created for you.</span></span> <span data-ttu-id="cb2db-112">また、管理者はサイト スコープまたはサービス スコープ (PSTN ゲートウェイ サービスの場合のみ) でカスタム設定のコレクションを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="cb2db-112">In addition, administrators can create custom setting collections at the site scope or at the service scope (for the PSTN gateway service, only).</span></span>

<div>

## <a name="to-view-sip-trunk-configuration-information-by-using-lync-server-control-panel"></a><span data-ttu-id="cb2db-113">Lync Server コントロールパネルを使用して SIP トランクの構成情報を表示するには</span><span class="sxs-lookup"><span data-stu-id="cb2db-113">To view SIP trunk configuration information by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="cb2db-114">Lync Server コントロールパネルで、[ **音声ルーティング** ] をクリックし、[ **トランク構成**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cb2db-114">In Lync Server Control Panel, click **Voice Routing** and then click **Trunk Configuration**.</span></span>

2.  <span data-ttu-id="cb2db-115">[ **トランクの構成** ] タブに、すべてのトランク構成設定のコレクションの一覧が表示されます。各コレクションについて、 **名前**、 **スコープ**、 **状態**、 **メディアバイパス** の各プロパティの値と共に、 **PSTN 使用** 量、 **通話番号の規則**、コレクションに関連付けられている **番号ルール** の数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="cb2db-115">On the **Trunk Configuration** tab you will see a list of all your trunk configuration settings collection; for each collection you will see values for the **Name**, **Scope**, **State**, and **Media bypass** properties, along with the number of **PSTN usages**, **Calling number rules**, and **Called number rules** associated with the collection.</span></span> <span data-ttu-id="cb2db-116">トランク構成設定のコレクションに関する追加情報を表示するには、目的のコレクションをクリックし、[ **編集**] をクリックして、[ **詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cb2db-116">To see additional details about a collection of trunk configuration settings, click the collection of interest, click **Edit**, and then click **Show details**.</span></span> <span data-ttu-id="cb2db-117">一度に1つのトランク構成設定のコレクションについてのみ、詳細情報を表示できます。</span><span class="sxs-lookup"><span data-stu-id="cb2db-117">Note that you can view detailed information only for one collection of trunk configuration settings at a time.</span></span>

</div>

<div>

## <a name="viewing-sip-trunk-configuration-information-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="cb2db-118">Windows PowerShell コマンドレットを使用した SIP トランク構成情報の表示</span><span class="sxs-lookup"><span data-stu-id="cb2db-118">Viewing SIP Trunk Configuration Information by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="cb2db-119">SIP トランク構成設定は、Lync Server PowerShell と Get-CsTrunkConfiguration コマンドレットを使用して表示できます。</span><span class="sxs-lookup"><span data-stu-id="cb2db-119">SIP trunk configuration settings can be viewed by using Lync Server PowerShell and the Get-CsTrunkConfiguration cmdlet.</span></span> <span data-ttu-id="cb2db-120">このコマンドレットは、Lync Server 2013 Management Shell またはリモートセッション Windows PowerShell から実行できます。</span><span class="sxs-lookup"><span data-stu-id="cb2db-120">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session Windows PowerShell.</span></span> <span data-ttu-id="cb2db-121">リモートの Windows PowerShell を使用して Lync Server に接続する方法について詳しくは、Lync Server Windows PowerShell のブログ記事「Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell (クイックスタート: リモート PowerShell を使用した Microsoft Lync Server 2010 の管理)」を[https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876)で参照してください。</span><span class="sxs-lookup"><span data-stu-id="cb2db-121">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-sip-trunk-configuration-information"></a><span data-ttu-id="cb2db-122">SIP トランクの構成情報を表示するには</span><span class="sxs-lookup"><span data-stu-id="cb2db-122">To view SIP trunk configuration information</span></span>

  - <span data-ttu-id="cb2db-123">SIP トランク構成のすべての設定に関する情報を表示するには、Lync Server 管理シェルで次のコマンドを入力して、enter キーを押します。</span><span class="sxs-lookup"><span data-stu-id="cb2db-123">To view information about all your SIP trunk configuration settings, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsTrunkConfiguration
    
    <span data-ttu-id="cb2db-124">次のような情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="cb2db-124">That will return information similar to this:</span></span>
    
        Identity                                  : Global
        OutboundTranslationRulesList              : {}
        SipResponseCodeTranslationRulesList       : {}
        OutboundCallingNumberTranslationRulesList : {}
        PstnUsages                                : {}
        Description                               :
        ConcentratedTopology                      : True
        EnableBypass                              : False
        EnableMobileTrunkSupport                  : False
        EnableReferSupport                        : True
        EnableSessionTimer                        : False
        EnableSignalBoost                         : False
        MaxEarlyDialogs                           : 20
        RemovePlusFromUri                         : False
        RTCPActiveCalls                           : True
        RTCPCallsOnHold                           : True
        SRTPMode                                  : Required
        EnablePIDFLOSupport                       : False
        EnableRTPLatching                         : False
        EnableOnlineVoice                         : False
        ForwardCallHistory                        : False
        Enable3pccRefer                           : False
        ForwardPAI                                : False
        EnableFastFailoverTimer                   : True

</div>

<span data-ttu-id="cb2db-125">詳細については、 [set-cstrunkconfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsTrunkConfiguration) コマンドレットのヘルプトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="cb2db-125">For more information, see the help topic for the [Get-CsTrunkConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsTrunkConfiguration) cmdlet.</span></span>

<span data-ttu-id="cb2db-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cb2db-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

