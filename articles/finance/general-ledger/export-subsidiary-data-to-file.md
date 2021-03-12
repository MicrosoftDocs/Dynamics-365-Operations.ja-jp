---
title: 関連会社のデータをファイルへエクスポートする
description: このトピックでは、Microsoft Dynamics 365 Finance からデータをエクスポートして連結法人に取り込む準備について説明します。
author: jinniew
manager: AnnBe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 179a401178935b8a76d6718a7fb1f63e08344f50
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968682"
---
# <a name="export-subsidiary-data-to-files"></a><span data-ttu-id="c39df-103">関連会社のデータをファイルへエクスポートする</span><span class="sxs-lookup"><span data-stu-id="c39df-103">Export subsidiary data to files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c39df-104">**エクスポート** ページ (**システム管理 \> ワークスペース \> インポート/エクスポート**) を使用して、連結法人にインポート可能なファイルに子会社のデータをエクスポートする準備します。</span><span class="sxs-lookup"><span data-stu-id="c39df-104">You use the **Export** page (**System administration \> Workspaces \> Import/Export**) to prepare to export subsidiary data to files that can then be imported into a consolidated legal entity.</span></span> <span data-ttu-id="c39df-105">インポートとエクスポートのプロセスについての詳細情報は、[データのインポートとジョブのエクスポートの概要](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c39df-105">For more information about the import and export processes, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>

