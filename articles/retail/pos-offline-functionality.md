---
title: オフライン販売時点管理 (POS) の機能
description: この記事では、小売サーバーが利用できない場合にチャンネルのデータベースからオフライン データベースに POS デバイスが自動的に切り替わる、Retail Modern POS のオフライン モードについて説明します。 また、この記事ではオフライン モードの一般的な設定情報も含まれ、オフライン データベースとチャンネルのデータベース間で発生するデータ同期についても説明します。
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTerminalTable
audience: IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 27041
ms.assetid: 20b51874-8912-40cf-9296-864df707315a
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c31aa7ddffa26618ffeb34e2f30334e5b8052867
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537089"
---
# <a name="offline-point-of-sale-pos-functionality"></a><span data-ttu-id="72d6b-104">オフライン販売時点管理 (POS) の機能</span><span class="sxs-lookup"><span data-stu-id="72d6b-104">Offline point of sale (POS) functionality</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="72d6b-105">この記事では、小売サーバーが利用できない場合にチャンネルのデータベースからオフライン データベースに POS デバイスが自動的に切り替わる、Retail Modern POS のオフライン モードについて説明します。</span><span class="sxs-lookup"><span data-stu-id="72d6b-105">This article provides information about offline mode for Retail Modern POS, in which POS devices automatically switch from the channel database to the offline database if the retail server is unavailable.</span></span> <span data-ttu-id="72d6b-106">また、この記事ではオフライン モードの一般的な設定情報も含まれ、オフライン データベースとチャンネルのデータベース間で発生するデータ同期についても説明します。</span><span class="sxs-lookup"><span data-stu-id="72d6b-106">This article also includes general setup information for offline mode and explains the data synchronization that occurs between the offline database and the channel database.</span></span>

## <a name="overview"></a><span data-ttu-id="72d6b-107">概要</span><span class="sxs-lookup"><span data-stu-id="72d6b-107">Overview</span></span>

<span data-ttu-id="72d6b-108">Retail Modern POS では、小売サーバーが利用できないときはいつでも 販売時点管理 (POS) デバイスがオフライン モードになります。</span><span class="sxs-lookup"><span data-stu-id="72d6b-108">In Retail Modern POS, a point of sale (POS) device goes into offline mode whenever the retail server is unavailable.</span></span> <span data-ttu-id="72d6b-109">したがって、小売サーバーとの接続が失われると、Retail Modern POS はオフライン データベースに自動的に切り替わります。</span><span class="sxs-lookup"><span data-stu-id="72d6b-109">Therefore, if the connection with the retail server is lost, Retail Modern POS automatically switches to the offline database.</span></span> <span data-ttu-id="72d6b-110">販売トランザクション中に、オフライン プロファイルでコンフィギュレーションされたタイムアウトの間隔内でデータの要求が成功しなかった場合、Retail Modern POS は自動的にオフライン データベースに切り替わり、販売トランザクションを続行します。</span><span class="sxs-lookup"><span data-stu-id="72d6b-110">During a sales transaction, if a data request doesn't succeed within the time-out interval that is configured in the offline profile, Retail Modern POS automatically switches to the offline database and continues the sales transaction.</span></span> <span data-ttu-id="72d6b-111">POS デバイスがオフライン モードの間に、Retail Modern POS はオフライン プロファイルでコンフィギュレーションされた再接続試行間隔の後に再接続を試みます。</span><span class="sxs-lookup"><span data-stu-id="72d6b-111">While POS device is in offline mode, Retail Modern POS tries to reconnect to the retail server after the reconnection attempt interval that is configured in the offline profile.</span></span> <span data-ttu-id="72d6b-112">この再接続試行は、トランザクションの先頭でのみ実行されます。</span><span class="sxs-lookup"><span data-stu-id="72d6b-112">This reconnection attempt occurs only at the beginning of a transaction.</span></span>

### <a name="determining-the-connection-mode-of-retail-modern-pos"></a><span data-ttu-id="72d6b-113">Retail Modern POS の接続モードを決定する</span><span class="sxs-lookup"><span data-stu-id="72d6b-113">Determining the connection mode of Retail Modern POS</span></span>

<span data-ttu-id="72d6b-114">Retail Modern POS のステータス ヘッダーは現在の接続ステータスを表示し、**接続ステータス** ウィンドウはオフライン データベースと同期する最後の試行のステータスを表示します。</span><span class="sxs-lookup"><span data-stu-id="72d6b-114">The status header in Retail Modern POS indicates the current connection status, and the **Connection status** window shows the status of the last attempt to sync with the offline database.</span></span>

<span data-ttu-id="72d6b-115">[![接続ステータス](./media/status.png)](./media/status.png)</span><span class="sxs-lookup"><span data-stu-id="72d6b-115">[![Connection status](./media/status.png)](./media/status.png)</span></span>

### <a name="creating-a-button-to-manually-switch-between-online-and-offline-modes"></a><span data-ttu-id="72d6b-116">手動でオンラインとオフライン モードを切り替えるためのボタンを作成</span><span class="sxs-lookup"><span data-stu-id="72d6b-116">Creating a button to manually switch between online and offline modes</span></span>

