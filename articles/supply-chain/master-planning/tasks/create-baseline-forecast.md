---
title: ベースライン予測の作成
description: タイム シリーズの予測モデルを使用するか、または履歴需要をコピーするかのいずれかの方法を使用して、生産計画担当者はベースライン予測を作成できます。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup, ReqIntercompanyPlanningGroupAllocKeys, ReqDemPlanForecastParameters, ReqDemPlanCreateForecastDialog, SysQueryForm, ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d23e245ed1c084c26554ef3f859fdadaef9990d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553002"
---
# <a name="create-a-baseline-forecast"></a>ベースライン予測の作成

[!include [task guide banner](../../includes/task-guide-banner.md)]

タイム シリーズの予測モデルを使用するか、または履歴需要をコピーするかのいずれかの方法を使用して、生産計画担当者はベースライン予測を作成できます。 この手順では、需要履歴をコピーし、1 つの品目配賦キーを使用してすべての製品のベースライン予測を作成する方法を示します。 


## <a name="set-up-an-item-allocation-key"></a>品目配賦キーの設定
1. [マスター プラン] > [設定] > [会社間計画グループ] の順に移動します。
2. クイック フィルターを使用して、レコードを見つけます。 たとえば、値「10」を含む [名前] フィールドをフィルター処理します。
    * 需要予測は法人間で実行されます。 このため、1 件の会社間計画グループの予測を生成するために使用するすべての会社を設定する必要があります。  
3. 一覧で、目的のレコードを見つけ、選択します。
4. [品目配賦キー] をクリックします。
    * 予測を作成するために使用するすべての品目配賦キーを選択します。  
5. 一覧で、選択された行をマークします。
    * D_Aloc の品目配賦キーを選択します。  
6. [>] を選択します。
7. ページを閉じます。
8. ページを閉じます。

## <a name="set-up-the-demand-forecasting-paramters"></a>需要予測のパラメーターの設定
1. [マスター プラン] > [設定] > [需要予測] > [需要予測のパラメーター] の順に移動します。
2. 予測アルゴリズム パラメータ セクションを展開します。
3. [予測生成戦略] フィールドで、[履歴需要の上書き] を選択します。
4. [保存] をクリックします。

## <a name="create-a-baseline-forecast"></a>ベースライン予測の作成
1. [マスター プラン] > [予測] > [需要予測] > [統計ベースライン予測の生成] の順に移動します。
2. [開始日] フィールドに日付を入力します。
    * 2015 年 1 月 1 日以降の販売注文がある場合、その日付を入力します。 ない場合、販売注文の最も早い日付を入力します。  
3. [終了日] フィールドで、日付を入力します。
    * 販売注文の終了日を入力します。例「2015-03-31」。  
4. [開始日] フィールドに日付を入力します。
    * 「2015-04-01」と入力します。 この日付は、次の予測バケットの開始日として自動的に計算されます。  
5. [対象に含めるレコード] セクションを展開します。
6. [フィルター] をクリックします。
7. 一覧で、選択された行をマークします。
    * [会社間計画グループ] フィールドの行をマークします。  
8. [基準] フィールドに値を入力します。
    * 会社間計画グループを入力します。たとえば、最初のタスクに使用した「10」を入力します。  
9. 一覧で、目的のレコードを見つけ、選択します。
    * [品目配賦キー] フィールドの行を選択します。  
10. [基準] フィールドに値を入力します。
11. [OK] をクリックします。
12. [詳細パラメーター] セクションを展開します。
13. [予測バケット] フィールドで [月] を選択します。
14. [予測期間] フィールドに「3」を入力します。
15. [凍結タイム フェンス] フィールドに「1」を入力します。
16. [OK] をクリックします。

## <a name="visualize-the-demand-forecast"></a>需要予測の視覚化
1. [マスター プラン] > [予測] > [需要予測] > [調整された需要予測] の順に移動します。
2. 集計ビュー テーブルで、行 1、行 2 のセルを選択します。 これは、作成した予測の 2 番目の月です。
3. QtyCell に「400」を設定します。
    * セルでは、予測された以外の数、例えば「400」を入力します。  
4. 予測に手動調整を実行しました。 次の手順ではグラフィカル インジケータに注意します。
5. [予測明細行の詳細] をクリックします。
    * このページでは、正確性の値、履歴需要および予測を確認できます。 予測にも変更を加えることができます。  

