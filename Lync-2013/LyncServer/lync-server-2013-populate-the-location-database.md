---
title: 'Lync Server 2013: 場所データベースを設定する'
description: 'Lync Server 2013: 場所データベースを設定します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Populate the location database
ms:assetid: fb84f5b6-c991-4893-bdbf-f195b4b7d28e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413069(v=OCS.15)
ms:contentKeyID: 48185939
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c6cf3204795ae2c4f8248517b84d7a5ac1bad0d9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442846"
---
# <a name="populate-the-location-database-in-lync-server-2013"></a><span data-ttu-id="6a329-103">Lync Server 2013 で位置情報データベースを設定する</span><span class="sxs-lookup"><span data-stu-id="6a329-103">Populate the location database in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6a329-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6a329-104">

<span> </span></span></span>

<span data-ttu-id="6a329-105">_**最終更新日:** 2012-09-17_</span><span class="sxs-lookup"><span data-stu-id="6a329-105">_**Topic Last Modified:** 2012-09-17_</span></span>

<span data-ttu-id="6a329-p101">ネットワーク内のクライアントを自動で検出するために、まず、ネットワーク要素を正式な住所にマップする、ネットワークの *ワイヤマップ* を場所データベースに読み込む必要があります。ワイヤマップの定義には、サブネット、ワイヤレス アクセス ポイント、スイッチ、およびポートを使用できます。</span><span class="sxs-lookup"><span data-stu-id="6a329-p101">To automatically locate clients within a network, you first need to populate the location database with a network *wiremap*, which maps network elements to civic (that is, street) addresses. You can use subnets, wireless access points, switches, and ports to define the wiremap.</span></span>

<span data-ttu-id="6a329-108">住所は場所データベースに個別に追加することも、次の表に示す列形式を含む CSV ファイルを使用して一括で追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="6a329-108">You can add addresses to the location database individually, or in bulk by using a CSV file that contains the column formats described in the following table.</span></span>

