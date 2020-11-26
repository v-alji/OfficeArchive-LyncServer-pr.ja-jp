---
title: 'Lync Server 2013: アーカイブのしくみ'
description: 'Lync Server 2013: アーカイブのしくみ'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: How Archiving works
ms:assetid: 536a52a9-cfb7-4392-9620-ffc5b319b31b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204900(v=OCS.15)
ms:contentKeyID: 48184174
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 57a5ef19c0781b4faa279a6aad46ac34b83ae0f9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427496"
---
# <a name="how-archiving-works-in-lync-server-2013"></a><span data-ttu-id="48aa8-103">Lync Server 2013 でのアーカイブのしくみ</span><span class="sxs-lookup"><span data-stu-id="48aa8-103">How Archiving works in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="48aa8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="48aa8-104">

<span> </span></span></span>

<span data-ttu-id="48aa8-105">_**最終更新日:** 2014-02-04_</span><span class="sxs-lookup"><span data-stu-id="48aa8-105">_**Topic Last Modified:** 2014-02-04_</span></span>

<span data-ttu-id="48aa8-106">Lync Server 2013 アーカイブは、コンプライアンスのニーズを満たすためのオプションを提供します。</span><span class="sxs-lookup"><span data-stu-id="48aa8-106">Lync Server 2013 Archiving provides options to help you meet your compliance needs.</span></span> <span data-ttu-id="48aa8-107">組織の要件を最も効果的に満たす方法で実装して維持するには、次のことを理解する必要があります。</span><span class="sxs-lookup"><span data-stu-id="48aa8-107">To implement and maintain it in a way that most effectively meets your organization’s requirements, you should understand:</span></span>

  - <span data-ttu-id="48aa8-108">どのような情報をアーカイブできますか。</span><span class="sxs-lookup"><span data-stu-id="48aa8-108">What information can be archived.</span></span>

  - <span data-ttu-id="48aa8-109">展開でアーカイブを有効または無効にする方法。</span><span class="sxs-lookup"><span data-stu-id="48aa8-109">How to enable and disable Archiving in your deployment.</span></span>

  - <span data-ttu-id="48aa8-110">アーカイブの実装方法を制御するために構成できるアーカイブオプション。</span><span class="sxs-lookup"><span data-stu-id="48aa8-110">The archiving options that you can configure to control how Archiving is implemented.</span></span>

<div>

## <a name="what-information-can-be-archived"></a><span data-ttu-id="48aa8-111">どのような情報をアーカイブできますか?</span><span class="sxs-lookup"><span data-stu-id="48aa8-111">What Information Can Be Archived?</span></span>

<span data-ttu-id="48aa8-112">次の種類のコンテンツをアーカイブできます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-112">The following types of content can be archived:</span></span>

  - <span data-ttu-id="48aa8-113">ピアツーピアのインスタント メッセージ</span><span class="sxs-lookup"><span data-stu-id="48aa8-113">Peer-to-peer instant messages</span></span>

  - <span data-ttu-id="48aa8-114">マルチパーティのインスタント メッセージである会議 (ミーティング)</span><span class="sxs-lookup"><span data-stu-id="48aa8-114">Conferences (meetings), which are multiparty instant messages</span></span>

  - <span data-ttu-id="48aa8-115">アップロードされたコンテンツ (配付資料など) およびイベント関連のコンテンツ (参加、退席、アップロード、共有、表示設定の変更など) を含む会議コンテンツ</span><span class="sxs-lookup"><span data-stu-id="48aa8-115">Conference content, including uploaded content (for example, handouts) and event-related content (for example, joining, leaving, uploading sharing, and changes in visibility)</span></span>

  - <span data-ttu-id="48aa8-116">会議中に共有するホワイトボードおよび投票</span><span class="sxs-lookup"><span data-stu-id="48aa8-116">Whiteboards and polls shared during a conference</span></span>

<span data-ttu-id="48aa8-117">次の種類のコンテンツはアーカイブされません。</span><span class="sxs-lookup"><span data-stu-id="48aa8-117">The following types of content are not archived:</span></span>

  - <span data-ttu-id="48aa8-118">ピアツーピアのファイル転送</span><span class="sxs-lookup"><span data-stu-id="48aa8-118">Peer-to-peer file transfers</span></span>

  - <span data-ttu-id="48aa8-119">ピアツーピアのインスタント メッセージおよび会議の音声ビデオ</span><span class="sxs-lookup"><span data-stu-id="48aa8-119">Audio/video for peer-to-peer instant messages and conferences</span></span>

  - <span data-ttu-id="48aa8-120">ピアツーピアのインスタント メッセージおよび会議のデスクトップ/アプリケーション共有</span><span class="sxs-lookup"><span data-stu-id="48aa8-120">Desktop and application sharing for peer-to-peer instant messages and conferences</span></span>

