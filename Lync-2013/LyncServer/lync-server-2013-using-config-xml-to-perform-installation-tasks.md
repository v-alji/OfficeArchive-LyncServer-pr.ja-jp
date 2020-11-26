---
title: 'Lync Server 2013: Config.xml を使ってインストールタスクを実行する'
description: 'Lync Server 2013: Config.xml を使ってインストールタスクを実行します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using Config.xml to perform installation tasks
ms:assetid: 0813184a-ab40-417c-b3a3-c2090766b831
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204651(v=OCS.15)
ms:contentKeyID: 48183332
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 22fff14e21a120c3a0ee2cd6432fd1eba2bbee5f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438954"
---
# <a name="using-configxml-to-perform-installation-tasks-in-lync-server-2013"></a><span data-ttu-id="91fe2-103">Lync Server 2013 で Config.xml を使ってインストールタスクを実行する</span><span class="sxs-lookup"><span data-stu-id="91fe2-103">Using Config.xml to perform installation tasks in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="91fe2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="91fe2-104">

<span> </span></span></span>

<span data-ttu-id="91fe2-105">_**最終更新日:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="91fe2-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="91fe2-p101">Office カスタマイズ ツール (OCT) はカスタマイズ インストール向けの主要ツールですが、管理者は OCT では使用できない追加のインストール手順を Config.xml ファイルによって指定できます。以下のカスタマイズは、Config.xml ファイルを使用しないと実行できません。</span><span class="sxs-lookup"><span data-stu-id="91fe2-p101">Although the Office Customization Tool (OCT) is the primary tool for customization installation, administrators can use the Config.xml file to specify additional installation instructions that are not available in the OCT. The following customizations can only be made by using the Config.xml file:</span></span>

  - <span data-ttu-id="91fe2-108">ネットワーク インストール ポイントのパスを指定する。</span><span class="sxs-lookup"><span data-stu-id="91fe2-108">Specify the path of the network installation point.</span></span>

  - <span data-ttu-id="91fe2-109">インストールする製品を選択する。</span><span class="sxs-lookup"><span data-stu-id="91fe2-109">Select the products to install.</span></span>

  - <span data-ttu-id="91fe2-110">ログ記録や、セットアップ カスタマイズ ファイルおよびソフトウェア更新プログラムの場所を構成する。</span><span class="sxs-lookup"><span data-stu-id="91fe2-110">Configure logging and the location of the Setup customization file and software updates.</span></span>

  - <span data-ttu-id="91fe2-111">インストール オプション (ユーザー名など) を指定する。</span><span class="sxs-lookup"><span data-stu-id="91fe2-111">Specify installation options, such as user name.</span></span>

  - <span data-ttu-id="91fe2-112">Office をインストールせずにローカル インストール ソース (LIS) をユーザーのコンピューターにコピーする。</span><span class="sxs-lookup"><span data-stu-id="91fe2-112">Copy the local installation source (LIS) to the user's computer without installing Office.</span></span>

  - <span data-ttu-id="91fe2-113">インストールに対する言語の追加または削除を行う。</span><span class="sxs-lookup"><span data-stu-id="91fe2-113">Add or remove languages from the installation.</span></span>

<span data-ttu-id="91fe2-114">Config.xml ファイルを使用して、Lync 2013 サイレントインストールを構成することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="91fe2-114">We recommend that you use the Config.xml file to configure Lync 2013 silent installation.</span></span>

<span data-ttu-id="91fe2-115">既定では、コア製品フォルダーに保存されている Config.xml ファイル (product など) が含まれ \\ ます。WW) その製品をインストールするようにセットアップに指示します。</span><span class="sxs-lookup"><span data-stu-id="91fe2-115">By default, the Config.xml file that is stored in the core product folder (for example, \\product.WW) directs Setup to install that product.</span></span> <span data-ttu-id="91fe2-116">たとえば、次のフォルダーの Config.xml ファイルには、Lync 2013 がインストールされます。</span><span class="sxs-lookup"><span data-stu-id="91fe2-116">For example, the Config.xml file in the following folder installs Lync 2013:</span></span>

  - <span data-ttu-id="91fe2-117">\\\\サーバー \\ 共有 \\ Lync15 \\ Lync \\Config.xml</span><span class="sxs-lookup"><span data-stu-id="91fe2-117">\\\\server\\share\\Lync15\\Lync.WW \\Config.xml</span></span>

