---
title: 'Lync Server 2013: 代理トランザクションの実行'
description: 'Lync Server 2013: 代理トランザクションを実行します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Running synthetic transactions
ms:assetid: 2b56c7bd-8956-4fa1-8232-1876b959b258
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720911(v=OCS.15)
ms:contentKeyID: 63969593
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 26b0c26024f361dac196319eaf849c1847033cc9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442181"
---
# <a name="running-synthetic-transactions-in-lync-server-2013"></a><span data-ttu-id="0f7a6-103">Lync Server 2013 での代理トランザクションの実行</span><span class="sxs-lookup"><span data-stu-id="0f7a6-103">Running synthetic transactions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0f7a6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0f7a6-104">

<span> </span></span></span>

<span data-ttu-id="0f7a6-105">_**最終更新日:** 2014-08-18_</span><span class="sxs-lookup"><span data-stu-id="0f7a6-105">_**Topic Last Modified:** 2014-08-18_</span></span>

<span data-ttu-id="0f7a6-106">通常、代理トランザクションは、次の2つの方法で行われます。</span><span class="sxs-lookup"><span data-stu-id="0f7a6-106">Synthetic transactions are typically conducted in two ways.</span></span> <span data-ttu-id="0f7a6-107">CsHealthMonitoringConfiguration コマンドレットを使用して、各レジストラープールのテストユーザーを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="0f7a6-107">You can use the CsHealthMonitoringConfiguration cmdlets to set up test users for each of their Registrar pools.</span></span> <span data-ttu-id="0f7a6-108">これらのテストユーザーは、代理トランザクションとして使用するように事前に構成されたユーザーのペアです。</span><span class="sxs-lookup"><span data-stu-id="0f7a6-108">These test users are a pair of users who were preconfigured for use with synthetic transactions.</span></span> <span data-ttu-id="0f7a6-109">(通常、テストアカウントであり、実際のユーザーに属するアカウントではありません)。プールに対して構成されたテストユーザーがいる場合、テストに関係しているユーザーアカウントの id を指定したり、資格情報を指定したりすることなく、そのプールに対して代理トランザクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="0f7a6-109">(Typically these are test accounts and not accounts that belong to actual users.) With test users configured for a pool, you can run a synthetic transaction against that pool without having to specify the identities of (and supply the credentials for) the user accounts involved in the test.</span></span>

<span data-ttu-id="0f7a6-110">または、実際のユーザーアカウントを使用して、代理トランザクションを実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="0f7a6-110">Or, you can run a synthetic transaction by using actual user accounts.</span></span> <span data-ttu-id="0f7a6-111">たとえば、2人のユーザーがインスタントメッセージを交換できない場合は、(1 組のテストアカウントではなく) 2 つのユーザーアカウントを使用して代理トランザクションを実行し、問題を診断して解決することができます。</span><span class="sxs-lookup"><span data-stu-id="0f7a6-111">For example, if two users cannot exchange instant messages, you could run a synthetic transaction using those two user accounts (instead of a pair of test accounts), and then try to diagnose and resolve the issue.</span></span> <span data-ttu-id="0f7a6-112">実際のユーザーアカウントを使用して代理トランザクションを実行する場合は、各ユーザーのログオン名とパスワードを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f7a6-112">If you decide to conduct a synthetic transaction using actual user accounts, you must supply the logon names and passwords for each user.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="0f7a6-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="0f7a6-113">See Also</span></span>


[<span data-ttu-id="0f7a6-114">Lync Server 2013 で監視ノードのテストユーザーと構成設定を構成する</span><span class="sxs-lookup"><span data-stu-id="0f7a6-114">Configuring watcher node test users and configuration settings in Lync Server 2013</span></span>](lync-server-2013-configuring-watcher-node-test-users-and-configuration-settings.md)  
[<span data-ttu-id="0f7a6-115">Lync Server 2013 での代理トランザクションの特別なセットアップ手順</span><span class="sxs-lookup"><span data-stu-id="0f7a6-115">Special setup instructions for synthetic transactions in Lync Server 2013</span></span>](lync-server-2013-special-setup-instructions-for-synthetic-transactions.md)  
  

<span data-ttu-id="0f7a6-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0f7a6-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

