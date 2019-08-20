---
title: ページ デザインのガイドライン
description: このトピックでは、モバイル アプリの設計に関する詳細な情報を示します。
author: makhabaz
manager: AnnBe
ms.date: 04/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 255544
ms.assetid: ''
ms.search.region: Global
ms.author: makhabaz
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Platform update 3
ms.openlocfilehash: f21735406a6893aa60c75a395ee47d545965a984
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851463"
---
# <a name="page-design-guidelines"></a><span data-ttu-id="fde79-103">ページ デザインのガイドライン</span><span class="sxs-lookup"><span data-stu-id="fde79-103">Page design guidelines</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fde79-104">デザイナーを使用してページとアクションを構築する前に、構築するモバイル ワークスペースの全体的なデザインを計画することが重要です。</span><span class="sxs-lookup"><span data-stu-id="fde79-104">Before you begin to use the designer to build pages and actions, it’s important that you plan the overall design of the mobile workspace that you want to build.</span></span> <span data-ttu-id="fde79-105">モバイル ワークスペースでの使用を予定しているエンティティを中心にして設計の方向を正しく位置付けることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="fde79-105">We recommend that you orient your design around the entities that you plan to use in the mobile workspace.</span></span> <span data-ttu-id="fde79-106">初めに使用希望のフォームを検討しないでください。</span><span class="sxs-lookup"><span data-stu-id="fde79-106">Don't begin by thinking about the forms that you want to use.</span></span> <span data-ttu-id="fde79-107">モバイル アプリの観点からは、フォームは単なるデータを取得するためのメカニズムであり、フォームのランタイム UI 動作はモバイル アプリに適用できません。</span><span class="sxs-lookup"><span data-stu-id="fde79-107">From the perspective of the mobile app, the forms are just a mechanism for retrieving data, and the run-time UI behavior of a form isn't applicable to the mobile app.</span></span> <span data-ttu-id="fde79-108">したがって、エンティティとエンティティ間のリレーションシップを最初に特定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fde79-108">Therefore, you should first identify your entities and the relationships between them.</span></span> <span data-ttu-id="fde79-109">各エンティティについて、以下の質問はフォームやページをどうデザインすべきかを決定するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="fde79-109">For each entity, the following questions will help you decide how you should design your forms and pages.</span></span>

### <a name="how-do-i-create-a-list-view-for-an-entity-in-the-mobile-app"></a><span data-ttu-id="fde79-110">モバイル アプリでエンティティのリスト ビューをどのように作成しますか。</span><span class="sxs-lookup"><span data-stu-id="fde79-110">How do I create a list view for an entity in the mobile app?</span></span>

1.  <span data-ttu-id="fde79-111">エンティティのグリッドを含む Finance and Operations のフォームを識別または作成します。</span><span class="sxs-lookup"><span data-stu-id="fde79-111">Identify or create a form in Finance and Operations that contains a grid for the entity.</span></span>
2.  <span data-ttu-id="fde79-112">グリッドがエンティティを表すテーブルにバインドされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fde79-112">Make sure that the grid is bound to the table that represents the entity.</span></span>
3.  <span data-ttu-id="fde79-113">フォームにルート移動可能なメニュー項目があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fde79-113">Make sure that the form has a menu item that is root-navigable.</span></span>
4.  <span data-ttu-id="fde79-114">フォームがメニュー項目のパラメーターを含む URL 経由で直接開くことができることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fde79-114">Make sure that the form can be opened directly via a URL that includes the menu item parameter.</span></span>
5.  <span data-ttu-id="fde79-115">フィルター ウィンドウで、目的のフィールドに基づいてグリッドをフィルター処理できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fde79-115">Make sure that the filter pane enables the grid to be filtered based on the desired fields.</span></span>
6.  <span data-ttu-id="fde79-116">デザイナーで、エンティティのページを作成します。</span><span class="sxs-lookup"><span data-stu-id="fde79-116">In the designer, create a page for the entity.</span></span>
7.  <span data-ttu-id="fde79-117">デザイナーで、ページ上に一覧のみ配置します。</span><span class="sxs-lookup"><span data-stu-id="fde79-117">In the designer, put only a list on the page.</span></span>
8.  <span data-ttu-id="fde79-118">デザイナーで、一覧にある目的のフィールドをページに配置します。</span><span class="sxs-lookup"><span data-stu-id="fde79-118">In the designer, put the desired fields in the list on the page.</span></span>

