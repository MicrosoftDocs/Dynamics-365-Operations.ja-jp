--- 
title: "WMS に対応した倉庫の場所のコンフィギュレーション"
description: "このガイドでは、新しい WMS が有効な倉庫 (詳細な倉庫管理プロセスを使用する倉庫) の場所の設定をコンフィギュレーションする方法を示します。"
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1082c86361180db84bb2b5c0b8158816f76a219e
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="configure-locations-in-a-wms-enabled-warehouse"></a><span data-ttu-id="f8808-103">WMS に対応した倉庫の場所のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="f8808-103">Configure locations in a WMS-enabled warehouse</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f8808-104">このガイドでは、新しい WMS が有効な倉庫 (詳細な倉庫管理プロセスを使用する倉庫) の場所の設定をコンフィギュレーションする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="f8808-104">This guide shows you how to configure the location setup for a new WMS-enabled warehouse (a warehouse that uses advanced warehouse management processes).</span></span> <span data-ttu-id="f8808-105">通常、このプロセスを実行するのは倉庫マネージャーです。</span><span class="sxs-lookup"><span data-stu-id="f8808-105">The process is typically done by a warehouse manager.</span></span> <span data-ttu-id="f8808-106">このガイドは、デモ データの会社 USMF で、または独自のデータで実行できます。</span><span class="sxs-lookup"><span data-stu-id="f8808-106">You can run this guide in demo data company USMF or on your own data.</span></span> <span data-ttu-id="f8808-107">少なくとも 1 つのサイトがコンフィギュレーションされていることが前提条件です。</span><span class="sxs-lookup"><span data-stu-id="f8808-107">A precondition is that you have at least one site configured.</span></span>


## <a name="create-a-new-warehouse"></a><span data-ttu-id="f8808-108">新しい倉庫の作成</span><span class="sxs-lookup"><span data-stu-id="f8808-108">Create a new warehouse</span></span>
1. <span data-ttu-id="f8808-109">[倉庫] に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8808-109">Go to Warehouses.</span></span>
2. <span data-ttu-id="f8808-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8808-110">Click New.</span></span>
3. <span data-ttu-id="f8808-111">[倉庫] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-111">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="f8808-112">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="f8808-113">[サイト] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-113">In the Site field, type a value.</span></span>
6. <span data-ttu-id="f8808-114">[倉庫] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="f8808-114">Expand or collapse the Warehouse section.</span></span>
7. <span data-ttu-id="f8808-115">[倉庫管理プロセスの使用] オプションを [はい] に設定します。</span><span class="sxs-lookup"><span data-stu-id="f8808-115">Set the Use warehouse management processes option to Yes.</span></span>
    * <span data-ttu-id="f8808-116">この設定により、倉庫作業やモバイル デバイスを使用して、詳細な倉庫プロセスを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="f8808-116">This setting allows you to  run advanced warehousing processes using warehouse work and mobile devices.</span></span>  
8. <span data-ttu-id="f8808-117">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f8808-117">Close the page.</span></span>

## <a name="define-a-location-format"></a><span data-ttu-id="f8808-118">場所形式の定義</span><span class="sxs-lookup"><span data-stu-id="f8808-118">Define a location format</span></span>
1. <span data-ttu-id="f8808-119">[場所形式] に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8808-119">Go to Location formats.</span></span>
    * <span data-ttu-id="f8808-120">場所形式は、倉庫内で使用されるさまざまな場所の在庫置場の位置に、固有の一貫した名前を作成するために使用するネーミング方式です。</span><span class="sxs-lookup"><span data-stu-id="f8808-120">Location formats are a naming-system used to create unique and consistent names for the different location bin positions used within a warehouse.</span></span> <span data-ttu-id="f8808-121">通路番号などの場所のコンポーネントの識別が容易になるように、場所形式の一部として区切りを使用すると便利です。</span><span class="sxs-lookup"><span data-stu-id="f8808-121">It can be useful to use separators as part of the location format to make it easier to identify components of the location such as the aisle number.</span></span> <span data-ttu-id="f8808-122">この例では、4 つのコンポーネントで名前を作成します。</span><span class="sxs-lookup"><span data-stu-id="f8808-122">In this example, we’ll create a name with four components.</span></span> <span data-ttu-id="f8808-123">たとえば、通路、ラック、棚、および在庫置場にすることができます。</span><span class="sxs-lookup"><span data-stu-id="f8808-123">For example, these could be aisle, rack, shelf, and bin.</span></span>  
