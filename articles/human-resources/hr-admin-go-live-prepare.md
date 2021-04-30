---
title: Human Resources - Go Live の準備
description: このページでは、Dynamics 365 Human Resources の準備に関するガイダンスをあつかいます。
author: rachel-profitt
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: df2c55a8a69efa20c6d8c41e97c9e1f80ee1640d
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892756"
---
# <a name="prepare-for-human-resources-go-live"></a><span data-ttu-id="ad064-103">Human Resources - Go Live の準備</span><span class="sxs-lookup"><span data-stu-id="ad064-103">Prepare for Human Resources go-live</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ad064-104">このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を使用して Dynamics 365 Human Resources プロジェクトにおける go live の準備方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="ad064-104">This topic describes how to prepare to go live with a Dynamics 365 Human Resources project by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> 

<span data-ttu-id="ad064-105">この図には、Go-Live プロセスのフェーズが表示しています。</span><span class="sxs-lookup"><span data-stu-id="ad064-105">This graphic shows the phases of the go-live process.</span></span> 

![Go-live プロセス](./media/hr-admin-go-live-prepare-process.png)

<span data-ttu-id="ad064-107">次のテーブルでは、プロセスのすべてのステップと、予定期間と、誰が処理を実行するのかについて示しています。</span><span class="sxs-lookup"><span data-stu-id="ad064-107">The following table lists all the steps in the process, the expected duration, and who is responsible for the action.</span></span>