### <a name="what-if-i-dont-want-a-list-view-for-this-entity"></a><span data-ttu-id="fde79-119">このエンティティの一覧表示が必要ない場合はどうしますか ?</span><span class="sxs-lookup"><span data-stu-id="fde79-119">What if I don’t want a list view for this entity?</span></span>

<span data-ttu-id="fde79-120">エンティティの詳細ビューだけを使用する場合は、エンティティは、特定のコンテキスト (特定のユーザーや特定の会社など) において単一のエンティティである可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fde79-120">If you want just a details view for an entity, it's likely that the entity is a singleton for a given context (such as a given user or a given company).</span></span> <span data-ttu-id="fde79-121">このパターンは、たとえば、セルフサービス ワークスペース内の従業員自身のプロファイルの詳細ビューまたは現在のセッションで使用される会社コンテキストの詳細ビューに適用されます。</span><span class="sxs-lookup"><span data-stu-id="fde79-121">This pattern applies, for example, to a details view for an employee’s own profile in a self-service workspace or a details view for the company context that is used for the current session.</span></span> <span data-ttu-id="fde79-122">詳細ビューのページを作成するためのガイドラインを参照してください。</span><span class="sxs-lookup"><span data-stu-id="fde79-122">See the guidelines for creating a page for a details view.</span></span>

### <a name="how-do-i-create-a-details-view-for-an-entity-in-the-mobile-app"></a><span data-ttu-id="fde79-123">モバイル アプリでエンティティの詳細ビューをどのように作成しますか。</span><span class="sxs-lookup"><span data-stu-id="fde79-123">How do I create a details view for an entity in the mobile app?</span></span>

1.  <span data-ttu-id="fde79-124">このエンティティの詳細ビューを含む Finance and Operations のフォームを識別または作成します。</span><span class="sxs-lookup"><span data-stu-id="fde79-124">Identify or create a form in Finance and Operations that contains the details view for this entity.</span></span>
2.  <span data-ttu-id="fde79-125">フォームのマスター ルート データ ソースがエンティティを表すテーブルにバインドされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fde79-125">Make sure that the Master Root Data Source on the form is bound to the table that represents the entity.</span></span>
3.  <span data-ttu-id="fde79-126">フォームにルート移動可能なメニュー項目があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fde79-126">Make sure that the form has a menu item that is root-navigable.</span></span>
4.  <span data-ttu-id="fde79-127">フォームがメニュー項目のパラメーターを含む URL 経由で直接開くことができることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fde79-127">Make sure that the form can be opened directly via a URL that includes the menu item parameter.</span></span>
5.  <span data-ttu-id="fde79-128">デザイナーで、エンティティのページを作成します。</span><span class="sxs-lookup"><span data-stu-id="fde79-128">In the designer, create a page for the entity.</span></span>
6.  <span data-ttu-id="fde79-129">デザイナーで、目的のフィールドをページに配置します。</span><span class="sxs-lookup"><span data-stu-id="fde79-129">In the designer, put the desired fields on the page.</span></span>

### <a name="how-do-i-create-list-to-details-navigation-for-an-entity-in-the-mobile-app"></a><span data-ttu-id="fde79-130">モバイル アプリでエンティティ用リストから詳細へのナビゲーションをどのように作成しますか。</span><span class="sxs-lookup"><span data-stu-id="fde79-130">How do I create list-to-details navigation for an entity in the mobile app?</span></span>

1.  <span data-ttu-id="fde79-131">デザイナーを使用してエンティティのリスト ビュー ページと詳細ビュー ページの両方を作成したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="fde79-131">Make sure that you've created both a list view page and a details view page for the entity by using the designer.</span></span>
2.  <span data-ttu-id="fde79-132">リスト ビューのエンティティが詳細ビューのエンティティと同じであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fde79-132">Make sure that the entity for the list view is the same as the entity for the details view.</span></span> <span data-ttu-id="fde79-133">つまり、リスト ビューに使用されるフォームのグリッドにバインドされているテーブルは、詳細表示に使用されるフォームでマスター ルート データ ソースとなっている同じテーブルである必要があります。</span><span class="sxs-lookup"><span data-stu-id="fde79-133">In other words, the table that is bound to the grid on the form that is used for the list view must be the same table that is the Master Root Data Source on the form that is used for the details view.</span></span>
3.  <span data-ttu-id="fde79-134">詳細ビューで使用されるフォームが、フィルター ウィンドウを使用して固有のキー フィールドでフィルターできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fde79-134">Make sure that the form that is used for the details view can be filtered on a unique key field by using the filter pane.</span></span>
4.  <span data-ttu-id="fde79-135">デザイナーで、リスト ビュー ページが詳細表示ページにリンクされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fde79-135">In the designer, make sure that the list view page is linked to the details view page.</span></span> <span data-ttu-id="fde79-136">リストをクリックしてプロパティを開き、ルックアップを使用して詳細表示ページを設定します。</span><span class="sxs-lookup"><span data-stu-id="fde79-136">Click the list, open the properties, and then set the details view page by using the lookup.</span></span> 

