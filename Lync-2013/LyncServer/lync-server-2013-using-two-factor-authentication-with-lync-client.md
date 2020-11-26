---
title: 'Lync Server 2013: Lync クライアントで2要素認証を使用する'
description: 'Lync Server 2013: Lync クライアントで2要素認証を使用します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using two-factor authentication with Lync client
ms:assetid: d4136e61-c3ab-4b26-85c8-c1b2c24f5ee3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn338071(v=OCS.15)
ms:contentKeyID: 55115593
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dbfde1d04d4e641c8fbe4817ffce214df891b565
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438688"
---
# <a name="using-two-factor-authentication-with-lync-client-and-lync-server-2013"></a><span data-ttu-id="c5a28-103">Lync クライアントおよび Lync Server 2013 での2要素認証の使用</span><span class="sxs-lookup"><span data-stu-id="c5a28-103">Using two-factor authentication with Lync client and Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c5a28-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c5a28-104">

<span> </span></span></span>

<span data-ttu-id="c5a28-105">_**最終更新日:** 2013-07-11_</span><span class="sxs-lookup"><span data-stu-id="c5a28-105">_**Topic Last Modified:** 2013-07-11_</span></span>

<span data-ttu-id="c5a28-106">このトピックでは、Lync 2013 クライアントで2要素認証を利用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c5a28-106">This topic described how to take advantage of two-factor authentication with Lync 2013 client.</span></span>

<div>

## <a name="sign-in-to-lync-2013-for-the-first-time"></a><span data-ttu-id="c5a28-107">Lync 2013 に初めてサインインする</span><span class="sxs-lookup"><span data-stu-id="c5a28-107">Sign in to Lync 2013 for the first time</span></span>

<span data-ttu-id="c5a28-108">Lync のサインイン情報は、Lync 2013 がインストールされているときに自動的に構成されます。</span><span class="sxs-lookup"><span data-stu-id="c5a28-108">Your Lync sign-in information is usually configured automatically when Lync 2013 is installed.</span></span> <span data-ttu-id="c5a28-109">ただし、初めて Lync を使用する場合は、クライアントを手動で開始しなければならない場合があります。</span><span class="sxs-lookup"><span data-stu-id="c5a28-109">But the first time you use Lync, you might have to manually start the client.</span></span>

<span data-ttu-id="c5a28-110">**Lync に初めてサインインするには**</span><span class="sxs-lookup"><span data-stu-id="c5a28-110">**To sign in to Lync for the first time**</span></span>

1.  <span data-ttu-id="c5a28-111">組織のネットワークにログオンします。</span><span class="sxs-lookup"><span data-stu-id="c5a28-111">Log on to your organization’s network.</span></span>

2.  <span data-ttu-id="c5a28-112">[ **Start** \> **All Programs** \> **Microsoft lync \> lync 2013** のすべてのプログラムを起動する] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5a28-112">Select **Start** \> **All Programs** \> **Microsoft Lync \> Lync 2013**.</span></span>
    
    <span data-ttu-id="c5a28-113">Lync のサインイン画面が表示されます。</span><span class="sxs-lookup"><span data-stu-id="c5a28-113">You should see the Lync sign-in screen.</span></span>
    
      - <span data-ttu-id="c5a28-114">[サインイン アドレス] ボックスが既に入力されている場合は、表示されているアドレスが正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="c5a28-114">If the sign-in address box is already filled in, confirm that the address shown is correct.</span></span>
    
      - <span data-ttu-id="c5a28-115">正しくない場合、またはボックスが空の場合は、Lync のサインインアドレス (通常はメールアドレスと同じ) を入力します。</span><span class="sxs-lookup"><span data-stu-id="c5a28-115">If it’s not correct, or if the box is empty, enter your Lync sign-in address (this is usually the same as your email address).</span></span>
    
      - <span data-ttu-id="c5a28-116">パスワードを入力するボックスが空の場合は、パスワードを追加します。</span><span class="sxs-lookup"><span data-stu-id="c5a28-116">If an empty password box is displayed, add your password.</span></span>

