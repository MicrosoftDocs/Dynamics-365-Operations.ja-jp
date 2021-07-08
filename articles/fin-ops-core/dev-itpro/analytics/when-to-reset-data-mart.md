---
title: データ マートのリセットに関する FAQ
description: このトピックでは、データ マートのリセットに関してよくある質問に対する回答を示します。
author: jinniew
ms.date: 06/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7cd96c7bc698986ef1ef07ca88479a3d49f22924
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266612"
---
# <a name="data-mart-resets-faq"></a><span data-ttu-id="55403-103">データ マートのリセットに関する FAQ</span><span class="sxs-lookup"><span data-stu-id="55403-103">Data mart resets FAQ</span></span>

<span data-ttu-id="55403-104">このトピックでは、データ マートのリセットに関してよくある質問に対する回答を示します。</span><span class="sxs-lookup"><span data-stu-id="55403-104">This topic provides answers to some frequently asked questions about data mart resets.</span></span> <span data-ttu-id="55403-105">データ マートのリセットには時間がかかる場合があり、状況によっては、必要なソリューションではない場合があります。</span><span class="sxs-lookup"><span data-stu-id="55403-105">A reset of the data mart can be a time-consuming process and, depending on the circumstances, might not be the solution that is required.</span></span> <span data-ttu-id="55403-106">したがって、このトピックには、データ マートのリセットが役立つ可能性がある状況、およびそれが役立ちそうにない状況に関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="55403-106">Therefore, this topic includes information about circumstances where a data mart reset might help and also circumstances where it's unlikely to help.</span></span>

## <a name="what-is-a-data-mart-reset"></a><span data-ttu-id="55403-107">データ マート リセットとは何ですか。</span><span class="sxs-lookup"><span data-stu-id="55403-107">What is a data mart reset?</span></span>

<span data-ttu-id="55403-108">データ マート リセットを実行すると、統合タスクが無効になり、すべてのデータ マート データが削除されてから、統合が再度有効になります。</span><span class="sxs-lookup"><span data-stu-id="55403-108">A data mart reset will disable the integration tasks, delete all the data mart data, and then re-enable integration.</span></span>

<span data-ttu-id="55403-109">古いデータを確実に挿入するため、既存のタスクの完了後にのみデータ マートのリセットを開始できます。</span><span class="sxs-lookup"><span data-stu-id="55403-109">To ensure that old data isn't inserted, a data mart reset can be started only after existing tasks are completed.</span></span> <span data-ttu-id="55403-110">すべてのタスクが完了する前にデータ マートをリセットしようとすると、次のエラーメッセージが表示される可能性があります。「有効なタスクが原因でデータ マートのリセットを処理できませんでした。</span><span class="sxs-lookup"><span data-stu-id="55403-110">If you try to reset the data mart before all tasks are completed, you might receive a message such as, "The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="55403-111">後でもう一度お試しください。」</span><span class="sxs-lookup"><span data-stu-id="55403-111">Please try again later."</span></span>

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a><span data-ttu-id="55403-112">データ マート リセットはいつ実行する必要がありますか?</span><span class="sxs-lookup"><span data-stu-id="55403-112">When do I have to do a data mart reset?</span></span>

<span data-ttu-id="55403-113">次のステートメントの 1 つ以上が状況に当てはまる場合、組織はデータ マート リセットのメリットを利用できます:</span><span class="sxs-lookup"><span data-stu-id="55403-113">If one or more of the following statements apply to your situation, your organization can benefit from a data mart reset:</span></span>

- <span data-ttu-id="55403-114">アプリケーション データベースが復元されました。</span><span class="sxs-lookup"><span data-stu-id="55403-114">The application database was restored.</span></span>
- <span data-ttu-id="55403-115">サポート チケットを開いて、サポート エンジニアから、トラブルシューティングの手順の一環としてデータ マートをリセットするように指示されました。</span><span class="sxs-lookup"><span data-stu-id="55403-115">You opened a support ticket, and a Support engineer instructed you to reset the data mart as part of a troubleshooting step.</span></span>
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a><span data-ttu-id="55403-116">データ マートのリセットが不適切なのはいつですか?</span><span class="sxs-lookup"><span data-stu-id="55403-116">When is a data mart reset inappropriate?</span></span>

