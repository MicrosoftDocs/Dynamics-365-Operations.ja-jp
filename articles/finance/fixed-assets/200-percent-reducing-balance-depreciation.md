---
title: 200% 逓減残高による減価償却
description: この記事では、減価償却の 200% 逓減残高法の概要を説明します。
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: kfend
ms.custom: 13951
ms.assetid: 69b4e010-7683-4dc2-8a06-6d572f37e903
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7abcf26f3e658e8a6f451f26240890d183547982
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870165"
---
# <a name="200-percent-reducing-balance-depreciation"></a>200% 逓減残高による減価償却

[!include [banner](../includes/banner.md)]

この記事では、減価償却の 200% 逓減残高法の概要を説明します。

固定資産減価償却プロファイルを設定し、**減価償却プロファイル** ページの **方法** フィールドで **200% 逓減残高** を選択すると、この減価償却プロファイルが割り当てられる固定資産の減価償却に、各減価償却期間で同じ比率が適用されます。 この比率は資産の耐用年数に基づいて計算されます。 たとえば、資産の耐用年数が 5 年の場合は、比率が 40% (200% ÷ 5) として計算されます。 

この方法は倍額定率法とも呼ばれます。

200% 逓減残高による減価償却を設定するには、**減価償却プロファイル** ページの **償却年** フィールドと **期間の頻度** フィールドでオプションを選択します。 **期間の頻度** フィールドで使用できるオプションは、**償却年** フィールドで選択した値によって異なります。

## <a name="select-a-depreciation-year"></a>償却年の選択
**減価償却プロファイル** ページの **償却年** フィールドで **暦年** または **会計年度** のいずれかを選択できます。 既定値は **暦年** です。 

この選択により、**期間の頻度** フィールドで指定できるオプションが決まります。 このフィールドによって、暦年を通した償却発生額の転記日付と金額が定義されます。

### <a name="calendar"></a>カレンダー

**償却年** フィールドの既定値である **暦年** をそのまま使用できます。 

**暦年** 選択すると、毎年 1 月 1 日に償却基礎額が更新されます。 通常、減価償却は、正味簿価額から仕損価格を差し引いた額です。 この記事の後の例では、計算列の最初の式の分子が減価償却基準です。 

償却年として **暦年** を選択すると、**期間の頻度** フィールドで次のオプションが使用できます。

-   **年 1 回** を選択すると、12 月 31 日に金額が転記されます。
-   **月 1 回** を選択すると、各カレンダー月の最終日に 1 か月分の金額が転記されます。
-   **四半期に 1 回** を選択すると、各四半期の最終日 (3 月 31 日、6 月 30 日、9 月 30 日、および 12 月 31 日) に、四半期分の金額が転記されます。
-   **半期に 1 回** を選択すると、暦年の半年の最終日 (6 月 30 日と 12 月 31 日) に半年分の金額が転記されます。
-   **毎日** を選択すると、減価償却方法を毎日に設定した場合の減価償却金額は、毎日 1 件のトランザクションを使用して転記されます。

### <a name="fiscal"></a>会計年度

**償却** 年フィールドで **会計年度** を選択した場合、200% 逓減残高による減価償却は、帳簿で指定した会計カレンダーまたは **元帳** ページで選択した会計カレンダーの会計年度に基づいて計算されます。 会計カレンダーは、**会計カレンダー** ページで設定します。 

たとえば、会計年度 7 月 1 日から 6 月 30 日の場合、減価償却計算は 7 月 1 日に開始されます。 会計年度の期間は 12 か月よりも長くすることも短くすることもできます。 減価償却は各年度期間に合わせて調整されます。 次の会計年度の長さは **会計カレンダー** ページで設定された期間で決定されます。 

償却年として **会計年度** を選択すると、**期間の頻度** フィールドで次のオプションが使用できます。

-   **年 1 回** を選択すると、会計年度に対して計算された減価償却の合計量が、会計年度の最終日に 1 つの量として転記されます。
-   **会計年度期間** では、会計年度に対して計算された減価償却の合計額が会計年度の最終日に転記されます。 この金額は **会計カレンダー** ページで定義された会計年度期間に見越計上されます。

## <a name="example-of-200-reducing-balance-depreciation"></a>200% 逓減残高による減価償却の例

| &nbsp;                         | &nbsp; |
|--------------------------------|--------|
| 取得価額               | 11,000 |
| 救済価格                  | 1, 000 |
| 償却基礎額              | 10,000 |
| 耐用年数             | 5      |
| 年次減価償却率 | 40%    |

200% 逓減残高法では、200% を耐用年数で除算します。 この比率は、資産の正味簿価額で乗算され、各年の減価償却金額が決まります。

| 期間 | 年次減価償却額の計算 | 簿価額             | 年末の正味簿価額 |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| 年 1 | (11,000 – 1,000) × 40% = 4,000                | 11,000 – 4,000 = 7,000 | 11,000 – 1,000 – 4,000 = 6,000        |
| 年 2 | 6,000 × 40% = 2,400                           | 7,000 – 2,400 = 4,600  | 6,000 – 2,400 = 3,600                 |
| 年 3 | 3,600 × 40% = 1,440                           | 4,600 – 1,440 = 3,160  | 3,600 – 1,440 = 2,160                 |

> [!NOTE] 
> 通常、200 =% 逓減残高による減価償却法を使用して計算した金額が、定額法を使用して計算した金額より低くなる場合、残存耐用年数は定額法に換算されます。





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
