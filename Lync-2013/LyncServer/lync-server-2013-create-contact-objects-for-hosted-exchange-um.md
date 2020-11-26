---
title: 'Lync Server 2013: Hosted Exchange UM の連絡先オブジェクトの作成'
description: 'Lync Server 2013: ホスティングされている Exchange UM の連絡先オブジェクトを作成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create contact objects for hosted Exchange UM
ms:assetid: a39be52f-488a-4523-ad5f-ce1f0d681959
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412765(v=OCS.15)
ms:contentKeyID: 48185045
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c9760e2a39b5182f9b5194e364e059bddc6a63d2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431975"
---
# <a name="create-contact-objects-for-hosted-exchange-um-in-lync-server-2013"></a><span data-ttu-id="24dd8-103">Lync Server 2013 での Hosted Exchange UM の連絡先オブジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="24dd8-103">Create contact objects for hosted Exchange UM in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="24dd8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="24dd8-104">

<span> </span></span></span>

<span data-ttu-id="24dd8-105">_**最終更新日:** 2012-09-24_</span><span class="sxs-lookup"><span data-stu-id="24dd8-105">_**Topic Last Modified:** 2012-09-24_</span></span>

<span data-ttu-id="24dd8-106">次の手順では、ホストされた Exchange ユニファイドメッセージング (UM) 用に自動応答 (AA) または加入者アクセス (SA) 連絡先オブジェクトを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="24dd8-106">The following procedure explains how to create Auto Attendant (AA) or Subscriber Access (SA) contact objects for hosted Exchange Unified Messaging (UM).</span></span>

<span data-ttu-id="24dd8-107">詳細については、計画ドキュメントの「 [Lync Server 2013 での Hosted Exchange Contact object management](lync-server-2013-hosted-exchange-contact-object-management.md) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="24dd8-107">For details, see [Hosted Exchange Contact object management in Lync Server 2013](lync-server-2013-hosted-exchange-contact-object-management.md) in the Planning documentation.</span></span>

<span data-ttu-id="24dd8-108">連絡先オブジェクトの構成の詳細については、次のコマンドレットの Lync Server 管理シェルに関するドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="24dd8-108">For details about configuring contact objects, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - [<span data-ttu-id="24dd8-109">New-CsExUmContact</span><span class="sxs-lookup"><span data-stu-id="24dd8-109">New-CsExUmContact</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsExUmContact)

  - [<span data-ttu-id="24dd8-110">Set-CsExUmContact</span><span class="sxs-lookup"><span data-stu-id="24dd8-110">Set-CsExUmContact</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsExUmContact)

<div class=" ">


> [!IMPORTANT]  
> <span data-ttu-id="24dd8-111">Lync Server 2013 連絡先オブジェクトをホストされた Exchange UM に対して有効にする前に、それらに適用されるホストされたボイスメールポリシーを展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="24dd8-111">Before Lync Server 2013 contact objects can be enabled for hosted Exchange UM, a hosted voice mail policy that applies to them must be deployed.</span></span> <span data-ttu-id="24dd8-112">詳細については、「 <A href="lync-server-2013-hosted-voice-mail-policies.md">Lync Server 2013 のホスト型ボイスメールポリシー</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="24dd8-112">For details, see <A href="lync-server-2013-hosted-voice-mail-policies.md">Hosted voice mail policies in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-create-aa-or-sa-contact-objects-for-hosted-exchange-um"></a><span data-ttu-id="24dd8-113">Hosted Exchange UM 用の AA または SA の連絡先オブジェクトを作成するには</span><span class="sxs-lookup"><span data-stu-id="24dd8-113">To create AA or SA contact objects for hosted Exchange UM</span></span>

