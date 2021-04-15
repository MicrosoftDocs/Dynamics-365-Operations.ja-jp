---
title: 住所変更の表示と管理
description: このトピックでは、Dynamics 365 Human Resources の住所変更を表示および管理する方法について説明します。
author: andreabichsel
ms.date: 08/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-07
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 5eca902ee7df7eb6835caf6f64b17f3f004b0776
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802458"
---
# <a name="view-and-manage-address-changes"></a><span data-ttu-id="54550-103">住所変更の表示と管理</span><span class="sxs-lookup"><span data-stu-id="54550-103">View and manage address changes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="54550-104">このトピックでは、Dynamics 365 Human Resources で従業員セルフサービスの **個人の詳細の編集** ページまたは **作業者**  の詳細ページで、住所の変更を表示および管理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="54550-104">This topic explains how you can view and manage address changes in the Employee self-service **Edit personal details** page or the **Worker** details page in Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="54550-105">多くの組織では、セルフサービス体験を通じた従業員の個人情報を管理することを希望しています。</span><span class="sxs-lookup"><span data-stu-id="54550-105">Many organizations want employees to manage their own personal details through a self-service experience.</span></span> <span data-ttu-id="54550-106">**従業員セルフ サービス** ワークスペースでユーザーが住所を更新できるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="54550-106">You can allow users to update their address in the **Employee self service** workspace.</span></span> <span data-ttu-id="54550-107">その後、**人事管理** ワークスペースでこれらの変更を監視できます。</span><span class="sxs-lookup"><span data-stu-id="54550-107">You can then monitor these changes in the **Personnel management** workspace.</span></span> <span data-ttu-id="54550-108">この機能を使用するには、**人事管理パラメータ** ページで変更を表示する日数を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="54550-108">To use this feature, you must specify the number of days that you want to view changes in the **Human resources parameters** page.</span></span>

## <a name="configure-address-change-parameters"></a><span data-ttu-id="54550-109">住所変更パラメータのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="54550-109">Configure address change parameters</span></span>

<span data-ttu-id="54550-110">**個人管理** ワークスペースに住所の変更を表示する日数をコンフィギュレーションするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="54550-110">To configure the number of days that you want address changes to appear in the **Personnel management** workspace, follow these steps:</span></span>

1. <span data-ttu-id="54550-111">ナビゲーション ウィンドウで、**個人管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="54550-111">On the navigation pane, select **Personnel management**.</span></span>

2. <span data-ttu-id="54550-112">**リンク** を選択します。</span><span class="sxs-lookup"><span data-stu-id="54550-112">Select **Links**.</span></span>

3. <span data-ttu-id="54550-113">**Human Resources パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="54550-113">Select **Human resources parameters**.</span></span>

4. <span data-ttu-id="54550-114">**住所の変更** の下の  **日数** フィールドに、**個人管理** ワークスペースに表示する住所の変更を表示する日数を入力します。</span><span class="sxs-lookup"><span data-stu-id="54550-114">In the **Number of days** field under **Address change**, enter the number of days that you want address changes to appear in the **Personnel management** workspace.</span></span>

5. <span data-ttu-id="54550-115">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="54550-115">Close the page.</span></span>

## <a name="create-or-change-an-employee-address"></a><span data-ttu-id="54550-116">従業員の住所の作成または変更</span><span class="sxs-lookup"><span data-stu-id="54550-116">Create or change an employee address</span></span>

<span data-ttu-id="54550-117">**従業員セルフ サービス** ワークスペースで従業員が自分の住所を更新できるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="54550-117">Employees can update their own address in the **Employee self service** workspace.</span></span> <span data-ttu-id="54550-118">住所を作成または変更するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="54550-118">Follow these steps to create or change an address:</span></span>

1. <span data-ttu-id="54550-119">自分のホーム ページで、**従業員セルフ サービス** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="54550-119">Select the **Employee self-service** tile on your home page.</span></span>

