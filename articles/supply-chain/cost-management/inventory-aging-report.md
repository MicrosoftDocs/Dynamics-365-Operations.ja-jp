---
title: 在庫エイジング レポートの例とロジック
description: このトピックでは、在庫のエイジング レポートの結果を解釈する方法を示すいくつかの例を示します。
author: JennySong-SH
ms.date: 5/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4cfffa49f802c601da391617b123134c435fba92
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672349"
---
# <a name="inventory-aging-report-examples-and-logic"></a>在庫エイジング レポートの例とロジック

[!include [banner](../includes/banner.md)]

このトピックでは、**在庫のエイジング** レポートの結果を解釈する方法を示すいくつかの例を示します。 このレポートでは、選択された品目または品目グループの手持在庫の数量と在庫価値が、いくつかの期間バケットに分類されます。 このトピックでは、レポートの内部ロジックについても説明します。

このトピックの例では、標準の **在庫エイジング レポート** で表示される結果を示します。 ただし、通常は、特に処理する必要がある品目と倉庫が多い場合は、このレポートの [在庫エイジング レポート ストレージ](inventory-aging-report-storage.md) バージョンを使用することをお勧めします。 在庫のエイジング レポートの保管では、生成された各レポートを保存し、結果をインタラクティブなページとグラフで表示して、レポートをエクスポートすることができます。

## <a name="sample-data-that-is-used-in-these-examples"></a>これらの例で使用されるサンプル データ

このトピックの例は、このセクションで説明するサンプル在庫トランザクション データに基づいています。

### <a name="storage-dimension-setup"></a>保管分析コード セットアップ

この例のシステムには、次の保管分析コードの設定が含まれています。

| 氏名      | 使用可能 | 現物在庫 | 資産在庫 |
|-----------|--------|--------------------|---------------------|
| サイト      | 有    | 有                | 有                 |
| 倉庫 | 有    | 有                | 無                  |

### <a name="inventory-model"></a>在庫モデル

この例のシステムでは、リリースされた製品の在庫モデルは *FIFO* で、在庫モデルの **原価価格** 設定には *現物価格* が含まれます。

### <a name="inventory-transactions"></a>在庫トランザクション

この例のシステムには、品目番号 *1000* を持つリリース済製品についての、次の在庫トランザクションが含まれています。

| 参照      | サイト | 倉庫 | 受信   | 問題 | 現物日付 | 財務日付 | 件数 | 原価金額 | 現物原価金額 |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| 発注書 | 1    | 11        | 購買済 |       | 3 月 15 日      | 3 月 15 日       | 10       | 1.000       | 1.000                |
| 発注書 | 2    | 21        | 購買済 |       | 3 月 15 日      | 3 月 15 日       | 10       | 2,000       | 2,000                |
| 発注書 | 1    | 11        | 受入済  |       | 4 月 15 日      |                | 5        |             | 375                  |
| 移動オーダー | 1    | 11        |           | 売却  | 5 月 2 日         | 5 月 2 日          | -5       | -458.33     | -458.33              |
| 移動オーダー | 1    | 12        | 購買済 |       | 5 月 2 日         | 5 月 2 日          | 5        | 458.33      | 458.33               |
| 販売注文    | 1    | 12        |           | 売却  | 5 月 3 日         | 5 月 3 日          | -1       | -91.67      | -91.67               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a>各期間バケットの数量と金額の計算方法

前のセクションで説明したサンプルデータを使用して、次のような設定の **在庫エイジング** レポートを実行できます。

- **現在の日付:** *2020 年 5 月 9 日*
- **サイト:** *表示*
- **倉庫:** *いいえ*
- **品目番号:** *合計*
- **エイジング期間:** 月ごとのバケットを生成する場合にこのフィールドを設定します。

この場合、生成されるレポートの内容は、次の例のようになります。

<table>
<thead>
<tr>
    <th rowspan="2">品目番号</th>
    <th rowspan="2">サイト</th>
    <th rowspan="2">手持在庫数量</th>
    <th rowspan="2">手持の金額</th>
    <th rowspan="2">在庫金額数量</th>
    <th rowspan="2">在庫金額</th>
    <th rowspan="2">平均単位原価</th>
    <th colspan="2">2020 年 5 月 8 日 - 2020 年 5 月 1 日</th>
    <th colspan="2">2020 年 4 月 30 日 - 2020 年 4 月 1 日</th>
    <th colspan="2">2020 年 3 月 31 日 - 2020 年 3 月 1 日</th>
</tr>
<tr>
    <th>P1:数量</th>
    <th>P1:額</th>
    <th>P2:数量</th>
    <th>P2:額</th>
    <th>P3:数量</th>
    <th>P3:額</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>91.67</td>
    <td></td>
    <td></td>
    <td>5.00</td>
    <td>458.33</td>
    <td>9.00</td>
    <td>825.00</td>
</tr>
<tr>
    <td>1000</td>
    <td>2</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>200.00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10.00</td>
    <td>2,000.00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>合計 1000</strong></td>
    <td></td>
    <td><strong>24.00</strong></td>
    <td><strong>3,283.33</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>5.00</strong></td>
    <td><strong>458.33</strong></td>
    <td><strong>19</strong></td>
    <td><strong>2,825.00</strong></td>
</tr>
</tfoot>
</table>

このサンプル レポートの詳細については、次を確認してください。

- レポートに表示される **在庫金額の数量**、**在庫金額**、**平均単位原価** の各値は、財務在庫分析コード (この場合は **サイト**) の値です。

    たとえば、サイト 1の場合、レポートには次の情報が表示されます。

    - **在庫金額の数量** の値は、*14* (= 10 + 5 – 5 + 5 – 1) になります。
    - **在庫金額の数量** の値は、*1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67) になります。
    - **平均単位原価** の値は *91.67* です。
    - 各期間バケットの **手持在庫** の値と **金額** の値は、**平均単位原価** の値を使用して計算されます。

