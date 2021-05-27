---
title: 給与統合 API の概要
description: このトピックでは、Dynamics 365 Human Resources 給与統合 API について説明します。
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3a7be5ad42642de48ffdb2731a1300a953c5ede4
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022766"
---
# <a name="payroll-integration-api-introduction"></a><span data-ttu-id="a156f-103">給与統合 API の概要</span><span class="sxs-lookup"><span data-stu-id="a156f-103">Payroll integration API introduction</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="a156f-104">このドキュメントでは、Dynamics 365 Human Resources 給与統合 API について説明します。</span><span class="sxs-lookup"><span data-stu-id="a156f-104">This document describes the Dynamics 365 Human Resources Payroll integration API.</span></span> <span data-ttu-id="a156f-105">API を使用すると、人事管理と給与システム パートナー間のエンド ツー エンドの統合を合理化できます。</span><span class="sxs-lookup"><span data-stu-id="a156f-105">The API enables streamlined end-to-end integrations between Human Resources and partnering payroll systems.</span></span> <span data-ttu-id="a156f-106">統合された経験は、Human Resources で、従業員のプロファイル、給与と控除、および貢献度情報で始まります。</span><span class="sxs-lookup"><span data-stu-id="a156f-106">The integrated experience begins in Human Resources with the employee profile, salary and deduction, and contribution information.</span></span> <span data-ttu-id="a156f-107">従業員を雇用し、必要なプロファイルと給与情報を Human Resources に入力すると、給与システムはこの情報を取得して、給与の処理時に使用します。</span><span class="sxs-lookup"><span data-stu-id="a156f-107">When you hire an employee and enter the required profile and pay information into Human Resources, the payroll system pulls this information to use when processing payroll.</span></span> <span data-ttu-id="a156f-108">従業員に対して行われた更新や支払情報も、後で支払の実行で使用されます。</span><span class="sxs-lookup"><span data-stu-id="a156f-108">Any updates made to the employee or pay information are also pulled for use in later pay runs.</span></span>

![給与統合フロー](media/hr-admin-integration-payroll-api-introduction-flow.png)

<span data-ttu-id="a156f-110">統合を有効にするため、Human Resources は、次のコンポーネントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a156f-110">To enable the integration, Human Resources includes the following components:</span></span>

- <span data-ttu-id="a156f-111">従業員に支払準備完了をマークするための機能</span><span class="sxs-lookup"><span data-stu-id="a156f-111">Functionality to mark an employee as ready to pay</span></span>
- <span data-ttu-id="a156f-112">アプリケーションを統合する新機能をオープンにした統合 API</span><span class="sxs-lookup"><span data-stu-id="a156f-112">An integration API opening up the new functionality to integrating applications</span></span>

## <a name="microsoft-dataverse"></a><span data-ttu-id="a156f-113">Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="a156f-113">Microsoft Dataverse</span></span>

<span data-ttu-id="a156f-114">この API は Microsoft Dataverse (旧 Common Data Service) に構築されています。</span><span class="sxs-lookup"><span data-stu-id="a156f-114">This API is built on Microsoft Dataverse (formerly Common Data Service).</span></span> <span data-ttu-id="a156f-115">この API との RESTful の対話は、ODataを使用する Microsoft Dataverse Web API を介して行われます。</span><span class="sxs-lookup"><span data-stu-id="a156f-115">All RESTful interaction with this API is done via the Microsoft Dataverse Web API, which uses OData.</span></span> <span data-ttu-id="a156f-116">この API は Dataverse Web API のサブセットです。</span><span class="sxs-lookup"><span data-stu-id="a156f-116">This API is a subset of the Dataverse Web API.</span></span> <span data-ttu-id="a156f-117">Dataverse Web APIでは、認証、SLA、バッチ、同時実行制御、エラー処理などの特性が定義されます。</span><span class="sxs-lookup"><span data-stu-id="a156f-117">The Dataverse Web API defines characteristics such as authentication, SLAs, batch, concurrency control, and error handling.</span></span>

