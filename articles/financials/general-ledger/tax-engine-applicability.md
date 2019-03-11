---
title: 税エンジンの適用性
description: このトピックでは、税エンジンの適用性について説明します。
author: yijialuan
manager: AnnBe
ms.date: 10/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, GTE, Applicability
audience: IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: India
ms.author: riluan
ms.search.validFrom: 2018-10-07
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: d3d3f09bc0dfb0299f9f4ef374eb920f16001cd3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368855"
---
# <a name="tax-engine-applicability"></a><span data-ttu-id="cda0f-103">税エンジンの適用性</span><span class="sxs-lookup"><span data-stu-id="cda0f-103">Tax engine applicability</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cda0f-104">[税エンジン](tax-engine.md) (GTE とも呼ばれる) は、税の適用、計算、転記、および決済を判断する、法律上およびビジネス要求に基づく税の諸規則を決定を構成することができます。</span><span class="sxs-lookup"><span data-stu-id="cda0f-104">The [Tax engine](tax-engine.md) (also referred to as GTE) lets you configure tax rules that determine tax applicability, calculation, posting, and settlement, based on legal and business requirements.</span></span> <span data-ttu-id="cda0f-105">このトピックでは、GTE が税金の適用性を処理する方法を理解するのに役立つ税エンジンコンフィギュレーションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="cda0f-105">This topic walks you through a tax engine configuration to help you understand how GTE handles tax applicability.</span></span>

