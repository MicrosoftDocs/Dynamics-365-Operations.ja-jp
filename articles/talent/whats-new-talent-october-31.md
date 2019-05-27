---
title: Dynamics 365 for Talent Core HR の新機能および変更された機能 (2018 年 10 月 31 日)
description: このトピックでは、Microsoft Dynamics 365 for Talent Core HR の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 10/31/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d6942f8e4dc86f18a081b347df0567b1358a87ab
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518488"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-31-2018"></a><span data-ttu-id="f82d5-103">Dynamics 365 for Talent Core HR の新機能および変更された機能 (2018 年 10 月 31 日)</span><span class="sxs-lookup"><span data-stu-id="f82d5-103">What's new or changed in Dynamics 365 for Talent Core HR (October 31, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f82d5-104">**ビルド 8.1.2031**</span><span class="sxs-lookup"><span data-stu-id="f82d5-104">**Build 8.1.2031**</span></span>

<span data-ttu-id="f82d5-105">このトピックでは、Core HR の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="f82d5-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="create-links-from-talent-to-finance-and-operations"></a><span data-ttu-id="f82d5-106">Talent から Finance and Operations へのリンクの作成</span><span class="sxs-lookup"><span data-stu-id="f82d5-106">Create links from Talent to Finance and Operations</span></span>
<span data-ttu-id="f82d5-107">この新しいナビゲーション機能により、Talent から Finance and Operations へリンクすることができ、Finance and Operations のページへの直接のナビゲーションが提供されます。</span><span class="sxs-lookup"><span data-stu-id="f82d5-107">This new navigation functionality allows you to link from Talent to Finance and Operations, giving you direct navigation into Finance and Operations pages.</span></span> <span data-ttu-id="f82d5-108">リンクがコンフィギュレーションされている場合、リンクの名前およびグループを指定することができますが、そのリンクは Talent 内で表示され、ターゲット ページは Finance and Operations 内で開かれます。</span><span class="sxs-lookup"><span data-stu-id="f82d5-108">When links are configured, you can specify the name and group of the link, where the link should surface in Talent, and the target page to be opened within Finance and Operations.</span></span>

#### <a name="coming-soon"></a><span data-ttu-id="f82d5-109">間もなく公開</span><span class="sxs-lookup"><span data-stu-id="f82d5-109">Coming soon</span></span>
<span data-ttu-id="f82d5-110">フィールド コンテキストは、直接ナビゲーションのために、Finance and Operations の対応するレコードに将来追加されます。</span><span class="sxs-lookup"><span data-stu-id="f82d5-110">Field context will be added in the future to allow for direct navigation to corresponding records in Finance and Operations.</span></span> <span data-ttu-id="f82d5-111">たとえば、**フィールドへのリンク**を使用して、Finance and Operations 内の特定の従業員または職位へ直接移動するためのコンテキストを提供できます。</span><span class="sxs-lookup"><span data-stu-id="f82d5-111">For example, you can use **Link to field** to provide the context to navigate directly to a specific employee or position in Finance and Operations.</span></span>

### <a name="configure-target-systems"></a><span data-ttu-id="f82d5-112">ターゲット システムの構成</span><span class="sxs-lookup"><span data-stu-id="f82d5-112">Configure target systems</span></span>

<span data-ttu-id="f82d5-113">Talent において、システム管理者は、システム管理ワークスペースを通じて表示されるリンクを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="f82d5-113">In Talent, system administrators can define links that will be surfaced through the System Administration workspace.</span></span> <span data-ttu-id="f82d5-114">リンクの「ターゲット」となる移動先の Finance and Operations 環境は、コンフィギュレーションの一部です。</span><span class="sxs-lookup"><span data-stu-id="f82d5-114">Part of the configuration is the Finance and Operations environments that you would like to navigate to as the "target" of the link.</span></span> <span data-ttu-id="f82d5-115">この操作は、ターゲット システムに名前を付け、Finance and Operations 環境の URL を提供することによって行われます。</span><span class="sxs-lookup"><span data-stu-id="f82d5-115">You do this by giving the target system a name and providing the URL of the Finance and Operations environment.</span></span> <span data-ttu-id="f82d5-116">提供できる Finance and Operations の URL の例を次に示します。https://devax00124aos.cloud.test.dynamics.com/</span><span class="sxs-lookup"><span data-stu-id="f82d5-116">Here is an example of a Finance and Operations URL that you would provide: https://devax00124aos.cloud.test.dynamics.com/.</span></span> <span data-ttu-id="f82d5-117">ターゲット システムのコンフィギュレーションの後に、リンクを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="f82d5-117">After you have configured your target systems,  you can define your links.</span></span>

