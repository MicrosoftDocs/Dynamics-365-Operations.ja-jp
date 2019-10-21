---
title: ワークフロー メッセージ処理バッチ ジョブの重要なものとしてのコンフィギュレーション
description: ワークフロー メッセージ処理バッチ ジョブの重要なものとしてのコンフィギュレーション
author: aneesmsft
manager: AnnBe
ms.date: 05/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.assetid: 9dc45189-6e7e-4207-ad78-dbbb644dd1ce
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2017-05-19
ms.dyn365.ops.version: Platform update 6
ms.openlocfilehash: d7bb1089d7fcb4da7cda91ba480065c3483a1a57
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191714"
---
# <a name="configure-the-workflow-message-processing-batch-job-as-critical"></a><span data-ttu-id="7d936-103">ワークフロー メッセージ処理バッチ ジョブの重要なものとしてのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="7d936-103">Configure the Workflow message processing batch job as critical</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d936-104">ワークフロー システムでは、さまざまなバッチ ジョブを使用します。</span><span class="sxs-lookup"><span data-stu-id="7d936-104">The workflow system uses various batch jobs.</span></span> <span data-ttu-id="7d936-105">**ワークフロー メッセージ処理**は、ワークフロー メッセージを処理するために使用される重要なバッチ ジョブです。</span><span class="sxs-lookup"><span data-stu-id="7d936-105">**Workflow message processing** is an important batch job used to process workflow messages.</span></span> <span data-ttu-id="7d936-106">ワークフローが組織の重要なコンポーネントである場合は、**ワークフロー メッセージ処理**バッチ ジョブを重要なものとして構成することを検討する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d936-106">If workflow is a key component of your organization, you should consider configuring the **Workflow message processing** batch job as critical.</span></span>

<span data-ttu-id="7d936-107">**処理中のワークフロー メッセージ** バッチジョブを重要なものとしてコンフィギュレーションすることにより、システムはその状態を積極的に追跡します。</span><span class="sxs-lookup"><span data-stu-id="7d936-107">Configuring the **Workflow message processing** batch job as critical ensures that the system actively tracks its status.</span></span> <span data-ttu-id="7d936-108">重要なバッチ ジョブが失敗したとき、サポート チームは、不具合の原因となった可能性のある問題を解決するために、不具合をよく観察して措置を講じることができます。</span><span class="sxs-lookup"><span data-stu-id="7d936-108">When a critical batch job fails, the support team can better monitor failures and take action to resolve any issues that may have caused the failure.</span></span>

<span data-ttu-id="7d936-109">**ワークフロー メッセージ処理**バッチ ジョブを重要なものとしてコンフィギュレーションするには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7d936-109">Follow these steps to configure the **Workflow message processing** batch job as critical.</span></span>

1. <span data-ttu-id="7d936-110">**バッチ ジョブ** ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="7d936-110">Navigate to the **Batch jobs** page.</span></span>
2. <span data-ttu-id="7d936-111">クイック フィルターを使用して**ワークフロー メッセージ処理**を検索します。</span><span class="sxs-lookup"><span data-stu-id="7d936-111">Search for **Workflow message processing** using the quick filter.</span></span>
3. <span data-ttu-id="7d936-112">**ワークフロー メッセージ処理** バッチ ジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="7d936-112">Select the **Workflow message processing** batch job.</span></span>
4. <span data-ttu-id="7d936-113">アクション ウィンドウの**編集**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d936-113">Click **Edit** in the action pane.</span></span>
5. <span data-ttu-id="7d936-114">**重要なジョブ** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="7d936-114">Select the **Critical Job** check box.</span></span>
6. <span data-ttu-id="7d936-115">アクション ウィンドウの**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d936-115">Click **Save** in the action pane.</span></span>
