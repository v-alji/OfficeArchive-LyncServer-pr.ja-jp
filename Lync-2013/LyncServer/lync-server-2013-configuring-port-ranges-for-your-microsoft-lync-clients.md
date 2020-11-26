---
title: 'Lync Server 2013: Microsoft Lync クライアントのポート範囲の構成'
description: 'Lync Server 2013: Microsoft Lync クライアントのポート範囲を構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring port ranges for your Microsoft Lync clients
ms:assetid: 287d5cea-7ada-461c-9b4a-9da2af315e71
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204760(v=OCS.15)
ms:contentKeyID: 48183694
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1e7fcabf81f8e0110010b1a4fb8e697fb0da986c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432731"
---
# <a name="configuring-port-ranges-for-your-microsoft-lync-clients-in-lync-server-2013"></a><span data-ttu-id="5cc65-103">Lync Server 2013 で Microsoft Lync クライアントのポート範囲を構成する</span><span class="sxs-lookup"><span data-stu-id="5cc65-103">Configuring port ranges for your Microsoft Lync clients in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5cc65-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5cc65-104">

<span> </span></span></span>

<span data-ttu-id="5cc65-105">_**最終更新日:** 2014-04-22_</span><span class="sxs-lookup"><span data-stu-id="5cc65-105">_**Topic Last Modified:** 2014-04-22_</span></span>

<span data-ttu-id="5cc65-106">既定では、Lync クライアントアプリケーションは、通信セッションに参加している場合は、ポート1024と65535の間の任意のポートを使うことができます。これは、特定のポート範囲がクライアントに対して自動的に有効にならないためです。</span><span class="sxs-lookup"><span data-stu-id="5cc65-106">By default, Lync client applications can use any port between ports 1024 and 65535 when involved in a communication session; this is because specific port ranges are not automatically enabled for clients.</span></span> <span data-ttu-id="5cc65-107">ただし、サービスの品質を使用するためには、さまざまな種類のトラフィック (オーディオ、ビデオ、メディア、アプリケーション共有、ファイル転送) を、一連の固有のポート範囲に割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="5cc65-107">In order to use Quality of Service, however, you will need to reassign the various traffic types (audio, video, media, application sharing, and file transfer) to a series of unique port ranges.</span></span> <span data-ttu-id="5cc65-108">これを行うには、Set-CsConferencingConfiguration コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="5cc65-108">This can be done by using the Set-CsConferencingConfiguration cmdlet.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5cc65-109">エンドユーザーはこれらの変更を行うことはできません。</span><span class="sxs-lookup"><span data-stu-id="5cc65-109">End users cannot make these changes themselves.</span></span> <span data-ttu-id="5cc65-110">ポートの変更は、管理者のみが Set-CsConferencingConfiguration コマンドレットを使用して行うことができます。</span><span class="sxs-lookup"><span data-stu-id="5cc65-110">Port changes can only be made by administrators using the Set-CsConferencingConfiguration cmdlet.</span></span>



</div>

<span data-ttu-id="5cc65-111">現在通信セッションに使用されているポート範囲を特定するには、Microsoft Lync Server 2013 管理シェルで次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="5cc65-111">You can determine which port ranges are currently used for communication sessions by running the following command from within the Microsoft Lync Server 2013 Management Shell:</span></span>

    Get-CsConferencingConfiguration

<span data-ttu-id="5cc65-112">Lync Server 2013 をインストールした後で会議の設定を変更していない場合は、次のプロパティ値を含む情報を取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5cc65-112">Assuming that you have not made any changes to your conferencing settings since you installed Lync Server 2013, you should get back information that includes these property values:</span></span>

    ClientMediaPortRangeEnabled : False
    ClientAudioPort             : 5350
    ClientAudioPortRange        : 40
    ClientVideoPort             : 5350
    ClientVideoPortRange        : 40
    ClientAppSharingPort        : 5350
    ClientAppSharingPortRange   : 40
    ClientFileTransferPort      : 5350
    ClientTransferPortRange     : 40

