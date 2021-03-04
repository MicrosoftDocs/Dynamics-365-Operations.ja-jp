---
title: Lifecycle Services (LCS) 内のカスタマイズ分析
description: カスタマイズ分析は、モデル ファイルをベスト プラクティス ルールに従って検証する Microsoft Dynamics AX 2012 の自動ツールです。
author: RobinARH
manager: AnnBe
ms.date: 11/13/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 19021
ms.assetid: 409386b2-98c8-44a7-be6f-252f8a21f819
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: e1a9d92d3c3915fd8c874f576b0438591aaa525b
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5129321"
---
# <a name="customization-analysis-in-lifecycle-services-lcs"></a><span data-ttu-id="dcef1-103">Lifecycle Services (LCS) 内のカスタマイズ分析</span><span class="sxs-lookup"><span data-stu-id="dcef1-103">Customization analysis in Lifecycle Services (LCS)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dcef1-104">Microsoft Dynamics Lifecycle Services では、カスタマイズ分析がテーブル、クラス、フォーム、および列挙の Microsoft Dynamics AX のベスト プラクティス ルールに対して顧客のモデル ファイルを検証する自動ツールを Microsoft Dynamics AX 2012 の顧客に提供します。</span><span class="sxs-lookup"><span data-stu-id="dcef1-104">In Microsoft Dynamics Lifecycle Services, Customization analysis offers Microsoft Dynamics AX 2012 customers an automated tool that validates the customer’s model files against Microsoft Dynamics AX best-practice rules for tables, classes, forms, and enums.</span></span> <span data-ttu-id="dcef1-105">その後、サイトでの概要レポートの表示、すべての問題を一覧表示する詳細な Microsoft Excel レポート、開発者が Microsoft Dynamics AX の開発環境で読み込むことができる開発者レポートを含んだレポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="dcef1-105">It then generates reports, including a summary report display on the site, a detailed Microsoft Excel report that lists all issues, and a developer report that the developer can load in the Microsoft Dynamics AX development environment.</span></span> 

<a name="prerequisites"></a><span data-ttu-id="dcef1-106">必要条件</span><span class="sxs-lookup"><span data-stu-id="dcef1-106">Prerequisites</span></span>
-------------