2. <span data-ttu-id="54550-120">**個人の詳細の編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="54550-120">Select **Edit personal details**.</span></span>

3. <span data-ttu-id="54550-121">住所を追加するために、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="54550-121">To add an address, select **Add**.</span></span> <span data-ttu-id="54550-122">既存の住所を更新するには、リストから住所を選択し、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="54550-122">To update an existing address, select the address from the list and then select **Edit**.</span></span>

4. <span data-ttu-id="54550-123">**名前や説明** を入力してください。</span><span class="sxs-lookup"><span data-stu-id="54550-123">Enter the **Name or description**.</span></span>

5. <span data-ttu-id="54550-124">**目的** のドロップダウン ボックスを選択し、住所のタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="54550-124">Select the **Purpose** drop-down box and then select the type of address.</span></span>

6. <span data-ttu-id="54550-125">**国/地域名** を入力します。</span><span class="sxs-lookup"><span data-stu-id="54550-125">Enter the **Country/region**.</span></span>

7. <span data-ttu-id="54550-126">**郵便番号** を入力します。</span><span class="sxs-lookup"><span data-stu-id="54550-126">Enter the **ZIP/postal code**.</span></span>

8. <span data-ttu-id="54550-127">**通り名** を入力します。</span><span class="sxs-lookup"><span data-stu-id="54550-127">Enter the **Street**.</span></span>

9. <span data-ttu-id="54550-128">**市町村**、**都道府県**、**市区郡** を入力します。</span><span class="sxs-lookup"><span data-stu-id="54550-128">Enter the **City**, **State**, and **County**.</span></span> <span data-ttu-id="54550-129">通常、これらのフィールドは、**郵便番号** フィールドに基づいて自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="54550-129">Typically, these fields are automatically set based on the **ZIP/postal code** field.</span></span>

10. <span data-ttu-id="54550-130">必要に応じて、基本住所を示す **基本** フィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="54550-130">Optionally, select the **Primary** field to indicate a primary address.</span></span> <span data-ttu-id="54550-131">1 つの住所のみを主住所としてマークできます。</span><span class="sxs-lookup"><span data-stu-id="54550-131">Only one address can be marked as the primary.</span></span> <span data-ttu-id="54550-132">既に別の住所が基本住所としてマークされている場合は、この住所を主住所として使用するかどうかを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="54550-132">If another address is already marked as the primary address, you'll need to confirm that you want to use this address as the primary.</span></span>

11. <span data-ttu-id="54550-133">オプションで、住所を非公開として示す **非公開** フィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="54550-133">Optionally, select the **Private** field to indicate that the address is private.</span></span> <span data-ttu-id="54550-134">個人の住所情報を表示するための明示的なアクセス許可を持つユーザーのみが、この住所を表示できます。</span><span class="sxs-lookup"><span data-stu-id="54550-134">Only users with explicit permission to view private address information can view this address.</span></span>

12. <span data-ttu-id="54550-135">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="54550-135">Select **OK**.</span></span>

## <a name="create-or-change-a-worker-address"></a><span data-ttu-id="54550-136">作業者の住所の作成または変更</span><span class="sxs-lookup"><span data-stu-id="54550-136">Create or change a worker address</span></span>

<span data-ttu-id="54550-137">**個人管理** ワークスペースの住所を更新できます。</span><span class="sxs-lookup"><span data-stu-id="54550-137">You can update an address in the **Personnel management** workspace.</span></span> <span data-ttu-id="54550-138">住所を作成または変更するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="54550-138">Follow these steps to create or change an address:</span></span>

1. <span data-ttu-id="54550-139">**人事管理** ワークスペースで、**リンク** を選択し、**作業者** を選択します。</span><span class="sxs-lookup"><span data-stu-id="54550-139">In the **Personnel management** workspace, select **Links**, and then select **Workers**.</span></span>

3. <span data-ttu-id="54550-140">作業者を選択し、**住所** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="54550-140">Select the worker, and then select **Addresses**.</span></span>

