---
title: "配賦基準"
description: "このトピックでは、配賦基準について説明します。 配賦基準は原価計算での主要コンポーネントで、間接費を配賦するために主に使用されます。"
author: YuyuScheller
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimensionMember
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 223174
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: YuyuScheller
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: 74a3033ffbdba2efc6c5ecd6c55019898751a146
ms.contentlocale: ja-jp
ms.lasthandoff: 06/20/2017

---

# <a name="allocation-bases"></a>配賦基準 

[!include[banner](../includes/banner.md)]

配賦基準は、原価計算で間接費を配賦する基盤です。 配賦基準は、たとえば使用された機械の時間、消費されたキロワット時間 (kWh)、または占有された平方フィートなどの数量の場合があります。 配賦基準は、生産される在庫に間接費を割り当てる場合に主に使用されます。 たとえば IT 部門は、各部門で使用しているコンピューターの数に応じて経費を割り当てます。

原価計算の配賦基準には 3 つのタイプがあります。

- 事前に定義された分析コード メンバー配賦基準
- 階層配賦基準
- フォーミュラの配賦基準

## <a name="predefined-dimension-member-allocation-bases"></a>事前に定義された分析コード メンバー配賦基準

事前に定義された分析コード メンバー配賦基準は、次のどれか 1 つのタイプの分析コード メンバーが作成された場合、自動的に作成されます。

- 統計分析コード メンバー
- 原価要素分析コード メンバー

> [!NOTE]
> 原価要素分析コード メンバーに基づく事前に定義された分析コード メンバー配賦基準は、総勘定元帳や一般予算などのデータ ソース プロバイダーからの値のみを考慮します。

### <a name="example-1-use-a-cost-element-dimension-member-as-the-allocation-base"></a>例 1: 配賦基準として原価要素分析コード メンバーを使用
この例では、原価要素10002 (従業員の保険) を原価要素10001 (給与) に記録されている残高に配賦する原価配賦ルールを作成する方法を示します。 配賦ルールは、給与全体に対する各部門の給与の比率に基づいて定義されます。 (レビュー必要)

総勘定元帳で、勘定科目表は次のように定義されています。

| 勘定科目表 | 主勘定 | 説明        | 主勘定タイプ |
|------------------|--------------|--------------------|-------------------|
| 共有           | 10001        | 給与           | 支出           |
| 共有           | 10002        | 従業員の保険 | 支出           |

原価要素分析コードを定義し、データ コネクタをコンフィギュレーションします。 データがインポートされると、次のエントリが原価計算に作成されます。

**原価要素分析コード メンバー**

| 原価要素分析コード名 | 原価要素 |  説明       | 種類    |
|-----------------------------|--------------|--------------------|---------|
| 原価要素               | 10001        | 給与           | 主要 |
| 原価要素               | 10002        | 従業員の保険 | 主要 |

**事前に定義された分析コード メンバー配賦基準** 

| 氏名  | 説明        | 原価要素分析コード |
|-------|--------------------|------------------------|
| 10001 | 給与           | 原価要素          |
| 10002 | 従業員の保険 | 原価要素          |

総勘定元帳には次のエントリが転記されています。

- 給与主勘定を示すエントリは給与システムから来ていて、原価部門に転記されています。
- 従業員の保険の費用は、既定の原価部門に手動で転記されます。

| 会計日 | コスト センター |  説明        | 主勘定 |  説明       | 会計通貨での金額 |
|-----------------|-------------|---------------------|--------------|--------------------|-------------------------------|
| 2017 年 1 月 3 日      | CC001       | HR                  | 10001        | 給与           | 2,000.00                      |
| 2017 年 1 月 3 日      | CC002       | FI                  | 10001        | 給与           | 5,000.00                      |
| 2017 年 1 月 3 日      | CC003       | IT                  | 10001        | 給与           | 3,000.00                      |
| 2017 年 1 月 3 日      | CC099       | 既定のコスト センター | 10002        | 従業員の保険 | 1,000.00                      |

一般会計ソース データが処理されると、次のエントリが原価計算に作成されます。

