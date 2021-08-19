---
title: 電子レポート形式でサポートされるプリミティブ データ型
description: このトピックでは、電子申告 (ER) の式でサポートされるプリミティブ データ型について説明します。
author: NickSelin
ms.date: 06/02/2021
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 72c372a4d9b6af337731ff0bbd750b3b58f27bb79cb3813a0b5e4f79707d9f5c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730610"
---
# <a name="supported-primitive-data-types-for-electronic-reporting-formulas"></a>電子レポート形式でサポートされるプリミティブ データ型

[!include [banner](../includes/banner.md)]

このトピックでは、[電子申告 (ER)](general-electronic-reporting.md)の式でサポートされるプリミティブ データ型について説明します。 プリミティブ データ型の一覧を次に示します。

- [ブール値](#boolean)
- [日付](#date)
- [datetime](#datetime)
- [列挙型](#enumeration)
- [guid](#guid)
- [整数](#integer)
- [int64](#int64)
- [実質](#real)
- [文字列](#string)

## <a name="boolean"></a><a name="boolean"></a>ブール値

*ブール値* プリミティブ データ型には、*true* または *false* のいずれかとして評価される値が含まれます。 *ブール値* 式が予期される場所では、引当済のリテラル キーワード **True** および **False** を使用することができます。 既定値は *false* です。

*ブール値* の内部テーブル現は *整数* です。 *整数* 値 0 (ゼロ) は *false* と評価され、他のすべての *整数値* は *true* と評価されます。 [ER 式デザイナー](er-advanced-formula-editor.md) で *ブール値* を返す構成済みの式を [検証](general-electronic-reporting-formula-designer.md#TestFormula) すると、式が *false* を返したときにテスト結果ペインに *0* (ゼロ) が表示されます。 それ以外の場合、テスト結果ペインに *1* が表示されます。

*ブール値* に暗黙的な変換はありません。 ただし、[TEXT](er-functions-text-text.md) 関数を使用して *ブール値* を *文字列* に明示的に変換することができます。

- *false* の値は、文字列 **False** に変換されます。
- *true* の値は、文字列 **True** に変換されます。

> [!NOTE]
> この変換は、提供された言語とカルチャの [コンテキスト](er-design-multilingual-reports.md) に依存しません。

比較 [演算子](er-formula-language.md#Operators) は、*ブール値* データ型で使用できる唯一の演算子です。 次の演算子を使用して、2 つの *ブール* 値を比較することができます:  \<\> and =。

## <a name="date"></a><a name="date"></a>日

*date* プリミティブ データ型は、年、月、日を含みます。 データは、次の関数を使用して開始できます。

- [DATEVALUE](er-functions-datetime-datevalue.md)
- [NULLDATE](er-functions-datetime-nulldate.md)
- [SESSIONTODAY](er-functions-datetime-sessiontoday.md)
- [TODAY](er-functions-datetime-today.md)

*日付* データ型は、1900 年 1 月 1 日～ 2154 年 12 月 31 日の日付を保持できます。 既定値は、**null** で、内部表示は、日付の 1900 年 1 月 1 日です。

*日付* に暗黙的な変換はありません。 ただし、次の明示的な変換関数を使用できます。

- [DATEFORMAT](er-functions-datetime-dateformat.md)
- [DATETODATETIME](er-functions-datetime-datetodatetime.md)
- [TEXT](er-functions-text-text.md)

[ADDDAYS](er-functions-datetime-adddays.md) 関数を使用すると、日付から日数を加算および減算できます。 このようにして、日付を特定の日数を未来と過去に移動できます。 [DAYS](er-functions-datetime-days.md) 関数を使用すると、日付を相互に減算し、日数での差を計算できます。 *日付* の値の変換に関する詳細は、[日時カテゴリーの ER 関数一覧](er-functions-category-datetime.md) を参照してください。

比較 [演算子](er-formula-language.md#Operators) は、*日付* データ型で使用できる唯一の演算子です。 次の演算子を使用して、2 つの *日付* の値を比較することができます: \<\>、\<, \<=, =, \>、および \>=。

## <a name="datetime"></a><a name="datetime"></a>Datetime

*日時* プリミティブ データ型は *日付* 型と、午前 0 時から経過した時刻を表す値を組み合わせたものです。 時間は、時間、分、秒、秒の分数で表されます。 *datetime* の値には、タイム ゾーンに関する情報も含まれています。

*日時* データ型は、1900 年 1 月 1 日 (ラウンド トリップ [形式](/dotnet/standard/base-types/standard-date-and-time-format-strings) で 1900-01-01T00:00:00.0000000+00:00) から 2154 年 12 月 31 日 (ラウンドトリップ形式で 2154/12/31T11:59:59.9999999+00:00)。 *日時* の最小時間単位は 1000 万分の 1 秒です。

> [!NOTE]
> **hh** [指定子](/dotnet/standard/base-types/standard-date-and-time-format-strings) を時間単位で使用すると、12:59:59:9999999 より上の時間値は有効時間と解釈できません。
>
> **HH** 指定子 を時間単位で使用すると、23:59:59:9999999 より上の時間値は有効時間と解釈できません。

既定値は **null** で、内部表現は 1900 年 1 月 1 日 (ラウンドトリップ形式で 1900-01-01T00:00:00.0000000+ 00:00) の日付です。

Datetimes は、次の関数を使用して開始できます。

- [DATETIMEVALUE](er-functions-datetime-datetimevalue.md)
- [NULNULLDATETIMELDATE](er-functions-datetime-nulldatetime.md)
- [SESSIONNOW](er-functions-datetime-sessionnow.md)
- [NOW](er-functions-datetime-now.md)

*datetime* に暗黙的な変換はありません。 ただし、次の明示的な変換関数を使用できます。

- [DATETIMEFORMAT](er-functions-datetime-datetimeformat.md)
- [TEXT](er-functions-text-text.md)

*datetime* の値の変換に関する詳細は、[日時カテゴリーの ER 関数一覧](er-functions-category-datetime.md) を参照してください。

比較 [演算子](er-formula-language.md#Operators) は、*datetime* データ型で使用できる唯一の演算子です。 次の演算子を使用して、2 つの *datetime* の値を比較することができます: \<\>、\<, \<=, =, \>、および \>=。

## <a name="enumeration"></a><a name="enumeration"></a>列挙型

*列挙* のプリミティブ データ型は、リテラルのリストです。 アプリケーションの [ソース コード](../dev-ref/xpp-data-primitive.md#enum) で定義されている列挙体を使用できます。 ER [データ モデル ](general-electronic-reporting.md#data-model-and-model-mapping-components)コンポーネントとER [形式](general-electronic-reporting.md#FormatComponentOutbound) コンポーネントで独自の列挙を導入することもできます。

アプリケーション *列挙* は、ER モデル マッピングと ER 形式の式で使用できます。

次の図は、編集可能なERデータ モデルに **CustVendCorrectiveReasonCode** モデル列挙体を追加する方法を示しています。

[![ER データ モデル デザイナーでモデルの列挙を構成する。](./media/er-formula-supported-data-types-primitive-enum1.gif)](./media/er-formula-supported-data-types-primitive-enum1.gif)

モデルの *列挙* は、*モデル* が導入されたデータ モデルの下で作成された ER モデル マッピングおよび ER 形式の式で使用できます 。

次の図は、**編集可能な ER 形式に Natura 逆請求サブ カテゴリー** の一覧の書式列挙を追加する方法を示しています。

[![ER 形式デザイナーで形式の列挙を構成する。](./media/er-formula-supported-data-types-primitive-enum2.gif)](./media/er-formula-supported-data-types-primitive-enum2.gif)

形式の *列挙* は、*列挙* が導入された ER 形式の式でのみ使用できます。

設定済 ER コンポーネントに特定の列挙を定数として、または ER ソリューションを実行しているユーザーが実行時にダイアログ ボックスで定義した値として、適切な種類の ER データ ソースを使用する必要があります。

- アプリケーションの列挙には、**Dynamics 365 for Operations \ 列挙** と **一般 \ ユーザー入力パラメータ** のデータ ソースを使用してアクセスできます。 次の図は **NoYes** アプリケーションの列挙を参照する編集可能な ER 形式 **appenumNoYes** データソースと **uipNoYes** データソースに追加する方法を示しています。

    [![ER 形式デザイナーでのアプリケーション列挙データ ソースの追加。](./media/er-formula-supported-data-types-primitive-enum3a.gif)](./media/er-formula-supported-data-types-primitive-enum3a.gif)

- データ モデルの列挙には、データ **モデル \ 列挙** および **データ モデル \ 列挙のユーザー入力パラメーター** データ ソースを使用してアクセスできます。 次の図は **CustVendCorrectiveReasonCode** データモデルの列挙を参照する編集可能な ER 形式 **CustVendCorrectiveReasonCode** データソースに追加する方法を示しています。

    [![ER 形式デザイナーでのアプリケーション列挙データ ソースの追加。](./media/er-formula-supported-data-types-primitive-enum3b.gif)](./media/er-formula-supported-data-types-primitive-enum3b.gif)

- データ モデルの列挙には、データ **モデル \ 列挙** および **データ モデル \ 列挙のユーザー入力パラメーター** データ ソースを使用してアクセスできます。 次の図は **Natura reverse charge subcategories** 形式の列挙を参照する編集可能な ER 形式 **NaturaReverseCharge** データソースに追加する方法を示しています。

    [![ER 形式デザイナーでのアプリケーション列挙データ ソースの追加。](./media/er-formula-supported-data-types-primitive-enum3c.gif)](./media/er-formula-supported-data-types-primitive-enum3c.gif)

*ブール値* に暗黙的な変換はありません。 [TEXT](er-functions-text-text.md) 変換関数を使用すると *列挙* をテキスト文字列に変換することができます。 この変換は言語に依存しません。 *列挙* 値を適切な言語固有のラベルに関連付ける方法については、[LISTOFFIELDS](er-functions-list-listoffields.md) 関数と [GETENUMVALUEBYNAME](er-functions-text-getenumvaluebyname.md) 関数の使用例を参照してください。

比較 [演算子](er-formula-language.md#Operators) は、*列挙* データ型で使用できる唯一の演算子です。 次の演算子を使用して、2 つの *列挙* 値を比較することができます:  \<\> and =。

## <a name="guid"></a><a name="guid"></a>Guid

*guid* プリミティブ データ型は、グローバルに一意の識別子 (GUID) 値を保持します。 GUID は、固有の識別子が必要な場合に、すべてのコンピューターとネットワークで使用できる値です。 数字が重複することはあまりありません。 有効な GUID は、次のすべての仕様を満たします。

- 32 桁の 16 進数が必要です。
- さらに、次の場所では埋め込まれるダッシュ文字が 4 つ必要です: 8-4-4-4-12。
- また、文字列の先頭と末尾にオプションの中かっこ \{\} を追加することもできます。 たとえば **\{2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212\}** および **2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212** は有効な GUID 文字列です。
- したがって、かっこを追加するかどうかに応じて、合計 36 文字または 38 文字にする必要があります。
- 16 進数の桁として使用されている文字は、大文字 (A–F)、小文字 (a–f)、または混在することができます。

次の明示的な変換関数を使用できます。

- [GUIDVALUE](er-functions-text-guidvalue.md)
- [TEXT](er-functions-text-text.md)

比較 [演算子](er-formula-language.md#Operators) は、*guid* データ型で使用できる唯一の演算子です。 次の演算子を使用して、2 つの *guid* 値を比較することができます:  \<\> and =。

## <a name="integer"></a><a name="integer"></a>整数

*整数* プリミティブ データ型は、小数点以下の桁数を持たない数値を表します。 整数は、繰り返しのステートメントの制御変数またはレコード リストのインデックスとして使用されます。

*整数* リテラルは **12345** のように、ER [式](general-electronic-reporting-formula-designer.md#formula-designer-overview) (フォーミュラ) に直接入力された整数です。 *整数* は 32 ビット幅です。 既定値は、**0** で、内部表示は、長い番号です。 *整数* は自動的に *実数* に変換されます。

さらに、次の明示的な変換関数を使用できます。

- [INTVALUE](er-functions-conversion-intvalue.md)
- [NUMBERFORMAT](er-functions-text-numberformat.md)
- [TEXT](er-functions-text-text.md)

*整数* の範囲は \[ -2,147,483,647: 2,147,483,647\] です。 この範囲内のすべての整数はリテラルとして使用できます。

すべての比較演算子と算術 [演算子](er-formula-language.md#Operators) は *整数* データ型と共に使用できます 。

## <a name="int64"></a><a name="int64"></a>Int64

*int64* プリミティブ データ型は、小数点以下の桁数を持たない数値を表します。 *int64* 値は、繰り返しのステートメントの制御変数またはレコード識別子として使用されます。

*int64* は 64 ビット幅です。 既定値は、**0** で、内部表示は、長い番号です。 *int64* は自動的に *実数* に変換されます。

さらに、次の明示的な変換関数を使用できます。

- [INT64VALUE](er-functions-conversion-int64value.md)
- [NUMBERFORMAT](er-functions-text-numberformat.md)
- [TEXT](er-functions-text-text.md)

*int64* の範囲は \[-9,223,372,036,854,775,807: 9,223,372,036,854,775,807\] です。

すべての比較演算子と算術 [演算子](er-formula-language.md#Operators) は *int64* データ型と共に使用できます。

## <a name="real"></a><a name="real"></a>実績

*実数* 変数は、整数に加えて小数値を保持できます。 10 進リテラル は *実数* が予期される場所ではどこでも使用することができます。 10 進数リテラルは、**2.19** のように、コードで直接入力された 10 進数です。

> [!NOTE]
> ER 式では、ピリオド (.) が常に小数点として使用されます。

Reals はすべての式で使用することができ、比較演算子と算術演算子の両方と共に使用できます。 *実数* は、16桁の有効な数値の精度があります。 *real* の既定値は **0.0** で、内部表示はバイナリコード化されたデジタル (BCD) 番号です。 BCD エンコードにより、0.1 の倍数の値の正確な表現が可能になります。 *実数* 変数の範囲は、-(10)<sup>127</sup> から (10)<sup>127</sup> です。 この範囲内のすべての実数は ER 式でリテラルとして使用できます。

*実数* に暗黙的な変換はありません。 ただし、次の関数を使用して *実数* を他のデータ型に明示的に変換し、その他のデータ型を *実数* に変換することもできます。

- [INTVALUE](er-functions-conversion-intvalue.md)
- [INT64VALUE](er-functions-conversion-int64value.md)
- [NUMBERFORMAT](er-functions-text-numberformat.md)
- [TEXT](er-functions-text-text.md)
- [VALUE](er-functions-conversion-value.md)

すべての比較演算子と算術 [演算子](er-formula-language.md#Operators) は *実数* データ型と共に使用できます。

## <a name="string"></a><a name="string"></a>文字列

*文字列* プリミティブ データ型は、テキスト、アカウント番号、住所、電話番号として使用される文字のシーケンスを表します。

*文字列* リテラルは引用符 ("") で囲まれた文字です。 *文字列* の値が ER 式に必要な場合はいつでも、*文字列* リテラルを使用することができます。 比較などの論理式では文字列を使用することができます。 **\&** 演算子または [CONCATENATE](er-functions-text-concatenate.md) 関数を使用して、*文字列* の値を連結することもできます。

> [!NOTE]
> 2 つの *文字列* 値を連結し、結果の *文字列* を複数の行にまたがたい場合は、値の間に改行区切りを使用します。 TEXT 出力の場合、この区切り文字は [CHAR](er-functions-text-char.md)(10) または CHAR(13) 式を使用して生成される文字にすることができます。 HTML の場合は、**\<br\>** タグにできます 。

*文字列* の既定値は、文字を含む空白のテキスト文字列で、内部表現は文字のリストです。

文字列の自動変換はありません。 ただし、次の明示的な変換関数を使用できます。

- [CHAR](er-functions-text-char.md)
- [FORMAT](er-functions-text-format.md)
- [LEFT](er-functions-text-left.md)
- [LEN](er-functions-text-len.md)
- [MID](er-functions-text-mid.md)
- [PADLEFT](er-functions-text-padleft.md)
- [REPLACE](er-functions-text-replace.md)
- [RIGHT](er-functions-text-right.md)
- [TEXT](er-functions-text-text.md)
- [TRANSLATE](er-functions-text-translate.md)
- [TRIM](er-functions-text-trim.md)
- [UPPER](er-functions-text-upper.md)

*文字列* の値の変換については、[テキスト カテゴリーの ER 関数一覧](er-functions-category-text.md) を参照してください。

*文字列* は、無制限の文字数を保持できます。

すべての比較 [演算子](er-formula-language.md#Operators) は *文字列* データ型と共に使用できます。

## <a name="additional-resources"></a>追加リソース

- [電子申告の概要](general-electronic-reporting.md)
- [電子報告のフォーミュラ言語](er-formula-language.md)
- [対応している複合データ型](er-formula-supported-data-types-composite.md)
