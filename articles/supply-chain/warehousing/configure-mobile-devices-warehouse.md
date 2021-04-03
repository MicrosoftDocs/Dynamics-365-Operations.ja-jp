---
title: 倉庫作業用のモバイル デバイスの設定
description: このトピックでは、倉庫作業者がモバイル デバイスで作業を実行するために使用するメニュー項目をコンフィギュレーションする方法について説明します。
author: MarkusFogelberg
manager: tfehr
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFSysDirSort, WHSWorkUserDisplaySettings
audience: Application User
ms.reviewer: kamaybac
ms.custom: 29941
ms.assetid: 6dff6313-dc6e-4f06-9c0c-dab24eefe4da
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db4c3a8c4bae226b5e154f4761e30b7341bc527b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232986"
---
# <a name="set-up-mobile-devices-for-warehouse-work"></a><span data-ttu-id="c4383-103">倉庫作業用のモバイル デバイスの設定</span><span class="sxs-lookup"><span data-stu-id="c4383-103">Set up mobile devices for warehouse work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c4383-104">このトピックでは、倉庫作業者がモバイル デバイスで作業を実行するために使用するメニュー項目をコンフィギュレーションする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c4383-104">This topic describes how to configure the menu items that warehouse workers use to perform work on a mobile device.</span></span>

> [!NOTE]
> <span data-ttu-id="c4383-105">このトピックは、倉庫管理の機能に適用されます。</span><span class="sxs-lookup"><span data-stu-id="c4383-105">This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="c4383-106">在庫管理の機能には適用しません。</span><span class="sxs-lookup"><span data-stu-id="c4383-106">It doesn't apply to features in Inventory management.</span></span> <span data-ttu-id="c4383-107">倉庫のモバイル デバイスのメニューに表示されるメニュー項目は、**モバイル デバイスのメニュー項目** ページで構成できます。</span><span class="sxs-lookup"><span data-stu-id="c4383-107">The menu items that appear on the menus on a warehouse mobile device are configured on the **Mobile device menu items** page.</span></span> <span data-ttu-id="c4383-108">メニュー項目は異なるメニューに配置できるため、構造化されたメニューを構成して、特定のタイプの作業が特定のユーザーにのみ公開されるようにするのが簡単です。</span><span class="sxs-lookup"><span data-stu-id="c4383-108">Because the menu items can be put onto different menus, it's easy to configure menu structures so that only specific types of work are exposed to specific users.</span></span> <span data-ttu-id="c4383-109">メニュー項目をコンフィギュレーションして、次のタスクを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="c4383-109">You can configure menu items to perform the following tasks:</span></span>

- <span data-ttu-id="c4383-110">照会の処理や活動の実行を行います。これには、ラベルの印刷、ライセンス プレート番号の生成、製造オーダーの開始、任意の場所にある品目に関する情報の迅速な検索などが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c4383-110">Process an inquiry or perform an activity, such as printing a label, generating license plate numbers, starting a production order, or quickly looking up information about items in a location.</span></span>
- <span data-ttu-id="c4383-111">別のプロセスで実行される作業を作成します。</span><span class="sxs-lookup"><span data-stu-id="c4383-111">Create work that will be performed through another process.</span></span> <span data-ttu-id="c4383-112">たとえば、発注書の品目の入荷により、別の作業者のプット アウェイ作業を作成できます。</span><span class="sxs-lookup"><span data-stu-id="c4383-112">For example, receiving an item for a purchase order can create put-away work for another worker.</span></span>
- <span data-ttu-id="c4383-113">別のプロセス (既存の作業) で作成した作業を実行します。これには、発注書の品目が入庫されたときに作成されたプット アウェイ作業などが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c4383-113">Perform work that was created by another process (existing work), such as put-away work that was created when an item was received for a purchase order.</span></span>

<span data-ttu-id="c4383-114">活動または照会のメニュー項目を作成するには、**モード** フィールドを **間接** に設定します。</span><span class="sxs-lookup"><span data-stu-id="c4383-114">To create a menu item for an activity or inquiry, set the **Mode** field to **Indirect**.</span></span> <span data-ttu-id="c4383-115">**活動コード** オプションのリストが有効になり、メニュー項目の対象にする照会または活動のタイプを選択できるようになります。</span><span class="sxs-lookup"><span data-stu-id="c4383-115">A list of **Activity code** options then becomes available, so that you can select the type of inquiry or activity that the menu item is for.</span></span> <span data-ttu-id="c4383-116">倉庫の作業を生成するメニュー項目を作成するには、**モード** フィールドを **作業** に設定します。</span><span class="sxs-lookup"><span data-stu-id="c4383-116">To create a menu item to generate warehouse work, set the **Mode** field to **Work**.</span></span> <span data-ttu-id="c4383-117">**作業作成プロセス** オプションの一覧が使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="c4383-117">A list of **Work creation process** options then becomes available.</span></span> <span data-ttu-id="c4383-118">既存の倉庫の作業を処理するメニュー項目を作成するには、**モード** フィールドを **作業** に設定し、**既存の作業を使用** オプションを **はい** に設定します 。</span><span class="sxs-lookup"><span data-stu-id="c4383-118">To create a menu item to process existing warehouse work, set the **Mode** field to **Work**, and then set the **Use existing work** option to **Yes**.</span></span> 

> [!NOTE]
> <span data-ttu-id="c4383-119">メニュー項目で使用できる追加のフィールドがある場合があります。これは、メニュー項目に選択したモード、およびメニュー項目を既存の作業の実行に使うかどうかによります。</span><span class="sxs-lookup"><span data-stu-id="c4383-119">Additional fields might be available for menu items, depending on the mode that you select for the menu item, and whether the menu item is used to perform existing work.</span></span> <span data-ttu-id="c4383-120">追加のフィールドのオプションの詳細については、このトピックの後半の “追加メニュー項目のオプション” を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c4383-120">For information about the additional field selections, see the “Additional menu item options” section later in this topic.</span></span>

## <a name="configure-menu-items-for-activities-and-inquiries"></a><span data-ttu-id="c4383-121">活動および照会のメニュー項目の構成</span><span class="sxs-lookup"><span data-stu-id="c4383-121">Configure menu items for activities and inquiries</span></span>
<span data-ttu-id="c4383-122">メニュー項目の **モード** フィールドが **間接** に設定されている場合、作業を作成せずに一般的な活動や照会を実行するメニュー項目を作成できます。</span><span class="sxs-lookup"><span data-stu-id="c4383-122">If the **Mode** field for a menu item is set to **Indirect**, you can create a menu item to perform a general activity or inquiry that doesn't create work.</span></span> <span data-ttu-id="c4383-123">たとえば、ライセンス プレート ラベルの再印刷や、場所の品目に関する照会などが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c4383-123">Examples include reprinting license plate labels and an inquiry about the items in a location.</span></span> <span data-ttu-id="c4383-124">次の表に、使用できるオプションを示します。</span><span class="sxs-lookup"><span data-stu-id="c4383-124">The following table lists the options that are available.</span></span>

