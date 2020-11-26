---
title: 'Lync Server 2013: クライアントコンピューターで個人用連絡先ストアを構成する'
description: 'Lync Server 2013: クライアントコンピューターで個人用の連絡先ストアを構成します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring the personal contacts store on client computers
ms:assetid: ec69a6cb-07f2-4057-9544-55035f83eeae
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721922(v=OCS.15)
ms:contentKeyID: 49733857
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c1040b3eb9aa38e3e0c537d690b9292ab8f1ead2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432521"
---
# <a name="configuring-the-personal-contacts-store-on-client-computers-for-lync-server-2013"></a><span data-ttu-id="466d1-103">Lync Server 2013 のクライアントコンピューターで個人用連絡先ストアを構成する</span><span class="sxs-lookup"><span data-stu-id="466d1-103">Configuring the personal contacts store on client computers for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="466d1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="466d1-104">

<span> </span></span></span>

<span data-ttu-id="466d1-105">_**最終更新日:** 2014-02-05_</span><span class="sxs-lookup"><span data-stu-id="466d1-105">_**Topic Last Modified:** 2014-02-05_</span></span>

<span data-ttu-id="466d1-106">Microsoft Lync Server 2013 と Microsoft Exchange Server 2013 を統合する場合は、Microsoft Lync 2010 を実行しているすべてのクライアントコンピューターで個人用連絡先ストアを構成することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="466d1-106">If you are integrating Microsoft Lync Server 2013 and Microsoft Exchange Server 2013 then it is recommended that you configure the personal contact store on any client computers running Microsoft Lync 2010.</span></span> <span data-ttu-id="466d1-107">特に、Exchange を個人用連絡先ストアとして使用するように Lync を構成し、同時にユーザーがその決定を上書きできないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="466d1-107">In particular, you should configure Lync to use Exchange as the personal contact store, and, at the same time, ensure that users are not able to override that decision.</span></span> <span data-ttu-id="466d1-108">そのためには、各クライアント コンピューターでレジストリ値を作成して構成します。</span><span class="sxs-lookup"><span data-stu-id="466d1-108">This can be done by creating and configuring a Registry value on each client computer.</span></span>

<span data-ttu-id="466d1-109">これは、Lync 2013 を実行しているコンピューターでは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="466d1-109">Note that this is not required on computers running Lync 2013.</span></span>

<span data-ttu-id="466d1-110">1 台のコンピューターでこの値を構成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="466d1-110">To configure this value on a single computer, complete the following procedure:</span></span>

1.  <span data-ttu-id="466d1-111">クライアント コンピューターで [**スタート**] ボタンをクリックし、[**ファイル名を指定して実行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="466d1-111">On the client computer, click **Start** and then click **Run**.</span></span>

2.  <span data-ttu-id="466d1-112">[**ファイル名を指定して実行**] ダイアログ ボックスで「regedit」と入力して、Enter キーを押します。</span><span class="sxs-lookup"><span data-stu-id="466d1-112">In the **Run** dialog box, type regedit and then press ENTER.</span></span>

3.  <span data-ttu-id="466d1-113">レジストリエディターで、[ **HKEY \_ ローカル \_ コンピューター**]、[ **ソフトウェア**]、[ **ポリシー**] の順に展開し、[ **Microsoft**]、[ **Communicator**] の順に展開します。</span><span class="sxs-lookup"><span data-stu-id="466d1-113">In Registry Editor, expand **HKEY\_LOCAL\_MACHINE**, expand **Software**, expand **Policies**, expand **Microsoft**, and then expand **Communicator**.</span></span>

4.  <span data-ttu-id="466d1-114">[**Communicator**] を右クリックし、[**新規**] をポイントし、[**DWORD (32 ビット) 値**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="466d1-114">Right-click **Communicator**, point to **New**, and then click **DWORD (32-bit) Value**.</span></span>

5.  <span data-ttu-id="466d1-115">新しい値を作成した後に「**PersonalContactStoreOverride**」と入力し、Enter キーを押して値の名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="466d1-115">After the new value is created, type **PersonalContactStoreOverride** and then press ENTER to rename the value.</span></span>

6.  <span data-ttu-id="466d1-116">PersonalContactStoreOverride の値が 0 に設定されていることを確認し、レジストリ エディターを閉じます。</span><span class="sxs-lookup"><span data-stu-id="466d1-116">Verify that the value of PersonalContactStoreOverride is set to 0 and then close Registry Editor.</span></span>

<span data-ttu-id="466d1-117">複数のコンピューターでこれと同じ変更をする必要がある場合は、カスタム グループ ポリシー オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="466d1-117">If you need to make this same change on multiple computers you can do so by creating a custom Group Policy object.</span></span> <span data-ttu-id="466d1-118">詳細については、のグループポリシードキュメントを参照してください [https://go.microsoft.com/fwlink/p/?LinkId=268543](https://go.microsoft.com/fwlink/p/?linkid=268543) 。</span><span class="sxs-lookup"><span data-stu-id="466d1-118">For details, see the Group Policy documentation at [https://go.microsoft.com/fwlink/p/?LinkId=268543](https://go.microsoft.com/fwlink/p/?linkid=268543).</span></span>

<span data-ttu-id="466d1-119"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="466d1-119"></div>

<span> </span>

</div>

</div>

</span></span></div>

