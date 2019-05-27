---
title: 最適化アドバイザー
description: このトピックでは、最適化アドバイザーを使用して  Microsoft Dynamics 365 Finance and Operations の最適なコンフィギュレーションを保証する方法について説明します。
author: roxanadiaconu
manager: AnnBe
ms.date: 03/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SelfHealingWorkspace
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: roxanad
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 206b8a23a52d412d1810b8a355b09ecc461f00b3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554946"
---
# <a name="optimization-advisor"></a><span data-ttu-id="f3826-103">最適化アドバイザー</span><span class="sxs-lookup"><span data-stu-id="f3826-103">Optimization advisor</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f3826-104">このトピックでは、最適化アドバイザーを使用して  Microsoft Dynamics 365 Finance and Operations の最適なコンフィギュレーションを保証する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f3826-104">This topic describes how you can use Optimization advisor to help guarantee optimal configuration of Microsoft Dynamics 365 Finance and Operations.</span></span>

## <a name="overview"></a><span data-ttu-id="f3826-105">概要</span><span class="sxs-lookup"><span data-stu-id="f3826-105">Overview</span></span>

<span data-ttu-id="f3826-106">間違ったコンフィギュレーションおよびモジュールの設定は、Finance and Operations、システムのパフォーマンス、および業務プロセスの円滑な操作に大幅な影響を与えかねます。</span><span class="sxs-lookup"><span data-stu-id="f3826-106">Incorrect configuration and setup of a module can adversely affect the availability of features in Finance and Operations, system performance, and the smooth operation of business processes.</span></span> <span data-ttu-id="f3826-107">業務データ (データの正確性、完全性、およびクリーン性など) は、システムのパフォーマンス、組織の意思決定能力、生産性などにも影響します。</span><span class="sxs-lookup"><span data-stu-id="f3826-107">The quality of business data (for example, the correctness, completeness, and cleanliness of the data) also affects system performance, and an organization's decision-making capabilities, productivity, and so on.</span></span>

<span data-ttu-id="f3826-108">**最適化アドバイザー** ワークスペースは、Power Users、業務アナリスト、機能コンサルタント、IT サポート機能がモジュールのコンフィギュレーションや業務データの問題を識別できるようにするツールです。</span><span class="sxs-lookup"><span data-stu-id="f3826-108">The **Optimization advisor** workspace is a tool that lets power users, business analysts, functional consultants, and IT support functions identify issues in module configuration and business data.</span></span> <span data-ttu-id="f3826-109">最適化アドバイザーは、モジュールのコンフィギュレーションのベスト プラクティスを提案し、古い形式または間違っている業務データを識別します。</span><span class="sxs-lookup"><span data-stu-id="f3826-109">Optimization advisor suggests best practices for module configuration and identifies business data that is obsolete or incorrect.</span></span>

