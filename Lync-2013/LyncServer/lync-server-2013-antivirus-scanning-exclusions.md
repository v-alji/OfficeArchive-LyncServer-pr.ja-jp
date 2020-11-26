---
title: 'Lync Server 2013: ウイルス スキャン除外範囲'
description: 'Lync Server 2013: ウイルス対策スキャンの除外。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Antivirus scanning exclusions for Lync Server 2013
ms:assetid: 71e1f1cc-2d16-4111-9864-9276bf24dfe0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn440138(v=OCS.15)
ms:contentKeyID: 57793042
ms.date: 11/03/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 20c395f529cad91993d003efdeb231bd66f4b9bc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440662"
---
# <a name="antivirus-scanning-exclusions-for-lync-server-2013"></a>Lync Server 2013 用のウイルス スキャン除外範囲

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2015-11-02_

ウイルス対策スキャナーが Lync Server 2013 の動作を妨害しないようにするには、ウイルススキャンを実行している Lync Server 2013 サーバーまたはサーバーの役割ごとに、特定のプロセスとディレクトリを除外する必要があります。 除外が必要なプロセスとディレクトリを以下に示します。

<div>


> [!NOTE]  
> 次に示すフォルダーとファイルの場所は、Lync Server 2013 の既定の場所です。 既定の設定を使用しなかったすべての場所については、ここに示す既定の場所の代わりに、組織で指定した場所を除外してください。



</div>

<div>


> [!IMPORTANT]  
> 一部のウイルス対策プログラムでは、除外リストに相対パスでなく絶対パスが必要な場合があります。



</div>

  - Lync Server 2013 のプロセス:
    
      - ABServer.exe
    
      - AcpMcuSvc.exe
    
      - ASMCUSvc.exe
    
      - AVMCUSvc.exe
    
      - ChannelService.exe
    
      - ClsAgent.exe
    
      - ComplianceService.exe
    
      - DataMCUSvc.exe
    
      - DataProxy.exe
    
      - FileTransferAgent.exe
    
      - IMMCUSvc.exe
    
      - LysSvc.exe
    
      - MasterReplicatorAgent.exe
    
      - MediaRelaySvc.exe
    
      - MediationServerSvc.exe
    
      - MRASSvc.exe
    
      - OcsAppServerHost.exe
    
      - ReplicaReplicatorAgent.exe
    
      - ReplicationApp.exe
    
      - RtcHost.exe
    
      - RTCSrv.exe
    
      - XmppProxy.exe
    
      - XmppTGW.exe

  - Windows Fabric Host Service のプロセス:
    
      - Fabric.exe
    
      - FabricDCA.exe
    
      - FabricHost.exe

  - IIS のプロセス:
    
      - % systemroot% \\ system32 \\ inetsrv \\w3wp.exe
    
      - % systemroot% \\ SysWOW64 \\ inetsrv \\w3wp.exe

  - SQL Server バックエンドのプロセス:
    
      - % ProgramFiles% \\ MICROSOFT SQL Server \\ MSSQL11。MSSQLSERVER \\ MSSQL \\ Binn \\SQLServr.exe
    
      - % ProgramFiles% \\ MICROSOFT SQL Server \\ MSRS11。MSSQLSERVER \\ Reporting Services の \\ ReportServer \\ Bin \\ReportingServicesService.exe
    
      - % ProgramFiles% \\ MICROSOFT SQL Server \\ MSAS11。MSSQLSERVER \\ OLAP \\ Bin \\MSMDSrv.exe

  - SQL Server フロントエンドのプロセス:
    
      - % ProgramFiles% \\ MICROSOFT SQL Server \\ MSSQL11。LYNCLOCAL \\ MSSQL \\ Binn \\SQLServr.exe
    
      - % ProgramFiles% \\ MICROSOFT SQL Server \\ MSSQL11。RTCLOCAL \\ MSSQL \\ Binn \\SQLServr.exe

  - ディレクトリとファイル:
    
      - % systemroot% \\ System32 \\ ログのログ
    
      - % systemroot% \\ SysWow64 \\ ログ
    
      - % systemroot% \\ Microsoft.NET \\ assembly \\ GAC \_ MSIL
    
      - % programfiles% \\ Microsoft Lync Server 2013
    
      - % programfiles% \\ 共通ファイル \\ Microsoft Lync Server 2013 \\ ウォッチャーノード
    
      - % programfiles% ( \\ 共通ファイル \\ Microsoft Lync Server 2013)
    
      - % SystemDrive% \\ RtcReplicaRoot
    
      - ファイル共有ストア (トポロジ ビルダーで指定)。 ファイル ストアはトポロジ ビルダーで指定されています。
    
      - SQL Server のデータおよびログ ファイル (バックエンド データベース、ユーザー ストア、アーカイブ ストア、監視ストア、およびアプリケーション ストア用のものを含みます)。 データベースとログ ファイルは、トポロジ ビルダーで指定できます。 既定の名前など、各データベースのデータファイルとログファイルの詳細については、「 [SQL server のデータと、Lync Server 2013 用のログファイルの配置](lync-server-2013-sql-server-data-and-log-file-placement.md) 」を参照してください。
    
      - SQL Server のデータファイルとログファイル (フロントエンドデータベース、Lync ストア、および RtcDatabase store のものを含む)。 通常、% localdrive% csdata の下にあり \\ ます。

</div>

<span> </span>

</div>

</div>

</div>

