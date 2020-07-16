---
title: Page クラス
description: このトピックでは、Page クラスについて説明します。
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
ms.openlocfilehash: 52354804795ee853738bea1e973a49942239192d
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502532"
---
# <a name="class-page"></a><span data-ttu-id="a906a-103">クラス ページ</span><span class="sxs-lookup"><span data-stu-id="a906a-103">Class Page</span></span>

[!include [banner](../../includes/banner.md)]


```xpp
class Page extends Object
```

<span data-ttu-id="a906a-104">このページ クラスでは、作成、読み取り、更新、および X++ コードおよびメタデータを削除できます。</span><span class="sxs-lookup"><span data-stu-id="a906a-104">This Page class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="a906a-105">備考</span><span class="sxs-lookup"><span data-stu-id="a906a-105">Remarks</span></span>

<span data-ttu-id="a906a-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a906a-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="a906a-107">例</span><span class="sxs-lookup"><span data-stu-id="a906a-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="a906a-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="a906a-108">Methods</span></span>

| <span data-ttu-id="a906a-109">方法</span><span class="sxs-lookup"><span data-stu-id="a906a-109">Method</span></span>                                                                        | <span data-ttu-id="a906a-110">説明</span><span class="sxs-lookup"><span data-stu-id="a906a-110">Description</span></span>                                                              |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="a906a-111">public boolean actionPaneControlEnabled(str controlName, \[boolean enabled\])</span><span class="sxs-lookup"><span data-stu-id="a906a-111">public boolean actionPaneControlEnabled(str controlName, \[boolean enabled\])</span></span> | <span data-ttu-id="a906a-112">アクション ウィンドウ上のコントロールの有効なプロパティの値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="a906a-112">Sets or gets the enabled property value of a control on the Action Pane.</span></span> |
| <span data-ttu-id="a906a-113">public boolean actionPaneControlVisible(str controlName, \[boolean visible\])</span><span class="sxs-lookup"><span data-stu-id="a906a-113">public boolean actionPaneControlVisible(str controlName, \[boolean visible\])</span></span> | <span data-ttu-id="a906a-114">アクション ウィンドウ上のコントロールの表示されるプロパティの値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="a906a-114">Sets or gets the visible property value of a control on the Action Pane.</span></span> |
| <span data-ttu-id="a906a-115">public Array activeActionPaneTabNames()</span><span class="sxs-lookup"><span data-stu-id="a906a-115">public Array activeActionPaneTabNames()</span></span>                                       |                                                                          |
| <span data-ttu-id="a906a-116">public Common activeRecord(str dataSourceName)</span><span class="sxs-lookup"><span data-stu-id="a906a-116">public Common activeRecord(str dataSourceName)</span></span>                                | <span data-ttu-id="a906a-117">特定のデータ ソース名の有効なレコードを取得します。</span><span class="sxs-lookup"><span data-stu-id="a906a-117">Gets the active record for the given data source name.</span></span>                   |
| <span data-ttu-id="a906a-118">public str name()</span><span class="sxs-lookup"><span data-stu-id="a906a-118">public str name()</span></span>                                                             | <span data-ttu-id="a906a-119">ページの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="a906a-119">Gets the name of the page.</span></span>                                               |
| <span data-ttu-id="a906a-120">public PageArgs pageArgs()</span><span class="sxs-lookup"><span data-stu-id="a906a-120">public PageArgs pageArgs()</span></span>                                                    | <span data-ttu-id="a906a-121">page 引数を取得します。</span><span class="sxs-lookup"><span data-stu-id="a906a-121">Gets the page arguments.</span></span>                                                 |
| <span data-ttu-id="a906a-122">public xFormRun formRun()</span><span class="sxs-lookup"><span data-stu-id="a906a-122">public xFormRun formRun()</span></span>                                                     |                                                                          |

## <a name="method-actionpanecontrolenabled"></a><span data-ttu-id="a906a-123">メソッド actionPaneControlEnabled</span><span class="sxs-lookup"><span data-stu-id="a906a-123">Method actionPaneControlEnabled</span></span>

