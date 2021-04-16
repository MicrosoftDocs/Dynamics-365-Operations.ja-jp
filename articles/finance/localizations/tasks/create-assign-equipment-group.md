---
title: 設備グループの作成および割り当て
description: この手順では、設備のグループの作成方法と設備グループの固定資産へのコンフィギュレーション方法について説明します。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetAcceleratedDepEquipmentGroup_JP, AssetTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2753b3d8e5c7861b16aaea73f541e56a250eb998
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821853"
---
# <a name="create-and-assign-an-equipment-group"></a><span data-ttu-id="d30bf-103">設備グループの作成および割り当て</span><span class="sxs-lookup"><span data-stu-id="d30bf-103">Create and assign an equipment group</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d30bf-104">この手順では、設備のグループの作成方法と設備グループの固定資産へのコンフィギュレーション方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d30bf-104">Use this procedure to learn how to create an equipment group and configure an equipment group it to a fixed asset.</span></span>



<span data-ttu-id="d30bf-105">設備のグループは、加速償却ドキュメントを作成する際の既定値を提供します。</span><span class="sxs-lookup"><span data-stu-id="d30bf-105">The equipment groups provide default values when creating an accelerated depreciation document.</span></span>



<span data-ttu-id="d30bf-106">この手順を完了するためには、[資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d30bf-106">In order to complete this procedure, the Asset configuration key must be selected.</span></span>



<span data-ttu-id="d30bf-107">この手順は、デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="d30bf-107">This procedure was created using the demo data company JPMF.</span></span>


## <a name="create-equipment-group"></a><span data-ttu-id="d30bf-108">設備グループの作成</span><span class="sxs-lookup"><span data-stu-id="d30bf-108">Create equipment group</span></span>
1. <span data-ttu-id="d30bf-109">[固定資産] > [設定] > [設備グループ] に移動します。</span><span class="sxs-lookup"><span data-stu-id="d30bf-109">Go to Fixed assets > Setup > Equipment group.</span></span>
2. <span data-ttu-id="d30bf-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d30bf-110">Click New.</span></span>
3. <span data-ttu-id="d30bf-111">[固定資産設備グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d30bf-111">In the Fixed asset equipment group field, type a value.</span></span>
4. <span data-ttu-id="d30bf-112">[説明] フィールドで値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d30bf-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d30bf-113">[設備のタイプ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d30bf-113">In the Equipment type field, type a value.</span></span>
6. <span data-ttu-id="d30bf-114">[場所] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d30bf-114">In the Location field, type a value.</span></span>
    * <span data-ttu-id="d30bf-115">これが加速償却ドキュメントを作成する際の既定値になります。</span><span class="sxs-lookup"><span data-stu-id="d30bf-115">This will be the default value when you create an accelerated depreciation document.</span></span>  
7. <span data-ttu-id="d30bf-116">[設備のタイプ区分] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d30bf-116">In the Equipment type division field, type a value.</span></span>
8. <span data-ttu-id="d30bf-117">[業種の 1 日あたりの平均時間] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d30bf-117">In the Industry average hours per day field, enter a number.</span></span>
    * <span data-ttu-id="d30bf-118">これが加速償却ドキュメントを作成する際の既定値になります。</span><span class="sxs-lookup"><span data-stu-id="d30bf-118">This will be the default value when you create an accelerated depreciation document.</span></span>  
9. <span data-ttu-id="d30bf-119">[年間の平均稼働日] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d30bf-119">In the Industry annual working days field, enter a number.</span></span>
    * <span data-ttu-id="d30bf-120">これが加速償却ドキュメントを作成する際の既定値になります。</span><span class="sxs-lookup"><span data-stu-id="d30bf-120">This will be the default value when you create an accelerated depreciation document.</span></span>  
10. <span data-ttu-id="d30bf-121">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d30bf-121">Click Save.</span></span>

## <a name="configure-default-equipment-group-on-fixed-assets"></a><span data-ttu-id="d30bf-122">固定資産の既定の設備グループのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="d30bf-122">Configure default equipment group on fixed assets</span></span>
1. <span data-ttu-id="d30bf-123">[固定資産] > [固定資産] > [固定資産] に移動します。</span><span class="sxs-lookup"><span data-stu-id="d30bf-123">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="d30bf-124">設備グループを割り当てる固定資産の選択</span><span class="sxs-lookup"><span data-stu-id="d30bf-124">Select the fixed asset that you would like to assign the equipment group to</span></span>
3. <span data-ttu-id="d30bf-125">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d30bf-125">Click Edit.</span></span>
4. <span data-ttu-id="d30bf-126">[固定資産設備グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d30bf-126">In the Fixed asset equipment group field, type a value.</span></span>
5. <span data-ttu-id="d30bf-127">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d30bf-127">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]