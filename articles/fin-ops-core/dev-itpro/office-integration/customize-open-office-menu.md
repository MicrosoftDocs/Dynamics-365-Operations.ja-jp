---
title: '[Microsoft Office で開く] メニューのカスタマイズ'
description: このトピックでは、[Open in Office] メニューについての情報を提供し、オプションの追加、削除、変更によってカスタマイズする方法について説明します。
author: jasongre
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 270774
ms.assetid: 3ff1184b-1a8a-4102-9600-f1776634d95f
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2017-02-28
ms.dyn365.ops.version: Platform update 4
ms.openlocfilehash: 6338e5701f88700d2b9527feaee18a893107a247
ms.sourcegitcommit: 890a0b3eb3c1f48d786b0789e5bb8641e0b8455e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/20/2021
ms.locfileid: "5919857"
---
# <a name="customize-the-open-in-microsoft-office-menu"></a><span data-ttu-id="81dab-103">Microsoft Office で開くメニューのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="81dab-103">Customize the Open in Microsoft Office menu</span></span>

[!include [applies to](../includes/applies-to-commerce-finance-scm.md)]

[!include [banner](../includes/banner.md)]

<span data-ttu-id="81dab-104">ほとんどのページには、Microsoft Office で開くメニューが含まれます。</span><span class="sxs-lookup"><span data-stu-id="81dab-104">Most pages include an Open in Microsoft Office menu.</span></span> <span data-ttu-id="81dab-105">このトピックでは、[Open in Office] メニューについての情報を提供し、オプションの追加、削除、変更によってカスタマイズする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="81dab-105">This topics provides information about the Open in Office menu, and explains how customize it by adding, removing, and changing options.</span></span>

<a name="overview"></a><span data-ttu-id="81dab-106">概要</span><span class="sxs-lookup"><span data-stu-id="81dab-106">Overview</span></span>
--------

<span data-ttu-id="81dab-107">**Microsoft Office で開く** メニュー ボタン (**Office で開く** メニュー) は、ページに表示されるシステム定義ボタンです。</span><span class="sxs-lookup"><span data-stu-id="81dab-107">The **Open in Microsoft Office** menu button (**Open in Office** menu) is a system-defined button that appears on pages.</span></span> <span data-ttu-id="81dab-108">**Office で開く** メニューには、Microsoft Excel や Microsoft Word などのさまざまな Office 製品にデータをエクスポートできるようにするためのメニュー項目が含まれています。</span><span class="sxs-lookup"><span data-stu-id="81dab-108">The **Open in Office** menu contains menu items that let you export data to various Office products, such as Microsoft Excel and Microsoft Word.</span></span> <span data-ttu-id="81dab-109">次のテーブルは、**Office で開く** メニューのメニュー項目について説明しています。</span><span class="sxs-lookup"><span data-stu-id="81dab-109">The following table describes the menu items on the **Open in Office** menu.</span></span>

| <span data-ttu-id="81dab-110">メニュー項目</span><span class="sxs-lookup"><span data-stu-id="81dab-110">Menu item</span></span>       | <span data-ttu-id="81dab-111">説明</span><span class="sxs-lookup"><span data-stu-id="81dab-111">Description</span></span>                                                                                                                                                                                                                                                  |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81dab-112">Excel にエクスポート</span><span class="sxs-lookup"><span data-stu-id="81dab-112">Export to Excel</span></span> | <span data-ttu-id="81dab-113">データは Excel ワークブックにエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="81dab-113">The data is exported to an Excel workbook.</span></span> <span data-ttu-id="81dab-114">このブックには Finance and Operations への逆参照が含まれていないため、データを更新することはできません。</span><span class="sxs-lookup"><span data-stu-id="81dab-114">The workbook contains no references back to Finance and Operations, and the data can't be refreshed.</span></span>                                                                                               |
| <span data-ttu-id="81dab-115">Word にエクスポート</span><span class="sxs-lookup"><span data-stu-id="81dab-115">Export to Word</span></span>  | <span data-ttu-id="81dab-116">データは Word 文書にエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="81dab-116">The data is exported to a Word document.</span></span> <span data-ttu-id="81dab-117">このドキュメントには Finance and Operations への逆参照が含まれていないため、データを更新することはできません。</span><span class="sxs-lookup"><span data-stu-id="81dab-117">The document contains no references back to Finance and Operations, and the data can't be refreshed.</span></span>                                                                                                           |
| <span data-ttu-id="81dab-118">Excel で開く</span><span class="sxs-lookup"><span data-stu-id="81dab-118">Open in Excel</span></span>   | <span data-ttu-id="81dab-119">Microsoft Dynamics Office アドインを含むブックが作成されます。</span><span class="sxs-lookup"><span data-stu-id="81dab-119">A workbook is created that contains the Microsoft Dynamics Office add-in.</span></span> <span data-ttu-id="81dab-120">ワークブックには Finance and Operations の参照が含まれており、アドインでホストされているデータ コネクタからデータをリフレッシュ、更新、公開することができます。</span><span class="sxs-lookup"><span data-stu-id="81dab-120">The workbook contains a reference back to Finance and Operations, and the data can be refreshed, updated, and published from the Data Connector that is hosted in the add-in.</span></span> |

