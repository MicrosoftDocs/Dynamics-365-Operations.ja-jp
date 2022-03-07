---
title: テスト ケースのチェーンへの変数のコピー
description: このトピックでは、 Regression Suite Automation Tool を使用してテスト ケースを連鎖させる方法 (テストが他のテストに値を渡す機能) について説明します。
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
ms.openlocfilehash: cfdae8dfa8ad7d8a34b85b5e1d54bb8cbdcfd215
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750344"
---
# <a name="copy-variables-to-chain-test-cases"></a>テスト ケースのチェーンへの変数のコピー

[!include [banner](../../includes/banner.md)]

Regression Suite Automation Tool の主要な機能の１つとして、テスト ケースの連鎖、つまり、テストが他のテストに値を渡す機能、があります。 テスト ケースは、 Azure DevOps テスト計画内で定義されている順序に従って実行され、テスト ツール自体で更新することもできます。 １つのテスト ケースから別のテスト ケースに変数を渡す場合は、テストを正しく順序付けることが重要です。

タスク レコーダーでテストを記録しながら変数の値を保存するには、次の図に示すように、フィールドを右クリックして **タスク レコーダー > コピー** を選択します。 コピーすると、変数は記録ファイルに保存されます。 この変数は、後続のテストで使用できます。

:::image type="content" source="media/task-recorder-copy.png" alt-text="タスク レコーダーのメニュー項目のコピー":::

RSAT が Excel パラメーター ファイルを生成する場合、保存された変数は **一般** タブの **保存された変数** テーブルに表示されます。これらの変数は、**TestCaseSteps** タブのテスト ケース ステップのコンテキストにも表示されます。次の画像内では、テスト ケースの記録中に発注書 ID の値がコピーされています (手順 5)。 この値は **{{PurchCreateOrder_PurchTable_PurchId_86_Copy}}** という名前の変数に格納されます 。

![Excel に保存された変数](media/saved-variables.png)

これらの変数をテスト再生中に再利用するには、次に示すように、変数名をコピーして、別のテスト (または同じテスト) のデータ ファイルでパラメーター値の代わりに使用します。

![Excel での変数の再利用](media/reuse-variables.png)

変数は、定義されている同じテストケースで使用できます。また、同じテストの実行中にテスト間で渡すこともできます。

## <a name="support-for-formulas-of-saved-variables"></a>保存された変数の式のサポート

保存された (コピーされた) 変数を含むフォーミュラを作成できます。 Regression Suite Automation Tool の古いバージョンのを使用している場合、この機能を利用するためには新しいExcel パラメーター ファイルを再生成する必要があります。 サポートされている演算子は、`+`, `-`, `/` および '\' です。 Regression Suite Automation Tool 式で使用できるのは、数値変数のみです。 文字列または日付はサポートされていません。 変数名は常に二重の中かっこ `{{varname}}` で指定します。 たとえば、`{{var1}} + {{var2}}`。

次の図では、2つの異なる変数が式で使用されています。

![Excelでの式の作成](media/formulas.png)

RSAT バージョン 1.220 の時点では、**ROUND**、**CONCAT**、**UPPER** などの Excel 関数を使用して、RAST 変数を使用した式を作成することもできます。 この機能は、Excel 式評価機能を使用して実装されるため、Excel でサポートされている関数は RSAT でサポートされています。

次にその例を示します。

+ 数値を最も近い整数に丸めるには、次のように使用します。

    `=ROUND({{Item_Price_3274_Copy}}, 0)`

+ 文字列を連結するには、以下を使用します。

    `=CONCATENATE({{AccountNum_3274_Copy}}, " ", {{ AddressBP_Locator_3274_Copy}})`

+ 日付を計算して文字列に変換するには、以下を使用します。

    `=TEXT(DATEVALUE({{SystemDate_CurrentDate_3276_Copy}}) - 1, "mm/dd/yyyy")`

    信頼性の高いテスト ケースを実行するため、必ず RSAT の日付値をテキストに変換してください。

RSAT では、テストの実行中にこれらの式が評価されるため、式の前に単一引用符 **\'** を付ける必要があります。これにより、Excel で式が不完全に計算されるのを防ぐことができます。 この図には、例が示されています。

![Excel 2 での式の作成](media/formulas-2.png)

## <a name="use-variables-in-message-validation"></a>メッセージ検証での変数の使用

保存された変数を、メッセージ検証タブの文字列の一部として使用することもできます。以下は、`Customer account {{variable name}} already exists.` というメッセージを検証する例です。 これは、テストの実行中に情報ログに表示されます。 `{{variable name}}` は、記録中にコピーされる変数です。

保存済 (コピー済) 変数は、同じテスト ケース内で、または同じテスト スイート内の複数のテスト ケース間で使用できます。

![変数を含むメッセージ](media/rsat-message-with-variable.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]