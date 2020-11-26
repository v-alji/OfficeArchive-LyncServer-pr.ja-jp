---
title: A/V エッジサーバーのサービス品質ポリシーを構成する
description: A/V エッジサーバーのサービス品質ポリシーを構成します。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring a Quality of Service policy for your A/V Edge Servers
ms:assetid: 119ee1f5-45b9-40ba-98e5-c694dd2fc5c2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204681(v=OCS.15)
ms:contentKeyID: 48183444
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1ec1f012260aa32df984925a86882a3201e07db0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433508"
---
# <a name="configuring-a-quality-of-service-policy-for-your-av-edge-servers-in-lync-server-2013"></a><span data-ttu-id="230be-103">Lync Server 2013 での、A/V エッジサーバーのサービス品質ポリシーの構成</span><span class="sxs-lookup"><span data-stu-id="230be-103">Configuring a Quality of Service policy for your A/V Edge Servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="230be-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="230be-104">

<span> </span></span></span>

<span data-ttu-id="230be-105">_**最終更新日:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="230be-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="230be-106">会議、アプリケーション、および仲介サーバーの QoS ポリシーの作成に加えて、A/V エッジサーバーの内部側のオーディオとビデオの両方のポリシーも作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="230be-106">In addition to creating QoS policies for your Conferencing, Application, and Mediation servers, you must also create both audio and video policies for the internal side of your A/V Edge servers.</span></span> <span data-ttu-id="230be-107">ただし、エッジサーバーで使用されるポリシーは、会議、アプリケーション、および仲介サーバーで使われるポリシーとは異なります。</span><span class="sxs-lookup"><span data-stu-id="230be-107">However, the policies used on your Edge servers are different from the policies used on your Conferencing, Application, and Mediation servers.</span></span> <span data-ttu-id="230be-108">会議、アプリケーション、および仲介サーバーの場合、ソースポートの範囲を指定しました。エッジサーバーでは、宛先ポートの範囲を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="230be-108">For the Conferencing, Application, and Mediation servers you specified a source port range; with Edge servers, you need to specify a destination port range.</span></span> <span data-ttu-id="230be-109">このため、会議、アプリケーション、および仲介サーバーの QoS ポリシーをエッジサーバーに適用することはできません。これらのポリシーは、単に機能しません。</span><span class="sxs-lookup"><span data-stu-id="230be-109">Because of that you cannot simply apply the Conferencing, Application, and Mediation server QoS policies to your Edge servers: these policies simply won't work.</span></span> <span data-ttu-id="230be-110">代わりに、新しいポリシーを作成して、それらのポリシーを Edge サーバーのみに適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="230be-110">Instead, you must create new policies and apply those policies to your Edge servers only.</span></span>

<span data-ttu-id="230be-111">次の手順では、エッジサーバー上のサービスの品質を管理するために使用できる Active Directory グループポリシーオブジェクトを作成するプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="230be-111">The following procedure describes the process for creating Active Directory Group Policy objects that can be used to manage Quality of Service on Edge Servers.</span></span> <span data-ttu-id="230be-112">ただし、エッジサーバーがスタンドアロンサーバーであり、Active Directory アカウントを持っていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="230be-112">Of course, it's possible that your Edge servers are stand-alone servers that do not have Active Directory accounts.</span></span> <span data-ttu-id="230be-113">このような場合は、Active Directory グループポリシーの代わりにローカルグループポリシーを使用できます。唯一の違いは、ローカルグループポリシーエディターを使ってこれらのローカルポリシーを作成する必要があります。また、各エッジサーバー上で同じポリシーセットを個別に作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="230be-113">If that's the case, you can use local Group Policy instead of Active Directory Group Policy: the only difference is that you must create these local policies using the Local Group Policy Editor, and must individually create the same set of policies on each Edge Server.</span></span> <span data-ttu-id="230be-114">エッジサーバーでローカルグループポリシーエディターを起動するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="230be-114">To start the Local Group Policy Editor on an Edge server do the following:</span></span>