<span data-ttu-id="5cc65-113">上記の出力をよく見ると、2つの重要な点が表示されます。</span><span class="sxs-lookup"><span data-stu-id="5cc65-113">If you look closely at the preceding output, you'll see two things of importance.</span></span> <span data-ttu-id="5cc65-114">まず、ClientMediaPortRangeEnabled プロパティが False に設定されます。</span><span class="sxs-lookup"><span data-stu-id="5cc65-114">First, the ClientMediaPortRangeEnabled property is set to False:</span></span>

    ClientMediaPortRangeEnabled : False

<span data-ttu-id="5cc65-115">このプロパティが False に設定されている場合、通信セッションに参加するときに、Lync クライアントは、ポート1024と65535の間で利用可能なポートを使用します。これは、他のポート設定 (ClientMediaPort や ClientVideoPort など) に関係なく true になります。</span><span class="sxs-lookup"><span data-stu-id="5cc65-115">That's important because, when this property is set to False, Lync clients will use any available port between ports 1024 and 65535 when involved in a communication session; this is true regardless of any other port settings (for example, ClientMediaPort or ClientVideoPort).</span></span> <span data-ttu-id="5cc65-116">指定した一連のポートに使用を制限する場合 (これは、サービスの品質の実装を計画している場合に実行します)、まずクライアントのメディアポート範囲を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5cc65-116">If you want to restrict usage to a specified set of ports (and this is something you do want to do if you plan on implementing Quality of Service) then you must first enable client media port ranges.</span></span> <span data-ttu-id="5cc65-117">この操作を行うには、次の Windows PowerShell コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="5cc65-117">That can be done using the following Windows PowerShell command:</span></span>

    Set-CsConferencingConfiguration -ClientMediaPortRangeEnabled $True

<span data-ttu-id="5cc65-118">上のコマンドを実行すると、会議構成設定のグローバルコレクションに対してクライアントのメディアポート範囲が有効になります。ただし、これらの設定は、サイトのスコープやサービスの範囲 (会議サーバーサービスのみ) に適用することもできます。</span><span class="sxs-lookup"><span data-stu-id="5cc65-118">The preceding command enables client media port ranges for the global collection of conferencing configuration settings; however, these settings can also be applied to the site scope and/or the service scope (for the Conferencing Server service only).</span></span> <span data-ttu-id="5cc65-119">特定のサイトまたはサーバーに対してクライアントのメディアポート範囲を有効にするには、Set-CsConferencingConfiguration を呼び出すときにそのサイトまたはサーバーの Id を指定します。</span><span class="sxs-lookup"><span data-stu-id="5cc65-119">To enable client media port ranges for a specific site or server, specify the Identity of that site or server when calling Set-CsConferencingConfiguration:</span></span>

    Set-CsConferencingConfiguration -Identity "site:Redmond" -ClientMediaPortRangeEnabled $True

<span data-ttu-id="5cc65-120">または、このコマンドを使用して、すべての会議構成設定のポート範囲を同時に有効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="5cc65-120">Alternatively, you can use this command to simultaneously enable port ranges for all your conferencing configuration settings:</span></span>

    Get-CsConferencingConfiguration | Set-CsConferencingConfiguration  -ClientMediaPortRangeEnabled $True

<span data-ttu-id="5cc65-121">2番目の重要な点は、既定では、各種類のネットワークトラフィックに設定されたメディアポート範囲が同じであることを示しています。</span><span class="sxs-lookup"><span data-stu-id="5cc65-121">The second thing of importance you will notice is that the sample output shows that, by default, the media port ranges set for each type of network traffic are identical:</span></span>

    ClientAudioPort             : 5350
    ClientVideoPort             : 5350
    ClientAppSharingPort        : 5350
    ClientFileTransferPort      : 5350

