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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sabinn
ms.search.validFrom: 2020-03-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee1872f0ef8cb5f7cb07d11fc5cc79c05f5b1902
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683661"
---
# <a name="customize-entity-and-field-mappings"></a><span data-ttu-id="7bfe0-103">エンティティとフィールドのマッピングのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="7bfe0-103">Customize entity and field mappings</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="7bfe0-104">すぐに使えるテーブル マップには、2 つのアプリ間のデータ フローを可能にする事前定義されたエンティティおよびフィールド マッピングがあります。</span><span class="sxs-lookup"><span data-stu-id="7bfe0-104">The out-of-box table maps have predefined entity and field mappings that enable the flow of data between two apps.</span></span> <span data-ttu-id="7bfe0-105">このように、それらは "青写真" として機能します。</span><span class="sxs-lookup"><span data-stu-id="7bfe0-105">In this way, they serve as "blueprints."</span></span> <span data-ttu-id="7bfe0-106">ただし、ビジネスごとに異なるため、既定のテーブル マップでは不十分な場合があります。</span><span class="sxs-lookup"><span data-stu-id="7bfe0-106">However, because every business is different, the default table maps might sometimes not be enough.</span></span> <span data-ttu-id="7bfe0-107">したがって、二重書き込みは、テーブル マップおよびフィールド マッピングを変更する方法を提供することにより、カスタマイズを完全にサポートします。</span><span class="sxs-lookup"><span data-stu-id="7bfe0-107">Therefore, dual-write fully supports customization by providing ways to change table maps and field mappings.</span></span>

## <a name="customize-field-mappings-add-transforms-and-enable-filtering"></a><span data-ttu-id="7bfe0-108">フィールド マッピングのカスタマイズ、変換の追加、およびフィルタ処理の有効化</span><span class="sxs-lookup"><span data-stu-id="7bfe0-108">Customize field mappings, add transforms, and enable filtering</span></span>

1. <span data-ttu-id="7bfe0-109">Finance and Operations アプリの **二重書き込み** ページの **テーブル マッピング** タブで、カスタマイズするテーブル マップを選択します。</span><span class="sxs-lookup"><span data-stu-id="7bfe0-109">In your Finance and Operations app, on the **Dual-write** page, on the **Table mappings** tab, select the table map to customize.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7bfe0-110">テーブル マッピングを変更する前に、停止する (実行しない) 必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bfe0-110">Before you change table mappings, they must be stopped (not running).</span></span> <span data-ttu-id="7bfe0-111">そうしないと、変更は保存されません。</span><span class="sxs-lookup"><span data-stu-id="7bfe0-111">Otherwise, your changes won't be saved.</span></span>

2. <span data-ttu-id="7bfe0-112">**テーブル マッピング** タブで、Finance and Operations アプリまたは Dataverse から新しいフィールドまたはカスタム フィールドを選択して、フィールドをカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="7bfe0-112">On the **Table mappings** tab, you can customize a field by selecting a new or custom field from either the Finance and Operations app or Dataverse.</span></span>

    ![フィールドのカスタマイズ](media/customize-a-field.png)

