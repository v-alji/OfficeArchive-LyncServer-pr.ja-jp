---
title: 'Lync Server 2013: 2 要素認証の計画'
description: 'Lync Server 2013: 2 要素認証の計画'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for two-factor authentication
ms:assetid: 16f08710-8961-4659-acbf-ebb95a198fb4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn308562(v=OCS.15)
ms:contentKeyID: 54973683
ms.date: 04/06/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6a3a2cd5508f6ce9a8a389b0059a09747b9f9a09
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442874"
---
# <a name="planning-for-two-factor-authentication-in-lync-server-2013"></a><span data-ttu-id="c62b5-103">Lync Server 2013 での2要素認証の計画</span><span class="sxs-lookup"><span data-stu-id="c62b5-103">Planning for two-factor authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c62b5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c62b5-104">

<span> </span></span></span>

<span data-ttu-id="c62b5-105">_**最終更新日:** 2015-04-06_</span><span class="sxs-lookup"><span data-stu-id="c62b5-105">_**Topic Last Modified:** 2015-04-06_</span></span>

<span data-ttu-id="c62b5-106">Microsoft Lync Server 2013 環境を構成して、2段階認証をサポートする場合の展開に関する考慮事項の一覧を次に示します。</span><span class="sxs-lookup"><span data-stu-id="c62b5-106">The following is a list of deployment considerations when configuring a Microsoft Lync Server 2013 environment to support two-factor authentication.</span></span>

<div>

## <a name="client-support"></a><span data-ttu-id="c62b5-107">クライアントのサポート</span><span class="sxs-lookup"><span data-stu-id="c62b5-107">Client Support</span></span>

<span data-ttu-id="c62b5-108">Lync 2013 の Lync Server 2013 の累積更新プログラム: 2013 デスクトップクライアントとすべてのモバイルクライアントで現在、2要素認証がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="c62b5-108">The Lync 2013 Cumulative Updates for Lync Server 2013: July 2013 desktop client and all mobile clients currently support two-factor authentication.</span></span>

</div>

<div>

## <a name="topology-requirements"></a><span data-ttu-id="c62b5-109">トポロジ要件</span><span class="sxs-lookup"><span data-stu-id="c62b5-109">Topology Requirements</span></span>

