---
title: 検証、既定値、およびマップされていないフィールド
description: このトピックでは、データ エンティティの値を検証する方法、既定値を設定する方法、およびデータ ソース値にマップされないが、代わりに仮想または計算のデータが含まれるフィールド (マップされていないフィールド) を使用する方法について説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 4624
ms.assetid: 7ea995fa-8ea0-403d-8a68-f19993c40a6d
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d850ca2fbaa417768493c49d7da4adc2363ec08
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681172"
---
# <a name="validations-default-values-and-unmapped-fields"></a><span data-ttu-id="fd676-103">検証、既定値、およびマップされていないフィールド</span><span class="sxs-lookup"><span data-stu-id="fd676-103">Validations, default values, and unmapped fields</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd676-104">このトピックでは、データ エンティティの値を検証する方法、既定値を設定する方法、およびデータ ソース値にマップされないが、代わりに仮想または計算のデータが含まれるフィールド (マップされていないフィールド) を使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="fd676-104">This topic describes how data entity values are validated, how default values can be provided, and how to use fields that are not mapped to data source values, but instead contain virtual or computed data (unmapped fields).</span></span>

## <a name="validations"></a><span data-ttu-id="fd676-105">検証</span><span class="sxs-lookup"><span data-stu-id="fd676-105">Validations</span></span>
<span data-ttu-id="fd676-106">検証は、フィールド レベルとレコード レベルの両方でエンティティをバックアップするテーブルで定義できます。</span><span class="sxs-lookup"><span data-stu-id="fd676-106">Validations can be defined on the tables that back up entities, at both the field level and the record level.</span></span> <span data-ttu-id="fd676-107">検証は、データ エンティティ レベルで定義することもできます。</span><span class="sxs-lookup"><span data-stu-id="fd676-107">Validations can also be defined at the data entity level.</span></span>

### <a name="table-data-source-vs-entity-validation"></a><span data-ttu-id="fd676-108">テーブル (データ ソース) とエンティティ検証</span><span class="sxs-lookup"><span data-stu-id="fd676-108">Table (data source) vs. entity validation</span></span>

<span data-ttu-id="fd676-109">エンティティはテーブル (データ ソース) によって戻され、検証はフィールド レベル (**Table.validateField()**) とレコード レベル (**Table.validateWrite()**) の両方でテーブルに対して定義されます。</span><span class="sxs-lookup"><span data-stu-id="fd676-109">Entities are backed by tables (data sources), and validations are defined for these tables at both the field level (**Table.validateField()**) and the record level (**Table.validateWrite()**).</span></span> <span data-ttu-id="fd676-110">検証は、これらのテーブルを使用して構築されたデータ エンティティによって考慮されます。</span><span class="sxs-lookup"><span data-stu-id="fd676-110">The validations are respected by data entities that are built by using those tables.</span></span> <span data-ttu-id="fd676-111">これらの検証はデータ エンティティを戻すテーブルに組み込まれますが、検証はデータ エンティティ レベルで定義することもできます。</span><span class="sxs-lookup"><span data-stu-id="fd676-111">Although these validations are intrinsic to the tables that back a data entity, validations can also be defined at the data entity level.</span></span> <span data-ttu-id="fd676-112">テーブルに基づく検証と同様に、エンティティに基づく検証はフィールド レベル (**DataEntity.validateField()**) またはレコード レベル (**DataEntity.validateWrite()**) で書き込むことができます。</span><span class="sxs-lookup"><span data-stu-id="fd676-112">Like table-based validations, entity-based validations can be written at the field level (**DataEntity.validateField()**) or the record level (**DataEntity.validateWrite()**).</span></span>

### <a name="table-based-validation-behavior"></a><span data-ttu-id="fd676-113">テーブル ベースの検証動作</span><span class="sxs-lookup"><span data-stu-id="fd676-113">Table-based validation behavior</span></span>

<span data-ttu-id="fd676-114">テーブルの検証は CUD 操作の一部として自動的に実行されます。</span><span class="sxs-lookup"><span data-stu-id="fd676-114">Table validations are fired automatically as a part of the CUD operations.</span></span> <span data-ttu-id="fd676-115">**Table.ValidateField、AllowEdit、AllowEditOnCreate** フィールド レベルの検証は、データ エンティティで挿入または更新を実行する時に、自動的に発生します。</span><span class="sxs-lookup"><span data-stu-id="fd676-115">**Table.ValidateField, AllowEdit, AllowEditOnCreate** Field-level validations are fired automatically when you perform inserts or updates on the data entity.</span></span> <span data-ttu-id="fd676-116">これは、すべてのパス (X++、OData など) に当てはまります。</span><span class="sxs-lookup"><span data-stu-id="fd676-116">This is true for all paths (X++, OData, and so on).</span></span> <span data-ttu-id="fd676-117">これらの検証は、エンティティから個々のデータ ソースにフィールドがマップされるマッピング処理中に行われます。</span><span class="sxs-lookup"><span data-stu-id="fd676-117">These validations occur during the mapping process, when fields are mapped from an entity to individual data sources.</span></span>

