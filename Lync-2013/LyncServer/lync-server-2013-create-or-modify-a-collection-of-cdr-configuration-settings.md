---
title: 'Lync Server 2013: CDR 構成設定のコレクションを作成または変更する'
description: 'Lync Server 2013: CDR 構成設定のコレクションを作成または変更します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a collection of CDR configuration settings
ms:assetid: c830be5a-2a82-468d-9c46-d3fec0f79fd0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721878(v=OCS.15)
ms:contentKeyID: 49733812
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3ba911607db55a7b7206645495e70a27ed453784
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399350"
---
# <a name="create-or-modify-a-collection-of-cdr-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="ccab0-103">Lync Server 2013 で CDR 構成設定のコレクションを作成または変更する</span><span class="sxs-lookup"><span data-stu-id="ccab0-103">Create or modify a collection of CDR configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ccab0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ccab0-104">

<span> </span></span></span>

<span data-ttu-id="ccab0-105">_**トピックの最終更新日:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="ccab0-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="ccab0-p101">通話詳細記録 (CDR) では、ピアツーピアのインスタント メッセージング セッション、ボイス オーバー IP (VoIP) 電話の通話、電話会議などの使用状況を追跡できます。この使用状況データの中には、通話の発信者と受信者、通話時刻、通話時間の情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ccab0-p101">Call detail recording (CDR) enables you to track usage of such things as peer-to-peer instant messaging sessions, Voice over Internet Protocol (VoIP) phone calls, and conferencing calls. This usage data includes information about who called whom, when they called, and how long they talked.</span></span>

<span data-ttu-id="ccab0-108">Microsoft Lync Server 2013 をインストールすると、1つのグローバルな CDR 構成設定のグローバルコレクションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="ccab0-108">When you install Microsoft Lync Server 2013 a single, global collection of CDR configuration settings is created for you.</span></span> <span data-ttu-id="ccab0-109">管理者は、サイト スコープでカスタム設定を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="ccab0-109">Administrators also have the option of creating custom settings at the site scope.</span></span> <span data-ttu-id="ccab0-110">これらのサイト スコープの設定が使用されるときは常に、グローバル設定よりも優先されます。</span><span class="sxs-lookup"><span data-stu-id="ccab0-110">Whenever these site-scoped settings are used, they take precedence over the global settings.</span></span> <span data-ttu-id="ccab0-111">たとえば、Redmond サイトにサイト スコープの設定を作成する場合、Redmond での CDR の管理には (グローバル設定ではなく) それらの設定が使用されます。</span><span class="sxs-lookup"><span data-stu-id="ccab0-111">For example, if you create site-scoped settings for the Redmond site then those settings (rather than the global settings) will be used to manage CDR in Redmond.</span></span>

