---
title: 初期の顧客支払予測モデルを評価する (プレビュー)
description: このトピックでは、顧客支払予測モデルを理解し、その有効性を評価するために実行できる手順について説明します。
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 014684595c7cd65383dc12d9eec2dd8ea7b8c20f
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186741"
---
# <a name="evaluate-the-initial-customer-payment-prediction-model-preview"></a><span data-ttu-id="f60fa-103">初期の顧客支払予測モデルを評価する (プレビュー)</span><span class="sxs-lookup"><span data-stu-id="f60fa-103">Evaluate the initial customer payment prediction model (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="f60fa-104">このトピックでは、財務インサイトをオンにして、最初のモデルを生成およびトレーニングした後、予測モデルを評価する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f60fa-104">This topic explains how to evaluate a prediction model after you've turned on Finance Insights and then generated and trained your first model.</span></span> <span data-ttu-id="f60fa-105">このトピックでは、顧客支払を予測するためのモデルについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f60fa-105">This topic addresses models for predicting customer payments.</span></span> <span data-ttu-id="f60fa-106">顧客支払予測モデルを理解し、その有効性を評価するために実行できる手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="f60fa-106">It describes the steps that you can take to understand the customer payment prediction model and evaluate its effectiveness.</span></span>

## <a name="getting-details-about-the-model"></a><span data-ttu-id="f60fa-107">モデルに関する詳細の取得</span><span class="sxs-lookup"><span data-stu-id="f60fa-107">Getting details about the model</span></span>

<span data-ttu-id="f60fa-108">Microsoft Dynamics 365 Finance の **財務インサイト パラメーター** ページで、**モデル精度の改善** リンクが精度スコアの横に表示されます。</span><span class="sxs-lookup"><span data-stu-id="f60fa-108">On the **Finance Insights parameters** page in Microsoft Dynamics 365 Finance, an **Improve model accuracy** link appears next to the accuracy score.</span></span>

<span data-ttu-id="f60fa-109">[![モデル精度の改善リンク](./media/prediction-model.png)](./media/prediction-model.png)</span><span class="sxs-lookup"><span data-stu-id="f60fa-109">[![Improve model accuracy link](./media/prediction-model.png)](./media/prediction-model.png)</span></span>

<span data-ttu-id="f60fa-110">このリンクは、AI Builder へのリンクであり、現在のモデルについての詳細を確認したり、改善するための手順を実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="f60fa-110">This link takes you to AI Builder, where you can learn more about the current model and also take steps to improve it.</span></span> <span data-ttu-id="f60fa-111">次の図は、開いたページを示しています。</span><span class="sxs-lookup"><span data-stu-id="f60fa-111">The following illustration shows the page that is opened.</span></span>

<span data-ttu-id="f60fa-112">[![AI Builder](./media/what-to-predict.png)](./media/what-to-predict.png)</span><span class="sxs-lookup"><span data-stu-id="f60fa-112">[![AI Builder](./media/what-to-predict.png)](./media/what-to-predict.png)</span></span>

<span data-ttu-id="f60fa-113">開いたページには、次の情報が表示されます:</span><span class="sxs-lookup"><span data-stu-id="f60fa-113">The page that is opened shows the following information:</span></span>

- <span data-ttu-id="f60fa-114">**パフォーマンス** セクションでは、モデル パフォーマンスの等級は、モデルの品質に関する分析視点を提供します。</span><span class="sxs-lookup"><span data-stu-id="f60fa-114">In the **Performance** section, the model performance grade provides perspective on the quality of the model.</span></span> <span data-ttu-id="f60fa-115">この等級の詳細については、AI Builder ドキュメントの [予測モデルのパフォーマンス](/ai-builder/prediction-performance) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f60fa-115">For more information about this grade, see [Prediction model performance](/ai-builder/prediction-performance) in the AI Builder documentation.</span></span>
- <span data-ttu-id="f60fa-116">**最も影響力のあるデータ** セクションでは、モデルに対して異なる入力タイプのデータの重要性を示します。</span><span class="sxs-lookup"><span data-stu-id="f60fa-116">The **Most influential data** section shows how important different input types of data were for your model.</span></span> <span data-ttu-id="f60fa-117">このリストと対応する割合を評価して、情報がビジネスと市場に関する知識と一致しているかどうかを判断できます。</span><span class="sxs-lookup"><span data-stu-id="f60fa-117">You can evaluate this list and the corresponding percentages to determine whether the information is consistent with what you know about your business and market.</span></span>

    <span data-ttu-id="f60fa-118">[![予測モデルのパフォーマンスと最も影響力のあるデータセクション](./media/models.png)](./media/models.png)</span><span class="sxs-lookup"><span data-stu-id="f60fa-118">[![Performance and Most influential data sections for the prediction model](./media/models.png)](./media/models.png)</span></span>

