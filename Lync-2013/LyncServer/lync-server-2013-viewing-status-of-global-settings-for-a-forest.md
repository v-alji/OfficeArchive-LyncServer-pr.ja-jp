---
title: 'Lync Server 2013: フォレストのグローバル設定の状態を表示する'
description: 'Lync Server 2013: フォレストのグローバル設定の状態を表示します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View status of global settings for a forest
ms:assetid: 2ab0f2f1-9908-4e6f-aff3-d6b3cc474b6b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn747889(v=OCS.15)
ms:contentKeyID: 63969590
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d9f722ea66f6c54c816703bd1af1d3def57bbd84
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443910"
---
# <a name="view-status-of-global-settings-for-a-forest-in-lync-server-2013"></a><span data-ttu-id="99c25-103">Lync Server 2013 でフォレストのグローバル設定の状態を表示する</span><span class="sxs-lookup"><span data-stu-id="99c25-103">View status of global settings for a forest in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="99c25-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="99c25-104">

<span> </span></span></span>

<span data-ttu-id="99c25-105">_**最終更新日:** 2014-05-20_</span><span class="sxs-lookup"><span data-stu-id="99c25-105">_**Topic Last Modified:** 2014-05-20_</span></span>

<span data-ttu-id="99c25-106">管理者は、Lync Server 2013 展開のグローバル設定を毎月確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="99c25-106">Administrators should review the global settings for a Lync Server 2013 deployment monthly.</span></span> <span data-ttu-id="99c25-107">目標として、実装されている設定を既知の構成のセットと照らし合わせて確認します。設定は有効であることを保証し、ベースラインのドキュメントを更新する必要があるかどうかを判断するための基準構成となります。</span><span class="sxs-lookup"><span data-stu-id="99c25-107">The objective would be to review implemented settings against a set of known configurations—a baseline configuration to help guarantee that settings are valid and to determine whether the baseline documentation should be updated.</span></span> <span data-ttu-id="99c25-108">グローバル設定の変更は、新しい設定の文書化を含める必要がある変更管理プロセスによって実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="99c25-108">Changes to global setting should be implemented through a Change Control process which should include documenting the new settings.</span></span>

<span data-ttu-id="99c25-109">レビューする必要があるグローバル設定については、次のセクションで説明します。</span><span class="sxs-lookup"><span data-stu-id="99c25-109">Global settings that should be reviewed are described in the following sections:</span></span>

<div>

## <a name="check-general-settings"></a><span data-ttu-id="99c25-110">全般設定を確認する</span><span class="sxs-lookup"><span data-stu-id="99c25-110">Check general settings</span></span>

<span data-ttu-id="99c25-111">Lync Server 2013 でサポートされているセッション開始プロトコル (SIP) ドメインなど、一般的な設定を確認します。</span><span class="sxs-lookup"><span data-stu-id="99c25-111">Check general settings, including the supported Session Initiation Protocol (SIP) domains for Lync Server 2013.</span></span>

<span data-ttu-id="99c25-112">SIP ドメイン情報は、Windows PowerShell と **CsSipDomain** コマンドレットを使って返すことができます。</span><span class="sxs-lookup"><span data-stu-id="99c25-112">SIP domain information can be returned by using Windows PowerShell and the **Get-CsSipDomain** cmdlet.</span></span> <span data-ttu-id="99c25-113">この情報を返すには、 `Get-CsSipDomain` Windows PowerShell コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="99c25-113">To return this information, run the `Get-CsSipDomain` Windows PowerShell command.</span></span>

<span data-ttu-id="99c25-114">Get-CsSipDomain は、認証されたすべての SIP ドメインについて、次のような情報を返します。</span><span class="sxs-lookup"><span data-stu-id="99c25-114">Get-CsSipDomain will return information similar to this for all the authorized SIP domains:</span></span>

<span data-ttu-id="99c25-115">識別名の IsDefault</span><span class="sxs-lookup"><span data-stu-id="99c25-115">Identity Name IsDefault</span></span>

<span data-ttu-id="99c25-116">\-------- ---- ---------</span><span class="sxs-lookup"><span data-stu-id="99c25-116">\-------- ---- ---------</span></span>

<span data-ttu-id="99c25-117">fabrikam.com fabrikam.com True</span><span class="sxs-lookup"><span data-stu-id="99c25-117">fabrikam.com fabrikam.com True</span></span>

<span data-ttu-id="99c25-118">na.fabrikam.com na.fabrikam.com False</span><span class="sxs-lookup"><span data-stu-id="99c25-118">na.fabrikam.com na.fabrikam.com False</span></span>

<span data-ttu-id="99c25-119">IsDefault プロパティが True に設定されている場合、対応するドメインは既定の SIP ドメインになります。</span><span class="sxs-lookup"><span data-stu-id="99c25-119">If the IsDefault property is set to True, the corresponding domain is your default SIP domain.</span></span> <span data-ttu-id="99c25-120">Set-CsSipDomain コマンドレットを使用して、組織の既定の SIP ドメインを変更できます。</span><span class="sxs-lookup"><span data-stu-id="99c25-120">You can use the Set-CsSipDomain cmdlet to change the default SIP domain for your organization.</span></span> <span data-ttu-id="99c25-121">ただし、既定のドメインがないままであるため、既定の SIP ドメインを削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="99c25-121">However, you can't just delete the default SIP domain because that would leave you without a default domain.</span></span> <span data-ttu-id="99c25-122">(前の例で示したように) fabrikam.com ドメインを削除する場合は、最初に既定のドメインとなるように na.fabrikam.com を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="99c25-122">If you wanted to delete the fabrikam.com domain (as shown in the previous example), you would first have to configure na.fabrikam.com to be your default domain.</span></span>

</div>

<div>

## <a name="check-meeting-settings"></a><span data-ttu-id="99c25-123">会議の設定を確認する</span><span class="sxs-lookup"><span data-stu-id="99c25-123">Check meeting settings</span></span>

<span data-ttu-id="99c25-124">会議の設定には、会議のポリシー定義と、会議での匿名ユーザーの参加のサポートが含まれます。</span><span class="sxs-lookup"><span data-stu-id="99c25-124">Meeting settings include meeting policy definitions and support for participation of anonymous users in meetings.</span></span>

<span data-ttu-id="99c25-125">会議の構成設定を取得するには、Windows PowerShell を使用するか、または **csmeeting 構成** コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="99c25-125">Meeting configuration settings can be retrieved by using Windows PowerShell and the **Get-CsMeetingConfiguration** cmdlet.</span></span> <span data-ttu-id="99c25-126">たとえば、次のコマンドは、グローバル会議の構成設定に関する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="99c25-126">For example, this command returns information about the global meeting configuration settings:</span></span>

