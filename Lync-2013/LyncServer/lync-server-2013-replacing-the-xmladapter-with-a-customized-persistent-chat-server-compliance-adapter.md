---
title: 'Lync Server 2013: カスタマイズされた常設チャット Server コンプライアンスアダプターを使用した Xml アダプターの置き換え'
description: 'Lync Server 2013: カスタマイズされた常設チャット Server コンプライアンスアダプターで Xml アダプターを置き換えます。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Replacing the XmlAdapter with a customized Persistent Chat Server Compliance adapter
ms:assetid: 2cb70db2-663f-40a6-abcf-89ea7d4a8b65
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ680106(v=OCS.15)
ms:contentKeyID: 49558152
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3a90b4df7df42ffdc6c55e9b551b0eb53d07ab1c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/24/2020
ms.locfileid: "49398978"
---
# <a name="replacing-the-xmladapter-with-a-customized-persistent-chat-server-compliance-adapter-in-lync-server-2013"></a><span data-ttu-id="134cf-103">Lync Server 2013 での、カスタマイズされた常設チャットサーバーのコンプライアンスアダプターを使用した Xml アダプターの置き換え</span><span class="sxs-lookup"><span data-stu-id="134cf-103">Replacing the XmlAdapter with a customized Persistent Chat Server Compliance adapter in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="134cf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="134cf-104">

<span> </span></span></span>

<span data-ttu-id="134cf-105">_**最終更新日:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="134cf-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="134cf-106">常設チャットサーバーと共にインストールされている XmlAdapter を使う代わりに、カスタムアダプターを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="134cf-106">You can write a custom adapter instead of using the XmlAdapter that is installed with Persistent Chat Server.</span></span> <span data-ttu-id="134cf-107">記述するには、**IComplianceAdapter** インターフェイスを実装するパブリック クラスを含む .NET Framework アセンブリを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="134cf-107">To accomplish this, you must provide a .NET Framework assembly that contains a public class that implements the **IComplianceAdapter** interface.</span></span> <span data-ttu-id="134cf-108">このアセンブリは、常設チャットサーバープールの各サーバーの常設チャットサーバーのインストールフォルダーに配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="134cf-108">You must place this assembly in the Persistent Chat Server installation folder of each server in your Persistent Chat Server pool.</span></span> <span data-ttu-id="134cf-109">任意のコンプライアンス サーバーからアダプターにコンプライアンス データを提供できますが、コンプライアンス サーバーからアダプターの複数のインスタンスに対して重複するコンプライアンス データを提供することはできません。</span><span class="sxs-lookup"><span data-stu-id="134cf-109">Any one of the Compliance servers can provide compliance data to your adapter, but the compliance servers will not provide duplicate compliance data to multiple instances of your adapter.</span></span>

<div>

## <a name="implementing-the-icomplianceadapter-interface"></a><span data-ttu-id="134cf-110">IComplianceAdapter インターフェイスの実装</span><span class="sxs-lookup"><span data-stu-id="134cf-110">Implementing the IComplianceAdapter interface</span></span>

<span data-ttu-id="134cf-111">インターフェイスは、名前空間の Compliance.dll アセンブリで定義され `Microsoft.Rtc.Internal.Chat.Server.Compliance` ます。</span><span class="sxs-lookup"><span data-stu-id="134cf-111">The interface is defined in the Compliance.dll assembly in the namespace `Microsoft.Rtc.Internal.Chat.Server.Compliance`.</span></span> <span data-ttu-id="134cf-112">このインターフェイスには、カスタム アダプターが実装する必要のある 2 つのメソッドが定義されています。</span><span class="sxs-lookup"><span data-stu-id="134cf-112">The interface defines two methods that your custom adapter must implement.</span></span>

    void SetConfig(AdapterConfig config)

<span data-ttu-id="134cf-113">常設チャットのコンプライアンスサーバーは、アダプターが最初に読み込まれたときにこのメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="134cf-113">The Persistent Chat Compliance server will call this method when the adapter first loads.</span></span> <span data-ttu-id="134cf-114">には、 `AdapterConfig` コンプライアンスアダプターに関連する常設チャットのコンプライアンス構成が含まれています。</span><span class="sxs-lookup"><span data-stu-id="134cf-114">The `AdapterConfig` contains the Persistent Chat compliance configuration that is relevant to the compliance adapter.</span></span>

    void Translate(ConversationCollection conversations)

<span data-ttu-id="134cf-115">常設チャットのコンプライアンスサーバーは、翻訳する新しいデータがある限り、定期的な間隔でこのメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="134cf-115">The Persistent Chat Compliance server calls this method at periodic intervals as long as there is new data to translate.</span></span> <span data-ttu-id="134cf-116">この時間間隔は、 `RunInterval` 常設チャットのコンプライアンス構成で設定された as と同じです。</span><span class="sxs-lookup"><span data-stu-id="134cf-116">This time interval is equal to the `RunInterval` as set in the Persistent Chat Compliance configuration.</span></span>

<span data-ttu-id="134cf-117">には、 `ConversationCollection` このメソッドが最後に呼び出されたときから収集されたスレッド情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="134cf-117">The `ConversationCollection` contains the conversation information that was collected from the last time this method was called.</span></span>

<span data-ttu-id="134cf-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="134cf-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

