---
title: SEPA の口座引落の概要
description: 単一ユーロ支払地域 (SEPA) は欧州委員会によって設定され、個人、事業または組織および銀行がどの国または地域にあるかに関係なく、すべての電子支払は国内と見なされます。 国内支払と国境を越えた支払の間に違いはありません。 SEPA には、28 の欧州連合 (EU) の加盟国とアイスランド、リヒテンシュタイン、ノルウェー、スイス、およびモナコとサンマリノが含まれます。 SEPA により、欧州経済領域 (EEA) 内の支払トランザクションの単一市場が形成されます。 最終的に、SEPA により、銀行、事業、および個人が扱う支払形式の数を減らすと予想されます。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, CustBankAccounts, CustParameters, CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 11144
ms.assetid: 3277c9b6-e46e-40c9-aa76-9b0449467842
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fcb7585d344988e00093231f785c1a746226e4e0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445088"
---
# <a name="sepa-direct-debit-overview"></a><span data-ttu-id="fc2a5-107">SEPA の口座引落の概要</span><span class="sxs-lookup"><span data-stu-id="fc2a5-107">SEPA direct debit overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fc2a5-108">単一ユーロ支払地域 (SEPA) は欧州委員会によって設定され、個人、事業または組織および銀行がどの国または地域にあるかに関係なく、すべての電子支払は国内と見なされます。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-108">The Single Euro Payments Area (SEPA) is set up by the European Commission, and dictates that all electronic payments are considered domestic, regardless of the country/region where the individual, business, or organization, and the bank are located.</span></span> <span data-ttu-id="fc2a5-109">国内支払と国境を越えた支払の間に違いはありません。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-109">There is no difference between national and cross-border payments.</span></span> <span data-ttu-id="fc2a5-110">SEPA には、28 の欧州連合 (EU) の加盟国とアイスランド、リヒテンシュタイン、ノルウェー、スイス、およびモナコとサンマリノが含まれます。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-110">The SEPA includes the 28 European Union (EU) member states, as well as Iceland, Liechtenstein, Norway, Switzerland, Monaco and San Marino.</span></span> <span data-ttu-id="fc2a5-111">SEPA により、欧州経済領域 (EEA) 内の支払トランザクションの単一市場が形成されます。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-111">The SEPA helps form a single market for payment transactions within the European Economic Area (EEA).</span></span> <span data-ttu-id="fc2a5-112">最終的に、SEPA により、銀行、事業、および個人が扱う支払形式の数を減らすと予想されます。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-112">Ultimately, the SEPA is expected to reduce the number of payment formats that banks, businesses, and individuals must work with.</span></span>   

<a name="what-is-the-goal-of-sepa-direct-debits"></a><span data-ttu-id="fc2a5-113">SEPA の口座引落の目的は何ですか。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-113">What is the goal of SEPA direct debits?</span></span>
---------------------------------------

<span data-ttu-id="fc2a5-114">署名済み委任状が顧客によって債権者に許可された場合、SEPA の口座引落により、債権者は顧客の銀行口座から資金を回収することができます。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-114">A SEPA direct debit allows a creditor to collect funds from a customer’s bank account, provided that a signed mandate has been granted by the customer to the creditor.</span></span> <span data-ttu-id="fc2a5-115">顧客は債権者が支払を回収することを承認する委任状に署名し、顧客の銀行に支払の回収を指示します。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-115">The customer signs a mandate that authorizes the creditor to collect a payment and instructs the customer’s bank to pay the collection.</span></span> 

<span data-ttu-id="fc2a5-116">SEPA 口座引落は、SEPA の 32 の国/地域内で国内および国境を越えたユーロ口座引落に使用できるはじめての支払手段です。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-116">SEPA Direct Debits create, for the first time, a payment instrument that can be used for both national and cross-border euro direct debits throughout the 32 SEPA countries/regions.</span></span> 

