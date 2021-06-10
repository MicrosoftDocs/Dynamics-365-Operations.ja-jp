---
title: 財務分析コードのコンフィギュレーション
description: このトピックでは、アプリケーション ページを統合するための財務分析コードの構成について説明します。
author: RyanCCarlson2
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 91363
ms.assetid: 6be04fc8-5e2b-4ea6-b9bc-940fb5b811e5
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 268ae30c8ec759d1491c62659fbfbf4f711d6264
ms.sourcegitcommit: eff3da7ea98758f100d44ff7feec17157afc2e80
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/27/2021
ms.locfileid: "6111710"
---
# <a name="financial-dimension-configuration"></a><span data-ttu-id="53b29-103">財務分析コードのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="53b29-103">Financial dimension configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53b29-104">このトピックでは、財務分析コードの構成について説明します。</span><span class="sxs-lookup"><span data-stu-id="53b29-104">This topic describes the Financial dimension configuration.</span></span> <span data-ttu-id="53b29-105">設定には 2 つの重要な領域があります。</span><span class="sxs-lookup"><span data-stu-id="53b29-105">There are two important areas for setup:</span></span> 

- <span data-ttu-id="53b29-106">財務諸表のための財務分析コードの順序。</span><span class="sxs-lookup"><span data-stu-id="53b29-106">The order of financial dimensions for financial reporting.</span></span> <span data-ttu-id="53b29-107">順序は、**財務諸表の設定** ページで設定します。</span><span class="sxs-lookup"><span data-stu-id="53b29-107">The order is configured on the **Financial reporting setup** page.</span></span> 
- <span data-ttu-id="53b29-108">データ エンティティ統合書式。</span><span class="sxs-lookup"><span data-stu-id="53b29-108">The data entity integration formats.</span></span> <span data-ttu-id="53b29-109">形式は、**アプリケーションの統合** ページで設定します。</span><span class="sxs-lookup"><span data-stu-id="53b29-109">The formats are configured on the **Integrating applications** page.</span></span> <span data-ttu-id="53b29-110">勘定や財務分析コードを含むトランザクションをインポートするには、データ エンティティの統合形式が必要です。</span><span class="sxs-lookup"><span data-stu-id="53b29-110">Data entity integration formats are required in order to import transactions that contain accounts and financial dimensions.</span></span>

## <a name="financial-reporting"></a><span data-ttu-id="53b29-111">財務諸表</span><span class="sxs-lookup"><span data-stu-id="53b29-111">Financial reporting</span></span>

<span data-ttu-id="53b29-112">**財務諸表の設定** ページには、システムのすべての財務分析コードの一覧があります (**一般会計** > **元帳の設定** > **財務諸表の設定**)。</span><span class="sxs-lookup"><span data-stu-id="53b29-112">The **Financial reporting setup** page has a list of all financial dimensions in the system (**General ledger** > **Ledger setup** > **Financial reporting setup**).</span></span>  

<span data-ttu-id="53b29-113">**財務諸表の設定** ページには、財務諸表でレポートするデータを特定する 2 つのセクションがあります。</span><span class="sxs-lookup"><span data-stu-id="53b29-113">The **Financial reporting setup** page has two sections that determine the data you report on in Financial reporting:</span></span>