## <a name="how-menu-items-are-added-to-the-open-in-office-menu"></a><span data-ttu-id="81dab-121">Office で開くメニューに、どのようにメニュー項目が追加されますか。</span><span class="sxs-lookup"><span data-stu-id="81dab-121">How menu items are added to the Open in Office menu</span></span>
<span data-ttu-id="81dab-122">エクスポート オプションは、次の方法で **Office で開く** メニューに追加されます。</span><span class="sxs-lookup"><span data-stu-id="81dab-122">The export options are added to the **Open in Office** menu in the following manner:</span></span>

1.  <span data-ttu-id="81dab-123">**Excel にエクスポート** グループで、メニュー項目が表示されている各グリッドに追加されます。</span><span class="sxs-lookup"><span data-stu-id="81dab-123">In the **Export to Excel** group, a menu item is added for each visible grid.</span></span>
2.  <span data-ttu-id="81dab-124">ページのルート データ ソースごとに、同じルート データ ソースを持つ一連のデータ エンティティが決定されます。</span><span class="sxs-lookup"><span data-stu-id="81dab-124">For each root data source on the page, the set of data entities that have the same root data source is determined.</span></span> <span data-ttu-id="81dab-125">これらの各データ エンティティについては、以下のメニュー項目が追加されます。</span><span class="sxs-lookup"><span data-stu-id="81dab-125">For each of these data entities, the following menu items are added:</span></span>
    -   <span data-ttu-id="81dab-126">**Excel で開く** グループで、メニュー項目がデータ エンティティの既定のエクスポートに追加されます。</span><span class="sxs-lookup"><span data-stu-id="81dab-126">In the **Open in Excel** group, a menu item is added for a default export of the data entity.</span></span>
    -   <span data-ttu-id="81dab-127">**Excel で開く** グループで、メニュー項目が同じルート データ エンティティを持つ **Excel** タイプのドキュメント テンプレート レコードごとに追加され、**Office で開く** メニューに含めるようマークされます。</span><span class="sxs-lookup"><span data-stu-id="81dab-127">In the **Open in Excel** group, a menu item is added for each Document Template record of the **Excel** type that has the same root data entity and is marked for inclusion on the **Open in Office** menu.</span></span>
    -   <span data-ttu-id="81dab-128">**Word にエクスポート** グループで、メニュー項目が同じルート データ エンティティを持つ **Word** タイプのドキュメント テンプレート レコードごとに追加され、**Office で開く** メニューに含めるようマークされます。</span><span class="sxs-lookup"><span data-stu-id="81dab-128">In the **Export to Word** group, a menu item is added for each Document Template record of the **Word** type that has the same root data entity and is marked for inclusion on the **Open in Office** menu.</span></span>

## <a name="default-exports"></a><span data-ttu-id="81dab-129">既定のエクスポート</span><span class="sxs-lookup"><span data-stu-id="81dab-129">Default exports</span></span>
<span data-ttu-id="81dab-130">**Office で開く** メニューは、各データ エンティティの既定のエクスポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="81dab-130">The **Open in Office** menu provides a default export for each data entity.</span></span> <span data-ttu-id="81dab-131">このエクスポートには、データ エンティティの **AutoReport** グループのすべてのフィールドが含まれます。</span><span class="sxs-lookup"><span data-stu-id="81dab-131">This export includes all the fields in the **AutoReport** group on the data entity.</span></span> <span data-ttu-id="81dab-132">**SaveDataPerCompany** が **はい** に設定されている場合、現在の会社へのデータを制限するようフィルターが適用されます。</span><span class="sxs-lookup"><span data-stu-id="81dab-132">If **SaveDataPerCompany** is set to **Yes** for the data entity, a filter is applied to limit the data to the current company.</span></span>

## <a name="document-templates"></a><span data-ttu-id="81dab-133">ドキュメント テンプレート</span><span class="sxs-lookup"><span data-stu-id="81dab-133">Document templates</span></span>
<span data-ttu-id="81dab-134">ドキュメント テンプレートは、**ドキュメント テンプレート** ページから追加できます。</span><span class="sxs-lookup"><span data-stu-id="81dab-134">Document templates can be added from the **Document templates** page.</span></span> <span data-ttu-id="81dab-135">各ドキュメント テンプレート レコードに関連付けられているいくつかのフィールドは、**Office で開く** メニューでのそのテンプレートの動作を制御します。</span><span class="sxs-lookup"><span data-stu-id="81dab-135">Several fields that are associated with each Document Template record control the behavior of that template on the **Open in Office** menu.</span></span>

