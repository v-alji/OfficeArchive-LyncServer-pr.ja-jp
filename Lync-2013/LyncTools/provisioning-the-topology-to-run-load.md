---
title: ロードを実行するトポロジのプロビジョニング
description: ロードを実行するトポロジのプロビジョニング。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Provisioning the Topology to Run Load
ms:assetid: 6fba03df-3914-4d2a-8208-e252ad993aff
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945598(v=OCS.15)
ms:contentKeyID: 51541424
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: da482fde949675acc1722305433b95b7a6a6b523
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446424"
---
# <a name="provisioning-the-topology-to-run-load"></a><span data-ttu-id="594a3-103">ロードを実行するトポロジのプロビジョニング</span><span class="sxs-lookup"><span data-stu-id="594a3-103">Provisioning the Topology to Run Load</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="594a3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="594a3-104">

<span> </span></span></span>

<span data-ttu-id="594a3-105">_**最終更新日:** 2013-02-04_</span><span class="sxs-lookup"><span data-stu-id="594a3-105">_**Topic Last Modified:** 2013-02-04_</span></span>

<div>

<span data-ttu-id="594a3-106">Lync Server 2013 の既存の設定と構成によっては、お使いの環境で次の変更を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="594a3-106">Depending on your existing settings and configuration of Lync Server 2013, you may need to make the following changes in your environment:</span></span>

1.  <span data-ttu-id="594a3-107">Windows PowerShell の実行ポリシーを無制限に設定します。</span><span class="sxs-lookup"><span data-stu-id="594a3-107">Set the Windows PowerShell execution policy to Unrestricted.</span></span> <span data-ttu-id="594a3-108">実行ポリシーの設定を確認するには、Lync Server 管理シェルを開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="594a3-108">To check your execution policy settings, open the Lync Server Management Shell and run the following command:</span></span>

    ``` powershell
        Get-ExecutionPolicy
    ```        

    <span data-ttu-id="594a3-109">このコマンドを実行しても無制限の値が返されない場合は、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="594a3-109">If this command does not return the value Unrestricted, run this command:</span></span>

    ``` powershell
        Set-ExecutionPolicy -Unrestricted
    ```

2.  <span data-ttu-id="594a3-110">Lync Server 2013 を効果的に構成するには、次のことを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="594a3-110">To effectively configure Lync Server 2013, you will need to:</span></span>
    
      - <span data-ttu-id="594a3-111">Lync Server 2013 トポロジ (コンピューター名、サービスインスタンス、サイト名、ポリシーなど) について理解している必要があります。</span><span class="sxs-lookup"><span data-stu-id="594a3-111">Be familiar with Lync Server 2013 topology (for example, computer names, service instances, site names, and policies).</span></span>
    
      - <span data-ttu-id="594a3-112">応答グループのハントグループ (SIP Uri など) など、グループに作成されたユーザーの一部を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="594a3-112">Assign some of the users that were created to groups, such as Response Group hunt groups (for example, SIP URIs).</span></span>

3.  <span data-ttu-id="594a3-113">コマンドラインからスクリプトを実行するには、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="594a3-113">To run the script from the command line, you may use:</span></span>

    ``` powershell
        Powershell.exe -file <path to the file>
    ```
    
4.  <span data-ttu-id="594a3-114">通常、このパッケージのいずれかのスクリプトが実行されると、スクリプトからの結果のトレースは、スクリプトが呼び出されたときと同じパスのファイルに格納され、 \<scriptname\> $h $ m $s.txt という名前が付けられます。</span><span class="sxs-lookup"><span data-stu-id="594a3-114">Typically, after one of the scripts in this package runs, the resulting traces from the script will be stored in a file in the same path from which the script was invoked, named \<scriptname\>$h$m$s.txt.</span></span> <span data-ttu-id="594a3-115">たとえば、ArchivingPolicy.ps1 を午後12:15 時に実行します。</span><span class="sxs-lookup"><span data-stu-id="594a3-115">For example, running ArchivingPolicy.ps1 at 12:15 P.M.</span></span> <span data-ttu-id="594a3-116">ArchivingPolicy121500.txt などのログファイルが生成されます。</span><span class="sxs-lookup"><span data-stu-id="594a3-116">will generate a log file such as ArchivingPolicy121500.txt.</span></span>

5.  <span data-ttu-id="594a3-117">最後に、サーバーを構成するための例を用意しましたが、ロードの実行が完了した後で構成を変更または削除する責任があります。</span><span class="sxs-lookup"><span data-stu-id="594a3-117">Finally, note that although we have provided examples to configure the server, you are responsible for modifying or deleting the configuration after you have finished running the load.</span></span>

<span data-ttu-id="594a3-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="594a3-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

