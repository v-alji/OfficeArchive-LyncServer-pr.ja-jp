---
title: 'Lync Server 2013: Lync と Skype の接続のプロビジョニング ガイド'
description: 'Lync Server 2013: Lync-Skype 接続のプロビジョニングガイド。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Provisioning guide for Lync-Skype connectivity
ms:assetid: 69adda9b-5b72-4538-9be6-079b2f462e09
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn440173(v=OCS.15)
ms:contentKeyID: 57793363
ms.date: 11/26/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9859a7a621ba4329fe0436fe50a0d9de1d0ae1ef
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436742"
---
# <a name="provisioning-guide-for-lync-skype-connectivity-in-lync-server-2013"></a><span data-ttu-id="360aa-103">Lync Server 2013 での Lync と Skype の接続のプロビジョニング ガイド</span><span class="sxs-lookup"><span data-stu-id="360aa-103">Provisioning guide for Lync-Skype connectivity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="360aa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="360aa-104">

<span> </span></span></span>

<span data-ttu-id="360aa-105">_**最終更新日:** 2014-11-26_</span><span class="sxs-lookup"><span data-stu-id="360aa-105">_**Topic Last Modified:** 2014-11-26_</span></span>

<span data-ttu-id="360aa-106">Lync Server 2013 は、Skype との接続をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="360aa-106">Lync Server 2013 supports connectivity with Skype.</span></span> <span data-ttu-id="360aa-107">この接続を使用すると、Lync 2013 ユーザーは、Skype ユーザーの Microsoft Account (MSA) を使用して Skype の連絡先を追加できます。</span><span class="sxs-lookup"><span data-stu-id="360aa-107">This connectivity enables your Lync 2013 users to add Skype contacts by using the Skype user’s Microsoft Account (MSA).</span></span> <span data-ttu-id="360aa-108">Skype クライアントも、Lync ユーザーを連絡先リストに追加できます。</span><span class="sxs-lookup"><span data-stu-id="360aa-108">Skype clients can also add Lync users to their contact list.</span></span> <span data-ttu-id="360aa-109">Lync Server で管理上設定されたポリシーに基づいて、Lync ユーザーと Skype ユーザーは、インスタント メッセージを使用して通信し、お互いのプレゼンスを確認し、音声およびビデオ通話を開始できるようになります。</span><span class="sxs-lookup"><span data-stu-id="360aa-109">Based on policies administratively set in Lync Server, Lync and Skype users will be able to communicate using instant messaging, see each other’s presence, and initiate audio and video calls.</span></span> <span data-ttu-id="360aa-110">Lync-Skype 接続は、Lync Online の機能でもあり、Microsoft 365 管理センター内の Lync 管理センターから Lync Online ユーザーに対して有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="360aa-110">Lync-Skype connectivity is also a feature of Lync Online, and can be enabled for Lync Online customers from the Lync Administration Center within the Microsoft 365 admin center.</span></span>

<div>

> [!IMPORTANT]  
> <span data-ttu-id="360aa-p102">Lync Server がパブリック インスタント メッセージング接続 (PIC) を使用して Windows Messenger と接続するように既に構成されている場合、展開は、既に Lync と Skype の接続用に構成されています。検討する対象となりうる唯一の変更は、既存の Messenger PIC エントリの名前を Skype などに変更することだけです。詳細については、このガイドで後述する Lync の「Lync 用の Skype PIC プロバイダー設定を構成する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="360aa-p102">If Lync Server is already configured to connect with Windows Messenger by using Public Instant Messaging Connectivity (PIC), your deployment is already configured for Lync-Skype connectivity. The only change you may want to consider is to rename your existing Messenger PIC entry as Skype. For details, see Configure the Skype PIC provider setting for Lync later in this guide.</span></span>

</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="360aa-114">このセクション中</span><span class="sxs-lookup"><span data-stu-id="360aa-114">In This Section</span></span>

  - [<span data-ttu-id="360aa-115">Lync Online ユーザー向けの Lync Server 2013 での Lync-Skype 接続についての注意</span><span class="sxs-lookup"><span data-stu-id="360aa-115">Note about Lync-Skype connectivity in Lync Server 2013 for Lync Online customers</span></span>](lync-server-2013-note-about-lync-skype-connectivity-for-lync-on.md)

  - [<span data-ttu-id="360aa-116">Lync Server 2013 から Lync Server パブリック IM 接続プロビジョニング サイトへのアクセス</span><span class="sxs-lookup"><span data-stu-id="360aa-116">Accessing the Lync Server public IM connectivity provisioning site from Lync Server 2013</span></span>](lync-server-2013-accessing-the-lync-server-public-im-connectivity-provisioning-site.md)

  - [<span data-ttu-id="360aa-117">Lync Server 2013 での Lync と Skype の接続の有効化</span><span class="sxs-lookup"><span data-stu-id="360aa-117">Enabling Lync-Skype connectivity in Lync Server 2013</span></span>](lync-server-2013-enabling-lync-skype-connectivity.md)

  - [<span data-ttu-id="360aa-118">エンド ユーザーとしての Lync Server 2013 での Lync と Skype の接続の使用</span><span class="sxs-lookup"><span data-stu-id="360aa-118">Using Lync-Skype connectivity in Lync Server 2013 as an end user</span></span>](lync-server-2013-using-lync-skype-connectivity-as-an-end-user.md)

  - [<span data-ttu-id="360aa-119">FAQ: Skype 接続用の Lync Server 2013 のプロビジョニング</span><span class="sxs-lookup"><span data-stu-id="360aa-119">Frequently Asked Questions: Provisioning Lync Server 2013 for Skype connectivity</span></span>](lync-server-2013-frequently-asked-questions-provisioning-lync-server-for-skype-connectivity.md)

<span data-ttu-id="360aa-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="360aa-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

