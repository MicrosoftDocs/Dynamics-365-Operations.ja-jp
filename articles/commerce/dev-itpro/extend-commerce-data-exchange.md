---
title: Commerce Data Exchange の拡張 - リアルタイム サービス
description: このトピックでは、RetailTransactionServiceEx クラスに拡張メソッドを追加して、Commerce Data Exchange - リアルタイム サービスを拡張する方法について説明します。
author: mugunthanm
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: tfehr
ms.custom: 68673
ms.assetid: 72a63836-2908-45fa-b1a6-3b1c499a19a2
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 835f37a5a49fdbff8183d3ea63318c68abf03cf6
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7783346"
---
# <a name="extend-commerce-data-exchange---real-time-service"></a>Commerce Data Exchange の拡張 - リアルタイム サービス

[!Include [banner](../includes/banner.md)]

このトピックでは、RetailTransactionServiceEx クラスに拡張メソッドを追加して、Commerce Data Exchange (CDX) - リアルタイム サービスを拡張する方法について説明します。 リアルタイム サービスは、クライアントがリアルタイムでコマース機能を操作できるようします。 Retail サーバーから Finance and Operation データベースとクラスに直接アクセスすることはできません。 Finance and Operations および Commerce Runtime 拡張機能を使用する CDX クラスの拡張機能を介してアクセスする必要があります。

Commerce Data Exchange - リアルタイム サービスを拡張するには、**RetailTransactionServiceEx** クラスで新しいメソッドを作成します。 このメソッドは、次の基準を満たしている必要があります。

-   このメソッドは、パブリック静的メソッドでなければなりません。
-   戻り値は、長さが 2 以上のコンテナーである必要があります。 最初の要素は、メソッド呼び出しが成功したかどうかを示すブール値と、コメントまたはエラー メッセージに使用できる文字列値でなければなりません。 コンテナー内の他の項目は任意の型になることができ、入れ子になったコンテナーにもなれます。
-   メソッドのパラメーターは、次のプリミティブ型のいずれかでなければなりません。
    -   ブール型
    -   日付
    -   int
    -   int64
    -   str
    -   guid
    -   実績

## <a name="create-and-call-a-new-extension-method"></a>新しい拡張メソッドの作成と呼び出し
1. Microsoft Visual Studio を起動します。
2. **Dynamics 365** メニューで、**モデル管理 > モデルの作成** をクリックします。
3. **モデルの作成** ダイアログ ボックスに、次の詳細を入力します。
   -   **モデル名** - Contoso
   -   **モデル発行元** - Contoso
   -   **レイヤー** - USR (関連するレイヤーを選択)
   -   **バージョン** - 1.0.0.0
   -   **モデルの表示名** - Contoso

