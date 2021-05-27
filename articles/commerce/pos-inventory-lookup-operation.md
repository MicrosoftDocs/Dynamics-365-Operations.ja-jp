---
title: POS での在庫検索操作
description: このトピックでは、Dynamics 365 Commerce 販売時点管理 (POS) で在庫検索操作を使用して、店舗および倉庫全体で製品の利用可能な在庫を確認する方法 について説明します。
author: boycezhu
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.openlocfilehash: 873c6413c14d2ee8315c149ee9c495bb59dbd930
ms.sourcegitcommit: 11ca5863175150b6c39f47a9322caa2186727a26
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025451"
---
# <a name="inventory-lookup-operation-in-pos"></a><span data-ttu-id="7f978-103">POS での在庫検索操作</span><span class="sxs-lookup"><span data-stu-id="7f978-103">Inventory lookup operation in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7f978-104">このトピックでは、Dynamics 365 Commerce 販売時点管理 (POS) で在庫検索操作を使用して、店舗および倉庫全体で製品の利用可能な在庫を確認する方法 について説明します。</span><span class="sxs-lookup"><span data-stu-id="7f978-104">This topic describes how to use the inventory lookup operation in Dynamics 365 Commerce point of sale (POS) to view the on-hand inventory availability of products across stores and warehouses.</span></span>

<span data-ttu-id="7f978-105">組織間の在庫の正確な表示により、店舗関係者が適切なタイミングで、効果的な顧客サービスを提供できるようにします。</span><span class="sxs-lookup"><span data-stu-id="7f978-105">An accurate view of inventory across an organization helps store associates provide timely, effective customer service.</span></span> <span data-ttu-id="7f978-106">最も重要な時点は、顧客が購入決定をする準備ができている時点です。</span><span class="sxs-lookup"><span data-stu-id="7f978-106">The moment that matters most is the moment when a customer is ready to make a purchase decision.</span></span> <span data-ttu-id="7f978-107">製品の出荷や受取を正確に保証できるように、小売り店舗のレジ担当者が、リアルタイムまたは準リアルタイムの在庫情報に精通していることが重要です。</span><span class="sxs-lookup"><span data-stu-id="7f978-107">It's important that cashiers in a retail store have real-time or near real-time inventory information at their fingertips, so that they can accurately promise product delivery and pickup.</span></span>

<span data-ttu-id="7f978-108">Commerce POS の在庫検索操作は、小売業者がオペレーショナル エクセレンスを達成し、店舗を Commerce 本社と関連付することで情報を得るのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="7f978-108">The inventory lookup operation in Commerce POS helps retailers achieve operational excellence and gain insights by connecting stores with Commerce headquarters.</span></span> <span data-ttu-id="7f978-109">この機能により、店舗および倉庫全体で製品の在庫を確認できます。</span><span class="sxs-lookup"><span data-stu-id="7f978-109">This functionality provides an inventory availability view of products across stores and warehouses.</span></span> <span data-ttu-id="7f978-110">また、リアルタイムで計画在庫を改善することにより、小売業者がさらに効率性およびコスト削減を向上するのを助けます。</span><span class="sxs-lookup"><span data-stu-id="7f978-110">It also helps retailers drive additional efficiencies and cost savings by improving inventory planning in real time.</span></span>

<span data-ttu-id="7f978-111">POS アプリケーションから在庫検索操作を開始すると、POS レジ係は数値キーボードを使用して、在庫情報を照会する製品番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="7f978-111">When the inventory lookup operation is started from the POS application, the POS cashier uses the numeric keyboard to enter a product number to query its inventory information.</span></span> <span data-ttu-id="7f978-112">入力した製品にバリアントがある場合は、必要に応じて分析コードまたは他の値を選択して、特定の製品バリアントの在庫情報を確認できます。</span><span class="sxs-lookup"><span data-stu-id="7f978-112">If the product entered has variants, the cashier can optionally select dimensions or other values to check inventory information of a specific product variant.</span></span>

## <a name="inventory-lookup-list-view-for-individual-products"></a><span data-ttu-id="7f978-113">個々の製品の在庫検索リスト ビュー</span><span class="sxs-lookup"><span data-stu-id="7f978-113">Inventory lookup list view for individual products</span></span>

