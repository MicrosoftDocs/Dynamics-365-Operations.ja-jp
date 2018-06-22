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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 76e35bd52ecaec7b60a2c75f7aef8ecac92d2d56
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="extend-commerce-data-exchange---real-time-service"></a><span data-ttu-id="6a25a-104">Commerce Data Exchange を拡張 - Real-time Service</span><span class="sxs-lookup"><span data-stu-id="6a25a-104">Extend Commerce Data Exchange - Real-time Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6a25a-105">この記事では、RetailTransactionServiceEx クラスに拡張メソッドを追加して、Commerce Data Exchange - リアルタイム サービスを拡張する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6a25a-105">This article explains how you can extend Commerce Data Exchange -  Real-time service by adding extension methods to the RetailTransactionServiceEx class.</span></span> <span data-ttu-id="6a25a-106">リアルタイム サービスは、Retail クライアントがリアルタイムで小売機能を操作できるようします。</span><span class="sxs-lookup"><span data-stu-id="6a25a-106">Real-time Service enables retail clients to interact with retail functionality in real time.</span></span>

<span data-ttu-id="6a25a-107">Commerce Data Exchange: リアルタイム サービスを拡張するには、**RetailTransactionServiceEx** クラスで新しいメソッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="6a25a-107">To extend Commerce Data Exchange: Real-time Service, you create a new method in the **RetailTransactionServiceEx** class.</span></span> <span data-ttu-id="6a25a-108">このメソッドは、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a25a-108">This method must meet the following criteria:</span></span>

-   <span data-ttu-id="6a25a-109">このメソッドは、パブリック静的メソッドでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="6a25a-109">The method must be a public static method.</span></span>
-   <span data-ttu-id="6a25a-110">戻り値は、長さが 2 以上のコンテナーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a25a-110">The return value must be a container that has a length of 2 or more.</span></span> <span data-ttu-id="6a25a-111">最初の 2 つの要素は、メソッド呼び出しが成功したかどうかを示すブール値と、コメントまたはエラー メッセージに使用できる文字列値でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="6a25a-111">The first two elements must be a Boolean value that indicates whether the method call was successful, and a string value that you can use for a comment or error message.</span></span> <span data-ttu-id="6a25a-112">コンテナー内の他の項目は任意の型になることができ、入れ子になったコンテナーにもなれます。</span><span class="sxs-lookup"><span data-stu-id="6a25a-112">The other items in the container can be of any type, and they can even be nested containers.</span></span>
-   <span data-ttu-id="6a25a-113">メソッドのパラメーターは、次のプリミティブ型のいずれかでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="6a25a-113">The method parameters must be one of the following primitive types:</span></span>
    -   <span data-ttu-id="6a25a-114">ブール型</span><span class="sxs-lookup"><span data-stu-id="6a25a-114">Boolean</span></span>
    -   <span data-ttu-id="6a25a-115">日付</span><span class="sxs-lookup"><span data-stu-id="6a25a-115">date</span></span>
    -   <span data-ttu-id="6a25a-116">int</span><span class="sxs-lookup"><span data-stu-id="6a25a-116">int</span></span>
    -   <span data-ttu-id="6a25a-117">int64</span><span class="sxs-lookup"><span data-stu-id="6a25a-117">int64</span></span>
    -   <span data-ttu-id="6a25a-118">str</span><span class="sxs-lookup"><span data-stu-id="6a25a-118">str</span></span>
    -   <span data-ttu-id="6a25a-119">guid</span><span class="sxs-lookup"><span data-stu-id="6a25a-119">guid</span></span>
    -   <span data-ttu-id="6a25a-120">実数</span><span class="sxs-lookup"><span data-stu-id="6a25a-120">Real</span></span>

## <a name="create-and-call-a-new-extension-method"></a><span data-ttu-id="6a25a-121">新しい拡張メソッドの作成と呼び出し</span><span class="sxs-lookup"><span data-stu-id="6a25a-121">Create and call a new extension method</span></span>
1. <span data-ttu-id="6a25a-122">Microsoft Visual Studio を開始します。</span><span class="sxs-lookup"><span data-stu-id="6a25a-122">Start Microsoft Visual Studio.</span></span>
2. <span data-ttu-id="6a25a-123"><strong>Dynamics 365 **メニューで、**モデル管理</strong> &gt; <strong>モデルの作成</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a25a-123">On the <strong>Dynamics 365 **menu, click **Model management</strong> &gt; <strong>Create model</strong>.</span></span>
3. <span data-ttu-id="6a25a-124">**モデルの作成**ダイアログ ボックスに、次の詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="6a25a-124">In the **Create model** dialog box, enter the following details.</span></span>
   -   <span data-ttu-id="6a25a-125">**モデル名**: Contoso</span><span class="sxs-lookup"><span data-stu-id="6a25a-125">**Model name**: Contoso</span></span>
   -   <span data-ttu-id="6a25a-126">**モデル発行元**: Contoso</span><span class="sxs-lookup"><span data-stu-id="6a25a-126">**Model publisher**: Contoso</span></span>
   -   <span data-ttu-id="6a25a-127">**レイヤー**: USR (関連するレイヤーを選択)</span><span class="sxs-lookup"><span data-stu-id="6a25a-127">**Layer**: USR (Select the relevant layer)</span></span>
   -   <span data-ttu-id="6a25a-128">**バージョン**:1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="6a25a-128">**Version**: 1.0.0.0</span></span>
   -   <span data-ttu-id="6a25a-129">**モデルの表示名**: Contoso</span><span class="sxs-lookup"><span data-stu-id="6a25a-129">**Model display name**: Contoso</span></span>

