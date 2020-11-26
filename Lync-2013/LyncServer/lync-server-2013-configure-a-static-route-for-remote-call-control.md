---
title: 'Lync Server 2013: リモート通話コントロールの静的ルートの構成'
description: 'Lync Server 2013: リモート通話コントロールの静的ルートを構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure a static route for remote call control
ms:assetid: f7003023-443d-48ee-989b-71e8b0b0abbd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615051(v=OCS.15)
ms:contentKeyID: 48185855
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8ecf6478d4fb7ab4f04f8a452d4837b327ba254a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434208"
---
# <a name="configure-a-static-route-for-remote-call-control-in-lync-server-2013"></a><span data-ttu-id="71f71-103">Lync Server 2013 でのリモート通話コントロールの静的ルートの構成</span><span class="sxs-lookup"><span data-stu-id="71f71-103">Configure a static route for remote call control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="71f71-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="71f71-104">

<span> </span></span></span>

<span data-ttu-id="71f71-105">_**最終更新日:** 2012-09-22_</span><span class="sxs-lookup"><span data-stu-id="71f71-105">_**Topic Last Modified:** 2012-09-22_</span></span>

<span data-ttu-id="71f71-106">リモート通話コントロールでは、すべての Lync Server プールが、そのプールからプライベートブランチ exchange (PBX) に接続する SIP/CSTA ゲートウェイへのパスを使用するように構成されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="71f71-106">Remote call control requires that every Lync Server pool is configured with a path from that pool to the SIP/CSTA gateway that connects to the private branch exchange (PBX).</span></span> <span data-ttu-id="71f71-107">このパスを使用するには、各プールに1つずつの静的ルートが必要です。各ゲートウェイは、PBX への通話に関連付けられた SIP コールコントロールメッセージをプロキシします。</span><span class="sxs-lookup"><span data-stu-id="71f71-107">This path requires that each pool has one static route for each gateway to which the pool will proxy SIP call control messages associated with calls to the PBX.</span></span> <span data-ttu-id="71f71-108">リモート通話コントロール用にグローバル静的ルートを構成する場合、プールレベルで静的ルートを使用して構成されていない各プールは、グローバル静的ルートを使用します。</span><span class="sxs-lookup"><span data-stu-id="71f71-108">If you configure a global static route for remote call control, each pool that is not configured with a static route at the pool level will use the global static route.</span></span>

<div>

## <a name="to-configure-a-static-route-for-remote-call-control"></a><span data-ttu-id="71f71-109">リモート通話コントロールの静的ルートを構成するには</span><span class="sxs-lookup"><span data-stu-id="71f71-109">To configure a static route for remote call control</span></span>

1.  <span data-ttu-id="71f71-110">Lync Server 管理シェルが RTCUniversalServerAdmins グループのメンバーとしてインストールされているコンピューター、または **新しい CsStaticRoute** コマンドレットを割り当てたロールベースのアクセス制御 (RBAC) ロールとしてログオンします。</span><span class="sxs-lookup"><span data-stu-id="71f71-110">Log on to a computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or a role-based access control (RBAC) role to which you have assigned the **New-CsStaticRoute** cmdlet.</span></span>

