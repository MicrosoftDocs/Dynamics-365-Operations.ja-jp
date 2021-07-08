---
title: グローバル在庫会計元帳
description: このトピックでは、通貨、カレンダー、規則、および法人との関連の組み合わせによって定義されるグローバル在庫会計元帳について説明します。
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea3434675aa3b7f2304be93ef9b489747994fa9d
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273184"
---
# <a name="global-inventory-accounting-ledger"></a><span data-ttu-id="41df2-103">グローバル在庫会計元帳</span><span class="sxs-lookup"><span data-stu-id="41df2-103">Global Inventory Accounting ledger</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="41df2-104">グローバル在庫会計には、独自の一連の元帳があります。</span><span class="sxs-lookup"><span data-stu-id="41df2-104">Global Inventory Accounting has its own set of ledgers.</span></span> <span data-ttu-id="41df2-105">必要に応じて、関連する法人に対して在庫関連のトランザクションが処理されるたびに、システムは任意の数のグローバル在庫会計元帳で、そのトランザクションを計上することができます。</span><span class="sxs-lookup"><span data-stu-id="41df2-105">Each time an inventory-related transaction is processed for a relevant legal entity, the system can account for that transaction in any number of Global Inventory Accounting ledgers, as required.</span></span>

<span data-ttu-id="41df2-106">元帳は借方と貸方で登録されます。</span><span class="sxs-lookup"><span data-stu-id="41df2-106">A ledger is a register of debit and credit measures.</span></span> <span data-ttu-id="41df2-107">これらの方法は、原価要素および補助元帳を使用して分類されます。</span><span class="sxs-lookup"><span data-stu-id="41df2-107">These measures are classified by using cost elements and subledger accounts.</span></span> <span data-ttu-id="41df2-108">グローバル在庫会計元帳は、通貨、カレンダー、規則、および法人との関連の組み合わせによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="41df2-108">A Global Inventory Accounting ledger is defined by its combination of a currency, a calendar, a convention, and an association with a legal entity.</span></span>

<span data-ttu-id="41df2-109">グローバル在庫会計元帳を設定するには、**グローバル在庫会計 \> 設定 \> グローバル在庫会計元帳** に移動します。</span><span class="sxs-lookup"><span data-stu-id="41df2-109">To set up your Global Inventory Accounting ledgers, go to **Global inventory accounting \> Setup \> Global inventory accounting ledgers**.</span></span> <span data-ttu-id="41df2-110">各元帳に、次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="41df2-110">For each ledger, set the following fields:</span></span>

- <span data-ttu-id="41df2-111">**名前** – 元帳の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="41df2-111">**Name** – Enter the name of the ledger.</span></span>
- <span data-ttu-id="41df2-112">**説明** – 元帳の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="41df2-112">**Description** – Enter a description of the ledger.</span></span>
- <span data-ttu-id="41df2-113">**会計カレンダー** – 元帳の会計カレンダーを指定します。</span><span class="sxs-lookup"><span data-stu-id="41df2-113">**Fiscal calendar** – Specify the fiscal calendar for the ledger.</span></span>
- <span data-ttu-id="41df2-114">**通貨と為替レート タイプ** – このクイックタブのフィールドを使用して、元帳が使用する会計通貨と為替レート タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="41df2-114">**Currency and exchange rate type** – Use the fields on this FastTab to select the accounting currency that the ledger uses, and the exchange rate type.</span></span> <span data-ttu-id="41df2-115">選択する通貨が、法人が使用する通貨とは異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="41df2-115">The currency that you select can differ from the currency that the legal entity uses.</span></span> <span data-ttu-id="41df2-116">グローバル在庫会計では、ユーザーは必要な数だけ原価元帳を定義できます。</span><span class="sxs-lookup"><span data-stu-id="41df2-116">In Global Inventory Accounting, users can define as many costing ledgers as they require.</span></span> <span data-ttu-id="41df2-117">グローバル在庫会計は、複数の通貨および複数の評価での在庫会計をサポートします。</span><span class="sxs-lookup"><span data-stu-id="41df2-117">Global Inventory Accounting supports inventory accounting in multiple currencies and in multiple valuations.</span></span> <span data-ttu-id="41df2-118">次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="41df2-118">Set the following fields:</span></span>

    - <span data-ttu-id="41df2-119">**通貨** – 在庫関連の値を管理する原価通貨を選択します。</span><span class="sxs-lookup"><span data-stu-id="41df2-119">**Currency** – Select the costing currency that inventory-related values are maintained in.</span></span> <span data-ttu-id="41df2-120">これらの値には、在庫金額、売却済商品の原価、輸送中の在庫、およびすべての種類の差異が含まれます。</span><span class="sxs-lookup"><span data-stu-id="41df2-120">These values include the inventory value, cost of goods sold, inventory in transit, and all kinds of variance.</span></span>
    - <span data-ttu-id="41df2-121">**為替レート タイプ** – トランザクション通貨および品目の標準原価を原価通貨に換算するためにシステムが使用する為替レートを選択します。</span><span class="sxs-lookup"><span data-stu-id="41df2-121">**Exchange rate type** – Select the exchange rate that the system should use to convert the transaction amount in the transaction currency and the standard cost of the items into the costing currency.</span></span>

- <span data-ttu-id="41df2-122">**規則名** – 規則を指定します。</span><span class="sxs-lookup"><span data-stu-id="41df2-122">**Convention name** – Specify a convention.</span></span> <span data-ttu-id="41df2-123">規則は、この元帳で原価を計上する方法を確立するポリシーのコレクションです。</span><span class="sxs-lookup"><span data-stu-id="41df2-123">A convention is a collection of policies that establish how costs will be accounted in this ledger.</span></span>
- <span data-ttu-id="41df2-124">**法人** – 元帳は、選択した法人に転記されるドキュメントを計上します。</span><span class="sxs-lookup"><span data-stu-id="41df2-124">**Legal entity** – The ledger will account the documents that are posted to the selected legal entity.</span></span>
- <span data-ttu-id="41df2-125">**プライミング** – 元帳が作成される前に作成された在庫トランザクションを、元帳の通貨や規則に従って処理するかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="41df2-125">**Priming** – Select whether inventory transactions that were created before the ledger was created should be processed according to the currency and convention in the ledger.</span></span> <span data-ttu-id="41df2-126">次の値からいずれか 1 つを選択します。</span><span class="sxs-lookup"><span data-stu-id="41df2-126">Select one of the following values:</span></span>

    - <span data-ttu-id="41df2-127">**有効化** – 元帳は、元帳が作成される前に作成されたトランザクションを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="41df2-127">**Activated** – The ledger should process transactions that were created before the ledger was created.</span></span>
    - <span data-ttu-id="41df2-128">**無効化** – 元帳は、元帳が作成された後に作成されるトランザクションだけを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="41df2-128">**Deactivated** – The ledger should process only transactions that are created after the ledger was created.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="41df2-129">新しいドキュメントを入力した後に戻って来てこのフィールドを設定することは **できません**。</span><span class="sxs-lookup"><span data-stu-id="41df2-129">You will **not** be able to come back and set this field after you enter new documents.</span></span>

- <span data-ttu-id="41df2-130">**状態** – システムは新しく作成された元帳の状態を、自動的に *準備* に設定します。</span><span class="sxs-lookup"><span data-stu-id="41df2-130">**Status** – The system automatically sets the status of newly created ledgers to *Prepare*.</span></span>
