---
title: 'Lync Server 2013: 場所のポリシーを作成する'
description: 'Lync Server 2013: 場所のポリシーを作成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create location policies
ms:assetid: f1878194-c756-4794-8fa1-15dd2118b4b3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413006(v=OCS.15)
ms:contentKeyID: 48185794
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 464ea9893890ab6185f180434e2dad13818123d1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431933"
---
# <a name="create-location-policies-in-lync-server-2013"></a><span data-ttu-id="139be-103">Lync Server 2013 で位置情報のポリシーを作成する</span><span class="sxs-lookup"><span data-stu-id="139be-103">Create location policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="139be-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="139be-104">

<span> </span></span></span>

<span data-ttu-id="139be-105">_**最終更新日:** 2012-09-11_</span><span class="sxs-lookup"><span data-stu-id="139be-105">_**Topic Last Modified:** 2012-09-11_</span></span>

<span data-ttu-id="139be-106">Lync Server は、位置情報ポリシーを使用して、クライアントの登録中に E9-1 の Lync クライアントを有効にします。</span><span class="sxs-lookup"><span data-stu-id="139be-106">Lync Server uses a location policy to enable Lync clients for E9-1-1 during client registration.</span></span> <span data-ttu-id="139be-107">場所ポリシーには、E9-1-1 の実装方法を定義する設定が含まれます。</span><span class="sxs-lookup"><span data-stu-id="139be-107">A location policy contains the settings that define how E9-1-1 will be implemented.</span></span>

<span data-ttu-id="139be-p102">グローバルの場所のポリシーを編集して、マークされた新しい場所のポリシーを作成できます。場所のポリシーが関連付けられたサブネット内部に配置されていない場合や、場所のポリシーが直接割り当てられていない場合に、クライアントはグローバル ポリシーを取得します。マークされたポリシーは、サブネットまたはユーザーに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="139be-p102">You can edit the global location policy and create new tagged location policies. A client obtains a global policy when it is not located within a subnet with an associated location policy, or when the client has not been directly assigned a location policy. Tagged policies are assigned to subnets or users.</span></span>

<span data-ttu-id="139be-111">場所のポリシーを作成するには、作成するユーザーが RTCUniversalServerAdmins グループまたは CsVoiceAdministrator 管理者役割のメンバーか、あるいは同等の管理者権限とアクセス許可を持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="139be-111">To create a location policy, you must use an account that is a member of the RTCUniversalServerAdmins group, or is a member of the CsVoiceAdministrator administrative role, or has equivalent administrator rights and permissions.</span></span>

