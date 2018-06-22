---
title: "メタデータの拡張"
description: "この記事では、CommerceModelFactory クラスを拡張するコードを説明します。"
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
ms.custom: 31641
ms.assetid: 6e25b63e-be1e-42fc-b1bd-c91585cd624d
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 06d8c92d661fd251d10200ce4ae6992d3ff9c23a
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="extend-the-metadata"></a><span data-ttu-id="4c0e0-103">メタデータの拡張</span><span class="sxs-lookup"><span data-stu-id="4c0e0-103">Extend the metadata</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4c0e0-104">この記事では、CommerceModelFactory クラスを拡張するコードを説明します。</span><span class="sxs-lookup"><span data-stu-id="4c0e0-104">This article provides code to extend the CommerceModelFactory class.</span></span>

<span data-ttu-id="4c0e0-105">OData を Microsoft Dynamics 365 for Retail と共に使用するとき、メタデータはクライアントとサーバー間の契約を定義します。</span><span class="sxs-lookup"><span data-stu-id="4c0e0-105">When you use OData together with Microsoft Dynamics 365 for Retail, metadata defines the contract between a client and server.</span></span> <span data-ttu-id="4c0e0-106">メタデータ はエンティティ定義とアクション定義を公開しているため、サーバー側で変更を加えると、クライアント側のツールを使用してプロキシ コードを生成できます。</span><span class="sxs-lookup"><span data-stu-id="4c0e0-106">The metadata exposes entity definitions and action definitions, so that when you make a change on the server side, you can use a tool on the client side to generate proxy code.</span></span> <span data-ttu-id="4c0e0-107">したがって、メンテナンスにかかる開発者の労力が軽減されます。</span><span class="sxs-lookup"><span data-stu-id="4c0e0-107">Therefore, the maintenance effort for developers is reduced.</span></span> <span data-ttu-id="4c0e0-108">新規または変更されたエンティティおよびアクションを使用するには、メタデータを拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c0e0-108">To consume new or changed entities and actions, you must extend the metadata.</span></span> <span data-ttu-id="4c0e0-109">Retail サーバーには、**CommerceModelFactory** という既定メタデータ コントローラーがあります。</span><span class="sxs-lookup"><span data-stu-id="4c0e0-109">Retail Server has a default metadata controller that is named **CommerceModelFactory**.</span></span> <span data-ttu-id="4c0e0-110">既定のコント ローラーを拡張するには、**エクスポート** 属性と **IEdmModelFactory** インターフェイスを使用する新しいクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="4c0e0-110">To extend the default controller, you create a new class that uses the **Export** attribute together with the **IEdmModelFactory** interface.</span></span> <span data-ttu-id="4c0e0-111">既存のコードを追加してオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="4c0e0-111">You can then add and override existing code.</span></span> <span data-ttu-id="4c0e0-112">たとえば、新しいエンティティ セット、新しいアクション、新しい複合型、または新しい例外タイプを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="4c0e0-112">For example, you can add new entity sets, new actions, new complex types, or new exception types.</span></span> <span data-ttu-id="4c0e0-113">次の例では、**ExtendedEdmModelFactory** クラスは **CommerceModelFactory** メタデータ コントローラーを拡張して、**NewAction** という新しいアクションおよび **NewEntities** という新しいエンティティ セットを作成します。</span><span class="sxs-lookup"><span data-stu-id="4c0e0-113">In the following example, the **ExtendedEdmModelFactory** class extends the **CommerceModelFactory** metadata controller and creates a new action that is named **NewAction** and a new entity set that is named **NewEntities**.</span></span> <span data-ttu-id="4c0e0-114">サンプル コードは、Retail ソフトウェアの開発キット (SDK) 内のこのトピックから見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="4c0e0-114">You can find the sample code from this topic in the Retail software development kit (SDK).</span></span>

    namespace Microsoft.Dynamics.RetailServer.Samples.Extensions
    {
        using System.ComponentModel.Composition;
        using Microsoft.Dynamics.Retail.StoreServerServiceLibrary;
        [Export(typeof(IEdmModelFactory))]
        public class ExtendedEdmModelFactory : CommerceModelFactory
        {
            protected override void BuildNonBindableActions()
            {
                base.BuildNonBindableActions();
                var NewAction = BindAction("NewAction");
                NewAction.Returns<string>();
            }
            protected override void BuildEntitySets()
            {
                base.BuildEntitySets();
                BuildEntitySet<NewEntity>("NewEntities");
            }
        }
    }



