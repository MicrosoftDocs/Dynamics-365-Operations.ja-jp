---
title: Lifecycle Services (LCS) でのインフラストラクチャ見積もりツール
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 19081
ms.assetid: ce126e17-5dc6-42fd-a9aa-4932e3db3830
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: c0477d50d89059e4425f7ee7883ab9e99af08b21
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537241"
---
# <a name="infrastructure-estimator-in-lifecycle-services-lcs"></a><span data-ttu-id="782ce-102">Lifecycle Services (LCS) でのインフラストラクチャ見積もりツール</span><span class="sxs-lookup"><span data-stu-id="782ce-102">Infrastructure estimator in Lifecycle Services (LCS)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="782ce-103">Microsoft Dynamics Lifecycle Services インフラストラクチャ見積もりツールは、環境に必要なハードウェアの最初の大まかな見積もりを自動的に行います。</span><span class="sxs-lookup"><span data-stu-id="782ce-103">The Microsoft Dynamics Lifecycle Services Infrastructure estimator provides an automated rough first estimate of the hardware needs of an environment.</span></span> <span data-ttu-id="782ce-104">オンプレミスまたはクラウドにある環境に対して見積もりを提供することができます。</span><span class="sxs-lookup"><span data-stu-id="782ce-104">Estimates can be provided for environments that are on your premises or in the cloud.</span></span> <span data-ttu-id="782ce-105">この見積は、より詳細な手動サイズ変更の見積の基礎として使用されるもので、置き換えられるものではありません。</span><span class="sxs-lookup"><span data-stu-id="782ce-105">The estimate is intended to be used as a basis for more in-depth, manual sizing estimates, not to replace them.</span></span>

<span data-ttu-id="782ce-106">インフラストラクチャ サイズの見積もりは以下によって作成されます。</span><span class="sxs-lookup"><span data-stu-id="782ce-106">An infrastructure sizing estimate is created by:</span></span>
1.  <span data-ttu-id="782ce-107">使用状況プロファイルでの使用状況とロール要件を収集しています。</span><span class="sxs-lookup"><span data-stu-id="782ce-107">Gathering usage and role requirements in a usage profile.</span></span>
2.  <span data-ttu-id="782ce-108">事前に定義されたサイズの一連のサーバーと要件を照合します。</span><span class="sxs-lookup"><span data-stu-id="782ce-108">Matching the requirements with a set of servers of predefined size.</span></span>

| <span data-ttu-id="782ce-109">**重要**</span><span class="sxs-lookup"><span data-stu-id="782ce-109">**Important**</span></span>                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="782ce-110">いくつかのデータ ポイントは見積を作成するために使用されるので、見積はおおまかになり、サイズ制限は比較的低くなります。</span><span class="sxs-lookup"><span data-stu-id="782ce-110">Because few data points are used to create an estimate, the estimate will be rough, and sizing limits are relatively low.</span></span> <span data-ttu-id="782ce-111">したがって、インフラストラクチャの見積り担当者は現在、大規模な実装のニーズに対応できません。</span><span class="sxs-lookup"><span data-stu-id="782ce-111">Therefore, the Infrastructure estimator can’t currently address the needs of large implementations.</span></span> |

