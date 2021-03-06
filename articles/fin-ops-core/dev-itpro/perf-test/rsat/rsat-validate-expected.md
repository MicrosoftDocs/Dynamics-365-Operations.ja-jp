---
title: 予測値を検証する
description: このトピックでは、Regression Suite Automation を使用して予測値を検証する方法を示します。
author: FrankDahl
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 21631
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dfd7f5479217e02258bf7e756dd3f3731da653dd
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866144"
---
# <a name="validate-expected-values"></a>予測値を検証する

[!include [banner](../../includes/banner.md)]

テスト ケースの重要なコンポーネントに、予期値の検証があります。 タスク レコーダーを使用するテスト ケースの作成時に検証パラメーターを定義できます。 記録中にコントロールを右クリックし、**タスク レコーダー > 検証** メニューの **現在の値** を選択します。 このアクションは、Regression Suite Automation Tool と共に使用できる検証手順になります。 このコントロール値は、自動的に生成された Excel パラメーター ファイルの検証変数になります。 メニュー項目を次の図に示します。

![メニュー項目の検証](media/validate-test-case.png)

タスク の作成方法についての詳細は、[タスク レコーダー リソース](../../user-interface/task-recorder.md)を参照してください。

RSAT がテスト ケースの Excel パラメーター ファイルを生成すると、次の図に示すように検証ステップが追加されます。 テスト ケースの実行中に使用する予測値を入力できます。

![変数の検証](media/rsat-validate-variables.png)

## <a name="validate-expected-values-using-operators"></a>演算子を使用して予測値を検証する

検証ステップで演算子を使用して、指定された値より変数が等しい、より小さい、または大きいことを検証することもできます。 この機能を使用するには、**設定** タブを開いて、**オプション** タブを選択します。**検証に演算子を使用する** という設定をオンにします。 このオプションは、RSAT バージョン 1.210 で使用できます。 以前のバージョンのツールを使用していた場合は、この機能を利用するために新しい Excel パラメーター ファイルを再生成する必要があります。 Excel ファイルに、次の図に示すような新しい **オペレーター** フィールドが表示されます。

![以前のバージョンの Excel での検証](media/validate-test-case-example.png)

## <a name="validate-the-state-of-a-control"></a>コントロールの状態の検証

テスト ケースを記録する場合、タスク レコーダーは、次の追加の検証アクションをサポートします。

+ コントロールが有効か無効かを検証します。
+ コントロールが編集可能か読み取り専用かを検証します。

この検証を活用するには、10.0.13 (またはそれ以降) および RSAT 2.0 (またはそれ以降) で実行されている Finance and Operationsアプリを使用する必要があります。 詳細については、[検証](../../user-interface/task-recorder.md#validate)を参照してください。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]