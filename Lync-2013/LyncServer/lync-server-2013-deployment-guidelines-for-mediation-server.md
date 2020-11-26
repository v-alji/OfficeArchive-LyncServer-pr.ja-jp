---
title: 'Lync Server 2013: 仲介サーバー向けの展開ガイドライン'
description: 'Lync Server 2013: 仲介サーバーの展開ガイドライン。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment guidelines for Mediation Server
ms:assetid: 7cc22b87-18d9-45e6-8402-015abd20f2e5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398622(v=OCS.15)
ms:contentKeyID: 48184606
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8198431b24714666c9411029aecd12835014fef4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429686"
---
# <a name="deployment-guidelines-for-mediation-server-in-lync-server-2013"></a>Lync Server 2013 での仲介サーバーの展開ガイドライン

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**最終更新日:** 2012-10-12_

このトピックでは、仲介サーバーの展開に関する計画ガイドラインについて説明します。 これらのガイドラインを確認した後、計画ツールを使用して、展開する予定の最終的なトポロジがどのように表示されるかのモデルとして利用できる、可能な代替トポロジを作成して表示することをお勧めします。

<div>

## <a name="collocated-or-stand-alone-mediation-server"></a>併置またはスタンドアロンの仲介サーバーですか?

仲介サーバーは、既定では、Standard Edition サーバーまたはフロントエンドサーバーの中央サイトのフロントエンドプールにあります。 処理することができる公衆交換電話網 (PSTN) 通話の数およびプール内で必要なコンピューターの数は、以下に応じて異なります。

  - 仲介サーバープールが制御するゲートウェイピアの数

  - それらのゲートウェイを経由する高ボリューム トラフィックの期間

  - 仲介サーバーを使用していないメディアを含む通話の割合

計画するときは、メディアのバイパス用に構成されていない PSTN 通話と A/V 会議のメディア処理要件、およびサポートする必要がある時間帯を含む通話のシグナル操作を処理するために必要な処理について必ず考慮してください。 CPU が不足している場合は、スタンドアロンのプールサーバーを展開する必要があります。また、PSTN ゲートウェイ、IP Pbx、および SBCs は、1つのプール内の併置されている仲介サーバーによって制御されるサブセットと1つ以上のスタンドアロンプールでスタンドアロンの仲介サーバーによって制御されるサブセットに分割する必要があります。

次のように、仲介サーバーのプールを操作する適切な機能をサポートしていない PSTN ゲートウェイ、IP Pbx、またはセッション境界コントローラー (SBCs) を展開した場合は、1つの仲介サーバーで構成されるスタンドアロンプールに関連付ける必要があります。

  - プール内の仲介サーバー間でネットワークレイヤーのドメインネームシステム (DNS) 負荷分散を実行する (または、プール内のすべての仲介サーバーに対して一律にトラフィックをルーティングする)

  - プール内の任意の仲介サーバーからのトラフィックを受け入れる

Microsoft Lync Server 2013 の計画ツールを使用すると、フロントエンドプールで仲介サーバーを検索して負荷を処理できるかどうかを評価できます。 環境がこれらの要件を満たしていない場合は、スタンドアロンの仲介サーバープールを展開する必要があります。

</div>

<div>

## <a name="central-site-and-branch-site-considerations"></a>中央サイトとブランチ サイトに関する考慮事項

セントラルサイトの仲介サーバーを使用して、ブランチサイトの IP-PBXs または PSTN ゲートウェイの呼び出しをルーティングすることができます。 ただし、SIP trunks を展開する場合は、各トランクが終了するサイトに仲介サーバーを展開する必要があります。 ブランチサイトで、IP PBX または PSTN ゲートウェイのセントラルサイトルートに仲介サーバーがある場合は、メディアバイパスの使用は必要ありません。 ただし、メディアのバイパスを有効にできる場合は、メディアパスの遅延を減らすことができます。その結果、メディアパスはシグナリングパスの追跡には必要なくなったため、メディアの品質が向上します。 メディア バイパスにより、プールの処理負荷も軽減することができます。

<div>


> [!NOTE]  
> メディア バイパスは、すべての PSTN ゲートウェイ、IP-PBX、および SBC と相互運用できるとは限りません。 マイクロソフトでは、認定パートナーの PSTN ゲートウェイと SBC でテストを行い、Cisco IP-PBX でも一定のテストを行いました。 メディアのバイパスは、統合された通信のオープンな相互運用性プログラム– Lync Server at の製品とバージョンでのみサポートされ <A href="https://go.microsoft.com/fwlink/p/?linkid=268730">https://go.microsoft.com/fwlink/p/?LinkId=268730</A> ます。



</div>

ブランチサイトの回復力が必要な場合は、Survivable Branch Appliance またはフロントエンドサーバー、仲介サーバー、ゲートウェイをブランチサイトに展開する必要があります。 (ブランチサイトの回復力を前提として、サイトでのプレゼンスと会議の弾力性がないことを前提としています)。ボイスのブランチサイトの計画に関するガイダンスについては、「 [Lync Server 2013 でのブランチサイトの音声回復の計画](lync-server-2013-planning-for-branch-site-voice-resiliency.md)」を参照してください。

Ip pbx との相互操作については、ip pbx で、複数の初期ダイアログと RFC 3960 の相互作用との早いメディア操作が適切にサポートされていない場合、IP PBX から Lync エンドポイントへの着信通話について、応答メッセージの最初のいくつかの単語をクリッピングすることができます。 この動作は、ルーティングを完了するためにより多くの時間が必要となるため、セントラルサイトの仲介サーバーが、ブランチサイトで終了する IP PBX の呼び出しをルーティングしている場合、より重大な可能性があります。 この問題が発生した場合は、最初のいくつかの単語のクリッピングを減らす唯一の方法は、ブランチサイトに仲介サーバーを展開することだけです。

最後に、セントラルサイトに TDM PBX がある場合、または、IP PBX で PSTN ゲートウェイを使用する必要がない場合は、仲介サーバーと PBX を接続する通話ルートにゲートウェイを展開する必要があります。

<div>


> [!NOTE]  
> スタンドアロン仲介サーバーのメディア パフォーマンスを向上させるには、これらのサーバーのネットワーク アダプターの Receive-side Scaling (RSS) を有効にする必要があります。 RSS は、着信パケットがサーバーの複数のプロセッサによって平行して処理されるのを可能にします。 詳細については、の「Windows Server の受信側スケーリングの拡張機能」を参照してください <A href="https://go.microsoft.com/fwlink/p/?linkid=268731">https://go.microsoft.com/fwlink/p/?LinkId=268731</A> 。 RSS を有効にする方法の詳細については、ネットワーク アダプターのドキュメントを参照してください。



</div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

