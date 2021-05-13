---
title: 品質および不適合管理の有効化
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management の品質および不適合管理機能を設定および構成するプロセスの概要を説明します。
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome, InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 67d5da648e31d07d054246f5d308a6c6cdeb506c
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956257"
---
# <a name="enable-quality-and-nonconformance-management"></a><span data-ttu-id="bb19e-103">品質および不適合管理の有効化</span><span class="sxs-lookup"><span data-stu-id="bb19e-103">Enable quality and nonconformance management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bb19e-104">このトピックでは、Microsoft Dynamics 365 Supply Chain Management の品質および不適合管理機能を設定および構成するプロセスの概要を説明します。</span><span class="sxs-lookup"><span data-stu-id="bb19e-104">This topic provides an overview of the process for setting up and configuring quality and nonconformance management features in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="enable-quality-and-nonconformance-management"></a><a name="enable-qm"></a><span data-ttu-id="bb19e-105">品質および不適合管理の有効化</span><span class="sxs-lookup"><span data-stu-id="bb19e-105">Enable quality and nonconformance management</span></span>

<span data-ttu-id="bb19e-106">次の手順に従って、システムの品質管理を有効にします。</span><span class="sxs-lookup"><span data-stu-id="bb19e-106">Follow these steps to enable quality management on your system.</span></span>

1. <span data-ttu-id="bb19e-107">**在庫管理 \> 設定 \> 在庫および倉庫管理パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bb19e-107">Go to **Inventory management \> Setup \> Inventory and warehouse management parameters**.</span></span>
1. <span data-ttu-id="bb19e-108">**品質管理** タブで、**品質管理の使用** オプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="bb19e-108">On the **Quality management** tab, set the **Use quality management** option to *Yes*.</span></span>
1. <span data-ttu-id="bb19e-109">**時間レート** フィールドに、国内通貨で時給レートを入力します。</span><span class="sxs-lookup"><span data-stu-id="bb19e-109">In the **Hourly rate** field, enter an hourly labor rate in the local currency.</span></span> <span data-ttu-id="bb19e-110">時給レートは、不適合に関連する工程の原価計算に使用されます。</span><span class="sxs-lookup"><span data-stu-id="bb19e-110">The hourly rate is used to calculate costs for operations that are related to a nonconformance.</span></span> <span data-ttu-id="bb19e-111">時間あたりのレートと算出原価は、不適合の参照情報を提供するものです。</span><span class="sxs-lookup"><span data-stu-id="bb19e-111">The hourly rate and calculated costs provide reference information for a nonconformance.</span></span> <span data-ttu-id="bb19e-112">これらは、他の機能に作用することはありません。</span><span class="sxs-lookup"><span data-stu-id="bb19e-112">They don't interact with other functionality.</span></span>
1. <span data-ttu-id="bb19e-113">**レポート設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bb19e-113">Select **Report setup**.</span></span>
1. <span data-ttu-id="bb19e-114">さまざまなレポート タイプの新しい行を追加し、各レポートで使用するドキュメントのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="bb19e-114">Add new lines for the various report types, and select the type of document to use for each report.</span></span>
1. <span data-ttu-id="bb19e-115">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="bb19e-115">Close the page.</span></span>
1. <span data-ttu-id="bb19e-116">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="bb19e-116">Close the page.</span></span>

## <a name="quality-management-configuration-process"></a><span data-ttu-id="bb19e-117">品質管理の構成プロセス</span><span class="sxs-lookup"><span data-stu-id="bb19e-117">Quality management configuration process</span></span>

<span data-ttu-id="bb19e-118">品質管理機能を使用し、品質指示を生成する前に、システムおよび前提条件を構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bb19e-118">Before you can start to use the quality management features and generate quality orders, you must configure the system and prerequisites.</span></span> <span data-ttu-id="bb19e-119">ここでは、品質管理を構成するために必要な手順の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="bb19e-119">Here is a list of the steps that are required to configure quality management.</span></span>