1.  <span data-ttu-id="230be-115">[ **スタート** ] をクリックし、[ **実行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="230be-115">Click **Start** and then click **Run**.</span></span>

2.  <span data-ttu-id="230be-116">[ **実行** ] ダイアログボックスで、「 **gpedit.msc** 」と入力し、enter キーを押します。</span><span class="sxs-lookup"><span data-stu-id="230be-116">In the **Run** dialog box, type **gpedit.msc** and then press ENTER.</span></span>

<span data-ttu-id="230be-117">Active Directory ベースのポリシーを作成する場合は、グループポリシー管理がインストールされているコンピューターにログオンする必要があります。</span><span class="sxs-lookup"><span data-stu-id="230be-117">If you are creating Active Directory-based policies, then you should log on to a computer where Group Policy Management has been installed.</span></span> <span data-ttu-id="230be-118">その場合は、[グループポリシーの管理] を開き ([ **スタート**] をクリックし、[ **管理ツール**] をポイントして、[ **グループポリシーの管理**] をクリックし)、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="230be-118">In that case, open Group Policy Management (click **Start**, point to **Administrative Tools**, and then click **Group Policy Management**) and then complete the following steps:</span></span>

1.  <span data-ttu-id="230be-119">[グループポリシーの管理] で、新しいポリシーを作成するコンテナーを見つけます。</span><span class="sxs-lookup"><span data-stu-id="230be-119">In Group Policy Management, locate the container where the new policy should be created.</span></span> <span data-ttu-id="230be-120">たとえば、すべての Lync Server コンピューターが Lync Server という名前の OU にある場合、新しいポリシーは Lync Server OU で作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="230be-120">For example, if all your Lync Server computers are located in an OU named Lync Server then the new policy should be created in the Lync Server OU.</span></span>

2.  <span data-ttu-id="230be-121">適切なコンテナーを右クリックし、[ **このドメインに GPO を作成**] をクリックして、ここにリンクを設定します。</span><span class="sxs-lookup"><span data-stu-id="230be-121">Right-click the appropriate container and then click **Create a GPO in this domain, and Link it here**.</span></span>

3.  <span data-ttu-id="230be-122">[ **新しい GPO** ] ダイアログボックスで、[ **名前** ] ボックスに新しいグループポリシーオブジェクトの名前を入力し (「 **Lync Server Audio**」など)、[ **OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="230be-122">In the **New GPO** dialog box, type a name for the new Group Policy object in the **Name** box (for example, **Lync Server Audio**) and then click **OK**.</span></span>

4.  <span data-ttu-id="230be-123">新しく作成したポリシーを右クリックし、[ **編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="230be-123">Right-click the newly-created policy and then click **Edit**.</span></span>

<span data-ttu-id="230be-124">ここからは、Active Directory ポリシーとローカルポリシーのどちらを作成するかに関係なく、プロセスは同じになります。</span><span class="sxs-lookup"><span data-stu-id="230be-124">From here the process is identical regardless of whether you are creating an Active Directory policy or a local policy:</span></span>

1.  <span data-ttu-id="230be-125">グループポリシー管理エディターまたはローカルグループポリシーエディターで、[ **コンピューターの構成**]、[ **ポリシー**]、[ **Windows 設定**] の順に展開し、[ **ポリシーベースの QoS**] を右クリックして、[ **新しいポリシーの作成**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="230be-125">In the Group Policy Management Editor or the Local Group Policy Editor, expand **Computer Configuration**, expand **Policies**, expand **Windows Settings**, right-click **Policy-based QoS**, and then click **Create new policy**.</span></span>

2.  <span data-ttu-id="230be-126">[**ポリシーベースの QoS** ] ダイアログボックスの [開く] ページで、[**名前**] ボックスに新しいポリシーの名前を入力します (例: **Lync Server Audio**)。</span><span class="sxs-lookup"><span data-stu-id="230be-126">In the **Policy-based QoS** dialog box, on the opening page, type a name for the new policy (e.g., **Lync Server Audio**) in the **Name** box.</span></span> <span data-ttu-id="230be-127">[ **DSCP 値の指定** ] を選択し、値を **46** に設定します。</span><span class="sxs-lookup"><span data-stu-id="230be-127">Select **Specify DSCP Value** and set the value to **46**.</span></span> <span data-ttu-id="230be-128">[ **送信スロットルの比率を指定する** ] をオフにして、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="230be-128">Leave **Specify Outbound Throttle Rate** unselected, and then click **Next**.</span></span>

3.  <span data-ttu-id="230be-129">次のページで、[すべての **アプリケーション** ] が選択されていることを確認し、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="230be-129">On the next page, make sure that **All applications** is selected and then click **Next**.</span></span> <span data-ttu-id="230be-130">この設定は、特定のアプリケーションによって作成されたパケットだけでなく、すべてのパケットを検索して46の DSCP マークを付けて、ネットワークに指示します。</span><span class="sxs-lookup"><span data-stu-id="230be-130">This setting instructs the network to look for all packets with a DSCP marking of 46, not just packets created by a specific application.</span></span>

4.  <span data-ttu-id="230be-131">3番目のページで、 **すべてのソース ip** アドレスと **宛先 ip アドレス** が選択されていることを確認し、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="230be-131">On the third page, make sure that both **Any source IP address** and **Any destination IP address** are selected and then click **Next**.</span></span> <span data-ttu-id="230be-132">この2つの設定では、どのコンピューター (IP アドレス) がそれらのパケットを送信したか、どのコンピューター (IP アドレス) がそれらのパケットを受信するかに関係なく、パケットが管理されるようにします。</span><span class="sxs-lookup"><span data-stu-id="230be-132">These two settings ensure that packets will be managed regardless of which computer (IP address) sent those packets and which computer (IP address) will receive those packets.</span></span>

5.  <span data-ttu-id="230be-133">4ページ目で、[**この QoS ポリシーが適用されるプロトコルを選択** してください] ドロップダウンリストから [ **TCP および UDP** ] を選びます。</span><span class="sxs-lookup"><span data-stu-id="230be-133">On page four, select **TCP and UDP** from the **Select the protocol this QoS policy applies to** dropdown list.</span></span> <span data-ttu-id="230be-134">TCP (伝送制御プロトコル) と UDP (ユーザーデータグラムプロトコル) は、Lync Server およびそのクライアントアプリケーションで最も一般的に使用される2つのネットワークプロトコルです。</span><span class="sxs-lookup"><span data-stu-id="230be-134">TCP (Transmission Control Protocol) and UDP (User Datagram Protocol) are the two networking protocols most-commonly used by Lync Server and its client applications.</span></span>

6.  <span data-ttu-id="230be-135">見出しの下で、 **宛先ポート番号を指定** して、[ **この宛先ポートまたは範囲から**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="230be-135">Under the heading **Specify the destination port number**, select **From this destination port or range**.</span></span> <span data-ttu-id="230be-136">[付随するテキスト] ボックスに、オーディオ送信用に予約されているポート範囲を入力します。</span><span class="sxs-lookup"><span data-stu-id="230be-136">In the accompanying text box, type the port range reserved for audio transmissions.</span></span> <span data-ttu-id="230be-137">たとえば、ポート49152からオーディオトラフィック用にポート57500を予約した場合、次の形式を使用してポート範囲を入力し **49152:57500** ます。</span><span class="sxs-lookup"><span data-stu-id="230be-137">For example, if you reserved ports 49152 through ports 57500 for audio traffic then enter the port range using this format: **49152:57500**.</span></span> <span data-ttu-id="230be-138">[**完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="230be-138">Click **Finish**.</span></span>

<span data-ttu-id="230be-139">オーディオトラフィックの QoS ポリシーを作成したら、ビデオトラフィック用に2つ目のポリシーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="230be-139">After you have created the QoS policy for audio traffic you should create a second policy for video traffic.</span></span> <span data-ttu-id="230be-140">ビデオのポリシーを作成するには、オーディオポリシーを作成する場合と同じ基本的な手順に従い、次のように置き換えます。</span><span class="sxs-lookup"><span data-stu-id="230be-140">To create a policy for video, follow the same basic procedure you followed when creating the audio policy, making these substitutions:</span></span>

  - <span data-ttu-id="230be-141">別の (一意の) ポリシー名 (「 **Lync Server Video**」など) を使用します。</span><span class="sxs-lookup"><span data-stu-id="230be-141">Use a different (and unique) policy name (for example, **Lync Server Video**).</span></span>

  - <span data-ttu-id="230be-142">DSCP 値を46ではなく、 **34** に設定します。</span><span class="sxs-lookup"><span data-stu-id="230be-142">Set the DSCP value to **34** instead of 46.</span></span> <span data-ttu-id="230be-143">(DSCP 値34は使う必要がないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="230be-143">(Note that you do not have to use a DSCP value of 34.</span></span> <span data-ttu-id="230be-144">唯一の要件は、オーディオに使用したものとは異なる DSCP 値をビデオに使用することです。</span><span class="sxs-lookup"><span data-stu-id="230be-144">The only requirement is that you use a different DSCP value for video than you used for audio.)</span></span>

  - <span data-ttu-id="230be-145">以前に構成したポート範囲をビデオトラフィックに使用します。</span><span class="sxs-lookup"><span data-stu-id="230be-145">Use the previously-configured port range for video traffic.</span></span> <span data-ttu-id="230be-146">たとえば、57501 ~ 65535 のビデオ用の予約ポートがある場合は、ポート範囲 **57501:65535** を次のように設定します。</span><span class="sxs-lookup"><span data-stu-id="230be-146">For example, if you have reserved ports 57501 through 65535 for video, then set the port range to this: **57501:65535**.</span></span> <span data-ttu-id="230be-147">この場合も、送信先ポートの範囲として構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="230be-147">Again, this should be configured as the destination port range.</span></span>

<span data-ttu-id="230be-148">アプリケーション共有トラフィックを管理するためのポリシーを作成する場合は、3番目のポリシーを作成し、次のように置き換えます。</span><span class="sxs-lookup"><span data-stu-id="230be-148">If you decide to create a policy for managing application sharing traffic you must create a third policy, making the following substitutions:</span></span>

  - <span data-ttu-id="230be-149">別の (一意の) ポリシー名 (「 **Lync Server アプリケーション共有**」など) を使用します。</span><span class="sxs-lookup"><span data-stu-id="230be-149">Use a different (and unique) policy name (for example, **Lync Server Application Sharing**).</span></span>

  - <span data-ttu-id="230be-150">DSCP 値を46の代わりに **24** に設定します。</span><span class="sxs-lookup"><span data-stu-id="230be-150">Set the DSCP value to **24** instead of 46.</span></span> <span data-ttu-id="230be-151">(この場合も、DSCP 値24を使用する必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="230be-151">(Again, you do not have to use a DSCP value of 24.</span></span> <span data-ttu-id="230be-152">唯一の要件として、アプリケーション共有には、オーディオまたはビデオに使用したのとは異なる DSCP 値を使用します。</span><span class="sxs-lookup"><span data-stu-id="230be-152">The only requirement is that you use a different DSCP value for application sharing than you used for audio or for video.)</span></span>

  - <span data-ttu-id="230be-153">以前に構成したポート範囲をビデオトラフィックに使用します。</span><span class="sxs-lookup"><span data-stu-id="230be-153">Use the previously-configured port range for video traffic.</span></span> <span data-ttu-id="230be-154">たとえば、アプリケーション共有用にポート 40803 ~ 49151 を予約している場合は、ポート範囲 **40803:49151** を次のように設定します。</span><span class="sxs-lookup"><span data-stu-id="230be-154">For example, if you have reserved ports 40803 through 49151 for application sharing, then set the port range to this: **40803:49151**.</span></span>

<span data-ttu-id="230be-155">作成した新しいポリシーは、エッジサーバーのグループポリシーが更新されるまで有効になりません。</span><span class="sxs-lookup"><span data-stu-id="230be-155">The new policies you have created will not take effect until Group Policy has been refreshed on your Edge servers.</span></span> <span data-ttu-id="230be-156">グループ ポリシーは定期的に自動更新されますが、グループ ポリシーを更新する必要がある各コンピューター上で次のコマンドを実行すると、即座に強制的に更新することができます。</span><span class="sxs-lookup"><span data-stu-id="230be-156">Although Group Policy periodically refreshes on its own, you can force an immediate refresh by running the following command on each computer where Group Policy needs to be refreshed:</span></span>

    Gpudate.exe /force

<span data-ttu-id="230be-157">このコマンドは、Lync Server 内から、または管理者の資格情報で実行されているコマンドウィンドウから実行できます。</span><span class="sxs-lookup"><span data-stu-id="230be-157">This command can be run from within the Lync Server or from any command window that is running under administrator credentials.</span></span> <span data-ttu-id="230be-158">管理者の資格情報のもとでコマンド ウィンドウを開くには、[**スタート**] メニューをクリックし、[**コマンド プロンプト**] を右クリックして、[**管理者として実行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="230be-158">To run a command window under administrator credentials, click **Start**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span> <span data-ttu-id="230be-159">Gpudate.exe を実行した後でも、エッジサーバーの再起動が必要になることがあります。</span><span class="sxs-lookup"><span data-stu-id="230be-159">Note that you might need to restart the Edge server even after running Gpudate.exe.</span></span>

<span data-ttu-id="230be-160">ネットワークパケットが適切な DSCP 値でマークされていることを確認するには、次の手順に従って、各コンピューターに新しいレジストリエントリを作成する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="230be-160">To help ensure that network packets are marked with the appropriate DSCP value, you should also create a new registry entry on each computer by completing the following procedure:</span></span>

1.  <span data-ttu-id="230be-161">[ **スタート** ] をクリックし、[ **実行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="230be-161">Click **Start** and then click **Run**.</span></span>

2.  <span data-ttu-id="230be-162">[ **実行** ] ダイアログボックスで、「 **regedit** 」と入力し、enter キーを押します。</span><span class="sxs-lookup"><span data-stu-id="230be-162">In the **Run** dialog box, type **regedit** and then press ENTER.</span></span>

3.  <span data-ttu-id="230be-163">レジストリエディターで、[ **HKEY \_ ローカル \_ コンピューター**]、[ **システム**]、[ **CurrentControlSet**] の順に展開し、[ **サービス**] を展開して、[ **Tcpip**] を展開します。</span><span class="sxs-lookup"><span data-stu-id="230be-163">In the Registry Editor, expand **HKEY\_LOCAL\_MACHINE**, expand **SYSTEM**, expand **CurrentControlSet**, expand **services**, and then expand **Tcpip**.</span></span>

4.  <span data-ttu-id="230be-164">[ **Tcpip**] を右クリックし、[ **新規作成**] をポイントして、[ **キー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="230be-164">Right-click **Tcpip**, point to **New**, and then click **Key**.</span></span> <span data-ttu-id="230be-165">新しいレジストリキーが作成されたら、「 **QoS** 」と入力し、enter キーを押してキーの名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="230be-165">After the new registry key is created, type **QoS** and then press ENTER to rename the key.</span></span>

5.  <span data-ttu-id="230be-166">[ **QoS**] を右クリックし、[ **新規作成**] をポイントして、[ **文字列値**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="230be-166">Right-click **QoS**, point to **New**, and then click **String Value**.</span></span> <span data-ttu-id="230be-167">新しいレジストリ値が作成されたら、[ **NLA を使用しない** ] と入力し、enter キーを押して値の名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="230be-167">After the new registry value is created, type **Do not use NLA** and then press ENTER to rename the value.</span></span>

6.  <span data-ttu-id="230be-168">[実行し **ない] を** ダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="230be-168">Double-click **Do no use NLA**.</span></span> <span data-ttu-id="230be-169">[**文字列の編集**] ダイアログボックスで、[**値のデータ**] ボックスに「 **1** 」と入力し、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="230be-169">In the **Edit String** dialog box, type **1** in the **Value data** box and then click **OK**.</span></span>

7.  <span data-ttu-id="230be-170">レジストリエディターを終了し、コンピューターを再起動します。</span><span class="sxs-lookup"><span data-stu-id="230be-170">Close the Registry Editor and then reboot your computer.</span></span>

<span data-ttu-id="230be-171"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="230be-171"></div>

<span> </span>

</div>

</div>

</span></span></div>

