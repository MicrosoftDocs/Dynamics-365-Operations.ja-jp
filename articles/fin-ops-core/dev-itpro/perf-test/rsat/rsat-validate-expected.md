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
ms.custom: 21631
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b95132ba773c81196bbabc4fd814d2b0fb073203
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680440"
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

