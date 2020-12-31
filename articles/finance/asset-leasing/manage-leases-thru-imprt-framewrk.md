---
title: リース インポート フレームワークでのリースの管理
description: このトピックでは、リースのインポート フレームワークを使用して、複数のリースを同時に調整する方法について説明します。
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d7a7d2afd8f352bc167ec8c0a354ee4ac0a9e77b
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4445391"
---
# <a name="manage-leases-through-the-lease-import-framework"></a><span data-ttu-id="77d21-103">リース インポート フレームワークでのリースの管理</span><span class="sxs-lookup"><span data-stu-id="77d21-103">Manage leases through the Lease import framework</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="77d21-104">このトピックでは、リースのインポート フレームワークを使用して、複数のリースをワンステップで調整する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="77d21-104">This topic explains how to use the Lease import framework to adjust multiple leases in one step.</span></span> <span data-ttu-id="77d21-105">この機能を使用すると、時間を節約することができ、また、人為的ミスの可能性を減らすことで、より正確な調整を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="77d21-105">By using this capability, you can save time, and you can also ensure more accurate adjustments by reducing the chance of human error.</span></span> <span data-ttu-id="77d21-106">また、この機能は Microsoft Dynamics 365 Finance を外部データ エンティティと接続することができ、データを効率的にアップロードできます。</span><span class="sxs-lookup"><span data-stu-id="77d21-106">Additionally, this capability can connect Microsoft Dynamics 365 Finance with external data entities to efficiently upload data.</span></span>

<span data-ttu-id="77d21-107">次のデータ エンティティを使用して、外部システムに資産リースを統合することができます。</span><span class="sxs-lookup"><span data-stu-id="77d21-107">The following data entities can be used to integrate Asset leasing with external systems:</span></span>

- <span data-ttu-id="77d21-108">リースのステージング</span><span class="sxs-lookup"><span data-stu-id="77d21-108">Lease staging</span></span>
- <span data-ttu-id="77d21-109">支払契約のステージング</span><span class="sxs-lookup"><span data-stu-id="77d21-109">Payment contract staging</span></span>
- <span data-ttu-id="77d21-110">履行契約ステージング</span><span class="sxs-lookup"><span data-stu-id="77d21-110">Executory contract staging</span></span>

<span data-ttu-id="77d21-111">インポート プロセスを使用して、リースの調整、財務以外の情報の更新、または新しいリースの追加を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="77d21-111">You can use the import process to adjust a lease, update non-financial information, or add new leases.</span></span> <span data-ttu-id="77d21-112">リース データは、インポートする前に表示および編集できます。</span><span class="sxs-lookup"><span data-stu-id="77d21-112">You can view and edit the leasing data before you import it.</span></span>

<span data-ttu-id="77d21-113">システムは、リース インポート スイートを使用して、次の 3 つのプロセスを実行できます。</span><span class="sxs-lookup"><span data-stu-id="77d21-113">The system can run the following three processes through the lease import suite.</span></span>

| <span data-ttu-id="77d21-114">プロセスのタイプ</span><span class="sxs-lookup"><span data-stu-id="77d21-114">Process type</span></span>  | <span data-ttu-id="77d21-115">説明</span><span class="sxs-lookup"><span data-stu-id="77d21-115">Description</span></span> |
|---------------|-------------|
| <span data-ttu-id="77d21-116">レコードの追加</span><span class="sxs-lookup"><span data-stu-id="77d21-116">Add record</span></span>    | <span data-ttu-id="77d21-117">このプロセス タイプを持つリースを移行すると、システムでリースが作成されます。</span><span class="sxs-lookup"><span data-stu-id="77d21-117">Migrated leases that have this process type create a lease in the system.</span></span> <span data-ttu-id="77d21-118">支払スケジュールを手動で確認する必要があり、そして、移行後に最初の認識仕訳入力を手動で転記する必要があります。</span><span class="sxs-lookup"><span data-stu-id="77d21-118">The payment schedule must be manually confirmed, and the initial recognition journal entry must be manually posted after the migration.</span></span> |
| <span data-ttu-id="77d21-119">レコードの更新</span><span class="sxs-lookup"><span data-stu-id="77d21-119">Update record</span></span> | <span data-ttu-id="77d21-120">このプロセス タイプが設定されている移行リースは、システムに既に存在するリースのフィールド値を更新します。</span><span class="sxs-lookup"><span data-stu-id="77d21-120">Migrated leases that have this process type update field values for a lease that is already in the system.</span></span> <span data-ttu-id="77d21-121">**更新するフィールドの選択** ページで選択したフィールドのみが更新されます。</span><span class="sxs-lookup"><span data-stu-id="77d21-121">Only the fields that have been selected on the **Update fields selection** page are updated.</span></span> <span data-ttu-id="77d21-122">このプロセス タイプはリースを調節しないことから、**更新するフィールドの選択** ページで、財務以外のフィールドを選択することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="77d21-122">We recommended that you select non-financial fields on the **Update fields selection** page, because this process type doesn't adjust the lease.</span></span> |
| <span data-ttu-id="77d21-123">レコードの調整</span><span class="sxs-lookup"><span data-stu-id="77d21-123">Adjust record</span></span> | <span data-ttu-id="77d21-124">このプロセス タイプを持つ移行されたリースは、リースが調節されます。</span><span class="sxs-lookup"><span data-stu-id="77d21-124">Migrated leases that have this process type adjust the lease.</span></span> <span data-ttu-id="77d21-125">この調整により、リースの財務リースが変更されます。</span><span class="sxs-lookup"><span data-stu-id="77d21-125">This adjustment causes a financial lease modification of the lease.</span></span> <span data-ttu-id="77d21-126">リースが処理された後、システムは、リース インポート スイートからの新しいデータを使用して、新規支払スケジュールを作成します。</span><span class="sxs-lookup"><span data-stu-id="77d21-126">After the lease is processed, the system creates a new payment schedule by using the new data from the lease import suite.</span></span> <span data-ttu-id="77d21-127">システムが支払スケジュールを確認していないか、調整仕訳入力を転記していません。</span><span class="sxs-lookup"><span data-stu-id="77d21-127">The system doesn't confirm the payment schedule or post the adjustment journal entry.</span></span> |

