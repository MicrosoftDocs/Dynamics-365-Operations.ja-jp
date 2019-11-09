---
title: 資産グループへの共有資産とのれんの帳簿価額の配賦
description: この手順では、各資産グループへの共有資産と営業権の帳簿価額の配賦について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetImpairmentSharedAssetAlloc_JP, AssetImpairmentPopulateAllocation_JP
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 341b82dbcae56ddc6d700557b5193ef32f56faf5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183751"
---
# <a name="allocate-carrying-amount-of-shared-asset-and-goodwill-to-cash-generating-units"></a><span data-ttu-id="7caa1-103">資産グループへの共有資産とのれんの帳簿価額の配賦</span><span class="sxs-lookup"><span data-stu-id="7caa1-103">Allocate carrying amount of shared asset and goodwill to cash generating units</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7caa1-104">この手順では、各資産グループへの共有資産と営業権の帳簿価額の配賦について説明します。</span><span class="sxs-lookup"><span data-stu-id="7caa1-104">This procedure walks you through allocating the carrying amount of shared asset and goodwill to each of the cash generating units.</span></span> <span data-ttu-id="7caa1-105">配賦は CGU グループを有効化する前に行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="7caa1-105">The allocation must be done before activating the CGU group.</span></span>



<span data-ttu-id="7caa1-106">日本では、共有資産とのれんの減損会計に、次の 2 つの方法が許可されています。</span><span class="sxs-lookup"><span data-stu-id="7caa1-106">In Japan, impairment accounting for shared assets and goodwill is permitted for the following two methods:</span></span> 

<span data-ttu-id="7caa1-107">方法 1: キャッシュ生成単位 (CGU) より大きい単位を対象にする。</span><span class="sxs-lookup"><span data-stu-id="7caa1-107">Method 1: On a bigger unit than cash generating unit (CGU).</span></span> 

<span data-ttu-id="7caa1-108">方法 2: 共有資産 / 営業権の帳簿価額を CGU に配賦する。</span><span class="sxs-lookup"><span data-stu-id="7caa1-108">Method 2: Allocate carrying amount of shared asset/goodwill to CGUs.</span></span> 

<span data-ttu-id="7caa1-109">この手順は、方法 2 を使用した CGU グループにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="7caa1-109">This procedure applies to only the CGU groups that use method 2.</span></span> 



<span data-ttu-id="7caa1-110">この手順を完了する前に [固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7caa1-110">Before you can complete this procedure, you must select the Fixed Asset configuration key.</span></span>



<span data-ttu-id="7caa1-111">この手順は、デモ データ会社 JPMF を使用して完成されました。</span><span class="sxs-lookup"><span data-stu-id="7caa1-111">This procedure was completed using the demo data company JPMF.</span></span>



1. <span data-ttu-id="7caa1-112">[固定資産] > [設定] > [減損] > [共有資産と営業権の正味簿価額の配賦] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7caa1-112">Go to Fixed assets > Setup > Impairment > Allocation of net book value of shared assets and  goodwill.</span></span>
    * <span data-ttu-id="7caa1-113">営業権および共有資産の配賦は方法 2 を用いた CGU グループにのみ適用され、また配賦は CGU グループを有効化する前に行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="7caa1-113">The allocation of goodwill and shared assets is applicable only to the CGU groups with method 2, and the allocation has to be done before activating the CGU group.</span></span>  
2. <span data-ttu-id="7caa1-114">[割合] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7caa1-114">In the Proportion field, enter a number.</span></span>
3. <span data-ttu-id="7caa1-115">次の資産グループの選択</span><span class="sxs-lookup"><span data-stu-id="7caa1-115">Select the next cash generating unit</span></span>
4. <span data-ttu-id="7caa1-116">[割合] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7caa1-116">In the Proportion field, enter a number.</span></span>
5. <span data-ttu-id="7caa1-117">[配賦の設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7caa1-117">Click Populate allocation.</span></span>
    * <span data-ttu-id="7caa1-118">前のステップを繰り返して個別に比率をコンフィギュレーションすることもできます。</span><span class="sxs-lookup"><span data-stu-id="7caa1-118">You can also choose to repeat the previous steps to configure the proportions individually.</span></span>  
6. <span data-ttu-id="7caa1-119">一覧で、すべての行のマークを設定または解除します。</span><span class="sxs-lookup"><span data-stu-id="7caa1-119">In the list, mark or unmark all rows.</span></span>
7. <span data-ttu-id="7caa1-120">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7caa1-120">Click OK.</span></span>
