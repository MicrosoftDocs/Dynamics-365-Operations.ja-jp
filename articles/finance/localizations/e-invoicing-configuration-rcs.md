---
title: Regulatory Configuration Services (RCS) で電子請求アドオンを構成する
description: このトピックでは、Dynamics 365 Regulatory Configuration Services (RCS) で電子請求アドオンを構成する方法について説明します。
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: bb4a426bb54ee21197f9954d946d60ea55f5eb76
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104406"
---
# <a name="configure-the-electronic-invoicing-add-on-in-regulatory-configuration-services-rcs"></a><span data-ttu-id="6fdb3-103">Regulatory Configuration Services (RCS) で電子請求アドオンを構成する</span><span class="sxs-lookup"><span data-stu-id="6fdb3-103">Configure the Electronic invoicing add-on in Regulatory Configuration Services (RCS)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6fdb3-104">このトピックでは、Dynamics 365 Regulatory Configuration Services (RCS) の電子請求アドオンの構成機能に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-104">This topic provides information about the configuration capabilities of the Electronic invoicing add-on in Dynamics 365 Regulatory Configuration Services (RCS).</span></span>

<span data-ttu-id="6fdb3-105">この構成機能を通じて、電子請求書アドオンは、コーディングを行うことなく、電子請求書のビジネス要件および規制要件を満たすことができます。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-105">It is through the configuration capabilities that Electronic invoicing add-on helps you meet business and regulatory requirements of electronic invoices without having to do any coding.</span></span> <span data-ttu-id="6fdb3-106">また、Webサービスで電子請求書を電子的に承認する必要がある場合は、この構成機能を使用して、コードを実行せずに Web サービスとメッセージを交換する要件を満たすことができます。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-106">And in the scenarios where electronic invoices must be electronically approved by a web services, the configuration capabilities also help you meet the requirements for exchanging messages with a web services, without doing any code.</span></span>

## <a name="electronic-reporting"></a><span data-ttu-id="6fdb3-107">電子申告</span><span class="sxs-lookup"><span data-stu-id="6fdb3-107">Electronic reporting</span></span>

<span data-ttu-id="6fdb3-108">電子レポート (ER) は、電子請求アドオンに対応しています。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-108">Electronic reporting (ER) supports the Electronic invoicing add-on.</span></span>

<span data-ttu-id="6fdb3-109">データモデルのマッピングと形式は、ER を通して作成・管理され、電子請求書作成アドオンで使用される構成可能なコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-109">The data model mapping and formats are configurable components that are created and maintained through ER and used in the Electronic invoicing add-on.</span></span> <span data-ttu-id="6fdb3-110">ER 形式デザイナは、ファイルの形式を作成・管理するためのツールです。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-110">The ER format designer is the tool for creating and maintaining file formats.</span></span> <span data-ttu-id="6fdb3-111">これは、電子請求機能の構成に使用されます。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-111">It's used to configure the electronic invoicing features.</span></span>

