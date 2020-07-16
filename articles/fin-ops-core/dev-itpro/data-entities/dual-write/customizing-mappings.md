---
title: エンティティとフィールドのマッピングのカスタマイズ
description: このトピックでは、エンティティとフィールド マッピングをカスタマイズする方法について説明します。
author: sabinn-msft
manager: AnnBe
ms.date: 03/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Developer
ms.reviewer: v-douklo
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sabinn
ms.search.validFrom: 2020-03-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5df54a2c40646c32b0261328fd83145bac8d731e
ms.sourcegitcommit: eda612d7dc6fc5be2d5d2f27a7472c8d59e42d76
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/23/2020
ms.locfileid: "3500003"
---
# <a name="customize-entity-and-field-mappings"></a><span data-ttu-id="25ca7-103">エンティティとフィールドのマッピングのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="25ca7-103">Customize entity and field mappings</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="25ca7-104">すぐに使えるエンティティ マップには、2 つのアプリ間のデータ フローを可能にする事前定義されたエンティティおよびフィールド マッピングがあります。</span><span class="sxs-lookup"><span data-stu-id="25ca7-104">The out-of-box entity maps have predefined entity and field mappings that enable the flow of data between two apps.</span></span> <span data-ttu-id="25ca7-105">このように、それらは "青写真" として機能します。</span><span class="sxs-lookup"><span data-stu-id="25ca7-105">In this way, they serve as "blueprints."</span></span> <span data-ttu-id="25ca7-106">ただし、ビジネスごとに異なるため、既定のエンティティ マップでは不十分な場合があります。</span><span class="sxs-lookup"><span data-stu-id="25ca7-106">However, because every business is different, the default entity maps might sometimes not be enough.</span></span> <span data-ttu-id="25ca7-107">したがって、二重書き込みは、エンティティ マップおよびフィールド マッピングを変更する方法を提供することにより、カスタマイズを完全にサポートします。</span><span class="sxs-lookup"><span data-stu-id="25ca7-107">Therefore, dual-write fully supports customization by providing ways to change entity maps and field mappings.</span></span>

## <a name="customize-field-mappings-add-transforms-and-enable-filtering"></a><span data-ttu-id="25ca7-108">フィールド マッピングのカスタマイズ、変換の追加、およびフィルタ処理の有効化</span><span class="sxs-lookup"><span data-stu-id="25ca7-108">Customize field mappings, add transforms, and enable filtering</span></span>

1. <span data-ttu-id="25ca7-109">Finance and Operations アプリの **二重書き込み** ページの **エンティティ マッピング** タブで、カスタマイズするエンティティ マップを選択します。</span><span class="sxs-lookup"><span data-stu-id="25ca7-109">In your Finance and Operations app, on the **Dual-write** page, on the **Entity mappings** tab, select the entity map to customize.</span></span>

    > [!NOTE]
    > <span data-ttu-id="25ca7-110">エンティティ マッピングを変更する前に、停止する (実行しない) 必要があります。</span><span class="sxs-lookup"><span data-stu-id="25ca7-110">Before you change entity mappings, they must be stopped (not running).</span></span> <span data-ttu-id="25ca7-111">そうしないと、変更は保存されません。</span><span class="sxs-lookup"><span data-stu-id="25ca7-111">Otherwise, your changes won't be saved.</span></span>

2. <span data-ttu-id="25ca7-112">**エンティティ マッピング** タブで、Finance and Operations アプリまたは Common Data Service から新しいフィールドまたはカスタム フィールドを選択して、フィールドをカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="25ca7-112">On the **Entity mappings** tab, you can customize a field by selecting a new or custom field from either the Finance and Operations app or Common Data Service.</span></span>

    ![フィールドのカスタマイズ](media/customize-a-field.png)

