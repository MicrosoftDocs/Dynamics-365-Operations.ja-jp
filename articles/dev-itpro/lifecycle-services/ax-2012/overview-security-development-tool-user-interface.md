---
title: セキュリティ開発ツール
description: このトピックでは、セキュリティ開発ツールのユーザー インターフェイスについて説明します。
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 18571
ms.assetid: bf4110a1-c23a-4fe9-8f56-ab9ff5766f76
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 006618c4e1073cbfa00aac6e9d51fa2b9608571f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555278"
---
# <a name="security-development-tool"></a><span data-ttu-id="f6016-103">セキュリティ開発ツール</span><span class="sxs-lookup"><span data-stu-id="f6016-103">Security Development Tool</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f6016-104">このトピックでは、セキュリティ開発ツールのユーザー インターフェイスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f6016-104">This topic describes the user interface of the Security Development Tool.</span></span>

<span data-ttu-id="f6016-105">**注記:** これは、予備的なプレリリース ドキュメントで、予告なしに変更される場合があります。</span><span class="sxs-lookup"><span data-stu-id="f6016-105">**Note:** This is pre-release documentation of a preliminary nature and is subject to change at any time without notice.</span></span> <span data-ttu-id="f6016-106">ここで提供されている情報の正確さは保障されていません。</span><span class="sxs-lookup"><span data-stu-id="f6016-106">Microsoft cannot guarantee the accuracy of any information provided herein.</span></span>

## <a name="overview-of-the-main-form"></a><span data-ttu-id="f6016-107">メイン フォームの概要</span><span class="sxs-lookup"><span data-stu-id="f6016-107">Overview of the main form</span></span>
<span data-ttu-id="f6016-108">このセクションでは、メイン フォームのコントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f6016-108">This section describes the controls in the main form.</span></span>

### <a name="main-form"></a><span data-ttu-id="f6016-109">主要フォーム</span><span class="sxs-lookup"><span data-stu-id="f6016-109">Main form</span></span>

![セキュリティ開発ツールの主要フォーム](./media/securitydevelopmenttoolmainform.png)

-   <span data-ttu-id="f6016-111">**タイプ**フィールド – セキュリティ オブジェクトのタイプ: **ロール**、**職務**、または**権限**。</span><span class="sxs-lookup"><span data-stu-id="f6016-111">**Type** field – The type of security object: **Role**, **Duty**, or **Privilege**.</span></span>
-   <span data-ttu-id="f6016-112">**名前**フィールド – 選択したセキュリティ オブジェクトのラベル。</span><span class="sxs-lookup"><span data-stu-id="f6016-112">**Name** field – The label of the selected security object.</span></span>
-   <span data-ttu-id="f6016-113">**更新**ボタン – 現在選択されているセキュリティ オブジェクトのアクセス許可を再読み込みします。</span><span class="sxs-lookup"><span data-stu-id="f6016-113">**Refresh** button – Reload permissions for the security object that is currently selected.</span></span>
-   <span data-ttu-id="f6016-114">ツリー ビュー - リッチ クライアント、Microsoft Dynamics AX のエンタープライズ ポータル、およびサービス操作のためのメイン メニュー ビュー。</span><span class="sxs-lookup"><span data-stu-id="f6016-114">Tree view – The main menu view for the rich client, Enterprise Portal for Microsoft Dynamics AX, and service operations.</span></span>

