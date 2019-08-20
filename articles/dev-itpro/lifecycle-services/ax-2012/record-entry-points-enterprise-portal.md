---
title: エンタープライズ ポータルのエントリ ポイントを記録
description: イベント トレースを使用して、Microsoft Dynamics AX のエンタープライズ ポータルに業務プロセス フローを記録することができます。 セキュリティ開発ツールに業務プロセス フローを表示することができます。
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: AX 2012
ms.custom: 74812
ms.assetid: 72a6964d-e8b6-4c3a-8b74-bd6550711f2a
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 2012 R3 CU8
ms.openlocfilehash: 4bbda83dfaa0af45f5f6b25c5498c5600c942145
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850511"
---
# <a name="record-entry-points-in-enterprise-portal"></a><span data-ttu-id="47f89-104">エンタープライズ ポータルのエントリ ポイントを記録</span><span class="sxs-lookup"><span data-stu-id="47f89-104">Record entry points in Enterprise Portal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="47f89-105">イベント トレースを使用して、Microsoft Dynamics AX のエンタープライズ ポータルに業務プロセス フローを記録することができます。</span><span class="sxs-lookup"><span data-stu-id="47f89-105">You can record business process flows in Enterprise Portal for Microsoft Dynamics AX by using event traces.</span></span> <span data-ttu-id="47f89-106">セキュリティ開発ツールに業務プロセス フローを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="47f89-106">You can then view the business process flows in the Security Development Tool.</span></span>

| <span data-ttu-id="47f89-107">**メモ**</span><span class="sxs-lookup"><span data-stu-id="47f89-107">**Note**</span></span>                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47f89-108">これは、予備的なプレリリース ドキュメントで、予告なしに変更される場合があります。</span><span class="sxs-lookup"><span data-stu-id="47f89-108">This is pre-release documentation of a preliminary nature and is subject to change at any time without notice.</span></span> <span data-ttu-id="47f89-109">ここで提供されている情報の正確さは保障されていません。</span><span class="sxs-lookup"><span data-stu-id="47f89-109">Microsoft cannot guarantee the accuracy of any information provided herein.</span></span> |

## <a name="collect-event-traces-for-enterprise-portal-entry-points-by-using-windows-performance-monitor"></a><span data-ttu-id="47f89-110">Windows パフォーマンス モニタを使用してエンタープライズ ポータルのエントリ ポイントのイベント トレースを収集する</span><span class="sxs-lookup"><span data-stu-id="47f89-110">Collect event traces for Enterprise Portal entry points by using Windows Performance Monitor</span></span>
1.  <span data-ttu-id="47f89-111">イベントのトレースを収集する、エンタープライズ ポータルのインスタンスを実行しているコンピューターで、Windows パフォーマンス モニターを開きます。</span><span class="sxs-lookup"><span data-stu-id="47f89-111">On a computer that is running the instance of Enterprise Portal that you want to collect event traces from, open Windows Performance Monitor.</span></span> <span data-ttu-id="47f89-112">ナビゲーション ウィンドウの**データ コレクター セット**で、**ユーザー定義**を右クリックし、**新規**を選択してから**データ コレクター セット**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="47f89-112">In the navigation pane, under **Data Collector Sets**, right-click **User Defined**, select **New**, and then click **Data Collector Set**.</span></span>
2.  <span data-ttu-id="47f89-113">新しいデータ コレクター セットの固有名を入力します。</span><span class="sxs-lookup"><span data-stu-id="47f89-113">Enter a unique name for the new data collector set.</span></span> <span data-ttu-id="47f89-114">**テンプレートから作成** を選択し、**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="47f89-114">Select **Create from a template**, and then click **Next.**</span></span>
3.  <span data-ttu-id="47f89-115">**参照**をクリックし、セキュリティ開発ツールと共にインストールされた EP **EntryPointTracingTemplate.xml** テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="47f89-115">Click **Browse**, and then select the EP **EntryPointTracingTemplate.xml** template that was installed together with the Security Development Tool.</span></span> <span data-ttu-id="47f89-116">**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="47f89-116">Click **Next**.</span></span>
4.  <span data-ttu-id="47f89-117">データを保存したいルート ディレクトリのアドレスを入力または**参照**をクリックしてディレクトリを検索します。</span><span class="sxs-lookup"><span data-stu-id="47f89-117">Enter the address of the root directory where you want to save the data, or click **Browse** to search for a directory.</span></span> <span data-ttu-id="47f89-118">**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="47f89-118">Click **Next**.</span></span>
5.  <span data-ttu-id="47f89-119">**完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="47f89-119">Click **Finish**.</span></span>
6.  <span data-ttu-id="47f89-120">新しいデータ コレクター セットを選択し、**開始** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="47f89-120">Select the new data collector set, and then click **Start**.</span></span>
7.  <span data-ttu-id="47f89-121">エンタープライズ ポータル サイトに移動し、ビジネス シナリオを実行します。</span><span class="sxs-lookup"><span data-stu-id="47f89-121">Navigate to the Enterprise Portal site, and execute your business scenario.</span></span>
8.  <span data-ttu-id="47f89-122">データ コレクター セットを停止します。</span><span class="sxs-lookup"><span data-stu-id="47f89-122">Stop the data collector set.</span></span>
9.  <span data-ttu-id="47f89-123">追跡ログを XML 形式に変換します。</span><span class="sxs-lookup"><span data-stu-id="47f89-123">Convert the trace log to XML format.</span></span>
    1.  <span data-ttu-id="47f89-124">**Windows イベント ビューアー**を開きます。</span><span class="sxs-lookup"><span data-stu-id="47f89-124">Open **Windows Event Viewer**.</span></span>
    2.  <span data-ttu-id="47f89-125">**アプリケーションとサービス ログ** ノードを右クリックし、**保存されたログを開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="47f89-125">Right-click the **Applications and Service Logs** node, and then select **Open Saved Log**.</span></span>
    3.  <span data-ttu-id="47f89-126">ステップ 4 で作成した出力ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="47f89-126">Select the output file that you created in step 4.</span></span> <span data-ttu-id="47f89-127">出力ファイルの拡張子は .etl です。</span><span class="sxs-lookup"><span data-stu-id="47f89-127">Output files have the .etl extension.</span></span>
    4.  <span data-ttu-id="47f89-128">メッセージが表示されたら、**はい** クリックして、イベント ログの新しいコピーを作成します。</span><span class="sxs-lookup"><span data-stu-id="47f89-128">When you are prompted, click **Yes** to create a new copy of the event log.</span></span>
    5.  <span data-ttu-id="47f89-129">ログの固有名を入力し、次に**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="47f89-129">Enter a unique name for the log, and then click **OK**.</span></span> <span data-ttu-id="47f89-130">ログは、**保存されたログ**ノードに表示されます。</span><span class="sxs-lookup"><span data-stu-id="47f89-130">The log is displayed in the **Saved Logs** node.</span></span>
    6.  <span data-ttu-id="47f89-131">保存されているログを右クリックし、**すべてのイベントに名前を付けて保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="47f89-131">Right-click the saved log, and then select **Save All Events As**.</span></span>
    7.  <span data-ttu-id="47f89-132">**ファイルの種類**フィールドで、**Xml (XML ファイル) (\*.xml)** を選択してからファイルの一意の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="47f89-132">In the **Save as type** field, select **Xml (XML File) (\*.xml)**, and then enter a unique name for the file.</span></span> <span data-ttu-id="47f89-133">表示情報を含める必要はありません。</span><span class="sxs-lookup"><span data-stu-id="47f89-133">You do not have to include display information.</span></span>

