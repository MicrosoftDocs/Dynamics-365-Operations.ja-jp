---
title: 小売店舗トランザクション用トリクル フィードベースの注文作成
description: このトピックでは、Microsoft Dynamics 365 Commerce の店舗トランザクションに対するトリクル フィードベースの注文作成について説明します。
author: josaw1
manager: AnnBe
ms.date: 09/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 79f99b9b401de3e3bcca6ec5a13a3b4f7bad6f8c
ms.sourcegitcommit: 5b620f670ac0f403a0fdcdeb9c3f970b163191ee
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2020
ms.locfileid: "3766739"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a><span data-ttu-id="271cd-103">小売店舗トランザクション用トリクル フィードベースの注文作成</span><span class="sxs-lookup"><span data-stu-id="271cd-103">Trickle feed-based order creation for retail store transactions</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="271cd-104">Dynamics 365 Retail バージョン 10.0.4 およびそれ以前のバージョンでは、明細書の転記は営業終了操作で、すべてのトランザクションは 1 日の終わりに帳簿に転記されます。</span><span class="sxs-lookup"><span data-stu-id="271cd-104">In Dynamics 365 Retail versions 10.0.4 and earlier, statement posting is an end-of-day operation and all transactions are posted in the books at the end of the day.</span></span> <span data-ttu-id="271cd-105">その後、限られた時間枠で大規模なトランザクションを処理する必要があります。その結果、負荷、ロック、明細書の転記エラーなどが発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="271cd-105">Large transactions must then be processed in a limited time window, sometimes resulting in load and locks and statement posting failures.</span></span> <span data-ttu-id="271cd-106">小売業者は、1 日を通して帳簿にある収益や支払も識別できません。</span><span class="sxs-lookup"><span data-stu-id="271cd-106">Retailers also can't recognize revenue and payments in their books throughout the day.</span></span>

<span data-ttu-id="271cd-107">Retail バージョン 10.0.5 に導入されたトリクル フィードベースの注文作成を使用すると、トランザクションは 1 日を通して処理されます。そして、支払/入金の財務調整およびその他の現金管理トランザクションのみが 1 日の最後に処理されます。</span><span class="sxs-lookup"><span data-stu-id="271cd-107">With trickle feed-based order creation introduced in Retail version 10.0.5, transactions are processed throughout the day, and only the financial reconciliation of tenders and other cash management transactions are processed at the end of the day.</span></span> <span data-ttu-id="271cd-108">この機能により、1 日の販売注文、請求書、支払の作成の負荷が分割され、より的確な業績が得られると共に、帳簿の収益や支払をほぼリアルタイムで認識することができます。</span><span class="sxs-lookup"><span data-stu-id="271cd-108">This functionality splits the load of creating sales orders, invoices, and payments throughout the day, providing better perceived performance and the ability to recognize revenue and payments in the books in near real-time.</span></span> 


## <a name="how-to-use-trickle-feed-based-posting"></a><span data-ttu-id="271cd-109">トリクル フィードベースの転記の使用方法</span><span class="sxs-lookup"><span data-stu-id="271cd-109">How to use trickle feed-based posting</span></span>
  
1. <span data-ttu-id="271cd-110">小売トランザクションのトリクル フィードベースの転記を有効にするには、機能管理を使用して **小売明細書 - トリクル フィード** という機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="271cd-110">To enable trickle feed-based posting of retail transactions, enable the feature named **Retail statements - Trickle feed** using Feature management.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="271cd-111">この機能を有効にする前に、転記を待機している保留中の明細書がないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="271cd-111">Before you enable the feature, make sure that no pending statements are waiting to be posted.</span></span>