1. <span data-ttu-id="c39df-106">連結プロセスで使用する法人を作成する。</span><span class="sxs-lookup"><span data-stu-id="c39df-106">Create a legal entity for the consolidation process.</span></span> <span data-ttu-id="c39df-107">法人の作成方法の詳細については、[法人の作成](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c39df-107">For information about how to create legal entities, see [Create a legal entity](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md).</span></span> <span data-ttu-id="c39df-108">詳細については、[連結プロセスに使用する法人の準備](prepare-company-for-consolidation.md) と [連結用の子会社の設定](set-up-subsidiary-company-for-consolidation.md)を参照してください 。</span><span class="sxs-lookup"><span data-stu-id="c39df-108">For more information, see [Prepare a legal entity for use in the consolidation process](prepare-company-for-consolidation.md) and [Set up a subsidiary legal entity for consolidation](set-up-subsidiary-company-for-consolidation.md).</span></span> 

2. <span data-ttu-id="c39df-109">**連結 \> エクスポート 会社の 残高** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c39df-109">Go to **Consolidations \> Export company balances**.</span></span> <span data-ttu-id="c39df-110">**会社の残高のエクスポート** ページの **基準** タブで、次のフィールドを設定して連結の詳細を指定します。</span><span class="sxs-lookup"><span data-stu-id="c39df-110">On the **Export company balances** page, on the **Criteria** tab, specify the details of the consolidation by setting the following fields.</span></span>

    | <span data-ttu-id="c39df-111">フィールド</span><span class="sxs-lookup"><span data-stu-id="c39df-111">Field</span></span>                             | <span data-ttu-id="c39df-112">説明</span><span class="sxs-lookup"><span data-stu-id="c39df-112">Description</span></span> |
    |-----------------------------------|-------|
    | <span data-ttu-id="c39df-113">主勘定</span><span class="sxs-lookup"><span data-stu-id="c39df-113">Main account</span></span>                      | <span data-ttu-id="c39df-114">連結する勘定を指定します。</span><span class="sxs-lookup"><span data-stu-id="c39df-114">Specify the accounts to consolidate.</span></span> <span data-ttu-id="c39df-115">すべての勘定を含めるには、このフィールドを空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="c39df-115">To include all accounts, leave this field blank.</span></span> |
    | <span data-ttu-id="c39df-116">連結勘定を使用する</span><span class="sxs-lookup"><span data-stu-id="c39df-116">Use consolidation account</span></span>         | <span data-ttu-id="c39df-117">連結勘定を指定した場合は、このオプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="c39df-117">If you've specified consolidation accounts, set this option to **Yes**.</span></span> |
    | <span data-ttu-id="c39df-118">連結勘定の選択元</span><span class="sxs-lookup"><span data-stu-id="c39df-118">Select consolidation account from</span></span> | <span data-ttu-id="c39df-119">**主要勘定** または **連結勘定グループ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c39df-119">Select either **Main account** or **Consolidation account group**.</span></span> |
    | <span data-ttu-id="c39df-120">連結勘定グループ</span><span class="sxs-lookup"><span data-stu-id="c39df-120">Consolidation account group</span></span>       | <span data-ttu-id="c39df-121">選択した連結勘定デ使用する連結勘定グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="c39df-121">Select a consolidation account group for the consolidation account that you selected.</span></span> |
    | <span data-ttu-id="c39df-122">連結期間</span><span class="sxs-lookup"><span data-stu-id="c39df-122">Consolidation period</span></span>              | <span data-ttu-id="c39df-123">連結の "開始日" と "終了日" を指定します。</span><span class="sxs-lookup"><span data-stu-id="c39df-123">Specify "from" and "to" dates for the consolidation.</span></span> |
    | <span data-ttu-id="c39df-124">実績金額を含む</span><span class="sxs-lookup"><span data-stu-id="c39df-124">Include actual amounts</span></span>            | <span data-ttu-id="c39df-125">実際の金額を含める場合は、このオプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="c39df-125">Set this option to **Yes** to include actual amounts.</span></span> |
    | <span data-ttu-id="c39df-126">予算金額を含む</span><span class="sxs-lookup"><span data-stu-id="c39df-126">Include budget amounts</span></span>            | <span data-ttu-id="c39df-127">このオプションを **はい** に設定し、連結に予算額を含めます。</span><span class="sxs-lookup"><span data-stu-id="c39df-127">Set this option to **Yes** to include budget amounts in consolidations.</span></span> |
    | <span data-ttu-id="c39df-128">予算モデル</span><span class="sxs-lookup"><span data-stu-id="c39df-128">Budget models</span></span>                     | <span data-ttu-id="c39df-129">含める予算モデルを指定します。</span><span class="sxs-lookup"><span data-stu-id="c39df-129">Specify the budget model to include.</span></span> |

3. <span data-ttu-id="c39df-130">**財務分析コード** タブで、連結の詳細を指定します。</span><span class="sxs-lookup"><span data-stu-id="c39df-130">On the **Financial dimensions** tab, specify the details of the consolidation:</span></span>

    - <span data-ttu-id="c39df-131">子会社勘定の取引から連結法人の取引に移行する財務分析コード情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="c39df-131">Specify the financial dimension information that should be transferred from the transactions in the subsidiary accounts to the transactions in the consolidated legal entity.</span></span>
    - <span data-ttu-id="c39df-132">リストの財務分析コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="c39df-132">Select financial dimensions in the list.</span></span>
    - <span data-ttu-id="c39df-133">連結される各財務分析コードに対して正しい詳細を識別します。</span><span class="sxs-lookup"><span data-stu-id="c39df-133">Identify the correct specification for each financial dimension that is consolidated.</span></span> <span data-ttu-id="c39df-134">使用できるオプションには、**分析コード**、**グループ分析コード**、**会社の勘定**、**勘定** があります。</span><span class="sxs-lookup"><span data-stu-id="c39df-134">The available options include **Dimension**, **Group dimension**, **Company accounts**, and **Account**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="c39df-135">**グループ分析コード** オプションを使用すると、連結対象の会社グループで使用される分析コードの値を定義できます。</span><span class="sxs-lookup"><span data-stu-id="c39df-135">The **Group dimension** option lets you define the dimension value that is used by the group of companies that is being consolidated.</span></span>

    - <span data-ttu-id="c39df-136">連結するセグメントの順番を指定します。</span><span class="sxs-lookup"><span data-stu-id="c39df-136">Specify the segment order to consolidate in.</span></span>

4. <span data-ttu-id="c39df-137">**法人** タブで 、次の手順に従って、エクスポートする法人を指定します。</span><span class="sxs-lookup"><span data-stu-id="c39df-137">On the **Legal entities** tab, follow these steps to specify the legal entity that you're exporting:</span></span>

    1. <span data-ttu-id="c39df-138">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c39df-138">Select **New**.</span></span>
    2. <span data-ttu-id="c39df-139">**ソースの法人** フィールドに、法人を入力します。</span><span class="sxs-lookup"><span data-stu-id="c39df-139">In the **Source legal entity** field, enter the legal entity.</span></span>

        <span data-ttu-id="c39df-140">同じデータベース内の複数の関連会社に同じ基準を適用する場合は、それらの関連会社から別のエクスポート ファイルへ一括してデータを転送できます。</span><span class="sxs-lookup"><span data-stu-id="c39df-140">If the same criteria apply to several subsidiaries that are in the same database, you can transfer data from those subsidiaries to separate export files in a single operation:</span></span>

        1. <span data-ttu-id="c39df-141">ファイルにエクスポートする勘定科目の子会社法人ごとに行を作成します。</span><span class="sxs-lookup"><span data-stu-id="c39df-141">Create a line for each subsidiary legal entity for which accounts should be exported to files.</span></span> <span data-ttu-id="c39df-142">これらのファイルは、後に連結法人にインポートされます。</span><span class="sxs-lookup"><span data-stu-id="c39df-142">These files will be imported into the consolidated legal entity later.</span></span>
        2. <span data-ttu-id="c39df-143">関連会社ごとに、その会社名とエクスポート ジョブで作成されるエクスポート ファイルの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="c39df-143">For each subsidiary, enter the subsidiary name and the name of the export file that will be created during the export job.</span></span>

    3. <span data-ttu-id="c39df-144">**換算差額の勘定タイプ** フィールドで 、**損益** または **貸借対照表** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c39df-144">In **Account type of conversion differences** field, Select **Profit and loss** or **Balance sheet**.</span></span>
    4. <span data-ttu-id="c39df-145">作成されるエクスポート ファイルのファイル名を入力します。</span><span class="sxs-lookup"><span data-stu-id="c39df-145">Enter a file name for the export file that will be created.</span></span>

5. <span data-ttu-id="c39df-146">**OK** を選択してエクスポートを実行します。</span><span class="sxs-lookup"><span data-stu-id="c39df-146">Select **OK** to run the export.</span></span>

<span data-ttu-id="c39df-147">エクスポートが完了すると、各ファイルに保存されたレコード数を示すメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c39df-147">When the export is completed, you receive a message that shows the number of records that were saved in each file.</span></span> <span data-ttu-id="c39df-148">その後、連結法人にファイルをインポートできます。</span><span class="sxs-lookup"><span data-stu-id="c39df-148">You can then import the files into the consolidated legal entity.</span></span>
