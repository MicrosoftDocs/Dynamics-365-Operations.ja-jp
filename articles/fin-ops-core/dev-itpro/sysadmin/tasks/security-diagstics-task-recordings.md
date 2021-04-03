---
title: タスク記録のセキュリティ診断
description: このトピックでは、タスクの記録に基づいてセキュリティ許可要件を分析して管理する方法について説明します。
author: Peakerbl
manager: AnnBe
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.openlocfilehash: 99f9da527e818892eb3f46aceca3cc4588b99e81
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570984"
---
# <a name="security-diagnostics-for-task-recordings"></a><span data-ttu-id="2cec5-103">タスク記録のセキュリティ診断</span><span class="sxs-lookup"><span data-stu-id="2cec5-103">Security diagnostics for task recordings</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a><span data-ttu-id="2cec5-104">準備</span><span class="sxs-lookup"><span data-stu-id="2cec5-104">Before you begin</span></span>

<span data-ttu-id="2cec5-105">このトピックでは、タスクの記録に基づいてセキュリティ許可要件を分析して管理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2cec5-105">This topic provides information about how to analyze and manage security permission requirements based on a task recording.</span></span> <span data-ttu-id="2cec5-106">このトピックのステップを完了する前に、分析する業務プロセスのタスク記録を保持している必要があります。</span><span class="sxs-lookup"><span data-stu-id="2cec5-106">Before you complete the steps in this topic, you must have a task recording of the business process that you want to analyze.</span></span> <span data-ttu-id="2cec5-107">業務プロセスを記録するには、[タスクレコーダーのリソース](../../user-interface/task-recorder.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2cec5-107">To record a business process, see [Task recorder resources](../../user-interface/task-recorder.md).</span></span> 

## <a name="manage-security-for-a-task-recording"></a><span data-ttu-id="2cec5-108">タスク記録のセキュリティ管理</span><span class="sxs-lookup"><span data-stu-id="2cec5-108">Manage security for a task recording</span></span>

1. <span data-ttu-id="2cec5-109">**システム管理** > **セキュリティ** > **タスク記録のセキュリティ診断** に移動します。</span><span class="sxs-lookup"><span data-stu-id="2cec5-109">Go to **System administration** > **Security** > **Security diagnostic for task recording**.</span></span>
2. <span data-ttu-id="2cec5-110">その場所からタスクの記録を開きます。</span><span class="sxs-lookup"><span data-stu-id="2cec5-110">Open the task recording from its location.</span></span> <span data-ttu-id="2cec5-111">**この PC から開く** または **Lifecycle Services から開く** を選択し、続いて **閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2cec5-111">Select **Open from this PC** or **Open from Lifecycle Services**, and then select **Close**.</span></span>
3. <span data-ttu-id="2cec5-112">これにより、**セキュリティ メニュー項目の詳細** ページが開きます。このページには、プロセスに必要なセキュリティ オブジェクトの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2cec5-112">This will open the **Security menu item details** page that lists the security objects required for the process.</span></span>

 > [!NOTE]
 > <span data-ttu-id="2cec5-113">**アクション** と **出力** のメニュー項目は、一覧には含まれません。</span><span class="sxs-lookup"><span data-stu-id="2cec5-113">The **Action** and **Output** menu items are not included in the list.</span></span>

4. <span data-ttu-id="2cec5-114">**ユーザー ID** フィールドでユーザー を選択します。</span><span class="sxs-lookup"><span data-stu-id="2cec5-114">In the **User ID** field, select a user.</span></span> <span data-ttu-id="2cec5-115">ユーザーが一部のメニュー項目に対するアクセス許可を持っていない場合、**不足しているアクセス許可** フィールドが **はい** に更新されます。</span><span class="sxs-lookup"><span data-stu-id="2cec5-115">If the user does not have permissions for some menu items, the **Missing permissions** field will update to **Yes**.</span></span>
  
  ![セキュリティ メニュー項目の詳細ページ](../media/Security-Menu-Item-Details.png)

5. <span data-ttu-id="2cec5-117">**参照の追加** を選択すると、欠落して いるアクセス許可を付与するロール、職務、特権などのセキュリティ オブジェクトの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2cec5-117">Select **Add Reference** to see a list of the security objects, including roles, duties, and privileges that grant the missing permission.</span></span>
6. <span data-ttu-id="2cec5-118">リストからセキュリティ オブジェクトを選択します：</span><span class="sxs-lookup"><span data-stu-id="2cec5-118">Select a security object from the list:</span></span>

    - <span data-ttu-id="2cec5-119">**ロール** を選択した場合は 、**ユーザーへの役割の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2cec5-119">If **Role** is selected, select **Add role to user**.</span></span> <span data-ttu-id="2cec5-120">**ロールにユーザーを割り当てる** ページが表示され ます。</span><span class="sxs-lookup"><span data-stu-id="2cec5-120">This will open the **Assign users to roles** page.</span></span> <span data-ttu-id="2cec5-121">詳細については、[ユーザーにセキュリティ ロールへを割り当てる](assign-users-security-roles.md)ページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2cec5-121">For more information, see [Assign users to security roles](assign-users-security-roles.md) page.</span></span>
    - <span data-ttu-id="2cec5-122">**職務** を選択した場合は、**ロールに職務を追加する** を選択し、職務を追加するロールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2cec5-122">If **Duty** is selected, select **Add duty to role**, select the roles that the duty should be added to, and then select **OK**.</span></span>
    - <span data-ttu-id="2cec5-123">**権限** を選択した場合は、**職務に権限を追加する** を選択し、権限を追加する職務を選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2cec5-123">If **Privilege** is selected, select **Add privilege to duties**, select the roles that the duty should be added to, and then select **OK**.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]