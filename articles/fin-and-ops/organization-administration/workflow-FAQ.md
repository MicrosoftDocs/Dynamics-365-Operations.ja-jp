---
title: ワークフローに関するよく寄せられる質問
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations のワークフロー システムについてよく寄せられる質問に回答します。
author: ChrisGarty
manager: AnnBe
ms.date: 05/07/2019
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
ms.openlocfilehash: f6240b1b5136937aa47f455547fed6f0c7c08e2c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509294"
---
# <a name="workflow-system"></a><span data-ttu-id="41658-103">ワークフロー システム</span><span class="sxs-lookup"><span data-stu-id="41658-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="41658-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations のワークフロー システムについてよく寄せられる質問に回答します。</span><span class="sxs-lookup"><span data-stu-id="41658-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="notifications"></a><span data-ttu-id="41658-105">通知</span><span class="sxs-lookup"><span data-stu-id="41658-105">Notifications</span></span>

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="41658-106">作業項目が否認された場合に複数の通知が受信されるのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="41658-106">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="41658-107">作業項目が否認されると、その作業項目は否認済として完了します。</span><span class="sxs-lookup"><span data-stu-id="41658-107">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="41658-108">別の作業項目が作成され、作成者に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="41658-108">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="41658-109">これは、否認された作業項目に関する発信者への通知と、新しい「変更要求済」の作業項目に割り当てられたユーザーへの個別の通知があることを意味します。</span><span class="sxs-lookup"><span data-stu-id="41658-109">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="41658-110">各通知は異なる作業項目に対するものですが、類似性により混乱が生じる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="41658-110">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="41658-111">将来のリリースでこれを改善する方法を検討しています。</span><span class="sxs-lookup"><span data-stu-id="41658-111">We are looking at ways to improve this in a future release.</span></span>

### <a name="why-are-my-workflow-exports-failing"></a><span data-ttu-id="41658-112">ワークフローのエクスポートが失敗するのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="41658-112">Why are my workflow exports failing?</span></span>
<span data-ttu-id="41658-113">現在、ワークフローのエクスポート機能には、ワークフロー名が 48 文字を超えないようにする制限があります。</span><span class="sxs-lookup"><span data-stu-id="41658-113">There is currently a limitation in the workflow export feature that prevents workflow names from exceeding 48 characters.</span></span> <span data-ttu-id="41658-114">48 文字を超える名前を使用すると、「サーバーは要求の認証に失敗しました」というエラーが発生するか、またはファイルがファイル タイプなしでエクスポートされるのを防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="41658-114">Using a name that is longer than 48 characters can result in a "Server failed to authenticate the request" error and/or prevent a file to be exported  without a file type.</span></span> <span data-ttu-id="41658-115">詳細については、次のブログ記事を参照してください [ワークフローのエクスポートに関するトラブルシューティング](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting)。</span><span class="sxs-lookup"><span data-stu-id="41658-115">The following blog post provides more details [Workflow Export Troubleshooting](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span></span>
