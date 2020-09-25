---
title: リソース キャパシティの同期
description: このトピックでは、カレンダーとプロジェクトの間でリソースの能力を同期化する方法について説明します。
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27b6fde91a72e37bb2712daba765032322cbd4e9
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760592"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="56430-103">リソース キャパシティの同期</span><span class="sxs-lookup"><span data-stu-id="56430-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="56430-104">リソース同期のプロセスは、カレンダーの情報および基準カレンダーがプロジェクトのリソース スケジューリングにトリクルダウンするのを保証するために役立ちます。</span><span class="sxs-lookup"><span data-stu-id="56430-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="56430-105">カレンダーが変更される場合、プロセスはプロジェクト リソースのスケジューリングに必要な更新を行います。</span><span class="sxs-lookup"><span data-stu-id="56430-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="56430-106">カレンダーのリソースの情報が事前に同期化されているため、プロセスもパフォーマンスを向上させるのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="56430-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="56430-107">したがって、リソースのスケジューリング情報の更新がより迅速に行われます。</span><span class="sxs-lookup"><span data-stu-id="56430-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="56430-108">一つずつ作成する代わりに、バッチとしてプロセスをスケジューリングすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="56430-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="56430-109">それ以外の場合は、情報が最後に同期された包含日付を忘れるリスクがあります。</span><span class="sxs-lookup"><span data-stu-id="56430-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="56430-110">包含日付を使用しない場合、日付の同期時にギャップが発生します。</span><span class="sxs-lookup"><span data-stu-id="56430-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![カレンダーの同期](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="56430-112">リソース能力のロールアップを同期</span><span class="sxs-lookup"><span data-stu-id="56430-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="56430-113">同期プロセスは、すべてのリソース カレンダー情報と同期するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="56430-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="56430-114">この情報には、プロジェクトのリソース カレンダー能力テーブルの変更についての基準カレンダーの情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="56430-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="56430-115">新しいリソースがプロジェクトに追加されると、同期により、更新されたカレンダー情報が使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="56430-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="56430-116">この同期はいつでも実行できます。</span><span class="sxs-lookup"><span data-stu-id="56430-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="56430-117">バッチを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="56430-117">We recommend that you use a batch.</span></span> <span data-ttu-id="56430-118">確保済能力の同期中に、このオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="56430-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="56430-119">**プロジェクト管理および会計** &gt; **定期処理** &gt; **能力の同期** &gt; **リソース能力のロールアップを同期**の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="56430-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="56430-120">次の表でオプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="56430-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="56430-121">オプション</span><span class="sxs-lookup"><span data-stu-id="56430-121">Option</span></span>      | <span data-ttu-id="56430-122">説明</span><span class="sxs-lookup"><span data-stu-id="56430-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="56430-123">期間コード</span><span class="sxs-lookup"><span data-stu-id="56430-123">Period code</span></span> | <span data-ttu-id="56430-124">必要に応じて、リソース能力のロールアップの同期プロセス用に開始日と終了日を設定する、一般会計の日付間隔コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="56430-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="56430-125">入社日</span><span class="sxs-lookup"><span data-stu-id="56430-125">Start date</span></span>  | <span data-ttu-id="56430-126">リソース能力のロールアップの同期プロセスの開始日を入力します。</span><span class="sxs-lookup"><span data-stu-id="56430-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="56430-127">終了日</span><span class="sxs-lookup"><span data-stu-id="56430-127">End date</span></span>    | <span data-ttu-id="56430-128">リソース能力のロールアップの同期プロセスの終了日を入力します。</span><span class="sxs-lookup"><span data-stu-id="56430-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="56430-129">[![同期プロセス](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="56430-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>
