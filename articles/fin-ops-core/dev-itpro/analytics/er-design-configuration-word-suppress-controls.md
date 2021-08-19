---
title: 生成されたレポートの Word コンテンツ コントロールを非表示にする
description: このトピックでは、コンテンツ コントロールが非表示の Microsoft Word ファイルとしてレポートを生成する電子申告 (ER) 形式の構成方法について説明します。
author: NickSelin
ms.date: 02/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: cfabd6f544dca6f48448da4ef9ff8383c6583f8488a718a7c971ff7b39c1f2cb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6737978"
---
# <a name="suppress-word-content-controls-in-generated-reports"></a>生成されたレポートの Word コンテンツ コントロールを非表示にする

[!include [banner](../includes/banner.md)]

Microsoft Word ドキュメントとしてレポートを生成するには、レポートのテンプレートを Word ドキュメントとしてデザインする必要があります。 このテンプレートには、ランタイムに入力されるデータのプレースホルダーとして Word コンテンツ コントロールを含む必要があります。 レポートのテンプレートとして作成された Word ドキュメントを使用するには、新しい[電子申告 (ER)](general-electronic-reporting.md) [ソリューション](er-quick-start1-new-solution.md) を[構成](er-design-configuration-word.md) できます。 ソリューションには、ER [形式](general-electronic-reporting.md#FormatComponentOutbound) コンポーネントを含む ER [構成](general-electronic-reporting.md#Configuration) を含める必要があります。 この ER 形式は、レポート生成用に設計されたテンプレートを使用するように構成する必要があります。

Dynamics 365 Finance のバージョン 10.0.6 以降のバージョンでは、ER 形式のフォーミュラを構成して生成されるドキュメントで一部の Word コンテンツ コントロールを非表示にできます。

次の手順では、システム管理者または電子申告機能コンサルタントのロールに割り当てられたユーザーが、レポートを Word ファイルとして生成し、Word テンプレートを使用して構成されている生成されたレポートの一部のコンテンツ コントロールを非表示にする ER 形式を構成する方法について説明します。

これらの手順を GBSI 社を使用して説明します。

## <a name="prerequisites"></a>必要条件

これらのステップを完了するには、まず次のタスク ガイドの手順を完了する必要があります。

- [OPENXML 形式のレポートを生成するコンフィギュレーションを設計する](./tasks/er-design-reports-openxml-2016-11.md)
- [Excel テンプレートで ER の構成を再利用して Word 形式のレポートを生成する](./tasks/er-design-configuration-word-2016-11.md)

これらのタスク ガイドの手順を完了すると、次の項目が準備されます。

- Word 形式でドキュメントを生成するために構成される **ワークシート レポートのサンプル** ER 形式
- **実行可能** としてマークされている **サンプル ワークシート レポート** ER 形式の [ドラフト](general-electronic-reporting.md#component-versioning) バージョン
- 仕入先支払の処理のために **サンプル ワークシート レポート** ER 形式を使用するために構成される **電子** 支払メソッド

また、サンプル レポート用に次のテンプレートをダウンロードして保存する必要があります。

- [支払レポートのバインドされたテンプレート 2 (SampleVendPaymDocReportBounded2.docx)](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded2.docx)

## <a name="review-the-downloaded-word-template"></a><a id="tag-control"></a>ダウンロードした Word テンプレートの確認

1. Word デスクトップ アプリケーションで、先にダウンロードした **SampleVendPaymDocReportBounded2.docx** テンプレート ファイルを開きます。
2. テンプレート ファイルに、処理された支払に使用される各通貨コードの合計支払金額を示す概要セクションが含まれていることを確認します。

    - 概要セクションは、Word ドキュメントの別のテーブルに存在します。
    - このテーブルの最初の行は、セクション ヘッダーとしてテーブル列のヘッダーを保持します。
    - このテーブルの 2 番目の行は、セクションの詳細として繰り返しコンテンツ コントロールを保持します。
    - このコンテンツ コントロールは、**レポート** カスタム XML パーツの **SummaryLines** フィールドにマップされます。
    - このマッピングに基づいて、コンテンツ コントロールは編集可能な ER 形式の **SummaryLines** 要素に関連付けらされます。

    > [!NOTE]
    > 繰り返しコンテンツ コントロールは、マップされているカスタム XML パーツのフィールドに一致する **SummaryLines** キーによってタグ付けされます。

    ![Word テンプレート レイアウト。](./media/er-design-configuration-word-suppress-controls-image1.gif)

## <a name="select-the-existing-er-report-configuration"></a>既存の ER レポート コンフィギュレーションを選択します

以下の手順では、前述のタスク ガイドの手順を完了したときに構成した既存の ER 構成を再利用します。

1. **組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。
2. **コンフィギュレーションをレポートする** を選択します。
3. **構成** ページの構成ツリーで、**支払モデル** を展開し、**サンプル ワークシート レポート** を選択します。
4. **デザイナー** を選択し、選択した ER 形式のドラフト バージョンを編集します。

## <a name="replace-the-current-template-with-the-new-template"></a>現在のテンプレートを新しいテンプレートに置き換えます

現在は、Word 形式で出力を生成するテンプレートとして SampleVendPaymDocReportBounded.docx ファイルが使用されます。 次の手順では、この Word テンプレートを、以前ダウンロードした新しい Word テンプレートである SampleVendPaymDocReportBounded2.docx に置き換えます。

1. **フォーマット デザイナー** ページで、**添付** を選択します。
2. **添付ファイル** ページで **削除** を選択して、既存のテンプレートを削除します。
3. **はい** を選択して削除を確認します。
4. **新規** \> **ファイル** を選択します。
5. **参照** を選択し、以前にダウンロードした **SampleVendPaymDocReportBounded2** ファイルを参照して選択します。
6. **OK** を選択します。
7. **添付ファイル** ページを閉じます。
8. **形式デザイナー** ページの **テンプレート** フィールドで、**SampleVendPaymDocReportBounded2.docx** ファイルを入力または選択します。

## <a name="run-the-format-to-create-word-output"></a>フォーマットを実行して Word 出力を作成する

1. **買掛金勘定** \> **支払** \> **支払仕訳帳** の順に移動します。
2. **仕入先支払** ページの、**リスト** タブで、すべての支払を選択します。
3. **支払ステータス** \> **なし** を選択します。
4. **支払の生成** を選択します。
5. **支払方法** フィールドで、**電子** を選択します。
6. **銀行口座** フィールドで、 **GBSI OPER** を選択します。
7. **OK** を選択します。
8. **電子申告パラメーター** ダイアログ ボックスで、**OK** を選択し、生成された出力を分析します。

    ![仕入先支払ページでの処理に対する支払。](./media/er-design-configuration-word-suppress-controls-image2.gif)

    出力は Word 形式で表示され、概要セクションを含みます。

## <a name="configure-the-editable-format-to-suppress-the-summary-section"></a><a id="configure-to-suppress-control"></a>編集可能な形式を構成して概要セクションを非表示にする

この ER 形式を実行するユーザーの要求に基づいて、生成されたドキュメントの概要セクションを非表示にする場合は、編集可能な ER 形式を変更する必要があります。

1. **組織管理** \> **ワークスペース** \> **電子申告** に移動し、編集用の ER 形式のドラフト バージョンを開きます。
2. **コンフィギュレーションをレポートする** を選択します。 
3. **構成** ページの構成ツリーで、**支払モデル** \> **サンプル ワークシート レポート** を展開します。
4. **デザイナー** をクリックします。
5. **形式デザイナー** ページで、**Word** を展開し、**SummaryLines** を選択します。
6. **マッピング** タブで、新しいデータソースを追加し、ランタイムに、概要セクションを非表示にするかどうかをユーザーに確認します。

    1. **ルートの追加** を選択します。
    2. **データ ソースの追加** ダイアログ ボックスで、**全般\ユーザー入力パラメーター** を選択し、**'ユーザー入力パラメーター' データ ソース プロパティ** のダイアログ ボックスを開きます。
    3. **名前** フィールドに、**uipSuppress** と入力します。
    4. **ラベル** フィールドに、**概要セクションの非表示** を入力します。
    5. **操作のデータ型名** フィールドに、**NoYes** を選択または入力します。
    6. **OK** を選択します。

7. **NoYes** アプリケーション列挙型の新しいデータ ソースを追加します:

    1. **ルートの追加** を選択します。
    2. **データ ソースの追加** ダイアログ ボックスで、**Dynamics 365 for Operations\列挙** を選択し、**'列挙型' データ ソースのプロパティ** ダイアログ ボックスを開きます。
    3. **名前** フィールドに、**enumNoYes** と入力します。
    4. **ラベル** フィールドに、**オプションの非表示** を入力します。
    5. **操作のデータ型名** フィールドに、**NoYes** を選択または入力します。
    6. **OK** を選択します。

8. 選択した **SummaryLines** 形式要素に対して、選択した形式要素に関連付けられている Word コンテンツ コントロールを非表示にする場合、指定する形式を構成します。

    1. **マッピング** タブの **削除済** セクションで、**編集** 選択して、**[フォーミュラ デザイナー](general-electronic-reporting-formula-designer.md)** ページを開きます。
    2. **フォーミュラ** フィールドで、`uipSuppress = enumNoYes.Yes` というフォーミュラを入力します。
    3. **保存** を選択し、**フォーミュラ デザイナー** ページを閉じます。

        > [!NOTE]
        > この数式は、**その他のすべての形式要素が実行された後** に生成されたドキュメントに適用されます。 この式を適用するには、式が構成される形式要素としてタグ付けされた Word コンテンツ コントロール (この場合は **SummaryLines**) は生成されたドキュメントにあります。 そのコンテンツ コントロールは、それを保持する Word テーブルの行と共に完全に削除されます。 概要セクションの詳細行は、生成されたドキュメントから削除されます。
        >
        > デザイン時に、使用している Word テンプレートのコンテンツ コントロールに **削除済み** プロパティが構成されている形式要素の名前に一致するタグがない場合でも、形式要素に対して **削除済み** の式を構成できます。 デザイン時に形式を検証すると、この不整合に関する[警告](er-components-inspections.md#i14) が表示されます。
        >
        > 実行時に、使用している Word テンプレートのコンテンツ コントロールに **削除済み** プロパティが構成されている形式要素の名前に一致するタグがない場合、例外がスローされます。

    4. **マッピング** タブの **削除済み** セクションで、**親を含む** オプションを **はい** に設定します。

        > [!NOTE]
        > このオプションを **はい** にして、概要セクションの詳細を保持する行の親オブジェクトとして Word テーブル全体を削除する必要があります。 このオプションを **いいえ** に設定した場合、セクション ヘッダーの行は生成されるドキュメント内に残ります。

9. **保存** を選択し、編集可能な形式への変更を保存します。

    ![Word 形式で生成された出力。](./media/er-design-configuration-word-suppress-controls-image3.gif)

## <a name="run-the-modified-format-to-create-word-output"></a>修正済みのフォーマットを実行して Word 出力を作成する

1. **買掛金勘定** \> **支払** \> **支払仕訳帳** の順に移動します。
2. 作成した支払仕訳帳を選択し、**明細行** を選択します。
3. **仕入先支払** ページで、すべての行を選択し、**支払ステータス** \> **なし** を選択します。
4. **支払の生成** を選択します。
5. **支払方法** フィールドで、**電子** を選択します。
6. **銀行口座** フィールドで、 **GBSI OPER** を選択します。
7. **OK** を選択します。
8. **電子申告パラメーター** ダイアログ ボックスの **概要セクションの非表示** フィールドで **はい** を選択します。
9. **OK** を選択し、生成された出力を分析します。

    ![Word 形式で生成された出力。](./media/er-design-configuration-word-suppress-controls-image4.gif)

    出力が非表示なので、概要セクションが含まれていないことに注意してください。

## <a name="additional-resources"></a>追加リソース

- [OPENXML 形式のレポートを生成するコンフィギュレーションを設計する](./tasks/er-design-reports-openxml-2016-11.md)
- [Word 形式のレポートを生成するための新しい ER コンフィギュレーションを設計する](er-design-configuration-word.md)
- [Excel テンプレートで ER の構成を再利用して Word 形式のレポートを生成する](./tasks/er-design-configuration-word-2016-11.md)
- [構成済み ER コンポーネントを検査して、ランタイムの問題を回避する](er-components-inspections.md#i14)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]