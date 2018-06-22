---
title: "Web API および OData コントローラー"
description: "この記事では、Retail サーバー用の Web API コントローラーを作成できるように、ApiController クラスを拡張するためのコードを提供します。"
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
ms.custom: 31481
ms.assetid: 4107b5a0-b4c4-4b83-b5b9-2fd82b26f36f
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 4251667b8ffaab5b579a0a03c1f086127f1f6b17
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="web-api-and-odata-controllers"></a><span data-ttu-id="49a49-103">Web API および OData コントローラー</span><span class="sxs-lookup"><span data-stu-id="49a49-103">Web API and OData controllers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="49a49-104">この記事では、Retail サーバー用の Web API コントローラーを作成できるように、ApiController クラスを拡張するためのコードを提供します。</span><span class="sxs-lookup"><span data-stu-id="49a49-104">This article provides code to extend the ApiController class so that you can create a Web API controller for Retail Server.</span></span>

<span data-ttu-id="49a49-105">既定では、Microsoft Dynamics 365 for Retail のすべての Retail サーバー バイナリは OData のみを使用します。</span><span class="sxs-lookup"><span data-stu-id="49a49-105">By default, all the Retail Server binaries in Microsoft Dynamics 365 for Retail use only OData.</span></span> <span data-ttu-id="49a49-106">従来の Web API を使用するコントローラーを使用する場合は、独自の Web API コントローラーを作成し、Web API 構成を拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="49a49-106">If you want to use a controller that uses a traditional Web API, you can create your own Web API controller and extend the Web API configuration.</span></span> <span data-ttu-id="49a49-107">次の例は、Retail Server 用の Web API コントローラーを作成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="49a49-107">The following example shows how to create a Web API controller for Retail Server.</span></span>

    namespace Microsoft.Dynamics.RetailServer.Samples.Extensions
    {
        using System.Collections.Generic;
        using System.Runtime.InteropServices;
        using System.Web.Http;
        using Commerce.Runtime.DataModel;
        using Retail.StoreServerServiceLibrary;
        [ComVisible(false)]
        [ExtendedController("Values")]
        [CommerceAuthorization(AllowedRetailRoles = new string[] { CommerceRoles.Anonymous }, CheckRetailOperation = false)]
        public class ValuesController : ApiController
        {
            // GET /api/values
            public IEnumerable<string> Get()
            {
                return new string[] { "value1", "value2" };
            }
        }
    }

<span data-ttu-id="49a49-108">コントローラを作成するには、**Export** 属性を使用する新しいクラスを作成し、タイプが **IWebApiConfig** インターフェイスであることを指定します。</span><span class="sxs-lookup"><span data-stu-id="49a49-108">To create the controller, create a new class that uses the **Export** attribute, and specify that the type is the **IWebApiConfig** interface.</span></span> <span data-ttu-id="49a49-109">**IWebApiConfig** インターフェイスには、上書きすることができる 1 つのメソッド **Register** メソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="49a49-109">The **IWebApiConfig** interface has one method that you can override, the **Register** method.</span></span> <span data-ttu-id="49a49-110">**レジスタ** メソッドを上書き後、OData メタデータ コントローラーと同じマッピングを取得する基本クラスを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="49a49-110">After you override the **Register** method, you can call the base class to get the same mapping as an OData metadata controller.</span></span> <span data-ttu-id="49a49-111">標準の Web API コントローラーから派生する必要があります。</span><span class="sxs-lookup"><span data-stu-id="49a49-111">You must derive from the standard Web API controller.</span></span> <span data-ttu-id="49a49-112">業務上の要件を満たすためにコントローラーをカスタマイズすることができます。</span><span class="sxs-lookup"><span data-stu-id="49a49-112">You can then customize the controller to meet your business requirements.</span></span> <span data-ttu-id="49a49-113">詳細については、「[ASP.NET Web API](http://msdn.microsoft.com/en-us/library/hh833994(v=vs.108).aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="49a49-113">For more information, see [ASP.NET Web API](http://msdn.microsoft.com/en-us/library/hh833994(v=vs.108).aspx).</span></span>




