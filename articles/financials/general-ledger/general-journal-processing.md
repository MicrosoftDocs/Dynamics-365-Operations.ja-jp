---
title: "一般仕訳帳の処理"
description: "このトピックでは、一般仕訳帳の処理を容易にすることができ、正確なデータがキャプチャされ、内部コントロールが悪影響を受けていないことを確認するのに役立つ Microsoft Dynamics 365 for Finance and Operations の機能について説明します。"
author: ShylaThompson
manager: AnnBe
ms.date: 09/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cf744bc41ffcca6d029da5dd2031ada607a0109b
ms.openlocfilehash: e77aafafed5c972a6ad8c064107306d3ebde0b79
ms.contentlocale: ja-jp
ms.lasthandoff: 10/16/2018

---

# <a name="general-journal-processing"></a><span data-ttu-id="8a61d-103">一般仕訳帳の処理</span><span class="sxs-lookup"><span data-stu-id="8a61d-103">General journal processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8a61d-104">このトピックでは、一般仕訳帳の処理を容易にすることができ、正確なデータがキャプチャされ、内部コントロールが悪影響を受けていないことを確認するのに役立つ Microsoft Dynamics 365 for Finance and Operations の機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="8a61d-104">This topic describes capabilities in Microsoft Dynamics 365 for Finance and Operations that can help make general journal processing easier, and that can also help ensure that correct data is captured and internal control isn't compromised.</span></span>  

## <a name="journal-names"></a><span data-ttu-id="8a61d-105">仕訳帳名</span><span class="sxs-lookup"><span data-stu-id="8a61d-105">Journal names</span></span>

<span data-ttu-id="8a61d-106">設定する重要な分野の 1 つは、仕訳帳名です。</span><span class="sxs-lookup"><span data-stu-id="8a61d-106">One of the most important areas to set up is journal names.</span></span> <span data-ttu-id="8a61d-107">会社間、見越計上調整、エラーの修正など、目的ごとに特定の仕訳帳名を定義することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="8a61d-107">It's a good idea to define specific journal names for each purpose, such as intercompany, accrual adjustment, and error correction.</span></span> <span data-ttu-id="8a61d-108">目的ごとにデータ入力を簡単かつ安全にするために、それぞれの仕訳帳名をカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="8a61d-108">You can tailor each journal name to help make data entry for each purpose easy and secure.</span></span> 

<span data-ttu-id="8a61d-109">**仕訳帳名** ページで、次の要素を設定できます :</span><span class="sxs-lookup"><span data-stu-id="8a61d-109">On the **Journal names** page, you can set up the following elements:</span></span>

-   <span data-ttu-id="8a61d-110">**ワークフローの承認** ー 内部コントロールを向上するために、合計借方金額などの基準に基づいて、確認および承認ステップの物質能力制限を設定する仕訳帳ワークフローを定義します。</span><span class="sxs-lookup"><span data-stu-id="8a61d-110">**Workflow approval** – To increase internal control, define journal workflows that establish materiality limits for review and approval steps, based on criteria such as total debit amount.</span></span> <span data-ttu-id="8a61d-111">一般仕訳帳のワークフローを **総勘定元帳ワークフロー** ページに設定します。</span><span class="sxs-lookup"><span data-stu-id="8a61d-111">You set up workflows for the general journals on the **General ledger workflows** page.</span></span>
-   <span data-ttu-id="8a61d-112">**既定値** – 相手勘定、通貨、財務分析コードの既定値を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a61d-112">**Default values** – Select default values for offset accounts, currency, and financial dimensions.</span></span>
-   <span data-ttu-id="8a61d-113">**仕訳帳コントロール** – 会社と勘定タイプの制限、および区分値を設定できます。</span><span class="sxs-lookup"><span data-stu-id="8a61d-113">**Journal control** – You can set up restrictions on the company and account type, and also the segment values.</span></span> 

<span data-ttu-id="8a61d-114">**例**</span><span class="sxs-lookup"><span data-stu-id="8a61d-114">**Examples**</span></span>

