---
title: 共有番号順序を使用して、顧客をコピーする
description: このトピックでは、同じ顧客 ID を維持したまま共有番号順序を使用して顧客を別の法人にコピーする方法について、説明します。
author: mikefalkner
manager: aolson
ms.date: 08/31/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 91f7568ea8364f97de7e514fb207191ee00041a5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4459365"
---
# <a name="copy-customers-by-using-shared-number-sequences"></a><span data-ttu-id="6e238-103">共有番号順序を使用して、顧客をコピーする</span><span class="sxs-lookup"><span data-stu-id="6e238-103">Copy customers by using shared number sequences</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e238-104">共有番号順序を使用して、顧客 ID を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="6e238-104">You can use shared number sequences to assign customer IDs.</span></span> <span data-ttu-id="6e238-105">また、共有番号順序を使用して、同じ顧客 ID を維持したまま、法人間で顧客をコピーすることもできます。</span><span class="sxs-lookup"><span data-stu-id="6e238-105">Shared number sequences also let you copy customers from one legal entity to another legal entity but use the same customer IDs in both legal entities.</span></span>

## <a name="setup"></a><span data-ttu-id="6e238-106">セットアップ</span><span class="sxs-lookup"><span data-stu-id="6e238-106">Setup</span></span>

<span data-ttu-id="6e238-107">この機能が有効化されるのは、共有番号順序を使用して顧客 ID を割り当てる場合です。</span><span class="sxs-lookup"><span data-stu-id="6e238-107">The feature is activated when you use a shared number sequence to assign customer IDs.</span></span> <span data-ttu-id="6e238-108">顧客のコピー先となるすべての法人内で、同じ番号順序を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e238-108">You must use the same number sequence in every legal entity that you want to copy a customer to.</span></span> <span data-ttu-id="6e238-109">顧客番号順序を変更するには、各法人に対する **売掛金パラメーター** ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="6e238-109">You change the customer number sequence on the **Accounts receivable parameters** page for each legal entity.</span></span> <span data-ttu-id="6e238-110">**売掛金** \> **パラメーター** を選択し、**番号順序** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="6e238-110">Select **Accounts receivable** \> **Parameters**, and then select the **Number sequences** tab.</span></span>

<span data-ttu-id="6e238-111">各顧客グループに対して顧客番号順序を指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="6e238-111">You can also set up customer number sequences for each customer group.</span></span> <span data-ttu-id="6e238-112">また、これらの番号順序を共有する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e238-112">These number sequences must also be shared.</span></span> <span data-ttu-id="6e238-113">顧客グループに対する番号順序が最初に使用されます。</span><span class="sxs-lookup"><span data-stu-id="6e238-113">The number sequence for a customer group is used first.</span></span> <span data-ttu-id="6e238-114">顧客グループに対して番号順序を指定しない場合、**売掛金パラメーター** ページで指定した番号順序が使用されます。</span><span class="sxs-lookup"><span data-stu-id="6e238-114">If no number sequence is specified for a customer group, the number sequence that is specified on the **Accounts receivable parameters** page is used.</span></span>

<span data-ttu-id="6e238-115">手動顧客 ID を使用する場合、法人間で顧客をコピーすることもできます。</span><span class="sxs-lookup"><span data-stu-id="6e238-115">You can also copy customers between legal entities if you use manual customer IDs.</span></span> <span data-ttu-id="6e238-116">ただし、顧客 ID が既に存在している法人に顧客をコピーしようとした場合、コピー プロセスは開始しません。</span><span class="sxs-lookup"><span data-stu-id="6e238-116">However, if you try to copy a customer to a legal entity where the customer ID already exists, the copy process won't be started.</span></span>

## <a name="copy-a-customer"></a><span data-ttu-id="6e238-117">顧客をコピーする</span><span class="sxs-lookup"><span data-stu-id="6e238-117">Copy a customer</span></span>

