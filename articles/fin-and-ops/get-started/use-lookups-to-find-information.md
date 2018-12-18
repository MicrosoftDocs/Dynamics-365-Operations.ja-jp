---
title: "ルックアップを使用して情報の検索"
description: "Microsoft Dynamics 365 for Finance and Operations では多数のフィールドに適切な修正または目的の値の検索が容易なルックアップがあります。 複数の拡張機能は、これらのコントロールの使用可能により、ユーザーにルックアップが表示されます。 このトピックでは、これらの新しいルックアップ機能について情報と、システムのルックアップから業務の使用を取得するために、必要な情報が表示されます。"
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 269934
ms.assetid: f20cbd2c-14e0-47e7-b351-8e60d3537f96
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: 0a0722f057c1613fdc03281ca68a90608a701aef
ms.contentlocale: ja-jp
ms.lasthandoff: 12/18/2018

---

# <a name="find-information-by-using-lookups"></a><span data-ttu-id="7435d-105">ルックアップを使用して情報の検索</span><span class="sxs-lookup"><span data-stu-id="7435d-105">Find information by using lookups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7435d-106">Microsoft Dynamics 365 for Finance and Operations では多数のフィールドに適切な修正または目的の値の検索が容易なルックアップがあります。</span><span class="sxs-lookup"><span data-stu-id="7435d-106">In Microsoft Dynamics 365 for Finance and Operations, many fields have lookups that can help you easily find the correct or desired value.</span></span> <span data-ttu-id="7435d-107">複数の拡張機能は、これらのコントロールの使用可能により、ユーザーにルックアップが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7435d-107">Several enhancements have been added to lookups that make these controls more usable and make users more productive.</span></span> <span data-ttu-id="7435d-108">このトピックでは、これらの新しいルックアップ機能について情報と、システムのルックアップから業務の使用を取得するために、必要な情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7435d-108">In this topic, you will learn about these new lookup features and will receive some helpful tips to get the optimal use out of lookups in the system.</span></span>

## <a name="responsive-lookups"></a><span data-ttu-id="7435d-109">関連するルックアップ</span><span class="sxs-lookup"><span data-stu-id="7435d-109">Responsive lookups</span></span>

<span data-ttu-id="7435d-110">Finance and Operations の以前のバージョンでは、ルックアップ制御と連携している場合、ユーザーがドロップダウンメニューを開き明示的アクションをとる必要があります。</span><span class="sxs-lookup"><span data-stu-id="7435d-110">In previous versions of Finance and Operations, when interacting with a lookup control, a user would have to take an explicit action to open the drop-down menu.</span></span> <span data-ttu-id="7435d-111">これは、コントロールでアスタリスク (\*) を入力したり、またはドロップダウンボタンをクリックしたり、**Alt**+**下矢印** キーボード ショートカットを使用することで、コントロールの現在の値に基づいてルックアップをフィルター処理されている場合があります。</span><span class="sxs-lookup"><span data-stu-id="7435d-111">This may have been by typing an asterisk (\*) in the control to filter the lookup based on the current value of the control, clicking the drop-down button, or by using the **Alt**+**Down arrow** keyboard shortcut.</span></span> <span data-ttu-id="7435d-112">ルックアップ制御は、現在の Web 推奨事項に対応するために、次のように変更されました。</span><span class="sxs-lookup"><span data-stu-id="7435d-112">Lookup controls have been modified in the following ways to better align with current web practices:</span></span>

- <span data-ttu-id="7435d-113">ルックアップのドロップダウン メニューでは、入力時に少し一時停止して、ルックアップ制御の値に基づくフィルター処理されたドロップダウン メニューのコンテンツを自動的に開きます。</span><span class="sxs-lookup"><span data-stu-id="7435d-113">Lookup drop-down menus will now open automatically after a slight pause in typing, with the drop-down menu contents filtered based on the lookup control's value.</span></span>

    <span data-ttu-id="7435d-114">アスタリスク (\*) を入力した後、以前の動作であるドロップダウンの自動開始が使用されていないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="7435d-114">Note that the old behavior of automatic opening of the dropdown after typing an asterisk (\*) has been deprecated.</span></span>