3. <span data-ttu-id="7bfe0-114">同期の方向 (単一方向または双方向) をカスタマイズし、マップの種類を選択して変換を追加できます。</span><span class="sxs-lookup"><span data-stu-id="7bfe0-114">You can customize the synchronization direction (unidirectional or bidirectional) and add transforms by selecting the map type.</span></span>

    ![同期の方向のカスタマイズと変換の追加](media/customize-sync-direction.png)

    <span data-ttu-id="7bfe0-116">次の表で、使用可能な同期の方向について説明します。</span><span class="sxs-lookup"><span data-stu-id="7bfe0-116">The following table describes the available synchronization directions.</span></span>

    | <span data-ttu-id="7bfe0-117">記号</span><span class="sxs-lookup"><span data-stu-id="7bfe0-117">Symbol</span></span> | <span data-ttu-id="7bfe0-118">説明</span><span class="sxs-lookup"><span data-stu-id="7bfe0-118">Description</span></span> |
    |---|---|
    | ![等号](media/equal-symbol.png) | <span data-ttu-id="7bfe0-120">双方向のフィールド割り当て</span><span class="sxs-lookup"><span data-stu-id="7bfe0-120">Bidirectional field assignment</span></span> |
    | ![大なり/小なり記号](media/greater-less-symbol.png) | <span data-ttu-id="7bfe0-122">変換を使用する双方向フィールド割り当て</span><span class="sxs-lookup"><span data-stu-id="7bfe0-122">Bidirectional field assignment that uses transforms</span></span> |
    | ![大なり記号](media/greater-than-symbol.png) | <span data-ttu-id="7bfe0-124">単一方向フィールド割り当て (左から右)</span><span class="sxs-lookup"><span data-stu-id="7bfe0-124">Unidirectional field assignment (left to right)</span></span> |
    | ![小なり記号](media/less-than-symbol.png) | <span data-ttu-id="7bfe0-126">単一方向フィールド割り当て (右から左)</span><span class="sxs-lookup"><span data-stu-id="7bfe0-126">Unidirectional field assignment (right to left)</span></span> |
    | ![右矢印キー](media/right-arrow-symbol.png) | <span data-ttu-id="7bfe0-128">変換を使用する単一方向フィールド割り当て (左から右)</span><span class="sxs-lookup"><span data-stu-id="7bfe0-128">Unidirectional field assignment that uses transforms (left to right)</span></span> |
    | ![左矢印キー](media/left-arrow-symbol.png) | <span data-ttu-id="7bfe0-130">変換を使用する単一方向フィールド割り当て (右から左)</span><span class="sxs-lookup"><span data-stu-id="7bfe0-130">Unidirectional field assignment that uses transforms (right to left)</span></span> |

    <span data-ttu-id="7bfe0-131">次の表で、使用可能な変換のタイプについて説明します。</span><span class="sxs-lookup"><span data-stu-id="7bfe0-131">The following table describes the available transform types.</span></span>

    | <span data-ttu-id="7bfe0-132">変換のタイプ</span><span class="sxs-lookup"><span data-stu-id="7bfe0-132">Transform type</span></span> | <span data-ttu-id="7bfe0-133">説明</span><span class="sxs-lookup"><span data-stu-id="7bfe0-133">Description</span></span> |
    |---|---|
    | <span data-ttu-id="7bfe0-134">既定</span><span class="sxs-lookup"><span data-stu-id="7bfe0-134">Default</span></span> | <span data-ttu-id="7bfe0-135">既定値は、ソース フィールド値が使用できない場合に、宛先フィールドに適用される値です。</span><span class="sxs-lookup"><span data-stu-id="7bfe0-135">Default values are values that are applied to destination fields when no source field value is available.</span></span> <span data-ttu-id="7bfe0-136">対応するソース フィールドがない場合に、宛先エンティティで必要なフィールドには既定値を使用します。</span><span class="sxs-lookup"><span data-stu-id="7bfe0-136">Use default values for fields that are required on the destination entity when you have no corresponding source field.</span></span> |
    | <span data-ttu-id="7bfe0-137">値のマップ</span><span class="sxs-lookup"><span data-stu-id="7bfe0-137">Value map</span></span> | <span data-ttu-id="7bfe0-138">値マップでは、あるエンティティに存在する値を他のエンティティの値にマップする方法を定義します。</span><span class="sxs-lookup"><span data-stu-id="7bfe0-138">Value maps define how values that are present in one entity should be mapped to values in the other entity.</span></span> |

