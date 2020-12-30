---
title: POS での注文の取り消し操作
description: このトピックでは、POS の注文の取り消しページを改善するために使用できる機能について説明します。
author: hhainesms
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 42b11ff16757d633b868dfdf248341193a44378f
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665301"
---
# <a name="recall-order-operation-in-pos"></a><span data-ttu-id="95723-103">POS での注文の取り消し操作</span><span class="sxs-lookup"><span data-stu-id="95723-103">Recall order operation in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="95723-104">コマースの販売時点管理 (POS) の **注文の取り消し** 処理では、更新された注文の検索およびフィルタ機能と注文固有の情報が提供されます。</span><span class="sxs-lookup"><span data-stu-id="95723-104">The **Recall order** operation in the Commerce point of sale (POS) provides updated order search and filtering features and order-specific information.</span></span> <span data-ttu-id="95723-105">この機能は、コマース バージョン 10.0.15 およびこれ以降でのみ利用できます。</span><span class="sxs-lookup"><span data-stu-id="95723-105">This feature is available in Commerce versions 10.0.15 and later.</span></span>

<span data-ttu-id="95723-106">この機能を有効にするには、コマース本社の **機能管理** で **POS の取消し注文操作の改善** 機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="95723-106">To enable this functionality, turn the **Improved Recall order operation in POS** feature on in **Feature management** workspace in Commerce headquarters.</span></span> <span data-ttu-id="95723-107">機能を有効にした後、POS の[スクリーン レイアウト](pos-screen-layouts.md) を更新し、変更された機能の一部を利用することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="95723-107">After you enable the feature, consider updating your [screen layouts](pos-screen-layouts.md) in POS to take advantage of some of the changed  capabilities.</span></span>

<span data-ttu-id="95723-108">**注文の取り消し** 操作ボタンの構成により、組織が事前定義された表示で操作を展開できるようにします。</span><span class="sxs-lookup"><span data-stu-id="95723-108">The configuration of the **Recall order** operation button allows organizations to deploy the operation with a pre-defined display.</span></span>

![ボタン グリッド構成](media/recallorderbuttongrid.png)

<span data-ttu-id="95723-110">表示オプションは以下の通りです。</span><span class="sxs-lookup"><span data-stu-id="95723-110">The display options are as follows.</span></span>
- <span data-ttu-id="95723-111">**なし** – このオプションは、特定表示なしで操作を展開します。</span><span class="sxs-lookup"><span data-stu-id="95723-111">**None** – This option deploys the operation with no specific display.</span></span> <span data-ttu-id="95723-112">ユーザーがこの構成で工程を開くと、注文を検索して見つけるか、定義済みの注文フィルターから選択するかを確認するメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="95723-112">When a user opens the operation with this configuration, they will be prompted to search and find orders or choose from a pre-defined order filter.</span></span>
- <span data-ttu-id="95723-113">**フルフィルメントの注文** – ユーザーが操作を開始すると、その店舗でフルフィルメントされる注文の一覧を検索して表示するクエリが自動的に実行されます。</span><span class="sxs-lookup"><span data-stu-id="95723-113">**Orders to fulfill** – When a user launches the operation, a query will run automatically to search and display a list of orders that are to be fulfilled by the store.</span></span> <span data-ttu-id="95723-114">これらの注文は、店舗内集荷または店舗出荷に対して構成されており、これらの注文の明細行はまだピッキングまたは梱包されていません。</span><span class="sxs-lookup"><span data-stu-id="95723-114">These orders are configured for in-store pickup or store shipment and the lines of these orders have not yet been picked or packed.</span></span>
- <span data-ttu-id="95723-115">**集荷の注文** – ユーザーが操作を開始すると、ユーザーの現店舗で店舗内集荷用に設定されている注文一覧を検索および表示し、クエリが自動的に実行されます。</span><span class="sxs-lookup"><span data-stu-id="95723-115">**Orders to pick up** – When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for in-store pickup at the user's current store.</span></span>
- <span data-ttu-id="95723-116">**出荷の注文** - ユーザーが操作を開始すると、ユーザーの現店舗から出荷用に設定されている注文一覧を検索および表示し、クエリが自動的に実行されます。</span><span class="sxs-lookup"><span data-stu-id="95723-116">**Orders to ship** - When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for shipment from the user's current store.</span></span>

