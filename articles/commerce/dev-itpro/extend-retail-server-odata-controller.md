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
# <a name="extend-a-commerce-scale-unit-odata-controller"></a><span data-ttu-id="6ecdc-103">Commerce Scale Unit OData コントローラーの拡張</span><span class="sxs-lookup"><span data-stu-id="6ecdc-103">Extend a Commerce Scale Unit OData controller</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6ecdc-104">このトピックでは、CustomersController クラスを拡張するコードを説明します。</span><span class="sxs-lookup"><span data-stu-id="6ecdc-104">This topic provides code that extends the CustomersController class.</span></span>

<span data-ttu-id="6ecdc-105">コントローラーは、commerce エンティティ タイプの作成、読み取り、更新、および削除 (CRUD) の動作とアクションをコントロールする commerce エンティティのマッピングです。</span><span class="sxs-lookup"><span data-stu-id="6ecdc-105">A controller is a mapping for a commerce entity that controls create, read, update, and delete (CRUD) behaviors and actions for a commerce entity type.</span></span> <span data-ttu-id="6ecdc-106">各コマース エンティティには、対応するコントローラーが必要です。</span><span class="sxs-lookup"><span data-stu-id="6ecdc-106">Each commerce entity must have a corresponding controller.</span></span> <span data-ttu-id="6ecdc-107">Microsoft Dynamics 365 Commerce に含まれるコントローラーを拡張して、業務上の要件を満たすように新しい業務処理を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="6ecdc-107">You can extend a controller that is included with Microsoft Dynamics 365 Commerce to add new business actions that meet your business requirement.</span></span> 

<span data-ttu-id="6ecdc-108">既存のコント ローラーを拡張するには、既存のコントローラー クラスを拡張する新しいクラスを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ecdc-108">To extend an existing controller, you must define a new class that extends an existing controller class.</span></span> <span data-ttu-id="6ecdc-109">既存のコント ローラーを拡張する新しいコント ローラーを作成するときは、新しいコントローラーは拡張されるコントローラーで新しいメソッドを作成するか既存のメソッドをオーバーライドできます。</span><span class="sxs-lookup"><span data-stu-id="6ecdc-109">When you create a new controller that extends an existing controller, the new controller can create new or override existing methods in the controller that is being extended.</span></span> <span data-ttu-id="6ecdc-110">オーバーライドされていない拡張コントローラー内のすべてのメソッドは、引き続き同じように機能します。</span><span class="sxs-lookup"><span data-stu-id="6ecdc-110">All methods in the extended controller that have not been overridden will continue to function as before.</span></span> <span data-ttu-id="6ecdc-111">この例では、**ExtendedCustomersController** クラスは **CustomersController** クラスを拡張し、**CustomersController**クラスは **Customers** エンティティ タイプのコントローラーです。</span><span class="sxs-lookup"><span data-stu-id="6ecdc-111">In this example, the **ExtendedCustomersController** class extends the **CustomersController** class, and the **CustomersController** class is the controller for the **Customers** entity type.</span></span>  

<span data-ttu-id="6ecdc-112">Commerce Scale Unit Web.config ファイルの **extensionComposition** セクションを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ecdc-112">You will need to update the **extensionComposition** section of the Commerce Scale Unit Web.config file.</span></span> <span data-ttu-id="6ecdc-113">詳細については、[Commerce Runtime CRT および Retail Server の拡張機能](commerce-runtime-extensibility.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ecdc-113">For more information, see [Commerce runtime (CRT) and Retail Server extensibility](commerce-runtime-extensibility.md).</span></span> <span data-ttu-id="6ecdc-114">サンプル コードは、Retail ソフトウェアの開発キット (SDK) 内のこのトピックから見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="6ecdc-114">You can find the sample code from this topic in the Retail software development kit (SDK).</span></span> 

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