3. <span data-ttu-id="25ca7-114">同期の方向 (単一方向または双方向) をカスタマイズし、マップの種類を選択して変換を追加できます。</span><span class="sxs-lookup"><span data-stu-id="25ca7-114">You can customize the synchronization direction (unidirectional or bidirectional) and add transforms by selecting the map type.</span></span>

    ![同期の方向のカスタマイズと変換の追加](media/customize-sync-direction.png)

    <span data-ttu-id="25ca7-116">次の表で、使用可能な同期の方向について説明します。</span><span class="sxs-lookup"><span data-stu-id="25ca7-116">The following table describes the available synchronization directions.</span></span>

    | <span data-ttu-id="25ca7-117">記号</span><span class="sxs-lookup"><span data-stu-id="25ca7-117">Symbol</span></span> | <span data-ttu-id="25ca7-118">説明</span><span class="sxs-lookup"><span data-stu-id="25ca7-118">Description</span></span> |
    |---|---|
    | ![等号](media/equal-symbol.png) | <span data-ttu-id="25ca7-120">双方向のフィールド割り当て</span><span class="sxs-lookup"><span data-stu-id="25ca7-120">Bidirectional field assignment</span></span> |
    | ![大なり/小なり記号](media/greater-less-symbol.png) | <span data-ttu-id="25ca7-122">変換を使用する双方向フィールド割り当て</span><span class="sxs-lookup"><span data-stu-id="25ca7-122">Bidirectional field assignment that uses transforms</span></span> |
    | ![大なり記号](media/greater-than-symbol.png) | <span data-ttu-id="25ca7-124">単一方向フィールド割り当て (左から右)</span><span class="sxs-lookup"><span data-stu-id="25ca7-124">Unidirectional field assignment (left to right)</span></span> |
    | ![小なり記号](media/less-than-symbol.png) | <span data-ttu-id="25ca7-126">単一方向フィールド割り当て (右から左)</span><span class="sxs-lookup"><span data-stu-id="25ca7-126">Unidirectional field assignment (right to left)</span></span> |
    | ![右矢印キー](media/right-arrow-symbol.png) | <span data-ttu-id="25ca7-128">変換を使用する単一方向フィールド割り当て (左から右)</span><span class="sxs-lookup"><span data-stu-id="25ca7-128">Unidirectional field assignment that uses transforms (left to right)</span></span> |
    | ![左矢印キー](media/left-arrow-symbol.png) | <span data-ttu-id="25ca7-130">変換を使用する単一方向フィールド割り当て (右から左)</span><span class="sxs-lookup"><span data-stu-id="25ca7-130">Unidirectional field assignment that uses transforms (right to left)</span></span> |

    <span data-ttu-id="25ca7-131">次の表で、使用可能な変換のタイプについて説明します。</span><span class="sxs-lookup"><span data-stu-id="25ca7-131">The following table describes the available transform types.</span></span>

    | <span data-ttu-id="25ca7-132">変換のタイプ</span><span class="sxs-lookup"><span data-stu-id="25ca7-132">Transform type</span></span> | <span data-ttu-id="25ca7-133">説明</span><span class="sxs-lookup"><span data-stu-id="25ca7-133">Description</span></span> |
    |---|---|
    | <span data-ttu-id="25ca7-134">既定</span><span class="sxs-lookup"><span data-stu-id="25ca7-134">Default</span></span> | <span data-ttu-id="25ca7-135">既定値は、ソース フィールド値が使用できない場合に、宛先フィールドに適用される値です。</span><span class="sxs-lookup"><span data-stu-id="25ca7-135">Default values are values that are applied to destination fields when no source field value is available.</span></span> <span data-ttu-id="25ca7-136">対応するソース フィールドがない場合に、宛先エンティティで必要なフィールドには既定値を使用します。</span><span class="sxs-lookup"><span data-stu-id="25ca7-136">Use default values for fields that are required on the destination entity when you have no corresponding source field.</span></span> |
    | <span data-ttu-id="25ca7-137">値のマップ</span><span class="sxs-lookup"><span data-stu-id="25ca7-137">Value map</span></span> | <span data-ttu-id="25ca7-138">値マップでは、あるエンティティに存在する値を他のエンティティの値にマップする方法を定義します。</span><span class="sxs-lookup"><span data-stu-id="25ca7-138">Value maps define how values that are present in one entity should be mapped to values in the other entity.</span></span> |