<span data-ttu-id="fc2a5-117">2 つのスキームを使用できます: SEPA Core 口座引落スキームおよび SEPA 企業間 (B2B) 口座引落スキーム。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-117">There are two schemes available: the SEPA Core Direct Debit Scheme and the SEPA Business to Business (B2B) Direct Debit Scheme.</span></span> <span data-ttu-id="fc2a5-118">スキームは両方とも同じファイル形式を使用します。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-118">Both schemes use the same file format.</span></span>

## <a name="what-is-the-core-direct-debit-scheme"></a><span data-ttu-id="fc2a5-119">Core 口座引落スキームとは何ですか。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-119">What is the Core Direct Debit scheme?</span></span>
<span data-ttu-id="fc2a5-120">SEPA Core 口座引落スキームは、基本スキームです。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-120">The SEPA Core Direct Debit Scheme is the basic scheme.</span></span> <span data-ttu-id="fc2a5-121">次の属性があります。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-121">It has the following attributes:</span></span>
-   <span data-ttu-id="fc2a5-122">資金の振替はユーロです (銀行口座に他の通貨の資金が含まれる場合でも)。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-122">The transfer of funds is in euros (even though the bank accounts may hold funds in other currencies).</span></span>
-   <span data-ttu-id="fc2a5-123">顧客および債権者は、SEPA 内にある信用機関の口座を保有している必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-123">The customer and creditor must each hold an account with a credit institution that is located within the SEPA.</span></span>
-   <span data-ttu-id="fc2a5-124">顧客が債権者に署名済委任状を付与する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-124">The customer must grant a signed mandate to the creditor.</span></span>
-   <span data-ttu-id="fc2a5-125">委任状は、最後の回収が開始されてから 36 か月後に有効期限が切れます。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-125">Mandates expire 36 months after the last initiated collection.</span></span>
-   <span data-ttu-id="fc2a5-126">債権者は、委任状が有効の間また最後の回収の後の少なくとも 14 か月間は、委任状を保管しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-126">The creditor must store mandates for as long as the mandate is valid and for at least 14 months after the last collection.</span></span>
-   <span data-ttu-id="fc2a5-127">スキームは、単一 (一回) または定期的な口座引落回収に使用する場合があります。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-127">The scheme may be used for single (one-time) or recurring direct debit collections.</span></span>
-   <span data-ttu-id="fc2a5-128">顧客には、自分の口座から引き落とされてから 8 週間まで、"何の質問もなしに" 払戻しを受ける権利があります。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-128">Customers have a “no questions asked” right to receive a refund for up to eight weeks after the debit of their account.</span></span>

## <a name="what-is-the-sepa-business-to-business-b2b-direct-debit-scheme"></a><span data-ttu-id="fc2a5-129">SEPA 企業間 (B2B) 口座引落スキームとは何ですか。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-129">What is the SEPA Business to Business (B2B) Direct Debit scheme?</span></span>
<span data-ttu-id="fc2a5-130">SEPA B2B 口座引落スキームは、企業間のトランザクションに適用され、SEPA Core 口座引落スキーム上に構築されます。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-130">The SEPA B2B Direct Debit Scheme applies to business-to-business transactions and builds on the SEPA Core Direct Debit Scheme.</span></span> <span data-ttu-id="fc2a5-131">主な違いは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-131">The main differences are:</span></span>
-   <span data-ttu-id="fc2a5-132">SEPA B2B 口座引落スキームは、顧客が一私人 (消費者) の場合は使用できません。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-132">The SEPA B2B Direct Debit Scheme is not allowed when the customer is a private individual (consumer).</span></span>
-   <span data-ttu-id="fc2a5-133">顧客には、承認されたトランザクションの払戻を取得する権利がありません。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-133">The customer is not entitled to obtain a refund of an authorized transaction.</span></span>
-   <span data-ttu-id="fc2a5-134">顧客銀行は、委任状の情報に対して回収を確認して、その回収が承認されたことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-134">Customer banks must make sure that that the collection is authorized, by verifying the collection against mandate information.</span></span> <span data-ttu-id="fc2a5-135">顧客銀行と顧客は、口座引落ごとに実行される検証に同意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-135">Customer banks and customers are required to agree on the verification that will be performed for each direct debit.</span></span>
-   <span data-ttu-id="fc2a5-136">このスキームでは、口座引落を提示するタイムラインが短縮され、返品期間が減少します。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-136">The scheme offers a shorter timeline for presenting direct debits and reduces the return period.</span></span>

