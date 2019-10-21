---
title: データベース移動操作ホーム ページ
description: このトピックでは、Lifecycle Services のデータベースの移動機能の使用可能なクイック スタート ガイドおよびチュートリアルへのリンクを示します。
author: laneswenka
manager: AnnBe
ms.date: 03/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: b2bc1eb8bf05ec3dd112ce245e1113b3b45316dd
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183462"
---
# <a name="database-movement-operations-home-page"></a><span data-ttu-id="394d9-103">データベース移動操作ホーム ページ</span><span class="sxs-lookup"><span data-stu-id="394d9-103">Database movement operations home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="394d9-104">データベース移動操作は、データ アプリケーション ライフ サイクル管理 (*DataALM* とも呼ばれます) の一部として使用できる一連のセルフ サービスのアクションです。</span><span class="sxs-lookup"><span data-stu-id="394d9-104">Database movement operations are a suite of self-service actions that can be used as part of Data Application Lifecycle Management (also referred to as *DataALM*).</span></span>  <span data-ttu-id="394d9-105">これらのアクションは、ゴールデン コンフィギュレーション プロモーション、デバッグ/診断、破壊試験、トレーニング目的での全般的な更新などの一般的な実装シナリオで構造化されたプロセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="394d9-105">These actions provide structured processes for common implementation scenarios such as golden configuration promotion, debugging/diagnostics, destructive testing, and general refresh for training purposes.</span></span>

<span data-ttu-id="394d9-106">このトピックでは、データベース移動操作を使用して、更新、エクスポート、インポート、およびさまざまなタイプのポイントインタイム復元を実行する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="394d9-106">In this topic, you will learn how to use database movement operations to perform refresh, export, import, and various flavors of point-in-time restore.</span></span>

## <a name="database-movement-quick-start-guides"></a><span data-ttu-id="394d9-107">データベース移動クイック スタート ガイド</span><span class="sxs-lookup"><span data-stu-id="394d9-107">Database movement quick start guides</span></span>
<span data-ttu-id="394d9-108">標準またはプレミア受け入れテスト環境で個々の操作を実行する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="394d9-108">Learn how to perform the individual operations on your Standard or Premier Acceptance Test environments:</span></span>
 * [<span data-ttu-id="394d9-109">データベースの更新</span><span class="sxs-lookup"><span data-stu-id="394d9-109">Refresh database</span></span>](database-refresh.md)
 * [<span data-ttu-id="394d9-110">データベースのエクスポート</span><span class="sxs-lookup"><span data-stu-id="394d9-110">Export a database</span></span>](export-database.md)
 * [<span data-ttu-id="394d9-111">データベースのインポート</span><span class="sxs-lookup"><span data-stu-id="394d9-111">Import a database</span></span>](import-database.md)
 * [<span data-ttu-id="394d9-112">データベース ポイントインタイム復元 (PITR)</span><span class="sxs-lookup"><span data-stu-id="394d9-112">Database point-in-time restore (PITR)</span></span>](database-point-in-time-restore.md)

 ## <a name="step-by-step-tutorials"></a><span data-ttu-id="394d9-113">ステップバイステップ チュートリアル</span><span class="sxs-lookup"><span data-stu-id="394d9-113">Step-by-step tutorials</span></span>
 <span data-ttu-id="394d9-114">お客様に合わせて DataALM を使用して実装の一般的なシナリオを達成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="394d9-114">Learn how to achieve common implementation scenarios using DataALM to your advantage:</span></span>
 * [<span data-ttu-id="394d9-115">トレーニング用の更新</span><span class="sxs-lookup"><span data-stu-id="394d9-115">Refresh for training purposes</span></span>](dbmovement-scenario-general-refresh.md)
 * [<span data-ttu-id="394d9-116">生産データベースのコピーのデバッグ</span><span class="sxs-lookup"><span data-stu-id="394d9-116">Debug a copy of the production database</span></span>](dbmovement-scenario-debugdiag.md)
 * [<span data-ttu-id="394d9-117">標準ユーザー受け入れテスト (UAT) データベースのコピーのエクスポート</span><span class="sxs-lookup"><span data-stu-id="394d9-117">Export a copy of the Standard User Acceptance Test (UAT) database</span></span>](dbmovement-scenario-exportuat.md)
 * [<span data-ttu-id="394d9-118">ゴールデン コンフィギュレーション プロモーション</span><span class="sxs-lookup"><span data-stu-id="394d9-118">Golden configuration promotion</span></span>](dbmovement-scenario-goldenconfig.md)
 * [<span data-ttu-id="394d9-119">破壊試験</span><span class="sxs-lookup"><span data-stu-id="394d9-119">Destructive testing</span></span>](dbmovement-scenario-destructivetests.md)
 
 > [!IMPORTANT]
 > <span data-ttu-id="394d9-120">ポイントインタイム復元の新機能と、RESTful API は、プライベート プレビューです。</span><span class="sxs-lookup"><span data-stu-id="394d9-120">New features around point-in-time restore, and RESTful APIs are in private preview.</span></span> <span data-ttu-id="394d9-121">プライベート プレビュー プログラムに登録するには、[プライベート プレビュー アンケート](https://aka.ms/SelfServiceDatabaseMovementPreview)に記入してください。</span><span class="sxs-lookup"><span data-stu-id="394d9-121">To sign up for the private preview program, please [complete the private preview survey](https://aka.ms/SelfServiceDatabaseMovementPreview).</span></span>
