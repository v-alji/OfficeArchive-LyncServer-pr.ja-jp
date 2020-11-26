---
title: 'Lync Server 2013: サイトレベルでホストされるボイスメールポリシーを作成する'
description: 'Lync Server 2013: サイトレベルでホストされるボイスメールのポリシーを作成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create a site-level hosted voice mail policy
ms:assetid: 145892c8-a6ca-45fb-9e83-786f709dd775
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398216(v=OCS.15)
ms:contentKeyID: 48183481
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8cd578359a8d20562e8887b61b86d53332e6f8d8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432115"
---
# <a name="create-a-site-level-hosted-voice-mail-policy-in-lync-server-2013"></a><span data-ttu-id="63c01-103">Lync Server 2013 でサイトレベルでホストされるボイスメールのポリシーを作成する</span><span class="sxs-lookup"><span data-stu-id="63c01-103">Create a site-level hosted voice mail policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="63c01-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="63c01-104">

<span> </span></span></span>

<span data-ttu-id="63c01-105">_**最終更新日:** 2012-09-24_</span><span class="sxs-lookup"><span data-stu-id="63c01-105">_**Topic Last Modified:** 2012-09-24_</span></span>

<span data-ttu-id="63c01-106">*サイト* ポリシーは、ポリシーが定義されているサイトをホームにしているすべてのユーザーに影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="63c01-106">A *site* policy can impact all users that are homed on the site for which the policy is defined.</span></span> <span data-ttu-id="63c01-107">ユーザーがホストされた Exchange UM アクセス用に構成されていて、ユーザーごとのポリシーが割り当てられていない場合は、サイトポリシーが適用されます。</span><span class="sxs-lookup"><span data-stu-id="63c01-107">If a user is configured for hosted Exchange UM access and has not been assigned a Per-user policy, the site policy applies.</span></span> <span data-ttu-id="63c01-108">サイトポリシーを展開していない場合は、グローバルポリシーが適用されます。</span><span class="sxs-lookup"><span data-stu-id="63c01-108">If you have not deployed a site policy, the global policy applies.</span></span>

<span data-ttu-id="63c01-109">サイトポリシーの構成の詳細については、次のコマンドレットの Lync Server 管理シェルに関するドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="63c01-109">For details about configuring site policies, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - [<span data-ttu-id="63c01-110">New-CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="63c01-110">New-CsHostedVoicemailPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsHostedVoicemailPolicy)

  - [<span data-ttu-id="63c01-111">Set-CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="63c01-111">Set-CsHostedVoicemailPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsHostedVoicemailPolicy)

  - [<span data-ttu-id="63c01-112">Get-CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="63c01-112">Get-CsHostedVoicemailPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsHostedVoicemailPolicy)

<div>

## <a name="to-create-a-site-hosted-voice-mail-policy"></a><span data-ttu-id="63c01-113">サイトでホストされているボイスメールポリシーを作成するには</span><span class="sxs-lookup"><span data-stu-id="63c01-113">To create a site hosted voice mail policy</span></span>

1.  <span data-ttu-id="63c01-114">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="63c01-114">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="63c01-115">New-CsHostedVoicemailPolicy コマンドレットを実行して、ポリシーを作成します。</span><span class="sxs-lookup"><span data-stu-id="63c01-115">Run the New-CsHostedVoicemailPolicy cmdlet to create the policy.</span></span> <span data-ttu-id="63c01-116">たとえば、以下を実行します。</span><span class="sxs-lookup"><span data-stu-id="63c01-116">For example, run:</span></span>
    
        New-CsHostedVoicemailPolicy -Identity site:Redmond -Destination ExUM.fabrikam.com -Description "Hosted voice mail policy for the Redmond site." -Organization "corp1.litwareinc.com, corp2.litwareinc.com"
    
    <span data-ttu-id="63c01-117">この例では、サイトのスコープを持つホストされたボイスメールのポリシーを作成し、次のパラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="63c01-117">This example creates a hosted voice mail policy with site scope, and sets the following parameters:</span></span>
    
      - <span data-ttu-id="63c01-118">**Id** は、スコープを含むポリシーの一意の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="63c01-118">**Identity** specifies a unique identifier for the policy, which includes the scope.</span></span> <span data-ttu-id="63c01-119">サイトのスコープを持つポリシーの場合、Id パラメーターの値を形式で指定する必要があり `site:` *\<name\>* `site:Redmond` ます。</span><span class="sxs-lookup"><span data-stu-id="63c01-119">For a policy with site scope, the Identity parameter value must be specified in the format `site:`*\<name\>*, for example, `site:Redmond`.</span></span>
    
      - <span data-ttu-id="63c01-120">[ **Destination** ] は、ホストされた Exchange UM サービスの完全修飾ドメイン名 (FQDN) を指定します。</span><span class="sxs-lookup"><span data-stu-id="63c01-120">**Destination** specifies the fully qualified domain name (FQDN) of the hosted Exchange UM service.</span></span> <span data-ttu-id="63c01-121">このパラメーターは省略可能ですが、ホストされたボイスメールに対してユーザーを有効にしようとしても、ユーザーに割り当てられているポリシーに送信先の値がない場合、有効にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="63c01-121">This parameter is optional, but if you attempt to enable a user for hosted voice mail and the user’s assigned policy does not have a Destination value, the enable will fail.</span></span>
    
      - <span data-ttu-id="63c01-122">**説明** ポリシーに関するオプションの説明情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="63c01-122">**Description** provides optional descriptive information about the policy.</span></span>
    
      - <span data-ttu-id="63c01-123">[**組織**] は、Lync Server 2013 のホームユーザーである Exchange テナントのコンマ区切りリストを指定します。</span><span class="sxs-lookup"><span data-stu-id="63c01-123">**Organization** specifies a comma-separated list of the Exchange tenants that home Lync Server 2013 users.</span></span> <span data-ttu-id="63c01-124">各テナントは、ホストされた Exchange UM サービスでそのテナントの FQDN として指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="63c01-124">Each tenant must be specified as the FQDN of that tenant on the hosted Exchange UM service.</span></span>

<span data-ttu-id="63c01-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="63c01-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

