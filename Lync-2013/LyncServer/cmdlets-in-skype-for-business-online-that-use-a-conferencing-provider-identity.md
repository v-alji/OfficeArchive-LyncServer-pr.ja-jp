---
title: 会議プロバイダー id を使用する Skype for Business Online のコマンドレット
description: 会議プロバイダー id を使用する Skype for Business Online のコマンドレット。
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Cmdlets that use a conferencing provider identity
ms:assetid: be5621b6-ec11-4b12-83ec-075af269ca6a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362841(v=OCS.15)
ms:contentKeyID: 56558858
ms.date: 05/04/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 61ab4fb410878ca73314b73737948d9961462c87
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398571"
---
# <a name="cmdlets-in-skype-for-business-online-that-use-a-conferencing-provider-identity"></a><span data-ttu-id="7ed07-103">会議プロバイダー id を使用する Skype for Business Online のコマンドレット</span><span class="sxs-lookup"><span data-stu-id="7ed07-103">Cmdlets in Skype for Business Online that use a conferencing provider identity</span></span>

 


<span data-ttu-id="7ed07-104">組織が契約しているすべての電話会議プロバイダーに関する情報を取得するには、パラメーターを指定せずに [CsAudioConferencingProvider](https://technet.microsoft.com/library/jj994030\(v=ocs.15\)) コマンドレットを呼び出すだけです。</span><span class="sxs-lookup"><span data-stu-id="7ed07-104">To return information about all of the audio conferencing providers that your organization has contracted with, you can simply call the [Get-CsAudioConferencingProvider](https://technet.microsoft.com/library/jj994030\(v=ocs.15\)) cmdlet without any parameters:</span></span>

    Get-CsAudioConferencingProvider

<span data-ttu-id="7ed07-105">返されるデータを1つのプロバイダーに制限する場合は (この例では、プロバイダーの Contoso Audio サービス)、Identity パラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="7ed07-105">If you want to limit the returned data to a single provider (in this example, the provider Contoso Audio Services), then use the Identity parameter:</span></span>

    Get-CsAudioConferencingProvider -Identity "Contoso Audio Services"

<span data-ttu-id="7ed07-106">電話会議プロバイダー ID を受け入れる Skype for Business Online コマンドレットは1つしかありません。</span><span class="sxs-lookup"><span data-stu-id="7ed07-106">There is only one Skype for Business Online cmdlet that accepts an audio conferencing provider ID:</span></span>

  - <span data-ttu-id="7ed07-107">[Get-CsAudioConferencingProvider](https://technet.microsoft.com/library/jj994030\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="7ed07-107">[Get-CsAudioConferencingProvider](https://technet.microsoft.com/library/jj994030\(v=ocs.15\))</span></span>

## <a name="see-also"></a><span data-ttu-id="7ed07-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="7ed07-108">See Also</span></span>


[<span data-ttu-id="7ed07-109">Skype for Business Online の id、スコープ、テナント</span><span class="sxs-lookup"><span data-stu-id="7ed07-109">Identities, scopes, and tenants in Skype for Business Online</span></span>](identities-scopes-and-tenants-in-skype-for-business-online.md)  
<span data-ttu-id="7ed07-110">[Lync Online のコマンドレット](https://technet.microsoft.com/library/dn362817\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="7ed07-110">[The Skype for Business Online cmdlets](https://technet.microsoft.com/library/dn362817\(v=ocs.15\))</span></span>