<span data-ttu-id="c62b5-110">お客様は、lync Server 2013 の累積更新プログラムを使用して、専用の Lync Server 2013 を使って2要素認証を展開することを強くお勧めします。これには、2013年7月のエッジ、監督、ユーザープールがあります。</span><span class="sxs-lookup"><span data-stu-id="c62b5-110">Customers are strongly encouraged to deploy two-factor authentication using dedicated Lync Server 2013 with Cumulative Updates for Lync Server 2013: July 2013 Edge, Director, and User Pools.</span></span> <span data-ttu-id="c62b5-111">Lync ユーザーに対してパッシブ認証を有効にするには、他の役割やサービスについて、次のような他の認証方法を無効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c62b5-111">To enable passive authentication for Lync users, other authentication methods must be disabled for other roles and services, including the following:</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c62b5-112">構成の種類</span><span class="sxs-lookup"><span data-stu-id="c62b5-112">Configuration Type</span></span></th>
<th><span data-ttu-id="c62b5-113">サービスの種類</span><span class="sxs-lookup"><span data-stu-id="c62b5-113">Service Type</span></span></th>
<th><span data-ttu-id="c62b5-114">サーバーの役割</span><span class="sxs-lookup"><span data-stu-id="c62b5-114">Server Role</span></span></th>
<th><span data-ttu-id="c62b5-115">無効にする認証の種類</span><span class="sxs-lookup"><span data-stu-id="c62b5-115">Authentication Type to Disable</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c62b5-116">Web サービス</span><span class="sxs-lookup"><span data-stu-id="c62b5-116">Web Service</span></span></p></td>
<td><p><span data-ttu-id="c62b5-117">WebServer</span><span class="sxs-lookup"><span data-stu-id="c62b5-117">WebServer</span></span></p></td>
<td><p><span data-ttu-id="c62b5-118">ディレクター</span><span class="sxs-lookup"><span data-stu-id="c62b5-118">Director</span></span></p></td>
<td><p><span data-ttu-id="c62b5-119">Kerberos、NTLM、証明書</span><span class="sxs-lookup"><span data-stu-id="c62b5-119">Kerberos, NTLM, and Certificate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c62b5-120">Web サービス</span><span class="sxs-lookup"><span data-stu-id="c62b5-120">Web Service</span></span></p></td>
<td><p><span data-ttu-id="c62b5-121">WebServer</span><span class="sxs-lookup"><span data-stu-id="c62b5-121">WebServer</span></span></p></td>
<td><p><span data-ttu-id="c62b5-122">フロントエンド</span><span class="sxs-lookup"><span data-stu-id="c62b5-122">Front End</span></span></p></td>
<td><p><span data-ttu-id="c62b5-123">Kerberos、NTLM、証明書</span><span class="sxs-lookup"><span data-stu-id="c62b5-123">Kerberos, NTLM, and Certificate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c62b5-124">プロキシ</span><span class="sxs-lookup"><span data-stu-id="c62b5-124">Proxy</span></span></p></td>
<td><p><span data-ttu-id="c62b5-125">EdgeServer</span><span class="sxs-lookup"><span data-stu-id="c62b5-125">EdgeServer</span></span></p></td>
<td><p><span data-ttu-id="c62b5-126">Edge</span><span class="sxs-lookup"><span data-stu-id="c62b5-126">Edge</span></span></p></td>
<td><p><span data-ttu-id="c62b5-127">Kerberos および NTLM</span><span class="sxs-lookup"><span data-stu-id="c62b5-127">Kerberos and NTLM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c62b5-128">プロキシ</span><span class="sxs-lookup"><span data-stu-id="c62b5-128">Proxy</span></span></p></td>
<td><p><span data-ttu-id="c62b5-129">レジストラー</span><span class="sxs-lookup"><span data-stu-id="c62b5-129">Registrar</span></span></p></td>
<td><p><span data-ttu-id="c62b5-130">フロントエンド</span><span class="sxs-lookup"><span data-stu-id="c62b5-130">Front End</span></span></p></td>
<td><p><span data-ttu-id="c62b5-131">Kerberos および NTLM</span><span class="sxs-lookup"><span data-stu-id="c62b5-131">Kerberos and NTLM</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c62b5-132">これらの認証の種類がサービスレベルで無効にされていない限り、展開で2要素認証が有効になると、Lync クライアントの他のすべてのバージョンが正常にサインインできなくなります。</span><span class="sxs-lookup"><span data-stu-id="c62b5-132">Unless these authentication types are disabled at the service level, all other versions of the Lync client will be unable to sign in successfully once two-factor authentication is enabled within in your deployment.</span></span>

</div>

<div>

## <a name="lync-service-discovery"></a><span data-ttu-id="c62b5-133">Lync サービスの検出</span><span class="sxs-lookup"><span data-stu-id="c62b5-133">Lync Service Discovery</span></span>

<span data-ttu-id="c62b5-134">内部および外部のクライアントによって使用される DNS レコードは、2要素認証が有効になっていない Lync サーバーに解決するように構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c62b5-134">DNS records used by internal and/or external clients to discover Lync services should be configured to resolve to a Lync server that is not enabled for two-factor authentication.</span></span> <span data-ttu-id="c62b5-135">この構成では、2要素認証が有効になっていない Lync プールのユーザーは、認証のために PIN を入力する必要がなく、2要素認証が有効になっている Lync プールのユーザーは、認証のために PIN を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c62b5-135">With this configuration, users from Lync Pools that are not enabled for two-factor authentication will not be required to enter a PIN to authenticate, while users from Lync Pools that are enabled for two-factor authentication will be required to enter their PIN to authenticate.</span></span>

</div>

<div>

