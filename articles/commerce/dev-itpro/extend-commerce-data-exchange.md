---
title: Commerce Data Exchange の拡張 - リアルタイム サービス
description: このトピックでは、RetailTransactionServiceEx クラスに拡張メソッドを追加して、Commerce Data Exchange - リアルタイム サービスを拡張する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 68673
ms.assetid: 72a63836-2908-45fa-b1a6-3b1c499a19a2
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 4e7ef72545249246263816612cf0054ccf36ecc0
ms.sourcegitcommit: 4846ce7248734cc5166a920910d87e4a3282e990
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/15/2020
ms.locfileid: "3815043"
---
# <a name="extend-commerce-data-exchange---real-time-service"></a><span data-ttu-id="32879-103">Commerce Data Exchange の拡張 - リアルタイム サービス</span><span class="sxs-lookup"><span data-stu-id="32879-103">Extend Commerce Data Exchange - Real-time Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="32879-104">このトピックでは、RetailTransactionServiceEx クラスに拡張メソッドを追加して、Commerce Data Exchange (CDX) - リアルタイム サービスを拡張する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="32879-104">This topic explains how you can extend Commerce Data Exchange (CDX) - Real-time service by adding extension methods to the RetailTransactionServiceEx class.</span></span> <span data-ttu-id="32879-105">リアルタイム サービスは、クライアントがリアルタイムでコマース機能を操作できるようします。</span><span class="sxs-lookup"><span data-stu-id="32879-105">Real-time Service enables clients to interact with Commerce functionality in real time.</span></span>

<span data-ttu-id="32879-106">Commerce Data Exchange - リアルタイム サービスを拡張するには、**RetailTransactionServiceEx** クラスで新しいメソッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="32879-106">To extend Commerce Data Exchange - Real-time Service, you create a new method in the **RetailTransactionServiceEx** class.</span></span> <span data-ttu-id="32879-107">このメソッドは、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="32879-107">This method must meet the following criteria:</span></span>

-   <span data-ttu-id="32879-108">このメソッドは、パブリック静的メソッドでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="32879-108">The method must be a public static method.</span></span>
-   <span data-ttu-id="32879-109">戻り値は、長さが 2 以上のコンテナーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="32879-109">The return value must be a container that has a length of 2 or more.</span></span> <span data-ttu-id="32879-110">最初の要素は、メソッド呼び出しが成功したかどうかを示すブール値と、コメントまたはエラー メッセージに使用できる文字列値でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="32879-110">The first element must be a Boolean value that indicates whether the method call was successful, and a string value that you can use for a comment or error message.</span></span> <span data-ttu-id="32879-111">コンテナー内の他の項目は任意の型になることができ、入れ子になったコンテナーにもなれます。</span><span class="sxs-lookup"><span data-stu-id="32879-111">The other items in the container can be of any type, and they can even be nested containers.</span></span>
-   <span data-ttu-id="32879-112">メソッドのパラメーターは、次のプリミティブ型のいずれかでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="32879-112">The method parameters must be one of the following primitive types:</span></span>
    -   <span data-ttu-id="32879-113">ブール型</span><span class="sxs-lookup"><span data-stu-id="32879-113">Boolean</span></span>
    -   <span data-ttu-id="32879-114">日付</span><span class="sxs-lookup"><span data-stu-id="32879-114">date</span></span>
    -   <span data-ttu-id="32879-115">int</span><span class="sxs-lookup"><span data-stu-id="32879-115">int</span></span>
    -   <span data-ttu-id="32879-116">int64</span><span class="sxs-lookup"><span data-stu-id="32879-116">int64</span></span>
    -   <span data-ttu-id="32879-117">str</span><span class="sxs-lookup"><span data-stu-id="32879-117">str</span></span>
    -   <span data-ttu-id="32879-118">guid</span><span class="sxs-lookup"><span data-stu-id="32879-118">guid</span></span>
    -   <span data-ttu-id="32879-119">実績</span><span class="sxs-lookup"><span data-stu-id="32879-119">Real</span></span>

