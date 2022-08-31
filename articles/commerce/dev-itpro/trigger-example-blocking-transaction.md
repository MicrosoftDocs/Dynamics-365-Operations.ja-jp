---
title: トリガーの使用によるトランザクションのブロック
description: この記事では、トリガーを使用して請求書またはクレジット取引をブロックする方法を示します。
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 65893
ms.assetid: 605f5986-f84f-4b18-b94e-b0912cb367a1
ms.openlocfilehash: 282edc12384da453beb5977a9b5f2339d8ac31d6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281039"
---
# <a name="block-transactions-by-using-triggers"></a>トリガーの使用によるトランザクションのブロック

[!include [banner](../includes/banner.md)]

この記事では、トリガーを使用して請求書またはクレジット取引をブロックする方法を示します。

この記事では、請求書またはクレジット取引をブロックする方法を示します。

1.  Visual Studio を管理者としてオープンします。 新しい Visual C\# クラス ライブラリ (ポータブル) プロジェクトを作成し、CRTTriggerExtension という名前を付けます。 選択内容によってこのプロジェクトが Visual Studio 2010 と互換性がなくなるというメッセージが表示される場合、**OK** をクリックします。
2.  ソリューション エクスプローラーで、既定の class1.cs を GetCustomersServiceRequestTrigger.cs に名前を変更します。
3.  プロジェクトで **参照** ノードを右クリックし、次の参照を追加します。 参照の場所は、配置トポロジによって異なります。
    -   Microsoft.Dynamics.Commerce.Runtime.Entities.dll
    -   Microsoft.Dynamics.Commerce.Runtime.Framework.dll
    -   Microsoft.Dynamics.Commerce.Runtime.Services.Messages.dll

4.  GetCustomersServiceRequestTrigger.cs ファイルに、次の明細書を **使用して** 追加します。

    ```typescript
    using Microsoft.Dynamics.Commerce.Runtime.Messages;
    using Microsoft.Dynamics.Commerce.Runtime.Services.Messages;
    using Microsoft.Dynamics.Commerce.Runtime;
    ```

5.  コードの class1.cs の名前を GetCustomersServiceRequestTrigger に変更し、IRequestTrigger インターフェイス宣言を追加します。

    ```typescript
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using Microsoft.Dynamics.Commerce.Runtime;
    using Microsoft.Dynamics.Commerce.Runtime.Services.Messages;
    using Microsoft.Dynamics.Commerce.Runtime.Messages;

    namespace CRTTriggerExtension
    public class GetCustomersServiceRequestTrigger : IRequestTrigger
    {
    ```

6.  IRequestTrigger インターフェイス トリガーを実装します。 IRequestTrigger クラスを右クリックして、**クイック アクション** をクリックし、**インターフェイスの実装** をクリックします。 Visual Studio はインターフェイスを実装します。 また、カーソルを IRequestTrigger の上に配置して、**Ctrl+** を押し、**インターフェイスの実装** を選択することができます。
7.  空のインターフェイス メンバー SupportedRequestTypes、OnExecuted、および OnExecuting メソッドを次のコード例に示します。

    ```typescript
    public class GetCustomersServiceRequestTrigger : IRequestTrigger
    {
        public IEnumerable<Type> SupportedRequestTypes
        {
            get
            {
                throw new NotImplementedException();
            }
        }

        public void OnExecuted(Request request, Response response)
        {
            throw new NotImplementedException();
        }

        public void OnExecuting(Request request)
        {
            throw new NotImplementedException();
        } 
    }
    ```

8.  Commerce Scale Unit は、GetCustomersServiceRequest オブジェクトを使用して Commerce Runtime (CRT) から顧客詳細を取得し、GetCustomersServiceRequest オブジェクトを使用して顧客をトランザクションに追加します。 トランザクションに顧客を追加する前に、顧客がブロックされているかどうかを確認する必要があります。 これを行うには、この要求の転記トリガーを実装し、顧客がブロックされているかどうかを確認します。 顧客がブロックされている場合、MPOS によって例外がスローされます。
9.  SupportedRequestTypes メソッドで、GetCustomersServiceRequest のトリガーを追加することを CRT に通知します。 次のコード例は、GetCustomersServiceRequest をサポートされている型として追加する方法を示しています。

    ```typescript
    public IEnumerable<Type> SupportedRequestTypes
    {
        get
        {
            return new[] { typeof(GetCustomersServiceRequest) };       
        }
    }
    ```

10. 顧客が次のコードで OnExecuted (転記トリガー) メソッドでブロックされているかどうかを確認します。

     ```typescript
     public void OnExecuted(Request request, Response response)
     {
        if (response == null)
        {
        throw new ArgumentNullException("request");
        }

        var getCustomersServiceResponse = (GetCustomersServiceResponse)response;
        if(getCustomersServiceResponse.Customers.FirstOrDefault().Blocked == true)
        {
            string message = string.Format("Failed to add customer '{0}' to cart. Blocked customers are not allowed for transactions.",
                getCustomersServiceResponse.Customers.FirstOrDefault().AccountNumber);
            throw new CartValidationException(DataValidationErrors.Microsoft_Dynamics_Commerce_Runtime_CustomerAccountIsBlocked, message);
        }
     }
     ```

11. 最後に、次のコードで OnExecuting メソッドを更新します。

     ```typescript
     public void OnExecuting(Request request) 
     {
        if (request == null)
        {
            throw new ArgumentNullException("request");
        }
     }
     ```
12. **保存** をクリックします。






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
