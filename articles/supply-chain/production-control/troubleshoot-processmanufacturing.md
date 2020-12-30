---
title: プロセス製造のトラブルシューティング
description: このトピックでは、プロセス製造を操作する際に発生する可能性がある問題の修正方法について説明します。
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 63993fca2164301d31dbfa1474a4cf5eb16273e6
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516819"
---
# <a name="troubleshoot-process-manufacturing"></a><span data-ttu-id="efe12-103">プロセス製造のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="efe12-103">Troubleshoot process manufacturing</span></span>

<span data-ttu-id="efe12-104">このトピックでは、プロセス製造を操作する際に発生する可能性がある問題の修正方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="efe12-104">This topic describes how to fix issues that you might encounter while you work with process manufacturing.</span></span>

## <a name="when-i-use-the-job-card-device-to-report-a-partial-quantity-on-the-last-job-in-a-production-order-all-the-previous-jobs-on-that-order-that-have-a-status-of-in-progress-are-automatically-ended"></a><span data-ttu-id="efe12-105">製造オーダーの最後のジョブで部分的な数量を報告するためにジョブ カード デバイスを使用している場合、その注文の以前のジョブのうち、ステータスが "処理中" になっているものがすべて自動的に終了します。</span><span class="sxs-lookup"><span data-stu-id="efe12-105">When I use the job card device to report a partial quantity on the last job in a production order, all the previous jobs on that order that have a status of In progress are automatically ended.</span></span>

<span data-ttu-id="efe12-106">この動作は仕様です。</span><span class="sxs-lookup"><span data-stu-id="efe12-106">This behavior is by design.</span></span> <span data-ttu-id="efe12-107">**製造オーダーの既定値** ページの **完了レポート** タブに、**エンド マーク ルート** という名前のオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="efe12-107">On the **Production order defaults** page, on the **Report as finished** tab, there is an option that is named **End-mark route**.</span></span> <span data-ttu-id="efe12-108">このトピックが *はい* に設定されている場合は、作業者がジョブ カード デバイスまたはジョブ カード ターミナルを使用して最後の工程を報告したときに、工順カード仕訳帳が転記されます。</span><span class="sxs-lookup"><span data-stu-id="efe12-108">If this topic is set to *Yes*, a route card journal is posted when a worker uses the job card device or job card terminal to report the last operation.</span></span> <span data-ttu-id="efe12-109">この仕訳帳では、すべての工程が完了としてマークされ、すべての生産ジョブが終了します。</span><span class="sxs-lookup"><span data-stu-id="efe12-109">This journal marks all the operations as completed and ends all the production jobs.</span></span> <span data-ttu-id="efe12-110">**エンド マーク ルート** オプションが *はい* に設定されている場合、システムは、前回の工程を報告したときに作業者が選択したジョブ ステータスを考慮しません。</span><span class="sxs-lookup"><span data-stu-id="efe12-110">When the **End-mark route** option is set to *Yes*, the system doesn't consider the job status that the worker selected when they reported the last operation.</span></span> <span data-ttu-id="efe12-111">また、作業者が数量の全体または一部を報告しているかどうかも考慮されません。</span><span class="sxs-lookup"><span data-stu-id="efe12-111">The system also doesn't consider whether the worker is reporting a full or partial quantity.</span></span>

## <a name="when-i-attempt-a-stock-closing-i-receive-the-following-warning-message-no-execution-of-backflush-costing-calculation-with-a-date-1-matching-period-end-has-been-registered"></a><span data-ttu-id="efe12-112">在庫決算を実行しようとすると、"期末と一致する日付 %1 では一括引き落とし原価計算の実行が登録されていません" という警告メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="efe12-112">When I attempt a stock closing, I receive the following warning message: "No execution of Backflush costing calculation with a date %1 matching period end has been registered."</span></span>

<span data-ttu-id="efe12-113">リリース 10.0.13 より前のリリースでは、リーン生産原価計算フローを使用していない場合は、在庫決算中に次の誤った警告メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="efe12-113">In releases before release 10.0.13, if you aren't using the lean production costing flow, you receive the following erroneous warning message during inventory closing:</span></span>

> <span data-ttu-id="efe12-114">日付 %1 で在庫決算を実行しようとしています。</span><span class="sxs-lookup"><span data-stu-id="efe12-114">You are about to execute an Inventory close with a date %1.</span></span> <span data-ttu-id="efe12-115">期末と一致する日付 %1 での一括引き落とし原価計算の実行が登録されていません。</span><span class="sxs-lookup"><span data-stu-id="efe12-115">No execution of Backflush costing calculation with a date %1 matching period end has been registered.</span></span> <span data-ttu-id="efe12-116">期末と一致する日付 %1 での一括引き落とし原価計算を必ず実行してください。</span><span class="sxs-lookup"><span data-stu-id="efe12-116">Please remember to execute a Backflush costing calculation with a date of %1 matching period end.</span></span> <span data-ttu-id="efe12-117">補助元帳および総勘定元帳において、在庫評価、売却済の商品の原価、および差異は、この処理が実行されるまで正しくない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="efe12-117">The valuation of inventories, cost of goods sold and variances might not be correct in Subledger or General ledger until this has been executed.</span></span>

<span data-ttu-id="efe12-118">この問題は、リリース 10.0.13 またはそれ以降で修正されています。</span><span class="sxs-lookup"><span data-stu-id="efe12-118">This issue has been fixed in release 10.0.13 and later.</span></span> <span data-ttu-id="efe12-119">詳細については、[KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="efe12-119">For more information, see [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).</span></span>
