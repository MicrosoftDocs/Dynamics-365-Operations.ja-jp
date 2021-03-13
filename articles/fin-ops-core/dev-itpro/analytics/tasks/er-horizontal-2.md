---
title: ER 水平に拡張された範囲を使用して Excel のレポートに列を動的に追加する (第 2 部 - 形式の実行)
description: このトピックでは、OPENXML ワークシート (Excel) ファイルとしてレポートを生成するように電子申告 (ER) 形式を構成する方法について説明します。 (第 2 部)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c13179f424d570b23615fe81ca5ddfb7afed582d
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093479"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-2---run-format"></a><span data-ttu-id="809e5-104">ER 水平に拡張された範囲を使用して Excel のレポートに列を動的に追加する (第 2 部 - 形式の実行)</span><span class="sxs-lookup"><span data-stu-id="809e5-104">ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 2 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="809e5-105">次の手順は、システム管理者または電子レポートのロールに割り当てられたユーザーが、 OPENXML ワークシート (Excel) ファイル（要求された列が水平に展開される範囲として動的に作成される）としてのレポートを生成する電子レポート（ER）フォーマットをどのように設定するのか説明します。</span><span class="sxs-lookup"><span data-stu-id="809e5-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="809e5-106">これらのステップは DEMF 会社で実行できます。</span><span class="sxs-lookup"><span data-stu-id="809e5-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="809e5-107">これらの手順を完了するには、まず 「ER 水平方向に拡張可能な範囲を使用して、Excelレポートで列を動的に追加する（パート1：デザイン フォーマット）」に記載の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="809e5-107">To complete these steps, you must first complete the steps in the "ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1: Design format)" procedure.</span></span>

<span data-ttu-id="809e5-108">この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="809e5-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="find-created-format"></a><span data-ttu-id="809e5-109">作成されたフォーマットを検索する</span><span class="sxs-lookup"><span data-stu-id="809e5-109">Find created format</span></span>
1. <span data-ttu-id="809e5-110">[組織管理] > [電子申告] > [コンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="809e5-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="809e5-111">[ツリー] フィールドで、「Financial dimensions sample model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="809e5-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="809e5-112">ツリーで、「Financial dimensions sample model\Sample report with horizontally expandable ranges」を選択します。</span><span class="sxs-lookup"><span data-stu-id="809e5-112">In the tree, select 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.</span></span>

## <a name="execute-format-to-create-excel-output"></a><span data-ttu-id="809e5-113">フォーマットを実行してExcel出力を作成する</span><span class="sxs-lookup"><span data-stu-id="809e5-113">Execute format to create Excel output</span></span>
1. <span data-ttu-id="809e5-114">[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="809e5-114">Click Run.</span></span>
2. <span data-ttu-id="809e5-115">[分析コード名] フィールドに、「事業単位、コストセンター、部門」を入力します。</span><span class="sxs-lookup"><span data-stu-id="809e5-115">In the Dimension name field, type 'BusinessUnit;CostCenter;Department'.</span></span>
    * <span data-ttu-id="809e5-116">[分析コード名] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="809e5-116">In the Dimension name field, enter or select a value.</span></span>  <span data-ttu-id="809e5-117">現在の会社のすべての分析コードを選択するには、次を入力します: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="809e5-117">To select all dimensions for the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
3. <span data-ttu-id="809e5-118">[対象に含めるレコード] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="809e5-118">Expand the Records to include section.</span></span>
4. <span data-ttu-id="809e5-119">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="809e5-119">Click Filter.</span></span>
5. <span data-ttu-id="809e5-120">仕訳元帳表および仕訳バッチ番号フィールドの行を選択します。</span><span class="sxs-lookup"><span data-stu-id="809e5-120">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
6. <span data-ttu-id="809e5-121">[基準] フィールドに、「00057..00058」と入力します。</span><span class="sxs-lookup"><span data-stu-id="809e5-121">In the Criteria field, type '00057..00058'.</span></span>
    * <span data-ttu-id="809e5-122">00057..00058</span><span class="sxs-lookup"><span data-stu-id="809e5-122">00057..00058</span></span>  
7. <span data-ttu-id="809e5-123">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="809e5-123">Click OK.</span></span>
8. <span data-ttu-id="809e5-124">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="809e5-124">Click OK.</span></span>
    * <span data-ttu-id="809e5-125">生成された出荷を確認します。</span><span class="sxs-lookup"><span data-stu-id="809e5-125">Review the generated output.</span></span> <span data-ttu-id="809e5-126">新しく作成したExcel ファイルには、財務分析コードに対して選択された同じ数の列が含まれることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="809e5-126">Note that the newly created Excel file contains the same number of columns that were selected for financial dimensions.</span></span> <span data-ttu-id="809e5-127">これらの列のレポート ヘッダーは財務分析コードの名称を表します。</span><span class="sxs-lookup"><span data-stu-id="809e5-127">The report header in those columns represents financial dimensions' names.</span></span> <span data-ttu-id="809e5-128">これらの列のトランザクションの明細行は財務分析コードを表します。</span><span class="sxs-lookup"><span data-stu-id="809e5-128">The transactions' lines in those columns represent financial dimensions.</span></span> <span data-ttu-id="809e5-129">このレポートを実行して、レポートが選択した分析コード数またはインスタンスに構成した分析コード数に依存していないことを確認するために異なる分析コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="809e5-129">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  