| <span data-ttu-id="c4383-125">オプション</span><span class="sxs-lookup"><span data-stu-id="c4383-125">Option</span></span> | <span data-ttu-id="c4383-126">説明</span><span class="sxs-lookup"><span data-stu-id="c4383-126">Description</span></span> |
|---|---|
| <span data-ttu-id="c4383-127">なし</span><span class="sxs-lookup"><span data-stu-id="c4383-127">None</span></span> | <span data-ttu-id="c4383-128">この既定値は、活動も照会も有効にしません。</span><span class="sxs-lookup"><span data-stu-id="c4383-128">This default value doesn't enable an activity or inquiry.</span></span> |
| <span data-ttu-id="c4383-129">情報</span><span class="sxs-lookup"><span data-stu-id="c4383-129">About</span></span> | <span data-ttu-id="c4383-130">バージョン番号、倉庫 ID、および現在ログオンしている作業者などの、システムに関する情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="c4383-130">View information about the system, such as the version number, the warehouse ID, and the worker who is currently logged on.</span></span> |
| <span data-ttu-id="c4383-131">倉庫の変更</span><span class="sxs-lookup"><span data-stu-id="c4383-131">Change warehouse</span></span> | <span data-ttu-id="c4383-132">作業者がログオンする倉庫を変更します。</span><span class="sxs-lookup"><span data-stu-id="c4383-132">Change the warehouse that a worker is logged on to.</span></span> |
| <span data-ttu-id="c4383-133">場所の照会</span><span class="sxs-lookup"><span data-stu-id="c4383-133">Location inquiry</span></span> | <span data-ttu-id="c4383-134">場所のすべての品目と数量に関する情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="c4383-134">View information about all items and quantities for a location.</span></span> |
| <span data-ttu-id="c4383-135">ライセンス プレートの照会</span><span class="sxs-lookup"><span data-stu-id="c4383-135">License plate inquiry</span></span> | <span data-ttu-id="c4383-136">ライセンス プレート上の品目の数量、およびライセンス プレートの場所を表示します。</span><span class="sxs-lookup"><span data-stu-id="c4383-136">View the quantity of items on a license plate and the location of the license plate.</span></span> |
| <span data-ttu-id="c4383-137">製造オーダーの開始</span><span class="sxs-lookup"><span data-stu-id="c4383-137">Start production order</span></span> | <span data-ttu-id="c4383-138">製造オーダーを開始します。</span><span class="sxs-lookup"><span data-stu-id="c4383-138">Start a production order.</span></span> |
| <span data-ttu-id="c4383-139">生産仕損</span><span class="sxs-lookup"><span data-stu-id="c4383-139">Production scrap</span></span> | <span data-ttu-id="c4383-140">部品表 (BOM) の各明細行に対する生産の間に作成された仕損の数量を入力します。</span><span class="sxs-lookup"><span data-stu-id="c4383-140">Enter the quantity of scrap that was created during production for each bill of materials (BOM) line.</span></span> |
| <span data-ttu-id="c4383-141">最後の生産パレット</span><span class="sxs-lookup"><span data-stu-id="c4383-141">Production last pallet</span></span> | <span data-ttu-id="c4383-142">製造オーダーに対して品目の最後のパレットが生産されたことと、製造オーダーのステータスを **完了報告済** に更新する必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="c4383-142">Indicate that the last pallet of items has been produced for a production order, and that the status of the production order must be updated to **Reported as finished**.</span></span> <span data-ttu-id="c4383-143">生産中に消費されなかった原材料のステータスが **ピッキング** から **注文中** に戻されて、品目を在庫に戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="c4383-143">The status of the raw materials that were not consumed during production is change back from **Picked** to **On order**, and the items can be returned to inventory.</span></span> |
| <span data-ttu-id="c4383-144">品目の照会</span><span class="sxs-lookup"><span data-stu-id="c4383-144">Item inquiry</span></span> | <span data-ttu-id="c4383-145">品目をスキャンして、倉庫のどこにあるかを決定します。</span><span class="sxs-lookup"><span data-stu-id="c4383-145">Scan an item to determine where it is in the warehouse.</span></span> <span data-ttu-id="c4383-146">照会によって、スキャンされた品目のすべての場所と数量が返されます。</span><span class="sxs-lookup"><span data-stu-id="c4383-146">The inquiry returns all locations and quantities for the scanned item.</span></span> |
| <span data-ttu-id="c4383-147">ラベルの再印刷</span><span class="sxs-lookup"><span data-stu-id="c4383-147">Reprint label</span></span> | <span data-ttu-id="c4383-148">ライセンス プレート ラベルを印刷します。</span><span class="sxs-lookup"><span data-stu-id="c4383-148">Reprint a license plate label.</span></span> |
| <span data-ttu-id="c4383-149">ライセンス プレートの構築</span><span class="sxs-lookup"><span data-stu-id="c4383-149">License plate build</span></span> | <span data-ttu-id="c4383-150">同じ場所にある複数のライセンス プレートを結合して、親のライセンス プレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="c4383-150">Create a parent license plate by combining multiple license plates in the same location.</span></span> <span data-ttu-id="c4383-151">このオプションは、複数のライセンス プレートを同時に移動する場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="c4383-151">This option is useful if you move multiple license plates at the same time.</span></span> <span data-ttu-id="c4383-152">親のライセンス プレートの移動後、各ライセンス プレートから品目をピッキングする前に、ライセンス プレートの分割を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4383-152">After the parent license plate is moved, you must perform a license plate break before you can pick items from each license plate.</span></span> <p></p><span data-ttu-id="c4383-153">**ヒント:** 親のライセンス プレートを移動するには、移動の作業を作成するようにコンフィギュレーションされているモバイル デバイスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4383-153">**Tip:** To move a parent license plate, you must use a mobile device that is configured to create work for movements.</span></span> |
| <span data-ttu-id="c4383-154">ライセンス プレートの分割</span><span class="sxs-lookup"><span data-stu-id="c4383-154">License plate break</span></span> | <span data-ttu-id="c4383-155">構築に含まれたライセンス プレートから品目をピッキングできるように、ライセンス プレートの構築を分割します。</span><span class="sxs-lookup"><span data-stu-id="c4383-155">Break up a license plate build so that you can pick items from the license plates that were in the build.</span></span> |
| <span data-ttu-id="c4383-156">配送担当者のチェックイン</span><span class="sxs-lookup"><span data-stu-id="c4383-156">Driver check in</span></span> | <span data-ttu-id="c4383-157">[輸送管理] を使用している場合は、出荷積荷 ID、予定 ID、または出荷 ID をスキャンすることによって配送担当者が到着したことを登録します。</span><span class="sxs-lookup"><span data-stu-id="c4383-157">If you’re using Transportation management, register the arrival of a driver by scanning the outbound load ID, appointment ID, or shipment ID.</span></span> <span data-ttu-id="c4383-158">このオプションでは、積荷は予定に割り当てられ、積荷の状態は **積載済** である必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4383-158">For this option, a load must be assigned to the appointment, and the status of the load must be **Loaded**.</span></span> |
| <span data-ttu-id="c4383-159">配送担当者のチェックアウト</span><span class="sxs-lookup"><span data-stu-id="c4383-159">Driver check out</span></span> | <span data-ttu-id="c4383-160">配送担当者の予定が完了したことを登録します。</span><span class="sxs-lookup"><span data-stu-id="c4383-160">Register that a driver has completed his or her appointment.</span></span> |
| <span data-ttu-id="c4383-161">番号順序キャッシュをフラッシュします</span><span class="sxs-lookup"><span data-stu-id="c4383-161">Flush number sequence cache</span></span> | <span data-ttu-id="c4383-162">番号順序の番号を番号順序キャッシュから削除します。</span><span class="sxs-lookup"><span data-stu-id="c4383-162">Delete number sequence numbers from the number sequence cache.</span></span> <span data-ttu-id="c4383-163">この活動は、モバイル デバイスを使用したときのキャッシュ問題を解決するために、通常はシステム管理者によって実行されます。</span><span class="sxs-lookup"><span data-stu-id="c4383-163">This activity is typically performed by a system administrator to resolve caching issues when mobile devices are used.</span></span> |
| <span data-ttu-id="c4383-164">バッチ廃棄を変更します</span><span class="sxs-lookup"><span data-stu-id="c4383-164">Change batch disposition</span></span> | <span data-ttu-id="c4383-165">作業者が品目およびバッチのバッチ廃棄コードを指定できるようにします。</span><span class="sxs-lookup"><span data-stu-id="c4383-165">Allow a worker to specify a batch disposition code for an item and batch.</span></span> <span data-ttu-id="c4383-166">この選択によって、バッチに対して指定されている廃棄コードが更新されます。</span><span class="sxs-lookup"><span data-stu-id="c4383-166">This selection updates the disposition code that is specified for the batch.</span></span> |
| <span data-ttu-id="c4383-167">オープン作業一覧の表示</span><span class="sxs-lookup"><span data-stu-id="c4383-167">Display open work list</span></span> | <span data-ttu-id="c4383-168">特定のユーザーに割り当て可能な作業の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="c4383-168">Show a list of available work to a particular user.</span></span> <span data-ttu-id="c4383-169">その後ユーザーは、実行する作業を選択し、指示が出されます。</span><span class="sxs-lookup"><span data-stu-id="c4383-169">The user can then select work to perform and will be directed to it.</span></span> <span data-ttu-id="c4383-170">このリストは画面サイズが 7 インチ以上のタブレット デバイス上で表示することを想定しています。</span><span class="sxs-lookup"><span data-stu-id="c4383-170">This list is intended to be viewed on tablet devices that have a screen size of 7 inches or more.</span></span> <span data-ttu-id="c4383-171">このオプションを選択すると、**クエリの編集** と **フィールド リスト** メニュー項目が有効になります。</span><span class="sxs-lookup"><span data-stu-id="c4383-171">When you select this option, the **Edit query** and **Field list** menu items become available.</span></span> <span data-ttu-id="c4383-172">**クエリの編集** ページでは、一覧表示される作業の条件を設定できます。</span><span class="sxs-lookup"><span data-stu-id="c4383-172">The **Edit query** page lets you set up criteria for the work that appears in the list.</span></span> <span data-ttu-id="c4383-173">**フィールド リスト** ページでは、作業一覧に表示するフィールドを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="c4383-173">The **Field list** page lets you select what fields appear in the work list.</span></span> <span data-ttu-id="c4383-174">たとえば、表示されるフィールドの数を減らして、ユーザーが最適な作業品目を素早く選択できるようにしたい場合があります。</span><span class="sxs-lookup"><span data-stu-id="c4383-174">For example, you can reduce the number of fields that appear, so that the user can more quickly select the most appropriate work item.</span></span> <span data-ttu-id="c4383-175">**全般** クイック タブの **1 ページのレコード数** フィールドで、1 ページに表示される作業レコード数も選択できます。</span><span class="sxs-lookup"><span data-stu-id="c4383-175">On the **General** FastTab, in the **Records per page** field, you can also select how many work records are shown per page.</span></span> <span data-ttu-id="c4383-176">**トランザクション タイプによる作業のフィルターをユーザーに許可する** オプションがオンの場合、作業一覧に **作業のフィルター処理** コントロールが表示され、ユーザーはトランザクション タイプによるフィルターを適用することができるようになります。</span><span class="sxs-lookup"><span data-stu-id="c4383-176">If the **Allow users to filter work by transaction type** option is selected, the work list will include a **Filter work** control that the user can use to filter by transaction type.</span></span> <span data-ttu-id="c4383-177">作業一覧には、ユーザーがアクセス許可を持つ作業のみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c4383-177">In the work list, users will see only work that they have permission to access.</span></span> <span data-ttu-id="c4383-178">アクセスできるようにする必要がある特定の作業クラス タイプをサポートする、1 つ以上のユーザー指定のメニュー項目に対するアクセス許可をユーザーに付与済みであることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4383-178">You must make sure that users have permission for one or more user-directed menu items that support the specific work class types that they should be able to access.</span></span> <span data-ttu-id="c4383-179">ユーザーが一覧の作業の実行を試みるときににアクセス許可が検証されます。</span><span class="sxs-lookup"><span data-stu-id="c4383-179">Permissions are verified when a user tries to perform work from the list.</span></span>|
| <span data-ttu-id="c4383-180">ライセンス プレートから移動オーダーを作成します</span><span class="sxs-lookup"><span data-stu-id="c4383-180">Create transfer order from license plates</span></span> | <span data-ttu-id="c4383-181">倉庫作業者が、倉庫アプリから移動オーダーを直接作成およびプロセスできるように許可します。</span><span class="sxs-lookup"><span data-stu-id="c4383-181">Allows warehouse workers create and process transfer orders directly from the warehouse app.</span></span> <span data-ttu-id="c4383-182">倉庫作業者は、出荷先倉庫を選択することによって開始し、アプリを使用して 1 つ以上のライセンス プレートをスキャンすることができます。</span><span class="sxs-lookup"><span data-stu-id="c4383-182">The warehouse workers start by selecting the destination warehouse and can then scan one or more license plates using the app.</span></span> <span data-ttu-id="c4383-183">倉庫作業者が **注文の完了** を選択すると、バッチ ジョブによって、そのライセンス プレートに対して登録されている手持在庫に基づいて必要な移動オーダーおよび注文明細行が作成されます。</span><span class="sxs-lookup"><span data-stu-id="c4383-183">When the warehouse worker selects **Complete order**, a batch job will create the required transfer order and order lines based on the on-hand inventory registered for those license plates.</span></span> <span data-ttu-id="c4383-184">詳細については、[倉庫アプリからの移動オーダーの作成](create-transfer-order-from-warehouse-app.md)を参照してください</span><span class="sxs-lookup"><span data-stu-id="c4383-184">For more information, see [Create transfer orders from the warehouse app](create-transfer-order-from-warehouse-app.md)</span></span>


## <a name="configure-menu-items-to-create-work-for-another-worker-or-process"></a><span data-ttu-id="c4383-185">別の作業者またはプロセスの作業を作成するメニュー項目の構成</span><span class="sxs-lookup"><span data-stu-id="c4383-185">Configure menu items to create work for another worker or process</span></span>
<span data-ttu-id="c4383-186">最初のアクションをモバイル デバイス上で実行後に、別の作業者の作業を作成するメニュー項目を設定できます。</span><span class="sxs-lookup"><span data-stu-id="c4383-186">You can set up a menu item that creates work for another worker after an initial action is performed on the mobile device.</span></span> <span data-ttu-id="c4383-187">たとえば、1 人の作業者がモバイル デバイスを使用して品目を受け入れるとき、プット アウェイ作業は別の作業者に対して作成されます。</span><span class="sxs-lookup"><span data-stu-id="c4383-187">For example, when one worker uses a mobile device to receive an item, put-away work is created for another worker.</span></span> <span data-ttu-id="c4383-188">作業を作成するメニュー項目を設定するには、**モバイル デバイスのメニュー項目** ページの **モード** フィールドで **作業** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c4383-188">To set up a menu item that creates work, on the **Mobile device menu items** page, in the **Mode** field, select **Work**.</span></span> <span data-ttu-id="c4383-189">次の表では、**作業の作成プロセス** フィールドの選択肢が作業の注文タイプによって並んでいます。</span><span class="sxs-lookup"><span data-stu-id="c4383-189">In the following table, the options in the **Work creation process** field are arranged by work order type.</span></span>