### <a name="configure-links"></a><span data-ttu-id="f82d5-118">リンクを構成する</span><span class="sxs-lookup"><span data-stu-id="f82d5-118">Configure links</span></span>

<span data-ttu-id="f82d5-119">作成される各リンクには、次の情報が定義されます。</span><span class="sxs-lookup"><span data-stu-id="f82d5-119">Each link that is created will have the following information defined.</span></span>

- <span data-ttu-id="f82d5-120">リンク - リンクの名前、識別のためにのみ使用。</span><span class="sxs-lookup"><span data-stu-id="f82d5-120">Link - Name of the link, used for identification only.</span></span>

- <span data-ttu-id="f82d5-121">このリンクを有効にする - Talent のユーザーにリンクを表示する場合、**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="f82d5-121">Enable this Link - Set to **Yes** if you want to display the link to users of Talent.</span></span>

- <span data-ttu-id="f82d5-122">表示名 - Finance and Operations へのリンクとして表示される名前を定義します。</span><span class="sxs-lookup"><span data-stu-id="f82d5-122">Display name - Define the name that will appear as a link to Finance and Operations.</span></span> <span data-ttu-id="f82d5-123">このデータは、現在翻訳されていません。</span><span class="sxs-lookup"><span data-stu-id="f82d5-123">This data is currently is not translated.</span></span>

- <span data-ttu-id="f82d5-124">フォームのサーフェス リンク - リンクを表示するページを選択します。</span><span class="sxs-lookup"><span data-stu-id="f82d5-124">Surface link on form - Choose which page you would like to display the link on.</span></span>

- <span data-ttu-id="f82d5-125">グループ - グループは必須ではありませんが、グループを使用してリンクを整理する場合、既存のグループを選択するか、または**グループ** フィールドを使用して新しいグループを作成します。</span><span class="sxs-lookup"><span data-stu-id="f82d5-125">Group - Groups are not required, but if you want to organize your links using groups, select an existing group or create a new one using the **Group** field.</span></span>

- <span data-ttu-id="f82d5-126">ターゲット システム - **ターゲット システムのコンフィギュレーション** オプションを使用して作成されたターゲット システムを選択します。</span><span class="sxs-lookup"><span data-stu-id="f82d5-126">Target system - Select the target system that was created using the **Configure target system** option.</span></span> <span data-ttu-id="f82d5-127">これは、リンクを使用して移動する時に使用される Finance and Operations の環境になります。</span><span class="sxs-lookup"><span data-stu-id="f82d5-127">This will be the Finance and Operations environment that will be used when navigating by using the link.</span></span>

- <span data-ttu-id="f82d5-128">ユーザーの現在の会社を使用する - Finance and Operations へ移動する時にユーザーの現在の会社のコンテキストを使用する場合に**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f82d5-128">Use user's current Company - Select **Yes** if you would like to use the User's current company context when navigating to Finance and Operations.</span></span> <span data-ttu-id="f82d5-129">**いいえ**が選択されている場合、使用する会社を選択することができます。</span><span class="sxs-lookup"><span data-stu-id="f82d5-129">If **No** is selected, then you can select the company that should be used.</span></span>

- <span data-ttu-id="f82d5-130">ターゲット メニュー項目 - 移動する時にリンクが使用する Finance and Operation からメニュー項目を入力します。</span><span class="sxs-lookup"><span data-stu-id="f82d5-130">Target menu item - Enter the menu item from Finance and Operation that the link should use when navigating.</span></span> <span data-ttu-id="f82d5-131">直接移動できるメニュー項目は使用可能です。</span><span class="sxs-lookup"><span data-stu-id="f82d5-131">Menu items that you can directly navigate to are available.</span></span> <span data-ttu-id="f82d5-132">必要なメニュー項目を検索するために、Finance and Operations を開き、ナビゲーションのターゲットとなるページを開きます。</span><span class="sxs-lookup"><span data-stu-id="f82d5-132">To find the menu item required, open Finance and Operations and open the page that is the target of the navigation.</span></span> <span data-ttu-id="f82d5-133">URL からメニュー項目をコピーします。</span><span class="sxs-lookup"><span data-stu-id="f82d5-133">Copy the menu item from the URL.</span></span> <span data-ttu-id="f82d5-134">たとえば、リンクにより Finance and Operations の従業員リストに移動したい場合、URL の「&mi」の後に表示される値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f82d5-134">For example, if you want the link to take you to the employee list in Finance and Operations, enter the value that appears after the "&mi" in the URL.</span></span> <span data-ttu-id="f82d5-135">https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees。</span><span class="sxs-lookup"><span data-stu-id="f82d5-135">https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees.</span></span> <span data-ttu-id="f82d5-136">この例の従業員リスト ページに移動するメニュー項目は、HcmWorkerListPage_Employees です。</span><span class="sxs-lookup"><span data-stu-id="f82d5-136">The menu item to navigate to the employee list page in this example is: HcmWorkerListPage_Employees.</span></span>

