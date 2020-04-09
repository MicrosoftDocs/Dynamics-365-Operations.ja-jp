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
ms.openlocfilehash: ec21415158ad611d0ad55778e76aa128f53561bd
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143387"
---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="d49b1-103">データ入力を容易にするレコード テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="d49b1-103">Create a record template to facilitate data entry</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d49b1-104">このトピックでは、レコード テンプレートの作成して、よく使用されるフィールド値を新しいレコードごとに明示的に入力する必要がないようにする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="d49b1-104">This topic demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="d49b1-105">この手順では、固定資産に追加する必要がある新しいラップトップのレコードを新規作成します。</span><span class="sxs-lookup"><span data-stu-id="d49b1-105">In this procedure, you'll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="d49b1-106">この手順では、USMF というサンプル会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="d49b1-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="d49b1-107">ナビゲーション ウィンドウで、**モジュール > 固定資産 > 固定資産 > 固定資産**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d49b1-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="d49b1-108">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d49b1-108">Select **New**.</span></span>
3. <span data-ttu-id="d49b1-109">**固定資産グループ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="d49b1-109">In the **Fixed asset group** field, enter or select a value.</span></span>
4. <span data-ttu-id="d49b1-110">**名前**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d49b1-110">In the **Name** field, type a value.</span></span> <span data-ttu-id="d49b1-111">たとえば、**企業潜在顧客のラップトップ**と入力します。</span><span class="sxs-lookup"><span data-stu-id="d49b1-111">For example, enter **Corporate lead laptop**.</span></span>  
5. <span data-ttu-id="d49b1-112">**検索名**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d49b1-112">In the **Search name** field, type a value.</span></span> <span data-ttu-id="d49b1-113">たとえば、**ラップトップ**と入力します。</span><span class="sxs-lookup"><span data-stu-id="d49b1-113">For example, enter **laptop**.</span></span>  
6. <span data-ttu-id="d49b1-114">**技術情報**セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="d49b1-114">Expand the **Technical information** section.</span></span>
7. <span data-ttu-id="d49b1-115">**メーカー**、**モデル**、および**年式**フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d49b1-115">In the **Make**, **Model**, and **Model year** fields, type values.</span></span>
8. <span data-ttu-id="d49b1-116">アクション ウィンドウで、**オプション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d49b1-116">On the Action Pane, select **Options**.</span></span>
9. <span data-ttu-id="d49b1-117">**レコード情報**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d49b1-117">Select **Record info**.</span></span>
10. <span data-ttu-id="d49b1-118">**ユーザー テンプレート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d49b1-118">Select **User template**.</span></span>
11. <span data-ttu-id="d49b1-119">**名前**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d49b1-119">In the **Name** field, type a value.</span></span>
12. <span data-ttu-id="d49b1-120">**説明**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d49b1-120">In the **Description** field, type a value.</span></span>
13. <span data-ttu-id="d49b1-121">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d49b1-121">Select **OK**.</span></span>
14. <span data-ttu-id="d49b1-122">**閉じる**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d49b1-122">Select **Close**.</span></span>