## <a name="exchange-authentication"></a><span data-ttu-id="c62b5-136">Exchange 認証</span><span class="sxs-lookup"><span data-stu-id="c62b5-136">Exchange Authentication</span></span>

<span data-ttu-id="c62b5-137">Microsoft Exchange の2要素認証を展開しているお客様は、Lync クライアントの一部の機能が利用できない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c62b5-137">Customers who have deployed two-factor authentication for Microsoft Exchange may find that certain features in the Lync client are unavailable.</span></span> <span data-ttu-id="c62b5-138">現時点では、Lync クライアントは Exchange の統合に依存する機能に対して2要素認証をサポートしていないため、現在の設計になっています。</span><span class="sxs-lookup"><span data-stu-id="c62b5-138">This is currently by design, as the Lync client does not support two-factor authentication for features that are dependent on Exchange integration.</span></span>

</div>

<div>

## <a name="lync-contacts"></a><span data-ttu-id="c62b5-139">Lync の連絡先</span><span class="sxs-lookup"><span data-stu-id="c62b5-139">Lync Contacts</span></span>

<span data-ttu-id="c62b5-140">統合連絡先ストア機能を利用するように構成されている Lync ユーザーは、2要素認証を使用してサインインした後、連絡先が利用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="c62b5-140">Lync users who are configured to leverage the Unified Contact Store feature will find that their contacts are no longer available after signing in with two-factor authentication.</span></span>

<span data-ttu-id="c62b5-141">2要素認証を有効にする前に、 **CsUcsRollback** コマンドレットを使用して、統合された連絡先ストアから既存のユーザーの連絡先を削除し、それらを Lync Server 2013 に保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c62b5-141">You should use the **Invoke-CsUcsRollback** cmdlet to remove existing user contacts from the Unified Contact Store and store them in Lync Server 2013 before enabling two-factor authentication.</span></span>

</div>

<div>

## <a name="skill-search"></a><span data-ttu-id="c62b5-142">スキル検索</span><span class="sxs-lookup"><span data-stu-id="c62b5-142">Skill Search</span></span>

<span data-ttu-id="c62b5-143">Lync 環境でスキル検索機能を構成している場合は、Lync が2要素認証を有効にしている場合、この機能が機能しないことがわかります。</span><span class="sxs-lookup"><span data-stu-id="c62b5-143">Customers who have configured the Skill Search feature in their Lync environment will find that this feature does not work when Lync is enabled for two-factor authentication.</span></span> <span data-ttu-id="c62b5-144">現在、Microsoft SharePoint では 2 要素認証がサポートされていないため、これは仕様です。</span><span class="sxs-lookup"><span data-stu-id="c62b5-144">This is by design, as Microsoft SharePoint does not currently support two-factor authentication.</span></span>

</div>

<div>

## <a name="lync-credentials"></a><span data-ttu-id="c62b5-145">Lync の資格情報</span><span class="sxs-lookup"><span data-stu-id="c62b5-145">Lync Credentials</span></span>

<span data-ttu-id="c62b5-146">2要素認証を使用するように構成されているユーザーに影響を与える可能性のある Lync 資格情報が保存されていることについて、いくつかの展開の考慮事項があります。</span><span class="sxs-lookup"><span data-stu-id="c62b5-146">There are a number of deployment considerations involving saved Lync credentials which may impact users who are configured to use two-factor authentication.</span></span>

<div>

## <a name="deleting-saved-credentials"></a><span data-ttu-id="c62b5-147">保存された資格情報の削除</span><span class="sxs-lookup"><span data-stu-id="c62b5-147">Deleting Saved Credentials</span></span>

<span data-ttu-id="c62b5-148">デスクトップクライアントユーザーは、Lync クライアントで **[サインイン情報の削除** ] オプションを使用し、 \\ \\ \\ \\ 2 段階認証を使用して初めてサインインする前に、% localappdata% Microsoft Office 15.0 Lync から SIP プロファイルフォルダーを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c62b5-148">Desktop client users should use the **Delete my sign-in info** option in the Lync client and delete their SIP profile folder from %localappdata%\\Microsoft\\Office\\15.0\\Lync before attempting to sign for the first time using two-factor authentication.</span></span>

