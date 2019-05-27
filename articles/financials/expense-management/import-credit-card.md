---
title: クレジット カード トランザクションのインポートおよび管理
description: このトピックでは、インポートおよび経費に関連するクレジット カード トランザクションを管理する方法について説明します。 定期スケジュールで自動的にインポートされるようこれらのトランザクションを設定したり、または必要に応じて手動でトランザクションをインポートすることができます。
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 9674cf495b7fdd40d8672580b9d10e9ebe626bb0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565116"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="57aac-104">クレジット カード トランザクションのインポートおよび管理</span><span class="sxs-lookup"><span data-stu-id="57aac-104">Import and maintain credit card transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="57aac-105">経費に関連するクレジット カード トランザクションは、定期的なスケジュールで自動的にインポートされるように設定できます。</span><span class="sxs-lookup"><span data-stu-id="57aac-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="57aac-106">または、必要に応じて手動でトランザクションをインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="57aac-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="57aac-107">クレジット カード トランザクションは、クレジット カード トランザクション データ エンティティを通じてインポートされます。</span><span class="sxs-lookup"><span data-stu-id="57aac-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="57aac-108">データ エンティティに関する詳細については、「[データ エンティティ](../../dev-itpro/data-entities/data-entities.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="57aac-108">For more information about data entities, see [Data entities](../../dev-itpro/data-entities/data-entities.md).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="57aac-109">クレジット カード トランザクションをインポートします</span><span class="sxs-lookup"><span data-stu-id="57aac-109">Import credit card transactions</span></span>

1. <span data-ttu-id="57aac-110">**クレジット カード トランザクション** ページで、**トランザクションのインポート** をします。</span><span class="sxs-lookup"><span data-stu-id="57aac-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="57aac-111">データ管理を初めて開く場合、続行する前に、システムはデータ エンティティの一覧を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="57aac-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="57aac-112">**名前** フィールドに、インポート ジョブの固有の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="57aac-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="57aac-113">**ソース データ形式** フィールドに、インポートするクレジット カード トランザクションを含むファイルの形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="57aac-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="57aac-114">**アップロード** を選択し、インポートするファイルを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="57aac-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="57aac-115">ファイルをアップロードした後、タイルの **マップの表示** リンクを選択することにより、クレジット カード トランザクション ファイルのマッピングおよびクレジット カード トランザクション データ エンティティの列を検証します。</span><span class="sxs-lookup"><span data-stu-id="57aac-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="57aac-116">マッピング エラーがある場合、またはマッピングを変更する必要がある場合は、**マッピングの視覚化** タブまたは **マッピング詳細** タブのいずれかからマッピング変更を行います。</span><span class="sxs-lookup"><span data-stu-id="57aac-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="57aac-117">クレジット カード トランザクションを自動化するには、**定期的なデータ ジョブの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57aac-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="57aac-118">どのくらいの頻度でクレジット カード トランザクションをインポートする必要があるかを定義する、定期的なアイテムを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="57aac-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="57aac-119">完了したら、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57aac-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="57aac-120">今すぐ選択したファイルをインポートするには、**インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57aac-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="57aac-121">インポート中にエラーが発生した場合は、修正する必要があるエラーを表示しインポートの成功を保証するために、実行ログまたはステージング データを表示できます。</span><span class="sxs-lookup"><span data-stu-id="57aac-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="57aac-122">1 つ以上のファイル形式をインポートする必要がある場合、形式タイプごとに個別のインポート ジョブを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="57aac-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="57aac-123">離職した従業員用のクレジット カード トランザクションの再割り当て</span><span class="sxs-lookup"><span data-stu-id="57aac-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="57aac-124">従業員レコードが終了すると、従業員の Active Directory Domain Services (AD DS) の勘定は無効になります。</span><span class="sxs-lookup"><span data-stu-id="57aac-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="57aac-125">ただし、経費で処理され、および払い戻しされなければならない、有効なクレジット カード トランザクションがあります。</span><span class="sxs-lookup"><span data-stu-id="57aac-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="57aac-126">**クレジット カード トランザクション** ページから、関連する従業員が離職した場合にすべてのクレジット カード トランザクションの従業員を再度割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="57aac-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="57aac-127">1 つまたは複数のクレジット カード トランザクションを選択し、**トランザクションの再割り当て** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57aac-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="57aac-128">クレジット カード トランザクションを割り当てる別の従業員を選択できます。</span><span class="sxs-lookup"><span data-stu-id="57aac-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="57aac-129">クレジット カード トランザクションを再度割り当てられた後、トランザクションは経費精算書用に選択され、経費精算書払い戻しの通常プロセスで支払うことができます。</span><span class="sxs-lookup"><span data-stu-id="57aac-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
