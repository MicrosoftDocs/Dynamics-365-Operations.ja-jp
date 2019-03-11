---
title: Microsoft Office で開くメニューのカスタマイズ
description: ほとんどのページには、Microsoft Office で開くメニューが含まれます。 このトピックでは、[Open in Office] メニューについての情報を提供し、オプションの追加、削除、変更によってカスタマイズする方法について説明します。
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 270774
ms.assetid: 3ff1184b-1a8a-4102-9600-f1776634d95f
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2017-02-28
ms.dyn365.ops.version: Platform update 4
ms.openlocfilehash: 6b9638418fcf964bf19724c7ef017f63d97a1f7e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368296"
---
# <a name="customize-the-open-in-microsoft-office-menu"></a><span data-ttu-id="1b8f6-104">Microsoft Office で開くメニューのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="1b8f6-104">Customize the Open in Microsoft Office menu</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1b8f6-105">ほとんどのページには、Microsoft Office で開くメニューが含まれます。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-105">Most pages include an Open in Microsoft Office menu.</span></span> <span data-ttu-id="1b8f6-106">このトピックでは、[Open in Office] メニューについての情報を提供し、オプションの追加、削除、変更によってカスタマイズする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-106">This topics provides information about the Open in Office menu, and explains how customize it by adding, removing, and changing options.</span></span>

<a name="overview"></a><span data-ttu-id="1b8f6-107">概要</span><span class="sxs-lookup"><span data-stu-id="1b8f6-107">Overview</span></span>
--------

<span data-ttu-id="1b8f6-108">**Microsoft Office で開く**メニュー ボタン (**Office で開く**メニュー) は、ページに表示されるシステム定義ボタンです。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-108">The **Open in Microsoft Office** menu button (**Open in Office** menu) is a system-defined button that appears on pages.</span></span> <span data-ttu-id="1b8f6-109">**Office で開く**メニューには、Microsoft Excel や Microsoft Word などのさまざまな Office 製品にデータをエクスポートできるようにするためのメニュー項目が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-109">The **Open in Office** menu contains menu items that let you export data to various Office products, such as Microsoft Excel and Microsoft Word.</span></span> <span data-ttu-id="1b8f6-110">次のテーブルは、**Office で開く** メニューのメニュー項目について説明しています。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-110">The following table describes the menu items on the **Open in Office** menu.</span></span>

| <span data-ttu-id="1b8f6-111">メニュー項目</span><span class="sxs-lookup"><span data-stu-id="1b8f6-111">Menu item</span></span>       | <span data-ttu-id="1b8f6-112">説明</span><span class="sxs-lookup"><span data-stu-id="1b8f6-112">Description</span></span>                                                                                                                                                                                                                                                  |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b8f6-113">Excel にエクスポート</span><span class="sxs-lookup"><span data-stu-id="1b8f6-113">Export to Excel</span></span> | <span data-ttu-id="1b8f6-114">データは Excel ワークブックにエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-114">The data is exported to an Excel workbook.</span></span> <span data-ttu-id="1b8f6-115">このブックには Microsoft Dynamics 365 for Finance and Operations への逆参照が含まれていないため、データを更新することはできません。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-115">The workbook contains no references back to Microsoft Dynamics 365 for Finance and Operations, and the data can't be refreshed.</span></span>                                                                                               |
| <span data-ttu-id="1b8f6-116">Word にエクスポート</span><span class="sxs-lookup"><span data-stu-id="1b8f6-116">Export to Word</span></span>  | <span data-ttu-id="1b8f6-117">データは Word 文書にエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-117">The data is exported to a Word document.</span></span> <span data-ttu-id="1b8f6-118">このドキュメントには、Finance and Operations の参照が含まれていないため、データを更新することはできません。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-118">The document contains no references back to Finance and Operations, and the data can't be refreshed.</span></span>                                                                                                           |
| <span data-ttu-id="1b8f6-119">Excel で開く</span><span class="sxs-lookup"><span data-stu-id="1b8f6-119">Open in Excel</span></span>   | <span data-ttu-id="1b8f6-120">Microsoft Dynamics Office アドインを含むブックが作成されます。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-120">A workbook is created that contains the Microsoft Dynamics Office add-in.</span></span> <span data-ttu-id="1b8f6-121">ワークブックには Finance and Operations の参照が含まれており、アドインでホストされているデータ コネクタからデータをリフレッシュ、更新、公開することができます。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-121">The workbook contains a reference back to Finance and Operations, and the data can be refreshed, updated, and published from the Data Connector that is hosted in the add-in.</span></span> |

