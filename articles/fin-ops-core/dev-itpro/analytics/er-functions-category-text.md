---
title: テキスト カテゴリ内の ER 関数のリスト
description: このトピックでは、電子申告 (ER) でサポートされるテキスト関数について説明します。
author: NickSelin
ms.date: 09/09/2021
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
ms.openlocfilehash: afe45bf1ff5c641346997aa4f32f3241dce2f0a2
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075503"
---
# <a name="list-of-er-functions-of-the-text-category"></a>テキスト カテゴリ内の ER 関数のリスト

[!include [banner](../includes/banner.md)]

電子申告 (ER) テキスト関数を使用して、*文字列* データ タイプのデータ ソースで操作を実行できます。 このトピックでは、これらの関数の概要を示します。

## <a name="list-of-supported-functions"></a>サポートされている関数のリスト

| 職務 | 説明 |
|----------|-------------|
| [Char](er-functions-text-char.md) | この関数は、指定された Unicode 番号で参照される単一の文字を表す *文字列* 値を返します。 |
| [連結](er-functions-text-concatenate.md) | この関数は、1 つの文字列に結合された後、*文字列* 値として指定されたすべてのテキスト文字列を返します。 |
| [形式](er-functions-text-format.md) | この関数は、*N* 番目の引数で **%N** の出現を置き換えることで書式設定した後に、*文字列* 値として指定された文字列を返します。 |
| [GetEnumValueByName](er-functions-text-getenumvaluebyname.md) | この関数は、*文字列* 値として指定された列挙名を使用して、指定された列挙データソースの特定の *列挙* 値を検索します。 *列挙* 値が見つかった場合、関数によって返されます。 |
| [GetLabelText](er-functions-text-getlabeltext.md) | この関数は、特定のラベルを検索して、指定したラベルの翻訳を表す *[文字列](er-formula-supported-data-types-primitive.md#string)* 値を指定した言語で返します。 |
| [GuidValue](er-functions-text-guidvalue.md) | この関数は、指定された *文字列* 型の入力を *GUID* 型のデータ品目に変換します。 |
| [JsonValue](er-functions-text-jsonvalue.md) | この関数は指定した ID に基づくスカラー値を抽出し、指定したパスでアクセスする JavaScript Object Notation (JSON) 形式で、データを解析します。 次に、抽出したスカラー値を *文字列* 値として返します。 |
| [左](er-functions-text-left.md) | この関数は、指定された文字列の冒頭から指定された数の文字を表す *文字列* 値を返します。 |
| [Len](er-functions-text-len.md) | この関数は、指定された文字列の文字数を表す *整数* 値を返します。 |
| [Lower](er-functions-text-lower.md) | この関数は、小文字に変換した後の *文字列* 値として指定されたテキスト返します。 |
| [Mid](er-functions-text-mid.md) | この関数は、指定された位置から始まる指定された文字列から、指定された数の文字を表す *[文字列](er-formula-supported-data-types-primitive.md#string)* 値を返します。 |
| [NewGUID](er-functions-text-newguid.md) | この関数は、新しく生成された *[GUID](er-formula-supported-data-types-primitive.md#guid)* 値を返します。 |
| [NumberFormat](er-functions-text-numberformat.md) | この関数は、指定された形式およびオプションで指定されたカルチャで指定された数を表す、*文字列* 値を返します。 |
| [NumeralsToText](er-functions-text-numeralstotext.md) | この関数は、指定された言語で綴らた (つまり、テキスト文字列に変換された) 後、*文字列* 値として指定された数を返します。 |
| [PadLeft](er-functions-text-padleft.md) | この関数は、指定された長さの *文字列* 値を返します。指定された文字列の先頭には、指定された文字のインスタンスが 1 つ以上パディングされます。 |
| [QrCode](er-functions-text-qrcode.md) | この関数は、バイナリ形式の指定された文字列に対して、クイック応答コード (QR コード) イメージを表示する *コンテナー* 値を返します。 |
| [置換](er-functions-text-replace.md) | この関数は、すべてまたはその一部が別の文字列に置換した後、*文字列* 値として指定されたテキストの文字列を返します。 |
| [右](er-functions-text-right.md) | この関数は、指定された文字列の末尾から指定された数の文字を表す *文字列* 値を返します。 |
| [テキスト](er-functions-text-text.md) | この関数は、現在のアプリケーション インスタンス のサーバー ロケール設定に従って書式設定されるテキスト文字列に変換した後に、*文字列* 値として指定された数を返します。 |
| [翻訳](er-functions-text-translate.md) | この関数は、指定したテキストを別の提供された文字セットに置換した結果を含む *文字列* 値を返します。 |
| [Trim](er-functions-text-trim.md) | この関数は、先頭と末尾のスペースを切り捨ててから *文字列* 値として指定されたテキスト文字列を返し、その後単語間の複数のスペースが削除されます。 |
| [Upper](er-functions-text-upper.md) | この関数は、大文字に変換した後の *文字列* 値として指定されたテキスト返します。 |

## <a name="additional-resources"></a>追加リソース

[電子申告の概要](general-electronic-reporting.md)

[電子申告のフォーミュラ デザイナー](general-electronic-reporting-formula-designer.md)

[電子報告のフォーミュラ言語](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