<table>
<tbody>
<tr>
<th><span data-ttu-id="c4383-190">ワーク オーダー タイプ</span><span class="sxs-lookup"><span data-stu-id="c4383-190">Work order type</span></span></th>
<th><span data-ttu-id="c4383-191">オプション</span><span class="sxs-lookup"><span data-stu-id="c4383-191">Option</span></span></th>
<th><span data-ttu-id="c4383-192">説明</span><span class="sxs-lookup"><span data-stu-id="c4383-192">Description</span></span></th>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="c4383-193">発注書</span><span class="sxs-lookup"><span data-stu-id="c4383-193">Purchase order</span></span></td>
<td><span data-ttu-id="c4383-194">発注書明細行受取</span><span class="sxs-lookup"><span data-stu-id="c4383-194">Purchase order line receiving</span></span></td>
<td><span data-ttu-id="c4383-195">発注書番号と発注書明細行番号を使用して品目の数量の受け入れを登録し、他の作業者のためのプット アウェイ作業を作成します。</span><span class="sxs-lookup"><span data-stu-id="c4383-195">Register the receipt of a quantity of an item by using the purchase order number and purchase order line number, and create put-away work for another worker.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c4383-196">発注書明細行受取とプット アウェイ</span><span class="sxs-lookup"><span data-stu-id="c4383-196">Purchase order line receiving and put away</span></span></td>
<td><span data-ttu-id="c4383-197">発注書番号と発注書明細行番号を使用して品目の数量の受け入れを登録し、その品目をプット アウェイします。</span><span class="sxs-lookup"><span data-stu-id="c4383-197">Register the receipt of a quantity of an item by using the purchase order number and purchase order line number, and put the items away.</span></span> <span data-ttu-id="c4383-198">同じ作業者が両方のアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="c4383-198">The same worker performs both actions.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c4383-199">発注書品目受取</span><span class="sxs-lookup"><span data-stu-id="c4383-199">Purchase order item receiving</span></span></td>
<td><span data-ttu-id="c4383-200">発注書番号と品目番号の登録により発注書の品目の数量の受け入れを登録し、他の作業者のためのプット アウェイ作業を作成します。</span><span class="sxs-lookup"><span data-stu-id="c4383-200">Register the receipt of a quantity of an item for a purchase order by registering the purchase order number and item number, and create put-away work for another worker.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c4383-201">発注書品目受取とプット アウェイ</span><span class="sxs-lookup"><span data-stu-id="c4383-201">Purchase order item receiving and put away</span></span></td>
<td><span data-ttu-id="c4383-202">発注書番号と品目番号を登録して、発注書の品目の数量の受け入れを登録し、その品目をプット アウェイします。</span><span class="sxs-lookup"><span data-stu-id="c4383-202">Register the receipt of a quantity of an item for a purchase order by registering the purchase order number, and put the item away.</span></span> <span data-ttu-id="c4383-203">同じ作業者が両方のアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="c4383-203">The same worker performs both actions.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c4383-204">ライセンス プレート受取</span><span class="sxs-lookup"><span data-stu-id="c4383-204">License plate receiving</span></span></td>
<td><span data-ttu-id="c4383-205">ライセンス プレート ID を使用して、受信事前出荷明細通知 (ASN) を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="c4383-205">Receive an inbound advance ship notice (ASN) by using the license plate ID.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c4383-206">ライセンス プレートの受け取りおよびプット アウェイ</span><span class="sxs-lookup"><span data-stu-id="c4383-206">License plate receiving and put away</span></span></td>
<td><span data-ttu-id="c4383-207">ライセンス プレート ID を使用して、受信事前出荷明細通知 (ASN) の受け入れとプット アウェイを行います。</span><span class="sxs-lookup"><span data-stu-id="c4383-207">Receive and put away an inbound advance ship notice (ASN) by using the license plate ID.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c4383-208">積荷品目入庫</span><span class="sxs-lookup"><span data-stu-id="c4383-208">Load item receiving</span></span></td>
<td><span data-ttu-id="c4383-209">積荷 ID を使用して積荷の数量の受け入れを登録し、プット アウェイ作業を別の作業者に対して作成します。</span><span class="sxs-lookup"><span data-stu-id="c4383-209">Register the receipt of a quantity for a load by using the load ID, and create put-away work for another worker.</span></span> <span data-ttu-id="c4383-210">品目番号および製品分析コードは、発注書の明細行の受け入れに一致します。</span><span class="sxs-lookup"><span data-stu-id="c4383-210">The item number and product dimensions match the receipt to the purchase order lines.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c4383-211">積荷品目入庫とプット アウェイ</span><span class="sxs-lookup"><span data-stu-id="c4383-211">Load item receiving and put away</span></span></td>
<td><span data-ttu-id="c4383-212">積荷 ID を使用して積荷の数量の受け入れを登録し、その品目をプット アウェイします。</span><span class="sxs-lookup"><span data-stu-id="c4383-212">Register the receipt of a load by using the load ID, and put the items away.</span></span> <span data-ttu-id="c4383-213">品目番号および製品分析コードは、発注書の明細行の受け入れに一致します。</span><span class="sxs-lookup"><span data-stu-id="c4383-213">The item number and product dimensions match the receipt to the purchase order lines.</span></span> <span data-ttu-id="c4383-214">同じ作業者が両方のアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="c4383-214">The same worker performs both actions.</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="c4383-215">返品注文</span><span class="sxs-lookup"><span data-stu-id="c4383-215">Return order</span></span></td>
<td><span data-ttu-id="c4383-216">返品注文入庫</span><span class="sxs-lookup"><span data-stu-id="c4383-216">Return order receiving</span></span></td>
<td><span data-ttu-id="c4383-217">RMA 番号を登録して品目の数量の受け入れを登録し、プット アウェイ作業を別の作業者に対して作成します。</span><span class="sxs-lookup"><span data-stu-id="c4383-217">Register the receipt of a quantity of an item by registering the RMA number, and create put-away work for another worker.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c4383-218">返品注文入庫およびプット アウェイ</span><span class="sxs-lookup"><span data-stu-id="c4383-218">Return order receiving and put away</span></span></td>
<td><span data-ttu-id="c4383-219">RMA 番号を登録して品目の数量の受け入れを登録し、その品目をプット アウェイします。</span><span class="sxs-lookup"><span data-stu-id="c4383-219">Register the receipt of a quantity of an item by registering the RMA number, and put the items away.</span></span> <span data-ttu-id="c4383-220">同じ作業者が両方のアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="c4383-220">The same worker performs both actions.</span></span></td>
</tr>
<tr>
<td rowspan="6"><span data-ttu-id="c4383-221">移動オーダー</span><span class="sxs-lookup"><span data-stu-id="c4383-221">Transfer order</span></span></td>
<td><span data-ttu-id="c4383-222">移動オーダー品目入庫</span><span class="sxs-lookup"><span data-stu-id="c4383-222">Transfer order item receiving</span></span></td>
<td><span data-ttu-id="c4383-223">品目の数量の受け入れを登録し、プット アウェイ作業を別の作業者に対して作成します。</span><span class="sxs-lookup"><span data-stu-id="c4383-223">Register the receipt of a quantity of an item, and create put-away work for another worker.</span></span>

<span data-ttu-id="c4383-224"><strong>注意:</strong> 倉庫管理プロセスが有効になっていない倉庫から品目が出荷された場合にのみ、このオプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="c4383-224"><strong>Note:</strong> Use this option only if the items were shipped from a warehouse that isn't enabled for warehouse management processes.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c4383-225">移動オーダー品目入庫とプット アウェイ</span><span class="sxs-lookup"><span data-stu-id="c4383-225">Transfer order item receiving and put away</span></span></td>
<td><span data-ttu-id="c4383-226">品目の数量の受け入れを登録し、その品目をプット アウェイします。</span><span class="sxs-lookup"><span data-stu-id="c4383-226">Register the receipt of a quantity of an item, and put the items away.</span></span> <span data-ttu-id="c4383-227">同じ作業者が両方のアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="c4383-227">The same worker performs both actions.</span></span>

