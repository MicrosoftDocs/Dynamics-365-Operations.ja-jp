---
title: Commerce Rumtime (CRT) の拡張機能とトリガー
description: このトピックでは、Microsoft Dynamics 365 Commerce Runtime (CRT) のトリガー サポートについて説明します。 CRT は、すべての要求に対してプレ トリガーおよびポスト トリガーをサポートしています。
author: RobinARH
manager: AnnBe
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 17731
ms.assetid: 2d6ec331-b266-4dbc-97c5-db2919b662dc
ms.search.region: Global
ms.search.industry: Retail
ms.author: sijoshi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: ef086eb954da6cf1b08948b843008c26ec32c65d
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/20/2020
ms.locfileid: "3711856"
---
# <a name="commerce-runtime-crt-extensibility-and-triggers"></a><span data-ttu-id="4cfe5-104">Commerce Rumtime (CRT) の拡張機能とトリガー</span><span class="sxs-lookup"><span data-stu-id="4cfe5-104">Commerce runtime (CRT) extensibility and triggers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4cfe5-105">このトピックでは、Dynamics 365 Commerce Runtime (CRT) のトリガー サポートについて説明します。</span><span class="sxs-lookup"><span data-stu-id="4cfe5-105">This topic explains trigger support for the Dynamics 365 commerce runtime (CRT).</span></span> <span data-ttu-id="4cfe5-106">CRT は、すべての要求に対してプレ トリガーおよびポスト トリガーをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="4cfe5-106">CRT supports pre-triggers and post-triggers for every request.</span></span>

## <a name="crt-trigger-overview"></a><span data-ttu-id="4cfe5-107">CRT トリガーの概要</span><span class="sxs-lookup"><span data-stu-id="4cfe5-107">CRT trigger overview</span></span>

<span data-ttu-id="4cfe5-108">Commerce Runtime (CRT) トリガーによって CRT のワークフローを拡張でき、全ての CRT リクエストが実行される前後に、ビジネス ロジックに追加できるようにします。</span><span class="sxs-lookup"><span data-stu-id="4cfe5-108">Commerce runtime (CRT) triggers give you a way to extend the CRT workflow, and let you add business logic before and after every CRT request is executed.</span></span> <span data-ttu-id="4cfe5-109">次の 2 つの方法が使用されます。</span><span class="sxs-lookup"><span data-stu-id="4cfe5-109">The following two methods are used:</span></span>

-   <span data-ttu-id="4cfe5-110">**OnExecuting** – このメソッドは、要求が対応する **IRequestHandler** 実装によって処理される前に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="4cfe5-110">**OnExecuting** – This method is invoked before a request has been processed by a corresponding **IRequestHandler** implementation.</span></span>
-   <span data-ttu-id="4cfe5-111">**OnExecuted** – このメソッドは、要求が対応する **IRequestHandler** 実装によって処理された後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="4cfe5-111">**OnExecuted** – This method is invoked after the request has been processed by a corresponding **IRequestHandler** implementation.</span></span>

## <a name="crt-trigger-extension"></a><span data-ttu-id="4cfe5-112">CRT トリガーの拡張</span><span class="sxs-lookup"><span data-stu-id="4cfe5-112">CRT trigger extension</span></span>
<span data-ttu-id="4cfe5-113">トリガーを実装するには、次のコード例に示すように、これらのタスクを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4cfe5-113">To implement a trigger, you must complete these tasks, as shown in the code example that follows:</span></span>