- <span data-ttu-id="f82d5-137">データ ソースへのリンク - リンクが参照しているデータのソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="f82d5-137">Link to data source - Select the source of data that the link is referencing.</span></span> <span data-ttu-id="f82d5-138">**作業者**および**職位**など、最も一般的なソースが利用可能です。</span><span class="sxs-lookup"><span data-stu-id="f82d5-138">The most common sources like **Worker** and **Position** are available.</span></span>

- <span data-ttu-id="f82d5-139">フィールドへのリンク - (間もなく公開) このフィールドの選択により、Talent の 1 つのレコードから Finance and Operations の 1 つのレコードへの直接ナビゲーションが可能になります。</span><span class="sxs-lookup"><span data-stu-id="f82d5-139">Link to field - (Coming soon) This field selection will allow for direct navigation from a single record in Talent to a single record in Finance and Operations.</span></span>

### <a name="access-to-links"></a><span data-ttu-id="f82d5-140">リンクへのアクセス</span><span class="sxs-lookup"><span data-stu-id="f82d5-140">Access to links</span></span>

<span data-ttu-id="f82d5-141">**このリンクを有効にする**オプションが**いいえ**に設定されている場合でも、システム管理者は、定義されたページ上で新しく作成されたリンクを参照することができます。</span><span class="sxs-lookup"><span data-stu-id="f82d5-141">System administrators will see the newly created links on the defined pages even if the **Enable this link** option is set to **No**.</span></span> <span data-ttu-id="f82d5-142">これは、リンクをテストするために、他の従業員に表示されるより前に使用できます。</span><span class="sxs-lookup"><span data-stu-id="f82d5-142">This can be used for testing links prior to surfacing them to other employees.</span></span> <span data-ttu-id="f82d5-143">他のすべてのロールには、**このリンクを有効にする**オプションを**はい**に設定した後、コンフィギュレーションされたリンクのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="f82d5-143">All other roles will only see the configured links after the **Enable this link** option is set to **Yes**.</span></span> <span data-ttu-id="f82d5-144">リンクが表示されるページにアクセスできる従業員は、このリンクにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="f82d5-144">Employees who have access to the pages in which the links are surfaced will have access to the links.</span></span>

<span data-ttu-id="f82d5-145">ユーザーには、Finance and Operations のページにアクセスするために定義された Finance and Operations 内でのセキュリティ権限もあります。</span><span class="sxs-lookup"><span data-stu-id="f82d5-145">Users can also have security rights within Finance and Operations defined to access the pages in Finance and Operations.</span></span> <span data-ttu-id="f82d5-146">そうでない場合、リンクを使用する時に、セキュリティ ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f82d5-146">If they don't, a security dialog box will be displayed when using the link.</span></span>


## <a name="other-changesfixes"></a><span data-ttu-id="f82d5-147">その他の変更または修正</span><span class="sxs-lookup"><span data-stu-id="f82d5-147">Other changes/fixes</span></span>

### <a name="positions-with-a-future-start-date-cannot-be-assigned-to-a-new-employee"></a><span data-ttu-id="f82d5-148">将来の開始日を持つ職位は、新しい従業員に割り当てることができません。</span><span class="sxs-lookup"><span data-stu-id="f82d5-148">Positions with a future start date cannot be assigned to a new employee</span></span>

<span data-ttu-id="f82d5-149">従業員が将来の日付に設定された職位に割り当てられるように、変更が行われました。</span><span class="sxs-lookup"><span data-stu-id="f82d5-149">Changes have been made to allow employee assignments to future-dated positions.</span></span> <span data-ttu-id="f82d5-150">将来の開始日が設定された職位を選択することができ、ワークフローの保存または完了において従業員の割り当てができます (ワークフローが有効の場合)。</span><span class="sxs-lookup"><span data-stu-id="f82d5-150">Positions that have start dates in the future can be selected and the employee assignment will be made upon save or completion of the workflow (if the workflow is enabled).</span></span>

