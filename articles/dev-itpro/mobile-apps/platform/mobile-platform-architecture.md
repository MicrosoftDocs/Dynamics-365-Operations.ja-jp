---
title: モバイル プラットフォームのアーキテクチャと設計の考慮事項
description: このトピックでは、モバイル アプリの設計に関する詳細な情報を示します。
author: makhabaz
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 255544
ms.assetid: ''
ms.search.region: Global
ms.author: makhabaz
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Platform update 3
ms.openlocfilehash: a007b7e50436a6dd223633707d7e4f6fc420e510
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368513"
---
# <a name="architecture-and-design-considerations-for-the-mobile-platform"></a><span data-ttu-id="db4fa-103">モバイル プラットフォームのアーキテクチャと設計の考慮事項</span><span class="sxs-lookup"><span data-stu-id="db4fa-103">Architecture and design considerations for the mobile platform</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="db4fa-104">モバイル アプリは、モバイル ワークスペース (およびページに表示されるページとフィールド) のメタデータを取得し、ページのフィールドのデータを取得するために Application Object Server (AOS) と通信します。</span><span class="sxs-lookup"><span data-stu-id="db4fa-104">The mobile app communicates with Application Object Server (AOS) to get the metadata for the mobile workspaces (and the pages and the fields that appear on the page), and to get the data for the fields on the pages.</span></span> <span data-ttu-id="db4fa-105">モバイル アプリがページのデータを要求するたびに、AOS では、モバイル アプリを使うユーザーのコンテキストで使用している新しいセッションを作成します。</span><span class="sxs-lookup"><span data-stu-id="db4fa-105">Each time that the mobile app requests data for a page, AOS creates a new session that uses the context of the user who is using the mobile app.</span></span> <span data-ttu-id="db4fa-106">AOSは、次にユーザーのコンテキストを使用して、対応するフォーム (対応するメニュー項目を使用) を開きます。</span><span class="sxs-lookup"><span data-stu-id="db4fa-106">AOS then uses the user's context to open the corresponding forms (by using the corresponding menu items).</span></span> <span data-ttu-id="db4fa-107">AOS は、すばやく連続して複数のフォームを開くことができ、それらのフォーム (フィルター処理、情報ボックスを開く、タブ ページの変更、ボタンのクリック) に対してアクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="db4fa-107">AOS can open multiple forms in quick succession and perform actions on those forms (for example, filtering, opening FactBoxes, changing tab pages, and clicking buttons).</span></span> <span data-ttu-id="db4fa-108">フォーム上のビジネス ロジックも通常どおり実行されます。</span><span class="sxs-lookup"><span data-stu-id="db4fa-108">Any business logic on the forms is also run as usual.</span></span> <span data-ttu-id="db4fa-109">そのプロセスを通じて AOS は要求されたフィールドからデータ値を収集し、そのデータをモバイル アプリに送り返します。</span><span class="sxs-lookup"><span data-stu-id="db4fa-109">Through that process, AOS collects the data values from the requested fields and then sends that data back to the mobile app.</span></span> 

![モバイル アーキテクチャ](media/mobilearchitecture.png)

<span data-ttu-id="db4fa-111">モバイル アプリ プラットフォームは、Finance and Operations への接続を想定していません。</span><span class="sxs-lookup"><span data-stu-id="db4fa-111">The mobile app platform doesn't assume connectivity to Finance and Operations.</span></span> <span data-ttu-id="db4fa-112">ナビゲーション、データの表示、データ入力などの活動は、データがキャッシュされた後にサーバー接続の必要はありません。</span><span class="sxs-lookup"><span data-stu-id="db4fa-112">Activities such as navigation, data view, and data entry don't require server connectivity after data has been cached.</span></span>

