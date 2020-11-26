---
title: 'Lync Server 2013: Lync Server の Windows 更新プログラム'
description: 'Lync Server 2013: Lync Server 用 Windows Update'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Windows Update for Lync Server 2013
ms:assetid: fe26ab32-b1a9-421d-9227-506703d4b834
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn518337(v=OCS.15)
ms:contentKeyID: 62625495
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fe4b6d201a35584fceae5628b91631b48b30faae
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446171"
---
# <a name="windows-update-for-lync-server-2013"></a><span data-ttu-id="6ea65-103">Lync Server 2013 の Windows 更新プログラム</span><span class="sxs-lookup"><span data-stu-id="6ea65-103">Windows Update for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6ea65-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6ea65-104">

<span> </span></span></span>

<span data-ttu-id="6ea65-105">_**最終更新日:** 2013-12-05_</span><span class="sxs-lookup"><span data-stu-id="6ea65-105">_**Topic Last Modified:** 2013-12-05_</span></span>

<span data-ttu-id="6ea65-106">Windows Update Services を使用して、更新プログラムとセキュリティ更新プログラムを頻繁に確認して適用します。</span><span class="sxs-lookup"><span data-stu-id="6ea65-106">Frequently check for and apply updates and security updates using Windows Update Services.</span></span> <span data-ttu-id="6ea65-107">こうすることによって、攻撃者が Microsoft Lync Server 2013 を実行しているサーバーへのアクセス権を管理者権限で実行し、Lync Server 2013 に悪影響を与える可能性のあるその他のシステムコンポーネントの脆弱性を防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="6ea65-107">Doing so helps prevents vulnerabilities in other system components that might lead to attackers being able to gain access to servers running Microsoft Lync Server 2013 with administrator rights and thereby compromise Lync Server 2013.</span></span>

<span data-ttu-id="6ea65-108">Microsoft SQL Server 2008 Express (64 ビット版) の更新プログラムは、各 Lync Server 2013 Standard Edition server (バックエンドデータベース用) と、その他のすべての Lync Server 2013 server (ローカル構成ストア用) で、これらのデータベースを SQL Server 2008 R2 Express にアップグレードしていない場合に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6ea65-108">Updates for Microsoft SQL Server 2008 Express (64-bit edition) runs on each Lync Server 2013 Standard Edition server (for the back-end database) and on all other Lync Server 2013 server roles (for the Local Configuration Store), unless you have upgraded these databases to SQL Server 2008 R2 Express.</span></span> <span data-ttu-id="6ea65-109">フロントエンドプールのバックエンドデータベース、監視データベース、アーカイブデータベースの SQL Server は、定期的なセキュリティ更新プログラムの保守の一部として考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ea65-109">You should consider these databases as part of routine security update maintenance, as should SQL Server on the back-end database of a Front End pool, the Monitoring database, and the Archiving database.</span></span>

<div>

## <a name="best-practice"></a><span data-ttu-id="6ea65-110">ベストプラクティス</span><span class="sxs-lookup"><span data-stu-id="6ea65-110">Best Practice</span></span>

  - <span data-ttu-id="6ea65-111">Windows Update で現在の状態を維持します。</span><span class="sxs-lookup"><span data-stu-id="6ea65-111">Keep current with Windows Update.</span></span>

<span data-ttu-id="6ea65-112"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6ea65-112"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

