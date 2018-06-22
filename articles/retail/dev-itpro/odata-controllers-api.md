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
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: c8724e28d088cbd9cb44ec96559c458ed7dc0a56
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="web-api-and-odata-controllers"></a>Web API および OData コントローラー

[!include [banner](../includes/banner.md)]

この記事では、Retail サーバー用の Web API コントローラーを作成できるように、ApiController クラスを拡張するためのコードを提供します。

既定では、Microsoft Dynamics 365 for Retail のすべての Retail サーバー バイナリは OData のみを使用します。 従来の Web API を使用するコントローラーを使用する場合は、独自の Web API コントローラーを作成し、Web API 構成を拡張することができます。 次の例は、Retail Server 用の Web API コントローラーを作成する方法を示しています。

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

コントローラを作成するには、**Export** 属性を使用する新しいクラスを作成し、タイプが **IWebApiConfig** インターフェイスであることを指定します。 **IWebApiConfig** インターフェイスには、上書きすることができる 1 つのメソッド **Register** メソッドがあります。 **レジスタ** メソッドを上書き後、OData メタデータ コントローラーと同じマッピングを取得する基本クラスを呼び出すことができます。 標準の Web API コントローラーから派生する必要があります。 業務上の要件を満たすためにコントローラーをカスタマイズすることができます。 詳細については、「[ASP.NET Web API](http://msdn.microsoft.com/en-us/library/hh833994(v=vs.108).aspx)」を参照してください。




