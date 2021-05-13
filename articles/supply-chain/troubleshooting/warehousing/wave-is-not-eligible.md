---
title: ウェーブがクリーンアップの使用に適さない
description: ウェーブがクリーンアップの使用に適さない
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWaveTable_WHSWaveProcessingDataCleanup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3e5142cf40a6c0d308e8e952bbe17e85b498826d
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924330"
---
# <a name="wave-isnt-eligible-for-cleanup"></a><span data-ttu-id="fbd4a-103">ウェーブがクリーンアップの使用に適さない</span><span class="sxs-lookup"><span data-stu-id="fbd4a-103">Wave isn't eligible for cleanup</span></span>

<span data-ttu-id="fbd4a-104">エラー コード: WaveNotEligibleForCleanup</span><span class="sxs-lookup"><span data-stu-id="fbd4a-104">Error code: WaveNotEligibleForCleanup</span></span>

## <a name="symptoms"></a><span data-ttu-id="fbd4a-105">現象</span><span class="sxs-lookup"><span data-stu-id="fbd4a-105">Symptoms</span></span>

<span data-ttu-id="fbd4a-106">システムは次のエラー メッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="fbd4a-106">The system shows the following error message:</span></span>

> <span data-ttu-id="fbd4a-107">ウェーブ %1 はクリーンアップに適しません。</span><span class="sxs-lookup"><span data-stu-id="fbd4a-107">Wave %1 is not eligible for cleanup.</span></span>

<span data-ttu-id="fbd4a-108">ウェーブ データは、クリーンアップできません。</span><span class="sxs-lookup"><span data-stu-id="fbd4a-108">The wave data can't be cleaned up.</span></span>  

## <a name="cause"></a><span data-ttu-id="fbd4a-109">原因</span><span class="sxs-lookup"><span data-stu-id="fbd4a-109">Cause</span></span>

<span data-ttu-id="fbd4a-110">次のいずれかの条件で示されているように、ウェーブは、現在処理されています。</span><span class="sxs-lookup"><span data-stu-id="fbd4a-110">The wave is currently being processed, as indicated by one of the following conditions:</span></span>

- <span data-ttu-id="fbd4a-111">**ウェーブの状態** フィールドは *実行中* に設定されます。</span><span class="sxs-lookup"><span data-stu-id="fbd4a-111">The **Wave status** field is set to *Executing*.</span></span>
- <span data-ttu-id="fbd4a-112">アクション ウィンドウの **ウェーブ** タブにある **ウェーブ** グループで **バッチ ジョブ** を選択すると、**状態** フィールドが *終了済*、*エラー*、または *キャンセル済* に設定されません。</span><span class="sxs-lookup"><span data-stu-id="fbd4a-112">When you select **Batch job** in the **Wave** group on the **Wave** tab of the Action Pane, the **Status** field isn't set to *Ended*, *Error*, or *Canceled*.</span></span> <span data-ttu-id="fbd4a-113">したがって、バッチ ジョブは現在実行中です。</span><span class="sxs-lookup"><span data-stu-id="fbd4a-113">Therefore, a batch job is currently running.</span></span>

## <a name="resolution"></a><span data-ttu-id="fbd4a-114">解像度</span><span class="sxs-lookup"><span data-stu-id="fbd4a-114">Resolution</span></span>

<span data-ttu-id="fbd4a-115">アクション ウィンドウの **ウェーブ** タブの **ウェーブ** グループで、**バッチ ジョブ** を選択し、次のいずれかの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="fbd4a-115">On the Action Pane, on the **Wave** tab, in the **Wave** group, select **Batch job**, and then follow one of these steps:</span></span>

- <span data-ttu-id="fbd4a-116">**状態** フィールドが *実行中* に設定されている場合: アクション ウィンドウの **バッチ ジョブ** タブにある **バッチ ジョブ** グループで、**タスクの表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fbd4a-116">If the **Status** field is set to *Executing*: On the Action Pane, on the **Batch job** tab, in the **Batch job** group, select **View tasks**.</span></span> <span data-ttu-id="fbd4a-117">**バッチ タスク** ページを更新すると、進捗状況を追跡することができます。</span><span class="sxs-lookup"><span data-stu-id="fbd4a-117">You can follow the progress by refreshing the **Batch tasks** page.</span></span>
- <span data-ttu-id="fbd4a-118">**状態** フィールドが *実行中* に設定されていない場合: アクション ウィンドウの **バッチ ジョブ** タブにある **機能** グループで、**状態の変更** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fbd4a-118">If the **Status** field isn't set to *Executing*: On the Action Pane, on the **Batch job** tab, in the **Functions** group, select **Change status**.</span></span> <span data-ttu-id="fbd4a-119">**新しい状態の選択** フィールドで、*待機中* を選択します。</span><span class="sxs-lookup"><span data-stu-id="fbd4a-119">In the **Select new status** field, select *Waiting*.</span></span> <span data-ttu-id="fbd4a-120">その後、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fbd4a-120">Then select **OK**.</span></span>
