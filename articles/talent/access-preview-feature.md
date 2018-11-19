---
title: "Talent のプレビュー機能の利用"
description: "このトピックでは、管理者がプレビュー機能を有効にできる方法について説明し、プレビューで現在有効な機能を一覧表示します。"
author: rschloma
manager: AnnBe
ms.date: 04/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: cd738cafc97477182e574ee0f363fdcf1df7da7a
ms.contentlocale: ja-jp
ms.lasthandoff: 10/22/2018

---

# <a name="access-preview-features-in-talent"></a><span data-ttu-id="8e85d-103">Talent のプレビュー機能の利用</span><span class="sxs-lookup"><span data-stu-id="8e85d-103">Access preview features in Talent</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8e85d-104">製品機能の継続的なロールアウトの一環として、お客様にできるだけ早く新しい機能を体験していただきたいと思います。</span><span class="sxs-lookup"><span data-stu-id="8e85d-104">As part of our continuous rollout of product capabilities, we want to let customers experience new features as soon as possible.</span></span> <span data-ttu-id="8e85d-105">管理者はそれぞれの環境でプレビュー機能を表示し使用することができます。</span><span class="sxs-lookup"><span data-stu-id="8e85d-105">Administrators can see and use preview features in their environments.</span></span> <span data-ttu-id="8e85d-106">これらの機能は、一般的な使用可能性の準備がほぼ整い、および徹底したテストを経ています。</span><span class="sxs-lookup"><span data-stu-id="8e85d-106">These features are almost ready for general availability and have gone through extensive testing.</span></span> <span data-ttu-id="8e85d-107">一般的なリリース前に、顧客フィードバックおよび検証の最終ラウンドを探しています。</span><span class="sxs-lookup"><span data-stu-id="8e85d-107">We are just looking for a final round of customer feedback and validation before we generally release them.</span></span>

<span data-ttu-id="8e85d-108">このトピックでは、管理者がプレビュー機能を有効にできる方法について説明し、プレビューで現在使用可能な機能を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="8e85d-108">This topic describes how an administrator can enable preview features, and it lists the features that are currently available for preview.</span></span> <span data-ttu-id="8e85d-109">このリストは、一般提供にリリースされる機能およびプレビューにリリースされる新しい機能として更新されます。</span><span class="sxs-lookup"><span data-stu-id="8e85d-109">This list will be updated as features are released to general availability and as new features are released to preview.</span></span> <span data-ttu-id="8e85d-110">プレビューに新しい機能がリリースされるときに、通知は表示されません。</span><span class="sxs-lookup"><span data-stu-id="8e85d-110">No notification is given when new features are released to preview.</span></span> <span data-ttu-id="8e85d-111">ユーザーは、機能を確認し始めます。</span><span class="sxs-lookup"><span data-stu-id="8e85d-111">Users will just start to see the features.</span></span>

## <a name="enable-or-disable-preview-features"></a><span data-ttu-id="8e85d-112">プレビュー機能の有効化または無効化</span><span class="sxs-lookup"><span data-stu-id="8e85d-112">Enable or disable preview features</span></span>

<span data-ttu-id="8e85d-113">Microsoft Dynamics 365 for Talent 管理者センターでプレビュー機能を有効化または無効化するため、**プレビュー機能**設定を使用できます。</span><span class="sxs-lookup"><span data-stu-id="8e85d-113">You can use the **Preview Features** setting in the Microsoft Dynamics 365 for Talent admin center to enable or disable preview features.</span></span> <span data-ttu-id="8e85d-114">既定では、設定がオフになっています。</span><span class="sxs-lookup"><span data-stu-id="8e85d-114">By default, the setting is turned off.</span></span> <span data-ttu-id="8e85d-115">プレビュー機能の有効化または無効化アクションは、環境に特有のものです。</span><span class="sxs-lookup"><span data-stu-id="8e85d-115">The action of enabling or disabling preview features is environment-specific.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8e85d-116">**プレビュー機能**設定をオンにして、その環境内の組織にいるすべてのユーザーに対してプレビュー機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="8e85d-116">By turning on the **Preview Features** setting, you enable preview features for all users in your organization who are in that environment.</span></span> <span data-ttu-id="8e85d-117">設定をオフにして、プレビュー機能を無効にし、ユーザーがアクセスできないようにします。</span><span class="sxs-lookup"><span data-stu-id="8e85d-117">By turning off the setting, you disable preview features and make them inaccessible to your users.</span></span> <span data-ttu-id="8e85d-118">プレビュー機能は、Talent でサポートが制限されます。</span><span class="sxs-lookup"><span data-stu-id="8e85d-118">Preview features have limited support in Talent.</span></span> <span data-ttu-id="8e85d-119">プライバシーとセキュリティ対策の使用は少なく、Talent サービス レベル契約には含まれません。</span><span class="sxs-lookup"><span data-stu-id="8e85d-119">They might use fewer privacy and security measures, and they aren't included in the Talent service level agreement.</span></span> <span data-ttu-id="8e85d-120">個人のデータ (つまり、ユーザーを識別する任意の情報)、または法律上または規制順守要件の対象となるその他のデータを処理するプレビュー機能を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="8e85d-120">You should not use preview features to process personal data (that is, any information that could identify you), or to process other data that is subject to legal or regulatory compliance requirements.</span></span>

