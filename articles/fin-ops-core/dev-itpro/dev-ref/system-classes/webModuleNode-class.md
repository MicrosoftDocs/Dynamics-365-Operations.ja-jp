---
title: webModuleNode クラス
description: このトピックでは、webModuleNode クラスについて説明します。
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
ms.openlocfilehash: 989463ca6fc709662e84749b33fa376d278789e3
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502998"
---
# <a name="class-webmodulenode"></a><span data-ttu-id="72b7a-103">クラス webModuleNode</span><span class="sxs-lookup"><span data-stu-id="72b7a-103">Class webModuleNode</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class webModuleNode extends TreeNode
```

## <a name="remarks"></a><span data-ttu-id="72b7a-104">備考</span><span class="sxs-lookup"><span data-stu-id="72b7a-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="72b7a-105">例</span><span class="sxs-lookup"><span data-stu-id="72b7a-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="72b7a-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="72b7a-106">Methods</span></span>

| <span data-ttu-id="72b7a-107">方法</span><span class="sxs-lookup"><span data-stu-id="72b7a-107">Method</span></span>                                                                   | <span data-ttu-id="72b7a-108">説明</span><span class="sxs-lookup"><span data-stu-id="72b7a-108">Description</span></span>                                                                                                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72b7a-109">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="72b7a-109">public str changedBy(\[str value\])</span></span>                                      | <span data-ttu-id="72b7a-110">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="72b7a-110">Gets or sets the name of the user who last changed the application object.</span></span>                                                                     |
| <span data-ttu-id="72b7a-111">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="72b7a-111">public Date changedDate(\[Date value\])</span></span>                                  | <span data-ttu-id="72b7a-112">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="72b7a-112">Gets or sets the date an application object was last changed.</span></span>                                                                                  |
| <span data-ttu-id="72b7a-113">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="72b7a-113">public str changedTime(\[str value\])</span></span>                                    | <span data-ttu-id="72b7a-114">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="72b7a-114">Gets or sets the time an application object was last changed.</span></span>                                                                                  |
| <span data-ttu-id="72b7a-115">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="72b7a-115">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span> | <span data-ttu-id="72b7a-116">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="72b7a-116">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                            |
| <span data-ttu-id="72b7a-117">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="72b7a-117">public str createdBy(\[str value\])</span></span>                                      | <span data-ttu-id="72b7a-118">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="72b7a-118">Gets or sets the name of the user who created the application object.</span></span>                                                                          |
| <span data-ttu-id="72b7a-119">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="72b7a-119">public Date creationDate(\[Date value\])</span></span>                                 | <span data-ttu-id="72b7a-120">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="72b7a-120">Gets or sets the date an application object was created.</span></span>                                                                                       |
| <span data-ttu-id="72b7a-121">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="72b7a-121">public str creationTime(\[str value\])</span></span>                                   |                                                                                                                                                |
| <span data-ttu-id="72b7a-122">public boolean extendedDataSecurity(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="72b7a-122">public boolean extendedDataSecurity(\[boolean value\])</span></span>                   |                                                                                                                                                |
| <span data-ttu-id="72b7a-123">public boolean inheritNavigation(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="72b7a-123">public boolean inheritNavigation(\[boolean value\])</span></span>                      |                                                                                                                                                |
| <span data-ttu-id="72b7a-124">public boolean inheritPermissions(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="72b7a-124">public boolean inheritPermissions(\[boolean value\])</span></span>                     |                                                                                                                                                |
| <span data-ttu-id="72b7a-125">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="72b7a-125">public str label(\[str value\])</span></span>                                          | <span data-ttu-id="72b7a-126">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="72b7a-126">Gets or sets the label for a control.</span></span>                                                                                                          |
| <span data-ttu-id="72b7a-127">public str masterPage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="72b7a-127">public str masterPage(\[str value\])</span></span>                                     |                                                                                                                                                |
| <span data-ttu-id="72b7a-128">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="72b7a-128">public str menuItemName(\[str value\])</span></span>                                   |                                                                                                                                                |
| <span data-ttu-id="72b7a-129">public WebMenuItemType menuItemType(\[WebMenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="72b7a-129">public WebMenuItemType menuItemType(\[WebMenuItemType value\])</span></span>           |                                                                                                                                                |
| <span data-ttu-id="72b7a-130">public str moduleName()</span><span class="sxs-lookup"><span data-stu-id="72b7a-130">public str moduleName()</span></span>                                                  |                                                                                                                                                |
| <span data-ttu-id="72b7a-131">public str modulePath()</span><span class="sxs-lookup"><span data-stu-id="72b7a-131">public str modulePath()</span></span>                                                  |                                                                                                                                                |
| <span data-ttu-id="72b7a-132">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="72b7a-132">public str name(\[str value\])</span></span>                                           | <span data-ttu-id="72b7a-133">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="72b7a-133">Gets or sets the name that is used in the code to identify a form, report, rabble, query, or other application object.</span></span> |
| <span data-ttu-id="72b7a-134">public int neededAccessLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="72b7a-134">public int neededAccessLevel(\[int value\])</span></span>                              | <span data-ttu-id="72b7a-135">MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="72b7a-135">Gets or sets the neededAccessLevel property for the MenuFunction class.</span></span>                                                                        |
| <span data-ttu-id="72b7a-136">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="72b7a-136">public Guid origin(\[Guid value\])</span></span>                                       |                                                                                                                                                |
| <span data-ttu-id="72b7a-137">public boolean publicModule(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="72b7a-137">public boolean publicModule(\[boolean value\])</span></span>                           |                                                                                                                                                |
| <span data-ttu-id="72b7a-138">public str quickLaunch(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="72b7a-138">public str quickLaunch(\[str value\])</span></span>                                    |                                                                                                                                                |
| <span data-ttu-id="72b7a-139">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="72b7a-139">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                |                                                                                                                                                |
| <span data-ttu-id="72b7a-140">public boolean showLink(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="72b7a-140">public boolean showLink(\[boolean value\])</span></span>                               |                                                                                                                                                |
| <span data-ttu-id="72b7a-141">public boolean showParentModule(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="72b7a-141">public boolean showParentModule(\[boolean value\])</span></span>                       |                                                                                                                                                |
| <span data-ttu-id="72b7a-142">public void addSubModule(str name)</span><span class="sxs-lookup"><span data-stu-id="72b7a-142">public void addSubModule(str name)</span></span>                                       |                                                                                                                                                |
| <span data-ttu-id="72b7a-143">public void new(str Name)</span><span class="sxs-lookup"><span data-stu-id="72b7a-143">public void new(str Name)</span></span>                                                | <span data-ttu-id="72b7a-144">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="72b7a-144">Initializes a new instance of the TreeNode class.</span></span>                                                                                              |
| <span data-ttu-id="72b7a-145">public void addMenuitem(WebMenuFunction webMenuFunction)</span><span class="sxs-lookup"><span data-stu-id="72b7a-145">public void addMenuitem(WebMenuFunction webMenuFunction)</span></span>                 |                                                                                                                                                |

## <a name="method-changedby"></a><span data-ttu-id="72b7a-146">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="72b7a-146">Method changedBy</span></span>

<span data-ttu-id="72b7a-147">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="72b7a-147">Gets or sets the name of the user who last changed the application object.</span></span>

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a><span data-ttu-id="72b7a-148">パラメーター - changedBy</span><span class="sxs-lookup"><span data-stu-id="72b7a-148">Parameters - changedBy</span></span>

<span data-ttu-id="72b7a-149">値</span><span class="sxs-lookup"><span data-stu-id="72b7a-149">value</span></span>  

### <a name="return-value---changedby"></a><span data-ttu-id="72b7a-150">戻り値 - changedBy</span><span class="sxs-lookup"><span data-stu-id="72b7a-150">Return Value - changedBy</span></span>

<span data-ttu-id="72b7a-151">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="72b7a-151">The name of the user.</span></span>

## <a name="method-changeddate"></a><span data-ttu-id="72b7a-152">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="72b7a-152">Method changedDate</span></span>

<span data-ttu-id="72b7a-153">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="72b7a-153">Gets or sets the date an application object was last changed.</span></span>

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a><span data-ttu-id="72b7a-154">パラメーター - changedDate</span><span class="sxs-lookup"><span data-stu-id="72b7a-154">Parameters - changedDate</span></span>

<span data-ttu-id="72b7a-155">値</span><span class="sxs-lookup"><span data-stu-id="72b7a-155">value</span></span>  

### <a name="return-value---changeddate"></a><span data-ttu-id="72b7a-156">戻り値 - changedDate</span><span class="sxs-lookup"><span data-stu-id="72b7a-156">Return Value - changedDate</span></span>

<span data-ttu-id="72b7a-157">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="72b7a-157">The date an application object was last changed.</span></span>

## <a name="method-changedtime"></a><span data-ttu-id="72b7a-158">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="72b7a-158">Method changedTime</span></span>

<span data-ttu-id="72b7a-159">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="72b7a-159">Gets or sets the time an application object was last changed.</span></span>

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a><span data-ttu-id="72b7a-160">パラメーター - changedTime</span><span class="sxs-lookup"><span data-stu-id="72b7a-160">Parameters - changedTime</span></span>

<span data-ttu-id="72b7a-161">値</span><span class="sxs-lookup"><span data-stu-id="72b7a-161">value</span></span>  

### <a name="return-value---changedtime"></a><span data-ttu-id="72b7a-162">戻り値 - changedTime</span><span class="sxs-lookup"><span data-stu-id="72b7a-162">Return Value - changedTime</span></span>

<span data-ttu-id="72b7a-163">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="72b7a-163">The time an application object was last changed.</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="72b7a-164">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="72b7a-164">Method configurationKey</span></span>

<span data-ttu-id="72b7a-165">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="72b7a-165">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="72b7a-166">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="72b7a-166">Parameters - configurationKey</span></span>

<span data-ttu-id="72b7a-167">値</span><span class="sxs-lookup"><span data-stu-id="72b7a-167">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="72b7a-168">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="72b7a-168">Return Value - configurationKey</span></span>

<span data-ttu-id="72b7a-169">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="72b7a-169">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="72b7a-170">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="72b7a-170">Remarks - configurationKey</span></span>

<span data-ttu-id="72b7a-171">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="72b7a-171">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="72b7a-172">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="72b7a-172">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-createdby"></a><span data-ttu-id="72b7a-173">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="72b7a-173">Method createdBy</span></span>

<span data-ttu-id="72b7a-174">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="72b7a-174">Gets or sets the name of the user who created the application object.</span></span>

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a><span data-ttu-id="72b7a-175">パラメーター - createdBy</span><span class="sxs-lookup"><span data-stu-id="72b7a-175">Parameters - createdBy</span></span>

<span data-ttu-id="72b7a-176">値</span><span class="sxs-lookup"><span data-stu-id="72b7a-176">value</span></span>  

### <a name="return-value---createdby"></a><span data-ttu-id="72b7a-177">戻り値 - createdBy</span><span class="sxs-lookup"><span data-stu-id="72b7a-177">Return Value - createdBy</span></span>

<span data-ttu-id="72b7a-178">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="72b7a-178">The name of the user.</span></span>

## <a name="method-creationdate"></a><span data-ttu-id="72b7a-179">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="72b7a-179">Method creationDate</span></span>

<span data-ttu-id="72b7a-180">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="72b7a-180">Gets or sets the date an application object was created.</span></span>

```xpp
public Date creationDate([Date value])
```

### <a name="parameters---creationdate"></a><span data-ttu-id="72b7a-181">パラメーター - creationDate</span><span class="sxs-lookup"><span data-stu-id="72b7a-181">Parameters - creationDate</span></span>

<span data-ttu-id="72b7a-182">値</span><span class="sxs-lookup"><span data-stu-id="72b7a-182">value</span></span>  

### <a name="return-value---creationdate"></a><span data-ttu-id="72b7a-183">戻り値 - creationDate</span><span class="sxs-lookup"><span data-stu-id="72b7a-183">Return Value - creationDate</span></span>

<span data-ttu-id="72b7a-184">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="72b7a-184">The date an application object was created.</span></span>

## <a name="method-creationtime"></a><span data-ttu-id="72b7a-185">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="72b7a-185">Method creationTime</span></span>

```xpp
public str creationTime([str value])
```

### <a name="parameters---creationtime"></a><span data-ttu-id="72b7a-186">パラメーター - creationTime</span><span class="sxs-lookup"><span data-stu-id="72b7a-186">Parameters - creationTime</span></span>

<span data-ttu-id="72b7a-187">値</span><span class="sxs-lookup"><span data-stu-id="72b7a-187">value</span></span>  

### <a name="return-value---creationtime"></a><span data-ttu-id="72b7a-188">戻り値 - creationTime</span><span class="sxs-lookup"><span data-stu-id="72b7a-188">Return Value - creationTime</span></span>

## <a name="method-extendeddatasecurity"></a><span data-ttu-id="72b7a-189">メソッド extendedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="72b7a-189">Method extendedDataSecurity</span></span>

```xpp
public boolean extendedDataSecurity([boolean value])
```

### <a name="parameters---extendeddatasecurity"></a><span data-ttu-id="72b7a-190">パラメーター - extendedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="72b7a-190">Parameters - extendedDataSecurity</span></span>

<span data-ttu-id="72b7a-191">値</span><span class="sxs-lookup"><span data-stu-id="72b7a-191">value</span></span>  

### <a name="return-value---extendeddatasecurity"></a><span data-ttu-id="72b7a-192">戻り値 - extendedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="72b7a-192">Return Value - extendedDataSecurity</span></span>

## <a name="method-inheritnavigation"></a><span data-ttu-id="72b7a-193">メソッド inheritNavigation</span><span class="sxs-lookup"><span data-stu-id="72b7a-193">Method inheritNavigation</span></span>

```xpp
public boolean inheritNavigation([boolean value])
```

### <a name="parameters---inheritnavigation"></a><span data-ttu-id="72b7a-194">パラメーター - inheritNavigation</span><span class="sxs-lookup"><span data-stu-id="72b7a-194">Parameters - inheritNavigation</span></span>

<span data-ttu-id="72b7a-195">値</span><span class="sxs-lookup"><span data-stu-id="72b7a-195">value</span></span>  

### <a name="return-value---inheritnavigation"></a><span data-ttu-id="72b7a-196">戻り値 - - inheritNavigation</span><span class="sxs-lookup"><span data-stu-id="72b7a-196">Return Value - inheritNavigation</span></span>

## <a name="method-inheritpermissions"></a><span data-ttu-id="72b7a-197">メソッド inheritPermissions</span><span class="sxs-lookup"><span data-stu-id="72b7a-197">Method inheritPermissions</span></span>

```xpp
public boolean inheritPermissions([boolean value])
```

### <a name="parameters---inheritpermissions"></a><span data-ttu-id="72b7a-198">パラメーター - inheritPermissions</span><span class="sxs-lookup"><span data-stu-id="72b7a-198">Parameters - inheritPermissions</span></span>

<span data-ttu-id="72b7a-199">値</span><span class="sxs-lookup"><span data-stu-id="72b7a-199">value</span></span>  

### <a name="return-value---inheritpermissions"></a><span data-ttu-id="72b7a-200">戻り値 - inheritPermissions</span><span class="sxs-lookup"><span data-stu-id="72b7a-200">Return Value - inheritPermissions</span></span>

## <a name="method-label"></a><span data-ttu-id="72b7a-201">メソッド label</span><span class="sxs-lookup"><span data-stu-id="72b7a-201">Method label</span></span>

<span data-ttu-id="72b7a-202">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="72b7a-202">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="72b7a-203">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="72b7a-203">Parameters - label</span></span>

<span data-ttu-id="72b7a-204">値</span><span class="sxs-lookup"><span data-stu-id="72b7a-204">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="72b7a-205">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="72b7a-205">Return Value - label</span></span>

<span data-ttu-id="72b7a-206">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="72b7a-206">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="72b7a-207">備考 - label</span><span class="sxs-lookup"><span data-stu-id="72b7a-207">Remarks - label</span></span>

<span data-ttu-id="72b7a-208">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="72b7a-208">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="72b7a-209">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="72b7a-209">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-masterpage"></a><span data-ttu-id="72b7a-210">メソッド masterPage</span><span class="sxs-lookup"><span data-stu-id="72b7a-210">Method masterPage</span></span>

```xpp
public str masterPage([str value])
```

### <a name="parameters---masterpage"></a><span data-ttu-id="72b7a-211">パラメーター - masterPage</span><span class="sxs-lookup"><span data-stu-id="72b7a-211">Parameters - masterPage</span></span>

<span data-ttu-id="72b7a-212">値</span><span class="sxs-lookup"><span data-stu-id="72b7a-212">value</span></span>  

### <a name="return-value---masterpage"></a><span data-ttu-id="72b7a-213">戻り値 - masterPage</span><span class="sxs-lookup"><span data-stu-id="72b7a-213">Return Value - masterPage</span></span>

## <a name="method-menuitemname"></a><span data-ttu-id="72b7a-214">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="72b7a-214">Method menuItemName</span></span>

```xpp
public str menuItemName([str value])
```

### <a name="parameters---menuitemname"></a><span data-ttu-id="72b7a-215">パラメーター - menuItemName</span><span class="sxs-lookup"><span data-stu-id="72b7a-215">Parameters - menuItemName</span></span>

<span data-ttu-id="72b7a-216">値</span><span class="sxs-lookup"><span data-stu-id="72b7a-216">value</span></span>  

### <a name="return-value---menuitemname"></a><span data-ttu-id="72b7a-217">戻り値 - menuItemName</span><span class="sxs-lookup"><span data-stu-id="72b7a-217">Return Value - menuItemName</span></span>

## <a name="method-menuitemtype"></a><span data-ttu-id="72b7a-218">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="72b7a-218">Method menuItemType</span></span>

```xpp
public WebMenuItemType menuItemType([WebMenuItemType value])
```

### <a name="parameters---menuitemtype"></a><span data-ttu-id="72b7a-219">パラメーター - menuItemType</span><span class="sxs-lookup"><span data-stu-id="72b7a-219">Parameters - menuItemType</span></span>

<span data-ttu-id="72b7a-220">値</span><span class="sxs-lookup"><span data-stu-id="72b7a-220">value</span></span>  

### <a name="return-value---menuitemtype"></a><span data-ttu-id="72b7a-221">戻り値 - menuItemType</span><span class="sxs-lookup"><span data-stu-id="72b7a-221">Return Value - menuItemType</span></span>

## <a name="method-modulename"></a><span data-ttu-id="72b7a-222">メソッド moduleName</span><span class="sxs-lookup"><span data-stu-id="72b7a-222">Method moduleName</span></span>

```xpp
public str moduleName()
```

### <a name="return-value---modulename"></a><span data-ttu-id="72b7a-223">戻り値 - moduleName</span><span class="sxs-lookup"><span data-stu-id="72b7a-223">Return Value - moduleName</span></span>

## <a name="method-modulepath"></a><span data-ttu-id="72b7a-224">メソッド modulePath</span><span class="sxs-lookup"><span data-stu-id="72b7a-224">Method modulePath</span></span>

```xpp
public str modulePath()
```

### <a name="return-value---modulepath"></a><span data-ttu-id="72b7a-225">戻り値 - modulePath</span><span class="sxs-lookup"><span data-stu-id="72b7a-225">Return Value - modulePath</span></span>

## <a name="method-name"></a><span data-ttu-id="72b7a-226">メソッド名</span><span class="sxs-lookup"><span data-stu-id="72b7a-226">Method name</span></span>

<span data-ttu-id="72b7a-227">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="72b7a-227">Gets or sets the name that is used in the code to identify a form, report, rabble, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="72b7a-228">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="72b7a-228">Parameters - name</span></span>

<span data-ttu-id="72b7a-229">値</span><span class="sxs-lookup"><span data-stu-id="72b7a-229">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="72b7a-230">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="72b7a-230">Return Value - name</span></span>

<span data-ttu-id="72b7a-231">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="72b7a-231">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="72b7a-232">備考 - name</span><span class="sxs-lookup"><span data-stu-id="72b7a-232">Remarks - name</span></span>

<span data-ttu-id="72b7a-233">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="72b7a-233">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="72b7a-234">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="72b7a-234">Begins with a letter.</span></span>
-   <span data-ttu-id="72b7a-235">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="72b7a-235">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="72b7a-236">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="72b7a-236">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="72b7a-237">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="72b7a-237">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="72b7a-238">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="72b7a-238">Tables cannot have the same name as other public objects, such as extended data types, base enumerations, or classes.</span></span>

## <a name="method-neededaccesslevel"></a><span data-ttu-id="72b7a-239">メソッド neededAccessLevel</span><span class="sxs-lookup"><span data-stu-id="72b7a-239">Method neededAccessLevel</span></span>

<span data-ttu-id="72b7a-240">MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="72b7a-240">Gets or sets the neededAccessLevel property for the MenuFunction class.</span></span>

```xpp
public int neededAccessLevel([int value])
```

### <a name="parameters---neededaccesslevel"></a><span data-ttu-id="72b7a-241">パラメーター - neededAccessLevel</span><span class="sxs-lookup"><span data-stu-id="72b7a-241">Parameters - neededAccessLevel</span></span>

<span data-ttu-id="72b7a-242">値</span><span class="sxs-lookup"><span data-stu-id="72b7a-242">value</span></span>  

### <a name="return-value---neededaccesslevel"></a><span data-ttu-id="72b7a-243">戻り値 - neededAccessLevel</span><span class="sxs-lookup"><span data-stu-id="72b7a-243">Return Value - neededAccessLevel</span></span>

<span data-ttu-id="72b7a-244">neededAccessLevel プロパティの現在の値。</span><span class="sxs-lookup"><span data-stu-id="72b7a-244">The current value of the neededAccessLevel property.</span></span>

### <a name="remarks---neededaccesslevel"></a><span data-ttu-id="72b7a-245">備考 - neededAccessLevel</span><span class="sxs-lookup"><span data-stu-id="72b7a-245">Remarks - neededAccessLevel</span></span>

<span data-ttu-id="72b7a-246">AccessType システム列挙値の使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="72b7a-246">The possible values for the AccessType system enumeration value are as follows:</span></span>

-   <span data-ttu-id="72b7a-247">AccessType::NoAccess</span><span class="sxs-lookup"><span data-stu-id="72b7a-247">AccessType::NoAccess</span></span>
-   <span data-ttu-id="72b7a-248">AccessType::View</span><span class="sxs-lookup"><span data-stu-id="72b7a-248">AccessType::View</span></span>
-   <span data-ttu-id="72b7a-249">AccessType::Edit</span><span class="sxs-lookup"><span data-stu-id="72b7a-249">AccessType::Edit</span></span>
-   <span data-ttu-id="72b7a-250">AccessType::Add</span><span class="sxs-lookup"><span data-stu-id="72b7a-250">AccessType::Add</span></span>
-   <span data-ttu-id="72b7a-251">AccessType::Delete</span><span class="sxs-lookup"><span data-stu-id="72b7a-251">AccessType::Delete</span></span>

## <a name="method-origin"></a><span data-ttu-id="72b7a-252">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="72b7a-252">Method origin</span></span>

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a><span data-ttu-id="72b7a-253">パラメーター - origin</span><span class="sxs-lookup"><span data-stu-id="72b7a-253">Parameters - origin</span></span>

<span data-ttu-id="72b7a-254">値</span><span class="sxs-lookup"><span data-stu-id="72b7a-254">value</span></span>  

### <a name="return-value---origin"></a><span data-ttu-id="72b7a-255">戻り値 - origin</span><span class="sxs-lookup"><span data-stu-id="72b7a-255">Return Value - origin</span></span>

## <a name="method-publicmodule"></a><span data-ttu-id="72b7a-256">メソッド publicModule</span><span class="sxs-lookup"><span data-stu-id="72b7a-256">Method publicModule</span></span>

```xpp
public boolean publicModule([boolean value])
```

### <a name="parameters---publicmodule"></a><span data-ttu-id="72b7a-257">パラメーター - publicModule</span><span class="sxs-lookup"><span data-stu-id="72b7a-257">Parameters - publicModule</span></span>

<span data-ttu-id="72b7a-258">値</span><span class="sxs-lookup"><span data-stu-id="72b7a-258">value</span></span>  

### <a name="return-value---publicmodule"></a><span data-ttu-id="72b7a-259">戻り値 - publicModule</span><span class="sxs-lookup"><span data-stu-id="72b7a-259">Return Value - publicModule</span></span>

## <a name="method-quicklaunch"></a><span data-ttu-id="72b7a-260">メソッド quickLaunch</span><span class="sxs-lookup"><span data-stu-id="72b7a-260">Method quickLaunch</span></span>

```xpp
public str quickLaunch([str value])
```

### <a name="parameters---quicklaunch"></a><span data-ttu-id="72b7a-261">パラメーター - quickLaunch</span><span class="sxs-lookup"><span data-stu-id="72b7a-261">Parameters - quickLaunch</span></span>

<span data-ttu-id="72b7a-262">値</span><span class="sxs-lookup"><span data-stu-id="72b7a-262">value</span></span>  

### <a name="return-value---quicklaunch"></a><span data-ttu-id="72b7a-263">戻り値 - quickLaunch</span><span class="sxs-lookup"><span data-stu-id="72b7a-263">Return Value - quickLaunch</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="72b7a-264">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="72b7a-264">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="72b7a-265">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="72b7a-265">Parameters - securityKey</span></span>

<span data-ttu-id="72b7a-266">値</span><span class="sxs-lookup"><span data-stu-id="72b7a-266">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="72b7a-267">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="72b7a-267">Return Value - securityKey</span></span>

## <a name="method-showlink"></a><span data-ttu-id="72b7a-268">メソッド showLink</span><span class="sxs-lookup"><span data-stu-id="72b7a-268">Method showLink</span></span>

```xpp
public boolean showLink([boolean value])
```

### <a name="parameters---showlink"></a><span data-ttu-id="72b7a-269">パラメーター - showLink</span><span class="sxs-lookup"><span data-stu-id="72b7a-269">Parameters - showLink</span></span>

<span data-ttu-id="72b7a-270">値</span><span class="sxs-lookup"><span data-stu-id="72b7a-270">value</span></span>  

### <a name="return-value---showlink"></a><span data-ttu-id="72b7a-271">戻り値 - showLink</span><span class="sxs-lookup"><span data-stu-id="72b7a-271">Return Value - showLink</span></span>

## <a name="method-showparentmodule"></a><span data-ttu-id="72b7a-272">メソッド showParentModule</span><span class="sxs-lookup"><span data-stu-id="72b7a-272">Method showParentModule</span></span>

```xpp
public boolean showParentModule([boolean value])
```

### <a name="parameters---showparentmodule"></a><span data-ttu-id="72b7a-273">パラメーター - showParentModule</span><span class="sxs-lookup"><span data-stu-id="72b7a-273">Parameters - showParentModule</span></span>

<span data-ttu-id="72b7a-274">値</span><span class="sxs-lookup"><span data-stu-id="72b7a-274">value</span></span>  

### <a name="return-value---showparentmodule"></a><span data-ttu-id="72b7a-275">戻り値 - showParentModule</span><span class="sxs-lookup"><span data-stu-id="72b7a-275">Return Value - showParentModule</span></span>

## <a name="method-addsubmodule"></a><span data-ttu-id="72b7a-276">メソッド addSubModule</span><span class="sxs-lookup"><span data-stu-id="72b7a-276">Method addSubModule</span></span>

```xpp
public void addSubModule(str name)
```

### <a name="parameters---addsubmodule"></a><span data-ttu-id="72b7a-277">パラメーター - addSubModule</span><span class="sxs-lookup"><span data-stu-id="72b7a-277">Parameters - addSubModule</span></span>

<span data-ttu-id="72b7a-278">名前</span><span class="sxs-lookup"><span data-stu-id="72b7a-278">name</span></span>  

## <a name="method-new"></a><span data-ttu-id="72b7a-279">メソッド new</span><span class="sxs-lookup"><span data-stu-id="72b7a-279">Method new</span></span>

<span data-ttu-id="72b7a-280">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="72b7a-280">Initializes a new instance of the TreeNode class.</span></span>

```xpp
public void new(str Name)
```

### <a name="parameters---new"></a><span data-ttu-id="72b7a-281">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="72b7a-281">Parameters - new</span></span>

<span data-ttu-id="72b7a-282">氏名</span><span class="sxs-lookup"><span data-stu-id="72b7a-282">Name</span></span>  

## <a name="method-addmenuitem"></a><span data-ttu-id="72b7a-283">メソッド addMenuitem</span><span class="sxs-lookup"><span data-stu-id="72b7a-283">Method addMenuitem</span></span>

```xpp
public void addMenuitem(WebMenuFunction webMenuFunction)
```

### <a name="parameters---addmenuitem"></a><span data-ttu-id="72b7a-284">パラメーター - addMenuitem</span><span class="sxs-lookup"><span data-stu-id="72b7a-284">Parameters - addMenuitem</span></span>

<span data-ttu-id="72b7a-285">webMenuFunction</span><span class="sxs-lookup"><span data-stu-id="72b7a-285">webMenuFunction</span></span>  