3.  <span data-ttu-id="c5a28-117">[**サインイン**] を選びます。</span><span class="sxs-lookup"><span data-stu-id="c5a28-117">Select **Sign-in**.</span></span>

</div>

<div>

## <a name="sign-out-of-lync"></a><span data-ttu-id="c5a28-118">Lync からサインアウトする</span><span class="sxs-lookup"><span data-stu-id="c5a28-118">Sign out of Lync</span></span>

<span data-ttu-id="c5a28-119">Lync の使用が完了したら、[ファイル] メニューから表示を閉じたり、セッションからサインアウトしたり、プログラムから退出したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="c5a28-119">When you’re finished using Lync, you can close the display, sign out of your session, or exit from the program, all from the File menu.</span></span> <span data-ttu-id="c5a28-120">次の表で、オプションの違いについて説明します。</span><span class="sxs-lookup"><span data-stu-id="c5a28-120">The following table explains the differences in the options.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c5a28-121">オプション</span><span class="sxs-lookup"><span data-stu-id="c5a28-121">Option</span></span></th>
<th><span data-ttu-id="c5a28-122">機能</span><span class="sxs-lookup"><span data-stu-id="c5a28-122">What it does</span></span></th>
<th><span data-ttu-id="c5a28-123">実行する方法</span><span class="sxs-lookup"><span data-stu-id="c5a28-123">How to perform it</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5a28-124">閉じる</span><span class="sxs-lookup"><span data-stu-id="c5a28-124">Close</span></span></p></td>
<td><p><span data-ttu-id="c5a28-125">Lync ディスプレイを閉じますが、ユーザー ID で識別された Lync セッションは引き続き実行できます。</span><span class="sxs-lookup"><span data-stu-id="c5a28-125">Closes your Lync display but lets the Lync session identified with your user ID continue to run.</span></span> <span data-ttu-id="c5a28-126">したがって、引き続き通知を受け取り、他のユーザーと対話できます。</span><span class="sxs-lookup"><span data-stu-id="c5a28-126">This is so you can continue to get notifications and interact with others.</span></span></p>
<p><span data-ttu-id="c5a28-127">タスクバーまたは画面の下部にある通知領域の Lync アイコンをクリックすると、いつでも表示を元に戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="c5a28-127">You can get the display back at any time by clicking the Lync icon on the taskbar or the notification area at the bottom of your screen.</span></span></p></td>
<td><p><span data-ttu-id="c5a28-128">Lync メインウィンドウで、次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="c5a28-128">On the Lync main window, do one of the following:</span></span></p>
<ol>
<li><p><span data-ttu-id="c5a28-129">[<strong>オプション</strong>] ボタンを選択し、[<strong>ファイル</strong>を閉じる] を選択し &gt; <strong>Close</strong>ます。</span><span class="sxs-lookup"><span data-stu-id="c5a28-129">Select the <strong>Options</strong> button, then select <strong>File</strong> &gt; <strong>Close</strong>.</span></span></p></li>
<li><p><span data-ttu-id="c5a28-130">ウィンドウの右上隅にある [<strong>閉じる</strong>] ボタン (X) をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c5a28-130">Click the <strong>Close</strong> button (X) in the upper-right corner of the window.</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5a28-131">サインアウトする</span><span class="sxs-lookup"><span data-stu-id="c5a28-131">Sign out</span></span></p></td>
<td><p><span data-ttu-id="c5a28-132">ユーザー ID に関連付けられた Lync セッションを終了しますが、Lync はバックグラウンドで実行され続けます。</span><span class="sxs-lookup"><span data-stu-id="c5a28-132">Ends the Lync session associated with your user ID, but Lync continues to run in the background.</span></span> <span data-ttu-id="c5a28-133">サインアウトすると、サインイン ウィンドウが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c5a28-133">When you sign out, the sign-in window will appear.</span></span></p>
<div>

