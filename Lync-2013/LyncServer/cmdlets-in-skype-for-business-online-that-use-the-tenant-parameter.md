---
title: テナントパラメーターを使う Skype for Business Online のコマンドレット
description: テナントパラメーターを使う Skype for Business Online のコマンドレット。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Cmdlets that use the Tenant parameter
ms:assetid: e7fe7c12-fbe0-49c1-9e8c-eef6958f27d0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362850(v=OCS.15)
ms:contentKeyID: 56558865
ms.date: 05/04/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ff2b8053dd855a854fa26699770d3dafaa0dcbd7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398414"
---
# <a name="cmdlets-in-skype-for-business-online-that-use-the-tenant-parameter"></a><span data-ttu-id="999c5-103">テナントパラメーターを使う Skype for Business Online のコマンドレット</span><span class="sxs-lookup"><span data-stu-id="999c5-103">Cmdlets in Skype for Business Online that use the Tenant parameter</span></span>

 


<span data-ttu-id="999c5-104">パブリックプロバイダーの設定を変更する場合は、常にテナント id を指定する必要があります。これは、1つのテナントのみがある場合にも当てはまります。</span><span class="sxs-lookup"><span data-stu-id="999c5-104">When modifying your public provider settings, you always need to supply a Tenant identity; this is true even if you only have a single tenant.</span></span> <span data-ttu-id="999c5-105">たとえば、次のコマンドは、Windows Live を、ユーザーが通信できる唯一のパブリックプロバイダーとして設定します。</span><span class="sxs-lookup"><span data-stu-id="999c5-105">For example, this command sets Windows Live as the only public provider your users are allowed to communicate with:</span></span>

    Set-CsTenantPublicProvider -Tenant "bf19b7db-6960-41e5-a139-2aa373474354" -Provider "WindowsLive"

