---
title: 拡張機能を通じた新しい在庫分析コードの追加
description: このトピックでは、拡張機能を通じて新しい在庫分析コードを追加する方法について説明します。
author: MichaelFruergaardPontoppidan
manager: AnnBe
ms.date: 02/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 89563
ms.assetid: ''
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 775097c087c342ad46453bf38ea5bdbe69853540
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183318"
---
# <a name="add-new-inventory-dimensions-through-extension"></a><span data-ttu-id="0ac26-103">拡張機能を通じた新しい在庫分析コードの追加</span><span class="sxs-lookup"><span data-stu-id="0ac26-103">Add new inventory dimensions through extension</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ac26-104">このトピックでは、拡張機能を使用して新しい在庫分析コードを追加する方法の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="0ac26-104">This topic provides a high-level overview of how to add new inventory dimensions through extensions.</span></span> <span data-ttu-id="0ac26-105">また、実際の実装を含むサンプル アプリケーションへのアクセス方法に関する情報も含まれます。</span><span class="sxs-lookup"><span data-stu-id="0ac26-105">It also includes information about how to access a sample application that contains an actual implementation.</span></span>

## <a name="solution-overview"></a><span data-ttu-id="0ac26-106">ソリューションの概要</span><span class="sxs-lookup"><span data-stu-id="0ac26-106">Solution overview</span></span>
<span data-ttu-id="0ac26-107">このソリューションで重要なことは、複数のロールが、拡張機能を介して新しい在庫分析コードを追加するライフサイクルに参加することです。</span><span class="sxs-lookup"><span data-stu-id="0ac26-107">The cornerstone in this solution is that multiple roles participate in the life cycle of adding new inventory dimensions through extensions.</span></span> <span data-ttu-id="0ac26-108">次の説明では、このソリューションを簡略化して一般化していますが、現実にはロールの重複があり、時には同じ人が複数のロールを果たす場合もあります。</span><span class="sxs-lookup"><span data-stu-id="0ac26-108">The following description simplifies and generalizes this solution, however, in real life there is overlap between the roles, and sometimes it might even be the same person filling several roles.</span></span>

### <a name="microsofts-role"></a><span data-ttu-id="0ac26-109">Microsoft のロール</span><span class="sxs-lookup"><span data-stu-id="0ac26-109">Microsoft's role</span></span>
<span data-ttu-id="0ac26-110">Microsoft は、使用されていない分析コード フィールドの限定的なセットを提供します。</span><span class="sxs-lookup"><span data-stu-id="0ac26-110">Microsoft provides a finite set of unused dimension fields.</span></span>

<span data-ttu-id="0ac26-111">15 の既存の分析コードに加えて、Microsoft は 10 の一般的な分析コードをサポートします。</span><span class="sxs-lookup"><span data-stu-id="0ac26-111">In addition to the 15 existing dimensions, Microsoft supports 10 generic dimensions:</span></span> 
- <span data-ttu-id="0ac26-112">8 つの文字列ベース</span><span class="sxs-lookup"><span data-stu-id="0ac26-112">8 string-based</span></span>
- <span data-ttu-id="0ac26-113">リアルベース 1 つ</span><span class="sxs-lookup"><span data-stu-id="0ac26-113">1 real-based</span></span>
- <span data-ttu-id="0ac26-114">utcdatetime ベース 1 つ</span><span class="sxs-lookup"><span data-stu-id="0ac26-114">1 utcdatetime-based</span></span>
 
  <span data-ttu-id="0ac26-115">これにより、標準アプリケーションのインベントリ ディメンションの合計数が 25 になります。</span><span class="sxs-lookup"><span data-stu-id="0ac26-115">This brings the total number of inventory dimensions in the standard application to 25:</span></span>
- <span data-ttu-id="0ac26-116">4 製品分析コード: 色、サイズ、スタイル、およびコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="0ac26-116">4 product dimensions: Color, Size, Style, and Config</span></span>
- <span data-ttu-id="0ac26-117">5 つの追跡用分析コード: シリアル、バッチ、所有者、プロファイル (ロシアのみ)、および GTD (ロシアのみ)</span><span class="sxs-lookup"><span data-stu-id="0ac26-117">5 tracking dimensions: Serial, Batch, Owner, Profile (Russia only), and GTD (Russia only)</span></span>
- <span data-ttu-id="0ac26-118">6. 保管分析コード: サイト、倉庫、場所、ステータス、ライセンス プレートおよびパレット (アップグレードと移行のみ)</span><span class="sxs-lookup"><span data-stu-id="0ac26-118">6 storage dimensions: Site, Warehouse, Location, Status, License Plate, and Pallet (for upgrade and migration only)</span></span>
- <span data-ttu-id="0ac26-119">10 個の未割り当ての一般的な分析コード: InventDimension10 から InventDimension1</span><span class="sxs-lookup"><span data-stu-id="0ac26-119">10 unassigned generic dimensions: InventDimension1 to InventDimension10</span></span>

