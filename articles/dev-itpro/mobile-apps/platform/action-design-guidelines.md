---
title: アクション デザインのガイドライン
description: このトピックでは、モバイル アプリの設計に関する詳細な情報を示します。
author: makhabaz
manager: AnnBe
ms.date: 08/14/2017
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
ms.openlocfilehash: 8e60b77015a7ac84a01161b5786299426f9ca070
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537355"
---
# <a name="action-design-guidelines"></a><span data-ttu-id="8ae9b-103">アクション デザインのガイドライン</span><span class="sxs-lookup"><span data-stu-id="8ae9b-103">Action design guidelines</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8ae9b-104">アクションでユーザーはデータの作成、更新、または削除を行うことができ、そのデータ (*送信*、*確認*、および*転記*など) で業務プロセスを実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-104">Actions let users create, update, or delete data, and also run business processes on that data (such as *submit*, *confirm*, and *post*).</span></span> <span data-ttu-id="8ae9b-105">アクションを完了したユーザーは、アクションのデータを最初に提供します (アクションがデータ入力を受け入れる場合)。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-105">A user who completes an action first supplies the data for the action (if the action accepts data input).</span></span> <span data-ttu-id="8ae9b-106">ユーザーがデータの提供を完了すると、アクションは同様のアクションのキューに配置されます (これは *データ同期操作* と呼ばれることもあります)。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-106">When the user has finished supplying the data, the action is put into a queue of similar actions (which are sometimes referred to as *data sync operations*).</span></span> <span data-ttu-id="8ae9b-107">デバイスが接続されているまたはオンラインである場合は、キューがすぐに処理されます。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-107">If the device is connected/online, the queue is processed immediately.</span></span> <span data-ttu-id="8ae9b-108">それ以外の場合、次回デバイスが接続されたときに処理されます。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-108">Otherwise, it's processed the next time that the device is connected.</span></span> <span data-ttu-id="8ae9b-109">キューは非同期で処理され、データ同期中にエラーが発生しない限り、ユーザーの注意を必要としません。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-109">The queue is processed asynchronously and doesn’t require the user’s attention unless there is an error during data synchronization.</span></span> <span data-ttu-id="8ae9b-110">このタイプのエラーは、サーバー側のデータ入力規則が原因で発生します。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-110">Errors of this type can occur because of server-side data validation.</span></span> <span data-ttu-id="8ae9b-111">アクションは、タスク記録に似たサーバー側メカニズムによって強化されます。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-111">Actions are powered by a server-side mechanism that resembles Task recordings.</span></span> <span data-ttu-id="8ae9b-112">このメカニズムはアクションからユーザーの入力を抽出し、ユーザーが入力した入力値を使用してビジネス プロセス ステップをサーバー上で自動的に実行します。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-112">This mechanism extracts the user’s input from the action and then automatically runs the business process steps on the server by using the input values that the user supplied.</span></span> <span data-ttu-id="8ae9b-113">この仕組みは、自動的にフォームを開き、フォーム上のボタンをクリックし、ユーザーの入力をフォームのコントロールに入力します。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-113">The mechanism automatically opens forms, clicks buttons on the forms, and enters the user's input into controls on the forms.</span></span> <span data-ttu-id="8ae9b-114">サーバー上のフォームに対してアクションを再生するこのプロセスは、「ヘッドレス」フォームとは非同期で行われます。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-114">This process of playing back the action against the forms on the server occurs asynchronously, against “headless” forms.</span></span> <span data-ttu-id="8ae9b-115">モバイル アプリは、プロセスが完了するとユーザーに通知し、フォームに記録された情報、警告、またはエラー メッセージをユーザーに表示します。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-115">The mobile app informs the user when the process is completed, and shows the user any info, warning, or error messages that the forms logged.</span></span> <span data-ttu-id="8ae9b-116">アクションをデザインするときは、アクションがどのようなエンティティに関連付けられているかを最初に検討することが重要です。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-116">When you design an action, it’s important that you first consider what entity the action is related to.</span></span> <span data-ttu-id="8ae9b-117">現在のフレームワークでは、アクションでエンティティを 1 つだけ操作する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-117">In the current framework, an action must operate on only one entity.</span></span> <span data-ttu-id="8ae9b-118">アクションは同時に複数のエンティティを更新するべきではありません。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-118">An action should not update multiple entities at the same time.</span></span> <span data-ttu-id="8ae9b-119">たとえば、新しい販売注文を作成するアクションは、注文のヘッダーのみを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-119">For example, an action to create a new sales order should create only the header for the order.</span></span> <span data-ttu-id="8ae9b-120">明細行は別々のエンティティであるため、明細行を作成しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-120">It should not also try to create lines, because the lines are separate entities.</span></span> <span data-ttu-id="8ae9b-121">アクションを設計することを決定したときは、以下の質問を検討して、展開の方法を決定します。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-121">When you decide to design the action, consider the following questions to determine how to proceed.</span></span>

