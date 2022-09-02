---
title: 消費税の計算と丸め
description: この記事では、売上税計算と丸めについて概説し、売上税計算および丸め設定のパラメーターについて説明します。
author: wangchen
ms.date: 06/01/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom:
- "13111"
- intro-internal
ms.assetid: fe5fdc7f-9834-49fb-a611-1dd9c289619d
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2022-05-31
ms.dyn365.ops.version: AX 10.0.28
ms.openlocfilehash: aa3564f0fcf4a958637ba4a5cdcc497bffc50000
ms.sourcegitcommit: 8b716849707ec96d1cb4cac85b9e782dc25f5a70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/07/2022
ms.locfileid: "8939236"
---
# <a name="sales-tax-calculation-and-rounding"></a>消費税の計算と丸め

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Finance での売上税計算と丸めについての概要を説明します。 また、売上税の計算と丸め設定の設定で使用されるパラメーターと、これらのパラメーターの組み合わせで使用される方法について説明します。

## <a name="parameters"></a>パラメーター

いくつかのパラメーターは、売上税の計算と丸めを制御します。

- **計算方法** – このパラメーターは、**総勘定元帳のパラメーター** ページで設定され、税基準額をドキュメントごとに計算するか、行ごとに計算するか定義します。 売上税コードの **基準金額** パラメーターが **請求書残高の正味金額** に設定されている場合、このパラメーターの設定に関係なく、税基準額は常にドキュメントごとに計算されます。
- **丸め方法** – このパラメーターは、売上税グループに対して設定され、税額を売上税コードごとに丸めるか、売上税コードの組み合わせごとに丸めるかを定義します。
- **発生元** – このパラメーターは、売上税コードに対して設定され、税額の計算方法を定義します。 詳細については、[[発生元] フィールドでの売上税計算方法](sales-tax-calculation-methods-origin-field.md) を参照して下さい。
- **基準金額** – このパラメーターは、売上税コード向けに設定されており、**売上税コード値** ページから適切な税率をピッキングするのにどの金額が使用されるかを決定します。 詳細については、[基準金額および計算方法フィールドに基づいた、売上税の税率](marginal-base-field.md) を参照して下さい。
- **売上税丸めルール** – このパラメーターは、売上税コードに対して設定され、丸め桁数や丸め方法など、特定の売上税金額の丸め方法を定義します。

この記事の残りの部分では、売上税計算およびこれらのパラメーターの組み合わせを使用する丸め処理の一般的な例を示します。

## <a name="scenario-for-the-examples"></a>サンプルのシナリオ

- 課税対象ドキュメントには 2 行あるので、各明細行の税基準額は 42.42 です。
- 行ごとに 2 つの売上税コード (売上税コード 1 と売上税コード 2) が定義されます。
- 税コード 1 と税コード 2 の両方の税率が 10% です。
- 価格は税抜です。
- 丸め精度は 0.01 です。
- 丸め方法は **切り上げ** です。

## <a name="example-1"></a>例 1

### <a name="parameter-values"></a>パラメーター値

| 計算方法 | 丸めの方法    | 元                   | 基準金額       |
| ------------------ | -------------- | ------------------------ | ------------------- |
| 明細行               | 消費税コード | 正味金額の割合 | ラインごとの正味金額 |

### <a name="calculation-and-rounding-behavior"></a>計算と丸めビヘイビアー

| 行番号 | 消費税コード | 元金額 | 売上税金額 |
| ------------| ---------------| --------------| -----------------|
| 1           | コード 1         | 42.42         | 4.25             |
| 1           | コード 2         | 42.42         | 4.25             |
| 2           | コード 1         | 42.42         | 4.25             |
| 2           | コード 2         | 42.42         | 4.25             |

税の基準金額は行ごとに計算されます:

- **行 1:** 42.42
- **行 2:** 42.42

税は、売上税コードごとに計算されます:

- **行 1:**

    - 売上税コード 1 の税額 = 42.42 &times; 10% = 4.242
    - 売上税コード 2 の税額 = 42.42 &times; 10% = 4.242

- **行 2:**

    - 売上税コード 1 の税額 = 42.42 &times; 10% = 4.242
    - 売上税コード 2 の税額 = 42.42 &times; 10% = 4.242

税は、売上税コードごとに丸められます:

