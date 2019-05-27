---
title: ルックアップ コントロール
description: この記事では、コントロールの検索動作を有効にする方法について説明します。 また、複数選択ルックアップを作成する方法について説明し、現在サポートされていないルックアップ シナリオの概要について説明します。
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 17464
ms.assetid: 1c71ebac-47c3-4c7e-bb48-a1c45619c95e
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cf7ad620f492bb4ab8793d10b0e62e1df6231964
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537120"
---
# <a name="lookup-controls"></a><span data-ttu-id="5f7c0-104">ルックアップ コントロール</span><span class="sxs-lookup"><span data-stu-id="5f7c0-104">Lookup controls</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5f7c0-105">この記事では、コントロールの検索動作を有効にする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-105">This article discusses how to enable lookup behavior on controls.</span></span> <span data-ttu-id="5f7c0-106">また、複数選択ルックアップを作成する方法について説明し、現在サポートされていないルックアップ シナリオの概要について説明します。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-106">It also discusses how to create multi-select lookups and outlines lookup scenarios that are no longer supported.</span></span>

<a name="enabling-lookup-behavior-in-controls"></a><span data-ttu-id="5f7c0-107">コントロールのルックアップ動作を有効化</span><span class="sxs-lookup"><span data-stu-id="5f7c0-107">Enabling lookup behavior in controls</span></span>
------------------------------------

### <a name="controls-bound-to-an-extended-data-type"></a><span data-ttu-id="5f7c0-108">拡張データ型にバインドされたコントロール</span><span class="sxs-lookup"><span data-stu-id="5f7c0-108">Controls bound to an Extended Data Type</span></span>

<span data-ttu-id="5f7c0-109">拡張データ型プロパティ セット (実行中の FormDataSource が無い) を持つコントロールは、次の条件の下で検索を行います。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-109">Controls with their Extended Data Type property set (no FormDataSource in play) will have a lookup under the following conditions:</span></span>

1.  <span data-ttu-id="5f7c0-110">EDT にはそのテーブル リレーションまたはテーブルの参照ノードが設定されているかどうか。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-110">If the EDT has its Table Relations or Table References node populated.</span></span>
2.  <span data-ttu-id="5f7c0-111">FormHelp プロパティが設定されている場合、ルール \#1 を true に設定 (カスタム ルックアップ) する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-111">If the FormHelp property is set (custom lookup); doesn’t require rule \#1 to be true.</span></span>
3.  <span data-ttu-id="5f7c0-112">コントロールでルックアップまたは lookupReference が上書きされている場合。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-112">If the control has lookup or lookupReference overridden.</span></span> <span data-ttu-id="5f7c0-113">このルールは、完全な非連結コントロール (EDT、フィールド、またはデータ メソッドなし) にも適用されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-113">Note, this rule also applies to fully unbound controls (no EDT, field, or data method).</span></span> <span data-ttu-id="5f7c0-114">これには、registerOverrideMethod などの上書きも含まれます。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-114">This includes overrides via registerOverrideMethod and others.</span></span>

### <a name="controls-bound-to-a-form-data-source"></a><span data-ttu-id="5f7c0-115">フォーム データ ソースにバインドされたコントロール</span><span class="sxs-lookup"><span data-stu-id="5f7c0-115">Controls bound to a form data source</span></span>

<span data-ttu-id="5f7c0-116">データ ソースにバインドされたコントロールは、次の条件の下で検索されます。**フィールド バインド**</span><span class="sxs-lookup"><span data-stu-id="5f7c0-116">Controls that are bound to a data source will have a lookup under the following conditions: **Field bound**</span></span>

