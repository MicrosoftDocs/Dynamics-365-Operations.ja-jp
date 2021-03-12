---
title: 不適合管理の前提条件を設定する
description: このトピックを使用して不適合管理プロセスを有効化します。
author: perlynne
manager: tfehr
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, SysUserManagement, SysUserSetup, InventTestDiagnosticType, InventTestMiscCharges, InventTestOperation, InventProblemType, InventProblemTypeSetup, InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 80a7ae2249179c561d03f7b729ebb942ba856046
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4961523"
---
# <a name="set-up-prerequisites-for-nonconformance-management"></a><span data-ttu-id="9f184-103">不適合管理の前提条件を設定する</span><span class="sxs-lookup"><span data-stu-id="9f184-103">Set up prerequisites for nonconformance management</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9f184-104">このトピックを使用して不適合管理プロセスを有効化します。</span><span class="sxs-lookup"><span data-stu-id="9f184-104">Use this topic to enable nonconformance management processes.</span></span> <span data-ttu-id="9f184-105">不適合とは、品質上の問題がある手順または品目を表し、その説明には問題の原因およびタイプが含まれます。</span><span class="sxs-lookup"><span data-stu-id="9f184-105">A nonconformance describes a procedure or item that has a quality problem, where the descriptive information includes the source and type of problem.</span></span> <span data-ttu-id="9f184-106">この手順では、デモ データの会社 USMF を使用します。</span><span class="sxs-lookup"><span data-stu-id="9f184-106">This procedure uses the USMF demo data company.</span></span> <span data-ttu-id="9f184-107">通常この手順は品質マネージャーが実施します。</span><span class="sxs-lookup"><span data-stu-id="9f184-107">This procedure is typically performed by a quality manager.</span></span>


## <a name="enable-quality-management-processes-within-the-company"></a><span data-ttu-id="9f184-108">社内品質管理プロセスの有効化</span><span class="sxs-lookup"><span data-stu-id="9f184-108">Enable quality management processes within the company</span></span>
1. <span data-ttu-id="9f184-109">ナビゲーション ウィンドウで、**モジュール > 在庫管理 > 設定 > 在庫および倉庫管理パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9f184-109">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory and warehouse management parameters**.</span></span>
2. <span data-ttu-id="9f184-110">**品質管理** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="9f184-110">Select the **Quality management** tab.</span></span>
3. <span data-ttu-id="9f184-111">**品質管理を使用する** フィールドで **はい** を選択して、会社の品質管理プロセスを有効にします。</span><span class="sxs-lookup"><span data-stu-id="9f184-111">Select **Yes** in the **Use quality management** field to enable quality management processes for the company.</span></span>
4. <span data-ttu-id="9f184-112">**時間レート** フィールドに、国内通貨で数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9f184-112">In the **Hourly rate** field, enter a number in the local currency.</span></span> <span data-ttu-id="9f184-113">時給レートは、不適合に関連する工程の原価計算に使用されます。</span><span class="sxs-lookup"><span data-stu-id="9f184-113">The hourly rate is used for calculating costs for operations that are related to a nonconformance.</span></span> <span data-ttu-id="9f184-114">時間あたりのレートと算出原価は、不適合の参照情報を提供するものであり、他の機能に作用することはありません。</span><span class="sxs-lookup"><span data-stu-id="9f184-114">The hourly rate and calculated costs provide reference information for a nonconformance, and they do not interact with other functionality.</span></span>  
5. <span data-ttu-id="9f184-115">**レポートの設定** を選択して、異なる種類の品質管理レポートで使用される品質レポートのメモのタイプを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="9f184-115">Select **Report setup** to define the quality report note types that will be used on different kinds of quality management reports.</span></span>

