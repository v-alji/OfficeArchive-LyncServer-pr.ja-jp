---
title: 移行のプロセス - 詳細
description: 移行プロセス-詳細。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migration process - details
ms:assetid: ca7e352c-9bde-47d9-8273-5cf2fdfdfe7e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205264(v=OCS.15)
ms:contentKeyID: 48185412
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b8ecc5f23a328aef7cc65ad84e28dbb629d44b91
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438604"
---
# <a name="migration-process---details"></a><span data-ttu-id="b715e-103">移行のプロセス - 詳細</span><span class="sxs-lookup"><span data-stu-id="b715e-103">Migration process - details</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b715e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b715e-104">

<span> </span></span></span>

<span data-ttu-id="b715e-105">_**最終更新日:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="b715e-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="b715e-106">Lync Server 2010、グループチャット、または Office Communications Server 2007 R2 グループチャットを Lync Server 2013、常設チャットサーバーに移行するには、次の前提条件と詳細な手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="b715e-106">Use the following prerequisites and detailed steps to migrate either Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server.</span></span>

<div>

## <a name="prerequisites-for-migration"></a><span data-ttu-id="b715e-107">移行の前提条件</span><span class="sxs-lookup"><span data-stu-id="b715e-107">Prerequisites for Migration</span></span>

<span data-ttu-id="b715e-108">Lync Server 2010、グループチャット、または Office Communications Server 2007 R2 グループチャットを Lync Server 2013、常設チャットサーバーに移行する前に、次の前提条件を満たしていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b715e-108">Be sure that you’ve met the following prerequisites before migrating either Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server.</span></span>

1.  <span data-ttu-id="b715e-109">Lync Server 2013 プールを少なくとも1つ展開します。</span><span class="sxs-lookup"><span data-stu-id="b715e-109">Deploy at least one Lync Server 2013 pool.</span></span> <span data-ttu-id="b715e-110">複数の Lync Server 2013 プールがある場合は、新しい Lync server 2013 常設チャットサーバープールのホームプールにする Lync Server 2013 プールを決定します。</span><span class="sxs-lookup"><span data-stu-id="b715e-110">If you have multiple Lync Server 2013 pools, decide which Lync Server 2013 pool will be the home pool for the new Lync Server 2013 Persistent Chat Server pool.</span></span>

2.  <span data-ttu-id="b715e-111">Lync Server 2013 の常設チャットサーバープールをインストールします。</span><span class="sxs-lookup"><span data-stu-id="b715e-111">Install the Lync Server 2013, Persistent Chat Server pool.</span></span> <span data-ttu-id="b715e-112">空 (カテゴリ、ルーム、アドインは含まれません) になります。</span><span class="sxs-lookup"><span data-stu-id="b715e-112">It will be empty (no categories, rooms, or add-ins).</span></span> <span data-ttu-id="b715e-113">従来のカテゴリ、会議室、またはアドインを移行する前に、Lync Server 2013 の常設チャットサーバーの展開で、会議室、カテゴリ、アドインを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="b715e-113">Before you migrate your legacy categories, rooms, or add-ins, you can create rooms, categories, or add-ins in your Lync Server 2013, Persistent Chat Server deployment.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="b715e-114">新しく作成されたアイテムは、移行した従来のアイテムと競合することがあります。</span><span class="sxs-lookup"><span data-stu-id="b715e-114">Be aware that these newly created items may conflict with legacy items that you migrate.</span></span> <span data-ttu-id="b715e-115">名前の競合を回避します。そうしないと、従来のデータが移行されるときに上書きされます。</span><span class="sxs-lookup"><span data-stu-id="b715e-115">Avoid any naming conflicts; otherwise, they will be overwritten when the legacy data is migrated.</span></span>

    
    </div>

</div>

<div>

## <a name="preparing-the-source-data-for-migration"></a><span data-ttu-id="b715e-116">移行のためのソースデータの準備</span><span class="sxs-lookup"><span data-stu-id="b715e-116">Preparing the Source Data for Migration</span></span>

<span data-ttu-id="b715e-117">移行のためにソースデータを適切に準備するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b715e-117">Perform the following steps to properly prepare your source data for migration.</span></span>

