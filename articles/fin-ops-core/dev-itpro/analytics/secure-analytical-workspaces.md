---
title: Power BI Embedded を使用して分析ワークスペースおよびレポートをセキュリティで保護
description: このトピックでは、Power BI Embedded を使用して提供されるレポートと、ビューアーのアクセス権に基づいてデータ セットへのアクセスを保護するための推奨方法について説明します。
author: robinarh
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: kfend
ms.custom: 21551
ms.assetid: ''
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b9fa3dcd0b81e2e323fdc9c08b8dd1d5625e0bed
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682205"
---
# <a name="help-secure-analytical-workspaces-and-reports-by-using-power-bi-embedded"></a><span data-ttu-id="18cc4-103">Power BI Embedded を使用して分析ワークスペースおよびレポートをセキュリティで保護</span><span class="sxs-lookup"><span data-stu-id="18cc4-103">Help secure analytical workspaces and reports by using Power BI Embedded</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="18cc4-104">この機能は、Microsoft Dynamics 365 for Finance and Operations、Enterprise edition (2017 年 7 月) (バージョン7.2) 以降のリリースでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="18cc4-104">This feature is supported in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) (version 7.2) and later releases.</span></span>

## <a name="introduction"></a><span data-ttu-id="18cc4-105">はじめに</span><span class="sxs-lookup"><span data-stu-id="18cc4-105">Introduction</span></span>
<span data-ttu-id="18cc4-106">このトピックでは、Microsoft Power BI Embedded を使用して提供される、分析ワークスペースとレポートのセキュリティ保護を支援するアプリケーション開発者向けにウォークスルーを提供します。</span><span class="sxs-lookup"><span data-stu-id="18cc4-106">This topic provides a walk-through for application developers who want to help secure analytical workspaces and reports that are delivered by using Microsoft Power BI Embedded.</span></span> <span data-ttu-id="18cc4-107">ビューアーのアクセス権に基づいてレポートおよびデータ セット両方へのアクセスを保護するための推奨方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="18cc4-107">It describes the recommended strategies for securing access to both the reports and the data set, based on viewer access rights.</span></span> <span data-ttu-id="18cc4-108">このトピックに記載されている手法を使用することにより、ユーザーからレポートを非表示にし、有効な会社のコンテキストに基づいて、特定のユーザーに適したデータ セットを表示するためにレポートをフィルター処理することができます。</span><span class="sxs-lookup"><span data-stu-id="18cc4-108">By using the techniques that are described in this topic, you can hide reports from users and filter reports to show the data set that is appropriate for a specific user, based on the active company context.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="18cc4-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="18cc4-109">Prerequisites</span></span>
+ <span data-ttu-id="18cc4-110">プラットフォーム更新プログラム 8 以降を実行する開発環境へのアクセス</span><span class="sxs-lookup"><span data-stu-id="18cc4-110">Access to a developer environment that runs Platform update 8 or later</span></span>
+ <span data-ttu-id="18cc4-111">Microsoft Power BI Desktop を使用して作成され、エンティティ格納 データベースから取得されたデータ モデルを持つ分析レポート (.pbix ファイル) です。</span><span class="sxs-lookup"><span data-stu-id="18cc4-111">An analytical report (.pbix file) that was created by using Microsoft Power BI Desktop, and that has a data model that is sourced from the Entity store database</span></span>

## <a name="overview"></a><span data-ttu-id="18cc4-112">概要</span><span class="sxs-lookup"><span data-stu-id="18cc4-112">Overview</span></span>
<span data-ttu-id="18cc4-113">既存のアプリケーション ワークスペースを拡張する場合でも、自身のワークスペースを追加する場合でも、埋め込み分析ビューを使用して、ビジネス データの洞察的でインタラクティブなビューを提供できます。</span><span class="sxs-lookup"><span data-stu-id="18cc4-113">Whether you're extending an existing application workspace or adding your own workspace, you can use embedded analytical views to deliver insightful and interactive views of your business data.</span></span> <span data-ttu-id="18cc4-114">新しい分析ワークスペースおよびレポートを追加する前に、コンテンツを保護するための戦略を確立することは重要です。</span><span class="sxs-lookup"><span data-stu-id="18cc4-114">Before you add new analytical workspaces and reports, it's important that you establish a strategy to help secure the content.</span></span>

