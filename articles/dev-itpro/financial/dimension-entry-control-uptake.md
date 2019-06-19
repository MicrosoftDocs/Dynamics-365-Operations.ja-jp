---
title: 分析コード エントリ コントロールの取得
description: 分析コード エントリ コントロールおよび関連するコントローラー クラスについて説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 25551
ms.assetid: dbc5c0af-ae97-463e-b5ff-9bfd242529ff
ms.search.region: Global
ms.author: ghenriks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 37c412a65a774b239cc23f91f3516712ddaa1b50
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555612"
---
# <a name="uptake-of-dimension-entry-controls"></a><span data-ttu-id="5aa8e-103">分析コード エントリ コントロールの取得</span><span class="sxs-lookup"><span data-stu-id="5aa8e-103">Uptake of Dimension Entry controls</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5aa8e-104">分析コード エントリ コントロールおよび関連するコントローラー クラスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-104">Describes the Dimension Entry control and associated Controller classes.</span></span>

<a name="general-approach"></a><span data-ttu-id="5aa8e-105">一般的なアプローチ</span><span class="sxs-lookup"><span data-stu-id="5aa8e-105">General approach</span></span>
----------------

<span data-ttu-id="5aa8e-106">設計の目標は、コントロールの実装をカプセル化し、コントロールをサポートするクラスとやり取りするフォームを必要としないことです。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-106">The design goal is to encapsulate the control implementation and not require the form to interact with the classes backing the control.</span></span> <span data-ttu-id="5aa8e-107">この設計に合わせて、LedgerDimensionEntryController、LedgerDefaultDimensionEntryController などのように、**すべてのフォームは直接コントローラー クラスではなく、分析コードのエントリ コントロール インスタンス API のみと対話する必要があります**。操作されたプロパティおよびコントローラーで呼び出されたメソッドは、コントロールで呼び出される必要があります。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-107">In alignment with this design, **all forms should interact only with the Dimension Entry control instance API and not directly with the controller classes**, like LedgerDimensionEntryController, LedgerDefaultDimensionEntryController, etc. Any property that was manipulated or any method that was called on the controller would now need to be called on the control.</span></span> <span data-ttu-id="5aa8e-108">**注記:**</span><span class="sxs-lookup"><span data-stu-id="5aa8e-108">**Note:**</span></span>

-   <span data-ttu-id="5aa8e-109">アップグレード スクリプトは、constructInGroupWithValues() メソッドおよび constructInTabWithValues() メソッドを使用して作成された分析コード エントリ コントロールのみを処理します。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-109">The upgrade script only handles Dimension Entry controls constructed with the constructInGroupWithValues() and constructInTabWithValues() methods.</span></span> <span data-ttu-id="5aa8e-110">他のコントロールは、手動でアップグレードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-110">Other controls will need to be upgraded manually.</span></span>
-   <span data-ttu-id="5aa8e-111">アップグレード スクリプトは、ヘルパー メソッドのパラメーターとして送信された分析コード エントリ コントロールを処理しません。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-111">The upgrade script will not handle any Dimension Entry controls sent as parameters to helper methods.</span></span> <span data-ttu-id="5aa8e-112">このコードは、手動でアップグレードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-112">This code will need to be manually upgraded.</span></span>
-   <span data-ttu-id="5aa8e-113">Dynamics AX 2012 では、既定の分析コード コントロールのコンテナーは、「必要なアクセス許可」 = 手動に設定することでセキュリティ保護可能なコントロールとして定義できました。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-113">In Dynamics AX 2012, the container for the default dimension control may have been defined as a securable control by setting ‘Needed Permission’ = Manual.</span></span> <span data-ttu-id="5aa8e-114">コントロールへのアクセスは、セキュリティ モデルで付与されているため、アクセスを正しく表示および管理することができました。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-114">Access to the control was granted in the security model so view and maintain access worked correctly.</span></span> <span data-ttu-id="5aa8e-115">既定の分析コードのコントロールは、デザイン時のエクスペリエンスになりました。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-115">The default dimension control is now a design-time experience.</span></span> <span data-ttu-id="5aa8e-116">したがって、フォームでは、コントロールのコンテナーを保護可能なコントロールとして定義する必要がなくなりました。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-116">Therefore forms no longer need to define the container of the control as a securable control.</span></span> <span data-ttu-id="5aa8e-117">ほとんどの場合、手動の設定を削除するためにメタデータを制御するフォームを更新して、セキュリティ モデルのコントロールへの参照を削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-117">In most cases, forms that control metadata should be updated to remove the Manual setting and the references to the control in the security model need to be removed.</span></span> <span data-ttu-id="5aa8e-118">Dimension Entry コントロールに対して細かいセキュリティ制御を維持するために使用される場合、この設定は [手動] のままにすることができます。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-118">The setting can be left as Manual if it is used to maintain fine-grained security control over the Dimension Entry control.</span></span>
-   <span data-ttu-id="5aa8e-119">Dynamics AX 2012 では、parmAttributeSetDataSource および parmAttributeValueSetDataSource がデータ ソースと既定の分析コード コントロールに関連付けられたデータ ソースのフィールドを設定するために使用されていました。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-119">In Dynamics AX 2012, parmAttributeSetDataSource and parmAttributeValueSetDataSource were used to set the datasource and datasource field associated with the Default Dimensions control.</span></span>  <span data-ttu-id="5aa8e-120">これらは通常、DimensionDefaultingController インスタンスを作成した直後にフォームの init メソッドで設定されていました。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-120">Typically these were set in the init method of the form, immediately after constructing the DimensionDefaultingController instance.</span></span>  <span data-ttu-id="5aa8e-121">すべての呼び出し parmAttributeSetDataSource および parmAttributeValueSetDataSource はアップグレード後に削除されます。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-121">All calls to parmAttributeSetDataSource and parmAttributeValueSetDataSource will be removed after upgrade.</span></span>  <span data-ttu-id="5aa8e-122">これらの呼び出しの値を使用して、アップグレードされたコントロールのメタデータを設定します。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-122">The values from these calls are used to populate metadata on the upgraded control.</span></span>  <span data-ttu-id="5aa8e-123">アップグレード後、これらの呼び出しをすべて削除した後、フォームが正常に機能していることを確認するために、フォームをチェックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-123">After upgrade the form should be checked to verify that it is working as expected after the removal of all these calls.</span></span>
-   <span data-ttu-id="5aa8e-124">ディメンション入力コントロールはフォーム デザインでモデル化されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-124">Dimension Entry controls are now modelled on form design.</span></span> <span data-ttu-id="5aa8e-125">分析コードの入力管理を検索するには、デザイン要素を展開するか、フォーム デザインで "DimensionEntry" を検索します。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-125">To find a Dimension Entry control, expand the design elements or search for “DimensionEntry” on the form design.</span></span> <span data-ttu-id="5aa8e-126">デザイン時に新しいコントロールがどのようなものかを次に示します。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-126">Here is what the new control will look like at design time.</span></span>

