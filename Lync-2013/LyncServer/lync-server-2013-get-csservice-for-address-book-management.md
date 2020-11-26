---
title: 'Lync Server 2013: アドレス帳管理の Get-CsService'
description: 'Lync Server 2013: アドレス帳の管理に Get-CsService します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Get-CsService for Address Book management
ms:assetid: 373b717d-5efa-4c36-a899-a23a5bd922b4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429698(v=OCS.15)
ms:contentKeyID: 48183853
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5e46173429988d87022c13fab33e3778279dd0e9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427986"
---
# <a name="get-csservice-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="6bee0-103">Lync Server 2013 でのアドレス帳管理の Get-CsService</span><span class="sxs-lookup"><span data-stu-id="6bee0-103">Get-CsService for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6bee0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6bee0-104">

<span> </span></span></span>

<span data-ttu-id="6bee0-105">_**最終更新日:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="6bee0-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="6bee0-106">このコマンドレットを実行できるユーザー: 既定では、次のグループのメンバーは、Get-CsService コマンドレットをローカルで実行することを許可されています: RTCUniversalUserAdmins、RTCUniversalServerAdmins。</span><span class="sxs-lookup"><span data-stu-id="6bee0-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Get-CsService cmdlet locally: RTCUniversalUserAdmins, RTCUniversalServerAdmins.</span></span> <span data-ttu-id="6bee0-107">このコマンドレットが割り当てられているすべての役割ベースのアクセス制御 (RBAC) ロールのリストを返すには (自分自身で作成したカスタム RBAC ロールを含む)、Windows PowerShell プロンプトから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="6bee0-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Get-CsService"}

<span data-ttu-id="6bee0-108">Get-CsService は、インフラストラクチャで定義された Web サービスの現在の構成を取得して表示するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="6bee0-108">Get-CsService is valuable to retrieve and display the current configuration of your infrastructure’s defined Web Services.</span></span> <span data-ttu-id="6bee0-109">プールの完全修飾ドメイン名 (FQDN) とパラメーター WebServer を定義することによって、サーバーによって提供される web ベースのサービス (アドレス帳ハンドラー、配布リスト展開の Uri など) が返されます。</span><span class="sxs-lookup"><span data-stu-id="6bee0-109">By defining the pool’s fully qualified domain name (FQDN) and the parameter WebServer, the cmdlet returns the web-based services offered by your server, including the Address Book handler and distribution list expansion URIs.</span></span>

<span data-ttu-id="6bee0-110">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="6bee0-110">For example:</span></span>

    Get-CsService -PoolFqdn "fe01.contoso.net" -WebServer

<span data-ttu-id="6bee0-111">このコマンドレットは、次の値を返します。</span><span class="sxs-lookup"><span data-stu-id="6bee0-111">This cmdlet returns the following:</span></span>

<span data-ttu-id="6bee0-112">Identity: WebServer: pool01. net.tcp</span><span class="sxs-lookup"><span data-stu-id="6bee0-112">Identity : WebServer:pool01.contoso.net</span></span>

<span data-ttu-id="6bee0-113">FileStore: FileStore: dc01. net</span><span class="sxs-lookup"><span data-stu-id="6bee0-113">FileStore : FileStore:dc01.contoso.net</span></span>

<span data-ttu-id="6bee0-114">UserServer: UserServer: pool01. net</span><span class="sxs-lookup"><span data-stu-id="6bee0-114">UserServer : UserServer:pool01.contoso.net</span></span>

<span data-ttu-id="6bee0-115">PrimaryHttpPort:80</span><span class="sxs-lookup"><span data-stu-id="6bee0-115">PrimaryHttpPort : 80</span></span>

<span data-ttu-id="6bee0-116">PrimaryHttpsPort: 443</span><span class="sxs-lookup"><span data-stu-id="6bee0-116">PrimaryHttpsPort : 443</span></span>

<span data-ttu-id="6bee0-117">ExternalHttpPort: 8080</span><span class="sxs-lookup"><span data-stu-id="6bee0-117">ExternalHttpPort : 8080</span></span>

<span data-ttu-id="6bee0-118">ExternalHttpsPort: 4443</span><span class="sxs-lookup"><span data-stu-id="6bee0-118">ExternalHttpsPort : 4443</span></span>

<span data-ttu-id="6bee0-119">PublishedPrimaryHttpPort:80</span><span class="sxs-lookup"><span data-stu-id="6bee0-119">PublishedPrimaryHttpPort : 80</span></span>

<span data-ttu-id="6bee0-120">PublishedPrimaryHttpsPort: 443</span><span class="sxs-lookup"><span data-stu-id="6bee0-120">PublishedPrimaryHttpsPort : 443</span></span>

<span data-ttu-id="6bee0-121">PublishedExternalHttpPort:80</span><span class="sxs-lookup"><span data-stu-id="6bee0-121">PublishedExternalHttpPort : 80</span></span>

<span data-ttu-id="6bee0-122">PublishedExternalHttpsPort: 443</span><span class="sxs-lookup"><span data-stu-id="6bee0-122">PublishedExternalHttpsPort : 443</span></span>

