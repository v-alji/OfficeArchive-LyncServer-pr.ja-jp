---
title: Lync Server 2013 ストレスおよびパフォーマンス ツール
description: Lync Server 2013 ストレスおよびパフォーマンスツール。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync Server 2013 Stress and Performance Tool
ms:assetid: dc03db19-d104-402e-9951-240681b3fb69
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945609(v=OCS.15)
ms:contentKeyID: 51541435
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 073aa49b8c9002ff23cfea61904735cdc0144cfa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446445"
---
# <a name="lync-server-2013-stress-and-performance-tool"></a><span data-ttu-id="4fb88-103">Lync Server 2013 ストレスおよびパフォーマンス ツール</span><span class="sxs-lookup"><span data-stu-id="4fb88-103">Lync Server 2013 Stress and Performance Tool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4fb88-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4fb88-104">

<span> </span></span></span>

<span data-ttu-id="4fb88-105">_**最終更新日:** 2013-01-25_</span><span class="sxs-lookup"><span data-stu-id="4fb88-105">_**Topic Last Modified:** 2013-01-25_</span></span>

<span data-ttu-id="4fb88-106">Lync Server 2013 のストレスとパフォーマンスツールには、Lync Server 2013 のキャパシティ計画を簡素化するためのツールが含まれています。</span><span class="sxs-lookup"><span data-stu-id="4fb88-106">The Lync Server 2013 Stress and Performance Tool includes tools that simplify capacity planning for Lync Server 2013.</span></span> <span data-ttu-id="4fb88-107">Lync Server 2013 のストレスとパフォーマンスツールは、次のことを行うのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="4fb88-107">The Lync Server 2013 Stress and Performance Tool will help you to:</span></span>

  - <span data-ttu-id="4fb88-108">Lync Server 2013 のハードウェア計画を簡素化します。</span><span class="sxs-lookup"><span data-stu-id="4fb88-108">Simplify your hardware planning for Lync Server 2013 .</span></span>

  - <span data-ttu-id="4fb88-109">パフォーマンスの調整に関する知識とベストプラクティスを強化します。</span><span class="sxs-lookup"><span data-stu-id="4fb88-109">Provide you with increased knowledge and best practices for performance tuning.</span></span>

  - <span data-ttu-id="4fb88-110">目的の Lync Server 2013 展開のパフォーマンスを測定します。</span><span class="sxs-lookup"><span data-stu-id="4fb88-110">Measure the performance of your intended Lync Server 2013 deployments.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="4fb88-111">このセクション中</span><span class="sxs-lookup"><span data-stu-id="4fb88-111">In This Section</span></span>

1.  [<span data-ttu-id="4fb88-112">概要</span><span class="sxs-lookup"><span data-stu-id="4fb88-112">Introduction</span></span>](introduction.md)

2.  [<span data-ttu-id="4fb88-113">前提条件</span><span class="sxs-lookup"><span data-stu-id="4fb88-113">Prerequisites</span></span>](prerequisites.md)

3.  [<span data-ttu-id="4fb88-114">セットアップ</span><span class="sxs-lookup"><span data-stu-id="4fb88-114">Setup</span></span>](setup.md)

4.  [<span data-ttu-id="4fb88-115">Lync Server 2013 のシナリオを構成する</span><span class="sxs-lookup"><span data-stu-id="4fb88-115">Configure Lync Server 2013 Scenarios</span></span>](configure-lync-server-2013-scenarios.md)

5.  [<span data-ttu-id="4fb88-116">ユーザーと連絡先の作成</span><span class="sxs-lookup"><span data-stu-id="4fb88-116">Create Users and Contacts</span></span>](create-users-and-contacts.md)

6.  [<span data-ttu-id="4fb88-117">ユーザー プロファイルの構成</span><span class="sxs-lookup"><span data-stu-id="4fb88-117">Configure User Profile</span></span>](configure-user-profile.md)

7.  [<span data-ttu-id="4fb88-118">LyncPerfTool の実行</span><span class="sxs-lookup"><span data-stu-id="4fb88-118">Run LyncPerfTool</span></span>](run-lyncperftool.md)

8.  [<span data-ttu-id="4fb88-119">結果の解釈</span><span class="sxs-lookup"><span data-stu-id="4fb88-119">Interpreting the Results</span></span>](interpreting-the-results.md)

9.  [<span data-ttu-id="4fb88-120">Lync Server 2013 のストレスとパフォーマンスに関するツールについてよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="4fb88-120">Lync Server 2013 Stress and Performance Tool FAQ</span></span>](lync-server-2013-stress-and-performance-tool-faq.md)

<span data-ttu-id="4fb88-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4fb88-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

