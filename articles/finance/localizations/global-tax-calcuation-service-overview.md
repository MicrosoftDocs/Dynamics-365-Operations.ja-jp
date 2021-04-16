---
title: 税計算サービス (プレビュー)
description: このトピックでは、税計算サービスの全体的な範囲と機能について説明します。
author: wangchen
ms.date: 03/02/2021
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
ms.openlocfilehash: 518d3fda7b97e55d23beea6a1ba0e50b44a7aa0e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818227"
---
# <a name="tax-calculation-service-preview"></a><span data-ttu-id="af18f-103">税計算サービス (プレビュー)</span><span class="sxs-lookup"><span data-stu-id="af18f-103">Tax calculation service (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="af18f-104">税計算サービスは、Global Tax Engine によって税の決定と計算プロセスを自動化および簡素化できる、超スケーラブルなマルチテナント サービスです。</span><span class="sxs-lookup"><span data-stu-id="af18f-104">The tax calculation service is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="af18f-105">税エンジンは完全にコンフィギュレーション可能です。</span><span class="sxs-lookup"><span data-stu-id="af18f-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="af18f-106">設定できる要素には、課税対象データ モデル、税コード、課税適用マトリックス、および税金計算式が含まれますが、これに限定されません。</span><span class="sxs-lookup"><span data-stu-id="af18f-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="af18f-107">税エンジンは  Microsoft Azureコア サービス プラットフォームで実行され、最新のテクノロジと指数関数的なスケーラビリティを提供します。</span><span class="sxs-lookup"><span data-stu-id="af18f-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="af18f-108">税務計算サービスは、Dynamics 365 Finance および Dynamics 365 Supply Chain Management と統合されます。</span><span class="sxs-lookup"><span data-stu-id="af18f-108">The tax calculation service integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="af18f-109">最終的には、Dynamics 365 Project Operations、Dynamics 365 Commerce やその他のファースト パーティ アプリケーションとも統合されます。</span><span class="sxs-lookup"><span data-stu-id="af18f-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

