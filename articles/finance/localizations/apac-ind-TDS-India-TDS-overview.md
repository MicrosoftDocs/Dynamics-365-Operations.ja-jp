---
title: インドの源泉徴収 (TDS) 概要
description: このトピックでは、源泉徴収 (TDS) で控除されたインドの税金に関する詳細情報を提供します。 TDS のドキュメントには、この機能の特徴が含まれています。
author: kailiang
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 28ee843036e11bd37b97a065ce53d2eb860c79d9
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023401"
---
# <a name="indian-tax-deducted-at-source-tds-overview"></a><span data-ttu-id="cdbe2-104">インドの源泉徴収 (TDS) 概要</span><span class="sxs-lookup"><span data-stu-id="cdbe2-104">Indian Tax Deducted at Source (TDS) overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cdbe2-105">このトピックでは、源泉徴収 (TDS) で控除されたインドの税金に関する詳細情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-105">This topic provides detailed information about Indian Tax Deducted at Source (TDS).</span></span>

<span data-ttu-id="cdbe2-106">TDS のドキュメントには、この機能の特徴が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-106">The TDS documentation covers the functionality of this capability.</span></span> <span data-ttu-id="cdbe2-107">また、TDS の基本設定の実行、トランザクションに関する TDS の計算、TDS 決済プロセスの完了、TDS 証明書番号の記録方法、また TDS の照会、TDS 明細書、TDS 証明書の生成方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-107">It also explains how to do the basic setup for TDS, calculate TDS on transactions, complete the TDS settlement process, record TDS certificate numbers, and generate TDS inquiries, TDS statements, and TDS certificates.</span></span> <span data-ttu-id="cdbe2-108">ドキュメントには次のトピックが含まれます:</span><span class="sxs-lookup"><span data-stu-id="cdbe2-108">The documentation includes the following topics:</span></span>

- [<span data-ttu-id="cdbe2-109">TDS の基本設定</span><span class="sxs-lookup"><span data-stu-id="cdbe2-109">Basic setup for TDS</span></span>](apac-ind-TDS-TDS-ledger-accounts-setup.md)
- [<span data-ttu-id="cdbe2-110">TDS の計算に使用する式デザイナーとしきい値制限機能</span><span class="sxs-lookup"><span data-stu-id="cdbe2-110">Formula designer and threshold limit functionality used for TDS calculation</span></span>](apac-ind-TDS-Formula-designer.md)
- [<span data-ttu-id="cdbe2-111">請求書、支払、支払手形、会社間トランザクションに関する TDS の計算</span><span class="sxs-lookup"><span data-stu-id="cdbe2-111">Calculation of TDS on invoices, payments, promissory notes, and intercompany transactions</span></span>](apac-ind-TDS-Calculate-TDS-on-invoices-using-journals.md)
- [<span data-ttu-id="cdbe2-112">定期的な TDS 決済プロセスと TDS 権限を持つ仕入先への TDS 金額の決済</span><span class="sxs-lookup"><span data-stu-id="cdbe2-112">Periodic TDS settlement process and settlement of TDS amounts to TDS authority vendors</span></span>](apac-ind-TDS-Run-the-periodic-TDS-settlement-process.md)
- [<span data-ttu-id="cdbe2-113">TDS 証明書番号と日付の記録と更新</span><span class="sxs-lookup"><span data-stu-id="cdbe2-113">Recording and updating TDS certificate numbers and dates</span></span>](apac-ind-TDS-Record-TDS-concession-certificate-numbers.md)

## <a name="introduction-to-tds"></a><span data-ttu-id="cdbe2-114">TDS の概要</span><span class="sxs-lookup"><span data-stu-id="cdbe2-114">Introduction to TDS</span></span>

