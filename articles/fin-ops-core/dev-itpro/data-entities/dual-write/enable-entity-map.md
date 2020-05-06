---
title: エンティティ マップの二重書き込みの有効化
description: このトピックでは、エンティティ マップが二重書き込みでどのように機能するかついて説明します。
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
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sabinn
ms.search.validFrom: 2020-03-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a2ceadd0906699a475ceec5b1ad2b511385f946c
ms.sourcegitcommit: e9fadf6f6dafdcefaff8e23eaa3c85f53437db3f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/22/2020
ms.locfileid: "3279123"
---
# <a name="enable-entity-maps-for-dual-write"></a><span data-ttu-id="1bc92-103">エンティティ マップの二重書き込みの有効化</span><span class="sxs-lookup"><span data-stu-id="1bc92-103">Enable entity maps for dual-write</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="1bc92-104">エンティティ マップの二重書き込みを有効にすると、**実行していません** 状態で開始されます。</span><span class="sxs-lookup"><span data-stu-id="1bc92-104">When you enable an entity map for dual-write, it begins at the **Not running** status.</span></span> <span data-ttu-id="1bc92-105">次に、エンティティ マップは初期化フェーズを実行し、両側のエンティティに既存のデータをコピーすることにより初期書き込みを行います。</span><span class="sxs-lookup"><span data-stu-id="1bc92-105">The entity map then goes through an initialization phase, where it does an initial write by copying pre-existing data on entities on both sides.</span></span> <span data-ttu-id="1bc92-106">最後に、エンティティが完全に有効化されると、エンティティ マップは状態を **実行中** に設定します。</span><span class="sxs-lookup"><span data-stu-id="1bc92-106">Finally, when the entity is completely enabled, the entity map sets the status to **Running**.</span></span>

![エンティティ マップの有効化](media/enabling-entity-map.png)

<span data-ttu-id="1bc92-108">状態が **実行中** の間、エンティティを一時停止できます。</span><span class="sxs-lookup"><span data-stu-id="1bc92-108">While the status is **Running**, you can pause an entity.</span></span> <span data-ttu-id="1bc92-109">その後、すべての変更は、再開するまでキューに配置されます。</span><span class="sxs-lookup"><span data-stu-id="1bc92-109">All changes are then queued until you resume.</span></span> <span data-ttu-id="1bc92-110">再開すると、エンティティは "キャッチ アップ モード" になり、キューに入れられたすべての変更が再生されます。</span><span class="sxs-lookup"><span data-stu-id="1bc92-110">When you resume, the entity goes into "catch-up mode," where all the queued changes are played back.</span></span>

<span data-ttu-id="1bc92-111">次の図で、一時停止しているエンティティの例を示します。</span><span class="sxs-lookup"><span data-stu-id="1bc92-111">The following illustration show an example of an entity that is paused.</span></span>

![一時停止したエンティティ](media/stop-pause-entity.png)

| <span data-ttu-id="1bc92-113">ステータス</span><span class="sxs-lookup"><span data-stu-id="1bc92-113">Status</span></span> | <span data-ttu-id="1bc92-114">説明</span><span class="sxs-lookup"><span data-stu-id="1bc92-114">Description</span></span> | <span data-ttu-id="1bc92-115">使用可能なアクション</span><span class="sxs-lookup"><span data-stu-id="1bc92-115">Available actions</span></span> |
|---|---|---|
| <span data-ttu-id="1bc92-116">実行していません</span><span class="sxs-lookup"><span data-stu-id="1bc92-116">Not running</span></span> | <span data-ttu-id="1bc92-117">エンティティは、まだ二重書き込みが有効になっていません。</span><span class="sxs-lookup"><span data-stu-id="1bc92-117">The entity has not yet been enabled for dual-write.</span></span> <span data-ttu-id="1bc92-118">すべてのエンティティは、**実行していません** 状態で開始します。</span><span class="sxs-lookup"><span data-stu-id="1bc92-118">Every entity begins at the **Not running** status.</span></span> | <span data-ttu-id="1bc92-119">実行</span><span class="sxs-lookup"><span data-stu-id="1bc92-119">Run</span></span> |
| <span data-ttu-id="1bc92-120">初期化</span><span class="sxs-lookup"><span data-stu-id="1bc92-120">Initializing</span></span> | <span data-ttu-id="1bc92-121">最初の書き込みが発生しています。</span><span class="sxs-lookup"><span data-stu-id="1bc92-121">The initial write is occurring.</span></span> | <span data-ttu-id="1bc92-122">None</span><span class="sxs-lookup"><span data-stu-id="1bc92-122">None</span></span> |
| <span data-ttu-id="1bc92-123">実行中</span><span class="sxs-lookup"><span data-stu-id="1bc92-123">Running</span></span> | <span data-ttu-id="1bc92-124">エンティティの二重書き込みが有効になっています。</span><span class="sxs-lookup"><span data-stu-id="1bc92-124">The entity has been enabled for dual-write.</span></span> | <span data-ttu-id="1bc92-125">停止、 一時停止</span><span class="sxs-lookup"><span data-stu-id="1bc92-125">Stop, Pause</span></span> |
| <span data-ttu-id="1bc92-126">一時停止</span><span class="sxs-lookup"><span data-stu-id="1bc92-126">Paused</span></span> | <span data-ttu-id="1bc92-127">エンティティは一時停止状態にあり、すべての新しい要求がキューに入れられます。</span><span class="sxs-lookup"><span data-stu-id="1bc92-127">The entity is in a paused state, and all new requests are queued.</span></span> | <span data-ttu-id="1bc92-128">実行</span><span class="sxs-lookup"><span data-stu-id="1bc92-128">Run</span></span> |
| <span data-ttu-id="1bc92-129">再開中</span><span class="sxs-lookup"><span data-stu-id="1bc92-129">Resuming</span></span> | <span data-ttu-id="1bc92-130">エンティティは、エンティティが一時停止中にキューに入れられたレコードを処理します。</span><span class="sxs-lookup"><span data-stu-id="1bc92-130">The entity is catching up on records that were queued while the entity was paused.</span></span> | <span data-ttu-id="1bc92-131">None</span><span class="sxs-lookup"><span data-stu-id="1bc92-131">None</span></span> |

