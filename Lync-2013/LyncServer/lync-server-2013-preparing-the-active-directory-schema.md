---
title: 'Lync Server 2013: Active Directory スキーマの準備'
description: 'Lync Server 2013: Active Directory スキーマの準備をしています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing the Active Directory schema
ms:assetid: 067726ae-fd3f-4133-a32f-26d2603ac674
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398119(v=OCS.15)
ms:contentKeyID: 48183300
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3df7533dcbabe278fd366b441cfd8daa83f54b23
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424115"
---
# <a name="preparing-the-active-directory-schema-in-lync-server-2013"></a><span data-ttu-id="d8a2a-103">Lync Server 2013 での Active Directory スキーマの準備</span><span class="sxs-lookup"><span data-stu-id="d8a2a-103">Preparing the Active Directory schema in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d8a2a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d8a2a-104">

<span> </span></span></span>

<span data-ttu-id="d8a2a-105">_**最終更新日:** 2012-08-27_</span><span class="sxs-lookup"><span data-stu-id="d8a2a-105">_**Topic Last Modified:** 2012-08-27_</span></span>

<span data-ttu-id="d8a2a-106">Active Directory ドメインサービスの準備を始める前に、Windows メモ帳などのテキストエディターを使用してスキーマファイルを開くか、lync server [2013 で使用さ](lync-server-2013-active-directory-schema-extensions-classes-and-attributes-used-by-lync-server.md) れている Active Directory ドメインサービスのスキーマ拡張機能を確認して、lync server 2013 で変更されるすべての Active Directory ドメインサービスのスキーマ拡張を確認することができます。</span><span class="sxs-lookup"><span data-stu-id="d8a2a-106">Before you begin preparing Active Directory Domain Services, you can open the schema files by using a text editor, such as Windows Notepad, or see [Active Directory schema extensions, classes, and attributes used by Lync Server 2013](lync-server-2013-active-directory-schema-extensions-classes-and-attributes-used-by-lync-server.md) to review all the Active Directory Domain Services schema extensions that will be modified for Lync Server 2013.</span></span> <span data-ttu-id="d8a2a-107">Lync Server では、次の4つのスキーマファイルが使用されます。</span><span class="sxs-lookup"><span data-stu-id="d8a2a-107">Lync Server uses four schema files:</span></span>

  - <span data-ttu-id="d8a2a-108">Microsoft Exchange Server との相互運用性を実現するために使用される ExternalSchema. .ldf</span><span class="sxs-lookup"><span data-stu-id="d8a2a-108">ExternalSchema.ldf, which is used for interoperability with Microsoft Exchange Server</span></span>

  - <span data-ttu-id="d8a2a-109">ServerSchema: プライマリ Lync Server 2013 スキーマファイル</span><span class="sxs-lookup"><span data-stu-id="d8a2a-109">ServerSchema.ldf, which is the primary Lync Server 2013 schema file</span></span>

  - <span data-ttu-id="d8a2a-110">BackCompatSchema。以前のリリースのコンポーネントとの相互運用性を実現するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d8a2a-110">BackCompatSchema.ldf, which is used for interoperability with any components from prior releases</span></span>

  - <span data-ttu-id="d8a2a-111">既成のスキーマのバージョン情報として使用される VersionSchema。</span><span class="sxs-lookup"><span data-stu-id="d8a2a-111">VersionSchema.ldf, which is used for version information of the prepared schema</span></span>

<span data-ttu-id="d8a2a-112">以前のリリースから移行するか、クリーンインストールを実行するかに関係なく、スキーマの準備中にすべての .ldf ファイルがインストールされます。</span><span class="sxs-lookup"><span data-stu-id="d8a2a-112">All .ldf files are installed during schema preparation, regardless of whether you are migrating from a previous release or performing a clean installation.</span></span> <span data-ttu-id="d8a2a-113">これらのスキーマファイルは、上に示した順序でインストールされ、 \\ \\ インストールメディアの [サポートスキーマ] フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="d8a2a-113">These schema files are installed in the sequence shown in the preceding list and are located in the \\Support\\schema folder on the installation media.</span></span>

