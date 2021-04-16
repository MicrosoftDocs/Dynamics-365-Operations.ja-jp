---
title: 場所別在庫限度
description: このトピックでは、場所別在庫限度機能について説明します。
author: perlynne
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-11-11
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: b9fb3c35f2f2e0fd7c0e3afe132efb4c51f163a9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831269"
---
# <a name="location-stocking-limits"></a><span data-ttu-id="95e7e-103">場所別在庫限度</span><span class="sxs-lookup"><span data-stu-id="95e7e-103">Location stocking limits</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="95e7e-104">**場所別在庫限度** ページ (**倉庫管理 \> 設定 \> 倉庫 \> 場所別在庫限度) を使用して、** 容積計算のための高度なプロセスを使用することなく、倉庫保管場所の積載能力を制御することができます。</span><span class="sxs-lookup"><span data-stu-id="95e7e-104">You can use the **Location stocking limits** page (**Warehouse management \> Setup \> Warehouse \> Location stocking limits**) to control the load capacity at warehouse locations without having to use the more advanced processes for volumetric calculations of physical products.</span></span>

<span data-ttu-id="95e7e-105">場所別在庫限度の目的は、場所に含めることができる最大数量を評価することです。</span><span class="sxs-lookup"><span data-stu-id="95e7e-105">The purpose of location stocking limits is to evaluate the maximum quantity that a location can contain.</span></span> <span data-ttu-id="95e7e-106">この機能は、次の 3 つのレベルのいずれかに設定できます。各レベルには、**場所別在庫限度** ページに独自のタブがあります:</span><span class="sxs-lookup"><span data-stu-id="95e7e-106">You can set up the feature on any of three levels, each of which has its own tab on the **Location stocking limits** page:</span></span>

- <span data-ttu-id="95e7e-107">製品</span><span class="sxs-lookup"><span data-stu-id="95e7e-107">Products</span></span>
- <span data-ttu-id="95e7e-108">製品バリアント</span><span class="sxs-lookup"><span data-stu-id="95e7e-108">Product variants</span></span>
- <span data-ttu-id="95e7e-109">コンテナー タイプ</span><span class="sxs-lookup"><span data-stu-id="95e7e-109">Container types</span></span>

<span data-ttu-id="95e7e-110">各レベルに対して、異なるフィールド値を定義できます。</span><span class="sxs-lookup"><span data-stu-id="95e7e-110">For each level, you can define different field values.</span></span> <span data-ttu-id="95e7e-111">システムは、各行の数量と **単位** の値に基づいて、特定の場所の **容量** を評価します。</span><span class="sxs-lookup"><span data-stu-id="95e7e-111">The system will then evaluate the capacity of a specific location, based on the **Quantity** and **Unit** values for each row.</span></span> <span data-ttu-id="95e7e-112">最も詳細に一致するレコードが最初に選択されます。</span><span class="sxs-lookup"><span data-stu-id="95e7e-112">It will select the most detailed matching record first.</span></span> <span data-ttu-id="95e7e-113">たとえば、**場所のプロファイル ID** フィールドに値が設定された行は、**倉庫** フィールドにのみ値がある行の前に評価されます。</span><span class="sxs-lookup"><span data-stu-id="95e7e-113">For example, a row that has a value in the **Location profile ID** field will be evaluated before a row that has a value only in the **Warehouse** field.</span></span> <span data-ttu-id="95e7e-114">残りの容量は、使用される場所の **場所別在庫限度** レコードの数量の値に基づいて評価されます。</span><span class="sxs-lookup"><span data-stu-id="95e7e-114">The remaining capacity will also be evaluated, based on the **Quantity** value for the location stocking limit record that is used.</span></span>

<span data-ttu-id="95e7e-115">ページの **製品** セクションで、場所別在庫限度の検索に対して次のフィールド値を定義できます。</span><span class="sxs-lookup"><span data-stu-id="95e7e-115">In the **Products** section of the page, you can define the following field values for the search for location stocking limits:</span></span>