## <a name="environments"></a><span data-ttu-id="782ce-112">環境</span><span class="sxs-lookup"><span data-stu-id="782ce-112">Environments</span></span>
<span data-ttu-id="782ce-113">インフラストラクチャ見積もりは、次のタイプの環境においてオンプレミスまたはクラウドで使用できます。</span><span class="sxs-lookup"><span data-stu-id="782ce-113">Infrastructure estimates are available for the following types of environments, either on premises or in the cloud.</span></span>
-   <span data-ttu-id="782ce-114">Development 開発者およびバージョン管理システムをサポートする環境の見積もりを作成します。</span><span class="sxs-lookup"><span data-stu-id="782ce-114">DevelopmentCreate an estimate for an environment that supports developers and a version control system.</span></span> <span data-ttu-id="782ce-115">開発環境の見積は、大量のトランザクション負荷をサポートするようには設計されていません。</span><span class="sxs-lookup"><span data-stu-id="782ce-115">The estimate for a development environment is not designed to support a heavy transaction load.</span></span> <span data-ttu-id="782ce-116">この見積では、3 台のコンピューターを想定しています。</span><span class="sxs-lookup"><span data-stu-id="782ce-116">The estimate assumes three computers.</span></span>
-   <span data-ttu-id="782ce-117">実稼働環境の見積を ProductionCreate します。</span><span class="sxs-lookup"><span data-stu-id="782ce-117">ProductionCreate an estimate for a live environment.</span></span> <span data-ttu-id="782ce-118">本番環境の見積は、使用状況プロファイラーで入力した情報に基づいています。</span><span class="sxs-lookup"><span data-stu-id="782ce-118">The estimate for a production environment is based on information that you entered in the Usage profiler.</span></span> <span data-ttu-id="782ce-119">この環境に提供される見積は、大量のビジネス トランザクションと多くのユーザーをサポートします。</span><span class="sxs-lookup"><span data-stu-id="782ce-119">The estimate provided for this environment will support a high volume of business transactions and many users.</span></span>
-   <span data-ttu-id="782ce-120">機能またはパフォーマンス テストをサポートする環境の見積を TestCreate します。</span><span class="sxs-lookup"><span data-stu-id="782ce-120">TestCreate an estimate for an environment that supports functional or performance testing.</span></span> <span data-ttu-id="782ce-121">見積には、最大 4 台のコンピューターを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="782ce-121">The estimate can include up to four computers.</span></span>
-   <span data-ttu-id="782ce-122">Microsoft Dynamics AX でトレーニング ユーザーをサポートする環境の見積もりを作成します。</span><span class="sxs-lookup"><span data-stu-id="782ce-122">TrainingCreate an estimate for an environment that supports training users on Microsoft Dynamics AX.</span></span> <span data-ttu-id="782ce-123">トレーニング環境に提供される見積は、大量のトランザクション負荷をサポートするようには設計されていません。</span><span class="sxs-lookup"><span data-stu-id="782ce-123">The estimate provided for a training environment is not designed to support a heavy transaction load.</span></span> <span data-ttu-id="782ce-124">見積には、最大 4 台のコンピューターを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="782ce-124">The estimate can include up to four computers.</span></span>

## <a name="server-roles"></a><span data-ttu-id="782ce-125">サーバー ロール</span><span class="sxs-lookup"><span data-stu-id="782ce-125">Server roles</span></span>
<span data-ttu-id="782ce-126">サーバー ロールは、Microsoft Dynamics AX 環境の主要なコンポーネントを表します。</span><span class="sxs-lookup"><span data-stu-id="782ce-126">Server roles represent the major components of the Microsoft Dynamics AX environment.</span></span> <span data-ttu-id="782ce-127">各サーバーは、複数のロール要件を満たすために使用できます (たとえば、Analysis Services および Reporting Services を同じコンピュータに配置)。</span><span class="sxs-lookup"><span data-stu-id="782ce-127">Each server can be used to meet multiple role requirements (for example, by putting Analysis Services and Reporting Services on the same computer).</span></span> <span data-ttu-id="782ce-128">インフラストラクチャ見積もりツールでは、各サーバー ロールには、処理能力を事前定義された量が必要です。</span><span class="sxs-lookup"><span data-stu-id="782ce-128">For the purposes of the Infrastructure estimator, each server role requires a predefined amount of processing power.</span></span> <span data-ttu-id="782ce-129">インフラストラクチャ見積もりツールは、環境の各ロールの CPU および RAM 要件を満たす最小サーバーを選択します。</span><span class="sxs-lookup"><span data-stu-id="782ce-129">The Infrastructure estimator selects the smallest server that meets the CPU and RAM requirements for each role in the environment.</span></span> <span data-ttu-id="782ce-130">環境によっては、次のサーバー ロールが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="782ce-130">The following server roles may be required, depending on your environment.</span></span>

