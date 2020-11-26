---
title: 'Lync Server 2013: アドレス帳サービスの管理'
description: 'Lync Server 2013: アドレス帳サービスを管理しています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Administering the Address Book Service
ms:assetid: 801e4243-9670-4477-aa2f-88b61ecf5351
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429711(v=OCS.15)
ms:contentKeyID: 48184649
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 86d549b06b5c6ac1c450edf9e7edb0b902ef9adf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440697"
---
# <a name="administering-the-address-book-service-in-lync-server-2013"></a><span data-ttu-id="8984c-103">Lync Server 2013 でのアドレス帳サービスの管理</span><span class="sxs-lookup"><span data-stu-id="8984c-103">Administering the Address Book Service in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8984c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8984c-104">

<span> </span></span></span>

<span data-ttu-id="8984c-105">_**最終更新日:** 2014-02-05_</span><span class="sxs-lookup"><span data-stu-id="8984c-105">_**Topic Last Modified:** 2014-02-05_</span></span>

<span data-ttu-id="8984c-106">Lync Server Enterprise Edition または Standard Edition サーバーの展開の一部として、アドレス帳サービスは既定でインストールされています。</span><span class="sxs-lookup"><span data-stu-id="8984c-106">As a part of the deployment of Lync Server, Enterprise Edition or Standard Edition server, the Address Book Service is installed by default.</span></span> <span data-ttu-id="8984c-107">アドレス帳サービス– RTCab によって使用されたデータベースは、SQL Server (Enterprise Edition) に作成されます。これは、sql server (標準エディションサーバーの場合は、sql Server の場合は併置されます) のバックエンド SQL Server です。</span><span class="sxs-lookup"><span data-stu-id="8984c-107">The database used by the Address Book Service – RTCab – is created on the SQL Server (for Enterprise Edition, this is the back-end SQL Server; for Standard Edition server, the collocated SQL Server).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8984c-108"><STRONG>Adsi エディター</STRONG>を使用して Active Directory ドメインサービスオブジェクトの属性を編集する方法について詳しくは、「 <A href="https://go.microsoft.com/fwlink/?linkid=330427">adsi edit</A>」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="8984c-108">For information about using <STRONG>ADSI Edit</STRONG> to edit Active Directory Domain Services object attributes, see <A href="https://go.microsoft.com/fwlink/?linkid=330427">ADSI Edit</A>.</span></span> <span data-ttu-id="8984c-109">アドレス帳サービス専用のリソースキットに含まれるツールの詳細については、「 <A href="https://go.microsoft.com/fwlink/?linkid=330429">Microsoft Lync Server 2013 リソースキットツール</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8984c-109">For information about a tool in the Resource Kit specifically for the Address Book service, see <A href="https://go.microsoft.com/fwlink/?linkid=330429">Microsoft Lync Server 2013 Resource Kit Tools</A>.</span></span>



</div>

<div>

## <a name="address-book-server-phone-number-normalization"></a><span data-ttu-id="8984c-110">アドレス帳のサーバー電話番号の正規化</span><span class="sxs-lookup"><span data-stu-id="8984c-110">Address Book Server Phone Number Normalization</span></span>

<span data-ttu-id="8984c-111">Lync Server では、標準化された RFC 3966/E.i 電話番号が必要です。</span><span class="sxs-lookup"><span data-stu-id="8984c-111">Lync Server requires standardized RFC 3966/E.164 phone numbers.</span></span> <span data-ttu-id="8984c-112">非構造化または一貫性のない電話番号を使用するために、Lync Server はアドレス帳サーバーに依存して、正規化ルールに渡される前に電話番号の前処理を行います。</span><span class="sxs-lookup"><span data-stu-id="8984c-112">To use phone numbers that are unstructured or inconsistently formatted, Lync Server relies on the Address Book Server to preprocess phone numbers before they are handed off to the normalization rules.</span></span> <span data-ttu-id="8984c-113">アドレス帳から電話番号を使用し、正規化ルールが適用されている場合、Lync Phone Edition や Lync Mobile などのクライアントでは、これらの正規化された数値を使用できます。</span><span class="sxs-lookup"><span data-stu-id="8984c-113">When a phone number is used from the address book and the normalization rule is applied, clients, such as Lync Phone Edition and Lync Mobile, can use these normalized numbers.</span></span>

<span data-ttu-id="8984c-114">以前のバージョンで使用されていた正規化ルールは、一部の調整なしで適切に動作しないことがあります。</span><span class="sxs-lookup"><span data-stu-id="8984c-114">The normalization rules that were used in previous versions may not work properly without some adjustments.</span></span> <span data-ttu-id="8984c-115">正規表現の規則を適用する前に空白文字と必須でない文字は削除されているため、regex 式が、削除されたダッシュや他の文字を探している場合は、正規化ルールが失敗する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8984c-115">Because the white space and non-mandatory characters are removed prior to the normalization rules, if your regex expression is specifically looking for a dash or other character that was removed, your normalization rule might fail.</span></span> <span data-ttu-id="8984c-116">正規化ルールを確認して、必須以外の文字を探していないことを確認するか、またはルールが適切に処理されないようにして、その文字が存在しないという問題が発生した場合は、そのルールが適切でないことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8984c-116">You should review your normalization rules to ensure that either they are not looking for these non-mandatory characters, or that the rule can fail gracefully and continue in the event that the character is not present where the rule anticipates it will be.</span></span>

</div>

<div>

## <a name="user-replicator-and-address-book-server"></a><span data-ttu-id="8984c-117">ユーザーレプリケーターおよびアドレス帳サーバー</span><span class="sxs-lookup"><span data-stu-id="8984c-117">User Replicator and Address Book Server</span></span>

