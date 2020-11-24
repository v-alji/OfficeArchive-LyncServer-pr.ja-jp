---
title: 'Lync Server 2013: Lync Room System Administrative Web Portal の使用'
description: 'Lync Server 2013: Lync Room System 管理 Web ポータルを使用しています。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using the Lync Room System Administrative Web Portal
ms:assetid: c387b2a3-3e42-4642-af72-88126ed2820f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743660(v=OCS.15)
ms:contentKeyID: 62268951
ms.date: 11/13/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 28c29677080bf081eae0fa4227e4cb56ccac697b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49400143"
---
# <a name="using-the-lync-room-system-administrative-web-portal-in-lync-server-2013"></a><span data-ttu-id="7d462-103">Lync Server 2013 での Lync Room System Administrative Web Portal の使用</span><span class="sxs-lookup"><span data-stu-id="7d462-103">Using the Lync Room System Administrative Web Portal in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7d462-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7d462-104">

<span> </span></span></span>

<span data-ttu-id="7d462-105">_**最終更新日:** 2014-11-10_</span><span class="sxs-lookup"><span data-stu-id="7d462-105">_**Topic Last Modified:** 2014-11-10_</span></span>

<span data-ttu-id="7d462-106">サーバーに LRS を展開した後は、ブラウザーから LRS 管理 Web ポータルにサインインして、すべての LRS 室の状態を確認できます。</span><span class="sxs-lookup"><span data-stu-id="7d462-106">After you deploy LRS on the server, you can check the status of all LRS rooms by signing into the LRS Administrative Web Portal from a browser.</span></span>

<div>

## <a name="sign-in"></a><span data-ttu-id="7d462-107">サインイン</span><span class="sxs-lookup"><span data-stu-id="7d462-107">Sign in</span></span>

1.  <span data-ttu-id="7d462-108">次の URL を参照します。</span><span class="sxs-lookup"><span data-stu-id="7d462-108">Browse to the following URL:</span></span>
    
    <span data-ttu-id="7d462-109"> https:// \<fe-server\> /lrs</span><span class="sxs-lookup"><span data-stu-id="7d462-109">https://\<fe-server\>/lrs</span></span>

2.  <span data-ttu-id="7d462-110">LRSSupport アカウントの資格情報または LRSSupportAdminGroup セキュリティグループに追加されたアカウントの資格情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="7d462-110">Enter the credentials for the LRSSupport account or an account that has been added to the LRSSupportAdminGroup security group.</span></span>

<span data-ttu-id="7d462-111">![Lync Room System、管理用ポータル サインイン画面](images/Dn436326.050bcf70-2f3b-46b2-9b96-ebd12679b713(OCS.15).png "Lync Room System、管理用ポータル サインイン画面")</span><span class="sxs-lookup"><span data-stu-id="7d462-111">![Lync Room System Admin Portal Sign In screen](images/Dn436326.050bcf70-2f3b-46b2-9b96-ebd12679b713(OCS.15).png "Lync Room System Admin Portal Sign In screen")</span></span>

</div>

<div>

## <a name="lrs-administrative-web-portal-summary-page"></a><span data-ttu-id="7d462-112">LRS 管理 Web ポータルの概要ページ</span><span class="sxs-lookup"><span data-stu-id="7d462-112">LRS Administrative Web Portal Summary Page</span></span>

<span data-ttu-id="7d462-113">概要ページには、サーバーに展開されているすべての LRS 室に関する次の情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7d462-113">The summary page provides the following information for all of the LRS rooms deployed on the server:</span></span>

  - <span data-ttu-id="7d462-114">**タグ**   管理者によってルームに付与されたカスタム名。</span><span class="sxs-lookup"><span data-stu-id="7d462-114">**Tag**   The custom name that the administrator gives to the room.</span></span> <span data-ttu-id="7d462-115">ルームの名前をクリックすると、ポータルでタグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="7d462-115">The Tag can be set in the portal by clicking on the room name.</span></span>

  - <span data-ttu-id="7d462-116">**動作状態**  ルームの動作状態です。これは、ルームの [動作状態集計] の動作状態から派生し、[ルーム設定] ページの [状態] セクションの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="7d462-116">**Health**   The health status of the room, which is derived from the Aggregate Health status of the room, which is shown under the Health section of the Room Settings page.</span></span>

  - <span data-ttu-id="7d462-117">**次の会議**   次の会議がスケジュールされている日時です。</span><span class="sxs-lookup"><span data-stu-id="7d462-117">**Next Meeting**   The date and time the next meeting is scheduled.</span></span>

  - <span data-ttu-id="7d462-118">**LRS のバージョン、製造元、モデル**   これらの値は、LRS で事前設定されています。</span><span class="sxs-lookup"><span data-stu-id="7d462-118">**LRS Version, Manufacturer, Model**   These values are preset in LRS.</span></span> <span data-ttu-id="7d462-119">製造元によって、これらのフィールドは空白のままである場合があります。</span><span class="sxs-lookup"><span data-stu-id="7d462-119">Depending on the manufacturer, these fields might be left blank.</span></span>

  - <span data-ttu-id="7d462-120">**最終更新**   Web ページの最終更新日を表示します。</span><span class="sxs-lookup"><span data-stu-id="7d462-120">**Last Refresh**   Displays the last time the webpage was refreshed.</span></span>

