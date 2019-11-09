---
title: Lifecycle Services (LCS) のライセンス数見積もりツール
description: この記事では、Microsoft Dynamics Lifecycle Services (LCS) のライセンス数見積もりツールに関する情報を提供します。 ライセンス数見積もりツールは、組織の Microsoft Dynamics AX に必要なライセンスの数の予測に役立ちます。 また、データを入力してレポートを生成する方法についても説明します。これで、ツールの使用を開始できます。
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: AX 2012
ms.custom: 13381
ms.assetid: 6f5723b9-a2f5-40e1-9a95-2fd5f6b9fd84
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 58ff80f52043a6674504cc7dac346e75ea079d08
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183244"
---
# <a name="license-sizing-estimator-in-lifecycle-services-lcs"></a><span data-ttu-id="cb4a1-105">Lifecycle Services (LCS) のライセンス数見積もりツール</span><span class="sxs-lookup"><span data-stu-id="cb4a1-105">License sizing estimator in Lifecycle Services (LCS)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cb4a1-106">この記事では、Microsoft Dynamics Lifecycle Services (LCS) のライセンス数見積もりツールに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="cb4a1-106">This article provides information about License sizing estimator in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="cb4a1-107">ライセンス数見積もりツールは、組織の Microsoft Dynamics AX に必要なライセンスの数の予測に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="cb4a1-107">The License sizing estimator tool helps you estimate the number of licenses that an organization will require for Microsoft Dynamics AX.</span></span> <span data-ttu-id="cb4a1-108">また、データを入力してレポートを生成する方法についても説明します。これで、ツールの使用を開始できます。</span><span class="sxs-lookup"><span data-stu-id="cb4a1-108">The article also explains how to enter data and generate a report so that you can start using the tool.</span></span>

<span data-ttu-id="cb4a1-109">Microsoft Dynamics Lifecycle Services (LCS) では、ライセンス数見積もりツールは、組織の Microsoft Dynamics AX に必要なライセンスの数の予測に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="cb4a1-109">In Microsoft Dynamics Lifecycle Services (LCS), License sizing estimator helps you estimate the number of licenses that an organization will require for Microsoft Dynamics AX.</span></span> <span data-ttu-id="cb4a1-110">これは、既定またはカスタマイズされたロールをモデル化して、必要なクライアント アクセス ライセンス (CAL) を自動的に計算するために使用できる共有ワークスペースを提供します。</span><span class="sxs-lookup"><span data-stu-id="cb4a1-110">It provides a shared workspace that you can use to model default and customized roles, and then automatically calculate the required client access licenses (CALs).</span></span> <span data-ttu-id="cb4a1-111">ライセンス数見積もりツールは、次の状況で使用できる情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="cb4a1-111">License sizing estimator provides information that you can use in the following circumstances:</span></span>

-   <span data-ttu-id="cb4a1-112">顧客が Microsoft Dynamics AX を購入する前に</span><span class="sxs-lookup"><span data-stu-id="cb4a1-112">Before a customer purchases Microsoft Dynamics AX</span></span>
-   <span data-ttu-id="cb4a1-113">既存の Microsoft Dynamics AX の実装を展開する前に</span><span class="sxs-lookup"><span data-stu-id="cb4a1-113">Before you expand your existing Microsoft Dynamics AX implementation</span></span>
-   <span data-ttu-id="cb4a1-114">新しいバージョンの Microsoft Dynamics AX にアップグレードする前に</span><span class="sxs-lookup"><span data-stu-id="cb4a1-114">Before you upgrade to a newer version of Microsoft Dynamics AX</span></span>