### <a name="how-do-i-design-an-action-that-enables-an-entity-to-be-created"></a><span data-ttu-id="8ae9b-122">エンティティが作成されるようにするアクションをどのように設計しますか。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-122">How do I design an action that enables an entity to be created?</span></span>

1.  <span data-ttu-id="8ae9b-123">エンティティのリスト ビュー ページを識別または作成します。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-123">Identify or create a list view page for the entity.</span></span>
2.  <span data-ttu-id="8ae9b-124">リスト ビュー ページに使用されるフォームに、新しいレコードをリストに追加するために使用できる**新規**ボタンが含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-124">Make sure that the form that is used for the list view page includes a **New** button that can be used to add new records to the list.</span></span>
3.  <span data-ttu-id="8ae9b-125">デザイナーを使用して、ページに新しいアクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-125">Use the designer to create a new action for the page.</span></span> <span data-ttu-id="8ae9b-126">アクションを作成するときは、不要なアクションを実行しないように注意します。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-126">While you're designing the action, be careful not to perform any unnecessary actions.</span></span> <span data-ttu-id="8ae9b-127">ユーザーが使用できるフィールドにのみデータを入力し、必要なボタンだけをクリックします (たとえば、**新規**ボタンおよび**保存**ボタン)。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-127">Enter data only in those fields that should be available to the user, and click only those buttons that are required (for example the **New** button and the **Save** button).</span></span>

### <a name="how-do-i-design-an-action-that-enables-an-entity-to-be-edited"></a><span data-ttu-id="8ae9b-128">エンティティが編集されるようにするアクションをどのように設計しますか。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-128">How do I design an action that enables an entity to be edited?</span></span>

1.  <span data-ttu-id="8ae9b-129">エンティティの詳細ビュー ページを識別または作成します。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-129">Identify or create a details view page for the entity.</span></span>
2.  <span data-ttu-id="8ae9b-130">詳細ビュー ページに使用されるフォームに、表示されているレコードを編集するために使用できる**編集**ボタンが含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-130">Make sure that the form that is used for the details view page includes an **Edit** button that can be used to edit the visible record.</span></span>
3.  <span data-ttu-id="8ae9b-131">詳細ビュー ページに使用されるフォームから、ユーザーがフィルター ウィンドウにフィルターを適用することで特定のレコードを開けることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-131">Make sure that the form that is used for the details view page lets users open a specific record by applying filters in the filter pane.</span></span>
4.  <span data-ttu-id="8ae9b-132">デザイナーを使用して、ページに新しいアクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-132">Use the designer to create a new action for the page.</span></span> <span data-ttu-id="8ae9b-133">アクションを作成するときは、不要なアクションを実行しないように注意します。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-133">While you're designing the action, be careful not to perform any unnecessary actions.</span></span> <span data-ttu-id="8ae9b-134">ユーザーが使用できるフィールドにのみデータを入力し、必要なボタンだけをクリックします (たとえば、**編集**ボタンおよび**保存**ボタン)。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-134">Enter data only in those fields that should be available to the user, and click only those buttons that are required (for example, the **Edit** button and the **Save** button).</span></span>

### <a name="how-do-i-design-an-action-that-enables-an-entity-to-be-deleted"></a><span data-ttu-id="8ae9b-135">エンティティが削除されるようにするアクションをどのように設計しますか。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-135">How do I design an action that enables an entity to be deleted?</span></span>

1.  <span data-ttu-id="8ae9b-136">エンティティの詳細ビュー ページを識別または作成します。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-136">Identify or create a details view page for the entity.</span></span>
2.  <span data-ttu-id="8ae9b-137">詳細ビュー ページに使用されるフォームに、表示されているレコードを削除するために使用できる**削除**ボタンが含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-137">Make sure that the form that is used for the details view page includes a **Delete** button that can be used to delete the visible record.</span></span>
3.  <span data-ttu-id="8ae9b-138">詳細ビュー ページに使用されるフォームから、ユーザーがフィルター ウィンドウにフィルターを適用することで特定のレコードを開けることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-138">Make sure that the form that is used for the details view page lets users open a specific record by applying filters in the filter pane.</span></span>
4.  <span data-ttu-id="8ae9b-139">デザイナーを使用してページの新しいアクションを作成し、アクションの設計プロセスの一部として **削除**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-139">Use the designer to create a new action for the page, and just click **Delete** as a part of the process of designing the action.</span></span>

