---
title: 在庫バッチのマージ
description: この記事は、2 つ以上の棚卸資産バッチをマージされたバッチに連結する方法に関する情報を提供します。
author: yufeihuang
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventBatchJournalListPage, InventBatchJournalMerge
audience: Application User
ms.reviewer: kamaybac
ms.custom: 39782
ms.assetid: 07c5e98b-10fd-4f5c-b471-41d2150f47b0
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 83c7fa6bf596510c3b902c12433cc55842ebe0b4
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571908"
---
# <a name="merge-inventory-batches"></a>在庫バッチのマージ

[!include [banner](../includes/banner.md)]

この記事は、2 つ以上の棚卸資産バッチをマージされたバッチに連結する方法に関する情報を提供します。

バッチをマージするとき、マージされたバッチの特性とバッチ属性の最適化に計算が役立ちます。 ソース バッチを選択した後、結合されたバッチを転記する前に確認および変更できます。 承認用に在庫仕訳帳にバッチのマージを転送することもできます。 在庫は、その在庫仕訳帳から直接引当または転記できます。 マージされたバッチを転記するとき、棚卸資産がソース バッチとマージされたバッチについて調整されます。

## <a name="are-there-any-prerequisites"></a>前提条件がありますか
はい。バッチ マージ ツールを使用するには、その前に、いくつかのことを設定する必要があります。 次の表に、前提条件を説明します。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>ページ</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>仕訳帳名、在庫</td>
<td>在庫仕訳帳のバッチ マージを転記するときに既定で使用されているタイプ BOM の仕訳帳名を作成する必要があります。 次はオプションですが、推奨されます。バッチ マージが在庫仕訳帳に移動されるときに、引当が自動的に行われるように指定できます。 そうでない場合は、バッチ マージの詳細が設定され、仕訳帳が転記された後に、手持在庫が変更されるリスクがあります。 仕訳帳名の自動割り当てを有効にするには、<strong><strong>引当</strong></strong> フィールドで、<strong>自動</strong> を選択します。</td>
</tr>
<tr class="even">
<td>在庫および倉庫管理パラメーター</td>
<td>在庫仕訳帳の既定の仕訳帳名を指定する必要があります。</td>
</tr>
<tr class="odd">
<td>リリースされた製品</td>
<td>品目の推奨設定を次に示します。
<ul>
<li>マージされたバッチのバッチ番号を自動的に生成するには、リリースされた製品をバッチ番号グループに割り当てる必要があります。 結合されたバッチを作成するとき、または既存のバッチ番号を選択するとき、バッチ番号を手動で入力することもできます。 既存のバッチ番号を選択する場合は、選択したバッチがどの在庫トランザクションにも含まれていないことを確認します。</li>
<li>リリースされた製品について有効期限または消費期限を使用する場合、マージされたバッチの日付は<strong>バッチ マージ日付計算</strong>フィールドの選択に基づいて計算されます。 次のオプションがあります。
<ul>
<li><strong>最短</strong> – 計算は、バッチ マージに対して選択されたソース バッチに指定されるもっとも早い日付に基づきます。</li>
<li><strong>最新</strong> – 計算は、バッチ マージに対して選択されたソース バッチに指定される最新の日付に基づきます。</li>
<li><strong>手動</strong> - 計算は行われません。 日付がすべてのソース バッチで同じ場合、日付が提案されます。 その日付は変更できます。 ソース バッチの日付が同じでない場合は、日付を手動で入力できます。</li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td>バッチ番号グループ</td>
<td>オプション: マージされたバッチを作成するときバッチ番号を生成するには、リリースされた製品にバッチ番号グループを割り当てる必要があります。 そうでない場合は、バッチ番号を手動で入力できます。</td>
</tr>
</tbody>
</table>

## <a name="when-might-i-want-to-merge-batches-of-inventory"></a>在庫のバッチをマージする必要がありますか。
バッチのマージが有用になるときを示すシナリオの例を次に示します。

-   サミーが倉庫の中を歩いていると、同じ品目のいくつかのバッチの数量が少ないことに気付きます。 彼は複数の新しい出荷を受け取る予定であり、半端な数量を 1 つの新しいバッチにマージすることでフロア面積を解放できることが分かっています。
-   サミーは在庫を受け取ると、その新しいバッチを受入済のバッチと結合して、既存のバッチのバッチ属性値を改善することを望んでいます。 これにより、新しいバッチを作成します。

## <a name="can-i-merge-batches-across-sites-and-legal-entities"></a>サイトと法人の全部のバッチを結合できますか
いいえ。1 つの法人の同じサイトと倉庫の保管分析コードを持つバッチのみをマージできます。 ただし、結合されたバッチに、別の場所とパレット ID を指定できます。

## <a name="can-i-merge-partial-quantities"></a>一部の数量をマージできますか。
いいえ、バッチの数量全体のみマージできます。 バッチのマージ機能は、生産機能ではなく在庫機能として使用されることを意図しています。

## <a name="what-if-the-batches-have-different-batch-attribute-values"></a>バッチのバッチ属性値が異なる場合はどうなりますか
ソース バッチを選択して結合されたバッチに統合するとき、Supply Chain Management は、すべてのバッチが同じ特性または属性値を持つかどうかを検証します。 属性値が同じであるとき、結合されたバッチの値が提案されます。 その値は変更できます。 結合されたバッチの属性値が等しくない場合、その値は空白のままとなり、それらの値は手動で入力できます。 属性値のバッチ属性タイプが整数または小数で、値がすべてのソース バッチで同じでない場合、値は加重平均計算を使用して計算されます。 計算値は、最も近い増分値に四捨五入されます。 ソース バッチの値が空白の場合、そのバッチとその数量は計算には含まれません。 **例** 次の例は、結合されたバッチの加重平均計算を示します。 2 つのソース バッチについて、整数であるバッチ属性タイプの値が空白になっています。 次の属性は、ソース バッチに割り当てられます。

