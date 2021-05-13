---
title: コンフィギュレーション可能な製品の販売注文の作成
description: この手順では、販売注文で製品にコンフィギュレーション テンプレートを適用する方法を示します。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8607de5705354aa58c985fb536f3e1d52acd1f37
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921292"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="6b879-103">コンフィギュレーション可能な製品の販売注文の作成</span><span class="sxs-lookup"><span data-stu-id="6b879-103">Create a sales order for a configurable product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6b879-104">この手順では、販売注文で製品にコンフィギュレーション テンプレートを適用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="6b879-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="6b879-105">この例では、デモ データの会社 USMF の D0006 スピーカー モデルが使用されています。</span><span class="sxs-lookup"><span data-stu-id="6b879-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="6b879-106">通常、販売注文担当者がこの手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="6b879-106">Typically, a sales order processor uses this procedure.</span></span>

## <a name="create-a-sales-order"></a><span data-ttu-id="6b879-107">販売注文の作成</span><span class="sxs-lookup"><span data-stu-id="6b879-107">Create a sales order</span></span>

1. <span data-ttu-id="6b879-108">**販売とマーケティング\>ワークスペース\>販売注文の処理と照会** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b879-108">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="6b879-109">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b879-109">Select **New**.</span></span>
1. <span data-ttu-id="6b879-110">**販売注文** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b879-110">Select **Sales order**.</span></span>
1. <span data-ttu-id="6b879-111">**顧客口座** フィールドで、*US-001* を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b879-111">In the **Customer account** field, select *US-001*.</span></span> 
1. <span data-ttu-id="6b879-112">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b879-112">Select **OK**.</span></span>
1. <span data-ttu-id="6b879-113">**品目番号** フィールドで、*D0006* を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b879-113">In the **Item number** field, select *D0006*.</span></span>
    * <span data-ttu-id="6b879-114">このタスクでは、コンフィギュレーション可能な製品を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b879-114">For this task, you must select a configurable product.</span></span>  
1. <span data-ttu-id="6b879-115">**製品と供給** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b879-115">Select **Product and supply**.</span></span>
1. <span data-ttu-id="6b879-116">**コンフィギュレーション明細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b879-116">Select **Configure line**.</span></span>
    * <span data-ttu-id="6b879-117">選択されたコンフィギュレーションに基づいて価格が変更され、**ケーブルを含める** フィールドが *True* に設定されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="6b879-117">Note that the price has changed, based on the configuration that was selected, and that the **Include cable** field is now set to *True*.</span></span>  
    * <span data-ttu-id="6b879-118">ケーブルに対して選択された既定の価格および設定に注意してください。</span><span class="sxs-lookup"><span data-stu-id="6b879-118">Note the default price and the settings that are selected for the cable.</span></span>  
1. <span data-ttu-id="6b879-119">**読み込みテンプレート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b879-119">Select **Load template**.</span></span>
    * <span data-ttu-id="6b879-120">この例では、事前定義済のコンフィギュレーションを選択するためにどのようにテンプレートを追加できるかを示します。</span><span class="sxs-lookup"><span data-stu-id="6b879-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="6b879-121">この手順をタスク ガイドとして使用し、使用できる他の属性値を確認する場合は、**ロック解除** ボタンを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b879-121">If you're using this procedure as a task guide and want to see the other attribute values that are available, you must select the **Unlock** button.</span></span>  
1. <span data-ttu-id="6b879-122">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b879-122">Select **OK**.</span></span>
1. <span data-ttu-id="6b879-123">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b879-123">Select **OK**.</span></span>
1. <span data-ttu-id="6b879-124">**行の詳細** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="6b879-124">Expand the **Line details** section.</span></span>
1. <span data-ttu-id="6b879-125">**製品** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="6b879-125">Select the **Product** tab.</span></span>
    * <span data-ttu-id="6b879-126">品目のコンフィギュレーションは、製品分析コードの下に一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="6b879-126">The configuration of the item is now listed under the product dimensions.</span></span>  
1. <span data-ttu-id="6b879-127">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6b879-127">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]