| <span data-ttu-id="782ce-131">役割</span><span class="sxs-lookup"><span data-stu-id="782ce-131">Role</span></span>                          | <span data-ttu-id="782ce-132">条件</span><span class="sxs-lookup"><span data-stu-id="782ce-132">Condition</span></span>                                                                                 |
|-------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="782ce-133">AOS</span><span class="sxs-lookup"><span data-stu-id="782ce-133">AOS</span></span>                           | <span data-ttu-id="782ce-134">常に必要です</span><span class="sxs-lookup"><span data-stu-id="782ce-134">Always required</span></span>                                                                           |
| <span data-ttu-id="782ce-135">SQL Server</span><span class="sxs-lookup"><span data-stu-id="782ce-135">SQL Server</span></span>                    | <span data-ttu-id="782ce-136">常に必要です</span><span class="sxs-lookup"><span data-stu-id="782ce-136">Always required</span></span>                                                                           |
| <span data-ttu-id="782ce-137">Terminal Services</span><span class="sxs-lookup"><span data-stu-id="782ce-137">Terminal Services</span></span>             | <span data-ttu-id="782ce-138">リモート運用サイトがある場合に必須</span><span class="sxs-lookup"><span data-stu-id="782ce-138">Required if there is a remote operating site</span></span>                                              |
| <span data-ttu-id="782ce-139">エンタープライズ ポータル</span><span class="sxs-lookup"><span data-stu-id="782ce-139">Enterprise Portal</span></span>             | <span data-ttu-id="782ce-140">使用状況プロファイラーの配置の詳細アンケートで指定されている場合に必須</span><span class="sxs-lookup"><span data-stu-id="782ce-140">Required if it is specified in the Deployment details questionnaire of the Usage profiler</span></span> |
| <span data-ttu-id="782ce-141">エンタープライズ ポータルの AOS</span><span class="sxs-lookup"><span data-stu-id="782ce-141">AOS for Enterprise Portal</span></span>     | <span data-ttu-id="782ce-142">エンタープライズ ポータルが必要な場合に必須</span><span class="sxs-lookup"><span data-stu-id="782ce-142">Required if Enterprise Portal is needed</span></span>                                                   |
| <span data-ttu-id="782ce-143">SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="782ce-143">SQL Server Reporting Services</span></span> | <span data-ttu-id="782ce-144">使用状況プロファイラーの配置の詳細アンケートで指定されている場合に必須</span><span class="sxs-lookup"><span data-stu-id="782ce-144">Required if it is specified in the Deployment details questionnaire of the Usage profiler</span></span> |
| <span data-ttu-id="782ce-145">SQL Server Analysis Services</span><span class="sxs-lookup"><span data-stu-id="782ce-145">SQL Server Analysis Services</span></span>  | <span data-ttu-id="782ce-146">使用状況プロファイラーの配置の詳細アンケートで指定されている場合に必須</span><span class="sxs-lookup"><span data-stu-id="782ce-146">Required if it is specified in the Deployment details questionnaire of the Usage profiler</span></span> |
| <span data-ttu-id="782ce-147">ヘルプ サーバー</span><span class="sxs-lookup"><span data-stu-id="782ce-147">Help server</span></span>                   | <span data-ttu-id="782ce-148">使用状況プロファイラーの配置の詳細アンケートで指定されている場合に必須</span><span class="sxs-lookup"><span data-stu-id="782ce-148">Required if it is specified in the Deployment details questionnaire of the Usage profiler</span></span> |