![詳細ビュー ページへのリスト ビュー ページのリンク](media/listtodetailsdesigner.png)

### <a name="how-do-i-add-a-reference-field-that-enables-navigation-to-a-related-entity"></a><span data-ttu-id="fde79-138">ナビゲーションを有効にする参照フィールドを関連するエンティティに追加する方法はありますか。</span><span class="sxs-lookup"><span data-stu-id="fde79-138">How do I add a reference field that enables navigation to a related entity?</span></span>

1.  <span data-ttu-id="fde79-139">参照を含むエンティティに対して、リスト ビュー ページまたは詳細ビュー ページのいずれかが存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="fde79-139">Make sure that either a list view page or a details view page exists for the entity that contains the reference.</span></span>
2.  <span data-ttu-id="fde79-140">ページに参照されているエンティティから参照フィールドが含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fde79-140">Make sure that the page contains the reference field from the entity that is being referenced.</span></span>
3.  <span data-ttu-id="fde79-141">参照先のフィールドが参照先のエンティティのデータ ソースにバインドされており、参照先のエンティティが参照を含むエンティティのデータ ソースに*外部結合*(1-0..1) または*内部結合*(1-1) されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fde79-141">Make sure that the referenced field is bound to the referenced entity’s data source, and that the referenced entity is *outer joined* (1-0..1) or *inner joined* (1-1) to the data source for the entity that contains the reference.</span></span> <span data-ttu-id="fde79-142">たとえば、次の図では、FMRental は参照を含むエンティティで、FMVehicle は参照されたエンティティです。</span><span class="sxs-lookup"><span data-stu-id="fde79-142">For example, in the following illustration, FMRental is the entity that contains the reference, and FMVehicle is the referenced entity.</span></span>

![参照フィールドを参照されるエンティティのデータ ソースにバインドする](media/relatedentityform.png)

4.  <span data-ttu-id="fde79-144">参照されているエンティティに対して個別の詳細ビュー ページを作成したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="fde79-144">Make sure that you've created a separate details view page for the entity that is being referenced.</span></span>
5.  <span data-ttu-id="fde79-145">参照フィールドがページに追加されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="fde79-145">Make sure that the reference field has been added to the page.</span></span>
6.  <span data-ttu-id="fde79-146">デザイナーで、参照フィールドが参照されているエンティティの詳細表示にリンクされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fde79-146">In the designer, make sure that the reference field has been linked to the details view for the referenced entity.</span></span> <span data-ttu-id="fde79-147">たとえば、次の図では、車両詳細は参照されたエンティティの詳細ビュー ページです。</span><span class="sxs-lookup"><span data-stu-id="fde79-147">For example, in the following illustration, Vehicle-details is the details view page for the referenced entity.</span></span>

![参照フィールドの参照先のエンティティの詳細ビューへのリンク](media/referencepagedesigner.png)

### <a name="how-do-i-add-a-list-that-contains-items-from-a-related-entity-to-a-details-view-page"></a><span data-ttu-id="fde79-149">関連するエンティティからの品目を含む一覧を、詳細ビュー ページに追加する方法はありますか。</span><span class="sxs-lookup"><span data-stu-id="fde79-149">How do I add a list that contains items from a related entity to a details view page?</span></span>

###### <a name="how-do-i-make-the-list-show-up-in-line-in-the-details-view"></a><span data-ttu-id="fde79-150">詳細ビューでインラインを表示できるようするにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="fde79-150">How do I make the list show up in-line in the details view?</span></span>

