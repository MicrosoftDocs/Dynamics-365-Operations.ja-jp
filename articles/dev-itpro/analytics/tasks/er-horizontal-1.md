--- 
title: "Excel レポートで水平に拡張された範囲を使用して列を動的に追加する形式を設計する"
description: "次の手順は、システム管理者または電子レポートのロールに割り当てられたユーザーが、 OPENXML ワークシート (Excel) ファイル（要求された列が水平に展開される範囲として動的に作成される）としてのレポートを生成する電子レポート（ER）フォーマットをどのように設定するのか説明します。"
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d9c3cf17cd406a50a9f92e78991289f9139d7c73
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---
# <a name="design-a-format-to-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports"></a>Excel レポートで水平に拡張された範囲を使用して列を動的に追加する形式を設計する

[!include [task guide banner](../../includes/task-guide-banner.md)]

次の手順は、システム管理者または電子レポートのロールに割り当てられたユーザーが、 OPENXML ワークシート (Excel) ファイル（要求された列が水平に展開される範囲として動的に作成される）としてのレポートを生成する電子レポート（ER）フォーマットをどのように設定するのか説明します。 これらの手順はどのタイプの企業でも実施できます。

これらのステップを完了するには、まず次の 3 つのタスク ガイドを完了する必要があります。 

「ER コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け」

「ER データ ソースとしての財務分析コードの使用 (パート 1: データ モデルのデザイン)」

「ER データ ソースとしての財務分析コードの使用 (パート 2: モデル マッピング)」

[https://go.microsoft.com/fwlink/?linkid=862266](https://go.microsoft.com/fwlink/?linkid=862266) にあるサンプル レポートで、テンプレートのローカル コピーをダウンロードし、保存する必要があります。 


この手順は、Dynamics 365 for Operations、バージョン 1611 に追加された機能です。


## <a name="create-a-new-report-configuration"></a>新しいレポート設定を作成する
1. [組織管理] > [電子申告] > [コンフィギュレーション] に移動します。
2. [ツリー] フィールドで、「財務分析コード・サンプル モデル」を選択します。
3. [コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。
4. [新規] フィールドで、「財務分析コード・サンプルモデルに基づくフォーマット」を入力します。
    * 新規レポートのデータ ソースとして事前に作成されたモデルを使用します。  
5. [名称] フィールドで、「水平に展開可能な範囲でのサンプルレポート」を入力します。
    * 水平に展開可能な範囲でレポートを試します。  
6. [説明] フィールドで、「列を動的に追加するExcelを出力」を入力します。
    * 動的に列を追加するExcelを出力  
7. [データモデル定義] フィールドで、「エントリ」を選択します。
8. [コンフィギュレーションの作成] をクリックします。

## <a name="design-the-report-format"></a>レポートフォーマットを デザインする
1. [デザイナー] をクリックします。
2. [詳細を表示] トグルボタンをオンします。
3. アクション ウィンドウで、[インポート] をクリックします。
4. [Excel からインポート] をクリックします。
5. [添付ファイル] クリックします。
    * レポートの テンプレートをインポートします。 そのためにダウンロードしたExcelファイルを使用します。  
6. [新規] をクリックします。
7. [ファイル] をクリックします。
8. ページを閉じます。
9. [テンプレート] フィールドで、値を入力または選択します。
    * ダウンロードしたテンプレートを選択します。  
10. [OK] をクリックします。
    * 財務分析コードで（ユーザーダイアログ形式）選択した可能な限りの列を有するExcel出力を動的に作成するには新しい範囲を加えます。 各列のセルは単一の財務分析コードの名称を表します。  
11. [追加] をクリックしてドロップ ダイアログを開きます。
12. ツリーで、[Excel\Range] を選択します。
13. [Excelの範囲] フィールドで、「DimNames 」を入力します。
    * DimNames  
14. [レプリケーション方向] フィールドで、「水平」を選択します。
15. [OK] をクリックします。
16. ツリーで、「Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal」を選択します。
17. [上へ移動] をクリックします。
18. ツリーで、「Excel = "SampleFinDimWsReport"\Cell<DimNames>」を選択します。
19. [カット] をクリックします。
20. ツリーで、「Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal」を選択します。
21. [ペースト] をクリックします。
22. ツリーで、「Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal」を展開します。
23. ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical」を展開します。
24. ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical」を展開します。
25. ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical」を選択します。
    * 財務分析コードで（ユーザーダイアログ形式）選択した可能な限りの列を有するExcel出力を動的に作成するには新しい範囲を加えます。 各列のセルは、各報告トランザクションの単一の財務分析コードの値を表します。  
26. [範囲を追加] をクリックします。
27. [Excelの範囲] フィールドで、「DimValues」を入力します。
    * DimValues  
28. [レプリケーション方向] フィールドで、「水平」を選択します。
29. [OK] をクリックします。
30. ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>」を選択します。
31. [カット] をクリックします。
32. ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal」を選択します。
33. [ペースト] をクリックします。
34. ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal」を展開します。

## <a name="map-format-elements-to-data-sources"></a>フォーマットエレメントをデータソースにマッピングする
1. [マッピング] タブをクリックします。
2. ツリーで、「model: Data model Financial dimensions sample model」を展開します。
3. ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list」を展開します。
4. ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list」を展開します。
5. ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list」を展開します。
6. ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>」を選択します。
7. ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record listt\Code: String」を選択します。
8. [バインド] をクリックします。
9. ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal」を選択します。
10. ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list」を展開します。
11. [バインド] をクリックします。
12. ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>」を選択します。
13. ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real」を選択します。
14. [バインド] をクリックします。
15. ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>」を選択します。
16. ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real」を選択します。
17. [バインド] をクリックします。
18. ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>」を選択します。
19. ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String」を選択します。
20. [バインド] をクリックします。
21. ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>」を選択します。
22. ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date」を選択します。
23. [バインド] をクリックします。
24. ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>」を選択します。
25. ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String」を選択します。
26. [バインド] をクリックします。
27. ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>」を選択します。
28. ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Batch: String」を選択します。
29. [バインド] をクリックします。
30. ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical」を選択します。
31. ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list」を選択します。
32. [バインド] をクリックします。
33. ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>」を選択します。
34. ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Batch: String」を選択します。
35. [バインド] をクリックします。
36. ツリーで、「Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical」を選択します。
37. ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list」を選択します。
38. [バインド] をクリックします。
39. ツリーで、「model: Data model Financial dimensions sample model\Dimensions setting: Record list」を展開します。
40. ツリーで、「model: Data model Financial dimensions sample model\Dimensions setting: Record list\Code: String」を選択します。
41. ツリーで、「Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>」を選択します。
42. [バインド] をクリックします。
43. ツリーで、「model: Data model Financial dimensions sample model\Dimensions setting: Record list」を選択します。
44. ツリーで、「Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal」を選択します。
45. [バインド] をクリックします。
46. ツリーで、「Excel = "SampleFinDimWsReport"\Cell<CompanyName>」を選択します。
47. ツリーで、「model: Data model Financial dimensions sample model\Company: String」を選択します。
48. [バインド] をクリックします。
49. [保存] をクリックします。
50. ページを閉じます。