<span data-ttu-id="99c25-127">Get-CsMeetingConfiguration – Id が "グローバル" の会議構成設定は、サイトのスコープで構成することもできます。</span><span class="sxs-lookup"><span data-stu-id="99c25-127">Get-CsMeetingConfiguration –Identity "Global"Meeting configuration settings can also be configured at the site scope.</span></span> <span data-ttu-id="99c25-128">そのため、次のコマンドを使用することができます。これは、すべての会議の構成設定に関する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="99c25-128">Because of that, you might want to use the following command, which returns information about all the meeting configuration settings:</span></span>

`Get-CsMeetingConfiguration`

<span data-ttu-id="99c25-129">**Cs会議構成** コマンドレットは、次のような情報を返します。</span><span class="sxs-lookup"><span data-stu-id="99c25-129">The **Get-CsMeetingConfiguration** cmdlet returns information similar to the following:</span></span>

<span data-ttu-id="99c25-130">Identity: グローバル</span><span class="sxs-lookup"><span data-stu-id="99c25-130">Identity : Global</span></span>

<span data-ttu-id="99c25-131">PstnCallersBypassLobby: True</span><span class="sxs-lookup"><span data-stu-id="99c25-131">PstnCallersBypassLobby : True</span></span>

<span data-ttu-id="99c25-132">EnableAssignedConferenceType: True</span><span class="sxs-lookup"><span data-stu-id="99c25-132">EnableAssignedConferenceType : True</span></span>

<span data-ttu-id="99c25-133">デザインの発表者: 会社</span><span class="sxs-lookup"><span data-stu-id="99c25-133">DesignateAsPresenter : Company</span></span>

<span data-ttu-id="99c25-134">AssignedConferenceTypeByDefault: True</span><span class="sxs-lookup"><span data-stu-id="99c25-134">AssignedConferenceTypeByDefault : True</span></span>

<span data-ttu-id="99c25-135">AdmitAnonymousUsersByDefault: True</span><span class="sxs-lookup"><span data-stu-id="99c25-135">AdmitAnonymousUsersByDefault : True</span></span>

<span data-ttu-id="99c25-136">**AdmitAnonymousUsersByDefault** の最後の項目では、匿名ユーザーが会議に参加する機能を有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="99c25-136">Again, the final item in the list, **AdmitAnonymousUsersByDefault**, enables or disables the ability of anonymous users to participate in meetings.</span></span>

<span data-ttu-id="99c25-137">会議の構成設定を確認するときに、現在の設定を既定の対応する値と比較すると便利な場合があります。</span><span class="sxs-lookup"><span data-stu-id="99c25-137">When checking meeting configuration settings, you might find it useful to compare the current settings against the default equivalents.</span></span> <span data-ttu-id="99c25-138">次のコマンドを実行して、既定の会議構成設定を表示できます。</span><span class="sxs-lookup"><span data-stu-id="99c25-138">You can view the default meeting configuration settings by running the following command:</span></span>

`New-CsMeetingConfiguration -Identity "Global" -InMemory`

<span data-ttu-id="99c25-139">前のコマンドでは、グローバル会議構成設定のメモリ内のインスタンス (各プロパティの既定値を使用するインスタンス) が作成されます。</span><span class="sxs-lookup"><span data-stu-id="99c25-139">The previous command creates an in-memory-only instance of the global meeting configuration settings, an instance that uses the default value for each property.</span></span> <span data-ttu-id="99c25-140">このコマンドを実行しても、実際の会議の構成設定は作成されません。</span><span class="sxs-lookup"><span data-stu-id="99c25-140">No actual meeting configuration settings are created when you run the command.</span></span> <span data-ttu-id="99c25-141">ただし、すべての既定のプロパティ値が画面に表示されます。</span><span class="sxs-lookup"><span data-stu-id="99c25-141">However, all the default property values will be displayed on-screen.</span></span>

</div>

<div>

## <a name="check-edge-servers-and-their-settings"></a><span data-ttu-id="99c25-142">エッジサーバーとその設定を確認する</span><span class="sxs-lookup"><span data-stu-id="99c25-142">Check Edge Servers and their settings</span></span>

<span data-ttu-id="99c25-143">エッジサーバーの情報は、Windows PowerShell を使用して取得できます。</span><span class="sxs-lookup"><span data-stu-id="99c25-143">Edge Server information can be retrieved by using Windows PowerShell.</span></span> <span data-ttu-id="99c25-144">このコマンドは、組織で使用するように構成されているすべてのエッジサーバーについての情報を返します。</span><span class="sxs-lookup"><span data-stu-id="99c25-144">This command returns information about all the Edge Servers configured for use in your organization:</span></span>

`Get-CsService -EdgeServer`

<span data-ttu-id="99c25-145">返される情報には、各エッジサーバーの FQDN とポートの設定がすべて含まれています。</span><span class="sxs-lookup"><span data-stu-id="99c25-145">The returned information includes all of the FQDN and port settings for each Edge Server:</span></span>

<span data-ttu-id="99c25-146">Id: EdgeServer: dc.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="99c25-146">Identity : EdgeServer: dc.fabrikam.com</span></span>

<span data-ttu-id="99c25-147">レジストラー: レジストラー: LYNC-SE.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="99c25-147">Registrar : Registrar: LYNC-SE.fabrikam.com</span></span>

<span data-ttu-id="99c25-148">AccessEdgeInternalSipPort: 5061</span><span class="sxs-lookup"><span data-stu-id="99c25-148">AccessEdgeInternalSipPort : 5061</span></span>

<span data-ttu-id="99c25-149">AccessEdgeExternalSipPort: 5061</span><span class="sxs-lookup"><span data-stu-id="99c25-149">AccessEdgeExternalSipPort : 5061</span></span>

<span data-ttu-id="99c25-150">AccessEdgeClientPort: 443</span><span class="sxs-lookup"><span data-stu-id="99c25-150">AccessEdgeClientPort : 443</span></span>

<span data-ttu-id="99c25-151">DataPsomServerPort: 8057</span><span class="sxs-lookup"><span data-stu-id="99c25-151">DataPsomServerPort : 8057</span></span>

<span data-ttu-id="99c25-152">DataPsomClientPort: 444</span><span class="sxs-lookup"><span data-stu-id="99c25-152">DataPsomClientPort : 444</span></span>

<span data-ttu-id="99c25-153">MediaRelayAuthEdgePort: 5062</span><span class="sxs-lookup"><span data-stu-id="99c25-153">MediaRelayAuthEdgePort : 5062</span></span>

<span data-ttu-id="99c25-154">MediaRelayAuthInternalTurnTcpPort: 443</span><span class="sxs-lookup"><span data-stu-id="99c25-154">MediaRelayAuthInternalTurnTcpPort : 443</span></span>

<span data-ttu-id="99c25-155">MediaRelayAuthExternalTurnTcpPort: 445</span><span class="sxs-lookup"><span data-stu-id="99c25-155">MediaRelayAuthExternalTurnTcpPort : 445</span></span>

