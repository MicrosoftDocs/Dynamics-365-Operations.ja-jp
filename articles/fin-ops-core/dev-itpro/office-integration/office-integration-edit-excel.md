---
title: '[Excel で開く] エクスペリエンスの作成'
description: Excel と Word を Office エクスペリエンスで開く機能について学んで作成します。
author: ChrisGarty
manager: AnnBe
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 79223
ms.assetid: 05d8f7af-df6a-452f-a532-0f059eba4377
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 92b86cf5412774e9c561c682fae568f8d0fc2087
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685419"
---
# <a name="create-open-in-excel-experiences"></a><span data-ttu-id="e1c59-103">[Excel で開く] エクスペリエンスの作成</span><span class="sxs-lookup"><span data-stu-id="e1c59-103">Create Open in Excel experiences</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1c59-104">Excel と Word を Office エクスペリエンスで開く機能について学んで作成します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-104">Learn about creating Open in Office experiences for Excel and Word.</span></span>

## <a name="what-are-open-in-excel-experiences"></a><span data-ttu-id="e1c59-105">[Excel で開く] エクスペリエンスとは</span><span class="sxs-lookup"><span data-stu-id="e1c59-105">What are Open in Excel experiences?</span></span>

<span data-ttu-id="e1c59-106">「Excel で開く」エクスペリエンスは：</span><span class="sxs-lookup"><span data-stu-id="e1c59-106">Open in Excel experiences are:</span></span>

-   <span data-ttu-id="e1c59-107">エンティティと作成した OData サービスに基づいています。</span><span class="sxs-lookup"><span data-stu-id="e1c59-107">Based on entities and the OData services that they create.</span></span>
-   <span data-ttu-id="e1c59-108">動的に生成されるか、あらかじめ定義されたテンプレートに基づきます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-108">Dynamically-generated or based on a pre-defined template.</span></span>
-   <span data-ttu-id="e1c59-109">Excel アドインを使用して、編集および更新が可能です。</span><span class="sxs-lookup"><span data-stu-id="e1c59-109">Editable and refreshable via the Excel Add-in.</span></span>

<span data-ttu-id="e1c59-110">次の図は、**Excel アドイン** が仕訳入力に使用されている様子を示しています。</span><span class="sxs-lookup"><span data-stu-id="e1c59-110">The following image shows the **Excel Add-in** being used for Journal entry.</span></span>

<span data-ttu-id="e1c59-111">[![Excel アドインの例](./media/off101a.png)](./media/off101a.png)</span><span class="sxs-lookup"><span data-stu-id="e1c59-111">[![Example of Excel add-in](./media/off101a.png)](./media/off101a.png)</span></span>

## <a name="where-are-the-open-in-excel-experiences"></a><span data-ttu-id="e1c59-112">[Excel で開く] エクスペリエンスが存在する場所は</span><span class="sxs-lookup"><span data-stu-id="e1c59-112">Where are the Open in Excel experiences?</span></span>
<span data-ttu-id="e1c59-113">Excel で開くエクスペリエンスは、通常Microsoft Office で開くメニューのExcel で開くセクションの下にありますが、これらのエクスペリエンスには明示的なボタンを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-113">Open in Excel experiences are usually found under in the Open in Excel section of the Open in Microsoft Office menu, but an explicit button can be added for these experiences.</span></span>

## <a name="whats-the-difference-between-export-to-excel-and-open-in-excel"></a><span data-ttu-id="e1c59-114">"Excel にエクスポート" と "Excel で開く" の違い</span><span class="sxs-lookup"><span data-stu-id="e1c59-114">What's the difference between Export to Excel and Open in Excel?</span></span>
<span data-ttu-id="e1c59-115">Excel にエクスポート オプションおよびエクスペリエンスは、どちらも Microsoft Office で開くメニューにあります。</span><span class="sxs-lookup"><span data-stu-id="e1c59-115">The Export to Excel options and experiences are both found in the Open in Microsoft Office menu:</span></span>

-   <span data-ttu-id="e1c59-116">Excel にエクスポート オプションは、グリッド データの静的エクスポートです。</span><span class="sxs-lookup"><span data-stu-id="e1c59-116">The Export to Excel options are static exports of grid data.</span></span> <span data-ttu-id="e1c59-117">それぞれ表示されているグリッドに対応しています。</span><span class="sxs-lookup"><span data-stu-id="e1c59-117">Each one corresponds to a visible grid.</span></span> <span data-ttu-id="e1c59-118">現在のフィルター内にあるすべてのグリッド データはブックに格納されます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-118">All the grid data for the current filter is placed into a workbook.</span></span>
-   <span data-ttu-id="e1c59-119">[Excel で開く] エクスペリエンスは、Excel アドインを利用して更新と公開を行います。</span><span class="sxs-lookup"><span data-stu-id="e1c59-119">The Open in Excel experiences utilize the Excel Add-in to facilitate refresh and publish.</span></span>

<span data-ttu-id="e1c59-120">次の図は、**フリート顧客** フォームの **Microsoft Office で開く** メニューをテンプレート **Excel で開く** オプション、生成された **Excel で開く** オプション、および静的な **Excel にエクスポート** オプションと共に示しています。</span><span class="sxs-lookup"><span data-stu-id="e1c59-120">The following image shows the **Open in Microsoft Office** menu on the **Fleet Customers** form with a template **Open in Excel** option, a generated **Open in Excel** option, and a static **Export to Excel** option.</span></span>

<span data-ttu-id="e1c59-121">[![Microsoft Office メニューで開く](./media/off101b.png)](./media/off101b.png)</span><span class="sxs-lookup"><span data-stu-id="e1c59-121">[![Open in Microsoft Office menu](./media/off101b.png)](./media/off101b.png)</span></span>

## <a name="when-will-an-entity-show-as-an-open-in-excel-option"></a><span data-ttu-id="e1c59-122">エンティティはいつ [Excel で開く] オプションとして表示されますか ?</span><span class="sxs-lookup"><span data-stu-id="e1c59-122">When will an entity show as an Open in Excel option?</span></span>
<span data-ttu-id="e1c59-123">エンティティにフォームと同じルート データ ソース (テーブル) が存在するとき、そのデータソースは、Microsoft Office で開くメニューの Excel で開くセクションのオプションとして追加されます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-123">When an entity has the same root datasource (table) as a form, it will be added as an option in the Open in Excel section of the Open in Microsoft Office menu.</span></span> <span data-ttu-id="e1c59-124">これは、「生成済み」オプションと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-124">This is referred to as a “generated” option.</span></span>

## <a name="what-fields-will-be-shown-in-the-workbook"></a><span data-ttu-id="e1c59-125">ブックに何というフィールドが表示されますか ?</span><span class="sxs-lookup"><span data-stu-id="e1c59-125">What fields will be shown in the workbook?</span></span>
<span data-ttu-id="e1c59-126">ワークブックに追加される既定のフィールドは、エンティティのキー フィールドと必須フィールドです。</span><span class="sxs-lookup"><span data-stu-id="e1c59-126">The default fields that will be added into the workbook are the key and mandatory fields of the entity.</span></span> <span data-ttu-id="e1c59-127">デフォルトで別のフィールドセットを提供する必要がある場合は、これらのフィールドをエンティティの **自動レポートのフィールド グループ** に追加できます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-127">If a different set of fields should be provided by default, then those fields can be added into the **AutoReport field group** on the entity.</span></span> <span data-ttu-id="e1c59-128">次の図は、FMCustomerEntity の AutoReport フィールド グループの Visual Studio  ビューを示しています。</span><span class="sxs-lookup"><span data-stu-id="e1c59-128">The following image shows the Visual Studio view of the AutoReport field group for the FMCustomerEntity.</span></span>

<span data-ttu-id="e1c59-129">[![AutoReport フィールド グループの Visual Studio ビュー](./media/off101c.png)](./media/off101c.png)</span><span class="sxs-lookup"><span data-stu-id="e1c59-129">[![Visual Studio view of AutoReport field group](./media/off101c.png)](./media/off101c.png)</span></span>

## <a name="what-fields-will-be-shown-when-an-entity-is-the-target-of-a-lookup"></a><span data-ttu-id="e1c59-130">エンティティが検索の対象のとき、何というフィールドが表示されますか ?</span><span class="sxs-lookup"><span data-stu-id="e1c59-130">What fields will be shown when an entity is the target of a lookup?</span></span>
<span data-ttu-id="e1c59-131">2 つのエンティティ間のリレーションシップが定義されると、1 つのエンティティの識別子が他のエンティティに表示されている場合、そのルックアップに表示されるフィールドは、キー フィールドであるか、または **AutoLookup フィールド グループ** が空でない場合はそのグループ内のフィールドです。</span><span class="sxs-lookup"><span data-stu-id="e1c59-131">When a relationship is defined between two entities, if the identifier for one entity is shown on the other entity, then the fields that will be shown in that lookup are either the key fields, or the fields in the **AutoLookup field group** if it is not empty.</span></span> <span data-ttu-id="e1c59-132">関係の参照は現在サポートされていませんが、最終的に列挙のルックアップを同様の方法でアプリに表示されます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-132">Relationship lookups are not currently supported, but they will eventually be displayed in the app in a similar way to the enumeration lookups.</span></span> <span data-ttu-id="e1c59-133">列挙ルックアップを持つ Excel アドインを次に示します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-133">The Excel Add-in with an enumeration lookup is shown below.</span></span>