<span data-ttu-id="8984c-118">アドレス帳サーバーは、ユーザーレプリケーターによって提供されたデータを使用して、最初にグローバルアドレス一覧 (GAL) から取得した情報を更新します。</span><span class="sxs-lookup"><span data-stu-id="8984c-118">The Address Book Server uses data provided by User Replicator to update the information that it initially obtains from the global address list (GAL).</span></span> <span data-ttu-id="8984c-119">ユーザーレプリケーターは、各ユーザー、連絡先、グループの Active Directory ドメインサービスの属性をデータベースの AbUserEntry テーブルに書き込み、アドレス帳サーバーは、データベースのユーザーデータをアドレス帳サーバーファイルストア内のファイルに、アドレス帳データベース RTCab に同期します。</span><span class="sxs-lookup"><span data-stu-id="8984c-119">User Replicator writes the Active Directory Domain Services attributes for each user, contact, and group into the AbUserEntry table in the database and the Address Book Server syncs the user data from the database into files in the Address Book Server file store and into the Address Book database RTCab.</span></span> <span data-ttu-id="8984c-120">AbUserEntry テーブルのスキーマでは、 **Userguid** と **UserData** の2つの列を使用します。</span><span class="sxs-lookup"><span data-stu-id="8984c-120">The schema for the AbUserEntry table uses two columns, **UserGuid** and **UserData**.</span></span> <span data-ttu-id="8984c-121">**Userguid** はインデックス列で、Active Directory オブジェクトの16バイトの GUID が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8984c-121">**UserGuid** is the index column and contains the 16-byte GUID of the Active Directory object.</span></span> <span data-ttu-id="8984c-122">**UserData** は、前に説明した、その連絡先の Active Directory ドメインサービスのすべての属性を含む image 列です。</span><span class="sxs-lookup"><span data-stu-id="8984c-122">**UserData** is an image column which contains all of the previously mentioned Active Directory Domain Services attributes for that contact.</span></span>

<span data-ttu-id="8984c-123">ユーザーレプリケーターは、AbUserEntry テーブルと同じ SQL Server ベースのインスタンスにある構成テーブルを読み取ることによって、どの Active Directory 属性を作成するかを決定します。</span><span class="sxs-lookup"><span data-stu-id="8984c-123">User Replicator determines which Active Directory attributes to write by reading a configuration table located in the same SQL Server-based instance as the AbUserEntry table.</span></span> <span data-ttu-id="8984c-124">AbAttribute テーブルには、 **ID**、 **Name**、 **Flags**、および **Enable** という3つの列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8984c-124">The AbAttribute table contains three columns, **ID**, **Name**, **Flags**, and **Enable**.</span></span> <span data-ttu-id="8984c-125">データベースのセットアップ中にテーブルが作成されます。</span><span class="sxs-lookup"><span data-stu-id="8984c-125">The table is created during database setup.</span></span> <span data-ttu-id="8984c-126">AbAttribute テーブルが空の場合、ユーザーレプリケーターは AbUserEntry テーブル処理ロジックをスキップします。</span><span class="sxs-lookup"><span data-stu-id="8984c-126">If the AbAttribute table is empty, User Replicator skips its AbUserEntry table processing logic.</span></span> <span data-ttu-id="8984c-127">アドレス帳のサーバー属性は動的であり、AbAttribute テーブルから取得されます。これは、アドレス帳サーバーがアクティブ化されたときに、最初にアドレス帳サーバーによって作成されます。</span><span class="sxs-lookup"><span data-stu-id="8984c-127">Address Book Server attributes are dynamic and are retrieved from the AbAttribute table, which is initially written by the Address Book Server when the Address Book Server is activated.</span></span>

