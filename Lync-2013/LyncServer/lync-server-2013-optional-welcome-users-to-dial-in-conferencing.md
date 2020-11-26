---
title: 'Lync Server 2013: (オプション) ダイヤルイン会議へのユーザーの受け入れ'
description: 'Lync Server 2013: (オプション) ダイヤルイン会議へのユーザーのようこそ。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: (Optional) Welcome users to dial-in conferencing
ms:assetid: caa4fd61-f506-4c09-bb5b-1aa260d7a720
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398846(v=OCS.15)
ms:contentKeyID: 48185443
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0d33c7184a8cf22699b4ebe8d8ea8b4ef1c133a3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424843"
---
# <a name="optional-welcome-users-to-dial-in-conferencing-in-lync-server-2013"></a><span data-ttu-id="7b6c5-103">(オプション) Lync Server 2013 でのダイヤルイン会議へのユーザーの受け入れ</span><span class="sxs-lookup"><span data-stu-id="7b6c5-103">(Optional) Welcome users to dial-in conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7b6c5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7b6c5-104">

<span> </span></span></span>

<span data-ttu-id="7b6c5-105">_**最終更新日:** 2012-09-30_</span><span class="sxs-lookup"><span data-stu-id="7b6c5-105">_**Topic Last Modified:** 2012-09-30_</span></span>

<span data-ttu-id="7b6c5-106">ダイヤルイン会議を構成し、テストを行って正常に機能していることを確認したら、最初の PIN や、ダイヤルイン会議の設定の web ページへのリンクなどの基本的な手順を含め、ユーザーのために最初の暗証番号 (Pin) を設定して、機能の利用状況をユーザーに通知する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b6c5-106">After you configure dial-in conferencing and test to verify that it is functioning properly, you should set initial personal identification numbers (PINs) for users and notify users about the availability of the feature, including introductory instructions such as the initial PIN and the link to the Dial-in Conferencing Settings webpage.</span></span> <span data-ttu-id="7b6c5-107">この手順は省略可能です。</span><span class="sxs-lookup"><span data-stu-id="7b6c5-107">This step is optional.</span></span> <span data-ttu-id="7b6c5-108">通常は、ユーザーが Pin をリセットするために、 **Set-CsClientPin** コマンドレットを使用しますが、情報を含むウェルカムメールを送信する場合は、このトピックの手順を初めて使用することができます。</span><span class="sxs-lookup"><span data-stu-id="7b6c5-108">Typically, you use the **Set-CsClientPin** cmdlet to reset PINs, but you can use the procedure in this topic the first time if you want to send a welcome email with the information.</span></span> <span data-ttu-id="7b6c5-109">ようこそメールを送信しない場合は、代わりに **Set-CsClientPin** を使用できます。</span><span class="sxs-lookup"><span data-stu-id="7b6c5-109">If you do not want to send the email, you can use **Set-CsClientPin** instead.</span></span>

<span data-ttu-id="7b6c5-110">PIN を設定し、1 人のユーザーにようこそメールを送信する場合は、**Set-CsPinSendCAWelcomeMail** スクリプトを使用できます。</span><span class="sxs-lookup"><span data-stu-id="7b6c5-110">You can use the **Set-CsPinSendCAWelcomeMail** script to set the PIN and send a welcome email to a single user.</span></span> <span data-ttu-id="7b6c5-111">既定では、スクリプトは既に設定されている場合、PIN はリセットされませんが、 **force** パラメーターを使用して pin を強制的にリセットすることができます。</span><span class="sxs-lookup"><span data-stu-id="7b6c5-111">By default, the script does not reset a PIN if it is already set, but you can use the **Force** parameter to force reset a PIN.</span></span> <span data-ttu-id="7b6c5-112">電子メール メッセージは、SMTP (Simple Mail Transfer Protocol) を使用して送信されます。</span><span class="sxs-lookup"><span data-stu-id="7b6c5-112">The email message is sent using Simple Mail Transfer Protocol (SMTP).</span></span>

<span data-ttu-id="7b6c5-113">**Set-CsPinSendCAWelcomeMail** スクリプトを繰り返し実行して PIN を設定し、ユーザー グループに電子メールを送信するスクリプトを作成できます。</span><span class="sxs-lookup"><span data-stu-id="7b6c5-113">You can create a script that runs the **Set-CsPinSendCAWelcomeMail** script iteratively to set PINs and send email to a group of users.</span></span> <span data-ttu-id="7b6c5-114">メールテンプレート ( **CAWelcomeEmailTemplate.html** ファイル) を変更して、イントラネットページへのリンクを追加したり、メールのテキストを変更したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="7b6c5-114">You can modify the email template (that is, the **CAWelcomeEmailTemplate.html** file) to add more links to intranet pages or modify the email text.</span></span>

<div>

## <a name="to-set-an-initial-pin-and-send-welcome-email"></a><span data-ttu-id="7b6c5-115">初期の PIN を設定し、[ようこそ] のメールを送信するには</span><span class="sxs-lookup"><span data-stu-id="7b6c5-115">To set an initial PIN and send welcome email</span></span>