## <a name="how-menu-items-are-added-to-the-open-in-office-menu"></a><span data-ttu-id="1b8f6-122">Office で開くメニューに、どのようにメニュー項目が追加されますか。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-122">How menu items are added to the Open in Office menu</span></span>
<span data-ttu-id="1b8f6-123">エクスポート オプションは、次の方法で **Office で開く** メニューに追加されます。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-123">The export options are added to the **Open in Office** menu in the following manner:</span></span>

1.  <span data-ttu-id="1b8f6-124">**Excel にエクスポート** グループで、メニュー項目が表示されている各グリッドに追加されます。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-124">In the **Export to Excel** group, a menu item is added for each visible grid.</span></span>
2.  <span data-ttu-id="1b8f6-125">ページのルート データ ソースごとに、同じルート データ ソースを持つ一連のデータ エンティティが決定されます。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-125">For each root data source on the page, the set of data entities that have the same root data source is determined.</span></span> <span data-ttu-id="1b8f6-126">これらの各データ エンティティについては、以下のメニュー項目が追加されます。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-126">For each of these data entities, the following menu items are added:</span></span>
    -   <span data-ttu-id="1b8f6-127">**Excel で開く**グループで、メニュー項目がデータ エンティティの既定のエクスポートに追加されます。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-127">In the **Open in Excel** group, a menu item is added for a default export of the data entity.</span></span>
    -   <span data-ttu-id="1b8f6-128">**Excel で開く**グループで、メニュー項目が同じルート データ エンティティを持つ **Excel** タイプのドキュメント テンプレート レコードごとに追加され、**Office で開く**メニューに含めるようマークされます。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-128">In the **Open in Excel** group, a menu item is added for each Document Template record of the **Excel** type that has the same root data entity and is marked for inclusion on the **Open in Office** menu.</span></span>
    -   <span data-ttu-id="1b8f6-129">**Word にエクスポート** グループで、メニュー項目が同じルート データ エンティティを持つ **Word** タイプのドキュメント テンプレート レコードごとに追加され、**Office で開く**メニューに含めるようマークされます。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-129">In the **Export to Word** group, a menu item is added for each Document Template record of the **Word** type that has the same root data entity and is marked for inclusion on the **Open in Office** menu.</span></span>

## <a name="default-exports"></a><span data-ttu-id="1b8f6-130">既定のエクスポート</span><span class="sxs-lookup"><span data-stu-id="1b8f6-130">Default exports</span></span>
<span data-ttu-id="1b8f6-131">**Office で開く** メニューは、各データ エンティティの既定のエクスポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-131">The **Open in Office** menu provides a default export for each data entity.</span></span> <span data-ttu-id="1b8f6-132">このエクスポートには、データ エンティティの **AutoReport** グループのすべてのフィールドが含まれます。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-132">This export includes all the fields in the **AutoReport** group on the data entity.</span></span> <span data-ttu-id="1b8f6-133">**SaveDataPerCompany**が**はい**に設定されている場合、現在の会社へのデータを制限するようフィルターが適用されます。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-133">If **SaveDataPerCompany** is set to **Yes** for the data entity, a filter is applied to limit the data to the current company.</span></span>

## <a name="document-templates"></a><span data-ttu-id="1b8f6-134">ドキュメント テンプレート</span><span class="sxs-lookup"><span data-stu-id="1b8f6-134">Document templates</span></span>
<span data-ttu-id="1b8f6-135">ドキュメント テンプレートは、**ドキュメント テンプレート**ページから追加できます。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-135">Document templates can be added from the **Document templates** page.</span></span> <span data-ttu-id="1b8f6-136">各ドキュメント テンプレート レコードに関連付けられているいくつかのフィールドは、**Office で開く** メニューでのそのテンプレートの動作を制御します。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-136">Several fields that are associated with each Document Template record control the behavior of that template on the **Open in Office** menu.</span></span>