<span data-ttu-id="d8a2a-114">Lync Server スキーマの拡張機能は、ネットワークトラフィックに影響を与えるすべてのドメインにわたってレプリケートされます。</span><span class="sxs-lookup"><span data-stu-id="d8a2a-114">The Lync Server schema extensions are replicated across all domains, which impacts network traffic.</span></span> <span data-ttu-id="d8a2a-115">ネットワーク使用量が少なくなったら、一度にスキーマの準備を実行します。</span><span class="sxs-lookup"><span data-stu-id="d8a2a-115">Run schema preparation at a time when network usage is low.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="d8a2a-116">Microsoft® Office Communicator mobile 2007 R2 for Java および Microsoft® Office communicator mobile を使用して 2013 Lync 1.0 モバイルクライアント用のサポートを追加する必要がある場合は、Lync Server 2013 のインストール中に Microsoft Office Communications Server 2007 R2 の Active Directory スキーマを準備する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8a2a-116">If you need to add support for Microsoft® Office Communicator Mobile 2007 R2 for Java and Microsoft® Office Communicator Mobile for Nokia 1.0 mobile clients to your Lync Server 2013 deployment, you need to prepare the Active Directory schema for Microsoft Office Communications Server 2007 R2 during installation of Lync Server 2013.</span></span> <span data-ttu-id="d8a2a-117">必要なソフトウェアとドキュメントについては、を参照してください <A href="https://go.microsoft.com/fwlink/p/?linkid=207172">https://go.microsoft.com/fwlink/p/?linkId=207172</A> 。</span><span class="sxs-lookup"><span data-stu-id="d8a2a-117">For the necessary software and documentation, see <A href="https://go.microsoft.com/fwlink/p/?linkid=207172">https://go.microsoft.com/fwlink/p/?linkId=207172</A>.</span></span>



</div>

<div>

## <a name="adsi-edit"></a><span data-ttu-id="d8a2a-118">ADSI の編集</span><span class="sxs-lookup"><span data-stu-id="d8a2a-118">ADSI Edit</span></span>

<span data-ttu-id="d8a2a-119">Active Directory サービスインターフェイスエディター (ADSI Edit) は、スキーマの準備とレプリケーションを確認するために使用できる AD DS 管理ツールです。</span><span class="sxs-lookup"><span data-stu-id="d8a2a-119">Active Directory Service Interfaces Editor (ADSI Edit) is an AD DS administration tool that you can use to verify schema preparation and replication.</span></span>

<span data-ttu-id="d8a2a-120">サーバーをドメインコントローラーにするには、AD DS の役割をインストールするときに、ADSI の編集が既定でインストールされます。</span><span class="sxs-lookup"><span data-stu-id="d8a2a-120">ADSI Edit is installed by default when you install the AD DS role to make a server a domain controller.</span></span> <span data-ttu-id="d8a2a-121">Windows Server 2008 および Windows Server 2008 R2 の場合、リモートサーバー管理ツール (RSAT) に ADSI Edit (adsiedit) が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d8a2a-121">For Windows Server 2008 and Windows Server 2008 R2, ADSI Edit (adsiedit.msc) is included with the Remote Server Administration Tools (RSAT).</span></span> <span data-ttu-id="d8a2a-122">また、ドメインメンバーサーバーまたはスタンドアロンサーバーに RSAT をインストールすることもできます。</span><span class="sxs-lookup"><span data-stu-id="d8a2a-122">You can also install RSAT on domain member servers or stand-alone servers.</span></span> <span data-ttu-id="d8a2a-123">Windows をインストールすると、既定では、RSAT パッケージはこれらのサーバーにコピーされますが、既定ではインストールされません。</span><span class="sxs-lookup"><span data-stu-id="d8a2a-123">The RSAT package is copied to these servers by default when you install Windows, but it is not installed by default.</span></span> <span data-ttu-id="d8a2a-124">サーバーマネージャーを使用して個々のツールをインストールします。</span><span class="sxs-lookup"><span data-stu-id="d8a2a-124">You install individual tools by using Server Manager.</span></span> <span data-ttu-id="d8a2a-125">ADSI Edit は、[ **役割管理ツール**]、[ **Active Directory ドメインサービスツール**]、[ **active directory ドメインコントローラーツール**] に含まれています。</span><span class="sxs-lookup"><span data-stu-id="d8a2a-125">ADSI Edit is included under **Role Administration Tools**, **Active Directory Domain Services Tools**, **Active Directory Domain Controller Tools**.</span></span>

