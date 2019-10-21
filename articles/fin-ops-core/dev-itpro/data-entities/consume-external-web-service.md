---
title: 外部 Web サービスの消費
description: このトピックでは、Microsoft Dynamics 365 Finance and Operations アプリで外部 Web サービスを使用する方法について説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 11/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 21311
ms.assetid: 5ff7fd93-1bb8-4883-9cca-c8c42ddc1746
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b09c625d262aa2ba73064a97a282023167fd7798
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183437"
---
# <a name="consume-external-web-services"></a><span data-ttu-id="ecaa0-103">外部 Web サービスの消費</span><span class="sxs-lookup"><span data-stu-id="ecaa0-103">Consume external web services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ecaa0-104">新しいクラス ライブラリを追加することによって、Web サービスを使用できます。</span><span class="sxs-lookup"><span data-stu-id="ecaa0-104">You can consume web services by adding new class libraries.</span></span> <span data-ttu-id="ecaa0-105">Microsoft Dynamics AX 2012 では、Microsoft Visual Studio プロジェクトを参照として追加し、**Aif::CreateServiceClient** を使用することで、X++ コードから Web サービスを使用できました。</span><span class="sxs-lookup"><span data-stu-id="ecaa0-105">In Microsoft Dynamics AX 2012, you could consume web services from X++ code by adding Microsoft Visual Studio projects as a reference and by using **Aif::CreateServiceClient**.</span></span> <span data-ttu-id="ecaa0-106">このシナリオはサポートされていますが、ステップが変更されています。</span><span class="sxs-lookup"><span data-stu-id="ecaa0-106">This scenario is supported, but the steps have changed.</span></span> <span data-ttu-id="ecaa0-107">アプリケーション統合フレームワーク (AIF) は現在サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="ecaa0-107">Application Integration Framework (AIF) is no longer supported.</span></span>

<span data-ttu-id="ecaa0-108">次の手順は、X++ から外部 StockQuote サービスを使用する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="ecaa0-108">The following steps show how to consume an external StockQuote service from X++.</span></span>

<span data-ttu-id="ecaa0-109">このサンプルの Web サービスの URL は架空のものであることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="ecaa0-109">Note that the web service URL in this sample is fictional.</span></span>  <span data-ttu-id="ecaa0-110">http://www.contoso.net/stockquote.asmx に既知の Web サービスはありません。</span><span class="sxs-lookup"><span data-stu-id="ecaa0-110">There is no known web service at http://www.contoso.net/stockquote.asmx.</span></span>  <span data-ttu-id="ecaa0-111">このコードを機能させるには、それを特定の Web サービスに適応させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="ecaa0-111">To make this code work you will need to adapt it to your specific web service.</span></span>

1. <span data-ttu-id="ecaa0-112">Visual Studio で新しいクラス ライブラリ プロジェクトを作成し、**ExternalServiceLibrary.csproj** という名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="ecaa0-112">Create a new Class Library project in Visual Studio, and name it **ExternalServiceLibrary.csproj**.</span></span>
2. <span data-ttu-id="ecaa0-113">Visual Studio プロジェクトで、外部 Web サービス `http://www.contoso.net/stockquote.asmx` へのサービス参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="ecaa0-113">In the Visual Studio project, add a service reference to the external web service: `http://www.contoso.net/stockquote.asmx`.</span></span>
3. <span data-ttu-id="ecaa0-114">新しい静的クラスを作成し、次の例に示すように StockQuote サービス操作をラップします。</span><span class="sxs-lookup"><span data-stu-id="ecaa0-114">Create a new static class, and wrap the StockQuote service operation as shown in the following example.</span></span>

    ```
    public static string GetQuote(string s)
    {
        var binding = new System.ServiceModel.BasicHttpBinding();
        var endpointAddress = new EndpointAddress("http://www.contoso.net/stockquote.asmx");
        ServiceLibrary.QuoteReference.StockQuoteSoapClient client = new ServiceLibrary.QuoteReference.StockQuoteSoapClient(binding, endpointAddress);

        //GetQuote is the operation on the StockQuote service
        return client.GetQuote("MSFT");
    }
    ```

4. <span data-ttu-id="ecaa0-115">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="ecaa0-115">Build the project.</span></span> <span data-ttu-id="ecaa0-116">バイナリ ExternalServiceLibrary.dll が作成されます。</span><span class="sxs-lookup"><span data-stu-id="ecaa0-116">The binary ExternalServiceLibrary.dll is created.</span></span>
5. <span data-ttu-id="ecaa0-117">Visual Studio で、新しい Dynamics プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="ecaa0-117">Create a new Dynamics project in Visual Studio.</span></span>
6. <span data-ttu-id="ecaa0-118">参照として **ExternalServiceLibrary.dll** を追加します。</span><span class="sxs-lookup"><span data-stu-id="ecaa0-118">Add **ExternalServiceLibrary.dll** as a reference.</span></span>
7. <span data-ttu-id="ecaa0-119">X++ クラスでは、ExternalServiceLibrary.dll で参照されていた外部 Web サービスを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="ecaa0-119">In the X++ class, you can use the external web services that were referenced in ExternalServiceLibrary.dll.</span></span>

    ```
    public static void main(Args _args)
    {
        info(ServiceLibrary.StockQuoteClass::GetQuote("MSFT"));
    }
    ```