## <a name="understanding-navigation-in-the-mobile-app"></a><span data-ttu-id="db4fa-113">モバイル アプリでのナビゲーションを理解する</span><span class="sxs-lookup"><span data-stu-id="db4fa-113">Understanding navigation in the mobile app</span></span>
<span data-ttu-id="db4fa-114">モバイル アプリのナビゲーションは、ダッシュボード、ワークスペース、ページ、およびアクションという 4 つの簡単な概念で構成されています。</span><span class="sxs-lookup"><span data-stu-id="db4fa-114">Navigation in the mobile app consists of four simple concepts: the dashboard, workspaces, pages, and actions.</span></span> 

![モバイル アプリのナビゲーション概念](media/mobilephoneapp1.png)

-   <span data-ttu-id="db4fa-116">アプリを起動すると、**ダッシュボード** が表示されます。</span><span class="sxs-lookup"><span data-stu-id="db4fa-116">When you start the app, you land on the **dashboard**.</span></span> <span data-ttu-id="db4fa-117">**ダッシュボード**には、Finance and Operations 環境で公開されている**ワークスペース**の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="db4fa-117">On the **dashboard**, you can see a list of **workspaces** that are published in your Finance and Operations environment.</span></span>
-   <span data-ttu-id="db4fa-118">各**ワークスペース**では、そのワークスペースで使用可能な**ページ**の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="db4fa-118">In each **workspace**, you can see a list of **pages** that are available for that workspace.</span></span>
-   <span data-ttu-id="db4fa-119">**ページ**では、1 ページ以上の Finance and Operations のホームから収集されたデータを表示できます。</span><span class="sxs-lookup"><span data-stu-id="db4fa-119">On a **page**, you can view data that is collected from one or more Finance and Operations forms.</span></span>
-   <span data-ttu-id="db4fa-120">**ページ**からは、エンティティの詳細または明細行などの、関連データの他の**ページ**に移動することができます。</span><span class="sxs-lookup"><span data-stu-id="db4fa-120">From a **page**, you can navigate to other **pages** for related data, such as an entity details or lines.</span></span>
-   <span data-ttu-id="db4fa-121">**ページ**では、そのページで使用可能な**アクション**のリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="db4fa-121">On a **page**, you can see a list of **actions** that are available for that page.</span></span>
-   <span data-ttu-id="db4fa-122">**アクション** 既存のデータを作成または編集できます。</span><span class="sxs-lookup"><span data-stu-id="db4fa-122">**Actions** let you create or edit existing data.</span></span>

### <a name="notes"></a><span data-ttu-id="db4fa-123">摘要</span><span class="sxs-lookup"><span data-stu-id="db4fa-123">Notes</span></span>

<span data-ttu-id="db4fa-124">モバイル アプリでデータやメタデータを更新するために、いつでもモバイル アプリでプルして更新することができます。</span><span class="sxs-lookup"><span data-stu-id="db4fa-124">At any time, you can pull-to-refresh in the mobile app to make the mobile app update its data or metadata.</span></span> <span data-ttu-id="db4fa-125">既存のワークスペースを編集またはワークスペースを発行した後、モバイル アプリ、ワークスペースのリスト (ワークスペースまたはビジネス ロジックを追加した場合) またはページのリスト (アクションおよびページ修正された) で、プルリフレッシュしてください。</span><span class="sxs-lookup"><span data-stu-id="db4fa-125">After you edit an existing workspace or publish a workspace, be sure to pull-to-refresh in the mobile app, in either the list of workspaces (if you added a workspace or business logic) or the list of pages (if you modified a page or an action).</span></span> <span data-ttu-id="db4fa-126">Finance and Operations に対して公開済みのワークスペースはすべてのユーザーに対して表示されます。</span><span class="sxs-lookup"><span data-stu-id="db4fa-126">Workspaces that have been published to Finance and Operations are visible to all users.</span></span> <span data-ttu-id="db4fa-127">Microsoft Dynamics 365 for Finance and Operationsプラットフォームの更新プログラム 3 では、メニュー項目のセキュリティにより、ユーザーにアクセス権がないページは自動的に非表示になります。</span><span class="sxs-lookup"><span data-stu-id="db4fa-127">In Microsoft Dynamics 365 for Finance and Operations platform update 3, menu item security automatically hides pages that the user doesn’t have access to.</span></span> <span data-ttu-id="db4fa-128">ワークスペースの任意のページへのへのアクセス権がユーザーにない場合、ワークスペース自体が非表示になります。</span><span class="sxs-lookup"><span data-stu-id="db4fa-128">If a user doesn’t have access to any pages in a workspace, the workspace itself is hidden.</span></span>