<span data-ttu-id="c4383-228"><strong>注意:</strong> 倉庫管理プロセスが有効になっていない倉庫から品目が出荷された場合にのみ、このオプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="c4383-228"><strong>Note:</strong> Use this option only if the items were shipped from a warehouse that isn't enabled for warehouse management processes.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c4383-229">移動オーダー明細行入庫</span><span class="sxs-lookup"><span data-stu-id="c4383-229">Transfer order line receiving</span></span></td>
<td><span data-ttu-id="c4383-230">品目の数量の受け入れを登録し、プット アウェイ作業を別の作業者に対して作成します。</span><span class="sxs-lookup"><span data-stu-id="c4383-230">Register the receipt of a quantity of an item, and create put-away work for another worker.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c4383-231">注文明細行の受取とプット アウェイの移動</span><span class="sxs-lookup"><span data-stu-id="c4383-231">Transfer order line receiving and put away</span></span></td>
<td><span data-ttu-id="c4383-232">品目の数量の受け入れを登録し、その品目をプット アウェイします。</span><span class="sxs-lookup"><span data-stu-id="c4383-232">Register the receipt of a quantity of an item, and put the items away.</span></span> <span data-ttu-id="c4383-233">同じ作業者が両方のアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="c4383-233">The same worker performs both actions.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c4383-234">ライセンス プレート受取</span><span class="sxs-lookup"><span data-stu-id="c4383-234">License plate receiving</span></span></td>
<td><span data-ttu-id="c4383-235">ライセンス プレート ID を使用して、受信事前出荷明細通知 (ASN) を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="c4383-235">Receive an inbound advance ship notice (ASN) by using the license plate ID.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c4383-236">ライセンス プレートの受け取りおよびプット アウェイ</span><span class="sxs-lookup"><span data-stu-id="c4383-236">License plate receiving and put away</span></span></td>
<td><span data-ttu-id="c4383-237">ライセンス プレート ID を使用して、受信事前出荷明細通知 (ASN) の受け入れとプット アウェイを行います。</span><span class="sxs-lookup"><span data-stu-id="c4383-237">Receive and put away an inbound advance ship notice (ASN) by using the license plate ID.</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="c4383-238">運用</span><span class="sxs-lookup"><span data-stu-id="c4383-238">Production</span></span></td>
<td><span data-ttu-id="c4383-239">完了レポート</span><span class="sxs-lookup"><span data-stu-id="c4383-239">Report as finished</span></span></td>
<td><span data-ttu-id="c4383-240">生産が完了した完成品目の数量を登録し、プット アウェイ作業を別の作業者に対して作成します。</span><span class="sxs-lookup"><span data-stu-id="c4383-240">Register a quantity of a finished item that has been finished for a production, and create put-away work for another worker.</span></span> <span data-ttu-id="c4383-241">数量は、生産に対して計画された数量の一部かまたは全部のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="c4383-241">The quantity can be some or all of the quantity that was planned for production.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c4383-242">完了レポートとプット アウェイ</span><span class="sxs-lookup"><span data-stu-id="c4383-242">Report as finished and put away</span></span></td>
<td><span data-ttu-id="c4383-243">生産が完了した完成品目の数量を登録し、その品目をプット アウェイします。</span><span class="sxs-lookup"><span data-stu-id="c4383-243">Register a quantity of a finished item that has been finished for a production, and put the items away.</span></span> <span data-ttu-id="c4383-244">数量は、生産に対して計画された数量の一部かまたは全部のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="c4383-244">The quantity can be some or all of the quantity that was planned for production.</span></span> <span data-ttu-id="c4383-245">同じ作業者が両方のアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="c4383-245">The same worker performs both actions.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c4383-246">かんばん</span><span class="sxs-lookup"><span data-stu-id="c4383-246">Kanban</span></span></td>
<td><span data-ttu-id="c4383-247">かんばんが完了したことを示し、プット アウェイ作業は別の作業者に対して作業します。</span><span class="sxs-lookup"><span data-stu-id="c4383-247">Indicate that a kanban is completed, and create put-away work for another worker.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c4383-248">かんばんのプット アウェイ</span><span class="sxs-lookup"><span data-stu-id="c4383-248">Kanban put away</span></span></td>
<td><span data-ttu-id="c4383-249">かんばんが完了したことを示し、その品目をプット アウェイします。</span><span class="sxs-lookup"><span data-stu-id="c4383-249">Indicate that a kanban is completed, and put away the items.</span></span> <span data-ttu-id="c4383-250">同じ作業者が両方のアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="c4383-250">The same worker performs both actions.</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="c4383-251">棚卸資産</span><span class="sxs-lookup"><span data-stu-id="c4383-251">Inventory</span></span></td>
<td><span data-ttu-id="c4383-252">移動</span><span class="sxs-lookup"><span data-stu-id="c4383-252">Movement</span></span></td>
<td><span data-ttu-id="c4383-253">品目が一つの場所から別の場所に移動されたことを登録します。</span><span class="sxs-lookup"><span data-stu-id="c4383-253">Register that items have been moved from one location to another.</span></span> <span data-ttu-id="c4383-254">作業者は、品目の移動元の場所と移動先の場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="c4383-254">The worker specifies the location that the items are moved from and where they are moved to.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c4383-255">検査</span><span class="sxs-lookup"><span data-stu-id="c4383-255">Quarantine</span></span></td>
<td><span data-ttu-id="c4383-256">破損または欠落している在庫品目を使用できないようにするために、ライセンス プレートまたは場所の手持在庫の状態を変更します。</span><span class="sxs-lookup"><span data-stu-id="c4383-256">Change the status of the on-hand inventory for a license plate or location to make damaged or missing inventory items unavailable.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c4383-257">テンプレートによる移動</span><span class="sxs-lookup"><span data-stu-id="c4383-257">Movement by template</span></span></td>
<td><span data-ttu-id="c4383-258">一つの場所から別の場所に、半自動の方法で品目を移動します。</span><span class="sxs-lookup"><span data-stu-id="c4383-258">Move items from one location to another in a semi-automated manner.</span></span> <span data-ttu-id="c4383-259">作業者が品目の移動元の場所を選択し、システムが場所ディレクティブを使用して品目の移動先の場所を決定します。</span><span class="sxs-lookup"><span data-stu-id="c4383-259">The worker selects the location to move items from, the system uses the location directive to determine where to move the items to.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c4383-260">倉庫間の移動</span><span class="sxs-lookup"><span data-stu-id="c4383-260">Warehouse transfer</span></span></td>
<td><span data-ttu-id="c4383-261">品目が一つの倉庫から別の倉庫に移動されたことを登録します。</span><span class="sxs-lookup"><span data-stu-id="c4383-261">Register that items have been transferred from one warehouse to another.</span></span> <span data-ttu-id="c4383-262">このオプションでは、作業者が両方の倉庫で作業を実行できる許可を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4383-262">This option requires that the worker be allowed to perform work in both warehouses.</span></span>

<span data-ttu-id="c4383-263"><strong>注意:</strong> このメニュー項目には、<strong>伝票の振出</strong>フィールドが<strong>転記</strong>に設定されている、既定の棚卸資産転送仕訳が必要です。</span><span class="sxs-lookup"><span data-stu-id="c4383-263"><strong>Note:</strong> This menu item requires a default inventory transfer journal where the <strong>Voucher draw</strong> field is set to <strong>Posting</strong>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c4383-264">ライセンス プレートの読み込み</span><span class="sxs-lookup"><span data-stu-id="c4383-264">License plate loading</span></span></td>
<td><span data-ttu-id="c4383-265">自分の倉庫を初めて設定するときに、このオプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="c4383-265">Use this option when you&#39;re setting up your warehouse for the first time.</span></span> <span data-ttu-id="c4383-266">倉庫内のすべての場所のライセンス プレートをすべてスキャンします。</span><span class="sxs-lookup"><span data-stu-id="c4383-266">Scan all the license plates in all locations in the warehouse.</span></span> <span data-ttu-id="c4383-267">これらの場所は、ライセンス プレートによって制御される必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4383-267">The locations must be license plate–controlled.</span></span> <span data-ttu-id="c4383-268"><strong>シリアル番号</strong>または<strong>バッチ番号</strong>が、在庫引当階層の<strong>場所</strong>の上部に表示された場合、このオプションは使用できません。</span><span class="sxs-lookup"><span data-stu-id="c4383-268">You can&#39;t use this option if <strong>Serial number</strong> or <strong>Batch number</strong> is listed above <strong>Location</strong> in the inventory reservation hierarchy.</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="c4383-269">循環棚卸</span><span class="sxs-lookup"><span data-stu-id="c4383-269">Cycle count</span></span></td>
<td><span data-ttu-id="c4383-270">調整内</span><span class="sxs-lookup"><span data-stu-id="c4383-270">Adjustment in</span></span></td>
<td><span data-ttu-id="c4383-271">在庫品目の数量を増します。</span><span class="sxs-lookup"><span data-stu-id="c4383-271">Increase the quantity of items in inventory.</span></span> <span data-ttu-id="c4383-272">場所、ライセンス プレート、品目、数量、測定単位、および状態を指定します。</span><span class="sxs-lookup"><span data-stu-id="c4383-272">Specify the location, license plate, item, quantity, unit of measure, and status.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c4383-273">調整外</span><span class="sxs-lookup"><span data-stu-id="c4383-273">Adjustment out</span></span></td>
<td><span data-ttu-id="c4383-274">在庫品目の数量を減らします。</span><span class="sxs-lookup"><span data-stu-id="c4383-274">Reduce the quantity of items in inventory.</span></span> <span data-ttu-id="c4383-275">在庫の場所、ライセンス プレート、品目、数量、測定単位、および状態を指定します。</span><span class="sxs-lookup"><span data-stu-id="c4383-275">Specify the location, license plate, item, quantity, unit of measure, and status of the inventory.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c4383-276">スポット循環棚卸</span><span class="sxs-lookup"><span data-stu-id="c4383-276">Spot cycle counting</span></span></td>
<td><span data-ttu-id="c4383-277">任意の場所での計数を開始します。</span><span class="sxs-lookup"><span data-stu-id="c4383-277">Start a count for a location.</span></span> <span data-ttu-id="c4383-278">作業者はその場所のすべての品目を計数する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4383-278">The worker must count all items in the location.</span></span> <span data-ttu-id="c4383-279">計数の結果が予定数量よりより少ない場合は、欠落している数量は損失と見なされます。</span><span class="sxs-lookup"><span data-stu-id="c4383-279">When the result of a count is less than the expected quantity, the missing quantity is considered a loss.</span></span></td>
</tr>
</tbody>
</table>

## <a name="configure-menu-items-to-process-existing-work"></a><span data-ttu-id="c4383-280">既存の作業を処理するメニュー項目の構成</span><span class="sxs-lookup"><span data-stu-id="c4383-280">Configure menu items to process existing work</span></span>
<span data-ttu-id="c4383-281">倉庫の作業を作成するメニュー項目の設定に加えて、既に作成されている作業を処理するメニュー項目を設定できます。</span><span class="sxs-lookup"><span data-stu-id="c4383-281">In addition to setting up menu items to create warehouse work, you can set up menu items to process work that has already been created.</span></span> <span data-ttu-id="c4383-282">**モード** フィールドを **作業** に設定し、**既存の作業を使用** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c4383-282">Set the **Mode** field to **Work**, and select the **Use existing work** option.</span></span> <span data-ttu-id="c4383-283">その後、**概要** タブで追加オプションが使用できるようになります。**作業クラス** クイック タブで 1 つ以上の作業クラスを割り当てることにより、メニュー項目へのアクセスを制御できます。</span><span class="sxs-lookup"><span data-stu-id="c4383-283">Some additional options then become available on the **General** tab. You can control access to the menu item by assigning one or more work classes on the **Work class** FastTab.</span></span> <span data-ttu-id="c4383-284">作業クラスは、メニュー項目により処理することができる作業を定義します。</span><span class="sxs-lookup"><span data-stu-id="c4383-284">The work classes define the work that the menu item can process.</span></span> <span data-ttu-id="c4383-285">また、作業クラスは、特定のユーザー ロールへのアクセス許可、またはさまざまな工程の異なる処理へのアクセスを許可を付与するのに使用できます。</span><span class="sxs-lookup"><span data-stu-id="c4383-285">The work class can also be used to grant access to specific user roles or to separate processing for different types of operations.</span></span> <span data-ttu-id="c4383-286">次の表に、使用できるオプションを示します。</span><span class="sxs-lookup"><span data-stu-id="c4383-286">The following table describes the options that are available.</span></span> <span data-ttu-id="c4383-287">オプションは、**モバイル デバイスのメニュー項目** ページの **指示者** フィールドで選択可能です。</span><span class="sxs-lookup"><span data-stu-id="c4383-287">The option can be chosen under the **Directed by** field in the **Mobile device menu items** page.</span></span> 

<table>