## <a name="create-and-call-a-new-extension-method"></a><span data-ttu-id="32879-120">新しい拡張メソッドの作成と呼び出し</span><span class="sxs-lookup"><span data-stu-id="32879-120">Create and call a new extension method</span></span>
1. <span data-ttu-id="32879-121">Microsoft Visual Studio を起動します。</span><span class="sxs-lookup"><span data-stu-id="32879-121">Start Microsoft Visual Studio.</span></span>
2. <span data-ttu-id="32879-122">**Dynamics 365** メニューで、**モデル管理 > モデルの作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="32879-122">On the **Dynamics 365** menu, click **Model management > Create model**.</span></span>
3. <span data-ttu-id="32879-123">**モデルの作成**ダイアログ ボックスに、次の詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="32879-123">In the **Create model** dialog box, enter the following details.</span></span>
   -   <span data-ttu-id="32879-124">**モデル名** - Contoso</span><span class="sxs-lookup"><span data-stu-id="32879-124">**Model name** - Contoso</span></span>
   -   <span data-ttu-id="32879-125">**モデル発行元** - Contoso</span><span class="sxs-lookup"><span data-stu-id="32879-125">**Model publisher** - Contoso</span></span>
   -   <span data-ttu-id="32879-126">**レイヤー** - USR (関連するレイヤーを選択)</span><span class="sxs-lookup"><span data-stu-id="32879-126">**Layer** - USR (Select the relevant layer)</span></span>
   -   <span data-ttu-id="32879-127">**バージョン** - 1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="32879-127">**Version** - 1.0.0.0</span></span>
   -   <span data-ttu-id="32879-128">**モデルの表示名** - Contoso</span><span class="sxs-lookup"><span data-stu-id="32879-128">**Model display name** - Contoso</span></span>

