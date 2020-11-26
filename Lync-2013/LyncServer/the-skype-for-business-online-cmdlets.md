---
title: Lync Online のコマンドレット
description: Skype for Business Online のコマンドレット。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: The Skype for Business Online cmdlets
ms:assetid: 71f38305-fd8b-4013-83e1-cb742e3174c3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362817(v=OCS.15)
ms:contentKeyID: 56558831
ms.date: 05/04/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4a3551e11ba943e46b48002f86f03a52174b3eed
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438409"
---
# <a name="the-skype-for-business-online-cmdlets"></a><span data-ttu-id="73e14-103">Lync Online のコマンドレット</span><span class="sxs-lookup"><span data-stu-id="73e14-103">The Skype for Business Online cmdlets</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="73e14-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="73e14-104">

<span> </span></span></span>

<span data-ttu-id="73e14-105">_**最終更新日:** 2013-07-05_</span><span class="sxs-lookup"><span data-stu-id="73e14-105">_**Topic Last Modified:** 2013-07-05_</span></span>

<span data-ttu-id="73e14-106">Windows PowerShell を使用して Skype for Business Online に接続すると、Skype for Business Online のコマンドレットのコレクションが、メモリ内でコンピューターにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="73e14-106">When you connect to Skype for Business Online by using Windows PowerShell, a collection of Skype for Business Online cmdlets is copied, in memory, to your computer.</span></span> <span data-ttu-id="73e14-107">これらのコマンドレットは、ローカルコンピューターで既に使用している他のコマンドレット (Windows PowerShell をインストールした場合にインストールされるコアコマンドレットを含む) に加えて、Skype for Business Online の展開と Skype for Business Online のユーザーアカウントを管理するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="73e14-107">These cmdlets, in addition to any other cmdlets you already have on your local computer (including the core cmdlets that are installed when you install Windows PowerShell), are then available for managing your Skype for Business Online deployment and your Skype for Business Online user accounts.</span></span> <span data-ttu-id="73e14-108">Skype for Business Online のコマンドレットは、次のトピックで導入されています。</span><span class="sxs-lookup"><span data-stu-id="73e14-108">The Skype for Business Online cmdlets are introduced in the following topics:</span></span>

  - [<span data-ttu-id="73e14-109">Lync Online テナントの管理</span><span class="sxs-lookup"><span data-stu-id="73e14-109">Managing Skype for Business Online tenants</span></span>](https://docs.microsoft.com/skypeforbusiness/set-up-your-computer-for-windows-powershell/manage-skype-for-business-online-organizations)

  - [<span data-ttu-id="73e14-110">Skype for Business Online のユーザーとユーザーアカウントのプロパティを管理する</span><span class="sxs-lookup"><span data-stu-id="73e14-110">Managing users and user account properties in Skype for Business Online</span></span>](https://docs.microsoft.com/skypeforbusiness/manage/user-accounts/user-accounts)

  - [<span data-ttu-id="73e14-111">Skype for Business Online のポリシーを管理する</span><span class="sxs-lookup"><span data-stu-id="73e14-111">Managing policies in Skype for Business Online</span></span>](https://docs.microsoft.com/office365/enterprise/powershell/manage-skype-for-business-online-policies-with-office-365-powershell)

  - [<span data-ttu-id="73e14-112">Skype for business クライアントを Skype for Business Online から管理する</span><span class="sxs-lookup"><span data-stu-id="73e14-112">Managing the Skype for Business client from Skype for Business Online</span></span>](https://docs.microsoft.com/skypeforbusiness/set-up-skype-for-business-online/deploy-the-skype-for-business-client-in-office-365)

  - [<span data-ttu-id="73e14-113">Skype for Business Online での Exchange ユニファイドメッセージングとホスト型ボイスメールの管理</span><span class="sxs-lookup"><span data-stu-id="73e14-113">Managing Exchange Unified Messaging and hosted voice mail in Skype for Business Online</span></span>](https://docs.microsoft.com/skypeforbusiness/set-up-your-computer-for-windows-powershell/manage-exchange-unified-messaging-and-hosted-voicemail)

  - [<span data-ttu-id="73e14-114">Skype for Business Online で外部ユーザーと組織との通信を管理する</span><span class="sxs-lookup"><span data-stu-id="73e14-114">Managing communications in Skype for Business Online with outside users and organizations</span></span>](https://docs.microsoft.com/skypeforbusiness/set-up-skype-for-business-online/allow-users-to-contact-external-skype-for-business-users)

  - [<span data-ttu-id="73e14-115">Lync Online のミーティングと会議の管理</span><span class="sxs-lookup"><span data-stu-id="73e14-115">Managing Skype for Business Online meetings and conferences</span></span>](https://docs.microsoft.com/skypeforbusiness/manage/conferencing/conferencing-policies)

  - [<span data-ttu-id="73e14-116">Skype for Business Online の携帯電話とモバイルデバイスの管理</span><span class="sxs-lookup"><span data-stu-id="73e14-116">Managing cell phones and mobile devices in Skype for Business Online</span></span>](https://docs.microsoft.com/skypeforbusiness/set-up-policies-in-your-organization/set-up-mobile-policies-for-your-organization)

<div>

## <a name="see-also"></a><span data-ttu-id="73e14-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="73e14-117">See Also</span></span>


[<span data-ttu-id="73e14-118">クイック リファレンス: Windows PowerShell を使用した一般的な Lync Online の管理タスクの実行</span><span class="sxs-lookup"><span data-stu-id="73e14-118">Quick reference: Using Windows PowerShell to do common Skype for Business Online management tasks</span></span>](https://docs.microsoft.com/office365/enterprise/powershell/manage-skype-for-business-online-with-office-365-powershell)  
  

<span data-ttu-id="73e14-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="73e14-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