| <span data-ttu-id="1b8f6-137">フィールド</span><span class="sxs-lookup"><span data-stu-id="1b8f6-137">Field</span></span>                | <span data-ttu-id="1b8f6-138">説明</span><span class="sxs-lookup"><span data-stu-id="1b8f6-138">Description</span></span>                                                                                                                                                         |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b8f6-139">ルート データ エンティティ</span><span class="sxs-lookup"><span data-stu-id="1b8f6-139">Root data entity</span></span>     | <span data-ttu-id="1b8f6-140">テンプレートのルート データ エンティティ。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-140">The root data entity of the template.</span></span> <span data-ttu-id="1b8f6-141">ルート データ エンティティは、テンプレートが含まれるページを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-141">The root data entity is used to determine which pages the template can be included on.</span></span>                                        |
| <span data-ttu-id="1b8f6-142">Office メニューのリスト</span><span class="sxs-lookup"><span data-stu-id="1b8f6-142">List in Office menu</span></span>  | <span data-ttu-id="1b8f6-143">このフィールドが選択されている場合に、テンプレートは該当するページの **Office で開く**メニューに含まれます。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-143">If this field is selected, the template will be included on the **Open in Office** menu on applicable pages.</span></span> <span data-ttu-id="1b8f6-144">(該当するページは、ルート データ エンティティによって異なります。)</span><span class="sxs-lookup"><span data-stu-id="1b8f6-144">(The applicable pages depend on the root data entity).</span></span> |
| <span data-ttu-id="1b8f6-145">レコード フィルターの適用</span><span class="sxs-lookup"><span data-stu-id="1b8f6-145">Apply record filter</span></span>  | <span data-ttu-id="1b8f6-146">このフィールドが選択されている場合、そのページで現在選択されているレコードをベースにデータがフィルター処理されます。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-146">If this field is selected, the data will be filtered, based on the record that is currently selected on the page.</span></span>                                                   |
| <span data-ttu-id="1b8f6-147">会社フィルターの適用</span><span class="sxs-lookup"><span data-stu-id="1b8f6-147">Apply company filter</span></span> | <span data-ttu-id="1b8f6-148">このフィールドが選択されている場合、現在の会社をベースにデータがフィルター処理されます。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-148">If this field is selected, the data will be filtered, based on the current company.</span></span>                                                                                 |

### <a name="trimmed-template-columns-and-fields"></a><span data-ttu-id="1b8f6-149">トリミングされたテンプレートの列とフィールド</span><span class="sxs-lookup"><span data-stu-id="1b8f6-149">Trimmed template columns and fields</span></span>

<span data-ttu-id="1b8f6-150">**Office で開く**メニューに含まれる Excel テンプレートで、列およびフィールドは、システムおよび該当する国/地域コンテキストに適用されているコンフィギュレーション キーに基づいて、ワークブックからトリミングされます。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-150">For Excel templates that are included on the **Open in Office** menu, columns and fields will be trimmed from the workbook, based on the configuration keys that are applied to the system and the applicable country/region context.</span></span> <span data-ttu-id="1b8f6-151">コンフィギュレーション キーがブック内の列またはフィールドに関連付けられている場合は、コンフィギュレーション キーが無効になっている場合は、列またはフィールドが削除されます。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-151">If a configuration key is associated with a column or field in the workbook, the column or field will be removed if the configuration key is disabled.</span></span> <span data-ttu-id="1b8f6-152">国/地域コードのセットがブックの列またはフィールドに関連付けられている場合、その国/地域コードが有効範囲にない場合は、列またはフィールドが削除されます。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-152">If a set of country/region codes is associated with the column or field in the workbook, the column or field will be removed if the country/region code isn't in scope.</span></span>

## <a name="open-in-office-menu-customization"></a><span data-ttu-id="1b8f6-153">「Office で開く」メニューのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="1b8f6-153">Open in Office menu customization</span></span>
<span data-ttu-id="1b8f6-154">特定のページの **Office で開** メニューに表示されるコンテンツをカスタマイズする方法はいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-154">There are several methods for customizing the content that appears on the **Open in Office** menu on a given page.</span></span> <span data-ttu-id="1b8f6-155">たとえば、モデル要素およびコード属性のメタデータ プロパティを通じて、静的にコンテンツをカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-155">For example, you can customize the content statically through metadata properties on model element and code attributes.</span></span> <span data-ttu-id="1b8f6-156">ただし、コード経由のカスタマイズによりコントロールの最高レベルを提供します。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-156">However, customization via code gives you the finest level of control.</span></span> <span data-ttu-id="1b8f6-157">コードでは、ページに 1 つまたは複数のインターフェイスを実装するか、拡張機能およびイベント サブスクリプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-157">In code, you can either implement one or more interfaces on a page, or use extensions and event subscriptions.</span></span> <span data-ttu-id="1b8f6-158">次のセクションでは、最も頻繁に使用されるカスタマイズ シナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-158">The following sections describe the customization scenarios that are most often used.</span></span>

### <a name="modifying-the-open-in-office-menu-through-interfaces"></a><span data-ttu-id="1b8f6-159">インターフェイスを通じた Office で開くメニューの変更</span><span class="sxs-lookup"><span data-stu-id="1b8f6-159">Modifying the Open in Office menu through interfaces</span></span>

<span data-ttu-id="1b8f6-160">自分の所有するページを変更する必要がある場合、のページのすべてのプライベート メンバーへのアクセス権を付与し、より深いカスタマイズが可能になるため、インターフェイスは最適なカスタマイズ方法となります。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-160">If you must modify a page that you own, interfaces are the most appropriate customization method, because they give access to all private members of the page and allow for deeper customization.</span></span> <span data-ttu-id="1b8f6-161">以下のインターフェイスをページのコードに適用することができます。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-161">You can apply the following interfaces to the code for a page.</span></span>

