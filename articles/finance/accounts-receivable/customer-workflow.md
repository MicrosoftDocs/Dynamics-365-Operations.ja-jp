---
title: 顧客ワークフロー
description: このトピックでは、顧客ワークフローに関する情報を提供します。 顧客の特定のフィールドを変更したら、その変更内容を顧客に追加する前に、承認のためワークフローを使用して送信します。
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: cb8519db2f5d52d4e317b485d6ecc910956788cb
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975319"
---
# <a name="customer-workflow"></a><span data-ttu-id="7834d-104">顧客ワークフロー</span><span class="sxs-lookup"><span data-stu-id="7834d-104">Customer workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7834d-105">顧客ワークフローがバージョン 8.0.4 に追加されました。</span><span class="sxs-lookup"><span data-stu-id="7834d-105">The customer workflow has been added to version 8.0.4.</span></span> <span data-ttu-id="7834d-106">顧客の特定のフィールドを変更したら、その変更内容を顧客に追加する前に、承認のためワークフローを使用して送信します。</span><span class="sxs-lookup"><span data-stu-id="7834d-106">You can change specific fields for a customer and then send those changes for approval by using the workflow before they are added to the customer.</span></span>

## <a name="set-up-the-customer-workflow"></a><span data-ttu-id="7834d-107">顧客ワークフローの設定</span><span class="sxs-lookup"><span data-stu-id="7834d-107">Set up the customer workflow</span></span>

<span data-ttu-id="7834d-108">顧客ワークフロー機能を使用するには、事前に有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7834d-108">Before you can use the customer workflow feature, you must enable it.</span></span>

1. <span data-ttu-id="7834d-109">**売掛金勘定 \> 設定 \> 売掛金勘定パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="7834d-109">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="7834d-110">**全般** タブの **顧客の承認** クイック タブで、**顧客の承認を有効にする** オプションを **はい** に設定して機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="7834d-110">On the **General** tab, on the **Customer approval** FastTab, set the **Enable customer approvals** option to **Yes** to enable the feature.</span></span>
3. <span data-ttu-id="7834d-111">**データエンティティの挙動** フィールドで、データのインポート時に、データ エンティティが使用する動作を選択します。</span><span class="sxs-lookup"><span data-stu-id="7834d-111">In the **Data entity behavior** field, select the behavior that the data entities should use when data is imported:</span></span>

    - <span data-ttu-id="7834d-112">**承認なしの変更を許可する** : エンティティは顧客レコードを、ワークフローで処理せずに更新できます。</span><span class="sxs-lookup"><span data-stu-id="7834d-112">**Allow changes without approval** – An entity can update the customer record without processing it through the workflow.</span></span>
    - <span data-ttu-id="7834d-113">**変更を元に戻す** : 顧客レコードに変更を加えることはできません。</span><span class="sxs-lookup"><span data-stu-id="7834d-113">**Reject changes** – Changes can't be made to the customer record.</span></span> <span data-ttu-id="7834d-114">ワークフローに対して有効化されているフィールドの場合、インポートでエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="7834d-114">The import will fail for the fields that are enabled for the workflow.</span></span>
    - <span data-ttu-id="7834d-115">**変更提案を作成する** : ワークフローに対して有効化されているフィールドを除くすべてのフィールドが変更されます。</span><span class="sxs-lookup"><span data-stu-id="7834d-115">**Create change proposals** – All fields will be changed except the fields that are enabled for the workflow.</span></span> <span data-ttu-id="7834d-116">これらのフィールドの新しい値は、変更の提案として顧客に追加され、ワークフローが自動的に開始されます。</span><span class="sxs-lookup"><span data-stu-id="7834d-116">The new values for those fields will be added to the customer as proposed changes, and the workflow will be started automatically.</span></span>

4. <span data-ttu-id="7834d-117">変更を行う前に、顧客のフィールドの一覧で、承認するすべてのフィールドの **有効にする** チェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="7834d-117">In the list of customer fields, select then **Enable** check box for every field that must be approved before the changes can be made.</span></span>
5. <span data-ttu-id="7834d-118">**売掛金勘定 \> 設定 \> 売掛金勘定ワークフロー** に移動します。</span><span class="sxs-lookup"><span data-stu-id="7834d-118">Go to **Accounts receivable \> Setup \> Accounts receivable workflows**.</span></span>
6. <span data-ttu-id="7834d-119">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7834d-119">Select **New**.</span></span>
7. <span data-ttu-id="7834d-120">**顧客に対する提案済み変更内容に関するワークフロー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7834d-120">Select **Proposed customer change workflow**.</span></span> 
8. <span data-ttu-id="7834d-121">承認プロセスに合わせてワークフローを設定します。</span><span class="sxs-lookup"><span data-stu-id="7834d-121">Set up the workflow so that it matches your approval process.</span></span> <span data-ttu-id="7834d-122">**顧客に対する提案済み変更内容に対するワークフロー承認** ワークフロー承認要素が顧客に変更を適用します。</span><span class="sxs-lookup"><span data-stu-id="7834d-122">The **Workflow approval for proposed customer change** workflow approval element will apply the changes to the customer.</span></span>

