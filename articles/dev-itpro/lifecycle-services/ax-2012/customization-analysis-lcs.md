---
title: Lifecycle Services (LCS) 内のカスタマイズ分析
description: Microsoft Dynamics Lifecycle Services では、カスタマイズ分析がテーブル、クラス、フォーム、および列挙の Microsoft Dynamics AX のベスト プラクティス ルールに対して顧客のモデル ファイルを検証する自動ツールを Microsoft Dynamics AX 2012 の顧客に提供します。 その後、サイトでの概要レポートの表示、すべての問題を一覧表示する詳細な Microsoft Excel レポート、開発者が Microsoft Dynamics AX の開発環境で読み込むことができる開発者レポートを含んだレポートを生成します。
author: RobinARH
manager: AnnBe
ms.date: 11/13/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 19021
ms.assetid: 409386b2-98c8-44a7-be6f-252f8a21f819
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 9bd15953d0f024a8df5959837ff3b39534eba1a9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369790"
---
# <a name="customization-analysis-in-lifecycle-services-lcs"></a><span data-ttu-id="9e56d-104">Lifecycle Services (LCS) 内のカスタマイズ分析</span><span class="sxs-lookup"><span data-stu-id="9e56d-104">Customization analysis in Lifecycle Services (LCS)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9e56d-105">Microsoft Dynamics Lifecycle Services では、カスタマイズ分析がテーブル、クラス、フォーム、および列挙の Microsoft Dynamics AX のベスト プラクティス ルールに対して顧客のモデル ファイルを検証する自動ツールを Microsoft Dynamics AX 2012 の顧客に提供します。</span><span class="sxs-lookup"><span data-stu-id="9e56d-105">In Microsoft Dynamics Lifecycle Services, Customization analysis offers Microsoft Dynamics AX 2012 customers an automated tool that validates the customer’s model files against Microsoft Dynamics AX best-practice rules for tables, classes, forms, and enums.</span></span> <span data-ttu-id="9e56d-106">その後、サイトでの概要レポートの表示、すべての問題を一覧表示する詳細な Microsoft Excel レポート、開発者が Microsoft Dynamics AX の開発環境で読み込むことができる開発者レポートを含んだレポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="9e56d-106">It then generates reports, including a summary report display on the site, a detailed Microsoft Excel report that lists all issues, and a developer report that the developer can load in the Microsoft Dynamics AX development environment.</span></span> 

<a name="prerequisites"></a><span data-ttu-id="9e56d-107">必要条件</span><span class="sxs-lookup"><span data-stu-id="9e56d-107">Prerequisites</span></span>
-------------

