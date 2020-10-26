---
title: カスタム サービスの開発
description: このトピックでは、カスタム サービスの作成方法を説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 02/07/2020
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
ms.openlocfilehash: 2ace272d940b5d30d64c76e74c34a30a0eb81048
ms.sourcegitcommit: 71ec2f48185b8104ca52ff70df52263ce5f87f26
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2020
ms.locfileid: "3893345"
---
# <a name="custom-service-development"></a><span data-ttu-id="7b3c4-103">顧客サービスの開発</span><span class="sxs-lookup"><span data-stu-id="7b3c4-103">Custom service development</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7b3c4-104">Finance and Operations に対してカスタム サービスを開発できます。</span><span class="sxs-lookup"><span data-stu-id="7b3c4-104">You can develop custom services for Finance and Operations.</span></span> <span data-ttu-id="7b3c4-105">開発者が 1 つのサービス グループに属するカスタム サービスを書き込むと、そのサービス グループは次の 2 つのエンドポイントに常に配置されます。</span><span class="sxs-lookup"><span data-stu-id="7b3c4-105">When a developer writes a custom service under a service group, the service group is always deployed on two endpoints:</span></span>

- <span data-ttu-id="7b3c4-106">SOAP エンドポイント</span><span class="sxs-lookup"><span data-stu-id="7b3c4-106">SOAP endpoint</span></span>
- <span data-ttu-id="7b3c4-107">JSON エンドポイント</span><span class="sxs-lookup"><span data-stu-id="7b3c4-107">JSON endpoint</span></span>

### <a name="soap-based-custom-service"></a><span data-ttu-id="7b3c4-108">SOAP ベース顧客サービス</span><span class="sxs-lookup"><span data-stu-id="7b3c4-108">SOAP-based custom service</span></span>

<span data-ttu-id="7b3c4-109">SOAP ベースのサービスは Dynamics AX 2012 のものと同じままです。</span><span class="sxs-lookup"><span data-stu-id="7b3c4-109">SOAP-based services remain the same as they were in Dynamics AX 2012.</span></span>

<span data-ttu-id="7b3c4-110">SOAP を使用したカスタム サービスを使用するためのコード例は、[Microsoft Dynamics AX 統合 GitHub リポジトリ](https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/ServiceSamples/SoapConsoleApplication)で利用できます。</span><span class="sxs-lookup"><span data-stu-id="7b3c4-110">Code examples for consuming custom services using SOAP are available in the [Microsoft Dynamics AX Integration GitHub repository](https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/ServiceSamples/SoapConsoleApplication).</span></span>

#### <a name="key-changes"></a><span data-ttu-id="7b3c4-111">キーの変更</span><span class="sxs-lookup"><span data-stu-id="7b3c4-111">Key changes</span></span>

- <span data-ttu-id="7b3c4-112">**AOTService グループ**ノードの下にあるすべてのサービス グループが自動的に配置されます。</span><span class="sxs-lookup"><span data-stu-id="7b3c4-112">All the service groups under the **AOTService group** node are automatically deployed.</span></span>
- <span data-ttu-id="7b3c4-113">配置する必要があるすべてのサービスはサービス グループの一部である必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b3c4-113">All services that must be deployed must be part of a service group.</span></span>

<span data-ttu-id="7b3c4-114">**開発環境でのエンドポイントの例**</span><span class="sxs-lookup"><span data-stu-id="7b3c4-114">**Example endpoint for a dev environment**</span></span>

`https://usnconeboxax1aos.cloud.onebox.dynamics.com/soap/services/UserSessionService?wsdl`

<span data-ttu-id="7b3c4-115">**非開発環境でのエンドポイントの例**</span><span class="sxs-lookup"><span data-stu-id="7b3c4-115">**Example endpoint for a non-dev environment**</span></span>

`https://<baseurl>/soap/services/UserSessionService?wsdl`

<span data-ttu-id="7b3c4-116">カスタム サービスの詳細については、次を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7b3c4-116">For more information about custom services, see:</span></span>

- <span data-ttu-id="7b3c4-117">[カスタム サービスを使用する \[AX 2012\] (TechNet)](https://technet.microsoft.com/library/hh509052.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b3c4-117">[Using Custom Services \[AX 2012\] (TechNet)](https://technet.microsoft.com/library/hh509052.aspx)</span></span>
- [<span data-ttu-id="7b3c4-118">チュートリアル: X++ クラスをデータ契約として公開する (TechNet)</span><span class="sxs-lookup"><span data-stu-id="7b3c4-118">Walkthrough: Exposing an X++ Class as a Data Contract (TechNet)</span></span>](https://technet.microsoft.com/library/gg844225.aspx)

### <a name="json-based-custom-service"></a><span data-ttu-id="7b3c4-119">JSON ベース顧客サービス</span><span class="sxs-lookup"><span data-stu-id="7b3c4-119">JSON-based custom service</span></span>

<span data-ttu-id="7b3c4-120">この機能により、X++ クラスを JSON サービスとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="7b3c4-120">This feature enables X++ classes to be consumed as JSON services.</span></span> <span data-ttu-id="7b3c4-121">つまり、返り値のデータ セットは、JSON 形式でです。</span><span class="sxs-lookup"><span data-stu-id="7b3c4-121">In other words, the return data set is in JSON format.</span></span> <span data-ttu-id="7b3c4-122">JavaScript Object Notation の略である JSON は、クライアントとサーバー間のデータ通信によく使用されるコンパクトで軽量なフォーマットです。</span><span class="sxs-lookup"><span data-stu-id="7b3c4-122">JSON, which stands for JavaScript Object Notation, is a compact, lightweight format that is commonly used communicate data between the client and the server.</span></span>

<span data-ttu-id="7b3c4-123">JSON エンドポイントが `https://host_uri/api/services/service_group_name/service_group_service_name/operation_name` にあります。</span><span class="sxs-lookup"><span data-stu-id="7b3c4-123">The JSON Endpoint is at `https://host_uri/api/services/service_group_name/service_group_service_name/operation_name`.</span></span>

<span data-ttu-id="7b3c4-124">**例**</span><span class="sxs-lookup"><span data-stu-id="7b3c4-124">**Example**</span></span>

`https://usnconeboxax1aos.cloud.onebox.dynamics.com/en/api/services/UserSessionService/AifUserSessionService/GetUserSessionInfo`

<span data-ttu-id="7b3c4-125">JSON サービスを使用するためのコード例は、[Microsoft Dynamics AX 統合 GitHub リポジトリ](https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/ServiceSamples/JsonConsoleApplication)で利用できます。</span><span class="sxs-lookup"><span data-stu-id="7b3c4-125">Code examples for consuming JSON services are available in the [Microsoft Dynamics AX Integration GitHub repository](https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/ServiceSamples/JsonConsoleApplication).</span></span>
