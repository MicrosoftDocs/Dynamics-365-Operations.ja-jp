---
title: 破壊試験
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations の破壊テスト シナリオについて説明します。
author: LaneSwenka
manager: AnnBe
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro, Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: laneswenka
ms.search.validFrom: 2019-01-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: dfdb21f6a0c6194e474010acaca20c0f78a5d582
ms.sourcegitcommit: 0c1deb100d0bf6dacd14b328968bbc7a9d92583a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/28/2019
ms.locfileid: "771269"
---
# <a name="destructive-testing"></a><span data-ttu-id="d4af0-103">破壊試験</span><span class="sxs-lookup"><span data-stu-id="d4af0-103">Destructive testing</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d4af0-104">データベース移動操作は、データ アプリケーション ライフ サイクル管理 (DataALM) の一部として使用できる一連のセルフ サービスのアクションです。</span><span class="sxs-lookup"><span data-stu-id="d4af0-104">Database movement operations are a suite of self-service actions that can be used as part of data application lifecycle management (DataALM).</span></span> <span data-ttu-id="d4af0-105">場合によっては、環境で破壊試験を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d4af0-105">In some situations,  destructive testing must be done on an environment.</span></span> <span data-ttu-id="d4af0-106">このコンテキストでは、破壊試験は、環境を継続的なテストに使用できなくなったと宣言することを意味します。</span><span class="sxs-lookup"><span data-stu-id="d4af0-106">In this context, destructive testing means that the environment is rendered no longer useful for continued testing.</span></span> <span data-ttu-id="d4af0-107">破壊試験は、会議室パイロット中の実装ライフ サイクルでは一般的です。</span><span class="sxs-lookup"><span data-stu-id="d4af0-107">Destructive testing is typical in an implementation lifecycle during Conference Room Pilots.</span></span> <span data-ttu-id="d4af0-108">このチュートリアルでは、破壊試験を容易にするデータベース移動操作の使用方法を示します。</span><span class="sxs-lookup"><span data-stu-id="d4af0-108">This tutorial shows how to use database movement operations to facilitate destructive testing.</span></span>

<span data-ttu-id="d4af0-109">このチュートリアルでは、2 つの操作について説明します。</span><span class="sxs-lookup"><span data-stu-id="d4af0-109">In this tutorial, you will learn two approaches:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="d4af0-110">データベース バックアップ資産を使用します。</span><span class="sxs-lookup"><span data-stu-id="d4af0-110">Use a database backup asset.</span></span>
> * <span data-ttu-id="d4af0-111">ポイントインタイム復元を使用します。</span><span class="sxs-lookup"><span data-stu-id="d4af0-111">Use point-in-time restore.</span></span>

<span data-ttu-id="d4af0-112">このシナリオの例として、顧客は会議室パイロットを実行しようとしており、トランザクションがない (つまり、販売注文や発注書がない) 環境で開始します。</span><span class="sxs-lookup"><span data-stu-id="d4af0-112">As an example of this scenario, a customer wants to do a Conference Room Pilot and wants to start with an environment that has no transactions (that is, no sales orders or purchase orders).</span></span> <span data-ttu-id="d4af0-113">顧客は、同じパイロットを行うために、ユーザーの地域間で物理的な倉庫から物理的な倉庫に移動し、各パイロットが行われる前に、環境を「リセット」することを希望しています。</span><span class="sxs-lookup"><span data-stu-id="d4af0-113">The customer will be traveling from physical warehouse to physical warehouse throughout his or her geographic region to do the same pilot, and wants the environment to be "reset" before each pilot is done.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d4af0-114">必要条件</span><span class="sxs-lookup"><span data-stu-id="d4af0-114">Prerequisites</span></span>

<span data-ttu-id="d4af0-115">このチュートリアルを完了するには、プロジェクトに標準ユーザー受け入れテスト (UAT) 環境が展開されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="d4af0-115">To complete this tutorial, you must have a standard user acceptance testing (UAT) environment deployed in your project.</span></span>

## <a name="using-a-database-backup"></a><span data-ttu-id="d4af0-116">データベースのバックアップの使用</span><span class="sxs-lookup"><span data-stu-id="d4af0-116">Using a database backup</span></span>

