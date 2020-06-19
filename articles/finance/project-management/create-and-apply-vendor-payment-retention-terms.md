---
title: 仕入先への支払留保条件の作成と適用
description: このトピックでは、仕入先への支払の保留条件の設定と管理に関する情報を提供します。
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 0e14050a79220b5d02763a025040edb934489d00
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410241"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="082e6-103">仕入先への支払留保条件の作成と適用</span><span class="sxs-lookup"><span data-stu-id="082e6-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="082e6-104">プロジェクトの仕入先に対する支払留保条件の設定は、組織で仕入先への支払いの一部を保持したい場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="082e6-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="082e6-105">たとえば、仕入先への支払を、商品が予定どおりに配送されるまで保留するとします。</span><span class="sxs-lookup"><span data-stu-id="082e6-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="082e6-106">仕入先との契約の交渉時に、仕入先への支払い留保の条件を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="082e6-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="082e6-107">仕入先への支払留保条件を作成する</span><span class="sxs-lookup"><span data-stu-id="082e6-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="082e6-108">留保する仕入先支払の割合と、リリースされる留保した金額の割合を入力できます。</span><span class="sxs-lookup"><span data-stu-id="082e6-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="082e6-109">仕入先請求書の金額は、契約が指定した完了状態に到達するまで、自動的に留保されます。</span><span class="sxs-lookup"><span data-stu-id="082e6-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="082e6-110">仕入先に対する留保条件の設定後は、当該仕入先が関連するすべてのプロジェクトにその条件を適用できます。</span><span class="sxs-lookup"><span data-stu-id="082e6-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="082e6-111">以下の手順を使用して、仕入先への支払の留保条件を設定および管理します。</span><span class="sxs-lookup"><span data-stu-id="082e6-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="082e6-112">**プロジェクト管理と会計** > **留保** > **仕入先支払留保条件**に移動します。</span><span class="sxs-lookup"><span data-stu-id="082e6-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="082e6-113">**新規** を選択して、新たな仕入先への留保条件を追加します。</span><span class="sxs-lookup"><span data-stu-id="082e6-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="082e6-114">新しい条件の **ルール ID** が自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="082e6-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="082e6-115">**説明**フィールドに簡単な説明を入力し、**条件**クイックタブの**明細行の追加**を選択して 、以下の条件値を入力します :</span><span class="sxs-lookup"><span data-stu-id="082e6-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="082e6-116">**配送単位の割合** : 条件の完了率を入力します。</span><span class="sxs-lookup"><span data-stu-id="082e6-116">**Percentage of units delivered**: Enter a percentage of completion for the term.</span></span> <span data-ttu-id="082e6-117">金額は、プロジェクトの完了段階が指定された割合になるまで、仕入先の請求書に自動的に保持されます。</span><span class="sxs-lookup"><span data-stu-id="082e6-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="082e6-118">たとえば、50 を入力すると、プロジェクトが 50% 完了するまで金額が留保されます。</span><span class="sxs-lookup"><span data-stu-id="082e6-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="082e6-119">**留保する割合** : 仕入先の請求金額のうち、保持する割合を入力します。</span><span class="sxs-lookup"><span data-stu-id="082e6-119">**Percentage to retain**: Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="082e6-120">たとえば、「10.00」 と入力した場合、仕入先の請求書に記載されている金額の 10% は、**納品単位の割合フィールド**で設定されている完了率に達するまで保持されます。</span><span class="sxs-lookup"><span data-stu-id="082e6-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="082e6-121">**リリースする割合** : **明細行の追加**を選択して、選択したプロジェクトの完了レベルに応じてリリースされる、留保済み金額の割合を入力します。</span><span class="sxs-lookup"><span data-stu-id="082e6-121">**Percentage to release**: Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="082e6-122">プロジェクト完了のさまざまなレベルに対して複数のマイルストーンが存在する場合は、留保ルールごとに別の仕入先の留保条件を入力します。</span><span class="sxs-lookup"><span data-stu-id="082e6-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="082e6-123">各明細行には、指定されたプロジェクト完了レベルごとに、異なる留保率と異なるリリース率を指定できます。</span><span class="sxs-lookup"><span data-stu-id="082e6-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="082e6-124">仕入先の留保条件の設定後は、プロジェクトにこの条件を適用することができます。</span><span class="sxs-lookup"><span data-stu-id="082e6-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="082e6-125">仕入先の留保条件をプロジェクトに適用する</span><span class="sxs-lookup"><span data-stu-id="082e6-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="082e6-126">**プロジェクト管理と会計** > **プロジェクト** > **すべてのプロジェクト** を開き、プロジェクトのリストページからプロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="082e6-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="082e6-127">**仕入先契約** クイック タブで、**行の追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="082e6-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="082e6-128">**口座コード フィールド**で、次のいずれかのオプションを選択します :</span><span class="sxs-lookup"><span data-stu-id="082e6-128">In the **Account code field**, select one of the following options:</span></span> 

   - <span data-ttu-id="082e6-129">**テーブル** : 仕入先の留保条件が、単一の仕入先に適用されます。</span><span class="sxs-lookup"><span data-stu-id="082e6-129">**Table**: The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="082e6-130">**グループ** : 仕入先の留保条件が、仕入先グループ内のすべての仕入先に適用されます。</span><span class="sxs-lookup"><span data-stu-id="082e6-130">**Group**: The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="082e6-131">**すべて** : 仕入先の留保条件が、すべての仕入先に適用されます。</span><span class="sxs-lookup"><span data-stu-id="082e6-131">**All**: The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="082e6-132">**仕入先 / 仕入先グループ フィールド**で、仕入先の留保条件を適用する仕入先、または仕入先グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="082e6-132">In the **Vendor/Vendor group field**, select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="082e6-133">前のステップで **すべて** を選択した場合、このフィールドは使用できません。</span><span class="sxs-lookup"><span data-stu-id="082e6-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="082e6-134">**仕入先の留保条件**フィールドで、前述の手順で作成した留保条件を選択します。</span><span class="sxs-lookup"><span data-stu-id="082e6-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="082e6-135">プロジェクトで仕入先に対して Pay-when-paid (PWP) 条件が設定されている場合は、**PWP しきい値の割合**フィールドににプロジェクトのしきい値の割合を入力します。</span><span class="sxs-lookup"><span data-stu-id="082e6-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="082e6-136">仕入先留保条件は、仕入先用に作成した発注書にも表示されます。</span><span class="sxs-lookup"><span data-stu-id="082e6-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>