<span data-ttu-id="6bee0-123">ReachPrimaryPsomServerPort: 8060</span><span class="sxs-lookup"><span data-stu-id="6bee0-123">ReachPrimaryPsomServerPort : 8060</span></span>

<span data-ttu-id="6bee0-124">ReachExternalPsomServerPort: 8061</span><span class="sxs-lookup"><span data-stu-id="6bee0-124">ReachExternalPsomServerPort : 8061</span></span>

<span data-ttu-id="6bee0-125">AppSharingPortStart: 49152</span><span class="sxs-lookup"><span data-stu-id="6bee0-125">AppSharingPortStart : 49152</span></span>

<span data-ttu-id="6bee0-126">AppSharingPortCount: 16383</span><span class="sxs-lookup"><span data-stu-id="6bee0-126">AppSharingPortCount : 16383</span></span>

<span data-ttu-id="6bee0-127">LIServiceInternalUri: https://internalweb.contoso.net/locationinformation/liservice.svc</span><span class="sxs-lookup"><span data-stu-id="6bee0-127">LIServiceInternalUri : https://internalweb.contoso.net/locationinformation/liservice.svc</span></span>

<span data-ttu-id="6bee0-128">Abハンドラ Internaluri: https://internalweb.contoso.net/abs/handler</span><span class="sxs-lookup"><span data-stu-id="6bee0-128">ABHandlerInternalUri : https://internalweb.contoso.net/abs/handler</span></span>

<span data-ttu-id="6bee0-129">Abハンドラ Externaluri: https://csweb.contoso.com/abs/handler</span><span class="sxs-lookup"><span data-stu-id="6bee0-129">ABHandlerExternalUri : https://csweb.contoso.com/abs/handler</span></span>

<span data-ttu-id="6bee0-130">Dlのお持ちの Uri: https://internalweb.contoso.net/groupexpansion/service.svc</span><span class="sxs-lookup"><span data-stu-id="6bee0-130">DLExpansionInternalUri : https://internalweb.contoso.net/groupexpansion/service.svc</span></span>

<span data-ttu-id="6bee0-131">Dlの外部の Uri: https://csweb.contoso.com/groupexpansion/service.svc</span><span class="sxs-lookup"><span data-stu-id="6bee0-131">DLExpansionExternalUri : https://csweb.contoso.com/groupexpansion/service.svc</span></span>

<span data-ttu-id="6bee0-132">Caハンドラ Internaluri: https://internalweb.contoso.net/CertProv/CertProvisioningService.svc</span><span class="sxs-lookup"><span data-stu-id="6bee0-132">CAHandlerInternalUri : https://internalweb.contoso.net/CertProv/CertProvisioningService.svc</span></span>

<span data-ttu-id="6bee0-133">CAHandlerInternalAnonUri : http://internalweb.contoso.net/CertProv/CertProvisioningService.svc</span><span class="sxs-lookup"><span data-stu-id="6bee0-133">CAHandlerInternalAnonUri : http://internalweb.contoso.net/CertProv/CertProvisioningService.svc</span></span>

<span data-ttu-id="6bee0-134">他のコンテンツ: https://internalweb.contoso.net/CollabContent</span><span class="sxs-lookup"><span data-stu-id="6bee0-134">CollabContentInternalUri : https://internalweb.contoso.net/CollabContent</span></span>

<span data-ttu-id="6bee0-135">他のコンテンツ: https://csweb.contoso.com/CollabContent</span><span class="sxs-lookup"><span data-stu-id="6bee0-135">CollabContentExternalUri : https://csweb.contoso.com/CollabContent</span></span>

<span data-ttu-id="6bee0-136">Caハンドラ Externaluri: https://csweb.contoso.com/CertProv/CertProvisioningService.svc</span><span class="sxs-lookup"><span data-stu-id="6bee0-136">CAHandlerExternalUri : https://csweb.contoso.com/CertProv/CertProvisioningService.svc</span></span>

<span data-ttu-id="6bee0-137">DeviceUpdateDownloadInternalUri: https://internalweb.contoso.net/RequestHandler/ucdevice.upx</span><span class="sxs-lookup"><span data-stu-id="6bee0-137">DeviceUpdateDownloadInternalUri : https://internalweb.contoso.net/RequestHandler/ucdevice.upx</span></span>

<span data-ttu-id="6bee0-138">DeviceUpdateDownloadExternalUri : https://csweb.contoso.com/RequestHandlerExt/ucdevice.upx</span><span class="sxs-lookup"><span data-stu-id="6bee0-138">DeviceUpdateDownloadExternalUri : https://csweb.contoso.com/RequestHandlerExt/ucdevice.upx</span></span>

<span data-ttu-id="6bee0-139">DeviceUpdateStoreInternalUri: http://internalweb.contoso.net/RequestHandler/Files</span><span class="sxs-lookup"><span data-stu-id="6bee0-139">DeviceUpdateStoreInternalUri : http://internalweb.contoso.net/RequestHandler/Files</span></span>

