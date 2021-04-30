---
title: 指標金利の設定
description: このトピックでは、指標金利を設定する方法について説明します。 指標金利は、組織がリース支払額を一連の指標金利に関連付ける場合に必要です。
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseIndexRateType
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 40f230a9d69a142b18eb27a2d5e420dbadc600d2
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880963"
---
# <a name="set-up-index-rates"></a><span data-ttu-id="50685-104">指標金利の設定</span><span class="sxs-lookup"><span data-stu-id="50685-104">Set up index rates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="50685-105">リース支払が指標に依存している場合は、システムで指標金利タイプを追加および管理できます。</span><span class="sxs-lookup"><span data-stu-id="50685-105">If lease payments depend on an index, the index rate types can be added and maintained in the system.</span></span> <span data-ttu-id="50685-106">**指標金利タイプ** ページからのリース支払を再評価する場合、指標金利の再評価プロセスでは、再評価日から見て最新の指標金利が使用されます。</span><span class="sxs-lookup"><span data-stu-id="50685-106">To revalue the lease payments from the **Index rate type** page, the index rate revaluation process uses the most recent index rate from the date of revaluation.</span></span>

<span data-ttu-id="50685-107">指標金利タイプと指標金利を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="50685-107">To add index rate types and index rates, follow these steps.</span></span>

1. <span data-ttu-id="50685-108">**資産リース \> 設定 \> 指標金利タイプ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="50685-108">Go to **Asset leasing \> Setup \> Index rate type**.</span></span>
2. <span data-ttu-id="50685-109">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50685-109">Select **New**.</span></span>
3. <span data-ttu-id="50685-110">適切なフィールドで、レート タイプと指標金利の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="50685-110">In the appropriate fields, enter the rate type and the name of the index rate.</span></span>
4. <span data-ttu-id="50685-111">新しい指標金利の値を追加するには、指標金利タイプを選択し、**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50685-111">To add a new index rate value, select the index rate type, and then select **Add**.</span></span>
5. <span data-ttu-id="50685-112">レートの有効開始日を選択し、レート値を選択します。</span><span class="sxs-lookup"><span data-stu-id="50685-112">Select the effective start date of the rate, and select the rate value.</span></span>

<span data-ttu-id="50685-113">**指標金利値の差** または **指標金利値** を指標金利の方法として選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="50685-113">You must select either **Index rate value difference** or **Index rate value** as the index rate method.</span></span>

- <span data-ttu-id="50685-114">開始日時点の指標金利と最新の指標金利の差に基づいて、新しいリース支払を計算する **指標金利値の差** の方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="50685-114">Select the **Index rate value difference** method to calculate a new lease payment, based on the difference between the index rate on the start date and the most recent index rate.</span></span> <span data-ttu-id="50685-115">指標金利は、**指標金利 (%)** フィールドで定義されます。</span><span class="sxs-lookup"><span data-stu-id="50685-115">The index rate is defined in the **Index rate (%)** field.</span></span>
- <span data-ttu-id="50685-116">**指標金利値** の方法を選択して、**指標金利 (%)** フィールドに指定されている割合を使用してリース支払を計算します。</span><span class="sxs-lookup"><span data-stu-id="50685-116">Select the **Index rate value** method to calculate the lease payment by using the percentage that is specified in the **Index rate (%)** field.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
