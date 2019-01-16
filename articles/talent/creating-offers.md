---
title: "オファーの作成、承認、および署名"
description: "このトピックでは、Dynamics 365 for Talent を使用して候補者へのオファーを作成、承認、および署名する方法について説明します。"
author: josaw
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-10-19
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: be66d9f95551066bb8bc25445c652d4fa59066d4
ms.openlocfilehash: f189df052ef299a2cca1d92065a7a4d377d25399
ms.contentlocale: ja-jp
ms.lasthandoff: 12/07/2018

---

# <a name="creating-approving-and-signing-offers"></a><span data-ttu-id="cd374-103">オファーの作成、承認、および署名</span><span class="sxs-lookup"><span data-stu-id="cd374-103">Creating, approving, and signing offers</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cd374-104">多くの場合、候補者へのオファー パッケージの準備は迅速なプロセスである必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd374-104">In many cases, preparing an offer package for a candidate needs to be a very quick process.</span></span>
<span data-ttu-id="cd374-105">Attract 管理者により設定されたテンプレートを使用して、オファー作成者は候補者にオファーを準備および送信するための時間と労力を短縮できます。</span><span class="sxs-lookup"><span data-stu-id="cd374-105">Using the templates set up by the Attract administrator will cut down the time and effort for the offer creators to prepare and send offers to a candidate.</span></span>

## <a name="create-an-offer"></a><span data-ttu-id="cd374-106">オファーの作成</span><span class="sxs-lookup"><span data-stu-id="cd374-106">Create an offer</span></span>

<span data-ttu-id="cd374-107">オファー管理アプリをオンにすると、採用マネージャーまたは採用担当者のロールを持つ任意ユーザーは、候補者へのオファー パッケージを準備できます。</span><span class="sxs-lookup"><span data-stu-id="cd374-107">When the Offer management app is turned on, any user with the role of hiring manager or recruiter can prepare an offer package for the candidate.</span></span> <span data-ttu-id="cd374-108">オファーを準備するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="cd374-108">To prepare the offer, do the following.</span></span>

1.  <span data-ttu-id="cd374-109">オファーの作成先であるジョブ求人および候補者申請に移動します。</span><span class="sxs-lookup"><span data-stu-id="cd374-109">Navigate to the job and the candidate application that you are creating the offer for.</span></span>

1.  <span data-ttu-id="cd374-110">**オファー ステージ**に移動し、**オファーの準備**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cd374-110">Go to **Offer stage** and click **Prepare offer**.</span></span>

    <span data-ttu-id="cd374-111">候補者の**新規**のステータスを表示できるよう、オファー アプリにリダイレクトされます。</span><span class="sxs-lookup"><span data-stu-id="cd374-111">You will be redirected to the Offer app where you can see the candidate with the status of **New**.</span></span> <span data-ttu-id="cd374-112">作成者または承認者のいずれかとして関与している他のオファーを表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="cd374-112">You can also see other offers that you are contributing to, either as a creator or an approver.</span></span>

1.  <span data-ttu-id="cd374-113">**オファーの準備**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cd374-113">Click **Prepare Offer**.</span></span> 
    
    <span data-ttu-id="cd374-114">管理者により使用可能になった別のオファー パッケージの選択肢が表示されます。</span><span class="sxs-lookup"><span data-stu-id="cd374-114">You will see a choice of different offer packages that have been made available by the administrator.</span></span>

1.  <span data-ttu-id="cd374-115">パッケージを選択し**完了**をクリックして、オファーの準備を開始します。</span><span class="sxs-lookup"><span data-stu-id="cd374-115">Select a package and click **Done** to start preparing the offer.</span></span>

    <span data-ttu-id="cd374-116">オファー パッケージ テンプレートには、対応するジョブおよびオファーで入力された候補者の詳細が読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="cd374-116">The offer package template loads with the corresponding job and candidate details populated in the offer.</span></span>

1.  <span data-ttu-id="cd374-117">オファー パッケージの一部であるすべてのオファー データ プレースホルダーは、ランディング ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="cd374-117">All the offer data placeholders that are part of the offer package are visible in the landing page.</span></span> <span data-ttu-id="cd374-118">このページでは、パッケージ間ですべての値を設定できます。</span><span class="sxs-lookup"><span data-stu-id="cd374-118">You can populate all the values across the package on this page.</span></span>

    <span data-ttu-id="cd374-119">ランディング ページで、オファー パッケージの一部であるすべてのオファー ドキュメント テンプレートも表示できます。</span><span class="sxs-lookup"><span data-stu-id="cd374-119">On the landing page, you can also see all the offer document templates that are part of the offer package.</span></span>

