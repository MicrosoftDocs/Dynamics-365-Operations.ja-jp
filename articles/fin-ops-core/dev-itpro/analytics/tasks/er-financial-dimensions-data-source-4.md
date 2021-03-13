---
title: ER 財務分析コードをデータ ソースとして使用する (第 4 部 - レポートの実行)
description: このトピックでは、財務分析コードを ER レポートのデータ ソースとして使用するために、電子申告 (ER) モデルを構成する方法について説明します。 (第 4 部)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
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
ms.openlocfilehash: c1fe332de84339d3369ba495ca13f50c4901f366
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092278"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a><span data-ttu-id="11266-104">ER 財務分析コードをデータ ソースとして使用する (第 4 部 - レポートの実行)</span><span class="sxs-lookup"><span data-stu-id="11266-104">ER Use financial dimensions as a data source (Part 4 - Run the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="11266-105">次の手順では、システム管理者に指定されたユーザーまたは電子レポート開発者のロールが、電子レポート・データソースとしての財務分析コードを使用するために 電子レポート（ER）モデルをどのように環境設定しているのか説明します。</span><span class="sxs-lookup"><span data-stu-id="11266-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="11266-106">これらのステップは DEMF 会社で実行できます。</span><span class="sxs-lookup"><span data-stu-id="11266-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="11266-107">この手順を実施するには、まず「ER 財務分析コードをデータソースとして使用する（パート 3：レポートのデザイン）」に記載の手順を実施する必要があります。</span><span class="sxs-lookup"><span data-stu-id="11266-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 3: Design the report)" procedure.</span></span> <span data-ttu-id="11266-108">また、電子レポート パラメーターのページで既定のドキュメント タイプを環境設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="11266-108">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="11266-109">既定のドキュメントタイプは、ERのコンフィギュレーションがダウンロード、インポートされるときにも設定されます。</span><span class="sxs-lookup"><span data-stu-id="11266-109">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="11266-110">レポートを実行する</span><span class="sxs-lookup"><span data-stu-id="11266-110">Run report</span></span>
1. <span data-ttu-id="11266-111">[組織管理] > [電子申告] > [コンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="11266-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="11266-112">[ツリー] フィールドで、「Financial dimensions sample model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="11266-112">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="11266-113">ツリーで、「Financial dimensions sample model\Ledger journal report」を選択します。</span><span class="sxs-lookup"><span data-stu-id="11266-113">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="11266-114">[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="11266-114">Click Run.</span></span>
<span data-ttu-id="11266-115">![ER コンフィギュレーション ページ](../media/er-financial-dimensions-guides-run1.png)</span><span class="sxs-lookup"><span data-stu-id="11266-115">![ER configurations page](../media/er-financial-dimensions-guides-run1.png)</span></span>
5. <span data-ttu-id="11266-116">[分析コード名] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="11266-116">In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="11266-117">現在の会社のすべての分析コードを選択するには、次の情報を入力します: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="11266-117">To select all dimensions in the current company, enter the following information:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
![ER コンフィギュレーション ページ](../media/er-financial-dimensions-guides-run2.png)
6. <span data-ttu-id="11266-119">[対象に含めるレコード] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="11266-119">Expand the Records to include section.</span></span>
7. <span data-ttu-id="11266-120">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="11266-120">Click Filter.</span></span>
8. <span data-ttu-id="11266-121">仕訳元帳表および仕訳バッチ番号フィールドの行を選択します。</span><span class="sxs-lookup"><span data-stu-id="11266-121">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="11266-122">[基準] フィールドで、「00057」と入力します。</span><span class="sxs-lookup"><span data-stu-id="11266-122">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="11266-123">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="11266-123">Click OK.</span></span>
11. <span data-ttu-id="11266-124">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="11266-124">Click OK.</span></span>
<span data-ttu-id="11266-125">![ER コンフィギュレーション ページ](../media/er-financial-dimensions-guides-run3.png)</span><span class="sxs-lookup"><span data-stu-id="11266-125">![ER configurations page](../media/er-financial-dimensions-guides-run3.png)</span></span>
    * <span data-ttu-id="11266-126">生成された出荷を確認します。</span><span class="sxs-lookup"><span data-stu-id="11266-126">Review the generated output.</span></span> <span data-ttu-id="11266-127">選択したバッチの各トランザクションについては、対応する分析コードの財務分析コードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="11266-127">For each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="11266-128">このレポートを実行して、レポートが選択した分析コード数またはインスタンスに構成した分析コード数に依存していないことを確認するために異なる分析コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="11266-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  
![ER コンフィギュレーション ページ](../media/er-financial-dimensions-guides-run4.png)
