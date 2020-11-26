---
title: 'Lync Server 2013: Kerberos 認証アカウント パスワードの設定'
description: 'Lync Server 2013: Kerberos 認証アカウントパスワードを設定します。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up Kerberos authentication account passwords
ms:assetid: b435f88e-4a77-4be7-b7e5-c17484303b74
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412870(v=OCS.15)
ms:contentKeyID: 48185167
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 614b1411f9454c39843f4e69cabbfc3b02986e51
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423973"
---
# <a name="setting-up-kerberos-authentication-account-passwords-in-lync-server-2013"></a><span data-ttu-id="34974-103">Lync Server 2013 での Kerberos 認証アカウント パスワードの設定</span><span class="sxs-lookup"><span data-stu-id="34974-103">Setting up Kerberos authentication account passwords in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="34974-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="34974-104">

<span> </span></span></span>

<span data-ttu-id="34974-105">_**最終更新日:** 2010-11-03_</span><span class="sxs-lookup"><span data-stu-id="34974-105">_**Topic Last Modified:** 2010-11-03_</span></span>

<span data-ttu-id="34974-106">Kerberos 認証アカウントのコンピューターオブジェクトを作成したら、アカウントのパスワードを設定できます。</span><span class="sxs-lookup"><span data-stu-id="34974-106">After you create the computer object for the Kerberos authentication account, you can set up the password for the account.</span></span> <span data-ttu-id="34974-107">1つのサーバーで Kerberos アカウントのパスワードを設定するための Windows PowerShell コマンドレットを実行します。</span><span class="sxs-lookup"><span data-stu-id="34974-107">You run the Windows PowerShell cmdlet for setting the Kerberos account password on one server.</span></span> <span data-ttu-id="34974-108">Kerberos 認証用に作成したオブジェクトに対してパスワードを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="34974-108">You can set the password on the object that you created for the Kerberos authentication.</span></span> <span data-ttu-id="34974-109">パスワードは既知の値に設定できますが、既定ではランダムなパスワードになります。</span><span class="sxs-lookup"><span data-stu-id="34974-109">The password can be set to a known value, but by default is a random password.</span></span> <span data-ttu-id="34974-110">パスワードは、そのアカウントを使用するすべての Kerberos 認証ソースで利用できます。</span><span class="sxs-lookup"><span data-stu-id="34974-110">The password is available to all Kerberos authentication sources that use the account.</span></span> <span data-ttu-id="34974-111">Kerberos アカウントのパスワードをセットアップして管理するには、Windows PowerShell コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="34974-111">You use Windows PowerShell cmdlets to set up and manage Kerberos account passwords.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="34974-112">Kerberos アカウントオブジェクトはコンピューターオブジェクトですが、参照されている Windows PowerShell コマンドレットの操作には UserAccount パラメーターを使います。</span><span class="sxs-lookup"><span data-stu-id="34974-112">The Kerberos account object is a computer object, but uses the UserAccount parameter for operations in the Windows PowerShell cmdlets that are referenced.</span></span> <span data-ttu-id="34974-113">これは間違いではありませんが、Kerberos アカウントの作成とメンテナンスで使用する場合のコマンドレットの動作です。</span><span class="sxs-lookup"><span data-stu-id="34974-113">Note that this is not a mistake, but the intended behavior of the cmdlet when used with the Kerberos account creation and maintenance.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="34974-114">このセクション中</span><span class="sxs-lookup"><span data-stu-id="34974-114">In This Section</span></span>

  - [<span data-ttu-id="34974-115">Lync Server 2013 でのサーバーへの Kerberos 認証アカウント パスワードの設定</span><span class="sxs-lookup"><span data-stu-id="34974-115">Set a Kerberos authentication account password on a server in Lync Server 2013</span></span>](lync-server-2013-set-a-kerberos-authentication-account-password-on-a-server.md)

  - [<span data-ttu-id="34974-116">Lync Server 2013 での Kerberos 認証アカウント パスワードと IIS との同期</span><span class="sxs-lookup"><span data-stu-id="34974-116">Synchronize a Kerberos authentication account password to IIS in Lync Server 2013</span></span>](lync-server-2013-synchronize-a-kerberos-authentication-account-password-to-iis.md)

<span data-ttu-id="34974-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="34974-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

