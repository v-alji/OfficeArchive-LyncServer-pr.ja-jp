---
title: 'Lync Server 2013: Lync Online の顧客とのフェデレーションの前提条件'
description: 'Lync Server 2013: Lync Online の顧客とのフェデレーションの前提条件'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Prerequisites for federating with a Lync Online customer
ms:assetid: f57d8f8a-2b1e-4186-a74f-1d7c6872bfdc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202196(v=OCS.15)
ms:contentKeyID: 48185838
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f99eabd4466385402d5e5983665e9349f1244348
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436924"
---
# <a name="prerequisites-for-federating-with-a-lync-online-customer-in-lync-server-2013"></a><span data-ttu-id="d833a-103">Lync Online のユーザーと Lync Server 2013 でフェデレーションを行うための前提条件</span><span class="sxs-lookup"><span data-stu-id="d833a-103">Prerequisites for federating with a Lync Online customer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d833a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d833a-104">

<span> </span></span></span>

<span data-ttu-id="d833a-105">_**最終更新日:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="d833a-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="d833a-106">Lync Online 2010 ユーザーとのフェデレーションを行うには、組織での Lync Server 2013 の最初の展開と構成を既に完了している必要があります。</span><span class="sxs-lookup"><span data-stu-id="d833a-106">To federate with a Lync Online 2010 customer, you should have already completed initial deployment and configuration of Lync Server 2013 in your organization.</span></span> <span data-ttu-id="d833a-107">これには、次のポリシーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d833a-107">This includes the following:</span></span>

  - <span data-ttu-id="d833a-108">少なくとも1つの Standard Edition サーバーまたは1つの Enterprise Edition フロントエンドプールを組織に展開します。</span><span class="sxs-lookup"><span data-stu-id="d833a-108">Deploying at least one Standard Edition server or one Enterprise Edition Front End pool in your organization.</span></span> <span data-ttu-id="d833a-109">内部サーバーの展開の詳細については、「展開ドキュメントに [Lync Server 2013 を展開](lync-server-2013-deploying-lync-server.md) する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d833a-109">For details about deploying internal servers, see [Deploying Lync Server 2013](lync-server-2013-deploying-lync-server.md) in the Deployment documentation.</span></span>

  - <span data-ttu-id="d833a-110">Lync Server 2013 の内部ユーザーアカウントを有効にします。</span><span class="sxs-lookup"><span data-stu-id="d833a-110">Enabling internal user accounts for Lync Server 2013.</span></span> <span data-ttu-id="d833a-111">詳細については、展開ドキュメントまたは運用マニュアルの「 [Lync Server 2013 のユーザーアカウントを無効にするか、もう一度有効にする](lync-server-2013-disable-or-re-enable-user-account-for-lync-server.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d833a-111">For details, see [Disable or re-enable user account for Lync Server 2013](lync-server-2013-disable-or-re-enable-user-account-for-lync-server.md) in the Deployment documentation or the Operations documentation.</span></span>

  - <span data-ttu-id="d833a-112">少なくとも1つのエッジサーバーと、外部ユーザーのアクセスをサポートするために必要なその他のコンポーネントを展開します。</span><span class="sxs-lookup"><span data-stu-id="d833a-112">Deploying at least one Edge Server and the other components required to support external user access.</span></span> <span data-ttu-id="d833a-113">詳細については、展開ドキュメントで「 [Lync Server 2013 へのフェデレーションと外部アクセスを管理する](lync-server-2013-managing-federation-and-external-access-to-lync-server-2013.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d833a-113">For details, see [Managing federation and external access to Lync Server 2013](lync-server-2013-managing-federation-and-external-access-to-lync-server-2013.md) in the Deployment documentation.</span></span>

  - <span data-ttu-id="d833a-114">組織内でフェデレーションサポートを有効にし、フェデレーションドメインによるアクセスを制御するための適切なメソッドを構成します。</span><span class="sxs-lookup"><span data-stu-id="d833a-114">Enabling federation support within your organization and configuring the appropriate method for controlling access by federated domains.</span></span> <span data-ttu-id="d833a-115">詳細については、「 [Lync server 2013 でリモートユーザーアクセスを有効または無効](lync-server-2013-enable-or-disable-remote-user-access.md) にする」および「運用ドキュメントの [lync server 2013 で組織の SIP フェデレーションプロバイダーを管理](lync-server-2013-manage-sip-federated-providers-for-your-organization.md) する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d833a-115">For details, see [Enable or disable remote user access in Lync Server 2013](lync-server-2013-enable-or-disable-remote-user-access.md) and [Manage SIP federated providers for your organization in Lync Server 2013](lync-server-2013-manage-sip-federated-providers-for-your-organization.md) in the Operations documentation.</span></span>

  - <span data-ttu-id="d833a-116">組織内のユーザーに対して外部ユーザーアクセスを有効にします。</span><span class="sxs-lookup"><span data-stu-id="d833a-116">Enabling external user access for users in your organization.</span></span> <span data-ttu-id="d833a-117">詳細については、「Lync Server 2013 で Lync を有効にしているユーザーと展開ドキュメントまたは操作ドキュメントに [外部ユーザーアクセスポリシーを割り当てる](lync-server-2013-assign-an-external-user-access-policy-to-a-lync-enabled-user.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d833a-117">For details, see [Assign an external user access policy to a Lync enabled user in Lync Server 2013](lync-server-2013-assign-an-external-user-access-policy-to-a-lync-enabled-user.md) and in the Deployment documentation or Operations documentation.</span></span>

<span data-ttu-id="d833a-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d833a-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