## <a name="enable-user-for-nonconformance-processing"></a><span data-ttu-id="9f184-116">不適合処理に対しユーザーを有効化</span><span class="sxs-lookup"><span data-stu-id="9f184-116">Enable user for nonconformance processing</span></span>
1. <span data-ttu-id="9f184-117">ナビゲーション ウィンドウで、**モジュール > システム管理 > ユーザー > ユーザー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9f184-117">In the navigation pane, go to **Modules > System administration > Users > Users**.</span></span> 
2. <span data-ttu-id="9f184-118">クイック フィルターを使用して不適合のレコードを承認または否認するユーザーを検索します。</span><span class="sxs-lookup"><span data-stu-id="9f184-118">Use the Quick Filter to find the user who will be approving or rejecting the nonconformance records.</span></span> <span data-ttu-id="9f184-119">たとえば、値 `Ricardo` を含む **名前** フィールドをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="9f184-119">For example, filter on the **Name** field with a value of `Ricardo`.</span></span> <span data-ttu-id="9f184-120">不適合の承認を処理する場合、不適合を承認または否認するユーザーは、**ユーザー** ページで "名前" の値が割り当てられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f184-120">To process the approval of a nonconformance, the user who approves or rejects nonconformances must have a "Name" value assigned on the **Users** page.</span></span> <span data-ttu-id="9f184-121">ドキュメントのメモを使用するには、ユーザー オプションで [ドキュメントの処理] も有効化されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f184-121">To use the document notes, the user must also have Document handling activated in the user options.</span></span>  
3. <span data-ttu-id="9f184-122">目的のレコードの行をマークします。</span><span class="sxs-lookup"><span data-stu-id="9f184-122">Mark the row of the desired record.</span></span>
4. <span data-ttu-id="9f184-123">**ユーザー オプション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f184-123">Select **User options**.</span></span>
5. <span data-ttu-id="9f184-124">**基本設定** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="9f184-124">Select the **Preferences** tab.</span></span>
6. <span data-ttu-id="9f184-125">**ドキュメントの処理の有効化** フィールドで **はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f184-125">Select **Yes** in the **Enable document handling** field.</span></span>

## <a name="define-diagnostic-types-for-nonconformance-processing"></a><span data-ttu-id="9f184-126">不適合処理の診断タイプの定義</span><span class="sxs-lookup"><span data-stu-id="9f184-126">Define diagnostic types for nonconformance processing</span></span>
1. <span data-ttu-id="9f184-127">ナビゲーション ウィンドウで、**モジュール > 在庫管理 > 設定 > 品質管理 > 診断タイプ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9f184-127">In the navigation pane, go to **Modules > Inventory management > Setup > Quality management > Diagnostic types**.</span></span> <span data-ttu-id="9f184-128">診断アクションの分類を定義するためには、**診断タイプ** ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="9f184-128">Use the **Diagnostic types** page to define a classification of diagnostic actions.</span></span> <span data-ttu-id="9f184-129">訂正は、承認された不適合に対して行う必要のある診断アクションのタイプ、担当者、要求された完了日、予定の完了日などを識別します。</span><span class="sxs-lookup"><span data-stu-id="9f184-129">A correction identifies what type of diagnostic action should be taken on an approved nonconformance, who should perform it, and the requested and planned completion date.</span></span>  
2. <span data-ttu-id="9f184-130">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f184-130">Select **New**.</span></span>
3. <span data-ttu-id="9f184-131">**診断** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9f184-131">In the **Diagnostic** field, type a value.</span></span>
4. <span data-ttu-id="9f184-132">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9f184-132">In the **Description** field, type a value.</span></span>

## <a name="define-quality-charges-for-nonconformance-processing"></a><span data-ttu-id="9f184-133">不適合処理の品質諸費用の定義</span><span class="sxs-lookup"><span data-stu-id="9f184-133">Define quality charges for nonconformance processing</span></span>
1. <span data-ttu-id="9f184-134">ナビゲーション ウィンドウで、**モジュール > 在庫管理 > 設定 > 品質管理 > 品質諸費用** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9f184-134">In the navigation pane, go to **Modules > Inventory management > Setup > Quality management > Quality charges**.</span></span> <span data-ttu-id="9f184-135">**品質諸費用** ページを使用して、不適合に関連する行程で使用される請求の分類を定義します。</span><span class="sxs-lookup"><span data-stu-id="9f184-135">Use the **Quality charges** page to define a classification of charges that will used in operations related to nonconformances.</span></span>  
2. <span data-ttu-id="9f184-136">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f184-136">Select **New**.</span></span>
3. <span data-ttu-id="9f184-137">**諸費用コード** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9f184-137">In the **Charges code** field, type a value.</span></span>
4. <span data-ttu-id="9f184-138">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9f184-138">In the **Description** field, type a value.</span></span>