<span data-ttu-id="6a329-p102">緊急位置識別番号 (ELIN) ゲートウェイを使用している場合、各場所の **[CompanyName]** フィールドに ELIN を含めます。各場所に複数の ELIN をセミコロンで区切って含めることができます。</span><span class="sxs-lookup"><span data-stu-id="6a329-p102">If you use an Emergency Location Identification Number (ELIN) gateway, include the ELIN in the **CompanyName** field for each location. You can include multiple ELINs for each location, each separated by a semicolon.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6a329-111">ネットワーク要素</span><span class="sxs-lookup"><span data-stu-id="6a329-111">Network Element</span></span></th>
<th><span data-ttu-id="6a329-112">必要な列</span><span class="sxs-lookup"><span data-stu-id="6a329-112">Required Columns</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6a329-113"><strong>ワイヤレス アクセス ポイント</strong></span><span class="sxs-lookup"><span data-stu-id="6a329-113"><strong>Wireless access point</strong></span></span></p></td>
<td><p><span data-ttu-id="6a329-114">&lt;BSSID &gt; 、 &lt; 説明 &gt; 、 &lt; 場所 &gt; 、 &lt; CompanyName &gt; 、 &lt; HouseNumber &gt; 、 &lt; HouseNumberSuffix &gt; 、 &lt; predirectional &gt; ,...</span><span class="sxs-lookup"><span data-stu-id="6a329-114">&lt;BSSID&gt;,&lt;Description&gt;,&lt;Location&gt;,&lt;CompanyName&gt;,&lt;HouseNumber&gt;,&lt;HouseNumberSuffix&gt;,&lt;PreDirectional&gt;,…</span></span></p>
<p><span data-ttu-id="6a329-115">... &lt;StreetName &gt; 、 &lt; StreetSuffix &gt; 、 &lt; postdirectional &gt; 、 &lt; 市区町村 &gt; 、 &lt; 都道府県、 &gt; &lt; 郵便 &gt; &lt; 番号、国&gt;</span><span class="sxs-lookup"><span data-stu-id="6a329-115">…&lt;StreetName&gt;,&lt;StreetSuffix&gt;,&lt;PostDirectional&gt;,&lt;City&gt;,&lt;State&gt;,&lt;PostalCode&gt;,&lt;Country&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a329-116"><strong>Subnet</strong></span><span class="sxs-lookup"><span data-stu-id="6a329-116"><strong>Subnet</strong></span></span></p></td>
<td><p><span data-ttu-id="6a329-117">&lt;サブネット &gt; 、 &lt; 説明 &gt; 、 &lt; 場所 &gt; 、 &lt; CompanyName &gt; 、 &lt; HouseNumber &gt; 、 &lt; HouseNumberSuffix &gt; 、 &lt; predirectional &gt; ,...</span><span class="sxs-lookup"><span data-stu-id="6a329-117">&lt;Subnet&gt;,&lt;Description&gt;,&lt;Location&gt;,&lt;CompanyName&gt;,&lt;HouseNumber&gt;,&lt;HouseNumberSuffix&gt;,&lt;PreDirectional&gt;,…</span></span></p>
<p><span data-ttu-id="6a329-118">... &lt;StreetName &gt; 、 &lt; StreetSuffix &gt; 、 &lt; postdirectional &gt; 、 &lt; 市区町村 &gt; 、 &lt; 都道府県、 &gt; &lt; 郵便 &gt; &lt; 番号、国&gt;</span><span class="sxs-lookup"><span data-stu-id="6a329-118">…&lt;StreetName&gt;,&lt;StreetSuffix&gt;,&lt;PostDirectional&gt;,&lt;City&gt;,&lt;State&gt;,&lt;PostalCode&gt;,&lt;Country&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a329-119"><strong>ポート</strong></span><span class="sxs-lookup"><span data-stu-id="6a329-119"><strong>Port</strong></span></span></p></td>
<td><p><span data-ttu-id="6a329-120">&lt;ChPortIDSubType Sid &gt; 、 &lt; &gt; 、 &lt; PortID &gt; 、 &lt; Description &gt; 、 &lt; Location &gt; 、 &lt; CompanyName &gt; 、 &lt; HouseNumber &gt; 、 &lt; HouseNumberSuffix &gt; ,...</span><span class="sxs-lookup"><span data-stu-id="6a329-120">&lt;ChassisID&gt;,&lt;PortIDSubType&gt;,&lt;PortID&gt;,&lt;Description&gt;,&lt;Location&gt;,&lt;CompanyName&gt;,&lt;HouseNumber&gt;,&lt;HouseNumberSuffix&gt;,…</span></span></p>
<p><span data-ttu-id="6a329-121">... &lt;PreDirectional &gt; 、 &lt; StreetName &gt; 、 &lt; StreetSuffix &gt; 、 &lt; &gt; postdirectional &lt; 市区町村 &gt; 、 &lt; 都道府県 &gt; 、 &lt; 郵便 &gt; &lt; 番号、国&gt;</span><span class="sxs-lookup"><span data-stu-id="6a329-121">…&lt;PreDirectional&gt;,&lt;StreetName&gt;,&lt;StreetSuffix&gt;,&lt;PostDirectional&gt;,&lt;City&gt;,&lt;State&gt;,&lt;PostalCode&gt;,&lt;Country&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a329-122"><strong>スイッチ</strong></span><span class="sxs-lookup"><span data-stu-id="6a329-122"><strong>Switch</strong></span></span></p></td>
<td><p><span data-ttu-id="6a329-123">&lt;ChHouseNumber Sid &gt; 、 &lt; 説明 &gt; 、 &lt; 場所 &gt; 、 &lt; CompanyName &gt; 、 &lt; &gt; 、 &lt; HouseNumberSuffix &gt; 、 &lt; predirectional &gt; ,...</span><span class="sxs-lookup"><span data-stu-id="6a329-123">&lt;ChassisID&gt;,&lt;Description&gt;,&lt;Location&gt;,&lt;CompanyName&gt;,&lt;HouseNumber&gt;,&lt;HouseNumberSuffix&gt;,&lt;PreDirectional&gt;,…</span></span></p>
<p><span data-ttu-id="6a329-124">... &lt;StreetName &gt; 、 &lt; StreetSuffix &gt; 、 &lt; postdirectional &gt; 、 &lt; 市区町村 &gt; 、 &lt; 都道府県、 &gt; &lt; 郵便 &gt; &lt; 番号、国&gt;</span><span class="sxs-lookup"><span data-stu-id="6a329-124">…&lt;StreetName&gt;,&lt;StreetSuffix&gt;,&lt;PostDirectional&gt;,&lt;City&gt;,&lt;State&gt;,&lt;PostalCode&gt;,&lt;Country&gt;</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6a329-125">場所のデータベースに情報を読み込んでいない場合に、場所のポリシーの **[場所 (必須)]** を **[はい]** または **[免責事項]** に設定すると、クライアントから場所の情報を手動で入力するように指示されます。</span><span class="sxs-lookup"><span data-stu-id="6a329-125">If you do not populate the location database, and the **Location Required** in the Location Policy is set to **Yes** or **Disclaimer**, the client will prompt the user to enter a location manually.</span></span>

