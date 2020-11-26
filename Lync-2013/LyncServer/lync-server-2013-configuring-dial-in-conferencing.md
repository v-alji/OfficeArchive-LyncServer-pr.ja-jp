---
title: 'Lync Server 2013: ダイヤルイン会議の構成'
description: 'Lync Server 2013: ダイヤルイン会議を構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring dial-in conferencing
ms:assetid: 79a98c5d-a0a8-4729-828d-b9166842432c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398600(v=OCS.15)
ms:contentKeyID: 48184587
ms.date: 10/03/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d9c3353caa1344b717b0f64c271149f078f194e5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433207"
---
# <a name="configuring-dial-in-conferencing-in-lync-server-2013"></a><span data-ttu-id="82353-103">Lync Server 2013 でのダイヤルイン会議の構成</span><span class="sxs-lookup"><span data-stu-id="82353-103">Configuring dial-in conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="82353-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="82353-104">

<span> </span></span></span>

<span data-ttu-id="82353-105">_**最終更新日:** 2014-10-03_</span><span class="sxs-lookup"><span data-stu-id="82353-105">_**Topic Last Modified:** 2014-10-03_</span></span>

<span data-ttu-id="82353-106">このセクションでは、Lync Server 2013 ダイヤルイン会議の構成について説明します。</span><span class="sxs-lookup"><span data-stu-id="82353-106">This section guides you through the configuration of Lync Server 2013 dial-in conferencing.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="82353-107">このセクション中</span><span class="sxs-lookup"><span data-stu-id="82353-107">In This Section</span></span>

  - [<span data-ttu-id="82353-108">Lync Server 2013 のダイヤルイン会議の前提条件とアクセス許可</span><span class="sxs-lookup"><span data-stu-id="82353-108">Dial-in conferencing configuration prerequisites and permissions in Lync Server 2013</span></span>](lync-server-2013-dial-in-conferencing-configuration-prerequisites-and-permissions.md)

  - [<span data-ttu-id="82353-109">Lync Server 2013 のダイヤルイン会議の展開チェックリスト</span><span class="sxs-lookup"><span data-stu-id="82353-109">Deployment checklist for dial-in conferencing in Lync Server 2013</span></span>](lync-server-2013-deployment-checklist-for-dial-in-conferencing.md)

  - [<span data-ttu-id="82353-110">Lync Server 2013 でのダイヤルイン会議のダイヤル プランの構成</span><span class="sxs-lookup"><span data-stu-id="82353-110">Configure dial plans for dial-in conferencing in Lync Server 2013</span></span>](lync-server-2013-configure-dial-plans-for-dial-in-conferencing.md)

  - [<span data-ttu-id="82353-111">「ダイヤルプラン Lync Server 2013 に地域が割り当てられていることを確認する」</span><span class="sxs-lookup"><span data-stu-id="82353-111">Make sure dial plans Lync Server 2013 have assigned regions</span></span>](lync-server-2013-make-sure-dial-plans-have-assigned-regions.md)

  - [<span data-ttu-id="82353-112">(オプション) Lync Server 2013 での PIN ポリシー設定の確認</span><span class="sxs-lookup"><span data-stu-id="82353-112">(Optional) Verify PIN policy settings in Lync Server 2013</span></span>](lync-server-2013-optional-verify-pin-policy-settings.md)

  - [<span data-ttu-id="82353-113">Lync Server 2013 でダイヤルインの会議ポリシーを構成する</span><span class="sxs-lookup"><span data-stu-id="82353-113">Configure conferencing policy for dial-in in Lync Server 2013</span></span>](lync-server-2013-configure-conferencing-policy-for-dial-in.md)

  - [<span data-ttu-id="82353-114">Lync Server 2013 でのダイヤルイン会議アクセス番号の構成</span><span class="sxs-lookup"><span data-stu-id="82353-114">Configure dial-in conferencing access numbers in Lync Server 2013</span></span>](lync-server-2013-configure-dial-in-conferencing-access-numbers.md)

  - [<span data-ttu-id="82353-115">(オプション) Lync Server 2013 でのダイヤルイン会議の設定の検証</span><span class="sxs-lookup"><span data-stu-id="82353-115">(Optional) Verify dial-in conferencing settings in Lync Server 2013</span></span>](lync-server-2013-optional-verify-dial-in-conferencing-settings.md)

  - [<span data-ttu-id="82353-116">(オプション) Lync Server 2013 で DTMF コマンドの主要なマッピングを変更する</span><span class="sxs-lookup"><span data-stu-id="82353-116">(Optional) Modify key mapping for DTMF commands in Lync Server 2013</span></span>](lync-server-2013-optional-modify-key-mapping-for-dtmf-commands.md)

  - [<span data-ttu-id="82353-117">(オプション) Lync Server 2013 での会議への入退出のアナウンスの有効化および無効化</span><span class="sxs-lookup"><span data-stu-id="82353-117">(Optional) Enable and disable conference join and leave announcements in Lync Server 2013</span></span>](lync-server-2013-optional-enable-and-disable-conference-join-and-leave-announcements.md)

  - [<span data-ttu-id="82353-118">(オプション) Lync Server 2013 でのダイヤルイン会議の検証</span><span class="sxs-lookup"><span data-stu-id="82353-118">(Optional) Verify dial-in conferencing in Lync Server 2013</span></span>](lync-server-2013-optional-verify-dial-in-conferencing.md)

  - [<span data-ttu-id="82353-119">Lync 2013 用オンライン会議アドインの展開</span><span class="sxs-lookup"><span data-stu-id="82353-119">Deploy the Online Meeting Add-in for Lync 2013</span></span>](lync-server-2013-deploy-the-online-meeting-add-in-for-lync-2013.md)

  - [<span data-ttu-id="82353-120">Lync Server 2013 でのユーザー アカウント設定の構成</span><span class="sxs-lookup"><span data-stu-id="82353-120">Configure user account settings in Lync Server 2013</span></span>](lync-server-2013-configure-user-account-settings.md)

  - [<span data-ttu-id="82353-121">(Recommended) Create Conference Directories</span><span class="sxs-lookup"><span data-stu-id="82353-121">(Recommended) Create Conference Directories</span></span>](recommended-create-conference-directories.md)

  - [<span data-ttu-id="82353-122">(オプション) Lync Server 2013 でのダイヤルイン会議へのユーザーの受け入れ</span><span class="sxs-lookup"><span data-stu-id="82353-122">(Optional) Welcome users to dial-in conferencing in Lync Server 2013</span></span>](lync-server-2013-optional-welcome-users-to-dial-in-conferencing.md)

</div>

<div>

## <a name="related-sections"></a><span data-ttu-id="82353-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="82353-123">Related Sections</span></span>

[<span data-ttu-id="82353-124">Lync Server 2013 の展開</span><span class="sxs-lookup"><span data-stu-id="82353-124">Deploying Lync Server 2013</span></span>](lync-server-2013-deploying-lync-server.md)

<span data-ttu-id="82353-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="82353-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

