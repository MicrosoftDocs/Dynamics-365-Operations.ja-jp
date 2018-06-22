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
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: ea79b0d4a86a68e8d23419b1e86287b529b63422
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="custom-services-for-microsoft-dynamics-365-for-finance-and-operations"></a><span data-ttu-id="62c3f-103">Microsoft Dynamics 365 for Finance and Operations の顧客サービス</span><span class="sxs-lookup"><span data-stu-id="62c3f-103">Custom services for Microsoft Dynamics 365 for Finance and Operations</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="62c3f-104">Microsoft Dynamics 365 for Finance and Operations のカスタム サービスを展開することができます。</span><span class="sxs-lookup"><span data-stu-id="62c3f-104">You can develop custom services for Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="62c3f-105">開発者がサービス グループに属するカスタム サービスを書き込むと、そのサービス グループは 2 つのエンドポイントに常に配置されます。</span><span class="sxs-lookup"><span data-stu-id="62c3f-105">When a developer writes a custom service under a service group, the service group is always deployed on two endpoints:</span></span>
-   <span data-ttu-id="62c3f-106">SOAP エンドポイント</span><span class="sxs-lookup"><span data-stu-id="62c3f-106">SOAP endpoint</span></span> 
-   <span data-ttu-id="62c3f-107">JSON エンドポイント</span><span class="sxs-lookup"><span data-stu-id="62c3f-107">JSON endpoint</span></span>

### <a name="soap-based-custom-service"></a><span data-ttu-id="62c3f-108">SOAP ベース顧客サービス</span><span class="sxs-lookup"><span data-stu-id="62c3f-108">SOAP-based custom service</span></span>

<span data-ttu-id="62c3f-109">SOAP ベースのサービスは AX 2012 のものと同じままです。</span><span class="sxs-lookup"><span data-stu-id="62c3f-109">SOAP-based services remain the same as they were in AX 2012.</span></span>

<span data-ttu-id="62c3f-110">SOAP を使用してカスタム サービスを使用するためのコード例は、[Microsoft Dynamics AX 統合 GitHub リポジトリ](https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/ServiceSamples/SoapConsoleApplication) です。</span><span class="sxs-lookup"><span data-stu-id="62c3f-110">Code examples for consuming custom services using SOAP are available in the [Microsoft Dynamics AX Integration GitHub repository](https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/ServiceSamples/SoapConsoleApplication).</span></span>

#### <a name="key-changes"></a><span data-ttu-id="62c3f-111">キーの変更</span><span class="sxs-lookup"><span data-stu-id="62c3f-111">Key changes</span></span>

-   <span data-ttu-id="62c3f-112">**AOTService グループ**ノードの下にあるすべてのサービス グループが自動的に配置されます。</span><span class="sxs-lookup"><span data-stu-id="62c3f-112">All the service groups under the **AOTService group** node are automatically deployed.</span></span>
-   <span data-ttu-id="62c3f-113">配置する必要があるすべてのサービスはサービス グループの一部である必要があります。</span><span class="sxs-lookup"><span data-stu-id="62c3f-113">All services that must be deployed must be part of a service group.</span></span>

<span data-ttu-id="62c3f-114">SOAP エンドポイントが `https://host_uri/soap/services/service_group_name` にあります。</span><span class="sxs-lookup"><span data-stu-id="62c3f-114">The SOAP endpoint is at `https://host_uri/soap/services/service_group_name`.</span></span> 

<span data-ttu-id="62c3f-115">**例:** `https://usnconeboxax1aos.cloud.onebox.dynamics.com/soap/services/UserSessionService?wsdl`</span><span class="sxs-lookup"><span data-stu-id="62c3f-115">**Example:** `https://usnconeboxax1aos.cloud.onebox.dynamics.com/soap/services/UserSessionService?wsdl`</span></span>

<span data-ttu-id="62c3f-116">詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="62c3f-116">For more information, see:</span></span>
-   <span data-ttu-id="62c3f-117">[カスタム サービスを使用する \[AX 2012\] (TechNet)](http://technet.microsoft.com/en-us/library/hh509052.aspx)</span><span class="sxs-lookup"><span data-stu-id="62c3f-117">[Using Custom Services \[AX 2012\] (TechNet)](http://technet.microsoft.com/en-us/library/hh509052.aspx)</span></span>
-   [<span data-ttu-id="62c3f-118">チュートリアル: X++ クラスをデータ契約として公開する (TechNet)</span><span class="sxs-lookup"><span data-stu-id="62c3f-118">Walkthrough: Exposing an X++ Class as a Data Contract (TechNet)</span></span>](http://technet.microsoft.com/en-us/library/gg844225.aspx)
-   <span data-ttu-id="62c3f-119">[カスタム サービス Office Mix プレゼンテーション](https://mix.office.com/watch/12e4fejbgj429)。</span><span class="sxs-lookup"><span data-stu-id="62c3f-119">[Custom services Office Mix presentation](https://mix.office.com/watch/12e4fejbgj429).</span></span> 


### <a name="json-based-custom-service"></a><span data-ttu-id="62c3f-120">JSON ベース顧客サービス</span><span class="sxs-lookup"><span data-stu-id="62c3f-120">JSON-based Custom Service</span></span>

<span data-ttu-id="62c3f-121">この機能により、X++ クラスを JSON サービスとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="62c3f-121">This feature enables X++ classes to be consumed as JSON services.</span></span> <span data-ttu-id="62c3f-122">つまり、返り値のデータ セットは、JSON 形式でです。</span><span class="sxs-lookup"><span data-stu-id="62c3f-122">In other words, the return data set is in JSON format.</span></span> <span data-ttu-id="62c3f-123">JavaScript Object Notation を示す JSON は、クライアントとサーバーの間でのデータ通信によく使用されるコンパクトで軽量なフォーマットです。</span><span class="sxs-lookup"><span data-stu-id="62c3f-123">JSON, which stands for JavaScript Object Notation, is a compact, lightweight format that is commonly used communicate data between the client and the server.</span></span> 

<span data-ttu-id="62c3f-124">JSON エンドポイントが `https://host_uri/api/services/service_group_name/service_group_service_name/operation_name` にあります。</span><span class="sxs-lookup"><span data-stu-id="62c3f-124">The JSON Endpoint is at `https://host_uri/api/services/service_group_name/service_group_service_name/operation_name`.</span></span>

<span data-ttu-id="62c3f-125">**例:** `https://usnconeboxax1aos.cloud.onebox.dynamics.com/en/api/services/UserSessionService/AifUserSessionService/GetUserSessionInfo`</span><span class="sxs-lookup"><span data-stu-id="62c3f-125">**Example:** `https://usnconeboxax1aos.cloud.onebox.dynamics.com/en/api/services/UserSessionService/AifUserSessionService/GetUserSessionInfo`</span></span>

<span data-ttu-id="62c3f-126">JSON サービスを使用するためのコード例は、[Microsoft Dynamics AX 統合 GitHub リポジトリ](https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/ServiceSamples/JsonConsoleApplication) です。</span><span class="sxs-lookup"><span data-stu-id="62c3f-126">Code examples for consuming JSON services are available in the [Microsoft Dynamics AX Integration GitHub repository](https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/ServiceSamples/JsonConsoleApplication).</span></span>


