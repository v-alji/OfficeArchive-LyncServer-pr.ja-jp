---
title: 'Lync Server 2013: Lync のメニューにコマンドを追加する'
description: 'Lync Server 2013: Lync のメニューにコマンドを追加します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Adding commands to Lync menus
ms:assetid: a8443bc2-e234-4022-870a-00700f38b1ea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412788(v=OCS.15)
ms:contentKeyID: 48185091
ms.date: 04/11/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ed4d62d085eaf115d107244ae50a7cc69e0aacd5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439241"
---
# <a name="adding-commands-to-lync-menus-in-lync-server-2013"></a><span data-ttu-id="25820-103">Lync Server 2013 での Lync メニューへのコマンドの追加</span><span class="sxs-lookup"><span data-stu-id="25820-103">Adding commands to Lync menus in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="25820-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="25820-104">

<span> </span></span></span>

<span data-ttu-id="25820-105">_**最終更新日:** 2016-04-11_</span><span class="sxs-lookup"><span data-stu-id="25820-105">_**Topic Last Modified:** 2016-04-11_</span></span>

<span data-ttu-id="25820-106">Lync 2013 メニューにカスタムコマンドを追加し、現在のユーザーの SIP Uniform リソース識別子 (URI) を、カスタムコマンドの開始時に選択した連絡先に渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="25820-106">You can add custom commands to Lync 2013 menus and pass the SIP Uniform Resource Identifier (URI) of the current user and selected contacts to the application that the custom command starts.</span></span>

<span data-ttu-id="25820-107">追加するカスタムコマンドは、次の1つ以上のメニューに表示されます。</span><span class="sxs-lookup"><span data-stu-id="25820-107">The custom commands that you add can appear on one or more of the following menus:</span></span>

  - <span data-ttu-id="25820-108">Lync メインウィンドウのメニューバーの [ツール] メニュー</span><span class="sxs-lookup"><span data-stu-id="25820-108">The Tools menu, on the menu bar in the Lync main window</span></span>

  - <span data-ttu-id="25820-109">連絡先リストの連絡先のショートカットメニュー</span><span class="sxs-lookup"><span data-stu-id="25820-109">The shortcut menu for contacts in the Contacts list</span></span>

  - <span data-ttu-id="25820-110">[会話] ウィンドウの [その他のオプション] メニュー</span><span class="sxs-lookup"><span data-stu-id="25820-110">The More Options menu, in the Conversation window</span></span>

  - <span data-ttu-id="25820-111">[会話] ウィンドウの参加者リストに一覧表示されたユーザーのショートカットメニュー</span><span class="sxs-lookup"><span data-stu-id="25820-111">The shortcut menu for people listed in the Conversation window participant list</span></span>

  - <span data-ttu-id="25820-112">連絡先カードの [オプション] メニュー</span><span class="sxs-lookup"><span data-stu-id="25820-112">The options menu in a contact card</span></span>

<span data-ttu-id="25820-113">2種類のアプリケーション (次のいずれかのアプリケーション) のカスタムコマンドを定義できます。</span><span class="sxs-lookup"><span data-stu-id="25820-113">You can define custom commands for two types of applications—applications that do either of the following:</span></span>

  - <span data-ttu-id="25820-114">現在のユーザーにのみ適用され、ローカルコンピューターで開始されます。</span><span class="sxs-lookup"><span data-stu-id="25820-114">Apply only to the current user and are started on the local computer.</span></span>

  - <span data-ttu-id="25820-115">オンラインコラボレーションプログラムなどの追加のユーザーを参加させると、各ユーザーのコンピューターで開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="25820-115">Involve additional users, such as an online collaboration program, and must be started on each user's computer.</span></span>