- <span data-ttu-id="95e7e-116">倉庫</span><span class="sxs-lookup"><span data-stu-id="95e7e-116">Warehouse</span></span>
- <span data-ttu-id="95e7e-117">場所プロファイル ID</span><span class="sxs-lookup"><span data-stu-id="95e7e-117">Location profile ID</span></span>
- <span data-ttu-id="95e7e-118">保管場所</span><span class="sxs-lookup"><span data-stu-id="95e7e-118">Location</span></span>
- <span data-ttu-id="95e7e-119">梱包サイズ カテゴリ ID</span><span class="sxs-lookup"><span data-stu-id="95e7e-119">Pack size category ID</span></span>
- <span data-ttu-id="95e7e-120">品目番号</span><span class="sxs-lookup"><span data-stu-id="95e7e-120">Item number</span></span>
- <span data-ttu-id="95e7e-121">単位</span><span class="sxs-lookup"><span data-stu-id="95e7e-121">Unit</span></span>

> [!NOTE]
> <span data-ttu-id="95e7e-122">各場所別在庫限度レコードに対して **単位** の値を定義する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="95e7e-122">You don't have to define a **Unit** value for each location stocking limit record.</span></span> <span data-ttu-id="95e7e-123">場所の容量計算は、在庫単位の数量に基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="95e7e-123">The location capacity calculations will be based on the inventory unit quantities.</span></span> <span data-ttu-id="95e7e-124">使用される値に対して単位換算が定義されていない場合は、場所別在庫限度レコードに対して別の **品目番号** 値が定義されている場合と同様に、そのレコードはスキップされます。</span><span class="sxs-lookup"><span data-stu-id="95e7e-124">If no unit conversion is defined for a value that is used, the location stocking limit record will be skipped, as if another **Item number** value is defined for it.</span></span>

## <a name="example--purchase-order-receiving"></a><span data-ttu-id="95e7e-125">例 – 発注書の受取</span><span class="sxs-lookup"><span data-stu-id="95e7e-125">Example – Purchase order receiving</span></span>

<span data-ttu-id="95e7e-126">この例は、**場所別在庫限度** ページの **製品バリアント** タブで、次の値が設定されているクリーンな *USMF* のデモ データに基づいています。</span><span class="sxs-lookup"><span data-stu-id="95e7e-126">This example is based on a clean *USMF* demo data set, where the following values are set on the **Product variants** tab of the **Location stocking limits** page.</span></span>

| <span data-ttu-id="95e7e-127">倉庫</span><span class="sxs-lookup"><span data-stu-id="95e7e-127">Warehouse</span></span> | <span data-ttu-id="95e7e-128">場所プロファイル ID</span><span class="sxs-lookup"><span data-stu-id="95e7e-128">Location profile ID</span></span> | <span data-ttu-id="95e7e-129">品目番号</span><span class="sxs-lookup"><span data-stu-id="95e7e-129">Item number</span></span> | <span data-ttu-id="95e7e-130">サイズ</span><span class="sxs-lookup"><span data-stu-id="95e7e-130">Size</span></span> | <span data-ttu-id="95e7e-131">件数</span><span class="sxs-lookup"><span data-stu-id="95e7e-131">Quantity</span></span> | <span data-ttu-id="95e7e-132">単位</span><span class="sxs-lookup"><span data-stu-id="95e7e-132">Unit</span></span> |
|-----------|---------------------|-------------|------|----------|------|
| <span data-ttu-id="95e7e-133">24</span><span class="sxs-lookup"><span data-stu-id="95e7e-133">24</span></span>        | <span data-ttu-id="95e7e-134">フロア</span><span class="sxs-lookup"><span data-stu-id="95e7e-134">FLOOR</span></span>               | <span data-ttu-id="95e7e-135">D0013</span><span class="sxs-lookup"><span data-stu-id="95e7e-135">D0013</span></span>       | <span data-ttu-id="95e7e-136">M</span><span class="sxs-lookup"><span data-stu-id="95e7e-136">M</span></span>    | <span data-ttu-id="95e7e-137">300</span><span class="sxs-lookup"><span data-stu-id="95e7e-137">300</span></span>      | <span data-ttu-id="95e7e-138">Ea</span><span class="sxs-lookup"><span data-stu-id="95e7e-138">Ea</span></span>   |
| <span data-ttu-id="95e7e-139">24</span><span class="sxs-lookup"><span data-stu-id="95e7e-139">24</span></span>        | <span data-ttu-id="95e7e-140">フロア</span><span class="sxs-lookup"><span data-stu-id="95e7e-140">FLOOR</span></span>               | <span data-ttu-id="95e7e-141">D0013</span><span class="sxs-lookup"><span data-stu-id="95e7e-141">D0013</span></span>       | <span data-ttu-id="95e7e-142">L</span><span class="sxs-lookup"><span data-stu-id="95e7e-142">L</span></span>    | <span data-ttu-id="95e7e-143">240</span><span class="sxs-lookup"><span data-stu-id="95e7e-143">240</span></span>      | <span data-ttu-id="95e7e-144">Ea</span><span class="sxs-lookup"><span data-stu-id="95e7e-144">Ea</span></span>   |
| <span data-ttu-id="95e7e-145">24</span><span class="sxs-lookup"><span data-stu-id="95e7e-145">24</span></span>        | <span data-ttu-id="95e7e-146">フロア</span><span class="sxs-lookup"><span data-stu-id="95e7e-146">FLOOR</span></span>               | <span data-ttu-id="95e7e-147">D0013</span><span class="sxs-lookup"><span data-stu-id="95e7e-147">D0013</span></span>       | <span data-ttu-id="95e7e-148">S</span><span class="sxs-lookup"><span data-stu-id="95e7e-148">S</span></span>    | <span data-ttu-id="95e7e-149">360</span><span class="sxs-lookup"><span data-stu-id="95e7e-149">360</span></span>      | <span data-ttu-id="95e7e-150">Ea</span><span class="sxs-lookup"><span data-stu-id="95e7e-150">Ea</span></span>   |