<span data-ttu-id="99c25-156">MediaRelayAuthInternalTurnUdpPort: 3478</span><span class="sxs-lookup"><span data-stu-id="99c25-156">MediaRelayAuthInternalTurnUdpPort : 3478</span></span>

<span data-ttu-id="99c25-157">MediaRelayAuthExternalTurnUdpPort: 3478</span><span class="sxs-lookup"><span data-stu-id="99c25-157">MediaRelayAuthExternalTurnUdpPort : 3478</span></span>

<span data-ttu-id="99c25-158">MediaCommunicationPortStart: 5万</span><span class="sxs-lookup"><span data-stu-id="99c25-158">MediaCommunicationPortStart : 50000</span></span>

<span data-ttu-id="99c25-159">MediaComunicationPortCount: 1万</span><span class="sxs-lookup"><span data-stu-id="99c25-159">MediaComunicationPortCount : 10000</span></span>

<span data-ttu-id="99c25-160">AccessEdgeExternalFqdn: dc.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="99c25-160">AccessEdgeExternalFqdn : dc.fabrikam.com</span></span>

<span data-ttu-id="99c25-161">DataEdgeExternalFqdn: dc.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="99c25-161">DataEdgeExternalFqdn : dc.fabrikam.com</span></span>

<span data-ttu-id="99c25-162">AVEdgeExternalFqdn :</span><span class="sxs-lookup"><span data-stu-id="99c25-162">AVEdgeExternalFqdn :</span></span>

<span data-ttu-id="99c25-163">InternalInterfaceFqdn :</span><span class="sxs-lookup"><span data-stu-id="99c25-163">InternalInterfaceFqdn :</span></span>

<span data-ttu-id="99c25-164">ExternalMrasFqdn: dc.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="99c25-164">ExternalMrasFqdn : dc.fabrikam.com</span></span>

<span data-ttu-id="99c25-165">DependentServiceList: {レジストラー: LYNC-SE.fabrikam.com,</span><span class="sxs-lookup"><span data-stu-id="99c25-165">DependentServiceList : {Registrar:LYNC-SE.fabrikam.com,</span></span>

<span data-ttu-id="99c25-166">ConferencingServer: LYNC-SE</span><span class="sxs-lookup"><span data-stu-id="99c25-166">ConferencingServer:LYNC-SE.fabrikam</span></span>

<span data-ttu-id="99c25-167">com、MediationServer: LYNC-SE。</span><span class="sxs-lookup"><span data-stu-id="99c25-167">com, MediationServer:LYNC-SE.</span></span>

<span data-ttu-id="99c25-168">fabrikam.com}</span><span class="sxs-lookup"><span data-stu-id="99c25-168">fabrikam.com}</span></span>

<span data-ttu-id="99c25-169">ServiceId: fabrikam.com-EdgeServer</span><span class="sxs-lookup"><span data-stu-id="99c25-169">ServiceId : fabrikam.com-EdgeServer-2</span></span>

<span data-ttu-id="99c25-170">SiteId: サイト: fabrikam</span><span class="sxs-lookup"><span data-stu-id="99c25-170">SiteId : site:fabrikam.com</span></span>

<span data-ttu-id="99c25-171">PoolFqdn: dc.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="99c25-171">PoolFqdn : dc.fabrikam.com</span></span>

<span data-ttu-id="99c25-172">バージョン: 5</span><span class="sxs-lookup"><span data-stu-id="99c25-172">Version : 5</span></span>

<span data-ttu-id="99c25-173">役割: EdgeServer</span><span class="sxs-lookup"><span data-stu-id="99c25-173">Role : EdgeServer</span></span>

<div>

## <a name="check-federation-settings"></a><span data-ttu-id="99c25-174">フェデレーション設定を確認する</span><span class="sxs-lookup"><span data-stu-id="99c25-174">Check federation settings</span></span>

<span data-ttu-id="99c25-175">構成されているかどうかなど、フェデレーション設定を確認します。回答が "yes" の場合は、FQDN とポートを確認します。</span><span class="sxs-lookup"><span data-stu-id="99c25-175">Check Federation settings, such as whether it is configured and, if the answer is "yes,", the FQDN and port.</span></span> <span data-ttu-id="99c25-176">フェデレーションは、アクセスエッジ構成のグローバルコレクションを使って有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="99c25-176">Federation is enabled and disabled by using the global collection of Access Edge configuration settings.</span></span> <span data-ttu-id="99c25-177">特に、フェデレーションがすべてまたはまったく機能していないことを意味します。組織全体でフェデレーションが有効になっているか、組織全体でフェデレーションが無効になっていることを意味します。</span><span class="sxs-lookup"><span data-stu-id="99c25-177">Among other things, these mean that federation is configured on an all-or-nothing basis: either federation is enabled for the whole organization or federation is disabled for the whole organization</span></span>

<span data-ttu-id="99c25-178">アクセスエッジの構成設定は、Windows PowerShell を使用して返すことができます。</span><span class="sxs-lookup"><span data-stu-id="99c25-178">Your Access Edge configuration settings can be returned by using Windows PowerShell.</span></span> <span data-ttu-id="99c25-179">そのためには、次の Windows PowerShell コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="99c25-179">To do that, run the following Windows PowerShell command:</span></span>

`Get-CsAccessEdgeConfiguration`

<span data-ttu-id="99c25-180">このコマンドを実行すると、次のようなデータが返されます。</span><span class="sxs-lookup"><span data-stu-id="99c25-180">In turn, that command will return data similar to this:</span></span>

<span data-ttu-id="99c25-181">Identity: グローバル</span><span class="sxs-lookup"><span data-stu-id="99c25-181">Identity : Global</span></span>

<span data-ttu-id="99c25-182">AllowAnonymousUsers: False</span><span class="sxs-lookup"><span data-stu-id="99c25-182">AllowAnonymousUsers : False</span></span>

<span data-ttu-id="99c25-183">AllowFederatedUsers: False</span><span class="sxs-lookup"><span data-stu-id="99c25-183">AllowFederatedUsers : False</span></span>

<span data-ttu-id="99c25-184">AllowOutsideUsers: False</span><span class="sxs-lookup"><span data-stu-id="99c25-184">AllowOutsideUsers : False</span></span>

<span data-ttu-id="99c25-185">BeClearingHouse: False</span><span class="sxs-lookup"><span data-stu-id="99c25-185">BeClearingHouse : False</span></span>

<span data-ttu-id="99c25-186">EnablePartnerDiscovery: False</span><span class="sxs-lookup"><span data-stu-id="99c25-186">EnablePartnerDiscovery : False</span></span>

<span data-ttu-id="99c25-187">EnableArchivingDisclaimer: False</span><span class="sxs-lookup"><span data-stu-id="99c25-187">EnableArchivingDisclaimer : False</span></span>