- **行 1:**

    - 売上税コード 1 の丸められた税額 = 4.25
    - 売上税コード 2 の丸められた税額 = 4.25

- **行 2:**

    - 売上税コード 1 の丸められた税額 = 4.25
    - 売上税コード 2 の丸められた税額 = 4.25

## <a name="example-2"></a>例 2

### <a name="parameter-values"></a>パラメーター値

| 計算方法 | 丸めの方法    | 元                   | 基準金額                 |
| ------------------ | -------------- | ------------------------ | ----------------------------- |
| 行/合計         | 消費税コード | 正味金額の割合 | 請求書残高の正味金額 |

### <a name="calculation-and-rounding-behavior"></a>計算と丸めビヘイビアー

| 行番号 | 消費税コード | 元金額 | 売上税金額 |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | コード 1         | 42.42         | 4.25             |
| 1           | コード 2         | 42.42         | 4.25             |
| 2           | コード 1         | 42.42         | 4.24             |
| 2           | コード 2         | 42.42         | 4.24             |

税の基準金額はドキュメントごとに計算されます:

- 税基準額 = 42.42 + 42.42 = 84.84

税は、売上税コードごとに計算されます:

- 売上税コード 1 の税額 = 84.84 &times; 10% = 8.484
- 売上税コード 2 の税額 = 84.84 &times; 10% = 8.484

税は、売上税コードごとに丸められます:

- 売上税コード 1 の丸められた税額 = 8.49
- 売上税コード 2 の丸められた税額 = 8.49

丸められた税額は、売上税コードごとの各行に割り当てられます:

- 売上税コード 1 (8.49) の丸めた税額を行 1 (4.25) および行 2 (4.24) に割り当てます。
- 売上税コード 2 (8.49) の丸めた税額を行 1 (4.25) および行 2 (4.24) に割り当てます。

## <a name="example-3"></a>例 3

### <a name="parameter-values"></a>パラメーター値

| 計算方法 | 丸めの方法    | 元                              | 基準金額       |
| ------------------ | -------------- | ----------------------------------- | ------------------- |
| 明細行               | 消費税コード | 計算済正味金額の割合 | ラインごとの正味金額 |

### <a name="calculation-and-rounding-behavior"></a>計算と丸めビヘイビアー

| 行番号 | 消費税コード | 元金額 | 売上税金額 |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | コード 1         | 42.42         | 4.72             |
| 1           | コード 2         | 42.42         | 4.72             |
| 2           | コード 1         | 42.42         | 4.72             |
| 2           | コード 2         | 42.42         | 4.72             |

税の基準金額は行ごとに計算されます:

- **行 1:** 42.42
- **行 2:** 42.42

税は、売上税コードごとに計算されます:

- **行 1:**

    - 売上税コード 1 の税額 = 42.42 &times; 10% &divide; (1 – 10 %) = 4.7133
    - 売上税コード 2 の税額 = 42.42 &times; 10% &divide; (1 – 10 %) = 4.7133

- **行 2:**

    - 売上税コード 1 の税額 = 42.42 &times; 10% &divide; (1 – 10 %) = 4.7133
    - 売上税コード 2 の税額 = 42.42 &times; 10% &divide; (1 – 10 %) = 4.7133

税は、売上税コードごとに丸められます:

- **行 1:**

    - 売上税コード 1 の丸められた税額 = 4.72
    - 売上税コード 2 の丸められた税額 = 4.72

- **行 2:**

    - 売上税コード 1 の丸められた税額 = 4.72
    - 売上税コード 2 の丸められた税額 = 4.72

## <a name="example-4"></a>例 4

### <a name="parameter-values"></a>パラメーター値

| 計算方法 | 丸めの方法    | 元                              | 基準金額                 |
| ------------------ | -------------- | ----------------------------------- | ----------------------------- |
| 行/合計         | 消費税コード | 計算済正味金額の割合 | 請求書残高の正味金額 |

### <a name="calculation-and-rounding-behavior"></a>計算と丸めビヘイビアー

| 行番号 | 消費税コード | 元金額 | 売上税金額 |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | コード 1         | 42.42         | 4.72             |
| 1           | コード 2         | 42.42         | 4.72             |
| 2           | コード 1         | 42.42         | 4.71             |
| 2           | コード 2         | 42.42         | 4.71             |

