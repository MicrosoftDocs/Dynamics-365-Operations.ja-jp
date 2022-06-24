---
title: 電子申告の高度なフォーミュラ エディター
description: この記事では、高度なフォーミュラ エディターを使用して、電子申告 (ER) モデル マッピングおよび形式コンポーネントで式を構成する方法について説明します。
author: NickSelin
ms.date: 06/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: f54ab248e38d87b0a9fb7a73143f56fa704a3f67
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869102"
---
# <a name="electronic-reporting-advanced-formula-editor"></a>電子申告の高度なフォーミュラ エディター

[!include [banner](../includes/banner.md)]

[電子申告](general-electronic-reporting.md) [フォーミュラ エディター](general-electronic-reporting-formula-designer.md) に加えて、高度な電子申告フォーミュラ エディターを使用して、電子申告 (ER) の式のコンフィギュレーション エクスペリエンスを改善することができます。 高度なエディターは、ブラウザー ベースで、[モナコ エディター](https://microsoft.github.io/monaco-editor) によって強化されています。 この記事では、最も使用頻度の高い高度なエディター機能について説明します。

- [コードのオートフォーマット](#Autoformatting)
- [IntelliSense](#IntelliSense)
- [コードの完了](#CodeCompletion)
- [コードのナビゲーション](#CodeNavigation)
- [コードの構築](#CodeStructuring)
- [検索および置換](#FindAndReplace)
- [データの貼り付け](#DataPasting)
- [構文の色付け](#SyntaxColorization)

## <a name=""></a><a name="ActivateAdvEditor">高度なフォーミュラ エディターの有効化</a>

Microsoft Dynamics 365 Finance のインスタンスで高度なフォーミュラ エディターの使用を開始するには、次の手順を完了します。

1.  **組織管理** \> **電子申告** \> **構成** の順に移動します。
2.  **構成** ページ、アクション ウィンドウ、**構成** タブ、**詳細設定** グループで、**ユーザー パラメーター** を選択します。
3.  **ユーザー パラメーター** ダイアログ ボックスの **実行トレース** セクションで、**詳細フォーミュラ エディターの有効化** パラメーターを **はい** に設定します。

[![ユーザー パラメーター ダイアログ ボックス、高度なフォーミュラ エディターの有効化が強調表示されている。](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)

> [!NOTE]
> このパラメーターはユーザー固有であり、また会社固有であることに注意してください。

Microsoft Dynamics 365 Finance バージョン 10.0.19 以降は、既定で提供される ER フォーミュラ エディターを制御できます。 現在の Finance インスタンスのすべてのユーザーと会社に対して高度なフォーミュラ エディターを有効にするには、次の手順を実行します。

1.  **機能管理** ワークスペースを開きます。
2.  リストで機能の **ER 高度なフォーミュラ エディターをすべてのユーザーに対して既定として設定する** を検索して選択し、**直ちに有効化** を選択します。
3.  **組織管理** >  **電子申告** >  **コンフィギュレーション** に移動します。
4.  **構成** ページ、アクション ウィンドウ、**構成** タブ、**詳細設定** グループで、**ユーザー パラメーター** を選択します。
5.  **ユーザー パラメーター** ダイアログ ボックスで、**高度なフォーミュラ エディターの無効化** のパラメーターを見つけて、**いいえ** に設定されていることを確認します。

[![ユーザー パラメーター ダイアログ ボックス、高度なフォーミュラ エディターの無効化が強調表示されている。](./media/ER-AdvEditor-Activate2.png)](./media/ER-AdvEditor-Activate2.png)

> [!NOTE]
> **高度なフォーミュラ エディターの有効化** と **高度なフォーミュラ エディターの無効化** のパラメーターの値は、各ユーザーごとに分離され、**ER 高度なフォーミュラ エディターをすべてのユーザーに対して既定として設定する** の機能の状態に応じて、**ユーザー パラメーター** ダイアログボックスで表示されます。

## <a name=""></a><a name="Autoformatting">コードのオートフォーマット</a>

複数のコード行で構成される複雑な式を記述する場合、新しく入力された行のインデントは前の行のインデントに基づいて自動的に設定されます。 行を選択し、**タブ** または **Shift+Tab** を押して、インデントを変更することができます。

[![明細行の選択とインデントの変更を示す ER フォーミュラ エディターの gif。](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)

オートフォーマットにより、式全体を適切な形式にしてより簡単にメンテナンスできるようにし、構成されたロジックを理解しやすくできます。

## <a name=""></a><a name="IntelliSense">IntelliSense</a>

エディターは単語補完を提供し、迅速な式の記述および入力ミスを回避するのに役立ちます。 新しいテキストの追加を開始すると、入力した文字を含む ER 関数でサポートされている機能のリストがエディターにより自動的に提供されます。 また、**Ctrl+Space** キー押すことにより、コンフィギュレーションされた式の任意の場所で IntelliSense をトリガーすることもできます。

[![IntelliSense のトリガーを示す ER フォーミュラ エディターの gif。](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)

## <a name=""></a><a name="CodeCompletion">コードの完了</a>

エディターでは、次の方法で自動的にコード補完が行われます。

- 左かっこを入力する時に右かっこを挿入し、かっこ内にカーソルを保持します。
- 最初の引用符が入力された時に 2 番目の引用符を挿入し、カーソルを引用符内に保持します。
- 最初の二重引用符が入力された時に 2 番目の二重引用符を挿入し、カーソルを引用符内に保持します。

[![エディターが自動的にコード補完を行っていることを示す ER フォーミュラ エディターの gif。](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)

入力したかっこをポイントすると、サポートするコンストラクトを示すために、このペアの 2 つ目のかっこが自動的に強調表示されます。

## <a name=""></a><a name="CodeNavigation">コードのナビゲーション</a>

コマンド パレットまたはコンテキスト メニューを使用して **移動** コマンドを入力することにより、式に必要な記号または行を見つけることができます。

たとえば、行 **8** にジャンプするには、次の操作を行います。

- **Ctrl+G** キーを押して、値 **8** を入力し、**Enter** キーを押します。

  または

- **F1** キーを押して **G** を入力し、**行に移動** を選択して、**8** を入力し、**Enter** キーを押します。

[![コマンド パレットを使用して式の一部を検索する方法を示す ER フォーミュラ エディターの gif。](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)

## <a name=""></a><a name="CodeStructuring">コードの構築</a>

[IF](er-functions-logical-if.md) または [CASE](er-functions-logical-case.md) などの一部の関数のコードは自動的に構造化されます。 このコードで折りたたまれている部分の一部または全体を展開したり折りたたんだりすることによって、注意を必要とするコードの部分だけに集中できるように、式の編集可能な部分を減らすことができます。 折りたたみ/展開コマンドを使用できます。

たとえば、すべての地域を折りたたむには、次の操作を行います。

- **Ctrl+K** キーを押します

  または

- **F1** キーを押して、**FO** キーを押し、**すべてを折りたたむ** を選択し、**Enter** キーを押します

すべての地域を展開するには、次の操作を行います。

- **Ctrl+J** キーを押します

  または
  
- **F1** キーを押して、**UN** キーを入力し、**すべてを展開する** を選択し、**Enter** キーを押します

[![コードが展開されていることを示す ER フォーミュラ エディターの gif。](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)

## <a name=""></a><a name="FindAndReplace">検索および置換</a>

特定のテキストの出現を検索するには、式のテキストを選択し、次の操作を行います。

- **Ctrl+F** キーを押し、**F3** キーを押して選択されたテキストが次に出現する場所を検索するか、または **Shift+F3** キーを押して、前に出現する場所を検索します。

  または
  
- **F1** キーを押し、**F** を入力して、選択したテキストを検索するのに必要なオプションを選択します。

特定のテキストの出現を置換するには、式のテキストを選択し、次の操作を行います。

- **Ctrl+H** キーを押します。 代替テキストを入力し、置換オプションを選択して、選択したテキストまたは現在の式でこのテキストが出現するすべての箇所を置換します。

  または
  
- **F1** キーを押し、**R** を入力して、選択したテキストを置換するのに必要なオプションを選択します。 代替テキストを入力し、置換オプションを選択して、選択したテキストまたは現在の式でこのテキストが出現するすべての箇所を置換します。

特定のテキストの出現すべてを変更するには、式のテキストを選択し、次の操作を行います。

- **Ctrl+F2** キーを押して、代替テキストを入力します。

  または
  
- **F1** キーを押し、**C** を入力して、選択したテキストを変更するのに必要なオプションを選択します。 代替テキストを入力します。

[![検索および置換を示す ER フォーミュラ エディターの gif。](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)

## <a name=""></a><a name="DataPasting">データ ソースと関数の貼り付け</a>

**データ ソースの追加** を選択すると、現在、左の **データ ソース** パネルで選択されているデータ ソースが、現在の式に貼り付けられます。 同様に、**関数の追加** を選択すると、現在、右の **関数** パネルで選択されている関数が、現在の式に貼り付けられます。 ER フォーミュラ エディターを使用する場合、選択した関数また選択したデータ ソースは常にコンフィギュレーションされた式の末尾に貼り付けられます。 高度な ER フォーミュラ エディターを使用する場合、選択した関数また選択したデータ ソースはコンフィギュレーションされた式のどこにでもに貼り付けられます。 カーソルを使用して、データを貼り付ける場所を指定する必要があります。

[![データ ソースの追加と機能の貼り付けを示す ER フォーミュラ エディターの gif。](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)

## <a name=""></a><a name="SyntaxColorization">構文の色付け</a>

現在、異なる色を使用して、次の式の部分を強調表示しています。

- テキスト定数のラベル ID を表す 2 つのかっこ内のテキスト。

[![ER フォーミュラ エディター。](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)

## <a name="limitations"></a>制限

現在、エディターは次の Web ブラウザーでサポートされています:

- Chrome
- Edge
- Firefox
- Opera
- Safari

## <a name="additional-resources"></a>追加リソース

- [電子申告 (ER) の概要](general-electronic-reporting.md)
- [電子申告のフォーミュラ デザイナー](general-electronic-reporting-formula-designer.md)
- [モナコ エディター](https://microsoft.github.io/monaco-editor)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