<span data-ttu-id="7f978-114">在庫検索操作では、個々の製品について、在庫場所の一覧に対して次の製品情報を示す在庫検索リスト ビューが提供されます。</span><span class="sxs-lookup"><span data-stu-id="7f978-114">For an individual product, the inventory lookup operation provides an inventory lookup list view showing the following product information for a list of locations:</span></span>

- <span data-ttu-id="7f978-115">**在庫** - 製品の「引当可能現物」数量を参照します。</span><span class="sxs-lookup"><span data-stu-id="7f978-115">**Inventory** - Refers to the "available physical" quantity of a product.</span></span>
- <span data-ttu-id="7f978-116">**予約済み** - 本社から取得された「予約済み」数量を参照します。</span><span class="sxs-lookup"><span data-stu-id="7f978-116">**Reserved** - Refers to the "physical reserved" quantity retrieved from headquarters.</span></span>
- <span data-ttu-id="7f978-117">**注文済み** - 本社から取得された「注文済み」数量を参照します。</span><span class="sxs-lookup"><span data-stu-id="7f978-117">**Ordered** - Refers to the "ordered in total" quantity retrieved from headquarters.</span></span>
- <span data-ttu-id="7f978-118">**単位** - 本社で設定された在庫測定単位を参照します。</span><span class="sxs-lookup"><span data-stu-id="7f978-118">**Unit** - Refers to the inventory unit of measure configured in headquarters.</span></span>

<span data-ttu-id="7f978-119">場所のリスト ビューには、次の例の画像のように、現在の店舗がリンクされているフルフィルメント グループで構成されているすべての店舗および倉庫が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7f978-119">The list view of locations includes all stores and warehouses that are configured in the fulfillment groups that the current store is linked to, as shown in the following example image.</span></span>

![在庫検索操作リスト ビュー](media/inventory-lookup-list-view.png)

<span data-ttu-id="7f978-121">以下のアクションは、POS アプリ バーで利用できます。</span><span class="sxs-lookup"><span data-stu-id="7f978-121">The following actions are available on the POS app bar:</span></span>

- <span data-ttu-id="7f978-122">**並べ替え** - このアクションにより、POS ユーザーは、さまざまな基準に基づいてリスト ビューのデータを並べ替えます。</span><span class="sxs-lookup"><span data-stu-id="7f978-122">**Sort** - This action lets the POS user sort the data in the list view based on various criteria.</span></span> <span data-ttu-id="7f978-123">場所に基づく並べ替えは、既定の並べ替えオプションです。</span><span class="sxs-lookup"><span data-stu-id="7f978-123">Location-based sorting is the default sort option.</span></span> 
  - <span data-ttu-id="7f978-124">**地理的場所** (現在の店舗と比較して最も近い場所から最も遠い場所の順)</span><span class="sxs-lookup"><span data-stu-id="7f978-124">**Geo location** (from the closest location to the farthest location, compared with the current store)</span></span>
  - <span data-ttu-id="7f978-125">**名前** (昇順または降順)</span><span class="sxs-lookup"><span data-stu-id="7f978-125">**Name** (in ascending or descending order)</span></span>
  - <span data-ttu-id="7f978-126">**店舗番号** (昇順または降順)</span><span class="sxs-lookup"><span data-stu-id="7f978-126">**Store number** (in ascending or descending order)</span></span>
  - <span data-ttu-id="7f978-127">**在庫** (降順)</span><span class="sxs-lookup"><span data-stu-id="7f978-127">**Inventory** (in descending order)</span></span>
  - <span data-ttu-id="7f978-128">**予約済み** (降順)</span><span class="sxs-lookup"><span data-stu-id="7f978-128">**Reserved** (in descending order)</span></span>
  - <span data-ttu-id="7f978-129">**注文済み** (降順)</span><span class="sxs-lookup"><span data-stu-id="7f978-129">**Ordered** (in descending order)</span></span>
