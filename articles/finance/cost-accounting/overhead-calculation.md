---
title: 間接費の計算
description: この記事では、間接費を計算し配賦するための標準的なプロセスについて説明します。
author: AndersGirke
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation, CAMOverheadRateCalculationJournalEntry, CAMFormulaAllocationBase
audience: Application User
ms.reviewer: twheeloc
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: twheeloc
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 9322fb5237afdbf73147bb549eb3f70929c46ce2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881994"
---
# <a name="overhead-calculation"></a>間接費の計算

[!include [banner](../includes/banner.md)]

この記事では、間接費を計算し配賦するための標準的なプロセスについて説明します。

## <a name="term-definition"></a>用語の定義

間接費とは、事業を経営するために発生するものの、どんな特定の業務活動、製品、またサービスにも直接は起因しないコストのことです。 間接費は、営利活動を生み出すのに不可欠な支援を提供します。 間接費の例を次に示します。

-   賃料
-   電気
-   管理給与

## <a name="overhead-calculation-overview"></a>間接費計算の概要
間接費計算は、コスト会計ポリシーを正しい順序で実行します。 コスト会計ポリシーが変更されたり特定のエラーが検出された場合は、同じ会計期間で複数回間接費計算を実行できます。 間接費計算は実行されるたびに保存され、さまざまなバージョンでその計算を比較できるようにする固有のバージョン ID を受け取ります。 間接費計算が生成するコスト エントリは転記日を受け取ります。 この転記日は、計算に使用される会計年度期間の終了日と一致します。 固有のバージョン ID は、次の要素で構成されます。

-   バージョン タイプ
-   日時
-   原価会計元帳
-   年度
-   会計年度期間

間接費計算は、バージョンとは無関係に実行されます。 そのため、実際のバージョンの前に予算バージョンを計算することができます。 間接費計算は、次の図に示されているように 4 つのステップで構成されます。 各ステップで、仕訳入力のある仕訳ヘッダーが作成されます。 この仕訳ヘッダーは、各計算ステップの入力データを保持します。 ポリシーやルールが各仕訳帳明細行に適用され、コスト エントリが出力として生成されます。 そのため、常に完全なトレーサビリティがあります。 