### <a name="how-do-i-design-an-action-that-enables-a-business-action-to-be-performed-on-an-entity"></a><span data-ttu-id="8ae9b-140">エンティティで実行される事業活動を有効にするアクションをどのように設計しますか。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-140">How do I design an action that enables a business action to be performed on an entity?</span></span>

1.  <span data-ttu-id="8ae9b-141">エンティティの詳細ビュー ページを識別または作成します。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-141">Identify or create a details view page for the entity.</span></span>
2.  <span data-ttu-id="8ae9b-142">詳細ビュー ページに使用されるフォームに、表示されているレコードを削除するために使用できる**削除**ボタンが含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-142">Make sure that the form that is used for the details view page includes a **Delete** button that can be used to delete the visible record.</span></span>
3.  <span data-ttu-id="8ae9b-143">詳細ビュー ページに使用されるフォームから、ユーザーがフィルター ウィンドウにフィルターを適用することで特定のレコードを開けることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-143">Make sure that the form that is used for the details view page lets users open a specific record by applying filters in the filter pane.</span></span>
4.  <span data-ttu-id="8ae9b-144">デザイナーを使用してページの新しいアクションを作成し、ビジネス アクションに必要な手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-144">Use the designer to create a new action for the page, and just perform the steps that are required in the business action.</span></span> <span data-ttu-id="8ae9b-145">アクションの一部として、必ずしもフィールドにデータを入力する必要があるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-145">You don't necessarily have to enter data in fields as part of the action.</span></span> <span data-ttu-id="8ae9b-146">*送信*などのアクションについては、単に**送信**ボタン (および任意の確認書が表示されることを確認します) をクリックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-146">For an action such as *submit*, you just have to click the **Submit** button (and acknowledge any confirmations that appear).</span></span>

### <a name="how-do-i-design-an-action-that-enables-a-field-value-to-be-set-via-a-rich-lookup"></a><span data-ttu-id="8ae9b-147">豊富なルックアップを介して設定するフィールド値を有効にするアクションをどのように設計しますか。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-147">How do I design an action that enables a field value to be set via a rich lookup?</span></span>

<span data-ttu-id="8ae9b-148">モバイル アプリでのフィールドのルックアップには、Finance and Operations の高度なルックアップ動作との相関関係はありません。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-148">Lookups for fields in the mobile app don't have a correlation to the advanced lookup behaviors in Finance and Operations.</span></span> <span data-ttu-id="8ae9b-149">Finance and Operations にカスタム ルックアップがあるのか、単純なクエリを使用する自動ルックアップがあるのかに関係なく、モバイル アプリはユーザーに表示される UI を決定する必要があるときに既存のルックアップ コードを実行しません。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-149">Regardless of whether you have a custom lookup in Finance and Operations or an automatic lookup that uses a simple query, the mobile app doesn't run existing lookup code when it must determine which UI to show the user.</span></span> <span data-ttu-id="8ae9b-150">(ユーザーがアプリケーションを使用している間はオフラインになっている可能性があり、アクションが同期されるまでサーバー側のコードは実行されないことに注意してください。) ただし、アクションからのデータを同期させるので、値がモバイル バック エンドによって設定される場合、*変更*などのルックアップ/コントロールの上書きは実行されます。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-150">(Remember that the user might be offline while he or she is using the app, and server-side code isn’t run until the action is synchronized.) However, lookup/control overrides such as *modified* are run when the value is set by the mobile back end as it synchronizes the data from the action.</span></span> <span data-ttu-id="8ae9b-151">モバイル アプリは、アクションのフィールドがフォームのルックアップ フィールドから選択されたことを検出すると、デバイス ネイティブ コンボ ボックス / リスト選択コントロールを表示して、そのルックアップ フィールドのサポート テーブルを直接照会して項目を実装します。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-151">When the mobile app detects that a field on an action was selected from a lookup field on a form, it shows a device-native combo box/list picker control, and populates the items by directly querying the backing table of that lookup field.</span></span> <span data-ttu-id="8ae9b-152">リスト内の項目は、そのテーブルのレコードの TitleField のユーザー データを示します。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-152">The items in the list show the user data from the TitleField for records in that table.</span></span> <span data-ttu-id="8ae9b-153">アクションに豊富なルックアップ エクスペリエンスを追加するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-153">Follow these steps to add the rich lookup experience to your action.</span></span> <span data-ttu-id="8ae9b-154">このルックアップ エクスペリエンスには、フルページの複数列のルックアップ セレクターがあり、オフライン検索が可能です。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-154">This lookup experience includes a full-page multi-column lookup selector that has offline search.</span></span>

