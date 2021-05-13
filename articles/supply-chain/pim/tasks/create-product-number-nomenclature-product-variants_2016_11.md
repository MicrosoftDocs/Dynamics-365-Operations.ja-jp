---
title: コンフィギュレーション済みの製品バリアントの製品番号の分類の作成
description: この手順では、コンフィギュレーション済製品バリアントにおける製品番号の分類を設定する方法、およびそれをコンフィギュレーション可能な製品マスターに関連付ける方法を示します。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ea30dc107213b1a2c6b2a109188066a6ea82159
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921014"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="86c90-103">コンフィギュレーション済みの製品バリアントの製品番号の分類の作成</span><span class="sxs-lookup"><span data-stu-id="86c90-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="86c90-104">この手順では、コンフィギュレーション済製品バリアントにおける製品番号の分類を設定する方法、およびそれをコンフィギュレーション可能な製品マスターに関連付ける方法を示します。</span><span class="sxs-lookup"><span data-stu-id="86c90-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="86c90-105">この手順では、製品コンフィギュレーション モデル コンポーネントのコンフィギュレーションに関する用語をどのように作成するかを示します。</span><span class="sxs-lookup"><span data-stu-id="86c90-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="86c90-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="86c90-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="86c90-107">新しい製品番号の分類は、「D0004」製品マスターに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="86c90-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="86c90-108">このタスクは、通常、製品デザイナーが行います。</span><span class="sxs-lookup"><span data-stu-id="86c90-108">This task would typically be done by a product designer.</span></span>

## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="86c90-109">[製品番号の分類] を作成します。</span><span class="sxs-lookup"><span data-stu-id="86c90-109">Create a product number nomenclature</span></span>

1. <span data-ttu-id="86c90-110">**製品情報管理\>設定\>製品の分類** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="86c90-110">Go to **Product information management \> Setup \> Product nomenclature**.</span></span>
1. <span data-ttu-id="86c90-111">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-111">Select **New**.</span></span>
1. <span data-ttu-id="86c90-112">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="86c90-112">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="86c90-113">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="86c90-113">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="86c90-114">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-114">Select **Add**.</span></span>
1. <span data-ttu-id="86c90-115">**製品マスター番号** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-115">Select **Product master number**.</span></span>
1. <span data-ttu-id="86c90-116">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-116">Select **Add**.</span></span>
1. <span data-ttu-id="86c90-117">**テキスト定数** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-117">Select **Text constant**.</span></span>
1. <span data-ttu-id="86c90-118">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="86c90-118">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="86c90-119">**テキスト** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="86c90-119">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="86c90-120">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-120">Select **Add**.</span></span>
1. <span data-ttu-id="86c90-121">**コンフィギュレーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-121">Select **Configuration**.</span></span>
1. <span data-ttu-id="86c90-122">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="86c90-122">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="86c90-123">製品番号の分類を製品マスターに割り当てる</span><span class="sxs-lookup"><span data-stu-id="86c90-123">Assign the product number nomenclature to a product master</span></span>

1. <span data-ttu-id="86c90-124">**製品情報管理 \> 製品 \> 製品マスター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="86c90-124">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="86c90-125">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="86c90-125">Use the Quick Filter to find records.</span></span> <span data-ttu-id="86c90-126">たとえば、「D」 という値を含む **製品番号** フィールドをフィルターします。</span><span class="sxs-lookup"><span data-stu-id="86c90-126">For example, filter on the **Product number** field with a value of 'D'.</span></span>
1. <span data-ttu-id="86c90-127">一覧で、選択した行のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-127">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="86c90-128">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-128">Select **Edit**.</span></span>
1. <span data-ttu-id="86c90-129">**分類の使用** フィールドで、*はい* を選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-129">Select *Yes* in the **Use nomenclature** field.</span></span>
1. <span data-ttu-id="86c90-130">**製品バリアント番号の分類** フィールドに、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-130">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
1. <span data-ttu-id="86c90-131">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="86c90-131">Close the page.</span></span>
1. <span data-ttu-id="86c90-132">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="86c90-132">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="86c90-133">製品コンフィギュレーション モデル コンポーネントの分類の作成</span><span class="sxs-lookup"><span data-stu-id="86c90-133">Create nomenclature for a product configuration model component</span></span>

