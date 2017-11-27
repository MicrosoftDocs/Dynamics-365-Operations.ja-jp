---
title: "一般仕訳帳の処理"
description: "この記事は、Microsoft Dynamics 365 for Finance and Operations で、一般仕訳帳の処理を容易にすることができ、正確なデータがキャプチャされ内部コントロールが悪影響を受けていないことを保証する手助けとなる Enterprise エディションの機能について説明します。"
author: twheeloc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 76386f7ab8033075f9db4cadc697f3a2a997163e
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="general-journal-processing"></a><span data-ttu-id="fa3d3-103">一般仕訳帳の処理</span><span class="sxs-lookup"><span data-stu-id="fa3d3-103">General journal processing</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="fa3d3-104">この記事は、Microsoft Dynamics 365 for Finance and Operations で、一般仕訳帳の処理を容易にすることができ、正確なデータがキャプチャされ内部コントロールが悪影響を受けていないことを保証する手助けとなる Enterprise エディションの機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="fa3d3-104">This articles describes capabilities in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition that can help make general journal processing easier, and that can also help guarantee that correct data is captured and internal control isn't compromised.</span></span>  

<span data-ttu-id="fa3d3-105">仕訳帳名</span><span class="sxs-lookup"><span data-stu-id="fa3d3-105">Journal names</span></span>

<span data-ttu-id="fa3d3-106">設定する重要な分野の 1 つは、仕訳帳名です。</span><span class="sxs-lookup"><span data-stu-id="fa3d3-106">One of the most important areas to set up is journal names.</span></span> <span data-ttu-id="fa3d3-107">会社間、見越計上調整、エラーの修正など、目的ごとに特定の仕訳帳名を定義することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="fa3d3-107">It's a good idea to define specific journal names for each purpose, such as intercompany, accrual adjustment, and error correction.</span></span> <span data-ttu-id="fa3d3-108">目的ごとにデータ入力を簡単かつ安全にするために、それぞれの仕訳帳名をカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="fa3d3-108">You can tailor each journal name to help make data entry for each purpose easy and secure.</span></span> 

<span data-ttu-id="fa3d3-109">[**仕訳帳名**] ページで、次の要素を設定できます :</span><span class="sxs-lookup"><span data-stu-id="fa3d3-109">On the **Journal names** page, you can set up the following elements:</span></span>

-   <span data-ttu-id="fa3d3-110">[**ワークフローの承認**] ー 内部コントロールを向上するために、合計借方金額などの基準に基づいて、確認および承認ステップの物質能力制限を設定する仕訳帳ワークフローを定義します。</span><span class="sxs-lookup"><span data-stu-id="fa3d3-110">**Workflow approval** – To increase internal control, define journal workflows that establish materiality limits for review and approval steps, based on criteria such as total debit amount.</span></span> <span data-ttu-id="fa3d3-111">一般仕訳帳のワークフローを [**総勘定元帳ワークフロー**] ページに設定します。</span><span class="sxs-lookup"><span data-stu-id="fa3d3-111">You set up workflows for the general journals on the** General ledger workflows** page.</span></span>
-   <span data-ttu-id="fa3d3-112">[**既定値**] – 相手勘定、通貨、財務分析コードの既定値を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa3d3-112">**Default values** – Select default values for offset accounts, currency, and financial dimensions.</span></span>
-   <span data-ttu-id="fa3d3-113">[**仕訳帳コントロール**] – 会社と勘定タイプの制限、および区分値を設定できます。</span><span class="sxs-lookup"><span data-stu-id="fa3d3-113">**Journal control** – You can set up restrictions on the company and account type, and also the segment values.</span></span> 

<span data-ttu-id="fa3d3-114">**例**</span><span class="sxs-lookup"><span data-stu-id="fa3d3-114">**Examples**</span></span>

