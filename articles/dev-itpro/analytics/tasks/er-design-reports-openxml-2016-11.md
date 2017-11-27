--- 
title: "電子申告 (ER) 用に OpenXML 形式のレポートを生成するためのコンフィギュレーションを設計する"
description: "次の手順では、システム管理者または電子申告開発者の役割のユーザーが、電子ドキュメントを OPENXML 形式で生成するためのテンプレートを含む新しい電子申告 (ER) のコンフィギュレーションを作成する方法を説明します。"
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8bbdbf882f6f73d03be0a036cb975109396e4a0d
ms.openlocfilehash: 09789957839097ba2898544102af908c198090c7
ms.contentlocale: ja-jp
ms.lasthandoff: 11/14/2017

---
# <a name="design-a-configuration-for-generating-reports-in-openxml-format-for-electronic-reporting-er"></a>電子申告 (ER) 用に OpenXML 形式のレポートを生成するためのコンフィギュレーションを設計する

[!include[task guide banner](../../includes/task-guide-banner.md)]

次の手順では、システム管理者または電子申告開発者の役割のユーザーが、電子ドキュメントを OPENXML 形式で生成するためのテンプレートを含む新しい電子申告 (ER) のコンフィギュレーションを作成する方法を説明します。 このコンフィギュレーションは、仕入先支払を処理するために使用されます。



この例では、サンプル会社 Litware, Inc. のコンフィギュレーションを作成します。これらの手順は GBSI 会社で実行されます。



