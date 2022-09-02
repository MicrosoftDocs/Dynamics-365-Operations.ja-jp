---
title: 日本の消費税レポート
description: この記事では、日本の法人向け、消費税レポートの設定および生成方法について説明します。
author: AdamTrukawka
ms.date: 06/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: atrukawk
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 28791
ms.search.form: CustBillOfExchangeEndorseListPage, CustBillOfExchangeEndorseToVendor
ms.openlocfilehash: 13465b949e9cafb49d6425c45c6947229eed8794
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268572"
---
# <a name="japan-consumption-tax-report"></a>日本の消費税レポート

[!include [banner](../includes/banner.md)]

このトピックでは、日本の法人向け、消費税レポートの設定および生成方法について説明します。

日本の消費税レポートは、**消費税計算シート** と **消費税レポート** の 2 つのレポートで構成されます。

- **消費税計算シート** : このレポートは、表 2-1 「課税売上比率/控除可能な購買税額の計算テーブル」 に対応しています。
- **消費税レポート** : このレポートは、表3 -(2) 「消費税の返品フォーム」 に対応しています。

表 2-1 および表 3-(2) の計算ルールの詳細については、[確定申告を準備するための手順 1](https://www.nta.go.jp/taxes/shiraberu/zeimokubetsu/shohi/keigenzeiritsu/pdf/0018008-056_01.pdf) を参照してください。

## <a name="prerequisites"></a>必要条件

2019 年 10 月 1 日から提出される消費税申告書を計算するには、**機能管理** ワークスペースの **消費税申告書** 機能を有効化する必要があります。 詳細については [機能管理の概要](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) を参照してください。

## <a name="setup"></a>設定

### <a name="enable-the-consumption-tax-report"></a>消費税申告を有効にする

1. **税** > **設定** > **パラメーター** > **総勘定元帳パラメーター** の順に移動します。
2. **消費税** タブの **日本の税レポート** クイックタブで、**消費税金レポート** オプションを **はい** に設定します。

### <a name="enter-japan-reporting-information-for-a-legal-entity"></a>法人の日本報告書情報を入力

1. **組織管理** > **組織** > **法人** の順に移動します。
2. **登録番号** クイックタブで、**編集** を選択します。
3. **経理担当者** フィールドに値を入力します。
4. **代表者氏名または氏名** フィールドに値を入力します。

### <a name="set-up-sales-tax-reporting-codes-for-consumption-tax-reporting"></a>詳細については、「消費税レポート コードの設定」を参照してください

消費税レポート コードの設定については、[消費税レポート コードの設定](../general-ledger/tasks/set-up-sales-tax-reporting-codes.md)に記載の手順に従って消費税レポート コードを設定します。

次の表に、日本の消費税レポート コードの例を示します。

「消費税計算シートで使用される場所」 列には、各レポート コードが使用される **消費税計算シート** ページの **品目** フィールドと、各レポート コードの **消費税計算シート レポート** の行 (表2- 1) が表示されます。 (詳細については、**品目** フィールドについては、このトピックの[日本向け消費税レポートの生成](#generate-the-japan-consumption-tax-report)の手順 4 を参照してください。 レポートの行の詳細については、[例](#example)セクションの手順 15 を参照 してください。

「消費税計算シートで使用される場所」 列には、各レポート コードが使用される **消費税計算レポート** ページの **品目** フィールドと、各レポート コードの **消費税計算レポート** の行 (表 3- (2)) が表示されます。 (詳細については、**品目** フィールドについては、このトピックの[日本向け消費税レポートの生成](#generate-the-japan-consumption-tax-report)の手順 8 を参照してください。 レポートの行の詳細については、[例](#example)セクションの手順 15 を参照 してください。

| 報告コード | レポート コード名 | 消費税計算シートで使用される場所 | 消費税計算レポートで使用される場所 | 消費税コードの設定  |
|----------------|---------------------|-------------------------------------------------------|--------------------------------------------|------------------------|
| **1**          | **課税売上**   | Item1 (Row1)   | Item1 (Row..Row6 (税率)、Row7 (合計)) | 課税売上     |
| 8001           | 課税売上に係わる消費税額   | 不使用  | Item2 (Row11..Row16 (税率))      | 消費税支払     |
| 9001           | 課税売上訂正票   | Item1 (Row1)   | 不使用    | 課税売上訂正票    |
| 7001           | 課税売上訂正票の消費税額     | 不使用   | Item5 (Row18)    | 売上訂正票上の消費税    |
| **202**        | **免税売上額**    | Item2 (Row2)    | 不使用     | 免税売上      |
| 9202           | 課税控除売上訂正票    | 202 と同じ   | 不使用     | 課税控除売上訂正票    |
| **203**        | **非課税エクスポート**    | Item3 (Row3)    | 不使用        | 免税売上    |
| 9203           | 非課税輸出に関する訂正票     | 203 と同じ     | 不使用   | 課税控除売上訂正票    |
| **206**        | **非課税売上額**    | Item6 (Row6)   | 不使用    | 免税売上      |
| 9206           | 非課税売上に関する訂正票   | 206 と同じ    | 不使用     | 課税控除売上訂正票    |
| **208**        | **課税売上に関する課税仕入**     | Item8 (Row9)、Item14 (Row17) (比率が 0.95 未満で **個別の方法** が計算方法として選択されている場合) | 不使用    | 課税対象購買     |
| 8208           | 課税売上に関連する課税購入に係わる消費税額   | 208 と同じ   | Row22、Row23   | 消費税収入     |
| 9208           | 課税売上に関連する購買訂正票   | 208 と同じ  | 不使用    | 課税対象購買訂正票     |
| 7208           | 課税売上に関する課税仕入訂正票の消費税額   | 208 と同じ    | Row22、Row23   | 購買訂正票上の消費税 |
| **214**        | **非課税売上に関連する課税対象購買**     | 品目8 (Row9)  | 不使用    | 課税対象購買   |
| 8214           | 非課税売上に関連する課税購入に係わる消費税額  | 214 と同じ  | Row22、Row23   | 消費税収入     |
| 9214           | 非課税売上に関連する課税購入訂正票   | 214 と同じ   | 不使用   | 課税対象購買訂正票   |
| 7214           | 非課税売上に関する課税購入訂正票の消費税額 | 214 と同じ | Row22、Row23  | 購買訂正票上の消費税 |
| **215**        | **一般的な課税対象購入品 (課税/非課税売上に関連する)**        | Item8 (Row9)、Item15 (Row18) (比率が 0.95 未満で **個別の方法** が計算方法として選択されている場合) | 不使用   | 課税対象購買   |
| 8215           | 一般的な課税仕入の消費税額    | 215 と同じ    | Row22、Row23      | 消費税収入    |
| 9215           | 一般的な課税仕入訂正票    | 215 と同じ  | 不使用      | 課税対象購買訂正票      |
| 7215           | 共通課税仕入訂正票の消費税額   | 215 と同じ  | Row22、Row23   | 購買訂正票上の消費税 |
| **210**        | **課税対象輸入**     | Item10 (Row13)     | 不使用     | 課税対象輸入   |
| 8210           | 課税対象輸入に係わる消費税額  | 210 と同じ    | Row22、Row23   | 使用税  |
| 9210           | 課税対象輸入の訂正票   | 210 と同じ    | 不使用    | 課税対象輸入の訂正票        |
| 7210           | 課税対象輸入に関する消費税額 - 訂正票のインポート   | 210 と同じ    | Row22、Row23   | 輸入の訂正票上の消費税   |
| **8308**       | **貸倒損失**   | 不使用   | Item6       | 消費税収入  |
| 8310           | 不良負債 - 支払済    | Item22 (Row25)    | 不使用   | 購買訂正票上の消費税 |

## <a name="set-up-sales-tax-codes"></a>消費税コードを設定します

消費税コードを設定については、[VAT レポートの消費税コード](emea-vat-reporting.md#sales-tax-codes-for-vat-reporting) と [消費税概要](../general-ledger/indirect-taxes-overview.md) に記載の手順に従います。

> [!NOTE]
> **税タイプ** フィールドで、税のタイプに **減額** または **標準** を選択します。

消費税法コードの消費税率と、レポート上の消費税率の対応は以下の通りです。

| 消費税率 | 消費税率 | 消費税額の計算 |
|----------------|----------------------|-------------------------------------------|
| 3              | 3                    | 税込み売上金額 × 3 ÷ 103      |
| 5              | 4                    | 税込み売上金額 × 4 ÷ 105      |
| 8 (標準)   | 6.3                  | 税込み売上金額 - 6.3 ÷ 108    |
| 8 (減額)    | 6.24                 | 税込み売上金額 × 6.24 ÷ 108   |
| 10             | 7.8                  | 税込み売上金額 × 7.8 ÷ 110    |

### <a name="set-up-tax-reporting-accounts-for-bad-debts"></a>不良債務に対する税務申告勘定の設定

報告するトランザクションの選択に使用される不良債務および回収された不良債務の元帳勘定を設定する。

1. **税** > **設定** > **売上税** > **税申告勘定** の順に移動します。
2. **編集** を選択します。
3. **不良債務** フィールドで、元帳勘定を指定します。 たとえば、**JPMF** の法人では、**84720** を選択します。
4. **回収済み不良債務** フィールドで、元帳勘定を指定します。 たとえば、**JPMF** の法人では、**84710** を選択します。

## <a name="generate-the-japan-consumption-tax-report"></a>日本向け消費税レポートの生成

1. **税** > **申告** > **売上税** > **消費税申告書**.の順に移動します。
2. **消費税作業シート** ダイアログ ボックスで、次のフィールドを設定します。

    | フィールド              | Description   |
    |--------------------|---------------|
    | 開始日、終了日 | 消費税精算期間の最初の日付と最後の日付を入力して、消費税を計算します。 |
    | 決済期間  | 該当する決済期間を選択します。    |
    | 申告のタイプ   | **最終** または **中間** を選択します。 |
    | 計算方法 | 課税売上と非課税売上の両方がある場合、税額控除額の計算に使用する方法を選択してください。  |
    | 修正          | 以前に生成されたレポートの修正レポートを印刷する場合は、このオプションを **はい** に設定します。 この設定により、**消費税レポート** レポートの Item26の 式が変更されます。 詳細については、このトピックの後のセクションを参照してください。</br>- 個別対応方式  </br>- 一括払方式|

3. **OK** を選択して、**消費税計算シート** ページの金額を計算します。

    ![消費税計算書ページ。](media/7ce6e142eb379f071cd6cb2866d15b5d.png)

4. **品目** フィールドの値を確認します。 これらの値は、「消費税申告」 フォームを生成する公式の推奨事項の表 2-1 (課税売上比率/控除可能な購買税額の計算テーブル) の行に入力される金額を表します。

    > [!NOTE] 
    > 次の表の 「計算」 列では、式のかっこ ([...]) がレポート コードの値を囲んでいます。

    | フィールド (行)     | Description   | 計算  |
    |-----------------|---------------|--------------|
    | Item1 (Row1)   | 課税対象売上 (税額を除外した金額)  | このフィールドの値は、次の式で算出されます: [1] – [9001]。  |
    | Item2 (Row2)   | 免税売上額  | このフィールドの値は、次の式で算出されます: [202] – [9202]。   |
    | Item3 (Row3)   | 非課税資産の輸出等の金額、海外支店等へ移送した資産額 | このフィールドの値は、次の式で算出されます: [203] – [9203]。 |
    | Item4 (Row4)   | 全課税売上高の金額  | このフィールドの値は、次の式で算出されます: **Item1** + **Item2** + **Item3**。 |
    | Item5 (Row5)   | 課税資産の譲渡等の対価の額。  | このフィールドの値は、次の式で算出されます: **Item4**。   |
    | Item6 (Row6)   | 非課税売上額   | このフィールドの値は、次の式で算出されます: [206] – [9206]。    |
    | Item7 (Row7)   | 合計売上金額   | このフィールドの値は、次の式で算出されます: **Item5** + **Item6**。   |
    | 課税売上割合 (Row8)   | 課税売上割合   | このフィールドの値は、次の式で算出されます: **Item4** ÷ **Item7**。    |
    | 品目8 (Row9)   | 課税対象購入金額 (税込み)  | このフィールドの値は、次の式で算出されます: [208] + [214] + [215] + [8208] + [8214] + [8215] – [9208] – [9214] – [9215] – [7208] – [7214] – [7215]。  |
    | Item9 (Row10)  | 課税仕入れに係る消費税額   | このフィールドの値は、税率別の **Item8 の消費税額の合計** として計算されます。   |
    | Item10 (Row13)  | 課税輸入に係る消費税の額  | このフィールドの値は、税率別の ([210] + [8210] – [9210] – [7210]) の消費税額の合計 として計算されます。  |
    | Item11 (Row14)    | 消費税等の調整額 (加算および減算)  | このフィールドの値は **0** です。   |
    | Item12 (Row15)  | 課税仕入れの税額の合計額    | このフィールドの値は、次の式で算出されます: **Item9** + **Item10** + **Item11**。   |
    | Item13 (Row16)  | **課税対象額の割合** が \>= 0.95 の場合の、課税仕入れに係る税額の合計額です    | **課税売上割合** フィールドの値が 0.95 以上の場合、このフィールドの値は **Item12** と等しくなります。 それ以外の場合、値は **0** となります。  |

    **Item14**、**Item15**、**Item16** の両方の条件が満たされた場合に計算されます。 
    
    - **課税売上割合** フィールドの値が 0.95 未満である。
    - **消費税作業シート** ダイアログ ボックスの  **計算方法** フィールドで、**個別の方法** が選択されている。
    
    それ以外の場合、これらのフィールドの値は **0** です。

    | フィールド (行)  | Description  | 計算   |
    |--------------|--------------|---------------|
    | Item14 (Row17)   | Item12 の一部を課税売上にのみ関連付けます  | このフィールドの値は、税率別の ([208] + [8208] – [9208] – [7208]) の消費税額の合計 として計算されます。   |
    | Item15 (Row18)   | Item12 のうち、課税売上と非課税売上の両方に関する部分  | このフィールドの値は、税率別の ([215] + [8215] – [9215] – [7215]) の消費税額の合計 として計算されます。  |
    | Item16 (Row19)  | 課税仕入れにかかる税金の控除額です。 | このフィールドの値は、**Item14** + **Item15** × **課税売上割合** として計算されます  |
    | Item17 (Row20)  | 一括支給方式により計算された課税仕入れに係る控除対象税額の金額  | **課税売上** フィールドの値が 0.95 未満で、**消費税作業シート** のダイアログ ボックスの **計算方法** フィールドで **合計方法** が選択されている場合、このフィールドの値は **Item12** × **課税売上率** として計算されます。 それ以外の場合、値は **0** となります。  |
    | Item18 (Row21)  | 売上比率が変更された場合の調整の対象となる固定資産の消費税の調整 (追加または減少) | このフィールドの値は **0** です。     |
    | Item19 (Row22)   | 固定資産を課税事業者 (非課税事業者) に移行した場合の消費税額の調整 (加算または減算) 額 | このフィールドの値は **0** です。  |
    | Item20 (Row23)     | 控除対象仕入税額  | **課税売上割合フィールド** の値が 0.95 以上の場合、このフィールドの値は **Item13** + **Item18** + **Item19** として算出されます。 **課税売上** フィールドの値が 0.95 未満で、**消費税作業シート** ダイアログ ボックスの **計算方法** フィールドで **個別の方法** が選択されている場合、このフィールドの値は **Item16** + **Item18** + **Item19** として計算されます。 **課税売上** フィールドの値が 0.95 未満で、**消費税作業シート** ダイアログ ボックスの **合計算出方法** フィールドで **個別の方法** が選択されている場合、このフィールドの値は **Item17** + **Item18** + **Item19** として計算されます。 |
    | Item21 (Row24)   | 購買に対する超過控除    | **Item20** フィールドの値が 0 より大きい場合、**このフィールドの値は 0** になります。 それ以外の場合、このフィールドの値は ABS(Item20) として計算され、**Item20** フィールドは **0** に設定される。   |
    | Item22 (Row25)  | 貸倒回収に係る消費税額    | このフィールドの値は、次の式で算出されます: [8310] × 6.3 ÷ 108。 **注:** レポート コード 8310 の金額は、**税務報告勘定** ページの **回収済み不良債務** フィールドに設定されている元帳勘定に関連しています。 詳細については、このトピックで前述した [不良債務に対する税務申告口座の設定](#set-up-tax-reporting-accounts-for-bad-debts) セクションを参照してください。  |

5. 税額を確定するには、**確定** を選択します。
6. 税額を確定した後に、**消費税レポート** を選択し、**消費税レポート** ページで金額を生成します。

    ![消費税報告書ページ、税額計算タブ。](media/e8aaba7ef01662b2bd6aaec8be74cc2d.png)

7. **ヘッダー** タブで、ヘッダー情報を確認します。

    | フィールド                                                                | Description                              |
    |----------------------------------------------------------------------|------------------------------------------|
    | 税務署名                                                 | 税務署名の詳細。      |
    | 会社担当者、会計担当者                         | 代表者氏名です。  |
    | 開始日、終了日                                                   | 税の計算期間。              |
    | 中間申告の開始日、中間申告の終了日 | 消費税の中間レポートの日付。 |

8. **税金計算** タブ で、**品目** フィールドの税額を確認します。 この値は、表 3-(2) (「消費税申告フォーム」) の行に入力される金額を表します。

    > [!NOTE]
    > 次の表の 「計算」 列では、式のかっこ ([...]) がレポート コードの値を囲んでいます。 消費税計算 **シート** ページの **品目フィールドの** 値は、**CalcSheet.Item** として参照されます。
    > 
    > "フィールド (行)" 列にアスタリスク (\*) が付いているフィールドは、2019 年 10 月 1 日現在、**消費税レポート** レポート (表3-(2)) で使用されません。

    | フィールド (行)  | Description   | 計算  |
    |--------------|---------------|--------------|
    | **消費税の計算**   |   &nbsp;   |   &nbsp;  |
    | Item1 (Row..Row6 (税率)、Row7 (合計)) | 課税標準額   | このフィールドの値は、千の位を四捨五入した [1] に等しくなります。  |
    | Item2 (Row11..Row16 (税率))  | 消費税額  | このフィールドの値は、税率別の ([1] + [8001]) の消費税額の合計として計算されます。   |
    | Item3\*   | 控除過大調整税額 | このフィールドの値は、次の式で算出されます: **CalcSheet.Item21** + **CalcSheet.Item22**。  |
    | Item4\*    | 控除対象仕入税額     | このフィールドの値は、**CalcSheet.Item20** と等しくなります。  |
    | Item5 (Row18)  | 売上訂正票からの税額の払戻   | このフィールドの値は、税率別の ([9001] + [7001]) の消費税額の合計として計算されます。     |
    | Item6\*        | 貸倒れに係る税額   | このフィールドの値は、次の式で算出されます: [8308] × 6.3 ÷ 108。 **注:** レポート コード 8308 の金額は、**税務報告勘定** ページの **不良債務** フィールドに設定されている元帳勘定に関連しています。 詳細については、このトピックで前述した [不良債務に対する税務申告口座の設定](#set-up-tax-reporting-accounts-for-bad-debts) セクションを参照してください。 |
    | Item7\*    | 控除税額小計   | このフィールドの値は、次の式で算出されます: **Item4** + **Item5** + **Item6**。   |
    | Item8\*      | 税還付        | 計算結果の値が正の場合は、このフィールドの値は次のように計算されます: **Item7** – **Item2** – **Item3**。 それ以外の場合、値は **0** となります。   |
    | Item9\*     | 差引税額     | 計算結果の値が正の場合は、このフィールドの値は次のように計算されます: **Item2** + **Item3** – **Item7**。 それ以外の場合、値はゼロとなります。     |
    | Item10\*     | 中間納付額  | このフィールドの値は 0 です。    |
    | Item11\*     | 支払対象の税          | **Item9** が **Item10** より大きい場合、このフィールドの値は次のように計算されます: **Item9** – **Item10**。 それ以外の場合、値はゼロとなります。     |
    | Item12\*    | 還付される税金     | **Item10** が **Item9** より大きい場合、このフィールドの値は次のように計算されます: **Item10** – **Item9**。 それ以外の場合、値はゼロとなります。    |
    | Item13\*    | 以前に申告された税 (この申告が修正後の申告の場合)   | このフィールドの値は 0 です。   |
    | Item14\*    | 納税期日 (この申告が修正後の申告の場合)    | このフィールドの値は 0 です。     |
    | Item15\*    | 課税売上金額 (課税売上割合)    | このフィールドの値は、**CalcSheet.Item4** と等しくなります。    |
    | Item16\*    | 売上金額の合計 (課税売上割合)    | このフィールドの値は、次の式で算出されます: **Item15** + [206] – [9206] and equals **CalcSheet.Item7**。    |
    | **地方消費税の計算**  | &nbsp; |   &nbsp; |
    | Item17\*   | 税還付     | このフィールドの値は、次の式で算出されます: **Item8**。   |
    | Item18\*   | 差引税額      | このフィールドの値は、次の式で算出されます: **Item9**。  |
    | Item19\*   | 税金の還付金額 (振替金額)      | このフィールドの値は、カッコ内の値が負の場合、- ((Row22×17÷63)+(Row23×22÷78)) を千単位で四捨五入した値となります。 Row22 と Row23 の計算例は、このトピックの [例](#example) の最後にあります。  |
    | Item20\*   | 税金の支払金額 (振替金額)    | このフィールドの値は、(Row22 × 17 ÷ 63) + (Row23 × 22 ÷ 78) で計算され、正の場合は千の位を丸めた値となります。 Row22 と Row23 の計算例は、このトピックの [例](#example) の最後にあります。 |
    | Item21\*   | 中間納付譲渡割額   | このフィールドの値は 0 です。   |
    | Item22\*   | 支払対象の税     | **Item20** が **Item21** より大きい場合、このフィールドの値は次のように計算されます: **Item20** – **Item21**。 それ以外の場合、値は **0** となります。    |
    | Item23\*    | 還付される税金     | **Item21** が **Item20** より大きい場合、このフィールドの値は次のように計算されます: **Item21** – **Item20**。 それ以外の場合、値は **0** となります。    |
    | Item24\*    | 以前に申告された税 (この申告が修正後の申告の場合)   | このフィールドの値は 0 です。   |
    | Item25\*      | 正味支払税額 (この申告が修正後の申告の場合) | このフィールドの値は 0 です。   |
    | Item26\*    | 消費税および地方消費税の合計額 (納付又は還付) 税額    | **消費税作業シート** ダイアログ ボックスで **変更** オプションを **はい** に設定した場合、このフィールドの値は **Item14** + **Item25** として計算されます。 それ以外の場合、この値は **Item11** + **Item22** - **Item8** – **Item12** – **Item19** – **Item23** として計算されます。    |

9. **消費税レポート** ページの **追加情報** タブで、次のフィールドを設定します。

    | フィールド                                    | Description                                                                       |
    |------------------------------------------|-----------------------------------------------------------------------------------|
    | 割賦基準の適用                        | このオプションを **はい** に設定 して、この分の基準を適用します。                        |
    | 延払基準の適用                   | 後払いを適用するするには、このオプションを **はい** に設定します。                             |
    | 工事進行基準の適用           | このオプションを **はい** に設定 して、進行基準を適用します。           |
    | 現金主義会計の適用                    | このオプションを **はい** に設定 して、現金ベースの会計を適用します。                    |
    | 課税標準額に対する消費税額の計算の特例の適用    | このオプションを **はい** に設定して、例外的な税額計算処理を適用します。    |
    | 個別対応方式                        | 税金の計算方法を個別に設定する場合は **はい** に設定します。          |
    | 一括払方式                          | 税金の計算方法を合計に設定する場合は **はい** に設定します。            |
    | 全額控除                         | 税額が全額控除される場合は、このオプションを **はい** に設定します。                 |
    | 基準期間の課税売上額 | ベンチマーク期間の課税売上高を入力します。                           |
    | 銀行情報                         | 返金方法に **銀行** が選択されている場合は、銀行口座を入力してください。    |
    | コメント                                 | レポートのコメントを入力してください。                                                    |
    | 税理士署名押印               | 税理士の名前を入力します。                                             |
    | 税理士法第 30 条の書面提出有             | ドキュメントが法律第 30 号に従って提出された場合、このオプションを **はい** に設定します。   |
    | 税理士法第 33 条の 2 の書面提出有           | ドキュメントが法律第 33-2 号に従って提出された場合、このオプションを **はい** に設定します。 |

10. 税額を確定するには、**確定** を選択します。
11. 税額を確定した後、**消費税レポート \> 印刷** を選択して、**消費税計算シート** および **消費税レポート レポート** を印刷します。

## <a name="example"></a>例

**JPMF** 法人の次の例では、消費税コードと消費税申告コードの設定、取引の計上、および日本の消費税報告書の作成と印刷を行う方法を示しています。

1. **税** > **設定** > **消費税** > **元帳転記不ループ** に移動し、**消費税支払**、**消費税収入**、**利用税費用**、**未払使用税** の主勘定を設定します。
2. **ワークスペース** > **機能管理** に移動し、**日本の消費税レポート** 機能を選択 して、**今すぐ有効化する** を選択します。
3. **税** > **間接税** > **消費税** > **消費税コード** に移動し、次の消費税コードを設定します。

    | 消費税コード | パーセンテージ | 税タイプ | Description                                                      |
    |----------------|------------|----------|------------------------------------------------------------------|
    | JP Cons        | 10         | 標準 | 率 10% の課税売上。                           |
    | JP Cons 8S     | 8          | 標準 | 率 8% の課税売上。                            |
    | JP Cons 8R     | 8          | 減額率  | 税率 8 パーセント (減額) の課税売上。                  |
    | JP ConsPoC     | 10         | 標準 | 10% の率で課税される共通購買。                |
    | JP PoC 8S      | 8          | 標準 | 8% の率で課税される共通購買。                 |
    | JP PoC 8R      | 8          | 減額率  | 8% の率で (減額) 課税される共通購買。       |
    | JP ConsEx      | 0          | 標準 | **免税** オプションに **はい** に設定されている売上をエクスポートします。      |
    | JP ConsNt      | 0          | 標準 | **免税** オプションに **はい** に設定されている非課税売上高。 |

4. **売上税コード** ページの **レポート設定** クイックタブで、レポート コードを消費税コードに割り当てる必要があります。

    次の表に、消費税レポート コードを消費税コードに割り当てる方法を示します。

    | 消費税コード | 課税売上 | 免税売上 | 消費税支払 | 課税対象購買 | 消費税収入 |
    |----------------|---------------|---------------|-------------------|-------------------|----------------------|
    | JP Cons        | 1             |               | 8001              | 208               | 8208                 |
    | JP Cons 8S     | 1             |               | 8001              | 208               | 8208                 |
    | JP Cons 8R     | 1             |               | 8001              | 208               | 8208                 |
    | JP ConsPoC     |               |               |                   | 215               | 8215                 |
    | JP PoC 8S      |               |               |                   | 215               | 8215                 |
    | JP PoC 8R      |               |               |                   | 215               | 8215                 |
    | JP ConsEx      |               | 202           |                   |                   |                      |
    | JP ConsNt      |               | 206           |                   |                   |                      |   
    
5. **売上税コード** ページの **レポート設定 - 訂正票** クイックタブで、レポート コードを消費税コードに割り当てる必要があります。

    次の表に、消費税レポート コードを消費税コードに割り当てる方法を示します。

    | 消費税コード | 課税対象売上 CN | 免税売上 CN | 消費税支払 CN | 課税対象購買 CN | 消費税収入 CN |
    |----------------|------------------|------------------|----------------------|----------------------|-------------------------|
    | JP Cons        | 9001             |    &nbsp;        | 7001                 | 9208                 | 7208                    |
    | JP Cons 8S     | 9001             |    &nbsp;        | 7001                 | 9208                 | 7208                    |
    | JP Cons 8R     | 9001             |    &nbsp;        | 7001                 | 9208                 | 7208                    |
    | JP ConsPoC     | &nbsp;           |    &nbsp;        | &nbsp;               | 9215                 | 7215                    |
    | JP PoC 8S      | &nbsp;           |    &nbsp;        | &nbsp;               | 9215                 | 7215                    |
    | JP PoC 8R      | &nbsp;           |    &nbsp;        | &nbsp;               | 9215                 | 7215                    |
    | JP ConsEx      | &nbsp;           | 9202             | &nbsp;               | &nbsp;               | &nbsp;                  |
    | JP ConsNt      | &nbsp;           | 9206             | &nbsp;               | &nbsp;               | &nbsp;                  |

    > [!NOTE]
    > 前述の構成は単なる一例です。 使用する消費税コードの構造によって、使用する構成が異なります。 消費税支払プロセスで使用される税コードごとに、値を計算して消費税レポートに転送する場合は、**レポートの設定** タブのひとつ以上のフィールドで関連する消費税レポート コードを設定する必要があります。

6. 次のトランザクションを転記します。

    たとえば、顧客請求書の場合は、**売掛金勘定** > **請求書** > **すべての自由形式請求書** に移動します。 仕入先の請求書で、**買掛金勘定** > **請求書** > **請求仕訳帳** の順に移動します。

    | 日付     | トランザクション タイプ     | 正味金額  | 課税売上に係わる消費税額 | 消費税コード | 報告コード上の予想される税基準額 / 税額 | 品目の消費税計算シートで予想される金額 | 項目の消費税報告書に記載される予定の金額 |
    |-----------------|----------------------|-------------|-------------------------------------------|----------------|------------------------------------------------------|----------------------------------------------------------------------|-----------------------------------------------------------|
    | 2020 年 1 月 1 日 | 顧客請求書     | 41,000,000  | 3,198,000 (4,100,000)                     | JP Cons        | 1 / 8001                                             | Item1                                                                | Item1、Item2                                              |
    | 2020 年 1 月 1 日 | 顧客請求書     | 280,095,592 | 17,645,796 (22,407,647)                   | JP Cons 8S     | 1 / 8001                                             | Item1                                                                | Item1、Item2                                              |
    | 2020 年 1 月 1 日 | 顧客請求書     | 62,925,925  | 3,926,520 (5,034,074)                     | JP Cons 8R     | 1 / 8001                                             | Item1                                                                | Item1、Item2                                              |
    | 2020 年 1 月 2 日 | 顧客訂正票 | \-1,435,000 | \-111,930 (-143,500)                      | JP Cons        | 9001 / 7001                                          | Item1                                                                | Item1、 Item2、Item5                                       |
    | 2020 年 1 月 2 日 | 顧客訂正票 | \-9,892,593 | \-623,233 (-791,407)                      | JP Cons 8S     | 9001 / 7001                                          | Item1                                                                | Item1、 Item2、Item5                                       |
    | 2020 年 1 月 2 日 | 顧客訂正票 | \-1,395,407 | \-87,073 (-111,632)                       | JP Cons 8R     | 9001 / 7001                                          | Item1                                                                | Item1、 Item2、Item5                                       |
    | 2020 年 1 月 1 日 | 仕入先請求書       | 31,570,000  | 2,238,600 (3,157,000)                     | JP ConsPoC     | 215 / 8215                                           | Item8、 Item15                                                        |                                                           |
    | 2020 年 1 月 1 日 | 仕入先請求書       | 201,680,000 | 11,764,667 (16,134,400)                   | JP PoC 8S      | 215 / 8215                                           | Item8、 Item15                                                        |                                                           |
    | 2020 年 1 月 1 日 | 仕入先請求書       | 40,076,000  | 2,315,502 (3,206,080)                     | JP PoC 8R      | 215 / 8215                                           | Item8、 Item15                                                        |                                                           |
    | 2020 年 1 月 2 日 | 仕入先訂正票   | \-5,900,000 | \-418,364 (-590,000)                      | JP ConsPoC     | 9215 / 7215                                          | Item8、 Item15                                                        |                                                           |
    | 2020 年 1 月 2 日 | 仕入先訂正票   | \-7,850,000 | \-453,556 (-628,000)                      | JP PoC 8R      | 9215/ 7215                                           | Item8、 Item15                                                        |                                                           |
    | 2020 年 1 月 1 日 | 顧客請求書     | 11,000,000  | 0 (0)                                     | JP ConsEx      | 202 / 該当なし                                 | Item2                                                                |                                                           |
    | 2020 年 1 月 1 日 | 顧客請求書     | 7,000,000   | 0 (0)                                     | JP ConsNt      | 206 / 該当なし                                 | Item6                                                                |                                                           |

7. **税** > **申告** > **売上税** > **消費税申告書**.の順に移動します。
8. **消費税作業シート** ダイアログ ボックスで、次の値を設定します:

    - **開始日:** 2020/1/1 (2020 年 1 月 1 日)
    - **収量日:** 2020/1/31 (2020 年 1 月 31 日)
    - **決済期間:** JP12
    - **申告タイプ:** 最終
    - **計算方法 :** 個別方法

9.  **OK** を選択します。 **消費税計算シート** ページを確認します。

    ![消費税計算書ページの例。](media/c2e67870bea8006576606dddb9241bdf.png)

    金額は以下の表のとおり算出されます。

    | フィールド  | Description   | 値    |
    |--------|---------------|----------|
    | 品目 1 (行 1)   | 課税対象売上 (税額を除外した金額)   | 371,295,517 = 41,000,000 + 280,092,592 + 6,925,925 – 1,435,000 – 9,892,593 – 1,395,407 |
    | 品目 2 (行 2)   | 免税売上額   | 11,000,000   |
    | 品目 4 (行 4)   | 課税額   | 382,295,517 = 371,295,517 + 11,000,000    |
    | 品目 5 (行 5)   | 課税資産の譲渡等の対価の額。    | 382,295,517   |
    | 品目 6 (行 6)   | 非課税売上額   | 7,000,000   |
    | 品目 7 (行 7)   | 合計売上金額   | 389,295,517 = 382,295,517 + 7,000,000  |
    | 課税売上割合 | 課税売上割合   | 0.98 = 382,295,517 ÷ 389,295,517  |
    | 品目 8 (行 8)         | 課税対象購入金額 (税込み)   | 259,576,000 = 31,570,000 + 201,680,000 + 40,076,000 – 5,900,000 – 7,850,000  |
    | 品目 9 (行 9)         | 課税仕入れに係る消費税額   | 15,446,848 = 2,238,600 + 11,764,667 + 2,315,502 – 418,364 – 453,556   |
    | 品目 12 (行 12)       | 課税仕入れの税額の合計額   | 15,446,848    |
    | 品目 13 (行 13)       | **課税対象額の割合** が \> 0.95 の場合の、課税仕入れに係る税額の合計額です | 15,446,848  |
    | 品目 20 (行 20)       | 控除対象仕入税額    | 15,446,848     |

10. **確定** を選択します。
11. **消費税レポート** を選択します。  **税金計算** タブで、データを確認します。

    ![消費税報告書ページ、税額計算タブの例。](media/ebc1627ad9422c925c43df3f4aa67070.png)

    金額は以下の表のとおり算出されます。

    | フィールド   | Description  | 値    |
    |---------|--------------|----------|
    | Item1 (Row..Row6 (税率)、Row7 (合計)) | 課税標準額  | 384,018,517 = 41,000,000 + 280,092,592 + 6,925,925   |
    | Item2 (Row11..Row16 (税率))   | 消費税額 | 24,770,316 = 3,198,000 + 17,645,796 + 3,926,520  |
    | Item4  | 控除対象仕入税額  | 15,446,848     |
    | Item5 (Row18)   | 売上訂正票からの税額の払戻    | 822,236 = 111,930 + 623,233 + 87,073  |
    | Item7   | 控除税額小計   | 16,269,084 = 15,446,848 + 822,236    |
    | Item9   | 差引税額   | 8,501,232 = 24,770,316 – 16,269,084    |
    | Item11  | 支払対象の税  | 8,501,232   |
    | Item15  | 課税売上金額 (課税売上割合) | 382,295,517    |
    | Item16  | 売上金額の合計 (課税売上割合)  | 389,295,517 = 382,295,517 + 7,000,000   |
    | Item18  | 差引税額   | 8,501,232   |
    | Item20  | 税金の支払金額 (振替金額)  | 2,333,583 = (5,257,897 × 17 ÷ 63) + (3,243,335 × 22 ÷ 78) |
    | Item22  | 支払対象の税   | 2,333,583     |

12. **確定** を選択します。
13. **消費税レポート** > **印刷** を選択します。
14. 印刷されたレポート フォームを開いて確認します。

**消費税計算シート**:

![消費税計算シート、パート 1。](media/ecc300c7be8c9af1c97d482767fa7620.png)

![消費税計算シート、パート 2。](media/650d83f8ccfea0ef924aaaf5358a1b6d.png)

**消費税レポート**:

![消費税申告書の作成。](media/ff309474b7f567efe567fd0a5ba36fb9.png)

このレポートの説明は以下の通りです:

- Row1 = 千の位を丸めた **Item1**
- Row2..Row6 = 税率 ÷ **Item1**
- Row7 = Row2 + Row3 + Row4 + Row5 + Row6
- Row11 = **Item2**
- Row12..Row16 = 税率 ÷ **Item2**
- Row11 = Row12 + Row13 + Row14 + Row15 + Row16
- Row18 = **Item5**
- Row19 = **0** (ゼロ)
- Row17 = Row18 + Row19
- Row20 = Row21 + Row22 + Row23
- Row21 = Row13
- Row22 = Row14 – Row18 6.3 パーセントの税率 (623,233) – **CalcSheet.Item9** 6.3 パーセントの税率 (11,764,667)
- Row23 = Row15 + Row16 – Row18 6.24 パーセントの税率 (87,073) – Row18 7.8 パーセントの税率 (111,930) – **CalcSheet.Item9** 6.24 パーセントの税率 (2,315,502 – 453,556 = 1,861,946) – **CalcSheet.Item9** 7.8 パーセントの税率 (2,238,600 – 418,364 = 1,820,236)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]