---
title: "インフラストラクチャ見積もりツール (AX 2012)"
description: "Microsoft Dynamics Lifecycle Services インフラストラクチャ見積もりツールは、環境に必要なハードウェアの最初の大まかな見積もりを自動的に行います。 オンプレミスまたはクラウドにある環境に対して見積もりを提供することができます。 この見積は、より詳細な手動サイズ変更の見積の基礎として使用されるもので、置き換えられるものではありません。"
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 19081
ms.assetid: ce126e17-5dc6-42fd-a9aa-4932e3db3830
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 9d695cb32decd5554890d66397971c56e00406ff
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="infrastructure-estimator-ax-2012"></a><span data-ttu-id="d3f31-105">インフラストラクチャ見積もりツール (AX 2012)</span><span class="sxs-lookup"><span data-stu-id="d3f31-105">Infrastructure estimator (AX 2012)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d3f31-106">Microsoft Dynamics Lifecycle Services インフラストラクチャ見積もりツールは、環境に必要なハードウェアの最初の大まかな見積もりを自動的に行います。</span><span class="sxs-lookup"><span data-stu-id="d3f31-106">The Microsoft Dynamics Lifecycle Services Infrastructure estimator provides an automated rough first estimate of the hardware needs of an environment.</span></span> <span data-ttu-id="d3f31-107">オンプレミスまたはクラウドにある環境に対して見積もりを提供することができます。</span><span class="sxs-lookup"><span data-stu-id="d3f31-107">Estimates can be provided for environments that are on your premises or in the cloud.</span></span> <span data-ttu-id="d3f31-108">この見積は、より詳細な手動サイズ変更の見積の基礎として使用されるもので、置き換えられるものではありません。</span><span class="sxs-lookup"><span data-stu-id="d3f31-108">The estimate is intended to be used as a basis for more in-depth, manual sizing estimates, not to replace them.</span></span>

<span data-ttu-id="d3f31-109">インフラストラクチャ サイズの見積もりは以下によって作成されます。</span><span class="sxs-lookup"><span data-stu-id="d3f31-109">An infrastructure sizing estimate is created by:</span></span>
1.  <span data-ttu-id="d3f31-110">使用状況プロファイルでの使用状況とロール要件を収集しています。</span><span class="sxs-lookup"><span data-stu-id="d3f31-110">Gathering usage and role requirements in a usage profile.</span></span>
2.  <span data-ttu-id="d3f31-111">事前に定義されたサイズの一連のサーバーと要件を照合します。</span><span class="sxs-lookup"><span data-stu-id="d3f31-111">Matching the requirements with a set of servers of predefined size.</span></span>

| <span data-ttu-id="d3f31-112">**重要**</span><span class="sxs-lookup"><span data-stu-id="d3f31-112">**Important**</span></span>                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3f31-113">いくつかのデータ ポイントは見積を作成するために使用されるので、見積はおおまかになり、サイズ制限は比較的低くなります。</span><span class="sxs-lookup"><span data-stu-id="d3f31-113">Because few data points are used to create an estimate, the estimate will be rough, and sizing limits are relatively low.</span></span> <span data-ttu-id="d3f31-114">したがって、インフラストラクチャの見積り担当者は現在、大規模な実装のニーズに対応できません。</span><span class="sxs-lookup"><span data-stu-id="d3f31-114">Therefore, the Infrastructure estimator can’t currently address the needs of large implementations.</span></span> |