> [!NOTE]
> <span data-ttu-id="cda0f-106">税エンジン機能は、インドに基本住所がある法人に対してのみ使用可能です。</span><span class="sxs-lookup"><span data-stu-id="cda0f-106">The Tax engine functionality is only available for legal entities with a primary address in India.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="cda0f-107">必要条件</span><span class="sxs-lookup"><span data-stu-id="cda0f-107">Prerequisites</span></span>                                               
<span data-ttu-id="cda0f-108">このドキュメントでは、インドの商品及びサービス税のコンフィギュレーションを使用して、税の適用について説明します。</span><span class="sxs-lookup"><span data-stu-id="cda0f-108">This document uses India Goods and Services Tax configuration to explain the tax applicability.</span></span> <span data-ttu-id="cda0f-109">詳細については、[インドの商品及びサービス税](../localizations/apac-ind-gst.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cda0f-109">For more information, see [India Goods and Services Tax](../localizations/apac-ind-gst.md).</span></span>

## <a name="overview"></a><span data-ttu-id="cda0f-110">概要</span><span class="sxs-lookup"><span data-stu-id="cda0f-110">Overview</span></span>
<span data-ttu-id="cda0f-111">税の適用性とは、税タイプ、税コンポーネント、または税率が適用される条件です。</span><span class="sxs-lookup"><span data-stu-id="cda0f-111">Tax applicability is the condition under which tax type, tax component, or tax rate are applicable.</span></span> <span data-ttu-id="cda0f-112">たとえば、インドの GST では、ある州から別の州に商品を販売する場合、IGST を請求する必要があります。販売している商品によって税率が決まります。</span><span class="sxs-lookup"><span data-stu-id="cda0f-112">For example, for India GST, if you sell goods from one state to another state, you need to charge IGST, and the goods you are selling will determine the tax rate.</span></span> <span data-ttu-id="cda0f-113">税エンジンは 2 種類の方法で、税の適用、ルックアップおよび条件を処理します。</span><span class="sxs-lookup"><span data-stu-id="cda0f-113">The tax engine provides two ways to handle the tax applicability, lookup and condition.</span></span> <span data-ttu-id="cda0f-114">ルックアップは主に動的適用ルールを処理するために使用され、条件は静的適用ルールを処理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="cda0f-114">A lookup is mainly used to handle the dynamic applicability rules, and a condition is used to handle the static applicability rules.</span></span>

<span data-ttu-id="cda0f-115">以下の GTE コンポーネントは、税の適用に関連しています。</span><span class="sxs-lookup"><span data-stu-id="cda0f-115">The following GTE components are relevant to tax applicability.</span></span>

|<span data-ttu-id="cda0f-116">GTE コンポーネント</span><span class="sxs-lookup"><span data-stu-id="cda0f-116">GTE component</span></span> | <span data-ttu-id="cda0f-117">ルックアップ/条件</span><span class="sxs-lookup"><span data-stu-id="cda0f-117">Lookup/Condition</span></span> | <span data-ttu-id="cda0f-118">備考</span><span class="sxs-lookup"><span data-stu-id="cda0f-118">Comments</span></span> |
|--------------|------------------|----------|
| <span data-ttu-id="cda0f-119">税タイプ</span><span class="sxs-lookup"><span data-stu-id="cda0f-119">Tax type</span></span> | <span data-ttu-id="cda0f-120">ルックアップ & 条件</span><span class="sxs-lookup"><span data-stu-id="cda0f-120">Lookup & Condition</span></span> |  |
| <span data-ttu-id="cda0f-121">税コンポーネント</span><span class="sxs-lookup"><span data-stu-id="cda0f-121">Tax component</span></span> | <span data-ttu-id="cda0f-122">ルックアップ & 条件</span><span class="sxs-lookup"><span data-stu-id="cda0f-122">Lookup & Condition</span></span> | <span data-ttu-id="cda0f-123">税コンポーネントと税タイプの両方に適用性ロジックを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="cda0f-123">Both tax component and tax type can have applicability logic.</span></span> <span data-ttu-id="cda0f-124">税コンポーネントは税タイプに属しているため、特定の税コンポーネントが適用可能かどうかを判断するために適用性ロジックが使用されます。</span><span class="sxs-lookup"><span data-stu-id="cda0f-124">Because the tax component is under tax type, applicability logic is used to determine whether a specific tax component is applicable.</span></span> |
| <span data-ttu-id="cda0f-125">税措置</span><span class="sxs-lookup"><span data-stu-id="cda0f-125">Tax measure</span></span> | <span data-ttu-id="cda0f-126">ルックアップ</span><span class="sxs-lookup"><span data-stu-id="cda0f-126">Lookup</span></span> | <span data-ttu-id="cda0f-127">測定タイプは、**税率**、**割合**、または**割合グループ**である必要があります。</span><span class="sxs-lookup"><span data-stu-id="cda0f-127">The measure type should be **Tax rate**, **Percentage**, or **Percentage group**.</span></span> |
| <span data-ttu-id="cda0f-128">式</span><span class="sxs-lookup"><span data-stu-id="cda0f-128">Formula</span></span> | <span data-ttu-id="cda0f-129">条件</span><span class="sxs-lookup"><span data-stu-id="cda0f-129">Condition</span></span> | <span data-ttu-id="cda0f-130">特定のトランザクション タイプに対して、すべての税計算式が関連するわけではありません。</span><span class="sxs-lookup"><span data-stu-id="cda0f-130">For a specific transaction type, not all tax formulas are relevant.</span></span> <span data-ttu-id="cda0f-131">たとえば、非控除税額の計算に使用される式は、ドキュメントの購入にのみ関連しています。</span><span class="sxs-lookup"><span data-stu-id="cda0f-131">For example, the formula that is used to calculate the non-deductible tax is only relevant for document purchases.</span></span> |
| <span data-ttu-id="cda0f-132">転記</span><span class="sxs-lookup"><span data-stu-id="cda0f-132">Posting</span></span> | <span data-ttu-id="cda0f-133">条件</span><span class="sxs-lookup"><span data-stu-id="cda0f-133">Condition</span></span> | <span data-ttu-id="cda0f-134">異なるトランザクション タイプには、異なる転記ロジックがあります。</span><span class="sxs-lookup"><span data-stu-id="cda0f-134">Different transaction types have different posting logic.</span></span> <span data-ttu-id="cda0f-135">この場合、条件を使用して正しい転記プロファイルが使用されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="cda0f-135">In this case, a condition is used to ensure that the correct posting profile is used.</span></span> | 
| <span data-ttu-id="cda0f-136">会計</span><span class="sxs-lookup"><span data-stu-id="cda0f-136">Accounting</span></span> | <span data-ttu-id="cda0f-137">ルックアップ</span><span class="sxs-lookup"><span data-stu-id="cda0f-137">Lookup</span></span> | <span data-ttu-id="cda0f-138">会計は税勘定と同じです。</span><span class="sxs-lookup"><span data-stu-id="cda0f-138">Accounting is the same as tax accounts.</span></span> <span data-ttu-id="cda0f-139">ルックアップを使用すると、さまざまなシナリオに応じてさまざまな税勘定セットを管理できます。</span><span class="sxs-lookup"><span data-stu-id="cda0f-139">With a lookup, you can maintain different sets of tax accounts for different scenarios.</span></span> <span data-ttu-id="cda0f-140">たとえば、税務登録番号が異なれば、税勘定も異なります。</span><span class="sxs-lookup"><span data-stu-id="cda0f-140">For example, different tax registration numbers have different tax accounts.</span></span> |
| <span data-ttu-id="cda0f-141">クレジット プール</span><span class="sxs-lookup"><span data-stu-id="cda0f-141">Credit pool</span></span> | <span data-ttu-id="cda0f-142">ルックアップ</span><span class="sxs-lookup"><span data-stu-id="cda0f-142">Lookup</span></span> | <span data-ttu-id="cda0f-143">ルックアップを使用して税の決済方法を決定します。</span><span class="sxs-lookup"><span data-stu-id="cda0f-143">Use a lookup to determine how to settle tax.</span></span> <span data-ttu-id="cda0f-144">たとえば、さまざまな税務登録番号に基づいて税を決済できます。</span><span class="sxs-lookup"><span data-stu-id="cda0f-144">For example, you can settle tax based on different tax registration numbers.</span></span> |
| <span data-ttu-id="cda0f-145">税期間</span><span class="sxs-lookup"><span data-stu-id="cda0f-145">Tax period</span></span> | <span data-ttu-id="cda0f-146">ルックアップ</span><span class="sxs-lookup"><span data-stu-id="cda0f-146">Lookup</span></span> | <span data-ttu-id="cda0f-147">ルックアップを使用して、さまざまなシナリオに使用する税の期間を決定します。</span><span class="sxs-lookup"><span data-stu-id="cda0f-147">Use a lookup to determine which tax period should be used for different scenarios.</span></span> |


## <a name="condition"></a><span data-ttu-id="cda0f-148">条件</span><span class="sxs-lookup"><span data-stu-id="cda0f-148">Condition</span></span>
<span data-ttu-id="cda0f-149">適用ルールが常に静的な場合は、条件を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cda0f-149">If the applicability rule is always static, you need to use a condition.</span></span> <span data-ttu-id="cda0f-150">たとえば、GST はインドの州内在庫移動には適用されません。</span><span class="sxs-lookup"><span data-stu-id="cda0f-150">For example, GST is not applicable for intra-state inventory transfer in India.</span></span>  

<span data-ttu-id="cda0f-151">**デザイナー**ボタンをクリックして税 (インドの GST) を開きます。</span><span class="sxs-lookup"><span data-stu-id="cda0f-151">Open Tax (India GST) by clicking the **Designer** button.</span></span> 

![CGST 条件](media/gte-tax-document-applicability-cgst.png)

<span data-ttu-id="cda0f-153">CGST、税コンポーネント CGST を選択し、鉛筆アイコンをクリックして、詳細な条件をチェックします。</span><span class="sxs-lookup"><span data-stu-id="cda0f-153">Select the tax component CGST, and click the pencil icon, to check the detailed condition.</span></span> 

![CGST 条件の詳細](media/gte-tax-document-applicability-cgst-condition.png)

<span data-ttu-id="cda0f-155">条件は、実際には、[電子申告](../../dev-itpro/analytics/general-electronic-reporting.md) 式です。</span><span class="sxs-lookup"><span data-stu-id="cda0f-155">The condition is actually an [Electronic Reporting](../../dev-itpro/analytics/general-electronic-reporting.md) expression.</span></span> <span data-ttu-id="cda0f-156">これは**データ ソース**の左側のフィールドと右側の**関数**で構成されています。</span><span class="sxs-lookup"><span data-stu-id="cda0f-156">It is comprised of the fields on the left in **Data source**, and **Functions** on the right.</span></span> <span data-ttu-id="cda0f-157">サポートされている関数の一覧については、[関数](../../dev-itpro/analytics/general-electronic-reporting-formula-designer.md#supported-functions) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cda0f-157">For a list of supported functions, see [Functions](../../dev-itpro/analytics/general-electronic-reporting-formula-designer.md#supported-functions).</span></span> 

<span data-ttu-id="cda0f-158">次の条件は、*課税対象文書のタイプ*を「在庫転送オーダー受信」、「在庫転送オーダー出荷」、または「在庫転送オーダー」にすることはできないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="cda0f-158">The following condition means that *Taxable Document Type* cannot be "Invent transfer order receive", "Invent transfer order shipment", or "Invent transfer order".</span></span> <span data-ttu-id="cda0f-159">つまり HSN コードまたは SAC のいずれかを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cda0f-159">This also means that either HSN Code or SAC should be specified.</span></span>
```
AND(Header.'Taxable Document Type'<>"Invent transfer order receive",
    Header.'Taxable Document Type'<>"Invent transfer order shipment",
    Header.'Taxable Document Type'<>"Invent transfer order", 
    OR(NOT(Header.Lines.'HSN Code'=""), NOT(Header.Lines.SAC=""))
   )
```
### <a name="enable-gst-for-intra-state-inventory-transfer-order"></a><span data-ttu-id="cda0f-160">州内在庫移動オーダーに対して GST を有効にする</span><span class="sxs-lookup"><span data-stu-id="cda0f-160">Enable GST for intra-state inventory transfer order</span></span>
<span data-ttu-id="cda0f-161">このシナリオでは、GST 登録番号が出荷元と出荷先の倉庫間で異なる場合、インド政府が州内在庫移動オーダーの GST の計算を要求するとします。</span><span class="sxs-lookup"><span data-stu-id="cda0f-161">In this scenario, suppose that the Indian government requires you to calculate GST for intra-state inventory transfer orders if the GST registration numbers are different between the ship from and ship to warehouse.</span></span> 

#### <a name="structure-of-the-data-source-in-the-formula-designer"></a><span data-ttu-id="cda0f-162">フォーミュラ デザイナーのデータソースの構造</span><span class="sxs-lookup"><span data-stu-id="cda0f-162">Structure of the Data source in the formula designer</span></span>
<span data-ttu-id="cda0f-163">フォーミュラ デザイナーの左端には、課税対象文書と税務書類に定義されているすべてのフィールドと、課税対象文書に定義されている参照モデルがあります。</span><span class="sxs-lookup"><span data-stu-id="cda0f-163">On the leftmost side of the formula designer, you can find all the fields that are defined in the taxable document and tax document, and the reference model that is defined in the taxable document.</span></span>
```
Header
└───Header fields
└───Lines
|   └───Lines field
|       └───Tax types
|           └───Tax components
|               └───Tax measures
Reference models
```
#### <a name="change-the-applicability-condition"></a><span data-ttu-id="cda0f-164">適用条件を変更する</span><span class="sxs-lookup"><span data-stu-id="cda0f-164">Change the applicability condition</span></span>
<span data-ttu-id="cda0f-165">適用条件を変更するには**ヘッダー > 明細行 > GST 登録番号**および**ヘッダー > 明細行 > パーティ GST 登録番号**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cda0f-165">To change the applicability condition, go to **Header > Lines > GST Registration number** and **Header > Lines > Party GST Registration number**.</span></span> <span data-ttu-id="cda0f-166">これらは、倉庫からの出荷および倉庫への出荷の GST 登録番号を表します。</span><span class="sxs-lookup"><span data-stu-id="cda0f-166">These represent the GST registration numbers for the ship from and ship to warehouse.</span></span> <span data-ttu-id="cda0f-167">条件は以下のように変更できます。</span><span class="sxs-lookup"><span data-stu-id="cda0f-167">The condition can be changed to the following.</span></span>
```
AND(
    OR(
       AND(
           OR(
              Header.'Taxable Document Type'="Invent transfer order receive",
              Header.'Taxable Document Type'="Invent transfer order shipment",
              Header.'Taxable Document Type'="Invent transfer order"
             ),
             'GST Registration Number'<>'Party GST Registration Number'
           ),
       AND(
           Header.'Taxable Document Type'<>"Invent transfer order receive",
           Header.'Taxable Document Type'<>"Invent transfer order shipment",
           Header.'Taxable Document Type'<>"Invent transfer order"
          )
      ), 
    OR(NOT(Header.Lines.'HSN Code'=""), NOT(Header.Lines.SAC=""))
   )
```
<span data-ttu-id="cda0f-168">データ ソースからフィールドを選択し、**データ ソースの追加**を使用して、式にフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="cda0f-168">Select the field from the data source, and use **Add data source** to add the field into the formula.</span></span> <span data-ttu-id="cda0f-169">「課税対象文書のタイプ」のように、名前に空白がある場合は、データ ソース フィールドの単一引用符を使用してください。</span><span class="sxs-lookup"><span data-stu-id="cda0f-169">Make sure to use single quotes for the data source field if there is an empty space in the name, like 'Taxable Document Type'.</span></span> <span data-ttu-id="cda0f-170">「在庫移動オーダー」のように空白がある場合は、値に対して二重引用符を使用します。</span><span class="sxs-lookup"><span data-stu-id="cda0f-170">Use a double quote for the value if there is an empty space, like "Inventory transfer order".</span></span>

<span data-ttu-id="cda0f-171">編集が完了した後に、**テスト**をクリックして式をテストします。</span><span class="sxs-lookup"><span data-stu-id="cda0f-171">Click **Test** to test your formula after you are done with editing.</span></span>

## <a name="lookup"></a><span data-ttu-id="cda0f-172">ルックアップ</span><span class="sxs-lookup"><span data-stu-id="cda0f-172">Lookup</span></span>
<span data-ttu-id="cda0f-173">静的適用ルールが複雑な場合、または動的適用ルールである場合は、ルックアップを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cda0f-173">If the static applicability rules are complex, or it is a dynamic applicability rule, you need to use a lookup.</span></span>

### <a name="lookup-for-static-applicability-rules"></a><span data-ttu-id="cda0f-174">静的適用ルールのルックアップ</span><span class="sxs-lookup"><span data-stu-id="cda0f-174">Lookup for static applicability rules</span></span>
<span data-ttu-id="cda0f-175">**GST** を選択して、**ルックアップ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cda0f-175">Select **GST**, click **Lookups**.</span></span>

![CGST 条件](media/gte-tax-document-applicability-static-lookups.png)

<span data-ttu-id="cda0f-177">ルックアップは静的適用ルールと動的適用ルールの両方を処理できるので、**ソース タイプ**ドロップダウンリストはこの目的のためにあります。</span><span class="sxs-lookup"><span data-stu-id="cda0f-177">Because a lookup can handle both static applicability rules and dynamic applicability rules, the **Source type** drop-down list is for this purpose.</span></span> <span data-ttu-id="cda0f-178">静的適用ルールには**コンフィギュレーション**を使用します。これは、ルックアップで使用されるデータがコンフィギュレーションから取得されることを意味します。</span><span class="sxs-lookup"><span data-stu-id="cda0f-178">Use **Configuration** for the static applicability rule, which means that the data used in the lookup comes from the configuration.</span></span> <span data-ttu-id="cda0f-179">動的適用ルールには**ユーザー データ**を使用します。これは、ルックアップに使用されるデータが Finance and Operations などのランタイム環境から取得されることを意味します。</span><span class="sxs-lookup"><span data-stu-id="cda0f-179">Use **User data** for the dynamic applicability rule, which means that the data used in the lookup comes from the runtime environment, such as Finance and Operations.</span></span>

<span data-ttu-id="cda0f-180">ルックアップはマトリックスです。</span><span class="sxs-lookup"><span data-stu-id="cda0f-180">A lookup is a matrix.</span></span> <span data-ttu-id="cda0f-181">各行の関係は *OR* で、行内の各列の関係は *AND* です。</span><span class="sxs-lookup"><span data-stu-id="cda0f-181">The relation of each line is *OR*, and the relation of each column within the line is *AND*.</span></span> <span data-ttu-id="cda0f-182">セルの値が空の場合は、すべての値が条件を満たすことを意味します。</span><span class="sxs-lookup"><span data-stu-id="cda0f-182">If the value of the cell is empty, it means that all of the values satisfy the condition.</span></span> 

<span data-ttu-id="cda0f-183">上のスクリーンショットでは、税タイプ GST のルックアップのためのすべてのデータはコンフィギュレーションから来ているので、**ソース タイプ**は**コンフィギュレーション**です。</span><span class="sxs-lookup"><span data-stu-id="cda0f-183">In the screenshot above, all the data for the lookup of tax type GST comes from the configuration, so the **Source type** is **Configuration**.</span></span>

<span data-ttu-id="cda0f-184">GST のルックアップを条件に変換する場合は次のように表示されます。</span><span class="sxs-lookup"><span data-stu-id="cda0f-184">If you convert the lookup of GST into a condition, it will look like following.</span></span>
``` 
OR(
    AND(Exempt=Exempt.No,
        AND('Tax Direction' = "Sales tax receivable",
            'GST Composition Scheme' = NoYes.No,
            'Party GST Registration Number' <> ""
        ),
        AND('Tax Direction' = "Sales tax payable",
            'Export Order' = NoYes.No,
            'GST Registration Number' <> ""
        ),
        AND('Tax Direction' = "Sales tax receivable",
            'GST Composition Scheme' = NoYes.No,
            'GST Registration Number' <> ""
        )
    )
)
```
### <a name="lookup-for-dynamic-applicability-rules"></a><span data-ttu-id="cda0f-185">動的適用ルールのルックアップ</span><span class="sxs-lookup"><span data-stu-id="cda0f-185">Lookup for dynamic applicability rules</span></span>
<span data-ttu-id="cda0f-186">多くの適用ルールは、ランタイム データに依存します。</span><span class="sxs-lookup"><span data-stu-id="cda0f-186">Many applicability rules depend on the runtime data.</span></span> <span data-ttu-id="cda0f-187">たとえば、一部の税コンポーネントは特定の商品またはサービスにのみ適用されるため、税務取引の種類が異なると税率も異なります。</span><span class="sxs-lookup"><span data-stu-id="cda0f-187">For example, some tax components are only applicable for a certain good or service, so a different type of tax transaction results in a different tax rate.</span></span> 

<span data-ttu-id="cda0f-188">**CESS** を選択して、**ルックアップ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cda0f-188">Select **CESS**, click **Lookups**.</span></span>

<span data-ttu-id="cda0f-189">インドでは、CESS は、特定の商品やサービスに適用されます。</span><span class="sxs-lookup"><span data-stu-id="cda0f-189">In India, CESS is applicable for certain goods and services.</span></span> <span data-ttu-id="cda0f-190">Finance and Operations では、HSN は商品を表し、SAC はサービスを表すため、ルックアップでは HSN コードと SAC が使用されます。</span><span class="sxs-lookup"><span data-stu-id="cda0f-190">In Finance and Operations, HSN represents goods, SAC represents services, so HSN Code and SAC are used in the lookup.</span></span> <span data-ttu-id="cda0f-191">HSN Code と SAC の実際の価は Finance and Operations から取得されるため、**ソース タイプ**は**ユーザー データ**です。</span><span class="sxs-lookup"><span data-stu-id="cda0f-191">The **Source type** is **User data**, because the real value of HSN Code and SAC come from Finance and Operations.</span></span>

<span data-ttu-id="cda0f-192">ここでは、CGST レートを決定する方法を確認しましょう。</span><span class="sxs-lookup"><span data-stu-id="cda0f-192">Now, let's check how the CGST rate is determined.</span></span> <span data-ttu-id="cda0f-193">**CGST > レート**の順に選択し、**ルックアップ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cda0f-193">Select **CGST > Rate**, click **Lookups**.</span></span>

![CGST > レート ルックアップ](media/gte-tax-document-applicability-dynamic-lookups.png)

<span data-ttu-id="cda0f-195">ランタイム データは税率を決定するために必要なので、システムは**ソース タイプ**と**ユーザー データ**の値を隠します。</span><span class="sxs-lookup"><span data-stu-id="cda0f-195">Runtime data is required to determine the tax rate, so the system hides the **Source type**, and the **User data** value.</span></span>

<span data-ttu-id="cda0f-196">商品やサービスが異なれば税率が異なるため、**HSN コード**および **SAC** があります。</span><span class="sxs-lookup"><span data-stu-id="cda0f-196">Different goods and services result in different tax rates, so there are **HSN Code** and **SAC**.</span></span> <span data-ttu-id="cda0f-197">**パーティ GST 登録番号**および**税提示方法**は、GST 未登録の仕入先から購入するシナリオを処理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="cda0f-197">**Party GST Registration Number** and **Tax Direction** are used to handle the scenario of purchasing from an unregistered GST supplier.</span></span> <span data-ttu-id="cda0f-198">**トランザクション開始日**および**トランザクション終了日**は、期間ごとに異なる税率を処理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="cda0f-198">**Transaction Date from** and **Transaction Date to** are used to handle different tax rate per periods.</span></span>

### <a name="enable-different-tax-rate-for-different-goods"></a><span data-ttu-id="cda0f-199">商品ごとに異なる税率を有効にする</span><span class="sxs-lookup"><span data-stu-id="cda0f-199">Enable different tax rate for different goods</span></span>
<span data-ttu-id="cda0f-200">異なる商品が 1 つの HSN コードを共有できるため、ルックアップでこのシナリオを満たすことはできません。</span><span class="sxs-lookup"><span data-stu-id="cda0f-200">Different goods can share one HSN code, so the lookup cannot satisfy this scenario.</span></span> <span data-ttu-id="cda0f-201">これに対応するには、別のルックアップ列が必要です。</span><span class="sxs-lookup"><span data-stu-id="cda0f-201">A different lookup column is needed to handle this.</span></span>

<span data-ttu-id="cda0f-202">**列**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cda0f-202">Click **Columns**.</span></span> <span data-ttu-id="cda0f-203">左側に**使用可能な列**がすべてあります。</span><span class="sxs-lookup"><span data-stu-id="cda0f-203">On the left side, you can find all of the **Available columns**.</span></span> <span data-ttu-id="cda0f-204">構造は、参照モデルがないことを除けば、フォーミュラ デザイナーの**データ ソース**と同じです。</span><span class="sxs-lookup"><span data-stu-id="cda0f-204">The structure is the same as the **Data source** in the formula designer, except that there are no reference models.</span></span>

![CGST > レート 変更 ルックアップ](media/gte-tax-document-applicability-change-lookups.png)

<span data-ttu-id="cda0f-206">**使用可能な列**で**品目 ID**を選択し、商品を一意に決定します。</span><span class="sxs-lookup"><span data-stu-id="cda0f-206">Select **Item ID** in **Available columns** to uniquely determine the goods.</span></span> <span data-ttu-id="cda0f-207">右矢印アイコンをクリックして、**選択された列**側に追加します。</span><span class="sxs-lookup"><span data-stu-id="cda0f-207">Click the right-arrow icon to add it to the **Selected columns** side.</span></span> <span data-ttu-id="cda0f-208">HSN が不要な場合は、**選択された列**で **HSN コード**を選択し、左矢印アイコンをクリックして削除できます。</span><span class="sxs-lookup"><span data-stu-id="cda0f-208">If HSN is not needed, you can select **HSN Code** in **Selected columns**, and click the left-arrow icon to remove it.</span></span> 
