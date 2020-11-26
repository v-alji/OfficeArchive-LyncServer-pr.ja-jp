---
title: アドレス帳の移行
description: アドレス帳を移行します。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate Address Book
ms:assetid: ac7f0f39-4c6d-4702-8e25-93a73e3d800f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205160(v=OCS.15)
ms:contentKeyID: 48185064
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ad6acd8cca58aa4e09e21b9b45cbdddec527b5f8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438611"
---
# <a name="migrate-address-book"></a><span data-ttu-id="fdc43-103">アドレス帳の移行</span><span class="sxs-lookup"><span data-stu-id="fdc43-103">Migrate Address Book</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fdc43-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fdc43-104">

<span> </span></span></span>

<span data-ttu-id="fdc43-105">_**最終更新日:** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="fdc43-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="fdc43-106">一般に、Lync Server 2010 アドレス帳は、他のトポロジと共に移行されます。</span><span class="sxs-lookup"><span data-stu-id="fdc43-106">In general, the Lync Server 2010 Address Book is migrated along with the rest of your topology.</span></span> <span data-ttu-id="fdc43-107">ただし、Lync Server 2010 環境で次のようにカスタマイズした場合は、移行後にいくつかの手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fdc43-107">However, you might need to perform some post-migration steps if you customized the following in your Lync Server 2010 environment:</span></span>

  - <span data-ttu-id="fdc43-108">**Partitionbyou** WMI プロパティを組織単位 (ou) ごとにグループのアドレス帳エントリに設定します。</span><span class="sxs-lookup"><span data-stu-id="fdc43-108">Set the **PartitionbyOU** WMI property to group Address Book entries by organizational unit (OU).</span></span>

  - <span data-ttu-id="fdc43-109">アドレス帳の正規化規則をカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="fdc43-109">Customized the Address Book normalization rules.</span></span>

  - <span data-ttu-id="fdc43-110">**UseNormalizationRules** パラメーターの既定値が False に変更されました。</span><span class="sxs-lookup"><span data-stu-id="fdc43-110">Changed the default value for the **UseNormalizationRules** parameter to False.</span></span>

<span data-ttu-id="fdc43-111">**グループ化されたアドレス帳のエントリ**</span><span class="sxs-lookup"><span data-stu-id="fdc43-111">**Grouped Address Book Entries**</span></span>

<span data-ttu-id="fdc43-112">**Partitionbyou** WMI プロパティを True に設定して、各組織のアドレス帳を作成する場合、アドレス帳エントリのグループ化を続けたい場合は、ユーザーと連絡先に対して **Msrtcsip-userenabled true-groupingid** Active Directory 属性を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fdc43-112">If you set the **PartitionbyOU** WMI property to True to create address books for each OU, you need to set the **msRTCSIP-GroupingId** Active Directory attribute on users and contacts if you want to continue grouping address book entries.</span></span> <span data-ttu-id="fdc43-113">アドレス帳の検索の範囲を制限するために、アドレス帳のエントリをグループ化することができます。</span><span class="sxs-lookup"><span data-stu-id="fdc43-113">You might want to group address book entries to limit the scope of Address Book searches.</span></span> <span data-ttu-id="fdc43-114">**Msrtcsip-userenabled true-GroupingId** 属性を使用するには、属性を設定するスクリプトを作成し、グループ化するすべてのユーザーに同じ値を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="fdc43-114">To use the **msRTCSIP-GroupingId** attribute, write a script to populate the attribute, assigning the same value for all of the users that you want to group together.</span></span> <span data-ttu-id="fdc43-115">たとえば、OU 内のすべてのユーザーに1つの値を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="fdc43-115">For example, assign a single value for all the users in an OU.</span></span>

<span data-ttu-id="fdc43-116">**アドレス帳正規化ルール**</span><span class="sxs-lookup"><span data-stu-id="fdc43-116">**Address Book Normalization Rules**</span></span>