4. <span data-ttu-id="7bfe0-139">新しいフィールドを追加するには、**マッピングの追加** を選択し、リストの既存のフィールドまたはカスタム フィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="7bfe0-139">You can add a new field by selecting **Add mapping** and then selecting an existing or custom field in the list.</span></span>

    <span data-ttu-id="7bfe0-140">次の図は、新しい **生年月日** フィールドを追加する例を示しています。</span><span class="sxs-lookup"><span data-stu-id="7bfe0-140">The following illustration shows an example where a new **birthdate** field is being added.</span></span>

    ![新しい生年月日フィールドの追加](media/add-new-field.png)

5. <span data-ttu-id="7bfe0-142">フィールド マッピングのカスタマイズが完了したら **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bfe0-142">When you've finished customizing the field mappings, select **Save**.</span></span> <span data-ttu-id="7bfe0-143">次に、プロンプトに従って、パブリッシャーとバージョン番号を指定します。</span><span class="sxs-lookup"><span data-stu-id="7bfe0-143">Then follow the prompts to specify a publisher and a version number.</span></span>

    ![パブリッシャーとバージョン番号の指定](media/choose-publisher-version.png)

### <a name="filter-your-data"></a><span data-ttu-id="7bfe0-145">データのフィルタ処理</span><span class="sxs-lookup"><span data-stu-id="7bfe0-145">Filter your data</span></span>

<span data-ttu-id="7bfe0-146">二重書き込みでは、Dataverse の [データ プロトコル (OData) を開く] フィルター式を使用してデータをフィルターできます。</span><span class="sxs-lookup"><span data-stu-id="7bfe0-146">Dual-write lets you filter data by using Open Data Protocol (OData) filter expressions for Dataverse.</span></span> <span data-ttu-id="7bfe0-147">Finance and Operations アプリの場合、フィルター処理は、クエリ範囲で使用される範囲式に似ています。</span><span class="sxs-lookup"><span data-stu-id="7bfe0-147">For the Finance and Operations app, filtering resembles range expressions that are used in the query range.</span></span>

1. <span data-ttu-id="7bfe0-148">テーブル マッピング ページで、フィルター ボタン (じょうごのアイコン) を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bfe0-148">On the table mapping page, select the filter button (funnel symbol).</span></span>

    ![フィルター ボタン](media/select-filter-icon.png)

