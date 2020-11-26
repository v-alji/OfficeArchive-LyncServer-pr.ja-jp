---
title: 通話詳細記録と QoE (Quality of Experience) 設定の構成
description: 通話の詳細の記録と音質の設定を構成します。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring call detail recording and Quality of Experience settings
ms:assetid: 009a0499-4f8c-450d-9c72-a565a08e9f7a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204621(v=OCS.15)
ms:contentKeyID: 48183223
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: be0238701f561e6694786faec7fc914dcc9cda40
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433256"
---
# <a name="configuring-call-detail-recording-and-quality-of-experience-settings-in-lync-server-2013"></a><span data-ttu-id="e917a-103">Lync Server 2013 での通話の記録と画質設定の設定</span><span class="sxs-lookup"><span data-stu-id="e917a-103">Configuring call detail recording and Quality of Experience settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e917a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e917a-104">

<span> </span></span></span>

<span data-ttu-id="e917a-105">_**最終更新日:** 2012-10-17_</span><span class="sxs-lookup"><span data-stu-id="e917a-105">_**Topic Last Modified:** 2012-10-17_</span></span>

<span data-ttu-id="e917a-106">フロントエンドプールを使って監視ストアに関連付けた後、監視ストアをセットアップし、SQL Server Reporting Services と監視レポートをインストールして構成すると、Lync Server 管理シェルを使用して、通話の詳細記録 (CDR) と品質 (QoE) の監視を管理できます。</span><span class="sxs-lookup"><span data-stu-id="e917a-106">After you have associated a monitoring store with a Front End pool, set up the monitoring store, and then installed and configured SQL Server Reporting Services and Monitoring Reports you can manage Call Detail Recording (CDR) and Quality of Experience (QoE) monitoring by using Lync Server Management Shell.</span></span> <span data-ttu-id="e917a-107">Lync Server 管理シェルコマンドレットを使用すると、特定のサイトまたは Lync Server の展開全体について、CDR または QoE の監視を有効または無効にすることができます。これは、次のような単純なコマンドで実行できます。</span><span class="sxs-lookup"><span data-stu-id="e917a-107">Lync Server Management Shell cmdlets allow you to enable and disable CDR and/or QoE monitoring for a particular site or for your entire Lync Server deployment; that can be done with a command as simple as this:</span></span>

    Set-CsQoEConfiguration -Identity "global" -EnableQoE $False