- <span data-ttu-id="53b29-114">**分析コード** タブ - 異なる会社がさまざまな分析コードや勘定構造を使用するため、レポートでユーザーがすべての財務分析コードを表示する順序を特定する方法はありません。</span><span class="sxs-lookup"><span data-stu-id="53b29-114">**Dimensions** tab - Because different companies use different dimensions and account structures, there is no way to determine the order in which users want to view all financial dimensions on reports.</span></span> <span data-ttu-id="53b29-115">このページでは、財務分析コードを財務諸表でレポートを作成および表示する際に表示する順序を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="53b29-115">This page allows you set the order in which you want financial dimensions to appear when you build and view a report in Financial reporting.</span></span> 
- <span data-ttu-id="53b29-116">**属性** タブ - **仕入先** および **顧客** をフィルタリングおよびレポート デザインの属性として使用するかどうかを選択できるタブです。</span><span class="sxs-lookup"><span data-stu-id="53b29-116">**Attributes** tab - This tab is where you can select whether you want the ability to use **Vendors** and **Customers** as attributes for filtering and report design.</span></span> <span data-ttu-id="53b29-117">トランザクションを転記する際に、複数の仕入先または顧客を単一伝票に入力しない場合、仕入先および顧客に関するレポートのみが役立ちます。</span><span class="sxs-lookup"><span data-stu-id="53b29-117">Reporting on Vendor and Customer will only be valuable if you do not enter multiple vendors or customers in a single voucher when posting transactions.</span></span> <span data-ttu-id="53b29-118">仕入先または顧客を選択すると、統合にさらに時間が追加されます。</span><span class="sxs-lookup"><span data-stu-id="53b29-118">Choosing Vendor and/or Customer will add additional time to the integration.</span></span>  

## <a name="data-entities"></a><span data-ttu-id="53b29-119">データ エンティティ</span><span class="sxs-lookup"><span data-stu-id="53b29-119">Data entities</span></span>

<span data-ttu-id="53b29-120">**データ エンティティ** タブでは、データをインポートするための財務分析コードの順序を定義します。</span><span class="sxs-lookup"><span data-stu-id="53b29-120">The **Data entities** tab is where you define the order of financial dimensions for importing data.</span></span> <span data-ttu-id="53b29-121">分析コードの形式の順序を設定する方法についてのルールはありません。</span><span class="sxs-lookup"><span data-stu-id="53b29-121">There is no rule about how you should set the order of your dimension formats.</span></span> <span data-ttu-id="53b29-122">これらは、外部システムからソース ファイルを取得し、ソース ファイルをアカウント構造に一致させるために、時間を費やさずにデータをインポートできるように柔軟に設計されています。</span><span class="sxs-lookup"><span data-stu-id="53b29-122">They are designed to be flexible enough that you can take your source files from an external system and import the data without spending time to make the source files match your account structures.</span></span> <span data-ttu-id="53b29-123">特定のセグメントに対して存在しない財務分析コード値をインポートしていないことを確認するために、インポート プロセス中にディメンションの検証が引き続き行われます。</span><span class="sxs-lookup"><span data-stu-id="53b29-123">Dimension validation still occurs during the import process, to verify that you aren't importing financial dimension values that don't exist for a particular segment.</span></span> <span data-ttu-id="53b29-124">ただし、検証範囲外で、勘定構造および分析コード形式は相互に依存しません。</span><span class="sxs-lookup"><span data-stu-id="53b29-124">However, outside validation, account structures and dimension formats are independent of each other.</span></span> <span data-ttu-id="53b29-125">次の 4 つの分析コード形式があります。</span><span class="sxs-lookup"><span data-stu-id="53b29-125">There are four dimension format types:</span></span>

