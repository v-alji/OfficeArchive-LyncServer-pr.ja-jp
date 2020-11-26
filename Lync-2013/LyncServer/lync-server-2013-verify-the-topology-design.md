---
title: 'Lync Server 2013: トポロジ設計の確認'
description: 'Lync Server 2013: トポロジの設計を確認します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify the topology design
ms:assetid: c1b61814-239e-4101-aab0-de3db1d8793c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412951(v=OCS.15)
ms:contentKeyID: 48185311
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cb1e65343aacddbc11d3b909dfdff715503cab93
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438912"
---
# <a name="verify-the-topology-design-in-lync-server-2013"></a><span data-ttu-id="8d70b-103">Lync Server 2013 でのトポロジ設計の確認</span><span class="sxs-lookup"><span data-stu-id="8d70b-103">Verify the topology design in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8d70b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8d70b-104">

<span> </span></span></span>

<span data-ttu-id="8d70b-105">_**最終更新日:** 2012-01-02_</span><span class="sxs-lookup"><span data-stu-id="8d70b-105">_**Topic Last Modified:** 2012-01-02_</span></span>

<span data-ttu-id="8d70b-106">トポロジビルダーは、トポロジを自動的に確認します。</span><span class="sxs-lookup"><span data-stu-id="8d70b-106">Topology Builder automatically verifies the topology.</span></span> <span data-ttu-id="8d70b-107">トポロジエラーは検証エラーとして識別され、サーバーの役割の横に表示される検証エラーアイコンによって示されます。</span><span class="sxs-lookup"><span data-stu-id="8d70b-107">Any topology error is identified as a validation error, indicated by the validation error icon next to the server role.</span></span> <span data-ttu-id="8d70b-108">トポロジが配置のトポロジを正しく表すことも確認することが重要です。</span><span class="sxs-lookup"><span data-stu-id="8d70b-108">It is important to also verify that the topology correctly represents the topology for your deployment.</span></span>

<div>

## <a name="to-verify-the-topology-prior-to-publication"></a><span data-ttu-id="8d70b-109">公開前にトポロジを確認するには</span><span class="sxs-lookup"><span data-stu-id="8d70b-109">To verify the topology prior to publication</span></span>

1.  <span data-ttu-id="8d70b-110">すべての簡易 URL が正しく構成されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8d70b-110">Check that all simple URLs are configured correctly.</span></span>

2.  <span data-ttu-id="8d70b-111">SQL Server ベースのサーバーがオンラインになっていることを確認します。また、トポロジ ビルダーがインストールされているコンピューターでこのサーバーが使用できることを確認します。必要なファイアウォール規則などを確認してください。</span><span class="sxs-lookup"><span data-stu-id="8d70b-111">Confirm that the SQL Server-based server is online and available to the computer where Topology Builder is installed, including any necessary firewall rules.</span></span>

3.  <span data-ttu-id="8d70b-112">ファイル共有が使用可能であり、適切なアクセス許可が定義されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8d70b-112">Confirm that the file share is available and has the proper permissions defined.</span></span>

4.  <span data-ttu-id="8d70b-113">トポロジで、展開要件を満たす正しいサーバーの役割が定義されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8d70b-113">Confirm that the correct server roles that meet the deployment requirements are defined in the topology.</span></span>

5.  <span data-ttu-id="8d70b-114">サーバーが Active Directory ドメインサービスに存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="8d70b-114">Verify that the servers exist in Active Directory Domain Services.</span></span> <span data-ttu-id="8d70b-115">この問題は、サーバーをドメインに参加している場合に自動的に発生します。</span><span class="sxs-lookup"><span data-stu-id="8d70b-115">This will happen automatically if you have joined the servers to the domain.</span></span>

<span data-ttu-id="8d70b-116">トポロジの検証が完了して検証エラーがないことが確認できたら、トポロジの公開の準備に移ります。</span><span class="sxs-lookup"><span data-stu-id="8d70b-116">When you have verified the topology and there are no validation errors, you should be ready to publish the topology.</span></span> <span data-ttu-id="8d70b-117">検証エラーがある場合は、トポロジを公開する前に修正する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d70b-117">If there are validation errors, you must correct these before you can publish the topology.</span></span> <span data-ttu-id="8d70b-118">トポロジの公開について詳しくは、「 [Lync Server 2013 でトポロジを発行する](lync-server-2013-publish-the-topology.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="8d70b-118">For details about publishing your topology, see [Publish the topology in Lync Server 2013](lync-server-2013-publish-the-topology.md).</span></span>

<span data-ttu-id="8d70b-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8d70b-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