1.  <span data-ttu-id="7b6c5-116">RTCUniversalServerAdmins group のメンバーとしてログオンします。</span><span class="sxs-lookup"><span data-stu-id="7b6c5-116">Log on as a member of the RTCUniversalServerAdmins group.</span></span>

2.  <span data-ttu-id="7b6c5-117">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="7b6c5-117">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="7b6c5-118">コマンド プロンプトで次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="7b6c5-118">Run the following at the command prompt:</span></span>
    
        Set-CsPinSendCAWelcomeMail -UserUri <user identifier>
        -From <email address of sender> [-Subject <subject for email message>]
        [-UserEmailAddress <destination email address>]
        [-Cc <email address of recipients who receive copy of email>]
        [-Bcc <email address of recipients who receive blind copies>]
        [-TemplatePath <path for email template>]
        [-SmtpServer] <SMTP server name>]
        [-BodyAsPlainText] [-UseSsl]
        [-Pin <new numeric PIN>] [-Force] `
        [-Credential <SMTP server credentials used to send email with the specified From address>]
    
    <span data-ttu-id="7b6c5-119">**Smtpserver**   既定では、スクリプトはこのパラメーターに対して予約された環境変数 **$PSEmailServer** の値を使います。</span><span class="sxs-lookup"><span data-stu-id="7b6c5-119">**SmtpServer**   By default, the script uses the value of the reserved environment variable **$PSEmailServer** for this parameter.</span></span> <span data-ttu-id="7b6c5-120">**$PSEmailServer** 変数が設定されていない場合は、このパラメーターを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b6c5-120">If the **$PSEmailServer** variable is not set, you must specify this parameter.</span></span>
    
    <span data-ttu-id="7b6c5-121">**資格情報**   既定では、スクリプトは現在のユーザーの資格情報を使用します。</span><span class="sxs-lookup"><span data-stu-id="7b6c5-121">**Credential**   By default, the script uses the credentials of the current user.</span></span> <span data-ttu-id="7b6c5-122">現在のユーザーが、指定された差出人アドレスに代わってメールを送信するアクセス許可を持っていない場合は、このパラメーターを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b6c5-122">If the current user does not have permission to send email on behalf of the specified From address, you must specify this parameter.</span></span> <span data-ttu-id="7b6c5-123">一般的な規則として、差出人アドレスとしてメールアドレスを指定しない場合は、このパラメーターを指定します。</span><span class="sxs-lookup"><span data-stu-id="7b6c5-123">As a general rule, specify this parameter if you do not specify your email address as the From address.</span></span>
    
    <span data-ttu-id="7b6c5-124">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="7b6c5-124">For example:</span></span>
    
        Set-CsPinSendCAWelcomeMail -UserUri "bob@contoso.com"
        -From "marco@contoso.com"
    
    <span data-ttu-id="7b6c5-125">この例では、新しい PIN を作成し、Marco からボブにウェルカムメールを送信します。</span><span class="sxs-lookup"><span data-stu-id="7b6c5-125">This example creates a new PIN and then sends a welcome email from Marco to Bob.</span></span> <span data-ttu-id="7b6c5-126">既定のテンプレートにある電子メール テキストを使用し、HTML 形式で電子メール メッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="7b6c5-126">It uses the email text from the default template and creates the email message in HTML format.</span></span> <span data-ttu-id="7b6c5-127">既定の件名は "会議へようこそ" です。</span><span class="sxs-lookup"><span data-stu-id="7b6c5-127">The default Subject is "Welcome to Dial In Conferencing".</span></span>
    
    <span data-ttu-id="7b6c5-128">もう1つの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="7b6c5-128">Another example:</span></span>
    
        Set-CsPinSendCAWelcomeMail -UserUri "bob@contoso.com"
        -From "marco@contoso.com" -Subject "Your new dial-in conferencing PIN"
        -Pin "383042650" -Force
        -Credential Admin@contoso.com -UseSsl
    
    <span data-ttu-id="7b6c5-129">次の例では、ボブが既存の PIN を持っている場合でも、Bob に対して "383042650" という新しい PIN を強制的に使用します。その後、Marco からボブにウェルカムメールを送信します。</span><span class="sxs-lookup"><span data-stu-id="7b6c5-129">This example forces a new PIN with a value of "383042650" for Bob, even though Bob had an existing PIN, and then sends a welcome email from Marco to Bob.</span></span> <span data-ttu-id="7b6c5-130">Credential パラメーターが指定されているため、コマンドを実行するユーザーはパスワードを入力するよう求められます。</span><span class="sxs-lookup"><span data-stu-id="7b6c5-130">Because the Credential parameter is specified, the person running the command is prompted to enter a password.</span></span> <span data-ttu-id="7b6c5-131">メールは、Secure Sockets Layer (SSL) を使って送信されます。</span><span class="sxs-lookup"><span data-stu-id="7b6c5-131">The email is sent by using the Secure Sockets Layer (SSL).</span></span>

<span data-ttu-id="7b6c5-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7b6c5-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

