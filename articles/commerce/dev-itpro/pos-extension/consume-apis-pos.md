---
title: POS でのカスタム ヘッドレス Commerce API およびエンティティの使用
description: この記事では、販売時点管理 (POS) のカスタム ヘッドレス Commerce API およびエンティティを消費するようにプロキシを使用する方法について説明します。
author: josaw1
ms.date: 04/13/2021
ms.topic: article
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-13
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 23e27572198105a3d252072b489f8a9c331f1385
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285710"
---
# <a name="consume-custom-headless-commerce-apis-and-entities-in-pos"></a>POS でのカスタム ヘッドレス Commerce API およびエンティティの使用

[!include [banner](../../../includes/banner.md)]

この記事では、販売時点管理 (POS) のカスタム ヘッドレス Commerce API およびエンティティを消費するようにプロキシを使用する方法について説明します。 Retail ソフトウェア開発キット (SDK) バージョン 10.0.18 以降に適用されます。

1. Commerce Runtime (CRT) 拡張機能プロジェクトは **Microsoft.Dynamics.Commerce.Sdk.Runtime** NuGet パッケージを参照し、POS 拡張機能プロジェクトが **Microsoft.Dynamics.Commerce.Sdk.Pos** NuGet パッケージを参照することを確認する必要があります。
2. POS 拡張機能プロジェクトから、API を定義する CRT プロジェクトへの参照を追加します。
3. ヘッドレス Commerce 拡張機能の TypeScript を生成するために、POS 拡張機能プロジェクトを構築します。 ビルドでは、プロジェクト ルートの **DataService** というフォルダーに、2 つの TypeScript ファイルが生成されます。

    + **DataServiceEntities.g.ts** – このファイルには、参照されるすべての CRT 拡張機能プロジェクトの TypeScript エンティティが含まれます。
    + **DataServiceRequests.g.ts** – このファイルには、参照されるすべての CRT 拡張機能プロジェクトの TypeScript データ サービス要求が含まれます。

4. 次の例に示すように、データ サービスのエンティティと要求を拡張機能コードにインポートします。

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