<span data-ttu-id="9e56d-108">Microsoft Dynamics AX 2012 モデル ファイルの分析を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e56d-108">You must have Microsoft Dynamics AX 2012 model files to be analyzed.</span></span> <span data-ttu-id="9e56d-109">モデル ファイルの詳細については、「[方法: モデルのエクスポートおよびインポート](http://msdn.microsoft.com/library/c2449a03-7574-4b9d-8518-9005b560209f(AX.60).aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9e56d-109">For more information about model files, see [How to: Export and Import a Model](http://msdn.microsoft.com/library/c2449a03-7574-4b9d-8518-9005b560209f(AX.60).aspx).</span></span>

## <a name="getting-started"></a><span data-ttu-id="9e56d-110">はじめに</span><span class="sxs-lookup"><span data-stu-id="9e56d-110">Getting started</span></span>
<span data-ttu-id="9e56d-111">カスタマイズ分析を使用するには、モデル ファイルをアップロードし、レポートを評価して、どのように変更するかを判断する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e56d-111">To use Customization analysis, you must upload model files and then evaluate the reports to determine what changes you want to make.</span></span>

### <a name="upload-model-files"></a><span data-ttu-id="9e56d-112">モデル ファイルのアップロード</span><span class="sxs-lookup"><span data-stu-id="9e56d-112">Upload model files</span></span>

1.  <span data-ttu-id="9e56d-113">[Lifecycle Services に移動](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="9e56d-113">[Go to Lifecycle Services](https://lcs.dynamics.com).</span></span>
2.  <span data-ttu-id="9e56d-114">プロジェクトを開いて、**カスタマイズ分析**タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e56d-114">Open a project, and then click the **Customization analysis** tile.</span></span>
3.  <span data-ttu-id="9e56d-115">**追加**をクリックし、**カスタマイズ分析: ジョブを作成**ページで、名前、適切なバージョンの Microsoft Dynamics AX、および適切なビルドを入力します。</span><span class="sxs-lookup"><span data-stu-id="9e56d-115">Click **Add**, and then, on the **Customization analysis: Create job** page, enter a name, the appropriate version of Microsoft Dynamics AX, and the appropriate build.</span></span>
4.  <span data-ttu-id="9e56d-116">**作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e56d-116">Click **Create**.</span></span>
5.  <span data-ttu-id="9e56d-117">**ファイルの追加**をクリックして分析するモデルを参照し、**アップロード**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e56d-117">Click **Add files**, browse to the model that you want to analyze, and click **Upload**.</span></span> <span data-ttu-id="9e56d-118">分析のために複数のモデル ファイルをアップロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="9e56d-118">You can upload multiple model files to analyze.</span></span>
6.  <span data-ttu-id="9e56d-119">**コードの分析**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e56d-119">Click **Analyze Code**.</span></span> <span data-ttu-id="9e56d-120">サイトがファイルを処理し、レポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="9e56d-120">The site processes the files, and then generates reports.</span></span> <span data-ttu-id="9e56d-121">処理中に、ステータス インジケーターは更新します。</span><span class="sxs-lookup"><span data-stu-id="9e56d-121">During processing, status indicators update.</span></span> <span data-ttu-id="9e56d-122">**注記:** 処理が続行されている間、ページを離れることができます。</span><span class="sxs-lookup"><span data-stu-id="9e56d-122">**Note:** You can leave the page while processing continues.</span></span> <span data-ttu-id="9e56d-123">処理には 10 分以上かかることがあります。</span><span class="sxs-lookup"><span data-stu-id="9e56d-123">Processing may take 10 minutes or longer.</span></span>

### <a name="evaluate-reports"></a><span data-ttu-id="9e56d-124">レポートの評価</span><span class="sxs-lookup"><span data-stu-id="9e56d-124">Evaluate reports</span></span>

<span data-ttu-id="9e56d-125">カスタマイズ分析は、テーブル、クラス、フォーム、および列挙の Microsoft Dynamics AX のベスト プラクティス ルールに照らして、モデル ファイルを検証します。</span><span class="sxs-lookup"><span data-stu-id="9e56d-125">Customization analysis checks your model files against the Microsoft Dynamics AX best-practice rules for tables, classes, forms, and enums.</span></span> <span data-ttu-id="9e56d-126">その後、コードがこれらのルールから逸脱するインスタンスの詳細なレポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="9e56d-126">It then generates detailed reports of instances where your code deviates from those rules.</span></span> <span data-ttu-id="9e56d-127">処理が完了したら、レビューするレポートを選択できます。</span><span class="sxs-lookup"><span data-stu-id="9e56d-127">After processing is complete, you can select the reports that you would like to review.</span></span> <span data-ttu-id="9e56d-128">カスタマイズの分析には、次のレポート タイプが用意されています。</span><span class="sxs-lookup"><span data-stu-id="9e56d-128">Customization analysis provides the following types of reports:</span></span>

1.  <span data-ttu-id="9e56d-129">ブラウザー内で表示できる HTML カスタマイズ分析のレポートです。</span><span class="sxs-lookup"><span data-stu-id="9e56d-129">An HTML Customization Analysis report that you can view in a browser.</span></span>
2.  <span data-ttu-id="9e56d-130">Excel ファイルを使用して生成されたエラーを確認できます。</span><span class="sxs-lookup"><span data-stu-id="9e56d-130">An Excel file that you can use to review the errors that are generated.</span></span> <span data-ttu-id="9e56d-131">このレポートを表示するには、**表示** をクリックし、ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="9e56d-131">To view this report, click **View**, and then open the file.</span></span>
3.  <span data-ttu-id="9e56d-132">HTML 開発者レポート。Microsoft Dynamics AX の開発者環境で開くことができます。</span><span class="sxs-lookup"><span data-stu-id="9e56d-132">An HTML developer report that you can open in a Microsoft Dynamics AX developer environment.</span></span> <span data-ttu-id="9e56d-133">Microsoft Dynamics AX 開発環境でこのレポートを表示するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="9e56d-133">To view this report in the Microsoft Dynamics AX development environment, perform the following steps:</span></span>
    1.  <span data-ttu-id="9e56d-134">**表示**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e56d-134">Click **View**.</span></span> <span data-ttu-id="9e56d-135">ファイルはブラウザー ウィンドウで開きます。</span><span class="sxs-lookup"><span data-stu-id="9e56d-135">The file will open in a browser window.</span></span>
    2.  <span data-ttu-id="9e56d-136">開発環境のコンピューターにレポートを保存します。</span><span class="sxs-lookup"><span data-stu-id="9e56d-136">Save the report to a computer in your development environment.</span></span>
    3.  <span data-ttu-id="9e56d-137">**コンパイラ出力**ウィンドウで、**インポート**をクリックし、ファイルを選択して開きます。</span><span class="sxs-lookup"><span data-stu-id="9e56d-137">In the **Compiler output** window, click **Import**, and select the file to open it.</span></span>
    4.  <span data-ttu-id="9e56d-138">レポート内で任意の行をダブルクリックして、報告された問題を含むオブジェクトおよび行を開くことができます。</span><span class="sxs-lookup"><span data-stu-id="9e56d-138">You can double-click any line within the report to open the object and line with the reported issue.</span></span>

### <a name="remove-a-customization-job"></a><span data-ttu-id="9e56d-139">カスタマイズ ジョブの削除</span><span class="sxs-lookup"><span data-stu-id="9e56d-139">Remove a customization job</span></span>

<span data-ttu-id="9e56d-140">プロジェクトのカスタマイズ一覧からジョブを削除するには、ジョブ名の上にカーソルを置き、左側のボックスをクリックして **削除** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e56d-140">To remove a job from the list of customizations for a project, hover over the job name, then click the box to the left, and click the **Remove** button.</span></span>

<a name="additional-resources"></a><span data-ttu-id="9e56d-141">追加リソース</span><span class="sxs-lookup"><span data-stu-id="9e56d-141">Additional resources</span></span>
--------

<span data-ttu-id="9e56d-142">[Microsoft Dynamics AX 開発のベスト プラクティス](http://msdn.microsoft.com/library/833e44ff-d89a-459a-84be-0cc5da57ee90(AX.60).aspx)</span><span class="sxs-lookup"><span data-stu-id="9e56d-142">[Best Practices for Microsoft Dynamics AX Development](http://msdn.microsoft.com/library/833e44ff-d89a-459a-84be-0cc5da57ee90(AX.60).aspx)</span></span>



