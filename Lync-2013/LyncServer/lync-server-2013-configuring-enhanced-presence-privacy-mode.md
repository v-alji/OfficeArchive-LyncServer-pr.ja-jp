---
title: 'Lync Server 2013: 拡張プレゼンスプライバシーモードを構成する'
description: 'Lync Server 2013: 拡張プレゼンスプライバシーモードを構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring enhanced presence privacy mode
ms:assetid: e7a6b873-486d-4dfb-a967-c48f61f237f3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399028(v=OCS.15)
ms:contentKeyID: 48185664
ms.date: 12/09/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c8eab347d233c23a9a4becf119dee673d3021dfa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433172"
---
# <a name="configuring-enhanced-presence-privacy-mode-in-lync-server-2013"></a><span data-ttu-id="4ead0-103">Lync Server 2013 で拡張プレゼンスプライバシーモードを構成する</span><span class="sxs-lookup"><span data-stu-id="4ead0-103">Configuring enhanced presence privacy mode in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4ead0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4ead0-104">

<span> </span></span></span>

<span data-ttu-id="4ead0-105">_**最終更新日:** 2014-12-08_</span><span class="sxs-lookup"><span data-stu-id="4ead0-105">_**Topic Last Modified:** 2014-12-08_</span></span>

<span data-ttu-id="4ead0-106">強化されたプレゼンスプライバシーモードでは、ユーザーは自分のプレゼンス情報を、Lync 2013 の連絡先リストに記載されている連絡先だけに表示されるように制限することができます。</span><span class="sxs-lookup"><span data-stu-id="4ead0-106">With enhanced presence privacy mode, users can restrict their presence information so that it is visible only to the contacts listed in their Lync 2013 Contacts list.</span></span> <span data-ttu-id="4ead0-107">**CsPrivacyConfiguration** と **CsPrivacyConfiguration** コマンドレットには、このオプションを制御する enableprivacymode パラメーターがあります。</span><span class="sxs-lookup"><span data-stu-id="4ead0-107">The **New-CsPrivacyConfiguration** and **Set-CsPrivacyConfiguration** cmdlets have an EnablePrivacyMode parameter controls this option.</span></span> <span data-ttu-id="4ead0-108">EnablePrivacyMode が True に設定されている場合、連絡先にプレゼンス情報を制限するオプションは Lync 2013 の [状態] オプションで利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="4ead0-108">When EnablePrivacyMode is set to True, the option to restrict presence information to contacts becomes available in the Lync 2013 Status options.</span></span> <span data-ttu-id="4ead0-109">EnablePrivacyMode が False に設定されている場合、ユーザーは自分のプレゼンス情報の表示を常に許可するか、管理者がプライバシーモードに加えた将来の変更に従うかを選ぶことができます。</span><span class="sxs-lookup"><span data-stu-id="4ead0-109">When EnablePrivacyMode is set to False, users can choose either to always allow everyone to see their presence information or to adhere to any future changes the administrator makes to the privacy mode.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="4ead0-110">Lync 2013 および Lync 2010 のプライバシー設定は、以前のバージョン (Microsoft Office Communicator 2007 R2 または Microsoft Office Communicator 2007) には有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="4ead0-110">Lync 2013 and Lync 2010 privacy settings are not honored by previous versions (Microsoft Office Communicator 2007 R2 or Microsoft Office Communicator 2007).</span></span> <span data-ttu-id="4ead0-111">以前のバージョンの Office Communicator でサインインが許可されている場合、Lync 2013 ユーザーの状態、連絡先情報、または画像を表示する権限が与えられていないユーザーは写真を表示できます。</span><span class="sxs-lookup"><span data-stu-id="4ead0-111">If previous versions of Office Communicator are allowed to sign in, a Lync 2013 user’s status, contact information, or picture could be viewed by someone who has not been authorized to view it.</span></span> <span data-ttu-id="4ead0-112">さらに、後で以前のバージョンの Communicator でサインインした場合は、Lync 2013 ユーザーのプライバシー設定がリセットされます。</span><span class="sxs-lookup"><span data-stu-id="4ead0-112">Additionally, a Lync 2013 user’s privacy settings are reset if he or she later signs in with previous version of Communicator.</span></span><BR><span data-ttu-id="4ead0-113">これらの理由から、拡張プレゼンスプライバシーモードを有効にする前に、移行シナリオで次のようにします。</span><span class="sxs-lookup"><span data-stu-id="4ead0-113">For these reasons, in a migration scenario, before you enable enhanced presence privacy mode:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="4ead0-114">すべてのユーザーに Lync 2013 がインストールされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4ead0-114">Ensure that every user has Lync 2013 installed.</span></span></P>
> <LI>
> <P><span data-ttu-id="4ead0-115">以前のバージョンの Communicator でサインインできないように、クライアントのバージョンポリシールールを定義します。</span><span class="sxs-lookup"><span data-stu-id="4ead0-115">Define a client version policy rule to prevent previous versions of Communicator from signing in.</span></span></P></LI></UL>



</div>

<div>

## <a name="to-enable-enhanced-presence-privacy-mode"></a><span data-ttu-id="4ead0-116">拡張プレゼンスプライバシーモードを有効にするには</span><span class="sxs-lookup"><span data-stu-id="4ead0-116">To enable enhanced presence privacy mode</span></span>

1.  <span data-ttu-id="4ead0-117">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="4ead0-117">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="4ead0-118">次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="4ead0-118">Run the following command:</span></span>
    
        Get-CsPrivacyConfiguration | Set-CsPrivacyConfiguration -EnablePrivacyMode $True
    
    <span data-ttu-id="4ead0-119">このコマンドにより、組織で現在使用されているすべてのプライバシー構成設定のプライバシーモードが有効になります。</span><span class="sxs-lookup"><span data-stu-id="4ead0-119">This command enables privacy mode for all the privacy configuration settings currently in use in the organization.</span></span> <span data-ttu-id="4ead0-120">Lync Server の機能強化されたプレゼンスプライバシーモードのポリシー構成で Lync 2013 クライアントの連絡先プレゼンスを管理する方法の詳細については、Microsoft サポート技術情報の記事「 [Lync Server の拡張プレゼンスプライバシーモードを有効にする」を参照してください。 lync の連絡先のプレゼンス状態が [利用不可] に更新](https://support.microsoft.com/kb/3020057)されます。</span><span class="sxs-lookup"><span data-stu-id="4ead0-120">For more information about how the Lync Server enhanced presence privacy mode policy configurations manages contact presence for the Lync 2013 client, see the Microsoft KB article [Enabling Lync Server enhanced presence privacy mode updates the presence status of some Lync contacts to "unavailable"](https://support.microsoft.com/kb/3020057).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="4ead0-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="4ead0-121">See Also</span></span>


[<span data-ttu-id="4ead0-122">Get-CsPrivacyConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ead0-122">Get-CsPrivacyConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsPrivacyConfiguration)  
[<span data-ttu-id="4ead0-123">新規-CsPrivacyConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ead0-123">New-CsPrivacyConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsPrivacyConfiguration)  
[<span data-ttu-id="4ead0-124">Set-CsPrivacyConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ead0-124">Set-CsPrivacyConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsPrivacyConfiguration)  
  

<span data-ttu-id="4ead0-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4ead0-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