2. <span data-ttu-id="7bfe0-150">**クエリの編集** ダイアログボックスで、フィルターを指定します。</span><span class="sxs-lookup"><span data-stu-id="7bfe0-150">In the **Edit query** dialog box, specify your filters.</span></span> <span data-ttu-id="7bfe0-151">この例では、指定されたフィルターは、アカウント タイプが **3** であるアカウントのみを返します。</span><span class="sxs-lookup"><span data-stu-id="7bfe0-151">In this example, the filter that is specified will return only accounts where the account type equals **3**.</span></span>

    ![フィルターの指定](media/specify-filters.png)

    <span data-ttu-id="7bfe0-153">次の表に、フィルター式の例を示します。</span><span class="sxs-lookup"><span data-stu-id="7bfe0-153">The following table shows some examples of filter expressions.</span></span>

    | <span data-ttu-id="7bfe0-154">Dataverse</span><span class="sxs-lookup"><span data-stu-id="7bfe0-154">Dataverse</span></span> | <span data-ttu-id="7bfe0-155">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="7bfe0-155">Finance and Operations apps</span></span> |
    |---|---|
    | <span data-ttu-id="7bfe0-156">Accounttype eq '3'</span><span class="sxs-lookup"><span data-stu-id="7bfe0-156">Accounttype eq '3'</span></span> | <span data-ttu-id="7bfe0-157">(accounttype == '3')</span><span class="sxs-lookup"><span data-stu-id="7bfe0-157">(accounttype == '3')</span></span> |
    | <span data-ttu-id="7bfe0-158">numberofemployees gt 1000 and</span><span class="sxs-lookup"><span data-stu-id="7bfe0-158">numberofemployees gt 1000 and</span></span><br><span data-ttu-id="7bfe0-159">numberofemployees le 2000</span><span class="sxs-lookup"><span data-stu-id="7bfe0-159">numberofemployees le 2000</span></span> | <span data-ttu-id="7bfe0-160">((numberofemployees > 1000) &&</span><span class="sxs-lookup"><span data-stu-id="7bfe0-160">((numberofemployees > 1000) &&</span></span><br><span data-ttu-id="7bfe0-161">(numberofemployees <= 2000))</span><span class="sxs-lookup"><span data-stu-id="7bfe0-161">(numberofemployees <= 2000))</span></span> |

    <span data-ttu-id="7bfe0-162">クエリ範囲で式を使用する方法の例については、[クエリ範囲での式の使用](https://docs.microsoft.com/dynamicsax-2012/developer/using-expressions-in-query-ranges) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bfe0-162">For more examples that show how to use expressions in query ranges, see [Using Expressions in Query Ranges](https://docs.microsoft.com/dynamicsax-2012/developer/using-expressions-in-query-ranges).</span></span>
    
    <span data-ttu-id="7bfe0-163">現時点では、二重書き込みソース フィルターでのネストされたルックアップはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="7bfe0-163">Currently, we do not support nested lookups in dual-write source filter.</span></span> <span data-ttu-id="7bfe0-164">エンティティのフィールドに対して直接、標準のフィルタ演算子のみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="7bfe0-164">Only standard filter operators directly against entity fields are supported.</span></span> <span data-ttu-id="7bfe0-165">例については、[標準フィルタ演算子](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/query-data-web-api#standard-filter-operators) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7bfe0-165">For more examples, see [Standard filter operators](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/query-data-web-api#standard-filter-operators).</span></span>
    
## <a name="add-new-table-maps"></a><span data-ttu-id="7bfe0-166">新しいテーブル マップの追加</span><span class="sxs-lookup"><span data-stu-id="7bfe0-166">Add new table maps</span></span>

<span data-ttu-id="7bfe0-167">Microsoft は引き続き新しいテーブルを追加していますが、標準またはカスタムのテーブル マップを追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="7bfe0-167">Although Microsoft is continuing to add new tables, you can also add standard or custom table maps.</span></span>

<span data-ttu-id="7bfe0-168">次の例は、**アドレス帳** という名前の新しいテーブル マップを追加する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="7bfe0-168">The following example shows how to add a new table map that is named **Address books**.</span></span>

1. <span data-ttu-id="7bfe0-169">Finance and Operations アプリの **二重書き込み** ページで、**テーブル マップの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7bfe0-169">In the Finance and Operations app, on the **Dual-write** page, select **Add table map**.</span></span>

    ![新しいテーブル マップの追加](media/add-new-entity-map.png)

    > [!NOTE]
    > <span data-ttu-id="7bfe0-171">これらの変更済みテーブル マップを使用する[新しいソリューションを作成する](app-lifecycle-management.md#create-new-solution) 場合は、同じパブリッシャーを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7bfe0-171">When you [create a new solution](app-lifecycle-management.md#create-new-solution) that uses these modified table maps, you must specify the same publisher.</span></span>

2. <span data-ttu-id="7bfe0-172">変更および追加したテーブル マップを確認します。</span><span class="sxs-lookup"><span data-stu-id="7bfe0-172">Confirm the table maps that you just modified and added.</span></span> <span data-ttu-id="7bfe0-173">それらを有効にしてテストし、期待どおりに機能することを確認してください。</span><span class="sxs-lookup"><span data-stu-id="7bfe0-173">Be sure to enable and test them, to ensure that they work as you expect.</span></span>

    ![テーブル マップの確認](media/confirm-entity-maps.png)

## <a name="next-steps"></a><span data-ttu-id="7bfe0-175">次のステップ</span><span class="sxs-lookup"><span data-stu-id="7bfe0-175">Next steps</span></span>

[<span data-ttu-id="7bfe0-176">エラー管理と警告通知</span><span class="sxs-lookup"><span data-stu-id="7bfe0-176">Error management and alert notifications</span></span>](errors-and-alerts.md)