<span data-ttu-id="fd676-118">[![redo1](./media/redo1-1024x582.png)](./media/redo1.png)</span><span class="sxs-lookup"><span data-stu-id="fd676-118">[![redo1](./media/redo1-1024x582.png)](./media/redo1.png)</span></span>

<span data-ttu-id="fd676-119">データ エンティティからフィールド値がマップされたデータ ソース フィールドにコピーされた後、フィールドの検証は設定されたフィールドで実行されます。</span><span class="sxs-lookup"><span data-stu-id="fd676-119">After the field values from the data entity are copied to mapped data source fields, field validations are run on the set fields.</span></span> <span data-ttu-id="fd676-120">検証にはテーブル レベルの **validateField** が含まれ、**AllowEdit** および **AllowEditOnCreate** を検証します。</span><span class="sxs-lookup"><span data-stu-id="fd676-120">Validations include table-level **validateField**, which validates **AllowEdit** and **AllowEditOnCreate**.</span></span> <span data-ttu-id="fd676-121">エラーにより検証が失敗した場合、残りのフィールドの検証が続行されます。</span><span class="sxs-lookup"><span data-stu-id="fd676-121">If a validation fails because of an error, validation for the remaining fields continues.</span></span> <span data-ttu-id="fd676-122">最後に、データ ソースのいずれかの検証プロセス中に発生したエラーが発生したかどうかを、検証によって確認します。</span><span class="sxs-lookup"><span data-stu-id="fd676-122">Finally, validation checks whether any error occurred during the validation process for any of the data sources.</span></span> <span data-ttu-id="fd676-123">エラーがあった場合、この時点でプロセス エラーが発生するようになり、テーブル レベルの **validateWrite()** は呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="fd676-123">If there was an error, the process errors out at this point, and table-level **validateWrite()** isn't called.</span></span> <span data-ttu-id="fd676-124">バックエンド テーブルに対して **validateField** をスキップするには、コンシューマーは **DataEntity.skipDataSourceValidateField(Int \_DataEntityFieldId, ブール値 \_skip)** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fd676-124">To skip **validateField** for a back-end table, a consumer can call **DataEntity.skipDataSourceValidateField(Int \_DataEntityFieldId, Boolean \_skip)**.</span></span> <span data-ttu-id="fd676-125">このメソッドのフィールド ID は、データ エンティティにマップされたフィールドのフィールド ID であり、フィールドに、バックエンド テーブルのフィールドではないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="fd676-125">Note that the field ID for this method is the field ID of the data-entity mapped field, not the back-end table field.</span></span> <span data-ttu-id="fd676-126">次の API を使用することによって、コンシューマーに関係なく、特定のフィールドの検証をスキップできます。</span><span class="sxs-lookup"><span data-stu-id="fd676-126">By using the following API, you can skip validation for a particular field, regardless of the consumer.</span></span>

<span data-ttu-id="fd676-127">[![Over9](./media/over9.png)](./media/over9.png)</span><span class="sxs-lookup"><span data-stu-id="fd676-127">[![Over9](./media/over9.png)](./media/over9.png)</span></span>

<span data-ttu-id="fd676-128">**Table.ValidateWrite** レコード レベル **Table.ValidateWrite** バックエンドテーブルに定義されている検証は、データ エンティティの挿入および更新を実行すると自動的に発生します。</span><span class="sxs-lookup"><span data-stu-id="fd676-128">**Table.ValidateWrite** Record-level **ValidateWrite** validations that are defined in back-end tables are fired automatically when you perform data-entity inserts and updates.</span></span> <span data-ttu-id="fd676-129">これは、すべてのパス (X++、OData など) に当てはまります。</span><span class="sxs-lookup"><span data-stu-id="fd676-129">This is true for all paths (X++, OData, and so on).</span></span> <span data-ttu-id="fd676-130">これらの検証は、実際の挿入または更新がデータ ソースに適用される直前に行われます。</span><span class="sxs-lookup"><span data-stu-id="fd676-130">These validations occur just before the actual insert or update is applied to the data source.</span></span> <span data-ttu-id="fd676-131">検証が失敗すると、エラーが発生し、その他のデータ ソースのプロセスが停止されます。</span><span class="sxs-lookup"><span data-stu-id="fd676-131">If the validation fails, an error is thrown, and the process stops for other data sources.</span></span> 

![redo2](./media/redo2-1024x636.png)