<span data-ttu-id="e917a-108">Microsoft Lync Server 2013 をインストールすると、CDR と QoE の両方のグローバル構成設定の定義済みコレクションもインストールされます。</span><span class="sxs-lookup"><span data-stu-id="e917a-108">When you install Microsoft Lync Server 2013, you will also install a predefined collection of global configuration settings for both CDR and QoE.</span></span> <span data-ttu-id="e917a-109">以下の表に、通話詳細記録で比較的よく使用される一部の設定の既定値を示します。</span><span class="sxs-lookup"><span data-stu-id="e917a-109">Default values for some of the more commonly-used settings used by Call Detail Recording are shown in the following table:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e917a-110">プロパティ</span><span class="sxs-lookup"><span data-stu-id="e917a-110">Property</span></span></th>
<th><span data-ttu-id="e917a-111">説明</span><span class="sxs-lookup"><span data-stu-id="e917a-111">Description</span></span></th>
<th><span data-ttu-id="e917a-112">既定値</span><span class="sxs-lookup"><span data-stu-id="e917a-112">Default Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e917a-113">EnableCDR</span><span class="sxs-lookup"><span data-stu-id="e917a-113">EnableCDR</span></span></p></td>
<td><p><span data-ttu-id="e917a-p103">CDR が有効かどうかを示します。True の場合、すべての CDR レコードが収集され、監視データベースに書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="e917a-p103">Indicates whether or not CDR is enabled. If True, all CDR records will be collected and written to the monitoring database.</span></span></p></td>
<td><p><span data-ttu-id="e917a-116">True</span><span class="sxs-lookup"><span data-stu-id="e917a-116">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e917a-117">EnablePurging</span><span class="sxs-lookup"><span data-stu-id="e917a-117">EnablePurging</span></span></p></td>
<td><p><span data-ttu-id="e917a-p104">CDR レコードをデータベースから定期的に削除するかどうかを示します。True の場合、KeepCallDetailForDays プロパティ (CDR レコードの場合) および KeepErrorReportForDays プロパティ (CDR エラーの場合) で指定されている期間を過ぎると、レコードが削除されます。False の場合、CDR レコードは無期限に保持されます。</span><span class="sxs-lookup"><span data-stu-id="e917a-p104">Indicates whether or not CDR records will periodically be deleted from the database. If True, records will be deleted after the time period specified by the properties KeepCallDetailForDays (for CDR records) and KeepErrorReportForDays (for CDR errors). If False, CDR records will be maintained indefinitely.</span></span></p></td>
<td><p><span data-ttu-id="e917a-121">True</span><span class="sxs-lookup"><span data-stu-id="e917a-121">True</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e917a-122">KeepCallDetailForDays</span><span class="sxs-lookup"><span data-stu-id="e917a-122">KeepCallDetailForDays</span></span></p></td>
<td><p><span data-ttu-id="e917a-p105">CDR レコードをデータベース内に保持する日数を指定します。指定した日数を超えて存在する古いレコードはすべて自動的に削除されます。ただし、この処理は削除が有効になっている場合にのみ実行されます。</span><span class="sxs-lookup"><span data-stu-id="e917a-p105">Indicates the number of days that CDR records will be kept in the database; any records older than the specified number of days will automatically be deleted. However, this will occur only if purging has been enabled.</span></span></p>
<p><span data-ttu-id="e917a-125">KeepCallDetailForDays には、1 ～ 2,562 日 (約 7 年間) の間の整数値を設定できます。</span><span class="sxs-lookup"><span data-stu-id="e917a-125">KeepCallDetailForDays can be set to any integer value between 1 and 2562 days (approximately 7 years).</span></span></p></td>
<td><p><span data-ttu-id="e917a-126">60 (日)</span><span class="sxs-lookup"><span data-stu-id="e917a-126">60 days</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e917a-127">KeepErrorReportForDays</span><span class="sxs-lookup"><span data-stu-id="e917a-127">KeepErrorReportForDays</span></span></p></td>
<td><p><span data-ttu-id="e917a-128">CDR エラーレポートが保持される日数を示します。指定した日数よりも古いレポートは、自動的に削除されます。</span><span class="sxs-lookup"><span data-stu-id="e917a-128">Indicates the number of days that CDR error reports are kept; any reports older than the specified number of days will automatically be deleted.</span></span> <span data-ttu-id="e917a-129">CDR エラーレポートは、Microsoft Lync 2013 などのクライアントアプリケーションによってアップロードされた診断レポートです。</span><span class="sxs-lookup"><span data-stu-id="e917a-129">CDR error reports are diagnostic reports uploaded by client applications such as Microsoft Lync 2013.</span></span></p>
<p><span data-ttu-id="e917a-130">このプロパティには、1 ～ 2,562 (日) の範囲の任意の整数値に指定できます。</span><span class="sxs-lookup"><span data-stu-id="e917a-130">You can set this property to any integer value between 1 and 2562 days.</span></span></p></td>
<td><p><span data-ttu-id="e917a-131">60 (日)</span><span class="sxs-lookup"><span data-stu-id="e917a-131">60 days</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e917a-132">同様に、一部の QoE 設定の既定値を以下の表に示します。</span><span class="sxs-lookup"><span data-stu-id="e917a-132">Similarly, default values for selected QoE settings are shown in this table:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e917a-133">プロパティ</span><span class="sxs-lookup"><span data-stu-id="e917a-133">Property</span></span></th>
<th><span data-ttu-id="e917a-134">説明</span><span class="sxs-lookup"><span data-stu-id="e917a-134">Description</span></span></th>
<th><span data-ttu-id="e917a-135">既定値</span><span class="sxs-lookup"><span data-stu-id="e917a-135">Default Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e917a-136">EnableQoE</span><span class="sxs-lookup"><span data-stu-id="e917a-136">EnableQoE</span></span></p></td>
<td><p><span data-ttu-id="e917a-p107">QoE 監視が有効かどうかを示します。True の場合、すべての QoE レコードが収集され、監視データベースに書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="e917a-p107">Indicates whether or not QoE monitoring is enabled. If True, all QoE records will be collected and written to the monitoring database.</span></span></p></td>
<td><p><span data-ttu-id="e917a-139">True</span><span class="sxs-lookup"><span data-stu-id="e917a-139">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e917a-140">EnablePurging</span><span class="sxs-lookup"><span data-stu-id="e917a-140">EnablePurging</span></span></p></td>
<td><p><span data-ttu-id="e917a-p108">QoE レコードをデータベースから定期的に削除するかどうかを示します。True の場合、KeepQoEDataForDays プロパティで指定されている期間を過ぎると、レコードが削除されます。False の場合、QoE レコードは無期限に保持されます。</span><span class="sxs-lookup"><span data-stu-id="e917a-p108">Indicates whether or not QoE records will periodically be deleted from the database. If True, records will be deleted after the time period specified by the KeepQoEDataForDays property. If False, QoE records will be maintained indefinitely.</span></span></p></td>
<td><p><span data-ttu-id="e917a-144">True</span><span class="sxs-lookup"><span data-stu-id="e917a-144">True</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e917a-145">KeepQoEDataForDays</span><span class="sxs-lookup"><span data-stu-id="e917a-145">KeepQoEDataForDays</span></span></p></td>
<td><p><span data-ttu-id="e917a-p109">QoE レコードをデータベース内に保持する日数を指定します。指定した日数を超えて存在する古いレコードはすべて自動的に削除されます。ただし、この処理は削除が有効になっている場合にのみ実行されます。</span><span class="sxs-lookup"><span data-stu-id="e917a-p109">Indicates the number of days that QoE records will be kept in the database; any records older than the specified number of days will automatically be deleted. However, this will occur only if purging has been enabled.</span></span></p>
<p><span data-ttu-id="e917a-148">KeepCallDetailForDays は、1 ～ 2,562 (日) の範囲の任意の整数値に設定できます。</span><span class="sxs-lookup"><span data-stu-id="e917a-148">KeepCallDetailForDays can be set to any integer value between 1 and 2562 days.</span></span></p></td>
<td><p><span data-ttu-id="e917a-149">60 日</span><span class="sxs-lookup"><span data-stu-id="e917a-149">60 days</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e917a-150">これらのグローバル設定を変更する必要がある場合は、Set-CsCdrConfiguration と Set-CsQoEConfiguration コマンドレットを使用して行うことができます。</span><span class="sxs-lookup"><span data-stu-id="e917a-150">If you need to modify these global settings you can do so by using the Set-CsCdrConfiguration and the Set-CsQoEConfiguration cmdlets.</span></span> <span data-ttu-id="e917a-151">たとえば、次のコマンド (Lync Server 管理シェル内から実行) は、グローバルスコープで CDR の監視を無効にします。これを行うには、EnableCDR プロパティを False ($False) に設定します。</span><span class="sxs-lookup"><span data-stu-id="e917a-151">For example, this command (run from within the Lync Server Management Shell) disables CDR monitoring at the global scope; that's done by setting the EnableCDR property to False ($False):</span></span>

    Set-CsCdrConfiguration -Identity "global" -EnableCDR $False

