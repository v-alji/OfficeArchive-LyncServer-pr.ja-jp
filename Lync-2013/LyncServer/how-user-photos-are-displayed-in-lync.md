---
title: Lync でユーザーの写真を表示する方法
description: Lync でユーザーの写真を表示する方法を説明します。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: How user photos are displayed in Lync
ms:assetid: b44a364d-a1d2-4d45-b27a-b5f77775e233
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn783119(v=OCS.15)
ms:contentKeyID: 62835297
ms.date: 08/27/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 12ea9e19b3965994c025659f1b2249c49ec32a3a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49399422"
---
# <a name="how-user-photos-are-displayed-in-lync"></a><span data-ttu-id="7560c-103">Lync でユーザーの写真を表示する方法</span><span class="sxs-lookup"><span data-stu-id="7560c-103">How user photos are displayed in Lync</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7560c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7560c-104">

<span> </span></span></span>

<span data-ttu-id="7560c-105">_**最終更新日:** 2014-08-25_</span><span class="sxs-lookup"><span data-stu-id="7560c-105">_**Topic Last Modified:** 2014-08-25_</span></span>

<span data-ttu-id="7560c-106">**概要:** Lync クライアントに表示されるユーザーの写真は、どの Lync 機能を使用しているかによって異なる場合があります。たとえば、会議中や IM チャット中などです。</span><span class="sxs-lookup"><span data-stu-id="7560c-106">**Summary:** User photos displayed in Lync client can be different depending on which Lync feature you are using, such as when in a conference or an IM chat.</span></span>

<span data-ttu-id="7560c-107">Lync 2010 では、他の Lync ユーザーに対して表示される、Lync プロファイルと共に写真を含める機能が導入されました。</span><span class="sxs-lookup"><span data-stu-id="7560c-107">Lync 2010 introduced the ability to include a photo with your Lync profile that is displayed to other Lync users.</span></span> <span data-ttu-id="7560c-108">Lync クライアントで連絡先の写真を表示するかどうかを選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="7560c-108">You can also choose whether or not to display photos for your contacts in Lync client.</span></span> <span data-ttu-id="7560c-109">Lync 2013 では、高解像度の写真をユーザー向けにサポートします。</span><span class="sxs-lookup"><span data-stu-id="7560c-109">In Lync 2013, support for high-resolution photos for users.</span></span> <span data-ttu-id="7560c-110">このトピックでは、Lync クライアントでユーザーの写真を取得して表示する方法、画像が保存されている場所、各画像ソースの制限事項、さまざまな Lync サービスでユーザーの写真を使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7560c-110">This topic describes how Lync client gets and displays user photos, where the images are stored, the limitations for each image source, and how user photos are used by different Lync services.</span></span>

<div>

## <a name="planning-considerations"></a><span data-ttu-id="7560c-111">計画の考慮事項</span><span class="sxs-lookup"><span data-stu-id="7560c-111">Planning considerations</span></span>

<span data-ttu-id="7560c-112">ユーザー写真のサポートを実装する計画を立てる場合は、次の点を考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7560c-112">You should consider the following when planning to implement support for user photos.</span></span>

  - <span data-ttu-id="7560c-113">高解像度ユーザーの写真のサポートでは、ユーザーのメールボックスを Exchange 2013 に配置し、Lync ユーザーアカウントを Lync 2013 プールに置く必要があります。</span><span class="sxs-lookup"><span data-stu-id="7560c-113">High-definition user photo support requires that the user’s mailbox be located on Exchange 2013 and the Lync user account to be in Lync 2013 pool.</span></span>

  - <span data-ttu-id="7560c-114">高精細ユーザーの写真は、Lync Server 2013 と Exchange 2013 の両方が使用されている環境でのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="7560c-114">High-definition user photos are supported only in an environment where both Lync Server 2013 and Exchange 2013 are used.</span></span>

  - <span data-ttu-id="7560c-115">Exchange 2010 上のメールボックスを使用しているユーザーは、常に、ユーザー写真のソースとして AD DS の **thumbnailPhoto** 属性を使用します。</span><span class="sxs-lookup"><span data-stu-id="7560c-115">Users with Mailboxes on Exchange 2010 will always use the **thumbnailPhoto** attribute from AD DS as the source for their user photo.</span></span>

  - <span data-ttu-id="7560c-116">AD DS から **thumbnailPhoto** 属性として保存されているユーザー写真は、外部/フェデレーションの連絡先には表示されません。</span><span class="sxs-lookup"><span data-stu-id="7560c-116">A user photo stored as the **thumbnailPhoto** attribute from AD DS will not be displayed to external / federated contacts.</span></span>

  - <span data-ttu-id="7560c-117">ユーザーの連絡先の写真が AD DS に保存されている場合、使用される画像ファイルは96×96ピクセルで、100 KB のファイルサイズに制限されています。</span><span class="sxs-lookup"><span data-stu-id="7560c-117">If the photos for user contacts are stored in AD DS, the image file used is limited to 96×96 pixels and no more than 100 KB file size.</span></span>

  - <span data-ttu-id="7560c-118">Lync Server と Exchange Server の間の接続が失われた場合、AD DS からのユーザーの低解像度 **thumbnailPhoto** が表示され、内部ユーザーのみになります。</span><span class="sxs-lookup"><span data-stu-id="7560c-118">If connectivity between Lync Server and Exchange Server is lost, the user’s low resolution **thumbnailPhoto** from AD DS will be displayed, and to internal users only.</span></span>

  - <span data-ttu-id="7560c-119">アクティブなスピーカーでビデオが有効になっていない場合、高解像度のユーザー写真が Lync 2013 会議に表示されます。</span><span class="sxs-lookup"><span data-stu-id="7560c-119">High-resolution user photos are displayed in Lync 2013 meetings when an active speaker does not have video enabled.</span></span> <span data-ttu-id="7560c-120">また、ギャラリーのサムネイル写真の上にマウスを移動すると、高解像度の写真が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7560c-120">Also, moving the mouse over thumbnail photo in the gallery will display the high-resolution photo.</span></span>