<span data-ttu-id="95e7e-151">製品に対して、さまざまな測定単位製品バリアントが設定されています。</span><span class="sxs-lookup"><span data-stu-id="95e7e-151">Different unit of measure product variants are set up for the products.</span></span> <span data-ttu-id="95e7e-152">これらのバリアントは、3 つのパレット (PL) の場所別在庫限度に揃えられます。</span><span class="sxs-lookup"><span data-stu-id="95e7e-152">These variants are aligned with the location stocking limits for three pallets (PL):</span></span>

- <span data-ttu-id="95e7e-153">**サイズ M:** 1 PL = 100 それぞれ (Ea)</span><span class="sxs-lookup"><span data-stu-id="95e7e-153">**Size M:** 1 PL = 100 each (Ea)</span></span>
- <span data-ttu-id="95e7e-154">**サイズ L:** 1 PL = 80 Ea</span><span class="sxs-lookup"><span data-stu-id="95e7e-154">**Size L:** 1 PL = 80 Ea</span></span>
- <span data-ttu-id="95e7e-155">**サイズ S:** 1 PL = 120 Ea</span><span class="sxs-lookup"><span data-stu-id="95e7e-155">**Size S:** 1 PL = 120 Ea</span></span>

<span data-ttu-id="95e7e-156">したがって、**場所プロファイル ID** 値が *FLOOR* に設定されている各場所は、品目番号 *D0013* の *3* つの *PL* を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="95e7e-156">Therefore, each location where the **Location profile ID** value is set to *FLOOR* can carry *3* *PL* of item number *D0013*.</span></span>

### <a name="prepare-for-the-example"></a><span data-ttu-id="95e7e-157">例の準備</span><span class="sxs-lookup"><span data-stu-id="95e7e-157">Prepare for the example</span></span>

<span data-ttu-id="95e7e-158">この例では、2 つの明細行の発注書入荷フローを実行します。</span><span class="sxs-lookup"><span data-stu-id="95e7e-158">In this example, you will run a purchase order receiving flow for two lines.</span></span> <span data-ttu-id="95e7e-159">ただし、最初に次の方法でデモ データを更新して、その場所で混在した品目を転送できるようにする必要があります。この場合、空の場所は *FL-002* ～ *FL-004* が使用され、未処理の入庫作業はありません。</span><span class="sxs-lookup"><span data-stu-id="95e7e-159">However, you must first update the demo data in the following way to ensure that the locations allow mixed items to be carried, only the empty locations *FL-002* through *FL-004* are used, and there is no open inbound work.</span></span>