<span data-ttu-id="e917a-152">監視を無効にしても、監視ストアとフロントエンド プールとの関連付けは解除されず、バックエンド監視データベースがアンインストールされたり、その他の影響がこのデータベースに及んだりすることもありません。</span><span class="sxs-lookup"><span data-stu-id="e917a-152">Note that disabling monitoring does not dissociate the monitoring store from the Front End pool, nor does it uninstall or otherwise affect the backend monitoring database.</span></span> <span data-ttu-id="e917a-153">Lync Server 管理シェルを使用して CDR または QoE の監視を無効にしている場合、実際には、Lync Server で監視データの収集とアーカイブが行われなくなります。</span><span class="sxs-lookup"><span data-stu-id="e917a-153">When you use Lync Server Management Shell to disable either CDR or QoE monitoring all you really do is temporarily stop Lync Server from collecting and archiving monitoring data.</span></span> <span data-ttu-id="e917a-154">この場合、次のように EnableCDR プロパティの設定を True ($True) に戻すだけで、CDR データの収集とアーカイブを再開できます。</span><span class="sxs-lookup"><span data-stu-id="e917a-154">If you want to resume, in this case, the collection and archiving of CDR data, all you need to do is set the EnableCDR property back to True ($True):</span></span>

    Set-CsCdrConfiguration -Identity "global" -EnableCDR $True