3. <span data-ttu-id="54550-141">住所を追加するために、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="54550-141">To add an address, select **Add**.</span></span> <span data-ttu-id="54550-142">既存の住所を更新するには、リストから住所を選択し、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="54550-142">To update an existing address, select the address from the list and then select **Edit**.</span></span>

4. <span data-ttu-id="54550-143">**名前や説明** を入力してください。</span><span class="sxs-lookup"><span data-stu-id="54550-143">Enter the **Name or description**.</span></span>

5. <span data-ttu-id="54550-144">**目的** のドロップダウン ボックスを選択し、住所のタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="54550-144">Select the **Purpose** drop-down box and then select the type of address.</span></span>

6. <span data-ttu-id="54550-145">**国/地域名** を入力します。</span><span class="sxs-lookup"><span data-stu-id="54550-145">Enter the **Country/region**.</span></span>

7. <span data-ttu-id="54550-146">**郵便番号** を入力します。</span><span class="sxs-lookup"><span data-stu-id="54550-146">Enter the **ZIP/postal code**.</span></span>

8. <span data-ttu-id="54550-147">**通り名** を入力します。</span><span class="sxs-lookup"><span data-stu-id="54550-147">Enter the **Street**.</span></span>

9. <span data-ttu-id="54550-148">**市町村**、**都道府県**、**市区郡** を入力します。</span><span class="sxs-lookup"><span data-stu-id="54550-148">Enter the **City**, **State**, and **County**.</span></span> <span data-ttu-id="54550-149">通常、これらのフィールドは、**郵便番号** フィールドに基づいて自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="54550-149">Typically, these fields are automatically set based on the **ZIP/postal code** field.</span></span>

10. <span data-ttu-id="54550-150">必要に応じて、基本住所を示す **基本** フィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="54550-150">Optionally, select the **Primary** field to indicate a primary address.</span></span> <span data-ttu-id="54550-151">1 つの住所のみを主住所としてマークできます。</span><span class="sxs-lookup"><span data-stu-id="54550-151">Only one address can be marked as the primary.</span></span> <span data-ttu-id="54550-152">既に別の住所が基本住所としてマークされている場合は、この住所を主住所として使用するかどうかを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="54550-152">If another address is already marked as the primary address, you'll need to confirm that you want to use this address as the primary.</span></span>

11. <span data-ttu-id="54550-153">オプションで、住所を非公開として示す **非公開** フィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="54550-153">Optionally, select the **Private** field to indicate that the address is private.</span></span> <span data-ttu-id="54550-154">個人の住所情報を表示するための明示的なアクセス許可を持つユーザーのみが、この住所を表示できます。</span><span class="sxs-lookup"><span data-stu-id="54550-154">Only users with explicit permission to view private address information can view this address.</span></span>

12. <span data-ttu-id="54550-155">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="54550-155">Select **OK**.</span></span>
 
## <a name="create-a-future-change-for-an-address"></a><span data-ttu-id="54550-156">住所の将来の変更を作成する</span><span class="sxs-lookup"><span data-stu-id="54550-156">Create a future change for an address</span></span>

<span data-ttu-id="54550-157">場合によっては、将来変更されるように住所を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="54550-157">In some cases, you might want to update an address to change in the future.</span></span> <span data-ttu-id="54550-158">たとえば、次の月の 15 日に従業員を移動している場合は、この機能が役立ちます。</span><span class="sxs-lookup"><span data-stu-id="54550-158">For example, this would be useful if an employee is moving on the 15th of the following month.</span></span>

1. <span data-ttu-id="54550-159">**住所の管理** ページを開くには、任意の住所グリッドから **その他のオプション > 詳細** をクリックし ます。</span><span class="sxs-lookup"><span data-stu-id="54550-159">Open the **Manage addresses** page by selecting **More options > Advanced** from any address grid.</span></span>