- <span data-ttu-id="53b29-126">**既定の分析コード形式** - この形式タイプは、データ管理と Microsoft Excel の統合の両方で、既定の分析コードをインポートする際に必要です。</span><span class="sxs-lookup"><span data-stu-id="53b29-126">**Default dimension format** – This format type is required when you import default dimensions, through both Data Management and the Microsoft Excel integration.</span></span> <span data-ttu-id="53b29-127">たとえば、顧客勘定または仕入先勘定に関連付けられている財務分析コードをインポートする場合は、既定の分析コードの形式を必要とする場合があります。</span><span class="sxs-lookup"><span data-stu-id="53b29-127">For example, you might require a default dimension format if you're importing the financial dimensions that are associated with a customer or vendor account.</span></span> <span data-ttu-id="53b29-128">主勘定は、この形式には含まれません。</span><span class="sxs-lookup"><span data-stu-id="53b29-128">Main account is not included in this format.</span></span>
- <span data-ttu-id="53b29-129">**元帳分析コード形式** – この形式タイプは、データ管理と Excel 統合の両方で、勘定分析コードをインポートする際に必要です。</span><span class="sxs-lookup"><span data-stu-id="53b29-129">**Ledger dimension format** – This format type is required when you import ledger dimensions, through both Data Management and the Excel integration.</span></span> <span data-ttu-id="53b29-130">元帳分析コード形式は、一般仕訳帳などを介してトランザクションがインポートされるときにいつでも使用されるため、最も一般的な形式です。</span><span class="sxs-lookup"><span data-stu-id="53b29-130">The ledger dimension format is the most common format, because it's used any time that transactions are imported, such as through the general journal.</span></span> <span data-ttu-id="53b29-131">主勘定は、この形式で指定されます。</span><span class="sxs-lookup"><span data-stu-id="53b29-131">The main account is specified on this format.</span></span> <span data-ttu-id="53b29-132">この設定は、環境で使用されるすべての法人および勘定構造に適用されます。</span><span class="sxs-lookup"><span data-stu-id="53b29-132">This setting applies across all legal entities and the account structures used in your environment.</span></span> <span data-ttu-id="53b29-133">設定には、法人全体のトランザクションのインポートに使用できるすべての分析コードの累積セットが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="53b29-133">The setup must include a cumulative set of all dimensions that can be used for transaction import across your legal entities.</span></span> <span data-ttu-id="53b29-134">特定の法人で使用されていない分析コードは、インポート ファイル内で空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="53b29-134">Any dimensions not used for a given legal entity are to be left blank in the import file.</span></span> 
- <span data-ttu-id="53b29-135">**予算登録分析コード形式** - この書式タイプは、データ管理と Excel 統合の両方で、予算作成と予算管理の分析コードをインポートするたびに必要です。</span><span class="sxs-lookup"><span data-stu-id="53b29-135">**Budget register dimension format** – This format type is required any time that you import dimensions for budgeting and budget control, through both Data Management and the Excel integration.</span></span>
- <span data-ttu-id="53b29-136">**予算計画分析コード形式** - この書式タイプは、データ管理と Excel 統合の両方で、予算計画の分析コードをインポートするたびに必要です。</span><span class="sxs-lookup"><span data-stu-id="53b29-136">**Budget planning dimension format** – This format type is required any time that you import dimensions for budget planning, through both Data Management and the Excel integration.</span></span>

> [!NOTE]
> <span data-ttu-id="53b29-137">*分析コード形式のタイプは、会社固有ではありません。この設定はグローバル設定です。*</span><span class="sxs-lookup"><span data-stu-id="53b29-137">*The dimension format types are not company-specific. The setup is a global setup.*</span></span> <span data-ttu-id="53b29-138">必要なだけの数の形式タイプを設定することができますが、同時にアクティブにすることができるのは 1 つの形式タイプのみです。</span><span class="sxs-lookup"><span data-stu-id="53b29-138">You can set up as many of each format type as you need, but only one format type can be active at one time.</span></span> <span data-ttu-id="53b29-139">形式タイプの分析コードが設定されていない場合、インポート時に、エラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="53b29-139">If no dimension format type is set up, you will receive an error when you import.</span></span> <span data-ttu-id="53b29-140">順序が正しくない場合も、エラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="53b29-140">You will also receive errors if the order is incorrect.</span></span> 
 
<span data-ttu-id="53b29-141">分析コード形式がどのように機能するかを示す例をいくつかを見てみましょう。</span><span class="sxs-lookup"><span data-stu-id="53b29-141">Let's look at some examples that show how the dimension formats work.</span></span> <span data-ttu-id="53b29-142">これらの例では、勘定分析コード形式を使用します。</span><span class="sxs-lookup"><span data-stu-id="53b29-142">We will use the ledger dimension format for these examples.</span></span>

### <a name="example-1"></a><span data-ttu-id="53b29-143">例 1</span><span class="sxs-lookup"><span data-stu-id="53b29-143">Example 1</span></span>