<span data-ttu-id="a906a-124">アクション ウィンドウ上のコントロールの有効なプロパティの値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="a906a-124">Sets or gets the enabled property value of a control on the Action Pane.</span></span>

```xpp
public boolean actionPaneControlEnabled(str controlName, [boolean enabled])
```

### <a name="parameters---actionpanecontrolenabled"></a><span data-ttu-id="a906a-125">パラメーター - actionPaneControlEnabled</span><span class="sxs-lookup"><span data-stu-id="a906a-125">Parameters - actionPaneControlEnabled</span></span>

<span data-ttu-id="a906a-126">controlName</span><span class="sxs-lookup"><span data-stu-id="a906a-126">controlName</span></span>  
<span data-ttu-id="a906a-127">アクション ウィンドウ コントロールが有効かどうかを指定する値、オプション。</span><span class="sxs-lookup"><span data-stu-id="a906a-127">A value that specifies whether the Action Pane control is enabled; optional.</span></span>

<!-- -->

<span data-ttu-id="a906a-128">有効</span><span class="sxs-lookup"><span data-stu-id="a906a-128">enabled</span></span>  
<span data-ttu-id="a906a-129">アクション ウィンドウ コントロールが有効かどうかを指定する値、オプション。</span><span class="sxs-lookup"><span data-stu-id="a906a-129">A value that specifies whether the Action Pane control is enabled; optional.</span></span>

### <a name="return-value---actionpanecontrolenabled"></a><span data-ttu-id="a906a-130">戻り値 - actionPaneControlEnabled</span><span class="sxs-lookup"><span data-stu-id="a906a-130">Return Value - actionPaneControlEnabled</span></span>

<span data-ttu-id="a906a-131">アクション ペイン コントロールが有効かどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="a906a-131">A Boolean value that indicates whether the Action Pane control is enabled.</span></span>

## <a name="method-actionpanecontrolvisible"></a><span data-ttu-id="a906a-132">メソッド actionPaneControlVisible</span><span class="sxs-lookup"><span data-stu-id="a906a-132">Method actionPaneControlVisible</span></span>

<span data-ttu-id="a906a-133">アクション ウィンドウ上のコントロールの表示されるプロパティの値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="a906a-133">Sets or gets the visible property value of a control on the Action Pane.</span></span>

```xpp
public boolean actionPaneControlVisible(str controlName, [boolean visible])
```

### <a name="parameters---actionpanecontrolvisible"></a><span data-ttu-id="a906a-134">パラメーター - actionPaneControlVisible</span><span class="sxs-lookup"><span data-stu-id="a906a-134">Parameters - actionPaneControlVisible</span></span>

<span data-ttu-id="a906a-135">controlName</span><span class="sxs-lookup"><span data-stu-id="a906a-135">controlName</span></span>  
<span data-ttu-id="a906a-136">アクション ウィンドウ コントロールが表示されるかどうかを指定する値、オプション。</span><span class="sxs-lookup"><span data-stu-id="a906a-136">A value that specifies whether the Action Pane control is visible; optional.</span></span>

<!-- -->

<span data-ttu-id="a906a-137">表示</span><span class="sxs-lookup"><span data-stu-id="a906a-137">visible</span></span>  
<span data-ttu-id="a906a-138">アクション ウィンドウ コントロールが表示されるかどうかを指定する値、オプション。</span><span class="sxs-lookup"><span data-stu-id="a906a-138">A value that specifies whether the Action Pane control is visible; optional.</span></span>

### <a name="return-value---actionpanecontrolvisible"></a><span data-ttu-id="a906a-139">戻り値 - actionPaneControlVisible</span><span class="sxs-lookup"><span data-stu-id="a906a-139">Return Value - actionPaneControlVisible</span></span>

<span data-ttu-id="a906a-140">アクション ペイン コントロールが表示されるかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="a906a-140">A Boolean value that indicates whether the Action Pane control is visible.</span></span>