<span data-ttu-id="cdbe2-115">1961年に制定された所得税法では、所得税はサービスを受ける側が、前払いまたはクレジットの計上のいずれか早い方の時点で源泉徴収されると定められています。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-115">Per the Income tax Act, 1961, income tax is deducted at the source by the receiver of the service at the time of advance payment or accounting of credit, whichever occurs first.</span></span> <span data-ttu-id="cdbe2-116">支払を行う担当者は、税額を控除し、サービスの提供者に正味残高のみを支払う必要があります。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-116">The person who makes the payment must deduct the tax amount and pay only the net balance to the provider of the service.</span></span> <span data-ttu-id="cdbe2-117">TDSは、政府が指定したサービスに対して適用され、政府が指定した期間のレートを使用して税金を控除します。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-117">TDS is applied on services that the government specifies, and the tax is deducted by using the rates that the government specifies for a period.</span></span> <span data-ttu-id="cdbe2-118">控除率は、支払いを受ける側、またはサービスを提供する側の企業の状況に応じて決定されます。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-118">The rate of deduction is based on the status of the entity that receives the payment or provides the service.</span></span> <span data-ttu-id="cdbe2-119">状態には、**個人**、**ヒンドゥ教徒同族会社** (**HUF**)、**会社**、**合資会社**、**個人関連** (**AOP**)、**個人の団体** (**BOI**)、および **地方自治体** が含まれます。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-119">Statuses include **Individual**, **Hindu Undivided Family** (**HUF**), **Company**, **Firm**, **Association of Persons** (**AOP**), **Body of Individuals** (**BOI**), and **Local authority**.</span></span>

<span data-ttu-id="cdbe2-120">以下のセクションでは、インド政府が指定した TDS が適用されるサービスを紹介します。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-120">The following sections list the services that TDS is applied on, as specified by the Government of India.</span></span>

<span data-ttu-id="cdbe2-121">**居住者**</span><span class="sxs-lookup"><span data-stu-id="cdbe2-121">**Residents**</span></span>

- <span data-ttu-id="cdbe2-122">給与からの収入 (セクション 192 に基づく)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-122">Income from salaries (Under section 192)</span></span>
- <span data-ttu-id="cdbe2-123">証券の利息からの収入 (セクション 193 に基づく)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-123">Income from interest on securities (Under section 193)</span></span>
- <span data-ttu-id="cdbe2-124">配当からの収入 (セクション 194 に基づく)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-124">Income from dividend (Under section 194)</span></span>
- <span data-ttu-id="cdbe2-125">利息からの収入 (セクション 194A に基づく)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-125">Income from interest (Under section 194A)</span></span>
- <span data-ttu-id="cdbe2-126">宝くじやクイズからの収入 (セクション 194B に基づく)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-126">Income from lotteries or puzzles (Under section 194B)</span></span>
- <span data-ttu-id="cdbe2-127">競馬などからの払戻金による収入 (セクション 194BB に基づく)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-127">Winning from horse races etc. (Under section 194BB)</span></span>
- <span data-ttu-id="cdbe2-128">契約者と請負業者 (セクション 194C に基づく)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-128">Contractors and sub-contractors (Under section 194C)</span></span>
- <span data-ttu-id="cdbe2-129">保険料収入 (セクション 194D に基づく)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-129">Insurance commission (Under section 194D)</span></span>
- <span data-ttu-id="cdbe2-130">国内貯蓄制度下の預金からの収入 (セクション 194EE に基づく)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-130">Income from deposit under national saving scheme (Under section 194EE)</span></span>
- <span data-ttu-id="cdbe2-131">相互資金または UTI からの収入 (セクション 194F に基づく)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-131">Income from mutual fund or UTI (Under section 194F)</span></span>
- <span data-ttu-id="cdbe2-132">販売または抽選による手数料、報酬、賞金など (セクション 194G に基づく)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-132">Commission, Remuneration, Prize etc., on sale or lottery (Under section 194G)</span></span>
- <span data-ttu-id="cdbe2-133">手数料や仲介料の支払い (セクション 194H に基づく)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-133">Payment of Commission or brokerage (Under section 194H)</span></span>
- <span data-ttu-id="cdbe2-134">賃借料 (セクション 194I に基づく)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-134">Rent (Under section 194I)</span></span>
- <span data-ttu-id="cdbe2-135">専門的サービス (セクション 194J に基づく)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-135">Professional service (Under section 194J)</span></span>
- <span data-ttu-id="cdbe2-136">設備からの収入 (セクション 194K に基づく)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-136">Income from Units (Under section 194K)</span></span>
- <span data-ttu-id="cdbe2-137">特定の差し込み資産の取得に対する報酬の支払 (セクション 194LA に基づく)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-137">Payment of compensation on acquisition of certain immovable property (Under section 194LA)</span></span>