<span data-ttu-id="99c25-188">KeepCrlsUpToDateForPeers: True</span><span class="sxs-lookup"><span data-stu-id="99c25-188">KeepCrlsUpToDateForPeers : True</span></span>

<span data-ttu-id="99c25-189">MarkSourceVerifiableOnOutgoingMessages: True</span><span class="sxs-lookup"><span data-stu-id="99c25-189">MarkSourceVerifiableOnOutgoingMessages : True</span></span>

<span data-ttu-id="99c25-190">OutgoingTlsCountForFederatedPartners: 4</span><span class="sxs-lookup"><span data-stu-id="99c25-190">OutgoingTlsCountForFederatedPartners : 4</span></span>

<span data-ttu-id="99c25-191">RoutingMethod: UseDnsSrvRouting</span><span class="sxs-lookup"><span data-stu-id="99c25-191">RoutingMethod : UseDnsSrvRouting</span></span>

<span data-ttu-id="99c25-192">**AllowFederatedUsers** プロパティが True に設定されている場合は、組織でフェデレーションが有効になっていることを意味します。</span><span class="sxs-lookup"><span data-stu-id="99c25-192">If the **AllowFederatedUsers** property is set to True, that means that federation is enabled for your organization.</span></span> <span data-ttu-id="99c25-193">( **AllowFederatedUsers** を True に設定すると、分割されたドメインのシナリオでは、オンプレミスのユーザーはクラウド内のユーザーとシームレスに通信できることを意味します)。</span><span class="sxs-lookup"><span data-stu-id="99c25-193">(Setting **AllowFederatedUsers** to True also means that, in a split domain scenario, your on-premises users will be able to communicate seamlessly with your in-the-cloud users.)</span></span>

<span data-ttu-id="99c25-194">エッジサーバーの FQDN とポートの設定を取得するには、前のタスク (エッジサーバーとその設定) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="99c25-194">To retrieve the FQDN and port settings for your Edge Server, see the previous task (Edge Servers and their settings).</span></span>

<span data-ttu-id="99c25-195">グローバルスコープでフェデレーションを有効にすると、ユーザーはフェデレーションされたユーザーと通信できる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="99c25-195">Enabling federation at the global scope only means that users can potentially communicate with federated users.</span></span> <span data-ttu-id="99c25-196">個々のユーザーが実際にフェデレーションユーザーと通信できるかどうかを判断するには、そのユーザーに割り当てられている外部ユーザーアクセスポリシーを調べる必要があります。</span><span class="sxs-lookup"><span data-stu-id="99c25-196">To determine whether any individual users can actually communicate with federated users requires you to examine the external user access policy assigned to that user.</span></span>

<span data-ttu-id="99c25-197">外部ユーザーアクセスの情報は、Windows PowerShell を使用して返すことができます。</span><span class="sxs-lookup"><span data-stu-id="99c25-197">External user access information can be returned by using Windows PowerShell.</span></span> <span data-ttu-id="99c25-198">たとえば、次のコマンドは、グローバル外部ユーザーアクセスポリシーに関する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="99c25-198">For example, this command returns information for the global external user access policy:</span></span>

`Get-CsExternalAccessPolicy -Identity "Global"`

<span data-ttu-id="99c25-199">このコマンドは、すべての外部ユーザーアクセスポリシーに関する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="99c25-199">And this command returns information for all the external user access policies:</span></span>

`Get-CsExternalAccessPolicy`

<span data-ttu-id="99c25-200">返される情報は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="99c25-200">The returned information will resemble this:</span></span>

<span data-ttu-id="99c25-201">Id: False</span><span class="sxs-lookup"><span data-stu-id="99c25-201">Identity : False</span></span>

<span data-ttu-id="99c25-202">説明</span><span class="sxs-lookup"><span data-stu-id="99c25-202">Description :</span></span>

<span data-ttu-id="99c25-203">EnableFederationAccess: False</span><span class="sxs-lookup"><span data-stu-id="99c25-203">EnableFederationAccess : False</span></span>

<span data-ttu-id="99c25-204">EnablePublicCloudAccess: False</span><span class="sxs-lookup"><span data-stu-id="99c25-204">EnablePublicCloudAccess : False</span></span>

<span data-ttu-id="99c25-205">EnablePublicCloudAccessAudioVideoAccess: False</span><span class="sxs-lookup"><span data-stu-id="99c25-205">EnablePublicCloudAccessAudioVideoAccess : False</span></span>

<span data-ttu-id="99c25-206">EnableOutsideAccess: False</span><span class="sxs-lookup"><span data-stu-id="99c25-206">EnableOutsideAccess : False</span></span>

<span data-ttu-id="99c25-207">**EnableFederationAccess** が True に設定されている場合、特定のポリシーによって管理されるユーザーはフェデレーションユーザーと通信できます。</span><span class="sxs-lookup"><span data-stu-id="99c25-207">If **EnableFederationAccess** is set to True, then users managed by the given policy can communicate with federated users.</span></span>

</div>

</div>

<div>

## <a name="check-archiving-settings"></a><span data-ttu-id="99c25-208">アーカイブ設定を確認する</span><span class="sxs-lookup"><span data-stu-id="99c25-208">Check archiving settings</span></span>

<span data-ttu-id="99c25-209">内部およびフェデレーションされた通信のアーカイブ設定を確認します。内部および外部のアーカイブの設定を確認する前に、アーカイブが有効になっていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="99c25-209">Check archiving settings for internal and federated communications.Before verifying the settings for internal and external archiving, you should verify that archiving is enabled.</span></span>

<span data-ttu-id="99c25-210">アーカイブ構成の設定を確認するには、Windows PowerShell と Get-CsArchivingConfiguration コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="99c25-210">Archiving configuration settings can be verified by using Windows PowerShell and the Get-CsArchivingConfiguration cmdlet:</span></span>

`Get-CsArchivingConfiguration -Identity "Global"`

<span data-ttu-id="99c25-211">アーカイブ設定は、サイトのスコープで構成することもできます。</span><span class="sxs-lookup"><span data-stu-id="99c25-211">Note that archiving settings can also be configured at the site scope.</span></span> <span data-ttu-id="99c25-212">すべてのアーカイブ設定に関する情報を取得するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="99c25-212">To return information about all the archiving settings, use this command:</span></span>

`Get-CsArchivingConfiguration`

<span data-ttu-id="99c25-213">Get-CsArchivingConfiguration コマンドレットは、次のようなデータを返します。</span><span class="sxs-lookup"><span data-stu-id="99c25-213">The Get-CsArchivingConfiguration cmdlet returns data similar to this:</span></span>

<span data-ttu-id="99c25-214">Identity: グローバル</span><span class="sxs-lookup"><span data-stu-id="99c25-214">Identity : Global</span></span>

<span data-ttu-id="99c25-215">EnableArchiving: False</span><span class="sxs-lookup"><span data-stu-id="99c25-215">EnableArchiving : False</span></span>

