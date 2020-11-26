---
title: 'Lync Server 2013: 翻訳ルールを手動で作成または変更する'
description: 'Lync Server 2013: 翻訳ルールを手動で作成または変更します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a translation rule manually
ms:assetid: 049d1db3-af58-48c5-be89-52e1d068a4bd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398099(v=OCS.15)
ms:contentKeyID: 48183276
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4f393ca1983e072090cc27d47b142dace8b566c5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431737"
---
# <a name="create-or-modify-a-translation-rule-manually-in-lync-server-2013"></a><span data-ttu-id="b525c-103">Lync Server 2013 で翻訳ルールを手動で作成または変更する</span><span class="sxs-lookup"><span data-stu-id="b525c-103">Create or modify a translation rule manually in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b525c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b525c-104">

<span> </span></span></span>

<span data-ttu-id="b525c-105">_**最終更新日:** 2012-08-06_</span><span class="sxs-lookup"><span data-stu-id="b525c-105">_**Topic Last Modified:** 2012-08-06_</span></span>

<span data-ttu-id="b525c-106">一致するパターンと翻訳ルールの正規表現を作成して、翻訳ルールを定義する場合は、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b525c-106">Follow these steps if you want to define a translation rule by writing a regular expression for the matching pattern and translation rule.</span></span> <span data-ttu-id="b525c-107">または、[ **翻訳ルール** ツールのビルド] ツールで一連の値を入力し、Lync Server コントロールパネルを有効にして、対応する照合パターンと翻訳ルールを生成することもできます。</span><span class="sxs-lookup"><span data-stu-id="b525c-107">Alternatively, you can enter a set of values in the **Build a Translation Rule** tool and enable Lync Server Control Panel to generate the corresponding matching pattern and translation rule for you.</span></span> <span data-ttu-id="b525c-108">詳細については、「 [Lync Server 2013 の翻訳ルールの作成ツールを使用して、翻訳ルールを作成または変更](lync-server-2013-create-or-modify-a-translation-rule-by-using-the-build-a-translation-rule-tool.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b525c-108">For details, see [Create or modify a translation rule by using the Build a Translation Rule tool in Lync Server 2013](lync-server-2013-create-or-modify-a-translation-rule-by-using-the-build-a-translation-rule-tool.md).</span></span>

<div>

## <a name="to-define-a-translation-rule-manually"></a><span data-ttu-id="b525c-109">変換ルールを手動で定義するには</span><span class="sxs-lookup"><span data-stu-id="b525c-109">To define a translation rule manually</span></span>