これらの手順を完了するには、先に「コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け」の手順の各ステップを完了する必要があります。 Microsoft Excel ファイル、[支払レポートのテンプレート](https://go.microsoft.com/fwlink/?linkid=862266) をダウンロードして保存する必要もあります。 

## <a name="upload-the-payments-data-model-configuration"></a>支払データ モデルのコンフィギュレーションをアップロードします。
1. [組織管理] > [ワークスペース] > [電子申告] の順に移動します。
2. 一覧で、選択された行をマークします。
    * サンプル会社 Litware, Inc. のコンフィギュレーション プロバイダーを選択します。このコンフィギュレーション プロバイダーが表示されない場合は、「コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け」という手順の最初のステップを実行する必要があります。  
3. [有効に設定] をクリックします。
4. [リポジトリ] をクリックします。
    * 運営リソース タイプのリポジトリを、必要に応じて選択します。 利用可能であれば、新しいリポジトリの作成に関する次の手順を省略します。  
5. [追加] をクリックしてドロップ ダイアログを開きます。
6. [設定リポジトリ タイプ] フィールドで、「運営 リソース」と入力します。
7. [リポジトリの作成] をクリックします。
8. [OK] をクリックします。
9. [開く] をクリックします。
10. ツリーで、「支払モデル」を選択します。
11. [インポート] をクリックします。
    * このデータ モデルをインポートします。 これは、新しい形式のコンフィギュレーションでデータ ソースとして使用されます。 このコンフィギュレーションが既にインポートされている場合は、この手順を省略します。  
12. [はい] をクリックします。
13. ページを閉じます。
14. ページを閉じます。

## <a name="create-a-new-format-configuration"></a>新しいコンフィギュレーションの書式設定の作成
1. [コンフィギュレーションをレポートする] をクリックします。
2. ツリーで、「支払モデル」を選択します。
3. [コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。
4. [新規] フィールドで、「PaymentModel データ モデルに基づいた書式」と入力します。
    * PaymentModel のデータ モデルに基づく形式を作成します。  
5. [名前] フィールドに、「サンプル ワークシート レポート」と入力します。
    * サンプル ワークシート レポート  
6. [説明] フィールドに、「仕入先の支払用サンプル ワークシート レポート」と入力します。
    * 仕入先の支払用サンプル ワークシート レポート。  
7. [データモデル定義] フィールドで、値を入力または選択します。
    * 「CustomerCreditTransferInitiation」の定義を選択します。  
8. [コンフィギュレーションの作成] をクリックします。

## <a name="design-a-new-document-in-openxml-worksheet-format"></a>OPENXML ワークシート形式で新しいドキュメントを設計します。
1. ツリーで、「Payment model\Sample worksheet report」を選択します。
2. [デザイナー] をクリックします。
3. アクション ウィンドウで、[インポート] をクリックします。
4. [Excel からインポート] をクリックします。
5. [添付ファイル] クリックします。
    * 既存の Excel ドキュメントをテンプレートとして添付します。  
6. [新規] をクリックします。
7. [ファイル] をクリックします。
    * 既存の Excel ファイルをポイントします。  
8. ページを閉じます。
9. [テンプレート] フィールドで、値を入力または選択します。
    * テンプレートとして使用する Excel の添付ファイルを選択します。  
10. [OK] をクリックします。
    * ER 形式のコンポーネントが、MS Excel ドキュメント参照の構造 (名前付き範囲) に基づく設計形式で作成されていることに注意して下さい。  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a>通貨コード別の合計を計算する新しいデータ ソースを作成します。
1. [マッピング] タブをクリックします。
2. [ルートの追加] をクリックして、ドロップ ダイアログを開きます。
3. ツリーで、「Functions\Group by」を選択します。
4. [名前] フィールドで、「PaymentByCurrency」と入力します。
    * PaymentByCurrency  
5. [次の基準でグループを編集] をクリックします。
6. ツリーで、「model」を展開します。
7. ツリーで、[model\Payments] を選択します。
8. [フィールドの追加先] をクリックします。
9. [グループ化の対象] をクリックします。
10. ツリーで、[model\Payments] を展開します。
11. ツリーで、「model\Payments\Currency」を選択します。
12. [フィールドの追加先] をクリックします。
13. [グループ化されたフィールド] をクリックします。
14. ツリーで、「model\Payments\Instructed Amount(InstructedAmount)」を選択します。
15. [フィールドの追加先] をクリックします。
16. [集計] フィールドをクリックします。
17. [方法] フィールドで、オプションを選択します。
    * 合計集計機能を選択します。  
18. [名前] フィールドに、「TotalInstructuredAmount」と入力します。
    * TotalInstructuredAmount  
19. [保存] をクリックします。
20. ページを閉じます。
21. [OK] をクリックします。

## <a name="map-format-components-to-data-sources"></a>データ ソースへの形式のコンポーネントのマッピング
1. ツリーで、「model」を展開します。
2. ツリーで、[model\Payments] を展開します。
3. ツリーで、「model\Payments\Initiating Party(InitiatingParty)」を展開します。
4. ツリーで、「model\Payments\Initiating Party(InitiatingParty)\Name」を選択します。
5. ツリーで、「Excel\ReportHeader」を展開します。
6. ツリーで、「Excel\ReportHeader\CompanyName」を展開します。
7. [バインド] をクリックします。
8. ツリーで、[model\Payments\Creditor] を展開します。
9. ツリーで、「model\Payments\Creditor\Identification」を展開します。
10. ツリーで、「model\Payments\Creditor\Identification\Source ID(SourceID)」を選択します。
11. ツリーで、「Excel\PaymLines」を展開します。
12. ツリーで、「Excel\PaymLines\VendAccountName」を選択します。
13. [バインド] をクリックします。
14. ツリーで、[model\Payments\Creditor\Name] を選択します。
15. ツリーで、「Excel\PaymLines\VendName」を選択します。
16. [バインド] をクリックします。
17. ツリーで、「model\Payments\Creditor Agent(CreditorAgent)」を展開します。
18. ツリーで、「model\Payments\Creditor Agent(CreditorAgent)\Name」を選択します。
19. ツリーで、「Excel\PaymLines\Bank」を選択します。
20. [バインド] をクリックします。
21. ツリーで、「model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)」を選択します。
22. ツリーで、「Excel\PaymLines\RoutingNumber」を展開します。
23. [バインド] をクリックします。
24. ツリーで、「model\Payments\Creditor Account(CreditorAccount)」を展開します。
25. ツリーで、「model\Payments\Creditor Account(CreditorAccount)\Identification」を展開します。
26. ツリーで、「model\Payments\Creditor Account(CreditorAccount)\Identification\Number」を選択します。
27. ツリーで、「Excel\PaymLines\AccountNumber」を展開します。
28. [バインド] をクリックします。
29. ツリーで、「model\Payments\Instructed Amount(InstructedAmount)」を選択します。
30. ツリーで、「Excel\PaymLines\Debit」を展開します。
31. [バインド] をクリックします。
32. ツリーで、[model\Payments\Creditor] を展開します。
33. ツリーで、「model\Payments\Creditor Account(CreditorAccount)」を展開します。
34. ツリーで、「model\Payments\Creditor Agent(CreditorAgent)」を展開します。
35. ツリーで、「model\Payments\Currency」を選択します。
36. ツリーで、「Excel\PaymLines\Currency」を選択します。
37. [バインド] をクリックします。
38. ツリーで、「PaymentByCurrency」を展開します。
39. ツリーで、「PaymentByCurrency\grouped」を展開します。
40. ツリーで、「PaymentByCurrency\grouped\Currency」を選択します。
41. ツリーで、「Excel\SummaryLines」を展開します。
42. ツリーで、「Excel\SummaryLines\SummaryCurrency」を選択します。
43. [バインド] をクリックします。
44. ツリーで、「PaymentByCurrency\aggregated」を展開します。
45. ツリーで、「PaymentByCurrency\aggregated\TotalInstructuredAmount」を選択します。
46. ツリーで、「Excel\SummaryLines\SummaryAmount」を選択します。
47. [バインド] をクリックします。
48. ツリーで、「PaymentByCurrency」を選択します。
49. ツリーで、[Excel\SummaryLines] を選択します。
50. [バインド] をクリックします。
51. ツリーで、[model\Payments] を選択します。
52. ツリーで、「Excel\PaymLines」を選択します。
53. [バインド] をクリックします。
54. [保存] をクリックします。
55. ページを閉じます。

## <a name="use-the-created-configuration-for-payments-processing"></a>支払処理用に作成されたコンフィギュレーションを使用する
1. [状態の変更] をクリックします。
2. [完了] をクリックします。
3. [OK] をクリックします。
4. ページを閉じます。
5. ページを閉じます。
6. [買掛金勘定] > [支払設定] > [支払方法] の順に移動します。
7. クイック フィルターを使用して、[支払い方法] フィールドに値「Electronic」でフィルターを適用します。
    * 電子  
8. [編集] をクリックします。
9. [ファイル形式] セクションを展開します。
10. [一般的な電子申告] フィールドで [はい] を選択します。
11. [エクスポート形式のコンフィギュレーション] フィールドで、値を入力または選択します。
    * 「サンプル ワークシート レポート」のコンフィギュレーションを選択します。  
12. [保存] をクリックします。
13. ページを閉じます。

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a>支払仕訳帳の処理のテスト用に作成されたコンフィギュレーションを使用します。
1. [買掛金勘定] > [支払] > [支払仕訳帳] の順に移動します。
2. [新規] をクリックします。
    * 新しい支払仕訳帳を作成します。  
3. [名前] フィールドに、「VendaPay」と入力します。
    * VendPay  
4. [明細行] をクリックします。
5. [口座] フィールドで、「GB_SI_000001」値を指定します。
    * GB_SI_000001  
6. [借方] を「1000」に設定します。
7. [新規] をクリックします。
8. [口座] フィールドで、「GB_SI_000005」値を指定します。
    * GB_SI_000005  
9. [借方] を「2000」に設定します。
10. [通貨] フィールドに、「EUR」と入力します。
    * EUR / EUR  
11. [相殺アカウント] フィールドで、「GBSI OPER」値を指定します。
    * GBSI OPER  
12. [支払方法] フィールドで、「電子」と入力します。
    * 電子  
13. [保存] をクリックします。
14. [支払の生成] をクリックします。
15. [支払方法] フィールドで、「電子」と入力します。
    * 電子  
16. [ファイル名] フィールドに、「Payments」を入力します。
    * たとえば、[支払] と入力します。  
17. [銀行口座] フィールドで、「GBSI OPER」と入力します。
    * GBSI OPER  
18. [OK] をクリックします。
19. [OK] をクリックします。
    * この支払メッセージに使用される各通貨コードの支払明細行および合計の詳細を含む、作成されたワークシートを確認します。  