4. <span data-ttu-id="25ca7-139">新しいフィールドを追加するには、**マッピングの追加** を選択し、リストの既存のフィールドまたはカスタム フィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="25ca7-139">You can add a new field by selecting **Add mapping** and then selecting an existing or custom field in the list.</span></span>

    <span data-ttu-id="25ca7-140">次の図は、新しい **生年月日** フィールドを追加する例を示しています。</span><span class="sxs-lookup"><span data-stu-id="25ca7-140">The following illustration shows an example where a new **birthdate** field is being added.</span></span>

    ![新しい生年月日フィールドの追加](media/add-new-field.png)

5. <span data-ttu-id="25ca7-142">フィールド マッピングのカスタマイズが完了したら **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="25ca7-142">When you've finished customizing the field mappings, select **Save**.</span></span> <span data-ttu-id="25ca7-143">次に、プロンプトに従って、パブリッシャーとバージョン番号を指定します。</span><span class="sxs-lookup"><span data-stu-id="25ca7-143">Then follow the prompts to specify a publisher and a version number.</span></span>

    ![パブリッシャーとバージョン番号の指定](media/choose-publisher-version.png)

### <a name="filter-your-data"></a><span data-ttu-id="25ca7-145">データのフィルタ処理</span><span class="sxs-lookup"><span data-stu-id="25ca7-145">Filter your data</span></span>

<span data-ttu-id="25ca7-146">二重書き込みでは、Common Data Service の [データ プロトコル (OData) を開く] フィルター式を使用してデータをフィルターできます。</span><span class="sxs-lookup"><span data-stu-id="25ca7-146">Dual-write lets you filter data by using Open Data Protocol (OData) filter expressions for Common Data Service.</span></span> <span data-ttu-id="25ca7-147">Finance and Operations アプリの場合、フィルター処理は、クエリ範囲で使用される範囲式に似ています。</span><span class="sxs-lookup"><span data-stu-id="25ca7-147">For the Finance and Operations app, filtering resembles range expressions that are used in the query range.</span></span>

1. <span data-ttu-id="25ca7-148">[エンティティ マッピング] ページで、フィルター ボタン (じょうごのアイコン) を選択します。</span><span class="sxs-lookup"><span data-stu-id="25ca7-148">On the entity mapping page, select the filter button (funnel symbol).</span></span>

    ![フィルター ボタン](media/select-filter-icon.png)