1. <span data-ttu-id="95e7e-160">場所 *FL-001* については、**場所プロファイル** フィールドの値を *FLOOR* から *FLOOR-05* に変更します。</span><span class="sxs-lookup"><span data-stu-id="95e7e-160">For location *FL-001*, change the value of the **Location profile** field from *FLOOR* to *FLOOR-05*.</span></span>
1. <span data-ttu-id="95e7e-161">*FLOOR* の場所プロファイルで、**混合品目を許可** を *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="95e7e-161">For the *FLOOR* location profile, set the **Allow mixed items** option to *Yes*.</span></span>
1. <span data-ttu-id="95e7e-162">次の 2 行の発注書を作成します。</span><span class="sxs-lookup"><span data-stu-id="95e7e-162">Create a purchase order that has the following two lines.</span></span>

    | <span data-ttu-id="95e7e-163">倉庫</span><span class="sxs-lookup"><span data-stu-id="95e7e-163">Warehouse</span></span> | <span data-ttu-id="95e7e-164">品目番号</span><span class="sxs-lookup"><span data-stu-id="95e7e-164">Item number</span></span> | <span data-ttu-id="95e7e-165">サイズ</span><span class="sxs-lookup"><span data-stu-id="95e7e-165">Size</span></span> | <span data-ttu-id="95e7e-166">件数</span><span class="sxs-lookup"><span data-stu-id="95e7e-166">Quantity</span></span> | <span data-ttu-id="95e7e-167">単位</span><span class="sxs-lookup"><span data-stu-id="95e7e-167">Unit</span></span> |
    |-----------|-------------|------|----------|------|
    | <span data-ttu-id="95e7e-168">24</span><span class="sxs-lookup"><span data-stu-id="95e7e-168">24</span></span>        | <span data-ttu-id="95e7e-169">D0013</span><span class="sxs-lookup"><span data-stu-id="95e7e-169">D0013</span></span>       | <span data-ttu-id="95e7e-170">S</span><span class="sxs-lookup"><span data-stu-id="95e7e-170">S</span></span>    | <span data-ttu-id="95e7e-171">4</span><span class="sxs-lookup"><span data-stu-id="95e7e-171">4</span></span>        | <span data-ttu-id="95e7e-172">PL</span><span class="sxs-lookup"><span data-stu-id="95e7e-172">PL</span></span>   |
    | <span data-ttu-id="95e7e-173">24</span><span class="sxs-lookup"><span data-stu-id="95e7e-173">24</span></span>        | <span data-ttu-id="95e7e-174">D0013</span><span class="sxs-lookup"><span data-stu-id="95e7e-174">D0013</span></span>       | <span data-ttu-id="95e7e-175">L</span><span class="sxs-lookup"><span data-stu-id="95e7e-175">L</span></span>    | <span data-ttu-id="95e7e-176">4</span><span class="sxs-lookup"><span data-stu-id="95e7e-176">4</span></span>        | <span data-ttu-id="95e7e-177">PL</span><span class="sxs-lookup"><span data-stu-id="95e7e-177">PL</span></span>   |

### <a name="process-the-example"></a><span data-ttu-id="95e7e-178">例を実行する</span><span class="sxs-lookup"><span data-stu-id="95e7e-178">Process the example</span></span>

<span data-ttu-id="95e7e-179">最初に、サイズ *S* のユニット *PL* の数量 *4* を受け取り、作成された作業のプット明細行の場所を確認します。</span><span class="sxs-lookup"><span data-stu-id="95e7e-179">You will first receive a quantity of *4* of unit *PL* in size *S*, and review the put line locations for the work that is created.</span></span> <span data-ttu-id="95e7e-180">次にに、サイズ *L* のユニット *PL* の数量 *4* を受け取り、作成された作業のプット明細行の場所を確認します。</span><span class="sxs-lookup"><span data-stu-id="95e7e-180">You will then receive a quantity of *4* of unit *PL* in size *L*, and review the put line locations for the work that is created.</span></span>

1. <span data-ttu-id="95e7e-181">倉庫管理モバイル アプリでは、ユーザー IDとして *24*、パスワードとして *1* を使用してサインインします。</span><span class="sxs-lookup"><span data-stu-id="95e7e-181">In the Warehouse Management mobile app, sign in by using *24* as the user ID and *1* as the password.</span></span>
1. <span data-ttu-id="95e7e-182">**入庫** \> **購買の入庫** に移動します。</span><span class="sxs-lookup"><span data-stu-id="95e7e-182">Select **Inbound** \> **Purchase Receive**.</span></span>
1. <span data-ttu-id="95e7e-183">サイズ *S* の品目番号 *D0013* の *4* *PL* を入庫します。</span><span class="sxs-lookup"><span data-stu-id="95e7e-183">Receive *4* *PL* of item number *D0013* in size *S*.</span></span>
1. <span data-ttu-id="95e7e-184">プットアウェイ作業が作成された日付を確認します。</span><span class="sxs-lookup"><span data-stu-id="95e7e-184">Review the putaway work that was created.</span></span> <span data-ttu-id="95e7e-185">次の結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="95e7e-185">You should see the following result:</span></span>

    - <span data-ttu-id="95e7e-186">3 PL -\> FL-002</span><span class="sxs-lookup"><span data-stu-id="95e7e-186">3 PL -\> FL-002</span></span>
    - <span data-ttu-id="95e7e-187">1 PL -\> FL-003</span><span class="sxs-lookup"><span data-stu-id="95e7e-187">1 PL -\> FL-003</span></span>

