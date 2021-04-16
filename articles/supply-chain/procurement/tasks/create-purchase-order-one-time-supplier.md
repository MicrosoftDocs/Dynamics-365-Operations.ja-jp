---
title: 一時仕入先に対する発注書の作成
description: この手順では、一時仕入先向けの発注書の作成方法を説明します。
author: kamaybac
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3fe76a3d481c3bc8dd3a3d45eda031df61ece4aa
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812376"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="bb873-103">一時仕入先に対する発注書の作成</span><span class="sxs-lookup"><span data-stu-id="bb873-103">Create a purchase order for a one-time supplier</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bb873-104">この手順では、一時仕入先向けの発注書の作成方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="bb873-104">This procedure shows you how to create a purchase order for a one-time supplier.</span></span> <span data-ttu-id="bb873-105">仕入先は、手動での仕入先アカウントの作成が必要というより、むしろ発注書で自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="bb873-105">The supplier is created automatically with the purchase order, rather than having to create the vendor account manually.</span></span> <span data-ttu-id="bb873-106">通常、発注書は購買担当者が作成します。</span><span class="sxs-lookup"><span data-stu-id="bb873-106">Purchase orders are typically created by a purchasing agent.</span></span> <span data-ttu-id="bb873-107">このガイドで示されている例は、デモ データの会社 USMF で使用できます。</span><span class="sxs-lookup"><span data-stu-id="bb873-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="bb873-108">一時仕入先勘定は [買掛金勘定パラメーター] ページで設定しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="bb873-108">It is a prerequisite that a one-time vendor account has been set up in the Account payable parameters page.</span></span>


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="bb873-109">一時仕入先に対する発注書の作成</span><span class="sxs-lookup"><span data-stu-id="bb873-109">Create a purchase order for a one-time supplier</span></span>
1. <span data-ttu-id="bb873-110">[調達] > [発注書] > [すべての発注書] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bb873-110">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="bb873-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb873-111">Click New.</span></span>
3. <span data-ttu-id="bb873-112">[一時仕入先] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="bb873-112">Select Yes in the One-time supplier field.</span></span>
    * <span data-ttu-id="bb873-113">仕入先は自動的に作成され、発注書に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="bb873-113">A vendor account is automatically created and assigned to the purchase order.</span></span> <span data-ttu-id="bb873-114">仕入先は、買掛金勘定パラメーター ページで一般タブで指定したテンプレートに基づいて作成されます。</span><span class="sxs-lookup"><span data-stu-id="bb873-114">The vendor account is created based on the template that is specified on the General tab in the Accounts payable parameters page.</span></span>  
4. <span data-ttu-id="bb873-115">[名前] フィールドには、仕入先の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="bb873-115">In the Name field, type a name for the supplier.</span></span>
5. <span data-ttu-id="bb873-116">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bb873-116">Click OK.</span></span>
    * <span data-ttu-id="bb873-117">これで他のすべての注文と同様に、発注書を完了し、処理できます。</span><span class="sxs-lookup"><span data-stu-id="bb873-117">The purchase order can now be completed and processed like any other order.</span></span> <span data-ttu-id="bb873-118">この実行方法に関する特殊な属性はありません。</span><span class="sxs-lookup"><span data-stu-id="bb873-118">There are no special characteristics related to how this is done.</span></span> <span data-ttu-id="bb873-119">請求書では、注文に伴い作成し、その後支払いの処理を実行する仕入先のトランザクションの期日が計上されます。</span><span class="sxs-lookup"><span data-stu-id="bb873-119">The invoice will account a due transaction on the vendor account that was created with the order, and payment will then be processed.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]