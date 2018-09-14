--- 
title: "リーン生産の転送活動の作成"
description: "リーン生産の移動活動を作成します。"
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 010ac08fa96ead49b6ecbbe083e59fb96427e29e
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="create-transfer-activities-for-lean-manufacturing"></a>リーン生産の転送活動の作成

[!include [task guide banner](../../includes/task-guide-banner.md)]

リーン生産の移動活動を作成します。 

前提条件: 

1. 有効ではない生産フローおよびバージョンを作成する必要があります。

2. 配送元と配送先の倉庫と場所を作成する必要があります。 必要に応じて、補充する作業セルまたは補充された作業セルを作成する必要があります。


## <a name="find-the-production-flow-version"></a>生産フロー バージョンの検索
1. [生産管理] > [設定] > [リーン生産フロー] > [生産フロー] の順に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
    * 生産フローはドラフト ステータスのバージョンが必要なことに注意してください。  
3. 一覧で、選択された行のリンクをクリックします。

## <a name="create-a-new-activity"></a>新しい活動の作成
1. [活動] をクリックします。
    * 選択した生産フローに、ドラフト バージョンがあることを確認し、そのバージョンを選択します。  
2. [新しい計画活動の作成] をクリックします。
3. [次へ] をクリックします。
4. [名前] フィールドに値を入力します。
5. [活動タイプ] フィールドで、「移動」を選択します。
6. [処理数量] フィールドで、数値を入力します。
7. [次へ] をクリックします。

## <a name="select-the-work-cells"></a>作業セルの選択
1. [補充中] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
    * 転送活動で移動元場所として作業セルの出荷場所を使用するには、作業セルを選択します。 転送活動の移動先の場所を設定する、補充する作業セルに対しても同じことが当てはまります。  
2. 一覧で、選択された行のリンクをクリックします。

## <a name="define-the-inventory-updates"></a>在庫更新の定義
1. [製品タイプ] フィールドで、オプションを選択します。
    * 転送は製品のタイプを変更しないことに注意してください。 完成品または半完成製品 (生産フローおよびかんばんフローなど 2 つの活動間の転送) を転送できます。     完成品を転送すると、在庫トランザクションのピッキングまたは受取結果を選択できます。  

## <a name="define-the-transfer-locations"></a>配送場所の定義
1. [次へ] をクリックします。
2. [倉庫] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
3. 一覧で、目的のレコードを見つけ、選択します。
4. 一覧で、選択された行のリンクをクリックします。
5. [場所] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
6. 一覧で、選択された行のリンクをクリックします。
7. [配送業者] フィールドで、「荷主」を選択します。
    * 次のオプションがあります。荷主 - 出荷倉庫を運営している組織。受取人 - 入荷倉庫を運営している組織。配送業者 - サード パーティの仕入先。 運営組織が仕入先である場合、転送活動には外注契約が必要です。  
8. [次へ] をクリックします。

## <a name="define-the-activity-times"></a>活動時間の定義
1. 一覧で、目的のレコードを見つけ、選択します。
    * ランタイムの定義が必要です。 ランタイムは、かんばん作業の原価およびスループットの時間の計算に使用されます。 ランタイムは最大能力負荷および消費の計算には使用されていません。これは生産フロー バージョンのタスクから導かれるサイクル時間で計算されます。  
2. [時刻] フィールドで、数値を入力します。
3. [単位] フィールドに値を入力します。
4. [時間単位] を選択します。
5. [数量ごと] フィールドで、数値を入力します。
6. 一覧で、目的のレコードを見つけ、選択します。
    * 待ち時間はオプションです。  
7. [時刻] フィールドで、数値を入力します。
8. [単位] フィールドに値を入力します。
9. [時間単位] を選択します。
10. [数量ごと] フィールドで、数値を入力します。
11. [次へ] をクリックします。
12. [完了] をクリックします。
13. ページを閉じます。