| <span data-ttu-id="81dab-136">フィールド</span><span class="sxs-lookup"><span data-stu-id="81dab-136">Field</span></span>                | <span data-ttu-id="81dab-137">説明</span><span class="sxs-lookup"><span data-stu-id="81dab-137">Description</span></span>                                                                                                                                                         |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81dab-138">ルート データ エンティティ</span><span class="sxs-lookup"><span data-stu-id="81dab-138">Root data entity</span></span>     | <span data-ttu-id="81dab-139">テンプレートのルート データ エンティティ。</span><span class="sxs-lookup"><span data-stu-id="81dab-139">The root data entity of the template.</span></span> <span data-ttu-id="81dab-140">ルート データ エンティティは、テンプレートが含まれるページを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="81dab-140">The root data entity is used to determine which pages the template can be included on.</span></span>                                        |
| <span data-ttu-id="81dab-141">Office メニューのリスト</span><span class="sxs-lookup"><span data-stu-id="81dab-141">List in Office menu</span></span>  | <span data-ttu-id="81dab-142">このフィールドが選択されている場合に、テンプレートは該当するページの **Office で開く** メニューに含まれます。</span><span class="sxs-lookup"><span data-stu-id="81dab-142">If this field is selected, the template will be included on the **Open in Office** menu on applicable pages.</span></span> <span data-ttu-id="81dab-143">(該当するページは、ルート データ エンティティによって異なります。)</span><span class="sxs-lookup"><span data-stu-id="81dab-143">(The applicable pages depend on the root data entity).</span></span> |
| <span data-ttu-id="81dab-144">レコード フィルターの適用</span><span class="sxs-lookup"><span data-stu-id="81dab-144">Apply record filter</span></span>  | <span data-ttu-id="81dab-145">このフィールドが選択されている場合、そのページで現在選択されているレコードをベースにデータがフィルター処理されます。</span><span class="sxs-lookup"><span data-stu-id="81dab-145">If this field is selected, the data will be filtered, based on the record that is currently selected on the page.</span></span>                                                   |
| <span data-ttu-id="81dab-146">会社フィルターの適用</span><span class="sxs-lookup"><span data-stu-id="81dab-146">Apply company filter</span></span> | <span data-ttu-id="81dab-147">このフィールドが選択されている場合、現在の会社をベースにデータがフィルター処理されます。</span><span class="sxs-lookup"><span data-stu-id="81dab-147">If this field is selected, the data will be filtered, based on the current company.</span></span>                                                                                 |

### <a name="trimmed-template-columns-and-fields"></a><span data-ttu-id="81dab-148">トリミングされたテンプレートの列とフィールド</span><span class="sxs-lookup"><span data-stu-id="81dab-148">Trimmed template columns and fields</span></span>

<span data-ttu-id="81dab-149">**Office で開く** メニューに含まれる Excel テンプレートで、列およびフィールドは、システムおよび該当する国/地域コンテキストに適用されているコンフィギュレーション キーに基づいて、ワークブックからトリミングされます。</span><span class="sxs-lookup"><span data-stu-id="81dab-149">For Excel templates that are included on the **Open in Office** menu, columns and fields will be trimmed from the workbook, based on the configuration keys that are applied to the system and the applicable country/region context.</span></span> <span data-ttu-id="81dab-150">コンフィギュレーション キーがブック内の列またはフィールドに関連付けられている場合は、コンフィギュレーション キーが無効になっている場合は、列またはフィールドが削除されます。</span><span class="sxs-lookup"><span data-stu-id="81dab-150">If a configuration key is associated with a column or field in the workbook, the column or field will be removed if the configuration key is disabled.</span></span> <span data-ttu-id="81dab-151">国/地域コードのセットがブックの列またはフィールドに関連付けられている場合、その国/地域コードが有効範囲にない場合は、列またはフィールドが削除されます。</span><span class="sxs-lookup"><span data-stu-id="81dab-151">If a set of country/region codes is associated with the column or field in the workbook, the column or field will be removed if the country/region code isn't in scope.</span></span>

## <a name="open-in-office-menu-customization"></a><span data-ttu-id="81dab-152">「Office で開く」メニューのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="81dab-152">Open in Office menu customization</span></span>
<span data-ttu-id="81dab-153">特定のページの **Office で開** メニューに表示されるコンテンツをカスタマイズする方法はいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="81dab-153">There are several methods for customizing the content that appears on the **Open in Office** menu on a given page.</span></span> <span data-ttu-id="81dab-154">たとえば、モデル要素およびコード属性のメタデータ プロパティを通じて、静的にコンテンツをカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="81dab-154">For example, you can customize the content statically through metadata properties on model element and code attributes.</span></span> <span data-ttu-id="81dab-155">ただし、コード経由のカスタマイズによりコントロールの最高レベルを提供します。</span><span class="sxs-lookup"><span data-stu-id="81dab-155">However, customization via code gives you the finest level of control.</span></span> <span data-ttu-id="81dab-156">コードでは、ページに 1 つまたは複数のインターフェイスを実装するか、拡張機能およびイベント サブスクリプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="81dab-156">In code, you can either implement one or more interfaces on a page, or use extensions and event subscriptions.</span></span> <span data-ttu-id="81dab-157">次のセクションでは、最も頻繁に使用されるカスタマイズ シナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="81dab-157">The following sections describe the customization scenarios that are most often used.</span></span>