<span data-ttu-id="fdc43-117">Lync Server 2010 環境でアドレス帳の正規化ルールをカスタマイズした場合は、カスタマイズしたルールをパイロットプールに移行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fdc43-117">If you customized Address Book normalization rules in your Lync Server 2010 environment, you must migrate the customized rules to your pilot pool.</span></span> <span data-ttu-id="fdc43-118">アドレス帳の正規化ルールをカスタマイズしていない場合、アドレス帳サービスに移行することはできません。</span><span class="sxs-lookup"><span data-stu-id="fdc43-118">If you did not customize Address Book normalization rules, you have nothing to migrate for Address Book service.</span></span> <span data-ttu-id="fdc43-119">Lync Server 2013 の既定の正規化ルールは、Lync Server 2010 の既定のルールと同じです。</span><span class="sxs-lookup"><span data-stu-id="fdc43-119">The default normalization rules for Lync Server 2013 are the same as the default rules for Lync Server 2010.</span></span> <span data-ttu-id="fdc43-120">カスタマイズされた正規化ルールを移行するには、このセクションの後半の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="fdc43-120">Follow the procedure later in this section to migrate customized normalization rules.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="fdc43-121">組織でリモート通話コントロールを使用していて、アドレス帳正規化ルールをカスタマイズしている場合、リモート通話コントロールを使用する前に、このトピックの手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fdc43-121">If your organization uses remote call control and you customized Address Book normalization rules, you must perform the procedure in this topic before you can use remote call control.</span></span> <span data-ttu-id="fdc43-122">この手順では、RTCUniversalServerAdmins グループのメンバーシップ、または同等の権限が必要です。</span><span class="sxs-lookup"><span data-stu-id="fdc43-122">The procedure requires membership in the RTCUniversalServerAdmins group or equivalent rights.</span></span>



</div>

<span data-ttu-id="fdc43-123">**UseNormalizationRules が False に設定**</span><span class="sxs-lookup"><span data-stu-id="fdc43-123">**UseNormalizationRules Set to False**</span></span>

<span data-ttu-id="fdc43-124">ユーザーが電話番号を使用できるように、 **UseNormalizationRules** の値を False に設定した場合、Lync Server 2013 で正規化ルールを適用することなく、Active Directory ドメインサービスで定義された電話番号を使用できるようにするには、 **UseNormalizationRules** と **Ignoregenericrules** パラメーターを True に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fdc43-124">If you set the value for **UseNormalizationRules** to False so that users can use phone numbers as they are defined in Active Directory Domain Services without having Lync Server 2013 apply normalization rules, you need to set the **UseNormalizationRules** and **IgnoreGenericRules** parameters to True.</span></span> <span data-ttu-id="fdc43-125">このセクションの後半の手順に従って、これらのパラメーターを True に設定します。</span><span class="sxs-lookup"><span data-stu-id="fdc43-125">Follow the procedure later in this section to set these parameters to True.</span></span>

<div>

## <a name="to-migrate-address-book-customized-normalization-rules"></a><span data-ttu-id="fdc43-126">アドレス帳のカスタマイズされた正規化ルールを移行するには</span><span class="sxs-lookup"><span data-stu-id="fdc43-126">To migrate Address Book customized normalization rules</span></span>