<span data-ttu-id="77d21-128">**データ管理** ワークスペースを使用して情報をアップロードした後 、**インポート ヘッダー** ページ **(資産リース \> リース インポート フレームワーク \> インポート ヘッダー**) を開きます。</span><span class="sxs-lookup"><span data-stu-id="77d21-128">After information is uploaded through the **Data management** workspace, open the **Import header** page (**Asset leasing \> Lease import framework \> Import header**).</span></span> <span data-ttu-id="77d21-129">このページには、前の 3 つのデータ エンティティのインポートのすべてが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="77d21-129">This page lists all imports of the three data entities that were listed earlier.</span></span>

<span data-ttu-id="77d21-130">処理が実行される前にリース ステージング データを表示するには、**ステージング データ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="77d21-130">To view the lease staging data before processing is run, select **Staging data**.</span></span>

<span data-ttu-id="77d21-131">比較機能を使用すると、インポート中のレコードと、システムに存在する対応するレコードを比較できます。</span><span class="sxs-lookup"><span data-stu-id="77d21-131">The compare function lets you compare a record that you're importing with the corresponding record that's already in your system.</span></span> <span data-ttu-id="77d21-132">個々のリース レコードを比較するには、リースを選択し、**比較** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="77d21-132">To compare an individual lease record, select a lease, and then select **Compare**.</span></span> <span data-ttu-id="77d21-133">このステップを実行して、リースレコードを移行する前に **差異** レポートを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="77d21-133">You should complete this step to generate a **Differences** report before you migrate the lease records.</span></span> <span data-ttu-id="77d21-134">比較機能では、ステージング データの値と現在システムにあるリースの値とが比較されます。</span><span class="sxs-lookup"><span data-stu-id="77d21-134">The Compare functionality compares the values in the staging data to the values for leases that are currently in the system.</span></span>

> [!NOTE]
> <span data-ttu-id="77d21-135">この比較機能は、**レコードの追加プロセス** タイプを持つリースに対してはそのリースと比較するものがないため機能しません。</span><span class="sxs-lookup"><span data-stu-id="77d21-135">The Compare functionality doesn't work for leases that have the **Add record** process type, because there is nothing to compare against that lease.</span></span>
>
> <span data-ttu-id="77d21-136">複数のリースを同時に比較するには、**資産リース \> リース インポート フレームワーク \> 定期的 \> 比較** に移動し、**比較** を選択します。</span><span class="sxs-lookup"><span data-stu-id="77d21-136">To compare multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic \> Compare**, and select **Compare**.</span></span>

<span data-ttu-id="77d21-137">エンティティごとに、現在システムに含まれているものと、ステージング テーブルに含まれるものとの差異を表示できます。</span><span class="sxs-lookup"><span data-stu-id="77d21-137">For each entity, you can view the differences between what is currently in the system and what is in the staging tables.</span></span> <span data-ttu-id="77d21-138">ステージング テーブルの各エンティティについて、**相違点を参照** を選択します。</span><span class="sxs-lookup"><span data-stu-id="77d21-138">For each entity in the staging tables, select **See differences**.</span></span> <span data-ttu-id="77d21-139">表示されるダイアログ ボックスには、現在の値と提案されているステージング値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="77d21-139">The dialog box that appears shows the current value and the proposed staging value.</span></span>