<span data-ttu-id="53b29-144">次のファイルをインポートしています。</span><span class="sxs-lookup"><span data-stu-id="53b29-144">You're importing the following file.</span></span>

| <span data-ttu-id="53b29-145">日</span><span class="sxs-lookup"><span data-stu-id="53b29-145">Date</span></span>     | <span data-ttu-id="53b29-146">主勘定および分析コード</span><span class="sxs-lookup"><span data-stu-id="53b29-146">Main account and dimensions</span></span> | <span data-ttu-id="53b29-147">量</span><span class="sxs-lookup"><span data-stu-id="53b29-147">Amount</span></span>   |
|----------|-----------------------------|----------|
| <span data-ttu-id="53b29-148">6/1/2016</span><span class="sxs-lookup"><span data-stu-id="53b29-148">6/1/2016</span></span> | <span data-ttu-id="53b29-149">605140-001-02</span><span class="sxs-lookup"><span data-stu-id="53b29-149">605140-001-02</span></span>               | <span data-ttu-id="53b29-150">$150.00</span><span class="sxs-lookup"><span data-stu-id="53b29-150">$150.00</span></span>  |
| <span data-ttu-id="53b29-151">6/1/2016</span><span class="sxs-lookup"><span data-stu-id="53b29-151">6/1/2016</span></span> | <span data-ttu-id="53b29-152">110110-002-04-ABC</span><span class="sxs-lookup"><span data-stu-id="53b29-152">110110-002-04-ABC</span></span>           | <span data-ttu-id="53b29-153">$-150.00</span><span class="sxs-lookup"><span data-stu-id="53b29-153">$-150.00</span></span> |

<span data-ttu-id="53b29-154">ファイルをインポートするとき、システムは **主勘定と分析コード** 列を確認し、有効な勘定分析コード形式で設定した内容にマップします。</span><span class="sxs-lookup"><span data-stu-id="53b29-154">When you import the file, the system reviews the **Main account and dimensions** column, and maps it to what you've set up in the active ledger dimension format.</span></span> <span data-ttu-id="53b29-155">この例では、有効な勘定分析コードの形式は、次のようになります: **主勘定 - 部門 - コスト センター**</span><span class="sxs-lookup"><span data-stu-id="53b29-155">For this example, the active ledger dimension format is as follows: **Main account - Department - Cost Center**</span></span> 

<span data-ttu-id="53b29-156">システムは、主勘定として **主勘定および分析コード** 列で最初のセグメントを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="53b29-156">The system reads the first segment in the **Main account and dimensions** column as the main account.</span></span> <span data-ttu-id="53b29-157">この例では、そのセグメントは最初の行の 605140 です。</span><span class="sxs-lookup"><span data-stu-id="53b29-157">In this example, that segment is 605140 in the first row.</span></span> <span data-ttu-id="53b29-158">したがって、インポート ファイルからアクティブな元帳の分析コード形式へのマッピングは次のようになります: **主勘定 == 605140** **部門 == 001** **コスト センター == 02**</span><span class="sxs-lookup"><span data-stu-id="53b29-158">Therefore, the mapping from the import file to the active ledger dimension format is as follows: **Main account == 605140** **Department == 001** **Cost Center == 02**</span></span> 

<span data-ttu-id="53b29-159">2 行目を見てみましょう。</span><span class="sxs-lookup"><span data-stu-id="53b29-159">Now let's look at the second row.</span></span> <span data-ttu-id="53b29-160">2 番目の行は、4 番目のセグメント、ABC が含まれます。</span><span class="sxs-lookup"><span data-stu-id="53b29-160">The second row contains a fourth segment, ABC.</span></span> <span data-ttu-id="53b29-161">この例では、ABC は行からインポート中に削除されます: **主勘定 == 110110** **部門 == 002** **コスト センター == 04** **区分 4、ABC はインポートされません。**</span><span class="sxs-lookup"><span data-stu-id="53b29-161">In this example, ABC is dropped during the import from the line: **Main account == 110110** **Department == 002** **Cost Center == 04** **Segment 4, ABC, isn't imported.**</span></span>

