---
title: 分析コード エントリ コントロールの取得
description: 分析コード エントリ コントロールおよび関連するコントローラー クラスについて説明します。
author: robinarh
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 25551
ms.assetid: dbc5c0af-ae97-463e-b5ff-9bfd242529ff
ms.search.region: Global
ms.author: ghenriks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 63f4f64641901988d626272b1f6246200fb39971
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753910"
---
# <a name="uptake-of-dimension-entry-controls"></a><span data-ttu-id="8861f-103">分析コード エントリ コントロールの取得</span><span class="sxs-lookup"><span data-stu-id="8861f-103">Uptake of Dimension Entry controls</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8861f-104">分析コード エントリ コントロールおよび関連するコントローラー クラスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="8861f-104">Describes the Dimension Entry control and associated Controller classes.</span></span>

## <a name="general-approach"></a><span data-ttu-id="8861f-105">一般的なアプローチ</span><span class="sxs-lookup"><span data-stu-id="8861f-105">General approach</span></span>

<span data-ttu-id="8861f-106">設計の目標は、コントロールの実装をカプセル化し、コントロールをサポートするクラスとやり取りするフォームを必要としないことです。</span><span class="sxs-lookup"><span data-stu-id="8861f-106">The design goal is to encapsulate the control implementation and not require the form to interact with the classes backing the control.</span></span> <span data-ttu-id="8861f-107">この設計に合わせて、LedgerDimensionEntryController、LedgerDefaultDimensionEntryController などのように、**すべてのフォームは直接コントローラー クラスではなく、分析コードのエントリ コントロール インスタンス API のみと対話する必要があります**。操作されたプロパティおよびコントローラーで呼び出されたメソッドは、コントロールで呼び出される必要があります。</span><span class="sxs-lookup"><span data-stu-id="8861f-107">In alignment with this design, **all forms should interact only with the Dimension Entry control instance API and not directly with the controller classes**, like LedgerDimensionEntryController, LedgerDefaultDimensionEntryController, etc. Any property that was manipulated or any method that was called on the controller would now need to be called on the control.</span></span>

<span data-ttu-id="8861f-108">**メモ :**</span><span class="sxs-lookup"><span data-stu-id="8861f-108">**Notes:**</span></span>

-   <span data-ttu-id="8861f-109">アップグレード スクリプトは、constructInGroupWithValues() メソッドおよび constructInTabWithValues() メソッドを使用して作成された分析コード エントリ コントロールのみを処理します。</span><span class="sxs-lookup"><span data-stu-id="8861f-109">The upgrade script only handles Dimension Entry controls constructed with the constructInGroupWithValues() and constructInTabWithValues() methods.</span></span> <span data-ttu-id="8861f-110">他のコントロールは、手動でアップグレードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8861f-110">Other controls will need to be upgraded manually.</span></span>
-   <span data-ttu-id="8861f-111">アップグレード スクリプトは、ヘルパー メソッドのパラメーターとして送信された分析コード エントリ コントロールを処理しません。</span><span class="sxs-lookup"><span data-stu-id="8861f-111">The upgrade script will not handle any Dimension Entry controls sent as parameters to helper methods.</span></span> <span data-ttu-id="8861f-112">このコードは、手動でアップグレードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8861f-112">This code will need to be manually upgraded.</span></span>
-   <span data-ttu-id="8861f-113">Dynamics AX 2012 では、既定の分析コード コントロールのコンテナーは、「必要なアクセス許可」 = 手動に設定することでセキュリティ保護可能なコントロールとして定義できました。</span><span class="sxs-lookup"><span data-stu-id="8861f-113">In Dynamics AX 2012, the container for the default dimension control may have been defined as a securable control by setting ‘Needed Permission’ = Manual.</span></span> <span data-ttu-id="8861f-114">コントロールへのアクセスは、セキュリティ モデルで付与されているため、アクセスを正しく表示および管理することができました。</span><span class="sxs-lookup"><span data-stu-id="8861f-114">Access to the control was granted in the security model so view and maintain access worked correctly.</span></span> <span data-ttu-id="8861f-115">既定の分析コードのコントロールは、デザイン時のエクスペリエンスになりました。</span><span class="sxs-lookup"><span data-stu-id="8861f-115">The default dimension control is now a design-time experience.</span></span> <span data-ttu-id="8861f-116">したがって、フォームでは、コントロールのコンテナーを保護可能なコントロールとして定義する必要がなくなりました。</span><span class="sxs-lookup"><span data-stu-id="8861f-116">Therefore forms no longer need to define the container of the control as a securable control.</span></span> <span data-ttu-id="8861f-117">ほとんどの場合、手動の設定を削除するためにメタデータを制御するフォームを更新して、セキュリティ モデルのコントロールへの参照を削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8861f-117">In most cases, forms that control metadata should be updated to remove the Manual setting and the references to the control in the security model need to be removed.</span></span> <span data-ttu-id="8861f-118">Dimension Entry コントロールに対して細かいセキュリティ制御を維持するために使用される場合、この設定は [手動] のままにすることができます。</span><span class="sxs-lookup"><span data-stu-id="8861f-118">The setting can be left as Manual if it is used to maintain fine-grained security control over the Dimension Entry control.</span></span>
-   <span data-ttu-id="8861f-119">Dynamics AX 2012 では、parmAttributeSetDataSource および parmAttributeValueSetDataSource がデータ ソースと既定の分析コード コントロールに関連付けられたデータ ソースのフィールドを設定するために使用されていました。</span><span class="sxs-lookup"><span data-stu-id="8861f-119">In Dynamics AX 2012, parmAttributeSetDataSource and parmAttributeValueSetDataSource were used to set the datasource and datasource field associated with the Default Dimensions control.</span></span>  <span data-ttu-id="8861f-120">これらは通常、DimensionDefaultingController インスタンスを作成した直後にフォームの init メソッドで設定されていました。</span><span class="sxs-lookup"><span data-stu-id="8861f-120">Typically these were set in the init method of the form, immediately after constructing the DimensionDefaultingController instance.</span></span>  <span data-ttu-id="8861f-121">すべての呼び出し parmAttributeSetDataSource および parmAttributeValueSetDataSource はアップグレード後に削除されます。</span><span class="sxs-lookup"><span data-stu-id="8861f-121">All calls to parmAttributeSetDataSource and parmAttributeValueSetDataSource will be removed after upgrade.</span></span>  <span data-ttu-id="8861f-122">これらの呼び出しの値を使用して、アップグレードされたコントロールのメタデータを設定します。</span><span class="sxs-lookup"><span data-stu-id="8861f-122">The values from these calls are used to populate metadata on the upgraded control.</span></span>  <span data-ttu-id="8861f-123">アップグレード後、これらの呼び出しをすべて削除した後、フォームが正常に機能していることを確認するために、フォームをチェックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8861f-123">After upgrade the form should be checked to verify that it is working as expected after the removal of all these calls.</span></span>
-   <span data-ttu-id="8861f-124">ディメンション入力コントロールはフォーム デザインでモデル化されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="8861f-124">Dimension Entry controls are now modelled on form design.</span></span> <span data-ttu-id="8861f-125">分析コードの入力管理を検索するには、デザイン要素を展開するか、フォーム デザインで "DimensionEntry" を検索します。</span><span class="sxs-lookup"><span data-stu-id="8861f-125">To find a Dimension Entry control, expand the design elements or search for “DimensionEntry” on the form design.</span></span> <span data-ttu-id="8861f-126">デザイン時に新しいコントロールがどのようなものかを次に示します。</span><span class="sxs-lookup"><span data-stu-id="8861f-126">Here is what the new control will look like at design time.</span></span>