<thead>
<tr class="header">
<th><span data-ttu-id="c4383-288">オプション</span><span class="sxs-lookup"><span data-stu-id="c4383-288">Option</span></span></th>
<th><span data-ttu-id="c4383-289">説明</span><span class="sxs-lookup"><span data-stu-id="c4383-289">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4383-290">なし</span><span class="sxs-lookup"><span data-stu-id="c4383-290">None</span></span></td>
<td><span data-ttu-id="c4383-291">この既定値は作業を処理しません。</span><span class="sxs-lookup"><span data-stu-id="c4383-291">This default value doesn&#39;t process work.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4383-292">システム主導</span><span class="sxs-lookup"><span data-stu-id="c4383-292">System directed</span></span></td>
<td><span data-ttu-id="c4383-293">Supply Chain Management では、作業者に割り当てられた作業のタイプ、および作業者が作業を実行する注文を管理します。</span><span class="sxs-lookup"><span data-stu-id="c4383-293">Supply Chain Management controls the type of work that is assigned to a worker and the order that the worker performs the work in.</span></span> <span data-ttu-id="c4383-294">このオプションを選択すると、アクション ウィンドウで <strong>システム主導の作業</strong> を選択し、<strong>システム主導の並べ替え順</strong> ページで作業の並べ替えの基準を設定できるようになります。</span><span class="sxs-lookup"><span data-stu-id="c4383-294">When you select this option, you can sekect <strong>System-directed work</strong> on the Action Pane to open the <strong>System-directed sorting order</strong> page, where you can set up sorting criteria for the work.</span></span> <span data-ttu-id="c4383-295">並べ替え基準は、作業者が作業を実行する順序を制御します。</span><span class="sxs-lookup"><span data-stu-id="c4383-295">The sorting criteria control the order that the worker performs the work in.</span></span> <span data-ttu-id="c4383-296">必要な数だけ基準を追加できます。</span><span class="sxs-lookup"><span data-stu-id="c4383-296">You can add as many criteria as you require.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4383-297">ユーザー主導</span><span class="sxs-lookup"><span data-stu-id="c4383-297">User directed</span></span></td>
<td><span data-ttu-id="c4383-298">作業者は、実行する作業と作業を実行する順序を選択します。</span><span class="sxs-lookup"><span data-stu-id="c4383-298">The worker selects the work to perform and the order to perform it in.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4383-299">ユーザーのグループ化</span><span class="sxs-lookup"><span data-stu-id="c4383-299">User grouping</span></span></td>
<td><span data-ttu-id="c4383-300">作業者は作業を手動でグループ化します。</span><span class="sxs-lookup"><span data-stu-id="c4383-300">The worker manually groups work.</span></span> <span data-ttu-id="c4383-301">このオプションは、たとえば、作業者が 1 つの場所で複数の品目を同時にピッキングするときに役に立ちます。</span><span class="sxs-lookup"><span data-stu-id="c4383-301">This option is useful when, for example, a worker can pick multiple items at the same time in a location.</span></span> <span data-ttu-id="c4383-302">作業者が必要な品目のすべてのピッキングが終了した後、その品目をプット アウェイすることができます。</span><span class="sxs-lookup"><span data-stu-id="c4383-302">After the worker has finished picking all the required items, he or she can put the items away.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4383-303">システム グループ化</span><span class="sxs-lookup"><span data-stu-id="c4383-303">System grouping</span></span></td>
<td><span data-ttu-id="c4383-304">Supply Chain Management グループは指定したフィールドに基づいた作業者のために働きます。</span><span class="sxs-lookup"><span data-stu-id="c4383-304">Supply Chain Management groups work for the worker, based on a specified field.</span></span> <span data-ttu-id="c4383-305">たとえば、作業者が出荷 ID、積荷 ID、または各作業単位をリンクできる値をスキャンするときに、ピッキング作業がグループ化されます。</span><span class="sxs-lookup"><span data-stu-id="c4383-305">For example, picking work is grouped when a worker scans a shipment ID, load ID, or any value that can link each work unit.</span></span> <span data-ttu-id="c4383-306">このオプションを選択する場合、次のフィールドが要求されます。</span><span class="sxs-lookup"><span data-stu-id="c4383-306">If you select this option, the following fields are required:</span></span>
<ul>
<li><span data-ttu-id="c4383-307"><strong>システム グループ化フィールド</strong> – 作業者が作業をグループ化するためにスキャンするフィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="c4383-307"><strong>System grouping field</strong> – Select the field that the worker scans to group the work.</span></span></li>
<li><span data-ttu-id="c4383-308"><strong>システム グループ化ラベル</strong> – 作業をグループ化するためにスキャンする内容を作業者に指示するテキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="c4383-308"><strong>System grouping label</strong> – Enter text to instruct the worker what to scan to group the work.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4383-309">検証済ユーザー主導</span><span class="sxs-lookup"><span data-stu-id="c4383-309">Validated user directed</span></span></td>
<td><span data-ttu-id="c4383-310">作業者は、作業が積荷または出荷などのより大きいエンティティに関連付けられるときに実行する作業を選択します。</span><span class="sxs-lookup"><span data-stu-id="c4383-310">The worker selects the work to perform when work is associated with a larger entity, such as a load or shipment.</span></span> <span data-ttu-id="c4383-311">作業者は、品目をピッキングする順序を決めます。</span><span class="sxs-lookup"><span data-stu-id="c4383-311">The worker determines the order that the items are picked in.</span></span> <span data-ttu-id="c4383-312">このオプションを選択する場合、次のフィールドが要求されます。</span><span class="sxs-lookup"><span data-stu-id="c4383-312">If you select this option, the following fields are required:</span></span>
<ul>
<li><span data-ttu-id="c4383-313"><strong>検証済ユーザー主導フィールド</strong> – 作業者が作業をグループ化するためにスキャンするフィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="c4383-313"><strong>Validated user directed field</strong> – Select the field that the worker scans to group the work.</span></span></li>
<li><span data-ttu-id="c4383-314"><strong>検証済ユーザー主導ラベル</strong> – システムによって作業をグループ化する時にスキャンする項目を作業者に指示するテキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="c4383-314"><strong>Validated user directed label</strong> – Enter text that instructs the worker what to scan when picking work is grouped by the system.</span></span></li>
</ul>
<span data-ttu-id="c4383-315">このオプションは、たとえば、複数のパレットが 1 つの積荷に対して置かれているときに役に立ちます。</span><span class="sxs-lookup"><span data-stu-id="c4383-315">This option is useful when, for example, multiple pallets are staged for a load.</span></span> <span data-ttu-id="c4383-316"><strong>検証済ユーザー主導</strong>フィールドの <strong>LoadId</strong> を選択すると、作業者は積荷に関連付けられているパレットをピッキングできます。</span><span class="sxs-lookup"><span data-stu-id="c4383-316">If you select <strong>LoadId</strong> in the <strong>Validated User Directed</strong> field, the worker can pick any pallet that is associated with the load.</span></span> <span data-ttu-id="c4383-317">作業者が積荷に関連付けられていない品目をスキャンすると、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c4383-317">The worker receives an error message if he or she scans an item that isn&#39;t associated with the load.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4383-318">クラスター ピッキング</span><span class="sxs-lookup"><span data-stu-id="c4383-318">Cluster picking</span></span></td>
<td><span data-ttu-id="c4383-319">作業者が作業をクラスタにグループ化します。</span><span class="sxs-lookup"><span data-stu-id="c4383-319">The worker groups work into clusters.</span></span> <span data-ttu-id="c4383-320">クラスタによって、作業者は、複数の作業オーダーに対して 1 つの場所から品目を同時にピッキングできます。</span><span class="sxs-lookup"><span data-stu-id="c4383-320">Clusters lets workers pick items from a single location for multiple work orders at the same time.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4383-321">循環棚卸のグループ化</span><span class="sxs-lookup"><span data-stu-id="c4383-321">Cycle count grouping</span></span></td>
<td><span data-ttu-id="c4383-322">作業者がゾーン、作業プール、または場所を選択すると、その選択に基づいて Supply Chain Management が作業を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="c4383-322">The worker selects a zone, work pool, or location, and Supply Chain Management assigns work, based on the selection.</span></span> <span data-ttu-id="c4383-323">このオプションを選択すると、アクション ウィンドウの <strong>循環棚卸</strong> をクリックすることで、表示する追加情報を指定でき、また、計数に不一致があった場合に作業者が計数を繰り返す必要のある回数を指定できます。</span><span class="sxs-lookup"><span data-stu-id="c4383-323">If you select this option, you can click <strong>Cycle counting</strong> on the Action Pane to specify additional information to display, and you can also specify the number of times that the worker must repeat the count if a difference is found.</span></span></td>
</tr>
 <tr class="odd">
<td><span data-ttu-id="c4383-324">輸送積荷</span><span class="sxs-lookup"><span data-stu-id="c4383-324">Transport loading</span></span></td>
<td><span data-ttu-id="c4383-325">この機能により、複数の倉庫作業者が同じまたは異なる積荷から在庫を同じトラックに積載し、積荷は完全または部分的に出荷されます。</span><span class="sxs-lookup"><span data-stu-id="c4383-325">This feature allows several warehouse workers to load inventory from the same or different loads onto the same truck, with loads that are fully or partially shipped.</span></span></td>
</tr>
</tbody>
</table>

## <a name="additional-menu-item-options"></a><span data-ttu-id="c4383-326">追加メニュー項目のオプション</span><span class="sxs-lookup"><span data-stu-id="c4383-326">Additional menu item options</span></span>
<span data-ttu-id="c4383-327">追加メニュー項目のオプションは、**モバイル デバイスのメニュー項目** ページで使用できます。</span><span class="sxs-lookup"><span data-stu-id="c4383-327">Additional menu items options are available on the **Mobile device menu items** page.</span></span> <span data-ttu-id="c4383-328">オプションは、メニュー項目を構成しようとしている工程により異なります。</span><span class="sxs-lookup"><span data-stu-id="c4383-328">The options vary, depending on the process that you’re configuring the menu item for.</span></span> 

<span data-ttu-id="c4383-329">次の表にこれらのオプションを示します。</span><span class="sxs-lookup"><span data-stu-id="c4383-329">The following table describes these options.</span></span>

<table>




