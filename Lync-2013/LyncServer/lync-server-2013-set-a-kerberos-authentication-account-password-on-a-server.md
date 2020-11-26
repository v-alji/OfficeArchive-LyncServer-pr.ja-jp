---
title: 'Lync Server 2013: サーバーへの Kerberos 認証アカウント パスワードの設定'
description: 'Lync Server 2013: サーバーで Kerberos 認証アカウントのパスワードを設定します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Set a Kerberos authentication account password on a server
ms:assetid: 902d3292-678d-4512-9248-586053cb638b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398734(v=OCS.15)
ms:contentKeyID: 48184787
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 723392e670ca0b4bc9796cd62dab3b1a61f99dd1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444785"
---
# <a name="set-a-kerberos-authentication-account-password-on-a-server-in-lync-server-2013"></a><span data-ttu-id="4634b-103">Lync Server 2013 でのサーバーへの Kerberos 認証アカウント パスワードの設定</span><span class="sxs-lookup"><span data-stu-id="4634b-103">Set a Kerberos authentication account password on a server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4634b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4634b-104">

<span> </span></span></span>

<span data-ttu-id="4634b-105">_**最終更新日:** 2012-01-16_</span><span class="sxs-lookup"><span data-stu-id="4634b-105">_**Topic Last Modified:** 2012-01-16_</span></span>

<span data-ttu-id="4634b-106">この手順を正常に完了するには、RTCUniversalServerAdmins グループのメンバーであるユーザーとしてログオンする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4634b-106">To successfully complete this procedure you should be logged on as a user who is a member of the RTCUniversalServerAdmins group.</span></span>

<span data-ttu-id="4634b-107">フロントエンドサーバー、標準エディションサーバー、およびディレクターがある各サイトの Kerberos アカウントでパスワードを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4634b-107">You must set up a password on the Kerberos account for each site that has Front End Servers, Standard Edition servers, and Directors.</span></span> <span data-ttu-id="4634b-108">パスワードを設定するには、サイト内の1つのサーバー (たとえば、1つのフロントエンドサーバー) に対して、 **set-CsKerberosAccountPassword** Windows PowerShell コマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="4634b-108">You can set up the password by running the **Set-CsKerberosAccountPassword** Windows PowerShell cmdlet on one server in the site (for example, one Front End Server).</span></span> <span data-ttu-id="4634b-109">各サイトについて、 **Set-Csker"@ Accountpassword** " コマンドレットを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4634b-109">For each site, you must run the **Set-CsKerberosAccountPassword** cmdlet.</span></span> <span data-ttu-id="4634b-110">Web サービス用のインターネットインフォメーションサービス (IIS) を構成し、Active Directory ドメインサービスのコンピューターアカウントにパスワードを設定します。</span><span class="sxs-lookup"><span data-stu-id="4634b-110">The cmdlet configures Internet Information Services (IIS) for the Web Services service, and then sets the password on the computer account in Active Directory Domain Services.</span></span> <span data-ttu-id="4634b-111">コマンドレットで使用されるパラメーターに基づいた代替メソッドは、Kerberos アカウントのパスワードのソースとして構成されている別のサーバーを使用しているときに、あるサーバーで IIS を構成します。</span><span class="sxs-lookup"><span data-stu-id="4634b-111">An alternate method, based on which parameter is used with the cmdlet, configures IIS on one server while using another server that has been configured as the source of the Kerberos account password.</span></span>

<span data-ttu-id="4634b-112">**Set-Cskerの** コマンドレットを使用してパスワードを設定すると、Kerberos はパスワードをランダムに生成された文字列に設定します。</span><span class="sxs-lookup"><span data-stu-id="4634b-112">When you use the **Set-CsKerberosAccountPassword** cmdlet to set a password, Kerberos sets the password to a randomly generated string.</span></span> <span data-ttu-id="4634b-113">このコマンドレットは、このアカウントが割り当てられているすべての Lync Server 2013 セントラルサイト内のすべての IIS インスタンスに接続します。</span><span class="sxs-lookup"><span data-stu-id="4634b-113">This cmdlet contacts all IIS instances in all Lync Server 2013 central sites to which this account is assigned.</span></span>

<div>

## <a name="to-set-a-password-for-a-kerberos-authentication-account"></a><span data-ttu-id="4634b-114">Kerberos 認証アカウントのパスワードを設定するには</span><span class="sxs-lookup"><span data-stu-id="4634b-114">To set a password for a Kerberos authentication account</span></span>

1.  <span data-ttu-id="4634b-115">RTCUniversalServerAdmins グループのメンバーとしてインストールされている Lync Server 管理シェルがインストールされている任意のドメインコンピューターにログオンします。</span><span class="sxs-lookup"><span data-stu-id="4634b-115">Log on to any domain computer with Lync Server Management Shell installed as a member of the RTCUniversalServerAdmins group.</span></span>

2.  <span data-ttu-id="4634b-116">Lync Server 管理シェルを起動します。 [ **スタート**] をクリックし、[ **すべてのプログラム**]、[ **Microsoft Lync Server 2013**]、[ **lync server 管理シェル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="4634b-116">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="4634b-117">コマンドラインで、次の2つのコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="4634b-117">From the command line, run the following two commands:</span></span>
    
        Set-CsKerberosAccountPassword -UserAccount "Domain\UserAccount"
    
    <span data-ttu-id="4634b-118">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="4634b-118">For example:</span></span>
    
        Set-CsKerberosAccountPassword -UserAccount "contoso\KerbAuth"
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="4634b-119">UserAccount パラメーターを指定するには、Domain\User 形式を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4634b-119">You must specify the UserAccount parameter by using the Domain\User format.</span></span> <span data-ttu-id="4634b-120">Kerberos 認証のために作成されたコンピューターオブジェクトを参照する場合、User@Domain 拡張子形式はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="4634b-120">The User@Domain.extension format is not supported for referencing the computer objects created for Kerberos authentication purposes.</span></span>

    
    </div>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="4634b-121">アカウントの追加やアカウントの削除など、Kerberos 認証を変更した後は、Lync Server 管理シェルのコマンドプロンプトから、 <STRONG>Enable-CsTopology</STRONG> 方法を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4634b-121">After making any changes to Kerberos authentication, such as adding an account or removing an account, you must run <STRONG>Enable-CsTopology</STRONG> from the Lync Server Management Shell command prompt.</span></span>

    
    <span data-ttu-id="4634b-122"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4634b-122"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