<span data-ttu-id="99c25-216">EnablePurging: False</span><span class="sxs-lookup"><span data-stu-id="99c25-216">EnablePurging : False</span></span>

<span data-ttu-id="99c25-217">PurgeExportedArchivesOnly: False</span><span class="sxs-lookup"><span data-stu-id="99c25-217">PurgeExportedArchivesOnly : False</span></span>

<span data-ttu-id="99c25-218">Blockonアーカイブエラー: False</span><span class="sxs-lookup"><span data-stu-id="99c25-218">BlockOnArchiveFailure : False</span></span>

<span data-ttu-id="99c25-219">KeepArchivingDataForDays:14</span><span class="sxs-lookup"><span data-stu-id="99c25-219">KeepArchivingDataForDays : 14</span></span>

<span data-ttu-id="99c25-220">PurgeHourOfDay: 2</span><span class="sxs-lookup"><span data-stu-id="99c25-220">PurgeHourOfDay : 2</span></span>

<span data-ttu-id="99c25-221">ArchiveDuplicateMessages: True</span><span class="sxs-lookup"><span data-stu-id="99c25-221">ArchiveDuplicateMessages : True</span></span>

<span data-ttu-id="99c25-222">CachePurgingInterval:24</span><span class="sxs-lookup"><span data-stu-id="99c25-222">CachePurgingInterval : 24</span></span>

<span data-ttu-id="99c25-223">EnableArchiving プロパティが False に設定されている場合は、通信セッションがアーカイブされないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="99c25-223">If the EnableArchiving property is set to False, that means that no communication sessions will be archived.</span></span> <span data-ttu-id="99c25-224">インスタントメッセージングセッションのみをアーカイブする場合は、次のようなコマンドを使用して、IM セッションのアーカイブを有効にします。</span><span class="sxs-lookup"><span data-stu-id="99c25-224">If you want to archive instant messaging sessions only, use a command such as the following to enable the archiving of IM sessions:</span></span>

`Set-CsArchivingConfiguration -Identity "Global" -EnableArchiving "IMOnly"`

<span data-ttu-id="99c25-225">会議セッションとインスタントメッセージングセッションをアーカイブするには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="99c25-225">To archive conferencing sessions and instant messaging sessions, use this command:</span></span>

`Set-CsArchivingConfiguration -Identity "Global" -EnableArchiving "IMOnly"`

<span data-ttu-id="99c25-226">現在のアーカイブ設定と既定の設定を比較する場合は、次の Windows PowerShell コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="99c25-226">If you’d like to compare your current archiving settings with the default settings, run the following Windows PowerShell command:</span></span>

`New-CsArchivingConfiguration -Identity "Global" -InMemory`

<span data-ttu-id="99c25-227">このコマンドによって、グローバルアーカイブ構成の設定のメモリ内のみのインスタンスが作成されます。</span><span class="sxs-lookup"><span data-stu-id="99c25-227">That command creates an in-memory-only instance of the global archiving configuration settings.</span></span> <span data-ttu-id="99c25-228">これは、Lync Server によって使用される設定の実際のコレクションではありません。</span><span class="sxs-lookup"><span data-stu-id="99c25-228">This is not a real collection of settings that is used by Lync Server.</span></span> <span data-ttu-id="99c25-229">ただし、すべてのアーカイブ構成プロパティの既定値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="99c25-229">However, it does display the default values for all the archiving configuration properties.</span></span>

<span data-ttu-id="99c25-230">このコマンドを使用して、アーカイブサーバーの FQDN を返すこともできます。</span><span class="sxs-lookup"><span data-stu-id="99c25-230">You can also use this command to return the FQDN of your Archiving servers:</span></span>

`Get-CsService -ArchivingServer`

<span data-ttu-id="99c25-231">アーカイブが有効になっていることを確認したら、アーカイブポリシーを表示して、内部と外部の通信セッションがアーカイブされているかどうかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="99c25-231">After you have verified that archiving is enabled, you can then view your archiving policies to determine whether internal and external communication sessions are being archived.</span></span>

<span data-ttu-id="99c25-232">アーカイブポリシー情報は Get-CsArchivingPolicy コマンドレットを使用して取得できます。</span><span class="sxs-lookup"><span data-stu-id="99c25-232">Archiving policy information can be retrieved by using the Get-CsArchivingPolicy cmdlet.</span></span> <span data-ttu-id="99c25-233">たとえば、次のコマンドはグローバルアーカイブポリシーに関する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="99c25-233">For example, this command returns information about the global archiving policy:</span></span>

`Get-CsArchivingPolicy -Identity "Global"`

<span data-ttu-id="99c25-234">アーカイブポリシーは、サイトとユーザーごとのスコープで構成することもできるため、次のコマンドを使用して、すべてのアーカイブポリシーに関する情報を返すこともできます。</span><span class="sxs-lookup"><span data-stu-id="99c25-234">Because archiving policies can also be configured at the site and the per-user scope, you might also want to use this command, which returns information about all the archiving policies:</span></span>

`Get-CsArchivingPolicy`

<span data-ttu-id="99c25-235">Get-CsArchivingPolicy から受け取る情報は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="99c25-235">The information that you receive from Get-CsArchivingPolicy will resemble this:</span></span>

<span data-ttu-id="99c25-236">Identity: グローバル</span><span class="sxs-lookup"><span data-stu-id="99c25-236">Identity : Global</span></span>

<span data-ttu-id="99c25-237">説明</span><span class="sxs-lookup"><span data-stu-id="99c25-237">Description :</span></span>

<span data-ttu-id="99c25-238">アーカイブ内部: False</span><span class="sxs-lookup"><span data-stu-id="99c25-238">ArchiveInternal : False</span></span>

<span data-ttu-id="99c25-239">アーカイブ外部: False</span><span class="sxs-lookup"><span data-stu-id="99c25-239">ArchiveExternal : False</span></span>

<span data-ttu-id="99c25-240">アーカイブポリシーでは、既定では、内部および外部のアーカイブの両方が無効になっていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="99c25-240">Note that, by default, both internal and external archiving are disabled in an archiving policy.</span></span>

</div>

<div>

## <a name="check-cdr-settings"></a><span data-ttu-id="99c25-241">CDR の設定を確認する</span><span class="sxs-lookup"><span data-stu-id="99c25-241">Check CDR settings</span></span>

<span data-ttu-id="99c25-242">ピアツーピア、電話会議、音声通話の詳細記録の通話の詳細レコード (CDR) 設定を確認します。</span><span class="sxs-lookup"><span data-stu-id="99c25-242">Check Call Detail Record (CDR) settings for peer-to-peer, conferencing, and Voice call detail recording.</span></span> <span data-ttu-id="99c25-243">CDR の設定の詳細については、CsCdrConfiguration コマンドレットを使用して **取得** できます。</span><span class="sxs-lookup"><span data-stu-id="99c25-243">Detailed information about your CDR settings can be returned by using the **Get-CsCdrConfiguration** cmdlet.</span></span> <span data-ttu-id="99c25-244">たとえば、次のコマンドは、CDR 構成設定のグローバルコレクションに関する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="99c25-244">For example, this command returns information about the global collection of CDR configuration settings:</span></span>

