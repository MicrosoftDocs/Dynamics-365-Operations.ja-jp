---
title: Dynamics 365 Talent - Core HR (2018 年 10 月 15 日) の新機能および変更された機能
description: このトピックでは、Microsoft Dynamics 365 Talent - Core HR の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 96f877ae284a0f914bae2d0f5e5f7caf49109511
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461735"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-15-2018"></a><span data-ttu-id="524f7-103">Dynamics 365 Talent - Core HR (2018 年 10 月 15 日) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="524f7-103">What's new or changed in Dynamics 365 Talent - Core HR (October 15, 2018)</span></span>

<span data-ttu-id="524f7-104">**ビルド 8.1.1056**</span><span class="sxs-lookup"><span data-stu-id="524f7-104">**Build 8.1.1056**</span></span>

<span data-ttu-id="524f7-105">このトピックでは、Core HR の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="524f7-105">This topic describes features that are either new or changed in Core HR.</span></span>


## <a name="changes"></a><span data-ttu-id="524f7-106">変更</span><span class="sxs-lookup"><span data-stu-id="524f7-106">Changes</span></span>
<span data-ttu-id="524f7-107">その他の修正プログラムに加え、次の更新プログラムが今回のリリースで行われました。</span><span class="sxs-lookup"><span data-stu-id="524f7-107">In addition to miscellanous fixes, the following updates have been made in this release:</span></span>
- <span data-ttu-id="524f7-108">最終勤務日は、採用時または雇用終了日を設定した時に設定されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="524f7-108">Last Day worked now set when hiring or setting an employment end date.</span></span>
- <span data-ttu-id="524f7-109">米国コンプライアンスの参照は、非米国企業の場合に削除されました (ACA, ADA, and I9)。</span><span class="sxs-lookup"><span data-stu-id="524f7-109">US compliance references removed when in non US companies (ACA, ADA, and I9).</span></span>
- <span data-ttu-id="524f7-110">無効な日付 (1900 年 1 月 1 日) が分析ページで非表示になりました。</span><span class="sxs-lookup"><span data-stu-id="524f7-110">Invalid dates (1/1/1900) are now hidden on analytics pages.</span></span>

## <a name="known-issue"></a><span data-ttu-id="524f7-111">既知の問題</span><span class="sxs-lookup"><span data-stu-id="524f7-111">Known issue</span></span>

<span data-ttu-id="524f7-112">**問題:** 作業者に新しい添付ファイルを追加する場合、**新規** および **編集** ボタンは灰色表示です。**回避策:** 添付ファイル ページを開く前に、**作業者** ページの Factbox が閉じていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="524f7-112">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="524f7-113">**作業者** ページが読み込まれる時、FactBoxes が閉じている場合には、添付ファイルボタンが有効になります。</span><span class="sxs-lookup"><span data-stu-id="524f7-113">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="524f7-114">(この問題は次のプラットフォーム更新プログラムで修正されます。)</span><span class="sxs-lookup"><span data-stu-id="524f7-114">(This issue will be fixed in the next platform update.)</span></span>
