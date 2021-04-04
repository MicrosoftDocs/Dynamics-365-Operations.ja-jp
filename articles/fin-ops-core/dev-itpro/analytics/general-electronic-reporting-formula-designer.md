---
title: 電子申告 (ER) のフォーミュラ デザイナー
description: このトピックでは、電子申告 (ER) でフォーミュラ デザイナーを使用する方法を説明します。
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1384307182e44fe7771ad6244eca6784434827f1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568754"
---
# <a name="formula-designer-in-electronic-reporting-er"></a>電子申告 (ER) のフォーミュラ デザイナー

[!include [banner](../includes/banner.md)]

このトピックでは、電子申告 (ER) でのフォーミュラ デザイナーの使用方法を説明します。 ER の特定の電子ドキュメントの形式を設計する場合、データを変換する式を使用して、ドキュメントのフルフィルメントおよび書式設定の要件を満たすことができます。 これらの式は、Microsoft Excel の式と類似しています。 計算式では、テキスト、日時、数学、論理式、詳細、データ種類の変換関数、および他のビジネス ドメイン固有の関数など、さまざまなタイプの関数がサポートされています。

## <a name="formula-designer-overview"></a>フォーミュラ デザイナーの概要

ER はフォーミュラ デザイナーをサポートします。 したがって、設計時に次のタスクに使用できる式を実行時にコンフィギュレーションできます。

- アプリケーション データベースから受信し、ER 形式のデータ ソースとして設計された ER データ モデルに入力する必要があるデータを変換します。 (たとえば、これらの変換にはフィルタ処理、グループ化、およびデータ型の変換が含まれる可能性があります。)
- 特定の ER フォーマットのレイアウトや条件に従って電子ドキュメントを生成するため、フォーマット データを送信する必要があります。 (たとえば、書式設定は、要求された言語またはカルチャ、またはエンコードに従って行われる可能性があります)。
- 電子ドキュメントを作成するプロセスを制御します。 (たとえば、式は、実行しているデータによってフォーマットの特定の要素の出力を有効または無効にできます。 これらはドキュメントの作成プロセスを中断したり、またはユーザーにメッセージをスローすることもできます。)

次のいずれかのアクションを実行する際 **フォーミュラ デザイナー** ページを開くことができます。

- データ モデルのコンポーネントへのデータ ソース項目のバインド。
- 形式コンポーネントへのデータ ソース項目のバインド。
- データ ソースの一部である計算済フィールドのメンテナンス完了。
- ユーザー入力パラメーターの表示条件の定義。
- 形式の変換の設計。
- 形式のコンポーネントに有効にする条件の定義。
- 形式のファイル コンポーネントに対するファイル名の定義。
- プロセス制御検証の条件の定義。
- プロセス制御検証のメッセージ テキストの定義。

## <a name="data-binding"></a><a name="Binding"></a>データ バインディング

ER フォーミュラ デザイナーを使用して、データ ソースから受信したデータを変換する式を定義し、実行時に次の方法でデータ コンシューマーにデータを入力できるようにすることができます。

- アプリケーション データ ソースとランタイム パラメーターから ER データ モデルへ
- ER データ モデルから ER 形式へ
- アプリケーション データ ソースとランタイム パラメーターから ER 形式へ

次の図は、このタイプの式の設計を示しています。 この例では、式はイントラスタット テーブルの **Intrastat.AmountMST** フィールドの値を小数点以下 2 桁に丸め、丸めた値を返します。