## <a name="using-the-mobile-app-designer"></a><span data-ttu-id="db4fa-129">モバイル アプリ デザイナーの使用</span><span class="sxs-lookup"><span data-stu-id="db4fa-129">Using the mobile app designer</span></span>
<span data-ttu-id="db4fa-130">モバイル アプリ デザイナーでは、モバイル アプリに表示されるフォームから特定のデータ フィールドを選択できます。</span><span class="sxs-lookup"><span data-stu-id="db4fa-130">The mobile app designer lets you select the specific data fields from forms that should appear in the mobile app.</span></span> 

<span data-ttu-id="db4fa-131">**モバイル ワークスペースは、デザイナーを通じて、X++ 属性 API、またはその両方の組み合わせを使用して作成することができます。モバイルワークスペースの構築に X++ API を使用する方法の詳細については**、[ワークスペース クラスの概要](scenarios/mobile-workspace-configuration.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="db4fa-131">**A mobile workspace can be created through designer, using X++ attribute APIs or a combination of both. See [Workspace class overview](scenarios/mobile-workspace-configuration.md) for more details on using X++ APIs for building a mobile workspace.**</span></span>

![モバイル アプリ デザイナー](media/mobileappdesigner.png)

1.  <span data-ttu-id="db4fa-133">Finance and Operations クライアントを開きます。</span><span class="sxs-lookup"><span data-stu-id="db4fa-133">Open the Finance and Operations client.</span></span> 
2.  <span data-ttu-id="db4fa-134">**設定** &gt; **モバイル アプリ**に移動します。</span><span class="sxs-lookup"><span data-stu-id="db4fa-134">Go to **Settings** &gt; **Mobile app**.</span></span>
3.  <span data-ttu-id="db4fa-135">新しいワークスペースを作成するか、編集する既存のワークスペースを選択します。</span><span class="sxs-lookup"><span data-stu-id="db4fa-135">Create a new workspace, or select an existing workspace to edit.</span></span>
4.  <span data-ttu-id="db4fa-136">ワークスペース、アイコン、および色の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="db4fa-136">Specify the name of the workspace, an icon, and a color.</span></span>
5.  <span data-ttu-id="db4fa-137">ワークスペースにページを追加するか、既存のページを編集します。</span><span class="sxs-lookup"><span data-stu-id="db4fa-137">Add pages to the workspace, or edit an existing page.</span></span>
6.  <span data-ttu-id="db4fa-138">ページの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="db4fa-138">Specify the name of the page.</span></span>
7.  <span data-ttu-id="db4fa-139">**フィールドの選択**をクリックし、ページに追加するデータ フィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="db4fa-139">Click **Select Fields** to select the data fields to add to the page.</span></span>
8.  <span data-ttu-id="db4fa-140">追加するデータ フィールドのあるフォームを開いて、フィールドの横に表示される黄色のプラス記号 (+) をクリックします。</span><span class="sxs-lookup"><span data-stu-id="db4fa-140">Open the forms that have the data fields that you want to add, and then click the yellow plus sign (+) that appears next to the fields.</span></span> <span data-ttu-id="db4fa-141">フィールドは、選択した順序で追加されます。</span><span class="sxs-lookup"><span data-stu-id="db4fa-141">The fields are added in the order that you select them in.</span></span> <span data-ttu-id="db4fa-142">複数のフォームから、任意の順序で、フィールドを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="db4fa-142">You can add fields from multiple forms, in any order.</span></span>
9.  <span data-ttu-id="db4fa-143">フィールドの選択を完了したら、**完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="db4fa-143">When you've finished selecting fields, click **Done**.</span></span>
10. <span data-ttu-id="db4fa-144">フィールド リストをページに追加した場合、**リスト** タイプがフィールド リスト内の項目のいずれかに指定されます。</span><span class="sxs-lookup"><span data-stu-id="db4fa-144">If you've added a field list to the page, you will see that the **List** type is specified for one of the items in the field list.</span></span> <span data-ttu-id="db4fa-145">以下の手順に従い、必要に応じてそのリストに品目の詳細ページを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="db4fa-145">You can optionally add a details page for items in that list by following these steps:</span></span>
    1.  <span data-ttu-id="db4fa-146">デザイナーでクリックしてリストを選択します。</span><span class="sxs-lookup"><span data-stu-id="db4fa-146">Select the list by clicking on it in the designer.</span></span>
    2.  <span data-ttu-id="db4fa-147">**詳細ページの追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="db4fa-147">Click **Add details page**.</span></span>
    3.  <span data-ttu-id="db4fa-148">必要に応じて、手順 6 ～ 10 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="db4fa-148">Repeat steps 6 through 10 as you require.</span></span>

### <a name="refreshing-the-app-after-you-make-changes"></a><span data-ttu-id="db4fa-149">変更が完了したら、アプリを更新</span><span class="sxs-lookup"><span data-stu-id="db4fa-149">Refreshing the app after you make changes</span></span>

| <span data-ttu-id="db4fa-150">変更のタイプ</span><span class="sxs-lookup"><span data-stu-id="db4fa-150">Type of change</span></span>     | <span data-ttu-id="db4fa-151">説明</span><span class="sxs-lookup"><span data-stu-id="db4fa-151">Description</span></span>                      |
|-------|----------------------------------------------|
| <span data-ttu-id="db4fa-152">新しいワークスペース、削除されたワークスペース、またはワークスペースの名前、色、またはアイコンへの変更</span><span class="sxs-lookup"><span data-stu-id="db4fa-152">New workspaces, deleted workspaces, or changes to the name, color, or icon of a workspace</span></span> | <span data-ttu-id="db4fa-153">ワークスペースの一覧が表示される、アプリの主要なランディング ページ (ダッシュボード) からプルして更新します。</span><span class="sxs-lookup"><span data-stu-id="db4fa-153">Pull-to-refresh from the main landing page (dashboard) of the app, where you see the list of workspaces.</span></span><br>![ダッシュボードからプルして更新](media/refreshworkspaces.png) |
| <span data-ttu-id="db4fa-155">その他のすべての変更 (新しいまたは変更されたページまたはアクション、またはビジネス ロジックへ変更)</span><span class="sxs-lookup"><span data-stu-id="db4fa-155">All other changes (new or changed pages or actions, or changes to business logic)</span></span>         | <span data-ttu-id="db4fa-156">編集されたページまたはアクションを持つワークスペースからプルして更新します。</span><span class="sxs-lookup"><span data-stu-id="db4fa-156">Pull-to-refresh from the workspace that has the edited pages or actions.</span></span><br>![ワークスペースからプルして更新](media/refreshpages.png)                                             |

### <a name="additional-resources"></a><span data-ttu-id="db4fa-158">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="db4fa-158">Additional resources</span></span>

[<span data-ttu-id="db4fa-159">ページ デザインのガイドライン</span><span class="sxs-lookup"><span data-stu-id="db4fa-159">Page design guidelines</span></span>](page-design-guidelines.md)

[<span data-ttu-id="db4fa-160">アクション デザインのガイドライン</span><span class="sxs-lookup"><span data-stu-id="db4fa-160">Action design guidelines</span></span>](action-design-guidelines.md)

[<span data-ttu-id="db4fa-161">フォーム デザインの要件</span><span class="sxs-lookup"><span data-stu-id="db4fa-161">Form design requirements</span></span>](form-design-requirements.md)
