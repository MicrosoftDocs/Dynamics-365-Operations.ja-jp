---
title: コンフィギュレーション可能な製品の販売注文の作成
description: この手順では、販売注文で製品にコンフィギュレーション テンプレートを適用する方法を示します。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e69fd2aa04a65d64db4d34f1839a01fb0f8e018
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213196"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="b20b9-103">コンフィギュレーション可能な製品の販売注文の作成</span><span class="sxs-lookup"><span data-stu-id="b20b9-103">Create a sales order for a configurable product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b20b9-104">この手順では、販売注文で製品にコンフィギュレーション テンプレートを適用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b20b9-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="b20b9-105">この例では、デモ データの会社 USMF の D0006 スピーカー モデルが使用されています。</span><span class="sxs-lookup"><span data-stu-id="b20b9-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="b20b9-106">通常、販売注文担当者がこの手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="b20b9-106">Typically, a sales order processor uses this procedure.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="b20b9-107">販売注文の作成</span><span class="sxs-lookup"><span data-stu-id="b20b9-107">Create a sales order</span></span>
1. <span data-ttu-id="b20b9-108">[販売注文の処理と照会] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b20b9-108">Click Sales order processing and inquiry.</span></span>
2. <span data-ttu-id="b20b9-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b20b9-109">Click New.</span></span>
3. <span data-ttu-id="b20b9-110">[販売注文] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b20b9-110">Click Sales order.</span></span>
4. <span data-ttu-id="b20b9-111">[顧客口座] フィールドで [US-001] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b20b9-111">In the Customer account field, select US-001.</span></span> 
5. <span data-ttu-id="b20b9-112">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b20b9-112">Click OK.</span></span>
6. <span data-ttu-id="b20b9-113">[品目番号] フィールドで D0006 を選択します。</span><span class="sxs-lookup"><span data-stu-id="b20b9-113">In the Item number field, select D0006.</span></span>
    * <span data-ttu-id="b20b9-114">このタスクでは、コンフィギュレーション可能な製品を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b20b9-114">For this task, you must select a configurable product.</span></span>  
7. <span data-ttu-id="b20b9-115">[製品と供給] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b20b9-115">Click Product and supply.</span></span>
8. <span data-ttu-id="b20b9-116">[コンフィギュレーション明細] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b20b9-116">Click Configure line.</span></span>
    * <span data-ttu-id="b20b9-117">選択されたコンフィギュレーションに基づいて価格が変更され、[ケーブルを含める] フィールドが True に設定されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b20b9-117">Note that the price has changed, based on the configuration that was selected, and that the Include cable field is now set to True.</span></span>  
    * <span data-ttu-id="b20b9-118">ケーブルに対して選択された既定の価格および設定に注意してください。</span><span class="sxs-lookup"><span data-stu-id="b20b9-118">Note the default price and the settings that are selected for the cable.</span></span>  
9. <span data-ttu-id="b20b9-119">[テンプレートの読み込み] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b20b9-119">Click Load template.</span></span>
    * <span data-ttu-id="b20b9-120">この例では、事前定義済のコンフィギュレーションを選択するためにどのようにテンプレートを追加できるかを示します。</span><span class="sxs-lookup"><span data-stu-id="b20b9-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="b20b9-121">この手順をタスク ガイドとして使用し、使用できる他の属性値を確認する場合は、[ロック解除] ボタンをクリックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b20b9-121">If you're using this procedure as a task guide and want to see the other attribute values that are available, you must click the Unlock button.</span></span>  
10. <span data-ttu-id="b20b9-122">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b20b9-122">Click OK.</span></span>
11. <span data-ttu-id="b20b9-123">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b20b9-123">Click OK.</span></span>
12. <span data-ttu-id="b20b9-124">[明細行の詳細] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="b20b9-124">Expand the Line details section.</span></span>
13. <span data-ttu-id="b20b9-125">[製品] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b20b9-125">Click the Product tab.</span></span>
    * <span data-ttu-id="b20b9-126">品目のコンフィギュレーションは、製品分析コードの下に一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="b20b9-126">The configuration of the item is now listed under the product dimensions.</span></span>  
14. <span data-ttu-id="b20b9-127">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b20b9-127">Close the page.</span></span>

## <a name="select-the-product-configuration"></a><span data-ttu-id="b20b9-128">製品コンフィギュレーションの選択</span><span class="sxs-lookup"><span data-stu-id="b20b9-128">Select the product configuration</span></span>

