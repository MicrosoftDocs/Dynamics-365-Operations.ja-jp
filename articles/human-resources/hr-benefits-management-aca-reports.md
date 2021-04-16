---
title: 福利厚生管理でアフォーダブル ケア法のレポートを生成する
description: このトピックでは、福利厚生管理を使用して、Form1095-B および Form 1095-C でアフォーダブル ケア法 (ACA) の雇用主の命令に関して報告された情報を追跡する方法について説明します。
author: andreabichsel
ms.date: 12/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: a41195ea3b52a707ce9deae38f12eb90de2ff5aa
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805805"
---
# <a name="generate-aca-reports-in-benefits-management"></a><span data-ttu-id="29cd7-103">福利厚生管理で ACA レポートを生成する</span><span class="sxs-lookup"><span data-stu-id="29cd7-103">Generate ACA reports in Benefits management</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="29cd7-104">福利厚生管理を使用すると、Form1095-B および Form 1095-C でアフォーダブル ケア法 (ACA) の雇用主の命令に関して報告された情報を追跡することができます。</span><span class="sxs-lookup"><span data-stu-id="29cd7-104">Benefits management helps you track information that is reported on Form 1095-B and Form 1095-C for the Affordable Care Act (ACA) employer mandate.</span></span> <span data-ttu-id="29cd7-105">古い **福利厚生** ワークスペースの ACA レポート機能と同様に、この機能は米国の法人にのみ適用されるものです。</span><span class="sxs-lookup"><span data-stu-id="29cd7-105">Like the ACA reporting capability in the old **Benefits** workspace, this functionality applies only to legal entities in the United States.</span></span>