### <a name="modifying-the-open-in-office-menu-through-interfaces"></a><span data-ttu-id="81dab-158">インターフェイスを通じた Office で開くメニューの変更</span><span class="sxs-lookup"><span data-stu-id="81dab-158">Modifying the Open in Office menu through interfaces</span></span>

<span data-ttu-id="81dab-159">自分の所有するページを変更する必要がある場合、のページのすべてのプライベート メンバーへのアクセス権を付与し、より深いカスタマイズが可能になるため、インターフェイスは最適なカスタマイズ方法となります。</span><span class="sxs-lookup"><span data-stu-id="81dab-159">If you must modify a page that you own, interfaces are the most appropriate customization method, because they give access to all private members of the page and allow for deeper customization.</span></span> <span data-ttu-id="81dab-160">以下のインターフェイスをページのコードに適用することができます。</span><span class="sxs-lookup"><span data-stu-id="81dab-160">You can apply the following interfaces to the code for a page.</span></span>

| <span data-ttu-id="81dab-161">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="81dab-161">Interface</span></span>                              | <span data-ttu-id="81dab-162">説明</span><span class="sxs-lookup"><span data-stu-id="81dab-162">Description</span></span>                                                                                                    |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81dab-163">OfficeIMenuCustomizer</span><span class="sxs-lookup"><span data-stu-id="81dab-163">OfficeIMenuCustomizer</span></span>                  | <span data-ttu-id="81dab-164">ページと見なされるデータ エンティティのセットを変更し、カスタムのメニュー項目を追加するには、このインターフェイスを使用します。</span><span class="sxs-lookup"><span data-stu-id="81dab-164">Use this interface to modify the set of data entities that is considered for a page and add custom menu items.</span></span> |
| <span data-ttu-id="81dab-165">OfficeIGeneratedWorkbookCustomExporter</span><span class="sxs-lookup"><span data-stu-id="81dab-165">OfficeIGeneratedWorkbookCustomExporter</span></span> | <span data-ttu-id="81dab-166">実行時に生成されるブックのカスタム エクスポートを行うには、このインターフェイスを使用します。</span><span class="sxs-lookup"><span data-stu-id="81dab-166">Use this interface to do a custom export of a workbook that is generated at run time.</span></span>                          |
| <span data-ttu-id="81dab-167">OfficeITemplateCustomExporter</span><span class="sxs-lookup"><span data-stu-id="81dab-167">OfficeITemplateCustomExporter</span></span>          | <span data-ttu-id="81dab-168">ドキュメント テンプレートのレコードに基づくカスタムのエクスポートを行うには、このインターフェイスを使用します。</span><span class="sxs-lookup"><span data-stu-id="81dab-168">Use this interface to do a custom export that is based on a Document Template record.</span></span>                          |

### <a name="modifying-the-open-in-office-menu-through-extensions-and-event-subscriptions"></a><span data-ttu-id="81dab-169">拡張機能とイベント サブスクリプションを通じた Office で開くメニューの変更</span><span class="sxs-lookup"><span data-stu-id="81dab-169">Modifying the Open in Office menu through extensions and event subscriptions</span></span>

<span data-ttu-id="81dab-170">所有していないページを変更する必要がある場合、オーバーレイが必要となるため、インターフェイスの使用を避ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="81dab-170">If you must modify a page that you don't own, you should avoid using interfaces, because that approach will require over-layering.</span></span> <span data-ttu-id="81dab-171">代わりに、拡張機能およびイベント サブスクリプションを通じてカスタマイズを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="81dab-171">Instead, you should do the customization through extensions and event subscriptions.</span></span> <span data-ttu-id="81dab-172">この方法を使用するには、カスタマイズするページの **OnIntializing** イベントにサブスクライブする拡張クラスを実装します。</span><span class="sxs-lookup"><span data-stu-id="81dab-172">To use this approach, implement an extension class that subscribes to the **OnIntializing** event of the page that you're customizing.</span></span> <span data-ttu-id="81dab-173">このイベント ハンドラーから、ページの **OfficeFormRunHelper** を取得し、その **OfficeMenuInitializing** イベントにサブスクライブします。</span><span class="sxs-lookup"><span data-stu-id="81dab-173">From this event handler, get the **OfficeFormRunHelper** for the page, and subscribe to its **OfficeMenuInitializing** event.</span></span> <span data-ttu-id="81dab-174">次の例は、この方法のサンプル コードを示しています。</span><span class="sxs-lookup"><span data-stu-id="81dab-174">The following example shows sample code for this approach.</span></span>