<span data-ttu-id="1bc92-132">初期化フェーズでは、既存のデータが初期書き込みフェーズの一部としてコピーされます。</span><span class="sxs-lookup"><span data-stu-id="1bc92-132">During the initialization phase, any pre-existing data that you have is copied as part of the initial write phase.</span></span>

![既存のデータのコピー](media/initial-write-phase.png)

<span data-ttu-id="1bc92-134">エンティティには複数の依存エンティティがあります。</span><span class="sxs-lookup"><span data-stu-id="1bc92-134">Entities have several dependent entities.</span></span> <span data-ttu-id="1bc92-135">たとえば、顧客-連絡先エンティティには、顧客グループと通貨が依存エンティティとしてあります。</span><span class="sxs-lookup"><span data-stu-id="1bc92-135">For example, Customer-Contact entities have customer groups and currencies as dependent entities.</span></span>

![依存エンティティ](media/dependent-or-related-entities.png)

<span data-ttu-id="1bc92-137">これらはリレーショナル データを持つリレーショナル アプリであるため、依存エンティティを有効にしないと、後でエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1bc92-137">Because these are relational apps that have relational data, if you don't enable the dependent entities, you might encounter errors later.</span></span> <span data-ttu-id="1bc92-138">これらのエラーを防ぐために、エンティティ マップを有効にする前に、有効にすることを推奨する関連エンティティの一覧が提供されます。</span><span class="sxs-lookup"><span data-stu-id="1bc92-138">To help prevent these errors, before you enable an entity map, you're provided with a list of the related entities that we recommend that you enable.</span></span>

## <a name="example-enabling-the-customers-v3contacts-entity-map"></a><span data-ttu-id="1bc92-139">例: 顧客 V3の有効化—連絡先エンティティ マップ</span><span class="sxs-lookup"><span data-stu-id="1bc92-139">Example: Enabling the Customers V3—Contacts entity map</span></span>

<span data-ttu-id="1bc92-140">エンティティ マップ (たとえば、**顧客 V3—連絡先**) を選択して、**実行** を選択すると、エンティティ マップが有効になる前にダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1bc92-140">When you select an entity map (for example, **Customers V3—Contacts**) and select **Run**, a dialog box appears before the entity map is enabled.</span></span> <span data-ttu-id="1bc92-141">このダイアログ ボックスには、すべての依存エンティティが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="1bc92-141">This dialog box lists all the dependent entities.</span></span> <span data-ttu-id="1bc92-142">**関連エンティティ マップの表示** オプションを選択すると、すべての関連するエンティティ マップを表示できます。</span><span class="sxs-lookup"><span data-stu-id="1bc92-142">You can select the **Show related entity map(s)** option to show all the related entity maps.</span></span> <span data-ttu-id="1bc92-143">選択したエンティティ マップとそれに関連するすべてのエンティティを有効にするには、ダイアログ ボックスの **実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1bc92-143">To enable the selected entity map and all its related entities, select **Run** in the dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="1bc92-144">エンティティを一時停止したときの動作も同様です。</span><span class="sxs-lookup"><span data-stu-id="1bc92-144">The behavior is similar when you pause an entity.</span></span> <span data-ttu-id="1bc92-145">その場合は、すべての関連するエンティティを一時停止することもできます。</span><span class="sxs-lookup"><span data-stu-id="1bc92-145">In that case, you have the option to pause all the related entities too.</span></span>

![すべての依存エンティティの一覧表示](media/related-entity-maps.png)

