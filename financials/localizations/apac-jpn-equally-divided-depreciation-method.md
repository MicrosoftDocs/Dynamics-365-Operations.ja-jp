---
title: "均等減価償却法"
description: "日本では、一括比例配分資産、低価額資産、および繰延資産は耐用年数期間中、毎年均等額で減価償却されます。 この記事は、均等減価償却についてよく寄せられる質問に回答します。"
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 10154
ms.assetid: da3d689f-3625-4896-a74a-7890e4fa26eb
ms.search.region: Japan
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f7fd20ef0c78bc781f0ef9f17fc612723906ac78
ms.openlocfilehash: a003b4d6aa7980e651315f28e3c89a8b509c47ff
ms.lasthandoff: 03/31/2017


---

# <a name="equally-divided-depreciation-method"></a>均等減価償却法

[!include[banner](../includes/banner.md)]


日本では、一括比例配分資産、低価額資産、および繰延資産は耐用年数期間中、毎年均等額で減価償却されます。 この記事は、均等減価償却についてよく寄せられる質問に回答します。

均等償却予定表で、固定資産の耐用年数内の 1 つまたは複数の会計年度期間の、繰延、少額、または一括比例配分の固定資産を均等減価償却できます。 **減価償却プロファイル** ページで均等減価償却法を設定できます。

## <a name="what-types-of-fixed-assets-can-i-depreciate-by-using-the-equally-divided-depreciation-method"></a>均等減価償却法を使用して、どの固定資産の種類を減価償却できますか。
均等減価償却法を使用して、繰延、少額、および一括比例配分の固定資産を減価償却できます。 次に、一つ以上の会計年度期間における資産の減価償却費を表示するレポートを生成できます。

## <a name="how-is-depreciation-calculated-using-the-equally-divided-depreciation-method"></a>均等減価償却法を使用して、どのように減価償却を計算しますか。
**減価償却プロファイル** ページの [**方式**] フィールドで、減価償却方法として [**均等**] を選択して、減価償却プロファイルを設定できます。 均等減価償却プロファイルを使用して固定資産を減価償却するとき、Microsoft Dynamics 365 for Operations は次の式を使用して減価償却金額を計算します。減価償却 = 残余量 × 四捨五入した (1 ÷ 残りの年数) × 四捨五入した (1 ÷ 現在の年の期間数)。次の式は、残りの量の計算に使用します。残余量 = 取得コスト – 減価償却累計額。減価償却量の計算に均等減価償却法を使用するとき、**減価償却プロファイル** ページの [**均等償却年数**] フィールドの値は、**帳簿** ページで指定した耐用年数および減価償却期間ではなく、固定資産の耐用年数が表示されます。

## <a name="does-the-depreciation-amount-that-is-calculated-by-using-the-equally-divided-depreciation-method-change-if-its-calculated-at-the-beginning-of-the-month-instead-of-in-the-middle-of-the-month"></a>均等減価償却法を使用して計算された減価償却量は、月の中間に計算された場合ではなく月初めに計算された場合に異なりますか。
一連番号 減価償却量は、月内のいつ計算されるかによって変化しません。 たとえば、以下の一括比例配分の固定資産を取得します。

-   一括比例配分の固定資産の取得値 = 150,000 円 (JPY)
-   取得日付 = April 1, 2013
-   均等減価償却量に対する年数 = 3 年

均等減価償却法を使用すると、計算が月初めまたは月の中間にかかわらず、この固定資産の各月の減価償却量は JPY 4,166.67 です。

## <a name="how-is-equally-divided-depreciation-calculated-for-a-lowvalue-asset-that-is-acquired-midyear"></a>年の中ごろに取得された低価格資産の均等減価償却を、どのように計算しますか。
会計年度の中ごろに低価額の固定資産を購入した場合、Microsoft Dynamics 365 for Operations は、現在の会計年度を減価償却計算の最初の会計年度であると仮定します。 たとえば、会計年度の中ごろに、低価額の固定資産を取得します。

-   会計年度 = 4 月 1 日から 3 月 31 日
-   低価格固定資産の取得値 = JPY 100,000
-   取得日付け= 2012 年 12 月 1 日
-   均等減価償却量に対する年数 = 1 年

次の表に示されているように、Microsoft Dynamics AX は 2012 年 4 月 1 日から 2013 年 3 月 31 日までの会計年に対し、減価償却を計算します。

