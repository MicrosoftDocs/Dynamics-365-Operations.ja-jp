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
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: f34a0a3cebcf5a374e8d6b3857af6b0dfa619e04
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="extend-a-retail-server-odata-controller"></a>Retail Server OData コントローラーの拡張

[!include [banner](../includes/banner.md)]

この記事では、CustomController クラスを拡張するコードを説明します。

コントローラーは、commerce エンティティ タイプの作成、読み取り、更新、および削除 (CRUD) の動作とアクションをコントロールする commerce エンティティのマッピングです。 各コマース エンティティには、対応するコントローラーが必要です。 Microsoft Dynamics 365 for Retail に含まれるコントローラーを拡張して、業務上の要件を満たすように新しい業務処理を追加することができます。 既存のコント ローラーを拡張するには、既存のコントローラー クラスを拡張する新しいクラスを定義する必要があります。 新しいクラスで、**ExtendedController** 属性を使用して、新しいクラスが既存のコントローラーを拡張していること、および新しいクラスがどのコントローラーを拡張するかを示します。 この例では、新しいクラスが**顧客**エンティティ タイプのコントローラーを拡張します。 各エンティティ タイプは、1 つのコント ローラーのみに関連付けられます。 既存のコント ローラーを上書きする新しいコント ローラーを作成するときは、**ExtendedController** 属性を持つ新しいコント ローラーが元のコントローラーの代わりに使用されます。 次の例では、**ExtendedCustomersController** クラスは **CustomersController** クラスを拡張して、**顧客**エンティティ タイプのエンティティ タイプとキー フィールドをパラメーターとして受け取ります。 サンプル コードは、Retail ソフトウェアの開発キット (SDK) 内のこのトピックから見つけることができます。

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




