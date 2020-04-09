---
title: 電子申告の高度なフォーミュラ エディター
description: このトピックでは、高度なフォーミュラ エディターを使用して、電子申告 (ER) モデル マッピングおよび形式コンポーネントで式をコンフィギュレーションする方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: df402bc20753d2ba14295592f4b40e20f9fdc7bf
ms.sourcegitcommit: b92c3e1b3403d0455fc4e0bf9132d6bc0d7aba5e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138901"
---
# <a name="electronic-reporting-advanced-formula-editor"></a><span data-ttu-id="1d7e2-103">電子申告の高度なフォーミュラ エディター</span><span class="sxs-lookup"><span data-stu-id="1d7e2-103">Electronic reporting advanced formula editor</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1d7e2-104">[電子申告](general-electronic-reporting.md) [フォーミュラ エディター](general-electronic-reporting-formula-designer.md) に加えて、高度な電子申告フォーミュラ エディターを使用して、電子申告 (ER) の式のコンフィギュレーション エクスペリエンスを改善することができます。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-104">In addition to the [Electronic reporting](general-electronic-reporting.md) [formula editor](general-electronic-reporting-formula-designer.md), you can use the advanced Electronic reporting formula editor to improve the experience of configuring Electronic reporting (ER) expressions.</span></span> <span data-ttu-id="1d7e2-105">高度なエディターは、ブラウザー ベースで、[モナコ エディター](https://microsoft.github.io/monaco-editor) によって強化されています。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-105">The advanced editor is browser-based and powered by the [Monaco editor](https://microsoft.github.io/monaco-editor).</span></span> <span data-ttu-id="1d7e2-106">このトピックでは、最も使用頻度の高い高度なエディター機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-106">The most commonly used advanced editor features are described in this topic:</span></span>