- <span data-ttu-id="7435d-115">ルックアップのドロップダウン メニューを開くと、次の点が実行します。</span><span class="sxs-lookup"><span data-stu-id="7435d-115">After the lookup drop-down menu has opened, the following will occur:</span></span>

    - <span data-ttu-id="7435d-116">カーソル は(ドロップダウン メニュー に移動するフォーカスではなく) ルックアップコントロール によって制御の値に変更することができます。</span><span class="sxs-lookup"><span data-stu-id="7435d-116">The cursor will stay in the lookup control (instead of focus moving into the drop-down menu) so you can continue to make modifications to the control's value.</span></span> <span data-ttu-id="7435d-117">ただし、ユーザーは **上矢印** と **下矢印** を使用してドロップダウン メニューの行を変更し、Enter キーを使用してドロップダウン メニューの現在の行を選択することができます。</span><span class="sxs-lookup"><span data-stu-id="7435d-117">However, the user can still use the **Up arrow** and **Down arrow** to change rows in the drop-down menu, and enter to select the current row in the drop-down menu.</span></span>
    - <span data-ttu-id="7435d-118">ドロップダウン メニューの内容はルックアップ制御の値に変更が行われた後にも調整されます。</span><span class="sxs-lookup"><span data-stu-id="7435d-118">The contents of the drop-down menu will adjust after any modifications are made to the lookup control's value.</span></span>

<span data-ttu-id="7435d-119">たとえば、**市町村** と呼ばれるルックアップ フィールドについて検討します。</span><span class="sxs-lookup"><span data-stu-id="7435d-119">For example, consider a lookup field called **City**.</span></span>

<span data-ttu-id="7435d-120">**市町村** フィールドにフォーカスを置くと、「col」のように複数の文字を入力して目的の市町村の検索ができるようになります。</span><span class="sxs-lookup"><span data-stu-id="7435d-120">When focus is in the **City** field, you can start looking for the city that you want by typing a few letters, like "col."</span></span> <span data-ttu-id="7435d-121">入力後、「col」で始まる市町村がフィルタ処理されてルックアップが自動的に開きます。</span><span class="sxs-lookup"><span data-stu-id="7435d-121">After you stop typing, the lookup will open automatically, filtered to those cities that begin with "col".</span></span>