<span data-ttu-id="6a329-126">場所データベースの設定の詳細については、次のコマンドレットの Lync Server 管理シェルに関するドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6a329-126">For details about populating the location database, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - <span data-ttu-id="6a329-127">**Get-CsLisSubnet**</span><span class="sxs-lookup"><span data-stu-id="6a329-127">**Get-CsLisSubnet**</span></span>

  - <span data-ttu-id="6a329-128">**Set-CsLisSubnet**</span><span class="sxs-lookup"><span data-stu-id="6a329-128">**Set-CsLisSubnet**</span></span>

  - <span data-ttu-id="6a329-129">Remove-CsLisSubnet</span><span class="sxs-lookup"><span data-stu-id="6a329-129">Remove-CsLisSubnet</span></span>

  - <span data-ttu-id="6a329-130">**Get-CsLisWirelessAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="6a329-130">**Get-CsLisWirelessAccessPoint**</span></span>

  - <span data-ttu-id="6a329-131">**Set-CsLisWirelessAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="6a329-131">**Set-CsLisWirelessAccessPoint**</span></span>

  - <span data-ttu-id="6a329-132">**Remove-CsLisWirelessAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="6a329-132">**Remove-CsLisWirelessAccessPoint**</span></span>

  - <span data-ttu-id="6a329-133">**Get-CsLisSwitch**</span><span class="sxs-lookup"><span data-stu-id="6a329-133">**Get-CsLisSwitch**</span></span>

  - <span data-ttu-id="6a329-134">**Set-CsLisSwitch**</span><span class="sxs-lookup"><span data-stu-id="6a329-134">**Set-CsLisSwitch**</span></span>

  - <span data-ttu-id="6a329-135">**Remove-CsLisSwitch**</span><span class="sxs-lookup"><span data-stu-id="6a329-135">**Remove-CsLisSwitch**</span></span>

  - <span data-ttu-id="6a329-136">**Get-CsLisPort**</span><span class="sxs-lookup"><span data-stu-id="6a329-136">**Get-CsLisPort**</span></span>

  - <span data-ttu-id="6a329-137">**Set-CsLisPort**</span><span class="sxs-lookup"><span data-stu-id="6a329-137">**Set-CsLisPort**</span></span>

  - <span data-ttu-id="6a329-138">**Remove-CsLisPort**</span><span class="sxs-lookup"><span data-stu-id="6a329-138">**Remove-CsLisPort**</span></span>

<div>

## <a name="to-add-network-elements-to-the-location-database"></a><span data-ttu-id="6a329-139">ネットワーク要素を場所のデータベースに追加するには</span><span class="sxs-lookup"><span data-stu-id="6a329-139">To add network elements to the location database</span></span>

1.  <span data-ttu-id="6a329-140">次のコマンドレットを実行して、サブネットの場所を場所データベースに追加します。</span><span class="sxs-lookup"><span data-stu-id="6a329-140">Run the following cmdlet to add a subnet location to the location database.</span></span>
    
        Set-CsLisSubnet -Subnet 157.56.66.0 -Description "Subnet 1" -Location Location1 -CompanyName "Litware" -HouseNumber 1234 -HouseNumberSuffix "" -PreDirectional "" -StreetName 163rd -StreetSuffix Ave -PostDirectional NE -City Redmond -State WA -PostalCode 99123 -Country US
    
    <span data-ttu-id="6a329-p103">ELIN ゲートウェイでは、ELIN を CompanyName フィールドに入れます。複数の ELIN を含めることもできます。次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="6a329-p103">For ELIN gateways, put the ELIN in the CompanyName field. You can include more than one ELIN. For example:</span></span>
    
        Set-CsLisSubnet -Subnet 157.56.66.0 -Description "Subnet 1" -Location Location1 -CompanyName 425-555-0100; 425-555-0200; 425-555-0300 -HouseNumber 1234 -HouseNumberSuffix "" -PreDirectional "" -StreetName 163rd -StreetSuffix Ave -PostDirectional NE -City Redmond -State WA -PostalCode 99123 -Country US
    
    <span data-ttu-id="6a329-144">また、"subnets.csv" という名前のファイルを使用して、次のコマンドレットでサブネットの場所を一括で更新することができます。</span><span class="sxs-lookup"><span data-stu-id="6a329-144">Alternately, you can run the following cmdlets and use a file named "subnets.csv" to bulk update subnet locations.</span></span>
    
        $g = Import-Csv subnets.csv
        $g | Set-CsLisSubnet

