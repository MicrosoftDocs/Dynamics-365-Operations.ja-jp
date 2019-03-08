---
title: 設備グループの作成および割り当て
description: この手順では、設備のグループの作成方法と設備グループの固定資産へのコンフィギュレーション方法について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetAcceleratedDepEquipmentGroup_JP, AssetTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2a23bc5aa021365e06f7f2455045f9e11b549dfe
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "371128"
---
# <a name="create-and-assign-an-equipment-group"></a><span data-ttu-id="0c7cd-103">設備グループの作成および割り当て</span><span class="sxs-lookup"><span data-stu-id="0c7cd-103">Create and assign an equipment group</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0c7cd-104">この手順では、設備のグループの作成方法と設備グループの固定資産へのコンフィギュレーション方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0c7cd-104">Use this procedure to learn how to create an equipment group and configure an equipment group it to a fixed asset.</span></span>



<span data-ttu-id="0c7cd-105">設備のグループは、加速償却ドキュメントを作成する際の既定値を提供します。</span><span class="sxs-lookup"><span data-stu-id="0c7cd-105">The equipment groups provide default values when creating an accelerated depreciation document.</span></span>



<span data-ttu-id="0c7cd-106">この手順を完了するためには、[資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c7cd-106">In order to complete this procedure, the Asset configuration key must be selected.</span></span>



<span data-ttu-id="0c7cd-107">この手順は、デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="0c7cd-107">This procedure was created using the demo data company JPMF.</span></span>


## <a name="create-equipment-group"></a><span data-ttu-id="0c7cd-108">設備グループの作成</span><span class="sxs-lookup"><span data-stu-id="0c7cd-108">Create equipment group</span></span>
1. <span data-ttu-id="0c7cd-109">[固定資産] > [設定] > [設備グループ] に移動します。</span><span class="sxs-lookup"><span data-stu-id="0c7cd-109">Go to Fixed assets > Setup > Equipment group.</span></span>
2. <span data-ttu-id="0c7cd-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c7cd-110">Click New.</span></span>
3. <span data-ttu-id="0c7cd-111">[固定資産設備グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0c7cd-111">In the Fixed asset equipment group field, type a value.</span></span>
4. <span data-ttu-id="0c7cd-112">[説明] フィールドで値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0c7cd-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0c7cd-113">[設備のタイプ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0c7cd-113">In the Equipment type field, type a value.</span></span>
6. <span data-ttu-id="0c7cd-114">[場所] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0c7cd-114">In the Location field, type a value.</span></span>
    * <span data-ttu-id="0c7cd-115">これが加速償却ドキュメントを作成する際の既定値になります。</span><span class="sxs-lookup"><span data-stu-id="0c7cd-115">This will be the default value when you create an accelerated depreciation document.</span></span>  
7. <span data-ttu-id="0c7cd-116">[設備のタイプ区分] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0c7cd-116">In the Equipment type division field, type a value.</span></span>
8. <span data-ttu-id="0c7cd-117">[業種の 1 日あたりの平均時間] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0c7cd-117">In the Industry average hours per day field, enter a number.</span></span>
    * <span data-ttu-id="0c7cd-118">これが加速償却ドキュメントを作成する際の既定値になります。</span><span class="sxs-lookup"><span data-stu-id="0c7cd-118">This will be the default value when you create an accelerated depreciation document.</span></span>  
9. <span data-ttu-id="0c7cd-119">[年間の平均稼働日] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0c7cd-119">In the Industry annual working days field, enter a number.</span></span>
    * <span data-ttu-id="0c7cd-120">これが加速償却ドキュメントを作成する際の既定値になります。</span><span class="sxs-lookup"><span data-stu-id="0c7cd-120">This will be the default value when you create an accelerated depreciation document.</span></span>  
10. <span data-ttu-id="0c7cd-121">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c7cd-121">Click Save.</span></span>

## <a name="configure-default-equipment-group-on-fixed-assets"></a><span data-ttu-id="0c7cd-122">固定資産の既定の設備グループのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="0c7cd-122">Configure default equipment group on fixed assets</span></span>
1. <span data-ttu-id="0c7cd-123">[固定資産] > [固定資産] > [固定資産] に移動します。</span><span class="sxs-lookup"><span data-stu-id="0c7cd-123">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="0c7cd-124">設備グループを割り当てる固定資産の選択</span><span class="sxs-lookup"><span data-stu-id="0c7cd-124">Select the fixed asset that you would like to assign the equipment group to</span></span>
3. <span data-ttu-id="0c7cd-125">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c7cd-125">Click Edit.</span></span>
4. <span data-ttu-id="0c7cd-126">[固定資産設備グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0c7cd-126">In the Fixed asset equipment group field, type a value.</span></span>
5. <span data-ttu-id="0c7cd-127">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c7cd-127">Click Save.</span></span>

