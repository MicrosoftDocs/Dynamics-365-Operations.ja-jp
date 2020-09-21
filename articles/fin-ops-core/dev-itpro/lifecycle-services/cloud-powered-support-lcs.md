---
title: Finance and Operations アプリのサポート エクスペリエンスを管理する
description: このトピックでは、Microsoft Dynamics Lifecycle Services のサポート ツールを使用して、サポート インシデントを管理する方法について説明します。
author: kfend
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 60373
ms.assetid: 0fa10573-8146-446e-8124-8a7af9546add
ms.search.region: Global
ms.author: anupams
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c8e908264901eda9be312caf98e97c043b64f4de
ms.sourcegitcommit: fa5c45f7842c4d20c994ac1655e2fbf2a1cf14a9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/28/2020
ms.locfileid: "3734892"
---
# <a name="manage-the-support-experiences-for-finance-and-operations-apps"></a><span data-ttu-id="4850e-103">Finance and Operations アプリのサポート エクスペリエンスを管理する</span><span class="sxs-lookup"><span data-stu-id="4850e-103">Manage the support experiences for Finance and Operations apps</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4850e-104">サポート ツールを使用するには、あらかじめ Lifecycle Services (LCS) でプロジェクトを作成して、環境にシステム診断プログラムをインストールして実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4850e-104">To use the Support tool, you must have previously created a project in Lifecycle Services (LCS) and installed and ran the System diagnostics in your environment.</span></span> <span data-ttu-id="4850e-105">詳細については、 [Lifecycle Services (LCS) の システム診断](ax-2012/system-diagnostics-lcs.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4850e-105">For more information, see [System diagnostics in Lifecycle Services (LCS)](ax-2012/system-diagnostics-lcs.md).</span></span>

## <a name="open-a-new-incident"></a><span data-ttu-id="4850e-106">新しいインシデントを開く</span><span class="sxs-lookup"><span data-stu-id="4850e-106">Open a new incident</span></span>
1. <span data-ttu-id="4850e-107">LCS にて、サポート インシデントを提出するプロジェクトに移動します。</span><span class="sxs-lookup"><span data-stu-id="4850e-107">In LCS, go to the project for which you want to file a support incident.</span></span> 

2. <span data-ttu-id="4850e-108">**サポート** タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="4850e-108">Click the **Support** tile.</span></span>

   ![サポート メニュー](media/CPS1.png)

3. <span data-ttu-id="4850e-110">**Microsoft に送信**タブで、**インシデントの送信**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="4850e-110">On the **Submitted to Microsoft** tab, click the **Submit an incident** button.</span></span>

   ![サポート ボタン](media/CPS2.png)

4. <span data-ttu-id="4850e-112">問題のカテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="4850e-112">Select an issue category.</span></span>

5. <span data-ttu-id="4850e-113">問題の領域を選択します。</span><span class="sxs-lookup"><span data-stu-id="4850e-113">Select an issue area.</span></span>

