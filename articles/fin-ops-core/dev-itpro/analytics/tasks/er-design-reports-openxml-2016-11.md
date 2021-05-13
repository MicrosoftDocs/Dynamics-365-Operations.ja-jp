---
title: OPENXML 形式でレポートを生成する ER コンフィギュレーションを設計する (2016 年 11 月)
description: このトピックでは、OPENXML 形式で電子ドキュメントを生成するためのテンプレートを含む新しい電子申告 (ER) コンフィギュレーションを作成する方法について説明します。
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERModelGroupByFunctionEditor, VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0f23748f6f1d2c3045b1dc69d8e46821f67da593
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944271"
---
# <a name="er-design-a-configuration-for-generating-reports-in-openxml-format-november-2016"></a>OPENXML 形式でレポートを生成する ER コンフィギュレーションを設計する (2016 年 11 月)

[!include [banner](../../includes/banner.md)]

このトピックでは、システム管理者または電子申告開発者の役割のユーザーが、電子ドキュメントを OPENXML 形式で生成するためのテンプレートを含む新しい電子申告 (ER) のコンフィギュレーションを作成する方法を説明します。 このコンフィギュレーションは、仕入先支払を処理するために使用されます。

この例では、サンプル会社 Litware, Inc. のコンフィギュレーションを作成します。これらの手順は GBSI 会社で実行されます。

この手順を完了するには、まず 「構成プロバイダーを作成し、有効としてマークする」 に記載の手順を完了する必要があります。 テンプレートを作成するときにインポートされる Excel ファイルも必要です。 このファイルは[支払レポートのテンプレート](https://download.microsoft.com/download/3/f/0/3f0658b2-042c-43cf-a776-0f4c7f7cfe4e/SampleVendPaymWsReport.xlsx) からアクセスできます。


## <a name="upload-the-payments-data-model-configuration"></a>支払データ モデルのコンフィギュレーションをアップロードします。
1. ナビゲーション ウィンドウで、**モジュール > 組織の管理 > ワークスペース > 電子レポート** へ移動します。
2. リストにて、サンプル会社 Litware, Inc. の構成プロバイダーをマークします。この構成プロバイダーが表示されない場合は、まず [構成プロバイダーの作成および有効なプロバイダーとしてのマーク付け](er-configuration-provider-mark-it-active-2016-11.md)  に記載の手順を実行する必要があります。
3. **有効に設定** を選択します。
4. **リポジトリ** を選択します。 運営リソース タイプのリポジトリを、必要に応じて選択します。 利用可能であれば、新しいリポジトリの作成に関する次の手順を省略します。  
5. **追加** を選択してドロップ ダイアログを開きます。
6. **構成リポジトリ タイプ** フィールドで、`Operations resourcesdd` を入力します。
7. **レポジトリを作成** を選択します。
8. **OK** を選択します。
9. **開く** を選択します。
10. ツリーで、**支払モデル** を選択します。
11. **インポート** を選択します。 このデータ モデルをインポートします。 これは、新しい形式のコンフィギュレーションでデータ ソースとして使用されます。 このコンフィギュレーションが既にインポートされている場合は、この手順を省略します。  
12. **はい** を選択します。
13. 電子レポートのページに戻るまで、ページを閉じます。

## <a name="create-a-new-format-configuration"></a>新しいコンフィギュレーションの書式設定の作成
1. **コンフィギュレーションをレポートする** を選択します。
2. ツリーで、**支払モデル** を選択します。
3. **コンフィギュレーションの作成** を選択して、ドロップ ダイアログを開きます。
4. **新規** フィールドで、`Format based on data model PaymentModel` と入力します。 PaymentModel のデータ モデルに基づく形式を作成します。
5. **名前** フィールドに、`Sample worksheet report` と入力します。 サンプル ワークシート レポート  
6. **説明** フィールドで、`Sample worksheet report for vendors' payments` を入力します。 仕入先の支払い ワークシート レポートのサンプル。  
7. **データ モデル定義** フィールドで、値を入力または選択します。 **CustomerCreditTransferInitiation** の定義を選択します。  
8. **コンフィギュレーションの作成** を選択します。

## <a name="design-a-new-document-in-openxml-worksheet-format"></a>OPENXML ワークシート形式で新しいドキュメントを設計します。
1. ツリーで、**Payment model\Sample worksheet report** を選択します。
2. **デザイナー** をクリックします。
3. アクション ウィンドウで、**インポート** を選択します。
4. **Excel からインポート** を選択します。
5. **添付ファイル** を選択します。 既存の Excel ドキュメントをテンプレートとして添付します。  
6. **新規** を選択します。
7. **ファイル** を選択します。 既存の Excel ファイルをポイントします。  
8. ページを閉じます。
9. **テンプレート** フィールドで、値を入力または選択します。 テンプレートとして使用する Excel の添付ファイルを選択します。  
10. **OK** を選択します。 ER 形式のコンポーネントが、MS Excel ドキュメント参照の構造 (名前付き範囲) に基づく設計形式で作成されていることに注意して下さい。  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a>通貨コード別の合計を計算する新しいデータ ソースを作成します。
1. **マッピング** タブを選択します。
2. **ルートの追加** を選択して、ドロップ ダイアログを開きます。
3. ツリーで、**Functions\Group by** を選択します。
4. **名前** フィールドに、`PaymentByCurrency` と入力します。
5. **次の基準でグループを編集** を選択します。
6. ツリーで、**モデル** を展開し、**model\Payments** を選択します。
7. **フィールドを追加** を選択します。
8. **グループ化の対象** を選択します。
9. ツリーで、**model\Payments** を展開し、**model\Payments\Currency** を選択します。
10. **フィールドを追加** を選択します。
11. **グループ化されたフィールド** を選択します。
12. ツリーで、**model\Payments\Instructed Amount(InstructedAmount)** を選択します。
13. **フィールドを追加** を選択し、**集計フィールド** を選択します。
14. **方法** フィールドで、オプションを選択します。 **合計集計** 機能を選択します。  
15. **名前** フィールドに、`TotalInstructuredAmount` と入力します。
16. **保存** を選択します。
17. ページを閉じます。
18. **OK** を選択します。

## <a name="map-format-components-to-data-sources"></a>データ ソースへの形式のコンポーネントのマッピング
1. ツリーで、**model\Payments\Initiating Party(InitiatingParty)\Name** および **Excel\ReportHeader\CompanyName** を選択します。
2. **バインド** を選択します。
3. ツリーで、**model\Payments\Creditor\Identification\Source ID(SourceID)** および **Excel\PaymLines\VendAccountName** を選択します。
4. **バインド** を選択します。
5. ツリーで、**model\Payments\Creditor\Name** および **Excel\PaymLines\VendName** を選択します。
6. **バインド** を選択します。
7. ツリーで、**model\Payments\Creditor Agent(CreditorAgent)\Name** および **Excel\PaymLines\Bank** を選択します。
8. **バインド** を選択します。
9. ツリーで、**model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)** および **Excel\PaymLines\RoutingNumber** を選択します。
10. **バインド** を選択します。
11. ツリーで、**model\Payments\Creditor Account(CreditorAccount)\Identification\Number** および **Excel\PaymLines\AccountNumber** を選択します。
12. **バインド** を選択します。
13. ツリーで、**model\Payments\Instructed Amount(InstructedAmount)** および **Excel\PaymLines\Debit** を選択します。
14. **バインド** を選択します。
15. ツリーで、**model\Payments\Currency** および **Excel\PaymLines\Currency** を選択します。
16. **バインド** を選択します。
17. ツリーで、**PaymentByCurrency\grouped\Currency** および **Excel\SummaryLines\SummaryCurrency** を選択します。
18. **バインド** を選択します。
19. ツリーで、**PaymentByCurrency\aggregated\TotalInstructuredAmount** および **Excel\SummaryLines\SummaryAmount** を選択します。
20. **バインド** を選択します。
21. ツリーで、**PaymentByCurrency** および **Excel\SummaryLines** を選択します。
22. **バインド** を選択します。
23. ツリーで、**model\Payments** および **Excel\PaymLines** を選択します。
24. **バインド** を選択します。
25. **保存** を選択し、ページを閉じます。

