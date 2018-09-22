---
title: "Finance and Operations における外部 Web サービスの使用"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations で外部 Web サービスを使用する方法について説明します。"
author: Sunil-Garg
manager: AnnBe
ms.date: 11/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 21311
ms.assetid: 5ff7fd93-1bb8-4883-9cca-c8c42ddc1746
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: cf7a214fd77a55da46b6281aaf64e6883a3e3a42
ms.contentlocale: ja-jp
ms.lasthandoff: 08/13/2018

---

# <a name="consume-external-web-services-in-finance-and-operations"></a><span data-ttu-id="aac40-103">Finance and Operations における外部 Web サービスの使用</span><span class="sxs-lookup"><span data-stu-id="aac40-103">Consume external web services in Finance and Operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aac40-104">新しいクラス ライブラリを Microsoft Dynamics 365 for Finance and Operations に追加することにより、 Web サービスを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="aac40-104">You can consume web services by adding new class libraries to Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="aac40-105">Microsoft Dynamics AX 2012 では、Microsoft Visual Studio プロジェクトを参照として追加して **Aif::CreateServiceClient** を使用することで、X++ コードから Web サービスを使用できました。</span><span class="sxs-lookup"><span data-stu-id="aac40-105">In Microsoft Dynamics AX 2012, you could consume web services from X++ code by adding Microsoft Visual Studio projects as a reference and by using **Aif::CreateServiceClient**.</span></span> <span data-ttu-id="aac40-106">このシナリオはサポートされていますが、ステップが変更されています。</span><span class="sxs-lookup"><span data-stu-id="aac40-106">This scenario is supported, but the steps have changed.</span></span> <span data-ttu-id="aac40-107">アプリケーション統合フレームワーク (AIF) は現在サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="aac40-107">Application Integration Framework (AIF) is no longer supported.</span></span>

<span data-ttu-id="aac40-108">次の手順は、X++ から外部 StockQuote サービスを使用する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="aac40-108">The following steps show how to consume an external StockQuote service from X++.</span></span>

1. <span data-ttu-id="aac40-109">Visual Studio で新しいクラス ライブラリ プロジェクトを作成し、**ExternalServiceLibrary.csproj** という名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="aac40-109">Create a new Class Library project in Visual Studio, and name it **ExternalServiceLibrary.csproj**.</span></span>
2. <span data-ttu-id="aac40-110">Visual Studio プロジェクトで、外部 Web サービスへのサービスの参照を追加します: `http://www.webservicex.net/stockquote.asmx`。</span><span class="sxs-lookup"><span data-stu-id="aac40-110">In the Visual Studio project, add a service reference to the external web service: `http://www.webservicex.net/stockquote.asmx`.</span></span>
3. <span data-ttu-id="aac40-111">新しい静的クラスを作成し、次の例に示すように StockQuote サービス操作をラップします。</span><span class="sxs-lookup"><span data-stu-id="aac40-111">Create a new static class, and wrap the StockQuote service operation as shown in the following example.</span></span>

    ```
    public static string GetQuote(string s)
    {
        var binding = new System.ServiceModel.BasicHttpBinding();
        var endpointAddress = new EndpointAddress("http://www.webservicex.net/stockquote.asmx");
        ServiceLibrary.QuoteReference.StockQuoteSoapClient client = new ServiceLibrary.QuoteReference.StockQuoteSoapClient(binding, endpointAddress);

        //GetQuote is the operation on the StockQuote service
        return client.GetQuote("MSFT");
    }
    ```

4. <span data-ttu-id="aac40-112">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="aac40-112">Build the project.</span></span> <span data-ttu-id="aac40-113">バイナリ ExternalServiceLibrary.dll が作成されます。</span><span class="sxs-lookup"><span data-stu-id="aac40-113">The binary ExternalServiceLibrary.dll is created.</span></span>
5. <span data-ttu-id="aac40-114">Visual Studio で新しい Dynamics プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="aac40-114">Create a new Dynamics project in Visual Studio.</span></span>
6. <span data-ttu-id="aac40-115">参照として **ExternalServiceLibrary.dll** を追加します。</span><span class="sxs-lookup"><span data-stu-id="aac40-115">Add **ExternalServiceLibrary.dll** as a reference.</span></span>
7. <span data-ttu-id="aac40-116">X++ クラスでは、ExternalesrviceLibrary.dll で参照されていた外部 Web サービスを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="aac40-116">In the X++ class, you can use the external web services that were referenced in ExternalesrviceLibrary.dll.</span></span>

    ```
    public static void main(Args _args)
    {
        info(ServiceLibrary.StockQuoteClass::GetQuote("MSFT"));
    }
    ```