1.  <span data-ttu-id="5f7c0-117">"lookup" または "lookupReference" (参照コントロール) メソッドが上書きされます。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-117">“lookup” or “lookupReference” (Reference Controls) methods are overridden.</span></span>
    1.  <span data-ttu-id="5f7c0-118">FormDataSource フィールドでルックアップまたは lookupReference が上書きされている場合。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-118">If the FormDataSource field has lookup or lookupReference overridden.</span></span>
    2.  <span data-ttu-id="5f7c0-119">コントロールでルックアップまたは lookupReference が上書きされている場合。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-119">If the control has lookup or lookupReference overridden.</span></span>
        -   <span data-ttu-id="5f7c0-120">これには、registerOverrideMethod などの上書きも含まれます。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-120">This includes overrides via registerOverrideMethod and others.</span></span>

2.  <span data-ttu-id="5f7c0-121">このフィールドに EDT がある場合、「拡張データ型にバインドされたコントロール」セクションのルール \# が適用されます。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-121">If the field has an EDT, then rule \#2 from the "Controls bound to an Extended Data Type" section applies.</span></span>
3.  <span data-ttu-id="5f7c0-122">バインディング フィールドは、DBFGetRef ルールごとにリレーションをマップします。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-122">If the bound field maps to a relation per DBFGetRef rules.</span></span>
    1.  <span data-ttu-id="5f7c0-123">高レベルのルール。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-123">High level rules:</span></span>
        1.  <span data-ttu-id="5f7c0-124">フィールドを支持する EDT 関係が存在し、テーブル関係ノードが入力され、Ignore EDT Relations がフィールド上で false である場合、その関係が使用されます (ルックアップがある)。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-124">If there is an EDT relation backing the field, with the Table Relations node populated and Ignore EDT Relations is false on the field, the relation is used (has a lookup).</span></span>
        2.  <span data-ttu-id="5f7c0-125">フィールドに対してリレーション マッピングが使用され、任意の固定フィールド リンク条件が満たされている場合は、そのリレーションが使用されます (ルックアップがある)。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-125">If there is a relation mapping to the field and any fixed field link conditions are satisfied, the relation is used (has a lookup).</span></span>
            1.  <span data-ttu-id="5f7c0-126">検証は「はい」にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-126">Validate must be “Yes”.</span></span>

        3.  <span data-ttu-id="5f7c0-127">次の場合に発生する 移行された EDT 関係の特殊なケースに注意してください。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-127">Note the special case of migrated EDT relations which occur when:</span></span>
            1.  <span data-ttu-id="5f7c0-128">フィールドは、関係ノードが設定される EDT によってサポートされます。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-128">Field is backed by an EDT with the Relations node populated.</span></span>
            2.  <span data-ttu-id="5f7c0-129">フィールドは、「EDTRelation」設定を「はい」にするテーブル関係によってサポートされます。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-129">Field is backed by a TABLE relation with the “EDTRelation” set to Yes.</span></span>
            3.  <span data-ttu-id="5f7c0-130">テーブル関係リンクは SourceEDT が適切な EDT に設定されています。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-130">The table relation link has the SourceEDT set to the appropriate EDT.</span></span>

        4.  <span data-ttu-id="5f7c0-131">また、IgnoreEDTRelation がフィールド上で true にセットされているケースを持つことができます。このケースでは、このセクションのルール \#3.1.2 が true である場合にのみルックアップが発生します。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-131">You can also have cases where IgnoreEDTRelation is set to true on a field, in which case a lookup will occur only if rule \#3.1.2 of this section is true.</span></span>

<span data-ttu-id="5f7c0-132">**データ メソッド バインド**</span><span class="sxs-lookup"><span data-stu-id="5f7c0-132">**Data method bound**</span></span>

1.  <span data-ttu-id="5f7c0-133">データ メソッドの戻り値が EDT である場合、「拡張データ型にバインドされたコントロール」セクションのルール \#1 と \# が適用されます。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-133">If the return type of the data method is an EDT, then rules \#1 and \#2 from the "Controls bound to an Extended Data Type" section apply.</span></span>
2.  <span data-ttu-id="5f7c0-134">コントロールでルックアップまたは lookupReference が上書きされている場合。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-134">If the control has lookup or lookupReference overridden.</span></span>
    -   <span data-ttu-id="5f7c0-135">これには、registerOverrideMethod を使用した上書きも含まれます。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-135">This includes overrides by using registerOverrideMethod.</span></span>

