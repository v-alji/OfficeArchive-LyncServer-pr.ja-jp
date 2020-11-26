---
title: Kerberos 認証アカウント パスワードと IIS との同期
description: Kerberos 認証アカウントのパスワードを IIS に同期します。
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Synchronize a Kerberos authentication account password to IIS
ms:assetid: 05925a66-2684-4c1b-adfa-69bd0da1bf38
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398107(v=OCS.15)
ms:contentKeyID: 48183296
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 59555fc25088d0d932105f77051f959b4bcebb46
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444587"
---
# <a name="synchronize-a-kerberos-authentication-account-password-to-iis-in-lync-server-2013"></a><span data-ttu-id="fecb9-103">Lync Server 2013 での Kerberos 認証アカウント パスワードと IIS との同期</span><span class="sxs-lookup"><span data-stu-id="fecb9-103">Synchronize a Kerberos authentication account password to IIS in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fecb9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fecb9-104">

<span> </span></span></span>

<span data-ttu-id="fecb9-105">_**最終更新日:** 2010-11-08_</span><span class="sxs-lookup"><span data-stu-id="fecb9-105">_**Topic Last Modified:** 2010-11-08_</span></span>

<span data-ttu-id="fecb9-106">この手順を正常に完了するには、RTCUniversalServerAdmins グループのメンバーであるユーザーとしてログオンする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fecb9-106">To successfully complete this procedure you should be logged on as a user who is a member of the RTCUniversalServerAdmins group.</span></span>

<span data-ttu-id="fecb9-107">サイトでは、フロントエンドサーバー、標準エディションサーバー、およびディレクターは、Web サービスサービスへの要求を認証するために、Kerberos 認証アカウントを使うことができます。</span><span class="sxs-lookup"><span data-stu-id="fecb9-107">In a site, Front End Servers, Standard Edition servers, and Directors can use a Kerberos authentication account for purposes of authenticating requests to the Web Services service.</span></span> <span data-ttu-id="fecb9-108">この手順では、Kerberos アカウントが割り当てられているサイトで Web サービスを実行している各サーバーを特定し、その Kerberos アカウントを使用するようにインターネットインフォメーションサービス (IIS) 構成設定を更新します。</span><span class="sxs-lookup"><span data-stu-id="fecb9-108">This procedure locates each server running Web Services in a site that has been assigned a Kerberos account and updates the Internet Information Services (IIS) configuration settings to use the Kerberos account.</span></span> <span data-ttu-id="fecb9-109">詳細については、「 [Lync server 2013 でサーバー上の Kerberos 認証アカウントパスワードを設定する](lync-server-2013-set-a-kerberos-authentication-account-password-on-a-server.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fecb9-109">For details, see [Set a Kerberos authentication account password on a server in Lync Server 2013](lync-server-2013-set-a-kerberos-authentication-account-password-on-a-server.md).</span></span>

<div>

## <a name="to-set-and-configure-a-kerberos-authentication-account-password"></a><span data-ttu-id="fecb9-110">Kerberos 認証アカウントのパスワードを設定および構成するには</span><span class="sxs-lookup"><span data-stu-id="fecb9-110">To set and configure a Kerberos authentication account password</span></span>

1.  <span data-ttu-id="fecb9-111">ソースコンピューター (fe01.contoso.com など) に RTCUniversalServerAdmins グループのメンバーとしてログオンします。</span><span class="sxs-lookup"><span data-stu-id="fecb9-111">Log on to a source computer (such as fe01.contoso.com) as a member of RTCUniversalServerAdmins group.</span></span>

2.  <span data-ttu-id="fecb9-112">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="fecb9-112">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="fecb9-113">Lync Server 管理シェルコマンドラインから次の2つのコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="fecb9-113">From the Lync Server Management Shell command line, run the following two commands:</span></span>
    
        Set-CsKerberosAccountPassword -FromComputer SourceComputer -ToComputer DestinationComputer
    
    <span data-ttu-id="fecb9-114">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="fecb9-114">For example:</span></span>
    
        Set-CsKerberosAccountPassword -FromComputer fe01.contoso.com -ToComputer dir01.contoso.com
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="fecb9-115">ソースコンピューターとターゲットコンピューターの名前は、サーバーの完全修飾ドメイン (FQDN) 名である必要があります。</span><span class="sxs-lookup"><span data-stu-id="fecb9-115">The name of the source computer and destination computer must be a fully qualified domain (FQDN) name of the server.</span></span> <span data-ttu-id="fecb9-116">プール名は、ソースコンピューターまたは移行先コンピューターとして使用しているコンピューターの名前と同じである場合を除き、プールの FQDN は使用できません。</span><span class="sxs-lookup"><span data-stu-id="fecb9-116">You cannot use the pool FQDN unless the pool name is the same as the name of the computer that you are using as a source computer or destination computer.</span></span>

    
    </div>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="fecb9-117">アカウントの追加やアカウントの削除など、Kerberos 認証を変更した後は、Lync Server 管理シェルのコマンドプロンプトから、 <STRONG>Enable-CsTopology</STRONG> 方法を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fecb9-117">After making any changes to Kerberos authentication, such as adding an account or removing an account, you must run <STRONG>Enable-CsTopology</STRONG> from the Lync Server Management Shell command prompt.</span></span>

    
    <span data-ttu-id="fecb9-118"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fecb9-118"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

