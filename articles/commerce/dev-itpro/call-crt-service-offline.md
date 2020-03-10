---
title: Commerce Runtime (CRT) サービスをオフライン モードで呼び出す
description: このトピックでは、販売時点管理 (POS) のオフライン サポートを提供する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 07/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 69834
ms.assetid: 4f4dbdd3-e48c-417c-b8bb-f7fd6628bd9b
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 200e34416c9f5b974c68919988c7908a299c7cef
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070468"
---
# <a name="call-the-commerce-runtime-crt-service-in-offline-mode"></a><span data-ttu-id="be8b1-103">Commerce Runtime (CRT) サービスをオフライン モードで呼び出す</span><span class="sxs-lookup"><span data-stu-id="be8b1-103">Call the Commerce runtime (CRT) service in offline mode</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="be8b1-104">このトピックは、Dynamics 365 for Finance and Operations バージョン 7.1 およびそれ以前のバージョンに適用されます。</span><span class="sxs-lookup"><span data-stu-id="be8b1-104">This topic is applicable for Dynamics 365 for Finance and Operations version 7.1 and earlier.</span></span> <span data-ttu-id="be8b1-105">バージョン 7.2 およびそれ以上の場合は、この実装はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="be8b1-105">This implementation is not supported for versions 7.2 and higher.</span></span> <span data-ttu-id="be8b1-106">これらのバージョンでは、オーバーレイせずに拡張モデルに従います。</span><span class="sxs-lookup"><span data-stu-id="be8b1-106">For those versions, follow the extension model without overlayering.</span></span>

<span data-ttu-id="be8b1-107">このトピックでは、販売時点管理 (POS) のオフライン サポートを提供する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="be8b1-107">This topic describes how provide offline support for point of sale (POS).</span></span>