<span data-ttu-id="29cd7-106">この機能を使用するには、最初に **高度な福利厚生管理** を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="29cd7-106">To use this functionality, you must first turn on **Advanced Benefits Management**.</span></span> <span data-ttu-id="29cd7-107">福利厚生管理に関する重要な説明などの詳細については、[福利厚生管理の有効化または無効化](hr-admin-manage-features.md#enable-or-disable-benefits-management) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="29cd7-107">For more information, including important caveats about Benefits management, see [Enable or disable Benefits management](hr-admin-manage-features.md#enable-or-disable-benefits-management).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="29cd7-108">ACA レポートは、**福利厚生管理** ワークスペース、または古い **福利厚生** ワークスペースのいずれかからのみ使用してください。この両方から使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="29cd7-108">You can use ACA reporting only from either the **Benefits management** workspace or the old **Benefits** workspace, not from both.</span></span> <span data-ttu-id="29cd7-109">たとえば、福利厚生管理に切り替えた場合、ACA レポートは、古い **福利厚生** ワークスペースからではなく、**福利厚生管理ワークスペース** からのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="29cd7-109">For example, if you switched to Benefits management, ACA reporting is available only from the **Benefits management** workspace, not from the old **Benefits** workspace.</span></span>
>
> <span data-ttu-id="29cd7-110">加入契約をした年度の途中で福利厚生管理に切り替える場合、福利厚生管理で通年分の従業員データを正しく構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="29cd7-110">If you switch to Benefits management in the middle of an enrollment year, you must correctly configure employee data for the whole year in Benefits management.</span></span> <span data-ttu-id="29cd7-111">これにより、年間を通して正確なレポート情報を確実に受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="29cd7-111">In this way, you ensure that you will receive accurate reporting information for the whole year.</span></span>

## <a name="getting-started"></a><span data-ttu-id="29cd7-112">はじめに</span><span class="sxs-lookup"><span data-stu-id="29cd7-112">Getting started</span></span>

<span data-ttu-id="29cd7-113">Form 1095-B および Form 1095-C の情報を追跡するには、まずアフォーダブル ケア法の補償グループを 1 つ以上作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="29cd7-113">To track information for 1095 forms, first create one or more Affordable Care coverage groups.</span></span> <span data-ttu-id="29cd7-114">これらのグループは、次の情報を示しています :</span><span class="sxs-lookup"><span data-stu-id="29cd7-114">These groups indicate the following information:</span></span>

- <span data-ttu-id="29cd7-115">従業員に提供された保険のオファー</span><span class="sxs-lookup"><span data-stu-id="29cd7-115">The offer of coverage that was provided to an employee</span></span>
- <span data-ttu-id="29cd7-116">コストが連邦政府の貧困ラインを超えている場合の、最低月額保険料の従業員負担額</span><span class="sxs-lookup"><span data-stu-id="29cd7-116">The employee's share of the lowest-cost monthly premium, if the cost is above the federal poverty line</span></span>
- <span data-ttu-id="29cd7-117">雇用主が使用する免責事項 (該当する場合)</span><span class="sxs-lookup"><span data-stu-id="29cd7-117">The safe harbor that is used by the employer, if applicable</span></span>

<span data-ttu-id="29cd7-118">変更されたアフォーダブル ケア法のグループを使用すると、同じ条件を持つ複数の従業員記録に対して、この情報を管理するの場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="29cd7-118">Affordable Care coverage groups help you manage this information for multiple employee records that have the same conditions.</span></span> <span data-ttu-id="29cd7-119">1人または複数の従業員に簡単にグループを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="29cd7-119">You can easily assign groups to one or more employees.</span></span>

### <a name="create-or-edit-an-affordable-care-coverage-group"></a><span data-ttu-id="29cd7-120">アフォーダブル ケア法のグループを作成・編集する</span><span class="sxs-lookup"><span data-stu-id="29cd7-120">Create or edit an Affordable Care coverage group</span></span>

1. <span data-ttu-id="29cd7-121">**福利厚生管理** ワークスペースで、**アフォーダブル ケア法のグループ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="29cd7-121">In the **Benefits management** workspace, select **Affordable Care coverage group**.</span></span>

    ![アフォーダブル ケア法のグループを選択する](./media/hr-benefits-management-aca-coverage-group.png)

2. <span data-ttu-id="29cd7-123">アフォーダブル ケア法のグループを新規作成するには、**新規** を選択し、既存のグループを編集するには、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="29cd7-123">Select **New** to create a new Affordable Care coverage group or **Edit** to change an existing group.</span></span>

    ![新規または編集を選択する](./media/hr-benefits-management-aca-new.png)

3. <span data-ttu-id="29cd7-125">次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="29cd7-125">Set the following fields.</span></span>

    | <span data-ttu-id="29cd7-126">フィールド</span><span class="sxs-lookup"><span data-stu-id="29cd7-126">Field</span></span> | <span data-ttu-id="29cd7-127">説明</span><span class="sxs-lookup"><span data-stu-id="29cd7-127">Description</span></span> |
    |---|---|
    | <span data-ttu-id="29cd7-128">氏名</span><span class="sxs-lookup"><span data-stu-id="29cd7-128">Name</span></span> | <span data-ttu-id="29cd7-129">グループの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="29cd7-129">Enter a name for the group.</span></span> |
    | <span data-ttu-id="29cd7-130">説明</span><span class="sxs-lookup"><span data-stu-id="29cd7-130">Description</span></span> | <span data-ttu-id="29cd7-131">グループの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="29cd7-131">Enter a description of the group.</span></span> |
    | <span data-ttu-id="29cd7-132">補償内容</span><span class="sxs-lookup"><span data-stu-id="29cd7-132">Offer of coverage</span></span> | <span data-ttu-id="29cd7-133">従業員、その配偶者、パートナー、その扶養家族に提供される保険です。</span><span class="sxs-lookup"><span data-stu-id="29cd7-133">The coverage that is offered to employees, their spouse or partner, and their dependents.</span></span> |
    | <span data-ttu-id="29cd7-134">費用の従業員負担</span><span class="sxs-lookup"><span data-stu-id="29cd7-134">Employee share of cost</span></span> | <span data-ttu-id="29cd7-135">従業員が負担する金額です。</span><span class="sxs-lookup"><span data-stu-id="29cd7-135">The amount that the employee is responsible for.</span></span> |
    | <span data-ttu-id="29cd7-136">適用区域 4980H Safe Harbor</span><span class="sxs-lookup"><span data-stu-id="29cd7-136">Applicable section 4980H safe harbor</span></span> | <span data-ttu-id="29cd7-137">4980 H 免責条項、または移行支援コードです。</span><span class="sxs-lookup"><span data-stu-id="29cd7-137">The 4980H safe harbor or transition relief code.</span></span> |
    | <span data-ttu-id="29cd7-138">計画開始月</span><span class="sxs-lookup"><span data-stu-id="29cd7-138">Plan start month</span></span> | <span data-ttu-id="29cd7-139">福利厚生プランの年度が始まる暦月を選択します。</span><span class="sxs-lookup"><span data-stu-id="29cd7-139">Select the calendar month when your benefit plan year begins.</span></span> |
    | <span data-ttu-id="29cd7-140">グループの発効日</span><span class="sxs-lookup"><span data-stu-id="29cd7-140">Group valid from</span></span> | <span data-ttu-id="29cd7-141">このレコードが有効となる最初の日付です。</span><span class="sxs-lookup"><span data-stu-id="29cd7-141">The first date when this record is valid.</span></span> |
    | <span data-ttu-id="29cd7-142">グループの有効期限</span><span class="sxs-lookup"><span data-stu-id="29cd7-142">Group valid through</span></span> | <span data-ttu-id="29cd7-143">このレコードが有効となる最後の日付です。</span><span class="sxs-lookup"><span data-stu-id="29cd7-143">The last date when this record is valid.</span></span> <span data-ttu-id="29cd7-144">有効期限がない場合は、**なし** と入力します。</span><span class="sxs-lookup"><span data-stu-id="29cd7-144">If there is no expiration date, enter **Never**.</span></span> |

    ![アフォーダブル ケア法のグループを作成する](./media/hr-benefits-management-aca-new-group.png)

4. <span data-ttu-id="29cd7-146">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="29cd7-146">Select **Save**.</span></span>

### <a name="assign-multiple-employees-to-an-affordable-care-coverage-group"></a><span data-ttu-id="29cd7-147">アフォーダブル ケア法のグループに複数の従業員を割り当てる</span><span class="sxs-lookup"><span data-stu-id="29cd7-147">Assign multiple employees to an Affordable Care coverage group</span></span>

1. <span data-ttu-id="29cd7-148">**福利厚生管理** ワークスペースで、**アフォーダブル ケア法のグループ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="29cd7-148">In the **Benefits management** workspace, select **Affordable Care coverage group**.</span></span>
2. <span data-ttu-id="29cd7-149">従業員を割り当てるグループを選択します。</span><span class="sxs-lookup"><span data-stu-id="29cd7-149">Select the group to assign employees to.</span></span>
3. <span data-ttu-id="29cd7-150">**一括割り当て** を選択します。</span><span class="sxs-lookup"><span data-stu-id="29cd7-150">Select **Mass assignment**.</span></span>

    ![一括割り当てを選択する](./media/hr-benefits-management-aca-mass-assignment.png)

4. <span data-ttu-id="29cd7-152">一覧で従業員を選択し、**割り当て** を選択します。</span><span class="sxs-lookup"><span data-stu-id="29cd7-152">Select employees in the list, and then select **Assign**.</span></span>

    ![選択した従業員をグループに割り当てる](./media/hr-benefits-management-aca-assign-coverage-group.png)

## <a name="maintain-multiple-versions-of-coverage-options"></a><span data-ttu-id="29cd7-154">アフォーダブル ケア法の複数バージョンのオプションを管理する</span><span class="sxs-lookup"><span data-stu-id="29cd7-154">Maintain multiple versions of coverage options</span></span>

<span data-ttu-id="29cd7-155">任意のアフォーダブル ケア法のグループの複数のバージョンを維持することができます。</span><span class="sxs-lookup"><span data-stu-id="29cd7-155">You can maintain multiple versions of any coverage group.</span></span> <span data-ttu-id="29cd7-156">組織内で変更があった場合や、提供する福利厚生が変わった際に、新しいグループを作成して社員を再割り当てすることなく、グループの情報を常に最新の状態に保つことができます。</span><span class="sxs-lookup"><span data-stu-id="29cd7-156">When something changes in your organization or the benefits that are offered, you can keep the group's information up to date without having to create a new group and reassign employees to it.</span></span>

<span data-ttu-id="29cd7-157">アフォーダブル ケア法のグループを作成した後は、従業員を大量に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="29cd7-157">After you've created Affordable Care coverage groups, you can mass-assign employees to them.</span></span> <span data-ttu-id="29cd7-158">従業員をグループに個別に割り当て、ACA の情報を追跡および報告するかどうかを指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="29cd7-158">You can also individually assign employees to groups, and indicate whether ACA information is tracked and reported.</span></span>

<span data-ttu-id="29cd7-159">従業員の ACA 情報を追跡・報告する必要がない場合は、**レポート補充** オプションを **いいえ** に 設定できます。</span><span class="sxs-lookup"><span data-stu-id="29cd7-159">If you don't have to track and report ACA information for an employee, you can set the **Report coverage** option to **No**.</span></span> <span data-ttu-id="29cd7-160">たとえば、ACA のレポートが不要なパートタイムの従業員がいるとします。</span><span class="sxs-lookup"><span data-stu-id="29cd7-160">For example, you might have part-time employees who don't require ACA reporting.</span></span>

### <a name="override-default-values-for-an-employee"></a><span data-ttu-id="29cd7-161">従業員の既定値を上書きする</span><span class="sxs-lookup"><span data-stu-id="29cd7-161">Override default values for an employee</span></span>

<span data-ttu-id="29cd7-162">アフォーダブル ケア法のグループに割り当てられている従業員の場合、異なる値を必要とする月については、以下のオプションを変更することができます :</span><span class="sxs-lookup"><span data-stu-id="29cd7-162">For employees who are assigned to an Affordable Care coverage group, you can change the following options for any months that require different values:</span></span>

- <span data-ttu-id="29cd7-163">補償内容</span><span class="sxs-lookup"><span data-stu-id="29cd7-163">Offer of coverage</span></span>
- <span data-ttu-id="29cd7-164">費用の従業員負担</span><span class="sxs-lookup"><span data-stu-id="29cd7-164">Employee share of cost</span></span>
- <span data-ttu-id="29cd7-165">適用区域 4980H Safe Harbor</span><span class="sxs-lookup"><span data-stu-id="29cd7-165">Applicable section 4980H safe harbor</span></span>

> [!NOTE]
> <span data-ttu-id="29cd7-166">2020 のACA レポートについては、Form 1095-C に仕事場と自宅の両方の郵便番号を報告刷る必要があります。</span><span class="sxs-lookup"><span data-stu-id="29cd7-166">For 2020 ACA reports, you must report both work and home ZIP Codes on Form 1095-C.</span></span> <span data-ttu-id="29cd7-167">値は現在のアクティブな場所に基づいて自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="29cd7-167">Values are automatically filled in, based on current active locations.</span></span> <span data-ttu-id="29cd7-168">いずれかの場所が年間のいずれかの期間で異なっていた場合は、値を上書きする必要があります。</span><span class="sxs-lookup"><span data-stu-id="29cd7-168">If either location was different during any part of the year, you must override the value.</span></span> <span data-ttu-id="29cd7-169">1095-C レポートの **郵便番号** フィールド (17行目) は、 **補償の提供** コードに **1L** から **1Q** が含まれている場合にのみ入力されます。</span><span class="sxs-lookup"><span data-stu-id="29cd7-169">The **ZIP Code** field (line 17) of the 1095-C report is filled in only if the **Offer of coverage** code contains **1L** through **1Q**, as follows:</span></span>
>
> - <span data-ttu-id="29cd7-170">**1L、1M、1N** : 基本住所の郵便番号です</span><span class="sxs-lookup"><span data-stu-id="29cd7-170">**1L, 1M, or 1N:** The primary residence ZIP Code</span></span>
> - <span data-ttu-id="29cd7-171">**1O、1P、1Q**: 基本勤務場所の郵便番号です</span><span class="sxs-lookup"><span data-stu-id="29cd7-171">**1O, 1P, 1Q:** The primary work ZIP Code</span></span>

<span data-ttu-id="29cd7-172">アフォーダブル ケア法のグループの値の例外を入力するには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="29cd7-172">To enter exceptions for any values of an Affordable Care coverage group, follow these steps.</span></span>

1. <span data-ttu-id="29cd7-173">**人事管理** ワークスペースで、**リンク** を選択し、**作業者** を選択します。</span><span class="sxs-lookup"><span data-stu-id="29cd7-173">In the **Personnel management** workspace, select **Links**, and then select **Workers**.</span></span>
2. <span data-ttu-id="29cd7-174">リストで従業員を選択します。</span><span class="sxs-lookup"><span data-stu-id="29cd7-174">Select the employee in the list.</span></span>
3. <span data-ttu-id="29cd7-175">**雇用** タブの **詳細** セクションで、**アフォーダブル ケア法** を選択します。</span><span class="sxs-lookup"><span data-stu-id="29cd7-175">On the **Employment** tab, in the **More information** section, select **Affordable Care coverage**.</span></span>

    ![1人の従業員のオプションを変更する](./media/hr-benefits-management-aca-change-single-employee.png)

4. <span data-ttu-id="29cd7-177">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="29cd7-177">Select **Edit**.</span></span>
5. <span data-ttu-id="29cd7-178">変更が必要な各月については、**既定を上書きする** チェックボックスを選択し、必要に応じて他の値を変更します。</span><span class="sxs-lookup"><span data-stu-id="29cd7-178">For each month that requires changes, select the **Override default** check box, and then change the other values as required.</span></span>

    ![既定値を上書きする](./media/hr-benefits-management-aca-override-default.png)

6. <span data-ttu-id="29cd7-180">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="29cd7-180">Select **Save**.</span></span>

## <a name="report-health-care-coverage"></a><span data-ttu-id="29cd7-181">医療補償のレポート</span><span class="sxs-lookup"><span data-stu-id="29cd7-181">Report health care coverage</span></span>

<span data-ttu-id="29cd7-182">フルタイム従業員およびパートタイムの従業員に対して、雇用主がスポンサーとなっている自己負担の医療保険の適用範囲を追跡する必要があります。</span><span class="sxs-lookup"><span data-stu-id="29cd7-182">You must track any employer-sponsored, self-insured health care coverage for full-time and part-time employees.</span></span> <span data-ttu-id="29cd7-183">各従業員を扶養家族とともに、対象となった月の 1095-C レポートに記載してください。</span><span class="sxs-lookup"><span data-stu-id="29cd7-183">Include each employee, together with their dependents, on the 1095-C report for the months when they were covered.</span></span>

<span data-ttu-id="29cd7-184">福利厚生プランをレポートする必要がある場合は、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="29cd7-184">To indicate whether a benefit plan must be reported, follow these steps.</span></span>

1. <span data-ttu-id="29cd7-185">**給付金管理** ワーク スペースで、**福利厚生プラン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="29cd7-185">In the **Benefits management** workspace, select **Benefit plans**.</span></span>
2. <span data-ttu-id="29cd7-186">レポートする福利厚生プランを選択します。</span><span class="sxs-lookup"><span data-stu-id="29cd7-186">Select the benefit plan to report.</span></span>
3. <span data-ttu-id="29cd7-187">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="29cd7-187">Select **Edit**.</span></span>
4. <span data-ttu-id="29cd7-188">**アフォーダブル ケア法に基づくレポート** のオプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="29cd7-188">Set the **Reported under the Affordable Care Act** option to **Yes**.</span></span>

    ![医療保険のレポート](./media/hr-benefits-management-aca-report-coverage.png)

5. <span data-ttu-id="29cd7-190">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="29cd7-190">Select **Save**.</span></span>

<span data-ttu-id="29cd7-191">従業員が被扶養者の医療保険を選択した場合、被扶養者の保険期間は、被扶養者が登録または削除された日によって決定されます。</span><span class="sxs-lookup"><span data-stu-id="29cd7-191">If an employee chooses health care coverage for a dependent, the dependent's coverage period is determined by the date when the dependent was enrolled or removed.</span></span> <span data-ttu-id="29cd7-192">扶養家族の保険適用日は、加入年度に扶養家族の資格があり、プランに加入していた期間に基づいて自動的に計算されます。</span><span class="sxs-lookup"><span data-stu-id="29cd7-192">Coverage dates for dependents are automatically calculated based on the period when the dependent was eligible and active in a plan during the enrollment year.</span></span>

## <a name="generate-1095-b-and-1095-c-forms"></a><span data-ttu-id="29cd7-193">Form 1095-B および Form 1095-C</span><span class="sxs-lookup"><span data-stu-id="29cd7-193">Generate 1095-B and 1095-C forms</span></span>

<span data-ttu-id="29cd7-194">ACA の 1095-B と 1095-C を作成し、各従業員に配布することができます。</span><span class="sxs-lookup"><span data-stu-id="29cd7-194">You can generate ACA 1095-B and 1095-C forms, and then distribute them to each of your employees.</span></span> <span data-ttu-id="29cd7-195">また、国税庁 (IRS) に送信するための Form1095-C と対応する Form 1094-C の送信ファイルを電子的に作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="29cd7-195">You can also electronically generate Form 1095-C and the corresponding 1094-C transmittal files to send to the Internal Revenue Service (IRS).</span></span>

1. <span data-ttu-id="29cd7-196">**福利厚生管理** ワークスペースで、**Form ACA 1095-B**、または **Form ACA 1095-C** を選択します。</span><span class="sxs-lookup"><span data-stu-id="29cd7-196">In the **Benefits management** workspace, select **ACA 1095-B form** or **ACA 1095-C form**.</span></span>
2. <span data-ttu-id="29cd7-197">必要に応じてパラメータを変更し、 **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="29cd7-197">Change the parameters as required, and then select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="29cd7-198">500 人を超える従業員に From 1095-C を印刷する場合は、複数の PDF ファイルが作成されます。</span><span class="sxs-lookup"><span data-stu-id="29cd7-198">If you're printing 1095-C forms for more than 500 employees, you will receive more than one PDF file.</span></span> <span data-ttu-id="29cd7-199">**ドキュメント管理パラメーター** ページの **最大ファイル サイズ (MB)** フィールドの値を **150** にすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="29cd7-199">We recommend that you increase the value of the **Maximum file size in megabytes** field on the **Document management parameters** page to **150**.</span></span> <span data-ttu-id="29cd7-200">(このページをすぐに開くには、ナビゲーション バーの検索フィールドを使用してください。)</span><span class="sxs-lookup"><span data-stu-id="29cd7-200">(To quickly open that page, you can use the search field on the navigation bar.)</span></span>
    >
    > ![最大ファイル サイズを変更する](./media/hr-benefits-management-aca-maximum-file-size.png)

3. <span data-ttu-id="29cd7-202">レポートの状態を確認して表示するには、ナビゲーション バーの検索フィールドを使用して **電子レポート ジョブ** のページを開きます。</span><span class="sxs-lookup"><span data-stu-id="29cd7-202">To check the status of your reports and view them, use the search field on the navigation bar to open the **Electronic reporting jobs** page.</span></span>

    ![電子レポート ジョブのページで検索する](./media/hr-benefits-management-aca-search-electronic-reporting-jobs.png)

4. <span data-ttu-id="29cd7-204">表示するレポートを選択し、**ファイルを表示する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="29cd7-204">Select the report to view, and then select **Show files**.</span></span>

    ![ファイルを表示する](./media/hr-benefits-management-aca-show-files.png)

5. <span data-ttu-id="29cd7-206">**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="29cd7-206">Select **Open**.</span></span>

    ![ファイルを開く](./media/hr-benefits-management-aca-open-file.png)

6. <span data-ttu-id="29cd7-208">ブラウザのウィンドウ下部に表示される通知バーから、zip ファイルを開き、レポートを選択します。</span><span class="sxs-lookup"><span data-stu-id="29cd7-208">From the Notification bar that appears at the bottom of the browser window, open the zip file, and then select the report.</span></span> <span data-ttu-id="29cd7-209">PDF ファイルを表示または印刷できます。</span><span class="sxs-lookup"><span data-stu-id="29cd7-209">You can view or print the PDF file.</span></span>

    ![Form 1095-C のサンプル](./media/hr-benefits-management-aca-1095-c-form.png)

## <a name="view-aca-coverage-information"></a><span data-ttu-id="29cd7-211">ACA 補償情報の表示</span><span class="sxs-lookup"><span data-stu-id="29cd7-211">View ACA coverage information</span></span>

<span data-ttu-id="29cd7-212">**労働者のアフォーダブル ケア** ページには、次の情報が表示されます:</span><span class="sxs-lookup"><span data-stu-id="29cd7-212">The **Worker Affordable Care coverage** page shows the following information:</span></span>

- <span data-ttu-id="29cd7-213">各補償グループに割り当てられている従業員</span><span class="sxs-lookup"><span data-stu-id="29cd7-213">Employees who are assigned to each coverage group</span></span>
- <span data-ttu-id="29cd7-214">レポートに含める必要ない従業員</span><span class="sxs-lookup"><span data-stu-id="29cd7-214">Employees who don't have to be included on a report</span></span>
- <span data-ttu-id="29cd7-215">未割り当ての従業員</span><span class="sxs-lookup"><span data-stu-id="29cd7-215">Unassigned employees</span></span>

<span data-ttu-id="29cd7-216">この情報を表示するには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="29cd7-216">To view this information, follow these steps.</span></span>

1. <span data-ttu-id="29cd7-217">**福利厚生管理** ワークスペースで、**労働者のアフォーダブル ケア法** を選択します。</span><span class="sxs-lookup"><span data-stu-id="29cd7-217">In the **Benefits management** workspace, select **Worker Affordable Care coverage**.</span></span>
2. <span data-ttu-id="29cd7-218">**グループ゜名** フィールドで、グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="29cd7-218">In the **Group name** field, select a group.</span></span>

    ![ACA 補償の表示](./media/hr-benefits-management-aca-view-coverage.png)

<span data-ttu-id="29cd7-220">アフォーダブルケア法グループに由来する既定値のいずれかが上書きされた場合、変更された値の横にアスタリスクが表示されます。</span><span class="sxs-lookup"><span data-stu-id="29cd7-220">If any default values from the Affordable Care coverage group have been overridden, an asterisk appears next to the value that was changed.</span></span> <span data-ttu-id="29cd7-221">12 か月間すべての値が同じ、または上書きされていない場合、**12 か月すべて** 列に値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="29cd7-221">If the values for all 12 months are the same and haven't been overridden, the value appears in the **All 12 months** column.</span></span>

<span data-ttu-id="29cd7-222">ACA のレポート可能ではないとマークされ、Form 1095-C が必要ない従業員を表示できます。</span><span class="sxs-lookup"><span data-stu-id="29cd7-222">You can view employees who are marked as not ACA-reportable, and who won't require a Form 1095-C.</span></span> <span data-ttu-id="29cd7-223">**フィルタ方法** フィールドで、 **ACA レポート不可** を選択します 。</span><span class="sxs-lookup"><span data-stu-id="29cd7-223">In the **Filter by** field, select **Not ACA reportable**.</span></span>

<span data-ttu-id="29cd7-224">グループに割り当てられていない従業員、または期限切れのグループに割り当てられている従業員を表示できます。</span><span class="sxs-lookup"><span data-stu-id="29cd7-224">You can view employees who aren't assigned to a group, or who are assigned to an expired group.</span></span> <span data-ttu-id="29cd7-225">**フィルタ方法** フィールドで 、**見割り当て、または期限切れのグループ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="29cd7-225">In the **Filter by** field, select **Unassigned or expired group**.</span></span>

### <a name="export-to-excel"></a><span data-ttu-id="29cd7-226">Excel にエクスポート</span><span class="sxs-lookup"><span data-stu-id="29cd7-226">Export to Excel</span></span>

<span data-ttu-id="29cd7-227">リストを Microsoft Excel にエクスポートするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="29cd7-227">To export any of the lists to Microsoft Excel, follow these steps.</span></span>

1. <span data-ttu-id="29cd7-228">**Microsoft Office で開く** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="29cd7-228">Select the **Open in Microsoft Office** button.</span></span>
2. <span data-ttu-id="29cd7-229">**内部利用 HCM 人事管理一時テーブル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="29cd7-229">Select **HCM Human Resources temporary table for internal use**.</span></span>
3. <span data-ttu-id="29cd7-230">**ダウンロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="29cd7-230">Select **Download**.</span></span>

### <a name="view-aca-reportable-dependents"></a><span data-ttu-id="29cd7-231">ACA レポート可能な従属データの表示</span><span class="sxs-lookup"><span data-stu-id="29cd7-231">View ACA-reportable dependents</span></span>

<span data-ttu-id="29cd7-232">自己保険を提供している理由で、被保険者を報告する必要がある場合は、**ACA のレポート対象** としてマークされている福利厚生プランで被保険者となっている扶養家族を表示できます。</span><span class="sxs-lookup"><span data-stu-id="29cd7-232">If you must report covered individuals because you provide self-insured coverage, you can view dependents who are covered under benefit plans that are marked as **ACA reportable**.</span></span> <span data-ttu-id="29cd7-233">アクション ペインで、**扶養家族の補償を表示する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="29cd7-233">On the Action Pane, select **View Dependent coverage**.</span></span>

![扶養家族の補償を表示する](./media/hr-benefits-management-aca-view-dependent-coverage.png)

<span data-ttu-id="29cd7-235">従業員の扶養家族の補償情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="29cd7-235">Coverage information for the employee's dependents is shown.</span></span>

![被扶養者の補償](./media/hr-benefits-management-aca-dependents.png)

> [!NOTE]
> <span data-ttu-id="29cd7-237">このページには、**ACA レポ-ト可能** としてマークされている福利厚生プランだけが表示されます。</span><span class="sxs-lookup"><span data-stu-id="29cd7-237">The page shows only benefits plans that are marked as **ACA reportable**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]