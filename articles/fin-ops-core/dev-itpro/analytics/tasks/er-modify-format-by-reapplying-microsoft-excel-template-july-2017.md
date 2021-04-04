---
title: Excel テンプレートの再適用による形式の変更
description: この手順にあるステップを完了するには、まず「ER - OPENXML 形式でレポートを生成するコンフィギュレーションの設計」の手順を完了する必要があります。
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6ca6707095765c25851ee864a99844a82844fae1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564317"
---
# <a name="modify-formats-by-reapplying-excel-templates"></a>Excel テンプレートの再適用による形式の変更

[!include [banner](../../includes/banner.md)]

この手順にあるステップを完了するには、まず「ER - OPENXML 形式でレポートを生成するコンフィギュレーションの設計」の手順を完了する必要があります。

この手順では、変更された Microsoft Excel テンプレートの更新を再適用して、電子申告 (ER) 形式コンフィギュレーションを変更する方法について説明します。 この手順では、サンプル会社 Litware, Inc. 用に作成した ER 形式コンフィギュレーションへ変更した Excel テンプレートをインポートし、電子ドキュメントを生成します。 この手順は、「システム管理者」または「電子レポート開発者」ロールを持つユーザーを対象としています。 これらのステップは、GBSI データ セットを使用して完了することができます。 開始する前に、ヘルプトピック「Excel テンプレートを再適用して電子申告形式を変更」 (modify-electronic-reporting-format-reapply-excel-template/) 内で一覧表示されている SampleVendPaymWsReport2.xlsx ファイルをダウンロードして保存します。

1. [組織管理] > [ワークスペース] > [電子申告] の順に移動します。
    * サンプル会社 Litware, Inc. のコンフィギュレーション プロバイダーが使用可能であり、アクティブとしてマークされていることを確認します。 この構成プロバイダーが表示されない場合は、「構成プロバイダーを作成し、有効としてマークする」 に記載の手順を完了しておく必要があります。  

## <a name="select-the-er-format"></a>ER 形式を選択する
1. [コンフィギュレーションをレポートする] をクリックします。
2. ツリーで、「Payment model」を展開します。
3. ツリーで、「Payment model\Sample worksheet report」を選択します。
4. [添付ファイル] クリックします。
    * SampleVendPaymWsReport.xlsx Excel ファイルが、支払仕訳処理のテンプレートとして現在使用されていることに注意してください。   
5. [開く] をクリックします。
    * [開く] をクリックして Excel テンプレートのレイアウトを検証します。  
    * テンプレートを確認します。 各支払い明細行には、現在以下の詳細が含まれていることに注意してください。仕入先勘定番号、仕入先の名前、銀行、支店コード、口座番号、借方、貸方、および通貨。 この例では、支払日についての詳細を追加することで、この一覧を拡張します。   
6. ページを閉じます。

## <a name="reapply-a-new-excel-template-to-er-format"></a>ER 形式に新しい Excel テンプレートを再適用する
1. [デザイナー] をクリックします。
    * 編集用に、選択した ER 形式のドラフト バージョンを開きます。  
2. アクション ウィンドウで、[インポート] をクリックします。
3. [Excel からの更新] をクリックします。
    * [テンプレートの更新] をクリックし、ファイル 「SampleVendPaymWsReport2.xlsx」 を選択します。  
    * [テンプレートの更新] をクリックし、以前にダウンロードした SampleVendPaymWsReport2.xlsx ファイルを参照して取得します。  
4. [OK] をクリックします。
    * SampleVendPaymWsReport2.xlsx テンプレートが適用されます。 ER 形式の構造は、要素を ER 形式に追加してあるテンプレートのコンテンツと同期します。 テンプレートに含まれていないERフォーマットの既存の要素は、フォーマットの定義から削除されます。  
5. ツリーで、「Excel」を選択します。
    * [テンプレート] フィールドに新しいテンプレートへの参照が含まれたことに注意してください。   
6. [添付ファイル] クリックします。
7. [開く] をクリックします。
    * [開く] をクリックして変更された Excel テンプレートのレイアウトを検証します。  
    * テンプレートを確認します。 支払日の明細行が含まれたことに注意してください。   
8. ページを閉じます。
9. ツリーで、「Excel」を展開します。
10. ツリーで、「Excel\PaymLines」を展開します。
11. ツリーで、「Excel\PaymLines\PaymDate」を選択します。
    * ER 形式にもう 1 つの項目が含まれたことに注意してください。 PaymDate というセルが Excel テンプレートに追加されています。  
12. [マッピング] タブをクリックします。
13. ツリーで、「model」を展開します。
14. ツリーで、[model\Payments] を展開します。
15. ツリーで、[model\Payments\Transaction date(TransactionDate)] を選択します。
16. [バインド] をクリックします。
    * 実行時に新しいセルに追加するデータを指定します。  
17. [保存] をクリックします。
18. ページを閉じます。

## <a name="enable-the-modified-draft-version-of-the-er-format-for-use-in-payment-journal-processing"></a>支払仕訳処理で使用するために ER 形式の変更されたドラフト バージョンを有効にする
1. アクション ウィンドウで、[設定] をクリックします。
2. [ユーザー パラメーター] をクリックします。
3. [設定の実行] フィールドで、[はい] を選択します。
4. [OK] をクリックします。
5. [編集] をクリックします。
6. [ドラフトの実行] フィールドで、[はい] を選択します。

## <a name="use-the-modified-draft-version-of-the-er-format-for-payment-journal-processing"></a>支払仕訳処理に ER 形式の変更されたドラフト バージョンを使用する

支払日という支払い明細行の新しい詳細を含む、作成したワークシートを確認します。  


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]