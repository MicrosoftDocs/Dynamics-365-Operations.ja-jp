---
title: Excel テンプレートと ER 構成を再利用して Word 形式でレポートを生成
description: このトピックでは、Excel ブックとしてレポートを生成するように設計されたレポート形式で、Word ドキュメントとしてレポートを生成するように構成する方法について説明します。
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4d4eb4fd4ea32db5aa19e9d2b1300818b3aaf6fc
ms.sourcegitcommit: e40a9fac5bac9f57a6dcfe73a1f21856eab9b6a9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/02/2021
ms.locfileid: "7594987"
---
# <a name="reuse-er-configurations-with-excel-templates-to-generate-reports-in-word-format"></a>Excel テンプレートと ER 構成を再利用して Word 形式でレポートを生成

[!include [banner](../../includes/banner.md)]

レポートを Microsoft Word ドキュメントとして生成するように、新しい [電子申告 (ER)](../general-electronic-reporting.md) [形式](../general-electronic-reporting.md#FormatComponentOutbound) を [構成](../er-design-configuration-word.md) することができます。 または、最初に Excel ブックとしてレポートを生成するように設計された ER 形式を再利用できます。 この場合、Excel テンプレートを Word テンプレートに置き換える必要があります。

次の手順は、システム管理者ロールまたは電子申告開発者ロールでユーザーが、レポートを Excel ファイルとして生成するように設計された ER 形式を再利用することで、Word ファイルとしてレポートを生成する ER 形式を構成する方法を示します。

GBSI 社を例に使用して、これらの手順について解説します。

## <a name="prerequisites"></a>必要条件

これらの手順を完了するには、まず [OPENXML 形式でレポートを生成する構成を設計する](er-design-reports-openxml-2016-11.md) タスク ガイドにある手順に従う必要があります。

また、サンプル レポート用に次のテンプレートをダウンロードしてローカルに保存する必要があります。

- [支払レポート (SampleVendPaymDocReport.docx) のテンプレート](https://download.microsoft.com/download/0/d/e/0de5a87c-95fc-4dfa-958f-285cb28b5b2b/SampleVendPaymDocReport.docx)
- [支払レポート (SampleVendPaymDocReportBounded.docx) のバインドされたテンプレート](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded.docx)

これらの手順は、Dynamics 365 for Operations バージョン 1611 (2016年11月) で追加された機能に関するものです。

## <a name="select-the-existing-er-report-configuration"></a>既存の ER レポート コンフィギュレーションを選択します

1. Dynamics 365 Finance で、**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。
2. **Litware, Inc.** 構成プロバイダーが **有効** として選択されていることを確認します。 有効になっていない場合は、[構成プロバイダーを作成して、有効としてマークする](er-configuration-provider-mark-it-active-2016-11.md) タスク ガイドにある手順に従います。
3. **コンフィギュレーションをレポートする** を選択します。 OPENXML 形式でレポート出力を生成するように設計された既存の ER 構成を再利用します。
4. **構成** ページの左側ペインにある構成ツリーで、**支払モデル** を展開し、**サンプル ワークシート レポート** を選択します。

    > [!NOTE]
    > 選択した ER 形式の下書きバージョンは、**バージョン** クイックタブで編集できます。

5. **デザイナー** をクリックします。
6. **形式デザイナー** ページで、ルート形式要素のタイトルが、Excel テンプレートが現在使用されていることを示していることに注意してください。

![既存の構成の選択。](../media/er-design-configuration-word-2016-11-image01.gif)

## <a name="review-the-downloaded-word-template"></a>ダウンロードした Word テンプレートの確認

1. Word デスクトップ アプリケーションで、先にダウンロードした **SampleVendPaymDocReport.docx** テンプレート ファイルを開きます。
2. テンプレートに、ER 出力として生成するドキュメントのレイアウトのみが含まれていることを確認します。

![デスクトップ アプリケーションの Word テンプレート レイアウト。](../media/er-design-configuration-word-2016-11-image02.png)

## <a name="replace-the-excel-template-with-the-word-template-and-add-a-custom-xml-part"></a>Excel テンプレートを Word テンプレートに置き換え、カスタム XML パーツを追加する

現在は、OPENXML 形式で出力を生成するテンプレートとして Excel ドキュメントが使用されます。 このテンプレートを、以前ダウンロードした SampleVendPaymDocReport.docx Word テンプレート ファイルに置き換えます。 また、カスタム XML パーツを追加して、Word テンプレートを拡張します。

1. Finance の **形式デザイナー** ページにある **形式** タブで、**添付ファイル** を選択します。
2. **添付ファイル** ページで **削除** を選択して、既存の Excel テンプレートを削除します。 **はい** を選択して、変更を確認します。
3. **新規** \> **ファイル** を選択します。

    > [!NOTE]
    > ER パラメーターで [構成](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) されているドキュメント タイプを選択して、ER 形式テンプレートを保存する必要があります。

4. **参照** を選択し、先にダウンロードした **SampleVendPaymDocReport.docx** ファイルを参照して選択します。
5. **OK** を選択します。
6. **添付ファイル** ページを閉じます。
7. **形式デザイナー** ページの **テンプレート** フィールドで、以前に使用した Excel テンプレートの代わりに、その Word テンプレートを使用する **SampleVendPaymDocReport.docx** ファイルを入力または選択します。
8. **保存** を選択します。

    **保存** アクションは、構成の変更を保存することに加えて、添付された Word テンプレートを更新します。 設計されたフォーマットの階層構造は、**レポート** という名前の新しいカスタム XML パーツとして、添付の Word ドキュメントに追加されます。 添付された Word テンプレートには、ER 出力として生成されるドキュメントのレイアウトと、実行時に ER がそのテンプレートに入力するデータの構造が含まれます。

9. ルート形式要素のタイトルが、Word テンプレートが現在使用されていることを示していることに注意してください。

    ![Excel テンプレートを Word テンプレートに置き換え、カスタム XML パーツを追加する。](../media/er-design-configuration-word-2016-11-image03.gif)

10. **形式** タブで、**添付ファイル** を選択します。

**レポート** カスタム XML パーツの要素を Word ドキュメントのコンテンツ コントロールにマップできるようになりました。

[カスタム XML パーツ](/visualstudio/vsto/custom-xml-parts-overview) の要素にマップされた [コンテンツ コントロール](/office/client-developer/word/content-controls-in-word) を含む形式として Word ドキュメントを設計するプロセスに精通している場合は、次の手順にあるすべてのステップを実行して、ドキュメントを作成します。 詳細については、[ユーザーが入力または印刷するフォームを Word で作成](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b) を参照してください。 それ以外の場合、次の手順をスキップします。

## <a name="get-a-word-document-that-has-a-custom-xml-part-and-do-data-mapping"></a><a id='get-word-doc'></a>カスタム XML パーツを含む Word ドキュメントの取得とデータ マッピングの実行

1. Finance の **添付ファイル** ページで **開く** を選択し、Finance から選択したテンプレートをダウンロードして、ローカルで Word ドキュメントとして保存します。
3. Word デスクトップ アプリケーションで、ダウンロードしたドキュメントを開きます。
4. **開発者** タブで、**XML マッピング ウィンドウ** を選択します。

    > [!NOTE]
    > **開発者** タブがリボンに表示されない場合は、リボンをカスタマイズして追加します。

5. **XML マッピング** ウィンドウの **カスタム XML パーツ** フィールドで、**レポート** カスタム XML パーツを選択します。
6. 選択した **レポート** カスタム XML パーツの要素と Word ドキュメントのコンテンツ コントロールをマップします。
7. 更新された Word ドキュメントを **SampleVendPaymDocReportBounded.docx** としてローカルに保存します。

## <a name="review-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a>カスタム XML パーツがコンテンツ コントロールにマップされている Word テンプレートを確認

1. Word デスクトップ アプリケーションで、**SampleVendPaymDocReportBounded.docx** テンプレート ファイルを開きます。
2. テンプレートに、ER 出力として生成するドキュメントのレイアウトが含まれていることを確認します。 このテンプレートで実行時に ER が入力するデータのプレースホルダーとして使用されるコンテンツ コントロールは、**レポート** カスタム XML パーツの要素と Word ドキュメントのコンテンツ コントロールの間で構成されるマッピングに基づきます。

![デスクトップ アプリケーションの Word テンプレート プレビュー。](../media/er-design-configuration-word-2016-11-image04.png)

## <a name="upload-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a>カスタム XML パーツがコンテンツ コントロールにマップされている Word テンプレートを更新

1. Finance の **添付ファイル** ページで、**削除** を選択して、**レポート** カスタム XML パーツの要素とコンテンツ コントロールの間にマッピングがない Word テンプレート を削除します。 **はい** を選択して、変更を確認します。
2. **新規** \> **ファイル** を選択し、**レポート** カスタム XML パーツの要素とコンテンツ コントロールの間のマッピングを含む新しいテンプレート ファイルを追加します。

    > [!NOTE]
    > ER パラメーターで [構成](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) されているドキュメント タイプを選択して、ER 形式テンプレートを保存する必要があります。

3. **参照** を選択し、[カスタム XML パーツを含む Word の取得とデータ マッピングの実行](#get-word-doc) セクションで手順を実行して、ダウンロードまたは準備した **SampleVendPaymDocReportBounded.docx** ファイルを参照して選択します。
4. **OK** を選択します。
5. **添付ファイル** ページを閉じます。
6. **形式デザイナー** ページの **テンプレート** フィールドで、ダウンロードしたドキュメントを選択します。
7. **保存** を選択します。
8. **形式デザイナー** ページを閉じます。

## <a name="mark-the-configured-format-as-runnable"></a>構成された形式を実行可能としてマーク

編集可能な形式の下書きバージョンを実行するには、[実行可能](../er-quick-start2-customize-report.md#MarkFormatRunnable) にする必要があります。

1. Finance の **構成** ページにあるアクション ペインの **構成** タブの **詳細設定** グループで、**ユーザー パラメーター** を選択します。
2. **ユーザー パラメーター** ダイアログ ボックスで、**実行設定** オプションを **はい** に設定し、**OK** を選択します。
3. **編集** を選択し、必要に応じて現在のページを編集可能にします。
4. 現在選択されている **サンプル ワークシート レポート** 構成について、**ドラフトの実行** オプションを **はい** に 設定します。
5. **保存** を選択します。

## <a name="run-the-format-to-create-output-in-word-format"></a>Word 形式で出力を作成するための形式の実行

1. Finance で **買掛金勘定** \> **支払** \> **支払仕訳帳** に移動します。
2. 先に入力した支払仕訳帳で、**明細行** を選択します。
3. **仕入先支払** ページ で、グリッド内のすべての行を選択します。
4. **支払ステータス** \> **なし** を選択します。

    ![仕入先支払ページでの処理に対する支払。](../media/er-design-configuration-word-2016-11-image05.png)

5. アクション ペインで **支払の生成** を選択します。
6. 表示されるダイアログ ボックスで、次の手順に従います:

    1. **支払方法** フィールドで、**電子** を選択します。
    2. **銀行口座** フィールドで、 **GBSI OPER** を選択します。
    3. **OK** を選択します。

7. **電子レポート パラメーター** ダイアログ ボックスで、**OK** を選択します。
8. 作成された出力は、Word 形式で表示され、処理済みの支払の詳細が含まれます。 生成された出力を解析します。

    ![Word 形式で生成された出力。](../media/er-design-configuration-word-2016-11-image06.png)

## <a name="additional-resources"></a>追加リソース

- [Word 形式のレポートを生成するための新しい ER コンフィギュレーションを設計する](../er-design-configuration-word.md)
- [ER を使用して生成されるドキュメントへの画像や図形の埋め込み](../electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