4. <span data-ttu-id="32879-129">**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="32879-129">Click **Next**.</span></span>
5. <span data-ttu-id="32879-130">ダイアログ ボックスで、**既存のパッケージを選択**を選択してから、一覧で**アプリケーション スイート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="32879-130">In the dialog box, select **Select existing package**, and then select **Application Suite** in the list.</span></span>
6. <span data-ttu-id="32879-131">**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="32879-131">Click **Next**.</span></span>
7. <span data-ttu-id="32879-132">**完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="32879-132">Click **Finish**.</span></span>
8. <span data-ttu-id="32879-133">**新しいプロジェクト** ダイアログ ボックスに、**ContosoRetailTransactionServiceEx** というプロジェクト名を入力します。</span><span class="sxs-lookup"><span data-stu-id="32879-133">In the **New project** dialog box, enter **ContosoRetailTransactionServiceEx** as the project name.</span></span>
9. <span data-ttu-id="32879-134">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="32879-134">Click **OK**.</span></span>
10. <span data-ttu-id="32879-135">プロジェクトを右クリックし、**追加 > 新しい項目** を選択します。</span><span class="sxs-lookup"><span data-stu-id="32879-135">Right-click the project and select **Add > New item**.</span></span> <span data-ttu-id="32879-136">**新しい項目の追加** ウィンドウで、**クラス** を選択し、**ContosoRetailTransactionServiceSample** としてクラスの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="32879-136">In the **Add New Item** window, select **Class** and enter the name of the class as **ContosoRetailTransactionServiceSample**.</span></span>

    <span data-ttu-id="32879-137">Commerce Runtime (CRT) で CDX メソッドを使用するには、ExtensionOf(classStr(RetailTransactionServiceEx) など、ExtensionOf 属性をクラスに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="32879-137">To consume the CDX method in Commerce runtime (CRT) you must add the ExtensionOf attribute to your class, such as ExtensionOf(classStr(RetailTransactionServiceEx).</span></span> <span data-ttu-id="32879-138">つまり、RetailTransactionServiceEx からクラスが拡張されます。</span><span class="sxs-lookup"><span data-stu-id="32879-138">This means that the class is extending from the RetailTransactionServiceEx.</span></span>

11. <span data-ttu-id="32879-139">コード エディターで、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="32879-139">In the code editor, add the following code.</span></span> 

    ```C#
    [ExtensionOf(classStr(RetailTransactionServiceEx))]
    final class ContosoRetailTransactionServiceSample
    {
    }
    ``` 

12. <span data-ttu-id="32879-140">クラス内部で、カスタム ロジックを実行する新しいメソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="32879-140">Inside the class, add a new method to do your custom logic.</span></span> <span data-ttu-id="32879-141">これは、カスタム ロジックを実行するために CRT から呼び出すメソッドです。</span><span class="sxs-lookup"><span data-stu-id="32879-141">This is the method that you will call from CRT to do the custom logic.</span></span>

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
13. <span data-ttu-id="32879-142">ソリューション エクスプローラーで、プロジェクトを右クリックしてから**ビルド**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="32879-142">In Solution Explorer, right-click the project, and then click **Build**.</span></span>

<span data-ttu-id="32879-143">新しい拡張メソッドを作成した後は、プロジェクトが展開されます。</span><span class="sxs-lookup"><span data-stu-id="32879-143">After you've finished building your new extension methods, the project will be deployed.</span></span>

## <a name="call-the-new-method-from-the-crt"></a><span data-ttu-id="32879-144">CRT から新しいメソッドを呼び出す</span><span class="sxs-lookup"><span data-stu-id="32879-144">Call the new method from the CRT</span></span>
1.  <span data-ttu-id="32879-145">Commerce runtime (CRT) 拡張機能に、Microsoft.Dynamics.Commerce.Runtime.RealtimeServices.Messages の nuget パッケージがまだ追加されていない場合は、それを含めます。</span><span class="sxs-lookup"><span data-stu-id="32879-145">In your commerce runtime (CRT) extension, include the Microsoft.Dynamics.Commerce.Runtime.RealtimeServices.Messages nuget package, if it hasn't already been added.</span></span>
2.  <span data-ttu-id="32879-146">新しいメソッドを呼び出すには、次のサンプル コードを使用します。</span><span class="sxs-lookup"><span data-stu-id="32879-146">Use the following sample code to call the new method.</span></span>

    ```C#
        
            InvokeExtensionMethodRealtimeRequest extensionRequest = new InvokeExtensionMethodRealtimeRequest("SerialCheck", "123");
            InvokeExtensionMethodRealtimeResponse response = await request.RequestContext.ExecuteAsync<InvokeExtensionMethodRealtimeResponse>   (extensionRequest).ConfigureAwait(false);
                ReadOnlyCollection<object> results = response.Result;
                
                string resValue = (string)results[0];       
    ```

3.  <span data-ttu-id="32879-147">results オブジェクトからは、リアルタイム サービスからの応答値を読み取ることができます。</span><span class="sxs-lookup"><span data-stu-id="32879-147">From the results object, you can read the response values from Real-time Service.</span></span>
4.  <span data-ttu-id="32879-148">CRT フレームワーク コードは、成功/失敗の状態を確認し、CDX メソッドから返された値に基づいてエラー メッセージを提供します。</span><span class="sxs-lookup"><span data-stu-id="32879-148">The CRT framework code  will check the success/failure state and provide an error message based on the values returned form the CDX methods.</span></span> <span data-ttu-id="32879-149">必要に応じて、拡張機能コードでこれをキャッチし、追加のロジックを提供することができます。</span><span class="sxs-lookup"><span data-stu-id="32879-149">If required, the extension code can catch this and provide additional logic.</span></span>  

    > [!NOTE]
    > <span data-ttu-id="32879-150">**InvokeExtensionMethodRealtimeRequest** メソッドは 2 つのパラメーターを取ります。</span><span class="sxs-lookup"><span data-stu-id="32879-150">The **InvokeExtensionMethodRealtimeRequest** method takes two parameters.</span></span> <span data-ttu-id="32879-151">1 つのパラメ ーターはリアルタイム サービス メソッド名であり、その他はパラメータの一覧を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="32879-151">One parameter is the Real-time Service method name, and the other is the list of parameters that should be used.</span></span> <span data-ttu-id="32879-152">渡されるメソッド名は、**ContosoRetailTransactionServiceSample** クラスで作成したメソッド名と同じにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="32879-152">The method name that is passed should be the same as the method name that you created in the **ContosoRetailTransactionServiceSample** class.</span></span>
    
 ```
  public InvokeExtensionMethodRealtimeRequest(string methodName, params object[] parameters)
            : base(methodName, parameters)
        {
        }
 ```


