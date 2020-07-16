---
title: xRecord クラス
description: このトピックでは、xRecord クラスについて説明します。
author: robinarh
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6332b76279e6c0f29fa4e58d0b70eb46d33c8049
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502761"
---
# <a name="class-xrecord"></a><span data-ttu-id="fce03-103">クラス xRecord</span><span class="sxs-lookup"><span data-stu-id="fce03-103">Class xRecord</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class xRecord extends Object
```

## <a name="remarks"></a><span data-ttu-id="fce03-104">備考</span><span class="sxs-lookup"><span data-stu-id="fce03-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="fce03-105">例</span><span class="sxs-lookup"><span data-stu-id="fce03-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="fce03-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="fce03-106">Methods</span></span>

| <span data-ttu-id="fce03-107">方法</span><span class="sxs-lookup"><span data-stu-id="fce03-107">Method</span></span>                                                                                                                     | <span data-ttu-id="fce03-108">説明</span><span class="sxs-lookup"><span data-stu-id="fce03-108">Description</span></span>                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fce03-109">public boolean aosValidateDelete()</span><span class="sxs-lookup"><span data-stu-id="fce03-109">public boolean aosValidateDelete()</span></span>                                                                                         | <span data-ttu-id="fce03-110">サーバー上で、指定されたレコードをテーブルから削除できることを検証します。</span><span class="sxs-lookup"><span data-stu-id="fce03-110">Validates on the server that the specified record can be deleted from a table.</span></span>                                                 |
| <span data-ttu-id="fce03-111">public boolean aosValidateInsert()</span><span class="sxs-lookup"><span data-stu-id="fce03-111">public boolean aosValidateInsert()</span></span>                                                                                         | <span data-ttu-id="fce03-112">サーバー上で、指定されたレコードを挿入できることを検証します。</span><span class="sxs-lookup"><span data-stu-id="fce03-112">Validates on the server that the specified record can be inserted.</span></span>                                                             |
| <span data-ttu-id="fce03-113">public boolean aosValidateRead()</span><span class="sxs-lookup"><span data-stu-id="fce03-113">public boolean aosValidateRead()</span></span>                                                                                           | <span data-ttu-id="fce03-114">サーバー上で、指定されたレコードを読み取れることを検証します。</span><span class="sxs-lookup"><span data-stu-id="fce03-114">Validates on the server that the specified record can be read.</span></span>                                                                 |
| <span data-ttu-id="fce03-115">public boolean aosValidateUpdate()</span><span class="sxs-lookup"><span data-stu-id="fce03-115">public boolean aosValidateUpdate()</span></span>                                                                                         | <span data-ttu-id="fce03-116">サーバー上で、指定されたレコードを更新できることを検証します。</span><span class="sxs-lookup"><span data-stu-id="fce03-116">Validates on the server that the specified record can be updated.</span></span>                                                              |
| <span data-ttu-id="fce03-117">public container buf2con(\[boolean packOrigBuffer\])</span><span class="sxs-lookup"><span data-stu-id="fce03-117">public container buf2con(\[boolean packOrigBuffer\])</span></span>                                                                       | <span data-ttu-id="fce03-118">X++ コンテナーに xRecord インスタンスのテーブル バッファーをパックします。</span><span class="sxs-lookup"><span data-stu-id="fce03-118">Packs the table buffers of an xRecord instance into an X++ container.</span></span>                                                          |
| <span data-ttu-id="fce03-119">public boolean canSubmitToWorkflow(\[str workflowType\])</span><span class="sxs-lookup"><span data-stu-id="fce03-119">public boolean canSubmitToWorkflow(\[str workflowType\])</span></span>                                                                   | <span data-ttu-id="fce03-120">ワークフローへの送信が可能かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="fce03-120">Indicates whether submission to workflow is possible.</span></span>                                                                          |
| <span data-ttu-id="fce03-121">public str caption()</span><span class="sxs-lookup"><span data-stu-id="fce03-121">public str caption()</span></span>                                                                                                       | <span data-ttu-id="fce03-122">テーブルのキャプション プロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-122">Gets and sets the caption property of a table.</span></span>                                                                                 |
| <span data-ttu-id="fce03-123">public boolean checkInvalidFieldAccess(\[boolean checkInvalidFieldAccess\])</span><span class="sxs-lookup"><span data-stu-id="fce03-123">public boolean checkInvalidFieldAccess(\[boolean checkInvalidFieldAccess\])</span></span>                                                | <span data-ttu-id="fce03-124">無効なフィールド アクセスを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-124">Gets and sets invalid field access.</span></span>                                                                                            |
| <span data-ttu-id="fce03-125">public boolean checkRecord(\[boolean checkMandatoryFields\])</span><span class="sxs-lookup"><span data-stu-id="fce03-125">public boolean checkRecord(\[boolean checkMandatoryFields\])</span></span>                                                               | <span data-ttu-id="fce03-126">必須フィールドをチェックするかどうかを示すプロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-126">Gets and sets the property that indicates whether to check mandatory fields.</span></span>                                                   |
| <span data-ttu-id="fce03-127">public boolean checkRestrictedDeleteActions(\[boolean checkRestrictedDeleteActions\])</span><span class="sxs-lookup"><span data-stu-id="fce03-127">public boolean checkRestrictedDeleteActions(\[boolean checkRestrictedDeleteActions\])</span></span>                                      | <span data-ttu-id="fce03-128">レコードが削除されるかどうかを示すプロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-128">Gets and sets the property that indicates whether a record can be deleted.</span></span>                                                     |
| <span data-ttu-id="fce03-129">public SelectableDataArea company(\[SelectableDataArea company\])</span><span class="sxs-lookup"><span data-stu-id="fce03-129">public SelectableDataArea company(\[SelectableDataArea company\])</span></span>                                                          | <span data-ttu-id="fce03-130">レコードの法人を示すプロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-130">Gets and sets the property that indicates a legal entity for the record.</span></span>                                                       |
| <span data-ttu-id="fce03-131">public Common con2buf(container container)</span><span class="sxs-lookup"><span data-stu-id="fce03-131">public Common con2buf(container container)</span></span>                                                                                 | <span data-ttu-id="fce03-132">コンテナをテーブル バッファに展開します。</span><span class="sxs-lookup"><span data-stu-id="fce03-132">Unpacks a container into the table buffers.</span></span>                                                                                    |
| <span data-ttu-id="fce03-133">public ConcurrencyModel concurrencyModel(\[ConcurrencyModel concurrencyModel\])</span><span class="sxs-lookup"><span data-stu-id="fce03-133">public ConcurrencyModel concurrencyModel(\[ConcurrencyModel concurrencyModel\])</span></span>                                            | <span data-ttu-id="fce03-134">レコードの更新に使用する既定の同時実行モデルを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-134">Gets and sets the default concurrency model to use to update records.</span></span>                                                          |
| <span data-ttu-id="fce03-135">public int context(\[int newValue\])</span><span class="sxs-lookup"><span data-stu-id="fce03-135">public int context(\[int newValue\])</span></span>                                                                                       | <span data-ttu-id="fce03-136">コンテキスト プロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-136">Gets and sets the context property.</span></span>                                                                                            |
| <span data-ttu-id="fce03-137">public Common data(\[Common cursor\])</span><span class="sxs-lookup"><span data-stu-id="fce03-137">public Common data(\[Common cursor\])</span></span>                                                                                      | <span data-ttu-id="fce03-138">テーブルから行を取得します。</span><span class="sxs-lookup"><span data-stu-id="fce03-138">Retrieves a row from the table.</span></span>                                                                                                |
| <span data-ttu-id="fce03-139">public FormObjectSet dataSource()</span><span class="sxs-lookup"><span data-stu-id="fce03-139">public FormObjectSet dataSource()</span></span>                                                                                          | <span data-ttu-id="fce03-140">テーブルのデータ ソースを取得します。</span><span class="sxs-lookup"><span data-stu-id="fce03-140">Retrieves the data source of the table.</span></span>                                                                                        |
| <span data-ttu-id="fce03-141">public boolean disableCache(\[boolean newValue\])</span><span class="sxs-lookup"><span data-stu-id="fce03-141">public boolean disableCache(\[boolean newValue\])</span></span>                                                                          | <span data-ttu-id="fce03-142">キャッシュが無効かどうかを示すプロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-142">Gets and sets the property that indicates whether caching is disabled.</span></span>                                                         |
| <span data-ttu-id="fce03-143">public boolean doValidateDelete()</span><span class="sxs-lookup"><span data-stu-id="fce03-143">public boolean doValidateDelete()</span></span>                                                                                          | <span data-ttu-id="fce03-144">レコードを削除できる検証するアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="fce03-144">Performs the action to validate that a record can be deleted.</span></span>                                                                  |
| <span data-ttu-id="fce03-145">public boolean equal(Common cursor)</span><span class="sxs-lookup"><span data-stu-id="fce03-145">public boolean equal(Common cursor)</span></span>                                                                                        | <span data-ttu-id="fce03-146">指定されたオブジェクトが現在のオブジェクトと等しいかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-146">Determines whether the specified object is equal to the current one.</span></span>                                                           |
| <span data-ttu-id="fce03-147">public AccessRight fieldAccessRight(FieldName fieldName)</span><span class="sxs-lookup"><span data-stu-id="fce03-147">public AccessRight fieldAccessRight(FieldName fieldName)</span></span>                                                                   | <span data-ttu-id="fce03-148">フィールドのアクセス権を返します。</span><span class="sxs-lookup"><span data-stu-id="fce03-148">Returns the field access right.</span></span>                                                                                                |
| <span data-ttu-id="fce03-149">public AccessRight fieldBufferAccessRight(FieldName fieldName)</span><span class="sxs-lookup"><span data-stu-id="fce03-149">public AccessRight fieldBufferAccessRight(FieldName fieldName)</span></span>                                                             | <span data-ttu-id="fce03-150">現在のレコードのフィールド アクセス権を返します。</span><span class="sxs-lookup"><span data-stu-id="fce03-150">Returns the field access right for the current record.</span></span>                                                                         |
| <span data-ttu-id="fce03-151">public FieldState fieldState(FieldId fieldId, \[FieldState state\])</span><span class="sxs-lookup"><span data-stu-id="fce03-151">public FieldState fieldState(FieldId fieldId, \[FieldState state\])</span></span>                                                        | <span data-ttu-id="fce03-152">テーブル バッファーのフィールドの状態を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="fce03-152">Sets or returns the state of a field in the table buffer.</span></span>                                                                      |
| <span data-ttu-id="fce03-153">public container getAllowRedefault()</span><span class="sxs-lookup"><span data-stu-id="fce03-153">public container getAllowRedefault()</span></span>                                                                                       | <span data-ttu-id="fce03-154">既定値に再度設定することを許可されているフィールドの一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="fce03-154">Returns the list of fields that are allowed to re-default.</span></span>                                                                     |
| <span data-ttu-id="fce03-155">public container getDefaultingDependencies()</span><span class="sxs-lookup"><span data-stu-id="fce03-155">public container getDefaultingDependencies()</span></span>                                                                               | <span data-ttu-id="fce03-156">デフォルトの依存関係を保持するコンテナーを返します。</span><span class="sxs-lookup"><span data-stu-id="fce03-156">Returns the container that holds defaulting dependencies.</span></span>                                                                      |
| <span data-ttu-id="fce03-157">public TableExtension getExtension()</span><span class="sxs-lookup"><span data-stu-id="fce03-157">public TableExtension getExtension()</span></span>                                                                                       | <span data-ttu-id="fce03-158">テーブル拡張機能を返します。</span><span class="sxs-lookup"><span data-stu-id="fce03-158">Returns the table extension.</span></span>                                                                                                   |
| <span data-ttu-id="fce03-159">public AnyType getFieldValue(str fieldName, \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="fce03-159">public AnyType getFieldValue(str fieldName, \[int arrayIndex\])</span></span>                                                            | <span data-ttu-id="fce03-160">テーブル バッファから指定したフィールドの値を取得します。</span><span class="sxs-lookup"><span data-stu-id="fce03-160">Gets the value of the specified field from a table buffer.</span></span>                                                                     |
| <span data-ttu-id="fce03-161">public str getInstanceRelationType()</span><span class="sxs-lookup"><span data-stu-id="fce03-161">public str getInstanceRelationType()</span></span>                                                                                       | <span data-ttu-id="fce03-162">InstanceRelationType ID に対応するテーブルの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="fce03-162">Returns the table name that corresponds to the InstanceRelationType ID.</span></span>                                                        |
| <span data-ttu-id="fce03-163">public str getPhysicalTableName()</span><span class="sxs-lookup"><span data-stu-id="fce03-163">public str getPhysicalTableName()</span></span>                                                                                          | <span data-ttu-id="fce03-164">物理テーブル名を返します。SQL Temp DB テーブルの場合は、テーブル インスタンス名です。</span><span class="sxs-lookup"><span data-stu-id="fce03-164">Return the physical table name, which, in the case of the SQL Temp DB table, is the table instance name.</span></span>                       |
| <span data-ttu-id="fce03-165">public PresenceInfo getPresenceFieldData(FieldId fieldId, AnyType fieldValue)</span><span class="sxs-lookup"><span data-stu-id="fce03-165">public PresenceInfo getPresenceFieldData(FieldId fieldId, AnyType fieldValue)</span></span>                                              | <span data-ttu-id="fce03-166">指定されたフィールドから PresenceInfo 値を取得します。</span><span class="sxs-lookup"><span data-stu-id="fce03-166">Retrieves the PresenceInfo value from the specified field.</span></span>                                                                     |
| <span data-ttu-id="fce03-167">public str getSQLStatement()</span><span class="sxs-lookup"><span data-stu-id="fce03-167">public str getSQLStatement()</span></span>                                                                                               | <span data-ttu-id="fce03-168">レコードをデータベースから取得するために使用される SQL ステートメントを取得します。</span><span class="sxs-lookup"><span data-stu-id="fce03-168">Gets the SQL statement that is used to return records from the database.</span></span>                                                       |
| <span data-ttu-id="fce03-169">public Common getTableInInstanceHierarchy(TableId tableId)</span><span class="sxs-lookup"><span data-stu-id="fce03-169">public Common getTableInInstanceHierarchy(TableId tableId)</span></span>                                                                 |                                                                                                                                |
| <span data-ttu-id="fce03-170">public TableType getTableType()</span><span class="sxs-lookup"><span data-stu-id="fce03-170">public TableType getTableType()</span></span>                                                                                            | <span data-ttu-id="fce03-171">テーブルのタイプを示します。</span><span class="sxs-lookup"><span data-stu-id="fce03-171">Indicates the type of the table.</span></span>                                                                                               |
| <span data-ttu-id="fce03-172">public boolean hasRelatedTable(str relatedRoleName)</span><span class="sxs-lookup"><span data-stu-id="fce03-172">public boolean hasRelatedTable(str relatedRoleName)</span></span>                                                                        | <span data-ttu-id="fce03-173">外部キー制約バッファがテーブルにリンクされているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="fce03-173">Indicates whether a foreign key constraint buffer is linked with the table.</span></span>                                                    |
| <span data-ttu-id="fce03-174">public str helpField(FieldId fieldId)</span><span class="sxs-lookup"><span data-stu-id="fce03-174">public str helpField(FieldId fieldId)</span></span>                                                                                      | <span data-ttu-id="fce03-175">指定したフィールドのヘルプ テキストを含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="fce03-175">Retrieves a string that contains the Help text for the specified field.</span></span>                                                        |
| <span data-ttu-id="fce03-176">public FieldState inputStatus(\[FieldState inputStatus\])</span><span class="sxs-lookup"><span data-stu-id="fce03-176">public FieldState inputStatus(\[FieldState inputStatus\])</span></span>                                                                  | <span data-ttu-id="fce03-177">テーブル バッファーの現在の入力ステータスを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="fce03-177">Sets or returns the current input status of the table buffer.</span></span>                                                                  |
| <span data-ttu-id="fce03-178">public boolean interactiveContext(\[boolean context\])</span><span class="sxs-lookup"><span data-stu-id="fce03-178">public boolean interactiveContext(\[boolean context\])</span></span>                                                                     | <span data-ttu-id="fce03-179">テーブル バッファーの現在のインタラクティブ コンテキストを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="fce03-179">Sets or returns the current interactive context of the table buffer.</span></span>                                                           |
| <span data-ttu-id="fce03-180">public boolean isFieldDataRetrieved(str fieldName, \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="fce03-180">public boolean isFieldDataRetrieved(str fieldName, \[int arrayIndex\])</span></span>                                                     | <span data-ttu-id="fce03-181">指定されたフィールドのデータが取得されたかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="fce03-181">Checks whether the data of the given field has been retrieved.</span></span>                                                                 |
| <span data-ttu-id="fce03-182">public boolean isFieldSet(FieldId fieldId)</span><span class="sxs-lookup"><span data-stu-id="fce03-182">public boolean isFieldSet(FieldId fieldId)</span></span>                                                                                 | <span data-ttu-id="fce03-183">フィールドがセットまたは既定状態かどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="fce03-183">Checks whether a field has a Set or Defaulted state.</span></span>                                                                           |
| <span data-ttu-id="fce03-184">public boolean isFormDataSource()</span><span class="sxs-lookup"><span data-stu-id="fce03-184">public boolean isFormDataSource()</span></span>                                                                                          | <span data-ttu-id="fce03-185">データ ソースがフォームであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="fce03-185">Indicates whether the data source is a form.</span></span>                                                                                   |
| <span data-ttu-id="fce03-186">public boolean isNewRecord()</span><span class="sxs-lookup"><span data-stu-id="fce03-186">public boolean isNewRecord()</span></span>                                                                                               | <span data-ttu-id="fce03-187">レコードがまだ保存されていない新しいレコードである場合は true を返します。</span><span class="sxs-lookup"><span data-stu-id="fce03-187">Returns true if the record is a new record that hasn't been persisted yet.</span></span>                                                     |
| <span data-ttu-id="fce03-188">public boolean isPartOfUOWSaveChanges()</span><span class="sxs-lookup"><span data-stu-id="fce03-188">public boolean isPartOfUOWSaveChanges()</span></span>                                                                                    |                                                                                                                                |
| <span data-ttu-id="fce03-189">public boolean isTempDb()</span><span class="sxs-lookup"><span data-stu-id="fce03-189">public boolean isTempDb()</span></span>                                                                                                  | <span data-ttu-id="fce03-190">テーブルのタイプが SQL TempDB であるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="fce03-190">Indicates whether the type of the table is SQL TempDB.</span></span>                                                                         |
| <span data-ttu-id="fce03-191">public boolean isTmp()</span><span class="sxs-lookup"><span data-stu-id="fce03-191">public boolean isTmp()</span></span>                                                                                                     | <span data-ttu-id="fce03-192">これが一時テーブルであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="fce03-192">Indicates whether this is a temporary table.</span></span>                                                                                   |
| <span data-ttu-id="fce03-193">public Common joinChild()</span><span class="sxs-lookup"><span data-stu-id="fce03-193">public Common joinChild()</span></span>                                                                                                  | <span data-ttu-id="fce03-194">現在のレコードの結合子を検索します。</span><span class="sxs-lookup"><span data-stu-id="fce03-194">Finds the join child of the current record.</span></span>                                                                                    |
| <span data-ttu-id="fce03-195">public Common joinParent()</span><span class="sxs-lookup"><span data-stu-id="fce03-195">public Common joinParent()</span></span>                                                                                                 | <span data-ttu-id="fce03-196">現在のレコードの結合の親を検索します。</span><span class="sxs-lookup"><span data-stu-id="fce03-196">Finds the join parent of the current record.</span></span>                                                                                   |
| <span data-ttu-id="fce03-197">public boolean linkPhysicalTableInstance(\[Common record\])</span><span class="sxs-lookup"><span data-stu-id="fce03-197">public boolean linkPhysicalTableInstance(\[Common record\])</span></span>                                                                | <span data-ttu-id="fce03-198">レコードの物理テーブル インスタンスへのリンクがあるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="fce03-198">Checks whether there is a link for the physical table instance for the record.</span></span>                                                 |
| <span data-ttu-id="fce03-199">public Common orig()</span><span class="sxs-lookup"><span data-stu-id="fce03-199">public Common orig()</span></span>                                                                                                       | <span data-ttu-id="fce03-200">現在のレコードの元の値を取得します。</span><span class="sxs-lookup"><span data-stu-id="fce03-200">Retrieves the original values of the current record.</span></span>                                                                           |
| <span data-ttu-id="fce03-201">public boolean overwriteSystemfields(\[boolean allowOverwrite\])</span><span class="sxs-lookup"><span data-stu-id="fce03-201">public boolean overwriteSystemfields(\[boolean allowOverwrite\])</span></span>                                                           | <span data-ttu-id="fce03-202">システム フィールドを上書きできるかどうかを示すプロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-202">Gets and sets the property that indicates whether system fields can be overwritten.</span></span>                                            |
| <span data-ttu-id="fce03-203">public boolean queryTimedOut()</span><span class="sxs-lookup"><span data-stu-id="fce03-203">public boolean queryTimedOut()</span></span>                                                                                             | <span data-ttu-id="fce03-204">クエリが実行の時間制限を超過したかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="fce03-204">Indicates whether the query exceeded the time limit for execution.</span></span>                                                             |
| <span data-ttu-id="fce03-205">public int queryTimeout(\[int seconds\], \[boolean raiseException\])</span><span class="sxs-lookup"><span data-stu-id="fce03-205">public int queryTimeout(\[int seconds\], \[boolean raiseException\])</span></span>                                                       | <span data-ttu-id="fce03-206">クエリの実行に対する時間制限を示すプロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-206">Gets and sets the property that indicates the time limit for the execution of a query.</span></span>                                         |
| <span data-ttu-id="fce03-207">public boolean readCommittedLock(\[boolean readCommittedLock\])</span><span class="sxs-lookup"><span data-stu-id="fce03-207">public boolean readCommittedLock(\[boolean readCommittedLock\])</span></span>                                                            |                                                                                                                                |
| <span data-ttu-id="fce03-208">public boolean readPast(\[boolean skipLockedRows\])</span><span class="sxs-lookup"><span data-stu-id="fce03-208">public boolean readPast(\[boolean skipLockedRows\])</span></span>                                                                        | <span data-ttu-id="fce03-209">レコードの読み取り時に、他のプロセスによりロックされる行をスキップするかどうかを示すプロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-209">Gets and sets the property that indicates whether to skip rows that are locked by other processes when a record is read.</span></span>       |
| <span data-ttu-id="fce03-210">public boolean recordLevelSecurity(\[boolean newValue\])</span><span class="sxs-lookup"><span data-stu-id="fce03-210">public boolean recordLevelSecurity(\[boolean newValue\])</span></span>                                                                   | <span data-ttu-id="fce03-211">レコード レベルのセキュリティを適用するかどうかを示すプロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-211">Gets and sets the property that indicates whether to apply security on a record level.</span></span>                                         |
| <span data-ttu-id="fce03-212">public Common relatedTable(str name, \[Common buffer\])</span><span class="sxs-lookup"><span data-stu-id="fce03-212">public Common relatedTable(str name, \[Common buffer\])</span></span>                                                                    | <span data-ttu-id="fce03-213">テーブル バッファのリンクに関連するバッファーを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="fce03-213">Sets or returns the related buffer of a link of a table buffer.</span></span>                                                                |
| <span data-ttu-id="fce03-214">public Int64 RowCount()</span><span class="sxs-lookup"><span data-stu-id="fce03-214">public Int64 RowCount()</span></span>                                                                                                    | <span data-ttu-id="fce03-215">テーブル内の行数を取得します。</span><span class="sxs-lookup"><span data-stu-id="fce03-215">Retrieves the number of rows in the table.</span></span>                                                                                     |
| <span data-ttu-id="fce03-216">public boolean selectForUpdate(\[boolean lockRecordsExclusive\])</span><span class="sxs-lookup"><span data-stu-id="fce03-216">public boolean selectForUpdate(\[boolean lockRecordsExclusive\])</span></span>                                                           | <span data-ttu-id="fce03-217">読み取り時に更新用のレコードを選択するかどうかを示すプロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-217">Gets and sets the property that indicates whether to select records for update when they are read.</span></span>                             |
| <span data-ttu-id="fce03-218">public boolean selectLocked(\[boolean lockRecordsShared\])</span><span class="sxs-lookup"><span data-stu-id="fce03-218">public boolean selectLocked(\[boolean lockRecordsShared\])</span></span>                                                                 | <span data-ttu-id="fce03-219">ロックされているレコードを選択するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="fce03-219">Indicates whether to select locked records.</span></span>                                                                                    |
| <span data-ttu-id="fce03-220">public Common selectRefRecord(FieldId referenceFieldId)</span><span class="sxs-lookup"><span data-stu-id="fce03-220">public Common selectRefRecord(FieldId referenceFieldId)</span></span>                                                                    | <span data-ttu-id="fce03-221">参照されているフィールド ID によりレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="fce03-221">Selects the record by referenced field ID.</span></span>                                                                                     |
| <span data-ttu-id="fce03-222">public boolean selectWithRepeatableRead(\[boolean useRepeatableRead\])</span><span class="sxs-lookup"><span data-stu-id="fce03-222">public boolean selectWithRepeatableRead(\[boolean useRepeatableRead\])</span></span>                                                     | <span data-ttu-id="fce03-223">反復可能な読み取りが有効かどうかを示すプロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-223">Gets and sets the property that indicates whether repeatable read is enabled.</span></span>                                                  |
| <span data-ttu-id="fce03-224">public boolean setTempDB()</span><span class="sxs-lookup"><span data-stu-id="fce03-224">public boolean setTempDB()</span></span>                                                                                                 |                                                                                                                                |
| <span data-ttu-id="fce03-225">public boolean setTmp()</span><span class="sxs-lookup"><span data-stu-id="fce03-225">public boolean setTmp()</span></span>                                                                                                    | <span data-ttu-id="fce03-226">データベースに保存されていない場合にテーブルを設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-226">Sets the table so that it is not persisted to the database.</span></span>                                                                    |
| <span data-ttu-id="fce03-227">public boolean skipAosValidation(\[boolean newValue\])</span><span class="sxs-lookup"><span data-stu-id="fce03-227">public boolean skipAosValidation(\[boolean newValue\])</span></span>                                                                     | <span data-ttu-id="fce03-228">Application Object Server (AOS) の検証をスキップするかどうかを示すプロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-228">Gets and sets the property that indicates whether to skip validation Application Object Server (AOS).</span></span> |
| <span data-ttu-id="fce03-229">public boolean skipDatabaseLog(\[boolean newValue\])</span><span class="sxs-lookup"><span data-stu-id="fce03-229">public boolean skipDatabaseLog(\[boolean newValue\])</span></span>                                                                       | <span data-ttu-id="fce03-230">データベース ログ要求をスキップするかどうかを示すプロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-230">Gets and sets the property that indicates whether to skip database log requests.</span></span>                                               |
| <span data-ttu-id="fce03-231">public boolean skipDataMethods(\[boolean newValue\])</span><span class="sxs-lookup"><span data-stu-id="fce03-231">public boolean skipDataMethods(\[boolean newValue\])</span></span>                                                                       | <span data-ttu-id="fce03-232">オーバーロードされたメソッドを破棄するかどうかを示すプロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-232">Gets and sets the property that indicates whether to discard overloaded methods.</span></span>                                               |
| <span data-ttu-id="fce03-233">public boolean skipDeleteActions(\[boolean newValue\])</span><span class="sxs-lookup"><span data-stu-id="fce03-233">public boolean skipDeleteActions(\[boolean newValue\])</span></span>                                                                     | <span data-ttu-id="fce03-234">テーブルで削除アクションをスキップするかどうかを示すプロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-234">Gets and sets the property that indicates whether to skip delete actions on the table.</span></span>                                         |
| <span data-ttu-id="fce03-235">public boolean skipDeleteMethod(\[boolean newValue\])</span><span class="sxs-lookup"><span data-stu-id="fce03-235">public boolean skipDeleteMethod(\[boolean newValue\])</span></span>                                                                      | <span data-ttu-id="fce03-236">オーバーロードされたメソッドを破棄するかどうかを示すプロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-236">Gets and sets the property that indicates whether to discard overloaded methods.</span></span>                                               |
| <span data-ttu-id="fce03-237">public boolean skipEvents(\[boolean newValue\])</span><span class="sxs-lookup"><span data-stu-id="fce03-237">public boolean skipEvents(\[boolean newValue\])</span></span>                                                                            | <span data-ttu-id="fce03-238">xRecord オブジェクトの有効期間の Application.event\* メソッドの呼び出しをオフにするオプションを提供します。</span><span class="sxs-lookup"><span data-stu-id="fce03-238">Provides an option to turn off calling the Application.event\* methods for the lifetime of an xRecord object.</span></span>                  |
| <span data-ttu-id="fce03-239">public boolean skipPostLoad(\[boolean newValue\])</span><span class="sxs-lookup"><span data-stu-id="fce03-239">public boolean skipPostLoad(\[boolean newValue\])</span></span>                                                                          | <span data-ttu-id="fce03-240">テーブルで xRecord.postLoad メソッドの実行をスキップするかどうかを示すプロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-240">Gets and sets the property that indicates whether to skip executing the xRecord.postLoad method on the table.</span></span>                  |
| <span data-ttu-id="fce03-241">public boolean skipTTSCheck(\[boolean newValue\])</span><span class="sxs-lookup"><span data-stu-id="fce03-241">public boolean skipTTSCheck(\[boolean newValue\])</span></span>                                                                          | <span data-ttu-id="fce03-242">更新用にレコードが選択されているかどうかを決定するため、チェックをスキップするかどうかを示すプロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-242">Gets and sets the property that indicates whether to skip the check to determine whether the record is selected for update.</span></span>    |
| <span data-ttu-id="fce03-243">public boolean suppressWarnings(\[boolean newValue\])</span><span class="sxs-lookup"><span data-stu-id="fce03-243">public boolean suppressWarnings(\[boolean newValue\])</span></span>                                                                      | <span data-ttu-id="fce03-244">このポインタの警告を非表示にするかどうかを示すプロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-244">Gets and sets the property that indicates whether to suppress warnings for this pointer.</span></span>                                       |
| <span data-ttu-id="fce03-245">public AccessRight tableAccessRight()</span><span class="sxs-lookup"><span data-stu-id="fce03-245">public AccessRight tableAccessRight()</span></span>                                                                                      | <span data-ttu-id="fce03-246">テーブルのアクセス権を返します。</span><span class="sxs-lookup"><span data-stu-id="fce03-246">Returns the table access right.</span></span>                                                                                                |
| <span data-ttu-id="fce03-247">public AccessRight tableBufferAccessRight()</span><span class="sxs-lookup"><span data-stu-id="fce03-247">public AccessRight tableBufferAccessRight()</span></span>                                                                                | <span data-ttu-id="fce03-248">現在のレコードのテーブル アクセス権を返します。</span><span class="sxs-lookup"><span data-stu-id="fce03-248">Returns the table access right for the current record.</span></span>                                                                         |
| <span data-ttu-id="fce03-249">public boolean takeOwnershipOfTempDBTable(boolean newValue)</span><span class="sxs-lookup"><span data-stu-id="fce03-249">public boolean takeOwnershipOfTempDBTable(boolean newValue)</span></span>                                                                |                                                                                                                                |
| <span data-ttu-id="fce03-250">public str toolTipField(FieldId fieldId)</span><span class="sxs-lookup"><span data-stu-id="fce03-250">public str toolTipField(FieldId fieldId)</span></span>                                                                                   | <span data-ttu-id="fce03-251">指定されたフィールドの HelpText 値を取得します。</span><span class="sxs-lookup"><span data-stu-id="fce03-251">Retrieves the HelpText value for the specified field.</span></span>                                                                          |
| <span data-ttu-id="fce03-252">public str toolTipRecord()</span><span class="sxs-lookup"><span data-stu-id="fce03-252">public str toolTipRecord()</span></span>                                                                                                 | <span data-ttu-id="fce03-253">現在のレコードのツールヒント値を取得します。</span><span class="sxs-lookup"><span data-stu-id="fce03-253">Retrieves the ToolTip value for the current record.</span></span>                                                                            |
| <span data-ttu-id="fce03-254">public int usageCount()</span><span class="sxs-lookup"><span data-stu-id="fce03-254">public int usageCount()</span></span>                                                                                                    | <span data-ttu-id="fce03-255">オブジェクトが持つ参照 (参照カウンターの値) の現在の番号を取得します。</span><span class="sxs-lookup"><span data-stu-id="fce03-255">Retrieves the current number of references (the value of the reference counter) that the object has.</span></span>                           |
| <span data-ttu-id="fce03-256">public boolean useExistingTempDBTable(str physicalTempTableName)</span><span class="sxs-lookup"><span data-stu-id="fce03-256">public boolean useExistingTempDBTable(str physicalTempTableName)</span></span>                                                           |                                                                                                                                |
| <span data-ttu-id="fce03-257">public boolean validateDelete()</span><span class="sxs-lookup"><span data-stu-id="fce03-257">public boolean validateDelete()</span></span>                                                                                            | <span data-ttu-id="fce03-258">現在のレコードが有効で、データベースから削除する準備ができているかどうかを調べます。</span><span class="sxs-lookup"><span data-stu-id="fce03-258">Determines whether the current record is valid and ready to be deleted from the database.</span></span>                                      |
| <span data-ttu-id="fce03-259">public boolean validateField(FieldId fieldIdToCheck)</span><span class="sxs-lookup"><span data-stu-id="fce03-259">public boolean validateField(FieldId fieldIdToCheck)</span></span>                                                                       | <span data-ttu-id="fce03-260">指定されたフィールドが有効かどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-260">Determines whether the specified field is valid.</span></span>                                                                               |
| <span data-ttu-id="fce03-261">public boolean validateFieldValue(FieldName fieldName, \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="fce03-261">public boolean validateFieldValue(FieldName fieldName, \[int arrayIndex\])</span></span>                                                 |                                                                                                                                |
| <span data-ttu-id="fce03-262">private container validateRelations(\[boolean onlyValidateCompositeRelations\], \[boolean onlyValidateModifiedRelations\])</span><span class="sxs-lookup"><span data-stu-id="fce03-262">private container validateRelations(\[boolean onlyValidateCompositeRelations\], \[boolean onlyValidateModifiedRelations\])</span></span> |                                                                                                                                |
| <span data-ttu-id="fce03-263">public boolean validateWrite()</span><span class="sxs-lookup"><span data-stu-id="fce03-263">public boolean validateWrite()</span></span>                                                                                             | <span data-ttu-id="fce03-264">現在のレコードが有効で、書き込み可能な状態かどうかを判別します。</span><span class="sxs-lookup"><span data-stu-id="fce03-264">Determines whether the current record is valid and ready to be written.</span></span>                                                        |
| <span data-ttu-id="fce03-265">public ValidTimeStateUpdate validTimeStateUpdateMode(ValidTimeStateUpdate validTimeStateUpdateMode)</span><span class="sxs-lookup"><span data-stu-id="fce03-265">public ValidTimeStateUpdate validTimeStateUpdateMode(ValidTimeStateUpdate validTimeStateUpdateMode)</span></span>                        | <span data-ttu-id="fce03-266">カーソルで有効な時間状態更新モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-266">Sets a valid time state update mode on the cursor.</span></span>                                                                             |
| <span data-ttu-id="fce03-267">public CachedHow wasCached()</span><span class="sxs-lookup"><span data-stu-id="fce03-267">public CachedHow wasCached()</span></span>                                                                                               | <span data-ttu-id="fce03-268">データの取得元となった場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-268">Specifies the location from which the data was retrieved.</span></span>                                                                      |
| <span data-ttu-id="fce03-269">public str xml(\[int indent\])</span><span class="sxs-lookup"><span data-stu-id="fce03-269">public str xml(\[int indent\])</span></span>                                                                                             | <span data-ttu-id="fce03-270">現在のオブジェクトを表す XML 文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="fce03-270">Retrieves an XML string that represents the current object.</span></span>                                                                    |
| <span data-ttu-id="fce03-271">public void doDelete()</span><span class="sxs-lookup"><span data-stu-id="fce03-271">public void doDelete()</span></span>                                                                                                     | <span data-ttu-id="fce03-272">現在のレコードをテーブルから削除し、テーブルの delete メソッドの追加ロジックをバイパスします。</span><span class="sxs-lookup"><span data-stu-id="fce03-272">Deletes the current record from the table and bypasses any additional logic in the delete method of the table.</span></span>                 |
| <span data-ttu-id="fce03-273">public void update()</span><span class="sxs-lookup"><span data-stu-id="fce03-273">public void update()</span></span>                                                                                                       | <span data-ttu-id="fce03-274">現在のレコードを更新します。</span><span class="sxs-lookup"><span data-stu-id="fce03-274">Updates the current record.</span></span>                                                                                                    |
| <span data-ttu-id="fce03-275">public void merge(Common mergeInto)</span><span class="sxs-lookup"><span data-stu-id="fce03-275">public void merge(Common mergeInto)</span></span>                                                                                        | <span data-ttu-id="fce03-276">現在のテーブルを指定されたテーブルとマージします。</span><span class="sxs-lookup"><span data-stu-id="fce03-276">Merges the current table with the specified table.</span></span>                                                                             |
| <span data-ttu-id="fce03-277">public void clear()</span><span class="sxs-lookup"><span data-stu-id="fce03-277">public void clear()</span></span>                                                                                                        | <span data-ttu-id="fce03-278">テーブル バッファーからすべての行を削除します。</span><span class="sxs-lookup"><span data-stu-id="fce03-278">Removes all rows from the table buffer.</span></span>                                                                                        |
| <span data-ttu-id="fce03-279">public void setXDSContext(\[str contextString\])</span><span class="sxs-lookup"><span data-stu-id="fce03-279">public void setXDSContext(\[str contextString\])</span></span>                                                                           | <span data-ttu-id="fce03-280">新しい XDS コンテキストを設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-280">Sets new XDS context.</span></span>                                                                                                          |
| <span data-ttu-id="fce03-281">public void renamePrimaryKey()</span><span class="sxs-lookup"><span data-stu-id="fce03-281">public void renamePrimaryKey()</span></span>                                                                                             | <span data-ttu-id="fce03-282">この表の対応する主キーの値の変更に従って、他のテーブルの外部キーの名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="fce03-282">Renames the foreign keys in other tables according to the change of the corresponding primary key value in this table.</span></span>         |
| <span data-ttu-id="fce03-283">public void dispose()</span><span class="sxs-lookup"><span data-stu-id="fce03-283">public void dispose()</span></span>                                                                                                      | <span data-ttu-id="fce03-284">XRecord オブジェクトによって使用されているリソースを解放します。</span><span class="sxs-lookup"><span data-stu-id="fce03-284">Releases resources that are used by the xRecord object.</span></span>                                                                        |
| <span data-ttu-id="fce03-285">public void setConnection(Connection connection)</span><span class="sxs-lookup"><span data-stu-id="fce03-285">public void setConnection(Connection connection)</span></span>                                                                           | <span data-ttu-id="fce03-286">この表のユーザー接続を設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-286">Sets the user connection for this table.</span></span>                                                                                       |
| <span data-ttu-id="fce03-287">public void delete()</span><span class="sxs-lookup"><span data-stu-id="fce03-287">public void delete()</span></span>                                                                                                       | <span data-ttu-id="fce03-288">テーブルから現在のレコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="fce03-288">Deletes the current record from the table.</span></span>                                                                                     |
| <span data-ttu-id="fce03-289">public void defaultField(FieldId fieldId)</span><span class="sxs-lookup"><span data-stu-id="fce03-289">public void defaultField(FieldId fieldId)</span></span>                                                                                  | <span data-ttu-id="fce03-290">テーブルのフィールドの既定値を設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-290">Populates default values in a field in the table.</span></span>                                                                              |
| <span data-ttu-id="fce03-291">private void dbOpInTransaction(\[boolean isWriteOperation\])</span><span class="sxs-lookup"><span data-stu-id="fce03-291">private void dbOpInTransaction(\[boolean isWriteOperation\])</span></span>                                                               | <span data-ttu-id="fce03-292">失敗した場合にデータベース操作が正しく閉じられていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fce03-292">Makes sure that database operations are correctly closed if they fail.</span></span>                                                         |
| <span data-ttu-id="fce03-293">public void write()</span><span class="sxs-lookup"><span data-stu-id="fce03-293">public void write()</span></span>                                                                                                        | <span data-ttu-id="fce03-294">レコードが存在する場合は更新します。存在しない場合はレコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="fce03-294">Updates a record if it exists; otherwise, inserts a record.</span></span>                                                                    |
| <span data-ttu-id="fce03-295">public void preRemoting()</span><span class="sxs-lookup"><span data-stu-id="fce03-295">public void preRemoting()</span></span>                                                                                                  | <span data-ttu-id="fce03-296">他のレベルに状態をパックしているテーブルに対してレベル間の呼び出しが実行される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="fce03-296">Is executed before a cross-tier call is about to be executed for the table that would pack its state to the other tier.</span></span>        |
| <span data-ttu-id="fce03-297">public void modifiedFieldValue(FieldName fieldName, \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="fce03-297">public void modifiedFieldValue(FieldName fieldName, \[int arrayIndex\])</span></span>                                                    | <span data-ttu-id="fce03-298">指定したフィールドを元の値に変更します。</span><span class="sxs-lookup"><span data-stu-id="fce03-298">Modifies the specified field to the original value.</span></span>                                                                            |
| <span data-ttu-id="fce03-299">public void defaultRow()</span><span class="sxs-lookup"><span data-stu-id="fce03-299">public void defaultRow()</span></span>                                                                                                   | <span data-ttu-id="fce03-300">非対話型の場合、テーブルのフィールドの既定値を設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-300">Populates default values in fields in the table in the non-interactive case.</span></span>                                                   |
| <span data-ttu-id="fce03-301">public void reread()</span><span class="sxs-lookup"><span data-stu-id="fce03-301">public void reread()</span></span>                                                                                                       | <span data-ttu-id="fce03-302">テーブルからレコードを再読み取りします。</span><span class="sxs-lookup"><span data-stu-id="fce03-302">Rereads the record from the table.</span></span>                                                                                             |
| <span data-ttu-id="fce03-303">public void modifiedField(FieldId fieldId)</span><span class="sxs-lookup"><span data-stu-id="fce03-303">public void modifiedField(FieldId fieldId)</span></span>                                                                                 | <span data-ttu-id="fce03-304">指定したフィールドを元通りに変更します。</span><span class="sxs-lookup"><span data-stu-id="fce03-304">Modifies the specified field to the original.</span></span>                                                                                  |
| <span data-ttu-id="fce03-305">public void ttsabort()</span><span class="sxs-lookup"><span data-stu-id="fce03-305">public void ttsabort()</span></span>                                                                                                     | <span data-ttu-id="fce03-306">ttsbegin メソッドの呼び出しによって開始されたトランザクションの廃棄。</span><span class="sxs-lookup"><span data-stu-id="fce03-306">Aborts a transaction that was started by a call to the ttsbegin method.</span></span>                                                        |
| <span data-ttu-id="fce03-307">public void insert()</span><span class="sxs-lookup"><span data-stu-id="fce03-307">public void insert()</span></span>                                                                                                       | <span data-ttu-id="fce03-308">テーブルにレコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="fce03-308">Inserts the record into the table.</span></span>                                                                                             |
| <span data-ttu-id="fce03-309">public void doClear()</span><span class="sxs-lookup"><span data-stu-id="fce03-309">public void doClear()</span></span>                                                                                                      | <span data-ttu-id="fce03-310">現在の行をテーブル バッファーから削除し、テーブルの clear メソッドの追加ロジックをバイパスします。</span><span class="sxs-lookup"><span data-stu-id="fce03-310">Removes all rows from the table buffer and bypasses any additional logic in the clear method of the table.</span></span>                     |
| <span data-ttu-id="fce03-311">public void initValue()</span><span class="sxs-lookup"><span data-stu-id="fce03-311">public void initValue()</span></span>                                                                                                    | <span data-ttu-id="fce03-312">フィールドを既定値に初期化します。</span><span class="sxs-lookup"><span data-stu-id="fce03-312">Initializes a field to the default value.</span></span>                                                                                      |
| <span data-ttu-id="fce03-313">public void doUpdate()</span><span class="sxs-lookup"><span data-stu-id="fce03-313">public void doUpdate()</span></span>                                                                                                     | <span data-ttu-id="fce03-314">現在のレコードを更新し、テーブルの更新メソッドにある追加ロジックをバイパスします。</span><span class="sxs-lookup"><span data-stu-id="fce03-314">Updates the current record and bypasses any additional logic in the update method of the table.</span></span>                                |
| <span data-ttu-id="fce03-315">public void ttsbegin()</span><span class="sxs-lookup"><span data-stu-id="fce03-315">public void ttsbegin()</span></span>                                                                                                     | <span data-ttu-id="fce03-316">ttscommit メソッドによりコミット、または ttsabort メソッドによって中止できるトランザクションを開始します。</span><span class="sxs-lookup"><span data-stu-id="fce03-316">Starts a transaction that can be either committed by the ttscommit method or aborted by the ttsabort method.</span></span>                   |
| <span data-ttu-id="fce03-317">public void setCrossPartition(boolean newValue)</span><span class="sxs-lookup"><span data-stu-id="fce03-317">public void setCrossPartition(boolean newValue)</span></span>                                                                            | <span data-ttu-id="fce03-318">テーブルのパーティション間分割を設定またはリセットします。</span><span class="sxs-lookup"><span data-stu-id="fce03-318">Sets or resets cross-partitioning for the table.</span></span>                                                                               |
| <span data-ttu-id="fce03-319">public void setTmpData(Common cursor)</span><span class="sxs-lookup"><span data-stu-id="fce03-319">public void setTmpData(Common cursor)</span></span>                                                                                      | <span data-ttu-id="fce03-320">一時的なテーブルの内容を指定されたデータに設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-320">Sets the contents of the temporary table to the specified data.</span></span>                                                                |
| <span data-ttu-id="fce03-321">public void ttscommit()</span><span class="sxs-lookup"><span data-stu-id="fce03-321">public void ttscommit()</span></span>                                                                                                    | <span data-ttu-id="fce03-322">ttsbegin メソッドの呼び出しによって開始されたトランザクションをコミットします。</span><span class="sxs-lookup"><span data-stu-id="fce03-322">Commits a transaction that was started by a call to the ttsbegin method.</span></span>                                                       |
| <span data-ttu-id="fce03-323">public void setFieldValue(str fieldName, AnyType value, \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="fce03-323">public void setFieldValue(str fieldName, AnyType value, \[int arrayIndex\])</span></span>                                                | <span data-ttu-id="fce03-324">レコード バッファーのフィールド値を設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-324">Sets the field value in the record buffer.</span></span>                                                                                     |
| <span data-ttu-id="fce03-325">public void doInsert()</span><span class="sxs-lookup"><span data-stu-id="fce03-325">public void doInsert()</span></span>                                                                                                     | <span data-ttu-id="fce03-326">テーブルにレコードを挿入し、テーブルの挿入メソッドで追加のロジックをバイパスします。</span><span class="sxs-lookup"><span data-stu-id="fce03-326">Inserts the record into the table and bypasses any additional logic in the insert method of the table.</span></span>                         |
| <span data-ttu-id="fce03-327">public void setSQLTracing(\[boolean tracingmode\])</span><span class="sxs-lookup"><span data-stu-id="fce03-327">public void setSQLTracing(\[boolean tracingmode\])</span></span>                                                                         | <span data-ttu-id="fce03-328">SQL トレース モードを有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="fce03-328">Enables or disables SQL tracing mode.</span></span>                                                                                          |
| <span data-ttu-id="fce03-329">public void postLoad()</span><span class="sxs-lookup"><span data-stu-id="fce03-329">public void postLoad()</span></span>                                                                                                     | <span data-ttu-id="fce03-330">レコードが読み取られた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="fce03-330">Is executed after a record is read.</span></span>                                                                                            |

## <a name="method-aosvalidatedelete"></a><span data-ttu-id="fce03-331">メソッド aosValidateDelete</span><span class="sxs-lookup"><span data-stu-id="fce03-331">Method aosValidateDelete</span></span>

<span data-ttu-id="fce03-332">サーバー上で、指定されたレコードをテーブルから削除できることを検証します。</span><span class="sxs-lookup"><span data-stu-id="fce03-332">Validates on the server that the specified record can be deleted from a table.</span></span>

```xpp
public boolean aosValidateDelete()
```

### <a name="return-value---aosvalidatedelete"></a><span data-ttu-id="fce03-333">戻り値 - aosValidateDelete</span><span class="sxs-lookup"><span data-stu-id="fce03-333">Return Value - aosValidateDelete</span></span>

<span data-ttu-id="fce03-334">レコードを削除することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fce03-334">true if the record can be deleted; otherwise, false.</span></span>

## <a name="method-aosvalidateinsert"></a><span data-ttu-id="fce03-335">メソッド aosValidateInsert</span><span class="sxs-lookup"><span data-stu-id="fce03-335">Method aosValidateInsert</span></span>

<span data-ttu-id="fce03-336">サーバー上で、指定されたレコードを挿入できることを検証します。</span><span class="sxs-lookup"><span data-stu-id="fce03-336">Validates on the server that the specified record can be inserted.</span></span>

```xpp
public boolean aosValidateInsert()
```

### <a name="return-value---aosvalidateinsert"></a><span data-ttu-id="fce03-337">戻り値 - aosValidateInsert</span><span class="sxs-lookup"><span data-stu-id="fce03-337">Return Value - aosValidateInsert</span></span>

<span data-ttu-id="fce03-338">レコードを挿入することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fce03-338">true if the record can be inserted; otherwise, false.</span></span>

## <a name="method-aosvalidateread"></a><span data-ttu-id="fce03-339">メソッド aosValidateRead</span><span class="sxs-lookup"><span data-stu-id="fce03-339">Method aosValidateRead</span></span>

<span data-ttu-id="fce03-340">サーバー上で、指定されたレコードを読み取れることを検証します。</span><span class="sxs-lookup"><span data-stu-id="fce03-340">Validates on the server that the specified record can be read.</span></span>

```xpp
public boolean aosValidateRead()
```

### <a name="return-value---aosvalidateread"></a><span data-ttu-id="fce03-341">戻り値 - aosValidateRead</span><span class="sxs-lookup"><span data-stu-id="fce03-341">Return Value - aosValidateRead</span></span>

<span data-ttu-id="fce03-342">レコードを読み取ることができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fce03-342">true if the record can be read; otherwise, false.</span></span>

## <a name="method-aosvalidateupdate"></a><span data-ttu-id="fce03-343">メソッド aosValidateUpdate</span><span class="sxs-lookup"><span data-stu-id="fce03-343">Method aosValidateUpdate</span></span>

<span data-ttu-id="fce03-344">サーバー上で、指定されたレコードを更新できることを検証します。</span><span class="sxs-lookup"><span data-stu-id="fce03-344">Validates on the server that the specified record can be updated.</span></span>

```xpp
public boolean aosValidateUpdate()
```

### <a name="return-value---aosvalidateupdate"></a><span data-ttu-id="fce03-345">戻り値 - aosValidateUpdate</span><span class="sxs-lookup"><span data-stu-id="fce03-345">Return Value - aosValidateUpdate</span></span>

<span data-ttu-id="fce03-346">レコードを更新することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fce03-346">true if the record can be updated; otherwise, false.</span></span>

## <a name="method-buf2con"></a><span data-ttu-id="fce03-347">メソッド buf2con</span><span class="sxs-lookup"><span data-stu-id="fce03-347">Method buf2con</span></span>

<span data-ttu-id="fce03-348">X++ コンテナーに xRecord インスタンスのテーブル バッファーをパックします。</span><span class="sxs-lookup"><span data-stu-id="fce03-348">Packs the table buffers of an xRecord instance into an X++ container.</span></span>

```xpp
public container buf2con([boolean packOrigBuffer])
```

### <a name="parameters---buf2con"></a><span data-ttu-id="fce03-349">パラメーター - buf2con</span><span class="sxs-lookup"><span data-stu-id="fce03-349">Parameters - buf2con</span></span>

<span data-ttu-id="fce03-350">packOrigBuffer</span><span class="sxs-lookup"><span data-stu-id="fce03-350">packOrigBuffer</span></span>  

### <a name="return-value---buf2con"></a><span data-ttu-id="fce03-351">戻り値 - buf2con</span><span class="sxs-lookup"><span data-stu-id="fce03-351">Return Value - buf2con</span></span>

<span data-ttu-id="fce03-352">梱包済みバッファーを保持するコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="fce03-352">A container that holds packed buffers.</span></span>

## <a name="method-cansubmittoworkflow"></a><span data-ttu-id="fce03-353">メソッド canSubmitToWorkflow</span><span class="sxs-lookup"><span data-stu-id="fce03-353">Method canSubmitToWorkflow</span></span>

<span data-ttu-id="fce03-354">ワークフローへの送信が可能かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="fce03-354">Indicates whether submission to workflow is possible.</span></span>

```xpp
public boolean canSubmitToWorkflow([str workflowType])
```

### <a name="parameters---cansubmittoworkflow"></a><span data-ttu-id="fce03-355">パラメーター - canSubmitToWorkflow</span><span class="sxs-lookup"><span data-stu-id="fce03-355">Parameters - canSubmitToWorkflow</span></span>

<span data-ttu-id="fce03-356">workflowType</span><span class="sxs-lookup"><span data-stu-id="fce03-356">workflowType</span></span>  

### <a name="return-value---cansubmittoworkflow"></a><span data-ttu-id="fce03-357">戻り値 - canSubmitToWorkflow</span><span class="sxs-lookup"><span data-stu-id="fce03-357">Return Value - canSubmitToWorkflow</span></span>

<span data-ttu-id="fce03-358">送信が可能な場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="fce03-358">true if submission is possible; otherwise, false.</span></span>

## <a name="method-caption"></a><span data-ttu-id="fce03-359">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="fce03-359">Method caption</span></span>

<span data-ttu-id="fce03-360">テーブルのキャプション プロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-360">Gets and sets the caption property of a table.</span></span>

```xpp
public str caption()
```

### <a name="return-value---caption"></a><span data-ttu-id="fce03-361">戻り値 - caption</span><span class="sxs-lookup"><span data-stu-id="fce03-361">Return Value - caption</span></span>

<span data-ttu-id="fce03-362">テーブルのキャプション。</span><span class="sxs-lookup"><span data-stu-id="fce03-362">The caption of the table.</span></span>

## <a name="method-checkinvalidfieldaccess"></a><span data-ttu-id="fce03-363">メソッド checkInvalidFieldAccess</span><span class="sxs-lookup"><span data-stu-id="fce03-363">Method checkInvalidFieldAccess</span></span>

<span data-ttu-id="fce03-364">無効なフィールド アクセスを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-364">Gets and sets invalid field access.</span></span>

```xpp
public boolean checkInvalidFieldAccess([boolean checkInvalidFieldAccess])
```

### <a name="parameters---checkinvalidfieldaccess"></a><span data-ttu-id="fce03-365">パラメーター - checkInvalidFieldAccess</span><span class="sxs-lookup"><span data-stu-id="fce03-365">Parameters - checkInvalidFieldAccess</span></span>

<span data-ttu-id="fce03-366">checkInvalidFieldAccess</span><span class="sxs-lookup"><span data-stu-id="fce03-366">checkInvalidFieldAccess</span></span>  
<span data-ttu-id="fce03-367">設定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="fce03-367">The value to set; optional.</span></span>

### <a name="return-value---checkinvalidfieldaccess"></a><span data-ttu-id="fce03-368">戻り値 - checkInvalidFieldAccess</span><span class="sxs-lookup"><span data-stu-id="fce03-368">Return Value - checkInvalidFieldAccess</span></span>

<span data-ttu-id="fce03-369">無効なフィールド アクセス権が設定されている場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fce03-369">true if invalid field access is set; otherwise, false.</span></span>

## <a name="method-checkrecord"></a><span data-ttu-id="fce03-370">メソッド checkRecord</span><span class="sxs-lookup"><span data-stu-id="fce03-370">Method checkRecord</span></span>

<span data-ttu-id="fce03-371">必須フィールドをチェックするかどうかを示すプロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-371">Gets and sets the property that indicates whether to check mandatory fields.</span></span>

```xpp
public boolean checkRecord([boolean checkMandatoryFields])
```

### <a name="parameters---checkrecord"></a><span data-ttu-id="fce03-372">パラメーター - checkRecord</span><span class="sxs-lookup"><span data-stu-id="fce03-372">Parameters - checkRecord</span></span>

<span data-ttu-id="fce03-373">checkMandatoryFields</span><span class="sxs-lookup"><span data-stu-id="fce03-373">checkMandatoryFields</span></span>  
<span data-ttu-id="fce03-374">必須フィールドをチェックするかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="fce03-374">A Boolean value that indicates whether to check mandatory fields; optional.</span></span>

### <a name="return-value---checkrecord"></a><span data-ttu-id="fce03-375">戻り値 - checkRecord</span><span class="sxs-lookup"><span data-stu-id="fce03-375">Return Value - checkRecord</span></span>

<span data-ttu-id="fce03-376">必須項目がオンになっている場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fce03-376">true if mandatory fields are checked; otherwise, false.</span></span>

## <a name="method-checkrestricteddeleteactions"></a><span data-ttu-id="fce03-377">メソッド checkRestrictedDeleteActions</span><span class="sxs-lookup"><span data-stu-id="fce03-377">Method checkRestrictedDeleteActions</span></span>

<span data-ttu-id="fce03-378">レコードが削除されるかどうかを示すプロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-378">Gets and sets the property that indicates whether a record can be deleted.</span></span>

```xpp
public boolean checkRestrictedDeleteActions([boolean checkRestrictedDeleteActions])
```

### <a name="parameters---checkrestricteddeleteactions"></a><span data-ttu-id="fce03-379">パラメーター - checkRestrictedDeleteActions</span><span class="sxs-lookup"><span data-stu-id="fce03-379">Parameters - checkRestrictedDeleteActions</span></span>

<span data-ttu-id="fce03-380">checkRestrictedDeleteActions</span><span class="sxs-lookup"><span data-stu-id="fce03-380">checkRestrictedDeleteActions</span></span>  
<span data-ttu-id="fce03-381">レコードが削除できるかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="fce03-381">A Boolean value that indicates whether a record can be deleted; optional.</span></span>

### <a name="return-value---checkrestricteddeleteactions"></a><span data-ttu-id="fce03-382">戻り値 - checkRestrictedDeleteActions</span><span class="sxs-lookup"><span data-stu-id="fce03-382">Return Value - checkRestrictedDeleteActions</span></span>

<span data-ttu-id="fce03-383">レコードを削除することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fce03-383">true if the record can be deleted; otherwise, false.</span></span>

### <a name="remarks---checkrestricteddeleteactions"></a><span data-ttu-id="fce03-384">備考 - checkRestrictedDeleteActions</span><span class="sxs-lookup"><span data-stu-id="fce03-384">Remarks - checkRestrictedDeleteActions</span></span>

<span data-ttu-id="fce03-385">プロパティはテーブルの削除アクションと、対応するレコードが対応するテーブルにあるときにテーブルが削除アクションを許可するかどうかに基づいています。</span><span class="sxs-lookup"><span data-stu-id="fce03-385">The property is based on delete actions for a table, and whether the table allows for delete actions when corresponding records are in corresponding tables.</span></span>

## <a name="method-company"></a><span data-ttu-id="fce03-386">メソッド company</span><span class="sxs-lookup"><span data-stu-id="fce03-386">Method company</span></span>

<span data-ttu-id="fce03-387">レコードの法人を示すプロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-387">Gets and sets the property that indicates a legal entity for the record.</span></span>

```xpp
public SelectableDataArea company([SelectableDataArea company])
```

### <a name="parameters---company"></a><span data-ttu-id="fce03-388">パラメーター - company</span><span class="sxs-lookup"><span data-stu-id="fce03-388">Parameters - company</span></span>

<span data-ttu-id="fce03-389">会社</span><span class="sxs-lookup"><span data-stu-id="fce03-389">company</span></span>  
<span data-ttu-id="fce03-390">レコードの新しい法人 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="fce03-390">A new legal entity for the record; optional.</span></span>

### <a name="return-value---company"></a><span data-ttu-id="fce03-391">戻り値 - company</span><span class="sxs-lookup"><span data-stu-id="fce03-391">Return Value - company</span></span>

<span data-ttu-id="fce03-392">法人 ID。</span><span class="sxs-lookup"><span data-stu-id="fce03-392">The legal entity ID.</span></span>

## <a name="method-con2buf"></a><span data-ttu-id="fce03-393">メソッド con2buf</span><span class="sxs-lookup"><span data-stu-id="fce03-393">Method con2buf</span></span>

<span data-ttu-id="fce03-394">コンテナをテーブル バッファに展開します。</span><span class="sxs-lookup"><span data-stu-id="fce03-394">Unpacks a container into the table buffers.</span></span>

```xpp
public Common con2buf(container container)
```

### <a name="parameters---con2buf"></a><span data-ttu-id="fce03-395">パラメーター - con2buf</span><span class="sxs-lookup"><span data-stu-id="fce03-395">Parameters - con2buf</span></span>

<span data-ttu-id="fce03-396">コンテナー</span><span class="sxs-lookup"><span data-stu-id="fce03-396">container</span></span>  

### <a name="return-value---con2buf"></a><span data-ttu-id="fce03-397">戻り値 - con2buf</span><span class="sxs-lookup"><span data-stu-id="fce03-397">Return Value - con2buf</span></span>

## <a name="method-concurrencymodel"></a><span data-ttu-id="fce03-398">メソッド concurrencyModel</span><span class="sxs-lookup"><span data-stu-id="fce03-398">Method concurrencyModel</span></span>

<span data-ttu-id="fce03-399">レコードの更新に使用する既定の同時実行モデルを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-399">Gets and sets the default concurrency model to use to update records.</span></span>

```xpp
public ConcurrencyModel concurrencyModel([ConcurrencyModel concurrencyModel])
```

### <a name="parameters---concurrencymodel"></a><span data-ttu-id="fce03-400">パラメーター - concurrencyModel</span><span class="sxs-lookup"><span data-stu-id="fce03-400">Parameters - concurrencyModel</span></span>

<span data-ttu-id="fce03-401">concurrencyModel</span><span class="sxs-lookup"><span data-stu-id="fce03-401">concurrencyModel</span></span>  
<span data-ttu-id="fce03-402">既定では、新しい同時実行モデル (オプション)。</span><span class="sxs-lookup"><span data-stu-id="fce03-402">The new concurrency model, by default; optional.</span></span>

### <a name="return-value---concurrencymodel"></a><span data-ttu-id="fce03-403">戻り値 - concurrencyModel</span><span class="sxs-lookup"><span data-stu-id="fce03-403">Return Value - concurrencyModel</span></span>

<span data-ttu-id="fce03-404">既定値では、同時実行モデル プロパティの現在の値です。</span><span class="sxs-lookup"><span data-stu-id="fce03-404">The current value of the concurrency model property, by default.</span></span>

## <a name="method-context"></a><span data-ttu-id="fce03-405">メソッド context</span><span class="sxs-lookup"><span data-stu-id="fce03-405">Method context</span></span>

<span data-ttu-id="fce03-406">コンテキスト プロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-406">Gets and sets the context property.</span></span>

```xpp
public int context([int newValue])
```

### <a name="parameters---context"></a><span data-ttu-id="fce03-407">パラメーター - context</span><span class="sxs-lookup"><span data-stu-id="fce03-407">Parameters - context</span></span>

<span data-ttu-id="fce03-408">newValue</span><span class="sxs-lookup"><span data-stu-id="fce03-408">newValue</span></span>  
<span data-ttu-id="fce03-409">コンテキスト プロパティの新しい値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="fce03-409">The new value of the context property; optional.</span></span>

### <a name="return-value---context"></a><span data-ttu-id="fce03-410">戻り値 - context</span><span class="sxs-lookup"><span data-stu-id="fce03-410">Return Value - context</span></span>

<span data-ttu-id="fce03-411">コンテキスト プロパティの現在の値。</span><span class="sxs-lookup"><span data-stu-id="fce03-411">The current value of the context property.</span></span>

## <a name="method-data"></a><span data-ttu-id="fce03-412">メソッド data</span><span class="sxs-lookup"><span data-stu-id="fce03-412">Method data</span></span>

<span data-ttu-id="fce03-413">テーブルから行を取得します。</span><span class="sxs-lookup"><span data-stu-id="fce03-413">Retrieves a row from the table.</span></span>

```xpp
public Common data([Common cursor])
```

### <a name="parameters---data"></a><span data-ttu-id="fce03-414">パラメーター - data</span><span class="sxs-lookup"><span data-stu-id="fce03-414">Parameters - data</span></span>

<span data-ttu-id="fce03-415">cursor</span><span class="sxs-lookup"><span data-stu-id="fce03-415">cursor</span></span>  
<span data-ttu-id="fce03-416">取得する行 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="fce03-416">The row to retrieve; optional.</span></span>

### <a name="return-value---data"></a><span data-ttu-id="fce03-417">戻り値 - data</span><span class="sxs-lookup"><span data-stu-id="fce03-417">Return Value - data</span></span>

<span data-ttu-id="fce03-418">レコード バッファ。</span><span class="sxs-lookup"><span data-stu-id="fce03-418">The record buffer.</span></span>

### <a name="remarks---data"></a><span data-ttu-id="fce03-419">備考 - data</span><span class="sxs-lookup"><span data-stu-id="fce03-419">Remarks - data</span></span>

<span data-ttu-id="fce03-420">1 つの理由としてテーブルの継承が関係するシナリオのため、グローバル クラスで con2buf、buf2con、および buf2buf メソッドを代わりに使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="fce03-420">Partly because scenarios that involve table inheritance, we recommend that you instead use the following methods on the Global class: con2buf, buf2con, and buf2buf.</span></span>

## <a name="method-datasource"></a><span data-ttu-id="fce03-421">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="fce03-421">Method dataSource</span></span>

<span data-ttu-id="fce03-422">テーブルのデータ ソースを取得します。</span><span class="sxs-lookup"><span data-stu-id="fce03-422">Retrieves the data source of the table.</span></span>

```xpp
public FormObjectSet dataSource()
```

### <a name="return-value---datasource"></a><span data-ttu-id="fce03-423">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="fce03-423">Return Value - dataSource</span></span>

<span data-ttu-id="fce03-424">テーブルのデータ ソース。</span><span class="sxs-lookup"><span data-stu-id="fce03-424">The data source of the table.</span></span>

## <a name="method-disablecache"></a><span data-ttu-id="fce03-425">メソッド disableCache</span><span class="sxs-lookup"><span data-stu-id="fce03-425">Method disableCache</span></span>

<span data-ttu-id="fce03-426">キャッシュが無効かどうかを示すプロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-426">Gets and sets the property that indicates whether caching is disabled.</span></span>

```xpp
public boolean disableCache([boolean newValue])
```

### <a name="parameters---disablecache"></a><span data-ttu-id="fce03-427">パラメーター - disableCache</span><span class="sxs-lookup"><span data-stu-id="fce03-427">Parameters - disableCache</span></span>

<span data-ttu-id="fce03-428">newValue</span><span class="sxs-lookup"><span data-stu-id="fce03-428">newValue</span></span>  
<span data-ttu-id="fce03-429">キャッシュが無効かどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="fce03-429">A Boolean value that indicates whether caching is disabled.</span></span>

### <a name="return-value---disablecache"></a><span data-ttu-id="fce03-430">戻り値 - disableCache</span><span class="sxs-lookup"><span data-stu-id="fce03-430">Return Value - disableCache</span></span>

<span data-ttu-id="fce03-431">無効なキャッシュ プロパティの新しい値。</span><span class="sxs-lookup"><span data-stu-id="fce03-431">The new value of the disable cache property.</span></span>

## <a name="method-dovalidatedelete"></a><span data-ttu-id="fce03-432">メソッド doValidateDelete</span><span class="sxs-lookup"><span data-stu-id="fce03-432">Method doValidateDelete</span></span>

<span data-ttu-id="fce03-433">レコードを削除できる検証するアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="fce03-433">Performs the action to validate that a record can be deleted.</span></span>

```xpp
public boolean doValidateDelete()
```

### <a name="return-value---dovalidatedelete"></a><span data-ttu-id="fce03-434">戻り値 - doValidateDelete</span><span class="sxs-lookup"><span data-stu-id="fce03-434">Return Value - doValidateDelete</span></span>

## <a name="method-equal"></a><span data-ttu-id="fce03-435">メソッド equal</span><span class="sxs-lookup"><span data-stu-id="fce03-435">Method equal</span></span>

<span data-ttu-id="fce03-436">指定されたオブジェクトが現在のオブジェクトと等しいかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-436">Determines whether the specified object is equal to the current one.</span></span>

```xpp
public boolean equal(Common cursor)
```

### <a name="parameters---equal"></a><span data-ttu-id="fce03-437">パラメーター - equal</span><span class="sxs-lookup"><span data-stu-id="fce03-437">Parameters - equal</span></span>

<span data-ttu-id="fce03-438">cursor</span><span class="sxs-lookup"><span data-stu-id="fce03-438">cursor</span></span>  
<span data-ttu-id="fce03-439">等しいかどうかをチェックするオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="fce03-439">The object to check for equality.</span></span>

### <a name="return-value---equal"></a><span data-ttu-id="fce03-440">戻り値 - equal</span><span class="sxs-lookup"><span data-stu-id="fce03-440">Return Value - equal</span></span>

<span data-ttu-id="fce03-441">オブジェクトが等しい場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fce03-441">true if the objects are equal; otherwise, false.</span></span>

### <a name="remarks---equal"></a><span data-ttu-id="fce03-442">備考 - equal</span><span class="sxs-lookup"><span data-stu-id="fce03-442">Remarks - equal</span></span>

<span data-ttu-id="fce03-443">このメソッドは上書きされます。</span><span class="sxs-lookup"><span data-stu-id="fce03-443">This method is overridden.</span></span> <span data-ttu-id="fce03-444">Object::equal メソッドの既定の実装では、照会の等価性のみをサポートします。</span><span class="sxs-lookup"><span data-stu-id="fce03-444">The default implementation of the Object::equal method supports only reference equality.</span></span> <span data-ttu-id="fce03-445">派生クラスは、値の等価性をサポートするために Object::equal メソッドを上書きできます。</span><span class="sxs-lookup"><span data-stu-id="fce03-445">Derived classes can override the Object::equal method to support value equality.</span></span>

## <a name="method-fieldaccessright"></a><span data-ttu-id="fce03-446">メソッド fieldAccessRight</span><span class="sxs-lookup"><span data-stu-id="fce03-446">Method fieldAccessRight</span></span>

<span data-ttu-id="fce03-447">フィールドのアクセス権を返します。</span><span class="sxs-lookup"><span data-stu-id="fce03-447">Returns the field access right.</span></span>

```xpp
public AccessRight fieldAccessRight(FieldName fieldName)
```

### <a name="parameters---fieldaccessright"></a><span data-ttu-id="fce03-448">パラメーター - fieldAccessRight</span><span class="sxs-lookup"><span data-stu-id="fce03-448">Parameters - fieldAccessRight</span></span>

<span data-ttu-id="fce03-449">fieldName</span><span class="sxs-lookup"><span data-stu-id="fce03-449">fieldName</span></span>  
<span data-ttu-id="fce03-450">フィールド アクセス権を取得するフィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="fce03-450">The name of the field for which to obtain the field access right.</span></span>

### <a name="return-value---fieldaccessright"></a><span data-ttu-id="fce03-451">戻り値 - fieldAccessRight</span><span class="sxs-lookup"><span data-stu-id="fce03-451">Return Value - fieldAccessRight</span></span>

<span data-ttu-id="fce03-452">フィールドのフィールド アクセス権限。</span><span class="sxs-lookup"><span data-stu-id="fce03-452">The field access right for the field.</span></span>

## <a name="method-fieldbufferaccessright"></a><span data-ttu-id="fce03-453">メソッド fieldBufferAccessRight</span><span class="sxs-lookup"><span data-stu-id="fce03-453">Method fieldBufferAccessRight</span></span>

<span data-ttu-id="fce03-454">現在のレコードのフィールド アクセス権を返します。</span><span class="sxs-lookup"><span data-stu-id="fce03-454">Returns the field access right for the current record.</span></span>

```xpp
public AccessRight fieldBufferAccessRight(FieldName fieldName)
```

### <a name="parameters---fieldbufferaccessright"></a><span data-ttu-id="fce03-455">パラメーター - fieldBufferAccessRight</span><span class="sxs-lookup"><span data-stu-id="fce03-455">Parameters - fieldBufferAccessRight</span></span>

<span data-ttu-id="fce03-456">fieldName</span><span class="sxs-lookup"><span data-stu-id="fce03-456">fieldName</span></span>  
<span data-ttu-id="fce03-457">フィールド アクセス権を取得するフィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="fce03-457">The name of the field for which to obtain the field access right.</span></span>

### <a name="return-value---fieldbufferaccessright"></a><span data-ttu-id="fce03-458">戻り値 - fieldBufferAccessRight</span><span class="sxs-lookup"><span data-stu-id="fce03-458">Return Value - fieldBufferAccessRight</span></span>

<span data-ttu-id="fce03-459">フィールド アクセス権限。</span><span class="sxs-lookup"><span data-stu-id="fce03-459">The field access right.</span></span>

## <a name="method-fieldstate"></a><span data-ttu-id="fce03-460">メソッド fieldState</span><span class="sxs-lookup"><span data-stu-id="fce03-460">Method fieldState</span></span>

<span data-ttu-id="fce03-461">テーブル バッファーのフィールドの状態を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="fce03-461">Sets or returns the state of a field in the table buffer.</span></span>

```xpp
public FieldState fieldState(FieldId fieldId, [FieldState state])
```

### <a name="parameters---fieldstate"></a><span data-ttu-id="fce03-462">パラメーター - fieldState</span><span class="sxs-lookup"><span data-stu-id="fce03-462">Parameters - fieldState</span></span>

<span data-ttu-id="fce03-463">fieldId</span><span class="sxs-lookup"><span data-stu-id="fce03-463">fieldId</span></span>  

<!-- -->

<span data-ttu-id="fce03-464">状態</span><span class="sxs-lookup"><span data-stu-id="fce03-464">state</span></span>  

### <a name="return-value---fieldstate"></a><span data-ttu-id="fce03-465">戻り値 - fieldState</span><span class="sxs-lookup"><span data-stu-id="fce03-465">Return Value - fieldState</span></span>

<span data-ttu-id="fce03-466">フィールドの古い状態。</span><span class="sxs-lookup"><span data-stu-id="fce03-466">The old state of the field.</span></span>

## <a name="method-getallowredefault"></a><span data-ttu-id="fce03-467">メソッド getAllowRedefault</span><span class="sxs-lookup"><span data-stu-id="fce03-467">Method getAllowRedefault</span></span>

<span data-ttu-id="fce03-468">既定値に再度設定することを許可されているフィールドの一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="fce03-468">Returns the list of fields that are allowed to re-default.</span></span>

```xpp
public container getAllowRedefault()
```

### <a name="return-value---getallowredefault"></a><span data-ttu-id="fce03-469">戻り値 - getAllowRedefault</span><span class="sxs-lookup"><span data-stu-id="fce03-469">Return Value - getAllowRedefault</span></span>

<span data-ttu-id="fce03-470">フィールドを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="fce03-470">The container that holds the fields.</span></span>

## <a name="method-getdefaultingdependencies"></a><span data-ttu-id="fce03-471">メソッド getDefaultingDependencies</span><span class="sxs-lookup"><span data-stu-id="fce03-471">Method getDefaultingDependencies</span></span>

<span data-ttu-id="fce03-472">デフォルトの依存関係を保持するコンテナーを返します。</span><span class="sxs-lookup"><span data-stu-id="fce03-472">Returns the container that holds defaulting dependencies.</span></span>

```xpp
public container getDefaultingDependencies()
```

### <a name="return-value---getdefaultingdependencies"></a><span data-ttu-id="fce03-473">戻り値 - getDefaultingDependencies</span><span class="sxs-lookup"><span data-stu-id="fce03-473">Return Value - getDefaultingDependencies</span></span>

<span data-ttu-id="fce03-474">デフォルトの依存関係を保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="fce03-474">The container that holds defaulting dependencies.</span></span>

## <a name="method-getextension"></a><span data-ttu-id="fce03-475">メソッド getExtension</span><span class="sxs-lookup"><span data-stu-id="fce03-475">Method getExtension</span></span>

<span data-ttu-id="fce03-476">テーブル拡張機能を返します。</span><span class="sxs-lookup"><span data-stu-id="fce03-476">Returns the table extension.</span></span>

```xpp
public TableExtension getExtension()
```

### <a name="return-value---getextension"></a><span data-ttu-id="fce03-477">戻り値 - getExtension</span><span class="sxs-lookup"><span data-stu-id="fce03-477">Return Value - getExtension</span></span>

<span data-ttu-id="fce03-478">テーブル拡張</span><span class="sxs-lookup"><span data-stu-id="fce03-478">The table extension.</span></span>

## <a name="method-getfieldvalue"></a><span data-ttu-id="fce03-479">メソッド getFieldValue</span><span class="sxs-lookup"><span data-stu-id="fce03-479">Method getFieldValue</span></span>

<span data-ttu-id="fce03-480">テーブル バッファから指定したフィールドの値を取得します。</span><span class="sxs-lookup"><span data-stu-id="fce03-480">Gets the value of the specified field from a table buffer.</span></span>

```xpp
public AnyType getFieldValue(str fieldName, [int arrayIndex])
```

### <a name="parameters---getfieldvalue"></a><span data-ttu-id="fce03-481">パラメーター - getFieldValue</span><span class="sxs-lookup"><span data-stu-id="fce03-481">Parameters - getFieldValue</span></span>

<span data-ttu-id="fce03-482">fieldName</span><span class="sxs-lookup"><span data-stu-id="fce03-482">fieldName</span></span>  
<span data-ttu-id="fce03-483">フィールドの配列インデックス (省略可能)。</span><span class="sxs-lookup"><span data-stu-id="fce03-483">The array index of the field; optional.</span></span>

<!-- -->

<span data-ttu-id="fce03-484">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="fce03-484">arrayIndex</span></span>  
<span data-ttu-id="fce03-485">フィールドの配列インデックス (省略可能)。</span><span class="sxs-lookup"><span data-stu-id="fce03-485">The array index of the field; optional.</span></span>

### <a name="return-value---getfieldvalue"></a><span data-ttu-id="fce03-486">戻り値 - getFieldValue</span><span class="sxs-lookup"><span data-stu-id="fce03-486">Return Value - getFieldValue</span></span>

<span data-ttu-id="fce03-487">フィールドの値。</span><span class="sxs-lookup"><span data-stu-id="fce03-487">The value of a field.</span></span>

### <a name="remarks---getfieldvalue"></a><span data-ttu-id="fce03-488">備考 - getFieldValue</span><span class="sxs-lookup"><span data-stu-id="fce03-488">Remarks - getFieldValue</span></span>

<span data-ttu-id="fce03-489">arrayIndex パラメーターは、配列フィールドにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="fce03-489">The arrayIndex parameter only applies to array fields.</span></span> <span data-ttu-id="fce03-490">配列でないフィールドには、このパラメーターを省略するか、または 0 (ゼロ) を指定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-490">Either omit this parameter or specify 0 (zero) for fields that are not arrays.</span></span> <span data-ttu-id="fce03-491">指定されたフィールドが不明な場合、このメソッドは ArgumentOutOfRange 例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="fce03-491">This method throws an ArgumentOutOfRange exception if the specified field is unknown.</span></span>

## <a name="method-getinstancerelationtype"></a><span data-ttu-id="fce03-492">メソッド getInstanceRelationType</span><span class="sxs-lookup"><span data-stu-id="fce03-492">Method getInstanceRelationType</span></span>

<span data-ttu-id="fce03-493">InstanceRelationType ID に対応するテーブルの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="fce03-493">Returns the table name that corresponds to the InstanceRelationType ID.</span></span>

```xpp
public str getInstanceRelationType()
```

### <a name="return-value---getinstancerelationtype"></a><span data-ttu-id="fce03-494">戻り値 - getInstanceRelationType</span><span class="sxs-lookup"><span data-stu-id="fce03-494">Return Value - getInstanceRelationType</span></span>

<span data-ttu-id="fce03-495">InstanceRelationType ID に対応するテーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="fce03-495">The table name that corresponds to the InstanceRelationType ID.</span></span>

## <a name="method-getphysicaltablename"></a><span data-ttu-id="fce03-496">メソッド getPhysicalTableName</span><span class="sxs-lookup"><span data-stu-id="fce03-496">Method getPhysicalTableName</span></span>

<span data-ttu-id="fce03-497">物理テーブル名を返します。SQL Temp DB テーブルの場合は、テーブル インスタンス名です。</span><span class="sxs-lookup"><span data-stu-id="fce03-497">Return the physical table name, which, in the case of the SQL Temp DB table, is the table instance name.</span></span>

```xpp
public str getPhysicalTableName()
```

### <a name="return-value---getphysicaltablename"></a><span data-ttu-id="fce03-498">戻り値 - getPhysicalTableName</span><span class="sxs-lookup"><span data-stu-id="fce03-498">Return Value - getPhysicalTableName</span></span>

<span data-ttu-id="fce03-499">物理テーブル名またはテーブル インスタンス名。</span><span class="sxs-lookup"><span data-stu-id="fce03-499">The physical table name or the table instance name.</span></span>

## <a name="method-getpresencefielddata"></a><span data-ttu-id="fce03-500">メソッド getPresenceFieldData</span><span class="sxs-lookup"><span data-stu-id="fce03-500">Method getPresenceFieldData</span></span>

<span data-ttu-id="fce03-501">指定されたフィールドから PresenceInfo 値を取得します。</span><span class="sxs-lookup"><span data-stu-id="fce03-501">Retrieves the PresenceInfo value from the specified field.</span></span>

```xpp
public PresenceInfo getPresenceFieldData(FieldId fieldId, AnyType fieldValue)
```

### <a name="parameters---getpresencefielddata"></a><span data-ttu-id="fce03-502">パラメーター - getPresenceFieldData</span><span class="sxs-lookup"><span data-stu-id="fce03-502">Parameters - getPresenceFieldData</span></span>

<span data-ttu-id="fce03-503">fieldId</span><span class="sxs-lookup"><span data-stu-id="fce03-503">fieldId</span></span>  

<!-- -->

<span data-ttu-id="fce03-504">fieldValue</span><span class="sxs-lookup"><span data-stu-id="fce03-504">fieldValue</span></span>  

### <a name="return-value---getpresencefielddata"></a><span data-ttu-id="fce03-505">戻り値 - getPresenceFieldData</span><span class="sxs-lookup"><span data-stu-id="fce03-505">Return Value - getPresenceFieldData</span></span>

## <a name="method-getsqlstatement"></a><span data-ttu-id="fce03-506">メソッド getSQLStatement</span><span class="sxs-lookup"><span data-stu-id="fce03-506">Method getSQLStatement</span></span>

<span data-ttu-id="fce03-507">レコードをデータベースから取得するために使用される SQL ステートメントを取得します。</span><span class="sxs-lookup"><span data-stu-id="fce03-507">Gets the SQL statement that is used to return records from the database.</span></span>

```xpp
public str getSQLStatement()
```

### <a name="return-value---getsqlstatement"></a><span data-ttu-id="fce03-508">戻り値 - getSQLStatement</span><span class="sxs-lookup"><span data-stu-id="fce03-508">Return Value - getSQLStatement</span></span>

<span data-ttu-id="fce03-509">SQL ステートメントを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="fce03-509">The string that contains the SQL statement.</span></span>

## <a name="method-gettableininstancehierarchy"></a><span data-ttu-id="fce03-510">メソッド getTableInInstanceHierarchy</span><span class="sxs-lookup"><span data-stu-id="fce03-510">Method getTableInInstanceHierarchy</span></span>

```xpp
public Common getTableInInstanceHierarchy(TableId tableId)
```

### <a name="parameters---gettableininstancehierarchy"></a><span data-ttu-id="fce03-511">パラメーター - getTableInInstanceHierarchy</span><span class="sxs-lookup"><span data-stu-id="fce03-511">Parameters - getTableInInstanceHierarchy</span></span>

<span data-ttu-id="fce03-512">tableId</span><span class="sxs-lookup"><span data-stu-id="fce03-512">tableId</span></span>  

### <a name="return-value---gettableininstancehierarchy"></a><span data-ttu-id="fce03-513">戻り値 - getTableInInstanceHierarchy</span><span class="sxs-lookup"><span data-stu-id="fce03-513">Return Value - getTableInInstanceHierarchy</span></span>

## <a name="method-gettabletype"></a><span data-ttu-id="fce03-514">メソッド getTableType</span><span class="sxs-lookup"><span data-stu-id="fce03-514">Method getTableType</span></span>

<span data-ttu-id="fce03-515">テーブルのタイプを示します。</span><span class="sxs-lookup"><span data-stu-id="fce03-515">Indicates the type of the table.</span></span>

```xpp
public TableType getTableType()
```

### <a name="return-value---gettabletype"></a><span data-ttu-id="fce03-516">戻り値 - getTableType</span><span class="sxs-lookup"><span data-stu-id="fce03-516">Return Value - getTableType</span></span>

<span data-ttu-id="fce03-517">テーブルのタイプ (Regular、InMemory、TempDB)。</span><span class="sxs-lookup"><span data-stu-id="fce03-517">The type of the table (Regular, InMemory, or TempDB).</span></span>

## <a name="method-hasrelatedtable"></a><span data-ttu-id="fce03-518">メソッド hasRelatedTable</span><span class="sxs-lookup"><span data-stu-id="fce03-518">Method hasRelatedTable</span></span>

<span data-ttu-id="fce03-519">外部キー制約バッファがテーブルにリンクされているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="fce03-519">Indicates whether a foreign key constraint buffer is linked with the table.</span></span>

```xpp
public boolean hasRelatedTable(str relatedRoleName)
```

### <a name="parameters---hasrelatedtable"></a><span data-ttu-id="fce03-520">パラメーター - hasRelatedTable</span><span class="sxs-lookup"><span data-stu-id="fce03-520">Parameters - hasRelatedTable</span></span>

<span data-ttu-id="fce03-521">relatedRoleName</span><span class="sxs-lookup"><span data-stu-id="fce03-521">relatedRoleName</span></span>  

### <a name="return-value---hasrelatedtable"></a><span data-ttu-id="fce03-522">戻り値 - hasRelatedTable</span><span class="sxs-lookup"><span data-stu-id="fce03-522">Return Value - hasRelatedTable</span></span>

<span data-ttu-id="fce03-523">外部キー制約バッファがテーブルにリンクされている場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fce03-523">true if a foreign key constraint buffer is linked with the table; otherwise, false.</span></span>

## <a name="method-helpfield"></a><span data-ttu-id="fce03-524">メソッド helpField</span><span class="sxs-lookup"><span data-stu-id="fce03-524">Method helpField</span></span>

<span data-ttu-id="fce03-525">指定したフィールドのヘルプ テキストを含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="fce03-525">Retrieves a string that contains the Help text for the specified field.</span></span>

```xpp
public str helpField(FieldId fieldId)
```

### <a name="parameters---helpfield"></a><span data-ttu-id="fce03-526">パラメーター - helpField</span><span class="sxs-lookup"><span data-stu-id="fce03-526">Parameters - helpField</span></span>

<span data-ttu-id="fce03-527">fieldId</span><span class="sxs-lookup"><span data-stu-id="fce03-527">fieldId</span></span>  
<span data-ttu-id="fce03-528">ヘルプ テキストを取得するフィールド。</span><span class="sxs-lookup"><span data-stu-id="fce03-528">The field for which to retrieve the Help text.</span></span>

### <a name="return-value---helpfield"></a><span data-ttu-id="fce03-529">戻り値 - helpField</span><span class="sxs-lookup"><span data-stu-id="fce03-529">Return Value - helpField</span></span>

<span data-ttu-id="fce03-530">指定されたフィールドのヘルプ文字列。</span><span class="sxs-lookup"><span data-stu-id="fce03-530">The Help text for the specified field.</span></span>

## <a name="method-inputstatus"></a><span data-ttu-id="fce03-531">メソッド inputStatus</span><span class="sxs-lookup"><span data-stu-id="fce03-531">Method inputStatus</span></span>

<span data-ttu-id="fce03-532">テーブル バッファーの現在の入力ステータスを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="fce03-532">Sets or returns the current input status of the table buffer.</span></span>

```xpp
public FieldState inputStatus([FieldState inputStatus])
```

### <a name="parameters---inputstatus"></a><span data-ttu-id="fce03-533">パラメーター - inputStatus</span><span class="sxs-lookup"><span data-stu-id="fce03-533">Parameters - inputStatus</span></span>

<span data-ttu-id="fce03-534">inputStatus</span><span class="sxs-lookup"><span data-stu-id="fce03-534">inputStatus</span></span>  

### <a name="return-value---inputstatus"></a><span data-ttu-id="fce03-535">戻り値 - inputStatus</span><span class="sxs-lookup"><span data-stu-id="fce03-535">Return Value - inputStatus</span></span>

<span data-ttu-id="fce03-536">古い入力のステータス。</span><span class="sxs-lookup"><span data-stu-id="fce03-536">The old input status.</span></span>

## <a name="method-interactivecontext"></a><span data-ttu-id="fce03-537">メソッド interactiveContext</span><span class="sxs-lookup"><span data-stu-id="fce03-537">Method interactiveContext</span></span>

<span data-ttu-id="fce03-538">テーブル バッファーの現在のインタラクティブ コンテキストを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="fce03-538">Sets or returns the current interactive context of the table buffer.</span></span>

```xpp
public boolean interactiveContext([boolean context])
```

### <a name="parameters---interactivecontext"></a><span data-ttu-id="fce03-539">パラメーター - interactiveContext</span><span class="sxs-lookup"><span data-stu-id="fce03-539">Parameters - interactiveContext</span></span>

<span data-ttu-id="fce03-540">context</span><span class="sxs-lookup"><span data-stu-id="fce03-540">context</span></span>  

### <a name="return-value---interactivecontext"></a><span data-ttu-id="fce03-541">戻り値 - interactiveContext</span><span class="sxs-lookup"><span data-stu-id="fce03-541">Return Value - interactiveContext</span></span>

<span data-ttu-id="fce03-542">テーブル バッファーの現在の対話型コンテキスト。</span><span class="sxs-lookup"><span data-stu-id="fce03-542">The current interactive context of the table buffer.</span></span>

## <a name="method-isfielddataretrieved"></a><span data-ttu-id="fce03-543">メソッド isFieldDataRetrieved</span><span class="sxs-lookup"><span data-stu-id="fce03-543">Method isFieldDataRetrieved</span></span>

<span data-ttu-id="fce03-544">指定されたフィールドのデータが取得されたかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="fce03-544">Checks whether the data of the given field has been retrieved.</span></span>

```xpp
public boolean isFieldDataRetrieved(str fieldName, [int arrayIndex])
```

### <a name="parameters---isfielddataretrieved"></a><span data-ttu-id="fce03-545">パラメーター - isFieldDataRetrieved</span><span class="sxs-lookup"><span data-stu-id="fce03-545">Parameters - isFieldDataRetrieved</span></span>

<span data-ttu-id="fce03-546">fieldName</span><span class="sxs-lookup"><span data-stu-id="fce03-546">fieldName</span></span>  

<!-- -->

<span data-ttu-id="fce03-547">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="fce03-547">arrayIndex</span></span>  

### <a name="return-value---isfielddataretrieved"></a><span data-ttu-id="fce03-548">戻り値 - isFieldDataRetrieved</span><span class="sxs-lookup"><span data-stu-id="fce03-548">Return Value - isFieldDataRetrieved</span></span>

<span data-ttu-id="fce03-549">データが取得済みの場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fce03-549">true if the data has been retrieved; otherwise, false.</span></span>

## <a name="method-isfieldset"></a><span data-ttu-id="fce03-550">メソッド isFieldSet</span><span class="sxs-lookup"><span data-stu-id="fce03-550">Method isFieldSet</span></span>

<span data-ttu-id="fce03-551">フィールドがセットまたは既定状態かどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="fce03-551">Checks whether a field has a Set or Defaulted state.</span></span>

```xpp
public boolean isFieldSet(FieldId fieldId)
```

### <a name="parameters---isfieldset"></a><span data-ttu-id="fce03-552">パラメーター - isFieldSet</span><span class="sxs-lookup"><span data-stu-id="fce03-552">Parameters - isFieldSet</span></span>

<span data-ttu-id="fce03-553">fieldId</span><span class="sxs-lookup"><span data-stu-id="fce03-553">fieldId</span></span>  

### <a name="return-value---isfieldset"></a><span data-ttu-id="fce03-554">戻り値 - isFieldSet</span><span class="sxs-lookup"><span data-stu-id="fce03-554">Return Value - isFieldSet</span></span>

<span data-ttu-id="fce03-555">フィールドがセット状態または既定状態の場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fce03-555">true if field has a Set or Defaulted state; otherwise, false.</span></span>

## <a name="method-isformdatasource"></a><span data-ttu-id="fce03-556">メソッド isFormDataSource</span><span class="sxs-lookup"><span data-stu-id="fce03-556">Method isFormDataSource</span></span>

<span data-ttu-id="fce03-557">データ ソースがフォームであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="fce03-557">Indicates whether the data source is a form.</span></span>

```xpp
public boolean isFormDataSource()
```

### <a name="return-value---isformdatasource"></a><span data-ttu-id="fce03-558">戻り値 - isFormDataSource</span><span class="sxs-lookup"><span data-stu-id="fce03-558">Return Value - isFormDataSource</span></span>

<span data-ttu-id="fce03-559">データ ソースがフォームである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fce03-559">true if the data source is a form; otherwise, false.</span></span>

## <a name="method-isnewrecord"></a><span data-ttu-id="fce03-560">メソッド isNewRecord</span><span class="sxs-lookup"><span data-stu-id="fce03-560">Method isNewRecord</span></span>

<span data-ttu-id="fce03-561">レコードがまだ保存されていない新しいレコードである場合は true を返します。</span><span class="sxs-lookup"><span data-stu-id="fce03-561">Returns true if the record is a new record that hasn't been persisted yet.</span></span>

```xpp
public boolean isNewRecord()
```

### <a name="return-value---isnewrecord"></a><span data-ttu-id="fce03-562">戻り値 - isNewRecord</span><span class="sxs-lookup"><span data-stu-id="fce03-562">Return Value - isNewRecord</span></span>

<span data-ttu-id="fce03-563">レコードがまだ保存されていない新しいレコードである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fce03-563">true if the record is a new record that hasn't been persisted yet; otherwise, false.</span></span>

## <a name="method-ispartofuowsavechanges"></a><span data-ttu-id="fce03-564">メソッド isPartOfUOWSaveChanges</span><span class="sxs-lookup"><span data-stu-id="fce03-564">Method isPartOfUOWSaveChanges</span></span>

```xpp
public boolean isPartOfUOWSaveChanges()
```

### <a name="return-value---ispartofuowsavechanges"></a><span data-ttu-id="fce03-565">戻り値 - isPartOfUOWSaveChanges</span><span class="sxs-lookup"><span data-stu-id="fce03-565">Return Value - isPartOfUOWSaveChanges</span></span>

## <a name="method-istempdb"></a><span data-ttu-id="fce03-566">メソッド isTempDb</span><span class="sxs-lookup"><span data-stu-id="fce03-566">Method isTempDb</span></span>

<span data-ttu-id="fce03-567">テーブルのタイプが SQL TempDB であるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="fce03-567">Indicates whether the type of the table is SQL TempDB.</span></span>

```xpp
public boolean isTempDb()
```

### <a name="return-value---istempdb"></a><span data-ttu-id="fce03-568">戻り値 - isTempDb</span><span class="sxs-lookup"><span data-stu-id="fce03-568">Return Value - isTempDb</span></span>

<span data-ttu-id="fce03-569">テーブルのタイプが SQL TempDB である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="fce03-569">true if the type of the table is SQL TempDB; otherwise, false.</span></span>

## <a name="method-istmp"></a><span data-ttu-id="fce03-570">メソッド isTmp</span><span class="sxs-lookup"><span data-stu-id="fce03-570">Method isTmp</span></span>

<span data-ttu-id="fce03-571">これが一時テーブルであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="fce03-571">Indicates whether this is a temporary table.</span></span>

```xpp
public boolean isTmp()
```

### <a name="return-value---istmp"></a><span data-ttu-id="fce03-572">戻り値 - isTmp</span><span class="sxs-lookup"><span data-stu-id="fce03-572">Return Value - isTmp</span></span>

<span data-ttu-id="fce03-573">これが一時テーブルである場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="fce03-573">true if this is a temporary table; otherwise, false.</span></span>

## <a name="method-joinchild"></a><span data-ttu-id="fce03-574">メソッド joinChild</span><span class="sxs-lookup"><span data-stu-id="fce03-574">Method joinChild</span></span>

<span data-ttu-id="fce03-575">現在のレコードの結合子を検索します。</span><span class="sxs-lookup"><span data-stu-id="fce03-575">Finds the join child of the current record.</span></span>

```xpp
public Common joinChild()
```

### <a name="return-value---joinchild"></a><span data-ttu-id="fce03-576">戻り値 - joinChild</span><span class="sxs-lookup"><span data-stu-id="fce03-576">Return Value - joinChild</span></span>

<span data-ttu-id="fce03-577">現在のレコードの結合子。</span><span class="sxs-lookup"><span data-stu-id="fce03-577">The join child of the current record.</span></span>

## <a name="method-joinparent"></a><span data-ttu-id="fce03-578">メソッド joinParent</span><span class="sxs-lookup"><span data-stu-id="fce03-578">Method joinParent</span></span>

<span data-ttu-id="fce03-579">現在のレコードの結合の親を検索します。</span><span class="sxs-lookup"><span data-stu-id="fce03-579">Finds the join parent of the current record.</span></span>

```xpp
public Common joinParent()
```

### <a name="return-value---joinparent"></a><span data-ttu-id="fce03-580">戻り値 - joinParent</span><span class="sxs-lookup"><span data-stu-id="fce03-580">Return Value - joinParent</span></span>

<span data-ttu-id="fce03-581">現在のレコードの結合の親。</span><span class="sxs-lookup"><span data-stu-id="fce03-581">The join parent of the current record.</span></span>

## <a name="method-linkphysicaltableinstance"></a><span data-ttu-id="fce03-582">メソッド linkPhysicalTableInstance</span><span class="sxs-lookup"><span data-stu-id="fce03-582">Method linkPhysicalTableInstance</span></span>

<span data-ttu-id="fce03-583">レコードの物理テーブル インスタンスへのリンクがあるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="fce03-583">Checks whether there is a link for the physical table instance for the record.</span></span>

```xpp
public boolean linkPhysicalTableInstance([Common record])
```

### <a name="parameters---linkphysicaltableinstance"></a><span data-ttu-id="fce03-584">パラメーター - linkPhysicalTableInstance</span><span class="sxs-lookup"><span data-stu-id="fce03-584">Parameters - linkPhysicalTableInstance</span></span>

<span data-ttu-id="fce03-585">記録</span><span class="sxs-lookup"><span data-stu-id="fce03-585">record</span></span>  

### <a name="return-value---linkphysicaltableinstance"></a><span data-ttu-id="fce03-586">戻り値 - linkPhysicalTableInstance</span><span class="sxs-lookup"><span data-stu-id="fce03-586">Return Value - linkPhysicalTableInstance</span></span>

<span data-ttu-id="fce03-587">リンク使用可能かどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="fce03-587">A Boolean value that indicates whether a link is available.</span></span>

## <a name="method-orig"></a><span data-ttu-id="fce03-588">メソッド orig</span><span class="sxs-lookup"><span data-stu-id="fce03-588">Method orig</span></span>

<span data-ttu-id="fce03-589">現在のレコードの元の値を取得します。</span><span class="sxs-lookup"><span data-stu-id="fce03-589">Retrieves the original values of the current record.</span></span>

```xpp
public Common orig()
```

### <a name="return-value---orig"></a><span data-ttu-id="fce03-590">戻り値 - orig</span><span class="sxs-lookup"><span data-stu-id="fce03-590">Return Value - orig</span></span>

### <a name="remarks---orig"></a><span data-ttu-id="fce03-591">備考 - orig</span><span class="sxs-lookup"><span data-stu-id="fce03-591">Remarks - orig</span></span>

<span data-ttu-id="fce03-592">1 つの理由としてテーブルの継承が関係するシナリオのため、グローバル クラスで con2buf、buf2con、および buf2buf メソッドを代わりに使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="fce03-592">Partly because of scenarios that involve table inheritance, we recommend that you instead use the following methods on the Global class: con2buf, buf2con, and buf2buf.</span></span>

## <a name="method-overwritesystemfields"></a><span data-ttu-id="fce03-593">メソッド overwriteSystemfields</span><span class="sxs-lookup"><span data-stu-id="fce03-593">Method overwriteSystemfields</span></span>

<span data-ttu-id="fce03-594">システム フィールドを上書きできるかどうかを示すプロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-594">Gets and sets the property that indicates whether system fields can be overwritten.</span></span>

```xpp
public boolean overwriteSystemfields([boolean allowOverwrite])
```

### <a name="parameters---overwritesystemfields"></a><span data-ttu-id="fce03-595">パラメーター - overwriteSystemfields</span><span class="sxs-lookup"><span data-stu-id="fce03-595">Parameters - overwriteSystemfields</span></span>

<span data-ttu-id="fce03-596">allowOverwrite</span><span class="sxs-lookup"><span data-stu-id="fce03-596">allowOverwrite</span></span>  
<span data-ttu-id="fce03-597">システム フィールドを上書きできるかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="fce03-597">A Boolean value that indicates whether system fields can be overwritten; optional.</span></span>

### <a name="return-value---overwritesystemfields"></a><span data-ttu-id="fce03-598">戻り値 - overwriteSystemfields</span><span class="sxs-lookup"><span data-stu-id="fce03-598">Return Value - overwriteSystemfields</span></span>

<span data-ttu-id="fce03-599">システム フィールドを上書きすることができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fce03-599">true if system fields can be overwritten; otherwise, false.</span></span>

## <a name="method-querytimedout"></a><span data-ttu-id="fce03-600">メソッド queryTimedOut</span><span class="sxs-lookup"><span data-stu-id="fce03-600">Method queryTimedOut</span></span>

<span data-ttu-id="fce03-601">クエリが実行の時間制限を超過したかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="fce03-601">Indicates whether the query exceeded the time limit for execution.</span></span>

```xpp
public boolean queryTimedOut()
```

### <a name="return-value---querytimedout"></a><span data-ttu-id="fce03-602">戻り値 - queryTimedOut</span><span class="sxs-lookup"><span data-stu-id="fce03-602">Return Value - queryTimedOut</span></span>

<span data-ttu-id="fce03-603">クエリが実行の時間制限を超過した場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fce03-603">true if the query exceeded the time limit for execution; otherwise, false.</span></span>

## <a name="method-querytimeout"></a><span data-ttu-id="fce03-604">メソッド queryTimeout</span><span class="sxs-lookup"><span data-stu-id="fce03-604">Method queryTimeout</span></span>

<span data-ttu-id="fce03-605">クエリの実行に対する時間制限を示すプロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-605">Gets and sets the property that indicates the time limit for the execution of a query.</span></span>

```xpp
public int queryTimeout([int seconds], [boolean raiseException])
```

### <a name="parameters---querytimeout"></a><span data-ttu-id="fce03-606">パラメーター - queryTimeout</span><span class="sxs-lookup"><span data-stu-id="fce03-606">Parameters - queryTimeout</span></span>

<span data-ttu-id="fce03-607">秒</span><span class="sxs-lookup"><span data-stu-id="fce03-607">seconds</span></span>  

<!-- -->

<span data-ttu-id="fce03-608">raiseException</span><span class="sxs-lookup"><span data-stu-id="fce03-608">raiseException</span></span>  

### <a name="return-value---querytimeout"></a><span data-ttu-id="fce03-609">戻り値 - queryTimeout</span><span class="sxs-lookup"><span data-stu-id="fce03-609">Return Value - queryTimeout</span></span>

<span data-ttu-id="fce03-610">クエリ タイムアウト プロパティの現在の値。</span><span class="sxs-lookup"><span data-stu-id="fce03-610">The current value of the query time-out property.</span></span>

## <a name="method-readcommittedlock"></a><span data-ttu-id="fce03-611">メソッド readCommittedLock</span><span class="sxs-lookup"><span data-stu-id="fce03-611">Method readCommittedLock</span></span>

```xpp
public boolean readCommittedLock([boolean readCommittedLock])
```

### <a name="parameters---readcommittedlock"></a><span data-ttu-id="fce03-612">パラメーター - readCommittedLock</span><span class="sxs-lookup"><span data-stu-id="fce03-612">Parameters - readCommittedLock</span></span>

<span data-ttu-id="fce03-613">readCommittedLock</span><span class="sxs-lookup"><span data-stu-id="fce03-613">readCommittedLock</span></span>  

### <a name="return-value---readcommittedlock"></a><span data-ttu-id="fce03-614">戻り値 - readCommittedLock</span><span class="sxs-lookup"><span data-stu-id="fce03-614">Return Value - readCommittedLock</span></span>

## <a name="method-readpast"></a><span data-ttu-id="fce03-615">メソッド readPast</span><span class="sxs-lookup"><span data-stu-id="fce03-615">Method readPast</span></span>

<span data-ttu-id="fce03-616">レコードの読み取り時に、他のプロセスによりロックされる行をスキップするかどうかを示すプロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-616">Gets and sets the property that indicates whether to skip rows that are locked by other processes when a record is read.</span></span>

```xpp
public boolean readPast([boolean skipLockedRows])
```

### <a name="parameters---readpast"></a><span data-ttu-id="fce03-617">パラメーター - readPast</span><span class="sxs-lookup"><span data-stu-id="fce03-617">Parameters - readPast</span></span>

<span data-ttu-id="fce03-618">skipLockedRows</span><span class="sxs-lookup"><span data-stu-id="fce03-618">skipLockedRows</span></span>  
<span data-ttu-id="fce03-619">ロックされている行をスキップするかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="fce03-619">A Boolean value that indicates whether to skip rows that are locked; optional.</span></span>

### <a name="return-value---readpast"></a><span data-ttu-id="fce03-620">戻り値 - readPast</span><span class="sxs-lookup"><span data-stu-id="fce03-620">Return Value - readPast</span></span>

<span data-ttu-id="fce03-621">ロックされた行をスキップする必要がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fce03-621">true if locked rows should be skipped; otherwise, false.</span></span>

## <a name="method-recordlevelsecurity"></a><span data-ttu-id="fce03-622">メソッド recordLevelSecurity</span><span class="sxs-lookup"><span data-stu-id="fce03-622">Method recordLevelSecurity</span></span>

<span data-ttu-id="fce03-623">レコード レベルのセキュリティを適用するかどうかを示すプロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-623">Gets and sets the property that indicates whether to apply security on a record level.</span></span>

```xpp
public boolean recordLevelSecurity([boolean newValue])
```

### <a name="parameters---recordlevelsecurity"></a><span data-ttu-id="fce03-624">パラメーター - recordLevelSecurity</span><span class="sxs-lookup"><span data-stu-id="fce03-624">Parameters - recordLevelSecurity</span></span>

<span data-ttu-id="fce03-625">newValue</span><span class="sxs-lookup"><span data-stu-id="fce03-625">newValue</span></span>  
<span data-ttu-id="fce03-626">レコード レベルのセキュリティを適用するかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="fce03-626">A Boolean value that indicates whether to apply security on a record level; optional.</span></span>

### <a name="return-value---recordlevelsecurity"></a><span data-ttu-id="fce03-627">戻り値 - recordLevelSecurity</span><span class="sxs-lookup"><span data-stu-id="fce03-627">Return Value - recordLevelSecurity</span></span>

<span data-ttu-id="fce03-628">セキュリティをレコード レベルで適用する必要がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fce03-628">true if security should be applied on a record level; otherwise, false.</span></span>

## <a name="method-relatedtable"></a><span data-ttu-id="fce03-629">メソッド relatedTable</span><span class="sxs-lookup"><span data-stu-id="fce03-629">Method relatedTable</span></span>

<span data-ttu-id="fce03-630">テーブル バッファのリンクに関連するバッファーを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="fce03-630">Sets or returns the related buffer of a link of a table buffer.</span></span>

```xpp
public Common relatedTable(str name, [Common buffer])
```

### <a name="parameters---relatedtable"></a><span data-ttu-id="fce03-631">パラメーター - relatedTable</span><span class="sxs-lookup"><span data-stu-id="fce03-631">Parameters - relatedTable</span></span>

<span data-ttu-id="fce03-632">名前</span><span class="sxs-lookup"><span data-stu-id="fce03-632">name</span></span>  

<!-- -->

<span data-ttu-id="fce03-633">バッファ</span><span class="sxs-lookup"><span data-stu-id="fce03-633">buffer</span></span>  

### <a name="return-value---relatedtable"></a><span data-ttu-id="fce03-634">戻り値 - relatedTable</span><span class="sxs-lookup"><span data-stu-id="fce03-634">Return Value - relatedTable</span></span>

<span data-ttu-id="fce03-635">テーブル バッファのリンクに関連するバッファ。</span><span class="sxs-lookup"><span data-stu-id="fce03-635">The related buffer of a link of a table buffer.</span></span>

## <a name="method-rowcount"></a><span data-ttu-id="fce03-636">メソッド RowCount</span><span class="sxs-lookup"><span data-stu-id="fce03-636">Method RowCount</span></span>

<span data-ttu-id="fce03-637">テーブル内の行数を取得します。</span><span class="sxs-lookup"><span data-stu-id="fce03-637">Retrieves the number of rows in the table.</span></span>

```xpp
public Int64 RowCount()
```

### <a name="return-value---rowcount"></a><span data-ttu-id="fce03-638">戻り値 - RowCount</span><span class="sxs-lookup"><span data-stu-id="fce03-638">Return Value - RowCount</span></span>

<span data-ttu-id="fce03-639">テーブルの行数。</span><span class="sxs-lookup"><span data-stu-id="fce03-639">The number of rows in the table.</span></span>

## <a name="method-selectforupdate"></a><span data-ttu-id="fce03-640">メソッド selectForUpdate</span><span class="sxs-lookup"><span data-stu-id="fce03-640">Method selectForUpdate</span></span>

<span data-ttu-id="fce03-641">読み取り時に更新用のレコードを選択するかどうかを示すプロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-641">Gets and sets the property that indicates whether to select records for update when they are read.</span></span>

```xpp
public boolean selectForUpdate([boolean lockRecordsExclusive])
```

### <a name="parameters---selectforupdate"></a><span data-ttu-id="fce03-642">パラメーター - selectForUpdate</span><span class="sxs-lookup"><span data-stu-id="fce03-642">Parameters - selectForUpdate</span></span>

<span data-ttu-id="fce03-643">lockRecordsExclusive</span><span class="sxs-lookup"><span data-stu-id="fce03-643">lockRecordsExclusive</span></span>  
<span data-ttu-id="fce03-644">更新のためにレコードを読み込むかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="fce03-644">A Boolean value that indicates whether to read records for update; optional.</span></span>

### <a name="return-value---selectforupdate"></a><span data-ttu-id="fce03-645">戻り値 - selectForUpdate</span><span class="sxs-lookup"><span data-stu-id="fce03-645">Return Value - selectForUpdate</span></span>

<span data-ttu-id="fce03-646">更新のためにレコードを読み取る必要がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fce03-646">true if records should be read for update; otherwise, false.</span></span>

## <a name="method-selectlocked"></a><span data-ttu-id="fce03-647">メソッド selectLocked</span><span class="sxs-lookup"><span data-stu-id="fce03-647">Method selectLocked</span></span>

<span data-ttu-id="fce03-648">ロックされているレコードを選択するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="fce03-648">Indicates whether to select locked records.</span></span>

```xpp
public boolean selectLocked([boolean lockRecordsShared])
```

### <a name="parameters---selectlocked"></a><span data-ttu-id="fce03-649">パラメーター - selectLocked</span><span class="sxs-lookup"><span data-stu-id="fce03-649">Parameters - selectLocked</span></span>

<span data-ttu-id="fce03-650">lockRecordsShared</span><span class="sxs-lookup"><span data-stu-id="fce03-650">lockRecordsShared</span></span>  
<span data-ttu-id="fce03-651">ロックされているレコードを選択するかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="fce03-651">A Boolean value that indicates whether to select locked records.</span></span>

### <a name="return-value---selectlocked"></a><span data-ttu-id="fce03-652">戻り値 - selectLocked</span><span class="sxs-lookup"><span data-stu-id="fce03-652">Return Value - selectLocked</span></span>

<span data-ttu-id="fce03-653">ロックされたレコードを選択する必要がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fce03-653">true if locked records should be selected; otherwise, false.</span></span>

## <a name="method-selectrefrecord"></a><span data-ttu-id="fce03-654">メソッド selectRefRecord</span><span class="sxs-lookup"><span data-stu-id="fce03-654">Method selectRefRecord</span></span>

<span data-ttu-id="fce03-655">参照されているフィールド ID によりレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="fce03-655">Selects the record by referenced field ID.</span></span>

```xpp
public Common selectRefRecord(FieldId referenceFieldId)
```

### <a name="parameters---selectrefrecord"></a><span data-ttu-id="fce03-656">パラメーター - selectRefRecord</span><span class="sxs-lookup"><span data-stu-id="fce03-656">Parameters - selectRefRecord</span></span>

<span data-ttu-id="fce03-657">referenceFieldId</span><span class="sxs-lookup"><span data-stu-id="fce03-657">referenceFieldId</span></span>  
<span data-ttu-id="fce03-658">参照フィールド ID。</span><span class="sxs-lookup"><span data-stu-id="fce03-658">The referenced field ID.</span></span>

### <a name="return-value---selectrefrecord"></a><span data-ttu-id="fce03-659">戻り値 - selectRefRecord</span><span class="sxs-lookup"><span data-stu-id="fce03-659">Return Value - selectRefRecord</span></span>

<span data-ttu-id="fce03-660">レコード バッファ。</span><span class="sxs-lookup"><span data-stu-id="fce03-660">The record buffer.</span></span>

## <a name="method-selectwithrepeatableread"></a><span data-ttu-id="fce03-661">メソッド selectWithRepeatableRead</span><span class="sxs-lookup"><span data-stu-id="fce03-661">Method selectWithRepeatableRead</span></span>

<span data-ttu-id="fce03-662">反復可能な読み取りが有効かどうかを示すプロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-662">Gets and sets the property that indicates whether repeatable read is enabled.</span></span>

```xpp
public boolean selectWithRepeatableRead([boolean useRepeatableRead])
```

### <a name="parameters---selectwithrepeatableread"></a><span data-ttu-id="fce03-663">パラメーター - selectWithRepeatableRead</span><span class="sxs-lookup"><span data-stu-id="fce03-663">Parameters - selectWithRepeatableRead</span></span>

<span data-ttu-id="fce03-664">useRepeatableRead</span><span class="sxs-lookup"><span data-stu-id="fce03-664">useRepeatableRead</span></span>  
<span data-ttu-id="fce03-665">反復可能な読み取りが有効かどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="fce03-665">A Boolean value that indicates whether repeatable read is enabled; optional.</span></span>

### <a name="return-value---selectwithrepeatableread"></a><span data-ttu-id="fce03-666">戻り値 - selectWithRepeatableRead</span><span class="sxs-lookup"><span data-stu-id="fce03-666">Return Value - selectWithRepeatableRead</span></span>

<span data-ttu-id="fce03-667">反復可能な読み取りが有効な場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fce03-667">true if repeatable read is enabled; otherwise, false.</span></span>

## <a name="method-settempdb"></a><span data-ttu-id="fce03-668">メソッド setTempDB</span><span class="sxs-lookup"><span data-stu-id="fce03-668">Method setTempDB</span></span>

```xpp
public boolean setTempDB()
```

### <a name="return-value---settempdb"></a><span data-ttu-id="fce03-669">戻り値 - setTempDB</span><span class="sxs-lookup"><span data-stu-id="fce03-669">Return Value - setTempDB</span></span>

## <a name="method-settmp"></a><span data-ttu-id="fce03-670">メソッド setTmp</span><span class="sxs-lookup"><span data-stu-id="fce03-670">Method setTmp</span></span>

<span data-ttu-id="fce03-671">データベースに保存されていない場合にテーブルを設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-671">Sets the table so that it is not persisted to the database.</span></span>

```xpp
public boolean setTmp()
```

### <a name="return-value---settmp"></a><span data-ttu-id="fce03-672">戻り値 - setTmp</span><span class="sxs-lookup"><span data-stu-id="fce03-672">Return Value - setTmp</span></span>

<span data-ttu-id="fce03-673">操作が成功した場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fce03-673">true if the operation was successful; otherwise, false.</span></span>

## <a name="method-skipaosvalidation"></a><span data-ttu-id="fce03-674">メソッド skipAosValidation</span><span class="sxs-lookup"><span data-stu-id="fce03-674">Method skipAosValidation</span></span>

<span data-ttu-id="fce03-675">Application Object Server (AOS) の検証をスキップするかどうかを示すプロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-675">Gets and sets the property that indicates whether to skip validation Application Object Server (AOS).</span></span>

```xpp
public boolean skipAosValidation([boolean newValue])
```

### <a name="parameters---skipaosvalidation"></a><span data-ttu-id="fce03-676">パラメーター - skipAosValidation</span><span class="sxs-lookup"><span data-stu-id="fce03-676">Parameters - skipAosValidation</span></span>

<span data-ttu-id="fce03-677">newValue</span><span class="sxs-lookup"><span data-stu-id="fce03-677">newValue</span></span>  
<span data-ttu-id="fce03-678">AOS の検証をスキップするかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="fce03-678">A Boolean value that indicates whether to skip AOS validation.</span></span>

### <a name="return-value---skipaosvalidation"></a><span data-ttu-id="fce03-679">戻り値 - skipAosValidation</span><span class="sxs-lookup"><span data-stu-id="fce03-679">Return Value - skipAosValidation</span></span>

<span data-ttu-id="fce03-680">AOS 検証をスキップする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="fce03-680">true if AOS validation should be skipped; otherwise, false.</span></span>

### <a name="remarks---skipaosvalidation"></a><span data-ttu-id="fce03-681">備考 - skipAosValidation</span><span class="sxs-lookup"><span data-stu-id="fce03-681">Remarks - skipAosValidation</span></span>

<span data-ttu-id="fce03-682">攻撃者が skipAosValidation メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="fce03-682">If an attacker can control input to the skipAosValidation method, a security risk exists.</span></span> <span data-ttu-id="fce03-683">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="fce03-683">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="fce03-684">サーバー上でこのメソッドを呼び出すには、SkipAOSValidationPermission クラスからのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="fce03-684">Calls to this method on the server require permission from the SkipAOSValidationPermission class.</span></span> <span data-ttu-id="fce03-685">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発ユーザー権を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fce03-685">Make sure that the user has development user rights by setting the security key to SysDevelopment on the control that calls this method.</span></span>

## <a name="method-skipdatabaselog"></a><span data-ttu-id="fce03-686">メソッド skipDatabaseLog</span><span class="sxs-lookup"><span data-stu-id="fce03-686">Method skipDatabaseLog</span></span>

<span data-ttu-id="fce03-687">データベース ログ要求をスキップするかどうかを示すプロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-687">Gets and sets the property that indicates whether to skip database log requests.</span></span>

```xpp
public boolean skipDatabaseLog([boolean newValue])
```

### <a name="parameters---skipdatabaselog"></a><span data-ttu-id="fce03-688">パラメーター - skipDatabaseLog</span><span class="sxs-lookup"><span data-stu-id="fce03-688">Parameters - skipDatabaseLog</span></span>

<span data-ttu-id="fce03-689">newValue</span><span class="sxs-lookup"><span data-stu-id="fce03-689">newValue</span></span>  
<span data-ttu-id="fce03-690">データベース ログ要求をスキップするかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="fce03-690">A Boolean value that indicates whether to skip database log requests; optional.</span></span>

### <a name="return-value---skipdatabaselog"></a><span data-ttu-id="fce03-691">戻り値 - skipDatabaseLog</span><span class="sxs-lookup"><span data-stu-id="fce03-691">Return Value - skipDatabaseLog</span></span>

<span data-ttu-id="fce03-692">データベース ログ要求をスキップする必要がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fce03-692">true if database log requests should be skipped; otherwise, false.</span></span>

## <a name="method-skipdatamethods"></a><span data-ttu-id="fce03-693">メソッド skipDataMethods</span><span class="sxs-lookup"><span data-stu-id="fce03-693">Method skipDataMethods</span></span>

<span data-ttu-id="fce03-694">オーバーロードされたメソッドを破棄するかどうかを示すプロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-694">Gets and sets the property that indicates whether to discard overloaded methods.</span></span>

```xpp
public boolean skipDataMethods([boolean newValue])
```

### <a name="parameters---skipdatamethods"></a><span data-ttu-id="fce03-695">パラメーター - skipDataMethods</span><span class="sxs-lookup"><span data-stu-id="fce03-695">Parameters - skipDataMethods</span></span>

<span data-ttu-id="fce03-696">newValue</span><span class="sxs-lookup"><span data-stu-id="fce03-696">newValue</span></span>  
<span data-ttu-id="fce03-697">オーバーロードされたメソッドを破棄するかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="fce03-697">A Boolean value that indicates whether to discard overloaded methods; optional.</span></span>

### <a name="return-value---skipdatamethods"></a><span data-ttu-id="fce03-698">戻り値 - skipDataMethods</span><span class="sxs-lookup"><span data-stu-id="fce03-698">Return Value - skipDataMethods</span></span>

<span data-ttu-id="fce03-699">オーバーロードされたメソッドを破棄する必要がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fce03-699">true if overloaded methods should be discarded; otherwise, false.</span></span>

## <a name="method-skipdeleteactions"></a><span data-ttu-id="fce03-700">メソッド skipDeleteActions</span><span class="sxs-lookup"><span data-stu-id="fce03-700">Method skipDeleteActions</span></span>

<span data-ttu-id="fce03-701">テーブルで削除アクションをスキップするかどうかを示すプロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-701">Gets and sets the property that indicates whether to skip delete actions on the table.</span></span>

```xpp
public boolean skipDeleteActions([boolean newValue])
```

### <a name="parameters---skipdeleteactions"></a><span data-ttu-id="fce03-702">パラメーター - skipDeleteActions</span><span class="sxs-lookup"><span data-stu-id="fce03-702">Parameters - skipDeleteActions</span></span>

<span data-ttu-id="fce03-703">newValue</span><span class="sxs-lookup"><span data-stu-id="fce03-703">newValue</span></span>  
<span data-ttu-id="fce03-704">レコードの削除要求を無視するかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="fce03-704">A Boolean value that indicates whether to ignore requests to delete records; optional.</span></span>

### <a name="return-value---skipdeleteactions"></a><span data-ttu-id="fce03-705">戻り値 - skipDeleteActions</span><span class="sxs-lookup"><span data-stu-id="fce03-705">Return Value - skipDeleteActions</span></span>

<span data-ttu-id="fce03-706">レコードを削除する要求を無視する必要がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fce03-706">true if requests to delete records should be ignored; otherwise, false.</span></span>

### <a name="remarks---skipdeleteactions"></a><span data-ttu-id="fce03-707">備考 - skipDeleteActions</span><span class="sxs-lookup"><span data-stu-id="fce03-707">Remarks - skipDeleteActions</span></span>

<span data-ttu-id="fce03-708">このメソッドは、delete\_from ステートメントなど、セットベースの操作を使用している場合にのみ機能します。</span><span class="sxs-lookup"><span data-stu-id="fce03-708">This method works only when you are using a set-based operation, such as the delete\_from statement.</span></span> <span data-ttu-id="fce03-709">xRecord.delete メソッドなどの行ベースの操作でそれを使用する場合、プロパティは重視されず、削除アクションは引き続き呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="fce03-709">If you use it on a row-based operation, such as the xRecord.delete method, the property will not be respected, and the delete action will still be called.</span></span>

## <a name="method-skipdeletemethod"></a><span data-ttu-id="fce03-710">メソッド skipDeleteMethod</span><span class="sxs-lookup"><span data-stu-id="fce03-710">Method skipDeleteMethod</span></span>

<span data-ttu-id="fce03-711">オーバーロードされたメソッドを破棄するかどうかを示すプロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-711">Gets and sets the property that indicates whether to discard overloaded methods.</span></span>

```xpp
public boolean skipDeleteMethod([boolean newValue])
```

### <a name="parameters---skipdeletemethod"></a><span data-ttu-id="fce03-712">パラメーター - skipDeleteMethod</span><span class="sxs-lookup"><span data-stu-id="fce03-712">Parameters - skipDeleteMethod</span></span>

<span data-ttu-id="fce03-713">newValue</span><span class="sxs-lookup"><span data-stu-id="fce03-713">newValue</span></span>  
<span data-ttu-id="fce03-714">オーバーロードされたメソッドを破棄するかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="fce03-714">A Boolean value that indicates whether to discard overloaded methods; optional.</span></span>

### <a name="return-value---skipdeletemethod"></a><span data-ttu-id="fce03-715">戻り値 - skipDeleteMethod</span><span class="sxs-lookup"><span data-stu-id="fce03-715">Return Value - skipDeleteMethod</span></span>

<span data-ttu-id="fce03-716">オーバーロードされたメソッドを破棄する必要がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fce03-716">true if overloaded methods should be discarded; otherwise, false.</span></span>

## <a name="method-skipevents"></a><span data-ttu-id="fce03-717">メソッド skipEvents</span><span class="sxs-lookup"><span data-stu-id="fce03-717">Method skipEvents</span></span>

<span data-ttu-id="fce03-718">xRecord オブジェクトの有効期間の Application.event\* メソッドの呼び出しをオフにするオプションを提供します。</span><span class="sxs-lookup"><span data-stu-id="fce03-718">Provides an option to turn off calling the Application.event\* methods for the lifetime of an xRecord object.</span></span>

```xpp
public boolean skipEvents([boolean newValue])
```

### <a name="parameters---skipevents"></a><span data-ttu-id="fce03-719">パラメーター - skipEvents</span><span class="sxs-lookup"><span data-stu-id="fce03-719">Parameters - skipEvents</span></span>

<span data-ttu-id="fce03-720">newValue</span><span class="sxs-lookup"><span data-stu-id="fce03-720">newValue</span></span>  
<span data-ttu-id="fce03-721">イベントをスキップするかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="fce03-721">A Boolean value that indicates whether to skip events; optional.</span></span>

### <a name="return-value---skipevents"></a><span data-ttu-id="fce03-722">戻り値 - skipEvents</span><span class="sxs-lookup"><span data-stu-id="fce03-722">Return Value - skipEvents</span></span>

<span data-ttu-id="fce03-723">イベントがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fce03-723">true if events are skipped; otherwise, false.</span></span>

### <a name="remarks---skipevents"></a><span data-ttu-id="fce03-724">備考 - skipEvents</span><span class="sxs-lookup"><span data-stu-id="fce03-724">Remarks - skipEvents</span></span>

<span data-ttu-id="fce03-725">このメソッドは、xRecord.skipDatabaseLog メソッドに似ています。</span><span class="sxs-lookup"><span data-stu-id="fce03-725">This method resembles the xRecord.skipDatabaseLog method.</span></span> <span data-ttu-id="fce03-726">skipEvents メソッドは、カーネル内で生成するのに意味のないイベントをスキップするためにも内部的に使用されます。これは xRecord.skipDatabaseLog メソッドの現在の動作と一致しています。</span><span class="sxs-lookup"><span data-stu-id="fce03-726">The skipEvents method is also used internally in the kernel to skip events that make no sense to generate; this is consistent with the current behavior of the xRecord.skipDatabaseLog method:</span></span>

-   <span data-ttu-id="fce03-727">Application.deleteCompany メソッド: 会社の削除操作の期間にイベント生成が無効になります。</span><span class="sxs-lookup"><span data-stu-id="fce03-727">The Application.deleteCompany method: Event generation is turned off for the duration of a company delete operation.</span></span> <span data-ttu-id="fce03-728">これは管理操作であり、この場合はイベントをサポートするためのパフォーマンス上の問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fce03-728">This is an admin operation, and it could cause performance issues to support events in this case.</span></span>
-   <span data-ttu-id="fce03-729">SqlDataDictionary.tableDelete メソッド: テーブル削除時にイベント生成がオフになります。</span><span class="sxs-lookup"><span data-stu-id="fce03-729">The SqlDataDictionary.tableDelete method: Event generation is turned off for the duration of a table delete.</span></span> <span data-ttu-id="fce03-730">これは管理操作であり、この場合はイベントをサポートするためのパフォーマンス上の問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fce03-730">This is an admin operation, and it could cause performance issues to support events in this case.</span></span>
-   <span data-ttu-id="fce03-731">カーネルで配列挿入機能を実装する RecordInsertList クラスは、開発者によって指定されたイベントを条件付きでスキップする新しいメソッドで、オプション引数 \_skipEvents = false を取得します。</span><span class="sxs-lookup"><span data-stu-id="fce03-731">The RecordInsertList class, which implements array insert capabilities in the kernel, takes an optional argument, \_skipEvents = false, in the new method that will conditionally skip events as specified by a developer.</span></span> <span data-ttu-id="fce03-732">イベントがスキップされない場合でも、カーネルは SQL を書き換えません。</span><span class="sxs-lookup"><span data-stu-id="fce03-732">Even if events are not skipped, this will not make the kernel rewrite the SQL.</span></span>
-   <span data-ttu-id="fce03-733">主キーの名前を変更するとき、名前の変更操作が終了するまで、イベントの生成が停止されます。</span><span class="sxs-lookup"><span data-stu-id="fce03-733">When a primary key is renamed, event generation is turned off for the duration of the rename operation.</span></span> <span data-ttu-id="fce03-734">これには、1 つのレコード内の主キーが含まれ、多くのレコードに外部キーを含まれることができます。</span><span class="sxs-lookup"><span data-stu-id="fce03-734">This includes a primary key in one record and can include a foreign key in many records.</span></span> <span data-ttu-id="fce03-735">リネーム操作後、eventRenameKey メソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="fce03-735">After the rename operation, the eventRenameKey method is called.</span></span>

## <a name="method-skippostload"></a><span data-ttu-id="fce03-736">メソッド skipPostLoad</span><span class="sxs-lookup"><span data-stu-id="fce03-736">Method skipPostLoad</span></span>

<span data-ttu-id="fce03-737">テーブルで xRecord.postLoad メソッドの実行をスキップするかどうかを示すプロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-737">Gets and sets the property that indicates whether to skip executing the xRecord.postLoad method on the table.</span></span>

```xpp
public boolean skipPostLoad([boolean newValue])
```

### <a name="parameters---skippostload"></a><span data-ttu-id="fce03-738">パラメーター - skipPostLoad</span><span class="sxs-lookup"><span data-stu-id="fce03-738">Parameters - skipPostLoad</span></span>

<span data-ttu-id="fce03-739">newValue</span><span class="sxs-lookup"><span data-stu-id="fce03-739">newValue</span></span>  
<span data-ttu-id="fce03-740">テーブルの postLoad メソッドの実行をスキップするかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="fce03-740">A Boolean value that indicates whether to skip executing the postLoad method on the table; optional.</span></span>

### <a name="return-value---skippostload"></a><span data-ttu-id="fce03-741">戻り値 - skipPostLoad</span><span class="sxs-lookup"><span data-stu-id="fce03-741">Return Value - skipPostLoad</span></span>

<span data-ttu-id="fce03-742">postLoad メソッドの実行をスキップする場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fce03-742">true to skip executing the postLoad method; otherwise, false.</span></span>

## <a name="method-skipttscheck"></a><span data-ttu-id="fce03-743">メソッド skipTTSCheck</span><span class="sxs-lookup"><span data-stu-id="fce03-743">Method skipTTSCheck</span></span>

<span data-ttu-id="fce03-744">更新用にレコードが選択されているかどうかを決定するため、チェックをスキップするかどうかを示すプロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-744">Gets and sets the property that indicates whether to skip the check to determine whether the record is selected for update.</span></span>

```xpp
public boolean skipTTSCheck([boolean newValue])
```

### <a name="parameters---skipttscheck"></a><span data-ttu-id="fce03-745">パラメーター - skipTTSCheck</span><span class="sxs-lookup"><span data-stu-id="fce03-745">Parameters - skipTTSCheck</span></span>

<span data-ttu-id="fce03-746">newValue</span><span class="sxs-lookup"><span data-stu-id="fce03-746">newValue</span></span>  
<span data-ttu-id="fce03-747">チェックをスキップするかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="fce03-747">A Boolean value that indicates whether to skip the check; optional.</span></span>

### <a name="return-value---skipttscheck"></a><span data-ttu-id="fce03-748">戻り値 - skipTTSCheck</span><span class="sxs-lookup"><span data-stu-id="fce03-748">Return Value - skipTTSCheck</span></span>

<span data-ttu-id="fce03-749">TTS チェックをスキップする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="fce03-749">true if the TTS check should be skipped; otherwise, false.</span></span>

## <a name="method-suppresswarnings"></a><span data-ttu-id="fce03-750">メソッド suppressWarnings</span><span class="sxs-lookup"><span data-stu-id="fce03-750">Method suppressWarnings</span></span>

<span data-ttu-id="fce03-751">このポインタの警告を非表示にするかどうかを示すプロパティを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-751">Gets and sets the property that indicates whether to suppress warnings for this pointer.</span></span>

```xpp
public boolean suppressWarnings([boolean newValue])
```

### <a name="parameters---suppresswarnings"></a><span data-ttu-id="fce03-752">パラメーター - suppressWarnings</span><span class="sxs-lookup"><span data-stu-id="fce03-752">Parameters - suppressWarnings</span></span>

<span data-ttu-id="fce03-753">newValue</span><span class="sxs-lookup"><span data-stu-id="fce03-753">newValue</span></span>  
<span data-ttu-id="fce03-754">このポインタの警告を非表示にするかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="fce03-754">A Boolean value that indicates whether to suppress warnings for this pointer; optional.</span></span>

### <a name="return-value---suppresswarnings"></a><span data-ttu-id="fce03-755">戻り値 - suppressWarnings</span><span class="sxs-lookup"><span data-stu-id="fce03-755">Return Value - suppressWarnings</span></span>

<span data-ttu-id="fce03-756">このポインターの警告を抑制する必要がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fce03-756">true if warnings for this pointer should be suppressed; otherwise, false.</span></span>

## <a name="method-tableaccessright"></a><span data-ttu-id="fce03-757">メソッド tableAccessRight</span><span class="sxs-lookup"><span data-stu-id="fce03-757">Method tableAccessRight</span></span>

<span data-ttu-id="fce03-758">テーブルのアクセス権を返します。</span><span class="sxs-lookup"><span data-stu-id="fce03-758">Returns the table access right.</span></span>

```xpp
public AccessRight tableAccessRight()
```

### <a name="return-value---tableaccessright"></a><span data-ttu-id="fce03-759">戻り値 - tableAccessRight</span><span class="sxs-lookup"><span data-stu-id="fce03-759">Return Value - tableAccessRight</span></span>

<span data-ttu-id="fce03-760">テーブル アクセス権の値。</span><span class="sxs-lookup"><span data-stu-id="fce03-760">The table access right value.</span></span>

## <a name="method-tablebufferaccessright"></a><span data-ttu-id="fce03-761">メソッド tableBufferAccessRight</span><span class="sxs-lookup"><span data-stu-id="fce03-761">Method tableBufferAccessRight</span></span>

<span data-ttu-id="fce03-762">現在のレコードのテーブル アクセス権を返します。</span><span class="sxs-lookup"><span data-stu-id="fce03-762">Returns the table access right for the current record.</span></span>

```xpp
public AccessRight tableBufferAccessRight()
```

### <a name="return-value---tablebufferaccessright"></a><span data-ttu-id="fce03-763">戻り値 - tableBufferAccessRight</span><span class="sxs-lookup"><span data-stu-id="fce03-763">Return Value - tableBufferAccessRight</span></span>

<span data-ttu-id="fce03-764">現在のレコードのテーブル アクセス権。</span><span class="sxs-lookup"><span data-stu-id="fce03-764">The table access right for the current record.</span></span>

## <a name="method-takeownershipoftempdbtable"></a><span data-ttu-id="fce03-765">メソッド takeOwnershipOfTempDBTable</span><span class="sxs-lookup"><span data-stu-id="fce03-765">Method takeOwnershipOfTempDBTable</span></span>

```xpp
public boolean takeOwnershipOfTempDBTable(boolean newValue)
```

### <a name="parameters---takeownershipoftempdbtable"></a><span data-ttu-id="fce03-766">パラメーター - takeOwnershipOfTempDBTable</span><span class="sxs-lookup"><span data-stu-id="fce03-766">Parameters - takeOwnershipOfTempDBTable</span></span>

<span data-ttu-id="fce03-767">newValue</span><span class="sxs-lookup"><span data-stu-id="fce03-767">newValue</span></span>  

### <a name="return-value---takeownershipoftempdbtable"></a><span data-ttu-id="fce03-768">戻り値 - takeOwnershipOfTempDBTable</span><span class="sxs-lookup"><span data-stu-id="fce03-768">Return Value - takeOwnershipOfTempDBTable</span></span>

## <a name="method-tooltipfield"></a><span data-ttu-id="fce03-769">メソッド toolTipField</span><span class="sxs-lookup"><span data-stu-id="fce03-769">Method toolTipField</span></span>

<span data-ttu-id="fce03-770">指定されたフィールドの HelpText 値を取得します。</span><span class="sxs-lookup"><span data-stu-id="fce03-770">Retrieves the HelpText value for the specified field.</span></span>

```xpp
public str toolTipField(FieldId fieldId)
```

### <a name="parameters---tooltipfield"></a><span data-ttu-id="fce03-771">パラメーター - toolTipField</span><span class="sxs-lookup"><span data-stu-id="fce03-771">Parameters - toolTipField</span></span>

<span data-ttu-id="fce03-772">fieldId</span><span class="sxs-lookup"><span data-stu-id="fce03-772">fieldId</span></span>  
<span data-ttu-id="fce03-773">HelpText の値を取得するフィールド。</span><span class="sxs-lookup"><span data-stu-id="fce03-773">The field for which to retrieve the HelpText value.</span></span>

### <a name="return-value---tooltipfield"></a><span data-ttu-id="fce03-774">戻り値 - toolTipField</span><span class="sxs-lookup"><span data-stu-id="fce03-774">Return Value - toolTipField</span></span>

<span data-ttu-id="fce03-775">指定されたフィールドの HelpText 値。</span><span class="sxs-lookup"><span data-stu-id="fce03-775">The HelpText value of the specified field.</span></span>

## <a name="method-tooltiprecord"></a><span data-ttu-id="fce03-776">メソッド toolTipRecord</span><span class="sxs-lookup"><span data-stu-id="fce03-776">Method toolTipRecord</span></span>

<span data-ttu-id="fce03-777">現在のレコードのツールヒント値を取得します。</span><span class="sxs-lookup"><span data-stu-id="fce03-777">Retrieves the ToolTip value for the current record.</span></span>

```xpp
public str toolTipRecord()
```

### <a name="return-value---tooltiprecord"></a><span data-ttu-id="fce03-778">戻り値 - toolTipRecord</span><span class="sxs-lookup"><span data-stu-id="fce03-778">Return Value - toolTipRecord</span></span>

<span data-ttu-id="fce03-779">現在のレコードのツールヒント値。</span><span class="sxs-lookup"><span data-stu-id="fce03-779">The ToolTip value for the current record.</span></span>

## <a name="method-usagecount"></a><span data-ttu-id="fce03-780">メソッド usageCount</span><span class="sxs-lookup"><span data-stu-id="fce03-780">Method usageCount</span></span>

<span data-ttu-id="fce03-781">オブジェクトが持つ参照 (参照カウンターの値) の現在の番号を取得します。</span><span class="sxs-lookup"><span data-stu-id="fce03-781">Retrieves the current number of references (the value of the reference counter) that the object has.</span></span>

```xpp
public int usageCount()
```

### <a name="return-value---usagecount"></a><span data-ttu-id="fce03-782">戻り値 - usageCount</span><span class="sxs-lookup"><span data-stu-id="fce03-782">Return Value - usageCount</span></span>

<span data-ttu-id="fce03-783">オブジェクトが持つ参照の現在の数。</span><span class="sxs-lookup"><span data-stu-id="fce03-783">The current number of references that the object has.</span></span>

### <a name="remarks---usagecount"></a><span data-ttu-id="fce03-784">備考 - usageCount</span><span class="sxs-lookup"><span data-stu-id="fce03-784">Remarks - usageCount</span></span>

<span data-ttu-id="fce03-785">このメソッドは上書きされます。</span><span class="sxs-lookup"><span data-stu-id="fce03-785">This method is overridden.</span></span> <span data-ttu-id="fce03-786">オブジェクトが作成されると、その参照カウンターが 1 になります。</span><span class="sxs-lookup"><span data-stu-id="fce03-786">When an object is created, its reference counter equals 1.</span></span> <span data-ttu-id="fce03-787">新しい参照が作成されると、その値が増加します。</span><span class="sxs-lookup"><span data-stu-id="fce03-787">When a new reference is created, its value increases.</span></span> <span data-ttu-id="fce03-788">スコープ外の参照は、値が減少します。</span><span class="sxs-lookup"><span data-stu-id="fce03-788">As a reference goes out of scope, its value decreases.</span></span>

## <a name="method-useexistingtempdbtable"></a><span data-ttu-id="fce03-789">メソッド useExistingTempDBTable</span><span class="sxs-lookup"><span data-stu-id="fce03-789">Method useExistingTempDBTable</span></span>

```xpp
public boolean useExistingTempDBTable(str physicalTempTableName)
```

### <a name="parameters---useexistingtempdbtable"></a><span data-ttu-id="fce03-790">パラメーター - useExistingTempDBTable</span><span class="sxs-lookup"><span data-stu-id="fce03-790">Parameters - useExistingTempDBTable</span></span>

<span data-ttu-id="fce03-791">physicalTempTableName</span><span class="sxs-lookup"><span data-stu-id="fce03-791">physicalTempTableName</span></span>  

### <a name="return-value---useexistingtempdbtable"></a><span data-ttu-id="fce03-792">戻り値 - useExistingTempDBTable</span><span class="sxs-lookup"><span data-stu-id="fce03-792">Return Value - useExistingTempDBTable</span></span>

## <a name="method-validatedelete"></a><span data-ttu-id="fce03-793">メソッド validateDelete</span><span class="sxs-lookup"><span data-stu-id="fce03-793">Method validateDelete</span></span>

<span data-ttu-id="fce03-794">現在のレコードが有効で、データベースから削除する準備ができているかどうかを調べます。</span><span class="sxs-lookup"><span data-stu-id="fce03-794">Determines whether the current record is valid and ready to be deleted from the database.</span></span>

```xpp
public boolean validateDelete()
```

### <a name="return-value---validatedelete"></a><span data-ttu-id="fce03-795">戻り値 - validateDelete</span><span class="sxs-lookup"><span data-stu-id="fce03-795">Return Value - validateDelete</span></span>

<span data-ttu-id="fce03-796">現在のレコードを削除することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fce03-796">true if the current record can be deleted; otherwise, false.</span></span>

## <a name="method-validatefield"></a><span data-ttu-id="fce03-797">メソッド validateField</span><span class="sxs-lookup"><span data-stu-id="fce03-797">Method validateField</span></span>

<span data-ttu-id="fce03-798">指定されたフィールドが有効かどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-798">Determines whether the specified field is valid.</span></span>

```xpp
public boolean validateField(FieldId fieldIdToCheck)
```

### <a name="parameters---validatefield"></a><span data-ttu-id="fce03-799">パラメーター - validateField</span><span class="sxs-lookup"><span data-stu-id="fce03-799">Parameters - validateField</span></span>

<span data-ttu-id="fce03-800">fieldIdToCheck</span><span class="sxs-lookup"><span data-stu-id="fce03-800">fieldIdToCheck</span></span>  
<span data-ttu-id="fce03-801">検証対象のフィールドのフィールド ID です。</span><span class="sxs-lookup"><span data-stu-id="fce03-801">The field ID of the field to validate.</span></span>

### <a name="return-value---validatefield"></a><span data-ttu-id="fce03-802">戻り値 - validateField</span><span class="sxs-lookup"><span data-stu-id="fce03-802">Return Value - validateField</span></span>

<span data-ttu-id="fce03-803">指定したフィールドが有効である場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="fce03-803">true if the specified field is valid; otherwise, false.</span></span>

## <a name="method-validatefieldvalue"></a><span data-ttu-id="fce03-804">メソッド validateFieldValue</span><span class="sxs-lookup"><span data-stu-id="fce03-804">Method validateFieldValue</span></span>

```xpp
public boolean validateFieldValue(FieldName fieldName, [int arrayIndex])
```

### <a name="parameters---validatefieldvalue"></a><span data-ttu-id="fce03-805">パラメーター - validateFieldValue</span><span class="sxs-lookup"><span data-stu-id="fce03-805">Parameters - validateFieldValue</span></span>

<span data-ttu-id="fce03-806">fieldName</span><span class="sxs-lookup"><span data-stu-id="fce03-806">fieldName</span></span>  

<!-- -->

<span data-ttu-id="fce03-807">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="fce03-807">arrayIndex</span></span>  

### <a name="return-value---validatefieldvalue"></a><span data-ttu-id="fce03-808">戻り値 - validateFieldValue</span><span class="sxs-lookup"><span data-stu-id="fce03-808">Return Value - validateFieldValue</span></span>

## <a name="method-validaterelations"></a><span data-ttu-id="fce03-809">メソッド validateRelations</span><span class="sxs-lookup"><span data-stu-id="fce03-809">Method validateRelations</span></span>

```xpp
private container validateRelations([boolean onlyValidateCompositeRelations], [boolean onlyValidateModifiedRelations])
```

### <a name="parameters---validaterelations"></a><span data-ttu-id="fce03-810">パラメーター - validateRelations</span><span class="sxs-lookup"><span data-stu-id="fce03-810">Parameters - validateRelations</span></span>

<span data-ttu-id="fce03-811">onlyValidateCompositeRelations</span><span class="sxs-lookup"><span data-stu-id="fce03-811">onlyValidateCompositeRelations</span></span>  

<!-- -->

<span data-ttu-id="fce03-812">onlyValidateModifiedRelations</span><span class="sxs-lookup"><span data-stu-id="fce03-812">onlyValidateModifiedRelations</span></span>  

### <a name="return-value---validaterelations"></a><span data-ttu-id="fce03-813">戻り値 - validateRelations</span><span class="sxs-lookup"><span data-stu-id="fce03-813">Return Value - validateRelations</span></span>

## <a name="method-validatewrite"></a><span data-ttu-id="fce03-814">メソッド validateWrite</span><span class="sxs-lookup"><span data-stu-id="fce03-814">Method validateWrite</span></span>

<span data-ttu-id="fce03-815">現在のレコードが有効で、書き込み可能な状態かどうかを判別します。</span><span class="sxs-lookup"><span data-stu-id="fce03-815">Determines whether the current record is valid and ready to be written.</span></span>

```xpp
public boolean validateWrite()
```

### <a name="return-value---validatewrite"></a><span data-ttu-id="fce03-816">戻り値 - validateWrite</span><span class="sxs-lookup"><span data-stu-id="fce03-816">Return Value - validateWrite</span></span>

<span data-ttu-id="fce03-817">現在のレコードを記述することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fce03-817">true if the current record can be written; otherwise, false.</span></span>

## <a name="method-validtimestateupdatemode"></a><span data-ttu-id="fce03-818">メソッド validTimeStateUpdateMode</span><span class="sxs-lookup"><span data-stu-id="fce03-818">Method validTimeStateUpdateMode</span></span>

<span data-ttu-id="fce03-819">カーソルで有効な時間状態更新モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-819">Sets a valid time state update mode on the cursor.</span></span>

```xpp
public ValidTimeStateUpdate validTimeStateUpdateMode(ValidTimeStateUpdate validTimeStateUpdateMode)
```

### <a name="parameters---validtimestateupdatemode"></a><span data-ttu-id="fce03-820">パラメーター - validTimeStateUpdateMode</span><span class="sxs-lookup"><span data-stu-id="fce03-820">Parameters - validTimeStateUpdateMode</span></span>

<span data-ttu-id="fce03-821">validTimeStateUpdateMode</span><span class="sxs-lookup"><span data-stu-id="fce03-821">validTimeStateUpdateMode</span></span>  

### <a name="return-value---validtimestateupdatemode"></a><span data-ttu-id="fce03-822">戻り値 - validTimeStateUpdateMode</span><span class="sxs-lookup"><span data-stu-id="fce03-822">Return Value - validTimeStateUpdateMode</span></span>

<span data-ttu-id="fce03-823">有効時間状態の更新モードの古い値。</span><span class="sxs-lookup"><span data-stu-id="fce03-823">The old value of the valid time state update mode.</span></span>

## <a name="method-wascached"></a><span data-ttu-id="fce03-824">メソッド wasCached</span><span class="sxs-lookup"><span data-stu-id="fce03-824">Method wasCached</span></span>

<span data-ttu-id="fce03-825">データの取得元となった場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-825">Specifies the location from which the data was retrieved.</span></span>

```xpp
public CachedHow wasCached()
```

### <a name="return-value---wascached"></a><span data-ttu-id="fce03-826">戻り値 - wasCached</span><span class="sxs-lookup"><span data-stu-id="fce03-826">Return Value - wasCached</span></span>

<span data-ttu-id="fce03-827">データが取得された場所を示す CachedHow 列挙値。</span><span class="sxs-lookup"><span data-stu-id="fce03-827">A CachedHow enumeration value that indicates the location from which the data was retrieved.</span></span>

## <a name="method-xml"></a><span data-ttu-id="fce03-828">メソッド xml</span><span class="sxs-lookup"><span data-stu-id="fce03-828">Method xml</span></span>

<span data-ttu-id="fce03-829">現在のオブジェクトを表す XML 文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="fce03-829">Retrieves an XML string that represents the current object.</span></span>

```xpp
public str xml([int indent])
```

### <a name="parameters---xml"></a><span data-ttu-id="fce03-830">パラメーター - xml</span><span class="sxs-lookup"><span data-stu-id="fce03-830">Parameters - xml</span></span>

<span data-ttu-id="fce03-831">インデント</span><span class="sxs-lookup"><span data-stu-id="fce03-831">indent</span></span>  
<span data-ttu-id="fce03-832">XML 文字列のインデントに使用するスペースの数を示す整数。</span><span class="sxs-lookup"><span data-stu-id="fce03-832">An integer that indicates the number of spaces to use for indentation in the XML string.</span></span>

### <a name="return-value---xml"></a><span data-ttu-id="fce03-833">戻り値 - xml</span><span class="sxs-lookup"><span data-stu-id="fce03-833">Return Value - xml</span></span>

<span data-ttu-id="fce03-834">現在のオブジェクトを表す XML 文字列です。</span><span class="sxs-lookup"><span data-stu-id="fce03-834">An XML string that represents the current object.</span></span>

### <a name="remarks---xml"></a><span data-ttu-id="fce03-835">備考 - xml</span><span class="sxs-lookup"><span data-stu-id="fce03-835">Remarks - xml</span></span>

<span data-ttu-id="fce03-836">このメソッドをオーバーライドして、その型に対して意味のある値を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="fce03-836">This method can be overridden to return values that are meaningful for that type.</span></span>

## <a name="method-dodelete"></a><span data-ttu-id="fce03-837">メソッド doDelete</span><span class="sxs-lookup"><span data-stu-id="fce03-837">Method doDelete</span></span>

<span data-ttu-id="fce03-838">現在のレコードをテーブルから削除し、テーブルの delete メソッドの追加ロジックをバイパスします。</span><span class="sxs-lookup"><span data-stu-id="fce03-838">Deletes the current record from the table and bypasses any additional logic in the delete method of the table.</span></span>

```xpp
public void doDelete()
```

## <a name="method-update"></a><span data-ttu-id="fce03-839">メソッド update</span><span class="sxs-lookup"><span data-stu-id="fce03-839">Method update</span></span>

<span data-ttu-id="fce03-840">現在のレコードを更新します。</span><span class="sxs-lookup"><span data-stu-id="fce03-840">Updates the current record.</span></span>

```xpp
public void update()
```

## <a name="method-merge"></a><span data-ttu-id="fce03-841">メソッド merge</span><span class="sxs-lookup"><span data-stu-id="fce03-841">Method merge</span></span>

<span data-ttu-id="fce03-842">現在のテーブルを指定されたテーブルとマージします。</span><span class="sxs-lookup"><span data-stu-id="fce03-842">Merges the current table with the specified table.</span></span>

```xpp
public void merge(Common mergeInto)
```

### <a name="parameters---merge"></a><span data-ttu-id="fce03-843">パラメーター - merge</span><span class="sxs-lookup"><span data-stu-id="fce03-843">Parameters - merge</span></span>

<span data-ttu-id="fce03-844">mergeInto</span><span class="sxs-lookup"><span data-stu-id="fce03-844">mergeInto</span></span>  
<span data-ttu-id="fce03-845">マージするテーブル。</span><span class="sxs-lookup"><span data-stu-id="fce03-845">The table to merge with.</span></span>

## <a name="method-clear"></a><span data-ttu-id="fce03-846">メソッド clear</span><span class="sxs-lookup"><span data-stu-id="fce03-846">Method clear</span></span>

<span data-ttu-id="fce03-847">テーブル バッファーからすべての行を削除します。</span><span class="sxs-lookup"><span data-stu-id="fce03-847">Removes all rows from the table buffer.</span></span>

```xpp
public void clear()
```

## <a name="method-setxdscontext"></a><span data-ttu-id="fce03-848">メソッド setXDSContext</span><span class="sxs-lookup"><span data-stu-id="fce03-848">Method setXDSContext</span></span>

<span data-ttu-id="fce03-849">新しい XDS コンテキストを設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-849">Sets new XDS context.</span></span>

```xpp
public void setXDSContext([str contextString])
```

### <a name="parameters---setxdscontext"></a><span data-ttu-id="fce03-850">パラメーター - setXDSContext</span><span class="sxs-lookup"><span data-stu-id="fce03-850">Parameters - setXDSContext</span></span>

<span data-ttu-id="fce03-851">contextString</span><span class="sxs-lookup"><span data-stu-id="fce03-851">contextString</span></span>  

## <a name="method-renameprimarykey"></a><span data-ttu-id="fce03-852">メソッド renamePrimaryKey</span><span class="sxs-lookup"><span data-stu-id="fce03-852">Method renamePrimaryKey</span></span>

<span data-ttu-id="fce03-853">この表の対応する主キーの値の変更に従って、他のテーブルの外部キーの名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="fce03-853">Renames the foreign keys in other tables according to the change of the corresponding primary key value in this table.</span></span>

```xpp
public void renamePrimaryKey()
```

## <a name="method-dispose"></a><span data-ttu-id="fce03-854">メソッド dispose</span><span class="sxs-lookup"><span data-stu-id="fce03-854">Method dispose</span></span>

<span data-ttu-id="fce03-855">XRecord オブジェクトによって使用されているリソースを解放します。</span><span class="sxs-lookup"><span data-stu-id="fce03-855">Releases resources that are used by the xRecord object.</span></span>

```xpp
public void dispose()
```

## <a name="method-setconnection"></a><span data-ttu-id="fce03-856">メソッド setConnection</span><span class="sxs-lookup"><span data-stu-id="fce03-856">Method setConnection</span></span>

<span data-ttu-id="fce03-857">この表のユーザー接続を設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-857">Sets the user connection for this table.</span></span>

```xpp
public void setConnection(Connection connection)
```

### <a name="parameters---setconnection"></a><span data-ttu-id="fce03-858">パラメーター - setConnection</span><span class="sxs-lookup"><span data-stu-id="fce03-858">Parameters - setConnection</span></span>

<span data-ttu-id="fce03-859">connection</span><span class="sxs-lookup"><span data-stu-id="fce03-859">connection</span></span>  

## <a name="method-delete"></a><span data-ttu-id="fce03-860">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="fce03-860">Method delete</span></span>

<span data-ttu-id="fce03-861">テーブルから現在のレコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="fce03-861">Deletes the current record from the table.</span></span>

```xpp
public void delete()
```

## <a name="method-defaultfield"></a><span data-ttu-id="fce03-862">メソッド defaultField</span><span class="sxs-lookup"><span data-stu-id="fce03-862">Method defaultField</span></span>

<span data-ttu-id="fce03-863">テーブルのフィールドの既定値を設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-863">Populates default values in a field in the table.</span></span>

```xpp
public void defaultField(FieldId fieldId)
```

### <a name="parameters---defaultfield"></a><span data-ttu-id="fce03-864">パラメーター - defaultField</span><span class="sxs-lookup"><span data-stu-id="fce03-864">Parameters - defaultField</span></span>

<span data-ttu-id="fce03-865">fieldId</span><span class="sxs-lookup"><span data-stu-id="fce03-865">fieldId</span></span>  

## <a name="method-dbopintransaction"></a><span data-ttu-id="fce03-866">メソッド dbOpInTransaction</span><span class="sxs-lookup"><span data-stu-id="fce03-866">Method dbOpInTransaction</span></span>

<span data-ttu-id="fce03-867">失敗した場合にデータベース操作が正しく閉じられていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fce03-867">Makes sure that database operations are correctly closed if they fail.</span></span>

```xpp
private void dbOpInTransaction([boolean isWriteOperation])
```

### <a name="parameters---dbopintransaction"></a><span data-ttu-id="fce03-868">パラメーター - dbOpInTransaction</span><span class="sxs-lookup"><span data-stu-id="fce03-868">Parameters - dbOpInTransaction</span></span>

<span data-ttu-id="fce03-869">isWriteOperation</span><span class="sxs-lookup"><span data-stu-id="fce03-869">isWriteOperation</span></span>  
<span data-ttu-id="fce03-870">操作が書き込み操作かどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="fce03-870">A Boolean value that indicates whether the operation is a write operation; optional.</span></span>

## <a name="method-write"></a><span data-ttu-id="fce03-871">メソッド write</span><span class="sxs-lookup"><span data-stu-id="fce03-871">Method write</span></span>

<span data-ttu-id="fce03-872">レコードが存在する場合は更新します。存在しない場合はレコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="fce03-872">Updates a record if it exists; otherwise, inserts a record.</span></span>

```xpp
public void write()
```

## <a name="method-preremoting"></a><span data-ttu-id="fce03-873">メソッド preRemoting</span><span class="sxs-lookup"><span data-stu-id="fce03-873">Method preRemoting</span></span>

<span data-ttu-id="fce03-874">他のレベルに状態をパックしているテーブルに対してレベル間の呼び出しが実行される前に実行されます。</span><span class="sxs-lookup"><span data-stu-id="fce03-874">Is executed before a cross-tier call is about to be executed for the table that would pack its state to the other tier.</span></span>

```xpp
public void preRemoting()
```

## <a name="method-modifiedfieldvalue"></a><span data-ttu-id="fce03-875">メソッド modifiedFieldValue</span><span class="sxs-lookup"><span data-stu-id="fce03-875">Method modifiedFieldValue</span></span>

<span data-ttu-id="fce03-876">指定したフィールドを元の値に変更します。</span><span class="sxs-lookup"><span data-stu-id="fce03-876">Modifies the specified field to the original value.</span></span>

```xpp
public void modifiedFieldValue(FieldName fieldName, [int arrayIndex])
```

### <a name="parameters---modifiedfieldvalue"></a><span data-ttu-id="fce03-877">パラメーター - modifiedFieldValue</span><span class="sxs-lookup"><span data-stu-id="fce03-877">Parameters - modifiedFieldValue</span></span>

<span data-ttu-id="fce03-878">fieldName</span><span class="sxs-lookup"><span data-stu-id="fce03-878">fieldName</span></span>  
<span data-ttu-id="fce03-879">フィールドの配列インデックス (省略可能)。</span><span class="sxs-lookup"><span data-stu-id="fce03-879">The array index of the field; optional.</span></span>

<!-- -->

<span data-ttu-id="fce03-880">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="fce03-880">arrayIndex</span></span>  
<span data-ttu-id="fce03-881">フィールドの配列インデックス (省略可能)。</span><span class="sxs-lookup"><span data-stu-id="fce03-881">The array index of the field; optional.</span></span>

## <a name="method-defaultrow"></a><span data-ttu-id="fce03-882">メソッド defaultRow</span><span class="sxs-lookup"><span data-stu-id="fce03-882">Method defaultRow</span></span>

<span data-ttu-id="fce03-883">非対話型の場合、テーブルのフィールドの既定値を設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-883">Populates default values in fields in the table in the non-interactive case.</span></span>

```xpp
public void defaultRow()
```

## <a name="method-reread"></a><span data-ttu-id="fce03-884">メソッド reread</span><span class="sxs-lookup"><span data-stu-id="fce03-884">Method reread</span></span>

<span data-ttu-id="fce03-885">テーブルからレコードを再読み取りします。</span><span class="sxs-lookup"><span data-stu-id="fce03-885">Rereads the record from the table.</span></span>

```xpp
public void reread()
```

## <a name="method-modifiedfield"></a><span data-ttu-id="fce03-886">メソッド modifiedField</span><span class="sxs-lookup"><span data-stu-id="fce03-886">Method modifiedField</span></span>

<span data-ttu-id="fce03-887">指定したフィールドを元通りに変更します。</span><span class="sxs-lookup"><span data-stu-id="fce03-887">Modifies the specified field to the original.</span></span>

```xpp
public void modifiedField(FieldId fieldId)
```

### <a name="parameters---modifiedfield"></a><span data-ttu-id="fce03-888">パラメーター - modifiedField</span><span class="sxs-lookup"><span data-stu-id="fce03-888">Parameters - modifiedField</span></span>

<span data-ttu-id="fce03-889">fieldId</span><span class="sxs-lookup"><span data-stu-id="fce03-889">fieldId</span></span>  
<span data-ttu-id="fce03-890">変更対象のフィールド ID。</span><span class="sxs-lookup"><span data-stu-id="fce03-890">The field ID to modify.</span></span>

## <a name="method-ttsabort"></a><span data-ttu-id="fce03-891">メソッド ttsabort</span><span class="sxs-lookup"><span data-stu-id="fce03-891">Method ttsabort</span></span>

<span data-ttu-id="fce03-892">ttsbegin メソッドの呼び出しによって開始されたトランザクションの廃棄。</span><span class="sxs-lookup"><span data-stu-id="fce03-892">Aborts a transaction that was started by a call to the ttsbegin method.</span></span>

```xpp
public void ttsabort()
```

## <a name="method-insert"></a><span data-ttu-id="fce03-893">メソッド insert</span><span class="sxs-lookup"><span data-stu-id="fce03-893">Method insert</span></span>

<span data-ttu-id="fce03-894">テーブルにレコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="fce03-894">Inserts the record into the table.</span></span>

```xpp
public void insert()
```

## <a name="method-doclear"></a><span data-ttu-id="fce03-895">メソッド doClear</span><span class="sxs-lookup"><span data-stu-id="fce03-895">Method doClear</span></span>

<span data-ttu-id="fce03-896">現在の行をテーブル バッファーから削除し、テーブルの clear メソッドの追加ロジックをバイパスします。</span><span class="sxs-lookup"><span data-stu-id="fce03-896">Removes all rows from the table buffer and bypasses any additional logic in the clear method of the table.</span></span>

```xpp
public void doClear()
```

## <a name="method-initvalue"></a><span data-ttu-id="fce03-897">メソッド initValue</span><span class="sxs-lookup"><span data-stu-id="fce03-897">Method initValue</span></span>

<span data-ttu-id="fce03-898">フィールドを既定値に初期化します。</span><span class="sxs-lookup"><span data-stu-id="fce03-898">Initializes a field to the default value.</span></span>

```xpp
public void initValue()
```

## <a name="method-doupdate"></a><span data-ttu-id="fce03-899">メソッド doUpdate</span><span class="sxs-lookup"><span data-stu-id="fce03-899">Method doUpdate</span></span>

<span data-ttu-id="fce03-900">現在のレコードを更新し、テーブルの更新メソッドにある追加ロジックをバイパスします。</span><span class="sxs-lookup"><span data-stu-id="fce03-900">Updates the current record and bypasses any additional logic in the update method of the table.</span></span>

```xpp
public void doUpdate()
```

## <a name="method-ttsbegin"></a><span data-ttu-id="fce03-901">メソッド ttsbegin</span><span class="sxs-lookup"><span data-stu-id="fce03-901">Method ttsbegin</span></span>

<span data-ttu-id="fce03-902">ttscommit メソッドによりコミット、または ttsabort メソッドによって中止できるトランザクションを開始します。</span><span class="sxs-lookup"><span data-stu-id="fce03-902">Starts a transaction that can be either committed by the ttscommit method or aborted by the ttsabort method.</span></span>

```xpp
public void ttsbegin()
```

## <a name="method-setcrosspartition"></a><span data-ttu-id="fce03-903">メソッド setCrossPartition</span><span class="sxs-lookup"><span data-stu-id="fce03-903">Method setCrossPartition</span></span>

<span data-ttu-id="fce03-904">テーブルのパーティション間分割を設定またはリセットします。</span><span class="sxs-lookup"><span data-stu-id="fce03-904">Sets or resets cross-partitioning for the table.</span></span>

```xpp
public void setCrossPartition(boolean newValue)
```

### <a name="parameters---setcrosspartition"></a><span data-ttu-id="fce03-905">パラメーター - setCrossPartition</span><span class="sxs-lookup"><span data-stu-id="fce03-905">Parameters - setCrossPartition</span></span>

<span data-ttu-id="fce03-906">newValue</span><span class="sxs-lookup"><span data-stu-id="fce03-906">newValue</span></span>  
<span data-ttu-id="fce03-907">クロス パーティションをセットまたはリセットする新しいブール値。</span><span class="sxs-lookup"><span data-stu-id="fce03-907">A new Boolean value to set or reset cross-partitioning.</span></span>

## <a name="method-settmpdata"></a><span data-ttu-id="fce03-908">メソッド setTmpData</span><span class="sxs-lookup"><span data-stu-id="fce03-908">Method setTmpData</span></span>

<span data-ttu-id="fce03-909">一時的なテーブルの内容を指定されたデータに設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-909">Sets the contents of the temporary table to the specified data.</span></span>

```xpp
public void setTmpData(Common cursor)
```

### <a name="parameters---settmpdata"></a><span data-ttu-id="fce03-910">パラメーター - setTmpData</span><span class="sxs-lookup"><span data-stu-id="fce03-910">Parameters - setTmpData</span></span>

<span data-ttu-id="fce03-911">cursor</span><span class="sxs-lookup"><span data-stu-id="fce03-911">cursor</span></span>  
<span data-ttu-id="fce03-912">一時テーブルの新しいデータ。</span><span class="sxs-lookup"><span data-stu-id="fce03-912">The new data for the temporary table.</span></span>

## <a name="method-ttscommit"></a><span data-ttu-id="fce03-913">メソッド ttscommit</span><span class="sxs-lookup"><span data-stu-id="fce03-913">Method ttscommit</span></span>

<span data-ttu-id="fce03-914">ttsbegin メソッドの呼び出しによって開始されたトランザクションをコミットします。</span><span class="sxs-lookup"><span data-stu-id="fce03-914">Commits a transaction that was started by a call to the ttsbegin method.</span></span>

```xpp
public void ttscommit()
```

## <a name="method-setfieldvalue"></a><span data-ttu-id="fce03-915">メソッド setFieldValue</span><span class="sxs-lookup"><span data-stu-id="fce03-915">Method setFieldValue</span></span>

<span data-ttu-id="fce03-916">レコード バッファーのフィールド値を設定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-916">Sets the field value in the record buffer.</span></span>

```xpp
public void setFieldValue(str fieldName, AnyType value, [int arrayIndex])
```

### <a name="parameters---setfieldvalue"></a><span data-ttu-id="fce03-917">パラメーター - setFieldValue</span><span class="sxs-lookup"><span data-stu-id="fce03-917">Parameters - setFieldValue</span></span>

<span data-ttu-id="fce03-918">fieldName</span><span class="sxs-lookup"><span data-stu-id="fce03-918">fieldName</span></span>  
<span data-ttu-id="fce03-919">フィールドの配列インデックス (省略可能)。</span><span class="sxs-lookup"><span data-stu-id="fce03-919">The array index of the field; optional.</span></span>

<!-- -->

<span data-ttu-id="fce03-920">値</span><span class="sxs-lookup"><span data-stu-id="fce03-920">value</span></span>  
<span data-ttu-id="fce03-921">フィールドの配列インデックス (省略可能)。</span><span class="sxs-lookup"><span data-stu-id="fce03-921">The array index of the field; optional.</span></span>

<!-- -->

<span data-ttu-id="fce03-922">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="fce03-922">arrayIndex</span></span>  
<span data-ttu-id="fce03-923">フィールドの配列インデックス (省略可能)。</span><span class="sxs-lookup"><span data-stu-id="fce03-923">The array index of the field; optional.</span></span>

### <a name="remarks---setfieldvalue"></a><span data-ttu-id="fce03-924">備考 - setFieldValue</span><span class="sxs-lookup"><span data-stu-id="fce03-924">Remarks - setFieldValue</span></span>

<span data-ttu-id="fce03-925">arrayIndex パラメーターは、配列フィールドにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="fce03-925">The arrayIndex parameter applies only to array fields.</span></span> <span data-ttu-id="fce03-926">配列でないフィールドには、このパラメーターを省略するか、または 0 (ゼロ) を指定します。</span><span class="sxs-lookup"><span data-stu-id="fce03-926">Either omit this parameter or specify0 (zero) for fields that are not arrays.</span></span> <span data-ttu-id="fce03-927">このメソッドは、指定されたフィールドが不明な場合は ArgumentOutOfRange 例外をスローし、値パラメーターが指定されたフィールドと互換性がない場合は TypeMismatch 例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="fce03-927">This method throws an ArgumentOutOfRange exception if the specified field is unknown or a TypeMismatch exception if the value parameter is incompatible with the specified field..</span></span>

## <a name="method-doinsert"></a><span data-ttu-id="fce03-928">メソッド doInsert</span><span class="sxs-lookup"><span data-stu-id="fce03-928">Method doInsert</span></span>

<span data-ttu-id="fce03-929">テーブルにレコードを挿入し、テーブルの挿入メソッドで追加のロジックをバイパスします。</span><span class="sxs-lookup"><span data-stu-id="fce03-929">Inserts the record into the table and bypasses any additional logic in the insert method of the table.</span></span>

```xpp
public void doInsert()
```

## <a name="method-setsqltracing"></a><span data-ttu-id="fce03-930">メソッド setSQLTracing</span><span class="sxs-lookup"><span data-stu-id="fce03-930">Method setSQLTracing</span></span>

<span data-ttu-id="fce03-931">SQL トレース モードを有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="fce03-931">Enables or disables SQL tracing mode.</span></span>

```xpp
public void setSQLTracing([boolean tracingmode])
```

### <a name="parameters---setsqltracing"></a><span data-ttu-id="fce03-932">パラメーター - setSQLTracing</span><span class="sxs-lookup"><span data-stu-id="fce03-932">Parameters - setSQLTracing</span></span>

<span data-ttu-id="fce03-933">tracingmode</span><span class="sxs-lookup"><span data-stu-id="fce03-933">tracingmode</span></span>  

## <a name="method-postload"></a><span data-ttu-id="fce03-934">メソッド postLoad</span><span class="sxs-lookup"><span data-stu-id="fce03-934">Method postLoad</span></span>

<span data-ttu-id="fce03-935">レコードが読み取られた後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="fce03-935">Is executed after a record is read.</span></span>

```xpp
public void postLoad()
```