**原価エントリ**

| 原価オブジェクト |  説明        | 原価要素  |  説明       | 原価動作   |金額|会計日|
|-------------|---------------------|---------------|--------------------|-----------------|------|---------------|
| CC001       | HR                  | 10001         | 給与           | 未分類    |2,000.00|  2017 年 1 月 3 日    |
| CC002       | FI                  | 10001         | 給与           | 未分類    |5,000.00|     2017 年 1 月 3 日         |
| CC003       | IT                  | 10001         | 給与           | 未分類    |3,000.00|      2017 年 1 月 3 日        |
| CC099       | 既定のコスト センター | 10002         | 従業員の保険 | 未分類    |1,000.00|      2017 年 1 月 3 日       |

この単純化された例では、原価要素10002 (従業員の保険) を原価要素10001 (給与) に記録されている残高に相対して配賦する原価配賦ルールが作成されています。

**原価配分ルール**

| 原価オブジェクト分析コード階層ノード | 原価要素分析コード階層ノード | 原価動作 | 配賦基準 |
|--------------------------------------|---------------------------------------|---------------|-----------------|
| CC099                                | 10002                                 | 未分類  | 10001           |

**間接費計算を実行する**

配賦基準として原価要素10001 (給与) が適用された後、間接費の計算結果は次のとおりです。

| 原価オブジェクト | 説明 | 大きさ |   配賦係数         | 金額 |
|-------------|-------------|-----------|-----------------------------|--------|
| CC001       | HR          | 2,000     | (2,000 ÷ 10,000) × 1,000.00 | 200.00 |
| CC002       | FI          | 5,000     | (5,000 ÷ 10,000) × 1,000.00 | 500.00 |
| CC003       | IT          | 3,000     | (3,000 ÷ 10,000) × 1,000.00 | 300.00 |

**仕訳帳**

| 仕訳帳 | 仕訳帳タイプ                          | 会計カレンダー期間 | 年 | 期間   | バージョン                                                                 |
|---------|---------------------------------------|------------------------|------|----------|-------------------------------------------------------------------------|
| 00001   | コスト配分計算仕訳 | 会計年度                 | 2017 | 期間 1 | 間接費計算 / 01-02-2017 午後 11:51:00 / 元帳 / 2017 / 期間 1 |

**原価オブジェクト残高の仕訳入力**

| 会計日 | 原価オブジェクト | 説明         | 原価要素 | 説明        | 原価動作 |  金額  |
|-----------------|-------------|---------------------|--------------|--------------------|---------------|----------|
| 2017 年 1 月 31 日      | CC099       | 既定のコスト センター | 10002        | 従業員の保険 | 未分類  | 1,000.00 |

**原価エントリ**

| 原価オブジェクト |  説明        | 原価要素 |    説明     | 原価動作 | 金額    | 会計日 |
|-------------|---------------------|--------------|--------------------|---------------|-----------|-----------------|
| CC099       | 既定のコスト センター | 10002        | 従業員の保険 | 未分類  | -1,000.00 | 2017 年 1 月 31 日      |
| CC001       | HR                  | 10002        | 従業員の保険 | 未分類  | 200.00    | 2017 年 1 月 31 日      |
| CC002       | FI                  | 10002        | 従業員の保険 | 未分類  | 500.00    | 2017 年 1 月 31 日      |
| CC099       | IT                  | 10002        | 従業員の保険 | 未分類  | 300.00    | 2017 年 1 月 31 日      |

### <a name="example-2-use-a-statistical-dimension-member-as-the-allocation-base"></a>例 2: 配賦基準として統計分析コード メンバーを使用

統計分析コード メンバーは、原価オブジェクトごとのポリシーの定義または非金銭消費のレポートとして、配賦基準として使用できます。 手動で統計分析コード メンバーを作成したり、データ管理インポート/エクスポート ツールを使用してファイルからインポートできます。

**統計分析コード メンバー**

| 統計分析コード名 | 統計要素 | 説明               | 単位 |
|----------------------------|---------------------|---------------------------|------|
| 統計要素       | FTE                 | フルタイム従業員       | Ea   |
| 統計要素       | 電気         | 電気消費   | kWh  |

