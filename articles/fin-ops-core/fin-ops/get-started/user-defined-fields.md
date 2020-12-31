---
title: カスタム フィールドの作成と操作
description: このトピックでは、ユーザー インターフェイスを通してカスタム フィールドを作成し、ビジネスに合わせてアプリケーションを調整する方法を示します。
author: jasongre
manager: AnnBe
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SysCustomFieldManageFields
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 5f74397bcdd59a1fe24f5b6046081cbd2bed461b
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693548"
---
# <a name="create-and-work-with-custom-fields"></a><span data-ttu-id="b05bc-103">カスタム フィールドの作成と操作</span><span class="sxs-lookup"><span data-stu-id="b05bc-103">Create and work with custom fields</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b05bc-104">広範囲なビジネス プロセスを管理しすぐに使えるフィールドの広範なセットがありますが、場合によっては会社がシステムで追加情報を追跡する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b05bc-104">While there is an extensive set of fields out-of-the-box for managing a broad range of business processes, sometimes there is a need for a company to track additional information in the system.</span></span> <span data-ttu-id="b05bc-105">プログラマーは、開発者ツールでこれらのフィールドを拡張機能として追加することができますが、カスタム フィールド機能を使用すると、ユーザー インターフェイスから直接フィールドを追加できるので、Web ブラウザーを使用してビジネスに合わせてアプリケーションをカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="b05bc-105">While programmers can be used to add those fields as extensions in the developer tools, the custom fields feature allows fields to be added directly from the user interface, thereby allowing you to tailor the application to fit your business using your web browser.</span></span>

<span data-ttu-id="b05bc-106">カスタム フィールドを追加する機能は、プラットフォームのアップデート 13 以降で利用できます。</span><span class="sxs-lookup"><span data-stu-id="b05bc-106">The ability to add custom fields is available in platform update 13 and later.</span></span> <span data-ttu-id="b05bc-107">この機能にアクセスできるのは、特別なアクセス許可を持つユーザーだけです。</span><span class="sxs-lookup"><span data-stu-id="b05bc-107">Only users with special permissions have access to this feature.</span></span>

