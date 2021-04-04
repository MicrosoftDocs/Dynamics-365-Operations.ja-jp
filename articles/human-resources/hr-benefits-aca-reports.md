---
title: 医療費負担適正化法 (Affordable Care Act) 報告の生成
description: アフォーダブルケア法 (ACA) の報告書は、アフォーダブルケア法 の **雇用主の責任** で定められた部分に対応するフォーム 1095-B および 1095-C を生成します。
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: f46a8efefd8e41c08bf4de49cfec856dc0a86da1
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468038"
---
# <a name="generate-aca-reports"></a><span data-ttu-id="540ef-103">ACA レポートの生成</span><span class="sxs-lookup"><span data-stu-id="540ef-103">Generate ACA reports</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="540ef-104">アフォーダブルケア法 (ACA) の報告書は、アフォーダブルケア法 の **雇用主の責任** で定められた部分に対応するフォーム 1095-B および 1095-C を生成します。</span><span class="sxs-lookup"><span data-stu-id="540ef-104">Affordable Care Act (ACA) reporting generates forms 1095-B and 1095-C in support of the **Employer Mandate** portion of the Affordable Care Act.</span></span>

> [!NOTE]
> <span data-ttu-id="540ef-105">ACA レポートは、米国の法人に対してのみ有効になります。</span><span class="sxs-lookup"><span data-stu-id="540ef-105">ACA reporting is only enabled for legal entities in the United States.</span></span>

## <a name="getting-started"></a><span data-ttu-id="540ef-106">はじめに</span><span class="sxs-lookup"><span data-stu-id="540ef-106">Getting started</span></span>

<span data-ttu-id="540ef-107">フォーム 1095-B および 1095-C の情報を追跡するには、まず、1 つ以上の アフォーダブルケア法の補償グループを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="540ef-107">To track information for forms 1095-B and 1095-C, you must first create one or more Affordable care coverage groups.</span></span> <span data-ttu-id="540ef-108">アフォーダブルケア補償グループの対象 :</span><span class="sxs-lookup"><span data-stu-id="540ef-108">Affordable Care coverage groups indicate:</span></span>

- <span data-ttu-id="540ef-109">従業員に対する補償の提供</span><span class="sxs-lookup"><span data-stu-id="540ef-109">The offer of coverage for an employee</span></span>
- <span data-ttu-id="540ef-110">最低月額保険料の従業員負担額 (コストが連邦政府の貧困ラインを超える場合)</span><span class="sxs-lookup"><span data-stu-id="540ef-110">The employee’s share of the lowest cost monthly premium, if the cost is above the federal poverty line</span></span>
- <span data-ttu-id="540ef-111">雇用主が使用する免責 (該当する場合)</span><span class="sxs-lookup"><span data-stu-id="540ef-111">Safe Harbor used by the employer, if applicable</span></span>

<span data-ttu-id="540ef-112">アフォーダブルケアの補償グループでは、条件が同じ従業員のレコードごとに変更することなく、これらのフィールドの情報を管理することができます。</span><span class="sxs-lookup"><span data-stu-id="540ef-112">Affordable Care coverage groups allow you to manage the information for these fields without changing every employee record where the conditions are the same.</span></span> <span data-ttu-id="540ef-113">ページの **一括割り当て** オプションを使用すると、アフォーダブルケアの補償グループを複数の従業員に簡単に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="540ef-113">You can easily assign Affordable Care coverage groups to one or more employees by using the **Mass assign** option on the page.</span></span>

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a><span data-ttu-id="540ef-114">補償グループの複数バージョンの管理</span><span class="sxs-lookup"><span data-stu-id="540ef-114">Maintaining multiple versions of a coverage group</span></span>

<span data-ttu-id="540ef-115">任意のアフォーダブル ケア法のグループの複数のバージョンを維持することができます。</span><span class="sxs-lookup"><span data-stu-id="540ef-115">You can maintain multiple versions of any coverage group.</span></span> <span data-ttu-id="540ef-116">この機能を使用すると、新しいグループを作成して従業員をそのグループに再配置せずに、変更を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="540ef-116">This functionality allows you to make changes without having to create a new group and reassign employees to it.</span></span> 

<span data-ttu-id="540ef-117">ACA 補償グループの作成後は、**一括割り当て** オプションを使用してそのグループを従業員に一括割り当てを行えます。</span><span class="sxs-lookup"><span data-stu-id="540ef-117">After you’ve created ACA coverage groups, you can mass assign the groups to employees with the **Mass assignment** option.</span></span> <span data-ttu-id="540ef-118">また、ACA情報の追跡と報告を行うかどうかを個別に指定し、従業員をアフォーダブルケアの補償グループに割り当てることもできます。</span><span class="sxs-lookup"><span data-stu-id="540ef-118">You can also individually indicate whether to track and report ACA information, and assign an employee to an Affordable Care coverage group.</span></span>

