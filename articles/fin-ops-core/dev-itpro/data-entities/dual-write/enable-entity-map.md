---
title: テーブル マップの二重書き込みの有効化
description: このトピックでは、テーブル マップが二重書き込みでどのように機能するかついて説明します。
author: sabinn-msft
manager: AnnBe
ms.date: 03/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Developer
ms.reviewer: v-douklo
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sabinn
ms.search.validFrom: 2020-03-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7df10e8b7eebad016a901bf9b3780220376c1d33
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744709"
---
# <a name="enable-table-maps-for-dual-write"></a><span data-ttu-id="12f1a-103">テーブル マップの二重書き込みの有効化</span><span class="sxs-lookup"><span data-stu-id="12f1a-103">Enable table maps for dual-write</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="12f1a-104">テーブル マップの二重書き込みを有効にすると、**実行していません** 状態で開始されます。</span><span class="sxs-lookup"><span data-stu-id="12f1a-104">When you enable a table map for dual-write, it begins at the **Not running** status.</span></span> <span data-ttu-id="12f1a-105">次に、テーブル マップは初期化フェーズを実行し、両側のテーブルに既存のデータをコピーすることにより初期書き込みを行います。</span><span class="sxs-lookup"><span data-stu-id="12f1a-105">The table map then goes through an initialization phase, where it does an initial write by copying pre-existing data on tables on both sides.</span></span> <span data-ttu-id="12f1a-106">最後に、テーブルが完全に有効化されると、テーブル マップは状態を **実行中** に設定します。</span><span class="sxs-lookup"><span data-stu-id="12f1a-106">Finally, when the table is completely enabled, the table map sets the status to **Running**.</span></span>

![テーブル マップの有効化](media/enabling-entity-map.png)

<span data-ttu-id="12f1a-108">状態が **実行中** の間、テーブルを一時停止できます。</span><span class="sxs-lookup"><span data-stu-id="12f1a-108">While the status is **Running**, you can pause a table.</span></span> <span data-ttu-id="12f1a-109">その後、すべての変更は、再開するまでキューに配置されます。</span><span class="sxs-lookup"><span data-stu-id="12f1a-109">All changes are then queued until you resume.</span></span> <span data-ttu-id="12f1a-110">再開すると、テーブルは "キャッチ アップ モード" になり、キューに入れられたすべての変更が再生されます。</span><span class="sxs-lookup"><span data-stu-id="12f1a-110">When you resume, the table goes into "catch-up mode," where all the queued changes are played back.</span></span>

<span data-ttu-id="12f1a-111">次の図で、一時停止しているテーブルの例を示します。</span><span class="sxs-lookup"><span data-stu-id="12f1a-111">The following illustration show an example of a table that is paused.</span></span>

![一時停止したテーブル](media/stop-pause-entity.png)

| <span data-ttu-id="12f1a-113">状態</span><span class="sxs-lookup"><span data-stu-id="12f1a-113">Status</span></span> | <span data-ttu-id="12f1a-114">説明</span><span class="sxs-lookup"><span data-stu-id="12f1a-114">Description</span></span> | <span data-ttu-id="12f1a-115">使用可能なアクション</span><span class="sxs-lookup"><span data-stu-id="12f1a-115">Available actions</span></span> |
|---|---|---|
| <span data-ttu-id="12f1a-116">実行していません</span><span class="sxs-lookup"><span data-stu-id="12f1a-116">Not running</span></span> | <span data-ttu-id="12f1a-117">テーブルでは、まだ二重書き込みが有効になっていません。</span><span class="sxs-lookup"><span data-stu-id="12f1a-117">The table has not yet been enabled for dual-write.</span></span> <span data-ttu-id="12f1a-118">すべてのテーブルは、**実行していません** 状態で開始します。</span><span class="sxs-lookup"><span data-stu-id="12f1a-118">Every table begins at the **Not running** status.</span></span> | <span data-ttu-id="12f1a-119">実行</span><span class="sxs-lookup"><span data-stu-id="12f1a-119">Run</span></span> |
| <span data-ttu-id="12f1a-120">初期化</span><span class="sxs-lookup"><span data-stu-id="12f1a-120">Initializing</span></span> | <span data-ttu-id="12f1a-121">最初の書き込みが発生しています。</span><span class="sxs-lookup"><span data-stu-id="12f1a-121">The initial write is occurring.</span></span> | <span data-ttu-id="12f1a-122">None</span><span class="sxs-lookup"><span data-stu-id="12f1a-122">None</span></span> |
| <span data-ttu-id="12f1a-123">実行中</span><span class="sxs-lookup"><span data-stu-id="12f1a-123">Running</span></span> | <span data-ttu-id="12f1a-124">テーブルの二重書き込みが有効になっています。</span><span class="sxs-lookup"><span data-stu-id="12f1a-124">The table has been enabled for dual-write.</span></span> | <span data-ttu-id="12f1a-125">停止、 一時停止</span><span class="sxs-lookup"><span data-stu-id="12f1a-125">Stop, Pause</span></span> |
| <span data-ttu-id="12f1a-126">一時停止</span><span class="sxs-lookup"><span data-stu-id="12f1a-126">Paused</span></span> | <span data-ttu-id="12f1a-127">テーブルは一時停止状態にあり、すべての新しい要求がキューに入れられます。</span><span class="sxs-lookup"><span data-stu-id="12f1a-127">The table is in a paused state, and all new requests are queued.</span></span> | <span data-ttu-id="12f1a-128">実行</span><span class="sxs-lookup"><span data-stu-id="12f1a-128">Run</span></span> |
| <span data-ttu-id="12f1a-129">再開中</span><span class="sxs-lookup"><span data-stu-id="12f1a-129">Resuming</span></span> | <span data-ttu-id="12f1a-130">テーブルは、テーブルが一時停止中にキューに入れられた行を処理します。</span><span class="sxs-lookup"><span data-stu-id="12f1a-130">The table is catching up on rows that were queued while the table was paused.</span></span> | <span data-ttu-id="12f1a-131">None</span><span class="sxs-lookup"><span data-stu-id="12f1a-131">None</span></span> |

