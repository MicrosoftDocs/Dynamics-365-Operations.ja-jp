---
title: LISTOFFIELDS ER 関数
description: このトピックでは、LISTOFFIELDS 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 494dc347fadf44121c7eae0acf8c30768c58f035
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567667"
---
# <a name="listoffields-er-function"></a>LISTOFFIELDS ER 関数

[!include [banner](../includes/banner.md)]

`LISTOFFIELDS` 関数は、*列挙* または *コンテナー (レコード)* タイプの指定された引数の構造に基づいて作成された *レコード リスト* の値を返します。

## <a name="syntax-1"></a>構文 1

```vb
LISTOFFIELDS (path)
```

## <a name="syntax-2"></a>構文 2

```vb
LISTOFFIELDS (path, language)
```

## <a name="arguments"></a>引数

`path`: データ ソース参照

次のいずれかのデータ型のデータ ソースの有効な参照パス。

- モデルの列挙
- 形式列挙
- アプリケーションの列挙
- コンテナー (レコード)

`language`: *文字列*

言語コードを表すテキスト。

## <a name="return-values"></a>戻り値

*レコード リスト*

レコードの結果リスト。

## <a name="usage-notes"></a>使用上の注意

作成するリストは、次のフィールドを持つレコードで構成されます。

- **名前** (*文字列* データ型)
- **ラベル** (*文字列* データ型)
- **説明** (*文字列* データ型)
- **IsTranslated** (*ブール値* データ型)

`path` 引数が *コンテナー (レコード)* タイプのデータ ソースを参照している場合、参照コンテナー レコードのすべてのフィールドに対して、作成されたリストに新しいレコードが追加されます。 作成されるすべてのレコードについて、**名前** フィールドは、現在のレコードが作成された参照コンテナー レコードのフィールドの名前を返します。

`path` 引数が *列挙* 型のいずれかのデータ ソースを参照している場合、参照列挙の列挙値ごとに、作成されるリストに新しいレコードが追加されます。 作成されるすべてのレコードについて、**名前** フィールドは現在のレコードが作成された、参照列挙の値を返し、**説明** フィールドはその列挙の説明を返し、**ラベル** フィールドは、その列挙のラベルを返します。

実行時に構文 1 を使用する場合、**ラベル** および **説明** フィールドは、実行中の電子申告 (ER) 形式の言語設定に基づく値を返す必要があります。

- 要求された言語のラベルと説明が使用可能な場合、**ラベル** および **説明** フィールドはその言語に基づく値を返し、**IsTranslated** フィールドは **True** を返します。
- 要求された言語のラベルと説明が使用できない場合、**ラベル** および **説明** フィールドは既定の **EN-US** 言語に基づく値を返し、**IsTranslated** フィールドは **False** を返します。

実行時に構文 2 を使用する場合、**ラベル** および **説明** フィールドは、呼び出された関数の 2 番目の引数として定義されている言語に基づく値を返す必要があります。

- 要求された言語のラベルと説明が使用可能な場合、**ラベル** および **説明** フィールドはその言語に基づく値を返し、**IsTranslated** フィールドは **True** を返します。
- 要求された言語のラベルと説明が使用できない場合、**ラベル** および **説明** フィールドは **EN-US** 言語に基づく値を返し、**IsTranslated** フィールドは **False** を返します。

## <a name="example-1"></a>例 1

次の図では、列挙は ER データ モデルで導入されます。

<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

次の図は、これらの詳細について説明しています。

- モデル列挙はデータ ソースとしてレポートに挿入されます。
- ER の式は `LISTOFFIELDS` 関数のパラメーターとしてモデル列挙を使用します。
- *レコード リスト* タイプのデータ ソースは、作成された ER の式を使用してレポートに挿入されます。

<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>

次の例では、`LISTOFFIELDS` 関数を使用して作成された *レコード リスト* タイプのデータ ソースにバインドされている ER 形式要素を示します。

<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

次の図は、設計された形式が実行される際の結果を示します。

<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a>

> [!NOTE] 
> 親 **FILE** および **FOLDER** 形式要素の言語設定に基づいて、ラベルと説明の翻訳文は、ER 形式出力に入力されます。

## <a name="example-2"></a>例 2

*計算済フィールド* データ ソース型を使用して、**enumType** データ モデル列挙に対して **enumType\_de** および **enumType\_deCH** データ ソースを構成します。

- **enumType\_de** = `LISTOFFIELDS (enumType, "de")`
- **enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`

この場合、その翻訳が使用可能な場合は、スイス ドイツ語の列挙値のラベルを取得する次の式を使用できます。 スイス ドイツ語翻訳を使用できない場合、ラベルはドイツ語になります。

```vb
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
```

## <a name="additional-resources"></a>追加リソース

[リスト機能](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]