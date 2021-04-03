---
title: GETENUMVALUEBYNAME ER 機能
description: このトピックでは、GETENUMVALUEBYNAME 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bfc173130a9fc57385826f77443ec28946ef68fd
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570593"
---
# <a name="getenumvaluebyname-er-function"></a><span data-ttu-id="3c1ba-103">GETENUMVALUEBYNAME ER 機能</span><span class="sxs-lookup"><span data-stu-id="3c1ba-103">GETENUMVALUEBYNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c1ba-104">`GETENUMVALUEBYNAME` 関数は、*文字列* 値して指定された列挙名を使用して、指定された列挙データソースの特定の *列挙* 値を検索します。</span><span class="sxs-lookup"><span data-stu-id="3c1ba-104">The `GETENUMVALUEBYNAME` function searches for a specific *Enum* value in the specified enumeration data source by using the enumeration name that is specified as a *String* value.</span></span> <span data-ttu-id="3c1ba-105">*列挙* 値が見つかった場合、関数によって返されます。</span><span class="sxs-lookup"><span data-stu-id="3c1ba-105">If the *Enum* value is found, the function returns it.</span></span> <span data-ttu-id="3c1ba-106">それ以外の場合、関数は **null** 列挙値を返します。</span><span class="sxs-lookup"><span data-stu-id="3c1ba-106">Otherwise, the function returns the **null** enumeration value.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c1ba-107">構文</span><span class="sxs-lookup"><span data-stu-id="3c1ba-107">Syntax</span></span>

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a><span data-ttu-id="3c1ba-108">引数</span><span class="sxs-lookup"><span data-stu-id="3c1ba-108">Arguments</span></span>

<span data-ttu-id="3c1ba-109">`enumeration data source path`: *列挙型*</span><span class="sxs-lookup"><span data-stu-id="3c1ba-109">`enumeration data source path`: *Enumeration*</span></span>

<span data-ttu-id="3c1ba-110">次のいずれかの列挙型のデータ ソースの有効なパス。</span><span class="sxs-lookup"><span data-stu-id="3c1ba-110">The valid path of a data source of one of the following enumeration types:</span></span>

- <span data-ttu-id="3c1ba-111">電子申告 (ER) モデル 列挙型</span><span class="sxs-lookup"><span data-stu-id="3c1ba-111">Electronic reporting (ER) model enumeration</span></span>
- <span data-ttu-id="3c1ba-112">ER 形式列挙型</span><span class="sxs-lookup"><span data-stu-id="3c1ba-112">ER format enumeration</span></span>
- <span data-ttu-id="3c1ba-113">Microsoft Dynamics 365 Finance 列挙型</span><span class="sxs-lookup"><span data-stu-id="3c1ba-113">Microsoft Dynamics 365 Finance enumeration</span></span>

<span data-ttu-id="3c1ba-114">`enumeration value text`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="3c1ba-114">`enumeration value text`: *String*</span></span>

<span data-ttu-id="3c1ba-115">単一の列挙型値の名前を表す文字列値。</span><span class="sxs-lookup"><span data-stu-id="3c1ba-115">A string value that represents the name of a single enumeration value.</span></span>

## <a name="return-values"></a><span data-ttu-id="3c1ba-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="3c1ba-116">Return values</span></span>

<span data-ttu-id="3c1ba-117">Nullable *列挙*</span><span class="sxs-lookup"><span data-stu-id="3c1ba-117">Nullable *Enum*</span></span>

<span data-ttu-id="3c1ba-118">結果列挙型の値。</span><span class="sxs-lookup"><span data-stu-id="3c1ba-118">The resulting enumeration value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3c1ba-119">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="3c1ba-119">Usage notes</span></span>

<span data-ttu-id="3c1ba-120">*文字列* 値として指定された列挙型値の名前を使用して *列挙* 値が見つからない場合は、例外がスローされません。</span><span class="sxs-lookup"><span data-stu-id="3c1ba-120">No exception is thrown if an *Enum* value isn't found by using the name of the enumeration value that is specified as a *String* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="3c1ba-121">例 1</span><span class="sxs-lookup"><span data-stu-id="3c1ba-121">Example 1</span></span>

<span data-ttu-id="3c1ba-122">次の図では、**ReportDirection** の列挙はデータ モデルで導入されます。</span><span class="sxs-lookup"><span data-stu-id="3c1ba-122">In the following illustration, the **ReportDirection** enumeration is introduced in a data model.</span></span> <span data-ttu-id="3c1ba-123">列挙型値のラベルが定義されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="3c1ba-123">Notice that labels are defined for the enumeration values.</span></span>

![データ モデル列挙に使用可能な値](./media/ER-data-model-enumeration-values.PNG)

<span data-ttu-id="3c1ba-125">次の図は、これらの詳細について説明しています。</span><span class="sxs-lookup"><span data-stu-id="3c1ba-125">The following illustration shows these details:</span></span>