<span data-ttu-id="18cc4-115">Power BI Embedded を使用して分析ソリューションを開発する際には、いくつか注意すべき点があります。</span><span class="sxs-lookup"><span data-stu-id="18cc4-115">There are several considerations that you should be aware of when you develop analytical solutions by using Power BI Embedded.</span></span> <span data-ttu-id="18cc4-116">分析レポートはメニュー項目を使用して保護されます。</span><span class="sxs-lookup"><span data-stu-id="18cc4-116">Analytical reports are secured by using menu items.</span></span> <span data-ttu-id="18cc4-117">レポートにアクセスすると、すべての閲覧者はレポートに定義されている基礎データ モデルにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="18cc4-117">After they have access to a report, all viewers can access the underlying data model that is defined in the report.</span></span> <span data-ttu-id="18cc4-118">サービス オプションはレポート データ セットを戻しフィールドを自動的に非表示にすることが可能ですが、レポートのすべての閲覧者はデータ モデル内のフィールドに有効的にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="18cc4-118">Although service options are available that automatically hide the fields that back a report data set, all viewers of the report have effective access to the fields in the data model.</span></span> <span data-ttu-id="18cc4-119">また、レポートがクライアントに表示される方法に影響を与える X++ 拡張機能が使用できます。</span><span class="sxs-lookup"><span data-stu-id="18cc4-119">Additionally, X++ extensions are available that influence the way that the report is presented in the client.</span></span> <span data-ttu-id="18cc4-120">**フィルター** ウィンドウと **レポート** タブの両方を非表示にすることができます。</span><span class="sxs-lookup"><span data-stu-id="18cc4-120">Both the **Filter** pane and the **Report** tabs can be hidden.</span></span> <span data-ttu-id="18cc4-121">ただし、Microsoft Power BI フィルターは、クライアント側スクリプト インジェクションを使用して変更できます。</span><span class="sxs-lookup"><span data-stu-id="18cc4-121">However, Microsoft Power BI filters can be modified by using client-side script injections.</span></span>

### <a name="recommendation"></a><span data-ttu-id="18cc4-122">推奨事項</span><span class="sxs-lookup"><span data-stu-id="18cc4-122">Recommendation</span></span>
<span data-ttu-id="18cc4-123">シナリオ固有の .pbix ファイルを作成して分析ビューを作成する:</span><span class="sxs-lookup"><span data-stu-id="18cc4-123">Create scenario-specific .pbix files to deliver analytical views:</span></span>

+ <span data-ttu-id="18cc4-124">ワークスペースを使用して提供される領域の概要</span><span class="sxs-lookup"><span data-stu-id="18cc4-124">Area overviews that are delivered by using workspaces</span></span>
+ <span data-ttu-id="18cc4-125">題材固有の分析レポート</span><span class="sxs-lookup"><span data-stu-id="18cc4-125">Subject matter–specific analytical reports</span></span>

    > [!NOTE]
    > <span data-ttu-id="18cc4-126">これらの分析レポートは、中堅企業や大規模企業に影響を与えるデータを含むレポートを配信するために使用されることがよくあります。</span><span class="sxs-lookup"><span data-stu-id="18cc4-126">These analytical reports are often used to deliver reports that contain medium-business-impact and high-business-impact data.</span></span>

