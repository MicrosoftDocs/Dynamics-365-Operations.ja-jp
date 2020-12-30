---
title: 資産および資産タイプに対する保証
description: このトピックでは、資産管理で資産および資産タイプの保証を設定する方法について説明します。
author: josaw1
manager: tfehr
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 75de9a51560dcd8fea7998425fee14a27e891972
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432102"
---
# <a name="warranties-on-assets-and-asset-types"></a><span data-ttu-id="dd8f9-103">資産および資産タイプに対する保証</span><span class="sxs-lookup"><span data-stu-id="dd8f9-103">Warranties on assets and asset types</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="dd8f9-104">このトピックでは、資産管理で資産および資産タイプの保証を設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="dd8f9-104">This topic explains how to set up warranties on assets and asset types in Asset Management.</span></span>

## <a name="set-up-a-warranty-on-an-asset-type"></a><span data-ttu-id="dd8f9-105">資産タイプに対する保証の設定</span><span class="sxs-lookup"><span data-stu-id="dd8f9-105">Set up a warranty on an asset type</span></span>

1. <span data-ttu-id="dd8f9-106">**資産管理** \> **設定** \> **資産タイプ** \> **資産タイプ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dd8f9-106">Select **Asset management** \> **Setup** \> **Asset types** \> **Asset types**.</span></span>
2. <span data-ttu-id="dd8f9-107">左ウィンドウで、仕入先保証契約を関連付ける資産タイプを選択し、**資産タイプの既定値** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dd8f9-107">In the left pane, select the asset type to attach a vendor warranty agreement to, and then select **Asset type defaults**.</span></span>
3. <span data-ttu-id="dd8f9-108">**一般** クイックタブの、**仕入先保証** フィールドで、契約を選択します。</span><span class="sxs-lookup"><span data-stu-id="dd8f9-108">On the **General** FastTab, in the **Vendor warranty** field, select the agreement.</span></span>

## <a name="set-up-a-warranty-on-an-asset"></a><span data-ttu-id="dd8f9-109">資産に対する保証の設定</span><span class="sxs-lookup"><span data-stu-id="dd8f9-109">Set up a warranty on an asset</span></span>

1. <span data-ttu-id="dd8f9-110">**資産管理** \> **共通** \> **資産** \> **全資産** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dd8f9-110">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="dd8f9-111">資産を選択し、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dd8f9-111">Select the asset, and then select **Edit**.</span></span>
3. <span data-ttu-id="dd8f9-112">**仕入先** クイック タブ、**仕入先保証** セクションの **保証** フィールドで、保証契約を選択します。</span><span class="sxs-lookup"><span data-stu-id="dd8f9-112">On the **Vendor** FastTab, in the **Vendor warranty** section, in the **Warranty** field, select the warranty agreement.</span></span>
4. <span data-ttu-id="dd8f9-113">**保証開始日** と **保証終了日** フィールドで、開始日と終了日を選択します。</span><span class="sxs-lookup"><span data-stu-id="dd8f9-113">In the **Warranty start** and **Warranty end** fields, select the start and end dates.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="dd8f9-114">ワーク オーダーの **保証開始日** フィールドで日付が選択されている場合、保証はその日付のワーク オーダーに対して有効になります。</span><span class="sxs-lookup"><span data-stu-id="dd8f9-114">If a date is selected in the **Warranty start** field on a work order, the warranty becomes valid for the work order on that date.</span></span> <span data-ttu-id="dd8f9-115">ワーク オーダーを作成すると、**保証開始日** フィールドは自動的に作成日に設定されます。</span><span class="sxs-lookup"><span data-stu-id="dd8f9-115">When you create a work order, the **Warranty start** field is automatically set to the date of creation.</span></span> <span data-ttu-id="dd8f9-116">ただし、この日付は、保証契約の開始日などに変更することができます。</span><span class="sxs-lookup"><span data-stu-id="dd8f9-116">However, you can change the date so that it corresponds to, for example, the start date of a warranty agreement.</span></span>
    >
    > ![ワーク オーダー ページ](media/02-warranty.png)

> [!NOTE]
> <span data-ttu-id="dd8f9-118">仕入先保証の対象となる資産のワーク オーダーを作成する場合、そのワーク オーダーの期間中に予定された開始日があると、保証契約に関する通知が表示されます。</span><span class="sxs-lookup"><span data-stu-id="dd8f9-118">When you create a work order for an asset that is covered by a vendor warranty, if the work order has an expected start date during the warranty period, you receive a notification about the warranty agreement.</span></span> <span data-ttu-id="dd8f9-119">その後、必要に応じて、ワーク オーダーをキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="dd8f9-119">You can then cancel the work order, as you require.</span></span>
