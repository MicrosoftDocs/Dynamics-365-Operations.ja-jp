---
title: データ入力を容易にするレコード テンプレートの作成
description: このトピックでは、レコード テンプレートの作成して、よく使用されるフィールド値を新しいレコードごとに明示的に入力する必要がないようにする方法を示します。
author: margoc
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, SysRecordInfo, SysRecordTemplatePromptOnCreate
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 08ee7d0f0ce7e92eaa85137dcd2761bfd702eb8c
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/08/2019
ms.locfileid: "1866931"
---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="9e707-103">データ入力を容易にするレコード テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="9e707-103">Create a record template to facilitate data entry</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9e707-104">このトピックでは、レコード テンプレートの作成して、よく使用されるフィールド値を新しいレコードごとに明示的に入力する必要がないようにする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="9e707-104">This topic demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="9e707-105">この手順では、固定資産に追加する必要がある新しいラップトップのレコードを新規作成します。</span><span class="sxs-lookup"><span data-stu-id="9e707-105">In this procedure, you’ll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="9e707-106">この手順では、USMF というサンプル会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="9e707-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="9e707-107">ナビゲーション ウィンドウで、**モジュール > 固定資産 > 固定資産 > 固定資産**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9e707-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="9e707-108">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e707-108">Select **New**.</span></span>
3. <span data-ttu-id="9e707-109">**固定資産グループ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9e707-109">In the **Fixed asset group** field, enter or select a value.</span></span>
4. <span data-ttu-id="9e707-110">**名前**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9e707-110">In the **Name** field, type a value.</span></span> <span data-ttu-id="9e707-111">たとえば、**企業潜在顧客のラップトップ**と入力します。</span><span class="sxs-lookup"><span data-stu-id="9e707-111">For example, enter **Corporate lead laptop**.</span></span>  
5. <span data-ttu-id="9e707-112">**検索名**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9e707-112">In the **Search name** field, type a value.</span></span> <span data-ttu-id="9e707-113">たとえば、**ラップトップ**と入力します。</span><span class="sxs-lookup"><span data-stu-id="9e707-113">For example, enter **laptop**.</span></span>  
6. <span data-ttu-id="9e707-114">**技術情報**セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="9e707-114">Expand the **Technical information** section.</span></span>
7. <span data-ttu-id="9e707-115">**メーカー**、**モデル**、および**年式**フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9e707-115">In the **Make**, **Model**, and **Model year** fields, type values.</span></span>
8. <span data-ttu-id="9e707-116">アクション ウィンドウで、**オプション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e707-116">On the Action Pane, select **Options**.</span></span>
9. <span data-ttu-id="9e707-117">**レコード情報**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e707-117">Select **Record info**.</span></span>
10. <span data-ttu-id="9e707-118">**ユーザー テンプレート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e707-118">Select **User template**.</span></span>
11. <span data-ttu-id="9e707-119">**名前**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9e707-119">In the **Name** field, type a value.</span></span>
12. <span data-ttu-id="9e707-120">**説明**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9e707-120">In the **Description** field, type a value.</span></span>
13. <span data-ttu-id="9e707-121">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e707-121">Select **OK**.</span></span>
14. <span data-ttu-id="9e707-122">**閉じる**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e707-122">Select **Close**.</span></span>

