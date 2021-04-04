---
title: 生成された ER レポートのトレース結果およびベースライン値との比較における改善
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations バージョン 10.0.3 (2019年6月) における ER ベースライン機能の改善について説明します。
author: NickSelin
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 1579a0bb0dcf21ae16a54969e57ca88301041076
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568952"
---
# <a name="improvements-in-tracing-the-results-of-generated-er-reports-and-comparing-them-with-baseline-values"></a><span data-ttu-id="ff0f6-103">生成された ER レポートのトレース結果およびベースライン値との比較における改善</span><span class="sxs-lookup"><span data-stu-id="ff0f6-103">Improvements in tracing the results of generated ER reports and comparing them with baseline values</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ff0f6-104">このトピックでは、電子申告 (ER) フレームワークのベースライン機能に対して行われた最初の一連の改善について説明します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-104">This topic describes the first set of improvements that have been made to the baseline feature of the Electronic reporting (ER) framework.</span></span> <span data-ttu-id="ff0f6-105">これらの改善は、Microsoft Dynamics 365 for Finance and Operations バージョン 10.0.3 (2019 年 6 月) 以降 で利用できます。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-105">These improvements are available in Microsoft Dynamics 365 for Finance and Operations version 10.0.3 (June 2019) and later.</span></span>

## <a name="automate-the-setting-of-baseline-rules"></a><span data-ttu-id="ff0f6-106">ベースライン ルールの設定の自動化</span><span class="sxs-lookup"><span data-stu-id="ff0f6-106">Automate the setting of baseline rules</span></span>

<span data-ttu-id="ff0f6-107">[生成されたレポート結果をトレースして、ベースライン値と比較する](er-trace-reports-compare-baseline.md)トピックでは、 ER 形式の実行に関する情報を収集し、その実行結果を評価するように ER フレームワークを構成する方法について説明しています。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-107">The [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic explains how to configure the ER framework to collect information about ER format executions and evaluate the results of those executions.</span></span> <span data-ttu-id="ff0f6-108">このトピックの例では、完了する必要があるステップを示します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-108">The example in this topic shows the steps that must be completed.</span></span>

<span data-ttu-id="ff0f6-109">次にステップの例を示します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-109">Here are some of the steps:</span></span>

- <span data-ttu-id="ff0f6-110">ER 形式を実行して送信ファイルを生成し、そのファイルをローカルに保存します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-110">Run an ER format to generate an outbound file, and store the file locally.</span></span>
- <span data-ttu-id="ff0f6-111">ローカルに保存されているファイルを、ER 形式用に追加されたベースラインの添付ファイルとして追加します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-111">Add the locally stored file as an attachment of the baseline that was added for an ER format.</span></span>
- <span data-ttu-id="ff0f6-112">追加したベースラインのベースライン ルールを構成します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-112">Configure the baseline rule for the added baseline.</span></span> <span data-ttu-id="ff0f6-113">この構成には、次のステップが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-113">This configuration includes the following steps:</span></span>

    - <span data-ttu-id="ff0f6-114">送信ファイルの生成に使用される ER 形式要素を指定します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-114">Specify an ER format element that is used to generate an outbound file.</span></span>
    - <span data-ttu-id="ff0f6-115">生成された発信ファイルを参照する添付ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-115">Select the attachment that refers to the generated outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="ff0f6-116">これらのステップは、新しい ER 機能を使用して自動化することはできますが、手動で行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-116">These steps must be done manually, even though the new ER capabilities enable them to be automated.</span></span> <span data-ttu-id="ff0f6-117">この機能の詳細を知るには、次の例を実行します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-117">To learn more about this feature, complete the following example.</span></span>

## <a name="example-automate-the-setting-of-baseline-rules"></a><span data-ttu-id="ff0f6-118">例: ベースライン ルールの設定の自動化</span><span class="sxs-lookup"><span data-stu-id="ff0f6-118">Example: Automate the setting of baseline rules</span></span>

