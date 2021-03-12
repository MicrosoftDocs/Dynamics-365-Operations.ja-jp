---
title: サービス期間の設定
description: サービス間隔は、サービス注文を作成する場合に、サービス契約項目に対してサービス注文明細行が作成される頻度を表します。
author: ShylaThompson
manager: tfehr
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementinterval
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 815da6b24de401ad11febb0b0564738ce6967a9c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991668"
---
# <a name="set-up-service-intervals"></a><span data-ttu-id="426a8-103">サービス期間の設定</span><span class="sxs-lookup"><span data-stu-id="426a8-103">Set up service intervals</span></span>  

[!include [banner](../includes/banner.md)]

<span data-ttu-id="426a8-104">サービス間隔は、サービス注文を作成する場合に、サービス契約項目に対してサービス注文明細行が作成される頻度を表します。</span><span class="sxs-lookup"><span data-stu-id="426a8-104">Service interval indicates the frequency with which service order lines are created for service agreement lines when you create service orders.</span></span>

1. <span data-ttu-id="426a8-105">**サービス管理** \> **設定** \> **サービス契約** \> **サービス期間** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="426a8-105">Click **Service management** \> **Setup** \> **Service agreements** \> **Service intervals**.</span></span>
2. <span data-ttu-id="426a8-106">新しいサービス期間を作成します。</span><span class="sxs-lookup"><span data-stu-id="426a8-106">Create a new service interval.</span></span>
3. <span data-ttu-id="426a8-107">サービス期間の ID と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="426a8-107">Enter the ID and description of the service interval.</span></span>
4. <span data-ttu-id="426a8-108">**範囲** フィールドで範囲を選択します。</span><span class="sxs-lookup"><span data-stu-id="426a8-108">In the **Range** field, select the range.</span></span>
5. <span data-ttu-id="426a8-109">**頻度** フィールドに、頻度をタイプします。</span><span class="sxs-lookup"><span data-stu-id="426a8-109">In the **Frequency** field, type the frequency.</span></span> <span data-ttu-id="426a8-110">サービス契約の期間を算出するには、この頻度を係数として範囲と掛け合わせます。</span><span class="sxs-lookup"><span data-stu-id="426a8-110">The frequency is the factor by which you must multiply the range to obtain the interval for a service agreement.</span></span>
6. <span data-ttu-id="426a8-111">**Alt + S** キーを押してサービス期間を保存します。</span><span class="sxs-lookup"><span data-stu-id="426a8-111">Press **Alt+S** to save the service interval.</span></span>

## <a name="example"></a><span data-ttu-id="426a8-112">例</span><span class="sxs-lookup"><span data-stu-id="426a8-112">Example</span></span>

<span data-ttu-id="426a8-113">10 日間のサービス期間を作成するとします。</span><span class="sxs-lookup"><span data-stu-id="426a8-113">You want to create a service interval of 10 days.</span></span>

<span data-ttu-id="426a8-114">**10 日間のサービス期間の作成**</span><span class="sxs-lookup"><span data-stu-id="426a8-114">**Create a 10-day service interval**</span></span>

1. <span data-ttu-id="426a8-115">**サービス管理** \> **設定** \> **サービス契約** \> **サービス期間** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="426a8-115">Click **Service management** \> **Setup** \> **Service agreements** \> **Service intervals**.</span></span>
2. <span data-ttu-id="426a8-116">新しいサービス期間を作成します。</span><span class="sxs-lookup"><span data-stu-id="426a8-116">Create a new service interval.</span></span>
3. <span data-ttu-id="426a8-117">サービス期間の ID と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="426a8-117">Enter the ID and description of the service interval.</span></span>
4. <span data-ttu-id="426a8-118">**範囲** フィールドで **毎日** を選択します。</span><span class="sxs-lookup"><span data-stu-id="426a8-118">In the **Range** field, select **Daily**.</span></span>
5. <span data-ttu-id="426a8-119">**頻度** フィールドに 10 を入力します。</span><span class="sxs-lookup"><span data-stu-id="426a8-119">In the **Frequency** field, type 10.</span></span>
6. <span data-ttu-id="426a8-120">**Alt + S** キーを押してサービス期間を保存します。</span><span class="sxs-lookup"><span data-stu-id="426a8-120">Press **Alt+S** to save the service interval.</span></span>

## <a name="related-topics"></a><span data-ttu-id="426a8-121">関連トピック</span><span class="sxs-lookup"><span data-stu-id="426a8-121">Related topics</span></span>

[<span data-ttu-id="426a8-122">サービス期間</span><span class="sxs-lookup"><span data-stu-id="426a8-122">Service intervals</span></span>](service-intervals.md)  