<span data-ttu-id="7d462-121">![Lync Room System、管理用ポータル概要ビュー](images/Dn743660.f829ce90-dd95-4725-bd94-6870c5dcf046(OCS.15).png "Lync Room System、管理用ポータル概要ビュー")</span><span class="sxs-lookup"><span data-stu-id="7d462-121">![Lync Room System Admin Portal Summary View](images/Dn743660.f829ce90-dd95-4725-bd94-6870c5dcf046(OCS.15).png "Lync Room System Admin Portal Summary View")</span></span>

</div>

<div>

## <a name="lrs-room-information"></a><span data-ttu-id="7d462-122">LRS 室の情報</span><span class="sxs-lookup"><span data-stu-id="7d462-122">LRS Room Information</span></span>

<span data-ttu-id="7d462-123">ポータルの [ルーム情報] セクションでは、個々の LRS ルームを表示して構成することができます。</span><span class="sxs-lookup"><span data-stu-id="7d462-123">The Room Info section of the portal allows you to view and configure individual LRS rooms.</span></span> <span data-ttu-id="7d462-124">これには、[設定]、[詳細]、[トラブルシューティング]、[正常性] の4つのセクションがあります。</span><span class="sxs-lookup"><span data-stu-id="7d462-124">It contains four sections: Settings, Details, Troubleshooting, and Health.</span></span>

<div>

## <a name="settings"></a><span data-ttu-id="7d462-125">設定</span><span class="sxs-lookup"><span data-stu-id="7d462-125">Settings</span></span>

<span data-ttu-id="7d462-126">[設定] セクションでは、パスワード、ルーム タグ、ルームの既定のボリューム レベルを設定できます。</span><span class="sxs-lookup"><span data-stu-id="7d462-126">In the Settings section, you can set the password, room tag, and default volume levels for the room.</span></span> <span data-ttu-id="7d462-127">これらの設定を構成した場合、変更は LRS 本体を再起動した後にのみレプリケートされます。</span><span class="sxs-lookup"><span data-stu-id="7d462-127">If you configure these settings, the changes are replicated only after you restart the LRS console.</span></span> <span data-ttu-id="7d462-128">Lync Room Systems のバージョン15.12 以降のシステム更新設定のみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7d462-128">You will only see System Updates settings for Lync Room Systems that are version 15.12 and later.</span></span>

<span data-ttu-id="7d462-129">![Lync Room System、管理用ポータル ルームの設定](images/Dn743660.ab162e19-41ac-4991-9b2a-92575aa53eda(OCS.15).png "Lync Room System、管理用ポータル ルームの設定")</span><span class="sxs-lookup"><span data-stu-id="7d462-129">![Lync Room System Admin Portal Room Settings](images/Dn743660.ab162e19-41ac-4991-9b2a-92575aa53eda(OCS.15).png "Lync Room System Admin Portal Room Settings")</span></span>

</div>

<div>

## <a name="details"></a><span data-ttu-id="7d462-130">詳細</span><span class="sxs-lookup"><span data-stu-id="7d462-130">Details</span></span>

<span data-ttu-id="7d462-131">[詳細] セクションには、LRS ルームの設定の読み取り専用の概要が表示されます。これには、最終更新時刻が含まれます。次の会議最終更新、メンテナンス、調整。既定のスピーカー、マイク、着信音の設定バージョンSIP URI画面の数と各画面の詳細。状態、アクティビティ。</span><span class="sxs-lookup"><span data-stu-id="7d462-131">The Details section provides a read-only summary of the LRS room’s settings, including: the time of last refresh; next meeting; last updates, maintenance and calibration; default speaker, mic, and ringer settings; version; SIP URI; number of screens and details about each screen; status, and activity.</span></span>