### <a name="new-employee-cannot-be-assigned-existing-position"></a><span data-ttu-id="f82d5-151">新しい従業員は既存の職位に割り当てることができません。</span><span class="sxs-lookup"><span data-stu-id="f82d5-151">New employee cannot be assigned existing position</span></span>

<span data-ttu-id="f82d5-152">新しい従業員の割り当てが既存の職位に割り当てられるように、変更が行われました。</span><span class="sxs-lookup"><span data-stu-id="f82d5-152">Changes have been made so new employee assignment can now be assigned to existing positions.</span></span>

### <a name="seniority-dateoffice-location-disappears-when-the-employment-start-date-is-in-the-past-and-the-record-is-saved"></a><span data-ttu-id="f82d5-153">従業員の開始日が過去の日付でレコードが保存されている場合、勤続年数または職場の場所は表示されなくなります</span><span class="sxs-lookup"><span data-stu-id="f82d5-153">Seniority date/Office location disappears when the employment start date is in the past and the record is saved</span></span>

<span data-ttu-id="f82d5-154">過去の従業員について変更を保存する場合、**勤続日数**および**職場の場所**の可視を修正できるように、変更が行われました。</span><span class="sxs-lookup"><span data-stu-id="f82d5-154">Changes have been made to correct the visibilty of the **Senority date** and **Office location** when saving changes for past employees.</span></span>

### <a name="cant-enter-data-for-future-dated-employments-on-the-worker-page"></a><span data-ttu-id="f82d5-155">作業者ページにおいて、将来の日付の雇用にデータを入力することはできません</span><span class="sxs-lookup"><span data-stu-id="f82d5-155">Can't enter data for future-dated employments on the worker page</span></span>

<span data-ttu-id="f82d5-156">将来の日付の雇用に対する雇用データは、作業者のメイン ページでは無効にされています。</span><span class="sxs-lookup"><span data-stu-id="f82d5-156">Employment data for future-dated employments has been disabled on the main worker page.</span></span> <span data-ttu-id="f82d5-157">雇用データは、**日付マネージャー**のページを通じて入力できます。</span><span class="sxs-lookup"><span data-stu-id="f82d5-157">Employment data can be entered through the **Date Manager** pages.</span></span> <span data-ttu-id="f82d5-158">ワークフロー プロセス中の雇用データの直接入力を有効にできるように、将来のリリースで追加の変更が行われます。</span><span class="sxs-lookup"><span data-stu-id="f82d5-158">Additional changes will be made in future releases to enable entering employment data directly during the workflow process.</span></span>

### <a name="add-validfrom-and-validto-to-hcmpersonalcontactpersonentity"></a><span data-ttu-id="f82d5-159">HcmPersonalContactPersonEntity への ValidFrom および ValidTo の追加</span><span class="sxs-lookup"><span data-stu-id="f82d5-159">Add ValidFrom and ValidTo to HcmPersonalContactPersonEntity</span></span>

<span data-ttu-id="f82d5-160">特定の給付金統合シナリオを有効にするために「発効日」および「失効日」を日付に含められるよう、Data Management Framework (DMF) エンティティの HcmPersonalContactPersonEntity が更新されました。</span><span class="sxs-lookup"><span data-stu-id="f82d5-160">The Data Management Framework (DMF) entity HcmPersonalContactPersonEntity has been updated to include "valid from" and "valid to" dates to enable certain benefit integration scenarios.</span></span> 

## <a name="known-issue"></a><span data-ttu-id="f82d5-161">既知の問題</span><span class="sxs-lookup"><span data-stu-id="f82d5-161">Known issue</span></span>
- <span data-ttu-id="f82d5-162">**問題**: 作業者に新しい添付ファイルを追加する時、**新規**および**編集**ボタンが灰色表示になります。</span><span class="sxs-lookup"><span data-stu-id="f82d5-162">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="f82d5-163">**回避策:** 添付ファイル ページを開く前に、**作業者**ページの Factbox が閉じていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f82d5-163">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="f82d5-164">**作業者**ページが読み込まれる時、FactBoxes が閉じている場合には、添付ファイルボタンが有効になります。</span><span class="sxs-lookup"><span data-stu-id="f82d5-164">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="f82d5-165">(この問題は次のプラットフォーム更新プログラムで修正されます。)</span><span class="sxs-lookup"><span data-stu-id="f82d5-165">(This issue will be fixed in the next platform update.)</span></span>