<thead>
<tr class="header">
<th><span data-ttu-id="c4383-330">フィールド</span><span class="sxs-lookup"><span data-stu-id="c4383-330">Field</span></span></th>
<th><span data-ttu-id="c4383-331">説明</span><span class="sxs-lookup"><span data-stu-id="c4383-331">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4383-332">作業の分割を許可</span><span class="sxs-lookup"><span data-stu-id="c4383-332">Allow splitting of work</span></span></td>
<td><span data-ttu-id="c4383-333">ユーザーが複数のターゲット ライセンス プレートにワーク オーダーの品目を入力できるようにするには、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c4383-333">Select this option to let users put items for a work order into more than one target license plate.</span></span> <span data-ttu-id="c4383-334">このオプションは、たとえば、ターゲットのライセンス プレートが満杯になり、作業者が残りの品目を別のライセンス プレートに追加する必要がある場合などに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="c4383-334">This option is useful when, for example, a target license plate is full, and the worker must add the remaining items to another license plate.</span></span> <span data-ttu-id="c4383-335">作業者は、<strong>フル</strong> を選択することで、ライセンス プレートが満杯になっていることを示し、それへのピッキング作業の受け入れを停止することができます。</span><span class="sxs-lookup"><span data-stu-id="c4383-335">The worker can select <strong>Full</strong> to indicate that the license plate is full and stop receiving picking work for it.</span></span> <span data-ttu-id="c4383-336">次にピッキング済品目のプット場所が表示され、既に完了しているピッキング作業が新しいワーク オーダーに移動されます。</span><span class="sxs-lookup"><span data-stu-id="c4383-336">The put location for the picked items is then displayed, and the picking work that has already been completed is moved to a new work order.</span></span> <span data-ttu-id="c4383-337">ターゲットのライセンス プレートの残りのピッキング作業は、元のワーク オーダーを維持します。</span><span class="sxs-lookup"><span data-stu-id="c4383-337">The remaining picking work for the target license plate stays on the original work order.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4383-338">固定</span><span class="sxs-lookup"><span data-stu-id="c4383-338">Anchoring</span></span></td>
<td><span data-ttu-id="c4383-339">提示されているステージングまたは積載場所を上書きする場所を作業者が指定できるようにするには、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c4383-339">Select this option to let workers specify a location that overrides the suggested staging or loading location.</span></span> <span data-ttu-id="c4383-340">残りのプット アウェイ作業のすべてが、新しい場所に振り分けられます。</span><span class="sxs-lookup"><span data-stu-id="c4383-340">All the remaining put-away work is directed to the new location.</span></span> <span data-ttu-id="c4383-341">このオプションは、たとえば、作業者がオーダー 1 の品目をドック 1 のステージング場所に配置しようとしたとき、前の積荷がその場所から取り除かれていないときに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="c4383-341">This option is useful when, for example, a worker who must put items for order 1 in a staging location by Dock 1 can’t, because a previous load hasn’t cleared the location.</span></span> <span data-ttu-id="c4383-342">作業者は、ドック 1 のステージングの場所が使用可能になるまで待つ代わりに、ドック 2 をステージングの場所に使用することを決定します。</span><span class="sxs-lookup"><span data-stu-id="c4383-342">Instead of waiting for the Dock 1 staging location to become available, the worker can decide to use the staging location for Dock 2.</span></span> <span data-ttu-id="c4383-343">この場合、作業者は、提示されているステージの場所を上書きします。</span><span class="sxs-lookup"><span data-stu-id="c4383-343">In this case, the worker overrides the suggested staging location.</span></span> <span data-ttu-id="c4383-344">ワーク オーダーの残りのすべての品目の収納場所が、ドック 2 のステージングの場所に更新されます。</span><span class="sxs-lookup"><span data-stu-id="c4383-344">The put location for all remaining items for the work order is then updated to the Dock 2 staging location.</span></span> <span data-ttu-id="c4383-345">このオプションを選択した場合、<strong>固定担当者</strong>フィールドを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4383-345">If you select this option, you must set the <strong>Anchor by</strong> field.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4383-346">固定担当者</span><span class="sxs-lookup"><span data-stu-id="c4383-346">Anchor by</span></span></td>
<td><span data-ttu-id="c4383-347">アンカーを使用する場合は、アンカーが出荷別か積荷別かを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4383-347">If you&#39;re using anchoring, you must specify whether to anchor by shipment or by load.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4383-348">監査テンプレート ID</span><span class="sxs-lookup"><span data-stu-id="c4383-348">Audit template ID</span></span></td>
<td><span data-ttu-id="c4383-349">別の工程を実行できるように、このメニュー項目の作業プロセスを中断する作業監査テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="c4383-349">Select the work audit template that will interrupt the work process for this menu item so that another operation can be performed.</span></span> <span data-ttu-id="c4383-350">たとえば、このメニュー項目が入荷作業用の場合、監査テンプレートは、作業者が配送用コンテナ内の温度を確認するように要求する場合があります。</span><span class="sxs-lookup"><span data-stu-id="c4383-350">For example, if this menu item is for inbound work, the audit template might require that the worker check the temperature in the delivery container.</span></span> <span data-ttu-id="c4383-351">プロセスが中断されるポイントは、監査のテンプレートで指定します。</span><span class="sxs-lookup"><span data-stu-id="c4383-351">The point at which the process is interrupted is specified on the audit template.</span></span> <span data-ttu-id="c4383-352">このポイントは、例えば、作業の開始または完了、またはステータス変更の時点になります。</span><span class="sxs-lookup"><span data-stu-id="c4383-352">This point can be, for example, when work is started or completed, or when its status changes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4383-353">クラスター プロファイル ID</span><span class="sxs-lookup"><span data-stu-id="c4383-353">Cluster profile ID</span></span></td>
<td><span data-ttu-id="c4383-354">クラスタのピッキングに使用するクラスタ プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="c4383-354">Select the cluster profile to use for cluster picking.</span></span> <span data-ttu-id="c4383-355">クラスタ プロファイルには、クラスタを自動作成するかどうか、クラスタに割り当てることができる職位の名前と作業単位数、クラスタをいつ個々の単位に分割するか、検証が必要かどうかなどの設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c4383-355">The cluster profile includes settings such as whether to create clusters automatically, the names of positions and the number of work units that they can be assigned, when to break clusters into individual units, and whether verification is required.</span></span> <span data-ttu-id="c4383-356">このフィールドは、<strong>指示者</strong>フィールドで<strong>クラスター ピッキング</strong>が選択されている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="c4383-356">This field is available only if <strong>Cluster picking</strong> is selected in the <strong>Directed by</strong> field.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4383-357">合計品目数量を最初にカウント</span><span class="sxs-lookup"><span data-stu-id="c4383-357">Count total item quantity first</span></span></td>
<td><span data-ttu-id="c4383-358">カウント時に最初に合計数量をカウントするように作業者に要求するには、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c4383-358">Select this option to require that a worker count the total quantity first during a count.</span></span> <span data-ttu-id="c4383-359">食い違いが見つかった場合は、作業者は、ライセンス プレート番号、バッチ番号、シリアル番号などの追加情報を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4383-359">If a difference is found, the worker must provide additional information, such as the license plate number, batch number, and serial numbers.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4383-360">移動の作成</span><span class="sxs-lookup"><span data-stu-id="c4383-360">Create movement</span></span></td>
<td><span data-ttu-id="c4383-361">作業者に作業をすぐ実行するように要求しないで、作業者が移動の作業を作成できるようにする場合は、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c4383-361">Select this option to let a worker create work for a movement, but without requiring that the worker perform the work immediately.</span></span> <span data-ttu-id="c4383-362">このオプションは、たとえば、品質検査が完了し、検査官が品目を品質検査領域から移動することを望む場合に役に立ちます。</span><span class="sxs-lookup"><span data-stu-id="c4383-362">This option is useful if, for example, a quality inspection has been completed, and the inspector wants the item to be moved from the quality inspection area.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4383-363">ディレクティブ コード</span><span class="sxs-lookup"><span data-stu-id="c4383-363">Directive code</span></span></td>
<td><span data-ttu-id="c4383-364">特定の場所ディレクティブを使用するには、場所ディレクティブに関連付けられているディレクティブ コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="c4383-364">To use a specific location directive, select the directive code that is associated the location directive.</span></span> <span data-ttu-id="c4383-365">このフィールドは、作業を作成し、作業作成プロセスが<strong>テンプレートによる移動</strong>の場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="c4383-365">This field is available when you create work and the work creation process is <strong>Movement by template</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4383-366">循環棚卸のしきい値を無効化</span><span class="sxs-lookup"><span data-stu-id="c4383-366">Disable cycle count thresholds</span></span></td>
<td><span data-ttu-id="c4383-367">サイクル カウントのしきい値を無効にする場合は、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c4383-367">Select this option to ignore the cycle count thresholds.</span></span> <span data-ttu-id="c4383-368">このオプションを選択すると、しきい値を超えたときにサイクル カウント作業は作成されません。</span><span class="sxs-lookup"><span data-stu-id="c4383-368">If you select this option, cycle count work isn&#39;t created when threshold values are exceeded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4383-369">バッチ状態コードを表示します</span><span class="sxs-lookup"><span data-stu-id="c4383-369">Display batch disposition code</span></span></td>
<td><span data-ttu-id="c4383-370">このオプションを選択すると、バッチ廃棄コードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c4383-370">Select this option to display batch disposition codes.</span></span> <span data-ttu-id="c4383-371">たとえば、返品されたバッチを受け入れるときに、バッチ廃棄コードを表示できます。</span><span class="sxs-lookup"><span data-stu-id="c4383-371">For example, you can display batch disposition codes when you receive a returned batch.</span></span> <span data-ttu-id="c4383-372">作業者は、これによって、バッチの状態や品質を評価して、適切なコードを選択できます。</span><span class="sxs-lookup"><span data-stu-id="c4383-372">Workers can then evaluate the status or quality of a batch, and select the appropriate code.</span></span> <span data-ttu-id="c4383-373">バッチ廃棄コードのルールによって、バッチを他の倉庫プロセスで使用できるようにするかどうかが決まります。</span><span class="sxs-lookup"><span data-stu-id="c4383-373">The rules on the batch disposition code determine whether the batch will be available to other warehouse processes.</span></span> <span data-ttu-id="c4383-374">このオプションを選択しない場合は、次のバッチ廃棄コードのうち 1 つが使用されます:</span><span class="sxs-lookup"><span data-stu-id="c4383-374">If you don&#39;t select this option, one of the following batch disposition codes is used:</span></span>
<ul>
<li><span data-ttu-id="c4383-375">新しいバッチ番号を受け取った場合は、品目モデル グループで指定されている既定のバッチ廃棄コード。</span><span class="sxs-lookup"><span data-stu-id="c4383-375">If you receive a new batch number, the default batch disposition code that is specified on the item model group.</span></span></li>
<li><span data-ttu-id="c4383-376">バッチに割り当て済みのバッチ廃棄コード。</span><span class="sxs-lookup"><span data-stu-id="c4383-376">The batch disposition code that is already assigned to the batch.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4383-377">破棄コードの表示</span><span class="sxs-lookup"><span data-stu-id="c4383-377">Display disposition code</span></span></td>
<td><span data-ttu-id="c4383-378">このオプションを選択すると、廃棄コードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c4383-378">Select this option to display disposition codes.</span></span> <span data-ttu-id="c4383-379">たとえば、返品された品目を受け入れるときに、廃棄コードを表示できます。</span><span class="sxs-lookup"><span data-stu-id="c4383-379">For example, you can display disposition codes when you receive return items.</span></span> <span data-ttu-id="c4383-380">作業者は、これによって、品目の状態や品質を評価して、適切なコードを選択できます。</span><span class="sxs-lookup"><span data-stu-id="c4383-380">Workers can then evaluate the status or quality of the items, and select the appropriate code.</span></span> <span data-ttu-id="c4383-381">廃棄コードのルールによって、品目を他の倉庫プロセスで使用できるようにするかどうかが決まります。</span><span class="sxs-lookup"><span data-stu-id="c4383-381">The rules on the disposition code determine whether the items will be available to other warehouse processes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4383-382">在庫状態の表示</span><span class="sxs-lookup"><span data-stu-id="c4383-382">Display inventory status</span></span></td>
<td><span data-ttu-id="c4383-383">このオプションを選択すると、在庫の品目の状態が表示されます。</span><span class="sxs-lookup"><span data-stu-id="c4383-383">Select this option to display the status of items in inventory.</span></span> <span data-ttu-id="c4383-384">このオプションは、循環棚卸を除く、既存の作業を使用するすべてのメニュー項目で使用できます。</span><span class="sxs-lookup"><span data-stu-id="c4383-384">This option is available for all menu items that use existing work, except cycle counting.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4383-385">ピッキング画面の集計を表示します</span><span class="sxs-lookup"><span data-stu-id="c4383-385">Display summary of pick screen</span></span></td>
<td><span data-ttu-id="c4383-386">選択した作業オーダーのピッキング作業の集計を表示するには、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c4383-386">Select this option to display a summary of picking work for the selected work order.</span></span> <span data-ttu-id="c4383-387">この集計は、作業オーダーの最初の作業の明細行が処理されるまで表示されます。</span><span class="sxs-lookup"><span data-stu-id="c4383-387">The summary is displayed until the first work line is processed for the work order.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4383-388">ライセンス プレートの生成</span><span class="sxs-lookup"><span data-stu-id="c4383-388">Generate license plate</span></span></td>
<td><span data-ttu-id="c4383-389">番号順序の選択に基づいて固有のライセンス プレート番号を生成するには、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c4383-389">Select this option to generate a unique license plate number, based on the number sequence selection.</span></span> <span data-ttu-id="c4383-390">たとえば、発注書に対して受け入れる品目のライセンス プレート番号を生成できます。</span><span class="sxs-lookup"><span data-stu-id="c4383-390">For example, you can generate a license plate number for items that are received for purchase orders.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4383-391">グループ プット アウェイ</span><span class="sxs-lookup"><span data-stu-id="c4383-391">Group put away</span></span></td>
<td><span data-ttu-id="c4383-392">プット アウェイ作業をグループ化するには、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c4383-392">Select this option to group the put-away work.</span></span> <span data-ttu-id="c4383-393">このオプションは、作業が作業者または Supply Chain Management によってグループ化された場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="c4383-393">This option is available when the work was grouped either by the worker or by Supply Chain Management.</span></span> <span data-ttu-id="c4383-394">作業者がグループ内のすべてのピッキング作業を終了すると、プット アウェイ作業がその同じグループに対して作成されます。</span><span class="sxs-lookup"><span data-stu-id="c4383-394">When the worker has finished all the picking work in the group, put-away work is created for the same group.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4383-395">在庫調整タイプ</span><span class="sxs-lookup"><span data-stu-id="c4383-395">Inventory adjustment types</span></span></td>
<td><span data-ttu-id="c4383-396">在庫調整の転記に使用される在庫棚卸仕訳帳と、引当を削除するかどうかを決定する在庫調整タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="c4383-396">Select the inventory adjustment type that determines the inventory counting journal that is used to post the adjustment, and whether to remove reservations.</span></span> <span data-ttu-id="c4383-397">このフィールドは、<strong>調整内</strong>または<strong>調整外</strong>の作業作成プロセスに対してのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="c4383-397">This field is available only for the <strong>Adjustment in</strong> or <strong>Adjustment out</strong> work creation process.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4383-398">バッチ番号を上書きします</span><span class="sxs-lookup"><span data-stu-id="c4383-398">Override batch number</span></span></td>
<td><span data-ttu-id="c4383-399">製造オーダーの完了の数量を報告する作業者が、製造オーダーに割り当てられたバッチ番号とは異なるバッチ番号を入力できるようにする場合は、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c4383-399">Select this option to let workers who are reporting a quantity as finished for a production order enter a batch number that differs from the batch number that is assigned to the production order.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4383-400">ターゲット ライセンス プレートを上書きします</span><span class="sxs-lookup"><span data-stu-id="c4383-400">Override target license plate</span></span></td>
<td><span data-ttu-id="c4383-401">作業者が、提示されたターゲット ライセンス プレートとは異なるターゲット ライセンス プレート番号を指定できるようにするには、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c4383-401">Select this option to let workers specify a target license plate number that differs from the suggested target license plate.</span></span> <span data-ttu-id="c4383-402">作業オーダーの最初のピッキングがライセンス プレート上の品目の全数量に対してである場合は、このオプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="c4383-402">Use this option when the first pick for a work order is for the entire quantity of an item on a license plate.</span></span> <span data-ttu-id="c4383-403">たとえば、これはパレットを再利用する場合に役に立ちます。</span><span class="sxs-lookup"><span data-stu-id="c4383-403">This option is useful when, for example, a pallet is reused.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4383-404">ピッキングと梱包</span><span class="sxs-lookup"><span data-stu-id="c4383-404">Pick and pack</span></span></td>
<td><span data-ttu-id="c4383-405">作業者が、販売注文または積荷の作業を単一の作業単位に一体化できるようにする場合は、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c4383-405">Select this option to let workers combine work for a sales order or load into a single work unit.</span></span> <span data-ttu-id="c4383-406">作業者は、販売注文または積荷に対する作業のみを実行できます。</span><span class="sxs-lookup"><span data-stu-id="c4383-406">A worker can perform work only for the sales order or load.</span></span> <span data-ttu-id="c4383-407">このオプションは、たとえば、積荷、出荷、および作業が販売注文に対して作成された後で、販売注文の数量を増加する必要がある場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="c4383-407">This option is useful when, for example, you must increase a quantity for a sales order after the load, shipment, and work have been created for the sales order.</span></span> <span data-ttu-id="c4383-408">このオプションは、メニュー項目で既存の作業が使用され、その作業がユーザーまたはシステムによって指示された場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="c4383-408">This option is available when the menu item uses existing work, and the work is directed by the user or system.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4383-409">最も古いバッチのピック</span><span class="sxs-lookup"><span data-stu-id="c4383-409">Pick oldest batch</span></span></td>
<td><span data-ttu-id="c4383-410">作業者が任意の場所で最も古いバッチを最初にピッキングする必要があるかどうかを指示します。</span><span class="sxs-lookup"><span data-stu-id="c4383-410">Indicate whether the worker must pick the oldest batch in a location first.</span></span> <span data-ttu-id="c4383-411">次のオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="c4383-411">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="c4383-412"><strong>なし</strong> – 作業者はその場所でどのバッチでもピッキングできます。</span><span class="sxs-lookup"><span data-stu-id="c4383-412"><strong>None</strong> – The worker can pick any batch in the location.</span></span> <span data-ttu-id="c4383-413">メッセージは作業者に表示されません。</span><span class="sxs-lookup"><span data-stu-id="c4383-413">The worker receives no message.</span></span></li>
<li><span data-ttu-id="c4383-414"><strong>警告</strong> – 作業者はその場所でどのバッチでもピッキングできますが、バッチが最も古くない場合、警告メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c4383-414"><strong>Warn</strong> – The worker can pick any batch in the location, but he or she receives a warning message if a batch isn&#39;t the oldest batch.</span></span></li>
<li><span data-ttu-id="c4383-415"><strong>強制</strong> – 作業者はその場所で最も古いバッチをピッキングする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4383-415"><strong>Force</strong> – The worker must pick the oldest batch in the location.</span></span> <span data-ttu-id="c4383-416">作業者は、バッチが最も古いバッチではないときに、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c4383-416">The worker receives an error message if a batch isn&#39;t the oldest batch.</span></span> <span data-ttu-id="c4383-417"><strong>注意:</strong> このオプションは、<strong>バッチ番号</strong>が品目に割り当てられている引当階層の<strong>場所</strong>よりも低い場合にのみ該当します。</span><span class="sxs-lookup"><span data-stu-id="c4383-417"><strong>Note:</strong> This option is relevant only if <strong>Batch number</strong> is lower than <strong>Location</strong> in the reservation hierarchy that is assigned to the item.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4383-418">ラベルの印刷</span><span class="sxs-lookup"><span data-stu-id="c4383-418">Print label</span></span></td>
<td><span data-ttu-id="c4383-419">作業者がライセンス プレート ラベルを印刷できるようにする場合は、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c4383-419">Select this option to let workers print license plate labels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4383-420">システム グループ化フィールド</span><span class="sxs-lookup"><span data-stu-id="c4383-420">System grouping field</span></span></td>
<td><span data-ttu-id="c4383-421">Supply Chain Management が作業者のピッキング作業をグループ化する方法を決定するためのフィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="c4383-421">Select the field that determine how Supply Chain Management will group picking work for workers.</span></span> <span data-ttu-id="c4383-422">たとえば、<strong>ShipmentId</strong> フィールドを選択した場合、作業者はピッキング作業をグループ化する出荷 ID をスキャンします。</span><span class="sxs-lookup"><span data-stu-id="c4383-422">For example, if you select the <strong>ShipmentId</strong> field, the worker will scan the shipment ID to group the picking work.</span></span> <span data-ttu-id="c4383-423">出荷のすべての作業が作業者に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="c4383-423">All work for the shipment is then assigned to the worker.</span></span> <span data-ttu-id="c4383-424">このフィールドは、システムによってグループ化された既存の作業を使用するメニュー項目の作成を要求します。</span><span class="sxs-lookup"><span data-stu-id="c4383-424">This field requires that you create a menu item to use existing work that is grouped by the system.</span></span> <span data-ttu-id="c4383-425">また、<strong>システム グループ化ラベル</strong> フィールドに、スキャンする内容を作業者に指示するテキストを入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4383-425">You must also enter text in the <strong>System grouping label</strong> field to instruct the worker what to scan.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4383-426">システム グループ化ラベル</span><span class="sxs-lookup"><span data-stu-id="c4383-426">System grouping label</span></span></td>
<td><span data-ttu-id="c4383-427">Supply Chain Management によってピッキング作業がグループ化されるときにスキャンする内容を作業者に指示するテキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="c4383-427">Enter the text that will instruct the worker what to scan when picking work is grouped by Supply Chain Management.</span></span> <span data-ttu-id="c4383-428"> <strong>ShipmentId</strong> フィールドを使用して出荷別にピッキング作業をグループ化する場合、このフィールドに<strong>出荷 ID</strong> を入力することができます。</span><span class="sxs-lookup"><span data-stu-id="c4383-428">For example, if you&#39;re using the <strong>ShipmentId</strong> field to group picking work by shipment, you might enter <strong>Shipment ID</strong> in the field.</span></span> <span data-ttu-id="c4383-429">このフィールドは、システムによってグループ化された既存の作業を使用するメニュー項目の作成を要求します。</span><span class="sxs-lookup"><span data-stu-id="c4383-429">This field requires that you create a menu item to use existing work that is grouped by the system.</span></span> <span data-ttu-id="c4383-430">また、<strong>システム グループ化</strong> フィールドでグループ化するフィールドを選択する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="c4383-430">You must also select the field to group by in the <strong>System grouping</strong> field.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4383-431">既定のデータを使用します</span><span class="sxs-lookup"><span data-stu-id="c4383-431">Use default data</span></span></td>
<td><span data-ttu-id="c4383-432">このオプションを選択すると、[アクション] ペインの<strong>既定のデータ</strong> ボタンを有効にし、毎日の作業で作業者に通常必要となるデータを表示するフィールドを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="c4383-432">Select this option to enable the <strong>Default data</strong> button on the Action Pane, where you can select fields to display data that a worker typically requires in his or her daily work.</span></span> <span data-ttu-id="c4383-433">このオプションは、たとえば、作業者がひんぱんに同じ場所から品目をピッキングする場合に役に立ちます。</span><span class="sxs-lookup"><span data-stu-id="c4383-433">This option is useful if, for example, a worker often picks items from the same location.</span></span> <span data-ttu-id="c4383-434"><strong>ソース場所</strong>フィールドを選択すると、既定で場所を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="c4383-434">You can select the <strong>From location</strong> field to display the location by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4383-435">検証済ユーザー主導フィールド</span><span class="sxs-lookup"><span data-stu-id="c4383-435">Validated User Directed Field</span></span></td>
<td><span data-ttu-id="c4383-436">作業者が作業をグループ化するためにスキャンするフィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="c4383-436">Select the field that the worker will scan to group the work.</span></span> <span data-ttu-id="c4383-437">たとえば、<strong>LoadId</strong> 選択した場合、作業者は、選択された積荷に関連付けられている作業をピッキングできます。</span><span class="sxs-lookup"><span data-stu-id="c4383-437">For example, if you select <strong>LoadId</strong>, a worker can pick any work that is associated with a selected load.</span></span> <span data-ttu-id="c4383-438">また、<strong>検証済ユーザー主導ラベル</strong> フィールドに、スキャンする内容を作業者に指示するテキストを入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4383-438">You must also enter text in the <strong>Validated User Directed Label</strong> field to instruct the worker what to scan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4383-439">検証済ユーザー主導ラベル</span><span class="sxs-lookup"><span data-stu-id="c4383-439">Validated User Directed Label</span></span></td>
<td><span data-ttu-id="c4383-440">ピッキング作業が検証済ユーザー主導フィールドによってグループ化されるときにスキャンする内容を作業者に指示するテキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="c4383-440">Enter the text that will instruct the worker what to scan when picking work is grouped by a validated user-directed field.</span></span> <span data-ttu-id="c4383-441">たとえば、<strong>LoadId</strong> フィールドを使用して積荷のピッキング作業をグループ化する場合、このフィールドに <strong>積荷 ID</strong> を入力することができます。</span><span class="sxs-lookup"><span data-stu-id="c4383-441">For example, if you’re using the <strong>LoadId</strong> field to group picking work for a load, you might enter <strong>Load ID</strong> in the field.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4383-442">作業テンプレートのコード</span><span class="sxs-lookup"><span data-stu-id="c4383-442">Work template code</span></span></td>
<td><span data-ttu-id="c4383-443">プロセスの作業を作成する作業テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="c4383-443">Select the work template that will create the work for a process.</span></span> <span data-ttu-id="c4383-444">たとえば、発注書の品目を受け取る場合、プット アウェイ作業は、作業テンプレートに基づいて生成されます。</span><span class="sxs-lookup"><span data-stu-id="c4383-444">For example, if you receive an item for a purchase order, the put-away work will be generated based on the work template.</span></span> <span data-ttu-id="c4383-445">作業テンプレートを選択しない場合、Supply Chain Management はクエリ基準に基づいてテンプレートを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="c4383-445">If you don&#39;t select a work template, Supply Chain Management assigns a template, based on query criteria.</span></span> <span data-ttu-id="c4383-446">作業のテンプレートの詳細については、<a href="control-warehouse-location-directives.md">作業テンプレートと場所ディレクティブの倉庫作業の制御</a> を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c4383-446">For more information about work templates, see <a href="control-warehouse-location-directives.md">Controlling warehouse work with work templates and location directives</a>.</span></span></td>
<tr class="even">
<td><span data-ttu-id="c4383-447">作業明細行リストの表示</span><span class="sxs-lookup"><span data-stu-id="c4383-447">Show work line list</span></span></td>
<td><span data-ttu-id="c4383-448">作業者が現在選択しているピッキング作業の明細行を表示、操作する方法についてのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c4383-448">Select an option for how workers will be able to view and interact with the lines for the currently selected picking work.</span></span> <span data-ttu-id="c4383-449">このオプションの詳細については、<a href="pick-line-overview.md">モバイル デバイスのメニュー項目の設定</a>を参照して、ピック行の概要を指定してください。</span><span class="sxs-lookup"><span data-stu-id="c4383-449">For more information about this option, see <a href="pick-line-overview.md">Set up a mobile device menu item to provide a pick line overview</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="require-workers-to-confirm-the-product-location-or-quantity-when-they-pick-items"></a><span data-ttu-id="c4383-450">品目のピッキング時に製品、場所、または数量の確認を作業者に要求</span><span class="sxs-lookup"><span data-stu-id="c4383-450">Require workers to confirm the product, location, or quantity when they pick items</span></span>
<span data-ttu-id="c4383-451">作業者が、倉庫内で作業をするときに場所または数量をモバイル デバイスで登録することを要求する、作業の確認を設定できます。</span><span class="sxs-lookup"><span data-stu-id="c4383-451">You can set up work confirmations that require that a worker use a mobile device to register the location or quantity when they perform work in the warehouse.</span></span> <span data-ttu-id="c4383-452">作業確認によって、作業者が正しい場所にいるか、または品目の正しい数量を処理しているかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="c4383-452">Work confirmations help ensure that the worker is at the correct location or is handling the correct quantity of items.</span></span> <span data-ttu-id="c4383-453">また、作業者の登録を自動的に確認するように Supply Chain Management を有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="c4383-453">You can also enable Supply Chain Management to automatically confirm the worker’s registration.</span></span> <span data-ttu-id="c4383-454">自動確認を有効にする場合は、場所または数量に対する確認を同時に要求することはできません。</span><span class="sxs-lookup"><span data-stu-id="c4383-454">If you enable automatic confirmation, you can't also require confirmations for location or quantity.</span></span> <span data-ttu-id="c4383-455">作業の確認には製品と製品バリアントも含まれます。</span><span class="sxs-lookup"><span data-stu-id="c4383-455">Work confirmations also include products and product variants.</span></span> <span data-ttu-id="c4383-456">また、バーコードのスキャンによって確認を登録できます。</span><span class="sxs-lookup"><span data-stu-id="c4383-456">Additionally, you can register confirmations by scanning a bar code.</span></span> <span data-ttu-id="c4383-457">製品および製品バリアントを確認するには、製品または製品バリアントの ID を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4383-457">To confirm products and product variants, you must enter an ID for the product or product variant.</span></span> <span data-ttu-id="c4383-458">この ID には、製品 ID、製品検索 ID、外部 ID、GTIN、またはバーコードがあります。</span><span class="sxs-lookup"><span data-stu-id="c4383-458">This ID can be a product ID, product search ID, external ID, GTIN, or bar code.</span></span> <span data-ttu-id="c4383-459">ID の入力後、またはバーコードのスキャン後、製品バリアントの分析コードがモバイル デバイスに表示されます。</span><span class="sxs-lookup"><span data-stu-id="c4383-459">After you enter the ID or scan the bar code, the dimensions for the product variant are displayed on the mobile device.</span></span> 