2. <span data-ttu-id="25ca7-150">**クエリの編集** ダイアログボックスで、フィルターを指定します。</span><span class="sxs-lookup"><span data-stu-id="25ca7-150">In the **Edit query** dialog box, specify your filters.</span></span> <span data-ttu-id="25ca7-151">この例では、指定されたフィルターは、アカウント タイプが **3** であるアカウントのみを返します。</span><span class="sxs-lookup"><span data-stu-id="25ca7-151">In this example, the filter that is specified will return only accounts where the account type equals **3**.</span></span>

    ![フィルターの指定](media/specify-filters.png)

    <span data-ttu-id="25ca7-153">次の表に、フィルター式の例を示します。</span><span class="sxs-lookup"><span data-stu-id="25ca7-153">The following table shows some examples of filter expressions.</span></span>

    | <span data-ttu-id="25ca7-154">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="25ca7-154">Common Data Service</span></span> | <span data-ttu-id="25ca7-155">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="25ca7-155">Finance and Operations apps</span></span> |
    |---|---|
    | <span data-ttu-id="25ca7-156">Accounttype eq '3'</span><span class="sxs-lookup"><span data-stu-id="25ca7-156">Accounttype eq '3'</span></span> | <span data-ttu-id="25ca7-157">(accounttype == '3')</span><span class="sxs-lookup"><span data-stu-id="25ca7-157">(accounttype == '3')</span></span> |
    | <span data-ttu-id="25ca7-158">numberofemployees gt 1000 and</span><span class="sxs-lookup"><span data-stu-id="25ca7-158">numberofemployees gt 1000 and</span></span><br><span data-ttu-id="25ca7-159">numberofemployees le 2000</span><span class="sxs-lookup"><span data-stu-id="25ca7-159">numberofemployees le 2000</span></span> | <span data-ttu-id="25ca7-160">((numberofemployees > 1000) &&</span><span class="sxs-lookup"><span data-stu-id="25ca7-160">((numberofemployees > 1000) &&</span></span><br><span data-ttu-id="25ca7-161">(numberofemployees <= 2000))</span><span class="sxs-lookup"><span data-stu-id="25ca7-161">(numberofemployees <= 2000))</span></span> |

    <span data-ttu-id="25ca7-162">クエリ範囲で式を使用する方法の例については、[クエリ範囲での式の使用](https://docs.microsoft.com/dynamicsax-2012/developer/using-expressions-in-query-ranges) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="25ca7-162">For more examples that show how to use expressions in query ranges, see [Using Expressions in Query Ranges](https://docs.microsoft.com/dynamicsax-2012/developer/using-expressions-in-query-ranges).</span></span>
    
    <span data-ttu-id="25ca7-163">現時点では、二重書き込みソース フィルターでのネストされたルックアップはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="25ca7-163">Currently, we do not support nested lookups in dual-write source filter.</span></span> <span data-ttu-id="25ca7-164">エンティティのフィールドに対して直接、標準のフィルタ演算子のみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="25ca7-164">Only standard filter operators directly against entity fields are supported.</span></span> <span data-ttu-id="25ca7-165">例については、[標準フィルタ演算子](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/query-data-web-api#standard-filter-operators) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="25ca7-165">For more examples, see [Standard filter operators](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/query-data-web-api#standard-filter-operators).</span></span>
    
## <a name="add-new-entity-maps"></a><span data-ttu-id="25ca7-166">新しいエンティティ マップの追加</span><span class="sxs-lookup"><span data-stu-id="25ca7-166">Add new entity maps</span></span>

<span data-ttu-id="25ca7-167">Microsoft は引き続き新しいエンティティを追加していますが、標準またはカスタムのエンティティ マップを追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="25ca7-167">Although Microsoft is continuing to add new entities, you can also add standard or custom entity maps.</span></span>

<span data-ttu-id="25ca7-168">次の例は、**アドレス帳** という名前の新しいエンティティ マップを追加する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="25ca7-168">The following example shows how to add a new entity map that is named **Address books**.</span></span>

1. <span data-ttu-id="25ca7-169">Finance and Operations アプリの **二重書き込み** ページで、**エンティティ マップの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="25ca7-169">In the Finance and Operations app, on the **Dual-write** page, select **Add entity map**.</span></span>

    ![新しいエンティティ マップの追加](media/add-new-entity-map.png)

    > [!NOTE]
    > <span data-ttu-id="25ca7-171">これらの変更済みエンティティ マップを使用する [新しいソリューションを作成する](app-lifecycle-management.md#create-a-new-dual-write-solution-and-add-your-components-customized-entity-maps) 場合は、同じパブリッシャーを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="25ca7-171">When you [create a new solution](app-lifecycle-management.md#create-a-new-dual-write-solution-and-add-your-components-customized-entity-maps) that uses these modified entity maps, you must specify the same publisher.</span></span>

2. <span data-ttu-id="25ca7-172">変更および追加したエンティティ マップを確認します。</span><span class="sxs-lookup"><span data-stu-id="25ca7-172">Confirm the entity maps that you just modified and added.</span></span> <span data-ttu-id="25ca7-173">それらを有効にしてテストし、期待どおりに機能することを確認してください。</span><span class="sxs-lookup"><span data-stu-id="25ca7-173">Be sure to enable and test them, to ensure that they work as you expect.</span></span>

    ![エンティティ マップの確認](media/confirm-entity-maps.png)

## <a name="next-steps"></a><span data-ttu-id="25ca7-175">次のステップ</span><span class="sxs-lookup"><span data-stu-id="25ca7-175">Next steps</span></span>

[<span data-ttu-id="25ca7-176">エラー管理と警告通知</span><span class="sxs-lookup"><span data-stu-id="25ca7-176">Error management and alert notifications</span></span>](errors-and-alerts.md)
