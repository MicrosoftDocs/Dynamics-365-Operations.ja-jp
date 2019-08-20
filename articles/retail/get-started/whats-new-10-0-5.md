---
title: Dynamics 365 for Retail バージョン 10.0.5 の機能をプレビューする
description: このトピックでは Dynamics 365 for Retail のプレビュー中の機能について説明します。
author: josaw1
manager: AnnBe
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-retail
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-08-02
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 99227b40d368c7cd278608253b543f8a05dffac9
ms.sourcegitcommit: 299e20b59ebefa584ed46a13da3f1a7ff709e43c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2019
ms.locfileid: "1863646"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-retail-version-1005"></a><span data-ttu-id="8e0f1-103">Dynamics 365 for Retail バージョン 10.0.5 の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="8e0f1-103">What's new or changed in Dynamics 365 for Retail version 10.0.5</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8e0f1-104">このトピックでは、Microsoft Dynamics 365 for Retail 10.0.5 の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="8e0f1-104">This topic describes features that are new or changed in Microsoft Dynamics 365 for Retail in 10.0.5.</span></span> 

<span data-ttu-id="8e0f1-105">Microsoft Dynamics 365 for Finance and Operations の機能の詳細については、 [Finance and Operations バージョン 10.0.5 (2019 年 10 月) の機能のプレビュー](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-changed-10-0-5). を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8e0f1-105">To learn about the features in Microsoft Dynamics 365 for Finance and Operations, see [Preview features in Finance and Operations version 10.0.5 (October 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-changed-10-0-5).</span></span>

## <a name="test-recorder-and-regression-suite-automation-tool-for-retail-cloud-pos"></a><span data-ttu-id="8e0f1-106">Retail Cloud POS 用のレコーダーおよRegression Suite Automation Tool のテスト</span><span class="sxs-lookup"><span data-stu-id="8e0f1-106">Test recorder and Regression suite automation tool for Retail Cloud POS</span></span>
  
### <a name="test-recorder"></a><span data-ttu-id="8e0f1-107">テスト レコーダー</span><span class="sxs-lookup"><span data-stu-id="8e0f1-107">Test recorder</span></span>
<span data-ttu-id="8e0f1-108">テストレコーダーは、ユーザー受け入れテストの時間と費用を大幅に削減するために POS に追加された新機能です。</span><span class="sxs-lookup"><span data-stu-id="8e0f1-108">Test recorder is a new feature added in POS to significantly reduce the time and cost of user acceptance testing.</span></span> <span data-ttu-id="8e0f1-109">通常、ユーザー受け入れテストは Microsoft アプリケーションの更新をおこなうか、カスタム コードと構成を自分の Retail POS 生産環境に適用することが求められます。</span><span class="sxs-lookup"><span data-stu-id="8e0f1-109">User acceptance testing is typically required before taking a Microsoft application update or applying custom code and configurations to your Retail POS production environments.</span></span> <span data-ttu-id="8e0f1-110">テストレコーダーでは、POS のすべてのコントロールおよび配布された注文管理 (DOM) 要素の正確な再現性をもって、クライアントにユーザーのアクションを記録できます。</span><span class="sxs-lookup"><span data-stu-id="8e0f1-110">Test recorder can record user actions in the client with exact fidelity for all the controls and distributed order management (DOM) elements in POS.</span></span> <span data-ttu-id="8e0f1-111">テストレコーダーは、イベントが発生した時を取得し、該当するユーザー アクションに関するすべての関連情報をリアルタイムで保存します。</span><span class="sxs-lookup"><span data-stu-id="8e0f1-111">Test recorder captures when the event occurred and stores all pertinent information about the corresponding user action in real time.</span></span> <span data-ttu-id="8e0f1-112">テスト レコーダーは、この情報からユーザー アクションのタイプ (ボタンのクリック、値の入力、ナビゲーションなど) と、ユーザー アクションに関連するデータ (入力データの値とタイプ、フォーム コンテキスト、レコード コンテキストなど) をキャプチャできます。</span><span class="sxs-lookup"><span data-stu-id="8e0f1-112">From this information, test recorder can capture the type of user action (such as a button click, value entry, or navigation) and any data that is related to the user action, such as the input data value and type, view context, or record context.</span></span> <span data-ttu-id="8e0f1-113">(パスワード情報は記録されません)。</span><span class="sxs-lookup"><span data-stu-id="8e0f1-113">(Password information is not recorded).</span></span> <span data-ttu-id="8e0f1-114">テストレコーダーは、録画中にメモリ内のすべてのレコーダー情報を保持し、記録の最後に出力ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="8e0f1-114">Test recorder persists all the recorder information in memory during the recording and generates an output file at the end of the recording.</span></span> <span data-ttu-id="8e0f1-115">この出力ファイルには、ユーザーが実行した正確なアクションを使用して、後で RSAT ツールを使用して再生するのに役立てるために十分な詳細な情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="8e0f1-115">This output file has enough detail to help playback later using the RSAT tool, using the exact actions that the user performed.</span></span>

