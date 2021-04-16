---
title: 個人情報の編集の制限
description: Dynamics 365 Human Resources で連絡先情報を編集する従業員を制限します。
author: andreabichsel
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 727e0d4dbc5b330045bc9f91abab4d43b09e4382
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794808"
---
# <a name="restrict-editing-of-personal-information"></a><span data-ttu-id="ff7e8-103">個人情報の編集の制限</span><span class="sxs-lookup"><span data-stu-id="ff7e8-103">Restrict editing of personal information</span></span>

[!include [applies to](../includes/applies-to-hr.md)]
[!include [preview feature](./includes/preview-feature.md)]

<span data-ttu-id="ff7e8-104">このトピックでは、Dynamics 365 Human Resources で従業員が連絡先情報を編集するのを制限する方法について説明します 。</span><span class="sxs-lookup"><span data-stu-id="ff7e8-104">This topic describes how to restrict employees from editing contact details in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="ff7e8-105">従業員が、ビジネスの場所や電子メール アドレスなど、特定の連絡先情報を編集できないようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="ff7e8-105">You might want to prevent employees from editing certain contact details, such as their business location or email address.</span></span>

> [!NOTE]
> <span data-ttu-id="ff7e8-106">この機能を使用するには、まず機能管理で **(プレビュー) 従業員が特定の目的で住所や連絡先情報の追加または編集を制限する** を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff7e8-106">To use this feature, you must first enable **(Preview) Restrict employees from adding or editing address and contact information for select purposes** in Feature management.</span></span> <span data-ttu-id="ff7e8-107">プレビュー機能を有効にする方法については、[機能の管理](hr-admin-manage-features.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ff7e8-107">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span><br><br><span data-ttu-id="ff7e8-108">![プレビュー機能を有効にする](./media/hr-employee-self-service-restrict-enable.png)</span><span class="sxs-lookup"><span data-stu-id="ff7e8-108">![Enable preview feature](./media/hr-employee-self-service-restrict-enable.png)</span></span>

## <a name="choose-the-information-an-employee-can-add-or-edit"></a><span data-ttu-id="ff7e8-109">従業員が追加または編集できる情報の選択</span><span class="sxs-lookup"><span data-stu-id="ff7e8-109">Choose the information an employee can add or edit</span></span>

1. <span data-ttu-id="ff7e8-110">Human Resources では、**人事管理** を選択し、**リンク** を選択して、**人事管理パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff7e8-110">In Human Resources, select **Personnel management**, select **Links**, and then select **Human resources parameters**.</span></span>

   ![人事管理パラメーターに移動する](./media/hr-employee-self-service-human-resources-parameters.png)

2. <span data-ttu-id="ff7e8-112">**人事管理パラメーター** ページで、**従業員セルフ サービス** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="ff7e8-112">On the **Human resources parameters** page, select the **Employee self service** tab.</span></span>

   ![従業員セルフ サービスの選択](./media/hr-employee-self-service-tab.png)

3. <span data-ttu-id="ff7e8-114">**従業員セルフ サービス** タブで、従業員に追加または編集してほしくない **住所と連絡先情報** セクションのすべての情報をオフにします。</span><span class="sxs-lookup"><span data-stu-id="ff7e8-114">On the **Employee self service** tab, uncheck all information in the **Address and contact information** section that you don't want employees to add or edit.</span></span> <span data-ttu-id="ff7e8-115">この例では、**ビジネス** の連絡先情報をオフにしました。</span><span class="sxs-lookup"><span data-stu-id="ff7e8-115">In this example, we've unchecked **Business** contact information.</span></span>

   ![ビジネスの連絡先情報の編集の制限](./media/hr-employee-self-service-restrict-business.png)

4. <span data-ttu-id="ff7e8-117">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff7e8-117">Select **Save**.</span></span>

   ![変更の保存](./media/hr-employee-self-service-restrict-save.png)

## <a name="employee-experience"></a><span data-ttu-id="ff7e8-119">従業員エクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="ff7e8-119">Employee experience</span></span>

<span data-ttu-id="ff7e8-120">従業員が連絡先情報を追加または編集するのを制限した後、従業員は情報を表示できますが、変更はできません。</span><span class="sxs-lookup"><span data-stu-id="ff7e8-120">After you've restricted employees from adding or editing contact details, they can see the information, but can't change it.</span></span>

<span data-ttu-id="ff7e8-121">この例では、従業員が **ビジネス** の連絡先情報を編集するのを制限されている場合でも、従業員セルフ サービスの情報を表示できます。</span><span class="sxs-lookup"><span data-stu-id="ff7e8-121">In this example, where employees are restricted from editing **Business** contact details, they can still see the information in Employee self service:</span></span>

![ビジネスの連絡先情報の表示](./media/hr-employee-self-service-restrict-view.png)

<span data-ttu-id="ff7e8-123">ただし、従業員がビジネスの連絡先情報を選択すると、**住所の編集** ウィンドウは読み取り専用として表示され、フィールドを一切変更できません。</span><span class="sxs-lookup"><span data-stu-id="ff7e8-123">However, when they select the business contact details, the **Edit address** pane appears as read-only, and they can't change any of the fields.</span></span>

![ビジネスの連絡先情報は読み取り専用として表示](./media/hr-employee-self-service-restrict-read-only.png)

<span data-ttu-id="ff7e8-125">さらに、**追加** を選択して新しい住所を追加した場合、**目的** のドロップダウン ボックスから **ビジネス** を選択することはできません。</span><span class="sxs-lookup"><span data-stu-id="ff7e8-125">In addition, if they select **Add** to add a new address, they can't select **Business** from the **Purpose** dropdown box.</span></span>

![従業員がビジネス住所を追加できない](./media/hr-employee-self-service-restrict-add.png)

<span data-ttu-id="ff7e8-127">**連絡先情報** ページで **個人情報** を選択し、新しい住所を追加すると、従業員は同じ体験をします。</span><span class="sxs-lookup"><span data-stu-id="ff7e8-127">Employees get the same experience when they select **Contact details** on the **Personal information** page and add a new address.</span></span> <span data-ttu-id="ff7e8-128">**目的** のドロップダウン ボックスには、追加できる情報の種類のみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ff7e8-128">The **Purpose** dropdown box only displays the types of information they can add.</span></span> 

![従業員は目的のドロップダウンでビジネスを選択できない](./media/hr-employee-self-service-restrict-purpose.png)

<span data-ttu-id="ff7e8-130">**連絡先情報** では、 グリッドに **目的** が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ff7e8-130">**Contact details** now shows **Purpose** in the grid.</span></span>

![連絡先情報グリッドに目的が表示される](./media/hr-employee-self-service-restrict-purpose-grid.png)

## <a name="see-also"></a><span data-ttu-id="ff7e8-132">参照</span><span class="sxs-lookup"><span data-stu-id="ff7e8-132">See also</span></span>

[<span data-ttu-id="ff7e8-133">従業員およびマネージャー セルフ サービスの概要</span><span class="sxs-lookup"><span data-stu-id="ff7e8-133">Employee and Manager self service overview</span></span>](hr-employee-manager-self-service-overview.md)<br>
[<span data-ttu-id="ff7e8-134">Human Resources パラメーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="ff7e8-134">Configure Human resources parameters</span></span>](hr-setup-parameters.md)<br>
[<span data-ttu-id="ff7e8-135">個人情報の編集</span><span class="sxs-lookup"><span data-stu-id="ff7e8-135">Edit personal information</span></span>](hr-employee-manager-self-service-edit-personal-information.md)