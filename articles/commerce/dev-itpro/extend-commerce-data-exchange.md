---
title: Commerce Data Exchange の拡張 - リアルタイム サービス
description: このトピックでは、RetailTransactionServiceEx クラスに拡張メソッドを追加して、Commerce Data Exchange - リアルタイム サービスを拡張する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 68673
ms.assetid: 72a63836-2908-45fa-b1a6-3b1c499a19a2
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 81756a4825171b94e538b5b64b2260f0b27ad26f
ms.sourcegitcommit: fd62ab3d399b0d6ea0d362f1d403a300e84a576d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/26/2021
ms.locfileid: "5067607"
---
# <a name="extend-commerce-data-exchange---real-time-service"></a><span data-ttu-id="4c750-103">Commerce Data Exchange の拡張 - リアルタイム サービス</span><span class="sxs-lookup"><span data-stu-id="4c750-103">Extend Commerce Data Exchange - Real-time Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4c750-104">このトピックでは、RetailTransactionServiceEx クラスに拡張メソッドを追加して、Commerce Data Exchange (CDX) - リアルタイム サービスを拡張する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4c750-104">This topic explains how you can extend Commerce Data Exchange (CDX) - Real-time service by adding extension methods to the RetailTransactionServiceEx class.</span></span> <span data-ttu-id="4c750-105">リアルタイム サービスは、クライアントがリアルタイムでコマース機能を操作できるようします。</span><span class="sxs-lookup"><span data-stu-id="4c750-105">Real-time Service enables clients to interact with Commerce functionality in real time.</span></span> <span data-ttu-id="4c750-106">Retail サーバーから Finance and Operation データベースとクラスに直接アクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="4c750-106">Finance and Operation databases and classes can’t be accessed directly from Retail server.</span></span> <span data-ttu-id="4c750-107">Finance and Operations および Commerce Runtime 拡張機能を使用する CDX クラスの拡張機能を介してアクセスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c750-107">You should access them through the CDX class extension using the Finance and Operations and Commerce Runtime extension.</span></span>

<span data-ttu-id="4c750-108">Commerce Data Exchange - リアルタイム サービスを拡張するには、**RetailTransactionServiceEx** クラスで新しいメソッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="4c750-108">To extend Commerce Data Exchange - Real-time Service, you create a new method in the **RetailTransactionServiceEx** class.</span></span> <span data-ttu-id="4c750-109">このメソッドは、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c750-109">This method must meet the following criteria:</span></span>

-   <span data-ttu-id="4c750-110">このメソッドは、パブリック静的メソッドでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="4c750-110">The method must be a public static method.</span></span>
-   <span data-ttu-id="4c750-111">戻り値は、長さが 2 以上のコンテナーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c750-111">The return value must be a container that has a length of 2 or more.</span></span> <span data-ttu-id="4c750-112">最初の要素は、メソッド呼び出しが成功したかどうかを示すブール値と、コメントまたはエラー メッセージに使用できる文字列値でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="4c750-112">The first element must be a Boolean value that indicates whether the method call was successful, and a string value that you can use for a comment or error message.</span></span> <span data-ttu-id="4c750-113">コンテナー内の他の項目は任意の型になることができ、入れ子になったコンテナーにもなれます。</span><span class="sxs-lookup"><span data-stu-id="4c750-113">The other items in the container can be of any type, and they can even be nested containers.</span></span>
-   <span data-ttu-id="4c750-114">メソッドのパラメーターは、次のプリミティブ型のいずれかでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="4c750-114">The method parameters must be one of the following primitive types:</span></span>
    -   <span data-ttu-id="4c750-115">ブール型</span><span class="sxs-lookup"><span data-stu-id="4c750-115">Boolean</span></span>
    -   <span data-ttu-id="4c750-116">日付</span><span class="sxs-lookup"><span data-stu-id="4c750-116">date</span></span>
    -   <span data-ttu-id="4c750-117">int</span><span class="sxs-lookup"><span data-stu-id="4c750-117">int</span></span>
    -   <span data-ttu-id="4c750-118">int64</span><span class="sxs-lookup"><span data-stu-id="4c750-118">int64</span></span>
    -   <span data-ttu-id="4c750-119">str</span><span class="sxs-lookup"><span data-stu-id="4c750-119">str</span></span>
    -   <span data-ttu-id="4c750-120">guid</span><span class="sxs-lookup"><span data-stu-id="4c750-120">guid</span></span>
    -   <span data-ttu-id="4c750-121">実績</span><span class="sxs-lookup"><span data-stu-id="4c750-121">Real</span></span>

