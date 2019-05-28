---
title: 作成から開始までのバッチ オーダーのライフサイクル
description: この手順では、バッチ オーダーのライフ サイクルの最初の部分を説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdBOM, PmfProdCoBy, ProdParmCostEstimation, ProdCalcTrans, ProdParmRelease, ProdSchedule, ProdRouteJob, ProdParmStartUp, ProdJournalTransBOM, ProdJournalTransRoute
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6484c1954ff4cc600938adb07b5384f1edce8bf7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545905"
---
# <a name="batch-order-lifecycle-from-create-to-start"></a>作成から開始までのバッチ オーダーのライフサイクル

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順では、バッチ オーダーのライフ サイクルの最初の部分を説明します。

作成、原価見積、超過生産ジョブ スケジュールからバッチ オーダーの実際の開始までです。



この手順の作成に使用するデモ データの会社は USMF です。 



別のデータセットの手順を実行する前提条件は、有効なフォーミュラおよび工順バージョンを含むリリース済製品です。


## <a name="create-a-batch-order"></a>バッチ オーダーの作成
1. [すべての製造オーダー] に移動します。
2. [新しいバッチ オーダー] をクリックします。
3. [品目番号] フィールドで、値を入力または選択します。
4. [作成] をクリックします。
5. [クイック フィルター] を使用して、値が「b」である [生産] フィールドをフィルター処理します。

## <a name="view-production-formula-and-expected-co-products"></a>生産フォーミュラおよび予想される連産品の表示
1. アクション ウィンドウで、[製造オーダー] をクリックします。
2. [式] をクリックします。
3. ページを閉じます。
4. [連産品 (複数)] をクリックします。
5. ページを閉じます。

## <a name="estimate-the-batch-order"></a>バッチ オーダーの見積
1. [見積] をクリックします。
2. [OK] をクリックします。
3. [アクション] ペインで [原価の管理] をクリックします。
4. [計算の詳細の表示] をクリックします。
5. ページを閉じます。

## <a name="release-the-batch-order"></a>バッチ オーダーのリリース
1. アクション ウィンドウで、[製造オーダー] をクリックします。
2. [リリース] をクリックします。
3. [OK] をクリックします。

## <a name="schedule-production-jobs"></a>生産ジョブのスケジュール
1. [アクション ペイン] で、[スケジュール] をクリックします。
2. [ジョブのスケジュール設定] をクリックします。
3. [有限能力] フィールドで [いいえ] を選択します。
4. [有限原材料] フィールドで [いいえ] を選択します。
5. [OK] をクリックします。
6. アクション ウィンドウで、[製造オーダー] をクリックします。
7. [すべてのジョブ] をクリックします。
8. ページを閉じます。

## <a name="start-the-batch-order"></a>バッチ オーダーの開始
1. [開始] をクリックします。
2. [一般] タブをクリックします。
3. [ピッキング リスト転記] フィールドで、[いいえ] を選択します。
4. [OK] をクリックします。
5. アクション ウィンドウで、[表示] をクリックします。
6. [ピッキング リスト] をクリックします。
7. 一覧で、選択された行のリンクをクリックします。
8. ページを閉じます。
9. ページを閉じます。
10. [工順カード] をクリックします。
11. 一覧で、選択された行のリンクをクリックします。
12. ページを閉じます。
13. ページを閉じます。