## <a name="multiselect-lookups"></a><span data-ttu-id="5f7c0-136">複数選択のルックアップ</span><span class="sxs-lookup"><span data-stu-id="5f7c0-136">Multiselect lookups</span></span>
### <a name="available-system-forms-for-building-multi-select-lookups"></a><span data-ttu-id="5f7c0-137">複数選択ルックアップを構築するために利用可能なシステム フォーム</span><span class="sxs-lookup"><span data-stu-id="5f7c0-137">Available system forms for building multi-select lookups</span></span>

<span data-ttu-id="5f7c0-138">現在、複数選択ルックアップを作成するためのシステム フォームが 2 つあります。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-138">There are currently two system forms for creating multi-select lookups:</span></span>

-   <span data-ttu-id="5f7c0-139">SysLookup: 列挙に基づいて複数選択します。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-139">SysLookup – Multiselect based on an Enum.</span></span>
-   <span data-ttu-id="5f7c0-140">SysLookupMultiselectGrid: データの収集に基づいて複数選択します。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-140">SysLookupMultiselectGrid – Multiselect based on a collection of data.</span></span>

### <a name="what-happened-to-the-syslookupmultiselect-form"></a><span data-ttu-id="5f7c0-141">SysLookupMultiselect フォームの変更点とは</span><span class="sxs-lookup"><span data-stu-id="5f7c0-141">What happened to the SysLookupMultiselect form?</span></span>

<span data-ttu-id="5f7c0-142">SysLookupMultiselect は、Microsoft Dynamics AX 2012 で廃止の対象としてマークされ、削除されました。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-142">SysLookupMultiselect was marked for deprecation in Microsoft Dynamics AX 2012 and has been removed.</span></span> <span data-ttu-id="5f7c0-143">複数選択のルックアップ シナリオでこのフォームを使用する場合、SysLookupMultiselectGrid を使用するように移行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-143">Any use of this form for multiselect lookup scenarios should be migrated to use SysLookupMultiselectGrid.</span></span> <span data-ttu-id="5f7c0-144">例については、チュートリアル\_LookupMultiSelectGrid のフォームを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-144">For an example, see the form tutorial\_LookupMultiSelectGrid.</span></span>

## <a name="unsupported-lookup-scenarios"></a><span data-ttu-id="5f7c0-145">検索シナリオはサポートされていません</span><span class="sxs-lookup"><span data-stu-id="5f7c0-145">Unsupported lookup scenarios</span></span>
### <a name="creating-multiple-lookup-forms-when-the-lookup-button-is-used"></a><span data-ttu-id="5f7c0-146">ルックアップ ボタンが使用されているときの複数のルックアップ フォームを作成しています</span><span class="sxs-lookup"><span data-stu-id="5f7c0-146">Creating multiple lookup forms when the lookup button is used</span></span>

<span data-ttu-id="5f7c0-147">ルックアップ ボタンを使用して複数のルックアップ フォームを作成する場合にエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-147">An error may occur if you create multiple lookup forms when the lookup button is used.</span></span> <span data-ttu-id="5f7c0-148">たとえば、「ルックアップ」メソッドを上書きして新しいルックアップ フォームを作成しても、「スーパー」 (別のルックアップ フォームを作成します) も呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-148">For example, overriding the ‘lookup’ method and creating a new lookup form, but also calling ‘super’ (which will create another lookup form).</span></span>

### <a name="using-selectedcontrol-to-determine-which-control-is-hosting-a-lookup"></a><span data-ttu-id="5f7c0-149">SelectedControl() を使用してルックアップをホストしているコントロールを決定</span><span class="sxs-lookup"><span data-stu-id="5f7c0-149">Using SelectedControl() to determine which control is hosting a lookup</span></span>