1.  <span data-ttu-id="8ae9b-155">ルックアップの背後にあるエンティティの詳細ビュー ページを識別または作成します。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-155">Identify or create a list view page for the entity behind the lookup.</span></span> <span data-ttu-id="8ae9b-156">既に作成済みの既存のリスト ビュー ページを再利用することができます。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-156">You can reuse existing list view pages that you've already created.</span></span>
2.  <span data-ttu-id="8ae9b-157">アクションのデザインが終了した後、フィールドを選択して豊富なルックアップ機能を追加し、**プロパティ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-157">After you've finished designing the action, select the field to add rich lookup functionality to, and then click **Properties**.</span></span>
3.  <span data-ttu-id="8ae9b-158">**コントロールのプロパティ** ダイアログ ボックスで、手順 1 で指定または作成したリスト ビュー ページを選択し、その他の関連するプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-158">In the **Control properties** dialog box, select the list view page that you identified or created in step 1, and set the other related properties.</span></span> 

![コントロール プロパティの設定](media/lookupdesigner.png)

4.  <span data-ttu-id="8ae9b-160">アクションに変更内容を保存して公開します。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-160">Save and publish your changes to the action.</span></span>

<span data-ttu-id="8ae9b-161">既存のリスト ビュー ページのプロパティが表示されていない、または**コントロールのプロパティ** ダイアログ ボックスにアクセスできない場合、Finance and Operations のより古いビルドを使用している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-161">If you don't see the property for the existing list view page or can't access the **Control properties** dialog box when you're designing your action, you might be using an older build of Finance and Operations.</span></span> <span data-ttu-id="8ae9b-162">この場合、ビジネス ロジック ファイルを使用して、豊富なルックアップ機能を追加できます。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-162">In this case, you can still add rich lookup functionality by using a business logic file.</span></span>

    function main(metadataService, dataService, cacheService, $q) { 
        return { 
            appInit: function (appMetadata) { 
                metadataService.configureLookup(
                    // specify the name of the Action to add the lookup to
                    'Add-Reservation',                      
                    // specify the name of the Action’s field to add the lookup to
                    'FMRental_Customer',                    
                    { 
                        // specify the name of the Page for the Entity for the lookup
                        lookupPage: 'All-Customers',          
                        // specify the Page’s field which contains the value to set on the lookup
                     // this value should be the same value you can type into the field on the Form
                        valueField: 'FMCustomer_RecId',        
                        // specify the Page’s field which contains the value to display to the user
                        // this value is only used for display. The value field is passed to the Form
                        displayField: 'FMCustomer_FullName',  
                        // set this to true to enable the rich lookup
                        showLookupPage: true                  
                    }
                );
            }, 
        }; 
    }

### <a name="how-do-i-prevent-an-action-from-appearing-in-the-list-of-actions-for-a-page"></a><span data-ttu-id="8ae9b-163">アクションを、ページのアクションの一覧に表示されないようにするにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-163">How do I prevent an action from appearing in the list of actions for a page?</span></span>

<span data-ttu-id="8ae9b-164">ページのアクション一覧にアクションが表示されないようにするには、ビジネス ロジックの **appInit()** セクションから次のコードを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-164">To prevent an action from appearing in the list of actions for any page, call the following code from the **appInit()** section of your business logic.</span></span> <span data-ttu-id="8ae9b-165">このコードでは、**アクション名**はアクションの名前です (デザイナーの**アクション名**フィールドで指定したとおり)。</span><span class="sxs-lookup"><span data-stu-id="8ae9b-165">In this code, **action-name** is the name of your action (as specified in the **Action name** field in the designer).</span></span>

    function main(metadataService, dataService, cacheService, $q) { 
        return { 
            appInit: function (appMetadata) { 
                metadataService.configureAction('action-name', { visible: false });
            }, 
        }; 
    }
