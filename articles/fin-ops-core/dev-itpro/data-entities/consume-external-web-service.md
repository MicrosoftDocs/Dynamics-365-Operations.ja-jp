---
title: 外部 Web サービスの消費
description: このトピックでは、Microsoft Dynamics 365 Finance and Operations アプリで外部 Web サービスを使用する方法について説明します。
author: Sunil-Garg
ms.date: 11/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 21311
ms.assetid: 5ff7fd93-1bb8-4883-9cca-c8c42ddc1746
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 064708f33aa410986b5398c31e54a927dceb4def
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752316"
---
# <a name="consume-external-web-services"></a>外部 Web サービスの消費

[!include [banner](../includes/banner.md)]

新しいクラス ライブラリを追加することによって、Web サービスを使用できます。 Microsoft Dynamics AX 2012 では、Microsoft Visual Studio プロジェクトを参照として追加し、**Aif::CreateServiceClient** を使用することで、X++ コードから Web サービスを使用できました。 このシナリオはサポートされていますが、ステップが変更されています。 アプリケーション統合フレームワーク (AIF) は現在サポートされていません。

次の手順は、X++ から外部 StockQuote サービスを使用する方法を示しています。

このサンプルの Web サービスの URL は架空のものであることに注意してください。  http://www.contoso.net/stockquote.asmx に既知の Web サービスはありません。  このコードを機能させるには、それを特定の Web サービスに適応させる必要があります。

1. Visual Studio で新しいクラス ライブラリ プロジェクトを作成し、**ExternalServiceLibrary.csproj** という名前を付けます。
2. Visual Studio プロジェクトで、外部 Web サービス `http://www.contoso.net/stockquote.asmx` へのサービス参照を追加します。
3. 新しい静的クラスを作成し、次の例に示すように StockQuote サービス操作をラップします。

    ```xpp
    public static string GetQuote(string s)
    {
        var binding = new System.ServiceModel.BasicHttpBinding();
        var endpointAddress = new EndpointAddress("http://www.contoso.net/stockquote.asmx");
        ServiceLibrary.QuoteReference.StockQuoteSoapClient client = new ServiceLibrary.QuoteReference.StockQuoteSoapClient(binding, endpointAddress);

        //GetQuote is the operation on the StockQuote service
        return client.GetQuote("MSFT");
    }
    ```

4. プロジェクトを構築します。 バイナリ ExternalServiceLibrary.dll が作成されます。
5. Visual Studio で、新しい Dynamics プロジェクトを作成します。
6. 参照として **ExternalServiceLibrary.dll** を追加します。
7. X++ クラスでは、ExternalServiceLibrary.dll で参照されていた外部 Web サービスを使用することができます。

    ```xpp
    public static void main(Args _args)
    {
        info(ServiceLibrary.StockQuoteClass::GetQuote("MSFT"));
    }
    ```


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]