| <span data-ttu-id="ad064-108">フェーズ</span><span class="sxs-lookup"><span data-stu-id="ad064-108">Phase</span></span> | <span data-ttu-id="ad064-109">アクション</span><span class="sxs-lookup"><span data-stu-id="ad064-109">Action</span></span> | <span data-ttu-id="ad064-110">期間/時</span><span class="sxs-lookup"><span data-stu-id="ad064-110">Duration/When</span></span> | <span data-ttu-id="ad064-111">誰</span><span class="sxs-lookup"><span data-stu-id="ad064-111">Who</span></span> | <span data-ttu-id="ad064-112">摘要</span><span class="sxs-lookup"><span data-stu-id="ad064-112">Notes</span></span> |
| --- | --- | --- | --- |--- |
| <span data-ttu-id="ad064-113">1</span><span class="sxs-lookup"><span data-stu-id="ad064-113">1</span></span> | <span data-ttu-id="ad064-114">LCS での Go-Live 日付の更新</span><span class="sxs-lookup"><span data-stu-id="ad064-114">Update go-live date in LCS</span></span> | <span data-ttu-id="ad064-115">遅くとも 2 ～ 3 か月前に</span><span class="sxs-lookup"><span data-stu-id="ad064-115">At the latest 2-3 months in advance</span></span> | <span data-ttu-id="ad064-116">パートナー/顧客</span><span class="sxs-lookup"><span data-stu-id="ad064-116">Partner/Customer</span></span> | <span data-ttu-id="ad064-117">マイルストーンの日付は、継続的に最新のものにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ad064-117">The milestone dates should be kept up to date on an ongoing basis.</span></span> |
| <span data-ttu-id="ad064-118">2</span><span class="sxs-lookup"><span data-stu-id="ad064-118">2</span></span> | <span data-ttu-id="ad064-119">チェックリストの完了および送信</span><span class="sxs-lookup"><span data-stu-id="ad064-119">Complete and send checklist</span></span> | <span data-ttu-id="ad064-120">ユーザー受け入れテスト (UAT) が完了した後</span><span class="sxs-lookup"><span data-stu-id="ad064-120">After user acceptance testing (UAT) is complete</span></span> | <span data-ttu-id="ad064-121">パートナー/顧客</span><span class="sxs-lookup"><span data-stu-id="ad064-121">Partner/Customer</span></span> | <span data-ttu-id="ad064-122">[FastTrack Go-live アセスメントの](hr-admin-go-live-prepare.md#fasttrack-go-live-assessment)に記載の指示に従います。</span><span class="sxs-lookup"><span data-stu-id="ad064-122">Follow the instructions provided in [FastTrack go-live assessment](hr-admin-go-live-prepare.md#fasttrack-go-live-assessment).</span></span> |
| <span data-ttu-id="ad064-123">3</span><span class="sxs-lookup"><span data-stu-id="ad064-123">3</span></span> | <span data-ttu-id="ad064-124">プロジェクト評価 (FastTrack)</span><span class="sxs-lookup"><span data-stu-id="ad064-124">Project assessment (FastTrack)</span></span> | <span data-ttu-id="ad064-125">FastTrack アーキテクト\*</span><span class="sxs-lookup"><span data-stu-id="ad064-125">FastTrack Architect\*</span></span> | <span data-ttu-id="ad064-126">アーキテクトは、チェックリストを受け取った後に評価を提供し、質問が明確化および軽減されるまでレビューを続行します。</span><span class="sxs-lookup"><span data-stu-id="ad064-126">Architect delivers assessment after checklist is received and continues review until questions are clarified and mitigations are in place, if applicable.</span></span> |
| <span data-ttu-id="ad064-127">4</span><span class="sxs-lookup"><span data-stu-id="ad064-127">4</span></span> | <span data-ttu-id="ad064-128">プロジェクト ワークショップ (FastTrack)</span><span class="sxs-lookup"><span data-stu-id="ad064-128">Project workshop (FastTrack)</span></span> | <span data-ttu-id="ad064-129">FastTrack アーキテクト\*</span><span class="sxs-lookup"><span data-stu-id="ad064-129">FastTrack Architect\*</span></span> | |
| <span data-ttu-id="ad064-130">5</span><span class="sxs-lookup"><span data-stu-id="ad064-130">5</span></span> | <span data-ttu-id="ad064-131">データ パッケージのインポート</span><span class="sxs-lookup"><span data-stu-id="ad064-131">Data package imports</span></span> | <span data-ttu-id="ad064-132">プロジェクトによって異なります</span><span class="sxs-lookup"><span data-stu-id="ad064-132">Depends on the project</span></span> | <span data-ttu-id="ad064-133">パートナー/顧客</span><span class="sxs-lookup"><span data-stu-id="ad064-133">Partner/Customer</span></span> | <span data-ttu-id="ad064-134">[データ管理の概要](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md)の指示に従います。</span><span class="sxs-lookup"><span data-stu-id="ad064-134">Follow the instructions in [Data management overview](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span></span>|
| <span data-ttu-id="ad064-135">6</span><span class="sxs-lookup"><span data-stu-id="ad064-135">6</span></span> | <span data-ttu-id="ad064-136">生産準備完了</span><span class="sxs-lookup"><span data-stu-id="ad064-136">Production ready</span></span> | <span data-ttu-id="ad064-137">前の手順すべてが完了した後</span><span class="sxs-lookup"><span data-stu-id="ad064-137">After all previous steps have been completed</span></span> | <span data-ttu-id="ad064-138">パートナー/顧客</span><span class="sxs-lookup"><span data-stu-id="ad064-138">Partner/Customer</span></span> | <span data-ttu-id="ad064-139">顧客/パートナーが引用環境を制御することができます。</span><span class="sxs-lookup"><span data-stu-id="ad064-139">Partner/Customer can take control of the production environment.</span></span>|
| <span data-ttu-id="ad064-140">7</span><span class="sxs-lookup"><span data-stu-id="ad064-140">7</span></span> | <span data-ttu-id="ad064-141">切替活動</span><span class="sxs-lookup"><span data-stu-id="ad064-141">Cutover activities</span></span> | <span data-ttu-id="ad064-142">プロジェクトによって異なります</span><span class="sxs-lookup"><span data-stu-id="ad064-142">Depends on the project</span></span> | <span data-ttu-id="ad064-143">パートナー/顧客</span><span class="sxs-lookup"><span data-stu-id="ad064-143">Partner/Customer</span></span> | |
| <span data-ttu-id="ad064-144">8</span><span class="sxs-lookup"><span data-stu-id="ad064-144">8</span></span> | <span data-ttu-id="ad064-145">Go live</span><span class="sxs-lookup"><span data-stu-id="ad064-145">Go live</span></span> | <span data-ttu-id="ad064-146">プロジェクトによって異なります</span><span class="sxs-lookup"><span data-stu-id="ad064-146">Depends on the project</span></span> | <span data-ttu-id="ad064-147">顧客</span><span class="sxs-lookup"><span data-stu-id="ad064-147">Customer</span></span> | |

> [!IMPORTANT]
> <span data-ttu-id="ad064-148">\*手順 3 と 手順 4 は、FastTrack の対象顧客に対してのみ実行されます。</span><span class="sxs-lookup"><span data-stu-id="ad064-148">\*Steps 3 and 4 are only completed for customers who qualify for FastTrack.</span></span>

## <a name="completing-the-lcs-methodology"></a><span data-ttu-id="ad064-149">LCS メソッドを完了しています</span><span class="sxs-lookup"><span data-stu-id="ad064-149">Completing the LCS methodology</span></span>

<span data-ttu-id="ad064-150">各実装プロジェクトにおける主要なマイルストーンは、実稼働環境への切替です。</span><span class="sxs-lookup"><span data-stu-id="ad064-150">A major milestone in each implementation project is the cutover to the production environment.</span></span> <span data-ttu-id="ad064-151">ステップを完了するプロセスは 2 つの部分で成り立っています。</span><span class="sxs-lookup"><span data-stu-id="ad064-151">The process of completing a step has two parts:</span></span> 

- <span data-ttu-id="ad064-152">フィット ギャップ解析またはユーザー受け入れテスト (UAT) など、実際の作業を行います。</span><span class="sxs-lookup"><span data-stu-id="ad064-152">Do the actual work, such as a fit-gap analysis or user acceptance testing (UAT).</span></span> 
- <span data-ttu-id="ad064-153">LCS 方法の対応するステップを完了としてマークします。</span><span class="sxs-lookup"><span data-stu-id="ad064-153">Mark the corresponding step in the LCS methodology as completed.</span></span> 

<span data-ttu-id="ad064-154">実装の進捗状況に応じて方法のステップを完了することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ad064-154">It's a good practice to complete the steps in the methodology as you make progress with the implementation.</span></span> <span data-ttu-id="ad064-155">最後まで待たないでください。</span><span class="sxs-lookup"><span data-stu-id="ad064-155">Don't wait until the last minute.</span></span> <span data-ttu-id="ad064-156">確かな実装が顧客の最高の利益となります。</span><span class="sxs-lookup"><span data-stu-id="ad064-156">It's in the customer's best interest to have a solid implementation.</span></span> 

## <a name="uat-for-your-solution"></a><span data-ttu-id="ad064-157">ソリューションの UAT</span><span class="sxs-lookup"><span data-stu-id="ad064-157">UAT for your solution</span></span>

<span data-ttu-id="ad064-158">UAT のフェーズでは、実装プロジェクトのサンドボックス環境で、実装したすべてのビジネス プロセスとカスタマイズをテストする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ad064-158">During the UAT phase, you must test all the business processes you've implemented, and any customizations you've made, in a Sandbox environment in the implementation project.</span></span> <span data-ttu-id="ad064-159">実稼働運用を成功させるためには、UAT フェーズを完了する際に次の点を考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ad064-159">To help ensure a successful go-live, you should consider the following as you complete the UAT phase:</span></span> 

- <span data-ttu-id="ad064-160">UAT のプロセスは、このプロセスを開始する前に、GOLD 構成からのデータを環境にコピーした新しい環境で開始することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ad064-160">We recommend that your UAT process starts with a clean and fresh environment where the data from your GOLD configuration is copied into the environment prior to the start of the UAT process.</span></span> <span data-ttu-id="ad064-161">環境が本番稼働するまでは、運用環境をGOLD環境として利用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ad064-161">We recommend that you use the production environment as your GOLD environment until you go-live, at which point the environment becomes production.</span></span>
- <span data-ttu-id="ad064-162">テスト ケースは、要件の範囲全体をカバーします。</span><span class="sxs-lookup"><span data-stu-id="ad064-162">Test cases cover the entire scope of requirements.</span></span> 
- <span data-ttu-id="ad064-163">移行したデータを使用してテストします。</span><span class="sxs-lookup"><span data-stu-id="ad064-163">Test by using migrated data.</span></span> <span data-ttu-id="ad064-164">これには、作業者、職務、職位などのデータを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="ad064-164">This should include data such as workers, jobs, and positions.</span></span> <span data-ttu-id="ad064-165">また、休暇および休暇の見越計上と同様に、期首残高も含めます。</span><span class="sxs-lookup"><span data-stu-id="ad064-165">Also include opening balances, like leave and absence accruals.</span></span> <span data-ttu-id="ad064-166">最後に、現在の福利厚生の登録など、未処理のトランザクションを含めます。</span><span class="sxs-lookup"><span data-stu-id="ad064-166">Finally, include open transactions, such as current benefits enrollments.</span></span> <span data-ttu-id="ad064-167">データセットが確定していない場合でも、すべてのタイプのデータで完全なテストを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="ad064-167">Complete testing with all types of data, even if the data set isn't finalized.</span></span> 
- <span data-ttu-id="ad064-168">ユーザーに割り当てられている適切なセキュリティ ロール (既定のロールおよびカスタム ロール) を使用してテストします。</span><span class="sxs-lookup"><span data-stu-id="ad064-168">Test by using the correct security roles (default roles and custom roles) that are assigned to users.</span></span> 
- <span data-ttu-id="ad064-169">ソリューションが会社や業界別の規制要件に準拠していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="ad064-169">Make sure that the solution complies with any company- and industry-specific regulatory requirements.</span></span> 
- <span data-ttu-id="ad064-170">すべての機能を文書化し、顧客の承認とサインオフを取得します。</span><span class="sxs-lookup"><span data-stu-id="ad064-170">Document all features and obtain approval and sign-off from the customer.</span></span> 

## <a name="mock-go-live"></a><span data-ttu-id="ad064-171">モック環境の本番稼働</span><span class="sxs-lookup"><span data-stu-id="ad064-171">Mock go-live</span></span>

<span data-ttu-id="ad064-172">本番稼働に先立ち、レガシーシステムから新システムへの稼働開始に必要なステップをテストするために、模擬稼働を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ad064-172">Prior to your go-live, you must perform a mock go-live to test the steps required to cutover from your legacy systems to the new system.</span></span> <span data-ttu-id="ad064-173">サンドボックス環境で模擬稼働を実行し、稼働開始の計画にすべてのステップを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="ad064-173">You should perform your mock go-live in a sandbox environment and include all the steps in your cutover plan.</span></span>

- <span data-ttu-id="ad064-174">稼働開始までは、運用環境を GOLD 構成環境として使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ad064-174">We recommend you use the production environment as the GOLD configuration environment until the go-live.</span></span>
- <span data-ttu-id="ad064-175">本番前の偶発的なトランザクションや更新から本番環境を保護するために、強力なガバナンス プロセスを導入してください。</span><span class="sxs-lookup"><span data-stu-id="ad064-175">Ensure that you have a strong governance process in place to protect the production environment from accidental transactions or updates prior to the go-live.</span></span>
- <span data-ttu-id="ad064-176">UAT を実施する準備、または模擬稼働の準備が整った場合、運用環境からサンドボックス環境を更新します。</span><span class="sxs-lookup"><span data-stu-id="ad064-176">When you're ready to perform UAT or the mock go-live, refresh the sandbox environment from the production environment.</span></span> <span data-ttu-id="ad064-177">詳細については、[インスタンスのコピー](hr-admin-setup-copy-instance.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ad064-177">For more information, see [Copy an instance](hr-admin-setup-copy-instance.md).</span></span>
- <span data-ttu-id="ad064-178">サンドボックス環境で本稼働計画に含まれる各ステップをテストし、スポット チェックの実行や、環境内の UAT スクリプトからテストを実行して、サンドボックス環境を検証します。</span><span class="sxs-lookup"><span data-stu-id="ad064-178">Test each step of your cutover plan in the sandbox environment and then validate the sandbox environment by performing spot checks or performing tests from your UAT scripts in the environment.</span></span>
  - <span data-ttu-id="ad064-179">テストには、本稼働に必要な変換を含むすべてのデータ移行が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="ad064-179">Tests should include all data migrations including transformations needed for the go-live.</span></span>
  - <span data-ttu-id="ad064-180">このプロセスには、レガシー システムのプラクティスのカットオフが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="ad064-180">The process should include a practice cutoff of any legacy systems.</span></span>
  - <span data-ttu-id="ad064-181">統合カットオーバーに含まれるステップや外部システムに含まれるステップは、必ず模擬稼働に含めるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="ad064-181">Be sure to include any integration cutover steps or external system steps in your mock cutover.</span></span>
- <span data-ttu-id="ad064-182">模試稼働中に課題が見つかった場合は、2回の模擬稼働が必要となるかもしれません。</span><span class="sxs-lookup"><span data-stu-id="ad064-182">If you find any issues during the mock cutover, a second mock-cutover may be required.</span></span> <span data-ttu-id="ad064-183">そのため、プロジェクト計画では、2 つの模試稼働を計画することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ad064-183">For this reason, we recommend that you plan for two mock cutovers in your project plan.</span></span>

## <a name="fasttrack-go-live-assessment"></a><span data-ttu-id="ad064-184">FastTrack Go-live アセスメント</span><span class="sxs-lookup"><span data-stu-id="ad064-184">FastTrack go-live assessment</span></span>

<span data-ttu-id="ad064-185">FastTrack の対象となっていて、FastTrack ソリューションアーキテクトと契約しているお客様は、Microsoft FastTrack を使用した Go-live レビューを完了します。</span><span class="sxs-lookup"><span data-stu-id="ad064-185">Customers who are qualified for FastTrack and are engaged with a FastTrack Solution Architect will complete a go-live review with Microsoft FastTrack.</span></span> <span data-ttu-id="ad064-186">詳細については、  [Microsoft FastTrack](/dynamics365/fasttrack/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ad064-186">For more information, see [Microsoft FastTrack](/dynamics365/fasttrack/).</span></span> 

<span data-ttu-id="ad064-187">Go-Live の約 8 週間前に、FastTrack チームが [Go-Live チェックリスト](https://go.microsoft.com/fwlink/?linkid=2146013)への記入を依頼します。</span><span class="sxs-lookup"><span data-stu-id="ad064-187">About eight weeks before go-live, the FastTrack team will ask you to fill in a [Go-live checklist](https://go.microsoft.com/fwlink/?linkid=2146013).</span></span>

<span data-ttu-id="ad064-188">プロジェクト マネージャーまたはプロジェクトの主要メンバーは、プロジェクトの Go-Live 前の段階の間に Go-Live チェックリストを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ad064-188">The project manager or a key project member must complete the go-live checklist during the pre-go-live phase of the project.</span></span> <span data-ttu-id="ad064-189">チェックリストは通常、稼働予定日の 4 ~ 6 週間前に完了し、UAT が完了したか、ほぼ完了したときです。</span><span class="sxs-lookup"><span data-stu-id="ad064-189">Typically, the checklist is completed four to six weeks before the proposed go-live date, when UAT is completed or almost completed.</span></span> 

<span data-ttu-id="ad064-190">Go-Live チェックリスト を完了したら、電子メールで、FastTrack ソリューション アーキテクトに送信します。</span><span class="sxs-lookup"><span data-stu-id="ad064-190">When you've completed the go-live checklist, email it to your FastTrack Solution Architect.</span></span> <span data-ttu-id="ad064-191">電子メールには、顧客からの主な関係者と実装パートナーを必ず含めます。</span><span class="sxs-lookup"><span data-stu-id="ad064-191">Always include a key stakeholder from the customer and the implementation partner on the email.</span></span> 

<span data-ttu-id="ad064-192">チェックリストを提出した後、FastTrack ソリューション アーキテクトがプロジェクトをレビューし、潜在的なリスク、ベスト プラクティス、プロジェクトの運用を成功させるにあたっての推奨事項を記載した評価を提供します。</span><span class="sxs-lookup"><span data-stu-id="ad064-192">After you submit the checklist, your FastTrack Solution Architect will review the project and provide an assessment that describes the potential risks, best practices, and recommendations for a successful go-live of the project.</span></span> <span data-ttu-id="ad064-193">場合によっては、ソリューション アーキテクトがリスク要因を強調表示し、軽減計画を求める場合があります。</span><span class="sxs-lookup"><span data-stu-id="ad064-193">In some cases, the solution architect might highlight risk factors and ask for a mitigation plan.</span></span> 

## <a name="see-also"></a><span data-ttu-id="ad064-194">参照</span><span class="sxs-lookup"><span data-stu-id="ad064-194">See also</span></span>

[<span data-ttu-id="ad064-195">Go-Live に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="ad064-195">Go-live FAQ</span></span>](hr-admin-go-live-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