<span data-ttu-id="5aa8e-127">[![1](./media/1.png)](./media/1.png)</span><span class="sxs-lookup"><span data-stu-id="5aa8e-127">[![1](./media/1.png)](./media/1.png)</span></span>

## <a name="properties"></a><span data-ttu-id="5aa8e-128">プロパティ</span><span class="sxs-lookup"><span data-stu-id="5aa8e-128">Properties</span></span>
<span data-ttu-id="5aa8e-129">分析コード エントリ コントロールのカスタム プロパティは、**コントローラー** グループの下にあります。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-129">The custom properties for the Dimension Entry control are found under the **Controller** group.</span></span> <span data-ttu-id="5aa8e-130">[![Capture1](./media/capture1.png)](./media/capture1.png)</span><span class="sxs-lookup"><span data-stu-id="5aa8e-130">[![Capture1](./media/capture1.png)](./media/capture1.png)</span></span>

#### <a name="details-on-the-properties"></a><span data-ttu-id="5aa8e-131">プロパティの詳細</span><span class="sxs-lookup"><span data-stu-id="5aa8e-131">Details on the properties</span></span>

|                  |                                                                                          |                                                                                                                                                                    |
|------------------|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5aa8e-132">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="5aa8e-132">**Property**</span></span>     | <span data-ttu-id="5aa8e-133">**有効な値**</span><span class="sxs-lookup"><span data-stu-id="5aa8e-133">**Valid Values**</span></span>                                                                         | <span data-ttu-id="5aa8e-134">**用途**</span><span class="sxs-lookup"><span data-stu-id="5aa8e-134">**Usage**</span></span>                                                                                                                                                          |
| <span data-ttu-id="5aa8e-135">キャプション テキスト</span><span class="sxs-lookup"><span data-stu-id="5aa8e-135">Caption Text</span></span>     | <span data-ttu-id="5aa8e-136">すべてのラベル</span><span class="sxs-lookup"><span data-stu-id="5aa8e-136">Any label</span></span>                                                                                | <span data-ttu-id="5aa8e-137">コントロールのキャプション。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-137">Caption for the control.</span></span>                                                                                                                                           |
| <span data-ttu-id="5aa8e-138">コントローラー クラス</span><span class="sxs-lookup"><span data-stu-id="5aa8e-138">Controller Class</span></span> | <span data-ttu-id="5aa8e-139">8 つのコントローラー クラスのうちの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-139">One of the 8 Controller classes.</span></span> <span data-ttu-id="5aa8e-140">たとえば、LedgerDefaultDimensionEntryController</span><span class="sxs-lookup"><span data-stu-id="5aa8e-140">For example, LedgerDefaultDimensionEntryController</span></span>      | <span data-ttu-id="5aa8e-141">分析コード エントリ コントロールの動作を決定します。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-141">Determines the behavior of the Dimension Entry control.</span></span> <span data-ttu-id="5aa8e-142">このプロパティの詳細については以下で説明します。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-142">More information about this property is provided below.</span></span>                                                    |
| <span data-ttu-id="5aa8e-143">データ ソース</span><span class="sxs-lookup"><span data-stu-id="5aa8e-143">Data Source</span></span>      | <span data-ttu-id="5aa8e-144">フォーム データ ソース一覧のデータ ソース</span><span class="sxs-lookup"><span data-stu-id="5aa8e-144">Any data source in the form data source list</span></span>                                             | <span data-ttu-id="5aa8e-145">ここで指定するデータソースは、値データフィールドプロパティおよび/または列挙データフィールドプロパティで指定したフィールドを保持するテーブルをポイントする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-145">The data source specified here should be pointed to the table that holds the field specified in the Value Data Field property and/or the Enum Data Field property.</span></span> |
| <span data-ttu-id="5aa8e-146">列挙データ フィールド</span><span class="sxs-lookup"><span data-stu-id="5aa8e-146">Enum Data Field</span></span>  | <span data-ttu-id="5aa8e-147">データ ソース プロパティに指定されたデータ ソースによって参照されるテーブルのフィールドです。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-147">A field in the table referenced by the data source provided in the Data Source property.</span></span> | <span data-ttu-id="5aa8e-148">これは、列挙型に格納されているフィールドです。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-148">This is the field that the enumeration values will be stored in.</span></span> <span data-ttu-id="5aa8e-149">コントロールが列挙を使用していない場合は、このプロパティを指定しないでください。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-149">This property shouldn’t be specified if the control is not using an enumeration.</span></span>                  |
| <span data-ttu-id="5aa8e-150">列挙</span><span class="sxs-lookup"><span data-stu-id="5aa8e-150">Enumeration</span></span>      | <span data-ttu-id="5aa8e-151">任意の列挙。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-151">Any enumeration.</span></span> <span data-ttu-id="5aa8e-152">たとえば、NoYes</span><span class="sxs-lookup"><span data-stu-id="5aa8e-152">For example, NoYes</span></span>                                                      | <span data-ttu-id="5aa8e-153">コントロールで使用する列挙型です。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-153">The enumeration used by the control.</span></span> <span data-ttu-id="5aa8e-154">列挙型は、分析コード値の代わりにコントロールによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-154">The enumeration will be used by the control instead of Dimension values.</span></span>                                                      |
| <span data-ttu-id="5aa8e-155">値 データ フィールド</span><span class="sxs-lookup"><span data-stu-id="5aa8e-155">Value Data Field</span></span> | <span data-ttu-id="5aa8e-156">データ ソース プロパティに指定されたデータ ソースによって参照されるテーブルのフィールドです。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-156">A field in the table referenced by the data source provided in the Data Source property.</span></span> | <span data-ttu-id="5aa8e-157">これは、分析コード エントリ コントロールがバインドされているフィールドです。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-157">This is the field that the Dimension Entry control is bound to.</span></span>                                                                                                    |

