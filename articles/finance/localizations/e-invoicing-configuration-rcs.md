---
title: Regulatory Configuration Services (RCS) から電子請求書を設定する
description: このトピックでは、Dynamics 365 Regulatory Configuration Services (RCS) で電子請求書を設定する方法について説明します。
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 9958091db4a3d7ce0b625e5adc8e2a6b37878618
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840247"
---
# <a name="configure-electronic-invoicing-in-regulatory-configuration-services-rcs"></a><span data-ttu-id="5dbcd-103">Regulatory Configuration Services (RCS) から電子請求書を設定する</span><span class="sxs-lookup"><span data-stu-id="5dbcd-103">Configure Electronic invoicing in Regulatory Configuration Services (RCS)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5dbcd-104">このトピックでは、Dynamics 365 Regulatory Configuration Services (RCS) で電子請求書を設定する機能に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-104">This topic provides information about the configuration capabilities of Electronic invoicing in Dynamics 365 Regulatory Configuration Services (RCS).</span></span>

<span data-ttu-id="5dbcd-105">設定機能により、コーディングを行わずに、電子請求書に関するビジネスや規制の要件を満たすことができる電子請求を使うことができます。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-105">It is through the configuration capabilities that Electronic invoicing helps you meet business and regulatory requirements of electronic invoices without having to do any coding.</span></span> <span data-ttu-id="5dbcd-106">また、Webサービスで電子請求書を電子的に承認する必要がある場合は、この構成機能を使用して、コードを実行せずに Web サービスとメッセージを交換する要件を満たすことができます。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-106">And in the scenarios where electronic invoices must be electronically approved by a web services, the configuration capabilities also help you meet the requirements for exchanging messages with a web services, without doing any code.</span></span>

## <a name="electronic-reporting"></a><span data-ttu-id="5dbcd-107">電子申告</span><span class="sxs-lookup"><span data-stu-id="5dbcd-107">Electronic reporting</span></span>

<span data-ttu-id="5dbcd-108">電子申告 (ER) は電子請求をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-108">Electronic reporting (ER) supports Electronic invoicing.</span></span>

<span data-ttu-id="5dbcd-109">データ モデルのマッピングとフォーマットは、ER で作成および維持される構成可能なコンポーネントであり、電子請求で使用されます。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-109">The data model mapping and formats are configurable components that are created and maintained through ER and used in Electronic invoicing.</span></span> <span data-ttu-id="5dbcd-110">ER 形式デザイナは、ファイルの形式を作成・管理するためのツールです。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-110">The ER format designer is the tool for creating and maintaining file formats.</span></span> <span data-ttu-id="5dbcd-111">これは、電子請求機能の構成に使用されます。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-111">It's used to configure the electronic invoicing features.</span></span>