1. <span data-ttu-id="95e7e-188">サイズ *L* の品目番号 *D0013* の *4* *PL* を入庫します。</span><span class="sxs-lookup"><span data-stu-id="95e7e-188">Receive *4* *PL* of item number *D0013* in size *L*.</span></span>
1. <span data-ttu-id="95e7e-189">プットアウェイ作業が作成された日付を確認します。</span><span class="sxs-lookup"><span data-stu-id="95e7e-189">Review the putaway work that was created.</span></span> <span data-ttu-id="95e7e-190">次の結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="95e7e-190">You should see the following result:</span></span>

    - <span data-ttu-id="95e7e-191">1 PL -\> FL-003</span><span class="sxs-lookup"><span data-stu-id="95e7e-191">1 PL -\> FL-003</span></span>
    - <span data-ttu-id="95e7e-192">3 PL -\> FL-004</span><span class="sxs-lookup"><span data-stu-id="95e7e-192">3 PL -\> FL-004</span></span>

<span data-ttu-id="95e7e-193">結果に基づいて、システムが正しいプットアウェイの場所を割り当てることができなかったと結論付けることができます。</span><span class="sxs-lookup"><span data-stu-id="95e7e-193">Based on the results, you might conclude that the system failed to allocate the correct putaway locations.</span></span> <span data-ttu-id="95e7e-194">それ以外の場合、最後のステップで、システムがサイズ *L* の *1* *PL* のみを場所 *FL-003* に追加し、*2* *PL* を追加しなかったのはなぜですか?</span><span class="sxs-lookup"><span data-stu-id="95e7e-194">Otherwise, why did the system add only *1* *PL* of size *L* to location *FL-003* in the last step, not *2* *PL*?</span></span> <span data-ttu-id="95e7e-195">つまり、なぜその場所へのプットアウェイ用に合計 *3* *PL* がないのはなぜでしょうか?</span><span class="sxs-lookup"><span data-stu-id="95e7e-195">That is, why isn't there is a total of *3* *PL* for putaway to that location?</span></span>

<span data-ttu-id="95e7e-196">この明らかな失敗を説明するには、場所別在庫限度の選択基準を理解する必要があります。</span><span class="sxs-lookup"><span data-stu-id="95e7e-196">To explain this apparent failure, you must understand the selection criteria for the location stocking limits.</span></span> <span data-ttu-id="95e7e-197">システムは、最も詳細に一致するレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="95e7e-197">The system selects the most detailed matching record.</span></span> <span data-ttu-id="95e7e-198">この例では、**サイズ** の値が *L*、**数量** の 値が *240*、**単位** の値が *Ea* の行が、最も詳細に一致するレコードです。</span><span class="sxs-lookup"><span data-stu-id="95e7e-198">In this example, the most detailed matching record is the line where the **Size** value is *L*, the **Quantity** value is *240*, and the **Unit** value is *Ea*.</span></span> <span data-ttu-id="95e7e-199">以前に受領したサイズ *S* の *120* *Ea* の数量からの未処理の作業が既に存在しているため、残りの容量は  *240* – *120* = *120* *Ea* として計算されます。</span><span class="sxs-lookup"><span data-stu-id="95e7e-199">Because you already have open work from the previous receipt of a quantity of *120* *Ea* of size *S*, the remaining capacity is calculated as *240* – *120* = *120* *Ea*.</span></span> <span data-ttu-id="95e7e-200">したがって、残りの容量は *80* *Ea* の *1* *PL* しかありません。</span><span class="sxs-lookup"><span data-stu-id="95e7e-200">Therefore, the remaining capacity can carry only *1* *PL* of *80* *Ea*.</span></span>

> [!NOTE]
> <span data-ttu-id="95e7e-201">たとえば、同じ場所に異なる数量を持つ品目の補充などを制御するために、場所別在庫限度を使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="95e7e-201">You can't use location stocking limits to control, for example, the replenishment of items that have different quantities in the same location.</span></span> <span data-ttu-id="95e7e-202">この場合は、*補充テンプレート* を使用します。</span><span class="sxs-lookup"><span data-stu-id="95e7e-202">In this case, use a *replenishment template*.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]