<span data-ttu-id="139be-112">場所のポリシーの詳細については、「 [Lync Server 2013 の位置情報ポリシーを定義](lync-server-2013-defining-the-location-policy.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="139be-112">For a complete description of Location policies, see [Defining the location policy for Lync Server 2013](lync-server-2013-defining-the-location-policy.md).</span></span> <span data-ttu-id="139be-113">この手順のコマンドレットは、次の値を使用して定義された位置情報ポリシーを使用します。</span><span class="sxs-lookup"><span data-stu-id="139be-113">Cmdlets in this procedure use a location policy defined using the following values:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="139be-114">要素</span><span class="sxs-lookup"><span data-stu-id="139be-114">Element</span></span></th>
<th><span data-ttu-id="139be-115">値</span><span class="sxs-lookup"><span data-stu-id="139be-115">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="139be-116">EnhancedEmergencyServicesEnabled</span><span class="sxs-lookup"><span data-stu-id="139be-116">EnhancedEmergencyServicesEnabled</span></span></p></td>
<td><p><span data-ttu-id="139be-117"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="139be-117"><strong>True</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="139be-118">LocationRequired</span><span class="sxs-lookup"><span data-stu-id="139be-118">LocationRequired</span></span></p></td>
<td><p><span data-ttu-id="139be-119"><strong>Disclaimer</strong></span><span class="sxs-lookup"><span data-stu-id="139be-119"><strong>Disclaimer</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="139be-120">EnhancedEmergencyServiceDisclaimer</span><span class="sxs-lookup"><span data-stu-id="139be-120">EnhancedEmergencyServiceDisclaimer</span></span></p></td>
<td><p><span data-ttu-id="139be-p104">会社のポリシーで場所の設定が要求されています。場所を設定しない場合、緊急サービスが緊急時に発見できません。場所を設定してください。</span><span class="sxs-lookup"><span data-stu-id="139be-p104">Your company policy requires you to set a location. If you do not set a location, emergency services will not be able to locate you in an emergency. Please set a location.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="139be-124">UseLocationForE911Only</span><span class="sxs-lookup"><span data-stu-id="139be-124">UseLocationForE911Only</span></span></p></td>
<td><p><span data-ttu-id="139be-125"><strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="139be-125"><strong>False</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="139be-126">PstnUsage</span><span class="sxs-lookup"><span data-stu-id="139be-126">PstnUsage</span></span></p></td>
<td><p><span data-ttu-id="139be-127"><strong>EmergencyUsage</strong></span><span class="sxs-lookup"><span data-stu-id="139be-127"><strong>EmergencyUsage</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="139be-128">EmergencyDialString</span><span class="sxs-lookup"><span data-stu-id="139be-128">EmergencyDialString</span></span></p></td>
<td><p><span data-ttu-id="139be-129"><strong>911</strong></span><span class="sxs-lookup"><span data-stu-id="139be-129"><strong>911</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="139be-130">EmergencyDialMask</span><span class="sxs-lookup"><span data-stu-id="139be-130">EmergencyDialMask</span></span></p></td>
<td><p><span data-ttu-id="139be-131"><strong>112</strong></span><span class="sxs-lookup"><span data-stu-id="139be-131"><strong>112</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="139be-132">NotificationUri</span><span class="sxs-lookup"><span data-stu-id="139be-132">NotificationUri</span></span></p></td>
<td><p><span data-ttu-id="139be-133"><strong>sip:security@litwareinc.com</strong></span><span class="sxs-lookup"><span data-stu-id="139be-133"><strong>sip:security@litwareinc.com</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="139be-134">ConferenceUri</span><span class="sxs-lookup"><span data-stu-id="139be-134">ConferenceUri</span></span></p></td>
<td><p><span data-ttu-id="139be-135"><strong>sip:+14255550123@litwareinc.com</strong></span><span class="sxs-lookup"><span data-stu-id="139be-135"><strong>sip:+14255550123@litwareinc.com</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="139be-136">ConferenceMode</span><span class="sxs-lookup"><span data-stu-id="139be-136">ConferenceMode</span></span></p></td>
<td><p><span data-ttu-id="139be-137"><strong>twoway</strong></span><span class="sxs-lookup"><span data-stu-id="139be-137"><strong>twoway</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="139be-138">LocationRefreshInterval</span><span class="sxs-lookup"><span data-stu-id="139be-138">LocationRefreshInterval</span></span></p></td>
<td><p><span data-ttu-id="139be-139"><strong>2</strong></span><span class="sxs-lookup"><span data-stu-id="139be-139"><strong>2</strong></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="139be-140">場所のポリシーの使用について詳しくは、次のコマンドレットの Lync Server 管理シェルに関するドキュメントをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="139be-140">For details about working with location policies, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - <span data-ttu-id="139be-141">New-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="139be-141">New-CsLocationPolicy</span></span>

  - <span data-ttu-id="139be-142">Get-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="139be-142">Get-CsLocationPolicy</span></span>

  - <span data-ttu-id="139be-143">Set-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="139be-143">Set-CsLocationPolicy</span></span>

  - <span data-ttu-id="139be-144">Remove-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="139be-144">Remove-CsLocationPolicy</span></span>

  - <span data-ttu-id="139be-145">Grant-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="139be-145">Grant-CsLocationPolicy</span></span>

<div>

## <a name="to-create-location-policies"></a><span data-ttu-id="139be-146">場所のポリシーを作成するには</span><span class="sxs-lookup"><span data-stu-id="139be-146">To create location policies</span></span>

1.  <span data-ttu-id="139be-147">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="139be-147">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="139be-148"><STRONG>PstnUsage</STRONG> の設定がグローバルの PstnUsages 一覧にあらかじめ存在していない場合、CsLocationPolicy は失敗します。</span><span class="sxs-lookup"><span data-stu-id="139be-148">CsLocationPolicy will fail if the setting for <STRONG>PstnUsage</STRONG> is not already in the Global list of PstnUsages.</span></span>

    
    </div>

2.  <span data-ttu-id="139be-149">オプションで、次のコマンドレットを実行して、グローバルの場所のポリシーを編集します。</span><span class="sxs-lookup"><span data-stu-id="139be-149">Optionally, run the following cmdlet to edit the global Location Policy:</span></span>
    
        Set-CsLocationPolicy -Identity Global -EnhancedEmergencyServicesEnabled $true -LocationRequired "disclaimer" -EnhancedEmergencyServiceDisclaimer "Your company policy requires you to set a location. If you do not set a location emergency services will not be able to locate you in an emergency. Please set a location." -PstnUsage "emergencyUsage" -EmergencyDialString "911" -ConferenceMode "twoway" -ConferenceUri "sip:+14255550123@litwareinc.com" -EmergencyDialMask "112" NotificationUri "sip:security@litwareinc.com" -UseLocationForE911Only $true -LocationRefreshInterval 2

3.  <span data-ttu-id="139be-150">次のコマンドレットを実行してマークされた場所のポリシーを作成します。</span><span class="sxs-lookup"><span data-stu-id="139be-150">Run the following to create a tagged Location Policy.</span></span>
    
        New-CsLocationPolicy -Identity Tag:Redmond - EnhancedEmergencyServicesEnabled $true -LocationRequired "disclaimer" -EnhancedEmergencyServiceDisclaimer "Your company policy requires you to set a location. If you do not set a location emergency services will not be able to locate you in an emergency. Please set a location." -UseLocationForE911Only $false -PstnUsage "EmergencyUsage" -EmergencyDialString "911" -EmergencyDialMask "112" -NotificationUri "sip:security@litwareinc.com" -ConferenceUri "sip:+14255550123@litwareinc.com" -ConferenceMode "twoway" -LocationRefreshInterval 2

4.  <span data-ttu-id="139be-151">次のコマンドレットを実行して、ステップ 3 で作成したマークされた場所のポリシーをユーザー ポリシーに適用します。</span><span class="sxs-lookup"><span data-stu-id="139be-151">Run the following cmdlet to apply the tagged Location Policy created in step 3 to a user policy.</span></span>
    
        (Get-CsUser | where { $_.Name -match "UserName" }) | Grant-CsLocationPolicy -PolicyName Redmond

<span data-ttu-id="139be-152"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="139be-152"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

