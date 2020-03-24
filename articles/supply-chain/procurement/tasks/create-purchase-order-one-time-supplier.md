---
title: 一時仕入先に対する発注書の作成
description: この手順では、一時仕入先向けの発注書の作成方法を説明します。
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e2fa54ff598bb6a09bbcc483995a6e1a3f4286b3
ms.sourcegitcommit: 16612a632aad9d390f8d80d3fc1f766585b2911e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/04/2020
ms.locfileid: "3098079"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="5d84a-103">一時仕入先に対する発注書の作成</span><span class="sxs-lookup"><span data-stu-id="5d84a-103">Create a purchase order for a one-time supplier</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5d84a-104">この手順では、一時仕入先向けの発注書の作成方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="5d84a-104">This procedure shows you how to create a purchase order for a one-time supplier.</span></span> <span data-ttu-id="5d84a-105">仕入先は、手動での仕入先アカウントの作成が必要というより、むしろ発注書で自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="5d84a-105">The supplier is created automatically with the purchase order, rather than having to create the vendor account manually.</span></span> <span data-ttu-id="5d84a-106">通常、発注書は購買担当者が作成します。</span><span class="sxs-lookup"><span data-stu-id="5d84a-106">Purchase orders are typically created by a purchasing agent.</span></span> <span data-ttu-id="5d84a-107">このガイドで示されている例は、デモ データの会社 USMF で使用できます。</span><span class="sxs-lookup"><span data-stu-id="5d84a-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="5d84a-108">一時仕入先勘定は [買掛金勘定パラメーター] ページで設定しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d84a-108">It is a prerequisite that a one-time vendor account has been set up in the Account payable parameters page.</span></span>


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="5d84a-109">一時仕入先に対する発注書の作成</span><span class="sxs-lookup"><span data-stu-id="5d84a-109">Create a purchase order for a one-time supplier</span></span>
1. <span data-ttu-id="5d84a-110">[調達] > [発注書] > [すべての発注書] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5d84a-110">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="5d84a-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d84a-111">Click New.</span></span>
3. <span data-ttu-id="5d84a-112">[一時仕入先] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="5d84a-112">Select Yes in the One-time supplier field.</span></span>
    * <span data-ttu-id="5d84a-113">仕入先は自動的に作成され、発注書に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="5d84a-113">A vendor account is automatically created and assigned to the purchase order.</span></span> <span data-ttu-id="5d84a-114">仕入先は、買掛金勘定パラメーター ページで一般タブで指定したテンプレートに基づいて作成されます。</span><span class="sxs-lookup"><span data-stu-id="5d84a-114">The vendor account is created based on the template that is specified on the General tab in the Accounts payable parameters page.</span></span>  
4. <span data-ttu-id="5d84a-115">[名前] フィールドには、仕入先の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="5d84a-115">In the Name field, type a name for the supplier.</span></span>
5. <span data-ttu-id="5d84a-116">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d84a-116">Click OK.</span></span>
    * <span data-ttu-id="5d84a-117">これで他のすべての注文と同様に、発注書を完了し、処理できます。</span><span class="sxs-lookup"><span data-stu-id="5d84a-117">The purchase order can now be completed and processed like any other order.</span></span> <span data-ttu-id="5d84a-118">この実行方法に関する特殊な属性はありません。</span><span class="sxs-lookup"><span data-stu-id="5d84a-118">There are no special characteristics related to how this is done.</span></span> <span data-ttu-id="5d84a-119">請求書では、注文に伴い作成し、その後支払いの処理を実行する仕入先のトランザクションの期日が計上されます。</span><span class="sxs-lookup"><span data-stu-id="5d84a-119">The invoice will account a due transaction on the vendor account that was created with the order, and payment will then be processed.</span></span>

