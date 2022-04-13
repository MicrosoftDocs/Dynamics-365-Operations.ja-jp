---
title: GETLABELTEXT ER 関数
description: このトピックでは、GETLABELTEXT 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 03/18/2022
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-01-01
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: 2ce66c9410abeee16bbd074204262edf79bf6d68
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462414"
---
# <a name="getlabeltext-er-function"></a>GETLABELTEXT ER 関数

[!include [banner](../includes/banner.md)]

`GETLABELTEXT` 関数は、特定のラベルを検索して、指定したラベルの翻訳を表す *[文字列](er-formula-supported-data-types-primitive.md#string)* 値を指定した言語で返します。

## <a name="syntax"></a>構文

```vb
GETLABELTEXT (label id, language)
```

## <a name="arguments"></a>引数

### <a name="label-id"></a>ラベル ID

`label id`: *文字列* または *ラベル ID*

次のいずれかのラベル タイプの有効なID:

- [電子申告 (ER)](general-electronic-reporting.md) ラベル
- Microsoft Dynamics 365 Finance ラベル

#### <a name="usage-notes"></a>使用上の注意

この引数は、次のサポートされているパターンのいずれかを使用して、定数としてのみ定義できます。

- ER ラベルの場合:

    - `@"GER_LABEL:<LABEL ID>"`
    - `"GER_LABEL:<LABEL ID>"`

- 財務ラベルの場合:

    - `@"<LABEL ID>"`
    - `"<LABEL ID>"`

> [!NOTE]
> 指定したラベル ID を使用してもラベルが見つからない場合は、デザイン時に **[フォーミュラ デザイナー](er-advanced-formula-editor.md)** ページに検証エラー メッセージが表示されます。

### <a name="language"></a>言語

`language`: *文字列*

言語コードを表す文字列。

#### <a name="usage-notes"></a>使用上の注意

この引数は、テキスト定数として、または *文字列* 値を返すデータ ソース フィールドのパスとして定義できます。

> [!NOTE]
> テキスト定数として定義されているときに、指定した `language` 引数を使用しても言語コードが見つからない場合は、デザイン時に検証エラー メッセージが表示されます。
>
> 実行時に、指定した `EN-US` 引数を使用しても言語コードが見つからない場合、`language` システム言語に対する翻訳が指定されたラベルに対して返されます。

## <a name="return-values"></a>戻り値

*文字列*

結果テキスト値。

## <a name="example-1-system-label"></a><a name=example-1></a>例 1: システム ラベル

式 `GETLABELTEXT (@"SYS70894", "en-us")` と `GETLABELTEXT ("SYS70894", "en-us")` は、`@SYS70894` アプリケーション ラベルの英語訳 "Nothing to print" を返します。

## <a name="example-2-er-label"></a><a name=example-2></a>例 2: ER ラベル

**ISO20022 口座振替 (DE)** の構成から [派生](er-quick-start2-customize-report.md#DeriveProvidedFormat) したER [構成](general-electronic-reporting.md#Configuration) の編集、*[計算フィールド](er-calculated-field-ds-performance.md)* 型の新しいデータ ソースの入力、およびこのデータ ソースの式 `GETLABELTEXT(@"GER_LABEL:VendorName", "de")` の構成を開始します。 この場合、データ ソースは実行時に、基準の **ISO20022 口座振替 (DE)** ER 構成で最初に構成された `@GER_LABEL:VendorName` ER ラベルのドイツ語訳 "Kreditorenname" を返します。

## <a name="additional-resources"></a>追加リソース

[テキスト関数](er-functions-category-text.md)

[電子申告における多言語レポートの設計](er-design-multilingual-reports.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