統計分析コード メンバーを保存すると、事前に定義された分析コード メンバー配賦基準に対応するレコードが作成されます。

**事前に定義された分析コード メンバー配賦基準**

| 氏名        | 説明             | 統計要素分析コード |
|-------------|-------------------------|-------------------------------|
| FTE         | フルタイム従業員     | 統計要素          |
| 電気 | 電気消費 | 統計要素          |

統計測定は、さまざまなソースから取得できます。

- 電気消費は、会社のさまざまな領域にインストールされているメーターで計測できます。
- テーブルには統計測定が保持されます。 たとえば、HcmEmployment の表には、すべての従業員の一覧および従業員が働くコスト センターが含まれます。

| 氏名       | コスト センター |  説明  | 作業者タイプ |
|------------|-------------|----|-------------|
| 従業員 A | CC001       | HR | 従業員    |
| 従業員 B | CC002       | FI | 従業員    |
| 従業員 C | CC002       | FI | 従業員    |
| 従業員 D | CC003       | IT | 従業員    |
| 従業員 F | CC003       | IT | 従業員    |

> [!NOTE]
> 財務分析コードを含むすべてのテーブルは、統計測定のソースとして使用できます。

原価計算では、次のデータ接続を使用して統計測定のコレクションをサポートしています。

- データ管理インポート/エクスポート ツール
- 統計測定

システムから統計測定を取得するには、統計測定プロバイダー テンプレートが必要です。 詳しくは、「統計測定プロバイダー テンプレート」を参照してください。 (このトピックの作成後にリンクを追加)。

**統計測定プロバイダー テンプレート**

| 氏名  | 職務 | ソース テーブル  | 合計フィールド      | 日付フィールド     |
|-------|----------|---------------|----------------|----------------|
| FTE の | カウント    | HcmEmployment | 適用できません | 適用できません |

統計測定ソース データが処理された後、次のエントリが原価計算に作成されます。

**統計エントリ**

| 原価オブジェクト | 説明      | 会計日 | 統計分析コード メンバー | 説明         | 大きさ |
|-------------|------------------|-----------------|------------------------------|---------------------|-----------|
| CC001       | HR               | 2017 年 1 月 31 日      | FTE の                        | フルタイム従業員 | 1.00      |
| CC002       | FI               | 2017 年 1 月 31 日      | FTE の                        | フルタイム従業員 | 2.00      |
| CC003       | IT               | 2017 年 1 月 31 日      | FTE の                        | フルタイム従業員 | 2.00      |

次のコスト配分ルールの例は、FTE の事前に定義された分析コード メンバー配賦基準が配賦基準として割り当てられた場合です。

| 原価オブジェクト | 説明  | 大きさ | 配賦係数 |
|-------------|------|-----------|-------------------|
| CC001       | HR   | 1.00      | (1/5) × 金額    |
| CC002       | FI   | 2.00      | (2/5) × 金額    |
| CC003       | IT   | 2.00      | (2/5) × 金額    |

インポートされた統計測定データ エンティティを使用して、原価計算に統計測定をインポートできます。 データ管理インポート/エクスポート ツールも使用できます。 Excel では、電気の消費が次のように記録されます。

| 会計日 | 分析コード メンバー | 大きさ | ソース識別子 |
|-----------------|------------------|-----------|-------------------|
| 2017 年 1 月 31 日      | CC001            | 2,450.00  | 電気       |
| 2017 年 1 月 31 日      | CC002            | 4,100.00  | 電気       |
| 2017 年 1 月 31 日      | CC003            | 15,000.00 | 電気       |

統計測定ソース データが処理された後、次のエントリが原価計算に作成されます。

**統計エントリ**

| 原価オブジェクト |    | 会計日 | 統計分析コード メンバー |    説明          | 大きさ |
|-------------|----|-----------------|------------------------------|-------------------------|-----------|
| CC001       | HR | 2017 年 1 月 31 日      | 電気                  | 電気消費 | 2,450.00  |
| CC002       | FI | 2017 年 1 月 31 日      | 電気                  | 電気消費 | 4,100.00  |
| CC003       | IT | 2017 年 1 月 31 日      | 電気                  | 電気消費 | 15,000.00 |