<span data-ttu-id="0ac26-120">Microsoft は、物理スキーマを提供しています。</span><span class="sxs-lookup"><span data-stu-id="0ac26-120">Microsoft provides the physical schema.</span></span>

### <a name="isv-role"></a><span data-ttu-id="0ac26-121">ISV 役割</span><span class="sxs-lookup"><span data-stu-id="0ac26-121">ISV role</span></span>
<span data-ttu-id="0ac26-122">ISV は、新規在庫分析コードを追加します。</span><span class="sxs-lookup"><span data-stu-id="0ac26-122">The ISV adds new inventory dimensions.</span></span> <span data-ttu-id="0ac26-123">ISV ソリューションは、分析コードの特定のすべての機能を提供します。強力な種類で、管理、テストしやすく、パフォーマンスの高いものでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="0ac26-123">The ISV solution provides all the specific functionality for the dimension - it must be strong-typed, maintainable, testable, and performant.</span></span> <span data-ttu-id="0ac26-124">さらに、ソリューションは、その他の ISV のソリューションに依存しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ac26-124">In addition, the solution must be agnostic to other ISV's solutions.</span></span>
<span data-ttu-id="0ac26-125">ISV は、物理スキーマを直接参照せず、シームレスに行うことができる間接参照を通過するソリューションを構築します。</span><span class="sxs-lookup"><span data-stu-id="0ac26-125">The ISV builds a solution that doesn't reference the physical schema directly, but goes through an indirection, which can be done seamlessly.</span></span> 

<span data-ttu-id="0ac26-126">ISV は、論理実装を提供します。</span><span class="sxs-lookup"><span data-stu-id="0ac26-126">The ISV provides the logical implementation.</span></span>

### <a name="var-role"></a><span data-ttu-id="0ac26-127">VAR ロール</span><span class="sxs-lookup"><span data-stu-id="0ac26-127">VAR role</span></span>
<span data-ttu-id="0ac26-128">VAR は、完全に機能するシステムを顧客に出荷できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ac26-128">The VAR must be able to deliver a fully functional system to a customer.</span></span> <span data-ttu-id="0ac26-129">システムには、複数の ISV のソリューションを含めることができます。それぞれに新しい在庫分析コードが含まれる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0ac26-129">The system can contain solutions from multiple ISV's - each potentially containing new inventory dimensions.</span></span> <span data-ttu-id="0ac26-130">合計で最大 10 個の ISV 分析コード フィールドがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="0ac26-130">In total, up to 10 ISV dimension fields are supported.</span></span>

<span data-ttu-id="0ac26-131">VAR により、物理的データ モデルと論理的実装が結合されます。</span><span class="sxs-lookup"><span data-stu-id="0ac26-131">The VAR provides the binding between the physical data model and logical implementation.</span></span>

## <a name="details"></a><span data-ttu-id="0ac26-132">細目</span><span class="sxs-lookup"><span data-stu-id="0ac26-132">Details</span></span>
<span data-ttu-id="0ac26-133">ソリューションの前半はシンプルです。</span><span class="sxs-lookup"><span data-stu-id="0ac26-133">The first half of the solution is straight forward.</span></span> <span data-ttu-id="0ac26-134">新しいクラス階層が導入されています。</span><span class="sxs-lookup"><span data-stu-id="0ac26-134">A new class hierarchy is introduced.</span></span> <span data-ttu-id="0ac26-135">それぞれの新しい分析コードは、InventProductDimension または InventTrackingDimension のいずれかから派生する新しいクラスに実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ac26-135">Each new dimension must be implemented in a new class deriving from either InventProductDimension or InventTrackingDimension.</span></span> <span data-ttu-id="0ac26-136">現在、保管分析コードのサポートがされていません。</span><span class="sxs-lookup"><span data-stu-id="0ac26-136">Currently, there is no support for storage dimensions.</span></span> <span data-ttu-id="0ac26-137">これを使用すると、ISV は InventDim テーブルのロジックを変更せずに新しい分析コードを導入することができます。</span><span class="sxs-lookup"><span data-stu-id="0ac26-137">With this, ISVs can introduce new dimensions without having to change any of the logic on the InventDim table.</span></span> 

