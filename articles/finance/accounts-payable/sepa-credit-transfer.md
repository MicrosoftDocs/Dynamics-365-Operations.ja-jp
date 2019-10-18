---
title: SEPA 口座振替の概要
description: この記事では、ISO 20022 口座振替に関する一般情報を提供します。これは単一ユーロ支払地域 (SEPA) 口座振替および仕入先に対するそのほかの電子支払を含みます。 SEPA 口座振替は、1 つの会社または個人から別の会社または個人に対する、ユーロでの特定のタイプの支払です。 このトピックは、口座振替の支払ファイルを設定して送信する方法も説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, VendPaymMode
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 11124
ms.assetid: 36b0f870-16d4-4bbb-8da5-e747e69b970d
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f0fc01508bd206f750a4101521cd9dff7b647656
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178727"
---
# <a name="sepa-credit-transfer-overview"></a><span data-ttu-id="bfe54-105">SEPA 口座振替の概要</span><span class="sxs-lookup"><span data-stu-id="bfe54-105">SEPA credit transfer overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bfe54-106">この記事では、ISO 20022 口座振替に関する一般情報を提供します。これは単一ユーロ支払地域 (SEPA) 口座振替および仕入先に対するそのほかの電子支払を含みます。</span><span class="sxs-lookup"><span data-stu-id="bfe54-106">This article provides general information about ISO 20022 credit transfers, which include Single Euro Payments Area (SEPA) credit transfers and any other electronic payments for vendors.</span></span> <span data-ttu-id="bfe54-107">SEPA 口座振替は、1 つの会社または個人から別の会社または個人に対する、ユーロでの特定のタイプの支払です。</span><span class="sxs-lookup"><span data-stu-id="bfe54-107">A SEPA credit transfer is a specific type of payment in euros from one company or individual to another company or individual.</span></span> <span data-ttu-id="bfe54-108">このトピックは、口座振替の支払ファイルを設定して送信する方法も説明します。</span><span class="sxs-lookup"><span data-stu-id="bfe54-108">The topic also explains how to set up and transmit a credit transfer payment file.</span></span>

## <a name="what-is-a-credit-transfer-message"></a><span data-ttu-id="bfe54-109">口座振替メッセージとは何ですか。</span><span class="sxs-lookup"><span data-stu-id="bfe54-109">What is a credit transfer message?</span></span>
<span data-ttu-id="bfe54-110">口座振替メッセージとは、開始側 (会社) が自身の口座から債権者に資金移動を送信する要求です。</span><span class="sxs-lookup"><span data-stu-id="bfe54-110">The credit transfer message is a request that an initiating party (your company) sends to move funds from its own account to a creditor.</span></span> <span data-ttu-id="bfe54-111">口座振替メッセージの国/地域固有のおよび銀行固有の実装が数多くあります。</span><span class="sxs-lookup"><span data-stu-id="bfe54-111">There are many country/region-specific and bank-specific implementations of credit transfer messages.</span></span> <span data-ttu-id="bfe54-112">そのいくつかは 1 つの国/地域内で使用され、いくつかは標準となります。</span><span class="sxs-lookup"><span data-stu-id="bfe54-112">Some of them are used within one country/region, and some are becoming standards.</span></span> <span data-ttu-id="bfe54-113">1 つの確立されているグローバル基準は、口座振替などの ISO 20022 およびその起動開始メッセージです。</span><span class="sxs-lookup"><span data-stu-id="bfe54-113">One well-established global standard is ISO 20022 and its initiation messages, such as Credit transfer.</span></span> <span data-ttu-id="bfe54-114">次の図は、選択された口座振替メッセージの関係と補償を示します。</span><span class="sxs-lookup"><span data-stu-id="bfe54-114">The following illustration shows the relations and coverage for selected credit transfer messages.</span></span> 
<span data-ttu-id="bfe54-115">![口座振替](./media/credit-transfer.jpg) 口座振替メッセージ</span><span class="sxs-lookup"><span data-stu-id="bfe54-115">![Credit tansfer](./media/credit-transfer.jpg) Credit transfer messages</span></span> 

