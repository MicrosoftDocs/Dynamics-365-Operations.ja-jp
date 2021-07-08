---
title: 計画製造オーダーは、確定する前にスケジュールする必要があります
description: 計画オーダーを確定しようとする場合、オーダーは確定する前にスケジュールする必要があるというエラー メッセージが表示されます。
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
ms.openlocfilehash: a360cb3cbd26e1bc1ebb1baf1a6a4d8282c28c5c
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294123"
---
# <a name="planned-production-order-must-be-scheduled-before-it-can-be-firmed"></a><span data-ttu-id="79c46-103">計画製造オーダーは、確定する前にスケジュールする必要があります</span><span class="sxs-lookup"><span data-stu-id="79c46-103">Planned production order must be scheduled before it can be firmed</span></span>

<span data-ttu-id="79c46-104">エラーコード: SYS309802</span><span class="sxs-lookup"><span data-stu-id="79c46-104">Error code: SYS309802</span></span>

## <a name="symptoms"></a><span data-ttu-id="79c46-105">現象</span><span class="sxs-lookup"><span data-stu-id="79c46-105">Symptoms</span></span>

<span data-ttu-id="79c46-106">計画オーダーを確定しようとする際に、次のエラー メッセージが表示されます:</span><span class="sxs-lookup"><span data-stu-id="79c46-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="79c46-107">計画製造オーダーは、スケジュールが済んでからでないと、確定できません。</span><span class="sxs-lookup"><span data-stu-id="79c46-107">The planned production order must be scheduled before it can be firmed.</span></span>

## <a name="cause"></a><span data-ttu-id="79c46-108">原因</span><span class="sxs-lookup"><span data-stu-id="79c46-108">Cause</span></span>

<span data-ttu-id="79c46-109">スケジュールされた開始日と終了日を空白にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="79c46-109">The scheduled start and end dates can't be blank.</span></span>

## <a name="resolution"></a><span data-ttu-id="79c46-110">解決策</span><span class="sxs-lookup"><span data-stu-id="79c46-110">Resolution</span></span>

<span data-ttu-id="79c46-111">計画オーダーの開始日と終了日を指定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="79c46-111">To specify start and end dates for the planned order, follow these steps.</span></span>

1. <span data-ttu-id="79c46-112">**マスター プラン \> マスタープラン \> 計画オーダー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="79c46-112">Go to **Master planning \> Master planning \> Planned orders**.</span></span>
1. <span data-ttu-id="79c46-113">関連する計画オーダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="79c46-113">Open the relevant planned order.</span></span>
1. <span data-ttu-id="79c46-114">**一般** クイック タブの、**スケジュール済** セクションで、**開始日** および **終了日** フィールドに日付を指定します。</span><span class="sxs-lookup"><span data-stu-id="79c46-114">On the **General** FastTab, in the **Scheduled** section, specify dates in the **Start date** and **End date** fields.</span></span>