1. <span data-ttu-id="86c90-134">**製品情報管理\>製品\>製品コンフィギュレーション モデル** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="86c90-134">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="86c90-135">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-135">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="86c90-136">一覧で、選択した行のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-136">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="86c90-137">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-137">Select **Edit**.</span></span>
1. <span data-ttu-id="86c90-138">**コンフィギュレーションの分類の使用** フィールドで、*はい* を選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-138">Select *Yes* in the **Use configuration nomenclature** field.</span></span>
1. <span data-ttu-id="86c90-139">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-139">Select **Add**.</span></span>
1. <span data-ttu-id="86c90-140">**属性値** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-140">Select **Attribute value**.</span></span>
1. <span data-ttu-id="86c90-141">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="86c90-141">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="86c90-142">**属性** フィールドに、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-142">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="86c90-143">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-143">Select **Add**.</span></span>
1. <span data-ttu-id="86c90-144">**テキスト定数** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-144">Select **Text constant**.</span></span>
1. <span data-ttu-id="86c90-145">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="86c90-145">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="86c90-146">**テキスト** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="86c90-146">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="86c90-147">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-147">Select **Add**.</span></span>
1. <span data-ttu-id="86c90-148">**属性値** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-148">Select **Attribute value**.</span></span>
1. <span data-ttu-id="86c90-149">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="86c90-149">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="86c90-150">**属性** フィールドに、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-150">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="86c90-151">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-151">Select **Add**.</span></span>
1. <span data-ttu-id="86c90-152">**テキスト定数** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-152">Select **Text constant**.</span></span>
1. <span data-ttu-id="86c90-153">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="86c90-153">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="86c90-154">**テキスト** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="86c90-154">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="86c90-155">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-155">Select **Add**.</span></span>
1. <span data-ttu-id="86c90-156">**属性値** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-156">Select **Attribute value**.</span></span>
1. <span data-ttu-id="86c90-157">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="86c90-157">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="86c90-158">**属性** フィールドに、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-158">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="86c90-159">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-159">Select **Add**.</span></span>
1. <span data-ttu-id="86c90-160">**テキスト定数** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-160">Select **Text constant**.</span></span>
1. <span data-ttu-id="86c90-161">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="86c90-161">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="86c90-162">**テキスト** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="86c90-162">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="86c90-163">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-163">Select **Add**.</span></span>
1. <span data-ttu-id="86c90-164">**属性値** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-164">Select **Attribute value**.</span></span>
1. <span data-ttu-id="86c90-165">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="86c90-165">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="86c90-166">**属性** フィールドに、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-166">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="86c90-167">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-167">Select **Add**.</span></span>
1. <span data-ttu-id="86c90-168">**テキスト定数** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-168">Select **Text constant**.</span></span>
1. <span data-ttu-id="86c90-169">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="86c90-169">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="86c90-170">**テキスト** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="86c90-170">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="86c90-171">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-171">Select **Add**.</span></span>
1. <span data-ttu-id="86c90-172">**番号順序値** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-172">Select **Number sequence value**.</span></span>
1. <span data-ttu-id="86c90-173">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="86c90-173">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="86c90-174">**番号順序** フィールドに、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="86c90-174">In the **Number sequence** field, enter or select a value.</span></span>
1. <span data-ttu-id="86c90-175">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="86c90-175">Close the page.</span></span>
1. <span data-ttu-id="86c90-176">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="86c90-176">Close the page.</span></span>
1. <span data-ttu-id="86c90-177">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="86c90-177">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]