1.  <span data-ttu-id="cd374-120">これにより管理者によってテンプレートが構成される方法に応じて、オファーのコンテンツを編集できる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="cd374-120">You may now be able to edit the content of the offer, depending on how the template was configured by the administrator.</span></span>

1.  <span data-ttu-id="cd374-121">必須ではないとマークされているドキュメントを削除する必要がある場合、削除できます。</span><span class="sxs-lookup"><span data-stu-id="cd374-121">If you need to remove documents marked as non-required, you can do so.</span></span>

1. <span data-ttu-id="cd374-122">すべてのオファー データ プレース ホルダーが設定されている場合、**保存**をクリックしてオファーのドラフトを保存します。</span><span class="sxs-lookup"><span data-stu-id="cd374-122">When all the offer data placeholders are populated, click **Save** to save a draft of the offer.</span></span>

>[!NOTE]
> <span data-ttu-id="cd374-123">ドラフトを保存した後、必要に応じて、オファーのドラフト バージョンを削除または新しいパッケージ テンプレートを選択できます。</span><span class="sxs-lookup"><span data-stu-id="cd374-123">After a draft is saved, you can delete the draft version of the offer or select a new package template, if necessary.</span></span>


## <a name="approve-an-offer"></a><span data-ttu-id="cd374-124">オファーの承認</span><span class="sxs-lookup"><span data-stu-id="cd374-124">Approve an offer</span></span>

<span data-ttu-id="cd374-125">ほとんどのオファーは、オファーが必要な基準を満たしているかどうかを確認する承認プロセスを経由する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd374-125">Most offers need to go through an approval process to make sure the offer meets the necessary standards.</span></span> <span data-ttu-id="cd374-126">オファーが基準を満たしていない場合、たとえばオファー作成者がオファー データ ルールに従わなかったかオファーの値を上書きした場合、承認プロセスが必須になります。</span><span class="sxs-lookup"><span data-stu-id="cd374-126">If an offer does not meet standards, for example if the offer creator didn't follow the offer data rules and overrode the values in the offer, the approval process will be mandated.</span></span> <span data-ttu-id="cd374-127">承認用にオファーを送信するには、次の操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="cd374-127">To send an offer for approval, do the following.</span></span>

1.  <span data-ttu-id="cd374-128">オファーがドラフト状態である場合、**承認者パネル**で承認者を追加します。</span><span class="sxs-lookup"><span data-stu-id="cd374-128">When the offer is in a draft state, add approvers on the **Approver panel**.</span></span> 
    >[!NOTE]
    > <span data-ttu-id="cd374-129">既定では、採用マネージャーが承認者として追加されます。</span><span class="sxs-lookup"><span data-stu-id="cd374-129">Hiring Managers are added as approver by default.</span></span> <span data-ttu-id="cd374-130">オファーの承認者として、組織内から任意のユーザーを選択できます。</span><span class="sxs-lookup"><span data-stu-id="cd374-130">You can choose any user from your organization as an approver for the offer.</span></span>

1.  <span data-ttu-id="cd374-131">必要に応じて、順次承認メソッドまたは同時承認メソッドで承認者を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="cd374-131">If needed, assign approvers in a sequential approval method or on a parallel approval method.</span></span> <span data-ttu-id="cd374-132">このオプションは、管理者によってそのように構成されていた場合にのみ使用可能です。</span><span class="sxs-lookup"><span data-stu-id="cd374-132">This option will only be available if it was configured as such by the administrator.</span></span>
    >[!NOTE]
    > <span data-ttu-id="cd374-133">承認プロセスが連続している場合は、必要に応じて承認者の順序を編集できます。</span><span class="sxs-lookup"><span data-stu-id="cd374-133">If the approval process is sequential, you can edit the sequence of approvers if needed.</span></span>

1.  <span data-ttu-id="cd374-134">承認チェーンの定義を行う場合、承認電子メールのコンテンツを編集して、承認者に通知を送信できます。</span><span class="sxs-lookup"><span data-stu-id="cd374-134">When you are done defining the approval chain, you can edit the content of the approval email and then send the notification to the approvers.</span></span> <span data-ttu-id="cd374-135">**承認者に送信**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cd374-135">Click **Send to approvers**.</span></span>
    >[!NOTE]
    > <span data-ttu-id="cd374-136">オファーが非標準であった場合、妥当性を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd374-136">If the offer was non-standard, you are required to provide a justification.</span></span>