<span data-ttu-id="8984c-128">アドレス帳サーバーのアクティブ化によって、次の表に示す値を含む AbAttribute テーブルが設定されます。</span><span class="sxs-lookup"><span data-stu-id="8984c-128">Address Book Server activation populates the AbAttribute table with the values shown in the following table.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8984c-129">ID</span><span class="sxs-lookup"><span data-stu-id="8984c-129">ID</span></span></th>
<th><span data-ttu-id="8984c-130">名前</span><span class="sxs-lookup"><span data-stu-id="8984c-130">Name</span></span></th>
<th><span data-ttu-id="8984c-131">フラグ</span><span class="sxs-lookup"><span data-stu-id="8984c-131">Flags</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8984c-132">1</span><span class="sxs-lookup"><span data-stu-id="8984c-132">1</span></span></p></td>
<td><p><span data-ttu-id="8984c-133">一定</span><span class="sxs-lookup"><span data-stu-id="8984c-133">givenName</span></span></p></td>
<td><p><span data-ttu-id="8984c-134">0x01400000</span><span class="sxs-lookup"><span data-stu-id="8984c-134">0x01400000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8984c-135">2</span><span class="sxs-lookup"><span data-stu-id="8984c-135">2</span></span></p></td>
<td><p><span data-ttu-id="8984c-136">Sn</span><span class="sxs-lookup"><span data-stu-id="8984c-136">Sn</span></span></p></td>
<td><p><span data-ttu-id="8984c-137">0x02400000</span><span class="sxs-lookup"><span data-stu-id="8984c-137">0x02400000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8984c-138">3</span><span class="sxs-lookup"><span data-stu-id="8984c-138">3</span></span></p></td>
<td><p><span data-ttu-id="8984c-139">displayName</span><span class="sxs-lookup"><span data-stu-id="8984c-139">displayName</span></span></p></td>
<td><p><span data-ttu-id="8984c-140">0x03420000</span><span class="sxs-lookup"><span data-stu-id="8984c-140">0x03420000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8984c-141">4</span><span class="sxs-lookup"><span data-stu-id="8984c-141">4</span></span></p></td>
<td><p><span data-ttu-id="8984c-142">タイトル</span><span class="sxs-lookup"><span data-stu-id="8984c-142">Title</span></span></p></td>
<td><p><span data-ttu-id="8984c-143">0x04000000</span><span class="sxs-lookup"><span data-stu-id="8984c-143">0x04000000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8984c-144">5</span><span class="sxs-lookup"><span data-stu-id="8984c-144">5</span></span></p></td>
<td><p><span data-ttu-id="8984c-145">mailNickname</span><span class="sxs-lookup"><span data-stu-id="8984c-145">mailNickname</span></span></p></td>
<td><p><span data-ttu-id="8984c-146">0x05400000</span><span class="sxs-lookup"><span data-stu-id="8984c-146">0x05400000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8984c-147">6</span><span class="sxs-lookup"><span data-stu-id="8984c-147">6</span></span></p></td>
<td><p><span data-ttu-id="8984c-148">貴社</span><span class="sxs-lookup"><span data-stu-id="8984c-148">Company</span></span></p></td>
<td><p><span data-ttu-id="8984c-149">0x06000000</span><span class="sxs-lookup"><span data-stu-id="8984c-149">0x06000000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8984c-150">7</span><span class="sxs-lookup"><span data-stu-id="8984c-150">7</span></span></p></td>
<td><p><span data-ttu-id="8984c-151">Physicaldeliveryのお Ename</span><span class="sxs-lookup"><span data-stu-id="8984c-151">physicalDeliveryOfficeName</span></span></p></td>
<td><p><span data-ttu-id="8984c-152">0x07000000</span><span class="sxs-lookup"><span data-stu-id="8984c-152">0x07000000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8984c-153">個</span><span class="sxs-lookup"><span data-stu-id="8984c-153">8</span></span></p></td>
<td><p><span data-ttu-id="8984c-154">msRTCSIP-PrimaryUserAddress</span><span class="sxs-lookup"><span data-stu-id="8984c-154">msRTCSIP-PrimaryUserAddress</span></span></p></td>
<td><p><span data-ttu-id="8984c-155">0x08520C00</span><span class="sxs-lookup"><span data-stu-id="8984c-155">0x08520C00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8984c-156">ファイブ</span><span class="sxs-lookup"><span data-stu-id="8984c-156">9</span></span></p></td>
<td><p><span data-ttu-id="8984c-157">telephoneNumber</span><span class="sxs-lookup"><span data-stu-id="8984c-157">telephoneNumber</span></span></p></td>
<td><p><span data-ttu-id="8984c-158">0x09022800</span><span class="sxs-lookup"><span data-stu-id="8984c-158">0x09022800</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8984c-159">常用</span><span class="sxs-lookup"><span data-stu-id="8984c-159">10</span></span></p></td>
<td><p><span data-ttu-id="8984c-160">homePhone</span><span class="sxs-lookup"><span data-stu-id="8984c-160">homePhone</span></span></p></td>
<td><p><span data-ttu-id="8984c-161">0x0A302800</span><span class="sxs-lookup"><span data-stu-id="8984c-161">0x0A302800</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8984c-162">折り</span><span class="sxs-lookup"><span data-stu-id="8984c-162">11</span></span></p></td>
<td><p><span data-ttu-id="8984c-163">モバイル</span><span class="sxs-lookup"><span data-stu-id="8984c-163">Mobile</span></span></p></td>
<td><p><span data-ttu-id="8984c-164">0x0B622800</span><span class="sxs-lookup"><span data-stu-id="8984c-164">0x0B622800</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8984c-165">以内</span><span class="sxs-lookup"><span data-stu-id="8984c-165">12</span></span></p></td>
<td><p><span data-ttu-id="8984c-166">その他の電話</span><span class="sxs-lookup"><span data-stu-id="8984c-166">otherTelephone</span></span></p></td>
<td><p><span data-ttu-id="8984c-167">0x0C302000</span><span class="sxs-lookup"><span data-stu-id="8984c-167">0x0C302000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8984c-168">14</span><span class="sxs-lookup"><span data-stu-id="8984c-168">13</span></span></p></td>
<td><p><span data-ttu-id="8984c-169">ipPhone</span><span class="sxs-lookup"><span data-stu-id="8984c-169">ipPhone</span></span></p></td>
<td><p><span data-ttu-id="8984c-170">0x0D302000</span><span class="sxs-lookup"><span data-stu-id="8984c-170">0x0D302000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8984c-171">14</span><span class="sxs-lookup"><span data-stu-id="8984c-171">14</span></span></p></td>
<td><p><span data-ttu-id="8984c-172">添付</span><span class="sxs-lookup"><span data-stu-id="8984c-172">Mail</span></span></p></td>
<td><p><span data-ttu-id="8984c-173">0x0E500000</span><span class="sxs-lookup"><span data-stu-id="8984c-173">0x0E500000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8984c-174">マート</span><span class="sxs-lookup"><span data-stu-id="8984c-174">15</span></span></p></td>
<td><p><span data-ttu-id="8984c-175">groupType</span><span class="sxs-lookup"><span data-stu-id="8984c-175">groupType</span></span></p></td>
<td><p><span data-ttu-id="8984c-176">0x0F010800</span><span class="sxs-lookup"><span data-stu-id="8984c-176">0x0F010800</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8984c-177">16</span><span class="sxs-lookup"><span data-stu-id="8984c-177">16</span></span></p></td>
<td><p><span data-ttu-id="8984c-178">各部</span><span class="sxs-lookup"><span data-stu-id="8984c-178">Department</span></span></p></td>
<td><p><span data-ttu-id="8984c-179">0x10000000</span><span class="sxs-lookup"><span data-stu-id="8984c-179">0x10000000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8984c-180">18</span><span class="sxs-lookup"><span data-stu-id="8984c-180">17</span></span></p></td>
<td><p><span data-ttu-id="8984c-181">説明</span><span class="sxs-lookup"><span data-stu-id="8984c-181">Description</span></span></p></td>
<td><p><span data-ttu-id="8984c-182">0x11000100</span><span class="sxs-lookup"><span data-stu-id="8984c-182">0x11000100</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8984c-183">才</span><span class="sxs-lookup"><span data-stu-id="8984c-183">18</span></span></p></td>
<td><p><span data-ttu-id="8984c-184">上司</span><span class="sxs-lookup"><span data-stu-id="8984c-184">Manager</span></span></p></td>
<td><p><span data-ttu-id="8984c-185">0x12040001</span><span class="sxs-lookup"><span data-stu-id="8984c-185">0x12040001</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8984c-186">#</span><span class="sxs-lookup"><span data-stu-id="8984c-186">19</span></span></p></td>
<td><p><span data-ttu-id="8984c-187">た proxyaddress</span><span class="sxs-lookup"><span data-stu-id="8984c-187">proxyAddress</span></span></p></td>
<td><p><span data-ttu-id="8984c-188">0x00500105</span><span class="sxs-lookup"><span data-stu-id="8984c-188">0x00500105</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8984c-189">超える</span><span class="sxs-lookup"><span data-stu-id="8984c-189">20</span></span></p></td>
<td><p><span data-ttu-id="8984c-190">msExchHideFromAddressLists</span><span class="sxs-lookup"><span data-stu-id="8984c-190">msExchHideFromAddressLists</span></span></p></td>
<td><p><span data-ttu-id="8984c-191">0xFF000003</span><span class="sxs-lookup"><span data-stu-id="8984c-191">0xFF000003</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8984c-192">99</span><span class="sxs-lookup"><span data-stu-id="8984c-192">99</span></span></p></td>
<td><p><span data-ttu-id="8984c-193">Id</span><span class="sxs-lookup"><span data-stu-id="8984c-193">entryID</span></span></p></td>
<td><p><span data-ttu-id="8984c-194">0x99000000</span><span class="sxs-lookup"><span data-stu-id="8984c-194">0x99000000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8984c-195">**ID** 列の数値は一意である必要があり、再利用することは避けてください。</span><span class="sxs-lookup"><span data-stu-id="8984c-195">The numbers in the **ID** column must be unique and should never be reused.</span></span> <span data-ttu-id="8984c-196">また、256の ID 値を保持すると、アドレス帳サーバーによって書き込まれた出力ファイル内のスペースが節約されます。</span><span class="sxs-lookup"><span data-stu-id="8984c-196">Also, keeping the ID values under 256 saves space in the output files written by the Address Book Server.</span></span> <span data-ttu-id="8984c-197">ただし、ID の最大値は65535です。</span><span class="sxs-lookup"><span data-stu-id="8984c-197">However, the maximum ID value is 65535.</span></span> <span data-ttu-id="8984c-198">**Name** 列は、ユーザーレプリケーターが各連絡先の AbUserEntry テーブルに配置する Active Directory 属性名に対応しています。</span><span class="sxs-lookup"><span data-stu-id="8984c-198">The **Name** column corresponds to the Active Directory attribute name that User Replicator should put in the AbUserEntry table for each contact.</span></span> <span data-ttu-id="8984c-199">**Flags** 列の値は、属性の型を定義するために使われます。</span><span class="sxs-lookup"><span data-stu-id="8984c-199">The value in the **Flags** column is used to define the type of attribute.</span></span> <span data-ttu-id="8984c-200">次の種類のアドレス帳サーバー属性は、 **Flags** 列の値の下位バイトで示されるユーザーレプリケーターによって認識されます。</span><span class="sxs-lookup"><span data-stu-id="8984c-200">The following types of Address Book Server attributes are recognized by User Replicator, indicated by the low byte of the value in the **Flags** column.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8984c-201">属性</span><span class="sxs-lookup"><span data-stu-id="8984c-201">Attribute</span></span></th>
<th><span data-ttu-id="8984c-202">説明</span><span class="sxs-lookup"><span data-stu-id="8984c-202">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8984c-203">100</span><span class="sxs-lookup"><span data-stu-id="8984c-203">0x0</span></span></p></td>
<td><p><span data-ttu-id="8984c-204">文字列属性。</span><span class="sxs-lookup"><span data-stu-id="8984c-204">A string attribute.</span></span> <span data-ttu-id="8984c-205">ユーザーレプリケーターは、AbUserEntry テーブルに保存する前に、この型を UTF-8 に変換します。</span><span class="sxs-lookup"><span data-stu-id="8984c-205">User Replicator converts this type to UTF-8 before storing it in the AbUserEntry table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8984c-206">0x1</span><span class="sxs-lookup"><span data-stu-id="8984c-206">0x1</span></span></p></td>
<td><p><span data-ttu-id="8984c-207">バイナリ属性。</span><span class="sxs-lookup"><span data-stu-id="8984c-207">A binary attribute.</span></span> <span data-ttu-id="8984c-208">ユーザーレプリケーターは、変換せずに blob にこれを格納します。</span><span class="sxs-lookup"><span data-stu-id="8984c-208">User Replicator stores this in the blob without any conversion.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8984c-209">0x2</span><span class="sxs-lookup"><span data-stu-id="8984c-209">0x2</span></span></p></td>
<td><p><span data-ttu-id="8984c-210">文字列属性。ただし、属性値が tel: で始まる場合にのみ含まれ &quot; &quot; ます。</span><span class="sxs-lookup"><span data-stu-id="8984c-210">A string attribute, but is included only if the attribute value begins with &quot;tel:&quot;.</span></span> <span data-ttu-id="8984c-211">これは主に、複数値を持つ文字列属性 (具体的には <strong>proxyAddresses</strong>です。</span><span class="sxs-lookup"><span data-stu-id="8984c-211">This is primarily for multi-valued string attributes, specifically <strong>proxyAddresses</strong>.</span></span> <span data-ttu-id="8984c-212">この場合、アドレス帳サーバーは、tel: で始まる <strong>proxyAddresses</strong> エントリのみに注目し &quot; &quot; ます。</span><span class="sxs-lookup"><span data-stu-id="8984c-212">In this case, Address Book Server is interested only in <strong>proxyAddresses</strong> entries that begin with &quot;tel:&quot;.</span></span> <span data-ttu-id="8984c-213">したがって、スペース節約のために、ユーザーレプリケーターには tel: で始まるエントリのみが格納され &quot; &quot; ます。</span><span class="sxs-lookup"><span data-stu-id="8984c-213">Therefore, in the interest of saving space, User Replicator stores only the entries that begin with &quot;tel:&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8984c-214">0x3</span><span class="sxs-lookup"><span data-stu-id="8984c-214">0x3</span></span></p></td>
<td><p><span data-ttu-id="8984c-215">ブール文字列属性。 TRUE の場合、ユーザーレプリケーターは AbUserEntry テーブルにこの連絡先を含めません。</span><span class="sxs-lookup"><span data-stu-id="8984c-215">A Boolean string attribute, which if TRUE causes User Replicator to not include this contact in the AbUserEntry table.</span></span> <span data-ttu-id="8984c-216">FALSE の場合、ユーザーレプリケーターによってこの連絡先の属性が AbUserEntry テーブルに含まれますが、このフラグの特定の属性は含まれません。</span><span class="sxs-lookup"><span data-stu-id="8984c-216">If FALSE, it causes User Replicator to include the attributes for this contact in the AbUserEntry table, but not the particular attribute with this flag.</span></span> <span data-ttu-id="8984c-217">これは、主に <strong>msExchHideFromAddressLists</strong> 属性用の別の特殊なケースの型です。</span><span class="sxs-lookup"><span data-stu-id="8984c-217">This is another special case type that is primarily for the <strong>msExchHideFromAddressLists</strong> attribute.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8984c-218">0x4</span><span class="sxs-lookup"><span data-stu-id="8984c-218">0x4</span></span></p></td>
<td><p><span data-ttu-id="8984c-219">文字列属性。ただし、属性値が smtp で始まり、記号が含まれている場合にのみ含まれ &quot; &quot; &quot; @ &quot; ます。</span><span class="sxs-lookup"><span data-stu-id="8984c-219">A string attribute, but is included only if the attribute value begins with &quot;smtp:&quot; and includes the &quot;@&quot; symbol.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8984c-220">0x5</span><span class="sxs-lookup"><span data-stu-id="8984c-220">0x5</span></span></p></td>
<td><p><span data-ttu-id="8984c-221">文字列属性。ただし、属性値が &quot; tel: &quot; または smtp: のいずれかで始まり、その記号が含まれている場合にのみ含まれ &quot; &quot; &quot; @ &quot; ます。</span><span class="sxs-lookup"><span data-stu-id="8984c-221">A string attribute, but is included only if the attribute value begins with either &quot;tel:&quot; or &quot;smtp:&quot; and includes the &quot;@&quot; symbol.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8984c-222">0x100</span><span class="sxs-lookup"><span data-stu-id="8984c-222">0x100</span></span></p></td>
<td><p><span data-ttu-id="8984c-223">設定されている場合、これは複数値の属性であり、連絡先ごとに複数回表示することができます。</span><span class="sxs-lookup"><span data-stu-id="8984c-223">If set, this is a multi-valued attribute that can appear more than once for each contact.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8984c-224">0x400</span><span class="sxs-lookup"><span data-stu-id="8984c-224">0x400</span></span></p></td>
<td><p><span data-ttu-id="8984c-225">設定すると、連絡先のメールユーザーアカウント名の属性が識別されます。</span><span class="sxs-lookup"><span data-stu-id="8984c-225">If set, this identifies the email user account name attribute for a contact.</span></span> <span data-ttu-id="8984c-226">アドレス帳サーバーは、このフラグを使って、電話の正規化イベントログエントリに表示する属性値を特定します。</span><span class="sxs-lookup"><span data-stu-id="8984c-226">Address Book Server uses this flag to identify which attribute value to show in the phone normalization event log entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8984c-227">0x800</span><span class="sxs-lookup"><span data-stu-id="8984c-227">0x800</span></span></p></td>
<td><p><span data-ttu-id="8984c-228">設定すると、連絡先に必須の属性が指定します。</span><span class="sxs-lookup"><span data-stu-id="8984c-228">If set, this identifies a required attribute for a contact.</span></span> <span data-ttu-id="8984c-229">アドレス帳サーバーには、Active Directory にこの属性の値がある場合にのみ、AbUserEntry テーブルにユーザーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8984c-229">Address Book Server includes a user in the AbUserEntry table only if there is a value for this attribute in Active Directory.</span></span> <span data-ttu-id="8984c-230">必要な属性が複数ある場合は、そのうちの1つだけが、AbUserEntry テーブルにユーザーを含めるための値を持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="8984c-230">If there is more than one required attribute, only one of them is required to have a value to include the user in the AbUserEntry table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8984c-231">0x1000</span><span class="sxs-lookup"><span data-stu-id="8984c-231">0x1000</span></span></p></td>
<td><p><span data-ttu-id="8984c-232">設定されている場合、アドレス帳サーバーはこの属性の値を常に標準化します。</span><span class="sxs-lookup"><span data-stu-id="8984c-232">If set, Address Book Server always normalizes the value of this attribute.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8984c-233">0x2000</span><span class="sxs-lookup"><span data-stu-id="8984c-233">0x2000</span></span></p></td>
<td><p><span data-ttu-id="8984c-234">設定されている場合、 <strong>UseNormalizationRules</strong> CMS 設定が FALSE の場合、アドレス帳サーバーは<strong>proxyAddresses</strong>の正規化された数値を使用します。それ以外の場合は、フラグビットが0x1000 の場合と同じように動作します。</span><span class="sxs-lookup"><span data-stu-id="8984c-234">If set, Address Book Server uses the normalized number from <strong>proxyAddresses</strong>, if the <strong>UseNormalizationRules</strong> CMS setting is FALSE; otherwise it behaves the same as when the flag bit is 0x1000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8984c-235">0x4000</span><span class="sxs-lookup"><span data-stu-id="8984c-235">0x4000</span></span></p></td>
<td><p><span data-ttu-id="8984c-236">設定されている場合、アドレス帳サーバーには、指定した属性に対してこの値を持つ AbUserEntry テーブル内のオブジェクトは含まれません。</span><span class="sxs-lookup"><span data-stu-id="8984c-236">If set, Address Book Server does not include objects in the AbUserEntry table that have this value for the specified attribute.</span></span> <span data-ttu-id="8984c-237">たとえば、 <strong>msrtcsip-userenabled true-PrimaryUserAddress</strong> 属性にこのフラグビットが設定されている場合、この属性を持つ連絡先はデータベースに書き込まれません。</span><span class="sxs-lookup"><span data-stu-id="8984c-237">For example, if the <strong>msRTCSIP-PrimaryUserAddress</strong> attribute has this flag bit set, then contacts that have this attribute are not written to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8984c-238">0x8000</span><span class="sxs-lookup"><span data-stu-id="8984c-238">0x8000</span></span></p></td>
<td><p><span data-ttu-id="8984c-239">設定されている場合、アドレス帳サーバーには、指定した属性に対してこの値を持たない AbUserEntry テーブル内のオブジェクトは含まれません。</span><span class="sxs-lookup"><span data-stu-id="8984c-239">If set, Address Book Server does not include objects in the AbUserEntry table that do not have this value for the specified attribute.</span></span> <span data-ttu-id="8984c-240">オブジェクトに0x4000 と0x8000 の両方のフラグビットが設定されている場合は、フラグビット値が0x4000 に設定された属性が優先され、オブジェクトは AbUserEntry テーブルから除外されます。</span><span class="sxs-lookup"><span data-stu-id="8984c-240">If both the 0x4000 and 0x8000 flag bits are set on an object, the attribute with the flag bit value set to 0x4000 takes precedence, and the object is excluded from the AbUserEntry table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8984c-241">○</span><span class="sxs-lookup"><span data-stu-id="8984c-241">0x10000</span></span></p></td>
<td><p><span data-ttu-id="8984c-242">設定すると、グループオブジェクトを表します。</span><span class="sxs-lookup"><span data-stu-id="8984c-242">If set, this represents a group object.</span></span> <span data-ttu-id="8984c-243">ユーザーレプリケーターは、このフラグビットを使用して、 <strong>groupType</strong> 属性が設定された連絡先を含めます (たとえば、配布リストまたはセキュリティグループの場合)。</span><span class="sxs-lookup"><span data-stu-id="8984c-243">User Replicator uses this flag bit to include contacts with the <strong>groupType</strong> attribute whose presence indicates a group (for example, a distribution list or security group).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8984c-244">0x20000</span><span class="sxs-lookup"><span data-stu-id="8984c-244">0x20000</span></span></p></td>
<td><p><span data-ttu-id="8984c-245">設定されている場合、ユーザーレプリケーターはこのフラグビットを使って、デバイス固有のアドレス帳サーバーファイル (つまり、dabs 拡張子を持つファイル) にこの属性を含めます。</span><span class="sxs-lookup"><span data-stu-id="8984c-245">If set, User Replicator uses this flag bit to include this attribute in device-specific Address Book Server files (that is, files with a .dabs extension).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8984c-246">以前のバージョンの Lync Server で、Active Directory に変更を適用する場合、管理者は、Lync Server ユーザーデータベースと RTCab データベースへの変更をすぐに保持するために、 **CSAddressBook** Windows PowerShell コマンドレット **を実行する** 必要があります。</span><span class="sxs-lookup"><span data-stu-id="8984c-246">In previous versions of Lync Server, when applying a change to Active Directory, the administrator would be required to run **Update -CSUserDatabase** and **Update –CSAddressBook** Windows PowerShell cmdlets to persist the change to the Lync Server user database and RTCab database immediately.</span></span> <span data-ttu-id="8984c-247">Lync server 2013 では、Lync Server ユーザーレプリケーターは Active Directory から変更を受け取り、構成された間隔に基づいて Lync Server ユーザーデータベースを更新します。</span><span class="sxs-lookup"><span data-stu-id="8984c-247">In Lync Server 2013, Lync Server User Replicator will pick up the changes from Active Directory and update the Lync Server user database based on a configured interval.</span></span> <span data-ttu-id="8984c-248">Lync Server ユーザーレプリケーターでは、管理者が更新プログラムを実行しなくても、変更内容が RTCab データベースにすばやく反映されます CSAddressBook。</span><span class="sxs-lookup"><span data-stu-id="8984c-248">Lync Server User Replicator will also propagate the changes to the RTCab database quickly without the administrator having to run Update-CSAddressBook.</span></span> <span data-ttu-id="8984c-249">アドレス帳 Web クエリが有効になっている場合、変更は Lync クライアントの検索結果に反映されます。</span><span class="sxs-lookup"><span data-stu-id="8984c-249">If Address Book Web query is enabled, then the changes will be reflected in search results by Lync clients.</span></span> <span data-ttu-id="8984c-250">CSAddressBook を実行するには、アドレス帳ファイルのダウンロードが有効になっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="8984c-250">Administrators will only need to run Update -CSAddressBook if the Address Book file download is enabled.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8984c-251">Lync Server ユーザーレプリケーターは、既定では、5分ごとに自動的に実行されます。</span><span class="sxs-lookup"><span data-stu-id="8984c-251">By default Lync Server User Replicator runs automatically every 5 minutes.</span></span> <span data-ttu-id="8984c-252">この間隔は、ReplicationCycleInterval を使用して設定でき &lt; &gt; ます。</span><span class="sxs-lookup"><span data-stu-id="8984c-252">You can configure this interval by using Set -CSUserReplicatorConfiguration -ReplicationCycleInterval &lt;&gt;.</span></span>



</div>

</div>

<div>

## <a name="filtering-the-address-book"></a><span data-ttu-id="8984c-253">アドレス帳をフィルター処理する</span><span class="sxs-lookup"><span data-stu-id="8984c-253">Filtering the Address Book</span></span>

<span data-ttu-id="8984c-254">アドレス帳のサーバーファイルに設定されているユーザーは、AbAttribute テーブルに記載されている特定の Active Directory ドメインサービスの属性に基づいて制御できます。</span><span class="sxs-lookup"><span data-stu-id="8984c-254">The users populated in the Address Book Server files can be controlled based on certain Active Directory Domain Services attributes listed in the AbAttribute table.</span></span> <span data-ttu-id="8984c-255">フィルター処理に使う属性は、 **msExchangeHideFromAddressBook** 属性の1つです。</span><span class="sxs-lookup"><span data-stu-id="8984c-255">One such attribute used for filtering is the **msExchangeHideFromAddressBook** attribute.</span></span> <span data-ttu-id="8984c-256">これは、Exchange スキーマによって追加されたユーザー属性です。</span><span class="sxs-lookup"><span data-stu-id="8984c-256">This is a user attribute added by the Exchange schema.</span></span> <span data-ttu-id="8984c-257">この属性の値が TRUE の場合、Exchange Server はこの属性を使って、連絡先を Outlook のグローバルアドレス一覧 (GAL) から非表示にします。</span><span class="sxs-lookup"><span data-stu-id="8984c-257">If the value of this attribute is TRUE, Exchange Server uses this attribute to hide the contact from the Outlook Global Address List (GAL).</span></span> <span data-ttu-id="8984c-258">同様に、この属性の値が TRUE の場合、ユーザーレプリケーターは AbUserEntry テーブルにそのユーザーを含めません。このユーザーはアドレス帳のサーバーファイルには含まれません。</span><span class="sxs-lookup"><span data-stu-id="8984c-258">Similarly, if the value of this attribute is TRUE, User Replicator does not include that user in the AbUserEntry table and this user will not be in the Address Book Server files.</span></span>

<span data-ttu-id="8984c-259">一部のフラグビットを使って、アドレス帳のサーバー属性で使用するフィルターを定義できます。</span><span class="sxs-lookup"><span data-stu-id="8984c-259">You can use some flag bits to define a filter to use on Address Book Server attributes.</span></span> <span data-ttu-id="8984c-260">たとえば、特定のフラグビットが存在する場合、属性は include 属性または exclude 属性として識別できます。</span><span class="sxs-lookup"><span data-stu-id="8984c-260">For example, the presence of certain flag bits can identify an attribute as an include attribute or an exclude attribute.</span></span> <span data-ttu-id="8984c-261">ユーザーレプリケーターフィルター除外属性が含まれている連絡先には、include 属性を含まない連絡先が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8984c-261">User Replicator filters out contacts that contain an exclude attribute and filters out contains that do not contain an include attribute.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="8984c-262">アドレス帳のフィルター処理の詳細については、「 <A href="https://technet.microsoft.com/library/gg415643(v=ocs.15)">Lync server 2013 のアドレス帳サーバーコマンドレット</A>」および「 <A href="https://go.microsoft.com/fwlink/?linkid=330430">lync 2013 のアドレス帳をフィルター</A>処理する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8984c-262">For more information about filtering the Address Book, see <A href="https://technet.microsoft.com/library/gg415643(v=ocs.15)">Address Book Server cmdlets in Lync Server 2013</A>, and <A href="https://go.microsoft.com/fwlink/?linkid=330430">Filter Lync 2013 address book</A></span></span>



</div>

<span data-ttu-id="8984c-263">現在、3種類のフィルターがあります。</span><span class="sxs-lookup"><span data-stu-id="8984c-263">Currently, there are three different filters.</span></span> <span data-ttu-id="8984c-264">次の表は、これらのフィルターの一覧です。</span><span class="sxs-lookup"><span data-stu-id="8984c-264">The following table lists these filters.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8984c-265">属性</span><span class="sxs-lookup"><span data-stu-id="8984c-265">Attribute</span></span></th>
<th><span data-ttu-id="8984c-266">説明</span><span class="sxs-lookup"><span data-stu-id="8984c-266">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8984c-267">0x800</span><span class="sxs-lookup"><span data-stu-id="8984c-267">0x800</span></span></p></td>
<td><p><span data-ttu-id="8984c-268">設定すると、連絡先に必須の属性が指定します。</span><span class="sxs-lookup"><span data-stu-id="8984c-268">If set, this identifies a required attribute for a contact.</span></span> <span data-ttu-id="8984c-269">ユーザーレプリケーターでは、少なくとも1つの必須属性が含まれていない連絡先を除外するために、このフラグビットを使用しています。</span><span class="sxs-lookup"><span data-stu-id="8984c-269">User Replicator uses this flag bit to filter out contacts that do not contain at least one required attribute.</span></span> <span data-ttu-id="8984c-270">OuPathId は必須の属性であり、常に設定されています。</span><span class="sxs-lookup"><span data-stu-id="8984c-270">The OuPathId is a required attribute, which is always set.</span></span> <span data-ttu-id="8984c-271">そのため、必要な他の属性の少なくとも1つを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8984c-271">So at least one of other required attributes should be set.</span></span> <span data-ttu-id="8984c-272">それ以外の場合は、(つまり、必須属性 OuPathId の値を持つ) 連絡先はデータベースに書き込まれません。</span><span class="sxs-lookup"><span data-stu-id="8984c-272">Otherwise, contact (that is, with value of required attribute OuPathId) will still not be written to database.</span></span> <span data-ttu-id="8984c-273">たとえば、 <strong>telephoneNumber</strong> と <strong>homePhone</strong> が必須属性として定義されている場合、これらの属性の少なくとも1つが含まれている連絡先のみがデータベースに書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="8984c-273">For example, if <strong>telephoneNumber</strong> and <strong>homePhone</strong> are defined as required attributes, only the contacts that have at least one of these attributes are written to the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8984c-274">0x4000</span><span class="sxs-lookup"><span data-stu-id="8984c-274">0x4000</span></span></p></td>
<td><p><span data-ttu-id="8984c-275">設定すると、exclude 属性が識別されます。</span><span class="sxs-lookup"><span data-stu-id="8984c-275">If set, this identifies an exclude attribute.</span></span> <span data-ttu-id="8984c-276">ユーザーレプリケーターはこのフラグビットを使って、この属性を含む連絡先をフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="8984c-276">User Replicator uses this flag bit to filter out contacts that contain this attribute.</span></span> <span data-ttu-id="8984c-277">たとえば、 <strong>msrtcsip-userenabled true-PrimaryUserAddress</strong> が exclude 属性として定義されている場合、この属性を持つ連絡先はデータベースに書き込まれません。</span><span class="sxs-lookup"><span data-stu-id="8984c-277">For example, if <strong>msRTCSIP-PrimaryUserAddress</strong> is defined as an exclude attribute, contacts that have this attribute are not written to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8984c-278">0x8000</span><span class="sxs-lookup"><span data-stu-id="8984c-278">0x8000</span></span></p></td>
<td><p><span data-ttu-id="8984c-279">設定すると、include 属性が識別されます。</span><span class="sxs-lookup"><span data-stu-id="8984c-279">If set, this identifies an include attribute.</span></span> <span data-ttu-id="8984c-280">ユーザーレプリケーターはこのフラグビットを使って、この属性が含まれていない連絡先を除外します。</span><span class="sxs-lookup"><span data-stu-id="8984c-280">User Replicator uses this flag bit to filter out contacts that do not contain this attribute.</span></span> <span data-ttu-id="8984c-281">たとえば、 <strong>msrtcsip-userenabled true-PrimaryUserAddress</strong> が include 属性として定義されている場合、この属性を持つ連絡先のみがデータベースに書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="8984c-281">For example, if <strong>msRTCSIP-PrimaryUserAddress</strong> is defined as an include attribute, only the contacts that have this attribute are written to the database.</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="8984c-282">0x4000 (exclude 属性) と 0x8000 (include 属性) の両方のフラグビットが設定されている場合、0x4000 ビットは0x8000 ビットよりも優先され、その連絡先は除外されます。</span><span class="sxs-lookup"><span data-stu-id="8984c-282">If both the 0x4000 (exclude attribute) and 0x8000 (include attribute) flag bits are set, the 0x4000 bit overrides the 0x8000 bit and the contact is excluded.</span></span>



</div>

<span data-ttu-id="8984c-283">アドレス帳をフィルター処理して特定のユーザーのみを含めることはできますが、エントリを制限しても、他のユーザーがフィルター処理されたユーザーに連絡したり、プレゼンス状態を表示したりすることを制限することはできません。</span><span class="sxs-lookup"><span data-stu-id="8984c-283">Although you can filter the Address Book to include only certain users, limiting entries does not limit other users' ability to contact the filtered users or to see their presence status.</span></span> <span data-ttu-id="8984c-284">ユーザーは、ユーザーの完全なサインイン名を入力して、いつでもインスタントメッセージを検索したり、手動でインスタントメッセージを送信したり、アドレス帳に登録されていないユーザーに対して手動で通話を開始したりできます。</span><span class="sxs-lookup"><span data-stu-id="8984c-284">Users can always find, manually send instant messages, or manually initiate calls to users not in the Address Book by entering a user's complete sign-in name.</span></span> <span data-ttu-id="8984c-285">また、ユーザーの連絡先情報も Outlook にあります。</span><span class="sxs-lookup"><span data-stu-id="8984c-285">Also, contact information for a user could also be found in Outlook.</span></span>

<span data-ttu-id="8984c-286">アドレス帳ファイルに完全な連絡先レコードを作成しているときに、Lync Server を使用して、セッション開始プロトコル (SIP) 用に構成されていないユーザーとメール、電話、またはエンタープライズの音声通話を開始することができます。また、組織によっては、SIP 対応ユーザーのみをアドレス帳サーバーに含めるようにします</span><span class="sxs-lookup"><span data-stu-id="8984c-286">While having full contact records in the Address Book files enables you to use Lync Server to initiate email, telephone, or Enterprise Voice calls (that is, if Enterprise Voice is enabled on the server) with users that are not configured for Session Initiation Protocol (SIP), some organizations prefer to include only SIP-enabled users in their Address Book Server entries.</span></span> <span data-ttu-id="8984c-287">アドレス帳にフィルターを適用して、SIP 対応ユーザーのみを含めることができます。これには、 **mailNickname**、 **telephoneNumber**、 **homePhone**、および **mobile** の各必須属性の **Flags** 列にある [0x800] ビットをオフにします。</span><span class="sxs-lookup"><span data-stu-id="8984c-287">You can filter the Address Book to include only SIP-enabled users by clearing the 0x800 bit in the **Flags** column of the following required attributes: **mailNickname**, **telephoneNumber**, **homePhone**, and **mobile**.</span></span> <span data-ttu-id="8984c-288">また、 **msrtcsip-userenabled true-PrimaryUserAddress** 属性の **Flags** 列に 0x8000 (include 属性) を設定することによって、SIP 対応ユーザーのみを含めるようにアドレス帳をフィルター処理することもできます。</span><span class="sxs-lookup"><span data-stu-id="8984c-288">You can also filter the Address Book to include only SIP-enabled users by setting the 0x8000 (include attribute) in the **Flags** column of the **msRTCSIP-PrimaryUserAddress** attribute.</span></span> <span data-ttu-id="8984c-289">これにより、アドレス帳ファイルからサービスアカウントを除外することもできます。</span><span class="sxs-lookup"><span data-stu-id="8984c-289">This also helps to exclude service accounts from the Address Book files.</span></span>

<span data-ttu-id="8984c-290">AbAttribute テーブルを変更したら、[コマンドレットの **更新** ] を実行して、AbUserEntry テーブルのデータを更新できます。</span><span class="sxs-lookup"><span data-stu-id="8984c-290">After you modify the AbAttribute table, you can refresh the data in the AbUserEntry table by running the cmdlet **Update-CsUserDatabase** command.</span></span> <span data-ttu-id="8984c-291">UR レプリケーションが完了したら、コマンドレット **UpdateCsAddressBook** コマンドを手動で実行することで、アドレス帳のサーバーファイルストア内のファイルを更新できます。</span><span class="sxs-lookup"><span data-stu-id="8984c-291">After UR replication completes, you can update the file in the Address Book Server file store by manually running the cmdlet **UpdateCsAddressBook** command.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8984c-292">アドレス帳サーバーが配置されているフロントエンドサーバーは、管理上では構成できません。</span><span class="sxs-lookup"><span data-stu-id="8984c-292">The Front End Server that the Address Book Server is placed is not administratively configurable.</span></span> <span data-ttu-id="8984c-293">1つは展開中に選択されます。通常は、最初のフロントエンドサーバーが展開されます。</span><span class="sxs-lookup"><span data-stu-id="8984c-293">One is chosen during deployment—typically, the first Front End Server deployed.</span></span> <span data-ttu-id="8984c-294">障害が発生した場合、アドレス帳サービスは別のフロントエンドサーバーに移動し、管理の注意は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="8984c-294">In the event of failure, the Address Book Service will move to another Front End Server, and requires no administrative attention.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="8984c-295">マルチフォレスト展開または親/子展開 (インフラストラクチャの統合など) からインフラストラクチャを統合または変更した場合に、一部のユーザーのアドレス帳サービスのダウンロードとアドレス帳 Web クエリが失敗することがあります。</span><span class="sxs-lookup"><span data-stu-id="8984c-295">If you have consolidated or otherwise modified your infrastructure from a multi-forest deployment or a parent/child deployment (such as consolidating your infrastructure before moving to Lync Server), you may find that the Address Book service download and the Address Book Web Query fails for some users.</span></span> <span data-ttu-id="8984c-296">複数のドメインまたはフォレストが含まれている展開では、この問題が発生しているユーザーオブジェクトに <STRONG>msrtcsip-userenabled true</STRONG> という属性が設定されます。</span><span class="sxs-lookup"><span data-stu-id="8984c-296">When in a deployment that had multiple domains or forests, the attribute <STRONG>MsRTCSIP-OriginatorSid</STRONG> is populated on the user objects that are exhibiting the issue.</span></span> <span data-ttu-id="8984c-297">問題を解決するには、これらのオブジェクトで <STRONG>msrtcsip-userenabled true-Atorsid</STRONG> 属性を NULL に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8984c-297">The <STRONG>MsRTCSIP-OriginatorSid</STRONG> attribute must be set to NULL on these objects to resolve the issue.</span></span>



<span data-ttu-id="8984c-298"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8984c-298"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