1.  <span data-ttu-id="24dd8-114">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="24dd8-114">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="24dd8-115">New-CsExUmContact コマンドレットを実行して、展開に必要な連絡先オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="24dd8-115">Run the New-CsExUmContact cmdlet to create any contact objects required for your deployment.</span></span> <span data-ttu-id="24dd8-116">たとえば、次のように実行して AA と SA の連絡先オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="24dd8-116">For example, run the following to create an AA and an SA contact object:</span></span>
    
       ```powershell
        New-CsExUmContact -SipAddress "sip:exumaa1@fabrikam.com" -RegistrarPool "RedmondPool.litwareinc.com" -OU "HostedExUM Integration" -DisplayNumber "+14255550101" -AutoAttendant $True
       ```
    
       ```powershell
        New-CsExUmContact -SipAddress "sip:exumsa1@fabrikam.com" -RegistrarPool "RedmondPool.litwareinc.com" -OU "HostedExUM Integration" -DisplayNumber "+14255550101"
       ```
    
    <span data-ttu-id="24dd8-117">これらの例では、次のパラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="24dd8-117">These examples set the following parameters:</span></span>
    
      - <span data-ttu-id="24dd8-118">**SipAddress** 連絡先オブジェクトの SIP アドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="24dd8-118">**SipAddress** specifies the SIP address of the contact object.</span></span> <span data-ttu-id="24dd8-119">これは、Active Directory ドメインサービスでユーザーまたは連絡先オブジェクトを構成するためにまだ使用されていないアドレスである必要があります。</span><span class="sxs-lookup"><span data-stu-id="24dd8-119">This must be an address that has not already been used to configure a user or contact object in Active Directory Domain Services.</span></span> <span data-ttu-id="24dd8-120">この値は、前の例のように "sip:" の形式で指定する必要があり \<*SIP address*\> ます。</span><span class="sxs-lookup"><span data-stu-id="24dd8-120">This value must be in the format “sip:\<*SIP address*\>“ as shown in the previous examples.</span></span>
    
      - <span data-ttu-id="24dd8-121">**RegistrarPool** は、レジストラーサービスが実行されているプールの完全修飾ドメイン名 (FQDN) を指定します。</span><span class="sxs-lookup"><span data-stu-id="24dd8-121">**RegistrarPool** specifies the fully qualified domain name (FQDN) of the pool on which the Registrar service is running.</span></span>
        
        <div class=" ">
        

        > [!NOTE]  
        > <span data-ttu-id="24dd8-122">Lync server 2013 より前の Lync Server 2013 展開の一部であるプールに Exchange UM 連絡先オブジェクトを移動することはできません。</span><span class="sxs-lookup"><span data-stu-id="24dd8-122">Exchange UM contact objects cannot be moved to pools that are part of Lync Server 2013 deployments prior to Lync Server 2013.</span></span>

        
        </div>
    
      - <span data-ttu-id="24dd8-123">**OU** この連絡先オブジェクトを配置する Active Directory の組織単位を指定します。</span><span class="sxs-lookup"><span data-stu-id="24dd8-123">**OU** specifies the Active Directory organizational unit where this contact object will be located.</span></span>
    
      - <span data-ttu-id="24dd8-124">**Displaynumber** 連絡先オブジェクトの電話番号を指定します。</span><span class="sxs-lookup"><span data-stu-id="24dd8-124">**DisplayNumber** specifies the telephone number of the contact object.</span></span> <span data-ttu-id="24dd8-125">各連絡先オブジェクトの電話番号は一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="24dd8-125">The phone number for each contact object must be unique.</span></span>
    
      - <span data-ttu-id="24dd8-126">**Autoattendant** 連絡先オブジェクトが自動応答かどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="24dd8-126">**AutoAttendant** specifies whether the Contact object is an Auto Attendant.</span></span> <span data-ttu-id="24dd8-127">自動応答では、発信者が電話システムを移動して、連絡を希望する当事者に連絡できるようにする一連の音声プロンプトが用意されています。</span><span class="sxs-lookup"><span data-stu-id="24dd8-127">Auto Attendant provides a set of voice prompts that allow callers to navigate the phone system and reach the party that they want to contact.</span></span> <span data-ttu-id="24dd8-128">このパラメーターの値が **False** (既定値) の場合、サブスクライバーアクセスの contact オブジェクトが示されます。</span><span class="sxs-lookup"><span data-stu-id="24dd8-128">A value of **False** (the default) for this parameter indicates a Subscriber Access contact object.</span></span>

<span data-ttu-id="24dd8-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="24dd8-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

