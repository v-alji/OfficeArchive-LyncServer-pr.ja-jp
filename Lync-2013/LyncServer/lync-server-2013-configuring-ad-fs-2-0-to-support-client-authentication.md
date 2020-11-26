---
title: 'Lync Server 2013: クライアント認証をサポートするように AD FS 2.0 を構成する'
description: 'Lync Server 2013: クライアント認証をサポートするように AD FS 2.0 を構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring AD FS 2.0 to support client authentication
ms:assetid: 4d93d400-ccaa-4da8-a71b-d05d7ba79d93
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn308565(v=OCS.15)
ms:contentKeyID: 54973687
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 156eb6d7e8af85dec04601ab8f88c55181db20d5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433396"
---
# <a name="configuring-ad-fs-20-to-support-client-authentication-in-lync-server-2013"></a><span data-ttu-id="37556-103">Lync Server 2013 でのクライアント認証をサポートするように AD FS 2.0 を構成する</span><span class="sxs-lookup"><span data-stu-id="37556-103">Configuring AD FS 2.0 to support client authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="37556-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="37556-104">

<span> </span></span></span>

<span data-ttu-id="37556-105">_**最終更新日:** 2013-07-03_</span><span class="sxs-lookup"><span data-stu-id="37556-105">_**Topic Last Modified:** 2013-07-03_</span></span>

<span data-ttu-id="37556-106">AD FS 2.0 でスマート カードを使用した認証をサポートできるように構成可能な認証の種類が 2 つあります。</span><span class="sxs-lookup"><span data-stu-id="37556-106">There are two possible authentication types that can be configured to allow AD FS 2.0 to support authentication using smart cards:</span></span>

  - <span data-ttu-id="37556-107">フォーム ベース認証 (FBA)</span><span class="sxs-lookup"><span data-stu-id="37556-107">Forms-based authentication (FBA)</span></span>

  - <span data-ttu-id="37556-108">トランスポート層セキュリティ クライアント認証</span><span class="sxs-lookup"><span data-stu-id="37556-108">Transport Layer Security Client Authentication</span></span>

<span data-ttu-id="37556-109">フォーム ベース認証を使用すると、ユーザー名/パスワードを使用した認証またはスマート カードと PIN を使用した認証をユーザーに許可できる Web ページを開発できます。</span><span class="sxs-lookup"><span data-stu-id="37556-109">Using forms-based authentication, you can develop a web page that allows users to authenticate either by using their username/password or by using their smart card and PIN.</span></span> <span data-ttu-id="37556-110">このトピックでは、AD FS 2.0 でトランスポート層セキュリティ クライアント認証を実装する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="37556-110">This topic focuses on how to implement Transport Layer Security Client Authentication with AD FS 2.0.</span></span> <span data-ttu-id="37556-111">AD FS 2.0 認証の種類の詳細については、「AD FS 2.0: でローカル認証の種類を変更する方法」を参照してください [https://go.microsoft.com/fwlink/p/?LinkId=313384](https://go.microsoft.com/fwlink/p/?linkid=313384) 。</span><span class="sxs-lookup"><span data-stu-id="37556-111">For more information about AD FS 2.0 authentication types, see AD FS 2.0: How to Change the Local Authentication Type at [https://go.microsoft.com/fwlink/p/?LinkId=313384](https://go.microsoft.com/fwlink/p/?linkid=313384).</span></span>

<div>


<span data-ttu-id="37556-112">**クライアント認証をサポートするように AD FS 2.0 を構成するには**</span><span class="sxs-lookup"><span data-stu-id="37556-112">**To Configure AD FS 2.0 to Support Client Authentication**</span></span>

1.  <span data-ttu-id="37556-113">ドメイン管理者のアカウントを使用して AD FS 2.0 コンピューターにログインします。</span><span class="sxs-lookup"><span data-stu-id="37556-113">Log in to the AD FS 2.0 computer using a Domain Admin account.</span></span>

2.  <span data-ttu-id="37556-114">エクスプローラーを起動します。</span><span class="sxs-lookup"><span data-stu-id="37556-114">Launch Windows Explorer.</span></span>

3.  <span data-ttu-id="37556-115">C: \\ inetpub \\ adfs \\ ls を参照してください</span><span class="sxs-lookup"><span data-stu-id="37556-115">Browse to C:\\inetpub\\adfs\\ls</span></span>

4.  <span data-ttu-id="37556-116">既存の web.config ファイルのバックアップ コピーを作成します。</span><span class="sxs-lookup"><span data-stu-id="37556-116">Make a backup copy of the existing web.config file.</span></span>

5.  <span data-ttu-id="37556-117">メモ帳を使用して既存の web.config ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="37556-117">Open the existing web.config file using Notepad.</span></span>

6.  <span data-ttu-id="37556-118">メニュー バーの [**編集**] をクリックし、[**検索**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="37556-118">From the Menu bar, select **Edit** and then select **Find**.</span></span>

7.  <span data-ttu-id="37556-119">を検索 **\<localAuthenticationTypes\>** します。</span><span class="sxs-lookup"><span data-stu-id="37556-119">Search for **\<localAuthenticationTypes\>**.</span></span>
    
    <span data-ttu-id="37556-120">4 つの認証の種類が 1 行に 1 つずつ表示されます。</span><span class="sxs-lookup"><span data-stu-id="37556-120">Note that there are four authentication types listed, one per line.</span></span>

8.  <span data-ttu-id="37556-121">TLSClient 認証の種類を含む行をセクションの一覧の一番上に移動します。</span><span class="sxs-lookup"><span data-stu-id="37556-121">Move the line containing the TLSClient authentication type to the top of the list in the section.</span></span>

9.  <span data-ttu-id="37556-122">web.config ファイルを保存して閉じます。</span><span class="sxs-lookup"><span data-stu-id="37556-122">Save and Close the web.config file.</span></span>

10. <span data-ttu-id="37556-123">管理者特権でコマンド プロンプトを起動します。</span><span class="sxs-lookup"><span data-stu-id="37556-123">Launch a Command Prompt with elevated privileges.</span></span>

11. <span data-ttu-id="37556-124">次のコマンドを実行して IIS を再起動します。</span><span class="sxs-lookup"><span data-stu-id="37556-124">Restart IIS by running the following command:</span></span>
    
        IISReset /Restart /NoForce

<span data-ttu-id="37556-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="37556-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