<span data-ttu-id="a156f-118">Microsoft Dataverse Web API の詳細については、次を参照してください :</span><span class="sxs-lookup"><span data-stu-id="a156f-118">For more general information about the Microsoft Dataverse Web API, see:</span></span>

- [<span data-ttu-id="a156f-119">Microsoft Dataverse とは</span><span class="sxs-lookup"><span data-stu-id="a156f-119">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)
- [<span data-ttu-id="a156f-120">Microsoft Dataverse Web API を使用する</span><span class="sxs-lookup"><span data-stu-id="a156f-120">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)
- [<span data-ttu-id="a156f-121">Microsoft Dataverse 開発者ガイド</span><span class="sxs-lookup"><span data-stu-id="a156f-121">Microsoft Dataverse developer guide</span></span>](/powerapps/developer/data-platform)

<span data-ttu-id="a156f-122">このドキュメントには、次のトピックを含む、Dataverse Web API の使用に関する詳細と開発者ガイダンスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="a156f-122">This documentation includes details and developer guidance for using the Dataverse Web API, including the following topics:</span></span>

- [<span data-ttu-id="a156f-123">Web API で Microsoft Dataverse を認証</span><span class="sxs-lookup"><span data-stu-id="a156f-123">Authenticate to Microsoft Dataverse with the Web API</span></span>](/powerapps/developer/data-platform/webapi/authenticate-web-api)
- [<span data-ttu-id="a156f-124">Web API を使用した操作の実行</span><span class="sxs-lookup"><span data-stu-id="a156f-124">Perform operations using the Web API</span></span>](/powerapps/developer/data-platform/webapi/perform-operations-web-api)
- [<span data-ttu-id="a156f-125">Web API で Postman を使用</span><span class="sxs-lookup"><span data-stu-id="a156f-125">Use Postman with the Web API</span></span>](/powerapps/developer/data-platform/webapi/use-postman-web-api)
- [<span data-ttu-id="a156f-126">変更追跡を使用した外部システムとのデータの同期</span><span class="sxs-lookup"><span data-stu-id="a156f-126">Use change tracking to synchronize data with external systems</span></span>](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)

### <a name="virtual-tables-for-human-resources-in-dataverse"></a><span data-ttu-id="a156f-127">Dataverse における Human Resources の仮想テーブル</span><span class="sxs-lookup"><span data-stu-id="a156f-127">Virtual tables for Human Resources in Dataverse</span></span>

<span data-ttu-id="a156f-128">給与統合 API のエンドポイントは、Microsoft Dataverse の仮想テーブル プラットフォーム機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="a156f-128">The endpoints for the Payroll integration API use the virtual table platform capabilities of Microsoft Dataverse.</span></span> <span data-ttu-id="a156f-129">既定では、仮想テーブルと関連する API エンドポイントは人事環境には配置されていないため、組織は環境で公開される OData エンドポイントを決定することができます。</span><span class="sxs-lookup"><span data-stu-id="a156f-129">By default, the virtual tables and their associated API endpoints aren't deployed for Human Resources environments, enabling organizations to determine which OData endpoints will be exposed for the environment.</span></span> <span data-ttu-id="a156f-130">このAPIを使用するには、その環境に対して Human Resources エンティティの仮想テーブルを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a156f-130">To use the API, the virtual tables for the Human Resources entities must be generated for the environment.</span></span>

