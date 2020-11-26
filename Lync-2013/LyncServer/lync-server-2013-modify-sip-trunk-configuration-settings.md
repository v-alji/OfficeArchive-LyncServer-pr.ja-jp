---
title: 'Lync Server 2013: SIP トランク構成設定の変更'
description: 'Lync Server 2013: SIP トランクの構成設定を変更します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Modify SIP trunk configuration settings
ms:assetid: 7d68b09c-9ea0-43bd-997c-df887869d607
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688104(v=OCS.15)
ms:contentKeyID: 49733703
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 42cb213211a11494a96b5a762734a2b5db49dfbb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425452"
---
# <a name="modify-sip-trunk-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="3c2c3-103">Lync Server 2013 で SIP トランクの設定を変更する</span><span class="sxs-lookup"><span data-stu-id="3c2c3-103">Modify SIP trunk configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3c2c3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3c2c3-104">

<span> </span></span></span>

<span data-ttu-id="3c2c3-105">_**最終更新日:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="3c2c3-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="3c2c3-106">SIP トランク構成設定は、仲介サーバーと公衆交換電話網 (PSTN) ゲートウェイ、IP パブリックブランチ交換 (PBX)、またはサービスプロバイダのセッションボーダーコントローラー (SBC) 間の関係と機能を定義します。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-106">SIP trunk configuration settings define the relationship and capabilities between a Mediation Server and the public switched telephone network (PSTN) gateway, an IP-public branch exchange (PBX), or a Session Border Controller (SBC) at the service provider.</span></span> <span data-ttu-id="3c2c3-107">たとえば、次の設定ができます。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-107">These settings do such things as specify:</span></span>

  - <span data-ttu-id="3c2c3-108">トランクでメディア バイパスを有効化するか。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-108">Whether media bypass should be enabled on the trunks.</span></span>

  - <span data-ttu-id="3c2c3-109">リアルタイム伝送制御プロトコル (RTCP) パケットを送信する条件。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-109">The conditions under which real-time transport control protocol (RTCP) packets are sent.</span></span>

  - <span data-ttu-id="3c2c3-110">各トランクで、セキュリティで保護されたリアルタイムプロトコル (SRTP) 暗号化が必要かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-110">Whether or not secure real-time protocol (SRTP) encryption is required on each trunk.</span></span>

<span data-ttu-id="3c2c3-111">Microsoft Lync Server 2013 をインストールすると、SIP トランク構成設定のグローバルコレクションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-111">When you install Microsoft Lync Server 2013, a global collection of SIP trunk configuration settings is created for you.</span></span> <span data-ttu-id="3c2c3-112">また、管理者はサイト スコープまたはサービス スコープ (PSTN ゲートウェイ サービスの場合のみ) でカスタム設定のコレクションを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-112">In addition, administrators can create custom setting collections at the site scope or at the service scope (for the PSTN gateway service, only).</span></span> <span data-ttu-id="3c2c3-113">Lync Server コントロールパネルまたは Windows PowerShell を使用して、後でこれらのコレクションのいずれかを変更できます。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-113">Any of these collections can later be modified using either Lync Server Control Panel or Windows PowerShell.</span></span>

