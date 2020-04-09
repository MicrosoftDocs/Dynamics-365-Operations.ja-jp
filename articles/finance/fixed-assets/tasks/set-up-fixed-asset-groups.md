---
title: 固定資産グループの設定
description: このトピックでは、新しい固定資産グループを作成する方法を説明します。
author: saraschi2
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetGroup, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9bcb78158afbf7bb0e9b83b35e37b1532a7c6283
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138187"
---
# <a name="set-up-fixed-asset-groups"></a><span data-ttu-id="db53b-103">固定資産グループの設定</span><span class="sxs-lookup"><span data-stu-id="db53b-103">Set up fixed asset groups</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="db53b-104">このトピックでは、新しい固定資産グループを作成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="db53b-104">This topic explains how to create a new fixed asset group.</span></span> <span data-ttu-id="db53b-105">これは USMF の法人に対して経理担当ロールとデモ データを使用します。</span><span class="sxs-lookup"><span data-stu-id="db53b-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="db53b-106">ナビゲーション ウィンドウで、**モジュール > 固定資産 > 設定 > 固定資産グループ**に移動します。</span><span class="sxs-lookup"><span data-stu-id="db53b-106">In the navigation pane, go to **Modules > Fixed assets > Setup > Fixed asset groups**.</span></span>
2. <span data-ttu-id="db53b-107">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="db53b-107">Select **New**.</span></span>
3. <span data-ttu-id="db53b-108">**固定資産グループ** フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="db53b-108">In the **Fixed asset group** field, type a value.</span></span>
4. <span data-ttu-id="db53b-109">**名前**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="db53b-109">In the **Name** field, type a value.</span></span> <span data-ttu-id="db53b-110">**固定資産**グループにおける固定資産の自動採番と番号順序コードは、固定資産のパラメータの設定より優先されます。</span><span class="sxs-lookup"><span data-stu-id="db53b-110">Autonumber fixed assets and Number sequence code on the **Fixed asset** group will override the settings on the Fixed assets parameters.</span></span> <span data-ttu-id="db53b-111">この固定資産グループの資産に他のグループからの異なる番号付けがある場合、ここでこれを変更できます。</span><span class="sxs-lookup"><span data-stu-id="db53b-111">You can change it here if the assets in this fixed asset group will have different numbering from other groups.</span></span>  
5. <span data-ttu-id="db53b-112">**帳簿**を選択します。</span><span class="sxs-lookup"><span data-stu-id="db53b-112">Select **Books**.</span></span>
6. <span data-ttu-id="db53b-113">**帳簿**フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="db53b-113">In the **Book** field, enter or select a value.</span></span> <span data-ttu-id="db53b-114">**減価償却の計算**フィールドが**はい**に設定されている場合、資産帳簿は償却提案に含まれます。</span><span class="sxs-lookup"><span data-stu-id="db53b-114">The **Calculate depreciation** field is set to **Yes**, so the asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="db53b-115">**減価償却の計算**が**いいえ**に設定されている場合、資産は自動的に償却されません。</span><span class="sxs-lookup"><span data-stu-id="db53b-115">If **Calculate depreciation** is set to **No**, the asset will not be automatically depreciated.</span></span>  
7. <span data-ttu-id="db53b-116">資産の耐用年数を設定します。</span><span class="sxs-lookup"><span data-stu-id="db53b-116">Set the Service life of the asset, in years.</span></span> <span data-ttu-id="db53b-117">耐用年数を設定した後に、**減価償却期間**のフィールド値が計算されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="db53b-117">Note that the **Depreciation periods** field value is calculated after setting the Service life.</span></span>  
8. <span data-ttu-id="db53b-118">**減価償却方法**フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="db53b-118">In the **Depreciation convention** field, select an option.</span></span>
9. <span data-ttu-id="db53b-119">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="db53b-119">Close the page.</span></span>