[![データ バインド式](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg)

次の図は、このタイプの式を使用できる方法を示しています。 この例では、入力された式の結果が、**税申告モデル** データ モデルの **Transaction.InvoicedAmount** コンポーネントに反映されます。

[![使用されているデータ バインド式](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg)

実行時に、デザインされた計算式 `ROUND (Intrastat.AmountMST, 2)` は、イントラスタット テーブルの各レコードの **AmountMST** フィールドの値を小数点以下 2 桁に丸めます。 **税レポート** データ モデルの **Transaction.InvoicedAmount** コンポーネントで丸めの値を入力します。

## <a name="data-formatting"></a><a name="Transformation"></a>データの書式設定

ER フォーミュラ デザイナーは、電子ドキュメント生成の一部として送信できるよう、データ ソースから受信されたデータを書式設定する式を定義するのに使用できます。 フォーマットに対して再使用すべき、標準的なルールとして適用されるはずの書式設定があります。 この場合、フォーマット式を持つ名前付きの変換として、書式設定のコンフィギュレーションで 1 度の書式設定を導入することができます。 この名前付き変換は、作成したフォーマット式に従って出力を書式設定する必要がある多くの形式コンポーネントに後でリンクできます。

次の図は、このタイプの変換の設計を示しています。 この例では、**TrimmedString** 変換は、先頭および末尾にあるスペースを削除することにより *文字列* データ型の受信データを切り詰めます。 その後、切り詰めた文字列を返します。

[![変換](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg)

次の図は、このタイプの変換を使用できる方法を示しています。 この例では、いくつかの形式のコンポーネントは、実行時に生成する電子ドキュメントにテキストを出力として送信します。 これらすべての形式のコンポーネントは、名前で **TrimmedString** 変換へと参照します。

[![使用されている変換](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg)

前の図の **partyName** コンポーネントなどの形式コンポーネントが **TrimmedString** 変換を参照する場合、変換は生成する電子ドキュメントへの出力としてテキストを送信します。 このテキストには、先頭および末尾にあるスペースは含まれません。

個別に適用する必要のある形式の場合、特定形式コンポーネントのバインディングの個別の式として導入できます。 次の図は、このタイプの式を示しています。 この例では、**partyType** の形式コンポーネントは、データ ソースの **Model.Company.RegistrationType** フィールドからの受信データを大文字テキストに変換する式を介してデータ ソースにバインドされます。 式は、そのテキストを出力として、電子ドキュメントに送信します。

[![個々のコンポーネントに書式設定を適用](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

## <a name="process-flow-control"></a><a name="Validation"></a>プロセス フローの制御

ER フォーミュラ デザイナーは、電子ドキュメントを生成するプロセス フローを制御する式を定義するために使用できます。 実行できるタスクは次のとおりです。

- ドキュメント作成のプロセスを停止する必要がある場合を判断する条件を定義します。
- 停止したプロセスに対してユーザーにメッセージを作成する式を指定するか、または報告書作成のプロセスに関する実行ログ メッセージをスローする式を指定します。
- 電子ドキュメント生成のファイル名と作成の管理条件を指定します。

プロセス フロー制御の各ルールは、個々の検証として設計されています。 次の図は、このタイプの検証を示しています。 この例のコンフィギュレーションの説明を次に示します。

- 検証は、XML ファイルの生成中に **INSTAT** ノードが作成されたときに評価されます。
- トランザクションのリストが空である場合、検証の実行プロセスを停止し、**FALSE** を返します。
- 検証では、ユーザーの優先的に使用する言語でラベル SYS70894 のテキストを含むエラー メッセージを返します。

[![妥当性確認](./media/picture-validation.jpg)](./media/picture-validation.jpg)

ER フォーミュラ デザイナーを使用して、生成する電子ドキュメントのファイル名を生成し、ファイル作成プロセスを制御することもできます。 次の図は、このタイプのプロセス フロー制御の設計を示しています。 この例のコンフィギュレーションの説明を次に示します。

- **model.Intrastat** データ ソースからのレコードの一覧はバッチに分かれています。 バッチごとに、最大1,000 レコードが含まれています。
- 出力は、作成されたバッチごとに XML 形式のファイル 1 つを含む zip ファイルを作成します。
- 式はファイル名とファイル名拡張子を連結して、生成する電子ドキュメントにファイル名を返します。 2 番目のバッチ以降すべてのバッチには、ファイル名の接尾語としてバッチ ID が表示されます。
- 式は、(**TRUE** を返すことで) 少なくともレコードを 1 つ含むバッチのファイル作成プロセスを有効にします。

[![プロセス フローの制御](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

## <a name="document-content-control"></a><a name="Enabled"></a>ドキュメント コンテンツ コントロール

ER フォーミュラ デザイナーを使用して、実行時に生成される電子ドキュメントに入れるデータを制御する式を構成できます。 式は、実行しているデータおよび構成されたロジックに応じて、フォーマットの特定の要素の出力を有効または無効にできます。 これらの式は、**操作デザイナー** ページの **マッピング** タブの **有効** フィールドで、単一のフォーマット要素に対して入力できます。 *ブール* 値を返すロジック条件として式を入力できます。

- 条件が **True** を返す場合、現在のフォーマット要素が実行されます。
- 条件が **False** を返す場合、現在のフォーマット要素はスキップされます。

次の図は、このタイプの式を示しています。 (Microsoft が提供する **ISO20022 口座振替 (NO)** バージョン 11.12.11例として使用されます。) **XMLHeader** 形式コンポーネントは、ISO 20022 XML のメッセージ標準に従って、口座振替メッセージの構造を記述するように構成されています。 **XMLHeader/Document/CstmrCdtTrfInitn/PmtInf/CdtTrfTxInf/RmtInf/Ustrd** 形式コンポーネントは、生成されたメッセージに **Ustrd** XML 要素を追加し、送金情報を非構造化形式で次の XML 要素のテキストとして配置するように構成されています。

- **PaymentNotes** コンポーネントは、支払票のテキストを生成するために使用されます。
- **DelimitedSequence** コンポーネントは、現在の口座振替の決済に使用されるコンマ区切りの請求書番号を生成します。

[![PaymentNotes および DelimitedSequence コンポーネント](./media/GER-FormulaEditor-ControlContent-1.png)](./media/GER-FormulaEditor-ControlContent-1.png)

> [!NOTE]
> **PaymentNotes** および **DelimitedSequence** コンポーネントは疑問符を使用してラベル付けされます。 疑問符は、コンポーネントの使用が条件付きであることを示します。 この場合、コンポーネントの使用は次の条件に基づいています。
>
> - **PaymentNotes** コンポーネントに定義されている `@.PaymentsNotes <> ""` 式は、(**TRUE** を返すことにより) そのテキストが現在の口座振替に対して空白でない場合、**Ustrd** XML 要素に支払票のテキストを入力することができます。
>
>    [![PaymentNotes コンポーネントの式](./media/GER-FormulaEditor-ControlContent-2.png)](./media/GER-FormulaEditor-ControlContent-2.png)
>
> - **DelimitedSequence** コンポーネント用に定義された `@.PaymentsNotes = ""` 式により、(**TRUE** を返すことにより) その口座振替の支払票のテキストが空白の場合、現在の口座振替の決済に使用される請求書番号のコンマ区切りリストを **Ustrd** XML 要素に入力することができます。
>
>    [![DelimitedSequence コンポーネントの式](./media/GER-FormulaEditor-ControlContent-3.png)](./media/GER-FormulaEditor-ControlContent-3.png)
> 
> この設定に基づいて、各債務者の支払いに対して生成されるメッセージ **Ustrd** XML 要素には、支払票のテキスト、またはそのテキストが空白の場合は、支払い決済に使用される請求書番号のコンマ区切りのリストが含まれます。

## <a name="validation-of-configured-formulas"></a><a name="TestFormula"></a>構成された式の検証

**フォーミュラ デザイナー** ページで,  **テスト** を選択して、構成された式の動作を検証します。

[![テストを選択して式を検証する](./media/ER-FormulaTest-Start.png)](./media/ER-FormulaTest-Start.png)

式の引数の値が必要な場合、**フォーミュラ デザイナー** ページから **テスト式** ダイアログ ボックスを開くことができます。 ほとんどの場合、構成されたバインドは設計時に実行されないため、これらの引数は手動で定義する必要があります。 **フォーミュラ デザイナー** ページで,  **テスト結果** タブには、構成された式の実行結果が表示されます。

次の例は、対外貿易ドメイン用に構成された式をテストして、イントラスタット商品コードに数字のみが含まれていることを確認する方法を示しています。

この式をテストする場合、**テスト式** ダイアログ ボックスを使用して、テスト用のイントラスタット商品コードの値を指定できます。

[![テスト用のイントラスタット商品コードを指定する](./media/ER-FormulaTest-Start-EnterArguments.png)](./media/ER-FormulaTest-Start-EnterArguments.png)

イントラスタット商品コードを指定して **OK** を選択すると、**フォーミュラ デザイナー** ページの **テスト結果** タブには、構成された式の実行結果が表示されます。 その後、結果が受け入れられるかどうかを評価できます。 結果が受け入れられない場合は、式を更新して再度テストできます。

[![テスト結果](./media/ER-FormulaTest-Result.png)](./media/ER-FormulaTest-Result.png)

一部の数式は設計時にテストできません。 たとえば、式は、**テスト結果** タブに表示できないデータ種類の結果を返す場合があります。この場合、式をテストできないことを示すエラー メッセージが表示されます。

[![エラー メッセージ](./media/ER-FormulaTest-Error.png)](./media/ER-FormulaTest-Error.png)

## <a name="additional-resources"></a>追加リソース

- [電子申告の概要](general-electronic-reporting.md)
- [電子報告のフォーミュラ言語](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]