<span data-ttu-id="8861f-127">[![新しいプロジェクト ダイアログ](./media/1.png)](./media/1.png)</span><span class="sxs-lookup"><span data-stu-id="8861f-127">[![New project dialog](./media/1.png)](./media/1.png)</span></span>

## <a name="properties"></a><span data-ttu-id="8861f-128">プロパティ</span><span class="sxs-lookup"><span data-stu-id="8861f-128">Properties</span></span>
<span data-ttu-id="8861f-129">分析コード エントリ コントロールのカスタム プロパティは、**コントローラー** グループの下にあります。</span><span class="sxs-lookup"><span data-stu-id="8861f-129">The custom properties for the Dimension Entry control are found under the **Controller** group.</span></span>

<span data-ttu-id="8861f-130">[![コントローラーのプロパティ](./media/capture1.png)](./media/capture1.png)</span><span class="sxs-lookup"><span data-stu-id="8861f-130">[![Properties for controller](./media/capture1.png)](./media/capture1.png)</span></span>

#### <a name="details-on-the-properties"></a><span data-ttu-id="8861f-131">プロパティの詳細</span><span class="sxs-lookup"><span data-stu-id="8861f-131">Details on the properties</span></span>

| <span data-ttu-id="8861f-132">プロパティ</span><span class="sxs-lookup"><span data-stu-id="8861f-132">Property</span></span>     | <span data-ttu-id="8861f-133">有効な値</span><span class="sxs-lookup"><span data-stu-id="8861f-133">Valid Values</span></span>            | <span data-ttu-id="8861f-134">用途</span><span class="sxs-lookup"><span data-stu-id="8861f-134">Usage</span></span> |
|------------------|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8861f-135">キャプション テキスト</span><span class="sxs-lookup"><span data-stu-id="8861f-135">Caption Text</span></span>     | <span data-ttu-id="8861f-136">すべてのラベル</span><span class="sxs-lookup"><span data-stu-id="8861f-136">Any label</span></span>                                                                                | <span data-ttu-id="8861f-137">コントロールのキャプション。</span><span class="sxs-lookup"><span data-stu-id="8861f-137">Caption for the control.</span></span>                                                                                                                                           |
| <span data-ttu-id="8861f-138">コントローラー クラス</span><span class="sxs-lookup"><span data-stu-id="8861f-138">Controller Class</span></span> | <span data-ttu-id="8861f-139">8 つのコントローラー クラスのうちの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="8861f-139">One of the 8 Controller classes.</span></span> <span data-ttu-id="8861f-140">たとえば、LedgerDefaultDimensionEntryController</span><span class="sxs-lookup"><span data-stu-id="8861f-140">For example, LedgerDefaultDimensionEntryController</span></span>      | <span data-ttu-id="8861f-141">分析コード エントリ コントロールの動作を決定します。</span><span class="sxs-lookup"><span data-stu-id="8861f-141">Determines the behavior of the Dimension Entry control.</span></span> <span data-ttu-id="8861f-142">このプロパティの詳細については以下で説明します。</span><span class="sxs-lookup"><span data-stu-id="8861f-142">More information about this property is provided below.</span></span>                                                    |
| <span data-ttu-id="8861f-143">データ ソース</span><span class="sxs-lookup"><span data-stu-id="8861f-143">Data Source</span></span>      | <span data-ttu-id="8861f-144">フォーム データ ソース一覧のデータ ソース</span><span class="sxs-lookup"><span data-stu-id="8861f-144">Any data source in the form data source list</span></span>                                             | <span data-ttu-id="8861f-145">ここで指定するデータソースは、値データフィールドプロパティおよび/または列挙データフィールドプロパティで指定したフィールドを保持するテーブルをポイントする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8861f-145">The data source specified here should be pointed to the table that holds the field specified in the Value Data Field property and/or the Enum Data Field property.</span></span> |
| <span data-ttu-id="8861f-146">列挙データ フィールド</span><span class="sxs-lookup"><span data-stu-id="8861f-146">Enum Data Field</span></span>  | <span data-ttu-id="8861f-147">データ ソース プロパティに指定されたデータ ソースによって参照されるテーブルのフィールドです。</span><span class="sxs-lookup"><span data-stu-id="8861f-147">A field in the table referenced by the data source provided in the Data Source property.</span></span> | <span data-ttu-id="8861f-148">これは、列挙型に格納されているフィールドです。</span><span class="sxs-lookup"><span data-stu-id="8861f-148">This is the field that the enumeration values will be stored in.</span></span> <span data-ttu-id="8861f-149">コントロールが列挙を使用していない場合は、このプロパティを指定しないでください。</span><span class="sxs-lookup"><span data-stu-id="8861f-149">This property shouldn’t be specified if the control is not using an enumeration.</span></span>                  |
| <span data-ttu-id="8861f-150">列挙</span><span class="sxs-lookup"><span data-stu-id="8861f-150">Enumeration</span></span>      | <span data-ttu-id="8861f-151">任意の列挙。</span><span class="sxs-lookup"><span data-stu-id="8861f-151">Any enumeration.</span></span> <span data-ttu-id="8861f-152">たとえば、NoYes</span><span class="sxs-lookup"><span data-stu-id="8861f-152">For example, NoYes</span></span>                                                      | <span data-ttu-id="8861f-153">コントロールで使用する列挙型です。</span><span class="sxs-lookup"><span data-stu-id="8861f-153">The enumeration used by the control.</span></span> <span data-ttu-id="8861f-154">列挙型は、分析コード値の代わりにコントロールによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="8861f-154">The enumeration will be used by the control instead of Dimension values.</span></span>                                                      |
| <span data-ttu-id="8861f-155">値 データ フィールド</span><span class="sxs-lookup"><span data-stu-id="8861f-155">Value Data Field</span></span> | <span data-ttu-id="8861f-156">データ ソース プロパティに指定されたデータ ソースによって参照されるテーブルのフィールドです。</span><span class="sxs-lookup"><span data-stu-id="8861f-156">A field in the table referenced by the data source provided in the Data Source property.</span></span> | <span data-ttu-id="8861f-157">これは、分析コード エントリ コントロールがバインドされているフィールドです。</span><span class="sxs-lookup"><span data-stu-id="8861f-157">This is the field that the Dimension Entry control is bound to.</span></span>                                                                                                    |