</div>

<div>

## <a name="disablentcredentials"></a><span data-ttu-id="c62b5-149">DisableNTCredentials</span><span class="sxs-lookup"><span data-stu-id="c62b5-149">DisableNTCredentials</span></span>

<span data-ttu-id="c62b5-150">認証方法が Kerberos または NTLM の場合は、ユーザーの Windows 資格情報が自動的に認証に使用されます。</span><span class="sxs-lookup"><span data-stu-id="c62b5-150">With the Kerberos or NTLM authentication method, the user’s Windows credentials are used automatically for authentication.</span></span> <span data-ttu-id="c62b5-151">認証に Kerberos または NTLM が有効になっている一般的な Lync Server 2013 の展開では、ユーザーがサインインするたびに資格情報を入力する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="c62b5-151">In a typical Lync Server 2013 deployment where Kerberos and/or NTLM is enabled for authentication, users should not have to enter their credentials every time that they sign in.</span></span>

<span data-ttu-id="c62b5-152">PIN の入力を求めるメッセージが表示される前に、意図せず資格情報の入力を求められた場合は、クライアント コンピューターで **DisableNTCredentials** レジストリ キーが誤って (おそらくグループ ポリシーを使用して) 構成されている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c62b5-152">If users are unintentionally prompted for credentials before they are prompted to enter their PIN, the **DisableNTCredentials** registry key may be unintentionally configured on client computers, possibly through Group Policy.</span></span>

<span data-ttu-id="c62b5-153">追加の資格情報の入力を求めるメッセージが表示されないようにするには、ローカルワークステーションで次のレジストリエントリを作成するか、グループポリシーを使って特定のプールのすべてのユーザーに適用する Lync 管理用テンプレートを使用します。</span><span class="sxs-lookup"><span data-stu-id="c62b5-153">To prevent the additional prompt for credentials, create the following registry entry on the local workstation or use the Lync administrative template to apply to all users for a given pool using Group Policy:</span></span>

<span data-ttu-id="c62b5-154">HKEY \_ ローカル \_ コンピューター \\ ソフトウェア \\ ポリシー \\ Microsoft \\ Office \\ 15.0 \\ Lync</span><span class="sxs-lookup"><span data-stu-id="c62b5-154">HKEY\_LOCAL\_MACHINE\\Software\\Policies\\Microsoft\\Office\\15.0\\Lync</span></span>

<span data-ttu-id="c62b5-155">REG \_ DWORD: DisableNTCredentials</span><span class="sxs-lookup"><span data-stu-id="c62b5-155">REG\_DWORD: DisableNTCredentials</span></span>

<span data-ttu-id="c62b5-156">値: 0x0</span><span class="sxs-lookup"><span data-stu-id="c62b5-156">Value: 0x0</span></span>

</div>

<div>

## <a name="savepassword"></a><span data-ttu-id="c62b5-157">SavePassword</span><span class="sxs-lookup"><span data-stu-id="c62b5-157">SavePassword</span></span>

<span data-ttu-id="c62b5-158">ユーザーが初めて Lync にサインインしたときに、ユーザーにパスワードの保存を促すメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c62b5-158">When a user signs in to Lync for the first time, the user is prompted to save his or her password.</span></span> <span data-ttu-id="c62b5-159">このオプションを選択すると、ユーザーのクライアント証明書を個人証明書ストアに保存したり、ユーザーの Windows 資格情報をローカル コンピューターの資格情報マネージャーに保存したりできます。</span><span class="sxs-lookup"><span data-stu-id="c62b5-159">If selected, this option allows the user’s client certificate to be stored in the personal certificate store and the user’s Windows credentials to be stored in the Credential Manager of the local computer.</span></span>

