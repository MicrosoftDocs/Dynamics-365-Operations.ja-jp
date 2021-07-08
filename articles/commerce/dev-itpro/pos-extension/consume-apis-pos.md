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
# <a name="consume-custom-headless-commerce-apis-and-entities-in-pos"></a>POS でのカスタム ヘッドレス Commerce API およびエンティティの使用

[!include [banner](../../../includes/banner.md)]

このトピックでは、プロキシを使用して POS のカスタム ヘッドレス Commerce API およびエンティティを消費する方法について説明します。 Retail SDK バージョン 10.0.18 以降に適用されます。

1. Commerce Runtime 拡張機能プロジェクトは **Microsoft.Dynamics.Commerce.Sdk.Runtime** NuGet パッケージを参照し、POS 拡張機能プロジェクトが **Microsoft.Dynamics.Commerce.Sdk.Pos** NuGet パッケージを参照することを確認する必要があります。

2. POS 拡張機能プロジェクトから、API を定義する Commerce Runtime プロジェクトへの参照を追加します。

3. ヘッドレス Commerce 拡張機能の TypeScript を生成するために、POS 拡張機能プロジェクトを構築します。 ビルドでは、プロジェクト ルートの **DataService** という名のフォルダーで、2 つの TypeScript ファイルが作成されます。

    + **DataServiceEntities.g.ts**: Commerce Runtime 拡張機能プロジェクトの TypeScript エンティティが含まれます。
    + **DataServiceRequests.g.ts**: 参照されたすべての Commerce Runtime 拡張機能プロジェクトの TypeScript データ サービス要求が含まれます。

4. 次のコード例に示すように、データ サービスのエンティティと要求を拡張機能コードにインポートします。

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
