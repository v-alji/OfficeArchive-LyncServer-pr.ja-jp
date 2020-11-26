---
title: 'Lync Server 2013: 認証済みユーザーのアクセス許可が削除されている'
description: 'Lync Server 2013: 認証されたユーザーのアクセス許可が削除されます。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Authenticated user permissions are removed
ms:assetid: 5fcd70a5-813a-4076-9bb6-5b0d47505038
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398425(v=OCS.15)
ms:contentKeyID: 48184304
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 59da0ec893395405010afdd0263bd6be5d646881
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438156"
---
# <a name="authenticated-user-permissions-are-removed-in-lync-server-2013"></a><span data-ttu-id="76c6e-103">Lync Server 2013 で認証済みユーザーのアクセス許可が削除されている</span><span class="sxs-lookup"><span data-stu-id="76c6e-103">Authenticated user permissions are removed in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="76c6e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="76c6e-104">

<span> </span></span></span>

<span data-ttu-id="76c6e-105">_**最終更新日:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="76c6e-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="76c6e-106">ロックダウンされた Active Directory 環境では、認証済みユーザーアクセス制御エントリ (Ace) は、ユーザー、構成、システム、およびユーザーオブジェクトが保存されている組織単位 (Ou) を含む、既定の Active Directory コンテナーから削除されます。</span><span class="sxs-lookup"><span data-stu-id="76c6e-106">In a locked-down Active Directory environment, authenticated user access control entries (ACEs) are removed from the default Active Directory containers, including the Users, Configuration or System, and organizational units (OUs) where User and Computer objects are stored.</span></span> <span data-ttu-id="76c6e-107">認証済みユーザー Ace を削除すると、Active Directory 情報への読み取りアクセスができなくなります。</span><span class="sxs-lookup"><span data-stu-id="76c6e-107">Removing authenticated user ACEs prevents read access to Active Directory information.</span></span> <span data-ttu-id="76c6e-108">ただし、Ace を削除すると、ユーザーがドメインの準備を実行できるように、これらのコンテナーの読み取りアクセス許可に依存するため、Lync Server 2013 の問題が発生します。</span><span class="sxs-lookup"><span data-stu-id="76c6e-108">However, removing the ACEs creates issues for Lync Server 2013 because it depends on read permissions to these containers to allow users to run domain preparation.</span></span>

<span data-ttu-id="76c6e-109">この状況では、ドメインの準備、サーバーのアクティブ化、プールの作成を実行するために必要な Domain Admins グループのメンバーシップが、既定のコンテナーに格納されている Active Directory 情報への読み取りアクセス許可を付与することはなくなりました。</span><span class="sxs-lookup"><span data-stu-id="76c6e-109">In this situation, membership in the Domain Admins group, which is required to run domain preparation, server activation, and pool creation, no longer grants read access to Active Directory information stored in the default containers.</span></span> <span data-ttu-id="76c6e-110">必要なフォレストの準備手順が完了していることを確認するには、フォレストルートドメイン内のさまざまなコンテナーの読み取りアクセス許可を手動で付与する必要があります。</span><span class="sxs-lookup"><span data-stu-id="76c6e-110">You must manually grant read-access permissions on various containers in the forest root domain to check that the prerequisite forest preparation procedure is complete.</span></span>

<span data-ttu-id="76c6e-111">フォレスト以外のルートドメインでドメインの準備、サーバーのアクティブ化、またはプールの作成を実行できるようにするには、次のオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="76c6e-111">To enable a user to run domain preparation, server activation, or pool creation on any non-forest root domain, you have the following options:</span></span>

  - <span data-ttu-id="76c6e-112">エンタープライズ管理者グループのメンバーであるアカウントを使用して、ドメインの準備を実行します。</span><span class="sxs-lookup"><span data-stu-id="76c6e-112">Use an account that is a member of the Enterprise Admins group to run domain preparation.</span></span>

  - <span data-ttu-id="76c6e-113">Domain Admins グループのメンバーであるアカウントを使用し、フォレストルートドメイン内の次の各コンテナーで、このアカウントに読み取りアクセス許可を付与します。</span><span class="sxs-lookup"><span data-stu-id="76c6e-113">Use an account that is a member of the Domain Admins group and grant this account read-access permissions on each of the following containers in the forest root domain:</span></span>
    
      - <span data-ttu-id="76c6e-114">Domain</span><span class="sxs-lookup"><span data-stu-id="76c6e-114">Domain</span></span>
    
      - <span data-ttu-id="76c6e-115">構成またはシステム</span><span class="sxs-lookup"><span data-stu-id="76c6e-115">Configuration or System</span></span>