## <a name="environments"></a><span data-ttu-id="d3f31-115">環境</span><span class="sxs-lookup"><span data-stu-id="d3f31-115">Environments</span></span>
<span data-ttu-id="d3f31-116">インフラストラクチャ見積もりは、次のタイプの環境においてオンプレミスまたはクラウドで使用できます。</span><span class="sxs-lookup"><span data-stu-id="d3f31-116">Infrastructure estimates are available for the following types of environments, either on premises or in the cloud.</span></span>
-   <span data-ttu-id="d3f31-117">Development 開発者およびバージョン管理システムをサポートする環境の見積もりを作成します。</span><span class="sxs-lookup"><span data-stu-id="d3f31-117">DevelopmentCreate an estimate for an environment that supports developers and a version control system.</span></span> <span data-ttu-id="d3f31-118">開発環境の見積は、大量のトランザクション負荷をサポートするようには設計されていません。</span><span class="sxs-lookup"><span data-stu-id="d3f31-118">The estimate for a development environment is not designed to support a heavy transaction load.</span></span> <span data-ttu-id="d3f31-119">この見積では、3 台のコンピューターを想定しています。</span><span class="sxs-lookup"><span data-stu-id="d3f31-119">The estimate assumes three computers.</span></span>
-   <span data-ttu-id="d3f31-120">実稼働環境の見積を ProductionCreate します。</span><span class="sxs-lookup"><span data-stu-id="d3f31-120">ProductionCreate an estimate for a live environment.</span></span> <span data-ttu-id="d3f31-121">本番環境の見積は、使用状況プロファイラーで入力した情報に基づいています。</span><span class="sxs-lookup"><span data-stu-id="d3f31-121">The estimate for a production environment is based on information that you entered in the Usage profiler.</span></span> <span data-ttu-id="d3f31-122">この環境に提供される見積は、大量のビジネス トランザクションと多くのユーザーをサポートします。</span><span class="sxs-lookup"><span data-stu-id="d3f31-122">The estimate provided for this environment will support a high volume of business transactions and many users.</span></span>
-   <span data-ttu-id="d3f31-123">機能またはパフォーマンス テストをサポートする環境の見積を TestCreate します。</span><span class="sxs-lookup"><span data-stu-id="d3f31-123">TestCreate an estimate for an environment that supports functional or performance testing.</span></span> <span data-ttu-id="d3f31-124">見積には、最大 4 台のコンピューターを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="d3f31-124">The estimate can include up to four computers.</span></span>
-   <span data-ttu-id="d3f31-125">Microsoft Dynamics AX でトレーニング ユーザーをサポートする環境の見積もりを作成します。</span><span class="sxs-lookup"><span data-stu-id="d3f31-125">TrainingCreate an estimate for an environment that supports training users on Microsoft Dynamics AX.</span></span> <span data-ttu-id="d3f31-126">トレーニング環境に提供される見積は、大量のトランザクション負荷をサポートするようには設計されていません。</span><span class="sxs-lookup"><span data-stu-id="d3f31-126">The estimate provided for a training environment is not designed to support a heavy transaction load.</span></span> <span data-ttu-id="d3f31-127">見積には、最大 4 台のコンピューターを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="d3f31-127">The estimate can include up to four computers.</span></span>

## <a name="server-roles"></a><span data-ttu-id="d3f31-128">サーバー ロール</span><span class="sxs-lookup"><span data-stu-id="d3f31-128">Server roles</span></span>
<span data-ttu-id="d3f31-129">サーバーの役割は、Microsoft Dynamics AX 環境の主要なコンポーネントを表します。</span><span class="sxs-lookup"><span data-stu-id="d3f31-129">Server roles represent the major components of the Microsoft Dynamics AX environment.</span></span> <span data-ttu-id="d3f31-130">各サーバーは、複数のロール要件を満たすために使用できます (たとえば、Analysis Services および Reporting Services を同じコンピュータに配置)。</span><span class="sxs-lookup"><span data-stu-id="d3f31-130">Each server can be used to meet multiple role requirements (for example, by putting Analysis Services and Reporting Services on the same computer).</span></span> <span data-ttu-id="d3f31-131">インフラストラクチャ見積もりツールでは、各サーバー ロールには、処理能力を事前定義された量が必要です。</span><span class="sxs-lookup"><span data-stu-id="d3f31-131">For the purposes of the Infrastructure estimator, each server role requires a predefined amount of processing power.</span></span> <span data-ttu-id="d3f31-132">インフラストラクチャ見積もりツールは、環境の各ロールの CPU および RAM 要件を満たす最小サーバーを選択します。</span><span class="sxs-lookup"><span data-stu-id="d3f31-132">The Infrastructure estimator selects the smallest server that meets the CPU and RAM requirements for each role in the environment.</span></span> <span data-ttu-id="d3f31-133">環境によっては、次のサーバー ロールが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="d3f31-133">The following server roles may be required, depending on your environment.</span></span>