<span data-ttu-id="f6016-115">メニュー項目、Web メニュー項目、またはサービス操作を選択すると、リスト ビュー内のエントリ ポイントが自動的に選択されます。</span><span class="sxs-lookup"><span data-stu-id="f6016-115">When you select a menu item, web menu item, or service operation, the entry point is selected automatically in the list view.</span></span> <span data-ttu-id="f6016-116">メニューについて表示されるアクセス レベルは、サブメニュー項目に与えられる最上位のアクセス レベルによって決定されます。</span><span class="sxs-lookup"><span data-stu-id="f6016-116">The access level that is shown for a menu is determined by the highest access level that is granted to a submenu item.</span></span> <span data-ttu-id="f6016-117">最低レベルから最高レベルへのアクセス レベルの優先順位は、**アクセス権なし**、**表示**、**編集**、**作成**、**修正**、および **フル コントロール** です。</span><span class="sxs-lookup"><span data-stu-id="f6016-117">The order of precedence for access levels, from lowest to highest, is **No Access**, **View**, **Edit**, **Create**, **Correction**, and **Full Control**.</span></span> <span data-ttu-id="f6016-118">たとえば、次の図で、**すべての仕入先**メニュー項目が**表示**アクセス レベルを付与し、**保留中の仕入先**メニュー項目が**編集**アクセス レベルを付与する場合、親メニュー、**買掛金管理**、**共通**、および**仕入先**は**編集**アクセス レベルでマークされます。</span><span class="sxs-lookup"><span data-stu-id="f6016-118">For example, in the following figure, if the **All vendors** menu item is granted the **View** access level, and the **Vendors on hold** menu item is granted the **Edit** access level, the parent menus, **Accounts payable**, **Common**, and **Vendors**, are marked with the **Edit** access level.</span></span>

### <a name="menu-access-aggregation-in-tree-view"></a><span data-ttu-id="f6016-119">ツリー ビューでのメニュー アクセス集約</span><span class="sxs-lookup"><span data-stu-id="f6016-119">Menu access aggregation in tree view</span></span>

<span data-ttu-id="f6016-120">![セキュリティ開発ツールのメニューアクセス集約](./media/sdt_menuaggregatedaccesslevel.png) ツリー ビューのノードへのアクセス レベルが変化すると、ノードは太字で表示されます。</span><span class="sxs-lookup"><span data-stu-id="f6016-120">![Security Development Tool Menu Access Aggregation](./media/sdt_menuaggregatedaccesslevel.png) When the level of access to a node in the tree view changes, the node is displayed in bold type.</span></span> <span data-ttu-id="f6016-121">メニュー項目へのアクセス レベルが変わりませんが、サブメニュー項目へのアクセス レベルが変わる場合は、親メニュー項目にはアスタリスク (\*) がマークされます。</span><span class="sxs-lookup"><span data-stu-id="f6016-121">If the level of access to a menu item remains the same, but the level of access to a submenu item changes, the parent menu item is marked with an asterisk (\*).</span></span> <span data-ttu-id="f6016-122">次の図では、**買掛金勘定/設定/請求金額/品目の諸費用グループ**へのアクセス レベルが **NoAccess** から**編集**に更新されました。</span><span class="sxs-lookup"><span data-stu-id="f6016-122">In the following figure, the level of access to **Accounts payable/Setup/Charges/Item charges groups** has been updated from **NoAccess** to **Edit**.</span></span>

### <a name="changed-items"></a><span data-ttu-id="f6016-123">変更された項目</span><span class="sxs-lookup"><span data-stu-id="f6016-123">Changed items</span></span>

![セキュリティ開発ツールのアクセス レベル変更](./media/sdtl_treeviewaccesslevelchange.png)

## <a name="shortcut-menu-options"></a><span data-ttu-id="f6016-125">ショートカット メニュー オプション</span><span class="sxs-lookup"><span data-stu-id="f6016-125">Shortcut menu options</span></span>
<span data-ttu-id="f6016-126">ツリー ビューのエントリ ポイントを操作するには、ショートカット メニューを使用します。</span><span class="sxs-lookup"><span data-stu-id="f6016-126">Use the shortcut menu to interact with entry points in the tree view.</span></span> ![SecurityDevelopmentTool\_TreeContextMenu](./media/sdt_treecontextmenu.png)