1.  <span data-ttu-id="b525c-110">RTCUniversalServerAdmins グループのメンバーとして、あるいは CsVoiceAdministrator、CsServerAdministrator、または CsAdministrator の役割のメンバーとしてコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="b525c-110">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="b525c-111">詳細については、「 [Lync Server 2013 でセットアップのアクセス許可を委任](lync-server-2013-delegate-setup-permissions.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b525c-111">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="b525c-112">ブラウザーウィンドウを開き、管理 URL を入力して Lync Server コントロールパネルを開きます。</span><span class="sxs-lookup"><span data-stu-id="b525c-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="b525c-113">Lync Server コントロールパネルを起動するために使用できるさまざまな方法について詳しくは、「 [Lync server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="b525c-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="b525c-114">翻訳ルールの定義を開始するには、「 [Lync server 2013 でメディアバイパスを使用してトランクを構成](lync-server-2013-configure-a-trunk-with-media-bypass.md) する」を参照するか、「 [lync server 2013 でメディアをバイパスしないトランクを構成](lync-server-2013-configure-a-trunk-without-media-bypass.md) する」の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="b525c-114">To begin defining a translation rule, follow the steps in [Configure a trunk with media bypass in Lync Server 2013](lync-server-2013-configure-a-trunk-with-media-bypass.md) through step 10 or [Configure a trunk without media bypass in Lync Server 2013](lync-server-2013-configure-a-trunk-without-media-bypass.md) through step 9.</span></span>

4.  <span data-ttu-id="b525c-115">[**新しい変換ルール**] ページまたは [**変換ルールの編集**] ページの [**名前**] フィールドに、変換対象の番号パターンを説明する名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="b525c-115">In the **Name** field on the **New Translation Rule** or **Edit Translation Rule** page, type a name that describes the number pattern being translated.</span></span>

5.  <span data-ttu-id="b525c-116">(オプション) [**説明**] に、「**US International long-distance dialing**」など、変換ルールの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="b525c-116">(Optional) In **Description**, type a description of the translation rule, for example **US International long-distance dialing**.</span></span>

6.  <span data-ttu-id="b525c-117">[**変換ルールの構築**] セクションの一番下にある [**編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b525c-117">Click **Edit** at the bottom of the **Build a Translation Rule** section.</span></span>

7.  <span data-ttu-id="b525c-118">[**正規表現の入力**] で次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="b525c-118">Enter the following in **Type a Regular Expression**:</span></span>
    
      - <span data-ttu-id="b525c-119">[**このパターンと一致**] に、変換する番号を照合するために使用するパターンを指定します。</span><span class="sxs-lookup"><span data-stu-id="b525c-119">In **Match this pattern**, specify the pattern that will be used to match the numbers to be translated.</span></span>
    
      - <span data-ttu-id="b525c-120">[**変換ルール**] に、変換される番号の形式のパターンを指定します。</span><span class="sxs-lookup"><span data-stu-id="b525c-120">In **Translation rule**, specify a pattern for the format of translated numbers.</span></span>
    
    <span data-ttu-id="b525c-121">たとえば、「 **^ \\ + ( \\ d {9} \\ d +) $** 」と入力すると (**このパターン** と **011 $ 1** の **翻訳ルール** が適用されます)、ルールは + 441235551010 から011441235551010に変換されます。</span><span class="sxs-lookup"><span data-stu-id="b525c-121">For example, if you enter **^\\+(\\d{9}\\d+)$** in **Match this pattern** and **011$1** in **Translation rule**, the rule will translate +441235551010 to 011441235551010.</span></span>

8.  <span data-ttu-id="b525c-122">[**OK**] をクリックして変換ルールを保存します。</span><span class="sxs-lookup"><span data-stu-id="b525c-122">Click **OK** to save the translation rule.</span></span>

9.  <span data-ttu-id="b525c-123">[**OK**] をクリックしてトランク構成を保存します。</span><span class="sxs-lookup"><span data-stu-id="b525c-123">Click **OK** to save the trunk configuration.</span></span>

10. <span data-ttu-id="b525c-124">[**トランク構成**] ページで [**確定**] をクリックして、[**すべて確定**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b525c-124">On the **Trunk Configuration** page, click **Commit**, and then click **Commit all**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="b525c-125">変換ルールを作成または変更したときは必ず、[<STRONG>すべて確定</STRONG>] コマンドを実行して構成の変更を公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b525c-125">Whenever you create or modify a translation rule, you must run the <STRONG>Commit all</STRONG> command to publish the configuration change.</span></span> <span data-ttu-id="b525c-126">詳細については、「操作のドキュメントで「 <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">Lync Server 2013 のボイスルーティング構成に保留中の変更を発行する</A> 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b525c-126">For details, see <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">Publish pending changes to the voice routing configuration in Lync Server 2013</A> in the Operations documentation.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="b525c-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="b525c-127">See Also</span></span>


[<span data-ttu-id="b525c-128">Lync Server 2013 の翻訳ルールの作成ツールを使用して、翻訳ルールを作成または変更する</span><span class="sxs-lookup"><span data-stu-id="b525c-128">Create or modify a translation rule by using the Build a Translation Rule tool in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-translation-rule-by-using-the-build-a-translation-rule-tool.md)  
[<span data-ttu-id="b525c-129">Configure a trunk with media bypass in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b525c-129">Configure a trunk with media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-with-media-bypass.md)  
[<span data-ttu-id="b525c-130">Lync Server 2013 でメディアをバイパスせずにトランクを構成する</span><span class="sxs-lookup"><span data-stu-id="b525c-130">Configure a trunk without media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-without-media-bypass.md)  
[<span data-ttu-id="b525c-131">Lync Server 2013 の音声ルーティング構成に保留中の変更を発行する</span><span class="sxs-lookup"><span data-stu-id="b525c-131">Publish pending changes to the voice routing configuration in Lync Server 2013</span></span>](lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md)  


[<span data-ttu-id="b525c-132">Lync Server 2013 のグローバルメディアバイパスオプション</span><span class="sxs-lookup"><span data-stu-id="b525c-132">Global media bypass options in Lync Server 2013</span></span>](lync-server-2013-global-media-bypass-options.md)  
  

<span data-ttu-id="b525c-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b525c-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

