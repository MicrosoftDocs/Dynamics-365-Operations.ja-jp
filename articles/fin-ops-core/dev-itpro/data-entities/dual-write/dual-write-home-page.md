---
title: 二重書き込みホーム ページ
description: このトピックでは、二重書き込みに関する情報へのリンクについて説明します。
author: robinarh
manager: AnnBe
ms.date: 02/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 21311
ms.assetid: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-01-08
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26b8d91adaf561b04c5a2e2ddfe457b21045954b
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5131259"
---
# <a name="dual-write-home-page"></a><span data-ttu-id="e6787-103">二重書き込みホーム ページ</span><span class="sxs-lookup"><span data-stu-id="e6787-103">Dual-write home page</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="e6787-104">次のトピックでは、二重書き込み統合について説明します。</span><span class="sxs-lookup"><span data-stu-id="e6787-104">These topics describe dual-write integration.</span></span>

+ [<span data-ttu-id="e6787-105">二重書き込みとは何ですか?</span><span class="sxs-lookup"><span data-stu-id="e6787-105">What is dual-write?</span></span>](dual-write-overview.md)

    - [<span data-ttu-id="e6787-106">二重書き込みを使用する主な理由</span><span class="sxs-lookup"><span data-stu-id="e6787-106">Top reasons to use dual-write</span></span>](dual-write-overview.md#top-reasons-to-use-dual-write)
    - [<span data-ttu-id="e6787-107">二重書き込みは、Customer Engagement アプリの開発者と設計者に取って何を意味しますか?</span><span class="sxs-lookup"><span data-stu-id="e6787-107">What does dual-write mean for developers and architects of customer engagement app?</span></span>](dual-write-overview.md#developer-architect)

+ [<span data-ttu-id="e6787-108">二重書き込みの新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="e6787-108">What's new or changed in dual-write</span></span>](whats-new-dual-write.md)
+ [<span data-ttu-id="e6787-109">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="e6787-109">Frequently asked questions</span></span>](dual-write-faq.md)    

## <a name="dual-write-setup"></a><span data-ttu-id="e6787-110">二重書き込みの設定</span><span class="sxs-lookup"><span data-stu-id="e6787-110">Dual-write setup</span></span>

+ [<span data-ttu-id="e6787-111">二重書き込みのシステム要件</span><span class="sxs-lookup"><span data-stu-id="e6787-111">System requirements for dual-write</span></span>](dual-write-system-req.md)
+ [<span data-ttu-id="e6787-112">二重書き込みの設定方法に関するガイダンス</span><span class="sxs-lookup"><span data-stu-id="e6787-112">Guidance for how to set up dual-write</span></span>](connection-setup.md)
+ [<span data-ttu-id="e6787-113">初期同期に関する考慮事項</span><span class="sxs-lookup"><span data-stu-id="e6787-113">Considerations for initial synchronization</span></span>](initial-sync-guidance.md)
+ [<span data-ttu-id="e6787-114">Lifecycle Services からの二重書き込みの設定</span><span class="sxs-lookup"><span data-stu-id="e6787-114">Dual-write setup from Lifecycle Services</span></span>](lcs-setup.md)
+ <span data-ttu-id="e6787-115">既存の Finance and Operations アプリの二重書き込みの有効化</span><span class="sxs-lookup"><span data-stu-id="e6787-115">Enable dual-write for existing Finance and Operations apps</span></span>

    + [<span data-ttu-id="e6787-116">既存 Finance and Operations アプリの二重書き込みを有効化</span><span class="sxs-lookup"><span data-stu-id="e6787-116">Enable dual-write for existing Finance and Operations apps</span></span>](enable-dual-write.md)
    + [<span data-ttu-id="e6787-117">システム要件と前提条件</span><span class="sxs-lookup"><span data-stu-id="e6787-117">System requirements and prerequisites</span></span>](requirements-and-prerequisites.md)
    + [<span data-ttu-id="e6787-118">二重書き込みウィザードを使用して環境をリンクする方法</span><span class="sxs-lookup"><span data-stu-id="e6787-118">How to use the dual-write wizard to link your environments</span></span>](link-your-environment.md)
    + [<span data-ttu-id="e6787-119">テーブル マップの二重書き込みの有効化</span><span class="sxs-lookup"><span data-stu-id="e6787-119">Enable table map for dual-write</span></span>](enable-entity-map.md)

+ [<span data-ttu-id="e6787-120">二重書き込みの通貨データ型の移行</span><span class="sxs-lookup"><span data-stu-id="e6787-120">Currency data-type migration for dual-write</span></span>](currrency-decimal-places.md)
+ [<span data-ttu-id="e6787-121">販売注文の状態列のマッピングを設定</span><span class="sxs-lookup"><span data-stu-id="e6787-121">Set up the mapping for the sales order status columns</span></span>](sales-status-map.md)
+ [<span data-ttu-id="e6787-122">会社間注文をフィルター処理して注文および注文明細行の同期を回避する</span><span class="sxs-lookup"><span data-stu-id="e6787-122">Filter intercompany orders to avoid synchronizing Orders and OrderLines</span></span>](filtering-intercompany-orders.md)

## <a name="managing-dual-write-after-setup"></a><span data-ttu-id="e6787-123">設定後の二重書き込みを管理</span><span class="sxs-lookup"><span data-stu-id="e6787-123">Managing dual-write after setup</span></span>

+ [<span data-ttu-id="e6787-124">テーブル マッピングと列マッピングのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="e6787-124">Customize table and column mappings</span></span>](customizing-mappings.md)
+ [<span data-ttu-id="e6787-125">複数のテーブル マップの処理</span><span class="sxs-lookup"><span data-stu-id="e6787-125">Handling multiple table maps</span></span>](multiple-entity-maps.md)
+ [<span data-ttu-id="e6787-126">二重書き込み設定後にリーガル テーブルの編集</span><span class="sxs-lookup"><span data-stu-id="e6787-126">Edit a legal table after dual-write setup</span></span>](edit-legal-entity.md)
+ [<span data-ttu-id="e6787-127">エラー管理と警告通知</span><span class="sxs-lookup"><span data-stu-id="e6787-127">Error management and alert notifications</span></span>](errors-and-alerts.md)
+ [<span data-ttu-id="e6787-128">アプリケーション ライフサイクル管理</span><span class="sxs-lookup"><span data-stu-id="e6787-128">Application lifecycle management</span></span>](app-lifecycle-management.md)

## <a name="mapping-concepts-between-apps"></a><span data-ttu-id="e6787-129">アプリ間の概念のマッピング</span><span class="sxs-lookup"><span data-stu-id="e6787-129">Mapping concepts between apps</span></span>

<span data-ttu-id="e6787-130">このトピックでは、Finance and Operations アプリケーションの概念と Microsoft Dynamics 365 のモデル駆動型アプリの概念間のマッピングについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e6787-130">These topics describe mapping between concepts in Finance and Operations applications and concepts in model-driven apps in Microsoft Dynamics 365.</span></span>

+ [<span data-ttu-id="e6787-131">統合された顧客マスター</span><span class="sxs-lookup"><span data-stu-id="e6787-131">Integrated customer master</span></span>](customer-mapping.md)
+ [<span data-ttu-id="e6787-132">統合された仕入先マスター</span><span class="sxs-lookup"><span data-stu-id="e6787-132">Integrated vendor master</span></span>](vendor-mapping.md)

    + [<span data-ttu-id="e6787-133">仕入先デザインの切り替え</span><span class="sxs-lookup"><span data-stu-id="e6787-133">Switch between vendor designs</span></span>](vendor-switch.md)

+ [<span data-ttu-id="e6787-134">顧客ロイヤルティ カードと報酬ポイント</span><span class="sxs-lookup"><span data-stu-id="e6787-134">Customer loyalty cards and reward points</span></span>](loyalty-mapping.md)
+ [<span data-ttu-id="e6787-135">統一された製品経験</span><span class="sxs-lookup"><span data-stu-id="e6787-135">Unified product experience</span></span>](product-mapping.md)

    + [<span data-ttu-id="e6787-136">統合されたサイトおよび倉庫</span><span class="sxs-lookup"><span data-stu-id="e6787-136">Integrated sites and warehouses</span></span>](sites-warehouses-mapping.md)

+ [<span data-ttu-id="e6787-137">Dataverse 企業理念</span><span class="sxs-lookup"><span data-stu-id="e6787-137">Company concept in Dataverse</span></span>](company-data.md)

    + [<span data-ttu-id="e6787-138">会社データの初期化</span><span class="sxs-lookup"><span data-stu-id="e6787-138">Initialize company data</span></span>](bootstrap-company-data.md)

+ [<span data-ttu-id="e6787-139">組織階層の認識</span><span class="sxs-lookup"><span data-stu-id="e6787-139">Organization hierarchy awareness</span></span>](organization-mapping.md)
+ [<span data-ttu-id="e6787-140">財務および税参照データへのアクセス</span><span class="sxs-lookup"><span data-stu-id="e6787-140">Access to finance and tax reference data</span></span>](finance-tax-reference.md)

    + [<span data-ttu-id="e6787-141">統合された元帳</span><span class="sxs-lookup"><span data-stu-id="e6787-141">Integrated ledger</span></span>](ledger-mapping.md)
    + [<span data-ttu-id="e6787-142">統合された税マスター</span><span class="sxs-lookup"><span data-stu-id="e6787-142">Integrated tax master</span></span>](tax-mapping.md)

+ [<span data-ttu-id="e6787-143">Field Service および Supply Chain Management の調達の統合</span><span class="sxs-lookup"><span data-stu-id="e6787-143">Integrate procurement in Supply Chain Management with Field Service</span></span>](scm-field-service-procurement.md)
+ [<span data-ttu-id="e6787-144">Supply Chain Management の価格エンジンとのオンデマンド同期</span><span class="sxs-lookup"><span data-stu-id="e6787-144">Sync on-demand with the Supply Chain Management price engine</span></span>](pricing-engine.md)
+ [<span data-ttu-id="e6787-145">二重書き込みでの見込顧客の現金化</span><span class="sxs-lookup"><span data-stu-id="e6787-145">Prospect to cash in dual-write</span></span>](dual-write-prospect-to-cash.md)
+ [<span data-ttu-id="e6787-146">サービスのための社内資産</span><span class="sxs-lookup"><span data-stu-id="e6787-146">In-house assets for servicing</span></span>](in-house-assets.md)
+ [<span data-ttu-id="e6787-147">作業者、職務、および職位の統合</span><span class="sxs-lookup"><span data-stu-id="e6787-147">Integrated worker, job, and position</span></span>](integrated-hr.md)
+ [<span data-ttu-id="e6787-148">手持在庫の可用性</span><span class="sxs-lookup"><span data-stu-id="e6787-148">Onhand inventory availability</span></span>](inventory-availability.md)

## <a name="support"></a><span data-ttu-id="e6787-149">サポート</span><span class="sxs-lookup"><span data-stu-id="e6787-149">Support</span></span>

+ [<span data-ttu-id="e6787-150">Field Service と Project Service Automation ソリューションのサポート</span><span class="sxs-lookup"><span data-stu-id="e6787-150">Support for Field Service and Project Service Automation solutions</span></span>](field-service-project-service-automation.md)
+ [<span data-ttu-id="e6787-151">データ統合から二重書き込みへの見込顧客の現金データへの移行</span><span class="sxs-lookup"><span data-stu-id="e6787-151">Migrate Prospect to cash data from Data Integrator to dual-write</span></span>](migrate-prospect-to-cash.md)

## <a name="troubleshooting"></a><span data-ttu-id="e6787-152">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="e6787-152">Troubleshooting</span></span>

+ [<span data-ttu-id="e6787-153">Finance and Operations アプリと Dataverse での二重書き込み構成の確認</span><span class="sxs-lookup"><span data-stu-id="e6787-153">Verify dual-write configuration in Finance and Operations apps and Dataverse</span></span>](dual-write-troubleshooting-verify-config.md)
+ [<span data-ttu-id="e6787-154">初期セットアップ中の問題のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="e6787-154">Troubleshoot issues during initial setup</span></span>](dual-write-troubleshooting-initial-setup.md)
+ [<span data-ttu-id="e6787-155">初期同期中の問題のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="e6787-155">Troubleshoot issues during initial synchronization</span></span>](dual-write-troubleshooting-initial-sync.md)
+ [<span data-ttu-id="e6787-156">Finance and Operations アプリでの二重書き込み問題のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="e6787-156">Troubleshoot dual-write issues in Finance and Operations apps</span></span>](dual-write-troubleshooting-dual-write-module.md)
+ [<span data-ttu-id="e6787-157">ライブ同期の問題のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="e6787-157">Troubleshoot live synchronization issues</span></span>](dual-write-troubleshooting-live-sync.md)
+ [<span data-ttu-id="e6787-158">ソリューションの認識に関する問題のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="e6787-158">Troubleshoot issues related to solution awareness</span></span>](dual-write-troubleshooting-solution-awareness.md)
+ [<span data-ttu-id="e6787-159">Finance and Operations アプリのアップグレードで生じる問題のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="e6787-159">Troubleshoot issues from upgrades of Finance and Operations apps</span></span>](dual-write-troubleshooting-finops-upgrades.md)
+ [<span data-ttu-id="e6787-160">一般的なトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="e6787-160">General troubleshooting</span></span>](dual-write-troubleshooting.md)