## <a name="controller-class-property"></a><span data-ttu-id="5aa8e-158">コントローラー クラス プロパティ</span><span class="sxs-lookup"><span data-stu-id="5aa8e-158">Controller class property</span></span>
<span data-ttu-id="5aa8e-159">各コントローラーの詳細は、以下のテーブルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-159">The table provided below gives details about each controller.</span></span>

|                                                |                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5aa8e-160">**コントローラー**</span><span class="sxs-lookup"><span data-stu-id="5aa8e-160">**Controller**</span></span>                                 | <span data-ttu-id="5aa8e-161">**詳細**</span><span class="sxs-lookup"><span data-stu-id="5aa8e-161">**Details**</span></span>                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="5aa8e-162">BudgetDefaultDimensionValueSet</span><span class="sxs-lookup"><span data-stu-id="5aa8e-162">BudgetDefaultDimensionValueSet</span></span>                 | <span data-ttu-id="5aa8e-163">このコントローラーは、分析コード エントリ コントロールの既定値のデータ入力を、予算ベースでサポートしています。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-163">This controller provides budget based support for default value data entry in the Dimension Entry control.</span></span> <span data-ttu-id="5aa8e-164">予算の既定分析コードでは、主勘定分析コードが必要です。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-164">Budget Default Dimensions require a Main Account Dimension.</span></span>                                                                                                                                                    |
| <span data-ttu-id="5aa8e-165">PurchReqDefaultDimensionValueSet</span><span class="sxs-lookup"><span data-stu-id="5aa8e-165">PurchReqDefaultDimensionValueSet</span></span>               | <span data-ttu-id="5aa8e-166">このコントローラーは、分析コード エントリ コントロールの既定値のデータ入力を、PurchReq ベースでサポートしています。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-166">This controller provides PurchReq based support for default value data entry in the Dimension Entry control.</span></span> <span data-ttu-id="5aa8e-167">PurchReq の既定分析コードでは、主勘定分析コードが必要です。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-167">PurchReq Default Dimensions require a Main Account Dimension.</span></span>                                                                                                                                                |
| <span data-ttu-id="5aa8e-168">LedgerDefaultDimensionValueSet</span><span class="sxs-lookup"><span data-stu-id="5aa8e-168">LedgerDefaultDimensionValueSet</span></span>                 | <span data-ttu-id="5aa8e-169">このコントローラーは、分析コード エントリ コントロールの既定値のデータ入力を、元帳ベースでサポートしています。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-169">This controller provides ledger based support for default value data entry in the Dimension Entry control.</span></span> <span data-ttu-id="5aa8e-170">既定の分析コードでは、値が指定されていない行の名前列に「既定値なし」という語句が表示されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-170">Default Dimensions require the phrase “No default” to appear in the name column of any row that doesn’t have a value specified.</span></span> <span data-ttu-id="5aa8e-171">このコントローラーは、通常、設定、マスター データ、およびヘッダー レコードで使用します。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-171">This controller is typically used with setup, master data, and header records.</span></span> |
| <span data-ttu-id="5aa8e-172">LedgerDimensionValueSet</span><span class="sxs-lookup"><span data-stu-id="5aa8e-172">LedgerDimensionValueSet</span></span>                        | <span data-ttu-id="5aa8e-173">このコントローラーは、分析コード エントリ コントロールのデータ入力の元帳に基づくサポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-173">This controller provides ledger based support for data entry in the Dimension Entry control.</span></span> <span data-ttu-id="5aa8e-174">このコントローラーは通常、明細行品目またはトランザクション データに使用されます。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-174">This controller is typically used with line item or transactional data.</span></span>                                                                                                                                                      |
| <span data-ttu-id="5aa8e-175">InventSiteLockedDimensionValueSet</span><span class="sxs-lookup"><span data-stu-id="5aa8e-175">InventSiteLockedDimensionValueSet</span></span>              | <span data-ttu-id="5aa8e-176">このコントローラーは、InventSite フォーム専用の分析コード エントリ コントロールのデータ入力をサポートします。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-176">This controller provides support for data entry in the Dimension Entry control specifically for the InventSite form.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="5aa8e-177">InventSiteLinkedDimensionValueSet</span><span class="sxs-lookup"><span data-stu-id="5aa8e-177">InventSiteLinkedDimensionValueSet</span></span>              | <span data-ttu-id="5aa8e-178">このコントローラーは、在庫ディメンション リンク設定によって要求される動作の分析コード エントリ コントロールのデータ入力をサポートします。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-178">This controller provides support for data entry in the Dimension Entry control for the behavior mandated by the Inventory Dimension Link setup.</span></span> <span data-ttu-id="5aa8e-179">このコントローラーでは、会社が変更されたときに、特別な方法で、コントロールを更新します。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-179">This controller updates the control in a special way when the company is changed.</span></span>                                                                                         |
| <span data-ttu-id="5aa8e-180">InventSiteSMAItemDimensionValueSet</span><span class="sxs-lookup"><span data-stu-id="5aa8e-180">InventSiteSMAItemDimensionValueSet</span></span>             | <span data-ttu-id="5aa8e-181">このコントローラーは、在庫ディメンション リンク設定によって要求される動作の分析コード エントリ コントロールのデータ入力をサポートします。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-181">This controller provides support for data entry in the Dimension Entry control for the behavior mandated by the Inventory Dimension Link setup.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="5aa8e-182">InventSiteTmpLedgerBaseLinkedDimensionValueSet</span><span class="sxs-lookup"><span data-stu-id="5aa8e-182">InventSiteTmpLedgerBaseLinkedDimensionValueSet</span></span> | <span data-ttu-id="5aa8e-183">このコントローラーは、在庫ディメンション リンク設定によって要求される動作の分析コード エントリ コントロールのデータ入力をサポートします。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-183">This controller provides support for data entry in the Dimension Entry control for the behavior mandated by the Inventory Dimension Link setup.</span></span> <span data-ttu-id="5aa8e-184">このコントローラーは、特に TmpLedgerBase テーブルの DefaultDimension フィールドで動作します。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-184">This controller specifically works with the DefaultDimension field on the TmpLedgerBase table.</span></span>                                                                            |