1.  <span data-ttu-id="cd374-137">オファー作成者が承認者のスキップを選択する場合は、注記を入力し次の承認者に進むことができます。</span><span class="sxs-lookup"><span data-stu-id="cd374-137">If the offer creator chooses to skip an approver, they can enter a note and skip to the next approver.</span></span>

<span data-ttu-id="cd374-138">承認者は、そのオファーを承認するよう求める電子メールを受信します。</span><span class="sxs-lookup"><span data-stu-id="cd374-138">Approvers will receive an email asking them to approve the offer.</span></span> <span data-ttu-id="cd374-139">電子メールでリンクをクリックしてオファーを開き、オファー パッケージ全体を確認し、それを承認するかまたはオファー作成者に返送できます。</span><span class="sxs-lookup"><span data-stu-id="cd374-139">They can click the link in the email to open the offer, review the entire offer package, and either approve it or send it back to the offer creator.</span></span> <span data-ttu-id="cd374-140">詳細な編集のオファー パッケージを拒否している場合は、オファー承認者がさらに注記を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd374-140">Offer approvers will need to add an additional note if they are rejecting the offer package for further edits.</span></span> 

<span data-ttu-id="cd374-141">承認者が実行する前に作成されたオファーの新しいバージョンがある場合、承認者はオファーを承認または拒否することはできません。</span><span class="sxs-lookup"><span data-stu-id="cd374-141">In cases where there is a new version of the offer created before the approver acts, the approver won’t be able to approve or reject the offer.</span></span>

## <a name="offer-versioning"></a><span data-ttu-id="cd374-142">オファーのバージョン管理</span><span class="sxs-lookup"><span data-stu-id="cd374-142">Offer versioning</span></span> 

<span data-ttu-id="cd374-143">オファーが承認されまたは詳細な編集用に返送された場合、**編集の有効化**オプションを選択してオファーの新しいバージョンを作成できます。</span><span class="sxs-lookup"><span data-stu-id="cd374-143">When the offer has been approved or sent back for further edits, you can choose the **Enable editing** option to create a new version of the offer.</span></span> <span data-ttu-id="cd374-144">オファー バージョンの新しいバージョンには、すべてのオファー データ値および最終バージョンから繰り越された承認者の一覧があります。</span><span class="sxs-lookup"><span data-stu-id="cd374-144">The new version of the offer version has all the offer data values and the list of approvers carried over from the last version.</span></span> 

<span data-ttu-id="cd374-145">バージョンが承認用に共有された場合、承認者は別のオファー バージョン間での切り替えができます。</span><span class="sxs-lookup"><span data-stu-id="cd374-145">Approvers can switch between different offer versions if the versions were shared with them for approval.</span></span> <span data-ttu-id="cd374-146">また、承認者またはオファー作成者は、前の状態に戻すため特定のドラフト オファー バージョンを削除する選択ができます。</span><span class="sxs-lookup"><span data-stu-id="cd374-146">Also, an approver or offer creator can choose to delete a specific draft offer version to go back to the previous state.</span></span>


## <a name="send-an-offer-to-a-candidate"></a><span data-ttu-id="cd374-147">候補者にオファーを送信</span><span class="sxs-lookup"><span data-stu-id="cd374-147">Send an offer to a candidate</span></span> 

<span data-ttu-id="cd374-148">オファーが保存され、承認され、および候補者に送信する準備ができたら、**候補者に送信**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cd374-148">When the offer is saved, approved, and ready to be sent to the candidate, click **Send to candidate**.</span></span>

<span data-ttu-id="cd374-149">候補者にオファーを送信する前に、実行できるいくつかの操作があります。</span><span class="sxs-lookup"><span data-stu-id="cd374-149">There are several actions you can take before sending the offer to the candidate.</span></span>
-  <span data-ttu-id="cd374-150">候補者に送信されるオファー パッケージの一部であるドキュメントの一覧を表示できます。</span><span class="sxs-lookup"><span data-stu-id="cd374-150">You can view the list of documents that are part of the offer package that will be sent to the candidate.</span></span>