<span data-ttu-id="95723-117">POS から **注文の取消し** 操作を開始すると、表示が **なし** に設定されている場合、ユーザーは次のいずれかの方法で注文を検索および取得できるようになります。</span><span class="sxs-lookup"><span data-stu-id="95723-117">When launching the **Recall order** operation from POS, if the display is configured to **None**, a user will be able to search and retrieve orders in one of the following ways.</span></span>
- <span data-ttu-id="95723-118">注文バーコードのスキャン。</span><span class="sxs-lookup"><span data-stu-id="95723-118">Scan order barcodes.</span></span> <span data-ttu-id="95723-119">これにより、注文番号、チャンネル参照、およびレシート ID の各フィールドが検索されます。</span><span class="sxs-lookup"><span data-stu-id="95723-119">This will search order number, channel reference, and receipt ID fields for matches.</span></span>
- <span data-ttu-id="95723-120">AppBar で **注文の検索** または **検索およびフィルター** アイコンを選択し、フィルタ条件を満たす注文を見つけるためにフィルタリング機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="95723-120">Select **Search orders** or **Search and filter** icon on the AppBar to use the filtering mechanism to locate orders that meet the filter criteria.</span></span>
- <span data-ttu-id="95723-121">**注文の表示** ドロップダウン メニューから定義済みのフィルターを選択します (フルフィルメントの注文、集荷の注文、出荷の注文)。</span><span class="sxs-lookup"><span data-stu-id="95723-121">Choose from a pre-defined filter from the **Show Orders** drop-down menu (orders to fulfill, orders to pick up, or orders to ship).</span></span>

![RecallOrderMainMenu](media/recallordermain.png)

<span data-ttu-id="95723-123">検索基準を適用すると、アプリケーションにより、一致する販売注文の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="95723-123">After search criteria are applied, the application will display a list of matching sales orders.</span></span>

![RecallOrderDetail](media/orderrecalldetail.png)

<span data-ttu-id="95723-125">ユーザーは、一覧で注文を選択して追加の詳細を表示できます。</span><span class="sxs-lookup"><span data-stu-id="95723-125">A user can select an order on the list to view additional details.</span></span> <span data-ttu-id="95723-126">画面右側の情報パネルには、注文明細行の詳細、配送の詳細、フルフィルメントの詳細を含む、選択した注文の詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="95723-126">The information panel on the right side of the screen displays specifics on the selected order, including order line details, delivery details, and fulfillment details.</span></span>

<span data-ttu-id="95723-127">AppBar から、ユーザーにより工程を選択できます。</span><span class="sxs-lookup"><span data-stu-id="95723-127">From the AppBar, a user can select an operation.</span></span> <span data-ttu-id="95723-128">注文状態によっては、特定操作が有効にならないことがあります。</span><span class="sxs-lookup"><span data-stu-id="95723-128">Depending on the status of the order, certain operations may not be enabled.</span></span>

- <span data-ttu-id="95723-129">**返却** – 選択した顧客注文に関連する 1 つまたは複数の請求書に対して、返却を実行します。</span><span class="sxs-lookup"><span data-stu-id="95723-129">**Return** – Executes a return for one or more invoices related to the selected customer order.</span></span>

- <span data-ttu-id="95723-130">**キャンセル** – 選択した販売注文の完全なキャンセルを発行します。</span><span class="sxs-lookup"><span data-stu-id="95723-130">**Cancel** – Issue a full cancellation of the selected sales order.</span></span>

- <span data-ttu-id="95723-131">**フルフィルメント** – 選択された注文に対して事前にフィルタリングされた注文フルフィルメント ページにユーザーを転送します。</span><span class="sxs-lookup"><span data-stu-id="95723-131">**Fulfill** – Transfers the user to the order fulfillment page, which will be pre-filtered for the selected order.</span></span> <span data-ttu-id="95723-132">選択した注文のユーザー店舗によって、フルフィルメントのために開く注文明細行のみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="95723-132">Only order lines that are open for fulfillment by the user's store for the selected order will be displayed.</span></span>

- <span data-ttu-id="95723-133">**編集** – ユーザーが選択した顧客注文を変更できるようにします。</span><span class="sxs-lookup"><span data-stu-id="95723-133">**Edit** – Allows users to make changes to the selected customer order.</span></span>

- <span data-ttu-id="95723-134">**集荷** – 集荷する製品を選択したり、集荷販売トランザクションを作成したりできように、集荷フローを開始します。</span><span class="sxs-lookup"><span data-stu-id="95723-134">**Pick up** – Launches the pickup flow, which allows the user to choose the products to be picked up and creates the pickup sales transaction.</span></span>