<span data-ttu-id="ccab0-112">CDR 構成設定を作成するには、Lync Server コントロールパネルまたは [CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsCdrConfiguration) コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="ccab0-112">You can create CDR configuration settings by using either Lync Server Control Panel or the [New-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsCdrConfiguration) cmdlet.</span></span> <span data-ttu-id="ccab0-113">Lync Server コントロールパネルまたは [CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsCdrConfiguration) コマンドレットを使用して、既存の設定を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="ccab0-113">You can use Lync Server Control Panel or the [Set-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsCdrConfiguration) cmdlet to modify existing settings.</span></span> <span data-ttu-id="ccab0-114">Lync Server コントロールパネルを使用して設定を作成または変更する場合は、次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="ccab0-114">If you are using Lync Server Control Panel to create or modify settings, the following options will be available to you:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ccab0-115">UI 設定</span><span class="sxs-lookup"><span data-stu-id="ccab0-115">UI Setting</span></span></th>
<th><span data-ttu-id="ccab0-116">PowerShell パラメーター</span><span class="sxs-lookup"><span data-stu-id="ccab0-116">PowerShell Parameter</span></span></th>
<th><span data-ttu-id="ccab0-117">説明</span><span class="sxs-lookup"><span data-stu-id="ccab0-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ccab0-118">名前</span><span class="sxs-lookup"><span data-stu-id="ccab0-118">Name</span></span></p></td>
<td><p><span data-ttu-id="ccab0-119">ID</span><span class="sxs-lookup"><span data-stu-id="ccab0-119">Identity</span></span></p></td>
<td><p><span data-ttu-id="ccab0-p104">作成する CDR 構成設定に対する一意の識別子。これらの設定はサイト スコープでのみ作成できます。</span><span class="sxs-lookup"><span data-stu-id="ccab0-p104">Unique identifier for the CDR configuration settings being created. These settings can only be created at the site scope.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccab0-122">CDR の監視を有効にする</span><span class="sxs-lookup"><span data-stu-id="ccab0-122">Enable monitoring of CDRs</span></span></p></td>
<td><p><span data-ttu-id="ccab0-123">EnableCDR</span><span class="sxs-lookup"><span data-stu-id="ccab0-123">EnableCDR</span></span></p></td>
<td><p><span data-ttu-id="ccab0-124">CDR が有効かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ccab0-124">Indicates whether or not CDR is enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccab0-125">CDR の削除を有効にする</span><span class="sxs-lookup"><span data-stu-id="ccab0-125">Enable purging of CDRs</span></span></p></td>
<td><p><span data-ttu-id="ccab0-126">EnablePurging</span><span class="sxs-lookup"><span data-stu-id="ccab0-126">EnablePurging</span></span></p></td>
<td><p><span data-ttu-id="ccab0-127">CDR の記録を CDR データベースから定期的に削除するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ccab0-127">Indicates whether or not CDR records will periodically be deleted from the CDR database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccab0-128">CDR を保持する最大期間 (日数)</span><span class="sxs-lookup"><span data-stu-id="ccab0-128">Keep CDRs for maximum duration (days)</span></span></p></td>
<td><p><span data-ttu-id="ccab0-129">KeepCallDetailForDays</span><span class="sxs-lookup"><span data-stu-id="ccab0-129">KeepCallDetailForDays</span></span></p></td>
<td><p><span data-ttu-id="ccab0-p105">CDR データベースに CDR レコードを保持する日数を示します。指定された日数より前のレコードは、自動的に削除されます (削除が実行されるのは、削除が有効になっている場合のみです)。</span><span class="sxs-lookup"><span data-stu-id="ccab0-p105">Indicates the number of days that CDR records will be kept in the CDR database. Any records older than the specified number of days will automatically be deleted. (Note that purging will take only place if purging has been enabled.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccab0-133">エラー報告データを保持する最大期間 (日数)</span><span class="sxs-lookup"><span data-stu-id="ccab0-133">Keep error report data for maximum duration (days)</span></span></p></td>
<td><p><span data-ttu-id="ccab0-134">KeepErrorReportForDays</span><span class="sxs-lookup"><span data-stu-id="ccab0-134">KeepErrorReportForDays</span></span></p></td>
<td><p><span data-ttu-id="ccab0-p106">CDR エラー報告を保持する日数を指定します。指定した日数を超えて保持されている報告は、自動的に削除されます。CDR エラー報告は、クライアント アプリケーションによってアップロードされる診断レポートです。</span><span class="sxs-lookup"><span data-stu-id="ccab0-p106">Indicates the number of days that CDR error reports are kept. Any reports older than the specified number of days will automatically be deleted. CDR error reports are diagnostic reports uploaded by client applications.</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="ccab0-138">New-CsCdrConfiguration と Set-CsCdrConfiguration のコマンドレットには、Lync Server コントロールパネルで利用できないその他のオプションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ccab0-138">The New-CsCdrConfiguration and Set-CsCdrConfiguration cmdlets include additional options not available in Lync Server Control Panel.</span></span> <span data-ttu-id="ccab0-139">詳細については、 <A href="https://docs.microsoft.com/powershell/module/skype/New-CsCdrConfiguration">CsCdrConfiguration</A> と <A href="https://docs.microsoft.com/powershell/module/skype/Set-CsCdrConfiguration">CsCdrConfiguration</A> のヘルプトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ccab0-139">See the <A href="https://docs.microsoft.com/powershell/module/skype/New-CsCdrConfiguration">New-CsCdrConfiguration</A> and the <A href="https://docs.microsoft.com/powershell/module/skype/Set-CsCdrConfiguration">Set-CsCdrConfiguration</A> help topics for more information.</span></span>



</div>

<div>

## <a name="to-create-cdr-configuration-settings-by-using-lync-server-control-panel"></a><span data-ttu-id="ccab0-140">Lync Server コントロールパネルを使用して CDR 構成設定を作成するには</span><span class="sxs-lookup"><span data-stu-id="ccab0-140">To create CDR configuration settings by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="ccab0-141">Lync Server コントロールパネルで **、[監視とアーカイブ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ccab0-141">In Lync Server Control Panel click **Monitoring and Archiving**.</span></span>

2.  <span data-ttu-id="ccab0-142">[ **通話の詳細記録** ] タブで、[ **新規**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ccab0-142">On the **Call Detail Recording** tab, click **New**.</span></span>

3.  <span data-ttu-id="ccab0-p108">[**サイトの選択**] ダイアログ ボックスで、新しい構成設定を作成するサイトを選択します。ダイアログ ボックスに何も表示されない場合は、すべてのサイトが CDR 構成設定のコレクションに割り当て済みであることを意味します。各サイトに対してこのようなコレクション 1 つに制限されています。その場合、設定を削除してから再作成するか、単純に既存の設定を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="ccab0-p108">In the **Select a Site** dialog box, select the site where the new configuration settings are to be created. If the dialog box is empty, that means all of your sites have already been assigned a collection of CDR configuration settings. Each site is limited to a single such collection. In that case you can either delete and then re-create the settings, or simply modify the existing settings.</span></span>

4.  <span data-ttu-id="ccab0-147">[**新しい通話詳細記録 (CDR) 設定を作成する**] ダイアログで、任意に選択を行ってから [**コミット**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ccab0-147">In the **New Call Detail Recording (CDR) Setting** dialog, make the desired selections and then click **Commit**.</span></span>

</div>

<div>

## <a name="to-modify-existing-cdr-configuration-settings-by-using-lync-server-control-panel"></a><span data-ttu-id="ccab0-148">Lync Server コントロールパネルを使用して既存の CDR 構成設定を変更するには</span><span class="sxs-lookup"><span data-stu-id="ccab0-148">To modify existing CDR configuration settings by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="ccab0-149">Lync Server コントロールパネルで **、[監視とアーカイブ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ccab0-149">In Lync Server Control Panel click **Monitoring and Archiving**.</span></span>

2.  <span data-ttu-id="ccab0-150">変更する設定のコレクションをダブルクリックするか、コレクションを選択して [**編集**] をクリックし、さらに [**詳細の表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ccab0-150">Double-click the collection of settings to be modified, or select the collection, click **Edit**, and then click **Show Details**.</span></span> <span data-ttu-id="ccab0-151">一度に変更できるのは 1 つのコレクションだけであることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="ccab0-151">Note that you can only modify a single collection at a time.</span></span> <span data-ttu-id="ccab0-152">複数のコレクションに同じ変更を加えるには、代わりに Lync Server Management Shell を使用します。</span><span class="sxs-lookup"><span data-stu-id="ccab0-152">To make the same changes to multiple collections, use the Lync Server Management Shell instead.</span></span>

3.  <span data-ttu-id="ccab0-153">[**通話詳細記録 (CDR) 設定の編集**] ダイアログで、任意の選択を行ってから [**コミット**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ccab0-153">In the **Edit Call Detail Recording (CDR) Setting** dialog, make the desired selections and then click **Commit**.</span></span>

</div>

<div>

## <a name="creating-cdr-configuration-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="ccab0-154">Windows PowerShell コマンドレットを使用した CDR 構成設定の作成</span><span class="sxs-lookup"><span data-stu-id="ccab0-154">Creating CDR Configuration Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="ccab0-155">CDR 構成設定は、Windows PowerShell と **CsCdrConfiguration** コマンドレットを使用して作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="ccab0-155">You can create CDR configuration settings can also be created by using Windows PowerShell and the **New-CsCdrConfiguration** cmdlet.</span></span> <span data-ttu-id="ccab0-156">このコマンドレットは、Lync Server 2013 管理シェルから、または Windows PowerShell のリモートセッションから実行できます。</span><span class="sxs-lookup"><span data-stu-id="ccab0-156">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="ccab0-157">リモートの Windows PowerShell を使用して Lync Server に接続する方法について詳しくは、Lync Server Windows PowerShell のブログ記事「Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell (クイックスタート: リモート PowerShell を使用した Microsoft Lync Server 2010 の管理)」を[https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876)で参照してください。</span><span class="sxs-lookup"><span data-stu-id="ccab0-157">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-create-a-new-collection-of-cdr-configuration-settings"></a><span data-ttu-id="ccab0-158">新しい CDR 構成設定のコレクションを作成するには</span><span class="sxs-lookup"><span data-stu-id="ccab0-158">To create a new collection of CDR configuration settings</span></span>

  - <span data-ttu-id="ccab0-159">このコマンドを実行すると、Redmond サイトに適用される新しい CDR 構成設定のコレクションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="ccab0-159">This command creates a new collection of CDR configuration settings applied to the Redmond site:</span></span>
    
        New-CsCdrConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-create-a-collection-of-cdr-configuration-settings-that-disable-call-detail-recording"></a><span data-ttu-id="ccab0-160">通話詳細記録を無効にする CDR 構成設定のコレクションを作成するには</span><span class="sxs-lookup"><span data-stu-id="ccab0-160">To create a collection of CDR configuration settings that disable call detail recording</span></span>

  - <span data-ttu-id="ccab0-p111">前述のコマンドでは、必須の Identity パラメーター以外のパラメーターは指定されていないため、新しい構成設定のコレクションではすべてのプロパティで既定値が使用されます。異なるプロパティ値を使用する設定を作成するには、適切なパラメーターとパラメーター値を指定します。たとえば、既定では通話詳細記録の無効化を許可する通話詳細の構成設定のコレクションを作成するには、次のようなコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="ccab0-p111">Because no parameters (other than the mandatory Identity parameter) were specified in the preceding command, the new collection of configuration settings will use the default values for all its properties. To create settings that use different property values, simply include the appropriate parameter and parameter value. For example, to create a collection of Call Detail configuration settings that, by default, allow disable Call Detail recording use a command like this:</span></span>
    
        New-CsCdrConfiguration -Identity "site:Redmond" -EnableCDR $False

</div>

<div>

## <a name="to-specify-multiple-property-values-when-creating-a-new-collection-of-cdr-configuration-settings"></a><span data-ttu-id="ccab0-164">新しい CDR 構成設定のコレクションの作成時に複数のプロパティ値を指定するには</span><span class="sxs-lookup"><span data-stu-id="ccab0-164">To specify multiple property values when creating a new collection of CDR configuration settings</span></span>

  - <span data-ttu-id="ccab0-p112">複数のパラメーターを含めることで、複数のプロパティ値を変更できます。たとえば、このコマンドを実行すると、通話詳細記録を 30 日間保持し、エラー レポートを 90 日間保持するための新しい設定が構成されます。</span><span class="sxs-lookup"><span data-stu-id="ccab0-p112">You can modify multiple property values by including multiple parameters. For example, this command configures the new settings to keep Call Detail records for 30 days and error reports for 90 days:</span></span>
    
        New-CsCdrConfiguration -Identity "site:Redmond" -KeepCallDetailForDays 30 -KeepErrorReportForDays 90

</div>

<span data-ttu-id="ccab0-167">詳細については、 [CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsCdrConfiguration) コマンドレットのヘルプトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ccab0-167">For more information, see the help topic for the [New-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsCdrConfiguration) cmdlet.</span></span>

<span data-ttu-id="ccab0-168"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ccab0-168"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

