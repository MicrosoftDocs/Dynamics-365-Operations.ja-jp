---
title: 拡張機能を使用した税統合のデータ フィールドの追加
description: このトピックでは、X++ 拡張機能を使用して税統合のデータ フィールドを追加する方法について説明します。
author: qire
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 8e3573f9c9971d4a5af33ece08b7e0b43f2e813a
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921168"
---
# <a name="add-data-fields-in-the-tax-integration-by-using-extension"></a><span data-ttu-id="3259b-103">拡張機能を使用した税統合のデータ フィールドの追加</span><span class="sxs-lookup"><span data-stu-id="3259b-103">Add data fields in the tax integration by using extension</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="3259b-104">このトピックでは、X++ 拡張機能を使用して税統合のデータ フィールドを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3259b-104">This topic explains how to use X++ extensions to add data fields in the tax integration.</span></span> <span data-ttu-id="3259b-105">これらのフィールドは、税サービスの税データ モデルに拡張し、税コードを決定するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="3259b-105">These fields can be extended to the tax data model of the tax service and used to determine tax codes.</span></span> <span data-ttu-id="3259b-106">詳細については、[税コンフィギュレーションにデータ フィールドを追加する](tax-service-add-data-fields-tax-configurations.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3259b-106">For more information, see [Add data fields in tax configurations](tax-service-add-data-fields-tax-configurations.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="3259b-107">データ モデル</span><span class="sxs-lookup"><span data-stu-id="3259b-107">Data model</span></span>

<span data-ttu-id="3259b-108">データ モデルのデータはオブジェクトによって転送され、クラスによって実装されます。</span><span class="sxs-lookup"><span data-stu-id="3259b-108">The data in the data model is carried by objects and implemented by classes.</span></span>

<span data-ttu-id="3259b-109">主なオブジェクトの一覧を次に示します。</span><span class="sxs-lookup"><span data-stu-id="3259b-109">Here is a list of the major objects:</span></span>

* <span data-ttu-id="3259b-110">AxClass/TaxIntegration **Document** Object</span><span class="sxs-lookup"><span data-stu-id="3259b-110">AxClass/TaxIntegration **Document** Object</span></span>
* <span data-ttu-id="3259b-111">AxClass/TaxIntegration **Line** Object</span><span class="sxs-lookup"><span data-stu-id="3259b-111">AxClass/TaxIntegration **Line** Object</span></span>
* <span data-ttu-id="3259b-112">AxClass/TaxIntegration **TaxLine** Object</span><span class="sxs-lookup"><span data-stu-id="3259b-112">AxClass/TaxIntegration **TaxLine** Object</span></span>

<span data-ttu-id="3259b-113">次の図に、これらのオブジェクトを関連付ける方法を示します。</span><span class="sxs-lookup"><span data-stu-id="3259b-113">The following illustration shows how these objects are related.</span></span>