- [<span data-ttu-id="1d7e2-107">コードのオートフォーマット</span><span class="sxs-lookup"><span data-stu-id="1d7e2-107">Code autoformatting</span></span>](#Autoformatting)
- [<span data-ttu-id="1d7e2-108">IntelliSense</span><span class="sxs-lookup"><span data-stu-id="1d7e2-108">IntelliSense</span></span>](#IntelliSense)
- [<span data-ttu-id="1d7e2-109">コードの完了</span><span class="sxs-lookup"><span data-stu-id="1d7e2-109">Code completion</span></span>](#CodeCompletion)
- [<span data-ttu-id="1d7e2-110">コードのナビゲーション</span><span class="sxs-lookup"><span data-stu-id="1d7e2-110">Code navigation</span></span>](#CodeNavigation)
- [<span data-ttu-id="1d7e2-111">コードの構築</span><span class="sxs-lookup"><span data-stu-id="1d7e2-111">Code structuring</span></span>](#CodeStructuring)
- [<span data-ttu-id="1d7e2-112">検索および置換</span><span class="sxs-lookup"><span data-stu-id="1d7e2-112">Find and replace</span></span>](#FindAndReplace)
- [<span data-ttu-id="1d7e2-113">データの貼り付け</span><span class="sxs-lookup"><span data-stu-id="1d7e2-113">Data pasting</span></span>](#DataPasting)
- [<span data-ttu-id="1d7e2-114">構文の色付け</span><span class="sxs-lookup"><span data-stu-id="1d7e2-114">Syntax colorization</span></span>](#SyntaxColorization)

## <a name=""></a><span data-ttu-id="1d7e2-115"><a name="ActivateAdvEditor">高度なフォーミュラ エディターの有効化</a></span><span class="sxs-lookup"><span data-stu-id="1d7e2-115"><a name="ActivateAdvEditor">Activate the advanced formula editor</a></span></span>

<span data-ttu-id="1d7e2-116">Microsoft Dynamics 365 Finance のインスタンスで高度なフォーミュラ エディターの使用を開始するには、次の手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-116">Complete the following steps to start using the advanced formula editor in your instance of Microsoft Dynamics 365 Finance.</span></span>

1.  <span data-ttu-id="1d7e2-117"> **組織管理** \> **電子申告** \> **コンフィギュレーション**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-117">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2.  <span data-ttu-id="1d7e2-118"> **構成** ページ、アクション ウィンドウ、 **構成** タブ、 **詳細設定** グループで、 **ユーザー パラメーター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-118">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3.  <span data-ttu-id="1d7e2-119"> **ユーザー パラメーター** ダイアログ ボックス、 **実行の追跡** セクションで、**高度なフォーミュラ エディターの有効化**パラメーターを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-119">In the **User parameters** dialog box, in the **Execution tracing** section, set the **Enable advanced formula editor** parameter to **Yes**.</span></span>

<span data-ttu-id="1d7e2-120">[![ER コンフィギュレーション ページ](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span><span class="sxs-lookup"><span data-stu-id="1d7e2-120">[![ER configurations page](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span></span>

> [!NOTE]
> <span data-ttu-id="1d7e2-121">このパラメーターはユーザー固有であり、また会社固有であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-121">Be aware that this parameter is user specific and company specific.</span></span>

## <a name=""></a><span data-ttu-id="1d7e2-122"><a name="Autoformatting">コードのオートフォーマット</a></span><span class="sxs-lookup"><span data-stu-id="1d7e2-122"><a name="Autoformatting">Code autoformatting</a></span></span>

<span data-ttu-id="1d7e2-123">複数のコード行で構成される複雑な式を記述する場合、新しく入力された行のインデントは前の行のインデントに基づいて自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-123">When you write a complex expression that consists of multiple rows of code, the indentation of a new entered line will be automatic based on the indentation of the previous row.</span></span> <span data-ttu-id="1d7e2-124">行を選択し、**タブ**または**Shift+Tab**を押して、インデントを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-124">You can select lines and change their indentation by typing **Tab** or **Shift+Tab**.</span></span>

<span data-ttu-id="1d7e2-125">[![ER フォーミュラ エディター](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span><span class="sxs-lookup"><span data-stu-id="1d7e2-125">[![ER formula editor](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span></span>

<span data-ttu-id="1d7e2-126">オートフォーマットにより、式全体を適切な形式にしてより簡単にメンテナンスできるようにし、構成されたロジックを理解しやすくできます。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-126">Autoformatting allows you to keep the entire expression well formatted to make further maintenance easier and to simplify understanding of the configured logic.</span></span>

## <a name=""></a><span data-ttu-id="1d7e2-127"><a name="IntelliSense">IntelliSense</a></span><span class="sxs-lookup"><span data-stu-id="1d7e2-127"><a name="IntelliSense">IntelliSense</a></span></span>

<span data-ttu-id="1d7e2-128">エディターは単語補完を提供し、迅速な式の記述および入力ミスを回避するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-128">The editor provides word completion to help you write expression faster and avoid typos.</span></span> <span data-ttu-id="1d7e2-129">新しいテキストの追加を開始すると、入力した文字を含む ER 関数でサポートされている機能のリストがエディターにより自動的に提供されます。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-129">When you start adding new text, the editor automatically offers a list of functions supported in ER functions that contain the characters you have entered.</span></span> <span data-ttu-id="1d7e2-130">また、**Ctrl+Space** キー押すことにより、コンフィギュレーションされた式の任意の場所で IntelliSense をトリガーすることもできます。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-130">You can also trigger IntelliSense in any place of a configured expression by typing **Ctrl+Space**.</span></span>

<span data-ttu-id="1d7e2-131">[![ER フォーミュラ エディター](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span><span class="sxs-lookup"><span data-stu-id="1d7e2-131">[![ER formula editor](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span></span>

## <a name=""></a><span data-ttu-id="1d7e2-132"><a name="CodeCompletion">コードの完了</a></span><span class="sxs-lookup"><span data-stu-id="1d7e2-132"><a name="CodeCompletion">Code completion</a></span></span>

<span data-ttu-id="1d7e2-133">エディターでは、次の方法で自動的にコード補完が行われます。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-133">The editor automatically provides code completion by:</span></span>

- <span data-ttu-id="1d7e2-134">左かっこを入力する時に右かっこを挿入し、かっこ内にカーソルを保持します。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-134">Inserting a closing bracket when an opening  bracket is entered, keeping the cursor inside the brackets.</span></span>
- <span data-ttu-id="1d7e2-135">最初の引用符が入力された時に 2 番目の引用符を挿入し、カーソルを引用符内に保持します。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-135">Inserting the second quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>
- <span data-ttu-id="1d7e2-136">最初の二重引用符が入力された時に 2 番目の二重引用符を挿入し、カーソルを引用符内に保持します。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-136">Inserting the second double quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>

<span data-ttu-id="1d7e2-137">[![ER フォーミュラ エディター](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span><span class="sxs-lookup"><span data-stu-id="1d7e2-137">[![ER formula editor](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span></span>

<span data-ttu-id="1d7e2-138">入力したかっこをポイントすると、サポートするコンストラクトを示すために、このペアの 2 つ目のかっこが自動的に強調表示されます。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-138">When you point to the typed bracket, the second bracket of this pair is automatically highlighted to show the construct that they support.</span></span>

## <a name=""></a><span data-ttu-id="1d7e2-139"><a name="CodeNavigation">コードのナビゲーション</a></span><span class="sxs-lookup"><span data-stu-id="1d7e2-139"><a name="CodeNavigation">Code navigation</a></span></span>

<span data-ttu-id="1d7e2-140">コマンド パレットまたはコンテキスト メニューを使用して**移動**コマンドを入力することにより、式に必要な記号または行を見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-140">You can locate required symbols or lines in your expression by typing the **Go to** command using the command palette or the context menu.</span></span>

<span data-ttu-id="1d7e2-141">たとえば、行 **8** にジャンプするには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-141">For example, to jump to line **8**, do the following:</span></span>

- <span data-ttu-id="1d7e2-142">**Ctrl+G** キーを押して、値 **8** を入力し、**Enter** キーを押します。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-142">Press **Ctrl+G**, enter the value **8**, and then press **Enter**.</span></span>

  <span data-ttu-id="1d7e2-143">または</span><span class="sxs-lookup"><span data-stu-id="1d7e2-143">-or-</span></span>

- <span data-ttu-id="1d7e2-144">**F1** キーを押して **G** を入力し、**行に移動**を選択して、**8** を入力し、**Enter** キーを押します。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-144">Press **F1**, type **G**, select **Go to line**, enter the value **8**, and the press **Enter**.</span></span>

<span data-ttu-id="1d7e2-145">[![ER フォーミュラ エディター](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span><span class="sxs-lookup"><span data-stu-id="1d7e2-145">[![ER formula editor](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span></span>

## <a name=""></a><span data-ttu-id="1d7e2-146"><a name="CodeStructuring">コードの構築</a></span><span class="sxs-lookup"><span data-stu-id="1d7e2-146"><a name="CodeStructuring">Code structuring</a></span></span>

<span data-ttu-id="1d7e2-147">[IF](er-functions-logical-if.md) または [CASE](er-functions-logical-case.md) などの一部の関数のコードは自動的に構造化されます。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-147">The code for some functions, such as [IF](er-functions-logical-if.md) or [CASE](er-functions-logical-case.md), is automatically structured.</span></span> <span data-ttu-id="1d7e2-148">このコードで折りたたまれている部分の一部または全体を展開したり折りたたんだりすることによって、注意を必要とするコードの部分だけに集中できるように、式の編集可能な部分を減らすことができます。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-148">You can expand and collapse any or all of the folding regions of this code to reduce the editable part of an expression in order to focus on only  thepiece of code that requires your attention.</span></span> <span data-ttu-id="1d7e2-149">折りたたみ/展開コマンドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-149">The toggle fold/unfold commands can be used for that.</span></span>

<span data-ttu-id="1d7e2-150">たとえば、すべての地域を折りたたむには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-150">For example, to fold all regions, do the following:</span></span>

- <span data-ttu-id="1d7e2-151">**Ctrl+K** キーを押します</span><span class="sxs-lookup"><span data-stu-id="1d7e2-151">Press **Ctrl+K**</span></span>

  <span data-ttu-id="1d7e2-152">または</span><span class="sxs-lookup"><span data-stu-id="1d7e2-152">-or-</span></span>

- <span data-ttu-id="1d7e2-153">**F1** キーを押して、**FO** キーを押し、**すべてを折りたたむ**を選択し、**Enter** キーを押します</span><span class="sxs-lookup"><span data-stu-id="1d7e2-153">Press **F1**, press **FO**, select **Fold all**, and then press **Enter**</span></span>

<span data-ttu-id="1d7e2-154">すべての地域を展開するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-154">To unfold all regions, do the following:</span></span>

- <span data-ttu-id="1d7e2-155">**Ctrl+J** キーを押します</span><span class="sxs-lookup"><span data-stu-id="1d7e2-155">Press **Ctrl+J**</span></span>

  <span data-ttu-id="1d7e2-156">または</span><span class="sxs-lookup"><span data-stu-id="1d7e2-156">-or-</span></span>
  
- <span data-ttu-id="1d7e2-157">**F1** キーを押して、**UN** キーを入力し、**すべてを展開する**を選択し、**Enter** キーを押します</span><span class="sxs-lookup"><span data-stu-id="1d7e2-157">Press **F1**, type **UN**, select **Unfold all**, and then press **Enter**</span></span>

<span data-ttu-id="1d7e2-158">[![ER フォーミュラ エディター](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span><span class="sxs-lookup"><span data-stu-id="1d7e2-158">[![ER formula editor](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span></span>

## <a name=""></a><span data-ttu-id="1d7e2-159"><a name="FindAndReplace">検索および置換</a></span><span class="sxs-lookup"><span data-stu-id="1d7e2-159"><a name="FindAndReplace">Find and replace</a></span></span>

<span data-ttu-id="1d7e2-160">特定のテキストの出現を検索するには、式のテキストを選択し、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-160">To find occurrences of certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="1d7e2-161">**Ctrl+F** キーを押し、**F3** キーを押して選択されたテキストが次に出現する場所を検索するか、または **Shift+F3** キーを押して、前に出現する場所を検索します。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-161">Press **Ctrl+F** and then press **F3** to find the next occurrence of the selected text, or press **Shift+F3** to find the previous occurrence.</span></span>

  <span data-ttu-id="1d7e2-162">または</span><span class="sxs-lookup"><span data-stu-id="1d7e2-162">-or-</span></span>
  
- <span data-ttu-id="1d7e2-163">**F1** キーを押し、**F** を入力して、選択したテキストを検索するのに必要なオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-163">Press **F1**, type **F**, and then select the required option to find the selected text.</span></span>

<span data-ttu-id="1d7e2-164">特定のテキストの出現を置換するには、式のテキストを選択し、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-164">To replace occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="1d7e2-165">**Ctrl+H** キーを押します。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-165">Press **Ctrl+H**.</span></span> <span data-ttu-id="1d7e2-166">代替テキストを入力し、置換オプションを選択して、選択したテキストまたは現在の式でこのテキストが出現するすべての箇所を置換します。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-166">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

  <span data-ttu-id="1d7e2-167">または</span><span class="sxs-lookup"><span data-stu-id="1d7e2-167">-or-</span></span>
  
- <span data-ttu-id="1d7e2-168">**F1** キーを押し、**R** を入力して、選択したテキストを置換するのに必要なオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-168">Press **F1**, type **R**, and then select the required option to replace the selected text.</span></span> <span data-ttu-id="1d7e2-169">代替テキストを入力し、置換オプションを選択して、選択したテキストまたは現在の式でこのテキストが出現するすべての箇所を置換します。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-169">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

<span data-ttu-id="1d7e2-170">特定のテキストの出現すべてを変更するには、式のテキストを選択し、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-170">To change all occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="1d7e2-171">**Ctrl+F2** キーを押して、代替テキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-171">Press **Ctrl+F2** and then enter the alternative text.</span></span>

  <span data-ttu-id="1d7e2-172">または</span><span class="sxs-lookup"><span data-stu-id="1d7e2-172">-or-</span></span>
  
- <span data-ttu-id="1d7e2-173">**F1** キーを押し、**C** を入力して、選択したテキストを変更するのに必要なオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-173">Press **F1**, type **C**, and then select the required option to change the selected text.</span></span> <span data-ttu-id="1d7e2-174">代替テキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-174">Enter the alternative text.</span></span>

<span data-ttu-id="1d7e2-175">[![ER フォーミュラ エディター](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span><span class="sxs-lookup"><span data-stu-id="1d7e2-175">[![ER formula editor](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span></span>

## <a name=""></a><span data-ttu-id="1d7e2-176"><a name="DataPasting">データ ソースと関数の貼り付け</a></span><span class="sxs-lookup"><span data-stu-id="1d7e2-176"><a name="DataPasting">Data sources and functions pasting</a></span></span>

<span data-ttu-id="1d7e2-177">**データ ソースの追加**を選択すると、現在、左の**データ ソース** パネルで選択されているデータ ソースが、現在の式に貼り付けられます。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-177">You can select **Add data source**, which pastes to the current expression a data source that is currently selected on the **Data source** left panel.</span></span> <span data-ttu-id="1d7e2-178">同様に、**関数の追加**を選択すると、現在、右の**関数**パネルで選択されている関数が、現在の式に貼り付けられます。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-178">Simlilarly, you can select **Add function**, which pastes to the current expression a function that is currently selected on the **Functions** right panel.</span></span> <span data-ttu-id="1d7e2-179">ER フォーミュラ エディターを使用する場合、選択した関数また選択したデータ ソースは常にコンフィギュレーションされた式の末尾に貼り付けられます。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-179">If you use the ER formula editor, a selected function or a selected data source will always be pasted to the end of the configured expression.</span></span> <span data-ttu-id="1d7e2-180">高度な ER フォーミュラ エディターを使用する場合、選択した関数また選択したデータ ソースはコンフィギュレーションされた式のどこにでもに貼り付けられます。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-180">When you use the advanced ER formula editor, a selected function or a selected data source can be pasted to any part of the configured expression.</span></span> <span data-ttu-id="1d7e2-181">カーソルを使用して、データを貼り付ける場所を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-181">You will need to use the cursor to specify where you want to paste the data.</span></span>

<span data-ttu-id="1d7e2-182">[![ER フォーミュラ エディター](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span><span class="sxs-lookup"><span data-stu-id="1d7e2-182">[![ER formula editor](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span></span>

## <a name=""></a><span data-ttu-id="1d7e2-183"><a name="SyntaxColorization">構文の色付け</a></span><span class="sxs-lookup"><span data-stu-id="1d7e2-183"><a name="SyntaxColorization">Syntax colorization</a></span></span>

<span data-ttu-id="1d7e2-184">現在、異なる色を使用して、次の式の部分を強調表示しています。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-184">Currently, different colors are used to highlight the following parts of expressions:</span></span>

- <span data-ttu-id="1d7e2-185">テキスト定数のラベル ID を表す 2 つのかっこ内のテキスト。</span><span class="sxs-lookup"><span data-stu-id="1d7e2-185">The text in double brackets that can represent a label ID of a text constant.</span></span>

<span data-ttu-id="1d7e2-186">[![ER フォーミュラ エディター](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span><span class="sxs-lookup"><span data-stu-id="1d7e2-186">[![ER formula editor](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1d7e2-187">追加リソース</span><span class="sxs-lookup"><span data-stu-id="1d7e2-187">Additional resources</span></span>

- [<span data-ttu-id="1d7e2-188">電子申告 (ER) の概要</span><span class="sxs-lookup"><span data-stu-id="1d7e2-188">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="1d7e2-189">電子申告のフォーミュラ デザイナー</span><span class="sxs-lookup"><span data-stu-id="1d7e2-189">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
- [<span data-ttu-id="1d7e2-190">モナコ エディター</span><span class="sxs-lookup"><span data-stu-id="1d7e2-190">Monaco editor</span></span>](https://microsoft.github.io/monaco-editor)