```xpp
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
```

## <a name="typical-customization-scenarios"></a><span data-ttu-id="81dab-175">一般的なカスタマイズ シナリオ</span><span class="sxs-lookup"><span data-stu-id="81dab-175">Typical customization scenarios</span></span>
<span data-ttu-id="81dab-176">次の例では、**\_menuOptions** 変数に、カスタマイズしている **OfficeMenuOptions** インスタンスが含まれていると想定しています。</span><span class="sxs-lookup"><span data-stu-id="81dab-176">The following examples assume that the **\_menuOptions** variable contains the **OfficeMenuOptions** instance that you're customizing.</span></span>

### <a name="modifying-the-set-of-data-entities-that-is-considered-for-a-page"></a><span data-ttu-id="81dab-177">ページで考慮されるデータ エンティティのセットの変更</span><span class="sxs-lookup"><span data-stu-id="81dab-177">Modifying the set of data entities that is considered for a page</span></span>

<span data-ttu-id="81dab-178">**Office で開く** メニューにあるメニュー項目の多くは、ページとみなされるデータ エンティティに基づいて自動的に追加されます。</span><span class="sxs-lookup"><span data-stu-id="81dab-178">Many of the menu items on the **Open in Office** menu are added automatically, based on the data entities that are considered for the page.</span></span> <span data-ttu-id="81dab-179">ただし、場合によっては、データ エンティティのセットを特定するために使用されるアルゴリズムが、正しいセットを特定しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="81dab-179">However, in some cases, the algorithm that is used to determine the set of data entities might not determine the correct set.</span></span> <span data-ttu-id="81dab-180">ページと見なされるデータ エンティティのセットを変更するには、**OfficeIMenuCustomizer.customizeMenuOptions** メソッドまたは **OfficeFormRunHelper.OfficeMenuInitializing** デリゲートから利用可能な **OfficeMenuOptions** を使用します。</span><span class="sxs-lookup"><span data-stu-id="81dab-180">To modify the set of data entities that is considered for the page, you can use the **OfficeMenuOptions** that is available from either the **OfficeIMenuCustomizer.customizeMenuOptions** method or the **OfficeFormRunHelper.OfficeMenuInitializing** delegate.</span></span>

> [!WARNING]
> <span data-ttu-id="81dab-181">このコードは、フォーム init() または run() には使用しません。</span><span class="sxs-lookup"><span data-stu-id="81dab-181">Do not use this code in form init() or run().</span></span> <span data-ttu-id="81dab-182">これは、特にシステムを変更した場合、フォームの読み込み速度に悪影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="81dab-182">This can negatively impact form load speed, especially upon system reboot.</span></span>


```xpp
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
```

### <a name="specifying-the-default-data-entityrelated-options-that-are-included"></a><span data-ttu-id="81dab-183">含まれている既定のデータ エンティティ関連のオプションを指定します。</span><span class="sxs-lookup"><span data-stu-id="81dab-183">Specifying the default data entity–related options that are included</span></span>

<span data-ttu-id="81dab-184">**OfficeMenuDataEntityOptions** クラスを使用すると、既定のエクスポートのためのメニュー項目またはドキュメント テンプレートに関連するメニュー項目を含めるかどうかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="81dab-184">The **OfficeMenuDataEntityOptions** class lets you specify whether to include a menu item for a default export or a menu item that is related to a document template.</span></span>

```xpp
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
```

### <a name="adding-a-custom-export-menu-item--generating-a-workbook"></a><span data-ttu-id="81dab-185">カスタム エクスポート メニュー項目の追加 – ブックの生成</span><span class="sxs-lookup"><span data-stu-id="81dab-185">Adding a custom export menu item – Generating a workbook</span></span>

<span data-ttu-id="81dab-186">明示的にメニュー項目を追加するには、それを **OfficeMenuOptions.customMenuItems()** リストに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="81dab-186">To explicitly add a menu item, you must add it to the **OfficeMenuOptions.customMenuItems()** list.</span></span> <span data-ttu-id="81dab-187">実行時に生成されるブックに対応するメニュー項目を追加するには、**OfficeGeneratedExportMenuItem** を使用します。</span><span class="sxs-lookup"><span data-stu-id="81dab-187">To add a menu item that corresponds to a workbook that is generated at run time, use an **OfficeGeneratedExportMenuItem**.</span></span>