<span data-ttu-id="72d6b-117">Retail Modern POS にオンラインとオフライン モードを手動で切り替えるボタンを追加できます。</span><span class="sxs-lookup"><span data-stu-id="72d6b-117">You can add a button to Retail Modern POS to manually switch between online and offline modes.</span></span> <span data-ttu-id="72d6b-118">POS 操作 **917 – データベース接続ステータス**のボタンを作成します。</span><span class="sxs-lookup"><span data-stu-id="72d6b-118">Create a button for POS operation **917 – Database connection status**.</span></span> <span data-ttu-id="72d6b-119">このボタンの名前は、Retail Modern POS が小売サーバーに接続されている場合は**接続解除**となり、接続解除されている場合は**接続**となります。</span><span class="sxs-lookup"><span data-stu-id="72d6b-119">The name of this button is **Disconnect** when Retail Modern POS is connected to the retail server and **Connect** when it is disconnected.</span></span> <span data-ttu-id="72d6b-120">このボタンは接続の表示、小売サーバーとの接続解除および接続に使用できます。</span><span class="sxs-lookup"><span data-stu-id="72d6b-120">You can use this button to view the connection, and to disconnect from the retail server or connect to it.</span></span>

<span data-ttu-id="72d6b-121">[![Retail Modern POS の接続解除ボタン](./media/details-1024x537.png)](./media/details.png)</span><span class="sxs-lookup"><span data-stu-id="72d6b-121">[![Disconnect button in Retail Modern POS](./media/details-1024x537.png)](./media/details.png)</span></span>

## <a name="setup"></a><span data-ttu-id="72d6b-122">セットアップ</span><span class="sxs-lookup"><span data-stu-id="72d6b-122">Setup</span></span>

<span data-ttu-id="72d6b-123">POS のデバイス (登録) のオフライン サポートを有効にするには、**登録** ページで、**オフラインのサポート** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="72d6b-123">To enable offline support for a POS device (register), set the **Support offline** option to **Yes** on the **Register** page.</span></span> <span data-ttu-id="72d6b-124">新しいチャンネル データベース エンティティが作成され、店舗のチャンネル データ グループに追加されます。</span><span class="sxs-lookup"><span data-stu-id="72d6b-124">A new channel database entity is created and added to the store's channel data group.</span></span> <span data-ttu-id="72d6b-125">その後、オフライン データベースのデータ パッケージを生成するためにすべての配送スケジュールを実行します。</span><span class="sxs-lookup"><span data-stu-id="72d6b-125">Then run all the required distribution schedules to generate the data packages for the offline database.</span></span> <span data-ttu-id="72d6b-126">次に、Retail Modern POS のオフライン バージョンをインストールします。</span><span class="sxs-lookup"><span data-stu-id="72d6b-126">Next, install the offline version of Retail Modern POS.</span></span> <span data-ttu-id="72d6b-127">インストール プロセスでは、オフライン データベースが作成されます。</span><span class="sxs-lookup"><span data-stu-id="72d6b-127">The installation process creates the offline database.</span></span> <span data-ttu-id="72d6b-128">さらに、必要な場合は、Microsoft SQL Server 2014 Express をインストールします。</span><span class="sxs-lookup"><span data-stu-id="72d6b-128">Additionally, install Microsoft SQL Server 2014 Express if it is required.</span></span> <span data-ttu-id="72d6b-129">Retail Modern POS への最初のサインイン後にオフライン データの同期が開始されます。</span><span class="sxs-lookup"><span data-stu-id="72d6b-129">Offline data synchronization starts after the first sign-in to Retail Modern POS.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="72d6b-130">データ同期</span><span class="sxs-lookup"><span data-stu-id="72d6b-130">Data synchronization</span></span>

<span data-ttu-id="72d6b-131">小売用スケジューラはオフライン データベースにマスター データを送信するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="72d6b-131">The Retail scheduler is used to send master data to the offline database.</span></span> <span data-ttu-id="72d6b-132">既定では、配送スケジュールの実行時に、データの変更がチャンネルのデータベースとオフライン データベースの両方に送信されます。</span><span class="sxs-lookup"><span data-stu-id="72d6b-132">By default, when a distribution schedule is run, data changes are sent to both the channel database and the offline database.</span></span> <span data-ttu-id="72d6b-133">Retail Modern POS には、使用可能なすべてのデータ パッケージをダウンロードし、オフライン データベースに挿入する async sync ライブラリが含まれます。</span><span class="sxs-lookup"><span data-stu-id="72d6b-133">Retail Modern POS includes the async sync library, which downloads any available data packages and inserts them into the offline database.</span></span> <span data-ttu-id="72d6b-134">トランザクションがオフラインで作成された場合、Retail Modern POS はそれらをチャンネル データベースに挿入するためにアップロードします。</span><span class="sxs-lookup"><span data-stu-id="72d6b-134">If any transactions are created offline, Retail Modern POS uploads them to the retail server, so that they can be inserted into the channel database.</span></span> <span data-ttu-id="72d6b-135">オフラインのデータ同期は、Retail Modern POS の実行時にのみ実行できます。</span><span class="sxs-lookup"><span data-stu-id="72d6b-135">Offline data synchronization can occur only if Retail Modern POS is running.</span></span>

<span data-ttu-id="72d6b-136">[![オフライン同期](./media/offline-sync-1024x521.png)](./media/offline-sync.png)</span><span class="sxs-lookup"><span data-stu-id="72d6b-136">[![Offline synchronization](./media/offline-sync-1024x521.png)](./media/offline-sync.png)</span></span>
