---
title: ピッキング リスト登録時に場所が選択された場合にエラーが発生します
description: ピッキング リスト登録時に場所が選択された場合にエラーが発生します。
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b7fc579821f9a80d94aea949fcc0301b9d8f6935
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026661"
---
# <a name="an-error-occurs-when-the-location-is-selected-during-picking-list-registration"></a><span data-ttu-id="7b9c6-103">ピッキング リスト登録時に場所が選択された場合にエラーが発生します</span><span class="sxs-lookup"><span data-stu-id="7b9c6-103">An error occurs when the location is selected during picking list registration</span></span>

<span data-ttu-id="7b9c6-104">KB 番号: 4613106</span><span class="sxs-lookup"><span data-stu-id="7b9c6-104">KB number: 4613106</span></span>

## <a name="symptoms"></a><span data-ttu-id="7b9c6-105">現象</span><span class="sxs-lookup"><span data-stu-id="7b9c6-105">Symptoms</span></span>

<span data-ttu-id="7b9c6-106">この問題は、販売注文の自動予約を自動的に行うシステムが構成されている場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="7b9c6-106">This issue occurs when your system is configured to automatically reserve sales orders.</span></span> <span data-ttu-id="7b9c6-107">ピッキング リスト登録行の場所を選択しようとする場合、倉庫管理 (WMS) の予約プロセスを使用するときに次のエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7b9c6-107">If you try to select the location for a picking list registration line, you receive the following error message when you use warehouse management (WMS) reservation processes:</span></span>

> <span data-ttu-id="7b9c6-108">数量を新しい分析コードで更新できない</span><span class="sxs-lookup"><span data-stu-id="7b9c6-108">Can't update quantity with new dimensions</span></span>

<span data-ttu-id="7b9c6-109">この問題は、指定した場所に十分な在庫がないので発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7b9c6-109">This issue can occur because you don't have enough on-hand inventory at a specified location.</span></span>

## <a name="resolution"></a><span data-ttu-id="7b9c6-110">解像度</span><span class="sxs-lookup"><span data-stu-id="7b9c6-110">Resolution</span></span>

<span data-ttu-id="7b9c6-111">システムはデザイン通り動作しています。</span><span class="sxs-lookup"><span data-stu-id="7b9c6-111">The system is behaving as designed.</span></span>

<span data-ttu-id="7b9c6-112">倉庫レベルの引当プロセスを使用する場合、すべての在庫分析コード レベルで在庫在庫の引当が行われなかったり、指定した場所に十分な在庫が存在しない場合は、ピッキング ラインからの手動引当プロセスを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7b9c6-112">In scenarios where you use the warehouse-level reservation process, if the on-hand inventory won't be reserved on all inventory dimension levels, and you don't have enough on-hand inventory at a specified location, we recommend that you use the manual reservation process from the picking line.</span></span> <span data-ttu-id="7b9c6-113">その後、*ロットの引当* 機能を使用して、利用可能なすべての在庫数量に、在庫場所などの低い引当 を配分できます。</span><span class="sxs-lookup"><span data-stu-id="7b9c6-113">You can then use the *Reserve lot* function to distribute the lower reservations, such as location, for all the available on-hand quantities.</span></span>