次のコスト配分ルールの例は、電気の事前に定義された分析コード メンバー配賦基準が配賦基準として割り当てられた場合です。

| 原価オブジェクト | 説明  | 大きさ | 配賦係数          |
|-------------|------|-----------|----------------------------|
| CC001       | HR   | 2,450.00  | (2,450 ÷ 21,550) × 金額  |
| CC002       | FI   | 4,100.00  | (4,100 ÷ 21,550) × 金額  |
| CC003       | IT   | 15,000.00 | (15,000 ÷ 21,550) × 金額 |

## <a name="hierarchy-allocation-bases"></a>階層配賦基準

原価オブジェクト分析コード階層ノードを既存の配賦基準に適用することで、会計士は階層配賦基準を手動で作成できます。 この方法では、元の事前に定義された分析コード メンバー配賦基準の範囲を制限できます。 1 つの事前に定義された分析コード メンバー配賦基準を使用して、複数の階層配賦基準を作成できます。 階層配賦基準に関連付けられている原価オブジェクト分析コード階層で、範囲を維持できます。

### <a name="example-hierarchy-allocation-bases-that-are-based-on-full-time-employees-in-the-organization"></a>例: 組織のフルタイム従業員に基づく階層配賦基準
これは、簡略化された組織を記述するために作成できる原価オブジェクト分析コード階層の例です。

| 階層名 | ノード レベル 0 | ノード レベル 1 | ノード レベル 2 | 分析コード メンバー |
|----------------|--------------|--------------|--------------|-------------------|
| 組織   | 最高経営責任者          | CFO          | FICO         | CC001             |
| 組織   | 最高経営責任者          | CFO          | HR           | CC002             |
| 組織   | 最高経営責任者          | CIO          | IT           | CC003             |

前のセクションで作成された、FTE の事前に定義された分析コード メンバー配賦基準には、次のエントリが含まれます。

**統計エントリ**

| 原価オブジェクト | 説明  | 会計日 | 統計分析コード メンバー | 説明 | 大きさ |
|-------------|------|-----------------|------------------------------|---------------------|-----------|
| CC001       | HR   | 2017 年 1 月 31 日      | FTE の                        | フルタイム従業員 | 1.00      |
| CC002       | FI   | 2017 年 1 月 31 日      | FTE の                        | フルタイム従業員 | 2.00      |
| CC003       | IT   | 2017 年 1 月 31 日      | FTE の                        | フルタイム従業員 | 2.00      |

コストは、組織の最高財務責任者 (CFO) に報告するコスト センター間で配分する必要があります。 正しい配賦率は、コスト センターごとのフルタイム従業員 (Fte) の数であることを認識できます。

**階層配賦基準**

| 氏名                  | 配賦基準 | 原価オブジェクト分析コード階層 | 原価オブジェクト分析コード階層ノード |
|-----------------------|-----------------|---------------------------------|--------------------------------------|
| CFO の FTE の数 | FTE の           | 組織                    | CFO                                  |

プレビュー機能を使用すると、作成された階層配賦基準を、システム内の統計エントリに基づいて検証できます。

**配賦基準の詳細**

| 原価オブジェクト | 説明  |  大きさ |
|-------------|------|------------|
| CC001       | HR   | 1.00       |
| CC002       | FI   | 2.00       |

次のコスト配分ルールの例は、CFO 階層配賦基準内の FTE の数が配賦基準として割り当てられた場合です。

| 原価オブジェクト | 説明  | 大きさ | 配賦係数 |
|-------------|------|-----------|-------------------|
| CC001       | HR   | 1.00      | (1/3) × 金額    |
| CC002       | FI   | 2.00      | (2/3) × 金額    |

## <a name="formula-allocation-bases"></a>フォーミュラの配賦基準

フォーミュラの配賦基準では、正しい配賦基準を実現する高度な式を定義できます。 フォーミュラ配賦基準を手動で作成することができます。

