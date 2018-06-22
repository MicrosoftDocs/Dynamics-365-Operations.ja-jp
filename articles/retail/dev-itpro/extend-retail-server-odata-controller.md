---
title: "Retail Server OData コントローラーの拡張"
description: "この記事では、CustomController クラスを拡張するコードを説明します。"
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 31681
ms.assetid: c39a34b5-3fce-446f-877b-0aa41817ef25
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e23a6f570a6753fc0a05f4b68a2b5bb6886b6bc8
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="extend-a-retail-server-odata-controller"></a><span data-ttu-id="b9ce4-103">Retail Server OData コントローラーの拡張</span><span class="sxs-lookup"><span data-stu-id="b9ce4-103">Extend a Retail Server OData controller</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9ce4-104">この記事では、CustomController クラスを拡張するコードを説明します。</span><span class="sxs-lookup"><span data-stu-id="b9ce4-104">This article provides code that extends the CustomController class.</span></span>

<span data-ttu-id="b9ce4-105">コントローラーは、commerce エンティティ タイプの作成、読み取り、更新、および削除 (CRUD) の動作とアクションをコントロールする commerce エンティティのマッピングです。</span><span class="sxs-lookup"><span data-stu-id="b9ce4-105">A controller is a mapping for a commerce entity that controls create, read, update, and delete (CRUD) behaviors and actions for a commerce entity type.</span></span> <span data-ttu-id="b9ce4-106">各コマース エンティティには、対応するコントローラーが必要です。</span><span class="sxs-lookup"><span data-stu-id="b9ce4-106">Each commerce entity must have a corresponding controller.</span></span> <span data-ttu-id="b9ce4-107">Microsoft Dynamics 365 for Retail に含まれるコントローラーを拡張して、業務上の要件を満たすように新しい業務処理を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="b9ce4-107">You can extend a controller that is included with Microsoft Dynamics 365 for Retail to add new business actions that meet your business requirement.</span></span> <span data-ttu-id="b9ce4-108">既存のコント ローラーを拡張するには、既存のコントローラー クラスを拡張する新しいクラスを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9ce4-108">To extend an existing controller, you must define a new class that extends an existing controller class.</span></span> <span data-ttu-id="b9ce4-109">新しいクラスで、**ExtendedController** 属性を使用して、新しいクラスが既存のコントローラーを拡張していること、および新しいクラスがどのコントローラーを拡張するかを示します。</span><span class="sxs-lookup"><span data-stu-id="b9ce4-109">In the new class, you use the **ExtendedController** attribute to indicate that the new class extends an existing controller, and to indicate which controller the new class extends.</span></span> <span data-ttu-id="b9ce4-110">この例では、新しいクラスが**顧客**エンティティ タイプのコントローラーを拡張します。</span><span class="sxs-lookup"><span data-stu-id="b9ce4-110">In this example, the new class extends the controller for the **Customer** entity type.</span></span> <span data-ttu-id="b9ce4-111">各エンティティ タイプは、1 つのコント ローラーのみに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="b9ce4-111">Each entity type is associated with only one controller.</span></span> <span data-ttu-id="b9ce4-112">既存のコント ローラーを上書きする新しいコント ローラーを作成するときは、**ExtendedController** 属性を持つ新しいコント ローラーが元のコントローラーの代わりに使用されます。</span><span class="sxs-lookup"><span data-stu-id="b9ce4-112">When you create a new controller that overrides an existing controller, the new controller that has the **ExtendedController** attribute is used instead of the original controller.</span></span> <span data-ttu-id="b9ce4-113">次の例では、**ExtendedCustomersController** クラスは **CustomersController** クラスを拡張して、**顧客**エンティティ タイプのエンティティ タイプとキー フィールドをパラメーターとして受け取ります。</span><span class="sxs-lookup"><span data-stu-id="b9ce4-113">In the following example, the **ExtendedCustomersController** class extends the **CustomersController** class, and takes the entity type and the key field of the **Customer** entity type as parameters.</span></span> <span data-ttu-id="b9ce4-114">サンプル コードは、Retail ソフトウェアの開発キット (SDK) 内のこのトピックから見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="b9ce4-114">You can find the sample code from this topic in the Retail software development kit (SDK).</span></span>

    namespace Microsoft.Dynamics.RetailServer.ExtensionSamples
    {
        using System;
        using System.Collections.Generic;
        using System.Linq;
        using System.Runtime.InteropServices;
        using Microsoft.Dynamics.Commerce.Runtime.DataModel;
        using Microsoft.Dynamics.Retail.StoreServerServiceLibrary;
        using Microsoft.Dynamics.Retail.StoreServerServiceLibrary.ODataControllers;
        [ExtendedController("Customers")]
        [ComVisible(false)]
        public class ExtendedCustomersController : CustomersController
        {
            public override IQueryable<Customer> Get()
            {
                List<Customer> customers = new List<Customer>();
                for (int i = 0; i < 10; i++)
                {
                    var customer = new Customer();
                    customer.AccountNumber = "customer" + i;
                    customer.Name = "Name" + i;
                    customers.Add(customer);
                }
                return customers.AsQueryable();
            }
        }
    }