<span data-ttu-id="f3826-110">最適化アドバイザーは定期的に一連のベスト プラクティス ルールを実行します。</span><span class="sxs-lookup"><span data-stu-id="f3826-110">Optimization advisor periodically runs a set of best practice rules.</span></span> <span data-ttu-id="f3826-111">既定のルールは Microsoft Dynamics 365 for Finance and Operations バージョン 8.0 (2018 年 4 月) と共にリリースされます。</span><span class="sxs-lookup"><span data-stu-id="f3826-111">A default set of rules is released together with Microsoft Dynamics 365 for Finance and Operations version 8.0 (April 2018).</span></span> <span data-ttu-id="f3826-112">ただし、ユーザーは、独立系ソフトウェア ベンダー (ISV)、およびビジネス データから、カスタマイズ、ソリューションに固有のルールも作成できます。</span><span class="sxs-lookup"><span data-stu-id="f3826-112">However, users can also create rules that are specific to their customizations, solutions from independent software vendors (ISVs), and business data.</span></span> <span data-ttu-id="f3826-113">ルールを作成する方法の詳細については、[新しいルールを作成](./create-rules-optimization-advisor.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f3826-113">For more information about how to create rules, see [Create new rules](./create-rules-optimization-advisor.md).</span></span>

<span data-ttu-id="f3826-114">ルールの違反が検出されると、最適化の機会が生成され、**最適化アドバイザー** ワークスペースに表示されます。</span><span class="sxs-lookup"><span data-stu-id="f3826-114">When a violation of a rule is detected, an optimization opportunity is generated and appears in the **Optimization advisor** workspace.</span></span> <span data-ttu-id="f3826-115">ユーザーは、**最適化アドバイザー** ワークスペースから直接適切な修正アクションを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="f3826-115">A user can take appropriate corrective action directly from the **Optimization advisor** workspace.</span></span>

<span data-ttu-id="f3826-116">営業案件は、検証されている設定とデータの種類に応じて、会社固有のものでも、会社間のものでもかまいません。</span><span class="sxs-lookup"><span data-stu-id="f3826-116">Opportunities can be company-specific or cross-company, depending on the type of setup and data that is being validated.</span></span> <span data-ttu-id="f3826-117">会社間の営業案件は、すべての会社から確認できます。</span><span class="sxs-lookup"><span data-stu-id="f3826-117">Cross-company opportunities can be viewed from all companies.</span></span> <span data-ttu-id="f3826-118">特定の会社の営業案件を見るには、まず会社を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3826-118">To view the opportunities for a specific company, you must first select the company.</span></span>

<span data-ttu-id="f3826-119">最適化の機会には標準的なセキュリティ ポリシーが適用されます。</span><span class="sxs-lookup"><span data-stu-id="f3826-119">Standard security policies apply to optimization opportunities.</span></span> <span data-ttu-id="f3826-120">たとえば、**倉庫管理**モジュールのコンフィギュレーションに関連する最適化の機会などは、倉庫管理にアクセスしてその設定を変更できるユーザーのみに表示されます。</span><span class="sxs-lookup"><span data-stu-id="f3826-120">For example, the optimization opportunities that are related to configuration of the **Warehouse management** module are visible only to users who have access to Warehouse management and can change its setup.</span></span>

<span data-ttu-id="f3826-121">いくつかの最適化の機会を捉えると、システムは業務プロセスのランタイムの短縮という点で営業案件の影響を計算します。</span><span class="sxs-lookup"><span data-stu-id="f3826-121">When you take action on some optimization opportunities, the system calculates the impact of the opportunity in terms of the reduction in the runtime of business processes.</span></span> <span data-ttu-id="f3826-122">ただし、すべての最適化の機会に対して、この機能は有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="f3826-122">Unfortunately, this feature isn't available for all optimization opportunities.</span></span>

<span data-ttu-id="f3826-123">最適化アドバイザーの詳細については、簡単なビデオ [Dynamics 365 for Finance and Operations の最適化アドバイザー](https://www.youtube.com/watch?v=MRsAzgFCUSQ)をご視聴ください。 </span><span class="sxs-lookup"><span data-stu-id="f3826-123">To learn more about Optimization advisor, watch the short [Optimization advisor in Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ) video.</span></span>

## <a name="optimization-rules"></a><span data-ttu-id="f3826-124">最適化ルール</span><span class="sxs-lookup"><span data-stu-id="f3826-124">Optimization rules</span></span>

<span data-ttu-id="f3826-125">最適化アドバイザーのルールの完全なリストを表示し、ルールの評価頻度を確認するには、**システム管理** &gt; **定期処理のタスク** &gt; **診断検証ルールの管理**に移動します。</span><span class="sxs-lookup"><span data-stu-id="f3826-125">To view the complete list of Optimization advisor rules and to see how often the rules are evaluated, go to **System administration** &gt; **Periodic tasks** &gt; **Maintain diagnostics validation rule**.</span></span> <span data-ttu-id="f3826-126">**有効**のステータスがあるルールのみが評価されます。</span><span class="sxs-lookup"><span data-stu-id="f3826-126">Only rules that have a status of **Active** are evaluated.</span></span> <span data-ttu-id="f3826-127">評価頻度は **毎日**、**毎週**、**毎月**、または**未スケジュール** に設定することができます。</span><span class="sxs-lookup"><span data-stu-id="f3826-127">The evaluation frequency can be set to **Daily**, **Weekly**, **Monthly**, or **Unscheduled**.</span></span>

<span data-ttu-id="f3826-128">スケジュールされていないルールの評価をトリガーする、または事前定義されたスケジュール外の定期的なルールを再評価するには、**システム管理** &gt; **定期処理のタスク** &gt; **診断検証ルールのスケジュール**に移動します。</span><span class="sxs-lookup"><span data-stu-id="f3826-128">To trigger the evaluation of unscheduled rules, or to reevaluate periodic rules outside their predefined schedule, go to **System administration** &gt; **Periodic tasks** &gt; **Schedule diagnostics validation rule**.</span></span> <span data-ttu-id="f3826-129">その後、**診断ルールの検証**ダイアログ ボックス内で評価頻度を選択します。</span><span class="sxs-lookup"><span data-stu-id="f3826-129">Then, in the **Diagnostic rule validation** dialog box, select an evaluation frequency.</span></span> <span data-ttu-id="f3826-130">指定された頻度を持つすべてのルールが再評価されます。</span><span class="sxs-lookup"><span data-stu-id="f3826-130">All rules that have the specified frequency will be reevaluated.</span></span>

<span data-ttu-id="f3826-131">現在の最適化ルールのセットは、次のカテゴリに分類できます。</span><span class="sxs-lookup"><span data-stu-id="f3826-131">The current set of optimization rules can be divided into the following categories.</span></span>

### <a name="module-configuration-and-setup"></a><span data-ttu-id="f3826-132">モジュール コンフィギュレーションおよび設定</span><span class="sxs-lookup"><span data-stu-id="f3826-132">Module configuration and setup</span></span>

<span data-ttu-id="f3826-133">倉庫管理の設定は複雑なプロセスです。</span><span class="sxs-lookup"><span data-stu-id="f3826-133">The setup of Warehouse management is a complicated process.</span></span> <span data-ttu-id="f3826-134">プロセスを簡略化するには、設定の正確性を検証するためのルールが導入されています。</span><span class="sxs-lookup"><span data-stu-id="f3826-134">To make the process easier, some rules have been introduced to help validate the correctness of the setup.</span></span> <span data-ttu-id="f3826-135">たとえば、1 つのルールは、販売注文および移動オーダー用の製品バリアントの固定の場所のための、倉庫の場所ディレクティブの設定を検証します。</span><span class="sxs-lookup"><span data-stu-id="f3826-135">For example, one rule validates the setup of warehouse location directives for fixed product variant locations for sales orders and transfer orders.</span></span>

<span data-ttu-id="f3826-136">また、いくつかのルールは、有効になっている機能が実際に使用されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="f3826-136">Additionally, some rules check whether features that have been enabled are actually used.</span></span> <span data-ttu-id="f3826-137">たとえば、1 つのルールは**マスター プラン**モジュールを使用しているかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="f3826-137">For example, one rule determines whether you're using the **Master planning** module.</span></span> <span data-ttu-id="f3826-138">ルールがモジュールを使用していないと判断した場合、計画プロセスを無効にすることを推奨する、最適化の営業案件が生成されます。</span><span class="sxs-lookup"><span data-stu-id="f3826-138">If the rule determines that you aren't using the module, an optimization opportunity is generated to suggest that you turn off the planning processes.</span></span>

### <a name="system-configuration"></a><span data-ttu-id="f3826-139">システム コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="f3826-139">System configuration</span></span>

<span data-ttu-id="f3826-140">コンフィギュレーション キーによって制御される特定の機能が使用されていない場合、コンフィギュレーション キーを無効にするよう提案する最適化の営業案件が生成されます。</span><span class="sxs-lookup"><span data-stu-id="f3826-140">If specific functionality that is controlled by a configuration key isn't used, an optimization opportunity is generated to suggest that you disable the configuration key.</span></span> <span data-ttu-id="f3826-141">コンフィギュレーション キーの例として、**CW**、**予算計画**、**プロジェクト**、および**承認済仕入先リスト**があります。</span><span class="sxs-lookup"><span data-stu-id="f3826-141">Examples of configuration keys include **Catch weight**, **Budget planning**, **Project**, and **Approved vendor list**.</span></span>

### <a name="business-data-consistency-and-cleanup"></a><span data-ttu-id="f3826-142">業務データの整合性とクリーンアップ</span><span class="sxs-lookup"><span data-stu-id="f3826-142">Business data consistency and cleanup</span></span>

<span data-ttu-id="f3826-143">マスター データが正しくない場合 (たとえば、定義されていない単位の測定単位換算がある場合、または 0 \[0\] による除算で測定単位換算がある場合)、データを修正することを提案する、最適化の営業案件が生成されます。</span><span class="sxs-lookup"><span data-stu-id="f3826-143">If master data isn't correct (for example, if you have unit of measure conversions for units that haven't been defined, or if you have unit of measure conversions that have a division by 0 \[zero\]), an optimization opportunity is generated to suggest that you correct the data.</span></span> 

<span data-ttu-id="f3826-144">バッチ ジョブ履歴エントリ、古い品目、倉庫管理対応品目に対する終了した手持在庫エントリなどが多すぎる場合、またはそれらのエントリおよび品目が古すぎる場合、データをクリーンアップするよう提案する最適化の営業案件が生成されます。</span><span class="sxs-lookup"><span data-stu-id="f3826-144">If you have too many batch job history entries, obsolete items, closed on-hand entries for warehouse enabled items, and so on, or if those entries and items are too old, optimization opportunities are generated to suggest that you clean up the data.</span></span> <span data-ttu-id="f3826-145">データを整理しておくことにより、システム全体のパフォーマンスを改善できます。</span><span class="sxs-lookup"><span data-stu-id="f3826-145">By keeping your data clean, you can help improve overall system performance.</span></span>

### <a name="best-practices"></a><span data-ttu-id="f3826-146">ベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="f3826-146">Best practices</span></span>

<span data-ttu-id="f3826-147">ベスト プラクティスに従っていくつかの業務プロセスを実行していない場合 (たとえば、在庫決済前の在庫原価計算の実行、または補助元帳仕訳のバッチ転送に対してスケジュールされているバッチを使用している場合)、最適化の営業案件はベスト プラクティスについて通知し、それに従うよう依頼します。</span><span class="sxs-lookup"><span data-stu-id="f3826-147">If you aren't running some business processes according to best practices (for example, if you run inventory pre-closing before the inventory is closed, or if you use the scheduled batch for subledger journal batch transfer), optimization opportunities inform you about the best practice and ask that you follow it.</span></span>

## <a name="optimization-opportunities"></a><span data-ttu-id="f3826-148">最適化の機会</span><span class="sxs-lookup"><span data-stu-id="f3826-148">Optimization opportunities</span></span>

<span data-ttu-id="f3826-149">最適化ルールの評価中に生成される最適化の機会を表示するには、**最適化アドバイザー** ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="f3826-149">To view the optimization opportunities that are generated during the evaluation of optimization rules, open the **Optimization advisor** workspace.</span></span>

<span data-ttu-id="f3826-150">このワークスペースでは、**詳細情報** を選択することにより営業案件に関する詳細情報を表示できます。</span><span class="sxs-lookup"><span data-stu-id="f3826-150">In this workspace, you can view more information about an opportunity by selecting **More information**.</span></span> <span data-ttu-id="f3826-151">システムがアクションの実行、設定の修正、データのクリーンアップなどをする場合、該当するページを手動で開かないように **アクションの実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f3826-151">If you want the system to take action and correct the setup, clean the data, and so on, so that you don't have to open the corresponding pages yourself, select **Take action**.</span></span>

<span data-ttu-id="f3826-152">最適化の機会のワークフローはありません。</span><span class="sxs-lookup"><span data-stu-id="f3826-152">There is no workflow for optimization opportunities.</span></span> <span data-ttu-id="f3826-153">**アクションの実行**を選択するか、**詳細**ダイアログ ボックスで提供されるナビゲーション パスを使用すると、最適化営業案件がリストから表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="f3826-153">After you select **Take action** or use a navigation path that is provided in the **More information** dialog box, the optimization opportunity disappears from the list.</span></span> <span data-ttu-id="f3826-154">修正アクションが問題を完全に解決しない場合、次にルールが評価されるときにもう一度営業案件が生成されます。</span><span class="sxs-lookup"><span data-stu-id="f3826-154">If the corrective action doesn't completely resolve an issue, the opportunity will be generated again the next time that the rule is evaluated.</span></span>

<span data-ttu-id="f3826-155">営業案件がロールに適用されない場合、**リストから非表示にする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f3826-155">If an opportunity doesn't apply to your role, you can select **Hide from my list**.</span></span> <span data-ttu-id="f3826-156">この営業案件と関連するルールが後でもう一度トリガーされる場合でも、営業案件はリストに表示されません。</span><span class="sxs-lookup"><span data-stu-id="f3826-156">Even if the rule behind this opportunity is triggered again later, you won't see the opportunity in your list.</span></span>

<span data-ttu-id="f3826-157">特定のルールの評価を無効にするには、ルールによって生成された営業案件を選択してから、**分析を無効化**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f3826-157">To deactivate the evaluation of specific rules, select the opportunity that was generated by the rule, and then select **Deactivate analysis**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f3826-158">追加リソース</span><span class="sxs-lookup"><span data-stu-id="f3826-158">Additional resources</span></span>

[<span data-ttu-id="f3826-159">新しいルールの作成</span><span class="sxs-lookup"><span data-stu-id="f3826-159">Create new rules</span></span>](./create-rules-optimization-advisor.md)

[<span data-ttu-id="f3826-160">Dynamics 365 for Finance and Operations の最適化アドバイザー (ビデオ)</span><span class="sxs-lookup"><span data-stu-id="f3826-160">Optimization advisor in Dynamics 365 for Finance and Operations (Video)</span></span>](https://www.youtube.com/watch?v=MRsAzgFCUSQ)