2.  <span data-ttu-id="6a329-145">次のコマンドレットを実行して、ワイヤレスの場所を場所データベースに追加します。</span><span class="sxs-lookup"><span data-stu-id="6a329-145">Run the following cmdlet to add wireless locations to the location database.</span></span>
    
        Set-CsLisWirelessAccessPoint -BSSID 0A-23-CD-16-AA-2E -Description "Wireless1" -Location Location2 -CompanyName "Litware" -HouseNumber 2345 -HouseNumberSuffix "" -PreDirectional "" -StreetName 163rd -StreetSuffix Ave -PostDirectional NE -City Bellevue -State WA -PostalCode 99234 -Country US
    
    <span data-ttu-id="6a329-146">また、"waps.csv" という名前のファイルを使用して、次のコマンドレットでワイヤレスの場所を一括で更新することもできます。</span><span class="sxs-lookup"><span data-stu-id="6a329-146">Alternately, you can run the following cmdlets and use a file named "waps.csv" to bulk update wireless locations.</span></span>
    
        $g = Import-Csv waps.csv
        $g | Set-CsLisWirelessAccessPoint

3.  <span data-ttu-id="6a329-147">次のコマンドレットを実行して、スイッチの場所を場所データベースに追加します。</span><span class="sxs-lookup"><span data-stu-id="6a329-147">Run the following cmdlet to add switch locations to the location database.</span></span>
    
        Set-CsLisSwitch-ChassisID 0B-23-CD-16-AA-BB -Description "Switch1" -Location Location1 -CompanyName "Litware" -HouseNumber 1234 -HouseNumberSuffix "" -PreDirectional "" -StreetName 163rd -StreetSuffix Ave -PostDirectional NE -City Redmond -State WA -PostalCode 99123 -Country US
    
    <span data-ttu-id="6a329-148">また、"switches.csv" という名前のファイルを使用して、次のコマンドレットでスイッチの場所を一括で更新することもできます。</span><span class="sxs-lookup"><span data-stu-id="6a329-148">Alternately, you can run the following cmdlets and use a file named "switches.csv" to bulk update switch locations.</span></span>
    
        $g = Import-Csv switches.csv
        $g | Set-CsLisSwitch

4.  <span data-ttu-id="6a329-149">次のコマンドレットを実行して、ポートの場所を場所データベースに追加します。</span><span class="sxs-lookup"><span data-stu-id="6a329-149">Run the following cmdlet to add port locations to the location database</span></span>
    
        Set-CsLisPort -ChassisID 0C-23-CD-16-AA-CC -PortID 0A-abcd -Description "Port1" -Location Location2 -CompanyName "Litware" -HouseNumber 2345 -HouseNumberSuffix "" -PreDirectional "" -StreetName 163rd -StreetSuffix Ave -PostDirectional NE -City Bellevue -State WA -PostalCode 99234 -Country US
    
    <span data-ttu-id="6a329-p104">PortIDSubType の既定値は、LocallyAssigned です。これを、InterfaceAlias または InterfaceName に設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="6a329-p104">The default for PortIDSubType is LocallyAssigned. You can also set it to InterfaceAlias or InterfaceName</span></span>
    
    <span data-ttu-id="6a329-152">また、"ports.csv" という名前のファイルを使用して、次のコマンドレットでポートの場所を一括で更新することもできます。</span><span class="sxs-lookup"><span data-stu-id="6a329-152">Alternately, you can run the following cmdlets and use a file named "ports.csv" to bulk update port locations.</span></span>
    
        $g = Import-Csv ports.csv
        $g | Set-CsLisPort

<span data-ttu-id="6a329-153"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6a329-153"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

