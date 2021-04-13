---
title: エンタープライズ ポータルのエントリ ポイントを記録
description: イベント トレースを使用して、Microsoft Dynamics AX のエンタープライズ ポータルに業務プロセス フローを記録し、フローを表示することができます。
author: kfend
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 74812
ms.assetid: 72a6964d-e8b6-4c3a-8b74-bd6550711f2a
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 2012 R3 CU8
ms.openlocfilehash: bcff88153cb77a652d4b9f3e33fe55be16788d26
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744773"
---
# <a name="record-entry-points-in-enterprise-portal"></a><span data-ttu-id="c1852-103">エンタープライズ ポータルのエントリ ポイントを記録</span><span class="sxs-lookup"><span data-stu-id="c1852-103">Record entry points in Enterprise Portal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c1852-104">イベント トレースを使用して、Microsoft Dynamics AX のエンタープライズ ポータルに業務プロセス フローを記録することができます。</span><span class="sxs-lookup"><span data-stu-id="c1852-104">You can record business process flows in Enterprise Portal for Microsoft Dynamics AX by using event traces.</span></span> <span data-ttu-id="c1852-105">セキュリティ開発ツールに業務プロセス フローを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="c1852-105">You can then view the business process flows in the Security Development Tool.</span></span>

| <span data-ttu-id="c1852-106">**メモ**</span><span class="sxs-lookup"><span data-stu-id="c1852-106">**Note**</span></span>                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1852-107">これは、予備的なプレリリース ドキュメントで、予告なしに変更される場合があります。</span><span class="sxs-lookup"><span data-stu-id="c1852-107">This is pre-release documentation of a preliminary nature and is subject to change at any time without notice.</span></span> <span data-ttu-id="c1852-108">ここで提供されている情報の正確さは保障されていません。</span><span class="sxs-lookup"><span data-stu-id="c1852-108">Microsoft cannot guarantee the accuracy of any information provided herein.</span></span> |

## <a name="collect-event-traces-for-enterprise-portal-entry-points-by-using-windows-performance-monitor"></a><span data-ttu-id="c1852-109">Windows パフォーマンス モニタを使用してエンタープライズ ポータルのエントリ ポイントのイベント トレースを収集する</span><span class="sxs-lookup"><span data-stu-id="c1852-109">Collect event traces for Enterprise Portal entry points by using Windows Performance Monitor</span></span>
1.  <span data-ttu-id="c1852-110">イベントのトレースを収集する、エンタープライズ ポータルのインスタンスを実行しているコンピューターで、Windows パフォーマンス モニターを開きます。</span><span class="sxs-lookup"><span data-stu-id="c1852-110">On a computer that is running the instance of Enterprise Portal that you want to collect event traces from, open Windows Performance Monitor.</span></span> <span data-ttu-id="c1852-111">ナビゲーション ウィンドウの **データ コレクター セット** で、**ユーザー定義** を右クリックし、**新規** を選択してから **データ コレクター セット** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c1852-111">In the navigation pane, under **Data Collector Sets**, right-click **User Defined**, select **New**, and then click **Data Collector Set**.</span></span>
2.  <span data-ttu-id="c1852-112">新しいデータ コレクター セットの固有名を入力します。</span><span class="sxs-lookup"><span data-stu-id="c1852-112">Enter a unique name for the new data collector set.</span></span> <span data-ttu-id="c1852-113">**テンプレートから作成** を選択し、**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c1852-113">Select **Create from a template**, and then click **Next.**</span></span>
3.  <span data-ttu-id="c1852-114">**参照** をクリックし、セキュリティ開発ツールと共にインストールされた EP **EntryPointTracingTemplate.xml** テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="c1852-114">Click **Browse**, and then select the EP **EntryPointTracingTemplate.xml** template that was installed together with the Security Development Tool.</span></span> <span data-ttu-id="c1852-115">**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c1852-115">Click **Next**.</span></span>
4.  <span data-ttu-id="c1852-116">データを保存したいルート ディレクトリのアドレスを入力または **参照** をクリックしてディレクトリを検索します。</span><span class="sxs-lookup"><span data-stu-id="c1852-116">Enter the address of the root directory where you want to save the data, or click **Browse** to search for a directory.</span></span> <span data-ttu-id="c1852-117">**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c1852-117">Click **Next**.</span></span>
5.  <span data-ttu-id="c1852-118">**完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c1852-118">Click **Finish**.</span></span>
6.  <span data-ttu-id="c1852-119">新しいデータ コレクター セットを選択し、**開始** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c1852-119">Select the new data collector set, and then click **Start**.</span></span>
7.  <span data-ttu-id="c1852-120">エンタープライズ ポータル サイトに移動し、ビジネス シナリオを実行します。</span><span class="sxs-lookup"><span data-stu-id="c1852-120">Navigate to the Enterprise Portal site, and execute your business scenario.</span></span>
8.  <span data-ttu-id="c1852-121">データ コレクター セットを停止します。</span><span class="sxs-lookup"><span data-stu-id="c1852-121">Stop the data collector set.</span></span>
9.  <span data-ttu-id="c1852-122">追跡ログを XML 形式に変換します。</span><span class="sxs-lookup"><span data-stu-id="c1852-122">Convert the trace log to XML format.</span></span>
    1.  <span data-ttu-id="c1852-123">**Windows イベント ビューアー** を開きます。</span><span class="sxs-lookup"><span data-stu-id="c1852-123">Open **Windows Event Viewer**.</span></span>
    2.  <span data-ttu-id="c1852-124">**アプリケーションとサービス ログ** ノードを右クリックし、**保存されたログを開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c1852-124">Right-click the **Applications and Service Logs** node, and then select **Open Saved Log**.</span></span>
    3.  <span data-ttu-id="c1852-125">ステップ 4 で作成した出力ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="c1852-125">Select the output file that you created in step 4.</span></span> <span data-ttu-id="c1852-126">出力ファイルの拡張子は .etl です。</span><span class="sxs-lookup"><span data-stu-id="c1852-126">Output files have the .etl extension.</span></span>
    4.  <span data-ttu-id="c1852-127">メッセージが表示されたら、**はい** クリックして、イベント ログの新しいコピーを作成します。</span><span class="sxs-lookup"><span data-stu-id="c1852-127">When you are prompted, click **Yes** to create a new copy of the event log.</span></span>
    5.  <span data-ttu-id="c1852-128">ログの固有名を入力し、次に **OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c1852-128">Enter a unique name for the log, and then click **OK**.</span></span> <span data-ttu-id="c1852-129">ログは、**保存されたログ** ノードに表示されます。</span><span class="sxs-lookup"><span data-stu-id="c1852-129">The log is displayed in the **Saved Logs** node.</span></span>
    6.  <span data-ttu-id="c1852-130">保存されているログを右クリックし、**すべてのイベントに名前を付けて保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c1852-130">Right-click the saved log, and then select **Save All Events As**.</span></span>
    7.  <span data-ttu-id="c1852-131">**ファイルの種類** フィールドで、**Xml (XML ファイル) (\*.xml)** を選択してからファイルの一意の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="c1852-131">In the **Save as type** field, select **Xml (XML File) (\*.xml)**, and then enter a unique name for the file.</span></span> <span data-ttu-id="c1852-132">表示情報を含める必要はありません。</span><span class="sxs-lookup"><span data-stu-id="c1852-132">You do not have to include display information.</span></span>

