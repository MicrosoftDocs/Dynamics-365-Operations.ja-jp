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
ms.openlocfilehash: d7945cc899cf161f294dfcc3f6d1a9a79c9453ab
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897723"
---
# <a name="configure-electronic-invoicing-in-regulatory-configuration-services-rcs"></a><span data-ttu-id="0611e-103">Regulatory Configuration Services (RCS) から電子請求書を設定する</span><span class="sxs-lookup"><span data-stu-id="0611e-103">Configure Electronic invoicing in Regulatory Configuration Services (RCS)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0611e-104">このトピックでは、Dynamics 365 Regulatory Configuration Services (RCS) で電子請求書を設定する機能に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="0611e-104">This topic provides information about the configuration capabilities of Electronic invoicing in Dynamics 365 Regulatory Configuration Services (RCS).</span></span>

<span data-ttu-id="0611e-105">設定機能により、コーディングを行わずに、電子請求書に関するビジネスや規制の要件を満たすことができる電子請求を使うことができます。</span><span class="sxs-lookup"><span data-stu-id="0611e-105">It is through the configuration capabilities that Electronic invoicing helps you meet business and regulatory requirements of electronic invoices without having to do any coding.</span></span> <span data-ttu-id="0611e-106">また、Webサービスで電子請求書を電子的に承認する必要がある場合は、この構成機能を使用して、コードを実行せずに Web サービスとメッセージを交換する要件を満たすことができます。</span><span class="sxs-lookup"><span data-stu-id="0611e-106">And in the scenarios where electronic invoices must be electronically approved by a web services, the configuration capabilities also help you meet the requirements for exchanging messages with a web services, without doing any code.</span></span>

## <a name="electronic-reporting"></a><span data-ttu-id="0611e-107">電子申告</span><span class="sxs-lookup"><span data-stu-id="0611e-107">Electronic reporting</span></span>

<span data-ttu-id="0611e-108">電子申告 (ER) は電子請求をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="0611e-108">Electronic reporting (ER) supports Electronic invoicing.</span></span>

<span data-ttu-id="0611e-109">データ モデルのマッピングとフォーマットは、ER で作成および維持される構成可能なコンポーネントであり、電子請求で使用されます。</span><span class="sxs-lookup"><span data-stu-id="0611e-109">The data model mapping and formats are configurable components that are created and maintained through ER and used in Electronic invoicing.</span></span> <span data-ttu-id="0611e-110">ER 形式デザイナは、ファイルの形式を作成・管理するためのツールです。</span><span class="sxs-lookup"><span data-stu-id="0611e-110">The ER format designer is the tool for creating and maintaining file formats.</span></span> <span data-ttu-id="0611e-111">これは、電子請求機能の構成に使用されます。</span><span class="sxs-lookup"><span data-stu-id="0611e-111">It's used to configure the electronic invoicing features.</span></span>