<span data-ttu-id="fd676-133">データ エンティティのすべてのバックエンド テーブルに対して **validateWrite** をスキップするには、コンシューマーは **DataEntity.skipDataSourceValidateWrite(ブール値 \_skip)** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fd676-133">To skip **validateWrite** for all back-end tables for a data entity, a consumer can call **DataEntity.skipDataSourceValidateWrite(Boolean \_skip)**.</span></span> <span data-ttu-id="fd676-134">このメソッドは、すべてのデータソースに対して **validateWrite** をオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="fd676-134">This method turns **validateWrite** on or off for all data sources.</span></span> <span data-ttu-id="fd676-135">次の API を使用することによって、コンシューマーに関係なく、特定のフィールドの検証をスキップできます。</span><span class="sxs-lookup"><span data-stu-id="fd676-135">By using the following API, you can skip validation for a particular field, regardless of the consumer.</span></span>

<span data-ttu-id="fd676-136">[![Over10](./media/over10.png)](./media/over10.png)</span><span class="sxs-lookup"><span data-stu-id="fd676-136">[![Over10](./media/over10.png)](./media/over10.png)</span></span>

<span data-ttu-id="fd676-137">バック エンド テーブルに定義されている **Table.ValidateDelete** レコード レベル **ValidateDelete** 検証は、データ エンティティの削除を実行すると自動的に発生します。</span><span class="sxs-lookup"><span data-stu-id="fd676-137">**Table.ValidateDelete** Record-level **ValidateDelete** validations that are defined in back-end tables are fired automatically when you perform data entity deletes.</span></span> <span data-ttu-id="fd676-138">これは、すべてのパス (X++、OData など) に当てはまります。</span><span class="sxs-lookup"><span data-stu-id="fd676-138">This is true for all paths (X++, OData, and so on).</span></span> <span data-ttu-id="fd676-139">これらの検証は、削除がデータ ソースに適用される直前に行われます。</span><span class="sxs-lookup"><span data-stu-id="fd676-139">These validations occur just before the delete is applied to the data source.</span></span> <span data-ttu-id="fd676-140">検証が失敗すると、エラーが発生し、その他のデータ ソースのプロセスが停止されます。</span><span class="sxs-lookup"><span data-stu-id="fd676-140">If the validation fails, an error is thrown, and the process stops for other data sources.</span></span>

<span data-ttu-id="fd676-141">[![Over11](./media/over11.png)](./media/over11.png)</span><span class="sxs-lookup"><span data-stu-id="fd676-141">[![Over11](./media/over11.png)](./media/over11.png)</span></span>

<span data-ttu-id="fd676-142">データ エンティティのすべてのバックエンド テーブルに対して **validateDelete** をスキップするには、コンシューマーは **DataEntity.skipDataSourceValidateDelete(ブール値 \_skip)** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fd676-142">To skip **validateDelete** for all back-end tables for a data entity, a consumer can call **DataEntity.skipDataSourceValidateDelete(Boolean \_skip)**.</span></span> <span data-ttu-id="fd676-143">このメソッドは、すべてのデータソースに対して **validateDelete** をオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="fd676-143">This method turns **validateDelete** on or off for all data sources.</span></span> <span data-ttu-id="fd676-144">次の API を使用すると、コンシューマーに関係なく、特定のデータ ソースの検証をスキップできます。</span><span class="sxs-lookup"><span data-stu-id="fd676-144">By using the following API, you can skip validation for a particular data source, regardless of the consumer.</span></span>

<span data-ttu-id="fd676-145">[![Over12](./media/over12.png)](./media/over12.png)</span><span class="sxs-lookup"><span data-stu-id="fd676-145">[![Over12](./media/over12.png)](./media/over12.png)</span></span>