> [!TIP]  
> <span data-ttu-id="c5a28-p105">[<STRONG>サインイン情報を削除</STRONG>] を選ぶと、サインアウトするときにコンピューターからログオン ID とパスワードの記録を削除できます。このようにすると、サポート担当者が行うサインインの問題のトラブルシューティングが容易になることがあります。また、権限のないユーザーがあなたの資格情報でログインすることは難しくなるため、サインイン情報のセキュリティも確保できます。</span><span class="sxs-lookup"><span data-stu-id="c5a28-p105">Select <STRONG>Delete my sign-in information</STRONG> when you sign out to remove the record of your logon ID and password from the computer. Doing this might make it easier for support people to troubleshoot sign-in issues. It can also help ensure your sign-in information is more secure by making it difficult for unauthorized users to log on with your credentials.</span></span>


</div></td>
<td><p><span data-ttu-id="c5a28-137">Lync メインウィンドウで、[<strong>オプション</strong>] ボタンを選択し、[<strong>ファイル</strong>]、[サインアウト] の順に選択し &gt; <strong>Sign Out</strong>ます。</span><span class="sxs-lookup"><span data-stu-id="c5a28-137">On the Lync main window, select the <strong>Options</strong> button, then select <strong>File</strong> &gt; <strong>Sign Out</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5a28-138">終了する</span><span class="sxs-lookup"><span data-stu-id="c5a28-138">Exit</span></span></p></td>
<td><p><span data-ttu-id="c5a28-139">Lync セッションが終了し、コンピューター上の Lync がシャットダウンされます。</span><span class="sxs-lookup"><span data-stu-id="c5a28-139">Ends your Lync session and shuts down Lync on your computer.</span></span> <span data-ttu-id="c5a28-140">終了後、Lync を再起動する場合は、 <strong>Start</strong> [ &gt; <strong>All Programs</strong> &gt; <strong>Microsoft lync</strong> &gt; <strong>lync 2013</strong>のすべてのプログラムを起動する] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c5a28-140">After exiting, if you want to restart Lync, select <strong>Start</strong> &gt; <strong>All Programs</strong> &gt; <strong>Microsoft Lync</strong> &gt; <strong>Lync 2013</strong>.</span></span></p></td>
<td><p><span data-ttu-id="c5a28-141">Lync メインウィンドウで、[<strong>オプション</strong>] ボタンを選択し、[<strong>ファイル</strong>終了] を選択し &gt; <strong>Exit</strong>ます。</span><span class="sxs-lookup"><span data-stu-id="c5a28-141">On the Lync main window, select the <strong>Options</strong> button, then select <strong>File</strong> &gt; <strong>Exit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="sign-in-to-lync-with-a-smart-card"></a><span data-ttu-id="c5a28-142">スマートカードを使って Lync にサインインする</span><span class="sxs-lookup"><span data-stu-id="c5a28-142">Sign in to Lync with a Smart Card</span></span>

<span data-ttu-id="c5a28-143">一部の組織では、Lync 2013 ユーザーのセキュリティを強化するために、2要素認証と呼ばれるマルチステップのサインインプロセスを使用しています。</span><span class="sxs-lookup"><span data-stu-id="c5a28-143">Some organizations now use a multi-step sign-in process, called two-factor authentication, to increase security for their Lync 2013 users.</span></span> <span data-ttu-id="c5a28-144">このオプションを使用することが予想される場合は、Lync にサインインするには「スマートカード」が必要です。</span><span class="sxs-lookup"><span data-stu-id="c5a28-144">If you’re expected to use this option, you’ll need a “smart card” to sign in to Lync.</span></span> <span data-ttu-id="c5a28-145">スマートカードには、物理と仮想の2種類があります。</span><span class="sxs-lookup"><span data-stu-id="c5a28-145">Smart cards come in two varieties, physical and virtual:</span></span>

  - <span data-ttu-id="c5a28-146">**物理**   クレジットカードのサイズについて。</span><span class="sxs-lookup"><span data-stu-id="c5a28-146">**Physical**   About the size of a credit card.</span></span> <span data-ttu-id="c5a28-147">ログインするときにスマート カード リーダーに挿入します。</span><span class="sxs-lookup"><span data-stu-id="c5a28-147">You insert it into a smart card reader when you log in.</span></span>

  - <span data-ttu-id="c5a28-148">**仮想**   物理的なオブジェクトではありませんが、コンピューター上の特殊なチップに書き込まれる電子的な識別子であり、これにより、基本的にスマートカードがコンピューターに作成されます。</span><span class="sxs-lookup"><span data-stu-id="c5a28-148">**Virtual**   Not a physical object, but an electronic identifier that gets written to a special chip on your computer, which in essence builds the smart card into your computer.</span></span> <span data-ttu-id="c5a28-149">TPM (トラステッドプラットフォームモジュール) チップが含まれている Windows 8 コンピューターでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="c5a28-149">Available only for use with Windows 8 computers that contain the TPM (Trusted Platform Module) chip.</span></span>

