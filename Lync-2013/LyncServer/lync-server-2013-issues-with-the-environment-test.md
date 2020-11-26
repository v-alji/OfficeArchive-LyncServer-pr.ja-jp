---
title: 'Lync Server 2013: 環境テストの問題'
description: 'Lync Server 2013: 環境テストの問題。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Issues with the environment test
ms:assetid: ff1fe0d3-35b2-41ef-87e7-6a61e9e1d2ca
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205421(v=OCS.15)
ms:contentKeyID: 48185970
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 551d7e914480e178e0558c1d17eefcf060c0688e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426719"
---
# <a name="issues-with-the-environment-test-in-lync-server-2013"></a><span data-ttu-id="1db5f-103">Lync Server 2013 での環境テストの問題</span><span class="sxs-lookup"><span data-stu-id="1db5f-103">Issues with the environment test in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1db5f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1db5f-104">

<span> </span></span></span>

<span data-ttu-id="1db5f-105">_**最終更新日:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="1db5f-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="1db5f-106">ベストプラクティスアナライザーは、Lync Server 2013 環境がサポートされている構成であることを確認するための手段を提供します。</span><span class="sxs-lookup"><span data-stu-id="1db5f-106">Best Practices Analyzer provides a way for you to verify that your Lync Server 2013 environment is a supported configuration.</span></span> <span data-ttu-id="1db5f-107">Active Directory ドメインサービスのチェックの一部として、ベストプラクティスアナライザーは次の操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="1db5f-107">As part of the Active Directory Domain Services check, Best Practices Analyzer does the following:</span></span>

  - <span data-ttu-id="1db5f-108">Active Directory ドメインサービスのフォレストとスキーマの準備を確認します。</span><span class="sxs-lookup"><span data-stu-id="1db5f-108">Verifies the Active Directory Domain Services forest and schema preparation.</span></span>

  - <span data-ttu-id="1db5f-109">展開内の Active Directory ドメインサービスのサイトとドメインの数を示します。</span><span class="sxs-lookup"><span data-stu-id="1db5f-109">Identifies the number of Active Directory Domain Services sites and domains in the deployment.</span></span>

  - <span data-ttu-id="1db5f-110">フォレストとドメインのレベルを確認します。</span><span class="sxs-lookup"><span data-stu-id="1db5f-110">Checks the forest and domain levels.</span></span>

  - <span data-ttu-id="1db5f-111">ドメインコントローラーのバージョンを確認します。</span><span class="sxs-lookup"><span data-stu-id="1db5f-111">Checks the domain controller version.</span></span>

  - <span data-ttu-id="1db5f-112">ドメイン、構成、およびスキーマの名前付けコンテキストを識別します。</span><span class="sxs-lookup"><span data-stu-id="1db5f-112">Identifies the domain, configuration, and schema naming context.</span></span>

  - <span data-ttu-id="1db5f-113">有効なユーザーの数を示します。</span><span class="sxs-lookup"><span data-stu-id="1db5f-113">Identifies the number of enabled users.</span></span>

  - <span data-ttu-id="1db5f-114">グローバル Active Directory ドメインサービスの設定が保存されている場所を確認します。</span><span class="sxs-lookup"><span data-stu-id="1db5f-114">Checks where the global Active Directory Domain Services settings are stored.</span></span>

  - <span data-ttu-id="1db5f-115">Lync Server のサービス接続ポイント (Scp) を確認します。</span><span class="sxs-lookup"><span data-stu-id="1db5f-115">Checks for the service connection points (SCPs) for Lync Server.</span></span>

  - <span data-ttu-id="1db5f-116">データベースのバージョンを示します。</span><span class="sxs-lookup"><span data-stu-id="1db5f-116">Identifies the database version.</span></span>

<div>

## <a name="resolving-issues-with-the-environment"></a><span data-ttu-id="1db5f-117">環境の問題を解決する</span><span class="sxs-lookup"><span data-stu-id="1db5f-117">Resolving Issues with the Environment</span></span>

<span data-ttu-id="1db5f-118">環境テストで環境の問題が検出された場合、これらの問題は、Active Directory 構成の問題、または特定のサーバーで実行されているソフトウェアのレベルに起因している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1db5f-118">If the environment test found problems with your environment, these problems are probably caused by issues with your Active Directory configuration or the level of software running on specific servers.</span></span> <span data-ttu-id="1db5f-119">たとえば、Windows Server 2000 を実行している環境内のドメインコントローラーを特定する場合は、警告が表示され、サポートされているバージョンの Windows Server にアップグレードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1db5f-119">For example, if Best Practices Analyzer identifies any domain controllers in your environment that are running Windows Server 2000, it will issue a warning and you will need to upgrade those domain controllers to a supported version of Windows Server.</span></span>

<span data-ttu-id="1db5f-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1db5f-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