## <a name="what-are-iso-20022-and-sepa-payments"></a><span data-ttu-id="bfe54-116">ISO 20022 および SEPA 支払とは何ですか。</span><span class="sxs-lookup"><span data-stu-id="bfe54-116">What are ISO 20022 and SEPA payments?</span></span>
<span data-ttu-id="bfe54-117">単一ユーロ支払地域 (SEPA) は欧州委員会によって設定され、個人、事業または組織および銀行がどの国または地域にあるかに関係なく、すべての電子支払は国内と見なされます。</span><span class="sxs-lookup"><span data-stu-id="bfe54-117">The Single Euro Payments Area (SEPA) is set up by the European Commission and dictates that all electronic payments are considered domestic, regardless of the country/region where the individual, business, or organization, and the bank are located.</span></span> <span data-ttu-id="bfe54-118">国内支払と国境を越えた支払の間に違いはありません。</span><span class="sxs-lookup"><span data-stu-id="bfe54-118">There is no difference between national payments and cross-border payments.</span></span> <span data-ttu-id="bfe54-119">SEPA には、28 の欧州連合 (EU) の加盟国とアイスランド、リヒテンシュタイン、ノルウェー、スイス、およびモナコとサンマリノが含まれます。</span><span class="sxs-lookup"><span data-stu-id="bfe54-119">The SEPA includes the 28 member states of the European Union (EU), and also Iceland, Liechtenstein, Norway, Switzerland, Monaco, and San Marino.</span></span> <span data-ttu-id="bfe54-120">SEPA により、欧州経済領域 (EEA) 内の支払トランザクションの単一市場が形成されます。</span><span class="sxs-lookup"><span data-stu-id="bfe54-120">The SEPA helps form a single market for payment transactions within the European Economic Area (EEA).</span></span> <span data-ttu-id="bfe54-121">最終的に、SEPA により、銀行、事業、および個人が扱う支払形式の数を減らすと予想されます。</span><span class="sxs-lookup"><span data-stu-id="bfe54-121">Ultimately, the SEPA is expected to reduce the number of payment formats that banks, businesses, and individuals must work with.</span></span> <span data-ttu-id="bfe54-122">指令への支払サービス ディレクティブ (PSD) を介した SEPA 支払の法的根拠は欧州委員会が設定しました。</span><span class="sxs-lookup"><span data-stu-id="bfe54-122">The European Commission established the legal foundation for SEPA payments through the Payment Services Directive (PSD).</span></span> <span data-ttu-id="bfe54-123">欧州決済協議会 (EPC) は、次の活動で SEPA をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="bfe54-123">The European Payments Council (EPC) supports the SEPA through the following activities:</span></span>

-   <span data-ttu-id="bfe54-124">これは、ISO 20022 の統合的な金融業務に関する通信メッセージ規格の XML 形式を使用して、SEPAの電子支払の標準を設定します。</span><span class="sxs-lookup"><span data-stu-id="bfe54-124">It sets the standards for SEPA electronic payments by using the ISO 20022 Universal financial industry message scheme XML format.</span></span>
-   <span data-ttu-id="bfe54-125">これはユーロ支払処理に関するルールとガイドラインを設定します。</span><span class="sxs-lookup"><span data-stu-id="bfe54-125">It establishes rules and guidelines about the handling of euro payments.</span></span>

<span data-ttu-id="bfe54-126">ヨーロッパの銀行から構成される EPC は SEPA 支払手段の商業的、技術的フレームワークを開発します。</span><span class="sxs-lookup"><span data-stu-id="bfe54-126">The EPC, which consists of European banks, develops the commercial and technical frameworks for SEPA payment instruments.</span></span> <span data-ttu-id="bfe54-127">3 つのタイプの SEPA 支払が使用されます。</span><span class="sxs-lookup"><span data-stu-id="bfe54-127">Three types of SEPA payments are used:</span></span>