### <a name="entity-based-validation-behavior"></a><span data-ttu-id="fd676-146">エンティティ ベースの検証動作</span><span class="sxs-lookup"><span data-stu-id="fd676-146">Entity-based validation behavior</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="fd676-147">検証</span><span class="sxs-lookup"><span data-stu-id="fd676-147">Validation</span></span></th>
<th><span data-ttu-id="fd676-148">ターゲット</span><span class="sxs-lookup"><span data-stu-id="fd676-148">Target</span></span></th>
<th><span data-ttu-id="fd676-149">呼び出し側</span><span class="sxs-lookup"><span data-stu-id="fd676-149">Caller</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fd676-150">DataEntity.ValidateField</span><span class="sxs-lookup"><span data-stu-id="fd676-150">DataEntity.ValidateField</span></span></td>
<td><ul>
<li><span data-ttu-id="fd676-151">データ型</span><span class="sxs-lookup"><span data-stu-id="fd676-151">Data types</span></span></li>
<li><span data-ttu-id="fd676-152">必須の関係 (テーブルおよび拡張データ型 [EDT] の両方)</span><span class="sxs-lookup"><span data-stu-id="fd676-152">Mandatory relationships (both tables and extended data types [EDTs])</span></span></li>
<li><span data-ttu-id="fd676-153">カスタム検証</span><span class="sxs-lookup"><span data-stu-id="fd676-153">Any custom validation</span></span></li>
<li><span data-ttu-id="fd676-154">基本マップのテーブル フィールドの <strong>validateField</strong> を呼び出さないでください。</span><span class="sxs-lookup"><span data-stu-id="fd676-154">Doesn't call <strong>validateField</strong> for underlying mapped table fields</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="fd676-155">OData から自動的に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="fd676-155">Is called automatically from OData</span></span></li>
<li><span data-ttu-id="fd676-156">フィールドが変更されたときに、フォーム エンジンで呼び出されます</span><span class="sxs-lookup"><span data-stu-id="fd676-156">Is called by the form engine when a field is modified</span></span></li>
<li><span data-ttu-id="fd676-157">挿入/更新が X++ コードから発生した場合は、自動的に呼び出されません</span><span class="sxs-lookup"><span data-stu-id="fd676-157">Isn't called automatically if an insert/update is fired from X++ code</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="fd676-158">DataEntity.ValidateWrite</span><span class="sxs-lookup"><span data-stu-id="fd676-158">DataEntity.ValidateWrite</span></span></td>
<td><ul>
<li><span data-ttu-id="fd676-159">必須の列</span><span class="sxs-lookup"><span data-stu-id="fd676-159">Mandatory columns</span></span></li>
<li><span data-ttu-id="fd676-160">関係 (テーブルおよび EDT の両方)</span><span class="sxs-lookup"><span data-stu-id="fd676-160">Relationships (both tables and EDTs)</span></span></li>
<li><span data-ttu-id="fd676-161">カスタム検証</span><span class="sxs-lookup"><span data-stu-id="fd676-161">Any custom validation</span></span></li>
<li><span data-ttu-id="fd676-162">基本テーブルのテーブル レベル <strong>validateWrite</strong> を呼び出さないでください。</span><span class="sxs-lookup"><span data-stu-id="fd676-162">Doesn't call table-level <strong>validateWrite</strong> for underlying tables</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="fd676-163">OData から自動的に呼び出されます</span><span class="sxs-lookup"><span data-stu-id="fd676-163">Is called automatically from OData</span></span></li>
<li><span data-ttu-id="fd676-164">レコードが保存されたときに、フォーム エンジンで呼び出されます</span><span class="sxs-lookup"><span data-stu-id="fd676-164">Is called by the form engine when a record is saved.</span></span></li>
<li><span data-ttu-id="fd676-165">挿入/更新が X++ コードから発生した場合は、自動的に呼び出されません</span><span class="sxs-lookup"><span data-stu-id="fd676-165">Isn't called automatically if an insert/update is fired from X++ code</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="fd676-166">DataEntity.ValidateDelete</span><span class="sxs-lookup"><span data-stu-id="fd676-166">DataEntity.ValidateDelete</span></span></td>
<td><ul>
<li><span data-ttu-id="fd676-167">DeleteActions</span><span class="sxs-lookup"><span data-stu-id="fd676-167">DeleteActions</span></span></li>
<li><span data-ttu-id="fd676-168">カスタム検証</span><span class="sxs-lookup"><span data-stu-id="fd676-168">Any custom validation</span></span></li>
<li><span data-ttu-id="fd676-169">基本テーブルの テーブル レベル <strong>validateDelete</strong> を呼び出さないでください。</span><span class="sxs-lookup"><span data-stu-id="fd676-169">Doesn't call table-level <strong>validateDelete</strong> for underlying tables</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="fd676-170">OData から自動的に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="fd676-170">Is called automatically from OData.</span></span></li>
<li><span data-ttu-id="fd676-171">レコードが削除されたときに、フォーム エンジンで呼び出されます</span><span class="sxs-lookup"><span data-stu-id="fd676-171">Is called by the form engine when a record is deleted</span></span></li>
<li><span data-ttu-id="fd676-172">削除が X++ コードから発生した場合は、自動的に呼び出されません</span><span class="sxs-lookup"><span data-stu-id="fd676-172">Isn't called automatically if a delete is fired from X++ code</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="defaults"></a><span data-ttu-id="fd676-173">既定</span><span class="sxs-lookup"><span data-stu-id="fd676-173">Defaults</span></span>
<span data-ttu-id="fd676-174">初期化と行には既定値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="fd676-174">Default values can be provided for initializations and rows.</span></span>

### <a name="initializations"></a><span data-ttu-id="fd676-175">初期化</span><span class="sxs-lookup"><span data-stu-id="fd676-175">Initializations</span></span>