1.  <span data-ttu-id="b715e-118">Lync Server 2010、グループチャット、または Office Communications Server 2007 R2 グループチャットのソースデータベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="b715e-118">Back up the source databases for either Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat.</span></span> <span data-ttu-id="b715e-119">SQL Server のバックアップの詳細については、「バックアップの概要 (SQL Server)」を参照してください <https://go.microsoft.com/fwlink/p/?linkid=254851> 。</span><span class="sxs-lookup"><span data-stu-id="b715e-119">For details about backing up SQL Server, see "Backup Overview (SQL Server)" at <https://go.microsoft.com/fwlink/p/?linkid=254851>.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="b715e-120">Active Directory ドメインサービスは同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="b715e-120">Active Directory Domain Services should be the same.</span></span> <span data-ttu-id="b715e-121">移行の条件として、別の展開 (具体的には別の Active Directory フォレスト) のプールに移行することはできません。</span><span class="sxs-lookup"><span data-stu-id="b715e-121">As a condition for migration, you cannot migrate to a pool in a different deployment (specifically, in a different Active Directory forest).</span></span>

    
    </div>

2.  <span data-ttu-id="b715e-122">Lync Server 2010、グループチャット、または Office Communications Server 2007 R2 グループチャットルームとカテゴリ構成を検査します。</span><span class="sxs-lookup"><span data-stu-id="b715e-122">Inspect your Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat chat rooms and category configuration.</span></span> <span data-ttu-id="b715e-123">既存のレガシー展開で、カテゴリ、ルーム、またはアドインに対する変更は、グループチャット管理ツールによって実行されます。</span><span class="sxs-lookup"><span data-stu-id="b715e-123">Any changes to categories, rooms, or add-ins in your existing legacy deployment will be done by the Group Chat Admin Tool.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="b715e-124">Lync Server 2013 の [カテゴリ]、[ルーム]、または [アドイン] に対する変更は、[Lync Server] コントロールパネルまたは Windows PowerShell コマンドレットによって実行されます。</span><span class="sxs-lookup"><span data-stu-id="b715e-124">Any changes to categories, rooms, or add-ins in your Lync Server 2013, Persistent Chat Server deployment are performed by the Lync Server Control Panel or Windows PowerShell cmdlets.</span></span>

    
    </div>
    
    <span data-ttu-id="b715e-125">次の手順に従って、移行用のレガシシステムを準備します。</span><span class="sxs-lookup"><span data-stu-id="b715e-125">Follow these steps to prepare your legacy system for migration.</span></span>
    
    1.  <span data-ttu-id="b715e-126">常設チャットサーバーは、カテゴリの深い階層セットとは異なり、1つのレベルのカテゴリをサポートします。</span><span class="sxs-lookup"><span data-stu-id="b715e-126">Persistent Chat Server supports a single level of categories, unlike a deep hierarchical set of categories.</span></span> <span data-ttu-id="b715e-127">移行後、サブカテゴリには完全な親カテゴリ名のプレフィックスが付きます。</span><span class="sxs-lookup"><span data-stu-id="b715e-127">After migration, the subcategories are prefixed with full parent category names.</span></span> <span data-ttu-id="b715e-128">結果としての構造が要件を満たすように、既存のカテゴリ構造を単純化してフラット化することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b715e-128">You might want to simplify and flatten your existing category structure so that the resulting structure meets your requirements.</span></span>
    
    2.  <span data-ttu-id="b715e-129">ルートカテゴリの **マネージャー** を確認します。</span><span class="sxs-lookup"><span data-stu-id="b715e-129">Verify the **Managers** at the root Category.</span></span> <span data-ttu-id="b715e-130">このレベルにマネージャーが存在する場合、これらのユーザーは、移行後 **にすべてのルームにマネージャー** として追加されます。</span><span class="sxs-lookup"><span data-stu-id="b715e-130">If any Managers exist at this level, these users will be added as **Managers to all rooms** after migration.</span></span> <span data-ttu-id="b715e-131">組織の要件ではない場合は、これらのマネージャーをルートカテゴリから削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b715e-131">If this is not a requirement for your organization, you need to remove these Managers from the root Category.</span></span>
    
    3.  <span data-ttu-id="b715e-132">ルーム名の長さを確認します。</span><span class="sxs-lookup"><span data-stu-id="b715e-132">Verify the length of room names.</span></span> <span data-ttu-id="b715e-133">カテゴリ構造が簡素化されたため、移行後、カテゴリ構造が子カテゴリの下に存在する場合、そのルームには完全な親カテゴリ名のプレフィックスが付きます。</span><span class="sxs-lookup"><span data-stu-id="b715e-133">After migration, due to simplified category structures, if the rooms exist under a child category, they are prefixed with full parent category names.</span></span> <span data-ttu-id="b715e-134">名前付けの制限は、親カテゴリ名を含む256文字です。</span><span class="sxs-lookup"><span data-stu-id="b715e-134">The naming limit is 256 characters, including parent category names.</span></span> <span data-ttu-id="b715e-135">会議室名の長さを確認し、長すぎる場合は長さを短くする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b715e-135">You must verify the length of the room names and possibly shorten the length, if they are too long.</span></span>
    
    4.  <span data-ttu-id="b715e-136">Lync Server 2013 で、カテゴリの **招待** の設定が true に設定されている場合は、そのカテゴリの下の会議室への招待について true または false を選ぶことができます。</span><span class="sxs-lookup"><span data-stu-id="b715e-136">In Lync Server 2013, if the category **invitations** settings are set to true, you can choose true or false for invitations to rooms under that category.</span></span> <span data-ttu-id="b715e-137">ただし、カテゴリの招待状の設定が false に設定されている場合、そのカテゴリの下の [会議出席依頼] はオフになっています。</span><span class="sxs-lookup"><span data-stu-id="b715e-137">However if the category invitations settings are set to false, rooms under that category have invitations turned off.</span></span> <span data-ttu-id="b715e-138">移行する前に、特定のカテゴリの下に会議室が存在するようにするには、従来の Lync Server グループチャットサーバーバージョンで招待の設定をリセットする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b715e-138">Before migration, you must reset the invitation settings in your legacy Lync Server Group Chat Server version, if you want room(s) to exist under a specific category.</span></span> <span data-ttu-id="b715e-139">そうしないと、移行中に、Lync Server 2013 で警告が表示され、会議室が false の既定値に設定されます。</span><span class="sxs-lookup"><span data-stu-id="b715e-139">Otherwise, during migration, Lync Server 2013 displays warnings and sets rooms to the default value of false.</span></span>
    
    5.  <span data-ttu-id="b715e-140">チャットルームでファイルを使用した場合は、移行後にファイルを新しい常設チャットファイルストアに手動で XCOPY する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b715e-140">If you used files in chat rooms, you must XCOPY the files manually to the new Persistent Chat file store after migration.</span></span> <span data-ttu-id="b715e-141">この操作は、ツールでは実行できません。</span><span class="sxs-lookup"><span data-stu-id="b715e-141">The tools don’t do this.</span></span>
    
    6.  <span data-ttu-id="b715e-142">フェデレーションされたユーザーとのフェデレーションユーザーとルームがある場合は、常設チャットサーバーでフェデレーションがサポートされていないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b715e-142">If you had federated users and rooms with federated users, be aware that Persistent Chat Server does not support federation.</span></span> <span data-ttu-id="b715e-143">フェデレーションされたユーザーがいるルームは移行されます。ただし、フェデレーションアクセスはサポートされていないため、ユーザー自身がコンテンツにアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="b715e-143">Rooms with federated users will be migrated; however, the users themselves won’t be able to access the content, because federated access is not supported.</span></span>
    
    7.  <span data-ttu-id="b715e-144">移行しない会議室を特定して、無効としてマークします。</span><span class="sxs-lookup"><span data-stu-id="b715e-144">Identify those rooms that you do not want to migrate, and mark them as disabled.</span></span>
    
    8.  <span data-ttu-id="b715e-145">チャットルームのコンテンツを移行する日付以降の日付を指定します。</span><span class="sxs-lookup"><span data-stu-id="b715e-145">Identify the date beyond which you want to migrate the chat room content.</span></span> <span data-ttu-id="b715e-146">たとえば、2010年1月1日より前にメッセージを移行したくない場合もあります。これらのメッセージは、移行に関連していない可能性があるためです。</span><span class="sxs-lookup"><span data-stu-id="b715e-146">For example, you may not want to migrate messages earlier than January 1, 2010, because these messages may be obsolete or not relevant for migration.</span></span>