<span data-ttu-id="6fdb3-112">詳細については、[電子申告 (ER) の概要](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-112">For more information, see [Electronic reporting (ER) overview](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).</span></span>

## <a name="electronic-invoicing-features"></a><span data-ttu-id="6fdb3-113">電子請求の機能</span><span class="sxs-lookup"><span data-stu-id="6fdb3-113">Electronic invoicing features</span></span>

<span data-ttu-id="6fdb3-114">電子請求書機能は、電子請求書アドオンを介して電子請求書を生成する役割を担っています。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-114">The electronic invoicing features are responsible for generating electronic invoices through the Electronic invoicing add-on.</span></span> <span data-ttu-id="6fdb3-115">これらは構成ルールをカプセル化し、Microsoft Dynamics 365 Finance と Dynamics 365 Supply Chain Management が電子請求書アドオンや電子請求書に送信するデータを処理するために使用します。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-115">They encapsulate the configuration rules and use them to process the data that Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management send to the Electronic invoicing add-on and to electronic invoices.</span></span>

<span data-ttu-id="6fdb3-116">この機能はまた、ファイル形式の仕様に準拠する必要があり、出力はスタンドアロンの電子ファイルのシナリオにも対応しています。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-116">The features also support scenarios where compliance with file format specifications is required and the output is a standalone electronic file.</span></span> <span data-ttu-id="6fdb3-117">ほとんどの場合、指定のファイル形式は税務当局が公開しています。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-117">In most cases, the file format specifications are published by the tax authority.</span></span>

<span data-ttu-id="6fdb3-118">また、税務当局や認定当事者によってホストされる外部の Web サービスとのメッセージ交換や、電子請求書での認証または承認スタンプの要求に対応しています。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-118">Finally, the features support the exchange of messages with external web services that are hosted either by the tax authority or by some accredited party, and requests for authorization or an approval stamp in the electronic invoice.</span></span>

### <a name="availability-of-electronic-invoicing-features"></a><span data-ttu-id="6fdb3-119">電子請求機能の可用性</span><span class="sxs-lookup"><span data-stu-id="6fdb3-119">Availability of electronic invoicing features</span></span>

<span data-ttu-id="6fdb3-120">電子請求機能の可用性は、国または地域によって異なります。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-120">Availability of the electronic invoicing features depends on the country or region.</span></span> <span data-ttu-id="6fdb3-121">一般公開されている機能もありますが、プレビュー段階の機能もあります。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-121">Although some features are generally available, others are in preview.</span></span>

#### <a name="preview-features"></a><span data-ttu-id="6fdb3-122">プレビュー機能</span><span class="sxs-lookup"><span data-stu-id="6fdb3-122">Preview features</span></span>

<span data-ttu-id="6fdb3-123">次の表に、現在プレビュー中の電子請求機能をまとめています。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-123">The following table shows the electronic invoicing features that are currently in preview.</span></span>

| <span data-ttu-id="6fdb3-124">国/地域</span><span class="sxs-lookup"><span data-stu-id="6fdb3-124">Country/region</span></span> | <span data-ttu-id="6fdb3-125">機能名</span><span class="sxs-lookup"><span data-stu-id="6fdb3-125">Feature name</span></span>                         | <span data-ttu-id="6fdb3-126">ビジネス ドキュメント</span><span class="sxs-lookup"><span data-stu-id="6fdb3-126">Business document</span></span> |
|----------------|--------------------------------------|-------------------|
| <span data-ttu-id="6fdb3-127">オーストリア</span><span class="sxs-lookup"><span data-stu-id="6fdb3-127">Austria</span></span>        | <span data-ttu-id="6fdb3-128">オーストリア 顧客電子請求書 (AT)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-128">Austrian electronic invoices (AT)</span></span>    | <span data-ttu-id="6fdb3-129">売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="6fdb3-129">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="6fdb3-130">ベルギー</span><span class="sxs-lookup"><span data-stu-id="6fdb3-130">Belgium</span></span>        | <span data-ttu-id="6fdb3-131">ベルギー 電子請求書 (BE)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-131">Belgian electronic invoice (BE)</span></span>      | <span data-ttu-id="6fdb3-132">売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="6fdb3-132">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="6fdb3-133">ブラジル</span><span class="sxs-lookup"><span data-stu-id="6fdb3-133">Brazil</span></span>         | <span data-ttu-id="6fdb3-134">ブラジル NF-e (BR)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-134">Brazilian NF-e (BR)</span></span>                  | <span data-ttu-id="6fdb3-135">財政文書モデル 55、督促状、取消書、廃棄物</span><span class="sxs-lookup"><span data-stu-id="6fdb3-135">Fiscal document model 55, correction letters, cancellations, and discards</span></span> |
| <span data-ttu-id="6fdb3-136">ブラジル</span><span class="sxs-lookup"><span data-stu-id="6fdb3-136">Brazil</span></span>         | <span data-ttu-id="6fdb3-137">ブラジル NFS-e ABRASF クリチバ (BR)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-137">Brazilian NFS-e ABRASF Curitiba (BR)</span></span> | <span data-ttu-id="6fdb3-138">会計ドキュメントのサービス</span><span class="sxs-lookup"><span data-stu-id="6fdb3-138">Service fiscal documents</span></span> |
| <span data-ttu-id="6fdb3-139">ブラジル</span><span class="sxs-lookup"><span data-stu-id="6fdb3-139">Brazil</span></span>         | <span data-ttu-id="6fdb3-140">ブラジル NFS-e サンパウロ (BR)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-140">Brazilian NFS-e São Paulo (BR)</span></span>       | <span data-ttu-id="6fdb3-141">会計ドキュメントのサービス</span><span class="sxs-lookup"><span data-stu-id="6fdb3-141">Service fiscal documents</span></span> |
| <span data-ttu-id="6fdb3-142">デンマーク</span><span class="sxs-lookup"><span data-stu-id="6fdb3-142">Denmark</span></span>        | <span data-ttu-id="6fdb3-143">デンマーク 電子請求書 (DK)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-143">Danish electronic invoice (DK)</span></span>       | <span data-ttu-id="6fdb3-144">売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="6fdb3-144">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="6fdb3-145">エジプト</span><span class="sxs-lookup"><span data-stu-id="6fdb3-145">Egypt</span></span>          | <span data-ttu-id="6fdb3-146">エジプト 電子請求書 (EG)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-146">Egyptian electronic invoice (EG)</span></span> | <span data-ttu-id="6fdb3-147">売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="6fdb3-147">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="6fdb3-148">エストニア</span><span class="sxs-lookup"><span data-stu-id="6fdb3-148">Estonia</span></span>        | <span data-ttu-id="6fdb3-149">エストニア 電子請求書 (EE)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-149">Estonian electronic invoice (EE)</span></span>     | <span data-ttu-id="6fdb3-150">売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="6fdb3-150">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="6fdb3-151">フィンランド</span><span class="sxs-lookup"><span data-stu-id="6fdb3-151">Finland</span></span>        | <span data-ttu-id="6fdb3-152">フィンランド 電子請求書 (FI)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-152">Finnish electronic invoice (FI)</span></span>      | <span data-ttu-id="6fdb3-153">売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="6fdb3-153">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="6fdb3-154">フランス</span><span class="sxs-lookup"><span data-stu-id="6fdb3-154">France</span></span>         | <span data-ttu-id="6fdb3-155">フランス 電子請求書 (FR)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-155">French electronic invoice (FR)</span></span>       | <span data-ttu-id="6fdb3-156">売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="6fdb3-156">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="6fdb3-157">ドイツ</span><span class="sxs-lookup"><span data-stu-id="6fdb3-157">Germany</span></span>        | <span data-ttu-id="6fdb3-158">ドイツ 電子請求書 (DE)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-158">German electronic invoice (DE)</span></span>       | <span data-ttu-id="6fdb3-159">売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="6fdb3-159">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="6fdb3-160">イタリア</span><span class="sxs-lookup"><span data-stu-id="6fdb3-160">Italy</span></span>          | <span data-ttu-id="6fdb3-161">FatturaPA (IT)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-161">FatturaPA (IT)</span></span>                       | <span data-ttu-id="6fdb3-162">売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="6fdb3-162">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="6fdb3-163">メキシコ</span><span class="sxs-lookup"><span data-stu-id="6fdb3-163">Mexico</span></span>         | <span data-ttu-id="6fdb3-164">メキシコ CFDI (MX)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-164">Mexican CFDI (MX)</span></span>                    | <span data-ttu-id="6fdb3-165">売上請求書、梱包伝票、在庫振替、支払い補完、キャンセル</span><span class="sxs-lookup"><span data-stu-id="6fdb3-165">Sales invoices, packing slips, inventory transfers, payment complements, and cancellations</span></span> |
| <span data-ttu-id="6fdb3-166">オランダ</span><span class="sxs-lookup"><span data-stu-id="6fdb3-166">Netherlands</span></span>    | <span data-ttu-id="6fdb3-167">オランダ 電子請求書</span><span class="sxs-lookup"><span data-stu-id="6fdb3-167">Dutch electronic invoice (NL)</span></span>        | <span data-ttu-id="6fdb3-168">売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="6fdb3-168">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="6fdb3-169">ノルウェー</span><span class="sxs-lookup"><span data-stu-id="6fdb3-169">Norway</span></span>         | <span data-ttu-id="6fdb3-170">ノルウェー 電子請求書 (NO)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-170">Norwegian electronic invoice (NO)</span></span>    | <span data-ttu-id="6fdb3-171">売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="6fdb3-171">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="6fdb3-172">スペイン</span><span class="sxs-lookup"><span data-stu-id="6fdb3-172">Spain</span></span>          | <span data-ttu-id="6fdb3-173">スペイン 電子請求書 (ES)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-173">Spanish electronic invoice (ES)</span></span>      | <span data-ttu-id="6fdb3-174">売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="6fdb3-174">Sales invoices and project invoices</span></span> |
| <span data-ttu-id="6fdb3-175">ヨーロッパ</span><span class="sxs-lookup"><span data-stu-id="6fdb3-175">Europe</span></span>         | <span data-ttu-id="6fdb3-176">PEPPOL 電子請求書</span><span class="sxs-lookup"><span data-stu-id="6fdb3-176">PEPPOL electronic invoice</span></span>            | <span data-ttu-id="6fdb3-177">PEPPOL 営業の請求書とプロジェクトの請求書</span><span class="sxs-lookup"><span data-stu-id="6fdb3-177">PEPPOL sales invoices and project invoices</span></span> |

### <a name="configurable-components-of-electronic-invoicing-features"></a><span data-ttu-id="6fdb3-178">電子請求機能のコ構成可能なコンポーネント</span><span class="sxs-lookup"><span data-stu-id="6fdb3-178">Configurable components of electronic invoicing features</span></span>

<span data-ttu-id="6fdb3-179">電子請求機能は、構成可能なコンポーネントの次のグループで構成されます。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-179">The electronic invoicing features consist of the following groups of configurable components:</span></span>

- <span data-ttu-id="6fdb3-180">**形式** - 電子ドキュメントが電子請求書になった際に電子請求アドオンで生成する必要がある機能を構成できます。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-180">**Formats** – Formats let you configure what the Electronic invoicing add-on must generate when an electronic document becomes an electronic invoice.</span></span> <span data-ttu-id="6fdb3-181">形式には、電子請求書の形式構成や、外部の Web サービスとの通信が必要な場合にリクエストの送信やレスポンスの受信に使用するファイルやメッセージの形式設定などがあります。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-181">Formats include the format configuration for the electronic invoice, and for files and messages that are used to submit requests and receive responses when communication with an external web service is required.</span></span>
- <span data-ttu-id="6fdb3-182">**アクション** - アクションを使用すると、Finance および Supply Chain Management が電子請求書に送信した電子ドキュメントの変換をどのように生成されるのかを構成できます。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-182">**Actions** – Actions let you configure how the Electronic invoicing add-on generates the transformation of an electronic document that Finance and Supply Chain Management submitted into an electronic invoice.</span></span>
- <span data-ttu-id="6fdb3-183">**適用ルール** - 適用ルールを使用すると、電子請求アドオンで電子請求機能を処理する際に考慮が必要となるコンテキストを構成できます。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-183">**Applicability rules** – Applicability rules let you configure the context that the Electronic invoicing add-on must consider to process an electronic invoicing feature.</span></span>
- <span data-ttu-id="6fdb3-184">**変数** - 変数を使用すると、構成ロジックを構築するサポートを構成できます。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-184">**Variables** – Variables let you configure the support for the construction of the configuration logic.</span></span> <span data-ttu-id="6fdb3-185">変数は、特定のアクションを実行する際の値の入力として機能します。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-185">Variables can work as the input of values to perform a specific action.</span></span> <span data-ttu-id="6fdb3-186">また、Finance および Supply Chain Management と電子請求アドオン間で値の変換として機能することもできます。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-186">Alternatively, they can work as an exchange of values between Finance and Supply Chain Management and the Electronic invoicing add-on.</span></span>
- <span data-ttu-id="6fdb3-187">**電子ドキュメント モデル マッピング** : 電子ドキュメント モデル マッピングを使用すると、ER モデル マッピングを構成できます。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-187">**Electronic document model mapping** – The electronic document model mapping lets you configure the ER model mapping.</span></span> <span data-ttu-id="6fdb3-188">モデル マッピングにより、電子ドキュメントの送信時に電子請求アドオンに統合される抽象請求書のデータ マッピングが定義されます。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-188">The model mapping defines the data mapping of the abstract invoice that is integrated into the Electronic invoicing add-on when electronic documents are submitted.</span></span>
- <span data-ttu-id="6fdb3-189">**請求書コンテキスト モデル** - 請求書コンテキスト モデルを使用すると、ER 請求書コンテキスト モデルを構成し、電子請求機能のコンテキストを定義できます。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-189">**Invoice context model** – The invoice context model lets you configure the ER invoice context model and define the context of an electronic invoicing feature.</span></span>
- <span data-ttu-id="6fdb3-190">**応答タイプ** - 応答タイプを使用すると、電子請求処理の結果として Finance および Supply Chain Management で電子請求アドオンを更新する必要がある項目を設定できます。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-190">**Response types** – Response types let you configure what the Electronic invoicing add-on must update in Finance and Supply Chain Management as a result of the electronic invoice processing.</span></span>

### <a name="formats"></a><span data-ttu-id="6fdb3-191">形式</span><span class="sxs-lookup"><span data-stu-id="6fdb3-191">Formats</span></span>

<span data-ttu-id="6fdb3-192">次の一覧は、電子請求機能に使用可能な ER 形式の構成を示しています。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-192">The following lists show the ER format configurations that are available for the electronic invoicing features.</span></span>

#### <a name="austrian-at-electronic-invoices-sales-and-project-invoices-for-austria"></a><span data-ttu-id="6fdb3-193">オーストリア (AT) 電子請求書 : オーストリア向け、売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="6fdb3-193">Austrian (AT) electronic invoices: Sales and project invoices for Austria</span></span>

- <span data-ttu-id="6fdb3-194">OIOUBL 売上請求書</span><span class="sxs-lookup"><span data-stu-id="6fdb3-194">OIOUBL Sales invoice</span></span>
- <span data-ttu-id="6fdb3-195">OIOUBL プロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="6fdb3-195">OIOUBL Project invoice</span></span>
- <span data-ttu-id="6fdb3-196">OIOUBL 売上訂正票</span><span class="sxs-lookup"><span data-stu-id="6fdb3-196">OIOUBL Sales credit note</span></span>
- <span data-ttu-id="6fdb3-197">OIOUBL プロジェクト訂正票</span><span class="sxs-lookup"><span data-stu-id="6fdb3-197">OIOUBL Project credit note</span></span>

#### <a name="belgian-be-electronic-invoice-sales-and-project-invoices-for-belgium"></a><span data-ttu-id="6fdb3-198">ベルギー (BE) 電子請求書 : ベルギー向け、売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="6fdb3-198">Belgian (BE) electronic invoice: Sales and project invoices for Belgium</span></span>

- <span data-ttu-id="6fdb3-199">UBL 売上請求書 BE</span><span class="sxs-lookup"><span data-stu-id="6fdb3-199">UBL Sales invoice BE</span></span>
- <span data-ttu-id="6fdb3-200">UBL プロジェクト請求書 BE</span><span class="sxs-lookup"><span data-stu-id="6fdb3-200">UBL Project invoice BE</span></span>
- <span data-ttu-id="6fdb3-201">UBL プロジェクト訂正票 BE</span><span class="sxs-lookup"><span data-stu-id="6fdb3-201">UBL Project credit note BE</span></span>
- <span data-ttu-id="6fdb3-202">UBL 売上訂正票 BE</span><span class="sxs-lookup"><span data-stu-id="6fdb3-202">UBL Sales credit note BE</span></span>

#### <a name="brazilian-br-nf-e-nf-e-federal-brazil"></a><span data-ttu-id="6fdb3-203">ブラジル (BR) NF-e: NF-e Federal (ブラジル)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-203">Brazilian (BR) NF-e: NF-e Federal (Brazil)</span></span>

- <span data-ttu-id="6fdb3-204">NF-e 送信エクスポートの形式 (BR)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-204">NF-e submit export format (BR)</span></span>
- <span data-ttu-id="6fdb3-205">NF-e 督促状エクスポートの形式 (BR)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-205">NF-e correction letter export format (BR)</span></span>
- <span data-ttu-id="6fdb3-206">NF-e キャンセル エクスポートの形式 (BR)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-206">NF-e cancel export format (BR)</span></span>
- <span data-ttu-id="6fdb3-207">NF-e 破棄エクスポートの形式 (BR)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-207">NF-e discard export format (BR)</span></span>

#### <a name="brazilian-nfs-e-br-nfs-e-abrasf-curitiba-city"></a><span data-ttu-id="6fdb3-208">ブラジル NFS-e (BR): NFS-e ABRASF クリチバ市</span><span class="sxs-lookup"><span data-stu-id="6fdb3-208">Brazilian NFS-e (BR): NFS-e ABRASF Curitiba city</span></span>

- <span data-ttu-id="6fdb3-209">NFS-e ABRASF クリチバ (BR)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-209">NFS-e ABRASF Curitiba (BR)</span></span>
- <span data-ttu-id="6fdb3-210">NFS-e ABRASF 調査書 クリチバ (BR)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-210">NFS-e ABRASF Inquire Curitiba (BR)</span></span>

#### <a name="brazilian-br-nfs-e-nfs-e-so-paulo-city"></a><span data-ttu-id="6fdb3-211">ブラジル (BR) NFS-e: NFS-e サンパウロ市</span><span class="sxs-lookup"><span data-stu-id="6fdb3-211">Brazilian (BR) NFS-e: NFS-e São Paulo city</span></span>

- <span data-ttu-id="6fdb3-212">NFS-e サンパウロ (BR)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-212">NFS-e Sao Paulo (BR)</span></span>

#### <a name="danish-dk-electronic-invoice-sales-and-project-invoices-for-denmark"></a><span data-ttu-id="6fdb3-213">デンマーク (BE) 電子請求書 : デンマーク向け、売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="6fdb3-213">Danish (DK) electronic invoice: Sales and project invoices for Denmark</span></span>

- <span data-ttu-id="6fdb3-214">OIOUBL 売上請求書</span><span class="sxs-lookup"><span data-stu-id="6fdb3-214">OIOUBL Sales invoice</span></span>
- <span data-ttu-id="6fdb3-215">OIOUBL プロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="6fdb3-215">OIOUBL Project invoice</span></span>
- <span data-ttu-id="6fdb3-216">OIOUBL 売上訂正票</span><span class="sxs-lookup"><span data-stu-id="6fdb3-216">OIOUBL Sales credit note</span></span>
- <span data-ttu-id="6fdb3-217">OIOUBL プロジェクト訂正票</span><span class="sxs-lookup"><span data-stu-id="6fdb3-217">OIOUBL Project credit note</span></span>

#### <a name="dutch-nl-electronic-invoice-sales-and-project-invoices-for-netherlands"></a><span data-ttu-id="6fdb3-218">オランダ (NL) 電子請求書 : オランダ向け、売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="6fdb3-218">Dutch (NL) electronic invoice: Sales and project invoices for Netherlands</span></span>

- <span data-ttu-id="6fdb3-219">UBL 売上請求書 NL</span><span class="sxs-lookup"><span data-stu-id="6fdb3-219">UBL Sales invoice NL</span></span>
- <span data-ttu-id="6fdb3-220">UBL プロジェクト請求書 NL</span><span class="sxs-lookup"><span data-stu-id="6fdb3-220">UBL Project invoice NL</span></span>
- <span data-ttu-id="6fdb3-221">UBL プロジェクト訂正票 NL</span><span class="sxs-lookup"><span data-stu-id="6fdb3-221">UBL Project credit note NL</span></span>
- <span data-ttu-id="6fdb3-222">UBL 売上訂正票 NL</span><span class="sxs-lookup"><span data-stu-id="6fdb3-222">UBL Sales credit note NL</span></span>

#### <a name="egyptian-eg-electronic-invoice-sales-and-project-invoices-for-egypt"></a><span data-ttu-id="6fdb3-223">エジプト (BE) 電子請求書 : エジプト向け、売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="6fdb3-223">Egyptian (EG) electronic invoice: Sales and project invoices for Egypt</span></span>

- <span data-ttu-id="6fdb3-224">売上請求書(EG)(請求書)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-224">Sales invoice (EG)(Invoicing)</span></span>
- <span data-ttu-id="6fdb3-225">プロジェクト請求書(EG)(請求書)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-225">Project invoice (EG)(Invoicing)</span></span>

#### <a name="estonian-ee-electronic-invoice-sales-and-project-invoices-for-estonia"></a><span data-ttu-id="6fdb3-226">エストニア (BE) 電子請求書 : エストニア向け、売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="6fdb3-226">Estonian (EE) electronic invoice: Sales and project invoices for Estonia</span></span>

- <span data-ttu-id="6fdb3-227">売上請求書 (EE)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-227">Sales invoice (EE)</span></span>
- <span data-ttu-id="6fdb3-228">プロジェクト請求書 (EE)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-228">Project invoice (EE)</span></span>

#### <a name="finnish-fi-electronic-invoice-sales-and-project-invoices-for-finland"></a><span data-ttu-id="6fdb3-229">フィンランド (FI) 電子請求書 : フィンランド向け、売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="6fdb3-229">Finnish (FI) electronic invoice: Sales and project invoices for Finland</span></span>

- <span data-ttu-id="6fdb3-230">売上請求書 (FI)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-230">Sales invoice (FI)</span></span>
- <span data-ttu-id="6fdb3-231">プロジェクト請求書 (FI)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-231">Project invoice (FI)</span></span>

#### <a name="french-fr-electronic-invoice-sales-and-project-invoices-for-france"></a><span data-ttu-id="6fdb3-232">フランス (FR) 電子請求書 : フランス向け、売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="6fdb3-232">French (FR) electronic invoice: Sales and project invoices for France</span></span>

- <span data-ttu-id="6fdb3-233">UBL 売上請求書 FR</span><span class="sxs-lookup"><span data-stu-id="6fdb3-233">UBL Sales invoice FR</span></span>
- <span data-ttu-id="6fdb3-234">UBL プロジェクト請求書 FR</span><span class="sxs-lookup"><span data-stu-id="6fdb3-234">UBL Project invoice FR</span></span>
- <span data-ttu-id="6fdb3-235">UBL プロジェクト訂正票 FR</span><span class="sxs-lookup"><span data-stu-id="6fdb3-235">UBL Project credit note FR</span></span>
- <span data-ttu-id="6fdb3-236">UBL 売上訂正票 FR</span><span class="sxs-lookup"><span data-stu-id="6fdb3-236">UBL Sales credit note FR</span></span>

#### <a name="german-de-electronic-invoice-sales-and-project-invoices-for-germany"></a><span data-ttu-id="6fdb3-237">ドイツ (DE) 電子請求書 : ドイツ向け、売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="6fdb3-237">German (DE) electronic invoice: Sales and project invoices for Germany</span></span>

- <span data-ttu-id="6fdb3-238">売上請求書 (DE)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-238">Sales invoice (DE)</span></span>
- <span data-ttu-id="6fdb3-239">プロジェクト請求書 (DE)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-239">Project invoice (DE)</span></span>

#### <a name="italian-it-electronic-invoice-sales-and-project-invoices-for-italy"></a><span data-ttu-id="6fdb3-240">イタリア (IT) 電子請求書 : イタリア向け、売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="6fdb3-240">Italian (IT) electronic invoice: Sales and project invoices for Italy</span></span>

- <span data-ttu-id="6fdb3-241">売上請求書 (IT)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-241">Sales invoice (IT)</span></span>
- <span data-ttu-id="6fdb3-242">プロジェクト請求書 (IT)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-242">Project invoice (IT)</span></span>

#### <a name="mexican-mx-cfdi-cfdi-for-mexico"></a><span data-ttu-id="6fdb3-243">メキシコ (MX) CFDI: メキシコ向け CFDI</span><span class="sxs-lookup"><span data-stu-id="6fdb3-243">Mexican (MX) CFDI: CFDI for Mexico</span></span>

- <span data-ttu-id="6fdb3-244">CFDI 請求書フォーマット (MX)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-244">CFDI invoice format (MX)</span></span>
- <span data-ttu-id="6fdb3-245">CFDI 梱包明細 (MX)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-245">CFDI Packing slip (MX)</span></span>
- <span data-ttu-id="6fdb3-246">CFDI 在庫振替 (MX)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-246">CFDI Inventory transfer (MX)</span></span>
- <span data-ttu-id="6fdb3-247">CFDI 支払い形式 (MX)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-247">CFDI payment format (MX)</span></span>
- <span data-ttu-id="6fdb3-248">CFDI 請求書キャンセル形式 (MX)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-248">CFDI invoice cancel format (MX)</span></span>

#### <a name="norwegian-no-electronic-invoice-sales-and-project-invoices-for-norway"></a><span data-ttu-id="6fdb3-249">ノルウェー (BE) 電子請求書 : ノルウェー向け、売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="6fdb3-249">Norwegian (NO) electronic invoice: Sales and project invoices for Norway</span></span>

- <span data-ttu-id="6fdb3-250">OIOUBL 売上請求書</span><span class="sxs-lookup"><span data-stu-id="6fdb3-250">OIOUBL Sales invoice</span></span>
- <span data-ttu-id="6fdb3-251">OIOUBL プロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="6fdb3-251">OIOUBL Project invoice</span></span>
- <span data-ttu-id="6fdb3-252">OIOUBL 売上訂正票</span><span class="sxs-lookup"><span data-stu-id="6fdb3-252">OIOUBL Sales credit note</span></span>
- <span data-ttu-id="6fdb3-253">OIOUBL プロジェクト訂正票</span><span class="sxs-lookup"><span data-stu-id="6fdb3-253">OIOUBL Project credit note</span></span>

#### <a name="peppol-electronic-invoice-peppol-sales-and-project-invoices"></a><span data-ttu-id="6fdb3-254">PEPPOL 電子請求書 :PEPPOL 売上とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="6fdb3-254">PEPPOL electronic invoice: PEPPOL sales and project invoices</span></span>

- <span data-ttu-id="6fdb3-255">PEPPOL 売上請求書</span><span class="sxs-lookup"><span data-stu-id="6fdb3-255">PEPPOL Sales invoice</span></span>
- <span data-ttu-id="6fdb3-256">PEPPOL プロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="6fdb3-256">PEPPOL Project invoice</span></span>
- <span data-ttu-id="6fdb3-257">PEPPOL 売上訂正票</span><span class="sxs-lookup"><span data-stu-id="6fdb3-257">PEPPOL Sales credit note</span></span>
- <span data-ttu-id="6fdb3-258">PEPPOL プロジェクト訂正票</span><span class="sxs-lookup"><span data-stu-id="6fdb3-258">PEPPOL Project credit note</span></span>

#### <a name="spanish-es-electronic-invoice-sales-and-project-invoices-for-spain"></a><span data-ttu-id="6fdb3-259">スペイン (ES) 電子請求書 : スペイン向け、売上請求書とプロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="6fdb3-259">Spanish (ES) electronic invoice: Sales and project invoices for Spain</span></span>

- <span data-ttu-id="6fdb3-260">売上請求書 (ES)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-260">Sales invoice (ES)</span></span>
- <span data-ttu-id="6fdb3-261">プロジェクト請求書 (ES)</span><span class="sxs-lookup"><span data-stu-id="6fdb3-261">Project invoice (ES)</span></span>

### <a name="actions"></a><span data-ttu-id="6fdb3-262">アクション</span><span class="sxs-lookup"><span data-stu-id="6fdb3-262">Actions</span></span>

<span data-ttu-id="6fdb3-263">次の表では、利用可能なアクションと、現在一般利用可能なのか、プレビュー段階であるのかを示しています。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-263">The following table lists the available actions, and whether they are currently generally available or still in preview.</span></span>

| <span data-ttu-id="6fdb3-264">操作</span><span class="sxs-lookup"><span data-stu-id="6fdb3-264">Action</span></span>                                        | <span data-ttu-id="6fdb3-265">説明</span><span class="sxs-lookup"><span data-stu-id="6fdb3-265">Description</span></span>                                                                  | <span data-ttu-id="6fdb3-266">適用の対象</span><span class="sxs-lookup"><span data-stu-id="6fdb3-266">Availability</span></span>         |
|-----------------------------------------------|------------------------------------------------------------------------------|----------------------|
| <span data-ttu-id="6fdb3-267">ドキュメントの変換</span><span class="sxs-lookup"><span data-stu-id="6fdb3-267">Transform document</span></span>                            | <span data-ttu-id="6fdb3-268">電子レポート形式を実行してドキュメントを変換します。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-268">Run Electronic Reporting format to transform the document.</span></span>                   | <span data-ttu-id="6fdb3-269">一般に入手可能</span><span class="sxs-lookup"><span data-stu-id="6fdb3-269">Generally available</span></span>  |
| <span data-ttu-id="6fdb3-270">xml ドキュメントへの署名</span><span class="sxs-lookup"><span data-stu-id="6fdb3-270">Sign xml document</span></span>                             | <span data-ttu-id="6fdb3-271">デジタル署名を使用して XML ドキュメントに署名します。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-271">Sign xml documents with digital signature.</span></span>                                   | <span data-ttu-id="6fdb3-272">プレビュー</span><span class="sxs-lookup"><span data-stu-id="6fdb3-272">In preview</span></span>           |
| <span data-ttu-id="6fdb3-273">エジプト税務当局に向けた json 文書に署名する</span><span class="sxs-lookup"><span data-stu-id="6fdb3-273">Sign json document for Egyptian Tax Authority</span></span> | <span data-ttu-id="6fdb3-274">エジプト税務局の電子署名で json 文書に署名します。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-274">Sign json documents with digital signature for Egyptian Tax Authority.</span></span>       | <span data-ttu-id="6fdb3-275">一般に入手可能</span><span class="sxs-lookup"><span data-stu-id="6fdb3-275">Generally available</span></span>  |
| <span data-ttu-id="6fdb3-276">エジプト ETA サービスとの統合</span><span class="sxs-lookup"><span data-stu-id="6fdb3-276">Integrate with Egyptian ETA service</span></span>           | <span data-ttu-id="6fdb3-277">エジプト税務当局とのやりとりを行います。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-277">Communicate with Egyptian Tax Authority.</span></span>                                     | <span data-ttu-id="6fdb3-278">一般に入手可能</span><span class="sxs-lookup"><span data-stu-id="6fdb3-278">Generally available</span></span>  |
| <span data-ttu-id="6fdb3-279">ブラジル SEFAZ サービスの呼び出し</span><span class="sxs-lookup"><span data-stu-id="6fdb3-279">Call Brazilian SEFAZ Service</span></span>                  | <span data-ttu-id="6fdb3-280">ブラジルの SEFAZ サービスと統合して会計書類を提出します。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-280">Integrate with Brazilian SEFAZ service for fiscal document submission.</span></span>       | <span data-ttu-id="6fdb3-281">プレビュー</span><span class="sxs-lookup"><span data-stu-id="6fdb3-281">In preview</span></span>           |
| <span data-ttu-id="6fdb3-282">メキシコ PAC サービスの呼び出し</span><span class="sxs-lookup"><span data-stu-id="6fdb3-282">Call Mexican PAC Service</span></span>                      | <span data-ttu-id="6fdb3-283">CFDI 提出に向けたメキシコ PAC サービスとの統合を行います。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-283">Integrate with Mexican PAC service for CFDI submission.</span></span>                      | <span data-ttu-id="6fdb3-284">プレビュー</span><span class="sxs-lookup"><span data-stu-id="6fdb3-284">In preview</span></span>           |
| <span data-ttu-id="6fdb3-285">応答の処理</span><span class="sxs-lookup"><span data-stu-id="6fdb3-285">Process response</span></span>                              | <span data-ttu-id="6fdb3-286">Web サービス コールから受信した応答を分析します。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-286">Analyze the response received from the web service call.</span></span>                     | <span data-ttu-id="6fdb3-287">一般に入手可能</span><span class="sxs-lookup"><span data-stu-id="6fdb3-287">Generally available</span></span>  |
| <span data-ttu-id="6fdb3-288">MS Power Automate を使用する</span><span class="sxs-lookup"><span data-stu-id="6fdb3-288">Use MS Power Automate</span></span>                         | <span data-ttu-id="6fdb3-289">Microsoft Power Automate に組み込まれたフローとの統合をします。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-289">Integrate with flow built in Microsoft Power Automate.</span></span>                       | <span data-ttu-id="6fdb3-290">プレビュー</span><span class="sxs-lookup"><span data-stu-id="6fdb3-290">In preview</span></span>           |

## <a name="configuration-providers"></a><span data-ttu-id="6fdb3-291">コンフィギュレーション提供者</span><span class="sxs-lookup"><span data-stu-id="6fdb3-291">Configuration providers</span></span>

<span data-ttu-id="6fdb3-292">構成プロバイダーは、電子請求書発行機能とその ER コンポーネント (モデル マッピング、フォーマット構成、コンテキスト モデルなど) を提供します。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-292">Configuration providers provide the electronic invoicing features and their ER components, such as the model mapping, format configuration, and context model.</span></span> <span data-ttu-id="6fdb3-293">関連するグローバル リポジトリで電子請求書発行機能と ER コンポーネントが公開されています。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-293">They publish the electronic invoicing features and ER components in the associated Global repository.</span></span> <span data-ttu-id="6fdb3-294">そこから他の組織がダウンロードできるようになっています。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-294">From there, other organizations can download them.</span></span>

<span data-ttu-id="6fdb3-295">RCS を介した電子請求書発行機能の構成を行う前に、 **電子レポート** モジュールの構成プロバイダーに独自の組織を構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-295">Before you configure the electronic invoicing features through RCS, you must configure your own organization as a configuration provider in the **Electronic reporting** module.</span></span> <span data-ttu-id="6fdb3-296">構成プロバイダーを **有効化** に設定する方法については、[構成プロバイダーを作成して有効化としてマークする](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-296">For information about how to set a configuration provider to **Active**, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="viewing-electronic-invoicing-features-in-the-global-repository"></a><span data-ttu-id="6fdb3-297">グローバル リポジトリでの電子請求機能を表示する</span><span class="sxs-lookup"><span data-stu-id="6fdb3-297">Viewing electronic invoicing features in the Global repository</span></span>

<span data-ttu-id="6fdb3-298">特定の構成プロバイダのグローバル リポジトリで利用可能な電子請求書発行機能を閲覧するには、組織の RCS インスタンスを同期します。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-298">To browse the electronic invoicing features that are available in the Global repository for a specific configuration provider, sync your organization's RCS instance.</span></span> <span data-ttu-id="6fdb3-299">同期が完了すると、使用可能な電子請求機能の一覧が更新されます。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-299">After synchronization is completed, the list of available electronic invoicing features is updated.</span></span>

## <a name="importing-electronic-invoicing-features"></a><span data-ttu-id="6fdb3-300">電子請求書機能のインポート</span><span class="sxs-lookup"><span data-stu-id="6fdb3-300">Importing electronic invoicing features</span></span>

<span data-ttu-id="6fdb3-301">電子請求機能を使用・構成する前に、組織の RCS インスタンスにインポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-301">Before you use or configure the electronic invoicing features, you must import them into your organization's RCS instance.</span></span> <span data-ttu-id="6fdb3-302">インポート操作により、機能のローカル コピーが作成され、機能で使用する ER コンポーネント (構成やモデル構成の書式設定など) が組織の RCS インスタンスにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-302">The import operation creates a local copy of the features and copies all the ER artifacts that the features use (for example, format configurations and model configurations) to your organization's RCS instance.</span></span>

<span data-ttu-id="6fdb3-303">任意の構成プロバイダから電子請求機能をインポートできます。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-303">You can import the electronic invoicing features from any configuration provider.</span></span>

## <a name="creating-electronic-invoicing-features"></a><span data-ttu-id="6fdb3-304">電子請求書機能の作成</span><span class="sxs-lookup"><span data-stu-id="6fdb3-304">Creating electronic invoicing features</span></span>

<span data-ttu-id="6fdb3-305">ゼロから電子請求書機能を作成することも、別の電子請求書機能から派生させることもできます。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-305">You can create an electronic invoicing feature from scratch, or you can derive it from another electronic invoicing feature.</span></span>

<span data-ttu-id="6fdb3-306">電子請求機能を最初から作成する場合は、ER コンポーネントを手動で追加する必要があります (機能バージョンの構成や、機能バージョンの設定やアプリケーションの設定などのその他構成など)。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-306">When you create an electronic invoicing feature from scratch, you must manually add the ER components (for example, feature version configurations and other configurations, such as the feature version setup and application setup).</span></span> <span data-ttu-id="6fdb3-307">別の機能から派生させて機能を作成した場合、この新しい機能は元の機能からすべての構成を引き継ぎます。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-307">When you create a feature by deriving it from another feature, the new feature inherits all configurations from the original.</span></span> 

## <a name="electronic-invoicing-feature-version"></a><span data-ttu-id="6fdb3-308">電子請求書機能のバージョン</span><span class="sxs-lookup"><span data-stu-id="6fdb3-308">Electronic invoicing feature version</span></span>

<span data-ttu-id="6fdb3-309">電子請求書機能の機能はバージョン管理されています。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-309">The electronic invoicing features are versioned.</span></span> <span data-ttu-id="6fdb3-310">新しいバージョンを作成すると、バージョン番号が自動的に増番で付与されます。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-310">When a new version is created, the version number is automatically incremented.</span></span> <span data-ttu-id="6fdb3-311">新しいバージョンの"有効開始日" を定義できます。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-311">An "effective from" date can be defined for the new version.</span></span>

<span data-ttu-id="6fdb3-312">電子請求機能のバージョンは、最大で 3 つのステータスを持つライフサイクルに従います。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-312">Electronic invoicing feature versions follow a lifecycle that has up to three statuses:</span></span>

- <span data-ttu-id="6fdb3-313">**下書き** - 機能バージョンがこのステータスにある場合、構成の属性とそのコンポーネント (ファイル形式の構成など)を編集できます。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-313">**Draft** – If a feature version is in this status, you can edit its configuration attributes and any of its artifacts (for example, file format configurations).</span></span>
- <span data-ttu-id="6fdb3-314">**完了** - 機能のバージョンがこのステータスの場合は、組織に関連付けられているグローバル リポジトリに公開されている状態を表わします。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-314">**Complete** – If a feature version is in this status, it has been published to the Global repository that is associated with your organization.</span></span> <span data-ttu-id="6fdb3-315">機能のバージョン、または ER コンポーネントの編集はできなくなります。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-315">You can no longer edit the feature version or any of the ER components.</span></span>
- <span data-ttu-id="6fdb3-316">**公開済** - 機能のバージョンがこのステータスの場合は、電子請求アドオンに発行されています。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-316">**Published** – If a feature version is in this status, it has been published to the Electronic invoicing add-on.</span></span> <span data-ttu-id="6fdb3-317">機能のバージョン、または ER コンポーネントの編集はできなくなります。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-317">You can no longer edit the feature version or any of the ER components.</span></span>

### <a name="feature-configurations"></a><span data-ttu-id="6fdb3-318">機能の構成</span><span class="sxs-lookup"><span data-stu-id="6fdb3-318">Feature configurations</span></span>

<span data-ttu-id="6fdb3-319">機能の構成には、電子請求機能で使用する ER 形式のすべての構成が保持されます。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-319">Feature configurations hold all the ER format configurations that the electronic invoicing features use.</span></span> <span data-ttu-id="6fdb3-320">電子請求書発行機能が処理中に使用するすべての電子ファイルは、その機能の構成に追加されたフォーマット構成に由来します。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-320">All the electronic files that an electronic invoicing feature uses during processing come from the format configurations that have been added to the feature configurations of that feature.</span></span>

<span data-ttu-id="6fdb3-321">ER 形式デザイナには、機能の構成からアクセスできます。ER 形式デザイナは、形式の構成を作成するために使用する ER ツールです。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-321">From the feature configurations, you can access the ER format designer, which is the ER tool that is used to create format configurations.</span></span>

### <a name="feature-setup"></a><span data-ttu-id="6fdb3-322">機能設定</span><span class="sxs-lookup"><span data-stu-id="6fdb3-322">Feature setup</span></span>

<span data-ttu-id="6fdb3-323">機能の設定は、機能ノ構成と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-323">Feature setups are used in combination with feature configurations.</span></span> <span data-ttu-id="6fdb3-324">各機能設定は、電子請求書機能が電子請求書の特定の要件を満たせるように、期待される動作を提供するアクション、適用ルール、および変数のセットをカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-324">Each feature setup encapsulates a set of actions, applicability rules, and variables that provide the expected behavior so that an electronic invoicing feature can meet a specific requirement of the electronic invoice.</span></span>

### <a name="application-setup"></a><span data-ttu-id="6fdb3-325">アプリケーションの設定</span><span class="sxs-lookup"><span data-stu-id="6fdb3-325">Application setup</span></span>

<span data-ttu-id="6fdb3-326">アプリケーションの設定は、既に作成した接続されたアプリケーションに関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-326">The application setup must be associated with a previously created connected application.</span></span>

<span data-ttu-id="6fdb3-327">アプリケーションの設定を通じて Finance と Supply Chain Management で行う必要がある電子請求機能の一部を構成できます。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-327">Through the application setup, you can configure the part of an electronic invoicing feature that must be done in Finance and Supply Chain Management.</span></span> <span data-ttu-id="6fdb3-328">構成可能なコンポーネントは、電子請求の機能を問わず、少なくとも 3 つ必要となります。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-328">At least three configurable components are mandatory, regardless of the electronic invoicing feature:</span></span>

- <span data-ttu-id="6fdb3-329">**テーブル名** : 転記された請求書を保持している、Finance と Supply Chain Management のエンティティ、電子請求書機能がベースになっています。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-329">**Table name** – The entity in Finance and Supply Chain Management that holds the posted invoices, and that the electronic invoicing feature is based on.</span></span>
- <span data-ttu-id="6fdb3-330">**コンテキスト** - ER を介して構成された請求書コンテキスト モデルの名前です。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-330">**Context** – The name of the invoice context model that was configured through ER.</span></span>
- <span data-ttu-id="6fdb3-331">**ビジネス ドキュメント マッピング** - ER を介して構成された請求書マッピング モデルの名前です。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-331">**Business document mapping** – The name of the invoice mapping model that was configured through ER.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6fdb3-332">アプリケーションの設定で入力された構成は、Finance と Supply Chain Management で表示できます。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-332">The configuration that is entered in the application setup can be viewed in Finance and Supply Chain Management.</span></span> <span data-ttu-id="6fdb3-333">**組織管理 \> 設定 \> 電子ドキュメント パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-333">Go to **Organization administration \> Setup \> Electronic document parameter**.</span></span> <span data-ttu-id="6fdb3-334">**電子ドキュメント** タブ で、**デプロイ** を選択し、**接続済みアプリケーション** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-334">On the **Electronic document** tab, select **Deploy**, and then select the **Connected application** option.</span></span>

### <a name="deploying-feature-versions"></a><span data-ttu-id="6fdb3-335">デプロイ機能のバージョン</span><span class="sxs-lookup"><span data-stu-id="6fdb3-335">Deploying feature versions</span></span>

<span data-ttu-id="6fdb3-336">RCS では、**デプロイ** コマンドを使用して電子請求機能のバージョンを target-publish します。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-336">In RCS, you use the **Deploy** command to target-publish an electronic invoicing feature version.</span></span> <span data-ttu-id="6fdb3-337">**デプロイ** を選択し、次のいずれかのオプションを選択して、デプロイするターゲットを定義します。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-337">Select **Deploy**, and then select one of the following options to define the target of the deployment:</span></span> 

- <span data-ttu-id="6fdb3-338">**サービス環境** - デプロイのターゲットがサービス環境の場合は、電子請求機能のバージョンをサービス環境に公開します。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-338">**Service environment** – When the target of the deployment is the service environment, the electronic invoicing feature version is published to the service environment.</span></span> <span data-ttu-id="6fdb3-339">以上で、電子請求アドオンが、Finance と Supply Chain Management から送信された電子ドキュメントの受信と処理をする準備が整います。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-339">The Electronic invoicing add-on is then ready to receive and process electronic documents that Finance and Supply Chain Management send.</span></span>
- <span data-ttu-id="6fdb3-340">**接続済アプリケーション** - デプロイのターゲットが接続されたアプリケーションである場合、アプリケーションの設定で提供される構成は、以前に関連付けらた Finance と Supply Chain Management のインスタンスに記述されます。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-340">**Connected application** – When the target of the deployment is the connected application, the configuration that is provided by the application setup is written in the Finance and Supply Chain Management instance that was previously associated with it.</span></span>

<span data-ttu-id="6fdb3-341">サービス環境や接続されたアプリケーションにデプロイできるバージョンは、ステータスが **完了** となっておる電子請求機能のバージョンのみです。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-341">Only electronic invoicing feature versions that have a status of **Completed** can be deployed to either a service environment or a connected application.</span></span>

### <a name="removing-feature-versions"></a><span data-ttu-id="6fdb3-342">機能のバージョンを削除する</span><span class="sxs-lookup"><span data-stu-id="6fdb3-342">Removing feature versions</span></span>

<span data-ttu-id="6fdb3-343">RCS では、**アンデプロイ** コマンドを使用して、電子請求アドオンのサービス環境から特定の電子請求機能のバージョンを削除します。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-343">In RCS, you use the **Undeploy** command to remove a specific electronic invoicing feature version from a service environment in the Electronic invoicing add-on.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6fdb3-344">**アンデプロイ** コマンドは、サービス環境でのみ機能します。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-344">The **Undeploy** command works only in service environments.</span></span> <span data-ttu-id="6fdb3-345">接続されたアプリケーションからは、電子請求機能のバージョンは削除されません。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-345">It doesn't remove electronic invoicing feature versions from connected applications.</span></span>

### <a name="rebasing-electronic-invoicing-features"></a><span data-ttu-id="6fdb3-346">電子請求書発行機能をリベースする</span><span class="sxs-lookup"><span data-stu-id="6fdb3-346">Rebasing electronic invoicing features</span></span>

<span data-ttu-id="6fdb3-347">電子請求書の作成機能が別の機能から派生したものである場合、**リベース** コマンドを使用すると、この派生した機能を元の機能に導入された変更を基に更新します。</span><span class="sxs-lookup"><span data-stu-id="6fdb3-347">When one electronic invoicing feature is derived from another, the **Rebase** command updates the derived feature with the changes that have been introduced in the original feature.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6fdb3-348">追加リソース</span><span class="sxs-lookup"><span data-stu-id="6fdb3-348">Additional resources</span></span>

- [<span data-ttu-id="6fdb3-349">Finance および Supply Chain Management で電子請求書を発行する</span><span class="sxs-lookup"><span data-stu-id="6fdb3-349">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)
