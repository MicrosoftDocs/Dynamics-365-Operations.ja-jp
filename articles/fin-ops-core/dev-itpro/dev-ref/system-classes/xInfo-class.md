---
title: xInfo クラス
description: このトピックでは、xInfo クラスについて説明します。
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
ms.openlocfilehash: 245a4d3cd0c6faa4cf9090114748d3ce112155cc
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502763"
---
# <a name="class-xinfo"></a><span data-ttu-id="d3325-103">クラス xInfo</span><span class="sxs-lookup"><span data-stu-id="d3325-103">Class xInfo</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class xInfo extends Object
```

## <a name="remarks"></a><span data-ttu-id="d3325-104">備考</span><span class="sxs-lookup"><span data-stu-id="d3325-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="d3325-105">例</span><span class="sxs-lookup"><span data-stu-id="d3325-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="d3325-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="d3325-106">Methods</span></span>

| <span data-ttu-id="d3325-107">方法</span><span class="sxs-lookup"><span data-stu-id="d3325-107">Method</span></span>                                                                                                                                                                                                       | <span data-ttu-id="d3325-108">説明</span><span class="sxs-lookup"><span data-stu-id="d3325-108">Description</span></span>                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3325-109">public int removeMessage(Int64 messageId)</span><span class="sxs-lookup"><span data-stu-id="d3325-109">public int removeMessage(Int64 messageId)</span></span>                                                                                                                                                                    |                                                                                                                                                                                         |
| <span data-ttu-id="d3325-110">public Int64 insertMessage(MessageSeverity type, str message)</span><span class="sxs-lookup"><span data-stu-id="d3325-110">public Int64 insertMessage(MessageSeverity type, str message)</span></span>                                                                                                                                                |                                                                                                                                                                                         |
| <span data-ttu-id="d3325-111">public Exception add(Exception exceptionType, str string, \[str helpURL\], \[Object obj\], \[boolean buildprefix\])</span><span class="sxs-lookup"><span data-stu-id="d3325-111">public Exception add(Exception exceptionType, str string, \[str helpURL\], \[Object obj\], \[boolean buildprefix\])</span></span>                                                                                          | <span data-ttu-id="d3325-112">情報ログ バッファに文字列を追加します。</span><span class="sxs-lookup"><span data-stu-id="d3325-112">Adds a string to the Infolog buffer.</span></span>                                                                                                                                                    |
| <span data-ttu-id="d3325-113">public Exception addException(str string, str stackTrace)</span><span class="sxs-lookup"><span data-stu-id="d3325-113">public Exception addException(str string, str stackTrace)</span></span>                                                                                                                                                    |                                                                                                                                                                                         |
| <span data-ttu-id="d3325-114">public container breakpoint(\[container breakpoint\])</span><span class="sxs-lookup"><span data-stu-id="d3325-114">public container breakpoint(\[container breakpoint\])</span></span>                                                                                                                                                        | <span data-ttu-id="d3325-115">ブレークポイントに関する情報を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d3325-115">Gets or sets information about breakpoints.</span></span>                                                                                                                                             |
| <span data-ttu-id="d3325-116">public boolean canShowCreateRuleMenuItem(xFormRun caller)</span><span class="sxs-lookup"><span data-stu-id="d3325-116">public boolean canShowCreateRuleMenuItem(xFormRun caller)</span></span>                                                                                                                                                    | <span data-ttu-id="d3325-117">フォームの警告ルール作成フォームのメニュー項目を表示するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d3325-117">Determines whether the menu item for the Create alert rule form should be displayed for a form.</span></span>                                                                                         |
| <span data-ttu-id="d3325-118">public boolean canShutdown(boolean silent)</span><span class="sxs-lookup"><span data-stu-id="d3325-118">public boolean canShutdown(boolean silent)</span></span>                                                                                                                                                                   | <span data-ttu-id="d3325-119">システムをシャットダウンできるかどうかをテストします。</span><span class="sxs-lookup"><span data-stu-id="d3325-119">Tests whether the system can be shut down.</span></span> <span data-ttu-id="d3325-120">このメソッドを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="d3325-120">Do not use this method.</span></span> <span data-ttu-id="d3325-121">代わりに、Info クラスでオーバーライドされたバージョンを使用します。</span><span class="sxs-lookup"><span data-stu-id="d3325-121">Use the version that is overridden on the Info class instead.</span></span>                                                        |
| <span data-ttu-id="d3325-122">public boolean canViewAlertInbox()</span><span class="sxs-lookup"><span data-stu-id="d3325-122">public boolean canViewAlertInbox()</span></span>                                                                                                                                                                           | <span data-ttu-id="d3325-123">現在のユーザーに警告の表示フォームを表示するアクセス許可があるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="d3325-123">Determines whether the current user has permission to view the View alerts form.</span></span>                                                                                                        |
| <span data-ttu-id="d3325-124">public xCompilerOutput compilerOutput(\[Object compilerOut\])</span><span class="sxs-lookup"><span data-stu-id="d3325-124">public xCompilerOutput compilerOutput(\[Object compilerOut\])</span></span>                                                                                                                                                | <span data-ttu-id="d3325-125">コンパイラ出力オブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d3325-125">Gets or sets the compiler output object.</span></span> <span data-ttu-id="d3325-126">コンパイラ出力オブジェクトは、デフォルトでコンパイラ出力ウィンドウです。</span><span class="sxs-lookup"><span data-stu-id="d3325-126">The compiler output object is the Compiler output window by default.</span></span>                                                                           |
| <span data-ttu-id="d3325-127">public container copy(int from, int to)</span><span class="sxs-lookup"><span data-stu-id="d3325-127">public container copy(int from, int to)</span></span>                                                                                                                                                                      | <span data-ttu-id="d3325-128">情報ログ バッファーから行をコピーします。</span><span class="sxs-lookup"><span data-stu-id="d3325-128">Copies lines from the Infolog buffer.</span></span>                                                                                                                                                   |
| <span data-ttu-id="d3325-129">public int createDevelopmentWorkspaceWindow()</span><span class="sxs-lookup"><span data-stu-id="d3325-129">public int createDevelopmentWorkspaceWindow()</span></span>                                                                                                                                                                |                                                                                                                                                                                         |
| <span data-ttu-id="d3325-130">public int createWorkspaceWindow()</span><span class="sxs-lookup"><span data-stu-id="d3325-130">public int createWorkspaceWindow()</span></span>                                                                                                                                                                           | <span data-ttu-id="d3325-131">新しいワークスペース ウィンドウを開きます。</span><span class="sxs-lookup"><span data-stu-id="d3325-131">Opens a new workspace window.</span></span> <span data-ttu-id="d3325-132">たとえば、これにより、異なるウィンドウでアプリケーション オブジェクトの異なるセットを開く、または会社コードの 2 つの異なるセットを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="d3325-132">For example, this enables you to open different sets of application objects in different windows, or to work with two different sets of company accounts.</span></span> |
| <span data-ttu-id="d3325-133">public UtilEntryLevel currentAOLayer()</span><span class="sxs-lookup"><span data-stu-id="d3325-133">public UtilEntryLevel currentAOLayer()</span></span>                                                                                                                                                                       | <span data-ttu-id="d3325-134">SYS または USR などで実行している現在の階層を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-134">Retrieves the current layer you are running in such as SYS, or USR.</span></span>                                                                                                                     |
| <span data-ttu-id="d3325-135">public container cut(int from, int to)</span><span class="sxs-lookup"><span data-stu-id="d3325-135">public container cut(int from, int to)</span></span>                                                                                                                                                                       | <span data-ttu-id="d3325-136">情報ログ バッファーから行を切り取りします。</span><span class="sxs-lookup"><span data-stu-id="d3325-136">Cuts lines from the Infolog buffer.</span></span>                                                                                                                                                     |
| <span data-ttu-id="d3325-137">public str documentationLanguage(\[str languageCode\])</span><span class="sxs-lookup"><span data-stu-id="d3325-137">public str documentationLanguage(\[str languageCode\])</span></span>                                                                                                                                                       | <span data-ttu-id="d3325-138">ドキュメントに使用される言語を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d3325-138">Gets or sets the language that is used for the documentation.</span></span>                                                                                                     |
| <span data-ttu-id="d3325-139">public container export()</span><span class="sxs-lookup"><span data-stu-id="d3325-139">public container export()</span></span>                                                                                                                                                                                    |                                                                                                                                                                                         |
| <span data-ttu-id="d3325-140">public TreeNode findNode(str nodePath)</span><span class="sxs-lookup"><span data-stu-id="d3325-140">public TreeNode findNode(str nodePath)</span></span>                                                                                                                                                                       | <span data-ttu-id="d3325-141">指定されたツリー ノードを取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-141">Retrieves the specified a tree node.</span></span>                                                                                                                                                    |
| <span data-ttu-id="d3325-142">public TreeNode getDocNode(UtilFileType helpType, int UtilType, str Name, \[UtilElementId ParentId\], \[int Type\], \[UtilEntryLevel UtilLevel\], \[boolean ForceLevel\], \[int Mode\], \[boolean OldUtil\])</span><span class="sxs-lookup"><span data-stu-id="d3325-142">public TreeNode getDocNode(UtilFileType helpType, int UtilType, str Name, \[UtilElementId ParentId\], \[int Type\], \[UtilEntryLevel UtilLevel\], \[boolean ForceLevel\], \[int Mode\], \[boolean OldUtil\])</span></span> | <span data-ttu-id="d3325-143">AOT から指定したドキュメント ノードを取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-143">Retrieves the specified documentation nodes from the AOT.</span></span>                                                                                                                               |
| <span data-ttu-id="d3325-144">public TreeNode getImportedNode(int id, int utilfiletype, UtilElementType utiltype, str name, int fileposition, int Flag)</span><span class="sxs-lookup"><span data-stu-id="d3325-144">public TreeNode getImportedNode(int id, int utilfiletype, UtilElementType utiltype, str name, int fileposition, int Flag)</span></span>                                                                                    | <span data-ttu-id="d3325-145">XPO ファイルからツリー ノードのインスタンスを作成しますが、AOT にインポートしません。</span><span class="sxs-lookup"><span data-stu-id="d3325-145">Creates an instance of a tree node from an XPO file but does not import it into the AOT.</span></span> <span data-ttu-id="d3325-146">たとえば、これにより、同じツリー ノードの別のバージョンと比較できます。</span><span class="sxs-lookup"><span data-stu-id="d3325-146">For example, this allows you to compare it with another version of the same tree node.</span></span>         |
| <span data-ttu-id="d3325-147">public TreeNode getNode(UtilElementType UtilType, str Name, \[UtilElementId ParentId\], \[int Type\], \[UtilEntryLevel Utillevel\], \[boolean Forcelevel\], \[int Mode\], \[boolean OldUtil\])</span><span class="sxs-lookup"><span data-stu-id="d3325-147">public TreeNode getNode(UtilElementType UtilType, str Name, \[UtilElementId ParentId\], \[int Type\], \[UtilEntryLevel Utillevel\], \[boolean Forcelevel\], \[int Mode\], \[boolean OldUtil\])</span></span>               | <span data-ttu-id="d3325-148">AOT 内のノードに対応するツリー ノードを取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-148">Retrieves a tree node that corresponds to a node in the AOT.</span></span>                                                                                                                            |
| <span data-ttu-id="d3325-149">public int getNodeResid(UtilElementType nodeType)</span><span class="sxs-lookup"><span data-stu-id="d3325-149">public int getNodeResid(UtilElementType nodeType)</span></span>                                                                                                                                                            | <span data-ttu-id="d3325-150">指定したタイプのノードを表示するために使用されるアイコンのリソース ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-150">Retrieves the resource ID for the icon that is used to display nodes of the specified type.</span></span>                                                                                             |
| <span data-ttu-id="d3325-151">public Struct getTaskInfo(int taskNumber)</span><span class="sxs-lookup"><span data-stu-id="d3325-151">public Struct getTaskInfo(int taskNumber)</span></span>                                                                                                                                                                    |                                                                                                                                                                                         |
| <span data-ttu-id="d3325-152">public UserSetup getUserSetup()</span><span class="sxs-lookup"><span data-stu-id="d3325-152">public UserSetup getUserSetup()</span></span>                                                                                                                                                                              | <span data-ttu-id="d3325-153">ユーザー パラメーターを設定するために使用する UserSetup オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-153">Retrieves a UserSetup object that is used to set user parameters.</span></span>                                                                                                                       |
| <span data-ttu-id="d3325-154">public container getWorkspaceList()</span><span class="sxs-lookup"><span data-stu-id="d3325-154">public container getWorkspaceList()</span></span>                                                                                                                                                                          |                                                                                                                                                                                         |
| <span data-ttu-id="d3325-155">public int hWnd(\[int workspaceNum\])</span><span class="sxs-lookup"><span data-stu-id="d3325-155">public int hWnd(\[int workspaceNum\])</span></span>                                                                                                                                                                        | <span data-ttu-id="d3325-156">ナビゲーション ペイン ウィンドウのハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-156">Retrieves a handle to the Navigation Pane window.</span></span>                                                                                                                  |
| <span data-ttu-id="d3325-157">public boolean import(container infologContainer, \[boolean clearExistingInfolog\])</span><span class="sxs-lookup"><span data-stu-id="d3325-157">public boolean import(container infologContainer, \[boolean clearExistingInfolog\])</span></span>                                                                                                                          |                                                                                                                                                                                         |
| <span data-ttu-id="d3325-158">public int importElement(int id, int utilfiletype, UtilElementType utiltype, str name, int fileposition, int Flag)</span><span class="sxs-lookup"><span data-stu-id="d3325-158">public int importElement(int id, int utilfiletype, UtilElementType utiltype, str name, int fileposition, int Flag)</span></span>                                                                                           | <span data-ttu-id="d3325-159">インポートする対象を指定します。</span><span class="sxs-lookup"><span data-stu-id="d3325-159">Specifies the object to be imported.</span></span>                                                                                                                                                    |
| <span data-ttu-id="d3325-160">public int importString(str source, UtilElementType kind, str name)</span><span class="sxs-lookup"><span data-stu-id="d3325-160">public int importString(str source, UtilElementType kind, str name)</span></span>                                                                                                                                          | <span data-ttu-id="d3325-161">ファイルからオブジェクトをインポートします。</span><span class="sxs-lookup"><span data-stu-id="d3325-161">Imports an object from a file.</span></span>                                                                                                                                                          |
| <span data-ttu-id="d3325-162">public int instance()</span><span class="sxs-lookup"><span data-stu-id="d3325-162">public int instance()</span></span>                                                                                                                                                                                        | <span data-ttu-id="d3325-163">アプリケーションの現在のインスタンスへのハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-163">Retrieves a handle to the current instance of the application.</span></span>                                                                                                                          |
| <span data-ttu-id="d3325-164">public str isoCurrencyCode(\[str code\])</span><span class="sxs-lookup"><span data-stu-id="d3325-164">public str isoCurrencyCode(\[str code\])</span></span>                                                                                                                                                                     | <span data-ttu-id="d3325-165">通貨コードを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d3325-165">Gets or sets the currency code.</span></span>                                                                                                                                                         |
| <span data-ttu-id="d3325-166">public boolean IsVisible()</span><span class="sxs-lookup"><span data-stu-id="d3325-166">public boolean IsVisible()</span></span>                                                                                                                                                                                   | <span data-ttu-id="d3325-167">クライアントのウィンドウが最小化されていないかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d3325-167">Determines whether the client window is not minimized.</span></span>                                                                                                                                  |
| <span data-ttu-id="d3325-168">public str language(\[str languageCode\])</span><span class="sxs-lookup"><span data-stu-id="d3325-168">public str language(\[str languageCode\])</span></span>                                                                                                                                                                    | <span data-ttu-id="d3325-169">GUI の言語を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d3325-169">Gets or sets the language for the GUI.</span></span>                                                                                                                                                  |
| <span data-ttu-id="d3325-170">public Exception level(int line)</span><span class="sxs-lookup"><span data-stu-id="d3325-170">public Exception level(int line)</span></span>                                                                                                                                                                             | <span data-ttu-id="d3325-171">情報ログ バッファー内の行の例外レベルを取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-171">Retrieves the exception level of a line in the Infolog buffer.</span></span>                                                                                                                          |
| <span data-ttu-id="d3325-172">public int line()</span><span class="sxs-lookup"><span data-stu-id="d3325-172">public int line()</span></span>                                                                                                                                                                                            | <span data-ttu-id="d3325-173">情報ログ バッファの明細行の数を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-173">Retrieves the number of lines in the Infolog buffer.</span></span>                                                                                                                                    |
| <span data-ttu-id="d3325-174">public MessageWin messageWin()</span><span class="sxs-lookup"><span data-stu-id="d3325-174">public MessageWin messageWin()</span></span>                                                                                                                                                                               | <span data-ttu-id="d3325-175">Infolog から Message ウィンドウに出力を送信できます。</span><span class="sxs-lookup"><span data-stu-id="d3325-175">Enables you to send output from the Infolog to the Message window.</span></span>                                                                                                                      |
| <span data-ttu-id="d3325-176">public Real nationalCurrencyFactor(\[Real factor\])</span><span class="sxs-lookup"><span data-stu-id="d3325-176">public Real nationalCurrencyFactor(\[Real factor\])</span></span>                                                                                                                                                          |                                                                                                                                                                                         |
| <span data-ttu-id="d3325-177">public str nationalCurrencyPostfix(\[str string\])</span><span class="sxs-lookup"><span data-stu-id="d3325-177">public str nationalCurrencyPostfix(\[str string\])</span></span>                                                                                                                                                           |                                                                                                                                                                                         |
| <span data-ttu-id="d3325-178">public str nationalCurrencyPrefix(\[str string\])</span><span class="sxs-lookup"><span data-stu-id="d3325-178">public str nationalCurrencyPrefix(\[str string\])</span></span>                                                                                                                                                            |                                                                                                                                                                                         |
| <span data-ttu-id="d3325-179">public xNavPane navPane()</span><span class="sxs-lookup"><span data-stu-id="d3325-179">public xNavPane navPane()</span></span>                                                                                                                                                                                    | <span data-ttu-id="d3325-180">プライマリ ナビゲーション コントロール クラスの xNavPane オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-180">Retrieves an xNavPane object, the primary navigation control class.</span></span>                                                                                                                     |
| <span data-ttu-id="d3325-181">public int num(\[Exception exceptionType\])</span><span class="sxs-lookup"><span data-stu-id="d3325-181">public int num(\[Exception exceptionType\])</span></span>                                                                                                                                                                  | <span data-ttu-id="d3325-182">情報ログ バッファにおける指定した型の例外の数を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-182">Retrieves the number of exceptions of the specified type in the Infolog buffer.</span></span>                                                                                                         |
| <span data-ttu-id="d3325-183">public int prevInstance()</span><span class="sxs-lookup"><span data-stu-id="d3325-183">public int prevInstance()</span></span>                                                                                                                                                                                    | <span data-ttu-id="d3325-184">アプリケーションの前のインスタンスへのハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-184">Retrieves a handle to the previous instance of the application.</span></span>                                                                                                                         |
| <span data-ttu-id="d3325-185">public int processId()</span><span class="sxs-lookup"><span data-stu-id="d3325-185">public int processId()</span></span>                                                                                                                                                                                       | <span data-ttu-id="d3325-186">プロセスの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-186">Retrieves the ID for the process.</span></span>                                                                                                                                 |
| <span data-ttu-id="d3325-187">public TreeNode projectRootNode()</span><span class="sxs-lookup"><span data-stu-id="d3325-187">public TreeNode projectRootNode()</span></span>                                                                                                                                                                            | <span data-ttu-id="d3325-188">X++ プロジェクト ノードを返します。</span><span class="sxs-lookup"><span data-stu-id="d3325-188">Returns the X++ Projects node.</span></span>                                                                                                                                                          |
| <span data-ttu-id="d3325-189">public TreeNode rootNode()</span><span class="sxs-lookup"><span data-stu-id="d3325-189">public TreeNode rootNode()</span></span>                                                                                                                                                                                   | <span data-ttu-id="d3325-190">アプリケーション オブジェクト ツリーのルートを取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-190">Retrieves the root of the application object tree.</span></span>                                                                                                                                      |
| <span data-ttu-id="d3325-191">public int startImport(str file, int flag, \[str labelSubstitutes\])</span><span class="sxs-lookup"><span data-stu-id="d3325-191">public int startImport(str file, int flag, \[str labelSubstitutes\])</span></span>                                                                                                                                         | <span data-ttu-id="d3325-192">インポート コンテキストを作成します。</span><span class="sxs-lookup"><span data-stu-id="d3325-192">Creates an import context.</span></span>                                                                                                                                                              |
| <span data-ttu-id="d3325-193">public str text(\[int line\])</span><span class="sxs-lookup"><span data-stu-id="d3325-193">public str text(\[int line\])</span></span>                                                                                                                                                                                | <span data-ttu-id="d3325-194">情報ログからテキストの行を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-194">Retrieves a line of text from the Infolog.</span></span>                                                                                                                                              |
| <span data-ttu-id="d3325-195">public TreeNode userNode()</span><span class="sxs-lookup"><span data-stu-id="d3325-195">public TreeNode userNode()</span></span>                                                                                                                                                                                   |                                                                                                                                                                                         |
| <span data-ttu-id="d3325-196">public AnyType webSession(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="d3325-196">public AnyType webSession(\[AnyType value\])</span></span>                                                                                                                                                                 |                                                                                                                                                                                         |
| <span data-ttu-id="d3325-197">::public static container activeXControls()</span><span class="sxs-lookup"><span data-stu-id="d3325-197">::public static container activeXControls()</span></span>                                                                                                                                                                  | <span data-ttu-id="d3325-198">ActiveX コントロールの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-198">Retrieves a list of the ActiveX controls.</span></span>                                                                                                             |
| <span data-ttu-id="d3325-199">::public static str AOTLogDirectory()</span><span class="sxs-lookup"><span data-stu-id="d3325-199">::public static str AOTLogDirectory()</span></span>                                                                                                                                                                        | <span data-ttu-id="d3325-200">現在のインストールのログ ディレクトリへのパスを取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-200">Gets the path to the log directory for the current installation.</span></span>                                                                                                                        |
| <span data-ttu-id="d3325-201">::public static container automationObjects()</span><span class="sxs-lookup"><span data-stu-id="d3325-201">::public static container automationObjects()</span></span>                                                                                                                                                                | <span data-ttu-id="d3325-202">使用可能な COM オブジェクトの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-202">Retrieves the list of COM objects that are available.</span></span>                                                                                                          |
| <span data-ttu-id="d3325-203">::public static str buildNo()</span><span class="sxs-lookup"><span data-stu-id="d3325-203">::public static str buildNo()</span></span>                                                                                                                                                                                | <span data-ttu-id="d3325-204">現在の実行可能ファイルのカーネル ビルド番号を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-204">Retrieves the kernel build number of the current executable.</span></span>                                                                                                      |
| <span data-ttu-id="d3325-205">::public static str compilationDate()</span><span class="sxs-lookup"><span data-stu-id="d3325-205">::public static str compilationDate()</span></span>                                                                                                                                                                        | <span data-ttu-id="d3325-206">現在のバージョンが最後にコンパイルされた日付を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-206">Retrieves the date on which the current version was last compiled.</span></span>                                                                                             |
| <span data-ttu-id="d3325-207">::public static str compilationTime()</span><span class="sxs-lookup"><span data-stu-id="d3325-207">::public static str compilationTime()</span></span>                                                                                                                                                                        | <span data-ttu-id="d3325-208">現在のバージョンが最後にコンパイルされた時刻を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-208">Retrieves the time at which the current version was last compiled.</span></span>                                                                                             |
| <span data-ttu-id="d3325-209">::public static str componentName()</span><span class="sxs-lookup"><span data-stu-id="d3325-209">::public static str componentName()</span></span>                                                                                                                                                                          | <span data-ttu-id="d3325-210">コンポーネントへのパスを取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-210">Retrieves the path to the component.</span></span>                                                                                                                                                    |
| <span data-ttu-id="d3325-211">::public static str configuration()</span><span class="sxs-lookup"><span data-stu-id="d3325-211">::public static str configuration()</span></span>                                                                                                                                                                          | <span data-ttu-id="d3325-212">現在のクライアント構成を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-212">Retrieves the current client configuration.</span></span>                                                                                                                                             |
| <span data-ttu-id="d3325-213">::public static int currentWorkspaceNum()</span><span class="sxs-lookup"><span data-stu-id="d3325-213">::public static int currentWorkspaceNum()</span></span>                                                                                                                                                                    | <span data-ttu-id="d3325-214">現在のワークスペースのアプリケーション ウィンドウ ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-214">Retrieves the application window ID of the current workspace.</span></span>                                                                                                                           |
| <span data-ttu-id="d3325-215">::public static str directory(DirectoryType type)</span><span class="sxs-lookup"><span data-stu-id="d3325-215">::public static str directory(DirectoryType type)</span></span>                                                                                                                                                            | <span data-ttu-id="d3325-216">クライアントがインストールされているディレクトリへのパスを取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-216">Retrieves the path to the directory where the client has been installed.</span></span>                                                                                          |
| <span data-ttu-id="d3325-217">::public static Date expireDate()</span><span class="sxs-lookup"><span data-stu-id="d3325-217">::public static Date expireDate()</span></span>                                                                                                                                                                            | <span data-ttu-id="d3325-218">現在のインストールのライセンスの有効期限が切れる日付を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-218">Retrieves the date on which the license for the current installation expires.</span></span>                                                                                                           |
| <span data-ttu-id="d3325-219">::public static ApplicationObjectTreeWindow getApplicationObjectTreeWindow()</span><span class="sxs-lookup"><span data-stu-id="d3325-219">::public static ApplicationObjectTreeWindow getApplicationObjectTreeWindow()</span></span>                                                                                                                                 |                                                                                                                                                                                         |
| <span data-ttu-id="d3325-220">::public static int getCurrentModelId()</span><span class="sxs-lookup"><span data-stu-id="d3325-220">::public static int getCurrentModelId()</span></span>                                                                                                                                                                      |                                                                                                                                                                                         |
| <span data-ttu-id="d3325-221">::public static int getNumberOfDecimals(Real number)</span><span class="sxs-lookup"><span data-stu-id="d3325-221">::public static int getNumberOfDecimals(Real number)</span></span>                                                                                                                                                         | <span data-ttu-id="d3325-222">指定された数値の小数点以下の桁数を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-222">Retrieves the number of decimal places in the specified number.</span></span>                                                                                                                         |
| <span data-ttu-id="d3325-223">::public static PropertiesWindow getPropertiesWindow()</span><span class="sxs-lookup"><span data-stu-id="d3325-223">::public static PropertiesWindow getPropertiesWindow()</span></span>                                                                                                                                                       |                                                                                                                                                                                         |
| <span data-ttu-id="d3325-224">::public static int getSystemGeneratedModelId(UtilEntryLevel layer)</span><span class="sxs-lookup"><span data-stu-id="d3325-224">::public static int getSystemGeneratedModelId(UtilEntryLevel layer)</span></span>                                                                                                                                          |                                                                                                                                                                                         |
| <span data-ttu-id="d3325-225">::public static str licenseName()</span><span class="sxs-lookup"><span data-stu-id="d3325-225">::public static str licenseName()</span></span>                                                                                                                                                                            | <span data-ttu-id="d3325-226">現在のライセンスの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-226">Retrieves the name of the current license.</span></span>                                                                                                                        |
| <span data-ttu-id="d3325-227">::public static str productName()</span><span class="sxs-lookup"><span data-stu-id="d3325-227">::public static str productName()</span></span>                                                                                                                                                                            | <span data-ttu-id="d3325-228">製品の名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-228">Retrieves the name of the product.</span></span>                                                                                                                                                      |
| <span data-ttu-id="d3325-229">::public static str productRegisteredName()</span><span class="sxs-lookup"><span data-stu-id="d3325-229">::public static str productRegisteredName()</span></span>                                                                                                                                                                  |                                                                                                                                                                                         |
| <span data-ttu-id="d3325-230">::public static str releaseVersion()</span><span class="sxs-lookup"><span data-stu-id="d3325-230">::public static str releaseVersion()</span></span>                                                                                                                                                                         | <span data-ttu-id="d3325-231">現在の実行可能ファイルのバージョン番号を取得します。例: 3.0、4.0。</span><span class="sxs-lookup"><span data-stu-id="d3325-231">Retrieves the version number of the current executable; for example: 3.0, or 4.0.</span></span>                                                                                 |
| <span data-ttu-id="d3325-232">::public static str releaseYear()</span><span class="sxs-lookup"><span data-stu-id="d3325-232">::public static str releaseYear()</span></span>                                                                                                                                                                            |                                                                                                                                                                                         |
| <span data-ttu-id="d3325-233">::public static str serialNo()</span><span class="sxs-lookup"><span data-stu-id="d3325-233">::public static str serialNo()</span></span>                                                                                                                                                                               | <span data-ttu-id="d3325-234">現在のライセンスのシリアル番号を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-234">Retrieves the serial number of the current license.</span></span>                                                                                                               |
| <span data-ttu-id="d3325-235">public void new()</span><span class="sxs-lookup"><span data-stu-id="d3325-235">public void new()</span></span>                                                                                                                                                                                            | <span data-ttu-id="d3325-236">新しい xInfo オブジェクトを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d3325-236">Initializes a new xInfo object.</span></span>                                                                                                                                                         |
| <span data-ttu-id="d3325-237">public void workspaceWindowDestroyed(int hWnd)</span><span class="sxs-lookup"><span data-stu-id="d3325-237">public void workspaceWindowDestroyed(int hWnd)</span></span>                                                                                                                                                               | <span data-ttu-id="d3325-238">新しいワークスペースが終了した時に実行します。</span><span class="sxs-lookup"><span data-stu-id="d3325-238">Executes when a workspace is closed.</span></span>                                                                                                                                                    |
| <span data-ttu-id="d3325-239">public void writeCustomStatlineItem(str text)</span><span class="sxs-lookup"><span data-stu-id="d3325-239">public void writeCustomStatlineItem(str text)</span></span>                                                                                                                                                                | <span data-ttu-id="d3325-240">テキストの行をステータス バーに記述します。</span><span class="sxs-lookup"><span data-stu-id="d3325-240">Writes a line of text to the status bar.</span></span>                                                                                                                                                |
| <span data-ttu-id="d3325-241">public void reloadRunningMode()</span><span class="sxs-lookup"><span data-stu-id="d3325-241">public void reloadRunningMode()</span></span>                                                                                                                                                                              |                                                                                                                                                                                         |
| <span data-ttu-id="d3325-242">public void setWindowOrder(int window, \[int afterWindow\])</span><span class="sxs-lookup"><span data-stu-id="d3325-242">public void setWindowOrder(int window, \[int afterWindow\])</span></span>                                                                                                                                                  | <span data-ttu-id="d3325-243">Windows の表示順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="d3325-243">Sets the order in which windows should be displayed.</span></span>                                                                                                                                    |
| <span data-ttu-id="d3325-244">public void shutDown(boolean force)</span><span class="sxs-lookup"><span data-stu-id="d3325-244">public void shutDown(boolean force)</span></span>                                                                                                                                                                          | <span data-ttu-id="d3325-245">クライアントをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="d3325-245">Shuts down the client.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="d3325-246">public void xref(str path, xRef x)</span><span class="sxs-lookup"><span data-stu-id="d3325-246">public void xref(str path, xRef x)</span></span>                                                                                                                                                                           | <span data-ttu-id="d3325-247">相互参照システムが使用される時に実行します。</span><span class="sxs-lookup"><span data-stu-id="d3325-247">Executes when the cross-reference system is used.</span></span>                                                                                                                                       |
| <span data-ttu-id="d3325-248">public void updateCurrentCompany()</span><span class="sxs-lookup"><span data-stu-id="d3325-248">public void updateCurrentCompany()</span></span>                                                                                                                                                                           |                                                                                                                                                                                         |
| <span data-ttu-id="d3325-249">public void redrawAllWindows()</span><span class="sxs-lookup"><span data-stu-id="d3325-249">public void redrawAllWindows()</span></span>                                                                                                                                                                               | <span data-ttu-id="d3325-250">すべてのウィンドウを再描画します。</span><span class="sxs-lookup"><span data-stu-id="d3325-250">Redraws all windows.</span></span>                                                                                                                                                                    |
| <span data-ttu-id="d3325-251">public void formNotify(xFormRun form, FormNotify notification, \[FormNotifyEventArgs formNotifyEventArgs\])</span><span class="sxs-lookup"><span data-stu-id="d3325-251">public void formNotify(xFormRun form, FormNotify notification, \[FormNotifyEventArgs formNotifyEventArgs\])</span></span>                                                                                                  | <span data-ttu-id="d3325-252">特定フォームへの変更特定タイプに基づいて実行し、カスタムコードの実行を許可します。</span><span class="sxs-lookup"><span data-stu-id="d3325-252">Executes based on a particular type of change to a specific form, allowing custom code to run.</span></span>                                                                                          |
| <span data-ttu-id="d3325-253">public void mayReloadMenu(boolean value)</span><span class="sxs-lookup"><span data-stu-id="d3325-253">public void mayReloadMenu(boolean value)</span></span>                                                                                                                                                                     | <span data-ttu-id="d3325-254">UI を更新できないようにする</span><span class="sxs-lookup"><span data-stu-id="d3325-254">Prevents the UI from refreshing.</span></span>                                                                                                                                                        |
| <span data-ttu-id="d3325-255">public void startLengthyOperation()</span><span class="sxs-lookup"><span data-stu-id="d3325-255">public void startLengthyOperation()</span></span>                                                                                                                                                                          | <span data-ttu-id="d3325-256">マウス カーソルをアイドルに設定します。</span><span class="sxs-lookup"><span data-stu-id="d3325-256">Sets the mouse cursor to idle.</span></span>                                                                                                                                                          |
| <span data-ttu-id="d3325-257">public void breakpointNotify(BreakpointNotify notification)</span><span class="sxs-lookup"><span data-stu-id="d3325-257">public void breakpointNotify(BreakpointNotify notification)</span></span>                                                                                                                                                  | <span data-ttu-id="d3325-258">ブレークポイントが変更されたときの通知システムを実装します。</span><span class="sxs-lookup"><span data-stu-id="d3325-258">Implements a notification system when a breakpoint is changed.</span></span>                                                                                                                          |
| <span data-ttu-id="d3325-259">public void initializeInfolog(int window)</span><span class="sxs-lookup"><span data-stu-id="d3325-259">public void initializeInfolog(int window)</span></span>                                                                                                                                                                    |                                                                                                                                                                                         |
| <span data-ttu-id="d3325-260">public void startup(str startupCmd)</span><span class="sxs-lookup"><span data-stu-id="d3325-260">public void startup(str startupCmd)</span></span>                                                                                                                                                                          | <span data-ttu-id="d3325-261">クライアントの起動時に実行します。</span><span class="sxs-lookup"><span data-stu-id="d3325-261">Executes when the client starts.</span></span>                                                                                                                                                        |
| <span data-ttu-id="d3325-262">public void endImport(int id, int elements)</span><span class="sxs-lookup"><span data-stu-id="d3325-262">public void endImport(int id, int elements)</span></span>                                                                                                                                                                  | <span data-ttu-id="d3325-263">インポート プロセスを完了します。</span><span class="sxs-lookup"><span data-stu-id="d3325-263">Completes an import process.</span></span>                                                                                                                                                            |
| <span data-ttu-id="d3325-264">public void yield()</span><span class="sxs-lookup"><span data-stu-id="d3325-264">public void yield()</span></span>                                                                                                                                                                                          |                                                                                                                                                                                         |
| <span data-ttu-id="d3325-265">public void viewAlertInbox(\[int selectedTab\])</span><span class="sxs-lookup"><span data-stu-id="d3325-265">public void viewAlertInbox(\[int selectedTab\])</span></span>                                                                                                                                                              | <span data-ttu-id="d3325-266">警告の表示フォームを起動します。</span><span class="sxs-lookup"><span data-stu-id="d3325-266">Launches the View alerts form.</span></span>                                                                                                                                                          |
| <span data-ttu-id="d3325-267">public void reportSendMailServer(PrintJobSettings settings)</span><span class="sxs-lookup"><span data-stu-id="d3325-267">public void reportSendMailServer(PrintJobSettings settings)</span></span>                                                                                                                                                  |                                                                                                                                                                                         |
| <span data-ttu-id="d3325-268">public void endLengthyOperation(\[boolean endAll\])</span><span class="sxs-lookup"><span data-stu-id="d3325-268">public void endLengthyOperation(\[boolean endAll\])</span></span>                                                                                                                                                          | <span data-ttu-id="d3325-269">startLengthyOperation の呼び出し後にマウス カーソルが標準に戻るように設定します。</span><span class="sxs-lookup"><span data-stu-id="d3325-269">Sets the mouse cursor back to normal after a call to startLengthyOperation.</span></span>                                                                                                             |
| <span data-ttu-id="d3325-270">public void setNumUnreadAlerts(\[int n\])</span><span class="sxs-lookup"><span data-stu-id="d3325-270">public void setNumUnreadAlerts(\[int n\])</span></span>                                                                                                                                                                    | <span data-ttu-id="d3325-271">未読の警告メールの数が変わると、ステータス バーのテキストを更新します。</span><span class="sxs-lookup"><span data-stu-id="d3325-271">Refreshes the status bar text when the number of unread Alert e-mails changes.</span></span>                                                                                                          |
| <span data-ttu-id="d3325-272">public void truncate(str prefix)</span><span class="sxs-lookup"><span data-stu-id="d3325-272">public void truncate(str prefix)</span></span>                                                                                                                                                                             | <span data-ttu-id="d3325-273">情報ログから指定した接頭語の付いた品目を削除します。</span><span class="sxs-lookup"><span data-stu-id="d3325-273">Removes the items with the specified prefix from the Infolog.</span></span>                                                                                                                           |
| <span data-ttu-id="d3325-274">public void formNoteButton(boolean enable, boolean value)</span><span class="sxs-lookup"><span data-stu-id="d3325-274">public void formNoteButton(boolean enable, boolean value)</span></span>                                                                                                                                                    | <span data-ttu-id="d3325-275">ツールバーのドキュメント処理ボタンをコントロールします。</span><span class="sxs-lookup"><span data-stu-id="d3325-275">Controls the Document handling button on the toolbar.</span></span>                                                                                                                                   |
| <span data-ttu-id="d3325-276">public void viewCreateRuleDialog(xFormRun caller)</span><span class="sxs-lookup"><span data-stu-id="d3325-276">public void viewCreateRuleDialog(xFormRun caller)</span></span>                                                                                                                                                            | <span data-ttu-id="d3325-277">警告ルールの作成フォームを起動します。</span><span class="sxs-lookup"><span data-stu-id="d3325-277">Launches the Create alert rule form.</span></span>                                                                                                                                                    |
| <span data-ttu-id="d3325-278">public void view(\[container container\])</span><span class="sxs-lookup"><span data-stu-id="d3325-278">public void view(\[container container\])</span></span>                                                                                                                                                                    |                                                                                                                                                                                         |
| <span data-ttu-id="d3325-279">public void clear(\[int linesLeft\])</span><span class="sxs-lookup"><span data-stu-id="d3325-279">public void clear(\[int linesLeft\])</span></span>                                                                                                                                                                         | <span data-ttu-id="d3325-280">情報ログ バッファーから行を削除します。</span><span class="sxs-lookup"><span data-stu-id="d3325-280">Deletes lines from the Infolog buffer.</span></span>                                                                                                                                                  |
| <span data-ttu-id="d3325-281">public void workspaceWindowCreated(int hWnd)</span><span class="sxs-lookup"><span data-stu-id="d3325-281">public void workspaceWindowCreated(int hWnd)</span></span>                                                                                                                                                                 | <span data-ttu-id="d3325-282">新しいワークスペースが作成された時に実行します。</span><span class="sxs-lookup"><span data-stu-id="d3325-282">Executes when a new workspace is created.</span></span>                                                                                                                                               |
| <span data-ttu-id="d3325-283">::public static void setCurrentModelId(int currentModelId)</span><span class="sxs-lookup"><span data-stu-id="d3325-283">::public static void setCurrentModelId(int currentModelId)</span></span>                                                                                                                                                   |                                                                                                                                                                                         |
| <span data-ttu-id="d3325-284">public void activateMenubarTask(int command)</span><span class="sxs-lookup"><span data-stu-id="d3325-284">public void activateMenubarTask(int command)</span></span>                                                                                                                                                                 |                                                                                                                                                                                         |
| <span data-ttu-id="d3325-285">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="d3325-285">public void finalize()</span></span>                                                                                                                                                                                       |                                                                                                                                                                                         |
| <span data-ttu-id="d3325-286">public void insertXReferences()</span><span class="sxs-lookup"><span data-stu-id="d3325-286">public void insertXReferences()</span></span>                                                                                                                                                                              |                                                                                                                                                                                         |
| <span data-ttu-id="d3325-287">public void activateButton(int command)</span><span class="sxs-lookup"><span data-stu-id="d3325-287">public void activateButton(int command)</span></span>                                                                                                                                                                      |                                                                                                                                                                                         |
| <span data-ttu-id="d3325-288">public void activateWindow(int window)</span><span class="sxs-lookup"><span data-stu-id="d3325-288">public void activateWindow(int window)</span></span>                                                                                                                                                                       | <span data-ttu-id="d3325-289">フォームまたはウィンドウにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="d3325-289">Sets the focus on a form or Window.</span></span>                                                                                                                                                     |
| <span data-ttu-id="d3325-290">public void reportSendMail(PrintJobSettings settings)</span><span class="sxs-lookup"><span data-stu-id="d3325-290">public void reportSendMail(PrintJobSettings settings)</span></span>                                                                                                                                                        | <span data-ttu-id="d3325-291">レポートを電子メールで送信するための設定を生成します。</span><span class="sxs-lookup"><span data-stu-id="d3325-291">Generates the settings for sending a report by email.</span></span>                                                                                                                                   |

## <a name="method-removemessage"></a><span data-ttu-id="d3325-292">メソッド removeMessage</span><span class="sxs-lookup"><span data-stu-id="d3325-292">Method removeMessage</span></span>

```xpp
public int removeMessage(Int64 messageId)
```

### <a name="parameters---removemessage"></a><span data-ttu-id="d3325-293">パラメーター - removeMessage</span><span class="sxs-lookup"><span data-stu-id="d3325-293">Parameters - removeMessage</span></span>

<span data-ttu-id="d3325-294">messageId</span><span class="sxs-lookup"><span data-stu-id="d3325-294">messageId</span></span>  

### <a name="return-value---removemessage"></a><span data-ttu-id="d3325-295">戻り値 - removeMessage</span><span class="sxs-lookup"><span data-stu-id="d3325-295">Return Value - removeMessage</span></span>

## <a name="method-insertmessage"></a><span data-ttu-id="d3325-296">メソッド insertMessage</span><span class="sxs-lookup"><span data-stu-id="d3325-296">Method insertMessage</span></span>

```xpp
public Int64 insertMessage(MessageSeverity type, str message)
```

### <a name="parameters---insertmessage"></a><span data-ttu-id="d3325-297">パラメーター - insertMessage</span><span class="sxs-lookup"><span data-stu-id="d3325-297">Parameters - insertMessage</span></span>

<span data-ttu-id="d3325-298">タイプ</span><span class="sxs-lookup"><span data-stu-id="d3325-298">type</span></span>  

<!-- -->

<span data-ttu-id="d3325-299">メッセージ</span><span class="sxs-lookup"><span data-stu-id="d3325-299">message</span></span>  

### <a name="return-value---insertmessage"></a><span data-ttu-id="d3325-300">戻り値 - insertMessage</span><span class="sxs-lookup"><span data-stu-id="d3325-300">Return Value - insertMessage</span></span>

## <a name="method-add"></a><span data-ttu-id="d3325-301">メソッド add</span><span class="sxs-lookup"><span data-stu-id="d3325-301">Method add</span></span>

<span data-ttu-id="d3325-302">情報ログ バッファに文字列を追加します。</span><span class="sxs-lookup"><span data-stu-id="d3325-302">Adds a string to the Infolog buffer.</span></span>

```xpp
public Exception add(Exception exceptionType, str string, [str helpURL], [Object obj], [boolean buildprefix])
```

### <a name="parameters---add"></a><span data-ttu-id="d3325-303">パラメーター - add</span><span class="sxs-lookup"><span data-stu-id="d3325-303">Parameters - add</span></span>

<span data-ttu-id="d3325-304">exceptionType</span><span class="sxs-lookup"><span data-stu-id="d3325-304">exceptionType</span></span>  
<span data-ttu-id="d3325-305">オプションのパラメーター。情報ログ メッセージにコンテキストを提供するために使用される接頭語情報の生成を停止できます。</span><span class="sxs-lookup"><span data-stu-id="d3325-305">Optional parameter, that enables you to turn off the generation of prefix information that is used to provide context to Infolog messages.</span></span>

<!-- -->

<span data-ttu-id="d3325-306">string</span><span class="sxs-lookup"><span data-stu-id="d3325-306">string</span></span>  
<span data-ttu-id="d3325-307">オプションのパラメーター。情報ログ メッセージにコンテキストを提供するために使用される接頭語情報の生成を停止できます。</span><span class="sxs-lookup"><span data-stu-id="d3325-307">Optional parameter, that enables you to turn off the generation of prefix information that is used to provide context to Infolog messages.</span></span>

<!-- -->

<span data-ttu-id="d3325-308">helpURL</span><span class="sxs-lookup"><span data-stu-id="d3325-308">helpURL</span></span>  
<span data-ttu-id="d3325-309">オプションのパラメーター。情報ログ メッセージにコンテキストを提供するために使用される接頭語情報の生成を停止できます。</span><span class="sxs-lookup"><span data-stu-id="d3325-309">Optional parameter, that enables you to turn off the generation of prefix information that is used to provide context to Infolog messages.</span></span>

<!-- -->

<span data-ttu-id="d3325-310">obj</span><span class="sxs-lookup"><span data-stu-id="d3325-310">obj</span></span>  
<span data-ttu-id="d3325-311">オプションのパラメーター。情報ログ メッセージにコンテキストを提供するために使用される接頭語情報の生成を停止できます。</span><span class="sxs-lookup"><span data-stu-id="d3325-311">Optional parameter, that enables you to turn off the generation of prefix information that is used to provide context to Infolog messages.</span></span>

<!-- -->

<span data-ttu-id="d3325-312">buildprefix</span><span class="sxs-lookup"><span data-stu-id="d3325-312">buildprefix</span></span>  
<span data-ttu-id="d3325-313">オプションのパラメーター。情報ログ メッセージにコンテキストを提供するために使用される接頭語情報の生成を停止できます。</span><span class="sxs-lookup"><span data-stu-id="d3325-313">Optional parameter, that enables you to turn off the generation of prefix information that is used to provide context to Infolog messages.</span></span>

### <a name="return-value---add"></a><span data-ttu-id="d3325-314">戻り値 - add</span><span class="sxs-lookup"><span data-stu-id="d3325-314">Return Value - add</span></span>

<span data-ttu-id="d3325-315">例外システム列挙値です。</span><span class="sxs-lookup"><span data-stu-id="d3325-315">An Exception system enumeration value.</span></span> <span data-ttu-id="d3325-316">詳細については、「トライおよびキャッチ キーワードで例外処理」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d3325-316">For more information, see Exception Handling with try and catch Keywords.</span></span>

### <a name="remarks---add"></a><span data-ttu-id="d3325-317">備考 - add</span><span class="sxs-lookup"><span data-stu-id="d3325-317">Remarks - add</span></span>

<span data-ttu-id="d3325-318">helpURL パラメーターの値の例は、「KernDoc:\\\\\\\\ 機能 \\\\substr」です。</span><span class="sxs-lookup"><span data-stu-id="d3325-318">An example value for the helpURL parameter is 'KernDoc:\\\\\\\\Functions\\\\substr'.</span></span> <span data-ttu-id="d3325-319">このメソッドは直接使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="d3325-319">This method should not be used directly.</span></span> <span data-ttu-id="d3325-320">代わりに、infolog.info、infolog.warning、infolog.error、または infolog.checkFailed メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d3325-320">Instead, use the infolog.info, infolog.warning, infolog.error, or infolog.checkFailed method instead.</span></span> <span data-ttu-id="d3325-321">ExceptionType パラメーターの詳細については、トライおよびキャッチ キーワードで例外処理を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d3325-321">For more information about the exceptionType parameter, see Exception Handling with try and catch Keywords.</span></span>

## <a name="method-addexception"></a><span data-ttu-id="d3325-322">メソッド addException</span><span class="sxs-lookup"><span data-stu-id="d3325-322">Method addException</span></span>

```xpp
public Exception addException(str string, str stackTrace)
```

### <a name="parameters---addexception"></a><span data-ttu-id="d3325-323">パラメーター - addException</span><span class="sxs-lookup"><span data-stu-id="d3325-323">Parameters - addException</span></span>

<span data-ttu-id="d3325-324">文字列</span><span class="sxs-lookup"><span data-stu-id="d3325-324">string</span></span>  

<!-- -->

<span data-ttu-id="d3325-325">stackTrace</span><span class="sxs-lookup"><span data-stu-id="d3325-325">stackTrace</span></span>  

### <a name="return-value---addexception"></a><span data-ttu-id="d3325-326">戻り値 - addException</span><span class="sxs-lookup"><span data-stu-id="d3325-326">Return Value - addException</span></span>

## <a name="method-breakpoint"></a><span data-ttu-id="d3325-327">メソッド breakpoint</span><span class="sxs-lookup"><span data-stu-id="d3325-327">Method breakpoint</span></span>

<span data-ttu-id="d3325-328">ブレークポイントに関する情報を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d3325-328">Gets or sets information about breakpoints.</span></span>

```xpp
public container breakpoint([container breakpoint])
```

### <a name="parameters---breakpoint"></a><span data-ttu-id="d3325-329">パラメーター - breakpoint</span><span class="sxs-lookup"><span data-stu-id="d3325-329">Parameters - breakpoint</span></span>

<span data-ttu-id="d3325-330">ブレークポイント</span><span class="sxs-lookup"><span data-stu-id="d3325-330">breakpoint</span></span>  
<span data-ttu-id="d3325-331">現在のブレークポイントに関する情報を保持するコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="d3325-331">A container that holds information about the current breakpoints.</span></span>

### <a name="return-value---breakpoint"></a><span data-ttu-id="d3325-332">戻り値 - breakpoint</span><span class="sxs-lookup"><span data-stu-id="d3325-332">Return Value - breakpoint</span></span>

<span data-ttu-id="d3325-333">現在のブレークポイントに関する情報を保持するコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="d3325-333">A container holding information about the current breakpoints.</span></span>

### <a name="remarks---breakpoint"></a><span data-ttu-id="d3325-334">備考 - breakpoint</span><span class="sxs-lookup"><span data-stu-id="d3325-334">Remarks - breakpoint</span></span>

<span data-ttu-id="d3325-335">ブレークポイントに関する情報を保持するコンテナーの形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d3325-335">The container that holds information about breakpoints is of the format:</span></span>

-   <span data-ttu-id="d3325-336">項目 1: バージョン番号</span><span class="sxs-lookup"><span data-stu-id="d3325-336">Item 1: Version number</span></span>
-   <span data-ttu-id="d3325-337">項目 2 - 4、5-7、n - n+2: 以下で構成される各ブレークポイントに関する情報:</span><span class="sxs-lookup"><span data-stu-id="d3325-337">Items 2 - 4, 5-7, � n - n+2: Information about each breakpoint, consisting of:</span></span>

```xpp
-   the AOT path
-   the line number on which the breakpoint is set
-   whether the breakpoint is enabled or disabled
```

<span data-ttu-id="d3325-338">アプリケーションで、このメソッドはブレークポイント フォームで使用されます。</span><span class="sxs-lookup"><span data-stu-id="d3325-338">In the application, this method is used by the Breakpoints form.</span></span> <span data-ttu-id="d3325-339">このフォームは、開いているときに、フォームに対して getBreakpoints メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d3325-339">When the form is opened it calls the getBreakpoints method on the form.</span></span> <span data-ttu-id="d3325-340">これは、xInfo.breakpoint メソッドを呼び出し、ブレークポイント情報を持つコンテナーをパラメーターとして使用します。</span><span class="sxs-lookup"><span data-stu-id="d3325-340">This calls the xInfo.breakpoint method, and uses a container with the breakpoint information as a parameter.</span></span> <span data-ttu-id="d3325-341">ブレークポイントを無効にするとき、有効にするとき、またはフォームから削除するとき、setBreakpoints メソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d3325-341">When a breakpoint is disabled, enabled, or deleted from the form, the setBreakpoints method is called.</span></span> <span data-ttu-id="d3325-342">これにより、ブレークポイントに関する情報が更新され、ブレークポイント パラメーターを使用せずに xInfo.breakpoint メソッドを使用してコンテナーとして返されます。</span><span class="sxs-lookup"><span data-stu-id="d3325-342">This updates the information about the breakpoints and returns this as a container using the xInfo.breakpoint method without using the breakpoint parameter.</span></span> <span data-ttu-id="d3325-343">コンテナーは、コード エディター ウィンドウのブレークポイント情報を更新するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d3325-343">The container is used to update the breakpoint information in the Code Editor window.</span></span>

## <a name="method-canshowcreaterulemenuitem"></a><span data-ttu-id="d3325-344">メソッド canShowCreateRuleMenuItem</span><span class="sxs-lookup"><span data-stu-id="d3325-344">Method canShowCreateRuleMenuItem</span></span>

<span data-ttu-id="d3325-345">フォームの警告ルール作成フォームのメニュー項目を表示するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d3325-345">Determines whether the menu item for the Create alert rule form should be displayed for a form.</span></span>

```xpp
public boolean canShowCreateRuleMenuItem(xFormRun caller)
```

### <a name="parameters---canshowcreaterulemenuitem"></a><span data-ttu-id="d3325-346">パラメーター - canShowCreateRuleMenuItem</span><span class="sxs-lookup"><span data-stu-id="d3325-346">Parameters - canShowCreateRuleMenuItem</span></span>

<span data-ttu-id="d3325-347">caller</span><span class="sxs-lookup"><span data-stu-id="d3325-347">caller</span></span>  
<span data-ttu-id="d3325-348">現在のフォーム: 警告ルールの作成メニュー項目が表示されるフォーム。</span><span class="sxs-lookup"><span data-stu-id="d3325-348">The current form: the form from which the Create alert rule menu item can be displayed.</span></span>

### <a name="return-value---canshowcreaterulemenuitem"></a><span data-ttu-id="d3325-349">戻り値 - canShowCreateRuleMenuItem</span><span class="sxs-lookup"><span data-stu-id="d3325-349">Return Value - canShowCreateRuleMenuItem</span></span>

<span data-ttu-id="d3325-350">現在のフォームが警告の作成をサポートする場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="d3325-350">true if the current form supports the creation of alerts; otherwise false.</span></span>

## <a name="method-canshutdown"></a><span data-ttu-id="d3325-351">メソッド canShutdown</span><span class="sxs-lookup"><span data-stu-id="d3325-351">Method canShutdown</span></span>

<span data-ttu-id="d3325-352">システムをシャットダウンできるかどうかをテストします。</span><span class="sxs-lookup"><span data-stu-id="d3325-352">Tests whether the system can be shut down.</span></span> <span data-ttu-id="d3325-353">このメソッドを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="d3325-353">Do not use this method.</span></span> <span data-ttu-id="d3325-354">代わりに、Info クラスでオーバーライドされたバージョンを使用します。</span><span class="sxs-lookup"><span data-stu-id="d3325-354">Use the version that is overridden on the Info class instead.</span></span>

```xpp
public boolean canShutdown(boolean silent)
```

### <a name="parameters---canshutdown"></a><span data-ttu-id="d3325-355">パラメーター - canShutdown</span><span class="sxs-lookup"><span data-stu-id="d3325-355">Parameters - canShutdown</span></span>

<span data-ttu-id="d3325-356">silent</span><span class="sxs-lookup"><span data-stu-id="d3325-356">silent</span></span>  
<span data-ttu-id="d3325-357">ユーザーがシステムを終了したいか尋ねるかどうかを決定するブール値。</span><span class="sxs-lookup"><span data-stu-id="d3325-357">A Boolean that determines whether users are asked if they want to exit the system.</span></span>

### <a name="return-value---canshutdown"></a><span data-ttu-id="d3325-358">戻り値 - canShutdown</span><span class="sxs-lookup"><span data-stu-id="d3325-358">Return Value - canShutdown</span></span>

<span data-ttu-id="d3325-359">システムをシャットダウンすることができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d3325-359">true of the system can be shut down; otherwise false.</span></span>

## <a name="method-canviewalertinbox"></a><span data-ttu-id="d3325-360">メソッド canViewAlertInbox</span><span class="sxs-lookup"><span data-stu-id="d3325-360">Method canViewAlertInbox</span></span>

<span data-ttu-id="d3325-361">現在のユーザーに警告の表示フォームを表示するアクセス許可があるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="d3325-361">Determines whether the current user has permission to view the View alerts form.</span></span>

```xpp
public boolean canViewAlertInbox()
```

### <a name="return-value---canviewalertinbox"></a><span data-ttu-id="d3325-362">戻り値 - canViewAlertInbox</span><span class="sxs-lookup"><span data-stu-id="d3325-362">Return Value - canViewAlertInbox</span></span>

<span data-ttu-id="d3325-363">ユーザーがフォームを表示するためのアクセス許可を持つ場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d3325-363">true if the user has permission to view the form; otherwise, false.</span></span>

### <a name="remarks---canviewalertinbox"></a><span data-ttu-id="d3325-364">備考 - canViewAlertInbox</span><span class="sxs-lookup"><span data-stu-id="d3325-364">Remarks - canViewAlertInbox</span></span>

<span data-ttu-id="d3325-365">xInfo.viewAlertInbox を呼び出す前に、このメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d3325-365">Call this method before calling xInfo.viewAlertInbox.</span></span>

## <a name="method-compileroutput"></a><span data-ttu-id="d3325-366">メソッド compilerOutput</span><span class="sxs-lookup"><span data-stu-id="d3325-366">Method compilerOutput</span></span>

<span data-ttu-id="d3325-367">コンパイラ出力オブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d3325-367">Gets or sets the compiler output object.</span></span> <span data-ttu-id="d3325-368">コンパイラ出力オブジェクトは、デフォルトでコンパイラ出力ウィンドウです。</span><span class="sxs-lookup"><span data-stu-id="d3325-368">The compiler output object is the Compiler output window by default.</span></span>

```xpp
public xCompilerOutput compilerOutput([Object compilerOut])
```

### <a name="parameters---compileroutput"></a><span data-ttu-id="d3325-369">パラメーター - compilerOutput</span><span class="sxs-lookup"><span data-stu-id="d3325-369">Parameters - compilerOutput</span></span>

<span data-ttu-id="d3325-370">compilerOut</span><span class="sxs-lookup"><span data-stu-id="d3325-370">compilerOut</span></span>  
<span data-ttu-id="d3325-371">コンパイラ出力オブジェクト; オプション。</span><span class="sxs-lookup"><span data-stu-id="d3325-371">A compiler output object; optional.</span></span> <span data-ttu-id="d3325-372">オプションのパラメーター。</span><span class="sxs-lookup"><span data-stu-id="d3325-372">Optional parameter.</span></span>

### <a name="return-value---compileroutput"></a><span data-ttu-id="d3325-373">戻り値 - compilerOutput</span><span class="sxs-lookup"><span data-stu-id="d3325-373">Return Value - compilerOutput</span></span>

<span data-ttu-id="d3325-374">xCompilerOutput オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="d3325-374">An xCompilerOutput object.</span></span>

### <a name="remarks---compileroutput"></a><span data-ttu-id="d3325-375">備考 - compilerOutput</span><span class="sxs-lookup"><span data-stu-id="d3325-375">Remarks - compilerOutput</span></span>

<span data-ttu-id="d3325-376">compilerOut パラメーターの既定値は、コンパイラ出力ウィンドウですが、メッセージ ウィンドウでもあります。</span><span class="sxs-lookup"><span data-stu-id="d3325-376">The default value of the compilerOut parameter is the Compiler output window, but it can also be the Message window.</span></span>

## <a name="method-copy"></a><span data-ttu-id="d3325-377">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="d3325-377">Method copy</span></span>

<span data-ttu-id="d3325-378">情報ログ バッファーから行をコピーします。</span><span class="sxs-lookup"><span data-stu-id="d3325-378">Copies lines from the Infolog buffer.</span></span>

```xpp
public container copy(int from, int to)
```

### <a name="parameters---copy"></a><span data-ttu-id="d3325-379">パラメーター - copy</span><span class="sxs-lookup"><span data-stu-id="d3325-379">Parameters - copy</span></span>

<span data-ttu-id="d3325-380">投稿者</span><span class="sxs-lookup"><span data-stu-id="d3325-380">from</span></span>  
<span data-ttu-id="d3325-381">コピーする最後の行。</span><span class="sxs-lookup"><span data-stu-id="d3325-381">The last line to copy.</span></span>

<!-- -->

<span data-ttu-id="d3325-382">終了日</span><span class="sxs-lookup"><span data-stu-id="d3325-382">to</span></span>  
<span data-ttu-id="d3325-383">コピーする最後の行。</span><span class="sxs-lookup"><span data-stu-id="d3325-383">The last line to copy.</span></span>

### <a name="return-value---copy"></a><span data-ttu-id="d3325-384">戻り値 - copy</span><span class="sxs-lookup"><span data-stu-id="d3325-384">Return Value - copy</span></span>

<span data-ttu-id="d3325-385">開始日と終了の間の情報ログ行を含むコンテナー。</span><span class="sxs-lookup"><span data-stu-id="d3325-385">Container that contains the Infolog lines between from and to.</span></span>

### <a name="examples---copy"></a><span data-ttu-id="d3325-386">例 - copy</span><span class="sxs-lookup"><span data-stu-id="d3325-386">Examples - copy</span></span>

<span data-ttu-id="d3325-387">次の例では、copy メソッドを使用して、情報ログの内容をログにコピーします。</span><span class="sxs-lookup"><span data-stu-id="d3325-387">The following example uses the copy method to copy the content of the Infolog into a log.</span></span>

```xpp
boolean validateRecord() 
{ 
    boolean     ok = true; 
    ok = intrastat.validateRecord(); 
    if (ok) 
        intrastat.log = ''; 
    else 
    { 
        intrastat.log = Info::infoCon2Str( 
            infolog.copy(infoLogCounter+1,infolog.num())); 
        infoLogCounter = infolog.num(); 
        errorFound = true; 
    } 
    intrastat.update(); 
    return ok; 
}
```

## <a name="method-createdevelopmentworkspacewindow"></a><span data-ttu-id="d3325-388">メソッド createDevelopmentWorkspaceWindow</span><span class="sxs-lookup"><span data-stu-id="d3325-388">Method createDevelopmentWorkspaceWindow</span></span>

```xpp
public int createDevelopmentWorkspaceWindow()
```

### <a name="return-value---createdevelopmentworkspacewindow"></a><span data-ttu-id="d3325-389">戻り値 - createDevelopmentWorkspaceWindow</span><span class="sxs-lookup"><span data-stu-id="d3325-389">Return Value - createDevelopmentWorkspaceWindow</span></span>

## <a name="method-createworkspacewindow"></a><span data-ttu-id="d3325-390">メソッド createWorkspaceWindow</span><span class="sxs-lookup"><span data-stu-id="d3325-390">Method createWorkspaceWindow</span></span>

<span data-ttu-id="d3325-391">新しいワークスペース ウィンドウを開きます。</span><span class="sxs-lookup"><span data-stu-id="d3325-391">Opens a new workspace window.</span></span> <span data-ttu-id="d3325-392">たとえば、これにより、異なるウィンドウでアプリケーション オブジェクトの異なるセットを開く、または会社コードの 2 つの異なるセットを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="d3325-392">For example, this enables you to open different sets of application objects in different windows, or to work with two different sets of company accounts.</span></span>

```xpp
public int createWorkspaceWindow()
```

### <a name="return-value---createworkspacewindow"></a><span data-ttu-id="d3325-393">戻り値 - createWorkspaceWindow</span><span class="sxs-lookup"><span data-stu-id="d3325-393">Return Value - createWorkspaceWindow</span></span>

<span data-ttu-id="d3325-394">新規のウィンドウにハンドルを返します。</span><span class="sxs-lookup"><span data-stu-id="d3325-394">Returns a handle to the new window.</span></span>

## <a name="method-currentaolayer"></a><span data-ttu-id="d3325-395">メソッド currentAOLayer</span><span class="sxs-lookup"><span data-stu-id="d3325-395">Method currentAOLayer</span></span>

<span data-ttu-id="d3325-396">SYS または USR などで実行している現在の階層を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-396">Retrieves the current layer you are running in such as SYS, or USR.</span></span>

```xpp
public UtilEntryLevel currentAOLayer()
```

### <a name="return-value---currentaolayer"></a><span data-ttu-id="d3325-397">戻り値 - currentAOLayer</span><span class="sxs-lookup"><span data-stu-id="d3325-397">Return Value - currentAOLayer</span></span>

<span data-ttu-id="d3325-398">作業中の現在のレイヤーを示す UtilEntryLevel システム列挙値。</span><span class="sxs-lookup"><span data-stu-id="d3325-398">A UtilEntryLevel system enumeration value that indicates the current layer you are working in.</span></span>

### <a name="remarks---currentaolayer"></a><span data-ttu-id="d3325-399">備考 - currentAOLayer</span><span class="sxs-lookup"><span data-stu-id="d3325-399">Remarks - currentAOLayer</span></span>

<span data-ttu-id="d3325-400">詳細については、「レイヤー」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d3325-400">For more information, see Layers.</span></span>

## <a name="method-cut"></a><span data-ttu-id="d3325-401">メソッド cut</span><span class="sxs-lookup"><span data-stu-id="d3325-401">Method cut</span></span>

<span data-ttu-id="d3325-402">情報ログ バッファーから行を切り取りします。</span><span class="sxs-lookup"><span data-stu-id="d3325-402">Cuts lines from the Infolog buffer.</span></span>

```xpp
public container cut(int from, int to)
```

### <a name="parameters---cut"></a><span data-ttu-id="d3325-403">パラメーター - cut</span><span class="sxs-lookup"><span data-stu-id="d3325-403">Parameters - cut</span></span>

<span data-ttu-id="d3325-404">投稿者</span><span class="sxs-lookup"><span data-stu-id="d3325-404">from</span></span>  
<span data-ttu-id="d3325-405">カットする最後の行。</span><span class="sxs-lookup"><span data-stu-id="d3325-405">The last line to cut.</span></span>

<!-- -->

<span data-ttu-id="d3325-406">終了日</span><span class="sxs-lookup"><span data-stu-id="d3325-406">to</span></span>  
<span data-ttu-id="d3325-407">カットする最後の行。</span><span class="sxs-lookup"><span data-stu-id="d3325-407">The last line to cut.</span></span>

### <a name="return-value---cut"></a><span data-ttu-id="d3325-408">戻り値 - cut</span><span class="sxs-lookup"><span data-stu-id="d3325-408">Return Value - cut</span></span>

<span data-ttu-id="d3325-409">「～から」と「～へ」のパラメーターで指定された行の間の情報ログ行を保持するコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="d3325-409">A container that contains the Infolog lines between the lines specified by the from and to parameters.</span></span>

### <a name="examples---cut"></a><span data-ttu-id="d3325-410">例 - cut</span><span class="sxs-lookup"><span data-stu-id="d3325-410">Examples - cut</span></span>

<span data-ttu-id="d3325-411">次の例では、fromLine 値で指定された行から最後の行まで Infolog の行を切り取ります。</span><span class="sxs-lookup"><span data-stu-id="d3325-411">The following example cuts the lines in the Infolog from the line specified by the fromLine value, up to the last line.</span></span>

```xpp
private void cutInfolog(int fromLine) 
{ 
    infolog.cut(fromLine+1, Global::infologLine()); 
}
```

## <a name="method-documentationlanguage"></a><span data-ttu-id="d3325-412">メソッド documentationLanguage</span><span class="sxs-lookup"><span data-stu-id="d3325-412">Method documentationLanguage</span></span>

<span data-ttu-id="d3325-413">ドキュメントに使用される言語を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d3325-413">Gets or sets the language that is used for the documentation.</span></span>

```xpp
public str documentationLanguage([str languageCode])
```

### <a name="parameters---documentationlanguage"></a><span data-ttu-id="d3325-414">パラメーター - documentationLanguage</span><span class="sxs-lookup"><span data-stu-id="d3325-414">Parameters - documentationLanguage</span></span>

<span data-ttu-id="d3325-415">languageCode</span><span class="sxs-lookup"><span data-stu-id="d3325-415">languageCode</span></span>  
<span data-ttu-id="d3325-416">設定する言語の ID。オプション。</span><span class="sxs-lookup"><span data-stu-id="d3325-416">The ID of the language you want to set; optional.</span></span>

### <a name="return-value---documentationlanguage"></a><span data-ttu-id="d3325-417">戻り値 - documentationLanguage</span><span class="sxs-lookup"><span data-stu-id="d3325-417">Return Value - documentationLanguage</span></span>

<span data-ttu-id="d3325-418">ドキュメントに現在使用されている言語の ID。</span><span class="sxs-lookup"><span data-stu-id="d3325-418">The ID of the language that is currently used for the documentation.</span></span>

### <a name="remarks---documentationlanguage"></a><span data-ttu-id="d3325-419">備考 - documentationLanguage</span><span class="sxs-lookup"><span data-stu-id="d3325-419">Remarks - documentationLanguage</span></span>

<span data-ttu-id="d3325-420">GUI の言語を設定するには、xInfo.language メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d3325-420">Use the xInfo.language Method to set the language for the GUI.</span></span> <span data-ttu-id="d3325-421">特定のセッションのドキュメント言語を設定するには、xSession.documentationLanguage メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d3325-421">To set the documentation language for a particular session, use the xSession.documentationLanguage Method.</span></span> <span data-ttu-id="d3325-422">languageCode パラメーターの値の例は「en-us」で、英語 (US) の言語に設定されます。</span><span class="sxs-lookup"><span data-stu-id="d3325-422">An example value for the languageCode parameter is "en-us", which will set the language to US English.</span></span>

## <a name="method-export"></a><span data-ttu-id="d3325-423">メソッド export</span><span class="sxs-lookup"><span data-stu-id="d3325-423">Method export</span></span>

```xpp
public container export()
```

### <a name="return-value---export"></a><span data-ttu-id="d3325-424">戻り値 - export</span><span class="sxs-lookup"><span data-stu-id="d3325-424">Return Value - export</span></span>

## <a name="method-findnode"></a><span data-ttu-id="d3325-425">メソッド findNode</span><span class="sxs-lookup"><span data-stu-id="d3325-425">Method findNode</span></span>

<span data-ttu-id="d3325-426">指定されたツリー ノードを取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-426">Retrieves the specified a tree node.</span></span>

```xpp
public TreeNode findNode(str nodePath)
```

### <a name="parameters---findnode"></a><span data-ttu-id="d3325-427">パラメーター - findNode</span><span class="sxs-lookup"><span data-stu-id="d3325-427">Parameters - findNode</span></span>

<span data-ttu-id="d3325-428">nodePath</span><span class="sxs-lookup"><span data-stu-id="d3325-428">nodePath</span></span>  
<span data-ttu-id="d3325-429">ノードへのパスを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="d3325-429">A string that contains the path to the node.</span></span>

### <a name="return-value---findnode"></a><span data-ttu-id="d3325-430">戻り値 - findNode</span><span class="sxs-lookup"><span data-stu-id="d3325-430">Return Value - findNode</span></span>

<span data-ttu-id="d3325-431">nodePath パラメーターで指定されるツリー ノードを返します。</span><span class="sxs-lookup"><span data-stu-id="d3325-431">Returns the tree node that is specified by the nodePath parameter.</span></span>

### <a name="remarks---findnode"></a><span data-ttu-id="d3325-432">備考 - findNode</span><span class="sxs-lookup"><span data-stu-id="d3325-432">Remarks - findNode</span></span>

<span data-ttu-id="d3325-433"> メソッドは廃止されています。</span><span class="sxs-lookup"><span data-stu-id="d3325-433">This method is obsolete.</span></span> <span data-ttu-id="d3325-434">代わりに TreeNode::findNode メソッドを使用してください。</span><span class="sxs-lookup"><span data-stu-id="d3325-434">Use the TreeNode::findNode Method instead.</span></span>

## <a name="method-getdocnode"></a><span data-ttu-id="d3325-435">メソッド getDocNode</span><span class="sxs-lookup"><span data-stu-id="d3325-435">Method getDocNode</span></span>

<span data-ttu-id="d3325-436">AOT から指定したドキュメント ノードを取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-436">Retrieves the specified documentation nodes from the AOT.</span></span>

```xpp
public TreeNode getDocNode(UtilFileType helpType, int UtilType, str Name, [UtilElementId ParentId], [int Type], [UtilEntryLevel UtilLevel], [boolean ForceLevel], [int Mode], [boolean OldUtil])
```

### <a name="parameters---getdocnode"></a><span data-ttu-id="d3325-437">パラメーター - getDocNode</span><span class="sxs-lookup"><span data-stu-id="d3325-437">Parameters - getDocNode</span></span>

<span data-ttu-id="d3325-438">helpType</span><span class="sxs-lookup"><span data-stu-id="d3325-438">helpType</span></span>  
<span data-ttu-id="d3325-439">oldAOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d3325-439">A Boolean value that indicates whether to retrieve the node from the old AOT in the oldAOT folder.</span></span>

<!-- -->

<span data-ttu-id="d3325-440">UtilType</span><span class="sxs-lookup"><span data-stu-id="d3325-440">UtilType</span></span>  
<span data-ttu-id="d3325-441">oldAOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d3325-441">A Boolean value that indicates whether to retrieve the node from the old AOT in the oldAOT folder.</span></span>

<!-- -->

<span data-ttu-id="d3325-442">氏名</span><span class="sxs-lookup"><span data-stu-id="d3325-442">Name</span></span>  
<span data-ttu-id="d3325-443">oldAOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d3325-443">A Boolean value that indicates whether to retrieve the node from the old AOT in the oldAOT folder.</span></span>

<!-- -->

<span data-ttu-id="d3325-444">ParentId</span><span class="sxs-lookup"><span data-stu-id="d3325-444">ParentId</span></span>  
<span data-ttu-id="d3325-445">oldAOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d3325-445">A Boolean value that indicates whether to retrieve the node from the old AOT in the oldAOT folder.</span></span>

<!-- -->

<span data-ttu-id="d3325-446">種類</span><span class="sxs-lookup"><span data-stu-id="d3325-446">Type</span></span>  
<span data-ttu-id="d3325-447">oldAOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d3325-447">A Boolean value that indicates whether to retrieve the node from the old AOT in the oldAOT folder.</span></span>

<!-- -->

<span data-ttu-id="d3325-448">UtilLevel</span><span class="sxs-lookup"><span data-stu-id="d3325-448">UtilLevel</span></span>  
<span data-ttu-id="d3325-449">oldAOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d3325-449">A Boolean value that indicates whether to retrieve the node from the old AOT in the oldAOT folder.</span></span>

<!-- -->

<span data-ttu-id="d3325-450">ForceLevel</span><span class="sxs-lookup"><span data-stu-id="d3325-450">ForceLevel</span></span>  
<span data-ttu-id="d3325-451">oldAOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d3325-451">A Boolean value that indicates whether to retrieve the node from the old AOT in the oldAOT folder.</span></span>

<!-- -->

<span data-ttu-id="d3325-452">モード</span><span class="sxs-lookup"><span data-stu-id="d3325-452">Mode</span></span>  
<span data-ttu-id="d3325-453">oldAOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d3325-453">A Boolean value that indicates whether to retrieve the node from the old AOT in the oldAOT folder.</span></span>

<!-- -->

<span data-ttu-id="d3325-454">OldUtil</span><span class="sxs-lookup"><span data-stu-id="d3325-454">OldUtil</span></span>  
<span data-ttu-id="d3325-455">oldAOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d3325-455">A Boolean value that indicates whether to retrieve the node from the old AOT in the oldAOT folder.</span></span>

### <a name="return-value---getdocnode"></a><span data-ttu-id="d3325-456">戻り値 - getDocNode</span><span class="sxs-lookup"><span data-stu-id="d3325-456">Return Value - getDocNode</span></span>

<span data-ttu-id="d3325-457">AOT からのドキュメント ノードです。</span><span class="sxs-lookup"><span data-stu-id="d3325-457">A documentation node from the AOT.</span></span>

### <a name="remarks---getdocnode"></a><span data-ttu-id="d3325-458">備考 - getDocNode</span><span class="sxs-lookup"><span data-stu-id="d3325-458">Remarks - getDocNode</span></span>

<span data-ttu-id="d3325-459">helpType パラメーターの使用可能な値は、UtilFileType システム列挙の値です。</span><span class="sxs-lookup"><span data-stu-id="d3325-459">The possible values for the helpType parameter are values of the UtilFileType system enumeration:</span></span>

-   <span data-ttu-id="d3325-460">KernelHelp: システム ドキュメント ノード</span><span class="sxs-lookup"><span data-stu-id="d3325-460">KernelHelp: the System Documentation node</span></span>
-   <span data-ttu-id="d3325-461">ApplicationHelp: アプリケーション ドキュメント ノード</span><span class="sxs-lookup"><span data-stu-id="d3325-461">ApplicationHelp: the Application Documentation node</span></span>
-   <span data-ttu-id="d3325-462">ApplicationCodeDocumentation: アプリケーション開発者ドキュメント ノード。</span><span class="sxs-lookup"><span data-stu-id="d3325-462">ApplicationCodeDocumentation: the Application Developer Documentation node.</span></span>

<span data-ttu-id="d3325-463">utilType パラメーターの値の例は、システム ドキュメント ノード内の機能ノードです。</span><span class="sxs-lookup"><span data-stu-id="d3325-463">An example value of the utilType parameter is the Functions node within the System Documentation node.</span></span> <span data-ttu-id="d3325-464">ForceLevel パラメーターの既定値は false です。</span><span class="sxs-lookup"><span data-stu-id="d3325-464">The default value of the ForceLevel parameter is false.</span></span> <span data-ttu-id="d3325-465">False に設定され、指定されたレイヤーでコンテンツがない場合は、ノードはコンテンツを持つ次のレイヤーから取得されます。</span><span class="sxs-lookup"><span data-stu-id="d3325-465">If it is set to false, and there is no content in the layer specified, the node will be taken from the next layer below this that does have content.</span></span> <span data-ttu-id="d3325-466">true に設定され、レイヤーにコンテンツがない場合、メソッドは nullNothingnullptrunita null 参照 (Visual Basic 上ではなし) を返します。</span><span class="sxs-lookup"><span data-stu-id="d3325-466">If it is set to true, and there is no content in the layer, the method will return nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

## <a name="method-getimportednode"></a><span data-ttu-id="d3325-467">メソッド getImportedNode</span><span class="sxs-lookup"><span data-stu-id="d3325-467">Method getImportedNode</span></span>

<span data-ttu-id="d3325-468">XPO ファイルからツリー ノードのインスタンスを作成しますが、AOT にインポートしません。</span><span class="sxs-lookup"><span data-stu-id="d3325-468">Creates an instance of a tree node from an XPO file but does not import it into the AOT.</span></span> <span data-ttu-id="d3325-469">たとえば、これにより、同じツリー ノードの別のバージョンと比較できます。</span><span class="sxs-lookup"><span data-stu-id="d3325-469">For example, this allows you to compare it with another version of the same tree node.</span></span>

```xpp
public TreeNode getImportedNode(int id, int utilfiletype, UtilElementType utiltype, str name, int fileposition, int Flag)
```

### <a name="parameters---getimportednode"></a><span data-ttu-id="d3325-470">パラメーター - getImportedNode</span><span class="sxs-lookup"><span data-stu-id="d3325-470">Parameters - getImportedNode</span></span>

<span data-ttu-id="d3325-471">id</span><span class="sxs-lookup"><span data-stu-id="d3325-471">id</span></span>  

<!-- -->

<span data-ttu-id="d3325-472">utilfiletype</span><span class="sxs-lookup"><span data-stu-id="d3325-472">utilfiletype</span></span>  

<!-- -->

<span data-ttu-id="d3325-473">utiltype</span><span class="sxs-lookup"><span data-stu-id="d3325-473">utiltype</span></span>  

<!-- -->

<span data-ttu-id="d3325-474">名前</span><span class="sxs-lookup"><span data-stu-id="d3325-474">name</span></span>  

<!-- -->

<span data-ttu-id="d3325-475">fileposition</span><span class="sxs-lookup"><span data-stu-id="d3325-475">fileposition</span></span>  

<!-- -->

<span data-ttu-id="d3325-476">フラグ</span><span class="sxs-lookup"><span data-stu-id="d3325-476">Flag</span></span>  

### <a name="return-value---getimportednode"></a><span data-ttu-id="d3325-477">戻り値 - getImportedNode</span><span class="sxs-lookup"><span data-stu-id="d3325-477">Return Value - getImportedNode</span></span>

<span data-ttu-id="d3325-478">ツリー ノード。</span><span class="sxs-lookup"><span data-stu-id="d3325-478">A tree node.</span></span>

### <a name="remarks---getimportednode"></a><span data-ttu-id="d3325-479">備考 - getImportedNode</span><span class="sxs-lookup"><span data-stu-id="d3325-479">Remarks - getImportedNode</span></span>

<span data-ttu-id="d3325-480">tilfiletype パラメーターの使用可能な値は UtilFileType 列挙で使用可能な値です。</span><span class="sxs-lookup"><span data-stu-id="d3325-480">The possible values for the utilfiletype parameter are those that are available in the UtilFileType Enumeration.</span></span> <span data-ttu-id="d3325-481">utiltype パラメーターの使用可能な値は UtilElementType 列挙で使用可能な値です。</span><span class="sxs-lookup"><span data-stu-id="d3325-481">The possible values for the utiltype parameter are those that are available in the UtilElementType Enumeration.</span></span> <span data-ttu-id="d3325-482">フラグ パラメーターの可能な値の一覧については、AOTExport マクロを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d3325-482">For a list of the possible values for the Flag parameter, see the AOTExport macro.</span></span> <span data-ttu-id="d3325-483">値は、システム インポート フラグ コメントの下に一覧で表示されています。</span><span class="sxs-lookup"><span data-stu-id="d3325-483">The values are listed under the System import flags comment.</span></span>

### <a name="examples---getimportednode"></a><span data-ttu-id="d3325-484">例 - getImportedNode</span><span class="sxs-lookup"><span data-stu-id="d3325-484">Examples - getImportedNode</span></span>

<span data-ttu-id="d3325-485">次の例では、getImportedNode メソッドを使用して仮想ツリー ノードを作成します。</span><span class="sxs-lookup"><span data-stu-id="d3325-485">The following example uses the getImportedNode method to create a virtual tree node.</span></span>

```xpp
public TreeNode getVirtualTreenode( 
    Filename _filename = this.fileName()) 
{ 
    #AOT 
    #AotExport 
    TmpAotImport      tmpImportAot; 
    SysImportElements sysImportElements = new SysImportElements(); 
    TreeNode treeNodeImport  = null; 
    int      exportId; 
    int      flag = (#impGetCompareNode + #impKeepIds); 
    str      name; 
    ; 
    // Set the filename. 
    sysImportElements.newFile(_filename); 
    // Get info from the file 
    tmpImportAot = sysImportElements.getTmpImportAot(); 
    // Create an import context 
    exportId     = infolog.startImport(_filename, flag); 
    // Get the right name 
    // for doc nodes it is the path excl. the first part 
    switch (tmpImportAot.UtilFileType) 
    { 
        case UtilFileType::Application: 
            name = tmpImportAot.TreeNodeName; 
            break; 
        case UtilFileType::ApplicationCodeDocumentation: 
            name = strdel(tmpImportAot.TreeNodePath, 1, strlen(#ApplicationDeveloperDocPath)); 
            break; 
        case UtilFileType::ApplicationHelp: 
            name = strdel(tmpImportAot.TreeNodePath, 1, strlen(#ApplicationDocPath)); 
            break; 
        case UtilFileType::KernelHelp: 
            name = strdel(tmpImportAot.TreeNodePath, 1, strlen(#SystemDocPath)); 
            break; 
        default: 
            name = tmpImportAot.TreeNodeName; 
            break; 
    } 
    // Import the node in memory 
    treeNodeImport  = infolog.getImportedNode( 
        exportId, 
        tmpImportAot.UtilFileType, 
        tmpImportAot.UtilElementType, 
        name, 
        tmpImportAot.FilePos, 
        flag); 
    // Close the import context 
    infolog.endImport(exportId, 1); 
    return treeNodeImport; 
}
```

## <a name="method-getnode"></a><span data-ttu-id="d3325-486">メソッド getNode</span><span class="sxs-lookup"><span data-stu-id="d3325-486">Method getNode</span></span>

<span data-ttu-id="d3325-487">AOT 内のノードに対応するツリー ノードを取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-487">Retrieves a tree node that corresponds to a node in the AOT.</span></span>

```xpp
public TreeNode getNode(UtilElementType UtilType, str Name, [UtilElementId ParentId], [int Type], [UtilEntryLevel Utillevel], [boolean Forcelevel], [int Mode], [boolean OldUtil])
```

### <a name="parameters---getnode"></a><span data-ttu-id="d3325-488">パラメーター - getNode</span><span class="sxs-lookup"><span data-stu-id="d3325-488">Parameters - getNode</span></span>

<span data-ttu-id="d3325-489">UtilType</span><span class="sxs-lookup"><span data-stu-id="d3325-489">UtilType</span></span>  
<span data-ttu-id="d3325-490">古い AOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d3325-490">A Boolean value that indicates whether to take the node from the old AOT in the old AOT folder.</span></span>

<!-- -->

<span data-ttu-id="d3325-491">氏名</span><span class="sxs-lookup"><span data-stu-id="d3325-491">Name</span></span>  
<span data-ttu-id="d3325-492">古い AOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d3325-492">A Boolean value that indicates whether to take the node from the old AOT in the old AOT folder.</span></span>

<!-- -->

<span data-ttu-id="d3325-493">ParentId</span><span class="sxs-lookup"><span data-stu-id="d3325-493">ParentId</span></span>  
<span data-ttu-id="d3325-494">古い AOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d3325-494">A Boolean value that indicates whether to take the node from the old AOT in the old AOT folder.</span></span>

<!-- -->

<span data-ttu-id="d3325-495">種類</span><span class="sxs-lookup"><span data-stu-id="d3325-495">Type</span></span>  
<span data-ttu-id="d3325-496">古い AOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d3325-496">A Boolean value that indicates whether to take the node from the old AOT in the old AOT folder.</span></span>

<!-- -->

<span data-ttu-id="d3325-497">Utillevel</span><span class="sxs-lookup"><span data-stu-id="d3325-497">Utillevel</span></span>  
<span data-ttu-id="d3325-498">古い AOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d3325-498">A Boolean value that indicates whether to take the node from the old AOT in the old AOT folder.</span></span>

<!-- -->

<span data-ttu-id="d3325-499">Forcelevel</span><span class="sxs-lookup"><span data-stu-id="d3325-499">Forcelevel</span></span>  
<span data-ttu-id="d3325-500">古い AOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d3325-500">A Boolean value that indicates whether to take the node from the old AOT in the old AOT folder.</span></span>

<!-- -->

<span data-ttu-id="d3325-501">モード</span><span class="sxs-lookup"><span data-stu-id="d3325-501">Mode</span></span>  
<span data-ttu-id="d3325-502">古い AOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d3325-502">A Boolean value that indicates whether to take the node from the old AOT in the old AOT folder.</span></span>

<!-- -->

<span data-ttu-id="d3325-503">OldUtil</span><span class="sxs-lookup"><span data-stu-id="d3325-503">OldUtil</span></span>  
<span data-ttu-id="d3325-504">古い AOT フォルダー内の古い AOT からノードを取得するかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d3325-504">A Boolean value that indicates whether to take the node from the old AOT in the old AOT folder.</span></span>

### <a name="return-value---getnode"></a><span data-ttu-id="d3325-505">戻り値 - getNode</span><span class="sxs-lookup"><span data-stu-id="d3325-505">Return Value - getNode</span></span>

<span data-ttu-id="d3325-506">UtilType パラメーターおよび Name パラメーターで指定されるツリー ノード。</span><span class="sxs-lookup"><span data-stu-id="d3325-506">The tree node that is specified by the UtilType and Name parameters.</span></span>

### <a name="remarks---getnode"></a><span data-ttu-id="d3325-507">備考 - getNode</span><span class="sxs-lookup"><span data-stu-id="d3325-507">Remarks - getNode</span></span>

<span data-ttu-id="d3325-508">戻されたノードは AOT にリンクされていないため、ノードで操作を実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="d3325-508">The node returned is not linked into the AOT, so you cannot perform operations on the node.</span></span> <span data-ttu-id="d3325-509">ノードの操作を行うには、代わりに findNode メソッドまたは rootNode メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d3325-509">To perform operations on a node, use the findNode or rootNode method instead.</span></span> <span data-ttu-id="d3325-510">UtilLevel trueparameter パラメーターの既定値は現在のレイヤーです。</span><span class="sxs-lookup"><span data-stu-id="d3325-510">The default value for the UtilLevel parameter is the current layer.</span></span> <span data-ttu-id="d3325-511">Mode パラメーターの使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d3325-511">The possible values for the Mode parameter are:</span></span>

-   <span data-ttu-id="d3325-512">0x001: 実行用の読み込み</span><span class="sxs-lookup"><span data-stu-id="d3325-512">0x001: Load for run</span></span>
-   <span data-ttu-id="d3325-513">0x002: 編集用の読み込み</span><span class="sxs-lookup"><span data-stu-id="d3325-513">0x002: Load for edit</span></span>

<span data-ttu-id="d3325-514">ForceLevel パラメーターの既定値は false です。</span><span class="sxs-lookup"><span data-stu-id="d3325-514">The default value of the ForceLevel parameter is false.</span></span> <span data-ttu-id="d3325-515">False に設定され、指定されたレイヤーでコンテンツがない場合は、ノードはコンテンツを持つ次のレイヤーから取得されます。</span><span class="sxs-lookup"><span data-stu-id="d3325-515">If it is set to false, and there is no content in the layer specified, the node will be taken from the next layer below this that does have content.</span></span> <span data-ttu-id="d3325-516">true に設定され、レイヤーにコンテンツがない場合、メソッドは nullNothingnullptrunita null 参照 (Visual Basic 上ではなし) を返します。</span><span class="sxs-lookup"><span data-stu-id="d3325-516">If it is set to true, and there is no content in the layer, the method will return nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

## <a name="method-getnoderesid"></a><span data-ttu-id="d3325-517">メソッド getNodeResid</span><span class="sxs-lookup"><span data-stu-id="d3325-517">Method getNodeResid</span></span>

<span data-ttu-id="d3325-518">指定したタイプのノードを表示するために使用されるアイコンのリソース ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-518">Retrieves the resource ID for the icon that is used to display nodes of the specified type.</span></span>

```xpp
public int getNodeResid(UtilElementType nodeType)
```

### <a name="parameters---getnoderesid"></a><span data-ttu-id="d3325-519">パラメーター - getNodeResid</span><span class="sxs-lookup"><span data-stu-id="d3325-519">Parameters - getNodeResid</span></span>

<span data-ttu-id="d3325-520">nodeType</span><span class="sxs-lookup"><span data-stu-id="d3325-520">nodeType</span></span>  
<span data-ttu-id="d3325-521">取得するノードのタイプを示す UtilElementType システム列挙値。</span><span class="sxs-lookup"><span data-stu-id="d3325-521">A UtilElementType system enumeration value that indicates the type of node to retrieve.</span></span>

### <a name="return-value---getnoderesid"></a><span data-ttu-id="d3325-522">戻り値 - getNodeResid</span><span class="sxs-lookup"><span data-stu-id="d3325-522">Return Value - getNodeResid</span></span>

<span data-ttu-id="d3325-523">ノードのリソース ID を表す整数。</span><span class="sxs-lookup"><span data-stu-id="d3325-523">An integer that represents the Resource ID for the node.</span></span>

## <a name="method-gettaskinfo"></a><span data-ttu-id="d3325-524">メソッド getTaskInfo</span><span class="sxs-lookup"><span data-stu-id="d3325-524">Method getTaskInfo</span></span>

```xpp
public Struct getTaskInfo(int taskNumber)
```

### <a name="parameters---gettaskinfo"></a><span data-ttu-id="d3325-525">パラメーター - getTaskInfo</span><span class="sxs-lookup"><span data-stu-id="d3325-525">Parameters - getTaskInfo</span></span>

<span data-ttu-id="d3325-526">taskNumber</span><span class="sxs-lookup"><span data-stu-id="d3325-526">taskNumber</span></span>  

### <a name="return-value---gettaskinfo"></a><span data-ttu-id="d3325-527">戻り値 - getTaskInfo</span><span class="sxs-lookup"><span data-stu-id="d3325-527">Return Value - getTaskInfo</span></span>

## <a name="method-getusersetup"></a><span data-ttu-id="d3325-528">メソッド getUserSetup</span><span class="sxs-lookup"><span data-stu-id="d3325-528">Method getUserSetup</span></span>

<span data-ttu-id="d3325-529">ユーザー パラメーターを設定するために使用する UserSetup オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-529">Retrieves a UserSetup object that is used to set user parameters.</span></span>

```xpp
public UserSetup getUserSetup()
```

### <a name="return-value---getusersetup"></a><span data-ttu-id="d3325-530">戻り値 - getUserSetup</span><span class="sxs-lookup"><span data-stu-id="d3325-530">Return Value - getUserSetup</span></span>

<span data-ttu-id="d3325-531">UserSetup オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="d3325-531">A UserSetup object.</span></span>

### <a name="remarks---getusersetup"></a><span data-ttu-id="d3325-532">備考 - getUserSetup</span><span class="sxs-lookup"><span data-stu-id="d3325-532">Remarks - getUserSetup</span></span>

<span data-ttu-id="d3325-533">UserSetup システム クラスは、ユーザー パラメーターを設定するためのインターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="d3325-533">The UserSetup system class provides an interface for setting user parameters.</span></span>

## <a name="method-getworkspacelist"></a><span data-ttu-id="d3325-534">メソッド getWorkspaceList</span><span class="sxs-lookup"><span data-stu-id="d3325-534">Method getWorkspaceList</span></span>

```xpp
public container getWorkspaceList()
```

### <a name="return-value---getworkspacelist"></a><span data-ttu-id="d3325-535">戻り値 - getWorkspaceList</span><span class="sxs-lookup"><span data-stu-id="d3325-535">Return Value - getWorkspaceList</span></span>

## <a name="method-hwnd"></a><span data-ttu-id="d3325-536">メソッド hWnd</span><span class="sxs-lookup"><span data-stu-id="d3325-536">Method hWnd</span></span>

<span data-ttu-id="d3325-537">ナビゲーション ペイン ウィンドウのハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-537">Retrieves a handle to the Navigation Pane window.</span></span>

```xpp
public int hWnd([int workspaceNum])
```

### <a name="parameters---hwnd"></a><span data-ttu-id="d3325-538">パラメーター - hWnd</span><span class="sxs-lookup"><span data-stu-id="d3325-538">Parameters - hWnd</span></span>

<span data-ttu-id="d3325-539">workspaceNum</span><span class="sxs-lookup"><span data-stu-id="d3325-539">workspaceNum</span></span>  
<span data-ttu-id="d3325-540">ナビゲーション ウィンドウ ハンドルを取得するワークスペースのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="d3325-540">The handle to the workspace from which to get the Navigation Pane handle.</span></span>

### <a name="return-value---hwnd"></a><span data-ttu-id="d3325-541">戻り値 - hWnd</span><span class="sxs-lookup"><span data-stu-id="d3325-541">Return Value - hWnd</span></span>

<span data-ttu-id="d3325-542">ナビゲーション ペイン ウィンドウにハンドルを表示する整数。</span><span class="sxs-lookup"><span data-stu-id="d3325-542">An integer that represents the handle to the Navigation Pane window.</span></span>

## <a name="method-import"></a><span data-ttu-id="d3325-543">メソッド import</span><span class="sxs-lookup"><span data-stu-id="d3325-543">Method import</span></span>

```xpp
public boolean import(container infologContainer, [boolean clearExistingInfolog])
```

### <a name="parameters---import"></a><span data-ttu-id="d3325-544">パラメーター - import</span><span class="sxs-lookup"><span data-stu-id="d3325-544">Parameters - import</span></span>

<span data-ttu-id="d3325-545">infologContainer</span><span class="sxs-lookup"><span data-stu-id="d3325-545">infologContainer</span></span>  

<!-- -->

<span data-ttu-id="d3325-546">clearExistingInfolog</span><span class="sxs-lookup"><span data-stu-id="d3325-546">clearExistingInfolog</span></span>  

### <a name="return-value---import"></a><span data-ttu-id="d3325-547">戻り値 - import</span><span class="sxs-lookup"><span data-stu-id="d3325-547">Return Value - import</span></span>

## <a name="method-importelement"></a><span data-ttu-id="d3325-548">メソッド importElement</span><span class="sxs-lookup"><span data-stu-id="d3325-548">Method importElement</span></span>

<span data-ttu-id="d3325-549">インポートする対象を指定します。</span><span class="sxs-lookup"><span data-stu-id="d3325-549">Specifies the object to be imported.</span></span>

```xpp
public int importElement(int id, int utilfiletype, UtilElementType utiltype, str name, int fileposition, int Flag)
```

### <a name="parameters---importelement"></a><span data-ttu-id="d3325-550">パラメーター - importElement</span><span class="sxs-lookup"><span data-stu-id="d3325-550">Parameters - importElement</span></span>

<span data-ttu-id="d3325-551">id</span><span class="sxs-lookup"><span data-stu-id="d3325-551">id</span></span>  

<!-- -->

<span data-ttu-id="d3325-552">utilfiletype</span><span class="sxs-lookup"><span data-stu-id="d3325-552">utilfiletype</span></span>  

<!-- -->

<span data-ttu-id="d3325-553">utiltype</span><span class="sxs-lookup"><span data-stu-id="d3325-553">utiltype</span></span>  

<!-- -->

<span data-ttu-id="d3325-554">名前</span><span class="sxs-lookup"><span data-stu-id="d3325-554">name</span></span>  

<!-- -->

<span data-ttu-id="d3325-555">fileposition</span><span class="sxs-lookup"><span data-stu-id="d3325-555">fileposition</span></span>  

<!-- -->

<span data-ttu-id="d3325-556">フラグ</span><span class="sxs-lookup"><span data-stu-id="d3325-556">Flag</span></span>  

### <a name="return-value---importelement"></a><span data-ttu-id="d3325-557">戻り値 - importElement</span><span class="sxs-lookup"><span data-stu-id="d3325-557">Return Value - importElement</span></span>

<span data-ttu-id="d3325-558"> メソッドは廃止されています。</span><span class="sxs-lookup"><span data-stu-id="d3325-558">This method is obsolete.</span></span> <span data-ttu-id="d3325-559">代わりに SysImportElements クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="d3325-559">Use the SysImportElements class instead.</span></span>

## <a name="method-importstring"></a><span data-ttu-id="d3325-560">メソッド importString</span><span class="sxs-lookup"><span data-stu-id="d3325-560">Method importString</span></span>

<span data-ttu-id="d3325-561">ファイルからオブジェクトをインポートします。</span><span class="sxs-lookup"><span data-stu-id="d3325-561">Imports an object from a file.</span></span>

```xpp
public int importString(str source, UtilElementType kind, str name)
```

### <a name="parameters---importstring"></a><span data-ttu-id="d3325-562">パラメーター - importString</span><span class="sxs-lookup"><span data-stu-id="d3325-562">Parameters - importString</span></span>

<span data-ttu-id="d3325-563">ソース</span><span class="sxs-lookup"><span data-stu-id="d3325-563">source</span></span>  
<span data-ttu-id="d3325-564">オブジェクトの名前です。</span><span class="sxs-lookup"><span data-stu-id="d3325-564">The name of the object.</span></span>

<!-- -->

<span data-ttu-id="d3325-565">kind</span><span class="sxs-lookup"><span data-stu-id="d3325-565">kind</span></span>  
<span data-ttu-id="d3325-566">オブジェクトの名前です。</span><span class="sxs-lookup"><span data-stu-id="d3325-566">The name of the object.</span></span>

<!-- -->

<span data-ttu-id="d3325-567">名前</span><span class="sxs-lookup"><span data-stu-id="d3325-567">name</span></span>  
<span data-ttu-id="d3325-568">オブジェクトの名前です。</span><span class="sxs-lookup"><span data-stu-id="d3325-568">The name of the object.</span></span>

### <a name="return-value---importstring"></a><span data-ttu-id="d3325-569">戻り値 - importString</span><span class="sxs-lookup"><span data-stu-id="d3325-569">Return Value - importString</span></span>

## <a name="method-instance"></a><span data-ttu-id="d3325-570">メソッド instance</span><span class="sxs-lookup"><span data-stu-id="d3325-570">Method instance</span></span>

<span data-ttu-id="d3325-571">アプリケーションの現在のインスタンスへのハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-571">Retrieves a handle to the current instance of the application.</span></span>

```xpp
public int instance()
```

### <a name="return-value---instance"></a><span data-ttu-id="d3325-572">戻り値 - instance</span><span class="sxs-lookup"><span data-stu-id="d3325-572">Return Value - instance</span></span>

<span data-ttu-id="d3325-573">アプリケーションの現在のインスタンスのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="d3325-573">The handle of the current instance of the application.</span></span>

## <a name="method-isocurrencycode"></a><span data-ttu-id="d3325-574">メソッド isoCurrencyCode</span><span class="sxs-lookup"><span data-stu-id="d3325-574">Method isoCurrencyCode</span></span>

<span data-ttu-id="d3325-575">通貨コードを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d3325-575">Gets or sets the currency code.</span></span>

```xpp
public str isoCurrencyCode([str code])
```

### <a name="parameters---isocurrencycode"></a><span data-ttu-id="d3325-576">パラメーター - isoCurrencyCode</span><span class="sxs-lookup"><span data-stu-id="d3325-576">Parameters - isoCurrencyCode</span></span>

<span data-ttu-id="d3325-577">コード</span><span class="sxs-lookup"><span data-stu-id="d3325-577">code</span></span>  
<span data-ttu-id="d3325-578">設定する ISO 通貨コードを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="d3325-578">A string that contains the ISO currency code to set.</span></span>

### <a name="return-value---isocurrencycode"></a><span data-ttu-id="d3325-579">戻り値 - isoCurrencyCode</span><span class="sxs-lookup"><span data-stu-id="d3325-579">Return Value - isoCurrencyCode</span></span>

<span data-ttu-id="d3325-580">現在のアプリケーションの通貨コードを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="d3325-580">A string that contains the currency code for the current application.</span></span>

## <a name="method-isvisible"></a><span data-ttu-id="d3325-581">メソッド IsVisible</span><span class="sxs-lookup"><span data-stu-id="d3325-581">Method IsVisible</span></span>

<span data-ttu-id="d3325-582">クライアントのウィンドウが最小化されていないかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d3325-582">Determines whether the client window is not minimized.</span></span>

```xpp
public boolean IsVisible()
```

### <a name="return-value---isvisible"></a><span data-ttu-id="d3325-583">戻り値 - IsVisible</span><span class="sxs-lookup"><span data-stu-id="d3325-583">Return Value - IsVisible</span></span>

<span data-ttu-id="d3325-584">クライアント ウィンドウが最小化されている場合は false; それ以外の場合は true。</span><span class="sxs-lookup"><span data-stu-id="d3325-584">false if the client window is minimized; otherwise, true.</span></span>

## <a name="method-language"></a><span data-ttu-id="d3325-585">メソッド language</span><span class="sxs-lookup"><span data-stu-id="d3325-585">Method language</span></span>

<span data-ttu-id="d3325-586">GUI の言語を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d3325-586">Gets or sets the language for the GUI.</span></span>

```xpp
public str language([str languageCode])
```

### <a name="parameters---language"></a><span data-ttu-id="d3325-587">パラメーター - language</span><span class="sxs-lookup"><span data-stu-id="d3325-587">Parameters - language</span></span>

<span data-ttu-id="d3325-588">languageCode</span><span class="sxs-lookup"><span data-stu-id="d3325-588">languageCode</span></span>  
<span data-ttu-id="d3325-589">設定の言語コードを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="d3325-589">A string that contains the language code to set.</span></span>

### <a name="return-value---language"></a><span data-ttu-id="d3325-590">戻り値 - language</span><span class="sxs-lookup"><span data-stu-id="d3325-590">Return Value - language</span></span>

<span data-ttu-id="d3325-591">現在の言語コードを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="d3325-591">A string that contains the current language code.</span></span>

### <a name="remarks---language"></a><span data-ttu-id="d3325-592">備考 - language</span><span class="sxs-lookup"><span data-stu-id="d3325-592">Remarks - language</span></span>

<span data-ttu-id="d3325-593">ドキュメントの言語を設定するには、xInfo.documentationLanguage メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d3325-593">To set the language for the documentation, use the xInfo.documentationLanguage Method.</span></span> <span data-ttu-id="d3325-594">特定のセッションの GUI 言語を設定するには、xSession.interfaceLanguage メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d3325-594">To set the GUI language for a particular session, use the xSession.interfaceLanguage Method.</span></span>

### <a name="examples---language"></a><span data-ttu-id="d3325-595">例 - language</span><span class="sxs-lookup"><span data-stu-id="d3325-595">Examples - language</span></span>

<span data-ttu-id="d3325-596">次の例では、現在設定されている言語のコードを出力します。</span><span class="sxs-lookup"><span data-stu-id="d3325-596">The following example prints the code for the language that is currently set.</span></span> <span data-ttu-id="d3325-597">たとえば、インターフェイスが英語 (US) であった場合、「en-us」を印刷します。</span><span class="sxs-lookup"><span data-stu-id="d3325-597">For example, if the interface was in US English, it would print "en-us".</span></span>

```xpp
{ 
    print infolog.language(); 
    pause; 
}
```

## <a name="method-level"></a><span data-ttu-id="d3325-598">メソッド level</span><span class="sxs-lookup"><span data-stu-id="d3325-598">Method level</span></span>

<span data-ttu-id="d3325-599">情報ログ バッファー内の行の例外レベルを取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-599">Retrieves the exception level of a line in the Infolog buffer.</span></span>

```xpp
public Exception level(int line)
```

### <a name="parameters---level"></a><span data-ttu-id="d3325-600">パラメーター - level</span><span class="sxs-lookup"><span data-stu-id="d3325-600">Parameters - level</span></span>

<span data-ttu-id="d3325-601">明細行</span><span class="sxs-lookup"><span data-stu-id="d3325-601">line</span></span>  
<span data-ttu-id="d3325-602">例外レベルを取得する情報ログの行。</span><span class="sxs-lookup"><span data-stu-id="d3325-602">The line in the Infolog for which to retrieve the exception level.</span></span>

### <a name="return-value---level"></a><span data-ttu-id="d3325-603">戻り値 - level</span><span class="sxs-lookup"><span data-stu-id="d3325-603">Return Value - level</span></span>

<span data-ttu-id="d3325-604">例外システム列挙値。</span><span class="sxs-lookup"><span data-stu-id="d3325-604">A Exception system enumeration value.</span></span>

### <a name="remarks---level"></a><span data-ttu-id="d3325-605">備考 - level</span><span class="sxs-lookup"><span data-stu-id="d3325-605">Remarks - level</span></span>

<span data-ttu-id="d3325-606">詳細については、「トライおよびキャッチ キーワードで例外処理」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d3325-606">For more information, see Exception Handling with try and catch Keywords.</span></span>

## <a name="method-line"></a><span data-ttu-id="d3325-607">メソッド line</span><span class="sxs-lookup"><span data-stu-id="d3325-607">Method line</span></span>

<span data-ttu-id="d3325-608">情報ログ バッファの明細行の数を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-608">Retrieves the number of lines in the Infolog buffer.</span></span>

```xpp
public int line()
```

### <a name="return-value---line"></a><span data-ttu-id="d3325-609">戻り値 - line</span><span class="sxs-lookup"><span data-stu-id="d3325-609">Return Value - line</span></span>

<span data-ttu-id="d3325-610">情報ログ バッファー内の行数を表す整数。</span><span class="sxs-lookup"><span data-stu-id="d3325-610">An integer that represents the number of lines in the Infolog buffer.</span></span>

### <a name="remarks---line"></a><span data-ttu-id="d3325-611">備考 - line</span><span class="sxs-lookup"><span data-stu-id="d3325-611">Remarks - line</span></span>

<span data-ttu-id="d3325-612">サーバーでコードを実行している場合は、代わりに xGlobal::infologLine メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d3325-612">If you are running code on the server, use the xGlobal::infologLine method instead.</span></span> <span data-ttu-id="d3325-613">サーバーとクライアントの間の呼び出しを除外します。</span><span class="sxs-lookup"><span data-stu-id="d3325-613">It eliminates calls between the server and client.</span></span> <span data-ttu-id="d3325-614">Infolog 内の特定タイプの例外の数を取得するには、xInfo.num メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d3325-614">To get the number of exceptions of a specific type in the Infolog, use the xInfo.num Method.</span></span>

## <a name="method-messagewin"></a><span data-ttu-id="d3325-615">メソッド messageWin</span><span class="sxs-lookup"><span data-stu-id="d3325-615">Method messageWin</span></span>

<span data-ttu-id="d3325-616">Infolog から Message ウィンドウに出力を送信できます。</span><span class="sxs-lookup"><span data-stu-id="d3325-616">Enables you to send output from the Infolog to the Message window.</span></span>

```xpp
public MessageWin messageWin()
```

### <a name="return-value---messagewin"></a><span data-ttu-id="d3325-617">戻り値 - messageWin</span><span class="sxs-lookup"><span data-stu-id="d3325-617">Return Value - messageWin</span></span>

<span data-ttu-id="d3325-618">MessageWin オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="d3325-618">A MessageWin object.</span></span>

### <a name="remarks---messagewin"></a><span data-ttu-id="d3325-619">備考 - messageWin</span><span class="sxs-lookup"><span data-stu-id="d3325-619">Remarks - messageWin</span></span>

<span data-ttu-id="d3325-620">時間がかかるプロセスがある場合は、メッセージ ウィンドウに出力を送信することが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="d3325-620">You may want to send output to the Message window if you have a lengthy process.</span></span> <span data-ttu-id="d3325-621">情報ログに出力を送信する場合、プロセスが完了するまで何も表示されません。</span><span class="sxs-lookup"><span data-stu-id="d3325-621">If you send output to the Infolog, nothing will be displayed until the process is completed.</span></span> <span data-ttu-id="d3325-622">メッセージ ウィンドウに出力を送信する場合は、工程の進行中のコンテンツが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d3325-622">If you send output to the Message window, content is displayed as the operation proceeds.</span></span>

## <a name="method-nationalcurrencyfactor"></a><span data-ttu-id="d3325-623">メソッド nationalCurrencyFactor</span><span class="sxs-lookup"><span data-stu-id="d3325-623">Method nationalCurrencyFactor</span></span>

```xpp
public Real nationalCurrencyFactor([Real factor])
```

### <a name="parameters---nationalcurrencyfactor"></a><span data-ttu-id="d3325-624">パラメーター - nationalCurrencyFactor</span><span class="sxs-lookup"><span data-stu-id="d3325-624">Parameters - nationalCurrencyFactor</span></span>

<span data-ttu-id="d3325-625">係数</span><span class="sxs-lookup"><span data-stu-id="d3325-625">factor</span></span>  

### <a name="return-value---nationalcurrencyfactor"></a><span data-ttu-id="d3325-626">戻り値 - nationalCurrencyFactor</span><span class="sxs-lookup"><span data-stu-id="d3325-626">Return Value - nationalCurrencyFactor</span></span>

## <a name="method-nationalcurrencypostfix"></a><span data-ttu-id="d3325-627">メソッド nationalCurrencyPostfix</span><span class="sxs-lookup"><span data-stu-id="d3325-627">Method nationalCurrencyPostfix</span></span>

```xpp
public str nationalCurrencyPostfix([str string])
```

### <a name="parameters---nationalcurrencypostfix"></a><span data-ttu-id="d3325-628">パラメーター - nationalCurrencyPostfix</span><span class="sxs-lookup"><span data-stu-id="d3325-628">Parameters - nationalCurrencyPostfix</span></span>

<span data-ttu-id="d3325-629">文字列</span><span class="sxs-lookup"><span data-stu-id="d3325-629">string</span></span>  

### <a name="return-value---nationalcurrencypostfix"></a><span data-ttu-id="d3325-630">戻り値 - nationalCurrencyPostfix</span><span class="sxs-lookup"><span data-stu-id="d3325-630">Return Value - nationalCurrencyPostfix</span></span>

## <a name="method-nationalcurrencyprefix"></a><span data-ttu-id="d3325-631">メソッド nationalCurrencyPrefix</span><span class="sxs-lookup"><span data-stu-id="d3325-631">Method nationalCurrencyPrefix</span></span>

```xpp
public str nationalCurrencyPrefix([str string])
```

### <a name="parameters---nationalcurrencyprefix"></a><span data-ttu-id="d3325-632">パラメーター - nationalCurrencyPrefix</span><span class="sxs-lookup"><span data-stu-id="d3325-632">Parameters - nationalCurrencyPrefix</span></span>

<span data-ttu-id="d3325-633">文字列</span><span class="sxs-lookup"><span data-stu-id="d3325-633">string</span></span>  

### <a name="return-value---nationalcurrencyprefix"></a><span data-ttu-id="d3325-634">戻り値 - nationalCurrencyPrefix</span><span class="sxs-lookup"><span data-stu-id="d3325-634">Return Value - nationalCurrencyPrefix</span></span>

## <a name="method-navpane"></a><span data-ttu-id="d3325-635">メソッド navPane</span><span class="sxs-lookup"><span data-stu-id="d3325-635">Method navPane</span></span>

<span data-ttu-id="d3325-636">プライマリ ナビゲーション コントロール クラスの xNavPane オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-636">Retrieves an xNavPane object, the primary navigation control class.</span></span>

```xpp
public xNavPane navPane()
```

### <a name="return-value---navpane"></a><span data-ttu-id="d3325-637">戻り値 - navPane</span><span class="sxs-lookup"><span data-stu-id="d3325-637">Return Value - navPane</span></span>

<span data-ttu-id="d3325-638">xNavPane クラスのインスタンス。</span><span class="sxs-lookup"><span data-stu-id="d3325-638">An instance of the xNavPane class.</span></span>

### <a name="remarks---navpane"></a><span data-ttu-id="d3325-639">備考 - navPane</span><span class="sxs-lookup"><span data-stu-id="d3325-639">Remarks - navPane</span></span>

<span data-ttu-id="d3325-640">このクラスのインスタンスはワークスペースごとに 1 つのみ持つことができます。</span><span class="sxs-lookup"><span data-stu-id="d3325-640">You can only have one instance of this class per workspace.</span></span>

## <a name="method-num"></a><span data-ttu-id="d3325-641">メソッド num</span><span class="sxs-lookup"><span data-stu-id="d3325-641">Method num</span></span>

<span data-ttu-id="d3325-642">情報ログ バッファにおける指定した型の例外の数を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-642">Retrieves the number of exceptions of the specified type in the Infolog buffer.</span></span>

```xpp
public int num([Exception exceptionType])
```

### <a name="parameters---num"></a><span data-ttu-id="d3325-643">パラメーター - num</span><span class="sxs-lookup"><span data-stu-id="d3325-643">Parameters - num</span></span>

<span data-ttu-id="d3325-644">exceptionType</span><span class="sxs-lookup"><span data-stu-id="d3325-644">exceptionType</span></span>  
<span data-ttu-id="d3325-645">カウントする例外のタイプを示す例外システム列挙値; オプション。</span><span class="sxs-lookup"><span data-stu-id="d3325-645">A Exception system enumeration value that indicates the exception type to count; optional.</span></span>

### <a name="return-value---num"></a><span data-ttu-id="d3325-646">戻り値 - num</span><span class="sxs-lookup"><span data-stu-id="d3325-646">Return Value - num</span></span>

<span data-ttu-id="d3325-647">exceptionType パラメーターで指定されたタイプの例外の数または、パラメーターが指定されていない場合の情報ログ内の行の合計数を表す整数。</span><span class="sxs-lookup"><span data-stu-id="d3325-647">An integer that represents the number of exceptions of the type specified by the exceptionType parameter, or the total number of lines in the Infolog if no parameter is specified.</span></span>

### <a name="remarks---num"></a><span data-ttu-id="d3325-648">備考 - num</span><span class="sxs-lookup"><span data-stu-id="d3325-648">Remarks - num</span></span>

<span data-ttu-id="d3325-649">詳細については、「トライおよびキャッチ キーワードで例外処理」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d3325-649">For more information, see Exception Handling with try and catch Keywords.</span></span>

### <a name="examples---num"></a><span data-ttu-id="d3325-650">例 - num</span><span class="sxs-lookup"><span data-stu-id="d3325-650">Examples - num</span></span>

<span data-ttu-id="d3325-651">次の例は、Infolog 内の警告の数を返します。</span><span class="sxs-lookup"><span data-stu-id="d3325-651">The following example returns the number of warnings in the Infolog.</span></span>

```xpp
{ 
    print infolog.num(Exception::Warning); 
    pause; 
}
```

## <a name="method-previnstance"></a><span data-ttu-id="d3325-652">メソッド prevInstance</span><span class="sxs-lookup"><span data-stu-id="d3325-652">Method prevInstance</span></span>

<span data-ttu-id="d3325-653">アプリケーションの前のインスタンスへのハンドルを取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-653">Retrieves a handle to the previous instance of the application.</span></span>

```xpp
public int prevInstance()
```

### <a name="return-value---previnstance"></a><span data-ttu-id="d3325-654">戻り値 - prevInstance</span><span class="sxs-lookup"><span data-stu-id="d3325-654">Return Value - prevInstance</span></span>

<span data-ttu-id="d3325-655">アプリケーションの以前のインスタンスのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="d3325-655">The handle of the previous instance of the application.</span></span>

### <a name="remarks---previnstance"></a><span data-ttu-id="d3325-656">備考 - prevInstance</span><span class="sxs-lookup"><span data-stu-id="d3325-656">Remarks - prevInstance</span></span>

<span data-ttu-id="d3325-657">このメソッドは使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="d3325-657">This method should not be used.</span></span>

## <a name="method-processid"></a><span data-ttu-id="d3325-658">メソッド processId</span><span class="sxs-lookup"><span data-stu-id="d3325-658">Method processId</span></span>

<span data-ttu-id="d3325-659">プロセスの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-659">Retrieves the ID for the process.</span></span>

```xpp
public int processId()
```

### <a name="return-value---processid"></a><span data-ttu-id="d3325-660">戻り値 - processId</span><span class="sxs-lookup"><span data-stu-id="d3325-660">Return Value - processId</span></span>

<span data-ttu-id="d3325-661">プロセスの ID。</span><span class="sxs-lookup"><span data-stu-id="d3325-661">The ID for the process.</span></span>

## <a name="method-projectrootnode"></a><span data-ttu-id="d3325-662">メソッド projectRootNode</span><span class="sxs-lookup"><span data-stu-id="d3325-662">Method projectRootNode</span></span>

<span data-ttu-id="d3325-663">X++ プロジェクト ノードを返します。</span><span class="sxs-lookup"><span data-stu-id="d3325-663">Returns the X++ Projects node.</span></span>

```xpp
public TreeNode projectRootNode()
```

### <a name="return-value---projectrootnode"></a><span data-ttu-id="d3325-664">戻り値 - projectRootNode</span><span class="sxs-lookup"><span data-stu-id="d3325-664">Return Value - projectRootNode</span></span>

<span data-ttu-id="d3325-665">X++ プロジェクトを含むツリー ノード。</span><span class="sxs-lookup"><span data-stu-id="d3325-665">The tree node that contains the X++ projects.</span></span>

### <a name="examples---projectrootnode"></a><span data-ttu-id="d3325-666">例 - projectRootNode</span><span class="sxs-lookup"><span data-stu-id="d3325-666">Examples - projectRootNode</span></span>

<span data-ttu-id="d3325-667">次の例では、共有プロジェクト フォルダー内のすべてのプロジェクトの名前を出力します。</span><span class="sxs-lookup"><span data-stu-id="d3325-667">The following example prints out the names of all the projects in the Shared projects folder.</span></span>

```xpp
void ProjectNames() 
{ 
    Treenode treenode; 
    TreenodeIterator it; 
    treenode = infolog.projectRootNode(); 
    treenode = treenode.AOTfindChild("Shared"); 
    it = treenode.AOTiterator(); 
    while (treenode) 
    { 
       print treenode.treeNodeName(); 
       treenode = it.next(); 
    } 
    pause; 
}
```

## <a name="method-rootnode"></a><span data-ttu-id="d3325-668">メソッド rootNode</span><span class="sxs-lookup"><span data-stu-id="d3325-668">Method rootNode</span></span>

<span data-ttu-id="d3325-669">アプリケーション オブジェクト ツリーのルートを取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-669">Retrieves the root of the application object tree.</span></span>

```xpp
public TreeNode rootNode()
```

### <a name="return-value---rootnode"></a><span data-ttu-id="d3325-670">戻り値 - rootNode</span><span class="sxs-lookup"><span data-stu-id="d3325-670">Return Value - rootNode</span></span>

<span data-ttu-id="d3325-671">アプリケーション オブジェクト ツリーのルート。</span><span class="sxs-lookup"><span data-stu-id="d3325-671">The root of the application object tree.</span></span>

### <a name="examples---rootnode"></a><span data-ttu-id="d3325-672">例 - rootNode</span><span class="sxs-lookup"><span data-stu-id="d3325-672">Examples - rootNode</span></span>

<span data-ttu-id="d3325-673">次の例では、AddressSelectForm クラスのメソッドのすべての名前を出力します。</span><span class="sxs-lookup"><span data-stu-id="d3325-673">The following example prints out all the names of the methods in the AddressSelectForm class.</span></span> <span data-ttu-id="d3325-674">rootnode メソッドは、子ノードを選択する前に、treenode オブジェクトを AOT ルートに設定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d3325-674">The rootnode method is used to set the treenode object to the AOT root before selecting a child node.</span></span>

```xpp
{ 
    Treenode treenode; 
    TreenodeIterator it; 
    treenode = infolog.rootNode(); 
    treenode = treenode.AOTfindChild("Classes"); 
    treenode = treenode.AOTfindChild("AddressSelectForm"); 
    it = treenode.AOTiterator(); 
    while (treenode) 
    { 
       print treenode.treeNodeName(); 
       treenode = it.next(); 
    } 
    pause; 
}
```

## <a name="method-startimport"></a><span data-ttu-id="d3325-675">メソッド startImport</span><span class="sxs-lookup"><span data-stu-id="d3325-675">Method startImport</span></span>

<span data-ttu-id="d3325-676">インポート コンテキストを作成します。</span><span class="sxs-lookup"><span data-stu-id="d3325-676">Creates an import context.</span></span>

```xpp
public int startImport(str file, int flag, [str labelSubstitutes])
```

### <a name="parameters---startimport"></a><span data-ttu-id="d3325-677">パラメーター - startImport</span><span class="sxs-lookup"><span data-stu-id="d3325-677">Parameters - startImport</span></span>

<span data-ttu-id="d3325-678">ファイル</span><span class="sxs-lookup"><span data-stu-id="d3325-678">file</span></span>  

<!-- -->

<span data-ttu-id="d3325-679">flag</span><span class="sxs-lookup"><span data-stu-id="d3325-679">flag</span></span>  

<!-- -->

<span data-ttu-id="d3325-680">labelSubstitutes</span><span class="sxs-lookup"><span data-stu-id="d3325-680">labelSubstitutes</span></span>  

### <a name="return-value---startimport"></a><span data-ttu-id="d3325-681">戻り値 - startImport</span><span class="sxs-lookup"><span data-stu-id="d3325-681">Return Value - startImport</span></span>

### <a name="remarks---startimport"></a><span data-ttu-id="d3325-682">備考 - startImport</span><span class="sxs-lookup"><span data-stu-id="d3325-682">Remarks - startImport</span></span>

<span data-ttu-id="d3325-683"> メソッドは廃止されています。</span><span class="sxs-lookup"><span data-stu-id="d3325-683">This method is obsolete.</span></span> <span data-ttu-id="d3325-684">代わりに SysImportElements クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="d3325-684">Use the SysImportElements class instead.</span></span>

## <a name="method-text"></a><span data-ttu-id="d3325-685">メソッド text</span><span class="sxs-lookup"><span data-stu-id="d3325-685">Method text</span></span>

<span data-ttu-id="d3325-686">情報ログからテキストの行を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-686">Retrieves a line of text from the Infolog.</span></span>

```xpp
public str text([int line])
```

### <a name="parameters---text"></a><span data-ttu-id="d3325-687">パラメーター - text</span><span class="sxs-lookup"><span data-stu-id="d3325-687">Parameters - text</span></span>

<span data-ttu-id="d3325-688">明細行</span><span class="sxs-lookup"><span data-stu-id="d3325-688">line</span></span>  
<span data-ttu-id="d3325-689">取得するテキストを含む情報ログ内の行。</span><span class="sxs-lookup"><span data-stu-id="d3325-689">The line in the Infolog with the text to retrieve.</span></span>

### <a name="return-value---text"></a><span data-ttu-id="d3325-690">戻り値 - text</span><span class="sxs-lookup"><span data-stu-id="d3325-690">Return Value - text</span></span>

<span data-ttu-id="d3325-691">情報ログのテキストを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="d3325-691">A string that contains the text from the Infolog.</span></span>

## <a name="method-usernode"></a><span data-ttu-id="d3325-692">メソッド userNode</span><span class="sxs-lookup"><span data-stu-id="d3325-692">Method userNode</span></span>

```xpp
public TreeNode userNode()
```

### <a name="return-value---usernode"></a><span data-ttu-id="d3325-693">戻り値 - userNode</span><span class="sxs-lookup"><span data-stu-id="d3325-693">Return Value - userNode</span></span>

## <a name="method-websession"></a><span data-ttu-id="d3325-694">メソッド webSession</span><span class="sxs-lookup"><span data-stu-id="d3325-694">Method webSession</span></span>

```xpp
public AnyType webSession([AnyType value])
```

### <a name="parameters---websession"></a><span data-ttu-id="d3325-695">パラメーター - webSession</span><span class="sxs-lookup"><span data-stu-id="d3325-695">Parameters - webSession</span></span>

<span data-ttu-id="d3325-696">値</span><span class="sxs-lookup"><span data-stu-id="d3325-696">value</span></span>  

### <a name="return-value---websession"></a><span data-ttu-id="d3325-697">戻り値 - webSession</span><span class="sxs-lookup"><span data-stu-id="d3325-697">Return Value - webSession</span></span>

## <a name="method-activexcontrols"></a><span data-ttu-id="d3325-698">メソッド activeXControls</span><span class="sxs-lookup"><span data-stu-id="d3325-698">Method activeXControls</span></span>

<span data-ttu-id="d3325-699">ActiveX コントロールの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-699">Retrieves a list of the ActiveX controls.</span></span>

```xpp
public static container activeXControls()
```

### <a name="return-value---activexcontrols"></a><span data-ttu-id="d3325-700">戻り値 - activeXControls</span><span class="sxs-lookup"><span data-stu-id="d3325-700">Return Value - activeXControls</span></span>

<span data-ttu-id="d3325-701">各 ActiveX コントロールに関する情報を保持する入れ子になったコンテナー。</span><span class="sxs-lookup"><span data-stu-id="d3325-701">A nested container that holds information about each of the ActiveX controls.</span></span>

### <a name="remarks---activexcontrols"></a><span data-ttu-id="d3325-702">備考 - activeXControls</span><span class="sxs-lookup"><span data-stu-id="d3325-702">Remarks - activeXControls</span></span>

<span data-ttu-id="d3325-703">返されるコンテナーには 4 つのコンテナーがあります。</span><span class="sxs-lookup"><span data-stu-id="d3325-703">The returned container contains four containers.</span></span> <span data-ttu-id="d3325-704">最初の内部コンテナーには、すべてのコントロールの名前が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d3325-704">The first inner container contains the names of all the controls.</span></span> <span data-ttu-id="d3325-705">2 番目の内部コンテナーには、各コントロールの ID (GUID) が格納されます。</span><span class="sxs-lookup"><span data-stu-id="d3325-705">The second inner container contains the ID for each control, which is a GUID.</span></span> <span data-ttu-id="d3325-706">3 番目の内部コンテナーには、各コントロールのセキュリティ設定が格納されます。</span><span class="sxs-lookup"><span data-stu-id="d3325-706">The third inner container contains the security setting for each control.</span></span> <span data-ttu-id="d3325-707">4 番目の内部コンテナーには、各コントロールの説明が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d3325-707">The fourth inner container contains a description of each control.</span></span>

### <a name="examples---activexcontrols"></a><span data-ttu-id="d3325-708">例 - activeXControls</span><span class="sxs-lookup"><span data-stu-id="d3325-708">Examples - activeXControls</span></span>

<span data-ttu-id="d3325-709">次の例は、各 ActiveX コントロールの説明を出力します。</span><span class="sxs-lookup"><span data-stu-id="d3325-709">The following example prints a description of each of the ActiveX controls.</span></span>

```xpp
static void activeXcontents(Args _args) 
{ 
    int       i; 
    str       strClsName, strTypeLibHelp, strClsId, strSafeForBits; 
    container c; 
    container clsName, clsId, safeForBits, typeLibHelp; 
    c = xinfo::activeXControls(); 
    clsName = conpeek(c, 1); 
    clsId = conpeek(c, 2); 
    safeForBits = conpeek(c, 3); 
    typeLibHelp = conpeek(c, 4); 
    for (i=1; i<conlen(clsName); i++) 
    { 
        strClsName = conpeek(clsName, i); 
        strClsId = conpeek(clsId, i); 
        strSafeForBits = conpeek(safeForBits, i); 
        strTypeLibHelp = conpeek(typeLibHelp, i); 
        print strClsName, " ", strClsId, " ", strSafeForBits, 
            " ", strTypeLibHelp; 
    } 
    pause; 
}
```

## <a name="method-aotlogdirectory"></a><span data-ttu-id="d3325-710">メソッド AOTLogDirectory</span><span class="sxs-lookup"><span data-stu-id="d3325-710">Method AOTLogDirectory</span></span>

<span data-ttu-id="d3325-711">現在のインストールのログ ディレクトリへのパスを取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-711">Gets the path to the log directory for the current installation.</span></span>

```xpp
public static str AOTLogDirectory()
```

### <a name="return-value---aotlogdirectory"></a><span data-ttu-id="d3325-712">戻り値 - AOTLogDirectory</span><span class="sxs-lookup"><span data-stu-id="d3325-712">Return Value - AOTLogDirectory</span></span>

<span data-ttu-id="d3325-713">現在のインストールのログ ディレクトリへのパスを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="d3325-713">A string that contains the path to the log directory for the current installation.</span></span>

### <a name="remarks---aotlogdirectory"></a><span data-ttu-id="d3325-714">備考 - AOTLogDirectory</span><span class="sxs-lookup"><span data-stu-id="d3325-714">Remarks - AOTLogDirectory</span></span>

<span data-ttu-id="d3325-715">AOT ログ オプションを有効にする場合は、コンパイルするたびにときに、ログ ディレクトリに情報が保存されます。</span><span class="sxs-lookup"><span data-stu-id="d3325-715">If you turn on the AOT Log option, information will be stored in the log directory each time you compile.</span></span> <span data-ttu-id="d3325-716">このオプションをオンにするには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="d3325-716">To turn on this option:</span></span>

1.  <span data-ttu-id="d3325-717">開発者ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="d3325-717">Open a developer workspace.</span></span>
2.  <span data-ttu-id="d3325-718">[ツール] &gt; [オプション] &gt; [開発]&gt; [コンパイラ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3325-718">Select Tools &gt; Options &gt; Development &gt; Compiler.</span></span>
3.  <span data-ttu-id="d3325-719">AOT ログ チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="d3325-719">Select the AOT log check box.</span></span>

## <a name="method-automationobjects"></a><span data-ttu-id="d3325-720">メソッド automationObjects</span><span class="sxs-lookup"><span data-stu-id="d3325-720">Method automationObjects</span></span>

<span data-ttu-id="d3325-721">使用可能な COM オブジェクトの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-721">Retrieves the list of COM objects that are available.</span></span>

```xpp
public static container automationObjects()
```

### <a name="return-value---automationobjects"></a><span data-ttu-id="d3325-722">戻り値 - automationObjects</span><span class="sxs-lookup"><span data-stu-id="d3325-722">Return Value - automationObjects</span></span>

<span data-ttu-id="d3325-723">各 COM オブジェクトの説明を保持する入れ子になったコンテナー。</span><span class="sxs-lookup"><span data-stu-id="d3325-723">A nested container that holds a description of each COM object.</span></span>

### <a name="examples---automationobjects"></a><span data-ttu-id="d3325-724">例 - automationObjects</span><span class="sxs-lookup"><span data-stu-id="d3325-724">Examples - automationObjects</span></span>

<span data-ttu-id="d3325-725">次の例では、automationObject から返される入れ子になったコンテナーを展開して、COM オブジェクトのリストを取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-725">The following example unpacks the nested container that is returned from automationObjects to get a list of COM objects.</span></span>

```xpp
void getAutomationObjects() 
{ 
    int idx; 
    FormListItem listItem; 
    int itemPos; 
    container clsGUID,clsDesc,clsVersion,clsPath; 
    [clsGUID,clsDesc,clsVersion,clsPath] = xInfo::automationObjects(); 
    for (idx = 1; idx < conlen(clsGUID); idx++) 
    { 
        itemPos = formListControl.add(conpeek(clsDesc,idx)); 
        listItem = formListControl.getItem(itemPos); 
        listItem.data(conpeek(clsPath,idx)); 
        formListControl.setItem(listItem); 
    } 
}
```

## <a name="method-buildno"></a><span data-ttu-id="d3325-726">メソッド buildNo</span><span class="sxs-lookup"><span data-stu-id="d3325-726">Method buildNo</span></span>

<span data-ttu-id="d3325-727">現在の実行可能ファイルのカーネル ビルド番号を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-727">Retrieves the kernel build number of the current executable.</span></span>

```xpp
public static str buildNo()
```

### <a name="return-value---buildno"></a><span data-ttu-id="d3325-728">戻り値 - buildNo</span><span class="sxs-lookup"><span data-stu-id="d3325-728">Return Value - buildNo</span></span>

<span data-ttu-id="d3325-729">カーネル ビルド番号を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="d3325-729">A string that contains the kernel build number.</span></span>

### <a name="examples---buildno"></a><span data-ttu-id="d3325-730">例 - buildNo</span><span class="sxs-lookup"><span data-stu-id="d3325-730">Examples - buildNo</span></span>

<span data-ttu-id="d3325-731">次の例では、このメソッドを使用して、バージョン情報を含む文字列の一部としてカーネル ビルド番号を返します。</span><span class="sxs-lookup"><span data-stu-id="d3325-731">The following example uses this method to return the kernel build number as part of a string that contains version information.</span></span>

```xpp
static client str axaptaReleaseID() 
{ 
    #define.versionPrefix('v') 
    #define.versionNumber('#') 
    #define.versionPartition('/') 
    return    #versionprefix+xInfo::releaseVersion()+ 
              #versionNumber+xInfo::buildNo()+ 
              #versionPartition+ApplicationVersion::buildNo(); 
}
```

## <a name="method-compilationdate"></a><span data-ttu-id="d3325-732">メソッド compilationDate</span><span class="sxs-lookup"><span data-stu-id="d3325-732">Method compilationDate</span></span>

<span data-ttu-id="d3325-733">現在のバージョンが最後にコンパイルされた日付を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-733">Retrieves the date on which the current version was last compiled.</span></span>

```xpp
public static str compilationDate()
```

### <a name="return-value---compilationdate"></a><span data-ttu-id="d3325-734">戻り値 - compilationDate</span><span class="sxs-lookup"><span data-stu-id="d3325-734">Return Value - compilationDate</span></span>

<span data-ttu-id="d3325-735">現在のバージョンが最後にコンパイルされた日付を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="d3325-735">A string that contains the date on which the current version was last compiled.</span></span>

### <a name="examples---compilationdate"></a><span data-ttu-id="d3325-736">例 - compilationDate</span><span class="sxs-lookup"><span data-stu-id="d3325-736">Examples - compilationDate</span></span>

<span data-ttu-id="d3325-737">次の例では、アプリケーションが最後にコンパイルされた日付を含むシステム情報を返します。</span><span class="sxs-lookup"><span data-stu-id="d3325-737">The following example returns system information, including the date on which the application was last compiled:</span></span>

```xpp
str environment() 
{ 
    return xInfo::buildNo() + ' - '  
        + xInfo::compilationDate() + ' - '  
        + xInfo::dbName() + ' - '  
        + xInfo::osName() + ' - '  
        + xInfo::productName() + ' - '  
        + xInfo::releaseVersion(); 
}
```

## <a name="method-compilationtime"></a><span data-ttu-id="d3325-738">メソッド compilationTime</span><span class="sxs-lookup"><span data-stu-id="d3325-738">Method compilationTime</span></span>

<span data-ttu-id="d3325-739">現在のバージョンが最後にコンパイルされた時刻を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-739">Retrieves the time at which the current version was last compiled.</span></span>

```xpp
public static str compilationTime()
```

### <a name="return-value---compilationtime"></a><span data-ttu-id="d3325-740">戻り値 - compilationTime</span><span class="sxs-lookup"><span data-stu-id="d3325-740">Return Value - compilationTime</span></span>

<span data-ttu-id="d3325-741">現在のバージョンが最後にコンパイルされた時刻を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="d3325-741">A string that contains the time at which the current version was last compiled.</span></span>

## <a name="method-componentname"></a><span data-ttu-id="d3325-742">メソッド componentName</span><span class="sxs-lookup"><span data-stu-id="d3325-742">Method componentName</span></span>

<span data-ttu-id="d3325-743">コンポーネントへのパスを取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-743">Retrieves the path to the component.</span></span>

```xpp
public static str componentName()
```

### <a name="return-value---componentname"></a><span data-ttu-id="d3325-744">戻り値 - componentName</span><span class="sxs-lookup"><span data-stu-id="d3325-744">Return Value - componentName</span></span>

<span data-ttu-id="d3325-745">実行可能ファイルへのパスを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="d3325-745">A string that contains the path to the executable.</span></span>

### <a name="remarks---componentname"></a><span data-ttu-id="d3325-746">備考 - componentName</span><span class="sxs-lookup"><span data-stu-id="d3325-746">Remarks - componentName</span></span>

<span data-ttu-id="d3325-747">このメソッドがクライアントで実行される場合、クライアントの .exe ファイルへのパスを返します。</span><span class="sxs-lookup"><span data-stu-id="d3325-747">If this method is run on the client, it returns the path to the .exe file for the client.</span></span> <span data-ttu-id="d3325-748">サーバーで実行する場合、AOS の .exe ファイルへのパスを返します。</span><span class="sxs-lookup"><span data-stu-id="d3325-748">If it is run on the server, it returns the path to the .exe file for the AOS.</span></span>

## <a name="method-configuration"></a><span data-ttu-id="d3325-749">メソッド configuration</span><span class="sxs-lookup"><span data-stu-id="d3325-749">Method configuration</span></span>

<span data-ttu-id="d3325-750">現在のクライアント構成を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-750">Retrieves the current client configuration.</span></span>

```xpp
public static str configuration()
```

### <a name="return-value---configuration"></a><span data-ttu-id="d3325-751">戻り値 - configuration</span><span class="sxs-lookup"><span data-stu-id="d3325-751">Return Value - configuration</span></span>

<span data-ttu-id="d3325-752">現在のクライアント コンフィギュレーションを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="d3325-752">A string that represents the current client configuration.</span></span>

### <a name="remarks---configuration"></a><span data-ttu-id="d3325-753">備考 - configuration</span><span class="sxs-lookup"><span data-stu-id="d3325-753">Remarks - configuration</span></span>

<span data-ttu-id="d3325-754">これは、クライアント構成ユーティリティー プログラムの「構成」ボックスで選択されている構成です。</span><span class="sxs-lookup"><span data-stu-id="d3325-754">This is the configuration that is selected in the Configuration box in the Client Configuration Utility program.</span></span> <span data-ttu-id="d3325-755">返される文字列の例としては「オリジナル (インストール済コンフィギュレーション)」です。</span><span class="sxs-lookup"><span data-stu-id="d3325-755">An example string that could be returned is "Original (installed configuration)".</span></span>

## <a name="method-currentworkspacenum"></a><span data-ttu-id="d3325-756">メソッド currentWorkspaceNum</span><span class="sxs-lookup"><span data-stu-id="d3325-756">Method currentWorkspaceNum</span></span>

<span data-ttu-id="d3325-757">現在のワークスペースのアプリケーション ウィンドウ ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-757">Retrieves the application window ID of the current workspace.</span></span>

```xpp
public static int currentWorkspaceNum()
```

### <a name="return-value---currentworkspacenum"></a><span data-ttu-id="d3325-758">戻り値 - currentWorkspaceNum</span><span class="sxs-lookup"><span data-stu-id="d3325-758">Return Value - currentWorkspaceNum</span></span>

<span data-ttu-id="d3325-759">現在のワークスペースのアプリケーション ウィンドウ ID。</span><span class="sxs-lookup"><span data-stu-id="d3325-759">The application window ID of the current workspace.</span></span>

### <a name="remarks---currentworkspacenum"></a><span data-ttu-id="d3325-760">備考 - currentWorkspaceNum</span><span class="sxs-lookup"><span data-stu-id="d3325-760">Remarks - currentWorkspaceNum</span></span>

<span data-ttu-id="d3325-761">createWorkspaceWindow メソッドを使用すると、アプリケーション内で追加のワークスペースを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="d3325-761">The createWorkspaceWindow method allows you to open additional workspaces in the application.</span></span>

## <a name="method-directory"></a><span data-ttu-id="d3325-762">メソッド directory</span><span class="sxs-lookup"><span data-stu-id="d3325-762">Method directory</span></span>

<span data-ttu-id="d3325-763">クライアントがインストールされているディレクトリへのパスを取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-763">Retrieves the path to the directory where the client has been installed.</span></span>

```xpp
public static str directory(DirectoryType type)
```

### <a name="parameters---directory"></a><span data-ttu-id="d3325-764">パラメーター - directory</span><span class="sxs-lookup"><span data-stu-id="d3325-764">Parameters - directory</span></span>

<span data-ttu-id="d3325-765">タイプ</span><span class="sxs-lookup"><span data-stu-id="d3325-765">type</span></span>  
<span data-ttu-id="d3325-766">クライアント インストールのサブフォルダーのいずれかを示す DirectoryType 列挙値。</span><span class="sxs-lookup"><span data-stu-id="d3325-766">A DirectoryType enumeration value that indicates one of the subfolders of the client installation.</span></span>

### <a name="return-value---directory"></a><span data-ttu-id="d3325-767">戻り値 - directory</span><span class="sxs-lookup"><span data-stu-id="d3325-767">Return Value - directory</span></span>

<span data-ttu-id="d3325-768">DirectoryType パラメーターで指定されているディレクトリへのパスを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="d3325-768">A string that contains the path to the directory that is specified by the DirectoryType parameter.</span></span>

### <a name="examples---directory"></a><span data-ttu-id="d3325-769">例 - directory</span><span class="sxs-lookup"><span data-stu-id="d3325-769">Examples - directory</span></span>

<span data-ttu-id="d3325-770">次の例は、現在のクライアント インストールの Bin ディレクトリへのパスを出力します。</span><span class="sxs-lookup"><span data-stu-id="d3325-770">The following example prints the path to the Bin directory for the current client installation.</span></span>

```xpp
{ 
    print xInfo::directory(DirectoryType::Bin); 
    pause; 
}
```

## <a name="method-expiredate"></a><span data-ttu-id="d3325-771">メソッド expireDate</span><span class="sxs-lookup"><span data-stu-id="d3325-771">Method expireDate</span></span>

<span data-ttu-id="d3325-772">現在のインストールのライセンスの有効期限が切れる日付を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-772">Retrieves the date on which the license for the current installation expires.</span></span>

```xpp
public static Date expireDate()
```

### <a name="return-value---expiredate"></a><span data-ttu-id="d3325-773">戻り値 - expireDate</span><span class="sxs-lookup"><span data-stu-id="d3325-773">Return Value - expireDate</span></span>

<span data-ttu-id="d3325-774">ライセンスの有効期限が切れる日を表す日付です。</span><span class="sxs-lookup"><span data-stu-id="d3325-774">A date that represents the date on which the license expires.</span></span>

## <a name="method-getapplicationobjecttreewindow"></a><span data-ttu-id="d3325-775">メソッド getApplicationObjectTreeWindow</span><span class="sxs-lookup"><span data-stu-id="d3325-775">Method getApplicationObjectTreeWindow</span></span>

```xpp
public static ApplicationObjectTreeWindow getApplicationObjectTreeWindow()
```

### <a name="return-value---getapplicationobjecttreewindow"></a><span data-ttu-id="d3325-776">戻り値 - getApplicationObjectTreeWindow</span><span class="sxs-lookup"><span data-stu-id="d3325-776">Return Value - getApplicationObjectTreeWindow</span></span>

## <a name="method-getcurrentmodelid"></a><span data-ttu-id="d3325-777">メソッド getCurrentModelId</span><span class="sxs-lookup"><span data-stu-id="d3325-777">Method getCurrentModelId</span></span>

```xpp
public static int getCurrentModelId()
```

### <a name="return-value---getcurrentmodelid"></a><span data-ttu-id="d3325-778">戻り値 - getCurrentModelId</span><span class="sxs-lookup"><span data-stu-id="d3325-778">Return Value - getCurrentModelId</span></span>

## <a name="method-getnumberofdecimals"></a><span data-ttu-id="d3325-779">メソッド getNumberOfDecimals</span><span class="sxs-lookup"><span data-stu-id="d3325-779">Method getNumberOfDecimals</span></span>

<span data-ttu-id="d3325-780">指定された数値の小数点以下の桁数を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-780">Retrieves the number of decimal places in the specified number.</span></span>

```xpp
public static int getNumberOfDecimals(Real number)
```

### <a name="parameters---getnumberofdecimals"></a><span data-ttu-id="d3325-781">パラメーター - getNumberOfDecimals</span><span class="sxs-lookup"><span data-stu-id="d3325-781">Parameters - getNumberOfDecimals</span></span>

<span data-ttu-id="d3325-782">番号</span><span class="sxs-lookup"><span data-stu-id="d3325-782">number</span></span>  
<span data-ttu-id="d3325-783">実数。</span><span class="sxs-lookup"><span data-stu-id="d3325-783">A real number.</span></span>

### <a name="return-value---getnumberofdecimals"></a><span data-ttu-id="d3325-784">戻り値 - getNumberOfDecimals</span><span class="sxs-lookup"><span data-stu-id="d3325-784">Return Value - getNumberOfDecimals</span></span>

<span data-ttu-id="d3325-785">数値パラメーターの小数点以下の桁数。</span><span class="sxs-lookup"><span data-stu-id="d3325-785">The number of decimal places in the number parameter.</span></span>

## <a name="method-getpropertieswindow"></a><span data-ttu-id="d3325-786">メソッド getPropertiesWindow</span><span class="sxs-lookup"><span data-stu-id="d3325-786">Method getPropertiesWindow</span></span>

```xpp
public static PropertiesWindow getPropertiesWindow()
```

### <a name="return-value---getpropertieswindow"></a><span data-ttu-id="d3325-787">戻り値 - getPropertiesWindow</span><span class="sxs-lookup"><span data-stu-id="d3325-787">Return Value - getPropertiesWindow</span></span>

## <a name="method-getsystemgeneratedmodelid"></a><span data-ttu-id="d3325-788">メソッド getSystemGeneratedModelId</span><span class="sxs-lookup"><span data-stu-id="d3325-788">Method getSystemGeneratedModelId</span></span>

```xpp
public static int getSystemGeneratedModelId(UtilEntryLevel layer)
```

### <a name="parameters---getsystemgeneratedmodelid"></a><span data-ttu-id="d3325-789">パラメーター - getSystemGeneratedModelId</span><span class="sxs-lookup"><span data-stu-id="d3325-789">Parameters - getSystemGeneratedModelId</span></span>

<span data-ttu-id="d3325-790"> レイヤー</span><span class="sxs-lookup"><span data-stu-id="d3325-790">layer</span></span>  

### <a name="return-value---getsystemgeneratedmodelid"></a><span data-ttu-id="d3325-791">戻り値 - getSystemGeneratedModelId</span><span class="sxs-lookup"><span data-stu-id="d3325-791">Return Value - getSystemGeneratedModelId</span></span>

## <a name="method-licensename"></a><span data-ttu-id="d3325-792">メソッド licenseName</span><span class="sxs-lookup"><span data-stu-id="d3325-792">Method licenseName</span></span>

<span data-ttu-id="d3325-793">現在のライセンスの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-793">Retrieves the name of the current license.</span></span>

```xpp
public static str licenseName()
```

### <a name="return-value---licensename"></a><span data-ttu-id="d3325-794">戻り値 - licenseName</span><span class="sxs-lookup"><span data-stu-id="d3325-794">Return Value - licenseName</span></span>

<span data-ttu-id="d3325-795">ライセンスの名前を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="d3325-795">A string that contains the name of the license.</span></span>

### <a name="remarks---licensename"></a><span data-ttu-id="d3325-796">備考 - licenseName</span><span class="sxs-lookup"><span data-stu-id="d3325-796">Remarks - licenseName</span></span>

<span data-ttu-id="d3325-797">xInfo::expireDate メソッドは、ライセンスが失効する日付を返します。</span><span class="sxs-lookup"><span data-stu-id="d3325-797">The xInfo::expireDate Method returns the date on which the license expires.</span></span> <span data-ttu-id="d3325-798">xInfo::serialNo メソッドは、ライセンスのシリアル番号を返します。</span><span class="sxs-lookup"><span data-stu-id="d3325-798">The xInfo::serialNo Method returns the serial number of the license.</span></span>

## <a name="method-productname"></a><span data-ttu-id="d3325-799">メソッド productName</span><span class="sxs-lookup"><span data-stu-id="d3325-799">Method productName</span></span>

<span data-ttu-id="d3325-800">製品の名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-800">Retrieves the name of the product.</span></span>

```xpp
public static str productName()
```

### <a name="return-value---productname"></a><span data-ttu-id="d3325-801">戻り値 - productName</span><span class="sxs-lookup"><span data-stu-id="d3325-801">Return Value - productName</span></span>

<span data-ttu-id="d3325-802">製品の名前を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="d3325-802">A string that contains the name of the product.</span></span>

### <a name="examples---productname"></a><span data-ttu-id="d3325-803">例 - productName</span><span class="sxs-lookup"><span data-stu-id="d3325-803">Examples - productName</span></span>

<span data-ttu-id="d3325-804">次の例では、製品の名前を含むシステム情報を戻します。</span><span class="sxs-lookup"><span data-stu-id="d3325-804">The following example returns system information, including the name of the product.</span></span>

```xpp
str environment() 
{ 
    return xInfo::buildNo() + ' - '  
        + xInfo::compilationDate() + ' - '  
        + xInfo::dbName() + ' - '  
        + xInfo::osName() + ' - '  
        + xInfo::productName() + ' - '  
        + xInfo::releaseVersion(); 
}
```

## <a name="method-productregisteredname"></a><span data-ttu-id="d3325-805">メソッド productRegisteredName</span><span class="sxs-lookup"><span data-stu-id="d3325-805">Method productRegisteredName</span></span>

```xpp
public static str productRegisteredName()
```

### <a name="return-value---productregisteredname"></a><span data-ttu-id="d3325-806">戻り値 - productRegisteredName</span><span class="sxs-lookup"><span data-stu-id="d3325-806">Return Value - productRegisteredName</span></span>

## <a name="method-releaseversion"></a><span data-ttu-id="d3325-807">メソッド releaseVersion</span><span class="sxs-lookup"><span data-stu-id="d3325-807">Method releaseVersion</span></span>

<span data-ttu-id="d3325-808">現在の実行可能ファイルのバージョン番号を取得します。例: 3.0、4.0。</span><span class="sxs-lookup"><span data-stu-id="d3325-808">Retrieves the version number of the current executable; for example: 3.0, or 4.0.</span></span>

```xpp
public static str releaseVersion()
```

### <a name="return-value---releaseversion"></a><span data-ttu-id="d3325-809">戻り値 - releaseVersion</span><span class="sxs-lookup"><span data-stu-id="d3325-809">Return Value - releaseVersion</span></span>

<span data-ttu-id="d3325-810">バージョン番号を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="d3325-810">A string containing the version number.</span></span>

### <a name="remarks---releaseversion"></a><span data-ttu-id="d3325-811">備考 - releaseVersion</span><span class="sxs-lookup"><span data-stu-id="d3325-811">Remarks - releaseVersion</span></span>

<span data-ttu-id="d3325-812">有効なバージョン番号は、3.0 および 4.0 などです。</span><span class="sxs-lookup"><span data-stu-id="d3325-812">Possible version numbers include 3.0 and 4.0.</span></span>

### <a name="examples---releaseversion"></a><span data-ttu-id="d3325-813">例 - releaseVersion</span><span class="sxs-lookup"><span data-stu-id="d3325-813">Examples - releaseVersion</span></span>

<span data-ttu-id="d3325-814">次の例では、これを使用して、バージョン情報を含む文字列の一部としてバージョン番号を返します。</span><span class="sxs-lookup"><span data-stu-id="d3325-814">The following example uses this return the version number as part of a string that contains version information.</span></span>

```xpp
static client str axaptaReleaseID() 
{ 
    #define.versionPrefix('v') 
    #define.versionNumber('#') 
    #define.versionPartition('/') 
    return    #versionprefix+xInfo::releaseVersion()+ 
              #versionNumber+xInfo::buildNo()+ 
              #versionPartition+ApplicationVersion::buildNo(); 
}
```

## <a name="method-releaseyear"></a><span data-ttu-id="d3325-815">メソッド releaseYear</span><span class="sxs-lookup"><span data-stu-id="d3325-815">Method releaseYear</span></span>

```xpp
public static str releaseYear()
```

### <a name="return-value---releaseyear"></a><span data-ttu-id="d3325-816">戻り値 - releaseYear</span><span class="sxs-lookup"><span data-stu-id="d3325-816">Return Value - releaseYear</span></span>

## <a name="method-serialno"></a><span data-ttu-id="d3325-817">メソッド serialNo</span><span class="sxs-lookup"><span data-stu-id="d3325-817">Method serialNo</span></span>

<span data-ttu-id="d3325-818">現在のライセンスのシリアル番号を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3325-818">Retrieves the serial number of the current license.</span></span>

```xpp
public static str serialNo()
```

### <a name="return-value---serialno"></a><span data-ttu-id="d3325-819">戻り値 - serialNo</span><span class="sxs-lookup"><span data-stu-id="d3325-819">Return Value - serialNo</span></span>

<span data-ttu-id="d3325-820">ライセンスのシリアル番号を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="d3325-820">A string that contains the serial number of the license.</span></span>

## <a name="method-new"></a><span data-ttu-id="d3325-821">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d3325-821">Method new</span></span>

<span data-ttu-id="d3325-822">新しい xInfo オブジェクトを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d3325-822">Initializes a new xInfo object.</span></span>

```xpp
public void new()
```

### <a name="remarks---new"></a><span data-ttu-id="d3325-823">備考 - new</span><span class="sxs-lookup"><span data-stu-id="d3325-823">Remarks - new</span></span>

<span data-ttu-id="d3325-824">注記: このメソッドを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="d3325-824">Note: Do not use this method.</span></span> <span data-ttu-id="d3325-825">代わりに、xInfo クラスのグローバル インスタンス infolog を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3325-825">You should use the global instance of the xInfo class, infolog, instead.</span></span> <span data-ttu-id="d3325-826">詳細については、「xInfo クラス」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d3325-826">For more information, see the xInfo class.</span></span>

## <a name="method-workspacewindowdestroyed"></a><span data-ttu-id="d3325-827">メソッド workspaceWindowDestroyed</span><span class="sxs-lookup"><span data-stu-id="d3325-827">Method workspaceWindowDestroyed</span></span>

<span data-ttu-id="d3325-828">新しいワークスペースが終了した時に実行します。</span><span class="sxs-lookup"><span data-stu-id="d3325-828">Executes when a workspace is closed.</span></span>

```xpp
public void workspaceWindowDestroyed(int hWnd)
```

### <a name="parameters---workspacewindowdestroyed"></a><span data-ttu-id="d3325-829">パラメーター - workspaceWindowDestroyed</span><span class="sxs-lookup"><span data-stu-id="d3325-829">Parameters - workspaceWindowDestroyed</span></span>

<span data-ttu-id="d3325-830">hWnd</span><span class="sxs-lookup"><span data-stu-id="d3325-830">hWnd</span></span>  
<span data-ttu-id="d3325-831">ワークスペースのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="d3325-831">The handle of the workspace.</span></span>

### <a name="remarks---workspacewindowdestroyed"></a><span data-ttu-id="d3325-832">備考 - workspaceWindowDestroyed</span><span class="sxs-lookup"><span data-stu-id="d3325-832">Remarks - workspaceWindowDestroyed</span></span>

<span data-ttu-id="d3325-833">このメソッドは、新しいワークスペースが閉じられるときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d3325-833">This method is called when a new workspace is closed.</span></span> <span data-ttu-id="d3325-834">これにより、発生したときにアクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="d3325-834">It allows you to perform an action when this occurs.</span></span>

## <a name="method-writecustomstatlineitem"></a><span data-ttu-id="d3325-835">メソッド writeCustomStatlineItem</span><span class="sxs-lookup"><span data-stu-id="d3325-835">Method writeCustomStatlineItem</span></span>

<span data-ttu-id="d3325-836">テキストの行をステータス バーに記述します。</span><span class="sxs-lookup"><span data-stu-id="d3325-836">Writes a line of text to the status bar.</span></span>

```xpp
public void writeCustomStatlineItem(str text)
```

### <a name="parameters---writecustomstatlineitem"></a><span data-ttu-id="d3325-837">パラメーター - writeCustomStatlineItem</span><span class="sxs-lookup"><span data-stu-id="d3325-837">Parameters - writeCustomStatlineItem</span></span>

<span data-ttu-id="d3325-838">テキスト</span><span class="sxs-lookup"><span data-stu-id="d3325-838">text</span></span>  
<span data-ttu-id="d3325-839">ステータス バーに入れるテキストの行。</span><span class="sxs-lookup"><span data-stu-id="d3325-839">The line of text to put on the status bar.</span></span>

## <a name="method-reloadrunningmode"></a><span data-ttu-id="d3325-840">メソッド reloadRunningMode</span><span class="sxs-lookup"><span data-stu-id="d3325-840">Method reloadRunningMode</span></span>

```xpp
public void reloadRunningMode()
```

## <a name="method-setwindoworder"></a><span data-ttu-id="d3325-841">メソッド setWindowOrder</span><span class="sxs-lookup"><span data-stu-id="d3325-841">Method setWindowOrder</span></span>

<span data-ttu-id="d3325-842">Windows の表示順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="d3325-842">Sets the order in which windows should be displayed.</span></span>

```xpp
public void setWindowOrder(int window, [int afterWindow])
```

### <a name="parameters---setwindoworder"></a><span data-ttu-id="d3325-843">パラメーター - setWindowOrder</span><span class="sxs-lookup"><span data-stu-id="d3325-843">Parameters - setWindowOrder</span></span>

<span data-ttu-id="d3325-844">window</span><span class="sxs-lookup"><span data-stu-id="d3325-844">window</span></span>  
<span data-ttu-id="d3325-845">ウィンドウ パラメーターで指定されたウィンドウの後に配置するウィンドウのハンドルです (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d3325-845">The handle to the window to place after the window specified by the window parameter; optional.</span></span>

<!-- -->

<span data-ttu-id="d3325-846">afterWindow</span><span class="sxs-lookup"><span data-stu-id="d3325-846">afterWindow</span></span>  
<span data-ttu-id="d3325-847">ウィンドウ パラメーターで指定されたウィンドウの後に配置するウィンドウのハンドルです (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d3325-847">The handle to the window to place after the window specified by the window parameter; optional.</span></span>

### <a name="examples---setwindoworder"></a><span data-ttu-id="d3325-848">例 - setWindowOrder</span><span class="sxs-lookup"><span data-stu-id="d3325-848">Examples - setWindowOrder</span></span>

<span data-ttu-id="d3325-849">次の例では、ウィンドウにフォーカスを設定し、ウィンドウを前面に移動します。</span><span class="sxs-lookup"><span data-stu-id="d3325-849">The following example sets focus on a window and brings it to the front.</span></span>

```xpp
void setFocus() 
{ 
    infolog.activateWindow(element.hWnd()); 
    infolog.setWindowOrder(element.hWnd()); 
}
```

## <a name="method-shutdown"></a><span data-ttu-id="d3325-850">メソッド shutDown</span><span class="sxs-lookup"><span data-stu-id="d3325-850">Method shutDown</span></span>

<span data-ttu-id="d3325-851">クライアントをシャットダウンします。</span><span class="sxs-lookup"><span data-stu-id="d3325-851">Shuts down the client.</span></span>

```xpp
public void shutDown(boolean force)
```

### <a name="parameters---shutdown"></a><span data-ttu-id="d3325-852">パラメーター - shutDown</span><span class="sxs-lookup"><span data-stu-id="d3325-852">Parameters - shutDown</span></span>

<span data-ttu-id="d3325-853">force</span><span class="sxs-lookup"><span data-stu-id="d3325-853">force</span></span>  
<span data-ttu-id="d3325-854">シャット ダウンを防止するオプションが、ユーザーに与えられたかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d3325-854">A Boolean value that indicates whether the user is given the option to prevent the shutdown.</span></span>

## <a name="method-xref"></a><span data-ttu-id="d3325-855">メソッド xref</span><span class="sxs-lookup"><span data-stu-id="d3325-855">Method xref</span></span>

<span data-ttu-id="d3325-856">相互参照システムが使用される時に実行します。</span><span class="sxs-lookup"><span data-stu-id="d3325-856">Executes when the cross-reference system is used.</span></span>

```xpp
public void xref(str path, xRef x)
```

### <a name="parameters---xref"></a><span data-ttu-id="d3325-857">パラメーター - xref</span><span class="sxs-lookup"><span data-stu-id="d3325-857">Parameters - xref</span></span>

<span data-ttu-id="d3325-858">path</span><span class="sxs-lookup"><span data-stu-id="d3325-858">path</span></span>  

<!-- -->

<span data-ttu-id="d3325-859">x</span><span class="sxs-lookup"><span data-stu-id="d3325-859">x</span></span>  

### <a name="remarks---xref"></a><span data-ttu-id="d3325-860">備考 - xref</span><span class="sxs-lookup"><span data-stu-id="d3325-860">Remarks - xref</span></span>

<span data-ttu-id="d3325-861">このメソッドを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="d3325-861">Do not use this method.</span></span>

## <a name="method-updatecurrentcompany"></a><span data-ttu-id="d3325-862">メソッド updateCurrentCompany</span><span class="sxs-lookup"><span data-stu-id="d3325-862">Method updateCurrentCompany</span></span>

```xpp
public void updateCurrentCompany()
```

## <a name="method-redrawallwindows"></a><span data-ttu-id="d3325-863">メソッド redrawAllWindows</span><span class="sxs-lookup"><span data-stu-id="d3325-863">Method redrawAllWindows</span></span>

<span data-ttu-id="d3325-864">すべてのウィンドウを再描画します。</span><span class="sxs-lookup"><span data-stu-id="d3325-864">Redraws all windows.</span></span>

```xpp
public void redrawAllWindows()
```

### <a name="remarks---redrawallwindows"></a><span data-ttu-id="d3325-865">備考 - redrawAllWindows</span><span class="sxs-lookup"><span data-stu-id="d3325-865">Remarks - redrawAllWindows</span></span>

<span data-ttu-id="d3325-866">このメソッドは、長いプロセス中に表示を更新するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="d3325-866">This method can be used to update the display during a long process.</span></span>

## <a name="method-formnotify"></a><span data-ttu-id="d3325-867">メソッド formNotify</span><span class="sxs-lookup"><span data-stu-id="d3325-867">Method formNotify</span></span>

<span data-ttu-id="d3325-868">特定フォームへの変更特定タイプに基づいて実行し、カスタムコードの実行を許可します。</span><span class="sxs-lookup"><span data-stu-id="d3325-868">Executes based on a particular type of change to a specific form, allowing custom code to run.</span></span>

```xpp
public void formNotify(xFormRun form, FormNotify notification, [FormNotifyEventArgs formNotifyEventArgs])
```

### <a name="parameters---formnotify"></a><span data-ttu-id="d3325-869">パラメーター - formNotify</span><span class="sxs-lookup"><span data-stu-id="d3325-869">Parameters - formNotify</span></span>

<span data-ttu-id="d3325-870">フォーム</span><span class="sxs-lookup"><span data-stu-id="d3325-870">form</span></span>  

<!-- -->

<span data-ttu-id="d3325-871">通知</span><span class="sxs-lookup"><span data-stu-id="d3325-871">notification</span></span>  

<!-- -->

<span data-ttu-id="d3325-872">formNotifyEventArgs</span><span class="sxs-lookup"><span data-stu-id="d3325-872">formNotifyEventArgs</span></span>  

### <a name="remarks---formnotify"></a><span data-ttu-id="d3325-873">備考 - formNotify</span><span class="sxs-lookup"><span data-stu-id="d3325-873">Remarks - formNotify</span></span>

<span data-ttu-id="d3325-874">通知パラメーターの使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d3325-874">Possible values for the notification parameter are:</span></span>

-   <span data-ttu-id="d3325-875">アクティブ化</span><span class="sxs-lookup"><span data-stu-id="d3325-875">Activate</span></span>
-   <span data-ttu-id="d3325-876">DeActivate</span><span class="sxs-lookup"><span data-stu-id="d3325-876">DeActivate</span></span>
-   <span data-ttu-id="d3325-877">求人開始</span><span class="sxs-lookup"><span data-stu-id="d3325-877">Open</span></span>
-   <span data-ttu-id="d3325-878">終了</span><span class="sxs-lookup"><span data-stu-id="d3325-878">Close</span></span>
-   <span data-ttu-id="d3325-879">RecordChange</span><span class="sxs-lookup"><span data-stu-id="d3325-879">RecordChange</span></span>
-   <span data-ttu-id="d3325-880">NoteClicked</span><span class="sxs-lookup"><span data-stu-id="d3325-880">NoteClicked</span></span>

<span data-ttu-id="d3325-881">このメソッドの使用例については、このメソッドが上書きされた情報クラスの formNotify メソッドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d3325-881">For an example of the usage of this method, see the formNotify method of the Info class, where this method has been overridden.</span></span>

## <a name="method-mayreloadmenu"></a><span data-ttu-id="d3325-882">メソッド mayReloadMenu</span><span class="sxs-lookup"><span data-stu-id="d3325-882">Method mayReloadMenu</span></span>

<span data-ttu-id="d3325-883">UI を更新できないようにする</span><span class="sxs-lookup"><span data-stu-id="d3325-883">Prevents the UI from refreshing.</span></span>

```xpp
public void mayReloadMenu(boolean value)
```

### <a name="parameters---mayreloadmenu"></a><span data-ttu-id="d3325-884">パラメーター - mayReloadMenu</span><span class="sxs-lookup"><span data-stu-id="d3325-884">Parameters - mayReloadMenu</span></span>

<span data-ttu-id="d3325-885">値</span><span class="sxs-lookup"><span data-stu-id="d3325-885">value</span></span>  
<span data-ttu-id="d3325-886">UI が更新されないようにするかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="d3325-886">A Boolean value that indicates whether to prevent the UI from refreshing.</span></span>

### <a name="remarks---mayreloadmenu"></a><span data-ttu-id="d3325-887">備考 - mayReloadMenu</span><span class="sxs-lookup"><span data-stu-id="d3325-887">Remarks - mayReloadMenu</span></span>

<span data-ttu-id="d3325-888">プロセスが実行されたときに UI が更新されないように値を false に設定し、プロセスが終了した後は true に設定します。</span><span class="sxs-lookup"><span data-stu-id="d3325-888">Set the value to false to prevent the UI from refreshing when a process is executing, and then set it to true after the process has finished.</span></span> <span data-ttu-id="d3325-889">mayReloadMenu メソッドは、AOT 内の多くのノードが読み取られているなど、UI がちらつくのを防ぐのに便利です。</span><span class="sxs-lookup"><span data-stu-id="d3325-889">The mayReloadMenu method can be useful to prevent the UI from flickering, for example when many nodes in the AOT are being read.</span></span>

## <a name="method-startlengthyoperation"></a><span data-ttu-id="d3325-890">メソッド startLengthyOperation</span><span class="sxs-lookup"><span data-stu-id="d3325-890">Method startLengthyOperation</span></span>

<span data-ttu-id="d3325-891">マウス カーソルをアイドルに設定します。</span><span class="sxs-lookup"><span data-stu-id="d3325-891">Sets the mouse cursor to idle.</span></span>

```xpp
public void startLengthyOperation()
```

### <a name="remarks---startlengthyoperation"></a><span data-ttu-id="d3325-892">備考 - startLengthyOperation</span><span class="sxs-lookup"><span data-stu-id="d3325-892">Remarks - startLengthyOperation</span></span>

<span data-ttu-id="d3325-893">時間のかかる操作の開始時に、プロセスが進行中であることを示すために使用します。</span><span class="sxs-lookup"><span data-stu-id="d3325-893">Use at the start of a lengthy operation to indicate that a process is in progress.</span></span> <span data-ttu-id="d3325-894">工程が完了したら、システムは endLengthyOperation メソッドを自動的に呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d3325-894">When the operation has finished, the system automatically calls the endLengthyOperation method.</span></span>

## <a name="method-breakpointnotify"></a><span data-ttu-id="d3325-895">メソッド breakpointNotify</span><span class="sxs-lookup"><span data-stu-id="d3325-895">Method breakpointNotify</span></span>

<span data-ttu-id="d3325-896">ブレークポイントが変更されたときの通知システムを実装します。</span><span class="sxs-lookup"><span data-stu-id="d3325-896">Implements a notification system when a breakpoint is changed.</span></span>

```xpp
public void breakpointNotify(BreakpointNotify notification)
```

### <a name="parameters---breakpointnotify"></a><span data-ttu-id="d3325-897">パラメーター - breakpointNotify</span><span class="sxs-lookup"><span data-stu-id="d3325-897">Parameters - breakpointNotify</span></span>

<span data-ttu-id="d3325-898">通知</span><span class="sxs-lookup"><span data-stu-id="d3325-898">notification</span></span>  
<span data-ttu-id="d3325-899">ブレークポイントに発生した変更のタイプを指定する BreakpointNotify システム列挙値。</span><span class="sxs-lookup"><span data-stu-id="d3325-899">A BreakpointNotify system enumeration value that specifies the type of change that has occurred to the breakpoints.</span></span>

### <a name="remarks---breakpointnotify"></a><span data-ttu-id="d3325-900">備考 - breakpointNotify</span><span class="sxs-lookup"><span data-stu-id="d3325-900">Remarks - breakpointNotify</span></span>

<span data-ttu-id="d3325-901">アプリケーションで、このメソッドはコード エディター ウィンドウでのブレークポイントの変更時に、ブレークポイント フォームを更新するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d3325-901">In the application, this method is used to update the Breakpoints form when a change is made to a breakpoint in the Code Editor window.</span></span> <span data-ttu-id="d3325-902">通知パラメーターには、次の BreakpointNotify 列挙型の値が有効です。</span><span class="sxs-lookup"><span data-stu-id="d3325-902">The following values of the BreakpointNotify enumeration type are valid for the notification parameter:</span></span>

-   <span data-ttu-id="d3325-903">BreakpointForm: ブレークポイント リストを再読み込みする必要があることをクライアントに通知します。</span><span class="sxs-lookup"><span data-stu-id="d3325-903">BreakpointForm: Notifies the client that the breakpoint list should be reloaded.</span></span>
-   <span data-ttu-id="d3325-904">BreakpointChange: クライアントとサーバーにブレークポイントの状態が変更 (有効、無効、または削除) されたことを通知します。</span><span class="sxs-lookup"><span data-stu-id="d3325-904">BreakpointChange: Notifies the client and server that the status of a breakpoint has changed (enabled, disabled, or deleted).</span></span>

## <a name="method-initializeinfolog"></a><span data-ttu-id="d3325-905">メソッド initializeInfolog</span><span class="sxs-lookup"><span data-stu-id="d3325-905">Method initializeInfolog</span></span>

```xpp
public void initializeInfolog(int window)
```

### <a name="parameters---initializeinfolog"></a><span data-ttu-id="d3325-906">パラメーター - initializeInfolog</span><span class="sxs-lookup"><span data-stu-id="d3325-906">Parameters - initializeInfolog</span></span>

<span data-ttu-id="d3325-907">window</span><span class="sxs-lookup"><span data-stu-id="d3325-907">window</span></span>  

## <a name="method-startup"></a><span data-ttu-id="d3325-908">メソッド startup</span><span class="sxs-lookup"><span data-stu-id="d3325-908">Method startup</span></span>

<span data-ttu-id="d3325-909">クライアントの起動時に実行します。</span><span class="sxs-lookup"><span data-stu-id="d3325-909">Executes when the client starts.</span></span>

```xpp
public void startup(str startupCmd)
```

### <a name="parameters---startup"></a><span data-ttu-id="d3325-910">パラメーター - startup</span><span class="sxs-lookup"><span data-stu-id="d3325-910">Parameters - startup</span></span>

<span data-ttu-id="d3325-911">startupCmd</span><span class="sxs-lookup"><span data-stu-id="d3325-911">startupCmd</span></span>  

### <a name="remarks---startup"></a><span data-ttu-id="d3325-912">備考 - startup</span><span class="sxs-lookup"><span data-stu-id="d3325-912">Remarks - startup</span></span>

<span data-ttu-id="d3325-913">このメソッドを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="d3325-913">Do not use this method.</span></span> <span data-ttu-id="d3325-914">代わりに次の方法のいずれかを使用します。</span><span class="sxs-lookup"><span data-stu-id="d3325-914">Use one following methods instead.</span></span> <span data-ttu-id="d3325-915">起動コマンドをクライアントに渡すには Info.startupPost メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d3325-915">Use the Info.startupPost Method to pass startup commands to the client.</span></span> <span data-ttu-id="d3325-916">起動コマンドをサーバーに渡すには Application.startupPost メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d3325-916">Use the Application.startupPost Method to pass startup commands to the server.</span></span> <span data-ttu-id="d3325-917">Application.startup または Info.startup メソッドを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="d3325-917">Do not use the Application.startup or Info.startup methods.</span></span> <span data-ttu-id="d3325-918">これは新しいバージョンのコードに影響する可能性があり、クライアントまたはサーバーの起動を妨げる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d3325-918">This might affect code in a new version, which could prevent the client or server from starting.</span></span>

## <a name="method-endimport"></a><span data-ttu-id="d3325-919">メソッド endImport</span><span class="sxs-lookup"><span data-stu-id="d3325-919">Method endImport</span></span>

<span data-ttu-id="d3325-920">インポート プロセスを完了します。</span><span class="sxs-lookup"><span data-stu-id="d3325-920">Completes an import process.</span></span>

```xpp
public void endImport(int id, int elements)
```

### <a name="parameters---endimport"></a><span data-ttu-id="d3325-921">パラメーター - endImport</span><span class="sxs-lookup"><span data-stu-id="d3325-921">Parameters - endImport</span></span>

<span data-ttu-id="d3325-922">id</span><span class="sxs-lookup"><span data-stu-id="d3325-922">id</span></span>  

<!-- -->

<span data-ttu-id="d3325-923">elements</span><span class="sxs-lookup"><span data-stu-id="d3325-923">elements</span></span>  

### <a name="remarks---endimport"></a><span data-ttu-id="d3325-924">備考 - endImport</span><span class="sxs-lookup"><span data-stu-id="d3325-924">Remarks - endImport</span></span>

<span data-ttu-id="d3325-925"> メソッドは廃止されています。</span><span class="sxs-lookup"><span data-stu-id="d3325-925">This method is obsolete.</span></span> <span data-ttu-id="d3325-926">代わりに SysImportElements クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="d3325-926">Use the SysImportElements class instead.</span></span>

## <a name="method-yield"></a><span data-ttu-id="d3325-927">メソッド yield</span><span class="sxs-lookup"><span data-stu-id="d3325-927">Method yield</span></span>

```xpp
public void yield()
```

## <a name="method-viewalertinbox"></a><span data-ttu-id="d3325-928">メソッド viewAlertInbox</span><span class="sxs-lookup"><span data-stu-id="d3325-928">Method viewAlertInbox</span></span>

<span data-ttu-id="d3325-929">警告の表示フォームを起動します。</span><span class="sxs-lookup"><span data-stu-id="d3325-929">Launches the View alerts form.</span></span>

```xpp
public void viewAlertInbox([int selectedTab])
```

### <a name="parameters---viewalertinbox"></a><span data-ttu-id="d3325-930">パラメーター - viewAlertInbox</span><span class="sxs-lookup"><span data-stu-id="d3325-930">Parameters - viewAlertInbox</span></span>

<span data-ttu-id="d3325-931">selectedTab</span><span class="sxs-lookup"><span data-stu-id="d3325-931">selectedTab</span></span>  
<span data-ttu-id="d3325-932">警告の表示フォームが表示されるタブを決定します。オプション。</span><span class="sxs-lookup"><span data-stu-id="d3325-932">Determines which tab the View alerts form opens on; optional.</span></span>

### <a name="remarks---viewalertinbox"></a><span data-ttu-id="d3325-933">備考 - viewAlertInbox</span><span class="sxs-lookup"><span data-stu-id="d3325-933">Remarks - viewAlertInbox</span></span>

<span data-ttu-id="d3325-934">selectedTab パラメーターの既定値は、最初のタブである概要です。xInfo.canViewAlertInbox メソッドを呼び出して、ユーザーがこのフォームを表示する権限を持っているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="d3325-934">The default value for the selectedTab parameter is Overview, the first tab. Call the xInfo.canViewAlertInbox Method to check whether the user has permission to view this form.</span></span>

## <a name="method-reportsendmailserver"></a><span data-ttu-id="d3325-935">メソッド reportSendMailServer</span><span class="sxs-lookup"><span data-stu-id="d3325-935">Method reportSendMailServer</span></span>

```xpp
public void reportSendMailServer(PrintJobSettings settings)
```

### <a name="parameters---reportsendmailserver"></a><span data-ttu-id="d3325-936">パラメーター - reportSendMailServer</span><span class="sxs-lookup"><span data-stu-id="d3325-936">Parameters - reportSendMailServer</span></span>

<span data-ttu-id="d3325-937">設定</span><span class="sxs-lookup"><span data-stu-id="d3325-937">settings</span></span>  

## <a name="method-endlengthyoperation"></a><span data-ttu-id="d3325-938">メソッド endLengthyOperation</span><span class="sxs-lookup"><span data-stu-id="d3325-938">Method endLengthyOperation</span></span>

<span data-ttu-id="d3325-939">startLengthyOperation の呼び出し後にマウス カーソルが標準に戻るように設定します。</span><span class="sxs-lookup"><span data-stu-id="d3325-939">Sets the mouse cursor back to normal after a call to startLengthyOperation.</span></span>

```xpp
public void endLengthyOperation([boolean endAll])
```

### <a name="parameters---endlengthyoperation"></a><span data-ttu-id="d3325-940">パラメータ－ - endLengthyOperation</span><span class="sxs-lookup"><span data-stu-id="d3325-940">Parameters - endLengthyOperation</span></span>

<span data-ttu-id="d3325-941">endAll</span><span class="sxs-lookup"><span data-stu-id="d3325-941">endAll</span></span>  
<span data-ttu-id="d3325-942">予約済み。</span><span class="sxs-lookup"><span data-stu-id="d3325-942">Reserved.</span></span>

### <a name="remarks---endlengthyoperation"></a><span data-ttu-id="d3325-943">備考 - endLengthyOperation</span><span class="sxs-lookup"><span data-stu-id="d3325-943">Remarks - endLengthyOperation</span></span>

<span data-ttu-id="d3325-944">このメソッドを呼び出さないことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d3325-944">It is best practice not to call this method.</span></span> <span data-ttu-id="d3325-945">操作が終了すると、システムによって自動的に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d3325-945">It will be called automatically by the system when the operation has ended.</span></span> <span data-ttu-id="d3325-946">明示的にこのメソッドを呼び出し、その他のプロセスまたはループのコードがある場合は、このメソッドを使用すると、マウス ポインターが点滅する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d3325-946">If you call this method explicitly and there are other processes, or looping code, that use the method, it could lead to the mouse pointer flickering.</span></span>

## <a name="method-setnumunreadalerts"></a><span data-ttu-id="d3325-947">メソッド setNumUnreadAlerts</span><span class="sxs-lookup"><span data-stu-id="d3325-947">Method setNumUnreadAlerts</span></span>

<span data-ttu-id="d3325-948">未読の警告メールの数が変わると、ステータス バーのテキストを更新します。</span><span class="sxs-lookup"><span data-stu-id="d3325-948">Refreshes the status bar text when the number of unread Alert e-mails changes.</span></span>

```xpp
public void setNumUnreadAlerts([int n])
```

### <a name="parameters---setnumunreadalerts"></a><span data-ttu-id="d3325-949">パラメーター - setNumUnreadAlerts</span><span class="sxs-lookup"><span data-stu-id="d3325-949">Parameters - setNumUnreadAlerts</span></span>

<span data-ttu-id="d3325-950">n</span><span class="sxs-lookup"><span data-stu-id="d3325-950">n</span></span>  
<span data-ttu-id="d3325-951">未読メールの数を特定の番号に設定できます。</span><span class="sxs-lookup"><span data-stu-id="d3325-951">Allows you to set the number of unread e-mails to a specific number.</span></span>

## <a name="method-truncate"></a><span data-ttu-id="d3325-952">メソッド truncate</span><span class="sxs-lookup"><span data-stu-id="d3325-952">Method truncate</span></span>

<span data-ttu-id="d3325-953">情報ログから指定した接頭語の付いた品目を削除します。</span><span class="sxs-lookup"><span data-stu-id="d3325-953">Removes the items with the specified prefix from the Infolog.</span></span>

```xpp
public void truncate(str prefix)
```

### <a name="parameters---truncate"></a><span data-ttu-id="d3325-954">パラメーター - truncate</span><span class="sxs-lookup"><span data-stu-id="d3325-954">Parameters - truncate</span></span>

<span data-ttu-id="d3325-955">prefix</span><span class="sxs-lookup"><span data-stu-id="d3325-955">prefix</span></span>  
<span data-ttu-id="d3325-956">情報ログから削除する必要のある項目の接頭語。</span><span class="sxs-lookup"><span data-stu-id="d3325-956">The prefix for the items that you want to remove from the Infolog.</span></span>

## <a name="method-formnotebutton"></a><span data-ttu-id="d3325-957">メソッド formNoteButton</span><span class="sxs-lookup"><span data-stu-id="d3325-957">Method formNoteButton</span></span>

<span data-ttu-id="d3325-958">ツールバーのドキュメント処理ボタンをコントロールします。</span><span class="sxs-lookup"><span data-stu-id="d3325-958">Controls the Document handling button on the toolbar.</span></span>

```xpp
public void formNoteButton(boolean enable, boolean value)
```

### <a name="parameters---formnotebutton"></a><span data-ttu-id="d3325-959">パラメーター - formNoteButton</span><span class="sxs-lookup"><span data-stu-id="d3325-959">Parameters - formNoteButton</span></span>

<span data-ttu-id="d3325-960">enable</span><span class="sxs-lookup"><span data-stu-id="d3325-960">enable</span></span>  
<span data-ttu-id="d3325-961">アイコンの表示が示すブール値データ型。</span><span class="sxs-lookup"><span data-stu-id="d3325-961">A Boolean data type that indicates the appearance of the icon.</span></span>

<!-- -->

<span data-ttu-id="d3325-962">値</span><span class="sxs-lookup"><span data-stu-id="d3325-962">value</span></span>  
<span data-ttu-id="d3325-963">アイコンの表示が示すブール値データ型。</span><span class="sxs-lookup"><span data-stu-id="d3325-963">A Boolean data type that indicates the appearance of the icon.</span></span>

### <a name="examples---formnotebutton"></a><span data-ttu-id="d3325-964">例 - formNoteButton</span><span class="sxs-lookup"><span data-stu-id="d3325-964">Examples - formNoteButton</span></span>

<span data-ttu-id="d3325-965">次の例は、ドキュメント処理ボタンを無効にする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="d3325-965">The following example shows how to disable the Document handling button.</span></span>

```xpp
void disableNoteButton() 
    { 
        infolog.formNoteButton(false, false); 
    }
```

## <a name="method-viewcreateruledialog"></a><span data-ttu-id="d3325-966">メソッド viewCreateRuleDialog</span><span class="sxs-lookup"><span data-stu-id="d3325-966">Method viewCreateRuleDialog</span></span>

<span data-ttu-id="d3325-967">警告ルールの作成フォームを起動します。</span><span class="sxs-lookup"><span data-stu-id="d3325-967">Launches the Create alert rule form.</span></span>

```xpp
public void viewCreateRuleDialog(xFormRun caller)
```

### <a name="parameters---viewcreateruledialog"></a><span data-ttu-id="d3325-968">パラメーター - viewCreateRuleDialog</span><span class="sxs-lookup"><span data-stu-id="d3325-968">Parameters - viewCreateRuleDialog</span></span>

<span data-ttu-id="d3325-969">caller</span><span class="sxs-lookup"><span data-stu-id="d3325-969">caller</span></span>  
<span data-ttu-id="d3325-970">現在のフォーム。</span><span class="sxs-lookup"><span data-stu-id="d3325-970">The current form.</span></span>

### <a name="remarks---viewcreateruledialog"></a><span data-ttu-id="d3325-971">備考 - viewCreateRuleDialog</span><span class="sxs-lookup"><span data-stu-id="d3325-971">Remarks - viewCreateRuleDialog</span></span>

<span data-ttu-id="d3325-972">作成警告ルール フォームは、呼び出し元のパラメーターで指定された現在のフォームから起動されます。</span><span class="sxs-lookup"><span data-stu-id="d3325-972">The Create alert rule form will be launched from the current form, as specified by the caller parameter.</span></span>

## <a name="method-view"></a><span data-ttu-id="d3325-973">メソッド view</span><span class="sxs-lookup"><span data-stu-id="d3325-973">Method view</span></span>

```xpp
public void view([container container])
```

### <a name="parameters---view"></a><span data-ttu-id="d3325-974">パラメーター - view</span><span class="sxs-lookup"><span data-stu-id="d3325-974">Parameters - view</span></span>

<span data-ttu-id="d3325-975">コンテナー</span><span class="sxs-lookup"><span data-stu-id="d3325-975">container</span></span>  

## <a name="method-clear"></a><span data-ttu-id="d3325-976">メソッド clear</span><span class="sxs-lookup"><span data-stu-id="d3325-976">Method clear</span></span>

<span data-ttu-id="d3325-977">情報ログ バッファーから行を削除します。</span><span class="sxs-lookup"><span data-stu-id="d3325-977">Deletes lines from the Infolog buffer.</span></span>

```xpp
public void clear([int linesLeft])
```

### <a name="parameters---clear"></a><span data-ttu-id="d3325-978">パラメーター - clear</span><span class="sxs-lookup"><span data-stu-id="d3325-978">Parameters - clear</span></span>

<span data-ttu-id="d3325-979">linesLeft</span><span class="sxs-lookup"><span data-stu-id="d3325-979">linesLeft</span></span>  
<span data-ttu-id="d3325-980">バッファに残す行の数、省略可能です。</span><span class="sxs-lookup"><span data-stu-id="d3325-980">Number of lines to leave in the buffer; optional.</span></span>

### <a name="remarks---clear"></a><span data-ttu-id="d3325-981">備考 - clear</span><span class="sxs-lookup"><span data-stu-id="d3325-981">Remarks - clear</span></span>

<span data-ttu-id="d3325-982">他のプロセスが情報を Infolog に入れていない限り、既定値がゼロのメソッドで呼び出さないでください。</span><span class="sxs-lookup"><span data-stu-id="d3325-982">Do not call this with method with the default value of zero unless another process has not put information into the Infolog.</span></span>

### <a name="examples---clear"></a><span data-ttu-id="d3325-983">例 - clear</span><span class="sxs-lookup"><span data-stu-id="d3325-983">Examples - clear</span></span>

<span data-ttu-id="d3325-984">Infolog キャッシュを消去するには、このパターンを使用します。</span><span class="sxs-lookup"><span data-stu-id="d3325-984">Use this pattern to clear the Infolog cache:</span></span>

```xpp
int line = Global::infologLine();
try 
{ 
    // 
} 
catch 
{ 
    infolog.clear(line); 
}
```

## <a name="method-workspacewindowcreated"></a><span data-ttu-id="d3325-985">メソッド workspaceWindowCreated</span><span class="sxs-lookup"><span data-stu-id="d3325-985">Method workspaceWindowCreated</span></span>

<span data-ttu-id="d3325-986">新しいワークスペースが作成された時に実行します。</span><span class="sxs-lookup"><span data-stu-id="d3325-986">Executes when a new workspace is created.</span></span>

```xpp
public void workspaceWindowCreated(int hWnd)
```

### <a name="parameters---workspacewindowcreated"></a><span data-ttu-id="d3325-987">パラメーター - workspaceWindowCreated</span><span class="sxs-lookup"><span data-stu-id="d3325-987">Parameters - workspaceWindowCreated</span></span>

<span data-ttu-id="d3325-988">hWnd</span><span class="sxs-lookup"><span data-stu-id="d3325-988">hWnd</span></span>  
<span data-ttu-id="d3325-989">新しいワークスペースのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="d3325-989">The handle of the new workspace.</span></span>

### <a name="remarks---workspacewindowcreated"></a><span data-ttu-id="d3325-990">備考 - workspaceWindowCreated</span><span class="sxs-lookup"><span data-stu-id="d3325-990">Remarks - workspaceWindowCreated</span></span>

<span data-ttu-id="d3325-991">このメソッドは、新しいワークスペースが作成されるときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d3325-991">This method is called when a new workspace is created.</span></span> <span data-ttu-id="d3325-992">これにより、発生したときにアクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="d3325-992">It allows you to perform an action when this occurs.</span></span>

## <a name="method-setcurrentmodelid"></a><span data-ttu-id="d3325-993">メソッド setCurrentModelId</span><span class="sxs-lookup"><span data-stu-id="d3325-993">Method setCurrentModelId</span></span>

```xpp
public static void setCurrentModelId(int currentModelId)
```

### <a name="parameters---setcurrentmodelid"></a><span data-ttu-id="d3325-994">パラメーター - setCurrentModelId</span><span class="sxs-lookup"><span data-stu-id="d3325-994">Parameters - setCurrentModelId</span></span>

<span data-ttu-id="d3325-995">currentModelId</span><span class="sxs-lookup"><span data-stu-id="d3325-995">currentModelId</span></span>  

## <a name="method-activatemenubartask"></a><span data-ttu-id="d3325-996">メソッド activateMenubarTask</span><span class="sxs-lookup"><span data-stu-id="d3325-996">Method activateMenubarTask</span></span>

```xpp
public void activateMenubarTask(int command)
```

### <a name="parameters---activatemenubartask"></a><span data-ttu-id="d3325-997">パラメーター - activateMenubarTask</span><span class="sxs-lookup"><span data-stu-id="d3325-997">Parameters - activateMenubarTask</span></span>

<span data-ttu-id="d3325-998">command</span><span class="sxs-lookup"><span data-stu-id="d3325-998">command</span></span>  

## <a name="method-finalize"></a><span data-ttu-id="d3325-999">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="d3325-999">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-insertxreferences"></a><span data-ttu-id="d3325-1000">メソッド insertXReferences</span><span class="sxs-lookup"><span data-stu-id="d3325-1000">Method insertXReferences</span></span>

```xpp
public void insertXReferences()
```

## <a name="method-activatebutton"></a><span data-ttu-id="d3325-1001">メソッド activateButton</span><span class="sxs-lookup"><span data-stu-id="d3325-1001">Method activateButton</span></span>

```xpp
public void activateButton(int command)
```

### <a name="parameters---activatebutton"></a><span data-ttu-id="d3325-1002">パラメーター - activateButton</span><span class="sxs-lookup"><span data-stu-id="d3325-1002">Parameters - activateButton</span></span>

<span data-ttu-id="d3325-1003">command</span><span class="sxs-lookup"><span data-stu-id="d3325-1003">command</span></span>  

## <a name="method-activatewindow"></a><span data-ttu-id="d3325-1004">メソッド activateWindow</span><span class="sxs-lookup"><span data-stu-id="d3325-1004">Method activateWindow</span></span>

<span data-ttu-id="d3325-1005">フォームまたはウィンドウにフォーカスを設定します。</span><span class="sxs-lookup"><span data-stu-id="d3325-1005">Sets the focus on a form or Window.</span></span>

```xpp
public void activateWindow(int window)
```

### <a name="parameters---activatewindow"></a><span data-ttu-id="d3325-1006">パラメーター - activateWindow</span><span class="sxs-lookup"><span data-stu-id="d3325-1006">Parameters - activateWindow</span></span>

<span data-ttu-id="d3325-1007">window</span><span class="sxs-lookup"><span data-stu-id="d3325-1007">window</span></span>  
<span data-ttu-id="d3325-1008">詳しく説明するフォームまたはウィンドウのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="d3325-1008">The handle to the form or window that you want to bring into focus.</span></span>

## <a name="method-reportsendmail"></a><span data-ttu-id="d3325-1009">メソッド reportSendMail</span><span class="sxs-lookup"><span data-stu-id="d3325-1009">Method reportSendMail</span></span>

<span data-ttu-id="d3325-1010">レポートを電子メールで送信するための設定を生成します。</span><span class="sxs-lookup"><span data-stu-id="d3325-1010">Generates the settings for sending a report by email.</span></span>

```xpp
public void reportSendMail(PrintJobSettings settings)
```

### <a name="parameters---reportsendmail"></a><span data-ttu-id="d3325-1011">パラメーター - reportSendMail</span><span class="sxs-lookup"><span data-stu-id="d3325-1011">Parameters - reportSendMail</span></span>

<span data-ttu-id="d3325-1012">設定</span><span class="sxs-lookup"><span data-stu-id="d3325-1012">settings</span></span>  
<span data-ttu-id="d3325-1013">ユーザーの電子メール設定。</span><span class="sxs-lookup"><span data-stu-id="d3325-1013">The email settings for the user.</span></span>