- <span data-ttu-id="7f978-130">**フィルター** - このアクションにより、POS ユーザーは特定の場所のフィルター済みデータを表示できます。</span><span class="sxs-lookup"><span data-stu-id="7f978-130">**Filter** - This action lets the POS user view filtered data for a specific location.</span></span>
- <span data-ttu-id="7f978-131">**店舗の可用性を表示する** - このアクションにより、POS ユーザーは、選択した店舗の製品のATP (利用可能数量 ) を表示できます。</span><span class="sxs-lookup"><span data-stu-id="7f978-131">**Show store availability** - This action lets the POS user view the available-to-promise (ATP) quantities for a product in the selected store.</span></span>
- <span data-ttu-id="7f978-132">**店舗の場所を表示する** - このアクションは、選択した店舗のマップ ビュー、住所、および店舗の営業時間を表示する別のページを開きます。</span><span class="sxs-lookup"><span data-stu-id="7f978-132">**Show store location** - This action opens a separate page to show the map view, address, and store hours for the selected store.</span></span>
- <span data-ttu-id="7f978-133">**店舗で受け取り** - このアクションでは選択した店舗から集荷される製品の顧客注文を作成し、トランザクション画面にユーザーをリダイレクトします。</span><span class="sxs-lookup"><span data-stu-id="7f978-133">**Pick up in store** - This action creates a customer order for the product that will be picked up from the selected store, and redirects the user to the transaction screen.</span></span>
- <span data-ttu-id="7f978-134">**製品の出荷** - このアクションでは選択した店舗から出荷される製品の顧客注文を作成し、トランザクション画面にユーザーをリダイレクトします。</span><span class="sxs-lookup"><span data-stu-id="7f978-134">**Ship product** - This action creates a customer order for the product that will be shipped from the selected store, and redirects the user to the transaction screen.</span></span>
- <span data-ttu-id="7f978-135">**すべてのバリアントを表示する** - バリアントを持つ製品の場合、このアクションはリスト ビューから、製品のすべてのバリアントの在庫情報を表示するマトリックス ビューに切り替わります。</span><span class="sxs-lookup"><span data-stu-id="7f978-135">**View all variants** - For a product with variants, this action switches from a list view to a matrix view that displays inventory information for all variants of the product.</span></span>
- <span data-ttu-id="7f978-136">**トランザクションに追加** - このアクションによって製品がカートに追加され、ユーザーはトランザクション画面にリダイレクトされます。</span><span class="sxs-lookup"><span data-stu-id="7f978-136">**Add to transaction** - This action adds the product to the cart and redirects the user to the transaction screen.</span></span>

> [!NOTE]
> <span data-ttu-id="7f978-137">場所に基づく並べ替えの場合、場所と現在の店舗の間の距離は、Commerce 本社で定義された座標 (緯度と経度) によって決定されます。</span><span class="sxs-lookup"><span data-stu-id="7f978-137">For a location-based sort, the distance between a location and current store is determined by the coordinates (latitude and longitude) defined in Commerce headquarters.</span></span> <span data-ttu-id="7f978-138">店舗の場合、場所情報は、その店舗に関連付けられている作業単位の基本住所で定義されます。</span><span class="sxs-lookup"><span data-stu-id="7f978-138">For a store, the location information is defined in the primary address of the operating unit associated with the store.</span></span> <span data-ttu-id="7f978-139">店舗以外の倉庫の場合、場所の情報は倉庫の住所で定義されます。</span><span class="sxs-lookup"><span data-stu-id="7f978-139">For a non-store warehouse, the location information is defined in the warehouse address.</span></span> <span data-ttu-id="7f978-140">現在の店舗に座標が適切に定義されていない場合は、場所ベースの並べ替えオプションにより一覧の最上部に現在の店舗が表示され、他の場所が名前で並べ替えられます。</span><span class="sxs-lookup"><span data-stu-id="7f978-140">If the current store doesn't have coordinates properly defined, the location-based sort option will display the current store at the top of the list and then sort other locations by name.</span></span>

> [!NOTE]
> <span data-ttu-id="7f978-141">**店舗の可用性を表示する**、**店舗の場所を表示する**、**店舗での受取り**、および **製品の出荷** アクションは、店舗以外の場所 では使用できません。</span><span class="sxs-lookup"><span data-stu-id="7f978-141">The **Show store availability**, **Show store location**, **Pick up in store**, and **Ship product** actions are not available for non-store locations.</span></span>

## <a name="inventory-lookup-matrix-view-for-variants"></a><span data-ttu-id="7f978-142">バリアントの在庫検索マトリックス ビュー</span><span class="sxs-lookup"><span data-stu-id="7f978-142">Inventory lookup matrix view for variants</span></span>

