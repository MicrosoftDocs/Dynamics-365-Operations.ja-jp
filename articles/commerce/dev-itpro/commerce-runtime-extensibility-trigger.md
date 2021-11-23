---
title: Commerce Rumtime (CRT) の拡張機能とトリガー
description: このトピックでは、Microsoft Dynamics 365 Commerce Runtime (CRT) のトリガー サポートについて説明します。 CRT は、すべての要求に対してプレ トリガーおよびポスト トリガーをサポートしています。
author: RobinARH
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: tfehr
ms.custom: 17731
ms.assetid: 2d6ec331-b266-4dbc-97c5-db2919b662dc
ms.search.region: Global
ms.search.industry: Retail
ms.author: sijoshi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: f267fbf5527af2da0adda56adc5e467bf1476cd1
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781576"
---
# <a name="commerce-runtime-crt-extensibility-and-triggers"></a>Commerce Rumtime (CRT) の拡張機能とトリガー

[!include [banner](../includes/banner.md)]

このトピックでは、Dynamics 365 Commerce Runtime (CRT) のトリガー サポートについて説明します。 CRT は、すべての要求に対してプレ トリガーおよびポスト トリガーをサポートしています。

## <a name="crt-trigger-overview"></a>CRT トリガーの概要

Commerce Runtime (CRT) トリガーによって CRT のワークフローを拡張でき、全ての CRT リクエストが実行される前後に、ビジネス ロジックに追加できるようにします。 次の 2 つの方法が使用されます。

-   **OnExecuting** – このメソッドは、要求が対応する **IRequestHandler** 実装によって処理される前に呼び出されます。
-   **OnExecuted** – このメソッドは、要求が対応する **IRequestHandler** 実装によって処理された後に呼び出されます。

## <a name="crt-trigger-extension"></a>CRT トリガーの拡張
トリガーを実装するには、次のコード例に示すように、これらのタスクを完了する必要があります。

1.  **IRequestTriggerAsync** を実装します。
2.  **SupportedRequestTypes** を指定して、トリガーを実行する必要のある要求のタイプを定義します。
3.  要求の解決前にビジネス ロジックを実行する必要がある場合、トリガーの実装を **OnExecuting** メソッドに記述します。
4.  要求の解決後にビジネス ロジックを実行する必要がある場合、トリガーの実装を **OnExecuted** メソッドに記述します。

### <a name="sample-trigger-implementation-for-get-customer-data-request"></a>顧客データ要求の取得のトリガー実装例。

```C#
    
        using Microsoft.Dynamics.Commerce.Runtime;
        using Microsoft.Dynamics.Commerce.Runtime.DataServices.Messages;
        using Microsoft.Dynamics.Commerce.Runtime.Messages;
        using System;
        using System.Collections.Generic;
        using System.Threading.Tasks;
        
        public class GetCustomerTriggers : IRequestTriggerAsync
        {
            /// <summary>
            /// Gets the supported requests for this trigger.
            /// </summary>
            public IEnumerable<Type> SupportedRequestTypes
            {
                get
                {
                    return new[] { typeof(GetCustomerDataRequest) };
                }
            }

            /// <summary>
            /// Post trigger code.
            /// </summary>
            /// <param name="request">The request.</param>
            /// <param name="response">The response.</param>
            public async Task OnExecuted(Request request, Response response)
            {
                //Custom logic
                
            // The only stub to handle async signature 
                await Task.CompletedTask;
            }

            /// <summary>
            /// Pre trigger code
            /// </summary>
            /// <param name="request">The request.</param>
            public async Task OnExecuting(Request request)
            {
                // custom logic 
                await Task.CompletedTask;
            }
        }
  ```

### <a name="register-the-extension"></a>拡張機能の登録

拡張ライブラリを **...\RetailServer\webroot\bin\ext フォルダー** にコピーして貼り付け、構成セクションのカスタム拡張ライブラリ情報を含む **commerceRuntime.ext.config** ファイルを更新します。 この例では、**Contoso.Commerce.Runtime.Services** はカスタムの拡張機能名です。

```xml
<add source="assembly" value="Contoso.Commerce.Runtime.Services" /> 
```

CRT 拡張機能がオフライン モードで動作するためには、構成セクションの下にある拡張ライブラリ情報で、**...\Microsoft Dynamics 365\70\Retail Modern POS\ClientBroker\ext\CommerceRuntime.MPOSOffline.ext.config** を更新してください。 次に、拡張ライブラリを **...\Microsoft Dynamics 365\70\Retail Modern POS\ClientBroker\ext** にコピーし貼り付けます。

### <a name="debugging-crt"></a>CRT のデバッグ

POS から CRT をデバッグするには、POS が Retail Server に接続されているときに、CRT 拡張プロジェクトを、w3wp.exe (Retail Server の IIS プロセス) に関連付けます。 オフライン モードの場合は、dllhost.exe プロセスに CRT 拡張プロジェクトを関連付けます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