税の基準金額はドキュメントごとに計算されます:

- 税基準額 = 42.42 + 42.42 = 84.84

税は、売上税コードごとに計算されます:

- 売上税コード 1 の税額 = 84.84 &times; 10% &divide; (1 – 10 %) = 9.4267
- 売上税コード 2 の税額 = 84.84 &times; 10% &divide; (1 – 10 %) = 9.4267

税は、売上税コードごとに丸められます:

- 売上税コード 1 の丸められた税額 = 9.43
- 売上税コード 2 の丸められた税額 = 9.43

丸められた税額は、売上税コードごとの各行に割り当てられます:

- 売上税コード 1 (9.43) の税額を行 1 (4.72) および行 2 (4.71) に割り当てます。
- 売上税コード 2 (9.43) の税額を行 1 (4.72) および行 2 (4.71) に割り当てます。

## <a name="example-5"></a>例 5

### <a name="parameter-values"></a>パラメーター値

| 計算方法 | 丸めの方法                | 元                   | 基準金額       |
| ------------------ | -------------------------- | ------------------------ | ------------------- |
| 明細行               | 消費税コードの組み合わせ | 正味金額の割合 | ラインごとの正味金額 |

### <a name="calculation-and-rounding-behavior"></a>計算と丸めビヘイビアー

| 行番号 | 消費税コード | 元金額 | 売上税金額 |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | コード 1         | 42.42         | 4.25             |
| 1           | コード 2         | 42.42         | 4.24             |
| 2           | コード 1         | 42.42         | 4.24             |
| 2           | コード 2         | 42.42         | 4.24             |

税の基準金額は行ごとに計算されます:

- **行 1:** 42.42
- **行 2:** 42.42

税は、売上税コードごとに計算されます:

- **行 1:**

    - 売上税コード 1 の税額 = 42.42 &times; 10% = 4.242
    - 売上税コード 2 の税額 = 42.42 &times; 10% = 4.242

- **行 2:**

    - 売上税コード 1 の税額 = 42.42 &times; 10% = 4.242
    - 売上税コード 2 の税額 = 42.42 &times; 10% = 4.242

税は、売上税コードの組み合わせごとに丸められます:

- 売上税金額の合計 = 4.242 + 4.242 + 4.242 + 4.242 = 16.968、この値は 16.97 に切り上げられます

丸められた税額は、売上税コードごとの各行に割り当てられます:

- 売上税金額 (16.97) を行 1 および行 2 に割り当てます:

    - **行 1:**

        - 売上税コード 1 の税額 = 4.25
        - 売上税コード 2 の税額 = 4.24

    - **行 2:**

        - 売上税コード 1 の税額 = 4.24
        - 売上税コード 2 の税額 = 4.24

## <a name="example-6"></a>例 6

### <a name="parameter-values"></a>パラメーター値

| 計算方法 | 丸めの方法                | 元                   | 基準金額                 |
| ------------------ | -------------------------- | ------------------------ | ----------------------------- |
| 行/合計         | 消費税コードの組み合わせ | 正味金額の割合 | 請求書残高の正味金額 |

### <a name="calculation-and-rounding-behavior"></a>計算と丸めビヘイビアー

| 行番号 | 消費税コード | 元金額 | 売上税金額 |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | コード 1         | 42.42         | 4.25             |
| 1           | コード 2         | 42.42         | 4.24             |
| 2           | コード 1         | 42.42         | 4.24             |
| 2           | コード 2         | 42.42         | 4.24             |

税の基準金額はドキュメントごとに計算されます:

- 税基準額 = 42.42 + 42.42 = 84.84

税は、売上税コードごとに計算されます:

- 売上税コード 1 の税額 = 84.84 &times; 10% = 8.484
- 売上税コード 2 の税額 = 84.84 &times; 10% = 8.484

税は、売上税コードの組み合わせごとに丸められます:

- 売上税金額の合計 = 8.484 + 8.484 = 16.968、この値は 16.97 に切り上げられます

丸められた税額は、売上税コードごとの各行に割り当てられます:

- 売上税金額 (16.97) を行 1 および行 2 に割り当てます:

    - **行 1:**

        - 売上税コード 1 の税額 = 4.25
        - 売上税コード 2 の税額 = 4.24

    - **行 2:**

        - 売上税コード 1 の税額 = 4.24
        - 売上税コード 2 の税額 = 4.24