<span data-ttu-id="dcef1-107">Microsoft Dynamics AX 2012 モデル ファイルの分析を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="dcef1-107">You must have Microsoft Dynamics AX 2012 model files to be analyzed.</span></span> <span data-ttu-id="dcef1-108">モデル ファイルの詳細については、「[方法: モデルのエクスポートおよびインポート](https://msdn.microsoft.com/library/c2449a03-7574-4b9d-8518-9005b560209f(AX.60).aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dcef1-108">For more information about model files, see [How to: Export and Import a Model](https://msdn.microsoft.com/library/c2449a03-7574-4b9d-8518-9005b560209f(AX.60).aspx).</span></span>

## <a name="getting-started"></a><span data-ttu-id="dcef1-109">はじめに</span><span class="sxs-lookup"><span data-stu-id="dcef1-109">Getting started</span></span>
<span data-ttu-id="dcef1-110">カスタマイズ分析を使用するには、モデル ファイルをアップロードし、レポートを評価して、どのように変更するかを判断する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dcef1-110">To use Customization analysis, you must upload model files and then evaluate the reports to determine what changes you want to make.</span></span>

### <a name="upload-model-files"></a><span data-ttu-id="dcef1-111">モデル ファイルのアップロード</span><span class="sxs-lookup"><span data-stu-id="dcef1-111">Upload model files</span></span>

1.  <span data-ttu-id="dcef1-112">[Lifecycle Services に移動](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="dcef1-112">[Go to Lifecycle Services](https://lcs.dynamics.com).</span></span>
2.  <span data-ttu-id="dcef1-113">プロジェクトを開いて、**カスタマイズ分析** タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="dcef1-113">Open a project, and then click the **Customization analysis** tile.</span></span>
3.  <span data-ttu-id="dcef1-114">**追加** をクリックし、**カスタマイズ分析: ジョブを作成** ページで、名前、適切なバージョンの Microsoft Dynamics AX、および適切なビルドを入力します。</span><span class="sxs-lookup"><span data-stu-id="dcef1-114">Click **Add**, and then, on the **Customization analysis: Create job** page, enter a name, the appropriate version of Microsoft Dynamics AX, and the appropriate build.</span></span>
4.  <span data-ttu-id="dcef1-115">**作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dcef1-115">Click **Create**.</span></span>
5.  <span data-ttu-id="dcef1-116">**ファイルの追加** をクリックして分析するモデルを参照し、**アップロード** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dcef1-116">Click **Add files**, browse to the model that you want to analyze, and click **Upload**.</span></span> <span data-ttu-id="dcef1-117">分析のために複数のモデル ファイルをアップロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="dcef1-117">You can upload multiple model files to analyze.</span></span>
6.  <span data-ttu-id="dcef1-118">**コードの分析** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dcef1-118">Click **Analyze Code**.</span></span> <span data-ttu-id="dcef1-119">サイトがファイルを処理し、レポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="dcef1-119">The site processes the files, and then generates reports.</span></span> <span data-ttu-id="dcef1-120">処理中に、ステータス インジケーターは更新します。</span><span class="sxs-lookup"><span data-stu-id="dcef1-120">During processing, status indicators update.</span></span> <span data-ttu-id="dcef1-121">**注記:** 処理が続行されている間、ページを離れることができます。</span><span class="sxs-lookup"><span data-stu-id="dcef1-121">**Note:** You can leave the page while processing continues.</span></span> <span data-ttu-id="dcef1-122">処理には 10 分以上かかることがあります。</span><span class="sxs-lookup"><span data-stu-id="dcef1-122">Processing may take 10 minutes or longer.</span></span>

### <a name="evaluate-reports"></a><span data-ttu-id="dcef1-123">レポートの評価</span><span class="sxs-lookup"><span data-stu-id="dcef1-123">Evaluate reports</span></span>

<span data-ttu-id="dcef1-124">カスタマイズ分析は、テーブル、クラス、フォーム、および列挙の Microsoft Dynamics AX のベスト プラクティス ルールに照らして、モデル ファイルを検証します。</span><span class="sxs-lookup"><span data-stu-id="dcef1-124">Customization analysis checks your model files against the Microsoft Dynamics AX best-practice rules for tables, classes, forms, and enums.</span></span> <span data-ttu-id="dcef1-125">その後、コードがこれらのルールから逸脱するインスタンスの詳細なレポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="dcef1-125">It then generates detailed reports of instances where your code deviates from those rules.</span></span> <span data-ttu-id="dcef1-126">処理が完了したら、レビューするレポートを選択できます。</span><span class="sxs-lookup"><span data-stu-id="dcef1-126">After processing is complete, you can select the reports that you would like to review.</span></span> <span data-ttu-id="dcef1-127">カスタマイズの分析には、次のレポート タイプが用意されています。</span><span class="sxs-lookup"><span data-stu-id="dcef1-127">Customization analysis provides the following types of reports:</span></span>

1.  <span data-ttu-id="dcef1-128">ブラウザー内で表示できる HTML カスタマイズ分析のレポートです。</span><span class="sxs-lookup"><span data-stu-id="dcef1-128">An HTML Customization Analysis report that you can view in a browser.</span></span>
2.  <span data-ttu-id="dcef1-129">Excel ファイルを使用して生成されたエラーを確認できます。</span><span class="sxs-lookup"><span data-stu-id="dcef1-129">An Excel file that you can use to review the errors that are generated.</span></span> <span data-ttu-id="dcef1-130">このレポートを表示するには、**表示** をクリックし、ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="dcef1-130">To view this report, click **View**, and then open the file.</span></span>
3.  <span data-ttu-id="dcef1-131">HTML 開発者レポート。Microsoft Dynamics AX の開発者環境で開くことができます。</span><span class="sxs-lookup"><span data-stu-id="dcef1-131">An HTML developer report that you can open in a Microsoft Dynamics AX developer environment.</span></span> <span data-ttu-id="dcef1-132">Microsoft Dynamics AX 開発環境でこのレポートを表示するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="dcef1-132">To view this report in the Microsoft Dynamics AX development environment, perform the following steps:</span></span>
    1.  <span data-ttu-id="dcef1-133">**表示** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dcef1-133">Click **View**.</span></span> <span data-ttu-id="dcef1-134">ファイルはブラウザー ウィンドウで開きます。</span><span class="sxs-lookup"><span data-stu-id="dcef1-134">The file will open in a browser window.</span></span>
    2.  <span data-ttu-id="dcef1-135">開発環境のコンピューターにレポートを保存します。</span><span class="sxs-lookup"><span data-stu-id="dcef1-135">Save the report to a computer in your development environment.</span></span>
    3.  <span data-ttu-id="dcef1-136">**コンパイラ出力** ウィンドウで、**インポート** をクリックし、ファイルを選択して開きます。</span><span class="sxs-lookup"><span data-stu-id="dcef1-136">In the **Compiler output** window, click **Import**, and select the file to open it.</span></span>
    4.  <span data-ttu-id="dcef1-137">レポート内で任意の行をダブルクリックして、報告された問題を含むオブジェクトおよび行を開くことができます。</span><span class="sxs-lookup"><span data-stu-id="dcef1-137">You can double-click any line within the report to open the object and line with the reported issue.</span></span>

### <a name="remove-a-customization-job"></a><span data-ttu-id="dcef1-138">カスタマイズ ジョブの削除</span><span class="sxs-lookup"><span data-stu-id="dcef1-138">Remove a customization job</span></span>

<span data-ttu-id="dcef1-139">プロジェクトのカスタマイズ一覧からジョブを削除するには、ジョブ名の上にカーソルを置き、左側のボックスをクリックして **削除** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="dcef1-139">To remove a job from the list of customizations for a project, hover over the job name, then click the box to the left, and click the **Remove** button.</span></span>

<a name="additional-resources"></a><span data-ttu-id="dcef1-140">追加リソース</span><span class="sxs-lookup"><span data-stu-id="dcef1-140">Additional resources</span></span>
--------

<span data-ttu-id="dcef1-141">[Microsoft Dynamics AX 開発のベスト プラクティス](https://msdn.microsoft.com/library/833e44ff-d89a-459a-84be-0cc5da57ee90(AX.60).aspx)</span><span class="sxs-lookup"><span data-stu-id="dcef1-141">[Best Practices for Microsoft Dynamics AX Development](https://msdn.microsoft.com/library/833e44ff-d89a-459a-84be-0cc5da57ee90(AX.60).aspx)</span></span>



