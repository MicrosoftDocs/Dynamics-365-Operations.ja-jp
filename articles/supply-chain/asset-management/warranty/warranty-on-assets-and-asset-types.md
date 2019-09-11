---
title: 資産および資産タイプに対する保証
description: このトピックでは、資産管理で資産および資産タイプの保証を設定する方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3b13f8aba7e1d2448495f97a4772eb573e08c025
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874604"
---
# <a name="warranty-on-assets-and-asset-types"></a><span data-ttu-id="1fad6-103">資産および資産タイプに対する保証</span><span class="sxs-lookup"><span data-stu-id="1fad6-103">Warranty on assets and asset types</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="1fad6-104">このトピックでは、資産管理で資産および資産タイプの保証を設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1fad6-104">This topic explains how to set up warranties on assets and asset types in Asset Management.</span></span>

## <a name="set-up-a-warranty-on-an-asset-type"></a><span data-ttu-id="1fad6-105">資産タイプに対する保証の設定</span><span class="sxs-lookup"><span data-stu-id="1fad6-105">Set up a warranty on an asset type</span></span>

1. <span data-ttu-id="1fad6-106">**資産管理** \> **設定** \> **資産タイプ** \> **資産タイプ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1fad6-106">Select **Asset management** \> **Setup** \> **Asset types** \> **Asset types**.</span></span>
2. <span data-ttu-id="1fad6-107">左ウィンドウで、仕入先保証契約を関連付ける資産タイプを選択し、**資産タイプの既定値**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1fad6-107">In the left pane, select the asset type to attach a vendor warranty agreement to, and then select **Asset type defaults**.</span></span>
3. <span data-ttu-id="1fad6-108">**一般**クイックタブの、**仕入先保証**フィールドで、契約を選択します。</span><span class="sxs-lookup"><span data-stu-id="1fad6-108">On the **General** FastTab, in the **Vendor warranty** field, select the agreement.</span></span>

## <a name="set-up-a-warranty-on-an-asset"></a><span data-ttu-id="1fad6-109">資産に対する保証の設定</span><span class="sxs-lookup"><span data-stu-id="1fad6-109">Set up a warranty on an asset</span></span>

1. <span data-ttu-id="1fad6-110">**資産管理** \> **共通** \> **資産** \> **全資産**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1fad6-110">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="1fad6-111">資産を選択し、**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1fad6-111">Select the asset, and then select **Edit**.</span></span>
3. <span data-ttu-id="1fad6-112">**仕入先**クイック タブ、**仕入先保証**セクションの**保証**フィールドで、保証契約を選択します。</span><span class="sxs-lookup"><span data-stu-id="1fad6-112">On the **Vendor** FastTab, in the **Vendor warranty** section, in the **Warranty** field, select the warranty agreement.</span></span>
4. <span data-ttu-id="1fad6-113">**保証開始日**と**保証終了日**フィールドで、開始日と終了日を選択します。</span><span class="sxs-lookup"><span data-stu-id="1fad6-113">In the **Warranty start** and **Warranty end** fields, select the start and end dates.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="1fad6-114">ワーク オーダーの**保証開始日**フィールドで日付が選択されている場合、保証はその日付のワーク オーダーに対して有効になります。</span><span class="sxs-lookup"><span data-stu-id="1fad6-114">If a date is selected in the **Warranty start** field on a work order, the warranty becomes valid for the work order on that date.</span></span> <span data-ttu-id="1fad6-115">ワーク オーダーを作成すると、**保証開始日**フィールドは自動的に作成日に設定されます。</span><span class="sxs-lookup"><span data-stu-id="1fad6-115">When you create a work order, the **Warranty start** field is automatically set to the date of creation.</span></span> <span data-ttu-id="1fad6-116">ただし、この日付は、保証契約の開始日などに変更することができます。</span><span class="sxs-lookup"><span data-stu-id="1fad6-116">However, you can change the date so that it corresponds to, for example, the start date of a warranty agreement.</span></span>
    >
    > ![図 1](media/02-warranty.png)

> [!NOTE]
> <span data-ttu-id="1fad6-118">仕入先保証の対象となる資産のワーク オーダーを作成する場合、そのワーク オーダーの期間中に予定された開始日があると、保証契約に関する通知が表示されます。</span><span class="sxs-lookup"><span data-stu-id="1fad6-118">When you create a work order for an asset that is covered by a vendor warranty, if the work order has an expected start date during the warranty period, you receive a notification about the warranty agreement.</span></span> <span data-ttu-id="1fad6-119">その後、必要に応じて、ワーク オーダーをキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="1fad6-119">You can then cancel the work order, as you require.</span></span>
