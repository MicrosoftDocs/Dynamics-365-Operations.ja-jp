---
title: 採用による既存の従業員の雇用
description: 場合によっては、空いている職位が既に組織の従業員である候補者によって一杯になることがあります。
author: andreabichsel
manager: AnnBe
ms.date: 02/10/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa020f17a6f893fc1360bfdec80b478e6f5dd686
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178758"
---
# <a name="hire-existing-employees-through-recruitment"></a><span data-ttu-id="3add1-103">採用による既存の従業員の雇用</span><span class="sxs-lookup"><span data-stu-id="3add1-103">Hire existing employees through recruitment</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3add1-104">場合によっては、空いている職位が既に組織の従業員である候補者によって一杯になることがあります。</span><span class="sxs-lookup"><span data-stu-id="3add1-104">Sometimes open positions can be filled by candidates who are already employees in your organization.</span></span> <span data-ttu-id="3add1-105">この手順は、採用プロセスを使用して既存の従業員を採用する手順を説明しています。</span><span class="sxs-lookup"><span data-stu-id="3add1-105">This procedure walks through the steps of hiring an existing employee through the recruiting process.</span></span> <span data-ttu-id="3add1-106">この手順では、採用プロジェクトは既に設定され、既存の従業員は既に採用プロジェクトの申請を送信しています。</span><span class="sxs-lookup"><span data-stu-id="3add1-106">In this procedure, a recruitment project has already been set up, and an existing employee has already submitted an application for the recruitment project.</span></span> <span data-ttu-id="3add1-107">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="3add1-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="3add1-108">[人事管理] > [採用] > [応募] > [応募] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3add1-108">Go to Human resources > Recruitment > Applications > Applications.</span></span>
2. <span data-ttu-id="3add1-109">リストで、雇用する従業員の申請を検索します。</span><span class="sxs-lookup"><span data-stu-id="3add1-109">In the list, find application for the employee that you would like to hire.</span></span> <span data-ttu-id="3add1-110">例: 00002 John Emory</span><span class="sxs-lookup"><span data-stu-id="3add1-110">Example:  00002  John Emory</span></span>
3. <span data-ttu-id="3add1-111">[申請ステータス] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3add1-111">Click Application status.</span></span>
    * <span data-ttu-id="3add1-112">申請状態は、申請が採用プロセスのどの段階にあるかを示します。</span><span class="sxs-lookup"><span data-stu-id="3add1-112">The application status indicates where an application is at in the recruitment process.</span></span>  <span data-ttu-id="3add1-113">これらの手順はオプションです。</span><span class="sxs-lookup"><span data-stu-id="3add1-113">Each of these steps is optional.</span></span> <span data-ttu-id="3add1-114">通常、申請は次の順でステータスを遷移します: 受領済、確認済、面接済。</span><span class="sxs-lookup"><span data-stu-id="3add1-114">Typically, an application would move the statuses in the following order:  received, confirmed, and interviewed.</span></span> <span data-ttu-id="3add1-115">面接プロセスのあと、雇用の判断が下されます。</span><span class="sxs-lookup"><span data-stu-id="3add1-115">After the interview process, a hiring decision would be made.</span></span>  
4. <span data-ttu-id="3add1-116">[職位の変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3add1-116">Click Change position.</span></span>
5. <span data-ttu-id="3add1-117">従業員を雇用する職位を選択します。</span><span class="sxs-lookup"><span data-stu-id="3add1-117">Select the position that you are hiring the employee into.</span></span>
6. <span data-ttu-id="3add1-118">[新しい割り当て開始日] フィールドで、従業員が新しい職位で仕事を開始する日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="3add1-118">In the New Assignment Start Date field, enter the date that the employee will begin working in the new position.</span></span>  
7. <span data-ttu-id="3add1-119">[割り当て終了日] フィールドで、従業員が現在の職位で仕事を停止する日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="3add1-119">In the Assignment end date, enter the date that the employee will stop working in their current position.</span></span>
    * <span data-ttu-id="3add1-120">新しい職位の開始日と古い職位の終了日は、重複する場合があります。</span><span class="sxs-lookup"><span data-stu-id="3add1-120">The starting date for the new position and the ending date of the old position may overlap.</span></span> <span data-ttu-id="3add1-121">この状況は、従業員が移行期間中に両方の職位の職務を実行しているときに発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3add1-121">This can happen when a person is performing duties for both positions during a transition period.</span></span>  
8. <span data-ttu-id="3add1-122">必要に応じて理由コードを選択できます。</span><span class="sxs-lookup"><span data-stu-id="3add1-122">Optionally, you can select a reason code.</span></span> <span data-ttu-id="3add1-123">例: 再編成</span><span class="sxs-lookup"><span data-stu-id="3add1-123">Example: Reorganization</span></span>
9. <span data-ttu-id="3add1-124">[職位の変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3add1-124">Click Change position.</span></span>
    * <span data-ttu-id="3add1-125">この時点で、報酬を変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="3add1-125">You may also change compensation at this time.</span></span> <span data-ttu-id="3add1-126">この時点で報酬を割り当てていない場合、作業者フォームに移動して、[報酬] タブを選択し、「固定プラン」を選択すると、報酬を変更できます。</span><span class="sxs-lookup"><span data-stu-id="3add1-126">If you do not assign compensation at this time, you can change it by going to the worker form, selecting the Compensation tab, and choosing 'Fixed Plan'.</span></span> <span data-ttu-id="3add1-127">「職位の変更」を選択すると、申請のステータスは「採用済」に更新されます。</span><span class="sxs-lookup"><span data-stu-id="3add1-127">After you select 'Change position', the status on the application will be updated to 'Employed'.</span></span>  

