---
title: ER を使用して生成されるドキュメントへの画像や図形の埋め込み
description: この記事では、電子申告ツールを使用して、画像や図形が埋め込まれたビジネス ドキュメントを生成する方法について説明します。
author: kfend
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.custom: 27621
ms.assetid: ''
ms.search.form: EROperationDesigner, ERParameters
ms.openlocfilehash: 0bb652f245db93424aeadcaadf2ad393945e616b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280991"
---
# <a name="embed-images-and-shapes-in-documents-that-you-generate-by-using-er"></a>ER を使用して生成されるドキュメントへの画像や図形の埋め込み

[!include [banner](../includes/banner.md)]

電子申告 (ER) ツールを使用すると、必要な電子ドキュメントを生成するために実行することができるレポートを設計することができます。 Microsoft Excel また Microsoft Word ドキュメントを使用してレポートのレイアウトを指定することができます。 ER Operations デザイナーを使用すると、レポートのテンプレートとして Excel または Wordドキュメントを添付できます。 添付されたテンプレートの名前付き要素は、ER レポートの書式要素に関連付けられます。 レポートの要素の書式設定は、データ ソースにバインドされます。 これらの要素は、実行時に生成されるドキュメントに入力されるデータを指定します。

この新しい機能は、Microsoft Office 形式の文書を作成する点で既存の ER 機能を超えています。 詳細については、次のタスク ガイドを実行してください。 これらのタスク ガイドは 7.5.4.3 IT サービス/ソリューション コンポーネントの取得/開発 (10677) 業務プロセスの下で見つけることができます。

- ER は、OPENXML 形式でレポートを生成するコンフィギュレーションを設計する
- ER は、Microsoft WORD 形式でレポートを生成するコンフィギュレーションを設計

## <a name="embed-an-image-in-an-excel-document"></a>Excel ドキュメントに画像を埋め込む

### <a name="embed-an-image-in-an-excel-worksheet"></a>Excel ワークシートに画像を埋め込む

最初に、Excel ドキュメントの画像に対するプレースホルダーを追加する必要があります。 Excel ブックを開き、後で追加する画像のプレース ホルダーとして、画像を追加します。 ER ツールを使用して、新しい ER フォーマット構成を追加して、設計中のレポートを組み込みます。 Excel ブックをレポートの形式のテンプレートとして添付し、ブックの内容を ER 形式にインポートします。 形式の定義が自動的に作成されます。 追加したイメージのプレースホルダーは、**セル** 要素として ER 形式の定義に含まれます。

> [!NOTE]
> 形式の定義をインポートせずに手動で指定できます。 変更を保存するとき、形式が検証されます。

