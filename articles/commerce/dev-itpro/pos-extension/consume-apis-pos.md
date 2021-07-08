---
title: POS でのカスタム ヘッドレス Commerce API およびエンティティの使用
description: このトピックでは、プロキシを使用して POS のカスタム ヘッドレス Commerce API およびエンティティを消費する方法について説明します。
author: mugunthanm
ms.date: 04/13/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-13-2020
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: e2c1c7bbdaf6ea0f515126e9248ad57fdd86b0f2
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271143"
---
# <a name="consume-custom-headless-commerce-apis-and-entities-in-pos"></a><span data-ttu-id="31e53-103">POS でのカスタム ヘッドレス Commerce API およびエンティティの使用</span><span class="sxs-lookup"><span data-stu-id="31e53-103">Consume custom headless Commerce APIs and entities in POS</span></span>

[!include [banner](../../../includes/banner.md)]

<span data-ttu-id="31e53-104">このトピックでは、プロキシを使用して POS のカスタム ヘッドレス Commerce API およびエンティティを消費する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="31e53-104">This topic explains how to consume custom headless Commerce APIs and entities in POS using Proxy.</span></span> <span data-ttu-id="31e53-105">Retail SDK バージョン 10.0.18 以降に適用されます。</span><span class="sxs-lookup"><span data-stu-id="31e53-105">It applies to the Retail SDK version 10.0.18 and later.</span></span>

1. <span data-ttu-id="31e53-106">Commerce Runtime 拡張機能プロジェクトは **Microsoft.Dynamics.Commerce.Sdk.Runtime** NuGet パッケージを参照し、POS 拡張機能プロジェクトが **Microsoft.Dynamics.Commerce.Sdk.Pos** NuGet パッケージを参照することを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="31e53-106">Make sure that your Commerce Runtime extension project references the **Microsoft.Dynamics.Commerce.Sdk.Runtime** NuGet package and that your POS extension project references the **Microsoft.Dynamics.Commerce.Sdk.Pos** NuGet package.</span></span>

2. <span data-ttu-id="31e53-107">POS 拡張機能プロジェクトから、API を定義する Commerce Runtime プロジェクトへの参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="31e53-107">Add a project reference from your POS extension project to the Commerce Runtime project that defines your APIs.</span></span>

3. <span data-ttu-id="31e53-108">ヘッドレス Commerce 拡張機能の TypeScript を生成するために、POS 拡張機能プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="31e53-108">Build your POS extension project to generate the TypeScript for your headless Commerce extensions.</span></span> <span data-ttu-id="31e53-109">ビルドでは、プロジェクト ルートの **DataService** という名のフォルダーで、2 つの TypeScript ファイルが作成されます。</span><span class="sxs-lookup"><span data-stu-id="31e53-109">The build generates two TypeScript files in a folder named **DataService** in your project root.</span></span>

    + <span data-ttu-id="31e53-110">**DataServiceEntities.g.ts**: Commerce Runtime 拡張機能プロジェクトの TypeScript エンティティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="31e53-110">**DataServiceEntities.g.ts**: Contains the TypeScript entities for all the referenced Commerce Runtime extension projects.</span></span>
    + <span data-ttu-id="31e53-111">**DataServiceRequests.g.ts**: 参照されたすべての Commerce Runtime 拡張機能プロジェクトの TypeScript データ サービス要求が含まれます。</span><span class="sxs-lookup"><span data-stu-id="31e53-111">**DataServiceRequests.g.ts**: Contains the TypeScript data service requests for all the referenced Commerce Runtime extension projects.</span></span>

4. <span data-ttu-id="31e53-112">次のコード例に示すように、データ サービスのエンティティと要求を拡張機能コードにインポートします。</span><span class="sxs-lookup"><span data-stu-id="31e53-112">Import your data service entities and requests into your extension code as shown in the following code example.</span></span>

    ```Javascript
    import * as Triggers from "PosApi/Extend/Triggers/ProductTriggers";
    import { ObjectExtensions } from "PosApi/TypeExtensions";
    import { ClientEntities } from "PosApi/Entities";
    import { StoreHours } from "../DataService/DataService.g"
    
    export default class PreProductSaleTrigger extends Triggers.PreProductSaleTrigger {
        /**
         * Executes the trigger functionality.
         * @param {Triggers.IPreProductSaleTriggerOptions} options The options provided to the trigger.
         */
        public execute(options: Triggers.IPreProductSaleTriggerOptions): Promise<ClientEntities.ICancelable> {
            if (ObjectExtensions.isNullOrUndefined(options)) {
                // This will never happen, but is included to demonstrate how to return a rejected promise when validation fails.
                let error: ClientEntities.ExtensionError
                    = new ClientEntities.ExtensionError("The options provided to the PreProductSaleTrigger were invalid. Please select a product and try again.");
    
                return Promise.reject(error);
            } else {
                return this._context.runtime.executeAsync(new StoreHours.GetStoreDaysByStoreRequest<StoreHours.GetStoreDaysByStoreResponse>(0));
            }
        }
    }
    ```

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