```xpp
OfficeGeneratedExportMenuItem menuItem = OfficeGeneratedExportMenuItem::construct(tableStr(MyEntity), "MyCustomGeneratedExportId");
menuItem.setDisplayNameWithDataEntity();
_menuOptions.customMenuItems().addEnd(menuItem);
```

<span data-ttu-id="81dab-188">実際にエクスポートする内容を定義するには、**ExportToExcelDataEntityContext** を使用します。</span><span class="sxs-lookup"><span data-stu-id="81dab-188">To define what is actually exported, use an **ExportToExcelDataEntityContext**.</span></span> <span data-ttu-id="81dab-189">**ExportToExcelDataEntityContext** を指定するメソッドは、インターフェイスまたは拡張機能とイベント サブスクリプションを使用して、**Office で開く** メニューをカスタマイズするかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="81dab-189">The method for specifying the **ExportToExcelDataEntityContext** depends on whether you're using interfaces or extensions and event subscriptions to customize the **Open in Office** menu.</span></span>


#### <a name="using-interfaces"></a><span data-ttu-id="81dab-190">インターフェイスの使用</span><span class="sxs-lookup"><span data-stu-id="81dab-190">Using interfaces</span></span>

<span data-ttu-id="81dab-191">インターフェイスを使用している場合、**OfficeIGeneratedWorkbookCustomExporter.getDataEntityContext()** メソッドを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="81dab-191">If you're using interfaces, you must implement the **OfficeIGeneratedWorkbookCustomExporter.getDataEntityContext()** method.</span></span>

```xpp
public ExportToExcelDataEntityContext getDataEntityContext(OfficeGeneratedExportMenuItem _menuItem)
{
    ExportToExcelDataEntityContext context = null;
    if (_menuItem.id() == "MyCustomGeneratedExportId")
    {
        context = ExportToExcelDataEntityContext::construct(tableStr(MyEntity), tableFieldGroupStr(MyEntity, MyFieldGroup);
    }
    return context;
}
```

#### <a name="using-extensions-and-event-subscriptions"></a><span data-ttu-id="81dab-192">拡張機能とイベント サブスクリプションの使用</span><span class="sxs-lookup"><span data-stu-id="81dab-192">Using extensions and event subscriptions</span></span>

<span data-ttu-id="81dab-193">拡張機能とイベント サブスクリプションを使用している場合、**OfficeGeneratedExportMenuItem.getDataEntityContext** デリゲートはメニュー項目を **OfficeMenuOptions.customMenuItems()** リストに追加する前にサブスクライブする必要があります。</span><span class="sxs-lookup"><span data-stu-id="81dab-193">If you're using extensions and event subscriptions, the **OfficeGeneratedExportMenuItem.getDataEntityContext** delegate should be subscribed to before you add the menu item to the **OfficeMenuOptions.customMenuItems()** list.</span></span> <span data-ttu-id="81dab-194">イベント ハンドラーのコードは、インターフェイスの先行するコードと同様である必要があります。</span><span class="sxs-lookup"><span data-stu-id="81dab-194">The code for the event handler should resemble the preceding code for the interface.</span></span> <span data-ttu-id="81dab-195">次の例は、イベント サブスクリプションの実行方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="81dab-195">The following example shows how to do the event subscription.</span></span>

```xpp
menuItem.getDataEntityContext += eventhandler(MyForm_Extension::getDataEntityContextHandler);
```

### <a name="adding-a-custom-export-menu-item--specifying-a-document-template"></a><span data-ttu-id="81dab-196">カスタム エクスポート メニュー項目の追加 – ドキュメント テンプレートの指定</span><span class="sxs-lookup"><span data-stu-id="81dab-196">Adding a custom export menu item – Specifying a document template</span></span>

<span data-ttu-id="81dab-197">明示的にメニュー項目を追加するには、それを **OfficeMenuOptions.customMenuItems()** リストに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="81dab-197">To explicitly add a menu item, you must add it to the **OfficeMenuOptions.customMenuItems()** list.</span></span> <span data-ttu-id="81dab-198">ドキュメント テンプレート レコードに対応するメニュー項目を追加するには、**OfficeTemplateExportMenuItem** を使用します。</span><span class="sxs-lookup"><span data-stu-id="81dab-198">To add a menu item that corresponds to a Document Template record, use an **OfficeTemplateExportMenuItem**.</span></span>

```xpp
OfficeTemplateExportMenuItem menuItem = OfficeTemplateExportMenuItem::construct(OfficeAppApplicationType::Excel, "MyTemplateId", "MyCustomTemplateExportId");
_menuOptions.customMenuItems().addEnd(menuItem);
```