<span data-ttu-id="d8a2a-126">Windows Server 2003 の場合、ADSI Edit はサポートツールに含まれています。</span><span class="sxs-lookup"><span data-stu-id="d8a2a-126">For Windows Server 2003, ADSI Edit is included with the Support Tools.</span></span> <span data-ttu-id="d8a2a-127">サポートツールは、Windows Server 2003 CD の [ \\ サポート \\ ツール] フォルダーにあります。または、"windows Server 2003 Service Pack 2 32 ビットサポートツール" からダウンロードすることもでき [https://go.microsoft.com/fwlink/p/?linkId=125770](https://go.microsoft.com/fwlink/p/?linkid=125770) ます。</span><span class="sxs-lookup"><span data-stu-id="d8a2a-127">The Support Tools are available from the Windows Server 2003 CD in the \\SUPPORT\\TOOLS folder, or you can download them from “Windows Server 2003 Service Pack 2 32-bit Support Tools” at [https://go.microsoft.com/fwlink/p/?linkId=125770](https://go.microsoft.com/fwlink/p/?linkid=125770).</span></span> <span data-ttu-id="d8a2a-128">製品 CD のサポートツールをインストールする手順については、「Windows サポートツールをインストールする」を参照 [https://go.microsoft.com/fwlink/p/?linkId=125771](https://go.microsoft.com/fwlink/p/?linkid=125771) してください。</span><span class="sxs-lookup"><span data-stu-id="d8a2a-128">Instructions for installing the Support Tools from the product CD are available from “Install Windows Support Tools” at [https://go.microsoft.com/fwlink/p/?linkId=125771](https://go.microsoft.com/fwlink/p/?linkid=125771).</span></span> <span data-ttu-id="d8a2a-129">サポートツールをインストールすると、Adsiedit.dll が自動的に登録されます。</span><span class="sxs-lookup"><span data-stu-id="d8a2a-129">Adsiedit.dll is automatically registered when you install the support tools.</span></span> <span data-ttu-id="d8a2a-130">ただし、ファイルをコンピューターにコピーした場合は、ツールを実行する前に、 **regsvr32** コマンドを実行して adsiedit.dll ファイルを登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8a2a-130">If, however, you copied the files to your computer, you must run the **regsvr32** command to register the adsiedit.dll file before you can run the tool.</span></span>

</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="d8a2a-131">このセクション中</span><span class="sxs-lookup"><span data-stu-id="d8a2a-131">In This Section</span></span>

  - [<span data-ttu-id="d8a2a-132">Lync Server 2013 での Active Directory スキーマの準備の実行</span><span class="sxs-lookup"><span data-stu-id="d8a2a-132">Running Active Directory schema preparation in Lync Server 2013</span></span>](lync-server-2013-running-schema-preparation.md)

  - [<span data-ttu-id="d8a2a-133">Lync Server 2013 での Active Directory スキーマのレプリケーションの確認</span><span class="sxs-lookup"><span data-stu-id="d8a2a-133">Verifying Active Directory schema replication in Lync Server 2013</span></span>](lync-server-2013-verifying-schema-replication.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d8a2a-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="d8a2a-134">See Also</span></span>


[<span data-ttu-id="d8a2a-135">Lync Server 2013 でのフォレストの準備</span><span class="sxs-lookup"><span data-stu-id="d8a2a-135">Preparing the forest for Lync Server 2013</span></span>](lync-server-2013-preparing-the-forest.md)  
[<span data-ttu-id="d8a2a-136">Lync Server 2013 のドメインの準備</span><span class="sxs-lookup"><span data-stu-id="d8a2a-136">Preparing domains for Lync Server 2013</span></span>](lync-server-2013-preparing-domains.md)  
  

<span data-ttu-id="d8a2a-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d8a2a-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