<span data-ttu-id="1bc92-147">競合を解決するために使用する別のマスターを指定することによって、これをさらにカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="1bc92-147">You can further customize this by specifying a different master that should be used to resolve conflicts.</span></span> <span data-ttu-id="1bc92-148">(既定では、Common Data Service が使用されます。) 既存のデータをコピーしない場合は、**初期同期** チェック ボックスをオフにして、初期同期をスキップします。</span><span class="sxs-lookup"><span data-stu-id="1bc92-148">(By default, Common Data Service is used.) If you don't want to copy pre-existing data, skip the initial synchronization by clearing the **Initial Sync** check box.</span></span> <span data-ttu-id="1bc92-149">または、1 つ以上の関連エンティティの選択をキャンセルして、それらを解除します。</span><span class="sxs-lookup"><span data-stu-id="1bc92-149">Alternatively, remove one or more of the related entities by canceling the selection of them.</span></span> <span data-ttu-id="1bc92-150">エンティティ マップをドラッグして、同期される順序を変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="1bc92-150">You can also drag the entity maps to change the order that they will be synced in.</span></span>

<span data-ttu-id="1bc92-151">ダイアログ ボックスで選択を完了し、**実行** を選択すると、エンティティ マップと関連するすべてのエンティティが初期書き込みフェーズを実行します。</span><span class="sxs-lookup"><span data-stu-id="1bc92-151">After you've finished making your selections in the dialog box, and you select **Run**, the entity map and all its related entities go through the initial write phase.</span></span> <span data-ttu-id="1bc92-152">エンティティ マップ一覧ページにリダイレクトされます。</span><span class="sxs-lookup"><span data-stu-id="1bc92-152">You're redirected to the entity map list page.</span></span> <span data-ttu-id="1bc92-153">エラーが発生した場合は、**初回同期の詳細** タブで詳細を確認できます。このタブでは、既存のデータのコピー中に発生するすべてのエラーの詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="1bc92-153">If any errors occur, you can view the details on the **Initial sync details** tab. This tab provides details about all the errors that occur while pre-existing data is being copied.</span></span> <span data-ttu-id="1bc92-154">原因となっているエラーを修正した後、実行を再実行し、結果を監視できます。</span><span class="sxs-lookup"><span data-stu-id="1bc92-154">After you fix the underlying errors, you can rerun the execution and monitor the outcome.</span></span> <span data-ttu-id="1bc92-155">または、既存のデータを同期する必要がなくなった場合や、基になるデータが原因で繰り返し問題が発生する場合は、初期書き込みフェーズをスキップできます。</span><span class="sxs-lookup"><span data-stu-id="1bc92-155">Alternatively, if you no longer want to sync the pre-existing data, or if you experience recurring issues because of underlying data, you can skip the initial write phase.</span></span> <span data-ttu-id="1bc92-156">代わりに、**初期同期をスキップ** を選択して、ライブ書き込みを有効にできます。</span><span class="sxs-lookup"><span data-stu-id="1bc92-156">Instead, you can turn on live writes by selecting **Skip initial sync**.</span></span>

![初期書き込みのスキップ](media/skip-initial-writes.png)

## <a name="criteria-for-linking-entities"></a><span data-ttu-id="1bc92-158">エンティティをリンクするための基準</span><span class="sxs-lookup"><span data-stu-id="1bc92-158">Criteria for linking entities</span></span>

<span data-ttu-id="1bc92-159">エンティティ マップの二重書き込みを有効にするには、Common Data Service で代替キーを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1bc92-159">To enable entity maps for dual-write, you must define an alternative key in Common Data Service.</span></span> <span data-ttu-id="1bc92-160">Common Data Service の代替キーの値は、Finance and Operations アプリで定義されているキーと一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1bc92-160">The value of the alternative key in Common Data Service must match the key that is defined in the Finance and Operations app.</span></span>

<span data-ttu-id="1bc92-161">たとえば、Finance and Operations アプリでは、**CustomerAccount** がアカウント エンティティのキーです。</span><span class="sxs-lookup"><span data-stu-id="1bc92-161">For example, in a Finance and Operations app, **CustomerAccount** is the key for the Account entity.</span></span>

![Finance and Operations アプリでのアカウント エンティティのキー](media/define-alternative-key.png)

<span data-ttu-id="1bc92-163">Common Data Service では、**accountnumber** はアカウント エンティティのキーとして定義されます。</span><span class="sxs-lookup"><span data-stu-id="1bc92-163">In Common Data Service, **accountnumber** is defined as the key for the Account entity.</span></span>

![Common Data Service で定義されたアカウント エンティティ](media/define-account-entity.png)

<span data-ttu-id="1bc92-165">顧客 V3 エンティティ マップでは、**accountnumber** が **CustomerAccount** にマップされていることがわかります。</span><span class="sxs-lookup"><span data-stu-id="1bc92-165">In the Customers V3 entity map, you can see that **accountnumber** is mapped to **CustomerAccount**.</span></span>

![エンティティ マップでのマッピング](media/mapped-to-entity-map.png)

## <a name="next-steps"></a><span data-ttu-id="1bc92-167">次のステップ</span><span class="sxs-lookup"><span data-stu-id="1bc92-167">Next steps</span></span>

[<span data-ttu-id="1bc92-168">エンティティとフィールドのマッピングのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="1bc92-168">Customize entity and field mappings</span></span>](customizing-mappings.md)
