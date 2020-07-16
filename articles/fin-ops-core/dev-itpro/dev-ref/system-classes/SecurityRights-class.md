---
title: SecurityRights クラス
description: このトピックでは、SecurityRights クラスについて説明します。
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
ms.openlocfilehash: 9fe35b199959089ca2b9e8e9e7acfa846c77db6c
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502811"
---
# <a name="class-securityrights"></a><span data-ttu-id="60940-103">クラス SecurityRights</span><span class="sxs-lookup"><span data-stu-id="60940-103">Class SecurityRights</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class SecurityRights extends Object
```

<span data-ttu-id="60940-104">SecurityRights クラスには、セキュリティの権利とアクセス許可の管理に関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="60940-104">The SecurityRights class holds the information about the security rights and permissions management.</span></span>

## <a name="remarks"></a><span data-ttu-id="60940-105">備考</span><span class="sxs-lookup"><span data-stu-id="60940-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="60940-106">例</span><span class="sxs-lookup"><span data-stu-id="60940-106">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="60940-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="60940-107">Methods</span></span>

| <span data-ttu-id="60940-108">方法</span><span class="sxs-lookup"><span data-stu-id="60940-108">Method</span></span>                                                                                                                                                                                 | <span data-ttu-id="60940-109">説明</span><span class="sxs-lookup"><span data-stu-id="60940-109">Description</span></span>                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="60940-110">public boolean hasDataServiceAccess(SecurableName name, StatementType operation, \[SecurableChildName fieldName\])</span><span class="sxs-lookup"><span data-stu-id="60940-110">public boolean hasDataServiceAccess(SecurableName name, StatementType operation, \[SecurableChildName fieldName\])</span></span>                                                                     |                                                                        |
| <span data-ttu-id="60940-111">public boolean hasDataServiceMethodAccess(SecurableName name, StatementType operation, SecurableChildName methodName)</span><span class="sxs-lookup"><span data-stu-id="60940-111">public boolean hasDataServiceMethodAccess(SecurableName name, StatementType operation, SecurableChildName methodName)</span></span>                                                                  |                                                                        |
| <span data-ttu-id="60940-112">public AccessRight dataManagementAccessRight(SecurableName dataEntityName, \[SecurableChildName fieldName\])</span><span class="sxs-lookup"><span data-stu-id="60940-112">public AccessRight dataManagementAccessRight(SecurableName dataEntityName, \[SecurableChildName fieldName\])</span></span>                                                                           |                                                                        |
| <span data-ttu-id="60940-113">public str listDataServiceAccess(SecurableName name, \[SecurableChildName context\])</span><span class="sxs-lookup"><span data-stu-id="60940-113">public str listDataServiceAccess(SecurableName name, \[SecurableChildName context\])</span></span>                                                                                                   |                                                                        |
| <span data-ttu-id="60940-114">public AccessRight fieldAccessRight(TableName tableName, FieldName fieldName, \[Common record\], \[DataAreaId dataArea\], \[boolean includeDerived\], \[AutoAuthzMode autoAuthzMode\])</span><span class="sxs-lookup"><span data-stu-id="60940-114">public AccessRight fieldAccessRight(TableName tableName, FieldName fieldName, \[Common record\], \[DataAreaId dataArea\], \[boolean includeDerived\], \[AutoAuthzMode autoAuthzMode\])</span></span> | <span data-ttu-id="60940-115">テーブルのフィールドのアクセス権を取得します。</span><span class="sxs-lookup"><span data-stu-id="60940-115">Retrieves the access rights for the field of the table.</span></span>                |
| <span data-ttu-id="60940-116">public AccessRight formControlAccessRight(FormName form, UtilElementName control, \[Common record\], \[DataAreaId dataArea\])</span><span class="sxs-lookup"><span data-stu-id="60940-116">public AccessRight formControlAccessRight(FormName form, UtilElementName control, \[Common record\], \[DataAreaId dataArea\])</span></span>                                                          | <span data-ttu-id="60940-117">フォーム コントロールのアクセス権を取得します。</span><span class="sxs-lookup"><span data-stu-id="60940-117">Retrieves the access rights for the form control.</span></span>                      |
| <span data-ttu-id="60940-118">public container getSelectableCompanies()</span><span class="sxs-lookup"><span data-stu-id="60940-118">public container getSelectableCompanies()</span></span>                                                                                                                                              |                                                                        |
| <span data-ttu-id="60940-119">public boolean hasMenuAccess(MenuName menu, \[boolean isWebMenu\])</span><span class="sxs-lookup"><span data-stu-id="60940-119">public boolean hasMenuAccess(MenuName menu, \[boolean isWebMenu\])</span></span>                                                                                                                     | <span data-ttu-id="60940-120">ユーザーが指定されたメニューにアクセスできるかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="60940-120">Checks whether the user has access to the specified menu.</span></span>              |
| <span data-ttu-id="60940-121">public boolean hasMenuItemAccess(SecurableType type, MenuItemName menuItem, \[Common record\], \[DataAreaId dataArea\])</span><span class="sxs-lookup"><span data-stu-id="60940-121">public boolean hasMenuItemAccess(SecurableType type, MenuItemName menuItem, \[Common record\], \[DataAreaId dataArea\])</span></span>                                                                | <span data-ttu-id="60940-122">ユーザーが指定されたメニュー項目にアクセスできるかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="60940-122">Checks whether the user has access to the specified menu item.</span></span>         |
| <span data-ttu-id="60940-123">public boolean SysObsoleteAttribute(ClassName class, MethodName method)</span><span class="sxs-lookup"><span data-stu-id="60940-123">public boolean SysObsoleteAttribute(ClassName class, MethodName method)</span></span>                                                                                                                |                                                                        |
| <span data-ttu-id="60940-124">public boolean hasServiceOperationAccess(UtilElementName service, UtilElementName operation)</span><span class="sxs-lookup"><span data-stu-id="60940-124">public boolean hasServiceOperationAccess(UtilElementName service, UtilElementName operation)</span></span>                                                                                           | <span data-ttu-id="60940-125">ユーザーが指定されたサービス操作にアクセスできるかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="60940-125">Checks whether the user has access to the specified service operation.</span></span> |
| <span data-ttu-id="60940-126">public boolean isDeveloper()</span><span class="sxs-lookup"><span data-stu-id="60940-126">public boolean isDeveloper()</span></span>                                                                                                                                                           |                                                                        |
| <span data-ttu-id="60940-127">public boolean isSystemAdministrator()</span><span class="sxs-lookup"><span data-stu-id="60940-127">public boolean isSystemAdministrator()</span></span>                                                                                                                                                 | <span data-ttu-id="60940-128">現在のユーザーがシステム管理者であるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="60940-128">Checks whether the current user is a system administrator.</span></span>             |
| <span data-ttu-id="60940-129">public AccessRight menuItemAccessRight(SecurableType type, MenuItemName menuItem, \[DataAreaId dataArea\])</span><span class="sxs-lookup"><span data-stu-id="60940-129">public AccessRight menuItemAccessRight(SecurableType type, MenuItemName menuItem, \[DataAreaId dataArea\])</span></span>                                                                             | <span data-ttu-id="60940-130">メニュー項目のアクセス権を取得します。</span><span class="sxs-lookup"><span data-stu-id="60940-130">Retrieves the access rights for the menu item.</span></span>                         |
| <span data-ttu-id="60940-131">public AccessRight tableAccessRight(TableName tableName, \[Common record\], \[DataAreaId dataArea\], \[boolean includeDerived\], \[AutoAuthzMode autoAuthzMode\])</span><span class="sxs-lookup"><span data-stu-id="60940-131">public AccessRight tableAccessRight(TableName tableName, \[Common record\], \[DataAreaId dataArea\], \[boolean includeDerived\], \[AutoAuthzMode autoAuthzMode\])</span></span>                      | <span data-ttu-id="60940-132">テーブルのアクセス権を取得します。</span><span class="sxs-lookup"><span data-stu-id="60940-132">Retrieves the access rights for the table.</span></span>                             |
| <span data-ttu-id="60940-133">public SecurityTableRights tableFieldAccessRights(TableName tableName, \[Common record\], \[DataAreaId dataArea\], \[boolean includeDerived\], \[AutoAuthzMode autoAuthzMode\])</span><span class="sxs-lookup"><span data-stu-id="60940-133">public SecurityTableRights tableFieldAccessRights(TableName tableName, \[Common record\], \[DataAreaId dataArea\], \[boolean includeDerived\], \[AutoAuthzMode autoAuthzMode\])</span></span>        | <span data-ttu-id="60940-134">テーブルのフィールド アクセス権を取得します。</span><span class="sxs-lookup"><span data-stu-id="60940-134">Retrieves the field access rights for the table.</span></span>                       |
| <span data-ttu-id="60940-135">public Set variableAccessFields(TableName tableName, \[AccessRight targetAccess\], \[DataAreaId dataArea\])</span><span class="sxs-lookup"><span data-stu-id="60940-135">public Set variableAccessFields(TableName tableName, \[AccessRight targetAccess\], \[DataAreaId dataArea\])</span></span>                                                                            | <span data-ttu-id="60940-136">一連のテーブル フィールド ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="60940-136">Retrieves a set of the table field IDs.</span></span>                                |
| <span data-ttu-id="60940-137">public AccessRight webContentAccessRight(SecurableType type, WebContentItemName name)</span><span class="sxs-lookup"><span data-stu-id="60940-137">public AccessRight webContentAccessRight(SecurableType type, WebContentItemName name)</span></span>                                                                                                  | <span data-ttu-id="60940-138">Web コンテンツ項目のアクセス権を取得します。</span><span class="sxs-lookup"><span data-stu-id="60940-138">Retrieves the access rights for the web content item.</span></span>                  |
| <span data-ttu-id="60940-139">::public static SecurityRights construct()</span><span class="sxs-lookup"><span data-stu-id="60940-139">::public static SecurityRights construct()</span></span>                                                                                                                                             | <span data-ttu-id="60940-140">現在のユーザーの新しいセキュリティ権限インスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="60940-140">Creates a new security rights instance for the current user.</span></span>           |
| <span data-ttu-id="60940-141">::public static SecurityRights newUser(UserId user)</span><span class="sxs-lookup"><span data-stu-id="60940-141">::public static SecurityRights newUser(UserId user)</span></span>                                                                                                                                    | <span data-ttu-id="60940-142">特定のユーザーの新しいセキュリティ権限インスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="60940-142">Creates a new security rights instance for the specified user.</span></span>         |
| <span data-ttu-id="60940-143">private void new()</span><span class="sxs-lookup"><span data-stu-id="60940-143">private void new()</span></span>                                                                                                                                                                     | <span data-ttu-id="60940-144">SecurityRights クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="60940-144">Initializes a new instance of the SecurityRights class.</span></span>                |
| <span data-ttu-id="60940-145">public void populateSelectableCompanies()</span><span class="sxs-lookup"><span data-stu-id="60940-145">public void populateSelectableCompanies()</span></span>                                                                                                                                              | <span data-ttu-id="60940-146">選択できる会社を取得します。</span><span class="sxs-lookup"><span data-stu-id="60940-146">Populates the selectable companies.</span></span>                                    |

## <a name="method-hasdataserviceaccess"></a><span data-ttu-id="60940-147">メソッド hasDataServiceAccess</span><span class="sxs-lookup"><span data-stu-id="60940-147">Method hasDataServiceAccess</span></span>

```xpp
public boolean hasDataServiceAccess(SecurableName name, StatementType operation, [SecurableChildName fieldName])
```

### <a name="parameters---hasdataserviceaccess"></a><span data-ttu-id="60940-148">パラメーター - hasDataServiceAccess</span><span class="sxs-lookup"><span data-stu-id="60940-148">Parameters - hasDataServiceAccess</span></span>

<span data-ttu-id="60940-149">名前</span><span class="sxs-lookup"><span data-stu-id="60940-149">name</span></span>  

<!-- -->

<span data-ttu-id="60940-150">工程</span><span class="sxs-lookup"><span data-stu-id="60940-150">operation</span></span>  

<!-- -->

<span data-ttu-id="60940-151">fieldName</span><span class="sxs-lookup"><span data-stu-id="60940-151">fieldName</span></span>  

### <a name="return-value---hasdataserviceaccess"></a><span data-ttu-id="60940-152">戻り値 - hasDataServiceAccess</span><span class="sxs-lookup"><span data-stu-id="60940-152">Return Value - hasDataServiceAccess</span></span>

## <a name="method-hasdataservicemethodaccess"></a><span data-ttu-id="60940-153">メソッド hasDataServiceMethodAccess</span><span class="sxs-lookup"><span data-stu-id="60940-153">Method hasDataServiceMethodAccess</span></span>

```xpp
public boolean hasDataServiceMethodAccess(SecurableName name, StatementType operation, SecurableChildName methodName)
```

### <a name="parameters---hasdataservicemethodaccess"></a><span data-ttu-id="60940-154">パラメーター - hasDataServiceMethodAccess</span><span class="sxs-lookup"><span data-stu-id="60940-154">Parameters - hasDataServiceMethodAccess</span></span>

<span data-ttu-id="60940-155">名前</span><span class="sxs-lookup"><span data-stu-id="60940-155">name</span></span>  

<!-- -->

<span data-ttu-id="60940-156">工程</span><span class="sxs-lookup"><span data-stu-id="60940-156">operation</span></span>  

<!-- -->

<span data-ttu-id="60940-157">methodName</span><span class="sxs-lookup"><span data-stu-id="60940-157">methodName</span></span>  

### <a name="return-value---hasdataservicemethodaccess"></a><span data-ttu-id="60940-158">戻り値 - hasDataServiceMethodAccess</span><span class="sxs-lookup"><span data-stu-id="60940-158">Return Value - hasDataServiceMethodAccess</span></span>

## <a name="method-datamanagementaccessright"></a><span data-ttu-id="60940-159">メソッド dataManagementAccessRight</span><span class="sxs-lookup"><span data-stu-id="60940-159">Method dataManagementAccessRight</span></span>

```xpp
public AccessRight dataManagementAccessRight(SecurableName dataEntityName, [SecurableChildName fieldName])
```

### <a name="parameters---datamanagementaccessright"></a><span data-ttu-id="60940-160">パラメーター - dataManagementAccessRight</span><span class="sxs-lookup"><span data-stu-id="60940-160">Parameters - dataManagementAccessRight</span></span>

<span data-ttu-id="60940-161">dataEntityName</span><span class="sxs-lookup"><span data-stu-id="60940-161">dataEntityName</span></span>  

<!-- -->

<span data-ttu-id="60940-162">fieldName</span><span class="sxs-lookup"><span data-stu-id="60940-162">fieldName</span></span>  

### <a name="return-value---datamanagementaccessright"></a><span data-ttu-id="60940-163">戻り値 - dataManagementAccessRight</span><span class="sxs-lookup"><span data-stu-id="60940-163">Return Value - dataManagementAccessRight</span></span>

## <a name="method-listdataserviceaccess"></a><span data-ttu-id="60940-164">メソッド listDataServiceAccess</span><span class="sxs-lookup"><span data-stu-id="60940-164">Method listDataServiceAccess</span></span>

```xpp
public str listDataServiceAccess(SecurableName name, [SecurableChildName context])
```

### <a name="parameters---listdataserviceaccess"></a><span data-ttu-id="60940-165">パラメーター - listDataServiceAccess</span><span class="sxs-lookup"><span data-stu-id="60940-165">Parameters - listDataServiceAccess</span></span>

<span data-ttu-id="60940-166">名前</span><span class="sxs-lookup"><span data-stu-id="60940-166">name</span></span>  

<!-- -->

<span data-ttu-id="60940-167">context</span><span class="sxs-lookup"><span data-stu-id="60940-167">context</span></span>  

### <a name="return-value---listdataserviceaccess"></a><span data-ttu-id="60940-168">戻り値 - listDataServiceAccess</span><span class="sxs-lookup"><span data-stu-id="60940-168">Return Value - listDataServiceAccess</span></span>

## <a name="method-fieldaccessright"></a><span data-ttu-id="60940-169">メソッド fieldAccessRight</span><span class="sxs-lookup"><span data-stu-id="60940-169">Method fieldAccessRight</span></span>

<span data-ttu-id="60940-170">テーブルのフィールドのアクセス権を取得します。</span><span class="sxs-lookup"><span data-stu-id="60940-170">Retrieves the access rights for the field of the table.</span></span>

```xpp
public AccessRight fieldAccessRight(TableName tableName, FieldName fieldName, [Common record], [DataAreaId dataArea], [boolean includeDerived], [AutoAuthzMode autoAuthzMode])
```

### <a name="parameters---fieldaccessright"></a><span data-ttu-id="60940-171">パラメーター - fieldAccessRight</span><span class="sxs-lookup"><span data-stu-id="60940-171">Parameters - fieldAccessRight</span></span>

<span data-ttu-id="60940-172">tableName</span><span class="sxs-lookup"><span data-stu-id="60940-172">tableName</span></span>  

<!-- -->

<span data-ttu-id="60940-173">fieldName</span><span class="sxs-lookup"><span data-stu-id="60940-173">fieldName</span></span>  

<!-- -->

<span data-ttu-id="60940-174">記録</span><span class="sxs-lookup"><span data-stu-id="60940-174">record</span></span>  

<!-- -->

<span data-ttu-id="60940-175">dataArea</span><span class="sxs-lookup"><span data-stu-id="60940-175">dataArea</span></span>  

<!-- -->

<span data-ttu-id="60940-176">includeDerived</span><span class="sxs-lookup"><span data-stu-id="60940-176">includeDerived</span></span>  

<!-- -->

<span data-ttu-id="60940-177">autoAuthzMode</span><span class="sxs-lookup"><span data-stu-id="60940-177">autoAuthzMode</span></span>  

### <a name="return-value---fieldaccessright"></a><span data-ttu-id="60940-178">戻り値 - fieldAccessRight</span><span class="sxs-lookup"><span data-stu-id="60940-178">Return Value - fieldAccessRight</span></span>

<span data-ttu-id="60940-179">テーブルのフィールドの AccesRight インスタンス。</span><span class="sxs-lookup"><span data-stu-id="60940-179">The AccesRight instance for the field of the table.</span></span>

## <a name="method-formcontrolaccessright"></a><span data-ttu-id="60940-180">メソッド formControlAccessRight</span><span class="sxs-lookup"><span data-stu-id="60940-180">Method formControlAccessRight</span></span>

<span data-ttu-id="60940-181">フォーム コントロールのアクセス権を取得します。</span><span class="sxs-lookup"><span data-stu-id="60940-181">Retrieves the access rights for the form control.</span></span>

```xpp
public AccessRight formControlAccessRight(FormName form, UtilElementName control, [Common record], [DataAreaId dataArea])
```

### <a name="parameters---formcontrolaccessright"></a><span data-ttu-id="60940-182">パラメーター - formControlAccessRight</span><span class="sxs-lookup"><span data-stu-id="60940-182">Parameters - formControlAccessRight</span></span>

<span data-ttu-id="60940-183">フォーム</span><span class="sxs-lookup"><span data-stu-id="60940-183">form</span></span>  

<!-- -->

<span data-ttu-id="60940-184">control</span><span class="sxs-lookup"><span data-stu-id="60940-184">control</span></span>  

<!-- -->

<span data-ttu-id="60940-185">記録</span><span class="sxs-lookup"><span data-stu-id="60940-185">record</span></span>  

<!-- -->

<span data-ttu-id="60940-186">dataArea</span><span class="sxs-lookup"><span data-stu-id="60940-186">dataArea</span></span>  

### <a name="return-value---formcontrolaccessright"></a><span data-ttu-id="60940-187">戻り値 - formControlAccessRight</span><span class="sxs-lookup"><span data-stu-id="60940-187">Return Value - formControlAccessRight</span></span>

<span data-ttu-id="60940-188">フォーム コントロールの AccesRight インスタンス。</span><span class="sxs-lookup"><span data-stu-id="60940-188">The AccesRight instance for the form control.</span></span>

## <a name="method-getselectablecompanies"></a><span data-ttu-id="60940-189">メソッド getSelectableCompanies</span><span class="sxs-lookup"><span data-stu-id="60940-189">Method getSelectableCompanies</span></span>

```xpp
public container getSelectableCompanies()
```

### <a name="return-value---getselectablecompanies"></a><span data-ttu-id="60940-190">戻り値 - getSelectableCompanies</span><span class="sxs-lookup"><span data-stu-id="60940-190">Return Value - getSelectableCompanies</span></span>

## <a name="method-hasmenuaccess"></a><span data-ttu-id="60940-191">メソッド hasMenuAccess</span><span class="sxs-lookup"><span data-stu-id="60940-191">Method hasMenuAccess</span></span>

<span data-ttu-id="60940-192">ユーザーが指定されたメニューにアクセスできるかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="60940-192">Checks whether the user has access to the specified menu.</span></span>

```xpp
public boolean hasMenuAccess(MenuName menu, [boolean isWebMenu])
```

### <a name="parameters---hasmenuaccess"></a><span data-ttu-id="60940-193">パラメーター - hasMenuAccess</span><span class="sxs-lookup"><span data-stu-id="60940-193">Parameters - hasMenuAccess</span></span>

<span data-ttu-id="60940-194">メニュー</span><span class="sxs-lookup"><span data-stu-id="60940-194">menu</span></span>  

<!-- -->

<span data-ttu-id="60940-195">isWebMenu</span><span class="sxs-lookup"><span data-stu-id="60940-195">isWebMenu</span></span>  

### <a name="return-value---hasmenuaccess"></a><span data-ttu-id="60940-196">戻り値 - hasMenuAccess</span><span class="sxs-lookup"><span data-stu-id="60940-196">Return Value - hasMenuAccess</span></span>

<span data-ttu-id="60940-197">ユーザーがメニューへのアクセス権を持つ場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="60940-197">true if the user has access to the menu; otherwise, false.</span></span>

## <a name="method-hasmenuitemaccess"></a><span data-ttu-id="60940-198">メソッド hasMenuItemAccess</span><span class="sxs-lookup"><span data-stu-id="60940-198">Method hasMenuItemAccess</span></span>

<span data-ttu-id="60940-199">ユーザーが指定されたメニュー項目にアクセスできるかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="60940-199">Checks whether the user has access to the specified menu item.</span></span>

```xpp
public boolean hasMenuItemAccess(SecurableType type, MenuItemName menuItem, [Common record], [DataAreaId dataArea])
```

### <a name="parameters---hasmenuitemaccess"></a><span data-ttu-id="60940-200">パラメーター - hasMenuItemAccess</span><span class="sxs-lookup"><span data-stu-id="60940-200">Parameters - hasMenuItemAccess</span></span>

<span data-ttu-id="60940-201">タイプ</span><span class="sxs-lookup"><span data-stu-id="60940-201">type</span></span>  

<!-- -->

<span data-ttu-id="60940-202">menuItem</span><span class="sxs-lookup"><span data-stu-id="60940-202">menuItem</span></span>  

<!-- -->

<span data-ttu-id="60940-203">記録</span><span class="sxs-lookup"><span data-stu-id="60940-203">record</span></span>  

<!-- -->

<span data-ttu-id="60940-204">dataArea</span><span class="sxs-lookup"><span data-stu-id="60940-204">dataArea</span></span>  

### <a name="return-value---hasmenuitemaccess"></a><span data-ttu-id="60940-205">戻り値 - hasMenuItemAccess</span><span class="sxs-lookup"><span data-stu-id="60940-205">Return Value - hasMenuItemAccess</span></span>

<span data-ttu-id="60940-206">ユーザーがメニュー項目へのアクセス権を持つ場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="60940-206">true if the user has access to the menu item; otherwise, false.</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="60940-207">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="60940-207">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(ClassName class, MethodName method)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="60940-208">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="60940-208">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="60940-209">クラス</span><span class="sxs-lookup"><span data-stu-id="60940-209">class</span></span>  

<!-- -->

<span data-ttu-id="60940-210">メソッド</span><span class="sxs-lookup"><span data-stu-id="60940-210">method</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="60940-211">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="60940-211">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-hasserviceoperationaccess"></a><span data-ttu-id="60940-212">メソッド hasServiceOperationAccess</span><span class="sxs-lookup"><span data-stu-id="60940-212">Method hasServiceOperationAccess</span></span>

<span data-ttu-id="60940-213">ユーザーが指定されたサービス操作にアクセスできるかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="60940-213">Checks whether the user has access to the specified service operation.</span></span>

```xpp
public boolean hasServiceOperationAccess(UtilElementName service, UtilElementName operation)
```

### <a name="parameters---hasserviceoperationaccess"></a><span data-ttu-id="60940-214">パラメーター - hasServiceOperationAccess</span><span class="sxs-lookup"><span data-stu-id="60940-214">Parameters - hasServiceOperationAccess</span></span>

<span data-ttu-id="60940-215">サービス</span><span class="sxs-lookup"><span data-stu-id="60940-215">service</span></span>  

<!-- -->

<span data-ttu-id="60940-216">工程</span><span class="sxs-lookup"><span data-stu-id="60940-216">operation</span></span>  

### <a name="return-value---hasserviceoperationaccess"></a><span data-ttu-id="60940-217">戻り値 - hasServiceOperationAccess</span><span class="sxs-lookup"><span data-stu-id="60940-217">Return Value - hasServiceOperationAccess</span></span>

<span data-ttu-id="60940-218">ユーザーがサービス操作へのアクセス権を持つ場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="60940-218">true if user has access to the service operation; otherwise, false.</span></span>

## <a name="method-isdeveloper"></a><span data-ttu-id="60940-219">メソッド isDeveloper</span><span class="sxs-lookup"><span data-stu-id="60940-219">Method isDeveloper</span></span>

```xpp
public boolean isDeveloper()
```

### <a name="return-value---isdeveloper"></a><span data-ttu-id="60940-220">戻り値 - isDeveloper</span><span class="sxs-lookup"><span data-stu-id="60940-220">Return Value - isDeveloper</span></span>

## <a name="method-issystemadministrator"></a><span data-ttu-id="60940-221">メソッド isSystemAdministrator</span><span class="sxs-lookup"><span data-stu-id="60940-221">Method isSystemAdministrator</span></span>

<span data-ttu-id="60940-222">現在のユーザーがシステム管理者であるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="60940-222">Checks whether the current user is a system administrator.</span></span>

```xpp
public boolean isSystemAdministrator()
```

### <a name="return-value---issystemadministrator"></a><span data-ttu-id="60940-223">戻り値 - isSystemAdministrator</span><span class="sxs-lookup"><span data-stu-id="60940-223">Return Value - isSystemAdministrator</span></span>

<span data-ttu-id="60940-224">現在のユーザーがシステム管理者である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="60940-224">true if the current user is a system administrator; otherwise, false.</span></span>

## <a name="method-menuitemaccessright"></a><span data-ttu-id="60940-225">メソッド menuItemAccessRight</span><span class="sxs-lookup"><span data-stu-id="60940-225">Method menuItemAccessRight</span></span>

<span data-ttu-id="60940-226">メニュー項目のアクセス権を取得します。</span><span class="sxs-lookup"><span data-stu-id="60940-226">Retrieves the access rights for the menu item.</span></span>

```xpp
public AccessRight menuItemAccessRight(SecurableType type, MenuItemName menuItem, [DataAreaId dataArea])
```

### <a name="parameters---menuitemaccessright"></a><span data-ttu-id="60940-227">パラメーター - menuItemAccessRight</span><span class="sxs-lookup"><span data-stu-id="60940-227">Parameters - menuItemAccessRight</span></span>

<span data-ttu-id="60940-228">タイプ</span><span class="sxs-lookup"><span data-stu-id="60940-228">type</span></span>  

<!-- -->

<span data-ttu-id="60940-229">menuItem</span><span class="sxs-lookup"><span data-stu-id="60940-229">menuItem</span></span>  

<!-- -->

<span data-ttu-id="60940-230">dataArea</span><span class="sxs-lookup"><span data-stu-id="60940-230">dataArea</span></span>  

### <a name="return-value---menuitemaccessright"></a><span data-ttu-id="60940-231">戻り値 - menuItemAccessRight</span><span class="sxs-lookup"><span data-stu-id="60940-231">Return Value - menuItemAccessRight</span></span>

<span data-ttu-id="60940-232">項目の AccesRight インスタンス。</span><span class="sxs-lookup"><span data-stu-id="60940-232">The AccesRight instance for the item.</span></span>

## <a name="method-tableaccessright"></a><span data-ttu-id="60940-233">メソッド tableAccessRight</span><span class="sxs-lookup"><span data-stu-id="60940-233">Method tableAccessRight</span></span>

<span data-ttu-id="60940-234">テーブルのアクセス権を取得します。</span><span class="sxs-lookup"><span data-stu-id="60940-234">Retrieves the access rights for the table.</span></span>

```xpp
public AccessRight tableAccessRight(TableName tableName, [Common record], [DataAreaId dataArea], [boolean includeDerived], [AutoAuthzMode autoAuthzMode])
```

### <a name="parameters---tableaccessright"></a><span data-ttu-id="60940-235">パラメーター - tableAccessRight</span><span class="sxs-lookup"><span data-stu-id="60940-235">Parameters - tableAccessRight</span></span>

<span data-ttu-id="60940-236">tableName</span><span class="sxs-lookup"><span data-stu-id="60940-236">tableName</span></span>  

<!-- -->

<span data-ttu-id="60940-237">記録</span><span class="sxs-lookup"><span data-stu-id="60940-237">record</span></span>  

<!-- -->

<span data-ttu-id="60940-238">dataArea</span><span class="sxs-lookup"><span data-stu-id="60940-238">dataArea</span></span>  

<!-- -->

<span data-ttu-id="60940-239">includeDerived</span><span class="sxs-lookup"><span data-stu-id="60940-239">includeDerived</span></span>  

<!-- -->

<span data-ttu-id="60940-240">autoAuthzMode</span><span class="sxs-lookup"><span data-stu-id="60940-240">autoAuthzMode</span></span>  

### <a name="return-value---tableaccessright"></a><span data-ttu-id="60940-241">戻り値 - tableAccessRight</span><span class="sxs-lookup"><span data-stu-id="60940-241">Return Value - tableAccessRight</span></span>

<span data-ttu-id="60940-242">テーブルの AccesRight インスタンス。</span><span class="sxs-lookup"><span data-stu-id="60940-242">The AccesRight instance for the table.</span></span>

## <a name="method-tablefieldaccessrights"></a><span data-ttu-id="60940-243">メソッド tableFieldAccessRights</span><span class="sxs-lookup"><span data-stu-id="60940-243">Method tableFieldAccessRights</span></span>

<span data-ttu-id="60940-244">テーブルのフィールド アクセス権を取得します。</span><span class="sxs-lookup"><span data-stu-id="60940-244">Retrieves the field access rights for the table.</span></span>

```xpp
public SecurityTableRights tableFieldAccessRights(TableName tableName, [Common record], [DataAreaId dataArea], [boolean includeDerived], [AutoAuthzMode autoAuthzMode])
```

### <a name="parameters---tablefieldaccessrights"></a><span data-ttu-id="60940-245">パラメーター - tableFieldAccessRights</span><span class="sxs-lookup"><span data-stu-id="60940-245">Parameters - tableFieldAccessRights</span></span>

<span data-ttu-id="60940-246">tableName</span><span class="sxs-lookup"><span data-stu-id="60940-246">tableName</span></span>  

<!-- -->

<span data-ttu-id="60940-247">記録</span><span class="sxs-lookup"><span data-stu-id="60940-247">record</span></span>  

<!-- -->

<span data-ttu-id="60940-248">dataArea</span><span class="sxs-lookup"><span data-stu-id="60940-248">dataArea</span></span>  

<!-- -->

<span data-ttu-id="60940-249">includeDerived</span><span class="sxs-lookup"><span data-stu-id="60940-249">includeDerived</span></span>  

<!-- -->

<span data-ttu-id="60940-250">autoAuthzMode</span><span class="sxs-lookup"><span data-stu-id="60940-250">autoAuthzMode</span></span>  

### <a name="return-value---tablefieldaccessrights"></a><span data-ttu-id="60940-251">戻り値 - tableFieldAccessRights</span><span class="sxs-lookup"><span data-stu-id="60940-251">Return Value - tableFieldAccessRights</span></span>

<span data-ttu-id="60940-252">テーブルの SecurityTableRights インスタンス。</span><span class="sxs-lookup"><span data-stu-id="60940-252">The SecurityTableRights instance for the table.</span></span>

## <a name="method-variableaccessfields"></a><span data-ttu-id="60940-253">メソッド variableAccessFields</span><span class="sxs-lookup"><span data-stu-id="60940-253">Method variableAccessFields</span></span>

<span data-ttu-id="60940-254">一連のテーブル フィールド ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="60940-254">Retrieves a set of the table field IDs.</span></span>

```xpp
public Set variableAccessFields(TableName tableName, [AccessRight targetAccess], [DataAreaId dataArea])
```

### <a name="parameters---variableaccessfields"></a><span data-ttu-id="60940-255">パラメーター - variableAccessFields</span><span class="sxs-lookup"><span data-stu-id="60940-255">Parameters - variableAccessFields</span></span>

<span data-ttu-id="60940-256">tableName</span><span class="sxs-lookup"><span data-stu-id="60940-256">tableName</span></span>  

<!-- -->

<span data-ttu-id="60940-257">targetAccess</span><span class="sxs-lookup"><span data-stu-id="60940-257">targetAccess</span></span>  

<!-- -->

<span data-ttu-id="60940-258">dataArea</span><span class="sxs-lookup"><span data-stu-id="60940-258">dataArea</span></span>  

### <a name="return-value---variableaccessfields"></a><span data-ttu-id="60940-259">戻り値 - variableAccessFields</span><span class="sxs-lookup"><span data-stu-id="60940-259">Return Value - variableAccessFields</span></span>

<span data-ttu-id="60940-260">一連のテーブル フィールド ID。</span><span class="sxs-lookup"><span data-stu-id="60940-260">A set of the table field IDs.</span></span>

## <a name="method-webcontentaccessright"></a><span data-ttu-id="60940-261">メソッド webContentAccessRight</span><span class="sxs-lookup"><span data-stu-id="60940-261">Method webContentAccessRight</span></span>

<span data-ttu-id="60940-262">Web コンテンツ項目のアクセス権を取得します。</span><span class="sxs-lookup"><span data-stu-id="60940-262">Retrieves the access rights for the web content item.</span></span>

```xpp
public AccessRight webContentAccessRight(SecurableType type, WebContentItemName name)
```

### <a name="parameters---webcontentaccessright"></a><span data-ttu-id="60940-263">パラメーター - webContentAccessRight</span><span class="sxs-lookup"><span data-stu-id="60940-263">Parameters - webContentAccessRight</span></span>

<span data-ttu-id="60940-264">タイプ</span><span class="sxs-lookup"><span data-stu-id="60940-264">type</span></span>  

<!-- -->

<span data-ttu-id="60940-265">名前</span><span class="sxs-lookup"><span data-stu-id="60940-265">name</span></span>  

### <a name="return-value---webcontentaccessright"></a><span data-ttu-id="60940-266">戻り値 - webContentAccessRight</span><span class="sxs-lookup"><span data-stu-id="60940-266">Return Value - webContentAccessRight</span></span>

<span data-ttu-id="60940-267">項目の AccesRight インスタンス。</span><span class="sxs-lookup"><span data-stu-id="60940-267">The AccesRight instance for the item.</span></span>

## <a name="method-construct"></a><span data-ttu-id="60940-268">メソッド construct</span><span class="sxs-lookup"><span data-stu-id="60940-268">Method construct</span></span>

<span data-ttu-id="60940-269">現在のユーザーの新しいセキュリティ権限インスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="60940-269">Creates a new security rights instance for the current user.</span></span>

```xpp
public static SecurityRights construct()
```

### <a name="return-value---construct"></a><span data-ttu-id="60940-270">戻り値 - construct</span><span class="sxs-lookup"><span data-stu-id="60940-270">Return Value - construct</span></span>

<span data-ttu-id="60940-271">作成された SecurityRights インスタンスです。</span><span class="sxs-lookup"><span data-stu-id="60940-271">The SecurityRights instance that was created.</span></span>

## <a name="method-newuser"></a><span data-ttu-id="60940-272">メソッド newUser</span><span class="sxs-lookup"><span data-stu-id="60940-272">Method newUser</span></span>

<span data-ttu-id="60940-273">特定のユーザーの新しいセキュリティ権限インスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="60940-273">Creates a new security rights instance for the specified user.</span></span>

```xpp
public static SecurityRights newUser(UserId user)
```

### <a name="parameters---newuser"></a><span data-ttu-id="60940-274">パラメーター - newUser</span><span class="sxs-lookup"><span data-stu-id="60940-274">Parameters - newUser</span></span>

<span data-ttu-id="60940-275">ユーザー</span><span class="sxs-lookup"><span data-stu-id="60940-275">user</span></span>  

### <a name="return-value---newuser"></a><span data-ttu-id="60940-276">戻り値 - newUser</span><span class="sxs-lookup"><span data-stu-id="60940-276">Return Value - newUser</span></span>

<span data-ttu-id="60940-277">作成された SecurityRights インスタンスです。</span><span class="sxs-lookup"><span data-stu-id="60940-277">The SecurityRights instance that was created.</span></span>

## <a name="method-new"></a><span data-ttu-id="60940-278">メソッド new</span><span class="sxs-lookup"><span data-stu-id="60940-278">Method new</span></span>

<span data-ttu-id="60940-279">SecurityRights クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="60940-279">Initializes a new instance of the SecurityRights class.</span></span>

```xpp
private void new()
```

## <a name="method-populateselectablecompanies"></a><span data-ttu-id="60940-280">メソッド populateSelectableCompanies</span><span class="sxs-lookup"><span data-stu-id="60940-280">Method populateSelectableCompanies</span></span>

<span data-ttu-id="60940-281">選択できる会社を取得します。</span><span class="sxs-lookup"><span data-stu-id="60940-281">Populates the selectable companies.</span></span>

```xpp
public void populateSelectableCompanies()
```