次に、ER 形式の **CELL** 要素を、実行時にバイナリ形式で画像のデータを提供する形式のデータ ソースからフィールドにバインドします。 ER データ モデルが形式のデータ ソースとして使用されるとき、このフィールドのデータ型を[コンテナー](er-formula-supported-data-types-composite.md#container)にする必要があります。 現在、[コンテナー](er-formula-supported-data-types-composite.md#container) データ型が存在する ER データ モデル フィールドは、バイナリ形式で画像を返すデータ ソースのいくつかの種類をバインドできます。 ドキュメント管理フレームワークを使用して、データ テーブル内のフィールド、およびデータ テーブルのレコードにアタッチされたファイルにアクセスすることができます。

> [!IMPORTANT]
> - Excel テンプレートを使用して作成するドキュメントのイメージ プレースホルダーを入力する場合、ER 形式に Excel テンプレートの名前付き写真要素を参照する **セル** 要素が含まれている必要があります。 それ以外の場合、レポートの出力にイメージのプレースホルダーが表示されません。 **CELL** 要素のバインディングが実行時にデータを返さない場合、生成されたドキュメントでは、テンプレートからイメージのプレース ホルダーが表示されます。 作成するドキュメントのイメージを非表示にするには、**CELL** 要素を定義し、**Enabling** 式が **FALSE** の値を返すように指定します。
> - Excel テンプレートでは、すべての要素で固有の名前を使用します。 これらの要素には、画像やセルが含まれます。 要素名を複製する場合、生成されるレポートの内容が曖昧になり、紛らわしくなります。

### <a name="embed-images-in-the-header-and-footer-of-an-excel-worksheet"></a>Excel ワークシートのヘッダーとフッターに画像を埋め込む

Excel ブック ドキュメントをテンプレートとして使用して、レポートのレイアウトを指定します。 ブックに複数のワークシートを含め、それぞれがヘッダーとフッターを持つように設計できます。 Excel では、各ワークシートのヘッダーとフッターに最大 3 つの画像がサポートされます。 画像は左揃え、右揃え、または中央揃えにすることができます。

Finance リリース 10.0.21 では、Excel テンプレートのある ER ソリューションによって生成されたヘッダーとフッターの画像を管理できます。

生成されるドキュメントのヘッダーまたはフッターに既定の画像を表示する場合は、ER テンプレートのワークシートのヘッダーまたはフッターに画像を追加できます。 ER 形式でこの画像にアクセスするには、**画像** コンポーネントを形式の[ヘッダー](er-fillable-excel.md#header-component)または[フッター](er-fillable-excel.md#footer-component) コンポーネントに追加する必要があります。 必要に応じて **画像** コンポーネントの配置を構成します。 

また、**画像** コンポーネントを使用すると、テンプレートに既定の画像が含まれていない場合でも、生成されるドキュメントのヘッダーまたはフッターに実行時に画像を挿入することもできます。 生成されるドキュメントのヘッダーまたはフッターに追加するメディア コンテンツを、新しい画像として、または既定の画像の代わりとして指定するには、バイナリ形式の画像を表す [コンテナー](er-formula-supported-data-types-composite.md#container) タイプのデータ ソースに **画像** コンポーネントをバインドする必要があります。

すべての **ヘッダー** または **フッター** コンポーネントには、サポートされている各配置の **画像** コンポーネントを保持できます。**左**、**中央**、および **右**。

**画像** コンポーネントの **高さをスケール** プロパティを使用すると、構成されたバインドを使用して、画像のサイズを制御できます。

- **オリジナル** を選択すると、画像の初期サイズが維持されます。
- 画像を保持するヘッダーまたはフッターの高さに比例して画像の高さをスケールするには、**相対** を選択します。

    - この場合、画像の高さを親ヘッダーまたはフッターの割合として定義する必要があります。
    - スケーリング値が 100% を超えると、画像が対応するワークシートのデータ領域と重なる場合があります。
    - スケーリングの適用時に画像の高さを変更すると、画像の元の縦横比を維持するために幅も変更されます。

- デザイン時に指定された高さと幅の値 (ピクセル単位) に従ってイメージのサイズを変更するには、**絶対** を選択します。

    - 指定した高さが親ヘッダーまたはフッターの高さを超えると、画像が対応するワークシートのデータ領域と重なる場合があります。

また、**画像** コンポーネントの **有効** プロパティを使用して、このコンポーネントを使用して生成されるドキュメントに挿入される画像の可視性を制御できます。

> [!NOTE]
> ER 形式デザイナーを使用して、編集可能な ER 形式に **画像** コンポーネントを追加する必要があります。 [ビジネス ドキュメント管理](er-business-document-management.md)ワークスペースを使用してビジネス ドキュメントのテンプレートを編集するときに、コンポーネントを追加することはできません。

この機能の詳細を知るには、[ER 形式をデザインして、ページのヘッダーまたはフッターに画像が埋め込まれた Excel 形式でレポートを生成する](er-embed-images-header-footer-excel-reports.md)の手順に従います。

## <a name="embed-a-shape-in-an-excel-document"></a>Excel ドキュメントに図形を埋め込む

最初に、Excel ドキュメントの図形に対するプレースホルダーを追加する必要があります。 Excel ブックを開いて、図形のプレース ホルダーとして **図形**、**テキスト ボックス**、または **WordArt** を選択します。 ER ツールを使用して、新しい ER フォーマット構成を追加して、設計中のレポートを組み込みます。 Excel ブックをレポートの形式のテンプレートとして添付し、ブックの内容を ER 形式にインポートします。 形式の定義が自動的に作成されます。 追加したシェイプ プレースホルダは、名前付き Excel シェイプ要素を参照する **CELL** 要素として ER フォーマット定義に含まれます。

> [!NOTE]
> 形式の定義をインポートせずに手動で指定できます。 変更を保存するとき、形式が検証されます。

次に、ER 形式で **CELL** 要素を、実行時にデータを提供する形式のデータ ソースからフィールドにバインドします。 このデータはテキスト文字列に変換できます。 ER 形式の **CELL** 要素がテキストをサポートする Excel テンプレート内の Shape 要素を参照するとき、実行時にこのバインディングによって提供されたテキストは、生成されるドキュメント内のシェイプに表示されます。

> [!IMPORTANT]
> - 図形のプレースホルダを含む Excel テンプレートを使用して新しいドキュメントを生成する場合、ER 形式には、Excel 図形要素を参照する **セル** 要素が含まれている必要があります。 それ以外の場合、レポートの出力にシェイプのプレースホルダーが表示されません。 指定された Excel シェイプ要素を参照する **CELL** 要素のバインディングが実行時にデータを返さない場合、生成されるドキュメントには、Excel テンプレートからシェイプ プレース ホルダのテキストが表示されます。 作成するドキュメントのシェイプを非表示にするには、名前付き Excel シェイプ要素を参照する **CELL** 要素を定義し、**Enabling** 式が **FALSE** の値を返すように指定します。
> - Excel テンプレートでは、すべての要素で固有の名前を使用します。 これらの要素には、図形やセルが含まれます。 要素名を複製する場合、生成されるレポートの内容が曖昧になり、紛らわしくなります。

## <a name="embed-an-image-in-a-word-document"></a>Word ドキュメントに画像を埋め込む
> [!IMPORTANT]
> Excel テンプレートを使用する ER 形式を再利用して、画像が埋め込まれた文書を作成することができます。 ER 形式で、Excel で名前付きの図の要素を参照する **CELL** 要素に名前が指定されており、実行時に画像を返すデータ ソースにバインドされていることを確認します。

最初に、Word ドキュメントのレイアウトをコンフィギュレーションする必要があります。 **写真コンテンツ** コントロールを使用して、埋め込みイメージのプレースホルダーを作成します。 このコントロールにアクセスするには、まず Word Ribbon の **開発者** タブを表示する必要があります。

次に、ER 形式から Excel テンプレートを削除し、Word テンプレート ドキュメントを添付します。 テンプレートへの参照を更新し、変更を保存します。 現在の ER 形式の構造は、**Report** という新しいカスタム XML パーツとして Word テンプレートに保存されます。

次に、ローカル コンピューターに現在の ER 形式の Word テンプレートを保存します。 テンプレートを開いて、**XML マッピング** ウィンドウを開きます。 **レポート** という名前のカスタム XML 部分を検索し、次にバイナリ形式で画像を返すデータ ソースにバインドされている ER レポート内の **セル** 要素をポイントします。 この XML 部分の項目に、選択した **画像コンテンツ** コントロールをマップして、変更を保存します。

[![画像の埋め込み。](./media/embed-images-shapes-01.png)](./media/embed-images-shapes-01.png)

最後に、ER フォーマットから Word テンプレートを削除し、マップされたカスタム XML 部分を含む Word 文書を添付します。 テンプレートへのフォーマット参照を更新し、この ER フォーマットに加えた変更を保存します。

## <a name="more-information"></a>詳細情報
この機能の詳細を理解するには、一連のタスク ガイド **画像を埋め込んだ MS Office 形式の ER Make レポート** を再生します。 これらのタスク ガイドは、Excel ツールと Word ドキュメントで ER ツールを使用して生成された支払小切手に、会社ロゴの画像と権限を与えられたユーザーの署名を埋め込む方法を示しています。

次のテーブルに、**ER 埋め込み画像付きで MS Office 形式のレポートを作成する** タスク ガイドを完了するために必要なファイルを示します。 ファイルをローカル コンピューターにダウンロード し、保存します。

| 説明                                          | ファイル名                   |
|------------------------------------------------------|-----------------------------|
| ER データ モデル構成                          | [cheques.xml 用のモデル](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| ER フォーマット構成                              | [format.xml を印刷する小切手](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| 会社のロゴ画像                                   | [会社の logo.png](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| 署名の画像                                      | [Signature image.png](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| 代替署名画像                          | [Signature image 2.png](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| 小切手印刷用の Microsoft Word テンプレート  | [小切手テンプレート Word.docx](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |
| 小切手印刷用の Microsoft Excel テンプレート | [小切手 template.xlsx](https://download.microsoft.com/download/1/f/6/1f671963-73aa-48d5-ae69-45f21fe7dfb4/Cheque%20template.xlsx)        |

次の図は、Excel テンプレートから生成された支払い小切手のテスト印刷の例です。

[![支払チェック テスト印刷。](./media/embed-images-shapes-02.png)](./media/embed-images-shapes-02.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