<span data-ttu-id="18cc4-127">分析レポートを作成する方法の詳細については、[Power BI Desktop の使い方](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="18cc4-127">For more information about how to create analytical reports, see [Getting started with Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).</span></span> <span data-ttu-id="18cc4-128">このページは、魅力的な分析レポート作成ソリューションの作成に役立つ素晴らしいソースです。</span><span class="sxs-lookup"><span data-stu-id="18cc4-128">This page is a great source for insights that can help you create compelling analytical reporting solutions.</span></span>

## <a name="help-secure-analytical-views-that-are-provided-through-embedded-power-bi-reports"></a><span data-ttu-id="18cc4-129">埋め込み Power BI レポートを通して提供される分析ビューのセキュリティを強化する</span><span class="sxs-lookup"><span data-stu-id="18cc4-129">Help secure analytical views that are provided through embedded Power BI reports</span></span>
<span data-ttu-id="18cc4-130">Power BI レポート フィルターと **フィルター** ウィンドウは、**分析** タブに埋め込まれたレポートにセッション コンテキストを渡すためのメカニズムとして機能します。**フィルター** ウィンドウの表示のオンとオフを切り替える機能は、セキュリティ機能ではありません。</span><span class="sxs-lookup"><span data-stu-id="18cc4-130">Power BI report filters and the **Filter** pane serve as a mechanism for passing session context into the report that is embedded on the **Analytics** tab. The capability to turn the visibility of the **Filter** pane on and off isn't a security feature.</span></span> <span data-ttu-id="18cc4-131">Power BI レポート フィルターと、**フィルター** ウィンドウを非表示および表示する機能は、アプリケーション デザイナーが行うユーザー エクスペリエンス (UX) の決定です。</span><span class="sxs-lookup"><span data-stu-id="18cc4-131">Power BI report filters and the capability to hide and show the **Filter** pane are user experience (UX) decisions that the application designer makes.</span></span>

<span data-ttu-id="18cc4-132">定義されている行レベルのセキュリティは Power BI レポートによって継承されていません。</span><span class="sxs-lookup"><span data-stu-id="18cc4-132">Row-level security that is defined isn't inherited by Power BI reports.</span></span> <span data-ttu-id="18cc4-133">代わりに、アプリケーション開発者は、ワークスペースまたはレポートのセキュリティを高めることができます。</span><span class="sxs-lookup"><span data-stu-id="18cc4-133">Instead, application developers can help secure the workspace or the report.</span></span>

### <a name="help-secure-analytical-workspaces-on-the-analytics-tab"></a><span data-ttu-id="18cc4-134">分析タブの分析ワークスペースのセキュリティを強化する</span><span class="sxs-lookup"><span data-stu-id="18cc4-134">Help secure analytical workspaces on the Analytics tab</span></span>
<span data-ttu-id="18cc4-135">分析ワークスペースはフォーム コントロールに表示される埋め込まれた Power BI レポートです。</span><span class="sxs-lookup"><span data-stu-id="18cc4-135">Analytical workspaces are embedded Power BI reports that are shown in a form control.</span></span> <span data-ttu-id="18cc4-136">次の手順を完了しない限り、ワークスペースにアクセスできるすべてのユーザーには **分析** タブが表示され、Power BI レポートにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="18cc4-136">Unless you complete the following procedure, anyone who has access to the workspace can see the **Analytics** tab and access the Power BI reports.</span></span>

1. <span data-ttu-id="18cc4-137">分析ワークスペースのメニュー項目を追加します。</span><span class="sxs-lookup"><span data-stu-id="18cc4-137">Add a menu item for the analytical workspace.</span></span>
2. <span data-ttu-id="18cc4-138">ユーザーがメニュー項目にアクセスできることを確認するために、フォームの初期化に **hasMenuItemAccess** アプリケーション プログラミング インターフェイス (API) が使用されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="18cc4-138">Verify that the form initialization uses the **hasMenuItemAccess** application programming interface (API) to verify that the user has access to the menu item.</span></span>

    ```xpp
    // Note: secure entry point into the Workspace's Analytics report
    if (Global::hasMenuItemAccess(menuItemDisplayStr(FMClerkWorkspace), MenuItemType::Display))
    {
        FMPBIWorkspaceController controller = new FMPBIWorkspaceController();
        PBIReportHelper::initializeReportControl('FMPBIWorkspaces', powerBIReportGroup);
    }
    ```

<span data-ttu-id="18cc4-139">上記のロジックは、Power BI ビューアー コントロールの初期化を阻止します。</span><span class="sxs-lookup"><span data-stu-id="18cc4-139">The preceding logic will prevent the Power BI Viewer control from being initialized.</span></span> <span data-ttu-id="18cc4-140">したがって、空のタブがページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="18cc4-140">Therefore, an empty tab will appear on the page.</span></span> <span data-ttu-id="18cc4-141">既定では、フレームワークは自動的に空のタブを非表示にします。</span><span class="sxs-lookup"><span data-stu-id="18cc4-141">By default, the framework automatically hides empty tabs.</span></span> <span data-ttu-id="18cc4-142">したがって、**分析** タブは非表示になっており、ユーザーが分析ワークスペースに関連付けられているメニュー項目へのアクセス権を持たない場合はアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="18cc4-142">Therefore, the **Analytics** tab is hidden and can't be access if the user doesn't have access to the menu item that is associated with the analytical workspace.</span></span>

### <a name="help-secure-analytical-reports"></a><span data-ttu-id="18cc4-143">分析レポートのセキュリティを強化する</span><span class="sxs-lookup"><span data-stu-id="18cc4-143">Help secure analytical reports</span></span>
<span data-ttu-id="18cc4-144">アプリケーションの埋め込み Power BI レポートは、メニュー項目を使用してセキュリティで保護されます。</span><span class="sxs-lookup"><span data-stu-id="18cc4-144">Embedded Power BI reports in the application are secured by using menu items.</span></span> <span data-ttu-id="18cc4-145">アプリケーションのメニュー項目を使用して Power BI レポートに直接アクセスを試みるユーザーに、エラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="18cc4-145">Users who try to access a Power BI report directly, by using a menu item in application, will receive an error.</span></span> <span data-ttu-id="18cc4-146">分析レポートのセキュリティを確保するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="18cc4-146">Follow these steps to help secure the analytical reports.</span></span>

1. <span data-ttu-id="18cc4-147">レポートまたは適切なタブのメニュー項目を追加します。既定では、その他のタブが選択されていない場合、レポートの最初のタブが表示されます。</span><span class="sxs-lookup"><span data-stu-id="18cc4-147">Add a menu item for the report or the appropriate tab. By default, the first tab of the report will be shown if no other tab is selected.</span></span>
2. <span data-ttu-id="18cc4-148">メニュー項目を **PowerBIEmbedded\_App** コンフィギュレーション キーにリンクします。</span><span class="sxs-lookup"><span data-stu-id="18cc4-148">Link the menu item to the **PowerBIEmbedded\_App** configuration key.</span></span>

    ![メニュー項目の PowerBIEmbedded_App コンフィギュレーション キーへのリンク](media/secure-workspace-key.png)

<span data-ttu-id="18cc4-150">このメニュー項目は、Power BI Embedded サービスの可用性に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="18cc4-150">The menu item is now associated with the availability of the Power BI Embedded service.</span></span> <span data-ttu-id="18cc4-151">サービスを使用できない場合は、アプリケーションからメニュー項目のリンクが削除されます。</span><span class="sxs-lookup"><span data-stu-id="18cc4-151">If the service is unavailable, the links for the menu items will be removed from the application.</span></span>

## <a name="help-secure-analytical-workspaces-and-reports-by-company"></a><span data-ttu-id="18cc4-152">会社ごとの分析ワークスペースおよびレポートのセキュリティを強化する</span><span class="sxs-lookup"><span data-stu-id="18cc4-152">Help secure analytical workspaces and reports by company</span></span>
<span data-ttu-id="18cc4-153">Power BI ワークスペースとレポートは会社が保護できます (たとえば、**DataAreaID** 値など)。</span><span class="sxs-lookup"><span data-stu-id="18cc4-153">Power BI workspaces and reports can be secured by company (for example, **DataAreaID** value).</span></span> <span data-ttu-id="18cc4-154">アプリケーション ソリューションは、分析ワークスペースとレポートで会社レベルのセキュリティのために、次の手順を適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="18cc4-154">Application solutions must apply the following steps for company-level security in analytical workspaces and reports.</span></span>

<span data-ttu-id="18cc4-155">このシナリオでは、Contoso USA の販売マネージャーが確認するワークスペースとレポートは、Contoso USA に関連するデータに限定されます。</span><span class="sxs-lookup"><span data-stu-id="18cc4-155">In this scenario, the workspaces and reports that the sales manager from Contoso USA sees are limited to data that is related to Contoso USA.</span></span> <span data-ttu-id="18cc4-156">レポート ビューアーは、会社のコンテキストが変更されない限り、他の会社に関連付けられたデータにアクセスできないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="18cc4-156">The report viewer must not have access to data that associated with any other company, unless the company context is changed.</span></span>

1. <span data-ttu-id="18cc4-157">Microsoft Visual Studio プロジェクト内のリソースをダブルクリックして、Power BI Desktop で分析レポートを開きます。</span><span class="sxs-lookup"><span data-stu-id="18cc4-157">Open the analytical report in Power BI Desktop by double-clicking the resource in a Microsoft Visual Studio project.</span></span>
2. <span data-ttu-id="18cc4-158">**モデリング** タブで、**ロールの管理** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="18cc4-158">On the **Modeling** tab, click **Manage Roles**.</span></span>
3. <span data-ttu-id="18cc4-159">**会社** フィールドを含むデータ モデル内の列に対して新しいロールを作成します。</span><span class="sxs-lookup"><span data-stu-id="18cc4-159">Create a new role against a column in the data model that contains the **Company** field.</span></span> <span data-ttu-id="18cc4-160">新しいロールに **CompanyFilter** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="18cc4-160">Name the new role **CompanyFilter**.</span></span> <span data-ttu-id="18cc4-161">会社によるアクセスを制限するために、データ モデルに **会社** フィールドが必要です。</span><span class="sxs-lookup"><span data-stu-id="18cc4-161">A **COMPANY** field must be present in the data model to restrict access by company.</span></span>

    ![新しいロールの作成](media/secure-workspace-filter.png)

4. <span data-ttu-id="18cc4-163">**テーブル フィルターの DAX 式** フィールドに、**\[COMPANY\]=username()** と入力します。</span><span class="sxs-lookup"><span data-stu-id="18cc4-163">In the **Table filter DAX expression** field, enter **\[COMPANY\]=username()**.</span></span>
5. <span data-ttu-id="18cc4-164">ルールが機能することを確認するには、**モデリング** タブで **ロールとして表示** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="18cc4-164">To make sure that the rules work, on the **Modeling** tab, click **View as Roles**.</span></span> <span data-ttu-id="18cc4-165">ダイアログ ボックスで、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="18cc4-165">In the dialog box, set the following fields:</span></span>

    1. <span data-ttu-id="18cc4-166">**なし** チェック ボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="18cc4-166">Clear the **None** check box.</span></span>
    2. <span data-ttu-id="18cc4-167">**その他のユーザー** チェック ボックスをオンにし、テキスト ボックスに **USMF** と入力します。</span><span class="sxs-lookup"><span data-stu-id="18cc4-167">Select the **Other user** check box, and then enter **USMF** in the text box.</span></span>
    3. <span data-ttu-id="18cc4-168">**CompanyFilter** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="18cc4-168">Select the **CompanyFilter** check box.</span></span>

<span data-ttu-id="18cc4-169">これでレポートに、USMF 企業を経営しているかのようなデータが表示されます。</span><span class="sxs-lookup"><span data-stu-id="18cc4-169">The reports will now show data as if you're running the USMF company.</span></span>