- <span data-ttu-id="3c1ba-126">**$Direction** データソースが、ER レポートで構成されます。</span><span class="sxs-lookup"><span data-stu-id="3c1ba-126">The **$Direction** data source is configured in an ER report.</span></span> <span data-ttu-id="3c1ba-127">このデータ ソースは、**ReportDirection** モデルの列挙型に基づいて構成されます。</span><span class="sxs-lookup"><span data-stu-id="3c1ba-127">This data source is configured based on the **ReportDirection** model enumeration.</span></span>
- <span data-ttu-id="3c1ba-128">`$IsArrivals` 式は、この関数のパラメーターとして **$Direction** データ ソースに基づきモデル列挙型を使用するため設計されています。</span><span class="sxs-lookup"><span data-stu-id="3c1ba-128">The `$IsArrivals` expression is designed to use the model enumeration–based **$Direction** data source as a parameter of this function.</span></span>
- <span data-ttu-id="3c1ba-129">この比較式の値は、**TRUE** です。</span><span class="sxs-lookup"><span data-stu-id="3c1ba-129">The value of this comparison expression is **TRUE**.</span></span>

![データ モデル列挙の例](./media/ER-data-model-enumeration-usage.PNG)

## <a name="example-2"></a><span data-ttu-id="3c1ba-131">例 2</span><span class="sxs-lookup"><span data-stu-id="3c1ba-131">Example 2</span></span>

<span data-ttu-id="3c1ba-132">`GETENUMVALUEBYNAME` および [`LISTOFFIELDS`](er-functions-list-listoffields.md) 関数を使用すると、サポートされている列挙の値とラベルをテキスト値としてフェッチできます。</span><span class="sxs-lookup"><span data-stu-id="3c1ba-132">The `GETENUMVALUEBYNAME` and [`LISTOFFIELDS`](er-functions-list-listoffields.md) functions let you fetch values and labels of supported enumerations as text values.</span></span> <span data-ttu-id="3c1ba-133">(サポートされている列挙は、アプリケーション列挙、データ モデル列挙、形式列挙です。)</span><span class="sxs-lookup"><span data-stu-id="3c1ba-133">(The supported enumerations are application enumerations, data model enumerations, and format enumerations.)</span></span>

<span data-ttu-id="3c1ba-134">次の図では、**TransType** データ ソースはモデル マッピングで導入されます。</span><span class="sxs-lookup"><span data-stu-id="3c1ba-134">In the following illustration, the **TransType** data source is introduced in a model mapping.</span></span> <span data-ttu-id="3c1ba-135">このデータ ソースは、**LedgerTransType** アプリケーション列挙を参照しています。</span><span class="sxs-lookup"><span data-stu-id="3c1ba-135">This data source refers to the **LedgerTransType** application enumeration.</span></span>

![アプリケーション列挙を参照するモデル マッピングのデータ ソース](./media/er-functions-text-getenumvaluebyname-example2-1.png)

<span data-ttu-id="3c1ba-137">次の図は、モデル マッピングで構成されている **TransTypeList** データ ソースを示しています。</span><span class="sxs-lookup"><span data-stu-id="3c1ba-137">The following illustration shows the **TransTypeList** data source that is configured in a model mapping.</span></span> <span data-ttu-id="3c1ba-138">このデータ ソースは、**TransType** アプリケーション列挙に基づいて構成されます。</span><span class="sxs-lookup"><span data-stu-id="3c1ba-138">This data source is configured based on the **TransType** application enumeration.</span></span> <span data-ttu-id="3c1ba-139">この `LISTOFFIELDS` 関数は、すべての列挙値を、フィールドを含むレコードの一覧として返すために使用します。</span><span class="sxs-lookup"><span data-stu-id="3c1ba-139">The `LISTOFFIELDS` function is used to return all enumeration values as a list of records that contain fields.</span></span> <span data-ttu-id="3c1ba-140">このようにして、すべての列挙値の詳細が公開されます。</span><span class="sxs-lookup"><span data-stu-id="3c1ba-140">In this way, the details of every enumeration value are exposed.</span></span>

> [!NOTE]
> <span data-ttu-id="3c1ba-141">**EnumValue** フィールドは、`GETENUMVALUEBYNAME(TransType, TransTypeList.Name)` 式を使用して **TransTypeList** データソースに対して構成されます。</span><span class="sxs-lookup"><span data-stu-id="3c1ba-141">The **EnumValue** field is configured for the **TransTypeList** data source by using the `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)` expression.</span></span> <span data-ttu-id="3c1ba-142">このフィールドは、このリストのすべてのレコードの列挙値を返します。</span><span class="sxs-lookup"><span data-stu-id="3c1ba-142">This field returns an enumeration value for every record in this list.</span></span>

![選択した列挙のすべての列挙値をレコードの一覧として返すモデル マッピングのデータ ソース](./media/er-functions-text-getenumvaluebyname-example2-2.png)