### <a name="enable-or-disable-preview-features-for-your-organization"></a><span data-ttu-id="8e85d-121">組織のプレビュー機能を有効化または無効化します</span><span class="sxs-lookup"><span data-stu-id="8e85d-121">Enable or disable preview features for your organization</span></span>

#### <a name="attract"></a><span data-ttu-id="8e85d-122">Attract</span><span class="sxs-lookup"><span data-stu-id="8e85d-122">Attract</span></span>

1. <span data-ttu-id="8e85d-123">Microsoft Dynamics 365 for Talent: Attract にサインインします。</span><span class="sxs-lookup"><span data-stu-id="8e85d-123">Sign in to Microsoft Dynamics 365 for Talent: Attract.</span></span>
2. <span data-ttu-id="8e85d-124">右上隅の**設定**メニュー (ギヤ記号) で、**管理者設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8e85d-124">On the **Setup** menu (the gear symbol) in the upper-right corner, select **Admin settings**.</span></span>
3. <span data-ttu-id="8e85d-125">**機能の管理**タブで、**プレビュー機能**の横のオプションを選択し、青色になるようにします。</span><span class="sxs-lookup"><span data-stu-id="8e85d-125">On the **Feature management** tab, select the option next to **Preview features** so that it turns blue.</span></span>
4. <span data-ttu-id="8e85d-126">必要に応じて、このページの特定の機能を有効化/無効化することで個々の機能を制御できます。</span><span class="sxs-lookup"><span data-stu-id="8e85d-126">Optionally you can control individual features by enabling/disabling specific features on this page.</span></span>
5. <span data-ttu-id="8e85d-127">新しい機能の表示を開始するブラウザーを更新します。</span><span class="sxs-lookup"><span data-stu-id="8e85d-127">Refresh your browser to start to see the new features.</span></span> <span data-ttu-id="8e85d-128">(既にサインインしているすべてのユーザーは、次にサインインするときに機能を表示し、または機能をすぐに表示するためにそのブラウザーを更新することができます。)</span><span class="sxs-lookup"><span data-stu-id="8e85d-128">(Any users who are already signed in will see the features the next time that they sign in, or they can refresh their browser to see the features immediately.)</span></span>

#### <a name="core-hr"></a><span data-ttu-id="8e85d-129">Core HR</span><span class="sxs-lookup"><span data-stu-id="8e85d-129">Core HR</span></span>

1. <span data-ttu-id="8e85d-130">Talent へサインインします。</span><span class="sxs-lookup"><span data-stu-id="8e85d-130">Sign in to Talent.</span></span> <span data-ttu-id="8e85d-131">コア人事管理ワークスペースを開き、残りの手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="8e85d-131">The core Human resources workspace will open, from which you'll complete the remaining steps.</span></span> 
2. <span data-ttu-id="8e85d-132">**システム管理 \> リンク システム パラメーター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8e85d-132">Select **System administration \> Links System parameters**.</span></span>
3. <span data-ttu-id="8e85d-133">**プレビュー機能**タブの**システム パラメーター ページ**で、**すべてのユーザーに対してプレビュー モードを有効化する**オプションを**はい**に設定してプレビュー機能を使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="8e85d-133">On the **System Parameters page**, on the **Preview features** tab, set the **Enable preview mode for all users** option to **Yes** to make preview features available.</span></span>

> [!NOTE]
> <span data-ttu-id="8e85d-134">プレビュー機能を無効にするには、同じ基本的な手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="8e85d-134">To disable preview features, use the same basic steps.</span></span> <span data-ttu-id="8e85d-135">プレビュー機能を無効にすると、ユーザーがアクセスできなくなり、機能に関連付けられているプロセスでエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8e85d-135">When you disable preview features, they become inaccessible to your users, and errors might occur in processes that are associated with the features.</span></span>

## <a name="features-that-are-currently-in-preview"></a><span data-ttu-id="8e85d-136">現在プレビューにある機能</span><span class="sxs-lookup"><span data-stu-id="8e85d-136">Features that are currently in preview</span></span>