1.  <span data-ttu-id="fde79-151">エンティティの詳細ビューを含む Finance and Operations のフォームを識別または作成し、フォームが「モバイル アプリケーションのエンティティの詳細ビューを作成する方法」のガイドラインに従っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fde79-151">Identify or create a form in Finance and Operations that contains the details view for the entity, and make sure that the form adheres to the guidelines in the "How do I create a details view for an entity in the mobile app" section.</span></span>
2.  <span data-ttu-id="fde79-152">フォームが関連するエンティティを表すテーブルにバインドされているグリッドを含むことを確認します。</span><span class="sxs-lookup"><span data-stu-id="fde79-152">Make sure that the form contains a grid that is bound to the table that represents the related entity.</span></span>
3.  <span data-ttu-id="fde79-153">関連するエンティティのテーブルが参照を含むエンティティのテーブルに*アクティブに結合*されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fde79-153">Make sure that the table for the related entity is *active joined* to the table for the entity that contains the reference.</span></span>
4.  <span data-ttu-id="fde79-154">エンティティの目的のフィールドを含む詳細ビュー ページを作成します。また、関連エンティティの希望のフィールドを持つリストも含まれます。</span><span class="sxs-lookup"><span data-stu-id="fde79-154">Create a details view page that contains the desired fields for the entity, and that also contains a list that has the desired fields from the related entity.</span></span>

###### <a name="how-do-i-make-the-list-accessible-from-a-link-in-the-details-view-instead-of-in-line"></a><span data-ttu-id="fde79-155">詳細ビュー (インラインではなく) のリンクからリストにアクセスできるようするにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="fde79-155">How do I make the list accessible from a link in the details view (instead of in-line)?</span></span>

1.  <span data-ttu-id="fde79-156">エンティティの詳細ビューを含む Finance and Operations のフォームを識別または作成し、フォームが「モバイル アプリケーションのエンティティの詳細ビューを作成する方法」のガイドラインに従っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fde79-156">Identify or create a form in Finance and Operations that contains the details view for the entity, and make sure that the form adheres to the guidelines in the "How do I create a details view for an entity in the mobile app" section.</span></span>
2.  <span data-ttu-id="fde79-157">フォームが関連するエンティティを表すテーブルにバインドされているグリッドを含むことを確認します。</span><span class="sxs-lookup"><span data-stu-id="fde79-157">Make sure that the form contains a grid that is bound to the table that represents the related entity.</span></span>
3.  <span data-ttu-id="fde79-158">関連するエンティティのテーブルが参照を含むエンティティのテーブルに*アクティブに結合*されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fde79-158">Make sure that the table for the related entity is *active joined* to the table for the entity that contains the reference.</span></span>
4.  <span data-ttu-id="fde79-159">フォームを使用して、エンティティの目的のフィールドを含む詳細ビュー ページを作成します。</span><span class="sxs-lookup"><span data-stu-id="fde79-159">Use the form to create a details view page that contains the desired fields for the entity.</span></span>
5.  <span data-ttu-id="fde79-160">同じフォームを使用して、関連するエンティティから目的のフィールドを持つリストのみを含む別のリスト ビュー ページを作成します。</span><span class="sxs-lookup"><span data-stu-id="fde79-160">Use the same form to create a separate list view page that contains only a list that has the desired fields from the related entity.</span></span>
6.  <span data-ttu-id="fde79-161">詳細表示ページで、リスト表示ページにリンクする PageLinkControl を追加します。</span><span class="sxs-lookup"><span data-stu-id="fde79-161">On the details view page, add a PageLinkControl that links to the list view page.</span></span> <span data-ttu-id="fde79-162">現在、ビジネス ロジックを使用して PageLinkControl を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fde79-162">Currently, you must use business logic to add the PageLinkControl.</span></span> <span data-ttu-id="fde79-163">次の例は、Fleet Management が使用するコードを示しています。</span><span class="sxs-lookup"><span data-stu-id="fde79-163">The following example show the code that Fleet Management uses.</span></span>

        function main(metadataService, dataService, cacheService, $q) { 
            return { 
                appInit: function (appMetadata) { 
                    metadataService.addLink( 
                        'Customer-details', // the Page to add the link to 
                        'Customer-rentals', // the Page the link goes to 
                        'cust-rentals-nav-control', // unique name for the control 
                        'Rentals', // text to display for the link in the UI 
                        true, // show/hide the count for items on the linked page 
                        ); 
                }, 
            }; 
        }