<span data-ttu-id="cdbe2-138">**非居住者**</span><span class="sxs-lookup"><span data-stu-id="cdbe2-138">**Non-residents**</span></span>

- <span data-ttu-id="cdbe2-139">非居住スポーツ選手またはスポーツ団体への支払 (セクション 194E に基づく)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-139">Payments to Non-resident sportsmen or sports association (Under section 194E)</span></span>
- <span data-ttu-id="cdbe2-140">その他の金額 (セクション 195 に基づく)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-140">Other sums (Under section 195)</span></span>
- <span data-ttu-id="cdbe2-141">非居住者の設備に関する収入 (セクション 196A に基く)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-141">Income in respect of units of non-residents (Under section 196A)</span></span>

    - <span data-ttu-id="cdbe2-142">インド企業の外貨建て債券または株式からの収入 (セクション 196C に基く)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-142">Income from foreign currency bonds or shares of Indian Company (Under section 196C)</span></span>
    - <span data-ttu-id="cdbe2-143">外国人機関投資家の有価証券からの収入 (セクション196D に基づく)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-143">Incomes of foreign institutional investors from securities (Under section 196D)</span></span>
    - <span data-ttu-id="cdbe2-144">所得に関するあらゆる項目に含まれる給与およびその他すべてのプラスの所得 (セクション192)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-144">Salary and all other positive incomes under any head on income (Section 192)</span></span>
    - <span data-ttu-id="cdbe2-145">有価証券の利息 (セクション 193)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-145">Interest on securities (Section 193)</span></span>
    - <span data-ttu-id="cdbe2-146">有価証券利息以外の利息 (セクション 194A)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-146">Interest other than interest on securities (Section 194A)</span></span>
    - <span data-ttu-id="cdbe2-147">請負業者および下請業者への支払い (セクション 194C)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-147">Payments to contractors and sub-contractors (Section 194C)</span></span>
    - <span data-ttu-id="cdbe2-148">宝くじやクロスワードパズルの賞金 (セクション 194B)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-148">Winnings from Lottery or crossword puzzles (Section 194B)</span></span>
    - <span data-ttu-id="cdbe2-149">競馬の払戻金による収入 (セクション 194BB)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-149">Winnings from horse races (Section 194BB)</span></span>
    - <span data-ttu-id="cdbe2-150">保険契約締結のための支払いをすべてカバーする保険手数料 (セクション 194D)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-150">Insurance Commission covering all payments for procuring Insurance business (Section 194D)</span></span>
    - <span data-ttu-id="cdbe2-151">会社ではない非居住者または外国会社に支払われる有価証券利息以外のすべての利息 (セクション 195)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-151">Any interest other than interest on securities payable to non-residents not being a company or to a foreign company (Section 195)</span></span>
    - <span data-ttu-id="cdbe2-152">スポーツ選手やスポーツ団体・機関を含む非居住者のスポーツ選手への支払い。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-152">Payment to non-resident sportsman including athlete or sports association or institution.</span></span> <span data-ttu-id="cdbe2-153">非居住者であるスポーツ選手の場合、新聞や雑誌などに掲載されるインド国内のあらゆる試合やスポーツに関する広告や記事に関する支払い。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-153">In case of non-resident sportsman, payments in respect of advertisements as well as articles on any game/sports in India in newspapers, magazines, and so.</span></span> <span data-ttu-id="cdbe2-154">以上が含まれます (セクション 194E)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-154">is included (Section 194E)</span></span>
    - <span data-ttu-id="cdbe2-155">NSS\[国民貯蓄制度\] に基づく預金に関する支払い (セクション 194EE)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-155">Payment in respect of deposits under NSS \[National Savings Scheme\] (Section 194EE)</span></span>
    - <span data-ttu-id="cdbe2-156">相互資金または UTI による再買戻しの勘定による支払 (セクション 194F)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-156">Payment on account of repurchase of Units by Mutual Fund or UTI (Section 194F)</span></span>
    - <span data-ttu-id="cdbe2-157">手数料や仲介料の支払い (セクション 194H)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-157">Payment for Commission or brokerage (Section 194H)</span></span>
    - <span data-ttu-id="cdbe2-158">賃借料の支払 (セクション 194I)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-158">Payment of rent (Section 194I)</span></span>
    - <span data-ttu-id="cdbe2-159">業務または技術サービスの手数料の支払 (セクション 194J)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-159">Payment of fees for professional or technical services (Section 194J)</span></span>
    - <span data-ttu-id="cdbe2-160">在庫切れ決定、ディストリビュータ、購入者、および編集者に対するコミッション (そのようなチケットに対する変更または変更を含む) (セクション 194G)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-160">Commission to Stockiest, distributors, buyers and sellers of Lottery tickets including remuneration or prize on such tickets (Section 194G)</span></span>
    - <span data-ttu-id="cdbe2-161">外貨で購入した通貨の移動によって生じた、または長期の資本利益で購入した単位からの収入 (セクション 196B)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-161">Income from Units purchased in foreign currency or long-term capital gain arising from the transfer of such Units purchased in foreign currency (Section 196B)</span></span>
    - <span data-ttu-id="cdbe2-162">利子または配当金に関して、非居住者に対する収入の支払 (セクション 196C)</span><span class="sxs-lookup"><span data-stu-id="cdbe2-162">Payment of any income to non-residents in respect of interest or dividend on bonds and shares (Section 196C)</span></span>