<span data-ttu-id="5f7c0-150">ルックアップをホストしているコントロールを決定する SelectedControl() の使用はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-150">Using SelectedControl() to determine which control is hosting a lookup is unsupported.</span></span> <span data-ttu-id="5f7c0-151">場合によっては動作しますが、他の場合には失敗します。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-151">While it may work in some cases, it will fail in others.</span></span> <span data-ttu-id="5f7c0-152">たとえば、曖昧性解消ルックアップでは、コントロールを離れる行為は、曖昧性解消ルックアップをトリガーすることであるため、親フォーム上でコントロールは選択されていません。。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-152">For example, in disambiguation lookups, no control is selected on the parent form since the act of leaving the control is what triggers a disambiguation lookup.</span></span> <span data-ttu-id="5f7c0-153">SelectedControl() を使用する代わりに、ルックアップをホストしているコントロールを取得するいくつかの方法があります。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-153">As an alternative to using SelectedControl(), there are a few other ways to retrieve the control that is hosting the lookup:</span></span>
-   <span data-ttu-id="5f7c0-154">ルックアップ フォームの「selectTarget」を確認してください。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-154">Check the ‘selectTarget’ of the lookup form.</span></span>

        FormStringControl selectTarget = formRun.selectTarget();

-   <span data-ttu-id="5f7c0-155">ルックアップ フォーム引数の「callerFormControl」を確認してください。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-155">Check the ‘callerFormControl’ on the lookup form args.</span></span> <span data-ttu-id="5f7c0-156">SysTableLookup::getCallerControl(Args args) はその呼び出しをカプセル化することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-156">Note that SysTableLookup::getCallerControl(Args args) encapsulates that call.</span></span>

        FormStringControl argsCallerFormControl = args.callerFormControl();

<span data-ttu-id="5f7c0-157">ルックアップ フォーム インスタンスがカーネルによって自動的にスピン アップされる場合、selectTarget および callerFormControl が自動的に設定されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-157">Note that the selectTarget and callerFormControl will be set automatically if the lookup form instance is spun up automatically by the kernel.</span></span> <span data-ttu-id="5f7c0-158">フォーム インスタンスがアプリケーション コードで作成される場合、これらを次のように手動で設定できます。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-158">If the form instance is created in app code, these can be set manually as shown below.</span></span>
<span data-ttu-id="5f7c0-159">public void lookup() { Args args = new Args(formStr(<formName>)); args.caller(element); args.callerFormControl(this); FormRun formRun = classfactory.formRunClass(args); formRun.init(); this.performFormLookup(formRun); }</span><span class="sxs-lookup"><span data-stu-id="5f7c0-159">public void lookup() { Args args = new Args(formStr(<formName>)); args.caller(element); args.callerFormControl(this); FormRun formRun = classfactory.formRunClass(args); formRun.init(); this.performFormLookup(formRun); }</span></span>

### <a name="creating-a-slider-dialog-instead-of-a-lookup-form-when-the-lookup-button-is-used"></a><span data-ttu-id="5f7c0-160">ルックアップ ボタンを使用する際のスライダーのダイアログ (ルックアップ フォームの代わりに) を作成しています</span><span class="sxs-lookup"><span data-stu-id="5f7c0-160">Creating a slider dialog (instead of a lookup form) when the lookup button is used</span></span>

<span data-ttu-id="5f7c0-161">ルックアップ ボタンを使用すると、ルックアップ コントロールによってルックアップ フォームを開く必要があります (スライダー ダイアログまたはその他の種類のフォームではありません)。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-161">Lookup controls should open lookup forms when the lookup button is used (not slider dialogs or other kinds of forms).</span></span>  <span data-ttu-id="5f7c0-162">これの第 1 の理由は、製品の整合性を保つことです。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-162">The first reason for this is product consistency.</span></span> <span data-ttu-id="5f7c0-163">2 番目の重要な理由は、ルックアップからスライダー ダイアログを開くことは、ルックアップの新しい先行入力機能と互換性がないことです。</span><span class="sxs-lookup"><span data-stu-id="5f7c0-163">The second and more important reason is that opening a slider dialog from a lookup is incompatible with the new type-ahead feature in lookups.</span></span>