-   <span data-ttu-id="f6016-128">**すべての子を展開** - サブツリーのすべての品目を展開します。</span><span class="sxs-lookup"><span data-stu-id="f6016-128">**Expand all children** – Expand all subtree items.</span></span>
-   <span data-ttu-id="f6016-129">**現在のワークスペースで開く** – 現在のワークスペースでリンクされたメニュー項目を開きます。</span><span class="sxs-lookup"><span data-stu-id="f6016-129">**Open in current workspace** – Open the linked menu item in the current workspace.</span></span>
-   <span data-ttu-id="f6016-130">**セキュリティ テスト ワークスペースで開く** – **セキュリティ テスト** ワークスペースでリンクされたメニュー項目を開きます。</span><span class="sxs-lookup"><span data-stu-id="f6016-130">**Open in security test workspace** – Open the linked menu item in the **Security test** workspace.</span></span>
-   <span data-ttu-id="f6016-131">**サブメニュー項目の検出** - アプリケーション オブジェクト ツリー (AOT) メタデータを使用して、現在選択されているメニュー項目のリンクされたフォームで使用されるエントリ ポイントを検出します。</span><span class="sxs-lookup"><span data-stu-id="f6016-131">**Discover submenu items** – Use Application Object Tree (AOT) metadata to discover entry points that are used in the linked form for the menu item that is currently selected.</span></span>
-   <span data-ttu-id="f6016-132">**現在のノードと展開したサブツリー品目のエントリ ポイントのアクセス許可を設定** – 選択したエントリ ポイントおよびすべての展開したサブツリー品目のアクセス レベルを設定できる、ガイド フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="f6016-132">**Set entry point permissions for current node and expanded subtree items** – Open a guided form, where you can set the access level for the selected entry point and all the expanded subtree items.</span></span> <span data-ttu-id="f6016-133">詳細については、[エントリ ポイントのアクセス許可の定義または編集](define-edit-entry-point-permissions.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f6016-133">For more information, see [Define or edit entry point permissions](define-edit-entry-point-permissions.md).</span></span>
-   <span data-ttu-id="f6016-134">**参照職務権限** – 選択したエントリ ポイントに対応するアクセス レベルを付与する職務のリストを表示します。</span><span class="sxs-lookup"><span data-stu-id="f6016-134">**Reference duty** – View a list of duties that grant the selected entry point the corresponding access level.</span></span> <span data-ttu-id="f6016-135">選択されたセキュリティ オブジェクトの参照職務権限を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="f6016-135">You can view the reference duty for the selected security object.</span></span> <span data-ttu-id="f6016-136">このオプションは、ロールに対してのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="f6016-136">This option is available only for roles.</span></span>
-   <span data-ttu-id="f6016-137">**参照権限** – 選択したエントリ ポイントに対応するアクセス レベルを付与する権限のリストを表示します。</span><span class="sxs-lookup"><span data-stu-id="f6016-137">**Reference privilege** – View a list of privileges that grant the selected entry point the corresponding access level.</span></span> <span data-ttu-id="f6016-138">選択されたセキュリティ オブジェクトの参照権限を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="f6016-138">You can view the reference privilege for the selected security object.</span></span> <span data-ttu-id="f6016-139">このオプションは、ロールおよび職務にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="f6016-139">This option is available only for roles and duties.</span></span>
-   <span data-ttu-id="f6016-140">**新しい AOT ウィンドウを開く** – 選択したノードの新しい AOT ウィンドウを開きます。</span><span class="sxs-lookup"><span data-stu-id="f6016-140">**Open new AOT window** – Open a new AOT window for the selected node.</span></span>
-   <span data-ttu-id="f6016-141">**AOT プロパティ** - 選択したノードの AOT プロパティを開きます。</span><span class="sxs-lookup"><span data-stu-id="f6016-141">**AOT properties** – Open the AOT properties for the selected node.</span></span>
-   <span data-ttu-id="f6016-142">**メニュー項目の新しい AOT ウィンドウを開く** – リンクされたメニュー項目の新しい AOT ウィンドウを開きます。</span><span class="sxs-lookup"><span data-stu-id="f6016-142">**Open new AOT window for menu item** – Open a new AOT window for the linked menu item.</span></span>
-   <span data-ttu-id="f6016-143">**メニュー項目の AOT プロパティ** - リンクされているメニュー項目の AOT プロパティを開きます。</span><span class="sxs-lookup"><span data-stu-id="f6016-143">**AOT properties for menu item** – Open the AOT properties for the linked menu item.</span></span>

## <a name="list-view"></a><span data-ttu-id="f6016-144">リスト ビュー</span><span class="sxs-lookup"><span data-stu-id="f6016-144">List view</span></span>
<span data-ttu-id="f6016-145">このセクションでは、リスト ビューのリボンのコントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f6016-145">This section describes the controls on the ribbon of the list view.</span></span> <span data-ttu-id="f6016-146">リスト ビューは、Microsoft Dynamics AX 環境のすべてのエントリ ポイントの一覧を提供します。</span><span class="sxs-lookup"><span data-stu-id="f6016-146">The list view provides a list of all entry points for your Microsoft Dynamics AX environment.</span></span> <span data-ttu-id="f6016-147">エントリ ポイントへのアクセス レベルを一括更新するには、一覧表示で複数の行を選択します。</span><span class="sxs-lookup"><span data-stu-id="f6016-147">To bulk update the level of access to entry points, you can select multiple rows in the list view.</span></span>
<span data-ttu-id="f6016-148">![セキュリティ開発ツール リスト ビュー](./media/sdt_listcontextmenu.png)</span><span class="sxs-lookup"><span data-stu-id="f6016-148">![Security Development Tool List View](./media/sdt_listcontextmenu.png)</span></span>

| <span data-ttu-id="f6016-149">**メモ**</span><span class="sxs-lookup"><span data-stu-id="f6016-149">**Note**</span></span>                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6016-150">一覧でエントリ ポイントを選択すると、エントリ ポイントはツリー ビューでは自動的に選択されません。</span><span class="sxs-lookup"><span data-stu-id="f6016-150">When you select an entry point in the list, the entry point is not selected automatically in the tree view.</span></span> <span data-ttu-id="f6016-151">リスト ビューのエントリ ポイントを操作するには、ショートカット メニューを使用します。</span><span class="sxs-lookup"><span data-stu-id="f6016-151">Use the shortcut menu to interact with entry points in the list view.</span></span> <span data-ttu-id="f6016-152">オプションは、ツリー ビューで使用可能なオプションに似ています。</span><span class="sxs-lookup"><span data-stu-id="f6016-152">The options resemble the options that are available in the tree view.</span></span> |

-   <span data-ttu-id="f6016-153">**セキュリティ テスト ワークスペースを開く** – 選択したセキュリティ オブジェクトのアクセス許可を使用してセキュリティ テスト ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="f6016-153">**Open the security test workspace** – Open a security test workspace by using the permissions for the selected security object.</span></span>
-   <span data-ttu-id="f6016-154">**レコードの開始** – レコーダーを開始するときには、現在のワークスペースで業務プロセス フローを実行できます。</span><span class="sxs-lookup"><span data-stu-id="f6016-154">**Start recording** – When you start the recorder, you can execute business process flows in the current workspace.</span></span> <span data-ttu-id="f6016-155">業務プロセス フローの完了時に、記録を停止して、記録されたすべてのエントリ ポイントを表示できます。</span><span class="sxs-lookup"><span data-stu-id="f6016-155">When a business process flow is completed, you can stop recording and view all entry points that were recorded.</span></span> <span data-ttu-id="f6016-156">この関数は、リッチ クライアントのメニュー項目のみを記録します。</span><span class="sxs-lookup"><span data-stu-id="f6016-156">This function records only menu items in the rich client.</span></span>
-   <span data-ttu-id="f6016-157">**トレース ファイルの読み込み** – エンタープライズ ポータルで追跡されたエントリ ポイントを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="f6016-157">**Load trace file** – Load the entry points that have been traced in Enterprise Portal.</span></span> <span data-ttu-id="f6016-158">詳細については、「[Microsoft Dynamics AX エンタープライズ ポータルでのエントリ ポイントの記録](record-entry-points-enterprise-portal.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f6016-158">For more information, see [Record entry points in Microsoft Dynamics AX Enterprise Portal](record-entry-points-enterprise-portal.md).</span></span>
-   <span data-ttu-id="f6016-159">**レコードの保存** – 直前に .xml ファイルに記録したエントリ ポイントの一覧を保存します。</span><span class="sxs-lookup"><span data-stu-id="f6016-159">**Save recording** – Save the list of entry points that you just recorded to an .xml file.</span></span>
-   <span data-ttu-id="f6016-160">**記録の読み込み** – .xml ファイルから記録されたエントリ ポイントの一覧を読み込みます。</span><span class="sxs-lookup"><span data-stu-id="f6016-160">**Load recording** – Load a list of recorded entry points from an .xml file.</span></span>
-   <span data-ttu-id="f6016-161">**追加のメタデータの読み込み** – すべてのエントリ ポイントの追加のメタデータを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="f6016-161">**Load additional metadata** – Load additional metadata for all entry points.</span></span> <span data-ttu-id="f6016-162">このデータには、ラベル、レイヤー、モデル、およびライセンス情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f6016-162">This data includes the label, layer, and model, and also license information.</span></span>
-   <span data-ttu-id="f6016-163">**組織の割り当て** - セキュリティ テスト ワークスペース内の選択されたロール、職務、または権限に組織を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="f6016-163">**Assign organizations** – Assign organizations to the selected role, duty, or privilege in the security test workspace.</span></span>
-   <span data-ttu-id="f6016-164">**ポータル セキュリティ** – セキュリティ テスト ワークスペースが開いている間、エンタープライズ ポータルのセキュリティと Microsoft SQL Server Reporting Services のレポートを有効にします。</span><span class="sxs-lookup"><span data-stu-id="f6016-164">**Portal security** – Enable security for Enterprise Portal and reports for Microsoft SQL Server Reporting Services while the security test workspace is open.</span></span> <span data-ttu-id="f6016-165">セキュリティ テスト ワークスペースが開いているときに、システム管理の役割のアクセス許可が無効になります。</span><span class="sxs-lookup"><span data-stu-id="f6016-165">Permissions for the system administration role are disabled while the security test workspace is open.</span></span> <span data-ttu-id="f6016-166">この機能が有効なとき、X++ ブレークポイントはトリガーされません。</span><span class="sxs-lookup"><span data-stu-id="f6016-166">X++ breakpoints are not triggered when this function is enabled.</span></span> <span data-ttu-id="f6016-167">この関数は、管理者ユーザーとして実行されるユーザーに対してはサポートされていません。 </span><span class="sxs-lookup"><span data-stu-id="f6016-167">This function is not supported for users who run as the Admin user.</span></span>
-   <span data-ttu-id="f6016-168">**フォームのコントロールのマーク** – フォームに **NoAccess** 権限を持つメニュー項目を表示するには、この機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="f6016-168">**Mark form controls** – Enable this function to display menu items that have **NoAccess** permission on forms.</span></span>



<a name="additional-resources"></a><span data-ttu-id="f6016-169">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="f6016-169">Additional resources</span></span>
--------

[<span data-ttu-id="f6016-170">セキュリティ開発ツールをインストールする</span><span class="sxs-lookup"><span data-stu-id="f6016-170">Install the Security Development Tool</span></span>](install-security-development-tool.md)

[<span data-ttu-id="f6016-171">エントリ ポイントのアクセス許可の定義または編集</span><span class="sxs-lookup"><span data-stu-id="f6016-171">Define or edit entry point permissions</span></span>](define-edit-entry-point-permissions.md)

[<span data-ttu-id="f6016-172">Microsoft Dynamics AX エンタープライズ ポータルのエントリ ポイントを記録</span><span class="sxs-lookup"><span data-stu-id="f6016-172">Record entry points in Microsoft Dynamics AX Enterprise Portal</span></span>](record-entry-points-enterprise-portal.md)



