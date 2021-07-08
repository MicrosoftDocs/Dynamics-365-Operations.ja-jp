---
title: 財務諸表に関するよく寄せられる質問
description: このトピックでは、よく寄せられる財務諸表に関するいくつかの質問に対する回答を提供します。
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e1b67f86446403933005008a9a1e2cc6739dc516
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266636"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="d3a69-103">財務諸表に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="d3a69-103">Financial reporting FAQ</span></span>

<span data-ttu-id="d3a69-104">このトピックでは、よく寄せられる財務諸表に関する質問に対する回答を提供します。</span><span class="sxs-lookup"><span data-stu-id="d3a69-104">This topic provides answers to frequently asked questions about Financial reporting.</span></span>

## <a name="how-do-i-restrict-access-to-a-report-by-using-tree-security"></a><span data-ttu-id="d3a69-105">ツリー セキュリティを使用して、レポートへのアクセスを制限するにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="d3a69-105">How do I restrict access to a report by using tree security?</span></span>

<span data-ttu-id="d3a69-106">次の例は、ツリー セキュリティを使用してレポートへのアクセスを制限する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="d3a69-106">The following example shows how to restrict access to a report by using tree security.</span></span>

<span data-ttu-id="d3a69-107">USMF デモ会社には、財務諸表のすべてのユーザーがアクセスすべきではない **貸借対照表** レポートがあります。</span><span class="sxs-lookup"><span data-stu-id="d3a69-107">The USMF demo company has a **Balance sheet** report that not all Financial reporting users should have access to.</span></span> <span data-ttu-id="d3a69-108">ツリー セキュリティを使用すると、あるレポートへのアクセスを制限して、特定のユーザーのみがそれにアクセスできるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="d3a69-108">You can use tree security to restrict access to a single report so that only specific users can access it.</span></span>

1. <span data-ttu-id="d3a69-109">Financial Reporter Report Designer にサインインします。</span><span class="sxs-lookup"><span data-stu-id="d3a69-109">Sign in to Financial Reporter Report Designer.</span></span>
2. <span data-ttu-id="d3a69-110">**ファイル \> 新規 \> ツリー定義** の順に選択して新しいツリー定義を作成します。</span><span class="sxs-lookup"><span data-stu-id="d3a69-110">Select **File \> New \> Tree Definition** to create a new tree definition.</span></span>
3. <span data-ttu-id="d3a69-111">**ユニットのセキュリティ** 列の **集計** 行をダブルタップ (またはダブルクリック) します。</span><span class="sxs-lookup"><span data-stu-id="d3a69-111">Double-tap (or double-click) the **Summary** line in the **Unit Security** column.</span></span>
4. <span data-ttu-id="d3a69-112">**ユーザーとグループ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a69-112">Select **Users and Groups**.</span></span>
5. <span data-ttu-id="d3a69-113">レポートにアクセスする必要があるユーザーまたはグループを選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a69-113">Select the users or groups that require access to the report.</span></span>
6. <span data-ttu-id="d3a69-114">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a69-114">Select **Save**.</span></span>
7. <span data-ttu-id="d3a69-115">レポート定義で、新しいツリー定義を追加します。</span><span class="sxs-lookup"><span data-stu-id="d3a69-115">In the report definition, add your new tree definition.</span></span>
8. <span data-ttu-id="d3a69-116">ツリー定義で、**設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a69-116">In the tree definition, select **Setting**.</span></span> <span data-ttu-id="d3a69-117">**レポート ユニットの選択** で、**すべてのユニットを含む** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a69-117">Then, under **Reporting unit selection**, select **Include all units**.</span></span>

## <a name="how-do-i-identify-which-accounts-dont-match-my-balances"></a><span data-ttu-id="d3a69-118">残高と一致しない勘定は、どのように識別できますか。</span><span class="sxs-lookup"><span data-stu-id="d3a69-118">How do I identify which accounts don't match my balances?</span></span>

<span data-ttu-id="d3a69-119">残高が一致しないレポートがある場合は、以下の手順に従って、各勘定と差異を特定します。</span><span class="sxs-lookup"><span data-stu-id="d3a69-119">If you have a report that doesn't have matching balances, use the following procedures to identify each account and variance.</span></span>

### <a name="in-financial-reporter-report-designer"></a><span data-ttu-id="d3a69-120">Financial Reporter Report Designer 内</span><span class="sxs-lookup"><span data-stu-id="d3a69-120">In Financial Reporter Report Designer</span></span>

1. <span data-ttu-id="d3a69-121">新しい行定義を作成します。</span><span class="sxs-lookup"><span data-stu-id="d3a69-121">Create a new row definition.</span></span>
2. <span data-ttu-id="d3a69-122">**編集 \> 分析コードからの行の挿入** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a69-122">Select **Edit \> Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="d3a69-123">**MainAccount** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a69-123">Select **MainAccount**.</span></span>
4. <span data-ttu-id="d3a69-124">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a69-124">Select **OK**.</span></span>
5. <span data-ttu-id="d3a69-125">行定義を保存します。</span><span class="sxs-lookup"><span data-stu-id="d3a69-125">Save the row definition.</span></span>
6. <span data-ttu-id="d3a69-126">新しい列定義を作成します。</span><span class="sxs-lookup"><span data-stu-id="d3a69-126">Create a new column definition.</span></span>
7. <span data-ttu-id="d3a69-127">新しいレポート定義を作成します。</span><span class="sxs-lookup"><span data-stu-id="d3a69-127">Create a new report definition.</span></span>
8. <span data-ttu-id="d3a69-128">**設定** を選択し、このオプションのマークを解除します。</span><span class="sxs-lookup"><span data-stu-id="d3a69-128">Select **Settings** and unmark this option.</span></span>
9. <span data-ttu-id="d3a69-129">レポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="d3a69-129">Generate the report.</span></span> 
10. <span data-ttu-id="d3a69-130">レポートを Microsoft Excel にエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="d3a69-130">Export the report to Microsoft Excel.</span></span>