<div>

## <a name="enroll-your-smart-card"></a><span data-ttu-id="c5a28-150">スマート カードを登録する</span><span class="sxs-lookup"><span data-stu-id="c5a28-150">Enroll your smart card</span></span>

<span data-ttu-id="c5a28-151">スマートカードでサインインするには、カードが "登録" されている必要があります。つまり、カードでユーザーの資格情報を識別する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5a28-151">Before you can sign in with a smart card, the card must be “enrolled”—that is, your user credentials have to be identified with the card.</span></span> <span data-ttu-id="c5a28-152">これは、カードが物理または仮想のどちらであるかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="c5a28-152">This is the case whether the card is physical or virtual.</span></span> <span data-ttu-id="c5a28-153">このプロセスは、Lync Server 管理者によって既に実行されている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c5a28-153">This process may already been carried out by your Lync Server administrator.</span></span> <span data-ttu-id="c5a28-154">実行されているかどうかがわからない場合は、確認してください。</span><span class="sxs-lookup"><span data-stu-id="c5a28-154">Check with them if you’re not sure whether that has been done.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c5a28-155">各仮想スマートカードは、それがインストールされているデバイスのみに関連付けられているため、使用する Windows 8 コンピューターごとに別のカードを登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5a28-155">Since each virtual smart card is associated only with the device it’s installed on, a separate card will need to be enrolled for each Windows 8 computer you use.</span></span>



</div>

<span data-ttu-id="c5a28-156">**スマート カードを手動で登録するには、次の操作を行います。**</span><span class="sxs-lookup"><span data-stu-id="c5a28-156">**To manually enroll your smart card**</span></span>

1.  <span data-ttu-id="c5a28-157">Lync を実行しているコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="c5a28-157">Log on to the computer you’ll be running Lync on.</span></span>

2.  <span data-ttu-id="c5a28-158">Internet Explorer を使って、組織の証明機関 Web 登録ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="c5a28-158">Using Internet Explorer, browse to your organization’s Certificate Authority Web Enrollment page.</span></span>
    
    <span data-ttu-id="c5a28-159">まだインストールしていない場合は、このリソースの web アドレスを Lync Server 管理者に確認してください。</span><span class="sxs-lookup"><span data-stu-id="c5a28-159">Ask your Lync Server administrator for the web address of this resource if you don’t already have it.</span></span> <span data-ttu-id="c5a28-160">URL は次のようになります。 https://MyCA.\ [companyname \] /certsrv] と表示されます。</span><span class="sxs-lookup"><span data-stu-id="c5a28-160">The URL will look something like this: https://MyCA.\[yourcompanyname\].com/certsrv.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="c5a28-161">Internet Explorer 10 を使っている場合は、この Web サイトを互換モードで見る必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="c5a28-161">If you’re using Internet Explorer 10, you may need to view this website in Compatibility Mode.</span></span>

    
    </div>

3.  <span data-ttu-id="c5a28-162">証明書のページにログオンするよう求められた場合は、ユーザーのドメイン アカウントを使ってログオンします (コンピューターの管理者としてはログオンしません)。</span><span class="sxs-lookup"><span data-stu-id="c5a28-162">When you’re prompted to log on to the certification page, log on using your domain account (rather than as administrator of your computer).</span></span>

4.  <span data-ttu-id="c5a28-163">Web サイトのようこそページで、[**証明書の要求**] を選びます。</span><span class="sxs-lookup"><span data-stu-id="c5a28-163">On the website Welcome Page, select **Request a certificate**.</span></span>