-  <span data-ttu-id="cd374-151">オファーの有効期限を指定できます。</span><span class="sxs-lookup"><span data-stu-id="cd374-151">You can specify an offer expiration date.</span></span> <span data-ttu-id="cd374-152">候補者には、有効期限前にオファーを承諾または拒否することが求められます。</span><span class="sxs-lookup"><span data-stu-id="cd374-152">Candidates are expected to accept or decline the offer before the expiration date.</span></span>  <span data-ttu-id="cd374-153">候補者には、オファーの期限が切れる 48 時間前にアラームが送信されます。</span><span class="sxs-lookup"><span data-stu-id="cd374-153">The candidate will be sent a reminder 48 hours before the offer expires.</span></span>

-  <span data-ttu-id="cd374-154">オファーの承諾プロセスに含める追加のドキュメントがある場合があります。</span><span class="sxs-lookup"><span data-stu-id="cd374-154">There may be additional documents that you want to include in the offer acceptance process.</span></span> <span data-ttu-id="cd374-155">必要なドキュメント タイプを一覧表示するオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="cd374-155">You will have the option to list the document type required.</span></span>

- <span data-ttu-id="cd374-156">電子署名のオプション: Adobe Sign が電子署名の優先メソッドとして選択されている場合は、オファー作成者は、Adobe Sign ライセンスを接続する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd374-156">e-Signature option: If Adobe Sign was chosen as the preferred e-sign method, offer creators need to connect their Adobe Sign license.</span></span> <span data-ttu-id="cd374-157">これを行うには 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="cd374-157">There are two ways to do this.</span></span> <span data-ttu-id="cd374-158">**Adobe Sign** に接続する**接続**の、**オファー**のユーザー**設定**に移動します。</span><span class="sxs-lookup"><span data-stu-id="cd374-158">Go to User **Settings** in **Offer**, under **Connections** connect to **Adobe Sign**.</span></span> <span data-ttu-id="cd374-159">または、ユーザー設定に基づいて接続がまだ確立されていない場合は、オファーの送信を候補者画面に接続するように求められます。</span><span class="sxs-lookup"><span data-stu-id="cd374-159">Alternatively, you will be asked to connect the Send offer to the candidate screen if the connection wasn't already established based on the user settings.</span></span> 

> [!NOTE]
> <span data-ttu-id="cd374-160">ユーザーは、Adobe Sign アカウントを 1 回だけ接続する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd374-160">Users only need to connect their Adobe Sign accounts once.</span></span> <span data-ttu-id="cd374-161">同じユーザーによって送信される今後のすべてのオファー パッケージには、同じユーザー ライセンスが使用されます。</span><span class="sxs-lookup"><span data-stu-id="cd374-161">The same user license is used for all future offer packages that will be sent out by the same user.</span></span> 

-  <span data-ttu-id="cd374-162">必要に応じて、電子メール テンプレートを表示および編集できます。</span><span class="sxs-lookup"><span data-stu-id="cd374-162">You can view and edit the email template as needed.</span></span>

<span data-ttu-id="cd374-163">オファーの準備ができ**候補者に送信**をクリックすると、候補者はオファーの確認が必要であるという電子メールを受信します。</span><span class="sxs-lookup"><span data-stu-id="cd374-163">When the offer is ready and you click **Send to candidate**, the candidate will receive an email that an offer is waiting for review.</span></span>


## <a name="candidates-actions-after-receiving-an-offer"></a><span data-ttu-id="cd374-164">オファーを受け取った後の候補者のアクション</span><span class="sxs-lookup"><span data-stu-id="cd374-164">Candidate’s actions after receiving an offer</span></span>

<span data-ttu-id="cd374-165">候補者にオファーが共有されたと通知された後、その電子メール内でリンクをクリックして申請ダッシュボードに移動しオファーを表示できます。</span><span class="sxs-lookup"><span data-stu-id="cd374-165">After the candidate has been notified that an offer has been shared with them, they can click the link in their email to go to the application dashboard and view the offer.</span></span> <span data-ttu-id="cd374-166">ダッシュボードには、候補者がまだ完了する必要のある任意のアクティビティが表示されます。</span><span class="sxs-lookup"><span data-stu-id="cd374-166">The dashboard will show the candidate any activities that they still need to complete.</span></span>

1.  <span data-ttu-id="cd374-167">オファーと関連するすべてのドキュメントを表示するには、候補者は**オファーを表示**をクリックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd374-167">To view the offer and all related documents, the candidate must click **View offer**.</span></span>

    <span data-ttu-id="cd374-168">候補者はオファー パッケージを .zip 形式でダウンロードもできます。</span><span class="sxs-lookup"><span data-stu-id="cd374-168">Candidates can also download the offer package in a .zip format.</span></span>