| 属性 | 最小 | 増分 | 最大 |
|-----------|---------|-----------|---------|
| 等級     | 3       | 3         | 30      |

ソース バッチの **等級バッチ** 属性の属性値は次のようになります。

| バッチ | 件数 | 属性 | 属性値 |
|-------|----------|-----------|-----------------|
| B1    | 10       | 等級     | 空白           |
| B2    | 15       | 等級     | 15              |
| B3    | 20       | 等級     | 20              |
| B4    | 25       | 等級     | 空白           |
| B5    | 30       | 等級     | 25              |

これらのバッチをソース バッチとして追加するとき、次の値が結合されたバッチに割り当てられます。

| バッチ | 件数 | 属性 | 属性値 |
|-------|----------|-----------|-----------------|
| B6    | 100      | 等級     | 21              |

バッチ B1 と B4 の値と数量は、加重平均の計算に含まれません。 したがって、結合されたバッチの値は次のように計算されます。

| 値 | 数量 (重量)                              | 相対重量 | 相対重量 × 値                                               |
|-------|------------------------------------------------|-----------------|-----------------------------------------------------------------------|
| 15    | 15                                             | 0.230769231     | 3.461538462                                                           |
| 20    | 20                                             | 0.307692308     | 6.153846154                                                           |
| 25    | 30                                             | 0.461538462     | 11.53846154                                                           |
|       | **合計:** 65 (総重量) |                 | **合計:** 21.5384615、四処分五入すると 21 (最も近い増分値) です。 |

## <a name="what-if-the-batches-have-different-batch-dates"></a>バッチのバッチ日付が異なる場合どうなりますか
バッチが異なるバッチ日付を持つ場合、いくつかの日付は、**バッチ マージ** ページの **マージ済みバッチ** クイック タブの **バッチ日付** グループの値に基づいて計算されます。 **バッチ日付** グループで、フィールドの値が計算されます。 これらの値には、製造日、有効期限、在庫通知日、および出庫期限の日付が含まれます。 日付は、**リリース済製品の詳細** ページの **品目データ** フィールド グループの品目の設定に基づいて計算されます。 値を変更したり、手動で入力できます。 他のすべての日付については、計算は行われません。 同じ原則が、バッチ属性値に使用されます。 日付がソース バッチすべてで同じ場合、その日付が結合されたバッチに対して提案されます。 日付がすべてのソース バッチで同じでない場合、結合されたバッチの日付は空白になり、手動で入力できます。

## <a name="what-if-the-dimensions-are-different-on-the-batches-that-i-want-to-merge"></a>分析コードが結合するバッチで異なる場合はどうなりますか
製品分析コード、追跡用分析コード、保管分析コードは次のように処理されます。

-   **製品分析コード** – 選択した品目のすべての製品分析コードは同じであることが必要です。 製品分析コード全体のバッチを結合することはできません。
-   **追跡用分析コード** – 品目のバッチ番号グループが指定されると、新しいバッチ番号が自動的に生成されます。 品目にバッチ番号グループが割り当てられない場合、既存のバッチを選択したり、番号を手動で入力できます。 シリアル番号が、ソース バッチから、結合されたバッチの在庫仕訳帳明細行へ移動されます。
-   **保管分析コード** – サイトと倉庫の保管分析コードは、ソース バッチと結合されたバッチのすべてに対して同じであることが必要です。 ただし、結合されたバッチに、新しい場所とパレット ID を指定できます。

## <a name="how-does-posting-work"></a>転記はどのように機能しますか
転記は、仕訳帳に承認プロセスを使用するかどうかに基づいて、次の 2 つの方法で機能します。 **仕訳帳への転送** および **バッチ マージの転記** アクションを使用してバッチ マージを確認して転記することができる仕訳帳へバッチ マージを移動するか、またはバッチ マージを直接転記できます。 2 つのアクションとの大きな違いは、仕訳帳への移動でバッチ マージを転記しないことです。 どちらのアクションでも、既存のバッチが選択されない場合は新しいバッチが作成され、すべてのバッチの詳細と属性値が更新され、在庫仕訳帳が作成されます。

-   **仕訳帳への転送** – バッチ マージの詳細を新しい在庫仕訳帳に転送します。 自動引当を設定していた場合は、ソース バッチの数量が引き当てられます。 バッチ マージの詳細は変更できません。 バッチ マージを変更するには、仕訳帳を削除する必要があります。 仕訳帳は、別の従業員が後で実行するタスクとして使用できます。 仕訳帳明細行に対するバッチ数量の引当は保護されています。 この割り当てにより、品質プランナーまたは倉庫マネージャーは従業員のタスクを作成することができます。
-   **バッチ マージの転記** – バッチ マージを直接転記します。 このアクションは現物マージの発生後に実行できます。

バッチ マージの在庫仕訳帳を **すべてのバッチ マージ** リスト ページから承認できます。 **仕訳帳** &gt; **転記** をクリックします。 仕訳帳の転記後、結合されたバッチの詳細を変更できません。 バッチ マージを在庫仕訳帳へ転送した後は、その仕訳帳が削除された場合にのみ詳細を変更できます。

## <a name="after-i-merged-a-catchweight-item-why-cant-i-see-the-catchweight-information-in-the-inventory-journal"></a>CW 品目の結合後に在庫仕訳帳上でその CW 情報を確認できないのはどうしてですか。
他のすべての品目と同様に、CW 品目のバッチを結合できます。 ただし、CW 情報は在庫仕訳帳に表示されません。 バッチ マージを在庫仕訳帳に転送する前に、CW 情報を確認することをお勧めします。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]