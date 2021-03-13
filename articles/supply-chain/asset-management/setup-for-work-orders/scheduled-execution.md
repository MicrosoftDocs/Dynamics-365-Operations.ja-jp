---
title: 実行予定
description: このトピックでは、資産管理の実行予定について説明します。
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a6d1761202697f62421bbf288c7e22efe559a986
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022410"
---
# <a name="scheduled-execution"></a><span data-ttu-id="dd469-103">実行予定</span><span class="sxs-lookup"><span data-stu-id="dd469-103">Scheduled execution</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="dd469-104">ワーク オーダーのサービス レベルを使用して、実行予定を設定できます。</span><span class="sxs-lookup"><span data-stu-id="dd469-104">You can use work order service levels to set up scheduled execution.</span></span> <span data-ttu-id="dd469-105">(ワーク オーダーのサービス レベルの詳細については、[サービス レベルおよび説明](service-level-and-description.md)を参照してください。) 実行予定により、メンテナンス作業者の作業計画に柔軟性がもたらされます。これは、ワーク オーダーを完了する間隔について、より詳細な要件または詳細度の低い要件を設定できるためです。</span><span class="sxs-lookup"><span data-stu-id="dd469-105">(For more information about work order service levels, see [Service level and description](service-level-and-description.md).) Scheduled execution provides flexibility in work planning for maintenance workers, because you can set up more detailed or less detailed requirements for the interval that a work order should be completed during.</span></span> <span data-ttu-id="dd469-106">たとえば、生産施設で予定よりも早く作業を完了するメンテナンス作業者は、現在の週に計画されていますが、当日とは限らない別の近い作業に進むことができます。</span><span class="sxs-lookup"><span data-stu-id="dd469-106">For example, a maintenance worker who completes a job faster than expected in a production facility might be able to move on to another nearby job that was planned for the current week but not necessarily for the current day.</span></span> <span data-ttu-id="dd469-107">このアプローチでは、作業者の計画とジョブの完了を最適化できます。</span><span class="sxs-lookup"><span data-stu-id="dd469-107">This approach allows for optimization of worker planning and job completion.</span></span>

<span data-ttu-id="dd469-108">ワーク オーダーに関連する実行予定の設定は、汎用または固有にすることができます。</span><span class="sxs-lookup"><span data-stu-id="dd469-108">Scheduled execution setup, which is related to work orders, can be generic or specific.</span></span> <span data-ttu-id="dd469-109">特定のワーク オーダー タイプ、資産タイプなどに限定されない汎用の明細行を設定できます。</span><span class="sxs-lookup"><span data-stu-id="dd469-109">You can set up generic lines that aren't limited to specific work order types, asset types, and so on.</span></span> <span data-ttu-id="dd469-110">または、特定のワーク オーダー タイプ、資産タイプ、メンテナンス作業タイプに適用される実行予定の明細行を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="dd469-110">Alternatively, you can create scheduled execution lines that apply to a specific work order type, asset type, maintenance job type, and so on.</span></span>

1. <span data-ttu-id="dd469-111">**資産管理** \> **設定** \> **ワーク オーダー** \> **実行予定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dd469-111">Select **Asset management** \> **Setup** \> **Work orders** \> **Scheduled execution**.</span></span>
2. <span data-ttu-id="dd469-112">**新規** を選択して、実行予定明細行を作成します。</span><span class="sxs-lookup"><span data-stu-id="dd469-112">Select **New** to create a scheduled execution line.</span></span>
3. <span data-ttu-id="dd469-113">**機能的な場所**、**ワーク オーダー タイプ**、**資産タイプ**、**メーカー**、**モデル**、**メンテナンス作業タイプ カテゴリ**、**メンテナンス作業タイプ**、**メンテナンス作業タイプ バリアント**、および **取引** のフィールドで、必要に応じて値を選択します。</span><span class="sxs-lookup"><span data-stu-id="dd469-113">In the **Functional location**, **Work order type**, **Asset type**, **Manufacturer**, **Model**, **Maintenance job type category**, **Maintenance job type**, **Maintenance job type variant**, and **Trade** fields, select values as you require.</span></span>
4. <span data-ttu-id="dd469-114">**サービス レベル** フィールドで、ワーク オーダーのサービス レベルを選択します。</span><span class="sxs-lookup"><span data-stu-id="dd469-114">In the **Service level** field, select a work order service level.</span></span> <span data-ttu-id="dd469-115">このフィールドを空白のままにした場合は、最も一般的なタイプの実行予定明細行を作成します。</span><span class="sxs-lookup"><span data-stu-id="dd469-115">If you leave this field blank, you make the most generic type of scheduled execution line.</span></span> <span data-ttu-id="dd469-116">一般的な明細行の例については、次の図の最初のレコードを参照してください。</span><span class="sxs-lookup"><span data-stu-id="dd469-116">For an example of a generic line, see the first record in the illustration that follows.</span></span> <span data-ttu-id="dd469-117">この明細行によって、ワーク オーダーのサービス レベルのないすべてのワーク オーダーを、特定の日時に対してスケジュールできるようになります。</span><span class="sxs-lookup"><span data-stu-id="dd469-117">That line enables all work orders that have no work order service level to be scheduled for a specific date and time.</span></span>
5. <span data-ttu-id="dd469-118">**実行予定** フィールドで、時間間隔を選択します。</span><span class="sxs-lookup"><span data-stu-id="dd469-118">In the **Scheduled execution** field, select the time interval.</span></span>
6. <span data-ttu-id="dd469-119">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dd469-119">Select **Save**.</span></span>

![実行予定](media/20-setup-for-work-orders.png)