## <a name="controller-class-property"></a><span data-ttu-id="8861f-158">コントローラー クラス プロパティ</span><span class="sxs-lookup"><span data-stu-id="8861f-158">Controller class property</span></span>
<span data-ttu-id="8861f-159">各コントローラーの詳細は、以下のテーブルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8861f-159">The table provided below gives details about each controller.</span></span>

| <span data-ttu-id="8861f-160">コントローラー</span><span class="sxs-lookup"><span data-stu-id="8861f-160">Controller</span></span>                                 | <span data-ttu-id="8861f-161">細目</span><span class="sxs-lookup"><span data-stu-id="8861f-161">Details</span></span>  |
|------------------------------------------------|------------------|
| <span data-ttu-id="8861f-162">BudgetDefaultDimensionValueSet</span><span class="sxs-lookup"><span data-stu-id="8861f-162">BudgetDefaultDimensionValueSet</span></span>                 | <span data-ttu-id="8861f-163">このコントローラーは、分析コード エントリ コントロールの既定値のデータ入力を、予算ベースでサポートしています。</span><span class="sxs-lookup"><span data-stu-id="8861f-163">This controller provides budget based support for default value data entry in the Dimension Entry control.</span></span> <span data-ttu-id="8861f-164">予算の既定分析コードでは、主勘定分析コードが必要です。</span><span class="sxs-lookup"><span data-stu-id="8861f-164">Budget Default Dimensions require a Main Account Dimension.</span></span>                                                                                                                                                    |
| <span data-ttu-id="8861f-165">PurchReqDefaultDimensionValueSet</span><span class="sxs-lookup"><span data-stu-id="8861f-165">PurchReqDefaultDimensionValueSet</span></span>               | <span data-ttu-id="8861f-166">このコントローラーは、分析コード エントリ コントロールの既定値のデータ入力を、PurchReq ベースでサポートしています。</span><span class="sxs-lookup"><span data-stu-id="8861f-166">This controller provides PurchReq based support for default value data entry in the Dimension Entry control.</span></span> <span data-ttu-id="8861f-167">PurchReq の既定分析コードでは、主勘定分析コードが必要です。</span><span class="sxs-lookup"><span data-stu-id="8861f-167">PurchReq Default Dimensions require a Main Account Dimension.</span></span>                                                                                                                                                |
| <span data-ttu-id="8861f-168">LedgerDefaultDimensionValueSet</span><span class="sxs-lookup"><span data-stu-id="8861f-168">LedgerDefaultDimensionValueSet</span></span>                 | <span data-ttu-id="8861f-169">このコントローラーは、分析コード エントリ コントロールの既定値のデータ入力を、元帳ベースでサポートしています。</span><span class="sxs-lookup"><span data-stu-id="8861f-169">This controller provides ledger based support for default value data entry in the Dimension Entry control.</span></span> <span data-ttu-id="8861f-170">既定の分析コードでは、値が指定されていない行の名前列に「既定値なし」という語句が表示されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="8861f-170">Default Dimensions require the phrase “No default” to appear in the name column of any row that doesn’t have a value specified.</span></span> <span data-ttu-id="8861f-171">このコントローラーは、通常、設定、マスター データ、およびヘッダー レコードで使用します。</span><span class="sxs-lookup"><span data-stu-id="8861f-171">This controller is typically used with setup, master data, and header records.</span></span> |
| <span data-ttu-id="8861f-172">LedgerDimensionValueSet</span><span class="sxs-lookup"><span data-stu-id="8861f-172">LedgerDimensionValueSet</span></span>                        | <span data-ttu-id="8861f-173">このコントローラーは、分析コード エントリ コントロールのデータ入力の元帳に基づくサポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="8861f-173">This controller provides ledger based support for data entry in the Dimension Entry control.</span></span> <span data-ttu-id="8861f-174">このコントローラーは通常、明細行品目またはトランザクション データに使用されます。</span><span class="sxs-lookup"><span data-stu-id="8861f-174">This controller is typically used with line item or transactional data.</span></span>                                                                                                                                                      |
| <span data-ttu-id="8861f-175">InventSiteLockedDimensionValueSet</span><span class="sxs-lookup"><span data-stu-id="8861f-175">InventSiteLockedDimensionValueSet</span></span>              | <span data-ttu-id="8861f-176">このコントローラーは、InventSite フォーム専用の分析コード エントリ コントロールのデータ入力をサポートします。</span><span class="sxs-lookup"><span data-stu-id="8861f-176">This controller provides support for data entry in the Dimension Entry control specifically for the InventSite form.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="8861f-177">InventSiteLinkedDimensionValueSet</span><span class="sxs-lookup"><span data-stu-id="8861f-177">InventSiteLinkedDimensionValueSet</span></span>              | <span data-ttu-id="8861f-178">このコントローラーは、在庫ディメンション リンク設定によって要求される動作の分析コード エントリ コントロールのデータ入力をサポートします。</span><span class="sxs-lookup"><span data-stu-id="8861f-178">This controller provides support for data entry in the Dimension Entry control for the behavior mandated by the Inventory Dimension Link setup.</span></span> <span data-ttu-id="8861f-179">このコントローラーでは、会社が変更されたときに、特別な方法で、コントロールを更新します。</span><span class="sxs-lookup"><span data-stu-id="8861f-179">This controller updates the control in a special way when the company is changed.</span></span>                                                                                         |
| <span data-ttu-id="8861f-180">InventSiteSMAItemDimensionValueSet</span><span class="sxs-lookup"><span data-stu-id="8861f-180">InventSiteSMAItemDimensionValueSet</span></span>             | <span data-ttu-id="8861f-181">このコントローラーは、在庫ディメンション リンク設定によって要求される動作の分析コード エントリ コントロールのデータ入力をサポートします。</span><span class="sxs-lookup"><span data-stu-id="8861f-181">This controller provides support for data entry in the Dimension Entry control for the behavior mandated by the Inventory Dimension Link setup.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="8861f-182">InventSiteTmpLedgerBaseLinkedDimensionValueSet</span><span class="sxs-lookup"><span data-stu-id="8861f-182">InventSiteTmpLedgerBaseLinkedDimensionValueSet</span></span> | <span data-ttu-id="8861f-183">このコントローラーは、在庫ディメンション リンク設定によって要求される動作の分析コード エントリ コントロールのデータ入力をサポートします。</span><span class="sxs-lookup"><span data-stu-id="8861f-183">This controller provides support for data entry in the Dimension Entry control for the behavior mandated by the Inventory Dimension Link setup.</span></span> <span data-ttu-id="8861f-184">このコントローラーは、特に TmpLedgerBase テーブルの DefaultDimension フィールドで動作します。</span><span class="sxs-lookup"><span data-stu-id="8861f-184">This controller specifically works with the DefaultDimension field on the TmpLedgerBase table.</span></span>                                                                            |