-   <span data-ttu-id="bfe54-128">口座振替</span><span class="sxs-lookup"><span data-stu-id="bfe54-128">Credit transfers</span></span>
-   <span data-ttu-id="bfe54-129">口座引落</span><span class="sxs-lookup"><span data-stu-id="bfe54-129">Direct debits</span></span>
-   <span data-ttu-id="bfe54-130">カード</span><span class="sxs-lookup"><span data-stu-id="bfe54-130">Cards</span></span>

## <a name="what-is-a-sepa-credit-transfer"></a><span data-ttu-id="bfe54-131">SEPA 口座振替とは何ですか。</span><span class="sxs-lookup"><span data-stu-id="bfe54-131">What is a SEPA credit transfer?</span></span>
<span data-ttu-id="bfe54-132">SEPA 口座振替は、個人または 1 つの会社から別の会社または個人に対する支払です。</span><span class="sxs-lookup"><span data-stu-id="bfe54-132">A SEPA credit transfer is a payment from one company or individual to another company or individual.</span></span> <span data-ttu-id="bfe54-133">支払はユーロで、国際銀行番号 (IBAN) および両方の当事者の銀行識別コード (BIC) を含む必要があります。</span><span class="sxs-lookup"><span data-stu-id="bfe54-133">Payments must be in euros, and must include the International Bank Account Number (IBAN) and the Bank Identifier Code (BIC) for both parties.</span></span> <span data-ttu-id="bfe54-134">(BIC は、国際銀行間通信協会 \[SWIFT\] とも呼ばれます。) また、トランザクション原価は両方の当事者間で共有する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bfe54-134">(The BIC is also known as the Society for Worldwide Interbank Financial Telecommunication \[SWIFT\] code.) Additionally, transaction costs must be shared between both parties.</span></span> <span data-ttu-id="bfe54-135">当事者間で発生する口座振替は、ISO 20022 支払処理標準に準拠した XML ファイル、EPC によって指定されている XML 形式を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bfe54-135">Credit transfers that occur between parties should use XML files that comply with ISO 20022 payment processing standards and the XML format, as specified by the EPC.</span></span>

## <a name="how-is-a-credit-transfer-implemented"></a><span data-ttu-id="bfe54-136">口座振替はどのように実装されますか。</span><span class="sxs-lookup"><span data-stu-id="bfe54-136">How is a credit transfer implemented?</span></span>
<span data-ttu-id="bfe54-137">欧州諸国の口座振替の支払形式は、Microsoft Dynamics 365 Finance の電子申告 (ER) および支払方法機能を使用して実行されます。</span><span class="sxs-lookup"><span data-stu-id="bfe54-137">The credit transfer payment format for European countries is implemented by using the Electronic reporting (ER) and Methods of payment functionality in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="bfe54-138">ほかの地域で使用されるいくつかの口座振替の形式は、レガシ支払フレームワークを使用します。</span><span class="sxs-lookup"><span data-stu-id="bfe54-138">A few credit transfer formats that are used in other regions still use the legacy payment framework.</span></span> <span data-ttu-id="bfe54-139">ほかの複数のフォームの間で、使用可能な 12 の ISO 20022 口座振替のファイル形式があります。</span><span class="sxs-lookup"><span data-stu-id="bfe54-139">Among many other formats, there are twelve ISO 20022 credit transfer file formats that are available.</span></span> <span data-ttu-id="bfe54-140">これらのエクスポート形式は、SEPA ISO 20022 XML 標準に準拠します。</span><span class="sxs-lookup"><span data-stu-id="bfe54-140">These export formats conform to the SEPA ISO 20022 XML standard.</span></span> <span data-ttu-id="bfe54-141">それらが使用されている国/地域の非ユーロの支払振替、および EPC がリリースする SEPA 口座振替設定ルールブックのバージョン 8.2 で指定されたユーロ支払を生成するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="bfe54-141">They are used to generate non-euro payment transfers for countries/regions where they are used and euro payments as specified in version 8.2 of the SEPA Credit Transfer Scheme Rulebook that the EPC releases.</span></span> <span data-ttu-id="bfe54-142">口座振替を実装する前に、電子銀行決済のファイルをアップロードするために必要なソフトウェアを取得するために、銀行にお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="bfe54-142">Before you can implement credit transfers, you must contact your bank to obtain the software that is required in order to upload electronic banking files.</span></span> <span data-ttu-id="bfe54-143">銀行に対する支払指図を含む XML ファイルの転送にそのソフトウェアを使用します。</span><span class="sxs-lookup"><span data-stu-id="bfe54-143">You will use that software to transfer the XML files that contain payment orders to your bank.</span></span>