<span data-ttu-id="7435d-122">[![typeaheadLookupExample](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png)</span><span class="sxs-lookup"><span data-stu-id="7435d-122">[![typeaheadLookupExample](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png)</span></span>

<span data-ttu-id="7435d-123">この時点で、カーソルがまだルックアップ フィールド上にあります。</span><span class="sxs-lookup"><span data-stu-id="7435d-123">At this point, the cursor is still in the lookup field.</span></span> <span data-ttu-id="7435d-124">値を「colum」のように入力を続けると、ルックアップ コンテンツは自動的にコントロールの最新の値を反映するように調整されます。</span><span class="sxs-lookup"><span data-stu-id="7435d-124">If you continue typing so the value is "colum," the lookup contents adjust automatically to reflect the latest value in the control.</span></span>

![updateFilterLookupExample](./media/updatefilterlookupexample.png)

<span data-ttu-id="7435d-126">ルックアップ コントロールにフォーカスを置いてあっても、選択したい行を強調表示するために **上矢印** または **下矢印** キーを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="7435d-126">Even though focus is still in the lookup control, you can also use the **Up arrow** or **Down arrow** keys to highlight the row that you want to select.</span></span> <span data-ttu-id="7435d-127">**Enter** を押すと、強調表示された行がルックアップから選択され、コントロールの値が更新されます。</span><span class="sxs-lookup"><span data-stu-id="7435d-127">If you press **Enter** the highlighted row will be selected from the lookup and the control's value will be updated.</span></span>

![changingSelectionLookup](./media/changingselectionlookup.png)

## <a name="typing-in-more-than-ids"></a><span data-ttu-id="7435d-129">詳細 ID の入力</span><span class="sxs-lookup"><span data-stu-id="7435d-129">Typing in more than IDs</span></span>

<span data-ttu-id="7435d-130">データを入力するとき、ユーザーは大抵、エンティティを表す ID よりもむしろ、顧客または仕入先などの名前でエンティティを識別することを試みます。</span><span class="sxs-lookup"><span data-stu-id="7435d-130">When entering data, it's natural for users to attempt to identify an entity, such as a customer or vendor, in terms of the name rather than an identifier representing the entity.</span></span> <span data-ttu-id="7435d-131">Finance and Operations の現在のバージョンでは、多数の (全てではない) ルックアップは、コンテキストでのデータ入力ができます。</span><span class="sxs-lookup"><span data-stu-id="7435d-131">In the current version of Finance and Operations, many (but not all) lookups now allow contextual data entry.</span></span> <span data-ttu-id="7435d-132">この強力な機能によって、ユーザーがルックアップ 制御に対応する名前または ID を入力することもできます。</span><span class="sxs-lookup"><span data-stu-id="7435d-132">This powerful feature allows the user to type the ID or the corresponding name into the lookup control.</span></span>

<span data-ttu-id="7435d-133">たとえば、販売注文の作成時に **顧客口座** フィールドを考慮します。</span><span class="sxs-lookup"><span data-stu-id="7435d-133">For example, consider the **Customer account** field when creating a sales order.</span></span> <span data-ttu-id="7435d-134">このフィールドは、顧客の **口座 ID** を表示しますが、ユーザーは「US-003」の代わりに、「Forest Wholesales」のような販売注文を作成するとき、通常は**口座 ID** よりも **アカウント名** を入力します。</span><span class="sxs-lookup"><span data-stu-id="7435d-134">This field shows the **Account ID** for the customer, but a user would typically prefer to enter an **Account name** instead of an **Account ID** for this field when creating a sales order, such as "Forest Wholesales" instead of "US-003."</span></span>

<span data-ttu-id="7435d-135">ユーザーがルックアップ制御に **口座 ID** を入力し始めると、前のセクションで説明されている通りドロップダウンメニューが自動的に開き、ユーザーには次に表示されるようにルックアップが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7435d-135">If the user started to enter an **Account ID** into the lookup control, the drop-down menu would automatically open as described in the previous section and the user would see the lookup as shown below.</span></span>

<span data-ttu-id="7435d-136">[![顧客 ID が入力されたときのコンテキスト ルックアップ](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)</span><span class="sxs-lookup"><span data-stu-id="7435d-136">[![Contextual lookup when a customer account ID is entered](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)</span></span>

<span data-ttu-id="7435d-137">ただし、ユーザーは **口座名** を入力し始めることもできます。</span><span class="sxs-lookup"><span data-stu-id="7435d-137">However, the user can also now enter the beginning of an **Account name** as well.</span></span> <span data-ttu-id="7435d-138">これが検出された場合は、次のルックアップを表示します。</span><span class="sxs-lookup"><span data-stu-id="7435d-138">If this is detected, then the user will see the following lookup.</span></span> <span data-ttu-id="7435d-139">**名前** 列がルックアップの最初の列に移動する方法と、ルックアップが **名前** 列に基づいて並べ替えおよびフィルタ処理される方法に注意してください。</span><span class="sxs-lookup"><span data-stu-id="7435d-139">Notice how the **Name** column is moved to be the first column in the lookup, and how the lookup is sorted and filtered based on the **Name** column.</span></span>

<span data-ttu-id="7435d-140">[![顧客名が入力されるときのコンテキスト ルックアップ](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)</span><span class="sxs-lookup"><span data-stu-id="7435d-140">[![Contextual lookup when a customer name is entered](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)</span></span>

## <a name="using-grid-column-headers-for-more-advanced-filtering-and-sorting"></a><span data-ttu-id="7435d-141">より高度なフィルタおよび並べ替えのグリッド列ヘッダーを使用する</span><span class="sxs-lookup"><span data-stu-id="7435d-141">Using grid column headers for more advanced filtering and sorting</span></span>

<span data-ttu-id="7435d-142">前の 2 つのセクションで説明したルックアップの拡張機能は、ユーザーがルックアップの **ID** または **名前** フィールドで「Begins with」検索に基づいてルックアップの行を移動するのにとても役立ちます。</span><span class="sxs-lookup"><span data-stu-id="7435d-142">The lookup enhancements discussed in the previous two sections greatly improve a user's ability to navigate the rows in a lookup based on a "begins with" search of the **ID** or **Name** field in the lookup.</span></span> <span data-ttu-id="7435d-143">ただし、適切な行を検索するために、より高度なフィルタ処理をするか (または並べ替え) が必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="7435d-143">However, there are situations in which more advanced filtering (or sorting) is needed to find the correct row.</span></span> <span data-ttu-id="7435d-144">この場合、ユーザーはルックアップ内のグリッド列ヘッダーで、フィルター処理および並べ替えのオプションを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7435d-144">In these situations, the user needs to use the filtering and sorting options in the grid column headers inside the lookup.</span></span> <span data-ttu-id="7435d-145">たとえば、製品として正しい「ケーブル」を指定する必要がある販売注文明細行を入力する従業員について考えます。</span><span class="sxs-lookup"><span data-stu-id="7435d-145">For example, consider an employee entering a sales order line who needs to locate the right "cable" as the product.</span></span> <span data-ttu-id="7435d-146">「ケーブル」から始まる製品名がないため、**品目番号** 管理に「ケーブル」を入力しても役立ちません。</span><span class="sxs-lookup"><span data-stu-id="7435d-146">Typing "cable" into the **Item number** control isn't helpful, as there are no product names that begin with "cable."</span></span>

![emptyitemlookup](./media/emptyitemlookup.png)

<span data-ttu-id="7435d-148">これに代わる方法として、ユーザーはルックアップ コントロールの値をオフにして、ルックアップのドロップダウンメニューを開き、次に示すようにグリッド列ヘッダーを使用して、ドロップダウン メニューをフィルタリングします。</span><span class="sxs-lookup"><span data-stu-id="7435d-148">Instead, the user needs to clear the value of the lookup control, open the lookup drop-down menu, and filter the drop-down menu using the grid column header, as shown below.</span></span> <span data-ttu-id="7435d-149">マウス (またはタッチ) ユーザーはその列のフィルタリングおよび並べ替えのオプションにアクセスするために、任意の列ヘッダーをクリック (またはタッチ) します。</span><span class="sxs-lookup"><span data-stu-id="7435d-149">A mouse (or touch) user can simply click (or touch) any column header to access the filtering and sorting options for that column.</span></span> <span data-ttu-id="7435d-150">キーボードユーザーの場合、ドロップダウン メニューにフォーカスを移動するために **Alt**+**↓** **矢印** を 2 回目に押し、正しい列にタブした後に、**Ctrl**+**G** を押して、グリッド列のヘッダーのドロップダウン メニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="7435d-150">For a keyboard user, the user simply needs to press **Alt**+**Down** **arrow** a second time to move focus into the drop-down menu, after which the user can tab to the correct column, and then press **Ctrl**+**G** to open the grid column header drop-down menu.</span></span>

<span data-ttu-id="7435d-151">[![gridfilteritemlookup](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png)</span><span class="sxs-lookup"><span data-stu-id="7435d-151">[![gridfilteritemlookup](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png)</span></span>

<span data-ttu-id="7435d-152">フィルターが適用された後 (以下の画像を参照)、ユーザーは通常通り行を検索して選択できます。</span><span class="sxs-lookup"><span data-stu-id="7435d-152">After the filter has been applied (see the image below), the user can find and select the row as usual.</span></span>

![filtereditemlookup](./media/filtereditemlookup.png)