[![間接費の計算。](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a>電気間接費の計算および配賦
財務会計では、電気などの一部のコストは一括比例配分として登録されます。 したがって、コスト会計には詳細な管理情報は提供されません。 コスト会計では、すべての組織単位およびレベルに正確な管理情報を提供するために、コストが組織単位をフローする必要があります。 このフローは、正確な消費記録もしくは適正な評価のいずれかに基づいている必要があります。 一般会計では、電気コストは以下の表に示されているように転記できます。

<table>
<thead>
<tr>
<th>会計日</th>
<th colspan="2">原価部門</th>
<th colspan="2">主勘定</th>
<th>会計通貨での金額</th>
</tr>
</thead>
<tbody>
<tr>
<td>2017 年 1 月 3 日</td>
<td>CC099</td>
<td>既定のコスト センター</td>
<td>10001</td>
<td>電気</td>
<td>10,000.00</td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a>手順 1: コスト動作計算を処理する

既定では、コスト エントリは、ソース データからインポートされる際に、コスト会計で **未分類** のコスト動作分類を受け取ります。 コスト動作ポリシー ルールを適用することにより、**固定費** もしくは **変動費** のいずれかとしてコスト エントリを再分類できます。

#### <a name="define-the-cost-behavior-rule"></a>コスト動作ルールの定義

場合によっては、コストの一部は固定料金で、残りのコストは消費に基づきます。 電気代は多くの場合この定義と一致します。 特定の固定料金を支払ったら、キロワット時 (Kwh) ごとに消費分を支払います。 たとえば、固定費の料金が 1,000.00 の場合、以下のようにコスト動作ルールが定義されます。

-   固定金額 1,000.00
    -   0 &lt;= 1,000.00 = 固定
    -   1000,01 &lt; N = 変動

##### <a name="journal"></a>仕訳帳

<table>
<thead>
<tr>
<th>仕訳帳</th>
<th>仕訳帳タイプ</th>
<th colspan="3">会計カレンダー期間</th>
<th>バージョン</th>
</tr>
</thead>
<tbody>
<tr>
<td>00001</td>
<td>原価動作計算仕訳帳</td>
<td>会計年度</td>
<td>2017</td>
<td>期間 1</td>
<td>間接費計算 / 01-02-2017 午後 11:51:00 / 元帳 / 2017 / 期間 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>仕訳入力 (コスト オブジェクト残高仕訳入力)

<table>
<thead>
<tr>
<th>会計日</th>
<th colspan="2">原価オブジェクト</th>
<th colspan="2">原価要素</th>
<th>原価動作</th>
<th>金額</th>
</tr>
</thead>
<tbody>
<tr>
<td>2017 年 1 月 3 日</td>
<td>CC099</td>
<td>既定のコスト センター</td>
<td>10001</td>
<td>電気</td>
<td>未分類</td>
<td>10,000.00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>原価エントリ

<table>
<thead>
<tr>
<th colspan="2">原価オブジェクト</th>
<th colspan="2">原価要素</th>
<th>原価動作</th>
<th>金額</th>
<th>会計日</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC099</td>
<td>既定のコスト センター</td>
<td>10001</td>
<td>電気</td>
<td>未分類</td>
<td>10,000.00</td>
<td>2017 年 1 月 3 日</td>
</tr>
<tr>
<td>CC099</td>
<td>既定のコスト センター</td>
<td>10001</td>
<td>電気</td>
<td>未分類</td>
<td>-10,000.00</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC099</td>
<td>既定のコスト センター</td>
<td>10001</td>
<td>電気</td>
<td>固定費</td>
<td>1,000.00</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC099</td>
<td>既定のコスト センター</td>
<td>10001</td>
<td>電気</td>
<td>変動費</td>
<td>9,000.00</td>
<td>2017 年 1 月 31 日</td>
</tr>
</tbody>
</table>

詳細については、「[原価動作ポリシーの作成と原価管理単位への割り当て](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)」を参照してください。
### <a name="step-2-process-the-cost-distribution-calculation"></a>手順 2: コスト配分計算を処理する

コスト配分は、関連する配賦基準を適用することによって、1 つのコスト オブジェクトから 1 つまたは複数の他のコスト オブジェクトへコストを再配分するために使用されます。 コスト配分とコスト配賦は、コスト配分は常に元のコストの主要コスト要素レベルで起こるという点が異なります。

#### <a name="define-the-cost-distribution-rule"></a>コスト配分ルールの定義

財務会計では、電気コストは多くの場合一括比例配分として登録されます。 コスト会計では、このアプローチは十分に詳細ではありません。 変動費は個々のコスト オブジェクトに公平に配分する必要があります。 最も論理的な配賦基準は、電気 (Kwh) の消費です。 電気という名前の付いた統計分析コード メンバーが作成され、電気の消費が記録されます。 既定では、すべての統計分析コード メンバーが配賦基準として使用可能になります。

<table>
<thead>
<tr>
<th colspan="2">原価オブジェクト</th>
<th>Kwh</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>HR</td>
<td>1.000</td>
</tr>
<tr>
<td>CC002</td>
<td>財務</td>
<td>6,000</td>
</tr>
<tr>
<td>CC003</td>
<td>組み立て</td>
<td>0</td>
</tr>
</tbody>
</table>

次の表は、電気消費が変動費の配賦基準として適用される際の結果を示します。

<table>
<thead>
<tr>
<th colspan="2">原価オブジェクト</th>
<th>大きさ</th>
<th>配賦係数</th>
<th>金額</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>HR</td>
<td>1.000</td>
<td>(1,000 ÷ 7,000) × 9,000.00</td>
<td>1,285.71</td>
</tr>
<tr>
<td>CC002</td>
<td>財務</td>
<td>6,000</td>
<td>(6,000 ÷ 7,000) × 9,000.00</td>
<td>7,714.29</td>
</tr>
<tr>
<td>CC003</td>
<td>組み立て</td>
<td>0</td>
<td>(0 ÷ 7,000) × 9,000.00</td>
<td>0.00</td>
</tr>
</tbody>
</table>

固定費は、電気を消費した個々のコスト オブジェクトに均等に配分される必要があります。 フォーミュラ配賦基準の電気統計分析コード メンバーを使用することによりこの結果を出すことができます。(電気 &gt; 0.00) 次の表は、電気消費が変動費の配賦基準として適用される際の結果を示します。

<table>
<thead>
<tr>
<th colspan="2">原価オブジェクト</th>
<th>フォーミュラ</th>
<th>大きさ</th>
<th>配賦係数</th>
<th>金額</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>HR</td>
<td>(1,000 &gt; 0.00)</td>
<td>1</td>
<td>(1 ÷ 2) × 1,000.00</td>
<td>500.00</td>
</tr>
<tr>
<td>CC002</td>
<td>財務</td>
<td>(6,000 &gt; 0.00)</td>
<td>1</td>
<td>(1 ÷ 2) × 1,000.00</td>
<td>500.00</td>
</tr>
<tr>
<td>CC003</td>
<td>組み立て</td>
<td>(0 &gt; 0.00)</td>
<td>0</td>
<td>(0 ÷ 2) × 1,000.00</td>
<td>0.00</td>
</tr>
</tbody>
</table>

##### <a name="journal"></a>仕訳帳

<table>
<thead>
<tr>
<th>仕訳帳</th>
<th>仕訳帳タイプ</th>
<th colspan="3">会計カレンダー期間</th>
<th>バージョン</th>
</tr>
</thead>
<tbody>
<tr>
<td>00002</td>
<td>コスト配分計算仕訳</td>
<td>会計年度</td>
<td>2017</td>
<td>期間 1</td>
<td>間接費計算 / 01-02-2017 午後 11:51:00 / 元帳 / 2017 / 期間 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>仕訳入力 (コスト オブジェクト残高仕訳入力)

<table>
<thead>
<tr>
<th>会計日</th>
<th colspan="2">原価オブジェクト</th>
<th colspan="2">原価要素</th>
<th>原価動作</th>
<th>金額</th>
</tr>
</thead>
<tbody>
<tr>
<td>2017 年 1 月 31 日</td>
<td>CC099</td>
<td>既定のコスト センター</td>
<td>10001</td>
<td>電気</td>
<td>固定費</td>
<td>1,000.00</td>
</tr>
<tr>
<td>2017 年 1 月 31 日</td>
<td>CC099</td>
<td>既定のコスト センター</td>
<td>10001</td>
<td>電気</td>
<td>変動費</td>
<td>9,000.00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>原価エントリ

<table>
<thead>
<tr>
<th colspan="2">原価オブジェクト</th>
<th colspan="2">原価要素</th>
<th>原価動作</th>
<th>金額</th>
<th>会計日</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC099</td>
<td>既定のコスト センター</td>
<td>10001</td>
<td>電気</td>
<td>固定費</td>
<td>-1,000.00</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>電気</td>
<td>固定費</td>
<td>500.00</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC002</td>
<td>財務</td>
<td>10001</td>
<td>電気</td>
<td>固定費</td>
<td>500.00</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC099</td>
<td>既定のコスト センター</td>
<td>10001</td>
<td>電気</td>
<td>変動費</td>
<td>-9,000.00</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>電気</td>
<td>変動費</td>
<td>1,285.71</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC002</td>
<td>財務</td>
<td>10001</td>
<td>電気</td>
<td>変動費</td>
<td>7,714.29</td>
<td>2017 年 1 月 31 日</td>
</tr>
</tbody>
</table>

詳細については、「[原価配分ポリシーの作成と原価管理単位への割り当て](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)」を参照してください。 

### <a name="step-3-process-the-overhead-rate-calculation"></a>手順 3: 間接費率の計算を処理する

間接費率は、1 つ以上の特定のコスト オブジェクトの請求に使用されます。 請求金額は、あらかじめ設定されたコスト レートと割り当てられた配賦基準の大きさに基づいています。 

#### <a name="define-the-overhead-rate"></a>間接費率の定義

コスト オブジェクト CC001 HR は、一連の内部プロジェクトに作用します。 HR プロジェクトという名前の付いた統計分析コード メンバーが、消費された大きさを測定するために作成されます。

<table>
<thead>
<tr>
<th colspan="2">原価オブジェクト</th>
<th>時間</th>
</tr>
</thead>
<tbody>
<tr>
<td>プロジェクト 1</td>
<td>プロジェクト 1</td>
<td>3</td>
</tr>
<tr>
<td>プロジェクト 2</td>
<td>プロジェクト 2</td>
<td>1</td>
</tr>
</tbody>
</table>

コスト プロジェクト貢献度用のあらかじめ設定されたコスト レートが定義されました。

<table>
<thead>
<tr>
<th colspan="2">原価オブジェクト</th>
<th>原価要素</th>
<th>原価動作</th>
<th>単位</th>
<th>率</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>変動費</td>
<td>1</td>
<td>10</td>
</tr>
</tbody>
</table>

次の表は、HR プロジェクトが配賦基準として適用される際の結果を示します。

<table>
<thead>
<tr>
<th colspan="2">原価オブジェクト</th>
<th>大きさ</th>
<th>原価要素</th>
<th>配賦係数</th>
<th>金額</th>
</tr>
</thead>
<tbody>
<tr>
<td>プロジェクト 1</td>
<td>プロジェクト 1</td>
<td>3</td>
<td>10001</td>
<td>(3 ÷ 1) × 10.00</td>
<td>30.00</td>
</tr>
<tr>
<td>プロジェクト 2</td>
<td>プロジェクト 2</td>
<td>1</td>
<td>10001</td>
<td>(1 ÷ 1) × 10.00</td>
<td>10.00</td>
</tr>
</tbody>
</table>

##### <a name="journal"></a>仕訳帳

<table>
<thead>
<tr>
<th>仕訳帳</th>
<th>仕訳帳タイプ</th>
<th colspan="3">会計カレンダー期間</th>
<th>バージョン</th>
</tr>
</thead>
<tbody>
<tr>
<td>00003</td>
<td>間接比率計算仕訳</td>
<td>会計年度</td>
<td>2017</td>
<td>期間 1</td>
<td>間接費計算 / 01-02-2017 午後 11:51:00 / 元帳 / 2017 / 期間 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a>仕訳入力 (間接比率計算のための仕訳入力)

<table>
<thead>
<tr>
<th>会計日</th>
<th colspan="2">原価オブジェクト</th>
<th>大きさ</th>
</tr>
</thead>
<tbody>
<tr>
<td>2017 年 1 月 31 日</td>
<td>プロジェクト 1</td>
<td>内部プロジェクト 1</td>
<td>3.00</td>
</tr>
<tr>
<td>2017 年 1 月 31 日</td>
<td>プロジェクト 2</td>
<td>内部プロジェクト 2</td>
<td>1.00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>原価エントリ

<table>
<thead>
<tr>
<th colspan="2">原価オブジェクト</th>
<th colspan="2">原価要素</th>
<th>原価動作</th>
<th>金額</th>
<th>会計日</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC0001</td>
<td>HR</td>
<td>10001</td>
<td>電気</td>
<td>変動費</td>
<td>-30.00</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>プロジェクト 1</td>
<td>内部プロジェクト 1</td>
<td>10001</td>
<td>電気</td>
<td>変動費</td>
<td>30.00</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>電気</td>
<td>変動費</td>
<td>-10.00</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>プロジェクト 2</td>
<td>内部プロジェクト 2</td>
<td>10001</td>
<td>電気</td>
<td>変動費</td>
<td>10.00</td>
<td>2017 年 1 月 31 日</td>
</tr>
</tbody>
</table>

詳細については、「[間接費計算を実行する](cost-rollup.md#perform-overhead-calculation)」を参照してください。

### <a name="step-4-process-the-cost-allocation-calculation"></a>手順 4: コスト配賦計算を処理する

配賦は、配賦基準を適用することによって、コスト オブジェクトの残高を他のコスト オブジェクトに配賦するために使用します。 Finance では、相互配賦手法をサポートします。 相互配賦手法では、補助コスト オブジェクトが交換する相互サービスが完全に認識されます。 システムは、配賦を実行する正しい順序を自動的に決定します。 コスト オブジェクトの残高は 1 つの配賦基準によって配賦されます。 コスト オブジェクト分析コードとその各メンバーにまたがる配賦がサポートされています。 配賦の順序は、コスト制御ユニットによって制御されます。 

[![相互手法。](./media/reciprocal-method.png)](./media/reciprocal-method.png)

#### <a name="define-the-cost-allocation"></a>コスト配賦の定義

次に、コストのフローを追跡する方法を説明する簡単な例を示します。 コスト オブジェクト CC001 HR は、複数のコスト オブジェクトに作用します。 HR サービスという名前の付いた統計分析コード メンバーが、消費された大きさを測定するために作成されます。

<table>
<thead>
<tr>
<th colspan="2">原価オブジェクト</th>
<th>HR サービス</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC002</td>
<td>財務</td>
<td>35</td>
</tr>
<tr>
<td>CC003</td>
<td>組み立て</td>
<td>55</td>
</tr>
<tr>
<td>CC004</td>
<td>梱包業</td>
<td>10</td>
</tr>
</tbody>
</table>

コスト オブジェクト CC002 財務は、複数のコスト オブジェクトに作用します。 財務サービスという名前の付いた統計分析コード メンバーが、消費された大きさを測定するために作成されます。

<table>
<thead>
<tr>
<th colspan="2">原価オブジェクト</th>
<th>財務サービス</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC003</td>
<td>組み立て</td>
<td>65</td>
</tr>
<tr>
<td>CC004</td>
<td>梱包業</td>
<td>35</td>
</tr>
</tbody>
</table>

コスト オブジェクト CC003 組み立ては、複数のコスト オブジェクトに作用します。 組み立てサービスという名前の付いた統計分析コード メンバーが、消費された大きさを測定するために作成されます。

<table>
<thead>
<tr>
<th colspan="2">原価オブジェクト</th>
<th>組み立てサービス (時間)</th>
</tr>
</thead>
<tbody>
<tr>
<td>製品 1</td>
<td>製品 1</td>
<td>60</td>
</tr>
<tr>
<td>製品 2</td>
<td>製品 2</td>
<td>20</td>
</tr>
</tbody>
</table>

コスト オブジェクト CC004 梱包業は、複数のコスト オブジェクトに作用します。 梱包業サービスという名前の付いた統計分析コード メンバーが、消費された大きさを測定するために作成されます。

<table>
<thead>
<tr>
<th colspan="2">原価オブジェクト</th>
<th>梱包業サービス (時間)</th>
</tr>
</thead>
<tbody>
<tr>
<td>製品 1</td>
<td>製品 1</td>
<td>80</td>
</tr>
<tr>
<td>製品 2</td>
<td>製品 2</td>
<td>15</td>
</tr>
</tbody>
</table>

> [!NOTE]
> 製品が消費する生産時間などの統計測定は、ソース データから抽出できます。 詳細については、「[統計測定プロバイダー テンプレート](statistical-measure-provider-template.md#statistical-measure-provider-template)」を参照してください。 次の表は、HR サービスが合計コスト (固定費と変動費) の配賦基準として適用される際の結果を示します。

<table>
<thead>
<tr>
<th colspan="2">原価オブジェクト</th>
<th>大きさ</th>
<th>配賦係数</th>
<th>金額</th>
<th>原価動作</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC002</td>
<td>財務</td>
<td>35</td>
<td>(35 ÷ 100) × 500.00</td>
<td>175.00</td>
<td>固定費</td>
</tr>
<tr>
<td>CC003</td>
<td>組み立て</td>
<td>55</td>
<td>(55 ÷ 100) × 500.00</td>
<td>275.00</td>
<td>固定費</td>
</tr>
<tr>
<td>CC004</td>
<td>梱包業</td>
<td>10</td>
<td>(10 ÷ 100) × 500.00</td>
<td>50.00</td>
<td>固定費</td>
</tr>
<tr>
<td>CC002</td>
<td>財務</td>
<td>35</td>
<td>(35 ÷ 100) × 1,245.71</td>
<td>436.00</td>
<td>変動費</td>
</tr>
<tr>
<td>CC003</td>
<td>組み立て</td>
<td>55</td>
<td>(55 ÷ 100) × 1,245.71</td>
<td>685.14</td>
<td>変動費</td>
</tr>
<tr>
<td>CC004</td>
<td>梱包業</td>
<td>10</td>
<td>(10 ÷ 100) × 1,245.71</td>
<td>124.57</td>
<td>変動費</td>
</tr>
</tbody>
</table>

次の表は、財務サービスが合計コスト (固定費と変動費) の配賦基準として適用される際の結果を示します。

<table>
<thead>
<tr>
<th colspan="2">原価オブジェクト</th>
<th>大きさ</th>
<th>配賦係数</th>
<th>金額</th>
<th>原価動作</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC003</td>
<td>組み立て</td>
<td>65</td>
<td>(65 ÷ 100) × (500.00 + 175.00)</td>
<td>438.75</td>
<td>固定費</td>
</tr>
<tr>
<td>CC004</td>
<td>梱包業</td>
<td>35</td>
<td>(35 ÷ 100) × (500.00 + 175.00)</td>
<td>236.25</td>
<td>固定費</td>
</tr>
<tr>
<td>CC003</td>
<td>組み立て</td>
<td>65</td>
<td>(65 ÷ 100) × (7,714.29 + 436.00)</td>
<td>5,297.69</td>
<td>変動費</td>
</tr>
<tr>
<td>CC004</td>
<td>梱包業</td>
<td>35</td>
<td>(35 ÷ 100) × (7,714.29 + 436.00)</td>
<td>2,852.60</td>
<td>変動費</td>
</tr>
</tbody>
</table>

次の表は、組み立てサービスが合計コスト (固定費と変動費) の配賦基準として適用される際の結果を示します。

<table>
<thead>
<tr>
<th colspan="2">原価オブジェクト</th>
<th>大きさ</th>
<th>配賦係数</th>
<th>金額</th>
<th>原価動作</th>
</tr>
</thead>
<tbody>
<tr>
<td>製品 1</td>
<td>製品 1</td>
<td>60</td>
<td>(60 ÷ 80) × (275.00 + 438.75)</td>
<td>535.31</td>
<td>固定費</td>
</tr>
<tr>
<td>製品 2</td>
<td>製品 2</td>
<td>20</td>
<td>(20 ÷ 80) × (275.00 + 438.75)</td>
<td>178.44</td>
<td>固定費</td>
</tr>
<tr>
<td>製品 1</td>
<td>製品 1</td>
<td>60</td>
<td>(60 ÷ 80) × (5,297.69 + 685.14)</td>
<td>4,487.12</td>
<td>変動費</td>
</tr>
<tr>
<td>製品 2</td>
<td>製品 2</td>
<td>20</td>
<td>(20 ÷ 80) × (5,297.69 + 685.14)</td>
<td>1,495.71</td>
<td>変動費</td>
</tr>
</tbody>
</table>

次の表は、梱包業サービスが合計コスト (固定費と変動費) の配賦基準として適用される際の結果を示します。

<table>
<thead>
<tr>
<th colspan="2">原価オブジェクト</th>
<th>大きさ</th>
<th>配賦係数</th>
<th>金額</th>
<th>原価動作</th>
</tr>
</thead>
<tbody>
<tr>
<td>製品 1</td>
<td>製品 1</td>
<td>80</td>
<td>(80 ÷ 95) × (50.00 + 236.25)</td>
<td>241.05</td>
<td>固定費</td>
</tr>
<tr>
<td>製品 2</td>
<td>製品 2</td>
<td>15</td>
<td>(15 ÷ 95) × (50.00 + 236.25)</td>
<td>45.20</td>
<td>固定費</td>
</tr>
<tr>
<td>製品 1</td>
<td>製品 1</td>
<td>80</td>
<td>(80 ÷ 95) × (2,852.60 + 124.57)</td>
<td>2,507.09</td>
<td>変動費</td>
</tr>
<tr>
<td>製品 2</td>
<td>製品 2</td>
<td>15</td>
<td>(15 ÷ 95) × (2,852.60 + 124.57)</td>
<td>470.08</td>
<td>変動費</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>仕訳入力 (コスト オブジェクト残高仕訳入力)

<table>
<thead>
<tr>
<th>仕訳帳</th>
<th>仕訳帳タイプ</th>
<th colspan="3">会計カレンダー期間</th>
<th>バージョン</th>
</tr>
</thead>
<tbody>
<tr>
<td>00004</td>
<td>原価配賦仕訳帳</td>
<td>会計年度</td>
<td>2017</td>
<td>期間 1</td>
<td>間接費計算 / 01-02-2017 午後 11:51:00 / 元帳 / 2017 / 期間 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a>仕訳帳明細行

<table>
<thead>
<tr>
<th>会計日</th>
<th colspan="2">原価オブジェクト</th>
<th colspan="2">原価要素</th>
<th>原価動作</th>
<th>金額</th>
</tr>
</thead>
<tbody>
<tr>
<td>2017 年 1 月 31 日</td>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>電気</td>
<td>固定費</td>
<td>500.00</td>
</tr>
<tr>
<td>2017 年 1 月 31 日</td>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>電気</td>
<td>変動費</td>
<td>1,245.71</td>
</tr>
<tr>
<td>2017 年 1 月 31 日</td>
<td>CC002</td>
<td>財務</td>
<td>10001</td>
<td>電気</td>
<td>固定費</td>
<td>675.00</td>
</tr>
<tr>
<td>2017 年 1 月 31 日</td>
<td>CC002</td>
<td>財務</td>
<td>10001</td>
<td>電気</td>
<td>変動費</td>
<td>8,150.29</td>
</tr>
<tr>
<td>2017 年 1 月 31 日</td>
<td>CC003</td>
<td>組み立て</td>
<td>10001</td>
<td>電気</td>
<td>固定費</td>
<td>713.75</td>
</tr>
<tr>
<td>2017 年 1 月 31 日</td>
<td>CC003</td>
<td>組み立て</td>
<td>10001</td>
<td>電気</td>
<td>変動費</td>
<td>5,982.83</td>
</tr>
<tr>
<td>2017 年 1 月 31 日</td>
<td>CC003</td>
<td>梱包業</td>
<td>10001</td>
<td>電気</td>
<td>固定費</td>
<td>286.25</td>
</tr>
<tr>
<td>2017 年 1 月 31 日</td>
<td>CC003</td>
<td>梱包業</td>
<td>10001</td>
<td>電気</td>
<td>変動費</td>
<td>2,977.17</td>
</tr>
<tr>
<td>2017 年 1 月 31 日</td>
<td>製品 1</td>
<td>製品 1</td>
<td>10001</td>
<td>電気</td>
<td>固定費</td>
<td>776.36</td>
</tr>
<tr>
<td>2017 年 1 月 31 日</td>
<td>製品 1</td>
<td>製品 1</td>
<td>10001</td>
<td>電気</td>
<td>変動費</td>
<td>6,994.21</td>
</tr>
<tr>
<td>2017 年 1 月 31 日</td>
<td>製品 2</td>
<td>製品 1</td>
<td>10001</td>
<td>電気</td>
<td>固定費</td>
<td>223.64</td>
</tr>
<tr>
<td>2017 年 1 月 31 日</td>
<td>製品 2</td>
<td>製品 1</td>
<td>10001</td>
<td>電気</td>
<td>変動費</td>
<td>1,965.79</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>原価エントリ

<table>
<thead>
<tr>
<th colspan="2">原価オブジェクト</th>
<th colspan="2">原価要素</th>
<th>原価動作</th>
<th>金額</th>
<th>会計日</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>電気</td>
<td>固定費</td>
<td>-500.00</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC002</td>
<td>財務</td>
<td>10001</td>
<td>電気</td>
<td>固定費</td>
<td>175.00</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC003</td>
<td>組み立て</td>
<td>10001</td>
<td>電気</td>
<td>固定費</td>
<td>275.00</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC004</td>
<td>梱包業</td>
<td>10001</td>
<td>電気</td>
<td>固定費</td>
<td>50,00</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC001</td>
<td>HR</td>
<td>10001</td>
<td>電気</td>
<td>変動費</td>
<td>-1,245.71</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC002</td>
<td>財務</td>
<td>10001</td>
<td>電気</td>
<td>変動費</td>
<td>436.00</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC003</td>
<td>組み立て</td>
<td>10001</td>
<td>電気</td>
<td>変動費</td>
<td>685.14</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC004</td>
<td>梱包業</td>
<td>10001</td>
<td>電気</td>
<td>変動費</td>
<td>124.57</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC002</td>
<td>財務</td>
<td>10001</td>
<td>電気</td>
<td>固定費</td>
<td>-675.00</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC003</td>
<td>組み立て</td>
<td>10001</td>
<td>電気</td>
<td>固定費</td>
<td>438.75</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC004</td>
<td>梱包業</td>
<td>10001</td>
<td>電気</td>
<td>固定費</td>
<td>236.25</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC002</td>
<td>財務</td>
<td>10001</td>
<td>電気</td>
<td>変動費</td>
<td>-8,150.29</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC003</td>
<td>組み立て</td>
<td>10001</td>
<td>電気</td>
<td>変動費</td>
<td>5,297.69</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC004</td>
<td>梱包業</td>
<td>10001</td>
<td>電気</td>
<td>変動費</td>
<td>2,852.60</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC003</td>
<td>組み立て</td>
<td>10001</td>
<td>電気</td>
<td>固定費</td>
<td>-713.75</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>製品 1</td>
<td>製品 1</td>
<td>10001</td>
<td>電気</td>
<td>固定費</td>
<td>535.31</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>製品 2</td>
<td>製品 2</td>
<td>10001</td>
<td>電気</td>
<td>固定費</td>
<td>178.44</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC003</td>
<td>組み立て</td>
<td>10001</td>
<td>電気</td>
<td>変動費</td>
<td>-5,982.83</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>製品 1</td>
<td>製品 1</td>
<td>10001</td>
<td>電気</td>
<td>変動費</td>
<td>4,487.12</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>製品 2</td>
<td>製品 2</td>
<td>10001</td>
<td>電気</td>
<td>変動費</td>
<td>1,495.71</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC003</td>
<td>組み立て</td>
<td>10001</td>
<td>電気</td>
<td>固定費</td>
<td>-286.25</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>製品 1</td>
<td>製品 1</td>
<td>10001</td>
<td>電気</td>
<td>固定費</td>
<td>241.05</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>製品 2</td>
<td>製品 2</td>
<td>10001</td>
<td>電気</td>
<td>固定費</td>
<td>45.20</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>CC003</td>
<td>組み立て</td>
<td>10001</td>
<td>電気</td>
<td>変動費</td>
<td>-2,977.17</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>製品 1</td>
<td>製品 1</td>
<td>10001</td>
<td>電気</td>
<td>変動費</td>
<td>2,507.09</td>
<td>2017 年 1 月 31 日</td>
</tr>
<tr>
<td>製品 2</td>
<td>製品 2</td>
<td>10001</td>
<td>電気</td>
<td>変動費</td>
<td>470.08</td>
<td>2017 年 1 月 31 日</td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a>まとめ
財務会計では、電気のコスト 10,000.00 がダミーのコスト センター ID に転記されます。 したがって、コスト経理担当者はこのコストが配賦される必要があることが分かります。 コスト会計では、コストは、適用されているポリシーおよびルールに基づいて、組織単位およびレベルをフローします。 各コストは、コスト配賦の最善の評価を提供する配賦基準に関連付けられています。

原価要素 | 原価オブジェクト<br>CC099 | 原価オブジェクト<br>CC001 | 原価オブジェクト<br>CC002 | 原価オブジェクト<br>CC003 | 原価オブジェクト<br>CC004 | 原価オブジェクト<br>プロジェクト 1 | 原価オブジェクト<br>プロジェクト 2 | 原価オブジェクト<br>製品 1 | 原価オブジェクト<br>製品 2 | 合計
---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:
10001 電気 | 0.00 | 0.00 | 0.00 | 0.00 |  | 30.00 | 10.00 | 7,770.57 | 2,189.43 | 10,000.00 |
未分類 | 0.00 |  |  |  |  |  |  |  |  |  |
固定費 | 0.00 | 0.00 | 0.00 | 0.00 | 0.00 |  |  | 776.36 | 223.64 | 1,000.00 |
変動費 | 000 | 0.00 | 0.00 | 0.00 | 0.00 | 30.00 | 10.00 | 6,994.21 | 1,965.79 | 9,000.00 |

> [!NOTE]
> この記事では、主要コスト要素である 10001 電気がどのようにコスト オブジェクトをフローするかを示します。 したがって、この間接費は組織の最下位レベルに配賦されます。 つまり、最下位レベルのコスト オブジェクトがそのコストを負担します。 コスト オブジェクト間のコストの視覚的なフローが必要な場合は、コスト ロールアップ ポリシー ルールを使用して、コストのフローを視覚化できます。 詳細については、[原価ロールアップ ポリシーおよび間接費の計算](cost-rollup.md) を参照してください。





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