## <a name="use-the-created-configuration-for-payments-processing"></a>支払処理用に作成されたコンフィギュレーションを使用する
1. **ステータスの変更** を選択します。
2. **完了** を選択します。
3. **OK** を選択します。
4. ナビゲーション ウィンドウで、**モジュール > 買掛金勘定 > 支払設定 > 支払方法** の順で移動します。
5. クイック フィルターを使用して、**支払方法** フィールドに **Electronic** 値でフィルターを適用します。
6. **編集** を選択します。
7. **ファイル形式** セクションを展開します。
8. **一般的な電子申告** フィールドで、**はい** を選択します。
9. **エクスポート形式のコンフィギュレーション** フィールドで、値を入力または選択します。 **サンプル ワークシート レポート** のコンフィギュレーションを選択します。  
10. **保存** を選択します。
11. ページを閉じます。

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a>支払仕訳帳の処理のテスト用に作成されたコンフィギュレーションを使用します。
1. ナビゲーション ウィンドウで、**モジュール > 買掛金勘定 > 支払 > 支払仕訳** の順に移動します。
2. **新規** を選択して、新しい支払仕訳を作成します。
3. **名前** フィールドで、**VendPay** と入力します。
4. **明細行** を選択します。
5. **口座** フィールドで、`GB_SI_000001` という値を指定します。
6. **借方** を `1000` に設定します。
7. **新規** を選択します。
8. **口座** フィールドで、`GB_SI_000005` という値を指定します。
9. **借方** を `2000` に設定します。
10. **通貨** フィールドで、`EUR` と入力します。
11. **相手勘定** フィールドで、`GBSI OPER` という値を指定します。
12. **支払方法** フィールドで、`Electronic` と入力します。
13. **保存** を選択します。
14. **支払の生成** を選択します。
15. **支払方法** フィールドで、`Electronic` と入力します。
16. **ファイル名** フィールドに、`Payments` と入力します。
17. **銀行口座** フィールドで、`GBSI OPER` と入力します。
18. **OK** を選択し、もう一度 **OK** を選択します。 この支払メッセージに使用される各通貨コードの支払明細行および合計の詳細を含む、作成されたワークシートを確認します。  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