| <span data-ttu-id="1b8f6-162">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="1b8f6-162">Interface</span></span>                              | <span data-ttu-id="1b8f6-163">説明</span><span class="sxs-lookup"><span data-stu-id="1b8f6-163">Description</span></span>                                                                                                    |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b8f6-164">OfficeIMenuCustomizer</span><span class="sxs-lookup"><span data-stu-id="1b8f6-164">OfficeIMenuCustomizer</span></span>                  | <span data-ttu-id="1b8f6-165">ページと見なされるデータ エンティティのセットを変更し、カスタムのメニュー項目を追加するには、このインターフェイスを使用します。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-165">Use this interface to modify the set of data entities that is considered for a page and add custom menu items.</span></span> |
| <span data-ttu-id="1b8f6-166">OfficeIGeneratedWorkbookCustomExporter</span><span class="sxs-lookup"><span data-stu-id="1b8f6-166">OfficeIGeneratedWorkbookCustomExporter</span></span> | <span data-ttu-id="1b8f6-167">実行時に生成されるブックのカスタム エクスポートを行うには、このインターフェイスを使用します。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-167">Use this interface to do a custom export of a workbook that is generated at run time.</span></span>                          |
| <span data-ttu-id="1b8f6-168">OfficeITemplateCustomExporter</span><span class="sxs-lookup"><span data-stu-id="1b8f6-168">OfficeITemplateCustomExporter</span></span>          | <span data-ttu-id="1b8f6-169">ドキュメント テンプレートのレコードに基づくカスタムのエクスポートを行うには、このインターフェイスを使用します。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-169">Use this interface to do a custom export that is based on a Document Template record.</span></span>                          |

### <a name="modifying-the-open-in-office-menu-through-extensions-and-event-subscriptions"></a><span data-ttu-id="1b8f6-170">拡張機能とイベント サブスクリプションを通じた Office で開くメニューの変更</span><span class="sxs-lookup"><span data-stu-id="1b8f6-170">Modifying the Open in Office menu through extensions and event subscriptions</span></span>

<span data-ttu-id="1b8f6-171">所有していないページを変更する必要がある場合、オーバーレイが必要となるため、インターフェイスの使用を避ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-171">If you must modify a page that you don't own, you should avoid using interfaces, because that approach will require over-layering.</span></span> <span data-ttu-id="1b8f6-172">代わりに、拡張機能およびイベント サブスクリプションを通じてカスタマイズを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-172">Instead, you should do the customization through extensions and event subscriptions.</span></span> <span data-ttu-id="1b8f6-173">この方法を使用するには、カスタマイズするページの **OnIntializing** イベントにサブスクライブする拡張クラスを実装します。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-173">To use this approach, implement an extension class that subscribes to the **OnIntializing** event of the page that you're customizing.</span></span> <span data-ttu-id="1b8f6-174">このイベント ハンドラーから、ページの **OfficeFormRunHelper** を取得し、その **OfficeMenuInitializing** イベントにサブスクライブします。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-174">From this event handler, get the **OfficeFormRunHelper** for the page, and subscribe to its **OfficeMenuInitializing** event.</span></span> <span data-ttu-id="1b8f6-175">次の例は、この方法のサンプル コードを示しています。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-175">The following example shows sample code for this approach.</span></span>

    public static class MyForm_Extension
    {
        [FormEventHandler(formStr(MyForm), FormEventType::Initializing)]
        public static void ExportToExcel_DataEntityCustom_OnInitializing(xFormRun sender, FormEventArgs e)
        {
            FormRun formRun = sender as FormRun;
            if (formRun)
            {
                OfficeFormRunHelper officeHelper = formRun.officeHelper();
                if (officeHelper)
                {
                    officeHelper.OfficeMenuInitializing += eventhandler(MyForm_Extension::officeMenuInitializingHandler);
                }
            }
        }
        private static void officeMenuInitializingHandler(FormRun _formRun, OfficeMenuEventArgs _eventArgs)
        {
            // Modify the OfficeMenuOptions available on the OfficeMenuEventArgs.menuOptions() as necessary.
        }
    }

## <a name="typical-customization-scenarios"></a><span data-ttu-id="1b8f6-176">一般的なカスタマイズ シナリオ</span><span class="sxs-lookup"><span data-stu-id="1b8f6-176">Typical customization scenarios</span></span>
<span data-ttu-id="1b8f6-177">次の例では、**\_menuOptions** 変数に、カスタマイズしている **OfficeMenuOptions** インスタンスが含まれていると想定しています。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-177">The following examples assume that the **\_menuOptions** variable contains the **OfficeMenuOptions** instance that you're customizing.</span></span>

### <a name="modifying-the-set-of-data-entities-that-is-considered-for-a-page"></a><span data-ttu-id="1b8f6-178">ページで考慮されるデータ エンティティのセットの変更</span><span class="sxs-lookup"><span data-stu-id="1b8f6-178">Modifying the set of data entities that is considered for a page</span></span>

