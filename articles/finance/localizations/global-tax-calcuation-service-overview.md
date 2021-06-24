---
title: 税の計算 (プレビュー)
description: このトピックでは、税計算機能の全体的な範囲と機能について説明します。
author: wangchen
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 9daa6e001200d03a2639974fb6de618d77ddf09d
ms.sourcegitcommit: cb282e8d2306ab71adf80a84346a6863d2d019e8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2021
ms.locfileid: "6184104"
---
# <a name="tax-calculation-preview"></a><span data-ttu-id="95c25-103">税の計算 (プレビュー)</span><span class="sxs-lookup"><span data-stu-id="95c25-103">Tax Calculation (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="95c25-104">税計算は、Global Tax Engine によって税の決定と計算プロセスを自動化および簡素化できる、超スケーラブルなマルチテナント サービスです。</span><span class="sxs-lookup"><span data-stu-id="95c25-104">Tax Calculation is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="95c25-105">税エンジンは完全にコンフィギュレーション可能です。</span><span class="sxs-lookup"><span data-stu-id="95c25-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="95c25-106">設定できる要素には、課税対象データ モデル、税コード、課税適用マトリックス、および税金計算式が含まれますが、これに限定されません。</span><span class="sxs-lookup"><span data-stu-id="95c25-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="95c25-107">税エンジンは  Microsoft Azureコア サービス プラットフォームで実行され、最新のテクノロジと指数関数的なスケーラビリティを提供します。</span><span class="sxs-lookup"><span data-stu-id="95c25-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="95c25-108">税計算は、Dynamics 365 Finance および Dynamics 365 Supply Chain Management と統合されます。</span><span class="sxs-lookup"><span data-stu-id="95c25-108">Tax Calculation integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="95c25-109">最終的には、Dynamics 365 Project Operations、Dynamics 365 Commerce やその他のファースト パーティ アプリケーションとも統合されます。</span><span class="sxs-lookup"><span data-stu-id="95c25-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="95c25-110">Tax Calculation サービスを有効にした場合、サービス データを管理するデータ センター以外のデータ センターで、関連データに対する一部の操作が実行される場合があります。</span><span class="sxs-lookup"><span data-stu-id="95c25-110">When you enable the Tax Calculation service, some operations on related data might be performed in a data center other than the data center that maintains your service data.</span></span> <span data-ttu-id="95c25-111">税計算サービスを有効にする前に、[条件](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md) を確認してください。</span><span class="sxs-lookup"><span data-stu-id="95c25-111">Review the [Terms and Conditions](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md) before you enable the Tax Calculation service.</span></span> <span data-ttu-id="95c25-112">Microsoft にとってお客様のプライバシーは重要です。</span><span class="sxs-lookup"><span data-stu-id="95c25-112">Your privacy is important to us.</span></span> <span data-ttu-id="95c25-113">詳細については、Microsoft [プライバシー ステートメント](https://go.microsoft.com/fwlink/?LinkId=521839)をお読みください。</span><span class="sxs-lookup"><span data-stu-id="95c25-113">To learn more, read our [Privacy Statement](https://go.microsoft.com/fwlink/?LinkId=521839).</span></span>

