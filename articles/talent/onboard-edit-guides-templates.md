---
title: Dynamics 365 Talent - Onboard で研修用ガイドとテンプレートの編集
description: このトピックでは、Microsoft Dynamics 365 Talent - Onboard の研修用ガイドおよびテンプレートに、活動やその他の情報を追加する方法について説明します。
author: andreabichsel
manager: ''
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 7803c7cd2c58b8544d2c8dd711c295d6882f9fca
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/23/2019
ms.locfileid: "2010801"
---
# <a name="edit-onboarding-guides-and-templates"></a><span data-ttu-id="c11ed-103">研修用ガイドとテンプレートの編集</span><span class="sxs-lookup"><span data-stu-id="c11ed-103">Edit onboarding guides and templates</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c11ed-104">Microsoft Dynamics 365 Talent: Onboard で研修用ガイドまたはテンプレートを作成した後、概要、活動、連絡先、およびリソースを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c11ed-104">After you create an onboarding guide or template in Microsoft Dynamics 365 Talent: Onboard, you must add an introduction, activities, contacts, and resources.</span></span> <span data-ttu-id="c11ed-105">研修用ガイドには、次の豊富な内容を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="c11ed-105">Onboard lets you include rich content in your onboarding guides, including:</span></span>

- <span data-ttu-id="c11ed-106">YouTube ビデオ</span><span class="sxs-lookup"><span data-stu-id="c11ed-106">YouTube videos</span></span>
- <span data-ttu-id="c11ed-107">Microsoft Sway プレゼンテーション</span><span class="sxs-lookup"><span data-stu-id="c11ed-107">Microsoft Sway presentations</span></span>
- <span data-ttu-id="c11ed-108">Microsoft PowerApps アプリ</span><span class="sxs-lookup"><span data-stu-id="c11ed-108">Microsoft PowerApps apps</span></span>
- <span data-ttu-id="c11ed-109">Microsoft Stream ビデオ</span><span class="sxs-lookup"><span data-stu-id="c11ed-109">Microsoft Stream videos</span></span>
- <span data-ttu-id="c11ed-110">Microsoft Forms フォーム</span><span class="sxs-lookup"><span data-stu-id="c11ed-110">Microsoft Forms forms</span></span>
- <span data-ttu-id="c11ed-111">Web コンテンツを含む iframe</span><span class="sxs-lookup"><span data-stu-id="c11ed-111">Iframes that contains web content</span></span>

## <a name="edit-introductions-or-activities-imported-from-a-template"></a><span data-ttu-id="c11ed-112">テンプレートからインポートされた概要または活動の編集</span><span class="sxs-lookup"><span data-stu-id="c11ed-112">Edit introductions or activities imported from a template</span></span>

<span data-ttu-id="c11ed-113">テンプレートからの研修用ガイドを作成した場合、または 1 つのテンプレートから別のテンプレートに活動をインポートした場合、インポートした活動に**ロック** ボタンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c11ed-113">If you create an onboarding guide from a template, or if you import activities from one template into another, you'll notice a **Lock** button on the imported activities.</span></span> <span data-ttu-id="c11ed-114">これらは*管理型活動*と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="c11ed-114">These are called *managed activities*.</span></span>