![InventDimensionClassHierarchy](media/InventDimensions1.png)

<span data-ttu-id="0ac26-139">厳密に型指定された新しい分析コードを参照するために、ISV では InventDim テーブルにテーブル拡張クラスが導入されました。</span><span class="sxs-lookup"><span data-stu-id="0ac26-139">To reference the new dimension in a strongly-typed fashion, the ISV introduces a table extension class to the InventDim table.</span></span> <span data-ttu-id="0ac26-140">スタイル、色、サイズの拡張クラスをテンプレートとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="0ac26-140">The extension classes for Style, Color, and Size can be used as templates.</span></span>
 
<span data-ttu-id="0ac26-141">**例: InventDimStyle_Extension**</span><span class="sxs-lookup"><span data-stu-id="0ac26-141">**Example: InventDimStyle_Extension**</span></span> 

```
/// <summary>
/// The <c>InventDimStyle_Extension</c> class extends the <c>InventDim</c> table with behavior for the style dimension.
/// </summary>
[ExtensionOf(tableStr(InventDim))]
final class InventDimStyle_Extension
{
    public EcoResItemStyleName parmInventStyleId(EcoResItemStyleName _style = this.getValueForDimension(classStr(InventProductDimensionStyle)))
    {
        if (!prmIsDefault(_style))
        {
            this.setValueForDimension(classStr(InventProductDimensionStyle), _style);
        }
        return _style;
    }

    /// <summary>
    /// Returns the field id for the style dimension.
    /// </summary>
    /// <returns>The field id.</returns>
    public static FieldId fieldIdStyle()
    {
        return InventDim::fieldIdForDimension(classStr(InventProductDimensionStyle));
    }
}
```

<span data-ttu-id="0ac26-142">分析コードは、次のように参照することができます。</span><span class="sxs-lookup"><span data-stu-id="0ac26-142">The dimensions can be referenced like this.</span></span>

```
//Setting a value
inventDim.parmISVDim("Some value");

//Select statements
select inventDim
    where inventDim.(InventDim::fieldIdISVDim()) == "Some value";
```

<span data-ttu-id="0ac26-143">ISV は、新しい在庫分析コードの分析コード値のリストを保持するために、データ モデルおよびユーザー インターフェイスなどのロジックを構築できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="0ac26-143">The ISV can now build logic, including the data model and user interface for maintaining the list of dimension values, for the new inventory dimension.</span></span>

<span data-ttu-id="0ac26-144">ソリューションの後半はデータ モデルです。</span><span class="sxs-lookup"><span data-stu-id="0ac26-144">The second half of the solution is the data model.</span></span> <span data-ttu-id="0ac26-145">標準アプリケーションには、新しい分析コードごとに次の内容が含まれます。</span><span class="sxs-lookup"><span data-stu-id="0ac26-145">The standard application will contain the following for each new dimension:</span></span>
- <span data-ttu-id="0ac26-146">ラベル ファイル。</span><span class="sxs-lookup"><span data-stu-id="0ac26-146">A label file.</span></span>
- <span data-ttu-id="0ac26-147">コンフィギュレーション キー。</span><span class="sxs-lookup"><span data-stu-id="0ac26-147">A configuration key.</span></span>
- <span data-ttu-id="0ac26-148">2 つの拡張データ型 (EDT) (InventDim のフィールド用と InventDimParm のフラグ用) です。</span><span class="sxs-lookup"><span data-stu-id="0ac26-148">Two extended data types (EDTs) (for the field on InventDim and for the flag on InventDimParm).</span></span>
- <span data-ttu-id="0ac26-149">InventDim テーブルの 1 つのフィールドです。</span><span class="sxs-lookup"><span data-stu-id="0ac26-149">One field on InventDim table.</span></span>
- <span data-ttu-id="0ac26-150">InventDimParm テーブルの 1 つのフィールドです。</span><span class="sxs-lookup"><span data-stu-id="0ac26-150">One field on InventDimParm table.</span></span>
- <span data-ttu-id="0ac26-151">InventDimFieldMap マップの 1 つのフィールドと、各テーブルの 1 つのフィールド (約 30) がマップされています。</span><span class="sxs-lookup"><span data-stu-id="0ac26-151">One field on InventDimFieldMap map and one field on each of the tables (approximately 30) mapped.</span></span>