## <a name="method-activeactionpanetabnames"></a><span data-ttu-id="a906a-141">メソッド activeActionPaneTabNames</span><span class="sxs-lookup"><span data-stu-id="a906a-141">Method activeActionPaneTabNames</span></span>

```xpp
public Array activeActionPaneTabNames()
```

### <a name="return-value---activeactionpanetabnames"></a><span data-ttu-id="a906a-142">戻り値 - activeActionPaneTabNames</span><span class="sxs-lookup"><span data-stu-id="a906a-142">Return Value - activeActionPaneTabNames</span></span>

## <a name="method-activerecord"></a><span data-ttu-id="a906a-143">メソッド activeRecord</span><span class="sxs-lookup"><span data-stu-id="a906a-143">Method activeRecord</span></span>

<span data-ttu-id="a906a-144">特定のデータ ソース名の有効なレコードを取得します。</span><span class="sxs-lookup"><span data-stu-id="a906a-144">Gets the active record for the given data source name.</span></span>

```xpp
public Common activeRecord(str dataSourceName)
```

### <a name="parameters---activerecord"></a><span data-ttu-id="a906a-145">パラメーター - activeRecord</span><span class="sxs-lookup"><span data-stu-id="a906a-145">Parameters - activeRecord</span></span>

<span data-ttu-id="a906a-146">dataSourceName</span><span class="sxs-lookup"><span data-stu-id="a906a-146">dataSourceName</span></span>  
<span data-ttu-id="a906a-147">検索するデータ ソースの名前。</span><span class="sxs-lookup"><span data-stu-id="a906a-147">The name of the data source to search on.</span></span>

### <a name="return-value---activerecord"></a><span data-ttu-id="a906a-148">戻り値 - activeRecord</span><span class="sxs-lookup"><span data-stu-id="a906a-148">Return Value - activeRecord</span></span>

<span data-ttu-id="a906a-149">特定のデータ ソース用の有効なレコード。</span><span class="sxs-lookup"><span data-stu-id="a906a-149">The active record for the given data source.</span></span>

## <a name="method-name"></a><span data-ttu-id="a906a-150">メソッド名</span><span class="sxs-lookup"><span data-stu-id="a906a-150">Method name</span></span>

<span data-ttu-id="a906a-151">ページの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="a906a-151">Gets the name of the page.</span></span>

```xpp
public str name()
```

### <a name="return-value---name"></a><span data-ttu-id="a906a-152">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="a906a-152">Return Value - name</span></span>

<span data-ttu-id="a906a-153">ページ名。</span><span class="sxs-lookup"><span data-stu-id="a906a-153">The page name.</span></span>

## <a name="method-pageargs"></a><span data-ttu-id="a906a-154">メソッド pageArgs</span><span class="sxs-lookup"><span data-stu-id="a906a-154">Method pageArgs</span></span>

<span data-ttu-id="a906a-155">page 引数を取得します。</span><span class="sxs-lookup"><span data-stu-id="a906a-155">Gets the page arguments.</span></span>

```xpp
public PageArgs pageArgs()
```

### <a name="return-value---pageargs"></a><span data-ttu-id="a906a-156">戻り値 - pageArgs</span><span class="sxs-lookup"><span data-stu-id="a906a-156">Return Value - pageArgs</span></span>

<span data-ttu-id="a906a-157">page 引数。</span><span class="sxs-lookup"><span data-stu-id="a906a-157">The page arguments.</span></span>

## <a name="method-formrun"></a><span data-ttu-id="a906a-158">メソッド formRun</span><span class="sxs-lookup"><span data-stu-id="a906a-158">Method formRun</span></span>

```xpp
public xFormRun formRun()
```

### <a name="return-value---formrun"></a><span data-ttu-id="a906a-159">戻り値 - formRun</span><span class="sxs-lookup"><span data-stu-id="a906a-159">Return Value - formRun</span></span>

