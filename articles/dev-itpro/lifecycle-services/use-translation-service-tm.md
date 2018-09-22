---
title: "翻訳メモリ ファイル"
description: "このトピックでは、翻訳メモリ ファイルを作成、編集、および使用して、Microsoft Dynamics 365 翻訳サービス (DTS) が高品質の翻訳出力ファイルを提供するのをいつ、どこで行うことができるかについて説明します。"
author: kfend
manager: AnnBe
ms.date: 03/29/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 6154
ms.assetid: 
ms.search.region: Global
ms.author: ejchoGIT
ms.search.validFrom: 2018-03-27
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: ce9c24a0a89dd4e6a0f3f2c7789b4f553d88d412
ms.openlocfilehash: 115832c4b6bf3e05e3bc621c0254a167e549e1af
ms.contentlocale: ja-jp
ms.lasthandoff: 08/13/2018

---

# <a name="translation-memory-files"></a><span data-ttu-id="67f82-103">翻訳メモリ ファイル</span><span class="sxs-lookup"><span data-stu-id="67f82-103">Translation memory files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="67f82-104">Microsoft Dynamics 365 翻訳サービス (DTS) は、2 か国語 XML ローカライズ交換ファイル形式 (XLIFF) ファイルを使用して、ソース言語とターゲット言語のペアを格納します。</span><span class="sxs-lookup"><span data-stu-id="67f82-104">Microsoft Dynamics 365 Translation Service (DTS) uses a bilingual XML Localization Interchange File Format (XLIFF) file to store pairs of source languages and target languages.</span></span> <span data-ttu-id="67f82-105">XLIFF は XML に基づいているため、任意のテキスト エディターで XLIFF ファイルを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="67f82-105">Because XLIFF is based on XML, you can open XLIFF files in any text editor.</span></span> <span data-ttu-id="67f82-106">ただし、この形式を使用するよう設計されている XLIFF エディターを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="67f82-106">However, we recommend that you use XLIFF editors that are specifically designed to work with this format.</span></span> <span data-ttu-id="67f82-107">たとえば、[多言語アプリ ツールキット (MAT)](https://developer.microsoft.com/en-us/windows/develop/multilingual-app-toolkit) で利用できる無料の Microsoft 多言語エディターを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="67f82-107">For example, you can use the free Microsoft Multilingual Editor that is available in the [Multilingual App Toolkit (MAT)](https://developer.microsoft.com/en-us/windows/develop/multilingual-app-toolkit).</span></span>

<span data-ttu-id="67f82-108">DTS では、2 つの方法で XLIFF 翻訳メモリ (TM) を入手できます。</span><span class="sxs-lookup"><span data-stu-id="67f82-108">In DTS, you can obtain an XLIFF translation memory (TM) in two ways:</span></span>