<span data-ttu-id="81dab-199">実行時にテンプレートを変更するには、一連の初期フィルターを指定します。</span><span class="sxs-lookup"><span data-stu-id="81dab-199">To modify the template at run time, you can supply a set of initial filters.</span></span> <span data-ttu-id="81dab-200">これらのフィルターは、指定されたデータ エンティティのテンプレート内のフィルターを置き換えます。</span><span class="sxs-lookup"><span data-stu-id="81dab-200">These filters will replace any filters in the template for the specified data entities.</span></span> <span data-ttu-id="81dab-201">また、**WorkbookSettingsManager** を使用してフィルターを変更し、多くの設定を指定できます。</span><span class="sxs-lookup"><span data-stu-id="81dab-201">Additionally, you can modify filters and specify many settings by using **WorkbookSettingsManager**.</span></span> <span data-ttu-id="81dab-202">次のセクションに例を示します。</span><span class="sxs-lookup"><span data-stu-id="81dab-202">The following sections show examples.</span></span>

#### <a name="using-interfaces"></a><span data-ttu-id="81dab-203">インターフェイスの使用</span><span class="sxs-lookup"><span data-stu-id="81dab-203">Using interfaces</span></span>

<span data-ttu-id="81dab-204">インターフェイスを使用している場合、**OfficeITemplateCustomExporter.getInitialTemplateFilters()** および **OfficeITemplateCustomExporter.updateTemplateSettings()** メソッドを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="81dab-204">If you're using interfaces, you must implement the **OfficeITemplateCustomExporter.getInitialTemplateFilters()** and **OfficeITemplateCustomExporter.updateTemplateSettings()** methods.</span></span>

```xpp
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
```

#### <a name="using-extensions-and-event-subscriptions"></a><span data-ttu-id="81dab-205">拡張機能とイベント サブスクリプションの使用</span><span class="sxs-lookup"><span data-stu-id="81dab-205">Using extensions and event subscriptions</span></span>

<span data-ttu-id="81dab-206">拡張機能とイベント サブスクリプションを使用している場合、**OfficeTemplateExportMenuItem.getInitialTemplateFilters** および **OfficeTemplateExportMenuItem.updateTemplateSettings** デリゲートはメニュー項目を **OfficeMenuOptions.customMenuItems()** リストに追加する前にサブスクライブする必要があります。</span><span class="sxs-lookup"><span data-stu-id="81dab-206">If you're using extensions and event subscriptions, the **OfficeTemplateExportMenuItem.getInitialTemplateFilters** and **OfficeTemplateExportMenuItem.updateTemplateSettings** delegates should be subscribed to before you add the menu item to the **OfficeMenuOptions.customMenuItems()** list.</span></span> <span data-ttu-id="81dab-207">イベント ハンドラーのコードは、インターフェイスの先行するコードと同様である必要があります。</span><span class="sxs-lookup"><span data-stu-id="81dab-207">The code for the event handlers should resemble the preceding code for the interface.</span></span> <span data-ttu-id="81dab-208">次の例は、イベント サブスクリプションの実行方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="81dab-208">The following example shows how to do the event subscription.</span></span>

```xpp
menuItem.getInitialTemplateFilters += eventhandler(MyForm_Extension::getInitialTemplateFiltersHander);
menuItem.updateTemplateSettings += eventhandler(MyForm_Extension::updateTemplateSettingsHandler);
```

## <a name="additional-customizations"></a><span data-ttu-id="81dab-209">追加のカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="81dab-209">Additional customizations</span></span>
<span data-ttu-id="81dab-210">次のカスタマイズを使用すると、インターフェイス、拡張機能、およびイベント ハンドラーを使用せずに、**Office で開く** メニューの内容を変更できます。</span><span class="sxs-lookup"><span data-stu-id="81dab-210">The following customizations let you modify the contents of the **Open in Office** menu for a page without using interfaces or extensions and event handlers.</span></span>

### <a name="removing-an-export-to-excel-menu-item-for-a-grid"></a><span data-ttu-id="81dab-211">グリッドの [Excel にエクスポート] メニュー項目を削除</span><span class="sxs-lookup"><span data-stu-id="81dab-211">Removing an Export to Excel menu item for a grid</span></span>

<span data-ttu-id="81dab-212">**Office で開く** メニューで、**Excel にエクスポート** グループには、表示されている各グリッドのメニュー項目が含まれます。</span><span class="sxs-lookup"><span data-stu-id="81dab-212">On the **Open in Office** menu, the **Export to Excel** group will contain a menu item for each visible grid.</span></span> <span data-ttu-id="81dab-213">**Office で開く** メニューからグリッドを削除するには、グリッドの **ExportAllowed** メタデータ プロパティを **いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="81dab-213">To remove a grid from the **Open in Office** menu, set the **ExportAllowed** metadata property on the grid to **No**.</span></span> <span data-ttu-id="81dab-214">この変更を行なった後、ユーザーはグリッドのショートカット メニューを使用してグリッドをエクスポートすることはできません。</span><span class="sxs-lookup"><span data-stu-id="81dab-214">After you make this change, users won't be able to export the grid by using the shortcut menu for the grid.</span></span>

