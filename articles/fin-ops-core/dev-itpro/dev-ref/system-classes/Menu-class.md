---
title: Menu クラス
description: このトピックでは､Menu クラスについて説明します。
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
ms.openlocfilehash: aeeff8db3a02c8246550fa6f0a2a71c1f8bfc3ca
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502576"
---
# <a name="class-menu"></a><span data-ttu-id="593af-103">クラス メニュー</span><span class="sxs-lookup"><span data-stu-id="593af-103">Class Menu</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class Menu extends TreeNode
```

<span data-ttu-id="593af-104">メニュー システム クラスを使用すると、メニュー オブジェクトのいずれかをコードから構成および実行できます。</span><span class="sxs-lookup"><span data-stu-id="593af-104">The Menu system class lets you configure and run any of the menu objects from code.</span></span>

## <a name="remarks"></a><span data-ttu-id="593af-105">備考</span><span class="sxs-lookup"><span data-stu-id="593af-105">Remarks</span></span>

<span data-ttu-id="593af-106">TreeNode システム クラスは、アプリケーション オブジェクト ツリー (AOT) で、メニューへのより一般的なアプローチとして機能します。</span><span class="sxs-lookup"><span data-stu-id="593af-106">The TreeNode system class serves as a more general approach to the menus in the Application Object Tree (AOT).</span></span> <span data-ttu-id="593af-107">サブメニューやメニュー項目などのメニュー内容を作成または操作するには、Menu クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="593af-107">You use the Menu class to create or manipulate the menus contents, such as submenus and menu items.</span></span> <span data-ttu-id="593af-108">このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。</span><span class="sxs-lookup"><span data-stu-id="593af-108">This class lets you create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="593af-109">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="593af-109">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="593af-110">例</span><span class="sxs-lookup"><span data-stu-id="593af-110">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="593af-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="593af-111">Methods</span></span>

| <span data-ttu-id="593af-112">方法</span><span class="sxs-lookup"><span data-stu-id="593af-112">Method</span></span>                                                                   | <span data-ttu-id="593af-113">説明</span><span class="sxs-lookup"><span data-stu-id="593af-113">Description</span></span>                                                                                                               |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="593af-114">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="593af-114">public str changedBy(\[str value\])</span></span>                                      | <span data-ttu-id="593af-115">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="593af-115">Gets or sets the name of the user who last changed the application object.</span></span>                                                |
| <span data-ttu-id="593af-116">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="593af-116">public Date changedDate(\[Date value\])</span></span>                                  | <span data-ttu-id="593af-117">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="593af-117">Gets or sets the date an application object was last changed.</span></span>                                                             |
| <span data-ttu-id="593af-118">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="593af-118">public str changedTime(\[str value\])</span></span>                                    | <span data-ttu-id="593af-119">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="593af-119">Gets or sets the time an application object was last changed.</span></span>                                                             |
| <span data-ttu-id="593af-120">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="593af-120">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span> | <span data-ttu-id="593af-121">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="593af-121">Gets or sets the configuration key that is assigned to the control.</span></span>                                                       |
| <span data-ttu-id="593af-122">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="593af-122">public str countryRegionCodes(\[str value\])</span></span>                             |                                                                                                                           |
| <span data-ttu-id="593af-123">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="593af-123">public str createdBy(\[str value\])</span></span>                                      | <span data-ttu-id="593af-124">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="593af-124">Gets or sets the name of the user who created the application object.</span></span>                                                     |
| <span data-ttu-id="593af-125">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="593af-125">public Date creationDate(\[Date value\])</span></span>                                 | <span data-ttu-id="593af-126">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="593af-126">Gets or sets the date an application object was created.</span></span>                                                                  |
| <span data-ttu-id="593af-127">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="593af-127">public str creationTime(\[str value\])</span></span>                                   |                                                                                                                           |
| <span data-ttu-id="593af-128">public str disabledImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="593af-128">public str disabledImage(\[str value\])</span></span>                                  | <span data-ttu-id="593af-129">コントロールの無効な画像を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="593af-129">Gets or sets the disabled image of the button.</span></span>                                                                            |
| <span data-ttu-id="593af-130">public int disabledImageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="593af-130">public int disabledImageLocation(\[int value\])</span></span>                          |                                                                                                                           |
| <span data-ttu-id="593af-131">public int disabledResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="593af-131">public int disabledResource(\[int value\])</span></span>                               | <span data-ttu-id="593af-132">無効なボタン画像として使用する画像リソース ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="593af-132">Gets or sets the resource ID of the image to use as the disabled button image.</span></span>                                            |
| <span data-ttu-id="593af-133">public int imageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="593af-133">public int imageLocation(\[int value\])</span></span>                                  |                                                                                                                           |
| <span data-ttu-id="593af-134">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="593af-134">public str label(\[str value\])</span></span>                                          | <span data-ttu-id="593af-135">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="593af-135">Gets or sets the label for a control.</span></span>                                                                                     |
| <span data-ttu-id="593af-136">public str menuFunctionName(\[str name\])</span><span class="sxs-lookup"><span data-stu-id="593af-136">public str menuFunctionName(\[str name\])</span></span>                                |                                                                                                                           |
| <span data-ttu-id="593af-137">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="593af-137">public str menuItemName(\[str value\])</span></span>                                   |                                                                                                                           |
| <span data-ttu-id="593af-138">public MenuItemType menuItemType(\[MenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="593af-138">public MenuItemType menuItemType(\[MenuItemType value\])</span></span>                 |                                                                                                                           |
| <span data-ttu-id="593af-139">public str menuName()</span><span class="sxs-lookup"><span data-stu-id="593af-139">public str menuName()</span></span>                                                    |                                                                                                                           |
| <span data-ttu-id="593af-140">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="593af-140">public str name(\[str value\])</span></span>                                           | <span data-ttu-id="593af-141">フォーム、レポート、テーブル、クエリ、または別の MSDAX アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="593af-141">Gets or sets the name that is used in code to identify a form, report, table, query, or another MSDAX application object.</span></span> |
| <span data-ttu-id="593af-142">public int neededAccessLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="593af-142">public int neededAccessLevel(\[int value\])</span></span>                              | <span data-ttu-id="593af-143">MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="593af-143">Gets or sets the neededAccessLevel property for the MenuFunction class.</span></span>                                                   |
| <span data-ttu-id="593af-144">public str normalImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="593af-144">public str normalImage(\[str value\])</span></span>                                    |                                                                                                                           |
| <span data-ttu-id="593af-145">public int normalResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="593af-145">public int normalResource(\[int value\])</span></span>                                 |                                                                                                                           |
| <span data-ttu-id="593af-146">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="593af-146">public Guid origin(\[Guid value\])</span></span>                                       |                                                                                                                           |
| <span data-ttu-id="593af-147">public str parameter(\[str parameter\])</span><span class="sxs-lookup"><span data-stu-id="593af-147">public str parameter(\[str parameter\])</span></span>                                  |                                                                                                                           |
| <span data-ttu-id="593af-148">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="593af-148">public str parameters(\[str value\])</span></span>                                     | <span data-ttu-id="593af-149">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="593af-149">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>                    |
| <span data-ttu-id="593af-150">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="593af-150">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                |                                                                                                                           |
| <span data-ttu-id="593af-151">public boolean setCompany(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="593af-151">public boolean setCompany(\[boolean value\])</span></span>                             |                                                                                                                           |
| <span data-ttu-id="593af-152">public str shortCut(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="593af-152">public str shortCut(\[str value\])</span></span>                                       |                                                                                                                           |
| <span data-ttu-id="593af-153">public boolean showParentModule(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="593af-153">public boolean showParentModule(\[boolean value\])</span></span>                       |                                                                                                                           |
| <span data-ttu-id="593af-154">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="593af-154">public boolean visible(\[boolean value\])</span></span>                                |                                                                                                                           |
| <span data-ttu-id="593af-155">public str webTarget(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="593af-155">public str webTarget(\[str value\])</span></span>                                      |                                                                                                                           |
| <span data-ttu-id="593af-156">public void save()</span><span class="sxs-lookup"><span data-stu-id="593af-156">public void save()</span></span>                                                       |                                                                                                                           |
| <span data-ttu-id="593af-157">public void new(str Name)</span><span class="sxs-lookup"><span data-stu-id="593af-157">public void new(str Name)</span></span>                                                | <span data-ttu-id="593af-158">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="593af-158">Initializes a new instance of the TreeNode class.</span></span>                                                                         |
| <span data-ttu-id="593af-159">public void makeWebMenu(Object outputClass)</span><span class="sxs-lookup"><span data-stu-id="593af-159">public void makeWebMenu(Object outputClass)</span></span>                              |                                                                                                                           |
| <span data-ttu-id="593af-160">public void addMenuitem(xMenuFunction menuFunction)</span><span class="sxs-lookup"><span data-stu-id="593af-160">public void addMenuitem(xMenuFunction menuFunction)</span></span>                      | <span data-ttu-id="593af-161">メニューにメニュー項目を追加します。</span><span class="sxs-lookup"><span data-stu-id="593af-161">Adds a menu item to the menu.</span></span>                                                                                             |
| <span data-ttu-id="593af-162">public void setTreeNodeName(str name)</span><span class="sxs-lookup"><span data-stu-id="593af-162">public void setTreeNodeName(str name)</span></span>                                    |                                                                                                                           |
| <span data-ttu-id="593af-163">public void addMenuReference(Menu menu)</span><span class="sxs-lookup"><span data-stu-id="593af-163">public void addMenuReference(Menu menu)</span></span>                                  |                                                                                                                           |
| <span data-ttu-id="593af-164">public void addSubmenu(str name)</span><span class="sxs-lookup"><span data-stu-id="593af-164">public void addSubmenu(str name)</span></span>                                         | <span data-ttu-id="593af-165">メニューにサブメニューを追加します。</span><span class="sxs-lookup"><span data-stu-id="593af-165">Adds a submenu to the menu.</span></span>                                                                                               |
| <span data-ttu-id="593af-166">public void addSeparator()</span><span class="sxs-lookup"><span data-stu-id="593af-166">public void addSeparator()</span></span>                                               | <span data-ttu-id="593af-167">メニューにメニューの区切りを追加します。</span><span class="sxs-lookup"><span data-stu-id="593af-167">Adds a menu separator to the menu.</span></span>                                                                                        |

## <a name="method-changedby"></a><span data-ttu-id="593af-168">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="593af-168">Method changedBy</span></span>

<span data-ttu-id="593af-169">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="593af-169">Gets or sets the name of the user who last changed the application object.</span></span>

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a><span data-ttu-id="593af-170">パラメーター - changedBy</span><span class="sxs-lookup"><span data-stu-id="593af-170">Parameters - changedBy</span></span>

<span data-ttu-id="593af-171">値</span><span class="sxs-lookup"><span data-stu-id="593af-171">value</span></span>  

### <a name="return-value---changedby"></a><span data-ttu-id="593af-172">戻り値 - changedBy</span><span class="sxs-lookup"><span data-stu-id="593af-172">Return Value - changedBy</span></span>

<span data-ttu-id="593af-173">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="593af-173">The name of the user.</span></span>

## <a name="method-changeddate"></a><span data-ttu-id="593af-174">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="593af-174">Method changedDate</span></span>

<span data-ttu-id="593af-175">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="593af-175">Gets or sets the date an application object was last changed.</span></span>

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a><span data-ttu-id="593af-176">パラメーター - changedDate</span><span class="sxs-lookup"><span data-stu-id="593af-176">Parameters - changedDate</span></span>

<span data-ttu-id="593af-177">値</span><span class="sxs-lookup"><span data-stu-id="593af-177">value</span></span>  

### <a name="return-value---changeddate"></a><span data-ttu-id="593af-178">戻り値 - changedDate</span><span class="sxs-lookup"><span data-stu-id="593af-178">Return Value - changedDate</span></span>

<span data-ttu-id="593af-179">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="593af-179">The date an application object was last changed.</span></span>

## <a name="method-changedtime"></a><span data-ttu-id="593af-180">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="593af-180">Method changedTime</span></span>

<span data-ttu-id="593af-181">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="593af-181">Gets or sets the time an application object was last changed.</span></span>

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a><span data-ttu-id="593af-182">パラメーター - changedTime</span><span class="sxs-lookup"><span data-stu-id="593af-182">Parameters - changedTime</span></span>

<span data-ttu-id="593af-183">値</span><span class="sxs-lookup"><span data-stu-id="593af-183">value</span></span>  

### <a name="return-value---changedtime"></a><span data-ttu-id="593af-184">戻り値 - changedTime</span><span class="sxs-lookup"><span data-stu-id="593af-184">Return Value - changedTime</span></span>

<span data-ttu-id="593af-185">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="593af-185">The time an application object was last changed.</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="593af-186">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="593af-186">Method configurationKey</span></span>

<span data-ttu-id="593af-187">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="593af-187">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="593af-188">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="593af-188">Parameters - configurationKey</span></span>

<span data-ttu-id="593af-189">値</span><span class="sxs-lookup"><span data-stu-id="593af-189">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="593af-190">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="593af-190">Return Value - configurationKey</span></span>

<span data-ttu-id="593af-191">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="593af-191">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="593af-192">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="593af-192">Remarks - configurationKey</span></span>

<span data-ttu-id="593af-193">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="593af-193">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="593af-194">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="593af-194">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="593af-195">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="593af-195">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="593af-196">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="593af-196">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="593af-197">値</span><span class="sxs-lookup"><span data-stu-id="593af-197">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="593af-198">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="593af-198">Return Value - countryRegionCodes</span></span>

## <a name="method-createdby"></a><span data-ttu-id="593af-199">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="593af-199">Method createdBy</span></span>

<span data-ttu-id="593af-200">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="593af-200">Gets or sets the name of the user who created the application object.</span></span>

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a><span data-ttu-id="593af-201">パラメーター - createdBy</span><span class="sxs-lookup"><span data-stu-id="593af-201">Parameters - createdBy</span></span>

<span data-ttu-id="593af-202">値</span><span class="sxs-lookup"><span data-stu-id="593af-202">value</span></span>  

### <a name="return-value---createdby"></a><span data-ttu-id="593af-203">戻り値 - createdBy</span><span class="sxs-lookup"><span data-stu-id="593af-203">Return Value - createdBy</span></span>

<span data-ttu-id="593af-204">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="593af-204">The name of the user.</span></span>

## <a name="method-creationdate"></a><span data-ttu-id="593af-205">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="593af-205">Method creationDate</span></span>

<span data-ttu-id="593af-206">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="593af-206">Gets or sets the date an application object was created.</span></span>

```xpp
public Date creationDate([Date value])
```

### <a name="parameters---creationdate"></a><span data-ttu-id="593af-207">パラメーター - creationDate</span><span class="sxs-lookup"><span data-stu-id="593af-207">Parameters - creationDate</span></span>

<span data-ttu-id="593af-208">値</span><span class="sxs-lookup"><span data-stu-id="593af-208">value</span></span>  

### <a name="return-value---creationdate"></a><span data-ttu-id="593af-209">戻り値 - creationDate</span><span class="sxs-lookup"><span data-stu-id="593af-209">Return Value - creationDate</span></span>

<span data-ttu-id="593af-210">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="593af-210">The date an application object was created.</span></span>

## <a name="method-creationtime"></a><span data-ttu-id="593af-211">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="593af-211">Method creationTime</span></span>

```xpp
public str creationTime([str value])
```

### <a name="parameters---creationtime"></a><span data-ttu-id="593af-212">パラメーター - creationTime</span><span class="sxs-lookup"><span data-stu-id="593af-212">Parameters - creationTime</span></span>

<span data-ttu-id="593af-213">値</span><span class="sxs-lookup"><span data-stu-id="593af-213">value</span></span>  

### <a name="return-value---creationtime"></a><span data-ttu-id="593af-214">戻り値 - creationTime</span><span class="sxs-lookup"><span data-stu-id="593af-214">Return Value - creationTime</span></span>

## <a name="method-disabledimage"></a><span data-ttu-id="593af-215">メソッド disabledImage</span><span class="sxs-lookup"><span data-stu-id="593af-215">Method disabledImage</span></span>

<span data-ttu-id="593af-216">コントロールの無効な画像を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="593af-216">Gets or sets the disabled image of the button.</span></span>

```xpp
public str disabledImage([str value])
```

### <a name="parameters---disabledimage"></a><span data-ttu-id="593af-217">パラメーター - disabledImage</span><span class="sxs-lookup"><span data-stu-id="593af-217">Parameters - disabledImage</span></span>

<span data-ttu-id="593af-218">値</span><span class="sxs-lookup"><span data-stu-id="593af-218">value</span></span>  

### <a name="return-value---disabledimage"></a><span data-ttu-id="593af-219">戻り値 - disabledImage</span><span class="sxs-lookup"><span data-stu-id="593af-219">Return Value - disabledImage</span></span>

<span data-ttu-id="593af-220">画像ファイルのフル ネーム。</span><span class="sxs-lookup"><span data-stu-id="593af-220">The full name of an image file.</span></span> <span data-ttu-id="593af-221">システムは、GDI でサポートされているすべてのイメージ形式をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="593af-221">The system supports all of the GDI-supported image formats.</span></span>

### <a name="remarks---disabledimage"></a><span data-ttu-id="593af-222">備考 - disabledImage</span><span class="sxs-lookup"><span data-stu-id="593af-222">Remarks - disabledImage</span></span>

<span data-ttu-id="593af-223">このプロパティは、disabledResource プロパティに優先します。</span><span class="sxs-lookup"><span data-stu-id="593af-223">This property has precedence over the disabledResource property .</span></span> <span data-ttu-id="593af-224">これらのプロパティの両方が設定されている場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="593af-224">It is used if both of these properties are set.</span></span>

## <a name="method-disabledimagelocation"></a><span data-ttu-id="593af-225">メソッド disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="593af-225">Method disabledImageLocation</span></span>

```xpp
public int disabledImageLocation([int value])
```

### <a name="parameters---disabledimagelocation"></a><span data-ttu-id="593af-226">パラメーター - disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="593af-226">Parameters - disabledImageLocation</span></span>

<span data-ttu-id="593af-227">値</span><span class="sxs-lookup"><span data-stu-id="593af-227">value</span></span>  

### <a name="return-value---disabledimagelocation"></a><span data-ttu-id="593af-228">戻り値 - disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="593af-228">Return Value - disabledImageLocation</span></span>

## <a name="method-disabledresource"></a><span data-ttu-id="593af-229">メソッド disabledResource</span><span class="sxs-lookup"><span data-stu-id="593af-229">Method disabledResource</span></span>

<span data-ttu-id="593af-230">無効なボタン画像として使用する画像リソース ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="593af-230">Gets or sets the resource ID of the image to use as the disabled button image.</span></span>

```xpp
public int disabledResource([int value])
```

### <a name="parameters---disabledresource"></a><span data-ttu-id="593af-231">パラメーター - disabledResource</span><span class="sxs-lookup"><span data-stu-id="593af-231">Parameters - disabledResource</span></span>

<span data-ttu-id="593af-232">値</span><span class="sxs-lookup"><span data-stu-id="593af-232">value</span></span>  

### <a name="return-value---disabledresource"></a><span data-ttu-id="593af-233">戻り値 - disabledResource</span><span class="sxs-lookup"><span data-stu-id="593af-233">Return Value - disabledResource</span></span>

<span data-ttu-id="593af-234">無効なボタン画像として使用する画像リソース ID。</span><span class="sxs-lookup"><span data-stu-id="593af-234">The resource ID of the image to use as the disabled button image.</span></span> <span data-ttu-id="593af-235">アイコンとビットマップ イメージの両方がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="593af-235">Both icon and bitmap images are supported.</span></span>

## <a name="method-imagelocation"></a><span data-ttu-id="593af-236">メソッド imageLocation</span><span class="sxs-lookup"><span data-stu-id="593af-236">Method imageLocation</span></span>

```xpp
public int imageLocation([int value])
```

### <a name="parameters---imagelocation"></a><span data-ttu-id="593af-237">パラメーター - imageLocation</span><span class="sxs-lookup"><span data-stu-id="593af-237">Parameters - imageLocation</span></span>

<span data-ttu-id="593af-238">値</span><span class="sxs-lookup"><span data-stu-id="593af-238">value</span></span>  

### <a name="return-value---imagelocation"></a><span data-ttu-id="593af-239">戻り値 - imageLocation</span><span class="sxs-lookup"><span data-stu-id="593af-239">Return Value - imageLocation</span></span>

## <a name="method-label"></a><span data-ttu-id="593af-240">メソッド label</span><span class="sxs-lookup"><span data-stu-id="593af-240">Method label</span></span>

<span data-ttu-id="593af-241">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="593af-241">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="593af-242">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="593af-242">Parameters - label</span></span>

<span data-ttu-id="593af-243">値</span><span class="sxs-lookup"><span data-stu-id="593af-243">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="593af-244">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="593af-244">Return Value - label</span></span>

<span data-ttu-id="593af-245">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="593af-245">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="593af-246">備考 - label</span><span class="sxs-lookup"><span data-stu-id="593af-246">Remarks - label</span></span>

<span data-ttu-id="593af-247">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="593af-247">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="593af-248">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="593af-248">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-menufunctionname"></a><span data-ttu-id="593af-249">メソッド menuFunctionName</span><span class="sxs-lookup"><span data-stu-id="593af-249">Method menuFunctionName</span></span>

```xpp
public str menuFunctionName([str name])
```

### <a name="parameters---menufunctionname"></a><span data-ttu-id="593af-250">パラメーター - menuFunctionName</span><span class="sxs-lookup"><span data-stu-id="593af-250">Parameters - menuFunctionName</span></span>

<span data-ttu-id="593af-251">名前</span><span class="sxs-lookup"><span data-stu-id="593af-251">name</span></span>  

### <a name="return-value---menufunctionname"></a><span data-ttu-id="593af-252">戻り値 - menuFunctionName</span><span class="sxs-lookup"><span data-stu-id="593af-252">Return Value - menuFunctionName</span></span>

## <a name="method-menuitemname"></a><span data-ttu-id="593af-253">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="593af-253">Method menuItemName</span></span>

```xpp
public str menuItemName([str value])
```

### <a name="parameters---menuitemname"></a><span data-ttu-id="593af-254">パラメーター - menuItemName</span><span class="sxs-lookup"><span data-stu-id="593af-254">Parameters - menuItemName</span></span>

<span data-ttu-id="593af-255">値</span><span class="sxs-lookup"><span data-stu-id="593af-255">value</span></span>  

### <a name="return-value---menuitemname"></a><span data-ttu-id="593af-256">戻り値 - menuItemName</span><span class="sxs-lookup"><span data-stu-id="593af-256">Return Value - menuItemName</span></span>

## <a name="method-menuitemtype"></a><span data-ttu-id="593af-257">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="593af-257">Method menuItemType</span></span>

```xpp
public MenuItemType menuItemType([MenuItemType value])
```

### <a name="parameters---menuitemtype"></a><span data-ttu-id="593af-258">パラメーター - menuItemType</span><span class="sxs-lookup"><span data-stu-id="593af-258">Parameters - menuItemType</span></span>

<span data-ttu-id="593af-259">値</span><span class="sxs-lookup"><span data-stu-id="593af-259">value</span></span>  

### <a name="return-value---menuitemtype"></a><span data-ttu-id="593af-260">戻り値 - menuItemType</span><span class="sxs-lookup"><span data-stu-id="593af-260">Return Value - menuItemType</span></span>

## <a name="method-menuname"></a><span data-ttu-id="593af-261">メソッド menuName</span><span class="sxs-lookup"><span data-stu-id="593af-261">Method menuName</span></span>

```xpp
public str menuName()
```

### <a name="return-value---menuname"></a><span data-ttu-id="593af-262">戻り値 - menuName</span><span class="sxs-lookup"><span data-stu-id="593af-262">Return Value - menuName</span></span>

## <a name="method-name"></a><span data-ttu-id="593af-263">メソッド名</span><span class="sxs-lookup"><span data-stu-id="593af-263">Method name</span></span>

<span data-ttu-id="593af-264">フォーム、レポート、テーブル、クエリ、または別の MSDAX アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="593af-264">Gets or sets the name that is used in code to identify a form, report, table, query, or another MSDAX application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="593af-265">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="593af-265">Parameters - name</span></span>

<span data-ttu-id="593af-266">値</span><span class="sxs-lookup"><span data-stu-id="593af-266">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="593af-267">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="593af-267">Return Value - name</span></span>

<span data-ttu-id="593af-268">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="593af-268">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="593af-269">備考 - name</span><span class="sxs-lookup"><span data-stu-id="593af-269">Remarks - name</span></span>

<span data-ttu-id="593af-270">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="593af-270">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="593af-271">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="593af-271">Begins with a letter.</span></span>
-   <span data-ttu-id="593af-272">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="593af-272">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="593af-273">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="593af-273">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="593af-274">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="593af-274">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="593af-275">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="593af-275">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-neededaccesslevel"></a><span data-ttu-id="593af-276">メソッド neededAccessLevel</span><span class="sxs-lookup"><span data-stu-id="593af-276">Method neededAccessLevel</span></span>

<span data-ttu-id="593af-277">MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="593af-277">Gets or sets the neededAccessLevel property for the MenuFunction class.</span></span>

```xpp
public int neededAccessLevel([int value])
```

### <a name="parameters---neededaccesslevel"></a><span data-ttu-id="593af-278">パラメーター - neededAccessLevel</span><span class="sxs-lookup"><span data-stu-id="593af-278">Parameters - neededAccessLevel</span></span>

<span data-ttu-id="593af-279">値</span><span class="sxs-lookup"><span data-stu-id="593af-279">value</span></span>  

### <a name="return-value---neededaccesslevel"></a><span data-ttu-id="593af-280">戻り値 - neededAccessLevel</span><span class="sxs-lookup"><span data-stu-id="593af-280">Return Value - neededAccessLevel</span></span>

<span data-ttu-id="593af-281">neededAccessLevel プロパティの現在の値。</span><span class="sxs-lookup"><span data-stu-id="593af-281">The current value of the neededAccessLevel property.</span></span>

### <a name="remarks---neededaccesslevel"></a><span data-ttu-id="593af-282">備考 - neededAccessLevel</span><span class="sxs-lookup"><span data-stu-id="593af-282">Remarks - neededAccessLevel</span></span>

<span data-ttu-id="593af-283">AccessType システム列挙値の使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="593af-283">The possible values for the AccessType system enumeration value are as follows:</span></span>

-   <span data-ttu-id="593af-284">AccessType::NoAccess。</span><span class="sxs-lookup"><span data-stu-id="593af-284">AccessType::NoAccess.</span></span>
-   <span data-ttu-id="593af-285">AccessType::View。</span><span class="sxs-lookup"><span data-stu-id="593af-285">AccessType::View.</span></span>
-   <span data-ttu-id="593af-286">AccessType::Edit。</span><span class="sxs-lookup"><span data-stu-id="593af-286">AccessType::Edit.</span></span>
-   <span data-ttu-id="593af-287">AccessType::Add。</span><span class="sxs-lookup"><span data-stu-id="593af-287">AccessType::Add.</span></span>
-   <span data-ttu-id="593af-288">AccessType::Delete。</span><span class="sxs-lookup"><span data-stu-id="593af-288">AccessType::Delete.</span></span>

## <a name="method-normalimage"></a><span data-ttu-id="593af-289">メソッド normalImage</span><span class="sxs-lookup"><span data-stu-id="593af-289">Method normalImage</span></span>

```xpp
public str normalImage([str value])
```

### <a name="parameters---normalimage"></a><span data-ttu-id="593af-290">パラメーター - normalImage</span><span class="sxs-lookup"><span data-stu-id="593af-290">Parameters - normalImage</span></span>

<span data-ttu-id="593af-291">値</span><span class="sxs-lookup"><span data-stu-id="593af-291">value</span></span>  

### <a name="return-value---normalimage"></a><span data-ttu-id="593af-292">戻り値 - normalImage</span><span class="sxs-lookup"><span data-stu-id="593af-292">Return Value - normalImage</span></span>

## <a name="method-normalresource"></a><span data-ttu-id="593af-293">メソッド normalResource</span><span class="sxs-lookup"><span data-stu-id="593af-293">Method normalResource</span></span>

```xpp
public int normalResource([int value])
```

### <a name="parameters---normalresource"></a><span data-ttu-id="593af-294">パラメーター - normalResource</span><span class="sxs-lookup"><span data-stu-id="593af-294">Parameters - normalResource</span></span>

<span data-ttu-id="593af-295">値</span><span class="sxs-lookup"><span data-stu-id="593af-295">value</span></span>  

### <a name="return-value---normalresource"></a><span data-ttu-id="593af-296">戻り値 - normalResource</span><span class="sxs-lookup"><span data-stu-id="593af-296">Return Value - normalResource</span></span>

## <a name="method-origin"></a><span data-ttu-id="593af-297">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="593af-297">Method origin</span></span>

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a><span data-ttu-id="593af-298">パラメーター - origin</span><span class="sxs-lookup"><span data-stu-id="593af-298">Parameters - origin</span></span>

<span data-ttu-id="593af-299">値</span><span class="sxs-lookup"><span data-stu-id="593af-299">value</span></span>  

### <a name="return-value---origin"></a><span data-ttu-id="593af-300">戻り値 - origin</span><span class="sxs-lookup"><span data-stu-id="593af-300">Return Value - origin</span></span>

## <a name="method-parameter"></a><span data-ttu-id="593af-301">メソッド parameter</span><span class="sxs-lookup"><span data-stu-id="593af-301">Method parameter</span></span>

```xpp
public str parameter([str parameter])
```

### <a name="parameters---parameter"></a><span data-ttu-id="593af-302">パラメーター - parameter</span><span class="sxs-lookup"><span data-stu-id="593af-302">Parameters - parameter</span></span>

<span data-ttu-id="593af-303">パラメーター</span><span class="sxs-lookup"><span data-stu-id="593af-303">parameter</span></span>  

### <a name="return-value---parameter"></a><span data-ttu-id="593af-304">戻り値 - パラメータ</span><span class="sxs-lookup"><span data-stu-id="593af-304">Return Value - parameter</span></span>

## <a name="method-parameters"></a><span data-ttu-id="593af-305">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="593af-305">Method parameters</span></span>

<span data-ttu-id="593af-306">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="593af-306">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

```xpp
public str parameters([str value])
```

### <a name="parameters---parameters"></a><span data-ttu-id="593af-307">パラメーター - parameters</span><span class="sxs-lookup"><span data-stu-id="593af-307">Parameters - parameters</span></span>

<span data-ttu-id="593af-308">値</span><span class="sxs-lookup"><span data-stu-id="593af-308">value</span></span>  

### <a name="return-value---parameters"></a><span data-ttu-id="593af-309">戻り値 - parameters</span><span class="sxs-lookup"><span data-stu-id="593af-309">Return Value - parameters</span></span>

<span data-ttu-id="593af-310">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="593af-310">The list of parameters that are passed to the object.</span></span>

### <a name="remarks---parameters"></a><span data-ttu-id="593af-311">備考 - parameters</span><span class="sxs-lookup"><span data-stu-id="593af-311">Remarks - parameters</span></span>

<span data-ttu-id="593af-312">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="593af-312">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="593af-313">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="593af-313">Objects ignore passed, unrecognized parameters.</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="593af-314">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="593af-314">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="593af-315">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="593af-315">Parameters - securityKey</span></span>

<span data-ttu-id="593af-316">値</span><span class="sxs-lookup"><span data-stu-id="593af-316">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="593af-317">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="593af-317">Return Value - securityKey</span></span>

## <a name="method-setcompany"></a><span data-ttu-id="593af-318">メソッド setCompany</span><span class="sxs-lookup"><span data-stu-id="593af-318">Method setCompany</span></span>

```xpp
public boolean setCompany([boolean value])
```

### <a name="parameters---setcompany"></a><span data-ttu-id="593af-319">パラメーター - setCompany</span><span class="sxs-lookup"><span data-stu-id="593af-319">Parameters - setCompany</span></span>

<span data-ttu-id="593af-320">値</span><span class="sxs-lookup"><span data-stu-id="593af-320">value</span></span>  

### <a name="return-value---setcompany"></a><span data-ttu-id="593af-321">戻り値 - setCompany</span><span class="sxs-lookup"><span data-stu-id="593af-321">Return Value - setCompany</span></span>

## <a name="method-shortcut"></a><span data-ttu-id="593af-322">メソッド shortCut</span><span class="sxs-lookup"><span data-stu-id="593af-322">Method shortCut</span></span>

```xpp
public str shortCut([str value])
```

### <a name="parameters---shortcut"></a><span data-ttu-id="593af-323">パラメーター - shortCut </span><span class="sxs-lookup"><span data-stu-id="593af-323">Parameters - shortCut</span></span>

<span data-ttu-id="593af-324">値</span><span class="sxs-lookup"><span data-stu-id="593af-324">value</span></span>  

### <a name="return-value---shortcut"></a><span data-ttu-id="593af-325">戻り値 - shortCut</span><span class="sxs-lookup"><span data-stu-id="593af-325">Return Value - shortCut</span></span>

## <a name="method-showparentmodule"></a><span data-ttu-id="593af-326">メソッド showParentModule</span><span class="sxs-lookup"><span data-stu-id="593af-326">Method showParentModule</span></span>

```xpp
public boolean showParentModule([boolean value])
```

### <a name="parameters---showparentmodule"></a><span data-ttu-id="593af-327">パラメーター - showParentModule</span><span class="sxs-lookup"><span data-stu-id="593af-327">Parameters - showParentModule</span></span>

<span data-ttu-id="593af-328">値</span><span class="sxs-lookup"><span data-stu-id="593af-328">value</span></span>  

### <a name="return-value---showparentmodule"></a><span data-ttu-id="593af-329">戻り値 - showParentModule</span><span class="sxs-lookup"><span data-stu-id="593af-329">Return Value - showParentModule</span></span>

## <a name="method-visible"></a><span data-ttu-id="593af-330">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="593af-330">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="593af-331">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="593af-331">Parameters - visible</span></span>

<span data-ttu-id="593af-332">値</span><span class="sxs-lookup"><span data-stu-id="593af-332">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="593af-333">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="593af-333">Return Value - visible</span></span>

## <a name="method-webtarget"></a><span data-ttu-id="593af-334">メソッド webTarget</span><span class="sxs-lookup"><span data-stu-id="593af-334">Method webTarget</span></span>

```xpp
public str webTarget([str value])
```

### <a name="parameters---webtarget"></a><span data-ttu-id="593af-335">パラメーター - webTarget</span><span class="sxs-lookup"><span data-stu-id="593af-335">Parameters - webTarget</span></span>

<span data-ttu-id="593af-336">値</span><span class="sxs-lookup"><span data-stu-id="593af-336">value</span></span>  

### <a name="return-value---webtarget"></a><span data-ttu-id="593af-337">戻り値 - webTarget</span><span class="sxs-lookup"><span data-stu-id="593af-337">Return Value - webTarget</span></span>

## <a name="method-save"></a><span data-ttu-id="593af-338">メソッド save</span><span class="sxs-lookup"><span data-stu-id="593af-338">Method save</span></span>

```xpp
public void save()
```

## <a name="method-new"></a><span data-ttu-id="593af-339">メソッド new</span><span class="sxs-lookup"><span data-stu-id="593af-339">Method new</span></span>

<span data-ttu-id="593af-340">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="593af-340">Initializes a new instance of the TreeNode class.</span></span>

```xpp
public void new(str Name)
```

### <a name="parameters---new"></a><span data-ttu-id="593af-341">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="593af-341">Parameters - new</span></span>

<span data-ttu-id="593af-342">氏名</span><span class="sxs-lookup"><span data-stu-id="593af-342">Name</span></span>  

## <a name="method-makewebmenu"></a><span data-ttu-id="593af-343">メソッド makeWebMenu</span><span class="sxs-lookup"><span data-stu-id="593af-343">Method makeWebMenu</span></span>

```xpp
public void makeWebMenu(Object outputClass)
```

### <a name="parameters---makewebmenu"></a><span data-ttu-id="593af-344">パラメーター - makeWebMenu</span><span class="sxs-lookup"><span data-stu-id="593af-344">Parameters - makeWebMenu</span></span>

<span data-ttu-id="593af-345">outputClass</span><span class="sxs-lookup"><span data-stu-id="593af-345">outputClass</span></span>  

## <a name="method-addmenuitem"></a><span data-ttu-id="593af-346">メソッド addMenuitem</span><span class="sxs-lookup"><span data-stu-id="593af-346">Method addMenuitem</span></span>

<span data-ttu-id="593af-347">メニューにメニュー項目を追加します。</span><span class="sxs-lookup"><span data-stu-id="593af-347">Adds a menu item to the menu.</span></span>

```xpp
public void addMenuitem(xMenuFunction menuFunction)
```

### <a name="parameters---addmenuitem"></a><span data-ttu-id="593af-348">パラメーター - addMenuitem</span><span class="sxs-lookup"><span data-stu-id="593af-348">Parameters - addMenuitem</span></span>

<span data-ttu-id="593af-349">menuFunction</span><span class="sxs-lookup"><span data-stu-id="593af-349">menuFunction</span></span>  
<span data-ttu-id="593af-350">追加するメニュー項目。</span><span class="sxs-lookup"><span data-stu-id="593af-350">The menu item to add.</span></span>

## <a name="method-settreenodename"></a><span data-ttu-id="593af-351">メソッド setTreeNodeName</span><span class="sxs-lookup"><span data-stu-id="593af-351">Method setTreeNodeName</span></span>

```xpp
public void setTreeNodeName(str name)
```

### <a name="parameters---settreenodename"></a><span data-ttu-id="593af-352">パラメーター - setTreeNodeName</span><span class="sxs-lookup"><span data-stu-id="593af-352">Parameters - setTreeNodeName</span></span>

<span data-ttu-id="593af-353">名前</span><span class="sxs-lookup"><span data-stu-id="593af-353">name</span></span>  

## <a name="method-addmenureference"></a><span data-ttu-id="593af-354">メソッド addMenuReference</span><span class="sxs-lookup"><span data-stu-id="593af-354">Method addMenuReference</span></span>

```xpp
public void addMenuReference(Menu menu)
```

### <a name="parameters---addmenureference"></a><span data-ttu-id="593af-355">パラメーター - addMenuReference</span><span class="sxs-lookup"><span data-stu-id="593af-355">Parameters - addMenuReference</span></span>

<span data-ttu-id="593af-356">メニュー</span><span class="sxs-lookup"><span data-stu-id="593af-356">menu</span></span>  

## <a name="method-addsubmenu"></a><span data-ttu-id="593af-357">メソッド addSubmenu</span><span class="sxs-lookup"><span data-stu-id="593af-357">Method addSubmenu</span></span>

<span data-ttu-id="593af-358">メニューにサブメニューを追加します。</span><span class="sxs-lookup"><span data-stu-id="593af-358">Adds a submenu to the menu.</span></span>

```xpp
public void addSubmenu(str name)
```

### <a name="parameters---addsubmenu"></a><span data-ttu-id="593af-359">パラメーター - addSubmenu</span><span class="sxs-lookup"><span data-stu-id="593af-359">Parameters - addSubmenu</span></span>

<span data-ttu-id="593af-360">名前</span><span class="sxs-lookup"><span data-stu-id="593af-360">name</span></span>  
<span data-ttu-id="593af-361">メニューに追加するサブメニューの名前に評価される文字列式。</span><span class="sxs-lookup"><span data-stu-id="593af-361">A string expression that evaluates to the name of the submenu to add to the menu.</span></span>

## <a name="method-addseparator"></a><span data-ttu-id="593af-362">メソッド addSeparator</span><span class="sxs-lookup"><span data-stu-id="593af-362">Method addSeparator</span></span>

<span data-ttu-id="593af-363">メニューにメニューの区切りを追加します。</span><span class="sxs-lookup"><span data-stu-id="593af-363">Adds a menu separator to the menu.</span></span>

```xpp
public void addSeparator()
```

