---
title: Commerce Data Exchange の拡張 - リアルタイム サービス
description: このトピックでは、RetailTransactionServiceEx クラスに拡張メソッドを追加して、Commerce Data Exchange - リアルタイム サービスを拡張する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 10/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 68673
ms.assetid: 72a63836-2908-45fa-b1a6-3b1c499a19a2
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: dbf138d5f60c5b72689460c4477f957b464d71f9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369247"
---
# <a name="extend-commerce-data-exchange---real-time-service"></a>Commerce Data Exchange の拡張 - リアルタイム サービス

[!include [banner](../includes/banner.md)]

このトピックでは、RetailTransactionServiceEx クラスに拡張メソッドを追加して、Commerce Data Exchange (CDX) - リアルタイム サービスを拡張する方法について説明します。 リアルタイム サービスは、Retail クライアントがリアルタイムで小売機能を操作できるようします。

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
3. **モデルの作成**ダイアログ ボックスに、次の詳細を入力します。
   -   **モデル名** - Contoso
   -   **モデル発行元** - Contoso
   -   **レイヤー** - USR (関連するレイヤーを選択)
   -   **バージョン** - 1.0.0.0
   -   **モデルの表示名** - Contoso

4. **次へ** をクリックします。
5. ダイアログ ボックスで、**既存のパッケージを選択**を選択してから、一覧で**アプリケーション スイート**を選択します。
6. **次へ** をクリックします。
7. **完了** をクリックします。
8. **新しいプロジェクト** ダイアログ ボックスに、**ContosoRetailTransactionServiceEx** というプロジェクト名を入力します。
9. **OK** をクリックします。
10. プロジェクトを右クリックし、**追加 > 新しい項目** を選択します。 **新しい項目の追加** ウィンドウで、**クラス** を選択し、**ContosoRetailTransactionServiceSample** としてクラスの名前を入力します。

Commerce Runtime (CRT) で CDX メソッドを使用するには、ExtensionOf(classStr(RetailTransactionServiceEx) など、ExtensionOf 属性をクラスに追加する必要があります。 つまり、RetailTransactionServiceEx からクラスが拡張されます。

11. コード エディターで、次のコードを追加します。
```C#
    [ExtensionOf(classStr(RetailTransactionServiceEx))]
    final class ContosoRetailTransactionServiceSample
    {
    }
```
12. クラス内部で、カスタム ロジックを実行する新しいメソッドを追加します。 これは、カスタム ロジックを実行するために CRT から呼び出すメソッドです。
```C#
    [ExtensionOf(classStr(RetailTransactionServiceEx))]
    final class ContosoRetailTransactionServiceSample
    {
        public static container SerialCheck(str _serialNum)
        {
            boolean success = false;
            str errorMessage;
            int fromLine;

            ttsbegin;

            try
            {
                if (_serialNum)
                {
                    // check whether the serial number exists

                    // Add your custom logic

                    errorMessage = "Serial number found";
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
                error = RetailTransactionServiceUtilities::getInfologMessages(fromLine);
            }

            ttscommit;

            // Return sanitized error code.
            errorMessage = RetailTransactionServiceUtilities::getErrorCode(errorMessage);

            return [success, errorMessage, "Custom values"];
        }
    }
```
13. ソリューション エクスプローラーで、プロジェクトを右クリックしてから**ビルド**をクリックします。

新しい拡張メソッドを作成した後は、プロジェクトが展開されます。

## <a name="call-the-new-method-from-the-crt"></a>CRT から新しいメソッドを呼び出す
1.  Commerce Runtime (CRT) で、Microsoft.Dynamics.Commerce.Runtime.TransactionService.dll への参照が追加されていない場合は追加します。
2.  新しいメソッドを呼び出すには、次のサンプル コードを使用します。
```C#
        try
        {
            TransactionServiceClient transactionService = new TransactionServiceClient(request.RequestContext);
            ReadOnlyCollection<object> results = transactionService.InvokeExtensionMethod("SerialCheck", "123");
        }
        catch (HeadquarterTransactionServiceException exception)
        {
             string errorCode = (string)exception.HeadquartersErrorData.FirstOrDefault();
             RetailLogger.Log.ExtendedErrorEvent(errorCode, "Custom information", "method name");
             throw new CommerceException("Error resource id", "message");
        }
```
> [!NOTE]
> 本社で例外が発生した場合、HeadquarterTransactionServiceException が発生します。これは、例外をキャプチャし、シナリオに基づいて POS にわかりやすいメッセージを表示します。 例外をログに記録する場合は、RetailLogger.Log クラス オブジェクトを使用してイベントを記録します。

3.  results オブジェクトからは、リアルタイム サービスからの応答値を読み取ることができます。

> [!NOTE]
> **InvokeExtensionMethod** メソッドは 2 つのパラメーターを取ります。 1 つのパラメ ーターはリアルタイム サービス メソッド名であり、その他はパラメータの一覧を使用する必要があります。 渡されるメソッド名は、**ContosoRetailTransactionServiceSample** クラスで作成したメソッド名と同じにする必要があります。