- このレポートでは、各期間バケットの入庫済在庫数量を集計することによって、各期間バケットの手持在庫数量を決定します。 次に、品目が使用している在庫モデルに関係なく、先入れ先出し (FIFO) 原則を適用して、合計出庫数量を差し引きます。

同じレポートを再度実行したときに、両方の **サイト** フィールドと **倉庫** フィールドを *表示する* ように設定した場合、新しいレポートは次の例のようになります。

<table>
<thead>
<tr>
    <th rowspan="2">品目番号</th>
    <th rowspan="2">サイト</th>
    <th rowspan="2">倉庫</th>
    <th rowspan="2">手持在庫数量</th>
    <th rowspan="2">手持の金額</th>
    <th rowspan="2">在庫金額数量</th>
    <th rowspan="2">在庫金額</th>
    <th rowspan="2">平均単位原価</th>
    <th colspan="2">2020 年 5 月 8 日 - 2020 年 5 月 1 日</th>
    <th colspan="2">2020 年 4 月 30 日 - 2020 年 4 月 1 日</th>
    <th colspan="2">2020 年 3 月 31 日 - 2020 年 3 月 1 日</th>
</tr>
<tr>
    <th>P1:数量</th>
    <th>P1:額</th>
    <th>P2:数量</th>
    <th>P2:額</th>
    <th>P3:数量</th>
    <th>P3:額</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>11</td>
    <td>10</td>
    <td>916.67</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>91.67</td>
    <td></td>
    <td></td>
    <td>5.00</td>
    <td>458.33</td>
    <td>5.00</td>
    <td>458.33</td>
</tr>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>12</td>
    <td>4</td>
    <td>366.67</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>91.67</td>
    <td>4.00</td>
    <td>366.67</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td>1000</td>
    <td>2</td>
    <td></td>
    <td>10</td>
    <td>2,000.00</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>200.00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10.00</td>
    <td>2,000.00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>合計 1000</strong></td>
    <td></td>
    <td></td>
    <td><strong>24.00</strong></td>
    <td><strong>3,283.33</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>4.00</strong></td>
    <td><strong>366.67</strong></td>
    <td><strong>5.00</strong></td>
    <td><strong>458.33</strong></td>
    <td><strong>15</strong></td>
    <td><strong>2,458.33</strong></td>
</tr>
</tfoot>
</table>

この場合、サイト 1 は 2 つの行に分割され、1 つは倉庫 11、もう 1 つは倉庫 12 に対応します。 ただし、財務在庫分析コードではないので、**在庫金額の数量**、**在庫金額**、**平均単位原価** の各値は、**倉庫** は同じになります。

また、サイト 1 の数量配分が異なることを確認します。 最初に実行したレポートでは、同じサイトで発生した移動オーダーが無視され、売上請求書の数量がサイト 1 の **3/31/2020 - 3/1/2020** の期間バケットから差し引かれます。 ただし、新しいレポートでは、システムによって、倉庫 12 の **5/8/2020 - 5/1/2020** 期間バケットからの売上請求書の数量が差し引かれます。

## <a name="effects-of-inventory-closing"></a>在庫決算の効果

5 月の在庫決算を実行した後に、前のレポートを再度実行しても、**現在の日付** フィールドが *2020 年 5 月 31 日* に設定されている場合は、次のような結果が確認できます。

- **在庫の値** と **平均単位原価** 価値が更新されます。
- **手持在庫の値** の値と、各区間バケットのすべての **金額** の値が、それに応じて更新されます。

新しいレポートは次の例のようになります。

<table>
<thead>
<tr>
    <th rowspan="2">品目番号</th>
    <th rowspan="2">サイト</th>
    <th rowspan="2">倉庫</th>
    <th rowspan="2">手持在庫数量</th>
    <th rowspan="2">手持の金額</th>
    <th rowspan="2">在庫金額数量</th>
    <th rowspan="2">在庫金額</th>
    <th rowspan="2">平均単位原価</th>
    <th colspan="2">2020 年 5 月 31 日 - 2020 年 5 月 1 日</th>
    <th colspan="2">2020 年 4 月 30 日 - 2020 年 4 月 1 日</th>
    <th colspan="2">2020 年 3 月 31 日 - 2020 年 3 月 1 日</th>
</tr>
<tr>
    <th>P1:数量</th>
    <th>P1:額</th>
    <th>P2:数量</th>
    <th>P2:額</th>
    <th>P3:数量</th>
    <th>P3:額</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>11</td>
    <td>10</td>
    <td>910.70</td>
    <td>14</td>
    <td>1,275.00</td>
    <td>91.07</td>
    <td>0.00</td>
    <td></td>
    <td>5.00</td>
    <td>455.36</td>
    <td>5.00</td>
    <td>455.36</td>
</tr>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>12</td>
    <td>4</td>
    <td>364.29</td>
    <td>14</td>
    <td>1,275.00</td>
    <td>91.07</td>
    <td>4.00</td>
    <td>364.29</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td>1000</td>
    <td>2</td>
    <td></td>
    <td>10</td>
    <td>2,000.00</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>200.00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10.00</td>
    <td>2,000.00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>合計 1000</strong></td>
    <td></td>
    <td></td>
    <td><strong>24.00</strong></td>
    <td><strong>3,275.00</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>4.00</strong></td>
    <td><strong>364.29</strong></td>
    <td><strong>5.00</strong></td>
    <td><strong>455.36</strong></td>
    <td><strong>15</strong></td>
    <td><strong>2,455.36</strong></td>
</tr>
</tfoot>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]