<span data-ttu-id="7f978-143">バリアントを持つマスター製品の場合は、在庫検索操作によって、選択した場所でマスター製品のすべてのバリアントの在庫引当情報を表示する分析コード ベースのマトリックス ビューも表示されます。</span><span class="sxs-lookup"><span data-stu-id="7f978-143">For a master product with variants, the inventory lookup operation also provides a dimension-based matrix view that displays inventory availability information for all variants of the master product at a selected location.</span></span> <span data-ttu-id="7f978-144">既定では、マトリックス ビューに現在の店舗のデータが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7f978-144">By default, the matrix view shows data for the current store.</span></span> <span data-ttu-id="7f978-145">アプリ バーの **店舗** アクションを使用すると、現在の店舗がリンクされているフルフィルメント グループに設定されている他の店舗の在庫情報 を検索できます。</span><span class="sxs-lookup"><span data-stu-id="7f978-145">You can use the **Store** action on the app bar to look up inventory information at other stores configured in the fulfillment groups that the current store is linked to.</span></span>

<span data-ttu-id="7f978-146">次の例の画像は、POS の在庫検索マトリックス ビューを示しています。</span><span class="sxs-lookup"><span data-stu-id="7f978-146">The following example image shows the inventory lookup matrix view in POS.</span></span>

![在庫検索操作マトリックス ビュー](media/inventory-lookup-matrix-view.png)

<span data-ttu-id="7f978-148">マトリックス ビューでは、各セルは個々のバリアントを表し、右下隅に手持在庫 (引当可能現物) の値と、左上隅の **引当済み** (現物引当済み) および **注文済み** (発注済み) の値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7f978-148">In the matrix view, each cell represents an individual variant, and displays an on-hand inventory (available physical) value in the lower-right corner, as well as **reserved** (physical reserved) and **ordered** (ordered in total) values in the upper-left corner.</span></span> <span data-ttu-id="7f978-149">次の表では、さまざまな手持値の意味について説明します。</span><span class="sxs-lookup"><span data-stu-id="7f978-149">The following table explains the meaning of the various on-hand values.</span></span>

| <span data-ttu-id="7f978-150">手持の金額</span><span class="sxs-lookup"><span data-stu-id="7f978-150">On-hand value</span></span>                            | <span data-ttu-id="7f978-151">説明</span><span class="sxs-lookup"><span data-stu-id="7f978-151">Description</span></span> |
|------------------------------------------|-------------|
| <span data-ttu-id="7f978-152">0 (ゼロ) よりも大きい数値</span><span class="sxs-lookup"><span data-stu-id="7f978-152">Numeric value that is more than 0 (zero)</span></span> | <span data-ttu-id="7f978-153">バリアントは選択した場所にリリースされており、セルに追加のアクションを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="7f978-153">A variant has been released to the selected location, and you can perform additional actions in the cell.</span></span> |
| <span data-ttu-id="7f978-154">**0** (ゼロ)</span><span class="sxs-lookup"><span data-stu-id="7f978-154">**0** (zero)</span></span>                             | <span data-ttu-id="7f978-155">バリアントが選択した場所にリリースされていても、品目は選択した場所で使用できません。</span><span class="sxs-lookup"><span data-stu-id="7f978-155">A variant has been released to the selected location, but the item isn't available at the selected location.</span></span> <span data-ttu-id="7f978-156">セルに追加のアクションを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="7f978-156">You can perform additional actions in the cell.</span></span> |
| <span data-ttu-id="7f978-157">**該当なし**、または無効なセル</span><span class="sxs-lookup"><span data-stu-id="7f978-157">**n/a**, or an inactive cell</span></span>              | <span data-ttu-id="7f978-158">バリアントは選択した場所にリリースされておらず、セルに追加のアクションを実行することができません。</span><span class="sxs-lookup"><span data-stu-id="7f978-158">A variant hasn't been released to the selected location, and you can't perform additional actions in the cell.</span></span> |