`Get-CsCdrConfiguration -Identity "Global"`

<span data-ttu-id="99c25-245">また、CDR はサイトのスコープでも設定できるため、このコマンドを実行することもできます。これは、すべての CDR 構成の設定に関する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="99c25-245">Because CDR can also be configured at the site scope, you might also want to run this command, which returns information about all the CDR configuration settings:</span></span>

`Get-CsCdrConfiguration`

<span data-ttu-id="99c25-246">Get-CsCdrConfiguration コマンドレットは、CDR 構成設定のコレクションごとに、次のような情報を返します。</span><span class="sxs-lookup"><span data-stu-id="99c25-246">The Get-CsCdrConfiguration cmdlet returns information similar to this for each collection of CDR configuration settings:</span></span>

<span data-ttu-id="99c25-247">Identity: グローバル</span><span class="sxs-lookup"><span data-stu-id="99c25-247">Identity : Global</span></span>

<span data-ttu-id="99c25-248">EnableCDR: True</span><span class="sxs-lookup"><span data-stu-id="99c25-248">EnableCDR : True</span></span>

<span data-ttu-id="99c25-249">EnablePurging: True</span><span class="sxs-lookup"><span data-stu-id="99c25-249">EnablePurging : True</span></span>

<span data-ttu-id="99c25-250">KeepCallDetailForDays:60</span><span class="sxs-lookup"><span data-stu-id="99c25-250">KeepCallDetailForDays : 60</span></span>

<span data-ttu-id="99c25-251">KeepErrorReportForDays:60</span><span class="sxs-lookup"><span data-stu-id="99c25-251">KeepErrorReportForDays : 60</span></span>

<span data-ttu-id="99c25-252">PurgeHourOfDay: 2</span><span class="sxs-lookup"><span data-stu-id="99c25-252">PurgeHourOfDay : 2</span></span>

<span data-ttu-id="99c25-253">QoE の監視の場合、Get-CsQoEConfiguration コマンドレットを使用して同様の情報を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="99c25-253">Similar information can be returned for QoE monitoring by using the Get-CsQoEConfiguration cmdlet.</span></span> <span data-ttu-id="99c25-254">たとえば、次のコマンドは、QoE 構成設定のグローバルコレクションに関する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="99c25-254">For example, this command returns information about the global collection of QoE configuration settings:</span></span>

`Get-QoEConfiguration -Identity "Global"`

<span data-ttu-id="99c25-255">この情報は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="99c25-255">That information will resemble this:</span></span>

<span data-ttu-id="99c25-256">Identity: グローバル</span><span class="sxs-lookup"><span data-stu-id="99c25-256">Identity : Global</span></span>

<span data-ttu-id="99c25-257">ExternalConsumerIssuedCertId :</span><span class="sxs-lookup"><span data-stu-id="99c25-257">ExternalConsumerIssuedCertId :</span></span>

<span data-ttu-id="99c25-258">EnablePurging: True</span><span class="sxs-lookup"><span data-stu-id="99c25-258">EnablePurging : True</span></span>

<span data-ttu-id="99c25-259">KeepQoEDataForDays:60</span><span class="sxs-lookup"><span data-stu-id="99c25-259">KeepQoEDataForDays : 60</span></span>

<span data-ttu-id="99c25-260">PurgeHourOfDay: 1</span><span class="sxs-lookup"><span data-stu-id="99c25-260">PurgeHourOfDay : 1</span></span>

<span data-ttu-id="99c25-261">EnableExternalConsumer: False</span><span class="sxs-lookup"><span data-stu-id="99c25-261">EnableExternalConsumer : False</span></span>

<span data-ttu-id="99c25-262">ExternalConsumerName :</span><span class="sxs-lookup"><span data-stu-id="99c25-262">ExternalConsumerName :</span></span>

<span data-ttu-id="99c25-263">ExternalConsumerURL :</span><span class="sxs-lookup"><span data-stu-id="99c25-263">ExternalConsumerURL :</span></span>

<span data-ttu-id="99c25-264">EnableQoE: True</span><span class="sxs-lookup"><span data-stu-id="99c25-264">EnableQoE : True</span></span>

<span data-ttu-id="99c25-265">現在の CDR 設定と既定の CDR 設定を比較する場合は、次のコマンドを実行して既定値を確認できます。</span><span class="sxs-lookup"><span data-stu-id="99c25-265">If you want to compare your current CDR settings with the default CDR settings, the default values can be reviewed by running this command:</span></span>

`New-CsCdrConfiguration -Identity "Global" -InMemory`

<span data-ttu-id="99c25-266">同様に、次のコマンドを使用して、QoE モニターの既定値を取得できます。</span><span class="sxs-lookup"><span data-stu-id="99c25-266">Likewise, the default values for QoE monitoring can be retrieved by using this command:</span></span>

`New-CsQoEConfiguration -Identity "Global" -InMemory`

<span data-ttu-id="99c25-267">このコマンドを実行して、監視サーバーの FQDN を返すこともできます。</span><span class="sxs-lookup"><span data-stu-id="99c25-267">You can also return the FQDN of your Monitoring servers by running this command:</span></span>

`Get-CsService -MonitoringServer`

</div>

<div>

## <a name="check-voice-settings"></a><span data-ttu-id="99c25-268">音声の設定を確認する</span><span class="sxs-lookup"><span data-stu-id="99c25-268">Check voice settings</span></span>

<span data-ttu-id="99c25-269">音声設定は、通常、管理者にとって重要です。音声ポリシーには、個々のユーザーに対して公開される機能を決定する設定 (通話の転送や転送機能など) が含まれていますが、音声ルーティングでは、通話が PSTN 経由でルーティングされる方法が決まります。</span><span class="sxs-lookup"><span data-stu-id="99c25-269">The voice settings typically important to administrators are contained in voice policies and voice routes: voice policies contain the settings that determine the capabilities exposed to individual users (such as the ability to forward or transfer calls), while voice routes determine how (and if) calls are routed across the PSTN.</span></span>

<span data-ttu-id="99c25-270">音声ポリシー情報は、Windows PowerShell を使用して取得できます。</span><span class="sxs-lookup"><span data-stu-id="99c25-270">Voice policy information can be retrieved by using Windows PowerShell.</span></span> <span data-ttu-id="99c25-271">たとえば、次のコマンドはグローバルボイスポリシーに関する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="99c25-271">For example, this command returns information about the global voice policy:</span></span>

`Get-CsVoicePolicy -Identity "Global"`

