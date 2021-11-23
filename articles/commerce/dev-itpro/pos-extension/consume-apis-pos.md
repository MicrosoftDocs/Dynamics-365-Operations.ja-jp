---
title: POS でのカスタム ヘッドレス Commerce API およびエンティティの使用
description: このトピックでは、販売時点管理 (POS) のカスタム ヘッドレス Commerce API およびエンティティを消費するようにプロキシを使用する方法について説明します。
author: mugunthanm
ms.date: 04/13/2021
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-13-2020
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 42454ddf607dc1f365603ec2ce296d6dfdbb71e0
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7783336"
---
# <a name="consume-custom-headless-commerce-apis-and-entities-in-pos"></a>POS でのカスタム ヘッドレス Commerce API およびエンティティの使用

[!include [banner](../../../includes/banner.md)]

このトピックでは、販売時点管理 (POS) のカスタム ヘッドレス Commerce API およびエンティティを消費するようにプロキシを使用する方法について説明します。 Retail ソフトウェア開発キット (SDK) バージョン 10.0.18 以降に適用されます。

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
