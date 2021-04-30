---
title: 一般会計への補助元帳の転送
description: このトピックでは、一般会計の補助元帳の転送プロセスに関する Microsoft Dynamics 365 Finance での機能について説明します。
author: roschlom
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 1efdf095e379b73d553ca3525abbeee8ca35bcbb
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897507"
---
# <a name="subledger-transfer-to-the-general-ledger"></a><span data-ttu-id="4e28e-103">一般会計への補助元帳の転送</span><span class="sxs-lookup"><span data-stu-id="4e28e-103">Subledger transfer to the General ledger</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4e28e-104">このトピックでは、補助元帳仕訳のバッチの転送のルールに関連する、Microsoft Dynamics 365 Finance での機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="4e28e-104">This topic describes capabilities in Microsoft Dynamics 365 Finance that are related to the rules for transferring batches of subledger journal entries.</span></span>

<span data-ttu-id="4e28e-105">バージョン 8.1 では、ルールの転送を許可するよう変更が加えられ、**同期** オプションは非推奨になりました。</span><span class="sxs-lookup"><span data-stu-id="4e28e-105">In version 8.1, changes were made to allow the transfer of rules, which deprecated the **Synchronous** option.</span></span> <span data-ttu-id="4e28e-106">詳細については、[Finance and Operations の削除済みまたは非推奨の機能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4e28e-106">For more information, see [Removed or deprecated features for Finance and Operations](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).</span></span>

<span data-ttu-id="4e28e-107">次のオプションは、補助元帳バッチの転送に使用できます。</span><span class="sxs-lookup"><span data-stu-id="4e28e-107">The following options are available for transferring subledger batches.</span></span> 

 - <span data-ttu-id="4e28e-108">非同期 – このオプションでは、総勘定元帳への補助元帳勘定項目の転送が直ちにスケジュールされます。</span><span class="sxs-lookup"><span data-stu-id="4e28e-108">Asynchronous – This option will immediately schedule the transfer of the subledger accounting entries to the general ledger.</span></span> <span data-ttu-id="4e28e-109">総勘定元帳伝票は、リソースがサーバー上でこの要求を自由に処理できるようになるとすぐに記録されます。</span><span class="sxs-lookup"><span data-stu-id="4e28e-109">The general ledger voucher will be recorded as soon as resources are free to process this request on the server.</span></span> 

- <span data-ttu-id="4e28e-110">スケジュール済バッチ – このオプションでは、総勘定元帳の処理キューに転送されている補助元帳勘定項目が追加されますが、この項目は、注文を受けた順序で処理されます。</span><span class="sxs-lookup"><span data-stu-id="4e28e-110">Scheduled batch – This option will add the subledger accounting entries that are being transferred to the processing queue in the general ledger, where the entries will be processed in order received.</span></span> <span data-ttu-id="4e28e-111">リソースがサーバー上でこのバッチ ジョブを自由に処理できる場合、総勘定元帳伝票は予定時刻に記録されます。</span><span class="sxs-lookup"><span data-stu-id="4e28e-111">The general ledger voucher will be recorded at the scheduled time if resources are free to process this batch job on the server.</span></span> 
 
<span data-ttu-id="4e28e-112">バージョン 10.0.8 では、非同期オプションのパフォーマンスを向上させるための改良が加えられました。</span><span class="sxs-lookup"><span data-stu-id="4e28e-112">In version 10.0.8, improvements were made to enhance the performance of the Asynchronous option.</span></span> <span data-ttu-id="4e28e-113">この機能は、機能名 **総勘定元帳への補助元帳の転送パフォーマンスの最適化** で有効にできます。</span><span class="sxs-lookup"><span data-stu-id="4e28e-113">This feature is enabled under the feature name **Subledger transfer to General Ledger performance optimization**.</span></span> 
 
<span data-ttu-id="4e28e-114">この機能により、補助元帳から総勘定元帳へのデータの転送が改善されます。</span><span class="sxs-lookup"><span data-stu-id="4e28e-114">This functionality improves the transfer of data from the subledger to the general ledger.</span></span> <span data-ttu-id="4e28e-115">これにより、処理をより効率的にすることができ、転送する一連の小さなトランザクションをグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="4e28e-115">It allows the process to be more efficient, and it groups together sets of smaller transactions to transfer.</span></span> <span data-ttu-id="4e28e-116">これにより、バッチ サーバーの使用がより効率的になります。</span><span class="sxs-lookup"><span data-stu-id="4e28e-116">This allows for a more efficient use of the batch server.</span></span> <span data-ttu-id="4e28e-117">この機能には、バッチ サーバーの設定、オンライン、および非同期転送オプションが作動する機能が必要です。</span><span class="sxs-lookup"><span data-stu-id="4e28e-117">This functionality requires that the batch server be set up, online, and functioning in order for the Asynchronous transfer option to work.</span></span> 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]