<span data-ttu-id="25820-116">カスタムコマンドは、次の方法で呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="25820-116">The custom command can be invoked in the following ways:</span></span>

  - <span data-ttu-id="25820-117">1人以上のユーザーを選択し、[ユーザー設定] コマンドを選択します。</span><span class="sxs-lookup"><span data-stu-id="25820-117">Select one or more users, and then choose the custom command.</span></span>

  - <span data-ttu-id="25820-118">2パーティまたはマルチパーティの会話を開始し、[ユーザー設定] コマンドを選択します。</span><span class="sxs-lookup"><span data-stu-id="25820-118">Start a two-party or multiparty conversation, and then choose the custom command.</span></span>

<div>

## <a name="to-add-a-custom-command"></a><span data-ttu-id="25820-119">カスタムコマンドを追加するには</span><span class="sxs-lookup"><span data-stu-id="25820-119">To add a custom command</span></span>

<span data-ttu-id="25820-120">次の表のレジストリ設定を使用して、メニューにコマンドを追加します。</span><span class="sxs-lookup"><span data-stu-id="25820-120">Use the registry settings in the following table to add a command to the menus.</span></span> <span data-ttu-id="25820-121">これらのエントリは、レジストリの次のいずれかの場所に配置されます。</span><span class="sxs-lookup"><span data-stu-id="25820-121">These entries are placed in the registry at one of the following locations:</span></span>

  - <span data-ttu-id="25820-122">32ビット OS の場合: HKEY \_ ローカル \_ コンピューター \\ ソフトウェア \\ Microsoft \\ Office \\ 15.0 \\ Lync \\ SessionManager \\ アプリ</span><span class="sxs-lookup"><span data-stu-id="25820-122">For 32bit OS: HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Office\\15.0\\Lync\\SessionManager\\Apps</span></span>

  - <span data-ttu-id="25820-123">64ビット OS の場合: HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Wow6432Node \\ Microsoft \\ Office \\ 15.0 \\ Lync \\ SessionManager \\ アプリ</span><span class="sxs-lookup"><span data-stu-id="25820-123">For 64bit OS: HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\Office\\15.0\\Lync\\SessionManager\\Apps</span></span>

### <a name="custom-command-registry-entries"></a><span data-ttu-id="25820-124">カスタムコマンドレジストリエントリ</span><span class="sxs-lookup"><span data-stu-id="25820-124">Custom Command Registry Entries</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="25820-125">名前</span><span class="sxs-lookup"><span data-stu-id="25820-125">Name</span></span></th>
<th><span data-ttu-id="25820-126">種類</span><span class="sxs-lookup"><span data-stu-id="25820-126">Type</span></span></th>
<th><span data-ttu-id="25820-127">データ</span><span class="sxs-lookup"><span data-stu-id="25820-127">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="25820-128">名前</span><span class="sxs-lookup"><span data-stu-id="25820-128">Name</span></span></p></td>
<td><p><span data-ttu-id="25820-129">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="25820-129">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="25820-130">メニューに表示されるアプリケーションの名前。</span><span class="sxs-lookup"><span data-stu-id="25820-130">Name of the application as it appears on the menu.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25820-131">ApplicationType</span><span class="sxs-lookup"><span data-stu-id="25820-131">ApplicationType</span></span></p></td>
<td><p><span data-ttu-id="25820-132">DWORD</span><span class="sxs-lookup"><span data-stu-id="25820-132">DWORD</span></span></p></td>
<td><p><span data-ttu-id="25820-133">0 = 実行可能ファイル (既定)</span><span class="sxs-lookup"><span data-stu-id="25820-133">0 = Executable (default)</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="25820-134">ApplicationInstallPath が必要です。</span><span class="sxs-lookup"><span data-stu-id="25820-134">Requires ApplicationInstallPath.</span></span>


