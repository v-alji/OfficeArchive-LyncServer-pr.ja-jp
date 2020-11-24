---
title: アーカイブ サーバーの関連付けの削除
description: アーカイブサーバーの関連付けを削除します。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove the Archiving server association
ms:assetid: dabac157-71ee-4afe-b0b6-4a083d165ffb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721903(v=OCS.15)
ms:contentKeyID: 49733837
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0f6c34e49b0217a8318a83752b3878a7625e5d58
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400083"
---
# <a name="remove-the-archiving-server-association"></a><span data-ttu-id="8a92f-103">アーカイブ サーバーの関連付けの削除</span><span class="sxs-lookup"><span data-stu-id="8a92f-103">Remove the Archiving server association</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8a92f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8a92f-104">

<span> </span></span></span>

<span data-ttu-id="8a92f-105">_**最終更新日:** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="8a92f-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="8a92f-106">アーカイブサーバーを削除するには、関連するフロントエンドプール、フロントエンドサーバー、Survivable Branch Appliance、および Survivable Branch Server の依存関係を変更またはクリアする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a92f-106">To remove an Archiving Server, you need to change or clear the dependency on the associated Front End pool, Front End Server, Survivable Branch Appliance and Survivable Branch Server.</span></span> <span data-ttu-id="8a92f-107">フロントエンドプール、フロントエンドサーバー、Survivable Branch Appliance、Survivable Branch Server のプロパティを編集して、依存関係を削除します。</span><span class="sxs-lookup"><span data-stu-id="8a92f-107">You edit the properties of the Front End pool, Front End Server, Survivable Branch Appliance and Survivable Branch Server to remove the dependency.</span></span> <span data-ttu-id="8a92f-108">依存関係を消去して、トポロジビルダーでサーバーを削除すると、トポロジビルダーの関連付けられたデータベースストアオブジェクトも削除されることが通知されます。</span><span class="sxs-lookup"><span data-stu-id="8a92f-108">After you clear the dependency and you delete the server in Topology Builder, you are notified that the associated database store object in Topology Builder will also be deleted.</span></span>

<div>

## <a name="to-remove-the-archiving-server-association"></a><span data-ttu-id="8a92f-109">アーカイブサーバーの関連付けを削除するには</span><span class="sxs-lookup"><span data-stu-id="8a92f-109">To remove the Archiving Server association</span></span>

1.  <span data-ttu-id="8a92f-110">Lync Server 2013 フロントエンドサーバーを開き、[トポロジビルダー] を開きます。</span><span class="sxs-lookup"><span data-stu-id="8a92f-110">Open the Lync Server 2013 Front End Server, open Topology Builder.</span></span>

2.  <span data-ttu-id="8a92f-111">Lync Server 2010 ノードに移動します。</span><span class="sxs-lookup"><span data-stu-id="8a92f-111">Navigate to the Lync Server 2010 node.</span></span>

3.  <span data-ttu-id="8a92f-112">[トポロジビルダー] で、アーカイブサーバーが定義されている場所に基づいて、 **Enterprise Edition のフロントエンドプール**、 **標準エディションのフロントエンドサーバー**、または **ブランチサイト** を展開します。</span><span class="sxs-lookup"><span data-stu-id="8a92f-112">In Topology Builder, expand **Enterprise Edition Front End pools**, **Standard Edition Front End Servers**, or **Branch sites**, based on where the Archiving Server is defined.</span></span>

4.  <span data-ttu-id="8a92f-113">Survivable Branch Server が関連付けられている場合は、[ **ブランチサイト**] を展開し、[ブランチサイト名] を展開して、[ **Survivable branch アプライアンス**] を展開します。</span><span class="sxs-lookup"><span data-stu-id="8a92f-113">If you have Survivable Branch Server associated, expand **Branch sites**, expand the branch site name, and then expand **Survivable Branch Appliances**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="8a92f-114">ユーザーインターフェイス内の<STRONG>Survivable Branch アプライアンス</STRONG>は、Survivable branch Server と Survivable branch Appliance の両方に適用されます。</span><span class="sxs-lookup"><span data-stu-id="8a92f-114"><STRONG>Survivable Branch Appliances</STRONG> in the user interface applies to both Survivable Branch Server and Survivable Branch Appliance.</span></span>

    
    </div>

5.  <span data-ttu-id="8a92f-115">アーカイブサーバーに関連付けられているプール、サーバー、またはデバイスを右クリックし、[ **プロパティの編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a92f-115">Right-click the pool, server, or device that is associated with the Archiving Server, and then click **Edit Properties**.</span></span>

6.  <span data-ttu-id="8a92f-116">[ **プロパティの編集**] の [ **全般**] で、[ **関連付け**] の下の [ **アーカイブサーバーの関連付け** ] チェックボックスをオフにして、[ **OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a92f-116">In **Edit Properties**, under **General**, under **Associations**, clear the **Associate Archiving Server** check box, and then click **OK**.</span></span>

7.  <span data-ttu-id="8a92f-117">削除するアーカイブサーバーに関連付けられているその他のプール、サーバー、またはデバイスについて、前の手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="8a92f-117">Repeat the previous step for any other pool, server or device associated with the Archiving Server that you want to remove.</span></span>

8.  <span data-ttu-id="8a92f-118">アーカイブサーバーを右クリックし、[ **削除**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a92f-118">Right-click the Archiving Server, and then click **Delete**.</span></span>

9.  <span data-ttu-id="8a92f-119">[ **依存** しているストアの削除] で、[ **OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a92f-119">On **Delete Dependent Stores**, click **OK**.</span></span>

10. <span data-ttu-id="8a92f-120">トポロジを公開し、レプリケーションの状態を確認してから、必要に応じて Lync Server 展開ウィザードを実行します。</span><span class="sxs-lookup"><span data-stu-id="8a92f-120">Publish the topology, check replication status, and then run the Lync Server Deployment Wizard as needed.</span></span>

<span data-ttu-id="8a92f-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8a92f-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

