---
title: 既存の会議および会議コンテンツの移行
description: 既存の会議と会議のコンテンツを移行します。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate existing meetings and meeting content
ms:assetid: 30516731-2ae1-4a6d-a7e1-d3f05778c954
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688011(v=OCS.15)
ms:contentKeyID: 49733599
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d94dd35063a121a057a218c27fdb36e42a155b77
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443805"
---
# <a name="migrate-existing-meetings-and-meeting-content"></a><span data-ttu-id="fe120-103">既存の会議および会議コンテンツの移行</span><span class="sxs-lookup"><span data-stu-id="fe120-103">Migrate existing meetings and meeting content</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fe120-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fe120-104">

<span> </span></span></span>

<span data-ttu-id="fe120-105">_**最終更新日:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="fe120-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="fe120-106">ユーザーアカウントを Lync Server 2010 から Lync Server 2013 サーバーに移動すると、次の情報がそのユーザーアカウントに移動されます。</span><span class="sxs-lookup"><span data-stu-id="fe120-106">When a user account is moved from Lync Server 2010 to a Lync Server 2013 server, the following information is moved with that user account:</span></span>

  - <span data-ttu-id="fe120-107">**ユーザーが既にスケジュールした会議**。</span><span class="sxs-lookup"><span data-stu-id="fe120-107">**Meetings already scheduled by the user**.</span></span> <span data-ttu-id="fe120-108">これには、会議ディレクトリと会議データの移動が含まれます。</span><span class="sxs-lookup"><span data-stu-id="fe120-108">This includes moving the conferencing directories and conferencing data.</span></span>

  - <span data-ttu-id="fe120-109">**ユーザーの暗証番号 (PIN)**。</span><span class="sxs-lookup"><span data-stu-id="fe120-109">**User’s personal identification number (PIN)**.</span></span> <span data-ttu-id="fe120-110">ユーザーの現在の PIN は、有効期限が切れるか、ユーザーが新しい PIN を要求するまで、引き続き動作します。</span><span class="sxs-lookup"><span data-stu-id="fe120-110">The user’s current PIN continues to work until it expires or the user requests a new PIN.</span></span>

<span data-ttu-id="fe120-111">次のユーザーアカウント情報は、新しいサーバーに移動されません。</span><span class="sxs-lookup"><span data-stu-id="fe120-111">The following user account information does not move to the new server.</span></span>

  - <span data-ttu-id="fe120-112">**会議コンテンツ**。</span><span class="sxs-lookup"><span data-stu-id="fe120-112">**Meeting content**.</span></span> <span data-ttu-id="fe120-113">会議中に共有されたコンテンツ (PowerPoint、ホワイトボード、添付ファイル、投票データなど) を移動するには、 **move-CsUser** コマンドレットの一部として、 **-moveconの [data** ] パラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="fe120-113">In order to move the content shared during a meeting, for example PowerPoint, Whiteboard, attachments or poll data, use the **-MoveConferenceData** parameter as part of the **Move-CsUser** cmdlet.</span></span>

<span data-ttu-id="fe120-114"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fe120-114"></div>

<span> </span>

</div>

</div>

</span></span></div>