<span data-ttu-id="3c1ba-144">次の図は、モデル マッピングで構成されている **VendTrans** データ ソースを示しています。</span><span class="sxs-lookup"><span data-stu-id="3c1ba-144">The following illustration shows the **VendTrans** data source that is configured in a model mapping.</span></span> <span data-ttu-id="3c1ba-145">このデータ ソースは、**VendTrans** アプリケーション テーブルから仕入先トランザクション レコードを返します。</span><span class="sxs-lookup"><span data-stu-id="3c1ba-145">This data source returns vendor transaction records from the **VendTrans** application table.</span></span> <span data-ttu-id="3c1ba-146">すべてのトランザクションの元帳タイプは、**TransType** フィールドの値によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="3c1ba-146">The ledger type of every transaction is defined by the value of the **TransType** field.</span></span>

> [!NOTE]
> <span data-ttu-id="3c1ba-147">**TransTypeTitle** フィールドは、`FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label` 式を使用して **VendTrans** データソースに対して構成されます。</span><span class="sxs-lookup"><span data-stu-id="3c1ba-147">The **TransTypeTitle** field is configured for the **VendTrans** data source by using the `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label` expression.</span></span> <span data-ttu-id="3c1ba-148">このフィールドは、この列挙値が使用可能な場合に、現在のトランザクションの列挙値のラベルをテキストとして返します。</span><span class="sxs-lookup"><span data-stu-id="3c1ba-148">This field returns the label of an enumeration value of the current transaction as text, if this enumeration value is available.</span></span> <span data-ttu-id="3c1ba-149">それ以外の場合は、空白文字列の値を返します。</span><span class="sxs-lookup"><span data-stu-id="3c1ba-149">Otherwise, it returns a blank string value.</span></span>
>
> <span data-ttu-id="3c1ba-150">**TransTypeTitle** フィールドは、データ モデルの **LedgerType** フィールドにバインドされ、データ ソースとしてデータモデルを使用するすべての ER 形式でこの情報を使用できます。</span><span class="sxs-lookup"><span data-stu-id="3c1ba-150">The **TransTypeTitle** field is bound to the **LedgerType** field of a data model that enables this information to be used in every ER format that uses the data model as a source of data.</span></span>

![仕入先トランザクションを返すモデル マッピングのデータ ソース](./media/er-functions-text-getenumvaluebyname-example2-3.png)

<span data-ttu-id="3c1ba-152">次の図は、[データ ソース デバッガー](er-debug-data-sources.md) を使用して、構成済みモデル マッピングをテストする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="3c1ba-152">The following illustration shows how you can use the [data source debugger](er-debug-data-sources.md) to test the configured model mapping.</span></span>

![データ ソース デバッガーを使用して、構成済モデル マッピングをテストする](./media/er-functions-text-getenumvaluebyname-example2-4.gif)

<span data-ttu-id="3c1ba-154">データ モデルの **LedgerType** フィールドは、期待どおりにトランザクション タイプのラベルを公開します。</span><span class="sxs-lookup"><span data-stu-id="3c1ba-154">The **LedgerType** field of a data model exposes labels of transaction types as expected.</span></span>

<span data-ttu-id="3c1ba-155">大量のトランザクション データにこのアプローチを使用する場合は、実行パフォーマンスを考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c1ba-155">If you plan to use this approach for a large amount of transactional data, you must consider execution performance.</span></span> <span data-ttu-id="3c1ba-156">詳細については、[電子申告形式の実行をトレースしてパフォーマンスの問題をトラブルシューティング](trace-execution-er-troubleshoot-perf.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3c1ba-156">For more information, see [Trace the execution of ER formats to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3c1ba-157">追加リソース</span><span class="sxs-lookup"><span data-stu-id="3c1ba-157">Additional resources</span></span>

[<span data-ttu-id="3c1ba-158">テキスト関数</span><span class="sxs-lookup"><span data-stu-id="3c1ba-158">Text functions</span></span>](er-functions-category-text.md)

[<span data-ttu-id="3c1ba-159">電子申告形式の実行をトレースしてパフォーマンスの問題をトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="3c1ba-159">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)

[<span data-ttu-id="3c1ba-160">LISTOFFIELDS ER 関数</span><span class="sxs-lookup"><span data-stu-id="3c1ba-160">LISTOFFIELDS ER function</span></span>](er-functions-list-listoffields.md)

[<span data-ttu-id="3c1ba-161">FIRSTORNULL ER 関数</span><span class="sxs-lookup"><span data-stu-id="3c1ba-161">FIRSTORNULL ER function</span></span>](er-functions-list-firstornull.md)

[<span data-ttu-id="3c1ba-162">WHERE ER 関数</span><span class="sxs-lookup"><span data-stu-id="3c1ba-162">WHERE ER function</span></span>](er-functions-list-where.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]