2. <span data-ttu-id="271cd-112">現在の明細書ドキュメントは、2 つのタイプ、トランザクション明細書と財務諸表に分割されます。</span><span class="sxs-lookup"><span data-stu-id="271cd-112">The current statement document will be split into two types: transactional statement and financial statement.</span></span>

      - <span data-ttu-id="271cd-113">トランザクション明細書は、すべての転記されていない有効なトランザクションを取得し、販売注文、売上請求書、支払および割引仕訳帳、収入経費トランザクションを設定した頻度で作成します。</span><span class="sxs-lookup"><span data-stu-id="271cd-113">The transactional statement will pick up all unposted and validated transactions and create sales orders, sales invoices, payment and discount journals, and income-expense transactions at the cadence that you configure.</span></span> <span data-ttu-id="271cd-114">このプロセスを高頻度で実行できるようにコンフィギュレーションして、トランザクションが P-ジョブを介して Headquarters にアップロードされる際にドキュメントが作成されるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="271cd-114">You should configure this process to run at a high frequency so that documents are created when the transactions are uploaded into Headquarters through the P-job.</span></span> <span data-ttu-id="271cd-115">販売注文と売上請求書が既に作成されているトランザクション明細書では、**在庫の転記** バッチ ジョブをコンフィギュレーションする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="271cd-115">With the transactional statement that already creates sales orders and sales invoices, there is no real need to configure the **Post inventory** batch job.</span></span> <span data-ttu-id="271cd-116">ただし、特定の業務要件を満たすために使用することはできます。</span><span class="sxs-lookup"><span data-stu-id="271cd-116">However, you can still use it to meet specific business requirements that you may have.</span></span>  
      
     - <span data-ttu-id="271cd-117">財務諸表は、その日の終わりに作成するように設計されており、**シフト** の決算方法のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="271cd-117">The financial statement is designed to be created at the end of the day and only supports the closing method of **Shift**.</span></span> <span data-ttu-id="271cd-118">この明細書は財務調整に限定され、他の現金管理トランザクションの仕訳帳と一緒に、異なる支払/入金の計算金額とトランザクション金額の差額が記載された仕訳帳のみが作成されます。</span><span class="sxs-lookup"><span data-stu-id="271cd-118">This statement will be limited to financial reconciliation and will only create the journals for the difference amounts between counted amount and transaction amount for the different tenders, along with journals for other cash management transactions.</span></span>   

3. <span data-ttu-id="271cd-119">トランザクション明細書を計算するには、**Retail と Commerce > Retail および Commerce IT > POS 転記 > バッチ内のトランザクション明細書の計算** へ移動します。</span><span class="sxs-lookup"><span data-stu-id="271cd-119">To calculate the transactional statement, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate transactional statements in batch**.</span></span> <span data-ttu-id="271cd-120">バッチ内のトランザクション明細書を転記するには、**Retail と Commerce > Retail および Commerce IT > POS 転記 > バッチ内のトランザクション明細書の転記** へ移動します。</span><span class="sxs-lookup"><span data-stu-id="271cd-120">To post the transactional statements in batch, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Post transactional statements in batch**.</span></span>

4. <span data-ttu-id="271cd-121">トランザクション財務諸表を計算するには、**Retail と Commerce > Retail および Commerce IT > POS 転記 > バッチ内の財務諸表の計算** へ移動します。</span><span class="sxs-lookup"><span data-stu-id="271cd-121">To calculate the financial statement, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate financial statements in batch**.</span></span> <span data-ttu-id="271cd-122">バッチ内の財務諸表を転記するには、**Retail と Commerce > Retail および Commerce IT > POS 転記 > バッチ内の財務諸表の転記** へ移動します。</span><span class="sxs-lookup"><span data-stu-id="271cd-122">To post the financial statements in batch, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Post financial statements in batch**.</span></span>

> [!NOTE]
> <span data-ttu-id="271cd-123">メニュー項目、**Retail と Commerce > Retail および Commerce IT > POS転記 > バッチ内の明細書の計算** と **Retail と Commerce > Retail および Commerce IT > POS 転記** は、この新しい機能により無効になります。</span><span class="sxs-lookup"><span data-stu-id="271cd-123">The menu items **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate statements in batch** and **Retail and Commerce > Retail and Commerce IT > POS Posting > Post statements in batch** are removed with this new feature.</span></span>

<span data-ttu-id="271cd-124">トランザクション タイプおよび財務諸表タイプは、手動で作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="271cd-124">Alternately, transactional and financial statement types can be created manually.</span></span> <span data-ttu-id="271cd-125">**Retail と Commerce > チャンネル > 店舗** に移動して、**明細書** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="271cd-125">Go to **Retail and Commerce > Channels > Stores** and click **Statements**.</span></span> <span data-ttu-id="271cd-126">**新規** をクリックし、作成する明細書のタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="271cd-126">Click **New** and then choose the type of statement that you want to create.</span></span> <span data-ttu-id="271cd-127">**明細書** ページのフィールドとそのページの **明細書グループ** にあるアクションは、選択した明細書タイプに基づいて、関連するデータおよびアクションを表示します。</span><span class="sxs-lookup"><span data-stu-id="271cd-127">Fields on the **Statements** page and actions under the **Statement group** of the page will show relevant data and actions based on the selected statement type.</span></span>