<span data-ttu-id="cdbe2-163">TDS は、購買、販売、販売返品、貸方書、固定資産の取得、前払、前払、約束手形、約束手形、会社間トランザクションに基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-163">TDS is calculated on purchases, sales, sales returns, credit notes, fixed asset acquisitions, prepayments, advance payments, promissory notes, works tax, and intercompany transactions.</span></span>

> [!NOTE]
> <span data-ttu-id="cdbe2-164">現在のインドの税シナリオでは、TDS は販売トランザクションで算出されません。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-164">In the current Indian tax scenario, TDS isn't calculated on sales transactions.</span></span> <span data-ttu-id="cdbe2-165">ただし、販売トランザクション (特に会社間トランザクション) で TDS で回収可能な計算を行う規定がシステムに含まれます。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-165">However, the system includes a provision to calculate TDS recoverable on sales transactions, especially for intercompany transactions.</span></span>

<span data-ttu-id="cdbe2-166">TDS の計算では、常にしきい値と、TDS コンポーネントに対して定義されている例外のしきい値が考慮されます。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-166">The calculation of TDS always considers the threshold and the exception threshold that are defined for the TDS component.</span></span>

<span data-ttu-id="cdbe2-167">定期的な TDS 決済プロセスを実行し、TDS 所轄官庁の仕入先に対して TDS の支払を決済する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-167">The periodic TDS settlement process must be run, and the TDS payments must be settled to TDS authority vendors.</span></span>