<span data-ttu-id="e1c59-134">[![列挙型ルックアップによる Excel アドイン](./media/off101d.png)](./media/off101d.png)</span><span class="sxs-lookup"><span data-stu-id="e1c59-134">[![Excel Add-in with an enumeration lookup](./media/off101d.png)](./media/off101d.png)</span></span>

## <a name="what-should-be-done-to-make-an-entity-ready-for-use-in-excel"></a><span data-ttu-id="e1c59-135">エンティティを Excel で使用できるようにするには何を行う必要がありますか ?</span><span class="sxs-lookup"><span data-stu-id="e1c59-135">What should be done to make an entity ready for use in Excel?</span></span>
<span data-ttu-id="e1c59-136">AutoReport および AutoLookup フィールド グループを定義し、Excel アプリ デザイン エクスペリエンスを使用してテストします。</span><span class="sxs-lookup"><span data-stu-id="e1c59-136">Define the AutoReport and AutoLookup field groups and test them using the Excel App design experience.</span></span>

## <a name="why-does-an-automatically-added-entity-option-have-unfiltered-after-the-entity-name"></a><span data-ttu-id="e1c59-137">自動的に追加されたエンティティ オプションでエンティティ名の後に「(フィルターなし)」と表示されるのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="e1c59-137">Why does an automatically added entity option have “(unfiltered)” after the entity name?</span></span>
<span data-ttu-id="e1c59-138">現在、フィルターはこれらのオプションに追加されないため、「(フィルターなし)」という用語になります。</span><span class="sxs-lookup"><span data-stu-id="e1c59-138">Currently, a filter is not added to these options, hence the term “(unfiltered)”.</span></span> <span data-ttu-id="e1c59-139">今後、フォームからこれらのオプションへのフィルターの適用が試行されます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-139">In the future, an attempt will be made to apply the filter from the form to these options.</span></span> <span data-ttu-id="e1c59-140">たとえば、顧客の一覧がカリフォルニア州で顧客だけにフィルター処理された場合、今後エンティティは州フィールドに対してスキャンされ、見つかるとフィルターは自動で追加されます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-140">For example, if a list of Customers was filtered to just Customers in the state of California, then, in the future, the entity will be scanned for the state field and if it is found then a filter would be added automatically.</span></span>