<span data-ttu-id="c11ed-115">[![管理型活動](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)</span><span class="sxs-lookup"><span data-stu-id="c11ed-115">[![Managed activities](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)</span></span>

<span data-ttu-id="c11ed-116">管理型活動を選択すると、ソース テンプレートが活動の上部に表示されます。</span><span class="sxs-lookup"><span data-stu-id="c11ed-116">When you select a managed activity, you can see the source template at the top of the activity.</span></span>

<span data-ttu-id="c11ed-117">[![管理型活動ソース](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)</span><span class="sxs-lookup"><span data-stu-id="c11ed-117">[![Managed activity source](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)</span></span>

<span data-ttu-id="c11ed-118">テンプレートの活動を編集すると、Onboard ではそのテンプレートに基づくすべてのテンプレートおよび未送信ガイドへの変更がプッシュされます。</span><span class="sxs-lookup"><span data-stu-id="c11ed-118">If you edit an activity in a template, Onboard will push the changes to all templates and unsent guides that are based on that template.</span></span> <span data-ttu-id="c11ed-119">編集したテンプレートに基づいて未送信ガイドを選択してから、ガイドの**活動**タブを選択すると、ガイドが変更されたことを示す通知が表示されます。</span><span class="sxs-lookup"><span data-stu-id="c11ed-119">If you select an unsent guide based on a template you edited and then select the **Activities** tab in the guide, you will see a notice that your guide has changed.</span></span> <span data-ttu-id="c11ed-120">通知を閉じるには、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-120">To dismiss the notification, select **OK**.</span></span> 

<span data-ttu-id="c11ed-121">[![変更通知](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)</span><span class="sxs-lookup"><span data-stu-id="c11ed-121">[![Change notification](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)</span></span>

<span data-ttu-id="c11ed-122">更新された活動の横に黒いドットが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c11ed-122">You'll see a black dot next to the updated activities.</span></span>

<span data-ttu-id="c11ed-123">[![変更済の活動](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)</span><span class="sxs-lookup"><span data-stu-id="c11ed-123">[![Changed activity](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)</span></span>

<span data-ttu-id="c11ed-124">活動の右側のセクションで割り当て対象者、期日、またはその他の情報を追加する場合を除いて、元のテンプレート外で管理型活動を編集することはできません。</span><span class="sxs-lookup"><span data-stu-id="c11ed-124">You can't edit managed activities outside of the original template, except to add an assignee, due date, or other information in the right-hand section of the activity.</span></span>

<span data-ttu-id="c11ed-125">管理型活動を編集する場合や、または活動が元のテンプレートから更新を受信しないようにする場合は、その活動の**ロック** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-125">If you want to edit a managed activity, or if you don't want an activity to receive updates from the template it came from, select the **Lock** button for that activity.</span></span> <span data-ttu-id="c11ed-126">**ロック** ボタンが表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="c11ed-126">The **Lock** button will disappear.</span></span> <span data-ttu-id="c11ed-127">活動は元のテンプレートにより管理されなくなり、そのテンプレートから更新を受け取ることができなくなります。</span><span class="sxs-lookup"><span data-stu-id="c11ed-127">The activity will no longer be managed by the original template, and it will no longer receive updates from that template.</span></span> <span data-ttu-id="c11ed-128">活動に対して行った更新は、元のテンプレートには影響しません。</span><span class="sxs-lookup"><span data-stu-id="c11ed-128">Updates you make to an activity do not affect the original template.</span></span>

<span data-ttu-id="c11ed-129">ガイドから活動を削除して、そのガイドのテンプレートから変更をプッシュすると、活動はガイドから削除されたままになります。</span><span class="sxs-lookup"><span data-stu-id="c11ed-129">If you delete an activity from a guide and push changes from that guide's template, the activity will remain deleted in the guide.</span></span>

> [!NOTE]
> <span data-ttu-id="c11ed-130">連絡先およびリソースは、テンプレートによって管理されていません。</span><span class="sxs-lookup"><span data-stu-id="c11ed-130">Contacts and resources aren't managed by templates.</span></span> <span data-ttu-id="c11ed-131">さらに、セクションは管理されていないため、テンプレートのセクションを追加または編集しても、そのテンプレートを使用するガイドやテンプレートに変更がプッシュされることはありません。</span><span class="sxs-lookup"><span data-stu-id="c11ed-131">In addition, sections aren't managed, so if you add or edit a section in a template, the changes won't be pushed to any guides or templates that use that template.</span></span>
> 
> <span data-ttu-id="c11ed-132">新しい活動をテンプレートに追加すると、新しい活動はそのテンプレートに基づいてガイドおよびテンプレートにプッシュされ、新しい活動が上部に表示されます。</span><span class="sxs-lookup"><span data-stu-id="c11ed-132">If you add new activities to a template, the new activities are pushed to guides and templates based on that template, and the new activities display at the top.</span></span>

## <a name="import-activities-from-another-template"></a><span data-ttu-id="c11ed-133">別のテンプレートからの活動のインポート</span><span class="sxs-lookup"><span data-stu-id="c11ed-133">Import activities from another template</span></span>

<span data-ttu-id="c11ed-134">1 つ以上のテンプレートからの活動をガイドまたはテンプレートにインポートできます。</span><span class="sxs-lookup"><span data-stu-id="c11ed-134">You can import activities from one or more templates into a guide or template.</span></span>

1. <span data-ttu-id="c11ed-135">編集するガイドまたはテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-135">Select the guide or template you want to edit.</span></span>

2. <span data-ttu-id="c11ed-136">**活動**タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-136">Select the **Activities** tab.</span></span>

3. <span data-ttu-id="c11ed-137">右側のセクションで、**インポート** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-137">Select the **Import** tab in the section on the right.</span></span>

   <span data-ttu-id="c11ed-138">[![活動のインポート](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)</span><span class="sxs-lookup"><span data-stu-id="c11ed-138">[![Import activities](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)</span></span>

4. <span data-ttu-id="c11ed-139">ブラウザーの新しいタブでタスクをプレビューするには、任意のテンプレートで**新しいタブで開く**ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-139">To preview the tasks in a new tab in your browser, select the **Open in new tab** button on any template.</span></span>

   <span data-ttu-id="c11ed-140">[![活動のインポート](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)</span><span class="sxs-lookup"><span data-stu-id="c11ed-140">[![Import activities](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)</span></span>

5. <span data-ttu-id="c11ed-141">目的のテンプレートを、ガイド テンプレート内の活動を表示する場所にドラッグ アンド ドロップします。</span><span class="sxs-lookup"><span data-stu-id="c11ed-141">Drag and drop the desired template to the place in your guide template where you want the activities to appear.</span></span> <span data-ttu-id="c11ed-142">ガイドまたはテンプレートの編集を続行します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-142">Continue editing your guide or template.</span></span>

<span data-ttu-id="c11ed-143">インポートされた活動には**ロック** ボタンが含まれており、これらの活動がインポートしたテンプレートによって管理されていることを示します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-143">The imported activities will contain a **Lock** button, which indicates those activities are managed by the template you imported from.</span></span> <span data-ttu-id="c11ed-144">インポートしたテンプレートに変更を加えると、それらの活動はインポートしたテンプレートで更新されます。</span><span class="sxs-lookup"><span data-stu-id="c11ed-144">When you make changes to the template you imported, those activities will update in the template you imported them to.</span></span> <span data-ttu-id="c11ed-145">ただし、インポートしたテンプレートから作成された任意のガイドに対しては、変更が自動的にプッシュされることはありません。</span><span class="sxs-lookup"><span data-stu-id="c11ed-145">However, the changes will not be pushed automatically to any guides created from the template you imported to.</span></span>

## <a name="push-changes-from-a-template-to-other-templates-or-guides"></a><span data-ttu-id="c11ed-146">テンプレートから他のテンプレートまたはガイドへの変更のプッシュ</span><span class="sxs-lookup"><span data-stu-id="c11ed-146">Push changes from a template to other templates or guides</span></span>

<span data-ttu-id="c11ed-147">他のテンプレートまたはガイドで使用される活動を含むテンプレートを編集する場合、他のテンプレートまたはガイドで表示する場合の変更をプッシュする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c11ed-147">If you edit a template that contains activities that are used in other templates or guides, you must push the changes if you want them to appear in the other templates or guides.</span></span>

<span data-ttu-id="c11ed-148">テンプレートの活動が別のテンプレートまたはガイドで使用されているかどうか分からない場合は、**使用先**タブを選択してそれらの活動が表示される場所を表示します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-148">If you're not sure whether your template's activities are used in other templates or guides, select the **Used in** tab to view where those activities appear.</span></span>

   <span data-ttu-id="c11ed-149">[![ガイドおよびテンプレート活動の使用先の表示](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)</span><span class="sxs-lookup"><span data-stu-id="c11ed-149">[![View guides and templates activities are used in](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)</span></span>

<span data-ttu-id="c11ed-150">変更をプッシュするには:</span><span class="sxs-lookup"><span data-stu-id="c11ed-150">To push your changes:</span></span>

1. <span data-ttu-id="c11ed-151">**保存**ボタンを選択して変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-151">Save your changes by selecting the **Save** button.</span></span> <span data-ttu-id="c11ed-152">この操作を行わない場合、次の手順で変更を保存するかどうかを確認するメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c11ed-152">If you don't do this, you'll be prompted to save your changes in the next step.</span></span>

2. <span data-ttu-id="c11ed-153">**これらの変更をプッシュする**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-153">Select **Push these changes**.</span></span>

   
## <a name="add-or-edit-an-introduction"></a><span data-ttu-id="c11ed-154">概要の追加または編集</span><span class="sxs-lookup"><span data-stu-id="c11ed-154">Add or edit an introduction</span></span>

1. <span data-ttu-id="c11ed-155">**概要**タブで、ガイドのタイトルと開始メッセージを入力します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-155">On the **Introduction** tab, enter a title for your guide and an opening message.</span></span> <span data-ttu-id="c11ed-156">サンプル テキストを使用するには、**このメッセージを使用する**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-156">To use the sample text, select **Use this message**.</span></span>

    <span data-ttu-id="c11ed-157">[![研修用テンプレートの概要タブ](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)</span><span class="sxs-lookup"><span data-stu-id="c11ed-157">[![Introduction tab in an Onboard template](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)</span></span>

2. <span data-ttu-id="c11ed-158">書式設定ボタンを使用して、必要に応じてテキストを呼び出したり、画像やリンクを追加したりできます。</span><span class="sxs-lookup"><span data-stu-id="c11ed-158">Use the formatting buttons to call out text as you require, or to add images or links.</span></span>
3. <span data-ttu-id="c11ed-159">**保存**を選択して作業内容を保存します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-159">Select **Save** to save your work.</span></span>

## <a name="add-or-edit-activities"></a><span data-ttu-id="c11ed-160">活動を追加または編集</span><span class="sxs-lookup"><span data-stu-id="c11ed-160">Add or edit activities</span></span>

1. <span data-ttu-id="c11ed-161">**活動**タブで、項目を右から編集領域にドラッグします。</span><span class="sxs-lookup"><span data-stu-id="c11ed-161">On the **Activities** tab, drag items from the right to the editing area.</span></span>
2. <span data-ttu-id="c11ed-162">ガイドをセクションに分けて整理するには、**新しいセクション**項目を編集領域にドラッグし、セクション名とオプションの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-162">To organize your guide into sections, drag the **New section** item to the editing area, and enter a name and an optional description for the section.</span></span>

    ![[<span data-ttu-id="c11ed-163">新しいセクションを研修用ガイドまたはテンプレートに追加する</span><span class="sxs-lookup"><span data-stu-id="c11ed-163">Adding a new section to an onboarding guide or template</span></span>](./media/onboard-edit-add-section.png)](./media/onboard-edit-add-section.png)

3. <span data-ttu-id="c11ed-164">新しい採用に対する活動を追加して完了するには、**新しい活動**項目を編集領域にドラッグし、活動の名前と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-164">To add activities for your new hire to complete, drag the **New activity** item to the editing area, and enter a name and description for the activity.</span></span>

    ![[<span data-ttu-id="c11ed-165">新しい活動を研修用ガイドまたはテンプレートに追加する</span><span class="sxs-lookup"><span data-stu-id="c11ed-165">Adding a new activity to an onboarding guide or template</span></span>](./media/onboard-edit-add-activity.png)](./media/onboard-edit-add-activity.png)

4. <span data-ttu-id="c11ed-166">豊富な内容を研修用ガイドに追加します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-166">Add rich content to your onboarding guide:</span></span>

    - <span data-ttu-id="c11ed-167">YouTube ビデオを追加するには、**YouTube** 項目を編集領域にドラッグし、活動の名前と説明を入力して、YouTube ビデオの URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-167">To add a YouTube video, drag the **YouTube** item to the editing area, enter a name and description for the activity, and enter the URL for the YouTube video.</span></span>
    - <span data-ttu-id="c11ed-168">Sway プレゼンテーションまたはニュースレターを追加するには、**Sway** 項目を編集領域にドラッグし、活動の名前と説明を入力して、Sway プレゼンテーションまたはニュースレターの埋め込み URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-168">To add a Sway presentation or newsletter, drag the **Sway** item to the editing area, enter a name and description for the activity, and enter the embedded URL for the Sway presentation or newsletter.</span></span>
    - <span data-ttu-id="c11ed-169">PowerApps アプリを追加するには、**PowerApps** 項目を編集領域にドラッグし、活動の名前と説明を入力して、PowerApps アプリを選択するか、または PowerApps アプリ ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-169">To add a PowerApps app, drag the **PowerApps** item to the editing area, enter a name and description for the activity, and either select the PowerApps app or enter the PowerApps app ID.</span></span>
    - <span data-ttu-id="c11ed-170">Microsoft Stream ビデオを追加するには、**Microsoft Stream** 項目を編集領域にドラッグし、活動の名前と説明を入力して、Microsoft Stream ビデオの URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-170">To add a Microsoft Stream video, drag the **Microsoft Stream** item to the editing area, enter a name and description for the activity, and enter the URL for the Microsoft Stream video.</span></span>
    - <span data-ttu-id="c11ed-171">Microsoft Forms フォームを追加するには、**Microsoft Forms** 項目を編集領域にドラッグし、活動の名前と説明を入力し、Microsoft Forms フォームの URL を入力して、画面領域のサイズを指定します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-171">To add a Microsoft Forms form, drag the **Microsoft Forms** item to the editing area, enter a name and description for the activity, enter the URL for the Microsoft Forms form, and specify the size of the screen area.</span></span>
    - <span data-ttu-id="c11ed-172">Web コンテンツを含む iframe を追加するには、**Web コンテンツ (iframe)** 項目を編集領域にドラッグし、活動の名前と説明を入力し、Web コンテンツの URL を入力して、画面領域のサイズを指定します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-172">To add an iframe that contains web content, drag the **Web Content (iframe)** item to the editing area, enter a name and description for the activity, enter the URL for the web content, and specify the size of the screen area.</span></span>

    ![[<span data-ttu-id="c11ed-173">豊富な内容を研修用ガイドまたはテンプレートに追加する</span><span class="sxs-lookup"><span data-stu-id="c11ed-173">Adding rich content to an onboarding guide or template</span></span>](./media/onboard-edit-add-rich-content.png)](./media/onboard-edit-add-rich-content.png)

2. <span data-ttu-id="c11ed-174">オプション: 各活動の右の領域で、活動を特定の個人またはロールに割り当て、期日と連絡担当者を追加し、カテゴリの色を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="c11ed-174">Optional: In the area on the right of each activity, assign the activity to a specific person or role, add a due date and contact person, and assign a category color.</span></span> <span data-ttu-id="c11ed-175">個人またはロールに活動を割り当てると、各個人に対してタスクが作成されます。</span><span class="sxs-lookup"><span data-stu-id="c11ed-175">When you assign an activity to a person or role, a task is created for each individual.</span></span> <span data-ttu-id="c11ed-176">このタスクは、Onboard の**タスク** メニューに表示されます。</span><span class="sxs-lookup"><span data-stu-id="c11ed-176">This task appears on the **Tasks** menu in Onboard.</span></span>

    <span data-ttu-id="c11ed-177">[![研修用ガイドまたはテンプレートで活動を割り当てる](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)</span><span class="sxs-lookup"><span data-stu-id="c11ed-177">[![Assigning an activity in an onboarding guide or template](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)</span></span>

3. <span data-ttu-id="c11ed-178">**保存**を選択して作業内容を保存します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-178">Select **Save** to save your work.</span></span>

<span data-ttu-id="c11ed-179">活動またはセクションを削除するには、活動またはセクションの右上隅にある**削除**ボタン (ゴミ箱記号) を選択します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-179">To delete an activity or section, select the **Delete** button (the trash can symbol) in the upper-right corner of the activity or section.</span></span>

<span data-ttu-id="c11ed-180">活動およびセクションを並べ替えるには、新しい場所に活動およびセクションをドラッグします。</span><span class="sxs-lookup"><span data-stu-id="c11ed-180">To rearrange activities and sections, drag them to a new location.</span></span>

## <a name="add-or-edit-contacts"></a><span data-ttu-id="c11ed-181">連絡先の追加または編集</span><span class="sxs-lookup"><span data-stu-id="c11ed-181">Add or edit contacts</span></span>

<span data-ttu-id="c11ed-182">初日から新しい採用の成功を支援できる連絡担当者を追加できます。</span><span class="sxs-lookup"><span data-stu-id="c11ed-182">You can add contact people who can help your new hire succeed from day one.</span></span> <span data-ttu-id="c11ed-183">これらの連絡先には、採用担当者、チームメート、先輩従業員、指導担当者、管理者、および IT サポート スタッフが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c11ed-183">These contacts can be recruiters, teammates, onboarding buddies, mentors, admins, and IT support staff.</span></span>

1. <span data-ttu-id="c11ed-184">**連絡先**タブで、**新しい連絡先**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-184">On the **Contacts** tab, select **New contact**.</span></span>
2. <span data-ttu-id="c11ed-185">**チーム メンバーの追加**ダイアログ ボックスで、連絡担当者の名前または電子メール アドレスを入力し、連絡担当者が新しい採用を支援する方法を示す簡単な説明を入力してから、**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-185">In the **Add team member** dialog box, enter the contact person's name or email address, enter a short description that explains how the contact person can help the new hire, and then select **Add**.</span></span> 

    ![[<span data-ttu-id="c11ed-186">連絡先を研修用ガイドまたはテンプレートに追加する</span><span class="sxs-lookup"><span data-stu-id="c11ed-186">Adding contacts to an onboarding guide or template</span></span>](./media/onboard-edit-add-contact.png)](./media/onboard-edit-add-contact.png)

    <span data-ttu-id="c11ed-187">別の方法として、1 つ以上の連絡先を**候補**から選択できます。</span><span class="sxs-lookup"><span data-stu-id="c11ed-187">Alternately, you can select one or more contacts under **Suggestions**.</span></span>

3. <span data-ttu-id="c11ed-188">**保存**を選択して作業内容を保存します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-188">Select **Save** to save your work.</span></span>

<span data-ttu-id="c11ed-189">連絡先を削除するには、連絡先の側にある**削除**ボタン (ごみ箱記号) を選択します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-189">To delete a contact, select the **Delete** button (the trash can symbol) to the right of the contact.</span></span>

<span data-ttu-id="c11ed-190">連絡先を編集するには、連絡先の右にある**編集**ボタン (鉛筆記号) を選択します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-190">To edit a contact, select the **Edit** button (the pencil symbol) to the right of the contact.</span></span>

## <a name="add-or-edit-resources"></a><span data-ttu-id="c11ed-191">リソースの追加または編集</span><span class="sxs-lookup"><span data-stu-id="c11ed-191">Add or edit resources</span></span>

<span data-ttu-id="c11ed-192">研修用ガイドの**リソース** セクションに、役立つファイル、マップ、およびリンクを追加できます。</span><span class="sxs-lookup"><span data-stu-id="c11ed-192">You can add useful files, maps, and links to the **Resources** section of your onboarding guide.</span></span>

1. <span data-ttu-id="c11ed-193">**リソース** タブで、**新しいリソース**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-193">On the **Resources** tab, select **New resource**.</span></span>
2. <span data-ttu-id="c11ed-194">次の手順のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-194">Follow one of these steps:</span></span>

    - <span data-ttu-id="c11ed-195">ファイルを追加するには、**ファイル** タブを選択し、指定した領域にファイルをドラッグします。</span><span class="sxs-lookup"><span data-stu-id="c11ed-195">To add a file, select the **File** tab, and drag the file into the designated area.</span></span> <span data-ttu-id="c11ed-196">(または、その領域内の任意の場所をクリックしてコンピュータ上のファイルを参照するか、または **OneDrive を参照**を選択します。) ファイルの名前を入力してから、**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c11ed-196">(Alternatively, click anywhere in that area to browse for the file on your computer, or select **Browse OneDrive**.) Enter a name for the file, and then select **Add**.</span></span>
    - <span data-ttu-id="c11ed-197">リンクを追加するには、**リンク** タブを選択し、リンクの名前と住所を入力してから、**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-197">To add a link, select the **Link** tab, enter a name and address for the link, and then select **Add**.</span></span>
    - <span data-ttu-id="c11ed-198">マップを追加するには、**マップ** タブを選択し、マップの名前と住所を入力してから、**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-198">To add a map, select the **Map** tab, enter a name and address for the map, and then select **Add**.</span></span> <span data-ttu-id="c11ed-199">Onboard には、指定するアドレスのマップが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c11ed-199">Onboard will include a map of the address that you specify.</span></span>

    ![[<span data-ttu-id="c11ed-200">リソースを研修用ガイドまたはテンプレートに追加する</span><span class="sxs-lookup"><span data-stu-id="c11ed-200">Adding a resource to an onboarding guide or template</span></span>](./media/onboard-edit-add-resource.png)](./media/onboard-edit-add-resource.png)

3. <span data-ttu-id="c11ed-201">**保存**を選択して作業内容を保存します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-201">Select **Save** to save your work.</span></span>

<span data-ttu-id="c11ed-202">リソースを削除するには、リソースの右にある**削除**ボタン (ごみ箱記号) を選択します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-202">To delete a resource, select the **Delete** button (the trash can symbol) to the right of the resource.</span></span>

<span data-ttu-id="c11ed-203">連絡先を編集するには、リソースの右にある**編集**ボタン (鉛筆記号) を選択します。</span><span class="sxs-lookup"><span data-stu-id="c11ed-203">To edit a contact, select the **Edit** button (the pencil symbol) to the right of the resource.</span></span>

## <a name="next-steps"></a><span data-ttu-id="c11ed-204">次のステップ</span><span class="sxs-lookup"><span data-stu-id="c11ed-204">Next steps</span></span>

- [<span data-ttu-id="c11ed-205">他の投稿者とコンテンツを共有する</span><span class="sxs-lookup"><span data-stu-id="c11ed-205">Share content with other contributors</span></span>](./onboard-share-template.md)
- [<span data-ttu-id="c11ed-206">タスクと研修中の従業員の状態の表示</span><span class="sxs-lookup"><span data-stu-id="c11ed-206">View the status of tasks and onboarding employees</span></span>](./onboard-view-status.md)
- [<span data-ttu-id="c11ed-207">Onboard での採用チームの作成</span><span class="sxs-lookup"><span data-stu-id="c11ed-207">Create hiring teams in Onboard</span></span>](./onboard-create-team.md)

### <a name="see-also"></a><span data-ttu-id="c11ed-208">参照</span><span class="sxs-lookup"><span data-stu-id="c11ed-208">See also</span></span>

- [<span data-ttu-id="c11ed-209">Onboard アプリを試すか購入する</span><span class="sxs-lookup"><span data-stu-id="c11ed-209">Try or buy the Onboard app</span></span>](https://dynamics.microsoft.com/talent/onboard/)
- [<span data-ttu-id="c11ed-210">新機能</span><span class="sxs-lookup"><span data-stu-id="c11ed-210">What's new</span></span>](./whats-new.md)
- [<span data-ttu-id="c11ed-211">リリース ノート</span><span class="sxs-lookup"><span data-stu-id="c11ed-211">Release notes</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="c11ed-212">サポートの利用</span><span class="sxs-lookup"><span data-stu-id="c11ed-212">Get support</span></span>](./talent-support.md)