<span data-ttu-id="8861f-185">いくつかの分析コード入力コントロールには、コントローラー プロパティが設定されていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8861f-185">Some Dimension Entry controls might not have the controller property set.</span></span> <span data-ttu-id="8861f-186">この場合、コントローラーはコントロールの値データ フィールドの EDT から推測されます。</span><span class="sxs-lookup"><span data-stu-id="8861f-186">The controller is inferred from the EDT of the control’s Value Data Field in these cases.</span></span> <span data-ttu-id="8861f-187">一連の分析コード エントリ コントロールの特定のプロパティを以下に示します。</span><span class="sxs-lookup"><span data-stu-id="8861f-187">A set of Dimension Entry control specific properties is provided below.</span></span> <span data-ttu-id="8861f-188">これらのプロパティは、上記の一般的なアプローチのセクション (DimensionEntryControlHeader) で選択した、分析コード入力コントロールの PurchTable フォームのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="8861f-188">These properties are for the Dimension Entry control selected in the General Approach section above (DimensionEntryControlHeader) on the PurchTable form.</span></span> <span data-ttu-id="8861f-189">この分析コード エントリ コントロールは、PurchTableのTable テーブルの DefaultDimension フィールドを使用しています。</span><span class="sxs-lookup"><span data-stu-id="8861f-189">This Dimension Entry control is using the DefaultDimension field on the PurchTable table.</span></span> <span data-ttu-id="8861f-190">PurchTable の DefaultDimension フィールドの拡張データ型プロパティは、LedgerDefaultDimensionValueSet (以下を参照) に設定されます。</span><span class="sxs-lookup"><span data-stu-id="8861f-190">The Extended Data Type property of the DefaultDimension field on PurchTable is set to LedgerDefaultDimensionValueSet (shown below).</span></span> <span data-ttu-id="8861f-191">実行時に、この EDT は LedgerDefaultDimensionEntryController にマップされます。</span><span class="sxs-lookup"><span data-stu-id="8861f-191">At runtime, this EDT will be mapped to the LedgerDefaultDimensionEntryController.</span></span> <span data-ttu-id="8861f-192">したがって、この場合 DimensionEntryControlHeader コントロールは LedgerDefaultDimensionEntryController を使用します。</span><span class="sxs-lookup"><span data-stu-id="8861f-192">So the DimensionEntryControlHeader control uses the LedgerDefaultDimensionEntryController in this case.</span></span> <span data-ttu-id="8861f-193">次の例は、EDT とそれがマップされているコントローラーを示しています。</span><span class="sxs-lookup"><span data-stu-id="8861f-193">The following example shows the EDTs and the controllers they are mapped to.</span></span>

![新しい品目を追加](./media/3.png)

![リソース ファイルの選択](./media/4.png)

#### <a name="extended-data-types-and-the-controllers-they-are-mapped-to"></a><span data-ttu-id="8861f-196">拡張データ型およびマップされるコントローラー</span><span class="sxs-lookup"><span data-stu-id="8861f-196">Extended data types and the controllers they are mapped to</span></span>

| <span data-ttu-id="8861f-197">拡張データ型</span><span class="sxs-lookup"><span data-stu-id="8861f-197">Extended data type</span></span>                         | <span data-ttu-id="8861f-198">コントローラー</span><span class="sxs-lookup"><span data-stu-id="8861f-198">Controller</span></span>                                        |
|------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="8861f-199">BudgetDefaultDimensionValueSet</span><span class="sxs-lookup"><span data-stu-id="8861f-199">BudgetDefaultDimensionValueSet</span></span>                 | <span data-ttu-id="8861f-200">BudgetDefaultDimensionEntryController</span><span class="sxs-lookup"><span data-stu-id="8861f-200">BudgetDefaultDimensionEntryController</span></span>                 |
| <span data-ttu-id="8861f-201">PurchReqDefaultDimensionValueSet</span><span class="sxs-lookup"><span data-stu-id="8861f-201">PurchReqDefaultDimensionValueSet</span></span>               | <span data-ttu-id="8861f-202">PurchReqDefaultDimensionEntryController</span><span class="sxs-lookup"><span data-stu-id="8861f-202">PurchReqDefaultDimensionEntryController</span></span>               |
| <span data-ttu-id="8861f-203">LedgerDefaultDimensionValueSet</span><span class="sxs-lookup"><span data-stu-id="8861f-203">LedgerDefaultDimensionValueSet</span></span>                 | <span data-ttu-id="8861f-204">LedgerDefaultDimensionEntryController</span><span class="sxs-lookup"><span data-stu-id="8861f-204">LedgerDefaultDimensionEntryController</span></span>                 |
| <span data-ttu-id="8861f-205">LedgerDimensionValueSet</span><span class="sxs-lookup"><span data-stu-id="8861f-205">LedgerDimensionValueSet</span></span>                        | <span data-ttu-id="8861f-206">LedgerDimensionEntryController</span><span class="sxs-lookup"><span data-stu-id="8861f-206">LedgerDimensionEntryController</span></span>                        |
| <span data-ttu-id="8861f-207">InventSiteLockedDimensionValueSet</span><span class="sxs-lookup"><span data-stu-id="8861f-207">InventSiteLockedDimensionValueSet</span></span>              | <span data-ttu-id="8861f-208">InventSiteLockedDimensionEntryController</span><span class="sxs-lookup"><span data-stu-id="8861f-208">InventSiteLockedDimensionEntryController</span></span>              |
| <span data-ttu-id="8861f-209">InventSiteLinkedDimensionValueSet</span><span class="sxs-lookup"><span data-stu-id="8861f-209">InventSiteLinkedDimensionValueSet</span></span>              | <span data-ttu-id="8861f-210">InventSiteLinkedDimensionEntryController</span><span class="sxs-lookup"><span data-stu-id="8861f-210">InventSiteLinkedDimensionEntryController</span></span>              |
| <span data-ttu-id="8861f-211">InventSiteSMAItemDimensionValueSet</span><span class="sxs-lookup"><span data-stu-id="8861f-211">InventSiteSMAItemDimensionValueSet</span></span>             | <span data-ttu-id="8861f-212">InventSiteSMAItemDimensionEntryController</span><span class="sxs-lookup"><span data-stu-id="8861f-212">InventSiteSMAItemDimensionEntryController</span></span>             |
| <span data-ttu-id="8861f-213">InventSiteTmpLedgerBaseLinkedDimensionValueSet</span><span class="sxs-lookup"><span data-stu-id="8861f-213">InventSiteTmpLedgerBaseLinkedDimensionValueSet</span></span> | <span data-ttu-id="8861f-214">InventSiteTmpLedgerBaseLinked-</span><span class="sxs-lookup"><span data-stu-id="8861f-214">InventSiteTmpLedgerBaseLinked-</span></span><br><span data-ttu-id="8861f-215">DimensionEntryController</span><span class="sxs-lookup"><span data-stu-id="8861f-215">DimensionEntryController</span></span> |

