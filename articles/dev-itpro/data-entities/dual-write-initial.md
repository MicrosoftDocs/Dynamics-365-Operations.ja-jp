---
title: Finance and Operations と Common Data Service の初期同期に対する執行命令
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
ms.openlocfilehash: b74bc2d3133af7e87663a4e6bafb8780e0a6a66f
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797301"
---
# <a name="execution-order-for-initial-sychronization-of-finance-and-operations-and-common-data-service"></a><span data-ttu-id="18442-103">Finance and Operations と Common Data Service の初期同期に対する執行命令</span><span class="sxs-lookup"><span data-stu-id="18442-103">Execution order for initial sychronization of Finance and Operations and Common Data Service</span></span>

<span data-ttu-id="18442-104">データ統合を使用する前に、顧客、仕入先、および取引先担当者に必要な初期データを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="18442-104">Before you use data integration, you must create the initial data required for customers, vendors and contacts.</span></span> <span data-ttu-id="18442-105">たとえば、新しい**仕入先グループ**品目を作成し、その**支払条件**を **Net30** として設定する場合、**仕入先グループ**品目の作成を試みる前に、**Net30** が Finance and Operations と Common Data Service 両方に存在しすることを確認します。</span><span class="sxs-lookup"><span data-stu-id="18442-105">For example, if you want to create a new **Vendor group** item and set its **Terms of Payment** as **Net30**, then before you attempt to create the **Vendor group** item you need to make sure that **Net30** exists in both Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="18442-106">(将来的には、**初期同期**と呼ばれるデュアル書き込みプラットフォーム機能をリリースする予定です。デュアル書き込みセットアップの一部として Finance and Operations と Common Data Service 間で 1 回限りのデータ同期が行われます)</span><span class="sxs-lookup"><span data-stu-id="18442-106">(In the future, we will release a  dual-write platform functionality called **Initial Sync**. It will do a one-time data synchronization between Finance and Operations and Common Data Service as part of the dual-write setup.)</span></span>

<span data-ttu-id="18442-107">ヒント: **支払条件** (支払条件) を含むすべての参照データのデュアル書き込みマップをリリースします。</span><span class="sxs-lookup"><span data-stu-id="18442-107">Tips: We are releasing a dual-write map for all reference data including **Terms of Payment** (Payment Terms).</span></span> <span data-ttu-id="18442-108">1 つのシステムに初期データが既に含まれる場合は、レコードの小さな更新操作によって、そのレコードのデュアル書き込みをトリガーできます。</span><span class="sxs-lookup"><span data-stu-id="18442-108">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span> 

<span data-ttu-id="18442-109">次の優先順位に従い、初期データが Finance and Operations と Common Data Service の両方で使用できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="18442-109">You must follow the following order of precedence and make sure that the initial data is available on both Finance and Operations and Common Data Service.</span></span>   

## <a name="vendor"></a><span data-ttu-id="18442-110">仕入先</span><span class="sxs-lookup"><span data-stu-id="18442-110">Vendor</span></span>

<span data-ttu-id="18442-111">仕入先の実行順序は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="18442-111">The order of execution for Vendor is:</span></span>

```
Vendor Group
    Terms of payment
        Payment day & lines
        Payment schedule
Vendor payment method
```

## <a name="customer-organization"></a><span data-ttu-id="18442-112">顧客 (組織)</span><span class="sxs-lookup"><span data-stu-id="18442-112">Customer (Organization)</span></span>

<span data-ttu-id="18442-113">顧客の実行順序は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="18442-113">The order of execution for Customer is:</span></span>

```
Customer Group
    Terms of payment
        Payment day & lines
        Payment 
Customer payment method
```

## <a name="contact-person"></a><span data-ttu-id="18442-114">連絡先 (名前)</span><span class="sxs-lookup"><span data-stu-id="18442-114">Contact (Person)</span></span>

<span data-ttu-id="18442-115">連絡先の実行順序は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="18442-115">The order of execution for Contact is:</span></span>

```
Customer
Vendor               
```