## <a name="can-i-use-the-cor1-scheme-for-direct-debit-mandates"></a><span data-ttu-id="fc2a5-137">口座引落手順については COR1 スキームを使用することもできますか。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-137">Can I use the COR1 scheme for direct debit mandates?</span></span>
<span data-ttu-id="fc2a5-138">はい。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-138">Yes.</span></span> <span data-ttu-id="fc2a5-139">オーストリア、ベルギー、ドイツ、フランス、イタリア、スペイン、およびオランダにおける SEPA 口座引落の委任状については COR1 スキームを使用できます。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-139">You can use the COR1 scheme for SEPA direct debit mandates in Austria, Belgium, Germany, France, Italy, Spain, and the Netherlands.</span></span> <span data-ttu-id="fc2a5-140">スキームでは、債権者の口座引落コレクションのための、より短い事前通知期間が用意されています。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-140">The scheme provides a shorter pre-notification period for the direct debit collection for the creditor.</span></span>

## <a name="what-are-international-bank-account-numbers-iban-and-bank-identifier-codes-bic"></a><span data-ttu-id="fc2a5-141">国際銀行番号 (IBAN) および金融機関識別コード (BIC) とは何ですか。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-141">What are International Bank Account Numbers (IBAN) and Bank Identifier Codes (BIC)?</span></span>
<span data-ttu-id="fc2a5-142">国際銀行番号が (IBAN) および銀行識別コード (BIC) は SEPA の 32 の国/地域の口座を識別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-142">The International Bank Account Number (IBAN) and Bank Identifier Code (BIC) are used to identify any account in the 32 SEPA countries/regions.</span></span> <span data-ttu-id="fc2a5-143">SWIFT コード フィールドに BIC を入力し、IBAN フィールドに IBAN を入力します。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-143">Enter the BIC in the SWIFT code field and the IBAN in the IBAN field.</span></span> <span data-ttu-id="fc2a5-144">両方のフィールドは、銀行口座のページにある [銀行口座] タブの [追加 ID] クイック タブにあります。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-144">Both fields are located on the Additional identification FastTab on the Bank account tab in the Bank accounts page.</span></span> <span data-ttu-id="fc2a5-145">これは債権者の銀行口座および顧客の銀行口座の両方に当てはまります。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-145">This is true for both the creditor’s bank account and the customer’s bank account.</span></span>

## <a name="where-do-i-enter-creditor-identifiers-direct-debit-ids"></a><span data-ttu-id="fc2a5-146">どこで債権者の識別子 (口座引落 ID) を入力しますか。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-146">Where do I enter creditor identifiers (Direct debit IDs)?</span></span>
<span data-ttu-id="fc2a5-147">SEPA では、各債権者は固有の債権者識別子で識別されます。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-147">In the SEPA, each creditor is identified by a unique creditor identifier.</span></span> <span data-ttu-id="fc2a5-148">この識別子により、顧客および顧客銀行は各口座引落をフィルター処理でき、顧客の指示によって、口座取引を処理または拒否できます。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-148">This identifier lets the customer and the customer bank filter each direct debit, and then process or reject the direct debit according to customer instructions.</span></span> <span data-ttu-id="fc2a5-149">債権者が自分の銀行を通じてこの識別子を要求する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-149">Creditors must request this identifier through their bank.</span></span> <span data-ttu-id="fc2a5-150">法人の銀行口座の [口座引落 ID] フィールドにこの識別子を入力します。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-150">Enter this identifier in the Direct debit ID field for the bank account for the legal entity.</span></span>