<span data-ttu-id="7d462-132">![Lync Room System、管理用ポータル詳細ビュー](images/Dn743660.2958bbba-db74-4670-a920-87fdfb2fc22d(OCS.15).png "Lync Room System、管理用ポータル詳細ビュー")</span><span class="sxs-lookup"><span data-stu-id="7d462-132">![Lync Room System Admin Portal Detail View](images/Dn743660.2958bbba-db74-4670-a920-87fdfb2fc22d(OCS.15).png "Lync Room System Admin Portal Detail View")</span></span>

</div>

<div>

## <a name="troubleshooting"></a><span data-ttu-id="7d462-133">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="7d462-133">Troubleshooting</span></span>

<span data-ttu-id="7d462-134">[トラブルシューティング] セクションを使用して、ログをリモートで収集し、指定した場所に保存できます。</span><span class="sxs-lookup"><span data-stu-id="7d462-134">The Troubleshooting section can be used to remotely collect logs and save them to a specified location.</span></span> <span data-ttu-id="7d462-135">LRS console (LRS ユーザーインターフェイス) を再起動するか、システム全体を再起動することもできます。</span><span class="sxs-lookup"><span data-stu-id="7d462-135">You can also restart the LRS console (LRS user interface) or restart the entire system.</span></span> <span data-ttu-id="7d462-136">ログを収集するには、指定した形式のフォルダーパスを指定し、フォルダーに LRS コンピューターアカウントに対する書き込みアクセス許可が与えられていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7d462-136">To collect logs, provide a folder path in the specified format and make sure that the folder has write permissions given to the LRS machine account.</span></span> <span data-ttu-id="7d462-137">ログ サイズが大きすぎる場合は、ログの収集を完了するのに最大約 5 分かかる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7d462-137">If the log size is too big, it can take up to 5 minutes to finish collecting logs.</span></span> <span data-ttu-id="7d462-138">ページを更新すると、最新の状態が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7d462-138">Refreshing the page will give you the latest status.</span></span>

<span data-ttu-id="7d462-139">![Lync Room System、管理用ポータル ルームのログ](images/Dn743660.749aee71-deaa-4ace-a146-fe2b349f0f42(OCS.15).png "Lync Room System、管理用ポータル ルームのログ")</span><span class="sxs-lookup"><span data-stu-id="7d462-139">![Lync Room System Admin Portal Room Logging](images/Dn743660.749aee71-deaa-4ace-a146-fe2b349f0f42(OCS.15).png "Lync Room System Admin Portal Room Logging")</span></span>

</div>

<div>

## <a name="health"></a><span data-ttu-id="7d462-140">動作状態</span><span class="sxs-lookup"><span data-stu-id="7d462-140">Health</span></span>

<span data-ttu-id="7d462-141">[正常性] セクションには、Lync Server の接続、オーディオデバイス、ビデオデバイス、復元の状態、および画面デバイスの正常性が視覚的に示されます。</span><span class="sxs-lookup"><span data-stu-id="7d462-141">The Health section gives a visual indication of the health of the Lync Server connection, audio device, video device, resiliency state, and screen device.</span></span>

<span data-ttu-id="7d462-142">![Lync Room System、管理用ポータル ルームの正常性](images/Dn743660.8cc644f8-8e3e-42d5-9079-045d8fe9daa7(OCS.15).png "Lync Room System、管理用ポータル ルームの正常性")</span><span class="sxs-lookup"><span data-stu-id="7d462-142">![Lync Room System Admin Portal Room Health](images/Dn743660.8cc644f8-8e3e-42d5-9079-045d8fe9daa7(OCS.15).png "Lync Room System Admin Portal Room Health")</span></span>

</div>

</div>

<div>

## <a name="additional-notes-about-the-administrative-web-portal"></a><span data-ttu-id="7d462-143">管理 Web ポータルに関する追加の注意事項</span><span class="sxs-lookup"><span data-stu-id="7d462-143">Additional Notes about the Administrative Web Portal</span></span>

<div>


> [!NOTE]  
> <UL>
> <LI>
> <P><span data-ttu-id="7d462-144">設定の変更は、LRS システムを再起動した後にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="7d462-144">Setting changes are applied only after the LRS system is restarted.</span></span></P>
> <LI>
> <P><span data-ttu-id="7d462-145">LRSApp アカウントのパスワードが期限切れになると、ルームの状態を確認できなくなります。</span><span class="sxs-lookup"><span data-stu-id="7d462-145">If the LRSApp account password expires, you will not be able to see the status of the rooms.</span></span> <span data-ttu-id="7d462-146">有効期限が切れないように LRSAppuser account のパスワードを構成するか、有効期限が近いときにパスワードを更新してください。</span><span class="sxs-lookup"><span data-stu-id="7d462-146">Configure the LRSAppuser account password so that it never expires, or be sure to update the password when it’s near expiration.</span></span></P>
> <LI>
> <P><span data-ttu-id="7d462-147">LRS 管理 web ポータルは、オンプレミスの展開でのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="7d462-147">The LRS administrative web portal is supported for on-premises deployments only.</span></span></P></LI></UL>



