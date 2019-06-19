---
title: 既定の財務分析コード
description: このトピックでは、既定の財務分析コードについて説明します。 ここでは、分析コードのがどのように生成されるか、その分析に使用されるAPI、および元帳分析コードの作成に使用する方法について説明します。
author: jasonsto
manager: annbe
ms.date: 04/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: ''
ms.search.scope: Operations
ms.search.region: Global
ms.author: rbrow
ms.search.validFrom: 2019-01-16
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3806c9f3d3a950490bfc528349467677d1914723
ms.sourcegitcommit: 574d4dda83dcab94728a3d35fc53ee7e2b90feb0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/22/2019
ms.locfileid: "1595415"
---
# <a name="default-financial-dimensions"></a><span data-ttu-id="8da1c-104">既定の財務分析コード</span><span class="sxs-lookup"><span data-stu-id="8da1c-104">Default financial dimensions</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="8da1c-105">このトピックでは、既定の財務分析コードについて開発者向けの説明を記載します。</span><span class="sxs-lookup"><span data-stu-id="8da1c-105">This topic explains default financial dimensions for developers.</span></span> <span data-ttu-id="8da1c-106">ここでは、分析コードのがどのように生成されるか、その分析に使用される application programming interfaces (API)、および元帳分析コードの作成に使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8da1c-106">It explains where the dimensions originate, the application programming interfaces (APIs) that are used to merge them, and how they are used to create ledger dimensions.</span></span> <span data-ttu-id="8da1c-107">このトピックには、ユーザーインターフェイス (UI)、SQLテーブルクエリ、およびそれらのクエリの出力例が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-107">The topic includes examples that show the user interface (UI), SQL table queries, and the output of those queries.</span></span> <span data-ttu-id="8da1c-108">また、API とその使用例についても説明します。</span><span class="sxs-lookup"><span data-stu-id="8da1c-108">It also includes some explanation of APIs and examples of how they are used.</span></span>

<span data-ttu-id="8da1c-109">このトピックでは、デモ データの会社として **USMF** を使用します。</span><span class="sxs-lookup"><span data-stu-id="8da1c-109">This topic uses examples from the **USMF** demo data company.</span></span>