<span data-ttu-id="91fe2-118">Lync 2013 をインストールするためによく使用される Config.xml の要素を次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="91fe2-118">The Config.xml elements most commonly used for Lync 2013 installation are listed in the following table.</span></span>

### <a name="configxml-elements"></a><span data-ttu-id="91fe2-119">Config.xml の要素</span><span class="sxs-lookup"><span data-stu-id="91fe2-119">Config.xml elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="91fe2-120">要素</span><span class="sxs-lookup"><span data-stu-id="91fe2-120">Element</span></span></th>
<th><span data-ttu-id="91fe2-121">説明</span><span class="sxs-lookup"><span data-stu-id="91fe2-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="91fe2-122">Configuration</span><span class="sxs-lookup"><span data-stu-id="91fe2-122">Configuration</span></span></p></td>
<td><p><span data-ttu-id="91fe2-123">トップレベルの要素 (必須)。</span><span class="sxs-lookup"><span data-stu-id="91fe2-123">Top-level element (required).</span></span> <span data-ttu-id="91fe2-124">Product 属性 (製品 = Lync など) が含まれています。</span><span class="sxs-lookup"><span data-stu-id="91fe2-124">Contains the Product attribute, for example: Product=Lync</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91fe2-125">OptionState</span><span class="sxs-lookup"><span data-stu-id="91fe2-125">OptionState</span></span></p></td>
<td><p><span data-ttu-id="91fe2-126">インストール中、特定の製品の機能が処理される方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="91fe2-126">Specifies how specific product features are handled during installation.</span></span> <span data-ttu-id="91fe2-127">次の属性を使用して、Business Connectivity Services のインストールを防止します。これには、Outlook 2010 を妨害する共有コンポーネントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="91fe2-127">Use the following attributes to prevent installation of Business Connectivity Services, which includes shared components that interfere with Outlook 2010:</span></span></p>
<ul>
<li><p><span data-ttu-id="91fe2-128">Id = &quot; lobimain&quot;</span><span class="sxs-lookup"><span data-stu-id="91fe2-128">Id=&quot;LOBiMain&quot;</span></span></p></li>
<li><p><span data-ttu-id="91fe2-129">都道府県 = &quot; 不在&quot;</span><span class="sxs-lookup"><span data-stu-id="91fe2-129">State=&quot;Absent&quot;</span></span></p></li>
<li><p><span data-ttu-id="91fe2-130">子供 = &quot; 強制&quot;</span><span class="sxs-lookup"><span data-stu-id="91fe2-130">Children=&quot;Force&quot;</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91fe2-131">Display</span><span class="sxs-lookup"><span data-stu-id="91fe2-131">Display</span></span></p></td>
<td><p><span data-ttu-id="91fe2-p105">セットアップがユーザーに表示する UI のレベル。一般的には次の属性があります。</span><span class="sxs-lookup"><span data-stu-id="91fe2-p105">The level of UI that Setup displays to the user. Typical attributes include the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="91fe2-134">&quot;"はい" の通知 = [ &quot;  |  &quot; いいえ] &quot; (既定)</span><span class="sxs-lookup"><span data-stu-id="91fe2-134">CompletionNotice=&quot;Yes&quot; | &quot;No&quot;(default)</span></span></p></li>
<li><p><span data-ttu-id="91fe2-135">AcceptEula = &quot; Yes &quot;  |  &quot; no &quot; (既定値)</span><span class="sxs-lookup"><span data-stu-id="91fe2-135">AcceptEula=&quot;Yes&quot; | &quot;No&quot;(default)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91fe2-136">Logging</span><span class="sxs-lookup"><span data-stu-id="91fe2-136">Logging</span></span></p></td>
<td><p><span data-ttu-id="91fe2-p106">セットアップが実行するログ記録の種類のオプション。一般的には次の属性があります。</span><span class="sxs-lookup"><span data-stu-id="91fe2-p106">Options for the kind of logging that Setup performs. Typical attributes include the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="91fe2-139">Type = &quot; Off &quot;  |  &quot; Standard &quot; (既定) | &quot;詳細な&quot;</span><span class="sxs-lookup"><span data-stu-id="91fe2-139">Type =&quot;Off&quot; | &quot;Standard&quot;(default) | &quot;Verbose&quot;</span></span></p></li>
<li><p><span data-ttu-id="91fe2-140">Template=”filename.txt” (ログファイルの名前)</span><span class="sxs-lookup"><span data-stu-id="91fe2-140">Template=”filename.txt” (the name of the log file)</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91fe2-141">Setting</span><span class="sxs-lookup"><span data-stu-id="91fe2-141">Setting</span></span></p></td>
<td><p><span data-ttu-id="91fe2-p107">Windows インストーラーのプロパティの値を指定します。一般的には次の属性があります。</span><span class="sxs-lookup"><span data-stu-id="91fe2-p107">Specifies values for Windows Installer properties. Typical attributes include the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="91fe2-144">設定 Id = &quot; name &quot; (Windows Installer プロパティの名前)</span><span class="sxs-lookup"><span data-stu-id="91fe2-144">Setting Id=&quot;name&quot; (the name of the Windows Installer property)</span></span></p></li>
<li><p><span data-ttu-id="91fe2-145">Value = &quot; value &quot; (プロパティに割り当てる値)</span><span class="sxs-lookup"><span data-stu-id="91fe2-145">Value=&quot;value&quot; (the value to assign to the property)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91fe2-146">DistributionPoint</span><span class="sxs-lookup"><span data-stu-id="91fe2-146">DistributionPoint</span></span></p></td>
<td><p><span data-ttu-id="91fe2-p108">インストールを実行するネットワーク インストール ポイントの完全修飾パス</span><span class="sxs-lookup"><span data-stu-id="91fe2-p108">The fully qualified path of the network installation point from which the installation is to run. Includes the Location attribute:</span></span></p>
<ul>
<li><p><span data-ttu-id="91fe2-149">Location=” path”</span><span class="sxs-lookup"><span data-stu-id="91fe2-149">Location=”path”</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<span data-ttu-id="91fe2-150">次の例は、Lync 2013 の一般的なサイレントインストールの Config.xml ファイルを示しています。</span><span class="sxs-lookup"><span data-stu-id="91fe2-150">The following example shows a Config.xml file for a typical silent installation of Lync 2013.</span></span>

    <Configuration Product="Lync">
      <OptionState Id="LOBiMain" State="Absent" Children="Force" />
      <Display Level="None" CompletionNotice="No" AcceptEula="Yes" />
      <Logging Type="verbose" Path="%temp%" Template="LyncSetupVerbose(*).log" />
      <Setting Id="SETUP_REBOOT" Value="Never" />
      <DistributionPoint Location="\\server\share\Lync15" />
    </Configuration>