### <a name="renaming-an-export-to-excel-menu-item-for-a-grid"></a><span data-ttu-id="81dab-215">グリッドの [Excel にエクスポート] メニュー項目を名前変更</span><span class="sxs-lookup"><span data-stu-id="81dab-215">Renaming an Export to Excel menu item for a grid</span></span>

<span data-ttu-id="81dab-216">グリッドに関連する **Excelにエクスポート** メニュー項目の名前を変更するには、グリッドの **ExportLabel** メタデータ プロパティを適切なラベルに設定します。</span><span class="sxs-lookup"><span data-stu-id="81dab-216">To rename the **Export to Excel** menu item that is related to a grid, set the **ExportLabel** metadata property on the grid to the appropriate label.</span></span>

### <a name="removing-all-menu-items-for-a-data-entity-from-all-pages"></a><span data-ttu-id="81dab-217">すべてのページからデータ エンティティのすべてのメニュー項目を削除</span><span class="sxs-lookup"><span data-stu-id="81dab-217">Removing all menu items for a data entity from all pages</span></span>

<span data-ttu-id="81dab-218">統合シナリオでは、一部のデータ エンティティを OData サービス経由で公開して使用できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="81dab-218">Integration scenarios require that some data entities be publicly available via the OData Service.</span></span> <span data-ttu-id="81dab-219">ただし、既定で **Office で開く** メニューでこれらのデータ エンティティが表示されるのは、常に適切とは言えません。</span><span class="sxs-lookup"><span data-stu-id="81dab-219">However, it isn't always appropriate that these data entities appear on the **Open in Office** menu by default.</span></span> <span data-ttu-id="81dab-220">このシナリオでは、**OfficeMenuOmit** コード属性をエンティティ申告に追加できます。</span><span class="sxs-lookup"><span data-stu-id="81dab-220">In this scenario, you can add the **OfficeMenuOmit** code attribute to the entity declaration.</span></span>

```xpp
[OfficeMenuOmit]
public class MyEntity extends common
{
    // Entity code…
}
```

<span data-ttu-id="81dab-221">この変更を行なった後、既定では、エンティティは一致するルート データ ソースのページを持つ **Office で開く** メニューには表示されません。</span><span class="sxs-lookup"><span data-stu-id="81dab-221">After you make this change, by default, the entity won't appear on the **Open in Office** menu on pages that have a matching root data source.</span></span> <span data-ttu-id="81dab-222">ただし、エンティティが特定のページに追加される必要がある場合、それを追加するのにその他のカスタマイズ メカニズムを使用できます。</span><span class="sxs-lookup"><span data-stu-id="81dab-222">However, if the entity should be added to a specific page, you can use other customization mechanisms to add it.</span></span>

### <a name="adding-a-menu-item-button-to-a-page-that-corresponds-to-an-open-in-office-menu-entry"></a><span data-ttu-id="81dab-223">Office メニュー エントリの開くに対応するページへのメニュー項目ボタンの追加</span><span class="sxs-lookup"><span data-stu-id="81dab-223">Adding a menu item button to a page that corresponds to an Open in Office menu entry</span></span>

<span data-ttu-id="81dab-224">ページのアクション ウィンドウに、**Office で開く** メニューのカスタム メニュー項目に対応するメニュー項目ボタンを配置するのが適切なことがあります。</span><span class="sxs-lookup"><span data-stu-id="81dab-224">Sometimes, it's appropriate that the Action Pane of a page have a menu item button that corresponds to a custom menu item on the **Open in Office** menu.</span></span> <span data-ttu-id="81dab-225">この場合、次のプロパティを持つメニュー項目ボタンをモデル化できます。</span><span class="sxs-lookup"><span data-stu-id="81dab-225">In this case, you can model a menu item button that has the following properties:</span></span>

-   <span data-ttu-id="81dab-226">**メニュー項目タイプ:** **アクション**</span><span class="sxs-lookup"><span data-stu-id="81dab-226">**Menu Item Type:** **Action**</span></span>
-   <span data-ttu-id="81dab-227">**メニュー項目名:** **ExportToExcelExportForm**</span><span class="sxs-lookup"><span data-stu-id="81dab-227">**Menu Item Name:** **ExportToExcelExportForm**</span></span>
-   <span data-ttu-id="81dab-228">**パラメーター:** メニュー項目の ID</span><span class="sxs-lookup"><span data-stu-id="81dab-228">**Parameters:** The ID of the menu item</span></span>

<span data-ttu-id="81dab-229">その後、このメニュー項目ボタンをマウスでクリックすると、**Office で開く** メニューの対応するメニュー項目をマウスでクリックしたのと同じになります。</span><span class="sxs-lookup"><span data-stu-id="81dab-229">Then, a mouse click of this menu item button is equivalent to a mouse click of the corresponding menu item on the **Open in Office** menu.</span></span>





[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
