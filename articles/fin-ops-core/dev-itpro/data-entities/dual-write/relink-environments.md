---
title: 二重書き込み環境のリンク解除および再リンク
description: このトピックでは、リンクの解除、キー テーブルのクリア、および二重書き込み環境の再リンクの方法について説明します。
author: RamaKrishnamoorthy
ms.date: 04/07/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: ramasri
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0d93440e86c13e20b83d2d9740d83540d4883ba2
ms.sourcegitcommit: 51cad1ce3ed44ebf7eb9bdf553ee2df4c1f03135
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6016197"
---
# <a name="unlink-and-relink-dual-write-environments"></a><span data-ttu-id="415cf-103">二重書き込み環境のリンク解除および再リンク</span><span class="sxs-lookup"><span data-stu-id="415cf-103">Unlink and relink dual-write environments</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="415cf-104">環境間の二重書き込み接続のリンクを解除および再リンクする場合は、キー テーブルからデータを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="415cf-104">When you unlink and relink dual-write connection between environments, you need to delete the data from the key tables.</span></span> <span data-ttu-id="415cf-105">この要件は、バックアップや復元などの活動中の、サンドボックス、製品、およびユーザー承認テスト (UAT) 環境に適用されます。</span><span class="sxs-lookup"><span data-stu-id="415cf-105">This requirement applies to sandbox, production, and user acceptance test (UAT) environments during activities like backup and restore.</span></span> <span data-ttu-id="415cf-106">このトピックでは、リンクの解除、キー テーブルでのデータの削除、および二重書き込み環境の再リンクの方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="415cf-106">This topic describes how to unlink, delete the data in the key tables, and then relink the dual-write environments.</span></span>

<span data-ttu-id="415cf-107">マッピングは Dataverse に格納されるので、リンクを解除および再リンクした場合マッピングは保存されます。</span><span class="sxs-lookup"><span data-stu-id="415cf-107">The mappings are preserved when you unlink and relink, because the mappings are stored in Dataverse.</span></span>

## <a name="scenario-dual-write-is-enabled-between-production-environments"></a><span data-ttu-id="415cf-108">シナリオ: 運用環境間で二重書き込みを有効にする</span><span class="sxs-lookup"><span data-stu-id="415cf-108">Scenario: Dual-write is enabled between production environments</span></span>

<span data-ttu-id="415cf-109">このシナリオでは、 Finance and Operations と Dataverse の間で二重書き込みを有効にします。</span><span class="sxs-lookup"><span data-stu-id="415cf-109">In this scenario, dual-write is enabled between Finance and Operations and Dataverse production environments.</span></span> <span data-ttu-id="415cf-110">Finance and Operations 運用環境 (ソース) をバックアップし、それを Finance and Operations UAT 環境 (出力先) に復元するとします。</span><span class="sxs-lookup"><span data-stu-id="415cf-110">You want to back up the Finance and Operations production environment (source) and restore it to Finance and Operations UAT environment (destination).</span></span> <span data-ttu-id="415cf-111">復元したら、Finance and Operations UAT 環境で次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="415cf-111">Once you restore, follow these steps on the Finance and Operations UAT environment:</span></span>

1. <span data-ttu-id="415cf-112">すべてのテーブル マップを停止します。</span><span class="sxs-lookup"><span data-stu-id="415cf-112">Stop all table maps.</span></span>
2. <span data-ttu-id="415cf-113">Finance and Operations UAT 環境が Dataverse 運用環境を指すように、二重書き込み接続を解除します。</span><span class="sxs-lookup"><span data-stu-id="415cf-113">Unlink the dual-write connection as the Finance and Operations UAT environment will be pointing towards Dataverse production environment.</span></span>
3. <span data-ttu-id="415cf-114">キー テーブルからデータを削除します。</span><span class="sxs-lookup"><span data-stu-id="415cf-114">Delete the data from the key tables.</span></span>

    - <span data-ttu-id="415cf-115">**DualWriteProjectConfiguration**</span><span class="sxs-lookup"><span data-stu-id="415cf-115">**DualWriteProjectConfiguration**</span></span>
    - <span data-ttu-id="415cf-116">**DualWriteFieldConfiguration**</span><span class="sxs-lookup"><span data-stu-id="415cf-116">**DualWriteFieldConfiguration**</span></span>
    - <span data-ttu-id="415cf-117">**BusinessEventsDefinition**</span><span class="sxs-lookup"><span data-stu-id="415cf-117">**BusinessEventsDefinition**</span></span>
    - <span data-ttu-id="415cf-118">**二重書き込みランタイムのコンフィギュレーション**</span><span class="sxs-lookup"><span data-stu-id="415cf-118">**Dual Write Runtime Configurations**</span></span>