<span data-ttu-id="3c2c3-114">Lync Server コントロールパネルを使用して SIP トランクの構成設定を変更する場合は、次のオプションを利用できます。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-114">When modifying SIP trunk configuration settings using Lync Server Control Panel, the following options are available to you:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3c2c3-115">UI 設定</span><span class="sxs-lookup"><span data-stu-id="3c2c3-115">UI Setting</span></span></th>
<th><span data-ttu-id="3c2c3-116">PowerShell パラメーター</span><span class="sxs-lookup"><span data-stu-id="3c2c3-116">PowerShell Parameter</span></span></th>
<th><span data-ttu-id="3c2c3-117">説明</span><span class="sxs-lookup"><span data-stu-id="3c2c3-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3c2c3-118">名前</span><span class="sxs-lookup"><span data-stu-id="3c2c3-118">Name</span></span></p></td>
<td><p><span data-ttu-id="3c2c3-119">ID</span><span class="sxs-lookup"><span data-stu-id="3c2c3-119">Identity</span></span></p></td>
<td><p><span data-ttu-id="3c2c3-p103">コレクションの一意の識別子。このプロパティは読み取り専用です。トランク構成設定のコレクションの Identity は変更できません。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-p103">Unique identifier for the collection. This property is read-only; you cannot change the Identity of a collection of trunk configuration settings.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c2c3-122">説明</span><span class="sxs-lookup"><span data-stu-id="3c2c3-122">Description</span></span></p></td>
<td><p><span data-ttu-id="3c2c3-123">説明</span><span class="sxs-lookup"><span data-stu-id="3c2c3-123">Description</span></span></p></td>
<td><p><span data-ttu-id="3c2c3-124">管理者が、設定に関する追加情報を格納できます (たとえば、トランク構成の目的)。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-124">Provides a way for administrators to store addition information about the settings (for example, the purpose of the trunk configuration).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c2c3-125">サポートされる最大初期ダイアログの数</span><span class="sxs-lookup"><span data-stu-id="3c2c3-125">Maximum early dialogs supported</span></span></p></td>
<td><p><span data-ttu-id="3c2c3-126">MaxEarlyDialogs</span><span class="sxs-lookup"><span data-stu-id="3c2c3-126">MaxEarlyDialogs</span></span></p></td>
<td><p><span data-ttu-id="3c2c3-127">サービス プロバイダーの PSTN ゲートウェイ、IP-PBX、または SBC が、仲介サーバーに送信した INVITE に対して受信できる分岐応答の最大数です。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-127">The maximum number of forked responses a PSTN gateway, IP-PBX, or SBC at the service provider can receive to an Invite that it sent to the Mediation Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c2c3-128">暗号化サポート レベル</span><span class="sxs-lookup"><span data-stu-id="3c2c3-128">Encryption support level</span></span></p></td>
<td><p><span data-ttu-id="3c2c3-129">SRTPMode</span><span class="sxs-lookup"><span data-stu-id="3c2c3-129">SRTPMode</span></span></p></td>
<td><p><span data-ttu-id="3c2c3-130">仲介サーバーと、サービス プロバイダーの PSTN ゲートウェイ、IP-PBX、または SBC 間のメディア トラフィックを保護するためのサポート レベルを示します。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-130">Indicates the level of support for protecting media traffic between the Mediation Server and the PSTN Gateway, IP-PBX, or SBC at the service provider.</span></span> <span data-ttu-id="3c2c3-131">メディア バイパスの場合、この値はメディア構成の EncryptionLevel 設定と互換性を持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-131">For media bypass cases, this value must be compatible with the EncryptionLevel setting in the media configuration.</span></span> <span data-ttu-id="3c2c3-132">メディア構成は、 <a href="https://docs.microsoft.com/powershell/module/skype/New-CsMediaConfiguration">CsMediaConfiguration</a> コマンドレットと <a href="https://docs.microsoft.com/powershell/module/skype/Set-CsMediaConfiguration">CsMediaConfiguration</a> コマンドレットを使用して設定されます。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-132">Media configuration is set by using the <a href="https://docs.microsoft.com/powershell/module/skype/New-CsMediaConfiguration">New-CsMediaConfiguration</a> and <a href="https://docs.microsoft.com/powershell/module/skype/Set-CsMediaConfiguration">Set-CsMediaConfiguration</a> cmdlets.</span></span></p>
<p><span data-ttu-id="3c2c3-133">有効な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-133">Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="3c2c3-134">Required: SRTP 暗号化を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-134">Required: SRTP encryption must be used.</span></span></p></li>
<li><p><span data-ttu-id="3c2c3-135">Optional: ゲートウェイでサポートされている場合は、SRTP が使用されます。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-135">Optional: SRTP will be used if the gateway supports it.</span></span></p></li>
<li><p><span data-ttu-id="3c2c3-136">Not Supported: SRTP 暗号化がサポートされていないので、使用されません。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-136">Not Supported: SRTP encryption is not supported and therefore will not be used.</span></span></p></li>
</ul>
<p><span data-ttu-id="3c2c3-p105">SRTPMode は、ゲートウェイがトランスポート層セキュリティ (TLS) プロトコルを使用するよう構成されている場合にのみ使用されます。ゲートウェイがトランスポートとして伝送制御プロトコル (TCP) を使用するように構成されている場合は、SRTPMode は内部で Not Supported に設定されます。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-p105">SRTPMode is used only if the gateway is configured to use Transport Layer Security (TLS). If the gateway is configured with Transmission Control Protocol (TCP) as the transport, SRTPMode is internally set to Not Supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c2c3-139">サポートの参照</span><span class="sxs-lookup"><span data-stu-id="3c2c3-139">Refer support</span></span></p></td>
<td><p><span data-ttu-id="3c2c3-140">Enable3pccRefer</span><span class="sxs-lookup"><span data-stu-id="3c2c3-140">Enable3pccRefer</span></span></p>
<p><span data-ttu-id="3c2c3-141">EnableReferSupport</span><span class="sxs-lookup"><span data-stu-id="3c2c3-141">EnableReferSupport</span></span></p></td>
<td><p><span data-ttu-id="3c2c3-142">[<strong>ゲートウェイへの参照の送信を有効にする</strong>] に設定した場合、トランクが仲介サーバーからの REFER 要求の受信をサポートすることを示します。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-142">If set to <strong>Enable sending refer to the gateway</strong>, indicates that the trunk supports receiving Refer requests from the Mediation Server.</span></span></p>
<p><span data-ttu-id="3c2c3-143">[<strong>サードパーティ通話コントロールを使用する参照を有効にする</strong>] に設定すると、3PCC プロトコルを使用して転送される通話がホストされたサイトをバイパスできるようにすることを示します。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-143">If set to <strong>Enable refer using third-party call control</strong>, indicates that the 3pcc protocol can be used to allow transferred calls to bypass the hosted site.</span></span> <span data-ttu-id="3c2c3-144">3pcc はサードパーティコントロールとも呼ばれ、 &quot; &quot; サードパーティが1組の発信者に接続するために使用される場合 (たとえば、ユーザー a からメンバー B に電話をかけているオペレーターなど) に発生します。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-144">3pcc is also known as &quot;third party control,&quot; and occurs when a third-party is used to connect a pair of callers (for example, an operator placing a call from person A to person B).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c2c3-145">メディアのバイパスを有効にする</span><span class="sxs-lookup"><span data-stu-id="3c2c3-145">Enable media bypass</span></span></p></td>
<td><p><span data-ttu-id="3c2c3-146">EnableBypass</span><span class="sxs-lookup"><span data-stu-id="3c2c3-146">EnableBypass</span></span></p></td>
<td><p><span data-ttu-id="3c2c3-p107">メディア バイパスがこのトランクに対して有効かどうかを示します。メディア バイパスは、[<strong>集中メディア処理</strong>] も有効になっている場合にのみ有効にできます。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-p107">Indicates whether media bypass is enabled for this trunk. Media bypass can only be enabled if <strong>Centralized media processing</strong> is also enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c2c3-149">集中メディア処理</span><span class="sxs-lookup"><span data-stu-id="3c2c3-149">Centralized media processing</span></span></p></td>
<td><p><span data-ttu-id="3c2c3-150">ConcentratedTopology</span><span class="sxs-lookup"><span data-stu-id="3c2c3-150">ConcentratedTopology</span></span></p></td>
<td><p><span data-ttu-id="3c2c3-p108">既知のメディア終端ポイントがあるかどうかを示します (既知のメディア終端ポイントの例として、メディア終端が信号終端と同じ IP を持つ PSTN ゲートウェイがあります)。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-p108">Indicates whether there is a well-known media termination point. (An example of a well-known media termination point would be a PSTN gateway where the media termination has the same IP as the signaling termination.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c2c3-153">RTP ラッチを有効にする</span><span class="sxs-lookup"><span data-stu-id="3c2c3-153">Enable RTP latching</span></span></p></td>
<td><p><span data-ttu-id="3c2c3-154">EnableRTPLatching</span><span class="sxs-lookup"><span data-stu-id="3c2c3-154">EnableRTPLatching</span></span></p></td>
<td><p><span data-ttu-id="3c2c3-p109">SIP トランクが RTP ラッチをサポートするかどうかを示します。RTP ラッチは、NAT (ネットワーク アドレス変換) 装置またはファイアウォールを経由した RTP/RTCP 接続を可能にする技術です。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-p109">Indicates whether or not the SIP trunks support RTP latching. RTP latching is a technology that enables RTP/RTCP connectivity through a NAT (network address translator) device or firewall.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c2c3-157">着信転送履歴を有効にする</span><span class="sxs-lookup"><span data-stu-id="3c2c3-157">Enable forward call history</span></span></p></td>
<td><p><span data-ttu-id="3c2c3-158">ForwardCallHistory</span><span class="sxs-lookup"><span data-stu-id="3c2c3-158">ForwardCallHistory</span></span></p></td>
<td><p><span data-ttu-id="3c2c3-159">通話履歴の情報をトランク経由で転送するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-159">Indicates whether call history information will be forwarded through the trunk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c2c3-160">P-Asserted-Identity データの転送を有効にする</span><span class="sxs-lookup"><span data-stu-id="3c2c3-160">Enable forward P-Asserted-Identity data</span></span></p></td>
<td><p><span data-ttu-id="3c2c3-161">ForwardPAI</span><span class="sxs-lookup"><span data-stu-id="3c2c3-161">ForwardPAI</span></span></p></td>
<td><p><span data-ttu-id="3c2c3-p110">P-Asserted-Identity (PAI) ヘッダーを通話とともに転送するかどうかを示します。PAI ヘッダーがあれば、発信者 ID を確認できます。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-p110">Indicates whether the P-Asserted-Identity (PAI) header will be forwarded along with the call. The PAI header provides a way to verify the identity of the caller.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c2c3-164">送信ルーティング フェールオーバー タイマーを有効にする</span><span class="sxs-lookup"><span data-stu-id="3c2c3-164">Enable outbound routing failover timer</span></span></p></td>
<td><p><span data-ttu-id="3c2c3-165">EnableFastFailoverTimer</span><span class="sxs-lookup"><span data-stu-id="3c2c3-165">EnableFastFailoverTimer</span></span></p></td>
<td><p><span data-ttu-id="3c2c3-p111">発信通話が 10 秒以内にゲートウェイによって応答されない場合に次に使用できるトランクにルーティングするかどうかを示します。他にトランクがない場合は、通話は自動的に破棄されます。ネットワークおよびゲートウェイの応答が遅い環境の場合、通話が不必要に破棄されるようになる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-p111">Indicates whether outbound calls that are not answered by the gateway within 10 seconds will be routed to the next available trunk; if there are no additional trunks then the call will automatically be dropped. In an organization with slow networks and gateway responses, that could potentially result in calls being dropped unnecessarily.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c2c3-168">関連付けられている PSTN 使用法</span><span class="sxs-lookup"><span data-stu-id="3c2c3-168">Associated PSTN usages</span></span></p></td>
<td><p><span data-ttu-id="3c2c3-169">PSTNUsages</span><span class="sxs-lookup"><span data-stu-id="3c2c3-169">PSTNUsages</span></span></p></td>
<td><p><span data-ttu-id="3c2c3-170">トランクに割り当てられた PSTN 使用法のコレクションです。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-170">Collection of PSTN usages assigned to the trunk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c2c3-171">テストする変換後の番号</span><span class="sxs-lookup"><span data-stu-id="3c2c3-171">Translated number to test</span></span></p></td>
<td><p><span data-ttu-id="3c2c3-172">該当なし</span><span class="sxs-lookup"><span data-stu-id="3c2c3-172">N/A</span></span></p></td>
<td><p><span data-ttu-id="3c2c3-173">トランクの構成設定の臨時テストを行うために使用できる電話番号です。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-173">Phone number that can be used to do an ad hoc test of the trunk configuration settings.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c2c3-174">関連付けられている変換ルール</span><span class="sxs-lookup"><span data-stu-id="3c2c3-174">Associated translation rules</span></span></p></td>
<td><p><span data-ttu-id="3c2c3-175">OutboundTranslationRulesList</span><span class="sxs-lookup"><span data-stu-id="3c2c3-175">OutboundTranslationRulesList</span></span></p></td>
<td><p><span data-ttu-id="3c2c3-176">発信ルーティングによって処理される通話 (PBX または PSTN の宛先にルーティングされる通話) に適用される、電話番号変換ルールのコレクションです。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-176">Collection of phone number translation rules that apply to calls handled by Outbound Routing (calls routed to PBX or PSTN destinations).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c2c3-177">着信者番号の変換ルール</span><span class="sxs-lookup"><span data-stu-id="3c2c3-177">Called number translation rules</span></span></p></td>
<td><p><span data-ttu-id="3c2c3-178">OutboundCallingNumberTranslationRulesList</span><span class="sxs-lookup"><span data-stu-id="3c2c3-178">OutboundCallingNumberTranslationRulesList</span></span></p></td>
<td><p><span data-ttu-id="3c2c3-179">トランクに割り当てられた発信電話番号の変換ルールのコレクションです。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-179">Collection of outbound calling number translation rules assigned to the trunk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c2c3-180">テストする電話番号</span><span class="sxs-lookup"><span data-stu-id="3c2c3-180">Phone number to test</span></span></p></td>
<td><p><span data-ttu-id="3c2c3-181">該当なし</span><span class="sxs-lookup"><span data-stu-id="3c2c3-181">N/A</span></span></p></td>
<td><p><span data-ttu-id="3c2c3-182">変換ルールの臨時テストを行うために使用できる電話番号です。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-182">Phone number that can be used to do an ad hoc test of the translation rules.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c2c3-183">発信者番号</span><span class="sxs-lookup"><span data-stu-id="3c2c3-183">Calling number</span></span></p></td>
<td><p><span data-ttu-id="3c2c3-184">該当なし</span><span class="sxs-lookup"><span data-stu-id="3c2c3-184">N/A</span></span></p></td>
<td><p><span data-ttu-id="3c2c3-185">テストする電話番号が発信者の電話番号であることを示します。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-185">Indicates that the phone number to test is the phone number of the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c2c3-186">着信者番号</span><span class="sxs-lookup"><span data-stu-id="3c2c3-186">Called number</span></span></p></td>
<td><p><span data-ttu-id="3c2c3-187">該当なし</span><span class="sxs-lookup"><span data-stu-id="3c2c3-187">N/A</span></span></p></td>
<td><p><span data-ttu-id="3c2c3-188">テストする電話番号が着信者の電話番号であることを示します。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-188">Indicates that the phone number to test is the phone number of the person being called.</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="3c2c3-189">Lync Server の Set-cstrunkconfiguration コマンドレットでは、Lync Server コントロールパネルに表示されない追加のプロパティがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-189">The Lync Server CsTrunkConfiguration cmdlets support additional properties not shown in Lync Server Control Panel.</span></span> <span data-ttu-id="3c2c3-190">詳細については、 <A href="https://docs.microsoft.com/powershell/module/skype/Set-CsTrunkConfiguration">set-cstrunkconfiguration</A> コマンドレットのヘルプトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-190">For more information, see the help topic for the <A href="https://docs.microsoft.com/powershell/module/skype/Set-CsTrunkConfiguration">Set-CsTrunkConfiguration</A> cmdlet.</span></span>