フォーミュラ配賦基準を作成するときは、どの統計分析コードと原価要素分析コードを式の基準にするかを選択します。 以前に選択した分析コードに起因するすべての配賦基準は、フォーミュラ配賦基準で使用できます。

> [!NOTE]
> 以前に定義されているフォーミュラ配賦基準は、新しいフォーミュラ配賦基準の定義に使用できます。

フォーミュラ配賦基準の係数では、エイリアスを作成し、配賦基準または定数のどちらかに関連付けます。 エイリアスを使用して式を定義します。

式の定義には次の演算子を使用できます。

| 記号:  | テキスト           |
|---------|----------------|
| ( )     | かっこ    |
| \<      | より小さい   |
| \>      | より大きい    |
| +       | 追加       |
| -       | 減算    |
| \*      | 乗算 |

従来型の **IF** ステートメントはサポートされていません。 ただし、ステートメントを作成し、それが正しいかを検証できます。

| ステートメント | 検証 | 結果 |
|-----------|------------|--------|
| a \> b    | True       | 1      |
| a \> b    | いいえ      | 0      |

### <a name="example-1-a-simple-formula"></a>例 1: 単純な式

電気代は多くの場合 2 つの部分で構成されます。

- グリッドに接続されている固定料金
- kWh あたりの消費に関連付けられているコスト

電気の事前に定義された分析コード メンバー配賦基準は既に定義され、これらの値を保持しています。

**統計エントリ**

| 原価オブジェクト | 氏名 | 会計日 | 統計分析コード メンバー | 説明             | 大きさ |
|-------------|------|-----------------|------------------------------|-------------------------|-----------|
| CC001       | HR   | 2017 年 1 月 31 日      | 電気                  | 電気消費 | 2,450.00  |
| CC002       | FI   | 2017 年 1 月 31 日      | 電気                  | 電気消費 | 4,100.00  |
| CC003       | IT   | 2017 年 1 月 31 日      | 電気                  | 電気消費 | 15,000.00 |

電気を消費する原価オブジェクトに固定費を均等に振り分ける必要がある場合、コストを配賦する 2 つのオプションがあります。

- 電気固定費という事前に定義された配賦基準を新たに作成し、電気を消費する各原価オブジェクトに 1.00 の統計測定を適用します。
- 電気固定費というフォーミュラ配賦基準を作成し、システムで既に定義されている電気の事前に定義された配賦基準を利用します。 このオプションのメリットは、1 つの電気統計分析コード メンバーだけに原価計算にデータを読み込む必要があるということです。

**フォーミュラ配賦基準** 

| 氏名              | 原価要素分析コード | 統計分析コード | フォーミュラ |
|-------------------|------------------------|-----------------------|---------|
| 電気固定費 |                        | 統計要素  |         |

[**フォーミュラ**] フィールドに入力する前に、フォーミュラで使用する必要があるエイリアスを指定する必要があります。

**フォーミュラ配賦基準係数**

| エイリアス | 定数 | 配賦基準 |
|-------|----------|-----------------|
| a     |          | 電気     |
| b     | 0.01     |                 |

0 (ゼロ) が定数としてサポートされていないことに注意してください。

**フォーミュラ配賦基準**

| 氏名              | 原価要素分析コード | 統計分析コード | フォーミュラ |
|-------------------|------------------------|-----------------------|---------|
| 電気固定費 |                        | 統計要素  | a \> b  |

プレビュー機能を使用すると、作成されたフォーミュラ配賦基を、システム内の統計エントリに基づいて検証できます。

**配賦基準の詳細**

| 原価オブジェクト | 説明  | フォーミュラ           | 大きさ |
|-------------|------|-------------------|-----------|
| CC001       | HR   | 2,450.00 \> 0.01  | 1.00      |
| CC002       | FI   | 4,100.00 \> 0.01  | 1.00      |
| CC003       | IT   | 15,000.00 \> 0.01 | 1.00      |

次のコスト配分ルールの例は、電気のフォーミュラ配賦基準が配賦基準として割り当てられた場合です。