6. <span data-ttu-id="4850e-114">**問題の説明** 欄で、次の内容を入力します。</span><span class="sxs-lookup"><span data-stu-id="4850e-114">In the **Describe your issue** area, enter the following:</span></span>

   - <span data-ttu-id="4850e-115">環境で問題が発生した場合は、 **はい** を選択して下さい。</span><span class="sxs-lookup"><span data-stu-id="4850e-115">Select **Yes** if the issue occurred in an environment.</span></span> <span data-ttu-id="4850e-116">環境名を選択します。</span><span class="sxs-lookup"><span data-stu-id="4850e-116">Select the environment name.</span></span>  
   - <span data-ttu-id="4850e-117">**タイトル**フィールドの問題について短い説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="4850e-117">Enter a short description of your issue in the **Title** field.</span></span>
   - <span data-ttu-id="4850e-118">問題の詳細と、エラーを再生成するために必要なステップに関する詳細を提供します。</span><span class="sxs-lookup"><span data-stu-id="4850e-118">Provide details about the issue detail and the steps needed to reproduce the error.</span></span>
   - <span data-ttu-id="4850e-119">該当する場合は、エラー メッセージを入力します。</span><span class="sxs-lookup"><span data-stu-id="4850e-119">If applicable, enter an error message.</span></span> 
   - <span data-ttu-id="4850e-120">可能であれば、問題を示すスクリーン ショットを関連付けます。</span><span class="sxs-lookup"><span data-stu-id="4850e-120">If possible, attach screenshots that illustrate the problem.</span></span> <span data-ttu-id="4850e-121">これを行うには、**コンピュータからの添付ファイル** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4850e-121">To do this, click **Attach file from computer**.</span></span>
 
 
   > [!NOTE]
   > <span data-ttu-id="4850e-122">インシデントを作成するときは、問題検索によって、ユーザーの選択と入力にもとづいて、上位 10 の「実行可能な問題のソリューション」という検索結果が設定され、サポート ケースの作成時に詳細情報が提供されると、これらの結果が動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="4850e-122">When you create an incident, Issue search will populate the top 10 "Possible issue solutions" search results based on the your selection and input, and dynamically refresh these results as more details are provided during support case creation.</span></span> 
   > 
   > <span data-ttu-id="4850e-123">さらにソリューションを検索する必要がある場合は、ドロップダウン メニューからスタンドアロン問題検索にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="4850e-123">Standalone Issue search is still accessible using the drop-down menu if you need to search for more solutions.</span></span> 
 
7. <span data-ttu-id="4850e-124">基本連絡先情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="4850e-124">Enter the primary contact information.</span></span> <span data-ttu-id="4850e-125">これらの連絡先の詳細は、カスタマー サポート チームがケースについて連絡するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="4850e-125">These contact details will be used by the customer support team to contact you about the case.</span></span>

8. <span data-ttu-id="4850e-126">サポート契約と重要度レベルを選択します。</span><span class="sxs-lookup"><span data-stu-id="4850e-126">Select the support contract and the severity level.</span></span> 
    
   - <span data-ttu-id="4850e-127">オンプレミス環境のサポート契約では、インシデント数に制限があります。</span><span class="sxs-lookup"><span data-stu-id="4850e-127">Support contracts for on-premises environments have a limited incident count.</span></span> 
   - <span data-ttu-id="4850e-128">クラウド環境のサポート契約では、インシデント数が無制限です。</span><span class="sxs-lookup"><span data-stu-id="4850e-128">Support contracts for cloud environments have an unlimited incident count.</span></span> 
   - <span data-ttu-id="4850e-129">オンプレミス製品またはクラウド環境では、使用可能なサポート契約の一覧から、複数層のサポート契約がある場合に使用するサポート オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="4850e-129">For on-premises products or cloud environments, from the list of available support contracts, select the support option to use if you have multiple tier support contracts.</span></span> 
  
9. <span data-ttu-id="4850e-130">**送信** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4850e-130">Click **Submit**.</span></span> 

<span data-ttu-id="4850e-131">**送信**をクリックした後、インシデントが作成され**インシデント** リストに追加されます。</span><span class="sxs-lookup"><span data-stu-id="4850e-131">After you click **Submit**, an incident is created and added to the **Incidents** list.</span></span> <span data-ttu-id="4850e-132">このケースに割り当てられている Microsoft サポート エンジニアから、電子メール メッセージを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="4850e-132">You will receive an email message from the Microsoft Support Engineer assigned to your case.</span></span> 