## <a name="upgrade-script-todos"></a><span data-ttu-id="8861f-216">スクリプト TODO のアップグレード</span><span class="sxs-lookup"><span data-stu-id="8861f-216">Upgrade Script TODOs</span></span>
### <a name="dynamics-ax-2012"></a><span data-ttu-id="8861f-217">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="8861f-217">Dynamics AX 2012</span></span>

```xpp
/* TODO: (Code Upgrade) [Dimension entry control]
Replace this based on the migration guidance. */
DimensionEntryControl.reactivate();
```

### <a name="finance-and-operations"></a><span data-ttu-id="8861f-218">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8861f-218">Finance and Operations</span></span>
<span data-ttu-id="8861f-219">reactivate メソッドは、分析コード エントリ コントロールを現在の設定でリフレッシュします。</span><span class="sxs-lookup"><span data-stu-id="8861f-219">The reactivate method refreshes the Dimension Entry control with current settings.</span></span> <span data-ttu-id="8861f-220">このメソッドは、会社または表示された分析コード リストが変更された場合にのみ、コントロールを更新します。</span><span class="sxs-lookup"><span data-stu-id="8861f-220">The method only refreshes the control if the company or displayed dimension list changes.</span></span> <span data-ttu-id="8861f-221">この呼び出しは、これらのどちらも以前に変更されていない場合に削除できます。</span><span class="sxs-lookup"><span data-stu-id="8861f-221">This call can be removed if neither of these are changed before it.</span></span> <span data-ttu-id="8861f-222">それ以外の場合は、呼び出しはそのままにします。</span><span class="sxs-lookup"><span data-stu-id="8861f-222">Otherwise leave the call as is.</span></span> <span data-ttu-id="8861f-223">reactivate() の直前で parmCompany() が呼び出され、それが reactivate() より前に呼び出された唯一の DEC API であり、そのメソッドがデータソースの active() 中に呼び出された場合、最適化を手動で行うことでパフォーマンスを向上させ、コードの取り込みを削減することができます。</span><span class="sxs-lookup"><span data-stu-id="8861f-223">If parmCompany() is called immediately before reactivate(), and it is the only DEC API called before reactivate(), and the method it resides in is called during the active() of the datasource, then an optimization can be manually made to improve performance and reduce code uptake:</span></span>

1. <span data-ttu-id="8861f-224"> データ ソースのアクティブ プロセス中に、parmCompany() および reactivate() 呼び出しを削除します。</span><span class="sxs-lookup"><span data-stu-id="8861f-224">Remove the parmCompany() and reactivate() calls during the datasource active process.</span></span>
2. <span data-ttu-id="8861f-225"> 最初のユーザーとフォームとのやりとりの前に呼び出されるフォーム init()、run()、datasource init()、または同様のメソッドでは、次のコード行を追加します。</span><span class="sxs-lookup"><span data-stu-id="8861f-225">In the form init(), run(), datasource init(), or similar methods called before initial user interaction with the form, add the following line of code:</span></span>

    ```xpp
    DimensionEntryControl.parmCompanyReference(
        fieldStr([myTable], [myCompanyContextField]);
    ```

    <span data-ttu-id="8861f-226">この変更により、DEC はアクティブなレコードが変更されたときに更新される会社フィールド参照を自動的に見つけ出し、それに応じてディメンションのリストを更新できます。</span><span class="sxs-lookup"><span data-stu-id="8861f-226">This change will allow the DEC to automatically find the company field reference that is updated when the active record changes and refresh the list of dimensions accordingly.</span></span>

> [!NOTE]
> <span data-ttu-id="8861f-227">これを parmDisplayedDimensionSet() の使用と組み合わせないでください。そうすると、分析コードの一覧が想定外のものになることがあります。</span><span class="sxs-lookup"><span data-stu-id="8861f-227">This should not be combined with the use of parmDisplayedDimensionSet() otherwise the list of dimensions may not be the ones expected.</span></span> <span data-ttu-id="8861f-228">会社の選択フィールドの変更されたメソッドなど、他のすべての場所で、データ ソースがその時点で読み取られるプロセスではないため、会社内の変更をすぐに反映するように parmCompany() を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="8861f-228">In all other locations, such as the modified method of a company selection field, parmCompany() must be called to immediately reflect the change in company as the datasource is not in the process of being read at that time.</span></span>

### <a name="dynamics-ax-2012"></a><span data-ttu-id="8861f-229">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="8861f-229">Dynamics AX 2012</span></span>

```xpp
/* TODO: (Code Upgrade) [Dimension entry control]
Replace this based on the migration guidance. */
DimensionEntryControl.setEditability(true, 0);
```