<span data-ttu-id="6bee0-140">DeviceUpdateStoreExternalUri: https://csweb.contoso.com/RequestHandlerExt/Files</span><span class="sxs-lookup"><span data-stu-id="6bee0-140">DeviceUpdateStoreExternalUri : https://csweb.contoso.com/RequestHandlerExt/Files</span></span>

<span data-ttu-id="6bee0-141">RgsAgentServiceInternalUri : https://internalweb.contoso.net/RgsClients/AgentService.svc</span><span class="sxs-lookup"><span data-stu-id="6bee0-141">RgsAgentServiceInternalUri : https://internalweb.contoso.net/RgsClients/AgentService.svc</span></span>

<span data-ttu-id="6bee0-142">RgsAgentServiceExternalUri : https://csweb.contoso.com/RgsClients/AgentService.svc</span><span class="sxs-lookup"><span data-stu-id="6bee0-142">RgsAgentServiceExternalUri : https://csweb.contoso.com/RgsClients/AgentService.svc</span></span>

<span data-ttu-id="6bee0-143">MeetExternalUri : https://csweb.contoso.com/Meet</span><span class="sxs-lookup"><span data-stu-id="6bee0-143">MeetExternalUri : https://csweb.contoso.com/Meet</span></span>

<span data-ttu-id="6bee0-144">ダイヤルイン Externaluri: https://csweb.contoso.com/Dialin</span><span class="sxs-lookup"><span data-stu-id="6bee0-144">DialinExternalUri : https://csweb.contoso.com/Dialin</span></span>

<span data-ttu-id="6bee0-145">CscpInternalUri : https://internalweb.contoso.net/Cscp</span><span class="sxs-lookup"><span data-stu-id="6bee0-145">CscpInternalUri : https://internalweb.contoso.net/Cscp</span></span>

<span data-ttu-id="6bee0-146">ReachExternalUri : https://csweb.contoso.com/Reach</span><span class="sxs-lookup"><span data-stu-id="6bee0-146">ReachExternalUri : https://csweb.contoso.com/Reach</span></span>

<span data-ttu-id="6bee0-147">ReachInternalUri : https://internalweb.contoso.net/Reach</span><span class="sxs-lookup"><span data-stu-id="6bee0-147">ReachInternalUri : https://internalweb.contoso.net/Reach</span></span>

<span data-ttu-id="6bee0-148">WebTicketExternalUri : https://csweb.contoso.com/WebTicket/WebTicketService.svc</span><span class="sxs-lookup"><span data-stu-id="6bee0-148">WebTicketExternalUri : https://csweb.contoso.com/WebTicket/WebTicketService.svc</span></span>

<span data-ttu-id="6bee0-149">WebTicketInternalUri : https://internalweb.contoso.net/WebTicket/WebTicketService.svc</span><span class="sxs-lookup"><span data-stu-id="6bee0-149">WebTicketInternalUri : https://internalweb.contoso.net/WebTicket/WebTicketService.svc</span></span>

<span data-ttu-id="6bee0-150">ExternalFqdn: csweb.contoso.com</span><span class="sxs-lookup"><span data-stu-id="6bee0-150">ExternalFqdn : csweb.contoso.com</span></span>

<span data-ttu-id="6bee0-151">InternalFqdn: internalweb.contoso.net</span><span class="sxs-lookup"><span data-stu-id="6bee0-151">InternalFqdn : internalweb.contoso.net</span></span>

<span data-ttu-id="6bee0-152">DependentServiceList: {レジストラー: pool01. net、ConferencingServer: pool01. net}</span><span class="sxs-lookup"><span data-stu-id="6bee0-152">DependentServiceList : {Registrar:pool01.contoso.net, ConferencingServer:pool01.contoso.net}</span></span>

<span data-ttu-id="6bee0-153">ServiceId: 1-1-1</span><span class="sxs-lookup"><span data-stu-id="6bee0-153">ServiceId : 1-WebServices-1</span></span>

<span data-ttu-id="6bee0-154">SiteId: サイト: レドモンド</span><span class="sxs-lookup"><span data-stu-id="6bee0-154">SiteId : Site:Redmond</span></span>

<span data-ttu-id="6bee0-155">PoolFqdn: pool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="6bee0-155">PoolFqdn : pool01.contoso.net</span></span>

<span data-ttu-id="6bee0-156">バージョン: 5</span><span class="sxs-lookup"><span data-stu-id="6bee0-156">Version : 5</span></span>

<span data-ttu-id="6bee0-157">役割: WebServer</span><span class="sxs-lookup"><span data-stu-id="6bee0-157">Role : WebServer</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="6bee0-158">関連項目</span><span class="sxs-lookup"><span data-stu-id="6bee0-158">See Also</span></span>


[<span data-ttu-id="6bee0-159">CsService の入手</span><span class="sxs-lookup"><span data-stu-id="6bee0-159">Get-CsService</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsService)  
  

<span data-ttu-id="6bee0-160"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6bee0-160"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

