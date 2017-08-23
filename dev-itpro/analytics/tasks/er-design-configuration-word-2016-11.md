--- 
title: "電子申告 (ER) 用に Microsoft Word 形式のレポートを生成するためのコンフィギュレーションを設計する"
description: "次の手順では、システム管理者または電子レポート開発者のロールを持つユーザーが、電子レポート (ER) 形式を構成して、Microsoft Word ファイルとしてレポートを生成する方法を説明します。"
author: NickSelin
manager: AnnBe
ms.date: 12/21/2016
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 5adf1d6e6314ac7ea4084cfb3fcde8b83168c7ae
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---
# <a name="design-a-configuration-for-generating-reports-in-microsoft-word-format-for-electronic-reporting-er"></a>電子申告 (ER) 用に Microsoft Word 形式のレポートを生成するためのコンフィギュレーションを設計する

[!include[task guide banner](../../includes/task-guide-banner.md)]

次の手順では、システム管理者または電子レポート開発者のロールを持つユーザーが、電子レポート (ER) 形式を構成して、Microsoft Word ファイルとしてレポートを生成する方法を説明します。 これらのステップは GBSI 会社で実行できます。

これらのステップを完了するには、「OPENXML 形式でレポートを生成する ER コンフィギュレーションの作成」タスク ガイドの手順を最初に完了する必要があります。 また事前に、サンプル レポート用に次のテンプレートをダウンロードしてローカルに保存する必要があります。

http://msdynamics.blob.core.windows.net/media/2016/10/SampleVendPaymDocReport.docx

http://msdynamics.blob.core.windows.net/media/2016/10/SampleVendPaymDocReportBounded.docx

この手順は、Microsoft Dynamics 365 for Operations バージョン 1611 に追加された機能です。


## <a name="select-the-existing-er-report-configuration"></a>既存の ER レポート コンフィギュレーションを選択します
1. [組織管理] > [ワークスペース] > [電子申告] の順に移動します。
    * コンフィギュレーション プロバイダー「Litware、Inc.」を確認します。 有効として選択されます。  
2. [コンフィギュレーションをレポートする] をクリックします。
    * OPENXML 形式でレポート出力を生成するように最初に設計された既存の ER コンフィギュレーションを再使用します。  
3. ツリーで、「Payment model」を展開します。
4. ツリーで、「Payment model\Sample worksheet report」を選択します。
5. [デザイナー] をクリックします。

## <a name="replace-the-excel-template-with-the-word-template"></a>Excel テンプレートを Word テンプレートに置き換えます
    * 現在は、OPENXML 形式で出力を生成するテンプレートとして Excel ドキュメントが使用されます。 レポートのテンプレートを Word 形式でインポートします。  
1. [添付ファイル] クリックします。
    * 既存の Excel テンプレートを、以前ダウンロードした Word テンプレート SampleVendPaymDocReport.docx に置き換えます。 このテンプレートには、ER 出力を生成するドキュメントのレイアウトのみが含まれていることに注意してください。  
2. [削除] をクリックします。
3. [はい] をクリックします。
4. [新規] をクリックします。
5. [ファイル] をクリックします。
6. [参照] をクリックします。 以前ダウンロードした SampleVendPaymDocReport.docx を参照して選択します。 [OK] をクリックします。
    * 前のステップでダウンロードしたテンプレートを選択します。  
7. [テンプレート] フィールドで、値を入力または選択します。

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a>カスタム XML 部分を追加して、Word テンプレートを拡張します。
1. [保存] をクリックします。
    * 保存アクションは、構成の変更を保存するだけでなく、添付されている Word テンプレートも更新します。 設計された形式の構造は、'報告' という名前の新しいカスタム XML 部分として、関連付けられている Word 文書にポートされます。 関連付けられている Word テンプレートには、ER 出力として生成するドキュメントのレイアウトを含むだけでなく、実行時に ER がこのテンプレートに実装するデータの構造も含まれます。  
2. [添付ファイル] クリックします。
    * ここで、カスタム XML 部分 '報告' の要素を Word ドキュメント パーツにバインドする必要があります。  
    * カスタム XML パーツの要素でバインドされたコンテンツ コントロールを含む形式としてデザイン可能な Word 文書に慣れている場合は、次のサブタスクのすべてのステップを再生して、そのようなドキュメントを作成します。 詳細については、このリンク (https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US) を参照してください。 そうでない場合は、次のサブタスクのすべてのステップをスキップします。  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a>データ バインドを行うカスタム XML 部分と共に Word を取得します。
    * Word でこのドキュメントを開き、以下の操作を行います: - [Word 開発者] タブを開きます (有効になっていない場合は、リボンをカスタマイズします)。  - XML マッピング ウィンドウを選択します。  - ルックアップで、'報告' カスタム XML 部分を選択します。  - 選択したカスタム XML 部分の要素と Word ドキュメントのコンテンツ コントロールとのマッピングを行います。  - ローカル ドライブに更新された Word ドキュメントを保存します。  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a>コンテンツ コントロールにバインドされたカスタム XML 部分と共に Word テンプレートをアップロードします。
1. [削除] をクリックします。
2. [はい] をクリックします。
    * 新しいテンプレートを追加します。 前のサブタスクのステップを完了した場合、作成してローカルに保存した Word 文書を選択します。 そうでない場合、以前ダウンロードした SampleVendPaymDocReportBounded.docx MS Word テンプレートを選択します。  
3. [新規] をクリックします。
4. [ファイル] をクリックします。
5. [参照] をクリックします。 以前ダウンロードした SampleVendPaymDocReportBounded.docx を参照して選択します。 [OK] をクリックします。
6. [テンプレート] フィールドで、前のステップでダウンロードしたドキュメントを選択します。
7. [保存] をクリックします。
8. ページを閉じます。

## <a name="execute-the-format-to-create-word-output"></a>フォーマットを実行して Word 出力を作成する
1. アクション ウィンドウで、[設定] をクリックします。
2. [ユーザー パラメーター] をクリックします。
3. [設定の実行] フィールドで、[はい] を選択します。
4. [OK] をクリックします。
5. [編集] をクリックします。
6. [ドラフトの実行] フィールドで、[はい] を選択します。
7. [保存] をクリックします。
8. ページを閉じます。
9. ページを閉じます。
10. [買掛金勘定] > [支払] > [支払仕訳帳] の順に移動します。
11. [明細行] をクリックします。
12. 一覧で、すべての行のマークを設定または解除します。
13. [支払ステータス] をクリックします。
14. [なし] をクリックします。
15. [支払の生成] をクリックします。
16. [OK] をクリックします。
17. [OK] をクリックします。
    * 生成された出力を解析します。 作成された出力が Word 形式で表示され、その出力に処理済みの支払の詳細が含まれます。  


