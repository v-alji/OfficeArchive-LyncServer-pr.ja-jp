---
title: 'Lync Server 2013: 常設チャット データベースのスキーマ'
description: 'Lync Server 2013: 常設チャットデータベーススキーマ。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Persistent Chat database schema
ms:assetid: 58d7d94f-42f5-4c3e-8fe5-901fbe92152e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558653(v=OCS.15)
ms:contentKeyID: 48184228
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 66151201f65310cc8e6d3f2251be4f86ce2be15d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398739"
---
# <a name="persistent-chat-database-schema-in-lync-server-2013"></a><span data-ttu-id="9130e-103">Lync Server 2013 の常設チャット データベースのスキーマ</span><span class="sxs-lookup"><span data-stu-id="9130e-103">Persistent Chat database schema in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9130e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9130e-104">

<span> </span></span></span>

<span data-ttu-id="9130e-105">_**最終更新日:** 2012-09-18_</span><span class="sxs-lookup"><span data-stu-id="9130e-105">_**Topic Last Modified:** 2012-09-18_</span></span>

<span data-ttu-id="9130e-106">これにより、Lync Server 2013 通信ソフトウェアの常設チャットデータベースのスキーマがドキュメントに記載されます。</span><span class="sxs-lookup"><span data-stu-id="9130e-106">This documents the schema of the Persistent Chat database in Lync Server 2013 communications software.</span></span>

<span data-ttu-id="9130e-107">常設チャットデータベースは、Lync Server 2013 バックエンドサーバーのロール PersistentChatStore (行うデータベースに対応) と **PersistentChatComplianceStore** ( **PersistentChatStore** ccomp データベースに対応) に対応するデータベースを参照します。</span><span class="sxs-lookup"><span data-stu-id="9130e-107">The Persistent Chat database refers to the database corresponding to the Lync Server 2013 Back End Server roles **PersistentChatStore** (corresponding to the mgc database) and **PersistentChatComplianceStore** (corresponding to the mgccomp database).</span></span> <span data-ttu-id="9130e-108">このスキーマを公開することは、お客様がクエリを作成して、チャットの利用状況、アクティブな会議室、トップ投稿などに関する有用なレポートを作成できるようにすることを目的としています。</span><span class="sxs-lookup"><span data-stu-id="9130e-108">The goal of publishing this schema is to enable you to build queries and gain some insights into building useful reporting around chat usage, active rooms, top posters, and so on.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="9130e-109">このスキーマを進化させる権利を留保します。</span><span class="sxs-lookup"><span data-stu-id="9130e-109">We reserve the right to evolve this schema.</span></span> <span data-ttu-id="9130e-110">Microsoft は、この公開されたスキーマとの完全な下位互換性を維持する保証を行っていません。</span><span class="sxs-lookup"><span data-stu-id="9130e-110">Microsoft does not make any guarantees to maintain full backward compatibility with this published schema.</span></span>



</div>

<span data-ttu-id="9130e-111">以下のベストプラクティスに従ってください。</span><span class="sxs-lookup"><span data-stu-id="9130e-111">Follow these best practices:</span></span>

  - <span data-ttu-id="9130e-112">\*列リストのサイズが大きくなる可能性があるため、SELECT//はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="9130e-112">No SELECT\* // is supported because the column list can grow.</span></span>

  - <span data-ttu-id="9130e-113">ユーザーが生成したスキーマの変更はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="9130e-113">No user-generated schema modifications are supported.</span></span>

  - <span data-ttu-id="9130e-114">書き込み操作はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="9130e-114">No write operations are supported.</span></span>

  - <span data-ttu-id="9130e-115">Representatively サイズのデータベースで作成したクエリをテストして、ニーズに合わせてクエリが確実に実行されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9130e-115">Test any queries that you build on representatively-sized databases to be sure that the queries can perform at a level to meet your needs.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="9130e-116">このセクション中</span><span class="sxs-lookup"><span data-stu-id="9130e-116">In This Section</span></span>

  - [<span data-ttu-id="9130e-117">Lync Server 2013 の常設チャット サーバーのテーブルのリスト</span><span class="sxs-lookup"><span data-stu-id="9130e-117">List of Persistent Chat Server tables in Lync Server 2013</span></span>](lync-server-2013-list-of-persistent-chat-server-tables.md)

  - [<span data-ttu-id="9130e-118">Lync Server 2013 の常設チャット サーバーのコンプライアンス テーブルのリスト</span><span class="sxs-lookup"><span data-stu-id="9130e-118">List of Persistent Chat Server compliance tables in Lync Server 2013</span></span>](lync-server-2013-list-of-persistent-chat-server-compliance-tables.md)

  - [<span data-ttu-id="9130e-119">Lync Server 2013 の常設チャット サーバー テーブルの詳細</span><span class="sxs-lookup"><span data-stu-id="9130e-119">Persistent Chat Server table details in Lync Server 2013</span></span>](lync-server-2013-persistent-chat-server-table-details.md)

  - [<span data-ttu-id="9130e-120">Lync Server 2013 の常設チャット データベースのクエリのサンプル</span><span class="sxs-lookup"><span data-stu-id="9130e-120">Sample Persistent Chat database queries for Lync Server 2013</span></span>](lync-server-2013-sample-persistent-chat-database-queries.md)

<span data-ttu-id="9130e-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9130e-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

