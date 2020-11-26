---
title: 'Lync Server 2013: スマートカード認証用のエンタープライズ CA の構成'
description: 'Lync Server 2013: スマートカード認証用のエンタープライズ CA の構成'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Enterprise CA for smart card authentication
ms:assetid: c24e0891-e108-4cb6-9902-c6a4c8e68455
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn308571(v=OCS.15)
ms:contentKeyID: 54973692
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 98044c96dd04d02fd87609918f309cf65227b133
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433151"
---
# <a name="configuring-enterprise-ca-for-smart-card-authentication-in-lync-server-2013"></a><span data-ttu-id="2a484-103">Lync Server 2013 でのスマートカード認証用のエンタープライズ CA の構成</span><span class="sxs-lookup"><span data-stu-id="2a484-103">Configuring Enterprise CA for smart card authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2a484-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2a484-104">

<span> </span></span></span>

<span data-ttu-id="2a484-105">_**最終更新日:** 2013-07-03_</span><span class="sxs-lookup"><span data-stu-id="2a484-105">_**Topic Last Modified:** 2013-07-03_</span></span>

<span data-ttu-id="2a484-106">以下のセクションでは、スマートカード認証をサポートするようにエンタープライズのルート証明機関 (CA) を構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2a484-106">The following section describes how to configure an Enterprise Root Certification Authority (CA) to support smart card authentication.</span></span> <span data-ttu-id="2a484-107">エンタープライズルート CA をインストールする方法については、「エンタープライズルート証明機関をインストールする」を参照してください [https://go.microsoft.com/fwlink/p/?LinkID=313364](https://go.microsoft.com/fwlink/p/?linkid=313364) 。</span><span class="sxs-lookup"><span data-stu-id="2a484-107">For information on how to install an Enterprise Root CA, see Install an Enterprise Root Certification Authority at [https://go.microsoft.com/fwlink/p/?LinkID=313364](https://go.microsoft.com/fwlink/p/?linkid=313364).</span></span>

<div>

## <a name="configuring-an-enterprise-root-certificate-authority-to-support-smart-card-authentication"></a><span data-ttu-id="2a484-108">スマートカード認証をサポートするようにエンタープライズルート証明機関を構成する</span><span class="sxs-lookup"><span data-stu-id="2a484-108">Configuring an Enterprise Root Certificate Authority to Support Smart Card Authentication</span></span>

<span data-ttu-id="2a484-109">スマート カード認証をサポートするようにエンタープライズ ルート CA を構成する方法を以下の手順で説明します。</span><span class="sxs-lookup"><span data-stu-id="2a484-109">The following steps describe how to configure an Enterprise Root CA to support Smart Card Authentication:</span></span>

1.  <span data-ttu-id="2a484-110">ドメイン管理者のアカウントを使用してエンタープライズ CA コンピューターにログインします。</span><span class="sxs-lookup"><span data-stu-id="2a484-110">Log in to the Enterprise CA computer using a Domain Admin account.</span></span>

2.  <span data-ttu-id="2a484-111">システム マネージャーを起動し、証明機関 Web 登録の役割がインストールされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2a484-111">Launch System Manager, and verify that the Certificate Authority Web Enrollment role is installed.</span></span>

3.  <span data-ttu-id="2a484-112">[**管理ツール**] メニューから **証明機関** 管理コンソールを開きます。</span><span class="sxs-lookup"><span data-stu-id="2a484-112">From the **Administrative Tools** menu, open the **Certification Authority** management console.</span></span>

4.  <span data-ttu-id="2a484-113">ナビゲーション ウィンドウで、[**証明機関**] を展開します。</span><span class="sxs-lookup"><span data-stu-id="2a484-113">In the Navigation pane, expand **Certification Authority**.</span></span>

5.  <span data-ttu-id="2a484-114">[**証明書テンプレート**] を右クリックし、[**新規作成**] をクリックして、[**発行する証明書テンプレート**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a484-114">Right click on **Certificate Templates**, select **New**, then select **Certificate Template to Issue**.</span></span>

6.  <span data-ttu-id="2a484-115">[**登録エージェント**]、[**スマート カード ユーザー**]、[**スマート カード ログオン**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="2a484-115">Select **Enrollment Agent**, **Smartcard User**, and **Smartcard Logon**.</span></span>

7.  <span data-ttu-id="2a484-116">[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2a484-116">Click **OK**.</span></span>

8.  <span data-ttu-id="2a484-117">[**証明書テンプレート**] を右クリックします。</span><span class="sxs-lookup"><span data-stu-id="2a484-117">Right click on **Certificate Templates**.</span></span>

9.  <span data-ttu-id="2a484-118">[**管理**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a484-118">Select **Manage**.</span></span>

10. <span data-ttu-id="2a484-119">スマート カード ユーザー テンプレートのプロパティを開きます。</span><span class="sxs-lookup"><span data-stu-id="2a484-119">Open the properties of the Smartcard User template.</span></span>

11. <span data-ttu-id="2a484-120">[**セキュリティ**] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2a484-120">Click on the **Security** tab.</span></span>

12. <span data-ttu-id="2a484-121">アクセス許可を次のように変更します。</span><span class="sxs-lookup"><span data-stu-id="2a484-121">Change the permissions as follows:</span></span>
    
      - <span data-ttu-id="2a484-122">読み取り/登録 (許可) アクセス許可を指定して個別のユーザー AD アカウントを追加します。または</span><span class="sxs-lookup"><span data-stu-id="2a484-122">Add individual user AD accounts with Read/Enroll (Allow) permissions, or</span></span>
    
      - <span data-ttu-id="2a484-123">読み取り/登録 (許可) のアクセス許可を指定してスマート カード ユーザーを含むセキュリティ グループを追加します。または</span><span class="sxs-lookup"><span data-stu-id="2a484-123">Add a security group containing smart card users with Read/Enroll (Allow) permissions, or</span></span>
    
      - <span data-ttu-id="2a484-124">読み取り/登録 (許可) のアクセス許可を指定してドメイン ユーザー グループを追加します。</span><span class="sxs-lookup"><span data-stu-id="2a484-124">Add the Domain Users group with Read/Enroll (Allow) permissions</span></span>

<span data-ttu-id="2a484-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2a484-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