1.  <span data-ttu-id="fdc43-127">\_ \_ \_ \_ アドレス帳の共有フォルダーのルートにある [会社電話番号の正規化]Rules.txt ファイルを見つけて、それを Lync Server 2013 パイロットプールのアドレス帳の共有フォルダーのルートにコピーします。</span><span class="sxs-lookup"><span data-stu-id="fdc43-127">Find the Company\_Phone\_Number\_Normalization\_Rules.txt file in the root of the Address Book shared folder, and copy it to the root of the Address Book shared folder in your Lync Server 2013 pilot pool.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="fdc43-128">サンプルのアドレス帳の正規化ルールは、ABS Web コンポーネントファイルディレクトリにインストールされています。</span><span class="sxs-lookup"><span data-stu-id="fdc43-128">The sample Address Book normalization rules have been installed in your ABS Web component file directory.</span></span> <span data-ttu-id="fdc43-129">パスは<STRONG>$installedDriveLetter: Files\Files\ と Lync Server 2013 \ Web Components\Address Book Sample_Company_Phone_Number_Normalization_Rules.txt</STRONG></span><span class="sxs-lookup"><span data-stu-id="fdc43-129">The path is <STRONG>$installedDriveLetter:\Program Files\Microsoft Lync Server 2013\Web Components\Address Book Files\Files\ Sample_Company_Phone_Number_Normalization_Rules.txt,</STRONG>.</span></span> <span data-ttu-id="fdc43-130">このファイルは &nbsp; <STRONG>Company_Phone_Number_Normalization_Rules.txt</STRONG> &nbsp; 、アドレス帳の共有フォルダーのルートディレクトリにCompany_Phone_Number_Normalization_Rules.txtとしてコピーしたり名前を変更したりできます。</span><span class="sxs-lookup"><span data-stu-id="fdc43-130">This file can be copied and renamed as &nbsp;<STRONG>Company_Phone_Number_Normalization_Rules.txt</STRONG> &nbsp;to the address book shared folder’s root directory.</span></span> <span data-ttu-id="fdc43-131">たとえば、 <STRONG>$serverX</STRONG>で共有されているアドレス帳は、 &nbsp; <STRONG> \\ $serverX \LyncFileShare\2-WebServices-1\ABFiles</STRONG>のようなパスになります。</span><span class="sxs-lookup"><span data-stu-id="fdc43-131">For example, the address book shared in <STRONG>$serverX</STRONG>,&nbsp;the path will be similar to: <STRONG>\\$serverX \LyncFileShare\2-WebServices-1\ABFiles</STRONG>.</span></span>

    
    </div>

2.  <span data-ttu-id="fdc43-132">メモ帳などのテキストエディターを使用して、会社の \_ 電話 \_ 番号の \_ 正規化 \_Rules.txt ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="fdc43-132">Use a text editor, such as Notepad, to open the Company\_Phone\_Number\_Normalization\_Rules.txt file.</span></span>

3.  <span data-ttu-id="fdc43-133">Lync Server 2013 では、特定の種類のエントリが正しく動作しないことがあります。</span><span class="sxs-lookup"><span data-stu-id="fdc43-133">Certain types of entries will not work correctly in Lync Server 2013.</span></span> <span data-ttu-id="fdc43-134">この手順で説明したエントリの種類をファイルで確認し、必要に応じて編集して、変更内容をパイロットプールのアドレス帳の共有フォルダーに保存します。</span><span class="sxs-lookup"><span data-stu-id="fdc43-134">Look through the file for the types of entries described in this step, edit them as necessary, and save the changes to the Address Book shared folder in your pilot pool.</span></span>
    
    <span data-ttu-id="fdc43-135">必要な空白または句読点を含む文字列は、正規化ルールに入力された文字列から削除されるため、正規化ルールが失敗します。</span><span class="sxs-lookup"><span data-stu-id="fdc43-135">Strings that include required whitespace or punctuation cause normalization rules to fail because these characters are stripped out of the string that is input to the normalization rules.</span></span> <span data-ttu-id="fdc43-136">文字列に必要な空白または句読点が含まれている場合は、文字列を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fdc43-136">If you have strings that include required whitespace or punctuation, you need to modify the strings.</span></span> <span data-ttu-id="fdc43-137">たとえば、次の文字列では正規化ルールが失敗します。</span><span class="sxs-lookup"><span data-stu-id="fdc43-137">For example, the following string would cause the normalization rule to fail:</span></span>
    
        \s*\(\s*\d\d\d\s*\)\s*\-\s*\d\d\d\s*\-\s*\d\d\d\d
    
    <span data-ttu-id="fdc43-138">次の文字列では、正規化ルールが失敗することはありません。</span><span class="sxs-lookup"><span data-stu-id="fdc43-138">The following string would not cause the normalization rule to fail:</span></span>
    
        \s*\(?\s*\d\d\d\s*\)?\s*\-?\s*\d\d\d\s*\-?\s*\d\d\d\d