<span data-ttu-id="d4af0-117">すでにテストの準備ができているデータベース バックアップ (.bacpac) ファイルがある場合、最も簡単な方法は、バックアップ ファイルを LCS プロジェクトの資産ライブラリ内の**データベース バックアップ**セクションにアップロードすることです。</span><span class="sxs-lookup"><span data-stu-id="d4af0-117">If you've prepared a database backup (.bacpac) file that is already at the starting point for the test, the easiest approach is to upload the backup file to the **Database backup** section in your LCS project's Asset Library.</span></span> <span data-ttu-id="d4af0-118">その後、ここで説明するように、対象となる環境にインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="d4af0-118">It can then be imported to your target environment as described here.</span></span>

[!include [dbmovement-import](../includes/dbmovement-import.md)]

### <a name="database-backup-pros-and-cons"></a><span data-ttu-id="d4af0-119">データベース バックアップの長所と短所</span><span class="sxs-lookup"><span data-stu-id="d4af0-119">Database backup pros and cons</span></span>

<span data-ttu-id="d4af0-120">バックアップ ファイル資産を使用する利点は、テストの開始点に戻るために、同じファイルのインポートを保持できることです。</span><span class="sxs-lookup"><span data-stu-id="d4af0-120">The advantage of using backup file assets is that you can keep importing the same file to get back to the starting point for the test.</span></span>

<span data-ttu-id="d4af0-121">デメリットは、インポートが完了する前かつユーザーが開始できるようになった後に多くの構成 (バッチ ジョブなど) を設定する必要がある場合、各破壊テスト セッションの前により多くの作業が必要になる点です。</span><span class="sxs-lookup"><span data-stu-id="d4af0-121">The disadvantage is that if many configurations (for example, batch jobs) must be set after the import is completed but before users can begin, more effort will be required before each destructive testing session.</span></span>

## <a name="using-point-in-time-restore"></a><span data-ttu-id="d4af0-122">ポイントインタイム復元の使用</span><span class="sxs-lookup"><span data-stu-id="d4af0-122">Using point-in-time restore</span></span>

<span data-ttu-id="d4af0-123">データベース バックアップ (.bacpac) ファイルで開始しなかった場合に、正常な状態であることがわかっている UAT 環境がある場合、自分のタイムゾーンの日時を記録できます。</span><span class="sxs-lookup"><span data-stu-id="d4af0-123">If you didn't start with a database backup (.bacpac) file but instead have the UAT environment in a known good state, you can just record the date and time in your time zone.</span></span> <span data-ttu-id="d4af0-124">その後、破壊試験を開始できます。</span><span class="sxs-lookup"><span data-stu-id="d4af0-124">You can then begin the destructive testing.</span></span> <span data-ttu-id="d4af0-125">次に、テストが完了したら、、次の手順を使用して、前の時点の環境を復元できます。</span><span class="sxs-lookup"><span data-stu-id="d4af0-125">Then, when the testing is completed, you can restore the environment to the previous time by using the following steps.</span></span>

[!include [dbmovement-import](../includes/dbmovement-pitr.md)]

### <a name="point-in-time-restore-pros-and-cons"></a><span data-ttu-id="d4af0-126">ポイントインタイム復元のメリットとデメリット</span><span class="sxs-lookup"><span data-stu-id="d4af0-126">Point-in-time restore pros and cons</span></span>

<span data-ttu-id="d4af0-127">ポイントタイム復元を使用する利点は、データベース バックアップ (.bacpac) ファイルの処理を回避できるため、破壊テスト セッションの間の時間を短縮できることです。</span><span class="sxs-lookup"><span data-stu-id="d4af0-127">The advantage of using point-in-time-restore is that you can avoid dealing with database backup (.bacpac) files and can reduce the time between destructive testing sessions.</span></span>

<span data-ttu-id="d4af0-128">デメリットは、ポイントインタイム復元の現在の制限により、復元が完了した後に新しい復元の日時を記録する必要があることです。</span><span class="sxs-lookup"><span data-stu-id="d4af0-128">The disadvantage is that, because of current limitations of point-in-time restore, you must record a new restore date and time in your time zone after the restore is completed.</span></span> <span data-ttu-id="d4af0-129">ポイントインタイム復元では常に新しいデータベースが作成されるため、使用された元の日時は新しいデータベースの復元ポイントとして使用できません。</span><span class="sxs-lookup"><span data-stu-id="d4af0-129">Because point-in-time restore always creates a new database, the original date and time that were used won't be available as a restore point on the new database.</span></span>