<span data-ttu-id="8da1c-110">財務分析コードのコンセプトおよび業務プロセスに対する影響について詳細は [財務分析コード](../../financials/general-ledger/financial-dimensions.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8da1c-110">For conceptual information about financial dimensions and how they affect business processes, see [Financial dimensions](../../financials/general-ledger/financial-dimensions.md).</span></span>

### <a name="entering-default-dimensions"></a><span data-ttu-id="8da1c-111">既定の分析コードを入力する</span><span class="sxs-lookup"><span data-stu-id="8da1c-111">Entering default dimensions</span></span>

<span data-ttu-id="8da1c-112">既定の財務分析コードを入力するには Microsoft Dynamics 365 for Finance and Operations を参照すると 250ページ以上に渡って記載がされています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-112">More than 250 pages in Microsoft Dynamics 365 for Finance and Operations let you enter default financial dimensions.</span></span> <span data-ttu-id="8da1c-113">分析コードは、ファストタブに値および説明と共に一覧表示されています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-113">The dimensions are shown on a FastTab that lists them together with values and descriptions.</span></span> <span data-ttu-id="8da1c-114">標準デモデータでは、30以上の分析コードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-114">In standard demo data, more than 30 dimensions are available.</span></span> <span data-ttu-id="8da1c-115">ただし、次の **財務分析コード** ファストタブには、次の5つの分析コード、BusinessUnit、課、部門、ItemGroup、プロジェクト のみを表示しています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-115">However, the following example of a **Financial dimensions** FastTab shows just five dimensions: BusinessUnit, CostCenter, Department, ItemGroup, and Project.</span></span> 

<span data-ttu-id="8da1c-116">![財務分析コード ファストタブ](./media/DefaultDimensionEntry.png "財務分析コード ファストタブ")</span><span class="sxs-lookup"><span data-stu-id="8da1c-116">![Financial dimensions FastTab](./media/DefaultDimensionEntry.png "Financial dimensions FastTab")</span></span>

### <a name="dimensions-list"></a><span data-ttu-id="8da1c-117">分析コード リスト</span><span class="sxs-lookup"><span data-stu-id="8da1c-117">Dimensions list</span></span>

<span data-ttu-id="8da1c-118">分析コードは、最初に勘定構造の一覧に基づいてフィルター処理されており、これらは現在の会社またはページで指定されている会社の元帳に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-118">The dimensions are first filtered based on the list of all active account structures that are associated with the ledger of the current company or the company that is specified on the page.</span></span> <span data-ttu-id="8da1c-119">次に、それらの構造に関連付けられている分析コードの一覧と、それらの構造に関連付けられている有効となっている高度なルールの一覧が結合されたリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-119">Next, a union of all the dimensions in those account structures, plus all active advanced rules that are associated with those structures, is obtained.</span></span> 

<span data-ttu-id="8da1c-120">![財務分析コード リスト](./media/FinancialDimensionList.png "財務分析コード リスト")</span><span class="sxs-lookup"><span data-stu-id="8da1c-120">![Financial dimensions list](./media/FinancialDimensionList.png "Financial dimensions list")</span></span>

### <a name="ledger-page"></a><span data-ttu-id="8da1c-121">元帳 ページ</span><span class="sxs-lookup"><span data-stu-id="8da1c-121">Ledger page</span></span>

<span data-ttu-id="8da1c-122">**元帳** ページ (**一般会計 \> 設定 \> 元帳**) にて、会社の勘定構造を管理できます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-122">On the **Ledger** page (**General Ledger \> Setup \> Ledger**), you can maintain the account structures for a company.</span></span> 

<span data-ttu-id="8da1c-123">![USMF会社の元帳ページ](./media/LedgerStructureConfiguration.png "USMF会社の元帳ページ")</span><span class="sxs-lookup"><span data-stu-id="8da1c-123">![Ledger page for the USMF company](./media/LedgerStructureConfiguration.png "Ledger page for the USMF company")</span></span>

### <a name="account-structures-where-the-number-of-dimensions-varies"></a><span data-ttu-id="8da1c-124">分析コードの数が変動する勘定構造</span><span class="sxs-lookup"><span data-stu-id="8da1c-124">Account structures where the number of dimensions varies</span></span>

<span data-ttu-id="8da1c-125">勘定構造で使用する分析コードの数を決定するには **元帳** ページで グリッド上の **勘定構造の設定** を選択し、列の数を数えます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-125">To determine how many dimensions an account structure uses, select it on the **Ledger** page, select **Configure account structure** above the grid, and then count the columns.</span></span> <span data-ttu-id="8da1c-126">以下の図は、3つの分析コードを使用しているの勘定構造と、5つの分析コードを使用する勘定構造を示しています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-126">The following illustrations show one account structure that uses three dimensions and another account structure that uses five dimensions.</span></span>

<span data-ttu-id="8da1c-127">**3つの分析コードを使っている勘定構造**</span><span class="sxs-lookup"><span data-stu-id="8da1c-127">**Account structure that uses three dimensions**</span></span>

<span data-ttu-id="8da1c-128">![USMF社の貸借対照表勘定構造](./media/BalanceSheetAccountStructureSetup.png "USMF社の貸借対照表勘定構造")</span><span class="sxs-lookup"><span data-stu-id="8da1c-128">![Setup of the Balance sheet account structure for the USMF company](./media/BalanceSheetAccountStructureSetup.png "Setup of the Balance sheet account structure for the USMF company")</span></span>

<span data-ttu-id="8da1c-129">**5つの分析コードを使っている勘定構造**</span><span class="sxs-lookup"><span data-stu-id="8da1c-129">**Account structure that uses five dimensions**</span></span>

<span data-ttu-id="8da1c-130">![USMF社の損益勘定構造設定](./media/PandLAccountStructureSetup.png "USMF社の損益勘定構造設定")</span><span class="sxs-lookup"><span data-stu-id="8da1c-130">![Setup of the Profit and loss account structure for the USMF company](./media/PandLAccountStructureSetup.png "Setup of the Profit and loss account structure for the USMF company")</span></span>

<span data-ttu-id="8da1c-131">上記の図に示した2つの勘定構造の間には、BusinessUnit、Department、CostCenter, ItemGroup、の4つの固有の分析コードがあります。</span><span class="sxs-lookup"><span data-stu-id="8da1c-131">Between the two account structures that are shown in the preceding illustrations, there are four unique dimensions: BusinessUnit, Department, CostCenter, and ItemGroup.</span></span> <span data-ttu-id="8da1c-132">これら4つの分析コードは、既定の分析コードの一覧に表示されます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-132">These four dimensions will appear in the list of default dimensions.</span></span> <span data-ttu-id="8da1c-133">さらに、高度なルールを介してアカウント構造に連係されている高度なルール構造からの分析コードが検証されます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-133">In addition, dimensions from advanced rule structures that are linked to the account structures through advanced rules are examined.</span></span> <span data-ttu-id="8da1c-134">この例では、高度なルール構造から分析コードを検証した結果、5番目の分析コードがデフォルトの分析コードのリストに追加されています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-134">In this example, the examination of dimensions from advanced rule structures causes a fifth dimension, Project, to be added to the list of default dimensions.</span></span>

<span data-ttu-id="8da1c-135">以下の図は、プロジェクト分析コードがデフォルト分析コードのリストに組み込むための高度なルールを示しています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-135">The following illustration shows the advanced rule that causes the Project dimension to be included in the list of default dimensions.</span></span>

<span data-ttu-id="8da1c-136">![損益勘定構造にリンクされている損益勘定構造](./media/AdvancedRuleLinked.png "損益勘定構造にリンクされている損益勘定構造")</span><span class="sxs-lookup"><span data-stu-id="8da1c-136">![Advanced rule that is linked to the Profit and loss account structure](./media/AdvancedRuleLinked.png "Advanced rule that is linked to the Profit and loss account structure")</span></span>

<span data-ttu-id="8da1c-137">以下の図は、ルール構造を示しています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-137">The following illustration shows the rule structure.</span></span>

<span data-ttu-id="8da1c-138">![プロジェクトのルール構造](./media/RuleStructure.png "プロジェクトのルール構造")</span><span class="sxs-lookup"><span data-stu-id="8da1c-138">![Rule structure for Project](./media/RuleStructure.png "Rule structure for Project")</span></span>

<span data-ttu-id="8da1c-139">この MainAccount 分析コードは、多くの場合は既定の分析コードの一覧には表示されないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="8da1c-139">Note that the MainAccount dimension isn't shown in most lists of default dimensions.</span></span> <span data-ttu-id="8da1c-140">ただし、予算作成は例外となります。</span><span class="sxs-lookup"><span data-stu-id="8da1c-140">However, Budgeting is the exception.</span></span> <span data-ttu-id="8da1c-141">この場合、既定の分析コードの一覧にはMainAccount分析コードが明示的に含まれています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-141">It does explicitly include the MainAccount dimension in the list of default dimensions.</span></span>

### <a name="api-for-the-list-of-default-dimensions"></a><span data-ttu-id="8da1c-142">既定の分析コード一覧用API</span><span class="sxs-lookup"><span data-stu-id="8da1c-142">API for the list of default dimensions</span></span>

<span data-ttu-id="8da1c-143">既定のdimensionコントローラである **DimensionDefaultingController** は、会社に適切な分析コードを判断するために **DimensionCache::getDimensionAttributeSetForLedger()** APIを使用します。</span><span class="sxs-lookup"><span data-stu-id="8da1c-143">The default dimension controller, **DimensionDefaultingController**, uses the **DimensionCache::getDimensionAttributeSetForLedger()** API to determine which dimensions are applicable to a company.</span></span>

## <a name="control-uptake-and-storage"></a><span data-ttu-id="8da1c-144">取込と保存の管理</span><span class="sxs-lookup"><span data-stu-id="8da1c-144">Control uptake and storage</span></span>

### <a name="form-uptake-and-the-dimensions-data-model"></a><span data-ttu-id="8da1c-145">取込みフォームと分析コードデータのモデル</span><span class="sxs-lookup"><span data-stu-id="8da1c-145">Form uptake and the dimensions data model</span></span>

<span data-ttu-id="8da1c-146">既定の分析コードを表示するすべてのページでは **DimensionDefaultingController** コントローラが使用されています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-146">All pages that show default dimensions use the **DimensionDefaultingController** controller.</span></span> <span data-ttu-id="8da1c-147">このコントローラでは、分析コードが自動的に表示され、値を読み込んで保存するので、対話的な操作を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-147">This controller automatically shows dimensions, and loads and saves values and user interactions.</span></span> <span data-ttu-id="8da1c-148">取込みパターンの詳細については、ホワイト ペーパー [Implementing the Account and Financial Dimensions Framework for Microsoft Dynamics AX 2012 Applications](https://go.microsoft.com/fwlink/?linkid=213133) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8da1c-148">For information about these uptake patterns, see the [Implementing the Account and Financial Dimensions Framework for Microsoft Dynamics AX 2012 Applications](https://go.microsoft.com/fwlink/?linkid=213133) white paper.</span></span>

### <a name="storage-of-default-dimension-values"></a><span data-ttu-id="8da1c-149">既定の分析コード値の保存</span><span class="sxs-lookup"><span data-stu-id="8da1c-149">Storage of default dimension values</span></span>

<span data-ttu-id="8da1c-150">分析コードに関連付けられている値は、これらの分析コード値を参照する主テーブルとは別のテーブルに格納されます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-150">The values that are associated with the dimensions are stored in a table that is separate from the primary table that references those dimension values.</span></span> <span data-ttu-id="8da1c-151">たとえば、LedgerJournalTableテーブルには、DimensionAttributeValueSetテーブル内のレコードへの外部キー参照を保持する **dimensiondefault** 列があります。</span><span class="sxs-lookup"><span data-stu-id="8da1c-151">For example, the LedgerJournalTable table has a **DimensionDefault** column that holds a foreign key reference to a record in the DimensionAttributeValueSet table.</span></span> <span data-ttu-id="8da1c-152">このレコードは、表示される一連の値を意味する親レコードです。</span><span class="sxs-lookup"><span data-stu-id="8da1c-152">This record is the parent record that represents the set of values that is shown.</span></span>

<span data-ttu-id="8da1c-153">![既定の分析コード値](./media/Part2DefaultDimensionEntry.png "既定の分析コード値")</span><span class="sxs-lookup"><span data-stu-id="8da1c-153">![Default dimension values](./media/Part2DefaultDimensionEntry.png "Default dimension values")</span></span>

<span data-ttu-id="8da1c-154">それぞれの値は、DimensionAttributeValueSetItem テーブルに独立した行として保存されますが、親レコードの外部キーは同じものとなります。</span><span class="sxs-lookup"><span data-stu-id="8da1c-154">Each value is stored as a separate row in the DimensionAttributeValueSetItem table and has the same parent record foreign key.</span></span>

<span data-ttu-id="8da1c-155">![すべての既定の分析コード値のSQL結果](./media/SQLResultofAllDefaultDimensionValues.png "すべての既定の分析コード値のSQL結果")</span><span class="sxs-lookup"><span data-stu-id="8da1c-155">![SQL results of all default dimension values](./media/SQLResultofAllDefaultDimensionValues.png "SQL results of all default dimension values")</span></span>

<span data-ttu-id="8da1c-156">データは、これらのテーブルを介して直接照会できます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-156">The data can be queried directly through these tables.</span></span> <span data-ttu-id="8da1c-157">また、以下の図に示すように **DimensionAttributeValueSetItemView** を使用してクエリを実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-157">Alternatively, it can be queried by using **DimensionAttributeValueSetItemView**, as shown in the following illustration.</span></span>

<span data-ttu-id="8da1c-158">![DimensionAttributeValueSetItemViewを使用してデータを照会](./media/SQLofAllDefaultDimensionValues.png "DimensionAttributeValueSetItemViewを使用してデータを照会")</span><span class="sxs-lookup"><span data-stu-id="8da1c-158">![Querying data by using DimensionAttributeValueSetItemView](./media/SQLofAllDefaultDimensionValues.png "Querying data by using DimensionAttributeValueSetItemView")</span></span>

### <a name="empty-values"></a><span data-ttu-id="8da1c-159">空の値</span><span class="sxs-lookup"><span data-stu-id="8da1c-159">Empty values</span></span>

<span data-ttu-id="8da1c-160">分析コードのフレームワークは、値が入力された分析コードについてのみ行を保存します。</span><span class="sxs-lookup"><span data-stu-id="8da1c-160">The dimension framework stores rows only for dimensions that a value has been entered for.</span></span> <span data-ttu-id="8da1c-161">空の行に対してはデータが保存されません。</span><span class="sxs-lookup"><span data-stu-id="8da1c-161">No data is stored for empty rows.</span></span> <span data-ttu-id="8da1c-162">したがって、データが保存された後、フレームワークは値を持たない分析コードについて、それがユーザーが削除したものなのか、そもそも値が入っていないものなのかを区別することができません。</span><span class="sxs-lookup"><span data-stu-id="8da1c-162">Therefore, after data is persisted, the framework can't distinguish a dimension that didn't have a value from a dimension that did have a value, but it was cleared by a user.</span></span> <span data-ttu-id="8da1c-163">空の値を保存するには、空白であることを意味する値を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8da1c-163">To save an empty value, you must create a real value and give it a name that indicates that it's empty.</span></span> <span data-ttu-id="8da1c-164">命名の例としては **empty** , **n/a** , **\<cleared\>**, **\*blank\*** などです。</span><span class="sxs-lookup"><span data-stu-id="8da1c-164">For example, name it **empty**, **n/a**, **\<cleared\>**, or **\*blank\***.</span></span> <span data-ttu-id="8da1c-165">ユーザーは、空白の値に対しては入力時にこの値を選択して、これは空白値入力の既定の動作とすることができます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-165">Users can then select this value at entry time to affect the defaulting behavior as they desire.</span></span>

### <a name="immutable-data"></a><span data-ttu-id="8da1c-166">不変データ</span><span class="sxs-lookup"><span data-stu-id="8da1c-166">Immutable data</span></span>

<span data-ttu-id="8da1c-167">ほとんどの分析コードと同様に、テーブルに挿入されたレコードは変更できません。</span><span class="sxs-lookup"><span data-stu-id="8da1c-167">Like most dimension data, the records that are inserted into the tables that were mentioned earlier are immutable.</span></span> <span data-ttu-id="8da1c-168">これらは最初に作成されますが、その後更新または削除されることがありません。</span><span class="sxs-lookup"><span data-stu-id="8da1c-168">They are initially written, but then never subsequently updated or deleted.</span></span> <span data-ttu-id="8da1c-169">たとえば、ユーザーがプロジェクトIDを分析コードとして追加し、変更を保存したとします。</span><span class="sxs-lookup"><span data-stu-id="8da1c-169">For example, a user adds a project ID as a dimension and then saves the change.</span></span>

<span data-ttu-id="8da1c-170">![既定の分析コードエントリと追加された値](./media/Part2-1DefaultDimensionEntry.png "既定の分析コードエントリと追加された値")</span><span class="sxs-lookup"><span data-stu-id="8da1c-170">![Default dimension entry and one added value](./media/Part2-1DefaultDimensionEntry.png "Default dimension entry and one added value")</span></span>

<span data-ttu-id="8da1c-171">この場合でも、新しい行が追加された場合でも、SQLクエリは以前と同様の3つの行を返します。</span><span class="sxs-lookup"><span data-stu-id="8da1c-171">In this case, the SQL query will still return the same three rows as shown previously even though a new row was added.</span></span> <span data-ttu-id="8da1c-172">新しい値が追加されると、分析コードフレームワークは新しい値セットレコードと、前の分析コードセットを変更するのではなく、新しい値セットにリンクされている4つの追加の値セットアイテムレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="8da1c-172">When a new value was added the dimension framework created a new value set record and four additional value set item records that are linked to the new value set rather than change the previous dimension set.</span></span>

<span data-ttu-id="8da1c-173">![sqlクエリのすべての既定の分析コード値に対するSQLクエリと出力 (列追加)](./media/Part2SQLResultsValueSet.png "sqlクエリのすべての既定の分析コード値に対するSQLクエリと出力 (列追加)")</span><span class="sxs-lookup"><span data-stu-id="8da1c-173">![SQL query and output (column-trimmed) for all default dimension values in the new set](./media/Part2SQLResultsValueSet.png "SQL query and (column trimmed) output for all default dimension values in the new set")</span></span>

## <a name="copy-patterns"></a><span data-ttu-id="8da1c-174">パターンのコピー</span><span class="sxs-lookup"><span data-stu-id="8da1c-174">Copy patterns</span></span>

<span data-ttu-id="8da1c-175">このセクションでは、エンティティ間で既定の分析コードがどのようにコピーされるかについて説明します。</span><span class="sxs-lookup"><span data-stu-id="8da1c-175">This section explains how default dimensions are copied between entities.</span></span>

### <a name="copy-vs-merge"></a><span data-ttu-id="8da1c-176">コピーとマージ</span><span class="sxs-lookup"><span data-stu-id="8da1c-176">Copy vs. merge</span></span>

<span data-ttu-id="8da1c-177">通常、既定の分析コードは、勘定科目分析コードを作成するために他の分析コードの組み合わせとコピーまたはマージされます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-177">Default dimensions are typically copied or merged with other dimension combinations to create ledger account dimensions.</span></span> <span data-ttu-id="8da1c-178">分析コードフレームワークは、既定の動作の優先順位を設定しません。</span><span class="sxs-lookup"><span data-stu-id="8da1c-178">The dimension framework doesn't set the precedence for defaulting behavior.</span></span> <span data-ttu-id="8da1c-179">各ページまたはプロセスは、ビジネスロジックの要件に基づいて、優先順位を決定します。</span><span class="sxs-lookup"><span data-stu-id="8da1c-179">Each page or process determines the precedence, based on the requirements of its business logic.</span></span>

<span data-ttu-id="8da1c-180">以下の例を、"仮想注文" ドキュメントに基づいて進めていきます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-180">A hypothetical order document will serve as the basis for the examples that follow.</span></span> <span data-ttu-id="8da1c-181">このドキュメントは、品目としてのサービスを含む顧客販売注文であると考えることができます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-181">This document might be a customer sales order that contains services as line items.</span></span> <span data-ttu-id="8da1c-182">または、在庫品目を品目として含む仕入先の発注書であると考えることもできます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-182">Alternatively, it might be a vendor purchase order that contains inventory items as line items.</span></span> <span data-ttu-id="8da1c-183">以下の図に示すように、処理内のさまざまな時点で既定の分析コードを入力または上書きすることができます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-183">Default dimensions can be entered or overridden at various points in the processing, as the following illustration shows.</span></span>

<span data-ttu-id="8da1c-184">![標準ドキュメントの既定の分析コードソース](./media/DefaultDimensionSourcesGraph.png "標準ドキュメントの既定の分析コードソース")</span><span class="sxs-lookup"><span data-stu-id="8da1c-184">![Default dimension sources on a typical document](./media/DefaultDimensionSourcesGraph.png "Default dimension sources on a typical document")</span></span>

<span data-ttu-id="8da1c-185">注文ドキュメントの場合は、ビジネスロジックに相当する既定の分析コードが複数用意されています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-185">For an order document, multiple default dimensions are available for the business logic to consider.</span></span> <span data-ttu-id="8da1c-186">この例で使用される発注書のように、ドキュメントヘッダーには既定の分析コードのセットが含まれている場合があります。</span><span class="sxs-lookup"><span data-stu-id="8da1c-186">The document header might have a set of default dimensions, as in the case of the purchase order that is used in this example.</span></span> <span data-ttu-id="8da1c-187">この例では、顧客または仕入先のオーダーには一連の既定の分析コードが存在します。</span><span class="sxs-lookup"><span data-stu-id="8da1c-187">The customer or, in this example, the vendor for the order also has a set of default dimensions.</span></span> <span data-ttu-id="8da1c-188">注文のビジネスロジックによっては、これらのさまざまな既定の分析コードの組み合わせによって優先順位が異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="8da1c-188">Depending on the business logic of the order, these various sets of default dimensions might have different precedence when they are combined.</span></span> <span data-ttu-id="8da1c-189">既定の分析コードの中で優先順位が高いものは、他の既定の分析コードを置き換えることがあります。</span><span class="sxs-lookup"><span data-stu-id="8da1c-189">Some default dimensions might have higher precedence and replace other default dimensions.</span></span> <span data-ttu-id="8da1c-190">また、既定の分析コードがマージされる場合もあります。</span><span class="sxs-lookup"><span data-stu-id="8da1c-190">However, some default dimensions might be merged together.</span></span>

### <a name="copying-default-dimensions"></a><span data-ttu-id="8da1c-191">既定の分析コードをコピーする</span><span class="sxs-lookup"><span data-stu-id="8da1c-191">Copying default dimensions</span></span>

<span data-ttu-id="8da1c-192">以下の図は、ある販売店の主勘定に入力された既定の分析コードを示しています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-192">The following illustration shows a default dimension that is entered on a specific vendor account.</span></span>

<span data-ttu-id="8da1c-193">![入力された特定の仕入先勘定の既定の分析コード](./media/DefaultDimensionVendor.png "入力された特定の仕入先勘定の既定の分析コード")</span><span class="sxs-lookup"><span data-stu-id="8da1c-193">![Default dimension entered on a specific vendor account](./media/DefaultDimensionVendor.png "Default dimension entered on a specific vendor account")</span></span>

<span data-ttu-id="8da1c-194">以下の図は、仕入先レコードの既定の分析コード参照に対するSQLクエリを示しています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-194">The following illustration shows the SQL query for the default dimension reference on the vendor record.</span></span>

<span data-ttu-id="8da1c-195">![仕入先レコードのデフォルトの分析コード参照に対するSQLクエリ](./media/DefaultDimensions3-SQLVendor.png "仕入先レコードのデフォルトの分析コード参照に対するSQLクエリ")</span><span class="sxs-lookup"><span data-stu-id="8da1c-195">![SQL query for the default dimension reference on the vendor record](./media/DefaultDimensions3-SQLVendor.png "SQL query for the default dimension reference on the vendor record")</span></span>

<span data-ttu-id="8da1c-196">以下の図は、作成された既定の分析コードを示しています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-196">The following illustration shows the default dimension that is created.</span></span>

<span data-ttu-id="8da1c-197">![既定の分析コードの生成](./media/DefaultDimensions3-SQLResultVendor.png "既定の分析コードの生成")</span><span class="sxs-lookup"><span data-stu-id="8da1c-197">![Resulting default dimension](./media/DefaultDimensions3-SQLResultVendor.png "Resulting default dimension")</span></span>

<span data-ttu-id="8da1c-198">以下の図は、この仕入先に対して作成された新しい発注書を示しています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-198">The following illustration shows a new purchase order that is created for this vendor.</span></span> <span data-ttu-id="8da1c-199">既定の分析コードがドキュメントヘッダーにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-199">The default dimension is copied to the document header.</span></span>

<span data-ttu-id="8da1c-200">![既定の分析コードドキュメントヘッダーにコピーされた既定の分析コード (発注書)](./media/DefaultDimensions3-CopiedToDocHeader.png "既定の分析コードドキュメントヘッダーにコピーされた既定の分析コード (発注書)")</span><span class="sxs-lookup"><span data-stu-id="8da1c-200">![Default dimension copied to a document header (purchase order)](./media/DefaultDimensions3-CopiedToDocHeader.png "Default dimension copied to a document header (purchase order)")</span></span>

<span data-ttu-id="8da1c-201">以下の図は、SQLクエリとヘッダレコードへの既定の分析コード参照を示しています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-201">The following illustration shows the SQL query and default dimension reference on the header record.</span></span> 

<span data-ttu-id="8da1c-202">![発注書レコードのデフォルトのディメンションを表示するSQLクエリと出力](./media/DefaultDimensions3-SQLCopiedToDocHeader.png "発注書レコードのデフォルトのディメンションを表示するSQLクエリと出力")</span><span class="sxs-lookup"><span data-stu-id="8da1c-202">![SQL query and output that shows default dimensions on a purchase order record](./media/DefaultDimensions3-SQLCopiedToDocHeader.png "SQL query and output showing default dimensions on a purchase order record")</span></span>

<span data-ttu-id="8da1c-203">以下の図にあるように、仕入先を選択するとただちに、発注書ヘッダーに既に存在する分析コードが仕入先の分析コードによって置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-203">As the following illustration shows, as soon as a vendor is selected, the dimensions from the vendor replaces any dimensions that were already on the purchase order header.</span></span>

![仕入先からコピーされた既定の分析コード。](./media/DefaultDimensions3-SQLResultCopiedToDocHeader.png)

<span data-ttu-id="8da1c-205">したがって、既定の分析コードの外部キーをコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8da1c-205">Therefore, the default dimension foreign key just had to be copied.</span></span> <span data-ttu-id="8da1c-206">以下の図は、仕入先から購買発注へ既定の分析コードをコピーするために使用されるコードを示しています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-206">The following illustration shows the code that is used to copy default dimensions from the vendor to the purchase order.</span></span>

<span data-ttu-id="8da1c-207">![仕入先から購買発注へのデフォルトディメンションのコピーに使用されるコード](./media/DefaultDimensions3-6CodetoCopy.png "仕入先から購買発注へのデフォルトディメンションのコピーに使用されるコード")</span><span class="sxs-lookup"><span data-stu-id="8da1c-207">![Code used to copy default dimensions from the vendor to the purchase order](./media/DefaultDimensions3-6CodetoCopy.png "Code used to copy default dimensions from the vendor to the purchase order")</span></span>

<span data-ttu-id="8da1c-208">次の図は、ユーザーがプロジェクト分析コード値を入力した後のヘッダー分析コードを示しています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-208">The following illustration shows the header dimensions after a user enters a value for the Project dimension.</span></span> 

<span data-ttu-id="8da1c-209">![伝票ヘッダ (発注書)でユーザが変更した既定の分析コード](./media/DefaultDimensions3-7DocumentHeader.png "伝票ヘッダ (発注書)でユーザが変更した既定の分析コード")</span><span class="sxs-lookup"><span data-stu-id="8da1c-209">![Default dimension modified by a user on a document header (purchase order)](./media/DefaultDimensions3-7DocumentHeader.png "Default dimension modified by a user on a document header (purchase order)")</span></span>

<span data-ttu-id="8da1c-210">以下の図は、ヘッダレコードの既定の分析コード参照に対するSQLクエリを示しています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-210">The following illustration shows the SQL query for the default dimension reference on the header record.</span></span>

<span data-ttu-id="8da1c-211">![DefaultDimensions3-8SQLModifiedDocHearder.png](./media/DefaultDimensions3-8SQLModifiedDocHearder.png "SQLクエリ")</span><span class="sxs-lookup"><span data-stu-id="8da1c-211">![DefaultDimensions3-8SQLModifiedDocHearder.png](./media/DefaultDimensions3-8SQLModifiedDocHearder.png "SQL query")</span></span>

<span data-ttu-id="8da1c-212">以下の図は、作成された既定の分析コードを示しています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-212">The following illustration shows the default dimension that is created.</span></span>

<span data-ttu-id="8da1c-213">![DefaultDimensions3-8SQLResultModifiedDocHearder.png](./media/DefaultDimensions3-8SQLResultModifiedDocHearder.png "発注書レコードの更新された既定の分析コード")</span><span class="sxs-lookup"><span data-stu-id="8da1c-213">![DefaultDimensions3-8SQLResultModifiedDocHearder.png](./media/DefaultDimensions3-8SQLResultModifiedDocHearder.png "Output showing updated default dimensions on purchase order record")</span></span>

<span data-ttu-id="8da1c-214">ユーザーが **ライン** ビューに切り替えて明細行を入力すると、以下の図に示すように、発注書ヘッダーから既定の分析コードがコピーされます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-214">When the user switches to the **Line** view to enter lines, default dimensions are copied from the purchase order header, as the following illustration shows.</span></span>

<span data-ttu-id="8da1c-215">![伝票明細(発注書)にコピーされた既定の分析コード](./media/DefaultDimensions3-9CopiedToLine.png "伝票明細(発注書)にコピーされた既定の分析コード")</span><span class="sxs-lookup"><span data-stu-id="8da1c-215">![Default dimensions copied to a document line (purchase order line)](./media/DefaultDimensions3-9CopiedToLine.png "Default dimensions copied to a document line (purchase order line)")</span></span>

<span data-ttu-id="8da1c-216">以下の図は、外部キー参照を行にコピーするために使用されるコードを示しています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-216">The following illustration shows the code that is used to copy the foreign key reference to the line.</span></span> <span data-ttu-id="8da1c-217">この例では、明細行はまだ保存されていません。</span><span class="sxs-lookup"><span data-stu-id="8da1c-217">In this case, the line hasn't yet been saved.</span></span> <span data-ttu-id="8da1c-218">そのため、既定の分析コードの外部キーは、メモリのテーブルバッファーのみに表示されます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-218">Therefore, the default dimension foreign key appears only in the table buffer in memory.</span></span>

<span data-ttu-id="8da1c-219">![既定の分析コードをヘッダーから行にコピーするために使用されるコード](./media/DefaultDimensions3-10CodeToCopyToLine.png "既定の分析コードをヘッダーから行にコピーするために使用されるコード")</span><span class="sxs-lookup"><span data-stu-id="8da1c-219">![Code used to copy default dimensions from the header to the line](./media/DefaultDimensions3-10CodeToCopyToLine.png "Code used to copy default dimensions from the header to the line")</span></span>

## <a name="merging-patterns"></a><span data-ttu-id="8da1c-220">パターンのマージ</span><span class="sxs-lookup"><span data-stu-id="8da1c-220">Merging patterns</span></span>

<span data-ttu-id="8da1c-221">このセクションでは、エンティティ間で既定の分析コードがどのようにマージされるかを説明します。</span><span class="sxs-lookup"><span data-stu-id="8da1c-221">This section explains how default dimensions are merged between entities.</span></span>

### <a name="merging-default-dimensions"></a><span data-ttu-id="8da1c-222">既定の分析コードのマージ</span><span class="sxs-lookup"><span data-stu-id="8da1c-222">Merging default dimensions</span></span>

<span data-ttu-id="8da1c-223">次の図では、ユーザーが行の BusinessUnit 分析コードを手動で削除しました。</span><span class="sxs-lookup"><span data-stu-id="8da1c-223">In the following illustration, the user has manually cleared the BusinessUnit dimension on the line.</span></span> <span data-ttu-id="8da1c-224">その結果、新しい既定の分析コード外部キーが作成され、発注書ヘッダーが更新されます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-224">Therefore, a new default dimension foreign key is created, and the purchase order header is updated.</span></span> 

<span data-ttu-id="8da1c-225">![伝票明細(発注書)で変更された既定の分析コード](./media/DefaultDimension4-1DimOnLine.png "伝票明細(発注書)で変更された既定の分析コード")</span><span class="sxs-lookup"><span data-stu-id="8da1c-225">![Default dimension modified on a document line (purchase order line)](./media/DefaultDimension4-1DimOnLine.png "Default dimension modified on a document line (purchase order line)")</span></span>

<span data-ttu-id="8da1c-226">この例ではヘッダーはまだ保存されていないため、更新された外部キーはメモリのテーブルバッファーにのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-226">Because the header hasn't yet been saved, the updated foreign key appears only in the table buffer in memory.</span></span> <span data-ttu-id="8da1c-227">ただし、以下の図に示すように、新しい既定の分析コードを照会して検索することができます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-227">However, as the following illustrations show, the new default dimension can be queried and found.</span></span>

<span data-ttu-id="8da1c-228">![新しい既定の分析コードを検索するSQLクエリ](./media/DefaultDimension4-1SQLDimOnLine.png "新しい既定の分析コードを検索するSQLクエリ")</span><span class="sxs-lookup"><span data-stu-id="8da1c-228">![SQL query to find the new default dimension](./media/DefaultDimension4-1SQLDimOnLine.png "SQL query to find the new default dimension")</span></span>

<span data-ttu-id="8da1c-229">![更新された既定の分析コード](./media/DefaultDimension4-2SQLResultsOnLine.png "更新された既定の分析コード")</span><span class="sxs-lookup"><span data-stu-id="8da1c-229">![Updated default dimensions](./media/DefaultDimension4-2SQLResultsOnLine.png "Updated default dimensions")</span></span>

<span data-ttu-id="8da1c-230">次に、ユーザーが購買注文の明細行に入力する品目を考えてみます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-230">Now consider the item that the user will enter on the purchase order line.</span></span> <span data-ttu-id="8da1c-231">以下の図は、製品タブでの既定の財務分析コードを示しています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-231">The following illustration shows the default financial dimensions on the released product.</span></span>

<span data-ttu-id="8da1c-232">![品目の既定の分析コード](./media/DefaultDimension4-3Item.png "品目の既定の分析コード")</span><span class="sxs-lookup"><span data-stu-id="8da1c-232">![Default dimensions on an item](./media/DefaultDimension4-3Item.png "Default dimensions on an item")</span></span>

<span data-ttu-id="8da1c-233">以下の図は、データベース内の既定の分析コードに対するSQLクエリを示しています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-233">The following illustration shows the SQL query for those default dimensions in the database.</span></span>

<span data-ttu-id="8da1c-234">![SQLクエリ](./media/DefaultDimension4-4SQLItem.png "SQLクエリ")</span><span class="sxs-lookup"><span data-stu-id="8da1c-234">![SQL query](./media/DefaultDimension4-4SQLItem.png "SQL query")</span></span>

<span data-ttu-id="8da1c-235">以下の図は、クエリの実行結果を示しています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-235">The following illustration shows the results of the query.</span></span>

<span data-ttu-id="8da1c-236">![品目レコードの既定の分析コードを出力](./media/DefaultDimension4-4SQLResultsItem.png "品目レコードの既定の分析コードを出力")</span><span class="sxs-lookup"><span data-stu-id="8da1c-236">![Output showing default dimensions on an item record](./media/DefaultDimension4-4SQLResultsItem.png "Output showing default dimensions on an item record")</span></span>

<span data-ttu-id="8da1c-237">続いて、購買注文の明細行に品目を入力します。</span><span class="sxs-lookup"><span data-stu-id="8da1c-237">Next, the user enters the item on the purchase order line.</span></span> <span data-ttu-id="8da1c-238">以下の図は、購買注文の明細行で選択された品目と、その結果の既定の分析コードを示しています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-238">The following illustration shows the item selected on the purchase order line and the resulting default dimensions.</span></span> <span data-ttu-id="8da1c-239">この場合、既定の分析コード値は発注書ロジックによってマージされています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-239">In this case, the default dimension values were merged by the purchase order logic.</span></span>

![ドキュメント明細行 (購買注文の明細行) の既定の分析コード値のマージ](./media/DefaultDimension4-5PurchLineResult.png)

<span data-ttu-id="8da1c-241">以下の図は、SQLクエリとその実行結果と購買注文明細行の品目レコードの既定の分析コードを示しています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-241">The following illustrations show the SQL query and the resulting default dimensions from the item record on the purchase order line.</span></span>

<span data-ttu-id="8da1c-242">[![SQL クエリ](./media/DefaultDimension4-6SQLOnItem.png)](./media/DefaultDimension4-6SQLOnItem.png)</span><span class="sxs-lookup"><span data-stu-id="8da1c-242">[![SQL query](./media/DefaultDimension4-6SQLOnItem.png)](./media/DefaultDimension4-6SQLOnItem.png)</span></span>

<span data-ttu-id="8da1c-243">[![ドキュメント明細行の品目レコードの既定の分析コードを示す出力 (購買注文明細行)](./media/DefaultDimension4-6SQLResultOnItem.png)](./media/DefaultDimension4-6SQLResultOnItem.png)</span><span class="sxs-lookup"><span data-stu-id="8da1c-243">[![Output showing default dimensions from an item record on an document line (purchase order line)](./media/DefaultDimension4-6SQLResultOnItem.png)](./media/DefaultDimension4-6SQLResultOnItem.png)</span></span>

<span data-ttu-id="8da1c-244">品目が購買注文の明細行に対して指定されている場合、発注書のロジックが3つの異なる参照元の既定の分析コードをマージます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-244">When the item is specified for a purchase order line, the purchase order logic merges the default dimensions from three different sources.</span></span> <span data-ttu-id="8da1c-245">以下の情報を参照してください</span><span class="sxs-lookup"><span data-stu-id="8da1c-245">Consider the following information:</span></span>

- <span data-ttu-id="8da1c-246">注文ヘッダーの既定の分析コードが、注文明細行の既定の分析コードとマージされて、"結合結果1" の既定の分析コードが生成されます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-246">Default dimensions on the order header are merged with default dimensions on the order line to yield "merged result 1" default dimensions.</span></span>

    |                  | <span data-ttu-id="8da1c-247">注文明細行</span><span class="sxs-lookup"><span data-stu-id="8da1c-247">Order line</span></span> | <span data-ttu-id="8da1c-248">注文ヘッダー</span><span class="sxs-lookup"><span data-stu-id="8da1c-248">Order header</span></span> | <span data-ttu-id="8da1c-249">マージの結果 1</span><span class="sxs-lookup"><span data-stu-id="8da1c-249">Merged result 1</span></span> | <span data-ttu-id="8da1c-250">説明</span><span class="sxs-lookup"><span data-stu-id="8da1c-250">Description</span></span> |
    |------------------|------------|--------------|-----------------|-------------|
    | <span data-ttu-id="8da1c-251">**BusinessUnit**</span><span class="sxs-lookup"><span data-stu-id="8da1c-251">**BusinessUnit**</span></span> |            |              |                 | <span data-ttu-id="8da1c-252">この値は、両方のソースで空白です。</span><span class="sxs-lookup"><span data-stu-id="8da1c-252">The value is blank in both sources.</span></span> |
    | <span data-ttu-id="8da1c-253">**CostCenter**</span><span class="sxs-lookup"><span data-stu-id="8da1c-253">**CostCenter**</span></span>   |            |              |                 | <span data-ttu-id="8da1c-254">この値は、両方のソースで空白です。</span><span class="sxs-lookup"><span data-stu-id="8da1c-254">The value is blank in both sources.</span></span> |
    | <span data-ttu-id="8da1c-255">**部門**</span><span class="sxs-lookup"><span data-stu-id="8da1c-255">**Department**</span></span>   |            | <span data-ttu-id="8da1c-256">027</span><span class="sxs-lookup"><span data-stu-id="8da1c-256">027</span></span>          | <span data-ttu-id="8da1c-257">027</span><span class="sxs-lookup"><span data-stu-id="8da1c-257">027</span></span>             | <span data-ttu-id="8da1c-258">注文明細行の値は空白です。</span><span class="sxs-lookup"><span data-stu-id="8da1c-258">The value is blank on the order line.</span></span> <span data-ttu-id="8da1c-259">結果として、この値は注文ヘッダーからコピーされます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-259">Therefore, the value is copied from the order header.</span></span> |
    | <span data-ttu-id="8da1c-260">**ItemGroup**</span><span class="sxs-lookup"><span data-stu-id="8da1c-260">**ItemGroup**</span></span>    |            |              |                 | <span data-ttu-id="8da1c-261">この値は、両方のソースで空白です。</span><span class="sxs-lookup"><span data-stu-id="8da1c-261">The value is blank in both sources.</span></span> |
    | <span data-ttu-id="8da1c-262">**プロジェクト**</span><span class="sxs-lookup"><span data-stu-id="8da1c-262">**Project**</span></span>      | <span data-ttu-id="8da1c-263">000003</span><span class="sxs-lookup"><span data-stu-id="8da1c-263">000003</span></span>     | <span data-ttu-id="8da1c-264">000003</span><span class="sxs-lookup"><span data-stu-id="8da1c-264">000003</span></span>       | <span data-ttu-id="8da1c-265">000003</span><span class="sxs-lookup"><span data-stu-id="8da1c-265">000003</span></span>          | <span data-ttu-id="8da1c-266">この値は、両方のソースで空白です。</span><span class="sxs-lookup"><span data-stu-id="8da1c-266">The value is the same in both sources.</span></span> |
    | <span data-ttu-id="8da1c-267">**外部キー**</span><span class="sxs-lookup"><span data-stu-id="8da1c-267">**Foreign key**</span></span>  | <span data-ttu-id="8da1c-268">\*\*6190</span><span class="sxs-lookup"><span data-stu-id="8da1c-268">\*\*6190</span></span>   | <span data-ttu-id="8da1c-269">\*9574</span><span class="sxs-lookup"><span data-stu-id="8da1c-269">\*9574</span></span>       | <span data-ttu-id="8da1c-270">\*9574</span><span class="sxs-lookup"><span data-stu-id="8da1c-270">\*9574</span></span>          | <span data-ttu-id="8da1c-271">マージされた後は、注文ヘッダーと同じレコードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-271">The merged result uses the same record as the order header.</span></span> |

- <span data-ttu-id="8da1c-272">品目の既定の分析コードが、注文明細行の "結合結果1" とマージされて、"結合結果2" の既定の分析コードが生成されます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-272">Default dimensions on the item are merged with the "merged result 1" default dimensions to yield default dimensions on the final order line ("merged result 2" default dimensions).</span></span> <span data-ttu-id="8da1c-273">以下の表では、マージ処理の際の論理ステップを示しています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-273">The following table shows the logical steps of the merge that occurs.</span></span> <span data-ttu-id="8da1c-274">ただし、これらの手順は、実行時に、dimensionフレームワークによって提供されるAPIを使用してマージされます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-274">However, these steps are combined during execution by using the APIs that the dimension framework provides.</span></span>

    |                  | <span data-ttu-id="8da1c-275">マージの結果 1</span><span class="sxs-lookup"><span data-stu-id="8da1c-275">Merged result 1</span></span> | <span data-ttu-id="8da1c-276">項目</span><span class="sxs-lookup"><span data-stu-id="8da1c-276">Item</span></span>     | <span data-ttu-id="8da1c-277">マージの結果 2</span><span class="sxs-lookup"><span data-stu-id="8da1c-277">Merged result 2</span></span> | <span data-ttu-id="8da1c-278">説明</span><span class="sxs-lookup"><span data-stu-id="8da1c-278">Description</span></span> |
    |------------------|-----------------|----------|-----------------|-------------|
    | <span data-ttu-id="8da1c-279">**BusinessUnit**</span><span class="sxs-lookup"><span data-stu-id="8da1c-279">**BusinessUnit**</span></span> |                 |          |                 | <span data-ttu-id="8da1c-280">この値は、両方のソースで空白です。</span><span class="sxs-lookup"><span data-stu-id="8da1c-280">The value is blank in both sources.</span></span> |
    | <span data-ttu-id="8da1c-281">**CostCenter**</span><span class="sxs-lookup"><span data-stu-id="8da1c-281">**CostCenter**</span></span>   |                 | <span data-ttu-id="8da1c-282">008</span><span class="sxs-lookup"><span data-stu-id="8da1c-282">008</span></span>      | <span data-ttu-id="8da1c-283">008</span><span class="sxs-lookup"><span data-stu-id="8da1c-283">008</span></span>             | <span data-ttu-id="8da1c-284">ヘッダー行の結合結果の値が空白です。</span><span class="sxs-lookup"><span data-stu-id="8da1c-284">The value is blank in the header line merged result.</span></span> <span data-ttu-id="8da1c-285">結果として、この値は品目からコピーされます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-285">Therefore, the value is copied from the item.</span></span> |
    | <span data-ttu-id="8da1c-286">**部門**</span><span class="sxs-lookup"><span data-stu-id="8da1c-286">**Department**</span></span>   | <span data-ttu-id="8da1c-287">027</span><span class="sxs-lookup"><span data-stu-id="8da1c-287">027</span></span>             | <span data-ttu-id="8da1c-288">023</span><span class="sxs-lookup"><span data-stu-id="8da1c-288">023</span></span>      | <span data-ttu-id="8da1c-289">027</span><span class="sxs-lookup"><span data-stu-id="8da1c-289">027</span></span>             | <span data-ttu-id="8da1c-290">ヘッダー行の結合結果の値がセットされます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-290">The value is set in the header line merged result.</span></span> <span data-ttu-id="8da1c-291">したがって、その品目はスキップされます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-291">Therefore, the item is skipped.</span></span> |
    | <span data-ttu-id="8da1c-292">**ItemGroup**</span><span class="sxs-lookup"><span data-stu-id="8da1c-292">**ItemGroup**</span></span>    |                 | <span data-ttu-id="8da1c-293">AudioRM</span><span class="sxs-lookup"><span data-stu-id="8da1c-293">AudioRM</span></span>  | <span data-ttu-id="8da1c-294">AudioRM</span><span class="sxs-lookup"><span data-stu-id="8da1c-294">AudioRM</span></span>         | <span data-ttu-id="8da1c-295">ヘッダー行の結合結果の値が空白です。</span><span class="sxs-lookup"><span data-stu-id="8da1c-295">The value is blank in the header line merged result.</span></span> <span data-ttu-id="8da1c-296">結果として、この値は品目からコピーされます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-296">Therefore, the value is copied from the item.</span></span> |
    | <span data-ttu-id="8da1c-297">**プロジェクト**</span><span class="sxs-lookup"><span data-stu-id="8da1c-297">**Project**</span></span>      | <span data-ttu-id="8da1c-298">000003</span><span class="sxs-lookup"><span data-stu-id="8da1c-298">000003</span></span>          |          | <span data-ttu-id="8da1c-299">000003</span><span class="sxs-lookup"><span data-stu-id="8da1c-299">000003</span></span>          | <span data-ttu-id="8da1c-300">ヘッダー行の結合結果の値がセットされます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-300">The value is set in the header line merged result.</span></span> |
    | <span data-ttu-id="8da1c-301">**外部キー**</span><span class="sxs-lookup"><span data-stu-id="8da1c-301">**Foreign key**</span></span>  | <span data-ttu-id="8da1c-302">\*6190</span><span class="sxs-lookup"><span data-stu-id="8da1c-302">\*6190</span></span>          | <span data-ttu-id="8da1c-303">\*\*0324</span><span class="sxs-lookup"><span data-stu-id="8da1c-303">\*\*0324</span></span> | <span data-ttu-id="8da1c-304">\*\*0325</span><span class="sxs-lookup"><span data-stu-id="8da1c-304">\*\*0325</span></span>        | <span data-ttu-id="8da1c-305">マージ後の結果に対して新しいレコードIDが使用されます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-305">A new record ID is used for the merged result.</span></span> |

<span data-ttu-id="8da1c-306">以下の図は、3つのソースからから既定の分析コードをマージするために使用されるコードを示しています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-306">The following illustration shows the code that is required in order to merge the dimensions from the three sources.</span></span>

<span data-ttu-id="8da1c-307">[![注文ヘッダー、注文明細行、および品目から分析コードをマージするコード](./media/DefaultDimension4-8CodeToMerge.png)](./media/DefaultDimension4-8CodeToMerge.png)</span><span class="sxs-lookup"><span data-stu-id="8da1c-307">[![Code to merge dimensions from the order header, order line, and item](./media/DefaultDimension4-8CodeToMerge.png)](./media/DefaultDimension4-8CodeToMerge.png)</span></span>

## <a name="creating-ledger-dimensions"></a><span data-ttu-id="8da1c-308">勘定分析コードの作成</span><span class="sxs-lookup"><span data-stu-id="8da1c-308">Creating ledger dimensions</span></span>

<span data-ttu-id="8da1c-309">このセクションでは、新しい勘定分析コードを作成するために既定の分析コードをマージするか方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8da1c-309">This section explains how default dimensions can be merged to create new ledger dimensions.</span></span>

<span data-ttu-id="8da1c-310">既定の分析コードは、仕訳帳と勘定配布で使用される勘定科目の組み合わせを作成するために後のステップで使用される値を提供します。</span><span class="sxs-lookup"><span data-stu-id="8da1c-310">Default dimensions provide values that will be used later to create ledger account combinations that are used in journals and accounting distributions.</span></span> <span data-ttu-id="8da1c-311">[勘定科目の組み合わせに関する一連のブログの記事](https://blogs.msdn.com/b/ax_gfm_framework_team_blog/archive/2013/02/15/ledger-account-combinations-part-5-_2800_ledger-dimensions_2900_-.aspx)に定義されている内容に従い、勘定科目の組み合わせには、構造と順序が適用される MainAccount と 分析コード値の組み合わせのみを使用します。</span><span class="sxs-lookup"><span data-stu-id="8da1c-311">According to the definition in the [Ledger account combinations series of blog posts](https://blogs.msdn.com/b/ax_gfm_framework_team_blog/archive/2013/02/15/ledger-account-combinations-part-5-_2800_ledger-dimensions_2900_-.aspx), a ledger account combination is just a set of MainAccount and dimension values that structure and order are applied to.</span></span>

<span data-ttu-id="8da1c-312">既定の分析コードには、 MainAccount 以外の勘定科目の組み合わせに必要なすべての分析コードが用意されています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-312">Default dimensions provide all the dimensions, except MainAccount, that are required for a ledger account combination.</span></span> <span data-ttu-id="8da1c-313">既定の分析コードは既定の勘定と組み合わせることも、別の勘定分析コードを組み合わせて勘定分析コードを生成することもできます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-313">Default dimensions can be combined with a default account, or they can be combined another ledger dimension to produce a ledger dimension.</span></span>

<span data-ttu-id="8da1c-314">次の図は、購買注文明細行から勘定配布を実行する例を示しています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-314">The following illustrations show an example where accounting distributions are being done from the purchase order line.</span></span> <span data-ttu-id="8da1c-315">注文明細行から **購買 \> 財務配分金額** を選択し **勘定配布** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-315">The user selects **Financials \> Distribute amounts** from the purchase order line to open the **Accounting distributions** page.</span></span> <span data-ttu-id="8da1c-316">このページでは、既定の勘定科目の組み合わせである **618900--027-008audiorm**-が既に入力されています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-316">On that page, a default ledger account combination, **618900--027-008-AudioRM**, is already entered.</span></span>

<span data-ttu-id="8da1c-317">[![金額の配分を配布する](./media/DefaultDimension5-1AccountingDistributions.png)](./media/DefaultDimension5-1AccountingDistributions.png)</span><span class="sxs-lookup"><span data-stu-id="8da1c-317">[![Distribute amounts command](./media/DefaultDimension5-1AccountingDistributions.png)](./media/DefaultDimension5-1AccountingDistributions.png)</span></span> 

<span data-ttu-id="8da1c-318">[![勘定配布ページ](./media/DefaultDimension5-1AcctDistForm.png)](./media/DefaultDimension5-1AcctDistForm.png)</span><span class="sxs-lookup"><span data-stu-id="8da1c-318">[![Accounting distributions page](./media/DefaultDimension5-1AcctDistForm.png)](./media/DefaultDimension5-1AcctDistForm.png)</span></span>

<span data-ttu-id="8da1c-319">プロジェクト、コストセンター、ItemGroup、部門 の各分析コードの値が会計のディストリビューションに入力されています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-319">The values for the Project, CostCenter, ItemGroup, and Department dimensions have been filled in to the accounting distrobution.</span></span> <span data-ttu-id="8da1c-320">また、次の図に示すように、転記品目グループの既定の MainAccount の値は、購買注文の経費勘定の購買経費として品目に入力されています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-320">Additionally, the default MainAccount value from the posting item group has been entered on the item as the purchase expenditure for expense account for a purchase order, as the following illustration shows.</span></span> <span data-ttu-id="8da1c-321">プロジェクトは、ここに該当する勘定構造の一部ではないため、表示されません。</span><span class="sxs-lookup"><span data-stu-id="8da1c-321">The project isn't shown because it isn't part of the applicable account structure.</span></span>

<span data-ttu-id="8da1c-322">[![リリース済製品の詳細ページ](./media/DefaultDimension5-1SourceofMainAccountOnPO.png)](./media/DefaultDimension5-1SourceofMainAccountOnPO.png)</span><span class="sxs-lookup"><span data-stu-id="8da1c-322">[![Released product details page](./media/DefaultDimension5-1SourceofMainAccountOnPO.png)](./media/DefaultDimension5-1SourceofMainAccountOnPO.png)</span></span> 

<span data-ttu-id="8da1c-323">[![消費品目 グループの詳細](./media/DefaultDimension5-1SourceOfMAonPO2.png)](./media/DefaultDimension5-1SourceOfMAonPO2.png)</span><span class="sxs-lookup"><span data-stu-id="8da1c-323">[![Details of the Consume item group](./media/DefaultDimension5-1SourceOfMAonPO2.png)](./media/DefaultDimension5-1SourceOfMAonPO2.png)</span></span> 

<span data-ttu-id="8da1c-324">以下の図は、クエリおよびその結果となる既定のアカウントのソースを示しています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-324">The following illustrations show the query and the resulting default account source.</span></span>

<span data-ttu-id="8da1c-325">![SQLクエリ](./media/DefaultDimension5-3SQLDefaultSource.png "SQLクエリ")</span><span class="sxs-lookup"><span data-stu-id="8da1c-325">![SQL query](./media/DefaultDimension5-3SQLDefaultSource.png "SQL query")</span></span>

<span data-ttu-id="8da1c-326">![既定のアカウントソースの結果表示](./media/DefaultDimension5-3SQLResultDefaultSource.png "既定のアカウントソースの結果表示")</span><span class="sxs-lookup"><span data-stu-id="8da1c-326">![Results showing the default account source](./media/DefaultDimension5-3SQLResultDefaultSource.png "Results showing the default account source")</span></span>

<span data-ttu-id="8da1c-327">次の図は、品目グループの既定の勘定を含む購買注文明細行の既定の分析コードをマージするために必要なコードを示しています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-327">The following illustration shows the code that is required in order to merge the default dimension on the purchase order line with the default account from the item group.</span></span> 

<span data-ttu-id="8da1c-328">![既定の勘定コードを既定の勘定と結合に使用されるコード](./media/DefaultDimension5-4CodeToMerge.png "既定の勘定コードを既定の勘定と結合に使用されるコード")</span><span class="sxs-lookup"><span data-stu-id="8da1c-328">![Code used to merge the default dimension with a default account](./media/DefaultDimension5-4CodeToMerge.png "Code used to merge the default dimension with a default account")</span></span>

<span data-ttu-id="8da1c-329">マージが完了すると、以下の図に示すクエリのように、新しい勘定科目の組み合わせが作成されます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-329">After the merge is completed, a new ledger account combination is created, as the query in the following illustration shows.</span></span> <span data-ttu-id="8da1c-330">この動作は、既定の分析コードが相互にマージされる際の挙動と共通しています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-330">This behavior resembles the behavior when default dimensions are merged with each other.</span></span>

<span data-ttu-id="8da1c-331">![マージされた既定の勘定と既定の分析コードを示すSQLクエリおよび結果](./media/DefaultDimension5-5SQLResultMerged.png "マージされた既定の勘定と既定の分析コードを示すSQLクエリおよび結果")</span><span class="sxs-lookup"><span data-stu-id="8da1c-331">![SQL query and results showing a merged default account and default dimension](./media/DefaultDimension5-5SQLResultMerged.png "SQL query and results showing a merged default account and default dimension")</span></span>

## <a name="common-pattern-apis"></a><span data-ttu-id="8da1c-332">一般的なAPIのパターン</span><span class="sxs-lookup"><span data-stu-id="8da1c-332">Common pattern APIs</span></span>

<span data-ttu-id="8da1c-333">このセクションでは、最も一般的な既定のパターンに使用されるAPIについて説明します。</span><span class="sxs-lookup"><span data-stu-id="8da1c-333">This section describes the APIs that are used for the most common defaulting patterns.</span></span>

### <a name="default-dimension-apis"></a><span data-ttu-id="8da1c-334">既定の分析コードAPI</span><span class="sxs-lookup"><span data-stu-id="8da1c-334">Default dimension APIs</span></span>

<span data-ttu-id="8da1c-335">**Dimensiondefaultfacade** と **LedgerDimensionDefaultFacade** クラスは、既定化を行うシナリオで必要なAPIを提供します。</span><span class="sxs-lookup"><span data-stu-id="8da1c-335">The **DimensionDefaultFacade** and **LedgerDimensionDefaultFacade** classes provide the APIs that are required for defaulting scenarios.</span></span> <span data-ttu-id="8da1c-336">**LedgerDimensionFacade** クラス" には、勘定分析コードで作業するためのメソッドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-336">The **LedgerDimensionFacade** class contains methods for working with ledger dimensions.</span></span> <span data-ttu-id="8da1c-337">この方法は、パフォーマンスを優先し、高度に最適化されています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-337">The methods are highly optimized for performance.</span></span>

### <a name="default-dimensions"></a><span data-ttu-id="8da1c-338">既定の分析コード</span><span class="sxs-lookup"><span data-stu-id="8da1c-338">Default dimensions</span></span>

#### <a name="servicemergedefaultdimensions"></a><span data-ttu-id="8da1c-339">serviceMergeDefaultDimensions()</span><span class="sxs-lookup"><span data-stu-id="8da1c-339">serviceMergeDefaultDimensions()</span></span>

<span data-ttu-id="8da1c-340">**ServiceMergeDefaultDimensions** APIは、既定の分析コードに対して最も頻繁に使用されるAPIです。</span><span class="sxs-lookup"><span data-stu-id="8da1c-340">The **serviceMergeDefaultDimensions()** API is the most frequently used API for default dimensions.</span></span> <span data-ttu-id="8da1c-341">2つから4つの既定の分析コードから新たな既定の分析コードを作成する必要がある場合は、これを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="8da1c-341">It should be called whenever a new default dimension must be created from two to four other default dimensions.</span></span> <span data-ttu-id="8da1c-342">4つ以上の既定の分析コードをマージする必要がある場合は、このAPIを複数回呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-342">If more than four default dimensions must be merged, this API can be called multiple times.</span></span> <span data-ttu-id="8da1c-343">この場合、前回の呼び出しの結果を、後続の呼び出しの初期パラメータとして使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8da1c-343">In this case, the result of the previous call should be used as the first parameter for each subsequent call.</span></span> <span data-ttu-id="8da1c-344">この方法では、値が有効かどうかにかかわらず、すべての値が確実にマージされます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-344">This method will blindly merge all values, regardless of whether they are valid.</span></span>

<span data-ttu-id="8da1c-345">**例: DimensionDefaultFacade::serviceMergeDefaultDimensions ()**</span><span class="sxs-lookup"><span data-stu-id="8da1c-345">**Example: DimensionDefaultFacade::serviceMergeDefaultDimensions()**</span></span>

```
public static DimensionDefault serviceMergeDefaultDimensions(
    DimensionDefault _value1,
    DimensionDefault _value2,
    DimensionDefault _value3 = 0,
    DimensionDefault _value4 = 0)
```

#### <a name="servicereplaceattributevalue"></a><span data-ttu-id="8da1c-346">serviceReplaceAttributeValue()</span><span class="sxs-lookup"><span data-stu-id="8da1c-346">serviceReplaceAttributeValue()</span></span>

<span data-ttu-id="8da1c-347">ServiceReplaceAttributeValue **()** APIは、1つの分析コード値をある既定のセットから別の既定セットへとコピーする必要がある場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-347">The **serviceReplaceAttributeValue()** API is useful if a single dimension value must be copied from one default set to another default set.</span></span> <span data-ttu-id="8da1c-348">指定された値は、ソースセットに既に存在する任意の値に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-348">The specified value will replace whatever value already exists in the source set.</span></span>

<span data-ttu-id="8da1c-349">**例: DimensionDefaultFacade::serviceReplaceAttributeValue ()**</span><span class="sxs-lookup"><span data-stu-id="8da1c-349">**Example: DimensionDefaultFacade::serviceReplaceAttributeValue()**</span></span> 

```
public static DimensionDefault serviceReplaceAttributeValue(
    DimensionDefault _target,
    DimensionDefault _source,
    RecId _dimensionAttributeId)
```

#### <a name="servicemergevaliddefaultdimensions"></a><span data-ttu-id="8da1c-350">serviceMergeValidDefaultDimensions()</span><span class="sxs-lookup"><span data-stu-id="8da1c-350">serviceMergeValidDefaultDimensions()</span></span>

<span data-ttu-id="8da1c-351">**ServiceMergeValidDefaultDimensions ()** APIは、現在の元帳に対して有効な値のみをマージしていく場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="8da1c-351">The **serviceMergeValidDefaultDimensions()** API is useful if you want the merge to merge only values that are valid for the current ledger.</span></span> <span data-ttu-id="8da1c-352">**ServiceMergeDefaultDimensions** と同じように動作しますが、有効な値の検証がされます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-352">It works just like **serviceMergeDefaultDimensions** but includes a check for valid values.</span></span>

<span data-ttu-id="8da1c-353">**例: DimensionDefaultFacade::serviceReplaceAttributeValue ()**</span><span class="sxs-lookup"><span data-stu-id="8da1c-353">**Example: DimensionDefaultFacade::serviceReplaceAttributeValue()**</span></span> 

```
public static DimensionDefault serviceMergeValidDefaultDimensions(
    DimensionDefault _defaultDimension1,
    DimensionDefault _defaultDimension2,
    DimensionDefault _defaultDimension3 = 0,
    DimensionDefault _defaultDimension4 = 0)
```

### <a name="ledger-dimensions"></a><span data-ttu-id="8da1c-354">勘定分析コード</span><span class="sxs-lookup"><span data-stu-id="8da1c-354">Ledger dimensions</span></span>

#### <a name="servicecreateledgerdimension"></a><span data-ttu-id="8da1c-355">serviceCreateLedgerDimension()</span><span class="sxs-lookup"><span data-stu-id="8da1c-355">serviceCreateLedgerDimension()</span></span>

<span data-ttu-id="8da1c-356">**ServiceMergeDefaultDimensions** APIは、勘定分析コードに対して最も頻繁に使用されるAPIです。</span><span class="sxs-lookup"><span data-stu-id="8da1c-356">The **serviceCreateLedgerDimension()** API is the most frequently used API for ledger dimensions.</span></span> <span data-ttu-id="8da1c-357">このメソッドは、既定の勘定または既存の勘定科目の組み合わせと0 から3つの既定の分析コードから、新しい勘定科目の組み合わせを作成する必要がある場合に呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="8da1c-357">It should be called whenever a new ledger account combination must be created from a default account or an existing ledger account combination and zero to three default dimensions.</span></span> <span data-ttu-id="8da1c-358">3つ以上の既定の分析コードをマージする必要がある場合は、このAPIを複数回呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-358">If more than three default dimensions must be merged, this API can be called multiple times.</span></span> <span data-ttu-id="8da1c-359">この場合、さまざまなソースが、後続の呼び出しの初期パラメーターとして前回の呼び出し結果を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="8da1c-359">In this case, different sources take the result of the previous call as the first parameter for each subsequent call.</span></span> <span data-ttu-id="8da1c-360">MainAccount 分析コードは、指定された勘定分析コードからのみ取得されます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-360">The MainAccount dimension is retrieved only from the ledger dimension that is supplied.</span></span>

<span data-ttu-id="8da1c-361">**例: LedgerDimensionFacade.serviceCreateLedgerDimension()**</span><span class="sxs-lookup"><span data-stu-id="8da1c-361">**Example: LedgerDimensionFacade.serviceCreateLedgerDimension()**</span></span>

```
public static LedgerDimensionAccount serviceCreateLedgerDimension(
    RecId            _ledgerDimensionId,
    DimensionDefault _dimensionDefault1 = 0,
    DimensionDefault _dimensionDefault2 = 0,
    DimensionDefault _dimensionDefault3 = 0)
    {
```

#### <a name="servicecreateledgerdimensionfortype"></a><span data-ttu-id="8da1c-362">serviceCreateLedgerDimensionForType()</span><span class="sxs-lookup"><span data-stu-id="8da1c-362">serviceCreateLedgerDimensionForType()</span></span>

<span data-ttu-id="8da1c-363">**ServiceCreateLedgerDimensionForType ()** APIは、serviceCreateLedgerDimension **()** API と共通した特徴があります。</span><span class="sxs-lookup"><span data-stu-id="8da1c-363">The **serviceCreateLedgerDimensionForType()** API resembles the **serviceCreateLedgerDimension()** API.</span></span> <span data-ttu-id="8da1c-364">ただし、勘定科目の組み合わせを作成する代わりに、予算勘定や予算計画勘定など、他の勘定分析コードタイプを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-364">However, instead of creating a ledger account combination, it can create other ledger dimension types, such as budget accounts or budget planning accounts.</span></span> <span data-ttu-id="8da1c-365">**LedgerDimensionType** パラメーター は、作成された勘定科目のタイプを指定する際に使用します。</span><span class="sxs-lookup"><span data-stu-id="8da1c-365">The **LedgerDimensionType** parameter is used to specify the type of ledger account that is created.</span></span>

<span data-ttu-id="8da1c-366">**例: LedgerDimensionFacade.serviceCreateLedgerDimensionForType()**</span><span class="sxs-lookup"><span data-stu-id="8da1c-366">**Example: LedgerDimensionFacade.serviceCreateLedgerDimensionForType()**</span></span>

```
public static LedgerDimensionBase serviceCreateLedgerDimensionForType(
    LedgerDimensionType _ledgerDimensionType,
    LedgerDimensionBase _ledgerDimensionId,
    DimensionDefault    _dimensionDefault1 = 0,
    DimensionDefault    _dimensionDefault2 = 0,
    DimensionDefault    _dimensionDefault3 = 0)
```

#### <a name="servicecreateledgerdimfordefaultdim"></a><span data-ttu-id="8da1c-367">serviceCreateLedgerDimForDefaultDim()</span><span class="sxs-lookup"><span data-stu-id="8da1c-367">serviceCreateLedgerDimForDefaultDim()</span></span>

<span data-ttu-id="8da1c-368">**ServiceCreateLedgerDimForDefaultDim ()** APIは **serviceCreateLedgerDimension ()** および **serviceCreateLedgerDimensionForType ()** APIと共通した特徴を持っています。しかし、既定の分析コードの値は、新しい勘定分析コードに直接コピーされ、元帳分析コードの値は後でマージされます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-368">The **serviceCreateLedgerDimForDefaultDim()** API resembles the **serviceCreateLedgerDimension()** and **serviceCreateLedgerDimensionForType()** APIs, but the values from the default dimension are copied directly to the new ledger dimension, whereas the dimension values from the ledger dimension are merged afterwards.</span></span> <span data-ttu-id="8da1c-369">対照的に、前述の2つのAPIについては、勘定分析コード値がコピーされ、既定の分析コード値が結合されています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-369">(By contrast, for the previous two APIs, the ledger dimension values were copied, and the default dimension values were merged.)</span></span>

<span data-ttu-id="8da1c-370">**例: LedgerDimensionFacade::serviceCreateLedgerDimForDefaultDim()**</span><span class="sxs-lookup"><span data-stu-id="8da1c-370">**Example: LedgerDimensionFacade::serviceCreateLedgerDimForDefaultDim()**</span></span>

```
public static LedgerDimensionBase serviceCreateLedgerDimForDefaultDim(
    DimensionDefault    _defaultDimension,
    LedgerDimensionBase _ledgerDimensionId)![\\\\blackwoodstone\\share\\Research\\GFMBlog2\\media\\MSDNBlogsFS\\prod.evol.blogs.msdn.com\\CommunityServer.Blogs.Components.WeblogFiles\\00\\00\\01\\50\\86\\5710.c65.png](media/146d284328279f4737c6e2bd23a30530.png)
```

#### <a name="serviceledgerdimensionfromledgerdims"></a><span data-ttu-id="8da1c-371">serviceLedgerDimensionFromLedgerDims()</span><span class="sxs-lookup"><span data-stu-id="8da1c-371">serviceLedgerDimensionFromLedgerDims()</span></span>

<span data-ttu-id="8da1c-372">**Serviceledgerdimensionfromledgerdims ()** API は前述のAPIと共通する特徴を持っていますがていますが、新しい勘定分析コードを作成するためには、ソースとして元帳分析コードのみを使用します。</span><span class="sxs-lookup"><span data-stu-id="8da1c-372">The **serviceLedgerDimensionFromLedgerDims()** API resembles the previous APIs, but it uses only ledger dimensions as sources to construct a new ledger dimension.</span></span> <span data-ttu-id="8da1c-373">主勘定には、勘定分析コードからの固定値のみが適用されます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-373">The main account is retrieved only from the first ledger dimension.</span></span>

<span data-ttu-id="8da1c-374">**例: LedgerDimensionFacade::serviceLedgerDimensionFromLedgerDims()**</span><span class="sxs-lookup"><span data-stu-id="8da1c-374">**Example LedgerDimensionFacade::serviceLedgerDimensionFromLedgerDims()**</span></span>

```
public static LedgerDimensionAccount serviceLedgerDimensionFromLedgerDims(
    LedgerDimensionBase _ledgerDimensionId1,
    LedgerDimensionBase _ledgerDimensionId2 = 0,
    LedgerDimensionBase _ledgerDimensionId3 = 0,
    LedgerDimensionBase _ledgerDimensionId4 = 0,
    LedgerDimensionBase _ledgerDimensionId5 = 0)
```

#### <a name="servicemergeledgerdimensions"></a><span data-ttu-id="8da1c-375">serviceMergeLedgerDimensions()</span><span class="sxs-lookup"><span data-stu-id="8da1c-375">serviceMergeLedgerDimensions()</span></span>

<span data-ttu-id="8da1c-376">**ServiceMergeLedgerDimensions ()** APIは、 **serviceledgerdimensionfromledgerdims()** APIと共通とした特徴を持っていますが、2つの会計分析コードだけを組み合わせるように最適化されています。</span><span class="sxs-lookup"><span data-stu-id="8da1c-376">The **serviceMergeLedgerDimensions()** API resembles the **serviceLedgerDimensionFromLedgerDims()** API, but it's optimized to combine just two ledger dimensions.</span></span> 

<span data-ttu-id="8da1c-377">**例: LedgerDimensionFacade::serviceMergeLedgerDimensions()**</span><span class="sxs-lookup"><span data-stu-id="8da1c-377">**Example: LedgerDimensionFacade::serviceMergeLedgerDimensions()**</span></span>

```
public static LedgerDimensionBase serviceMergeLedgerDimensions(
    LedgerDimensionBase _ledgerDimension1,
    LedgerDimensionBase _ledgerDimension2,
    LedgerDimensionType _ledgerDimensionType = LedgerDimensionType::Account)
```

#### <a name="servicecreateledgerdimfromledgerdim"></a><span data-ttu-id="8da1c-378">serviceCreateLedgerDimFromLedgerDim()</span><span class="sxs-lookup"><span data-stu-id="8da1c-378">serviceCreateLedgerDimFromLedgerDim()</span></span>

<span data-ttu-id="8da1c-379">**ServiceCreateLedgerDimFromLedgerDim ()** APIは、過去に転記されたドキュメントから新しい未転記のドキュメントに元帳分析コードをコピーする場合と、現在の勘定構造の設定を確実に使用すように設定したい場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="8da1c-379">The **serviceCreateLedgerDimFromLedgerDim()** API is useful if you want to copy ledger dimensions from a historic posted document to a new unposted document, and you want to make sure that the current account structure configuration is used.</span></span> <span data-ttu-id="8da1c-380">これにより、転記時に新しい元帳分析コードを検証する際の検証エラーを防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="8da1c-380">In this way, you help prevent validation errors when the new ledger dimensions are validated during posting.</span></span>

<span data-ttu-id="8da1c-381">**例: LedgerDimensionFacade::serviceCreateLedgerDimFromLedgerDim()**</span><span class="sxs-lookup"><span data-stu-id="8da1c-381">**Example: LedgerDimensionFacade::serviceCreateLedgerDimFromLedgerDim()**</span></span>

```
public static LedgerDimensionAccount serviceCreateLedgerDimFromLedgerDim(LedgerDimensionAccount _ledgerDimension)
```