<span data-ttu-id="5aa8e-185">いくつかの分析コード入力コントロールには、コントローラー プロパティが設定されていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-185">Some Dimension Entry controls might not have the controller property set.</span></span> <span data-ttu-id="5aa8e-186">この場合、コントローラーはコントロールの値データ フィールドの EDT から推測されます。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-186">The controller is inferred from the EDT of the control’s Value Data Field in these cases.</span></span> <span data-ttu-id="5aa8e-187">一連の分析コード エントリ コントロールの特定のプロパティを以下に示します。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-187">A set of Dimension Entry control specific properties is provided below.</span></span> <span data-ttu-id="5aa8e-188">これらのプロパティは、上記の一般的なアプローチのセクション (DimensionEntryControlHeader) で選択した、分析コード入力コントロールの PurchTable フォームのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-188">These properties are for the Dimension Entry control selected in the General Approach section above (DimensionEntryControlHeader) on the PurchTable form.</span></span> <span data-ttu-id="5aa8e-189">この分析コード エントリ コントロールは、PurchTableのTable テーブルの DefaultDimension フィールドを使用しています。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-189">This Dimension Entry control is using the DefaultDimension field on the PurchTable table.</span></span> <span data-ttu-id="5aa8e-190">PurchTable の DefaultDimension フィールドの拡張データ型プロパティは、LedgerDefaultDimensionValueSet (以下を参照) に設定されます。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-190">The Extended Data Type property of the DefaultDimension field on PurchTable is set to LedgerDefaultDimensionValueSet (shown below).</span></span> <span data-ttu-id="5aa8e-191">実行時に、この EDT は LedgerDefaultDimensionEntryController にマップされます。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-191">At runtime, this EDT will be mapped to the LedgerDefaultDimensionEntryController.</span></span> <span data-ttu-id="5aa8e-192">したがって、この場合 DimensionEntryControlHeader コントロールは LedgerDefaultDimensionEntryController を使用します。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-192">So the DimensionEntryControlHeader control uses the LedgerDefaultDimensionEntryController in this case.</span></span> <span data-ttu-id="5aa8e-193">次の例は、EDT とそれがマップされているコントローラーを示しています。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-193">The following example shows the EDTs and the controllers they are mapped to.</span></span> <span data-ttu-id="5aa8e-194">[![3](./media/3.png)](./media/3.png) [![4](./media/4.png)](./media/4.png)</span><span class="sxs-lookup"><span data-stu-id="5aa8e-194">[![3](./media/3.png)](./media/3.png) [![4](./media/4.png)](./media/4.png)</span></span>

#### <a name="extended-data-types-and-the-controllers-they-are-mapped-to"></a><span data-ttu-id="5aa8e-195">拡張データ型およびマップされるコントローラー</span><span class="sxs-lookup"><span data-stu-id="5aa8e-195">Extended data types and the controllers they are mapped to</span></span>

|                                                |                                                       |
|------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="5aa8e-196">**拡張データ型**</span><span class="sxs-lookup"><span data-stu-id="5aa8e-196">**Extended data type**</span></span>                         | <span data-ttu-id="5aa8e-197">**コントローラー**</span><span class="sxs-lookup"><span data-stu-id="5aa8e-197">**Controller**</span></span>                                        |
| <span data-ttu-id="5aa8e-198">BudgetDefaultDimensionValueSet</span><span class="sxs-lookup"><span data-stu-id="5aa8e-198">BudgetDefaultDimensionValueSet</span></span>                 | <span data-ttu-id="5aa8e-199">BudgetDefaultDimensionEntryController</span><span class="sxs-lookup"><span data-stu-id="5aa8e-199">BudgetDefaultDimensionEntryController</span></span>                 |
| <span data-ttu-id="5aa8e-200">PurchReqDefaultDimensionValueSet</span><span class="sxs-lookup"><span data-stu-id="5aa8e-200">PurchReqDefaultDimensionValueSet</span></span>               | <span data-ttu-id="5aa8e-201">PurchReqDefaultDimensionEntryController</span><span class="sxs-lookup"><span data-stu-id="5aa8e-201">PurchReqDefaultDimensionEntryController</span></span>               |
| <span data-ttu-id="5aa8e-202">LedgerDefaultDimensionValueSet</span><span class="sxs-lookup"><span data-stu-id="5aa8e-202">LedgerDefaultDimensionValueSet</span></span>                 | <span data-ttu-id="5aa8e-203">LedgerDefaultDimensionEntryController</span><span class="sxs-lookup"><span data-stu-id="5aa8e-203">LedgerDefaultDimensionEntryController</span></span>                 |
| <span data-ttu-id="5aa8e-204">LedgerDimensionValueSet</span><span class="sxs-lookup"><span data-stu-id="5aa8e-204">LedgerDimensionValueSet</span></span>                        | <span data-ttu-id="5aa8e-205">LedgerDimensionEntryController</span><span class="sxs-lookup"><span data-stu-id="5aa8e-205">LedgerDimensionEntryController</span></span>                        |
| <span data-ttu-id="5aa8e-206">InventSiteLockedDimensionValueSet</span><span class="sxs-lookup"><span data-stu-id="5aa8e-206">InventSiteLockedDimensionValueSet</span></span>              | <span data-ttu-id="5aa8e-207">InventSiteLockedDimensionEntryController</span><span class="sxs-lookup"><span data-stu-id="5aa8e-207">InventSiteLockedDimensionEntryController</span></span>              |
| <span data-ttu-id="5aa8e-208">InventSiteLinkedDimensionValueSet</span><span class="sxs-lookup"><span data-stu-id="5aa8e-208">InventSiteLinkedDimensionValueSet</span></span>              | <span data-ttu-id="5aa8e-209">InventSiteLinkedDimensionEntryController</span><span class="sxs-lookup"><span data-stu-id="5aa8e-209">InventSiteLinkedDimensionEntryController</span></span>              |
| <span data-ttu-id="5aa8e-210">InventSiteSMAItemDimensionValueSet</span><span class="sxs-lookup"><span data-stu-id="5aa8e-210">InventSiteSMAItemDimensionValueSet</span></span>             | <span data-ttu-id="5aa8e-211">InventSiteSMAItemDimensionEntryController</span><span class="sxs-lookup"><span data-stu-id="5aa8e-211">InventSiteSMAItemDimensionEntryController</span></span>             |
| <span data-ttu-id="5aa8e-212">InventSiteTmpLedgerBaseLinkedDimensionValueSet</span><span class="sxs-lookup"><span data-stu-id="5aa8e-212">InventSiteTmpLedgerBaseLinkedDimensionValueSet</span></span> | <span data-ttu-id="5aa8e-213">InventSiteTmpLedgerBaseLinked-</span><span class="sxs-lookup"><span data-stu-id="5aa8e-213">InventSiteTmpLedgerBaseLinked-</span></span><br><span data-ttu-id="5aa8e-214">DimensionEntryController</span><span class="sxs-lookup"><span data-stu-id="5aa8e-214">DimensionEntryController</span></span> |

