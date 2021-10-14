---
title: Word 形式でレポートを生成するための新しい ER 構成を設計する
description: このトピックでは、ユーザーが新しい電子申告 (ER) 形式を構成して、レポートを Microsoft Word ドキュメントとして生成する方法について説明します。
author: NickSelin
ms.date: 12/17/2020
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
ms.openlocfilehash: a351567e0ed61fac040a6209a221833ab73a242a
ms.sourcegitcommit: e40a9fac5bac9f57a6dcfe73a1f21856eab9b6a9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/02/2021
ms.locfileid: "7595265"
---
# <a name="design-a-new-er-configuration-to-generate-reports-in-word-format"></a>Word 形式でレポートを生成するための新しい ER 構成を設計する

[!include [banner](../includes/banner.md)]

レポートを Microsoft Word ドキュメントとして生成するには、Word デスクトップ アプリケーションなどを使用して、レポートのテンプレートをデザインする必要があります。 次の図は、処理済仕入先支払の詳細を表示するために生成できる管理レポートのサンプル テンプレートを示しています。

![Word デスクトップ アプリケーションの管理レポートのサンプル テンプレート。](./media/er-design-configuration-word-image1.png)

Word ドキュメントを Word 形式のレポートのテンプレートとして使用するには、新しい [電子申告 (ER)](general-electronic-reporting.md) [ソリューション](er-quick-start1-new-solution.md) を構成できます。 このソリューションには、ER [形式](general-electronic-reporting.md#FormatComponentOutbound) コンポーネントを含む ER [構成](general-electronic-reporting.md#Configuration) を含める必要があります。

> [!NOTE]
> Word 形式でレポートを生成するために新しい ER 形式の構成を作成する場合は、**構成の作成** ドロップダウン ダイアログ ボックスで形式タイプとして **Word** を選択するか、**形式タイプ** フィールドを空白のままにする必要があります。

![構成ページで形式構成を作成。](./media/er-design-configuration-word-image2.gif)

ソリューションの ER 形式コンポーネントには **Excel\\File** 形式要素を含む必要があり、その形式要素は、実行時に生成されるレポートのテンプレートとして使用される Word ドキュメントにリンクされている必要があります。 ER 形式コンポーネントを構成するには、ER 形式デザイナーで作成された ER 構成の [ドラフト](general-electronic-reporting.md#component-versioning) バージョンを開く必要があります。 その後、**Excel\\File** 要素を追加し、編集可能な ER 形式に Word テンプレートを添付し、そのテンプレートを追加した **Excel\\File** 要素にリンクします。

> [!NOTE]
> テンプレートを添付する場合、ER パラメーターで事前に [構成](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) されている [ドキュメント タイプ](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types) を使用して、ER 形式のテンプレートを保存する必要があります。

![形式デザイナー ページでテンプレートを添付。](./media/er-design-configuration-word-image3.gif)

**Excel\\File** 要素に **Excel\\Range** と **Excel\\Cell** の入れ子になった要素を追加して、実行時に生成されるレポートに入力されるデータの構造を指定できます。 次に、これらの要素を編集可能な ER 形式のデータ ソースにバインドして、実行時に生成されるレポートに入力される実際のデータを指定する必要があります。

![形式デザイナー ページで入れ子になった要素を追加。](./media/er-design-configuration-word-image4.gif)

ER 形式への変更をデザイン時に保存すると、階層形式の構造は、添付された Word テンプレートに、**レポート** という名前の [カスタム XML パーツ](/visualstudio/vsto/custom-xml-parts-overview) として保存されます。 変更したテンプレートにアクセスし、Finance からダウンロードして、ローカルに保存して、Word デスクトップ アプリケーションで開く必要があります。 次の図は、**レポート** カスタム XML パーツを含む管理レポートのローカルに保存されているサンプル テンプレートを示します。

![Word デスクトップ アプリケーションでサンプル レポート テンプレートをプレビュー。](./media/er-design-configuration-word-image5.gif)

**Excel\\Range** と **Excel\\Cell** 形式要素のバインドが実行時に実行される場合、すべてのバインドによって提供されるデータは、**レポート** のカスタム XML パーツの個別のフィールドとして、生成された Word ドキュメントに取り込まれます。 生成されるドキュメントでカスタム XML パーツのフィールドから値を入力するには、実行時に入力されるデータのプレースホルダーとして機能させるために、適切な Word [コンテンツ コントロール](/office/client-developer/word/content-controls-in-word) を Word テンプレートに追加する必要があります。 コンテンツ コントロールの入力方法を指定するには、すべてのコンテンツ コントロールを **レポート** カスタム XML パーツの適切なフィールドにマップします。

![Word デスクトップ アプリケーションでコンテンツ コントロールを追加およびマッピング。](./media/er-design-configuration-word-image6.gif)

次に、編集可能な ER 形式の元の Word テンプレートを、**レポート** カスタム XML パーツのフィールドにマップされた Word コンテンツ コントロールを含む変更されたテンプレートに置き換える必要があります。

![形式デザイナー ページでテンプレートを置換。](./media/er-design-configuration-word-image7.gif)

構成された ER 形式を実行すると、添付された Word テンプレートを使用して新しいレポートが生成されます。 実際のデータは、**レポート** という名前のカスタム XML パーツとして Word レポートに格納されます。 生成されたレポートを開くと、Word コンテンツ コントロールに **レポート** カスタム XML パーツからデータが入力されます。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

**質問:** 会社の住所を含む Word ドキュメントを印刷するように ER 形式を構成しました。 この ER 形式の Word テンプレートで、会社の住所を表示するリッチ テキスト コンテンツ コントロールを挿入しました。 Finance では、会社の住所を複数行テキストとして入力し、入力した各行にキャリッジ・リターンを追加するために **Enter** を選択しました。 したがって、生成されたドキュメントでは、会社住所が複数行テキストとして表示されることを期待します。 しかし、住所は、キャリッジ リターンの代わりに特殊記号を含む 1 行のテキストとして表示されます。 設定の何が悪いのですか?

**回答:** リッチ テキスト コンテンツ コントロールを使用する代わりに、プレーン テキスト コンテンツ コントロールを使用し、コントロールのプロパティで **キャリッジ リターンを許可 (複数の段落)** チェック ボックスを選択する必要があります。

## <a name="additional-resources"></a>追加リソース

- [Excel テンプレートと ER 構成を再利用して Word 形式でレポートを生成](./tasks/er-design-configuration-word-2016-11.md)
- [ER を使用して生成されるドキュメントへの画像や図形の埋め込み](electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]