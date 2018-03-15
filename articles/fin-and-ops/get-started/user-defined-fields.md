---
title: "カスタム フィールド"
description: "このトピックでは、どのように Microsoft Dynamics 365 for Finance and Operations で、一部のユーザーがアプリケーションをビジネスに合わせて調整するためのカスタム フィールドを作成できるかを示します。"
author: jasongre
manager: AnnBe
ms.date: 01/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SysCustomFieldManageFields
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: Platform update 13
ms.translationtype: HT
ms.sourcegitcommit: ad59346f88b7a5984e16418e2aade7ccaedf180b
ms.openlocfilehash: 142c66c189d6401cfb3db128e45fea6c071e99bf
ms.contentlocale: ja-jp
ms.lasthandoff: 02/28/2018

---

# <a name="custom-fields"></a><span data-ttu-id="4c956-103">カスタム フィールド</span><span class="sxs-lookup"><span data-stu-id="4c956-103">Custom fields</span></span>

[!include[banner](../includes/banner.md)] 

[!include[banner](../includes/pre-release.md)] 

<span data-ttu-id="4c956-104">Microsoft Dynamics 365 for Finance and Operations、Enterprise edition が、広範囲なビジネス プロセスを管理しすぐに使えるフィールドの広範なセットを作成する間、システムで追加情報を追跡する会社がたびたび必要です。</span><span class="sxs-lookup"><span data-stu-id="4c956-104">While Microsoft Dynamics 365 for Finance and Operations, Enterprise edition provides an extensive set of fields out-of-the-box for managing a broad range of business processes, sometimes there is a need for a company to track additional information in the system.</span></span> <span data-ttu-id="4c956-105">このニーズに合わせて、Finance and Operations は、機能へのアクセス許可を提供された自社に合うアプリケーションを調整するカスタム フィールドを作成できます。</span><span class="sxs-lookup"><span data-stu-id="4c956-105">To accommodate this need, Finance and Operations allows you to create custom fields to tailor the application to fit your business, provided you have permissions to the feature.</span></span>

<span data-ttu-id="4c956-106">このビデオでは、ページにカスタム フィールドを追加するのがどれほど簡単か示します。</span><span class="sxs-lookup"><span data-stu-id="4c956-106">This video shows how easy it is to add a custom field to a page.</span></span>


