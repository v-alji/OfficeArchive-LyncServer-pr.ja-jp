---
title: 'Lync Server 2013: (オプション) DTMF コマンドの主要なマッピングを変更する'
description: 'Lync Server 2013: (省略可能) DTMF コマンドのキーマッピングを変更します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: (Optional) Modify key mapping for DTMF commands
ms:assetid: d753b78d-400c-4df2-957f-e7576b2019c2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398943(v=OCS.15)
ms:contentKeyID: 48185563
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7581001c31d929163962378a8734435f6d07c6c8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424892"
---
# <a name="optional-modify-key-mapping-for-dtmf-commands-in-lync-server-2013"></a><span data-ttu-id="bdb3a-103">(オプション) Lync Server 2013 で DTMF コマンドの主要なマッピングを変更する</span><span class="sxs-lookup"><span data-stu-id="bdb3a-103">(Optional) Modify key mapping for DTMF commands in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bdb3a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bdb3a-104">

<span> </span></span></span>

<span data-ttu-id="bdb3a-105">_**最終更新日:** 2012-09-30_</span><span class="sxs-lookup"><span data-stu-id="bdb3a-105">_**Topic Last Modified:** 2012-09-30_</span></span>

<span data-ttu-id="bdb3a-106">ダイヤルイン会議のユーザーは、電話キーパッドのキーを押して、デュアルトーン多重周波数 (DTMF) のコマンドを実行できます。</span><span class="sxs-lookup"><span data-stu-id="bdb3a-106">Dial-in conferencing users can press keys on the telephone keypad to perform dual-tone multi-frequency (DTMF) commands.</span></span> <span data-ttu-id="bdb3a-107">DTMF コマンドを使用すると、会議にダイヤルインするユーザーは、電話のキーパッドを使用して会議設定 (自身をミュートおよびミュート解除したり、会議をロックおよびロック解除したりするなど) を制御できます。</span><span class="sxs-lookup"><span data-stu-id="bdb3a-107">DTMF commands enable users who dial in to a conference to control conference settings (such as muting and unmuting themselves or locking and unlocking the conference) by using the keypad on their telephone.</span></span> <span data-ttu-id="bdb3a-108">コマンドレットを使用して、DTMF コマンドに使用されるキーを変更できます。</span><span class="sxs-lookup"><span data-stu-id="bdb3a-108">You can use cmdlets to modify the keys used for the DTMF commands.</span></span> <span data-ttu-id="bdb3a-109">この手順は省略可能です。</span><span class="sxs-lookup"><span data-stu-id="bdb3a-109">This step is optional.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="bdb3a-110">これらのコマンドレットと、使用可能な DTMF オプションの詳細については、「Lync Server 管理シェルのドキュメント」または「Lync Server 管理シェルのコマンドラインのヘルプ」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bdb3a-110">For details about these cmdlets and the possible DTMF options, see Lync Server Management Shell documentation or Lync Server Management Shell command-line Help.</span></span>



</div>

<div>

## <a name="to-modify-the-key-mapping-of-dtmf-commands"></a><span data-ttu-id="bdb3a-111">DTMF コマンドのキーマッピングを変更するには</span><span class="sxs-lookup"><span data-stu-id="bdb3a-111">To modify the key mapping of DTMF commands</span></span>

1.  <span data-ttu-id="bdb3a-112">**RTCUniversalServerAdmins** グループのメンバーとして、または **Cs-Serveradministrator** または **csadministrator** の役割のメンバーとしてコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="bdb3a-112">Log on to the computer as a member of the **RTCUniversalServerAdmins** group, or as a member of the **Cs-ServerAdministrator** or **CsAdministrator** role.</span></span>

2.  <span data-ttu-id="bdb3a-113">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="bdb3a-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="bdb3a-114">コマンド プロンプトで次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="bdb3a-114">Run the following at the command prompt:</span></span>
    
        Get-CsDialinConferencingDtmfConfiguration
    
    <span data-ttu-id="bdb3a-115">このコマンドレットは、ダイヤルイン会議で使用される DTMF 設定を返します。</span><span class="sxs-lookup"><span data-stu-id="bdb3a-115">This cmdlet returns the DTMF settings used for dial-in conferencing.</span></span>

4.  <span data-ttu-id="bdb3a-116">次のコマンドレットを実行し、変更する各オプションに対して押すキーを指定します。</span><span class="sxs-lookup"><span data-stu-id="bdb3a-116">Run the following cmdlet and specify the key to be pressed for each option that you want to change:</span></span>
    
        Set-CsDialinConferencingDtmfConfiguration [-Identity <global or site collection to be changed>]
        [-AdmitAll <default key is 8>] [-AudienceMuteCommand <default key is 4>]
        [-CommandCharacter <* (default) | #>] [-EnableDisableAnnouncementsCommand <default key is 9>]
        [-HelpCommand <default key is 1>] [-LockUnlockConferenceCommand <default key is 7>]
        [-MuteUnmuteCommand <default key is 6>] [-PrivateRollCallCommand <default key is 3>]
    
    <span data-ttu-id="bdb3a-117">このコマンドレットは、ダイヤルイン会議で使用される DTMF 設定を変更します。</span><span class="sxs-lookup"><span data-stu-id="bdb3a-117">This cmdlet modifies the DTMF settings used for dial-in conferencing.</span></span>
    
    <span data-ttu-id="bdb3a-118">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="bdb3a-118">For example:</span></span>
    
        Set-CsDialinConferencingDtmfConfiguration -EnableDisableAnnouncementsCommand 4 -AudienceMuteCommand 9
    
    <span data-ttu-id="bdb3a-119">次の例では、押されたキーを入れ替えて、アナウンスメントを有効または無効にします。キーを押すと、すべての参加者をミュートおよびミュート解除することができます。</span><span class="sxs-lookup"><span data-stu-id="bdb3a-119">This example swaps the key that is pressed to enable or disable announcements and the key that is pressed to mute and unmute all participants.</span></span> <span data-ttu-id="bdb3a-120">Id が指定されていないため、これらの変更はグローバルな DTMF 設定に適用されます。</span><span class="sxs-lookup"><span data-stu-id="bdb3a-120">Because no Identity is specified, these changes apply to the global DTMF settings.</span></span>

5.  <span data-ttu-id="bdb3a-121">(オプション) 特定サイトに対する DTMF コマンドの追加セットを作成するには、サイト ID と **New-CsDialinConferencingDtmfConfiguration** コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="bdb3a-121">(Optional) To create additional sets of DTMF commands for specific sites, use the **New-CsDialinConferencingDtmfConfiguration** cmdlet with a site identity.</span></span> <span data-ttu-id="bdb3a-122">サイトの新たな DTMF 設定を作成すると、そのサイト設定はグローバル設定よりも優先されるようになります。</span><span class="sxs-lookup"><span data-stu-id="bdb3a-122">When you create new DTMF settings for sites, the site settings take precedence over the global settings.</span></span> <span data-ttu-id="bdb3a-123">詳細については、「Lync Server 管理シェルのドキュメント」または「Lync Server 管理シェルのコマンドラインのヘルプ」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bdb3a-123">For details, see Lync Server Management Shell documentation or Lync Server Management Shell command-line Help.</span></span>

<span data-ttu-id="bdb3a-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bdb3a-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