| <span data-ttu-id="d3f31-134">役割</span><span class="sxs-lookup"><span data-stu-id="d3f31-134">Role</span></span>                          | <span data-ttu-id="d3f31-135">条件</span><span class="sxs-lookup"><span data-stu-id="d3f31-135">Condition</span></span>                                                                                 |
|-------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3f31-136">AOS</span><span class="sxs-lookup"><span data-stu-id="d3f31-136">AOS</span></span>                           | <span data-ttu-id="d3f31-137">常に必要です</span><span class="sxs-lookup"><span data-stu-id="d3f31-137">Always required</span></span>                                                                           |
| <span data-ttu-id="d3f31-138">SQL Server</span><span class="sxs-lookup"><span data-stu-id="d3f31-138">SQL Server</span></span>                    | <span data-ttu-id="d3f31-139">常に必要です</span><span class="sxs-lookup"><span data-stu-id="d3f31-139">Always required</span></span>                                                                           |
| <span data-ttu-id="d3f31-140">Terminal Services</span><span class="sxs-lookup"><span data-stu-id="d3f31-140">Terminal Services</span></span>             | <span data-ttu-id="d3f31-141">リモート運用サイトがある場合に必須</span><span class="sxs-lookup"><span data-stu-id="d3f31-141">Required if there is a remote operating site</span></span>                                              |
| <span data-ttu-id="d3f31-142">エンタープライズ ポータル</span><span class="sxs-lookup"><span data-stu-id="d3f31-142">Enterprise Portal</span></span>             | <span data-ttu-id="d3f31-143">使用状況プロファイラーの配置の詳細アンケートで指定されている場合に必須</span><span class="sxs-lookup"><span data-stu-id="d3f31-143">Required if it is specified in the Deployment details questionnaire of the Usage profiler</span></span> |
| <span data-ttu-id="d3f31-144">エンタープライズ ポータルの AOS</span><span class="sxs-lookup"><span data-stu-id="d3f31-144">AOS for Enterprise Portal</span></span>     | <span data-ttu-id="d3f31-145">エンタープライズ ポータルが必要な場合に必須</span><span class="sxs-lookup"><span data-stu-id="d3f31-145">Required if Enterprise Portal is needed</span></span>                                                   |
| <span data-ttu-id="d3f31-146">SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="d3f31-146">SQL Server Reporting Services</span></span> | <span data-ttu-id="d3f31-147">使用状況プロファイラーの配置の詳細アンケートで指定されている場合に必須</span><span class="sxs-lookup"><span data-stu-id="d3f31-147">Required if it is specified in the Deployment details questionnaire of the Usage profiler</span></span> |
| <span data-ttu-id="d3f31-148">SQL Server Analysis Services</span><span class="sxs-lookup"><span data-stu-id="d3f31-148">SQL Server Analysis Services</span></span>  | <span data-ttu-id="d3f31-149">使用状況プロファイラーの配置の詳細アンケートで指定されている場合に必須</span><span class="sxs-lookup"><span data-stu-id="d3f31-149">Required if it is specified in the Deployment details questionnaire of the Usage profiler</span></span> |
| <span data-ttu-id="d3f31-150">ヘルプ サーバー</span><span class="sxs-lookup"><span data-stu-id="d3f31-150">Help server</span></span>                   | <span data-ttu-id="d3f31-151">使用状況プロファイラーの配置の詳細アンケートで指定されている場合に必須</span><span class="sxs-lookup"><span data-stu-id="d3f31-151">Required if it is specified in the Deployment details questionnaire of the Usage profiler</span></span> |

## <a name="prerequisites"></a><span data-ttu-id="d3f31-152">前提条件</span><span class="sxs-lookup"><span data-stu-id="d3f31-152">Prerequisites</span></span>
<span data-ttu-id="d3f31-153">実稼働環境のインフラストラクチャの見積を作成する場合は、使用状況プロファイルを最初に完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3f31-153">If you want to create an infrastructure estimate for a production environment, you must first complete a usage profile.</span></span> <span data-ttu-id="d3f31-154">詳細については、[使用状況プロファイラー (Lifecycle Services, LCS)](usage-profiler-lcs.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d3f31-154">For more information, see [Usage profiler (Lifecycle Services, LCS)](usage-profiler-lcs.md).</span></span> <span data-ttu-id="d3f31-155">開発、テスト、およびトレーニング環境での見積には、完了した使用プロファイルは不要です。</span><span class="sxs-lookup"><span data-stu-id="d3f31-155">Estimates for development, test, and training environments do not require a completed usage profile.</span></span>

