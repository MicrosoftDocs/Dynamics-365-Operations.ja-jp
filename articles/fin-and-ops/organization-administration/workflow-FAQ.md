---
title: ワークフローに関するよく寄せられる質問
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations のワークフロー システムについてよく寄せられる質問に回答します。
author: ChrisGarty
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: adcc9bbc422a3fddfd51d248daf95c0da6d4c9bb
ms.sourcegitcommit: 8cf77e9171d6cad8ae6c8bfad9e4f9a46fef6d23
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/19/2019
ms.locfileid: "1689003"
---
# <a name="workflow-faq"></a><span data-ttu-id="3b5e7-103">ワークフローに関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="3b5e7-103">Workflow FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3b5e7-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations のワークフロー システムについてよく寄せられる質問に回答します。</span><span class="sxs-lookup"><span data-stu-id="3b5e7-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="3b5e7-105">作業項目が否認された場合に複数の通知が受信されるのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="3b5e7-105">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="3b5e7-106">作業項目が否認されると、その作業項目は否認済として完了します。</span><span class="sxs-lookup"><span data-stu-id="3b5e7-106">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="3b5e7-107">別の作業項目が作成され、作成者に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="3b5e7-107">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="3b5e7-108">これは、否認された作業項目に関する発信者への通知と、新しい「変更要求済」の作業項目に割り当てられたユーザーへの個別の通知があることを意味します。</span><span class="sxs-lookup"><span data-stu-id="3b5e7-108">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="3b5e7-109">各通知は異なる作業項目に対するものですが、類似性により混乱が生じる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3b5e7-109">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="3b5e7-110">将来のリリースでこれを改善する方法を検討しています。</span><span class="sxs-lookup"><span data-stu-id="3b5e7-110">We are looking at ways to improve this in a future release.</span></span>