## <a name="load-the-trace-file"></a><span data-ttu-id="47f89-134">トレース ファイルの読み込み</span><span class="sxs-lookup"><span data-stu-id="47f89-134">Load the trace file</span></span>
1.  <span data-ttu-id="47f89-135">主要フォームのリボンで、**トレース ファイルの読み込み**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="47f89-135">On the ribbon of the main form, click **Load trace file**.</span></span>
2.  <span data-ttu-id="47f89-136">エンタープライズ ポータル イベントの追跡を使用して作成された .xml ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="47f89-136">Select the .xml file that was created by using the Enterprise Portal event traces.</span></span> <span data-ttu-id="47f89-137">新しいウィンドウが開き、記録されているすべてのエントリ ポイントを表示します。</span><span class="sxs-lookup"><span data-stu-id="47f89-137">A new window opens that displays all entry points that have been recorded.</span></span>

    | <span data-ttu-id="47f89-138">**ヒント**</span><span class="sxs-lookup"><span data-stu-id="47f89-138">**Tip**</span></span>                                                                                                                                                                                 |
    |-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="47f89-139">システム ユーザー ロール アクセス レベル列によってエントリ ポイントを並べ替え、システム ユーザー ロールのアクセス レベルが NoAccess 以外になっているすべてのエントリ ポイントを削除します。</span><span class="sxs-lookup"><span data-stu-id="47f89-139">Sort the entry points by the System user role access level column, and then remove all entry points for which the access level of the System User role is anything other than NoAccess.</span></span> |

3.  <span data-ttu-id="47f89-140">記録されたエントリ ポイントのアクセス レベルを更新するには、一覧で複数の行を選択し、**記録済みとしてマーク** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="47f89-140">To update the level of access for the recorded entry points, select multiple rows in the list, and then click **Mark as recorded**.</span></span> <span data-ttu-id="47f89-141">メイン フォームに戻り、エントリ ポイントは記録済みとしてマークされます。</span><span class="sxs-lookup"><span data-stu-id="47f89-141">You are returned to the main form, and the entry points are marked as recorded.</span></span> <span data-ttu-id="47f89-142">主要なフォームから、アクセス レベルを更新する**エントリ ポイントのアクセス許可を設定**機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="47f89-142">From the main form, you can use the **Set entry point permissio**ns function to update the access level.</span></span> <span data-ttu-id="47f89-143">終了したら、**エンタープライズ ポータルのトレース データ ウィンドウに移動する** をクリックして、エンタープライズ ポータルのエントリ ポイントのトレース データを表示するウィンドウに切り替えることができます。</span><span class="sxs-lookup"><span data-stu-id="47f89-143">When you have finished, you can switch back to the window that displays the trace data for the Enterprise Portal entry point by clicking **Go to the Enterprise Portal trace data window**.</span></span>





