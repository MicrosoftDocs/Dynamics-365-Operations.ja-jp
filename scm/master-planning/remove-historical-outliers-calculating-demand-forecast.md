---
title: "需要予測を計算するときに、トランザクション履歴データから異常値を削除します。"
description: "この記事では、需要予測の計算に使用される履歴データから異常値を除外する方法について説明します。 異常値を除外すると、予測の精度が向上します。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 6f44e1ce566781f1586203528d55b13b28001a2c
ms.lasthandoff: 03/31/2017


---

# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a>需要予測を計算するときに、トランザクション履歴データから異常値を削除します。

この記事では、需要予測の計算に使用される履歴データから異常値を除外する方法について説明します。 異常値を除外すると、予測の精度が向上します。

予測の精度を高めるために飛び各を除外できます。 これはオプションのタスクです。 次にプロセスの概要について示します。

1.  [**マスタ プラン** &gt; **設定** &gt; **需要予測** &gt; **飛びの**の削除トランザクションを選択、除外するクエリを使用する**飛びの削除の**ページを開きます。
2.  クエリを適用する会社を選択し、名前と説明を入力します。 [**クエリの日付**] フィールドには、現在の日付が自動的に設定されます。
3.  [**有効**] チェック ボックスをオンにし、クエリによって検索されたトランザクションを履歴データから除外します。 この設定は、ベースライン予測を作成するときに適用されます。
4.  [**異常値削除クエリ**] ページで、ベースライン予測を計算するときに、除外するトランザクションを定義する基準を追加、削除、および選択できます。 たとえば、除外する特定の品目または注文トランザクションを選択します。
5.  [**トランザクションの表示**] をクリックします。 [**異常値トランザクション**] ページに、クエリで定義した条件を満たし、需要予測の計算時に履歴データから除外されるトランザクションが表示されます。

**注記:** 既存のクエリに基づいたクエリの作成もできます。 コピーするクエリを選択してから [**重複**] をクリックします。 [**クエリ日付**] フィールドがバージョンを識別します。 クエリをそのまま使用するか、[**クエリの編集**] をクリックして基準を変更することもできます。 必要に応じて新しいクエリの名前と説明を変更できます。

<a name="see-also"></a>参照
--------

[Introduction to demand forecasting](introduction-demand-forecasting.md)

[Monitoring forecast accuracy](monitor-forecast-accuracy.md)