| 開始日    | 終了日       | 会計年度期間の減価償却量 | 減価償却累計額 | 残りの減価償却量 | その月の減価償却量 |
|---------------|----------------|-------------------------------------------|--------------------------|-------------------------------|-----------------------------------|
| 2012 年 4 月 1 日 | 2013 年 3 月 31 日 | JPY 100,000                               | JPY 100,000              | 0                             | JPY 100,000                      |

## <a name="how-is-equally-divided-depreciation-calculated-for-a-lumpsum-asset-that-is-acquired-midyear"></a>年の中ごろに取得された一括比例配分資産の均等減価償却を、どのように計算しますか。
会計年度の中ごろに一括比例配分の固定資産を購入した場合、Microsoft Dynamics 365 for Operations は固定資産の購買日付から現在の会計年度を計算します。 たとえば、会計年度の中ごろに、一括比例配分の固定資産を取得します。

-   会計年度 = 4 月 1 日から 3 月 31 日
-   一括比例配分の固定資産の取得値 = JPY 150,000
-   取得日付け= 2012 年 12 月 1 日
-   均等減価償却量に対する年数 = 3 年

次の表に示されているように、Microsoft Dynamics AX は 2012 年 12 月 1 日から 2013 年 3 月 31 日までの最初の年に対し、減価償却を計算します。

| 開始日       | 終了日       | 会計年度期間の減価償却量 | 減価償却累計額 | 残りの減価償却量 | 月の減価償却量 |
|------------------|----------------|-----------------------------------------|--------------------------|-------------------------------|---------------------------------|
| 2012 年 12 月 1 日 | 2013 年 3 月 31 日 | JPY 50,000                              | JPY 50,000               | JPY 100,000                   | JPY 12,500                      |
| 2013 年 4 月 1 日    | 2014 年 3 月 31 日 | JPY 50,000                              | JPY 100,000              | JPY 50,000                    | JPY 4,167                       |
| 2014 年 4 月 1 日    | 2015 年 3 月 31 日 | JPY 50,000                              | JPY 150,000              | 0                             | JPY 4,167                       |

## <a name="how-is-depreciation-calculated-using-the-equally-divided-depreciation-method-if-the-asset-calendar-is-changed-during-the-asset-life-cycle"></a>試算カレンダーが資産の有効期間中に変更される場合、均等減価償却法を使用してどのように減価償却を計算しますか。
Microsoft Dynamics 365 for Operations が均等減価償却法を使用して減価償却を計算する場合、**帳簿**ページの [**カレンダー**] フィールドで選択された会計カレンダーに基づいて計算されます。 資産カレンダーが資産の有効期間中に変更された場合、現在のカレンダーに基づいて、会計年度内の月または四半期などの会計年度期間の数を計算します。 たとえば、以下の一括比例配分の固定資産を取得します。

-   会計カレンダー = 4 月 1 日から 3 月 31 日
-   一括比例配分の固定資産の取得日付 = 2012 年 4 月 1 日
-   均等減価償却量に対する年数 = 3 年

2013 年 4 月、第 2 会計年度中に、会計カレンダー 4 月 1 日～ 3 月 31 日を 1 月 1 日～ 12 月 31 日に変更すると、次の表のように会計年度の減価償却期間の数が計算されます。

| 年度                                | 減価償却期間の数 |
|--------------------------------------------|--------------------------------|
| 2012 年 4 月 1 日～ 2013 年 3 月 31 日      | 12 期間                     |
| 2013 年 4 月 1 日～2013 年 12 月 31 日   | 9 期間                      |
| 2014 年 1 月 1 日～2014 年 12 月 31 日 | 12 期間                     |
| 2015 年 1 月 1 日～ 2015 年 3 月 31 日    | 3 期間                      |

## <a name="can-i-modify-the-equally-divided-depreciation-method-during-the-life-cycle-of-a-fixed-asset"></a>固定資産の有効期間中に均等減価償却法を変更できますか。
一連番号 均等減価償却法を使用して固定資産を減価償却するとき、減価償却量は、固定資産の耐用期間内の会計年度期間中に均等分割されます。 したがって、固定資産の有効期間中は減価償却方法を変更できません。

## <a name="can-i-change-the-depreciation-period-for-an-equally-divided-depreciation-profile"></a>均等減価償却法プロファイルの減価償却期間を変更できますか。
一連番号 **減価償却簿**ページで均等減価償却法プロファイルを選択した場合、減価償却プロファイルの**減価償却プロファイル** ページの [**均等償却年数**] フィールドの値は変更できません。

<a name="see-also"></a>参照
--------

[固定資産減価償却の FAQ](apac-jpn-fixed-asset-depreciation.md)