## <a name="example-7"></a>例 7

### <a name="parameter-values"></a>パラメーター値

| 計算方法 | 丸めの方法                | 元                              | 基準金額       |
| ------------------ | -------------------------- | ----------------------------------- | ------------------- |
| 明細行               | 消費税コードの組み合わせ | 計算済正味金額の割合 | ラインごとの正味金額 |

### <a name="calculation-and-rounding-behavior"></a>計算と丸めビヘイビアー

| 行番号 | 消費税コード | 元金額 | 売上税金額 |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | コード 1         | 42.42         | 4.72             |
| 1           | コード 2         | 42.42         | 4.71             |
| 2           | コード 1         | 42.42         | 4.71             |
| 2           | コード 2         | 42.42         | 4.72             |

税の基準金額は行ごとに計算されます:

- **行 1:** 42.42
- **行 2:** 42.42

税は、売上税コードごとに計算されます:

- **行 1:**

    - 売上税コード 1 の税額 = 42.42 &times; 10% &divide; (1 – 10 %) = 4.7133
    - 売上税コード 2 の税額 = 42.42 &times; 10% &divide; (1 – 10 %) = 4.7133

- **行 2:**

    - 売上税コード 1 の税額 = 42.42 &times; 10% &divide; (1 – 10 %) = 4.7133
    - 売上税コード 2 の税額 = 42.42 &times; 10% &divide; (1 – 10 %) = 4.7133

税は、売上税コードの組み合わせごとに丸められます:

- 売上税金額の合計 = 4.7133 + 4.7133 + 4.7133 + 4.7133 = 18.8532、この値は 18.86 に切り上げられます

丸められた税額は、売上税コードごとの各行に割り当てられます:

- 売上税金額 (18.86) を行 1 および行 2 に割り当てます:

    - **行 1:**

        - 売上税コード 1 の税額 = 4.72
        - 売上税コード 2 の税額 = 4.71

    - **行 2:**

        - 売上税コード 1 の税額 = 4.71
        - 売上税コード 2 の税額 = 4.72

## <a name="example-8"></a>例 8

### <a name="parameter-values"></a>パラメーター値

| 計算方法 | 丸めの方法                | 元                              | 基準金額                 |
| ------------------ | -------------------------- | ----------------------------------- | ----------------------------- |
| 行/合計         | 消費税コードの組み合わせ | 計算済正味金額の割合 | 請求書残高の正味金額 |

### <a name="calculation-and-rounding-behavior"></a>計算と丸めビヘイビアー

| 行番号 | 消費税コード | 元金額 | 売上税金額 |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | コード 1         | 42.42         | 4.72             |
| 1           | コード 2         | 42.42         | 4.71             |
| 2           | コード 1         | 42.42         | 4.71             |
| 2           | コード 2         | 42.42         | 4.72             |

税の基準金額はドキュメントごとに計算されます:

- 税基準額 = 42.42 + 42.42 = 84.84

税は、売上税コードごとに計算されます:

- 売上税コード 1 の税額 = 84.84 &times; 10% &divide; (1 – 10 %) = 9.4267
- 売上税コード 2 の税額 = 84.84 &times; 10% &divide; (1 – 10 %) = 9.4267

税は、売上税コードの組み合わせごとに丸められます:

- 売上税金額の合計 = 9.4267 + 9.4267 = 18.8534、この値は 18.86 に切り上げられます

丸められた税額は、売上税コードごとの各行に割り当てられます:

- 売上税金額 (18.86) を行 1 および行 2 に割り当てます:

    - **行 1:**

        - 売上税コード 1 の税額 = 4.72
        - 売上税コード 2 の税額 = 4.71

    - **行 2:**

        - 売上税コード 1 の税額 = 4.71
        - 売上税コード 2 の税額 = 4.72

## <a name="additional-resources"></a>追加リソース

- [[発生元] フィールドでの消費税計算方法](sales-tax-calculation-methods-origin-field.md)
- [基準金額および計算方法に基づいた、売上税の税率](marginal-base-field.md)
- [消費税コードの合計額と間隔計算オプション](whole-amount-interval-options-sales-tax-codes.md)