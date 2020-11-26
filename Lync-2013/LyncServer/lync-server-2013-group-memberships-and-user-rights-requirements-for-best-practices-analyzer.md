---
title: ベストプラクティスアナライザーのグループメンバーシップとユーザー権限の要件
description: ベストプラクティスアナライザーのグループメンバーシップとユーザー権限の要件。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Group memberships and user rights requirements for Best Practices Analyzer
ms:assetid: f812e343-8f75-454e-b7a8-1b404e32071a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg591354(v=OCS.15)
ms:contentKeyID: 48185869
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 64a7d785a77701c6796488178a7cce10caf54f42
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427825"
---
# <a name="group-memberships-and-user-rights-requirements-for-best-practices-analyzer-in-lync-server-2013"></a><span data-ttu-id="accf4-103">Lync Server 2013 でのベストプラクティスアナライザーのグループメンバーシップとユーザー権限の要件</span><span class="sxs-lookup"><span data-stu-id="accf4-103">Group memberships and user rights requirements for Best Practices Analyzer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="accf4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="accf4-104">

<span> </span></span></span>

<span data-ttu-id="accf4-105">_**最終更新日:** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="accf4-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="accf4-106">ベストプラクティスアナライザーを正常に実行するには、ログオンに使用するユーザーアカウントが、ローカルコンピューターの管理者グループのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="accf4-106">To successfully run Best Practices Analyzer, the user account that you use to log on must be a member of the Administrators group on the local computer.</span></span> <span data-ttu-id="accf4-107">さらに、環境をスキャンするには、ユーザーアカウントが次のグループのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="accf4-107">Additionally, to scan your environment, the user account must be a member of the following groups:</span></span>

  - <span data-ttu-id="accf4-108">**ドメイン管理者**   Active Directory ドメインサービスの情報を列挙し、ドメインコントローラーとグローバルカタログサーバー上の Windows Management Instrumentation (WMI) プロバイダーを呼び出すには、こちらを参照してください。</span><span class="sxs-lookup"><span data-stu-id="accf4-108">**Domain Admins**   To enumerate Active Directory Domain Services information and to call the Windows Management Instrumentation (WMI) providers on domain controllers and global catalog servers.</span></span>

  - <span data-ttu-id="accf4-109">**管理者**   各 Lync Server 2013 内部コンピューターと各エッジサーバーで、Windows Management Instrumentation (WMI) プロバイダーを呼び出してレジストリにアクセスするために必要です。</span><span class="sxs-lookup"><span data-stu-id="accf4-109">**Administrators**   Required on each Lync Server 2013 internal computer and each Edge Server to call the Windows Management Instrumentation (WMI) providers and to access the registry.</span></span>

  - <span data-ttu-id="accf4-110">**RTCUniversalReadOnlyAdmins**   フルまたは委任された読み取り専用の Lync Server 2013 管理者権限。</span><span class="sxs-lookup"><span data-stu-id="accf4-110">**RTCUniversalReadOnlyAdmins**   Full or delegated read only Lync Server 2013 administrative rights.</span></span>

  - <span data-ttu-id="accf4-111">**Exchange の表示のみ管理者**   Microsoft Exchange 組織のフルまたは委任された Exchange の表示のみの管理者。</span><span class="sxs-lookup"><span data-stu-id="accf4-111">**Exchange View Only Administrator**   Full or delegated Exchange View Only Administrator on the Microsoft Exchange organization.</span></span>

<span data-ttu-id="accf4-112">ユーザーアカウントに十分なユーザー権限がない場合は、次の2つのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="accf4-112">If your user account does not have sufficient user rights, you have two options:</span></span>

  - <span data-ttu-id="accf4-113">コマンドプロンプトで、 **runas** コマンドを使用して、十分なユーザー権限があるアカウントでツールを実行します。</span><span class="sxs-lookup"><span data-stu-id="accf4-113">At a command prompt, use the **runas** command to run the tool under an account that does have sufficient user rights.</span></span> <span data-ttu-id="accf4-114">構文は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="accf4-114">The syntax is as follows:</span></span>
    
        runas /netonly /user:<domain>\<userName> rtcbpa.exe

  - <span data-ttu-id="accf4-115">[ **Active Directory に接続する** ] ページで、ベストプラクティスアナライザーを実行するために使用する予定のアカウントの資格情報を設定します。</span><span class="sxs-lookup"><span data-stu-id="accf4-115">On the **Connect to Active Directory** page, set the credentials for the accounts that you plan to use to run Best Practices Analyzer.</span></span> <span data-ttu-id="accf4-116">[ **詳細ログインオプションの表示] を** クリックします。</span><span class="sxs-lookup"><span data-stu-id="accf4-116">Click **Show advanced login options**.</span></span> <span data-ttu-id="accf4-117">Active Directory ドメインサービスへの接続用に1つ、Lync Server 2013 エッジサーバーへの接続用、および Exchange サーバーへの接続用の3つのアカウントを入力できます。</span><span class="sxs-lookup"><span data-stu-id="accf4-117">You can enter three accounts: one for connecting to Active Directory Domain Services, one for connecting to Lync Server 2013 Edge Servers, and one for connecting to the Exchange Servers.</span></span> <span data-ttu-id="accf4-118">これらのいずれかのアカウントを指定しない場合、ログオンに使用したユーザーアカウントとベストプラクティスアナライザーを実行するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="accf4-118">If you do not specify any of these accounts, the user account that you used to log on and run Best Practices Analyzer is used.</span></span>

<span data-ttu-id="accf4-119"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="accf4-119"></div>

<span> </span>

</div>

</div>

</span></span></div>

