---
title: "CRT サービスのオフライン モードでの呼び出し"
description: "このトピックでは、販売時点管理 (POS) のオフライン サポートを提供する方法について説明します。"
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
ms.custom: 69834
ms.assetid: 4f4dbdd3-e48c-417c-b8bb-f7fd6628bd9b
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 35016cfc3c8d34e165f3e350efc4da68be716840
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="call-crt-service-in-offline-mode"></a>CRT サービスのオフライン モードでの呼び出し

[!include [banner](../includes/banner.md)]

このトピックでは、販売時点管理 (POS) のオフライン サポートを提供する方法について説明します。

販売時点管理 (POS) デバイスがオフラインになると (すなわち、Retail サーバーに接続されていないとき)、その POS はローカル商業ランタイム (CRT) に自動的に切り替わります。 POS クライアントは、Retail プロキシを使用して、ローカル CRT と通信します。 プロキシがカスタム サービスを理解できるようにするには、Retail プロキシ プロジェクトを拡張して要求タイプをサポートする必要があります。

1.  Microsoft Visual Studio で、Retail SDK\\プロキシ フォルダーから Proxies.RetailProxy.csproj を開きます。
2.  RetailSDK\\Proxies\\RetailProxy\\Adapters\\UsingStatements.Extensions を、CRT 拡張プロジェクトで導入された新しいエンティティ/複合型に対して定義した新しい名前空間で更新します。 これらのプロジェクトまたはダイナミクス リンク ライブラリ (DLL) は、まず Proxies.RetailProxy.csproj によって参照される必要があります。
3.  Proxies.RetailProxy プロジェクトをコンパイルします。 コンパイル中に、アダプタ \\Interfaces.g.cs は、新しいエンティティおよびインターフェイスの情報で更新されます。 自動的に生成されたクラスを変更しないでください。
4.  アダプタ フォルダーに新しいマネージャー クラスを追加し、そのマネージャーから CRT サービスを呼び出します。 **SalesOrderManager** や **PurchaseOrderManager** などの標準エンティティ マネージャー クラスは、[Adapters] フォルダーにあります。 **注記:** プロジェクトで使用されるすべてのライブラリは、移動可能で署名されている必要があります。 (参照されるカスタムの CRT サービスは、移動可能なライブラリである必要があります。)
5.  コンパイル後に新しい公開キーが生成されるため、CRT 構成ファイルの公開キーを更新します。
6.  Microsoft Dynamics AX\\70\\Retail Modern POS\\ClientBroker フォルダー内の新しいプロキシ DLL をビルドし置き換えます。 また、カスタム CRT 拡張子ライブラリを Microsoft Dynamics AX \\70\\ Retail Modern POS\\ ClientBroker フォルダーにドロップします。 (参照されるすべてのライブラリは、このフォルダにドロップする必要があります)。
7.  DllHost.exe.config ファイルで、**RetailProxyAssemblyName** および **AdaptorCallerFullTypeName** を新しいプロキシ DLL およびアダプタ名に更新します。

        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy" />
        <add key="AdaptorCallerFullTypeName" value="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller" />

8.  CommerceRuntime.MPOSOffline.config ファイルの **&lt;構成&gt;** 要素で、commerceRuntime.config ファイルに関する新しい CRT DLL 情報を更新します。

        <add source="assembly" value="Contoso.Commerce.Runtime.Services" />

9.  dllhost.exe を再起動します。 (新しい構成ファイルを読むために MPOS の dllhost.exe を再起動する必要があります。構成ファイルの変更がある場合、アップグレードをする際に必要になります。)