### <a name="finance-and-operations"></a><span data-ttu-id="8861f-230">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8861f-230">Finance and Operations</span></span>
<span data-ttu-id="8861f-231">特定の編集可能なディメンション セットが必要な場合は、この呼び出しを次のように置き換えます。</span><span class="sxs-lookup"><span data-stu-id="8861f-231">If a specific editable dimension set is needed, replace this call with:</span></span>

```xpp
DimensionEntryControl.parmEditableDimensionSet(
    editableDimensionSet);
```

> [!NOTE]
> <span data-ttu-id="8861f-232">editableDimensionSet パラメーターのタイプは、 DimensionEnumeration です。</span><span class="sxs-lookup"><span data-stu-id="8861f-232">The editableDimensionSet parameter is of type DimensionEnumeration.</span></span>

### <a name="dynamics-ax-2012"></a><span data-ttu-id="8861f-233">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="8861f-233">Dynamics AX 2012</span></span>

```xpp
/* TODO: (Code Upgrade) [Dimension entry control]
This method can be removed if there is
no custom implementation */
// dimensionDefaultingController.pageActivated();
```

### <a name="finance-and-operations"></a><span data-ttu-id="8861f-234">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8861f-234">Finance and Operations</span></span>
<span data-ttu-id="8861f-235">このコールを、分析コード エントリ コントロールの親コントロールの pageActivated メソッドまたは Form Init メソッド内で実行する場合、削除することができます。</span><span class="sxs-lookup"><span data-stu-id="8861f-235">If this call is made within the pageActivated method of the Dimension Entry control’s parent control or the form init method, it can be removed.</span></span> <span data-ttu-id="8861f-236">上記の場所以外のメソッド呼び出しの意図は明確ではありません。</span><span class="sxs-lookup"><span data-stu-id="8861f-236">The intent of this method call outside the above mentioned locations isn’t clear.</span></span> <span data-ttu-id="8861f-237">呼び出しを削除して、コントロールをテストします。</span><span class="sxs-lookup"><span data-stu-id="8861f-237">Remove the call and test the control.</span></span>

### <a name="dynamics-ax-2012"></a><span data-ttu-id="8861f-238">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="8861f-238">Dynamics AX 2012</span></span>

```xpp
/* TODO: (Code Upgrade) [Dimension entry control]
Replace this based on the migration guidance. */
DimensionEntryControl.deleted();
```

### <a name="finance-and-operations"></a><span data-ttu-id="8861f-239">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8861f-239">Finance and Operations</span></span>
<span data-ttu-id="8861f-240">データ ソースの削除メソッド内にはない deleted() の呼び出しのために、TODO が残されます。</span><span class="sxs-lookup"><span data-stu-id="8861f-240">A TODO will be left for a call to deleted() that is not inside a data source delete method.</span></span> <span data-ttu-id="8861f-241">これらの呼び出しは、データソースの削除メソッド内にのみ存在すると予想され、置換はありません。</span><span class="sxs-lookup"><span data-stu-id="8861f-241">These calls are only expected to be in data source delete methods, and there is no replacement.</span></span> <span data-ttu-id="8861f-242">呼び出しを削除して、コントロールをテストしてみてください。</span><span class="sxs-lookup"><span data-stu-id="8861f-242">Try to remove the call and test the control.</span></span>

### <a name="dynamics-ax-2012"></a><span data-ttu-id="8861f-243">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="8861f-243">Dynamics AX 2012</span></span>

```xpp
/* TODO: (Code Upgrade) [Dimension entry control]
Replace this based on the migration guidance. */
// dimensionDefaultingController.writing();
```

### <a name="finance-and-operations"></a><span data-ttu-id="8861f-244">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8861f-244">Finance and Operations</span></span>
<span data-ttu-id="8861f-245">分析コード エントリ コントロール フレームワークは、値を保存します。</span><span class="sxs-lookup"><span data-stu-id="8861f-245">The Dimension Entry control framework will save values.</span></span> <span data-ttu-id="8861f-246">呼び出しを削除して、コントロールをテストします。</span><span class="sxs-lookup"><span data-stu-id="8861f-246">Remove the call and test the control.</span></span>

### <a name="dynamics-ax-2012"></a><span data-ttu-id="8861f-247">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="8861f-247">Dynamics AX 2012</span></span>

```xpp
/* TODO: (Code Upgrade) [Dimension entry control]
Replace this based on the migration guidance. */
dimensionDefaultingController::findBackingEntityInstance();
```

### <a name="finance-and-operations"></a><span data-ttu-id="8861f-248">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8861f-248">Finance and Operations</span></span>
<span data-ttu-id="8861f-249">エンティティを検索するには、getEntityInstance メソッドを DimensionAttributeValue から呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="8861f-249">To find the entity, the getEntityInstance method needs to be called from the DimensionAttributeValue.</span></span> <span data-ttu-id="8861f-250">この呼び出しを次のようなものに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="8861f-250">Replace this call with something similar to the following:</span></span>

```xpp
DimensionAttributeValue dimAttrValue =
    DimensionAttributeValue::
        findByDimensionAttributeAndValueNoError(
            dimensionAttributeTable, dimensionValue);
if (dimAttrValue) {
    common = dimAttrValue.getEntityInstance();
}
```

### <a name="dynamics-ax-2012"></a><span data-ttu-id="8861f-251">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="8861f-251">Dynamics AX 2012</span></span>

```xpp
/* TODO: (Code Upgrade) [Dimension entry control]
Replace this based on the migration guidance. */
DimensionEntryControlHeader.updateValues(NoYesUnchanged::Yes);
```

### <a name="finance-and-operations"></a><span data-ttu-id="8861f-252">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8861f-252">Finance and Operations</span></span>
<span data-ttu-id="8861f-253">ここに 1 つのパラメーターがある場合のみ updateValues() メソッドが呼び出されるため、呼び出しは allowEdit() の呼び出しに置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="8861f-253">Since the updateValues() method is only called with one parameter here, the call can be replaced with a call to allowEdit().</span></span>

```xpp
DimensionEntryControlHeader.allowEdit(
    NoYesUnchanged::Yes);
```

### <a name="dynamics-ax-2012"></a><span data-ttu-id="8861f-254">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="8861f-254">Dynamics AX 2012</span></span>

```xpp
/* TODO: (Code Upgrade) [Dimension entry control]
Replace this based on the migration guidance. */
DimensionEntryControlHeader.updateValues(
    NoYesUnchanged::No, true);
```