<span data-ttu-id="cb4a1-115">いくつかの方法で、ロールおよびその関連する職務を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="cb4a1-115">You can define roles and their associated duties in several ways.</span></span> <span data-ttu-id="cb4a1-116">ライセンス数見積もりツールは、Microsoft Dynamics AX に含まれる既定のロールを提供します。</span><span class="sxs-lookup"><span data-stu-id="cb4a1-116">License sizing estimator provides the default roles that are included in Microsoft Dynamics AX.</span></span> <span data-ttu-id="cb4a1-117">顧客の組織内のロールを適切に説明している場合、これらの定義済みロールのいずれかを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="cb4a1-117">You can use any of these predefined roles if they adequately describe the roles in the customer organization.</span></span> <span data-ttu-id="cb4a1-118">定義済みのロールが組織の要件を満たしていない場合は、職務を追加したり、職務を削除してカスタム ロールをモデル化することができます。</span><span class="sxs-lookup"><span data-stu-id="cb4a1-118">If a predefined role doesn't meet the organization’s requirements, you can add duties or remove duties to model a custom role.</span></span> <span data-ttu-id="cb4a1-119">使用可能な職務の一覧から新しいロールをモデル化することもできます。</span><span class="sxs-lookup"><span data-stu-id="cb4a1-119">You can also model a new role from the list of available duties.</span></span> <span data-ttu-id="cb4a1-120">**重要**: ライセンス数見積もりツールで定義したロールは、Microsoft Dynamics AX にエクスポートできません。</span><span class="sxs-lookup"><span data-stu-id="cb4a1-120">**Important:** The roles that you define in License sizing estimator can't be exported to Microsoft Dynamics AX.</span></span> <span data-ttu-id="cb4a1-121">Microsoft Dynamics AX でカスタム ロールを実装するには、「[Microsoft Dynamics AX でユーザー セキュリティを設定する](http://technet.microsoft.com/library/a9eea83b-60bf-4690-8442-a459de3c2001(AX.60).aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cb4a1-121">To implement custom roles in Microsoft Dynamics AX, see [Set up user security in Microsoft Dynamics AX](http://technet.microsoft.com/library/a9eea83b-60bf-4690-8442-a459de3c2001(AX.60).aspx).</span></span> <span data-ttu-id="cb4a1-122">組織内のロールを定義した後は、入力した情報を要約したレポートを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="cb4a1-122">After you define the roles in the organization, you can view a report that summarizes the information that you entered.</span></span> <span data-ttu-id="cb4a1-123">このレポートは、組織が必要とするライセンスの数と種類を自動的に推定します。</span><span class="sxs-lookup"><span data-stu-id="cb4a1-123">This report automatically estimates the number and types of licenses that the organization requires.</span></span> <span data-ttu-id="cb4a1-124">見積は、各ロールに含まれる職務を実行するために必要な CAL レベル、および各ロールの人数に基づいています。</span><span class="sxs-lookup"><span data-stu-id="cb4a1-124">The estimate is based on the CAL levels that are required to perform the duties that are included in each role, and the number of people in each role.</span></span> <span data-ttu-id="cb4a1-125">見積は、ユーザーが Microsoft Dynamics AX にアクセスする方法にも基づいています。</span><span class="sxs-lookup"><span data-stu-id="cb4a1-125">The estimate is also based on the way that users access Microsoft Dynamics AX.</span></span> <span data-ttu-id="cb4a1-126">ユーザーは、ネームド ユーザーとして、またはライセンスされたデバイスを介して Microsoft Dynamics AX にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="cb4a1-126">Users can access Microsoft Dynamics AX either as named users or through a licensed device.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="cb4a1-127">必要条件</span><span class="sxs-lookup"><span data-stu-id="cb4a1-127">Prerequisites</span></span>
<span data-ttu-id="cb4a1-128">None</span><span class="sxs-lookup"><span data-stu-id="cb4a1-128">None</span></span>

## <a name="getting-started"></a><span data-ttu-id="cb4a1-129">はじめに</span><span class="sxs-lookup"><span data-stu-id="cb4a1-129">Getting started</span></span>
<span data-ttu-id="cb4a1-130">ライセンス数見積もりツールを使用するには、データを入力し、レポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="cb4a1-130">To use License sizing estimator, you enter data and generate reports.</span></span> <span data-ttu-id="cb4a1-131">**重要:** このツールは、各ユーザーが単一のロールを実行すると想定しています。</span><span class="sxs-lookup"><span data-stu-id="cb4a1-131">**Important:** This tool assumes that each user performs a single role.</span></span> <span data-ttu-id="cb4a1-132">複数のロールに同じ担当者を入力すると、その人は、レポート上独立した複数のユーザーとしてカウントされるようになります。</span><span class="sxs-lookup"><span data-stu-id="cb4a1-132">If you enter the same person in multiple roles, that person will be counted as multiple separate users on the report.</span></span> <span data-ttu-id="cb4a1-133">たとえば、3 つのロールを持つユーザーは、3 つのユーザーとして見なされます。</span><span class="sxs-lookup"><span data-stu-id="cb4a1-133">For example, a person who has three roles will be counted as three users.</span></span>

### <a name="enter-data"></a><span data-ttu-id="cb4a1-134">データの入力</span><span class="sxs-lookup"><span data-stu-id="cb4a1-134">Enter data</span></span>

1.  <span data-ttu-id="cb4a1-135">[Lifecycle Services に移動](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="cb4a1-135">[Go to Lifecycle Services](https://lcs.dynamics.com).</span></span>
2.  <span data-ttu-id="cb4a1-136">プロジェクトで、**ライセンス数見積もりツール**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cb4a1-136">In a project, click **License sizing estimator**.</span></span>
3.  <span data-ttu-id="cb4a1-137">**編集の概要**ページで、従業員と仕入先ユーザーの番号に関する情報を入力し、新規または既存の実装の見積を作成するかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="cb4a1-137">On the **Edit overview** page, enter information about the number of employees and vendor users, and select whether you're creating an estimate for a new or existing implementation.</span></span>
4.  <span data-ttu-id="cb4a1-138">追加する部門を選択するには、**部門の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cb4a1-138">Click **Add department** to select departments to add.</span></span>
5.  <span data-ttu-id="cb4a1-139">**ライセンス数見積もりツール**ページで、顧客組織のロールに関する詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="cb4a1-139">On the **License sizing estimator** page, enter details about the roles in the customer organization.</span></span> <span data-ttu-id="cb4a1-140">**注記:** **ライセンス数見積もりツール**ページは、パノラマ ページです。</span><span class="sxs-lookup"><span data-stu-id="cb4a1-140">**Note:** The **License sizing estimator** page is a panorama page.</span></span> <span data-ttu-id="cb4a1-141">このページのすべての情報を表示するには、マウス ホイールまたはブラウザーの下のスクロールバーを使用して右にスクロールします。</span><span class="sxs-lookup"><span data-stu-id="cb4a1-141">To see all the information on this page, scroll to the right by using your mouse wheel or the lower scrollbar in your browser.</span></span>

### <a name="generate-a-report"></a><span data-ttu-id="cb4a1-142">レポートの生成</span><span class="sxs-lookup"><span data-stu-id="cb4a1-142">Generate a report</span></span>

<span data-ttu-id="cb4a1-143">**ライセンス数見積もりツール**ページで、**レポートの生成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cb4a1-143">On the **License sizing estimator** page, click **Generate report**.</span></span> <span data-ttu-id="cb4a1-144">レポートでは、入力したデータが要約され、見積済ライセンス情報が表形式と円グラフ形式で表示されます。</span><span class="sxs-lookup"><span data-stu-id="cb4a1-144">The report summarizes the data that you’ve entered, and provides estimated licensing information in the form of a table and a pie chart.</span></span>