4. **次へ** をクリックします。
5. ダイアログ ボックスで、**既存のパッケージを選択** を選択してから、一覧で **アプリケーション スイート** を選択します。
6. **次へ** をクリックします。
7. **完了** をクリックします。
8. **新しいプロジェクト** ダイアログ ボックスに、**ContosoRetailTransactionServiceEx** というプロジェクト名を入力します。
9. **OK** をクリックします。
10. プロジェクトを右クリックし、**追加 > 新しい項目** を選択します。 **新しい項目の追加** ウィンドウで、**クラス** を選択し、**ContosoRetailTransactionServiceSample** としてクラスの名前を入力します。

    Commerce Runtime (CRT) で CDX メソッドを使用するには、ExtensionOf(classStr(RetailTransactionServiceEx) など、ExtensionOf 属性をクラスに追加する必要があります。 つまり、RetailTransactionServiceEx からクラスが拡張されます。

11. コード エディターで、次のコードを追加します。 

    ```X++
    [ExtensionOf(classStr(RetailTransactionServiceEx))]
    final class ContosoRetailTransactionServiceSample
    {
    }
    ``` 

12. クラス内部で、カスタム ロジックを実行する新しいメソッドを追加します。 これは、カスタム ロジックを実行するために CRT から呼び出すメソッドです。

    ```X++
    [ExtensionOf(classStr(RetailTransactionServiceEx))]
    final class ContosoRetailTransactionServiceSample_Extension
    {
        public static container SerialCheck(str _serialNum)
        {
            boolean success = false;
            str errorMessage;
            int fromLine;
            
            try
            {
                if (_serialNum)
                {
                     ttsbegin;
                   // check whether the serial number exists

                    // Add your custom logic

                    errorMessage = "Serial number found";
                    ttscommit;
                }
                else
                {
                    // Add your custom logic
                    success = false;
                    errorMessage = "Serial number not found";
                }
            }
            catch (Exception::Error)
            {
                ttsAbort;
                error = RetailTransactionServiceUtilities::getInfologMessages(fromLine);
            }

            // Return sanitized error code.
            errorMessage = RetailTransactionServiceUtilities::getErrorCode(errorMessage);

            return [success, errorMessage, "Custom values"];
        }
    }
    ```
13. ソリューション エクスプローラーで、プロジェクトを右クリックしてから **ビルド** をクリックします。

新しい拡張メソッドを作成した後は、プロジェクトが展開されます。

## <a name="call-the-new-method-from-the-crt"></a>CRT から新しいメソッドを呼び出す
1.  Commerce runtime (CRT) 拡張機能に、Microsoft.Dynamics.Commerce.Runtime.RealtimeServices.Messages の nuget パッケージがまだ追加されていない場合は、それを含めます。
2.  新しいメソッドを呼び出すには、次のサンプル コードを使用します。

    ```C#
        
            InvokeExtensionMethodRealtimeRequest extensionRequest = new InvokeExtensionMethodRealtimeRequest("SerialCheck", "123");
            InvokeExtensionMethodRealtimeResponse response = await request.RequestContext.ExecuteAsync<InvokeExtensionMethodRealtimeResponse>   (extensionRequest).ConfigureAwait(false);
                ReadOnlyCollection<object> results = response.Result;
                
                string resValue = (string)results[0];       
    ```

3.  results オブジェクトからは、リアルタイム サービスからの応答値を読み取ることができます。
4.  CRT フレームワーク コードは、成功/失敗の状態を確認し、CDX メソッドから返された値に基づいてエラー メッセージを提供します。 必要に応じて、拡張機能コードでこれをキャッチし、追加のロジックを提供することができます。  

    > [!NOTE]
    > **InvokeExtensionMethodRealtimeRequest** メソッドは 2 つのパラメーターを取ります。 1 つのパラメ ーターはリアルタイム サービス メソッド名であり、その他はパラメータの一覧を使用する必要があります。 渡されるメソッド名は、**ContosoRetailTransactionServiceSample** クラスで作成したメソッド名と同じにする必要があります。
    
 ```
  public InvokeExtensionMethodRealtimeRequest(string methodName, params object[] parameters)
            : base(methodName, parameters)
        {
        }
 ```

## <a name="cdx-offline"></a>CDX オフライン

HQ に接続されていない場合、クライアント/Retail Server は CDX メソッドを呼び出すことができません。 この場合、拡張機能コードは次のベスト プラクティスに従う必要があります。

-   CDX メソッドを呼び出す前に、CRT がオンライン (Retail Server) データベースまたはオフライン (ローカル) データベースに接続されているかどうかを確認します。 この操作は、POS および CRT から行うことができ ます。

### <a name="how-to-check-the-connection-status"></a>接続ステータスを確認する方法

**POS**

**GetConnectionStatusClientRequest** POS API を使用します。

**CRT**

```C#
if(request.RequestContext.Runtime.Configuration.IsMasterDatabaseConnectionString)
{ }
```

-   CDX メソッドへの接続に失敗した場合には、HQ に接続していない場合は操作を実行できない、または CDX メソッドに接続されていない状態でこの操作をする場合には軽減ロジックを実行する必要がある、というエラー メッセージが表示されることがあります。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
