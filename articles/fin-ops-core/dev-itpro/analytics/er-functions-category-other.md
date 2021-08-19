---
title: ビジネス ドメイン固有のカテゴリ内の ER 関数のリスト
description: このトピックでは、電子申告 (ER) でサポートされるビジネス ドメイン固有の関数について説明します。
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: a8f0812e4262a264ffc89b72e0f4fc8c55d6c6822095f550c8f05296bb057a38
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712336"
---
# <a name="list-of-er-functions-in-the-business-domainspecific-category"></a>ビジネス ドメイン固有のカテゴリ内の ER 関数のリスト

[!include [banner](../includes/banner.md)]

電子報告 (ER) ドメイン固有の関数を使用すると、Microsoft Dynamics 365 Finance の実装固有の計算およびデータ アクセス要求を実行できます。 このトピックでは、これらの関数の概要を示します。

## <a name="list-of-supported-functions"></a>サポートされている関数のリスト

| 職務| 説明 |
|---------|-------------|
| [CH_Bank_Mod_10](er-functions-other-chbankmode10.md) | この関数は、指定された請求書番号の桁数に基づいて、MOD10 式として債権者参照を表す *文字列* 値を返します。 |
| [CN_GBT_AdditionalDimensionID](er-functions-other-cngbtadditionaldimensionid.md) | この関数は、指定された文字列から取得された単一の財務分析コード ID を表す *文字列* 値を返します。 指定された文字列は、ID のコンマ区切りのリストとしてすべての分析コードを示します。 |
| [ConvertCurrency](er-functions-other-convertcurrency.md) | この関数は、特定の日付で指定された会社の設定を使用して、指定された換算元の通貨から指定された換算先の通貨に指定された金額を変換した結果を表す、*実数* 値を返します。 |
| [CurCredRef](er-functions-other-curcredref.md) | この関数は、指定された請求書番号の桁数に基づいて、債権者参照を表す *文字列* 値を返します。 |
| [FA_Balance](er-functions-other-fabalance.md) | この関数は、指定された固定資産品目、価値モデル コード、レポート年度、およびレポート日付の固定資産残高のデータで構成される *コンテナー (レコード)* 値を返します。 |
| [FA_Sum](er-functions-other-fasum.md) | この関数は、指定された固定資産品目、価値モデル コード、およびの固定資産額のデータで構成される *コンテナー (レコード)* 値を返します。 |
| [GetCurrentCompany](er-functions-other-getcurrentcompany.md) | この関数は、現在ユーザーがサイン インしている法人 (会社) コードのテキスト表現する *文字列* 値を返します。 |
| [ISOCredRef](er-functions-other-isocredref.md) | この関数は、指定された請求書番号の数字とアルファベット記号に基づいて、国際標準化機構 (ISO) 送金受取人参照情報を表す *文字列* 値を返します。 |
| [IsValidCharacterISO7064](er-functions-other-isvalidchariso7064.md) | この関数は、指定された文字列が有効な国際銀行番号 (IBAN) を表す場合、**TRUE** の *ブール* 値を返します。 それ以外の場合は、**FALSE** の *ブール* 値が返されます。 |
| [Mod_97](er-functions-other-mod97.md) | この関数は、指定された請求書番号の桁数に基づいて、MOD97 式として債権者参照を表す *文字列* 値を返します。 |
| [NumSeqValue](er-functions-other-numseqvalue.md) | この関数は、指定された番号順序、範囲、およびスコープ ID に基づいて、番号順序の新しい生成値を表す *文字列* 値を返します。 スコープ ID は、ER 形式が実行されるコンテキストによって提供される会社コードと同じです。 |
| [RoundAmount](er-functions-other-roundamount.md) | この関数は、指定された丸めルールに従って、指定された数値を指定された小数点以下の桁数となるように丸めた結果を表す *実数* 値を返します。 |
| [TableName2ID](er-functions-other-tablename2id.md) | この関数は、*整数* 値として指定されたテーブル名に対応するテーブル ID の数値表現を返します。 |

## <a name="additional-resources"></a>追加リソース

[電子申告の概要](general-electronic-reporting.md)

[電子申告のフォーミュラ デザイナー](general-electronic-reporting-formula-designer.md)

[電子報告のフォーミュラ言語](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]