<span data-ttu-id="5cc65-122">QoS を実装するために、これらの各ポート範囲は一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="5cc65-122">In order to implement QoS, each of these port ranges will need to be unique.</span></span> <span data-ttu-id="5cc65-123">たとえば、次のようなポート範囲を構成することができます。</span><span class="sxs-lookup"><span data-stu-id="5cc65-123">For example, you might configure the port ranges like this:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5cc65-124">クライアントトラフィックの種類</span><span class="sxs-lookup"><span data-stu-id="5cc65-124">Client Traffic Type</span></span></th>
<th><span data-ttu-id="5cc65-125">ポートの開始</span><span class="sxs-lookup"><span data-stu-id="5cc65-125">Port Start</span></span></th>
<th><span data-ttu-id="5cc65-126">ポートの範囲</span><span class="sxs-lookup"><span data-stu-id="5cc65-126">Port Range</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5cc65-127">オーディオ</span><span class="sxs-lookup"><span data-stu-id="5cc65-127">Audio</span></span></p></td>
<td><p><span data-ttu-id="5cc65-128">50020</span><span class="sxs-lookup"><span data-stu-id="5cc65-128">50020</span></span></p></td>
<td><p><span data-ttu-id="5cc65-129">超える</span><span class="sxs-lookup"><span data-stu-id="5cc65-129">20</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cc65-130">ビデオ</span><span class="sxs-lookup"><span data-stu-id="5cc65-130">Video</span></span></p></td>
<td><p><span data-ttu-id="5cc65-131">58000</span><span class="sxs-lookup"><span data-stu-id="5cc65-131">58000</span></span></p></td>
<td><p><span data-ttu-id="5cc65-132">超える</span><span class="sxs-lookup"><span data-stu-id="5cc65-132">20</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cc65-133">アプリケーション共有</span><span class="sxs-lookup"><span data-stu-id="5cc65-133">Application sharing</span></span></p></td>
<td><p><span data-ttu-id="5cc65-134">42000</span><span class="sxs-lookup"><span data-stu-id="5cc65-134">42000</span></span></p></td>
<td><p><span data-ttu-id="5cc65-135">超える</span><span class="sxs-lookup"><span data-stu-id="5cc65-135">20</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cc65-136">ファイル転送</span><span class="sxs-lookup"><span data-stu-id="5cc65-136">File transfer</span></span></p></td>
<td><p><span data-ttu-id="5cc65-137">42020</span><span class="sxs-lookup"><span data-stu-id="5cc65-137">42020</span></span></p></td>
<td><p><span data-ttu-id="5cc65-138">超える</span><span class="sxs-lookup"><span data-stu-id="5cc65-138">20</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5cc65-139">上の表のクライアントポート範囲は、サーバーに構成されているポート範囲のサブセットを表しています。</span><span class="sxs-lookup"><span data-stu-id="5cc65-139">In the preceding table, client port ranges represent a subset of the port ranges configured for your servers.</span></span> <span data-ttu-id="5cc65-140">たとえば、サーバー上では、40803 ~ 49151 のポートを使用するようにアプリケーション共有が構成されています。クライアントコンピューターでは、[アプリケーション共有] は、42000 ~ 42019 のポートを使用するように構成されます。</span><span class="sxs-lookup"><span data-stu-id="5cc65-140">For example, on the servers, application sharing was configured to use ports 40803 through 49151; on the client computers, application sharing is configured to use ports 42000 through 42019.</span></span> <span data-ttu-id="5cc65-141">これは主に、QoS の管理を簡単にするために行われています。クライアントポートは、サーバーで使われているポートのサブセットを表す必要はありません。</span><span class="sxs-lookup"><span data-stu-id="5cc65-141">This, too is done primarily to make administration of QoS easier: client ports do not have to represent a subset of the ports used on the server.</span></span> <span data-ttu-id="5cc65-142">(たとえば、クライアントコンピューターで、1万 ~ 10019 のポートを使用するようにアプリケーション共有を構成することができます)。ただし、クライアントポート範囲をサーバーのポート範囲のサブセットにすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="5cc65-142">(For example, on the client computers you could configure application sharing to use, say, ports 10000 through 10019.) However, it is recommended that you make your client port ranges a subset of your server port ranges.</span></span>

