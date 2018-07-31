---
title: "顧客サービス"
description: "このトピックでは、カスタム サービスの作成方法を説明します。"
author: Sunil-Garg
manager: AnnBe
ms.date: 10/26/2017
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2475c6db57d1fa01ca914e568407b5f618ba95a1
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="custom-services-for-microsoft-dynamics-365-for-finance-and-operations"></a><span data-ttu-id="dc998-103">Microsoft Dynamics 365 for Finance and Operations の顧客サービス</span><span class="sxs-lookup"><span data-stu-id="dc998-103">Custom services for Microsoft Dynamics 365 for Finance and Operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc998-104">Microsoft Dynamics 365 for Finance and Operations のカスタム サービスを展開することができます。</span><span class="sxs-lookup"><span data-stu-id="dc998-104">You can develop custom services for Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="dc998-105">開発者がサービス グループに属するカスタム サービスを書き込むと、そのサービス グループは 2 つのエンドポイントに常に配置されます。</span><span class="sxs-lookup"><span data-stu-id="dc998-105">When a developer writes a custom service under a service group, the service group is always deployed on two endpoints:</span></span>
-   <span data-ttu-id="dc998-106">SOAP エンドポイント</span><span class="sxs-lookup"><span data-stu-id="dc998-106">SOAP endpoint</span></span> 
-   <span data-ttu-id="dc998-107">JSON エンドポイント</span><span class="sxs-lookup"><span data-stu-id="dc998-107">JSON endpoint</span></span>

### <a name="soap-based-custom-service"></a><span data-ttu-id="dc998-108">SOAP ベース顧客サービス</span><span class="sxs-lookup"><span data-stu-id="dc998-108">SOAP-based custom service</span></span>

<span data-ttu-id="dc998-109">SOAP ベースのサービスは AX 2012 のものと同じままです。</span><span class="sxs-lookup"><span data-stu-id="dc998-109">SOAP-based services remain the same as they were in AX 2012.</span></span>

<span data-ttu-id="dc998-110">SOAP を使用してカスタム サービスを使用するためのコード例は、[Microsoft Dynamics AX 統合 GitHub リポジトリ](https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/ServiceSamples/SoapConsoleApplication) です。</span><span class="sxs-lookup"><span data-stu-id="dc998-110">Code examples for consuming custom services using SOAP are available in the [Microsoft Dynamics AX Integration GitHub repository](https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/ServiceSamples/SoapConsoleApplication).</span></span>

#### <a name="key-changes"></a><span data-ttu-id="dc998-111">キーの変更</span><span class="sxs-lookup"><span data-stu-id="dc998-111">Key changes</span></span>

-   <span data-ttu-id="dc998-112">**AOTService グループ**ノードの下にあるすべてのサービス グループが自動的に配置されます。</span><span class="sxs-lookup"><span data-stu-id="dc998-112">All the service groups under the **AOTService group** node are automatically deployed.</span></span>
-   <span data-ttu-id="dc998-113">配置する必要があるすべてのサービスはサービス グループの一部である必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc998-113">All services that must be deployed must be part of a service group.</span></span>

<span data-ttu-id="dc998-114">SOAP エンドポイントが `https://host_uri/soap/services/service_group_name` にあります。</span><span class="sxs-lookup"><span data-stu-id="dc998-114">The SOAP endpoint is at `https://host_uri/soap/services/service_group_name`.</span></span> 

<span data-ttu-id="dc998-115">**例:** `https://usnconeboxax1aos.cloud.onebox.dynamics.com/soap/services/UserSessionService?wsdl`</span><span class="sxs-lookup"><span data-stu-id="dc998-115">**Example:** `https://usnconeboxax1aos.cloud.onebox.dynamics.com/soap/services/UserSessionService?wsdl`</span></span>

<span data-ttu-id="dc998-116">詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dc998-116">For more information, see:</span></span>
-   <span data-ttu-id="dc998-117">[カスタム サービスを使用する \[AX 2012\] (TechNet)](http://technet.microsoft.com/en-us/library/hh509052.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc998-117">[Using Custom Services \[AX 2012\] (TechNet)](http://technet.microsoft.com/en-us/library/hh509052.aspx)</span></span>
-   [<span data-ttu-id="dc998-118">チュートリアル: X++ クラスをデータ契約として公開する (TechNet)</span><span class="sxs-lookup"><span data-stu-id="dc998-118">Walkthrough: Exposing an X++ Class as a Data Contract (TechNet)</span></span>](http://technet.microsoft.com/en-us/library/gg844225.aspx)

<!--
-   [Custom services Office Mix presentation](https://mix.office.com/watch/12e4fejbgj429). -->


### <a name="json-based-custom-service"></a><span data-ttu-id="dc998-119">JSON ベース顧客サービス</span><span class="sxs-lookup"><span data-stu-id="dc998-119">JSON-based Custom Service</span></span>

<span data-ttu-id="dc998-120">この機能により、X++ クラスを JSON サービスとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="dc998-120">This feature enables X++ classes to be consumed as JSON services.</span></span> <span data-ttu-id="dc998-121">つまり、返り値のデータ セットは、JSON 形式でです。</span><span class="sxs-lookup"><span data-stu-id="dc998-121">In other words, the return data set is in JSON format.</span></span> <span data-ttu-id="dc998-122">JavaScript Object Notation を示す JSON は、クライアントとサーバーの間でのデータ通信によく使用されるコンパクトで軽量なフォーマットです。</span><span class="sxs-lookup"><span data-stu-id="dc998-122">JSON, which stands for JavaScript Object Notation, is a compact, lightweight format that is commonly used communicate data between the client and the server.</span></span> 

<span data-ttu-id="dc998-123">JSON エンドポイントが `https://host_uri/api/services/service_group_name/service_group_service_name/operation_name` にあります。</span><span class="sxs-lookup"><span data-stu-id="dc998-123">The JSON Endpoint is at `https://host_uri/api/services/service_group_name/service_group_service_name/operation_name`.</span></span>

<span data-ttu-id="dc998-124">**例:** `https://usnconeboxax1aos.cloud.onebox.dynamics.com/en/api/services/UserSessionService/AifUserSessionService/GetUserSessionInfo`</span><span class="sxs-lookup"><span data-stu-id="dc998-124">**Example:** `https://usnconeboxax1aos.cloud.onebox.dynamics.com/en/api/services/UserSessionService/AifUserSessionService/GetUserSessionInfo`</span></span>

<span data-ttu-id="dc998-125">JSON サービスを使用するためのコード例は、[Microsoft Dynamics AX 統合 GitHub リポジトリ](https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/ServiceSamples/JsonConsoleApplication) です。</span><span class="sxs-lookup"><span data-stu-id="dc998-125">Code examples for consuming JSON services are available in the [Microsoft Dynamics AX Integration GitHub repository](https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/ServiceSamples/JsonConsoleApplication).</span></span>


