---
title: ER 水平に拡張された範囲を使用して Excel のレポートに列を動的に追加する (第 1 部 - デザイン形式)
description: この記事では、OPENXML ワークシート (Excel) ファイルとしてレポートを生成するように電子申告 (ER) 形式を構成する方法について説明します。 (第 1 部)
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 157a486252d9447c2509fe5e05b02cf1684683fd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886736"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-1---design-format"></a>ER 水平に拡張された範囲を使用して Excel のレポートに列を動的に追加する (第 1 部 - デザイン形式)

[!include [banner](../../includes/banner.md)]

次の手順は、システム管理者または電子レポートのロールに割り当てられたユーザーが、 OPENXML ワークシート (Excel) ファイル（要求された列が水平に展開される範囲として動的に作成される）としてのレポートを生成する電子レポート（ER）フォーマットをどのように設定するのか説明します。 これらの手順はどのタイプの企業でも実施できます。

これらのステップを完了するには、まず次の 3 つのタスク ガイドを完了する必要があります。

ER 構成プロバイダーを作成し、アクティブとしてマークする

ER 財務分析コードをデータ ソースとして使用する（第 1 部：データ モデルのデザイン）

ER 財務分析コードをデータ ソースとして使用する（第 2 部：モデル マッピング）

[財務分析コードのサンプル Web サービス レポート](https://download.microsoft.com/download/3/1/3/313e2090-bc0a-421f-bf96-c58da9bc0dea/SampleFinDimWsReport.xlsx) にあるサンプル レポートで、テンプレートのローカル コピーをダウンロードし、保存する必要があります。

この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。

## <a name="create-a-new-report-configuration"></a>新しいレポート設定を作成する

1. [組織管理] > [電子申告] > [コンフィギュレーション] に移動します。
2. ツリーで、`Financial dimensions sample model` を選択します。
3. [コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。
4. 新規フィールドで、`Format based on data model Financial dimensions sample model` と入力します。
    * 新規レポートのデータ ソースとして事前に作成されたモデルを使用します。  
5. 名前フィールドに、`Sample report with horizontally expandable ranges` と入力します。
    * 水平に展開可能な範囲でレポートを試します。  
6. 説明フィールドで、 `To make Excel output with dynamically adding columns` を入力します。
    * 動的に列を追加するExcelを出力  
7. [データモデル定義] フィールドで、「エントリ」を選択します。
8. [コンフィギュレーションの作成] をクリックします。

## <a name="design-the-report-format"></a>レポートフォーマットを デザインする

1. [デザイナー] をクリックします。
2. `Show details` トグル ボタンをオンにします。
3. アクション ウィンドウで、[インポート] をクリックします。
4. [Excel からインポート] をクリックします。
5. [添付ファイル] クリックします。
    * レポートのテンプレートをインポートします。 そのためにダウンロードしたExcelファイルを使用します。  
6. [新規] をクリックします。
7. [ファイル] をクリックします。
8. ページを閉じます。
9. [テンプレート] フィールドで、値を入力または選択します。
    * ダウンロードしたテンプレートを選択します。  
10. [OK] をクリックします。
    * 財務分析コードで（ユーザーダイアログ形式）選択した可能な限りの列を有するExcel出力を動的に作成するには新しい範囲を加えます。 それぞれの列のセルは単一の財務分析コードの名称を表します。  
11. [追加] をクリックしてドロップ ダイアログを開きます。
12. ツリーで、`Excel\Range` を選択します。
13. [Excelの範囲] フィールドで、`DimNames` を入力します。
    * DimNames  
14. [レプリケーションの方向] フィールドで、`Horizontal` を選択します。
15. [OK] をクリックします。
16. ツリーで、`Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal` を選択します。
17. [上へ移動] をクリックします。
18. ツリーで、`Excel = "SampleFinDimWsReport"\Cell<DimNames>` を選択します。
19. [カット] をクリックします。
20. ツリーで、`Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal` を選択します。
21. [ペースト] をクリックします。
22. ツリーで、`Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal` を展開します。
23. ツリーで、`Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical` を展開します。
24. ツリーで、`Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical` を展開します。
25. ツリーで、`Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical` を選択します。
    * 財務分析コードで（ユーザーダイアログ形式）選択した可能な限りの列を有するExcel出力を動的に作成するには新しい範囲を加えます。 それぞれの列のセルは、各レポート トランザクションの単一の財務分析コードの値を表します。  
26. [範囲を追加] をクリックします。
27. [Excelの範囲] フィールドで、`DimValues` と入力します。
    * DimValues  
28. [レプリケーションの方向] フィールドで、`Horizontal` を選択します。
29. [OK] をクリックします。
30. ツリーで、`Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>` を選択します。
31. [カット] をクリックします。
32. ツリーで、`Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal` を選択します。
33. [ペースト] をクリックします。
34. ツリーで、`Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal` を展開します。

## <a name="map-format-elements-to-data-sources"></a>フォーマットエレメントをデータソースにマッピングする

1. [マッピング] タブをクリックします。
2. ツリーで、`model: Data model Financial dimensions sample model` を展開します。
3. ツリーで、`model: Data model Financial dimensions sample model\Journal: Record list` を展開します。
4. ツリーで、`model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list` を展開します。
5. ツリーで、`model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list` を展開します。
6. ツリーで、`Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>` を選択します。
7. ツリーで、`model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String` を選択します。
8. [バインド] をクリックします。
9. ツリーで、`Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal` を選択します。
10. ツリーで、`model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list` を選択します。
11. [バインド] をクリックします。
12. ツリーで、`Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>` を選択します。
13. ツリーで、`model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real` を選択します。
14. [バインド] をクリックします。
15. ツリーで、`Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>` を選択します。
16. ツリーで、`model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real` を選択します。
17. [バインド] をクリックします。
18. ツリーで、`Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>` を選択します。
19. ツリーで、`model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String` を選択します。
20. [バインド] をクリックします。
21. ツリーで、`Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>` を選択します。
22. ツリーで、`model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date` を選択します。
23. [バインド] をクリックします。
24. ツリーで、`Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>` を選択します。
25. ツリーで、`model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String` を選択します。
26. [バインド] をクリックします。
27. ツリーで、`Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>` を選択します。
28. ツリーで、`model: Data model Financial dimensions sample model\Journal: Record list\Batch: String` を選択します。
29. [バインド] をクリックします。
30. ツリーで、`Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical` を選択します。
31. ツリーで、`model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list` を選択します。
32. [バインド] をクリックします。
33. ツリーで、`Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>` を選択します。
34. ツリーで、`model: Data model Financial dimensions sample model\Journal: Record list\Batch: String` を選択します。
35. [バインド] をクリックします。
36. ツリーで、`Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical` を選択します。
37. ツリーで、`model: Data model Financial dimensions sample model\Journal: Record list` を選択します。
38. [バインド] をクリックします。
39. ツリーで、`model: Data model Financial dimensions sample model\Dimensions setting: Record list` を展開します。
40. ツリーで、`model: Data model Financial dimensions sample model\Dimensions setting: Record list\Code: String` を選択します。
41. ツリーで、`Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>` を選択します。
42. [バインド] をクリックします。
43. ツリーで、`model: Data model Financial dimensions sample model\Dimensions setting: Record list` を選択します。
44. ツリーで、`Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal` を選択します。
45. [バインド] をクリックします。
46. ツリーで、`Excel = "SampleFinDimWsReport"\Cell<CompanyName>` を選択します。
47. ツリーで、`model: Data model Financial dimensions sample model\Company: String` を選択します。
48. [バインド] をクリックします。
49. 保存 をクリックします。
50. ページを閉じます。

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