## <a name="define-the-operations-for-nonconformance-processing"></a><span data-ttu-id="9f184-139">不適合処理の行程の定義</span><span class="sxs-lookup"><span data-stu-id="9f184-139">Define the operations for nonconformance processing</span></span>
1. <span data-ttu-id="9f184-140">ナビゲーション ウィンドウで、**モジュール > 在庫管理 > 設定 > 品質管理 > 工程** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9f184-140">In the navigation pane, go to **Modules > Inventory management > Setup > Quality management > Operations**.</span></span> <span data-ttu-id="9f184-141">**工程** ページを使用して、承認済の不適合に対して実行することができる作業の分類を定義します。</span><span class="sxs-lookup"><span data-stu-id="9f184-141">Use the **Operations** page to define a classification of the work that may be performed for an approved nonconformance.</span></span> <span data-ttu-id="9f184-142">行程をを不適合に関連付ける際、その操作を実行するために必要な関連する材料、労働時間、雑費などの情報を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="9f184-142">When you relate an operation to a nonconformance, you can define information about the associated material, labor hours, and miscellaneous charges that are required to perform the operation.</span></span> <span data-ttu-id="9f184-143">この情報は、この工程を実行するための見積原価を計算する基準を提供します。</span><span class="sxs-lookup"><span data-stu-id="9f184-143">This information provides the basis for calculating an estimated cost for performing the operation.</span></span>  
2. <span data-ttu-id="9f184-144">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f184-144">Select **New**.</span></span>
3. <span data-ttu-id="9f184-145">**工程** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9f184-145">In the **Operation** field, type a value.</span></span>
4. <span data-ttu-id="9f184-146">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9f184-146">In the **Description** field, type a value.</span></span>

## <a name="define-problem-types-for-nonconformance-processing"></a><span data-ttu-id="9f184-147">不適合処理の問題タイプの定義</span><span class="sxs-lookup"><span data-stu-id="9f184-147">Define problem types for nonconformance processing</span></span>
1. <span data-ttu-id="9f184-148">ナビゲーション ウィンドウで、**モジュール > 在庫管理 > 設定 > 品質管理 > 問題タイプ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9f184-148">In the navigation pane, go to **Modules > Inventory management > Setup > Quality management > Problem types**.</span></span> <span data-ttu-id="9f184-149">**問題タイプ** ページを使用して、さまざまな不適合タイプで発生する品質上の問題の分類を定義します。</span><span class="sxs-lookup"><span data-stu-id="9f184-149">Use the **Problem types** page to define a classification of quality problems that are encountered in the various nonconformance types.</span></span> <span data-ttu-id="9f184-150">不適合タイプには、**内部**、**顧客**、**仕入先**、**サービス要求**、**生産** および **連産品の生産** があります。</span><span class="sxs-lookup"><span data-stu-id="9f184-150">The nonconformance types include **Internal**, **Customer**, **Vendor**, **Service request**, **Production**, and **Co-product production**.</span></span> <span data-ttu-id="9f184-151">1 つの問題タイプを複数の不適合タイプに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="9f184-151">A single problem type can be associated with multiple nonconformance types.</span></span>  
2. <span data-ttu-id="9f184-152">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f184-152">Select **New**.</span></span>
3. <span data-ttu-id="9f184-153">**問題タイプ** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9f184-153">In the **Problem type** field, type a value.</span></span>
4. <span data-ttu-id="9f184-154">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9f184-154">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="9f184-155">**不適合タイプ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f184-155">Select **Non conformance types**.</span></span> <span data-ttu-id="9f184-156">**不適合タイプ** ページを使用して、1 つ以上の不適合タイプでの問題タイプの使用を承認します。</span><span class="sxs-lookup"><span data-stu-id="9f184-156">Use the **Non conformance types** page to authorize the use of a problem type for one or more of the nonconformance types.</span></span> <span data-ttu-id="9f184-157">たとえば、欠陥コードに関連した問題タイプは、すべての不適合タイプに適用できます。一方、顧客の苦情に関する問題タイプは、顧客およびサービス要求の不適合タイプにしか適用できません。</span><span class="sxs-lookup"><span data-stu-id="9f184-157">For example, a problem type regarding a defect code could apply to all nonconformance types, whereas a problem type about customer complaints may only apply to the customer and service request nonconformance types.</span></span>  
6. <span data-ttu-id="9f184-158">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f184-158">Select **New**.</span></span>
7. <span data-ttu-id="9f184-159">新しい行の **不適合タイプ** フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="9f184-159">In the **Non conformance type** field of the new row, select an option.</span></span>

## <a name="define-quarantine-zones-for-nonconformance-processing"></a><span data-ttu-id="9f184-160">不適合処理の検査ゾーンの定義</span><span class="sxs-lookup"><span data-stu-id="9f184-160">Define quarantine zones for nonconformance processing</span></span>
1. <span data-ttu-id="9f184-161">ナビゲーション ウィンドウで、**モジュール > 在庫管理 > 設定 > 品質管理 > 検査ゾーン** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9f184-161">In the navigation pane, go to **Modules > Inventory management > Setup > Quality management > Quarantine zones**.</span></span>
2. <span data-ttu-id="9f184-162">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f184-162">Select **New**.</span></span>
3. <span data-ttu-id="9f184-163">**検査ゾーン** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9f184-163">In the **Quarantine zone** field, type a value.</span></span>
4. <span data-ttu-id="9f184-164">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9f184-164">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="9f184-165">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9f184-165">Close the page.</span></span>

