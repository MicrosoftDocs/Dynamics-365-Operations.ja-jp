---
title: 需要予測を計算するときに、トランザクション履歴データから異常値を削除します。
description: この記事では、需要予測の計算に使用される履歴データから異常値を除外する方法について説明します。 異常値を除外すると、予測の精度が向上します。
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup, ReqDemPlanOutlierQueryPreview
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d4e42e566cef774c1a25cf48ec131b74924868d0
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2022
ms.locfileid: "9741097"
---
# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a>需要予測を計算するときに、トランザクション履歴データから異常値を削除します。

[!include [banner](../includes/banner.md)]

この記事では、需要予測の計算に使用される履歴データから異常値を除外する方法について説明します。 異常値を除外すると、予測の精度が向上します。

異常値を除外すると、予測の精度が向上します。 これはオプションのタスクです。 次にプロセスの概要について示します。

1.  **マスター プラン** &gt; **設定** &gt; **需要予測** &gt; **異常値の削除** の順にクリックして、クエリを使用して除外するトランザクションを選択できる **異常値の削除** ページを開きます。
2.  クエリを適用する会社を選択し、名前と説明を入力します。 **クエリの日付** フィールドには、現在の日付が自動的に設定されます。
3.  **有効** チェック ボックスをオンにし、クエリによって検索されたトランザクションを履歴データから除外します。 この設定は、ベースライン予測を作成するときに適用されます。
4.  **異常値削除クエリ** ページで、ベースライン予測を計算するときに、除外するトランザクションを定義する基準を追加、削除、および選択できます。 たとえば、除外する特定の品目または注文トランザクションを選択します。
5.  **トランザクションの表示** をクリックします。 **異常値トランザクション** ページに、クエリで定義した条件を満たし、需要予測の計算時に履歴データから除外されるトランザクションが表示されます。

**注記:** 既存のクエリに基づいたクエリの作成もできます。 コピーするクエリを選択してから **重複** をクリックします。 **クエリ日付** フィールドがバージョンを識別します。 クエリをそのまま使用するか、**クエリの編集** をクリックして基準を変更することもできます。 必要に応じて新しいクエリの名前と説明を変更できます。

## <a name="additional-resources"></a>追加リソース

- [需要予測の概要](introduction-demand-forecasting.md)
- [予測精度の監視](monitor-forecast-accuracy.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]