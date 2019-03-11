---
title: ユーザー サインインの追跡
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations にサインインして使用するユーザーの監査ログを作成する方法について説明します。
author: manalidongre
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2017-10-31
ms.dyn365.ops.version: Platform update 12
ms.openlocfilehash: 42010539b63c582bfd4729175ecf8e06663bb274
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368652"
---
# <a name="track-user-sign-ins"></a><span data-ttu-id="b0d25-103">ユーザー サインインの追跡</span><span class="sxs-lookup"><span data-stu-id="b0d25-103">Track user sign-ins</span></span> 
 
[!include [banner](../includes/banner.md)]

<span data-ttu-id="b0d25-104">多くの組織は、システムを使用したユーザーの監査証跡を管理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0d25-104">Many organizations are required to maintain an audit trail of users who have used the system.</span></span> <span data-ttu-id="b0d25-105">この要件は、コンプライアンス上の理由から、または不適切な使用が発生した場合にトラックバックを有効にできます。 </span><span class="sxs-lookup"><span data-stu-id="b0d25-105">This requirement can be in place for compliance reasons, or to enable trackbacks in the event of incorrect use.</span></span>

<span data-ttu-id="b0d25-106">Microsoft Dynamics AX 2012 では、**監査ログ**フォームが Microsoft Dynamics AX 環境にアクセスしたユーザーを記録していました。</span><span class="sxs-lookup"><span data-stu-id="b0d25-106">In Microsoft Dynamics AX 2012, the **Audit log** form recorded which users accessed the Microsoft Dynamics AX environment.</span></span> <span data-ttu-id="b0d25-107">Microsoft Dynamics 365 for Finance and Operations では、この情報はテレメトリでキャプチャされます。</span><span class="sxs-lookup"><span data-stu-id="b0d25-107">In Microsoft Dynamics 365 for Finance and Operations, this information is captured in telemetry.</span></span> <span data-ttu-id="b0d25-108">IT 管理者は、Microsoft Dynamics Lifecycle Services (LCS) を使用して、この情報をダウンロードし、サインインしているユーザーの監査証跡を維持するためにオフライン ストレージに移動することができます。</span><span class="sxs-lookup"><span data-stu-id="b0d25-108">IT administrators can download this information by using Microsoft Dynamics Lifecycle Services (LCS) and then move it to offline storage to maintain the audit trail of users who have signed in.</span></span>

<span data-ttu-id="b0d25-109">システムを使用したユーザーの監査ログを生成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b0d25-109">To generate an audit log of users who have used the system, follow these steps.</span></span>

1. <span data-ttu-id="b0d25-110">LCS にサインインし、Finance and Operations 実装に関連付けられているプロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="b0d25-110">Sign in to LCS, and open the project that is associated with the Finance and Operations implementation.</span></span>
2. <span data-ttu-id="b0d25-111">実稼働環境に移動して、**環境の詳細**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="b0d25-111">Navigate to the production environment, and open the **Environment details** page.</span></span>
3. <span data-ttu-id="b0d25-112">**監視**タブで、**環境の監視**リンクを選択して、監視ダッシュボードを開きます。</span><span class="sxs-lookup"><span data-stu-id="b0d25-112">On the **Monitoring** tab, select the **Environment monitoring** link to open the monitoring dashboard.</span></span>
4. <span data-ttu-id="b0d25-113">**活動**タブで、**未加工のログの表示**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b0d25-113">On the **Activity** tab, select **View raw logs**.</span></span>
5. <span data-ttu-id="b0d25-114">**クエリ** フィールドで、**ユーザー ログイン イベント**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b0d25-114">In the **Query** field, select **User Login Events**.</span></span> <span data-ttu-id="b0d25-115">開始日が **終了日 - 7日** に設定されている期間を参照します。</span><span class="sxs-lookup"><span data-stu-id="b0d25-115">You see a time duration that has a start date that is set to **End date - 7 days**.</span></span>
6. <span data-ttu-id="b0d25-116">終了日を設定し、**検索** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b0d25-116">Set the end date, and then select **Search**.</span></span> <span data-ttu-id="b0d25-117">返される検索結果には、選択した終了日より 7 日前にシステムにサインインしたすべてのユーザーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b0d25-117">The search results that are returned include all users who signed in to the system during the seven days before the selected end date.</span></span>
7. <span data-ttu-id="b0d25-118">検索結果には、ユーザーのセッションの **AADUserID** 値と、サインインの開始時刻と終了時刻が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b0d25-118">The search results show the **AADUserID** value and the sign-in start and end times of the user's session.</span></span> <span data-ttu-id="b0d25-119">**AADUserID**の値をユーザーのユーザー名と電子メールアドレスにマップするには、Finance and Operations の **ユーザー** ページ (**システム管理** > **ユーザー**) を使用します。</span><span class="sxs-lookup"><span data-stu-id="b0d25-119">To map the **AADUserID** value to the user's user name and email address, use the **Users** page in Finance and Operations (**System administration** > **Users**).</span></span>
8. <span data-ttu-id="b0d25-120">レコードをエクスポートして長期間保存するには、**エクスポート グリッド** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b0d25-120">To export the records and keep them for a longer period, select **Export grid**.</span></span>

<span data-ttu-id="b0d25-121">完全な監査証跡を保証するために、IT 管理者は 7 日ごとにこの手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0d25-121">To help guarantee a complete audit trail, an IT administrator must complete this procedure every seven days.</span></span>