<span data-ttu-id="7f978-159">マトリックス ビューでの分析コード値の表示順序は、Commerce 本社での分析コード表示注文コンフィギュレーションに基づいています。</span><span class="sxs-lookup"><span data-stu-id="7f978-159">The display order of the dimension values in the matrix view is based on the dimension display order configuration in Commerce headquarters.</span></span> <span data-ttu-id="7f978-160">使用する新しい分析コードを選択することで、分析コード表示順序のコンフィギュレーションを変更できます。</span><span class="sxs-lookup"><span data-stu-id="7f978-160">You can change the dimension display order configuration by selecting a new dimension to use.</span></span> 

<span data-ttu-id="7f978-161">マトリックス ビュー セルでは、次アクションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="7f978-161">The following actions are available in the matrix view cell:</span></span>

- <span data-ttu-id="7f978-162">**すぐに販売** - このアクションによって選択したバリアントがカートに追加され、ユーザーはトランザクション画面にリダイレクトされます。</span><span class="sxs-lookup"><span data-stu-id="7f978-162">**Sell now** - This action adds the selected variant to the cart, and redirects the user to the transaction screen.</span></span>
- <span data-ttu-id="7f978-163">**店舗で受け取り** - このアクションでは選択した店舗から集荷される選択したバリアントの顧客注文を作成し、トランザクション画面にユーザーをリダイレクトします。</span><span class="sxs-lookup"><span data-stu-id="7f978-163">**Pick up in store** - This action creates a customer order for the selected variant that will be picked up from the selected store, and redirects the user to the transaction screen.</span></span>
- <span data-ttu-id="7f978-164">**製品の出荷** - このアクションでは選択した店舗から出荷される選択したバリアントの顧客注文を作成し、トランザクション画面にユーザーをリダイレクトします。</span><span class="sxs-lookup"><span data-stu-id="7f978-164">**Ship product** - This action creates a customer order for the selected variant that will be shipped from the selected store, and redirects the user to the transaction screen.</span></span>
- <span data-ttu-id="7f978-165">**引当可能性** - このアクションでは、選択した店舗で選んだバリアントの ATP 数量を示す別のページ にユーザーを移動します。</span><span class="sxs-lookup"><span data-stu-id="7f978-165">**Availability** - This action takes the user to a separate page showing the ATP quantities for the selected variant in the selected store.</span></span>
- <span data-ttu-id="7f978-166">**すべての場所を表示する** - このアクションは、選択したバリアントの在庫情報を示す標準の引当可能在庫数量リスト ビューに切り替えます。</span><span class="sxs-lookup"><span data-stu-id="7f978-166">**Show all locations** - This action switches to the standard inventory availability list view showing the inventory information for the selected variant.</span></span>
- <span data-ttu-id="7f978-167">**製品の詳細を表示する** - このアクションにより、選択したバリアントの製品詳細ページ (PDP) にリダイレクトされます。</span><span class="sxs-lookup"><span data-stu-id="7f978-167">**View product details** - This action redirects the user to the product details page (PDP) of the selected variant.</span></span>

## <a name="access-inventory-lookup-from-other-pages-in-pos"></a><span data-ttu-id="7f978-168">POS の他のページから在庫検索へアクセスする</span><span class="sxs-lookup"><span data-stu-id="7f978-168">Access inventory lookup from other pages in POS</span></span>

<span data-ttu-id="7f978-169">POS ユーザーは、POS の他のページから在庫検索操作にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="7f978-169">POS users can access the inventory lookup operation from other pages in POS.</span></span>

<span data-ttu-id="7f978-170">次の例の画像は、POS の PDP からの在庫検索結果を示しています。</span><span class="sxs-lookup"><span data-stu-id="7f978-170">The following example image shows inventory lookup results from a PDP in POS.</span></span>

![製品の詳細ページからの在庫検索](media/inventory-lookup-from-product-details-page.png)

<span data-ttu-id="7f978-172">マスター製品の PDP で、アプリケーション バーの **すべてのバリアントの表示** アクションを使用して、製品のすべてのバリアントについて、現在の店舗の在庫引当可能情報を表示する在庫検索マトリックス ビューを起動できます。</span><span class="sxs-lookup"><span data-stu-id="7f978-172">On the PDP of a master product, you can use the **View all variants** action on the app bar to launch the inventory lookup matrix view that displays inventory availability information for the current store for all variants of a product.</span></span> <span data-ttu-id="7f978-173">個々の製品の場合、PDP は現在の店舗のその製品の手持在庫 (引当可能現物数) 値を表示します。</span><span class="sxs-lookup"><span data-stu-id="7f978-173">For an individual product, the PDP displays the on-hand inventory (available physical) value of that product for the current store.</span></span> <span data-ttu-id="7f978-174">また、**その他の店舗の在庫** リンクを選択して在庫検索操作を開始し、他の店舗または倉庫全体の製品の在庫引当可能数量を確認できます。</span><span class="sxs-lookup"><span data-stu-id="7f978-174">Additionally, you can select the **Other stores inventory** link to launch the inventory lookup operation to check the inventory availability of a product across other stores or warehouses.</span></span>

