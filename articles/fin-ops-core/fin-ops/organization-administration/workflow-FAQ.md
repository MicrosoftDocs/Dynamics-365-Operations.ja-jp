---
title: ワークフローに関するよく寄せられる質問
description: このトピックでは、ワークフロー システムについてよく寄せられる質問に回答します。
author: ChrisGarty
manager: AnnBe
ms.date: 09/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 58aa4a6d313a78e88c2858637d6de167895ec534
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797394"
---
# <a name="workflow-faq"></a><span data-ttu-id="db80f-103">ワークフローに関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="db80f-103">Workflow FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="db80f-104">このトピックでは、ワークフロー システムについてよく寄せられる質問に回答します。</span><span class="sxs-lookup"><span data-stu-id="db80f-104">This topic answers frequently asked questions about the workflow system.</span></span>

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="db80f-105">作業項目が否認された場合に複数の通知が受信されるのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="db80f-105">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="db80f-106">作業項目が否認されると、その作業項目は否認済として完了します。</span><span class="sxs-lookup"><span data-stu-id="db80f-106">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="db80f-107">別の作業項目が作成され、作成者に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="db80f-107">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="db80f-108">これは、否認された作業項目に関する発信者への通知と、新しい「変更要求済」の作業項目に割り当てられたユーザーへの個別の通知があることを意味します。</span><span class="sxs-lookup"><span data-stu-id="db80f-108">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="db80f-109">各通知は異なる作業項目に対するものですが、類似性により混乱が生じる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="db80f-109">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="db80f-110">将来のリリースでこれを改善する方法を検討しています。</span><span class="sxs-lookup"><span data-stu-id="db80f-110">We are looking at ways to improve this in a future release.</span></span>

