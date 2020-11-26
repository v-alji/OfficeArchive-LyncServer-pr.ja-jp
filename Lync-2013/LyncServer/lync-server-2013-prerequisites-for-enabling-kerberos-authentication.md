---
title: 'Lync Server 2013: Kerberos 認証を有効にするための前提条件'
description: 'Lync Server 2013: Kerberos 認証を有効にするための前提条件。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Prerequisites for enabling Kerberos authentication
ms:assetid: 3f276a21-7476-4bc0-9fd1-59e844d2e9c1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425909(v=OCS.15)
ms:contentKeyID: 48183945
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 65a45bad0eb249fdbc717fe05f080ce737c87c6f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436973"
---
# <a name="prerequisites-for-enabling-kerberos-authentication-in-lync-server-2013"></a><span data-ttu-id="4b906-103">Lync Server 2013 で Kerberos 認証を有効にするための前提条件</span><span class="sxs-lookup"><span data-stu-id="4b906-103">Prerequisites for enabling Kerberos authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4b906-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4b906-104">

<span> </span></span></span>

<span data-ttu-id="4b906-105">_**最終更新日:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="4b906-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="4b906-106">Kerberos 認証を有効にする前に、必要な構成とインフラストラクチャの準備がすべて完了していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="4b906-106">Before enabling Kerberos authentication, make sure that you complete all prerequisite configuration and infrastructure preparations:</span></span>

  - <span data-ttu-id="4b906-107">Lync Server 2013 の Active Directory スキーマが拡張されています。</span><span class="sxs-lookup"><span data-stu-id="4b906-107">Active Directory schema is extended for Lync Server 2013.</span></span>

  - <span data-ttu-id="4b906-108">Lync Server 2013 の Active Directory フォレストの準備が完了しました。</span><span class="sxs-lookup"><span data-stu-id="4b906-108">Active Directory forest preparation is completed for Lync Server 2013.</span></span>

  - <span data-ttu-id="4b906-109">Lync Server 2013 の Active Directory ドメインの準備が完了しました。</span><span class="sxs-lookup"><span data-stu-id="4b906-109">Active Directory domain preparation is completed for Lync Server 2013.</span></span>

  - <span data-ttu-id="4b906-110">中央管理ストアが正常にインストールされ、使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="4b906-110">Central Management store is successfully installed and available.</span></span>

  - <span data-ttu-id="4b906-111">トポロジは、トポロジビルダーを使用して作成および公開されています。</span><span class="sxs-lookup"><span data-stu-id="4b906-111">The topology has been created and published by using Topology Builder.</span></span>

  - <span data-ttu-id="4b906-112">Web サービスを必要とするサーバーと役割は、フロントエンドサーバー、標準エディションサーバー、およびディレクターなど、定義および展開されています。</span><span class="sxs-lookup"><span data-stu-id="4b906-112">Servers and roles that require Web Services have been defined and deployed, including Front End Servers, Standard Edition servers, and Directors.</span></span>

  - <span data-ttu-id="4b906-113">Lync Server 2013 で Web サービスをサポートするために推奨される役割サービスを使用して、インターネットインフォメーションサービス (IIS) を構成し、展開します。</span><span class="sxs-lookup"><span data-stu-id="4b906-113">Internet Information Services (IIS) is configured and deployed with the recommended role services to support Web Services in Lync Server 2013.</span></span>

<span data-ttu-id="4b906-114">前提条件が満たされた後で、展開のために Kerberos 認証に使用する1つ以上のアカウントを Web サービス用に作成する準備ができている必要があります。</span><span class="sxs-lookup"><span data-stu-id="4b906-114">After the prerequisites have been met, you should be ready to create one or more accounts for Web Services to use for Kerberos authentication for your deployment.</span></span> <span data-ttu-id="4b906-115">少なくとも、展開ごとに1つの Kerberos 認証アカウントを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4b906-115">At a minimum, you need to create one Kerberos authentication account for each deployment.</span></span> <span data-ttu-id="4b906-116">ただし、サイトにローカルの Kerberos 認証を提供するために、各サイトのアカウントを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="4b906-116">However, you can create an account for each site to provide local Kerberos authentication at the site.</span></span> <span data-ttu-id="4b906-117">1つのサイトにつき1つの Kerberos 認証アカウントのみを指定できます。</span><span class="sxs-lookup"><span data-stu-id="4b906-117">You can only specify one Kerberos authentication account per site.</span></span>

<span data-ttu-id="4b906-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4b906-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