<span data-ttu-id="c4383-460">次の表では、作業確認に使用できるさまざまな作業タイプを示します。</span><span class="sxs-lookup"><span data-stu-id="c4383-460">The following table describes the various work types that you can use work confirmations with.</span></span>

| <span data-ttu-id="c4383-461">オプション</span><span class="sxs-lookup"><span data-stu-id="c4383-461">Option</span></span> | <span data-ttu-id="c4383-462">説明</span><span class="sxs-lookup"><span data-stu-id="c4383-462">Description</span></span> |
|------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="c4383-463">選択</span><span class="sxs-lookup"><span data-stu-id="c4383-463">Pick</span></span> | <span data-ttu-id="c4383-464">品目のピッキング時に確認を要求します。</span><span class="sxs-lookup"><span data-stu-id="c4383-464">Require confirmation when items are picked.</span></span> |
| <span data-ttu-id="c4383-465">プット</span><span class="sxs-lookup"><span data-stu-id="c4383-465">Put</span></span> | <span data-ttu-id="c4383-466">品目を場所に置くときに確認を要求します。</span><span class="sxs-lookup"><span data-stu-id="c4383-466">Require confirmation when items are put in a location.</span></span> |
| <span data-ttu-id="c4383-467">棚卸</span><span class="sxs-lookup"><span data-stu-id="c4383-467">Counting</span></span> | <span data-ttu-id="c4383-468">循環棚卸時に確認を要求します。</span><span class="sxs-lookup"><span data-stu-id="c4383-468">Require confirmation during cycle counting.</span></span> |
| <span data-ttu-id="c4383-469">調整</span><span class="sxs-lookup"><span data-stu-id="c4383-469">Adjustments</span></span> | <span data-ttu-id="c4383-470">在庫数量の調整時に確認を要求します。</span><span class="sxs-lookup"><span data-stu-id="c4383-470">Require confirmation when inventory quantities are adjusted.</span></span> |
| <span data-ttu-id="c4383-471">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="c4383-471">Custom</span></span> | <span data-ttu-id="c4383-472">ユーザ指定の作業に確認を要求します。</span><span class="sxs-lookup"><span data-stu-id="c4383-472">Require confirmation for custom work.</span></span> |
| <span data-ttu-id="c4383-473">検査</span><span class="sxs-lookup"><span data-stu-id="c4383-473">Quarantine</span></span> | <span data-ttu-id="c4383-474">品目を検査に移動するときに確認を要求します。</span><span class="sxs-lookup"><span data-stu-id="c4383-474">Require confirmation when items are moved to quarantine.</span></span> |
| <span data-ttu-id="c4383-475">ライセンス プレートの構築</span><span class="sxs-lookup"><span data-stu-id="c4383-475">License plate building</span></span> | <span data-ttu-id="c4383-476">品目を統合してライセンス プレートを作成するときに確認を要求します。</span><span class="sxs-lookup"><span data-stu-id="c4383-476">Require confirmation when items are consolidated to build a license plate.</span></span> |
| <span data-ttu-id="c4383-477">印刷</span><span class="sxs-lookup"><span data-stu-id="c4383-477">Print</span></span> | <span data-ttu-id="c4383-478">ライセンス プレート ラベルの印刷時に確認を要求します。</span><span class="sxs-lookup"><span data-stu-id="c4383-478">Require confirmation when license plate labels are printed.</span></span> |
| <span data-ttu-id="c4383-479">状態変更</span><span class="sxs-lookup"><span data-stu-id="c4383-479">Status change</span></span> | <span data-ttu-id="c4383-480">在庫の状態を変更するときに確認を要求します。</span><span class="sxs-lookup"><span data-stu-id="c4383-480">Require confirmation when the status of inventory is changed.</span></span> |

