---
title: メンテナンス スケジュール コスト
description: このトピックでは、資産管理におけるメンテナンス スケジュール コストについて説明します。
author: johanhoffmann
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 405fd7fbbbb8862446d09b9ea33ef14348e691f9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813776"
---
# <a name="maintenance-schedule-cost"></a><span data-ttu-id="3b5ca-103">メンテナンス スケジュール コスト</span><span class="sxs-lookup"><span data-stu-id="3b5ca-103">Maintenance schedule cost</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="3b5ca-104">資産管理で、メンテナンス スケジュールの明細行に関する予算原価を計算することができます。</span><span class="sxs-lookup"><span data-stu-id="3b5ca-104">In Asset Management, you can calculate budget costs on maintenance schedule lines.</span></span> <span data-ttu-id="3b5ca-105">たとえば、来年の予定された予防的メンテナンス ジョブに関連する原価など、予定原価の概要を知りたい場合に役立ちます</span><span class="sxs-lookup"><span data-stu-id="3b5ca-105">This is useful if you want to get an overview of expected costs, for example, costs relating to planned preventive maintenance jobs for the next year.</span></span> <span data-ttu-id="3b5ca-106">計算は、「メンテナンス計画」、「メンテナンス ラウンド」、および「メンテナンス要求」タイプの既存のメンテナンス スケジュールの明細行に基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="3b5ca-106">The calculations are based on existing maintenance schedule lines of type "Maintenance plans" and "Maintenance rounds" and "Maintenance requests".</span></span>

1. <span data-ttu-id="3b5ca-107">**資産管理** > **照会** > **資産** > **メンテナンス スケジュール コスト** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b5ca-107">Click **Asset management** > **Inquiries** > **Assets** > **Maintenance schedule cost**.</span></span>

2. <span data-ttu-id="3b5ca-108">財務分析コードにグループ化された原価を表示したい場合は、**メンテナンス スケジュール コスト** ダイアログで、**財務分析コード セット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b5ca-108">In the **Maintenance schedule cost** dialog, you can select a **Financial dimension set** if you want to see costs grouped in financial dimensions.</span></span>

>[!NOTE]
><span data-ttu-id="3b5ca-109">財務分析コード セットは、**一般会計** > **勘定科目表** > **分析コード** > **財務分析コード セット** で設定することができます。</span><span class="sxs-lookup"><span data-stu-id="3b5ca-109">Financial dimension sets are set up in **General ledger** > **Chart of accounts** > **Dimensions** > **Financial dimension sets**.</span></span>

3. <span data-ttu-id="3b5ca-110">**レベル** フィールドを使用すると、機能的な場所に関するメンテナンス スケジュール明細行の詳細度を指定できます。</span><span class="sxs-lookup"><span data-stu-id="3b5ca-110">You can use the **Level** field to indicate how detailed you want the maintenance schedule lines to be regarding functional locations.</span></span> <span data-ttu-id="3b5ca-111">たとえば、フィールドに「1」の番号を挿入し、複数レベルの機能的な場所構造がある場合、機能的な場所に対するすべてのメンテナンス スケジュール明細行が最上位レベルに表示されます。したがって明細行の時間は、下位レベルにある機能的な場所から追加される場合があります。</span><span class="sxs-lookup"><span data-stu-id="3b5ca-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="3b5ca-112">**レベル** フィールドに数値 "0" を挿入すると、関連するすべての機能的な場所レベルですべてメンテナンス スケジュール明細行を示す、詳細な結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3b5ca-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="3b5ca-113">特定の資産に対して計算を実行する場合は、**対象に含めるレコード** クイック タブの **フィルター** をクリックし、該当する資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b5ca-113">If you want to make a calculation for specific assets, click **Filter** on the **Records to include** FastTab, and select the relevant assets.</span></span> <span data-ttu-id="3b5ca-114">必要に応じて、原価計算の **開始予定** 日を指定したり、原価計算の異なる **ステータス** を選択したりすることもできます。</span><span class="sxs-lookup"><span data-stu-id="3b5ca-114">If required, you can also specify an **Expected start** date for the cost calculation or select a different **Status** for the cost calculation</span></span>

5. <span data-ttu-id="3b5ca-115">**OK** をクリックして、原価計算を開始します。</span><span class="sxs-lookup"><span data-stu-id="3b5ca-115">Click **OK** to start the cost calculation.</span></span>

6. <span data-ttu-id="3b5ca-116">**グループ化** アクション ウィンドウ グループの **メンテナンス スケジュール コスト** タブで該当するボタンをクリックし、原価計算に必要な詳細レベルを表示します。</span><span class="sxs-lookup"><span data-stu-id="3b5ca-116">On the **Maintenance schedule cost** tab > in the **Group by...** Action Pane groups, click the relevant buttons to show the required detail level of the cost calculation.</span></span> <span data-ttu-id="3b5ca-117">選択したアクション ウィンドウ グループが強調表示されます。</span><span class="sxs-lookup"><span data-stu-id="3b5ca-117">The selected Action Pane group buttons are highlighted.</span></span> <span data-ttu-id="3b5ca-118">ボタンをクリックして、有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="3b5ca-118">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="3b5ca-119">新しい原価計算を実行する場合、**原価計算** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b5ca-119">Click the **Calculate cost** button if you want to make a new cost calculation.</span></span>

<span data-ttu-id="3b5ca-120">次の図では、メンテナンス スケジュールの原価計算の結果を表示します。</span><span class="sxs-lookup"><span data-stu-id="3b5ca-120">The illustration below shows the results of a maintenance schedule cost calculation.</span></span>

![図 1](media/17-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]