1.  <span data-ttu-id="4cfe5-114">**IRequestTriggerAsync** を実装します。</span><span class="sxs-lookup"><span data-stu-id="4cfe5-114">Implement **IRequestTriggerAsync**.</span></span>
2.  <span data-ttu-id="4cfe5-115">**SupportedRequestTypes** を指定して、トリガーを実行する必要のある要求のタイプを定義します。</span><span class="sxs-lookup"><span data-stu-id="4cfe5-115">Specify **SupportedRequestTypes** to define the request types that the trigger must be executed for.</span></span>
3.  <span data-ttu-id="4cfe5-116">要求の解決前にビジネス ロジックを実行する必要がある場合、トリガーの実装を **OnExecuting** メソッドに記述します。</span><span class="sxs-lookup"><span data-stu-id="4cfe5-116">Write a trigger implementation in the **OnExecuting** method if business logic must be run before the request is addressed.</span></span>
4.  <span data-ttu-id="4cfe5-117">要求の解決後にビジネス ロジックを実行する必要がある場合、トリガーの実装を **OnExecuted** メソッドに記述します。</span><span class="sxs-lookup"><span data-stu-id="4cfe5-117">Write a trigger implementation in the **OnExecuted** method if business logic must be run after the request is addressed.</span></span>

### <a name="sample-trigger-implementation-for-get-customer-data-request"></a><span data-ttu-id="4cfe5-118">顧客データ要求の取得のトリガー実装例。</span><span class="sxs-lookup"><span data-stu-id="4cfe5-118">Sample trigger implementation for Get customer data request:</span></span>

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

### <a name="register-the-extension"></a><span data-ttu-id="4cfe5-119">拡張機能の登録</span><span class="sxs-lookup"><span data-stu-id="4cfe5-119">Register the extension</span></span>

<span data-ttu-id="4cfe5-120">拡張ライブラリを **...\RetailServer\webroot\bin\ext フォルダー**にコピーして貼り付け、構成セクションのカスタム拡張ライブラリ情報を含む **commerceRuntime.ext.config** ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="4cfe5-120">Copy and paste the extension library to **...\RetailServer\webroot\bin\ext folder** and update the **commerceRuntime.ext.config** file with the custom extension library information under composition section.</span></span> <span data-ttu-id="4cfe5-121">この例では、**Contoso.Commerce.Runtime.Services** はカスタムの拡張機能名です。</span><span class="sxs-lookup"><span data-stu-id="4cfe5-121">In this example, **Contoso.Commerce.Runtime.Services** is the  custom extension name.</span></span>
    <add source="assembly" value="Contoso.Commerce.Runtime.Services" /> 

<span data-ttu-id="4cfe5-122">CRT 拡張機能がオフライン モードで動作するためには、構成セクションの下にある拡張ライブラリ情報で、**...\Microsoft Dynamics 365\70\Retail Modern POS\ClientBroker\ext\CommerceRuntime.MPOSOffline.ext.config** を更新してください。</span><span class="sxs-lookup"><span data-stu-id="4cfe5-122">For the CRT extension to work in offline mode, update **...\Microsoft Dynamics 365\70\Retail Modern POS\ClientBroker\ext\CommerceRuntime.MPOSOffline.ext.config** with the extension library information under the composition section.</span></span> <span data-ttu-id="4cfe5-123">次に、拡張ライブラリを **...\Microsoft Dynamics 365\70\Retail Modern POS\ClientBroker\ext** にコピーし貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="4cfe5-123">Then copy and paste the extension library to **...\Microsoft Dynamics 365\70\Retail Modern POS\ClientBroker\ext**.</span></span>

### <a name="debugging-crt"></a><span data-ttu-id="4cfe5-124">CRT のデバッグ</span><span class="sxs-lookup"><span data-stu-id="4cfe5-124">Debugging CRT</span></span>

<span data-ttu-id="4cfe5-125">POS から CRT をデバッグするには、POS が Retail Server に接続されているときに、CRT 拡張プロジェクトを、w3wp.exe (Retail Server の IIS プロセス) に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="4cfe5-125">To debug CRT from POS, attach the CRT extension project to the w3wp.exe (IIS process for Retail server) when POS is connected to Retail server.</span></span> <span data-ttu-id="4cfe5-126">オフライン モードの場合は、dllhost.exe プロセスに CRT 拡張プロジェクトを関連付けます。</span><span class="sxs-lookup"><span data-stu-id="4cfe5-126">For offline mode, attach the CRT extension project to the dllhost.exe process.</span></span>