4. <span data-ttu-id="415cf-119">Dataverse UAT 環境に対して、Finance and Operations UAT 環境を再リンクすることが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="415cf-119">You may want to relink Finance and Operations UAT environment against Dataverse UAT environment.</span></span> 
5. <span data-ttu-id="415cf-120">マッピングを有効にします。</span><span class="sxs-lookup"><span data-stu-id="415cf-120">Enable the maps.</span></span>

<span data-ttu-id="415cf-121">Dataverse でバックアップおよび復元のプロセスが実行されている場合は、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="415cf-121">If the backup and restore processes are running on Dataverse, then follow these steps:</span></span>

1. <span data-ttu-id="415cf-122">Finance and Operations UAT 環境にサイン インします。</span><span class="sxs-lookup"><span data-stu-id="415cf-122">Sign in to Finance and Operations UAT environment.</span></span>
2. <span data-ttu-id="415cf-123">すべてのテーブル マップを停止します。</span><span class="sxs-lookup"><span data-stu-id="415cf-123">Stop all table maps.</span></span>
3. <span data-ttu-id="415cf-124">Dataverse UAT 環境が Finance and Operations 運用環境を指すように、二重書き込み接続を解除します。</span><span class="sxs-lookup"><span data-stu-id="415cf-124">Unlink the dual-write connection as the Dataverse UAT environment will be pointing towards Finance and Operations production environment.</span></span>
4. <span data-ttu-id="415cf-125">Dataverse でキー テーブルからデータを削除します。</span><span class="sxs-lookup"><span data-stu-id="415cf-125">Delete the data from the key tables on Dataverse.</span></span>

    - <span data-ttu-id="415cf-126">**DualWriteProjectConfiguration**</span><span class="sxs-lookup"><span data-stu-id="415cf-126">**DualWriteProjectConfiguration**</span></span>
    - <span data-ttu-id="415cf-127">**DualWriteFieldConfiguration**</span><span class="sxs-lookup"><span data-stu-id="415cf-127">**DualWriteFieldConfiguration**</span></span>
    - <span data-ttu-id="415cf-128">**BusinessEventsDefinition**</span><span class="sxs-lookup"><span data-stu-id="415cf-128">**BusinessEventsDefinition**</span></span>

5. <span data-ttu-id="415cf-129">Dataverse UAT 環境に対して、Finance and Operations UAT 環境を再リンクすることが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="415cf-129">You may want to relink Finance and Operations UAT environment against Dataverse UAT environment.</span></span>
6. <span data-ttu-id="415cf-130">マッピングを有効にします。</span><span class="sxs-lookup"><span data-stu-id="415cf-130">Enable the maps.</span></span>

## <a name="scenario-reset-or-change-linking"></a><span data-ttu-id="415cf-131">シナリオ: リンクのリセットまたは変更</span><span class="sxs-lookup"><span data-stu-id="415cf-131">Scenario: Reset or change linking</span></span>

<span data-ttu-id="415cf-132">二重書き込みに関連付けられている既存のサンドボックス Dataverse インスタンスをリセットする場合、または別の Dataverse インスタンスにリンクを変更する場合は、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="415cf-132">If you want to reset your existing sandbox Dataverse instance that is linked for dual-write or you want to change the linking to a different Dataverse instance, then follow these steps:</span></span>