<span data-ttu-id="1b8f6-179">**Office で開く**メニューにあるメニュー項目の多くは、ページとみなされるデータ エンティティに基づいて自動的に追加されます。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-179">Many of the menu items on the **Open in Office** menu are added automatically, based on the data entities that are considered for the page.</span></span> <span data-ttu-id="1b8f6-180">ただし、場合によっては、データ エンティティのセットを特定するために使用されるアルゴリズムが、正しいセットを特定しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-180">However, in some cases, the algorithm that is used to determine the set of data entities might not determine the correct set.</span></span> <span data-ttu-id="1b8f6-181">ページと見なされるデータ エンティティのセットを変更するには、**OfficeIMenuCustomizer.customizeMenuOptions** メソッドまたは **OfficeFormRunHelper.OfficeMenuInitializing** デリゲートから利用可能な **OfficeMenuOptions** を使用します。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-181">To modify the set of data entities that is considered for the page, you can use the **OfficeMenuOptions** that is available from either the **OfficeIMenuCustomizer.customizeMenuOptions** method or the **OfficeFormRunHelper.OfficeMenuInitializing** delegate.</span></span>

    // Add an entity to the list
    OfficeMenuDataEntityOptions entityOptions  = OfficeMenuDataEntityOptions::construct(tableStr(MyEntity));
    _menuOptions.dataEntityOptions().addEnd(entityOptions);
    // Remove an entity from the list
    ListIterator dataEntityOptionsIterator = new ListIterator(_menuOptions.dataEntityOptions());
    while (dataEntityOptionsIterator.more())
    {
        OfficeMenuDataEntityOptions dataEntityOptions = dataEntityOptionsIterator.value();
        if (dataEntityOptions.dataEntityName() == tableStr(MyOtherEntity))
        {
            dataEntityOptionsIterator.delete();
        }
        else
        {
            dataEntityOptionsIterator.next();
        }
    }

### <a name="specifying-the-default-data-entityrelated-options-that-are-included"></a><span data-ttu-id="1b8f6-182">含まれている既定のデータ エンティティ関連のオプションを指定します。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-182">Specifying the default data entity–related options that are included</span></span>