<span data-ttu-id="cdbe2-168">仕入先または顧客から受け取った TDS 証明書の証明書番号と日付を記録、更新できます。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-168">The certificate numbers and dates for TDS certificates that are received from vendors or customers can be recorded and updated.</span></span> <span data-ttu-id="cdbe2-169">また、フォーム 26Q とフォーム 27Q の四半期明細書、および TDS のフォーム16A 証明書は Finance で生成できます。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-169">Additionally, Form 26Q and Form 27Q quarterly statements, and the Form 16A certificate for TDS, can be generated in Finance.</span></span>

## <a name="setting-up-and-working-with-tds"></a><span data-ttu-id="cdbe2-170">TDS の設定と操作</span><span class="sxs-lookup"><span data-stu-id="cdbe2-170">Setting up and working with TDS</span></span>

<span data-ttu-id="cdbe2-171">ここでは、TDS の設定と操作のプロセスについての概要を示します。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-171">Here is an overview of the process for setting up and working with TDS:</span></span>

1. <span data-ttu-id="cdbe2-172">**TDS の設定:**</span><span class="sxs-lookup"><span data-stu-id="cdbe2-172">**TDS setup:**</span></span>

    - <span data-ttu-id="cdbe2-173">パラメーターの設定:</span><span class="sxs-lookup"><span data-stu-id="cdbe2-173">Parameter setup:</span></span>

        - <span data-ttu-id="cdbe2-174">総勘定元帳のパラメーターで、TDS に関連するパラメータを有効化します。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-174">In General ledger parameters, activate parameters that are related to TDS.</span></span>
        - <span data-ttu-id="cdbe2-175">総勘定元帳のパラメーターで、源泉徴収税支払の番号順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-175">In General ledger parameters, set up the number sequence for withholding tax payments.</span></span>
        - <span data-ttu-id="cdbe2-176">買掛金勘定と売掛金勘定のパラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-176">Set up parameters in Accounts payable and Accounts receivable.</span></span>

    - <span data-ttu-id="cdbe2-177">基本設定:</span><span class="sxs-lookup"><span data-stu-id="cdbe2-177">Basic setup:</span></span>

        - <span data-ttu-id="cdbe2-178">会社、顧客、仕入先の TDS 登録番号を設定します。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-178">Set up TDS registration numbers for a company, customers, and vendors.</span></span>
        - <span data-ttu-id="cdbe2-179">TDS コンポーネントのグループを設定します。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-179">Set up TDS component groups.</span></span>
        - <span data-ttu-id="cdbe2-180">TDS コンポーネントの設定、TDS コンポーネント グループの関連付け、TDS コンポーネント グループのしきい値と例外のしきい値の定義を行います。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-180">Set up TDS components, attach TDS component groups to them, and define the threshold and exception threshold for them.</span></span>
        - <span data-ttu-id="cdbe2-181">TDS の所轄官庁を設定します。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-181">Set up TDS authorities.</span></span>
        - <span data-ttu-id="cdbe2-182">TDS の精算期間を設定します。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-182">Set up TDS settlement periods.</span></span>
        - <span data-ttu-id="cdbe2-183">TDS 税コードを設定し、そのコードに TDS コンポーネントを関連付けます。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-183">Set up TDS tax codes, and attach TDS components to them.</span></span>
        - <span data-ttu-id="cdbe2-184">TDS 税グループを設定し、そのコードに TDS 税コードを関連付けます。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-184">Set up TDS tax groups, and attach TDS tax codes to them.</span></span>
        - <span data-ttu-id="cdbe2-185">式デザイナーで、式を定義し、TDS グループの TDS を計算します。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-185">In the formula designer, define a formula to calculate TDS for a TDS group.</span></span>
        - <span data-ttu-id="cdbe2-186">TDS 特約証明書番号を記録します。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-186">Record TDS concession certificate numbers.</span></span>

    - <span data-ttu-id="cdbe2-187">勘定科目と会社の設定:</span><span class="sxs-lookup"><span data-stu-id="cdbe2-187">Ledger accounts and company setup:</span></span>

        - <span data-ttu-id="cdbe2-188">TDS 買掛/未払金および売掛/未収金元帳勘定を設定します。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-188">Set up TDS payable and receivable ledger accounts.</span></span>
        - <span data-ttu-id="cdbe2-189">会社の税控除および回収勘定科目番号 (TAN) と控除項目タイプのカテゴリを設定します。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-189">Set up a Tax Deduction and Collection Account Number (TAN) and a deductor type category for the company.</span></span>

    - <span data-ttu-id="cdbe2-190">その他の設定:</span><span class="sxs-lookup"><span data-stu-id="cdbe2-190">Other setup:</span></span>

        - <span data-ttu-id="cdbe2-191">TDS 配賦を含む支払スケジュールを設定します。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-191">Set up a payment schedule that includes TDS allocation.</span></span>
        - <span data-ttu-id="cdbe2-192">TDS 所轄官庁への支払の支払手数料タイプを設定します。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-192">Set up a payment fee type for payments to the TDS authority.</span></span>
        - <span data-ttu-id="cdbe2-193">仕入先および顧客の TDS グループ、固定勘定番号(PANs) 、および TANs に関する情報を設定します。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-193">Set up information about TDS groups, permanent account numbers (PANs), and TANs for vendors and customers.</span></span>