2. <span data-ttu-id="f8808-124">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8808-124">Click New.</span></span>
3. <span data-ttu-id="f8808-125">[場所形式] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-125">In the Location format field, type a value.</span></span>
4. <span data-ttu-id="f8808-126">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-126">In the Name field, type a value.</span></span>
5. <span data-ttu-id="f8808-127">[区分の説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-127">In the Segment description field, type a value.</span></span>
    * <span data-ttu-id="f8808-128">場所の名前の最初のコンポーネントが表すものについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f8808-128">This describes what the first component of the location name represents.</span></span> <span data-ttu-id="f8808-129">たとえば、通路にすることができます。</span><span class="sxs-lookup"><span data-stu-id="f8808-129">For example, it could be Aisle.</span></span>  
6. <span data-ttu-id="f8808-130">[長さ] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-130">In the Length field, enter a number.</span></span>
    * <span data-ttu-id="f8808-131">これにより、場所の名前のこの部分の文字数が決まります。</span><span class="sxs-lookup"><span data-stu-id="f8808-131">This determines how many characters this part of the location name must have.</span></span> <span data-ttu-id="f8808-132">名前のすべてのコンポーネントの合計が、区切りを含み、10 文字を超えることができないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f8808-132">Note that the total of all components in the name, including the separators, cannot exceed 10 characters.</span></span>  
7. <span data-ttu-id="f8808-133">[区切り] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-133">In the Separator field, type a value.</span></span>
    * <span data-ttu-id="f8808-134">これにより、名前の 1 番目と 2 番目のコンポーネントの間で使用する文字や記号が決まります。</span><span class="sxs-lookup"><span data-stu-id="f8808-134">This determines which character or symbol is used between the first and second component of the name.</span></span>  
8. <span data-ttu-id="f8808-135">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8808-135">Click New.</span></span>
9. <span data-ttu-id="f8808-136">[区分の説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-136">In the Segment description field, type a value.</span></span>
10. <span data-ttu-id="f8808-137">[長さ] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-137">In the Length field, enter a number.</span></span>
11. <span data-ttu-id="f8808-138">[区切り] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-138">In the Separator field, type a value.</span></span>
12. <span data-ttu-id="f8808-139">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8808-139">Click New.</span></span>
13. <span data-ttu-id="f8808-140">[区分の説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-140">In the Segment description field, type a value.</span></span>
14. <span data-ttu-id="f8808-141">[長さ] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-141">In the Length field, enter a number.</span></span>
15. <span data-ttu-id="f8808-142">[区切り] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-142">In the Separator field, type a value.</span></span>
16. <span data-ttu-id="f8808-143">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8808-143">Click New.</span></span>
17. <span data-ttu-id="f8808-144">[区分の説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-144">In the Segment description field, type a value.</span></span>
18. <span data-ttu-id="f8808-145">[長さ] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-145">In the Length field, enter a number.</span></span>
19. <span data-ttu-id="f8808-146">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8808-146">Click Save.</span></span>
20. <span data-ttu-id="f8808-147">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f8808-147">Close the page.</span></span>

## <a name="define-location-types"></a><span data-ttu-id="f8808-148">場所のタイプの定義</span><span class="sxs-lookup"><span data-stu-id="f8808-148">Define location types</span></span>
1. <span data-ttu-id="f8808-149">[在庫場所タイプ] に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8808-149">Go to Location types.</span></span>
    * <span data-ttu-id="f8808-150">在庫場所タイプは、異なる倉庫管理プロセスを制御するためのフィルター処理オプションとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="f8808-150">Location types can be used as filtering options to control the different warehouse management processes.</span></span> <span data-ttu-id="f8808-151">少なくとも、出荷の倉庫管理プロセスを定義するためにステージングおよび最終配送場所タイプを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8808-151">As a minimum, you need to create staging and final shipping location types in order to define the outbound warehouse management process.</span></span>  
2. <span data-ttu-id="f8808-152">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8808-152">Click New.</span></span>
3. <span data-ttu-id="f8808-153">[場所タイプ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-153">In the Location type field, type a value.</span></span>
4. <span data-ttu-id="f8808-154">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-154">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f8808-155">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f8808-155">Close the page.</span></span>

## <a name="define-location-profile"></a><span data-ttu-id="f8808-156">場所プロファイルの定義</span><span class="sxs-lookup"><span data-stu-id="f8808-156">Define location profile</span></span>
1. <span data-ttu-id="f8808-157">[場所プロファイル] に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8808-157">Go to Location profiles.</span></span>
    * <span data-ttu-id="f8808-158">場所プロファイルの定義は非常に重要です。</span><span class="sxs-lookup"><span data-stu-id="f8808-158">The definition of location profiles is very important.</span></span> <span data-ttu-id="f8808-159">グループ化された場所の能力は、保管される在庫と保管方法に関連するポリシーとともに、ここで制御できます。</span><span class="sxs-lookup"><span data-stu-id="f8808-159">Grouped locations capacity can be controlled here, as well as the policies related to what inventory gets stored, and how it is stored.</span></span> <span data-ttu-id="f8808-160">場所プロファイルは、異なる倉庫管理プロセスを制御するためのフィルター処理オプションとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="f8808-160">Location profiles can be used as filtering options to control the different warehouse management processes.</span></span> <span data-ttu-id="f8808-161">少なくとも、倉庫管理プロセスを有効にするために、ユーザーの場所のプロファイルを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8808-161">As a minimum, you must create a user location profile in order to enable the warehouse management processes.</span></span>  
2. <span data-ttu-id="f8808-162">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8808-162">Click New.</span></span>
3. <span data-ttu-id="f8808-163">[場所プロファイル ID] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-163">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="f8808-164">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-164">In the Name field, type a value.</span></span>
5. <span data-ttu-id="f8808-165">[場所形式] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="f8808-165">In the Location format field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="f8808-166">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="f8808-166">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="f8808-167">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8808-167">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="f8808-168">[場所タイプ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="f8808-168">In the Location type field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="f8808-169">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="f8808-169">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="f8808-170">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8808-170">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="f8808-171">[混合在庫状態を許可] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="f8808-171">Select or clear the Allow mixed  inventory statuses check box.</span></span>
    * <span data-ttu-id="f8808-172">この場所プロファイルによりグループ化する場所で混合在庫状態の値を許可する場合は、このオプションを有効にします。</span><span class="sxs-lookup"><span data-stu-id="f8808-172">Enable this option if you want to allow mixed inventory status values in the locations that are going to be grouped by this location profile.</span></span>  
12. <span data-ttu-id="f8808-173">[バッチ日数ルールの上書き] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="f8808-173">Select or clear the Override rules for batch days check box.</span></span>
    * <span data-ttu-id="f8808-174">このルールに従わない在庫バッチの混合を許可するには、異なる場合の在庫バッチの有効期限日数のルールを上書きするために、このオプションを有効にします。</span><span class="sxs-lookup"><span data-stu-id="f8808-174">Enable this option to override the rule for how many days the inventory batch expiration dates can differ, to allow mixing of inventory batches that don’t obeying this rule.</span></span>  
13. <span data-ttu-id="f8808-175">[循環棚卸を許可] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="f8808-175">Select or clear the Allow cycle counting check box.</span></span>
    * <span data-ttu-id="f8808-176">この場所プロファイルによりグループ化するすべての場所で循環棚卸プロセスを許可するには、このオプションを有効にします。</span><span class="sxs-lookup"><span data-stu-id="f8808-176">Enable this option to allow cycle counting processing in all the locations that are going to be grouped by this location profile.</span></span>  
14. <span data-ttu-id="f8808-177">[分析コード] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="f8808-177">Expand or collapse the Dimensions section.</span></span>
    * <span data-ttu-id="f8808-178">[分析コード] タブでは、各場所内の積載能力の詳細な計算を有効にするために、パラメーターと方法を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="f8808-178">The Dimensions tab allows you to define parameters and methods to enable precise calculations of the load capacity within each of the locations.</span></span>  
15. <span data-ttu-id="f8808-179">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f8808-179">Close the page.</span></span>

## <a name="enable-warehouse-management-parameters"></a><span data-ttu-id="f8808-180">倉庫管理パラメーターの有効化</span><span class="sxs-lookup"><span data-stu-id="f8808-180">Enable warehouse management parameters</span></span>
1. <span data-ttu-id="f8808-181">[倉庫管理パラメーター] に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8808-181">Go to Warehouse management parameters.</span></span>
    * <span data-ttu-id="f8808-182">倉庫の作業を処理するには、ユーザーの場所プロファイルのパラメーターでステージング場所のタイプおよび最終出荷場所タイプを設定する必要があります。定義した最終出荷場所タイプで出荷プロセスが終了するとすぐに、関連する出荷トランザクションが「ピッキング済」に更新されます。</span><span class="sxs-lookup"><span data-stu-id="f8808-182">To be able to process warehouse work, you need to set parameters for the user location profile the staging location type, and the final shipping location type  As soon as the outbound process ends at the final shipping location type that you define, the related outbound transactions will be updated to ‘Picked’.</span></span>  
2. <span data-ttu-id="f8808-183">[場所プロファイル] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="f8808-183">Expand or collapse the Location profiles section.</span></span>
3. <span data-ttu-id="f8808-184">[ユーザーの場所] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="f8808-184">In the User location field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="f8808-185">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8808-185">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="f8808-186">[場所タイプ] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="f8808-186">Expand or collapse the Location types section.</span></span>
6. <span data-ttu-id="f8808-187">[ステージング場所のタイプ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="f8808-187">In the Staging location type field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="f8808-188">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8808-188">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="f8808-189">[最終出荷場所のタイプ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="f8808-189">In the Final shipping location type field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="f8808-190">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8808-190">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="f8808-191">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f8808-191">Close the page.</span></span>

## <a name="define-warehouse-zone-groups"></a><span data-ttu-id="f8808-192">倉庫ゾーン グループの定義</span><span class="sxs-lookup"><span data-stu-id="f8808-192">Define warehouse zone groups</span></span>
1. <span data-ttu-id="f8808-193">[倉庫ゾーン グループ] に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8808-193">Go to Warehouse zone groups.</span></span>
    * <span data-ttu-id="f8808-194">倉庫ゾーンは、異なる倉庫管理プロセスを制御するためのフィルター処理オプションとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="f8808-194">Warehouse zones can be used as filters for options to control the different warehouse management processes.</span></span> <span data-ttu-id="f8808-195">ゾーンを定義する前に、ゾーン グループを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8808-195">You need to create a zone group before you can define a zone.</span></span>  
2. <span data-ttu-id="f8808-196">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8808-196">Click New.</span></span>
3. <span data-ttu-id="f8808-197">[ゾーン グループ ID] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-197">In the Zone group ID field, type a value.</span></span>
4. <span data-ttu-id="f8808-198">[ゾーン グループ名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-198">In the Zone group name field, type a value.</span></span>
5. <span data-ttu-id="f8808-199">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f8808-199">Close the page.</span></span>

## <a name="define-warehouse-zones"></a><span data-ttu-id="f8808-200">倉庫ゾーンの定義</span><span class="sxs-lookup"><span data-stu-id="f8808-200">Define Warehouse zones</span></span>
1. <span data-ttu-id="f8808-201">[ゾーン] に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8808-201">Go to Zones.</span></span>
2. <span data-ttu-id="f8808-202">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8808-202">Click New.</span></span>
3. <span data-ttu-id="f8808-203">[ゾーン ID] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-203">In the Zone ID field, type a value.</span></span>
4. <span data-ttu-id="f8808-204">[ゾーン名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-204">In the Zone name field, type a value.</span></span>
5. <span data-ttu-id="f8808-205">[ゾーン グループ ID] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="f8808-205">In the Zone group ID field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="f8808-206">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="f8808-206">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="f8808-207">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8808-207">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="f8808-208">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f8808-208">Close the page.</span></span>

## <a name="create-locations-using-the-location-setup-wizard"></a><span data-ttu-id="f8808-209">場所設定ウィザードを使用した場所の作成</span><span class="sxs-lookup"><span data-stu-id="f8808-209">Create locations using the Location setup wizard</span></span>
1. <span data-ttu-id="f8808-210">[場所設定ウィザード] に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8808-210">Go to Location setup wizard.</span></span>
2. <span data-ttu-id="f8808-211">[倉庫] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="f8808-211">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="f8808-212">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="f8808-212">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="f8808-213">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8808-213">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="f8808-214">[ゾーン ID] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="f8808-214">In the Zone ID field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="f8808-215">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="f8808-215">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="f8808-216">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8808-216">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="f8808-217">[場所プロファイル ID] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="f8808-217">In the Location profile ID field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="f8808-218">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="f8808-218">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="f8808-219">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8808-219">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="f8808-220">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="f8808-220">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="f8808-221">[開始番号] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-221">In the From number field, enter a number.</span></span>
    * <span data-ttu-id="f8808-222">[開始番号] と [終了番号] フィールドで、作成された場所の数を定義します。</span><span class="sxs-lookup"><span data-stu-id="f8808-222">The From number and To number fields define how many locations will be created.</span></span> <span data-ttu-id="f8808-223">たとえば、場所形式の 4 つの明細行すべてで、[開始番号] に「1」を設定し、[終了番号] に「3」を設定する場合、81 の場所が作成されます (3 x 3 x 3 x 3)。</span><span class="sxs-lookup"><span data-stu-id="f8808-223">For example, if you set From number to 1 and To number to 3 for all four lines in the location format, 81 locations will be created (3x3x3x3).</span></span>  
13. <span data-ttu-id="f8808-224">[終了番号] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-224">In the To number field, enter a number.</span></span>
14. <span data-ttu-id="f8808-225">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="f8808-225">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="f8808-226">[開始番号] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-226">In the From number field, enter a number.</span></span>
16. <span data-ttu-id="f8808-227">[終了番号] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-227">In the To number field, enter a number.</span></span>
17. <span data-ttu-id="f8808-228">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="f8808-228">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="f8808-229">[開始番号] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-229">In the From number field, enter a number.</span></span>
19. <span data-ttu-id="f8808-230">[終了番号] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-230">In the To number field, enter a number.</span></span>
20. <span data-ttu-id="f8808-231">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="f8808-231">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="f8808-232">[開始番号] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-232">In the From number field, enter a number.</span></span>
22. <span data-ttu-id="f8808-233">[終了番号] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-233">In the To number field, enter a number.</span></span>
23. <span data-ttu-id="f8808-234">[作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8808-234">Click Create.</span></span>

## <a name="create-locations-manually"></a><span data-ttu-id="f8808-235">手動での場所の作成</span><span class="sxs-lookup"><span data-stu-id="f8808-235">Create locations manually</span></span>
1. <span data-ttu-id="f8808-236">[場所] に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8808-236">Go to Locations.</span></span>
    * <span data-ttu-id="f8808-237">倉庫内の場所は手動で簡単に作成できます。</span><span class="sxs-lookup"><span data-stu-id="f8808-237">Manually creation of locations within a warehouse can easily be done.</span></span> <span data-ttu-id="f8808-238">場所の名前と場所プロファイル ID は、必須の値です。</span><span class="sxs-lookup"><span data-stu-id="f8808-238">The location name and the Location profile ID are mandatory values.</span></span>  
2. <span data-ttu-id="f8808-239">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8808-239">Click New.</span></span>
3. <span data-ttu-id="f8808-240">[倉庫] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-240">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="f8808-241">[場所] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-241">In the Location field, type a value.</span></span>
    * <span data-ttu-id="f8808-242">ここに新しい場所を作成する場合、既存の名前を選択するのではなく、新しい固有の名前を入力する必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f8808-242">Note that you're creating a new location here, so you need to type a new unique name, rather than selecting an existing one.</span></span>  
5. <span data-ttu-id="f8808-243">[場所プロファイル ID] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-243">In the Location profile ID field, type a value.</span></span>
6. <span data-ttu-id="f8808-244">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f8808-244">Close the page.</span></span>

## <a name="define-pack-size-categories"></a><span data-ttu-id="f8808-245">梱包サイズ カテゴリの定義</span><span class="sxs-lookup"><span data-stu-id="f8808-245">Define Pack size categories</span></span>
1. <span data-ttu-id="f8808-246">[梱包サイズ カテゴリ] に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8808-246">Go to Pack size categories.</span></span>
    * <span data-ttu-id="f8808-247">梱包サイズ カテゴリは、物理的な梱包サイズが類似している品目をグループ化するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="f8808-247">Pack size categories can be used to group items that have similar physical packing sizes.</span></span> <span data-ttu-id="f8808-248">この例では、梱包サイズ カテゴリは、倉庫の特定のゾーン内でのピッキング場所で能力を制御するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f8808-248">In this example the pack size category will be used to control the capacity at the picking locations within a specific zone of the warehouse.</span></span> <span data-ttu-id="f8808-249">梱包サイズ カテゴリ ID は、在庫限度として使用するためにリリース済製品エンティティに割り当てる必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f8808-249">Please note that the pack size category ID must be assigned to the released product entity in order to be used as part of the stocking limits processing.</span></span>  
2. <span data-ttu-id="f8808-250">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8808-250">Click New.</span></span>
3. <span data-ttu-id="f8808-251">[梱包サイズ カテゴリ ID] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-251">In the Pack size category ID field, type a value.</span></span>
4. <span data-ttu-id="f8808-252">[梱包サイズ カテゴリ名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-252">In the Pack size category name field, type a value.</span></span>
5. <span data-ttu-id="f8808-253">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f8808-253">Close the page.</span></span>

## <a name="define-location-stocking-limits"></a><span data-ttu-id="f8808-254">場所別在庫限度の設定</span><span class="sxs-lookup"><span data-stu-id="f8808-254">Define location stocking limits</span></span>
1. <span data-ttu-id="f8808-255">[場所別在庫限度] に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8808-255">Go to Location stocking limits.</span></span>
    * <span data-ttu-id="f8808-256">場所別在庫限度は、在庫を配送する物理的能力がない場所に在庫の配置を要求する作業が作成されないことを確認するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="f8808-256">Location stocking limits help to make sure that work isn't created to request that inventory to be put in a location that doesn't have the physical capacity to carry the inventory.</span></span>  
2. <span data-ttu-id="f8808-257">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8808-257">Click New.</span></span>
3. <span data-ttu-id="f8808-258">[倉庫] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-258">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="f8808-259">[場所プロファイル ID] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-259">In the Location profile ID field, type a value.</span></span>
5. <span data-ttu-id="f8808-260">[梱包サイズ カテゴリ ID] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-260">In the Pack size category ID field, type a value.</span></span>
6. <span data-ttu-id="f8808-261">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-261">In the Quantity field, enter a number.</span></span>
7. <span data-ttu-id="f8808-262">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8808-262">Click Save.</span></span>
8. <span data-ttu-id="f8808-263">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f8808-263">Close the page.</span></span>

## <a name="define-fixed-picking-locations"></a><span data-ttu-id="f8808-264">固定のピッキング場所の定義</span><span class="sxs-lookup"><span data-stu-id="f8808-264">Define fixed picking locations</span></span>
1. <span data-ttu-id="f8808-265">[固定の場所] に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8808-265">Go to Fixed locations.</span></span>
    * <span data-ttu-id="f8808-266">製品または製品バリアントごとに使用される場所を定義できます。</span><span class="sxs-lookup"><span data-stu-id="f8808-266">You can define the locations to be used per product or per product variant.</span></span> <span data-ttu-id="f8808-267">同じ倉庫内の同じ製品に複数の固定の場所を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="f8808-267">It is possible to create multiple fixed locations for the same product within the same warehouse.</span></span>  
2. <span data-ttu-id="f8808-268">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8808-268">Click New.</span></span>
3. <span data-ttu-id="f8808-269">[品目番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-269">In the Item number field, type a value.</span></span>
4. <span data-ttu-id="f8808-270">[倉庫] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8808-270">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="f8808-271">[場所] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="f8808-271">In the Location field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="f8808-272">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8808-272">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="f8808-273">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f8808-273">Close the page.</span></span>


