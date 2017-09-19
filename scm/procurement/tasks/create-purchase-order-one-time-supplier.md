--- 
title: "一時仕入先に対する発注書の作成"
description: "この手順では、一時仕入先向けの発注書の作成方法を説明します。"
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2d4dabaf6e1d79cbd626294ee4e327f2725a5e43
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="e41df-103">一時仕入先に対する発注書の作成</span><span class="sxs-lookup"><span data-stu-id="e41df-103">Create a purchase order for a one-time supplier</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e41df-104">この手順では、一時仕入先向けの発注書の作成方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="e41df-104">This procedure shows you how to create a purchase order for a one-time supplier.</span></span> <span data-ttu-id="e41df-105">仕入先は、手動での仕入先アカウントの作成が必要というより、むしろ発注書で自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="e41df-105">The supplier is created automatically with the purchase order, rather than having to create the vendor account manually.</span></span> <span data-ttu-id="e41df-106">通常、発注書は購買担当者が作成します。</span><span class="sxs-lookup"><span data-stu-id="e41df-106">Purchase orders are typically created by a purchasing agent.</span></span> <span data-ttu-id="e41df-107">このガイドで示されている例は、デモ データの会社 USMF で使用できます。</span><span class="sxs-lookup"><span data-stu-id="e41df-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="e41df-108">一時仕入先勘定は [買掛金勘定パラメーター] ページで設定しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="e41df-108">It is a prerequisite that a one-time vendor account has been set up in the Account payable parameters page.</span></span>


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="e41df-109">一時仕入先に対する発注書の作成</span><span class="sxs-lookup"><span data-stu-id="e41df-109">Create a purchase order for a one-time supplier</span></span>
1. <span data-ttu-id="e41df-110">[調達] > [発注書] > [すべての発注書] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e41df-110">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="e41df-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e41df-111">Click New.</span></span>
3. <span data-ttu-id="e41df-112">[一時仕入先] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e41df-112">Select Yes in the One-time supplier field.</span></span>
    * <span data-ttu-id="e41df-113">仕入先は自動的に作成され、発注書に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="e41df-113">A vendor account is automatically created and assigned to the purchase order.</span></span> <span data-ttu-id="e41df-114">仕入先は、買掛金勘定パラメーター ページで一般タブで指定したテンプレートに基づいて作成されます。</span><span class="sxs-lookup"><span data-stu-id="e41df-114">The vendor account is created based on the template that is specified on the General tab in the Accounts payable parameters page.</span></span>  
4. <span data-ttu-id="e41df-115">[名前] フィールドには、仕入先の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="e41df-115">In the Name field, type a name for the supplier.</span></span>
5. <span data-ttu-id="e41df-116">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e41df-116">Click OK.</span></span>
    * <span data-ttu-id="e41df-117">これで他のすべての注文と同様に、発注書を完了し、処理できます。</span><span class="sxs-lookup"><span data-stu-id="e41df-117">The purchase order can now be completed and processed like any other order.</span></span> <span data-ttu-id="e41df-118">この実行方法に関する特殊な属性はありません。</span><span class="sxs-lookup"><span data-stu-id="e41df-118">There are no special characteristics related to how this is done.</span></span> <span data-ttu-id="e41df-119">請求書では、注文に伴い作成し、その後支払いの処理を実行する仕入先のトランザクションの期日が計上されます。</span><span class="sxs-lookup"><span data-stu-id="e41df-119">The invoice will account a due transaction on the vendor account that was created with the order, and payment will then be processed.</span></span> <span data-ttu-id="e41df-120">これが完了すると、仕入先を削除できます。</span><span class="sxs-lookup"><span data-stu-id="e41df-120">When this is completed, the vendor account can be deleted.</span></span> <span data-ttu-id="e41df-121">これは通常、買掛金勘定部門により実行されます。</span><span class="sxs-lookup"><span data-stu-id="e41df-121">This is typically done by the accounts payable department.</span></span>  