<span data-ttu-id="12f1a-132">初期化フェーズでは、既存のデータが初期書き込みフェーズの一部としてコピーされます。</span><span class="sxs-lookup"><span data-stu-id="12f1a-132">During the initialization phase, any pre-existing data that you have is copied as part of the initial write phase.</span></span>

![既存のデータのコピー](media/initial-write-phase.png)

<span data-ttu-id="12f1a-134">エンティティには複数の依存テーブルがあります。</span><span class="sxs-lookup"><span data-stu-id="12f1a-134">Entities have several dependent tables.</span></span> <span data-ttu-id="12f1a-135">たとえば、顧客-連絡先テーブルには、顧客グループと通貨が依存テーブルとしてあります。</span><span class="sxs-lookup"><span data-stu-id="12f1a-135">For example, Customer-Contact tables have customer groups and currencies as dependent tables.</span></span>

![依存テーブル](media/dependent-or-related-entities.png)

<span data-ttu-id="12f1a-137">これらはリレーショナル データを持つリレーショナル アプリであるため、依存テーブルを有効にしないと、後でエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="12f1a-137">Because these are relational apps that have relational data, if you don't enable the dependent tables, you might encounter errors later.</span></span> <span data-ttu-id="12f1a-138">これらのエラーを防ぐために、テーブル マップを有効にする前に、有効にすることを推奨する関連テーブルの一覧が提供されます。</span><span class="sxs-lookup"><span data-stu-id="12f1a-138">To help prevent these errors, before you enable a table map, you're provided with a list of the related tables that we recommend that you enable.</span></span>

## <a name="example-enabling-the-customers-v3contacts-table-map"></a><a id="enable-table-map"></a> <span data-ttu-id="12f1a-139">例: 顧客 V3 の有効化—連絡先テーブル マップ</span><span class="sxs-lookup"><span data-stu-id="12f1a-139">Example: Enabling the Customers V3—Contacts table map</span></span>

<span data-ttu-id="12f1a-140">テーブル マップ (たとえば、**顧客 V3—連絡先**) を選択して、**実行** を選択すると、テーブル マップが有効になる前にダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="12f1a-140">When you select a table map (for example, **Customers V3—Contacts**) and select **Run**, a dialog box appears before the table map is enabled.</span></span> <span data-ttu-id="12f1a-141">このダイアログ ボックスには、すべての依存テーブルが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="12f1a-141">This dialog box lists all the dependent tables.</span></span> <span data-ttu-id="12f1a-142">**関連テーブル マップの表示** オプションを選択すると、すべての関連するテーブル マップを表示できます。</span><span class="sxs-lookup"><span data-stu-id="12f1a-142">You can select the **Show related table map(s)** option to show all the related table maps.</span></span> <span data-ttu-id="12f1a-143">選択したテーブル マップおよびそれに関連するすべてのテーブルを有効にするには、ダイアログ ボックスの **実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="12f1a-143">To enable the selected table map and all its related tables, select **Run** in the dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="12f1a-144">テーブルを一時停止したときの動作も同様です。</span><span class="sxs-lookup"><span data-stu-id="12f1a-144">The behavior is similar when you pause a table.</span></span> <span data-ttu-id="12f1a-145">その場合は、すべての関連するテーブルを一時停止することもできます。</span><span class="sxs-lookup"><span data-stu-id="12f1a-145">In that case, you have the option to pause all the related tables too.</span></span>

![すべての依存テーブルの一覧表示](media/related-entity-maps.png)