<span data-ttu-id="77d21-140">**新規の値** 列でステージング値を変更して、**ステージングの更新** を選択することでステージング値を更新することもできます。</span><span class="sxs-lookup"><span data-stu-id="77d21-140">You can also update the staging value by changing it in the **New Value** column and then selecting **Update staging**.</span></span>

<span data-ttu-id="77d21-141">リースを検証して、エラーを発生させずにレコードをシステムに取り込めるようにできます。</span><span class="sxs-lookup"><span data-stu-id="77d21-141">You can validate leases to ensure that the records can be brought into the system without introducing errors.</span></span> <span data-ttu-id="77d21-142">リース レコードを移行する前に、システムによって複数の検証が実行され、レコードが正常にインポートされるようになっています。</span><span class="sxs-lookup"><span data-stu-id="77d21-142">Before a lease record is migrated, the system runs several validations to ensure that the record will be successfully imported.</span></span> <span data-ttu-id="77d21-143">個々のリースを検証するには、**検証** を選択します。</span><span class="sxs-lookup"><span data-stu-id="77d21-143">To validate an individual lease, select **Validate**.</span></span>

> [!NOTE]
> <span data-ttu-id="77d21-144">複数のリースを同時に比較するには、**資産リース \> リース インポート フレームワーク \> 定期的 \> 検証** に移動し、**比較** を選択します。</span><span class="sxs-lookup"><span data-stu-id="77d21-144">To validate multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic \> Validate**, and select **Compare**.</span></span>

<span data-ttu-id="77d21-145">個々のリースを処理するには、**インポート ヘッダー** ページで **リース レコードの移行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="77d21-145">To process an individual lease, select **Migrate lease records** on the **Import header** page.</span></span> <span data-ttu-id="77d21-146">リースが移行されると、**プロセス タイプ** フィールドで指定されたアクションが実行されます。</span><span class="sxs-lookup"><span data-stu-id="77d21-146">When a lease is migrated, the system performs the action that is specified in the **Process type** field.</span></span>

> [!NOTE]
> <span data-ttu-id="77d21-147">複数のリースを同時に比較するには、**資産リース \> リース インポート フレームワーク \> 定期的 \> 検証** に移動し、**比較** を選択します。</span><span class="sxs-lookup"><span data-stu-id="77d21-147">To validate multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic \> Validate**, and select **Compare**.</span></span>

<span data-ttu-id="77d21-148">リースを比較した後、レポートを実行して、インポート ID に含まれている各リースの違いを表示できます。</span><span class="sxs-lookup"><span data-stu-id="77d21-148">After the leases are compared, you can run a report to view the differences for each lease that is included in the import ID.</span></span> <span data-ttu-id="77d21-149">1 つのリースに対してレポートを実行するには、ステージング データでリースを選択し、**比較とレポートの表示 \> レポートの差異** を選択します。</span><span class="sxs-lookup"><span data-stu-id="77d21-149">To run the report for one lease, select that lease in the staging data, and then select **Compare and view report \> Differences report**.</span></span>

> [!NOTE]
> <span data-ttu-id="77d21-150">複数のリースを同時に検証するには、 **資産リース \> 照会とレポート \> 差異レポート** に移動して、**比較** を選択します。</span><span class="sxs-lookup"><span data-stu-id="77d21-150">To validate multiple leases at the same time, go to **Asset leasing \> Inquiries and reports \> Differences report**, and select **Compare**.</span></span>

## <a name="set-up-update-fields"></a><span data-ttu-id="77d21-151">更新フィールドの設定</span><span class="sxs-lookup"><span data-stu-id="77d21-151">Set up update fields</span></span>

<span data-ttu-id="77d21-152">リースの更新にリース インポート フレームワークを使用していて、プロセス タイプが **更新レコード** の場合は、更新する特定のフィールドを選択できます。</span><span class="sxs-lookup"><span data-stu-id="77d21-152">If you're using the Lease import framework to update leases, and the process type is **Update record**, you can select specific fields to update.</span></span>

1. <span data-ttu-id="77d21-153">**資産のリース \> リース インポート フレームワーク \> 設定 \> フィールド選択の更新** に移動します。</span><span class="sxs-lookup"><span data-stu-id="77d21-153">Go to **Asset leasing \> Lease import framework \> Setup \> Update field selection**.</span></span>
2. <span data-ttu-id="77d21-154">表示されるページで、更新するフィールドを選択し、緑色の矢印を選択してそれを **選択したフィールド** リストに移動します。</span><span class="sxs-lookup"><span data-stu-id="77d21-154">On the page that appears, select the fields to update, and then select the green arrow to move them to the **Selected fields** list.</span></span> <span data-ttu-id="77d21-155">**選択したフィールド** リストのフィールドのみが、リース インポート スイートを使用して更新できます。</span><span class="sxs-lookup"><span data-stu-id="77d21-155">Only fields in the **Selected fields** list can be updated by using the lease import suite.</span></span>