</div>

<div>

## <a name="to-set-usenormalizationrules-and-ignoregenericrules-to-true"></a><span data-ttu-id="fdc43-139">UseNormalizationRules と IgnoreGenericRules を true に設定するには</span><span class="sxs-lookup"><span data-stu-id="fdc43-139">To set UseNormalizationRules and IgnoreGenericRules to true</span></span>

1.  <span data-ttu-id="fdc43-140">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="fdc43-140">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="fdc43-141">次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="fdc43-141">Do one of the following:</span></span>
    
      - <span data-ttu-id="fdc43-142">展開に Lync Server 2013 のみが含まれている場合、次のコマンドレットをグローバルレベルで実行して、 **UseNormalizationRules** と **ignoregenericrules** の値を True に変更します。</span><span class="sxs-lookup"><span data-stu-id="fdc43-142">If your deployment includes only Lync Server 2013, run the following cmdlet at the global level to change the values for **UseNormalizationRules** and **IgnoreGenericRules** to True:</span></span>
        
            Set-CsAddressBookConfiguration -identity <XdsIdentity> -UseNormalizationRules=$true -IgnoreGenericRules=$true
    
      - <span data-ttu-id="fdc43-143">展開に Lync Server 2013 および Lync Server 2010 または Office Communications Server 2007 R2 の組み合わせが含まれている場合は、次のコマンドレットを実行して、トポロジの各 Lync Server 2013 プールに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="fdc43-143">If your deployment includes a combination of Lync Server 2013 and Lync Server 2010 or Office Communications Server 2007 R2, run the following cmdlet and assign it to each Lync Server 2013 pool in the topology:</span></span>
        
            New-CsAddressBookConfiguration -identity <XdsIdentity> -UseNormalizationRules=$true -IgnoreGenericRules=$true

3.  <span data-ttu-id="fdc43-144">すべてのプールで一元管理ストアのレプリケーションが実行されるのを待ちます。</span><span class="sxs-lookup"><span data-stu-id="fdc43-144">Wait for Central Management store replication to occur on all pools.</span></span>

4.  <span data-ttu-id="fdc43-145">\_ \_ \_ \_ 展開でコンテンツをクリアするために、電話の正規化ルールファイル "会社電話番号の正規化Rules.txt" を変更します。</span><span class="sxs-lookup"><span data-stu-id="fdc43-145">Modify the phone normalization rules file, "Company\_Phone\_Number\_Normalization\_Rules.txt", for your deployment to clear the content.</span></span> <span data-ttu-id="fdc43-146">ファイルは、各 Lync Server 2013 プールのファイル共有にあります。</span><span class="sxs-lookup"><span data-stu-id="fdc43-146">The file is on the file share of each Lync Server 2013 pool.</span></span> <span data-ttu-id="fdc43-147">ファイルが存在しない場合は、"会社 \_ 電話 \_ 番号の \_ 正規化Rules.txt" という名前の空のファイルを作成し \_ ます。</span><span class="sxs-lookup"><span data-stu-id="fdc43-147">If the file is not present, then create an empty file named "Company\_Phone\_Number\_Normalization\_Rules.txt".</span></span>

5.  <span data-ttu-id="fdc43-148">すべてのフロントエンドプールが新しいファイルを読み取るまで数分待ちます。</span><span class="sxs-lookup"><span data-stu-id="fdc43-148">Wait several minutes for all Front End pools to read the new files.</span></span>

6.  <span data-ttu-id="fdc43-149">展開の各 Lync Server 2013 プールで次のコマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="fdc43-149">Run the following cmdlet on each Lync Server 2013 pool in your deployment:</span></span>
    
        Update-CsAddressBook

<span data-ttu-id="fdc43-150"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fdc43-150"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

