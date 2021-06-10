---
title: 雇用されていない作業者
description: 将来雇用、現職、または過去の職歴が存在しない作業者は、雇用されていない作業者フォームに表示されます。
author: andreabichsel
ms.date: 04/06/2021
ms.topic: ''
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorkerV2, HRMMassHireProject, HRMMassHireLine, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-04-06
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f6fbada6feb55b8627b1aa1ddfe367177edb7a0a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051716"
---
# <a name="workers-without-employment"></a><span data-ttu-id="9f93d-103">雇用されていない作業者</span><span class="sxs-lookup"><span data-stu-id="9f93d-103">Workers without employment</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="9f93d-104">将来雇用、現職、または過去の職歴が存在しない作業者は、**雇用されていない作業者** フォームに表示されます。</span><span class="sxs-lookup"><span data-stu-id="9f93d-104">Workers with no future, active, or historical employment with your organization appear in the **Workers without employment** form.</span></span> <span data-ttu-id="9f93d-105">この状態を持つ作業者は、雇用レコードのない作業者をインポートする場合や、**作業者 > 雇用履歴** を使用して作業者の雇用を削除する場合に表示されます。</span><span class="sxs-lookup"><span data-stu-id="9f93d-105">Workers with this status can appear when you import workers without an employment record, or when you delete a worker's employment via **Workers > Employment history**.</span></span>

<span data-ttu-id="9f93d-106">既定では、**雇用されていない作業者** フォームは次のロールに使用できます。</span><span class="sxs-lookup"><span data-stu-id="9f93d-106">By default, the **Workers without employment** form is available to the following roles:</span></span>

- <span data-ttu-id="9f93d-107">人事管理アシスタント</span><span class="sxs-lookup"><span data-stu-id="9f93d-107">Human Resources Assistant</span></span>
- <span data-ttu-id="9f93d-108">人事管理マネージャー</span><span class="sxs-lookup"><span data-stu-id="9f93d-108">Human Resources Manager</span></span>
- <span data-ttu-id="9f93d-109">採用担当者</span><span class="sxs-lookup"><span data-stu-id="9f93d-109">Recruiter</span></span>
- <span data-ttu-id="9f93d-110">報酬と給付金のマネージャー</span><span class="sxs-lookup"><span data-stu-id="9f93d-110">Comp and Benefits Manager</span></span>
- <span data-ttu-id="9f93d-111">給与管理者</span><span class="sxs-lookup"><span data-stu-id="9f93d-111">Payroll Administrator</span></span>
- <span data-ttu-id="9f93d-112">給与マネージャー</span><span class="sxs-lookup"><span data-stu-id="9f93d-112">Payroll Manager</span></span>
- <span data-ttu-id="9f93d-113">トレーニング マネージャー</span><span class="sxs-lookup"><span data-stu-id="9f93d-113">Training Manager</span></span>

<span data-ttu-id="9f93d-114">**雇用されていない作業者** リストで、一覧表示された個人を削除できます。</span><span class="sxs-lookup"><span data-stu-id="9f93d-114">In the **Workers without employment** list, you can delete the individuals listed.</span></span> <span data-ttu-id="9f93d-115">既定では、この権限は人事管理アシスタントのロールに与えられます。</span><span class="sxs-lookup"><span data-stu-id="9f93d-115">By default, this privilege is given to the Human Resources Assistant role.</span></span> <span data-ttu-id="9f93d-116">この権限は、次の手順で他のロールにも付与できます。</span><span class="sxs-lookup"><span data-stu-id="9f93d-116">You can give this privilege to other roles with the following steps:</span></span>

1. <span data-ttu-id="9f93d-117">**システム管理** を選択し、**セキュリティの構成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f93d-117">Select **System administration**, and then select **Security configuration**.</span></span>

2. <span data-ttu-id="9f93d-118">**権限** タブで、**権限** リストを **作業者の管理** にフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="9f93d-118">In the **Privileges** tab, filter the **Privileges** list to **Maintain workers**.</span></span>

   <span data-ttu-id="9f93d-119">[![特権リストのフィルター処理](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)</span><span class="sxs-lookup"><span data-stu-id="9f93d-119">[![Filter Privileges list](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)</span></span>

3. <span data-ttu-id="9f93d-120">**参照** 列で、**メニュー項目の表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f93d-120">In the **References** column, select **Display menu items**.</span></span>

4. <span data-ttu-id="9f93d-121">**メニュー項目の表示** で、**HcmWorkersWithoutEmployment** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f93d-121">In **Display menu items**, select **HcmWorkersWithoutEmployment**.</span></span>

   <span data-ttu-id="9f93d-122">[![フォームの選択](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)</span><span class="sxs-lookup"><span data-stu-id="9f93d-122">[![Select form](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)</span></span>

5. <span data-ttu-id="9f93d-123">**削除** のアクセス許可を **付与** に設定します。</span><span class="sxs-lookup"><span data-stu-id="9f93d-123">Set the **Delete** permission to **Grant**.</span></span>

6. <span data-ttu-id="9f93d-124">**未公開のオブジェクト** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="9f93d-124">Select the **Unpublished objects** tab.</span></span>

7. <span data-ttu-id="9f93d-125">**すべて公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f93d-125">Select **Publish all**.</span></span>

   <span data-ttu-id="9f93d-126">[![変更の公開](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)</span><span class="sxs-lookup"><span data-stu-id="9f93d-126">[![Publish changes](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]