1. <span data-ttu-id="415cf-133">Finance and Operations アプリにサインインします。</span><span class="sxs-lookup"><span data-stu-id="415cf-133">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="415cf-134">すべてのエンティティ マップを停止します。</span><span class="sxs-lookup"><span data-stu-id="415cf-134">Stop all entity maps.</span></span>
3. <span data-ttu-id="415cf-135">Finance and Operations アプリと Dataverse の間の二重書き込み接続のリンクを解除します。</span><span class="sxs-lookup"><span data-stu-id="415cf-135">Unlink the dual-write connection between Finance and Operations app and Dataverse.</span></span>
5. <span data-ttu-id="415cf-136">Dataverse 環境をリセットします。</span><span class="sxs-lookup"><span data-stu-id="415cf-136">Reset the Dataverse environment.</span></span>
6. <span data-ttu-id="415cf-137">Finance and Operations アプリでキー テーブルからデータを削除します。</span><span class="sxs-lookup"><span data-stu-id="415cf-137">Delete the data from the key tables in the Finance and Operations app.</span></span>

    - <span data-ttu-id="415cf-138">**DualWriteProjectConfiguration**</span><span class="sxs-lookup"><span data-stu-id="415cf-138">**DualWriteProjectConfiguration**</span></span>
    - <span data-ttu-id="415cf-139">**DualWriteFieldConfiguration**</span><span class="sxs-lookup"><span data-stu-id="415cf-139">**DualWriteFieldConfiguration**</span></span>
    - <span data-ttu-id="415cf-140">**BusinessEventsDefinition**</span><span class="sxs-lookup"><span data-stu-id="415cf-140">**BusinessEventsDefinition**</span></span>

7. <span data-ttu-id="415cf-141">リセットする環境に二重書き込みを設定します。</span><span class="sxs-lookup"><span data-stu-id="415cf-141">Set up dual-write on the environment that you want to reset.</span></span> <span data-ttu-id="415cf-142">詳細については、[システム要求と前提条件](requirements-and-prerequisites.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="415cf-142">For more information, see [System requirements and prerequisites](requirements-and-prerequisites.md).</span></span>

## <a name="known-issues"></a><span data-ttu-id="415cf-143">既知の問題</span><span class="sxs-lookup"><span data-stu-id="415cf-143">Known issues</span></span>

### <a name="secureconfig-organization-error"></a><span data-ttu-id="415cf-144">SecureConfig の組織エラー</span><span class="sxs-lookup"><span data-stu-id="415cf-144">SecureConfig Organization error</span></span>

<span data-ttu-id="415cf-145">環境をコピーした後にレコードをコピー、更新、または削除しようとする場合、**SecureConfig Organization (ProjVcTest4) が実際の CRM 組織 (org6459f7a8_195867911_20200717T174709) と一致しない** というエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="415cf-145">When you try to copy, update, or delete records after copying the environment, the following error appears: **SecureConfig Organization (ProjOpsTest4) does not match actual CRM Organization (org6459f7a8_195867911_20200717T174709)**.</span></span>

<span data-ttu-id="415cf-146">エラーを軽減するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="415cf-146">Follow these steps to mitigate the error:</span></span>

1. <span data-ttu-id="415cf-147">Customer Engagement アプリで、**高度な検索** を選択します。</span><span class="sxs-lookup"><span data-stu-id="415cf-147">In the customer engagement app, select **Advanced find**.</span></span>
2. <span data-ttu-id="415cf-148">**検索** フィールドで、**二重書き込みランタイムのコンフィギュレーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="415cf-148">In the **Look for** field, select **Dual Write Runtime Configurations**.</span></span>
3. <span data-ttu-id="415cf-149">**結果** を選択します。</span><span class="sxs-lookup"><span data-stu-id="415cf-149">Select **Results**.</span></span>
4. <span data-ttu-id="415cf-150">行が表示されます。</span><span class="sxs-lookup"><span data-stu-id="415cf-150">Rows will be displayed.</span></span> <span data-ttu-id="415cf-151">すべての行を選択します。</span><span class="sxs-lookup"><span data-stu-id="415cf-151">Select all the rows.</span></span>
5. <span data-ttu-id="415cf-152">**削除** アイコンを選択します。</span><span class="sxs-lookup"><span data-stu-id="415cf-152">Select the **Delete** icon.</span></span>

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
