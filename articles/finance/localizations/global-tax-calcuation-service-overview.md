---
title: 税の計算 (プレビュー)
description: このトピックでは、税計算機能の全体的な範囲と機能について説明します。
author: wangchen
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 3df952e0632807e55f176e63dc2047be5e622ec2
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892352"
---
# <a name="tax-calculation-preview"></a><span data-ttu-id="b43cb-103">税の計算 (プレビュー)</span><span class="sxs-lookup"><span data-stu-id="b43cb-103">Tax Calculation (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="b43cb-104">税計算は、Global Tax Engine によって税の決定と計算プロセスを自動化および簡素化できる、超スケーラブルなマルチテナント サービスです。</span><span class="sxs-lookup"><span data-stu-id="b43cb-104">Tax Calculation is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="b43cb-105">税エンジンは完全にコンフィギュレーション可能です。</span><span class="sxs-lookup"><span data-stu-id="b43cb-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="b43cb-106">設定できる要素には、課税対象データ モデル、税コード、課税適用マトリックス、および税金計算式が含まれますが、これに限定されません。</span><span class="sxs-lookup"><span data-stu-id="b43cb-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="b43cb-107">税エンジンは  Microsoft Azureコア サービス プラットフォームで実行され、最新のテクノロジと指数関数的なスケーラビリティを提供します。</span><span class="sxs-lookup"><span data-stu-id="b43cb-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="b43cb-108">税計算は、Dynamics 365 Finance および Dynamics 365 Supply Chain Management と統合されます。</span><span class="sxs-lookup"><span data-stu-id="b43cb-108">Tax Calculation integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="b43cb-109">最終的には、Dynamics 365 Project Operations、Dynamics 365 Commerce やその他のファースト パーティ アプリケーションとも統合されます。</span><span class="sxs-lookup"><span data-stu-id="b43cb-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

<span data-ttu-id="b43cb-110">税計算は、指数関数的なスケーラビリティを提供するマイクロサービス ベースの税エンジンです。</span><span class="sxs-lookup"><span data-stu-id="b43cb-110">Tax Calculation is a microservice-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="b43cb-111">実行できるスケジューリング タスクは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b43cb-111">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="b43cb-112">Regulatory Configuration Service (RCS) を通じて税計算を構成します。</span><span class="sxs-lookup"><span data-stu-id="b43cb-112">Configure Tax Calculation through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="b43cb-113">RCS は、電子レポート (ER) デザイナの拡張バージョンであり、スタンドアロンのサービスとして利用できます。</span><span class="sxs-lookup"><span data-stu-id="b43cb-113">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="b43cb-114">税マトリックスを構成して、税コードと税率を自動的に決定します。</span><span class="sxs-lookup"><span data-stu-id="b43cb-114">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="b43cb-115">税マトリックスを構成して、税登録番号を自動的に決定します。</span><span class="sxs-lookup"><span data-stu-id="b43cb-115">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="b43cb-116">フォーミュラと条件を定義するには、税計算デザイナーを構成します。</span><span class="sxs-lookup"><span data-stu-id="b43cb-116">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="b43cb-117">税の決定および計算ソリューションを、複数の法人間で共有します。</span><span class="sxs-lookup"><span data-stu-id="b43cb-117">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="b43cb-118">税計算サービスを使用するには、Microsoft Dynamics Lifecycle Services (LCS) のプロジェクトから税計算サービス アドインをインストールします。</span><span class="sxs-lookup"><span data-stu-id="b43cb-118">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="b43cb-119">その後、RCS の設定を完了し、Finance および Supply Chain Management の税計算サービスを有効にしてください。</span><span class="sxs-lookup"><span data-stu-id="b43cb-119">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="b43cb-120">詳細については、[税サービスの使用を開始する](./global-get-started-with-tax-calculation-service.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b43cb-120">For more information, see [Get started with tax service](./global-get-started-with-tax-calculation-service.md).</span></span>

## <a name="availability"></a><span data-ttu-id="b43cb-121">適用の対象</span><span class="sxs-lookup"><span data-stu-id="b43cb-121">Availability</span></span>

