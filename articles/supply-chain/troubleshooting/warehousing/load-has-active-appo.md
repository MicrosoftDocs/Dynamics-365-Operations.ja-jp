---
title: カレンダーに問題がある場合は、出荷を確認できない
description: カレンダーに問題がある場合は、出荷を確認できない
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f1fccd10d8867252f32b37c77f9a3bad54157bdd
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938506"
---
# <a name="you-cant-confirm-a-shipment-because-of-an-issue-with-the-calendar"></a><span data-ttu-id="25281-103">カレンダーに問題がある場合は、出荷を確認できない</span><span class="sxs-lookup"><span data-stu-id="25281-103">You can't confirm a shipment because of an issue with the calendar</span></span>

<span data-ttu-id="25281-104">エラーコード: TRX2716</span><span class="sxs-lookup"><span data-stu-id="25281-104">Error code: TRX2716</span></span>

## <a name="symptoms"></a><span data-ttu-id="25281-105">現象</span><span class="sxs-lookup"><span data-stu-id="25281-105">Symptoms</span></span>

<span data-ttu-id="25281-106">出荷を確認しようとすると、次のエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="25281-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="25281-107">カレンダー タイプ %1 では、予定 %2 をチェックイン/チェックアウトする必要があります。</span><span class="sxs-lookup"><span data-stu-id="25281-107">The calendar type %1 requires the appointment %2 to be checked in and out.</span></span>

<span data-ttu-id="25281-108">したがって、積荷の出荷を確認できません。</span><span class="sxs-lookup"><span data-stu-id="25281-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="25281-109">原因</span><span class="sxs-lookup"><span data-stu-id="25281-109">Cause</span></span>

<span data-ttu-id="25281-110">積荷の有効な予定が存在します。</span><span class="sxs-lookup"><span data-stu-id="25281-110">Active appointments for the load exist.</span></span> <span data-ttu-id="25281-111">たとえば、ドライバーのチェックインを必要とするルールがあります。</span><span class="sxs-lookup"><span data-stu-id="25281-111">For example, there is a rule that requires driver check-in.</span></span> <span data-ttu-id="25281-112">そのため、積荷の状態は、現在出荷確認に失敗しています。</span><span class="sxs-lookup"><span data-stu-id="25281-112">Therefore, the load is currently in a state where shipment confirmation fails.</span></span>

## <a name="resolution"></a><span data-ttu-id="25281-113">解像度</span><span class="sxs-lookup"><span data-stu-id="25281-113">Resolution</span></span>

<span data-ttu-id="25281-114">積荷にリンクされている有効な予定に関する問題を調査および修正する必要があります。</span><span class="sxs-lookup"><span data-stu-id="25281-114">You must investigate and fix any issues with the active appointments that are linked to the load.</span></span>

1. <span data-ttu-id="25281-115">**倉庫管理 \> 積荷 \> すべての積荷** に移動します。</span><span class="sxs-lookup"><span data-stu-id="25281-115">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="25281-116">発送が確認できない積荷を選択します。</span><span class="sxs-lookup"><span data-stu-id="25281-116">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="25281-117">アクション ペインで、**輸送** タブの **予定** グループで、**予定のスケジューリング** を選択します。</span><span class="sxs-lookup"><span data-stu-id="25281-117">On the Action Pane, on the **Transportation** tab, in the **Appointments** group, select **Appointment scheduling**.</span></span>
1. <span data-ttu-id="25281-118">次の手順のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="25281-118">Follow one of these steps:</span></span>

    - <span data-ttu-id="25281-119">予定に対してドライバーのチェックイン/チェックアウトが完了済であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="25281-119">Make sure that driver check-in/check-out is completed for the appointment.</span></span>
    - <span data-ttu-id="25281-120">予定を完了またはキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="25281-120">Complete or cancel the appointment.</span></span>
    - <span data-ttu-id="25281-121">関連する予定ルールで **ドライバーのチェックイン必須** オプションを無効にします。</span><span class="sxs-lookup"><span data-stu-id="25281-121">Disable the **Driver check-in required** option for the related appointment rule.</span></span>
