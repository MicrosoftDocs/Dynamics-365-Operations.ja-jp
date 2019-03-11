---
title: Commerce Rumtime (CRT) の拡張機能とトリガー
description: この記事では、Microsoft Dynamics AX commerce ランタイム (CRT) のトリガー サポートについて説明します。 CRTは、すべての要求に対してプレトリガーおよびポストトリガーをサポートしています。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 17731
ms.assetid: 2d6ec331-b266-4dbc-97c5-db2919b662dc
ms.search.region: Global
ms.search.industry: Retail
ms.author: sijoshi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 23998cfead02ad1dd514c373e4d7ec42d0327b3c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368773"
---
# <a name="commerce-runtime-crt-extensibility-and-triggers"></a><span data-ttu-id="d6a48-104">Commerce Rumtime (CRT) の拡張機能とトリガー</span><span class="sxs-lookup"><span data-stu-id="d6a48-104">Commerce runtime (CRT) extensibility and triggers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d6a48-105">この記事では、Dynamics 365 for Retail commerce ランタイム (CRT) のトリガー サポートについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d6a48-105">This article explains trigger support for the Dynamics 365 for Retail commerce runtime (CRT).</span></span> <span data-ttu-id="d6a48-106">CRTは、すべての要求に対してプレトリガーおよびポストトリガーをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="d6a48-106">CRT supports pre-triggers and post-triggers for every request.</span></span>

## <a name="crt-trigger-overview"></a><span data-ttu-id="d6a48-107">CRT トリガーの概要</span><span class="sxs-lookup"><span data-stu-id="d6a48-107">CRT trigger overview</span></span>

<span data-ttu-id="d6a48-108">Commerce Runtime (CRT) トリガーによって CRT のワークフローを拡張でき、全ての CRT リクエストが実行される前後に、ビジネス ロジックに追加できるようにします。</span><span class="sxs-lookup"><span data-stu-id="d6a48-108">Commerce runtime (CRT) triggers give you a way to extend the CRT workflow, and let you add business logic before and after every CRT request is executed.</span></span> <span data-ttu-id="d6a48-109">次の 2 つの方法が使用されます。</span><span class="sxs-lookup"><span data-stu-id="d6a48-109">The following two methods are used:</span></span>

-   <span data-ttu-id="d6a48-110">**OnExecuting** – このメソッドは、要求が対応する **IRequestHandler** 実装によって処理される前に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d6a48-110">**OnExecuting** – This method is invoked before a request has been processed by a corresponding **IRequestHandler** implementation.</span></span>
-   <span data-ttu-id="d6a48-111">**OnExecuted** – このメソッドは、要求が対応する **IRequestHandler** 実装によって処理された後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d6a48-111">**OnExecuted** – This method is invoked after the request has been processed by a corresponding **IRequestHandler** implementation.</span></span>

## <a name="crt-trigger-interface"></a><span data-ttu-id="d6a48-112">CRT トリガー インターフェイス</span><span class="sxs-lookup"><span data-stu-id="d6a48-112">CRT trigger interface</span></span>
<span data-ttu-id="d6a48-113">トリガーを実装するには、次のコード例に示すように、これらのタスクを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d6a48-113">To implement a trigger, you must complete these tasks, as shown in the code example that follows:</span></span>

1.  <span data-ttu-id="d6a48-114">**IRequestTrigger** を実装します。</span><span class="sxs-lookup"><span data-stu-id="d6a48-114">Implement **IRequestTrigger**.</span></span>
2.  <span data-ttu-id="d6a48-115">**SupportedRequestTypes** を指定して、トリガーを実行する必要のある要求のタイプを定義します。</span><span class="sxs-lookup"><span data-stu-id="d6a48-115">Specify **SupportedRequestTypes** to define the request types that the trigger must be executed for.</span></span>
3.  <span data-ttu-id="d6a48-116">要求の解決前にビジネス ロジックを実行する必要がある場合、トリガーの実装を **OnExecuting** メソッドに記述します。</span><span class="sxs-lookup"><span data-stu-id="d6a48-116">Write a trigger implementation in the **OnExecuting** method if business logic must be run before the request is addressed.</span></span>
4.  <span data-ttu-id="d6a48-117">要求の解決後にビジネス ロジックを実行する必要がある場合、トリガーの実装を **OnExecuted** メソッドに記述します。</span><span class="sxs-lookup"><span data-stu-id="d6a48-117">Write a trigger implementation in the **OnExecuted** method if business logic must be run after the request is addressed.</span></span>

<!-- -->

    /// <summary>
    /// The interface for request trigger.
    /// </summary>
    public interface IRequestTrigger
    {
        /// <summary>
        /// Gets the collection of request types supported by this trigger.
        /// </summary>
        /// <remarks>If null or empty collection returned trigger will be called for all request.</remarks>
        IEnumerable<Type> SupportedRequestTypes { get; }
        /// <summary>
        /// Invoked before request has been processed by <see cref="IRequestHandler"/>.
        /// </summary>
        /// <param name="request">The incoming request message.</param>
        void OnExecuting(Request request);
        /// <summary>
        /// Invoked after request has been processed by <see cref="IRequestHandler"/>.
        /// </summary>
        /// <param name="request">The request message processed by handler.</param>
        /// <param name="response">The response message generated by handler.</param>
        void OnExecuted(Request request, Response response);
    }

    Sample trigger implemntation for Get customer data request:

            public class GetCustomerTriggers : IRequestTrigger
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
            /// Post trigger code to retrieve extension properties.
            /// </summary>
            /// <param name="request">The request.</param>
            /// <param name="response">The response.</param>
            public void OnExecuted(Request request, Response response)
            {
                ThrowIf.Null(request, "request");
                ThrowIf.Null(response, "response");

                //Custom logic
            }

            /// <summary>
            /// Pre trigger code.
            /// </summary>
            /// <param name="request">The request.</param>
            public void OnExecuting(Request request)
            {
                //Custom logic
            }
        }