<span data-ttu-id="95c25-114">税計算は、指数関数的なスケーラビリティを提供するマイクロサービス ベースの税エンジンです。</span><span class="sxs-lookup"><span data-stu-id="95c25-114">Tax Calculation is a microservice-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="95c25-115">実行できるスケジューリング タスクは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="95c25-115">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="95c25-116">Regulatory Configuration Service (RCS) を通じて税計算を構成します。</span><span class="sxs-lookup"><span data-stu-id="95c25-116">Configure Tax Calculation through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="95c25-117">RCS は、電子レポート (ER) デザイナの拡張バージョンであり、スタンドアロンのサービスとして利用できます。</span><span class="sxs-lookup"><span data-stu-id="95c25-117">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="95c25-118">税マトリックスを構成して、税コードと税率を自動的に決定します。</span><span class="sxs-lookup"><span data-stu-id="95c25-118">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="95c25-119">税マトリックスを構成して、税登録番号を自動的に決定します。</span><span class="sxs-lookup"><span data-stu-id="95c25-119">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="95c25-120">フォーミュラと条件を定義するには、税計算デザイナーを構成します。</span><span class="sxs-lookup"><span data-stu-id="95c25-120">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="95c25-121">税の決定および計算ソリューションを、複数の法人間で共有します。</span><span class="sxs-lookup"><span data-stu-id="95c25-121">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="95c25-122">税計算サービスを使用するには、Microsoft Dynamics Lifecycle Services (LCS) のプロジェクトから税計算サービス アドインをインストールします。</span><span class="sxs-lookup"><span data-stu-id="95c25-122">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="95c25-123">その後、RCS の設定を完了し、Finance および Supply Chain Management の税計算サービスを有効にしてください。</span><span class="sxs-lookup"><span data-stu-id="95c25-123">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="95c25-124">詳細については、[税サービスの使用を開始する](./global-get-started-with-tax-calculation-service.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="95c25-124">For more information, see [Get started with tax service](./global-get-started-with-tax-calculation-service.md).</span></span>

## <a name="availability"></a><span data-ttu-id="95c25-125">適用の対象</span><span class="sxs-lookup"><span data-stu-id="95c25-125">Availability</span></span>

<span data-ttu-id="95c25-126">税計算は、パブリック プレビュー プログラムを通じて、選択した顧客および複数の税金環境でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="95c25-126">Tax Calculation is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="95c25-127">最終的には、一般にすべての顧客および運用環境で使用できます。</span><span class="sxs-lookup"><span data-stu-id="95c25-127">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="95c25-128">引き続き新しい機能が提供されるため、サポートされる機能の補充と範囲について把握するために最新のドキュメントをチェックしてください。</span><span class="sxs-lookup"><span data-stu-id="95c25-128">New features will continue to be delivered, so be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="95c25-129">税計算は、次の Azure 地域に配置されます。</span><span class="sxs-lookup"><span data-stu-id="95c25-129">Tax Calculation is deployed in the following Azure geographies.</span></span> <span data-ttu-id="95c25-130">また、顧客のニーズに基づいて、より多くの Azure 地域にもデプロイされます。</span><span class="sxs-lookup"><span data-stu-id="95c25-130">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="95c25-131">米国</span><span class="sxs-lookup"><span data-stu-id="95c25-131">United States</span></span>
- <span data-ttu-id="95c25-132">ヨーロッパ</span><span class="sxs-lookup"><span data-stu-id="95c25-132">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="95c25-133">税計算は、Dynamics 365 のオンプレミス デプロイメントをサポートしません。</span><span class="sxs-lookup"><span data-stu-id="95c25-133">Tax Calculation doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="95c25-134">また、Dynamics 2012 AX などの以前のバージョンはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="95c25-134">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="95c25-135">機能の特徴</span><span class="sxs-lookup"><span data-stu-id="95c25-135">Feature highlights</span></span>

- <span data-ttu-id="95c25-136">税を自動的に決定する構成可能な税マトリックス</span><span class="sxs-lookup"><span data-stu-id="95c25-136">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="95c25-137">複数の税登録番号のサポート</span><span class="sxs-lookup"><span data-stu-id="95c25-137">Support for multiple tax registration numbers</span></span>
- <span data-ttu-id="95c25-138">税の決定と計算のための移動オーダーのサポート</span><span class="sxs-lookup"><span data-stu-id="95c25-138">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="95c25-139">複数の税登録番号の決定のための移動オーダーのサポート</span><span class="sxs-lookup"><span data-stu-id="95c25-139">Transfer order support for determination of multiple tax registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="95c25-140">サポートされるトランザクション</span><span class="sxs-lookup"><span data-stu-id="95c25-140">Supported transactions</span></span>

<span data-ttu-id="95c25-141">税計算は、法人およびトランザクション別に有効にできます。</span><span class="sxs-lookup"><span data-stu-id="95c25-141">Tax Calculation can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="95c25-142">次のトランザクションがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="95c25-142">The following transactions are supported:</span></span>

- <span data-ttu-id="95c25-143">販売プロセス</span><span class="sxs-lookup"><span data-stu-id="95c25-143">Sales process</span></span>

    - <span data-ttu-id="95c25-144">販売見積</span><span class="sxs-lookup"><span data-stu-id="95c25-144">Sales quotation</span></span>
    - <span data-ttu-id="95c25-145">販売注文</span><span class="sxs-lookup"><span data-stu-id="95c25-145">Sales order</span></span>
    - <span data-ttu-id="95c25-146">確認書</span><span class="sxs-lookup"><span data-stu-id="95c25-146">Confirmation</span></span>
    - <span data-ttu-id="95c25-147">ピッキング リスト</span><span class="sxs-lookup"><span data-stu-id="95c25-147">Picking list</span></span>
    - <span data-ttu-id="95c25-148">梱包明細</span><span class="sxs-lookup"><span data-stu-id="95c25-148">Packing slip</span></span>
    - <span data-ttu-id="95c25-149">売上請求書</span><span class="sxs-lookup"><span data-stu-id="95c25-149">Sales invoice</span></span>
    - <span data-ttu-id="95c25-150">訂正票</span><span class="sxs-lookup"><span data-stu-id="95c25-150">Credit note</span></span>
    - <span data-ttu-id="95c25-151">返品注文</span><span class="sxs-lookup"><span data-stu-id="95c25-151">Return order</span></span>
    - <span data-ttu-id="95c25-152">ヘッダー雑費</span><span class="sxs-lookup"><span data-stu-id="95c25-152">Header miscellaneous charge</span></span>
    - <span data-ttu-id="95c25-153">明細行の雑費</span><span class="sxs-lookup"><span data-stu-id="95c25-153">Line miscellaneous charge</span></span>

- <span data-ttu-id="95c25-154">購入プロセス</span><span class="sxs-lookup"><span data-stu-id="95c25-154">Purchase process</span></span>

    - <span data-ttu-id="95c25-155">発注書</span><span class="sxs-lookup"><span data-stu-id="95c25-155">Purchase order</span></span>
    - <span data-ttu-id="95c25-156">確認書</span><span class="sxs-lookup"><span data-stu-id="95c25-156">Confirmation</span></span>
    - <span data-ttu-id="95c25-157">入庫リスト</span><span class="sxs-lookup"><span data-stu-id="95c25-157">Receipts list</span></span>
    - <span data-ttu-id="95c25-158">製品受領書</span><span class="sxs-lookup"><span data-stu-id="95c25-158">Product receipt</span></span>
    - <span data-ttu-id="95c25-159">仕入請求書</span><span class="sxs-lookup"><span data-stu-id="95c25-159">Purchase invoice</span></span>
    - <span data-ttu-id="95c25-160">ヘッダー雑費</span><span class="sxs-lookup"><span data-stu-id="95c25-160">Header miscellaneous charge</span></span>
    - <span data-ttu-id="95c25-161">明細行の雑費</span><span class="sxs-lookup"><span data-stu-id="95c25-161">Line miscellaneous charge</span></span>
    - <span data-ttu-id="95c25-162">訂正票</span><span class="sxs-lookup"><span data-stu-id="95c25-162">Credit note</span></span>
    - <span data-ttu-id="95c25-163">返品注文</span><span class="sxs-lookup"><span data-stu-id="95c25-163">Return order</span></span>
    - <span data-ttu-id="95c25-164">購買要求</span><span class="sxs-lookup"><span data-stu-id="95c25-164">Purchase requisition</span></span>
    - <span data-ttu-id="95c25-165">購買要求明細行の雑費</span><span class="sxs-lookup"><span data-stu-id="95c25-165">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="95c25-166">見積依頼</span><span class="sxs-lookup"><span data-stu-id="95c25-166">Request for quotation</span></span>
    - <span data-ttu-id="95c25-167">見積依頼ヘッダーの雑費</span><span class="sxs-lookup"><span data-stu-id="95c25-167">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="95c25-168">見積依頼行の雑費</span><span class="sxs-lookup"><span data-stu-id="95c25-168">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="95c25-169">在庫プロセス</span><span class="sxs-lookup"><span data-stu-id="95c25-169">Inventory process</span></span>

    - <span data-ttu-id="95c25-170">移動オーダー - 出荷</span><span class="sxs-lookup"><span data-stu-id="95c25-170">Transfer order – ship</span></span>
    - <span data-ttu-id="95c25-171">移動オーダー - 入庫</span><span class="sxs-lookup"><span data-stu-id="95c25-171">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="95c25-172">関連するリソース</span><span class="sxs-lookup"><span data-stu-id="95c25-172">Related resources</span></span>

[<span data-ttu-id="95c25-173">税サービスの使用を開始する</span><span class="sxs-lookup"><span data-stu-id="95c25-173">Get started with tax service</span></span>](./global-get-started-with-tax-calculation-service.md)

[<span data-ttu-id="95c25-174">複数の VAT 登録番号</span><span class="sxs-lookup"><span data-stu-id="95c25-174">Multiple VAT registration number</span></span>](./emea-multiple-vat-registration-numbers.md)

[<span data-ttu-id="95c25-175">移動オーダーに対する税機能のサポート</span><span class="sxs-lookup"><span data-stu-id="95c25-175">Tax feature support for transfer order</span></span>](./tasks/tax-feature-support-for-transfer-order.md)

[<span data-ttu-id="95c25-176">税サービスで拡張機能を作成する方法</span><span class="sxs-lookup"><span data-stu-id="95c25-176">How to build extension in tax service</span></span>](./tax-service-add-data-fields-tax-integration-by-extension.md)
