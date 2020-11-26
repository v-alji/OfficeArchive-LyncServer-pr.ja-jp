---
title: 'Lync Server 2013: SQL Server のシステム要件'
description: 'Lync Server 2013: SQL Server のシステム要件'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: System requirements for SQL Server
ms:assetid: 9c235085-cbfa-4e9e-9cec-3f5749039a6b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205112(v=OCS.15)
ms:contentKeyID: 48184904
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 524136174be8798aed1dc7d5d236dbb45ab18330
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444554"
---
# <a name="system-requirements-for-sql-server-in-lync-server-2013"></a><span data-ttu-id="f6a01-103">Lync Server 2013 の SQL Server のシステム要件</span><span class="sxs-lookup"><span data-stu-id="f6a01-103">System requirements for SQL Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f6a01-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f6a01-104">

<span> </span></span></span>

<span data-ttu-id="f6a01-105">_**最終更新日:** 2013-10-25_</span><span class="sxs-lookup"><span data-stu-id="f6a01-105">_**Topic Last Modified:** 2013-10-25_</span></span>

<span data-ttu-id="f6a01-106">Enterprise Edition server を展開する前に、ハードウェア要件を満たす専用のコンピューターに Microsoft SQL Server 2008 R2 または Microsoft SQL Server 2012 をインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="f6a01-106">Before you deploy Enterprise Edition server, install Microsoft SQL Server 2008 R2 or Microsoft SQL Server 2012 on a dedicated computer that meets the hardware requirements.</span></span> <span data-ttu-id="f6a01-107">ハードウェア要件の詳細については、サポートドキュメントの「 [サーバーハードウェアプラットフォーム (Lync server 2013 の場合](lync-server-2013-server-hardware-platforms.md) )」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f6a01-107">For details about hardware requirements, see [Server hardware platforms for Lync Server 2013](lync-server-2013-server-hardware-platforms.md) in the Supportability documentation.</span></span> <span data-ttu-id="f6a01-108">ソフトウェア要件の詳細については、サポートドキュメントの「 [Lync Server 2013 でのデータベースソフトウェアのサポート](lync-server-2013-database-software-support.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f6a01-108">For details about software requirements, see [Database software support in Lync Server 2013](lync-server-2013-database-software-support.md) in the Supportability documentation.</span></span> <span data-ttu-id="f6a01-109">展開に必要なアクセス許可については、「 [Lync server 2013 の SQL Server の展開権限](lync-server-2013-deployment-permissions-for-sql-server.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f6a01-109">For information about the permissions necessary for deployment, see [Deployment permissions for SQL Server in Lync Server 2013](lync-server-2013-deployment-permissions-for-sql-server.md).</span></span>

<span data-ttu-id="f6a01-110">フロントエンドプールを作成する前に、SQL Server 構成マネージャーを使用してサーバーのポートを定義し、Advanced Security を使用して Windows ファイアウォールでポートを開いて、Lync Server 2013 で特定のポートを介して SQL Server へのアクセスを許可するように Windows ファイアウォールを構成する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="f6a01-110">Before you create the Front End pool, you must also configure Windows Firewall to allow Lync Server 2013 access to SQL Server over specific ports by defining ports for the server using SQL Server Configuration Manager and opening ports in Windows Firewall with Advanced Security.</span></span>

<span data-ttu-id="f6a01-111"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f6a01-111"></div>

<span> </span>

</div>

</div>

</span></span></div>

