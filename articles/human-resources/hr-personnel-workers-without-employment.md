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
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-04-06
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1a137de25924f4c4ec6f6b1fe70f9d21af591c0
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924574"
---
# <a name="workers-without-employment"></a><span data-ttu-id="b2c38-103">雇用されていない作業者</span><span class="sxs-lookup"><span data-stu-id="b2c38-103">Workers without employment</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b2c38-104">将来雇用、現職、または過去の職歴が存在しない作業者は、**雇用されていない作業者** フォームに表示されます。</span><span class="sxs-lookup"><span data-stu-id="b2c38-104">Workers with no future, active, or historical employment with your organization appear in the **Workers without employment** form.</span></span> <span data-ttu-id="b2c38-105">この状態を持つ作業者は、雇用レコードのない作業者をインポートする場合や、**作業者 > 雇用履歴** を使用して作業者の雇用を削除する場合に表示されます。</span><span class="sxs-lookup"><span data-stu-id="b2c38-105">Workers with this status can appear when you import workers without an employment record, or when you delete a worker's employment via **Workers > Employment history**.</span></span>

<span data-ttu-id="b2c38-106">既定では、**雇用されていない作業者** フォームは次のロールに使用できます。</span><span class="sxs-lookup"><span data-stu-id="b2c38-106">By default, the **Workers without employment** form is available to the following roles:</span></span>

- <span data-ttu-id="b2c38-107">人事管理アシスタント</span><span class="sxs-lookup"><span data-stu-id="b2c38-107">Human Resources Assistant</span></span>
- <span data-ttu-id="b2c38-108">人事管理マネージャー</span><span class="sxs-lookup"><span data-stu-id="b2c38-108">Human Resources Manager</span></span>
- <span data-ttu-id="b2c38-109">採用担当者</span><span class="sxs-lookup"><span data-stu-id="b2c38-109">Recruiter</span></span>
- <span data-ttu-id="b2c38-110">報酬と給付金のマネージャー</span><span class="sxs-lookup"><span data-stu-id="b2c38-110">Comp and Benefits Manager</span></span>
- <span data-ttu-id="b2c38-111">給与管理者</span><span class="sxs-lookup"><span data-stu-id="b2c38-111">Payroll Administrator</span></span>
- <span data-ttu-id="b2c38-112">給与マネージャー</span><span class="sxs-lookup"><span data-stu-id="b2c38-112">Payroll Manager</span></span>
- <span data-ttu-id="b2c38-113">トレーニング マネージャー</span><span class="sxs-lookup"><span data-stu-id="b2c38-113">Training Manager</span></span>

<span data-ttu-id="b2c38-114">**雇用されていない作業者** リストで、一覧表示された個人を削除できます。</span><span class="sxs-lookup"><span data-stu-id="b2c38-114">In the **Workers without employment** list, you can delete the individuals listed.</span></span> <span data-ttu-id="b2c38-115">既定では、この権限は人事管理アシスタントのロールに与えられます。</span><span class="sxs-lookup"><span data-stu-id="b2c38-115">By default, this privilege is given to the Human Resources Assistant role.</span></span> <span data-ttu-id="b2c38-116">この権限は、次の手順で他のロールにも付与できます。</span><span class="sxs-lookup"><span data-stu-id="b2c38-116">You can give this privilege to other roles with the following steps:</span></span>

1. <span data-ttu-id="b2c38-117">**システム管理** を選択し、**セキュリティの構成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c38-117">Select **System administration**, and then select **Security configuration**.</span></span>

2. <span data-ttu-id="b2c38-118">**権限** タブで、**権限** リストを **作業者の管理** にフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="b2c38-118">In the **Privileges** tab, filter the **Privileges** list to **Maintain workers**.</span></span>

   <span data-ttu-id="b2c38-119">[![特権リストのフィルター処理](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)</span><span class="sxs-lookup"><span data-stu-id="b2c38-119">[![Filter Privileges list](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)</span></span>

3. <span data-ttu-id="b2c38-120">**参照** 列で、**メニュー項目の表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c38-120">In the **References** column, select **Display menu items**.</span></span>

4. <span data-ttu-id="b2c38-121">**メニュー項目の表示** で、**HcmWorkersWithoutEmployment** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c38-121">In **Display menu items**, select **HcmWorkersWithoutEmployment**.</span></span>

   <span data-ttu-id="b2c38-122">[![フォームの選択](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)</span><span class="sxs-lookup"><span data-stu-id="b2c38-122">[![Select form](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)</span></span>

5. <span data-ttu-id="b2c38-123">**削除** のアクセス許可を **付与** に設定します。</span><span class="sxs-lookup"><span data-stu-id="b2c38-123">Set the **Delete** permission to **Grant**.</span></span>

6. <span data-ttu-id="b2c38-124">**未公開のオブジェクト** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c38-124">Select the **Unpublished objects** tab.</span></span>

7. <span data-ttu-id="b2c38-125">**すべて公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c38-125">Select **Publish all**.</span></span>

   <span data-ttu-id="b2c38-126">[![変更の公開](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)</span><span class="sxs-lookup"><span data-stu-id="b2c38-126">[![Publish changes](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]