<span data-ttu-id="91fe2-151">Config.xml ファイルを使用して Office のインストールとメンテナンスタスクを実行する方法の詳細については、を参照して <https://go.microsoft.com/fwlink/p/?linkid=267514> ください。</span><span class="sxs-lookup"><span data-stu-id="91fe2-151">Detailed information about using the Config.xml file to perform Office installation and maintenance tasks is available at <https://go.microsoft.com/fwlink/p/?linkid=267514>.</span></span>

<div>

## <a name="to-customize-the-configxml-file"></a><span data-ttu-id="91fe2-152">Config.xml ファイルをカスタマイズするには</span><span class="sxs-lookup"><span data-stu-id="91fe2-152">To customize the Config.xml file</span></span>

1.  <span data-ttu-id="91fe2-153">Notepad などのテキスト エディター ツールで Config.xml ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="91fe2-153">Open the Config.xml file by using a text editor tool, such as Notepad.</span></span>

2.  <span data-ttu-id="91fe2-154">変更する要素を含む行に移動します。</span><span class="sxs-lookup"><span data-stu-id="91fe2-154">Locate the lines that contain the elements you want to change.</span></span>

3.  <span data-ttu-id="91fe2-155">使用するサイレント オプションで要素のエントリを変更します。</span><span class="sxs-lookup"><span data-stu-id="91fe2-155">Modify the element entry with the silent options that you want to use.</span></span> <span data-ttu-id="91fe2-156">コメントの区切り文字 "" を削除していることを確認してください \<\!--" and "--\> 。</span><span class="sxs-lookup"><span data-stu-id="91fe2-156">Make sure that you remove the comment delimiters, "\<\!--" and "--\>".</span></span> <span data-ttu-id="91fe2-157">たとえば、次の構文を使用します。</span><span class="sxs-lookup"><span data-stu-id="91fe2-157">For example, use the following syntax:</span></span>
    
        < DistributionPoint Location="\\server\share\Lync15" />

4.  <span data-ttu-id="91fe2-158">Config.xml ファイルを保存します。</span><span class="sxs-lookup"><span data-stu-id="91fe2-158">Save the Config.xml file.</span></span>

<span data-ttu-id="91fe2-159"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="91fe2-159"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