<span data-ttu-id="b43cb-122">税計算は、パブリック プレビュー プログラムを通じて、選択した顧客および複数の税金環境でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="b43cb-122">Tax Calculation is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="b43cb-123">最終的には、一般にすべての顧客および運用環境で使用できます。</span><span class="sxs-lookup"><span data-stu-id="b43cb-123">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="b43cb-124">引き続き新しい機能が提供されるため、サポートされる機能の補充と範囲について把握するために最新のドキュメントをチェックしてください。</span><span class="sxs-lookup"><span data-stu-id="b43cb-124">New features will continue to be delivered, so be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="b43cb-125">税計算は、次の Azure 地域に配置されます。</span><span class="sxs-lookup"><span data-stu-id="b43cb-125">Tax Calculation is deployed in the following Azure geographies.</span></span> <span data-ttu-id="b43cb-126">また、顧客のニーズに基づいて、より多くの Azure 地域にもデプロイされます。</span><span class="sxs-lookup"><span data-stu-id="b43cb-126">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="b43cb-127">米国</span><span class="sxs-lookup"><span data-stu-id="b43cb-127">United States</span></span>
- <span data-ttu-id="b43cb-128">ヨーロッパ</span><span class="sxs-lookup"><span data-stu-id="b43cb-128">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="b43cb-129">税計算は、Dynamics 365 のオンプレミス デプロイメントをサポートしません。</span><span class="sxs-lookup"><span data-stu-id="b43cb-129">Tax Calculation doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="b43cb-130">また、Dynamics 2012 AX などの以前のバージョンはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="b43cb-130">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="b43cb-131">機能の特徴</span><span class="sxs-lookup"><span data-stu-id="b43cb-131">Feature highlights</span></span>

- <span data-ttu-id="b43cb-132">税を自動的に決定する構成可能な税マトリックス</span><span class="sxs-lookup"><span data-stu-id="b43cb-132">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="b43cb-133">複数の税登録番号のサポート</span><span class="sxs-lookup"><span data-stu-id="b43cb-133">Support for multiple tax registration numbers</span></span>
- <span data-ttu-id="b43cb-134">税の決定と計算のための移動オーダーのサポート</span><span class="sxs-lookup"><span data-stu-id="b43cb-134">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="b43cb-135">複数の税登録番号の決定のための移動オーダーのサポート</span><span class="sxs-lookup"><span data-stu-id="b43cb-135">Transfer order support for determination of multiple tax registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="b43cb-136">サポートされるトランザクション</span><span class="sxs-lookup"><span data-stu-id="b43cb-136">Supported transactions</span></span>

<span data-ttu-id="b43cb-137">税計算は、法人およびトランザクション別に有効にできます。</span><span class="sxs-lookup"><span data-stu-id="b43cb-137">Tax Calculation can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="b43cb-138">次のトランザクションがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="b43cb-138">The following transactions are supported:</span></span>

- <span data-ttu-id="b43cb-139">販売プロセス</span><span class="sxs-lookup"><span data-stu-id="b43cb-139">Sales process</span></span>

    - <span data-ttu-id="b43cb-140">販売見積</span><span class="sxs-lookup"><span data-stu-id="b43cb-140">Sales quotation</span></span>
    - <span data-ttu-id="b43cb-141">販売注文</span><span class="sxs-lookup"><span data-stu-id="b43cb-141">Sales order</span></span>
    - <span data-ttu-id="b43cb-142">確認書</span><span class="sxs-lookup"><span data-stu-id="b43cb-142">Confirmation</span></span>
    - <span data-ttu-id="b43cb-143">ピッキング リスト</span><span class="sxs-lookup"><span data-stu-id="b43cb-143">Picking list</span></span>
    - <span data-ttu-id="b43cb-144">梱包明細</span><span class="sxs-lookup"><span data-stu-id="b43cb-144">Packing slip</span></span>
    - <span data-ttu-id="b43cb-145">売上請求書</span><span class="sxs-lookup"><span data-stu-id="b43cb-145">Sales invoice</span></span>
    - <span data-ttu-id="b43cb-146">訂正票</span><span class="sxs-lookup"><span data-stu-id="b43cb-146">Credit note</span></span>
    - <span data-ttu-id="b43cb-147">返品注文</span><span class="sxs-lookup"><span data-stu-id="b43cb-147">Return order</span></span>
    - <span data-ttu-id="b43cb-148">ヘッダー雑費</span><span class="sxs-lookup"><span data-stu-id="b43cb-148">Header miscellaneous charge</span></span>
    - <span data-ttu-id="b43cb-149">明細行の雑費</span><span class="sxs-lookup"><span data-stu-id="b43cb-149">Line miscellaneous charge</span></span>