## <a name="upgrade-script-todos"></a><span data-ttu-id="5aa8e-215">スクリプト TODO のアップグレード</span><span class="sxs-lookup"><span data-stu-id="5aa8e-215">Upgrade Script TODOs</span></span>
### <a name="dynamics-ax-2012"></a><span data-ttu-id="5aa8e-216">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="5aa8e-216">Dynamics AX 2012</span></span> 
<pre><code>/* TODO: (Code Upgrade) [Dimension entry control] 
Replace this based on the migration guidance. */
DimensionEntryControl.reactivate();</code></pre>

### <a name="microsoft-dynamics-365-for-finance-and-operations"></a><span data-ttu-id="5aa8e-217">Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5aa8e-217">Microsoft Dynamics 365 for Finance and Operations</span></span> 
<span data-ttu-id="5aa8e-218">reactivate メソッドは、分析コード エントリ コントロールを現在の設定でリフレッシュします。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-218">The reactivate method refreshes the Dimension Entry control with current settings.</span></span> <span data-ttu-id="5aa8e-219">このメソッドは、会社または表示された分析コード リストが変更された場合にのみ、コントロールを更新します。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-219">The method only refreshes the control if the company or displayed dimension list changes.</span></span> <span data-ttu-id="5aa8e-220">この呼び出しは、これらのどちらも以前に変更されていない場合に削除できます。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-220">This call can be removed if neither of these are changed before it.</span></span> <span data-ttu-id="5aa8e-221">それ以外の場合は、呼び出しはそのままにします。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-221">Otherwise leave the call as is.</span></span> <span data-ttu-id="5aa8e-222">reactivate() の直前で parmCompany() が呼び出され、それが reactivate() より前に呼び出された唯一の DEC API であり、そのメソッドがデータソースの active() 中に呼び出された場合、最適化を手動で行うことでパフォーマンスを向上させ、コードの取り込みを減らすことができます。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-222">If parmCompany() is called immediately before reactivate(), and it is the only DEC API called before reactivate(), and the method it resides in is called during the active() of the datasource; an optimization can be manually made to improve performance and reduce code uptake:</span></span>
<p><span data-ttu-id="5aa8e-223">1) データ ソースのアクティブ プロセス中に、parmCompany() および reactivate() 呼び出しを削除します。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-223">1) Remove the parmCompany() and reactivate() calls during the datasource active process.</span></span></p>
<p><span data-ttu-id="5aa8e-224">2) 最初のユーザーとフォームとのやりとりの前に呼び出されるフォーム init()、run()、datasource init()、または同様のメソッドでは、次のコード行を追加します。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-224">2) In the form init(), run(), datasource init(), or similar methods called before initial user interaction with the form, add the following line of code:</span></span></p>
<pre><code>DimensionEntryControl.parmCompanyReference(
    fieldStr([myTable], [myCompanyContextField]);</code></pre>
<span data-ttu-id="5aa8e-225">この変更により、DEC はアクティブなレコードが変更されたときに更新される会社フィールド参照を自動的に見つけ出し、それに応じてディメンションのリストを更新できます。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-225">This change will allow the DEC to automatically find the company field reference that is updated when the active record changes and refresh the list of dimensions accordingly.</span></span> <span data-ttu-id="5aa8e-226"><strong>注記:</strong> これは、parmDisplayedDimensionSet() の使用と組み合わせないでください。そうすると、分析コードの一覧が予想外のものになることがあります。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-226"><strong>Note:</strong> This should not be combined with the use of parmDisplayedDimensionSet() otherwise the list of dimensions may not be the ones expected.</span></span> <span data-ttu-id="5aa8e-227">会社の選択フィールドの変更されたメソッドなど、他のすべての場所で、データ ソースがその時点で読み取られるプロセスではないため、会社内の変更をすぐに反映するように parmCompany() を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-227">In all other locations, such as the modified method of a company selection field, parmCompany() must be called to immediately reflect the change in company as the datasource is not in the process of being read at that time.</span></span>

### <a name="dynamics-ax-2012"></a><span data-ttu-id="5aa8e-228">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="5aa8e-228">Dynamics AX 2012</span></span>
<pre><code>/* TODO: (Code Upgrade) [Dimension entry control] 
Replace this based on the migration guidance. */
DimensionEntryControl.setEditability(true, 0);</code></pre>

### <a name="finance-and-operations"></a><span data-ttu-id="5aa8e-229">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5aa8e-229">Finance and Operations</span></span>  
<span data-ttu-id="5aa8e-230">特定の編集可能なディメンション セットが必要な場合は、この呼び出しを次のように置き換えます。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-230">If a specific editable dimension set is needed, replace this call with:</span></span>
<pre><code>DimensionEntryControl.parmEditableDimensionSet(
    editableDimensionSet);</code></pre><span data-ttu-id="5aa8e-231">
<strong>注記</strong>: editableDimensionSet パラメーターは、タイプ DimensionEnumeration です。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-231">
<strong>Note</strong>: The editableDimensionSet parameter is of type DimensionEnumeration.</span></span>

### <a name="dynamics-ax-2012"></a><span data-ttu-id="5aa8e-232">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="5aa8e-232">Dynamics AX 2012</span></span> 
<pre><code>/* TODO: (Code Upgrade) [Dimension entry control] 
This method can be removed if there is 
no custom implementation */
// dimensionDefaultingController.pageActivated();</code></pre>

### <a name="finance-and-operations"></a><span data-ttu-id="5aa8e-233">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5aa8e-233">Finance and Operations</span></span>  
<span data-ttu-id="5aa8e-234">このコールを、分析コード エントリ コントロールの親コントロールの pageActivated メソッドまたは Form Init メソッド内で実行する場合、削除することができます。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-234">If this call is made within the pageActivated method of the Dimension Entry control’s parent control or the form init method, it can be removed.</span></span> <span data-ttu-id="5aa8e-235">上記の場所以外のメソッド呼び出しの意図は明確ではありません。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-235">The intent of this method call outside the above mentioned locations isn’t clear.</span></span> <span data-ttu-id="5aa8e-236">呼び出しを削除して、コントロールをテストします。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-236">Remove the call and test the control.</span></span>

### <a name="dynamics-ax-2012"></a><span data-ttu-id="5aa8e-237">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="5aa8e-237">Dynamics AX 2012</span></span>
<pre><code>/* TODO: (Code Upgrade) [Dimension entry control] 
Replace this based on the migration guidance. */
DimensionEntryControl.deleted();</code></pre>

### <a name="finance-and-operations"></a><span data-ttu-id="5aa8e-238">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5aa8e-238">Finance and Operations</span></span>  
<span data-ttu-id="5aa8e-239">データ ソースの削除メソッド内にはない deleted() の呼び出しのために、TODO が残されます。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-239">A TODO will be left for a call to deleted() that is not inside a data source delete method.</span></span> <span data-ttu-id="5aa8e-240">これらの呼び出しは、データソースの削除メソッド内にのみ存在すると予想され、置換はありません。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-240">These calls are only expected to be in data source delete methods, and there is no replacement.</span></span> <span data-ttu-id="5aa8e-241">呼び出しを削除して、コントロールをテストしてみてください。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-241">Try to remove the call and test the control.</span></span>

### <a name="dynamics-ax-2012"></a><span data-ttu-id="5aa8e-242">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="5aa8e-242">Dynamics AX 2012</span></span>
<pre><code>/* TODO: (Code Upgrade) [Dimension entry control] 
Replace this based on the migration guidance. */
// dimensionDefaultingController.writing();</code></pre>

### <a name="finance-and-operations"></a><span data-ttu-id="5aa8e-243">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5aa8e-243">Finance and Operations</span></span>  
<span data-ttu-id="5aa8e-244">分析コード エントリ コントロール フレームワークは、値を保存します。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-244">The Dimension Entry control framework will save values.</span></span> <span data-ttu-id="5aa8e-245">呼び出しを削除して、コントロールをテストします。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-245">Remove the call and test the control.</span></span>

### <a name="dynamics-ax-2012"></a><span data-ttu-id="5aa8e-246">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="5aa8e-246">Dynamics AX 2012</span></span>
<pre><code>/* TODO: (Code Upgrade) [Dimension entry control] 
Replace this based on the migration guidance. */
dimensionDefaultingController::findBackingEntityInstance();</code></pre>

### <a name="finance-and-operations"></a><span data-ttu-id="5aa8e-247">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5aa8e-247">Finance and Operations</span></span>  
<span data-ttu-id="5aa8e-248">エンティティを検索するには、getEntityInstance メソッドを DimensionAttributeValue から呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-248">To find the entity, the getEntityInstance method needs to be called from the DimensionAttributeValue.</span></span> <span data-ttu-id="5aa8e-249">この呼び出しを次のようなものに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-249">Replace this call with something similar to the following:</span></span>
<pre><code>DimensionAttributeValue dimAttrValue = 
    DimensionAttributeValue::
        findByDimensionAttributeAndValueNoError(
            dimensionAttributeTable, dimensionValue);
if (dimAttrValue) {
    common = dimAttrValue.getEntityInstance();
}</code></pre>

### <a name="dynamics-ax-2012"></a><span data-ttu-id="5aa8e-250">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="5aa8e-250">Dynamics AX 2012</span></span>
<pre><code>/* TODO: (Code Upgrade) [Dimension entry control] 
Replace this based on the migration guidance. */
DimensionEntryControlHeader.updateValues(NoYesUnchanged::Yes);</code></pre>

### <a name="finance-and-operations"></a><span data-ttu-id="5aa8e-251">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5aa8e-251">Finance and Operations</span></span>  
<span data-ttu-id="5aa8e-252">ここに 1 つのパラメーターがある場合のみ updateValues() メソッドが呼び出されるため、呼び出しは allowEdit() の呼び出しに置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-252">Since the updateValues() method is only called with one parameter here, the call can be replaced with a call to allowEdit().</span></span>
<pre><code>DimensionEntryControlHeader.allowEdit(
    NoYesUnchanged::Yes);</code></pre>

### <a name="dynamics-ax-2012"></a><span data-ttu-id="5aa8e-253">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="5aa8e-253">Dynamics AX 2012</span></span>
<pre><code>/* TODO: (Code Upgrade) [Dimension entry control] 
Replace this based on the migration guidance. */
DimensionEntryControlHeader.updateValues(
    NoYesUnchanged::No, true);</code></pre>

### <a name="finance-and-operations"></a><span data-ttu-id="5aa8e-254">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5aa8e-254">Finance and Operations</span></span> 
<span data-ttu-id="5aa8e-255">この場合、updateValues() の呼び出しには 2 つのパラメーターがあるので、コントロールの編集機能を変更するには allowEdit() の呼び出しと置き換え、コントロールの値をクリアするには loadAttributeValueSet() の呼び出しと置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-255">Since the call to updateValues() has two parameters in this case, it needs to be replaced with a call to allowEdit() to change the editability of the control and a call to loadAttributeValueSet() to clear the control’s values.</span></span>
<pre><code>DimensionEntryControlHeader.allowEdit(
    NoYesUnchanged::No);
DimensionEntryControlHeader.loadAttributeValueSet(0);</code></pre><span data-ttu-id="5aa8e-256">
<strong>注記:</strong> updateValues メソッド呼び出しの最初のパラメーターが NoYesUnchanged::Unchanged の場合、allowEdit の新しい呼び出しは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-256">
<strong>Note:</strong>If the first parameter in the updateValues method call was NoYesUnchanged::Unchanged, then the new call to allowEdit is not needed.</span></span> <span data-ttu-id="5aa8e-257">同様に、updateValues メソッドの 2 番目のパラメーターの呼び出しが false の場合、loadAttributeValueSet への呼び出しは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-257">Similarly, if the second parameter in the updateValues method call was false, then the call to loadAttributeValueSet is not needed.</span></span>

## <a name="methods-to-potentially-remove"></a><span data-ttu-id="5aa8e-258">**削除する可能性のあるメソッド**</span><span class="sxs-lookup"><span data-stu-id="5aa8e-258">**Methods to potentially remove**</span></span>
<span data-ttu-id="5aa8e-259">分析コード エントリ コントロールを保持するデータソースまたは tabpage/グループの残りのメソッドは、カスタム ロジックがない場合、削除することができます。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-259">Any leftover methods on the datasource or tabpage/group that holds the Dimension Entry control can be removed if there is no custom logic.</span></span> <span data-ttu-id="5aa8e-260">次のテーブルは、削除する必要があるカスタマイズのないメソッドの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-260">The following table shows examples of methods without customizations which should be deleted.</span></span>

### <a name="dynamics-ax-2012"></a><span data-ttu-id="5aa8e-261">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="5aa8e-261">Dynamics AX 2012</span></span>
<pre><code>public int active(){int ret;ret = super();return ret;}</code></pre>

### <a name="finance-and-operations"></a><span data-ttu-id="5aa8e-262">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5aa8e-262">Finance and Operations</span></span> 
<span data-ttu-id="5aa8e-263">このメソッドはデータソースにあります。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-263">This method will be on the data source.</span></span> <span data-ttu-id="5aa8e-264">カスタム ロジックがない場合に削除することができます。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-264">It can be removed if there is no custom logic.</span></span>

### <a name="dynamics-ax-2012"></a><span data-ttu-id="5aa8e-265">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="5aa8e-265">Dynamics AX 2012</span></span>
<pre><code>public void delete(){super();}</code></pre>
### <span data-ttu-id="5aa8e-266">Finance and Operations この方法はデータ ソースになります。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-266">Finance and Operations This method will be on the data source.</span></span> <span data-ttu-id="5aa8e-267">カスタム ロジックがない場合に削除することができます。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-267">It can be removed if there is no custom logic.</span></span>

### <a name="dynamics-ax-2012"></a><span data-ttu-id="5aa8e-268">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="5aa8e-268">Dynamics AX 2012</span></span>
<pre><code>public void deleted(){super();}</code></pre>

### <a name="finance-and-operations"></a><span data-ttu-id="5aa8e-269">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5aa8e-269">Finance and Operations</span></span> 
<span data-ttu-id="5aa8e-270">このメソッドはデータソースにあります。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-270">This method will be on the data source.</span></span> <span data-ttu-id="5aa8e-271">カスタム ロジックがない場合に削除することができます。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-271">It can be removed if there is no custom logic.</span></span>

### <a name="dynamics-ax-2012"></a><span data-ttu-id="5aa8e-272">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="5aa8e-272">Dynamics AX 2012</span></span>
<pre><code>public void deleting(){super();}</code></pre>

### <a name="finance-and-operations"></a><span data-ttu-id="5aa8e-273">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5aa8e-273">Finance and Operations</span></span> 
<span data-ttu-id="5aa8e-274">このメソッドはデータソースにあります。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-274">This method will be on the data source.</span></span> <span data-ttu-id="5aa8e-275">カスタム ロジックがない場合に削除することができます。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-275">It can be removed if there is no custom logic.</span></span>

### <a name="dynamics-ax-2012"></a><span data-ttu-id="5aa8e-276">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="5aa8e-276">Dynamics AX 2012</span></span>
<pre><code>public boolean validateDelete(){boolean ret;ret = super();return ret;}</code></pre>

### <a name="finance-and-operations"></a><span data-ttu-id="5aa8e-277">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5aa8e-277">Finance and Operations</span></span> 
<span data-ttu-id="5aa8e-278">このメソッドはデータソースにあります。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-278">This method will be on the data source.</span></span> <span data-ttu-id="5aa8e-279">カスタム ロジックがない場合に削除することができます。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-279">It can be removed if there is no custom logic.</span></span>

### <a name="dynamics-ax-2012"></a><span data-ttu-id="5aa8e-280">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="5aa8e-280">Dynamics AX 2012</span></span>
<pre><code>public void write(){super();}</code></pre>

### <a name="finance-and-operations"></a><span data-ttu-id="5aa8e-281">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5aa8e-281">Finance and Operations</span></span> 
<span data-ttu-id="5aa8e-282">このメソッドはデータソースにあります。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-282">This method will be on the data source.</span></span> <span data-ttu-id="5aa8e-283">カスタム ロジックがない場合に削除することができます。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-283">It can be removed if there is no custom logic.</span></span>

### <a name="dynamics-ax-2012"></a><span data-ttu-id="5aa8e-284">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="5aa8e-284">Dynamics AX 2012</span></span>
<pre><code>public void writing(){super();}</code></pre>
### <span data-ttu-id="5aa8e-285">Finance and Operations この方法はデータ ソースになります。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-285">Finance and Operations This method will be on the data source.</span></span> <span data-ttu-id="5aa8e-286">カスタム ロジックがない場合に削除することができます。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-286">It can be removed if there is no custom logic.</span></span>

### <a name="dynamics-ax-2012"></a><span data-ttu-id="5aa8e-287">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="5aa8e-287">Dynamics AX 2012</span></span>
<pre><code>public void written(){super();}</code></pre>
### <span data-ttu-id="5aa8e-288">Finance and Operations この方法はデータ ソースになります。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-288">Finance and Operations This method will be on the data source.</span></span> <span data-ttu-id="5aa8e-289">カスタム ロジックがない場合に削除することができます。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-289">It can be removed if there is no custom logic.</span></span>

### <a name="dynamics-ax-2012"></a><span data-ttu-id="5aa8e-290">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="5aa8e-290">Dynamics AX 2012</span></span>
<pre><code>public boolean validateWrite(){boolean ret;ret = super();return ret;}</code></pre>
### <span data-ttu-id="5aa8e-291">Finance and Operations この方法はデータ ソースになります。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-291">Finance and Operations This method will be on the data source.</span></span> <span data-ttu-id="5aa8e-292">カスタム ロジックがない場合に削除することができます。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-292">It can be removed if there is no custom logic.</span></span>

### <a name="dynamics-ax-2012"></a><span data-ttu-id="5aa8e-293">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="5aa8e-293">Dynamics AX 2012</span></span>
<pre><code>public void pageActivated()
{
    super();
    /* TODO: (Code Upgrade) [Dimension entry control] This method can be removed if 
    there is no custom implementation */
    // dimensionDefaultingController.pageActivated();
}</code></pre>
### <span data-ttu-id="5aa8e-294">Finance and Operations この方法は、分析コード エントリ コントロールを保持する TabPage またはグループになります。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-294">Finance and Operations This method will be on the tabpage or group that holds the Dimension Entry control.</span></span> <span data-ttu-id="5aa8e-295">カスタム ロジックがない場合は、メソッドを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-295">If there is no custom logic, the method can be deleted.</span></span>

## <a name="compile-errors"></a><span data-ttu-id="5aa8e-296">**コンパイル エラー**</span><span class="sxs-lookup"><span data-stu-id="5aa8e-296">**Compile Errors**</span></span>
<span data-ttu-id="5aa8e-297">このセクションでは、取り残される可能性のある一般的なコンパイル エラーに対処する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5aa8e-297">This section will go through how to address common compile errors that may be left behind.</span></span>


### <a name="dynamics-ax-2012"></a><span data-ttu-id="5aa8e-298">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="5aa8e-298">Dynamics AX 2012</span></span>

<span data-ttu-id="5aa8e-299"><strong>フォームで (PurchTable)。</strong></span><span class="sxs-lookup"><span data-stu-id="5aa8e-299"><strong>On the form (PurchTable):</strong></span></span>
<pre><code>purchTableForm.parmDimensionDefaultingControllerHeader(
    dimensionDefaultingControllerHeader);</code></pre><span data-ttu-id="5aa8e-300">
<strong>クラス内 (PurchTableForm):</strong>
</span><span class="sxs-lookup"><span data-stu-id="5aa8e-300">
<strong>In the class (PurchTableForm):</strong>
</span></span><pre><code>public DimensionDefaultingController 
parmDimensionDefaultingControllerHeader(
    DimensionDefaultingController 
        _dimensionDefaultingControllerHeader = 
        dimensionDefaultingControllerHeader)
{
   dimensionDefaultingControllerHeader =
       _dimensionDefaultingControllerHeader;
   return dimensionDefaultingControllerHeader;
}</code></pre>

### <a name="finance-and-operations"></a><span data-ttu-id="5aa8e-301">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5aa8e-301">Finance and Operations</span></span> 

<span data-ttu-id="5aa8e-302"><strong>フォームで (PurchTable)。</strong></span><span class="sxs-lookup"><span data-stu-id="5aa8e-302"><strong>On the form (PurchTable):</strong></span></span>
<pre><code>purchTableForm.parmDimensionEntryControlHeader(
    DimensionEntryControlHeader);</code></pre><span data-ttu-id="5aa8e-303">
<strong>クラス内 (PurchTableForm):</strong>
</span><span class="sxs-lookup"><span data-stu-id="5aa8e-303">
<strong>In the class (PurchTableForm):</strong>
</span></span><pre><code>public DimensionEntryControl 
parmDimensionEntryControlHeader(
    DimensionEntryControl 
       _dimensionEntryControlHeader = 
       dimensionEntryControlHeader)

{
    dimensionEntryControlHeader =
        _dimensionEntryControlHeader;
    return dimensionEntryControlHeader;
}</code></pre>



<a name="additional-resources"></a><span data-ttu-id="5aa8e-304">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="5aa8e-304">Additional resources</span></span>
--------

[<span data-ttu-id="5aa8e-305">分析コード エントリ コントロールのチュートリアル</span><span class="sxs-lookup"><span data-stu-id="5aa8e-305">Dimension Entry control migration walkthrough</span></span>](dimension-entry-control-migration.md)

[<span data-ttu-id="5aa8e-306">分析コード エントリ コントロール ダイアログのサポート</span><span class="sxs-lookup"><span data-stu-id="5aa8e-306">Dimension Entry control dialog support</span></span>](dimension-entry-control-dialog-support.md)