<span data-ttu-id="3259b-114">[![データ モデル オブジェクト リレーションシップ](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)</span><span class="sxs-lookup"><span data-stu-id="3259b-114">[![Data model object relationship](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)</span></span>

<span data-ttu-id="3259b-115">**Document** オブジェクトには 多数の **Document** オブジェクトを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="3259b-115">A **Document** object can contain many **Line** objects.</span></span> <span data-ttu-id="3259b-116">各オブジェクトには、税サービスのメタデータが含まれます。</span><span class="sxs-lookup"><span data-stu-id="3259b-116">Each object contains metadata for the tax service.</span></span>

- <span data-ttu-id="3259b-117">`TaxIntegrationDocumentObject` には、ソース アドレスと `includingTax` メタデータに関する情報を含む `originAddress` メタデータがあり、その行に売上税が含まれるかどうかが示されます。</span><span class="sxs-lookup"><span data-stu-id="3259b-117">`TaxIntegrationDocumentObject` has `originAddress` metadata, which contains information about the source address, and `includingTax` metadata, which indicates whether the line amount includes sales tax.</span></span>
- <span data-ttu-id="3259b-118">`TaxIntegrationLineObject`には、`itemId`、`quantity`、および`categoryId` メタデータが含まれます。</span><span class="sxs-lookup"><span data-stu-id="3259b-118">`TaxIntegrationLineObject` has `itemId`, `quantity`, and `categoryId` metadata.</span></span>

> [!NOTE]
> <span data-ttu-id="3259b-119">`TaxIntegrationLineObject` には、**Charge** オブジェクトも実装されます。</span><span class="sxs-lookup"><span data-stu-id="3259b-119">`TaxIntegrationLineObject` also implements **Charge** objects.</span></span>

## <a name="integration-flow"></a><span data-ttu-id="3259b-120">統合フロー</span><span class="sxs-lookup"><span data-stu-id="3259b-120">Integration flow</span></span>

<span data-ttu-id="3259b-121">フロー内のデータは活動によって操作されます。</span><span class="sxs-lookup"><span data-stu-id="3259b-121">The data in the flow is manipulated by activities.</span></span>

### <a name="key-activities"></a><span data-ttu-id="3259b-122">主な活動</span><span class="sxs-lookup"><span data-stu-id="3259b-122">Key activities</span></span>

* <span data-ttu-id="3259b-123">AxClass/TaxIntegration **Calculation** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="3259b-123">AxClass/TaxIntegration **Calculation** ActivityOnDocument</span></span>
* <span data-ttu-id="3259b-124">AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="3259b-124">AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument</span></span>
* <span data-ttu-id="3259b-125">AxClass/TaxIntegration **DataPersistence** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="3259b-125">AxClass/TaxIntegration **DataPersistence** ActivityOnDocument</span></span>
* <span data-ttu-id="3259b-126">AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="3259b-126">AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument</span></span>
* <span data-ttu-id="3259b-127">AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="3259b-127">AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument</span></span>

<span data-ttu-id="3259b-128">活動は次の順序で実行されます。</span><span class="sxs-lookup"><span data-stu-id="3259b-128">Activities are run in the following order:</span></span>

1. <span data-ttu-id="3259b-129">取得の設定</span><span class="sxs-lookup"><span data-stu-id="3259b-129">Setting Retrieval</span></span>
2. <span data-ttu-id="3259b-130">データ取得</span><span class="sxs-lookup"><span data-stu-id="3259b-130">Data Retrieval</span></span>
3. <span data-ttu-id="3259b-131">計算サービス</span><span class="sxs-lookup"><span data-stu-id="3259b-131">Calculation Service</span></span>
4. <span data-ttu-id="3259b-132">通貨為替</span><span class="sxs-lookup"><span data-stu-id="3259b-132">Currency Exchange</span></span>
5. <span data-ttu-id="3259b-133">データ持続性</span><span class="sxs-lookup"><span data-stu-id="3259b-133">Data Persistence</span></span>

<span data-ttu-id="3259b-134">たとえば、**計算サービス** の前に **データ取得** を拡張します。</span><span class="sxs-lookup"><span data-stu-id="3259b-134">For example, extend **Data Retrieval** before **Calculation Service**.</span></span>

#### <a name="data-retrieval-activities"></a><span data-ttu-id="3259b-135">データ取得活動</span><span class="sxs-lookup"><span data-stu-id="3259b-135">Data Retrieval activities</span></span>

<span data-ttu-id="3259b-136">**データ取得** 活動は、データベースからデータを取得します。</span><span class="sxs-lookup"><span data-stu-id="3259b-136">**Data Retrieval** activities retrieve data from the database.</span></span> <span data-ttu-id="3259b-137">さまざまなトランザクションに対するアダプタにより、次の異なるトランザクション テーブルからデータを取得できます。</span><span class="sxs-lookup"><span data-stu-id="3259b-137">Adapters for different transactions are available to retrieve data from different transaction tables:</span></span>

- <span data-ttu-id="3259b-138">AxClass/TaxIntegration **PurchTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="3259b-138">AxClass/TaxIntegration **PurchTable** DataRetrieval</span></span>
- <span data-ttu-id="3259b-139">AxClass/TaxIntegration **PurchParmTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="3259b-139">AxClass/TaxIntegration **PurchParmTable** DataRetrieval</span></span>
- <span data-ttu-id="3259b-140">AxClass/TaxIntegration **PurchREQTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="3259b-140">AxClass/TaxIntegration **PurchREQTable** DataRetrieval</span></span>
- <span data-ttu-id="3259b-141">AxClass/TaxIntegration **PurchRFQTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="3259b-141">AxClass/TaxIntegration **PurchRFQTable** DataRetrieval</span></span>
- <span data-ttu-id="3259b-142">AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="3259b-142">AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval</span></span>
- <span data-ttu-id="3259b-143">AxClass/TaxIntegration **SalesTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="3259b-143">AxClass/TaxIntegration **SalesTable** DataRetrieval</span></span>
- <span data-ttu-id="3259b-144">AxClass/TaxIntegration **SalesParm** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="3259b-144">AxClass/TaxIntegration **SalesParm** DataRetrieval</span></span>

<span data-ttu-id="3259b-145">これらの **データ取得** 活動では、データベースから `TaxIntegrationDocumentObject` と `TaxIntegrationLineObject` にデータがコピーされます。</span><span class="sxs-lookup"><span data-stu-id="3259b-145">In these **Data Retrieval** activities, data is copied from the database to `TaxIntegrationDocumentObject` and `TaxIntegrationLineObject`.</span></span> <span data-ttu-id="3259b-146">これらの活動はすべて同じ抽象テンプレート クラスを拡張するので、メソッドは共通です。</span><span class="sxs-lookup"><span data-stu-id="3259b-146">Because all these activities extend the same abstract template class, they have common methods.</span></span>

#### <a name="calculation-service-activities"></a><span data-ttu-id="3259b-147">計算サービス活動</span><span class="sxs-lookup"><span data-stu-id="3259b-147">Calculation Service activities</span></span>

<span data-ttu-id="3259b-148">**税計算** 活動は、税サービスと税統合の間のリンクです。</span><span class="sxs-lookup"><span data-stu-id="3259b-148">The **Calculation Service** activity is the link between the tax service and the tax integration.</span></span> <span data-ttu-id="3259b-149">この活動は、次の機能を担当します。</span><span class="sxs-lookup"><span data-stu-id="3259b-149">This activity is responsible for the following functions:</span></span>

1. <span data-ttu-id="3259b-150">要求を作成する。</span><span class="sxs-lookup"><span data-stu-id="3259b-150">Construct the request.</span></span>
2. <span data-ttu-id="3259b-151">税務サービスへ要求を転記する。</span><span class="sxs-lookup"><span data-stu-id="3259b-151">Post the request to the tax service.</span></span>
3. <span data-ttu-id="3259b-152">税サービスから応答を取得する。</span><span class="sxs-lookup"><span data-stu-id="3259b-152">Get the response from the tax service.</span></span>
4. <span data-ttu-id="3259b-153">応答を解析する。</span><span class="sxs-lookup"><span data-stu-id="3259b-153">Parse the response.</span></span>

<span data-ttu-id="3259b-154">要求に追加するデータ フィールドは、他のメタデータと共に転記されます。</span><span class="sxs-lookup"><span data-stu-id="3259b-154">A data field that you add to the request will be posted together with other metadata.</span></span> 

## <a name="extension-implementation"></a><span data-ttu-id="3259b-155">拡張機能の実装</span><span class="sxs-lookup"><span data-stu-id="3259b-155">Extension implementation</span></span>

<span data-ttu-id="3259b-156">ここでは、拡張機能の実装方法を説明する詳細な手順を示します。</span><span class="sxs-lookup"><span data-stu-id="3259b-156">This section provides detailed steps that explain how to implement the extension.</span></span> <span data-ttu-id="3259b-157">例として **コスト センター** と **プロジェクト** の財務分析コードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="3259b-157">It uses the **Cost center** and **Project** financial dimensions as examples.</span></span>

### <a name="step-1-add-the-data-variable-in-the-object-class"></a><span data-ttu-id="3259b-158">手順 1</span><span class="sxs-lookup"><span data-stu-id="3259b-158">Step 1.</span></span> <span data-ttu-id="3259b-159">オブジェクト クラスにデータ変数を追加する</span><span class="sxs-lookup"><span data-stu-id="3259b-159">Add the data variable in the object class</span></span>

<span data-ttu-id="3259b-160">オブジェクト クラスには、データ変数およびデータの getter/setter メソッドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="3259b-160">The object class contains the data variable and getter/setter methods for the data.</span></span> <span data-ttu-id="3259b-161">フィールドのレベルに応じて、`TaxIntegrationDocumentObject` または `TaxIntegrationLineObject` にデータ フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="3259b-161">Add the data field to either `TaxIntegrationDocumentObject` or `TaxIntegrationLineObject`, depending on the level of the field.</span></span> <span data-ttu-id="3259b-162">次の例では行レベルを使用し、ファイル名は `TaxIntegrationLineObject_Extension.xpp` です。</span><span class="sxs-lookup"><span data-stu-id="3259b-162">The following example uses the line level, and the file name is `TaxIntegrationLineObject_Extension.xpp`.</span></span>

> [!NOTE]
> <span data-ttu-id="3259b-163">追加するデータ フィールドがドキュメント レベルの場合は、ファイル名を `TaxIntegrationDocumentObject_Extension.xpp` に変更します。</span><span class="sxs-lookup"><span data-stu-id="3259b-163">If the data field that you're adding is at the document level, change the file name to `TaxIntegrationDocumentObject_Extension.xpp`.</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

<span data-ttu-id="3259b-164">**コスト センター** と **プロジェクト** が、プライベート変数として追加されます。</span><span class="sxs-lookup"><span data-stu-id="3259b-164">**Cost center** and **Project** are added as private variables.</span></span> <span data-ttu-id="3259b-165">これらのデータ フィールドでデータを操作するための getter メソッドおよび Setter メソッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="3259b-165">Create getter and setter methods for these data fields to manipulate the data.</span></span>

### <a name="step-2-retrieve-data-from-the-database"></a><span data-ttu-id="3259b-166">手順 2</span><span class="sxs-lookup"><span data-stu-id="3259b-166">Step 2.</span></span> <span data-ttu-id="3259b-167">データベースからデータを取得する</span><span class="sxs-lookup"><span data-stu-id="3259b-167">Retrieve data from the database</span></span>

<span data-ttu-id="3259b-168">トランザクションを指定し、適切なアダプタ クラスを拡張してデータを取得します。</span><span class="sxs-lookup"><span data-stu-id="3259b-168">Specify the transaction, and extend the appropriate adapter classes to retrieve the data.</span></span> <span data-ttu-id="3259b-169">たとえば、**発注書** トランザクションを使用する場合は、`TaxIntegrationPurchTableDataRetrieval` および `TaxIntegrationVendInvoiceInfoTableDataRetrieval` を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3259b-169">For example, if you use a **Purchase order** transaction, you must extend `TaxIntegrationPurchTableDataRetrieval` and `TaxIntegrationVendInvoiceInfoTableDataRetrieval`.</span></span> 

> [!NOTE]
> <span data-ttu-id="3259b-170">`TaxIntegrationPurchParmTableDataRetrieval` は、`TaxIntegrationPurchTableDataRetrieval` から継承されています。</span><span class="sxs-lookup"><span data-stu-id="3259b-170">`TaxIntegrationPurchParmTableDataRetrieval` is inherited from `TaxIntegrationPurchTableDataRetrieval`.</span></span> <span data-ttu-id="3259b-171">`purchTable` と `purchParmTable` テーブルのロジックが異なる場合以外、変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="3259b-171">It should not be changed unless the logic of the `purchTable` and `purchParmTable` tables differs.</span></span>

<span data-ttu-id="3259b-172">すべてのトランザクションにデータ フィールドを追加する必要がある場合は、すべての `DataRetrieval` クラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="3259b-172">If the data field should be added for all transactions, extend all `DataRetrieval` classes.</span></span>

<span data-ttu-id="3259b-173">すべての **データ取得** 活動は同じテンプレート クラスを拡張するため、クラス構造、変数、およびメソッドは類似しています。</span><span class="sxs-lookup"><span data-stu-id="3259b-173">Because all **Data Retrieval** activities extend the same template class, the class structures, variables, and methods are similar.</span></span>

```X++
protected TaxIntegrationDocumentObject document;

/// <summary>
/// Copies to the document.
/// </summary>
protected abstract void copyToDocument()
{
    // It is recommended to implement as:
    //
    // this.copyToDocumentByDefault();
    // this.copyToDocumentFromHeaderTable();
    // this.copyAddressToDocument();
}
 
/// <summary>
/// Copies to the current line of the document.
/// </summary>
/// <param name = "_line">The current line of the document.</param>
protected abstract void copyToLine(TaxIntegrationLineObject _line)
{
    // It is recommended to implement as:
    //
    // this.copyToLineByDefault(_line);
    // this.copyToLineFromLineTable(_line);
    // this.copyQuantityAndTransactionAmountToLine(_line);
    // this.copyAddressToLine(_line);
    // this.copyToLineFromHeaderTable(_line);
}
```

<span data-ttu-id="3259b-174">次の例では、`PurchTable` テーブルを使用する場合の基本的な構造を示します。</span><span class="sxs-lookup"><span data-stu-id="3259b-174">The following example shows the basic structure when the `PurchTable` table is used.</span></span>

```X++
public class TaxIntegrationPurchTableDataRetrieval extends TaxIntegrationAbstractDataRetrievalTemplate
{
    protected PurchTable purchTable;
    protected PurchLine purchLine;

    // Query builder methods
    [Replaceable]
    protected SysDaQueryObject getDocumentQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineQueryObject()
    [Replaceable]
    protected SysDaQueryObject getDocumentChargeQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineChargeQueryObject()

    // Data retrieval methods
    protected void copyToDocument()
    protected void copyToDocumentFromHeaderTable()
    protected void copyToLine(TaxIntegrationLineObject _line)
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    ...
}
```

<span data-ttu-id="3259b-175">`CopyToDocument` メソッドが呼び出されたとき、`this.purchTable` バッファは既に存在します。</span><span class="sxs-lookup"><span data-stu-id="3259b-175">When the `CopyToDocument` method is called, the `this.purchTable` buffer already exists.</span></span> <span data-ttu-id="3259b-176">このメソッドの目的は、`DocumentObject` クラスで作成された Setter メソッドを使用して、必要なすべてのデータを `this.purchTable` から `document` オブジェクトにコピーすることです。</span><span class="sxs-lookup"><span data-stu-id="3259b-176">The purpose of this method is to copy all the required data from `this.purchTable` to the `document` object by using the setter method that was created in the `DocumentObject` class.</span></span>

<span data-ttu-id="3259b-177">同様に、`CopyToLine` メソッドには `this.purchLine` バッファが既に存在します。</span><span class="sxs-lookup"><span data-stu-id="3259b-177">Likewise, a `this.purchLine` buffer already exists in the `CopyToLine` method.</span></span> <span data-ttu-id="3259b-178">このメソッドの目的は、`LineObject` クラスで作成された Setter メソッドを使用して、必要なすべてのデータを `this.purchLine` から `_line` オブジェクトにコピーすることです。</span><span class="sxs-lookup"><span data-stu-id="3259b-178">The purpose of this method is to copy all the required data from `this.purchLine` to the `_line` object by using the setter method that was created in the `LineObject` class.</span></span>

<span data-ttu-id="3259b-179">最も単純な方法は、`CopyToDocument` と `CopyToLine` メソッドを拡張する方法です。</span><span class="sxs-lookup"><span data-stu-id="3259b-179">The most straightforward approach is to extend the `CopyToDocument` and `CopyToLine` methods.</span></span> <span data-ttu-id="3259b-180">ただし、最初に `copyToDocumentFromHeaderTable` と `copyToLineFromLineTable` メソッドを試することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="3259b-180">However, we recommend that you try the `copyToDocumentFromHeaderTable` and `copyToLineFromLineTable` methods first.</span></span> <span data-ttu-id="3259b-181">希望通りに機能しない場合、独自のメソッドを実装し、`CopyToDocument` と `CopyToLine` で呼び出 します 。</span><span class="sxs-lookup"><span data-stu-id="3259b-181">If they don't work as you require, implement your own method, and call it in `CopyToDocument` and `CopyToLine`.</span></span> <span data-ttu-id="3259b-182">このメソッドを使用できる一般的な状況には次の 3 種類があります。</span><span class="sxs-lookup"><span data-stu-id="3259b-182">There are three common situations where you might use this approach:</span></span>

- <span data-ttu-id="3259b-183">必須フィールドは、`PurchTable` または `PurchLine` にあります。</span><span class="sxs-lookup"><span data-stu-id="3259b-183">The required field is in `PurchTable` or `PurchLine`.</span></span> <span data-ttu-id="3259b-184">この場合、`copyToDocumentFromHeaderTable` と `copyToLineFromLineTable` を拡張できます。</span><span class="sxs-lookup"><span data-stu-id="3259b-184">In this situation, you can extend `copyToDocumentFromHeaderTable` and `copyToLineFromLineTable`.</span></span> <span data-ttu-id="3259b-185">サンプル コードを次に示します。</span><span class="sxs-lookup"><span data-stu-id="3259b-185">Here is the sample code.</span></span>

    ```X++
    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        next copyToLineFromLineTable(_line);
        // if we already added XXX in TaxIntegrationLineObject
        _line.setXXX(this.purchLine.XXX);
    }
    ```

- <span data-ttu-id="3259b-186">必要なデータは、トランザクションの既定テーブルにはありません。</span><span class="sxs-lookup"><span data-stu-id="3259b-186">The required data isn't in the default table of the transaction.</span></span> <span data-ttu-id="3259b-187">ただし、既定のテーブルとの結合リレーションシップがいくつかあるため、フィールドはほとんどの行で必須です。</span><span class="sxs-lookup"><span data-stu-id="3259b-187">However, there are some join relationships with the default table, and the field is required on most lines.</span></span> <span data-ttu-id="3259b-188">この場合は、`getDocumentQueryObject` または `getLineObject` を置換して、結合リレーションシップによってテーブルをクエリします。</span><span class="sxs-lookup"><span data-stu-id="3259b-188">In this situation, replace `getDocumentQueryObject` or `getLineObject` to query the table by join relationship.</span></span> <span data-ttu-id="3259b-189">次の例では、**今すぐ配送** フィールドが行レベルで販売注文と統合されています。</span><span class="sxs-lookup"><span data-stu-id="3259b-189">In the following example, the **Deliver Now** field is integrated with the sales order at the line level.</span></span>

    ```X++
    public class TaxIntegrationSalesTableDataRetrieval
    {
        protected MCRSalesLineDropShipment mcrSalesLineDropShipment;

        /// <summary>
        /// Gets the query for the lines of the document.
        /// </summary>
        /// <returns>The query for the lines of the document</returns>
        [Replaceable]
        protected SysDaQueryObject getLineQueryObject()
        {
            return SysDaQueryObjectBuilder::from(this.salesLine)
                .where(this.salesLine, fieldStr(SalesLine, SalesId)).isEqualToLiteral(this.salesTable.SalesId)
                .outerJoin(this.mcrSalesLineDropShipment)
                .where(this.mcrSalesLineDropShipment, fieldStr(MCRSalesLineDropShipment, SalesLine)).isEqualTo(this.salesLine, fieldStr(SalesLine, RecId))
                .toSysDaQueryObject();
        }
    }
    ```

    <span data-ttu-id="3259b-190">この例では、`mcrSalesLineDropShipment` バッファが申告され、クエリが `getLineQueryObject` で定義されています。</span><span class="sxs-lookup"><span data-stu-id="3259b-190">In this example, a `mcrSalesLineDropShipment` buffer is declared, and the query is defined in `getLineQueryObject`.</span></span> <span data-ttu-id="3259b-191">クエリは、リレーションシップ `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId` を使用します。</span><span class="sxs-lookup"><span data-stu-id="3259b-191">The query uses the relationship `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`.</span></span> <span data-ttu-id="3259b-192">この状況を拡張している間、`getLineQueryObject` を独自に作成したクエリ オブジェクトで置換できます。</span><span class="sxs-lookup"><span data-stu-id="3259b-192">While you're extending in this situation, you can replace `getLineQueryObject` with your own constructed query object.</span></span> <span data-ttu-id="3259b-193">ただし、次の点に留意してください。</span><span class="sxs-lookup"><span data-stu-id="3259b-193">However, note the following points:</span></span>

    * <span data-ttu-id="3259b-194">`getLineQueryObject` メソッドの戻り値は `SysDaQueryObject` なので、SysDa法を使用してこの オブジェクトを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3259b-194">Because the return value of the `getLineQueryObject` method is `SysDaQueryObject`, you must construct this object by using the SysDa approach.</span></span>
    * <span data-ttu-id="3259b-195">存在するテーブルは削除できません。</span><span class="sxs-lookup"><span data-stu-id="3259b-195">Can't remove existed table.</span></span>

- <span data-ttu-id="3259b-196">必須データがトランザクション テーブルに複雑な結合リレーションシップで関連付けられている、またはリレーションシップが 1 対 1 (1:1) ではなく 1 対多 (1:N) です。</span><span class="sxs-lookup"><span data-stu-id="3259b-196">The required data is related to the transaction table by a complicated join relationship, or the relation isn't one to one (1:1) but one to many (1:N).</span></span> <span data-ttu-id="3259b-197">そのような状況では、少し複雑になります。</span><span class="sxs-lookup"><span data-stu-id="3259b-197">In this situation, things become a little complicated.</span></span> <span data-ttu-id="3259b-198">このような状況は、財務分析コードの例に適用されます。</span><span class="sxs-lookup"><span data-stu-id="3259b-198">This situation applies to the example of financial dimensions.</span></span> 

    <span data-ttu-id="3259b-199">この場合、独自のメソッドを実装してデータを取得できます。</span><span class="sxs-lookup"><span data-stu-id="3259b-199">In this situation, you can implement your own method to retrieve the data.</span></span> <span data-ttu-id="3259b-200">`TaxIntegrationPurchTableDataRetrieval_Extension.xpp` ファイル内のサンプル コードを次に示します。</span><span class="sxs-lookup"><span data-stu-id="3259b-200">Here is the sample code in the `TaxIntegrationPurchTableDataRetrieval_Extension.xpp` file.</span></span>

    ```X++
    [ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
    final class TaxIntegrationPurchTableDataRetrieval_Extension
    {
        private const str CostCenterKey = 'CostCenter';
        private const str ProjectKey = 'Project';

        /// <summary>
        /// Copies to the current line of the document from.
        /// </summary>
        /// <param name = "_line">The current line of the document.</param>
        protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
        {
            Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
            if (dimensionAttributeMap.exists(CostCenterKey))
            {
                _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
            }
            if (dimensionAttributeMap.exists(ProjectKey))
            {
                _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
            }
            next copyToLineFromLineTable(_line);
        }
        private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
        {
            DimensionAttribute dimensionAttribute;
            DimensionAttributeValue dimensionAttributeValue;
            DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
            Map ret = new Map(Types::String, Types::String);

            select Name, RecId from dimensionAttribute
                join dimensionAttributeValue
                    where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
                join DimensionAttributeValueSetItem
                    where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                        && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;

            while(dimensionAttribute.RecId)
            {
                ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
                next dimensionAttribute;
            }
            return ret;
        }
    }
    ```

### <a name="step-3-add-data-to-the-request"></a><span data-ttu-id="3259b-201">手順 3</span><span class="sxs-lookup"><span data-stu-id="3259b-201">Step 3.</span></span> <span data-ttu-id="3259b-202">要求へデータを追加する</span><span class="sxs-lookup"><span data-stu-id="3259b-202">Add data to the request</span></span>

<span data-ttu-id="3259b-203">`copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` または `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` メソッドを拡張して、データを要求に追加します。</span><span class="sxs-lookup"><span data-stu-id="3259b-203">Extend the `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` or `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` method to add data to the request.</span></span> <span data-ttu-id="3259b-204">`TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp` ファイル内のサンプル コードを次に示します。</span><span class="sxs-lookup"><span data-stu-id="3259b-204">Here is the sample code in the `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp` file.</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define key for the form in post request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());
    }
}
```

<span data-ttu-id="3259b-205">このコードでは `_destination` が転記要求の生成に使用されるラッパー オブジェクトであり、`_source` が `TaxIntegrationLineObject` オブジェクトになります。</span><span class="sxs-lookup"><span data-stu-id="3259b-205">In this code, `_destination` is the wrapper object that is used to generate the post request, and `_source` is the `TaxIntegrationLineObject` object.</span></span> 

> [!NOTE]
> * <span data-ttu-id="3259b-206">要求フォームで `private const str` と使用されるキーは次のように定義します 。</span><span class="sxs-lookup"><span data-stu-id="3259b-206">Define the key that is used in the request form as `private const str`.</span></span>
> * <span data-ttu-id="3259b-207">`SetField` メソッドを使って、`copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` メソッドのフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="3259b-207">Set the field in the `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` method by using the `SetField` method.</span></span> <span data-ttu-id="3259b-208">2 番目のパラメータのデータ型は、`string` である必要があります。</span><span class="sxs-lookup"><span data-stu-id="3259b-208">The data type of the second parameter should be `string`.</span></span> <span data-ttu-id="3259b-209">データ型が `string` でない場合、データ型を `string` に変換します。</span><span class="sxs-lookup"><span data-stu-id="3259b-209">If the data type isn't `string`, convert it to `string`.</span></span>

## <a name="appendix"></a><span data-ttu-id="3259b-210">付録</span><span class="sxs-lookup"><span data-stu-id="3259b-210">Appendix</span></span>

<span data-ttu-id="3259b-211">この付録では、財務分析コード (**コスト センター** および **プロジェクト**) を明細行レベルで統合する完全なサンプル コードを示しています。</span><span class="sxs-lookup"><span data-stu-id="3259b-211">This appendix shows the complete sample code for the integration of financial dimensions (**Cost center** and **Project**) at the line level.</span></span>

### <a name="taxintegrationlineobject_extensionxpp"></a><span data-ttu-id="3259b-212">TaxIntegrationLineObject_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="3259b-212">TaxIntegrationLineObject_Extension.xpp</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

### <a name="taxintegrationpurchtabledataretrieval_extensionxpp"></a><span data-ttu-id="3259b-213">TaxIntegrationPurchTableDataRetrieval_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="3259b-213">TaxIntegrationPurchTableDataRetrieval_Extension.xpp</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
final class TaxIntegrationPurchTableDataRetrieval_Extension
{
    private const str CostCenterKey = 'CostCenter';
    private const str ProjectKey = 'Project';

    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
        if (dimensionAttributeMap.exists(CostCenterKey))
        {
            _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
        }
        if (dimensionAttributeMap.exists(ProjectKey))
        {
            _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
        }
        next copyToLineFromLineTable(_line);
    }
    private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
    {
        DimensionAttribute dimensionAttribute;
        DimensionAttributeValue dimensionAttributeValue;
        DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
        Map ret = new Map(Types::String, Types::String);
        select Name, RecId from dimensionAttribute
            join dimensionAttributeValue
                where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
            join DimensionAttributeValueSetItem
                where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                    && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;
        while(dimensionAttribute.RecId)
        {
            ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
            next dimensionAttribute;
        }
        return ret;
    }
}
```

### <a name="taxintegrationcalculationactivityondocument_calculationservice_extensionxpp"></a><span data-ttu-id="3259b-214">TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="3259b-214">TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define key for the form in post request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());
    }
}
```