### <a name="example-2"></a><span data-ttu-id="53b29-162">例 2</span><span class="sxs-lookup"><span data-stu-id="53b29-162">Example 2</span></span>

<span data-ttu-id="53b29-163">この例では、同じインポート ファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="53b29-163">For this example, we will use the same import file.</span></span>

| <span data-ttu-id="53b29-164">日</span><span class="sxs-lookup"><span data-stu-id="53b29-164">Date</span></span>     | <span data-ttu-id="53b29-165">主勘定および分析コード</span><span class="sxs-lookup"><span data-stu-id="53b29-165">Main account and dimensions</span></span> | <span data-ttu-id="53b29-166">量</span><span class="sxs-lookup"><span data-stu-id="53b29-166">Amount</span></span>   |
|----------|-----------------------------|----------|
| <span data-ttu-id="53b29-167">6/1/2016</span><span class="sxs-lookup"><span data-stu-id="53b29-167">6/1/2016</span></span> | <span data-ttu-id="53b29-168">605140-001-02</span><span class="sxs-lookup"><span data-stu-id="53b29-168">605140-001-02</span></span>               | <span data-ttu-id="53b29-169">$150.00</span><span class="sxs-lookup"><span data-stu-id="53b29-169">$150.00</span></span>  |
| <span data-ttu-id="53b29-170">6/1/2016</span><span class="sxs-lookup"><span data-stu-id="53b29-170">6/1/2016</span></span> | <span data-ttu-id="53b29-171">110110-002-04-ABC</span><span class="sxs-lookup"><span data-stu-id="53b29-171">110110-002-04-ABC</span></span>           | <span data-ttu-id="53b29-172">$-150.00</span><span class="sxs-lookup"><span data-stu-id="53b29-172">$-150.00</span></span> |

<span data-ttu-id="53b29-173">ただし、次の有効な勘定分析コードの形式を使用します: **主勘定 - 部門 - コスト センター - 顧客**</span><span class="sxs-lookup"><span data-stu-id="53b29-173">However, we will use the following active ledger dimension format: **Main account - Department - Cost Center - Customer**</span></span> 

<span data-ttu-id="53b29-174">インポート ファイルの最初の行では、3 つのセグメントのみが定義されるため、空白またはダッシュが顧客セグメントとして想定されます: **主勘定 == 605140** **部門 == 001** **コスト センター == 02** **顧客 == 空白**</span><span class="sxs-lookup"><span data-stu-id="53b29-174">For the first row of the import file, because only three segments are defined, a blank or dash is assumed for the Customer segment: **Main account == 605140** **Department == 001** **Cost Center == 02** **Customer == blank**</span></span> 

<span data-ttu-id="53b29-175">したがって、文字列は次のようになります: **605140-001-02-**</span><span class="sxs-lookup"><span data-stu-id="53b29-175">Therefore, the string looks like this: **605140-001-02-**</span></span> 

<span data-ttu-id="53b29-176">2 番目の行は、インポート ファイルで定義されたとおりにインポートされます: **主勘定 == 110110** **部門 == 002** **コスト センター == 04** **顧客 == ABC**</span><span class="sxs-lookup"><span data-stu-id="53b29-176">The second row is imported as defined in the import file: **Main account == 110110** **Department == 002** **Cost Center == 04** **Customer == ABC**</span></span>

## <a name="additional-resources"></a><span data-ttu-id="53b29-177">追加リソース</span><span class="sxs-lookup"><span data-stu-id="53b29-177">Additional resources</span></span>

[<span data-ttu-id="53b29-178">Excel テンプレートへの分析コードの追加</span><span class="sxs-lookup"><span data-stu-id="53b29-178">Add dimensions to Excel templates</span></span>](dimensions-overview.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
