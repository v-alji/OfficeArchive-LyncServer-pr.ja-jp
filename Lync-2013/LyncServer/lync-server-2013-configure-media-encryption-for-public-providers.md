---
title: 'Lync Server 2013: 公開プロバイダーに対するメディアの暗号化の構成'
description: 'Lync Server 2013: パブリックプロバイダーのメディア暗号化を構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure media encryption for public providers
ms:assetid: a95814cf-c5a9-4652-8ffc-c469a2653153
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205149(v=OCS.15)
ms:contentKeyID: 48185036
ms.date: 12/13/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 177c19f151b67d741c7e26506f7ebc98b3ce831a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433886"
---
# <a name="configure-media-encryption-for-public-providers-in-lync-server-2013"></a><span data-ttu-id="a3826-103">Lync Server 2013 での公開プロバイダーに対するメディアの暗号化の構成</span><span class="sxs-lookup"><span data-stu-id="a3826-103">Configure media encryption for public providers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a3826-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a3826-104">

<span> </span></span></span>

<span data-ttu-id="a3826-105">_**最終更新日:** 2014-12-12_</span><span class="sxs-lookup"><span data-stu-id="a3826-105">_**Topic Last Modified:** 2014-12-12_</span></span>

<span data-ttu-id="a3826-106">音声/ビデオ (A/V) フェデレーションを Windows Live Messenger と共に実装する場合は、Lync Server の暗号化レベルと EnablePublicCloudAccess ポリシーという2つのパラメーターを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a3826-106">If you are implementing audio/video (A/V) federation with Windows Live Messenger, there are two parameters that you need to modify: the Lync Server encryption level and the EnablePublicCloudAccess policy.</span></span> <span data-ttu-id="a3826-107">既定では、暗号化レベルは [必須] に設定されています。</span><span class="sxs-lookup"><span data-stu-id="a3826-107">By default, the encryption level is set to Required.</span></span> <span data-ttu-id="a3826-108">この設定は、"サポート" に変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a3826-108">You must change this setting to Supported.</span></span> <span data-ttu-id="a3826-109">EnablePublicCloudAccess ポリシーが false に設定されている場合は、 **True** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a3826-109">If the EnablePublicCloudAccess policy is set to false, this needs to be set to **True**.</span></span> <span data-ttu-id="a3826-110">これは、Lync Server 管理シェルから行うことができます。</span><span class="sxs-lookup"><span data-stu-id="a3826-110">You can do this from the Lync Server Management Shell.</span></span>

<div>

## <a name="configure-federation-for-windows-live"></a><span data-ttu-id="a3826-111">Windows Live 用フェデレーションを構成する</span><span class="sxs-lookup"><span data-stu-id="a3826-111">Configure Federation for Windows Live</span></span>

1.  <span data-ttu-id="a3826-112">フロントエンドサーバーで Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="a3826-112">Start the Lync Server Management Shell on the Front End server: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="a3826-113">コマンドプロンプトで、次のコマンドを入力します。</span><span class="sxs-lookup"><span data-stu-id="a3826-113">From the command prompt, type the following commands:</span></span>
    
       ```powershell
        Set-CsMediaConfiguration -EncryptionLevel SupportEncryption
       ```
    
       ```powershell
        Set-CsExternalAccessPolicy Global -EnablePublicCloudAccess $true -EnablePublicCloudAudioVideoAccess $true
       ```
    
    <div class=" ">
    

    > [!NOTE]  
    > <span data-ttu-id="a3826-114">Windows Live Messenger では音声/ビデオの暗号化がサポートされていないため、これは必須の手順です。</span><span class="sxs-lookup"><span data-stu-id="a3826-114">This is required step because Windows Live Messenger does not support encryption of audio/video.</span></span> <span data-ttu-id="a3826-115">このコマンドは、オーディオ/ビデオデータの暗号化を必要とするのではなく、グローバルポリシーをサポート暗号化設定に設定します。</span><span class="sxs-lookup"><span data-stu-id="a3826-115">The command sets your global policy to a support encryption setting instead of requiring encryption of the audio/video data.</span></span> <span data-ttu-id="a3826-116">暗号化をサポートするクライアントでも、Lync 2013 などの暗号化が使用されます。</span><span class="sxs-lookup"><span data-stu-id="a3826-116">Clients that support encryption will still use encryption, such as Lync 2013.</span></span>

    
    <span data-ttu-id="a3826-117"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a3826-117"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