</div>

<div>

## <a name="performing-the-migration"></a><span data-ttu-id="b715e-147">移行の実行</span><span class="sxs-lookup"><span data-stu-id="b715e-147">Performing the Migration</span></span>

<span data-ttu-id="b715e-148">次の手順を実行して、従来のグループチャットサーバーを移行します。</span><span class="sxs-lookup"><span data-stu-id="b715e-148">Perform the following steps to migrate your legacy Group Chat Server.</span></span>

1.  <span data-ttu-id="b715e-149">Lync Server 2010、グループチャット、Office Communications Server 2007 R2 グループチャット、または Lync Server 2013、常設 Chat Server サービスをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="b715e-149">Shut down the Lync Server 2010, Group Chat, Office Communications Server 2007 R2 Group Chat or Lync Server 2013, Persistent Chat Server services.</span></span> <span data-ttu-id="b715e-150">すべてのサービスを停止する必要があるため、十分なダウンタイムがある場合は一度にこの操作を計画してください。</span><span class="sxs-lookup"><span data-stu-id="b715e-150">All services must be stopped, so plan to do this at a time when there is enough downtime.</span></span> <span data-ttu-id="b715e-151">前に説明したように、現在のグループチャットデータベースをバックアップしてください。</span><span class="sxs-lookup"><span data-stu-id="b715e-151">As previously described, make sure to back up your current Group Chat database.</span></span>