## <a name="trigger-commerceruntimeconfig-updates-for-70"></a><span data-ttu-id="d6a48-118">7.0 の CommerceRunTime.config 更新プログラムをトリガーする</span><span class="sxs-lookup"><span data-stu-id="d6a48-118">Trigger CommerceRunTime.config updates for 7.0</span></span>
<span data-ttu-id="d6a48-119">CRT を拡張するときは、ユーザー独自のアセンブリ内で拡張機能を記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d6a48-119">When you extend the CRT, you must write your extension in your own assembly.</span></span> <span data-ttu-id="d6a48-120">トリガー拡張子をアセンブリに書き込んだ後、Retail サーバー bin フォルダーに拡張子ライブラリをコピーし、実行時にトリガーがロードされるように、CRT の commerceRuntime.config ファイルの**合成**セクションに入力を追加します。</span><span class="sxs-lookup"><span data-stu-id="d6a48-120">After you write the trigger extension in your assembly, you must copy the extension library to the Retail server bin folder and add an entry in the **composition** section of the commerceRuntime.config file for the CRT, so that the trigger is loaded at run time.</span></span> <span data-ttu-id="d6a48-121">次の例は、**CRTExtensionTrigger** アセンブリ内のトリガー実装のエントリを含む .config ファイルを示しています。</span><span class="sxs-lookup"><span data-stu-id="d6a48-121">The following example shows a .config file that includes an entry for a trigger implementation in the **CRTExtensionTrigger** assembly.</span></span> 

<span data-ttu-id="d6a48-122">[![CRTExtensionTrigger](./media/crtextensiontrigger-1024x489.png)](./media/crtextensiontrigger.png)</span><span class="sxs-lookup"><span data-stu-id="d6a48-122">[![CRTExtensionTrigger](./media/crtextensiontrigger-1024x489.png)](./media/crtextensiontrigger.png)</span></span>

<span data-ttu-id="d6a48-123">オフライン モードで作業する CRT 拡張機能については、合成セクションの拡張ライブラリ情報で **...\Microsoft Dynamics 365\70\Retail Modern POS\ClientBroker\CommerceRuntime.MPOSOffline.config** を更新し、その拡張ライブラリをコピーして **...\Microsoft Dynamics 365\70\Retail Modern POS\ClientBroker** に貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="d6a48-123">For the CRT extension to work in offline mode update **...\Microsoft Dynamics 365\70\Retail Modern POS\ClientBroker\CommerceRuntime.MPOSOffline.config** with the extension library information under the composition section and copy and paste the extension library to **...\Microsoft Dynamics 365\70\Retail Modern POS\ClientBroker**.</span></span>

## <a name="trigger-commerceruntimeconfig-updates-for-71-with-may-2017-monthly-update-72-and-73"></a><span data-ttu-id="d6a48-124">7.1 (2017 年 5 月の月次更新)、7.2 および 7.3 の CommerceRunTime.config 更新プログラムのトリガー</span><span class="sxs-lookup"><span data-stu-id="d6a48-124">Trigger CommerceRunTime.config updates for 7.1 (with May 2017 monthly update), 7.2 and 7.3</span></span>
<span data-ttu-id="d6a48-125">拡張ライブラリを **...\RetailServer\webroot\bin\ext フォルダー**にコピーして貼り付け、構成セクションのカスタム拡張ライブラリ情報を含む **commerceRuntime.ext.config** ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="d6a48-125">Copy and paste the extension library to **...\RetailServer\webroot\bin\ext folder** and update the **commerceRuntime.ext.config** file with the custom extension library information under composition section.</span></span> <span data-ttu-id="d6a48-126">この例では、**Contoso.Commerce.Runtime.Services** はカスタムの拡張機能名です。</span><span class="sxs-lookup"><span data-stu-id="d6a48-126">In this example, **Contoso.Commerce.Runtime.Services** is the  custom extension name.</span></span>
    <add source="assembly" value="Contoso.Commerce.Runtime.Services" /> 

<span data-ttu-id="d6a48-127">オフライン モードで作業する CRT 拡張機能については、合成セクションの拡張ライブラリ情報で **...\Microsoft Dynamics 365\70\Retail Modern POS\ClientBroker\extCommerceRuntime.MPOSOffline.ext.config** を更新し、その拡張ライブラリをコピーして **...\Microsoft Dynamics 365\70\Retail Modern POS\ClientBroker\ext** に貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="d6a48-127">For the CRT extension to work in offline mode update **...\Microsoft Dynamics 365\70\Retail Modern POS\ClientBroker\extCommerceRuntime.MPOSOffline.ext.config** with the extension library information under the composition section and copy and paste the extension library to **...\Microsoft Dynamics 365\70\Retail Modern POS\ClientBroker\ext**.</span></span>