<span data-ttu-id="6e238-118">顧客をコピーするには、**すべての顧客** リスト ページで **新規** を選択し、**顧客を作成** ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="6e238-118">To copy a customer, select **New** on the **All customers** list page to open the **Create customer** dialog box.</span></span> <span data-ttu-id="6e238-119">新規顧客 ID は、すぐには割り当てられません。</span><span class="sxs-lookup"><span data-stu-id="6e238-119">Notice that the new customer ID isn't assigned immediately.</span></span> <span data-ttu-id="6e238-120">この挙動は旧バージョンとは異なります。</span><span class="sxs-lookup"><span data-stu-id="6e238-120">This behavior differs from the behavior in previous versions.</span></span> <span data-ttu-id="6e238-121">顧客グループが選択されていないため、使用する正しい番号順序を決定できません。</span><span class="sxs-lookup"><span data-stu-id="6e238-121">Because you haven't yet selected the customer group, the system can't determine the correct number sequence to use.</span></span> <span data-ttu-id="6e238-122">また、顧客を新規に作成しようとしているのか、それとも顧客をコピーしようとしているのか、を判断できません。</span><span class="sxs-lookup"><span data-stu-id="6e238-122">Additionally, it can't determine whether you're trying to create a new customer or copy a customer.</span></span> <span data-ttu-id="6e238-123">したがって、ダイアログ ボックスの下端にある **保存** を選択するまで、顧客 ID は割り当てられません。</span><span class="sxs-lookup"><span data-stu-id="6e238-123">Therefore, the customer ID isn't assigned until you select **Save** at the bottom of the dialog box.</span></span>

<span data-ttu-id="6e238-124">顧客を新規に作成する場合、今までどおり、すべてのフィールドの値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="6e238-124">If you're creating a new customer, you can continue to fill in all the fields as you usually do.</span></span> <span data-ttu-id="6e238-125">フィールド値をすべて指定して **保存** を選択すると、顧客 ID が自動的に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="6e238-125">When you've finished, and you select **Save**, you will see that the customer ID was assigned automatically.</span></span> <span data-ttu-id="6e238-126">手動番号順序の場合は、手動顧客 ID が使用されます。</span><span class="sxs-lookup"><span data-stu-id="6e238-126">Alternatively, for manual number sequences, you will see that your manual customer ID was used.</span></span>

<span data-ttu-id="6e238-127">**名前** フィールドに顧客をコピーするには、探している顧客を表す 1 つ以上の文字を入力します。</span><span class="sxs-lookup"><span data-stu-id="6e238-127">To copy a customer, in the **Name** field, enter one or more characters that represent the customer that you're looking for.</span></span> <span data-ttu-id="6e238-128">検索ダイアログ ボックスに、探している顧客の可能性がある関係者が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="6e238-128">A search dialog box shows a list of parties that might represent the customer that you're looking for.</span></span> <span data-ttu-id="6e238-129">いずれかの関係者を選択すると、ダイアログ ボックスの右部に詳細情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6e238-129">When you select one of the parties, additional information appears on the right side of the dialog box:</span></span>

- <span data-ttu-id="6e238-130">**全般** タブ ページには、その関係者の電話番号と住所が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6e238-130">The **General** tab shows the party's phone number and address.</span></span>
- <span data-ttu-id="6e238-131">**ロール** タブ ページには、その関係者に割り当て可能なロール、および、どの法人内で各ロールがその関係者に割り当てられるか、が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6e238-131">The **Roles** tab shows the roles that the selected party can have and the legal entity where it has each role.</span></span>
- <span data-ttu-id="6e238-132">**税登録 ID** タブ ページには、その関係者に割り当てられている税登録 ID が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6e238-132">**Tax registration ID** tab shows the tax registration IDs that are assigned to the party.</span></span>

<span data-ttu-id="6e238-133">関係者をコピーできるのは、その関係者に顧客ロールが割り当てられている場合、および、現在の法人以外の法人内でその関係者にロールが割り当てられている場合だけです。</span><span class="sxs-lookup"><span data-stu-id="6e238-133">You can copy a party only if it has a customer role, and if it has that role in a legal entity that isn't the current legal entity.</span></span> <span data-ttu-id="6e238-134">これらの条件を満たす関係者を探すには、次のステップを実行します。</span><span class="sxs-lookup"><span data-stu-id="6e238-134">When you find a party that meets these criteria, follow these steps.</span></span>

1. <span data-ttu-id="6e238-135">**顧客をコピー** オプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6e238-135">A **Copy customer** option appears.</span></span> <span data-ttu-id="6e238-136">このオプションの既定値は **いいえ** です。</span><span class="sxs-lookup"><span data-stu-id="6e238-136">By default, this option is set to **No**.</span></span> <span data-ttu-id="6e238-137">顧客を現在の法人にコピーするには、このオプションで **はい** を指定します。</span><span class="sxs-lookup"><span data-stu-id="6e238-137">To copy the customer to the current legal entity, set the option to **Yes**.</span></span> 
2. <span data-ttu-id="6e238-138">**法人** フィールドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6e238-138">A **Legal entity** field appears.</span></span> <span data-ttu-id="6e238-139">顧客のコピー元となる法人を選択します。</span><span class="sxs-lookup"><span data-stu-id="6e238-139">Select the legal entity to copy the customer from.</span></span> <span data-ttu-id="6e238-140">顧客が 1 つの法人内にのみ存在している場合、このフィールドの既定値はその法人になります。</span><span class="sxs-lookup"><span data-stu-id="6e238-140">If the customer exists in only one legal entity, the field is set to that legal entity by default.</span></span>
3. <span data-ttu-id="6e238-141">**選択** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6e238-141">Select **Select**.</span></span> <span data-ttu-id="6e238-142">顧客が新規に作成されます。</span><span class="sxs-lookup"><span data-stu-id="6e238-142">The new customer is created.</span></span>