> [!NOTE]
> <span data-ttu-id="7f978-175">**すべてのバリアントの表示** アクションは、バリアントを持つマスター製品に対してのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="7f978-175">The **View all variants** action on the PDP is available only for master products that have variants.</span></span> <span data-ttu-id="7f978-176">特定の製品やキットには使用できません。</span><span class="sxs-lookup"><span data-stu-id="7f978-176">It isn't available for specific products or kits.</span></span>

<span data-ttu-id="7f978-177">POS トランザクション画面のボタン グリッドにリンクとして表示される在庫検索操作を構成できます。</span><span class="sxs-lookup"><span data-stu-id="7f978-177">You can configure the inventory lookup operation to appear as a link in the button grid on the POS transaction screen.</span></span> <span data-ttu-id="7f978-178">コンフィギュレーション後、ユーザーがカートの行を選択して **在庫検索** ボタンを選択すると、選択した製品の在庫検索リスト ビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7f978-178">After configuration, when the user selects a cart line and then selects the **Inventory lookup** button, the inventory lookup list view for the selected product will be displayed.</span></span> <span data-ttu-id="7f978-179">POS 画面レイアウト デザイナー ツールを使用してボタン グリッドをコンフィギュレーションする方法の詳細については、[POS ユーザー インターフェイスの視覚コンフィギュレーション](pos-screen-layouts.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7f978-179">For more information about how to configure button grids using POS screen layout designer tool, see [POS user interface visual configurations](pos-screen-layouts.md).</span></span>

## <a name="inventory-lookup-with-channel-side-calculation"></a><span data-ttu-id="7f978-180">チャネル側の計算を使用した在庫検索</span><span class="sxs-lookup"><span data-stu-id="7f978-180">Inventory lookup with channel-side calculation</span></span>

<span data-ttu-id="7f978-181">Commerce リリース 10.0.9 以前では、在庫検索操作で使用可能な **引当可能現物** の値が、リアルタイム サービス コールを通じて Commerce 本社から取得されます。</span><span class="sxs-lookup"><span data-stu-id="7f978-181">In Commerce release 10.0.9 and earlier, the **available physical** value in the inventory lookup operation is retrieved from Commerce headquarters via a real-time service call.</span></span> <span data-ttu-id="7f978-182">Commerce リリース 10.0.10 以降では、POS 在庫検索操作を構成して Commerce サーバーでチャンネル側の計算を使用して引当可能現物の値を決定できます。これにより、本社にまだ同期されていないトランザクション データを考慮することで、より信頼性が高く正確な在庫の見積を提供できます。</span><span class="sxs-lookup"><span data-stu-id="7f978-182">In Commerce release 10.0.10 and later, you can configure the POS inventory lookup operation to use channel-side calculation on the Commerce server to determine the available physical value, which can provide a more reliable and more accurate estimate of the on-hand inventory by factoring in the transactional data that is not yet synchronized to headquarters.</span></span> <span data-ttu-id="7f978-183">本社でのチャネル側の在庫計算および関連する POS コンフィギュレーションの詳細については、[小売チャネルの在庫可能性の計算](calculated-inventory-retail-channels.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7f978-183">For more information about channel-side inventory calculation and related POS configuration in headquarters, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7f978-184">追加リソース</span><span class="sxs-lookup"><span data-stu-id="7f978-184">Additional resources</span></span>

[<span data-ttu-id="7f978-185">POS ユーザー インターフェイスのビジュアル コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="7f978-185">POS user interface visual configurations</span></span>](pos-screen-layouts.md)

[<span data-ttu-id="7f978-186">小売チャンネルの引当可能在庫数量の計算</span><span class="sxs-lookup"><span data-stu-id="7f978-186">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