2. <span data-ttu-id="54550-160">**新規** を選択して、新しい住所を作成します。</span><span class="sxs-lookup"><span data-stu-id="54550-160">Select **New** to create a new address.</span></span>

3. <span data-ttu-id="54550-161">住所の詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="54550-161">Enter the details of the address.</span></span>

4. <span data-ttu-id="54550-162">**一般** クイック タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="54550-162">Select the **General** FastTab.</span></span>

5. <span data-ttu-id="54550-163">**有効日** フィールドで、新しい住所が有効になる日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="54550-163">In the **Effective date** field, select the date the new address will be effective.</span></span>

6. <span data-ttu-id="54550-164">**有効期限** フィールドで、オプションで住所が無効になる時を選択します。</span><span class="sxs-lookup"><span data-stu-id="54550-164">In the **Expiration date** field, optionally select when the address will no longer be effective.</span></span>

7. <span data-ttu-id="54550-165">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="54550-165">Close the pages.</span></span>

## <a name="view-and-monitor-address-changes"></a><span data-ttu-id="54550-166">住所変更の表示と監視</span><span class="sxs-lookup"><span data-stu-id="54550-166">View and monitor address changes</span></span>

<span data-ttu-id="54550-167">人事担当者は、**人事管理** ワークスペースの住所変更を表示および監視できます。</span><span class="sxs-lookup"><span data-stu-id="54550-167">HR personnel can view and monitor address changes from the **Personnel management** workspace.</span></span> <span data-ttu-id="54550-168">住所の変更を表示するには、**人事管理** タイルを **ホーム** ページから開きます。</span><span class="sxs-lookup"><span data-stu-id="54550-168">To view the address changes, open the **Personnel management** tile from the **Home** page.</span></span> <span data-ttu-id="54550-169">住所の変更は、右上隅のタイルに表示されます。</span><span class="sxs-lookup"><span data-stu-id="54550-169">The address changes display on a tile in the upper-right corner.</span></span> <span data-ttu-id="54550-170">上記の **住所変更** は、**人事リソースパラメータ** ページで指定された日数で発生した住所変更の数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="54550-170">The number above **Address changes** shows how many address changes occurred in the number of days specified in the **Human resources parameters** page.</span></span> 

<span data-ttu-id="54550-171">**住所変更** タイルを選択すると、新しいページに住所変更の詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="54550-171">When you select the **Address changes** tile, a new page displays the details of any address changes.</span></span> <span data-ttu-id="54550-172">右上隅の **将来の住所変更を含める** を選択して、将来の日付での住所の変更を表示できます。</span><span class="sxs-lookup"><span data-stu-id="54550-172">You can optionally select **Include future address changes** in the upper-right corner to display address changes with a future date.</span></span>

> [!NOTE]
> <span data-ttu-id="54550-173">これらの住所変更に関する警告またはメールを受信する場合は、アクション ウィンドウの **オプション** タブで新しいアラート ルールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="54550-173">If you want to receive an alert or email about these address changes, you can create a new alert rule on the **Options** tab in the Action Pane.</span></span> <span data-ttu-id="54550-174">アラート ルールを作成する方法の詳細については、[アラート ルールを作成](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/create-alerts) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="54550-174">For more information about alert rules, see [Create alert rules](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/create-alerts).</span></span><br><br>

> <span data-ttu-id="54550-175">住所の変更に対してワークフローをコンフィギュレーションする場合は、アラート ルールで **外部送信** オプションを選択し、Power Automate を使用して、ビジネス イベントのトリガーとワークフローのコンフィギュレーションを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="54550-175">If you want to configure a workflow for the address changes, you can select the **Send externally** option on your alert rule, and then use Power Automate to trigger the business event and configure a workflow.</span></span> <span data-ttu-id="54550-176">詳細については、[ビジネス イベントとしてのアラート](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/create-alerts#alerts-as-business-events) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="54550-176">For more information, see [Alerts as business events](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/create-alerts#alerts-as-business-events).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]