## <a name="what-credit-transfer-formats-are-currently-supported"></a><span data-ttu-id="bfe54-144">現在どんな口座振替フォーマットがサポートされていますか。</span><span class="sxs-lookup"><span data-stu-id="bfe54-144">What credit transfer formats are currently supported?</span></span>
<span data-ttu-id="bfe54-145">必要に応じていつでも Microsoft Dynamics Lifecycle services (LCS) の共有アセット ライブラリに移動して、**GER コンフィギュレーション**資産タイプのある利用可能なファイルで最新の一覧を表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bfe54-145">You should always go to the Shared asset library on Microsoft Dynamics Lifecycle services (LCS) and view the most up-to-date list of available files that have an asset type of **GER configuration**.</span></span> <span data-ttu-id="bfe54-146">次のセクション、"何を設定する必要がありますか。"では、利用可能なコンフィギュレーションおよびインポート選択されているコンフィギュレーションを表示するための LCS リポジトリの作成方法について説明するトピックへのリンクを提供します。</span><span class="sxs-lookup"><span data-stu-id="bfe54-146">The next section, "What do I have to set up?", provides a link to the topic that explains how to create an LCS repository to review available configurations and import selected configurations.</span></span>

## <a name="what-do-i-have-to-set-up"></a><span data-ttu-id="bfe54-147">何を設定する必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="bfe54-147">What do I have to set up?</span></span>
-   <span data-ttu-id="bfe54-148">口座振替ファイルを作成する前に、少なくとも 1 つの有効な口座振替コンフィギュレーションを、ER コンフィギュレーションにインポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="bfe54-148">Before you can create credit transfer files, at least one active credit transfer configuration must be imported into your ER configurations.</span></span> <span data-ttu-id="bfe54-149">手順については、[Lifecycle Services の電子申告コンフィギュレーションのダウンロード](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bfe54-149">For instructions, see [Download Electronic reporting configurations from Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>
-   <span data-ttu-id="bfe54-150">支払の買掛金勘定の方法をコンフィギュレーションするときに、**一般的な電子申告** チェック ボックスをオンにし、エクスポート形式のコンフィギュレーションとして適切な口座振替形式 (たとえば、**ISO 20022 口座振替 (AT)**) を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfe54-150">When you configure Accounts payable methods of payment, select the **Generic electronic reporting** check box, and select the appropriate credit transfer format (for example, **ISO 20022 Credit transfer (AT)**) as an export format configuration.</span></span>
-   <span data-ttu-id="bfe54-151">法人および銀行口座情報を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bfe54-151">You must also set up the legal entity and bank account information.</span></span>
-   <span data-ttu-id="bfe54-152">銀行口座番号、IBAN、および時にはSWIFT コード (BICs) または他の ID が、有効な口座振替の支払を作成するため必要になります。</span><span class="sxs-lookup"><span data-stu-id="bfe54-152">Bank account numbers, IBANs, and sometimes SWIFT codes (BICs) or other IDs are required in order to create valid credit transfer payments.</span></span> <span data-ttu-id="bfe54-153">したがって、仕入先の銀行口座および振込を要求する組織の銀行口座用にそれらを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bfe54-153">Therefore, you must set up them for the vendor bank account and the bank account for the organization that is requesting the transfer.</span></span>
-   <span data-ttu-id="bfe54-154">口座振替メッセージで参照される関係者の付加価値税 (VAT) 番号など、追加情報が必要になるかもしれません。</span><span class="sxs-lookup"><span data-stu-id="bfe54-154">Additional information might be required, such as value-added tax (VAT) numbers for the parties that are referred to in the credit transfer message.</span></span> <span data-ttu-id="bfe54-155">この情報は、必要時に仕入先と法人用に設定される必要があります。</span><span class="sxs-lookup"><span data-stu-id="bfe54-155">This information must be set up for vendors and for the legal entity when it's requested.</span></span>
-   <span data-ttu-id="bfe54-156">いくつかの買掛金勘定支払方法、ほとんど支払の ISO 20022 基準メソッドは、**サービス タイプ** = **SLEV**などの **支払フォーマット コード セット**の追加設定を要求するかもしれません。</span><span class="sxs-lookup"><span data-stu-id="bfe54-156">Some Accounts payable methods of payment, mostly ISO 20022–based methods of payment, might require additional setup for **Payment format code sets**, such as **Service type** = **SLEV**.</span></span> <span data-ttu-id="bfe54-157">これらのコードは、支払処理中に支払トランザクションに対する追加のタグ付けとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="bfe54-157">Those codes are used as additional tagging for payment transactions during payment processing.</span></span> <span data-ttu-id="bfe54-158">支払コードの既定値では、**カテゴリ目的**、**手数料負担者**、**ローカル支払方法** および **サービス レベル** などが 2 箇所に設定されます。</span><span class="sxs-lookup"><span data-stu-id="bfe54-158">Default values of Payment codes, like **Category purpose**, **Charge bearer**, **Local instrument** and **Service level** can be set in two places.</span></span> <span data-ttu-id="bfe54-159">1 箇所は **買掛金勘定支払仕訳帳ヘッダー** および 2 箇所目は **買掛金勘定支払方法**です。</span><span class="sxs-lookup"><span data-stu-id="bfe54-159">The first place is **Accounts payable payment journal header** and the second is **Accounts payable methods for payments**.</span></span> <span data-ttu-id="bfe54-160">支払仕訳帳明細行の作成時に、支払仕訳帳ヘッダーで設定された支払コードの値が仕訳帳明細行に転送されます。設定されていない場合は、支払方法が使用されます。</span><span class="sxs-lookup"><span data-stu-id="bfe54-160">Upon payment journal lines creation, Payment code values set on payment journal header are transferred to a journal line, if not set, the values from Methods of payment are used.</span></span>

## <a name="what-parameters-are-available-for-generating-credit-transfer-payments"></a><span data-ttu-id="bfe54-161">口座振替支払の生成にどのパラメーターが使用できますか。</span><span class="sxs-lookup"><span data-stu-id="bfe54-161">What parameters are available for generating credit transfer payments?</span></span>
<span data-ttu-id="bfe54-162">特定のパラメータの一覧は、口座振替形式によって異なります。</span><span class="sxs-lookup"><span data-stu-id="bfe54-162">The list of specific parameters depends on the credit transfer format.</span></span> <span data-ttu-id="bfe54-163">次の表は、仕入先支払仕訳帳のドイツの ISO 20022 口座振替の支払ファイルを生成するときに使用可能なパラメーターを示します。</span><span class="sxs-lookup"><span data-stu-id="bfe54-163">The following table shows the parameters that are available when you generate a ISO 20022 credit transfer payment file for Germany in a vendor payment journal.</span></span> <span data-ttu-id="bfe54-164">**バックグラウンドで実行** タブで使用できるオプションを使用して、支払の生成をバッチ モードで実行できます。</span><span class="sxs-lookup"><span data-stu-id="bfe54-164">By using the options that are available on the **Run in the background** tab, you can run payment generation in batch mode.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bfe54-165">フィールド</span><span class="sxs-lookup"><span data-stu-id="bfe54-165">Field</span></span></th>
<th><span data-ttu-id="bfe54-166">説明</span><span class="sxs-lookup"><span data-stu-id="bfe54-166">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bfe54-167">バッチ記帳</span><span class="sxs-lookup"><span data-stu-id="bfe54-167">Batch booking</span></span></td>
<td><span data-ttu-id="bfe54-168">XML ファイルにバッチ記帳タグを含める場合は、このチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="bfe54-168">Select this check box to include the batch booking tag in the XML file.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfe54-169">処理日</span><span class="sxs-lookup"><span data-stu-id="bfe54-169">Processing date</span></span></td>
<td><span data-ttu-id="bfe54-170">銀行が支払を処理する日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="bfe54-170">Enter the date when the bank should process the payments.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bfe54-171">書式設定</span><span class="sxs-lookup"><span data-stu-id="bfe54-171">Format</span></span></td>
<td><span data-ttu-id="bfe54-172">国/地域または銀行の条件に応じて送金情報の形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfe54-172">Select the format for remittance information, depending on the requirements of your country/region or bank:</span></span>
<ul>
<li><span data-ttu-id="bfe54-173"><strong>Strd</strong> – 1 つの支払明細行が 1 つの請求書に対して決済されるときに構造化された形式を使用する場合は、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="bfe54-173"><strong>Strd</strong> – Select this option to use the structured format when one payment line is settled against one invoice.</span></span> <span data-ttu-id="bfe54-174">このオプションは、フランス、ドイツ、またはオランダの国/地域固有のエクスポート形式では使用できません。</span><span class="sxs-lookup"><span data-stu-id="bfe54-174">This option isn&#39;t available for the country/region-specific export formats for France, Germany, or the Netherlands.</span></span></li>
<li><span data-ttu-id="bfe54-175"><strong>Ustrd</strong> – 支払が複数の請求書に対して決済されるときに構造化されていない形式を使用する場合は、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="bfe54-175"><strong>Ustrd</strong> – Select this option to use the unstructured format when the payment is settled against multiple invoices.</span></span> <span data-ttu-id="bfe54-176">決済された請求書の請求書番号が送金情報として連結して使用されます。</span><span class="sxs-lookup"><span data-stu-id="bfe54-176">The invoice numbers for the settled invoices are concatenated and used as the remittance information.</span></span> <span data-ttu-id="bfe54-177">ISO 20022 のガイドラインに準拠するために、構造化されていない送金情報は 140 文字に限定されます。</span><span class="sxs-lookup"><span data-stu-id="bfe54-177">In compliance with ISO 20022 guidelines, unstructured remittance information is limited to 140 characters.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfe54-178">請求書の数</span><span class="sxs-lookup"><span data-stu-id="bfe54-178">Number of invoices</span></span></td>
<td><span data-ttu-id="bfe54-179"><strong>支払通知</strong> レポートが印刷される請求書の数を入力します。</span><span class="sxs-lookup"><span data-stu-id="bfe54-179">Enter the number of invoices that the <strong>Payment advice</strong> report is printed from.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bfe54-180">順序番号</span><span class="sxs-lookup"><span data-stu-id="bfe54-180">Sequence number</span></span></td>
<td><span data-ttu-id="bfe54-181">ファイルを識別する順序番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="bfe54-181">Enter a sequence number to identify the file.</span></span> <span data-ttu-id="bfe54-182">順序番号が <strong>出席メモ</strong> レポートに表示されます。</span><span class="sxs-lookup"><span data-stu-id="bfe54-182">The sequence number appears on the <strong>Attending note</strong> report.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfe54-183">出席メモの印刷</span><span class="sxs-lookup"><span data-stu-id="bfe54-183">Print attending note</span></span></td>
<td><span data-ttu-id="bfe54-184"><strong>出席メモ</strong> レポートを印刷するには、このチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="bfe54-184">Select this check box to print the <strong>Attending note</strong> report.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bfe54-185">管理レポートの印刷</span><span class="sxs-lookup"><span data-stu-id="bfe54-185">Print control report</span></span></td>
<td><span data-ttu-id="bfe54-186">支払情報を含むレポートを印刷するには、このチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="bfe54-186">Select this check box to print a report that contains the payment information.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bfe54-187">送付状の印刷</span><span class="sxs-lookup"><span data-stu-id="bfe54-187">Print covering letter</span></span></td>
<td><span data-ttu-id="bfe54-188"><strong>支払通知</strong> レポートを印刷する場合は、このチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="bfe54-188">Select this check box to print the <strong>Payment advice</strong> report.</span></span></td>
</tr>
</tbody>
</table>

## <a name="what-are-ibans-and-bics"></a><span data-ttu-id="bfe54-189">IBAN や BICs とは何ですか。</span><span class="sxs-lookup"><span data-stu-id="bfe54-189">What are IBANs and BICs?</span></span>
<span data-ttu-id="bfe54-190">国際銀行番号が (IBAN) および銀行識別コード (BIC) は世界中の多くの国/地域の口座を識別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="bfe54-190">The International Bank Account Number (IBAN) and Bank Identifier Code (BIC) are used to identify any account in many countries/regions worldwide.</span></span> <span data-ttu-id="bfe54-191">これらには 34 の SEPA 国/地域が含まれます。</span><span class="sxs-lookup"><span data-stu-id="bfe54-191">These include the 34 SEPA countries/regions.</span></span> <span data-ttu-id="bfe54-192">**SWIFT コード** フィールドに BIC を入力し、**IBAN** フィールドに IBAN を入力します。</span><span class="sxs-lookup"><span data-stu-id="bfe54-192">Enter the BIC in the **SWIFT code** field and the IBAN in the **IBAN** field.</span></span> <span data-ttu-id="bfe54-193">これらのフィールドは債権者の銀行口座および顧客の銀行口座の両方に対して、**銀行口座** ページの **銀行口座** タブの **銀行口座** クイック タブにあります。</span><span class="sxs-lookup"><span data-stu-id="bfe54-193">For both the creditor’s bank account and the customer’s bank account, these fields are located on the **Additional identification** FastTab on the **Bank account** tab of the **Bank accounts** page.</span></span> <span data-ttu-id="bfe54-194">SEPA の支払に対する BIC の使用は現在適用されません。</span><span class="sxs-lookup"><span data-stu-id="bfe54-194">The use of BIC for SEPA payments is no longer enforced.</span></span>

## <a name="how-do-i-transmit-a-payment-file-to-the-bank"></a><span data-ttu-id="bfe54-195">支払ファイルはどのように銀行に送信しますか。</span><span class="sxs-lookup"><span data-stu-id="bfe54-195">How do I transmit a payment file to the bank?</span></span>
<span data-ttu-id="bfe54-196">支払を生成すると、支払ファイルが生成され、Web ブラウザから使用可能な場所に保存するよう求められます。</span><span class="sxs-lookup"><span data-stu-id="bfe54-196">When you generate payments, the payment file is generated, and you're asked to save it from your web browser to any available location.</span></span> <span data-ttu-id="bfe54-197">次の手順として、銀行へ XML ファイルを送信します。</span><span class="sxs-lookup"><span data-stu-id="bfe54-197">The next step is to send the XML file to your bank.</span></span> <span data-ttu-id="bfe54-198">このプロセスは、銀行によって異なります。</span><span class="sxs-lookup"><span data-stu-id="bfe54-198">This process varies from bank to bank.</span></span> <span data-ttu-id="bfe54-199">銀行の指示に従って、処理用のファイルを銀行に送信します。</span><span class="sxs-lookup"><span data-stu-id="bfe54-199">Follow the instructions from your bank to submit the files to the bank for processing.</span></span>