<span data-ttu-id="999c5-106">ただし、これらのコマンドレットのいずれかを実行するたびに、テナント ID (bf19b7db-6960-41e5-a139-2aa373474354 など) を入力する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="999c5-106">Fortunately, you do not need to type the Tenant ID (for example, bf19b7db-6960-41e5-a139-2aa373474354) each time you run one of these cmdlets.</span></span> <span data-ttu-id="999c5-107">代わりに、 [CsTenant](https://technet.microsoft.com/library/jj994044\(v=ocs.15\)) コマンドレットを実行し、テナント id を変数に保存してから、他のコマンドレットのいずれかを呼び出すときにその変数を使用して、テナント id を取得できます。</span><span class="sxs-lookup"><span data-stu-id="999c5-107">Instead, you can retrieve the Tenant ID by running the [Get-CsTenant](https://technet.microsoft.com/library/jj994044\(v=ocs.15\)) cmdlet, storing the Tenant ID in a variable, and then using that variable when you call one of the other cmdlets.</span></span> <span data-ttu-id="999c5-108">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="999c5-108">For example:</span></span>

    $x = (Get-CsTenant).TenantId
    Set-CsTenantPublicProvider -Tenant $x -Provider "WindowsLive"

<span data-ttu-id="999c5-109">または、1つのコマンドでテナント ID を取得し、その値を Set-CsTenantPublicProvider コマンドレットにパイプすることで、これを行うこともできます。</span><span class="sxs-lookup"><span data-stu-id="999c5-109">Alternatively, you can do this in a single command by retrieving the Tenant ID and then piping that value to the Set-CsTenantPublicProvider cmdlet:</span></span>

    Get-CsTenant | Select-Object TenantId | ForEach-Object {Set-CsTenantPublicProvider -Tenant $_.TenantId -Provider "WindowsLive"}

<span data-ttu-id="999c5-110">**Get-CsTenant** コマンドレットを呼び出すときに、テナント ID を指定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="999c5-110">You do not need to specify the tenant ID when calling the **Get-CsTenant** cmdlet.</span></span> <span data-ttu-id="999c5-111">このコマンドは、テナントに関する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="999c5-111">This command returns information about your tenant:</span></span>

    Get-CsTenant

<span data-ttu-id="999c5-112">次のコマンドレットは、テナント id を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="999c5-112">The following cmdlets accept a tenant identity.</span></span> <span data-ttu-id="999c5-113">ただし、この場合、パラメーターは省略可能であり、コマンドレットを呼び出すときに入力する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="999c5-113">However, in these cases, the parameter is optional and does not need to be entered when calling the cmdlet.</span></span> <span data-ttu-id="999c5-114">代わりに、Windows PowerShell は、現在接続している Skype for Business Online テナントに基づいて、適切にテナント id を入力します。</span><span class="sxs-lookup"><span data-stu-id="999c5-114">Instead, Windows PowerShell will effectively enter the tenant identity for you based on the Skype for Business Online tenant you are currently connected to:</span></span>

  - <span data-ttu-id="999c5-115">[Get-CsTenant](https://technet.microsoft.com/library/jj994044\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="999c5-115">[Get-CsTenant](https://technet.microsoft.com/library/jj994044\(v=ocs.15\))</span></span>

  - <span data-ttu-id="999c5-116">[Set-CsTenantFederationConfiguration](https://technet.microsoft.com/library/jj994080\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="999c5-116">[Set-CsTenantFederationConfiguration](https://technet.microsoft.com/library/jj994080\(v=ocs.15\))</span></span>

  - <span data-ttu-id="999c5-117">[Set-CsTenantHybridConfiguration](https://technet.microsoft.com/library/jj994046\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="999c5-117">[Set-CsTenantHybridConfiguration](https://technet.microsoft.com/library/jj994046\(v=ocs.15\))</span></span>

  - <span data-ttu-id="999c5-118">[Get-CsTenantFederationConfiguration](https://technet.microsoft.com/library/jj994072\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="999c5-118">[Get-CsTenantFederationConfiguration](https://technet.microsoft.com/library/jj994072\(v=ocs.15\))</span></span>

  - <span data-ttu-id="999c5-119">[Get-CsTenantHybridConfiguration](https://technet.microsoft.com/library/jj994034\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="999c5-119">[Get-CsTenantHybridConfiguration](https://technet.microsoft.com/library/jj994034\(v=ocs.15\))</span></span>

  - <span data-ttu-id="999c5-120">[Get-CsTenantLicensingConfiguration](https://technet.microsoft.com/library/dn362770\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="999c5-120">[Get-CsTenantLicensingConfiguration](https://technet.microsoft.com/library/dn362770\(v=ocs.15\))</span></span>

<span data-ttu-id="999c5-121">たとえば、 **CsTenantFederationConfiguration** コマンドレットは、次のコマンドを使って呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="999c5-121">For example, the **Get-CsTenantFederationConfiguration** cmdlet can be called by using this command:</span></span>

    Get-CsTenantFederationConfiguration

<span data-ttu-id="999c5-122">必須ではありませんが、Get-CsTenantFederationConfiguration を呼び出すときにテナントパラメーターを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="999c5-122">Although not required, you can include the Tenant parameter when calling Get-CsTenantFederationConfiguration :</span></span>

    Get-CsTenantFederationConfiguration -Tenant "bf19b7db-6960-41e5-a139-2aa373474354"

## <a name="see-also"></a><span data-ttu-id="999c5-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="999c5-123">See Also</span></span>


[<span data-ttu-id="999c5-124">Skype for Business Online の id、スコープ、テナント</span><span class="sxs-lookup"><span data-stu-id="999c5-124">Identities, scopes, and tenants in Skype for Business Online</span></span>](identities-scopes-and-tenants-in-skype-for-business-online.md)  
<span data-ttu-id="999c5-125">[Lync Online のコマンドレット](https://technet.microsoft.com/library/dn362817\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="999c5-125">[The Skype for Business Online cmdlets](https://technet.microsoft.com/library/dn362817\(v=ocs.15\))</span></span>