1.  <span data-ttu-id="cd374-169">オファーを承諾するには、候補者はオファー パッケージの一部である各ドキュメントの**署名にジャンプする**をクリックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd374-169">To accept the offer, the candidates must click **Jump to signature** for each document that’s part of the offer package.</span></span>

1.  <span data-ttu-id="cd374-170">すべてのドキュメントが個別に署名され承諾された時点で、候補者はページの上部にある**オファーの承諾**をクリックして、承諾プロセスを完了するための選択をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd374-170">When all of the documents have been individually signed and accepted, the candidate must choose to finish the acceptance process by clicking **Accept Offer** at the top of the page.</span></span>

1.  <span data-ttu-id="cd374-171">オファーを辞退するには、候補者はページの上部にある**オファーを辞退**をクリックし、該当する理由を選択し、必要に応じてコメントを追加してから、**辞退**をクリックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd374-171">To decline the offer, the candidate must click **Decline the offer** on the top of the page, select an appropriate reason, add a comment as necessary, and then click **Decline**.</span></span>

1.  <span data-ttu-id="cd374-172">オファーを承認または辞退した後、候補者はオファーの一覧内にとどまるか、または申請ダッシュボードに戻るかを続行できます。</span><span class="sxs-lookup"><span data-stu-id="cd374-172">After they have accepted or declined the offer, the candidate can continue to stay in the offer view or go back to the application dashboard.</span></span>

1.  <span data-ttu-id="cd374-173">オファー承諾プロセスの一部として要求されるその他のドキュメントがある場合、必要に応じて、候補者はドキュメントをアップロードする選択をし、要求されたドキュメント タイプにタグ付けする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd374-173">If there were other documents requested as part of the offer acceptance process, the candidate should choose to upload the documents as necessary and tag them to the document type requested.</span></span>

1.  <span data-ttu-id="cd374-174">オファー作成者は、すべてのドキュメントがアップロードされ、オファー パッケージが署名された時点で通知されます。</span><span class="sxs-lookup"><span data-stu-id="cd374-174">The offer creator will be notified when all the documents have been uploaded and the offer package has been signed.</span></span>


## <a name="withdrawing-an-offer"></a><span data-ttu-id="cd374-175">オファーの取消</span><span class="sxs-lookup"><span data-stu-id="cd374-175">Withdrawing an offer</span></span>

<span data-ttu-id="cd374-176">オファーは、任意の時点でさまざまな理由で、候補者により取り消されます。</span><span class="sxs-lookup"><span data-stu-id="cd374-176">An offer can be withdrawn from a candidate at any point in time for various reasons.</span></span> 
1.  <span data-ttu-id="cd374-177">省略記号ボタン (**…**) をクリックしてオファーを取り消し、**オファーの取り消し**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cd374-177">Withdraw the offer by clicking the ellipsis button (**…**), and then click **Withdraw the offer**.</span></span> 

2. <span data-ttu-id="cd374-178">候補者がステータスの変更に関して連絡を受けたかどうかを確認するメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="cd374-178">A message will appear asking whether the candidate has been contacted about the change in status.</span></span> <span data-ttu-id="cd374-179">候補者がまだ連絡を受けていない場合は、候補者にさらなるアクションを通知する電子メールを送信するオプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="cd374-179">If the candidate hasn't been contacted yet, you will have the option to send an email to the candidate informing them of further actions.</span></span> 

   <span data-ttu-id="cd374-180">オファーは候補者によりアクセスできなくなります。</span><span class="sxs-lookup"><span data-stu-id="cd374-180">The offer will no longer accessible by the candidate.</span></span>


## <a name="closing-an-offer"></a><span data-ttu-id="cd374-181">オファーの終了</span><span class="sxs-lookup"><span data-stu-id="cd374-181">Closing an offer</span></span> 

<span data-ttu-id="cd374-182">オファーが承諾され、辞退され、またはさらなるアクションの必要もなく取り消された場合、オファーを終了してこのオファー パッケージがそれ以上変更されないようにできます。</span><span class="sxs-lookup"><span data-stu-id="cd374-182">When an offer has been accepted, declined, or withdrawn with no further actions needed, you can close the offer so that no further edits can be made to this offer package.</span></span>