<span data-ttu-id="12f1a-147">競合を解決するために使用する別のマスターを指定することによって、これをさらにカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="12f1a-147">You can further customize this by specifying a different master that should be used to resolve conflicts.</span></span> <span data-ttu-id="12f1a-148">(既定では、Dataverse が使用されます。) 既存のデータをコピーしない場合は、**初期同期** チェック ボックスをオフにして、初期同期をスキップします。</span><span class="sxs-lookup"><span data-stu-id="12f1a-148">(By default, Dataverse is used.) If you don't want to copy pre-existing data, skip the initial synchronization by clearing the **Initial Sync** check box.</span></span> <span data-ttu-id="12f1a-149">または、1 つ以上の関連テーブルの選択をキャンセルして、それらを解除します。</span><span class="sxs-lookup"><span data-stu-id="12f1a-149">Alternatively, remove one or more of the related tables by canceling the selection of them.</span></span> <span data-ttu-id="12f1a-150">テーブル マップをドラッグして、同期される順序を変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="12f1a-150">You can also drag the table maps to change the order that they will be synced in.</span></span>

<span data-ttu-id="12f1a-151">ダイアログ ボックスで選択を完了し、**実行** を選択すると、テーブル マップおよび関連するすべてのテーブルが初期書き込みフェーズを実行します。</span><span class="sxs-lookup"><span data-stu-id="12f1a-151">After you've finished making your selections in the dialog box, and you select **Run**, the table map and all its related tables go through the initial write phase.</span></span> <span data-ttu-id="12f1a-152">テーブル マップ一覧ページにリダイレクトされます。</span><span class="sxs-lookup"><span data-stu-id="12f1a-152">You're redirected to the table map list page.</span></span> <span data-ttu-id="12f1a-153">エラーが発生した場合は、**初回同期の詳細** タブで詳細を確認できます。このタブでは、既存のデータのコピー中に発生するすべてのエラーの詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="12f1a-153">If any errors occur, you can view the details on the **Initial sync details** tab. This tab provides details about all the errors that occur while pre-existing data is being copied.</span></span> <span data-ttu-id="12f1a-154">原因となっているエラーを修正した後、実行を再実行し、結果を監視できます。</span><span class="sxs-lookup"><span data-stu-id="12f1a-154">After you fix the underlying errors, you can rerun the execution and monitor the outcome.</span></span> <span data-ttu-id="12f1a-155">または、既存のデータを同期する必要がなくなった場合や、基になるデータが原因で繰り返し問題が発生する場合は、初期書き込みフェーズをスキップできます。</span><span class="sxs-lookup"><span data-stu-id="12f1a-155">Alternatively, if you no longer want to sync the pre-existing data, or if you experience recurring issues because of underlying data, you can skip the initial write phase.</span></span> <span data-ttu-id="12f1a-156">代わりに、**初期同期をスキップ** を選択して、ライブ書き込みを有効にできます。</span><span class="sxs-lookup"><span data-stu-id="12f1a-156">Instead, you can turn on live writes by selecting **Skip initial sync**.</span></span>

![初期書き込みのスキップ](media/skip-initial-writes.png)

## <a name="criteria-for-linking-tables"></a><a id="criteria-for-linking"></a> <span data-ttu-id="12f1a-158">テーブルをリンクするための基準</span><span class="sxs-lookup"><span data-stu-id="12f1a-158">Criteria for linking tables</span></span>

<span data-ttu-id="12f1a-159">テーブル マップの二重書き込みを有効にするには、Dataverse で代替キーを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="12f1a-159">To enable table maps for dual-write, you must define an alternative key in Dataverse.</span></span> <span data-ttu-id="12f1a-160">Dataverse の代替キーの値は、Finance and Operations アプリで定義されているキーと一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="12f1a-160">The value of the alternative key in Dataverse must match the key that is defined in the Finance and Operations app.</span></span>

<span data-ttu-id="12f1a-161">たとえば、Finance and Operations アプリでは、**CustomerAccount** がアカウント テーブルのキーです。</span><span class="sxs-lookup"><span data-stu-id="12f1a-161">For example, in a Finance and Operations app, **CustomerAccount** is the key for the Account table.</span></span>

![Finance and Operations アプリでのアカウント テーブルのキー](media/define-alternative-key.png)

<span data-ttu-id="12f1a-163">Dataverse では、**accountnumber** はアカウント テーブルのキーとして定義されます。</span><span class="sxs-lookup"><span data-stu-id="12f1a-163">In Dataverse, **accountnumber** is defined as the key for the Account table.</span></span>

![Dataverse で定義されたアカウント テーブル](media/define-account-entity.png)

<span data-ttu-id="12f1a-165">顧客 V3 テーブル マップでは、**accountnumber** が **CustomerAccount** にマップされていることがわかります。</span><span class="sxs-lookup"><span data-stu-id="12f1a-165">In the Customers V3 table map, you can see that **accountnumber** is mapped to **CustomerAccount**.</span></span>

![テーブル マップでのマッピング](media/mapped-to-entity-map.png)

## <a name="next-steps"></a><span data-ttu-id="12f1a-167">次のステップ</span><span class="sxs-lookup"><span data-stu-id="12f1a-167">Next steps</span></span>

[<span data-ttu-id="12f1a-168">テーブル マッピングと列マッピングのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="12f1a-168">Customize table and column mappings</span></span>](customizing-mappings.md)