> [!Video https://www.youtube.com/embed/gWSGZI9Vtnc]

## <a name="creating-custom-fields"></a><span data-ttu-id="4c956-107">カスタム フィールドを作成</span><span class="sxs-lookup"><span data-stu-id="4c956-107">Creating custom fields</span></span>
<span data-ttu-id="4c956-108">アプリケーションで追跡するには追加情報を識別した後、適切なテーブルでカスタム フィールドを作成し、ページに新しいフィールドを公開します。</span><span class="sxs-lookup"><span data-stu-id="4c956-108">After you’ve identified additional information that you would like to track in the application, you can create the custom field on the appropriate table and expose that new field on a page.</span></span>   

<span data-ttu-id="4c956-109">次の手順で、カスタム フィールドの作成とフォーム上のフィールド配置のプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="4c956-109">The following steps describe the process for creating a custom field and placing that field on a form.</span></span>  

1.   <span data-ttu-id="4c956-110">新しいフィールドを必要とするフォームへ移動します。</span><span class="sxs-lookup"><span data-stu-id="4c956-110">Navigate to the form where the new field is needed.</span></span> 
2.   <span data-ttu-id="4c956-111">最終目標は、フォーム上のカスタム フィールドを公開することなので、カスタム フィールドを作成するためのエントリ ポイントは、個人用設定のエクスペリエンス内に存在します。</span><span class="sxs-lookup"><span data-stu-id="4c956-111">Because the end goal is to expose the custom field on a form, the entry point for creating custom fields exists inside the personalization experience.</span></span> <span data-ttu-id="4c956-112">個人用設定のツールバーを開くには、[**オプション**] を選択し、そして [**このフォームをカスタマイズ**] を選びます。</span><span class="sxs-lookup"><span data-stu-id="4c956-112">Open the personalization toolbar by selecting **Options**, and then **Personalize this form**.</span></span> 
3.   <span data-ttu-id="4c956-113">[**挿入**] をクリックし、次に [**フィールド**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c956-113">Click **Insert** and then **Field**.</span></span>  
4.   <span data-ttu-id="4c956-114">新しいフィールドを公開するフォームの領域を選択します。</span><span class="sxs-lookup"><span data-stu-id="4c956-114">Select the region of the form where you want to expose the new field.</span></span> <span data-ttu-id="4c956-115">選択した後、[**フィールドを挿入**] ダイアログ ボックスで、選択したフォームの領域を挿入する既存のフィールドの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4c956-115">After selection, the **Insert fields** dialog box will display a list of existing fields that can be inserted into the selected region of the form.</span></span>  
5.   <span data-ttu-id="4c956-116">興味のあるフィールドが一覧に存在しないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="4c956-116">Ensure that the field you are interested in does not already exist in the list.</span></span> <span data-ttu-id="4c956-117">その場合は、単に一覧のフィールドを選択し、[**挿入**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c956-117">If it does, you can simply select that field in the list and click **Insert**.</span></span>   
6.   <span data-ttu-id="4c956-118">カスタム フィールドを作成するプロセスを開始する一覧の上にある [**新しいフィールドを作成**] ボタンをクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="4c956-118">Click the **Create new field** button above the list to initiate the process of creating a custom field.</span></span> <span data-ttu-id="4c956-119">これで [**新しいフィールドを作成**] ダイアログ ボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="4c956-119">This will open the **Create new field** dialog box.</span></span> 

     <span data-ttu-id="4c956-120">[**新しいフィールドを作成**] ボタンが表示されない場合、あなたはこの機能を使用するための必要な権限を持っていません。</span><span class="sxs-lookup"><span data-stu-id="4c956-120">If you do not see the **Create new field** button, you do not have the necessary permissions to use this feature.</span></span>  
     
7.   <span data-ttu-id="4c956-121">[**新しいフィールドを作成**] ダイアログ ボックスで、次の情報を入力してください。</span><span class="sxs-lookup"><span data-stu-id="4c956-121">In the **Create new field** dialog box, enter the following information.</span></span>
     1.   <span data-ttu-id="4c956-122">このフィールドを追加する必要があるデータベース テーブルを選択します。</span><span class="sxs-lookup"><span data-stu-id="4c956-122">Select the database table where this field should be added.</span></span> <span data-ttu-id="4c956-123">カスタム フィールドをサポートするテーブルのみ、ドロップダウン リストに表示されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="4c956-123">Note that only tables that support custom fields will appear in the drop-down list.</span></span> <span data-ttu-id="4c956-124">サポートされているテーブルの技術上の詳細については、以下のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4c956-124">See the section below for technical details on supported tables.</span></span>  
     2.   <span data-ttu-id="4c956-125">新しいフィールドのデータ タイプを選択してください。</span><span class="sxs-lookup"><span data-stu-id="4c956-125">Select the data type for the new field.</span></span> <span data-ttu-id="4c956-126">使用可能なデータ タイプは、チェック ボックス、日付、日時、10 進数、番号、ピッキングリスト、およびテキストです。</span><span class="sxs-lookup"><span data-stu-id="4c956-126">The available data types are checkbox, date, date time, decimal, number, picklist, and text.</span></span>   
          - <span data-ttu-id="4c956-127">テキストのデータ タイプを選択する場合は、このフィールドに入力できるテキストの最長も指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="4c956-127">If you choose the text data type, you can also specify the maximum length of the text that can be entered in this field.</span></span> 
          - <span data-ttu-id="4c956-128">ピッキングリストのデータ タイプを選択する場合は、フィールドの有効な値のセットを選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="4c956-128">If you choose the picklist data type, you can also select the set of valid values for the field.</span></span>  
     3.   <span data-ttu-id="4c956-129">フィールドの名前、ラベル、およびヘルプ テキストを指定してください。</span><span class="sxs-lookup"><span data-stu-id="4c956-129">Provide a name, label, and help text for the field.</span></span> <span data-ttu-id="4c956-130">名前はデータベースの現物フィールド名に対応しています。一方、ラベルとヘルプ テキストはユーザー インターフェイスでこのフィールドを表すために使用されるテキストです。</span><span class="sxs-lookup"><span data-stu-id="4c956-130">The name corresponds to the physical field name in the database, whereas the label and help text are the text used to represent this field in the user interface.</span></span>  
8.   <span data-ttu-id="4c956-131">これがこのフォームを作成する必要がある唯一のフィールドである場合は、[**保存**] をクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="4c956-131">If this is the only field that you need to create for this form, click **Save**.</span></span> <span data-ttu-id="4c956-132">追加のフィールドを作成する必要がある場合は、[**保存して新規**] をクリックし、ステップ 7に戻ってください。</span><span class="sxs-lookup"><span data-stu-id="4c956-132">If you need to create additional fields, click **Save and new** and go back to step 7.</span></span> <span data-ttu-id="4c956-133">現在のところ、[**テーブルごとの 20 カスタム フィールド**] の制限があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="4c956-133">Note that there is currently a limit of **20 custom fields per table**.</span></span>
9.   <span data-ttu-id="4c956-134">[**新しいフィールドを作成**] ダイアログ ボックスを離れると、[**フィールドを挿入**] ダイアログ ボックスに戻ります。</span><span class="sxs-lookup"><span data-stu-id="4c956-134">Leaving the **Create new field** dialog box will return you to the **Insert fields** dialog box.</span></span> <span data-ttu-id="4c956-135">追加したカスタム フィールドは、フォームに挿入されるフィールド一覧内に自動的にマークされます。</span><span class="sxs-lookup"><span data-stu-id="4c956-135">Any custom fields that were just added will be automatically marked in the field list to be inserted into the form.</span></span>  
10.   <span data-ttu-id="4c956-136">[**挿入**] をクリックして、マークされたフィールドを選択したフォームの領域に挿入します。</span><span class="sxs-lookup"><span data-stu-id="4c956-136">Click **Insert** to insert the marked fields into the selected region of the form.</span></span> 
11.   <span data-ttu-id="4c956-137">**オプション:** 新しいフィールドを移動する個人用設定ツールバーから、選択された領域の挿入位置まで [**移動**] モードを有効にします。</span><span class="sxs-lookup"><span data-stu-id="4c956-137">**Optional:** Enable **Move** mode from the personalization toolbar to move the new fields to their desired location in the selected region.</span></span> <span data-ttu-id="4c956-138">個人使用のフォームを最適化にするさまざまな個人用設定機能を使用する方法については、[ユーザー エクスペリエンスのパーソナライズ](personalize-user-experience.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4c956-138">See [Personalize the user experience](personalize-user-experience.md) for more information about how to use the various personalization capabilities to optimize a form for your personal usage.</span></span>  

## <a name="sharing-custom-fields-with-other-users"></a><span data-ttu-id="4c956-139">他のユーザーとカスタム フィールドを共有</span><span class="sxs-lookup"><span data-stu-id="4c956-139">Sharing custom fields with other users</span></span>
<span data-ttu-id="4c956-140">カスタム フィールドを作成しフォームに公開した後、システム内の他のユーザーに新しいフィールドを含む更新されたページ ビューを提供したいかもしれません。</span><span class="sxs-lookup"><span data-stu-id="4c956-140">After you have created a custom field and exposed it on a form, you might want to provide this updated page view that includes the new field to other users in the system.</span></span> <span data-ttu-id="4c956-141">これは、製品の個人用設定機能を使用して、2つの異なる方法で実行できます。</span><span class="sxs-lookup"><span data-stu-id="4c956-141">This can be accomplished in two different ways using the personalization capabilities of the product:</span></span>

-   <span data-ttu-id="4c956-142">推奨される工順は、すべてのユーザーまたはユーザーのサブセットに個人用設定をプッシュできるシステム管理者によるものです。</span><span class="sxs-lookup"><span data-stu-id="4c956-142">The recommended route is through the system administrator, who can push a personalization to all users or a subset of users.</span></span> <span data-ttu-id="4c956-143">詳細については、[ユーザー エクスペリエンスのパーソナライズ](personalize-user-experience.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4c956-143">See [Personalize the user experience](personalize-user-experience.md) for more details.</span></span> 

-   <span data-ttu-id="4c956-144">或いは、変更内容をエクスポートし ([*個人用設定*] と呼ぶ) 1 つまたは複数のユーザーに送信し、これらのユーザーのそれぞれに変更をインポートさせることが可能です。</span><span class="sxs-lookup"><span data-stu-id="4c956-144">Alternatively, you can export your changes (called *personalizations*), send them to one or more users, and have each of those users import your changes.</span></span> <span data-ttu-id="4c956-145">個人用設定のツールバー上の [**管理**] オプションで、個人用設定をエクスポートし、インポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="4c956-145">The **Manage** option on the personalization toolbar enables you to export and import personalizations.</span></span>

## <a name="managing-custom-fields"></a><span data-ttu-id="4c956-146">カスタム フィールドを管理</span><span class="sxs-lookup"><span data-stu-id="4c956-146">Managing custom fields</span></span>

<span data-ttu-id="4c956-147">システム内のすべてのカスタム フィールドの管理については、システム管理モジュールの [**カスタム フィールド**] ページを通じて達成できます。</span><span class="sxs-lookup"><span data-stu-id="4c956-147">Management of all the custom fields in the system can be accomplished through the **Custom fields** page in the System administration module.</span></span>  <span data-ttu-id="4c956-148">ユーザーは、このページで次にある多くの機能へアクセスが可能です。</span><span class="sxs-lookup"><span data-stu-id="4c956-148">This page allows users access to many capabilities, including:</span></span> 
-   <span data-ttu-id="4c956-149">システム内のすべてのカスタム フィールドの一覧を表示。</span><span class="sxs-lookup"><span data-stu-id="4c956-149">Viewing a list of all custom fields in the system.</span></span>
-   <span data-ttu-id="4c956-150">既存のカスタム フィールドの制限付き編集。</span><span class="sxs-lookup"><span data-stu-id="4c956-150">Limited editing of existing custom fields.</span></span>
-   <span data-ttu-id="4c956-151">カスタム フィールドを削除。</span><span class="sxs-lookup"><span data-stu-id="4c956-151">Deleting custom fields.</span></span>
-   <span data-ttu-id="4c956-152">データ エンティティのカスタム フィールドを公開。</span><span class="sxs-lookup"><span data-stu-id="4c956-152">Exposing custom fields on data entities.</span></span>
-   <span data-ttu-id="4c956-153">カスタム フィールドのラベルおよびヘルプ テキストの翻訳を提供。</span><span class="sxs-lookup"><span data-stu-id="4c956-153">Providing translations of custom field labels and help text.</span></span>

### <a name="viewing-all-custom-fields"></a><span data-ttu-id="4c956-154">すべてのカスタム フィールドの表示</span><span class="sxs-lookup"><span data-stu-id="4c956-154">Viewing all custom fields</span></span>
<span data-ttu-id="4c956-155">[**カスタム フィールド**] ページでは、システム内で定義されているすべてのカスタム フィールドへの可視性を提供します。</span><span class="sxs-lookup"><span data-stu-id="4c956-155">The **Custom fields** page provides visibility to all the custom fields that have been defined in the system.</span></span> <span data-ttu-id="4c956-156">単に興味のあるテーブルを選択するだけで、ページが更新され、そのテーブルに関連付けられたカスタム フィールドの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4c956-156">Simply select the table that you are interested in, and the page will update to show a list of the custom fields associated with that table.</span></span> <span data-ttu-id="4c956-157">一覧からカスタム フィールドを選択すると、フィールドのすべての詳細を表示できます。</span><span class="sxs-lookup"><span data-stu-id="4c956-157">Choosing a custom field from the list will allow you to view all the details about the field.</span></span>

### <a name="editing-custom-fields"></a><span data-ttu-id="4c956-158">カスタム フィールドを編集。</span><span class="sxs-lookup"><span data-stu-id="4c956-158">Editing custom fields</span></span>
<span data-ttu-id="4c956-159">カスタム フィールドが作成されると、カスタム フィールドに関する特定の情報のみが [**カスタム フィールド**] ページで変更可能です。</span><span class="sxs-lookup"><span data-stu-id="4c956-159">After a custom field has been created, only certain pieces of information about the custom field can be modified on the **Custom fields** page.</span></span>   

<span data-ttu-id="4c956-160">これらの属性の変更が [*可能*] です。</span><span class="sxs-lookup"><span data-stu-id="4c956-160">You *can* modify these attributes:</span></span> 
-   <span data-ttu-id="4c956-161">ラベル</span><span class="sxs-lookup"><span data-stu-id="4c956-161">Label</span></span> 
-   <span data-ttu-id="4c956-162">ヘルプ テキスト</span><span class="sxs-lookup"><span data-stu-id="4c956-162">Help text</span></span>
-   <span data-ttu-id="4c956-163">テキスト フィールドの長さ</span><span class="sxs-lookup"><span data-stu-id="4c956-163">Length, for Text fields</span></span>

<span data-ttu-id="4c956-164">次の属性の編集が [*不可能*] です。</span><span class="sxs-lookup"><span data-stu-id="4c956-164">You *cannot* edit the following attributes:</span></span> 
-   <span data-ttu-id="4c956-165">フィールド名</span><span class="sxs-lookup"><span data-stu-id="4c956-165">Field name</span></span>
-   <span data-ttu-id="4c956-166">データ型</span><span class="sxs-lookup"><span data-stu-id="4c956-166">Data type</span></span>

<span data-ttu-id="4c956-167">さらに、ピッキングリスト フィールドに対して、カスタム フィールドの有効値のセットを変更ができ、新しい値を追加することができます。ただし、ピッキングリスト フィールドの既存の値は削除できません。</span><span class="sxs-lookup"><span data-stu-id="4c956-167">Additionally, for picklist fields, the set of valid values for the custom field can be reordered, and new values can be added; however, existing values for the picklist field cannot be removed.</span></span> <span data-ttu-id="4c956-168">変更が保存されるように特定のテーブルのフィールドを編集する際は、[**変更を適用**] クリックしてください。</span><span class="sxs-lookup"><span data-stu-id="4c956-168">Remember to click **Apply changes** when you are done editing fields for a particular table so the changes are saved.</span></span> 

### <a name="exposing-custom-fields-on-data-entities"></a><span data-ttu-id="4c956-169">データ エンティティのカスタム フィールドを公開。</span><span class="sxs-lookup"><span data-stu-id="4c956-169">Exposing custom fields on data entities</span></span>
<span data-ttu-id="4c956-170">データ エンティティに表示するカスタム フィールドを許可することが重要な場合もあります。</span><span class="sxs-lookup"><span data-stu-id="4c956-170">It may also be important to allow custom fields to be visible on data entities.</span></span> <span data-ttu-id="4c956-171">データ エンティティは、データのインポート/エクスポート シナリオと同様に、[Officeでオープン](../../dev-itpro/office-integration/office-integration.md) 機能で使用されます。</span><span class="sxs-lookup"><span data-stu-id="4c956-171">Data entities are utilized in the [Open in Office](../../dev-itpro/office-integration/office-integration.md) feature, as well as for data import/export scenarios.</span></span>  

<span data-ttu-id="4c956-172">データ エンティティでカスタム フィールドを公開するには、次の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="4c956-172">Follow these steps to expose a custom field on a data entity:</span></span> 
1.   <span data-ttu-id="4c956-173">[**カスタム フィールド**] フォームでカスタム フィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="4c956-173">Select the custom field on the **Custom fields** form.</span></span> 
2.   <span data-ttu-id="4c956-174">関連するエンティティのセットを表示するには、[**エンティティ**] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="4c956-174">Expand the **Entities** section to view the set of relevant entities.</span></span>  
3.   <span data-ttu-id="4c956-175">[**編集**] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c956-175">Click the **Edit** button.</span></span>
4.   <span data-ttu-id="4c956-176">このフィールドを公開する各エンティティを選択するには、[**有効**] フィールドを変更します。</span><span class="sxs-lookup"><span data-stu-id="4c956-176">Modify the **Enabled** field to be selected for each entity that should expose this field.</span></span>  
5.   <span data-ttu-id="4c956-177">[**変更を適用**] をクリックして選択を保存します。</span><span class="sxs-lookup"><span data-stu-id="4c956-177">Click **Apply changes** to save your selections.</span></span>  

### <a name="allowing-custom-fields-to-be-displayed-in-other-languages"></a><span data-ttu-id="4c956-178">他の言語で表示するカスタム フィールドを許可します。</span><span class="sxs-lookup"><span data-stu-id="4c956-178">Allowing custom fields to be displayed in other languages</span></span>
<span data-ttu-id="4c956-179">カスタム フィールドは、さまざまな言語でユーザーがアクセスする必要が生じた場合、[**カスタム フィールド]** ページは、他の言語に翻訳するカスタム フィールドのラベルとヘルプ テキストを許可するメカニズムを提供します。</span><span class="sxs-lookup"><span data-stu-id="4c956-179">Because custom fields may need to be accessed by users in a variety of languages, the **Custom fields** page provides a mechanism to allow the label and help text for a custom field to be translated into other languages.</span></span>  

<span data-ttu-id="4c956-180">次の手順では、他の言語でカスタム フィールドに変換するプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="4c956-180">The following steps describe the process for translating custom fields in other languages:</span></span> 
1.   <span data-ttu-id="4c956-181">[**カスタム フィールド**] ページでカスタム フィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="4c956-181">Select the custom field on the **Custom fields** page.</span></span> 
2.   <span data-ttu-id="4c956-182">アクション ペインで [**翻訳**] ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="4c956-182">Select the **Translations** button in the Action Pane.</span></span> <span data-ttu-id="4c956-183">このフィールドの既存の翻訳でドロップダウン メニューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4c956-183">This will open a drop-down menu with existing translations for this field.</span></span>
3.   <span data-ttu-id="4c956-184">[**言語**] ドロップダウン メニューでは、既に提供されている翻訳の言語のセットを表示します。</span><span class="sxs-lookup"><span data-stu-id="4c956-184">The **Language** drop-down menu shows the set of languages for which translations have already been provided.</span></span> 
     1.   <span data-ttu-id="4c956-185">既存の翻訳を編集する場合は、メニューから目的の言語を選択し、ラベルおよびヘルプ テキストの値を変更します。</span><span class="sxs-lookup"><span data-stu-id="4c956-185">If you want to edit an existing translation, select the desired language from the menu and modify the values for the label and help text.</span></span>  
     2.   <span data-ttu-id="4c956-186">それ以外の場合、[**言語の追加**] ボタンをクリックし、メニューから目的の言語を選択し、翻訳された値のラベルおよびヘルプ テキストを提供します。</span><span class="sxs-lookup"><span data-stu-id="4c956-186">Otherwise, click the **Add language** button, select the desired language from the menu, and then provide translated values for the label and help text.</span></span>  
4.   <span data-ttu-id="4c956-187">完了したら、[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c956-187">Click **OK** when you are finished.</span></span>  

### <a name="deleting-custom-fields"></a><span data-ttu-id="4c956-188">カスタム フィールドを削除。</span><span class="sxs-lookup"><span data-stu-id="4c956-188">Deleting custom fields</span></span>
<span data-ttu-id="4c956-189">まれなケースでは、カスタム フィールドが不要になることがあります。</span><span class="sxs-lookup"><span data-stu-id="4c956-189">In some rare cases, you may decide that a custom field is no longer needed.</span></span> <span data-ttu-id="4c956-190">このような場合、システム管理者は [**カスタム フィールド**] ページからフィールド削除を選択できます。</span><span class="sxs-lookup"><span data-stu-id="4c956-190">When this occurs, a system administrator can choose to delete the field from the **Custom fields** page.</span></span> <span data-ttu-id="4c956-191">これを行うには、適切なフィールドが選択されていることを確認し、[**削除**] をクリックして、削除確認のため [**はい**] をクリックし、最後に [**変更を適用**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c956-191">To do this, ensure the correct field is selected, click **Delete**, click **Yes** to confirm the deletion, and finally click **Apply changes**.</span></span> 

> [!Note]
> <span data-ttu-id="4c956-192">この操作は取り消すことができず、データベースから完全に削除されるフィールドに関連付けられているデータになります。</span><span class="sxs-lookup"><span data-stu-id="4c956-192">This action cannot be undone, and will result in the data associated with the field being permanently deleted from the database.</span></span> 

## <a name="appendix"></a><span data-ttu-id="4c956-193">付録</span><span class="sxs-lookup"><span data-stu-id="4c956-193">Appendix</span></span> 
### <a name="who-can-create-custom-fields"></a><span data-ttu-id="4c956-194">誰がカスタム フィールドを作成できますか。</span><span class="sxs-lookup"><span data-stu-id="4c956-194">Who can create custom fields?</span></span>
<span data-ttu-id="4c956-195">システムの安全対策として、システム管理者だけが既定でカスタム フィールドを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="4c956-195">As a safeguard to the system, only system administrators are able to create custom fields by default.</span></span> <span data-ttu-id="4c956-196">ただし、組織が必要と判断する Powe Users が、[**ランタイム カスタマイズ パワー ユーザー**] セキュリティ ロールを使うシステム管理者によってカスタム フィールドを作成する権限を与えることができます。</span><span class="sxs-lookup"><span data-stu-id="4c956-196">However, those power users whom the organization deems necessary can be given rights to create custom fields by a system administrator using the **Runtime customization power user** security role.</span></span> <span data-ttu-id="4c956-197">このセキュリティ ロールがないユーザーはユーザー設定のフィールドを作成することはできませんが、システム内の他のユーザーによって追加されたカスタム フィールドを表示および対話することができます。</span><span class="sxs-lookup"><span data-stu-id="4c956-197">Users without this security role will not be able to create custom fields, but will still be able to see and interact with custom fields added by other users in the system.</span></span>    

### <a name="what-tables-support-custom-fields"></a><span data-ttu-id="4c956-198">どのようなテーブルがカスタム フィールドをサポートしますか。</span><span class="sxs-lookup"><span data-stu-id="4c956-198">What tables support custom fields?</span></span>
<span data-ttu-id="4c956-199">パフォーマンスと技術的な理由として、次の条件を現在満たすテーブルのみが追加されるカスタム フィールドを使用します。</span><span class="sxs-lookup"><span data-stu-id="4c956-199">For performance and technical reasons, only tables that meet the following conditions currently allow custom fields to be added.</span></span>

- <span data-ttu-id="4c956-200">テーブルは、これらのグループの 1 つとしてタグ付けされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c956-200">The table must be tagged as one of these groups:</span></span> 
     -   <span data-ttu-id="4c956-201">グループ化</span><span class="sxs-lookup"><span data-stu-id="4c956-201">Group</span></span>
     -   <span data-ttu-id="4c956-202">WorksheetHeader</span><span class="sxs-lookup"><span data-stu-id="4c956-202">WorksheetHeader</span></span>
     -   <span data-ttu-id="4c956-203">主要</span><span class="sxs-lookup"><span data-stu-id="4c956-203">Main</span></span>
     -   <span data-ttu-id="4c956-204">その他</span><span class="sxs-lookup"><span data-stu-id="4c956-204">Miscellaneous</span></span>
     -   <span data-ttu-id="4c956-205">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4c956-205">Parameter</span></span>
     -   <span data-ttu-id="4c956-206">参照</span><span class="sxs-lookup"><span data-stu-id="4c956-206">Reference</span></span>
     -   <span data-ttu-id="4c956-207">TransactionHeader</span><span class="sxs-lookup"><span data-stu-id="4c956-207">TransactionHeader</span></span>
- <span data-ttu-id="4c956-208">テーブルは、別のテーブルを拡張できません。</span><span class="sxs-lookup"><span data-stu-id="4c956-208">The table cannot not extend another table.</span></span>
- <span data-ttu-id="4c956-209">テーブルは、システム テーブルとしてマークできません。</span><span class="sxs-lookup"><span data-stu-id="4c956-209">The table cannot be marked as a system table.</span></span>
- <span data-ttu-id="4c956-210">テーブルは、一時的テーブルになることができますか。</span><span class="sxs-lookup"><span data-stu-id="4c956-210">The table cannot be a temporary table.</span></span>