## <a name="prerequisites"></a><span data-ttu-id="782ce-149">前提条件</span><span class="sxs-lookup"><span data-stu-id="782ce-149">Prerequisites</span></span>
<span data-ttu-id="782ce-150">実稼働環境のインフラストラクチャの見積を作成する場合は、使用状況プロファイルを最初に完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="782ce-150">If you want to create an infrastructure estimate for a production environment, you must first complete a usage profile.</span></span> <span data-ttu-id="782ce-151">詳細については、[使用状況プロファイラー (Lifecycle Services, LCS)](usage-profiler-lcs.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="782ce-151">For more information, see [Usage profiler (Lifecycle Services, LCS)](usage-profiler-lcs.md).</span></span> <span data-ttu-id="782ce-152">開発、テスト、およびトレーニング環境での見積には、完了した使用プロファイルは不要です。</span><span class="sxs-lookup"><span data-stu-id="782ce-152">Estimates for development, test, and training environments do not require a completed usage profile.</span></span>

## <a name="create-an-infrastructure-estimate"></a><span data-ttu-id="782ce-153">インフラストラクチャ見積もりを作成する</span><span class="sxs-lookup"><span data-stu-id="782ce-153">Create an infrastructure estimate</span></span>
1.  <span data-ttu-id="782ce-154">[Lifecycle Services に移動](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="782ce-154">[Go to Lifecycle Services](https://lcs.dynamics.com).</span></span>
2.  <span data-ttu-id="782ce-155">プロジェクトのホーム ページで、インフラストラクチャ見積もりツール タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="782ce-155">On the project home page, click the Infrastructure estimator tile.</span></span>
3.  <span data-ttu-id="782ce-156">実稼働環境の見積が必要であり、利用状況プロファイルをまだ完了していない場合は、使用状況プロファイラー ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="782ce-156">If you need an estimate for a production environment and you haven’t yet completed a usage profile, click the Usage profiler button.</span></span> <span data-ttu-id="782ce-157">詳細については、[使用状況プロファイラー (Lifecycle Services, LCS)](usage-profiler-lcs.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="782ce-157">For more information, see [Usage profiler (Lifecycle Services, LCS)](usage-profiler-lcs.md).</span></span>
4.  <span data-ttu-id="782ce-158">新規見積をクリックします。</span><span class="sxs-lookup"><span data-stu-id="782ce-158">Click New estimate.</span></span>
5.  <span data-ttu-id="782ce-159">見積を作成する環境のタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="782ce-159">Select the type of environment that you are creating an estimate for.</span></span>
6.  <span data-ttu-id="782ce-160">見積名を入力し、社内またはクラウドでは、環境がオンプレミス内またはクラウド内でホストされるかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="782ce-160">Enter a name for the estimate, and select whether the environment will be hosted on premises or in the cloud.</span></span>
7.  <span data-ttu-id="782ce-161">必要に応じて、その他の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="782ce-161">Enter other information as needed.</span></span> <span data-ttu-id="782ce-162">次のテーブルに、選択した環境のタイプに応じて、追加する必要がある可能性のある追加情報について説明します。</span><span class="sxs-lookup"><span data-stu-id="782ce-162">The following table describes the additional information that you may need to provide, depending on the type of environment that you selected.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="782ce-163">環境</span><span class="sxs-lookup"><span data-stu-id="782ce-163">Environment</span></span></th>
    <th><span data-ttu-id="782ce-164">パラメーター</span><span class="sxs-lookup"><span data-stu-id="782ce-164">Parameters</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="782ce-165">開発</span><span class="sxs-lookup"><span data-stu-id="782ce-165">Development</span></span></td>
    <td><ul>
    <li><span data-ttu-id="782ce-166">開発者数</span><span class="sxs-lookup"><span data-stu-id="782ce-166">Number of developers</span></span></li>
    <li><span data-ttu-id="782ce-167">バージョン管理システム</span><span class="sxs-lookup"><span data-stu-id="782ce-167">Version control system</span></span></li>
    </ul></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="782ce-168">実稼働</span><span class="sxs-lookup"><span data-stu-id="782ce-168">Production</span></span></td>
    <td><span data-ttu-id="782ce-169">None</span><span class="sxs-lookup"><span data-stu-id="782ce-169">None</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="782ce-170">テスト</span><span class="sxs-lookup"><span data-stu-id="782ce-170">Test</span></span></td>
    <td><ul>
    <li><span data-ttu-id="782ce-171">テストのタイプ</span><span class="sxs-lookup"><span data-stu-id="782ce-171">Type of testing</span></span></li>
    <li><span data-ttu-id="782ce-172">コンピューターの数。</span><span class="sxs-lookup"><span data-stu-id="782ce-172">Number of computers</span></span></li>
    </ul></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="782ce-173">トレーニング</span><span class="sxs-lookup"><span data-stu-id="782ce-173">Training</span></span></td>
    <td><span data-ttu-id="782ce-174">コンピューターの数。</span><span class="sxs-lookup"><span data-stu-id="782ce-174">Number of computers</span></span></td>
    </tr>
    </tbody>
    </table>

8.  <span data-ttu-id="782ce-175">[作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="782ce-175">Click Create.</span></span>

## <a name="view-infrastructure-estimates"></a><span data-ttu-id="782ce-176">インフラストラクチャの見積もりの表示</span><span class="sxs-lookup"><span data-stu-id="782ce-176">View infrastructure estimates</span></span>
<span data-ttu-id="782ce-177">主要なインフラストラクチャ見積もりツールページで、詳細を表示する見積もりを選択します。</span><span class="sxs-lookup"><span data-stu-id="782ce-177">On the main Infrastructure estimator page, select an estimate to view the details.</span></span>