<span data-ttu-id="ff0f6-119">この例のステップを完了するには、最初に[生成されたレポート結果をトレースして、ベースライン値と比較する](er-trace-reports-compare-baseline.md) トピックの例のステップの「デザインされた ER 形式の新しいベースラインの追加」までを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-119">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, up through the "Add a new baseline for a designed ER format" section.</span></span>

### <a name="review-added-baseline"></a><span data-ttu-id="ff0f6-120">追加したベースラインの確認</span><span class="sxs-lookup"><span data-stu-id="ff0f6-120">Review added baseline</span></span>

1. <span data-ttu-id="ff0f6-121">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-121">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="ff0f6-122">**ベースライン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-122">Select **Baselines**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ff0f6-123">アクション ウィンドウの **ベースライン** ボタンは、**デバッグ モードの実行** ER ユーザー パラメーターが現在の会社に対してオンになっている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-123">The **Baselines** button on the Action Pane is available only when the **Run in debug mode** ER user parameter is turned on for the current company.</span></span>

<span data-ttu-id="ff0f6-124">選択した **ER ベースラインを学習するための形式** 形式にベースラインが追加されましたが、このベースラインにはまだベースライン ルールが追加されていません。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-124">The baseline has been added for the selected **Format to learn ER baselines** format, but the baseline rules haven't yet been added for this baseline.</span></span>