### <a name="in-dynamics-365-finance"></a><span data-ttu-id="d3a69-131">Dynamics 365 Finance 内</span><span class="sxs-lookup"><span data-stu-id="d3a69-131">In Dynamics 365 Finance</span></span>

1. <span data-ttu-id="d3a69-132">**一般会計 \> 照会およびレポート \> 試算表** の順に進みます。</span><span class="sxs-lookup"><span data-stu-id="d3a69-132">Go to **General ledger \> Inquiries and reports \> Trial balance**.</span></span>
2. <span data-ttu-id="d3a69-133">次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="d3a69-133">Set the following fields:</span></span>

    - <span data-ttu-id="d3a69-134">**開始日** – 会計年度の開始日を入力します。</span><span class="sxs-lookup"><span data-stu-id="d3a69-134">**From Date** – Enter the start date of the fiscal year.</span></span>
    - <span data-ttu-id="d3a69-135">**終了日** – レポートを生成する日を入力します。</span><span class="sxs-lookup"><span data-stu-id="d3a69-135">**To Date** – Enter the date that you're generating the report for.</span></span>
    - <span data-ttu-id="d3a69-136">**財務分析コード** – このフィールドを **主勘定セット** に設定します。</span><span class="sxs-lookup"><span data-stu-id="d3a69-136">**Financial Dimension** – Set this field to **Main Account set**.</span></span>

3. <span data-ttu-id="d3a69-137">**計算** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3a69-137">Select **Calculate**.</span></span>
4. <span data-ttu-id="d3a69-138">レポートを Excel にエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="d3a69-138">Export the report to Excel.</span></span>

<span data-ttu-id="d3a69-139">これで、Financial Reporter Excel レポートから **試算表** レポートにデータをコピーして、**決算残高** 列を比較できます。</span><span class="sxs-lookup"><span data-stu-id="d3a69-139">You should now be able to copy the data from the Financial Reporter Excel report to the **Trial Balance** report, so that you can compare the **Closing Balance** columns.</span></span>

## <a name="when-i-design-a-report-in-report-designer-or-when-i-generate-a-financial-report-i-received-the-following-message-the-operation-could-not-be-completed-due-to-a-problem-in-the-data-provider-framework-how-should-i-respond"></a><span data-ttu-id="d3a69-140">Report Designer でレポートを設計したり、財務諸表を生成する場合に、「データ プロバイダー フレームワークの問題が原因で操作を完了できません」というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d3a69-140">When I design a report in Report Designer, or when I generate a financial report, I received the following message: "The operation could not be completed due to a problem in the data provider framework."</span></span> <span data-ttu-id="d3a69-141">対応方法を教えてください。</span><span class="sxs-lookup"><span data-stu-id="d3a69-141">How should I respond?</span></span>

<span data-ttu-id="d3a69-142">このメッセージは、財務諸表の使用中にシステムがデータ マートから財務メタデータを取得しようとしたときに問題が発生したことを示します。</span><span class="sxs-lookup"><span data-stu-id="d3a69-142">The message indicates that an issue occurred when the system tried to retrieve financial metadata from the data mart while you were using Financial reporting.</span></span> <span data-ttu-id="d3a69-143">この問題に対応するには、次の 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="d3a69-143">There are two ways to respond to this issue:</span></span>

- <span data-ttu-id="d3a69-144">Report Designer の **ツール \> 統合の状態** に移動して、データの統合の状態を確認します。</span><span class="sxs-lookup"><span data-stu-id="d3a69-144">Review the integration status of the data by going to **Tools \> Integration status** in Report Designer.</span></span> <span data-ttu-id="d3a69-145">統合が不完全な場合は、完了するまで待ちます。</span><span class="sxs-lookup"><span data-stu-id="d3a69-145">If the integration is incomplete, wait for it to be completed.</span></span> <span data-ttu-id="d3a69-146">その後、メッセージを受信したときに行っていた操作を再試行します。</span><span class="sxs-lookup"><span data-stu-id="d3a69-146">Then retry what you were doing when you received the message.</span></span>
- <span data-ttu-id="d3a69-147">サポートに問い合わせ、問題を特定して作業してください。</span><span class="sxs-lookup"><span data-stu-id="d3a69-147">Contact Support to identify and work through the issue.</span></span> <span data-ttu-id="d3a69-148">システムにデータの不整合がある可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d3a69-148">There might be inconsistent data in the system.</span></span> <span data-ttu-id="d3a69-149">サポート エンジニアは、サーバー上の問題を特定し、更新が必要な可能性がある特定のデータを探す支援を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="d3a69-149">Support engineers can help you identify that issue on the server and find the specific data that might require an update.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