<span data-ttu-id="0611e-112">詳細については、[電子申告 (ER) の概要](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0611e-112">For more information, see [Electronic reporting (ER) overview](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).</span></span>

## <a name="electronic-invoicing-features"></a><span data-ttu-id="0611e-113">電子請求の機能</span><span class="sxs-lookup"><span data-stu-id="0611e-113">Electronic invoicing features</span></span>

<span data-ttu-id="0611e-114">電子請求機能で、電子請求を通じて電子請求書を生成することができます。</span><span class="sxs-lookup"><span data-stu-id="0611e-114">The electronic invoicing features are responsible for generating electronic invoices through Electronic invoicing.</span></span> <span data-ttu-id="0611e-115">これにより設定ルールがカプセル化され、Microsoft Dynamics 365 Finance と Dynamics 365 Supply Chain Management が電子請求および電子請求書に送信するデータを処理するために使用します。</span><span class="sxs-lookup"><span data-stu-id="0611e-115">They encapsulate the configuration rules and use them to process the data that Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management send to Electronic invoicing and to electronic invoices.</span></span>

<span data-ttu-id="0611e-116">この機能はまた、ファイル形式の仕様に準拠する必要があり、出力はスタンドアロンの電子ファイルのシナリオにも対応しています。</span><span class="sxs-lookup"><span data-stu-id="0611e-116">The features also support scenarios where compliance with file format specifications is required and the output is a standalone electronic file.</span></span> <span data-ttu-id="0611e-117">ほとんどの場合、指定のファイル形式は税務当局が公開しています。</span><span class="sxs-lookup"><span data-stu-id="0611e-117">In most cases, the file format specifications are published by the tax authority.</span></span>

<span data-ttu-id="0611e-118">また、税務当局や認定当事者によってホストされる外部の Web サービスとのメッセージ交換や、電子請求書での認証または承認スタンプの要求に対応しています。</span><span class="sxs-lookup"><span data-stu-id="0611e-118">Finally, the features support the exchange of messages with external web services that are hosted either by the tax authority or by some accredited party, and requests for authorization or an approval stamp in the electronic invoice.</span></span>

### <a name="availability-of-electronic-invoicing-features"></a><span data-ttu-id="0611e-119">電子請求機能の可用性</span><span class="sxs-lookup"><span data-stu-id="0611e-119">Availability of electronic invoicing features</span></span>

<span data-ttu-id="0611e-120">電子請求機能の可用性は、国または地域によって異なります。</span><span class="sxs-lookup"><span data-stu-id="0611e-120">Availability of the electronic invoicing features depends on the country or region.</span></span> <span data-ttu-id="0611e-121">一般公開されている機能もありますが、プレビュー段階の機能もあります。</span><span class="sxs-lookup"><span data-stu-id="0611e-121">Although some features are generally available, others are in preview.</span></span>

#### <a name="generally-available-features"></a><span data-ttu-id="0611e-122">一般公開されている機能</span><span class="sxs-lookup"><span data-stu-id="0611e-122">Generally available features</span></span>

<span data-ttu-id="0611e-123">次の表に、一般公開されている電子請求機能を示しています。</span><span class="sxs-lookup"><span data-stu-id="0611e-123">The following table shows the electronic invoicing features that are generally available.</span></span>

| <span data-ttu-id="0611e-124">国/地域</span><span class="sxs-lookup"><span data-stu-id="0611e-124">Country/region</span></span> | <span data-ttu-id="0611e-125">機能名</span><span class="sxs-lookup"><span data-stu-id="0611e-125">Feature name</span></span>                         | <span data-ttu-id="0611e-126">ビジネス ドキュメント</span><span class="sxs-lookup"><span data-stu-id="0611e-126">Business document</span></span> |
|----------------|--------------------------------------|-------------------|
| <span data-ttu-id="0611e-127">エジプト</span><span class="sxs-lookup"><span data-stu-id="0611e-127">Egypt</span></span>          | <span data-ttu-id="0611e-128">エジプト 電子請求書 (EG)</span><span class="sxs-lookup"><span data-stu-id="0611e-128">Egyptian electronic invoice (EG)</span></span> | <span data-ttu-id="0611e-129">売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="0611e-129">Sales invoices and project invoices</span></span> |

#### <a name="preview-features"></a><span data-ttu-id="0611e-130">プレビュー機能</span><span class="sxs-lookup"><span data-stu-id="0611e-130">Preview features</span></span>

<span data-ttu-id="0611e-131">次の表に、現在プレビュー中の電子請求機能をまとめています。</span><span class="sxs-lookup"><span data-stu-id="0611e-131">The following table shows the electronic invoicing features that are currently in preview.</span></span>

| <span data-ttu-id="0611e-132">国/地域</span><span class="sxs-lookup"><span data-stu-id="0611e-132">Country/region</span></span> | <span data-ttu-id="0611e-133">機能名</span><span class="sxs-lookup"><span data-stu-id="0611e-133">Feature name</span></span>                         | <span data-ttu-id="0611e-134">ビジネス ドキュメント</span><span class="sxs-lookup"><span data-stu-id="0611e-134">Business document</span></span> |
|----------------|--------------------------------------|-------------------|
| <span data-ttu-id="0611e-135">オーストリア</span><span class="sxs-lookup"><span data-stu-id="0611e-135">Austria</span></span>        | <span data-ttu-id="0611e-136">オーストリア 顧客電子請求書 (AT)</span><span class="sxs-lookup"><span data-stu-id="0611e-136">Austrian electronic invoices (AT)</span></span>    | <span data-ttu-id="0611e-137">売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="0611e-137">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="0611e-138">ベルギー</span><span class="sxs-lookup"><span data-stu-id="0611e-138">Belgium</span></span>        | <span data-ttu-id="0611e-139">ベルギー 電子請求書 (BE)</span><span class="sxs-lookup"><span data-stu-id="0611e-139">Belgian electronic invoice (BE)</span></span>      | <span data-ttu-id="0611e-140">売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="0611e-140">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="0611e-141">ブラジル</span><span class="sxs-lookup"><span data-stu-id="0611e-141">Brazil</span></span>         | <span data-ttu-id="0611e-142">ブラジル NF-e (BR)</span><span class="sxs-lookup"><span data-stu-id="0611e-142">Brazilian NF-e (BR)</span></span>                  | <span data-ttu-id="0611e-143">財政文書モデル 55、督促状、取消書、廃棄物</span><span class="sxs-lookup"><span data-stu-id="0611e-143">Fiscal document model 55, correction letters, cancellations, and discards</span></span> |
| <span data-ttu-id="0611e-144">ブラジル</span><span class="sxs-lookup"><span data-stu-id="0611e-144">Brazil</span></span>         | <span data-ttu-id="0611e-145">ブラジル NFS-e ABRASF クリチバ (BR)</span><span class="sxs-lookup"><span data-stu-id="0611e-145">Brazilian NFS-e ABRASF Curitiba (BR)</span></span> | <span data-ttu-id="0611e-146">会計ドキュメントのサービス</span><span class="sxs-lookup"><span data-stu-id="0611e-146">Service fiscal documents</span></span> |
| <span data-ttu-id="0611e-147">デンマーク</span><span class="sxs-lookup"><span data-stu-id="0611e-147">Denmark</span></span>        | <span data-ttu-id="0611e-148">デンマーク 電子請求書 (DK)</span><span class="sxs-lookup"><span data-stu-id="0611e-148">Danish electronic invoice (DK)</span></span>       | <span data-ttu-id="0611e-149">売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="0611e-149">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="0611e-150">エストニア</span><span class="sxs-lookup"><span data-stu-id="0611e-150">Estonia</span></span>        | <span data-ttu-id="0611e-151">エストニア 電子請求書 (EE)</span><span class="sxs-lookup"><span data-stu-id="0611e-151">Estonian electronic invoice (EE)</span></span>     | <span data-ttu-id="0611e-152">売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="0611e-152">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="0611e-153">フィンランド</span><span class="sxs-lookup"><span data-stu-id="0611e-153">Finland</span></span>        | <span data-ttu-id="0611e-154">フィンランド 電子請求書 (FI)</span><span class="sxs-lookup"><span data-stu-id="0611e-154">Finnish electronic invoice (FI)</span></span>      | <span data-ttu-id="0611e-155">売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="0611e-155">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="0611e-156">フランス</span><span class="sxs-lookup"><span data-stu-id="0611e-156">France</span></span>         | <span data-ttu-id="0611e-157">フランス 電子請求書 (FR)</span><span class="sxs-lookup"><span data-stu-id="0611e-157">French electronic invoice (FR)</span></span>       | <span data-ttu-id="0611e-158">売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="0611e-158">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="0611e-159">ドイツ</span><span class="sxs-lookup"><span data-stu-id="0611e-159">Germany</span></span>        | <span data-ttu-id="0611e-160">ドイツ 電子請求書 (DE)</span><span class="sxs-lookup"><span data-stu-id="0611e-160">German electronic invoice (DE)</span></span>       | <span data-ttu-id="0611e-161">売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="0611e-161">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="0611e-162">イタリア</span><span class="sxs-lookup"><span data-stu-id="0611e-162">Italy</span></span>          | <span data-ttu-id="0611e-163">FatturaPA (IT)</span><span class="sxs-lookup"><span data-stu-id="0611e-163">FatturaPA (IT)</span></span>                       | <span data-ttu-id="0611e-164">売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="0611e-164">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="0611e-165">メキシコ</span><span class="sxs-lookup"><span data-stu-id="0611e-165">Mexico</span></span>         | <span data-ttu-id="0611e-166">メキシコ CFDI (MX)</span><span class="sxs-lookup"><span data-stu-id="0611e-166">Mexican CFDI (MX)</span></span>                    | <span data-ttu-id="0611e-167">売上請求書、梱包伝票、在庫振替、支払い補完、キャンセル</span><span class="sxs-lookup"><span data-stu-id="0611e-167">Sales invoices, packing slips, inventory transfers, payment complements, and cancellations</span></span> |
| <span data-ttu-id="0611e-168">オランダ</span><span class="sxs-lookup"><span data-stu-id="0611e-168">Netherlands</span></span>    | <span data-ttu-id="0611e-169">オランダ 電子請求書</span><span class="sxs-lookup"><span data-stu-id="0611e-169">Dutch electronic invoice (NL)</span></span>        | <span data-ttu-id="0611e-170">売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="0611e-170">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="0611e-171">ノルウェー</span><span class="sxs-lookup"><span data-stu-id="0611e-171">Norway</span></span>         | <span data-ttu-id="0611e-172">ノルウェー 電子請求書 (NO)</span><span class="sxs-lookup"><span data-stu-id="0611e-172">Norwegian electronic invoice (NO)</span></span>    | <span data-ttu-id="0611e-173">売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="0611e-173">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="0611e-174">スペイン</span><span class="sxs-lookup"><span data-stu-id="0611e-174">Spain</span></span>          | <span data-ttu-id="0611e-175">スペイン 電子請求書 (ES)</span><span class="sxs-lookup"><span data-stu-id="0611e-175">Spanish electronic invoice (ES)</span></span>      | <span data-ttu-id="0611e-176">売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="0611e-176">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="0611e-177">ヨーロッパ</span><span class="sxs-lookup"><span data-stu-id="0611e-177">Europe</span></span>         | <span data-ttu-id="0611e-178">PEPPOL 電子請求書</span><span class="sxs-lookup"><span data-stu-id="0611e-178">PEPPOL electronic invoice</span></span>            | <span data-ttu-id="0611e-179">PEPPOL 営業の請求書とプロジェクトの請求書</span><span class="sxs-lookup"><span data-stu-id="0611e-179">PEPPOL sales invoices and project invoices</span></span> |

### <a name="configurable-components-of-electronic-invoicing-features"></a><span data-ttu-id="0611e-180">電子請求機能のコ構成可能なコンポーネント</span><span class="sxs-lookup"><span data-stu-id="0611e-180">Configurable components of electronic invoicing features</span></span>

<span data-ttu-id="0611e-181">電子請求機能は、構成可能なコンポーネントの次のグループで構成されます。</span><span class="sxs-lookup"><span data-stu-id="0611e-181">The electronic invoicing features consist of the following groups of configurable components:</span></span>

- <span data-ttu-id="0611e-182">**フォーマット** – フォーマットでは、電子ドキュメントが電子請求書になるときに電子請求で生成すべき項目を設定します。</span><span class="sxs-lookup"><span data-stu-id="0611e-182">**Formats** – Formats let you configure what Electronic invoicing must generate when an electronic document becomes an electronic invoice.</span></span> <span data-ttu-id="0611e-183">形式には、電子請求書の形式構成や、外部の Web サービスとの通信が必要な場合にリクエストの送信やレスポンスの受信に使用するファイルやメッセージの形式設定などがあります。</span><span class="sxs-lookup"><span data-stu-id="0611e-183">Formats include the format configuration for the electronic invoice, and for files and messages that are used to submit requests and receive responses when communication with an external web service is required.</span></span>
- <span data-ttu-id="0611e-184">**アクション** – アクションでは、Finance および Supply Chain Management が電子請求書に送信する電子ドキュメントの変換を電子請求で生成する方法を設定できます。</span><span class="sxs-lookup"><span data-stu-id="0611e-184">**Actions** – Actions let you configure how Electronic invoicing generates the transformation of an electronic document that Finance and Supply Chain Management submitted into an electronic invoice.</span></span>
- <span data-ttu-id="0611e-185">**適合性ルール** – 適合性ルールでは、電子請求機能を処理するために電子請求で考慮すべきコンテキストを設定できます。</span><span class="sxs-lookup"><span data-stu-id="0611e-185">**Applicability rules** – Applicability rules let you configure the context that Electronic invoicing must consider to process an electronic invoicing feature.</span></span>
- <span data-ttu-id="0611e-186">**変数** - 変数を使用すると、構成ロジックを構築するサポートを構成できます。</span><span class="sxs-lookup"><span data-stu-id="0611e-186">**Variables** – Variables let you configure the support for the construction of the configuration logic.</span></span> <span data-ttu-id="0611e-187">変数は、特定のアクションを実行する際の値の入力として機能します。</span><span class="sxs-lookup"><span data-stu-id="0611e-187">Variables can work as the input of values to perform a specific action.</span></span> <span data-ttu-id="0611e-188">あるいは、Finance および Supply Chain Management と電子請求間の値の交換としても機能します。</span><span class="sxs-lookup"><span data-stu-id="0611e-188">Alternatively, they can work as an exchange of values between Finance and Supply Chain Management and Electronic invoicing.</span></span>
- <span data-ttu-id="0611e-189">**電子ドキュメント モデル マッピング** : 電子ドキュメント モデル マッピングを使用すると、ER モデル マッピングを構成できます。</span><span class="sxs-lookup"><span data-stu-id="0611e-189">**Electronic document model mapping** – The electronic document model mapping lets you configure the ER model mapping.</span></span> <span data-ttu-id="0611e-190">モデル マッピングでは、電子ドキュメントが提出された際に、電子請求書に統合される抽象的な請求書のデータ マッピングを定義します。</span><span class="sxs-lookup"><span data-stu-id="0611e-190">The model mapping defines the data mapping of the abstract invoice that is integrated into Electronic invoicing when electronic documents are submitted.</span></span>
- <span data-ttu-id="0611e-191">**請求書コンテキスト モデル** - 請求書コンテキスト モデルを使用すると、ER 請求書コンテキスト モデルを構成し、電子請求機能のコンテキストを定義できます。</span><span class="sxs-lookup"><span data-stu-id="0611e-191">**Invoice context model** – The invoice context model lets you configure the ER invoice context model and define the context of an electronic invoicing feature.</span></span>
- <span data-ttu-id="0611e-192">**応答タイプ** – 応答タイプでは、電子請求書処理の結果として Finance および Supply Chain Management で更新される電子請求書を設定できます。</span><span class="sxs-lookup"><span data-stu-id="0611e-192">**Response types** – Response types let you configure what Electronic invoicing must update in Finance and Supply Chain Management as a result of the electronic invoice processing.</span></span>

### <a name="formats"></a><span data-ttu-id="0611e-193">形式</span><span class="sxs-lookup"><span data-stu-id="0611e-193">Formats</span></span>

<span data-ttu-id="0611e-194">次の一覧は、電子請求機能に使用可能な ER 形式の構成を示しています。</span><span class="sxs-lookup"><span data-stu-id="0611e-194">The following lists show the ER format configurations that are available for the electronic invoicing features.</span></span>

#### <a name="austrian-at-electronic-invoices-sales-and-project-invoices-for-austria"></a><span data-ttu-id="0611e-195">オーストリア (AT) 電子請求書 : オーストリア向け、売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="0611e-195">Austrian (AT) electronic invoices: Sales and project invoices for Austria</span></span>

- <span data-ttu-id="0611e-196">OIOUBL 売上請求書</span><span class="sxs-lookup"><span data-stu-id="0611e-196">OIOUBL Sales invoice</span></span>
- <span data-ttu-id="0611e-197">OIOUBL プロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="0611e-197">OIOUBL Project invoice</span></span>
- <span data-ttu-id="0611e-198">OIOUBL 売上訂正票</span><span class="sxs-lookup"><span data-stu-id="0611e-198">OIOUBL Sales credit note</span></span>
- <span data-ttu-id="0611e-199">OIOUBL プロジェクト訂正票</span><span class="sxs-lookup"><span data-stu-id="0611e-199">OIOUBL Project credit note</span></span>

#### <a name="belgian-be-electronic-invoice-sales-and-project-invoices-for-belgium"></a><span data-ttu-id="0611e-200">ベルギー (BE) 電子請求書 : ベルギー向け、売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="0611e-200">Belgian (BE) electronic invoice: Sales and project invoices for Belgium</span></span>

- <span data-ttu-id="0611e-201">UBL 売上請求書 BE</span><span class="sxs-lookup"><span data-stu-id="0611e-201">UBL Sales invoice BE</span></span>
- <span data-ttu-id="0611e-202">UBL プロジェクト請求書 BE</span><span class="sxs-lookup"><span data-stu-id="0611e-202">UBL Project invoice BE</span></span>
- <span data-ttu-id="0611e-203">UBL プロジェクト訂正票 BE</span><span class="sxs-lookup"><span data-stu-id="0611e-203">UBL Project credit note BE</span></span>
- <span data-ttu-id="0611e-204">UBL 売上訂正票 BE</span><span class="sxs-lookup"><span data-stu-id="0611e-204">UBL Sales credit note BE</span></span>

#### <a name="brazilian-br-nf-e-nf-e-federal-brazil"></a><span data-ttu-id="0611e-205">ブラジル (BR) NF-e: NF-e Federal (ブラジル)</span><span class="sxs-lookup"><span data-stu-id="0611e-205">Brazilian (BR) NF-e: NF-e Federal (Brazil)</span></span>

- <span data-ttu-id="0611e-206">NF-e 送信エクスポートの形式 (BR)</span><span class="sxs-lookup"><span data-stu-id="0611e-206">NF-e submit export format (BR)</span></span>
- <span data-ttu-id="0611e-207">NF-e 督促状エクスポートの形式 (BR)</span><span class="sxs-lookup"><span data-stu-id="0611e-207">NF-e correction letter export format (BR)</span></span>
- <span data-ttu-id="0611e-208">NF-e キャンセル エクスポートの形式 (BR)</span><span class="sxs-lookup"><span data-stu-id="0611e-208">NF-e cancel export format (BR)</span></span>
- <span data-ttu-id="0611e-209">NF-e 破棄エクスポートの形式 (BR)</span><span class="sxs-lookup"><span data-stu-id="0611e-209">NF-e discard export format (BR)</span></span>

#### <a name="brazilian-nfs-e-br-nfs-e-abrasf-curitiba-city"></a><span data-ttu-id="0611e-210">ブラジル NFS-e (BR): NFS-e ABRASF クリチバ市</span><span class="sxs-lookup"><span data-stu-id="0611e-210">Brazilian NFS-e (BR): NFS-e ABRASF Curitiba city</span></span>

- <span data-ttu-id="0611e-211">NFS-e ABRASF クリチバ (BR)</span><span class="sxs-lookup"><span data-stu-id="0611e-211">NFS-e ABRASF Curitiba (BR)</span></span>
- <span data-ttu-id="0611e-212">NFS-e ABRASF 調査書 クリチバ (BR)</span><span class="sxs-lookup"><span data-stu-id="0611e-212">NFS-e ABRASF Inquire Curitiba (BR)</span></span>

#### <a name="danish-dk-electronic-invoice-sales-and-project-invoices-for-denmark"></a><span data-ttu-id="0611e-213">デンマーク (BE) 電子請求書 : デンマーク向け、売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="0611e-213">Danish (DK) electronic invoice: Sales and project invoices for Denmark</span></span>

- <span data-ttu-id="0611e-214">OIOUBL 売上請求書</span><span class="sxs-lookup"><span data-stu-id="0611e-214">OIOUBL Sales invoice</span></span>
- <span data-ttu-id="0611e-215">OIOUBL プロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="0611e-215">OIOUBL Project invoice</span></span>
- <span data-ttu-id="0611e-216">OIOUBL 売上訂正票</span><span class="sxs-lookup"><span data-stu-id="0611e-216">OIOUBL Sales credit note</span></span>
- <span data-ttu-id="0611e-217">OIOUBL プロジェクト訂正票</span><span class="sxs-lookup"><span data-stu-id="0611e-217">OIOUBL Project credit note</span></span>

#### <a name="dutch-nl-electronic-invoice-sales-and-project-invoices-for-netherlands"></a><span data-ttu-id="0611e-218">オランダ (NL) 電子請求書 : オランダ向け、売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="0611e-218">Dutch (NL) electronic invoice: Sales and project invoices for Netherlands</span></span>

- <span data-ttu-id="0611e-219">UBL 売上請求書 NL</span><span class="sxs-lookup"><span data-stu-id="0611e-219">UBL Sales invoice NL</span></span>
- <span data-ttu-id="0611e-220">UBL プロジェクト請求書 NL</span><span class="sxs-lookup"><span data-stu-id="0611e-220">UBL Project invoice NL</span></span>
- <span data-ttu-id="0611e-221">UBL プロジェクト訂正票 NL</span><span class="sxs-lookup"><span data-stu-id="0611e-221">UBL Project credit note NL</span></span>
- <span data-ttu-id="0611e-222">UBL 売上訂正票 NL</span><span class="sxs-lookup"><span data-stu-id="0611e-222">UBL Sales credit note NL</span></span>

#### <a name="egyptian-eg-electronic-invoice-sales-and-project-invoices-for-egypt"></a><span data-ttu-id="0611e-223">エジプト (BE) 電子請求書 : エジプト向け、売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="0611e-223">Egyptian (EG) electronic invoice: Sales and project invoices for Egypt</span></span>

- <span data-ttu-id="0611e-224">売上請求書(EG)(請求書)</span><span class="sxs-lookup"><span data-stu-id="0611e-224">Sales invoice (EG)(Invoicing)</span></span>
- <span data-ttu-id="0611e-225">プロジェクト請求書(EG)(請求書)</span><span class="sxs-lookup"><span data-stu-id="0611e-225">Project invoice (EG)(Invoicing)</span></span>

#### <a name="estonian-ee-electronic-invoice-sales-and-project-invoices-for-estonia"></a><span data-ttu-id="0611e-226">エストニア (BE) 電子請求書 : エストニア向け、売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="0611e-226">Estonian (EE) electronic invoice: Sales and project invoices for Estonia</span></span>

- <span data-ttu-id="0611e-227">売上請求書 (EE)</span><span class="sxs-lookup"><span data-stu-id="0611e-227">Sales invoice (EE)</span></span>
- <span data-ttu-id="0611e-228">プロジェクト請求書 (EE)</span><span class="sxs-lookup"><span data-stu-id="0611e-228">Project invoice (EE)</span></span>

#### <a name="finnish-fi-electronic-invoice-sales-and-project-invoices-for-finland"></a><span data-ttu-id="0611e-229">フィンランド (FI) 電子請求書 : フィンランド向け、売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="0611e-229">Finnish (FI) electronic invoice: Sales and project invoices for Finland</span></span>

- <span data-ttu-id="0611e-230">売上請求書 (FI)</span><span class="sxs-lookup"><span data-stu-id="0611e-230">Sales invoice (FI)</span></span>
- <span data-ttu-id="0611e-231">プロジェクト請求書 (FI)</span><span class="sxs-lookup"><span data-stu-id="0611e-231">Project invoice (FI)</span></span>

#### <a name="french-fr-electronic-invoice-sales-and-project-invoices-for-france"></a><span data-ttu-id="0611e-232">フランス (FR) 電子請求書 : フランス向け、売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="0611e-232">French (FR) electronic invoice: Sales and project invoices for France</span></span>

- <span data-ttu-id="0611e-233">UBL 売上請求書 FR</span><span class="sxs-lookup"><span data-stu-id="0611e-233">UBL Sales invoice FR</span></span>
- <span data-ttu-id="0611e-234">UBL プロジェクト請求書 FR</span><span class="sxs-lookup"><span data-stu-id="0611e-234">UBL Project invoice FR</span></span>
- <span data-ttu-id="0611e-235">UBL プロジェクト訂正票 FR</span><span class="sxs-lookup"><span data-stu-id="0611e-235">UBL Project credit note FR</span></span>
- <span data-ttu-id="0611e-236">UBL 売上訂正票 FR</span><span class="sxs-lookup"><span data-stu-id="0611e-236">UBL Sales credit note FR</span></span>

#### <a name="german-de-electronic-invoice-sales-and-project-invoices-for-germany"></a><span data-ttu-id="0611e-237">ドイツ (DE) 電子請求書 : ドイツ向け、売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="0611e-237">German (DE) electronic invoice: Sales and project invoices for Germany</span></span>

- <span data-ttu-id="0611e-238">売上請求書 (DE)</span><span class="sxs-lookup"><span data-stu-id="0611e-238">Sales invoice (DE)</span></span>
- <span data-ttu-id="0611e-239">プロジェクト請求書 (DE)</span><span class="sxs-lookup"><span data-stu-id="0611e-239">Project invoice (DE)</span></span>

#### <a name="italian-it-electronic-invoice-sales-and-project-invoices-for-italy"></a><span data-ttu-id="0611e-240">イタリア (IT) 電子請求書 : イタリア向け、売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="0611e-240">Italian (IT) electronic invoice: Sales and project invoices for Italy</span></span>

- <span data-ttu-id="0611e-241">売上請求書 (IT)</span><span class="sxs-lookup"><span data-stu-id="0611e-241">Sales invoice (IT)</span></span>
- <span data-ttu-id="0611e-242">プロジェクト請求書 (IT)</span><span class="sxs-lookup"><span data-stu-id="0611e-242">Project invoice (IT)</span></span>

#### <a name="mexican-mx-cfdi-cfdi-for-mexico"></a><span data-ttu-id="0611e-243">メキシコ (MX) CFDI: メキシコ向け CFDI</span><span class="sxs-lookup"><span data-stu-id="0611e-243">Mexican (MX) CFDI: CFDI for Mexico</span></span>

- <span data-ttu-id="0611e-244">CFDI 請求書フォーマット (MX)</span><span class="sxs-lookup"><span data-stu-id="0611e-244">CFDI invoice format (MX)</span></span>
- <span data-ttu-id="0611e-245">CFDI 梱包明細 (MX)</span><span class="sxs-lookup"><span data-stu-id="0611e-245">CFDI Packing slip (MX)</span></span>
- <span data-ttu-id="0611e-246">CFDI 在庫振替 (MX)</span><span class="sxs-lookup"><span data-stu-id="0611e-246">CFDI Inventory transfer (MX)</span></span>
- <span data-ttu-id="0611e-247">CFDI 支払い形式 (MX)</span><span class="sxs-lookup"><span data-stu-id="0611e-247">CFDI payment format (MX)</span></span>
- <span data-ttu-id="0611e-248">CFDI 請求書キャンセル形式 (MX)</span><span class="sxs-lookup"><span data-stu-id="0611e-248">CFDI invoice cancel format (MX)</span></span>

#### <a name="norwegian-no-electronic-invoice-sales-and-project-invoices-for-norway"></a><span data-ttu-id="0611e-249">ノルウェー (BE) 電子請求書 : ノルウェー向け、売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="0611e-249">Norwegian (NO) electronic invoice: Sales and project invoices for Norway</span></span>

- <span data-ttu-id="0611e-250">OIOUBL 売上請求書</span><span class="sxs-lookup"><span data-stu-id="0611e-250">OIOUBL Sales invoice</span></span>
- <span data-ttu-id="0611e-251">OIOUBL プロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="0611e-251">OIOUBL Project invoice</span></span>
- <span data-ttu-id="0611e-252">OIOUBL 売上訂正票</span><span class="sxs-lookup"><span data-stu-id="0611e-252">OIOUBL Sales credit note</span></span>
- <span data-ttu-id="0611e-253">OIOUBL プロジェクト訂正票</span><span class="sxs-lookup"><span data-stu-id="0611e-253">OIOUBL Project credit note</span></span>

#### <a name="peppol-electronic-invoice-peppol-sales-and-project-invoices"></a><span data-ttu-id="0611e-254">PEPPOL 電子請求書 :PEPPOL 売上とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="0611e-254">PEPPOL electronic invoice: PEPPOL sales and project invoices</span></span>

- <span data-ttu-id="0611e-255">PEPPOL 売上請求書</span><span class="sxs-lookup"><span data-stu-id="0611e-255">PEPPOL Sales invoice</span></span>
- <span data-ttu-id="0611e-256">PEPPOL プロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="0611e-256">PEPPOL Project invoice</span></span>
- <span data-ttu-id="0611e-257">PEPPOL 売上訂正票</span><span class="sxs-lookup"><span data-stu-id="0611e-257">PEPPOL Sales credit note</span></span>
- <span data-ttu-id="0611e-258">PEPPOL プロジェクト訂正票</span><span class="sxs-lookup"><span data-stu-id="0611e-258">PEPPOL Project credit note</span></span>

#### <a name="spanish-es-electronic-invoice-sales-and-project-invoices-for-spain"></a><span data-ttu-id="0611e-259">スペイン (ES) 電子請求書 : スペイン向け、売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="0611e-259">Spanish (ES) electronic invoice: Sales and project invoices for Spain</span></span>

- <span data-ttu-id="0611e-260">売上請求書 (ES)</span><span class="sxs-lookup"><span data-stu-id="0611e-260">Sales invoice (ES)</span></span>
- <span data-ttu-id="0611e-261">プロジェクト請求書 (ES)</span><span class="sxs-lookup"><span data-stu-id="0611e-261">Project invoice (ES)</span></span>

### <a name="actions"></a><span data-ttu-id="0611e-262">アクション</span><span class="sxs-lookup"><span data-stu-id="0611e-262">Actions</span></span>

<span data-ttu-id="0611e-263">次の表では、利用可能なアクションと、現在一般利用可能なのか、プレビュー段階であるのかを示しています。</span><span class="sxs-lookup"><span data-stu-id="0611e-263">The following table lists the available actions, and whether they are currently generally available or still in preview.</span></span>

| <span data-ttu-id="0611e-264">操作</span><span class="sxs-lookup"><span data-stu-id="0611e-264">Action</span></span>                                        | <span data-ttu-id="0611e-265">説明</span><span class="sxs-lookup"><span data-stu-id="0611e-265">Description</span></span>                                                                  | <span data-ttu-id="0611e-266">適用の対象</span><span class="sxs-lookup"><span data-stu-id="0611e-266">Availability</span></span>         |
|-----------------------------------------------|------------------------------------------------------------------------------|----------------------|
| <span data-ttu-id="0611e-267">ドキュメントの変換</span><span class="sxs-lookup"><span data-stu-id="0611e-267">Transform document</span></span>                            | <span data-ttu-id="0611e-268">電子レポート形式を実行してドキュメントを変換します。</span><span class="sxs-lookup"><span data-stu-id="0611e-268">Run Electronic Reporting format to transform the document.</span></span>                   | <span data-ttu-id="0611e-269">一般に入手可能</span><span class="sxs-lookup"><span data-stu-id="0611e-269">Generally available</span></span>  |
| <span data-ttu-id="0611e-270">xml ドキュメントへの署名</span><span class="sxs-lookup"><span data-stu-id="0611e-270">Sign xml document</span></span>                             | <span data-ttu-id="0611e-271">デジタル署名を使用して XML ドキュメントに署名します。</span><span class="sxs-lookup"><span data-stu-id="0611e-271">Sign xml documents with digital signature.</span></span>                                   | <span data-ttu-id="0611e-272">プレビュー</span><span class="sxs-lookup"><span data-stu-id="0611e-272">In preview</span></span>           |
| <span data-ttu-id="0611e-273">エジプト税務当局に向けた json 文書に署名する</span><span class="sxs-lookup"><span data-stu-id="0611e-273">Sign json document for Egyptian Tax Authority</span></span> | <span data-ttu-id="0611e-274">エジプト税務局の電子署名で json 文書に署名します。</span><span class="sxs-lookup"><span data-stu-id="0611e-274">Sign json documents with digital signature for Egyptian Tax Authority.</span></span>       | <span data-ttu-id="0611e-275">一般に入手可能</span><span class="sxs-lookup"><span data-stu-id="0611e-275">Generally available</span></span>  |
| <span data-ttu-id="0611e-276">エジプト ETA サービスとの統合</span><span class="sxs-lookup"><span data-stu-id="0611e-276">Integrate with Egyptian ETA service</span></span>           | <span data-ttu-id="0611e-277">エジプト税務当局とのやりとりを行います。</span><span class="sxs-lookup"><span data-stu-id="0611e-277">Communicate with Egyptian Tax Authority.</span></span>                                     | <span data-ttu-id="0611e-278">一般に入手可能</span><span class="sxs-lookup"><span data-stu-id="0611e-278">Generally available</span></span>  |
| <span data-ttu-id="0611e-279">ブラジル SEFAZ サービスの呼び出し</span><span class="sxs-lookup"><span data-stu-id="0611e-279">Call Brazilian SEFAZ Service</span></span>                  | <span data-ttu-id="0611e-280">ブラジルの SEFAZ サービスと統合して会計書類を提出します。</span><span class="sxs-lookup"><span data-stu-id="0611e-280">Integrate with Brazilian SEFAZ service for fiscal document submission.</span></span>       | <span data-ttu-id="0611e-281">プレビュー</span><span class="sxs-lookup"><span data-stu-id="0611e-281">In preview</span></span>           |
| <span data-ttu-id="0611e-282">メキシコ PAC サービスの呼び出し</span><span class="sxs-lookup"><span data-stu-id="0611e-282">Call Mexican PAC Service</span></span>                      | <span data-ttu-id="0611e-283">CFDI 提出に向けたメキシコ PAC サービスとの統合を行います。</span><span class="sxs-lookup"><span data-stu-id="0611e-283">Integrate with Mexican PAC service for CFDI submission.</span></span>                      | <span data-ttu-id="0611e-284">プレビュー</span><span class="sxs-lookup"><span data-stu-id="0611e-284">In preview</span></span>           |
| <span data-ttu-id="0611e-285">応答の処理</span><span class="sxs-lookup"><span data-stu-id="0611e-285">Process response</span></span>                              | <span data-ttu-id="0611e-286">Web サービス コールから受信した応答を分析します。</span><span class="sxs-lookup"><span data-stu-id="0611e-286">Analyze the response received from the web service call.</span></span>                     | <span data-ttu-id="0611e-287">一般に入手可能</span><span class="sxs-lookup"><span data-stu-id="0611e-287">Generally available</span></span>  |
| <span data-ttu-id="0611e-288">MS Power Automate を使用する</span><span class="sxs-lookup"><span data-stu-id="0611e-288">Use MS Power Automate</span></span>                         | <span data-ttu-id="0611e-289">Microsoft Power Automate に組み込まれたフローと統合します。</span><span class="sxs-lookup"><span data-stu-id="0611e-289">Integrate with flow built in Microsoft Power Automate.</span></span>                       | <span data-ttu-id="0611e-290">プレビュー</span><span class="sxs-lookup"><span data-stu-id="0611e-290">In preview</span></span>           |

### <a name="applicability-rules"></a><span data-ttu-id="0611e-291">適合性ルール</span><span class="sxs-lookup"><span data-stu-id="0611e-291">Applicability rules</span></span>

<span data-ttu-id="0611e-292">適合性ルールは、電子請求機能レベルで定義される構成可能な条件です。</span><span class="sxs-lookup"><span data-stu-id="0611e-292">Applicability rules are configurable clauses that are defined at the Electronic invoicing feature level.</span></span> <span data-ttu-id="0611e-293">ルールを構成して、電子請求機能セットを通じて電子請求機能を実行するためのコンテキストを提供することができます。</span><span class="sxs-lookup"><span data-stu-id="0611e-293">The rules are configured to provide a context for execution of electronic invoicing features through the Electronic Invoicing capability set.</span></span>

<span data-ttu-id="0611e-294">Finance または Supply Chain Management からビジネス ドキュメントが電子請求に送信されると、ビジネス ドキュメントは、電子請求機能セットが特定の電子請求機能を呼び出して送信処理をできるようにする明示的な参照は行いません。</span><span class="sxs-lookup"><span data-stu-id="0611e-294">When a business document from Finance or Supply Chain Management is submitted to electronic invoicing, the business document doesn't carry an explicit reference that allows the Electronic Invoicing capability set to call a particular electronic invoicing feature to process the submission.</span></span>

<span data-ttu-id="0611e-295">ただし、正しく構成されている場合、ビジネス ドキュメントには、電子請求機能を選択して電子請求書を生成する必要がある電子請求を解決できるようにするのに必要な要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="0611e-295">Nevertheless, when properly configured, the business document contains the necessary elements that allow electronic invoicing to resolve which electronic invoicing feature must be selected and then generate the electronic invoice.</span></span>

<span data-ttu-id="0611e-296">適合性ルールにより、電子請求機能セットは送信処理に使用する必要がある正確な電子請求機能を検索できるようになります。</span><span class="sxs-lookup"><span data-stu-id="0611e-296">Applicability rules allow the Electronic Invoicing capability set to find the exact electronic invoicing features that must be used to process the submission.</span></span> <span data-ttu-id="0611e-297">これは、送信されたビジネス ドキュメントからのコンテンツを適合性ルールの条件と照合することによって行われます。</span><span class="sxs-lookup"><span data-stu-id="0611e-297">This is done by matching the contents from the submitted business document with the clauses from the Applicability rules.</span></span>

<span data-ttu-id="0611e-298">たとえば、関連する適用性ルールを持つ 2 つの電子請求機能が電子請求機能セットに展開されます。</span><span class="sxs-lookup"><span data-stu-id="0611e-298">For example, two electronic invoicing features with related Applicability rules are deployed into the Electronic Invoicing capability set.</span></span>

| <span data-ttu-id="0611e-299">電子請求の機能</span><span class="sxs-lookup"><span data-stu-id="0611e-299">Electronic invoicing feature</span></span> | <span data-ttu-id="0611e-300">適合性ルール</span><span class="sxs-lookup"><span data-stu-id="0611e-300">Applicability rules</span></span>        |
|------------------------------|--------------------------- |
| <span data-ttu-id="0611e-301">A</span><span class="sxs-lookup"><span data-stu-id="0611e-301">A</span></span>                            | <p><span data-ttu-id="0611e-302">国 = BR</span><span class="sxs-lookup"><span data-stu-id="0611e-302">Country = BR</span></span></p><p><span data-ttu-id="0611e-303">および</span><span class="sxs-lookup"><span data-stu-id="0611e-303">and</span></span></p><p><span data-ttu-id="0611e-304">法人 = BRMF</span><span class="sxs-lookup"><span data-stu-id="0611e-304">Legal entity = BRMF</span></span></p>  |
| <span data-ttu-id="0611e-305">B</span><span class="sxs-lookup"><span data-stu-id="0611e-305">B</span></span>                            | <p><span data-ttu-id="0611e-306">国 = MX</span><span class="sxs-lookup"><span data-stu-id="0611e-306">Country = MX</span></span></p><p><span data-ttu-id="0611e-307">および</span><span class="sxs-lookup"><span data-stu-id="0611e-307">and</span></span></p><p><span data-ttu-id="0611e-308">法人 = MXMF</span><span class="sxs-lookup"><span data-stu-id="0611e-308">Legal entity = MXMF</span></span></p>  |

<span data-ttu-id="0611e-309">Finance または Supply Chain Management からのビジネス ドキュメントが電子請求機能セットに送信された場合、ビジネス ドキュメントには次のように属性が含まれます。</span><span class="sxs-lookup"><span data-stu-id="0611e-309">If a business document from Finance or Supply Chain Management is submitted to the Electronic Invoicing capability set, the business document contains the following attributes filled as:</span></span>

- <span data-ttu-id="0611e-310">国 = BR</span><span class="sxs-lookup"><span data-stu-id="0611e-310">Country = BR</span></span>
- <span data-ttu-id="0611e-311">法人 = BRMF</span><span class="sxs-lookup"><span data-stu-id="0611e-311">Legal entity = BRMF</span></span>

<span data-ttu-id="0611e-312">電子請求機能セットは、送信処理と電子請求書の生成を処理する電子請求機能 **A** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0611e-312">The Electronic Invoicing capability set will select the electronic invoicing feature **A** to process the submission and generate the electronic invoice.</span></span>

<span data-ttu-id="0611e-313">ビジネス ドキュメントに次が含まれている場合も同様です。</span><span class="sxs-lookup"><span data-stu-id="0611e-313">In the same way, if the business document contains:</span></span>

- <span data-ttu-id="0611e-314">国 = MX</span><span class="sxs-lookup"><span data-stu-id="0611e-314">Country = MX</span></span>
- <span data-ttu-id="0611e-315">法人 = MXMF</span><span class="sxs-lookup"><span data-stu-id="0611e-315">Legal entity = MXMF</span></span>

<span data-ttu-id="0611e-316">電子請求機能 **B** を選択して、電子請求書を生成します。</span><span class="sxs-lookup"><span data-stu-id="0611e-316">Electronic invoicing feature **B** is selected to generate the electronic invoice.</span></span>

<span data-ttu-id="0611e-317">適合性ルールの構成をあいまいにすることはできません。</span><span class="sxs-lookup"><span data-stu-id="0611e-317">The configuration of Applicability rules can't be ambiguous.</span></span> <span data-ttu-id="0611e-318">つまり、複数の電子請求機能が同じ条項を持つことはなく、それ以外の場合は選択が行なえないことになります。</span><span class="sxs-lookup"><span data-stu-id="0611e-318">This means that two or more electronic invoicing features can't have the same clauses, otherwise it will lead to no selection.</span></span> <span data-ttu-id="0611e-319">電子請求機能が重複している場合は、あいまいさを回避するために、追加の条件を使用して電子請求機能セットが 2 つの電子請求機能を区別できるようにします。</span><span class="sxs-lookup"><span data-stu-id="0611e-319">If there is a duplication of electronic invoicing features, to avoid ambiguity, use additional clauses to allow the Electronic Invoicing capability set to distinguish between the two electronic invoicing features.</span></span>

<span data-ttu-id="0611e-320">たとえば、電子請求機能 **C** を考慮します。この機能は電子請求機能 **A** のコピーです。</span><span class="sxs-lookup"><span data-stu-id="0611e-320">For example, consider electronic invoicing feature **C**. This feature is a copy of electronic invoicing feature **A**.</span></span>

| <span data-ttu-id="0611e-321">電子請求の機能</span><span class="sxs-lookup"><span data-stu-id="0611e-321">Electronic invoicing feature</span></span> | <span data-ttu-id="0611e-322">適合性ルール</span><span class="sxs-lookup"><span data-stu-id="0611e-322">Applicability rules</span></span>        |
|------------------------------|--------------------------- |
| <span data-ttu-id="0611e-323">A</span><span class="sxs-lookup"><span data-stu-id="0611e-323">A</span></span>                            | <p><span data-ttu-id="0611e-324">国 = BR</span><span class="sxs-lookup"><span data-stu-id="0611e-324">Country = BR</span></span></p><p><span data-ttu-id="0611e-325">および</span><span class="sxs-lookup"><span data-stu-id="0611e-325">and</span></span></p><p><span data-ttu-id="0611e-326">法人 = BRMF</span><span class="sxs-lookup"><span data-stu-id="0611e-326">Legal entity = BRMF</span></span></p>  |
| <span data-ttu-id="0611e-327">貸方</span><span class="sxs-lookup"><span data-stu-id="0611e-327">C</span></span>                            | <p><span data-ttu-id="0611e-328">国 = BR</span><span class="sxs-lookup"><span data-stu-id="0611e-328">Country = BR</span></span></p><p><span data-ttu-id="0611e-329">および</span><span class="sxs-lookup"><span data-stu-id="0611e-329">and</span></span></p><p><span data-ttu-id="0611e-330">法人 = BRMF</span><span class="sxs-lookup"><span data-stu-id="0611e-330">Legal entity = BRMF</span></span></p>  |

<span data-ttu-id="0611e-331">この例では、機能 **C** は、次のコンテンツを含むビジネス ドキュメントの送信の前にあります。</span><span class="sxs-lookup"><span data-stu-id="0611e-331">In this example, feature **C** is in front of a business document submission that contains the following:</span></span>

- <span data-ttu-id="0611e-332">国 = BR</span><span class="sxs-lookup"><span data-stu-id="0611e-332">Country = BR</span></span>
- <span data-ttu-id="0611e-333">法人 = BRMF</span><span class="sxs-lookup"><span data-stu-id="0611e-333">Legal entity = BRMF</span></span>

<span data-ttu-id="0611e-334">送信物にまったく同じ条件が含まれているため、電子請求機能は送信処理に使用する電子請求機能を区別できません。</span><span class="sxs-lookup"><span data-stu-id="0611e-334">The Electronic Invoicing capability can't distinguish which electronic invoicing feature must be used to process the submission because the submissions contain the exact same clauses.</span></span>

<span data-ttu-id="0611e-335">適合性ルールを通じて 2 つの機能に違いを作成するために、電子請求機能セットが正しい電子請求機能を選択できるように、機能の 1 つに新しい条件を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0611e-335">To create a distinction between the two features through Applicability rules, a new clause must be added to one of the features to allow the Electronic Invoicing capability set to select the proper electronic invoicing feature.</span></span>

| <span data-ttu-id="0611e-336">電子請求の機能</span><span class="sxs-lookup"><span data-stu-id="0611e-336">Electronic invoicing feature</span></span> | <span data-ttu-id="0611e-337">適合性ルール</span><span class="sxs-lookup"><span data-stu-id="0611e-337">Applicability rules</span></span>        |
|------------------------------|--------------------------- |
| <span data-ttu-id="0611e-338">A</span><span class="sxs-lookup"><span data-stu-id="0611e-338">A</span></span>                            | <p><span data-ttu-id="0611e-339">国 = BR</span><span class="sxs-lookup"><span data-stu-id="0611e-339">Country = BR</span></span></p><p><span data-ttu-id="0611e-340">および</span><span class="sxs-lookup"><span data-stu-id="0611e-340">and</span></span></p><p><span data-ttu-id="0611e-341">法人 = BRMF</span><span class="sxs-lookup"><span data-stu-id="0611e-341">Legal entity = BRMF</span></span></p>  |
| <span data-ttu-id="0611e-342">貸方</span><span class="sxs-lookup"><span data-stu-id="0611e-342">C</span></span>                            | <p><span data-ttu-id="0611e-343">国 = BR</span><span class="sxs-lookup"><span data-stu-id="0611e-343">Country = BR</span></span></p><p><span data-ttu-id="0611e-344">および</span><span class="sxs-lookup"><span data-stu-id="0611e-344">and</span></span></p><p><span data-ttu-id="0611e-345">法人 = BRMF</span><span class="sxs-lookup"><span data-stu-id="0611e-345">Legal entity = BRMF</span></span></p><p><span data-ttu-id="0611e-346">および</span><span class="sxs-lookup"><span data-stu-id="0611e-346">and</span></span></p><p><span data-ttu-id="0611e-347">Model=55</span><span class="sxs-lookup"><span data-stu-id="0611e-347">Model=55</span></span></p>  |

<span data-ttu-id="0611e-348">より複雑な条件の作成をサポートするために、次のリソースが使用可能です。</span><span class="sxs-lookup"><span data-stu-id="0611e-348">To support creating more complex clauses, the following resources are available:</span></span>

<span data-ttu-id="0611e-349">論理演算子:</span><span class="sxs-lookup"><span data-stu-id="0611e-349">Logic operators:</span></span>
- <span data-ttu-id="0611e-350">かつ</span><span class="sxs-lookup"><span data-stu-id="0611e-350">And</span></span>
- <span data-ttu-id="0611e-351">又は</span><span class="sxs-lookup"><span data-stu-id="0611e-351">Or</span></span>

<span data-ttu-id="0611e-352">演算子のタイプ:</span><span class="sxs-lookup"><span data-stu-id="0611e-352">Operators types:</span></span>
- <span data-ttu-id="0611e-353">Equal</span><span class="sxs-lookup"><span data-stu-id="0611e-353">Equal</span></span>
- <span data-ttu-id="0611e-354">Not equal</span><span class="sxs-lookup"><span data-stu-id="0611e-354">Not equal</span></span>
- <span data-ttu-id="0611e-355">Greater than</span><span class="sxs-lookup"><span data-stu-id="0611e-355">Greater than</span></span>
- <span data-ttu-id="0611e-356">Less than</span><span class="sxs-lookup"><span data-stu-id="0611e-356">Less than</span></span>
- <span data-ttu-id="0611e-357">以上</span><span class="sxs-lookup"><span data-stu-id="0611e-357">Greater than or equal to</span></span>
- <span data-ttu-id="0611e-358">以下</span><span class="sxs-lookup"><span data-stu-id="0611e-358">Less than or equal to</span></span>
- <span data-ttu-id="0611e-359">Contains</span><span class="sxs-lookup"><span data-stu-id="0611e-359">Contains</span></span>
- <span data-ttu-id="0611e-360">次の値で始まる</span><span class="sxs-lookup"><span data-stu-id="0611e-360">Begins with</span></span>

<span data-ttu-id="0611e-361">データ型:</span><span class="sxs-lookup"><span data-stu-id="0611e-361">Data types:</span></span>
- <span data-ttu-id="0611e-362">文字列</span><span class="sxs-lookup"><span data-stu-id="0611e-362">String</span></span>
- <span data-ttu-id="0611e-363">番号</span><span class="sxs-lookup"><span data-stu-id="0611e-363">Number</span></span>
- <span data-ttu-id="0611e-364">ブール値</span><span class="sxs-lookup"><span data-stu-id="0611e-364">Boolean</span></span>
- <span data-ttu-id="0611e-365">日</span><span class="sxs-lookup"><span data-stu-id="0611e-365">Date</span></span>
- <span data-ttu-id="0611e-366">UUID</span><span class="sxs-lookup"><span data-stu-id="0611e-366">UUID</span></span>

<span data-ttu-id="0611e-367">条件をグループ化およびグループ解除する機能。</span><span class="sxs-lookup"><span data-stu-id="0611e-367">Capability to group and ungroup clauses.</span></span>
<span data-ttu-id="0611e-368">例は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="0611e-368">The example looks like this.</span></span>

| <span data-ttu-id="0611e-369">電子請求の機能</span><span class="sxs-lookup"><span data-stu-id="0611e-369">Electronic invoicing feature</span></span> | <span data-ttu-id="0611e-370">適合性ルール</span><span class="sxs-lookup"><span data-stu-id="0611e-370">Applicability rules</span></span>        |
|------------------------------|--------------------------- |
| <span data-ttu-id="0611e-371">貸方</span><span class="sxs-lookup"><span data-stu-id="0611e-371">C</span></span>                            | <p><span data-ttu-id="0611e-372">国 = BR</span><span class="sxs-lookup"><span data-stu-id="0611e-372">Country = BR</span></span></p><p><span data-ttu-id="0611e-373">および</span><span class="sxs-lookup"><span data-stu-id="0611e-373">and</span></span></p><p><span data-ttu-id="0611e-374">( 法人 = BRMF</span><span class="sxs-lookup"><span data-stu-id="0611e-374">( Legal entity = BRMF</span></span></p><p><span data-ttu-id="0611e-375">または</span><span class="sxs-lookup"><span data-stu-id="0611e-375">or</span></span></p><p><span data-ttu-id="0611e-376">Model=55)</span><span class="sxs-lookup"><span data-stu-id="0611e-376">Model=55)</span></span></p>  |


## <a name="configuration-providers"></a><span data-ttu-id="0611e-377">コンフィギュレーション提供者</span><span class="sxs-lookup"><span data-stu-id="0611e-377">Configuration providers</span></span>

<span data-ttu-id="0611e-378">構成プロバイダーは、電子請求書発行機能とその ER コンポーネント (モデル マッピング、フォーマット構成、コンテキスト モデルなど) を提供します。</span><span class="sxs-lookup"><span data-stu-id="0611e-378">Configuration providers provide the electronic invoicing features and their ER components, such as the model mapping, format configuration, and context model.</span></span> <span data-ttu-id="0611e-379">関連するグローバル リポジトリで電子請求書発行機能と ER コンポーネントが公開されています。</span><span class="sxs-lookup"><span data-stu-id="0611e-379">They publish the electronic invoicing features and ER components in the associated Global repository.</span></span> <span data-ttu-id="0611e-380">そこから他の組織がダウンロードできるようになっています。</span><span class="sxs-lookup"><span data-stu-id="0611e-380">From there, other organizations can download them.</span></span>

<span data-ttu-id="0611e-381">RCS を介した電子請求書発行機能の構成を行う前に、 **電子レポート** モジュールの構成プロバイダーに独自の組織を構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0611e-381">Before you configure the electronic invoicing features through RCS, you must configure your own organization as a configuration provider in the **Electronic reporting** module.</span></span> <span data-ttu-id="0611e-382">構成プロバイダーを **有効化** に設定する方法については、[構成プロバイダーを作成して有効化としてマークする](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0611e-382">For information about how to set a configuration provider to **Active**, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="viewing-electronic-invoicing-features-in-the-global-repository"></a><span data-ttu-id="0611e-383">グローバル リポジトリでの電子請求機能を表示する</span><span class="sxs-lookup"><span data-stu-id="0611e-383">Viewing electronic invoicing features in the Global repository</span></span>

<span data-ttu-id="0611e-384">特定の構成プロバイダのグローバル リポジトリで利用可能な電子請求書発行機能を閲覧するには、組織の RCS インスタンスを同期します。</span><span class="sxs-lookup"><span data-stu-id="0611e-384">To browse the electronic invoicing features that are available in the Global repository for a specific configuration provider, sync your organization's RCS instance.</span></span> <span data-ttu-id="0611e-385">同期が完了すると、使用可能な電子請求機能の一覧が更新されます。</span><span class="sxs-lookup"><span data-stu-id="0611e-385">After synchronization is completed, the list of available electronic invoicing features is updated.</span></span>

## <a name="importing-electronic-invoicing-features"></a><span data-ttu-id="0611e-386">電子請求書機能のインポート</span><span class="sxs-lookup"><span data-stu-id="0611e-386">Importing electronic invoicing features</span></span>

<span data-ttu-id="0611e-387">電子請求機能を使用・構成する前に、組織の RCS インスタンスにインポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0611e-387">Before you use or configure the electronic invoicing features, you must import them into your organization's RCS instance.</span></span> <span data-ttu-id="0611e-388">インポート操作により、機能のローカル コピーが作成され、機能で使用する ER コンポーネント (構成やモデル構成の書式設定など) が組織の RCS インスタンスにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="0611e-388">The import operation creates a local copy of the features and copies all the ER artifacts that the features use (for example, format configurations and model configurations) to your organization's RCS instance.</span></span>

<span data-ttu-id="0611e-389">任意の構成プロバイダから電子請求機能をインポートできます。</span><span class="sxs-lookup"><span data-stu-id="0611e-389">You can import the electronic invoicing features from any configuration provider.</span></span>

## <a name="creating-electronic-invoicing-features"></a><span data-ttu-id="0611e-390">電子請求書機能の作成</span><span class="sxs-lookup"><span data-stu-id="0611e-390">Creating electronic invoicing features</span></span>

<span data-ttu-id="0611e-391">ゼロから電子請求書機能を作成することも、別の電子請求書機能から派生させることもできます。</span><span class="sxs-lookup"><span data-stu-id="0611e-391">You can create an electronic invoicing feature from scratch, or you can derive it from another electronic invoicing feature.</span></span>

<span data-ttu-id="0611e-392">電子請求機能を最初から作成する場合は、ER コンポーネントを手動で追加する必要があります (機能バージョンの構成や、機能バージョンの設定やアプリケーションの設定などのその他構成など)。</span><span class="sxs-lookup"><span data-stu-id="0611e-392">When you create an electronic invoicing feature from scratch, you must manually add the ER components (for example, feature version configurations and other configurations, such as the feature version setup and application setup).</span></span> <span data-ttu-id="0611e-393">別の機能から派生させて機能を作成した場合、この新しい機能は元の機能からすべての構成を引き継ぎます。</span><span class="sxs-lookup"><span data-stu-id="0611e-393">When you create a feature by deriving it from another feature, the new feature inherits all configurations from the original.</span></span> 

## <a name="electronic-invoicing-feature-version"></a><span data-ttu-id="0611e-394">電子請求書機能のバージョン</span><span class="sxs-lookup"><span data-stu-id="0611e-394">Electronic invoicing feature version</span></span>

<span data-ttu-id="0611e-395">電子請求書機能の機能はバージョン管理されています。</span><span class="sxs-lookup"><span data-stu-id="0611e-395">The electronic invoicing features are versioned.</span></span> <span data-ttu-id="0611e-396">新しいバージョンを作成すると、バージョン番号が自動的に増番で付与されます。</span><span class="sxs-lookup"><span data-stu-id="0611e-396">When a new version is created, the version number is automatically incremented.</span></span> <span data-ttu-id="0611e-397">新しいバージョンの"有効開始日" を定義できます。</span><span class="sxs-lookup"><span data-stu-id="0611e-397">An "effective from" date can be defined for the new version.</span></span>

<span data-ttu-id="0611e-398">電子請求機能のバージョンは、最大で 3 つのステータスを持つライフサイクルに従います。</span><span class="sxs-lookup"><span data-stu-id="0611e-398">Electronic invoicing feature versions follow a lifecycle that has up to three statuses:</span></span>

- <span data-ttu-id="0611e-399">**下書き** - 機能バージョンがこのステータスにある場合、構成の属性とそのコンポーネント (ファイル形式の構成など)を編集できます。</span><span class="sxs-lookup"><span data-stu-id="0611e-399">**Draft** – If a feature version is in this status, you can edit its configuration attributes and any of its artifacts (for example, file format configurations).</span></span>
- <span data-ttu-id="0611e-400">**完了** - 機能のバージョンがこのステータスの場合は、組織に関連付けられているグローバル リポジトリに公開されている状態を表わします。</span><span class="sxs-lookup"><span data-stu-id="0611e-400">**Complete** – If a feature version is in this status, it has been published to the Global repository that is associated with your organization.</span></span> <span data-ttu-id="0611e-401">機能のバージョン、または ER コンポーネントの編集はできなくなります。</span><span class="sxs-lookup"><span data-stu-id="0611e-401">You can no longer edit the feature version or any of the ER components.</span></span>
- <span data-ttu-id="0611e-402">**公開済み** – 機能のバージョンがこのステータスである場合、電子請求に公開されています。</span><span class="sxs-lookup"><span data-stu-id="0611e-402">**Published** – If a feature version is in this status, it has been published to Electronic invoicing.</span></span> <span data-ttu-id="0611e-403">機能のバージョン、または ER コンポーネントの編集はできなくなります。</span><span class="sxs-lookup"><span data-stu-id="0611e-403">You can no longer edit the feature version or any of the ER components.</span></span>

### <a name="feature-configurations"></a><span data-ttu-id="0611e-404">機能の構成</span><span class="sxs-lookup"><span data-stu-id="0611e-404">Feature configurations</span></span>

<span data-ttu-id="0611e-405">機能の構成には、電子請求機能で使用する ER 形式のすべての構成が保持されます。</span><span class="sxs-lookup"><span data-stu-id="0611e-405">Feature configurations hold all the ER format configurations that the electronic invoicing features use.</span></span> <span data-ttu-id="0611e-406">電子請求書発行機能が処理中に使用するすべての電子ファイルは、その機能の構成に追加されたフォーマット構成に由来します。</span><span class="sxs-lookup"><span data-stu-id="0611e-406">All the electronic files that an electronic invoicing feature uses during processing come from the format configurations that have been added to the feature configurations of that feature.</span></span>

<span data-ttu-id="0611e-407">ER 形式デザイナには、機能の構成からアクセスできます。ER 形式デザイナは、形式の構成を作成するために使用する ER ツールです。</span><span class="sxs-lookup"><span data-stu-id="0611e-407">From the feature configurations, you can access the ER format designer, which is the ER tool that is used to create format configurations.</span></span>

### <a name="feature-setup"></a><span data-ttu-id="0611e-408">機能設定</span><span class="sxs-lookup"><span data-stu-id="0611e-408">Feature setup</span></span>

<span data-ttu-id="0611e-409">機能の設定は、機能ノ構成と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="0611e-409">Feature setups are used in combination with feature configurations.</span></span> <span data-ttu-id="0611e-410">各機能設定は、電子請求書機能が電子請求書の特定の要件を満たせるように、期待される動作を提供するアクション、適用ルール、および変数のセットをカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="0611e-410">Each feature setup encapsulates a set of actions, applicability rules, and variables that provide the expected behavior so that an electronic invoicing feature can meet a specific requirement of the electronic invoice.</span></span>

### <a name="application-setup"></a><span data-ttu-id="0611e-411">アプリケーションの設定</span><span class="sxs-lookup"><span data-stu-id="0611e-411">Application setup</span></span>

<span data-ttu-id="0611e-412">アプリケーションの設定は、既に作成した接続されたアプリケーションに関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="0611e-412">The application setup must be associated with a previously created connected application.</span></span>

<span data-ttu-id="0611e-413">アプリケーションの設定を通じて Finance と Supply Chain Management で行う必要がある電子請求機能の一部を構成できます。</span><span class="sxs-lookup"><span data-stu-id="0611e-413">Through the application setup, you can configure the part of an electronic invoicing feature that must be done in Finance and Supply Chain Management.</span></span> <span data-ttu-id="0611e-414">構成可能なコンポーネントは、電子請求の機能を問わず、少なくとも 3 つ必要となります。</span><span class="sxs-lookup"><span data-stu-id="0611e-414">At least three configurable components are mandatory, regardless of the electronic invoicing feature:</span></span>

- <span data-ttu-id="0611e-415">**テーブル名** : 転記された請求書を保持している、Finance と Supply Chain Management のエンティティ、電子請求書機能がベースになっています。</span><span class="sxs-lookup"><span data-stu-id="0611e-415">**Table name** – The entity in Finance and Supply Chain Management that holds the posted invoices, and that the electronic invoicing feature is based on.</span></span>
- <span data-ttu-id="0611e-416">**コンテキスト** - ER を介して構成された請求書コンテキスト モデルの名前です。</span><span class="sxs-lookup"><span data-stu-id="0611e-416">**Context** – The name of the invoice context model that was configured through ER.</span></span>
- <span data-ttu-id="0611e-417">**ビジネス ドキュメント マッピング** - ER を介して構成された請求書マッピング モデルの名前です。</span><span class="sxs-lookup"><span data-stu-id="0611e-417">**Business document mapping** – The name of the invoice mapping model that was configured through ER.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0611e-418">アプリケーションの設定で入力された構成は、Finance と Supply Chain Management で表示できます。</span><span class="sxs-lookup"><span data-stu-id="0611e-418">The configuration that is entered in the application setup can be viewed in Finance and Supply Chain Management.</span></span> <span data-ttu-id="0611e-419">**組織管理 \> 設定 \> 電子ドキュメント パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="0611e-419">Go to **Organization administration \> Setup \> Electronic document parameter**.</span></span> <span data-ttu-id="0611e-420">**電子ドキュメント** タブ で、**デプロイ** を選択し、**接続済みアプリケーション** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="0611e-420">On the **Electronic document** tab, select **Deploy**, and then select the **Connected application** option.</span></span>

### <a name="deploying-feature-versions"></a><span data-ttu-id="0611e-421">デプロイ機能のバージョン</span><span class="sxs-lookup"><span data-stu-id="0611e-421">Deploying feature versions</span></span>

<span data-ttu-id="0611e-422">RCS では、**デプロイ** コマンドを使用して電子請求機能のバージョンを target-publish します。</span><span class="sxs-lookup"><span data-stu-id="0611e-422">In RCS, you use the **Deploy** command to target-publish an electronic invoicing feature version.</span></span> <span data-ttu-id="0611e-423">**デプロイ** を選択し、次のいずれかのオプションを選択して、デプロイするターゲットを定義します。</span><span class="sxs-lookup"><span data-stu-id="0611e-423">Select **Deploy**, and then select one of the following options to define the target of the deployment:</span></span> 

- <span data-ttu-id="0611e-424">**サービス環境** - デプロイのターゲットがサービス環境の場合は、電子請求機能のバージョンをサービス環境に公開します。</span><span class="sxs-lookup"><span data-stu-id="0611e-424">**Service environment** – When the target of the deployment is the service environment, the electronic invoicing feature version is published to the service environment.</span></span> <span data-ttu-id="0611e-425">これにより、電子請求で Finance および Supply Chain Management が送信する電子ドキュメントを受信して処理することができます。</span><span class="sxs-lookup"><span data-stu-id="0611e-425">Electronic invoicing is then ready to receive and process electronic documents that Finance and Supply Chain Management send.</span></span>
- <span data-ttu-id="0611e-426">**接続済アプリケーション** - デプロイのターゲットが接続されたアプリケーションである場合、アプリケーションの設定で提供される構成は、以前に関連付けらた Finance と Supply Chain Management のインスタンスに記述されます。</span><span class="sxs-lookup"><span data-stu-id="0611e-426">**Connected application** – When the target of the deployment is the connected application, the configuration that is provided by the application setup is written in the Finance and Supply Chain Management instance that was previously associated with it.</span></span>

<span data-ttu-id="0611e-427">サービス環境や接続されたアプリケーションにデプロイできるバージョンは、ステータスが **完了** となっておる電子請求機能のバージョンのみです。</span><span class="sxs-lookup"><span data-stu-id="0611e-427">Only electronic invoicing feature versions that have a status of **Completed** can be deployed to either a service environment or a connected application.</span></span>

### <a name="removing-feature-versions"></a><span data-ttu-id="0611e-428">機能のバージョンを削除する</span><span class="sxs-lookup"><span data-stu-id="0611e-428">Removing feature versions</span></span>

<span data-ttu-id="0611e-429">RCS では、**Undeploy** コマンドを使用して、電子請求のサービス環境から特定の電子請求機能のバージョンを削除します。</span><span class="sxs-lookup"><span data-stu-id="0611e-429">In RCS, you use the **Undeploy** command to remove a specific electronic invoicing feature version from a service environment in Electronic invoicing.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0611e-430">**アンデプロイ** コマンドは、サービス環境でのみ機能します。</span><span class="sxs-lookup"><span data-stu-id="0611e-430">The **Undeploy** command works only in service environments.</span></span> <span data-ttu-id="0611e-431">接続されたアプリケーションからは、電子請求機能のバージョンは削除されません。</span><span class="sxs-lookup"><span data-stu-id="0611e-431">It doesn't remove electronic invoicing feature versions from connected applications.</span></span>

### <a name="rebasing-electronic-invoicing-features"></a><span data-ttu-id="0611e-432">電子請求書発行機能をリベースする</span><span class="sxs-lookup"><span data-stu-id="0611e-432">Rebasing electronic invoicing features</span></span>

<span data-ttu-id="0611e-433">電子請求書の作成機能が別の機能から派生したものである場合、**リベース** コマンドを使用すると、この派生した機能を元の機能に導入された変更を基に更新します。</span><span class="sxs-lookup"><span data-stu-id="0611e-433">When one electronic invoicing feature is derived from another, the **Rebase** command updates the derived feature with the changes that have been introduced in the original feature.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0611e-434">追加リソース</span><span class="sxs-lookup"><span data-stu-id="0611e-434">Additional resources</span></span>

- [<span data-ttu-id="0611e-435">Finance および Supply Chain Management で電子請求書を発行する</span><span class="sxs-lookup"><span data-stu-id="0611e-435">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