2.  <span data-ttu-id="71f71-111">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="71f71-111">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="71f71-112">静的ルートを作成して、変数 $TLSRoute または $TCPRoute に配置するには、次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="71f71-112">To create a static route and put it in the variable $TLSRoute or $TCPRoute, do one of the following:</span></span>
    
    <div class="">
    

    > [!TIP]  
    > <span data-ttu-id="71f71-113">ドメインの子ドメインと一致させるには、MatchUri パラメーターでワイルドカード値を指定します。</span><span class="sxs-lookup"><span data-stu-id="71f71-113">To match child domains of a domain, you can specify a wildcard value in the MatchUri parameter.</span></span> <span data-ttu-id="71f71-114">たとえば、 <STRONG>contoso.net</STRONG>のようになります。</span><span class="sxs-lookup"><span data-stu-id="71f71-114">For example, <STRONG>\*.contoso.net</STRONG>.</span></span> <span data-ttu-id="71f71-115">この値は、サフィックス <STRONG>contoso.net</STRONG>で終わるドメインと一致します。</span><span class="sxs-lookup"><span data-stu-id="71f71-115">That value matches any domain that ends with the suffix <STRONG>contoso.net</STRONG>.</span></span>

    
    </div>
    
      - <span data-ttu-id="71f71-116">トランスポート層セキュリティ (TLS) 接続の場合は、コマンドプロンプトで次を入力します。</span><span class="sxs-lookup"><span data-stu-id="71f71-116">For a Transport Layer Security (TLS) connection, type the following at the command prompt:</span></span>
        
        ```powershell
        $TLSRoute = New-CsStaticRoute -TLSRoute -Destination <gateway FQDN> -Port <gateway SIP listening port> -UseDefaultCertificate $true -MatchUri <destination domain>
        ```
        <span data-ttu-id="71f71-117">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="71f71-117">For example:</span></span>
        ```powershell
        $TLSRoute = New-CsStaticRoute -TLSRoute -Destination rccgateway.contoso.net -Port 5065 -UseDefaultCertificate $true -MatchUri *.contoso.net
        ```
        <span data-ttu-id="71f71-118">UseDefaultCertificate が False に設定されている場合は、TLSCertIssuer パラメーターと TLSCertSerialNumber パラメーターを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="71f71-118">If UseDefaultCertificate is set to False, you must specify TLSCertIssuer and TLSCertSerialNumber parameters.</span></span> <span data-ttu-id="71f71-119">これらのパラメーターは、静的ルートで使用された証明書を発行した証明機関 (CA) の名前と、その TLS 証明書のシリアル番号を示します。</span><span class="sxs-lookup"><span data-stu-id="71f71-119">These parameters indicate the name of the certification authority (CA) that issued the certificate used in the static route, and the serial number of that TLS certificate, respectively.</span></span> <span data-ttu-id="71f71-120">これらのパラメーターの詳細については、コマンドプロンプトで次を入力して、「Lync Server 管理シェルのヘルプ」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="71f71-120">For details about these parameters, see Lync Server Management Shell Help by typing the following at the command prompt:</span></span>
        ```powershell
        Get-Help New-CsStaticRoute -Full
        ```
      - <span data-ttu-id="71f71-121">伝送制御プロトコル (TCP) 接続の場合は、コマンドプロンプトで次を入力します。</span><span class="sxs-lookup"><span data-stu-id="71f71-121">For a Transmission Control Protocol (TCP) connection, type the following at the command prompt:</span></span>
        
        <div class="">
        

        > [!NOTE]  
        > <span data-ttu-id="71f71-122">完全修飾ドメイン名 (FQDN) を指定した場合は、ドメインネームシステム (DNS) で最初にレコードを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="71f71-122">If you specify a fully qualified domain name (FQDN), you must configure a Domain Name System (DNS) A record first.</span></span>

        
        </div>
        
        ```powershell
        $TCPRoute = New-CsStaticRoute -TCPRoute -Destination <gateway IP address or FQDN> -Port <gateway SIP listening port> -MatchUri <destination domain>
        ```
        <span data-ttu-id="71f71-123">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="71f71-123">For example:</span></span>
        ```powershell
        $TCPRoute = New-CsStaticRoute -TCPRoute -Destination 192.168.0.240 -Port 5065 -MatchUri *.contoso.net
        ```
        <span data-ttu-id="71f71-124">静的ルートのオプションパラメーターには、次の既定値があります。</span><span class="sxs-lookup"><span data-stu-id="71f71-124">The following are default values for optional parameters for static routes:</span></span>
        
          - <span data-ttu-id="71f71-125">Enabled = True</span><span class="sxs-lookup"><span data-stu-id="71f71-125">Enabled = True</span></span>
        
          - <span data-ttu-id="71f71-126">MatchOnlyPhoneUri = False</span><span class="sxs-lookup"><span data-stu-id="71f71-126">MatchOnlyPhoneUri = False</span></span>
        
          - <span data-ttu-id="71f71-127">ReplaceHostInRequestUri = False</span><span class="sxs-lookup"><span data-stu-id="71f71-127">ReplaceHostInRequestUri = False</span></span>
        
        <span data-ttu-id="71f71-128">これらの既定値は変更しないことを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="71f71-128">We strongly recommend that you do not change these default values.</span></span> <span data-ttu-id="71f71-129">ただし、これらのパラメーターを変更する必要がある場合は、コマンドプロンプトで次を入力して、「Lync Server 管理シェルのヘルプ」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="71f71-129">However, if you must change any of these parameters, see Lync Server Management Shell Help by typing the following at the command prompt:</span></span>
        ```powershell
        Get-Help New-CsStaticRoute -Full
        ```
4.  <span data-ttu-id="71f71-130">新しく作成された静的ルートを中央管理ストアで保持するには、必要に応じて次のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="71f71-130">To persist a newly created static route in the Central Management store, run one of the following, as appropriate:</span></span>
    
       ```powershell
        Set-CsStaticRoutingConfiguration -Route @{Add=$TLSRoute}
       ```
    
       ```powershell
        Set-CsStaticRoutingConfiguration -Route @{Add=$TCPRoute}
       ```

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="71f71-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="71f71-131">See Also</span></span>


[<span data-ttu-id="71f71-132">Lync Server 2013 でリモート通話コントロールの信頼済みアプリケーション エントリを構成する</span><span class="sxs-lookup"><span data-stu-id="71f71-132">Configure a trusted application entry for remote call control in Lync Server 2013</span></span>](lync-server-2013-configure-a-trusted-application-entry-for-remote-call-control.md)  
[<span data-ttu-id="71f71-133">Lync Server 2013 での SIP/CSTA ゲートウェイの IP アドレスの定義</span><span class="sxs-lookup"><span data-stu-id="71f71-133">Define a SIP/CSTA gateway IP address in Lync Server 2013</span></span>](lync-server-2013-define-a-sip-csta-gateway-ip-address.md)  
  

<span data-ttu-id="71f71-134"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="71f71-134"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