<span data-ttu-id="0ac26-152">VAR の職務は、特定の顧客の InventDim の分析コード フィールドに ISV ソリューションを書き込むことです。</span><span class="sxs-lookup"><span data-stu-id="0ac26-152">The VAR's job is to wire the ISV solutions to the available dimension fields on InventDim for a given customer.</span></span> <span data-ttu-id="0ac26-153">この作業を最小にするために、現在以下が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0ac26-153">To minimize this work, it currently includes the following:</span></span>
- <span data-ttu-id="0ac26-154">バインディング マッピングを実装します。</span><span class="sxs-lookup"><span data-stu-id="0ac26-154">Implement the binding mapping.</span></span> <span data-ttu-id="0ac26-155">これは、メソッド InventDimFieldBinding.className2FieldName() メソッドを拡張するよって行います。</span><span class="sxs-lookup"><span data-stu-id="0ac26-155">This is accomplished by extending the method InventDimFieldBinding.className2FieldName().</span></span>
- <span data-ttu-id="0ac26-156">コンフィギュレーション キーを有効にします。</span><span class="sxs-lookup"><span data-stu-id="0ac26-156">Enable the configuration key.</span></span>
- <span data-ttu-id="0ac26-157">右側の文字列のサイズを指定するには、EDT を拡張します。</span><span class="sxs-lookup"><span data-stu-id="0ac26-157">Extend the EDT to specify the right string size.</span></span>
- <span data-ttu-id="0ac26-158">ISV 製ラベルを正しいラベル ファイルにコピーするなど、ラベル ファイルを拡張します。</span><span class="sxs-lookup"><span data-stu-id="0ac26-158">Extend the Label file, such as copy the ISV-provided labels into the correct label file.</span></span>
- <span data-ttu-id="0ac26-159">InventDim の ProductDimensions または TrackingDimensions フィールド グループおよび分析コードのタイプに応じていくつかの他のテーブルを拡張します。</span><span class="sxs-lookup"><span data-stu-id="0ac26-159">Extend the ProductDimensions or TrackingDimensions field groups on InventDim, and a few other tables, depending on the type of dimension.</span></span>
- <span data-ttu-id="0ac26-160">関係およびインデックスを必要に応じて、InventDim で拡張します。</span><span class="sxs-lookup"><span data-stu-id="0ac26-160">Extend relations and index as needed on InventDim.</span></span>

![InventDimensionISVVARExtensions](media/InventDimensions4.png)

## <a name="known-issues"></a><span data-ttu-id="0ac26-162">既知の問題</span><span class="sxs-lookup"><span data-stu-id="0ac26-162">Known issues</span></span>

<span data-ttu-id="0ac26-163">ソリューションの設計に影響を与えるいくつかの技術的な制限があります。</span><span class="sxs-lookup"><span data-stu-id="0ac26-163">There are some technical limitations influencing the design of the solution.</span></span> <span data-ttu-id="0ac26-164">最も重要なのは、InventDim のWhere 句を含むアプリケーション全体の SQL 文です。</span><span class="sxs-lookup"><span data-stu-id="0ac26-164">The most significant is the SQL statements throughout the application that contain where-clauses on InventDim.</span></span> <span data-ttu-id="0ac26-165">これらのほとんどはマクロを使用して実装され、SQL ステートメントが拡張可能ではないという事実を変更しません。</span><span class="sxs-lookup"><span data-stu-id="0ac26-165">Most of these are implemented using macros, which doesn't change the fact that SQL statements are not extensible.</span></span> <span data-ttu-id="0ac26-166">SQL ステートメントの多くは書き換えることができ、クエリ オブジェクトを使用して拡張できますが、多くの delete_from および update_recordset は残ります。</span><span class="sxs-lookup"><span data-stu-id="0ac26-166">Many of the SQL statements could be rewritten to use query objects to make them extensible, however many delete_from and update_recordset would remain.</span></span> <span data-ttu-id="0ac26-167">実行可能なソリューションは、新しい分析コードを追加するときに、これらの SQL ステートメントへの変更を要求することはできません。</span><span class="sxs-lookup"><span data-stu-id="0ac26-167">A viable solution cannot require changes to these SQL statements when adding new dimensions.</span></span>

