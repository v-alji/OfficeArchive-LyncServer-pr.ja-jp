---
title: 'Lync Server 2013: 登録ビュー'
description: 'Lync Server 2013: 登録ビュー。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Registration view
ms:assetid: 8a42bc7d-3d4f-43c1-9e15-89b2ee419ade
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688120(v=OCS.15)
ms:contentKeyID: 49733718
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: be169cafc324f89cacedda154ca49a8ff1ff39aa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398732"
---
# <a name="registration-view-in-lync-server-2013"></a><span data-ttu-id="7bb8e-103">Lync Server 2013 に表示される登録情報</span><span class="sxs-lookup"><span data-stu-id="7bb8e-103">Registration view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7bb8e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7bb8e-104">

<span> </span></span></span>

<span data-ttu-id="7bb8e-105">_**最終更新日:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="7bb8e-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="7bb8e-106">登録ビューには、ユーザー登録に関する情報が格納されます。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-106">The Registration view stores information about user registration.</span></span> <span data-ttu-id="7bb8e-107">このビューは、Lync Server 2013 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-107">This view was introduced in Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7bb8e-108">列</span><span class="sxs-lookup"><span data-stu-id="7bb8e-108">Column</span></span></th>
<th><span data-ttu-id="7bb8e-109">データ型</span><span class="sxs-lookup"><span data-stu-id="7bb8e-109">Data Type</span></span></th>
<th><span data-ttu-id="7bb8e-110">詳細</span><span class="sxs-lookup"><span data-stu-id="7bb8e-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7bb8e-111"><strong>セッション Id</strong></span><span class="sxs-lookup"><span data-stu-id="7bb8e-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="7bb8e-112">datetime</span><span class="sxs-lookup"><span data-stu-id="7bb8e-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="7bb8e-113">セッション要求の時刻。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-113">Time of session request.</span></span> <span data-ttu-id="7bb8e-114">セッションを一意に識別するために SessionIdSeq と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-114">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="7bb8e-115">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-115">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bb8e-116"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="7bb8e-116"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="7bb8e-117">int</span><span class="sxs-lookup"><span data-stu-id="7bb8e-117">int</span></span></p></td>
<td><p><span data-ttu-id="7bb8e-118">セッションを識別する ID 番号。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-118">ID number to identify the session.</span></span> <span data-ttu-id="7bb8e-119">セッションを一意に識別するために SessionIdTime と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-119">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="7bb8e-120">詳細については、「 <a href="lync-server-2013-dialogs-table.md">Lync Server 2013 のダイアログテーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-120">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bb8e-121"><strong>RegisterTime</strong></span><span class="sxs-lookup"><span data-stu-id="7bb8e-121"><strong>RegisterTime</strong></span></span></p></td>
<td><p><span data-ttu-id="7bb8e-122">datetime</span><span class="sxs-lookup"><span data-stu-id="7bb8e-122">datetime</span></span></p></td>
<td><p><span data-ttu-id="7bb8e-123">登録が発生した時刻。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-123">Time at which registration occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bb8e-124"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="7bb8e-124"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="7bb8e-125">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="7bb8e-125">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="7bb8e-126">登録されたユーザーの URI。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-126">URI of the user who registered.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bb8e-127"><strong>UserUriType</strong></span><span class="sxs-lookup"><span data-stu-id="7bb8e-127"><strong>UserUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="7bb8e-128">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7bb8e-128">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7bb8e-129">登録したユーザーの URI の種類。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-129">Type of URI of the user who registered.</span></span> <span data-ttu-id="7bb8e-130">詳細については、「 <a href="lync-server-2013-uritypes-table.md">Lync Server 2013 の UriTypes テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-130">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bb8e-131"><strong>UserTenant</strong></span><span class="sxs-lookup"><span data-stu-id="7bb8e-131"><strong>UserTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="7bb8e-132">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7bb8e-132">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7bb8e-133">登録したユーザーのテナント。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-133">Tenant of the user who registered.</span></span> <span data-ttu-id="7bb8e-134">詳細については、「 <a href="lync-server-2013-tenants-table.md">Lync Server 2013 のテナントの一覧</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-134">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bb8e-135"><strong>EndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="7bb8e-135"><strong>EndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="7bb8e-136">長さ</span><span class="sxs-lookup"><span data-stu-id="7bb8e-136">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="7bb8e-137">登録されているユーザーのエンドポイントの一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-137">Unique identifier of the endpoint of the user registered with.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bb8e-138"><strong>Endポインタ a</strong></span><span class="sxs-lookup"><span data-stu-id="7bb8e-138"><strong>EndpointEra</strong></span></span></p></td>
<td><p><span data-ttu-id="7bb8e-139">長さ</span><span class="sxs-lookup"><span data-stu-id="7bb8e-139">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="7bb8e-140">同じユーザーと同じエンドポイントを含む登録を区別するために使用される一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-140">Unique identifier used to differentiate registrations that involve the same user and the same endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bb8e-141"><strong>DeRegisterType</strong></span><span class="sxs-lookup"><span data-stu-id="7bb8e-141"><strong>DeRegisterType</strong></span></span></p></td>
<td><p><span data-ttu-id="7bb8e-142">datetime</span><span class="sxs-lookup"><span data-stu-id="7bb8e-142">datetime</span></span></p></td>
<td><p><span data-ttu-id="7bb8e-143">登録解除が行われた時刻。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-143">Time at which deregistration occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bb8e-144"><strong>DeRegisterReason</strong></span><span class="sxs-lookup"><span data-stu-id="7bb8e-144"><strong>DeRegisterReason</strong></span></span></p></td>
<td><p><span data-ttu-id="7bb8e-145">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7bb8e-145">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7bb8e-146">登録解除の理由。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-146">Reason for deregistration.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bb8e-147"><strong>ClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="7bb8e-147"><strong>ClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="7bb8e-148">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7bb8e-148">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7bb8e-149">登録したユーザーによって使用されたクライアントのバージョン。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-149">Version of client used by the user who registered.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bb8e-150"><strong>ClientType</strong></span><span class="sxs-lookup"><span data-stu-id="7bb8e-150"><strong>ClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="7bb8e-151">int</span><span class="sxs-lookup"><span data-stu-id="7bb8e-151">int</span></span></p></td>
<td><p><span data-ttu-id="7bb8e-152">登録したユーザーによって使用されたクライアント。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-152">Client used by the user who registered.</span></span> <span data-ttu-id="7bb8e-153">詳細については、「 <a href="lync-server-2013-useragentdef-table.md">Lync Server 2013 の Useragentdef テーブル</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-153">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bb8e-154"><strong>ClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="7bb8e-154"><strong>ClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="7bb8e-155">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="7bb8e-155">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="7bb8e-156">登録されたユーザーによって使用されたクライアントのカテゴリです。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-156">Category of the client used by the user who registered.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bb8e-157"><strong>Ip</strong></span><span class="sxs-lookup"><span data-stu-id="7bb8e-157"><strong>IpAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="7bb8e-158">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7bb8e-158">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7bb8e-159">ユーザーが登録した IP アドレス。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-159">IP Address the user registered with.</span></span> <span data-ttu-id="7bb8e-160">これは IPv4 または IPv6 アドレスである可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-160">This may be an IPv4 or IPv6 address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bb8e-161"><strong>この Id</strong></span><span class="sxs-lookup"><span data-stu-id="7bb8e-161"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="7bb8e-162">varstring (775)</span><span class="sxs-lookup"><span data-stu-id="7bb8e-162">varstring(775)</span></span></p></td>
<td><p><span data-ttu-id="7bb8e-163">SIP ダイアログ ID。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-163">SIP dialog ID.</span></span> <span data-ttu-id="7bb8e-164">の形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-164">The format of the is:</span></span></p>
<p><span data-ttu-id="7bb8e-165">ダイアログ; 開始タグからタグへ</span><span class="sxs-lookup"><span data-stu-id="7bb8e-165">dialog;from-tag;to-tag</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bb8e-166"><strong>返信</strong></span><span class="sxs-lookup"><span data-stu-id="7bb8e-166"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="7bb8e-167">int</span><span class="sxs-lookup"><span data-stu-id="7bb8e-167">int</span></span></p></td>
<td><p><span data-ttu-id="7bb8e-168">セッション招待状への SIP 応答コード。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-168">SIP response code to the session invitation.</span></span> <span data-ttu-id="7bb8e-169">通常、このフィールドは、セッションの最初の INVITE メッセージから生成されたデータによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-169">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="7bb8e-170">招待メッセージがない場合は、最初に関連する SIP メッセージ (BYE、キャンセル、メッセージ、または情報) の日付と時刻がフィールドに設定されています。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-170">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bb8e-171"><strong>DiagnosticId</strong></span><span class="sxs-lookup"><span data-stu-id="7bb8e-171"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="7bb8e-172">int</span><span class="sxs-lookup"><span data-stu-id="7bb8e-172">int</span></span></p></td>
<td><p><span data-ttu-id="7bb8e-173">SIP ヘッダーからキャプチャされた診断 ID。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-173">Diagnostic ID captured from SIP header.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bb8e-174"><strong>レジストラー</strong></span><span class="sxs-lookup"><span data-stu-id="7bb8e-174"><strong>Registrar</strong></span></span></p></td>
<td><p><span data-ttu-id="7bb8e-175">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7bb8e-175">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7bb8e-176">レジストラーの FQDN。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-176">FQDN of the Registrar.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bb8e-177"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="7bb8e-177"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="7bb8e-178">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7bb8e-178">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7bb8e-179">セッションのデータをキャプチャしたプールの FQDN。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-179">FQDN of the pool that captured the data for the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bb8e-180"><strong>EdgeServer</strong></span><span class="sxs-lookup"><span data-stu-id="7bb8e-180"><strong>EdgeServer</strong></span></span></p></td>
<td><p><span data-ttu-id="7bb8e-181">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7bb8e-181">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7bb8e-182">登録されたユーザーによって使用されたエッジサーバーの FQDN。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-182">FQDN of the Edge Server used by the user who registered.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bb8e-183"><strong>IsInternal</strong></span><span class="sxs-lookup"><span data-stu-id="7bb8e-183"><strong>IsInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="7bb8e-184">bit</span><span class="sxs-lookup"><span data-stu-id="7bb8e-184">bit</span></span></p></td>
<td><p><span data-ttu-id="7bb8e-185">ユーザーが内部ネットワークからログオンしているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-185">Indicates whether the user logged on from the internal network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bb8e-186"><strong>IsUserServiceAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="7bb8e-186"><strong>IsUserServiceAvailable</strong></span></span></p></td>
<td><p><span data-ttu-id="7bb8e-187">bit</span><span class="sxs-lookup"><span data-stu-id="7bb8e-187">bit</span></span></p></td>
<td><p><span data-ttu-id="7bb8e-188">登録時に UserService が利用可能であったかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-188">Indicates whether the UserService was available at registration time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bb8e-189"><strong>IsPrimaryRegistrar</strong></span><span class="sxs-lookup"><span data-stu-id="7bb8e-189"><strong>IsPrimaryRegistrar</strong></span></span></p></td>
<td><p><span data-ttu-id="7bb8e-190">bit</span><span class="sxs-lookup"><span data-stu-id="7bb8e-190">bit</span></span></p></td>
<td><p><span data-ttu-id="7bb8e-191">登録がプライマリレジストラーであったかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-191">Indicates whether registration was with the primary Registrar.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bb8e-192"><strong>DeviceMacAddress</strong></span><span class="sxs-lookup"><span data-stu-id="7bb8e-192"><strong>DeviceMacAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="7bb8e-193">bigint</span><span class="sxs-lookup"><span data-stu-id="7bb8e-193">bigint</span></span></p></td>
<td><p><span data-ttu-id="7bb8e-194">登録されているデバイスの MAC アドレス。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-194">MAC Address of device registered.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bb8e-195"><strong>DeviceManufacturer</strong></span><span class="sxs-lookup"><span data-stu-id="7bb8e-195"><strong>DeviceManufacturer</strong></span></span></p></td>
<td><p><span data-ttu-id="7bb8e-196">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7bb8e-196">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7bb8e-197">登録されているデバイスの製造元。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-197">Manufacturer of the device registered.</span></span> <span data-ttu-id="7bb8e-198">詳細については、「 <a href="lync-server-2013-manufacturers-table.md">Lync Server 2013 の製造元の表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-198">See the <a href="lync-server-2013-manufacturers-table.md">Manufacturers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bb8e-199"><strong>DeviceHardwareVersion</strong></span><span class="sxs-lookup"><span data-stu-id="7bb8e-199"><strong>DeviceHardwareVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="7bb8e-200">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="7bb8e-200">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="7bb8e-201">登録されているデバイスのハードウェアバージョン。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-201">Hardware version of the device registered.</span></span> <span data-ttu-id="7bb8e-202">詳細については、「 <a href="lync-server-2013-hardwareversions-table.md">Lync Server 2013 のハードウェアバージョンの表</a> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-202">See the <a href="lync-server-2013-hardwareversions-table.md">HardwareVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="7bb8e-203">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7bb8e-203">


</div>

<span> </span>

</div>

</div>

</span></span></div>