### <a name="finance-and-operations"></a><span data-ttu-id="8861f-255">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8861f-255">Finance and Operations</span></span>
<span data-ttu-id="8861f-256">この場合、updateValues() の呼び出しには 2 つのパラメーターがあるので、コントロールの編集機能を変更するには allowEdit() の呼び出しと置き換え、コントロールの値をクリアするには loadAttributeValueSet() の呼び出しと置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="8861f-256">Since the call to updateValues() has two parameters in this case, it needs to be replaced with a call to allowEdit() to change the editability of the control and a call to loadAttributeValueSet() to clear the control’s values.</span></span>

```xpp
DimensionEntryControlHeader.allowEdit(
    NoYesUnchanged::No);
DimensionEntryControlHeader.loadAttributeValueSet(0);
```

> [!NOTE]
> <span data-ttu-id="8861f-257">updateValues メソッド 呼び出しの最初の パラメーター が NoYesUnchangedUnchanged::の場合は、allowEdit の新しい呼び出しは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="8861f-257">If the first parameter in the updateValues method call was NoYesUnchanged::Unchanged, then the new call to allowEdit is not needed.</span></span> <span data-ttu-id="8861f-258">同様に、updateValues メソッドの 2 番目のパラメーターの呼び出しが false の場合、loadAttributeValueSet への呼び出しは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="8861f-258">Similarly, if the second parameter in the updateValues method call was false, then the call to loadAttributeValueSet is not needed.</span></span>

## <a name="methods-to-potentially-remove"></a><span data-ttu-id="8861f-259">削除する可能性のあるメソッド</span><span class="sxs-lookup"><span data-stu-id="8861f-259">Methods to potentially remove</span></span>
<span data-ttu-id="8861f-260">分析コード エントリ コントロールを保持するデータソースまたは tabpage/グループの残りのメソッドは、カスタム ロジックがない場合、削除することができます。</span><span class="sxs-lookup"><span data-stu-id="8861f-260">Any leftover methods on the datasource or tabpage/group that holds the Dimension Entry control can be removed if there is no custom logic.</span></span> <span data-ttu-id="8861f-261">次のテーブルは、削除する必要があるカスタマイズのないメソッドの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="8861f-261">The following table shows examples of methods without customizations which should be deleted.</span></span>

### <a name="dynamics-ax-2012"></a><span data-ttu-id="8861f-262">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="8861f-262">Dynamics AX 2012</span></span>

```xpp
public int active(){int ret;ret = super();return ret;}
```

### <a name="finance-and-operations"></a><span data-ttu-id="8861f-263">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8861f-263">Finance and Operations</span></span>
<span data-ttu-id="8861f-264">このメソッドはデータソースにあります。</span><span class="sxs-lookup"><span data-stu-id="8861f-264">This method will be on the data source.</span></span> <span data-ttu-id="8861f-265">カスタム ロジックがない場合に削除することができます。</span><span class="sxs-lookup"><span data-stu-id="8861f-265">It can be removed if there is no custom logic.</span></span>

### <a name="dynamics-ax-2012"></a><span data-ttu-id="8861f-266">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="8861f-266">Dynamics AX 2012</span></span>

```xpp
public void delete(){super();}
```

### <a name="finance-and-operations"></a><span data-ttu-id="8861f-267">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8861f-267">Finance and Operations</span></span>
<span data-ttu-id="8861f-268">このメソッドはデータソースにあります。</span><span class="sxs-lookup"><span data-stu-id="8861f-268">This method will be on the data source.</span></span> <span data-ttu-id="8861f-269">カスタム ロジックがない場合に削除することができます。</span><span class="sxs-lookup"><span data-stu-id="8861f-269">It can be removed if there is no custom logic.</span></span>

### <a name="dynamics-ax-2012"></a><span data-ttu-id="8861f-270">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="8861f-270">Dynamics AX 2012</span></span>

```xpp
public void deleted(){super();}
```

### <a name="finance-and-operations"></a><span data-ttu-id="8861f-271">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8861f-271">Finance and Operations</span></span>
<span data-ttu-id="8861f-272">このメソッドはデータソースにあります。</span><span class="sxs-lookup"><span data-stu-id="8861f-272">This method will be on the data source.</span></span> <span data-ttu-id="8861f-273">カスタム ロジックがない場合に削除することができます。</span><span class="sxs-lookup"><span data-stu-id="8861f-273">It can be removed if there is no custom logic.</span></span>

### <a name="dynamics-ax-2012"></a><span data-ttu-id="8861f-274">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="8861f-274">Dynamics AX 2012</span></span>

```xpp
public void deleting(){super();}
```

### <a name="finance-and-operations"></a><span data-ttu-id="8861f-275">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8861f-275">Finance and Operations</span></span>
<span data-ttu-id="8861f-276">このメソッドはデータソースにあります。</span><span class="sxs-lookup"><span data-stu-id="8861f-276">This method will be on the data source.</span></span> <span data-ttu-id="8861f-277">カスタム ロジックがない場合に削除することができます。</span><span class="sxs-lookup"><span data-stu-id="8861f-277">It can be removed if there is no custom logic.</span></span>

### <a name="dynamics-ax-2012"></a><span data-ttu-id="8861f-278">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="8861f-278">Dynamics AX 2012</span></span>

```xpp
public boolean validateDelete(){boolean ret;ret = super();return ret;}
```

### <a name="finance-and-operations"></a><span data-ttu-id="8861f-279">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8861f-279">Finance and Operations</span></span>
<span data-ttu-id="8861f-280">このメソッドはデータソースにあります。</span><span class="sxs-lookup"><span data-stu-id="8861f-280">This method will be on the data source.</span></span> <span data-ttu-id="8861f-281">カスタム ロジックがない場合に削除することができます。</span><span class="sxs-lookup"><span data-stu-id="8861f-281">It can be removed if there is no custom logic.</span></span>

### <a name="dynamics-ax-2012"></a><span data-ttu-id="8861f-282">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="8861f-282">Dynamics AX 2012</span></span>

```xpp
public void write(){super();}
```

### <a name="finance-and-operations"></a><span data-ttu-id="8861f-283">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8861f-283">Finance and Operations</span></span>
<span data-ttu-id="8861f-284">このメソッドはデータソースにあります。</span><span class="sxs-lookup"><span data-stu-id="8861f-284">This method will be on the data source.</span></span> <span data-ttu-id="8861f-285">カスタム ロジックがない場合に削除することができます。</span><span class="sxs-lookup"><span data-stu-id="8861f-285">It can be removed if there is no custom logic.</span></span>