## <a name="change-customer-information-and-submit-the-changes-to-the-workflow"></a><span data-ttu-id="7834d-123">顧客情報の変更とワークフローへの変更の送信</span><span class="sxs-lookup"><span data-stu-id="7834d-123">Change customer information and submit the changes to the workflow</span></span>

<span data-ttu-id="7834d-124">ワークフローに対して有効化されているフィールドを変更する場合、**提案済みの変更** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7834d-124">When you change a field that is enabled for the workflow, the **Proposed changes** page appears.</span></span> <span data-ttu-id="7834d-125">このページでは、フィールドの元の値と入力した新しい値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7834d-125">This page shows the original value of the field and the new value that you entered.</span></span> <span data-ttu-id="7834d-126">変更したフィールドは、元の値に戻されます。</span><span class="sxs-lookup"><span data-stu-id="7834d-126">The field that you changed is reverted to its original value.</span></span> <span data-ttu-id="7834d-127">ページのステータス メッセージにより、変更内容が送信されなかったことが通知されます。</span><span class="sxs-lookup"><span data-stu-id="7834d-127">A status message on the page informs you that your changes haven't been submitted.</span></span>

<span data-ttu-id="7834d-128">ワークフローに対して有効化されているフィールドを変更するたびに、そのフィールドは提案済みの変更のリストに追加されます。</span><span class="sxs-lookup"><span data-stu-id="7834d-128">Every time that you change a field that is enabled for the workflow, that field is added to the list of proposed changes.</span></span> <span data-ttu-id="7834d-129">フィールドの提案値を破棄するには、リストのフィールド名の横にある **破棄** ボタンを使用します。</span><span class="sxs-lookup"><span data-stu-id="7834d-129">To discard the proposed value for a field, use the **Discard** button next to the field in the list.</span></span> <span data-ttu-id="7834d-130">すべての変更を破棄するには、ページの下部にある **すべての変更を破棄** ボタンを使用します。</span><span class="sxs-lookup"><span data-stu-id="7834d-130">To discard all changes, use the **Discard all change** button at the bottom of the page.</span></span> <span data-ttu-id="7834d-131">**OK** を選択してページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7834d-131">Select **OK** to close the page.</span></span>

<span data-ttu-id="7834d-132">提案済みの変更が 1 つ以上ある場合、アクション ウィンドウ上に **提案済みの変更** と **ワークフロー** の 2 つのメニューがさらに表示されます</span><span class="sxs-lookup"><span data-stu-id="7834d-132">After you have at least one proposed change, two additional menus appear on the Action Pane: **Proposed changes** and **Workflow**.</span></span>

1. <span data-ttu-id="7834d-133">**提案済み変更** を選択して **提案済み変更** ページを開き、変更内容を確認してください。</span><span class="sxs-lookup"><span data-stu-id="7834d-133">Select **Proposed changes** to open the **Proposed changes** page and review your changes.</span></span>
2. <span data-ttu-id="7834d-134">**ワークフロー \> 送信** を選択して変更内容をワークフローに送信します。</span><span class="sxs-lookup"><span data-stu-id="7834d-134">Select **Workflow \> Submit** to submit the changes to the workflow.</span></span>

    <span data-ttu-id="7834d-135">ページの状態が**変更の承認待ち**に変わります。</span><span class="sxs-lookup"><span data-stu-id="7834d-135">The status on the page is changed to **Changes pending approval**.</span></span>

<span data-ttu-id="7834d-136">ワークフローは、アプリケーションの標準的なワークフロー プロセスに従います。</span><span class="sxs-lookup"><span data-stu-id="7834d-136">The workflow follows the standard workflow process in the application.</span></span> <span data-ttu-id="7834d-137">承認者は**顧客**ページに転送され、そこで**提案済みの変更**ページの変更を確認してから**ワークフロー \> 承認**を選択してワークフローを承認します。</span><span class="sxs-lookup"><span data-stu-id="7834d-137">The approver is directed to the **Customer** page, where he or she can review the changes on the **Proposed changes** page and then select **Workflow \> Approve** to approve the workflow.</span></span> <span data-ttu-id="7834d-138">すべての承認が完了すると、フィールドは提示した値に更新されます。</span><span class="sxs-lookup"><span data-stu-id="7834d-138">After all approvals are completed, the fields are updated with the values that you proposed.</span></span>