<span data-ttu-id="5dbcd-112">詳細については、[電子申告 (ER) の概要](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-112">For more information, see [Electronic reporting (ER) overview](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).</span></span>

## <a name="electronic-invoicing-features"></a><span data-ttu-id="5dbcd-113">電子請求の機能</span><span class="sxs-lookup"><span data-stu-id="5dbcd-113">Electronic invoicing features</span></span>

<span data-ttu-id="5dbcd-114">電子請求機能で、電子請求を通じて電子請求書を生成することができます。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-114">The electronic invoicing features are responsible for generating electronic invoices through Electronic invoicing.</span></span> <span data-ttu-id="5dbcd-115">これにより設定ルールがカプセル化され、Microsoft Dynamics 365 Finance と Dynamics 365 Supply Chain Management が電子請求および電子請求書に送信するデータを処理するために使用します。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-115">They encapsulate the configuration rules and use them to process the data that Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management send to Electronic invoicing and to electronic invoices.</span></span>

<span data-ttu-id="5dbcd-116">この機能はまた、ファイル形式の仕様に準拠する必要があり、出力はスタンドアロンの電子ファイルのシナリオにも対応しています。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-116">The features also support scenarios where compliance with file format specifications is required and the output is a standalone electronic file.</span></span> <span data-ttu-id="5dbcd-117">ほとんどの場合、指定のファイル形式は税務当局が公開しています。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-117">In most cases, the file format specifications are published by the tax authority.</span></span>

<span data-ttu-id="5dbcd-118">また、税務当局や認定当事者によってホストされる外部の Web サービスとのメッセージ交換や、電子請求書での認証または承認スタンプの要求に対応しています。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-118">Finally, the features support the exchange of messages with external web services that are hosted either by the tax authority or by some accredited party, and requests for authorization or an approval stamp in the electronic invoice.</span></span>

### <a name="availability-of-electronic-invoicing-features"></a><span data-ttu-id="5dbcd-119">電子請求機能の可用性</span><span class="sxs-lookup"><span data-stu-id="5dbcd-119">Availability of electronic invoicing features</span></span>

<span data-ttu-id="5dbcd-120">電子請求機能の可用性は、国または地域によって異なります。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-120">Availability of the electronic invoicing features depends on the country or region.</span></span> <span data-ttu-id="5dbcd-121">一般公開されている機能もありますが、プレビュー段階の機能もあります。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-121">Although some features are generally available, others are in preview.</span></span>

#### <a name="preview-features"></a><span data-ttu-id="5dbcd-122">プレビュー機能</span><span class="sxs-lookup"><span data-stu-id="5dbcd-122">Preview features</span></span>

<span data-ttu-id="5dbcd-123">次の表に、現在プレビュー中の電子請求機能をまとめています。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-123">The following table shows the electronic invoicing features that are currently in preview.</span></span>

| <span data-ttu-id="5dbcd-124">国/地域</span><span class="sxs-lookup"><span data-stu-id="5dbcd-124">Country/region</span></span> | <span data-ttu-id="5dbcd-125">機能名</span><span class="sxs-lookup"><span data-stu-id="5dbcd-125">Feature name</span></span>                         | <span data-ttu-id="5dbcd-126">ビジネス ドキュメント</span><span class="sxs-lookup"><span data-stu-id="5dbcd-126">Business document</span></span> |
|----------------|--------------------------------------|-------------------|
| <span data-ttu-id="5dbcd-127">オーストリア</span><span class="sxs-lookup"><span data-stu-id="5dbcd-127">Austria</span></span>        | <span data-ttu-id="5dbcd-128">オーストリア 顧客電子請求書 (AT)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-128">Austrian electronic invoices (AT)</span></span>    | <span data-ttu-id="5dbcd-129">売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="5dbcd-129">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="5dbcd-130">ベルギー</span><span class="sxs-lookup"><span data-stu-id="5dbcd-130">Belgium</span></span>        | <span data-ttu-id="5dbcd-131">ベルギー 電子請求書 (BE)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-131">Belgian electronic invoice (BE)</span></span>      | <span data-ttu-id="5dbcd-132">売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="5dbcd-132">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="5dbcd-133">ブラジル</span><span class="sxs-lookup"><span data-stu-id="5dbcd-133">Brazil</span></span>         | <span data-ttu-id="5dbcd-134">ブラジル NF-e (BR)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-134">Brazilian NF-e (BR)</span></span>                  | <span data-ttu-id="5dbcd-135">財政文書モデル 55、督促状、取消書、廃棄物</span><span class="sxs-lookup"><span data-stu-id="5dbcd-135">Fiscal document model 55, correction letters, cancellations, and discards</span></span> |
| <span data-ttu-id="5dbcd-136">ブラジル</span><span class="sxs-lookup"><span data-stu-id="5dbcd-136">Brazil</span></span>         | <span data-ttu-id="5dbcd-137">ブラジル NFS-e ABRASF クリチバ (BR)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-137">Brazilian NFS-e ABRASF Curitiba (BR)</span></span> | <span data-ttu-id="5dbcd-138">会計ドキュメントのサービス</span><span class="sxs-lookup"><span data-stu-id="5dbcd-138">Service fiscal documents</span></span> |
| <span data-ttu-id="5dbcd-139">デンマーク</span><span class="sxs-lookup"><span data-stu-id="5dbcd-139">Denmark</span></span>        | <span data-ttu-id="5dbcd-140">デンマーク 電子請求書 (DK)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-140">Danish electronic invoice (DK)</span></span>       | <span data-ttu-id="5dbcd-141">売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="5dbcd-141">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="5dbcd-142">エジプト</span><span class="sxs-lookup"><span data-stu-id="5dbcd-142">Egypt</span></span>          | <span data-ttu-id="5dbcd-143">エジプト 電子請求書 (EG)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-143">Egyptian electronic invoice (EG)</span></span> | <span data-ttu-id="5dbcd-144">売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="5dbcd-144">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="5dbcd-145">エストニア</span><span class="sxs-lookup"><span data-stu-id="5dbcd-145">Estonia</span></span>        | <span data-ttu-id="5dbcd-146">エストニア 電子請求書 (EE)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-146">Estonian electronic invoice (EE)</span></span>     | <span data-ttu-id="5dbcd-147">売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="5dbcd-147">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="5dbcd-148">フィンランド</span><span class="sxs-lookup"><span data-stu-id="5dbcd-148">Finland</span></span>        | <span data-ttu-id="5dbcd-149">フィンランド 電子請求書 (FI)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-149">Finnish electronic invoice (FI)</span></span>      | <span data-ttu-id="5dbcd-150">売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="5dbcd-150">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="5dbcd-151">フランス</span><span class="sxs-lookup"><span data-stu-id="5dbcd-151">France</span></span>         | <span data-ttu-id="5dbcd-152">フランス 電子請求書 (FR)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-152">French electronic invoice (FR)</span></span>       | <span data-ttu-id="5dbcd-153">売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="5dbcd-153">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="5dbcd-154">ドイツ</span><span class="sxs-lookup"><span data-stu-id="5dbcd-154">Germany</span></span>        | <span data-ttu-id="5dbcd-155">ドイツ 電子請求書 (DE)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-155">German electronic invoice (DE)</span></span>       | <span data-ttu-id="5dbcd-156">売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="5dbcd-156">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="5dbcd-157">イタリア</span><span class="sxs-lookup"><span data-stu-id="5dbcd-157">Italy</span></span>          | <span data-ttu-id="5dbcd-158">FatturaPA (IT)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-158">FatturaPA (IT)</span></span>                       | <span data-ttu-id="5dbcd-159">売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="5dbcd-159">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="5dbcd-160">メキシコ</span><span class="sxs-lookup"><span data-stu-id="5dbcd-160">Mexico</span></span>         | <span data-ttu-id="5dbcd-161">メキシコ CFDI (MX)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-161">Mexican CFDI (MX)</span></span>                    | <span data-ttu-id="5dbcd-162">売上請求書、梱包伝票、在庫振替、支払い補完、キャンセル</span><span class="sxs-lookup"><span data-stu-id="5dbcd-162">Sales invoices, packing slips, inventory transfers, payment complements, and cancellations</span></span> |
| <span data-ttu-id="5dbcd-163">オランダ</span><span class="sxs-lookup"><span data-stu-id="5dbcd-163">Netherlands</span></span>    | <span data-ttu-id="5dbcd-164">オランダ 電子請求書</span><span class="sxs-lookup"><span data-stu-id="5dbcd-164">Dutch electronic invoice (NL)</span></span>        | <span data-ttu-id="5dbcd-165">売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="5dbcd-165">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="5dbcd-166">ノルウェー</span><span class="sxs-lookup"><span data-stu-id="5dbcd-166">Norway</span></span>         | <span data-ttu-id="5dbcd-167">ノルウェー 電子請求書 (NO)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-167">Norwegian electronic invoice (NO)</span></span>    | <span data-ttu-id="5dbcd-168">売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="5dbcd-168">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="5dbcd-169">スペイン</span><span class="sxs-lookup"><span data-stu-id="5dbcd-169">Spain</span></span>          | <span data-ttu-id="5dbcd-170">スペイン 電子請求書 (ES)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-170">Spanish electronic invoice (ES)</span></span>      | <span data-ttu-id="5dbcd-171">売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="5dbcd-171">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="5dbcd-172">ヨーロッパ</span><span class="sxs-lookup"><span data-stu-id="5dbcd-172">Europe</span></span>         | <span data-ttu-id="5dbcd-173">PEPPOL 電子請求書</span><span class="sxs-lookup"><span data-stu-id="5dbcd-173">PEPPOL electronic invoice</span></span>            | <span data-ttu-id="5dbcd-174">PEPPOL 営業の請求書とプロジェクトの請求書</span><span class="sxs-lookup"><span data-stu-id="5dbcd-174">PEPPOL sales invoices and project invoices</span></span> |

### <a name="configurable-components-of-electronic-invoicing-features"></a><span data-ttu-id="5dbcd-175">電子請求機能のコ構成可能なコンポーネント</span><span class="sxs-lookup"><span data-stu-id="5dbcd-175">Configurable components of electronic invoicing features</span></span>

<span data-ttu-id="5dbcd-176">電子請求機能は、構成可能なコンポーネントの次のグループで構成されます。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-176">The electronic invoicing features consist of the following groups of configurable components:</span></span>

- <span data-ttu-id="5dbcd-177">**フォーマット** – フォーマットでは、電子ドキュメントが電子請求書になるときに電子請求で生成すべき項目を設定します。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-177">**Formats** – Formats let you configure what Electronic invoicing must generate when an electronic document becomes an electronic invoice.</span></span> <span data-ttu-id="5dbcd-178">形式には、電子請求書の形式構成や、外部の Web サービスとの通信が必要な場合にリクエストの送信やレスポンスの受信に使用するファイルやメッセージの形式設定などがあります。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-178">Formats include the format configuration for the electronic invoice, and for files and messages that are used to submit requests and receive responses when communication with an external web service is required.</span></span>
- <span data-ttu-id="5dbcd-179">**アクション** – アクションでは、Finance および Supply Chain Management が電子請求書に送信する電子ドキュメントの変換を電子請求で生成する方法を設定できます。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-179">**Actions** – Actions let you configure how Electronic invoicing generates the transformation of an electronic document that Finance and Supply Chain Management submitted into an electronic invoice.</span></span>
- <span data-ttu-id="5dbcd-180">**適合性ルール** – 適合性ルールでは、電子請求機能を処理するために電子請求で考慮すべきコンテキストを設定できます。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-180">**Applicability rules** – Applicability rules let you configure the context that Electronic invoicing must consider to process an electronic invoicing feature.</span></span>
- <span data-ttu-id="5dbcd-181">**変数** - 変数を使用すると、構成ロジックを構築するサポートを構成できます。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-181">**Variables** – Variables let you configure the support for the construction of the configuration logic.</span></span> <span data-ttu-id="5dbcd-182">変数は、特定のアクションを実行する際の値の入力として機能します。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-182">Variables can work as the input of values to perform a specific action.</span></span> <span data-ttu-id="5dbcd-183">あるいは、Finance および Supply Chain Management と電子請求間の値の交換としても機能します。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-183">Alternatively, they can work as an exchange of values between Finance and Supply Chain Management and Electronic invoicing.</span></span>
- <span data-ttu-id="5dbcd-184">**電子ドキュメント モデル マッピング** : 電子ドキュメント モデル マッピングを使用すると、ER モデル マッピングを構成できます。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-184">**Electronic document model mapping** – The electronic document model mapping lets you configure the ER model mapping.</span></span> <span data-ttu-id="5dbcd-185">モデル マッピングでは、電子ドキュメントが提出された際に、電子請求書に統合される抽象的な請求書のデータ マッピングを定義します。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-185">The model mapping defines the data mapping of the abstract invoice that is integrated into Electronic invoicing when electronic documents are submitted.</span></span>
- <span data-ttu-id="5dbcd-186">**請求書コンテキスト モデル** - 請求書コンテキスト モデルを使用すると、ER 請求書コンテキスト モデルを構成し、電子請求機能のコンテキストを定義できます。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-186">**Invoice context model** – The invoice context model lets you configure the ER invoice context model and define the context of an electronic invoicing feature.</span></span>
- <span data-ttu-id="5dbcd-187">**応答タイプ** – 応答タイプでは、電子請求書処理の結果として Finance および Supply Chain Management で更新される電子請求書を設定できます。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-187">**Response types** – Response types let you configure what Electronic invoicing must update in Finance and Supply Chain Management as a result of the electronic invoice processing.</span></span>

### <a name="formats"></a><span data-ttu-id="5dbcd-188">形式</span><span class="sxs-lookup"><span data-stu-id="5dbcd-188">Formats</span></span>

<span data-ttu-id="5dbcd-189">次の一覧は、電子請求機能に使用可能な ER 形式の構成を示しています。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-189">The following lists show the ER format configurations that are available for the electronic invoicing features.</span></span>

#### <a name="austrian-at-electronic-invoices-sales-and-project-invoices-for-austria"></a><span data-ttu-id="5dbcd-190">オーストリア (AT) 電子請求書 : オーストリア向け、売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="5dbcd-190">Austrian (AT) electronic invoices: Sales and project invoices for Austria</span></span>

- <span data-ttu-id="5dbcd-191">OIOUBL 売上請求書</span><span class="sxs-lookup"><span data-stu-id="5dbcd-191">OIOUBL Sales invoice</span></span>
- <span data-ttu-id="5dbcd-192">OIOUBL プロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="5dbcd-192">OIOUBL Project invoice</span></span>
- <span data-ttu-id="5dbcd-193">OIOUBL 売上訂正票</span><span class="sxs-lookup"><span data-stu-id="5dbcd-193">OIOUBL Sales credit note</span></span>
- <span data-ttu-id="5dbcd-194">OIOUBL プロジェクト訂正票</span><span class="sxs-lookup"><span data-stu-id="5dbcd-194">OIOUBL Project credit note</span></span>

#### <a name="belgian-be-electronic-invoice-sales-and-project-invoices-for-belgium"></a><span data-ttu-id="5dbcd-195">ベルギー (BE) 電子請求書 : ベルギー向け、売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="5dbcd-195">Belgian (BE) electronic invoice: Sales and project invoices for Belgium</span></span>

- <span data-ttu-id="5dbcd-196">UBL 売上請求書 BE</span><span class="sxs-lookup"><span data-stu-id="5dbcd-196">UBL Sales invoice BE</span></span>
- <span data-ttu-id="5dbcd-197">UBL プロジェクト請求書 BE</span><span class="sxs-lookup"><span data-stu-id="5dbcd-197">UBL Project invoice BE</span></span>
- <span data-ttu-id="5dbcd-198">UBL プロジェクト訂正票 BE</span><span class="sxs-lookup"><span data-stu-id="5dbcd-198">UBL Project credit note BE</span></span>
- <span data-ttu-id="5dbcd-199">UBL 売上訂正票 BE</span><span class="sxs-lookup"><span data-stu-id="5dbcd-199">UBL Sales credit note BE</span></span>

#### <a name="brazilian-br-nf-e-nf-e-federal-brazil"></a><span data-ttu-id="5dbcd-200">ブラジル (BR) NF-e: NF-e Federal (ブラジル)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-200">Brazilian (BR) NF-e: NF-e Federal (Brazil)</span></span>

- <span data-ttu-id="5dbcd-201">NF-e 送信エクスポートの形式 (BR)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-201">NF-e submit export format (BR)</span></span>
- <span data-ttu-id="5dbcd-202">NF-e 督促状エクスポートの形式 (BR)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-202">NF-e correction letter export format (BR)</span></span>
- <span data-ttu-id="5dbcd-203">NF-e キャンセル エクスポートの形式 (BR)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-203">NF-e cancel export format (BR)</span></span>
- <span data-ttu-id="5dbcd-204">NF-e 破棄エクスポートの形式 (BR)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-204">NF-e discard export format (BR)</span></span>

#### <a name="brazilian-nfs-e-br-nfs-e-abrasf-curitiba-city"></a><span data-ttu-id="5dbcd-205">ブラジル NFS-e (BR): NFS-e ABRASF クリチバ市</span><span class="sxs-lookup"><span data-stu-id="5dbcd-205">Brazilian NFS-e (BR): NFS-e ABRASF Curitiba city</span></span>

- <span data-ttu-id="5dbcd-206">NFS-e ABRASF クリチバ (BR)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-206">NFS-e ABRASF Curitiba (BR)</span></span>
- <span data-ttu-id="5dbcd-207">NFS-e ABRASF 調査書 クリチバ (BR)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-207">NFS-e ABRASF Inquire Curitiba (BR)</span></span>

#### <a name="danish-dk-electronic-invoice-sales-and-project-invoices-for-denmark"></a><span data-ttu-id="5dbcd-208">デンマーク (BE) 電子請求書 : デンマーク向け、売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="5dbcd-208">Danish (DK) electronic invoice: Sales and project invoices for Denmark</span></span>

- <span data-ttu-id="5dbcd-209">OIOUBL 売上請求書</span><span class="sxs-lookup"><span data-stu-id="5dbcd-209">OIOUBL Sales invoice</span></span>
- <span data-ttu-id="5dbcd-210">OIOUBL プロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="5dbcd-210">OIOUBL Project invoice</span></span>
- <span data-ttu-id="5dbcd-211">OIOUBL 売上訂正票</span><span class="sxs-lookup"><span data-stu-id="5dbcd-211">OIOUBL Sales credit note</span></span>
- <span data-ttu-id="5dbcd-212">OIOUBL プロジェクト訂正票</span><span class="sxs-lookup"><span data-stu-id="5dbcd-212">OIOUBL Project credit note</span></span>

#### <a name="dutch-nl-electronic-invoice-sales-and-project-invoices-for-netherlands"></a><span data-ttu-id="5dbcd-213">オランダ (NL) 電子請求書 : オランダ向け、売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="5dbcd-213">Dutch (NL) electronic invoice: Sales and project invoices for Netherlands</span></span>

- <span data-ttu-id="5dbcd-214">UBL 売上請求書 NL</span><span class="sxs-lookup"><span data-stu-id="5dbcd-214">UBL Sales invoice NL</span></span>
- <span data-ttu-id="5dbcd-215">UBL プロジェクト請求書 NL</span><span class="sxs-lookup"><span data-stu-id="5dbcd-215">UBL Project invoice NL</span></span>
- <span data-ttu-id="5dbcd-216">UBL プロジェクト訂正票 NL</span><span class="sxs-lookup"><span data-stu-id="5dbcd-216">UBL Project credit note NL</span></span>
- <span data-ttu-id="5dbcd-217">UBL 売上訂正票 NL</span><span class="sxs-lookup"><span data-stu-id="5dbcd-217">UBL Sales credit note NL</span></span>

#### <a name="egyptian-eg-electronic-invoice-sales-and-project-invoices-for-egypt"></a><span data-ttu-id="5dbcd-218">エジプト (BE) 電子請求書 : エジプト向け、売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="5dbcd-218">Egyptian (EG) electronic invoice: Sales and project invoices for Egypt</span></span>

- <span data-ttu-id="5dbcd-219">売上請求書(EG)(請求書)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-219">Sales invoice (EG)(Invoicing)</span></span>
- <span data-ttu-id="5dbcd-220">プロジェクト請求書(EG)(請求書)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-220">Project invoice (EG)(Invoicing)</span></span>

#### <a name="estonian-ee-electronic-invoice-sales-and-project-invoices-for-estonia"></a><span data-ttu-id="5dbcd-221">エストニア (BE) 電子請求書 : エストニア向け、売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="5dbcd-221">Estonian (EE) electronic invoice: Sales and project invoices for Estonia</span></span>

- <span data-ttu-id="5dbcd-222">売上請求書 (EE)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-222">Sales invoice (EE)</span></span>
- <span data-ttu-id="5dbcd-223">プロジェクト請求書 (EE)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-223">Project invoice (EE)</span></span>

#### <a name="finnish-fi-electronic-invoice-sales-and-project-invoices-for-finland"></a><span data-ttu-id="5dbcd-224">フィンランド (FI) 電子請求書 : フィンランド向け、売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="5dbcd-224">Finnish (FI) electronic invoice: Sales and project invoices for Finland</span></span>

- <span data-ttu-id="5dbcd-225">売上請求書 (FI)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-225">Sales invoice (FI)</span></span>
- <span data-ttu-id="5dbcd-226">プロジェクト請求書 (FI)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-226">Project invoice (FI)</span></span>

#### <a name="french-fr-electronic-invoice-sales-and-project-invoices-for-france"></a><span data-ttu-id="5dbcd-227">フランス (FR) 電子請求書 : フランス向け、売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="5dbcd-227">French (FR) electronic invoice: Sales and project invoices for France</span></span>

- <span data-ttu-id="5dbcd-228">UBL 売上請求書 FR</span><span class="sxs-lookup"><span data-stu-id="5dbcd-228">UBL Sales invoice FR</span></span>
- <span data-ttu-id="5dbcd-229">UBL プロジェクト請求書 FR</span><span class="sxs-lookup"><span data-stu-id="5dbcd-229">UBL Project invoice FR</span></span>
- <span data-ttu-id="5dbcd-230">UBL プロジェクト訂正票 FR</span><span class="sxs-lookup"><span data-stu-id="5dbcd-230">UBL Project credit note FR</span></span>
- <span data-ttu-id="5dbcd-231">UBL 売上訂正票 FR</span><span class="sxs-lookup"><span data-stu-id="5dbcd-231">UBL Sales credit note FR</span></span>

#### <a name="german-de-electronic-invoice-sales-and-project-invoices-for-germany"></a><span data-ttu-id="5dbcd-232">ドイツ (DE) 電子請求書 : ドイツ向け、売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="5dbcd-232">German (DE) electronic invoice: Sales and project invoices for Germany</span></span>

- <span data-ttu-id="5dbcd-233">売上請求書 (DE)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-233">Sales invoice (DE)</span></span>
- <span data-ttu-id="5dbcd-234">プロジェクト請求書 (DE)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-234">Project invoice (DE)</span></span>

#### <a name="italian-it-electronic-invoice-sales-and-project-invoices-for-italy"></a><span data-ttu-id="5dbcd-235">イタリア (IT) 電子請求書 : イタリア向け、売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="5dbcd-235">Italian (IT) electronic invoice: Sales and project invoices for Italy</span></span>

- <span data-ttu-id="5dbcd-236">売上請求書 (IT)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-236">Sales invoice (IT)</span></span>
- <span data-ttu-id="5dbcd-237">プロジェクト請求書 (IT)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-237">Project invoice (IT)</span></span>

#### <a name="mexican-mx-cfdi-cfdi-for-mexico"></a><span data-ttu-id="5dbcd-238">メキシコ (MX) CFDI: メキシコ向け CFDI</span><span class="sxs-lookup"><span data-stu-id="5dbcd-238">Mexican (MX) CFDI: CFDI for Mexico</span></span>

- <span data-ttu-id="5dbcd-239">CFDI 請求書フォーマット (MX)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-239">CFDI invoice format (MX)</span></span>
- <span data-ttu-id="5dbcd-240">CFDI 梱包明細 (MX)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-240">CFDI Packing slip (MX)</span></span>
- <span data-ttu-id="5dbcd-241">CFDI 在庫振替 (MX)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-241">CFDI Inventory transfer (MX)</span></span>
- <span data-ttu-id="5dbcd-242">CFDI 支払い形式 (MX)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-242">CFDI payment format (MX)</span></span>
- <span data-ttu-id="5dbcd-243">CFDI 請求書キャンセル形式 (MX)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-243">CFDI invoice cancel format (MX)</span></span>

#### <a name="norwegian-no-electronic-invoice-sales-and-project-invoices-for-norway"></a><span data-ttu-id="5dbcd-244">ノルウェー (BE) 電子請求書 : ノルウェー向け、売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="5dbcd-244">Norwegian (NO) electronic invoice: Sales and project invoices for Norway</span></span>

- <span data-ttu-id="5dbcd-245">OIOUBL 売上請求書</span><span class="sxs-lookup"><span data-stu-id="5dbcd-245">OIOUBL Sales invoice</span></span>
- <span data-ttu-id="5dbcd-246">OIOUBL プロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="5dbcd-246">OIOUBL Project invoice</span></span>
- <span data-ttu-id="5dbcd-247">OIOUBL 売上訂正票</span><span class="sxs-lookup"><span data-stu-id="5dbcd-247">OIOUBL Sales credit note</span></span>
- <span data-ttu-id="5dbcd-248">OIOUBL プロジェクト訂正票</span><span class="sxs-lookup"><span data-stu-id="5dbcd-248">OIOUBL Project credit note</span></span>

#### <a name="peppol-electronic-invoice-peppol-sales-and-project-invoices"></a><span data-ttu-id="5dbcd-249">PEPPOL 電子請求書 :PEPPOL 売上とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="5dbcd-249">PEPPOL electronic invoice: PEPPOL sales and project invoices</span></span>

- <span data-ttu-id="5dbcd-250">PEPPOL 売上請求書</span><span class="sxs-lookup"><span data-stu-id="5dbcd-250">PEPPOL Sales invoice</span></span>
- <span data-ttu-id="5dbcd-251">PEPPOL プロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="5dbcd-251">PEPPOL Project invoice</span></span>
- <span data-ttu-id="5dbcd-252">PEPPOL 売上訂正票</span><span class="sxs-lookup"><span data-stu-id="5dbcd-252">PEPPOL Sales credit note</span></span>
- <span data-ttu-id="5dbcd-253">PEPPOL プロジェクト訂正票</span><span class="sxs-lookup"><span data-stu-id="5dbcd-253">PEPPOL Project credit note</span></span>

#### <a name="spanish-es-electronic-invoice-sales-and-project-invoices-for-spain"></a><span data-ttu-id="5dbcd-254">スペイン (ES) 電子請求書 : スペイン向け、売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="5dbcd-254">Spanish (ES) electronic invoice: Sales and project invoices for Spain</span></span>

- <span data-ttu-id="5dbcd-255">売上請求書 (ES)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-255">Sales invoice (ES)</span></span>
- <span data-ttu-id="5dbcd-256">プロジェクト請求書 (ES)</span><span class="sxs-lookup"><span data-stu-id="5dbcd-256">Project invoice (ES)</span></span>

### <a name="actions"></a><span data-ttu-id="5dbcd-257">アクション</span><span class="sxs-lookup"><span data-stu-id="5dbcd-257">Actions</span></span>

<span data-ttu-id="5dbcd-258">次の表では、利用可能なアクションと、現在一般利用可能なのか、プレビュー段階であるのかを示しています。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-258">The following table lists the available actions, and whether they are currently generally available or still in preview.</span></span>

| <span data-ttu-id="5dbcd-259">操作</span><span class="sxs-lookup"><span data-stu-id="5dbcd-259">Action</span></span>                                        | <span data-ttu-id="5dbcd-260">説明</span><span class="sxs-lookup"><span data-stu-id="5dbcd-260">Description</span></span>                                                                  | <span data-ttu-id="5dbcd-261">適用の対象</span><span class="sxs-lookup"><span data-stu-id="5dbcd-261">Availability</span></span>         |
|-----------------------------------------------|------------------------------------------------------------------------------|----------------------|
| <span data-ttu-id="5dbcd-262">ドキュメントの変換</span><span class="sxs-lookup"><span data-stu-id="5dbcd-262">Transform document</span></span>                            | <span data-ttu-id="5dbcd-263">電子レポート形式を実行してドキュメントを変換します。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-263">Run Electronic Reporting format to transform the document.</span></span>                   | <span data-ttu-id="5dbcd-264">一般に入手可能</span><span class="sxs-lookup"><span data-stu-id="5dbcd-264">Generally available</span></span>  |
| <span data-ttu-id="5dbcd-265">xml ドキュメントへの署名</span><span class="sxs-lookup"><span data-stu-id="5dbcd-265">Sign xml document</span></span>                             | <span data-ttu-id="5dbcd-266">デジタル署名を使用して XML ドキュメントに署名します。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-266">Sign xml documents with digital signature.</span></span>                                   | <span data-ttu-id="5dbcd-267">プレビュー</span><span class="sxs-lookup"><span data-stu-id="5dbcd-267">In preview</span></span>           |
| <span data-ttu-id="5dbcd-268">エジプト税務当局に向けた json 文書に署名する</span><span class="sxs-lookup"><span data-stu-id="5dbcd-268">Sign json document for Egyptian Tax Authority</span></span> | <span data-ttu-id="5dbcd-269">エジプト税務局の電子署名で json 文書に署名します。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-269">Sign json documents with digital signature for Egyptian Tax Authority.</span></span>       | <span data-ttu-id="5dbcd-270">一般に入手可能</span><span class="sxs-lookup"><span data-stu-id="5dbcd-270">Generally available</span></span>  |
| <span data-ttu-id="5dbcd-271">エジプト ETA サービスとの統合</span><span class="sxs-lookup"><span data-stu-id="5dbcd-271">Integrate with Egyptian ETA service</span></span>           | <span data-ttu-id="5dbcd-272">エジプト税務当局とのやりとりを行います。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-272">Communicate with Egyptian Tax Authority.</span></span>                                     | <span data-ttu-id="5dbcd-273">一般に入手可能</span><span class="sxs-lookup"><span data-stu-id="5dbcd-273">Generally available</span></span>  |
| <span data-ttu-id="5dbcd-274">ブラジル SEFAZ サービスの呼び出し</span><span class="sxs-lookup"><span data-stu-id="5dbcd-274">Call Brazilian SEFAZ Service</span></span>                  | <span data-ttu-id="5dbcd-275">ブラジルの SEFAZ サービスと統合して会計書類を提出します。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-275">Integrate with Brazilian SEFAZ service for fiscal document submission.</span></span>       | <span data-ttu-id="5dbcd-276">プレビュー</span><span class="sxs-lookup"><span data-stu-id="5dbcd-276">In preview</span></span>           |
| <span data-ttu-id="5dbcd-277">メキシコ PAC サービスの呼び出し</span><span class="sxs-lookup"><span data-stu-id="5dbcd-277">Call Mexican PAC Service</span></span>                      | <span data-ttu-id="5dbcd-278">CFDI 提出に向けたメキシコ PAC サービスとの統合を行います。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-278">Integrate with Mexican PAC service for CFDI submission.</span></span>                      | <span data-ttu-id="5dbcd-279">プレビュー</span><span class="sxs-lookup"><span data-stu-id="5dbcd-279">In preview</span></span>           |
| <span data-ttu-id="5dbcd-280">応答の処理</span><span class="sxs-lookup"><span data-stu-id="5dbcd-280">Process response</span></span>                              | <span data-ttu-id="5dbcd-281">Web サービス コールから受信した応答を分析します。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-281">Analyze the response received from the web service call.</span></span>                     | <span data-ttu-id="5dbcd-282">一般に入手可能</span><span class="sxs-lookup"><span data-stu-id="5dbcd-282">Generally available</span></span>  |
| <span data-ttu-id="5dbcd-283">MS Power Automate を使用する</span><span class="sxs-lookup"><span data-stu-id="5dbcd-283">Use MS Power Automate</span></span>                         | <span data-ttu-id="5dbcd-284">Microsoft Power Automate に組み込まれたフローと統合します。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-284">Integrate with flow built in Microsoft Power Automate.</span></span>                       | <span data-ttu-id="5dbcd-285">プレビュー</span><span class="sxs-lookup"><span data-stu-id="5dbcd-285">In preview</span></span>           |

## <a name="configuration-providers"></a><span data-ttu-id="5dbcd-286">コンフィギュレーション提供者</span><span class="sxs-lookup"><span data-stu-id="5dbcd-286">Configuration providers</span></span>

<span data-ttu-id="5dbcd-287">構成プロバイダーは、電子請求書発行機能とその ER コンポーネント (モデル マッピング、フォーマット構成、コンテキスト モデルなど) を提供します。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-287">Configuration providers provide the electronic invoicing features and their ER components, such as the model mapping, format configuration, and context model.</span></span> <span data-ttu-id="5dbcd-288">関連するグローバル リポジトリで電子請求書発行機能と ER コンポーネントが公開されています。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-288">They publish the electronic invoicing features and ER components in the associated Global repository.</span></span> <span data-ttu-id="5dbcd-289">そこから他の組織がダウンロードできるようになっています。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-289">From there, other organizations can download them.</span></span>

<span data-ttu-id="5dbcd-290">RCS を介した電子請求書発行機能の構成を行う前に、 **電子レポート** モジュールの構成プロバイダーに独自の組織を構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-290">Before you configure the electronic invoicing features through RCS, you must configure your own organization as a configuration provider in the **Electronic reporting** module.</span></span> <span data-ttu-id="5dbcd-291">構成プロバイダーを **有効化** に設定する方法については、[構成プロバイダーを作成して有効化としてマークする](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-291">For information about how to set a configuration provider to **Active**, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="viewing-electronic-invoicing-features-in-the-global-repository"></a><span data-ttu-id="5dbcd-292">グローバル リポジトリでの電子請求機能を表示する</span><span class="sxs-lookup"><span data-stu-id="5dbcd-292">Viewing electronic invoicing features in the Global repository</span></span>

<span data-ttu-id="5dbcd-293">特定の構成プロバイダのグローバル リポジトリで利用可能な電子請求書発行機能を閲覧するには、組織の RCS インスタンスを同期します。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-293">To browse the electronic invoicing features that are available in the Global repository for a specific configuration provider, sync your organization's RCS instance.</span></span> <span data-ttu-id="5dbcd-294">同期が完了すると、使用可能な電子請求機能の一覧が更新されます。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-294">After synchronization is completed, the list of available electronic invoicing features is updated.</span></span>

## <a name="importing-electronic-invoicing-features"></a><span data-ttu-id="5dbcd-295">電子請求書機能のインポート</span><span class="sxs-lookup"><span data-stu-id="5dbcd-295">Importing electronic invoicing features</span></span>

<span data-ttu-id="5dbcd-296">電子請求機能を使用・構成する前に、組織の RCS インスタンスにインポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-296">Before you use or configure the electronic invoicing features, you must import them into your organization's RCS instance.</span></span> <span data-ttu-id="5dbcd-297">インポート操作により、機能のローカル コピーが作成され、機能で使用する ER コンポーネント (構成やモデル構成の書式設定など) が組織の RCS インスタンスにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-297">The import operation creates a local copy of the features and copies all the ER artifacts that the features use (for example, format configurations and model configurations) to your organization's RCS instance.</span></span>

<span data-ttu-id="5dbcd-298">任意の構成プロバイダから電子請求機能をインポートできます。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-298">You can import the electronic invoicing features from any configuration provider.</span></span>

## <a name="creating-electronic-invoicing-features"></a><span data-ttu-id="5dbcd-299">電子請求書機能の作成</span><span class="sxs-lookup"><span data-stu-id="5dbcd-299">Creating electronic invoicing features</span></span>

<span data-ttu-id="5dbcd-300">ゼロから電子請求書機能を作成することも、別の電子請求書機能から派生させることもできます。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-300">You can create an electronic invoicing feature from scratch, or you can derive it from another electronic invoicing feature.</span></span>

<span data-ttu-id="5dbcd-301">電子請求機能を最初から作成する場合は、ER コンポーネントを手動で追加する必要があります (機能バージョンの構成や、機能バージョンの設定やアプリケーションの設定などのその他構成など)。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-301">When you create an electronic invoicing feature from scratch, you must manually add the ER components (for example, feature version configurations and other configurations, such as the feature version setup and application setup).</span></span> <span data-ttu-id="5dbcd-302">別の機能から派生させて機能を作成した場合、この新しい機能は元の機能からすべての構成を引き継ぎます。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-302">When you create a feature by deriving it from another feature, the new feature inherits all configurations from the original.</span></span> 

## <a name="electronic-invoicing-feature-version"></a><span data-ttu-id="5dbcd-303">電子請求書機能のバージョン</span><span class="sxs-lookup"><span data-stu-id="5dbcd-303">Electronic invoicing feature version</span></span>

<span data-ttu-id="5dbcd-304">電子請求書機能の機能はバージョン管理されています。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-304">The electronic invoicing features are versioned.</span></span> <span data-ttu-id="5dbcd-305">新しいバージョンを作成すると、バージョン番号が自動的に増番で付与されます。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-305">When a new version is created, the version number is automatically incremented.</span></span> <span data-ttu-id="5dbcd-306">新しいバージョンの"有効開始日" を定義できます。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-306">An "effective from" date can be defined for the new version.</span></span>

<span data-ttu-id="5dbcd-307">電子請求機能のバージョンは、最大で 3 つのステータスを持つライフサイクルに従います。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-307">Electronic invoicing feature versions follow a lifecycle that has up to three statuses:</span></span>

- <span data-ttu-id="5dbcd-308">**下書き** - 機能バージョンがこのステータスにある場合、構成の属性とそのコンポーネント (ファイル形式の構成など)を編集できます。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-308">**Draft** – If a feature version is in this status, you can edit its configuration attributes and any of its artifacts (for example, file format configurations).</span></span>
- <span data-ttu-id="5dbcd-309">**完了** - 機能のバージョンがこのステータスの場合は、組織に関連付けられているグローバル リポジトリに公開されている状態を表わします。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-309">**Complete** – If a feature version is in this status, it has been published to the Global repository that is associated with your organization.</span></span> <span data-ttu-id="5dbcd-310">機能のバージョン、または ER コンポーネントの編集はできなくなります。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-310">You can no longer edit the feature version or any of the ER components.</span></span>
- <span data-ttu-id="5dbcd-311">**公開済み** – 機能のバージョンがこのステータスである場合、電子請求に公開されています。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-311">**Published** – If a feature version is in this status, it has been published to Electronic invoicing.</span></span> <span data-ttu-id="5dbcd-312">機能のバージョン、または ER コンポーネントの編集はできなくなります。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-312">You can no longer edit the feature version or any of the ER components.</span></span>

### <a name="feature-configurations"></a><span data-ttu-id="5dbcd-313">機能の構成</span><span class="sxs-lookup"><span data-stu-id="5dbcd-313">Feature configurations</span></span>

<span data-ttu-id="5dbcd-314">機能の構成には、電子請求機能で使用する ER 形式のすべての構成が保持されます。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-314">Feature configurations hold all the ER format configurations that the electronic invoicing features use.</span></span> <span data-ttu-id="5dbcd-315">電子請求書発行機能が処理中に使用するすべての電子ファイルは、その機能の構成に追加されたフォーマット構成に由来します。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-315">All the electronic files that an electronic invoicing feature uses during processing come from the format configurations that have been added to the feature configurations of that feature.</span></span>

<span data-ttu-id="5dbcd-316">ER 形式デザイナには、機能の構成からアクセスできます。ER 形式デザイナは、形式の構成を作成するために使用する ER ツールです。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-316">From the feature configurations, you can access the ER format designer, which is the ER tool that is used to create format configurations.</span></span>

### <a name="feature-setup"></a><span data-ttu-id="5dbcd-317">機能設定</span><span class="sxs-lookup"><span data-stu-id="5dbcd-317">Feature setup</span></span>

<span data-ttu-id="5dbcd-318">機能の設定は、機能ノ構成と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-318">Feature setups are used in combination with feature configurations.</span></span> <span data-ttu-id="5dbcd-319">各機能設定は、電子請求書機能が電子請求書の特定の要件を満たせるように、期待される動作を提供するアクション、適用ルール、および変数のセットをカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-319">Each feature setup encapsulates a set of actions, applicability rules, and variables that provide the expected behavior so that an electronic invoicing feature can meet a specific requirement of the electronic invoice.</span></span>

### <a name="application-setup"></a><span data-ttu-id="5dbcd-320">アプリケーションの設定</span><span class="sxs-lookup"><span data-stu-id="5dbcd-320">Application setup</span></span>

<span data-ttu-id="5dbcd-321">アプリケーションの設定は、既に作成した接続されたアプリケーションに関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-321">The application setup must be associated with a previously created connected application.</span></span>

<span data-ttu-id="5dbcd-322">アプリケーションの設定を通じて Finance と Supply Chain Management で行う必要がある電子請求機能の一部を構成できます。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-322">Through the application setup, you can configure the part of an electronic invoicing feature that must be done in Finance and Supply Chain Management.</span></span> <span data-ttu-id="5dbcd-323">構成可能なコンポーネントは、電子請求の機能を問わず、少なくとも 3 つ必要となります。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-323">At least three configurable components are mandatory, regardless of the electronic invoicing feature:</span></span>

- <span data-ttu-id="5dbcd-324">**テーブル名** : 転記された請求書を保持している、Finance と Supply Chain Management のエンティティ、電子請求書機能がベースになっています。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-324">**Table name** – The entity in Finance and Supply Chain Management that holds the posted invoices, and that the electronic invoicing feature is based on.</span></span>
- <span data-ttu-id="5dbcd-325">**コンテキスト** - ER を介して構成された請求書コンテキスト モデルの名前です。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-325">**Context** – The name of the invoice context model that was configured through ER.</span></span>
- <span data-ttu-id="5dbcd-326">**ビジネス ドキュメント マッピング** - ER を介して構成された請求書マッピング モデルの名前です。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-326">**Business document mapping** – The name of the invoice mapping model that was configured through ER.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5dbcd-327">アプリケーションの設定で入力された構成は、Finance と Supply Chain Management で表示できます。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-327">The configuration that is entered in the application setup can be viewed in Finance and Supply Chain Management.</span></span> <span data-ttu-id="5dbcd-328">**組織管理 \> 設定 \> 電子ドキュメント パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-328">Go to **Organization administration \> Setup \> Electronic document parameter**.</span></span> <span data-ttu-id="5dbcd-329">**電子ドキュメント** タブ で、**デプロイ** を選択し、**接続済みアプリケーション** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-329">On the **Electronic document** tab, select **Deploy**, and then select the **Connected application** option.</span></span>

### <a name="deploying-feature-versions"></a><span data-ttu-id="5dbcd-330">デプロイ機能のバージョン</span><span class="sxs-lookup"><span data-stu-id="5dbcd-330">Deploying feature versions</span></span>

<span data-ttu-id="5dbcd-331">RCS では、**デプロイ** コマンドを使用して電子請求機能のバージョンを target-publish します。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-331">In RCS, you use the **Deploy** command to target-publish an electronic invoicing feature version.</span></span> <span data-ttu-id="5dbcd-332">**デプロイ** を選択し、次のいずれかのオプションを選択して、デプロイするターゲットを定義します。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-332">Select **Deploy**, and then select one of the following options to define the target of the deployment:</span></span> 

- <span data-ttu-id="5dbcd-333">**サービス環境** - デプロイのターゲットがサービス環境の場合は、電子請求機能のバージョンをサービス環境に公開します。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-333">**Service environment** – When the target of the deployment is the service environment, the electronic invoicing feature version is published to the service environment.</span></span> <span data-ttu-id="5dbcd-334">これにより、電子請求で Finance および Supply Chain Management が送信する電子ドキュメントを受信して処理することができます。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-334">Electronic invoicing is then ready to receive and process electronic documents that Finance and Supply Chain Management send.</span></span>
- <span data-ttu-id="5dbcd-335">**接続済アプリケーション** - デプロイのターゲットが接続されたアプリケーションである場合、アプリケーションの設定で提供される構成は、以前に関連付けらた Finance と Supply Chain Management のインスタンスに記述されます。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-335">**Connected application** – When the target of the deployment is the connected application, the configuration that is provided by the application setup is written in the Finance and Supply Chain Management instance that was previously associated with it.</span></span>

<span data-ttu-id="5dbcd-336">サービス環境や接続されたアプリケーションにデプロイできるバージョンは、ステータスが **完了** となっておる電子請求機能のバージョンのみです。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-336">Only electronic invoicing feature versions that have a status of **Completed** can be deployed to either a service environment or a connected application.</span></span>

### <a name="removing-feature-versions"></a><span data-ttu-id="5dbcd-337">機能のバージョンを削除する</span><span class="sxs-lookup"><span data-stu-id="5dbcd-337">Removing feature versions</span></span>

<span data-ttu-id="5dbcd-338">RCS では、**Undeploy** コマンドを使用して、電子請求のサービス環境から特定の電子請求機能のバージョンを削除します。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-338">In RCS, you use the **Undeploy** command to remove a specific electronic invoicing feature version from a service environment in Electronic invoicing.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5dbcd-339">**アンデプロイ** コマンドは、サービス環境でのみ機能します。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-339">The **Undeploy** command works only in service environments.</span></span> <span data-ttu-id="5dbcd-340">接続されたアプリケーションからは、電子請求機能のバージョンは削除されません。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-340">It doesn't remove electronic invoicing feature versions from connected applications.</span></span>

### <a name="rebasing-electronic-invoicing-features"></a><span data-ttu-id="5dbcd-341">電子請求書発行機能をリベースする</span><span class="sxs-lookup"><span data-stu-id="5dbcd-341">Rebasing electronic invoicing features</span></span>

<span data-ttu-id="5dbcd-342">電子請求書の作成機能が別の機能から派生したものである場合、**リベース** コマンドを使用すると、この派生した機能を元の機能に導入された変更を基に更新します。</span><span class="sxs-lookup"><span data-stu-id="5dbcd-342">When one electronic invoicing feature is derived from another, the **Rebase** command updates the derived feature with the changes that have been introduced in the original feature.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5dbcd-343">追加リソース</span><span class="sxs-lookup"><span data-stu-id="5dbcd-343">Additional resources</span></span>

- [<span data-ttu-id="5dbcd-344">Finance および Supply Chain Management で電子請求書を発行する</span><span class="sxs-lookup"><span data-stu-id="5dbcd-344">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
