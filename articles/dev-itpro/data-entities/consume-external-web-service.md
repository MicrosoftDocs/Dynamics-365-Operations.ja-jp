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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: a1c33f794c4be99f421ac4c4a43cbc45f1e4cd6e
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="consume-external-web-services-in-finance-and-operations"></a>Finance and Operations における外部 Web サービスの使用

[!include [banner](../includes/banner.md)]

新しいクラス ライブラリを Microsoft Dynamics 365 for Finance and Operations に追加することにより、 Web サービスを使用することができます。 Microsoft Dynamics AX 2012 では、Microsoft Visual Studio プロジェクトを参照として追加して **Aif::CreateServiceClient** を使用することで、X++ コードから Web サービスを使用できました。 このシナリオはサポートされていますが、ステップが変更されています。 アプリケーション統合フレームワーク (AIF) は現在サポートされていません。 

次の手順は、X++ から外部 StockQuote サービスを使用する方法を示しています。

1.  Visual Studio で新しいクラス ライブラリ プロジェクトを作成し、**ExternalServiceLibrary.csproj** という名前を付けます。
2.  Visual Studio プロジェクトで、外部 Web サービスへのサービスの参照を追加します: http:\//www.webservicex.net/stockquote.asmx。
3.  新しい静的クラスを作成し、次の例に示すように StockQuote サービス操作をラップします。

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
4. プロジェクトを構築します。 バイナリ ExternalServiceLibrary.dll が作成されます。
5. Visual Studio で新しい Dynamics プロジェクトを作成します。
6. 参照として **ExternalServiceLibrary.dll** を追加します。
7. X++ クラスでは、ExternalesrviceLibrary.dll で参照されていた外部 Web サービスを使用することができます。
   ```
   public static void main(Args _args)
    {
      info(ServiceLibrary.StockQuoteClass::GetQuote("MSFT"));
     }
   ```