## <a name="create-and-call-a-new-extension-method"></a><span data-ttu-id="4c750-122">新しい拡張メソッドの作成と呼び出し</span><span class="sxs-lookup"><span data-stu-id="4c750-122">Create and call a new extension method</span></span>
1. <span data-ttu-id="4c750-123">Microsoft Visual Studio を起動します。</span><span class="sxs-lookup"><span data-stu-id="4c750-123">Start Microsoft Visual Studio.</span></span>
2. <span data-ttu-id="4c750-124">**Dynamics 365** メニューで、**モデル管理 > モデルの作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c750-124">On the **Dynamics 365** menu, click **Model management > Create model**.</span></span>
3. <span data-ttu-id="4c750-125">**モデルの作成** ダイアログ ボックスに、次の詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="4c750-125">In the **Create model** dialog box, enter the following details.</span></span>
   -   <span data-ttu-id="4c750-126">**モデル名** - Contoso</span><span class="sxs-lookup"><span data-stu-id="4c750-126">**Model name** - Contoso</span></span>
   -   <span data-ttu-id="4c750-127">**モデル発行元** - Contoso</span><span class="sxs-lookup"><span data-stu-id="4c750-127">**Model publisher** - Contoso</span></span>
   -   <span data-ttu-id="4c750-128">**レイヤー** - USR (関連するレイヤーを選択)</span><span class="sxs-lookup"><span data-stu-id="4c750-128">**Layer** - USR (Select the relevant layer)</span></span>
   -   <span data-ttu-id="4c750-129">**バージョン** - 1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="4c750-129">**Version** - 1.0.0.0</span></span>
   -   <span data-ttu-id="4c750-130">**モデルの表示名** - Contoso</span><span class="sxs-lookup"><span data-stu-id="4c750-130">**Model display name** - Contoso</span></span>