### <a name="attract"></a><span data-ttu-id="8e85d-137">人材の獲得</span><span class="sxs-lookup"><span data-stu-id="8e85d-137">Attract</span></span>

- <span data-ttu-id="8e85d-138">**職務の関連候補者** – 採用担当者および雇用マネージャーは、すべての申請者の中で、どの候補者が任務に最も関連性があるかを簡単に確認することができます。</span><span class="sxs-lookup"><span data-stu-id="8e85d-138">**Relevant Candidates in a Job** – Recruiters and hiring managers can easily see which candidates may be the most relevant for the job across all applicants.</span></span> <span data-ttu-id="8e85d-139">上位 5 名の申請者は、自分の経歴書/プロファイルと職務内容の関連性に基づいて表示されます。</span><span class="sxs-lookup"><span data-stu-id="8e85d-139">The top 5 applicants are shown based on their the relevance of their resume/profile to the job description.</span></span>
- <span data-ttu-id="8e85d-140">**関連する職務** – 経歴書/プロファイルと任務内容に基づいて、候補者に関連するその他のジョブの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="8e85d-140">**Relevant Jobs** – Candidates now see a list of other jobs that are relevant to them based on their resume/profile and the job descriptions.</span></span>  <span data-ttu-id="8e85d-141">現在別の機会の候補として適用されると、候補者に表示されます。</span><span class="sxs-lookup"><span data-stu-id="8e85d-141">Currently this is shown to candidates once they apply as a suggestion for other opportunities.</span></span>
- <span data-ttu-id="8e85d-142">**EEO/OFCCP サポート** – 新しい活動タイプは、候補者からの雇用機会均等 (EEO) および連邦契約遵守プログラム部 (OFCCP) データの収集のため、事前に定義されたフォームの使用を可能にします。</span><span class="sxs-lookup"><span data-stu-id="8e85d-142">**EEO/OFCCP Support** – New activity types enable the use of a predefined form for the collection of Equal Employment Opportunity  (EEO) and Office of Federal Contract Compliance Program (OFCCP) data from the candidate.</span></span>  <span data-ttu-id="8e85d-143">これは事前に定義されたフォームで、編集できません。</span><span class="sxs-lookup"><span data-stu-id="8e85d-143">This is a predefined form and is not editable.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8e85d-144">投稿される求人は、1 つまたは複数の LinkedIn 人材募集の製品にサブスクライブしている顧客にのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="8e85d-144">Jobs that are posted are visible only to customers who subscribe to one or more LinkedIn job listing products.</span></span> <span data-ttu-id="8e85d-145">それ以外の場合は、顧客は明示的に検索する場合にのみ職務を表示します。</span><span class="sxs-lookup"><span data-stu-id="8e85d-145">Otherwise, customers see a job only if they explicitly search for it.</span></span> <span data-ttu-id="8e85d-146">求人が LinkedIn に投稿されるときに遅延が発生します。</span><span class="sxs-lookup"><span data-stu-id="8e85d-146">There is a delay when jobs are posted to LinkedIn.</span></span> <span data-ttu-id="8e85d-147">職務が Attract からの投稿後に表示されるには数時間かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="8e85d-147">A job might take up to a few hours to appear after it's posted from Attract.</span></span>

- <span data-ttu-id="8e85d-148">**候補者の適用**– 内部および外部の候補者が、キャリア サイトのジョブ ページから直接適用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="8e85d-148">**Candidate apply** – Both internal and external candidates can now apply directly from the job page on the career site.</span></span>
- <span data-ttu-id="8e85d-149">**オファー管理**– ユーザーはプレースホルダーを含むテンプレートからオファー レターを作成できるようになります。</span><span class="sxs-lookup"><span data-stu-id="8e85d-149">**Offer management** – Users can now create offer letters from templates that include placeholders.</span></span> <span data-ttu-id="8e85d-150">オファー ステージに進む候補者として、採用担当者および雇用マネージャーは、テンプレートを通して候補者の正式なオファーを準備するオファー ツールを使用でき、内部認証のオファーを送信し、さらに最終的に署名のために候補者にオファーを送信できます。</span><span class="sxs-lookup"><span data-stu-id="8e85d-150">As candidates advance to the Offer stage, recruiters and hiring managers can use the Offer tool to prepare a candidate's formal offer via templates, send the offer for internal approval, and finally send the offer to the candidate for signature.</span></span> <span data-ttu-id="8e85d-151">時間の経過と共に多くの新しい機能がオファー ツールに追加され、プレビューにリリースする準備が整っているため、プレビュー機能がこれらの機能により更新されます。</span><span class="sxs-lookup"><span data-stu-id="8e85d-151">Many new capabilities will be added to the Offer tool over time, and the preview feature will be updated with these capabilities as we are ready to release them to preview.</span></span>

