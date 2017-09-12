---
title: "簡易インポート/エクスポートの使用"
description: "簡易インポート/エクスポートの目的は、より少ない手順でインポートとエクスポートを実行できるようにすることです。"
author: margoc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: ax-2012
audience: Application User
ms.reviewer: margoc
ms.search.scope: AX 2012 R3 CU8, UnifiedOperations
ms.custom: 89041
ms.assetid: 990d64e6-d436-4c79-9bb5-bf8c5c5a048f
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 
ms.dyn365.ops.version: AX 2012 R3 CU8
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 121d8f757e2d5453308d8846bd299f3db339db67
ms.contentlocale: ja-jp
ms.lasthandoff: 07/18/2017

---

# <a name="run-the-test-data-transfer-tool-beta-for-dynamics-ax-ax-2012"></a><span data-ttu-id="64a85-103">Dynamics AX (AX 2012) 用のテスト データ転送ツール (ベータ版) の実行</span><span class="sxs-lookup"><span data-stu-id="64a85-103">Run the Test Data Transfer Tool (beta) for Dynamics AX (AX 2012)</span></span>

[!include[banner](../../includes/banner.md)]


<span data-ttu-id="64a85-104">簡易インポート/エクスポートの目的は、より少ない手順でインポートとエクスポートを実行できるようにすることです。</span><span class="sxs-lookup"><span data-stu-id="64a85-104">The purpose of Quick import export is to let you import and export with fewer steps.</span></span>

<span data-ttu-id="64a85-105">ユーザーがインポートまたはエクスポートの簡易なジョブを迅速に実行できるよう [簡易インポート/エクスポート] 機能を追加しました。</span><span class="sxs-lookup"><span data-stu-id="64a85-105">We added the Quick Import Export feature to let users import or export simple jobs that they want to execute quickly.</span></span> <span data-ttu-id="64a85-106">原則的にこの機能は、ファイルがシステムに自動的にマップしており、ユーザーは高度なマッピングを行ったりインポートまたはエクスポート ジョブを繰り返し作成する必要はない、というシナリオ内で使用します。</span><span class="sxs-lookup"><span data-stu-id="64a85-106">Ideally this feature is used in scenarios in which a file automatically maps to the system and user does not need to go through advanced mapping or create repeated import or export jobs.</span></span>

-   <span data-ttu-id="64a85-107">この機能は、追加設定なしでの使用、さらにカスタム エンティティ両方の操作をサポートします。</span><span class="sxs-lookup"><span data-stu-id="64a85-107">This feature supports working with both out-of-the-box and custom entities.</span></span>
-   <span data-ttu-id="64a85-108">ファイルからインポートすることができ、ODBC データ ソースを使用している場合は、インポートを定義するクエリを選択します。</span><span class="sxs-lookup"><span data-stu-id="64a85-108">You can import from files, and if you are using an ODBC data source, you can select a query to use to define your import.</span></span>
-   <span data-ttu-id="64a85-109">AX またはファイルのいずれかのソース データ形式を事前に定義しておく必要があり、それらの場所が決まっています。</span><span class="sxs-lookup"><span data-stu-id="64a85-109">You must have previously defined source data formats for either AX or File, and know where they are located.</span></span>
-   <span data-ttu-id="64a85-110">簡易インポート/エクスポートを使用するために処理グループを作成する必要はありません。それはインポートまたはエクスポート ジョブを実行するとき自動的にシステムにより作成されます。</span><span class="sxs-lookup"><span data-stu-id="64a85-110">You do not need to create a processing group to use quick import/export, one will be automatically created by the system when executing the import or export job.</span></span> <span data-ttu-id="64a85-111">簡易インポート/エクスポートによりインポートされたデータの履歴を保存するよう選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="64a85-111">You can also choose keep the history of the data imported by the quick import/export.</span></span>

  <span data-ttu-id="64a85-112">簡易インポート/エクスポートは、DIXF の概念に精通しているという前提で使用するように注意してください。</span><span class="sxs-lookup"><span data-stu-id="64a85-112">Note that Quick import export assumes that you are familiar with the concepts of DIXF.</span></span>