- <span data-ttu-id="b43cb-150">購入プロセス</span><span class="sxs-lookup"><span data-stu-id="b43cb-150">Purchase process</span></span>

    - <span data-ttu-id="b43cb-151">発注書</span><span class="sxs-lookup"><span data-stu-id="b43cb-151">Purchase order</span></span>
    - <span data-ttu-id="b43cb-152">確認書</span><span class="sxs-lookup"><span data-stu-id="b43cb-152">Confirmation</span></span>
    - <span data-ttu-id="b43cb-153">入庫リスト</span><span class="sxs-lookup"><span data-stu-id="b43cb-153">Receipts list</span></span>
    - <span data-ttu-id="b43cb-154">製品受領書</span><span class="sxs-lookup"><span data-stu-id="b43cb-154">Product receipt</span></span>
    - <span data-ttu-id="b43cb-155">仕入請求書</span><span class="sxs-lookup"><span data-stu-id="b43cb-155">Purchase invoice</span></span>
    - <span data-ttu-id="b43cb-156">ヘッダー雑費</span><span class="sxs-lookup"><span data-stu-id="b43cb-156">Header miscellaneous charge</span></span>
    - <span data-ttu-id="b43cb-157">明細行の雑費</span><span class="sxs-lookup"><span data-stu-id="b43cb-157">Line miscellaneous charge</span></span>
    - <span data-ttu-id="b43cb-158">訂正票</span><span class="sxs-lookup"><span data-stu-id="b43cb-158">Credit note</span></span>
    - <span data-ttu-id="b43cb-159">返品注文</span><span class="sxs-lookup"><span data-stu-id="b43cb-159">Return order</span></span>
    - <span data-ttu-id="b43cb-160">購買要求</span><span class="sxs-lookup"><span data-stu-id="b43cb-160">Purchase requisition</span></span>
    - <span data-ttu-id="b43cb-161">購買要求明細行の雑費</span><span class="sxs-lookup"><span data-stu-id="b43cb-161">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="b43cb-162">見積依頼</span><span class="sxs-lookup"><span data-stu-id="b43cb-162">Request for quotation</span></span>
    - <span data-ttu-id="b43cb-163">見積依頼ヘッダーの雑費</span><span class="sxs-lookup"><span data-stu-id="b43cb-163">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="b43cb-164">見積依頼行の雑費</span><span class="sxs-lookup"><span data-stu-id="b43cb-164">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="b43cb-165">在庫プロセス</span><span class="sxs-lookup"><span data-stu-id="b43cb-165">Inventory process</span></span>

    - <span data-ttu-id="b43cb-166">移動オーダー - 出荷</span><span class="sxs-lookup"><span data-stu-id="b43cb-166">Transfer order – ship</span></span>
    - <span data-ttu-id="b43cb-167">移動オーダー - 入庫</span><span class="sxs-lookup"><span data-stu-id="b43cb-167">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="b43cb-168">関連するリソース</span><span class="sxs-lookup"><span data-stu-id="b43cb-168">Related resources</span></span>

[<span data-ttu-id="b43cb-169">税サービスの使用を開始する</span><span class="sxs-lookup"><span data-stu-id="b43cb-169">Get started with tax service</span></span>](./global-get-started-with-tax-calculation-service.md)

[<span data-ttu-id="b43cb-170">複数の VAT 登録番号</span><span class="sxs-lookup"><span data-stu-id="b43cb-170">Multiple VAT registration number</span></span>](./emea-multiple-vat-registration-numbers.md)

[<span data-ttu-id="b43cb-171">移動オーダーに対する税機能のサポート</span><span class="sxs-lookup"><span data-stu-id="b43cb-171">Tax feature support for transfer order</span></span>](./tasks/tax-feature-support-for-transfer-order.md)

[<span data-ttu-id="b43cb-172">税サービスで拡張機能を作成する方法</span><span class="sxs-lookup"><span data-stu-id="b43cb-172">How to build extension in tax service</span></span>](./tax-service-add-data-fields-tax-integration-by-extension.md)