<span data-ttu-id="fd676-176">**DataEntity.initValue:** データ エンティティは、既定値で、エンティティ レベル **initValue** に存在するカスタム ロジックを使用して初期化されます。</span><span class="sxs-lookup"><span data-stu-id="fd676-176">**DataEntity.initValue:** A data entity is initialized with default values and by using any custom logic that is present in entity-level **initValue**.</span></span> <span data-ttu-id="fd676-177">このメソッドは、X++ からのデータ エンティティに対して挿入または更新が実行されたときに自動的に呼び出されることはありません。</span><span class="sxs-lookup"><span data-stu-id="fd676-177">This method isn't called automatically when an insert or update is performed on a data entity from X++.</span></span> <span data-ttu-id="fd676-178">必要な場合に明示的に呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd676-178">It must be called explicitly if it's required.</span></span> <span data-ttu-id="fd676-179">このメソッドは、新しいレコードが作成されるときにフォーム エンジンによって自動的に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="fd676-179">The method is called automatically by the form engine when a new record is created.</span></span> <span data-ttu-id="fd676-180">**DataEntity.initValue** は、データ エンティティで使用されるバック エンド テーブルの **initValue** メソッドを呼び出しません。</span><span class="sxs-lookup"><span data-stu-id="fd676-180">**DataEntity.initValue** doesn't call the **initValue** method for back-end tables that are used in the data entity.</span></span> <span data-ttu-id="fd676-181">**Table.initValue:** テーブル レベル **initValue** は、バック エンド テーブル定義に従って、データ エンティティの挿入を実行するときに発生します。</span><span class="sxs-lookup"><span data-stu-id="fd676-181">**Table.initValue:** Table-level **initValue**, as defined for back-end tables, is fired when you perform a data entity insert.</span></span> <span data-ttu-id="fd676-182">これは、すべてのパス (X++、OData など) に当てはまります。</span><span class="sxs-lookup"><span data-stu-id="fd676-182">This is true for all paths (X++, OData, and so on).</span></span> <span data-ttu-id="fd676-183">**Table.initValue** はエンティティがデータ ソース フィールドにマップされる直前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="fd676-183">**Table.initValue** is run just before the entity is mapped to data source fields.</span></span>

<span data-ttu-id="fd676-184">[![Over13](./media/over13.png)](./media/over13.png)</span><span class="sxs-lookup"><span data-stu-id="fd676-184">[![Over13](./media/over13.png)](./media/over13.png)</span></span>

<span data-ttu-id="fd676-185">データ エンティティのすべてのバックエンド テーブルに対してエンティティ レベルの **initValue** をスキップするには、コンシューマーは **DataEntity.skipDataSourceInitValue(ブール値 \_skip)** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fd676-185">To skip entity-level **initValue** for all back-end tables for a data entity, a consumer can call **DataEntity.skipDataSourceInitValue(Boolean \_skip)**.</span></span> <span data-ttu-id="fd676-186">このメソッドは、すべてのデータソースに対して **initValue** をオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="fd676-186">This method turns **initValue** on or off for all data sources.</span></span> <span data-ttu-id="fd676-187">次の API を使用することによって、コンシューマーに関係なく、特定のフィールドの **initValue** をスキップできます。</span><span class="sxs-lookup"><span data-stu-id="fd676-187">By using the following API, you can skip **initValue** for a particular field, regardless of the consumer.</span></span>

<span data-ttu-id="fd676-188">[![Capturea](./media/capturea.png)](./media/capturea.png)</span><span class="sxs-lookup"><span data-stu-id="fd676-188">[![Capturea](./media/capturea.png)](./media/capturea.png)</span></span>

### <a name="defaultrow"></a><span data-ttu-id="fd676-189">DefaultRow</span><span class="sxs-lookup"><span data-stu-id="fd676-189">DefaultRow</span></span>

<span data-ttu-id="fd676-190">**DataEntity.DefaultRow: DataEntity.DefaultRow** は、**defaultField** および **getDefaultingDependencies** と組み合わせて使用され、既定値を提供します。</span><span class="sxs-lookup"><span data-stu-id="fd676-190">**DataEntity.DefaultRow: DataEntity.DefaultRow** is used in conjunction with **defaultField** and **getDefaultingDependencies** to provide defaults.</span></span> <span data-ttu-id="fd676-191">X++ またはフォーム エンジンによって自動的に呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="fd676-191">It isn't called automatically by X++ or the form engine.</span></span> <span data-ttu-id="fd676-192">**Table.DefaultRow: Table.DefaultRow** は、データソースの挿入と検証の前に、マッピングが完了した後データソースに対して自動的に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="fd676-192">**Table.DefaultRow: Table.DefaultRow** is called automatically for each data source after mapping is completed, and before the insert and validation on the data source.</span></span>

<span data-ttu-id="fd676-193">[![Captureb](./media/captureb.png)](./media/captureb.png)</span><span class="sxs-lookup"><span data-stu-id="fd676-193">[![Captureb](./media/captureb.png)](./media/captureb.png)</span></span>