> [!NOTE]
> <span data-ttu-id="8e0f1-116">テスト レコーダーは、Chrome ブラウザーを使用て Cloud POS のみでサポートされ、他のブラウザーやデバイスタイプのサポートは後で追加されます。</span><span class="sxs-lookup"><span data-stu-id="8e0f1-116">Test recorder is supported only in Cloud POS using Chrome browser, support for other browsers and device types will be added later.</span></span>

<span data-ttu-id="8e0f1-117">[![テスト レコーダー](.././media/CreateTest.png)](.././media/CreateTest.png)</span><span class="sxs-lookup"><span data-stu-id="8e0f1-117">[![Test recorder](.././media/CreateTest.png)](.././media/CreateTest.png)</span></span>

### <a name="regression-suite-automation-tool"></a><span data-ttu-id="8e0f1-118">Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="8e0f1-118">Regression suite Automation Tool</span></span>
<span data-ttu-id="8e0f1-119">Regression Suite Automation Tool (RSAT) を使用すると、機能パワーユーザーは Retail POS でテストケースを実行し、テストの実行 Azure DevOps 結果をレポートおよび調査に対して再度更新できます。</span><span class="sxs-lookup"><span data-stu-id="8e0f1-119">The Regression suite automation tool (RSAT) enables functional power users to execute the test case in Retail POS and update the test execution result back in Azure DevOps for reporting and investigation.</span></span> <span data-ttu-id="8e0f1-120">RSAT には、テストの失敗を調査するためのオプションが用意されています。</span><span class="sxs-lookup"><span data-stu-id="8e0f1-120">RSAT provides options to investigate the test failures.</span></span> <span data-ttu-id="8e0f1-121">RSAT では、テストパラメーターをテストステップから切り離し、Microsoft Excel でパラメーターをファイルに格納して、テストパラメーター値を簡単に編集できるようにします。</span><span class="sxs-lookup"><span data-stu-id="8e0f1-121">RSAT decouples the test parameters from test steps and stores the parameters in Microsoft Excel files for easy editing of the test parameter values.</span></span> <span data-ttu-id="8e0f1-122">これで、RSATツールは Retail POS タブで更新され、Retail POS の記録を再生し、小売パラメーターと変数ファイルを生成するための小売固有の設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="8e0f1-122">The RSAT tool is now updated with a Retail POS tab to specify the Retail specific settings to play back Retail POS recordings and generate retail parameters and variable files.</span></span>

<span data-ttu-id="8e0f1-123">[![POS 再生環境設定](.././media/Setting.png)](.././media/Setting.png)</span><span class="sxs-lookup"><span data-stu-id="8e0f1-123">[![POS playback environement setting](.././media/Setting.png)](.././media/Setting.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8e0f1-124">追加リソース</span><span class="sxs-lookup"><span data-stu-id="8e0f1-124">Additional resources</span></span>

### <a name="dynamics-365-2019-release-wave-2-plan"></a><span data-ttu-id="8e0f1-125">Dynamics 365: 2019 リリースのウェーブ 2 プラン</span><span class="sxs-lookup"><span data-stu-id="8e0f1-125">Dynamics 365: 2019 release wave 2 plan</span></span>

<span data-ttu-id="8e0f1-126">当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?</span><span class="sxs-lookup"><span data-stu-id="8e0f1-126">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="8e0f1-127">[Dynamics 365: 2019 リリース ウェーブ 2 プラン](https://docs.microsoft.com/en-us/dynamics365-release-plan/2019wave2/index) をご確認ください。</span><span class="sxs-lookup"><span data-stu-id="8e0f1-127">Check out the [Dynamics 365: 2019 release wave 2 plan](https://docs.microsoft.com/en-us/dynamics365-release-plan/2019wave2/index).</span></span> <span data-ttu-id="8e0f1-128">あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。</span><span class="sxs-lookup"><span data-stu-id="8e0f1-128">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>