<span data-ttu-id="b05bc-108">このビデオでは、簡単にページにカスタム フィールドを追加する方法を示します: [カスタム フィールドを追加する](https://www.youtube.com/watch?v=gWSGZI9Vtnc)。</span><span class="sxs-lookup"><span data-stu-id="b05bc-108">This video shows how easy it is to add a custom field to a page: [Adding custom fields](https://www.youtube.com/watch?v=gWSGZI9Vtnc).</span></span>

## <a name="creating-custom-fields"></a><span data-ttu-id="b05bc-109">カスタム フィールドを作成</span><span class="sxs-lookup"><span data-stu-id="b05bc-109">Creating custom fields</span></span>

<span data-ttu-id="b05bc-110">アプリケーションで追跡する追加情報を識別した後、適切なテーブルでカスタム フィールドを作成し、ページに新しいフィールドを公開します。</span><span class="sxs-lookup"><span data-stu-id="b05bc-110">After you've identified additional information that you would like to track in the application, you can create the custom field on the appropriate table and expose that new field on a page.</span></span>

<span data-ttu-id="b05bc-111">次の手順で、カスタム フィールドの作成とフォーム上のフィールド配置のプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="b05bc-111">The following steps describe the process for creating a custom field and placing that field on a form.</span></span>

1. <span data-ttu-id="b05bc-112">新しいフィールドを必要とするフォームへ移動します。</span><span class="sxs-lookup"><span data-stu-id="b05bc-112">Navigate to the form where the new field is needed.</span></span>
2. <span data-ttu-id="b05bc-113">最終目標は、フォーム上のカスタム フィールドを公開することなので、カスタム フィールドを作成するためのエントリ ポイントは、個人用設定のエクスペリエンス内に存在します。</span><span class="sxs-lookup"><span data-stu-id="b05bc-113">Because the end goal is to expose the custom field on a form, the entry point for creating custom fields exists inside the personalization experience.</span></span> <span data-ttu-id="b05bc-114">個人用設定のツールバーを開くには、**オプション** を選択し、そして **このフォームをカスタマイズ** を選びます。</span><span class="sxs-lookup"><span data-stu-id="b05bc-114">Open the personalization toolbar by selecting **Options**, and then **Personalize this form**.</span></span>
3. <span data-ttu-id="b05bc-115">**挿入** をクリックし、次に **フィールド** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b05bc-115">Click **Insert** and then **Field**.</span></span>
4. <span data-ttu-id="b05bc-116">新しいフィールドを公開するフォームの領域を選択します。</span><span class="sxs-lookup"><span data-stu-id="b05bc-116">Select the region of the form where you want to expose the new field.</span></span> <span data-ttu-id="b05bc-117">選択した後、**フィールドを挿入** ダイアログ ボックスで、選択したフォームの領域を挿入する既存のフィールドの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b05bc-117">After selection, the **Insert fields** dialog box will display a list of existing fields that can be inserted into the selected region of the form.</span></span>
5. <span data-ttu-id="b05bc-118">興味のあるフィールドが一覧に存在しないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b05bc-118">Ensure that the field you are interested in does not already exist in the list.</span></span> <span data-ttu-id="b05bc-119">その場合は、単に一覧のフィールドを選択し、**挿入** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b05bc-119">If it does, you can simply select that field in the list and click **Insert**.</span></span>
6. <span data-ttu-id="b05bc-120">カスタム フィールドを作成するプロセスを開始する一覧の上にある **新しいフィールドを作成** ボタンをクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="b05bc-120">Click the **Create new field** button above the list to initiate the process of creating a custom field.</span></span> <span data-ttu-id="b05bc-121">これで **新しいフィールドを作成** ダイアログ ボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="b05bc-121">This will open the **Create new field** dialog box.</span></span>

    <span data-ttu-id="b05bc-122">**新しいフィールドを作成** ボタンが表示されない場合、あなたはこの機能を使用するための必要な権限を持っていません。</span><span class="sxs-lookup"><span data-stu-id="b05bc-122">If you do not see the **Create new field** button, you do not have the necessary permissions to use this feature.</span></span>

7. <span data-ttu-id="b05bc-123">**新しいフィールドを作成** ダイアログ ボックスで、次の情報を入力してください。</span><span class="sxs-lookup"><span data-stu-id="b05bc-123">In the **Create new field** dialog box, enter the following information.</span></span>

    1. <span data-ttu-id="b05bc-124">このフィールドを追加する必要があるデータベース テーブルを選択します。</span><span class="sxs-lookup"><span data-stu-id="b05bc-124">Select the database table where this field should be added.</span></span> <span data-ttu-id="b05bc-125">カスタム フィールドをサポートするテーブルのみ、ドロップダウン リストに表示されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b05bc-125">Note that only tables that support custom fields will appear in the drop-down list.</span></span> <span data-ttu-id="b05bc-126">サポートされているテーブルの技術上の詳細については、以下のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b05bc-126">See the section below for technical details on supported tables.</span></span>
    2. <span data-ttu-id="b05bc-127">新しいフィールドのデータ タイプを選択してください。</span><span class="sxs-lookup"><span data-stu-id="b05bc-127">Select the data type for the new field.</span></span> <span data-ttu-id="b05bc-128">使用可能なデータ タイプは、チェック ボックス、日付、日時、10 進数、番号、ピッキングリスト、およびテキストです。</span><span class="sxs-lookup"><span data-stu-id="b05bc-128">The available data types are checkbox, date, date time, decimal, number, picklist, and text.</span></span>

        - <span data-ttu-id="b05bc-129">テキストのデータ タイプを選択する場合は、このフィールドに入力できるテキストの最長も指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="b05bc-129">If you choose the text data type, you can also specify the maximum length of the text that can be entered in this field.</span></span>
        - <span data-ttu-id="b05bc-130">ピッキングリストのデータ タイプを選択する場合は、フィールドの有効な値のセットを選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="b05bc-130">If you choose the picklist data type, you can also select the set of valid values for the field.</span></span>

    3. <span data-ttu-id="b05bc-131">フィールドの名前、ラベル、およびヘルプ テキストを指定してください。</span><span class="sxs-lookup"><span data-stu-id="b05bc-131">Provide a name, label, and help text for the field.</span></span> <span data-ttu-id="b05bc-132">名前はデータベースの現物フィールド名に対応しています。一方、ラベルとヘルプ テキストはユーザー インターフェイスでこのフィールドを表すために使用されるテキストです。</span><span class="sxs-lookup"><span data-stu-id="b05bc-132">The name corresponds to the physical field name in the database, whereas the label and help text are the text used to represent this field in the user interface.</span></span>

8. <span data-ttu-id="b05bc-133">これがこのフォームを作成する必要がある唯一のフィールドである場合は、**保存** をクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="b05bc-133">If this is the only field that you need to create for this form, click **Save**.</span></span> <span data-ttu-id="b05bc-134">追加のフィールドを作成する必要がある場合は、**保存して新規** をクリックし、ステップ 7に戻ってください。</span><span class="sxs-lookup"><span data-stu-id="b05bc-134">If you need to create additional fields, click **Save and new** and go back to step 7.</span></span> <span data-ttu-id="b05bc-135">現在のところ、**テーブルごとの 20 カスタム フィールド** の制限があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b05bc-135">Note that there is currently a limit of **20 custom fields per table**.</span></span>
9. <span data-ttu-id="b05bc-136">**新しいフィールドを作成** ダイアログ ボックスを離れると、**フィールドを挿入** ダイアログ ボックスに戻ります。</span><span class="sxs-lookup"><span data-stu-id="b05bc-136">Leaving the **Create new field** dialog box will return you to the **Insert fields** dialog box.</span></span> <span data-ttu-id="b05bc-137">追加したカスタム フィールドは、フォームに挿入されるフィールド一覧内に自動的にマークされます。</span><span class="sxs-lookup"><span data-stu-id="b05bc-137">Any custom fields that were just added will be automatically marked in the field list to be inserted into the form.</span></span>
10. <span data-ttu-id="b05bc-138">**挿入** をクリックして、マークされたフィールドを選択したフォームの領域に挿入します。</span><span class="sxs-lookup"><span data-stu-id="b05bc-138">Click **Insert** to insert the marked fields into the selected region of the form.</span></span>
11. <span data-ttu-id="b05bc-139">**オプション:** 新しいフィールドを移動する個人用設定ツールバーから、選択された領域の挿入位置まで **移動** モードを有効にします。</span><span class="sxs-lookup"><span data-stu-id="b05bc-139">**Optional:** Enable **Move** mode from the personalization toolbar to move the new fields to their desired location in the selected region.</span></span> <span data-ttu-id="b05bc-140">個人使用のフォームを最適化にするさまざまな個人用設定機能を使用する方法については、[ユーザー エクスペリエンスのパーソナライズ](personalize-user-experience.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b05bc-140">See [Personalize the user experience](personalize-user-experience.md) for more information about how to use the various personalization capabilities to optimize a form for your personal usage.</span></span>

## <a name="sharing-custom-fields-with-other-users"></a><span data-ttu-id="b05bc-141">他のユーザーとカスタム フィールドを共有</span><span class="sxs-lookup"><span data-stu-id="b05bc-141">Sharing custom fields with other users</span></span>

<span data-ttu-id="b05bc-142">カスタム フィールドを作成しフォームに公開した後、システム内の他のユーザーに新しいフィールドを含む更新されたページ ビューを提供したいかもしれません。</span><span class="sxs-lookup"><span data-stu-id="b05bc-142">After you have created a custom field and exposed it on a form, you might want to provide this updated page view that includes the new field to other users in the system.</span></span> <span data-ttu-id="b05bc-143">これは、製品の個人用設定機能を使用して、2つの異なる方法で実行できます。</span><span class="sxs-lookup"><span data-stu-id="b05bc-143">This can be accomplished in two different ways using the personalization capabilities of the product:</span></span>

- <span data-ttu-id="b05bc-144">推奨される工順は、すべてのユーザーまたはユーザーのサブセットに個人用設定をプッシュできるシステム管理者によるものです。</span><span class="sxs-lookup"><span data-stu-id="b05bc-144">The recommended route is through the system administrator, who can push a personalization to all users or a subset of users.</span></span> <span data-ttu-id="b05bc-145">詳細については、[ユーザー エクスペリエンスのパーソナライズ](personalize-user-experience.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b05bc-145">See [Personalize the user experience](personalize-user-experience.md) for more details.</span></span>
- <span data-ttu-id="b05bc-146">或いは、変更内容をエクスポートし (*個人用設定* と呼ぶ) 1 つまたは複数のユーザーに送信し、これらのユーザーのそれぞれに変更をインポートさせることが可能です。</span><span class="sxs-lookup"><span data-stu-id="b05bc-146">Alternatively, you can export your changes (called *personalizations*), send them to one or more users, and have each of those users import your changes.</span></span> <span data-ttu-id="b05bc-147">個人用設定のツールバー上の **管理** オプションで、個人用設定をエクスポートし、インポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="b05bc-147">The **Manage** option on the personalization toolbar enables you to export and import personalizations.</span></span>

## <a name="managing-custom-fields"></a><span data-ttu-id="b05bc-148">カスタム フィールドを管理</span><span class="sxs-lookup"><span data-stu-id="b05bc-148">Managing custom fields</span></span>

<span data-ttu-id="b05bc-149">システム内のすべてのカスタム フィールドの管理については、システム管理モジュールの **カスタム フィールド** ページを通じて達成できます。</span><span class="sxs-lookup"><span data-stu-id="b05bc-149">Management of all the custom fields in the system can be accomplished through the **Custom fields** page in the System administration module.</span></span> <span data-ttu-id="b05bc-150">ユーザーは、このページで次にある多くの機能へアクセスが可能です。</span><span class="sxs-lookup"><span data-stu-id="b05bc-150">This page allows users access to many capabilities, including:</span></span>

- <span data-ttu-id="b05bc-151">システム内のすべてのカスタム フィールドの一覧を表示。</span><span class="sxs-lookup"><span data-stu-id="b05bc-151">Viewing a list of all custom fields in the system.</span></span>
- <span data-ttu-id="b05bc-152">既存のカスタム フィールドの制限付き編集。</span><span class="sxs-lookup"><span data-stu-id="b05bc-152">Limited editing of existing custom fields.</span></span>
- <span data-ttu-id="b05bc-153">カスタム フィールドを削除。</span><span class="sxs-lookup"><span data-stu-id="b05bc-153">Deleting custom fields.</span></span>
- <span data-ttu-id="b05bc-154">データ エンティティのカスタム フィールドを公開。</span><span class="sxs-lookup"><span data-stu-id="b05bc-154">Exposing custom fields on data entities.</span></span>
- <span data-ttu-id="b05bc-155">カスタム フィールドのラベルおよびヘルプ テキストの翻訳を提供。</span><span class="sxs-lookup"><span data-stu-id="b05bc-155">Providing translations of custom field labels and help text.</span></span>

### <a name="viewing-all-custom-fields"></a><span data-ttu-id="b05bc-156">すべてのカスタム フィールドの表示</span><span class="sxs-lookup"><span data-stu-id="b05bc-156">Viewing all custom fields</span></span>

<span data-ttu-id="b05bc-157">**カスタム フィールド** ページでは、システム内で定義されているすべてのカスタム フィールドへの可視性を提供します。</span><span class="sxs-lookup"><span data-stu-id="b05bc-157">The **Custom fields** page provides visibility to all the custom fields that have been defined in the system.</span></span> <span data-ttu-id="b05bc-158">単に興味のあるテーブルを選択するだけで、ページが更新され、そのテーブルに関連付けられたカスタム フィールドの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b05bc-158">Simply select the table that you are interested in, and the page will update to show a list of the custom fields associated with that table.</span></span> <span data-ttu-id="b05bc-159">一覧からカスタム フィールドを選択すると、フィールドのすべての詳細を表示できます。</span><span class="sxs-lookup"><span data-stu-id="b05bc-159">Choosing a custom field from the list will allow you to view all the details about the field.</span></span>

### <a name="editing-custom-fields"></a><span data-ttu-id="b05bc-160">カスタム フィールドを編集。</span><span class="sxs-lookup"><span data-stu-id="b05bc-160">Editing custom fields</span></span>

<span data-ttu-id="b05bc-161">カスタム フィールドが作成されると、カスタム フィールドに関する特定の情報のみが **カスタム フィールド** ページで変更可能です。</span><span class="sxs-lookup"><span data-stu-id="b05bc-161">After a custom field has been created, only certain pieces of information about the custom field can be modified on the **Custom fields** page.</span></span>

<span data-ttu-id="b05bc-162">これらの属性の変更が *可能* です。</span><span class="sxs-lookup"><span data-stu-id="b05bc-162">You *can* modify these attributes:</span></span>

- <span data-ttu-id="b05bc-163">ラベル</span><span class="sxs-lookup"><span data-stu-id="b05bc-163">Label</span></span>
- <span data-ttu-id="b05bc-164">ヘルプ テキスト</span><span class="sxs-lookup"><span data-stu-id="b05bc-164">Help text</span></span>
- <span data-ttu-id="b05bc-165">テキスト フィールドの長さ</span><span class="sxs-lookup"><span data-stu-id="b05bc-165">Length, for Text fields</span></span>

<span data-ttu-id="b05bc-166">次の属性の編集が *不可能* です。</span><span class="sxs-lookup"><span data-stu-id="b05bc-166">You *cannot* edit the following attributes:</span></span>

- <span data-ttu-id="b05bc-167">フィールド名</span><span class="sxs-lookup"><span data-stu-id="b05bc-167">Field name</span></span>
- <span data-ttu-id="b05bc-168">データ型</span><span class="sxs-lookup"><span data-stu-id="b05bc-168">Data type</span></span>

<span data-ttu-id="b05bc-169">さらに、ピッキングリスト フィールドに対して、カスタム フィールドの有効値のセットを変更ができ、新しい値を追加することができます。ただし、ピッキングリスト フィールドの既存の値は削除できません。</span><span class="sxs-lookup"><span data-stu-id="b05bc-169">Additionally, for picklist fields, the set of valid values for the custom field can be reordered, and new values can be added; however, existing values for the picklist field cannot be removed.</span></span> <span data-ttu-id="b05bc-170">変更が保存されるように特定のテーブルのフィールドを編集する際は、**変更を適用** クリックしてください。</span><span class="sxs-lookup"><span data-stu-id="b05bc-170">Remember to click **Apply changes** when you are done editing fields for a particular table so the changes are saved.</span></span>

### <a name="exposing-custom-fields-on-data-entities"></a><span data-ttu-id="b05bc-171">データ エンティティのカスタム フィールドを公開。</span><span class="sxs-lookup"><span data-stu-id="b05bc-171">Exposing custom fields on data entities</span></span>

<span data-ttu-id="b05bc-172">データ エンティティに表示するカスタム フィールドを許可することが重要な場合もあります。</span><span class="sxs-lookup"><span data-stu-id="b05bc-172">It may also be important to allow custom fields to be visible on data entities.</span></span> <span data-ttu-id="b05bc-173">データ エンティティは、データのインポート/エクスポート シナリオと同様に、[Office 統合の概要](../../dev-itpro/office-integration/office-integration.md) 機能で使用されます。</span><span class="sxs-lookup"><span data-stu-id="b05bc-173">Data entities are utilized in the [Office integration overview](../../dev-itpro/office-integration/office-integration.md) feature, as well as for data import/export scenarios.</span></span>

<span data-ttu-id="b05bc-174">データ エンティティでカスタム フィールドを公開するには、次の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="b05bc-174">Follow these steps to expose a custom field on a data entity:</span></span>

1. <span data-ttu-id="b05bc-175">**カスタム フィールド** フォームでカスタム フィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="b05bc-175">Select the custom field on the **Custom fields** form.</span></span>
2. <span data-ttu-id="b05bc-176">関連するエンティティのセットを表示するには、**エンティティ** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="b05bc-176">Expand the **Entities** section to view the set of relevant entities.</span></span>
3. <span data-ttu-id="b05bc-177">**編集** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b05bc-177">Click the **Edit** button.</span></span>
4. <span data-ttu-id="b05bc-178">このフィールドを公開する各エンティティを選択するには、**有効** フィールドを変更します。</span><span class="sxs-lookup"><span data-stu-id="b05bc-178">Modify the **Enabled** field to be selected for each entity that should expose this field.</span></span>
5. <span data-ttu-id="b05bc-179">**変更を適用** をクリックして選択を保存します。</span><span class="sxs-lookup"><span data-stu-id="b05bc-179">Click **Apply changes** to save your selections.</span></span>

### <a name="allowing-custom-fields-to-be-displayed-in-other-languages"></a><span data-ttu-id="b05bc-180">他の言語で表示するカスタム フィールドを許可します。</span><span class="sxs-lookup"><span data-stu-id="b05bc-180">Allowing custom fields to be displayed in other languages</span></span>

<span data-ttu-id="b05bc-181">カスタム フィールドは、さまざまな言語でユーザーがアクセスする必要が生じた場合、**カスタム フィールド** ページは、他の言語に翻訳するカスタム フィールドのラベルとヘルプ テキストを許可するメカニズムを提供します。</span><span class="sxs-lookup"><span data-stu-id="b05bc-181">Because custom fields may need to be accessed by users in a variety of languages, the **Custom fields** page provides a mechanism to allow the label and help text for a custom field to be translated into other languages.</span></span>

<span data-ttu-id="b05bc-182">次の手順では、他の言語でカスタム フィールドに変換するプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="b05bc-182">The following steps describe the process for translating custom fields in other languages:</span></span>

1. <span data-ttu-id="b05bc-183">**カスタム フィールド** ページでカスタム フィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="b05bc-183">Select the custom field on the **Custom fields** page.</span></span>
2. <span data-ttu-id="b05bc-184">アクション ペインで **翻訳** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="b05bc-184">Select the **Translations** button in the Action Pane.</span></span> <span data-ttu-id="b05bc-185">このフィールドの既存の翻訳でドロップダウン メニューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b05bc-185">This will open a drop-down menu with existing translations for this field.</span></span>
3. <span data-ttu-id="b05bc-186">**言語** ドロップダウン メニューでは、既に提供されている翻訳の言語のセットを表示します。</span><span class="sxs-lookup"><span data-stu-id="b05bc-186">The **Language** drop-down menu shows the set of languages for which translations have already been provided.</span></span>

    <span data-ttu-id="b05bc-187">既存の翻訳を編集する場合は、メニューから目的の言語を選択し、ラベルおよびヘルプ テキストの値を変更します。</span><span class="sxs-lookup"><span data-stu-id="b05bc-187">If you want to edit an existing translation, select the desired language from the menu and modify the values for the label and help text.</span></span>

    <span data-ttu-id="b05bc-188">それ以外の場合、**言語の追加** ボタンをクリックし、メニューから目的の言語を選択し、翻訳された値のラベルおよびヘルプ テキストを提供します。</span><span class="sxs-lookup"><span data-stu-id="b05bc-188">Otherwise, click the **Add language** button, select the desired language from the menu, and then provide translated values for the label and help text.</span></span>

4. <span data-ttu-id="b05bc-189">完了したら、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b05bc-189">Click **OK** when you are finished.</span></span>

### <a name="deleting-custom-fields"></a><span data-ttu-id="b05bc-190">カスタム フィールドを削除。</span><span class="sxs-lookup"><span data-stu-id="b05bc-190">Deleting custom fields</span></span>

<span data-ttu-id="b05bc-191">まれなケースでは、カスタム フィールドが不要になることがあります。</span><span class="sxs-lookup"><span data-stu-id="b05bc-191">In some rare cases, you may decide that a custom field is no longer needed.</span></span> <span data-ttu-id="b05bc-192">このような場合、システム管理者は **カスタム フィールド** ページからフィールド削除を選択できます。</span><span class="sxs-lookup"><span data-stu-id="b05bc-192">When this occurs, a system administrator can choose to delete the field from the **Custom fields** page.</span></span> <span data-ttu-id="b05bc-193">これを行うには、適切なフィールドが選択されていることを確認し、**削除** をクリックして、削除確認のため **はい** をクリックし、最後に **変更を適用** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b05bc-193">To do this, ensure the correct field is selected, click **Delete**, click **Yes** to confirm the deletion, and finally click **Apply changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="b05bc-194">この操作は取り消すことができず、データベースから完全に削除されるフィールドに関連付けられているデータになります。</span><span class="sxs-lookup"><span data-stu-id="b05bc-194">This action cannot be undone, and will result in the data associated with the field being permanently deleted from the database.</span></span>

## <a name="appendix"></a><span data-ttu-id="b05bc-195">付録</span><span class="sxs-lookup"><span data-stu-id="b05bc-195">Appendix</span></span>

### <a name="who-can-create-custom-fields"></a><span data-ttu-id="b05bc-196">誰がカスタム フィールドを作成できますか。</span><span class="sxs-lookup"><span data-stu-id="b05bc-196">Who can create custom fields?</span></span>

<span data-ttu-id="b05bc-197">システムの安全対策として、システム管理者だけが既定でカスタム フィールドを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="b05bc-197">As a safeguard to the system, only system administrators are able to create custom fields by default.</span></span> <span data-ttu-id="b05bc-198">ただし、組織が必要と判断する Powe Users が、**ランタイム カスタマイズ パワー ユーザー** セキュリティ ロールを使うシステム管理者によってカスタム フィールドを作成する権限を与えることができます。</span><span class="sxs-lookup"><span data-stu-id="b05bc-198">However, those power users whom the organization deems necessary can be given rights to create custom fields by a system administrator using the **Runtime customization power user** security role.</span></span> <span data-ttu-id="b05bc-199">このセキュリティ ロールがないユーザーはユーザー設定のフィールドを作成することはできませんが、システム内の他のユーザーによって追加されたカスタム フィールドを表示および対話することができます。</span><span class="sxs-lookup"><span data-stu-id="b05bc-199">Users without this security role will not be able to create custom fields, but will still be able to see and interact with custom fields added by other users in the system.</span></span>

### <a name="what-tables-support-custom-fields"></a><span data-ttu-id="b05bc-200">どのようなテーブルがカスタム フィールドをサポートしますか。</span><span class="sxs-lookup"><span data-stu-id="b05bc-200">What tables support custom fields?</span></span>

<span data-ttu-id="b05bc-201">パフォーマンスと技術的な理由として、次の条件を現在満たすテーブルのみが追加されるカスタム フィールドを使用します。</span><span class="sxs-lookup"><span data-stu-id="b05bc-201">For performance and technical reasons, only tables that meet the following conditions currently allow custom fields to be added.</span></span>

- <span data-ttu-id="b05bc-202">テーブルは、これらのグループの 1 つとしてタグ付けされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="b05bc-202">The table must be tagged as one of these groups:</span></span>

    - <span data-ttu-id="b05bc-203">グループ化</span><span class="sxs-lookup"><span data-stu-id="b05bc-203">Group</span></span>
    - <span data-ttu-id="b05bc-204">WorksheetHeader</span><span class="sxs-lookup"><span data-stu-id="b05bc-204">WorksheetHeader</span></span>
    - <span data-ttu-id="b05bc-205">主要</span><span class="sxs-lookup"><span data-stu-id="b05bc-205">Main</span></span>
    - <span data-ttu-id="b05bc-206">その他</span><span class="sxs-lookup"><span data-stu-id="b05bc-206">Miscellaneous</span></span>
    - <span data-ttu-id="b05bc-207">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b05bc-207">Parameter</span></span>
    - <span data-ttu-id="b05bc-208">参照</span><span class="sxs-lookup"><span data-stu-id="b05bc-208">Reference</span></span>
    - <span data-ttu-id="b05bc-209">TransactionHeader</span><span class="sxs-lookup"><span data-stu-id="b05bc-209">TransactionHeader</span></span>

- <span data-ttu-id="b05bc-210">テーブルは、別のテーブルを拡張できません。</span><span class="sxs-lookup"><span data-stu-id="b05bc-210">The table cannot extend another table.</span></span>
- <span data-ttu-id="b05bc-211">テーブルは、システム テーブルとしてマークできません。</span><span class="sxs-lookup"><span data-stu-id="b05bc-211">The table cannot be marked as a system table.</span></span>
- <span data-ttu-id="b05bc-212">テーブルは、一時的テーブルになることができますか。</span><span class="sxs-lookup"><span data-stu-id="b05bc-212">The table cannot be a temporary table.</span></span>

### <a name="can-i-reference-custom-fields-from-the-developer-tools"></a><span data-ttu-id="b05bc-213">開発者ツールからカスタム フィールドを参照することはできますか?</span><span class="sxs-lookup"><span data-stu-id="b05bc-213">Can I reference custom fields from the developer tools?</span></span>  

<span data-ttu-id="b05bc-214">カスタム フィールドは、ユーザー インターフェイスを通してのみ管理でき、コードからは参照できません。</span><span class="sxs-lookup"><span data-stu-id="b05bc-214">Custom fields can only be managed through the user interface and cannot be referenced by code.</span></span> 
