---
title: ProjectNode クラス
description: このトピックでは、ProjectNode クラスについて説明します。
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
ms.openlocfilehash: 664126a7be58f23dab115dde8de5932f1284cfe9
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502872"
---
# <a name="class-projectnode"></a><span data-ttu-id="54ea1-103">クラス ProjectNode</span><span class="sxs-lookup"><span data-stu-id="54ea1-103">Class ProjectNode</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ProjectNode extends TreeNode
```

<span data-ttu-id="54ea1-104">ProjectNode クラスは、AOT プロジェクトの動作を制御します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-104">The ProjectNode class controls the behavior of an AOT project.</span></span>

## <a name="remarks"></a><span data-ttu-id="54ea1-105">備考</span><span class="sxs-lookup"><span data-stu-id="54ea1-105">Remarks</span></span>

<span data-ttu-id="54ea1-106">このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="54ea1-106">This class enables you to create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="54ea1-107">このクラスから拡張して、新しいユーザー定義の AOT プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-107">Create a new, user-defined AOT project by extending from this class.</span></span> <span data-ttu-id="54ea1-108">このクラスのメソッドを上書きすることによって、プロジェクトの動作を制御します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-108">Control the behavior of the project by overriding the methods of this class.</span></span> <span data-ttu-id="54ea1-109">Web プロジェクトとヘルプ プロジェクトの両方を作成するには、ProjectNode クラスを拡張するクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-109">Create both Web projects and Help projects by creating classes that extend the ProjectNode class.</span></span>

## <a name="examples"></a><span data-ttu-id="54ea1-110">例</span><span class="sxs-lookup"><span data-stu-id="54ea1-110">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="54ea1-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="54ea1-111">Methods</span></span>

| <span data-ttu-id="54ea1-112">方法</span><span class="sxs-lookup"><span data-stu-id="54ea1-112">Method</span></span>                                                                                       | <span data-ttu-id="54ea1-113">説明</span><span class="sxs-lookup"><span data-stu-id="54ea1-113">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54ea1-114">public str addContextMenuItems()</span><span class="sxs-lookup"><span data-stu-id="54ea1-114">public str addContextMenuItems()</span></span>                                                             | <span data-ttu-id="54ea1-115">プロジェクト ノードのショートカット メニューに品目のリストを追加します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-115">Adds a list of items to the shortcut menu of the project node.</span></span>                                                                                |
| <span data-ttu-id="54ea1-116">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="54ea1-116">public str changedBy(\[str value\])</span></span>                                                          | <span data-ttu-id="54ea1-117">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-117">Gets or sets the name of the user who last changed the application object.</span></span>                                                                    |
| <span data-ttu-id="54ea1-118">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="54ea1-118">public Date changedDate(\[Date value\])</span></span>                                                      | <span data-ttu-id="54ea1-119">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-119">Gets or sets the date an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="54ea1-120">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="54ea1-120">public str changedTime(\[str value\])</span></span>                                                        | <span data-ttu-id="54ea1-121">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-121">Gets or sets the time an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="54ea1-122">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="54ea1-122">public str createdBy(\[str value\])</span></span>                                                          | <span data-ttu-id="54ea1-123">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-123">Gets or sets the name of the user who created the application object.</span></span>                                                                         |
| <span data-ttu-id="54ea1-124">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="54ea1-124">public Date creationDate(\[Date value\])</span></span>                                                     | <span data-ttu-id="54ea1-125">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-125">Gets or sets the date an application object was created.</span></span>                                                                                      |
| <span data-ttu-id="54ea1-126">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="54ea1-126">public str creationTime(\[str value\])</span></span>                                                       |                                                                                                                                               |
| <span data-ttu-id="54ea1-127">public str export(str buffer)</span><span class="sxs-lookup"><span data-stu-id="54ea1-127">public str export(str buffer)</span></span>                                                                |                                                                                                                                               |
| <span data-ttu-id="54ea1-128">public TreeNode findGroupMember(str name, UtilElementType type, \[boolean searchSubgroups\])</span><span class="sxs-lookup"><span data-stu-id="54ea1-128">public TreeNode findGroupMember(str name, UtilElementType type, \[boolean searchSubgroups\])</span></span> | <span data-ttu-id="54ea1-129">特定の要素のプロジェクトまたはグループを検索します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-129">Searches the project or group for a specific element.</span></span>                                                                                         |
| <span data-ttu-id="54ea1-130">public str getProjectClassName()</span><span class="sxs-lookup"><span data-stu-id="54ea1-130">public str getProjectClassName()</span></span>                                                             | <span data-ttu-id="54ea1-131">プロジェクトの classid に対応するクラスの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-131">Returns the name of the class corresponding to the classid of the project.</span></span>                                                                    |
| <span data-ttu-id="54ea1-132">public ProjectNode getRunNode()</span><span class="sxs-lookup"><span data-stu-id="54ea1-132">public ProjectNode getRunNode()</span></span>                                                              | <span data-ttu-id="54ea1-133">プロジェクト ウィンドウを開いて、プロジェクトの概要ウィンドウで見つかった特定の projectNode のためにそのウィンドウのルート projectNode を返します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-133">Opens the project window and returns the root projectNode of that window, for a particular projectNode found in the project overview window.</span></span>  |
| <span data-ttu-id="54ea1-134">public str import(str buffer)</span><span class="sxs-lookup"><span data-stu-id="54ea1-134">public str import(str buffer)</span></span>                                                                |                                                                                                                                               |
| <span data-ttu-id="54ea1-135">public boolean isRunNode()</span><span class="sxs-lookup"><span data-stu-id="54ea1-135">public boolean isRunNode()</span></span>                                                                   |                                                                                                                                               |
| <span data-ttu-id="54ea1-136">public ProjectNode loadForInspection()</span><span class="sxs-lookup"><span data-stu-id="54ea1-136">public ProjectNode loadForInspection()</span></span>                                                       | <span data-ttu-id="54ea1-137">プロジェクトの概要ウィンドウにある projectNode の読み込まれたバージョンを返します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-137">Returns a loaded version of a projectNode found in the project overview window.</span></span>                                                               |
| <span data-ttu-id="54ea1-138">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="54ea1-138">public str name(\[str value\])</span></span>                                                               | <span data-ttu-id="54ea1-139">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-139">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="54ea1-140">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="54ea1-140">public Guid origin(\[Guid value\])</span></span>                                                           |                                                                                                                                               |
| <span data-ttu-id="54ea1-141">public boolean removeFromProject(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="54ea1-141">public boolean removeFromProject(TreeNode node)</span></span>                                              |                                                                                                                                               |
| <span data-ttu-id="54ea1-142">public str tooltipText(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="54ea1-142">public str tooltipText(TreeNode node)</span></span>                                                        |                                                                                                                                               |
| <span data-ttu-id="54ea1-143">::public static str projectType()</span><span class="sxs-lookup"><span data-stu-id="54ea1-143">::public static str projectType()</span></span>                                                            |                                                                                                                                               |
| <span data-ttu-id="54ea1-144">public void lockUpdate()</span><span class="sxs-lookup"><span data-stu-id="54ea1-144">public void lockUpdate()</span></span>                                                                     | <span data-ttu-id="54ea1-145">一連のアクションを実行中に、視覚的な更新を禁止します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-145">Prevents visual updates while a series of actions is being performed.</span></span>                                                                         |
| <span data-ttu-id="54ea1-146">public void addSpecialOverlayIcon(str path, int resId, \[int xOffset\], \[int yOffset\])</span><span class="sxs-lookup"><span data-stu-id="54ea1-146">public void addSpecialOverlayIcon(str path, int resId, \[int xOffset\], \[int yOffset\])</span></span>     |                                                                                                                                               |
| <span data-ttu-id="54ea1-147">public void created(str name)</span><span class="sxs-lookup"><span data-stu-id="54ea1-147">public void created(str name)</span></span>                                                                | <span data-ttu-id="54ea1-148">プロジェクトの新しいインスタンスが作成された際、プロジェクトでカスタム アクションを実行を有効にします。</span><span class="sxs-lookup"><span data-stu-id="54ea1-148">Enables the ability to perform custom actions on a project when a new instance of the project is created.</span></span>                                     |
| <span data-ttu-id="54ea1-149">public void setSpecialIcon(int type, str name, int resId)</span><span class="sxs-lookup"><span data-stu-id="54ea1-149">public void setSpecialIcon(int type, str name, int resId)</span></span>                                    | <span data-ttu-id="54ea1-150">プロジェクト内の特定のノードに別のアイコンを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="54ea1-150">Assigns a different icon to a specific node in the project.</span></span>                                                                                   |
| <span data-ttu-id="54ea1-151">public void loadProject(str buffer)</span><span class="sxs-lookup"><span data-stu-id="54ea1-151">public void loadProject(str buffer)</span></span>                                                          | <span data-ttu-id="54ea1-152">プロジェクトが読み込まれた際、プロジェクト定義にカスタムデータの格納と取得を有効にします。</span><span class="sxs-lookup"><span data-stu-id="54ea1-152">Enables storing and retrieving custom data in the project definition when a project is loaded.</span></span>                                                |
| <span data-ttu-id="54ea1-153">public void saveProject(str buffer)</span><span class="sxs-lookup"><span data-stu-id="54ea1-153">public void saveProject(str buffer)</span></span>                                                          | <span data-ttu-id="54ea1-154">アプリケーション オブジェクト データベースでは、プロジェクトと共にカスタム データの保存を有効にします。</span><span class="sxs-lookup"><span data-stu-id="54ea1-154">Enables saving custom data together with the project in the application object database.</span></span>                                                      |
| <span data-ttu-id="54ea1-155">public void unlockUpdate()</span><span class="sxs-lookup"><span data-stu-id="54ea1-155">public void unlockUpdate()</span></span>                                                                   | <span data-ttu-id="54ea1-156">lockUpdate で一連のアクションを開始した後にビジュアル更新プログラムを有効にします。</span><span class="sxs-lookup"><span data-stu-id="54ea1-156">Enables a visual update after a series of actions started with lockUpdate.</span></span>                                                                    |
| <span data-ttu-id="54ea1-157">public void handleContextMenuItem(int id)</span><span class="sxs-lookup"><span data-stu-id="54ea1-157">public void handleContextMenuItem(int id)</span></span>                                                    | <span data-ttu-id="54ea1-158">ユーザーが対応するメソッド addContextMenuItems で定義されているショートカット メニューの項目を選択するのを処理します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-158">Handles a user selecting an item on the shortcut menu that has been defined by the corresponding method addContextMenuItems.</span></span>                  |
| <span data-ttu-id="54ea1-159">public void addNode(TreeNode node)</span><span class="sxs-lookup"><span data-stu-id="54ea1-159">public void addNode(TreeNode node)</span></span>                                                           | <span data-ttu-id="54ea1-160">プロジェクトに既存のノードを追加します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-160">Adds an existing node to the project.</span></span>                                                                                                         |
| <span data-ttu-id="54ea1-161">public void addUtilNode(UtilElementType type, str name)</span><span class="sxs-lookup"><span data-stu-id="54ea1-161">public void addUtilNode(UtilElementType type, str name)</span></span>                                      | <span data-ttu-id="54ea1-162">プロジェクトにノードを追加します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-162">Adds a node to the project.</span></span>                                                                                                                   |
| <span data-ttu-id="54ea1-163">public void clear()</span><span class="sxs-lookup"><span data-stu-id="54ea1-163">public void clear()</span></span>                                                                          | <span data-ttu-id="54ea1-164">プロジェクトの内容を削除します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-164">Removes the contents of a project.</span></span>                                                                                                            |
| <span data-ttu-id="54ea1-165">public void setProjectClass(int classid)</span><span class="sxs-lookup"><span data-stu-id="54ea1-165">public void setProjectClass(int classid)</span></span>                                                     | <span data-ttu-id="54ea1-166">クラスをプロジェクトに割り当てますが、クラスに定義されているタイプをプロジェクトに与えます。</span><span class="sxs-lookup"><span data-stu-id="54ea1-166">Assigns a class to the project, which gives the project the type that the class defines.</span></span>                                                      |
| <span data-ttu-id="54ea1-167">public void removeSpecialOverlayIcons(str path)</span><span class="sxs-lookup"><span data-stu-id="54ea1-167">public void removeSpecialOverlayIcons(str path)</span></span>                                              |                                                                                                                                               |
| <span data-ttu-id="54ea1-168">public void new()</span><span class="sxs-lookup"><span data-stu-id="54ea1-168">public void new()</span></span>                                                                            | <span data-ttu-id="54ea1-169">ProjectNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-169">Initializes a new instance of the ProjectNode class.</span></span>                                                                                          |

## <a name="method-addcontextmenuitems"></a><span data-ttu-id="54ea1-170">メソッド addContextMenuItems</span><span class="sxs-lookup"><span data-stu-id="54ea1-170">Method addContextMenuItems</span></span>

<span data-ttu-id="54ea1-171">プロジェクト ノードのショートカット メニューに品目のリストを追加します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-171">Adds a list of items to the shortcut menu of the project node.</span></span>

```xpp
public str addContextMenuItems()
```

### <a name="return-value---addcontextmenuitems"></a><span data-ttu-id="54ea1-172">戻り値 - addContextMenuItems</span><span class="sxs-lookup"><span data-stu-id="54ea1-172">Return Value - addContextMenuItems</span></span>

<span data-ttu-id="54ea1-173">追加するメニュー項目のコンマ区切りリスト。</span><span class="sxs-lookup"><span data-stu-id="54ea1-173">A comma-separated list of the menu items to be added.</span></span>

### <a name="remarks---addcontextmenuitems"></a><span data-ttu-id="54ea1-174">備考 - addContextMenuItems</span><span class="sxs-lookup"><span data-stu-id="54ea1-174">Remarks - addContextMenuItems</span></span>

<span data-ttu-id="54ea1-175">プロジェクト ノードのショートカット メニューに品目のリストを追加するには、このメソッドを上書きします。</span><span class="sxs-lookup"><span data-stu-id="54ea1-175">Override this method to add a list of items to the shortcut menu of the project node.</span></span> <span data-ttu-id="54ea1-176">追加されたメニュー項目の 1 つがユーザーによって選択されると、handleContextMenuItem メソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="54ea1-176">When one of the added menu items is selected by a user, the handleContextMenuItem method is called.</span></span> <span data-ttu-id="54ea1-177">適切なアクションを実行するには、このメソッドを上書きします。</span><span class="sxs-lookup"><span data-stu-id="54ea1-177">Override this method to perform the appropriate action.</span></span>

## <a name="method-changedby"></a><span data-ttu-id="54ea1-178">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="54ea1-178">Method changedBy</span></span>

<span data-ttu-id="54ea1-179">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-179">Gets or sets the name of the user who last changed the application object.</span></span>

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a><span data-ttu-id="54ea1-180">パラメーター - changedBy</span><span class="sxs-lookup"><span data-stu-id="54ea1-180">Parameters - changedBy</span></span>

<span data-ttu-id="54ea1-181">値</span><span class="sxs-lookup"><span data-stu-id="54ea1-181">value</span></span>  

### <a name="return-value---changedby"></a><span data-ttu-id="54ea1-182">戻り値 - changedBy</span><span class="sxs-lookup"><span data-stu-id="54ea1-182">Return Value - changedBy</span></span>

<span data-ttu-id="54ea1-183">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="54ea1-183">The name of the user.</span></span>

## <a name="method-changeddate"></a><span data-ttu-id="54ea1-184">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="54ea1-184">Method changedDate</span></span>

<span data-ttu-id="54ea1-185">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-185">Gets or sets the date an application object was last changed.</span></span>

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a><span data-ttu-id="54ea1-186">パラメーター - changedDate</span><span class="sxs-lookup"><span data-stu-id="54ea1-186">Parameters - changedDate</span></span>

<span data-ttu-id="54ea1-187">値</span><span class="sxs-lookup"><span data-stu-id="54ea1-187">value</span></span>  

### <a name="return-value---changeddate"></a><span data-ttu-id="54ea1-188">戻り値 - changedDate</span><span class="sxs-lookup"><span data-stu-id="54ea1-188">Return Value - changedDate</span></span>

<span data-ttu-id="54ea1-189">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="54ea1-189">The date an application object was last changed.</span></span>

## <a name="method-changedtime"></a><span data-ttu-id="54ea1-190">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="54ea1-190">Method changedTime</span></span>

<span data-ttu-id="54ea1-191">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-191">Gets or sets the time an application object was last changed.</span></span>

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a><span data-ttu-id="54ea1-192">パラメーター - changedTime</span><span class="sxs-lookup"><span data-stu-id="54ea1-192">Parameters - changedTime</span></span>

<span data-ttu-id="54ea1-193">値</span><span class="sxs-lookup"><span data-stu-id="54ea1-193">value</span></span>  

### <a name="return-value---changedtime"></a><span data-ttu-id="54ea1-194">戻り値 - changedTime</span><span class="sxs-lookup"><span data-stu-id="54ea1-194">Return Value - changedTime</span></span>

<span data-ttu-id="54ea1-195">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="54ea1-195">The time an application object was last changed.</span></span>

## <a name="method-createdby"></a><span data-ttu-id="54ea1-196">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="54ea1-196">Method createdBy</span></span>

<span data-ttu-id="54ea1-197">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-197">Gets or sets the name of the user who created the application object.</span></span>

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a><span data-ttu-id="54ea1-198">パラメーター - createdBy</span><span class="sxs-lookup"><span data-stu-id="54ea1-198">Parameters - createdBy</span></span>

<span data-ttu-id="54ea1-199">値</span><span class="sxs-lookup"><span data-stu-id="54ea1-199">value</span></span>  

### <a name="return-value---createdby"></a><span data-ttu-id="54ea1-200">戻り値 - createdBy</span><span class="sxs-lookup"><span data-stu-id="54ea1-200">Return Value - createdBy</span></span>

<span data-ttu-id="54ea1-201">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="54ea1-201">The name of the user.</span></span>

## <a name="method-creationdate"></a><span data-ttu-id="54ea1-202">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="54ea1-202">Method creationDate</span></span>

<span data-ttu-id="54ea1-203">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-203">Gets or sets the date an application object was created.</span></span>

```xpp
public Date creationDate([Date value])
```

### <a name="parameters---creationdate"></a><span data-ttu-id="54ea1-204">パラメーター - creationDate</span><span class="sxs-lookup"><span data-stu-id="54ea1-204">Parameters - creationDate</span></span>

<span data-ttu-id="54ea1-205">値</span><span class="sxs-lookup"><span data-stu-id="54ea1-205">value</span></span>  

### <a name="return-value---creationdate"></a><span data-ttu-id="54ea1-206">戻り値 - creationDate</span><span class="sxs-lookup"><span data-stu-id="54ea1-206">Return Value - creationDate</span></span>

<span data-ttu-id="54ea1-207">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="54ea1-207">The date an application object was created.</span></span>

## <a name="method-creationtime"></a><span data-ttu-id="54ea1-208">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="54ea1-208">Method creationTime</span></span>

```xpp
public str creationTime([str value])
```

### <a name="parameters---creationtime"></a><span data-ttu-id="54ea1-209">パラメーター - creationTime</span><span class="sxs-lookup"><span data-stu-id="54ea1-209">Parameters - creationTime</span></span>

<span data-ttu-id="54ea1-210">値</span><span class="sxs-lookup"><span data-stu-id="54ea1-210">value</span></span>  

### <a name="return-value---creationtime"></a><span data-ttu-id="54ea1-211">戻り値 - creationTime</span><span class="sxs-lookup"><span data-stu-id="54ea1-211">Return Value - creationTime</span></span>

## <a name="method-export"></a><span data-ttu-id="54ea1-212">メソッド export</span><span class="sxs-lookup"><span data-stu-id="54ea1-212">Method export</span></span>

```xpp
public str export(str buffer)
```

### <a name="parameters---export"></a><span data-ttu-id="54ea1-213">パラメーター - export</span><span class="sxs-lookup"><span data-stu-id="54ea1-213">Parameters - export</span></span>

<span data-ttu-id="54ea1-214">バッファ</span><span class="sxs-lookup"><span data-stu-id="54ea1-214">buffer</span></span>  

### <a name="return-value---export"></a><span data-ttu-id="54ea1-215">戻り値 - export</span><span class="sxs-lookup"><span data-stu-id="54ea1-215">Return Value - export</span></span>

## <a name="method-findgroupmember"></a><span data-ttu-id="54ea1-216">メソッド findGroupMember</span><span class="sxs-lookup"><span data-stu-id="54ea1-216">Method findGroupMember</span></span>

<span data-ttu-id="54ea1-217">特定の要素のプロジェクトまたはグループを検索します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-217">Searches the project or group for a specific element.</span></span>

```xpp
public TreeNode findGroupMember(str name, UtilElementType type, [boolean searchSubgroups])
```

### <a name="parameters---findgroupmember"></a><span data-ttu-id="54ea1-218">パラメーター - findGroupMember</span><span class="sxs-lookup"><span data-stu-id="54ea1-218">Parameters - findGroupMember</span></span>

<span data-ttu-id="54ea1-219">名前</span><span class="sxs-lookup"><span data-stu-id="54ea1-219">name</span></span>  
<span data-ttu-id="54ea1-220">検索を再帰的に行うかどうかを決定するブール値フラグ; オプション。</span><span class="sxs-lookup"><span data-stu-id="54ea1-220">A Boolean flag to determine whether the search should be recursive; optional.</span></span>

<!-- -->

<span data-ttu-id="54ea1-221">タイプ</span><span class="sxs-lookup"><span data-stu-id="54ea1-221">type</span></span>  
<span data-ttu-id="54ea1-222">検索を再帰的に行うかどうかを決定するブール値フラグ; オプション。</span><span class="sxs-lookup"><span data-stu-id="54ea1-222">A Boolean flag to determine whether the search should be recursive; optional.</span></span>

<!-- -->

<span data-ttu-id="54ea1-223">searchSubgroups</span><span class="sxs-lookup"><span data-stu-id="54ea1-223">searchSubgroups</span></span>  
<span data-ttu-id="54ea1-224">検索を再帰的に行うかどうかを決定するブール値フラグ; オプション。</span><span class="sxs-lookup"><span data-stu-id="54ea1-224">A Boolean flag to determine whether the search should be recursive; optional.</span></span>

### <a name="return-value---findgroupmember"></a><span data-ttu-id="54ea1-225">戻り値 - findGroupMember</span><span class="sxs-lookup"><span data-stu-id="54ea1-225">Return Value - findGroupMember</span></span>

<span data-ttu-id="54ea1-226">オブジェクトが見つからない場合は、条件を満たす最初のオブジェクト、または nullNothingnullptrunita null 参照 (Visual Basic にはなし)。</span><span class="sxs-lookup"><span data-stu-id="54ea1-226">The first object that fits the criteria, or nullNothingnullptrunita null reference (Nothing in Visual Basic) if no object is found.</span></span>

### <a name="remarks---findgroupmember"></a><span data-ttu-id="54ea1-227">備考 - findGroupMember</span><span class="sxs-lookup"><span data-stu-id="54ea1-227">Remarks - findGroupMember</span></span>

<span data-ttu-id="54ea1-228">このメソッドは ProjectGroupNode にもあります。</span><span class="sxs-lookup"><span data-stu-id="54ea1-228">This method is also found on ProjectGroupNode.</span></span>

## <a name="method-getprojectclassname"></a><span data-ttu-id="54ea1-229">メソッド getProjectClassName</span><span class="sxs-lookup"><span data-stu-id="54ea1-229">Method getProjectClassName</span></span>

<span data-ttu-id="54ea1-230">プロジェクトの classid に対応するクラスの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-230">Returns the name of the class corresponding to the classid of the project.</span></span>

```xpp
public str getProjectClassName()
```

### <a name="return-value---getprojectclassname"></a><span data-ttu-id="54ea1-231">戻り値 - getProjectClassName</span><span class="sxs-lookup"><span data-stu-id="54ea1-231">Return Value - getProjectClassName</span></span>

<span data-ttu-id="54ea1-232">プロジェクトの classid に対応するクラスの名前。</span><span class="sxs-lookup"><span data-stu-id="54ea1-232">The name of the class corresponding to the classid of the project.</span></span>

### <a name="remarks---getprojectclassname"></a><span data-ttu-id="54ea1-233">備考 - getProjectClassName</span><span class="sxs-lookup"><span data-stu-id="54ea1-233">Remarks - getProjectClassName</span></span>

<span data-ttu-id="54ea1-234">setClassId メソッドは、クラス ID をプロジェクトに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="54ea1-234">The setClassId method assigns a classid to the project.</span></span>

## <a name="method-getrunnode"></a><span data-ttu-id="54ea1-235">メソッド getRunNode</span><span class="sxs-lookup"><span data-stu-id="54ea1-235">Method getRunNode</span></span>

<span data-ttu-id="54ea1-236">プロジェクト ウィンドウを開いて、プロジェクトの概要ウィンドウで見つかった特定の projectNode のためにそのウィンドウのルート projectNode を返します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-236">Opens the project window and returns the root projectNode of that window, for a particular projectNode found in the project overview window.</span></span>

```xpp
public ProjectNode getRunNode()
```

### <a name="return-value---getrunnode"></a><span data-ttu-id="54ea1-237">戻り値 - getRunNode</span><span class="sxs-lookup"><span data-stu-id="54ea1-237">Return Value - getRunNode</span></span>

<span data-ttu-id="54ea1-238">実行中の projectNode。</span><span class="sxs-lookup"><span data-stu-id="54ea1-238">The running projectNode.</span></span>

### <a name="remarks---getrunnode"></a><span data-ttu-id="54ea1-239">備考 - getRunNode</span><span class="sxs-lookup"><span data-stu-id="54ea1-239">Remarks - getRunNode</span></span>

<span data-ttu-id="54ea1-240">[プロジェクト] ウィンドウを開くことがなく実行中の projectNode を取得するには、ProjectNode.loadForInspection メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-240">To obtain a running projectNode without opening the project window, use the ProjectNode.loadForInspection Method.</span></span>

## <a name="method-import"></a><span data-ttu-id="54ea1-241">メソッド import</span><span class="sxs-lookup"><span data-stu-id="54ea1-241">Method import</span></span>

```xpp
public str import(str buffer)
```

### <a name="parameters---import"></a><span data-ttu-id="54ea1-242">パラメーター - import</span><span class="sxs-lookup"><span data-stu-id="54ea1-242">Parameters - import</span></span>

<span data-ttu-id="54ea1-243">バッファ</span><span class="sxs-lookup"><span data-stu-id="54ea1-243">buffer</span></span>  

### <a name="return-value---import"></a><span data-ttu-id="54ea1-244">戻り値 - import</span><span class="sxs-lookup"><span data-stu-id="54ea1-244">Return Value - import</span></span>

## <a name="method-isrunnode"></a><span data-ttu-id="54ea1-245">メソッド isRunNode</span><span class="sxs-lookup"><span data-stu-id="54ea1-245">Method isRunNode</span></span>

```xpp
public boolean isRunNode()
```

### <a name="return-value---isrunnode"></a><span data-ttu-id="54ea1-246">戻り値 - isRunNode</span><span class="sxs-lookup"><span data-stu-id="54ea1-246">Return Value - isRunNode</span></span>

## <a name="method-loadforinspection"></a><span data-ttu-id="54ea1-247">メソッド loadForInspection</span><span class="sxs-lookup"><span data-stu-id="54ea1-247">Method loadForInspection</span></span>

<span data-ttu-id="54ea1-248">プロジェクトの概要ウィンドウにある projectNode の読み込まれたバージョンを返します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-248">Returns a loaded version of a projectNode found in the project overview window.</span></span>

```xpp
public ProjectNode loadForInspection()
```

### <a name="return-value---loadforinspection"></a><span data-ttu-id="54ea1-249">戻り値 - loadForInspection</span><span class="sxs-lookup"><span data-stu-id="54ea1-249">Return Value - loadForInspection</span></span>

<span data-ttu-id="54ea1-250">読み込まれた projectNode。</span><span class="sxs-lookup"><span data-stu-id="54ea1-250">The loaded projectNode.</span></span>

### <a name="remarks---loadforinspection"></a><span data-ttu-id="54ea1-251">備考 - loadForInspection</span><span class="sxs-lookup"><span data-stu-id="54ea1-251">Remarks - loadForInspection</span></span>

<span data-ttu-id="54ea1-252">[プロジェクト] ウィンドウを開いたときに projectNode を読み込むには、getRunNode メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-252">To get a loaded projectNode while also opening the project window, use the method getRunNode.</span></span>

## <a name="method-name"></a><span data-ttu-id="54ea1-253">メソッド名</span><span class="sxs-lookup"><span data-stu-id="54ea1-253">Method name</span></span>

<span data-ttu-id="54ea1-254">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-254">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="54ea1-255">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="54ea1-255">Parameters - name</span></span>

<span data-ttu-id="54ea1-256">値</span><span class="sxs-lookup"><span data-stu-id="54ea1-256">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="54ea1-257">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="54ea1-257">Return Value - name</span></span>

<span data-ttu-id="54ea1-258">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="54ea1-258">The name that is used in the code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="54ea1-259">備考 - name</span><span class="sxs-lookup"><span data-stu-id="54ea1-259">Remarks - name</span></span>

<span data-ttu-id="54ea1-260">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="54ea1-260">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="54ea1-261">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="54ea1-261">Begins with a letter.</span></span>
-   <span data-ttu-id="54ea1-262">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="54ea1-262">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="54ea1-263">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="54ea1-263">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="54ea1-264">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="54ea1-264">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="54ea1-265">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="54ea1-265">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-origin"></a><span data-ttu-id="54ea1-266">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="54ea1-266">Method origin</span></span>

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a><span data-ttu-id="54ea1-267">パラメーター - origin</span><span class="sxs-lookup"><span data-stu-id="54ea1-267">Parameters - origin</span></span>

<span data-ttu-id="54ea1-268">値</span><span class="sxs-lookup"><span data-stu-id="54ea1-268">value</span></span>  

### <a name="return-value---origin"></a><span data-ttu-id="54ea1-269">戻り値 - origin</span><span class="sxs-lookup"><span data-stu-id="54ea1-269">Return Value - origin</span></span>

## <a name="method-removefromproject"></a><span data-ttu-id="54ea1-270">メソッド removeFromProject</span><span class="sxs-lookup"><span data-stu-id="54ea1-270">Method removeFromProject</span></span>

```xpp
public boolean removeFromProject(TreeNode node)
```

### <a name="parameters---removefromproject"></a><span data-ttu-id="54ea1-271">パラメーター - removeFromProject</span><span class="sxs-lookup"><span data-stu-id="54ea1-271">Parameters - removeFromProject</span></span>

<span data-ttu-id="54ea1-272">node</span><span class="sxs-lookup"><span data-stu-id="54ea1-272">node</span></span>  

### <a name="return-value---removefromproject"></a><span data-ttu-id="54ea1-273">戻り値 - removeFromProject</span><span class="sxs-lookup"><span data-stu-id="54ea1-273">Return Value - removeFromProject</span></span>

## <a name="method-tooltiptext"></a><span data-ttu-id="54ea1-274">メソッド tooltipText</span><span class="sxs-lookup"><span data-stu-id="54ea1-274">Method tooltipText</span></span>

```xpp
public str tooltipText(TreeNode node)
```

### <a name="parameters---tooltiptext"></a><span data-ttu-id="54ea1-275">パラメーター - tooltipText</span><span class="sxs-lookup"><span data-stu-id="54ea1-275">Parameters - tooltipText</span></span>

<span data-ttu-id="54ea1-276">node</span><span class="sxs-lookup"><span data-stu-id="54ea1-276">node</span></span>  

### <a name="return-value---tooltiptext"></a><span data-ttu-id="54ea1-277">戻り値 - tooltipText</span><span class="sxs-lookup"><span data-stu-id="54ea1-277">Return Value - tooltipText</span></span>

## <a name="method-projecttype"></a><span data-ttu-id="54ea1-278">メソッド projectType</span><span class="sxs-lookup"><span data-stu-id="54ea1-278">Method projectType</span></span>

```xpp
public static str projectType()
```

### <a name="return-value---projecttype"></a><span data-ttu-id="54ea1-279">戻り値 - projectType</span><span class="sxs-lookup"><span data-stu-id="54ea1-279">Return Value - projectType</span></span>

## <a name="method-lockupdate"></a><span data-ttu-id="54ea1-280">メソッド lockUpdate</span><span class="sxs-lookup"><span data-stu-id="54ea1-280">Method lockUpdate</span></span>

<span data-ttu-id="54ea1-281">一連のアクションを実行中に、視覚的な更新を禁止します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-281">Prevents visual updates while a series of actions is being performed.</span></span>

```xpp
public void lockUpdate()
```

### <a name="remarks---lockupdate"></a><span data-ttu-id="54ea1-282">備考 - lockUpdate</span><span class="sxs-lookup"><span data-stu-id="54ea1-282">Remarks - lockUpdate</span></span>

<span data-ttu-id="54ea1-283">一連のアクションの後にビジュアル アップデートを実行するには、unlockUpdate を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-283">To perform visual updates after the series of actions, call unlockUpdate.</span></span>

## <a name="method-addspecialoverlayicon"></a><span data-ttu-id="54ea1-284">メソッド addSpecialOverlayIcon</span><span class="sxs-lookup"><span data-stu-id="54ea1-284">Method addSpecialOverlayIcon</span></span>

```xpp
public void addSpecialOverlayIcon(str path, int resId, [int xOffset], [int yOffset])
```

### <a name="parameters---addspecialoverlayicon"></a><span data-ttu-id="54ea1-285">パラメーター - addSpecialOverlayIcon</span><span class="sxs-lookup"><span data-stu-id="54ea1-285">Parameters - addSpecialOverlayIcon</span></span>

<span data-ttu-id="54ea1-286">path</span><span class="sxs-lookup"><span data-stu-id="54ea1-286">path</span></span>  

<!-- -->

<span data-ttu-id="54ea1-287">resId</span><span class="sxs-lookup"><span data-stu-id="54ea1-287">resId</span></span>  

<!-- -->

<span data-ttu-id="54ea1-288">xOffset</span><span class="sxs-lookup"><span data-stu-id="54ea1-288">xOffset</span></span>  

<!-- -->

<span data-ttu-id="54ea1-289">yOffset</span><span class="sxs-lookup"><span data-stu-id="54ea1-289">yOffset</span></span>  

## <a name="method-created"></a><span data-ttu-id="54ea1-290">メソッド created</span><span class="sxs-lookup"><span data-stu-id="54ea1-290">Method created</span></span>

<span data-ttu-id="54ea1-291">プロジェクトの新しいインスタンスが作成された際、プロジェクトでカスタム アクションを実行を有効にします。</span><span class="sxs-lookup"><span data-stu-id="54ea1-291">Enables the ability to perform custom actions on a project when a new instance of the project is created.</span></span>

```xpp
public void created(str name)
```

### <a name="parameters---created"></a><span data-ttu-id="54ea1-292">パラメーター - created</span><span class="sxs-lookup"><span data-stu-id="54ea1-292">Parameters - created</span></span>

<span data-ttu-id="54ea1-293">名前</span><span class="sxs-lookup"><span data-stu-id="54ea1-293">name</span></span>  
<span data-ttu-id="54ea1-294">プロジェクト インスタンスの名前。</span><span class="sxs-lookup"><span data-stu-id="54ea1-294">The name of the project instance.</span></span>

### <a name="remarks---created"></a><span data-ttu-id="54ea1-295">備考 - created</span><span class="sxs-lookup"><span data-stu-id="54ea1-295">Remarks - created</span></span>

<span data-ttu-id="54ea1-296">このメソッドは、プロジェクトの新しいインスタンスが作成されるときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="54ea1-296">This method is called when a new instance of the project is created.</span></span> <span data-ttu-id="54ea1-297">プロジェクトでカスタム アクションを実行するには、このメソッドを上書きします。</span><span class="sxs-lookup"><span data-stu-id="54ea1-297">Override this method to perform custom actions on your project.</span></span>

## <a name="method-setspecialicon"></a><span data-ttu-id="54ea1-298">メソッド setSpecialIcon</span><span class="sxs-lookup"><span data-stu-id="54ea1-298">Method setSpecialIcon</span></span>

<span data-ttu-id="54ea1-299">プロジェクト内の特定のノードに別のアイコンを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="54ea1-299">Assigns a different icon to a specific node in the project.</span></span>

```xpp
public void setSpecialIcon(int type, str name, int resId)
```

### <a name="parameters---setspecialicon"></a><span data-ttu-id="54ea1-300">パラメーター - setSpecialIcon</span><span class="sxs-lookup"><span data-stu-id="54ea1-300">Parameters - setSpecialIcon</span></span>

<span data-ttu-id="54ea1-301">タイプ</span><span class="sxs-lookup"><span data-stu-id="54ea1-301">type</span></span>  
<span data-ttu-id="54ea1-302">指定されたノードに使用する必要があるアイコンの ID。</span><span class="sxs-lookup"><span data-stu-id="54ea1-302">The ID of the icon that must be used for the specified node.</span></span>

<!-- -->

<span data-ttu-id="54ea1-303">名前</span><span class="sxs-lookup"><span data-stu-id="54ea1-303">name</span></span>  
<span data-ttu-id="54ea1-304">指定されたノードに使用する必要があるアイコンの ID。</span><span class="sxs-lookup"><span data-stu-id="54ea1-304">The ID of the icon that must be used for the specified node.</span></span>

<!-- -->

<span data-ttu-id="54ea1-305">resId</span><span class="sxs-lookup"><span data-stu-id="54ea1-305">resId</span></span>  
<span data-ttu-id="54ea1-306">指定されたノードに使用する必要があるアイコンの ID。</span><span class="sxs-lookup"><span data-stu-id="54ea1-306">The ID of the icon that must be used for the specified node.</span></span>

## <a name="method-loadproject"></a><span data-ttu-id="54ea1-307">メソッド loadProject</span><span class="sxs-lookup"><span data-stu-id="54ea1-307">Method loadProject</span></span>

<span data-ttu-id="54ea1-308">プロジェクトが読み込まれた際、プロジェクト定義にカスタムデータの格納と取得を有効にします。</span><span class="sxs-lookup"><span data-stu-id="54ea1-308">Enables storing and retrieving custom data in the project definition when a project is loaded.</span></span>

```xpp
public void loadProject(str buffer)
```

### <a name="parameters---loadproject"></a><span data-ttu-id="54ea1-309">パラメーター - loadProject</span><span class="sxs-lookup"><span data-stu-id="54ea1-309">Parameters - loadProject</span></span>

<span data-ttu-id="54ea1-310">バッファ</span><span class="sxs-lookup"><span data-stu-id="54ea1-310">buffer</span></span>  
<span data-ttu-id="54ea1-311">saveProject によってプロジェクトに保存されたカスタム データを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="54ea1-311">A string that contains the custom data that was saved in the project by saveProject.</span></span>

### <a name="remarks---loadproject"></a><span data-ttu-id="54ea1-312">備考 - loadProject</span><span class="sxs-lookup"><span data-stu-id="54ea1-312">Remarks - loadProject</span></span>

<span data-ttu-id="54ea1-313">このメソッドは、プロジェクトが読み込まれたときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="54ea1-313">This method is called when a project is loaded.</span></span> <span data-ttu-id="54ea1-314">saveProject および loadProject を上書きすることにより、ユーザーはカスタム データをプロジェクト定義に保存して取得できます。</span><span class="sxs-lookup"><span data-stu-id="54ea1-314">By overriding saveProject and loadProject, a user can store and retrieve custom data in the project definition.</span></span> <span data-ttu-id="54ea1-315">読み込みを続行するには、プロジェクトの super() を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="54ea1-315">You must call super() for the project to continue loading.</span></span>

## <a name="method-saveproject"></a><span data-ttu-id="54ea1-316">メソッド saveProject</span><span class="sxs-lookup"><span data-stu-id="54ea1-316">Method saveProject</span></span>

<span data-ttu-id="54ea1-317">アプリケーション オブジェクト データベースでは、プロジェクトと共にカスタム データの保存を有効にします。</span><span class="sxs-lookup"><span data-stu-id="54ea1-317">Enables saving custom data together with the project in the application object database.</span></span>

```xpp
public void saveProject(str buffer)
```

### <a name="parameters---saveproject"></a><span data-ttu-id="54ea1-318">パラメーター - saveProject</span><span class="sxs-lookup"><span data-stu-id="54ea1-318">Parameters - saveProject</span></span>

<span data-ttu-id="54ea1-319">バッファ</span><span class="sxs-lookup"><span data-stu-id="54ea1-319">buffer</span></span>  
<span data-ttu-id="54ea1-320">データをパッキングするために使用する必要がある文字列バッファ。</span><span class="sxs-lookup"><span data-stu-id="54ea1-320">A string buffer that must be used for packing the data.</span></span> <span data-ttu-id="54ea1-321">その後、バッファ はsuper() に渡されなければなりません。</span><span class="sxs-lookup"><span data-stu-id="54ea1-321">The buffer must then be passed on to super().</span></span>

### <a name="remarks---saveproject"></a><span data-ttu-id="54ea1-322">備考 - saveProject</span><span class="sxs-lookup"><span data-stu-id="54ea1-322">Remarks - saveProject</span></span>

<span data-ttu-id="54ea1-323">このメソッドを上書きすることにより、アプリケーション オブジェクト データベースでは、プロジェクトと共にカスタム データを保存できます。</span><span class="sxs-lookup"><span data-stu-id="54ea1-323">By overriding this method, you can save custom data together with the project in the application object database.</span></span> <span data-ttu-id="54ea1-324">データは「&lt;APPDATA&gt; ... &lt;/APPDATA&gt;」の形式で XML 文字列として形成することをお勧めします。このデータは loadProject メソッドをオーバーライドして取得できます。</span><span class="sxs-lookup"><span data-stu-id="54ea1-324">It is recommended that the data be formed as an XML string in the following form: "&lt;APPDATA&gt; ... &lt;/APPDATA&gt;" The data can be retrieved by overriding the loadProject method.</span></span>

## <a name="method-unlockupdate"></a><span data-ttu-id="54ea1-325">メソッド unlockUpdate</span><span class="sxs-lookup"><span data-stu-id="54ea1-325">Method unlockUpdate</span></span>

<span data-ttu-id="54ea1-326">lockUpdate で一連のアクションを開始した後にビジュアル更新プログラムを有効にします。</span><span class="sxs-lookup"><span data-stu-id="54ea1-326">Enables a visual update after a series of actions started with lockUpdate.</span></span>

```xpp
public void unlockUpdate()
```

## <a name="method-handlecontextmenuitem"></a><span data-ttu-id="54ea1-327">メソッド handleContextMenuItem</span><span class="sxs-lookup"><span data-stu-id="54ea1-327">Method handleContextMenuItem</span></span>

<span data-ttu-id="54ea1-328">ユーザーが対応するメソッド addContextMenuItems で定義されているショートカット メニューの項目を選択するのを処理します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-328">Handles a user selecting an item on the shortcut menu that has been defined by the corresponding method addContextMenuItems.</span></span>

```xpp
public void handleContextMenuItem(int id)
```

### <a name="parameters---handlecontextmenuitem"></a><span data-ttu-id="54ea1-329">パラメーター - handleContextMenuItem</span><span class="sxs-lookup"><span data-stu-id="54ea1-329">Parameters - handleContextMenuItem</span></span>

<span data-ttu-id="54ea1-330">id</span><span class="sxs-lookup"><span data-stu-id="54ea1-330">id</span></span>  
<span data-ttu-id="54ea1-331">メニュー項目の ID。</span><span class="sxs-lookup"><span data-stu-id="54ea1-331">The ID of the menu items.</span></span> <span data-ttu-id="54ea1-332">これは、addContextMenuItems メソッドによって設定されたリスト内の 0 から始まる数値です。</span><span class="sxs-lookup"><span data-stu-id="54ea1-332">This is the zero-based number in the list set by the addContextMenuItems method.</span></span> <span data-ttu-id="54ea1-333">accContextMenuItems が文字列である "item1,item2" を返し、ユーザーがショートカット メニューの品目である "item2" を選択した場合、この方法では値 1 を使用します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-333">If accContextMenuItems returns the string "item1,item2" and the user selects the item "item2" in the shortcut menu, this method uses the value 1.</span></span>

### <a name="remarks---handlecontextmenuitem"></a><span data-ttu-id="54ea1-334">備考 - handleContextMenuItem</span><span class="sxs-lookup"><span data-stu-id="54ea1-334">Remarks - handleContextMenuItem</span></span>

<span data-ttu-id="54ea1-335">このメソッドは、ユーザーが対応するメソッド addContextMenuItems で定義されているショートカット メニューの項目を選択するときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="54ea1-335">This method is called when a user selects an item on the shortcut menu that has been defined by the corresponding method addContextMenuItems.</span></span>

## <a name="method-addnode"></a><span data-ttu-id="54ea1-336">メソッド addNode</span><span class="sxs-lookup"><span data-stu-id="54ea1-336">Method addNode</span></span>

<span data-ttu-id="54ea1-337">プロジェクトに既存のノードを追加します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-337">Adds an existing node to the project.</span></span>

```xpp
public void addNode(TreeNode node)
```

### <a name="parameters---addnode"></a><span data-ttu-id="54ea1-338">パラメーター - addNode</span><span class="sxs-lookup"><span data-stu-id="54ea1-338">Parameters - addNode</span></span>

<span data-ttu-id="54ea1-339">node</span><span class="sxs-lookup"><span data-stu-id="54ea1-339">node</span></span>  
<span data-ttu-id="54ea1-340">追加するノード。</span><span class="sxs-lookup"><span data-stu-id="54ea1-340">The node to add.</span></span>

## <a name="method-addutilnode"></a><span data-ttu-id="54ea1-341">メソッド addUtilNode</span><span class="sxs-lookup"><span data-stu-id="54ea1-341">Method addUtilNode</span></span>

<span data-ttu-id="54ea1-342">プロジェクトにノードを追加します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-342">Adds a node to the project.</span></span>

```xpp
public void addUtilNode(UtilElementType type, str name)
```

### <a name="parameters---addutilnode"></a><span data-ttu-id="54ea1-343">パラメーター - addUtilNode</span><span class="sxs-lookup"><span data-stu-id="54ea1-343">Parameters - addUtilNode</span></span>

<span data-ttu-id="54ea1-344">タイプ</span><span class="sxs-lookup"><span data-stu-id="54ea1-344">type</span></span>  
<span data-ttu-id="54ea1-345">ノードの名前。</span><span class="sxs-lookup"><span data-stu-id="54ea1-345">The name of the node.</span></span>

<!-- -->

<span data-ttu-id="54ea1-346">名前</span><span class="sxs-lookup"><span data-stu-id="54ea1-346">name</span></span>  
<span data-ttu-id="54ea1-347">ノードの名前。</span><span class="sxs-lookup"><span data-stu-id="54ea1-347">The name of the node.</span></span>

### <a name="remarks---addutilnode"></a><span data-ttu-id="54ea1-348">備考 - addUtilNode</span><span class="sxs-lookup"><span data-stu-id="54ea1-348">Remarks - addUtilNode</span></span>

<span data-ttu-id="54ea1-349">この関数は ProjectGroupNode にもあります。</span><span class="sxs-lookup"><span data-stu-id="54ea1-349">This function is also found on ProjectGroupNode.</span></span>

## <a name="method-clear"></a><span data-ttu-id="54ea1-350">メソッド clear</span><span class="sxs-lookup"><span data-stu-id="54ea1-350">Method clear</span></span>

<span data-ttu-id="54ea1-351">プロジェクトの内容を削除します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-351">Removes the contents of a project.</span></span>

```xpp
public void clear()
```

### <a name="remarks---clear"></a><span data-ttu-id="54ea1-352">備考 - clear</span><span class="sxs-lookup"><span data-stu-id="54ea1-352">Remarks - clear</span></span>

<span data-ttu-id="54ea1-353">このメソッドは、アプリケーション オブジェクト ツリー (AOT) からプロジェクトの内容を削除しません。�プロジェクト自体からのみです。</span><span class="sxs-lookup"><span data-stu-id="54ea1-353">This method does not remove the project contents from the Application Object Tree (AOT)�only from the project itself.</span></span> <span data-ttu-id="54ea1-354">このメソッドはプロジェクトの内容を削除しますが、プロジェクト フォルダーは削除しません。</span><span class="sxs-lookup"><span data-stu-id="54ea1-354">This method removes the project contents but does not remove the project folder.</span></span> <span data-ttu-id="54ea1-355">1 回のメソッド呼び出しでプロジェクトとその内容を削除するには、AOTdelete メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-355">To delete a project and its contents in one method call, use the AOTdelete method.</span></span> <span data-ttu-id="54ea1-356">オブジェクトを AOT から削除するには、AOTdelete メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-356">To delete objects from the AOT, use the AOTdelete method.</span></span>

### <a name="examples---clear"></a><span data-ttu-id="54ea1-357">例 - clear</span><span class="sxs-lookup"><span data-stu-id="54ea1-357">Examples - clear</span></span>

<span data-ttu-id="54ea1-358">次の例では、Project1 プロジェクト内のプライベート フォルダー内のオブジェクトをすべて削除します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-358">The following example removes any objects in the Project1 project in the Private folder.</span></span>

```xpp
static void clearProjectObjects(Args _args) 
    { 
        ProjectNode privatePn; 
        ProjectNode pn; 
        // Navigate to the Private projects folder. 
        privatePn = infolog.projectRootNode().AOTfindChild("Private"); 
        // Get a reference to the project. 
        pn = privatePn.AOTfindChild("Project1"); 
        // Clear the project. 
        pn.clear(); 
    }
