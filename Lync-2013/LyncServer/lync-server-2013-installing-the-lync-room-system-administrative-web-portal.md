---
title: 'Lync Server 2013: Lync Room System 管理 Web ポータルをインストールする'
description: 'Lync Server 2013: Lync Room System 管理 Web ポータルをインストールします。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Installing the Lync Room System Administrative Web Portal
ms:assetid: dd19e368-c338-4e21-a40d-6439d46a9748
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn436326(v=OCS.15)
ms:contentKeyID: 56737622
ms.date: 04/09/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0fba239346d75142bb4009c58e0ac67e8e1f3bcb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427006"
---
# <a name="installing-the-lync-room-system-administrative-web-portal-in-lync-server-2013"></a><span data-ttu-id="6e04f-103">Installing the Lync Room System Administrative Web Portal in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6e04f-103">Installing the Lync Room System Administrative Web Portal in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6e04f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6e04f-104">

<span> </span></span></span>

<span data-ttu-id="6e04f-105">_**最終更新日:** 2015-04-09_</span><span class="sxs-lookup"><span data-stu-id="6e04f-105">_**Topic Last Modified:** 2015-04-09_</span></span>

<span data-ttu-id="6e04f-106">Microsoft Lync Room System 管理 Web ポータルは、Microsoft ダウンロードセンターからダウンロードでき [https://go.microsoft.com/fwlink/p/?LinkId=324044](https://go.microsoft.com/fwlink/p/?linkid=324044) ます。</span><span class="sxs-lookup"><span data-stu-id="6e04f-106">You can download the Microsoft Lync Room System Administrative Web Portal from the Microsoft Download Center at [https://go.microsoft.com/fwlink/p/?LinkId=324044](https://go.microsoft.com/fwlink/p/?linkid=324044).</span></span>

<span data-ttu-id="6e04f-107">Lync Room System 管理 Web ポータルをインストールするには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="6e04f-107">To install the Lync Room System Administrative Web Portal, use the following steps.</span></span>

1.  <span data-ttu-id="6e04f-108">Lync Server 管理シェルで次のコマンドレットを実行して、信頼されているアプリケーションポートを構成します。</span><span class="sxs-lookup"><span data-stu-id="6e04f-108">Configure the Trusted Application Port by running the following cmdlet in Lync Server Management Shell:</span></span>
    
        Set-CsWebServer -Identity POOLFQDN -MeetingRoomAdminPortalInternalListeningPort 4456 -MeetingRoomAdminPortalExternalListeningPort 4457

2.  <span data-ttu-id="6e04f-109">会議室ポータルをインストールするには、 **LyncRoomAdminPortal.exe** をダウンロードしてから、管理者として実行します。</span><span class="sxs-lookup"><span data-stu-id="6e04f-109">To install the Meeting Room Portal, download **LyncRoomAdminPortal.exe** and then run it as an administrator.</span></span>

3.  <span data-ttu-id="6e04f-110">Web.config ファイルを次の場所から開きます。</span><span class="sxs-lookup"><span data-stu-id="6e04f-110">Open the Web.config file from the following location:</span></span>
    
    <span data-ttu-id="6e04f-111">% Program Files% \\ Microsoft Lync Server 2013 \\ Web コンポーネント \\ 会議室ポータルの \\ Int \\ ハンドラー</span><span class="sxs-lookup"><span data-stu-id="6e04f-111">%Program Files%\\Microsoft Lync Server 2013\\Web Components\\Meeting Room Portal\\Int\\Handler</span></span>\\

4.  <span data-ttu-id="6e04f-112">Web.Config ファイルで、「Lync Room System 管理ポータルの前提条件を設定する」セクションの「手順2で作成したユーザー名に PortalUserName を変更します (手順は LRSApp の推奨名)。</span><span class="sxs-lookup"><span data-stu-id="6e04f-112">In the Web.Config file, change the PortalUserName to the username created in Step 2 under the section “Configuring Prerequisites for Lync Room System Admin Portal” (the recommended name in the step is LRSApp):</span></span>
    
        <add key="PortalUserName" value="sip:LRSApp@domain.com" />

5.  <span data-ttu-id="6e04f-113">LRS 管理ポータルは信頼できるアプリケーションであるため、ポータル構成でパスワードを入力する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="6e04f-113">Because the LRS Admin Portal is a trusted application, you do not need to provide the password in the portal configuration.</span></span> <span data-ttu-id="6e04f-114">このユーザーがローカル レジストラーとは別のレジストラーを使用している場合、Web.Config ファイルで次の行を追加してレジストラを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e04f-114">If this user is using a different registrar than local registrar, you need to specify the registrar for it by adding the following line in the Web.Config file:</span></span>
    
        <add key="PortalUserRegistrarFQDN" value="pool-xxxx.domain.com" />

6.  <span data-ttu-id="6e04f-115">5061 以外のポートが使用されている場合は、Web.Config ファイルに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="6e04f-115">If the port used is other than 5061, add the following line in the Web.Config file:</span></span>
    
        <add key="PortalUserRegistrarPort" value="5061" />

<div>

## <a name="verifying-installation-of-the-lync-room-system-administrative-web-portal"></a><span data-ttu-id="6e04f-116">Lync Room System 管理 Web ポータルのインストールを確認する</span><span class="sxs-lookup"><span data-stu-id="6e04f-116">Verifying Installation of the Lync Room System Administrative Web Portal</span></span>

<span data-ttu-id="6e04f-117">Lync Room System 管理 Web ポータルのインストールを確認するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="6e04f-117">To verify installation of the Lync Room System Administrative Web Portal, do the following:</span></span>


1.  <span data-ttu-id="6e04f-118">フロントエンド サーバーで、次の URL を参照します。</span><span class="sxs-lookup"><span data-stu-id="6e04f-118">On a Front End server, browse to the following URL:</span></span>
    
    <span data-ttu-id="6e04f-119"> https:// \<fe-server\> /lrs</span><span class="sxs-lookup"><span data-stu-id="6e04f-119">https://\<fe-server\>/lrs</span></span>
    
    <span data-ttu-id="6e04f-120">下記の画像のように、エラーが表示されないようにします。</span><span class="sxs-lookup"><span data-stu-id="6e04f-120">You should not see any errors, as shown in the following image:</span></span>
    
    <span data-ttu-id="6e04f-121">![Lync Room System、管理用ポータル サインイン画面](images/Dn436326.050bcf70-2f3b-46b2-9b96-ebd12679b713(OCS.15).png "Lync Room System、管理用ポータル サインイン画面")</span><span class="sxs-lookup"><span data-stu-id="6e04f-121">![Lync Room System Admin Portal Sign In screen](images/Dn436326.050bcf70-2f3b-46b2-9b96-ebd12679b713(OCS.15).png "Lync Room System Admin Portal Sign In screen")</span></span>

2.  <span data-ttu-id="6e04f-122">エラーが表示されない場合は、トポロジ内の他のいずれかのコンピューターから次の URL へのアクセスを試行します。</span><span class="sxs-lookup"><span data-stu-id="6e04f-122">If you do not see any errors, try accessing the following URL from any other computer in the topology:</span></span>
    
    <span data-ttu-id="6e04f-123"> https:// \<fe-server\> /lrs</span><span class="sxs-lookup"><span data-stu-id="6e04f-123">https://\<fe-server\>/lrs</span></span>
    
    <span data-ttu-id="6e04f-124">このページにアクセスするには、「」の「自動クライアントサインイン用の DNS レコード」の説明に従って DNS レコードを追加する必要があり [https://go.microsoft.com/fwlink/p/?LinkId=318056](https://go.microsoft.com/fwlink/p/?linkid=318056) ます。</span><span class="sxs-lookup"><span data-stu-id="6e04f-124">To access the page, you will need to add the DNS records as described in “Required DNS Records for Automatic Client Sign-In” at [https://go.microsoft.com/fwlink/p/?LinkId=318056](https://go.microsoft.com/fwlink/p/?linkid=318056).</span></span>

<span data-ttu-id="6e04f-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6e04f-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