</div>

<div>

## <a name="user-photos-in-lync-2010"></a><span data-ttu-id="7560c-121">Lync 2010 でのユーザーの写真</span><span class="sxs-lookup"><span data-stu-id="7560c-121">User Photos in Lync 2010</span></span>

<span data-ttu-id="7560c-122">Lync 2010 クライアントでは、次の2つのオプションのいずれかを選択して、自分のプロファイルの写真を表示したり、 **既定の会社の画像** を表示したり、 **web アドレスの画像を表示** したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="7560c-122">In the Lync 2010 client, you can choose from two options to display a photo for your profile, **Default corporate picture** and **Show picture from a web address**.</span></span>

<div>

## <a name="default-corporate-picture"></a><span data-ttu-id="7560c-123">既定の企業の画像</span><span class="sxs-lookup"><span data-stu-id="7560c-123">Default corporate picture</span></span>

<span data-ttu-id="7560c-124">**既定の企業図** オプションを選択すると、Lync は Active Directory ドメインサービスから表示した写真を取得します。</span><span class="sxs-lookup"><span data-stu-id="7560c-124">When you choose the **Default corporate picture** option, Lync gets the photo displayed for you from Active Directory Domain Services.</span></span> <span data-ttu-id="7560c-125">使用される画像は、Active Directory ドメインサービスの **thumbnailPhoto** 属性の値として定義されている画像です。</span><span class="sxs-lookup"><span data-stu-id="7560c-125">The image used is the image defined as the value for the **thumbnailPhoto** attribute in Active Directory Domain Services.</span></span> <span data-ttu-id="7560c-126">これは、Outlook で画像を表示するために Exchange で使用されるファイルと同じです。</span><span class="sxs-lookup"><span data-stu-id="7560c-126">This is the same file that is used by Exchange to display images in Outlook.</span></span>

<span data-ttu-id="7560c-127">Active Directory ドメインサービスからの画像の使用に関する考慮事項には、次のようなものがあります。</span><span class="sxs-lookup"><span data-stu-id="7560c-127">Considerations for using images from Active Directory Domain Services include the following:</span></span>

  - <span data-ttu-id="7560c-128">96ピクセルで最大96ピクセルのサイズの画像のみがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="7560c-128">Only images with dimensions up to 96 pixels by 96 pixels are supported.</span></span> <span data-ttu-id="7560c-129">画像のファイルサイズは、100 KB に制限されています。</span><span class="sxs-lookup"><span data-stu-id="7560c-129">The file size for the image is limited to 100 KB.</span></span>

  - <span data-ttu-id="7560c-130">既定では、ユーザーは **thumbnailPhoto** 属性に使用される画像を変更できますが、Lync クライアントから直接変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="7560c-130">By default, users are able to change the image used for the **thumbnailPhoto** attribute, though not directly through Lync client.</span></span> <span data-ttu-id="7560c-131">Active Directory ドメインサービスを使用して、これを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="7560c-131">You can disable this through Active Directory Domain Services.</span></span>

  - <span data-ttu-id="7560c-132">Active Directory ドメインサービスに保存されている画像は、フェデレーションされた連絡先である場合でも、組織外の連絡先には表示されません。</span><span class="sxs-lookup"><span data-stu-id="7560c-132">Images stored in Active Directory Domain Services are not displayed to contacts external to your organization, even if they are federated contacts.</span></span>

  - <span data-ttu-id="7560c-133">大規模な組織では、多数のユーザーのために画像を保存して取得すると、Active Directory ドメインサービスのデータベースのサイズとパフォーマンスに影響する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7560c-133">In large organizations, storing and retrieving the images for large numbers of users may impact the Active Directory Domain Services database size and performance.</span></span>

  - <span data-ttu-id="7560c-134">限られた画像サイズとファイルサイズは、低解像度の画像のみを使用できることを意味します。</span><span class="sxs-lookup"><span data-stu-id="7560c-134">The limited image dimensions and file size mean that only low resolution images can be used.</span></span>

<div>

## <a name="how-users-manage-their-user-photos-in-active-directory-domain-services"></a><span data-ttu-id="7560c-135">Active Directory ドメインサービスでユーザーの写真を管理する方法</span><span class="sxs-lookup"><span data-stu-id="7560c-135">How users manage their user photos in Active Directory Domain Services</span></span>