## <a name="unmapped-fields"></a><span data-ttu-id="fd676-194">マップされていないフィールド</span><span class="sxs-lookup"><span data-stu-id="fd676-194">Unmapped fields</span></span>
<span data-ttu-id="fd676-195">データ エンティティは、データ ソースのフィールドに直接マップされているフィールドに *マップされていない* フィールドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="fd676-195">A data entity can have *unmapped* fields in addition those fields that are directly mapped to fields of the data sources.</span></span> <span data-ttu-id="fd676-196">マップされていないフィールドの値を生成するメカニズムは 2 つあります。</span><span class="sxs-lookup"><span data-stu-id="fd676-196">There are two mechanisms for generating values for unmapped fields:</span></span>

- <span data-ttu-id="fd676-197">カスタム X++ コード</span><span class="sxs-lookup"><span data-stu-id="fd676-197">Custom X++ code</span></span>
- <span data-ttu-id="fd676-198">Microsoft SQL Server によって実行される SQL</span><span class="sxs-lookup"><span data-stu-id="fd676-198">SQL that is run by Microsoft SQL Server</span></span>

<span data-ttu-id="fd676-199">マップされていない2種類のフィールドは、*仮想* と *計算* です。</span><span class="sxs-lookup"><span data-stu-id="fd676-199">The two types of unmapped fields are *virtual* and *computed*.</span></span> <span data-ttu-id="fd676-200">マップされていないフィールドは常に読み取り操作をサポートしますが、機能仕様では、書き込み操作をサポートするための開発作業は必要とされない場合があります。</span><span class="sxs-lookup"><span data-stu-id="fd676-200">Unmapped fields always support read actions, but the feature specification might not require any development effort to support write actions.</span></span>

<span data-ttu-id="fd676-201">**仮想フィールド**</span><span class="sxs-lookup"><span data-stu-id="fd676-201">**Virtual field**</span></span>

- <span data-ttu-id="fd676-202">保持されないフィールド。</span><span class="sxs-lookup"><span data-stu-id="fd676-202">A non-persisted field.</span></span>
- <span data-ttu-id="fd676-203">カスタム X++ コードによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="fd676-203">Controlled by custom X++ code.</span></span>
- <span data-ttu-id="fd676-204">読み取り/書き込みは、カスタム X++ コードを通じて発生します。</span><span class="sxs-lookup"><span data-stu-id="fd676-204">Read and writes occur through custom X++ code.</span></span>
- <span data-ttu-id="fd676-205">通常は X++ コードを用いて計算される入力値に使用され、計算された列によって置き換わることはできません。</span><span class="sxs-lookup"><span data-stu-id="fd676-205">Typically used for intake values that are calculated by using X++ code and can't be replaced by computed columns.</span></span>

<span data-ttu-id="fd676-206">**計算フィールド**</span><span class="sxs-lookup"><span data-stu-id="fd676-206">**Computed field**</span></span>

- <span data-ttu-id="fd676-207">値は、SQL ビューの計算列によって生成されます。</span><span class="sxs-lookup"><span data-stu-id="fd676-207">The value is generated by an SQL view computed column.</span></span>
- <span data-ttu-id="fd676-208">読み取り中に、データは SQL によって計算され、ビューから直接フェッチされます。</span><span class="sxs-lookup"><span data-stu-id="fd676-208">During reads, data is computed by SQL and fetched directly from the view.</span></span>
- <span data-ttu-id="fd676-209">書き込みについては、カスタム X++ コードは入力値を解析し、データ エンティティの通常のフィールドに解析された値を書き込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd676-209">For writes, custom X++ code must parse the input value and then write the parsed values to the regular fields of the data entity.</span></span> <span data-ttu-id="fd676-210">値はエンティティのデータ ソースの通常のフィールドに格納されます。</span><span class="sxs-lookup"><span data-stu-id="fd676-210">The values are stored in the regular fields of the data sources of the entity.</span></span>
- <span data-ttu-id="fd676-211">ほとんどの場合の読み取りに使用されます。</span><span class="sxs-lookup"><span data-stu-id="fd676-211">Used mostly for reads.</span></span>
- <span data-ttu-id="fd676-212">計算された列は SQL Server レベルで計算されている一方、仮想フィールドは、X++ の行ごとに計算された行であるため、可能な限り仮想フィールドではなく計算された列を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="fd676-212">It's a good idea to use computed columns instead of virtual fields whenever you can, because computed columns are computed at the SQL Server level, whereas virtual fields are computed row by row in X++.</span></span>

