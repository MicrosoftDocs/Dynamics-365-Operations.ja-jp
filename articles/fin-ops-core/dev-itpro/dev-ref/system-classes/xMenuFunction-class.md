---
title: xMenuFunction クラス
description: このトピックでは、xMenuFunction クラスについて説明します。
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
ms.openlocfilehash: 0cdefef3ddf8fc9b6dbeeaeb3a2a362e8e304de2
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502758"
---
# <a name="class-xmenufunction"></a><span data-ttu-id="f0b36-103">クラス xMenuFunction</span><span class="sxs-lookup"><span data-stu-id="f0b36-103">Class xMenuFunction</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class xMenuFunction extends SecureNode
```

<span data-ttu-id="f0b36-104">xMenuFunction クラスは、フォーム、レポート、ジョブ、クラス、クエリにアクセスして実行するための簡単な方法を提供する、他のオブジェクトへのインターフェイスを表します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-104">The xMenuFunction class represents an interface to other objects, providing an easy way to access and run any Form, Report, Job, Class, and Query.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0b36-105">備考</span><span class="sxs-lookup"><span data-stu-id="f0b36-105">Remarks</span></span>

<span data-ttu-id="f0b36-106">xMenuFunction オブジェクトとそのメソッドおよびプロパティを使用して、アプリケーション オブジェクトを参照します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-106">You refer to an Application object using a xMenuFunction object and its methods and properties.</span></span> <span data-ttu-id="f0b36-107">たとえば、次のことを実行できます。</span><span class="sxs-lookup"><span data-stu-id="f0b36-107">For example, you can:</span></span>

-   <span data-ttu-id="f0b36-108">Run メソッドを使用してプロパティで参照されるオブジェクトを実行する</span><span class="sxs-lookup"><span data-stu-id="f0b36-108">Use the Run Method to run the object referenced in the property</span></span>
-   <span data-ttu-id="f0b36-109">xMenuFunction オブジェクトを作成し、そのオブジェクトが実行する (または参照する) オブジェクトへの参照を作成します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-109">Create a xMenuFunction object and make a reference to the object it runs (or references to).</span></span> <span data-ttu-id="f0b36-110">これにより、オブジェクトを実行する前に渡された引数を操作できます</span><span class="sxs-lookup"><span data-stu-id="f0b36-110">This enables you to manipulate the arguments passed to the object before running it</span></span>

<span data-ttu-id="f0b36-111">注記: このシステム クラスは、AOT 内の MenuItem ノードを表します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-111">Note: This system class represents MenuItem nodes in the AOT.</span></span> <span data-ttu-id="f0b36-112">このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="f0b36-112">This class enables you to create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="f0b36-113">ユーザーがこの API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-113">Make sure that the user has access to the development security key (SysDevelopment) before calling this API.</span></span>

## <a name="examples"></a><span data-ttu-id="f0b36-114">例</span><span class="sxs-lookup"><span data-stu-id="f0b36-114">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="f0b36-115">メソッド</span><span class="sxs-lookup"><span data-stu-id="f0b36-115">Methods</span></span>

| <span data-ttu-id="f0b36-116">方法</span><span class="sxs-lookup"><span data-stu-id="f0b36-116">Method</span></span>                                                                                                  | <span data-ttu-id="f0b36-117">説明</span><span class="sxs-lookup"><span data-stu-id="f0b36-117">Description</span></span>                                                                                                                               |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0b36-118">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-118">public str changedBy(\[str value\])</span></span>                                                                     | <span data-ttu-id="f0b36-119">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-119">Gets or sets the name of the user who last changed the application object.</span></span>                                                                |
| <span data-ttu-id="f0b36-120">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-120">public Date changedDate(\[Date value\])</span></span>                                                                 | <span data-ttu-id="f0b36-121">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-121">Gets or sets the date when an application object was last changed.</span></span>                                                                        |
| <span data-ttu-id="f0b36-122">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-122">public str changedTime(\[str value\])</span></span>                                                                   | <span data-ttu-id="f0b36-123">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-123">Gets or sets the time when an application object was last changed.</span></span>                                                                        |
| <span data-ttu-id="f0b36-124">public boolean checkAccessRights()</span><span class="sxs-lookup"><span data-stu-id="f0b36-124">public boolean checkAccessRights()</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="f0b36-125">public int copyCallerQuery(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-125">public int copyCallerQuery(\[int value\])</span></span>                                                               |                                                                                                                                           |
| <span data-ttu-id="f0b36-126">public int correctPermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-126">public int correctPermissions(\[int value\])</span></span>                                                            |                                                                                                                                           |
| <span data-ttu-id="f0b36-127">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-127">public str countryRegionCodes(\[str value\])</span></span>                                                            |                                                                                                                                           |
| <span data-ttu-id="f0b36-128">public ObjectRun create(\[xArgs args\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-128">public ObjectRun create(\[xArgs args\])</span></span>                                                                 | <span data-ttu-id="f0b36-129">アプリケーション オブジェクトへの参照を作成して返します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-129">Creates and returns a reference to an application object.</span></span>                                                           |
| <span data-ttu-id="f0b36-130">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-130">public str createdBy(\[str value\])</span></span>                                                                     | <span data-ttu-id="f0b36-131">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-131">Gets or sets the name of the user who created the application object.</span></span>                                                                     |
| <span data-ttu-id="f0b36-132">public int createPermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-132">public int createPermissions(\[int value\])</span></span>                                                             |                                                                                                                                           |
| <span data-ttu-id="f0b36-133">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-133">public Date creationDate(\[Date value\])</span></span>                                                                | <span data-ttu-id="f0b36-134">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-134">Gets or sets the date an application object was created.</span></span>                                                                                  |
| <span data-ttu-id="f0b36-135">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-135">public str creationTime(\[str value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="f0b36-136">public int deletePermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-136">public int deletePermissions(\[int value\])</span></span>                                                             |                                                                                                                                           |
| <span data-ttu-id="f0b36-137">public str disabledImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-137">public str disabledImage(\[str value\])</span></span>                                                                 | <span data-ttu-id="f0b36-138">コントロールの無効な画像を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-138">Gets or sets the disabled image of the button.</span></span>                                                                                            |
| <span data-ttu-id="f0b36-139">public int disabledImageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-139">public int disabledImageLocation(\[int value\])</span></span>                                                         |                                                                                                                                           |
| <span data-ttu-id="f0b36-140">public int disabledResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-140">public int disabledResource(\[int value\])</span></span>                                                              | <span data-ttu-id="f0b36-141">無効なボタン画像として使用する画像リソース ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-141">Gets or sets the resource ID of the image to use as the disabled button image.</span></span>                                                            |
| <span data-ttu-id="f0b36-142">public int enumParameter(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-142">public int enumParameter(\[int value\])</span></span>                                                                 | <span data-ttu-id="f0b36-143">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-143">Gets or sets the enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>                               |
| <span data-ttu-id="f0b36-144">public EnumId enumTypeParameter(\[EnumId value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-144">public EnumId enumTypeParameter(\[EnumId value\])</span></span>                                                       | <span data-ttu-id="f0b36-145">MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-145">Gets or sets the enumTypeParameter property for the MenuFunction class.</span></span>                                                                   |
| <span data-ttu-id="f0b36-146">public int formViewOption(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-146">public int formViewOption(\[int value\])</span></span>                                                                |                                                                                                                                           |
| <span data-ttu-id="f0b36-147">public Query getRootQuery()</span><span class="sxs-lookup"><span data-stu-id="f0b36-147">public Query getRootQuery()</span></span>                                                                             |                                                                                                                                           |
| <span data-ttu-id="f0b36-148">public boolean hasRunPermissions(\[xArgs args\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-148">public boolean hasRunPermissions(\[xArgs args\])</span></span>                                                        | <span data-ttu-id="f0b36-149">xMenuFunction オブジェクトに実行権限があり、run() が正常に呼び出されるかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="f0b36-149">Checks if the xMenuFunction object has execute permissions and run() may be called successfully.</span></span>                                          |
| <span data-ttu-id="f0b36-150">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-150">public str helpText(\[str value\])</span></span>                                                                      | <span data-ttu-id="f0b36-151">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-151">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                  |
| <span data-ttu-id="f0b36-152">public int imageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-152">public int imageLocation(\[int value\])</span></span>                                                                 |                                                                                                                                           |
| <span data-ttu-id="f0b36-153">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-153">public str label(\[str value\])</span></span>                                                                         | <span data-ttu-id="f0b36-154">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-154">Gets or sets the label for a control.</span></span>                                                                                                     |
| <span data-ttu-id="f0b36-155">public str linkedPermissionObject(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-155">public str linkedPermissionObject(\[str value\])</span></span>                                                        |                                                                                                                                           |
| <span data-ttu-id="f0b36-156">public str linkedPermissionObjectChild(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-156">public str linkedPermissionObjectChild(\[str value\])</span></span>                                                   |                                                                                                                                           |
| <span data-ttu-id="f0b36-157">public int linkedPermissionType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-157">public int linkedPermissionType(\[int value\])</span></span>                                                          |                                                                                                                                           |
| <span data-ttu-id="f0b36-158">public int maintainUserLicense(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-158">public int maintainUserLicense(\[int value\])</span></span>                                                           |                                                                                                                                           |
| <span data-ttu-id="f0b36-159">public boolean multiSelect(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-159">public boolean multiSelect(\[boolean value\])</span></span>                                                           |                                                                                                                                           |
| <span data-ttu-id="f0b36-160">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-160">public str name(\[str value\])</span></span>                                                                          | <span data-ttu-id="f0b36-161">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-161">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="f0b36-162">public int needsRecord(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-162">public int needsRecord(\[int value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="f0b36-163">public str normalImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-163">public str normalImage(\[str value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="f0b36-164">public int normalResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-164">public int normalResource(\[int value\])</span></span>                                                                |                                                                                                                                           |
| <span data-ttu-id="f0b36-165">public str object(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-165">public str object(\[str value\])</span></span>                                                                        | <span data-ttu-id="f0b36-166">MenuFunction クラスにより実行されるオブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-166">Gets or sets the object that is run by the MenuFunction class.</span></span>                                                                            |
| <span data-ttu-id="f0b36-167">public int objectType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-167">public int objectType(\[int value\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="f0b36-168">public int openMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-168">public int openMode(\[int value\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="f0b36-169">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-169">public Guid origin(\[Guid value\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="f0b36-170">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-170">public str parameters(\[str value\])</span></span>                                                                    | <span data-ttu-id="f0b36-171">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-171">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>                                    |
| <span data-ttu-id="f0b36-172">public str query(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-172">public str query(\[str value\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="f0b36-173">public int readPermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-173">public int readPermissions(\[int value\])</span></span>                                                               |                                                                                                                                           |
| <span data-ttu-id="f0b36-174">public str reportDesign(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-174">public str reportDesign(\[str value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="f0b36-175">public int runOn(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-175">public int runOn(\[int value\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="f0b36-176">public MenuItemType type()</span><span class="sxs-lookup"><span data-stu-id="f0b36-176">public MenuItemType type()</span></span>                                                                              |                                                                                                                                           |
| <span data-ttu-id="f0b36-177">public int updatePermissions(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-177">public int updatePermissions(\[int value\])</span></span>                                                             |                                                                                                                                           |
| <span data-ttu-id="f0b36-178">public int viewUserLicense(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-178">public int viewUserLicense(\[int value\])</span></span>                                                               |                                                                                                                                           |
| <span data-ttu-id="f0b36-179">public str web(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-179">public str web(\[str value\])</span></span>                                                                           |                                                                                                                                           |
| <span data-ttu-id="f0b36-180">public int webAccess(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-180">public int webAccess(\[int value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="f0b36-181">public str webMenuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-181">public str webMenuItemName(\[str value\])</span></span>                                                               |                                                                                                                                           |
| <span data-ttu-id="f0b36-182">public str webPage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-182">public str webPage(\[str value\])</span></span>                                                                       |                                                                                                                                           |
| <span data-ttu-id="f0b36-183">public boolean webSecureTransaction(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-183">public boolean webSecureTransaction(\[boolean value\])</span></span>                                                  |                                                                                                                                           |
| <span data-ttu-id="f0b36-184">public void run(\[xArgs args\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-184">public void run(\[xArgs args\])</span></span>                                                                         | <span data-ttu-id="f0b36-185">xMenuFunction オブジェクトを実行します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-185">Runs the xMenuFunction object.</span></span>                                                                                                            |
| <span data-ttu-id="f0b36-186">::public static void runCalled(str Name, MenuItemType type, \[boolean setContextMenu\], \[xArgs args\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-186">::public static void runCalled(str Name, MenuItemType type, \[boolean setContextMenu\], \[xArgs args\])</span></span> |                                                                                                                                           |
| <span data-ttu-id="f0b36-187">::public static void runClient(str Name, MenuItemType type, \[boolean setContextMenu\], \[xArgs args\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-187">::public static void runClient(str Name, MenuItemType type, \[boolean setContextMenu\], \[xArgs args\])</span></span> |                                                                                                                                           |
| <span data-ttu-id="f0b36-188">::public static void runServer(str Name, MenuItemType type, \[boolean setContextMenu\], \[xArgs args\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-188">::public static void runServer(str Name, MenuItemType type, \[boolean setContextMenu\], \[xArgs args\])</span></span> |                                                                                                                                           |
| <span data-ttu-id="f0b36-189">public void new(str Name, MenuItemType type)</span><span class="sxs-lookup"><span data-stu-id="f0b36-189">public void new(str Name, MenuItemType type)</span></span>                                                            | <span data-ttu-id="f0b36-190">xMenuFunction の名前と MenuItemType を xMenuFunction コンストラクターに渡して、新しい xMenuFunction オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-190">Creates a new xMenuFunction object by passing xMenuFunction's name and MenuItemType to the xMenuFunction constructor.</span></span>                     |
| <span data-ttu-id="f0b36-191">public void AOTrun(\[xArgs args\])</span><span class="sxs-lookup"><span data-stu-id="f0b36-191">public void AOTrun(\[xArgs args\])</span></span>                                                                      | <span data-ttu-id="f0b36-192">アプリケーション オブジェクト ツリー (AOT) でこのノードとそのサブツリーをコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="f0b36-192">Compiles this node and its subtree in the Application Object Tree (AOT).</span></span>                                                                  |

## <a name="method-changedby"></a><span data-ttu-id="f0b36-193">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="f0b36-193">Method changedBy</span></span>

<span data-ttu-id="f0b36-194">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-194">Gets or sets the name of the user who last changed the application object.</span></span>

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a><span data-ttu-id="f0b36-195">パラメーター - changedBy</span><span class="sxs-lookup"><span data-stu-id="f0b36-195">Parameters - changedBy</span></span>

<span data-ttu-id="f0b36-196">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-196">value</span></span>  
<span data-ttu-id="f0b36-197">設定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f0b36-197">The value to set; optional.</span></span>

### <a name="return-value---changedby"></a><span data-ttu-id="f0b36-198">戻り値 - changedBy</span><span class="sxs-lookup"><span data-stu-id="f0b36-198">Return Value - changedBy</span></span>

<span data-ttu-id="f0b36-199">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="f0b36-199">The name of the user.</span></span>

## <a name="method-changeddate"></a><span data-ttu-id="f0b36-200">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="f0b36-200">Method changedDate</span></span>

<span data-ttu-id="f0b36-201">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-201">Gets or sets the date when an application object was last changed.</span></span>

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a><span data-ttu-id="f0b36-202">パラメーター - changedDate</span><span class="sxs-lookup"><span data-stu-id="f0b36-202">Parameters - changedDate</span></span>

<span data-ttu-id="f0b36-203">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-203">value</span></span>  
<span data-ttu-id="f0b36-204">設定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f0b36-204">The value to set; optional.</span></span>

### <a name="return-value---changeddate"></a><span data-ttu-id="f0b36-205">戻り値 - changedDate</span><span class="sxs-lookup"><span data-stu-id="f0b36-205">Return Value - changedDate</span></span>

<span data-ttu-id="f0b36-206">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="f0b36-206">The date when an application object was last changed.</span></span>

## <a name="method-changedtime"></a><span data-ttu-id="f0b36-207">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="f0b36-207">Method changedTime</span></span>

<span data-ttu-id="f0b36-208">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-208">Gets or sets the time when an application object was last changed.</span></span>

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a><span data-ttu-id="f0b36-209">パラメーター - changedTime</span><span class="sxs-lookup"><span data-stu-id="f0b36-209">Parameters - changedTime</span></span>

<span data-ttu-id="f0b36-210">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-210">value</span></span>  
<span data-ttu-id="f0b36-211">設定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f0b36-211">The value to set; optional.</span></span>

### <a name="return-value---changedtime"></a><span data-ttu-id="f0b36-212">戻り値 - changedTime</span><span class="sxs-lookup"><span data-stu-id="f0b36-212">Return Value - changedTime</span></span>

<span data-ttu-id="f0b36-213">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="f0b36-213">The time when an application object was last changed.</span></span>

## <a name="method-checkaccessrights"></a><span data-ttu-id="f0b36-214">メソッド checkAccessRights</span><span class="sxs-lookup"><span data-stu-id="f0b36-214">Method checkAccessRights</span></span>

```xpp
public boolean checkAccessRights()
```

### <a name="return-value---checkaccessrights"></a><span data-ttu-id="f0b36-215">戻り値 - checkAccessRights</span><span class="sxs-lookup"><span data-stu-id="f0b36-215">Return Value - checkAccessRights</span></span>

## <a name="method-copycallerquery"></a><span data-ttu-id="f0b36-216">メソッド copyCallerQuery</span><span class="sxs-lookup"><span data-stu-id="f0b36-216">Method copyCallerQuery</span></span>

```xpp
public int copyCallerQuery([int value])
```

### <a name="parameters---copycallerquery"></a><span data-ttu-id="f0b36-217">パラメーター - copyCallerQuery</span><span class="sxs-lookup"><span data-stu-id="f0b36-217">Parameters - copyCallerQuery</span></span>

<span data-ttu-id="f0b36-218">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-218">value</span></span>  

### <a name="return-value---copycallerquery"></a><span data-ttu-id="f0b36-219">戻り値 - copyCallerQuery</span><span class="sxs-lookup"><span data-stu-id="f0b36-219">Return Value - copyCallerQuery</span></span>

## <a name="method-correctpermissions"></a><span data-ttu-id="f0b36-220">メソッド correctPermissions</span><span class="sxs-lookup"><span data-stu-id="f0b36-220">Method correctPermissions</span></span>

```xpp
public int correctPermissions([int value])
```

### <a name="parameters---correctpermissions"></a><span data-ttu-id="f0b36-221">パラメーター - correctPermissions</span><span class="sxs-lookup"><span data-stu-id="f0b36-221">Parameters - correctPermissions</span></span>

<span data-ttu-id="f0b36-222">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-222">value</span></span>  

### <a name="return-value---correctpermissions"></a><span data-ttu-id="f0b36-223">戻り値 - correctPermissions</span><span class="sxs-lookup"><span data-stu-id="f0b36-223">Return Value - correctPermissions</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="f0b36-224">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="f0b36-224">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="f0b36-225">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="f0b36-225">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="f0b36-226">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-226">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="f0b36-227">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="f0b36-227">Return Value - countryRegionCodes</span></span>

## <a name="method-create"></a><span data-ttu-id="f0b36-228">メソッド create</span><span class="sxs-lookup"><span data-stu-id="f0b36-228">Method create</span></span>

<span data-ttu-id="f0b36-229">アプリケーション オブジェクトへの参照を作成して返します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-229">Creates and returns a reference to an application object.</span></span>

```xpp
public ObjectRun create([xArgs args])
```

### <a name="parameters---create"></a><span data-ttu-id="f0b36-230">パラメーター - create</span><span class="sxs-lookup"><span data-stu-id="f0b36-230">Parameters - create</span></span>

<span data-ttu-id="f0b36-231">args</span><span class="sxs-lookup"><span data-stu-id="f0b36-231">args</span></span>  
<span data-ttu-id="f0b36-232">xArgs クラス オブジェクト。オプション。</span><span class="sxs-lookup"><span data-stu-id="f0b36-232">An xArgs class object; optional.</span></span>

### <a name="return-value---create"></a><span data-ttu-id="f0b36-233">戻り値 - create</span><span class="sxs-lookup"><span data-stu-id="f0b36-233">Return Value - create</span></span>

<span data-ttu-id="f0b36-234">アプリケーション オブジェクトへの参照。</span><span class="sxs-lookup"><span data-stu-id="f0b36-234">A reference to an application object.</span></span>

### <a name="remarks---create"></a><span data-ttu-id="f0b36-235">備考 - create</span><span class="sxs-lookup"><span data-stu-id="f0b36-235">Remarks - create</span></span>

<span data-ttu-id="f0b36-236">このメソッドは、アプリケーション オブジェクトの作成に使用されます。</span><span class="sxs-lookup"><span data-stu-id="f0b36-236">This method is used to create an application object.</span></span> <span data-ttu-id="f0b36-237">返されるオブジェクトは、オブジェクト変数に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="f0b36-237">The object that is returned is assigned to an object variable.</span></span> <span data-ttu-id="f0b36-238">init 関数は create 関数によって呼び出されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f0b36-238">Note that the init function is invoked by the create function.</span></span> <span data-ttu-id="f0b36-239">したがって、それを呼び出すべきではありません。</span><span class="sxs-lookup"><span data-stu-id="f0b36-239">Therefore you should not invoke it.</span></span>

## <a name="method-createdby"></a><span data-ttu-id="f0b36-240">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="f0b36-240">Method createdBy</span></span>

<span data-ttu-id="f0b36-241">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-241">Gets or sets the name of the user who created the application object.</span></span>

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a><span data-ttu-id="f0b36-242">パラメーター - createdBy</span><span class="sxs-lookup"><span data-stu-id="f0b36-242">Parameters - createdBy</span></span>

<span data-ttu-id="f0b36-243">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-243">value</span></span>  

### <a name="return-value---createdby"></a><span data-ttu-id="f0b36-244">戻り値 - createdBy</span><span class="sxs-lookup"><span data-stu-id="f0b36-244">Return Value - createdBy</span></span>

<span data-ttu-id="f0b36-245">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="f0b36-245">The name of the user.</span></span>

## <a name="method-createpermissions"></a><span data-ttu-id="f0b36-246">メソッド createPermissions</span><span class="sxs-lookup"><span data-stu-id="f0b36-246">Method createPermissions</span></span>

```xpp
public int createPermissions([int value])
```

### <a name="parameters---createpermissions"></a><span data-ttu-id="f0b36-247">パラメーター - createPermissions</span><span class="sxs-lookup"><span data-stu-id="f0b36-247">Parameters - createPermissions</span></span>

<span data-ttu-id="f0b36-248">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-248">value</span></span>  

### <a name="return-value---createpermissions"></a><span data-ttu-id="f0b36-249">戻り値 - createPermissions</span><span class="sxs-lookup"><span data-stu-id="f0b36-249">Return Value - createPermissions</span></span>

## <a name="method-creationdate"></a><span data-ttu-id="f0b36-250">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="f0b36-250">Method creationDate</span></span>

<span data-ttu-id="f0b36-251">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-251">Gets or sets the date an application object was created.</span></span>

```xpp
public Date creationDate([Date value])
```

### <a name="parameters---creationdate"></a><span data-ttu-id="f0b36-252">パラメーター - creationDate</span><span class="sxs-lookup"><span data-stu-id="f0b36-252">Parameters - creationDate</span></span>

<span data-ttu-id="f0b36-253">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-253">value</span></span>  

### <a name="return-value---creationdate"></a><span data-ttu-id="f0b36-254">戻り値 - creationDate</span><span class="sxs-lookup"><span data-stu-id="f0b36-254">Return Value - creationDate</span></span>

<span data-ttu-id="f0b36-255">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="f0b36-255">The date an application object was created.</span></span>

## <a name="method-creationtime"></a><span data-ttu-id="f0b36-256">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="f0b36-256">Method creationTime</span></span>

```xpp
public str creationTime([str value])
```

### <a name="parameters---creationtime"></a><span data-ttu-id="f0b36-257">パラメーター - creationTime</span><span class="sxs-lookup"><span data-stu-id="f0b36-257">Parameters - creationTime</span></span>

<span data-ttu-id="f0b36-258">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-258">value</span></span>  

### <a name="return-value---creationtime"></a><span data-ttu-id="f0b36-259">戻り値 - creationTime</span><span class="sxs-lookup"><span data-stu-id="f0b36-259">Return Value - creationTime</span></span>

## <a name="method-deletepermissions"></a><span data-ttu-id="f0b36-260">メソッド deletePermissions</span><span class="sxs-lookup"><span data-stu-id="f0b36-260">Method deletePermissions</span></span>

```xpp
public int deletePermissions([int value])
```

### <a name="parameters---deletepermissions"></a><span data-ttu-id="f0b36-261">パラメーター - deletePermissions</span><span class="sxs-lookup"><span data-stu-id="f0b36-261">Parameters - deletePermissions</span></span>

<span data-ttu-id="f0b36-262">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-262">value</span></span>  

### <a name="return-value---deletepermissions"></a><span data-ttu-id="f0b36-263">戻り値 - deletePermissions</span><span class="sxs-lookup"><span data-stu-id="f0b36-263">Return Value - deletePermissions</span></span>

## <a name="method-disabledimage"></a><span data-ttu-id="f0b36-264">メソッド disabledImage</span><span class="sxs-lookup"><span data-stu-id="f0b36-264">Method disabledImage</span></span>

<span data-ttu-id="f0b36-265">コントロールの無効な画像を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-265">Gets or sets the disabled image of the button.</span></span>

```xpp
public str disabledImage([str value])
```

### <a name="parameters---disabledimage"></a><span data-ttu-id="f0b36-266">パラメーター - disabledImage</span><span class="sxs-lookup"><span data-stu-id="f0b36-266">Parameters - disabledImage</span></span>

<span data-ttu-id="f0b36-267">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-267">value</span></span>  

### <a name="return-value---disabledimage"></a><span data-ttu-id="f0b36-268">戻り値 - disabledImage</span><span class="sxs-lookup"><span data-stu-id="f0b36-268">Return Value - disabledImage</span></span>

<span data-ttu-id="f0b36-269">画像ファイルのフル ネーム。システムは GDI でサポートされているすべての画像形式をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="f0b36-269">The full name of an image file; the system supports all of the GDI-supported image formats.</span></span>

### <a name="remarks---disabledimage"></a><span data-ttu-id="f0b36-270">備考 - disabledImage</span><span class="sxs-lookup"><span data-stu-id="f0b36-270">Remarks - disabledImage</span></span>

<span data-ttu-id="f0b36-271">このプロパティは、disabledResource プロパティ値に優先します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-271">This property has precedence over the disabledResource property value.</span></span> <span data-ttu-id="f0b36-272">これらのプロパティの両方が設定されている場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="f0b36-272">It is used if both of these properties are set.</span></span>

## <a name="method-disabledimagelocation"></a><span data-ttu-id="f0b36-273">メソッド disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="f0b36-273">Method disabledImageLocation</span></span>

```xpp
public int disabledImageLocation([int value])
```

### <a name="parameters---disabledimagelocation"></a><span data-ttu-id="f0b36-274">パラメーター - disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="f0b36-274">Parameters - disabledImageLocation</span></span>

<span data-ttu-id="f0b36-275">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-275">value</span></span>  

### <a name="return-value---disabledimagelocation"></a><span data-ttu-id="f0b36-276">戻り値 - disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="f0b36-276">Return Value - disabledImageLocation</span></span>

## <a name="method-disabledresource"></a><span data-ttu-id="f0b36-277">メソッド disabledResource</span><span class="sxs-lookup"><span data-stu-id="f0b36-277">Method disabledResource</span></span>

<span data-ttu-id="f0b36-278">無効なボタン画像として使用する画像リソース ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-278">Gets or sets the resource ID of the image to use as the disabled button image.</span></span>

```xpp
public int disabledResource([int value])
```

### <a name="parameters---disabledresource"></a><span data-ttu-id="f0b36-279">パラメーター - disabledResource</span><span class="sxs-lookup"><span data-stu-id="f0b36-279">Parameters - disabledResource</span></span>

<span data-ttu-id="f0b36-280">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-280">value</span></span>  

### <a name="return-value---disabledresource"></a><span data-ttu-id="f0b36-281">戻り値 - disabledResource</span><span class="sxs-lookup"><span data-stu-id="f0b36-281">Return Value - disabledResource</span></span>

<span data-ttu-id="f0b36-282">無効なボタン画像として使用する画像リソース ID。</span><span class="sxs-lookup"><span data-stu-id="f0b36-282">The resource ID of the image to use as the disabled button image.</span></span> <span data-ttu-id="f0b36-283">アイコンとビットマップ イメージの両方がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="f0b36-283">Both icon and bitmap images are supported.</span></span>

## <a name="method-enumparameter"></a><span data-ttu-id="f0b36-284">メソッド enumParameter</span><span class="sxs-lookup"><span data-stu-id="f0b36-284">Method enumParameter</span></span>

<span data-ttu-id="f0b36-285">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-285">Gets or sets the enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>

```xpp
public int enumParameter([int value])
```

### <a name="parameters---enumparameter"></a><span data-ttu-id="f0b36-286">パラメーター - enumParameter</span><span class="sxs-lookup"><span data-stu-id="f0b36-286">Parameters - enumParameter</span></span>

<span data-ttu-id="f0b36-287">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-287">value</span></span>  

### <a name="return-value---enumparameter"></a><span data-ttu-id="f0b36-288">戻り値 - enumParameter</span><span class="sxs-lookup"><span data-stu-id="f0b36-288">Return Value - enumParameter</span></span>

<span data-ttu-id="f0b36-289">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティ。</span><span class="sxs-lookup"><span data-stu-id="f0b36-289">The enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>

## <a name="method-enumtypeparameter"></a><span data-ttu-id="f0b36-290">メソッド enumTypeParameter</span><span class="sxs-lookup"><span data-stu-id="f0b36-290">Method enumTypeParameter</span></span>

<span data-ttu-id="f0b36-291">MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-291">Gets or sets the enumTypeParameter property for the MenuFunction class.</span></span>

```xpp
public EnumId enumTypeParameter([EnumId value])
```

### <a name="parameters---enumtypeparameter"></a><span data-ttu-id="f0b36-292">パラメーター - enumTypeParameter</span><span class="sxs-lookup"><span data-stu-id="f0b36-292">Parameters - enumTypeParameter</span></span>

<span data-ttu-id="f0b36-293">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-293">value</span></span>  

### <a name="return-value---enumtypeparameter"></a><span data-ttu-id="f0b36-294">戻り値 - enumTypeParameter</span><span class="sxs-lookup"><span data-stu-id="f0b36-294">Return Value - enumTypeParameter</span></span>

<span data-ttu-id="f0b36-295">MenuFunction クラスの enumTypeParameter プロパティ。</span><span class="sxs-lookup"><span data-stu-id="f0b36-295">The enumTypeParameter property for the MenuFunction class.</span></span>

## <a name="method-formviewoption"></a><span data-ttu-id="f0b36-296">メソッド formViewOption</span><span class="sxs-lookup"><span data-stu-id="f0b36-296">Method formViewOption</span></span>

```xpp
public int formViewOption([int value])
```

### <a name="parameters---formviewoption"></a><span data-ttu-id="f0b36-297">パラメーター - formViewOption</span><span class="sxs-lookup"><span data-stu-id="f0b36-297">Parameters - formViewOption</span></span>

<span data-ttu-id="f0b36-298">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-298">value</span></span>  

### <a name="return-value---formviewoption"></a><span data-ttu-id="f0b36-299">戻り値 - formViewOption</span><span class="sxs-lookup"><span data-stu-id="f0b36-299">Return Value - formViewOption</span></span>

## <a name="method-getrootquery"></a><span data-ttu-id="f0b36-300">メソッド getRootQuery</span><span class="sxs-lookup"><span data-stu-id="f0b36-300">Method getRootQuery</span></span>

```xpp
public Query getRootQuery()
```

### <a name="return-value---getrootquery"></a><span data-ttu-id="f0b36-301">戻り値 - getRootQuery</span><span class="sxs-lookup"><span data-stu-id="f0b36-301">Return Value - getRootQuery</span></span>

## <a name="method-hasrunpermissions"></a><span data-ttu-id="f0b36-302">メソッド hasRunPermissions</span><span class="sxs-lookup"><span data-stu-id="f0b36-302">Method hasRunPermissions</span></span>

<span data-ttu-id="f0b36-303">xMenuFunction オブジェクトに実行権限があり、run() が正常に呼び出されるかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="f0b36-303">Checks if the xMenuFunction object has execute permissions and run() may be called successfully.</span></span>

```xpp
public boolean hasRunPermissions([xArgs args])
```

### <a name="parameters---hasrunpermissions"></a><span data-ttu-id="f0b36-304">パラメーター - hasRunPermissions</span><span class="sxs-lookup"><span data-stu-id="f0b36-304">Parameters - hasRunPermissions</span></span>

<span data-ttu-id="f0b36-305">args</span><span class="sxs-lookup"><span data-stu-id="f0b36-305">args</span></span>  
<span data-ttu-id="f0b36-306">run() メソッドに渡される xArgs クラス オブジェクト。オプション。</span><span class="sxs-lookup"><span data-stu-id="f0b36-306">An xArgs class object as would be passed to the run() method; optional.</span></span>

### <a name="return-value---hasrunpermissions"></a><span data-ttu-id="f0b36-307">戻り値 - hasRunPermissions</span><span class="sxs-lookup"><span data-stu-id="f0b36-307">Return Value - hasRunPermissions</span></span>

<span data-ttu-id="f0b36-308">run() を正常に呼び出すために必要なアクセス許可が存在する場合は true。</span><span class="sxs-lookup"><span data-stu-id="f0b36-308">true if necessary permissions exist to successfully call run().</span></span>

### <a name="remarks---hasrunpermissions"></a><span data-ttu-id="f0b36-309">備考 - hasRunPermissions</span><span class="sxs-lookup"><span data-stu-id="f0b36-309">Remarks - hasRunPermissions</span></span>

<span data-ttu-id="f0b36-310">この関数は、アクセス許可が失敗した場合にスローされることがあります。</span><span class="sxs-lookup"><span data-stu-id="f0b36-310">This function may throw in case of permissions failure.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="f0b36-311">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="f0b36-311">Method helpText</span></span>

<span data-ttu-id="f0b36-312">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-312">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="f0b36-313">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="f0b36-313">Parameters - helpText</span></span>

<span data-ttu-id="f0b36-314">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-314">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="f0b36-315">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="f0b36-315">Return Value - helpText</span></span>

<span data-ttu-id="f0b36-316">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="f0b36-316">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="f0b36-317">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="f0b36-317">Remarks - helpText</span></span>

<span data-ttu-id="f0b36-318">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-318">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="f0b36-319">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="f0b36-319">The help text must not exceed 250 characters.</span></span>

## <a name="method-imagelocation"></a><span data-ttu-id="f0b36-320">メソッド imageLocation</span><span class="sxs-lookup"><span data-stu-id="f0b36-320">Method imageLocation</span></span>

```xpp
public int imageLocation([int value])
```

### <a name="parameters---imagelocation"></a><span data-ttu-id="f0b36-321">パラメーター - imageLocation</span><span class="sxs-lookup"><span data-stu-id="f0b36-321">Parameters - imageLocation</span></span>

<span data-ttu-id="f0b36-322">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-322">value</span></span>  

### <a name="return-value---imagelocation"></a><span data-ttu-id="f0b36-323">戻り値 - imageLocation</span><span class="sxs-lookup"><span data-stu-id="f0b36-323">Return Value - imageLocation</span></span>

## <a name="method-label"></a><span data-ttu-id="f0b36-324">メソッド label</span><span class="sxs-lookup"><span data-stu-id="f0b36-324">Method label</span></span>

<span data-ttu-id="f0b36-325">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-325">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="f0b36-326">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="f0b36-326">Parameters - label</span></span>

<span data-ttu-id="f0b36-327">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-327">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="f0b36-328">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="f0b36-328">Return Value - label</span></span>

<span data-ttu-id="f0b36-329">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="f0b36-329">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="f0b36-330">備考 - label</span><span class="sxs-lookup"><span data-stu-id="f0b36-330">Remarks - label</span></span>

<span data-ttu-id="f0b36-331">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-331">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="f0b36-332">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="f0b36-332">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-linkedpermissionobject"></a><span data-ttu-id="f0b36-333">メソッド linkedPermissionObject</span><span class="sxs-lookup"><span data-stu-id="f0b36-333">Method linkedPermissionObject</span></span>

```xpp
public str linkedPermissionObject([str value])
```

### <a name="parameters---linkedpermissionobject"></a><span data-ttu-id="f0b36-334">パラメーター - linkedPermissionObject</span><span class="sxs-lookup"><span data-stu-id="f0b36-334">Parameters - linkedPermissionObject</span></span>

<span data-ttu-id="f0b36-335">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-335">value</span></span>  

### <a name="return-value---linkedpermissionobject"></a><span data-ttu-id="f0b36-336">戻り値 - linkedPermissionObject</span><span class="sxs-lookup"><span data-stu-id="f0b36-336">Return Value - linkedPermissionObject</span></span>

## <a name="method-linkedpermissionobjectchild"></a><span data-ttu-id="f0b36-337">メソッド linkedPermissionObjectChild</span><span class="sxs-lookup"><span data-stu-id="f0b36-337">Method linkedPermissionObjectChild</span></span>

```xpp
public str linkedPermissionObjectChild([str value])
```

### <a name="parameters---linkedpermissionobjectchild"></a><span data-ttu-id="f0b36-338">パラメーター - linkedPermissionObjectChild</span><span class="sxs-lookup"><span data-stu-id="f0b36-338">Parameters - linkedPermissionObjectChild</span></span>

<span data-ttu-id="f0b36-339">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-339">value</span></span>  

### <a name="return-value---linkedpermissionobjectchild"></a><span data-ttu-id="f0b36-340">戻り値 - linkedPermissionObjectChild</span><span class="sxs-lookup"><span data-stu-id="f0b36-340">Return Value - linkedPermissionObjectChild</span></span>

## <a name="method-linkedpermissiontype"></a><span data-ttu-id="f0b36-341">メソッド linkedPermissionType</span><span class="sxs-lookup"><span data-stu-id="f0b36-341">Method linkedPermissionType</span></span>

```xpp
public int linkedPermissionType([int value])
```

### <a name="parameters---linkedpermissiontype"></a><span data-ttu-id="f0b36-342">パラメーター - linkedPermissionType</span><span class="sxs-lookup"><span data-stu-id="f0b36-342">Parameters - linkedPermissionType</span></span>

<span data-ttu-id="f0b36-343">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-343">value</span></span>  

### <a name="return-value---linkedpermissiontype"></a><span data-ttu-id="f0b36-344">戻り値 - linkedPermissionType</span><span class="sxs-lookup"><span data-stu-id="f0b36-344">Return Value - linkedPermissionType</span></span>

## <a name="method-maintainuserlicense"></a><span data-ttu-id="f0b36-345">メソッド maintainUserLicense</span><span class="sxs-lookup"><span data-stu-id="f0b36-345">Method maintainUserLicense</span></span>

```xpp
public int maintainUserLicense([int value])
```

### <a name="parameters---maintainuserlicense"></a><span data-ttu-id="f0b36-346">パラメーター - maintainUserLicense</span><span class="sxs-lookup"><span data-stu-id="f0b36-346">Parameters - maintainUserLicense</span></span>

<span data-ttu-id="f0b36-347">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-347">value</span></span>  

### <a name="return-value---maintainuserlicense"></a><span data-ttu-id="f0b36-348">戻り値 - maintainUserLicense</span><span class="sxs-lookup"><span data-stu-id="f0b36-348">Return Value - maintainUserLicense</span></span>

## <a name="method-multiselect"></a><span data-ttu-id="f0b36-349">メソッド multiSelect</span><span class="sxs-lookup"><span data-stu-id="f0b36-349">Method multiSelect</span></span>

```xpp
public boolean multiSelect([boolean value])
```

### <a name="parameters---multiselect"></a><span data-ttu-id="f0b36-350">パラメーター - multiSelect</span><span class="sxs-lookup"><span data-stu-id="f0b36-350">Parameters - multiSelect</span></span>

<span data-ttu-id="f0b36-351">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-351">value</span></span>  

### <a name="return-value---multiselect"></a><span data-ttu-id="f0b36-352">戻り値 - multiSelect</span><span class="sxs-lookup"><span data-stu-id="f0b36-352">Return Value - multiSelect</span></span>

## <a name="method-name"></a><span data-ttu-id="f0b36-353">メソッド名</span><span class="sxs-lookup"><span data-stu-id="f0b36-353">Method name</span></span>

<span data-ttu-id="f0b36-354">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-354">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="f0b36-355">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="f0b36-355">Parameters - name</span></span>

<span data-ttu-id="f0b36-356">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-356">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="f0b36-357">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="f0b36-357">Return Value - name</span></span>

<span data-ttu-id="f0b36-358">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="f0b36-358">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="f0b36-359">備考 - name</span><span class="sxs-lookup"><span data-stu-id="f0b36-359">Remarks - name</span></span>

<span data-ttu-id="f0b36-360">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="f0b36-360">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="f0b36-361">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="f0b36-361">Begins with a letter.</span></span>
-   <span data-ttu-id="f0b36-362">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="f0b36-362">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="f0b36-363">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="f0b36-363">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="f0b36-364">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="f0b36-364">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="f0b36-365">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="f0b36-365">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-needsrecord"></a><span data-ttu-id="f0b36-366">メソッド needsRecord</span><span class="sxs-lookup"><span data-stu-id="f0b36-366">Method needsRecord</span></span>

```xpp
public int needsRecord([int value])
```

### <a name="parameters---needsrecord"></a><span data-ttu-id="f0b36-367">パラメーター - needsRecord</span><span class="sxs-lookup"><span data-stu-id="f0b36-367">Parameters - needsRecord</span></span>

<span data-ttu-id="f0b36-368">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-368">value</span></span>  

### <a name="return-value---needsrecord"></a><span data-ttu-id="f0b36-369">戻り値 - needsRecord</span><span class="sxs-lookup"><span data-stu-id="f0b36-369">Return Value - needsRecord</span></span>

## <a name="method-normalimage"></a><span data-ttu-id="f0b36-370">メソッド normalImage</span><span class="sxs-lookup"><span data-stu-id="f0b36-370">Method normalImage</span></span>

```xpp
public str normalImage([str value])
```

### <a name="parameters---normalimage"></a><span data-ttu-id="f0b36-371">パラメーター - normalImage</span><span class="sxs-lookup"><span data-stu-id="f0b36-371">Parameters - normalImage</span></span>

<span data-ttu-id="f0b36-372">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-372">value</span></span>  

### <a name="return-value---normalimage"></a><span data-ttu-id="f0b36-373">戻り値 - normalImage</span><span class="sxs-lookup"><span data-stu-id="f0b36-373">Return Value - normalImage</span></span>

## <a name="method-normalresource"></a><span data-ttu-id="f0b36-374">メソッド normalResource</span><span class="sxs-lookup"><span data-stu-id="f0b36-374">Method normalResource</span></span>

```xpp
public int normalResource([int value])
```

### <a name="parameters---normalresource"></a><span data-ttu-id="f0b36-375">パラメーター - normalResource</span><span class="sxs-lookup"><span data-stu-id="f0b36-375">Parameters - normalResource</span></span>

<span data-ttu-id="f0b36-376">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-376">value</span></span>  

### <a name="return-value---normalresource"></a><span data-ttu-id="f0b36-377">戻り値 - normalResource</span><span class="sxs-lookup"><span data-stu-id="f0b36-377">Return Value - normalResource</span></span>

## <a name="method-object"></a><span data-ttu-id="f0b36-378">メソッド object</span><span class="sxs-lookup"><span data-stu-id="f0b36-378">Method object</span></span>

<span data-ttu-id="f0b36-379">MenuFunction クラスにより実行されるオブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-379">Gets or sets the object that is run by the MenuFunction class.</span></span>

```xpp
public str object([str value])
```

### <a name="parameters---object"></a><span data-ttu-id="f0b36-380">パラメーター - object</span><span class="sxs-lookup"><span data-stu-id="f0b36-380">Parameters - object</span></span>

<span data-ttu-id="f0b36-381">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-381">value</span></span>  

### <a name="return-value---object"></a><span data-ttu-id="f0b36-382">戻り値 - object</span><span class="sxs-lookup"><span data-stu-id="f0b36-382">Return Value - object</span></span>

<span data-ttu-id="f0b36-383">MenuFunction クラスにより実行されるオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="f0b36-383">The object that is run by the MenuFunction class.</span></span>

### <a name="remarks---object"></a><span data-ttu-id="f0b36-384">備考 - object</span><span class="sxs-lookup"><span data-stu-id="f0b36-384">Remarks - object</span></span>

<span data-ttu-id="f0b36-385">プロパティ値は、次のオブジェクトのいずれかである場合があります。</span><span class="sxs-lookup"><span data-stu-id="f0b36-385">The property value may be one of the following objects:</span></span>

-   <span data-ttu-id="f0b36-386">フォーム。</span><span class="sxs-lookup"><span data-stu-id="f0b36-386">Form.</span></span>
-   <span data-ttu-id="f0b36-387">レポート。</span><span class="sxs-lookup"><span data-stu-id="f0b36-387">Report.</span></span>
-   <span data-ttu-id="f0b36-388">ジョブ。</span><span class="sxs-lookup"><span data-stu-id="f0b36-388">Job.</span></span>
-   <span data-ttu-id="f0b36-389">クラス。</span><span class="sxs-lookup"><span data-stu-id="f0b36-389">Class.</span></span>
-   <span data-ttu-id="f0b36-390">クエリ。</span><span class="sxs-lookup"><span data-stu-id="f0b36-390">Query.</span></span>

## <a name="method-objecttype"></a><span data-ttu-id="f0b36-391">メソッド objectType</span><span class="sxs-lookup"><span data-stu-id="f0b36-391">Method objectType</span></span>

```xpp
public int objectType([int value])
```

### <a name="parameters---objecttype"></a><span data-ttu-id="f0b36-392">パラメーター - objectType</span><span class="sxs-lookup"><span data-stu-id="f0b36-392">Parameters - objectType</span></span>

<span data-ttu-id="f0b36-393">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-393">value</span></span>  

### <a name="return-value---objecttype"></a><span data-ttu-id="f0b36-394">戻り値 - objectType</span><span class="sxs-lookup"><span data-stu-id="f0b36-394">Return Value - objectType</span></span>

## <a name="method-openmode"></a><span data-ttu-id="f0b36-395">メソッド openMode</span><span class="sxs-lookup"><span data-stu-id="f0b36-395">Method openMode</span></span>

```xpp
public int openMode([int value])
```

### <a name="parameters---openmode"></a><span data-ttu-id="f0b36-396">パラメーター - openMode</span><span class="sxs-lookup"><span data-stu-id="f0b36-396">Parameters - openMode</span></span>

<span data-ttu-id="f0b36-397">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-397">value</span></span>  

### <a name="return-value---openmode"></a><span data-ttu-id="f0b36-398">戻り値 - openMode</span><span class="sxs-lookup"><span data-stu-id="f0b36-398">Return Value - openMode</span></span>

## <a name="method-origin"></a><span data-ttu-id="f0b36-399">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="f0b36-399">Method origin</span></span>

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a><span data-ttu-id="f0b36-400">パラメーター - origin</span><span class="sxs-lookup"><span data-stu-id="f0b36-400">Parameters - origin</span></span>

<span data-ttu-id="f0b36-401">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-401">value</span></span>  

### <a name="return-value---origin"></a><span data-ttu-id="f0b36-402">戻り値 - origin</span><span class="sxs-lookup"><span data-stu-id="f0b36-402">Return Value - origin</span></span>

## <a name="method-parameters"></a><span data-ttu-id="f0b36-403">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="f0b36-403">Method parameters</span></span>

<span data-ttu-id="f0b36-404">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-404">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

```xpp
public str parameters([str value])
```

### <a name="parameters---parameters"></a><span data-ttu-id="f0b36-405">パラメーター - parameters</span><span class="sxs-lookup"><span data-stu-id="f0b36-405">Parameters - parameters</span></span>

<span data-ttu-id="f0b36-406">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-406">value</span></span>  

### <a name="return-value---parameters"></a><span data-ttu-id="f0b36-407">戻り値 - parameters</span><span class="sxs-lookup"><span data-stu-id="f0b36-407">Return Value - parameters</span></span>

<span data-ttu-id="f0b36-408">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="f0b36-408">The list of parameters that are passed to the object.</span></span>

### <a name="remarks---parameters"></a><span data-ttu-id="f0b36-409">備考 - parameters</span><span class="sxs-lookup"><span data-stu-id="f0b36-409">Remarks - parameters</span></span>

<span data-ttu-id="f0b36-410">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="f0b36-410">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="f0b36-411">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-411">Objects ignore passed, unrecognized parameters.</span></span>

## <a name="method-query"></a><span data-ttu-id="f0b36-412">メソッド query</span><span class="sxs-lookup"><span data-stu-id="f0b36-412">Method query</span></span>

```xpp
public str query([str value])
```

### <a name="parameters---query"></a><span data-ttu-id="f0b36-413">パラメーター - query</span><span class="sxs-lookup"><span data-stu-id="f0b36-413">Parameters - query</span></span>

<span data-ttu-id="f0b36-414">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-414">value</span></span>  

### <a name="return-value---query"></a><span data-ttu-id="f0b36-415">戻り値 - query</span><span class="sxs-lookup"><span data-stu-id="f0b36-415">Return Value - query</span></span>

## <a name="method-readpermissions"></a><span data-ttu-id="f0b36-416">メソッド readPermissions</span><span class="sxs-lookup"><span data-stu-id="f0b36-416">Method readPermissions</span></span>

```xpp
public int readPermissions([int value])
```

### <a name="parameters---readpermissions"></a><span data-ttu-id="f0b36-417">パラメーター - readPermissions</span><span class="sxs-lookup"><span data-stu-id="f0b36-417">Parameters - readPermissions</span></span>

<span data-ttu-id="f0b36-418">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-418">value</span></span>  

### <a name="return-value---readpermissions"></a><span data-ttu-id="f0b36-419">戻り値 - readPermissions</span><span class="sxs-lookup"><span data-stu-id="f0b36-419">Return Value - readPermissions</span></span>

## <a name="method-reportdesign"></a><span data-ttu-id="f0b36-420">メソッド reportDesign</span><span class="sxs-lookup"><span data-stu-id="f0b36-420">Method reportDesign</span></span>

```xpp
public str reportDesign([str value])
```

### <a name="parameters---reportdesign"></a><span data-ttu-id="f0b36-421">パラメーター - reportDesign</span><span class="sxs-lookup"><span data-stu-id="f0b36-421">Parameters - reportDesign</span></span>

<span data-ttu-id="f0b36-422">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-422">value</span></span>  

### <a name="return-value---reportdesign"></a><span data-ttu-id="f0b36-423">戻り値 - reportDesign</span><span class="sxs-lookup"><span data-stu-id="f0b36-423">Return Value - reportDesign</span></span>

## <a name="method-runon"></a><span data-ttu-id="f0b36-424">メソッド runOn</span><span class="sxs-lookup"><span data-stu-id="f0b36-424">Method runOn</span></span>

```xpp
public int runOn([int value])
```

### <a name="parameters---runon"></a><span data-ttu-id="f0b36-425">パラメーター - runOn</span><span class="sxs-lookup"><span data-stu-id="f0b36-425">Parameters - runOn</span></span>

<span data-ttu-id="f0b36-426">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-426">value</span></span>  

### <a name="return-value---runon"></a><span data-ttu-id="f0b36-427">戻り値 - runOn</span><span class="sxs-lookup"><span data-stu-id="f0b36-427">Return Value - runOn</span></span>

## <a name="method-type"></a><span data-ttu-id="f0b36-428">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="f0b36-428">Method type</span></span>

```xpp
public MenuItemType type()
```

### <a name="return-value---type"></a><span data-ttu-id="f0b36-429">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="f0b36-429">Return Value - type</span></span>

## <a name="method-updatepermissions"></a><span data-ttu-id="f0b36-430">メソッド updatePermissions</span><span class="sxs-lookup"><span data-stu-id="f0b36-430">Method updatePermissions</span></span>

```xpp
public int updatePermissions([int value])
```

### <a name="parameters---updatepermissions"></a><span data-ttu-id="f0b36-431">パラメーター - updatePermissions</span><span class="sxs-lookup"><span data-stu-id="f0b36-431">Parameters - updatePermissions</span></span>

<span data-ttu-id="f0b36-432">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-432">value</span></span>  

### <a name="return-value---updatepermissions"></a><span data-ttu-id="f0b36-433">戻り値 - updatePermissions</span><span class="sxs-lookup"><span data-stu-id="f0b36-433">Return Value - updatePermissions</span></span>

## <a name="method-viewuserlicense"></a><span data-ttu-id="f0b36-434">メソッド viewUserLicense</span><span class="sxs-lookup"><span data-stu-id="f0b36-434">Method viewUserLicense</span></span>

```xpp
public int viewUserLicense([int value])
```

### <a name="parameters---viewuserlicense"></a><span data-ttu-id="f0b36-435">パラメーター - viewUserLicense</span><span class="sxs-lookup"><span data-stu-id="f0b36-435">Parameters - viewUserLicense</span></span>

<span data-ttu-id="f0b36-436">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-436">value</span></span>  

### <a name="return-value---viewuserlicense"></a><span data-ttu-id="f0b36-437">戻り値 - viewUserLicense</span><span class="sxs-lookup"><span data-stu-id="f0b36-437">Return Value - viewUserLicense</span></span>

## <a name="method-web"></a><span data-ttu-id="f0b36-438">メソッド web</span><span class="sxs-lookup"><span data-stu-id="f0b36-438">Method web</span></span>

```xpp
public str web([str value])
```

### <a name="parameters---web"></a><span data-ttu-id="f0b36-439">パラメーター - web</span><span class="sxs-lookup"><span data-stu-id="f0b36-439">Parameters - web</span></span>

<span data-ttu-id="f0b36-440">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-440">value</span></span>  

### <a name="return-value---web"></a><span data-ttu-id="f0b36-441">戻り値 - web</span><span class="sxs-lookup"><span data-stu-id="f0b36-441">Return Value - web</span></span>

## <a name="method-webaccess"></a><span data-ttu-id="f0b36-442">メソッド webAccess</span><span class="sxs-lookup"><span data-stu-id="f0b36-442">Method webAccess</span></span>

```xpp
public int webAccess([int value])
```

### <a name="parameters---webaccess"></a><span data-ttu-id="f0b36-443">パラメーター - webAccess</span><span class="sxs-lookup"><span data-stu-id="f0b36-443">Parameters - webAccess</span></span>

<span data-ttu-id="f0b36-444">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-444">value</span></span>  

### <a name="return-value---webaccess"></a><span data-ttu-id="f0b36-445">戻り値 - webAccess</span><span class="sxs-lookup"><span data-stu-id="f0b36-445">Return Value - webAccess</span></span>

## <a name="method-webmenuitemname"></a><span data-ttu-id="f0b36-446">メソッド webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="f0b36-446">Method webMenuItemName</span></span>

```xpp
public str webMenuItemName([str value])
```

### <a name="parameters---webmenuitemname"></a><span data-ttu-id="f0b36-447">パラメーター - webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="f0b36-447">Parameters - webMenuItemName</span></span>

<span data-ttu-id="f0b36-448">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-448">value</span></span>  

### <a name="return-value---webmenuitemname"></a><span data-ttu-id="f0b36-449">戻り値 - webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="f0b36-449">Return Value - webMenuItemName</span></span>

## <a name="method-webpage"></a><span data-ttu-id="f0b36-450">メソッド webPage</span><span class="sxs-lookup"><span data-stu-id="f0b36-450">Method webPage</span></span>

```xpp
public str webPage([str value])
```

### <a name="parameters---webpage"></a><span data-ttu-id="f0b36-451">パラメーター - webPage</span><span class="sxs-lookup"><span data-stu-id="f0b36-451">Parameters - webPage</span></span>

<span data-ttu-id="f0b36-452">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-452">value</span></span>  

### <a name="return-value---webpage"></a><span data-ttu-id="f0b36-453">戻り値 - webPage</span><span class="sxs-lookup"><span data-stu-id="f0b36-453">Return Value - webPage</span></span>

## <a name="method-websecuretransaction"></a><span data-ttu-id="f0b36-454">メソッド webSecureTransaction</span><span class="sxs-lookup"><span data-stu-id="f0b36-454">Method webSecureTransaction</span></span>

```xpp
public boolean webSecureTransaction([boolean value])
```

### <a name="parameters---websecuretransaction"></a><span data-ttu-id="f0b36-455">パラメーター - webSecureTransaction</span><span class="sxs-lookup"><span data-stu-id="f0b36-455">Parameters - webSecureTransaction</span></span>

<span data-ttu-id="f0b36-456">値</span><span class="sxs-lookup"><span data-stu-id="f0b36-456">value</span></span>  

### <a name="return-value---websecuretransaction"></a><span data-ttu-id="f0b36-457">戻り値 - webSecureTransaction</span><span class="sxs-lookup"><span data-stu-id="f0b36-457">Return Value - webSecureTransaction</span></span>

## <a name="method-run"></a><span data-ttu-id="f0b36-458">メソッド run</span><span class="sxs-lookup"><span data-stu-id="f0b36-458">Method run</span></span>

<span data-ttu-id="f0b36-459">xMenuFunction オブジェクトを実行します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-459">Runs the xMenuFunction object.</span></span>

```xpp
public void run([xArgs args])
```

### <a name="parameters---run"></a><span data-ttu-id="f0b36-460">パラメーター - run</span><span class="sxs-lookup"><span data-stu-id="f0b36-460">Parameters - run</span></span>

<span data-ttu-id="f0b36-461">args</span><span class="sxs-lookup"><span data-stu-id="f0b36-461">args</span></span>  
<span data-ttu-id="f0b36-462">xArgs クラス オブジェクト。オプション。</span><span class="sxs-lookup"><span data-stu-id="f0b36-462">An xArgs class object; optional.</span></span>

### <a name="remarks---run"></a><span data-ttu-id="f0b36-463">備考 - run</span><span class="sxs-lookup"><span data-stu-id="f0b36-463">Remarks - run</span></span>

<span data-ttu-id="f0b36-464">この関数は、コードから xMenuFunction オブジェクトを実行するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f0b36-464">This function is used to run a xMenuFunction object from code.</span></span>

## <a name="method-runcalled"></a><span data-ttu-id="f0b36-465">メソッド runCalled</span><span class="sxs-lookup"><span data-stu-id="f0b36-465">Method runCalled</span></span>

```xpp
public static void runCalled(str Name, MenuItemType type, [boolean setContextMenu], [xArgs args])
```

### <a name="parameters---runcalled"></a><span data-ttu-id="f0b36-466">パラメーター - runCalled</span><span class="sxs-lookup"><span data-stu-id="f0b36-466">Parameters - runCalled</span></span>

<span data-ttu-id="f0b36-467">氏名</span><span class="sxs-lookup"><span data-stu-id="f0b36-467">Name</span></span>  

<!-- -->

<span data-ttu-id="f0b36-468">タイプ</span><span class="sxs-lookup"><span data-stu-id="f0b36-468">type</span></span>  

<!-- -->

<span data-ttu-id="f0b36-469">setContextMenu</span><span class="sxs-lookup"><span data-stu-id="f0b36-469">setContextMenu</span></span>  

<!-- -->

<span data-ttu-id="f0b36-470">args</span><span class="sxs-lookup"><span data-stu-id="f0b36-470">args</span></span>  

## <a name="method-runclient"></a><span data-ttu-id="f0b36-471">メソッド runClient</span><span class="sxs-lookup"><span data-stu-id="f0b36-471">Method runClient</span></span>

```xpp
public static void runClient(str Name, MenuItemType type, [boolean setContextMenu], [xArgs args])
```

### <a name="parameters---runclient"></a><span data-ttu-id="f0b36-472">パラメーター - runClient</span><span class="sxs-lookup"><span data-stu-id="f0b36-472">Parameters - runClient</span></span>

<span data-ttu-id="f0b36-473">氏名</span><span class="sxs-lookup"><span data-stu-id="f0b36-473">Name</span></span>  

<!-- -->

<span data-ttu-id="f0b36-474">タイプ</span><span class="sxs-lookup"><span data-stu-id="f0b36-474">type</span></span>  

<!-- -->

<span data-ttu-id="f0b36-475">setContextMenu</span><span class="sxs-lookup"><span data-stu-id="f0b36-475">setContextMenu</span></span>  

<!-- -->

<span data-ttu-id="f0b36-476">args</span><span class="sxs-lookup"><span data-stu-id="f0b36-476">args</span></span>  

## <a name="method-runserver"></a><span data-ttu-id="f0b36-477">メソッド runServer</span><span class="sxs-lookup"><span data-stu-id="f0b36-477">Method runServer</span></span>

```xpp
public static void runServer(str Name, MenuItemType type, [boolean setContextMenu], [xArgs args])
```

### <a name="parameters---runserver"></a><span data-ttu-id="f0b36-478">パラメーター - runServer</span><span class="sxs-lookup"><span data-stu-id="f0b36-478">Parameters - runServer</span></span>

<span data-ttu-id="f0b36-479">氏名</span><span class="sxs-lookup"><span data-stu-id="f0b36-479">Name</span></span>  

<!-- -->

<span data-ttu-id="f0b36-480">タイプ</span><span class="sxs-lookup"><span data-stu-id="f0b36-480">type</span></span>  

<!-- -->

<span data-ttu-id="f0b36-481">setContextMenu</span><span class="sxs-lookup"><span data-stu-id="f0b36-481">setContextMenu</span></span>  

<!-- -->

<span data-ttu-id="f0b36-482">args</span><span class="sxs-lookup"><span data-stu-id="f0b36-482">args</span></span>  

## <a name="method-new"></a><span data-ttu-id="f0b36-483">メソッド new</span><span class="sxs-lookup"><span data-stu-id="f0b36-483">Method new</span></span>

<span data-ttu-id="f0b36-484">xMenuFunction の名前と MenuItemType を xMenuFunction コンストラクターに渡して、新しい xMenuFunction オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="f0b36-484">Creates a new xMenuFunction object by passing xMenuFunction's name and MenuItemType to the xMenuFunction constructor.</span></span>

```xpp
public void new(str Name, MenuItemType type)
```

### <a name="parameters---new"></a><span data-ttu-id="f0b36-485">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="f0b36-485">Parameters - new</span></span>

<span data-ttu-id="f0b36-486">氏名</span><span class="sxs-lookup"><span data-stu-id="f0b36-486">Name</span></span>  
<span data-ttu-id="f0b36-487">MenuItemType システム列挙型の定数: MenuItemType::Display、MenuItemType::Output、または MenuItemType::Action。</span><span class="sxs-lookup"><span data-stu-id="f0b36-487">A constant in the MenuItemType system enumeration: MenuItemType::Display, MenuItemType::Output, or MenuItemType::Action.</span></span>

<!-- -->

<span data-ttu-id="f0b36-488">タイプ</span><span class="sxs-lookup"><span data-stu-id="f0b36-488">type</span></span>  
<span data-ttu-id="f0b36-489">MenuItemType システム列挙型の定数: MenuItemType::Display、MenuItemType::Output、または MenuItemType::Action。</span><span class="sxs-lookup"><span data-stu-id="f0b36-489">A constant in the MenuItemType system enumeration: MenuItemType::Display, MenuItemType::Output, or MenuItemType::Action.</span></span>

### <a name="remarks---new"></a><span data-ttu-id="f0b36-490">備考 - new</span><span class="sxs-lookup"><span data-stu-id="f0b36-490">Remarks - new</span></span>

<span data-ttu-id="f0b36-491">xMenuFunction オブジェクトを作成するとき、パラメータは既存の xMenuFunction を一意に識別する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f0b36-491">When creating a xMenuFunction object, the parameters must uniquely identify an existing xMenuFunction.</span></span> <span data-ttu-id="f0b36-492">それ以外の場合は、Exception::Internal がスローされます。</span><span class="sxs-lookup"><span data-stu-id="f0b36-492">If not, Exception::Internal is thrown.</span></span>

## <a name="method-aotrun"></a><span data-ttu-id="f0b36-493">メソッド AOTrun</span><span class="sxs-lookup"><span data-stu-id="f0b36-493">Method AOTrun</span></span>

<span data-ttu-id="f0b36-494">アプリケーション オブジェクト ツリー (AOT) でこのノードとそのサブツリーをコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="f0b36-494">Compiles this node and its subtree in the Application Object Tree (AOT).</span></span>

```xpp
public void AOTrun([xArgs args])
```

### <a name="parameters---aotrun"></a><span data-ttu-id="f0b36-495">パラメーター - AOTrun</span><span class="sxs-lookup"><span data-stu-id="f0b36-495">Parameters - AOTrun</span></span>

<span data-ttu-id="f0b36-496">args</span><span class="sxs-lookup"><span data-stu-id="f0b36-496">args</span></span>  

