---
title: 重量には正の値を指定してください
description: 重量には正の値を指定してください
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSContainerCloseDiag_canClose
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dcbcde3143cb509b68b277cb7c709263e2659b5b
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924306"
---
# <a name="weight-must-be-positive"></a><span data-ttu-id="ed49e-103">重量には正の値を指定してください</span><span class="sxs-lookup"><span data-stu-id="ed49e-103">Weight must be positive</span></span>

<span data-ttu-id="ed49e-104">エラー コード: WeightMustBePositive</span><span class="sxs-lookup"><span data-stu-id="ed49e-104">Error code: WeightMustBePositive</span></span>

## <a name="symptoms"></a><span data-ttu-id="ed49e-105">現象</span><span class="sxs-lookup"><span data-stu-id="ed49e-105">Symptoms</span></span>

<span data-ttu-id="ed49e-106">システムは次のエラー メッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="ed49e-106">The system shows the following error message:</span></span>

> <span data-ttu-id="ed49e-107">重量には正の値を指定してください。</span><span class="sxs-lookup"><span data-stu-id="ed49e-107">Weight must be positive.</span></span>

## <a name="cause"></a><span data-ttu-id="ed49e-108">原因</span><span class="sxs-lookup"><span data-stu-id="ed49e-108">Cause</span></span>

<span data-ttu-id="ed49e-109">**総重量** フィールドは *0* (ゼロ) または負の値に設定されています。</span><span class="sxs-lookup"><span data-stu-id="ed49e-109">The **Gross Weight** field is set to *0* (zero) or a negative value.</span></span>

## <a name="resolution"></a><span data-ttu-id="ed49e-110">解像度</span><span class="sxs-lookup"><span data-stu-id="ed49e-110">Resolution</span></span>

<span data-ttu-id="ed49e-111">重量を指定するには、次の手順のいずれかに従います。</span><span class="sxs-lookup"><span data-stu-id="ed49e-111">To specify a weight, follow one of these steps.</span></span>

- <span data-ttu-id="ed49e-112">**総重量** フィールドで、値を設定します。</span><span class="sxs-lookup"><span data-stu-id="ed49e-112">In the **Gross weight** field, set a value.</span></span> <span data-ttu-id="ed49e-113">その後、ドロップダウン リストで単位を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed49e-113">Then select a unit in the drop-down list.</span></span>
- <span data-ttu-id="ed49e-114">**システム重量を取得** を選択して、**総重量** 値を計算します。</span><span class="sxs-lookup"><span data-stu-id="ed49e-114">Select **Get system weight** to calculate the **Gross weight** value.</span></span>