</div>
<p><span data-ttu-id="25820-135">1 = プロトコル</span><span class="sxs-lookup"><span data-stu-id="25820-135">1 = Protocol</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25820-136">ApplicationInstallPath</span><span class="sxs-lookup"><span data-stu-id="25820-136">ApplicationInstallPath</span></span></p></td>
<td><p><span data-ttu-id="25820-137">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="25820-137">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="25820-138">実行可能ファイルの完全パス。</span><span class="sxs-lookup"><span data-stu-id="25820-138">Full path of the executable.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="25820-139">ApplicationType が 0 (実行可能ファイル) の場合は指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="25820-139">Must be specified if ApplicationType is 0 (Executable).</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25820-140">パス</span><span class="sxs-lookup"><span data-stu-id="25820-140">Path</span></span></p></td>
<td><p><span data-ttu-id="25820-141">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="25820-141">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="25820-142">既定のパラメーター <em>%、ユーザー id</em> %、 <em>連絡先 id</em>% など、すべてのパラメーターと共に開始する完全パス。</span><span class="sxs-lookup"><span data-stu-id="25820-142">Full path to be started along with any parameters, including the default parameters <em>%user-id%</em> and <em>%contact-id%</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25820-143">SessionType</span><span class="sxs-lookup"><span data-stu-id="25820-143">SessionType</span></span></p></td>
<td><p><span data-ttu-id="25820-144">DWORD</span><span class="sxs-lookup"><span data-stu-id="25820-144">DWORD</span></span></p></td>
<td><p><span data-ttu-id="25820-145">0 = ローカルセッション。</span><span class="sxs-lookup"><span data-stu-id="25820-145">0 = Local session.</span></span> <span data-ttu-id="25820-146">アプリケーションがローカルコンピューターで開始されます。</span><span class="sxs-lookup"><span data-stu-id="25820-146">The application is started on the local computer.</span></span></p>
<p><span data-ttu-id="25820-147">1 = 2 パーティセッション (既定)。</span><span class="sxs-lookup"><span data-stu-id="25820-147">1 = Two-party session (default).</span></span> <span data-ttu-id="25820-148">Lync 2013 では、アプリケーションをローカルで開始した後、他のユーザーにデスクトップ通知が送信されます。</span><span class="sxs-lookup"><span data-stu-id="25820-148">Lync 2013 starts the application locally and then sends a desktop notification to the other user.</span></span> <span data-ttu-id="25820-149">他のユーザーが通知をクリックして、コンピューター上でアプリケーションを起動します。</span><span class="sxs-lookup"><span data-stu-id="25820-149">The other user clicks the notification to start the application on their computer.</span></span></p>
<p><span data-ttu-id="25820-150">2 = マルチパーティセッション。</span><span class="sxs-lookup"><span data-stu-id="25820-150">2 = Multiparty session.</span></span> <span data-ttu-id="25820-151">Lync 2013 は、アプリケーションをローカルで開始してから、デスクトップ通知を他のユーザーに送信します。</span><span class="sxs-lookup"><span data-stu-id="25820-151">Lync 2013 starts the application locally and then sends desktop notifications to the other users.</span></span> <span data-ttu-id="25820-152">他のユーザーが通知をクリックして、指定されたアプリケーションを自分のコンピューターで起動します。</span><span class="sxs-lookup"><span data-stu-id="25820-152">The other user clicks the notification to start the specified application on their computer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25820-153">ExtensibleMenu</span><span class="sxs-lookup"><span data-stu-id="25820-153">ExtensibleMenu</span></span></p></td>
<td><p><span data-ttu-id="25820-154">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="25820-154">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="25820-155">このコマンドが表示されるメニューの一覧。セミコロンで区切ります。</span><span class="sxs-lookup"><span data-stu-id="25820-155">A list of the menus where this command will appear, separated by semicolons.</span></span> <span data-ttu-id="25820-156">値の例は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="25820-156">Possible values are:</span></span></p>
<p><span data-ttu-id="25820-157">MainWindowActions</span><span class="sxs-lookup"><span data-stu-id="25820-157">MainWindowActions</span></span></p>
<p><span data-ttu-id="25820-158">MainWindowRightClick 上</span><span class="sxs-lookup"><span data-stu-id="25820-158">MainWindowRightClick</span></span></p>
<p><span data-ttu-id="25820-159">ConversationWindowActions</span><span class="sxs-lookup"><span data-stu-id="25820-159">ConversationWindowActions</span></span></p>
<p><span data-ttu-id="25820-160">ConversationWindowRightClick</span><span class="sxs-lookup"><span data-stu-id="25820-160">ConversationWindowRightClick</span></span></p>
<p><span data-ttu-id="25820-161">連絡先カードメニュー</span><span class="sxs-lookup"><span data-stu-id="25820-161">ContactCardMenu</span></span></p>
<p><span data-ttu-id="25820-162">ExtensibleMenu が定義されていない場合は、MainWindowRightClick と ConversationWindowActions の既定値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="25820-162">If ExtensibleMenu is not defined, the default values of MainWindowRightClick and ConversationWindowActions are used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="25820-163">たとえば、次のレジストリエディター (.REG) ファイルには、[会話] ウィンドウの [アクション] メニューに Contoso の営業連絡先マネージャーのメニュー項目を追加した結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="25820-163">For example, the following Registry Editor (.REG) file shows the results of adding a Contoso Sales Contact Manager menu item to Actions menu in the Conversation window:</span></span>

    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Lync\SessionManager\Apps\{1F9F07C6-7E0B-462B-AAD7-98C6DBEA8F69}]
    "Name"="Contoso Sales Contact Manager"
    "HelpMessage"="The Contoso Sales Contact Manager is not installed. Contact the Help Desk for more information."
    "ApplicationType"=dword:00000000
    "ApplicationInstallPath"="C:\\cscm.exe"
    "Path"="C:\\cscm.exe %user-id% %contact-id%"
    "SessionType"=dword:00000001
    "ExtensibleMenu"="ConversationWindowActions;MainWindowRightClick"

