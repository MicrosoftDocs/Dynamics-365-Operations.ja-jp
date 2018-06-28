---
title: "Commerce Data Exchange を拡張 - Real-time Service"
description: "この記事では、RetailTransactionServiceEx クラスに拡張メソッドを追加して、Commerce Data Exchange - リアルタイム サービスを拡張する方法について説明します。 リアルタイム サービスは、Retail クライアントがリアルタイムで小売機能を操作できるようします。"
author: mugunthanm
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 68673
ms.assetid: 72a63836-2908-45fa-b1a6-3b1c499a19a2
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 5c63e82cf77a4425bc9d36f455b987c12a4af847
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="extend-commerce-data-exchange---real-time-service"></a>Commerce Data Exchange を拡張 - Real-time Service

[!include [banner](../includes/banner.md)]

この記事では、RetailTransactionServiceEx クラスに拡張メソッドを追加して、Commerce Data Exchange - リアルタイム サービスを拡張する方法について説明します。 リアルタイム サービスは、Retail クライアントがリアルタイムで小売機能を操作できるようします。

Commerce Data Exchange: リアルタイム サービスを拡張するには、**RetailTransactionServiceEx** クラスで新しいメソッドを作成します。 このメソッドは、次の基準を満たしている必要があります。

-   このメソッドは、パブリック静的メソッドでなければなりません。
-   戻り値は、長さが 2 以上のコンテナーである必要があります。 最初の 2 つの要素は、メソッド呼び出しが成功したかどうかを示すブール値と、コメントまたはエラー メッセージに使用できる文字列値でなければなりません。 コンテナー内の他の項目は任意の型になることができ、入れ子になったコンテナーにもなれます。
-   メソッドのパラメーターは、次のプリミティブ型のいずれかでなければなりません。
    -   ブール型
    -   日付
    -   int
    -   int64
    -   str
    -   guid
    -   実数

## <a name="create-and-call-a-new-extension-method"></a>新しい拡張メソッドの作成と呼び出し
1. Microsoft Visual Studio を開始します。
2. <strong>Dynamics 365 **メニューで、**モデル管理</strong> &gt; <strong>モデルの作成</strong>をクリックします。
3. **モデルの作成**ダイアログ ボックスに、次の詳細を入力します。
   -   **モデル名**: Contoso
   -   **モデル発行元**: Contoso
   -   **レイヤー**: USR (関連するレイヤーを選択)
   -   **バージョン**:1.0.0.0
   -   **モデルの表示名**: Contoso

4. **次へ** をクリックします。
5. ダイアログ ボックスで、**既存のパッケージを選択**を選択してから、一覧で**アプリケーション スイート**を選択します。
6. **次へ** をクリックします。
7. **完了** をクリックします。
8. **新しいプロジェクト** ダイアログ ボックスに、**ContosoRetailTransactionServiceEx** というプロジェクト名を入力します。
9. **OK** をクリックします。
10. アプリケーション エクスプローラーで、**コード** ノードを展開して**クラス**を選択します。
11. **RetailTransactionServiceEx** クラスを右クリックし、、**カスタマイズ** をクリックします。
12. コード エディターで、次のコードを追加します。

        public static container SerialCheck(str _serialNum)
            {
                boolean             success = true;
                str                 errorMessage;
                container           serialNumResult;
                if (_serialNum)
                {
                // check whether the serial number exists
                    errorMessage = "Serial number found";
                }
                else
                {
                    success = false;
                    errorMessage = "Serial number not found";
                }

                return [success, errorMessage, "Serial number found"];
        }

13. ソリューション エクスプローラーで、プロジェクトを右クリックしてから**ビルド**をクリックします。

新しい拡張メソッドを作成した後は、プロジェクトが展開されます。

## <a name="call-the-new-method-from-the-crt"></a>CRT から新しいメソッドを呼び出す
1.  Commerce Runtime (CRT) で、Microsoft.Dynamics.Commerce.Runtime.TransactionService.dll への参照が追加されていない場合は追加します。
2.  新しいメソッドを呼び出すには、次のサンプル コードを使用します。

        TransactionServiceClient transactionService = new TransactionServiceClient(request.RequestContext);
        ReadOnlyCollection serviceResponse = transactionService.InvokeExtensionMethod("SerialCheck", "123");

3.  ServiceResponse オブジェクトからは、リアルタイム サービスからの応答値を読み取ることができます。

**注記:** **InvokeExtensionMethod** メソッドは 2 つのパラメーターを取ります。 1 つのパラメ ーターはリアルタイム サービス メソッド名であり、その他はパラメータの一覧を使用する必要があります。 渡されるメソッド名は、**RetailTransactionServiceEx** クラスで作成したメソッド名と同じにする必要があります。




