---
title: 日本の固定資産減価償却のよく寄せられる質問
description: この記事は、日本の固定資産の減価償却についてよく寄せられる質問に回答します。
author: EricWangChen
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile, AssetDepRate_JP
audience: Application User
ms.reviewer: kfend
ms.custom: 10294
ms.search.region: Japan
ms.author: wangchen
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9a4edec8e9247a5896a7164f3625f89f558ea709
ms.sourcegitcommit: 49f29aaa553eb105ddd5d9b42529f15b8e64007e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/01/2021
ms.locfileid: "7592647"
---
# <a name="fixed-asset-depreciation-for-japan-faq"></a>日本の固定資産減価償却のよく寄せられる質問

[!include [banner](../includes/banner.md)]

この記事は、日本の固定資産の減価償却についてよく寄せられる質問に回答します。

固定資産は、耐用期間中に償却されます。 そのため、固定資産の取得金額は、減少します。 固定資産の減価償却を調整するには、資産がサービスに分類された日付に基づいて、以下の減価償却方法のいずれかを割当てる必要があります。

-   **旧定額法** – 2007 年 4 月 1 日より前にサービスに投入された資産を償却します。
-   **定額法** – 2007 年 4 月 1 日以後にサービスに投入された資産を償却します。
-   **旧定率法** – 2007 年 4 月 1 日以前にサービスに投入された資産を償却します。
-   **250% 定率法** – 2012 年 4 月 1 日より前にサービスに投入された資産を償却します。
-   **200% 定率法** – 2012 年 4 月 1 日以後にサービスに投入された資産を償却します。

## <a name="what-are-special-depreciation-and-additional-depreciation"></a>特別減価償却および追加減価償却は何ですか。
特別減価償却と追加減価償却は、次の、固定資産の特別なタイプに適用される減価償却のタイプです。

-   波エネルギーなどの、自然エネルギーまたは新エネルギーの供給および開発を促進する、特定の産業政策に基づいて使用される固定資産
-   安全と環境保護のために購入した固定資産
-   身体障碍を持つ従業員を支援するために使用される固定資産
-   高齢者または疾病のある従業員を支援するために作成された固定資産

特別償却を使用すると、特別償却金額は、取得原価と特別償却率を乗算して計算されます。 割増償却を使用すると、特別償却金額は、普通償却と割増償却率を乗算して計算されます。 **注記:** 固定資産が特別償却および割増償却の両方に該当する場合、償却期間の資産に対していずれか 1 つのみを適用できます。

## <a name="what-is-the-allowable-limit-for-depreciation"></a>減価償却の許容制限は何ですか。
減価償却の許容制限は、各減価償却期間の税帳簿ごとに損金として許容される、合計減価償却経費の最大量です。 固定資産の減価償却に対して許容される制限は、会社の固定資産を減価償却するために使用される減価償却のタイプに対応します。

| 減価償却タイプ        | 減価償却の許容限度             |
|--------------------------|----------------------------------------------|
| 通常の減価償却    | 通常の減価償却の許容限度    |
| 加速償却 | 加速償却の許容制限 |
| 特別償却     | 特別償却の許容制限     |
| 増加償却の届出  | 追加の減価償却の許容制限  |

会社の固定資産の期間ごとの減価償却の限度額は、次の式を使用して計算されます: 減価償却の許容限度 = 通常の減価償却の許容限度 + 加速償却の許容制限 + 特別償却限度額または追加の減価償却の許容制限

## <a name="what-is-the-allowable-limit-for-accumulated-depreciation"></a>減価償却累計額の許容限度とは何ですか。
減価償却累計額の許容限度は、耐用年数の間、固定資産の取得金額から控除できる減価償却累計額の最大量です。 減価償却累計額の許容限度の値を選択できます。 この選択は、固定資産に適用する減価償却方法と、固定資産は有形または無形かによります。 以下の 2 種類の減価償却累計額の許容限度があります。

-   **減価償却累計額の 95% の許容限度** – この限度は、古い定額法または古い定率法を使用して減価償却される有形資産にのみ適用されます。 この限度は固定資産の取得コストの 95% に制限されます。
-   **減価償却累計額の最大許容限度** – この限度は、定額法または古い定率法以外の減価償却方法を使用して減価償却される、有形および無形資産の両方に適用されます。 有形資産の場合、減価償却累計額の最大許容限度は資産の取得コストです。 無形資産の減価償却累計額の最大許容限度は、1 円を差し引いた資産の取得コストです。

## <a name="can-i-calculate-depreciation-for-a-fixed-asset-for-a-fiscal-year-that-has-fewer-than-12-months"></a>12 か月未満の会計年に対して固定資産の減価償却を計算できますか。
はい。 本ソフトウェアは会計年度の月数が 12 か月に満たない場合でも減価償却の計算をサポートします。 複数の減価償却カレンダーを設定し、それらの間で変更できます。 減価償却のカレンダーの変更後に現在の会計年度が 12 か月未満となる場合、現在の会計年度および 12 か月ある会計年度に基づいて減価償却の割合が比例的に調整されます。 次の例は、12 か月に満たない会計年度における減価償却の計算例を示します。 元の会計年度が 2010 年 4 月 1 日から 2011 年 3 月 31 日までの期間であり、減価償却が会計年度全体に対して計算されます。 減価償却のカレンダーを変更した後、会計年度は 2011 年 1 月 1 日から 2011 年 12 月 31 日までになります。 このシナリオでは、1 月、2 月、3 月は前の会計カレンダーの一部になり、現在の会計年度は 9 か月のみで構成されます。 残りの 9 か月の減価償却 (2011 年 4 月 1 日から 2011 年 12 月 31 日まで) は、比例分割方法を使用して、前年度の会計年度からの減価償却比率を使用して計算されます。