## <a name="why-are-my-workflow-exports-failing"></a><span data-ttu-id="3b5e7-111">ワークフローのエクスポートが失敗するのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="3b5e7-111">Why are my workflow exports failing?</span></span>
<span data-ttu-id="3b5e7-112">現在、ワークフローのエクスポート機能には、ワークフロー名が 48 文字を超えないようにする制限があります。</span><span class="sxs-lookup"><span data-stu-id="3b5e7-112">There is currently a limitation in the workflow export feature that prevents workflow names from exceeding 48 characters.</span></span> <span data-ttu-id="3b5e7-113">48 文字を超える名前を使用すると、「サーバーは要求の認証に失敗しました」というエラーが発生するか、またはファイルがファイル タイプなしでエクスポートされるのを防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="3b5e7-113">Using a name that is longer than 48 characters can result in a "Server failed to authenticate the request" error and/or prevent a file to be exported  without a file type.</span></span> <span data-ttu-id="3b5e7-114">詳細については、次のブログ記事を参照してください [ワークフローのエクスポートに関するトラブルシューティング](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting)。</span><span class="sxs-lookup"><span data-stu-id="3b5e7-114">The following blog post provides more details [Workflow Export Troubleshooting](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span></span>

## <a name="can-the-submitter-of-a-workflow-also-approve-the-workflow"></a><span data-ttu-id="3b5e7-115">ワークフローの送信者はワークフローを承認することもできますか。</span><span class="sxs-lookup"><span data-stu-id="3b5e7-115">Can the submitter of a workflow also approve the workflow?</span></span>
<span data-ttu-id="3b5e7-116">はい、そのように構成されている場合、ワークフローの送信者は、ワークフローを承認することもできます。</span><span class="sxs-lookup"><span data-stu-id="3b5e7-116">Yes, a submitter of a workflow can also approve the workflow if it is configured that way.</span></span> <span data-ttu-id="3b5e7-117">この動作を回避するには、**ワークフロー パラメーター > 一般 > 承認者 > 送信者による承認を許可しない**を**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="3b5e7-117">To prevent this behavior, set **Workflow parameters > General > Approver > Disallow approval by submitter** to **Yes**.</span></span>

## <a name="can-i-add-alerts-to-workflows-to-provide-notifications-to-users"></a><span data-ttu-id="3b5e7-118">ユーザーに通知を行うためにワークフローに警告を追加することはできますか?</span><span class="sxs-lookup"><span data-stu-id="3b5e7-118">Can I add alerts to workflows to provide notifications to users?</span></span>
<span data-ttu-id="3b5e7-119">通知を行うワークフローへの警告の追加に関する注意事項の重要な領域を次に示します。</span><span class="sxs-lookup"><span data-stu-id="3b5e7-119">Here are a few key areas to note about adding alerts to workflows to provide notifications:</span></span>
- <span data-ttu-id="3b5e7-120">警告とワークフロー通知のメカニズム</span><span class="sxs-lookup"><span data-stu-id="3b5e7-120">Alerts versus workflow notification mechanisms</span></span>
    - <span data-ttu-id="3b5e7-121">警告はレコードの変更に設定することができます。</span><span class="sxs-lookup"><span data-stu-id="3b5e7-121">Alerts can be set up for record changes.</span></span> <span data-ttu-id="3b5e7-122">ワークフローがレコードを変更するので、ワークフローによって発生するレコードの変更に関連付けられた警告を設定することが可能です。</span><span class="sxs-lookup"><span data-stu-id="3b5e7-122">Workflows change records, so it's possible to set up an alert related to a record change caused by a workflow.</span></span> <span data-ttu-id="3b5e7-123">ただし、ワークフローにはさまざまな組み込み通知オプションがあるので、警告を使用することは理想的ではありません。</span><span class="sxs-lookup"><span data-stu-id="3b5e7-123">However, because workflows have different built-in notification options, using alerts isn’t ideal.</span></span>
- <span data-ttu-id="3b5e7-124">ワークフローからの標準通知</span><span class="sxs-lookup"><span data-stu-id="3b5e7-124">Standard notifications from workflows</span></span> 
    - <span data-ttu-id="3b5e7-125">ワークフローには電子メール通知が組み込まれています。</span><span class="sxs-lookup"><span data-stu-id="3b5e7-125">Workflows have built in email notifications.</span></span> <span data-ttu-id="3b5e7-126">顧客は通知を構成できるので、ユーザーに電子メールが送信されます。</span><span class="sxs-lookup"><span data-stu-id="3b5e7-126">A customer can configure the notifications so that the users are sent emails.</span></span> <span data-ttu-id="3b5e7-127">それらの通知は、ユーザーに対するアクション センター メッセージにはなりません。</span><span class="sxs-lookup"><span data-stu-id="3b5e7-127">Those notifications don’t result in Action Center messages for users.</span></span>
    - <span data-ttu-id="3b5e7-128">今後の更新で、ユーザーにワークフロー 作業項目が割り当てられるようにアクション センター メッセージを追加します。</span><span class="sxs-lookup"><span data-stu-id="3b5e7-128">In a future update we will be adding an Action Center message so a user is assigned a workflow work item.</span></span> 
- <span data-ttu-id="3b5e7-129">ワークフローへの通知の追加</span><span class="sxs-lookup"><span data-stu-id="3b5e7-129">Adding notifications to workflows</span></span>
    - <span data-ttu-id="3b5e7-130">アクション センター メッセージは、X++ のワークフローから作成されたメッセージのように、特定のユーザーに対して作成されます。</span><span class="sxs-lookup"><span data-stu-id="3b5e7-130">Action Center messages can be created for specific users, such as a message created from a workflow in X++.</span></span>
    - <span data-ttu-id="3b5e7-131">[ビジネス イベントのあるワークフロー](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) 顧客は探している通知のあるフローをトリガーがすることができました。</span><span class="sxs-lookup"><span data-stu-id="3b5e7-131">[Workflows have Business Events](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) that the customer could use to trigger Flows have the notifications that they are looking for.</span></span>   

<span data-ttu-id="3b5e7-132">要約すると、ユーザーがワークフロー作業項目を割り当てられた時、アクション センターから適切な通知を取得できなかった場合、[ワークフロー ビジネス イベント](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) と Microsoft Flow を活用して、追加のまたは異なる通知を行います。</span><span class="sxs-lookup"><span data-stu-id="3b5e7-132">In summary, if a user does not get the proper notification from the Action Center when they are assigned a workflow work item, then leverage [Workflow Business Events](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) with Microsoft Flow to provide additional or different notifications.</span></span>