5.  <span data-ttu-id="c5a28-164">[**証明書の要求の詳細設定**] を選びます。</span><span class="sxs-lookup"><span data-stu-id="c5a28-164">Select **Advanced Request**.</span></span>

6.  <span data-ttu-id="c5a28-165">[**この CA への要求を作成し送信する。**] を選んで、[**次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c5a28-165">Select **Create and submit a request to this CA**, then click **Next**.</span></span>

7.  <span data-ttu-id="c5a28-166">「スマート カードの登録ステーション」というページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c5a28-166">Now you’ll see a page called Smart Card Enrollment Station.</span></span> <span data-ttu-id="c5a28-167">要求を承認して ActiveX コントロールをインストールし、[証明書の要求の詳細設定] を次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="c5a28-167">Approve the request to install the ActiveX control, and then complete the Advanced Certificate Request form as follows:</span></span>
    
    1.  <span data-ttu-id="c5a28-168">[**証明書のテンプレート**] ボックスの一覧から [**スマート カード ユーザー**] を選びます。</span><span class="sxs-lookup"><span data-stu-id="c5a28-168">Select **Smartcard user** from the **Certificate Template** dropdown list.</span></span>
    
    2.  <span data-ttu-id="c5a28-169">[**新しいキー セットを作成する**] を選びます。</span><span class="sxs-lookup"><span data-stu-id="c5a28-169">Select **Create new key set**.</span></span>
    
    3.  <span data-ttu-id="c5a28-170">スマート カードのラベルから製造元情報を確認し、[**CSP**] ボックスの一覧から製造元を選びます。</span><span class="sxs-lookup"><span data-stu-id="c5a28-170">Find the manufacturer information on the label of your smart card and select that manufacturer from the **CSP** dropdown list.</span></span>
    
    4.  <span data-ttu-id="c5a28-171">まだ選んでいない場合は、要求の形式として [**CSP**] を選びます。</span><span class="sxs-lookup"><span data-stu-id="c5a28-171">Select **CSP** as the Request Format, if it’s not already selected.</span></span>
    
    5.  <span data-ttu-id="c5a28-172">まだ選んでいない場合は、[ハッシュ アルゴリズム] ボックスの一覧から [**sha1**] を選びます。</span><span class="sxs-lookup"><span data-stu-id="c5a28-172">Select **sha1** from the Hash Algorithm dropdown list, if it’s not already selected.</span></span>
    
    6.  <span data-ttu-id="c5a28-173">証明書に分かりやすい名前を付けて、[**送信**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c5a28-173">Give your certificate a name you’ll recognize, and click **Submit**.</span></span>

8.  <span data-ttu-id="c5a28-174">登録ステーションに接続したカード リーダーに空のスマート カードを挿入し、[**登録**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c5a28-174">Now insert your blank smart card into the card reader attached to the enrollment station and click **Enroll**.</span></span>

9.  <span data-ttu-id="c5a28-175">要求メッセージが表示されたら、暗証番号 (PIN) を入力し、[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c5a28-175">When prompted, enter your personal identification number (PIN), and then click **OK**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="c5a28-176">スマート カードを登録するために使う特別な PIN をテクニカル サポート担当者から受け取っていない場合は、既定のスマート カード PIN の値である 12345678 を使用します。</span><span class="sxs-lookup"><span data-stu-id="c5a28-176">If your technical support person has not given you a special PIN to use to enroll your smart card, use the default smart card PIN value, which is 12345678.</span></span>

    
    </div>

10. <span data-ttu-id="c5a28-177">スマート カードを最初に使うときに PIN の変更をユーザーに強制するオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c5a28-177">Select the option to force the user (you) to change the PIN the first time the smart card is used.</span></span>

11. <span data-ttu-id="c5a28-178">登録ステーションに接続したカード リーダーに空のスマート カードを挿入し、[**登録**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c5a28-178">Now insert your blank smart card into the card reader attached to the enrollment station and click **Enroll**.</span></span>

12. <span data-ttu-id="c5a28-179">要求メッセージが表示されたら、暗証番号 (PIN) を入力し、[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c5a28-179">When prompted, enter your personal identification number (PIN), and then click **OK**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="c5a28-180">スマート カードを登録するために使う特別な PIN をテクニカル サポート担当者から受け取っていない場合は、既定のスマート カード PIN の値である 12345678 を使用します。</span><span class="sxs-lookup"><span data-stu-id="c5a28-180">If your technical support person has not given you a special PIN to use to enroll your smart card, use the default smart card PIN value, which is 12345678.</span></span>

    
    </div>

13. <span data-ttu-id="c5a28-181">スマート カードを最初に使うときに PIN の変更をユーザーに強制するオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c5a28-181">Select the option to force the user (you) to change the PIN the first time the smart card is used.</span></span>

14. <span data-ttu-id="c5a28-182">表示された証明書に記載されたユーザーの情報を確認したら、[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c5a28-182">Click **OK** to confirm that the certificate displayed has your information on it.</span></span>

15. <span data-ttu-id="c5a28-183">証明書が発行されたことを知らせる通知を確認したら、[**この証明書のインストール**] をクリックして登録プロセスを完了します。</span><span class="sxs-lookup"><span data-stu-id="c5a28-183">Once you see the notice that the certificate has been issued, click **Install this certificate** to complete the enrollment process.</span></span>

</div>

<div>

## <a name="sign-in-to-lync-with-your-smart-card-credentials"></a><span data-ttu-id="c5a28-184">スマートカードの資格情報を使用して Lync にサインインする</span><span class="sxs-lookup"><span data-stu-id="c5a28-184">Sign in to Lync with your smart card credentials</span></span>

<span data-ttu-id="c5a28-185">スマートカードを初めて使用する前に、Lync のサインインページで [ **サインイン情報を削除** する] をクリックすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="c5a28-185">Before you use your smart card for the first time, it’s recommended that you click **Delete my sign-in info** on the Lync sign-in page.</span></span> <span data-ttu-id="c5a28-186">これにより、コンピューターに保存されているすべてのサインイン情報がクリアされ、エラーの原因を取り除くことができます。</span><span class="sxs-lookup"><span data-stu-id="c5a28-186">Doing this clears any sign-in credentials stored on your computer, and eliminates a possible source of error.</span></span>

<span data-ttu-id="c5a28-187">**スマートカードの資格情報を使用して Lync にサインインするには**</span><span class="sxs-lookup"><span data-stu-id="c5a28-187">**To sign in to Lync with your smart card credentials**</span></span>

1.  <span data-ttu-id="c5a28-188">Lync クライアントを起動します。</span><span class="sxs-lookup"><span data-stu-id="c5a28-188">Start the Lync client.</span></span>

2.  <span data-ttu-id="c5a28-189">サインイン画面で、ユーザーのアカウント名を [**サインイン アドレス**] ボックスに入力し、[**サインイン**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c5a28-189">On the Sign in screen, type your sign in user account name in the **Sign-in address** box, and then click **Sign In**.</span></span>

3.  <span data-ttu-id="c5a28-190">仮想スマート カードを使っている場合は、この手順は省略します。</span><span class="sxs-lookup"><span data-stu-id="c5a28-190">If you are using a virtual smart card, skip this step.</span></span>
    
    <span data-ttu-id="c5a28-191">物理スマート カードを使っている場合は、メッセージが表示されたらスマート カードをスマート カード リーダーに挿入し、カードが認識されたら [**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c5a28-191">If you are using a physical smart card, insert the smart card into your smart card reader and prompted to do so, and then click **OK** when the card is detected.</span></span>

4.  <span data-ttu-id="c5a28-192">スマート カードの PIN 番号を入力し、[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c5a28-192">Type in the PIN number you for your smart card and then click **OK**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="c5a28-193">サポート担当者からスマート カードの PIN 番号が割り当てられなかった場合は、既定の値 (12345678) を入力します。</span><span class="sxs-lookup"><span data-stu-id="c5a28-193">If you were not assigned a smart card PIN number by your support person, use the default value, which is 12345678.</span></span>

    
    <span data-ttu-id="c5a28-194"></div>

</div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c5a28-194"></div>

</div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