<span data-ttu-id="ff0f6-125">![電子申告形式のベースライン ページ、ルールは未設定](media/GER-BaselineSample-AddBaseline2.PNG "電子申告形式のベースライン ページのスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="ff0f6-125">![Electronic reporting format baselines page, no rules yet](media/GER-BaselineSample-AddBaseline2.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="ff0f6-126">新しいベースライン ルールの作成</span><span class="sxs-lookup"><span data-stu-id="ff0f6-126">Make a new baseline rule</span></span>

1. <span data-ttu-id="ff0f6-127">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-127">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="ff0f6-128">ツリーで、**ER ベースラインを学習するためのモデル** を展開します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-128">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="ff0f6-129">ツリーで、**ER ベースラインを学習するためのモデル\\ER ベースラインを学習するための形式** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-129">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="ff0f6-130">**バージョン** クイック タブで、**実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-130">On the **Versions** FastTab, select **Run**.</span></span>
5. <span data-ttu-id="ff0f6-131">**ID を入力** フィールドで、**1** と入力します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-131">In the **Enter Id** field, enter **1**.</span></span>
6. <span data-ttu-id="ff0f6-132">**ベースライン ファイルの作成** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-132">Set the **Make baseline files** option to **Yes**.</span></span>
7. <span data-ttu-id="ff0f6-133">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-133">Select **OK**.</span></span>
8. <span data-ttu-id="ff0f6-134">**ベースライン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-134">Select **Baselines**.</span></span>

    <span data-ttu-id="ff0f6-135">![電子申告形式のベースライン ページ、選択したベースライン](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "電子申告形式のベースライン ページのスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="ff0f6-135">![Electronic reporting format baselines page, baselines selected](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

    <span data-ttu-id="ff0f6-136">生成された送信ファイルは、実行された ER 形式のベースラインに自動的に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-136">The generated outbound file has been automatically attached to the baseline of the executed ER format.</span></span> <span data-ttu-id="ff0f6-137">ベースライン ルールは、このベースラインに自動的に追加され、関連付けられたファイルへの参照も含まれます。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-137">The baseline rule has been automatically added to this baseline and also contains the reference to the attached file.</span></span>

9. <span data-ttu-id="ff0f6-138">**名前** フィールドに、**ベースライン 1** と入力します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-138">In the **Name** field, enter **Baseline 1**.</span></span>
10. <span data-ttu-id="ff0f6-139">**ファイル名マスク** フィールドに、**.xml** と入力します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-139">In the **File name mask** field, enter **.xml**.</span></span>
11. <span data-ttu-id="ff0f6-140">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-140">Select **Save**.</span></span>

### <a name="run-the-format"></a><span data-ttu-id="ff0f6-141">形式を実行する</span><span class="sxs-lookup"><span data-stu-id="ff0f6-141">Run the format</span></span>

<span data-ttu-id="ff0f6-142">これで、[生成されたレポート結果をトレースして、ベースライン値と比較する](er-trace-reports-compare-baseline.md) トピックの例の「デザインされた ER 形式を実行して結果を分析するためのログを確認する」から始まる残りのステップを完了する準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-142">You're now ready to complete the remaining steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, starting from the "Run the designed ER format and review the log to analyze the results" section.</span></span>

> [!NOTE]
> <span data-ttu-id="ff0f6-143">自動的に追加されたベースライン ルールを **ベースライン** クイックタブで削除しても、参照した添付ファイルが自動的に削除されることはありません。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-143">When you delete the automatically added baseline rule on the **Baselines** FastTab, the referenced attachment isn't automatically deleted.</span></span>

## <a name="configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="ff0f6-144">常に変化する ER 出力の部分を無視するようにベースラインを構成する</span><span class="sxs-lookup"><span data-stu-id="ff0f6-144">Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="ff0f6-145">ER 形式が、形式の実行時に変更される情報を含むように設計されている場合、ER ベースライン機能を使用して生成された結果とベースライン値を比較するには、形式を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-145">When an ER format has been designed to contain information that is changed when the format is run, the format must be required to use the ER baseline feature to compare the generated results with baseline values.</span></span> <span data-ttu-id="ff0f6-146">たとえば、情報は処理日時またはさまざまな形式で生成された文書の一意の識別子 (グローバル一意識別子 \[GUID\] など) になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-146">For example, the information might be the processing date and time or the unique identifier of a generated document in different formats (globally unique identifier \[GUID\], and so on).</span></span> <span data-ttu-id="ff0f6-147">新しい ER 機能を使用すると、ベースラインの値を形式の実行結果と比較することを目的として形式が実行される場合に、ER 形式の変更可能な要素を無視するようにベースライン ルールを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-147">The new ER capabilities let you configure the baseline rule so that it ignores changeable elements of an ER format when the format is run with the purpose of comparing baseline values with the results of the format's execution.</span></span> <span data-ttu-id="ff0f6-148">この機能の詳細を知るには、次の例を実行します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-148">To learn more about this feature, complete the following example.</span></span>

## <a name="example-configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="ff0f6-149">例: 常に変化する ER 出力の部分を無視するようにベースラインを構成する</span><span class="sxs-lookup"><span data-stu-id="ff0f6-149">Example: Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="ff0f6-150">この例のステップを完了するには、最初に[生成されたレポート結果をトレースして、ベースライン値と比較する](er-trace-reports-compare-baseline.md) トピックの例のステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-150">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic.</span></span>

### <a name="modify-a-configured-er-format"></a><span data-ttu-id="ff0f6-151">構成された ER 形式の変更</span><span class="sxs-lookup"><span data-stu-id="ff0f6-151">Modify a configured ER format</span></span>

1. <span data-ttu-id="ff0f6-152">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-152">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="ff0f6-153">ツリーで、**ER ベースラインを学習するためのモデル** を展開します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-153">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="ff0f6-154">ツリーで、**ER ベースラインを学習するためのモデル\\ER ベースラインを学習するための形式** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-154">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="ff0f6-155">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-155">Select **Designer**.</span></span>
5. <span data-ttu-id="ff0f6-156">ツリーで、**出力\\ドキュメント** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-156">In the tree, select **Output\\Document**.</span></span>
6. <span data-ttu-id="ff0f6-157">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-157">Select **Add**.</span></span>
7. <span data-ttu-id="ff0f6-158">ドロップダウン ダイアログ ボックスのツリーで、**XML\\属性** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-158">In the drop-down dialog box, in the tree, select **XML\\Attribute**.</span></span>
8. <span data-ttu-id="ff0f6-159">**名前** フィールドに、**ProcessingDateTime** と入力します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-159">In the **Name** field, enter **ProcessingDateTime**.</span></span>
9. <span data-ttu-id="ff0f6-160">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-160">Select **OK**.</span></span>
10. <span data-ttu-id="ff0f6-161">ツリーの **マッピング** タブで、**出力\\ドキュメント\\ProcessingDateTime** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-161">On the **Mapping** tab, in the tree, select **Output\\Document\\ProcessingDateTime**.</span></span>
11. <span data-ttu-id="ff0f6-162">**式の編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-162">Select **Edit formula**.</span></span>
12. <span data-ttu-id="ff0f6-163">**式** フィールドで、次の式を入力します。**DATETIMEFORMAT(NOW(), "O")**</span><span class="sxs-lookup"><span data-stu-id="ff0f6-163">In the **Formula** field, enter the following expression: **DATETIMEFORMAT(NOW(), "O")**</span></span>
13. <span data-ttu-id="ff0f6-164">**保存** を選択してから、**テスト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-164">Select **Save**, and then select **Test**.</span></span>
14. <span data-ttu-id="ff0f6-165">再度 **テスト** を選択して、構成されている式を再テストします。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-165">Select **Test** again to retest the configured expression.</span></span>

    <span data-ttu-id="ff0f6-166">![フォーミュラ デザイナー ページ](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "フォーミュラ デザイナー ページのスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="ff0f6-166">![Formula designer page](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Screenshot of the Formula designer page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="ff0f6-167">**テスト結果** タブは、構成された式が呼び出されるたびに、異なる日付と時刻の値を返すことを示します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-167">The **Test result** tab shows that the configured expression returns a different date and time value whenever it's called.</span></span>

15. <span data-ttu-id="ff0f6-168">**フォーミュラ デザイナー** ページを閉じて、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-168">Close the **Formula designer** page, and then select **Save**.</span></span>

    <span data-ttu-id="ff0f6-169">![形式デザイナーのページ](media/GER-BaselineSample-FormatMappingDesign2.PNG "形式デザイナー ページのスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="ff0f6-169">![Format designer page](media/GER-BaselineSample-FormatMappingDesign2.PNG "Screenshot of the Format designer page")</span></span>

16. <span data-ttu-id="ff0f6-170">**形式デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-170">Close the **Format designer** page.</span></span>

### <a name="remove-an-existing-baseline-rule"></a><span data-ttu-id="ff0f6-171">既存のベースライン ルールの削除</span><span class="sxs-lookup"><span data-stu-id="ff0f6-171">Remove an existing baseline rule</span></span>

1. <span data-ttu-id="ff0f6-172">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-172">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="ff0f6-173">**ベースライン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-173">Select **Baselines**.</span></span>
3. <span data-ttu-id="ff0f6-174">ベースラインの一覧で、**ER ベースラインを学習するための形式** 形式に対して構成されているベースラインを選択します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-174">In the list of baselines, select the baseline that is configured for the **Format to learn ER baselines** format.</span></span>
4. <span data-ttu-id="ff0f6-175">**ベースライン** クイックタブで、**削除** を選択して先ほど構成したベースライン ルールを削除します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-175">On the **Baselines** FastTab, select **Delete** to remove the baseline rule that you configured earlier.</span></span>

<span data-ttu-id="ff0f6-176">![電子申告形式のベースライン ページ、削除済](media/GER-BaselineSample-AddBaseline3.PNG "電子申告形式のベースライン ページのスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="ff0f6-176">![Electronic reporting format baselines page, deleted](media/GER-BaselineSample-AddBaseline3.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="define-replacements-for-bindings-of-designed-er-format"></a><span data-ttu-id="ff0f6-177">デザインされたER形式のバインドの置換を定義する</span><span class="sxs-lookup"><span data-stu-id="ff0f6-177">Define replacements for bindings of designed ER format</span></span>

1. <span data-ttu-id="ff0f6-178">**置換** クイックタブの **構成** ページで、**コンポーネントの選択** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-178">On the **Configurations** page, on the **Replacements** FastTab, select **Select components**.</span></span>
2. <span data-ttu-id="ff0f6-179">形式のコンポーネント ツリーで、**出力** を展開して、**出力\\ドキュメント** を展開し、**出力\\ドキュメント\\ProcessingDateTime** のチェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-179">In the format components tree, expand **Output**, expand **Output\\Document**, and then select the check box for **Output\\Document\\ProcessingDateTime**.</span></span>
3. <span data-ttu-id="ff0f6-180">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-180">Select **OK**.</span></span>

<span data-ttu-id="ff0f6-181">![電子申告形式のベースライン ページ、コンポーネント](media/GER-BaselineSample-AddBaseline4.PNG "電子申告形式のベースライン ページのスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="ff0f6-181">![Electronic reporting format baselines page, components](media/GER-BaselineSample-AddBaseline4.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

<span data-ttu-id="ff0f6-182">選択した ER 形式のコンポーネントが、**置換** クイックタブのコンポーネントの一覧に追加されました。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-182">The selected ER format component has been added to the list of components on the **Replacements** FastTab.</span></span> <span data-ttu-id="ff0f6-183">基本 ER 形式をデバッグ モードで実行すると、各コンポーネントの形式のバインドは、**バインド** 列に表示されるバインドによって置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-183">When the base ER format is run in debug mode, the format's binding for each component will be replaced by the binding that is shown in the **Binding** column.</span></span> <span data-ttu-id="ff0f6-184">**置換** クイックタブに表示されているコンポーネントの既定のバインドを変更するには、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-184">To change the default binding for a component that is listed on the **Replacements** FastTab, select **Edit**.</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="ff0f6-185">新しいベースライン ルールの作成</span><span class="sxs-lookup"><span data-stu-id="ff0f6-185">Make a new baseline rule</span></span>

<span data-ttu-id="ff0f6-186">このトピックで前述した「例: ベースライン ルールの設定の自動化」のステップに従ってください。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-186">Follow the steps in the "Example: Automate the setting of baseline rules" section earlier in this topic.</span></span> <span data-ttu-id="ff0f6-187">通知は、送信ファイルがベースライン設定を使用して生成されたこと、および形式バインドの強制的な置換が行われたことを警告します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-187">A notification warns you that the outbound file has been generated by using baseline settings, and that a forced replacement of the format bindings has occurred.</span></span>

<span data-ttu-id="ff0f6-188">![構成ページの通知](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "構成ページの通知のスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="ff0f6-188">![Notification on the Configurations page](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Screenshot of the notification on the Configurations page")</span></span>

### <a name="suppress-warnings-about-the-replacement-of-format-bindings"></a><span data-ttu-id="ff0f6-189">形式バインドの置換に関する警告を非表示にする</span><span class="sxs-lookup"><span data-stu-id="ff0f6-189">Suppress warnings about the replacement of format bindings</span></span>

<span data-ttu-id="ff0f6-190">特定の ER パラメーターを設定することにより、形式バインドの置換に関する通知を非表示にすることができます。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-190">By setting specific ER parameters, you can suppress notifications that warn about the replacement of format bindings.</span></span> <span data-ttu-id="ff0f6-191">これは、Regression Suite Automation Tool を使用して無人モードで形式バインドを置換する場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-191">This suppression can be useful when format bindings are replaced in an unattended mode by using the Regression Suite Automation Tool.</span></span> <span data-ttu-id="ff0f6-192">この場合、警告は実行中のテスト ケースの失敗とみなすことができます。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-192">In this case, the warning can be considered a failure of the test case that is running.</span></span>

1. <span data-ttu-id="ff0f6-193">**構成** ページのアクション ウィンドウの **構成** タブで、**ユーザー パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-193">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, select **User parameters**.</span></span>
2. <span data-ttu-id="ff0f6-194">**ベースラインの警告を非表示にする** オプションを **はい** に設定して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-194">Set the **Suppress baseline warnings** option to **Yes**, and then select **OK**.</span></span>

### <a name="review-the-generated-baseline-file"></a><span data-ttu-id="ff0f6-195">生成したベースライン ファイルを確認します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-195">Review the generated baseline file</span></span>

1. <span data-ttu-id="ff0f6-196">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-196">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="ff0f6-197">**ベースライン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-197">Select **Baselines**.</span></span>
3. <span data-ttu-id="ff0f6-198">**添付ファイル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-198">Select **Attachments**.</span></span>
    > [!NOTE]
    > <span data-ttu-id="ff0f6-199">生成されるファイルには、形式のバインドではなく、追加したベースラインで構成されたバインドからの処理日時テキスト (**"#"**) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-199">The generated file contains the processing date and time text (**"#"**) from the binding that was configured in the added baseline rule, not from the format's binding.</span></span>
    
4. <span data-ttu-id="ff0f6-200">**添付ファイル** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-200">Close the **Attachments** page.</span></span>

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a><span data-ttu-id="ff0f6-201">デザインされた ER 形式を実行し、ログを確認して結果を分析する</span><span class="sxs-lookup"><span data-stu-id="ff0f6-201">Run the designed ER format and review the log to analyze the results</span></span>

1. <span data-ttu-id="ff0f6-202">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-202">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="ff0f6-203">ツリーで、**ER ベースラインを学習するためのモデル** を展開します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-203">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="ff0f6-204">ツリーで、**ER ベースラインを学習するためのモデル\\ER ベースラインを学習するための形式** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-204">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="ff0f6-205">**バージョン** クイック タブで、**実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-205">On the **Versions** FastTab select **Run**.</span></span>
5. <span data-ttu-id="ff0f6-206">**ID を入力** フィールドで、**1** とタイプします。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-206">In the **Enter Id** field, type **1**.</span></span>
6. <span data-ttu-id="ff0f6-207">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-207">Select **OK**.</span></span>
7. <span data-ttu-id="ff0f6-208">**組織管理** \> **電子申告** \> **構成デバッグ ログ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-208">Go to **Organization administration** \> **Electronic reporting** \> **Configuration debug logs**.</span></span>

<span data-ttu-id="ff0f6-209">実行ログには、生成されたファイルと構成されたベースラインとの比較の結果に関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-209">The execution log contains information about the results of the comparison of the generated file with the configured baseline.</span></span> <span data-ttu-id="ff0f6-210">ログは生成されたファイルとベースラインが同じであることを示していますが、実行された形式には送信ファイルに常に変化する日付と時刻の値を入力するためのバインドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-210">The log indicates that the generated file and the baseline are equal, even though the executed format contains the binding to enter a constantly changing date and time value in the outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="ff0f6-211">送信ファイルは、形式のバインドを強制的に置換するベースライン設定を使用して生成されていますが、置換に関する警告は表示されません。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-211">Although the outbound file has been generated by using baseline settings that force the replacement of the format's bindings, you don't receive any warnings about the replacement.</span></span>

## <a name="exchange-baseline-settings-between-environments"></a><span data-ttu-id="ff0f6-212">環境間でのベースライン設定の交換</span><span class="sxs-lookup"><span data-stu-id="ff0f6-212">Exchange baseline settings between environments</span></span>

### <a name="export-baseline-settings"></a><span data-ttu-id="ff0f6-213">ベースラインの設定をエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-213">Export baseline settings</span></span>

<span data-ttu-id="ff0f6-214">新しい ER 機能を使用すると、選択した ER 形式のベースライン設定を現在の環境からエクスポートし、それらを XML ファイルとして保存できます。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-214">The new ER capabilities let you export baseline settings for the selected ER format from the current environment and store them as XML files.</span></span> 

<span data-ttu-id="ff0f6-215">ベースライン設定をエクスポートするには、**電子申告形式のベースライン** ページで **エクスポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-215">To export baseline settings, on the **Electronic reporting format baselines** page, select **Export**.</span></span>

### <a name="import-baseline-settings"></a><span data-ttu-id="ff0f6-216">ベースライン設定をインポートします</span><span class="sxs-lookup"><span data-stu-id="ff0f6-216">Import baseline settings</span></span>

<span data-ttu-id="ff0f6-217">エクスポートされたベースライン設定は、別の環境にインポートできます。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-217">Exported baseline settings can be imported into a different environment.</span></span> <span data-ttu-id="ff0f6-218">まず、環境を ER 形式としてインポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-218">The environment must first be imported as an ER format.</span></span> <span data-ttu-id="ff0f6-219">その後、ベースライン設定をインポートできます。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-219">You can then import the baseline settings.</span></span>

<span data-ttu-id="ff0f6-220">ローカルに保存されている XML ファイルからベースライン設定をインポートするには、**電子申告形式のベースライン** ページで **インポート** を選択して、その後 **参照** を選択して XML ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-220">To import baseline settings from a locally stored XML file, on the **Electronic reporting format baselines** page, select **Import**, and then select **Browse** to select the XML file.</span></span>

<span data-ttu-id="ff0f6-221">![ベースライン設定のインポート ダイアログ ボックス](media/GER-BaselineSample-ImportBaseline1.PNG "ベースライン設定のインポート ダイアログ ボックスのスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="ff0f6-221">![Import baseline settings dialog box](media/GER-BaselineSample-ImportBaseline1.PNG "Screenshot of the Import baseline settings dialog box")</span></span>

<span data-ttu-id="ff0f6-222">現在のドキュメント管理設定と選択したドキュメント タイプに基づいて、Microsoft SharePoint Server に保存されている XML ファイルからベースライン設定をインポートするには、**電子申告形式のベースライン** ページで、**ソースからインポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-222">To import baseline settings from an XML file that is stored on the Microsoft SharePoint Server, based on the current Document management settings and the selected document type, on the **Electronic reporting format baselines** page, select **Import from source**.</span></span> <span data-ttu-id="ff0f6-223">その後、ドキュメント タイプと XML ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-223">Then select the document type and the XML file.</span></span> <span data-ttu-id="ff0f6-224">SharePoint フォルダーへのアクセスに必要なドキュメント タイプは事前に構成されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-224">The required document type to access the SharePoint folder must be configured in advance.</span></span>

<span data-ttu-id="ff0f6-225">![ソースからインポート ダイアログ ボックス](media/GER-BaselineSample-ImportBaseline2.PNG "ソースからインポート ダイアログ ボックスのスクリーンショット")</span><span class="sxs-lookup"><span data-stu-id="ff0f6-225">![Import from source dialog box](media/GER-BaselineSample-ImportBaseline2.PNG "Screenshot of the Import from source dialog box")</span></span>

> [!NOTE]
> <span data-ttu-id="ff0f6-226">**ソースからインポート** ダイアログ ボックスで、必要なドキュメント タイプおよびファイル名を選択するためのステップを、タスク レコーダーを使用して記録できます。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-226">You can use Task recorder to record the steps for selecting the required document type and the file name in the **Import from source** dialog box.</span></span> <span data-ttu-id="ff0f6-227">この方法により、必要なベースライン設定を SharePoint Server に保持した後、Regression Suite Automation Tool を使用して自動テストを実行する際に、タスク記録を再生することによって自動的にそれらをインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="ff0f6-227">In this way, you can keep required baseline settings on SharePoint Server and then automatically import them by playing a task recording when you run automated tests by using the Regression Suite Automation Tool.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ff0f6-228">追加リソース</span><span class="sxs-lookup"><span data-stu-id="ff0f6-228">Additional resources</span></span>

- [<span data-ttu-id="ff0f6-229">生成されたレポート結果を追跡し、ベースライン値と比較する</span><span class="sxs-lookup"><span data-stu-id="ff0f6-229">Trace generated report results and compare them with baseline values</span></span>](er-trace-reports-compare-baseline.md)
- [<span data-ttu-id="ff0f6-230">タスク レコーダー リソース</span><span class="sxs-lookup"><span data-stu-id="ff0f6-230">Task recorder resources</span></span>](../user-interface/task-recorder.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]