</div>

</div>

<div>

## <a name="frequently-asked-questions"></a><span data-ttu-id="7d462-148">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="7d462-148">Frequently Asked Questions</span></span>

<div>

## <a name="why-cant-i-sign-in-to-the-administrative-web-portal"></a><span data-ttu-id="7d462-149">管理 Web ポータルにサインインできないのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="7d462-149">Why can’t I sign in to the administrative web portal?</span></span>

  - <span data-ttu-id="7d462-150">を開くと、 https://localhost/lrs サインインページが表示されますが、資格情報を入力するときにサインインすることはできません。</span><span class="sxs-lookup"><span data-stu-id="7d462-150">When you open https://localhost/lrs, you will be able to see the sign in page, but when you type in your credentials, you cannot sign in.</span></span> <span data-ttu-id="7d462-151">この場合、 https://FQDNofFEserver/lrs 管理 web ポータルにサインインするには、を開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d462-151">In this case, you must open https://FQDNofFEserver/lrs to sign in to the administrative web portal.</span></span>

  - <span data-ttu-id="7d462-152">管理 web ポータルにアクセスするコンピューターがワークグループ内にある場合、"http://" は動作しません。</span><span class="sxs-lookup"><span data-stu-id="7d462-152">If the machine from which you are accessing the administrative web portal is in a workgroup, "http://" will not work.</span></span> <span data-ttu-id="7d462-153">代わりに "https" を使用します。</span><span class="sxs-lookup"><span data-stu-id="7d462-153">Use "https" instead.</span></span>

</div>

<div>

## <a name="why-cant-i-see-lrs-in-the-administrative-web-portal"></a><span data-ttu-id="7d462-154">管理 web ポータルに LRS が表示されないのはなぜですか?</span><span class="sxs-lookup"><span data-stu-id="7d462-154">Why can’t I see LRS in the administrative web portal?</span></span>

  - <span data-ttu-id="7d462-155">LRS アカウントが展開に含まれていること、および LRS 管理 Web ポータルの展開に関する推奨事項に従って作成されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7d462-155">Make sure you have LRS accounts in your deployment and that they are created according to the LRS Administrative Web Portal deployment recommendations.</span></span> <span data-ttu-id="7d462-156">Lync server で、LRS のアカウントが、ユーザーを有効にすることなく、Csroom room を使用してプロビジョニングされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7d462-156">Make sure the LRS accounts are provisioned using Enable-CsMeetingRoom, not Enable-CsUser, on the Lync server.</span></span>

  - <span data-ttu-id="7d462-157">LRS アカウントを作成していて、管理 web ポータルにアカウントが表示されない場合は、Lync Server ログツールを使って、 **会議ポータル** コンポーネントが選択されている状態で、サーバーログを収集し、LRS サポート連絡先に送信します。</span><span class="sxs-lookup"><span data-stu-id="7d462-157">If you have created LRS accounts and cannot see the accounts in administrative web portal, collect the server logs by using the Lync Server Logging tool with the **MeetingPortal** component selected, and then send them to your LRS support contact.</span></span>

</div>

<div>

## <a name="why-cant-i-see-the-status-of-lrs-in-the-administrative-web-portal"></a><span data-ttu-id="7d462-158">管理 web ポータルで LRS の状態が表示されないのはなぜですか?</span><span class="sxs-lookup"><span data-stu-id="7d462-158">Why can’t I see the status of LRS in the administrative web portal?</span></span>

  - <span data-ttu-id="7d462-159">LRSApp ユーザー アカウントが SIP 対応であることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="7d462-159">Make sure that the LRSApp user account is SIP-enabled.</span></span>

  - <span data-ttu-id="7d462-160">それでも問題が解決されない場合は、D: Tracing lrsadminlogs から LRS システムの **Trace .log** ファイルを収集して、 \\ LRS の \\ \\ サポート担当者に送信します。</span><span class="sxs-lookup"><span data-stu-id="7d462-160">If you are still having issues, collect the **Trace.log** file in the LRS system from D:\\Tracing\\LRSAdminLogs\\, and then send it to your LRS support contact.</span></span>

<span data-ttu-id="7d462-161"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7d462-161"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

