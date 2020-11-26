---
title: 'Lync Server 2013: Kerberos 認証の設定'
description: 'Lync Server 2013: Kerberos 認証を設定する。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up Kerberos authentication
ms:assetid: dd8009ef-6265-4cc0-b2c7-e474cd1f4b09
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398976(v=OCS.15)
ms:contentKeyID: 48185601
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bb461968bc073edbfe640f609257f3e84c192461
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441719"
---
# <a name="setting-up-kerberos-authentication-in-lync-server-2013"></a><span data-ttu-id="52be5-103">Lync Server 2013 での Kerberos 認証の設定</span><span class="sxs-lookup"><span data-stu-id="52be5-103">Setting up Kerberos authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="52be5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="52be5-104">

<span> </span></span></span>

<span data-ttu-id="52be5-105">_**最終更新日:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="52be5-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="52be5-106">Lync Server 2013 は、Web サービスの NTLM 認証と Kerberos 認証をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="52be5-106">Lync Server 2013 supports NTLM and Kerberos authentication for Web Services.</span></span> <span data-ttu-id="52be5-107">Office Communications Server 2007 および Office Communications Server 2007 R2 では、サービスプリンシパル名 (SPN) をユーザーアカウントに割り当てて、認証プリンシパルとして機能させることができるようにするために、既定の RTCComponentService と RTCService をユーザーアカウントとして使用しました。</span><span class="sxs-lookup"><span data-stu-id="52be5-107">Office Communications Server 2007 and Office Communications Server 2007 R2 used the default RTCComponentService and RTCService as the user accounts to run the Web Services application pools, allowing for a service principal name (SPN) to be assigned to the user accounts and to act as the authentication principal.</span></span> <span data-ttu-id="52be5-108">Lync Server は NetworkService を使って Web サービスを実行します。 NetworkService には、Spn を割り当てることはできません。</span><span class="sxs-lookup"><span data-stu-id="52be5-108">Lync Server uses NetworkService to run Web Services and NetworkService cannot have SPNs assigned to it.</span></span>

<span data-ttu-id="52be5-109">Active Directory オブジェクトに Spn を保持する必要がないという問題を解決するために、Lync Server コントロールパネルでは、この目的でコンピューターアカウントオブジェクトを使うことができます。</span><span class="sxs-lookup"><span data-stu-id="52be5-109">To solve the issue of not having Active Directory objects to hold the SPNs, Lync Server Control Panel can use computer account objects for this purpose.</span></span> <span data-ttu-id="52be5-110">コンピューターアカウントオブジェクトは、Spn を保持することができ、パスワードの有効期限は適用されません。これは、以前のバージョンでのユーザーアカウントの使用に関する問題です。</span><span class="sxs-lookup"><span data-stu-id="52be5-110">The computer account objects can hold the SPNs and are not subject to password expiration, which was an issue with using user accounts in previous versions.</span></span>

<span data-ttu-id="52be5-111">Kerberos 認証を提供するようにコンピューターオブジェクトを構成するには、Windows PowerShell コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="52be5-111">You use Windows PowerShell cmdlets to configure the computer objects to provide Kerberos authentication.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="52be5-112">このセクション中</span><span class="sxs-lookup"><span data-stu-id="52be5-112">In This Section</span></span>

  - [<span data-ttu-id="52be5-113">Lync Server 2013 で Kerberos 認証を有効にするための前提条件</span><span class="sxs-lookup"><span data-stu-id="52be5-113">Prerequisites for enabling Kerberos authentication in Lync Server 2013</span></span>](lync-server-2013-prerequisites-for-enabling-kerberos-authentication.md)

  - [<span data-ttu-id="52be5-114">Lync Server 2013 での Kerberos 認証アカウントの作成</span><span class="sxs-lookup"><span data-stu-id="52be5-114">Create a Kerberos authentication account in Lync Server 2013</span></span>](lync-server-2013-create-a-kerberos-authentication-account.md)

  - [<span data-ttu-id="52be5-115">Lync Server 2013 での、サイトへの Kerberos 認証アカウントの割り当て</span><span class="sxs-lookup"><span data-stu-id="52be5-115">Assign a Kerberos authentication account to a site in Lync Server 2013</span></span>](lync-server-2013-assign-a-kerberos-authentication-account-to-a-site.md)

  - [<span data-ttu-id="52be5-116">Lync Server 2013 での Kerberos 認証アカウント パスワードの設定</span><span class="sxs-lookup"><span data-stu-id="52be5-116">Setting up Kerberos authentication account passwords in Lync Server 2013</span></span>](lync-server-2013-setting-up-kerberos-authentication-account-passwords.md)

  - [<span data-ttu-id="52be5-117">Lync Server 2013 での他のサイトへの Kerberos 認証の追加</span><span class="sxs-lookup"><span data-stu-id="52be5-117">In Lync Server 2013 add Kerberos authentication to other sites</span></span>](lync-server-2013-add-kerberos-authentication-to-other-sites.md)

  - [<span data-ttu-id="52be5-118">Lync Server 2013 でのサイトからの Kerberos 認証の削除</span><span class="sxs-lookup"><span data-stu-id="52be5-118">In Lync Server 2013 remove Kerberos authentication from a site</span></span>](lync-server-2013-remove-kerberos-authentication-from-a-site.md)

  - [<span data-ttu-id="52be5-119">Lync Server 2013 での Kerberos 認証の状態と割り当てについてのテストおよびレポート</span><span class="sxs-lookup"><span data-stu-id="52be5-119">Testing and reporting the status and assignment of Kerberos authentication in Lync Server 2013</span></span>](lync-server-2013-testing-and-reporting-the-status-and-assignment-of-kerberos-authentication.md)

<span data-ttu-id="52be5-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="52be5-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