### <a name="dynamics-ax-2012"></a><span data-ttu-id="8861f-286">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="8861f-286">Dynamics AX 2012</span></span>

```xpp
public void writing(){super();}
```

### <a name="finance-and-operations"></a><span data-ttu-id="8861f-287">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8861f-287">Finance and Operations</span></span>
<span data-ttu-id="8861f-288">このメソッドはデータソースにあります。</span><span class="sxs-lookup"><span data-stu-id="8861f-288">This method will be on the data source.</span></span> <span data-ttu-id="8861f-289">カスタム ロジックがない場合に削除することができます。</span><span class="sxs-lookup"><span data-stu-id="8861f-289">It can be removed if there is no custom logic.</span></span>

### <a name="dynamics-ax-2012"></a><span data-ttu-id="8861f-290">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="8861f-290">Dynamics AX 2012</span></span>

```xpp
public void written(){super();}
```

### <a name="finance-and-operations"></a><span data-ttu-id="8861f-291">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8861f-291">Finance and Operations</span></span>
<span data-ttu-id="8861f-292">このメソッドはデータソースにあります。</span><span class="sxs-lookup"><span data-stu-id="8861f-292">This method will be on the data source.</span></span> <span data-ttu-id="8861f-293">カスタム ロジックがない場合に削除することができます。</span><span class="sxs-lookup"><span data-stu-id="8861f-293">It can be removed if there is no custom logic.</span></span>

### <a name="dynamics-ax-2012"></a><span data-ttu-id="8861f-294">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="8861f-294">Dynamics AX 2012</span></span>

```xpp
public boolean validateWrite(){boolean ret;ret = super();return ret;}
```

### <a name="finance-and-operations"></a><span data-ttu-id="8861f-295">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8861f-295">Finance and Operations</span></span>
<span data-ttu-id="8861f-296">このメソッドはデータソースにあります。</span><span class="sxs-lookup"><span data-stu-id="8861f-296">This method will be on the data source.</span></span> <span data-ttu-id="8861f-297">カスタム ロジックがない場合に削除することができます。</span><span class="sxs-lookup"><span data-stu-id="8861f-297">It can be removed if there is no custom logic.</span></span>

### <a name="dynamics-ax-2012"></a><span data-ttu-id="8861f-298">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="8861f-298">Dynamics AX 2012</span></span>

```xpp
public void pageActivated()
{
    super();
    /* TODO: (Code Upgrade) [Dimension entry control] This method can be removed if
    there is no custom implementation */
    // dimensionDefaultingController.pageActivated();
}
```

### <a name="finance-and-operations"></a><span data-ttu-id="8861f-299">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8861f-299">Finance and Operations</span></span>
<span data-ttu-id="8861f-300">この方法は分析コード エントリ コントロールを保持する TabPage またはグループになります。</span><span class="sxs-lookup"><span data-stu-id="8861f-300">This method will be on the tabpage or group that holds the Dimension Entry control.</span></span> <span data-ttu-id="8861f-301">カスタム ロジックがない場合は、メソッドを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="8861f-301">If there is no custom logic, the method can be deleted.</span></span>

## <a name="compile-errors"></a><span data-ttu-id="8861f-302">コンパイル エラー</span><span class="sxs-lookup"><span data-stu-id="8861f-302">Compile Errors</span></span>
<span data-ttu-id="8861f-303">このセクションでは、取り残される可能性のある一般的なコンパイル エラーに対処する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8861f-303">This section will go through how to address common compile errors that may be left behind.</span></span>


### <a name="dynamics-ax-2012"></a><span data-ttu-id="8861f-304">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="8861f-304">Dynamics AX 2012</span></span>

<span data-ttu-id="8861f-305"><strong>フォームで (PurchTable)。</strong></span><span class="sxs-lookup"><span data-stu-id="8861f-305"><strong>On the form (PurchTable):</strong></span></span>

```xpp
purchTableForm.parmDimensionDefaultingControllerHeader(
    dimensionDefaultingControllerHeader);
```

<span data-ttu-id="8861f-306"><strong>クラス内 (PurchTableForm):</strong></span><span class="sxs-lookup"><span data-stu-id="8861f-306"><strong>In the class (PurchTableForm):</strong></span></span>

```xpp
public DimensionDefaultingController
parmDimensionDefaultingControllerHeader(
    DimensionDefaultingController
        _dimensionDefaultingControllerHeader =
        dimensionDefaultingControllerHeader)
{
   dimensionDefaultingControllerHeader =
       _dimensionDefaultingControllerHeader;
   return dimensionDefaultingControllerHeader;
}
```

### <a name="finance-and-operations"></a><span data-ttu-id="8861f-307">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8861f-307">Finance and Operations</span></span>

<span data-ttu-id="8861f-308"><strong>フォームで (PurchTable)。</strong></span><span class="sxs-lookup"><span data-stu-id="8861f-308"><strong>On the form (PurchTable):</strong></span></span>

```xpp
purchTableForm.parmDimensionEntryControlHeader(
    DimensionEntryControlHeader);
```

<span data-ttu-id="8861f-309"><strong>クラス内 (PurchTableForm):</strong></span><span class="sxs-lookup"><span data-stu-id="8861f-309"><strong>In the class (PurchTableForm):</strong></span></span>

```xpp
public DimensionEntryControl
parmDimensionEntryControlHeader(
    DimensionEntryControl
       _dimensionEntryControlHeader =
       dimensionEntryControlHeader)

{
    dimensionEntryControlHeader =
        _dimensionEntryControlHeader;
    return dimensionEntryControlHeader;
}
```


## <a name="additional-resources"></a><span data-ttu-id="8861f-310">追加リソース</span><span class="sxs-lookup"><span data-stu-id="8861f-310">Additional resources</span></span>

[<span data-ttu-id="8861f-311">既定の分析コード コントロールの分析コード エントリ コントロールへの移行</span><span class="sxs-lookup"><span data-stu-id="8861f-311">Migrate default dimensions controls to Dimension Entry controls</span></span>](dimension-entry-control-migration.md)

[<span data-ttu-id="8861f-312">ダイアログの分析コード エントリ コントロールのサポート</span><span class="sxs-lookup"><span data-stu-id="8861f-312">Support for Dimension Entry controls on dialogs</span></span>](dimension-entry-control-dialog-support.md)




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]