```

## <a name="method-setprojectclass"></a><span data-ttu-id="54ea1-359">メソッド setProjectClass</span><span class="sxs-lookup"><span data-stu-id="54ea1-359">Method setProjectClass</span></span>

<span data-ttu-id="54ea1-360">クラスをプロジェクトに割り当てますが、クラスに定義されているタイプをプロジェクトに与えます。</span><span class="sxs-lookup"><span data-stu-id="54ea1-360">Assigns a class to the project, which gives the project the type that the class defines.</span></span>

```xpp
public void setProjectClass(int classid)
```

### <a name="parameters---setprojectclass"></a><span data-ttu-id="54ea1-361">パラメーター - setProjectClass</span><span class="sxs-lookup"><span data-stu-id="54ea1-361">Parameters - setProjectClass</span></span>

<span data-ttu-id="54ea1-362">classid</span><span class="sxs-lookup"><span data-stu-id="54ea1-362">classid</span></span>  
<span data-ttu-id="54ea1-363">プロジェクトに割り当てるクラスの ID。</span><span class="sxs-lookup"><span data-stu-id="54ea1-363">The ID of the class to assign to the project.</span></span>

### <a name="remarks---setprojectclass"></a><span data-ttu-id="54ea1-364">備考 - setProjectClass</span><span class="sxs-lookup"><span data-stu-id="54ea1-364">Remarks - setProjectClass</span></span>

<span data-ttu-id="54ea1-365">指定されたクラスは、projectNode クラスを拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="54ea1-365">The specified class must extend the projectNode class.</span></span>

## <a name="method-removespecialoverlayicons"></a><span data-ttu-id="54ea1-366">メソッド removeSpecialOverlayIcons</span><span class="sxs-lookup"><span data-stu-id="54ea1-366">Method removeSpecialOverlayIcons</span></span>

```xpp
public void removeSpecialOverlayIcons(str path)
```

### <a name="parameters---removespecialoverlayicons"></a><span data-ttu-id="54ea1-367">パラメーター - removeSpecialOverlayIcons</span><span class="sxs-lookup"><span data-stu-id="54ea1-367">Parameters - removeSpecialOverlayIcons</span></span>

<span data-ttu-id="54ea1-368">path</span><span class="sxs-lookup"><span data-stu-id="54ea1-368">path</span></span>  

## <a name="method-new"></a><span data-ttu-id="54ea1-369">メソッド new</span><span class="sxs-lookup"><span data-stu-id="54ea1-369">Method new</span></span>

<span data-ttu-id="54ea1-370">ProjectNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="54ea1-370">Initializes a new instance of the ProjectNode class.</span></span>

```xpp
public void new()
```