**コスト オブジェクト規模配賦係数**

| 原価オブジェクト | 氏名 | 大きさ |  配賦係数 |
|-------------|------|-----------|--------------------|
| CC001       | HR   | 1.00      | (1/3) × 金額     |
| CC002       | FI   | 1.00      | (1/3) × 金額     |
| CC003       | IT   | 1.00      | (1/3) × 金額     |

### <a name="example-2-an-advanced-formula"></a>例 2: 高度な式
この例では、電気のコストは実際に消費される kWh だけによるわけではありません。 管理は、電気使用量を減らすためのインセンティブを組み込みたいと思っています。 

| ルール              | 率 | 
|-------------------|------|
| a <= 10000,00 kWh | 0.75 |
| a > 10000,00 kWh  | 1.15 |

新しいフォーミュラ配賦基準、電気使用量、が作成されます。

**フォーミュラ配賦基準**

| 氏名              | 原価要素分析コード | 統計分析コード | フォーミュラ |
|-------------------|------------------------|-----------------------|---------|
| 電気使用量 |                        | 統計要素  |         |

[**フォーミュラ**] フィールドに入力する前に、フォーミュラで使用する必要があるエイリアスを指定する必要があります。

**フォーミュラ配賦基準係数**

| エイリアス | 定数  | 配賦基準 |
|-------|-----------|-----------------|
| a     |           | 電気     |
| b     | 10,000.00 |                 |
| 貸方     | 0.75      |                 |
| d     | 1.15      |                 |

**フォーミュラ配賦基準**

| 氏名              | 原価要素分析コード | 統計分析コード | フォーミュラ                                                    |
|-------------------|------------------------|-----------------------|------------------------------------------------------------|
| 電気固定費 |                        | 統計要素  | ((a \> b) × ((b × c) + (a – b) × d)) + ((a \<= b] × a × c) |

プレビュー機能を使用すると、作成されたフォーミュラ配賦基を、システム内の統計エントリに基づいて検証できます。

**配賦基準の詳細**

| 原価オブジェクト |    | フォーミュラ                                                                                                                             | 大きさ |
|-------------|----|-------------------------------------------------------------------------------------------------------------------------------------|-----------|
| CC001       | HR | ((2,450.00 \> 10.000.00) × ((10,000.00 × 0.75) + (2,450.00 – 10,000.00) × 1.15)) + ((2,450.00 \<= 10,000.00) × 2,450.00 × 0.75)     | 1,837.50  |
| CC002       | FI | ((4,100.00 \> 10.000.00) × ((10,000.00 × 0.75) + (4,100.00 – 10,000.00) × 1.15)) + ((4,100.00 \<= 10,000.00) × 4,100.00 × 0.75)     | 3,075.00  |
| CC003       | IT | ((15,000.00 \> 10.000.00) × ((10,000.00 × 0.75) + (15,000.00 – 10,000.00) × 1.15)) + ((15,000.00 \<= 10,000.00) × 15,000.00 × 0.75) | 1,3250.00 |

ここでは、CC003 (IT) の式の詳細を確認します。

((15,000.00 \> 10,000.00) × ((10,000.00 × 0.75) + (15,000.00 – 10,000.00) × 1.15)) + ((15,000.00 \<= 10,000.00) × 15,000.00 × 0.75) = 13,250.00

(1 × (7,500.00 + 5,000.00 × 1.15)) + (0 × 15,000.00 × 0.75)            

1 × 7,500.00 + 5,750.00 + 0 

次のコスト配分ルールの例は、電気固定費のフォーミュラ配賦基準が配賦基準として割り当てられた場合です。

| 原価オブジェクト |  説明  | 大きさ | 配賦係数                |
|-------------|----|-----------|----------------------------------|
| CC001       | HR | 1,837.50  | (1,837.50 ÷ 18,162.50) × 金額  |
| CC002       | FI | 3,075.00  | (3,075.00 ÷ 18,162.50) × 金額  |
| CC003       | IT | 13,250.00 | (13,250.00 ÷ 18,162.50) × 金額 |