## <a name="support-plans-in-lifecycle-services"></a><span data-ttu-id="4850e-133">Lifecycle Servicesにおけるサポートプラン</span><span class="sxs-lookup"><span data-stu-id="4850e-133">Support plans in Lifecycle Services</span></span>
<span data-ttu-id="4850e-134">サポートプランのエンタイトルメントは、さまざまな識別子に基づき提供されます。</span><span class="sxs-lookup"><span data-stu-id="4850e-134">Support plan entitlements are derived based on several different identifiers.</span></span> <span data-ttu-id="4850e-135">すべてが適用されるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="4850e-135">Not all will apply to your situation.</span></span> <span data-ttu-id="4850e-136">サポートプランまたはLCSでエンタイトルメントが見つからない場合は、LCSのプロジェクトでどのような識別子が関連付けられるべきかを決定することになります。</span><span class="sxs-lookup"><span data-stu-id="4850e-136">If you are missing a support plan or entitlement in LCS, determine which identifier is needed to tie it to your project in LCS.</span></span> <span data-ttu-id="4850e-137">複数の組織がある場合は、LCSの右上の名称をクリックすることで現行のものを示してください。</span><span class="sxs-lookup"><span data-stu-id="4850e-137">If there is more than one organization, note which one is current by clicking on your name in the upper-right corner of LCS.</span></span> <span data-ttu-id="4850e-138">シナリオに適合し、利用したいベネフィットを含む組織を選択して下さい。</span><span class="sxs-lookup"><span data-stu-id="4850e-138">Select the organization that applies to your scenario and contains the benefits that you want to utilize.</span></span>

### <a name="unique-contract-idaccess-id"></a><span data-ttu-id="4850e-139">契約者固有ID/固有アクセスID</span><span class="sxs-lookup"><span data-stu-id="4850e-139">Unique contract ID/access ID</span></span>
<span data-ttu-id="4850e-140">次のオンライン サポートプランでは、LCSでのサインインと関連付けられた契約者固有ID/固有アクセスIDが必要です。</span><span class="sxs-lookup"><span data-stu-id="4850e-140">The following online support plans require a unique contract ID/access ID combination linked to your sign-in in LCS:</span></span>

-   <span data-ttu-id="4850e-141">統合サポート</span><span class="sxs-lookup"><span data-stu-id="4850e-141">Unified</span></span>
-   <span data-ttu-id="4850e-142">プレミア</span><span class="sxs-lookup"><span data-stu-id="4850e-142">Premier</span></span>
-   <span data-ttu-id="4850e-143">パートナー様向け Advanced サポート</span><span class="sxs-lookup"><span data-stu-id="4850e-143">Advanced support for partners</span></span>

<span data-ttu-id="4850e-144">契約者固有ID/固有アクセスIDの組み合わせがわからない場合は、マイクロソフトの顧客担当者に問い合わせの上IDの再作成をご依頼ください。</span><span class="sxs-lookup"><span data-stu-id="4850e-144">If you do not know your unique contract ID/access ID combination, contact your Microsoft account manager to have an ID created for you.</span></span>

<span data-ttu-id="4850e-145">アカウントと契約社ID/アクセスIDを関連付けるには、次の手順を完了してください</span><span class="sxs-lookup"><span data-stu-id="4850e-145">To link your contract ID/access ID to your account, complete the following steps:</span></span>

1. <span data-ttu-id="4850e-146">プロジェクト内から選択 **サポート** し、メイン メニューなどの選択から **管理サポート プラン** します。</span><span class="sxs-lookup"><span data-stu-id="4850e-146">From within a project, select **Support** from the main menu, and then select **Manage Support plans**.</span></span> 
2. <span data-ttu-id="4850e-147">**契約の追加** を選択します</span><span class="sxs-lookup"><span data-stu-id="4850e-147">Select **Add contract**.</span></span>

   ![契約の追加](media/56c7bfd469f6d850d456e9e7a89e0d8d.png)

3. <span data-ttu-id="4850e-149">アクセスIDと、パスワードまたは契約IDを入力し、 **契約の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4850e-149">Enter your access ID and your password or contract ID, and then select **Add contract**.</span></span>

   ![契約の資格情報の追加](media/4abba1127549ef484a58daf51609d924.png)

