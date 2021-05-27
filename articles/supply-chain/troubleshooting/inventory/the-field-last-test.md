---
title: 複数の品質指示が作成された場合に [最終テスト日] フィールドが更新されない
description: 複数の品質指示が作成された場合に [最終テスト日] フィールドが更新されていません。
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f796bdaa88d32b1c58dd8a4bca19f0ce4f3943d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026688"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a><span data-ttu-id="65d95-103">複数の品質指示が作成された場合に [最終テスト日] フィールドが更新されない</span><span class="sxs-lookup"><span data-stu-id="65d95-103">The Last tested date field isn't updated when multiple quality orders are created</span></span>

<span data-ttu-id="65d95-104">KB 番号: 4612803</span><span class="sxs-lookup"><span data-stu-id="65d95-104">KB number: 4612803</span></span>

## <a name="symptoms"></a><span data-ttu-id="65d95-105">現象</span><span class="sxs-lookup"><span data-stu-id="65d95-105">Symptoms</span></span>

<span data-ttu-id="65d95-106">複数の品質指示が作成された場合に **最終テスト日** フィールドが更新されていません。</span><span class="sxs-lookup"><span data-stu-id="65d95-106">The **Last tested date** field isn't updated when multiple quality orders are created.</span></span>

## <a name="resolution"></a><span data-ttu-id="65d95-107">解像度</span><span class="sxs-lookup"><span data-stu-id="65d95-107">Resolution</span></span>

<span data-ttu-id="65d95-108">システムはデザイン通り動作しています。</span><span class="sxs-lookup"><span data-stu-id="65d95-108">The system is behaving as designed.</span></span> <span data-ttu-id="65d95-109">最終テスト日は、品質指示に関連していません。</span><span class="sxs-lookup"><span data-stu-id="65d95-109">The last tested date isn't related to quality orders.</span></span> <span data-ttu-id="65d95-110">完成品が最初に購入または製造された日付が保存されます。</span><span class="sxs-lookup"><span data-stu-id="65d95-110">It stores the date when the finished goods were first purchased or manufactured.</span></span> <span data-ttu-id="65d95-111">この日付は、有効期限通知日の計算に使用されます。</span><span class="sxs-lookup"><span data-stu-id="65d95-111">This date is used to calculate the shelf life advice date.</span></span>
