---
title: 'Lync Server 2013: Windows 7 または Windows 8 で実行されているクライアントのサービス品質ポリシーを構成する'
description: 'Lync Server 2013: Windows 7 または Windows 8 で実行されているクライアントのサービス品質ポリシーを構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Quality of Service policies for clients running on Windows 7 or Windows 8
ms:assetid: efff2b98-b3fb-4183-a4f0-329a9105ce2c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205371(v=OCS.15)
ms:contentKeyID: 48185785
ms.date: 03/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: faba5fc54ef73bfc738f94ee7209fc46a7cdc208
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432696"
---
# <a name="configuring-quality-of-service-policies-in-lync-server-2013-for-clients-running-on-windows-7-or-windows-8"></a><span data-ttu-id="8ec3f-103">Windows 7 または Windows 8 で実行しているクライアントのために Lync Server 2013 でサービスの品質ポリシーを構成する</span><span class="sxs-lookup"><span data-stu-id="8ec3f-103">Configuring Quality of Service policies in Lync Server 2013 for clients running on Windows 7 or Windows 8</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8ec3f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8ec3f-104">

<span> </span></span></span>

<span data-ttu-id="8ec3f-105">_**最終更新日:** 2016-03-29_</span><span class="sxs-lookup"><span data-stu-id="8ec3f-105">_**Topic Last Modified:** 2016-03-29_</span></span>

<span data-ttu-id="8ec3f-106">Lync クライアントで使用するポート範囲を指定するだけでなく、クライアントコンピューターに適用される別のサービス品質のポリシーも作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-106">In addition to specifying port ranges for use by your Lync clients you must also create separate Quality of Service policies that will be applied to client computers.</span></span> <span data-ttu-id="8ec3f-107">(会議、アプリケーション、および仲介サーバー用に作成されたサービスの品質ポリシーは、クライアントコンピューターに適用しないでください)。この情報は、Lync 2013 クライアントを実行しているコンピューターと、Windows 7 または Windows 8 を実行しているコンピューターにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-107">(The Quality of Service policies created for Conferencing, Application, and Mediation servers should not be applied to client computers.) This information applies only to computers running the Lync 2013 client and either Windows 7 or Windows 8.</span></span>

<span data-ttu-id="8ec3f-108">次の例では、この一連のポート範囲を使ってオーディオポリシーとビデオポリシーを作成しています。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-108">The following example uses this set of port ranges to create an audio policy and a video policy:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8ec3f-109">クライアントトラフィックの種類</span><span class="sxs-lookup"><span data-stu-id="8ec3f-109">Client Traffic Type</span></span></th>
<th><span data-ttu-id="8ec3f-110">ポートの開始</span><span class="sxs-lookup"><span data-stu-id="8ec3f-110">Port Start</span></span></th>
<th><span data-ttu-id="8ec3f-111">ポートの範囲</span><span class="sxs-lookup"><span data-stu-id="8ec3f-111">Port Range</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8ec3f-112">オーディオ</span><span class="sxs-lookup"><span data-stu-id="8ec3f-112">Audio</span></span></p></td>
<td><p><span data-ttu-id="8ec3f-113">50020</span><span class="sxs-lookup"><span data-stu-id="8ec3f-113">50020</span></span></p></td>
<td><p><span data-ttu-id="8ec3f-114">超える</span><span class="sxs-lookup"><span data-stu-id="8ec3f-114">20</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ec3f-115">ビデオ</span><span class="sxs-lookup"><span data-stu-id="8ec3f-115">Video</span></span></p></td>
<td><p><span data-ttu-id="8ec3f-116">58000</span><span class="sxs-lookup"><span data-stu-id="8ec3f-116">58000</span></span></p></td>
<td><p><span data-ttu-id="8ec3f-117">超える</span><span class="sxs-lookup"><span data-stu-id="8ec3f-117">20</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ec3f-118">アプリケーション共有</span><span class="sxs-lookup"><span data-stu-id="8ec3f-118">Application sharing</span></span></p></td>
<td><p><span data-ttu-id="8ec3f-119">42000</span><span class="sxs-lookup"><span data-stu-id="8ec3f-119">42000</span></span></p></td>
<td><p><span data-ttu-id="8ec3f-120">超える</span><span class="sxs-lookup"><span data-stu-id="8ec3f-120">20</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ec3f-121">ファイル転送</span><span class="sxs-lookup"><span data-stu-id="8ec3f-121">File transfer</span></span></p></td>
<td><p><span data-ttu-id="8ec3f-122">42020</span><span class="sxs-lookup"><span data-stu-id="8ec3f-122">42020</span></span></p></td>
<td><p><span data-ttu-id="8ec3f-123">超える</span><span class="sxs-lookup"><span data-stu-id="8ec3f-123">20</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8ec3f-124">Windows 7 または Windows 8 コンピューターのサービス品質のオーディオポリシーを作成するには、まずグループポリシー管理がインストールされているコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-124">To create a Quality of Service audio policy for Windows 7 or Windows 8 computers, first log on to a computer where Group Policy Management has been installed.</span></span> <span data-ttu-id="8ec3f-125">[グループポリシーの管理] を開き ([ **スタート**] をクリックし、[ **管理ツール**] をポイントして、[ **グループポリシーの管理**] をクリックし)、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-125">Open Group Policy Management (click **Start**, point to **Administrative Tools**, and then click **Group Policy Management**) and then complete the following procedure:</span></span>