### <a name="properties-of-unmapped-fields"></a><span data-ttu-id="fd676-213">マップされていないフィールドのプロパティ</span><span class="sxs-lookup"><span data-stu-id="fd676-213">Properties of unmapped fields</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="fd676-214">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="fd676-214">Category</span></span></th>
<th><span data-ttu-id="fd676-215">氏名</span><span class="sxs-lookup"><span data-stu-id="fd676-215">Name</span></span></th>
<th><span data-ttu-id="fd676-216">種類</span><span class="sxs-lookup"><span data-stu-id="fd676-216">Type</span></span></th>
<th><span data-ttu-id="fd676-217">既定値</span><span class="sxs-lookup"><span data-stu-id="fd676-217">Default value</span></span></th>
<th><span data-ttu-id="fd676-218">動作</span><span class="sxs-lookup"><span data-stu-id="fd676-218">Behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fd676-219">データ</span><span class="sxs-lookup"><span data-stu-id="fd676-219">Data</span></span></td>
<td><span data-ttu-id="fd676-220">IsComputedField</span><span class="sxs-lookup"><span data-stu-id="fd676-220">IsComputedField</span></span></td>
<td><span data-ttu-id="fd676-221">NoYes</span><span class="sxs-lookup"><span data-stu-id="fd676-221">NoYes</span></span></td>
<td><span data-ttu-id="fd676-222">有</span><span class="sxs-lookup"><span data-stu-id="fd676-222">Yes</span></span></td>
<td><ul>
<li><span data-ttu-id="fd676-223"><strong>はい:</strong> フィールドは、SQL ビューの計算済み列として同期されます。</span><span class="sxs-lookup"><span data-stu-id="fd676-223"><strong>Yes:</strong> The field is synchronized as a SQL view computed column.</span></span> <span data-ttu-id="fd676-224">X++ メソッドは列の SQL 定義文字列を計算する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd676-224">An X++ method is required to compute the SQL definition string for the column.</span></span> <span data-ttu-id="fd676-225">仮想列の定義は静的であり、エンティティが同期されているときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="fd676-225">The virtual column definition is static and is used when the entity is synchronized.</span></span> <span data-ttu-id="fd676-226">その後は、X++ メソッドは、実行時に呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="fd676-226">After that, the X++ method isn't called at run time.</span></span></li>
<li><span data-ttu-id="fd676-227"><strong>いいえ:</strong> フィールドは、入庫および出荷の値がカスタム コードによって完全に制御される真の仮想フィールドです。</span><span class="sxs-lookup"><span data-stu-id="fd676-227"><strong>No:</strong> The field is a true virtual field, where inbound and outbound values are fully controlled through custom code.</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="fd676-228">データ</span><span class="sxs-lookup"><span data-stu-id="fd676-228">Data</span></span></td>
<td><span data-ttu-id="fd676-229">ComputedFieldMethod</span><span class="sxs-lookup"><span data-stu-id="fd676-229">ComputedFieldMethod</span></span></td>
<td><span data-ttu-id="fd676-230">文字列</span><span class="sxs-lookup"><span data-stu-id="fd676-230">String</span></span></td>
<td></td>
<td><span data-ttu-id="fd676-231">X++ の静的 <strong>DataEntity</strong> メソッドは、フィールド定義を生成する SQL 式の構築に使用されます。</span><span class="sxs-lookup"><span data-stu-id="fd676-231">A static <strong>DataEntity</strong> method in X++ is used to build the SQL expression that generates the field definition.</span></span> <span data-ttu-id="fd676-232"><strong>IsComputedField</strong> プロパティが <strong>いいえ</strong> に設定されている場合、このプロパティは無効で無関係です。</span><span class="sxs-lookup"><span data-stu-id="fd676-232">This property is disabled and irrelevant if the <strong>IsComputedField</strong> property is set to <strong>No</strong>.</span></span> <span data-ttu-id="fd676-233">このメソッドは、<strong>IsComputedField</strong> プロパティが <strong>はい</strong> に設定されている場合に必要です。</span><span class="sxs-lookup"><span data-stu-id="fd676-233">The method is required if the <strong>IsComputedField</strong> property is set to <strong>Yes</strong>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fd676-234">データ</span><span class="sxs-lookup"><span data-stu-id="fd676-234">Data</span></span></td>
<td><span data-ttu-id="fd676-235">ExtendedDataType</span><span class="sxs-lookup"><span data-stu-id="fd676-235">ExtendedDataType</span></span></td>
<td><span data-ttu-id="fd676-236">文字列</span><span class="sxs-lookup"><span data-stu-id="fd676-236">String</span></span></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

### <a name="unmapped-field-comparison"></a><span data-ttu-id="fd676-237">マップされていないフィールドの比較</span><span class="sxs-lookup"><span data-stu-id="fd676-237">Unmapped field comparison</span></span>

