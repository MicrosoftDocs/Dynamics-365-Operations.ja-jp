---
title: 採用による候補者の雇用
description: この手順によって、リクルーターは、特定の採用プロジェクトで雇用申請を提出した申請者を雇用できます。
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMApplication, HcmWorkerNewWorker, HcmPositionLookup, HcmWorker, HcmPosition, HcmPositionDateManager,  DefaultDashboard
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f56769abb4da0068d6e2916df8dc782e662a2d56
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/19/2019
ms.locfileid: "858908"
---
# <a name="hiring-candidate-through-recruiting"></a><span data-ttu-id="c0c36-103">採用による候補者の雇用</span><span class="sxs-lookup"><span data-stu-id="c0c36-103">Hiring candidate through recruiting</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c0c36-104">この手順によって、リクルーターは、特定の採用プロジェクトで雇用申請を提出した申請者を雇用できます。</span><span class="sxs-lookup"><span data-stu-id="c0c36-104">This procedure enables a recruiter to hire an applicant who submitted an application through a specific recruitment project.</span></span> <span data-ttu-id="c0c36-105">採用プロジェクトを通して申請者を雇用する場合、新しい作業者レコードが作成され、申請者レコードのステータスは採用済となります。</span><span class="sxs-lookup"><span data-stu-id="c0c36-105">When you hire an applicant through a recruiting project, a new worker record will be created and the applicant’s record will have a status of Employed.</span></span> <span data-ttu-id="c0c36-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="c0c36-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="c0c36-107">この手順を完了するには、[人事管理] > [採用] > [申請] > [申請] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c0c36-107">To complete this procedure, navigate to Human resources > Recruitment > Applications >Applications</span></span> 

1. <span data-ttu-id="c0c36-108">外部申請者の申請の設定</span><span class="sxs-lookup"><span data-stu-id="c0c36-108">Select an Application for an External applicant</span></span>
2. <span data-ttu-id="c0c36-109">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c0c36-109">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="c0c36-110">[申請ステータス] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c0c36-110">Click Application status.</span></span>
4. <span data-ttu-id="c0c36-111">[新しい作業者の採用] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c0c36-111">Click Hire new worker.</span></span>
5. <span data-ttu-id="c0c36-112">[雇用の開始日] フィールドで、日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="c0c36-112">In the Employment start date field, enter a date and time.</span></span>
6. <span data-ttu-id="c0c36-113">[配置] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="c0c36-113">In the Position field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="c0c36-114">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c0c36-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="c0c36-115">[割り当て開始] フィールドに、日付と時刻を入力します。</span><span class="sxs-lookup"><span data-stu-id="c0c36-115">In the Assignment start field, enter a date and time.</span></span>
9. <span data-ttu-id="c0c36-116">[新しい作業者の採用] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c0c36-116">Click Hire new worker.</span></span>
10. <span data-ttu-id="c0c36-117">[職歴] 情報ボックスを展開します。</span><span class="sxs-lookup"><span data-stu-id="c0c36-117">Expand the Employment history FactBox.</span></span>
11. <span data-ttu-id="c0c36-118">[現在の職位] 情報ボックスを展開します。</span><span class="sxs-lookup"><span data-stu-id="c0c36-118">Expand the Current positions FactBox.</span></span>
12. <span data-ttu-id="c0c36-119">[職歴] 情報ボックスを展開します。</span><span class="sxs-lookup"><span data-stu-id="c0c36-119">Expand the Employment history FactBox.</span></span>
13. <span data-ttu-id="c0c36-120">[現在の職位] 情報ボックスを展開します。</span><span class="sxs-lookup"><span data-stu-id="c0c36-120">Expand the Current positions FactBox.</span></span>
14. <span data-ttu-id="c0c36-121">[住所] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="c0c36-121">Expand or collapse the Addresses section.</span></span>
15. <span data-ttu-id="c0c36-122">[連絡先情報] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="c0c36-122">Expand or collapse the Contact information section.</span></span>
16. <span data-ttu-id="c0c36-123">[個人情報] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="c0c36-123">Expand or collapse the Personal information section.</span></span>