###### <a name="how-do-i-read-data-from-a-hidden-page"></a><span data-ttu-id="fde79-164">非表示ページからデータを読み取るにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="fde79-164">How do I read data from a hidden page?</span></span>

1.  <span data-ttu-id="fde79-165">希望するデータでコントロールを含むページを識別または作成します。</span><span class="sxs-lookup"><span data-stu-id="fde79-165">Identify or create a page that contains the controls with the data that you want.</span></span>
2.  <span data-ttu-id="fde79-166">次のコード例をご覧ください。ナビゲーション メニューからページを非表示にし、提供される API を使用してページ上のデータにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="fde79-166">Refer to the following code example, which hides the page from the navigation menus, and accesses data on the page using the provided APIs.</span></span> <span data-ttu-id="fde79-167">「My-Hidden-Page」および「My-Field-Id」は、それぞれページおよびコントロールの名前であり、デザイナーで対応するページを表示するときに確認できることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="fde79-167">Note that 'My-Hidden-Page' and 'My-Field-Id' are the names of the page and control, respectively, and can be found when viewing the corresponding page in the designer.</span></span>

        function main(metadataService, dataService, cacheService, $q) {
            myField1Value = ''; // This variable will be populated in appInit, and can then be used elsewhere in the business logic. 
            return { 
                appInit: function (appMetadata) { 
                    var myHiddenPage = metadataService.findPage('My-Hidden-Page');
                    if(myHiddenPage) {
                        var dataPromise = dataService.getPageData(myHiddenPage.Id,'','',0);
                        dataPromise.then(function (result) {
                            var myField1Id = metadataService.findControl(myHiddenPage, 'My-Field-1').Id;
                            myField1Value = result.data[myField1Id];
                        }
                    }
            }; 
        }
        
### <a name="how-do-i-adjust-the-number-of-records-returned-in-a-list-page-using-list-fetch-size"></a><span data-ttu-id="fde79-168">リスト フェッチ サイズを使用して、リスト ページで返されるレコードの数を調整する方法はありますか。</span><span class="sxs-lookup"><span data-stu-id="fde79-168">How do I adjust the number of records returned in a list page using list fetch size?</span></span>

<span data-ttu-id="fde79-169">リストページで返されるレコードの数は、**List fetch size** 値によって制御されます。</span><span class="sxs-lookup"><span data-stu-id="fde79-169">The number of records returned in a list page is controlled by the **List fetch size** value.</span></span> <span data-ttu-id="fde79-170">既定は 50 レコードです。</span><span class="sxs-lookup"><span data-stu-id="fde79-170">The default is 50 records.</span></span> <span data-ttu-id="fde79-171">**リスト フェッチ サイズ** は、最初に読み込まれたときにページにより返されたレコードの最大数と、検索を使用して特定のレコード セットが検索されたときに返されたレコードの最大数を示します。</span><span class="sxs-lookup"><span data-stu-id="fde79-171">The **List fetch size** indicates the maximum number of records returned by a page when it first loads, and the maximum number of records returned  when search is used to find a specific set of records.</span></span> <span data-ttu-id="fde79-172">値を大きくしすぎないように注意が必要です。ユーザー エクスペリエンスに悪影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fde79-172">Be careful not to make the value too large or it may negatively affect the user experience.</span></span>

1. <span data-ttu-id="fde79-173">モバイル アプリ デザイナーで、グリッドを含むページを追加し、グリッドからいくつかのフィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="fde79-173">In the Mobile App designer,add a page containing a grid and select some fields from the grid.</span></span>
2. <span data-ttu-id="fde79-174">**グリッド** ノードをクリックし、**プロパティ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fde79-174">Click the **Grid** node and then click **Properties**.</span></span>
3. <span data-ttu-id="fde79-175">**コントロールのプロパティ** ダイアログ ボックスには 50 件のレコードの既定のフェッチ サイズが表示されます。</span><span class="sxs-lookup"><span data-stu-id="fde79-175">The **Control properties** dialog box will contain a default fetch size of 50 records.</span></span>
4. <span data-ttu-id="fde79-176">必要に応じて、フェッチ サイズを調整します。</span><span class="sxs-lookup"><span data-stu-id="fde79-176">Adjust the fetch size as needed.</span></span>