<table>
<thead>
<tr>
<th></th>
<th><span data-ttu-id="fd676-238">仮想フィールド</span><span class="sxs-lookup"><span data-stu-id="fd676-238">Virtual field</span></span></th>
<th><span data-ttu-id="fd676-239">計算フィールド</span><span class="sxs-lookup"><span data-stu-id="fd676-239">Computed field</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fd676-240">メタデータのプロパティ</span><span class="sxs-lookup"><span data-stu-id="fd676-240">Metadata properties</span></span></td>
<td><span data-ttu-id="fd676-241">No と算出されます</span><span class="sxs-lookup"><span data-stu-id="fd676-241">Is computed = No</span></span></td>
<td><ul>
<li><span data-ttu-id="fd676-242">計算済み = はいとなります。</span><span class="sxs-lookup"><span data-stu-id="fd676-242">Is Computed = Yes</span></span></li>
<li><span data-ttu-id="fd676-243">計算フィールド メソッド = 静的メソッド</span><span class="sxs-lookup"><span data-stu-id="fd676-243">Computed Field Method = static method</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="fd676-244">既読</span><span class="sxs-lookup"><span data-stu-id="fd676-244">Read</span></span></td>
<td><ul>
<li><span data-ttu-id="fd676-245">X++ (override <strong>postLoad</strong>)</span><span class="sxs-lookup"><span data-stu-id="fd676-245">X++ (override <strong>postLoad</strong>)</span></span></li>
<li><span data-ttu-id="fd676-246">1 行ずつ</span><span class="sxs-lookup"><span data-stu-id="fd676-246">Row by row</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="fd676-247">SQL 計算列</span><span class="sxs-lookup"><span data-stu-id="fd676-247">SQL computed column</span></span></li>
<li><span data-ttu-id="fd676-248">セット ベースの読み取り可能</span><span class="sxs-lookup"><span data-stu-id="fd676-248">Set-based read possible</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="fd676-249">書き込み</span><span class="sxs-lookup"><span data-stu-id="fd676-249">Write</span></span></td>
<td><span data-ttu-id="fd676-250">X++ (override <strong>mapEntityToDataSource</strong>)</span><span class="sxs-lookup"><span data-stu-id="fd676-250">X++ (override <strong>mapEntityToDataSource</strong>)</span></span></td>
<td><span data-ttu-id="fd676-251">X++ (override <strong>mapEntityToDataSource</strong>)</span><span class="sxs-lookup"><span data-stu-id="fd676-251">X++ (override <strong>mapEntityToDataSource</strong>)</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fd676-252">メリット</span><span class="sxs-lookup"><span data-stu-id="fd676-252">Advantages</span></span></td>
<td><ul>
<li><span data-ttu-id="fd676-253">スキーマにバインドされていないため公開契約は同じですが、実装が変更される可能性があります</span><span class="sxs-lookup"><span data-stu-id="fd676-253">Unbound to the schema, keeps the public contract the same, but the implementation can change</span></span></li>
<li><span data-ttu-id="fd676-254">X++ メソッドの呼び出し</span><span class="sxs-lookup"><span data-stu-id="fd676-254">Call X++ methods</span></span></li>
</ul></td>
<td><span data-ttu-id="fd676-255">高速読み込みで、大きなエクスポートはビューから直接発生が可能</span><span class="sxs-lookup"><span data-stu-id="fd676-255">Faster reads, large export can occur directly from the view</span></span></td>
</tr>
</tbody>
</table>

### <a name="examples"></a><span data-ttu-id="fd676-256">例</span><span class="sxs-lookup"><span data-stu-id="fd676-256">Examples</span></span>

<span data-ttu-id="fd676-257">次のテーブルは、**UnitOfMeasure** のリレーションシップが存在する場合の計算例を示し、マップされていないフィールドにその値を表示します。</span><span class="sxs-lookup"><span data-stu-id="fd676-257">The following table provides a computed example if a **UnitOfMeasure** relationship exists, and displays that in an unmapped field.</span></span>

| <span data-ttu-id="fd676-258">仮想フィールド</span><span class="sxs-lookup"><span data-stu-id="fd676-258">Virtual field</span></span> | <span data-ttu-id="fd676-259">計算フィールド</span><span class="sxs-lookup"><span data-stu-id="fd676-259">Computed field</span></span> |
|---------------|----------------|
| <span data-ttu-id="fd676-260">postLoad() で、*// UnitOfMeasureInternalCode.UnitOfMeasure//Set hasFixedInternalCode 値に、フィールドに基づいてレコードが存在するかどうかを確認します* (this.UnitOfMeasure)this.HasFixedInternalCodeVirtual = NoYes::Yes; else this.HasFixedInternalCodeVirtual = NoYes::No; の場合</span><span class="sxs-lookup"><span data-stu-id="fd676-260">On postLoad()*//Check to see if record exists in UnitOfMeasureInternalCode.UnitOfMeasure//Set hasFixedInternalCode value based on the field* if(this.UnitOfMeasure)this.HasFixedInternalCodeVirtual = NoYes::Yes; else this.HasFixedInternalCodeVirtual = NoYes::No;</span></span> | <span data-ttu-id="fd676-261">ComputedFieldMethod() で *// 任意の SQL 計算された列の明細書 (T2.RECID が NULL の場合は 0 ELSE 1)INTとして)*</span><span class="sxs-lookup"><span data-stu-id="fd676-261">On computedFieldMethod()*//Desired SQL computed column statement(CASE WHEN T2.RECID IS NULL THEN 0 ELSE 1 END) AS INT)*</span></span> |