<span data-ttu-id="55403-117">データ マートのリセットをお勧めできないいくつかの状況があります:</span><span class="sxs-lookup"><span data-stu-id="55403-117">Here are some of the circumstances where we don't recommend that you reset the data mart:</span></span>

- <span data-ttu-id="55403-118">データ同期に関連するパフォーマンス問題が発生しています。</span><span class="sxs-lookup"><span data-stu-id="55403-118">You're experiencing performance issues that are associated with data synchronization.</span></span>
- <span data-ttu-id="55403-119">次のいずれかの理由により、リセット パターンが繰り返し発生します:</span><span class="sxs-lookup"><span data-stu-id="55403-119">You have a recurring reset pattern for any of the following reasons:</span></span>

    - <span data-ttu-id="55403-120">**欠落しているデータ** – データが欠落している場合は、Microsoft のサポート チケットを開き、レポート形式と可能なデータ同期の問題を確認します。</span><span class="sxs-lookup"><span data-stu-id="55403-120">**Missing data** – If you notice that data is missing, open a support ticket with Microsoft to review your report format and possible data synchronization issues.</span></span>
    - <span data-ttu-id="55403-121">**統合の行き詰まり状態**</span><span class="sxs-lookup"><span data-stu-id="55403-121">**Stuck integration state**</span></span>
    - <span data-ttu-id="55403-122">**古いレコード** – 古いレコード自体は、必ずしもデータ マートのリセットを正当化するわけではありません。</span><span class="sxs-lookup"><span data-stu-id="55403-122">**Stale records** – Stale records by themselves don't necessarily justify a data mart reset.</span></span> <span data-ttu-id="55403-123">大規模なデータ セットがある場合、リセット プロセスの実行に時間がかかりますが、改善につながる可能性はほとんどありません。</span><span class="sxs-lookup"><span data-stu-id="55403-123">If you have a large data set, the reset process will take some time to run but is unlikely to lead to any improvement.</span></span>

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a><span data-ttu-id="55403-124">データ マートをリセットすると、デザインしたレポートが失われますか。</span><span class="sxs-lookup"><span data-stu-id="55403-124">If I reset the data mart, will I lose reports that I've already designed?</span></span>

<span data-ttu-id="55403-125">いいえ。</span><span class="sxs-lookup"><span data-stu-id="55403-125">No.</span></span> <span data-ttu-id="55403-126">レポートは、データ マートのリセットの影響を受けない SQL テーブルに格納されます。</span><span class="sxs-lookup"><span data-stu-id="55403-126">Your reports are stored in SQL tables that aren't affected by a data mart reset.</span></span> <span data-ttu-id="55403-127">デザインしたレポートが失われるのではないかと心配な場合は、失いたくないデザインをバックアップできます。</span><span class="sxs-lookup"><span data-stu-id="55403-127">If you're concerned about losing reports that you've designed, you can back up the designs that you don't want to lose.</span></span> <span data-ttu-id="55403-128">デザインをバックアップするには、レポート デザイナーを開き、**会社 \> 会社 \> 構成要素 \> エクスポート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="55403-128">To back up designs, open Report Designer, and go to **Company \> Companies \> Building Blocks \> Export**.</span></span>
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a><span data-ttu-id="55403-129">データ マートをリセットする前に、すべてのユーザーがシステムを終了する必要がありますか?</span><span class="sxs-lookup"><span data-stu-id="55403-129">Do all users have to exit the system before I can reset the data mart?</span></span>

<span data-ttu-id="55403-130">いいえ。</span><span class="sxs-lookup"><span data-stu-id="55403-130">No.</span></span> <span data-ttu-id="55403-131">データ マート リセット中でも、ユーザーはシステムで作業を続行できます。</span><span class="sxs-lookup"><span data-stu-id="55403-131">Users can continue to work in the system during a data mart reset.</span></span> <span data-ttu-id="55403-132">ただしユーザーは、リセットが完了するまで、Financial Reporter を使用して作成されたレポートにはアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="55403-132">However, until the reset is completed, users won't be able to access any reports that were created by using Financial Reporter.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