## <a name="load-the-trace-file"></a><span data-ttu-id="c1852-133">トレース ファイルの読み込み</span><span class="sxs-lookup"><span data-stu-id="c1852-133">Load the trace file</span></span>
1.  <span data-ttu-id="c1852-134">主要フォームのリボンで、**トレース ファイルの読み込み** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c1852-134">On the ribbon of the main form, click **Load trace file**.</span></span>
2.  <span data-ttu-id="c1852-135">エンタープライズ ポータル イベントの追跡を使用して作成された .xml ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="c1852-135">Select the .xml file that was created by using the Enterprise Portal event traces.</span></span> <span data-ttu-id="c1852-136">新しいウィンドウが開き、記録されているすべてのエントリ ポイントを表示します。</span><span class="sxs-lookup"><span data-stu-id="c1852-136">A new window opens that displays all entry points that have been recorded.</span></span>

    | <span data-ttu-id="c1852-137">**ヒント**</span><span class="sxs-lookup"><span data-stu-id="c1852-137">**Tip**</span></span>                                                                                                                                                                                 |
    |-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="c1852-138">システム ユーザー ロール アクセス レベル列によってエントリ ポイントを並べ替え、システム ユーザー ロールのアクセス レベルが NoAccess 以外になっているすべてのエントリ ポイントを削除します。</span><span class="sxs-lookup"><span data-stu-id="c1852-138">Sort the entry points by the System user role access level column, and then remove all entry points for which the access level of the System User role is anything other than NoAccess.</span></span> |

3.  <span data-ttu-id="c1852-139">記録されたエントリ ポイントのアクセス レベルを更新するには、一覧で複数の行を選択し、**記録済みとしてマーク** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c1852-139">To update the level of access for the recorded entry points, select multiple rows in the list, and then click **Mark as recorded**.</span></span> <span data-ttu-id="c1852-140">メイン フォームに戻り、エントリ ポイントは記録済みとしてマークされます。</span><span class="sxs-lookup"><span data-stu-id="c1852-140">You are returned to the main form, and the entry points are marked as recorded.</span></span> <span data-ttu-id="c1852-141">主要なフォームから、アクセス レベルを更新する **エントリ ポイントのアクセス許可を設定** 機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="c1852-141">From the main form, you can use the **Set entry point permissio** ns function to update the access level.</span></span> <span data-ttu-id="c1852-142">終了したら、**エンタープライズ ポータルのトレース データ ウィンドウに移動する** をクリックして、エンタープライズ ポータルのエントリ ポイントのトレース データを表示するウィンドウに切り替えることができます。</span><span class="sxs-lookup"><span data-stu-id="c1852-142">When you have finished, you can switch back to the window that displays the trace data for the Enterprise Portal entry point by clicking **Go to the Enterprise Portal trace data window**.</span></span>







[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]