<span data-ttu-id="7560c-136">ユーザーは、Lync 2010 クライアントを介して、Active Directory ドメインサービスプロファイルで使用されている画像を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="7560c-136">User cannot change the image used in their Active Directory Domain Services profile directly through Lync 2010 client.</span></span> <span data-ttu-id="7560c-137">使用できる場合は、次のいずれかのオプションを使うことができます。</span><span class="sxs-lookup"><span data-stu-id="7560c-137">They can use one of the following options to do so, if available:</span></span>

  - <span data-ttu-id="7560c-138">**SharePoint Server**   ユーザーは、SharePoint サーバー上の [個人用サイト] に写真をアップロードし、 [sharepoint でプロファイルの同期を構成](https://go.microsoft.com/fwlink/p/?linkid=507466) して、その写真を Active Directory Domain Services の **thumbnailPhoto** 属性と同期させることができます。</span><span class="sxs-lookup"><span data-stu-id="7560c-138">**SharePoint Server**   Users can upload a photo to ‘My Site’ on a SharePoint Server and then [configure profile synchronization in SharePoint](https://go.microsoft.com/fwlink/p/?linkid=507466) to synchronize the photo to the **thumbnailPhoto** attribute in Active Directory Domain Services.</span></span>

  - <span data-ttu-id="7560c-139">**公開可能な URL に保存された写真**   ユーザーは、使用する画像の公開可能な URL を指定してユーザーの写真を構成できます。</span><span class="sxs-lookup"><span data-stu-id="7560c-139">**Photo stored on publicly accessible URL**   Users can configure their user photo specifying a publicly accessible URL for the image that they want to use.</span></span> <span data-ttu-id="7560c-140">画像には、パスワードなしでアクセスできるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7560c-140">The image must be publicly accessible without a password.</span></span> <span data-ttu-id="7560c-141">指定した web アドレスに保存されている画像は、プレゼンス情報の連絡先カードカテゴリを通じて他のユーザーに転送されます。</span><span class="sxs-lookup"><span data-stu-id="7560c-141">The image stored at the specified web address is transferred to other users through the contact card category in the presence information.</span></span> <span data-ttu-id="7560c-142">Lync クライアントでユーザーの写真を表示する必要がある場合は、指定した web アドレスから画像を取得します。</span><span class="sxs-lookup"><span data-stu-id="7560c-142">When Lync client needs to display a user photo, it retrieves the image from the specified web address.</span></span>

  - <span data-ttu-id="7560c-143">**Windows PowerShell 用 Exchange 2010 コマンドレット**  管理者は、ThumbnailPhoto 属性を管理するために、Exchange 2010 管理シェルで、Import として **thumbnailPhoto** の [dataproperty](https://go.microsoft.com/fwlink/p/?linkid=507468)コマンドレットを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="7560c-143">**Exchange 2010 cmdlets for Windows PowerShell**   Administrators can run the [Import-RecipientDataProperty](https://go.microsoft.com/fwlink/p/?linkid=507468) cmdlet in the Exchange 2010 Management Shell in to manage the **thumbnailPhoto** attribute.</span></span> <span data-ttu-id="7560c-144">Exchange 2010 コマンドレットを使用して画像をインポートすると、ファイルサイズは 10 KB に制限されます。</span><span class="sxs-lookup"><span data-stu-id="7560c-144">When images are imported with Exchange 2010 cmdlets, the file size is limited to 10 KB.</span></span>

  - <span data-ttu-id="7560c-145">**サードパーティ製ツール**   ユーザーは、自分の写真だけを **thumbnailPhoto** 属性にアップロードできます。</span><span class="sxs-lookup"><span data-stu-id="7560c-145">**Third Party tools**   Users can upload only their own photo to for the **thumbnailPhoto** attribute.</span></span>

</div>

</div>

<div>

## <a name="show-a-picture-from-a-web-address"></a><span data-ttu-id="7560c-146">Web アドレスの画像を表示する</span><span class="sxs-lookup"><span data-stu-id="7560c-146">Show a picture from a web address</span></span>

<span data-ttu-id="7560c-147">[ **Web アドレスから画像を表示** する] オプションを選ぶと、lync では、入力したアドレスに画像が表示され、lync でユーザー写真の画像が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7560c-147">When you choose the **Show a picture from a web address** option, Lync gets the image at the address you enter and displays it for your user photo in Lync.</span></span>

<span data-ttu-id="7560c-148">Web アドレスからの画像の使用に関する考慮事項には、次のものがあります。</span><span class="sxs-lookup"><span data-stu-id="7560c-148">Considerations for using images from a web address include the following:</span></span>

  - <span data-ttu-id="7560c-149">ファイルサイズの制限は、[新しい-CsClientPolicy](https://go.microsoft.com/fwlink/p/?linkid=507463)コマンドレットで定義された、クライアントポリシーの **Maxphotosizekb** 属性によって決定されます。</span><span class="sxs-lookup"><span data-stu-id="7560c-149">File size limits are determined by the **MaxPhotoSizeKB** attribute in the client policy, defined with the [New-CsClientPolicy](https://go.microsoft.com/fwlink/p/?linkid=507463) cmdlet.</span></span> <span data-ttu-id="7560c-150">既定のサイズ制限は、30 KB です。</span><span class="sxs-lookup"><span data-stu-id="7560c-150">The default size limit is 30 KB.</span></span> <span data-ttu-id="7560c-151">最大値は 100 KB です。</span><span class="sxs-lookup"><span data-stu-id="7560c-151">The maximum value is 100 KB.</span></span> <span data-ttu-id="7560c-152">画像の解像度には制限はありませんが、サイズ制限を超えている画像ファイルを使用しようとしても、Lync クライアントにダウンロードされません。</span><span class="sxs-lookup"><span data-stu-id="7560c-152">There is no restriction on the resolution of the image, but if you try to use an image file that exceeds the size limit it will not be downloaded to Lync clients.</span></span> <span data-ttu-id="7560c-153">この値を0に設定すると、すべてのユーザーの写真を Lync で使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="7560c-153">You can set the value to 0 to disable all user photos from being used in Lync.</span></span>

  - <span data-ttu-id="7560c-154">Web アドレスからのユーザーの写真は、フェデレーションされた外部の連絡先から見ることができます。</span><span class="sxs-lookup"><span data-stu-id="7560c-154">User photos from a web address can be seen by external federated contacts.</span></span>

</div>

<div>

## <a name="managing-users-photo-with-client-policy-cmdlets"></a><span data-ttu-id="7560c-155">クライアントポリシーコマンドレットを使用してユーザーの写真を管理する</span><span class="sxs-lookup"><span data-stu-id="7560c-155">Managing user’s photo with Client Policy cmdlets</span></span>

<span data-ttu-id="7560c-156">Lync Server 2010 では、クライアントポリシー設定は CsClientPolicy コマンドレットで構成されています。</span><span class="sxs-lookup"><span data-stu-id="7560c-156">In Lync Server 2010, client policy settings are configured with the CsClientPolicy cmdlets.</span></span> <span data-ttu-id="7560c-157">構成済みのポリシー設定は、インバンドプロビジョニングを通じてクライアントに送信されます。</span><span class="sxs-lookup"><span data-stu-id="7560c-157">The configured policy settings are sent to clients through in-band provisioning.</span></span> <span data-ttu-id="7560c-158">ユーザーの写真エクスペリエンスを決定する CsClientPolicy コマンドレットの2つのパラメーターは、 **DisplayPhoto** と **Maxphotosizekb** です。</span><span class="sxs-lookup"><span data-stu-id="7560c-158">The two parameters of the CsClientPolicy cmdlets that determine the user photo experience are **DisplayPhoto** and **MaxPhotoSizeKB**.</span></span> <span data-ttu-id="7560c-159">**DisplayPhoto** と **Maxphotosizekb** の対応するインバンドプロビジョニングパラメーターは、 **PhotoUsage** という名前です。</span><span class="sxs-lookup"><span data-stu-id="7560c-159">The corresponding in-band provisioning parameter for **DisplayPhoto** and **MaxPhotoSizeKB** is named **PhotoUsage**.</span></span> <span data-ttu-id="7560c-160">**PhotoUsage** パラメーターの値は、 **endpointConfiguration** **provisionGroup** 経由でクライアントに送信されます。</span><span class="sxs-lookup"><span data-stu-id="7560c-160">Values for the **PhotoUsage** parameter are send to clients through the **endpointConfiguration** **provisionGroup**.</span></span> <span data-ttu-id="7560c-161">詳細については [、「クライアントポリシーと設定の概要](https://go.microsoft.com/fwlink/?linkid=507470) 」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7560c-161">See [Overview of Client Policies and Settings](https://go.microsoft.com/fwlink/?linkid=507470) for more information.</span></span>

<span data-ttu-id="7560c-162">**DisplayPhoto** パラメーターの値は、ユーザーの写真イメージのソースを決定します。</span><span class="sxs-lookup"><span data-stu-id="7560c-162">The **DisplayPhoto** parameter value determines the source of the user's photo image.</span></span> <span data-ttu-id="7560c-163">サポートされている値は、次の表に記載されています。</span><span class="sxs-lookup"><span data-stu-id="7560c-163">The supported values are included in the following table.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7560c-164">DisplayPhoto パラメーター値</span><span class="sxs-lookup"><span data-stu-id="7560c-164">DisplayPhoto parameter value</span></span></th>
<th><span data-ttu-id="7560c-165">画像ソース</span><span class="sxs-lookup"><span data-stu-id="7560c-165">Image source</span></span></th>
<th><span data-ttu-id="7560c-166">Lync 2010 クライアントの設定</span><span class="sxs-lookup"><span data-stu-id="7560c-166">Lync 2010 client settings</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7560c-167">NoPhoto</span><span class="sxs-lookup"><span data-stu-id="7560c-167">NoPhoto</span></span></p></td>
<td><p><span data-ttu-id="7560c-168">なし</span><span class="sxs-lookup"><span data-stu-id="7560c-168">none</span></span></p></td>
<td><p><span data-ttu-id="7560c-169"><strong>自分の写真を表示しない</strong></span><span class="sxs-lookup"><span data-stu-id="7560c-169"><strong>Do not show my picture</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7560c-170">PhotoFromADOnly</span><span class="sxs-lookup"><span data-stu-id="7560c-170">PhotoFromADOnly</span></span></p></td>
<td><p><span data-ttu-id="7560c-171">Active Directory</span><span class="sxs-lookup"><span data-stu-id="7560c-171">Active Directory</span></span></p></td>
<td><p><span data-ttu-id="7560c-172"><strong>既定の企業の画像</strong></span><span class="sxs-lookup"><span data-stu-id="7560c-172"><strong>Default corporate picture</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7560c-173">すべての写真</span><span class="sxs-lookup"><span data-stu-id="7560c-173">AllPhotos</span></span></p></td>
<td><p><span data-ttu-id="7560c-174">Web アドレス</span><span class="sxs-lookup"><span data-stu-id="7560c-174">Web address</span></span></p></td>
<td><p><span data-ttu-id="7560c-175"><strong>Web アドレスの画像を表示する</strong></span><span class="sxs-lookup"><span data-stu-id="7560c-175"><strong>Show a picture from a web address</strong></span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="how-lync-2010-client-gets-photos"></a><span data-ttu-id="7560c-176">Lync 2010 クライアントで写真を取得する方法</span><span class="sxs-lookup"><span data-stu-id="7560c-176">How Lync 2010 client gets photos</span></span>

<span data-ttu-id="7560c-177">Lync 2010 では、ユーザーの写真はアドレス帳サービスによってサーバー上で管理されます。</span><span class="sxs-lookup"><span data-stu-id="7560c-177">In Lync 2010, user photos are managed on the server by the Address Book Service.</span></span> <span data-ttu-id="7560c-178">Lync クライアントは、最初に、配布リスト展開 web サービスを通じて公開されるサーバー上のアドレス帳 Web クエリ (ABWQ) サービスを照会することによって、ユーザーの写真を取得します。</span><span class="sxs-lookup"><span data-stu-id="7560c-178">Lync client gets user photos by first querying the Address Book Web Query (ABWQ) service on the server, which is exposed through the Distribution List Expansion web service.</span></span> <span data-ttu-id="7560c-179">クライアントはイメージファイルを受け取り、ユーザーのキャッシュにコピーして、表示する必要があるたびにイメージをダウンロードしないようにします。</span><span class="sxs-lookup"><span data-stu-id="7560c-179">The client receives the image file and then copies it to the user's cache to avoid downloading the image each time it needs to be displayed.</span></span> <span data-ttu-id="7560c-180">クエリから返された属性値は、ユーザーのキャッシュされたアドレス帳サービスエントリにも格納されます。</span><span class="sxs-lookup"><span data-stu-id="7560c-180">The attribute values returned from the query are also stored in the cached Address Book Service entry for the user.</span></span> <span data-ttu-id="7560c-181">アドレス帳サービスは、キャッシュされているすべての画像を24時間ごとに削除します。つまり、サーバー上のキャッシュで新しいユーザーの画像が更新されるまでに最大24時間かかる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7560c-181">The Address Book Service deletes all cached images every 24 hours, which means that it can take up to 24 hours for new user images to be updated in the cache on the server.</span></span> <span data-ttu-id="7560c-182">[CsAddressBook](https://docs.microsoft.com/powershell/module/skype/Update-CsAddressBook)コマンドレットを使用して、キャッシュを強制的に更新できます。</span><span class="sxs-lookup"><span data-stu-id="7560c-182">You can force an update to the cache by using the [Update-CsAddressBook](https://docs.microsoft.com/powershell/module/skype/Update-CsAddressBook) cmdlet.</span></span>

<span data-ttu-id="7560c-183">プレゼンス状態に含まれているユーザーの写真にも、新しい画像が利用可能かどうかを判断するために Lync クライアントによって使用されるハッシュ値が関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="7560c-183">User photos included in Presence status also have an associated hash value that Lync client uses to determine whether there is a newer image available.</span></span> <span data-ttu-id="7560c-184">プレゼンス状態で使用される画像ファイルへの変更がクライアントに自動的に通知されます。</span><span class="sxs-lookup"><span data-stu-id="7560c-184">The client is automatically notified of changes to the image file used in Presence status.</span></span>

<div class=" ">


> [!NOTE]  
> <span data-ttu-id="7560c-185">写真は GalContacts データベースに保存されていないため、ユーザーの写真をダウンロードしても、クライアントポリシー (<A href="https://go.microsoft.com/fwlink/p/?linkid=507508">CsClientPolicy</A>) の<STRONG>addressbookavailability</STRONG>の設定に依存していません。</span><span class="sxs-lookup"><span data-stu-id="7560c-185">Because photos are not stored in the GalContacts.db database, downloading user photos is not dependent on the <STRONG>AddressBookAvailability</STRONG> setting in the client policy (<A href="https://go.microsoft.com/fwlink/p/?linkid=507508">Set-CsClientPolicy</A>).</span></span>



</div>

<span data-ttu-id="7560c-186">ABWQ サービスへのクエリには、次の属性が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7560c-186">The query to the ABWQ service includes the following attributes:</span></span>

  - <span data-ttu-id="7560c-187">**Photohash**   バイナリ写真データのハッシュ値。現在の写真が変更されたかどうかを確認するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7560c-187">**PhotoHash**   The hash value of the binary photo data, and is used to determine whether the current photo has changed.</span></span>

  - <span data-ttu-id="7560c-188">**PhotoRelPath**   サーバーに保存されている画像ファイルへの相対パスです。</span><span class="sxs-lookup"><span data-stu-id="7560c-188">**PhotoRelPath**   The relative path to the image file stored on the server.</span></span>

  - <span data-ttu-id="7560c-189">**Photosize**   画像ファイルのサイズ (バイト単位) です。</span><span class="sxs-lookup"><span data-stu-id="7560c-189">**PhotoSize**   The size of the image file, in bytes.</span></span>

  - <span data-ttu-id="7560c-190">**TimeStamp**   イメージファイルが最後にサーバーからダウンロードされ、クライアントキャッシュにコピーされた日付と時刻。</span><span class="sxs-lookup"><span data-stu-id="7560c-190">**TimeStamp**   The date and time at which the image file was last downloaded from the server and copied to the client cache.</span></span>

<span data-ttu-id="7560c-191">次に、画像ファイルを取得した後、Lync 2010 クライアントは、クエリから返された属性値と、インバンドプロビジョニングからクライアントが受け取った属性値とを比較して、それらが異なるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="7560c-191">Next, after retrieving the image file, Lync 2010 client compares the attribute values returned from the query against the attribute values received by the client from in-band provisioning to see if they are different.</span></span> <span data-ttu-id="7560c-192">値が異なる場合、クライアントは、サインインしたユーザーの画像ファイルを HTTP GET 要求で取得します。</span><span class="sxs-lookup"><span data-stu-id="7560c-192">If the values are different, the client retrieves the image file of the signed-in user with an HTTP GET request.</span></span>

<span data-ttu-id="7560c-193">さらに、クライアントは、キャッシュされたバージョンのイメージファイルが作成された時点から24時間ごとにサーバーに確認して、サーバー上の **Photohash** 属性の値とクライアント上の値とを比較します。</span><span class="sxs-lookup"><span data-stu-id="7560c-193">Additionally, the client checks with the server every 24 hours from the time at which the cached version of the image file was created to compare the value of the **PhotoHash** attribute on the server with the value on the client.</span></span> <span data-ttu-id="7560c-194">値が異なる場合は、画像ファイルが変更されていることがクライアントに認識されます。</span><span class="sxs-lookup"><span data-stu-id="7560c-194">If the values are different, the client knows that the image file has changed.</span></span> <span data-ttu-id="7560c-195">更新された画像ファイルを取得するために、クライアントはもう一度 ABWQ サービスを照会して、クライアントキャッシュのイメージファイルをサーバー上の画像ファイルに更新します。これにより、クライアントキャッシュ内のファイルの **タイムスタンプ** もリセットされます。</span><span class="sxs-lookup"><span data-stu-id="7560c-195">To obtain the updated image file, the client again queries the ABWQ service to update the image file in the client cache with the image file on the server, which also resets the **TimeStamp** on the file in the client cache.</span></span>

<span data-ttu-id="7560c-196">次に示すのは、ABWQ サービスへのクエリに対する応答の例です。</span><span class="sxs-lookup"><span data-stu-id="7560c-196">The following is an example response to a query to the ABWQ service:</span></span>
```xml
    <Attribute>
              <Name>PhotoRelPath</Name>
              <Value>efa6096aed2746cb9ab2037f7dbdde9d.f2eeeb5946db54a7aa607ecd3ae09d
              95.photo</Value>
              <Values xmlns:d6p1="http://schemas.microsoft.com/2003/10/Serialization/Arrays" i:nil="true" />
    </Attribute>
    <Attribute>
              <Name>PhotoHash</Name>
              <Value>f2eeeb5946db54a7aa607ecd3ae09d95</Value>
              <Values xmlns:d6p1="http://schemas.microsoft.com/2003/10/Serialization/Arrays" i:nil="true" />
    </Attribute>
    <Attribute>
         <Name>PhotoSize</Name>
         <Value>4620</Value>
         <Valuesxmlns:d6p1="http://schemas.microsoft.com/2003/10/Serialization/Arrays"
    i:nil="true" />
    </Attribute>
```

</div>

</div>

<div>

## <a name="user-photos-in-lync-2013"></a><span data-ttu-id="7560c-197">Lync 2013 でのユーザーの写真</span><span class="sxs-lookup"><span data-stu-id="7560c-197">User photos in Lync 2013</span></span>

<span data-ttu-id="7560c-198">Lync 2013 では、ユーザー写真用の高解像度の画像のサポートが導入されました。</span><span class="sxs-lookup"><span data-stu-id="7560c-198">Lync 2013 introduced support for high-resolution images for user photos.</span></span> <span data-ttu-id="7560c-199">Lync 2013 には、ユーザーの写真を Exchange 2013 上のユーザーのメールボックスに保存する機能もサポートされています。これにより、Lync 2010 に含まれる画像の解像度とサイズの制限が削除されます。</span><span class="sxs-lookup"><span data-stu-id="7560c-199">Lync 2013 also includes support for storing user photos in the user's mailbox on Exchange 2013, which removes the image resolution and size limitations present in Lync 2010.</span></span> <span data-ttu-id="7560c-200">Lync 2013 でのユーザーの写真は、最大 20 MB のファイルサイズで、648ピクセルで最大648ピクセルにすることができます。</span><span class="sxs-lookup"><span data-stu-id="7560c-200">User photos in Lync 2013 can be up to 648 pixels by 648 pixels with a file size of up to 20 MB.</span></span> <span data-ttu-id="7560c-201">Lync 2013 の高解像度の写真は、Exchange 2013 のユーザーのメールボックスに配置されている必要があります。また、Lync 2013 クライアントでのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="7560c-201">High-resolution photos in Lync 2013 must be located in the user's mailbox on Exchange 2013, and are supported only with Lync 2013 client.</span></span> <span data-ttu-id="7560c-202">Exchange との統合により、2013バージョンの Lync、Exchange、および SharePoint の Oauth という新しい承認フレームワークが利用されます。</span><span class="sxs-lookup"><span data-stu-id="7560c-202">This integration with Exchange takes advantage of the new authorization framework included in the 2013 versions of Lync, Exchange, and SharePoint called Oauth.</span></span>

<span data-ttu-id="7560c-203">展開で Exchange 2013 が使用されていない場合、ユーザーの写真のサポートは Lync 2010 と同じです。</span><span class="sxs-lookup"><span data-stu-id="7560c-203">If Exchange 2013 is not used in your deployment, support for user photos is the same as with Lync 2010.</span></span> <span data-ttu-id="7560c-204">ただし、使用する写真を選ぶためのユーザーオプションは、Lync 2013 クライアントでは異なります。</span><span class="sxs-lookup"><span data-stu-id="7560c-204">However, the user options to choose the photo to use are different in Lync 2013 client.</span></span> <span data-ttu-id="7560c-205">Lync 2013 クライアントでは、ユーザーは [ **写真を非表示** にする] または [ **マイピクチャを表示** する] のいずれかを選ぶことができます。</span><span class="sxs-lookup"><span data-stu-id="7560c-205">In Lync 2013 client, users can select either **Hide my picture** or **Show my picture**.</span></span> <span data-ttu-id="7560c-206">[ **Web サイトの画像を表示** する] オプションは既定では利用できませんが、クライアントポリシーを割り当てることで有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="7560c-206">The option **Show a picture from a website** is not available by default, but can be enabled by assigning a client policy.</span></span>

<div>

## <a name="hide-my-picture"></a><span data-ttu-id="7560c-207">写真を表示しない</span><span class="sxs-lookup"><span data-stu-id="7560c-207">Hide my picture</span></span>

<span data-ttu-id="7560c-208">ユーザー写真の設定は、Lync 2013 の [ **オプション** ] ダイアログにあります。</span><span class="sxs-lookup"><span data-stu-id="7560c-208">Settings for user photos are on the **Options** dialog in Lync 2013.</span></span> <span data-ttu-id="7560c-209">[自分の **写真を表示** しない] を選ぶと、lync クライアントではユーザーの写真は表示されませんが、自分の写真は連絡先カードと lync の外部に表示されたままになります。</span><span class="sxs-lookup"><span data-stu-id="7560c-209">When you choose **Hide my picture**, no user photo is displayed for you in Lync client, but your photo is still displayed on your contact card and outside of Lync.</span></span>

</div>

<div>

## <a name="show-my-picture"></a><span data-ttu-id="7560c-210">自分の写真を表示</span><span class="sxs-lookup"><span data-stu-id="7560c-210">Show my picture</span></span>

<span data-ttu-id="7560c-211">**[自分の写真を表示** する] オプションを選択すると、lync クライアントおよび lync での会話で他のユーザーにユーザーの写真が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7560c-211">When you choose the **Show my picture** option, your user photo is displayed in your Lync client and to other users in Lync conversations.</span></span> <span data-ttu-id="7560c-212">使用されている画像は、AD DS に保存されているものです。</span><span class="sxs-lookup"><span data-stu-id="7560c-212">The image used is the one stored in AD DS.</span></span>

</div>

<div>

## <a name="show-a-picture-from-a-website"></a><span data-ttu-id="7560c-213">Web サイトの画像を表示する</span><span class="sxs-lookup"><span data-stu-id="7560c-213">Show a picture from a website</span></span>

<span data-ttu-id="7560c-214">クライアントポリシーを有効にするように設定した後、[ **web サイトの画像を表示** する] オプションが Lync 2013 で使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="7560c-214">The **Show picture from a website** option becomes available in Lync 2013 after a client policy is set to enable it.</span></span> <span data-ttu-id="7560c-215">クライアントバージョンは、Lync 累積更新プログラムと共にインストールされている15.0.4535.1002 よりも新しいバージョンである必要があります。 [2013 年11月](https://go.microsoft.com/fwlink/p/?linkid=509908)。</span><span class="sxs-lookup"><span data-stu-id="7560c-215">The client version must be newer than 15.0.4535.1002, which is installed with the [Lync Cumulative Updates: November 2013](https://go.microsoft.com/fwlink/p/?linkid=509908).</span></span> <span data-ttu-id="7560c-216">クライアントの変更を確認するには、ユーザーがもう一度ログアウトしてから再びログインしなければならない場合があります。</span><span class="sxs-lookup"><span data-stu-id="7560c-216">Users may need to log out and then back in again to see the changes in the client.</span></span>

<span data-ttu-id="7560c-217">Lync Server 管理シェルで [set-CsClientPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsClientPolicy)ポリシーを実行して、 **web サイトの設定から画像が表示** されるようにクライアントポリシーを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="7560c-217">You can set the client policy to enable to **Show picture from a website** setting by running the [Set-CsClientPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsClientPolicy) policy in the Lync Server Management Shell.</span></span> <span data-ttu-id="7560c-218">展開内のすべてのユーザーに対してグローバルにポリシーを設定する方法を示すコマンドレットの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="7560c-218">The following example cmdlets demonstrate how to set the policy globally for all users in your deployment:</span></span>

   ```powershell
    $pe=New-CsClientPolicyEntry -Name EnablePresencePhotoOptions -Value True
   ```

   ```powershell
    $po=Get-CsClientPolicy -Identity Global
   ```

   ```powershell
    $po.PolicyEntry.Add($pe)
   ```

   ```powershell
    Set-CsClientPolicy -Instance $po
   ```


<span data-ttu-id="7560c-219">ユーザーのメールボックスに画像がアップロードされると、Exchange では、クライアントアプリケーションで使用できる画像の低解像度バージョンが自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="7560c-219">When an image is uploaded to the user’s mailbox, Exchange automatically creates a lower resolution version of the image which can be used in client applications.</span></span> <span data-ttu-id="7560c-220">また、ユーザーの写真は、AD DS でも更新されます。</span><span class="sxs-lookup"><span data-stu-id="7560c-220">The user photo is also updated in AD DS.</span></span>

<div class=" ">


> [!NOTE]  
> <span data-ttu-id="7560c-221">AD DS でイメージファイルが更新されると、48 x 48 ピクセルのイメージが作成され、AD DS の thumbnailPhoto に使用されます。</span><span class="sxs-lookup"><span data-stu-id="7560c-221">When an image file is updated in AD DS, a 48 x 48 pixel image is created and used for the thumbnailPhoto in AD DS.</span></span> <span data-ttu-id="7560c-222">既存の画像はすべて置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="7560c-222">Any existing image is replaced.</span></span> <span data-ttu-id="7560c-223">そのため、96 x 96 のイメージを AD DS に追加した場合は、新しい 48 x 48 イメージによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="7560c-223">So if you added a 96 x 96 image to AD DS, it will be overwritten with the new 48 x 48 image.</span></span> <span data-ttu-id="7560c-224">これは重要なのは、Lync 2010 クライアントを使用している環境内にユーザーがいて、ユーザーの写真が AD DS から取得されるためです。</span><span class="sxs-lookup"><span data-stu-id="7560c-224">This is only important is you have users in your environment using Lync 2010 clients, as those clients will obtain user photos from AD DS.</span></span> <span data-ttu-id="7560c-225">組織内に Lync 2010 クライアントがある場合は、96 x 96 ピクセルのイメージをインポートして、AD DS によって作成されたものを置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="7560c-225">You can import 96 x 96 pixel images to replace the ones created by AD DS if you have Lync 2010 clients in your organization.</span></span>



</div>

</div>

<div>

## <a name="user-photo-support-in-lync-2013"></a><span data-ttu-id="7560c-226">Lync 2013 でのユーザー写真のサポート</span><span class="sxs-lookup"><span data-stu-id="7560c-226">User photo support in Lync 2013</span></span>

<span data-ttu-id="7560c-227">Lync 2013 では、次の表に示すように、ユーザーの写真で3つの画像解像度がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="7560c-227">In Lync 2013, three image resolutions are supported for user photos as described in the following table.</span></span> <span data-ttu-id="7560c-228">使用される画像は、Lync ユーザーに割り当てられているクライアントポリシーの設定によって決まります。</span><span class="sxs-lookup"><span data-stu-id="7560c-228">The image that is used is determined by the client policy setting assigned to Lync users.</span></span> <span data-ttu-id="7560c-229">詳細については、このトピックの「クライアントポリシーコマンドレットを使用してユーザーの写真を管理する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7560c-229">See “Managing user’s photo with Client Policy cmdlets” in this topic for more information.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7560c-230">画像の解像度 (ピクセル)</span><span class="sxs-lookup"><span data-stu-id="7560c-230">Image resolution (pixels)</span></span></th>
<th><span data-ttu-id="7560c-231">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="7560c-231">Application</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7560c-232">48 x 48</span><span class="sxs-lookup"><span data-stu-id="7560c-232">48 x 48</span></span></p></td>
<td><p><span data-ttu-id="7560c-233">高解像度の画像が選択されていない場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="7560c-233">Used if no higher resolution image is selected</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7560c-234">96 x 96</span><span class="sxs-lookup"><span data-stu-id="7560c-234">96 x 96</span></span></p></td>
<td><p><span data-ttu-id="7560c-235">Outlook Web App および Outlook 2013 で使用</span><span class="sxs-lookup"><span data-stu-id="7560c-235">Used in Outlook Web App and Outlook 2013</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7560c-236">648 x 648</span><span class="sxs-lookup"><span data-stu-id="7560c-236">648 x 648</span></span></p></td>
<td><p><span data-ttu-id="7560c-237">Lync 2013 デスクトップクライアントおよび Lync 2013 Web アプリで使用</span><span class="sxs-lookup"><span data-stu-id="7560c-237">Used in Lync 2013 desktop client and Lync 2013 Web App</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7560c-238">Exchange 2013 でメールボックスが有効になっているユーザーは、高解像度の写真など、Outlook Web Access または Lync 2013 クライアントオプションを使用して、別の画像をアップロードできます。</span><span class="sxs-lookup"><span data-stu-id="7560c-238">Any user with a mailbox enabled in Exchange 2013 can upload a different image, including high-resolution photos, through Outlook Web Access or Lync 2013 client options.</span></span> <span data-ttu-id="7560c-239">使用する画像の推奨設定は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="7560c-239">The recommended settings for images used include:</span></span>

  - <span data-ttu-id="7560c-240">648 x 648 ピクセルの **画像解像度**</span><span class="sxs-lookup"><span data-stu-id="7560c-240">**Image Resolution**   648 by 648 pixels</span></span>

  - <span data-ttu-id="7560c-241">**色深度**   24 ビット</span><span class="sxs-lookup"><span data-stu-id="7560c-241">**Color Depth**   24-bit</span></span>

  - <span data-ttu-id="7560c-242">**画像ファイルのサイズ**   が最大 20 MB</span><span class="sxs-lookup"><span data-stu-id="7560c-242">**Image file size**   up to 20 MB</span></span>

  - <span data-ttu-id="7560c-243">**ファイル形式**   JPEG</span><span class="sxs-lookup"><span data-stu-id="7560c-243">**File format**   JPEG</span></span>

<span data-ttu-id="7560c-244">648ピクセル x 648 ピクセルの標準的な24ビット JPEG 画像のファイルサイズは約 240 KB であるため、4ユーザー写真ごとに 1 MB の記憶領域が必要です。</span><span class="sxs-lookup"><span data-stu-id="7560c-244">A typical 24-bit JPEG image that is 648 pixels by 648 pixels has a file size of about 240 KB, so 1 MB of storage space is needed for every 4 user photos.</span></span>

<span data-ttu-id="7560c-245"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7560c-245"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