<span data-ttu-id="5cc65-143">また、サーバー上でのアプリケーション共有のために8348のポートが設定されていても、クライアントでのアプリケーション共有については20個のポートしか設定されていないことに気付いた場合もあります。</span><span class="sxs-lookup"><span data-stu-id="5cc65-143">In addition, you might have noticed that 8348 ports were set aside for application sharing on the servers, but only 20 ports were set aside for application sharing on the clients.</span></span> <span data-ttu-id="5cc65-144">これは推奨されていますが、ハード・ファースト・ファーストルールではありません。</span><span class="sxs-lookup"><span data-stu-id="5cc65-144">This, too is recommended, but is not a hard-and-fast rule.</span></span> <span data-ttu-id="5cc65-145">一般的に、1つの通信セッションを表すために使用可能な各ポートを検討することができます。ポートの範囲内で利用可能な100ポートがある場合は、特定の時間に最大100の通信セッションに参加できることを意味します。</span><span class="sxs-lookup"><span data-stu-id="5cc65-145">In general, you can consider each available port to represent a single communication session: if you have 100 ports available in a port range that means that the computer in question could participate in, at most, 100 communication sessions at any given time.</span></span> <span data-ttu-id="5cc65-146">サーバーはクライアントよりも多くの会話に参加する可能性があるため、クライアントよりも多くのポートをサーバー上で開くことが適切です。</span><span class="sxs-lookup"><span data-stu-id="5cc65-146">Because servers will likely take part in many more conversations than clients, it makes sense to open many more ports on servers than on clients.</span></span> <span data-ttu-id="5cc65-147">クライアント上のアプリケーション共有に20個のポートを確保することは、ユーザーが指定したデバイスで20個のアプリケーション共有セッションに参加することを意味します。</span><span class="sxs-lookup"><span data-stu-id="5cc65-147">Setting aside 20 ports for application sharing on a client means that a user could participate in 20 application sharing sessions on the specified device, and all at the same time.</span></span> <span data-ttu-id="5cc65-148">これは、ほとんどのユーザーにとって十分なものであることを証明する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5cc65-148">That should prove sufficient for the vast majority of your users.</span></span>

<span data-ttu-id="5cc65-149">会議の構成設定のグローバルコレクションに上記のポート範囲を割り当てるには、次の Lync Server 管理シェルコマンドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="5cc65-149">To assign the preceding port ranges to your global collection of conferencing configuration settings you can use the following Lync Server Management Shell command:</span></span>

    Set-CsConferencingConfiguration -Identity global -ClientAudioPort 50020 -ClientAudioPortRange 20 -ClientVideoPort 58000 -ClientVideoPortRange 20 -ClientAppSharingPort 42000 -ClientAppSharingPortRange 20 - ClientFileTransferPort 42020 -ClientFileTransferPortRange 20

<span data-ttu-id="5cc65-150">または、このコマンドを使用して、すべての会議の構成設定にこれらと同じポート範囲を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="5cc65-150">Or, use this command to assign these same port ranges for all your conferencing configuration settings:</span></span>

    Get-CsConferencingConfiguration | Set-CsConferencingConfiguration -ClientAudioPort 50020 -ClientAudioPortRange 20 -ClientVideoPort 58000 -ClientVideoPortRange 20 -ClientAppSharingPort 42000 -ClientAppSharingPortRange 20 - ClientFileTransferPort 42020 -ClientFileTransferPortRange 20

<span data-ttu-id="5cc65-151">個々のユーザーは Lync からログオフしてから再びログインする必要があります。実際には、これらの変更は有効になります。</span><span class="sxs-lookup"><span data-stu-id="5cc65-151">Individual users must log off from Lync and then log back on before these changes will actually take effect.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5cc65-152">クライアントのメディアポート範囲を有効にして、1つのコマンドを使用してこれらのポート範囲を割り当てることもできます。</span><span class="sxs-lookup"><span data-stu-id="5cc65-152">You can also enable client media port ranges, and then assign those port ranges, using a single command.</span></span> <span data-ttu-id="5cc65-153">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="5cc65-153">For example:</span></span><BR><CODE>Set-CsConferencingConfiguration -ClientMediaPortRangeEnabled $True -ClientAudioPort 50020 -ClientAudioPortRange 20 -ClientVideoPort 58000 -ClientVideoPortRange 20 -ClientAppSharingPort 42000 -ClientAppSharingPortRange 20 -ClientFileTransferPort 42020 -ClientFileTransferPortRange 20</CODE>



<span data-ttu-id="5cc65-154"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5cc65-154"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