4. <span data-ttu-id="4c750-131">**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c750-131">Click **Next**.</span></span>
5. <span data-ttu-id="4c750-132">ダイアログ ボックスで、**既存のパッケージを選択** を選択してから、一覧で **アプリケーション スイート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c750-132">In the dialog box, select **Select existing package**, and then select **Application Suite** in the list.</span></span>
6. <span data-ttu-id="4c750-133">**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c750-133">Click **Next**.</span></span>
7. <span data-ttu-id="4c750-134">**完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c750-134">Click **Finish**.</span></span>
8. <span data-ttu-id="4c750-135">**新しいプロジェクト** ダイアログ ボックスに、**ContosoRetailTransactionServiceEx** というプロジェクト名を入力します。</span><span class="sxs-lookup"><span data-stu-id="4c750-135">In the **New project** dialog box, enter **ContosoRetailTransactionServiceEx** as the project name.</span></span>
9. <span data-ttu-id="4c750-136">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c750-136">Click **OK**.</span></span>
10. <span data-ttu-id="4c750-137">プロジェクトを右クリックし、**追加 > 新しい項目** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c750-137">Right-click the project and select **Add > New item**.</span></span> <span data-ttu-id="4c750-138">**新しい項目の追加** ウィンドウで、**クラス** を選択し、**ContosoRetailTransactionServiceSample** としてクラスの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="4c750-138">In the **Add New Item** window, select **Class** and enter the name of the class as **ContosoRetailTransactionServiceSample**.</span></span>

    <span data-ttu-id="4c750-139">Commerce Runtime (CRT) で CDX メソッドを使用するには、ExtensionOf(classStr(RetailTransactionServiceEx) など、ExtensionOf 属性をクラスに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c750-139">To consume the CDX method in Commerce runtime (CRT) you must add the ExtensionOf attribute to your class, such as ExtensionOf(classStr(RetailTransactionServiceEx).</span></span> <span data-ttu-id="4c750-140">つまり、RetailTransactionServiceEx からクラスが拡張されます。</span><span class="sxs-lookup"><span data-stu-id="4c750-140">This means that the class is extending from the RetailTransactionServiceEx.</span></span>

11. <span data-ttu-id="4c750-141">コード エディターで、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="4c750-141">In the code editor, add the following code.</span></span> 

    ```C#
    [ExtensionOf(classStr(RetailTransactionServiceEx))]
    final class ContosoRetailTransactionServiceSample
    {
    }
    ``` 

12. <span data-ttu-id="4c750-142">クラス内部で、カスタム ロジックを実行する新しいメソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="4c750-142">Inside the class, add a new method to do your custom logic.</span></span> <span data-ttu-id="4c750-143">これは、カスタム ロジックを実行するために CRT から呼び出すメソッドです。</span><span class="sxs-lookup"><span data-stu-id="4c750-143">This is the method that you will call from CRT to do the custom logic.</span></span>

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
13. <span data-ttu-id="4c750-144">ソリューション エクスプローラーで、プロジェクトを右クリックしてから **ビルド** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c750-144">In Solution Explorer, right-click the project, and then click **Build**.</span></span>

<span data-ttu-id="4c750-145">新しい拡張メソッドを作成した後は、プロジェクトが展開されます。</span><span class="sxs-lookup"><span data-stu-id="4c750-145">After you've finished building your new extension methods, the project will be deployed.</span></span>

## <a name="call-the-new-method-from-the-crt"></a><span data-ttu-id="4c750-146">CRT から新しいメソッドを呼び出す</span><span class="sxs-lookup"><span data-stu-id="4c750-146">Call the new method from the CRT</span></span>
1.  <span data-ttu-id="4c750-147">Commerce runtime (CRT) 拡張機能に、Microsoft.Dynamics.Commerce.Runtime.RealtimeServices.Messages の nuget パッケージがまだ追加されていない場合は、それを含めます。</span><span class="sxs-lookup"><span data-stu-id="4c750-147">In your commerce runtime (CRT) extension, include the Microsoft.Dynamics.Commerce.Runtime.RealtimeServices.Messages nuget package, if it hasn't already been added.</span></span>
2.  <span data-ttu-id="4c750-148">新しいメソッドを呼び出すには、次のサンプル コードを使用します。</span><span class="sxs-lookup"><span data-stu-id="4c750-148">Use the following sample code to call the new method.</span></span>

    ```C#
        
            InvokeExtensionMethodRealtimeRequest extensionRequest = new InvokeExtensionMethodRealtimeRequest("SerialCheck", "123");
            InvokeExtensionMethodRealtimeResponse response = await request.RequestContext.ExecuteAsync<InvokeExtensionMethodRealtimeResponse>   (extensionRequest).ConfigureAwait(false);
                ReadOnlyCollection<object> results = response.Result;
                
                string resValue = (string)results[0];       
    ```

3.  <span data-ttu-id="4c750-149">results オブジェクトからは、リアルタイム サービスからの応答値を読み取ることができます。</span><span class="sxs-lookup"><span data-stu-id="4c750-149">From the results object, you can read the response values from Real-time Service.</span></span>
4.  <span data-ttu-id="4c750-150">CRT フレームワーク コードは、成功/失敗の状態を確認し、CDX メソッドから返された値に基づいてエラー メッセージを提供します。</span><span class="sxs-lookup"><span data-stu-id="4c750-150">The CRT framework code  will check the success/failure state and provide an error message based on the values returned form the CDX methods.</span></span> <span data-ttu-id="4c750-151">必要に応じて、拡張機能コードでこれをキャッチし、追加のロジックを提供することができます。</span><span class="sxs-lookup"><span data-stu-id="4c750-151">If required, the extension code can catch this and provide additional logic.</span></span>  

    > [!NOTE]
    > <span data-ttu-id="4c750-152">**InvokeExtensionMethodRealtimeRequest** メソッドは 2 つのパラメーターを取ります。</span><span class="sxs-lookup"><span data-stu-id="4c750-152">The **InvokeExtensionMethodRealtimeRequest** method takes two parameters.</span></span> <span data-ttu-id="4c750-153">1 つのパラメ ーターはリアルタイム サービス メソッド名であり、その他はパラメータの一覧を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c750-153">One parameter is the Real-time Service method name, and the other is the list of parameters that should be used.</span></span> <span data-ttu-id="4c750-154">渡されるメソッド名は、**ContosoRetailTransactionServiceSample** クラスで作成したメソッド名と同じにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c750-154">The method name that is passed should be the same as the method name that you created in the **ContosoRetailTransactionServiceSample** class.</span></span>
    
 ```
  public InvokeExtensionMethodRealtimeRequest(string methodName, params object[] parameters)
            : base(methodName, parameters)
        {
        }
 ```

## <a name="cdx-offline"></a><span data-ttu-id="4c750-155">CDX オフライン</span><span class="sxs-lookup"><span data-stu-id="4c750-155">CDX offline</span></span>

<span data-ttu-id="4c750-156">HQ に接続されていない場合、クライアント/Retail Server は CDX メソッドを呼び出すことができません。</span><span class="sxs-lookup"><span data-stu-id="4c750-156">When there is no connectivity to the HQ, client/Retail Server will not be able to call the CDX method.</span></span> <span data-ttu-id="4c750-157">この場合、拡張機能コードは次のベスト プラクティスに従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c750-157">In this case, the extension code should follow the best practice mentioned below:</span></span>

-   <span data-ttu-id="4c750-158">CDX メソッドを呼び出す前に、CRT がオンライン (Retail Server) データベースまたはオフライン (ローカル) データベースに接続されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="4c750-158">Check before calling the CDX method  to determine if CRT is connected to the online (Retail server) or the offline (local) database.</span></span> <span data-ttu-id="4c750-159">この操作は、POS および CRT から行うことができ ます。</span><span class="sxs-lookup"><span data-stu-id="4c750-159">This can be done both in POS and CRT.</span></span>

### <a name="how-to-check-the-connection-status"></a><span data-ttu-id="4c750-160">接続ステータスを確認する方法</span><span class="sxs-lookup"><span data-stu-id="4c750-160">How to check the connection status</span></span>

<span data-ttu-id="4c750-161">**POS**</span><span class="sxs-lookup"><span data-stu-id="4c750-161">**POS**</span></span>

<span data-ttu-id="4c750-162">**GetConnectionStatusClientRequest** POS API を使用します。</span><span class="sxs-lookup"><span data-stu-id="4c750-162">Use the **GetConnectionStatusClientRequest** POS API.</span></span>

<span data-ttu-id="4c750-163">**CRT**</span><span class="sxs-lookup"><span data-stu-id="4c750-163">**CRT**</span></span>

```C#
if(request.RequestContext.Runtime.Configuration.IsMasterDatabaseConnectionString)
{ }
```

-   <span data-ttu-id="4c750-164">CDX メソッドへの接続に失敗した場合には、HQ に接続していない場合は操作を実行できない、または CDX メソッドに接続されていない状態でこの操作をする場合には軽減ロジックを実行する必要がある、というエラー メッセージが表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="4c750-164">If the connection to the CDX method failed, an error message might display saying that the operation cannot be performed if there is no connectivity to HQ or that you need to have mitigation logic if this operation needs to work if there is no connectivity to the CDX method.</span></span>