<span data-ttu-id="c62b5-160">Lync が2要素認証をサポートするように構成されている場合は、 **Savepassword** レジストリ設定を無効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c62b5-160">The **SavePassword** registry setting should be disabled when Lync is configured to support two-factor authentication.</span></span> <span data-ttu-id="c62b5-161">ユーザーがパスワードを保存できないようにするには、ローカルワークステーションの次のレジストリエントリを変更するか、グループポリシーを使って、特定のプールのすべてのユーザーに適用する Lync 管理用テンプレートを使用します。</span><span class="sxs-lookup"><span data-stu-id="c62b5-161">To prevent users from saving their passwords, change the following registry entry on the local workstation or use the Lync administrative template to apply to all users for a given pool using Group Policy:</span></span>

<span data-ttu-id="c62b5-162">HKEY \_ 現在の \_ ユーザー \\ ソフトウェア \\ Microsoft \\ Office \\ 15.0 \\ Lync</span><span class="sxs-lookup"><span data-stu-id="c62b5-162">HKEY\_CURRENT\_USER\\Software\\Microsoft\\Office\\15.0\\Lync</span></span>

<span data-ttu-id="c62b5-163">REG \_ DWORD: SavePassword</span><span class="sxs-lookup"><span data-stu-id="c62b5-163">REG\_DWORD: SavePassword</span></span>

<span data-ttu-id="c62b5-164">値: 0x0</span><span class="sxs-lookup"><span data-stu-id="c62b5-164">Value: 0x0</span></span>

</div>

</div>

<div>

## <a name="ad-fs-20-token-replay"></a><span data-ttu-id="c62b5-165">AD FS 2.0 のトークンのリプレイ</span><span class="sxs-lookup"><span data-stu-id="c62b5-165">AD FS 2.0 Token Replay</span></span>

<span data-ttu-id="c62b5-p108">AD FS 2.0 には、トークン リプレイ検出と呼ばれる機能が用意されています。この機能によって、同じトークンを使用する複数のトークン要求を検出して破棄できます。この機能が有効な場合は、同じトークンが複数回使用されることがなくなるため、WS-Federation パッシブ プロファイルと SAML WebSSO プロファイルの両方において認証要求の整合性が確保されます。</span><span class="sxs-lookup"><span data-stu-id="c62b5-p108">AD FS 2.0 provides a feature referred to as token replay detection, by which multiple token requests using the same token can be detected and then discarded. When this feature is enabled, token replay detection protects the integrity of authentication requests in both the WS-Federation passive profile and the SAML WebSSO profile by making sure that the same token is never used more than once.</span></span>

<span data-ttu-id="c62b5-168">キオスクを使用する場合など、セキュリティが最も重視される状況では、この機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c62b5-168">This feature should be enabled in situations where security is a very high concern such as when using kiosks.</span></span> <span data-ttu-id="c62b5-169">トークンの再生検出の詳細については、「AD FS 2.0 のセキュリティで保護された計画と展開のためのベストプラクティス」を参照してください [https://go.microsoft.com/fwlink/p/?LinkId=309215](https://go.microsoft.com/fwlink/p/?linkid=309215) 。</span><span class="sxs-lookup"><span data-stu-id="c62b5-169">For more information about token replay detection, see Best Practices for Secure Planning and Deployment of AD FS 2.0 at [https://go.microsoft.com/fwlink/p/?LinkId=309215](https://go.microsoft.com/fwlink/p/?linkid=309215).</span></span>

</div>

<div>

## <a name="external-user-access"></a><span data-ttu-id="c62b5-170">外部ユーザー アクセス</span><span class="sxs-lookup"><span data-stu-id="c62b5-170">External User Access</span></span>

<span data-ttu-id="c62b5-171">外部ネットワークからの Lync の2要素認証をサポートするように AD FS プロキシまたはリバースプロキシを構成する方法については、以下のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c62b5-171">Configuring an AD FS Proxy or Reverse Proxy to support Lync two-factor authentication from external networks is not covered in these topics.</span></span>

<span data-ttu-id="c62b5-172"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c62b5-172"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