<span data-ttu-id="af18f-110">税計算サービスは、指数関数的なスケーラビリティを提供する Microsoft ベースの税エンジンです。</span><span class="sxs-lookup"><span data-stu-id="af18f-110">The tax calculation service is a Microsoft-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="af18f-111">実行できるスケジューリング タスクは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="af18f-111">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="af18f-112">規制コンフィギュレーション サービス (RCS) を通じて税計算サービスを構成します。</span><span class="sxs-lookup"><span data-stu-id="af18f-112">Configure the tax calculation service through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="af18f-113">RCS は、電子レポート (ER) デザイナの拡張バージョンであり、スタンドアロンのサービスとして利用できます。</span><span class="sxs-lookup"><span data-stu-id="af18f-113">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="af18f-114">税マトリックスを構成して、税コードと税率を自動的に決定します。</span><span class="sxs-lookup"><span data-stu-id="af18f-114">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="af18f-115">税マトリックスを構成して、税登録番号を自動的に決定します。</span><span class="sxs-lookup"><span data-stu-id="af18f-115">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="af18f-116">フォーミュラと条件を定義するには、税計算デザイナーを構成します。</span><span class="sxs-lookup"><span data-stu-id="af18f-116">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="af18f-117">税の決定および計算ソリューションを、複数の法人間で共有します。</span><span class="sxs-lookup"><span data-stu-id="af18f-117">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="af18f-118">税計算サービスを使用するには、Microsoft Dynamics Lifecycle Services (LCS) のプロジェクトから税計算サービス アドインをインストールします。</span><span class="sxs-lookup"><span data-stu-id="af18f-118">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="af18f-119">その後、RCS の設定を完了し、Finance および Supply Chain Management の税計算サービスを有効にしてください。</span><span class="sxs-lookup"><span data-stu-id="af18f-119">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="af18f-120">詳細については、[税サービスの使用を開始する](https://go.microsoft.com/fwlink/?linkid=2138482)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="af18f-120">For more information, see [Get started with tax service](https://go.microsoft.com/fwlink/?linkid=2138482).</span></span>

## <a name="availability"></a><span data-ttu-id="af18f-121">適用の対象</span><span class="sxs-lookup"><span data-stu-id="af18f-121">Availability</span></span>

<span data-ttu-id="af18f-122">税計算サービスは、パブリック プレビュー プログラムを通じて、選択した顧客および複数の税金環境でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="af18f-122">The tax calculation service is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="af18f-123">最終的には、一般にすべての顧客および運用環境で使用できます。</span><span class="sxs-lookup"><span data-stu-id="af18f-123">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="af18f-124">税計算サービスでは、引き続き新しい機能が提供されます。</span><span class="sxs-lookup"><span data-stu-id="af18f-124">New features will continue to be delivered in the tax calculation service.</span></span> <span data-ttu-id="af18f-125">そのため、サポートされる機能の補充と範囲について把握するために最新のドキュメントをチェックしてください。</span><span class="sxs-lookup"><span data-stu-id="af18f-125">Therefore, be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="af18f-126">税計算サービスは、次の Azure 地域に配置されます。</span><span class="sxs-lookup"><span data-stu-id="af18f-126">The tax calculation service is deployed in the following Azure geographies.</span></span> <span data-ttu-id="af18f-127">また、顧客のニーズに基づいて、より多くの Azure 地域にもデプロイされます。</span><span class="sxs-lookup"><span data-stu-id="af18f-127">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="af18f-128">米国</span><span class="sxs-lookup"><span data-stu-id="af18f-128">United States</span></span>
- <span data-ttu-id="af18f-129">ヨーロッパ</span><span class="sxs-lookup"><span data-stu-id="af18f-129">Europe</span></span>
- <span data-ttu-id="af18f-130">フランス</span><span class="sxs-lookup"><span data-stu-id="af18f-130">France</span></span>
- <span data-ttu-id="af18f-131">英国</span><span class="sxs-lookup"><span data-stu-id="af18f-131">United Kingdom</span></span>

> [!NOTE]
> <span data-ttu-id="af18f-132">税計算サービスは、Dynamics 365 のオンプレミス デプロイメントをサポートしません。</span><span class="sxs-lookup"><span data-stu-id="af18f-132">The tax calculation service doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="af18f-133">また、Dynamics 2012 AX などの以前のバージョンはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="af18f-133">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="af18f-134">機能の特徴</span><span class="sxs-lookup"><span data-stu-id="af18f-134">Feature highlights</span></span>

- <span data-ttu-id="af18f-135">税を自動的に決定する構成可能な税マトリックス</span><span class="sxs-lookup"><span data-stu-id="af18f-135">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="af18f-136">複数の付加価値税 (VAT) 登録番号のサポート</span><span class="sxs-lookup"><span data-stu-id="af18f-136">Support for multiple value-added tax (VAT) registration numbers</span></span>
- <span data-ttu-id="af18f-137">税の決定と計算のための移動オーダーのサポート</span><span class="sxs-lookup"><span data-stu-id="af18f-137">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="af18f-138">複数の VAT 登録番号の決定のための移動オーダーのサポート</span><span class="sxs-lookup"><span data-stu-id="af18f-138">Transfer order support for determination of multiple VAT registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="af18f-139">サポートされるトランザクション</span><span class="sxs-lookup"><span data-stu-id="af18f-139">Supported transactions</span></span>

<span data-ttu-id="af18f-140">税計算サービスは、法人およびトランザクション別に有効にできます。</span><span class="sxs-lookup"><span data-stu-id="af18f-140">The tax calculation service can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="af18f-141">次のトランザクションがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="af18f-141">The following transactions are supported:</span></span>

- <span data-ttu-id="af18f-142">販売プロセス</span><span class="sxs-lookup"><span data-stu-id="af18f-142">Sales process</span></span>

    - <span data-ttu-id="af18f-143">販売見積</span><span class="sxs-lookup"><span data-stu-id="af18f-143">Sales quotation</span></span>
    - <span data-ttu-id="af18f-144">販売注文</span><span class="sxs-lookup"><span data-stu-id="af18f-144">Sales order</span></span>
    - <span data-ttu-id="af18f-145">確認書</span><span class="sxs-lookup"><span data-stu-id="af18f-145">Confirmation</span></span>
    - <span data-ttu-id="af18f-146">ピッキング リスト</span><span class="sxs-lookup"><span data-stu-id="af18f-146">Picking list</span></span>
    - <span data-ttu-id="af18f-147">梱包明細</span><span class="sxs-lookup"><span data-stu-id="af18f-147">Packing slip</span></span>
    - <span data-ttu-id="af18f-148">売上請求書</span><span class="sxs-lookup"><span data-stu-id="af18f-148">Sales invoice</span></span>
    - <span data-ttu-id="af18f-149">訂正票</span><span class="sxs-lookup"><span data-stu-id="af18f-149">Credit note</span></span>
    - <span data-ttu-id="af18f-150">返品注文</span><span class="sxs-lookup"><span data-stu-id="af18f-150">Return order</span></span>
    - <span data-ttu-id="af18f-151">ヘッダー雑費</span><span class="sxs-lookup"><span data-stu-id="af18f-151">Header miscellaneous charge</span></span>
    - <span data-ttu-id="af18f-152">明細行の雑費</span><span class="sxs-lookup"><span data-stu-id="af18f-152">Line miscellaneous charge</span></span>

- <span data-ttu-id="af18f-153">購入プロセス</span><span class="sxs-lookup"><span data-stu-id="af18f-153">Purchase process</span></span>

    - <span data-ttu-id="af18f-154">発注書</span><span class="sxs-lookup"><span data-stu-id="af18f-154">Purchase order</span></span>
    - <span data-ttu-id="af18f-155">確認書</span><span class="sxs-lookup"><span data-stu-id="af18f-155">Confirmation</span></span>
    - <span data-ttu-id="af18f-156">入庫リスト</span><span class="sxs-lookup"><span data-stu-id="af18f-156">Receipts list</span></span>
    - <span data-ttu-id="af18f-157">製品受領書</span><span class="sxs-lookup"><span data-stu-id="af18f-157">Product receipt</span></span>
    - <span data-ttu-id="af18f-158">仕入請求書</span><span class="sxs-lookup"><span data-stu-id="af18f-158">Purchase invoice</span></span>
    - <span data-ttu-id="af18f-159">ヘッダー雑費</span><span class="sxs-lookup"><span data-stu-id="af18f-159">Header miscellaneous charge</span></span>
    - <span data-ttu-id="af18f-160">明細行の雑費</span><span class="sxs-lookup"><span data-stu-id="af18f-160">Line miscellaneous charge</span></span>
    - <span data-ttu-id="af18f-161">訂正票</span><span class="sxs-lookup"><span data-stu-id="af18f-161">Credit note</span></span>
    - <span data-ttu-id="af18f-162">返品注文</span><span class="sxs-lookup"><span data-stu-id="af18f-162">Return order</span></span>
    - <span data-ttu-id="af18f-163">購買要求</span><span class="sxs-lookup"><span data-stu-id="af18f-163">Purchase requisition</span></span>
    - <span data-ttu-id="af18f-164">購買要求明細行の雑費</span><span class="sxs-lookup"><span data-stu-id="af18f-164">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="af18f-165">見積依頼</span><span class="sxs-lookup"><span data-stu-id="af18f-165">Request for quotation</span></span>
    - <span data-ttu-id="af18f-166">見積依頼ヘッダーの雑費</span><span class="sxs-lookup"><span data-stu-id="af18f-166">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="af18f-167">見積依頼行の雑費</span><span class="sxs-lookup"><span data-stu-id="af18f-167">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="af18f-168">在庫プロセス</span><span class="sxs-lookup"><span data-stu-id="af18f-168">Inventory process</span></span>

    - <span data-ttu-id="af18f-169">移動オーダー - 出荷</span><span class="sxs-lookup"><span data-stu-id="af18f-169">Transfer order – ship</span></span>
    - <span data-ttu-id="af18f-170">移動オーダー - 入庫</span><span class="sxs-lookup"><span data-stu-id="af18f-170">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="af18f-171">関連するリソース</span><span class="sxs-lookup"><span data-stu-id="af18f-171">Related resources</span></span>

[<span data-ttu-id="af18f-172">税サービスの使用を開始する</span><span class="sxs-lookup"><span data-stu-id="af18f-172">Get started with tax service</span></span>](https://go.microsoft.com/fwlink/?linkid=2138482)

[<span data-ttu-id="af18f-173">複数の VAT 登録番号</span><span class="sxs-lookup"><span data-stu-id="af18f-173">Multiple VAT registration number</span></span>](https://go.microsoft.com/fwlink/?linkid=2153387)

[<span data-ttu-id="af18f-174">移動オーダーに対する税機能のサポート</span><span class="sxs-lookup"><span data-stu-id="af18f-174">Tax feature support for transfer order</span></span>](https://go.microsoft.com/fwlink/?linkid=2153388)

[<span data-ttu-id="af18f-175">税サービスで拡張機能を作成する方法</span><span class="sxs-lookup"><span data-stu-id="af18f-175">How to build extension in tax service</span></span>](https://go.microsoft.com/fwlink/?linkid=2138483)