<span data-ttu-id="540ef-119">パートタイム従業員の場合など、すべての ACA 補償情報を追跡する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="540ef-119">You don't need to track some ACA coverage information, such as for part-time employees.</span></span> <span data-ttu-id="540ef-120">この場合、**レポート補充** フィールドを **いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="540ef-120">In this case, set the **Report coverage** field to **No**.</span></span> <span data-ttu-id="540ef-121">追跡可能な ACA 情報を持つ各従業員をアフォーダブルケアの補償グループに割り当てる必要がありますが、値の異なる月については、以下のオプションを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="540ef-121">Although you must assign each employee with trackable ACA information to an Affordable Care coverage group, you can still change the following options for months with different values:</span></span>

- <span data-ttu-id="540ef-122">**補償内容**</span><span class="sxs-lookup"><span data-stu-id="540ef-122">**Offer of coverage**</span></span>
- <span data-ttu-id="540ef-123">**費用の従業員負担**</span><span class="sxs-lookup"><span data-stu-id="540ef-123">**Employee share of cost**</span></span>
- <span data-ttu-id="540ef-124">**Safe Harbor**</span><span class="sxs-lookup"><span data-stu-id="540ef-124">**Safe Harbor**</span></span>

<span data-ttu-id="540ef-125">アフォーダブルケア補償グループ値の例外を入力するには、**労働者の詳細** ページの **雇用** タブの **追加情報** セクションで **アフォーダブルケアの補償** リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="540ef-125">To enter exceptions for Affordable Care coverage group values, select the **Affordable Care Coverage** link on the **Worker detail** page under the **Additional information** section on the **Employment tab**.</span></span>

## <a name="reporting-health-care-coverage"></a><span data-ttu-id="540ef-126">医療保険のレポート</span><span class="sxs-lookup"><span data-stu-id="540ef-126">Reporting health care coverage</span></span>

<span data-ttu-id="540ef-127">フルタイム従業員に提供された医療保険の追跡に加え、雇用主が従業員が加入している雇用主負担の自己負担の健康保険を提供している場合 (雇用形態がフルタイムかパートタイムかを問わず)、追加情報を 1095-C で報告する必要があります。</span><span class="sxs-lookup"><span data-stu-id="540ef-127">In addition to tracking health insurance coverage offered to full-time employees, if the employer offers employer-sponsored self-insured health coverage for which the employee is enrolled (regardless of whether their employment status is full-time or part-time), additional information needs to be reported on the 1095-C.</span></span> <span data-ttu-id="540ef-128">雇用主出資の福利厚生プランにより補償される各従業員 (被扶養者を含む) は、補償対象となった月のレポートに含められる必要があります。</span><span class="sxs-lookup"><span data-stu-id="540ef-128">Each employee (including dependents) covered by the employer-sponsored benefit plans needs to be included on the report for the months they were covered.</span></span> 

<span data-ttu-id="540ef-129">**ACA 報告** チェック ボックスをオンにすることで、各福利厚生プランを報告する必要があるかどうかを表示できます。</span><span class="sxs-lookup"><span data-stu-id="540ef-129">You can indicate whether or not each benefit plan must be reported by selecting the **ACA reportable** check box.</span></span>

<span data-ttu-id="540ef-130">また、従業員が扶養家族の誰を福利厚生の対象に選択した場合、**福利厚生の維持** ページに、各従業員の扶養家族が対象となった日付を表示できます。</span><span class="sxs-lookup"><span data-stu-id="540ef-130">In addition, if employees have chosen to have any of their dependents covered under a benefit, you can indicate the dates the dependent was covered for each employee on the **Maintain benefits** page.</span></span> <span data-ttu-id="540ef-131">被扶養者が給付金の対象となることを示すには、**被扶養者** クイック タブのアクション ウィンドウで **編集** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="540ef-131">To indicate that the dependent is covered under the benefit, select the **Edit** button in the action pane of the **Dependents** fast tab.</span></span>

<span data-ttu-id="540ef-132">**被扶養者の補償日マネージャー** ページで、給付金の対象となった日付を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="540ef-132">On the **Dependent coverage date manager** page, you can indicate the dates the dependent was covered by the benefit.</span></span> <span data-ttu-id="540ef-133">このページで日付を入力すると、**給付金の管理** ページで **対象** チェック ボックスが自動でオンになります。</span><span class="sxs-lookup"><span data-stu-id="540ef-133">Entering dates on this page will automatically select the **Covered** checkbox on the **Maintain benefits** page.</span></span>

## <a name="generate-1095-b-and-1095-c-forms"></a><span data-ttu-id="540ef-134">Form 1095-B および Form 1095-C</span><span class="sxs-lookup"><span data-stu-id="540ef-134">Generate 1095-B and 1095-C forms</span></span>

<span data-ttu-id="540ef-135">製品内から 1095-B および 1095-C フォームを生成し、各従業員に配布することもできます。</span><span class="sxs-lookup"><span data-stu-id="540ef-135">You can also generate 1095-B and 1095-C forms from within the product, and distribute them to each of your employees.</span></span> <span data-ttu-id="540ef-136">また、1095-C フォームおよび 1094-C IRS 送信ファイルを電子的に生成することもできます。</span><span class="sxs-lookup"><span data-stu-id="540ef-136">The system can also electronically generate 1095-C forms and the 1094-C IRS transmittal files.</span></span>  

