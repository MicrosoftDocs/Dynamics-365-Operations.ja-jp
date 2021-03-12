---
title: 申請者およびアプリケーション データの手動入力
description: この手順では、手動で申請者とその申請に関する情報を管理する方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmApplicant, LogisticsContactInfoGrid, HRMApplication,  DirPartyTable
audience: Application User
ms.reviewer: anbichse
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a1039acd53f493e810b11aafd85116d034b7d323
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797316"
---
# <a name="enter-applicant-and-application-data-manually"></a><span data-ttu-id="a6e33-103">申請者およびアプリケーション データの手動入力</span><span class="sxs-lookup"><span data-stu-id="a6e33-103">Enter applicant and application data manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a6e33-104">この手順では、手動で申請者とその申請に関する情報を管理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a6e33-104">This procedure shows how to manually maintain information about applicants and their application.</span></span>   <span data-ttu-id="a6e33-105">申請者についての個人情報、面接の日時、能力、宿舎施設のリクエストを入力および管理できます。</span><span class="sxs-lookup"><span data-stu-id="a6e33-105">You can enter and maintain personal information, interview dates and times, references, competencies, and accommodation requests for applicants.</span></span> <span data-ttu-id="a6e33-106">また、雇用申請者の申請状態を更新し、申請者とやり取りを行う書状または電子メールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="a6e33-106">You can also update the status of applicants' applications for employment and create letters or email messages to communicate with applicants.</span></span> <span data-ttu-id="a6e33-107">申請者レコードを作成すると、その申請者の人物のレコードはグローバル アドレス帳で作成されます。</span><span class="sxs-lookup"><span data-stu-id="a6e33-107">When you create an applicant record, a person record for that applicant is created in the global address book.</span></span>       <span data-ttu-id="a6e33-108">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="a6e33-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-new-applicant-record"></a><span data-ttu-id="a6e33-109">新しいレコードの作成</span><span class="sxs-lookup"><span data-stu-id="a6e33-109">Create a new applicant record</span></span>
1. <span data-ttu-id="a6e33-110">[人事管理] > [採用] > [申請者] > [申請者] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a6e33-110">Go to Human resources > Recruitment > Applicants > Applicants.</span></span>
2. <span data-ttu-id="a6e33-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a6e33-111">Click New.</span></span>
3. <span data-ttu-id="a6e33-112">[名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a6e33-112">In the First name field, type a value.</span></span>
4. <span data-ttu-id="a6e33-113">[姓] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a6e33-113">In the Last name field, type a value.</span></span>
    * <span data-ttu-id="a6e33-114">可能な場合、追加の申請者情報を入力できます。</span><span class="sxs-lookup"><span data-stu-id="a6e33-114">You can enter additional applicant information if it's available.</span></span> <span data-ttu-id="a6e33-115">たとえば、申請者の最高学位、現在の職位、または以前の雇用者を申請者の情報として含めることができます。</span><span class="sxs-lookup"><span data-stu-id="a6e33-115">For example, information can include the applicant's highest degree, current job title, or previous employer.</span></span>  
5. <span data-ttu-id="a6e33-116">[連絡先情報] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="a6e33-116">Toggle the expansion of the Contact information section.</span></span>
6. <span data-ttu-id="a6e33-117">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a6e33-117">Click Add.</span></span>
7. <span data-ttu-id="a6e33-118">[説明] フィールドに、[電子メール通知] を入力します。</span><span class="sxs-lookup"><span data-stu-id="a6e33-118">In the Description field, type 'Communications email'.</span></span>
8. <span data-ttu-id="a6e33-119">[タイプ] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="a6e33-119">In the Type field, select an option.</span></span>
9. <span data-ttu-id="a6e33-120">[連絡先の電話番号/住所] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a6e33-120">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="a6e33-121">この電子メール アドレスは申請者との電子メール通信を生成するのに使用されるようになります。</span><span class="sxs-lookup"><span data-stu-id="a6e33-121">This email address will be used to generate email communication with the applicant.</span></span>  
10. <span data-ttu-id="a6e33-122">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a6e33-122">Click Add.</span></span>
11. <span data-ttu-id="a6e33-123">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a6e33-123">In the Description field, type a value.</span></span>
12. <span data-ttu-id="a6e33-124">[連絡先の電話番号/住所] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a6e33-124">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="a6e33-125">申請者の個人情報を編集します。</span><span class="sxs-lookup"><span data-stu-id="a6e33-125">Applicant personal information.</span></span>  
    * <span data-ttu-id="a6e33-126">必要に応じて、申請者の追加個人情報を入力できます。</span><span class="sxs-lookup"><span data-stu-id="a6e33-126">You can enter additional personal information for the applicant, if needed.</span></span> <span data-ttu-id="a6e33-127">たとえば、生年月日、出身民族、性別、または配偶者の有無を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="a6e33-127">For example, this can include birth date, ethnic origin, gender, or marital status.</span></span>  
13. <span data-ttu-id="a6e33-128">[アクション] ウィンドウで、[コンピテンシー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a6e33-128">On the Action Pane, click Competencies.</span></span>
    * <span data-ttu-id="a6e33-129">スキル、職務経験、教育、テスト、または資格証明書を含む申請者の能力プロファイルを入力できます。</span><span class="sxs-lookup"><span data-stu-id="a6e33-129">You can enter the applicant's competency profile, including their skills, professional experiences, education, tests, or certificates.</span></span>  
    * <span data-ttu-id="a6e33-130">この情報は、会社のデータで定義されているジョブと関連付けられるスキルを申請者のスキルとマップするのに使用できます。</span><span class="sxs-lookup"><span data-stu-id="a6e33-130">This information can be used to map the applicant's skills to the skills associated with the jobs defined in your company's data.</span></span>   

## <a name="create-an-application-for-the-applicant"></a><span data-ttu-id="a6e33-131">申請者のアプリケーションの作成</span><span class="sxs-lookup"><span data-stu-id="a6e33-131">Create an application for the applicant</span></span>
1. <span data-ttu-id="a6e33-132">[アプリケーション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a6e33-132">Click Applications.</span></span>
2. <span data-ttu-id="a6e33-133">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a6e33-133">Click New.</span></span>
3. <span data-ttu-id="a6e33-134">[採用プロジェクト] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="a6e33-134">In the Recruitment project field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a6e33-135">採用プロジェクトを選択することによって、申請者は、その採用プロジェクトに含まれている特定の空きと関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="a6e33-135">By selecting a recruitment project, the applicant will be associated with a specific opening included in that recruitment project.</span></span>  
4. <span data-ttu-id="a6e33-136">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="a6e33-136">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="a6e33-137">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a6e33-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a6e33-138">既定では、ジョブと部門は選択した採用プロジェクトに基づいています。</span><span class="sxs-lookup"><span data-stu-id="a6e33-138">By default, the job and department are based on the selected recruitment project.</span></span>  
6. <span data-ttu-id="a6e33-139">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a6e33-139">Click Save.</span></span>
    * <span data-ttu-id="a6e33-140">申請を保存した後、申請者の経験、報奨と送付状を含むドキュメントを添付できます。</span><span class="sxs-lookup"><span data-stu-id="a6e33-140">After saving the application, you can attach documents to it, including the applicant's experience, awards, and cover letter.</span></span>  

