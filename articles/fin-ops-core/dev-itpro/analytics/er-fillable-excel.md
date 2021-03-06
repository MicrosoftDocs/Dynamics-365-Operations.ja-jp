---
title: ドキュメントを Excel 形式で生成するためのコンフィギュレーションを設計する
description: このトピックでは、Excel テンプレートに入力する電子レポート (ER) のフォーマットを設計し、Excel 形式の出力ドキュメントを生成する方法について説明します。
author: NickSelin
ms.date: 03/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1c8d939fef4fd0f9e189ca37318c2c0306511785
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893911"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a>Excel 形式でドキュメントを生成する構成を設計する

[!include[banner](../includes/banner.md)]

ER [フォーマットのコンポーネント](general-electronic-reporting.md#FormatComponentOutbound) を持つ[電子レポート (ER) ](general-electronic-reporting.md) フォーマットの構成を設計して、 Microsoft Excel ワークブック形式の出力ドキュメントを生成するように構成することができます。 これには、特定の ERフォーマットのコンポーネントを使用する必要があります。

この機能の詳細については、[OPENXML 形式でレポートを生成する構成を設計する](tasks/er-design-reports-openxml-2016-11.md)に記載の手順に従ってください。

## <a name="add-a-new-er-format"></a>新規 ER 形式の追加

新たな ER 形式の構成を追加して、Excel ブック形式で送信ドキュメントを生成する場合は、形式の **形式のタイプ** 属性に **excel** の値を選択するか、**形式のタイプ** 属性を空白のままにしておく必要があります。

- **Excel** を選択した場合は 、Excel 形式でのみ送信ドキュメントを生成するように形式を構成することができます。
- 属性を空白のままにすると、ERフ レームワークでサポートされている任意の形式で送信ドキュメントを生成するように形式を構成することができます。

ER 形式のコンポーネントを構成するには、アクション ウィンドウで **デザイナー** を選択し、ER オペレーション デザイナーで編集用の ER 形式のコンポーネントを開きます。

![構成ページ](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a>Excel ファイル コンポーネント

### <a name="manual-entry"></a>手動入力

出力ドキュメントを Excel 形式で生成するには、**Excel\\ファイル** コンポーネントを、構成されたER形式に追加する必要があります。

![Excel\ファイル コンポーネント](./media/er-excel-format-add-file-component.png)

送信ドキュメントのレイアウトを指定するには、 **Excel\\ファイル** コンポーネントに拡張子 .xlsx の Excel ワークブックを 出力ドキュメントのテンプレートとして添付します。

> [!NOTE]
> テンプレートを手動で関連付ける場合は、[ER パラメータ](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) でこの目的に対して構成されている[ドキュメント タイプ](../../../fin-ops-core/fin-ops/organization-administration/configure-document-management.md#configure-document-types)を使用する必要があり ます。

![Excel\ファイル コンポーネントに添付ファイルを追加する](./media/er-excel-format-add-file-component2.png)

構成された ER 形式を実行する際に添付のテンプレートがどのように入力されるかを指定するには、**Excel\\ファイル** コンポーネントに入れ子になった **シート**、**範囲**、**セル** コンポーネントを追加する必要があります。 入れ子になった各コンポーネントは、Excel の名前付きアイテムに関連付けられている必要があります。

### <a name="template-import"></a>テンプレートのインポート

新しいテンプレートを空の ER 形式にインポートするには、アクションウィンドウの **インポート** タブの **Excel からインポート** を選択します。 この例では、**Excel \\ファイル** コンポーネントが自動的に作成され、インポートされたテンプレートがそのコンポーネントに関連付けられます。 検出された Excel の名前付きアイテムの一覧に基づき、必要な ER コンポーネントもすべて自動的に作成されます。

![[Excel からインポート] を選択します](./media/er-excel-format-import-template.png)

> [!NOTE]
> オプションの **シート** 要素を編集可能な形式で作成する場合は、 **Excel シート形式の要素の作成** オプションを **はい** に設定します。

## <a name="sheet-component"></a>シート コンポーネント

**シート** コンポーネントは、入力する必要がある関連付けられた Excel ブックのワークシートを示します。 Excel テンプレートのワークシートの名前は、このコンポーネントの **シート** プロパティで定義されます。

> [!NOTE]
> Excel ブックに1つのワークシートのみが存在する場合、このコンポーネントは省略可能です。

ER オペレーション デザイナーの **マッピング** タブで、**シート** コンポーネントの **有効化** プロパティを構成して、生成されるドキュメントにコンポーネントを配置するかどうかを指定することができます。

- **有効化** プロパティの式が実行時に **True** を返すように設定されている場合、または式が全く設定されていない場合は、適切なワークシートが生成されたドキュメントに配置されます。
- 実行時に **有効化** プロパティの式が **False** を返すように構成されている場合、生成されたドキュメントにはワークシートが含まれません。

![シート コンポーネントの例](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a>範囲コンポーネント

**範囲** コンポーネントは、この ER コンポーネントによって制御される必要がある Excel の範囲を示します。 範囲の名前は、このコンポーネントの **Excel の範囲** プロパティで定義されています。

**レプリケーションの方向**  プロパティでは、生成されたドキュメントで範囲を繰り返すかどうか、どのように繰り返すかを指定します。

- **レプリケーションの方向** プロパティが **レプリケーションなし** に設定されている場合、該当する Excel 範囲は、生成されたドキュメント内で繰り返されません。
- **レプリケーションの方向** プロパティが **縦方向** に設定されている場合、該当する Excel 範囲が、生成されたドキュメント内で繰り返されます。 レプリケートされたすべての範囲は、Excel テンプレートの元の範囲の下部に配置されます。 繰り返される回数は、この ER コンポーネントにバインドされている **レコード リスト** タイプのデータソース内のレコード数で定義されます。
- **レプリケーションの方向** プロパティが **水平方向** に設定されている場合、該当する Excel 範囲が、生成されたドキュメント内で繰り返されます。 レプリケートされたすべての範囲は、Excel テンプレートの元の範囲の右側に配置されます。 繰り返される回数は、この ER コンポーネントにバインドされている **レコード リスト** タイプのデータソース内のレコード数で定義されます。

水平方向のレプリケーションの詳細については、[水平方向に拡張可能な範囲を使用して、Excel レポートで列を動的に追加する](tasks/er-horizontal-1.md) に記載の手順に従ってください。

**範囲** コンポーネントは、他のネストされた ER コンポーネントを持つことができ、これは適切な Excel の名前付き範囲に値を入力する目的で使用されます。

- **テキスト** グループのいずれかのコンポーネントが値の入力に使用されている場合、その値は Excel の範囲のテキスト値として入力されます。

    > [!NOTE]
    > このパターンを使用して、アプリケーションで定義されているロケールに基づいて入力された値の書式を設定します。

- **Excel** グループの **セル** コンポーネントを使用して値を入力する場合、その値は、その **セル** コンポーネントのバインドが定義するデータ型  ( **文字列**、**実数**、**整数** など ) の値として Excel の範囲に入力されます。

    > [!NOTE]
    > このパターンを使用すると、Excel アプリケーションが、送信ドキュメントを開くローカル コンピュータのロケールに基づいて入力された値を書式設定できるようになります。

ER オペレーション デザイナーの **マッピング** タブで、**範囲** コンポーネントの **有効化** プロパティを構成して、生成されるドキュメントにコンポーネントを配置するかどうかを指定することができます。

- **有効化** プロパティの式が実行時に **True** を返すように設定されている場合、または式が全く設定されていない場合は、適切な範囲が生成されたドキュメントに入力されます。
- **有効化** プロパティの式が実行時に **True** を返すように設定されている場合、かつこの範囲が行や列全体を表していない場合、生成されたドキュメントでは適切な範囲が入力されません。
- **有効化** プロパティの式が実行時に **True** を返すように設定されている場合、かつこの範囲が行または列全体を表す場合、生成されたドキュメントにはそれらの行や列が非表示の行や列として含まれます。

## <a name="cell-component"></a>セルのコンポーネント

**セル** コンポーネントは、Excel の名前付きセル、図形、画像の入力に使用されます。 **セル** ER コンポーネントで入力する必要がある Excel の名前付きオブジェクトを指定するには、**セル** コンポーネントの **Excel の範囲** プロパティでそのオブジェクトの名前を指定する必要があります。

ER オペレーション デザイナーの **マッピング** タブで、**セル** コンポーネントの **有効化** プロパティを構成して、生成されるドキュメントにオブジェクトを配置するかどうかを指定することができます。

- **有効化** プロパティの式が実行時に **True** を返すように設定されている場合、または式が全く設定されていない場合は、適切なオブジェクトが生成されたドキュメントに入力されます。 この **セル** コンポーネントのバインディングによって、適切なオブジェクトに配置される値が指定されます。
- 実行時に **有効化** プロパティの式が **False** を返すように構成されている場合、生成されたドキュメントには適切なオブジェクトが含まれません。

**セル** コンポーネントがセルに値を入力するように構成されている場合は、プリミティブ データ型 ( **文字列**、**実数**、 **整数** など) の値を返すデータソースにバインドでき ます。 この場合、値は同一のデータ型の値としてセルに入力されます。

**セル** コンポーネントが Excel のシェイプで値を入力するように構成されている場合は、プリミティブ データ型 ( **文字列**、**実数**、 **整数** など) の値を返すデータソースにバインドでき ます。 この場合、値はこのシェイプのテキストとして Excel のシェイプに入力されます。 **文字列** ではないデータ型の値については、自動的にテキストへの変換が行われます。

> [!NOTE]
> [シェイプ テキスト] プロパティがサポートされている場合にのみ、**セル** コンポーネントを構成してシェイプに入力できます。

**セル** コンポーネントが Excel ピクチャに値を入力するように構成されている場合は、バイナリ形式で画像を表す **コンテナ** データ型の値を返すデータソースにバインドすることができます。 この場合、値が Excel ピクチャに画像として入力されます。

> [!NOTE]
> すべての Excel のピクチャとシェイプは、その左上隅が特定の Excel セル、または範囲に固定されていると考えられます。 Excel のピクチャまたはシェイプをレプリケートする場合は、固定されているセルまたは範囲をレプリケートされたセル、または範囲として構成する必要があります。

画像とシェイプを埋め込む方法の詳細については、[ER を使用して生成したドキュメントに画像やシェイプを埋め込む](electronic-reporting-embed-images-shapes.md)を参照してください。

## <a name="page-break-component"></a>改ページ コンポーネント

**改ページ** コンポーネントは、Excel が新たなページを開始するように強制します。 Excel の既定のページ設定を使用する場合、このコンポーネントは必要ありませんが、Excel で ER 形式のページ構造を使用する場合にはこのコンポーネントを推奨します。

## <a name="footer-component"></a>フッター コンポーネント

**フッター** コンポーネントは、Excel ブックの生成されたワークシートの下部にフッターを入力するために使用されます。

> [!NOTE]
> このコンポーネントを各 **シート** コンポーネントに追加して、生成された Excel ブックの異なるワークシートに異なるフッターを指定できます。

個々の **フッター** コンポーネントを構成する場合、**ヘッダー/フッターの外観** プロパティを使用して、コンポーネントが使用されるページを指定できます。 使用可能な値は次のとおりです。

- **任意** - 親 Excel ワークシートの任意のページに対して構成されている **フッター** コンポーネントを実行します。
- **最初** - 親 Excel ワークシートの最初のページに対して構成されている **フッター** コンポーネントを実行します。
- **偶数** - 親 Excel ワークシートの偶数ページに対して構成されている **フッター** コンポーネントを実行します。
- **奇数** - 親 Excel ワークシートの奇数ページに対して構成されている **フッター** コンポーネントを実行します。

1つの **シート** コンポーネントに対して、それぞれ **ヘッダー/フッターの外観** プロパティに対して異なる値を持つ複数の **フッター** コンポーネントを追加できます。 この方法で、Excel ワークシートの異なるタイプのページに異なるフッターを生成できます。

> [!NOTE]
> 1つの **シート** コンポーネントに対して、それぞれ **ヘッダー/フッターの外観** プロパティに対して異なる値を持つ複数の **フッター** コンポーネントを追加できます。 それ以外の場合、[検証エラー](er-components-inspections.md#i16) が発生します。 受信したエラー メッセージで不整合が通知されます。

追加された **フッター** コンポーネントの下に、**テキスト\\列**、**テキスト\\日時**、または他のタイプの要求された入れ子のコンポーネントを追加します。 それらのコンポーネントのバインディングを構成して、ページ フッターの入力方法を指定します。

特別な[形式コード](/office/vba/excel/concepts/workbooks-and-worksheets/formatting-and-vba-codes-for-headers-and-footers) を使用して、生成されるフッターのコンテンツを正しく書式設定することもできます。 この方法を学習するには、このトピックの後半にある[例 1](#example-1) の手順に従います。

> [!NOTE]
> 形式を構成する場合は、Excel の[制限](https://support.microsoft.com/office/excel-specifications-and-limits-1672b34d-7043-467e-8e27-269d656771c3) と 1 つのヘッダーまたはフッターの最大文字数を必ず考慮してください。

## <a name="header-component"></a>ヘッダー コンポーネント

**ヘッダー** コンポーネントは、Excel ブックの生成されたワークシートの上部にヘッダーを入力するために使用されます。 **フッター** コンポーネントと同じように使用されます。

## <a name="edit-an-added-er-format"></a>追加された ER 形式の編集

### <a name="update-a-template"></a>テンプレートの更新

更新されたテンプレートを編集可能な ER 形式にインポートするには、アクションウィンドウの **インポート** タブの **Excel から更新する** を選択します。 このプロセスでは、選択された **Excel \\ファイル** コンポーネントのテンプレートが新たなテンプレートに置き換えられます。 編集可能な ER 形式の内容は、更新されたERテンプレートの内容と同期されます。

- ER 形式のコンポーネントが編集可能なフォーマットで見つからなかった場合、新たな ERフォーマットのコンポーネントがすべての Excel 名に対して自動的に作成されます。
- 必要な Excel 名が見つからない場合、すべての ER 形式のコンポーネントが編集可能な ER 形式から削除されます。

> [!NOTE]
> オプションの **シート** 要素を編集可能な ER 形式で作成する場合は、 **Excel シート形式の要素の作成** オプションを **はい** に設定し ます。
>
> 編集可能な ER 形式に元の **シート** 要素が含まれている場合は、更新した テンプレートをインポートする際に、**Excel シート形式の要素の作成**  オプションを **はい** に設定することを推奨します。 それ以外の場合、元の **シート** 要素の入れ子になった要素はすべて最初から作成されます。 したがって、再作成された形式要素のすべてのバインドは、更新された ER 形式では失われます。

![[Excelから更新] ダイアログ ボックスの [Excel シート形式の要素] オプションの作成](./media/er-excel-format-update-template.png)

この機能の詳細については、[Excel のテンプレートを再適用することで、電子レポートの形式を変更する](modify-electronic-reporting-format-reapply-excel-template.md) に記載の手順に従っ てください。

## <a name="validate-an-er-format"></a>ER 形式の検証

編集可能な ER 形式を検証する場合は、現在使用している Excel のテンプレートに Excel 名が存在することを確認する整合性チェックが行われます。 不整合性がある場合には通知されます。 不整合がある場合は、自動的に問題を修正するオプションが表示されます。

![検証エラー メッセージ](./media/er-excel-format-validate.png)

## <a name="control-the-calculation-of-excel-formulas"></a>Excel の数式の計算の制御

Microsoft Excel ブック形式の送信ドキュメントが生成された場合、このドキュメントの一部のセルに Excel の数式が含まれている可能性があります。 **電子レポート フレームワーク機能で EPPlus ライブラリの使用を有効にする** 機能が有効になっている場合、使用中の Excel テンプレートの **計算オプション** [パラメーター](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows) の値を変更することで、数式を計算するタイミングを制御できます。

- 生成されたドキュメントに新しい範囲やセルなどが追加されるたびに、すべての従属数式を再計算するには、**自動** を選択します。
    >[!NOTE]
    > これにより、複数の関連する数式を含む Excel テンプレートでパフォーマンスの問題が発生する可能性があります。
- ドキュメントの生成時に数式の再計算を回避するには、**手動** を選択します。
    >[!NOTE]
    > 生成されたドキュメントを Excel でプレビュー用に開くと、数式の再計算が手動で強制されます。
    > このオプションは、生成されたドキュメントに数式を含むセルの値が含まれていない可能性があるため、Excel でのプレビューなしで生成されたドキュメント (PDF の変換、電子メールなど) の使用を想定する ER 送信先を構成する場合は、使用しないでください。

## <a name="example-1-format-footer-content"></a><a name="example-1"></a>例1: フッターのコンテンツを書式設定する

1. 提供されている ER コンフィギュレーションを使用して、自由書式のドキュメントを[生成](er-generate-printable-fti-forms.md) します。
2. 生成されたドキュメントのフッターを確認します。 ドキュメントの現在のページ番号とページの合計数に関する情報が含まれることに注意してください。

    ![生成されたドキュメントのフッターを Excel 形式で確認する](./media/er-fillable-excel-footer-1.gif)

3. ER 形式デザイナーで、確認のためにサンプルの ER 形式を[開き](er-generate-printable-fti-forms.md#features-that-are-implemented-in-the-sample-er-format) ます。

    **請求書** ワークシートのフッターは、**フッター** コンポーネントの下に存在する 2 つの **文字列** コンポーネントの設定に基づいて生成されます。

    - 最初の **文字列** コンポーネントは、Excel が特定の形式を強制的に適用する次の特別な形式コードを入力します。

        - **&C**- 中央にフッター テキストを配置する。
        - **&"Segoe UI,Regular"&8**- フッター テキストを 8 ポイントの "Segoe UI Regular" フォントで表示します。

    - 2 番目の **文字列** コンポーネントは、現在のドキュメントの現在のページ数とページの合計数を含むテキストを入力します。

    ![形式デザイナーのページでフッター ER 形式コンポーネントを確認する](./media/er-fillable-excel-footer-2.png)

4. サンプル ER 形式をカスタマイズして、現在のページ フッターを変更します。

    1. サンプル ER 形式に基づく派生 ER 形式の **自由形式の請求書 (Excel)** を[作成](er-quick-start2-customize-report.md#DeriveProvidedFormat) します。
    2. **請求書** ワークシートの **フッター** コンポーネントのための最初の新しい **文字列** コンポーネントのペアを追加します。

        1. 左側の会社名に対応し、8 ポイントの "Segoe UI Regular" フォント (**"&L&"Segoe UI,Regular"&8"**) で表示される **文字列** コンポーネントを追加します。
        2. 会社名を入力する **文字列** コンポーネント (**model.InvoiceBase.CompanyInfo.Name**) を追加します。

    3. **請求書** ワークシートの **フッター** コンポーネントのための 2 番目の新しい **文字列** コンポーネントのペアを追加します。

        1. 右側の処理日に対応し、8 ポイントの "Segoe UI Regular" フォント (**"&R&"Segoe UI,Regular"&8"**) で表示される **文字列** コンポーネントを追加します。
        2. カスタム形式で処理日を入力する **文字列** コンポーネント を追加します (**"&nbsp;"&DATEFORMAT(SESSIONTODAY(), "yyyy-MM-dd")**)。

        ![形式デザイナーのページでフッター ER 形式コンポーネントを確認する](./media/er-fillable-excel-footer-3.png)

    4. 派生 ER 形式の **自由書式の請求書 (Excel)** のドラフト バージョンを[完了](er-quick-start2-customize-report.md#CompleteDerivedFormat) します。

5. 印刷管理を [コンフィギュレーション](er-generate-printable-fti-forms.md#configure-print-management) して、サンプル ER 形式の代わりに派生 ER 形式の **自由書式の請求書 (Excel)** を使用します。
6. 印刷可能な FTI ドキュメントを生成し、生成されたドキュメントのフッターを確認します。

    ![生成されたドキュメントのフッターを Excel 形式で確認する](./media/er-fillable-excel-footer-4.gif)

## <a name="additional-resources"></a>追加リソース

[電子申告の概要](general-electronic-reporting.md)

[OPENXML 形式のレポートを生成するコンフィギュレーションを設計する](tasks\er-design-reports-openxml-2016-11.md)

[Excel テンプレートを再適用して電子申告形式を変更する](modify-electronic-reporting-format-reapply-excel-template.md)

[水平方向に拡張可能な範囲を活用して、Excel のレポートで動的に列を追加する](tasks/er-horizontal-1.md)

[ER を使用して生成されるドキュメントへの画像や図形の埋め込み](electronic-reporting-embed-images-shapes.md)

[Power BI にデータをプルするよう電子申告 (ER) を構成する](general-electronic-reporting-report-configuration-get-data-powerbi.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]