1. <span data-ttu-id="bb19e-120">[品質および不適合管理を有効にします](#enable-qm)。</span><span class="sxs-lookup"><span data-stu-id="bb19e-120">[Enable quality and nonconformance management](#enable-qm).</span></span>
1. <span data-ttu-id="bb19e-121">オプション : [テスト機器を構成します](quality-test-instruments.md)。</span><span class="sxs-lookup"><span data-stu-id="bb19e-121">Optional: [Configure test instruments](quality-test-instruments.md).</span></span>
1. <span data-ttu-id="bb19e-122">[テストを構成します](quality-tests.md)。</span><span class="sxs-lookup"><span data-stu-id="bb19e-122">[Configure tests](quality-tests.md).</span></span>
1. <span data-ttu-id="bb19e-123">[テスト変数と結果を構成します](quality-test-variables.md)。</span><span class="sxs-lookup"><span data-stu-id="bb19e-123">[Configure test variables and outcomes](quality-test-variables.md).</span></span>
1. <span data-ttu-id="bb19e-124">[テスト グループを構成します](quality-test-groups.md)。</span><span class="sxs-lookup"><span data-stu-id="bb19e-124">[Configure test groups](quality-test-groups.md).</span></span>
1. <span data-ttu-id="bb19e-125">オプション : [品質グループを構成し、製品にリンクします](quality-groups.md)。</span><span class="sxs-lookup"><span data-stu-id="bb19e-125">Optional: [Configure quality groups, and link to products](quality-groups.md).</span></span>
1. <span data-ttu-id="bb19e-126">オプション : [品質アソシエーションを構成します](quality-associations.md)。</span><span class="sxs-lookup"><span data-stu-id="bb19e-126">Optional: [Configure quality associations](quality-associations.md).</span></span>

<span data-ttu-id="bb19e-127">構成が完了したら、品質指示の作成と処理を開始できます。</span><span class="sxs-lookup"><span data-stu-id="bb19e-127">After the configuration is completed, you can start to create and process quality orders.</span></span> <span data-ttu-id="bb19e-128">品質指示の作成および使用方法の詳細については、[品質指示](quality-orders.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bb19e-128">For more information about how to create and work with quality orders, see [Quality orders](quality-orders.md).</span></span>

## <a name="nonconformance-management-configuration-process"></a><span data-ttu-id="bb19e-129">不適合管理の構成プロセス</span><span class="sxs-lookup"><span data-stu-id="bb19e-129">Nonconformance management configuration process</span></span>

<span data-ttu-id="bb19e-130">不適合管理機能を使用し、不適合を生成する前に、システムおよび前提条件を構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bb19e-130">Before you can start to use the nonconformance management features and generate nonconformances, you must configure the system and prerequisites.</span></span> <span data-ttu-id="bb19e-131">ここでは、不適合管理を構成するために必要な手順の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="bb19e-131">Here is a list of the steps that are required to configure nonconformance management.</span></span>

1. <span data-ttu-id="bb19e-132">[品質および不適合管理を有効にします](#enable-qm)。</span><span class="sxs-lookup"><span data-stu-id="bb19e-132">[Enable quality and nonconformance management](#enable-qm).</span></span>
1. <span data-ttu-id="bb19e-133">[不適合の承認を担当する作業者を構成します](quality-responsible-workers.md)。</span><span class="sxs-lookup"><span data-stu-id="bb19e-133">[Configure workers who are responsible for approving nonconformances](quality-responsible-workers.md).</span></span>
1. <span data-ttu-id="bb19e-134">[問題タイプを構成します](quality-problem-types.md)。</span><span class="sxs-lookup"><span data-stu-id="bb19e-134">[Configure problem types](quality-problem-types.md).</span></span>
1. <span data-ttu-id="bb19e-135">[検査ゾーンを構成します](quality-quarantine-zones.md)。</span><span class="sxs-lookup"><span data-stu-id="bb19e-135">[Configure quarantine zones](quality-quarantine-zones.md).</span></span>
1. <span data-ttu-id="bb19e-136">[診断タイプを構成します](quality-diagnostic-types.md)。</span><span class="sxs-lookup"><span data-stu-id="bb19e-136">[Configure diagnostic types](quality-diagnostic-types.md).</span></span>
1. <span data-ttu-id="bb19e-137">[操作を構成します](quality-operations.md)。</span><span class="sxs-lookup"><span data-stu-id="bb19e-137">[Configure operations](quality-operations.md).</span></span>
1. <span data-ttu-id="bb19e-138">オプション : [品質諸費用を構成します](quality-charges.md)。</span><span class="sxs-lookup"><span data-stu-id="bb19e-138">Optional: [Configure quality charges](quality-charges.md).</span></span>

<span data-ttu-id="bb19e-139">構成が完了したら、不適合の作成と処理を開始できます。</span><span class="sxs-lookup"><span data-stu-id="bb19e-139">After the configuration is completed, you can start to create and process nonconformances.</span></span> <span data-ttu-id="bb19e-140">不適合を作成し使用する方法の詳細については、「[不適合の作成および処理](tasks/create-process-non-conformance.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bb19e-140">For more information about how to create and work with nonconformances, see [Create and process nonconformances](tasks/create-process-non-conformance.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bb19e-141">追加リソース</span><span class="sxs-lookup"><span data-stu-id="bb19e-141">Additional resources</span></span>

- [<span data-ttu-id="bb19e-142">品質管理の概要</span><span class="sxs-lookup"><span data-stu-id="bb19e-142">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="bb19e-143">品質および不適合管理の有効化</span><span class="sxs-lookup"><span data-stu-id="bb19e-143">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="bb19e-144">倉庫プロセスに対する品質管理</span><span class="sxs-lookup"><span data-stu-id="bb19e-144">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
