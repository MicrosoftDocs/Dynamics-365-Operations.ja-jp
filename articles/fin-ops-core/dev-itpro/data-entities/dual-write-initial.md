---
title: Finance and Operations アプリおよび Common Data Service の初期同期の実行順序
description: このトピックでは、初期データを作成するために従う必要がある同期の順序を指定します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: cf444ef1192fed3a6a49282da37374dd8c443356
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769640"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-apps-and-common-data-service"></a><span data-ttu-id="bb1ba-103">Finance and Operations アプリおよび Common Data Service の初期同期の実行順序</span><span class="sxs-lookup"><span data-stu-id="bb1ba-103">Execution order for initial synchronization of Finance and Operations apps and Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bb1ba-104">データ統合を使用する前に、顧客、仕入先、および取引先担当者に必要な初期データを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bb1ba-104">Before you use data integration, you must create the initial data that is required for customers, vendors, and contacts.</span></span> <span data-ttu-id="bb1ba-105">たとえば、新しい**仕入先グループ**の品目を作成し、**支払条件**の値を **Net30** に設定するとします。</span><span class="sxs-lookup"><span data-stu-id="bb1ba-105">For example, you want to create a new **Vendor group** item and set its **Terms of Payment** value to **Net30**.</span></span> <span data-ttu-id="bb1ba-106">この場合、**仕入先グループ**の品目を作成する前に、**Net30** がアプリケーションおよび Common Data Service の両方に存在することを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bb1ba-106">In this case, before you try to create the **Vendor group** item, you must make sure that **Net30** exists in both the application and Common Data Service.</span></span> <span data-ttu-id="bb1ba-107">(将来的には、Microsoft は初期同期と呼ばれるデュアル書き込みプラットフォーム機能をリリースする予定です。この機能によりデュアル書き込みセットアップの一部としてアプリケーションおよび Common Data Service 間で 1 回限りのデータ同期が行われます。)</span><span class="sxs-lookup"><span data-stu-id="bb1ba-107">(In the future, Microsoft will release dual-write platform functionality that is named Initial Sync. This functionality will do a one-time data synchronization between the application and Common Data Service as part of the dual-write setup.)</span></span>

> [!TIP]
> <span data-ttu-id="bb1ba-108">Microsoft は**支払条件** (支払条件) を含む、すべての参照データのデュアル書き込みマップをリリースします。</span><span class="sxs-lookup"><span data-stu-id="bb1ba-108">Microsoft is releasing a dual-write map for all reference data, including **Terms of Payment** (payment terms).</span></span> <span data-ttu-id="bb1ba-109">1 つのシステムに初期データが既に含まれる場合は、レコードの小さな更新操作によって、そのレコードのデュアル書き込みをトリガーできます。</span><span class="sxs-lookup"><span data-stu-id="bb1ba-109">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span>

<span data-ttu-id="bb1ba-110">次の優先順位に従い、初期データがアプリケーションと Common Data Service の両方で使用できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="bb1ba-110">You must follow the following order of precedence and make sure that the initial data is available in the application and Common Data Service.</span></span>

## <a name="vendor"></a><span data-ttu-id="bb1ba-111">仕入先</span><span class="sxs-lookup"><span data-stu-id="bb1ba-111">Vendor</span></span>

<span data-ttu-id="bb1ba-112">**仕入先**エンティティに対する実行の順序を次に示します。</span><span class="sxs-lookup"><span data-stu-id="bb1ba-112">Here is the order of execution for the **Vendor** entity:</span></span>

1. <span data-ttu-id="bb1ba-113">仕入先グループ</span><span class="sxs-lookup"><span data-stu-id="bb1ba-113">Vendor group</span></span>

    1. <span data-ttu-id="bb1ba-114">支払条件</span><span class="sxs-lookup"><span data-stu-id="bb1ba-114">Terms of payment</span></span>

        1. <span data-ttu-id="bb1ba-115">支払期日および明細行</span><span class="sxs-lookup"><span data-stu-id="bb1ba-115">Payment day and lines</span></span>
        2. <span data-ttu-id="bb1ba-116">支払スケジュール</span><span class="sxs-lookup"><span data-stu-id="bb1ba-116">Payment schedule</span></span>

2. <span data-ttu-id="bb1ba-117">仕入先支払方法</span><span class="sxs-lookup"><span data-stu-id="bb1ba-117">Vendor payment method</span></span>

## <a name="customer-organization"></a><span data-ttu-id="bb1ba-118">顧客 (組織)</span><span class="sxs-lookup"><span data-stu-id="bb1ba-118">Customer (Organization)</span></span>

<span data-ttu-id="bb1ba-119">**顧客**エンティティに対する実行の順序を次に示します。</span><span class="sxs-lookup"><span data-stu-id="bb1ba-119">Here is the order of execution for the **Customer** entity:</span></span>

1. <span data-ttu-id="bb1ba-120">顧客グループ</span><span class="sxs-lookup"><span data-stu-id="bb1ba-120">Customer group</span></span>

    1. <span data-ttu-id="bb1ba-121">支払条件</span><span class="sxs-lookup"><span data-stu-id="bb1ba-121">Terms of payment</span></span>

        1. <span data-ttu-id="bb1ba-122">支払期日および明細行</span><span class="sxs-lookup"><span data-stu-id="bb1ba-122">Payment day and lines</span></span>
        2. <span data-ttu-id="bb1ba-123">支払</span><span class="sxs-lookup"><span data-stu-id="bb1ba-123">Payment</span></span> 

2. <span data-ttu-id="bb1ba-124">顧客支払方法</span><span class="sxs-lookup"><span data-stu-id="bb1ba-124">Customer payment method</span></span>

## <a name="contact-person"></a><span data-ttu-id="bb1ba-125">連絡先 (名前)</span><span class="sxs-lookup"><span data-stu-id="bb1ba-125">Contact (Person)</span></span>

<span data-ttu-id="bb1ba-126">**連絡先**エンティティに対する実行の順序を次に示します。</span><span class="sxs-lookup"><span data-stu-id="bb1ba-126">Here is the order of execution for the **Contact** entity:</span></span>

1. <span data-ttu-id="bb1ba-127">顧客</span><span class="sxs-lookup"><span data-stu-id="bb1ba-127">Customer</span></span>
2. <span data-ttu-id="bb1ba-128">仕入先</span><span class="sxs-lookup"><span data-stu-id="bb1ba-128">Vendor</span></span>