<span data-ttu-id="48aa8-121">Lync サーバーでは、常設チャットの会話もアーカイブされません。</span><span class="sxs-lookup"><span data-stu-id="48aa8-121">Lync Server also does not archive Persistent Chat conversations.</span></span> <span data-ttu-id="48aa8-122">常設チャットの会話をアーカイブするには、コンプライアンスサービスを有効にして構成する必要があります。これは、Microsoft Lync Server 2013、常設チャットサーバーで展開できるコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="48aa8-122">To archive Persistent Chat conversations, you must enable and configure the compliance service, which is a component that can be deployed with Microsoft Lync Server 2013, Persistent Chat Server.</span></span> <span data-ttu-id="48aa8-123">詳細については、計画ドキュメントの「 [Lync server 2013 での常設チャットサーバーの計画](lync-server-2013-planning-for-persistent-chat-server.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="48aa8-123">For details, see [Planning for Persistent Chat Server in Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md) in the Planning documentation.</span></span>

</div>

<div>

## <a name="how-do-i-start-using-archiving"></a><span data-ttu-id="48aa8-124">アーカイブを使い始めるにはどうすればよいですか?</span><span class="sxs-lookup"><span data-stu-id="48aa8-124">How Do I Start Using Archiving?</span></span>

<span data-ttu-id="48aa8-125">サーバーを展開すると、各フロントエンドサーバーに自動的にアーカイブがインストールされますが、構成しないとアーカイブは有効になりません。</span><span class="sxs-lookup"><span data-stu-id="48aa8-125">Archiving is automatically installed on each Front End Server when you deploy the server, but Archiving is not enabled until you configure it.</span></span> <span data-ttu-id="48aa8-126">この構成は、アーカイブの展開方法によって決まります。</span><span class="sxs-lookup"><span data-stu-id="48aa8-126">How you configure it is determined by how you deploy Archiving:</span></span>

  - <span data-ttu-id="48aa8-127">**Microsoft Exchange 統合を使用したアーカイブ。**</span><span class="sxs-lookup"><span data-stu-id="48aa8-127">**Archiving using Microsoft Exchange integration.**</span></span> <span data-ttu-id="48aa8-128">Exchange 2013 を使っているユーザーが In-Place 保留になっている場合は、Lync Server 2013 ストレージを Exchange ストレージに統合するためのオプションを選択できます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-128">If you have users who are homed on Exchange 2013 and their mailboxes have been put on In-Place Hold, you can select the option to integrate Lync Server 2013 storage with Exchange storage.</span></span> <span data-ttu-id="48aa8-129">[Microsoft Exchange 統合] オプションを選択した場合は、Exchange 2013 のポリシーと構成を使って、これらのユーザーの Lync Server 2013 データのアーカイブを管理します。</span><span class="sxs-lookup"><span data-stu-id="48aa8-129">If you choose the Microsoft Exchange integration option, you use Exchange 2013 policies and configurations to control the archiving of Lync Server 2013 data for those users.</span></span>

  - <span data-ttu-id="48aa8-130">**Lync Server アーカイブデータベースを使用したアーカイブ。**</span><span class="sxs-lookup"><span data-stu-id="48aa8-130">**Archiving using Lync Server Archiving databases.**</span></span> <span data-ttu-id="48aa8-131">Exchange 2013 を使用していないユーザー、または In-Place のメールボックスが保持されていないユーザーがいる場合、または展開のいずれかまたはすべてのユーザーに対して Microsoft Exchange 統合を使用しない場合は、SQL Server を使用して Lync Server アーカイブデータベースを展開して、ユーザーのアーカイブデータを保存することができます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-131">If you have users who are not homed on Exchange 2013 or who have not had their mailboxes put on In-Place Hold, or if you don’t want to use Microsoft Exchange integration for any or all users in your deployment, you can deploy Lync Server Archiving databases using SQL Server to store Archiving data for those users.</span></span> <span data-ttu-id="48aa8-132">この場合、Lync Server 2013 のアーカイブポリシーと構成によって、アーカイブが有効になっているかどうか、およびその実装方法が決定されます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-132">In this case, Lync Server 2013 Archiving policies and configurations determine whether Archiving is enabled and how it is implemented.</span></span> <span data-ttu-id="48aa8-133">Lync Server 2013 を使用するには、適切な SQL Server データベースをトポロジに追加し、トポロジを公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="48aa8-133">To use Lync Server 2013, you must add the appropriate SQL Server databases to your topology and publish the topology.</span></span>

<div>

## <a name="archiving-setup-when-using-microsoft-exchange-integration"></a><span data-ttu-id="48aa8-134">Microsoft Exchange との統合を使用するときのアーカイブセットアップ</span><span class="sxs-lookup"><span data-stu-id="48aa8-134">Archiving Setup When Using Microsoft Exchange Integration</span></span>

<span data-ttu-id="48aa8-135">ユーザーが Exchange 2013 を使用していて、そのメールボックスが In-Place 保持されている場合は、 **Microsoft exchange 統合** オプション (このセクションの後半で説明します) を選択して、これらのユーザーに対して lync server 2013 をアーカイブし、次の項目を管理するために Exchange In-Place のポリシーと設定、および lync server の構成を指定して</span><span class="sxs-lookup"><span data-stu-id="48aa8-135">If your users are homed on Exchange 2013 and their mailboxes have been put on In-Place Hold, you can choose the **Microsoft Exchange integration** option (as described later in this section) to archive Lync Server 2013 for those users, and then you control archiving for those users by specifying Exchange In-Place Hold policies and settings, as well as Lync Server configurations to control the following:</span></span>

  - <span data-ttu-id="48aa8-136">IM、会議、またはその両方をアーカイブするかどうか。</span><span class="sxs-lookup"><span data-stu-id="48aa8-136">Whether to archive IM, conferencing, or both.</span></span>

  - <span data-ttu-id="48aa8-137">Lync Server の展開に対して、クリティカルモードを実装するかどうか。</span><span class="sxs-lookup"><span data-stu-id="48aa8-137">Whether to implement critical mode for your Lync Server deployment.</span></span>

  - <span data-ttu-id="48aa8-138">[Microsoft Exchange 統合] オプションを選択して、アーカイブデータの保存に Exchange 2013 を使用する。</span><span class="sxs-lookup"><span data-stu-id="48aa8-138">Selection of the Microsoft Exchange integration option to use Exchange 2013 for storage of archived data.</span></span>

<span data-ttu-id="48aa8-139">これらの Lync Server 2013 アーカイブ構成オプションについては、このセクションの後半で説明します。</span><span class="sxs-lookup"><span data-stu-id="48aa8-139">These Lync Server 2013 Archiving configuration options are described later in this section.</span></span> <span data-ttu-id="48aa8-140">アーカイブをサポートするポリシーと設定を保持するように Exchange In-Place を構成する方法については、「Exchange 2013 の製品ドキュメント」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="48aa8-140">For information about how to configure Exchange In-Place Hold policies and settings to support archiving, see the Exchange 2013 product documentation.</span></span>

</div>

<div>

## <a name="archiving-setup-when-using-lync-server-archiving-database-storage"></a><span data-ttu-id="48aa8-141">Lync Server のアーカイブデータベースストレージを使用するときのアーカイブのセットアップ</span><span class="sxs-lookup"><span data-stu-id="48aa8-141">Archiving Setup When Using Lync Server Archiving Database Storage</span></span>

<span data-ttu-id="48aa8-142">(SQL Server データベースを使用して) Lync Server アーカイブデータベースを使用して、展開されているユーザーのデータをアーカイブする場合は、それらのユーザーに対してアーカイブが有効になっているかどうかを制御するように Lync Server のアーカイブポリシーを構成できます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-142">If you want to use Lync Server Archiving databases (using SQL Server databases) to archive data for any users in your deployment, you can configure Lync Server Archiving policies to control whether Archiving is enabled for those users.</span></span> <span data-ttu-id="48aa8-143">各アーカイブポリシーでは、次のいずれかまたは両方のアーカイブを有効または無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-143">In each Archiving policy, you can enable or disable Archiving for either or both of the following:</span></span>

  - <span data-ttu-id="48aa8-144">内部通信</span><span class="sxs-lookup"><span data-stu-id="48aa8-144">Internal communications</span></span>

  - <span data-ttu-id="48aa8-145">外部通信</span><span class="sxs-lookup"><span data-stu-id="48aa8-145">External communications</span></span>

<span data-ttu-id="48aa8-146">既定では、すべての Lync Server アーカイブポリシーで、内部通信または外部通信に対してアーカイブが有効になっていません。</span><span class="sxs-lookup"><span data-stu-id="48aa8-146">By default, archiving is not enabled for internal communications or external communications in any Lync Server Archiving policy.</span></span> <span data-ttu-id="48aa8-147">Lync Server 2013 コントロールパネルを使用して通信を有効または無効にするか、Lync Server 2013 Management Shell でコマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="48aa8-147">You enable and disable communications using Lync Server 2013 Control Panel or using cmdlets in the Lync Server 2013 Management Shell.</span></span>

<span data-ttu-id="48aa8-148">Lync Server 2013 アーカイブポリシーには、次のものが含まれます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-148">Lync Server 2013 Archiving policies include the following:</span></span>

  - <span data-ttu-id="48aa8-149">**グローバルアーカイブポリシー**。</span><span class="sxs-lookup"><span data-stu-id="48aa8-149">**Global Archiving policy**.</span></span> <span data-ttu-id="48aa8-150">これは既定のアーカイブポリシーであり、展開全体に適用されます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-150">This is the default Archiving policy and applies to your entire deployment.</span></span> <span data-ttu-id="48aa8-151">これは Lync Server 2013 を展開したときに作成され、既定では、内部と外部の両方の通信のアーカイブが無効になります。</span><span class="sxs-lookup"><span data-stu-id="48aa8-151">It is created when you deploy Lync Server 2013 and, by default, disables Archiving for both internal and external communications.</span></span> <span data-ttu-id="48aa8-152">このポリシーは削除できません。</span><span class="sxs-lookup"><span data-stu-id="48aa8-152">You cannot delete this policy.</span></span> <span data-ttu-id="48aa8-153">[削除] オプションを選ぶと、グローバルポリシーは既定の設定にリセットされます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-153">If you choose the delete option, the global policy is reset to the default settings.</span></span>

  - <span data-ttu-id="48aa8-154">**サイトのアーカイブポリシー**。</span><span class="sxs-lookup"><span data-stu-id="48aa8-154">**Site Archiving policy**.</span></span> <span data-ttu-id="48aa8-155">必要に応じて、サイトのサイトレベルのアーカイブポリシーを作成して構成することによって、1つ以上の特定のサイトのアーカイブを有効または無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-155">Optionally, you can enable or disable Archiving for one or more specific sites by creating and configuring a site-level Archiving policy for the site.</span></span> <span data-ttu-id="48aa8-156">サイトレベルのアーカイブポリシーを作成する場合、既定ではアーカイブは有効になっていません。</span><span class="sxs-lookup"><span data-stu-id="48aa8-156">When you create a site-level Archiving policy, by default, archiving is not enabled.</span></span> <span data-ttu-id="48aa8-157">作成したサイトレベルのアーカイブポリシーは、削除することができます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-157">You can delete any site-level Archiving policy that you create.</span></span> <span data-ttu-id="48aa8-158">サイトレベルのアーカイブポリシーは、ポリシーで指定したサイトに対してのみ、グローバルポリシーを上書きします。</span><span class="sxs-lookup"><span data-stu-id="48aa8-158">A site-level Archiving policy overrides the global policy, but only for the site specified in the policy.</span></span> <span data-ttu-id="48aa8-159">たとえば、グローバルポリシーで内部および外部通信のアーカイブを有効にし、外部通信のアーカイブを無効にするサイトポリシーを作成すると、そのサイトの内部通信のみがアーカイブされます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-159">For example, if you enable Archiving for internal and external communications in your global policy and create a site policy in which you disable Archiving for external communications, only internal communications would be archived for that site.</span></span>

  - <span data-ttu-id="48aa8-160">**ユーザーアーカイブポリシー**。</span><span class="sxs-lookup"><span data-stu-id="48aa8-160">**User Archiving policy**.</span></span> <span data-ttu-id="48aa8-161">必要に応じて、指定したユーザーとユーザーグループに対して、ユーザーレベルのアーカイブポリシーを作成、構成、適用することによって、1つ以上の特定のユーザーとユーザーグループのアーカイブを有効または無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-161">Optionally, you can enable or disable Archiving for one or more specific users and group of users by creating, configuring, and applying a user-level Archiving policy for the specified users and user groups.</span></span> <span data-ttu-id="48aa8-162">既定では、ユーザーレベルのアーカイブポリシーを作成すると、アーカイブは有効になりません。</span><span class="sxs-lookup"><span data-stu-id="48aa8-162">When you create a user-level Archiving policy, by default, archiving is not enabled.</span></span> <span data-ttu-id="48aa8-163">作成したユーザーレベルのアーカイブポリシーは削除できます。また、アーカイブポリシーを適用するユーザーやユーザーのグループを変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-163">You can delete any user-level Archiving policy that you create, and you can change which users and group of users the Archiving policy applies to.</span></span> <span data-ttu-id="48aa8-164">ユーザーレベルのアーカイブポリシーは、グローバルポリシーやサイトポリシーよりも優先されますが、ポリシーが適用されているユーザーとユーザーグループについてのみ無効になります。</span><span class="sxs-lookup"><span data-stu-id="48aa8-164">A user-level Archiving policy overrides the global policy and any site policies, but only for the users and user groups to whom the policy is applied.</span></span> <span data-ttu-id="48aa8-165">たとえば、グローバルポリシーで内部および外部通信のアーカイブを無効にした場合、内部と外部の通信のアーカイブを有効にするサイトレベルのポリシーを作成し、外部通信のアーカイブを無効にするユーザーレベルのポリシーを作成すると、ユーザーレベルのポリシーを適用したユーザーに対して、外部と内部の両方の通信のために通信がアーカイブされます。内部通信のみがアーカイブされます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-165">For example, if you disable Archiving for internal and external communications in your global policy, create a site-level policy in which you enable Archiving for internal and external communications, and then create a user-level policy in which you disable Archiving for external communications, the communications would be archived for both external and internal communications for all site users except that, for the users to whom you apply the user-level policy, only internal communications would be archived.</span></span>

<span data-ttu-id="48aa8-166">アーカイブを展開するときに最初のアーカイブポリシーを設定する方法について詳しくは、「展開ドキュメントの [Lync Server 2013 でのアーカイブポリシーの構成と割り当て](lync-server-2013-configuring-and-assigning-archiving-policies.md) 」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="48aa8-166">For details about how to set up initial Archiving policies when you deploy Archiving, see [Configuring and assigning Archiving policies in Lync Server 2013](lync-server-2013-configuring-and-assigning-archiving-policies.md) in the Deployment documentation.</span></span> <span data-ttu-id="48aa8-167">展開後の通信を有効または無効にするためにアーカイブポリシーを使用する方法について詳しくは、「運用ドキュメントの [Lync Server 2013 での社内および社外の通信のアーカイブを管理](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md) する」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="48aa8-167">For details about using Archiving policies to enable and disable communications after deployment, see [Managing the Archiving of internal and external communications in Lync Server 2013](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md) in the Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="48aa8-168">Lync Server 2013 アーカイブデータベースの両方を実装していて、Microsoft Exchange 統合を有効にしている場合、Exchange 2013 のポリシーは Lync Server のアーカイブポリシーを上書きします。ただし、exchange 2013 を使用していて、メールボックスが In-Place 保留になっているユーザーにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-168">If you implement both Lync Server 2013 Archiving databases and enable Microsoft Exchange integration, Exchange 2013 policies override Lync Server Archiving policies, but only for users who are homed on Exchange 2013 and have had their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="48aa8-169">Lync アーカイブは、Microsoft Exchange In-Place ホールドポリシーのみに依存します。</span><span class="sxs-lookup"><span data-stu-id="48aa8-169">Lync Archiving depends on Microsoft Exchange In-Place Hold policy only.</span></span>



</div>

</div>

<div>

## <a name="what-options-do-i-have-for-configuring-archiving"></a><span data-ttu-id="48aa8-170">アーカイブを構成するには、どのようなオプションがありますか?</span><span class="sxs-lookup"><span data-stu-id="48aa8-170">What Options Do I Have for Configuring Archiving?</span></span>

<span data-ttu-id="48aa8-171">ポリシーを使用してアーカイブを有効または無効にすることに加えて、展開全体に対して構成できるその他のアーカイブオプションもあります。また、必要に応じて、特定のサイトとプールについて構成することもできます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-171">In addition to using policies and to enable and disable Archiving, you have other Archiving options that can be configure for your entire deployment and, optionally, for specific sites and pools.</span></span> <span data-ttu-id="48aa8-172">ほとんどのアーカイブオプションは、Lync Server 2013 コントロールパネルで利用できる1つまたは複数のアーカイブ構成を使用して制御できますが、Lync Server 2013 管理シェルを使用して構成できる別のオプションもあります。</span><span class="sxs-lookup"><span data-stu-id="48aa8-172">You control most Archiving options by using one or more Archiving configurations, which are available in Lync Server 2013 Control Panel, but also have another option that is only available for configuration using Lync Server 2013 Management Shell.</span></span>

<div>

## <a name="archiving-configuration-options-available-in-lync-server-2013-control-panel"></a><span data-ttu-id="48aa8-173">Lync Server 2013 コントロールパネルで使用可能なアーカイブ構成オプション</span><span class="sxs-lookup"><span data-stu-id="48aa8-173">Archiving Configuration Options Available in Lync Server 2013 Control Panel</span></span>

<span data-ttu-id="48aa8-174">各アーカイブ構成では、次のオプションが用意されています。</span><span class="sxs-lookup"><span data-stu-id="48aa8-174">Each archiving configuration provides the following options:</span></span>

<span data-ttu-id="48aa8-175">グローバルレベルの構成は、アーカイブを展開するときに自動的に作成されますが、構成することはできますが、削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="48aa8-175">The global-level configuration is created automatically when you deploy archiving and can be configured, but not deleted.</span></span> <span data-ttu-id="48aa8-176">グローバル構成を削除するオプションを選択すると、設定は既定値にリセットされます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-176">If you select the option to delete the global configuration, the settings are reset to the default values.</span></span> <span data-ttu-id="48aa8-177">グローバル構成と共に、アーカイブの設定を制御する、複数のサイトとプールの構成を作成できます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-177">You can create multiple site and pool configurations that, together with the global configuration, control archiving settings.</span></span> <span data-ttu-id="48aa8-178">グローバル構成、およびサイトとプールの各構成では、次のオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="48aa8-178">For the global configuration and each site and pool configuration, you have the following options:</span></span>

  - <span data-ttu-id="48aa8-179">アーカイブを無効にしたり、インスタントメッセージング (IM) のみのアーカイブを有効にしたり、IM と会議の両方のアーカイブを有効にしたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-179">Disable archiving, enable archiving only for instant messaging (IM), or enable archiving of both IM and conferencing.</span></span>

  - <span data-ttu-id="48aa8-180">Lync Server に障害が発生したときに IM と会議セッションをブロックするように、重要なモードを構成します。</span><span class="sxs-lookup"><span data-stu-id="48aa8-180">Configure critical mode to block IM and conferencing sessions in the event of a Lync Server failure.</span></span> <span data-ttu-id="48aa8-181">エラーには、次のようなものがあります。</span><span class="sxs-lookup"><span data-stu-id="48aa8-181">Failures include the following:</span></span>
    
      - <span data-ttu-id="48aa8-182">**IM**。</span><span class="sxs-lookup"><span data-stu-id="48aa8-182">**IM**.</span></span> <span data-ttu-id="48aa8-183">Lync Server ストレージサービスに問題があります。</span><span class="sxs-lookup"><span data-stu-id="48aa8-183">A problem with the Lync Server storage service.</span></span> <span data-ttu-id="48aa8-184">この場合、アーカイブが有効になっているユーザーでは IM がブロックされます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-184">In this case, IM is blocked for users who are enabled for Archiving.</span></span>
    
      - <span data-ttu-id="48aa8-185">[**電話会議**]。</span><span class="sxs-lookup"><span data-stu-id="48aa8-185">**Conferencing**.</span></span> <span data-ttu-id="48aa8-186">エラーの原因として、ファイル共有が利用できないか、ストレージサービスに問題がある可能性があります。</span><span class="sxs-lookup"><span data-stu-id="48aa8-186">A failure could be an unavailable file share or a problem with the storage service.</span></span> <span data-ttu-id="48aa8-187">この場合、障害発生時にプール内でホストされているアクティブな会議がすべて制限モードに切り替えられ、新しい会議をアクティブにすることはできません。</span><span class="sxs-lookup"><span data-stu-id="48aa8-187">In this case, all active conferences hosted in the pool at the time of failure are switched to restricted mode and new conferences cannot be activated.</span></span>
    
    <span data-ttu-id="48aa8-188">障害から回復した後、IM および会議は自動的に回復します。</span><span class="sxs-lookup"><span data-stu-id="48aa8-188">Both IM and conferencing automatically recover after the failures are corrected.</span></span>

  - <span data-ttu-id="48aa8-189">Lync Server 2013 アーカイブデータの保存用に別の SQL Server データベースを設定するのではなく、Microsoft Exchange Server 2013 統合を使用して、アーカイブデータのストレージに Exchange 2013 を使用するように指定します。</span><span class="sxs-lookup"><span data-stu-id="48aa8-189">Specify the use of Microsoft Exchange Server 2013 integration to use Exchange 2013 for storage of archived data, instead of setting up separate SQL Server databases for storage of Lync Server 2013 archiving data.</span></span>

  - <span data-ttu-id="48aa8-190">アーカイブデータの消去オプションを構成します。</span><span class="sxs-lookup"><span data-stu-id="48aa8-190">Configure purging options for archived data.</span></span> <span data-ttu-id="48aa8-191">これには、アーカイブデータを消去するタイミングの指定が含まれます。これは、次のいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="48aa8-191">This includes specifying when to purge archived data, which can be either of the following:</span></span>
    
      - <span data-ttu-id="48aa8-192">指定した日数が経過した後</span><span class="sxs-lookup"><span data-stu-id="48aa8-192">After a specific number of days that you specify</span></span>
    
      - <span data-ttu-id="48aa8-193">アーカイブデータがエクスポートされた後 (Microsoft Exchange との統合を有効にした場合は、Exchange にアップロードされたデータが含まれます)。</span><span class="sxs-lookup"><span data-stu-id="48aa8-193">After the archiving data has been exported (which includes data that has been uploaded to Exchange, if you enable Microsoft Exchange integration).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="48aa8-194">Microsoft Exchange の統合を有効にした場合、Exchange 2013 上に置かれているユーザーと、そのユーザーのメールボックス In-Place 保留になっているユーザーは Exchange によって管理されます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-194">If you enable Microsoft Exchange integration, purging for users homed on Exchange 2013 and with their mailboxes put on In-Place Hold is controlled by Exchange.</span></span> <span data-ttu-id="48aa8-195">唯一の制約は、Lync Server ファイル共有に保存されている会議ファイルです。</span><span class="sxs-lookup"><span data-stu-id="48aa8-195">The only qualification is for conferencing files, which are stored on the Lync Server file share.</span></span> <span data-ttu-id="48aa8-196">これらのファイルは、アーカイブ データがエクスポートされた後でデータを削除するオプションを選択した場合はファイルがエクスポートされた後 (Exchange にアップロードされた後)、保持する最大日数を指定した場合は指定した最大日数経過後にのみファイル共有から削除されます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-196">These files are purged from the file share only after the files have been exported (uploaded to Exchange), if you select the option to purge data after the archiving data has been exported, or after the specified maximum number of days, if you specify a maximum number of days for retention.</span></span>

    
    </div>

<span data-ttu-id="48aa8-197">既定では、アーカイブオプションは有効になっていません。</span><span class="sxs-lookup"><span data-stu-id="48aa8-197">By default, no archiving options are enabled.</span></span> <span data-ttu-id="48aa8-198">Lync Server 2013 コントロールパネルを使用して、アーカイブ構成を管理することができます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-198">You can manage Archiving configurations using Lync Server 2013 Control Panel.</span></span>

<span data-ttu-id="48aa8-199">次のアーカイブ構成を指定できます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-199">You can specify the following Archiving configurations:</span></span>

  - <span data-ttu-id="48aa8-200">**グローバルアーカイブ構成**。</span><span class="sxs-lookup"><span data-stu-id="48aa8-200">**Global Archiving configuration**.</span></span> <span data-ttu-id="48aa8-201">これは既定のアーカイブ構成であり、展開全体に適用されます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-201">This is the default Archiving configuration and applies to your entire deployment.</span></span> <span data-ttu-id="48aa8-202">これは Lync Server 2013 を展開したときに作成され、既定では、アーカイブ機能は有効になりません。</span><span class="sxs-lookup"><span data-stu-id="48aa8-202">It is created when you deploy Lync Server 2013 and, by default, does not enable archiving functionality.</span></span> <span data-ttu-id="48aa8-203">グローバル構成を変更することはできますが、削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="48aa8-203">You can modify the global configuration, but you cannot delete it.</span></span> <span data-ttu-id="48aa8-204">構成の [削除] オプションを選ぶと、グローバル構成が既定の設定にリセットされます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-204">If you choose the delete option for the configuration, the global configuration is reset to the default settings.</span></span>

  - <span data-ttu-id="48aa8-205">**サイトのアーカイブ構成**。</span><span class="sxs-lookup"><span data-stu-id="48aa8-205">**Site Archiving configuration**.</span></span> <span data-ttu-id="48aa8-206">必要に応じて、個々のサイトのサイトレベルのアーカイブ構成を作成して構成することによって、1つ以上の特定のサイトのアーカイブを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-206">Optionally, you can configure Archiving for one or more specific sites by creating and configuring a site-level Archiving configuration for an individual site.</span></span> <span data-ttu-id="48aa8-207">サイトレベルのアーカイブ構成は、作成した場合にのみ存在します。</span><span class="sxs-lookup"><span data-stu-id="48aa8-207">A site-level Archiving configuration exists only if you create it.</span></span> <span data-ttu-id="48aa8-208">サイトレベルのアーカイブ構成は、変更または削除することができます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-208">You can modify or delete any site-level Archiving configuration.</span></span> <span data-ttu-id="48aa8-209">サイトレベルのアーカイブ構成では、サイトレベルの構成で指定したサイトに対してのみ、グローバル構成が上書きされます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-209">A site-level Archiving configuration overrides the global configuration, but only for the site specified in the site-level configuration.</span></span> <span data-ttu-id="48aa8-210">たとえば、グローバル構成で IM のみのアーカイブを有効にし、IM と会議の両方のアーカイブを有効にするサイト構成を作成した場合、会議は組織の残りの部分ではなく、サイトに対してのみアーカイブされます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-210">For example, if you enable Archiving for only IM in your global configuration and create a site configuration in which you enable Archiving for both IM and conferencing, conferencing would only be archived for the site, not for the remainder of your organization.</span></span>

  - <span data-ttu-id="48aa8-211">**プールのアーカイブ構成**。</span><span class="sxs-lookup"><span data-stu-id="48aa8-211">**Pool Archiving configuration**.</span></span> <span data-ttu-id="48aa8-212">必要に応じて、個々のプールのプールレベルの構成を作成して構成することによって、1つ以上の特定のプールのアーカイブ設定を指定できます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-212">Optionally, you can specify Archiving settings for one or more specific pools by creating and configuring a pool-level configuration for the individual pool.</span></span> <span data-ttu-id="48aa8-213">プールレベルのアーカイブ構成は、作成した場合にのみ存在します。</span><span class="sxs-lookup"><span data-stu-id="48aa8-213">A pool-level Archiving configuration exists only if you create it.</span></span> <span data-ttu-id="48aa8-214">プールレベルのアーカイブ構成を変更したり、削除したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-214">You can modify and delete any pool-level Archiving configuration.</span></span> <span data-ttu-id="48aa8-215">プールレベルのアーカイブ構成は、グローバル構成と、作成した可能性のあるサイトアーカイブ構成よりも優先されます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-215">A pool-level Archiving configuration overrides the global configuration and any site archiving configuration you may have created.</span></span> <span data-ttu-id="48aa8-216">たとえば、グローバル構成で IM のみのアーカイブを有効にする場合は、サイトの IM と会議の両方のアーカイブを有効にするサイトレベルの構成を作成し、IM のみのアーカイブを有効にするプールレベルの構成を作成します。この場合、プールレベルの構成で指定したプールを使用しているユーザーを除き、そのサイトのすべてのユーザーの IM と会議の両方の通信がアーカイブされます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-216">For example, if you enable Archiving for only IM in your global configuration, create a site-level configuration in which you enable Archiving for both IM and conferencing for the site, and then create a pool-level configuration in which you enable Archiving only for IM, the communications would be archived for both IM and conferencing for all users of the site except the users homed in the pool specified in the pool-level configuration.</span></span> <span data-ttu-id="48aa8-217">組織内の他のすべてのユーザーについては、アーカイブは IM に対してのみ有効になります。</span><span class="sxs-lookup"><span data-stu-id="48aa8-217">For all other users in your organization, Archiving would be enabled only for IM.</span></span>

<span data-ttu-id="48aa8-218">アーカイブを展開するときに最初のアーカイブ構成を設定する方法の詳細については、展開ドキュメントの「 [Lync Server 2013 でアーカイブオプションを構成](lync-server-2013-configuring-archiving-options.md) する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="48aa8-218">For details about how to set up initial Archiving configurations when you deploy Archiving, see [Configuring Archiving options in Lync Server 2013](lync-server-2013-configuring-archiving-options.md) in the Deployment documentation.</span></span> <span data-ttu-id="48aa8-219">展開後の通信を有効または無効にするアーカイブポリシーの使用について詳しくは、「 [Lync Server 2013 でアーカイブ構成オプションを管理](lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md) する」を参照してください。このドキュメントでは、組織、サイト、プールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="48aa8-219">For details about using Archiving policies to enable and disable communications after deployment, see [Managing Archiving configuration options in Lync Server 2013 for your organization, sites, and pools](lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md) in the Operations documentation.</span></span>

</div>

<div>

## <a name="archiving-options-available-only-in-windows-powershell"></a><span data-ttu-id="48aa8-220">Windows PowerShell でのみ使用できるアーカイブオプション</span><span class="sxs-lookup"><span data-stu-id="48aa8-220">Archiving Options Available Only in Windows PowerShell</span></span>

<span data-ttu-id="48aa8-221">Lync Server 2013 管理シェルを使用すると、コマンドレットを使用して、Lync Server 2013 コントロールパネルで利用できないオプションを実装できます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-221">Using Lync Server 2013 Management Shell, you can use cmdlets to implement options that are not available in Lync Server 2013 Control Panel.</span></span> <span data-ttu-id="48aa8-222">次のようなオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="48aa8-222">These options include the following:</span></span>

  - <span data-ttu-id="48aa8-223">**重複するメッセージをアーカイブ** します。</span><span class="sxs-lookup"><span data-stu-id="48aa8-223">**Archive duplicate messages**.</span></span> <span data-ttu-id="48aa8-224">詳細については、操作のドキュメントの「 [New-CsArchivingConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsArchivingConfiguration) and [CsArchivingConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsArchivingConfiguration) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="48aa8-224">For details, see [New-CsArchivingConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsArchivingConfiguration) and [Set-CsArchivingConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsArchivingConfiguration) in the Operations documentation.</span></span>

  - <span data-ttu-id="48aa8-225">**アーカイブデータをエクスポート** します。</span><span class="sxs-lookup"><span data-stu-id="48aa8-225">**Export archived data**.</span></span> <span data-ttu-id="48aa8-226">詳細については、「[エクスポート-CsArchivingData](https://docs.microsoft.com/powershell/module/skype/Export-CsArchivingData) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="48aa8-226">For details, see [Export-CsArchivingData](https://docs.microsoft.com/powershell/module/skype/Export-CsArchivingData)</span></span>

</div>

</div>

</div>

<div>

## <a name="how-do-i-access-archived-data"></a><span data-ttu-id="48aa8-227">アーカイブデータにアクセスする方法を教えてください。</span><span class="sxs-lookup"><span data-stu-id="48aa8-227">How Do I Access Archived Data?</span></span>

<span data-ttu-id="48aa8-228">アーカイブされたデータへのアクセス方法は、データの保管場所に応じて異なります。</span><span class="sxs-lookup"><span data-stu-id="48aa8-228">Access to archived data is dependent on where the data is stored:</span></span>

  - <span data-ttu-id="48aa8-229">**Microsoft Exchange ストレージ**。</span><span class="sxs-lookup"><span data-stu-id="48aa8-229">**Microsoft Exchange storage**.</span></span> <span data-ttu-id="48aa8-230">[Exchange 統合] オプションを選ぶと、Lync Server は exchange 2013 を使用しているすべてのユーザーの Exchange 2013 ストアのアーカイブコンテンツを保存します。また、ユーザーのメールボックスが In-Place 保留になっています。</span><span class="sxs-lookup"><span data-stu-id="48aa8-230">If you choose the Exchange integration option, Lync Server deposits the archiving content in the Exchange 2013 store for all users who are homed on Exchange 2013, and who have had their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="48aa8-231">アーカイブされたデータは [ユーザーメールボックスの回復可能なアイテム] フォルダーに格納されます。これは通常、ユーザーには見えません。また、Exchange の **検出管理** 役割を持つユーザーのみが検索できます。</span><span class="sxs-lookup"><span data-stu-id="48aa8-231">Archived data is stored in user mailboxes Recoverable items folder, which is generally invisible to users, and can only be searched by users with an Exchange **Discovery Management** role.</span></span> <span data-ttu-id="48aa8-232">展開されている場合、SharePoint と共にフェデレーション検索および検出が有効になります。</span><span class="sxs-lookup"><span data-stu-id="48aa8-232">Exchange enables federated search and discovery, along with SharePoint, if it is deployed.</span></span> <span data-ttu-id="48aa8-233">Exchange に保存されているデータの記憶域、保持、および検出の詳細については、「Exchange 2013 と SharePoint に関するドキュメント」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="48aa8-233">For more details about storage, retention, and discovery of data stored in Exchange, see the Exchange 2013 and SharePoint documentation.</span></span>

  - <span data-ttu-id="48aa8-234">**Lync Server ストレージ**。</span><span class="sxs-lookup"><span data-stu-id="48aa8-234">**Lync Server storage**.</span></span> <span data-ttu-id="48aa8-235">Lync server 2013 アーカイブデータベースで Lync Server のデータを保存するように設定した場合、Lync server は、Exchange 2013 を使用していないユーザーのために、lync Server のアーカイブデータベース (SQL Server データベース) のアーカイブコンテンツをデポジットし、メールボックスが In-Place 保持されていないユーザーを対象にします。</span><span class="sxs-lookup"><span data-stu-id="48aa8-235">If you set up Lync Server 2013 Archiving databases for storage of Lync Server data, Lync Server deposits archiving content in the Lync Server Archiving databases (SQL Server databases) for any users not homed on Exchange 2013, and who have not had their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="48aa8-236">This data is not searchable, but it can be exported to formats that are searchable using other tools.</span><span class="sxs-lookup"><span data-stu-id="48aa8-236">This data is not searchable, but it can be exported to formats that are searchable using other tools.</span></span> <span data-ttu-id="48aa8-237">アーカイブデータベースに格納されているデータのエクスポートの詳細については、「運用ドキュメントの「 [Lync Server 2013 からのアーカイブデータのエクスポート](lync-server-2013-exporting-archived-data.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="48aa8-237">For details about exporting data stored in Archiving databases, see [Exporting archived data from Lync Server 2013](lync-server-2013-exporting-archived-data.md) in the Operations documentation.</span></span>

<span data-ttu-id="48aa8-238">Lync Server 2013 と Exchange 2013 の連携のしくみの詳細については、サポートドキュメントで「 [Exchange server および Lync server 2013 の SharePoint 統合のサポート](lync-server-2013-exchange-and-sharepoint-integration-support.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="48aa8-238">For more details about how Lync Server 2013 and Exchange 2013 work together, see [Exchange Server and SharePoint integration support in Lync Server 2013](lync-server-2013-exchange-and-sharepoint-integration-support.md) in the Supportability documentation.</span></span>

<span data-ttu-id="48aa8-239"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="48aa8-239"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