## <a name="what-are-mandates"></a><span data-ttu-id="fc2a5-151">委任状とは何ですか。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-151">What are mandates?</span></span>
<span data-ttu-id="fc2a5-152">顧客は債権者が支払を回収することを承認する委任状に署名し、顧客の銀行に支払の回収を指示します。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-152">The customer signs a mandate that authorizes the creditor to collect a payment and instructs the customer’s bank to pay the collection.</span></span> <span data-ttu-id="fc2a5-153">顧客は、用紙フォームでまたは電子的に委任状を発行できます。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-153">The customer can issue the mandate in paper form or electronically.</span></span> <span data-ttu-id="fc2a5-154">既定では、委任状は、口座引落が最後に開始されてから 36 か月に有効期限が切れます。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-154">By default, the mandate expires 36 months after the direct debit is last initiated.</span></span>

## <a name="where-do-i-specify-the-sepa-direct-debit-file-format-iso-20022"></a><span data-ttu-id="fc2a5-155">SEPA 口座引落ファイル形式 (ISO 20022) をどこで指定しますか。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-155">Where do I specify the SEPA Direct Debit file format (ISO 20022)?</span></span>
<span data-ttu-id="fc2a5-156">SEPA のデータ形式は、ISO 20022 のメッセージの標準に基づきます。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-156">The SEPA data formats are based on the ISO 20022 message standards.</span></span> <span data-ttu-id="fc2a5-157">[一般的な電子申告] チェック ボックスをオンにし、支払の売掛金勘定の方法をコンフィギュレーションするときにエクスポート形式のコンフィギュレーションとして SEPA 口座振替形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-157">You will check the Generic electronic reporting checkbox and select the SEPA Direct debit format as an export format configuration when you configure accounts receivable methods of payment.</span></span> <span data-ttu-id="fc2a5-158">顧客支払仕訳帳の支払ファイルを生成すると、その支払方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-158">You use that method of payment when you generate a payment file in a customer payment journal.</span></span>

## <a name="in-what-file-formats-can-i-generate-sepa-direct-debit-payment-files"></a><span data-ttu-id="fc2a5-159">どのファイル形式で SEPA 口座引落支払ファイルを生成できますか。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-159">In what file formats can I generate SEPA direct debit payment files?</span></span>
<span data-ttu-id="fc2a5-160">SEPA 口座引落用の電子支払ファイルを次の形式で生成します。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-160">You can generate electronic payment files for SEPA direct debits in the following formats:</span></span>
-   <span data-ttu-id="fc2a5-161">ベルギー、ドイツ、スペイン、フランス、イタリア、オランダの PAIN.008.001.02 XML ファイル形式で SEPA 口座引落支払ファイルを生成できます。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-161">SEPA direct debit payment files in the PAIN.008.001.02 XML file format for Belgium, Germany, Spain, France, Italy, and the Netherlands.</span></span>
-   <span data-ttu-id="fc2a5-162">SEPA 口座引落支払はオーストリアの PAIN.008.001.02 XML ファイル形式とドイツの PAIN.008.003.02 XML ファイル形式でファイルします。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-162">SEPA direct debit payment files in the PAIN.008.001.02 XML file format for Austria, and in the PAIN.008.003.02 XML file format for Germany.</span></span>

## <a name="how-do-refunds-and-returns-work-with-sepa-direct-debits"></a><span data-ttu-id="fc2a5-163">払戻および返品は SEPA 口座引落ではどのように扱われますか。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-163">How do refunds and returns work with SEPA direct debits?</span></span>
<span data-ttu-id="fc2a5-164">両方の SEPA 口座引落のスキームで、顧客には払戻の一定の権利があります。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-164">Under both SEPA Direct Debit schemes, customers have certain rights to refunds.</span></span> <span data-ttu-id="fc2a5-165">顧客は、理由を与えずに、期日から 8 週間の間に承認されたトランザクションを取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-165">The customer is allowed to recall any authorized transactions during an eight-week period after the due date, without having to give a reason.</span></span> <span data-ttu-id="fc2a5-166">無許可のトランザクションの場合、期間は期日から 13 か月に延長されます。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-166">In the case of unauthorized transactions, the period is extended to 13 months after the due date.</span></span> <span data-ttu-id="fc2a5-167">[顧客トランザクション] ページの [支払いのキャンセル] ボタンを使用して、既に支払われたどんな支払でも手動で取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="fc2a5-167">Reversals of any payments that have been made are accomplished manually by using the Cancel payment button in the Customer transactions page.</span></span>