<span data-ttu-id="0ac26-168">もう 1 つの技術的な制限は、サポートできる在庫分析コードの量です。</span><span class="sxs-lookup"><span data-stu-id="0ac26-168">Another technical limitation is the amount of inventory dimensions that can be supported.</span></span> <span data-ttu-id="0ac26-169">それぞれが小さなオーバーヘッドを追加し、InventDimFixed EDT は上限を 32 に設定します。</span><span class="sxs-lookup"><span data-stu-id="0ac26-169">Each adds a small overhead, and the InventDimFixed EDT sets an upper limit at 32.</span></span> <span data-ttu-id="0ac26-170">この EDT には各分析コードのビットマスクが含まれており、EDT は整数であるため制限は 32 です。</span><span class="sxs-lookup"><span data-stu-id="0ac26-170">This EDT contains a bit mask for each dimension, and because the EDT is an integer, the limit is 32.</span></span> <span data-ttu-id="0ac26-171">指定されたソリューションは 32 の制限内で保持されます。</span><span class="sxs-lookup"><span data-stu-id="0ac26-171">The provided solution stays within the limit of 32.</span></span> <span data-ttu-id="0ac26-172">将来に必要になる場合、InventDimFixed を Int64、コンテナーに変更するまたは削除することができます。</span><span class="sxs-lookup"><span data-stu-id="0ac26-172">If required in the future, InventDimFixed could be changed to be an Int64, a container, or it could be removed.</span></span>

## <a name="sample-application"></a><span data-ttu-id="0ac26-173">サンプル アプリケーション</span><span class="sxs-lookup"><span data-stu-id="0ac26-173">Sample application</span></span>

<span data-ttu-id="0ac26-174">「製品フレーバーの分析コード サンプル アプリケーション」と呼ばれるサンプル アプリケーションは、[GitHub](https://github.com/Microsoft/Product-flavor-dimension-sample-app) で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="0ac26-174">A sample application called "Product flavor dimension sample app" can be found on [GitHub](https://github.com/Microsoft/Product-flavor-dimension-sample-app).</span></span> 

<span data-ttu-id="0ac26-175">この例は 3 つのモデルで構成されています。</span><span class="sxs-lookup"><span data-stu-id="0ac26-175">This sample consists of three models:</span></span> 
 - <span data-ttu-id="0ac26-176">ISV の生産コード</span><span class="sxs-lookup"><span data-stu-id="0ac26-176">ISV production code</span></span>
 - <span data-ttu-id="0ac26-177">ISV テスト コード</span><span class="sxs-lookup"><span data-stu-id="0ac26-177">ISV test code</span></span>
 - <span data-ttu-id="0ac26-178">VAR 統合コード</span><span class="sxs-lookup"><span data-stu-id="0ac26-178">VAR integration code</span></span>
 
<span data-ttu-id="0ac26-179">これらのモデルを組み合わせると、新しい在庫分析コードを実装するための出発点となります。</span><span class="sxs-lookup"><span data-stu-id="0ac26-179">Together these models provide a great starting point for implementing new inventory dimensions.</span></span> <span data-ttu-id="0ac26-180">サンプル アプリケーションでは、Flavor という新しい製品ディメンションが導入されています。</span><span class="sxs-lookup"><span data-stu-id="0ac26-180">The sample application introduces a new product dimension: Flavor.</span></span> 

<span data-ttu-id="0ac26-181">アプリケーションでは、さまざまなフレーバーの品目の製造、購入、販売などの多くのエンド ツー エンドのビジネス シナリオがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="0ac26-181">The application supports many end-to-end business scenarios, for example creating, buying, and selling items with various flavors.</span></span>

<span data-ttu-id="0ac26-182">必要な場合は、問題を GitHub に直接記録し、追加の補充を提供するサンプル アプリケーションへ自由に投稿してください。</span><span class="sxs-lookup"><span data-stu-id="0ac26-182">If needed, please log issues directly in GitHub, and feel free to contribute to the sample application to provide additional coverage.</span></span>
 
![InventDimensionFlavorScreenshot](media/InventDimensions5.jpg)