## <a name="create-an-infrastructure-estimate"></a><span data-ttu-id="d3f31-156">インフラストラクチャ見積もりを作成する</span><span class="sxs-lookup"><span data-stu-id="d3f31-156">Create an infrastructure estimate</span></span>
1.  <span data-ttu-id="d3f31-157">[Lifecycle Services に移動](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="d3f31-157">[Go to Lifecycle Services](https://lcs.dynamics.com).</span></span>
2.  <span data-ttu-id="d3f31-158">プロジェクトのホーム ページで、インフラストラクチャ見積もりツール タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d3f31-158">On the project home page, click the Infrastructure estimator tile.</span></span>
3.  <span data-ttu-id="d3f31-159">実稼働環境の見積が必要であり、利用状況プロファイルをまだ完了していない場合は、使用状況プロファイラー ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d3f31-159">If you need an estimate for a production environment and you haven’t yet completed a usage profile, click the Usage profiler button.</span></span> <span data-ttu-id="d3f31-160">詳細については、[使用状況プロファイラー (Lifecycle Services, LCS)](usage-profiler-lcs.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d3f31-160">For more information, see [Usage profiler (Lifecycle Services, LCS)](usage-profiler-lcs.md).</span></span>
4.  <span data-ttu-id="d3f31-161">新規見積をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d3f31-161">Click New estimate.</span></span>
5.  <span data-ttu-id="d3f31-162">見積を作成する環境のタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="d3f31-162">Select the type of environment that you are creating an estimate for.</span></span>
6.  <span data-ttu-id="d3f31-163">見積名を入力し、社内またはクラウドでは、環境がオンプレミス内またはクラウド内でホストされるかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="d3f31-163">Enter a name for the estimate, and select whether the environment will be hosted on premises or in the cloud.</span></span>
7.  <span data-ttu-id="d3f31-164">必要に応じて、その他の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="d3f31-164">Enter other information as needed.</span></span> <span data-ttu-id="d3f31-165">次のテーブルに、選択した環境のタイプに応じて、追加する必要がある可能性のある追加情報について説明します。</span><span class="sxs-lookup"><span data-stu-id="d3f31-165">The following table describes the additional information that you may need to provide, depending on the type of environment that you selected.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="d3f31-166">環境</span><span class="sxs-lookup"><span data-stu-id="d3f31-166">Environment</span></span></th>
    <th><span data-ttu-id="d3f31-167">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d3f31-167">Parameters</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="d3f31-168">開発</span><span class="sxs-lookup"><span data-stu-id="d3f31-168">Development</span></span></td>
    <td><ul>
    <li><span data-ttu-id="d3f31-169">開発者数</span><span class="sxs-lookup"><span data-stu-id="d3f31-169">Number of developers</span></span></li>
    <li><span data-ttu-id="d3f31-170">バージョン管理システム</span><span class="sxs-lookup"><span data-stu-id="d3f31-170">Version control system</span></span></li>
    </ul></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="d3f31-171">実稼働</span><span class="sxs-lookup"><span data-stu-id="d3f31-171">Production</span></span></td>
    <td><span data-ttu-id="d3f31-172">None</span><span class="sxs-lookup"><span data-stu-id="d3f31-172">None</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="d3f31-173">テスト</span><span class="sxs-lookup"><span data-stu-id="d3f31-173">Test</span></span></td>
    <td><ul>
    <li><span data-ttu-id="d3f31-174">テストのタイプ</span><span class="sxs-lookup"><span data-stu-id="d3f31-174">Type of testing</span></span></li>
    <li><span data-ttu-id="d3f31-175">コンピューターの数。</span><span class="sxs-lookup"><span data-stu-id="d3f31-175">Number of computers</span></span></li>
    </ul></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="d3f31-176">トレーニング</span><span class="sxs-lookup"><span data-stu-id="d3f31-176">Training</span></span></td>
    <td><span data-ttu-id="d3f31-177">コンピューターの数。</span><span class="sxs-lookup"><span data-stu-id="d3f31-177">Number of computers</span></span></td>
    </tr>
    </tbody>
    </table>

8.  <span data-ttu-id="d3f31-178">[作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d3f31-178">Click Create.</span></span>

## <a name="view-infrastructure-estimates"></a><span data-ttu-id="d3f31-179">インフラストラクチャの見積もりの表示</span><span class="sxs-lookup"><span data-stu-id="d3f31-179">View infrastructure estimates</span></span>
<span data-ttu-id="d3f31-180">主要なインフラストラクチャ見積もりツールページで、詳細を表示する見積もりを選択します。</span><span class="sxs-lookup"><span data-stu-id="d3f31-180">On the main Infrastructure estimator page, select an estimate to view the details.</span></span>