1.  <span data-ttu-id="8ec3f-126">[グループポリシーの管理] で、新しいポリシーを作成するコンテナーを見つけます。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-126">In Group Policy Management, locate the container where the new policy should be created.</span></span> <span data-ttu-id="8ec3f-127">たとえば、すべてのクライアントコンピューターがクライアントという名前の OU に配置されている場合、新しいポリシーはクライアント OU で作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-127">For example, if all your client computers are located in an OU named Clients then the new policy should be created in the Client OU.</span></span>

2.  <span data-ttu-id="8ec3f-128">適切なコンテナーを右クリックし、[ **このドメインに GPO を作成**] をクリックして、ここにリンクを設定します。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-128">Right-click the appropriate container and then click **Create a GPO in this domain, and Link it here**.</span></span>

3.  <span data-ttu-id="8ec3f-129">[ **新しい GPO** ] ダイアログボックスで、[ **名前** ] ボックスに新しいグループポリシーオブジェクトの名前を入力し (「 **Lync Audio**」など)、[ **OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-129">In the **New GPO** dialog box, type a name for the new Group Policy object in the **Name** box (for example, **Lync Audio**) and then click **OK**.</span></span>

4.  <span data-ttu-id="8ec3f-130">新しく作成したポリシーを右クリックし、[ **編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-130">Right-click the newly-created policy and then click **Edit**.</span></span>

5.  <span data-ttu-id="8ec3f-131">グループポリシー管理エディターで、[ **コンピューターの構成**]、[ **ポリシー**]、[ **Windows 設定**] の順に展開し、[ **ポリシーベースの QoS**] を右クリックして、[ **新しいポリシーの作成**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-131">In the Group Policy Management Editor, expand **Computer Configuration**, expand **Policies**, expand **Windows Settings**, right-click **Policy-based QoS**, and then click **Create new policy**.</span></span>

6.  <span data-ttu-id="8ec3f-132">[**ポリシーベースの QoS** ] ダイアログボックスの [開く] ページで、[**名前**] ボックスに新しいポリシーの名前を入力します (例: **Lync Audio**)。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-132">In the **Policy-based QoS** dialog box, on the opening page, type a name for the new policy (e.g., **Lync Audio**) in the **Name** box.</span></span> <span data-ttu-id="8ec3f-133">[ **DSCP 値の指定** ] を選択し、値を **46** に設定します。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-133">Select **Specify DSCP Value** and set the value to **46**.</span></span> <span data-ttu-id="8ec3f-134">[ **送信スロットルの比率を指定する** ] をオフにして、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-134">Leave **Specify Outbound Throttle Rate** unselected, and then click **Next**.</span></span>

7. <span data-ttu-id="8ec3f-135">次のページで、[ **この実行可能ファイル名のアプリケーションのみ** ] を選択して **Lync.exe** 名前を入力し、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-135">On the next page, select **Only applications with this executable name** and enter the name **Lync.exe**, and then click **Next**.</span></span> <span data-ttu-id="8ec3f-136">この設定は、Lync クライアントからの一致トラフィックのみの優先順位付けをポリシーに指示します。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-136">This setting instructs the policy to only prioritize matching traffic from the Lync client.</span></span>

8.  <span data-ttu-id="8ec3f-137">3番目のページで、 **すべてのソース ip** アドレスと **宛先 ip アドレス** が選択されていることを確認し、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-137">On the third page, make sure that both **Any source IP address** and **Any destination IP address** are selected and then click **Next**.</span></span> <span data-ttu-id="8ec3f-138">この2つの設定では、どのコンピューター (IP アドレス) がそれらのパケットを送信したか、どのコンピューター (IP アドレス) がそれらのパケットを受信するかに関係なく、パケットが管理されるようにします。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-138">These two settings ensure that packets will be managed regardless of which computer (IP address) sent those packets and which computer (IP address) will receive those packets.</span></span>

9.  <span data-ttu-id="8ec3f-139">4ページ目で、[**この QoS ポリシーが適用されるプロトコルを選択** してください] ドロップダウンリストから [ **TCP および UDP** ] を選びます。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-139">On page four, select **TCP and UDP** from the **Select the protocol this QoS policy applies to** dropdown list.</span></span> <span data-ttu-id="8ec3f-140">TCP (伝送制御プロトコル) と UDP (ユーザーデータグラムプロトコル) は、Lync Server およびそのクライアントアプリケーションで最も一般的に使用される2つのネットワークプロトコルです。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-140">TCP (Transmission Control Protocol) and UDP (User Datagram Protocol) are the two networking protocols most-commonly used by Lync Server and its client applications.</span></span>

10. <span data-ttu-id="8ec3f-141">見出しの下で、 **ソースポート番号を指定** して、[ **このソースポートまたは範囲から**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-141">Under the heading **Specify the source port number**, select **From this source port or range**.</span></span> <span data-ttu-id="8ec3f-142">[付随するテキスト] ボックスに、オーディオ送信用に予約されているポート範囲を入力します。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-142">In the accompanying text box, type the port range reserved for audio transmissions.</span></span> <span data-ttu-id="8ec3f-143">たとえば、ポート50020からオーディオトラフィック用にポート50039を予約した場合、次の形式を使用してポート範囲を入力します **50020:50039**。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-143">For example, if you reserved ports 50020 through ports 50039 for audio traffic enter the port range using this format: **50020:50039**.</span></span> <span data-ttu-id="8ec3f-144">[**完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-144">Click **Finish**.</span></span>

<span data-ttu-id="8ec3f-145">オーディオの QoS ポリシーを作成したら、ビデオ用の第2のポリシーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-145">After you have created the QoS policy for audio you should then create a second policy for video.</span></span> <span data-ttu-id="8ec3f-146">ビデオのポリシーを作成するには、オーディオポリシーを作成する場合と同じ基本的な手順に従い、次のように置き換えます。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-146">To create a policy for video, follow the same basic procedure you followed when creating the audio policy, making these substitutions:</span></span>

  - <span data-ttu-id="8ec3f-147">別の (一意の) ポリシー名を使用します (例、 **Lync Video**)。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-147">Use a different (and unique) policy name (for example, **Lync Video**).</span></span>

  - <span data-ttu-id="8ec3f-148">DSCP 値を46ではなく、 **34** に設定します。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-148">Set the DSCP value to **34** instead of 46.</span></span> <span data-ttu-id="8ec3f-149">(前に説明したように、DSCP 値34を使用する必要はありません。単に、オーディオに使用されている別の DSCP 値を割り当てる必要があります)。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-149">(As noted previously, you do not have to use the DSCP value 34; you simply must assign a different DSCP value than the one used for audio.)</span></span>

  - <span data-ttu-id="8ec3f-150">以前に構成したポート範囲をビデオトラフィックに使用します。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-150">Use the previously-configured port range for video traffic.</span></span> <span data-ttu-id="8ec3f-151">たとえば、58000 ~ 58019 のビデオ用の予約ポートがある場合は、ポート範囲 **58000:58019** を次のように設定します。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-151">For example, if you have reserved ports 58000 through 58019 for video, then set the port range to this: **58000:58019**.</span></span>

<span data-ttu-id="8ec3f-152">アプリケーション共有トラフィックを管理するためのポリシーを作成する場合は、次のように置き換えます。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-152">If you decide to create a policy for managing application sharing traffic make these substitutions:</span></span>

  - <span data-ttu-id="8ec3f-153">別の (一意の) ポリシー名 (「 **Lync Server アプリケーション共有**」など) を使用します。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-153">Use a different (and unique) policy name (for example, **Lync Server Application Sharing**).</span></span>

  - <span data-ttu-id="8ec3f-154">DSCP 値を46の代わりに **24** に設定します。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-154">Set the DSCP value to **24** instead of 46.</span></span> <span data-ttu-id="8ec3f-155">(この値は、必ずしも24である必要はありません。単に、音声とビデオに使われる DSCP 値とは異なる必要があります)。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-155">(Again, this value does not have to be 24; it simply must be different than the DSCP values used for audio and for video.)</span></span>

  - <span data-ttu-id="8ec3f-156">以前に構成したポート範囲をビデオトラフィックに使用します。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-156">Use the previously-configured port range for video traffic.</span></span> <span data-ttu-id="8ec3f-157">たとえば、アプリケーション共有用にポート 42000 ~ 42019 を予約している場合は、ポート範囲 **42000:42019** を次のように設定します。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-157">For example, if you have reserved ports 42000 through 42019 for application sharing, then set the port range to this: **42000:42019**.</span></span>

<span data-ttu-id="8ec3f-158">ファイル転送ポリシーの場合:</span><span class="sxs-lookup"><span data-stu-id="8ec3f-158">For a file transfer policy:</span></span>

  - <span data-ttu-id="8ec3f-159">別の (一意の) ポリシー名 (「 **Lync Server ファイル転送**」など) を使用します。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-159">Use a different (and unique) policy name (for example, **Lync Server File Transfers**).</span></span>

  - <span data-ttu-id="8ec3f-160">DSCP 値を **14** に設定します。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-160">Set the DSCP value to **14**.</span></span> <span data-ttu-id="8ec3f-161">(この値は、14でなくてもかまいません。単に一意の DSCP コードである必要があります)。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-161">(Again, this value does not have to be 14; it simply must be a unique DSCP code.)</span></span>

  - <span data-ttu-id="8ec3f-162">以前に設定したアプリケーションのポート範囲を使用します。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-162">Use the previously-configured port range for application.</span></span> <span data-ttu-id="8ec3f-163">たとえば、アプリケーション共有用にポート 42020 ~ 42039 を予約している場合は、ポート範囲 **42020:42039** を次のように設定します。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-163">For example, if you have reserved ports 42020 through 42039 for application sharing, then set the port range to this: **42020:42039**.</span></span>

<span data-ttu-id="8ec3f-164">クライアントコンピューターでグループポリシーが更新されるまで、作成した新しいポリシーは有効になりません。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-164">The new policies you have created will not take effect until Group Policy has been refreshed on your client computers.</span></span> <span data-ttu-id="8ec3f-165">グループ ポリシーは定期的に自動更新されますが、グループ ポリシーを更新する必要がある各コンピューター上で次のコマンドを実行すると、即座に強制的に更新することができます。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-165">Although Group Policy periodically refreshes on its own, you can force an immediate refresh by running the following command on each computer where Group Policy needs to be refreshed:</span></span>

    Gpudate.exe /force

<span data-ttu-id="8ec3f-166">このコマンドは、管理者の資格情報のもとで実行されているコマンド ウィンドウから実行できます。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-166">This command can be run from any command window that is running under administrator credentials.</span></span> <span data-ttu-id="8ec3f-167">管理者の資格情報のもとでコマンド ウィンドウを開くには、[**スタート**] メニューをクリックし、[**コマンド プロンプト**] を右クリックして、[**管理者として実行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-167">To run a command window under administrator credentials, click **Start**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>

<span data-ttu-id="8ec3f-168">これらのポリシーは、クライアントコンピューターのターゲットにする必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-168">Keep in mind that these policies should be targeted towards your client computers.</span></span> <span data-ttu-id="8ec3f-169">Lync Server を実行しているサーバーには適用しないでください。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-169">They should not be applied to servers running Lync Server.</span></span>

<span data-ttu-id="8ec3f-170">ネットワークパケットが適切な DSCP 値でマークされていることを確認するには、次の手順に従って、各コンピューターに新しいレジストリエントリを作成する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-170">To help ensure that network packets are marked with the appropriate DSCP value, you should also create a new registry entry on each computer by completing the following procedure:</span></span>

1.  <span data-ttu-id="8ec3f-171">[ **スタート** ] をクリックし、[ **実行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-171">Click **Start** and then click **Run**.</span></span>

2.  <span data-ttu-id="8ec3f-172">[ **実行** ] ダイアログボックスで、「 **regedit** 」と入力し、enter キーを押します。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-172">In the **Run** dialog box, type **regedit** and then press ENTER.</span></span>

3.  <span data-ttu-id="8ec3f-173">レジストリエディターで、[ **HKEY \_ ローカル \_ コンピューター**]、[ **システム**]、[ **CurrentControlSet**] の順に展開し、[ **サービス**] を展開して、[ **Tcpip**] を展開します。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-173">In the Registry Editor, expand **HKEY\_LOCAL\_MACHINE**, expand **SYSTEM**, expand **CurrentControlSet**, expand **services**, and then expand **Tcpip**.</span></span>

4.  <span data-ttu-id="8ec3f-174">[ **Tcpip**] を右クリックし、[ **新規作成**] をポイントして、[ **キー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-174">Right-click **Tcpip**, point to **New**, and then click **Key**.</span></span> <span data-ttu-id="8ec3f-175">新しいレジストリキーが作成されたら、「 **QoS** 」と入力し、enter キーを押してキーの名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-175">After the new registry key is created, type **QoS** and then press ENTER to rename the key.</span></span>

5.  <span data-ttu-id="8ec3f-176">[ **QoS**] を右クリックし、[ **新規作成**] をポイントして、[ **文字列値**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-176">Right-click **QoS**, point to **New**, and then click **String Value**.</span></span> <span data-ttu-id="8ec3f-177">新しいレジストリ値が作成されたら、[ **NLA を使用しない** ] と入力し、enter キーを押して値の名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-177">After the new registry value is created, type **Do not use NLA** and then press ENTER to rename the value.</span></span>

6.  <span data-ttu-id="8ec3f-178">[ **NLA を使わない**] をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-178">Double-click **Do not use NLA**.</span></span> <span data-ttu-id="8ec3f-179">[**文字列の編集**] ダイアログボックスで、[**値のデータ**] ボックスに「 **1** 」と入力し、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-179">In the **Edit String** dialog box, type **1** in the **Value data** box and then click **OK**.</span></span>

7.  <span data-ttu-id="8ec3f-180">レジストリエディターを終了し、コンピューターを再起動します。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-180">Close the Registry Editor and then reboot your computer.</span></span>

<div>

## <a name="configuring-quality-of-service-on-computers-with-multiple-network-adapters"></a><span data-ttu-id="8ec3f-181">複数のネットワークアダプターを搭載したコンピューターでサービスの品質を設定する</span><span class="sxs-lookup"><span data-stu-id="8ec3f-181">Configuring Quality of Service on Computers with Multiple Network Adapters</span></span>

<span data-ttu-id="8ec3f-182">複数のネットワークアダプターを搭載したコンピューターを使用している場合、DSCP 値が構成された値ではなく0x00 として表示される問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-182">If you have a computer that has multiple network adapters you might occasionally run into issues where DSCP values are shown as 0x00 rather than the configured value.</span></span> <span data-ttu-id="8ec3f-183">これは通常、1つ以上のネットワークアダプターが Active Directory ドメインにアクセスできない (たとえば、これらのアダプターがプライベートネットワーク用に使用されている) 場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-183">This will typically occur on computers where one or more of the network adapters are not able to access your Active Directory domain (for example, if these adapters are used for a private network).</span></span> <span data-ttu-id="8ec3f-184">このような場合、DSCP 値は、ドメインにアクセスできるアダプターに対してタグ付けされますが、ドメインにアクセスできないアダプターにはタグ付けされません。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-184">In cases like that, DSCP values will be tagged for the adapters that can access the domain, but will not be tagged for adapters that cannot access the domain.</span></span>

<span data-ttu-id="8ec3f-185">ドメインにアクセスできないアダプターも含め、コンピューターのすべてのネットワークアダプターの DSCP 値にタグを付ける場合は、レジストリに値を追加して構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-185">If you would like to tag DSCP values for all the network adapters in a computer, including adapters that do not have access to your domain, then you will need to add and configure a value to the registry.</span></span> <span data-ttu-id="8ec3f-186">この操作を行うには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-186">That can be done by completing the following procedure:</span></span>

1.  <span data-ttu-id="8ec3f-187">[ **スタート** ] をクリックし、[ **実行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-187">Click **Start** and then click **Run**.</span></span>

2.  <span data-ttu-id="8ec3f-188">[ **実行** ] ダイアログボックスで、「 **regedit** 」と入力し、enter キーを押します。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-188">In the **Run** dialog box, type **regedit** and then press ENTER.</span></span>

3.  <span data-ttu-id="8ec3f-189">レジストリエディターで、[ **HKEY \_ ローカル \_ コンピューター**]、[ **システム**]、[ **CurrentControlSet**] の順に展開し、[ **サービス**] を展開して、[ **Tcpip**] を展開します。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-189">In the Registry Editor, expand **HKEY\_LOCAL\_MACHINE**, expand **SYSTEM**, expand **CurrentControlSet**, expand **services**, and then expand **Tcpip**.</span></span>

4.  <span data-ttu-id="8ec3f-190">[ **QoS** ] というラベルのレジストリキーが表示されない場合は、[ **Tcpip**] を右クリックし、[ **新規**] をポイントして、[ **キー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-190">If you do not see a registry key labeled **QoS** then right-click **Tcpip**, point to **New**, and then click **Key**.</span></span> <span data-ttu-id="8ec3f-191">新しいキーを作成したら、「 **QoS** 」と入力し、enter キーを押してキーの名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-191">After the new key is created, type **QoS** and then press ENTER to rename the key.</span></span>

5.  <span data-ttu-id="8ec3f-192">[ **QoS**] を右クリックし、[ **新規作成**] をポイントして、[ **文字列値**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-192">Right-click **QoS**, point to **New**, and then click **String Value**.</span></span> <span data-ttu-id="8ec3f-193">新しいレジストリ値が作成されたら、[ **NLA を使用しない** ] と入力し、enter キーを押して値の名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-193">After the new registry value is created, type **Do not use NLA** and then press ENTER to rename the value.</span></span>

6.  <span data-ttu-id="8ec3f-194">[ **NLA を使わない**] をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-194">Double-click **Do not use NLA**.</span></span> <span data-ttu-id="8ec3f-195">[**文字列の編集**] ダイアログボックスで、[**値のデータ**] ボックスに「 **1** 」と入力し、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-195">In the **Edit String** dialog box, type **1** in the **Value data** box and then click **OK**.</span></span>

<span data-ttu-id="8ec3f-196">新しいレジストリ値を作成して構成した後、変更を有効にするためにコンピューターを再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8ec3f-196">After creating and configuring the new registry value you will need to reboot your computer in order for the changes to take effect.</span></span>

<span data-ttu-id="8ec3f-197"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8ec3f-197"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

