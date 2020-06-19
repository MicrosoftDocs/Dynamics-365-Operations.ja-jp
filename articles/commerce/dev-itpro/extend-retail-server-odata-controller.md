---
title: Commerce Scale Unit OData コントローラーの拡張
description: このトピックでは、CustomController クラスを拡張するコードを説明します。
author: kfend
manager: AnnBe
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 31681
ms.assetid: c39a34b5-3fce-446f-877b-0aa41817ef25
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 56a3e7f659b6c38249d7c580a1958a6ff0afbe7b
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426325"
---
# <a name="extend-a-commerce-scale-unit-odata-controller"></a>Commerce Scale Unit OData コントローラーの拡張

[!include [banner](../includes/banner.md)]

このトピックでは、CustomersController クラスを拡張するコードを説明します。

コントローラーは、commerce エンティティ タイプの作成、読み取り、更新、および削除 (CRUD) の動作とアクションをコントロールする commerce エンティティのマッピングです。 各コマース エンティティには、対応するコントローラーが必要です。 Microsoft Dynamics 365 Commerce に含まれるコントローラーを拡張して、業務上の要件を満たすように新しい業務処理を追加することができます。 

既存のコント ローラーを拡張するには、既存のコントローラー クラスを拡張する新しいクラスを定義する必要があります。 既存のコント ローラーを拡張する新しいコント ローラーを作成するときは、新しいコントローラーは拡張されるコントローラーで新しいメソッドを作成するか既存のメソッドをオーバーライドできます。 オーバーライドされていない拡張コントローラー内のすべてのメソッドは、引き続き同じように機能します。 この例では、**ExtendedCustomersController** クラスは **CustomersController** クラスを拡張し、**CustomersController**クラスは **Customers** エンティティ タイプのコントローラーです。  

Commerce Scale Unit Web.config ファイルの **extensionComposition** セクションを更新する必要があります。 詳細については、[Commerce Runtime CRT および Retail Server の拡張機能](commerce-runtime-extensibility.md) を参照してください。 サンプル コードは、Retail ソフトウェアの開発キット (SDK) 内のこのトピックから見つけることができます。 

```csharp
using System.Web.Http;
using System.Web.OData;
using Microsoft.Dynamics.Commerce.Runtime;
using Microsoft.Dynamics.Commerce.Runtime.DataModel;
using Microsoft.Dynamics.Retail.RetailServerLibrary;
using Microsoft.Dynamics.Retail.RetailServerLibrary.ODataControllers;
    
namespace Microsoft.Dynamics.RetailServer.ExtensionSamples
{
    class ExtendedCustomersController : CustomersController
    {
        [CommerceAuthorization(new string[] { "Employee", "Application" })]
        [HttpPost]
        public override PageResult<GlobalCustomer> Search(ODataActionParameters parameters)
        {
            ThrowIf.Null<ODataActionParameters>(parameters, nameof(parameters));
            parameters["customerSearchCriteria"] += " My custom criteria";
            return base.Search(parameters);
        }
    }
}
```