<span data-ttu-id="99c25-272">このコマンドは、組織で使用するように構成されているすべてのボイスポリシーに関する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="99c25-272">And this command returns information about all the voice policies configured for use in the organization:</span></span>

`Get-CsVoicePolicy`

<span data-ttu-id="99c25-273">Get-CsVoicePolicy コマンドレットによって返される情報は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="99c25-273">The information returned by the Get-CsVoicePolicy cmdlet resembles the following:</span></span>

<span data-ttu-id="99c25-274">Identity: グローバル</span><span class="sxs-lookup"><span data-stu-id="99c25-274">Identity : Global</span></span>

<span data-ttu-id="99c25-275">PstnUsages : {}</span><span class="sxs-lookup"><span data-stu-id="99c25-275">PstnUsages : {}</span></span>

<span data-ttu-id="99c25-276">説明</span><span class="sxs-lookup"><span data-stu-id="99c25-276">Description :</span></span>

<span data-ttu-id="99c25-277">AllowSimulRing: True</span><span class="sxs-lookup"><span data-stu-id="99c25-277">AllowSimulRing : True</span></span>

<span data-ttu-id="99c25-278">AllowCallForwarding: True</span><span class="sxs-lookup"><span data-stu-id="99c25-278">AllowCallForwarding : True</span></span>

<span data-ttu-id="99c25-279">AllowPSTNReRouting: True</span><span class="sxs-lookup"><span data-stu-id="99c25-279">AllowPSTNReRouting : True</span></span>

<span data-ttu-id="99c25-280">Name: DefaultPolicy</span><span class="sxs-lookup"><span data-stu-id="99c25-280">Name : DefaultPolicy</span></span>

<span data-ttu-id="99c25-281">EnableDelegation: True</span><span class="sxs-lookup"><span data-stu-id="99c25-281">EnableDelegation : True</span></span>

<span data-ttu-id="99c25-282">EnableTeamCall: True</span><span class="sxs-lookup"><span data-stu-id="99c25-282">EnableTeamCall : True</span></span>

<span data-ttu-id="99c25-283">EnableCallTransfer: True</span><span class="sxs-lookup"><span data-stu-id="99c25-283">EnableCallTransfer : True</span></span>

<span data-ttu-id="99c25-284">EnableCallPark: False</span><span class="sxs-lookup"><span data-stu-id="99c25-284">EnableCallPark : False</span></span>

<span data-ttu-id="99c25-285">EnableMaliciousCallTracing: False</span><span class="sxs-lookup"><span data-stu-id="99c25-285">EnableMaliciousCallTracing : False</span></span>

<span data-ttu-id="99c25-286">EnableBWPolicyOverride: False</span><span class="sxs-lookup"><span data-stu-id="99c25-286">EnableBWPolicyOverride : False</span></span>

<span data-ttu-id="99c25-287">PreventPSTNTollBypass: False</span><span class="sxs-lookup"><span data-stu-id="99c25-287">PreventPSTNTollBypass : False</span></span>

<span data-ttu-id="99c25-288">音声ポリシーのサブセットを返すクエリを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="99c25-288">You can also create queries that returned a subset of your voice policies.</span></span> <span data-ttu-id="99c25-289">たとえば、次のコマンドは、着信の転送を許可するすべての音声ポリシーを返します。</span><span class="sxs-lookup"><span data-stu-id="99c25-289">For example, this command returns all the voice policies that allow call forwarding:</span></span>

`Get-CsVoicePolicy | Where-Object {$_.AllowCallForwarding -eq $True}`

<span data-ttu-id="99c25-290">このコマンドは、着信の転送を許可していないすべての音声ポリシーを返します。</span><span class="sxs-lookup"><span data-stu-id="99c25-290">And this command returns all the voice policies that don’t allow call forwarding:</span></span>

`Get-CsVoicePolicy | Where-Object {$_.AllowCallForwarding -eq $False}`

<span data-ttu-id="99c25-291">Windows PowerShell では、Get-CsVoiceRouting コマンドレットを使用して、音声ルートに関する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="99c25-291">In Windows PowerShell, use the Get-CsVoiceRouting cmdlet to return information about your voice routes:</span></span>

`Get-CsVoiceRoute`

<span data-ttu-id="99c25-292">このコマンドは、すべての音声ルートについて、次のような情報を返します。</span><span class="sxs-lookup"><span data-stu-id="99c25-292">That command returns information such as this for all the voice routes:</span></span>

<span data-ttu-id="99c25-293">Identity: LocalRoute</span><span class="sxs-lookup"><span data-stu-id="99c25-293">Identity : LocalRoute</span></span>

<span data-ttu-id="99c25-294">優先度: 0</span><span class="sxs-lookup"><span data-stu-id="99c25-294">Priority : 0</span></span>

<span data-ttu-id="99c25-295">説明</span><span class="sxs-lookup"><span data-stu-id="99c25-295">Description :</span></span>

<span data-ttu-id="99c25-296">数字パターン: ^ ( \\ + 1 \[ 0-9 \] {10} ) $</span><span class="sxs-lookup"><span data-stu-id="99c25-296">NumberPattern : ^(\\+1\[0-9\]{10})$</span></span>

<span data-ttu-id="99c25-297">PstnUsages : {}</span><span class="sxs-lookup"><span data-stu-id="99c25-297">PstnUsages : {}</span></span>

<span data-ttu-id="99c25-298">PstnGatewayList : {}</span><span class="sxs-lookup"><span data-stu-id="99c25-298">PstnGatewayList : {}</span></span>

<span data-ttu-id="99c25-299">Name: LocalRoute</span><span class="sxs-lookup"><span data-stu-id="99c25-299">Name : LocalRoute</span></span>

<span data-ttu-id="99c25-300">SuppressCallerId :</span><span class="sxs-lookup"><span data-stu-id="99c25-300">SuppressCallerId :</span></span>

<span data-ttu-id="99c25-301">AlternateCallerId :</span><span class="sxs-lookup"><span data-stu-id="99c25-301">AlternateCallerId :</span></span>

<span data-ttu-id="99c25-302">Lync Server を使用すると、PSTN を使わず、PSTN ゲートウェイを指定しないボイスルートを作成できます。</span><span class="sxs-lookup"><span data-stu-id="99c25-302">Lync Server allows you to create voice routes that do not have a PSTN usage and do not specify a PSTN gateway.</span></span> <span data-ttu-id="99c25-303">ただし、この2つのプロパティ値が構成されていないボイスルーティングでは、実際に着信をルーティングすることはできません。</span><span class="sxs-lookup"><span data-stu-id="99c25-303">However, you can't actually route calls over a voice route that does not have these two property values configured.</span></span> <span data-ttu-id="99c25-304">そのため、このコマンドを定期的に実行すると便利な場合があります。これは、PSTN を使用していないボイスルートの id を返します。</span><span class="sxs-lookup"><span data-stu-id="99c25-304">Because of that, you might find it useful to periodically run this command, which returns the identity of any voice route that does not have a PSTN usage:</span></span>

