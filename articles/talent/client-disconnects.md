---
title: Talent のクライアントが切断される
description: このトピックでは、顧客が自身の環境から切断され、またその理由が分からない場合の対処方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 02df31b56c0e960a16ec2aadd8b1e817e0b6ec65
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898460"
---
# <a name="talent-client-disconnects"></a><span data-ttu-id="30c1e-103">Talent のクライアントが切断される</span><span class="sxs-lookup"><span data-stu-id="30c1e-103">Talent client disconnects</span></span>

<span data-ttu-id="30c1e-104">**環境の詳細**</span><span class="sxs-lookup"><span data-stu-id="30c1e-104">**Environment details**</span></span> 

<span data-ttu-id="30c1e-105">この問題は、すべての環境で発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="30c1e-105">This issue can occur in all environments.</span></span>
 
<span data-ttu-id="30c1e-106">**現象**</span><span class="sxs-lookup"><span data-stu-id="30c1e-106">**Symptom**</span></span> 

<span data-ttu-id="30c1e-107">顧客は自身の環境から切断され、またその理由が分かりません。</span><span class="sxs-lookup"><span data-stu-id="30c1e-107">The customer is disconnected from his or her environment and doesn't know why.</span></span> <span data-ttu-id="30c1e-108">顧客は、次のエラー メッセージのいずれかを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="30c1e-108">The customer receives one of the following error messages:</span></span>

- <span data-ttu-id="30c1e-109">接続が失われました。</span><span class="sxs-lookup"><span data-stu-id="30c1e-109">We've lost your connection.</span></span> <span data-ttu-id="30c1e-110">作業を続行するには、閉じるをクリックします。</span><span class="sxs-lookup"><span data-stu-id="30c1e-110">Click Close to continue working.</span></span>
- <span data-ttu-id="30c1e-111">ネットワーク接続が失われた可能性があります。もう一度実行するには [再試行] をクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="30c1e-111">It appears you lost network connectivity, click Retry to try again.</span></span>

<span data-ttu-id="30c1e-112">**赤いフラグ**</span><span class="sxs-lookup"><span data-stu-id="30c1e-112">**Red flag**</span></span>

<span data-ttu-id="30c1e-113">この問題は、ユーザーが実装のステージで、実稼働環境とテスト環境の間で情報を比較していて、セッション間で移動していることを忘れている場合によく発生します。</span><span class="sxs-lookup"><span data-stu-id="30c1e-113">This issue often occurs when users are in the implementation stage, are comparing information across production and test environments, and forget that they are moving between sessions.</span></span> <span data-ttu-id="30c1e-114">ユーザーがこのステージにいる場合は、この問題が発生する可能性が高くなります。</span><span class="sxs-lookup"><span data-stu-id="30c1e-114">If users are at this stage, they will most likely experience this issue.</span></span>

<span data-ttu-id="30c1e-115">**問題点**</span><span class="sxs-lookup"><span data-stu-id="30c1e-115">**Issue**</span></span> 

<span data-ttu-id="30c1e-116">**ブラウザーの種類:** Google Chrome Internet Explorer、および Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="30c1e-116">**Browser types:** Google Chrome, Internet Explorer, and Microsoft Edge</span></span>

<span data-ttu-id="30c1e-117">Microsoft Dynamics 365 Talent は、2 つの異なるセッションが同じユーザーと同じブラウザー タイプで同時に開いているときにユーザーを切断します。</span><span class="sxs-lookup"><span data-stu-id="30c1e-117">Microsoft Dynamics 365 Talent disconnects users when two different sessions are open at the same time for the same user and the same browser type.</span></span> <span data-ttu-id="30c1e-118">(たとえば、ユーザー A が Chrome で環境 1 と環境 2 の両方を表示しています。) ユーザーがブラウザーの別のウィンドウを開いているのか、別のタブを開いているのかは関係ありません。</span><span class="sxs-lookup"><span data-stu-id="30c1e-118">(For example, user A is viewing both environment 1 and environment 2 in Chrome.) It doesn't matter whether the users open different browser windows or different tabs.</span></span> <span data-ttu-id="30c1e-119">同じユーザー資格情報が、同じブラウザー タイプで同時に環境 1 と環境 2 の両方へのサインインに使用される場合、Talent はセッションのいずれかを切断します。</span><span class="sxs-lookup"><span data-stu-id="30c1e-119">If the same user credentials are used to sign in to both environment 1 and environment 2 at the same time and in the same browser type, Talent disconnects one of the sessions.</span></span>

<span data-ttu-id="30c1e-120">**ソリューション**</span><span class="sxs-lookup"><span data-stu-id="30c1e-120">**Solution**</span></span>

<span data-ttu-id="30c1e-121">特定のブラウザー タイプにつき 1 つだけの環境が開いていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="30c1e-121">Make sure that only one environment is open at a time for a given browser type.</span></span> <span data-ttu-id="30c1e-122">ユーザーは、同じ環境 (つまり、同じブラウザの複数のタブ) に対して複数のセッションを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="30c1e-122">Users can open multiple sessions to the same environment (that is, multiple tabs in the same browser).</span></span>

<span data-ttu-id="30c1e-123">同時に 2 つの環境間を移動するユーザーは、異なるブラウザー タイプで各環境を開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="30c1e-123">Users who want to jump between two environments at the same time should open each environment in a different browser type.</span></span> <span data-ttu-id="30c1e-124">(たとえば、ユーザー A は Chrome で環境 1 を、Microsoft Edge で環境 2 を表示できます。)</span><span class="sxs-lookup"><span data-stu-id="30c1e-124">(For example, user A can view environment 1 in Chrome and environment 2 in Microsoft Edge.)</span></span>