<span data-ttu-id="1b8f6-183">**OfficeMenuDataEntityOptions** クラスを使用すると、既定のエクスポートのためのメニュー項目またはドキュメント テンプレートに関連するメニュー項目を含めるかどうかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-183">The **OfficeMenuDataEntityOptions** class lets you specify whether to include a menu item for a default export or a menu item that is related to a document template.</span></span>

    // Find the entity options if they were included by default.
    OfficeMenuDataEntityOptions entityOptions = _menuOptions.getOptionsForEntity(tableStr(MyEntity));
    if (!entityOptions)
    {
        // The entity options were not included. Add them.
        entityOptions = OfficeMenuDataEntityOptions::construct(tableStr(MyEntity);
        _menuOptions.dataEntityOptions().addEnd(entityOptions);
    }
    entityOptions.includeDefault(false); // Don't include the default export menu item.
    entityOptions.includeTemplates(false); // Don’t include Document Template related menu items.

### <a name="adding-a-custom-export-menu-item--generating-a-workbook"></a><span data-ttu-id="1b8f6-184">カスタム エクスポート メニュー項目の追加 – ブックの生成</span><span class="sxs-lookup"><span data-stu-id="1b8f6-184">Adding a custom export menu item – Generating a workbook</span></span>

<span data-ttu-id="1b8f6-185">明示的にメニュー項目を追加するには、それを **OfficeMenuOptions.customMenuItems()** リストに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-185">To explicitly add a menu item, you must add it to the **OfficeMenuOptions.customMenuItems()** list.</span></span> <span data-ttu-id="1b8f6-186">実行時に生成されるブックに対応するメニュー項目を追加するには、**OfficeGeneratedExportMenuItem** を使用します。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-186">To add a menu item that corresponds to a workbook that is generated at run time, use an **OfficeGeneratedExportMenuItem**.</span></span>

    OfficeGeneratedExportMenuItem menuItem = OfficeGeneratedExportMenuItem::construct(tableStr(MyEntity), "MyCustomGeneratedExportId");
    menuItem.setDisplayNameWithDataEntity();
    _menuOptions.customMenuItems().addEnd(menuItem);

<span data-ttu-id="1b8f6-187">実際にエクスポートする内容を定義するには、**ExportToExcelDataEntityContext** を使用します。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-187">To define what is actually exported, use an **ExportToExcelDataEntityContext**.</span></span> <span data-ttu-id="1b8f6-188">**ExportToExcelDataEntityContext** を指定するメソッドは、インターフェイスまたは拡張機能とイベント サブスクリプションを使用して、**Office で開く** メニューをカスタマイズするかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-188">The method for specifying the **ExportToExcelDataEntityContext** depends on whether you're using interfaces or extensions and event subscriptions to customize the **Open in Office** menu.</span></span>

#### <a name="using-interfaces"></a><span data-ttu-id="1b8f6-189">インターフェイスの使用</span><span class="sxs-lookup"><span data-stu-id="1b8f6-189">Using interfaces</span></span>

<span data-ttu-id="1b8f6-190">インターフェイスを使用している場合、**OfficeIGeneratedWorkbookCustomExporter.getDataEntityContext()** メソッドを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-190">If you're using interfaces, you must implement the **OfficeIGeneratedWorkbookCustomExporter.getDataEntityContext()** method.</span></span>

    public ExportToExcelDataEntityContext getDataEntityContext(OfficeGeneratedExportMenuItem _menuItem)
    {
        ExportToExcelDataEntityContext context = null;
        if (_menuItem.id() == "MyCustomGeneratedExportId")
        {
            context = ExportToExcelDataEntityContext::construct(tableStr(MyEntity), tableFieldGroupStr(MyEntity, MyFieldGroup);
        }
        return context;
    }

#### <a name="using-extensions-and-event-subscriptions"></a><span data-ttu-id="1b8f6-191">拡張機能とイベント サブスクリプションの使用</span><span class="sxs-lookup"><span data-stu-id="1b8f6-191">Using extensions and event subscriptions</span></span>

<span data-ttu-id="1b8f6-192">拡張機能とイベント サブスクリプションを使用している場合、**OfficeGeneratedExportMenuItem.getDataEntityContext** デリゲートはメニュー項目を **OfficeMenuOptions.customMenuItems()** リストに追加する前にサブスクライブする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-192">If you're using extensions and event subscriptions, the **OfficeGeneratedExportMenuItem.getDataEntityContext** delegate should be subscribed to before you add the menu item to the **OfficeMenuOptions.customMenuItems()** list.</span></span> <span data-ttu-id="1b8f6-193">イベント ハンドラーのコードは、インターフェイスの先行するコードと同様である必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-193">The code for the event handler should resemble the preceding code for the interface.</span></span> <span data-ttu-id="1b8f6-194">次の例は、イベント サブスクリプションの実行方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-194">The following example shows how to do the event subscription.</span></span>

    menuItem.getDataEntityContext += eventhandler(MyForm_Extension::getDataEntityContextHandler);

### <a name="adding-a-custom-export-menu-item--specifying-a-document-template"></a><span data-ttu-id="1b8f6-195">カスタム エクスポート メニュー項目の追加 – ドキュメント テンプレートの指定</span><span class="sxs-lookup"><span data-stu-id="1b8f6-195">Adding a custom export menu item – Specifying a document template</span></span>

<span data-ttu-id="1b8f6-196">明示的にメニュー項目を追加するには、それを **OfficeMenuOptions.customMenuItems()** リストに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-196">To explicitly add a menu item, you must add it to the **OfficeMenuOptions.customMenuItems()** list.</span></span> <span data-ttu-id="1b8f6-197">ドキュメント テンプレート レコードに対応するメニュー項目を追加するには、**OfficeTemplateExportMenuItem** を使用します。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-197">To add a menu item that corresponds to a Document Template record, use an **OfficeTemplateExportMenuItem**.</span></span>

    OfficeTemplateExportMenuItem menuItem = OfficeTemplateExportMenuItem::construct(OfficeAppApplicationType::Excel, "MyTemplateId", "MyCustomTemplateExportId");
    _menuOptions.customMenuItems().addEnd(menuItem);

<span data-ttu-id="1b8f6-198">実行時にテンプレートを変更するには、一連の初期フィルターを指定します。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-198">To modify the template at run time, you can supply a set of initial filters.</span></span> <span data-ttu-id="1b8f6-199">これらのフィルターは、指定されたデータ エンティティのテンプレート内のフィルターを置き換えます。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-199">These filters will replace any filters in the template for the specified data entities.</span></span> <span data-ttu-id="1b8f6-200">また、**WorkbookSettingsManager** を使用してフィルターを変更し、多くの設定を指定できます。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-200">Additionally, you can modify filters and specify many settings by using **WorkbookSettingsManager**.</span></span> <span data-ttu-id="1b8f6-201">次のセクションに例を示します。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-201">The following sections show examples.</span></span>

#### <a name="using-interfaces"></a><span data-ttu-id="1b8f6-202">インターフェイスの使用</span><span class="sxs-lookup"><span data-stu-id="1b8f6-202">Using interfaces</span></span>

<span data-ttu-id="1b8f6-203">インターフェイスを使用している場合、**OfficeITemplateCustomExporter.getInitialTemplateFilters()** および **OfficeITemplateCustomExporter.updateTemplateSettings()** メソッドを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-203">If you're using interfaces, you must implement the **OfficeITemplateCustomExporter.getInitialTemplateFilters()** and **OfficeITemplateCustomExporter.updateTemplateSettings()** methods.</span></span>

    public Map getInitialTemplateFilters(OfficeTemplateExportMenuItem _menuItem)
    {
        Map initialFilters = new Map(Types::String, Types::Class);
        if (_menuItem.id() == "MyCustomTemplateExportId")
        {
            // Add an initial filter.
            ExportToExcelFilterTreeBuilder bldr = new ExportToExcelFilterTreeBuilder(_menuItem.dataEntityName());
            FilterNode filter = // create the filter…
            initialFilters.insert(_menuItem.dataEntityName(), filter);
        }
        return initialFilters;
    }
    public void updateTemplateSettings(OfficeTemplateExportMenuItem _menuItem, Microsoft.Dynamics.Platform.Integration.Office.SettingsManager _settingsManager)
    {
        if (_menuItem.id() == "MyCustomTemplateExportId")
        {
            // Set a new filter.
            ExportToExcelFilterTreeBuilder bldr = new ExportToExcelFilterTreeBuilder(_menuItem.dataEntityName());
            FilterNode filter = // create the filter…
            Excel.WorkbookSettingsManager workbookSettingsManager = _settingsManager as Excel.WorkbookSettingsManager;
            workbookSettingsManager.SetEntityFilter(entityMetadata.PublicEntityName, filter);
            // Adjust settings.
            DataConnectorAppletSettings settings = settingsManager.DataConnectorSettings;
            DataConnectorAppletUserOptions options = settings.DataOptions;
            options.RefreshOnOpen = true;
            options.EnableDesign = false;
            workbookSettingsManager.DataConnectorSettings = settings;
        }
    }

#### <a name="using-extensions-and-event-subscriptions"></a><span data-ttu-id="1b8f6-204">拡張機能とイベント サブスクリプションの使用</span><span class="sxs-lookup"><span data-stu-id="1b8f6-204">Using extensions and event subscriptions</span></span>

<span data-ttu-id="1b8f6-205">拡張機能とイベント サブスクリプションを使用している場合、**OfficeTemplateExportMenuItem.getInitialTemplateFilters** および **OfficeTemplateExportMenuItem.updateTemplateSettings** デリゲートはメニュー項目を **OfficeMenuOptions.customMenuItems()** リストに追加する前にサブスクライブする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-205">If you're using extensions and event subscriptions, the **OfficeTemplateExportMenuItem.getInitialTemplateFilters** and **OfficeTemplateExportMenuItem.updateTemplateSettings** delegates should be subscribed to before you add the menu item to the **OfficeMenuOptions.customMenuItems()** list.</span></span> <span data-ttu-id="1b8f6-206">イベント ハンドラーのコードは、インターフェイスの先行するコードと同様である必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-206">The code for the event handlers should resemble the preceding code for the interface.</span></span> <span data-ttu-id="1b8f6-207">次の例は、イベント サブスクリプションの実行方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-207">The following example shows how to do the event subscription.</span></span>

    menuItem.getInitialTemplateFilters += eventhandler(MyForm_Extension::getInitialTemplateFiltersHander);
    menuItem.updateTemplateSettings += eventhandler(MyForm_Extension::updateTemplateSettingsHandler);

## <a name="additional-customizations"></a><span data-ttu-id="1b8f6-208">追加のカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="1b8f6-208">Additional customizations</span></span>
<span data-ttu-id="1b8f6-209">次のカスタマイズを使用すると、インターフェイス、拡張機能、およびイベント ハンドラーを使用せずに、**Office で開く** メニューの内容を変更できます。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-209">The following customizations let you modify the contents of the **Open in Office** menu for a page without using interfaces or extensions and event handlers.</span></span>

### <a name="removing-an-export-to-excel-menu-item-for-a-grid"></a><span data-ttu-id="1b8f6-210">グリッドの [Excel にエクスポート] メニュー項目を削除</span><span class="sxs-lookup"><span data-stu-id="1b8f6-210">Removing an Export to Excel menu item for a grid</span></span>

<span data-ttu-id="1b8f6-211">**Office で開く**メニューで、**Excel にエクスポート**グループには、表示されている各グリッドのメニュー項目が含まれます。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-211">On the **Open in Office** menu, the **Export to Excel** group will contain a menu item for each visible grid.</span></span> <span data-ttu-id="1b8f6-212">**Office で開く** メニューからグリッドを削除するには、グリッドの **ExportAllowed** メタデータ プロパティを **いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-212">To remove a grid from the **Open in Office** menu, set the **ExportAllowed** metadata property on the grid to **No**.</span></span> <span data-ttu-id="1b8f6-213">この変更を行なった後、ユーザーはグリッドのショートカット メニューを使用してグリッドをエクスポートすることはできません。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-213">After you make this change, users won't be able to export the grid by using the shortcut menu for the grid.</span></span>

### <a name="renaming-an-export-to-excel-menu-item-for-a-grid"></a><span data-ttu-id="1b8f6-214">グリッドの [Excel にエクスポート] メニュー項目を名前変更</span><span class="sxs-lookup"><span data-stu-id="1b8f6-214">Renaming an Export to Excel menu item for a grid</span></span>

<span data-ttu-id="1b8f6-215">グリッドに関連する **Excelにエクスポート** メニュー項目の名前を変更するには、グリッドの **ExportLabel** メタデータ プロパティを適切なラベルに設定します。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-215">To rename the **Export to Excel** menu item that is related to a grid, set the **ExportLabel** metadata property on the grid to the appropriate label.</span></span>

### <a name="removing-all-menu-items-for-a-data-entity-from-all-pages"></a><span data-ttu-id="1b8f6-216">すべてのページからデータ エンティティのすべてのメニュー項目を削除</span><span class="sxs-lookup"><span data-stu-id="1b8f6-216">Removing all menu items for a data entity from all pages</span></span>

<span data-ttu-id="1b8f6-217">統合シナリオでは、一部のデータ エンティティを OData サービス経由で公開して使用できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-217">Integration scenarios require that some data entities be publicly available via the OData Service.</span></span> <span data-ttu-id="1b8f6-218">ただし、既定で **Office で開く**メニューでこれらのデータ エンティティが表示されるのは、常に適切とは言えません。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-218">However, it isn't always appropriate that these data entities appear on the **Open in Office** menu by default.</span></span> <span data-ttu-id="1b8f6-219">このシナリオでは、**OfficeMenuOmit** コード属性をエンティティ申告に追加できます。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-219">In this scenario, you can add the **OfficeMenuOmit** code attribute to the entity declaration.</span></span>

    [OfficeMenuOmit]
    public class MyEntity extends common
    {
        // Entity code…
    }

<span data-ttu-id="1b8f6-220">この変更を行なった後、既定では、エンティティは一致するルート データ ソースのページを持つ **Office で開く**メニューには表示されません。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-220">After you make this change, by default, the entity won't appear on the **Open in Office** menu on pages that have a matching root data source.</span></span> <span data-ttu-id="1b8f6-221">ただし、エンティティが特定のページに追加される必要がある場合、それを追加するのにその他のカスタマイズ メカニズムを使用できます。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-221">However, if the entity should be added to a specific page, you can use other customization mechanisms to add it.</span></span>

### <a name="adding-a-menu-item-button-to-a-page-that-corresponds-to-an-open-in-office-menu-entry"></a><span data-ttu-id="1b8f6-222">Office メニュー エントリの開くに対応するページへのメニュー項目ボタンの追加</span><span class="sxs-lookup"><span data-stu-id="1b8f6-222">Adding a menu item button to a page that corresponds to an Open in Office menu entry</span></span>

<span data-ttu-id="1b8f6-223">ページのアクション ウィンドウに、**Office で開く** メニューのカスタム メニュー項目に対応するメニュー項目ボタンを配置するのが適切なことがあります。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-223">Sometimes, it's appropriate that the Action Pane of a page have a menu item button that corresponds to a custom menu item on the **Open in Office** menu.</span></span> <span data-ttu-id="1b8f6-224">この場合、次のプロパティを持つメニュー項目ボタンをモデル化できます。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-224">In this case, you can model a menu item button that has the following properties:</span></span>

-   <span data-ttu-id="1b8f6-225">**メニュー項目タイプ:** **アクション**</span><span class="sxs-lookup"><span data-stu-id="1b8f6-225">**Menu Item Type:** **Action**</span></span>
-   <span data-ttu-id="1b8f6-226">**メニュー項目名:** **ExportToExcelExportForm**</span><span class="sxs-lookup"><span data-stu-id="1b8f6-226">**Menu Item Name:** **ExportToExcelExportForm**</span></span>
-   <span data-ttu-id="1b8f6-227">**パラメーター:** メニュー項目の ID</span><span class="sxs-lookup"><span data-stu-id="1b8f6-227">**Parameters:** The ID of the menu item</span></span>

<span data-ttu-id="1b8f6-228">その後、このメニュー項目ボタンをマウスでクリックすると、**Office で開く** メニューの対応するメニュー項目をマウスでクリックしたのと同じになります。</span><span class="sxs-lookup"><span data-stu-id="1b8f6-228">Then, a mouse click of this menu item button is equivalent to a mouse click of the corresponding menu item on the **Open in Office** menu.</span></span>



