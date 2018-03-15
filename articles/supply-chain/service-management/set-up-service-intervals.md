---
title: "サービス期間の設定"
description: "サービス間隔は、サービス注文を作成する場合に、サービス契約項目に対してサービス注文明細行が作成される頻度を表します。"
author: YuyuScheller
manager: AnnBe
ms.date: 02/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementinterval
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 4ea10e4c0fbfd21538bba16d2b01deb3e4b3a10d
ms.openlocfilehash: 03ebf4fd4615eac77e6f990a2d4e7f7326c0d257
ms.contentlocale: ja-jp
ms.lasthandoff: 02/20/2018

---

# <a name="set-up-service-intervals"></a><span data-ttu-id="f8ca5-103">サービス期間の設定</span><span class="sxs-lookup"><span data-stu-id="f8ca5-103">Set up service intervals</span></span>  

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f8ca5-104">サービス間隔は、サービス注文を作成する場合に、サービス契約項目に対してサービス注文明細行が作成される頻度を表します。</span><span class="sxs-lookup"><span data-stu-id="f8ca5-104">Service interval indicates the frequency with which service order lines are created for service agreement lines when you create service orders.</span></span>

1. <span data-ttu-id="f8ca5-105">**サービス管理** \> **設定** \> **サービス契約** \> **サービス期間**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8ca5-105">Click **Service management** \> **Setup** \> **Service agreements** \> **Service intervals**.</span></span>
2. <span data-ttu-id="f8ca5-106">新しいサービス期間を作成します。</span><span class="sxs-lookup"><span data-stu-id="f8ca5-106">Create a new service interval.</span></span>
3. <span data-ttu-id="f8ca5-107">サービス期間の ID と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8ca5-107">Enter the ID and description of the service interval.</span></span>
4. <span data-ttu-id="f8ca5-108">**範囲** フィールドで範囲を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8ca5-108">In the **Range** field, select the range.</span></span>
5. <span data-ttu-id="f8ca5-109">**頻度** フィールドに、頻度をタイプします。</span><span class="sxs-lookup"><span data-stu-id="f8ca5-109">In the **Frequency** field, type the frequency.</span></span> <span data-ttu-id="f8ca5-110">サービス契約の期間を算出するには、この頻度を係数として範囲と掛け合わせます。</span><span class="sxs-lookup"><span data-stu-id="f8ca5-110">The frequency is the factor by which you must multiply the range to obtain the interval for a service agreement.</span></span>
6. <span data-ttu-id="f8ca5-111">**Alt + S** キーを押してサービス期間を保存します。</span><span class="sxs-lookup"><span data-stu-id="f8ca5-111">Press **Alt+S** to save the service interval.</span></span>

## <a name="example"></a><span data-ttu-id="f8ca5-112">例</span><span class="sxs-lookup"><span data-stu-id="f8ca5-112">Example</span></span>

<span data-ttu-id="f8ca5-113">10 日間のサービス期間を作成するとします。</span><span class="sxs-lookup"><span data-stu-id="f8ca5-113">You want to create a service interval of 10 days.</span></span>

<span data-ttu-id="f8ca5-114">**10 日間のサービス期間の作成**</span><span class="sxs-lookup"><span data-stu-id="f8ca5-114">**Create a 10-day service interval**</span></span>

1. <span data-ttu-id="f8ca5-115">**サービス管理** \> **設定** \> **サービス契約** \> **サービス期間**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8ca5-115">Click **Service management** \> **Setup** \> **Service agreements** \> **Service intervals**.</span></span>
2. <span data-ttu-id="f8ca5-116">新しいサービス期間を作成します。</span><span class="sxs-lookup"><span data-stu-id="f8ca5-116">Create a new service interval.</span></span>
3. <span data-ttu-id="f8ca5-117">サービス期間の ID と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8ca5-117">Enter the ID and description of the service interval.</span></span>
4. <span data-ttu-id="f8ca5-118">**範囲** フィールドで **毎日**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8ca5-118">In the **Range** field, select **Daily**.</span></span>
5. <span data-ttu-id="f8ca5-119">**頻度** フィールドに 10 を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8ca5-119">In the **Frequency** field, type 10.</span></span>
6. <span data-ttu-id="f8ca5-120">**Alt + S** キーを押してサービス期間を保存します。</span><span class="sxs-lookup"><span data-stu-id="f8ca5-120">Press **Alt+S** to save the service interval.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f8ca5-121">関連トピック</span><span class="sxs-lookup"><span data-stu-id="f8ca5-121">Related topics</span></span>

[<span data-ttu-id="f8ca5-122">サービス期間</span><span class="sxs-lookup"><span data-stu-id="f8ca5-122">Service intervals</span></span>](service-intervals.md)  

