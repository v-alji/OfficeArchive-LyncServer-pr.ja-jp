---
title: 'Lync Server 2013: ボイスメールのエスケープの設定'
description: 'Lync Server 2013: ボイスメールのエスケープを構成しています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring voice mail escape
ms:assetid: a1d19e6c-82ff-4768-8ae5-da981368ce40
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688157(v=OCS.15)
ms:contentKeyID: 49733761
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: afbb2dd10c7ff8809eb8dfbcc64e40a599aa06a4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432402"
---
# <a name="configuring-voice-mail-escape-in-lync-server-2013"></a><span data-ttu-id="68267-103">Lync Server 2013 でボイスメールのエスケープを構成する</span><span class="sxs-lookup"><span data-stu-id="68267-103">Configuring voice mail escape in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="68267-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="68267-104">

<span> </span></span></span>

<span data-ttu-id="68267-105">_**最終更新日:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="68267-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="68267-106">ユーザーが携帯電話への同時着信を構成している場合、携帯電話がオフになっている、バッテリが切れている、または圏外になっているときは、通常、発信者はユーザーの個人ボイス メールにルーティングされます。</span><span class="sxs-lookup"><span data-stu-id="68267-106">When a user configures simultaneous ringing to a mobile phone, a caller will typically be routed to the user’s personal voice mail if the mobile phone is turned off, out of battery power, or out of range.</span></span> <span data-ttu-id="68267-107">Lync Server 2013 を使用すると、ユーザーはビジネス関連の通話を会社のボイスメールシステムにルーティングすることを選択できます。</span><span class="sxs-lookup"><span data-stu-id="68267-107">With Lync Server 2013, users can opt to have business-related calls routed to their corporate voice mail system.</span></span> <span data-ttu-id="68267-108">特に、タイマーは構成可能であり、定義された時間内に電話会社のボイスメールによって通話が応答された場合、Lync Server は電話会社のボイスメールシステム (およびユーザーの個人のボイスメール) から切断されますが、企業システム内のユーザーの残りのエンドポイントは引き続き呼び出しを続けます。</span><span class="sxs-lookup"><span data-stu-id="68267-108">Specifically, a timer can be configured, and if the call is answered by the carrier’s voice mail within the range of time defined, Lync Server will disconnect from the carrier’s voice mail system (and the user’s personal voice mail), while the user’s remaining endpoints in the corporate system continue to ring.</span></span> <span data-ttu-id="68267-109">これにより、発信者は自動的にユーザーの会社のボイス メールにルーティングされます。</span><span class="sxs-lookup"><span data-stu-id="68267-109">This way, the caller is automatically routed to the user’s corporate voice mail.</span></span>

<span data-ttu-id="68267-110">この構成は、Lync Server Management Shell コマンドレット **CsVoicePolicy** を使用して、ボイスポリシーレベルで次のパラメーターを指定して実行します。</span><span class="sxs-lookup"><span data-stu-id="68267-110">This configuration is performed using the Lync Server Management Shell cmdlet, **Set-CsVoicePolicy**, at the voice policy level, with the following parameters.</span></span>

<div>

## <a name="to-configure-voice-mail-escape"></a><span data-ttu-id="68267-111">ボイス メール エスケープを構成するには</span><span class="sxs-lookup"><span data-stu-id="68267-111">To configure voice mail escape</span></span>

1.  <span data-ttu-id="68267-112">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="68267-112">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="68267-113">**Set-CsVoicePolicy** に対して次のパラメーターを指定します。</span><span class="sxs-lookup"><span data-stu-id="68267-113">Specify the following parameters to **Set-CsVoicePolicy**:</span></span>
    
      - <span data-ttu-id="68267-114">**EnableVoicemailEscapeTimer** - エスケープ タイマーを有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="68267-114">**EnableVoicemailEscapeTimer** - Enables or disables the escape timer.</span></span>
    
      - <span data-ttu-id="68267-p102">**PSTNVoicemailEscapeTimer**: タイムアウト値をミリ秒単位で指定します。既定値は 1500 ミリ秒で、指定できる値の範囲は 0 ～ 8000 ミリ秒です。</span><span class="sxs-lookup"><span data-stu-id="68267-p102">**PSTNVoicemailEscapeTimer** - Specifies the timeout value in milliseconds. The default value is 1500 milliseconds, and the value can range from 0 milliseconds to 8000 milliseconds.</span></span>

</div>

<div>

## <a name="example"></a><span data-ttu-id="68267-117">例</span><span class="sxs-lookup"><span data-stu-id="68267-117">Example</span></span>

    Set-CsVoicePolicy UserVoicePolicy -EnableVoiceMailEscapeTimer $true - PSTNVoicemailEscapeTimer 2000
    
    Set-CsVoicePolicy -Identity site:SitePolicy -EnableVoiceMailEscapeTimer $true -PSTNVoicemailEscapeTimer 1500

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="68267-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="68267-118">See Also</span></span>


[<span data-ttu-id="68267-119">Lync Server 2013 での通話機能と特権の承認のための音声ポリシーと PSTN 使用法レコードの構成</span><span class="sxs-lookup"><span data-stu-id="68267-119">Configuring voice policies and PSTN usage records to authorize calling features and privileges in Lync Server 2013</span></span>](lync-server-2013-configuring-voice-policies-and-pstn-usage-records-to-authorize-calling-features-and-privileges.md)  
  

<span data-ttu-id="68267-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="68267-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