> [!NOTE]
> <span data-ttu-id="c4383-481">ピッキングとプット作業タイプに対してのみ製品の確認を要求できます。</span><span class="sxs-lookup"><span data-stu-id="c4383-481">You can require product confirmation only for pick and put work types.</span></span>

<a name="additional-resources"></a><span data-ttu-id="c4383-482">追加リソース</span><span class="sxs-lookup"><span data-stu-id="c4383-482">Additional resources</span></span>
--------

[<span data-ttu-id="c4383-483">タイプが発注書のタスクを完了するためのモバイル デバイスのメニュー項目を設定します。</span><span class="sxs-lookup"><span data-stu-id="c4383-483">Set up a mobile device menu item for completing work of type Purchase order</span></span>](tasks/set-up-mobile-device-menu.md)

[<span data-ttu-id="c4383-484">入庫済品目を登録するためのモバイル デバイスのメニュー項目の設定</span><span class="sxs-lookup"><span data-stu-id="c4383-484">Set up a mobile device menu item to register received items</span></span>](tasks/set-up-mobile-device-menu-item-register-received-items.md)

[<span data-ttu-id="c4383-485">在庫状態</span><span class="sxs-lookup"><span data-stu-id="c4383-485">Inventory statuses</span></span>](../inventory/inventory-statuses.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]