+ <span data-ttu-id="67f82-109">**整列ツールの実行** – 前回翻訳したファイルがあり、対応するソース ファイルもある場合、整列ツールを使用して XLIFF TM を作成できます。</span><span class="sxs-lookup"><span data-stu-id="67f82-109">**Run the Align tool** – When you have files that were previously translated, and you also have corresponding source files, you can use the Align tool to create an XLIFF TM.</span></span> <span data-ttu-id="67f82-110">詳細については、このトピックで後述の [翻訳メモリを作成する](#creating-a-translation-memory) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="67f82-110">For more details, see the [Creating a translation memory](#creating-a-translation-memory) section later in this topic.</span></span>
+ <span data-ttu-id="67f82-111">**翻訳要求を完了** - DTS 翻訳要求が完了すると、要求出力の一部として XLIFF TM が提供されます。</span><span class="sxs-lookup"><span data-stu-id="67f82-111">**Complete a translation request** – When a DTS translation request is completed, it provides the XLIFF TMs as part of the request output.</span></span> <span data-ttu-id="67f82-112">更新済みソース ファイルを含む新しいトランザクション要求を次に送信するときに、ファイルを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="67f82-112">You can then use the files the next time that you submit a new translation request that includes the updated source files.</span></span>

<span data-ttu-id="67f82-113">XLIFF ファイルにはソース ファイルから抽出された一連の翻訳単位 (TU) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="67f82-113">XLIFF files contain a series of translation units (TUs) that are extracted from the source files.</span></span> <span data-ttu-id="67f82-114">次の図は、TU の例を示します。</span><span class="sxs-lookup"><span data-stu-id="67f82-114">The following illustration shows an example of a TU.</span></span>

<span data-ttu-id="67f82-115">![XLIFF 翻訳単位](./media/dts-xlf.png "XLIFF 翻訳単位")</span><span class="sxs-lookup"><span data-stu-id="67f82-115">![XLIFF translation unit](./media/dts-xlf.png "XLIFF translation unit")</span></span>

<span data-ttu-id="67f82-116">次の図は、多言語エディターで同じTU (青色で強調表示) を示しています。</span><span class="sxs-lookup"><span data-stu-id="67f82-116">The following illustration shows the same TU (highlighted in blue) in the Multilingual Editor.</span></span>

<span data-ttu-id="67f82-117">![多言語エディタでの XLIFF 翻訳単位](./media/dts-editor3.png "多言語エディタでの XLIFF 翻訳単位")</span><span class="sxs-lookup"><span data-stu-id="67f82-117">![XLIFF translation unit in the Multilingual Editor](./media/dts-editor3.png "XLIFF translation unit in the Multilingual Editor")</span></span>

## <a name="state"></a><span data-ttu-id="67f82-118">行政単位 (区画)</span><span class="sxs-lookup"><span data-stu-id="67f82-118">State</span></span>
<span data-ttu-id="67f82-119">XLIFF ファイルの各移動は、状態値に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="67f82-119">Each translation in the XLIFF file is associated with a state value.</span></span> <span data-ttu-id="67f82-120">DTS が各翻訳に割り当てる状態値は、文字列の変換方法によって異なります。</span><span class="sxs-lookup"><span data-stu-id="67f82-120">The state value that DTS assigns to each translation depends on the way that the string is translated.</span></span> <span data-ttu-id="67f82-121">アライン ツールを使用して XLIFF TM が作成されると、アラインされた TU は以前の製品バージョンなどの既知の適正な翻訳から生成されるので、すべての翻訳に **変換済み** のマークが付きます。</span><span class="sxs-lookup"><span data-stu-id="67f82-121">When an XLIFF TM is created by using the Align tool, all translations are marked as **Translated**, because the aligned TUs are produced from known good translations, such as a previous product version.</span></span>

<span data-ttu-id="67f82-122">ただし、翻訳要求を通して XLIFF ファイルが生成されると、2 種類の状態値が使用できます。</span><span class="sxs-lookup"><span data-stu-id="67f82-122">However, when the XLIFF files are generated through a translation request, two types of state values can be used:</span></span>

+ <span data-ttu-id="67f82-123">**確認が必要** – 文字列は機械翻訳されています。</span><span class="sxs-lookup"><span data-stu-id="67f82-123">**Needs Review** – The string has been machine-translated.</span></span>
+ <span data-ttu-id="67f82-124">**翻訳済み**、**最終**、または**サインオフ済** – 文字列が再利用されました。</span><span class="sxs-lookup"><span data-stu-id="67f82-124">**Translated**, **Final**, or **Signed off** – The string has been recycled.</span></span> <span data-ttu-id="67f82-125">状態値は XLIFF TM から継承されます。</span><span class="sxs-lookup"><span data-stu-id="67f82-125">The state value is inherited from the XLIFF TM.</span></span>

<span data-ttu-id="67f82-126">転記の編集プロセス中に、**レビューて必要**とマークされている文字列を直ちに識別できます。</span><span class="sxs-lookup"><span data-stu-id="67f82-126">During the post-editing process, you can immediately identify the strings that are marked as **Needs Review**.</span></span> <span data-ttu-id="67f82-127">これらの文字列を確認した後、それらを**翻訳済み**、**最終**、または**サインオフ**とマークして再利用することができます。</span><span class="sxs-lookup"><span data-stu-id="67f82-127">After you've finished reviewing those strings, you should mark them as **Translated**, **Final**, or **Signed off**, so that they can be used for recycling.</span></span> <span data-ttu-id="67f82-128">**要レビュー**としてマークされている翻訳はリサイクルには含まれません。</span><span class="sxs-lookup"><span data-stu-id="67f82-128">Translations that are marked as **Needs Review** aren't included for recycling.</span></span>

<span data-ttu-id="67f82-129">再利用される文字列について継承される状態値は、同じ文字列 (つまり、同じ ID を持つ文字列) を再度確認する必要がないため役立ちます。</span><span class="sxs-lookup"><span data-stu-id="67f82-129">Inherited state values for recycled strings are helpful, because you won't have to review the same string (that is, a string that has the same ID) again.</span></span>

## <a name="creating-a-translation-memory"></a><span data-ttu-id="67f82-130">翻訳メモリの作成</span><span class="sxs-lookup"><span data-stu-id="67f82-130">Creating a translation memory</span></span>
<span data-ttu-id="67f82-131">以前に翻訳されたファイルを使用する場合は、XLIFF を使用する翻訳メモリを作成し、ソース ファイルの新しいバージョンの翻訳されたファイルを再利用できます。</span><span class="sxs-lookup"><span data-stu-id="67f82-131">If you have files that were previously translated, you can recycle the translated files for a newer version of the source files by creating a TM that uses XLIFF.</span></span>

1. <span data-ttu-id="67f82-132">DTS ダッシュ ボードで、**整列**ボタンを選択し整列ツールを開始します。</span><span class="sxs-lookup"><span data-stu-id="67f82-132">On the DTS dashboard, select the **Align** button to start the Align tool.</span></span>

    <span data-ttu-id="67f82-133">![配置ボタン](./media/dts-align-icon.png "配置ボタン")</span><span class="sxs-lookup"><span data-stu-id="67f82-133">![Align button](./media/dts-align-icon.png "Align button")</span></span>

    > [!NOTE]
    > - <span data-ttu-id="67f82-134">アライン ツールは現在、ユーザー インターフェイス (UI) ファイルのみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="67f82-134">The Align tool currently supports only user interface (UI) files.</span></span>
    > - <span data-ttu-id="67f82-135">アライン ツールを開始するには、ブラウザーでポップアップ ウィンドウを明示的に許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="67f82-135">To start the Align tool, you might have to explicitly allow pop-up windows in your browser.</span></span>

2. <span data-ttu-id="67f82-136">**配置**ページで、ソース言語、ターゲット言語、および調整するファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="67f82-136">On the **Align** page, select the source language, the target language, and the files to align.</span></span>
3. <span data-ttu-id="67f82-137">**配置** を選択し、配置を完了します。</span><span class="sxs-lookup"><span data-stu-id="67f82-137">Select **Align** to complete the alignment.</span></span> <span data-ttu-id="67f82-138">配置が完了すると、メッセージに結果が集計されます。</span><span class="sxs-lookup"><span data-stu-id="67f82-138">When the alignment is completed, a message summarizes the results.</span></span>

<span data-ttu-id="67f82-139">![配置の完了](./media/dts-align1.png "配置の完了")</span><span class="sxs-lookup"><span data-stu-id="67f82-139">![Alignment completed](./media/dts-align1.png "Alignment completed")</span></span>

<span data-ttu-id="67f82-140">最良の XLIFF TM を作成するには、次の条件が満たされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="67f82-140">To create the best XLIFF TM, make sure that the following conditions are met:</span></span>

- <span data-ttu-id="67f82-141">ソース ファイルとターゲット ファイルのリソース数が同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="67f82-141">Both the source file and the target file have the same number of resources.</span></span>
- <span data-ttu-id="67f82-142">リソースはソース ファイルとターゲット ファイルの両方で同じ順序です。</span><span class="sxs-lookup"><span data-stu-id="67f82-142">The resources are in the same order in both the source file and the target file.</span></span>
- <span data-ttu-id="67f82-143">空の文字列はありません。</span><span class="sxs-lookup"><span data-stu-id="67f82-143">There are no empty strings.</span></span> <span data-ttu-id="67f82-144">次の図は、ソースとターゲットの空の文字列の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="67f82-144">The following illustration shows examples of empty strings in the source and the target.</span></span>

    <span data-ttu-id="67f82-145">![空の文字列](./media/dts-align3.png "空の文字列")</span><span class="sxs-lookup"><span data-stu-id="67f82-145">![Empty strings](./media/dts-align3.png "Empty strings")</span></span>

    <span data-ttu-id="67f82-146">空の文字列は、XLIFF TM によって継承されます。</span><span class="sxs-lookup"><span data-stu-id="67f82-146">Empty strings are inherited by the XLIFF TM.</span></span> <span data-ttu-id="67f82-147">ソース内の**リベート**文字列がターゲット内に空の文字列を持つ場合、この XLIFF TM が使用されていると、空の文字列として変換される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="67f82-147">If a **Rebate** string in the source has an empty string in the target, it will likely be translated as an empty string if this XLIFF TM is used.</span></span>

    <span data-ttu-id="67f82-148">![文字列の欠落](./media/dts-align4.png "文字列の欠落")</span><span class="sxs-lookup"><span data-stu-id="67f82-148">![Missing strings](./media/dts-align4.png "Missing strings")</span></span>

<span data-ttu-id="67f82-149">アライン ツールはこれらの問題のいくつかを解決できますが、出力に予期しない結果が表示される前に防ぐ方が簡単です。</span><span class="sxs-lookup"><span data-stu-id="67f82-149">Although the Align tool can resolve some of these issues, it's easier if you prevent them before you see unexpected results in the output.</span></span>

<span data-ttu-id="67f82-150">TM として使用する前に、整合された XLIFF ファイルを確認します。</span><span class="sxs-lookup"><span data-stu-id="67f82-150">Review the aligned XLIFF file before you use it as a TM.</span></span> <span data-ttu-id="67f82-151">確認された TU は、未確認の TU と間違えないように **最終** または **サインオフ** とマークされます。</span><span class="sxs-lookup"><span data-stu-id="67f82-151">TUs that have been reviewed should be marked as **Final** or **Signed off**, so that they aren't mistaken for unreviewed TUs.</span></span>

## <a name="editing-an-xliff-translation-memory"></a><span data-ttu-id="67f82-152">XLIFF 翻訳メモリを編集</span><span class="sxs-lookup"><span data-stu-id="67f82-152">Editing an XLIFF translation memory</span></span>

<span data-ttu-id="67f82-153">無料の多言語エディターまたは別の XLIFF エディターを使用して、DTS が提供する XLIFF ファイル内の翻訳をレビューおよび編集することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="67f82-153">We recommend that you use the free Multilingual Editor, or another XLIFF editor, to review and edit the translations in the XLIFF file that DTS provides.</span></span> <span data-ttu-id="67f82-154">少なくとも、翻訳出力が製品の品質基準を満たしていることを確認するために、翻訳をレビューする必要があります。</span><span class="sxs-lookup"><span data-stu-id="67f82-154">At a minimum, you should review the translations to verify that the translation output meets your product's quality standards.</span></span>

<span data-ttu-id="67f82-155">多言語エディタで XLIFF ファイルを開くと、次の図のようになります。</span><span class="sxs-lookup"><span data-stu-id="67f82-155">When you open an XLIFF file in the Multilingual Editor, it resembles the following illustration.</span></span>

<span data-ttu-id="67f82-156">![多言語エディタでの XLIFF ファイル](./media/dts-editor1.png "多言語エディタでの XLIFF ファイル")</span><span class="sxs-lookup"><span data-stu-id="67f82-156">![XLIFF file in the Multilingual Editor](./media/dts-editor1.png "XLIFF file in the Multilingual Editor")</span></span>

<span data-ttu-id="67f82-157">各行の冒頭に円があることに確認します。</span><span class="sxs-lookup"><span data-stu-id="67f82-157">Notice that there is a circle near the beginning of each line.</span></span> <span data-ttu-id="67f82-158">円の色は翻訳の状態を示します。</span><span class="sxs-lookup"><span data-stu-id="67f82-158">The color of the circle indicates the state of the translation.</span></span> <span data-ttu-id="67f82-159">DTS は、文字列の出所に応じて、これらの状態を自動的に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="67f82-159">DTS automatically assigns these states, depending on where the string came from.</span></span>

+ <span data-ttu-id="67f82-160">**赤い円** – 文字列は機械翻訳されました。</span><span class="sxs-lookup"><span data-stu-id="67f82-160">**Red circle** – The string was machine-translated.</span></span> <span data-ttu-id="67f82-161">DTS は**確認が必要**状態を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="67f82-161">DTS assigns the **Needs Review** state.</span></span>

    > [!NOTE]
    > <span data-ttu-id="67f82-162">表示されている状態値は、使用している XLIFF エディターによって若干異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="67f82-162">The state value that is shown might differ slightly, depending on the XLIFF editor that you're using.</span></span>

+ <span data-ttu-id="67f82-163">**黄色、緑 / 黄色または緑の円** – その文字列はリサイクルされました。</span><span class="sxs-lookup"><span data-stu-id="67f82-163">**Yellow, green/yellow, or green circle** – The string was recycled.</span></span> <span data-ttu-id="67f82-164">DTS は、要求で使用された XLIFF TM から状態を継承しました。</span><span class="sxs-lookup"><span data-stu-id="67f82-164">DTS inherited the state from the XLIFF TM that was used in the request.</span></span>

<span data-ttu-id="67f82-165">翻訳を確認するには、**要確認** 状態にある文字列のみを表示するフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="67f82-165">To verify the translations, you can apply a filter to show only strings that are in the **Needs Review** state.</span></span>

<span data-ttu-id="67f82-166">![要レビュー状態での文字列](./media/dts-editor2.png "要レビュー状態でのファイル")</span><span class="sxs-lookup"><span data-stu-id="67f82-166">![Strings in the Needs Review state](./media/dts-editor2.png "Files in the Needs Review state")</span></span>

<span data-ttu-id="67f82-167">確認された文字列は **翻訳済み**、**最終**、または**サインオフ**とマークされ、再利用することができます。</span><span class="sxs-lookup"><span data-stu-id="67f82-167">Strings that have been reviewed should be marked as **Translated**, **Final**, or **Signed off**, so that they can be used for recycling.</span></span> <span data-ttu-id="67f82-168">**要レビュー**としてマークされている翻訳はリサイクルには含まれません。</span><span class="sxs-lookup"><span data-stu-id="67f82-168">Translations that are marked as **Needs Review** aren't included for recycling.</span></span>

<span data-ttu-id="67f82-169">XLIFF TM を編集した後、DTS はリフレッシュされた出力ファイルをソース形式で再生成します。</span><span class="sxs-lookup"><span data-stu-id="67f82-169">After you've finished editing the XLIFF TM, remember to have DTS regenerate the refreshed output file in the source format.</span></span> <span data-ttu-id="67f82-170">ファイルを再生成する方法の詳細については、[出力ファイルの再生成](./use-translation-service.md#regenerate-output-files) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="67f82-170">For more information about how to regenerate the file, see [Regenerate output files](./use-translation-service.md#regenerate-output-files).</span></span>

