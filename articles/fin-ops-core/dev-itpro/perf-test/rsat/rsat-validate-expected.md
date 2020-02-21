---
title: 予測値を検証する
description: このトピックでは、Regression Suite Automation を使用して予測値を検証する方法を示します。
author: robadawy
manager: AnnBe
ms.date: 08/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 21631
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 158b641a1e3aaf41288d273fab2f0e391fb2b154
ms.sourcegitcommit: c5ef9a1d1853095ab537389b9a8e2d2adb39ed8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/08/2020
ms.locfileid: "3033080"
---
# <a name="validate-expected-values"></a>予測値を検証する

[!include [banner](../../includes/banner.md)]

テスト ケースの重要なコンポーネントに、予期値の検証があります。 タスク レコーダーを使用するテスト ケースの作成時に検証パラメーターを定義できます。 記録中にコントロールを右クリックし、**タスク レコーダー > 検証** メニューの **現在の値** を選択します。 このアクションは、Regression Suite Automation Tool と共に使用できる検証手順になります。 このコントロール値は、自動的に生成された Excel パラメーター ファイルの検証変数になります。 メニュー項目を次の図に示します。

![メニュー項目の検証](media/validate-test-case.png)
 
タスク の作成方法についての詳細は、[タスク レコーダー リソース](../../user-interface/task-recorder.md)を参照してください。

RSAT がテスト ケースの Excel パラメーター ファイルを生成すると、次の図に示すように検証ステップが追加されます。 テスト ケースの実行中に使用する予測値を入力できます。 

![変数の検証](media/rsat-validate-variables.png)

## <a name="validate-expected-values-using-operators"></a>演算子を使用して予測値を検証する

検証ステップでは、演算子を使用することもできます。 この機能を使用するには、Regression Suite Automation Tool のインストール フォルダーの **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** という名前の構成ファイルを編集する必要があります。 ファイルを編集し、**AddOperatorFieldsToExcelValidation** の値を **true** に変更します。

```Xml
<add key=" AddOperatorFieldsToExcelValidation" value="true" />
```

Regression Suite Automation Tool の以前のバージョンでは、コントロール値が予測値に等しいかどうかのみが検証可能でした。 この新しい機能を使用すると、変数が指定された値と等しくない、指定された値より小さい、または指定された値より大きいことを検証できます。

このツールの古いバージョンを使用してきた場合、この機能を活用するためには、新しい Excel パラメーター ファイルを再生成する必要があります。 Excel ファイルに、次の図に示すような新しい **オペレーター** フィールドが表示されます。

![以前のバージョンの Excel での検証](media/validate-test-case-example.png)