## <a name="validation"></a><span data-ttu-id="6e238-143">妥当性確認</span><span class="sxs-lookup"><span data-stu-id="6e238-143">Validation</span></span>

<span data-ttu-id="6e238-144">顧客をコピーする際、新規顧客情報の保存が試みられます。</span><span class="sxs-lookup"><span data-stu-id="6e238-144">When you copy a customer, the system tries to save the new customer information.</span></span> <span data-ttu-id="6e238-145">妥当性確認処理が実行され、コピーされたデータが正しいかどうかが検証されます。</span><span class="sxs-lookup"><span data-stu-id="6e238-145">Validations are run to verify that the data that was copied is good.</span></span> <span data-ttu-id="6e238-146">妥当性確認処理で不合格になった場合、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6e238-146">You receive an error message for every validation that fails.</span></span> <span data-ttu-id="6e238-147">エラー メッセージの中で、更新する必要のある情報について説明されています。</span><span class="sxs-lookup"><span data-stu-id="6e238-147">The error messages explain what information must be updated.</span></span> <span data-ttu-id="6e238-148">すべての妥当性確認エラーを修正するまで、顧客のコピーを保存することはできません。</span><span class="sxs-lookup"><span data-stu-id="6e238-148">The copy of the customer can't be saved until you fix all the validation errors.</span></span>

## <a name="copy-a-customer-by-using-tax-exempt-number-search-feature"></a><span data-ttu-id="6e238-149">課税控除番号検索機能を使用して顧客をコピーする</span><span class="sxs-lookup"><span data-stu-id="6e238-149">Copy a customer by using tax exempt number search feature</span></span>

<span data-ttu-id="6e238-150">**すべての顧客** ページのアクション ペインの **顧客** タブで、**登録** グループにある課税控除番号検索機能を利用して、顧客をコピーすることもできます。</span><span class="sxs-lookup"><span data-stu-id="6e238-150">You can also copy customers by using the Tax exempt number search feature that is in the **Registration** group on the **Customer** tab on the Action Pane of the **All customers** page.</span></span> <span data-ttu-id="6e238-151">**課税控除番号検索** ダイアログ ボックスが開き、課税控除番号、顧客 ID、顧客名、および、どの法人内で課税控除 ID が使用されるか、が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6e238-151">The **Tax exempt number search** dialog box that appears shows tax exempt numbers, the customer ID, the customer name, and the legal entity where the tax exempt ID is used.</span></span> <span data-ttu-id="6e238-152">顧客をコピーできるのは、現在の法人でない法人内に存在している場合だけです。</span><span class="sxs-lookup"><span data-stu-id="6e238-152">You can copy a customer only if it's in a legal entity that isn't the current legal entity.</span></span> <span data-ttu-id="6e238-153">この条件を満たす顧客を選択したら、次ステップを実行します。</span><span class="sxs-lookup"><span data-stu-id="6e238-153">After you select a customer that meets this criterion, follow these steps.</span></span>

1. <span data-ttu-id="6e238-154">**顧客をコピー** オプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6e238-154">A **Copy customer** option appears.</span></span> <span data-ttu-id="6e238-155">このオプションの既定値は **いいえ** です。</span><span class="sxs-lookup"><span data-stu-id="6e238-155">By default, this option is set to **No**.</span></span> <span data-ttu-id="6e238-156">顧客を現在の法人にコピーするには、このオプションで **はい** を指定します。</span><span class="sxs-lookup"><span data-stu-id="6e238-156">To copy the customer to the current legal entity, set the option to **Yes**.</span></span> 
2. <span data-ttu-id="6e238-157">**選択** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6e238-157">Select **Select**.</span></span> <span data-ttu-id="6e238-158">顧客が新規に作成されます。</span><span class="sxs-lookup"><span data-stu-id="6e238-158">The new customer is created.</span></span>