- <span data-ttu-id="f60fa-119">**パフォーマンス** セクションで **詳細を表示** を選択して、等級やその他の考慮事項の詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="f60fa-119">In the **Performance** section, select **See details** to learn more about the grade and other considerations.</span></span> <span data-ttu-id="f60fa-120">次の図では、モデルが推奨されている情報よりも少ない情報を使用していることを詳細に示しています。</span><span class="sxs-lookup"><span data-stu-id="f60fa-120">In the following illustration, the details show that the model uses less information than is recommended.</span></span> <span data-ttu-id="f60fa-121">したがって、システムは警告メッセージを生成しました。</span><span class="sxs-lookup"><span data-stu-id="f60fa-121">Therefore, the system has generated a warning message.</span></span>

    <span data-ttu-id="f60fa-122">[![モデルのパフォーマンスに関する警告](./media/details.png)](./media/details.png)</span><span class="sxs-lookup"><span data-stu-id="f60fa-122">[![Warnings about the model's performance](./media/details.png)](./media/details.png)</span></span>

## <a name="digging-deeper"></a><span data-ttu-id="f60fa-123">専門的な情報</span><span class="sxs-lookup"><span data-stu-id="f60fa-123">Digging deeper</span></span>

<span data-ttu-id="f60fa-124">精度はモデルを評価するための良い出発点であり、パフォーマンスの等級は分析視点を提供しますが、AI Builder は評価に使用できるより詳細なメトリックを提供します。</span><span class="sxs-lookup"><span data-stu-id="f60fa-124">Although accuracy is a good starting point for evaluating a model, and the performance grade provides perspective, AI Builder provides more detailed metrics that you can use for your evaluation.</span></span> <span data-ttu-id="f60fa-125">詳細をダウンロードするには、**パフォーマンス** セクションで **モデルの使用** ボタンの横にある省略記号ボタン (**...**) ボタンを選択し、**詳細なメトリックをダウンロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f60fa-125">To download the details, in the **Performance** section, select the ellipsis button (**...**) next to the **Use model** button, and then select **Download detailed metrics**.</span></span>

<span data-ttu-id="f60fa-126">[![詳細なメトリックスのダウンロード コマンド](./media/performance.png)](./media/performance.png)</span><span class="sxs-lookup"><span data-stu-id="f60fa-126">[![Download detailed metrics command](./media/performance.png)](./media/performance.png)</span></span>

<span data-ttu-id="f60fa-127">次の図は、データをダウンロードできる形式を示します。</span><span class="sxs-lookup"><span data-stu-id="f60fa-127">The following illustration shows the format that you can download the data in.</span></span>

<span data-ttu-id="f60fa-128">[![ダウンロードしたデータの形式](./media/data-format.png)](./media/data-format.png)</span><span class="sxs-lookup"><span data-stu-id="f60fa-128">[![Format of downloaded data](./media/data-format.png)](./media/data-format.png)</span></span>

<span data-ttu-id="f60fa-129">結果をより詳細に分析するには、"混同行列" メトリックを確認することが出発点になります。</span><span class="sxs-lookup"><span data-stu-id="f60fa-129">For a deeper analysis of the results, a good starting point is to review the "Confusion Matrix" metric.</span></span> <span data-ttu-id="f60fa-130">たとえば、前述の図で、このメトリックに対して示されているデータは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="f60fa-130">For example, here is the data that is shown for this metric in the previous illustration.</span></span>

`{"name": "Confusion Matrix", "value": {"schema_type": "confusion_matrix", "schema_version": "1.0.0", "data": {"class_labels": ["0", "1", "2"], "matrix": [[71, 9, 21], [5, 0, 27], [2, 0, 45]]}}, "type": "dictionaryNumericalList", "isGlobalScore": false}`

<span data-ttu-id="f60fa-131">このデータは、次の方法で拡張できます。</span><span class="sxs-lookup"><span data-stu-id="f60fa-131">You can expand this data in the following way.</span></span>

| &nbsp;                   | <span data-ttu-id="f60fa-132">予測期限内</span><span class="sxs-lookup"><span data-stu-id="f60fa-132">Predicted On time</span></span> | <span data-ttu-id="f60fa-133">予測遅延</span><span class="sxs-lookup"><span data-stu-id="f60fa-133">Predicted Late</span></span> | <span data-ttu-id="f60fa-134">予測かなりの遅延</span><span class="sxs-lookup"><span data-stu-id="f60fa-134">Predicted Very late</span></span> |
|--------------------------|-------------------|----------------|---------------------|
| <span data-ttu-id="f60fa-135">実際の期限内の支払</span><span class="sxs-lookup"><span data-stu-id="f60fa-135">Actual on time payment</span></span>   | <span data-ttu-id="f60fa-136">**71**</span><span class="sxs-lookup"><span data-stu-id="f60fa-136">**71**</span></span>            | <span data-ttu-id="f60fa-137">0</span><span class="sxs-lookup"><span data-stu-id="f60fa-137">0</span></span>              | <span data-ttu-id="f60fa-138">21</span><span class="sxs-lookup"><span data-stu-id="f60fa-138">21</span></span>                  |
| <span data-ttu-id="f60fa-139">実際の遅延支払</span><span class="sxs-lookup"><span data-stu-id="f60fa-139">Actual late payment</span></span>      | <span data-ttu-id="f60fa-140">5</span><span class="sxs-lookup"><span data-stu-id="f60fa-140">5</span></span>                 | <span data-ttu-id="f60fa-141">**0**</span><span class="sxs-lookup"><span data-stu-id="f60fa-141">**0**</span></span>          | <span data-ttu-id="f60fa-142">27</span><span class="sxs-lookup"><span data-stu-id="f60fa-142">27</span></span>                  |
| <span data-ttu-id="f60fa-143">実際のかなりの遅延支払</span><span class="sxs-lookup"><span data-stu-id="f60fa-143">Actual very late payment</span></span> | <span data-ttu-id="f60fa-144">2</span><span class="sxs-lookup"><span data-stu-id="f60fa-144">2</span></span>                 | <span data-ttu-id="f60fa-145">0</span><span class="sxs-lookup"><span data-stu-id="f60fa-145">0</span></span>              | <span data-ttu-id="f60fa-146">**45**</span><span class="sxs-lookup"><span data-stu-id="f60fa-146">**45**</span></span>              |

<span data-ttu-id="f60fa-147">混同行列には、トレーニング プロセスからランダムに選択されたテスト データセットの結果が示されます。</span><span class="sxs-lookup"><span data-stu-id="f60fa-147">The confusion matrix shows the results of a randomly selected test dataset from the training process.</span></span> <span data-ttu-id="f60fa-148">これらの終了した請求書はモデルのトレーニングに使用されていなかったため、モデルの良いテスト ケースです。</span><span class="sxs-lookup"><span data-stu-id="f60fa-148">Because these closed invoices weren't used to train the model, they are good test cases for the model.</span></span> <span data-ttu-id="f60fa-149">また、請求書の実際の状態がわかっているので、モデルのパフォーマンスを表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="f60fa-149">Additionally, because the actual state of the invoice is known, the model's performance can also be seen.</span></span>

<span data-ttu-id="f60fa-150">最初に検索するのは、最も一般的な実績値です。</span><span class="sxs-lookup"><span data-stu-id="f60fa-150">The first thing to look for is the most common actual value.</span></span> <span data-ttu-id="f60fa-151">この値は、データセット全体と完全に一致しているわけではありませんが、妥当な近似値です。</span><span class="sxs-lookup"><span data-stu-id="f60fa-151">Although this value might not be perfectly aligned with the overall dataset, it's a reasonable approximation.</span></span> <span data-ttu-id="f60fa-152">この場合、**実際の期限内の支払** は請求書合計 171 件のうち 92 件で発生し、最も一般的な実際値になります。</span><span class="sxs-lookup"><span data-stu-id="f60fa-152">In this case, **Actual on time payment** occurs for 92 of the 171 total invoices and is the most common actual value.</span></span> <span data-ttu-id="f60fa-153">したがって、モデルのベースラインとして適しています。</span><span class="sxs-lookup"><span data-stu-id="f60fa-153">Therefore, it's a good baseline for your model.</span></span> <span data-ttu-id="f60fa-154">すべての請求書が期限内に処理されると予想した場合、171 回中 92 回 (つまり 54％ の確率) が正しく処理されます。</span><span class="sxs-lookup"><span data-stu-id="f60fa-154">If you just guessed that all invoices would be on time, you would be correct 92 out of 171 times (that is, 54 percent of the time).</span></span>

<span data-ttu-id="f60fa-155">データセットのバランスを理解することが重要です。</span><span class="sxs-lookup"><span data-stu-id="f60fa-155">It's important that you understand how balanced your dataset is.</span></span> <span data-ttu-id="f60fa-156">この場合、171 件の請求書のうち 92 件は期限内に支払われ、32 件は支払いが遅れ、47 件は非常に遅れて支払われました。</span><span class="sxs-lookup"><span data-stu-id="f60fa-156">In this case, 92 out of 171 invoices were paid on time, 32 were paid late, and 47 were paid very late.</span></span> <span data-ttu-id="f60fa-157">これらの値は、各分類において重要な結果があるため、適度にバランスをとったデータセットを示します。</span><span class="sxs-lookup"><span data-stu-id="f60fa-157">These values indicate a reasonably balanced dataset, because there are non-trivial results in each classification.</span></span> <span data-ttu-id="f60fa-158">いずれかの状態において結果が非常に少ない状況は、機械学習モデルにとって困難な場合があります。</span><span class="sxs-lookup"><span data-stu-id="f60fa-158">A situation where one of the states has very few results can be challenging for a machine learning model.</span></span>

<span data-ttu-id="f60fa-159">モデルの精度は、テスト データセットの正しい予測の数を示します。</span><span class="sxs-lookup"><span data-stu-id="f60fa-159">The accuracy of the model indicates the number of correct predictions for the test dataset.</span></span> <span data-ttu-id="f60fa-160">これらの正しい予測は、前の例で太字で示した値です。</span><span class="sxs-lookup"><span data-stu-id="f60fa-160">These correct predictions are the values that are shown in bold in the preceding example.</span></span> <span data-ttu-id="f60fa-161">この場合、これらの値は、計算精度 67.8% (= \[71 + 0 + 45\] ÷ 171) となります。</span><span class="sxs-lookup"><span data-stu-id="f60fa-161">In this case, the values produce a calculated accuracy of 67.8 percent (= \[71 + 0 + 45\] ÷ 171).</span></span> <span data-ttu-id="f60fa-162">この値はベースラインの推測値 54% に対して 14% の改善を表し、モデルの品質の 1 つの指標です。</span><span class="sxs-lookup"><span data-stu-id="f60fa-162">This value represents an improvement of 14 percent over the baseline guess of 54 percent and is one indicator of the model's quality.</span></span>

<span data-ttu-id="f60fa-163">混同行列をさらに詳しく見ると、このモデルが、期限内およびかなりの遅い請求書の支払いを、予測するの適していることがわかります。</span><span class="sxs-lookup"><span data-stu-id="f60fa-163">If you look more closely at the confusion matrix, you will notice that the model does a good job of predicting on-time and very late invoice payments.</span></span> <span data-ttu-id="f60fa-164">ただし、実際に支払いが遅れた (しかし、それほど遅れていいない) 32 件の請求書すべてについて間違っています。</span><span class="sxs-lookup"><span data-stu-id="f60fa-164">However, it's wrong about all 32 invoices that were actually paid late (but not very late).</span></span> <span data-ttu-id="f60fa-165">この結果は、モデルの追加調査と改善が必要であることを示しています。</span><span class="sxs-lookup"><span data-stu-id="f60fa-165">This result suggests that additional exploration and improvement of the model are required.</span></span>

<span data-ttu-id="f60fa-166">精度より良いモデルのパフォーマンスを表す数値は、F1 マクロ スコアです。</span><span class="sxs-lookup"><span data-stu-id="f60fa-166">A number that represents the performance of the model better than accuracy is the F1 Macro score.</span></span> <span data-ttu-id="f60fa-167">このスコアでは、各分類の状態 (期限内、遅延、かなりの遅延) の結果が考慮されます。</span><span class="sxs-lookup"><span data-stu-id="f60fa-167">This score considers the results of each classification state (on-time, late, and very late).</span></span> <span data-ttu-id="f60fa-168">たとえば、前述の図で、"F1 マクロ" メトリックに対して示されているデータは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="f60fa-168">For example, here is the data that is shown for the "F1 Macro" metric in the previous illustration.</span></span>

`{"name": "F1 Macro", "value": 0.4927170868347339, "type": "percentage", "isGlobalScore": false}`

<span data-ttu-id="f60fa-169">この場合、約 49.3% の F1 マクロ スコアは、それなりに高いと思われる全体的な精度スコアにもかかわらず、各状態において、モデルが効果的な予測をできていないことを示してます。</span><span class="sxs-lookup"><span data-stu-id="f60fa-169">In this case, the F1 Macro score of approximately 49.3 percent indicates that the model doesn't provide effective predictions across each state, despite an overall accuracy score that seems reasonably high.</span></span>

## <a name="improving-the-model"></a><span data-ttu-id="f60fa-170">モデルの改善</span><span class="sxs-lookup"><span data-stu-id="f60fa-170">Improving the model</span></span>

<span data-ttu-id="f60fa-171">最初のモデルの結果をよく理解した後、機能列を追加または削除したり、正確な予測をサポートしていないデータセットの一部をフィルタリングしたりすることにより、モデルを改善することができます。</span><span class="sxs-lookup"><span data-stu-id="f60fa-171">After you understand the results of your first model better, you might want to improve the model by adding or removing feature columns, or by filtering any parts of the dataset that don't support accurate predictions.</span></span> <span data-ttu-id="f60fa-172">AI Builder を閉じ、Dynamics 365 Finance での **モデルの改善** リンクを使用して、AI Builder プロセスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="f60fa-172">Close AI Builder, and then use the **Improve model** link in Dynamics 365 Finance to restart the AI Builder process.</span></span> <span data-ttu-id="f60fa-173">公開されたモデルに影響を与えずに、さまざまな特性を試すことができます。</span><span class="sxs-lookup"><span data-stu-id="f60fa-173">You can experiment with different characteristics without affecting the published model.</span></span> <span data-ttu-id="f60fa-174">公開されたモデルは、**公開** を選択した場合にのみ影響を受けます。</span><span class="sxs-lookup"><span data-stu-id="f60fa-174">The published model is affected only when you select **Publish**.</span></span> <span data-ttu-id="f60fa-175">Dynamics 365 Finance のインスタンスには、1 つのモデルが使用されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f60fa-175">Remember that a single model is used for your instance of Dynamics 365 Finance.</span></span> <span data-ttu-id="f60fa-176">そのため、新しいモデルを公開する前に、そのモデルを慎重に確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f60fa-176">Therefore, you should carefully review any new model before you publish it.</span></span>

## <a name="for-more-information"></a><span data-ttu-id="f60fa-177">詳細情報</span><span class="sxs-lookup"><span data-stu-id="f60fa-177">For more information</span></span>

<span data-ttu-id="f60fa-178">予測モデルの評価方法の詳細については、[機械学習モデルの結果](/confusion-matrix.md)</span><span class="sxs-lookup"><span data-stu-id="f60fa-178">For more information about how to evaluate prediction models, [Results of machine learning models](/confusion-matrix.md)</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
