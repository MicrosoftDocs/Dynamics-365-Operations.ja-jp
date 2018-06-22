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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2c029cdd1e63bb7a228f3f0e0776249e9b4b1f8e
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="call-crt-service-in-offline-mode"></a><span data-ttu-id="aec84-103">CRT サービスのオフライン モードでの呼び出し</span><span class="sxs-lookup"><span data-stu-id="aec84-103">Call CRT service in offline mode</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aec84-104">このトピックでは、販売時点管理 (POS) のオフライン サポートを提供する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="aec84-104">This topic describes how provide offline support for point of sale (POS).</span></span>

<span data-ttu-id="aec84-105">販売時点管理 (POS) デバイスがオフラインになると (すなわち、Retail サーバーに接続されていないとき)、その POS はローカル商業ランタイム (CRT) に自動的に切り替わります。</span><span class="sxs-lookup"><span data-stu-id="aec84-105">When a point of sale (POS) device goes offline (in other words, when it isn't connected to Retail Server), the POS automatically switches to the local commerce runtime (CRT).</span></span> <span data-ttu-id="aec84-106">POS クライアントは、Retail プロキシを使用して、ローカル CRT と通信します。</span><span class="sxs-lookup"><span data-stu-id="aec84-106">The POS client communicates with the local CRT by using the Retail proxy.</span></span> <span data-ttu-id="aec84-107">プロキシがカスタム サービスを理解できるようにするには、Retail プロキシ プロジェクトを拡張して要求タイプをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="aec84-107">To enable the proxy to understand your custom service, you must extend the Retail proxy project to support your request type.</span></span>

1.  <span data-ttu-id="aec84-108">Microsoft Visual Studio で、Retail SDK\\プロキシ フォルダーから Proxies.RetailProxy.csproj を開きます。</span><span class="sxs-lookup"><span data-stu-id="aec84-108">In Microsoft Visual Studio, from the Retail SDK\\Proxies folder, open Proxies.RetailProxy.csproj.</span></span>
2.  <span data-ttu-id="aec84-109">RetailSDK\\Proxies\\RetailProxy\\Adapters\\UsingStatements.Extensions を、CRT 拡張プロジェクトで導入された新しいエンティティ/複合型に対して定義した新しい名前空間で更新します。</span><span class="sxs-lookup"><span data-stu-id="aec84-109">Update RetailSDK\\Proxies\\RetailProxy\\Adapters\\UsingStatements.Extensions with the new namespace that you defined for the new entity/complex types that were introduced in CRT extension projects.</span></span> <span data-ttu-id="aec84-110">これらのプロジェクトまたはダイナミクス リンク ライブラリ (DLL) は、まず Proxies.RetailProxy.csproj によって参照される必要があります。</span><span class="sxs-lookup"><span data-stu-id="aec84-110">These projects or dynamics-link libraries (DLLs) must first be referenced by Proxies.RetailProxy.csproj.</span></span>
3.  <span data-ttu-id="aec84-111">Proxies.RetailProxy プロジェクトをコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="aec84-111">Compile the Proxies.RetailProxy project.</span></span> <span data-ttu-id="aec84-112">コンパイル中に、アダプタ \\Interfaces.g.cs は、新しいエンティティおよびインターフェイスの情報で更新されます。</span><span class="sxs-lookup"><span data-stu-id="aec84-112">During compilation, Adapters\\Interfaces.g.cs is updated with your new entity and interface information.</span></span> <span data-ttu-id="aec84-113">自動的に生成されたクラスを変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="aec84-113">Don't modify this automatically generated class.</span></span>
4.  <span data-ttu-id="aec84-114">アダプタ フォルダーに新しいマネージャー クラスを追加し、そのマネージャーから CRT サービスを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="aec84-114">Add your new manager class to the Adapters folder, and call your CRT service from that manager.</span></span> <span data-ttu-id="aec84-115">**SalesOrderManager** や **PurchaseOrderManager** などの標準エンティティ マネージャー クラスは、[Adapters] フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="aec84-115">The standard entity manager classes, such as **SalesOrderManager** and **PurchaseOrderManager**, are available in the Adapters folder.</span></span> <span data-ttu-id="aec84-116">**注記:** プロジェクトで使用されるすべてのライブラリは、移動可能で署名されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="aec84-116">**Note:** All the libraries that are used in the project must be portable and signed.</span></span> <span data-ttu-id="aec84-117">(参照されるカスタムの CRT サービスは、移動可能なライブラリである必要があります。)</span><span class="sxs-lookup"><span data-stu-id="aec84-117">(Any custom CRT service that is referenced must be a portable library.)</span></span>
5.  <span data-ttu-id="aec84-118">コンパイル後に新しい公開キーが生成されるため、CRT 構成ファイルの公開キーを更新します。</span><span class="sxs-lookup"><span data-stu-id="aec84-118">Update the public key in the CRT configuration file, because a new public key is generated after compilation.</span></span>
6.  <span data-ttu-id="aec84-119">Microsoft Dynamics AX\\70\\Retail Modern POS\\ClientBroker フォルダー内の新しいプロキシ DLL をビルドし置き換えます。</span><span class="sxs-lookup"><span data-stu-id="aec84-119">Build and replace the new proxy DLL in the Microsoft Dynamics AX\\70\\Retail Modern POS\\ClientBroker folder.</span></span> <span data-ttu-id="aec84-120">また、カスタム CRT 拡張子ライブラリを Microsoft Dynamics AX \\70\\ Retail Modern POS\\ ClientBroker フォルダーにドロップします。</span><span class="sxs-lookup"><span data-stu-id="aec84-120">Additionally, drop the custom CRT extension library into the Microsoft Dynamics AX\\70\\Retail Modern POS\\ClientBroker folder.</span></span> <span data-ttu-id="aec84-121">(参照されるすべてのライブラリは、このフォルダにドロップする必要があります)。</span><span class="sxs-lookup"><span data-stu-id="aec84-121">(All libraries that are referenced should be dropped into this folder.)</span></span>
7.  <span data-ttu-id="aec84-122">DllHost.exe.config ファイルで、**RetailProxyAssemblyName** および **AdaptorCallerFullTypeName** を新しいプロキシ DLL およびアダプタ名に更新します。</span><span class="sxs-lookup"><span data-stu-id="aec84-122">In the DllHost.exe.config file, update **RetailProxyAssemblyName** and **AdaptorCallerFullTypeName** with the new proxy DLL and adapter name.</span></span>

        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy" />
        <add key="AdaptorCallerFullTypeName" value="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller" />

8.  <span data-ttu-id="aec84-123">CommerceRuntime.MPOSOffline.config ファイルの **&lt;構成&gt;** 要素で、commerceRuntime.config ファイルに関する新しい CRT DLL 情報を更新します。</span><span class="sxs-lookup"><span data-stu-id="aec84-123">In the CommerceRuntime.MPOSOffline.config file, in the **&lt;composition&gt;** element, update the new CRT DLL information as for the commerceRuntime.config file.</span></span>

        <add source="assembly" value="Contoso.Commerce.Runtime.Services" />

9.  <span data-ttu-id="aec84-124">dllhost.exe を再起動します。</span><span class="sxs-lookup"><span data-stu-id="aec84-124">Restart dllhost.exe.</span></span> <span data-ttu-id="aec84-125">(新しい構成ファイルを読むために MPOS の dllhost.exe を再起動する必要があります。構成ファイルの変更がある場合、アップグレードをする際に必要になります。)</span><span class="sxs-lookup"><span data-stu-id="aec84-125">(You should restart the dllhost.exe for MPOS to read the new config file, this will be required even when you do any upgrade if it has config file changes.)</span></span>