`Get-CsVoiceRoute | Where-Object {$_.PstnUsages -eq $Null} | Select-Object Identity`

<span data-ttu-id="99c25-305">同様に、このコマンドは、PSTN ゲートウェイを使用するように構成されていないすべてのボイスルートの id を返します。</span><span class="sxs-lookup"><span data-stu-id="99c25-305">Similarly, this command returns the identity of any voice route that has not been configured to have a PSTN gateway:</span></span>

`Get-CsVoiceRoute | Where-Object {$_.PstnGatewayList -eq $Null}} | Select-Object Identity`

</div>

<div>

## <a name="check-conferencing-attendant-settings"></a><span data-ttu-id="99c25-306">会議アテンダントの設定を確認する</span><span class="sxs-lookup"><span data-stu-id="99c25-306">Check Conferencing Attendant settings</span></span>

<span data-ttu-id="99c25-307">PSTN ダイヤルイン会議の会議アテンダントの設定を確認します。</span><span class="sxs-lookup"><span data-stu-id="99c25-307">Check conferencing Attendant settings for PSTN dial-in conferencing.</span></span> <span data-ttu-id="99c25-308">会議アテンダントの設定を取得するには、 **CsDialInConferencingConfiguration** コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="99c25-308">Conferencing Attendant settings can only be retrieved by using the **Get-CsDialInConferencingConfiguration** cmdlet.</span></span> <span data-ttu-id="99c25-309">これらの設定は Lync Server コントロールパネルでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="99c25-309">These settings are not available in the Lync Server Control Panel.</span></span> <span data-ttu-id="99c25-310">会議アテンダントの設定を表示するには、次のような Windows PowerShell コマンドを使います。これは、会議アテンダント設定のグローバルコレクションを返します。</span><span class="sxs-lookup"><span data-stu-id="99c25-310">To view your Conferencing Attendant settings, use a Windows PowerShell command similar to the following, which returns the global collection of Conferencing Attendant settings:</span></span>

`Get-CsDialInConferencingConfiguration -Identity "Global"`

<span data-ttu-id="99c25-311">会議アテンダントの設定は、サイトのスコープで構成することもできます。</span><span class="sxs-lookup"><span data-stu-id="99c25-311">Note that Conferencing Attendant settings can also be configured at the site scope.</span></span> <span data-ttu-id="99c25-312">会議アテンダントのすべての設定に関する情報を取得するには、代わりに次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="99c25-312">To return information about all the Conferencing Attendant settings, use this command instead:</span></span>

`Get-CsDialInConferencingConfiguration`

<span data-ttu-id="99c25-313">Get-CsDialInConferencingConfiguration コマンドレットは、次のようなデータを返します。</span><span class="sxs-lookup"><span data-stu-id="99c25-313">The Get-CsDialInConferencingConfiguration cmdlet returns data similar to this:</span></span>

<span data-ttu-id="99c25-314">Identity: グローバル</span><span class="sxs-lookup"><span data-stu-id="99c25-314">Identity : Global</span></span>

<span data-ttu-id="99c25-315">Entryexitアナウンスの場合: UseNames</span><span class="sxs-lookup"><span data-stu-id="99c25-315">EntryExitAnnouncementsType : UseNames</span></span>

<span data-ttu-id="99c25-316">EnableNameRecording: True</span><span class="sxs-lookup"><span data-stu-id="99c25-316">EnableNameRecording : True</span></span>

<span data-ttu-id="99c25-317">EntryExitAnnouncementsEnabledByDefault: False</span><span class="sxs-lookup"><span data-stu-id="99c25-317">EntryExitAnnouncementsEnabledByDefault : False</span></span>

<span data-ttu-id="99c25-318">EntryExitAnnouncementsEnabledByDefault が False に設定されている場合は、会議のアナウンスが無効になっていることを意味します。</span><span class="sxs-lookup"><span data-stu-id="99c25-318">If EntryExitAnnouncementsEnabledByDefault is set to False, that means the conferencing announcements are disabled.</span></span> <span data-ttu-id="99c25-319">エントリと終了のアナウンスを有効にするには、次のように Windows PowerShell コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="99c25-319">To enable entry and exit announcements, run a Windows PowerShell command similar to this:</span></span>

`Set-CsDialInConferencingConfiguration -Identity "Global" -EntryExitAnnouncementsEnabledByDefault $True`

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="99c25-320">関連項目</span><span class="sxs-lookup"><span data-stu-id="99c25-320">See Also</span></span>


[<span data-ttu-id="99c25-321">Get-CsSipDomain</span><span class="sxs-lookup"><span data-stu-id="99c25-321">Get-CsSipDomain</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsSipDomain)  
[<span data-ttu-id="99c25-322">Get-CsMeetingConfiguration</span><span class="sxs-lookup"><span data-stu-id="99c25-322">Get-CsMeetingConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsMeetingConfiguration)  
[<span data-ttu-id="99c25-323">CsService の入手</span><span class="sxs-lookup"><span data-stu-id="99c25-323">Get-CsService</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsService)  
[<span data-ttu-id="99c25-324">Get-CsAccessEdgeConfiguration</span><span class="sxs-lookup"><span data-stu-id="99c25-324">Get-CsAccessEdgeConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsAccessEdgeConfiguration)  
[<span data-ttu-id="99c25-325">Get-CsExternalAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="99c25-325">Get-CsExternalAccessPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsExternalAccessPolicy)  
[<span data-ttu-id="99c25-326">Get-CsArchivingConfiguration</span><span class="sxs-lookup"><span data-stu-id="99c25-326">Get-CsArchivingConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsArchivingConfiguration)  
[<span data-ttu-id="99c25-327">Get-CsCdrConfiguration</span><span class="sxs-lookup"><span data-stu-id="99c25-327">Get-CsCdrConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsCdrConfiguration)  
[<span data-ttu-id="99c25-328">取得-CsQoEConfiguration しくみ</span><span class="sxs-lookup"><span data-stu-id="99c25-328">Get-CsQoEConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsQoEConfiguration)  
[<span data-ttu-id="99c25-329">Get-CsVoicePolicy</span><span class="sxs-lookup"><span data-stu-id="99c25-329">Get-CsVoicePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsVoicePolicy)  
[<span data-ttu-id="99c25-330">Get-CsVoiceRoute</span><span class="sxs-lookup"><span data-stu-id="99c25-330">Get-CsVoiceRoute</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsVoiceRoute)  
[<span data-ttu-id="99c25-331">Get-CsDialInConferencingConfiguration</span><span class="sxs-lookup"><span data-stu-id="99c25-331">Get-CsDialInConferencingConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsDialInConferencingConfiguration)  
  

<span data-ttu-id="99c25-332"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="99c25-332"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