2.  <span data-ttu-id="b715e-152">常設チャット管理者の RBAC 役割 (CsPersistentChatAdministrator) のメンバーとして Windows PowerShell **CsPersistentChatData** コマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="b715e-152">Run the Windows PowerShell **Export-CsPersistentChatData** cmdlet as a member of the Persistent Chat administrator RBAC role (CsPersistentChatAdministrator).</span></span> <span data-ttu-id="b715e-153">エクスポート/インポートコマンドレットの詳細については、「 [Lync server 2013 で Windows PowerShell コマンドレットを使用した常設チャットサーバー構成のトラブルシューティング](lync-server-2013-troubleshooting-persistent-chat-server-configuration-using-windows-powershell-cmdlets.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b715e-153">For details about the export/import cmdlets, see [Troubleshooting Persistent Chat Server configuration using Windows PowerShell cmdlets in Lync Server 2013](lync-server-2013-troubleshooting-persistent-chat-server-configuration-using-windows-powershell-cmdlets.md).</span></span>
    
    <span data-ttu-id="b715e-154">エクスポートされた内容を検査します。</span><span class="sxs-lookup"><span data-stu-id="b715e-154">Inspect the exported contents.</span></span>

3.  <span data-ttu-id="b715e-155">インポートする準備ができたら、Lync Server 2013 の常設チャットサーバーサービスを終了します。</span><span class="sxs-lookup"><span data-stu-id="b715e-155">Before you’re ready to import, shut down Lync Server 2013, Persistent Chat Server services.</span></span> <span data-ttu-id="b715e-156">すべてのサービスを停止する必要があるため、十分なダウンタイムがある場合は一度にこの操作を計画してください。</span><span class="sxs-lookup"><span data-stu-id="b715e-156">All services need to be stopped, so plan to do this at a time when there is enough downtime.</span></span>

4.  <span data-ttu-id="b715e-157">移行前に、Lync Server 2013 展開でカテゴリ、ルーム、またはアドインを作成した場合は、常設チャットデータベースのバックアップを実行します。</span><span class="sxs-lookup"><span data-stu-id="b715e-157">Perform a backup of the Persistent Chat database if you had created any categories, rooms, or add-ins in your Lync Server 2013 deployment before the migration.</span></span> <span data-ttu-id="b715e-158">エクスポート/インポートプロセスでは、従来のデータを Lync Server 2013 の展開に統合することはできますが、コンテンツが誤って上書きされる場合 (たとえば、名前の競合が存在する場合)、データベースのバックアップを作成することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b715e-158">The export/import process will be able to merge the legacy data into the Lync Server 2013 deployment, but you’ll want to back up the database in case that content is inadvertently overwritten (for example, if naming conflicts still exist).</span></span>

5.  <span data-ttu-id="b715e-159">**WhatIf** コマンドを使用して Windows PowerShell **CsPersistentChatData** コマンドレット (インポートツール) を実行し、移行されたデータを使用して常設チャットサーバープールのバックエンドサーバーを設定します。</span><span class="sxs-lookup"><span data-stu-id="b715e-159">Run the Windows PowerShell **Import-CsPersistentChatData** cmdlet (import tool), with a **WhatIf** command to populate the Back End Server of the Persistent Chat Server pool with migrated data.</span></span> <span data-ttu-id="b715e-160">単純化された管理モデルに対応するために、一部の変換がプロセスで行われます。</span><span class="sxs-lookup"><span data-stu-id="b715e-160">Some conversions happen in the process to accommodate the simplified administration model.</span></span> <span data-ttu-id="b715e-161">表示されるエラーや警告を修正します。</span><span class="sxs-lookup"><span data-stu-id="b715e-161">Fix any errors or warnings that appear.</span></span>

6.  <span data-ttu-id="b715e-162">常設チャットサーバー Windows PowerShell の **CsPersistentChatData** コマンドレットを、常設チャット管理者の RBAC 役割 (CsPersistentChatAdministrator) のメンバーとして実行します。</span><span class="sxs-lookup"><span data-stu-id="b715e-162">Run the Persistent Chat Server Windows PowerShell **Import-CsPersistentChatData** cmdlet as a member of the Persistent Chat administrator RBAC role (CsPersistentChatAdministrator).</span></span> <span data-ttu-id="b715e-163">エクスポート/インポートコマンドレットの詳細については、「 [Lync server 2013 で Windows PowerShell コマンドレットを使用した常設チャットサーバー構成のトラブルシューティング](lync-server-2013-troubleshooting-persistent-chat-server-configuration-using-windows-powershell-cmdlets.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b715e-163">For details about the export/import cmdlets, see [Troubleshooting Persistent Chat Server configuration using Windows PowerShell cmdlets in Lync Server 2013](lync-server-2013-troubleshooting-persistent-chat-server-configuration-using-windows-powershell-cmdlets.md).</span></span>

7.  <span data-ttu-id="b715e-164">アップロードされたすべてのファイル (フォルダー全体) を新しい Lync Server 2013 の常設チャットファイルストアに XCOPY する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b715e-164">You must XCOPY all uploaded files (the entire folder) to the new Lync Server 2013, Persistent Chat file store.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="b715e-165">Lync 2013 (クライアント) では、チャットルームでのファイルのアップロードまたは表示はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="b715e-165">The Lync 2013 (client) does not support uploading or viewing files in chat rooms.</span></span> <span data-ttu-id="b715e-166">引き続き、従来のクライアントを使用して、会議室でのファイルの投稿と表示を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="b715e-166">You can still use the legacy client to post and view files in the room.</span></span>

    
    </div>

8.  <span data-ttu-id="b715e-167">Lync Server 2010、グループチャット、または Office Communications Server 2007 R2 グループチャット検索サーバー URI を Lync Server 2013、常設チャットサーバーの連絡先オブジェクトに移植します。</span><span class="sxs-lookup"><span data-stu-id="b715e-167">Port the Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat Lookup Server URI to the Lync Server 2013, Persistent Chat Server contact object.</span></span> <span data-ttu-id="b715e-168">次の手順が必要なのは、Lync 2010 グループチャットまたは Office Communicator 2007 R2 グループチャットクライアントで、移行後に最新の Lync 2013、常設チャット (クライアント) に接続する必要がある場合に、クライアント側の構成が変更されない場合です。</span><span class="sxs-lookup"><span data-stu-id="b715e-168">The following steps are required if either your Lync 2010 Group Chat or Office Communicator 2007 R2 Group Chat clients need to connect to the latest Lync 2013, Persistent Chat (client) after migration without any client-side configuration changes:</span></span>
    
      - <span data-ttu-id="b715e-169">Ocschat@ \<domainName\> .Com 参照サーバーのユーザーアカウントを削除します。</span><span class="sxs-lookup"><span data-stu-id="b715e-169">Delete the ocschat@\<domainName\>.com Lookup Server user account.</span></span> <span data-ttu-id="b715e-170">これは、Lync Server 2010 の [グループチャット] で参照サービスを指すために使用されました。</span><span class="sxs-lookup"><span data-stu-id="b715e-170">This was used to point to the Lookup Service in Lync Server 2010, Group Chat.</span></span> <span data-ttu-id="b715e-171">プールをアンインストールして、後で信頼済みエントリを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="b715e-171">You can uninstall the pool and remove trusted entries later.</span></span>
    
      - <span data-ttu-id="b715e-172">従来のエンドポイント (常設チャットサーバーの連絡先オブジェクト) を作成するには、同じ SIP URI を使用して Windows PowerShell コマンドレット **CsPersistentChatEndpoint を実行** します。これにより、サービスの再開時にレガシクライアントが効率的に動作するようになります。</span><span class="sxs-lookup"><span data-stu-id="b715e-172">Create a legacy endpoint (Persistent Chat Server contact object) by running the Windows PowerShell cmdlet, **New-CsPersistentChatEndpoint**, with the identical SIP URI so that the legacy client will work effectively when the service is restarted.</span></span>
    
    <span data-ttu-id="b715e-173">この時点では、必須の移行プロセスが完了しています。</span><span class="sxs-lookup"><span data-stu-id="b715e-173">The mandatory migration process is complete at this point.</span></span> <span data-ttu-id="b715e-174">Lync 2010 グループチャット (クライアント) または Office Communicator 2007 R2 グループチャット (クライアント) は、新しい常設チャットサーバープールに、透過的に接続できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="b715e-174">Lync 2010 Group Chat (clients) or Office Communicator 2007 R2 Group Chat (clients) can connect to the new Persistent Chat Server pool now, transparently.</span></span>
    
    <span data-ttu-id="b715e-175">Lync Server 2010、グループチャット、または Office Communications Server 2007 R2 グループチャットのその他の廃止手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b715e-175">Follow these additional decommissioning steps for Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat.</span></span>

9.  <span data-ttu-id="b715e-176">新しい常設チャットサーバープールのすべてのコンピューターをオンにして、常設チャットサーバーサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="b715e-176">Start the Persistent Chat Server services by turning on all computers in the new Persistent Chat Server pool.</span></span>

10. <span data-ttu-id="b715e-177">Lync Server コントロールパネルと Windows PowerShell コマンドレットを使用して、データが正常に移行されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="b715e-177">Use the Lync Server Control Panel and Windows PowerShell cmdlets to verify that the data has migrated successfully.</span></span>

11. <span data-ttu-id="b715e-178">グループチャットサーバープールのコンピューターから Lync 2010 グループチャットまたは Office Communicator 2007 R2 グループチャットをアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="b715e-178">Uninstall Lync 2010 Group Chat or Office Communicator 2007 R2 Group Chat from the computers in the Group Chat Server pool.</span></span>

12. <span data-ttu-id="b715e-179">Windows PowerShell コマンドレットを使用して、信頼されているアプリケーションと信頼されているアプリケーションプールを削除します。</span><span class="sxs-lookup"><span data-stu-id="b715e-179">Delete the trusted application and trusted application pool using Windows PowerShell cmdlets.</span></span> <span data-ttu-id="b715e-180">これにより、これらのアイテムは、サーバーの全体管理ストアと、関連付けられた信頼済みサービスエントリ (TSEs) から Active Directory から削除されます。</span><span class="sxs-lookup"><span data-stu-id="b715e-180">This deletes these items from the Central Management store and the associated Trusted Service Entries (TSEs) from the Active Directory.</span></span> <span data-ttu-id="b715e-181">または、この手順はトポロジービルダーを使用して動作します (信頼されているアプリケーション/プールにも、専用のノードが含まれています)。</span><span class="sxs-lookup"><span data-stu-id="b715e-181">Alternatively, this step works by using the Topology Builder (the trusted applications/pools have a dedicated node there, also).</span></span>

13. <span data-ttu-id="b715e-182">これで、新しいクライアントで常設チャットサーバー機能を有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="b715e-182">You can now begin to enable Persistent Chat Server functionality through the new clients.</span></span> <span data-ttu-id="b715e-183">常設チャットサーバーを有効にする方法について詳しくは、「 [Lync server 2013 での常設チャットサーバーの展開](lync-server-2013-deploying-persistent-chat-server.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="b715e-183">For details about enabling Persistent Chat Server, see [Deploying Persistent Chat Server in Lync Server 2013](lync-server-2013-deploying-persistent-chat-server.md).</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="b715e-184">Lync Server 2013 は、複数の常設チャットサーバープールをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="b715e-184">Lync Server 2013 supports multiple Persistent Chat Server pools.</span></span> <span data-ttu-id="b715e-185">ただし、Lync 2010 グループチャットまたは Office Communications Server 2007 R2 &nbsp; グループチャットプールを単一の Lync Server 2013、常設チャットサーバープールに移行することをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="b715e-185">However, we support migrating a Lync 2010 Group Chat or Office Communications Server 2007 R2&nbsp;Group Chat pool to a single Lync Server 2013, Persistent Chat Server pool.</span></span> <span data-ttu-id="b715e-186">新しい常設チャットサーバープールを展開に追加して、規制要件を満たすことができます (たとえば、特定の地理内のデータを保持する)。</span><span class="sxs-lookup"><span data-stu-id="b715e-186">You can add additional new Persistent Chat Server pools in your deployment to meet the regulatory needs (for example, keeping data within a given geography).</span></span>

    
    <span data-ttu-id="b715e-187"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b715e-187"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