4. <span data-ttu-id="6a25a-130">**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a25a-130">Click **Next**.</span></span>
5. <span data-ttu-id="6a25a-131">ダイアログ ボックスで、**既存のパッケージを選択**を選択してから、一覧で**アプリケーション スイート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a25a-131">In the dialog, select **Select existing package**, and then select **Application Suite** in the list.</span></span>
6. <span data-ttu-id="6a25a-132">**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a25a-132">Click **Next**.</span></span>
7. <span data-ttu-id="6a25a-133">**完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a25a-133">Click **Finish**.</span></span>
8. <span data-ttu-id="6a25a-134">**新しいプロジェクト** ダイアログ ボックスに、**ContosoRetailTransactionServiceEx** というプロジェクト名を入力します。</span><span class="sxs-lookup"><span data-stu-id="6a25a-134">In the **New project** dialog box, enter **ContosoRetailTransactionServiceEx** as the project name.</span></span>
9. <span data-ttu-id="6a25a-135">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a25a-135">Click **OK**.</span></span>
10. <span data-ttu-id="6a25a-136">アプリケーション エクスプローラーで、**コード** ノードを展開して**クラス**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a25a-136">In Application Explorer, expand the **Code** node, and select **Classes**.</span></span>
11. <span data-ttu-id="6a25a-137">**RetailTransactionServiceEx** クラスを右クリックし、、**カスタマイズ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a25a-137">Right-click the **RetailTransactionServiceEx** class, and then click **Customize**.</span></span>
12. <span data-ttu-id="6a25a-138">コード エディターで、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="6a25a-138">In the code editor, add the following code.</span></span>

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

13. <span data-ttu-id="6a25a-139">ソリューション エクスプローラーで、プロジェクトを右クリックしてから**ビルド**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a25a-139">In Solution Explorer, right-click the project, and then click **Build**.</span></span>

<span data-ttu-id="6a25a-140">新しい拡張メソッドを作成した後は、プロジェクトが展開されます。</span><span class="sxs-lookup"><span data-stu-id="6a25a-140">After you've finished building your new extension methods, the project will be deployed.</span></span>

## <a name="call-the-new-method-from-the-crt"></a><span data-ttu-id="6a25a-141">CRT から新しいメソッドを呼び出す</span><span class="sxs-lookup"><span data-stu-id="6a25a-141">Call the new method from the CRT</span></span>
1.  <span data-ttu-id="6a25a-142">Commerce Runtime (CRT) で、Microsoft.Dynamics.Commerce.Runtime.TransactionService.dll への参照が追加されていない場合は追加します。</span><span class="sxs-lookup"><span data-stu-id="6a25a-142">In your commerce runtime (CRT), add a reference to the Microsoft.Dynamics.Commerce.Runtime.TransactionService.dll, if it hasn't already been added.</span></span>
2.  <span data-ttu-id="6a25a-143">新しいメソッドを呼び出すには、次のサンプル コードを使用します。</span><span class="sxs-lookup"><span data-stu-id="6a25a-143">Use the following sample code to call the new method.</span></span>

        TransactionServiceClient transactionService = new TransactionServiceClient(request.RequestContext);
        ReadOnlyCollection serviceResponse = transactionService.InvokeExtensionMethod("SerialCheck", "123");

3.  <span data-ttu-id="6a25a-144">ServiceResponse オブジェクトからは、リアルタイム サービスからの応答値を読み取ることができます。</span><span class="sxs-lookup"><span data-stu-id="6a25a-144">From the serviceResponse object, you can read the response values from Real-time Service.</span></span>

<span data-ttu-id="6a25a-145">**注記:** **InvokeExtensionMethod** メソッドは 2 つのパラメーターを取ります。</span><span class="sxs-lookup"><span data-stu-id="6a25a-145">**Note:** The **InvokeExtensionMethod** method takes two parameters.</span></span> <span data-ttu-id="6a25a-146">1 つのパラメ ーターはリアルタイム サービス メソッド名であり、その他はパラメータの一覧を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a25a-146">One parameter is the Real-time Service method name, and the other is the list of parameters that should be used.</span></span> <span data-ttu-id="6a25a-147">渡されるメソッド名は、**RetailTransactionServiceEx** クラスで作成したメソッド名と同じにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a25a-147">The method name that is passed should be the same as the method name that you created in the **RetailTransactionServiceEx** class.</span></span>




