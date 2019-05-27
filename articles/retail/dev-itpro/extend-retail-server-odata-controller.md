---
title: Retail Server OData コントローラーの拡張
description: このトピックでは、CustomController クラスを拡張するコードを説明します。
author: kfend
manager: AnnBe
ms.date: 11/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 31681
ms.assetid: c39a34b5-3fce-446f-877b-0aa41817ef25
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 6234906ad04df54171eec1fed1ff3718e6bb0e8e
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537559"
---
# <a name="extend-a-retail-server-odata-controller"></a>Retail Server OData コントローラーの拡張

[!include [banner](../includes/banner.md)]

このトピックでは、CustomersController クラスを拡張するコードを説明します。

コントローラーは、commerce エンティティ タイプの作成、読み取り、更新、および削除 (CRUD) の動作とアクションをコントロールする commerce エンティティのマッピングです。 各コマース エンティティには、対応するコントローラーが必要です。 Microsoft Dynamics 365 for Retail に含まれるコントローラーを拡張して、業務上の要件を満たすように新しい業務処理を追加することができます。 既存のコント ローラーを拡張するには、既存のコントローラー クラスを拡張する新しいクラスを定義する必要があります。 既存のコント ローラーを拡張する新しいコント ローラーを作成するときは、新しいコントローラーは拡張されるコントローラーで新しいメソッドを作成するか既存のメソッドをオーバーライドできます。 オーバーライドされていない拡張コントローラー内のすべてのメソッドは、引き続き同じように機能します。 この例では、**ExtendedCustomersController** クラスは **CustomersController** クラスを拡張し、**CustomersController**クラスは **Customers** エンティティ タイプのコントローラーです。  Retail サーバー Web.config ファイルの **extensionComposition** セクションを更新する必要があります。 詳細については、[Commerce Runtime (CRT) および Retail サーバー拡張機能](commerce-runtime-extensibility.md)の **MPOS/クラウド POS から新しい Retail サーバー API を呼び出す方法** セクションを参照してください。 サンプル コードは、Retail ソフトウェアの開発キット (SDK) 内のこのトピックから見つけることができます。 

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