## <a name="how-can-an-entity-be-added-as-an-open-in-excel-option-on-a-form-that-doesnt-share-the-same-root-datasource"></a><span data-ttu-id="e1c59-141">同じルート データソースを共有しないフォーム上で、Excel で開くオプションとしてエンティティを追加するにはどうしたらいいですか。</span><span class="sxs-lookup"><span data-stu-id="e1c59-141">How can an entity be added as an Open in Excel option on a form that doesn’t share the same root datasource?</span></span>
<span data-ttu-id="e1c59-142">生成された Excel で開くオプションは、OfficeIGeneratedWorkbookCustomExporter インターフェイスを実装することにより、任意のフォームに追加できます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-142">A generated Open in Excel option can be added on any form by implementing the OfficeIGeneratedWorkbookCustomExporter interface.</span></span> <span data-ttu-id="e1c59-143">生成されたオプションをプログラムで追加するとき、一組のフィールドを明示的に指定できます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-143">When adding a generated option programmatically, the set of fields can be explicitly specified.</span></span> <span data-ttu-id="e1c59-144">詳細については、[インターフェイスを通じた Office で開くメニューの変更](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/office-integration/customize-open-office-menu#modifying-the-open-in-office-menu-through-interfaces)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e1c59-144">For more information, see [Modifying the Open in Office menu through interfaces](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/office-integration/customize-open-office-menu#modifying-the-open-in-office-menu-through-interfaces).</span></span>

## <a name="what-are-the-region-specific-considerations-for-defining-entities"></a><span data-ttu-id="e1c59-145">エンティティを定義するための地域固有の考慮事項</span><span class="sxs-lookup"><span data-stu-id="e1c59-145">What are the region-specific considerations for defining entities?</span></span>
<span data-ttu-id="e1c59-146">[Excel で開く] により生成されたエクスペリエンスは、AutoLookup グループに地域固有のフィールドを追加することで地域固有にできます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-146">The Open in Excel generated experiences can be made region-specific by adding region-specific fields into the AutoLookup group.</span></span> <span data-ttu-id="e1c59-147">これらの領域固有のフィールドは、生成されたワークブックに含まれます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-147">These region-specific fields will then be included in the generated workbook.</span></span>

## <a name="how-can-i-create-a-custom-lookup-for-an-entity-field-in-excel"></a><span data-ttu-id="e1c59-148">Excel でのエンティティ フィールドに対してどのようにカスタム ルックアップを作成しますか。</span><span class="sxs-lookup"><span data-stu-id="e1c59-148">How can I create a custom lookup for an entity field in Excel?</span></span>
<span data-ttu-id="e1c59-149">カスタム ルックアップでは、エンティティ フィールドを表示できます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-149">A custom lookup can be shown for an Entity field.</span></span>

-   <span data-ttu-id="e1c59-150">名前 - メソッドには、「lookup\_&lt;フィールド名&gt;」の名前が必要です。例: フィールド「MyField」は、ルックアップ メソッド「lookup\_MyField」とすることができます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-150">Name - The method needs to have a name that is “lookup\_&lt;fieldname&gt;” e.g. a field “MyField” could have a lookup method “lookup\_MyField”.</span></span>
-   <span data-ttu-id="e1c59-151">属性 – 属性をメソッドに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e1c59-151">Attributes – Attributes need to be added to the method:</span></span>
    -   <span data-ttu-id="e1c59-152">SysODataActionAttribute(str &lt;name&gt;, Boolean &lt;isInstanceMethod&gt;)</span><span class="sxs-lookup"><span data-stu-id="e1c59-152">SysODataActionAttribute(str &lt;name&gt;, Boolean &lt;isInstanceMethod&gt;)</span></span>
    -   <span data-ttu-id="e1c59-153">SysODataCollectionAttribute(str &lt;name&gt;, Types &lt;type&gt;, “Value”)</span><span class="sxs-lookup"><span data-stu-id="e1c59-153">SysODataCollectionAttribute(str &lt;name&gt;, Types &lt;type&gt;, “Value”)</span></span>
-   <span data-ttu-id="e1c59-154">戻り値: メソッドは、文字列のリストを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e1c59-154">Return – The method should return a list of strings.</span></span>

<span data-ttu-id="e1c59-155">**例**</span><span class="sxs-lookup"><span data-stu-id="e1c59-155">**Example**</span></span> 

```xpp
public class ExportToExcel_SimpleEntity extends common
{
    [SysODataActionAttribute("Lookup_StringLookupField", true),
    SysODataCollectionAttribute("return", Types::String, "Value")]
    public List lookup_StringLookupField()
    {
        List lookupList = new List(Types::String);
        const int items = 5;

        for (int item = 0; item < items; item++)
        {
            lookupList.addEnd(strfmt('%1 - %2 (%3)', this.StringField, this.IntField, item));
        }

        return lookupList;
    }
}
```

## <a name="how-does-the-app-get-injected-into-a-workbook-to-start-building-a-template"></a><span data-ttu-id="e1c59-156">アプリはどのようにテンプレートの構築を開始するブックに挿入されますか。</span><span class="sxs-lookup"><span data-stu-id="e1c59-156">How does the app get injected into a workbook to start building a template?</span></span>

<span data-ttu-id="e1c59-157">Excel アドインは、生成された [Excel で開く] エクスペリエンスがトリガーされたとき、または **一般** &gt; **一般** &gt; **Office 統合** &gt; **Excel ブック デザイナー** フォームを使用してブックが作成されたときに、ブックに挿入されます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-157">The Excel Add-in is injected into a workbook when a generated Open in Excel experience is triggered or when a workbook is created using the **Common** &gt; **Common** &gt; **Office integration** &gt; **Excel workbook designer** form.</span></span>

-   <span data-ttu-id="e1c59-158">**ブックの作成** ボタンは、選択したエンティティおよびフィールド、ポインターをサーバーに、アプリをブックに追加します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-158">The **Create workbook** button will add the selected entity and fields, a pointer to the server, and the app into a workbook.</span></span>
-   <span data-ttu-id="e1c59-159">**空白ブックの作成** ボタンは、ポインターをサーバーに、アプリをブックにそのまま追加します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-159">The **Create blank workbook** button will simply add a pointer to the server and the app into a workbook.</span></span>
-   <span data-ttu-id="e1c59-160">**ビュー関連** フォームは、Excel で加えられたデータの変更の影響をより簡単に確認するため、現在選択されているエンティティに関連するフォームに移動します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-160">The **View related** form will navigate to the form relating to the currently selected entity to more easily review the effect of data changes made in Excel.</span></span>
-   <span data-ttu-id="e1c59-161">**エンティティ レコード数を取得** ボタンは、現在選択されているエンティティのレコード数を表示します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-161">The **Get entity record count** button will show the record count for the currently selected entity.</span></span> <span data-ttu-id="e1c59-162">Excel アドインは、ユーザーのコンピューターのメモリ制限内の大量のデータを処理します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-162">The Excel Add-in will handle large sets of data within the memory limits of a user's machine.</span></span> <span data-ttu-id="e1c59-163">既定の Excel アドインにはデータ サイズが 100 万個のセルに制限されるデータ ガバナーがありますが、ユーザーのコンピューターの性能に応じて通常 250 万個程度のセルに拡張できます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-163">By default, the Excel Add-in has a data governor that restricts the data size to one million cells but, depending on the performance abilities of the user's machine, this can usually be extended to around 2.5 million cells.</span></span>

<span data-ttu-id="e1c59-164">次の図は、**Excel ブック デザイナー** フォームを示しています。</span><span class="sxs-lookup"><span data-stu-id="e1c59-164">The following image shows the **Excel workbook designer** form.</span></span>

<span data-ttu-id="e1c59-165">[![Excel ブック デザイナー フォーム](./media/off101e.png)](./media/off101e.png)</span><span class="sxs-lookup"><span data-stu-id="e1c59-165">[![Excel workbook designer form](./media/off101e.png)](./media/off101e.png)</span></span> 

<span data-ttu-id="e1c59-166">Excel アドインを含むワークブックを取得すると、追加のデータソースは、**デザイン** ボタンを使用して追加することができます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-166">After obtaining a workbook containing the Excel Add-in, additional datasources can be added using the **Design** button.</span></span> <span data-ttu-id="e1c59-167">現在、データ ソースを削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="e1c59-167">Currently, datasources cannot be removed.</span></span> 

## <a name="when-will-a-template-show-as-an-open-in-excel-option"></a><span data-ttu-id="e1c59-168">テンプレートはいつ [Excel で開く] オプションとして表示されますか ?</span><span class="sxs-lookup"><span data-stu-id="e1c59-168">When will a template show as an Open in Excel option?</span></span>
<span data-ttu-id="e1c59-169">**共通** &gt; **共通** &gt; **Office 統合** &gt; **ドキュメント テンプレート** フォーム (DocuTemplate) に表示されているテンプレートで、ShowInOpenInOfficeMenu が "はい" に設定されていて、ルート データ ソース (テーブル) が現在のフォームと同じとき、そのテンプレートは、Microsoft Office で開くメニューの Excel で開くセクションのオプションとして追加されます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-169">When a template listed in the **Common** &gt; **Common** &gt; **Office integration** &gt; **Document templates** form (DocuTemplate) has ShowInOpenInOfficeMenu set to Yes and has the same root datasource (table) as the current form, it will be added as an option in the Open in Excel section of the Open in Microsoft Office menu.</span></span> <span data-ttu-id="e1c59-170">次の図は、**ドキュメント テンプレート** フォームを示しています。</span><span class="sxs-lookup"><span data-stu-id="e1c59-170">The following image shows the **Document templates** form.</span></span>

<span data-ttu-id="e1c59-171">[![ドキュメント テンプレート フォーム](./media/off101g.png)](./media/off101g.png)</span><span class="sxs-lookup"><span data-stu-id="e1c59-171">[![Document templates form](./media/off101g.png)](./media/off101g.png)</span></span>

## <a name="will-a-filter-be-added-to-the-template"></a><span data-ttu-id="e1c59-172">フィルターはテンプレートに追加されますか。</span><span class="sxs-lookup"><span data-stu-id="e1c59-172">Will a filter be added to the template?</span></span>
<span data-ttu-id="e1c59-173">**ドキュメント テンプレート** フォームでは、「現在のレコード」の標準フィルターを有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="e1c59-173">In the **Document Templates** form, the standard filter for “current record” can be turned on and off.</span></span> <span data-ttu-id="e1c59-174">テンプレートが Excel で開くオプションとして呼び出されたときにフィルターがオンになっている場合、現在のレコードのフィルターがワークブックに追加されます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-174">If the filter is on, when the template is invoked as an Open in Excel option, then a filter for the current record will be added to the workbook.</span></span> <span data-ttu-id="e1c59-175">フィルターはキー フィールドとその値になります。</span><span class="sxs-lookup"><span data-stu-id="e1c59-175">The filter will be the key fields and their values.</span></span>

## <a name="how-can-templates-be-defined-in-metadata-and-code-and-loaded-automatically"></a><span data-ttu-id="e1c59-176">テンプレートはどのようにメタデータとコードで定義されるおよび自動的に読み込まれますか。</span><span class="sxs-lookup"><span data-stu-id="e1c59-176">How can templates be defined in metadata and code and loaded automatically?</span></span>
<span data-ttu-id="e1c59-177">**ドキュメント テンプレートの** フォームにテンプレートを追加するとき、それはそのインスタンスに追加され、「ユーザー定義」のテンプレートと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-177">When adding a template into the **Document Templates** form, it is added for that instance and is referred to as a “user-defined” template.</span></span> <span data-ttu-id="e1c59-178">テンプレートは、メタデータおよびコードで定義することもでき、自動的に読み込まれるため、「システム定義」のテンプレートになります。</span><span class="sxs-lookup"><span data-stu-id="e1c59-178">Templates can also be defined in metadata and code and loaded automatically, thus making them “system-defined” templates.</span></span> <span data-ttu-id="e1c59-179">メタデータとコードを使用してシステム定義のテンプレートを作成するには、以下を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e1c59-179">To create a system-defined template using metadata and code, you need to do the following:</span></span>

-   <span data-ttu-id="e1c59-180">テンプレートの定義。</span><span class="sxs-lookup"><span data-stu-id="e1c59-180">Define the template.</span></span>
-   <span data-ttu-id="e1c59-181">プロジェクトに新しいリソースを作成します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-181">Create a new resource in a project.</span></span>
-   <span data-ttu-id="e1c59-182">DocuTemplateRegistrationBase クラスを拡張する新しいクラスを定義し、registerTemplates メソッドの実装を追加します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-182">Define a new class that extends the DocuTemplateRegistrationBase class and add an implementation of the registerTemplates method.</span></span>

<span data-ttu-id="e1c59-183">LedgerJournalLineEntryTemplateRegistration および FMTemplateRegistrations クラスは、コードで定義されたテンプレート登録の良い例です。</span><span class="sxs-lookup"><span data-stu-id="e1c59-183">The LedgerJournalLineEntryTemplateRegistration and FMTemplateRegistrations classes are good examples of template registrations defined in code.</span></span> <span data-ttu-id="e1c59-184">LedgerJournalLineEntryTemplate および FMTemplateCustomersWithLocations リソースは、リソースとしてメタデータに格納された対応するテンプレートです。</span><span class="sxs-lookup"><span data-stu-id="e1c59-184">The LedgerJournalLineEntryTemplate and FMTemplateCustomersWithLocations resources are the corresponding templates stored in metadata as resources.</span></span> <span data-ttu-id="e1c59-185">テンプレートに登録クラスが存在するとき、そのテンプレートは、**ドキュメント テンプレート** フォームの **システム テンプレートの再読み込み** ボタンがクリックされたときに読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-185">When a template has a registration class, it will be loaded when the **Reload system templates** button is clicked in the **Document Templates** form.</span></span>

## <a name="how-do-templates-get-loaded-into-a-fresh-deployment"></a><span data-ttu-id="e1c59-186">テンプレートはどのように新しい展開に読み込まれますか？</span><span class="sxs-lookup"><span data-stu-id="e1c59-186">How do templates get loaded into a fresh deployment?</span></span>
<span data-ttu-id="e1c59-187">システム定義のテンプレートを読み込むには、次に示すように、**Common**&gt;**Common**&gt;**Office 統合**&gt;**ドキュメント テンプレート** フォームの **システム テンプレートを再読込み** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1c59-187">To load system defined templates, click the **Reload system templates** button in the **Common** &gt; **Common** &gt; **Office integration** &gt; **Document templates** form, as shown below.</span></span>

<span data-ttu-id="e1c59-188">[![システム テンプレート ボタンの再読み込み](./media/off101h.png)](./media/off101h.png)</span><span class="sxs-lookup"><span data-stu-id="e1c59-188">[![Reload system templates button](./media/off101h.png)](./media/off101h.png)</span></span> 

<span data-ttu-id="e1c59-189">今後、配置の際にそのボタンのクリックに相当する操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-189">In the future, we will do the equivalent of clicking that button during deployment.</span></span>

## <a name="how-do-i-decide-if-i-should-create-a-template"></a><span data-ttu-id="e1c59-190">テンプレートを作成する必要があるかどうかをどのように決定しますか。</span><span class="sxs-lookup"><span data-stu-id="e1c59-190">How do I decide if I should create a template?</span></span>
<span data-ttu-id="e1c59-191">テンプレートは、管理とバージョン管理する必要なコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="e1c59-191">A template is an artifact that needs to be maintained and versioned.</span></span> <span data-ttu-id="e1c59-192">ユーザー エクスペリエンスを低下させることがなく、テンプレートを定義することを避けることができれば、おそらくテンプレートを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e1c59-192">If you can avoid defining a template without sacrificing much from the user experience, then you probably should use a template.</span></span> <span data-ttu-id="e1c59-193">次の場合にテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-193">Create a template if:</span></span>

-   <span data-ttu-id="e1c59-194">テンプレートに追加のコンテンツまたは書式が必要な場合。</span><span class="sxs-lookup"><span data-stu-id="e1c59-194">You need additional content or formatting in the template.</span></span>
-   <span data-ttu-id="e1c59-195">同じブック内の複数のエンティティとデータ ソースを結合する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e1c59-195">You want to combine multiple entities/datasources in the same workbook.</span></span>

<span data-ttu-id="e1c59-196">テンプレートを作成しない場合:</span><span class="sxs-lookup"><span data-stu-id="e1c59-196">Don’t create a template if:</span></span>

-   <span data-ttu-id="e1c59-197">テーブル バインドに表示するフィールドのセットを指定するだけです。</span><span class="sxs-lookup"><span data-stu-id="e1c59-197">You can just specify a set of fields to show in a table binding.</span></span>

## <a name="what-are-the-region-specific-considerations-for-templates"></a><span data-ttu-id="e1c59-198">テンプレートのための地域固有の考慮事項</span><span class="sxs-lookup"><span data-stu-id="e1c59-198">What are the region-specific considerations for templates?</span></span>
<span data-ttu-id="e1c59-199">地域固有フィールドを持つエンティティのテンプレートを作成するとき、テンプレートからそれらの地域固有フィールドを除外する必要があります。そうしない場合、すべてのユーザーに地域固有フィールドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-199">When creating a template for an entity that has region-specific fields, you should leave those region-specific fields out of the template, otherwise all users will see the region-specific fields.</span></span> <span data-ttu-id="e1c59-200">テンプレートは、ユーザーの大半に既定で提供される必要があり、地域に固有のユーザーは Excel アドインの使いやすいデザイン エクスペリエンスを使用してこれらのフィールドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-200">Templates should cater to the majority of users by default and region-specific users can add those fields using the easy-to-use design experience of the Excel Add-in.</span></span>  <span data-ttu-id="e1c59-201">必要に応じて、ユーザーはリージョン固有のフィールドと列を追加できます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-201">The region-specific fields and columns can be added by users as needed.</span></span> <span data-ttu-id="e1c59-202">そのテンプレートは、1 人のユーザーが再利用するためにローカル コンピューターに保存するか、そのインスタンスの任意のユーザーが再利用するためにドキュメント テンプレートを通じてアップロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-202">That template can be either saved to local computer for reuse by a single user or uploaded via the Document Templates form for reuse by any user of that instance.</span></span> <span data-ttu-id="e1c59-203">いくつかの他の考慮事項。</span><span class="sxs-lookup"><span data-stu-id="e1c59-203">A couple of other considerations:</span></span>

-   <span data-ttu-id="e1c59-204">領域に領域固有のエンティティがある場合、領域固有のテンプレートを作成できます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-204">If a region has a region-specific entity, then a region-specific template could be created.</span></span>
-   <span data-ttu-id="e1c59-205">地域が十分に重要な場合は、地域固有テンプレートと地域汎用テンプレートを定義できます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-205">If a region is important enough, then you could define a region-specific template as well as a region-generic template.</span></span>

## <a name="how-do-i-add-an-explicit-button-for-a-template-open-in-excel-option"></a><span data-ttu-id="e1c59-206">テンプレート Excel を開くオプションに明示的なボタンを追加する方法がありますか。</span><span class="sxs-lookup"><span data-stu-id="e1c59-206">How do I add an explicit button for a template Open in Excel option?</span></span>

<span data-ttu-id="e1c59-207">Excel で開くエクスペリエンスに明示的なボタンを追加できます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-207">An explicit button can be added for Open in Excel experiences.</span></span> <span data-ttu-id="e1c59-208">ボタンに表示されるラベルは、通常、「Excel で開くターゲット」である必要があります。ターゲットは、「明細行」や「カタログ」などのターゲット データの名前です。</span><span class="sxs-lookup"><span data-stu-id="e1c59-208">The label shown on the button should usually be “Open target in Excel” where target is the name of the target data like “lines” or “catalog”.</span></span> <span data-ttu-id="e1c59-209">そのようなボタンの背後にあるコードは次のようになります:</span><span class="sxs-lookup"><span data-stu-id="e1c59-209">The code behind such a button will:</span></span>

-   <span data-ttu-id="e1c59-210">使用されるテンプレートを取得します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-210">Obtain the template to be used.</span></span>
-   <span data-ttu-id="e1c59-211">フィルターを追加します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-211">Add a filter.</span></span>
-   <span data-ttu-id="e1c59-212">テンプレートをユーザーに渡します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-212">Pass the template to the user.</span></span>

<span data-ttu-id="e1c59-213">このコードの例としては、**LedgerJournalTable** フォーム (**一般会計**&gt;**仕訳帳**&gt;**一般仕訳帳**) の **クリック済み** メソッド内の **OpenLinesInExcel** ボタン上で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-213">An example of this code can be found on the **LedgerJournalTable** form (**General ledger** &gt; **Journals** &gt; **General journal**) in the **Clicked** method on the **OpenLinesInExcel** button.</span></span>

```xpp
[Control("Button")]
class OpenLinesInExcel
{

    /// <summary>
    /// Opens the current journal in Excel for line entry and editing
    /// </summary>
    public void clicked()
    {
        super();

        const str templateName = resourceStr(LedgerJournalLineEntryTemplate);
                DocuTemplate template = DocuTemplate::findTemplate(OfficeAppApplicationType::Excel, templateName);

        // Ensure the template was present
        if (template && template.TemplateID == templateName)
        {
            Map filtersToApply = new Map(Types::String, Types::String);

            // Create lines filter
            ExportToExcelFilterBuilder filterBuilder = new ExportToExcelFilterBuilder(tablestr(LedgerJournalLineEntity));
            str filterString = filterBuilder.areEqual(fieldstr(LedgerJournalLineEntity, JournalBatchNumber), LedgerJournalTable.JournalNum);
            filtersToApply.insert(tablestr(LedgerJournalLineEntity), filterString);

            // Create header filter
            filterBuilder = new ExportToExcelFilterBuilder(tablestr(LedgerJournalHeaderEntity));
            filterString = filterBuilder.areEqual(fieldstr(LedgerJournalHeaderEntity, JournalBatchNumber), LedgerJournalTable.JournalNum);
            filtersToApply.insert(tablestr(LedgerJournalHeaderEntity), filterString);

            // Generate the workbook using the template and filters
            DocuTemplateRender renderer = new DocuTemplateRender();
            str documentUrl = renderer.renderTemplateToStorage(template, filtersToApply);

            // Pass the workbook to the user
            if (documentUrl)
            {
                Browser b = new Browser();
                b.navigate(documentUrl, false, false);
            }
            else
            {
                error(strFmt("@ApplicationFoundation:DocuTemplateGenerationFailed", templateName));
            }
        }
        else
        {
            warning(strFmt("@ApplicationFoundation:DocuTemplateNotFound", templateName));
        }
    }

}
```

<span data-ttu-id="e1c59-214">次の図は、**総勘定元帳** &gt; **仕訳帳** &gt; **一般仕訳帳** フォームを強調表示された **Excel で明細行を開く** ボタンと共に示しています。</span><span class="sxs-lookup"><span data-stu-id="e1c59-214">The following image shows the **General ledger** &gt; **Journals** &gt; **General journal** form with the **Open lines in Excel** button highlighted.</span></span> 

<span data-ttu-id="e1c59-215">[![Excel ボタンで開いた明細行を強調表示](./media/off101i.png)](./media/off101i.png)</span><span class="sxs-lookup"><span data-stu-id="e1c59-215">[![Highlighted Open lines in Excel button](./media/off101i.png)](./media/off101i.png)</span></span>

<span data-ttu-id="e1c59-216">作成された Open in Excel オプションとテンプレートの Open in Excel オプションをプログラムで追加するには、ExportToExcelIGeneratedCustomExport および ExportToExcelITemplateCustomExport インターフェイスを実装して、Open in Excel オプションを追加します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-216">To programmatically add generated and template Open in Excel options, Open in Excel options can be added by implementing the ExportToExcelIGeneratedCustomExport and ExportToExcelITemplateCustomExport interfaces.</span></span> <span data-ttu-id="e1c59-217">これにより、エンティティまたはテンプレートがルート データ ソースと同じテーブルを持たないフォームにオプションを追加できます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-217">This allows the addition of options to forms where the entity or template doesn’t have the same table as the root datasource.</span></span> <span data-ttu-id="e1c59-218">この機能を使用する場合の例としてはデータソースのないフォーム、フォーム パーツのコレクションのみを含む可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e1c59-218">An example of when you would use this capability is on forms without a datasource, potentially containing only a collection of form parts.</span></span> <span data-ttu-id="e1c59-219">次の例では、**FMRental** フォームに、生成されたテンプレートと ExcelのOpen in Excel オプションをプログラムによって追加します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-219">The following example adds generated and template Open in Excel options programmatically to the **FMRental** form.</span></span>

```xpp
[Form]
public class FMRental extends FormRun implements ExportToExcelIGeneratedCustomExport, ExportToExcelITemplateCustomExport
{    
...

    public List getExportOptions()
    {
        List exportOptions = new List(Types::Class);

        ExportToExcelExportOption exportOption = ExportToExcelExportOption::construct(ExportToExcelExportType::CustomGenerated, int2str(1));
        exportOption.setDisplayNameWithDataEntity(tablestr(FMRentalEntity));
        exportOptions.addEnd(exportOption);

        ExportToExcelExportOption exportOption2 = ExportToExcelExportOption::construct(ExportToExcelExportType::CustomTemplate, int2str(2));
        exportOption2.displayName("Analyze rentals");
        exportOptions.addEnd(exportOption2);

        return exportOptions;
    }

    public ExportToExcelDataEntityContext getDataEntityContext(ExportToExcelExportOption _exportOption)
    {
        ExportToExcelDataEntityContext context = null;

        if (_exportOption.id() == int2str(1))
        {
            context = ExportToExcelDataEntityContext::construct(tablestr(FMRentalEntity), tablefieldgroupstr(FMRentalEntity, AutoReport));
        }

        return context;
    }

    public System.IO.Stream getTemplate(ExportToExcelExportOption _exportOption)
    {
        System.IO.Stream stream = null;

        if (_exportOption.id() == int2str(2))
        {
            stream = Microsoft.Dynamics.Ax.Xpp.MetadataSupport::GetResourceContentStream(resourcestr(FMRentalEditableExportTemplate));
        }

        return stream;
    }

    public void updateTemplateSettings(ExportToExcelExportOption _exportOption, Microsoft.Dynamics.Platform.Integration.Office.ExportToExcelHelper.SettingsEditor _settingsEditor)
    {
    }
...
```

## <a name="how-do-i-add-a-filter-for-a-programmatically-added-template-open-in-excel-option"></a><span data-ttu-id="e1c59-220">プログラムにより追加するテンプレート Excel を開くオプション用のフィルターを追加する方法がありますか。</span><span class="sxs-lookup"><span data-stu-id="e1c59-220">How do I add a filter for a programmatically-added template Open in Excel option?</span></span>

<span data-ttu-id="e1c59-221">Excel で開く オプション テンプレートは、ExportToExcelITemplateCustomExport インターフェイスを実装し、getTemplate メソッドでテンプレートを提供することで、プログラムにより追加できます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-221">A template Open in Excel option can be programmatically added by implementing the ExportToExcelITemplateCustomExport interface and providing a template in the getTemplate method.</span></span> <span data-ttu-id="e1c59-222">このオプションのフィルターは、updateTemplateSettings メソッドの ExportToExcelFilterBuilder API を使用してプログラムで追加できます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-222">A filter for that option can be programmatically added by using the ExportToExcelFilterBuilder API in the updateTemplateSettings method.</span></span>

```xpp
public void updateTemplateSettings(ExportToExcelExportOption _exportOption, Microsoft.Dynamics.Platform.Integration.Office.ExportToExcelHelper.SettingsEditor _settingsEditor)

{

_settingsEditor.SetFilterExpression(tableStr(RetailTmpBulkProductAttributeValueEntity), element.getExportToExcelFilterExpression());

DictDataEntity dictDataEntity = new DictDataEntity(tableNum(RetailTmpBulkProductAttributeValueEntity));

_settingsEditor.SetFilterExpressionByPublicName(dictDataEntity.publicEntityName(), element.getExportToExcelFilterExpression());

}
```

<span data-ttu-id="e1c59-223">フィルターがプログラムで追加された後、結果のフィルターは、**フィルター** ボタンを使用して Excel アドインで表示できます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-223">After a filter has been added programmatically, the resulting filter can be viewed in the Excel Add-in using the **Filter** button.</span></span> <span data-ttu-id="e1c59-224">次の図は、**フィルター** ボタンが強調表示された Excel アドインを示しています。</span><span class="sxs-lookup"><span data-stu-id="e1c59-224">The following image shows the Excel Add-in with the **Filter** button highlighted.</span></span>

<span data-ttu-id="e1c59-225">[![強調表示されたフィルター ボタン](./media/off101j.png)](./media/off101j.png)</span><span class="sxs-lookup"><span data-stu-id="e1c59-225">[![Highlighted Filter button](./media/off101j.png)](./media/off101j.png)</span></span> 

<span data-ttu-id="e1c59-226">次の図は、**フィルター** ダイアログ ボックスが強調表示された Excel アドインを示しています。</span><span class="sxs-lookup"><span data-stu-id="e1c59-226">The following image shows the Excel Add-in with the **Filter** dialog box opened.</span></span>

<span data-ttu-id="e1c59-227">[![開いたフィルター ダイアログ ボックス](./media/off101k.png)](./media/off101k.png)</span><span class="sxs-lookup"><span data-stu-id="e1c59-227">[![Filter dialog box opened](./media/off101k.png)](./media/off101k.png)</span></span>

## <a name="how-do-i-enable-relationship-lookups-in-excel"></a><span data-ttu-id="e1c59-228">Excel でリレーションシップ ルックアップをどのように有効にしますか。</span><span class="sxs-lookup"><span data-stu-id="e1c59-228">How do I enable relationship lookups in Excel?</span></span>
<span data-ttu-id="e1c59-229">Excel データ コネクタでリレーションシップ ルックアップを有効にするには、次のメタデータが設定されていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e1c59-229">To enable relationship lookups in the Excel Data Connector, you must ensure that the following metadata is set.</span></span>

- <span data-ttu-id="e1c59-230">関係で定義されているロールと関連データ エンティティ ロールは、ソースおよびターゲット エンティティの両方のすべての関係間で一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="e1c59-230">The Role and Related Data Entity Role defined on the relationship need to be unique among all relationships on both the source and target entity.</span></span> <span data-ttu-id="e1c59-231">これは、DimensionCombinationEntity など多くのリレーションシップを持つエンティティのリレーションシップにとって特に重要です。</span><span class="sxs-lookup"><span data-stu-id="e1c59-231">This is particularly important for relationships involving entities with lots of relationships, such as DimensionCombinationEntity.</span></span> <span data-ttu-id="e1c59-232">予想されるルックアップが表示されない場合は、ロール名を次の形式に変更してみます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-232">If you're not seeing an expected lookup, try changing the role names to the following format:</span></span>

   - <span data-ttu-id="e1c59-233">**ロール**: \[このエンティティのパブリック名\] + \[ターゲット エンティティのパブリック名\] + \[ターゲット エンティティ フィールド\] + 「ソース」</span><span class="sxs-lookup"><span data-stu-id="e1c59-233">**Role**: \[this entity's public name\] + \[target entity's public name\] + \[target entity field\] + "Source"</span></span>
   - <span data-ttu-id="e1c59-234">**関連データ エンティティ ロール**: \[このエンティティのパブリック名\] + \[ターゲット エンティティのパブリック名\] + \[ターゲット エンティティ フィールド\] + 「ターゲット」</span><span class="sxs-lookup"><span data-stu-id="e1c59-234">**Related Data Entity Role**: \[this entity's public name\] + \[target entity's public name\] + \[target entity field\] + "Target"</span></span>

  - <span data-ttu-id="e1c59-235">カーディナリティと関連データ エンティティ カーディナリティは、適切に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e1c59-235">The Cardinality and Related Data Entity Cardinality need to be set appropriately.</span></span>
  -  <span data-ttu-id="e1c59-236">少なくとも 1 つの制約がリレーションシップに追加される必要があます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-236">At least one constraint must be added to the relationship.</span></span> <span data-ttu-id="e1c59-237">特殊なケースである、分析コード関係の例外により、制約されたプロパティは両方とも公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e1c59-237">With the exception of dimension relationships, which are a special case, the properties constrained must both be public.</span></span>

## <a name="how-can-i-enable-users-to-create-new-header-records-as-well-as-lines-in-a-workbook"></a><span data-ttu-id="e1c59-238">ブック内の明細行と共に新しいヘッダー レコードを作成するユーザーをどのように有効にできますか。</span><span class="sxs-lookup"><span data-stu-id="e1c59-238">How can I enable users to create new header records as well as lines in a workbook?</span></span>
<span data-ttu-id="e1c59-239">ヘッダー レコードと関連行の作成を有効にするには、ヘッダー データソースを「フィールド」のセットとして追加し、行データ ソースを関連テーブルとして追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e1c59-239">To enable creation of header records and related lines, the header data source must be added as a set of "fields" and the lines data source must be added as a related table.</span></span> <span data-ttu-id="e1c59-240">このパターンは、仕訳入力などの文書データ入力シナリオでうまく機能します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-240">This pattern can work well for document data entry scenarios such as Journal entry.</span></span>

<span data-ttu-id="e1c59-241">ヘッダー レコードと関連行の詳細については、「[Dynamics 365 for Finance and Operations でヘッダーと明細行のパターンの Excel テンプレートを作成する](https://youtu.be/RTicLb-6dbI)」ビデオをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="e1c59-241">To learn more about header records and related lines, watch the short [Create an Excel template for header and line patterns in Dynamics 365 for Finance and Operations](https://youtu.be/RTicLb-6dbI) video.</span></span>

<span data-ttu-id="e1c59-242">ヘッダーの作成を有効にするヘッダー フィールドと行テーブルを含むブックを設計するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-242">To design a workbook with header fields and a lines table that enables header creation:</span></span>
1. <span data-ttu-id="e1c59-243">Excel アドインで、**デザイン** をクリックしてデザイナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-243">In the Excel Add-in, click **Design** to open the Designer.</span></span> <span data-ttu-id="e1c59-244">**フィールドを追加** を選択してヘッダー データ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-244">Select **Add fields** to add a header data source.</span></span>
2. <span data-ttu-id="e1c59-245">使用するヘッダー フィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-245">Select the header fields that you want to use.</span></span> <span data-ttu-id="e1c59-246">すべてのキー フィールドを含めるか、**新規** ボタンを有効にしないでください。</span><span class="sxs-lookup"><span data-stu-id="e1c59-246">Be sure to include all the key fields or the **New** button won't be enabled.</span></span>
3. <span data-ttu-id="e1c59-247">すべての文字列ヘッダー値フィールドでは、ドロップダウン メニューの形式で **Excel リボン > ホーム タブ > 番号グループ > 「数値」の設定** を使用するそのセルの「テキスト」形式を手動で適用します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-247">For all of the string header value fields, manually apply "Text" format for that cell using **Excel ribbon > Home tab > Number group > set "Number"** in the format drop-down menu.</span></span> <span data-ttu-id="e1c59-248">文字列フィールドにテキスト形式が手動で設定されておらず、"00045" のような先行ゼロの文字列値がある場合、Excel は自動的に "45" に変更し、*"PurchaseOrderHeader の PurchaseOrderNumber フィールドの値はキー フィールドであるため変更できません"* というようなエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-248">If the Text format isn't manually set on a string field and there's a string value with leading zeros like "00045", then Excel will automatically change it to "45" and an error will be shown like: *"Unable to change the value of PurchaseOrderHeader's PurchaseOrderNumber field as it is a key field"*.</span></span> <span data-ttu-id="e1c59-249">現在、API を個々のセル (対応するテーブルの列) にテキスト形式を自動的に適用することはできません。</span><span class="sxs-lookup"><span data-stu-id="e1c59-249">Currently, the API doesn't allow for automatically applying the text formatting on individual cells (versus table columns).</span></span>
4. <span data-ttu-id="e1c59-250">デザイナーのヘッダー データ ソースで、2 つのプラス アイコンで表された **関連するテーブルの追加** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1c59-250">In the Designer, on the header data source, click the **Add related table** button represented by a double plus icon.</span></span>
5. <span data-ttu-id="e1c59-251">使用する行フィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-251">Select the line fields that you want to use.</span></span>

<span data-ttu-id="e1c59-252">関連するテーブル データ ソースのヘッダー データ ソースの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-252">Here's an example of a header data source with a related table data source.</span></span>
- <span data-ttu-id="e1c59-253">PurchaseOrderHeader (フィールド)</span><span class="sxs-lookup"><span data-stu-id="e1c59-253">PurchaseOrderHeader (Fields)</span></span>
   - <span data-ttu-id="e1c59-254">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="e1c59-254">dataAreaId</span></span>
   - <span data-ttu-id="e1c59-255">PurchaseOrderNumber</span><span class="sxs-lookup"><span data-stu-id="e1c59-255">PurchaseOrderNumber</span></span>
   - <span data-ttu-id="e1c59-256">PurchaseOrderName</span><span class="sxs-lookup"><span data-stu-id="e1c59-256">PurchaseOrderName</span></span>
   - <span data-ttu-id="e1c59-257">OrderVendorAccountNumber</span><span class="sxs-lookup"><span data-stu-id="e1c59-257">OrderVendorAccountNumber</span></span>
- <span data-ttu-id="e1c59-258">PurchaseOrderLine (テーブル - 関連)</span><span class="sxs-lookup"><span data-stu-id="e1c59-258">PurchaseOrderLine (Table - related)</span></span>
   - <span data-ttu-id="e1c59-259">LineNumber</span><span class="sxs-lookup"><span data-stu-id="e1c59-259">LineNumber</span></span>
   - <span data-ttu-id="e1c59-260">ItemNumber</span><span class="sxs-lookup"><span data-stu-id="e1c59-260">ItemNumber</span></span>
   - <span data-ttu-id="e1c59-261">LineDescription</span><span class="sxs-lookup"><span data-stu-id="e1c59-261">LineDescription</span></span>
   - <span data-ttu-id="e1c59-262">OrderedPurchaseQuantity</span><span class="sxs-lookup"><span data-stu-id="e1c59-262">OrderedPurchaseQuantity</span></span>
   - <span data-ttu-id="e1c59-263">LineAmount</span><span class="sxs-lookup"><span data-stu-id="e1c59-263">LineAmount</span></span>

<span data-ttu-id="e1c59-264">ヘッダーと明細行のブックを使用して、新しいヘッダーと明細行を作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-264">To use a header and lines workbook to create a new header and lines, follow these steps:</span></span>
1. <span data-ttu-id="e1c59-265">ブック内で、ヘッダーの値を持つセルにフォーカスを移動します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-265">In the workbook, move the focus to a cell with a header value.</span></span>
2. <span data-ttu-id="e1c59-266">Excel アドインで **新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1c59-266">In the Excel Add-in, click **New**.</span></span>
3. <span data-ttu-id="e1c59-267">必要に応じて、値のヘッダーと明細行を入力します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-267">Enter header values and lines as needed.</span></span>
4. <span data-ttu-id="e1c59-268">**公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-268">Select **Publish**.</span></span>

## <a name="how-can-fields-be-added-removed-or-moved-within-an-existing-template-workbook"></a><span data-ttu-id="e1c59-269">既存のテンプレート ブック内で、どのようにフィールドを追加、削除、または移動できますか。</span><span class="sxs-lookup"><span data-stu-id="e1c59-269">How can fields be added, removed, or moved within an existing template workbook?</span></span>
<span data-ttu-id="e1c59-270">**ドキュメント テンプレート** で保存されるワークブックを編集することによって、既存のテンプレート ワークブックにフィールドを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-270">Fields can be added into an existing template workbook by editing the workbook stored in **Document Templates**.</span></span>

1. <span data-ttu-id="e1c59-271">元のテンプレート ブックを取得します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-271">Get the original template workbook.</span></span>
   1. <span data-ttu-id="e1c59-272">**ドキュメント テンプレート** フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-272">Open the **Document Templates** form.</span></span>
   2. <span data-ttu-id="e1c59-273">既存のテンプレート ワークブックを検索します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-273">Find the existing template workbook.</span></span>
   3. <span data-ttu-id="e1c59-274">ブックをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="e1c59-274">Download the workbook.</span></span>
   4. <span data-ttu-id="e1c59-275">ブックを開いて、Excel アドインが実行されるように編集を有効にします。</span><span class="sxs-lookup"><span data-stu-id="e1c59-275">Open the workbook and enable editing so that the Excel Add-in runs.</span></span>
2. <span data-ttu-id="e1c59-276">テンプレートに変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-276">Make changes to the template.</span></span> 
   1. <span data-ttu-id="e1c59-277">Excel アドインで **デザイン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-277">In the Excel Add-in, select **Design**.</span></span>
   2. <span data-ttu-id="e1c59-278">フィールドを追加するデータソースの横にある **編集** ボタン (鉛筆アイコン) をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1c59-278">Click the **Edit** button (pencil icon) next to the datasource that you want to add a field into.</span></span>
   3. <span data-ttu-id="e1c59-279">**利用可能なフィールド** リストから **選択されたフィールド** リストに移動して、フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-279">Add fields by moving them from the **Available fields** list into the **Selected fields** list.</span></span> <span data-ttu-id="e1c59-280">フィールドをダブルクリックすると移動します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-280">Double-clicking a field will move it.</span></span> <span data-ttu-id="e1c59-281">**選択したフィールド** ボックスの一覧から **使用可能なフィールド** ボックスの一覧にフィールドを移動して削除します。**上へ** および **下へ** ボタンを使ってフィールドを移動します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-281">Remove fields by moving them from the **Selected fields** list into the **Available fields** list.Move fields using the **Up** and **Down** buttons.</span></span>
   6. <span data-ttu-id="e1c59-282">変更が完了したら、**更新** を選択して、**はい** を選択して確定し、**完了** を選択してデザイナーを終了します (必要に応じて、**更新** を選択して、データが正しく入力されていることを確認します)。</span><span class="sxs-lookup"><span data-stu-id="e1c59-282">After changes are complete, select **Update**, select **Yes** to confirm, and then select **Done** to exit the Designer (if appropriate, select **Refresh** to verify that the data is correctly populated).</span></span>
   7. <span data-ttu-id="e1c59-283">アップロードする前に **オプション** (ギア アイコン) をクリックし、**データ コネクタ** セクションを展開し、**バインディング データのクリア** ボタンをクリックしてテンプレートのデータを消去します</span><span class="sxs-lookup"><span data-stu-id="e1c59-283">Clear the data from the template before upload by clicking **Options** (gear icon), expand the **Data Connector** section, then click the **Clear binding data** button.</span></span>
   8. <span data-ttu-id="e1c59-284">**名前を付けて保存** を使用して、テンプレートを一時的にどこかに保存します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-284">Use **Save As** to store the template somewhere temporarily.</span></span>
3. <span data-ttu-id="e1c59-285">変更したテンプレートをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="e1c59-285">Upload the changed template.</span></span>
   1. <span data-ttu-id="e1c59-286">**ドキュメント テンプレート** フォームに戻り、変更されたテンプレートをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="e1c59-286">Return to the **Document Templates** form and upload the changed template.</span></span>
   2.  <span data-ttu-id="e1c59-287">**新規** をクリックして表示し、変更されたテンプレートを検索します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-287">Click **New** and browse to find the changed template.</span></span>
   3. <span data-ttu-id="e1c59-288">保存されたテンプレート ファイルを選択してから、**開く** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1c59-288">Select the saved template file and click **Open**.</span></span>
   4. <span data-ttu-id="e1c59-289">**テンプレートのアップロード** ダイアログ ボックスで、名前からアンダースコアと末尾のランダムな数字を削除します。たとえば「CustInvoiceJournalTemplate_636564840743000567」は、「CustInvoiceJournalTemplate」になります。</span><span class="sxs-lookup"><span data-stu-id="e1c59-289">In the **Upload template** dialog box, remove the underscore and trailing random number from the name For example, "CustInvoiceJournalTemplate_636564840743000567" becomes "CustInvoiceJournalTemplate".</span></span>
   5. <span data-ttu-id="e1c59-290">確認ダイアログボックスに「この名前のテンプレートが既に存在します ...」と表示されたら、**はい** をクリックして前のテンプレートの置換を確認します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-290">A confirmation dialog box should show that "A template with this name already exists...", click **Yes** to confirm replacement of the previous template.</span></span> <span data-ttu-id="e1c59-291">この確認が表示されない場合、テンプレート名が異なっており、新しいテンプレートとしてアップロードされていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="e1c59-291">Note that if this confirmation is not shown, then the template name is different and it is being uploaded as a new template.</span></span>
4. <span data-ttu-id="e1c59-292">テンプレートが使用されるフォームを開いて、変更されたテンプレートを使用します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-292">Open the form that the template is used on and use the changed template.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="e1c59-293">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="e1c59-293">Troubleshooting</span></span>

<span data-ttu-id="e1c59-294">予想されるルックアップを参照しない場合は、\[YourSiteURL\]/data/$metadata で利用できるメタデータ フィードを確認して、リレーションシップ メタデータを検証します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-294">If you are not seeing an expected lookup, validate relationship metadata by checking the metadata feed available at \[YourSiteURL\]/data/$metadata.</span></span> <span data-ttu-id="e1c59-295">エンティティのパブリック名の $metadat フィードを検索してその EntityType 要素を検索し、関係のロールの値と同じ名前を持つ子 NavigationProperty 要素があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-295">Search the $metadat feed for the public name of your entity to find its EntityType element, then make sure there is a child NavigationProperty element with a name equal to the Role value of the relationship.</span></span> <span data-ttu-id="e1c59-296">ナビゲーション プロパティが存在する場合、Excel データ コネクターが使用され、関係の参照を表示します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-296">If the navigation property exists, it will be used by the Excel Data Connector to show a relationship lookup.</span></span> <span data-ttu-id="e1c59-297">ルックアップは、次の条件下では表示されません。</span><span class="sxs-lookup"><span data-stu-id="e1c59-297">Lookups are not shown under the following conditions:</span></span>

  - <span data-ttu-id="e1c59-298">エンティティのすべてのキー フィールドは関係の中に制約として含まれています。</span><span class="sxs-lookup"><span data-stu-id="e1c59-298">All of the entity's key fields are included as constraints in the relationship.</span></span>
  - <span data-ttu-id="e1c59-299">選択されたフィールドはキーであり、選択されたレコードは新規ではありません。</span><span class="sxs-lookup"><span data-stu-id="e1c59-299">The selected field is a key and the selected record is not new.</span></span>
  - <span data-ttu-id="e1c59-300">認証されたユーザーには、ルックアップの対象となるエンティティにアクセスするためのアクセス許可がありません。</span><span class="sxs-lookup"><span data-stu-id="e1c59-300">The authenticated user does not have permission to access the entity targeted by the lookup.</span></span>

## <a name="how-do-dimensions-work"></a><span data-ttu-id="e1c59-301">分析コードはどのように機能しますか。</span><span class="sxs-lookup"><span data-stu-id="e1c59-301">How do dimensions work?</span></span>
<span data-ttu-id="e1c59-302">データ エンティティに分析コード メタデータを設定する最も簡単な方法は、データ エンティティ作成ウィザードを使用することで、これにより、分析コード フレームワークが必要とするものとまったく同じプライベート リレーションシップおよび公開表示値フィールドが自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-302">The easiest way to set up dimension metadata on data entities is to use the data entity creation wizard, which will automatically create the private relationships and public display value fields exactly as the dimensions framework needs them.</span></span> <span data-ttu-id="e1c59-303">分析コードの設定をカスタマイズする場合は、 [Excel テンプレートへの分析コードの追加](../financial/dimensions-overview.md) を参照します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-303">If you want to customize your dimensions setup, see [Add dimensions to Excel templates](../financial/dimensions-overview.md).</span></span> <span data-ttu-id="e1c59-304">ルックアップは非元帳分析コードに対してのみ自動的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-304">Lookups, are only generated automatically for non-ledger dimensions.</span></span> <span data-ttu-id="e1c59-305">カスタム分析コードは現在サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="e1c59-305">Custom dimensions are not supported currently.</span></span> <span data-ttu-id="e1c59-306">勘定分析コード (MainAccount、Department、CostCenter など) のルックアップを有効にする場合は、DimensionCombationEntity および DimensionSetEntity フィールドのリレーションシップの作成に関するガイダンスについては、 [Excel テンプレートへの分析コードの追加](../financial/dimensions-overview.md) を参照します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-306">If you want to enable lookups for ledger dimensions (MainAccount, Department, CostCenter, etc.), see [Add dimensions to Excel templates](../financial/dimensions-overview.md) for guidance on creating relationships on DimensionCombationEntity and DimensionSetEntity fields.</span></span> <span data-ttu-id="e1c59-307">これらのリレーションシップが存在するときは、Excel データ コネクタに、リレーションシップ ルックアップが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-307">When those relationships are present, relationship lookups will be displayed in the Excel Data Connector.</span></span> <span data-ttu-id="e1c59-308">Excel Data Connector は、表示値を直接編集したり、別の列にある表示値の各属性を編集したりという、2 つのタイプの分析コード データ入力をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="e1c59-308">The Excel Data Connector supports two types of dimension data entry: editing the display value directly or editing each attribute of the display value in a separate column.</span></span> <span data-ttu-id="e1c59-309">表示値の列と個々の属性の列の両方を連結した場合、両方を編集して、個別に公開できます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-309">If both the display value column and the individual attribute columns are bound, they can both be edited and published separately.</span></span> <span data-ttu-id="e1c59-310">表示値と個々の属性の両方を同じ行で編集した場合、個々の属性の変更は表示値の変更を上書きします。</span><span class="sxs-lookup"><span data-stu-id="e1c59-310">If both the display value and an individual attribute are edited in the same row, the individual attribute change overrides the display value change.</span></span>

## <a name="how-do-i-create-formula-table-columns"></a><span data-ttu-id="e1c59-311">フォーミュラ テーブル列をどのように作成しますか。</span><span class="sxs-lookup"><span data-stu-id="e1c59-311">How do I create formula table columns?</span></span>
<span data-ttu-id="e1c59-312">テーブルに式が必要な場合は、式の列を追加します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-312">If a formula is needed in a table, then add a formula column.</span></span> <span data-ttu-id="e1c59-313">テーブル バインドのフィールド選択ページで、[選択済のフィールド] リストの上にある **式** ボタンをクリックして、新しい式列を追加します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-313">When in the field selection page for a table binding, click the **Formula** button above the Selected fields list to add a new formula column.</span></span> <span data-ttu-id="e1c59-314">式のラベルと値は、選択したフィールド リストのすぐ下のフィールドに入力されます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-314">The label and value for the formula are entered in the fields immediately below the Selected fields list.</span></span> <span data-ttu-id="e1c59-315">新しい式の列を追加すると、値を空白のままにして、**更新** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e1c59-315">After adding a new formula column, leave the value empty and click **Update**.</span></span> <span data-ttu-id="e1c59-316">フィールドがテーブルに追加されると、Excel の標準機能を使用して数式を作成し、数式をコピーして数式列の値フィールドに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-316">After the field has been added to the table, use standard Excel capabilities to create a formula, then copy the formula and paste it into the formula column value field.</span></span> <span data-ttu-id="e1c59-317">式を定義するときは、テーブルに複数の行が存在することを確認してください。そうでない場合、Excel が提供する式は、該当する行ではなく、すべての行を対象としている場合があります。</span><span class="sxs-lookup"><span data-stu-id="e1c59-317">When defining a formula, make sure there is more than one row in the table, otherwise the formula that Excel provides may be for ALL rows instead of THAT row.</span></span> <span data-ttu-id="e1c59-318">現在の行だけを指定するには、アット マーク (@) が必要です。</span><span class="sxs-lookup"><span data-stu-id="e1c59-318">To specify just the current row, the at sign (@) is needed.</span></span> <span data-ttu-id="e1c59-319">たとえば、すべての行に対する 4 つの列の合計「=SUM(Table1\[\[ColumnA\]:\[ColumnD\]\])」と現在の行の 4 つの列の合計「=SUM (Table1\[@\[ColumnA\]:\[ColumnD\]\])」。</span><span class="sxs-lookup"><span data-stu-id="e1c59-319">For example, sum of four columns for all rows "=SUM(Table1\[\[ColumnA\]:\[ColumnD\]\])" versus sum of four columns for the current row "=SUM(Table1\[@\[ColumnA\]:\[ColumnD\]\])".</span></span>

## <a name="known-issues"></a><span data-ttu-id="e1c59-320">既知の問題</span><span class="sxs-lookup"><span data-stu-id="e1c59-320">Known issues</span></span>
### <a name="refresh-doesnt-automatically-occur-in-old-templates"></a><span data-ttu-id="e1c59-321">更新は、以前のテンプレートでは自動的に行われません</span><span class="sxs-lookup"><span data-stu-id="e1c59-321">Refresh doesn’t automatically occur in old templates</span></span>

<span data-ttu-id="e1c59-322">「開くときの更新」を制御する機能が設定として追加されました。</span><span class="sxs-lookup"><span data-stu-id="e1c59-322">The ability to control “refresh on open” was added as a setting.</span></span> <span data-ttu-id="e1c59-323">これをデフォルトの動作に追加するには、既存のテンプレートとブックで、**Options** &gt; **Data Connector** &gt; **Refresh Options** にある **Refresh on open** チェック ボックスをオンにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e1c59-323">To add this to the default behavior, existing templates and workbooks need to have the **Refresh on open** check box selected in **Options** &gt; **Data Connector** &gt; **Refresh Options**.</span></span>

### <a name="error-finding-entity"></a><span data-ttu-id="e1c59-324">エンティティ検索中のエラー</span><span class="sxs-lookup"><span data-stu-id="e1c59-324">Error finding entity</span></span>

<span data-ttu-id="e1c59-325">エンティティへの参照が、プライベート エンティティ名 (DataEntity.Name) からパブリック エンティティ名 (DataEntity.PublicEntityName) に変更されました。</span><span class="sxs-lookup"><span data-stu-id="e1c59-325">The reference to entities changed from using the Private Entity Name (DataEntity.Name) to Public Entity Name (DataEntity.PublicEntityName).</span></span> <span data-ttu-id="e1c59-326">エンティティのパブリックおよびプライベート名が異なっており、Excel テンプレートまたはブックで使用されている場合、「エラー検索エンティティ」というメッセージが Excel アプリに表示されます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-326">If the public and private names for an entity were different and that entity was used in an Excel template or workbook, then this will cause the following error to be displayed in the Excel App: “Error Finding Entity.</span></span> <span data-ttu-id="e1c59-327">詳細: エンティティ "&lt;DataEntity.Name&gt;" は見つかりません"。</span><span class="sxs-lookup"><span data-stu-id="e1c59-327">Details: Entity "&lt;DataEntity.Name&gt;" not found”.</span></span>

<span data-ttu-id="e1c59-328">これを解決するには、影響を受けるテンプレートのバインド情報を変更して、DataEntity.Name の代わりに DataEntity.PublicEntityName を指すようにします。</span><span class="sxs-lookup"><span data-stu-id="e1c59-328">To resolve this, change the binding information in the affected template so that it points to DataEntity.PublicEntityName instead of DataEntity.Name.</span></span>

1.  <span data-ttu-id="e1c59-329">置き換える必要のある DataEntity.Name については、DataEntity.PublicEntityName を決定し、たとえば FMCustomerEntity を FleetCustomer に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-329">For the DataEntity.Name that needs to be replaced, determine the DataEntity.PublicEntityName, for example replace FMCustomerEntity with FleetCustomer.</span></span>
2.  <span data-ttu-id="e1c59-330">影響を受けるテンプレートを検索します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-330">Find the affected template.</span></span>
3.  <span data-ttu-id="e1c59-331">テンプレートのファイル拡張子を .xlsx から .zip に変更します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-331">Change the file extension on the template from .xlsx to .zip.</span></span>

    <span data-ttu-id="e1c59-332">[![ダイアログ ボックス名を変更](./media/off101m.png)](./media/off101m.png)</span><span class="sxs-lookup"><span data-stu-id="e1c59-332">[![Rename dialog box](./media/off101m.png)](./media/off101m.png)</span></span>
    
4.  <span data-ttu-id="e1c59-333">変更するファイルは、2015-05-25-FleetCustomersWithLocations.zipxlwebextensionswebextension2.xml など、xlwebextensions ディレクトリ内の webextension\*.xml ファイルのいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="e1c59-333">The file to be changed will be one of the webextension\*.xml files in the xlwebextensions directory, such as 2015-05-25-FleetCustomersWithLocations.zipxlwebextensionswebextension2.xml.</span></span>
5.  <span data-ttu-id="e1c59-334">ファイルを開き、適切な場所であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-334">Open the file to ensure that you have the correct location.</span></span>
6.  <span data-ttu-id="e1c59-335">FMCustomerEntity などの、DataEntity.Name を検索します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-335">Find the DataEntity.Name,  such as FMCustomerEntity.</span></span>

    <span data-ttu-id="e1c59-336">[![DataEntity.Name を検索](./media/off101n.png)](./media/off101n.png)</span><span class="sxs-lookup"><span data-stu-id="e1c59-336">[![Find DataEntity.Name](./media/off101n.png)](./media/off101n.png)</span></span>
    
7.  <span data-ttu-id="e1c59-337">ZIP ファイルを抽出します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-337">Extract the zip file.</span></span>
8.  <span data-ttu-id="e1c59-338">webextension xml ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-338">Open the webextension xml file.</span></span>
9.  <span data-ttu-id="e1c59-339">DataEntity.Name を対応する DataEntity.PublicEntityName に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="e1c59-339">Replace the DataEntity.Name with the corresponding DataEntity.PublicEntityName.</span></span>
10. <span data-ttu-id="e1c59-340">webextension .xml ファイルの変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-340">Save the webextension .xml file changes.</span></span>
11. <span data-ttu-id="e1c59-341">たとえば、古い zip ファイルの名前を変更し、名前に ".old" を追加します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-341">Rename the old zip file, for example, add “.old” to the name.</span></span>
12. <span data-ttu-id="e1c59-342">以前に抽出したすべてのコンテンツの新しい ZIP ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-342">Create a new zip file of all the previously extracted content.</span></span> <span data-ttu-id="e1c59-343">これは通常、アーカイブ/zip フォルダ内のコンテンツを強調表示し、そのコンテンツを使用して zip フォルダを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e1c59-343">This usually involves highlighting the content inside the archive/zip folder and creating a zipped folder using that content.</span></span>
13. <span data-ttu-id="e1c59-344">ZIP ファイルには ZIP ファイルのルートに \_rels"、"docProps"、および "xl" の各フォルダがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-344">Verify that the zip file has the “\_rels”, “docProps”, and “xl” folders in the root of the zip file.</span></span>
14. <span data-ttu-id="e1c59-345">必要に応じて zip ファイルの名前を変更します。たとえば、ファイル 2015-05-25-FleetCustomersWithLocations.zip の名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-345">Rename the zip file as needed, for example rename the file 2015-05-25-FleetCustomersWithLocations.zip.</span></span>
15. <span data-ttu-id="e1c59-346">zip ファイル拡張子を .xlsx に変更します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-346">Change the zip file extension to .xlsx.</span></span>
16. <span data-ttu-id="e1c59-347">必要な場合は、ブック .xlsx ファイルを再発行します。</span><span class="sxs-lookup"><span data-stu-id="e1c59-347">Re-publish the workbook .xlsx file, if needed.</span></span>