## <a name="why-are-my-workflow-exports-failing"></a><span data-ttu-id="db80f-111">ワークフローのエクスポートが失敗するのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="db80f-111">Why are my workflow exports failing?</span></span>
<span data-ttu-id="db80f-112">現在、ワークフローのエクスポート機能には、ワークフロー名が 48 文字を超えないようにする制限があります。</span><span class="sxs-lookup"><span data-stu-id="db80f-112">There is currently a limitation in the workflow export feature that prevents workflow names from exceeding 48 characters.</span></span> <span data-ttu-id="db80f-113">48 文字を超える名前を使用すると、「サーバーは要求の認証に失敗しました」というエラーが発生するか、またはファイルがファイル タイプなしでエクスポートされるのを防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="db80f-113">Using a name that is longer than 48 characters can result in a "Server failed to authenticate the request" error and/or prevent a file to be exported  without a file type.</span></span> <span data-ttu-id="db80f-114">詳細については、次のブログ記事を参照してください [ワークフローのエクスポートに関するトラブルシューティング](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting)。</span><span class="sxs-lookup"><span data-stu-id="db80f-114">The following blog post provides more details, [Workflow export troubleshooting](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span></span>

## <a name="can-the-submitter-of-a-workflow-also-approve-the-workflow"></a><span data-ttu-id="db80f-115">ワークフローの送信者はワークフローを承認することもできますか。</span><span class="sxs-lookup"><span data-stu-id="db80f-115">Can the submitter of a workflow also approve the workflow?</span></span>
<span data-ttu-id="db80f-116">はい、そのように構成されている場合、ワークフローの送信者は、ワークフローを承認することもできます。</span><span class="sxs-lookup"><span data-stu-id="db80f-116">Yes, a submitter of a workflow can also approve the workflow if it is configured that way.</span></span> <span data-ttu-id="db80f-117">この動作を回避するには、**システム管理 > ワークフロー > ワークフロー パラメーター > 一般 > 承認者 > 送信者による承認を許可しない** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="db80f-117">To prevent this behavior, set **System administration > Workflow > Workflow parameters > General > Approver > Disallow approval by submitter** to **Yes**.</span></span>

## <a name="can-i-add-alerts-to-workflows-to-provide-notifications-to-users"></a><span data-ttu-id="db80f-118">ユーザーに通知を行うためにワークフローに警告を追加することはできますか?</span><span class="sxs-lookup"><span data-stu-id="db80f-118">Can I add alerts to workflows to provide notifications to users?</span></span>
<span data-ttu-id="db80f-119">通知を行うワークフローへの警告の追加に関する注意事項の重要な領域を次に示します。</span><span class="sxs-lookup"><span data-stu-id="db80f-119">Here are a few key areas to note about adding alerts to workflows to provide notifications:</span></span>
- <span data-ttu-id="db80f-120">警告とワークフロー通知のメカニズム</span><span class="sxs-lookup"><span data-stu-id="db80f-120">Alerts versus workflow notification mechanisms</span></span>
    - <span data-ttu-id="db80f-121">警告はレコードの変更に設定することができます。</span><span class="sxs-lookup"><span data-stu-id="db80f-121">Alerts can be set up for record changes.</span></span> <span data-ttu-id="db80f-122">ワークフローがレコードを変更するので、ワークフローによって発生するレコードの変更に関連付けられた警告を設定することが可能です。</span><span class="sxs-lookup"><span data-stu-id="db80f-122">Workflows change records, so it's possible to set up an alert related to a record change caused by a workflow.</span></span> <span data-ttu-id="db80f-123">ただし、ワークフローにはさまざまな組み込み通知オプションがあるので、警告を使用することは理想的ではありません。</span><span class="sxs-lookup"><span data-stu-id="db80f-123">However, because workflows have different built-in notification options, using alerts isn’t ideal.</span></span>
- <span data-ttu-id="db80f-124">ワークフローからの標準通知</span><span class="sxs-lookup"><span data-stu-id="db80f-124">Standard notifications from workflows</span></span> 
    - <span data-ttu-id="db80f-125">ワークフローには電子メール通知が組み込まれています。</span><span class="sxs-lookup"><span data-stu-id="db80f-125">Workflows have built in email notifications.</span></span> <span data-ttu-id="db80f-126">顧客は通知を構成できるので、ユーザーに電子メールが送信されます。</span><span class="sxs-lookup"><span data-stu-id="db80f-126">A customer can configure the notifications so that the users are sent emails.</span></span> <span data-ttu-id="db80f-127">それらの通知は、ユーザーに対するアクション センター メッセージにはなりません。</span><span class="sxs-lookup"><span data-stu-id="db80f-127">Those notifications don’t result in Action Center messages for users.</span></span>
    - <span data-ttu-id="db80f-128">今後の更新で、ユーザーにワークフロー 作業項目が割り当てられるようにアクション センター メッセージを追加します。</span><span class="sxs-lookup"><span data-stu-id="db80f-128">In a future update we will be adding an Action Center message so a user is assigned a workflow work item.</span></span> 
- <span data-ttu-id="db80f-129">ワークフローへの通知の追加</span><span class="sxs-lookup"><span data-stu-id="db80f-129">Adding notifications to workflows</span></span>
    - <span data-ttu-id="db80f-130">アクション センター メッセージは、X++ のワークフローから作成されたメッセージのように、特定のユーザーに対して作成されます。</span><span class="sxs-lookup"><span data-stu-id="db80f-130">Action Center messages can be created for specific users, such as a message created from a workflow in X++.</span></span>
    - <span data-ttu-id="db80f-131">顧客が探している通知を持つフローをトリガーするために使用できる [ビジネス イベントのあるワークフロー](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow)。</span><span class="sxs-lookup"><span data-stu-id="db80f-131">[Workflows have business events](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) that the customer could use to trigger Flows have the notifications that they are looking for.</span></span>   

<span data-ttu-id="db80f-132">要約すると、ユーザーがワークフロー作業項目を割り当てられた時、アクション センターから適切な通知を取得できなかった場合、[ワークフロー ビジネス イベント](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) と Microsoft Power Automate を活用して、追加のまたは異なる通知を行います。</span><span class="sxs-lookup"><span data-stu-id="db80f-132">In summary, if a user does not get the proper notification from the Action Center when they are assigned a workflow work item, then leverage [Workflow business events](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) with Microsoft Power Automate to provide additional or different notifications.</span></span>

## <a name="why-is-workflow-editor-not-able-to-start-under-ad-fs"></a><span data-ttu-id="db80f-133">AD FS 下でワークフロー エディターを起動できないのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="db80f-133">Why is workflow editor not able to start under AD FS?</span></span>
<span data-ttu-id="db80f-134">アップグレードされた環境で Active Directory フェデレーション サービス (AD FS) を実行している場合、ワークフロー エディターで問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="db80f-134">When running under Active Directory Federation Services (AD FS) in an upgraded environment, the workflow editor may have trouble starting.</span></span> <span data-ttu-id="db80f-135">その場合、ADFS 設定の **Microsoft Dynamics 365 for Operations オンプレミス - ワークフロー - ネイティブ アプリケーション** プロパティに、URL 「https://dynamicsaxworkfloweditor/」が追加されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="db80f-135">If it does, make sure that the URL "https://dynamicsaxworkfloweditor/" is added to the property **Microsoft Dynamics 365 for Operations On-premises - Workflow - Native application** in the ADFS settings.</span></span>

## <a name="why-am-i-getting-sql-deadlocks-on-workflow-processing"></a><span data-ttu-id="db80f-136">ワークフロー処理で SQL デッドロックが発生するのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="db80f-136">Why am I getting SQL deadlocks on workflow processing?</span></span> 
<span data-ttu-id="db80f-137">**ワークフロー パラメーター** ページの **バッチごとのワークフロー項目数** のフィールドの既定値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="db80f-137">The default field value for the **Number of workflow items per batch** on the **Workflow parameters** page is 0.</span></span> <span data-ttu-id="db80f-138">値が 0 の場合、既定がバッチあたり 20 項目に変更されます。</span><span class="sxs-lookup"><span data-stu-id="db80f-138">A value of 0 causes the  default to change to 20 items per batch.</span></span> <span data-ttu-id="db80f-139">バッチごとの項目数が大きいと (> 40) SQL デッドロックが発生することがあるため、この値を調整する場合は注意が必要です。</span><span class="sxs-lookup"><span data-stu-id="db80f-139">Be careful when adjusting this value because a high number of items per batch (> 40) can cause SQL deadlocks.</span></span>

## <a name="what-is-the-workflow-enhanced-error-feature"></a><span data-ttu-id="db80f-140">ワークフロー拡張エラー機能とは ?</span><span class="sxs-lookup"><span data-stu-id="db80f-140">What is the Workflow Enhanced Error feature?</span></span>
<span data-ttu-id="db80f-141">Version 10.0.13 のワークフロー拡張エラー機能によって、さまざまなクラスのワークフロー エラーを区別するためのエラー コードが追加されます。</span><span class="sxs-lookup"><span data-stu-id="db80f-141">The Workflow Enhanced Error feature in version 10.0.13 adds error codes to differentiate different classes of workflow errors.</span></span> <span data-ttu-id="db80f-142">報告されたエラーメッセージは、多くの場合、若干の違いがあるため、わかりやすくすることができます。</span><span class="sxs-lookup"><span data-stu-id="db80f-142">The error messages reported will be mostly similar with minor differences to make them clearer.</span></span>