</div>

<div>

## <a name="to-modify-sip-trunk-configuration-settings-by-using-lync-server-control-panel"></a><span data-ttu-id="3c2c3-191">Lync Server コントロールパネルを使用して SIP トランクの設定を変更するには</span><span class="sxs-lookup"><span data-stu-id="3c2c3-191">To modify SIP trunk configuration settings by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="3c2c3-192">Lync Server コントロールパネルで、[ **音声ルーティング**] をクリックし、[ **Trunk 構成**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-192">In Lync Server Control Panel, click **Voice Routing**, and then click **Trunk Configuration**.</span></span>

2.  <span data-ttu-id="3c2c3-p113">[**トランク構成**] タブで、変更するトランク構成の設定をダブルクリックします。編集できる設定のコレクションは一度に 1 つだけです。複数のコレクションで同じ変更を行う場合は、Windows PowerShell を使用してください。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-p113">On the **Trunk Configuration** tab, double-click the trunk configuration settings to be modified. Note that you can only edit one collection of settings at a time. If you would like to make the same changes on multiple collections, use Windows PowerShell instead.</span></span>

3.  <span data-ttu-id="3c2c3-196">[**トランク構成の編集**] ダイアログ ボックスで、適切な選択を行った後、[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-196">In the **Edit Trunk Configuration** dialog, make the appropriate selections and then click **OK**.</span></span>

4.  <span data-ttu-id="3c2c3-p114">コレクションの [**状態**] プロパティが、[**コミットされていません**] に変わります。変更をコミットし、コレクションを削除するには、[**コミット**] をクリックした後、[**すべてコミット**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-p114">The **State** property for the collection will be updated to **Uncommitted**. To commit the changes, and to delete the collection, click **Commit** and then click **Commit All**.</span></span>

5.  <span data-ttu-id="3c2c3-199">[**コミットされていない音声構成設定**] ダイアログ ボックスで、[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-199">In the **Uncommitted Voice Configuration Settings** dialog box, click **OK**.</span></span>

6.  <span data-ttu-id="3c2c3-200">[ **Microsoft Lync Server 2013 コントロールパネル** ] ダイアログボックスで、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3c2c3-200">In the **Microsoft Lync Server 2013 Control Panel** dialog box click **OK**.</span></span>

<span data-ttu-id="3c2c3-201"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3c2c3-201"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