</div>

<div>

## <a name="to-access-a-custom-command"></a><span data-ttu-id="25820-164">カスタムコマンドにアクセスするには</span><span class="sxs-lookup"><span data-stu-id="25820-164">To access a custom command</span></span>

<span data-ttu-id="25820-165">追加したカスタムコマンドにアクセスするには、定義した ExtensibleMenu 値に応じて、次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="25820-165">To access a custom command after it is added, do one of the following, depending on the ExtensibleMenu values that you define:</span></span>

  - <span data-ttu-id="25820-166">**Mainwindowactions**   Lync メインウィンドウで、[ **ツール**] をクリックし、[ユーザー設定] コマンドをクリックします。</span><span class="sxs-lookup"><span data-stu-id="25820-166">**MainWindowActions**   In the Lync main window, click **Tools**, and then click your custom command.</span></span>

  - <span data-ttu-id="25820-167">**Mainwindowrightclick**   上  Lync メインウィンドウで、連絡先を右クリックし、[ユーザー設定] コマンドをクリックします。</span><span class="sxs-lookup"><span data-stu-id="25820-167">**MainWindowRightClick**   In the Lync main window, right-click a contact, and then click your custom command.</span></span>

  - <span data-ttu-id="25820-168">**ConversationWindowActions**   会話ウィンドウで、[ **その他のオプション** ] アイコンをクリックし、ユーザー設定のコマンドをクリックします。</span><span class="sxs-lookup"><span data-stu-id="25820-168">**ConversationWindowActions**   In the Conversation window, click the **More Options** icon, and then click your custom command.</span></span>

  - <span data-ttu-id="25820-169">**ConversationWindowRightClick**   会話ウィンドウで、連絡先の名前を右クリックし、[ユーザー設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="25820-169">**ConversationWindowRightClick**   In the Conversation window, right-click a contact name, and then click your custom command.</span></span>

<span data-ttu-id="25820-170"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="25820-170"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