<span data-ttu-id="540ef-137">1095-C フォームを生成する場合、該当する税年度を入力し、社会保障番号をマスキングすべきかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="540ef-137">When generating the 1095-C form, enter the appropriate tax year and indicate if social security numbers should be masked.</span></span> <span data-ttu-id="540ef-138">500 人を超える従業員に対して 1095-C フォームを印刷する場合は、2つ以上の PDF ファイルが送信されます。</span><span class="sxs-lookup"><span data-stu-id="540ef-138">If you're printing 1095-C forms for more than 500 employees, you'll receive more than one PDF file.</span></span> <span data-ttu-id="540ef-139">**ドキュメント管理パラメーター** ウィンドウで、**最大ファイル サイズ** を 150 MB に拡大することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="540ef-139">It’s recommended that you increase the **Maximum file size** in the **Document management parameters** window to 150 MB.</span></span>

## <a name="viewing-information"></a><span data-ttu-id="540ef-140">情報の表示</span><span class="sxs-lookup"><span data-stu-id="540ef-140">Viewing information</span></span>

<span data-ttu-id="540ef-141">**作業者の Affordable Care Act 補償** ページを使用して、どの従業員が各補償グループに割り当てられているか、どの従業員がレポートに含められる必要がないか、さらにどの従業員が割り当てられていないかを確認します。</span><span class="sxs-lookup"><span data-stu-id="540ef-141">You can use the **Worker Affordable Care coverage** page to see which employees have been assigned to each coverage group, which employees don’t need to be included on a report, and which employees are unassigned.</span></span>

<span data-ttu-id="540ef-142">アフォーダブルケア補償グループに由来する既定値のいずれかが上書きされた場合、変更された値の横にアスタリスクが表示されます。</span><span class="sxs-lookup"><span data-stu-id="540ef-142">If any of the default values from the Affordable Care coverage group have been overridden, an asterisk will appear next to the value that was changed.</span></span> <span data-ttu-id="540ef-143">12 か月すべての値が同じまたは上書きされていない場合、値が **12 か月すべて** 列で印刷されます。</span><span class="sxs-lookup"><span data-stu-id="540ef-143">If the values for all 12 months are the same and haven’t been overridden, the value will print in the **All 12 months** column.</span></span>

<span data-ttu-id="540ef-144">照会ウィンドウを使用して、どの従業員がACAの報告対象外としてフラグを立てられたかを把握することもできます。</span><span class="sxs-lookup"><span data-stu-id="540ef-144">You can also use the inquiry window to understand which employees have been flagged as not ACA reportable.</span></span> <span data-ttu-id="540ef-145">補償が提供されたかどうかを追跡する必要はなく、年度末に 1095-C を発行する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="540ef-145">You don’t need to track whether coverage was offered to them and won't need to issue a 1095-C to them at the end of the year.</span></span> <span data-ttu-id="540ef-146">**フィルタ方法** フィールドで **ACA報告不可** を選択すると、1095-C が送信されない従業員の一覧が生成されます。</span><span class="sxs-lookup"><span data-stu-id="540ef-146">Select **Not ACA reportable** in the **Filter by** field to generate a list of all employees who won't receive a 1095-C.</span></span>

<span data-ttu-id="540ef-147">また、未割り当ての従業員 (**ACA レポートの補償** フィールドが空欄)、または **年** フィールドで選択した年の有効期限が切れたアフォーダブルケアの補償グループに割り当てられている従業員を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="540ef-147">In addition, you can view any employees who are unassigned (the **ACA Report coverage** field is empty) or who have been assigned to an Affordable Care coverage group that is expired for the year selected in the **Year** field.</span></span>

<span data-ttu-id="540ef-148">Excel へのフィルター処理オプションのいずれかを使用して生成された従業員リストをエクスポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="540ef-148">You can export lists of employees that were generated using any of the filtering options to Excel.</span></span>

<span data-ttu-id="540ef-149">自己保険を提供している理由で、被保険者を報告する必要がある場合は、**ACAの報告対象** としてマークされている給付計画で被保険者となっている扶養家族を表示できます。</span><span class="sxs-lookup"><span data-stu-id="540ef-149">If you need to report covered individuals because you provide self-insured coverage, you can view any dependents covered under benefit plans marked as **ACA reportable**.</span></span> <span data-ttu-id="540ef-150">アクション ペインで **扶養家族の補償を表示する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="540ef-150">Select **View Dependent coverage** on the action pane.</span></span>

> [!NOTE]
> <span data-ttu-id="540ef-151">照会ウィンドウには、**ACA 報告可能** としてマークされている福利厚生計画のみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="540ef-151">Only benefit plans marked as **ACA reportable** display in the inquiry window.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]