<span data-ttu-id="e917a-155">同様に、次のコマンドは、QoE レコードの削除をグローバル スコープで無効にします。</span><span class="sxs-lookup"><span data-stu-id="e917a-155">Similarly, this command disables the purging of QoE records at the global scope:</span></span>

    Set-CsQoEConfiguration -Identity "global" -EnablePurging $False

<span data-ttu-id="e917a-p112">CDR と QoE の構成設定は、グローバル設定だけでなく、サイト スコープに割り当てることもできます。この操作を行うと、監視についての管理の柔軟性が向上します。たとえば、管理者は Redmond サイトで CDR 監視を有効にする一方で Dublin サイトでは CDR 監視を無効にできます。新しい CDR 構成設定をサイト スコープで作成するには、次のようなコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="e917a-p112">In addition to the global settings, CDR and QoE configurations settings can be assigned to the site scope. This provides additional management flexibility when it comes to monitoring; for example, an administrator can enable CDR monitoring for the Redmond site but disable CDR monitoring for the Dublin site. To create new CDR configuration settings at the site scope, use a command similar to this:</span></span>

    New-CsCdrConfiguration -Identity "site:Redmond" -EnableCDR $False

<span data-ttu-id="e917a-p113">サイト スコープで構成されたこの設定は、グローバル スコープで構成された設定よりも優先されることに注意してください。たとえば、CDR 監視がグローバル スコープで有効になっていても、サイト スコープ (Redmond サイト) では無効になっているとします。この場合、Redmond サイト内のユーザーについては通話詳細記録の情報がアーカイブされません。ただし、その他のサイト内のユーザー (つまり、Redmond サイトの設定ではなくグローバル設定によって管理されているユーザー) の通話詳細記録の情報はアーカイブされます。</span><span class="sxs-lookup"><span data-stu-id="e917a-p113">Keep in mind that settings configured at the site scope take precedence over settings configured at the global scope. For example, suppose CDR monitoring is enabled at the global scope, but disabled at the site scope (for the Redmond site). That means that call detail recording information will not be archived for users in the Redmond site. However, users in other sites (that is, users managed by the global settings instead of the Redmond site settings) will have their call detail recording information archived.</span></span>

<span data-ttu-id="e917a-163">新しい QoE 構成設定をサイト スコープで作成するには、次のようなコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="e917a-163">New QoE configuration settings can be created at the site scope by using a command like this one:</span></span>

    New-CsQoEConfiguration -Identity "site:Redmond" -KeepQoEDataForDays 15

<span data-ttu-id="e917a-164">詳細については、Lync Server 管理シェルで次のコマンドを入力します。</span><span class="sxs-lookup"><span data-stu-id="e917a-164">For more information, type the following commands from within the Lync Server Management Shell:</span></span>

    Get-Help New-CsCdrConfiguration | more
    Get-Help Set-CsCdrConfiguration | more
    Get-Help New-CsQoEConfiguration | more
    Get-Help Set-CsQoEConfiguration | more

<span data-ttu-id="e917a-165"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e917a-165"></div>

<span> </span>

</div>

</div>

</span></span></div>