## <a name="what-is-the-catchup-rule-for-depreciation-and-how-does-it-work"></a>減価償却の差額計上方式とは何ですか。どのような仕組みですか。
減価償却の差額計上方式は、年次減価償却の経費を各期間の減価償却の経費に配分するための効果的な方法として提供されます。 差額計上方式を有効にするには、**固定資産パラメーター** ページの **差額計上方式** チェック ボックスをオンにします。 また、差額計上方式を会計期間の終了時または会計年度末に適用するかどうかを指定できます。

## <a name="how-do-i-calculate-a-depreciation-expense-by-using-the-catchup-rule"></a>減価償却の経費は差額計上方式を使用してどのように計算しますか。
各月の減価償却費が計算され、次の月に転記されます。 以下の要素を使用して毎月の減価償却経費を計算します。

-   年始からの合計償却費: 年次減価償却費 × (年度内の現在の月数 ÷ 12) = 100,000 円
-   1 月から現在の月までに転記された減価償却経費の合計
-   現在の月に転記される減価償却経費: 年の初めから発生している減価償却経費の合計 - 1 月から現在の月までに転記された減価償却経費の合計 = 100,000 JPY

月次の減価償却の計算では、次の式が使用されます: 年次減価償却の経費 × (年度内の現在の月数 ÷ カレンダー年度の月の合計数) – 1 月から現在の月までに転記された減価償却経費の合計。この計算方法は、毎月の減価償却経費の合計が資産の年次減価償却経費と同じになることを保証するために役立ちます。

## <a name="can-i-change-the-depreciation-profile-of-a-fixed-asset-after-the-depreciation-for-the-asset-has-been-posted"></a>資産の減価償却を転記後に固定資産の減価償却プロファイルを変更できますか。
はい。 資産の減価償却を転記後であっても、固定資産の減価償却プロファイルは変更できます。 次の表に、減価償却方法において許可される変更を示します。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>減価償却方法の開始</th>
<th>許可された減価償却方法の変更</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>旧定額法</td>
<td>旧定率法</td>
</tr>
<tr class="even">
<td>旧定率法</td>
<td>旧定額法</td>
</tr>
<tr class="odd">
<td>定額法</td>
<td><ul>
<li>250% 定率法</li>
<li>200% 定率法</li>
</ul></td>
</tr>
<tr class="even">
<td>250% 定率法</td>
<td><ul>
<li>200% 定率法</li>
<li>定額法</li>
</ul></td>
</tr>
<tr class="odd">
<td>200% 定率法</td>
<td><ul>
<li>250% 定率法</li>
<li>定額法</li>
</ul></td>
</tr>
</tbody>
</table>

また、変更履歴を追跡し、資産の新しい耐用年数を、未償却残高スケジュールおよび経過年数スケジュールに基づいて自動的に計算できます。

## <a name="what-types-of-schedules-can-i-import-for-depreciation-purposes"></a>減価償却用にどのタイプのスケジュールをインポートできますか。
固定資産の減価償却と耐用年数を再計算するため、次のスケジュールをインポートできます。

-   未償却残高スケジュール
-   経過年数スケジュール

インポートする減価償却率スケジュールは、固定資産に使用する減価償却方法のタイプによって異なります。

## <a name="additional-resources"></a>追加リソース

- [均等償却を使用した一括比例配分減価償却資産の作成](./tasks/create-lump-sum-depreciation-assets-equally-divided-method.md)
- [帳簿の資産耐用年数期間中の減価償却方法の変更](./tasks/change-depreciation-method-during-asset-life-book.md)
- [単一資産の資産耐用年数期間中の減価償却方法の変更](./tasks/change-depreciation-method-during-asset-life-one-asset.md)
- [増加償却パラメーターおよび転記プロファイルのコンフィギュレーション](./tasks/accelerated-depreciation-posting-profiles.md)
- [割増償却に対する減価償却プロファイルおよび転記プロファイルのコンフィギュレーション](./tasks/configure-depreciation-profile-posting.md)
- [割増償却を使用する固定資産の作成](./tasks/create-fixed-asset-additional-depreciation.md)
- [特別償却プロファイルのある固定資産の作成](./tasks/create-fixed-asset-special-depreciation-profile.md)
- [増加償却ドキュメントの作成および使用状況データの入力](./tasks/create-accelerated-depreciation-document-enter-usage-data.md)
- [加速減価償却プロファイルを作成し、帳簿に割り当てる](./tasks/create-accelerated-depreciation-profile-assign-it-book.md)
- [資産のアイドル期間の定義および減価償却プロセスの検証](./tasks/define-asset-idle-period-validate-depreciation-process.md)
- [償却率表の入力および減価償却プロファイルへの関連付け](./tasks/enter-depreciation-rate-schedule.md)
- [償却超過額/償却不足額の定期決済](./tasks/periodic-settlement-over-under-depreciation.md)
- [割増償却の提案](./tasks/propose-additional-depreciation.md)
- [増加償却の提案と転記](./tasks/propose-post-accelerated-depreciation.md)
- [特別償却の提案](./tasks/propose-special-depreciation.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