### <a name="partnersource-business-center-account"></a><span data-ttu-id="4850e-151">PartnerSource Business Center アカウント</span><span class="sxs-lookup"><span data-stu-id="4850e-151">PartnerSource Business Center account</span></span>
<span data-ttu-id="4850e-152">利用可能な場合は、次のサポートプランインシデントがPartnerSource業務部門 (PSBC) アカウントの一部として使用できます。</span><span class="sxs-lookup"><span data-stu-id="4850e-152">The following support plan incidents can be used as part of your PartnerSource Business Center (PSBC) account if they exist:</span></span> 

> [!NOTE]
> <span data-ttu-id="4850e-153">PSBCアカウントではオンライン サポートプランはご利用できません。</span><span class="sxs-lookup"><span data-stu-id="4850e-153">No online support plans can be utilized through the PSBC account.</span></span>

-   <span data-ttu-id="4850e-154">顧客向け オンプレミス インシデントの高度なサポート</span><span class="sxs-lookup"><span data-stu-id="4850e-154">Advanced support for partners on-premises incidents.</span></span>
-   <span data-ttu-id="4850e-155">優先 または 優先 + オンプレミスインシデント</span><span class="sxs-lookup"><span data-stu-id="4850e-155">Advantage or Advantage + on-premises incidents.</span></span>
-   <span data-ttu-id="4850e-156">既存のインシデントタイプのプランごとの支払いについては、PSBCに算出されます。</span><span class="sxs-lookup"><span data-stu-id="4850e-156">Other pay per incident types of plans with an existing incident count in PSBC.</span></span>

<span data-ttu-id="4850e-157">PartnerSourceビジネス センター アカウントが見つからない場合は、PSBCの組織でサインインがプロフェッショナルとして追加されているか確認してください。</span><span class="sxs-lookup"><span data-stu-id="4850e-157">If you do not find the PartnerSource Business Center account, ensure that your sign in is added as a professional in your organization in PSBC.</span></span> <span data-ttu-id="4850e-158">同一のMicrosoftアカウントまたは職場アカウントを使用してログインしていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4850e-158">Make sure that you are signing in with the same Microsoft or work account login.</span></span> <span data-ttu-id="4850e-159">このアカウントは、オンプレミスプロジェクトにのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="4850e-159">This account is only applicable in an on-premises project.</span></span>

![契約の追加](media/56c7bfd469f6d850d456e9e7a89e0d8d.png)

### <a name="sign-in-specfic-options"></a><span data-ttu-id="4850e-161">サインイン 特定のオプション</span><span class="sxs-lookup"><span data-stu-id="4850e-161">Sign-in specfic options</span></span>
<span data-ttu-id="4850e-162">該当するものがある場合、ログインのアカウントに基づき次の問題とサポートの特典が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4850e-162">The following incidents and support benefits will appear based on your sign in, if applicable:</span></span>

-   <span data-ttu-id="4850e-163">MPN gold および シルバー インシデント</span><span class="sxs-lookup"><span data-stu-id="4850e-163">MPN gold and silver incidents.</span></span>
-   <span data-ttu-id="4850e-164">シグネイチャークラウドサポート</span><span class="sxs-lookup"><span data-stu-id="4850e-164">Signature cloud support.</span></span>
-   <span data-ttu-id="4850e-165">個々のインシデントと [support.microsoft.com/supportforbusiness] で購入した5パック</span><span class="sxs-lookup"><span data-stu-id="4850e-165">Individual incidents and 5 packs purchased on [support.microsoft.com/supportforbusiness].</span></span> 

   > [!NOTE]
   > <span data-ttu-id="4850e-166">インシデントはMicrosoftアカウントを使用して購入する必要があります。 Microsoftアカウントは \@hotmail.com または \@outlook.com のような形式です。</span><span class="sxs-lookup"><span data-stu-id="4850e-166">Incidents must be purchased with a Microsoft account such as \@hotmail.com or \@outlook.com.</span></span> <span data-ttu-id="4850e-167">作業アカウントまたは Azure Active Directory アカウントは、それぞれに関連付けられているインシデントを持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="4850e-167">Work or Azure Active Directory accounts cannot have incidents tied to them.</span></span>

