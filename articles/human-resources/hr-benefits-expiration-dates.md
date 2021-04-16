---
title: 給付金の有効期限の管理
description: この手順では、給付金付を期限切れにするまたは延長する方法、および福利厚生に登録されている作業者の登録日を管理する方法について説明します。
author: andreabichsel
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefit, HcmMassBenefitExpiration, HcmMassBenefitExpirationResults, HcmWorker, HcmWorkerEnrollment, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 2eeb9ccc5bb386d036f44ab6bb8f0999e05439b7
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803756"
---
# <a name="manage-benefit-expiration-dates"></a><span data-ttu-id="e9569-103">給付金の有効期限の管理</span><span class="sxs-lookup"><span data-stu-id="e9569-103">Manage benefit expiration dates</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e9569-104">この手順では、給付金付を期限切れにするまたは延長する方法、および福利厚生に登録されている作業者の登録日を管理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e9569-104">This procedure shows how you can expire or extend a benefit, and manage the enrollment dates of workers that are enrolled in the benefit.</span></span> <span data-ttu-id="e9569-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="e9569-105">The demo data company used to create this procedure is USMF.</span></span>

## <a name="benefit-expiration-dates"></a><span data-ttu-id="e9569-106">給付金の有効期限</span><span class="sxs-lookup"><span data-stu-id="e9569-106">Benefit expiration dates</span></span>

1. <span data-ttu-id="e9569-107">[人事管理] > [福利厚生] > [福利厚生] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e9569-107">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="e9569-108">[登録された作業者] 情報ボックスを展開します。</span><span class="sxs-lookup"><span data-stu-id="e9569-108">Expand the Enrolled workers FactBox.</span></span>
3. <span data-ttu-id="e9569-109">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="e9569-109">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="e9569-110">[アクション] ウィンドウで、[福利厚生] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e9569-110">On the Action Pane, click Benefit.</span></span>
5. <span data-ttu-id="e9569-111">[給付金の期限切れと延長] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e9569-111">Click Expire or extend benefits.</span></span>
6. <span data-ttu-id="e9569-112">[新しい給付金の有効期限] フィールドに日付と時刻を入力します。</span><span class="sxs-lookup"><span data-stu-id="e9569-112">In the New benefit expiration date field, enter a date and time.</span></span>
7. <span data-ttu-id="e9569-113">[期限切れ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e9569-113">Click Expire.</span></span>
8. <span data-ttu-id="e9569-114">[アクション] ウィンドウで、[福利厚生] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e9569-114">On the Action Pane, click Benefit.</span></span>
9. <span data-ttu-id="e9569-115">[給付金の期限切れと延長の結果] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e9569-115">Click Benefit expiration and extension results.</span></span>
10. <span data-ttu-id="e9569-116">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="e9569-116">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="e9569-117">一覧で、[対象の作業者リンク] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e9569-117">In the list, click the Workers affected link.</span></span>
12. <span data-ttu-id="e9569-118">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="e9569-118">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="e9569-119">クリックして、[個人番号] フィールドのリンク先を表示します。</span><span class="sxs-lookup"><span data-stu-id="e9569-119">Click to follow the link in the Personnel number field.</span></span>
14. <span data-ttu-id="e9569-120">[個人情報] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="e9569-120">Expand the Personal information section.</span></span>
15. <span data-ttu-id="e9569-121">[福利厚生] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e9569-121">Click Benefits.</span></span>
16. <span data-ttu-id="e9569-122">一覧で、福利厚生を検索し、レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="e9569-122">In the list, find the benefit and select the record.</span></span> <span data-ttu-id="e9569-123">新しい適用終了日に注意します。</span><span class="sxs-lookup"><span data-stu-id="e9569-123">Note the new coverage end date.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]