### <a name="core-hr"></a><span data-ttu-id="8e85d-152">Core HR</span><span class="sxs-lookup"><span data-stu-id="8e85d-152">Core HR</span></span>

- <span data-ttu-id="8e85d-153">**自由登録**– 給付金の自由登録は従業員に、給付金を選択するための単純なセルフ サービス エクスペリエンスを提供します。</span><span class="sxs-lookup"><span data-stu-id="8e85d-153">**Open Enrollment** – Benefits open enrollment gives employees a simple, self-service experience for selecting their benefits.</span></span> <span data-ttu-id="8e85d-154">分かりやすいガイド付きソリューションを使用して、人事管理 (HR) の管理者は組織の給付金の自由登録プロセス、および従業員の登録エクスペリエンスを構成できます。</span><span class="sxs-lookup"><span data-stu-id="8e85d-154">Human Resource (HR) administrators can configure the benefits open enrollment process for their organization, and the enrollment experience for employees, by using an easy-to-follow guided solution.</span></span>

## <a name="feedback"></a><span data-ttu-id="8e85d-155">フィードバック</span><span class="sxs-lookup"><span data-stu-id="8e85d-155">Feedback</span></span>

<span data-ttu-id="8e85d-156">フィードバックがポジティブまたはネガティブかどうかに関係なく、プレビュー機能の使用に関するお客様の率直なご意見をお聞かせください。</span><span class="sxs-lookup"><span data-stu-id="8e85d-156">Regardless of whether the feedback is positive or negative, we want to hear from you about your use of the preview features.</span></span> <span data-ttu-id="8e85d-157">これらまたはその他の機能を使用する際に、以下のサイトでフィードバックを定期的に転記することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="8e85d-157">We encourage you to regularly post your feedback on the following sites as you use these or any other features.</span></span>

- <span data-ttu-id="8e85d-158">[コミュニティ](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – このサイトは、ユーザーが使用ケースを説明したり、質問したり、およびコミュニティ ヘルプを得られる優れたリソースです。</span><span class="sxs-lookup"><span data-stu-id="8e85d-158">[Community](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – This site is a great resource where users can discuss use cases, ask questions, and get community help.</span></span>
- <span data-ttu-id="8e85d-159">製品アイデアを提示する以下のサイトを使用します。</span><span class="sxs-lookup"><span data-stu-id="8e85d-159">Use the following sites to suggest product ideas.</span></span> <span data-ttu-id="8e85d-160">製品に必要な機能、および既存の機能に対して行われるべき変更があればお知らせください。</span><span class="sxs-lookup"><span data-stu-id="8e85d-160">Let us know about features that you want to see in the product, and also any changes that you think should be made to existing features.</span></span>

    - [<span data-ttu-id="8e85d-161">Attract アイデア</span><span class="sxs-lookup"><span data-stu-id="8e85d-161">Attract Ideas</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [<span data-ttu-id="8e85d-162">Core HR</span><span class="sxs-lookup"><span data-stu-id="8e85d-162">Core HR</span></span>](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources)

<span data-ttu-id="8e85d-163">フィードバックまたは製品のレビュー申請には個人データ (ユーザーを識別できる任意の情報) を含めないでください。</span><span class="sxs-lookup"><span data-stu-id="8e85d-163">Don't include personal data (any information that could identify you) in your feedback or product review submissions.</span></span> <span data-ttu-id="8e85d-164">収集した情報はさらに分析されることがありますが、該当するプライバシーに関する法律の下で要求に回答するためには使用されません。</span><span class="sxs-lookup"><span data-stu-id="8e85d-164">Information that is collected might be analyzed further, and it won't be used to answer requests under applicable privacy laws.</span></span> <span data-ttu-id="8e85d-165">これらのプログラムで個別に収集された個人データは、[Microsoft のプライバシーに関する声明](https://privacy.microsoft.com/privacystatement) の対象となります。</span><span class="sxs-lookup"><span data-stu-id="8e85d-165">Personal data that is collected separately under these programs is subject to the [Microsoft Privacy Statement](https://privacy.microsoft.com/privacystatement).</span></span>

> [!TIP]
> <span data-ttu-id="8e85d-166">リリースに際して新しいプレビュー機能に関して最新の状態を保つため、このトピックをブックマークし、頻繁に確認してください。</span><span class="sxs-lookup"><span data-stu-id="8e85d-166">Bookmark this topic, and check back often to stay up to date about new preview features as we release them.</span></span>

