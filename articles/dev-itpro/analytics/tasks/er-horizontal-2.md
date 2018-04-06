--- 
title: "水平に拡張された範囲を使用して電子申告 (ER) の Excel のレポートに列を動的に追加するための形式の実行"
description: "次の手順は、システム管理者または電子レポートのロールに割り当てられたユーザーが、 OPENXML ワークシート (Excel) ファイル（要求された列が水平に展開される範囲として動的に作成される）としてのレポートを生成する電子レポート（ER）フォーマットをどのように設定するのか説明します。"
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 3ca72ab5c7ac15f3a788ea457a360d93a0b505b0
ms.contentlocale: ja-jp
ms.lasthandoff: 03/26/2018

---
# <a name="run-a-format-that-uses-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-for-electronic-reporting-er"></a><span data-ttu-id="f0c67-103">水平に拡張された範囲を使用して電子申告 (ER) の Excel のレポートに列を動的に追加するための形式の実行</span><span class="sxs-lookup"><span data-stu-id="f0c67-103">Run a format that uses horizontally-expandable ranges to dynamically add columns in Excel reports for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f0c67-104">次の手順は、システム管理者または電子レポートのロールに割り当てられたユーザーが、 OPENXML ワークシート (Excel) ファイル（要求された列が水平に展開される範囲として動的に作成される）としてのレポートを生成する電子レポート（ER）フォーマットをどのように設定するのか説明します。</span><span class="sxs-lookup"><span data-stu-id="f0c67-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="f0c67-105">これらのステップは DEMF 会社で実行できます。</span><span class="sxs-lookup"><span data-stu-id="f0c67-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="f0c67-106">これらの手順を完了するには、まず「水平に展開可能な範囲をER 使用してExcelレポートに動的に列を加える (パート1: デザインフォーマット」の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f0c67-106">To complete these steps, you must first complete the steps in the “ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1: Design format)” procedure.</span></span>

<span data-ttu-id="f0c67-107">この手順は、Dynamics 365 for Operations、バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="f0c67-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="find-created-format"></a><span data-ttu-id="f0c67-108">作成されたフォーマットを検索する</span><span class="sxs-lookup"><span data-stu-id="f0c67-108">Find created format</span></span>
1. <span data-ttu-id="f0c67-109">[組織管理] > [電子申告] > [コンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="f0c67-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="f0c67-110">[ツリー] フィールドで、「Financial dimensions sample model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="f0c67-110">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="f0c67-111">ツリーで、「Financial dimensions sample model\Sample report with horizontally expandable ranges」を選択します。</span><span class="sxs-lookup"><span data-stu-id="f0c67-111">In the tree, select 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.</span></span>

## <a name="execute-format-to-create-excel-output"></a><span data-ttu-id="f0c67-112">フォーマットを実行してExcel出力を作成する</span><span class="sxs-lookup"><span data-stu-id="f0c67-112">Execute format to create Excel output</span></span>
1. <span data-ttu-id="f0c67-113">[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f0c67-113">Click Run.</span></span>
2. <span data-ttu-id="f0c67-114">[分析コード名] フィールドに、「事業単位、コストセンター、部門」を入力します。</span><span class="sxs-lookup"><span data-stu-id="f0c67-114">In the Dimension name field, type 'BusinessUnit;CostCenter;Department'.</span></span>
    * <span data-ttu-id="f0c67-115">[分析コード名] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="f0c67-115">In the Dimension name field, enter or select a value.</span></span>  <span data-ttu-id="f0c67-116">現在の会社のすべての分析コードを選択するには、次を入力します: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="f0c67-116">To select all dimensions for the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
3. <span data-ttu-id="f0c67-117">[対象に含めるレコード] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="f0c67-117">Expand the Records to include section.</span></span>
4. <span data-ttu-id="f0c67-118">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f0c67-118">Click Filter.</span></span>
5. <span data-ttu-id="f0c67-119">仕訳元帳表および仕訳バッチ番号フィールドの行を選択します。</span><span class="sxs-lookup"><span data-stu-id="f0c67-119">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
6. <span data-ttu-id="f0c67-120">[基準] フィールドに、「00057..00058」と入力します。</span><span class="sxs-lookup"><span data-stu-id="f0c67-120">In the Criteria field, type '00057..00058'.</span></span>
    * <span data-ttu-id="f0c67-121">00057..00058</span><span class="sxs-lookup"><span data-stu-id="f0c67-121">00057..00058</span></span>  
7. <span data-ttu-id="f0c67-122">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f0c67-122">Click OK.</span></span>
8. <span data-ttu-id="f0c67-123">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f0c67-123">Click OK.</span></span>
    * <span data-ttu-id="f0c67-124">生成された出荷を確認します。</span><span class="sxs-lookup"><span data-stu-id="f0c67-124">Review the generated output.</span></span> <span data-ttu-id="f0c67-125">新しく作成したExcel ファイルには、財務分析コードに対して選択された同じ数の列が含まれることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f0c67-125">Note that the newly created Excel file contains the same number of columns that were selected for financial dimensions.</span></span> <span data-ttu-id="f0c67-126">これらの列のレポートヘッダーは財務分析コードの名称を表します。</span><span class="sxs-lookup"><span data-stu-id="f0c67-126">The report header in those columns represents financial dimensions’ names.</span></span> <span data-ttu-id="f0c67-127">これらの列のトランザクションの明細行は財務分析コードを表します。</span><span class="sxs-lookup"><span data-stu-id="f0c67-127">The transactions’ lines in those columns represent financial dimensions.</span></span> <span data-ttu-id="f0c67-128">このレポートを実行し異なる分析コードを選択して、レポートが選択した分析コードの数または Dynamics 365 for Finance and Operations インスタンスに構成した分析コードの数に依存していないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="f0c67-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations instance.</span></span>  


