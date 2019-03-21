---
title: データベース移動操作ホーム ページ
description: このトピックでは、Lifecycle Services のデータベースの移動機能の使用可能なクイック スタート ガイドおよびチュートリアルへのリンクを示します。
author: laneswenka
manager: AnnBe
ms.date: 01/25/2019
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
ms.openlocfilehash: fe58e65201148702955f9c276dbdb08a4c913ec6
ms.sourcegitcommit: 313e13afe17be45a53ae71bfee20ccb616fca62b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2019
ms.locfileid: "380281"
---
# <a name="database-movement-operations-home-page"></a><span data-ttu-id="d0b5d-103">データベース移動操作ホーム ページ</span><span class="sxs-lookup"><span data-stu-id="d0b5d-103">Database movement operations home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d0b5d-104">データベース移動操作は、データ アプリケーション ライフ サイクル管理 (*DataALM* とも呼ばれます) の一部として使用できる一連のセルフ サービスのアクションです。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-104">Database movement operations are a suite of self-service actions that can be used as part of Data Application Lifecycle Management (also referred to as *DataALM*).</span></span>  <span data-ttu-id="d0b5d-105">これらのアクションは、ゴールデン コンフィギュレーション プロモーション、デバッグ/診断、破壊試験、トレーニング目的での全般的な更新などの一般的な実装シナリオで構造化されたプロセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-105">These actions provide structured processes for common implementation scenarios such as golden configuration promotion, debugging/diagnostics, destructive testing, and general refresh for training purposes.</span></span>

<span data-ttu-id="d0b5d-106">このトピックでは、データベース移動操作を使用して、更新、エクスポート、インポート、およびさまざまなタイプのポイントインタイム復元を実行する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-106">In this topic, you will learn how to use database movement operations to perform refresh, export, import, and various flavors of point-in-time restore.</span></span>

## <a name="database-movement-quick-start-guides"></a><span data-ttu-id="d0b5d-107">データベース移動クイック スタート ガイド</span><span class="sxs-lookup"><span data-stu-id="d0b5d-107">Database movement quick start guides</span></span>
<span data-ttu-id="d0b5d-108">標準またはプレミア受け入れテスト環境で個々の操作を実行する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-108">Learn how to perform the individual operations on your Standard or Premier Acceptance Test environments:</span></span>
 * [<span data-ttu-id="d0b5d-109">データベースの更新</span><span class="sxs-lookup"><span data-stu-id="d0b5d-109">Refresh database</span></span>](database-refresh.md)
 * [<span data-ttu-id="d0b5d-110">データベースのエクスポート</span><span class="sxs-lookup"><span data-stu-id="d0b5d-110">Export a database</span></span>](export-database.md)
 * [<span data-ttu-id="d0b5d-111">データベースのインポート</span><span class="sxs-lookup"><span data-stu-id="d0b5d-111">Import a database</span></span>](import-database.md)
 * [<span data-ttu-id="d0b5d-112">データベース ポイントインタイム復元 (PITR)</span><span class="sxs-lookup"><span data-stu-id="d0b5d-112">Database point-in-time restore (PITR)</span></span>](database-point-in-time-restore.md)

 ## <a name="step-by-step-tutorials"></a><span data-ttu-id="d0b5d-113">ステップバイステップ チュートリアル</span><span class="sxs-lookup"><span data-stu-id="d0b5d-113">Step-by-step tutorials</span></span>
 <span data-ttu-id="d0b5d-114">お客様に合わせて DataALM を使用して実装の一般的なシナリオを達成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-114">Learn how to achieve common implementation scenarios using DataALM to your advantage:</span></span>
 * [<span data-ttu-id="d0b5d-115">トレーニング用の更新</span><span class="sxs-lookup"><span data-stu-id="d0b5d-115">Refresh for training purposes</span></span>](dbmovement-scenario-general-refresh.md)
 * [<span data-ttu-id="d0b5d-116">デバッグおよび診断</span><span class="sxs-lookup"><span data-stu-id="d0b5d-116">Debugging and diagnostics</span></span>](dbmovement-scenario-debugdiag.md)
 * [<span data-ttu-id="d0b5d-117">ゴールデン コンフィギュレーション プロモーション</span><span class="sxs-lookup"><span data-stu-id="d0b5d-117">Golden configuration promotion</span></span>](dbmovement-scenario-goldenconfig.md)
 * [<span data-ttu-id="d0b5d-118">破壊試験</span><span class="sxs-lookup"><span data-stu-id="d0b5d-118">Destructive testing</span></span>](dbmovement-scenario-destructivetests.md)
 
 > [!Important]
 > <span data-ttu-id="d0b5d-119">ポイントインタイム復元の新機能と、RESTful API は、プライベート プレビューです。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-119">New features around point-in-time restore, and RESTful APIs are in private preview.</span></span> <span data-ttu-id="d0b5d-120">プライベート プレビュー プログラムに登録するには、[プライベート プレビュー アンケート](https://aka.ms/SelfServiceDatabaseMovementPreview)に記入してください。</span><span class="sxs-lookup"><span data-stu-id="d0b5d-120">To sign up for the private preview program, please [complete the private preview survey](https://aka.ms/SelfServiceDatabaseMovementPreview).</span></span>
