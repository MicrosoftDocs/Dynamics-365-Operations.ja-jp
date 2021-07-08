---
title: マスター プランのパラメーターが存在しない
description: 計画オーダーを確定しようとすると、マスター プランのパラメーターが存在しないというエラー メッセージが表示されます。
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d4b64af2e30109b8560d40c4c532504611528bbe
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294121"
---
# <a name="parameters-for-the-master-plan-dont-exist"></a><span data-ttu-id="2404d-103">マスター プランのパラメーターが存在しない</span><span class="sxs-lookup"><span data-stu-id="2404d-103">Parameters for the master plan don't exist</span></span>

<span data-ttu-id="2404d-104">エラーコード: SYS25368</span><span class="sxs-lookup"><span data-stu-id="2404d-104">Error code: SYS25368</span></span>

## <a name="symptoms"></a><span data-ttu-id="2404d-105">現象</span><span class="sxs-lookup"><span data-stu-id="2404d-105">Symptoms</span></span>

<span data-ttu-id="2404d-106">計画オーダーを確定しようとする際に、次のエラー メッセージが表示されます:</span><span class="sxs-lookup"><span data-stu-id="2404d-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="2404d-107">マスター プラン %1 のパラメーターは存在しません。</span><span class="sxs-lookup"><span data-stu-id="2404d-107">Parameters for master plan %1 do not exist.</span></span>

## <a name="cause"></a><span data-ttu-id="2404d-108">原因</span><span class="sxs-lookup"><span data-stu-id="2404d-108">Cause</span></span>

<span data-ttu-id="2404d-109">コンフィギュレーションの問題により、システムは指定した計画の設定を見つけられません。</span><span class="sxs-lookup"><span data-stu-id="2404d-109">Because of configuration issues, the system can't find the settings for the specified plan.</span></span>

## <a name="resolution"></a><span data-ttu-id="2404d-110">解決策</span><span class="sxs-lookup"><span data-stu-id="2404d-110">Resolution</span></span>

- <span data-ttu-id="2404d-111">**マスター プラン \> 設定 \> 計画 \> マスター プラン** に移動し、指定した名前の計画が存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="2404d-111">Go to **Master planning \> Setup \> Plans \> Master plans**, and make sure that a plan that has the specified name exists.</span></span>