<span data-ttu-id="a156f-131">API 用の仮想テーブルの生成の詳細については、[Dataverse 仮想テーブルの構成](./hr-admin-integration-common-data-service-virtual-entities.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a156f-131">For information on generating the virtual tables for the API, see [Configure Dataverse virtual tables](./hr-admin-integration-common-data-service-virtual-entities.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="a156f-132">データ モデル</span><span class="sxs-lookup"><span data-stu-id="a156f-132">Data model</span></span>

<span data-ttu-id="a156f-133">次の図では、API 内の関係性を示しています。</span><span class="sxs-lookup"><span data-stu-id="a156f-133">The following diagram illustrates relationships within the API.</span></span> <span data-ttu-id="a156f-134">Human Resources 内の既存のエンティティには、その他のエンティティに対する外部キーがあり、それについてはここでは示されていません。</span><span class="sxs-lookup"><span data-stu-id="a156f-134">Several types have foreign keys to other, pre-existing entities in Human Resources that aren't illustrated here.</span></span> <span data-ttu-id="a156f-135">このドキュメントでは、給与統合のシナリオに固有のエンティティに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="a156f-135">This document provides information on entities that are specific to payroll integration scenarios.</span></span> <span data-ttu-id="a156f-136">しかし、Human Resources 向け Dataverse Web API には他にも多くのエンティティが存在しており、これらのエンティティも統合に関連している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a156f-136">However, there are many other entities in the Dataverse Web API for Human Resources that may also be relevant to your integration.</span></span> <span data-ttu-id="a156f-137">これらのエンティティの一部は、外部キーとの関係性やナビゲーション プロパティで参照されます。</span><span class="sxs-lookup"><span data-stu-id="a156f-137">Some of these entities are referenced in foreign key relationships or navigation properties.</span></span>

![給与統合の API データ モデル](media/hr-admin-payroll-api-data-model.png)

## <a name="payroll-employee-and-related-entities"></a><span data-ttu-id="a156f-139">給与従業員および関連エンティティ</span><span class="sxs-lookup"><span data-stu-id="a156f-139">Payroll employee and related entities</span></span>

<span data-ttu-id="a156f-140">エンティティ:</span><span class="sxs-lookup"><span data-stu-id="a156f-140">Entities:</span></span>

- [<span data-ttu-id="a156f-141">給与従業員</span><span class="sxs-lookup"><span data-stu-id="a156f-141">Payroll employee</span></span>](hr-admin-integration-payroll-api-payroll-employee.md)
- [<span data-ttu-id="a156f-142">給与作業者の住所</span><span class="sxs-lookup"><span data-stu-id="a156f-142">Payroll worker address</span></span>](hr-admin-integration-payroll-api-payroll-worker-address.md)
- [<span data-ttu-id="a156f-143">固定報酬の報酬計画</span><span class="sxs-lookup"><span data-stu-id="a156f-143">Payroll fixed compensation plan</span></span>](hr-admin-integration-ats-api-recruiting-request-education.md)
- [<span data-ttu-id="a156f-144">給与職位職務</span><span class="sxs-lookup"><span data-stu-id="a156f-144">Payroll position job</span></span>](hr-admin-integration-payroll-api-payroll-position-job.md)
- [<span data-ttu-id="a156f-145">給与職位</span><span class="sxs-lookup"><span data-stu-id="a156f-145">Payroll position</span></span>](hr-admin-integration-payroll-api-payroll-position.md)

## <a name="see-also"></a><span data-ttu-id="a156f-146">参照</span><span class="sxs-lookup"><span data-stu-id="a156f-146">See also</span></span>

[<span data-ttu-id="a156f-147">給与エンティティの生成および確認</span><span class="sxs-lookup"><span data-stu-id="a156f-147">Generate and review payroll entities</span></span>](hr-admin-integration-payroll-api-generate-review-entities.md)<br>
[<span data-ttu-id="a156f-148">Human Resources パラメーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="a156f-148">Configure Human Resources parameters</span></span>](hr-setup-parameters.md)<br>
[<span data-ttu-id="a156f-149">Human Resources 共有パラメーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="a156f-149">Configure Human Resources shared parameters</span></span>](hr-setup-shared-parameters.md)<br>
[<span data-ttu-id="a156f-150">Microsoft Dataverse とは</span><span class="sxs-lookup"><span data-stu-id="a156f-150">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="a156f-151">Microsoft Dataverse Web API を使用する</span><span class="sxs-lookup"><span data-stu-id="a156f-151">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]