<span data-ttu-id="fa3d3-115">仕訳帳名は調整のためのみにに使用されます。</span><span class="sxs-lookup"><span data-stu-id="fa3d3-115">A journal name can be used only for adjustments.</span></span> <span data-ttu-id="fa3d3-116">この場合、すべての会社で [**元帳**] 勘定タイプのみが有効であるように指定できます。</span><span class="sxs-lookup"><span data-stu-id="fa3d3-116">In this case, you can specify that only the **Ledger** account type is valid across all companies.</span></span> <span data-ttu-id="fa3d3-117">[![仕訳帳コントロール勘定タイプ](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span><span class="sxs-lookup"><span data-stu-id="fa3d3-117">[![Journal control account types](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span></span>

<span data-ttu-id="fa3d3-118">仕訳帳名は、特定の区分のみまたは主勘定の範囲に対して使用できます。</span><span class="sxs-lookup"><span data-stu-id="fa3d3-118">A journal name can be used only for a specific segment or for a range for main accounts.</span></span> <span data-ttu-id="fa3d3-119">[![仕訳帳コントロール区分](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span><span class="sxs-lookup"><span data-stu-id="fa3d3-119">[![Journal control segment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span></span>

<span data-ttu-id="fa3d3-120">[**自動取消**] オプションは、一般仕訳帳で使用できます。</span><span class="sxs-lookup"><span data-stu-id="fa3d3-120">The **Automatic reversal** option is available in general journals.</span></span> <span data-ttu-id="fa3d3-121">たとえば、次の図に示すように、実際のドキュメントがまだ処理されていない見越計上の調整が行われます。</span><span class="sxs-lookup"><span data-stu-id="fa3d3-121">For example, you have an accrual adjustment where the actual document hasn't yet been processed, as shown in the following illustration.</span></span>
<span data-ttu-id="fa3d3-122">[![一般仕訳帳の取り消し](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span><span class="sxs-lookup"><span data-stu-id="fa3d3-122">[![General journal reversing](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span></span> 

<span data-ttu-id="fa3d3-123">仕訳帳入力のための Microsoft Excel アドインは、自動化の追加のレベルを提供し、データ入力をより簡単にします。</span><span class="sxs-lookup"><span data-stu-id="fa3d3-123">The Microsoft Excel add-in for journal entry provides an additional level of automation and makes data entry easier.</span></span> <span data-ttu-id="fa3d3-124">[**Excel で明細行を開く**] アクションは、[**一般仕訳帳**] および [**仕訳伝票**] ページで使用できます。</span><span class="sxs-lookup"><span data-stu-id="fa3d3-124">The **Open lines in Excel** action is available on the **General journal** and **Journal voucher** pages.</span></span> 

<span data-ttu-id="fa3d3-125">[**定期処理仕訳帳**] ページで、繰返しの仕訳帳を仕訳処理の自動化に設定できます。</span><span class="sxs-lookup"><span data-stu-id="fa3d3-125">On the **Periodic journals** page, you can set up recurring journals to automate journal processing.</span></span> 

<span data-ttu-id="fa3d3-126">伝票テンプレートはいつでも使用できます。</span><span class="sxs-lookup"><span data-stu-id="fa3d3-126">You can use voucher templates at any time.</span></span> <span data-ttu-id="fa3d3-127">[**一般仕訳帳**] ページでは、[**保存**] および [**伝票テンプレートの選択**] アクションは、伝票明細行の [**機能**] の **仕訳伝票** ページにあります。</span><span class="sxs-lookup"><span data-stu-id="fa3d3-127">On the **General journals** page, the **Save** and **Select voucher template** actions are found on the **Journal voucher** page, under **Functions** for the voucher lines.</span></span>

## <a name="related-setup"></a><span data-ttu-id="fa3d3-128">関連する設定</span><span class="sxs-lookup"><span data-stu-id="fa3d3-128">Related setup</span></span>
<span data-ttu-id="fa3d3-129">次の設定は、一般仕訳帳に特定していませんが、データ入力が正しいデータで簡単なことを保障します。</span><span class="sxs-lookup"><span data-stu-id="fa3d3-129">The following setup isn't specific to general journals, but will help guarantee that data entry is correct data and easy.</span></span>

### <a name="main-account"></a><span data-ttu-id="fa3d3-130">主勘定</span><span class="sxs-lookup"><span data-stu-id="fa3d3-130">Main account</span></span>

<span data-ttu-id="fa3d3-131">主勘定の設定には、一般仕訳帳の処理にさまざまなオプションが提供されます :</span><span class="sxs-lookup"><span data-stu-id="fa3d3-131">The main account setup provides many options for general journal processing:</span></span>

-   <span data-ttu-id="fa3d3-132">[**DC/CRの条件**] ー 主勘定が借方もしくは貸方トランザクションに限定される場合はこのオプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="fa3d3-132">**DC/CR requirement** – Use this option if a main account is limited to debit or credit transactions.</span></span> <span data-ttu-id="fa3d3-133">設定は、仕訳帳を検証するか、または転記したときに確認されます。</span><span class="sxs-lookup"><span data-stu-id="fa3d3-133">The setup is verified when a journal is validated or posted.</span></span>
-   <span data-ttu-id="fa3d3-134">**既定の相手勘定**</span><span class="sxs-lookup"><span data-stu-id="fa3d3-134">**Default offset account**</span></span>
-   <span data-ttu-id="fa3d3-135">[**中断**] – は、すべての会社または特定の会社や法人のデータ入力用の主勘定を中断します。</span><span class="sxs-lookup"><span data-stu-id="fa3d3-135">**Suspended** – Suspend a main account for data entry across all companies or for a specific company/legal entities.</span></span>
-   <span data-ttu-id="fa3d3-136">**手動入力を許可しない** – ユーザーが仕訳帳の勘定に手動で値を入力することを防ぎます。</span><span class="sxs-lookup"><span data-stu-id="fa3d3-136">**Do not allow manual entry** – Prevent users from manually entering a value for the account in journals.</span></span>
-   <span data-ttu-id="fa3d3-137">[**既定 / 通貨の検証**]</span><span class="sxs-lookup"><span data-stu-id="fa3d3-137">**Default/Validate currency**</span></span>
-   <span data-ttu-id="fa3d3-138">[**法人の上書き**] – この設定は、定義された会社や法人固有のものです :</span><span class="sxs-lookup"><span data-stu-id="fa3d3-138">**Legal entity override** – This setup is specific to the defined company/legal entity:</span></span>
    -   <span data-ttu-id="fa3d3-139">[**規定 / 売上税の検証**]</span><span class="sxs-lookup"><span data-stu-id="fa3d3-139">**Default/Validate sales tax**</span></span>
    -   <span data-ttu-id="fa3d3-140">[**既定の分析コード**] ー [**固定なし**] または [**固定値**]</span><span class="sxs-lookup"><span data-stu-id="fa3d3-140">**Default dimension** – **Not fixed** or **Fixed value**.</span></span> <span data-ttu-id="fa3d3-141">[**固定値**] この主勘定のすべての転記が、常に [**固定**] として設定されているどの分析コード値でも使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="fa3d3-141">**Fixed value** will help guarantee that all postings for this main account always use any dimension value that is set up as **Fixed**.</span></span>
-   <span data-ttu-id="fa3d3-142">**転記検証**</span><span class="sxs-lookup"><span data-stu-id="fa3d3-142">**Posting validation**</span></span>
    -   <span data-ttu-id="fa3d3-143">[**ユーザーの検証**] – このオプションは、主勘定に転記することが許可されるユーザーを管理します。</span><span class="sxs-lookup"><span data-stu-id="fa3d3-143">**User validation** – This option controls which users are allowed to post to a main account.</span></span>
    -   <span data-ttu-id="fa3d3-144">[**転記タイプの検証**] – このオプションは、主勘定に対して使用できる転記タイプを管理します。</span><span class="sxs-lookup"><span data-stu-id="fa3d3-144">**Posting type validation** – This option controls which posting types are allowed for a main account.</span></span>

### <a name="accounting-structures-and-advanced-rules-structures"></a><span data-ttu-id="fa3d3-145">勘定構造および詳細ルール構造</span><span class="sxs-lookup"><span data-stu-id="fa3d3-145">Accounting structures and advanced rules structures</span></span>

<span data-ttu-id="fa3d3-146">勘定構造および詳細ルールの構造は、財務レポートに必要とされるデータおよびパフォーマンスの追跡が、一般仕訳帳の処理とドキュメンテーションの間にキャプチャされるようにするために非常に重要です。</span><span class="sxs-lookup"><span data-stu-id="fa3d3-146">Accounting structures and advanced rules structures are extremely important for guaranteeing that the data that is required for financial reporting and performance tracking is captured during general journal processing and any documentation.</span></span> <span data-ttu-id="fa3d3-147">勘定構造および詳細ルール構造により、データ入力経験のカスタマイズが可能になります。</span><span class="sxs-lookup"><span data-stu-id="fa3d3-147">Accounting structures and advanced rules structures let you tailor the data entry experience.</span></span> <span data-ttu-id="fa3d3-148">それぞれの状況に該当する財務分析コードにのみデータ入力を許可し、必須および正確なデータが常にキャプチャされるという条件を適用できます。</span><span class="sxs-lookup"><span data-stu-id="fa3d3-148">You can allow data entry only for financial dimensions that are relevant in each situation, and can also enforce the requirement that mandatory and correct data always be captured.</span></span>

<span data-ttu-id="fa3d3-149">詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="fa3d3-149">For more information, see the following topics:</span></span>
- <span data-ttu-id="fa3d3-150">[計画: 勘定科目表](plan-chart-of-accounts.md)。</span><span class="sxs-lookup"><span data-stu-id="fa3d3-150">[Planning: Chart of accounts](plan-chart-of-accounts.md).</span></span> 
- [<span data-ttu-id="fa3d3-151">仕訳帳の詳細なルールの作成</span><span class="sxs-lookup"><span data-stu-id="fa3d3-151">Create advanced rules for journals</span></span>](tasks/create-advanced-rules-journals.md)
- [<span data-ttu-id="fa3d3-152">テンプレートを使用した仕訳入力の作成</span><span class="sxs-lookup"><span data-stu-id="fa3d3-152">Create a journal entry using a template</span></span>](tasks/create-journal-entry-template.md)
- [<span data-ttu-id="fa3d3-153">仕訳帳の作成および検証</span><span class="sxs-lookup"><span data-stu-id="fa3d3-153">Create and validate journals</span></span>](tasks/create-validate-journals.md)
- [<span data-ttu-id="fa3d3-154">定期処理仕訳帳の転記</span><span class="sxs-lookup"><span data-stu-id="fa3d3-154">Post periodic journals</span></span>](tasks/post-periodic-journals.md)
- [<span data-ttu-id="fa3d3-155">元帳配賦仕訳帳の処理</span><span class="sxs-lookup"><span data-stu-id="fa3d3-155">Process ledger allocation journal</span></span>](tasks/process-ledger-allocation-journal.md)