<span data-ttu-id="be8b1-108">販売時点管理 (POS) デバイスがオフラインになると (すなわち、Retail サーバーに接続されていないとき)、その POS はローカル商業ランタイム (CRT) に自動的に切り替わります。</span><span class="sxs-lookup"><span data-stu-id="be8b1-108">When a point of sale (POS) device goes offline (in other words, when it isn't connected to Retail Server), the POS automatically switches to the local commerce runtime (CRT).</span></span> <span data-ttu-id="be8b1-109">POS クライアントは、Retail プロキシを使用して、ローカル CRT と通信します。</span><span class="sxs-lookup"><span data-stu-id="be8b1-109">The POS client communicates with the local CRT by using the Retail proxy.</span></span> <span data-ttu-id="be8b1-110">プロキシがカスタム サービスを理解できるようにするには、Retail プロキシ プロジェクトを拡張して要求タイプをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="be8b1-110">To enable the proxy to understand your custom service, you must extend the Retail proxy project to support your request type.</span></span>

1.  <span data-ttu-id="be8b1-111">Microsoft Visual Studio で、Retail SDK\\プロキシ フォルダーから Proxies.RetailProxy.csproj を開きます。</span><span class="sxs-lookup"><span data-stu-id="be8b1-111">In Microsoft Visual Studio, from the Retail SDK\\Proxies folder, open Proxies.RetailProxy.csproj.</span></span>
2.  <span data-ttu-id="be8b1-112">RetailSDK\\Proxies\\RetailProxy\\Adapters\\UsingStatements.Extensions を、CRT 拡張プロジェクトで導入された新しいエンティティ/複合型に対して定義した新しい名前空間で更新します。</span><span class="sxs-lookup"><span data-stu-id="be8b1-112">Update RetailSDK\\Proxies\\RetailProxy\\Adapters\\UsingStatements.Extensions with the new namespace that you defined for the new entity/complex types that were introduced in CRT extension projects.</span></span> <span data-ttu-id="be8b1-113">これらのプロジェクトまたはダイナミクス リンク ライブラリ (DLL) は、まず Proxies.RetailProxy.csproj によって参照される必要があります。</span><span class="sxs-lookup"><span data-stu-id="be8b1-113">These projects or dynamics-link libraries (DLLs) must first be referenced by Proxies.RetailProxy.csproj.</span></span>
3.  <span data-ttu-id="be8b1-114">Proxies.RetailProxy プロジェクトをコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="be8b1-114">Compile the Proxies.RetailProxy project.</span></span> <span data-ttu-id="be8b1-115">コンパイル中に、アダプタ \\Interfaces.g.cs は、新しいエンティティおよびインターフェイスの情報で更新されます。</span><span class="sxs-lookup"><span data-stu-id="be8b1-115">During compilation, Adapters\\Interfaces.g.cs is updated with your new entity and interface information.</span></span> <span data-ttu-id="be8b1-116">自動的に生成されたクラスを変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="be8b1-116">Don't modify this automatically generated class.</span></span>
4.  <span data-ttu-id="be8b1-117">アダプタ フォルダーに新しいマネージャー クラスを追加し、そのマネージャーから CRT サービスを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="be8b1-117">Add your new manager class to the Adapters folder, and call your CRT service from that manager.</span></span> <span data-ttu-id="be8b1-118">**SalesOrderManager** や **PurchaseOrderManager** などの標準エンティティ マネージャー クラスは、[Adapters] フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="be8b1-118">The standard entity manager classes, such as **SalesOrderManager** and **PurchaseOrderManager**, are available in the Adapters folder.</span></span> <span data-ttu-id="be8b1-119">**注記:** プロジェクトで使用されるすべてのライブラリは、移動可能で署名されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="be8b1-119">**Note:** All the libraries that are used in the project must be portable and signed.</span></span> <span data-ttu-id="be8b1-120">(参照されるカスタムの CRT サービスは、移動可能なライブラリである必要があります。)</span><span class="sxs-lookup"><span data-stu-id="be8b1-120">(Any custom CRT service that is referenced must be a portable library.)</span></span>
5.  <span data-ttu-id="be8b1-121">コンパイル後に新しい公開キーが生成されるため、CRT 構成ファイルの公開キーを更新します。</span><span class="sxs-lookup"><span data-stu-id="be8b1-121">Update the public key in the CRT configuration file, because a new public key is generated after compilation.</span></span>
6.  <span data-ttu-id="be8b1-122">Microsoft Dynamics AX\\70\\Retail Modern POS\\ClientBroker フォルダで、新しいプロキシ DLL をビルドして置き換えます。</span><span class="sxs-lookup"><span data-stu-id="be8b1-122">Build and replace the new proxy DLL in the Microsoft Dynamics AX\\70\\Retail Modern POS\\ClientBroker folder.</span></span> <span data-ttu-id="be8b1-123">また、カスタム CRT 拡張ライブラリを、Microsoft DynamicsAX\\70\\Retail Modern POS\\ClientBroker フォルダへドロップします。</span><span class="sxs-lookup"><span data-stu-id="be8b1-123">Additionally, drop the custom CRT extension library into the Microsoft Dynamics AX\\70\\Retail Modern POS\\ClientBroker folder.</span></span> <span data-ttu-id="be8b1-124">(参照されるすべてのライブラリは、このフォルダにドロップする必要があります)。</span><span class="sxs-lookup"><span data-stu-id="be8b1-124">(All libraries that are referenced should be dropped into this folder.)</span></span>
7.  <span data-ttu-id="be8b1-125">DllHost.exe.config ファイルで、**RetailProxyAssemblyName** および **AdaptorCallerFullTypeName** を新しいプロキシ DLL およびアダプタ名に更新します。</span><span class="sxs-lookup"><span data-stu-id="be8b1-125">In the DllHost.exe.config file, update **RetailProxyAssemblyName** and **AdaptorCallerFullTypeName** with the new proxy DLL and adapter name.</span></span>

    ```xml
    <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy" />
    <add key="AdaptorCallerFullTypeName" value="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller" />
    ```

8.  <span data-ttu-id="be8b1-126">CommerceRuntime.MPOSOffline.config ファイルの **&lt;構成&gt;** 要素で、commerceRuntime.config ファイルに関する新しい CRT DLL 情報を更新します。</span><span class="sxs-lookup"><span data-stu-id="be8b1-126">In the CommerceRuntime.MPOSOffline.config file, in the **&lt;composition&gt;** element, update the new CRT DLL information as for the commerceRuntime.config file.</span></span>

    ```xml
    <add source="assembly" value="Contoso.Commerce.Runtime.Services" />
    ```

9.  <span data-ttu-id="be8b1-127">dllhost.exe を再起動します。</span><span class="sxs-lookup"><span data-stu-id="be8b1-127">Restart dllhost.exe.</span></span> <span data-ttu-id="be8b1-128">(新しい構成ファイルを読むために MPOS の dllhost.exe を再起動する必要があります。構成ファイルの変更がある場合、アップグレードをする際に必要になります。)</span><span class="sxs-lookup"><span data-stu-id="be8b1-128">(You should restart the dllhost.exe for MPOS to read the new config file, this will be required even when you do any upgrade if it has config file changes.)</span></span>