2. <span data-ttu-id="cdbe2-194">**トランザクションにおける TDS の計算:**</span><span class="sxs-lookup"><span data-stu-id="cdbe2-194">**Calculation of TDS in transactions:**</span></span>

    - <span data-ttu-id="cdbe2-195">請求と支払</span><span class="sxs-lookup"><span data-stu-id="cdbe2-195">Invoices and payments</span></span>
    - <span data-ttu-id="cdbe2-196">支払手形</span><span class="sxs-lookup"><span data-stu-id="cdbe2-196">Promissory notes</span></span>
    - <span data-ttu-id="cdbe2-197">前払</span><span class="sxs-lookup"><span data-stu-id="cdbe2-197">Advance payments</span></span>
    - <span data-ttu-id="cdbe2-198">前払</span><span class="sxs-lookup"><span data-stu-id="cdbe2-198">Prepayments</span></span>

3. <span data-ttu-id="cdbe2-199">**TDS 決済:**</span><span class="sxs-lookup"><span data-stu-id="cdbe2-199">**TDS settlement:**</span></span>

    - <span data-ttu-id="cdbe2-200">定期 TDS 決済プロセス</span><span class="sxs-lookup"><span data-stu-id="cdbe2-200">Periodic TDS settlement process</span></span>
    - <span data-ttu-id="cdbe2-201">TDS 所轄官庁の仕入先への TDS 支払いの決済と TDS チャランの生成</span><span class="sxs-lookup"><span data-stu-id="cdbe2-201">Settlement of TDS payments to TDS authority vendors and generation of TDS challan</span></span>

4. <span data-ttu-id="cdbe2-202">**TDSの照会、明細書、証明書:**</span><span class="sxs-lookup"><span data-stu-id="cdbe2-202">**TDS inquiries, statements, and certificate:**</span></span>

    - <span data-ttu-id="cdbe2-203">TDS証明書の番号と日付を記録および更新します。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-203">Record and update TDS certificate numbers and dates.</span></span>
    - <span data-ttu-id="cdbe2-204">TDS 照会および転記済 TDS 照会を生成します。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-204">Generate a TDS inquiry and a posted TDS inquiry.</span></span>
    - <span data-ttu-id="cdbe2-205">フォーム 27A、フォーム 26Q、フォーム 27Q TDS、e-TDS 四半期明細書を生成します。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-205">Generate Form 27A, Form 26Q, and Form 27Q TDS and e-TDS quarterly statements.</span></span>
    - <span data-ttu-id="cdbe2-206">フォーム 16 A の TDS 証明書を生成します。</span><span class="sxs-lookup"><span data-stu-id="cdbe2-206">Generate a Form 16A TDS certificate.</span></span>