<span data-ttu-id="8a61d-115">仕訳帳名は調整のためのみにに使用されます。</span><span class="sxs-lookup"><span data-stu-id="8a61d-115">A journal name can be used only for adjustments.</span></span> <span data-ttu-id="8a61d-116">この場合、すべての会社で **元帳** 勘定タイプのみが有効であるように指定できます。</span><span class="sxs-lookup"><span data-stu-id="8a61d-116">In this case, you can specify that only the **Ledger** account type is valid across all companies.</span></span> 

<span data-ttu-id="8a61d-117">[![仕訳帳コントロール勘定タイプ](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span><span class="sxs-lookup"><span data-stu-id="8a61d-117">[![Journal control account types](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span></span>

<span data-ttu-id="8a61d-118">仕訳帳名は、特定の区分のみまたは主勘定の範囲に対して使用できます。</span><span class="sxs-lookup"><span data-stu-id="8a61d-118">A journal name can be used only for a specific segment or for a range for main accounts.</span></span> 

<span data-ttu-id="8a61d-119">[![仕訳帳コントロール区分](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span><span class="sxs-lookup"><span data-stu-id="8a61d-119">[![Journal control segment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span></span>

<span data-ttu-id="8a61d-120">**自動取消** オプションは、一般仕訳帳で使用できます。</span><span class="sxs-lookup"><span data-stu-id="8a61d-120">The **Automatic reversal** option is available in general journals.</span></span> <span data-ttu-id="8a61d-121">たとえば、次の図に示すように、実際のドキュメントがまだ処理されていない見越計上の調整が行われます。</span><span class="sxs-lookup"><span data-stu-id="8a61d-121">For example, you have an accrual adjustment where the actual document hasn't yet been processed, as shown in the following illustration.</span></span>
<span data-ttu-id="8a61d-122">[![一般仕訳帳の取り消し](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span><span class="sxs-lookup"><span data-stu-id="8a61d-122">[![General journal reversing](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span></span> 

<span data-ttu-id="8a61d-123">仕訳帳入力のための Microsoft Excel アドインは、自動化の追加のレベルを提供し、データ入力をより簡単にします。</span><span class="sxs-lookup"><span data-stu-id="8a61d-123">The Microsoft Excel add-in for journal entry provides an additional level of automation and makes data entry easier.</span></span> <span data-ttu-id="8a61d-124">**Excel で明細行を開く** アクションは、**一般仕訳帳** および **仕訳伝票** ページで使用できます。</span><span class="sxs-lookup"><span data-stu-id="8a61d-124">The **Open lines in Excel** action is available on the **General journal** and **Journal voucher** pages.</span></span> 

<span data-ttu-id="8a61d-125">**定期処理仕訳帳** ページで、繰返しの仕訳帳を仕訳処理の自動化に設定できます。</span><span class="sxs-lookup"><span data-stu-id="8a61d-125">On the **Periodic journals** page, you can set up recurring journals to automate journal processing.</span></span> 

<span data-ttu-id="8a61d-126">伝票テンプレートはいつでも使用できます。</span><span class="sxs-lookup"><span data-stu-id="8a61d-126">You can use voucher templates at any time.</span></span> <span data-ttu-id="8a61d-127">**一般仕訳帳** ページでは、**保存** および **伝票テンプレートの選択** アクションは、伝票明細行の **機能** の **仕訳伝票** ページにあります。</span><span class="sxs-lookup"><span data-stu-id="8a61d-127">On the **General journals** page, the **Save** and **Select voucher template** actions are found on the **Journal voucher** page, under **Functions** for the voucher lines.</span></span>

## <a name="related-setup"></a><span data-ttu-id="8a61d-128">関連する設定</span><span class="sxs-lookup"><span data-stu-id="8a61d-128">Related setup</span></span>
<span data-ttu-id="8a61d-129">次の設定は、一般仕訳帳に固有のものではありませんが、データ入力が正しいデータで簡単であることを確認するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="8a61d-129">The following setup isn't specific to general journals, but will help ensure that data entry is correct data and easy.</span></span>

### <a name="main-account"></a><span data-ttu-id="8a61d-130">主勘定</span><span class="sxs-lookup"><span data-stu-id="8a61d-130">Main account</span></span>

<span data-ttu-id="8a61d-131">主勘定の設定には、一般仕訳帳の処理にさまざまなオプションが提供されます :</span><span class="sxs-lookup"><span data-stu-id="8a61d-131">The main account setup provides many options for general journal processing:</span></span>

-   <span data-ttu-id="8a61d-132">**DC/CRの条件** ー 主勘定が借方もしくは貸方トランザクションに限定される場合はこのオプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="8a61d-132">**DC/CR requirement** – Use this option if a main account is limited to debit or credit transactions.</span></span> <span data-ttu-id="8a61d-133">設定は、仕訳帳を検証するか、または転記したときに確認されます。</span><span class="sxs-lookup"><span data-stu-id="8a61d-133">The setup is verified when a journal is validated or posted.</span></span>

-   <span data-ttu-id="8a61d-134">**既定の相手勘定**</span><span class="sxs-lookup"><span data-stu-id="8a61d-134">**Default offset account**</span></span>
-   <span data-ttu-id="8a61d-135">**中断** – は、すべての会社または特定の会社や法人のデータ入力用の主勘定を中断します。</span><span class="sxs-lookup"><span data-stu-id="8a61d-135">**Suspended** – Suspend a main account for data entry across all companies or for a specific company/legal entity.</span></span>
-   <span data-ttu-id="8a61d-136">**手動入力を許可しない** – ユーザーが仕訳帳の勘定に手動で値を入力することを防ぎます。</span><span class="sxs-lookup"><span data-stu-id="8a61d-136">**Do not allow manual entry** – Prevent users from manually entering a value for the account in journals.</span></span>
-   <span data-ttu-id="8a61d-137">**既定 / 通貨の検証**</span><span class="sxs-lookup"><span data-stu-id="8a61d-137">**Default/Validate currency**</span></span>
-   <span data-ttu-id="8a61d-138">**法人の上書き** – この設定は、定義された会社や法人固有のものです :</span><span class="sxs-lookup"><span data-stu-id="8a61d-138">**Legal entity override** – This setup is specific to the defined company/legal entity:</span></span>
    -   <span data-ttu-id="8a61d-139">**規定 / 売上税の検証**</span><span class="sxs-lookup"><span data-stu-id="8a61d-139">**Default/Validate sales tax**</span></span>
    -   <span data-ttu-id="8a61d-140">**既定の分析コード** ー **固定なし** または **固定値**</span><span class="sxs-lookup"><span data-stu-id="8a61d-140">**Default dimension** – **Not fixed** or **Fixed value**.</span></span> <span data-ttu-id="8a61d-141">**固定値**はこの主勘定のすべての転記が、常に**固定**として設定されているどの分析コード値でも使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="8a61d-141">**Fixed value** will help ensure that all postings for this main account always use any dimension value that is set up as **Fixed**.</span></span>
-   <span data-ttu-id="8a61d-142">**転記検証**</span><span class="sxs-lookup"><span data-stu-id="8a61d-142">**Posting validation**</span></span>
    -   <span data-ttu-id="8a61d-143">**ユーザーの検証** – このオプションは、主勘定に転記することが許可されるユーザーを管理します。</span><span class="sxs-lookup"><span data-stu-id="8a61d-143">**User validation** – This option controls which users are allowed to post to a main account.</span></span>
    -   <span data-ttu-id="8a61d-144">**転記タイプの検証** – このオプションは、主勘定に対して使用できる転記タイプを管理します。</span><span class="sxs-lookup"><span data-stu-id="8a61d-144">**Posting type validation** – This option controls which posting types are allowed for a main account.</span></span>

### <a name="accounting-structures-and-advanced-rules-structures"></a><span data-ttu-id="8a61d-145">勘定構造および詳細ルール構造</span><span class="sxs-lookup"><span data-stu-id="8a61d-145">Accounting structures and advanced rules structures</span></span>

<span data-ttu-id="8a61d-146">勘定構造および詳細ルールの構造は、財務報告に必要とされるデータおよびパフォーマンスの追跡が、一般仕訳帳の処理とドキュメンテーションの間にキャプチャされることを確認するために非常に重要です。</span><span class="sxs-lookup"><span data-stu-id="8a61d-146">Accounting structures and advanced rules structures are extremely important for ensuring that the data that is required for financial reporting and performance tracking is captured during general journal processing and any documentation.</span></span> <span data-ttu-id="8a61d-147">勘定構造および詳細ルール構造により、データ入力経験のカスタマイズが可能になります。</span><span class="sxs-lookup"><span data-stu-id="8a61d-147">Accounting structures and advanced rules structures let you tailor the data entry experience.</span></span> <span data-ttu-id="8a61d-148">それぞれの状況に該当する財務分析コードに対してのみデータ入力を許可し、必要かつ正確なデータを常にキャプチャするという要件を適用することもできます。</span><span class="sxs-lookup"><span data-stu-id="8a61d-148">You can allow data entry only for financial dimensions that are relevant in each situation, and can also enforce the requirement that required and accurate data always be captured.</span></span>

<span data-ttu-id="8a61d-149">詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8a61d-149">For more information, see the following topics:</span></span>
- <span data-ttu-id="8a61d-150">[計画: 勘定科目表](plan-chart-of-accounts.md)。</span><span class="sxs-lookup"><span data-stu-id="8a61d-150">[Planning: Chart of accounts](plan-chart-of-accounts.md).</span></span> 
- [<span data-ttu-id="8a61d-151">仕訳帳の詳細なルールの作成</span><span class="sxs-lookup"><span data-stu-id="8a61d-151">Create advanced rules for journals</span></span>](tasks/create-advanced-rules-journals.md)
- [<span data-ttu-id="8a61d-152">テンプレートを使用した仕訳入力の作成</span><span class="sxs-lookup"><span data-stu-id="8a61d-152">Create a journal entry using a template</span></span>](tasks/create-journal-entry-template.md)
- [<span data-ttu-id="8a61d-153">仕訳帳の作成および検証</span><span class="sxs-lookup"><span data-stu-id="8a61d-153">Create and validate journals</span></span>](tasks/create-validate-journals.md)
- [<span data-ttu-id="8a61d-154">定期処理仕訳帳の転記</span><span class="sxs-lookup"><span data-stu-id="8a61d-154">Post periodic journals</span></span>](tasks/post-periodic-journals.md)
- [<span data-ttu-id="8a61d-155">元帳配賦仕訳帳の処理</span><span class="sxs-lookup"><span data-stu-id="8a61d-155">Process ledger allocation journal</span></span>](tasks/process-ledger-allocation-journal.md)

## <a name="simulate-posting"></a><span data-ttu-id="8a61d-156">転記をシミュレーション</span><span class="sxs-lookup"><span data-stu-id="8a61d-156">Simulate posting</span></span>
<span data-ttu-id="8a61d-157">**検証**メニューで、ほとんどの仕訳帳の**シミュレート転記**を検索できます。</span><span class="sxs-lookup"><span data-stu-id="8a61d-157">You can find **Simulate posting** on the **Validate** menu for most journals.</span></span> <span data-ttu-id="8a61d-158">**検証**機能を使用して仕訳帳を検証すると、システムは特定のエラー条件について仕訳帳をテストします。</span><span class="sxs-lookup"><span data-stu-id="8a61d-158">When you validate a journal using the **Validate** function, the system tests the journal for specific error conditions.</span></span> <span data-ttu-id="8a61d-159">**シミュレート転記**を使用すると、転記中に実行されるすべてのプロセスが実際に転記されずに実行されます。</span><span class="sxs-lookup"><span data-stu-id="8a61d-159">If you use the **Simulate posting** function, the system runs all of the same processes that are run during posting without actually posting the journal.</span></span> <span data-ttu-id="8a61d-160">その後、表示される転記メッセージの確認、エラーの修正を行い、**転記**メニューをクリックして、仕訳帳を転記します。</span><span class="sxs-lookup"><span data-stu-id="8a61d-160">You can then review the posting messages that are displayed, fix any errors that you find, and then click the **Post** menu to post the journal.</span></span> 

<span data-ttu-id="8a61d-161">**シミュレート転記**はバッチ処理では使用できません。</span><span class="sxs-lookup"><span data-stu-id="8a61d-161">**Simulate posting** is not available for batch processing.</span></span> <span data-ttu-id="8a61d-162">ただし、バッチの転記をシミュレートするために使用可能なコードがあり、開発者はコードを拡張してその機能を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="8a61d-162">However, there is code available to simulate posting in batch and developers can extend the code to add that functionality.</span></span>  