### <a name="tenant-subscription"></a><span data-ttu-id="4850e-168">テナントサブスクリプション</span><span class="sxs-lookup"><span data-stu-id="4850e-168">Tenant subscription</span></span>
<span data-ttu-id="4850e-169">次のエンタイトルメントが、サブスクリプションおよびテナント組織内でのProDirect購入に基づいて表示されます。</span><span class="sxs-lookup"><span data-stu-id="4850e-169">The following entitlements will appear based on your subscription and ProDirect purchases within your tenant organization:</span></span>

-   <span data-ttu-id="4850e-170">定期売買</span><span class="sxs-lookup"><span data-stu-id="4850e-170">Subscription</span></span>
-   <span data-ttu-id="4850e-171">ProDirect</span><span class="sxs-lookup"><span data-stu-id="4850e-171">ProDirect</span></span>

### <a name="software-assurance"></a><span data-ttu-id="4850e-172">ソフトウェア保証</span><span class="sxs-lookup"><span data-stu-id="4850e-172">Software assurance</span></span>
<span data-ttu-id="4850e-173">次のエンタイトルメントは、定期売買番号および連絡先電子メール アドレスを連携させることで追加可能です。</span><span class="sxs-lookup"><span data-stu-id="4850e-173">The following entitlements can be added by linking a subscription number and contact email:</span></span>

-   <span data-ttu-id="4850e-174">ソフトウェア保証</span><span class="sxs-lookup"><span data-stu-id="4850e-174">Software assurance</span></span>

<span data-ttu-id="4850e-175">サポート インシデントを作成する際に **ソフトウェア保証プラン追加** することで追加します。</span><span class="sxs-lookup"><span data-stu-id="4850e-175">To add, select **Add a Software Assurance plan** when you create the support incident.</span></span> <span data-ttu-id="4850e-176">定期売買番号および連絡先の電子メールを入力し、 **続行します** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4850e-176">Enter the subscription number and the contact email, and then click **Continue**.</span></span>

![ソフトウェア保証プラン](media/cd8f65a32c30722ea687dfbc5cc30874.png)
   
## <a name="report-production-outage"></a><span data-ttu-id="4850e-178">稼働停止のレポート</span><span class="sxs-lookup"><span data-stu-id="4850e-178">Report production outage</span></span>
<span data-ttu-id="4850e-179">プロダクション環境の品質が低下または使用不可能になった際に、Microsoft サポートに迅速に問題を効果的にエスカレーションするには、 [稼働停止をレポート](report-production-outage.md) をご確認ください。</span><span class="sxs-lookup"><span data-stu-id="4850e-179">For a quick and effective way to escalate issues to Microsoft Support in the event that the services in a production environment are degraded or become unavailable, see [Report a production outage](report-production-outage.md).</span></span>

## <a name="phone-support"></a><span data-ttu-id="4850e-180">電話サポート</span><span class="sxs-lookup"><span data-stu-id="4850e-180">Phone support</span></span>
<span data-ttu-id="4850e-181">[新しいインシデントを開く](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/cloud-powered-support-lcs#open-a-new-incident) の手順に従ってサポートに連絡することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="4850e-181">We prefer that you contact Support following the steps in [Open a new incident](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/cloud-powered-support-lcs#open-a-new-incident).</span></span> <span data-ttu-id="4850e-182">LCS で新しいインシデントを開けない場合は、次のいずれかのオプションで電話サポートを受けることができます:</span><span class="sxs-lookup"><span data-stu-id="4850e-182">If you're unable to open a new incident in LCS, phone support is available using one of the following options:</span></span>

- [<span data-ttu-id="4850e-183">プレミア電話サポート</span><span class="sxs-lookup"><span data-stu-id="4850e-183">Premier phone support</span></span>](https://support.microsoft.com/premier/contacts)
- [<span data-ttu-id="4850e-184">広範な商業電話サポート</span><span class="sxs-lookup"><span data-stu-id="4850e-184">Broad commercial phone support</span></span>](https://mbs.microsoft.com/customersource/northamerica/GP/support/support-news/global_support_contacts_eng)