<span data-ttu-id="76c6e-116">エンタープライズ管理者グループのメンバーであるアカウントを使用して、ドメインの準備またはその他のセットアップタスクを実行しない場合は、フォレストルートの関連するコンテナーで読み取りアクセスを使用するアカウントを明示的に付与します。</span><span class="sxs-lookup"><span data-stu-id="76c6e-116">If you do not want to use an account that is a member of the Enterprise Admins group to run domain preparation or other Setup tasks, explicitly grant the account you want to use read access on the relevant containers in the forest root.</span></span>

<div>

## <a name="to-give-users-read-access-permissions-on-containers-in-the-forest-root-domain"></a><span data-ttu-id="76c6e-117">フォレストのルートドメインのコンテナーの読み取りアクセス許可をユーザーに付与するには</span><span class="sxs-lookup"><span data-stu-id="76c6e-117">To give users read-access permissions on containers in the forest root domain</span></span>

1.  <span data-ttu-id="76c6e-118">フォレストルートドメインの Domain Admins グループのメンバーであるアカウントで、フォレストルートドメインに参加しているコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="76c6e-118">Log on to the computer joined to the forest root domain with an account that is a member of the Domain Admins group for the forest root domain.</span></span>

2.  <span data-ttu-id="76c6e-119">フォレストルートドメインに対して adsiedit を実行します。</span><span class="sxs-lookup"><span data-stu-id="76c6e-119">Run adsiedit.msc for the forest root domain.</span></span>
    
    <span data-ttu-id="76c6e-120">認証済みユーザー Ace がドメイン、構成、またはシステムコンテナーから削除された場合は、次の手順で説明するように、コンテナーに読み取り専用のアクセス許可を付与する必要があります。</span><span class="sxs-lookup"><span data-stu-id="76c6e-120">If authenticated user ACEs were removed from the Domain, Configuration, or System container, you must grant read-only permissions to the container, as described in the following steps.</span></span>

3.  <span data-ttu-id="76c6e-121">コンテナーを右クリックし、[ **プロパティ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="76c6e-121">Right-click the container, and then click **Properties**.</span></span>

4.  <span data-ttu-id="76c6e-122">[ **セキュリティ** ] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="76c6e-122">Click the **Security** tab.</span></span>

5.  <span data-ttu-id="76c6e-123">[**詳細設定**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="76c6e-123">Click **Advanced**.</span></span>

6.  <span data-ttu-id="76c6e-124">[ **権限** ] タブの [ **追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="76c6e-124">On the **Permissions** tab, click **Add**.</span></span>

7.  <span data-ttu-id="76c6e-125">次の形式を使用して、アクセス許可を付与するユーザーまたはグループの名前を入力し `domain\account name` 、[ **OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="76c6e-125">Type the name of the user or group receiving permissions by using the following format: `domain\account name`, and then click **OK**.</span></span>

8.  <span data-ttu-id="76c6e-126">[ **オブジェクト** ] タブの [ **適用** 対象] で、[ **このオブジェクトのみ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="76c6e-126">On the **Objects** tab, in **Applies To**, click **This Object Only**.</span></span>

9.  <span data-ttu-id="76c6e-127">[ **権限**] で、[ **許可する** 列: **リストコンテンツ**]、[すべての **プロパティの読み取り**]、[ **アクセス許可の読み取り**] の順にクリックして、次の許可 ace を選択します。</span><span class="sxs-lookup"><span data-stu-id="76c6e-127">In **Permissions**, select the following Allow ACEs by clicking the **Allow** column: **List Content**, **Read All Properties**, and **Read Permissions**.</span></span>

10. <span data-ttu-id="76c6e-128">[ **OK]** を2回クリックします。</span><span class="sxs-lookup"><span data-stu-id="76c6e-128">Click **OK** twice.</span></span>

11. <span data-ttu-id="76c6e-129">手順2に示されている関連コンテナーについて、この手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="76c6e-129">Repeat these steps for any of the relevant containers listed in Step 2.</span></span>

<span data-ttu-id="76c6e-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="76c6e-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

