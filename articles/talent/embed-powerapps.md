---
title: Dynamics 365 Human Resources の Power Apps アプリの埋め込み
description: このトピックでは、Microsoft Power Apps メニュー項目がシステム管理モジュールから消えてしまう問題を解決する方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8275a8a7c68fa13d6b9880c4c411deaa2dcbb998
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2020
ms.locfileid: "3017876"
---
# <a name="embed-power-apps-apps-in-dynamics-365-human-resources"></a><span data-ttu-id="e5d55-103">Dynamics 365 Human Resources の Power Apps アプリの埋め込み</span><span class="sxs-lookup"><span data-stu-id="e5d55-103">Embed Power Apps apps in Dynamics 365 Human Resources</span></span>

<span data-ttu-id="e5d55-104">**問題点**</span><span class="sxs-lookup"><span data-stu-id="e5d55-104">**Issue**</span></span>

<span data-ttu-id="e5d55-105">**Power Apps** メニュー項目が**システム管理**モジュールから消えました。</span><span class="sxs-lookup"><span data-stu-id="e5d55-105">The **Power Apps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="e5d55-106">**原因**</span><span class="sxs-lookup"><span data-stu-id="e5d55-106">**Cause**</span></span>

<span data-ttu-id="e5d55-107">ユーザー インターフェイス (UI) のデザインが変更され、Microsoft Power Apps が標準の個人用設定モデルに含まれるようになりました。</span><span class="sxs-lookup"><span data-stu-id="e5d55-107">The user interface (UI) design has been changed, and Microsoft Power Apps is now included in the standard personalization model.</span></span>

<span data-ttu-id="e5d55-108">**解像度**</span><span class="sxs-lookup"><span data-stu-id="e5d55-108">**Resolution**</span></span>

<span data-ttu-id="e5d55-109">Power Apps が埋め込まれる方法が変更されました。</span><span class="sxs-lookup"><span data-stu-id="e5d55-109">The way that Power Apps are embedded has been changed.</span></span> <span data-ttu-id="e5d55-110">Power Apps は個人用設定モデルによって追加されます。</span><span class="sxs-lookup"><span data-stu-id="e5d55-110">Power Apps are now added through the personalization model.</span></span> <span data-ttu-id="e5d55-111">Power Apps は、Microsoft Dynamics 365 Talent のほとんどすべてのページに追加できます。</span><span class="sxs-lookup"><span data-stu-id="e5d55-111">You can add Power Apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="e5d55-112">Power Apps を Talent に埋め込む方法の詳細については、[Power Apps の埋め込み](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e5d55-112">For information about how to embed Power Apps in Talent, see [Embed Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="e5d55-113">変更前にアプリを埋め込んだ Power Apps の顧客は、新しいモデルにアップグレードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5d55-113">Any Power Apps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="e5d55-114">**Power Apps** ボタンは、Talent のほとんどすべてのページの右上隅にあります。</span><span class="sxs-lookup"><span data-stu-id="e5d55-114">The **Power Apps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="e5d55-115">このボタンを使用して、アプリを挿入することができます。</span><span class="sxs-lookup"><span data-stu-id="e5d55-115">You can use this button to insert apps.</span></span>

<span data-ttu-id="e5d55-116">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="e5d55-116">Here is an example.</span></span>

1. <span data-ttu-id="e5d55-117">**人事管理\>リンク\>作業者\>従業員**に移動します。</span><span class="sxs-lookup"><span data-stu-id="e5d55-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="e5d55-118">**Power Apps** ボタンを選択し、**Power Apps からアプリを追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5d55-118">Select the **Power Apps** button, and then select **Add an app from Power Apps**.</span></span>

    ![Power Apps ボタン](media/png.png)

3. <span data-ttu-id="e5d55-120">**Power Apps からアプリを追加** ダイアログ ボックスのフィールドに入力します。</span><span class="sxs-lookup"><span data-stu-id="e5d55-120">Complete the fields in the **Add an app from Power Apps** dialog box.</span></span>

    ![Power Apps からアプリを追加ダイアログボックス](media/insert-powerapp.png)

<span data-ttu-id="e5d55-122">または、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e5d55-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="e5d55-123">ページのアクション ウィンドウの**オプション**タブ上の**個人用設定**グループで、**このページのパーソナライズ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5d55-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this page**.</span></span>

    ![オプション タブのグループをパーソナライズする](media/options.png)

    <span data-ttu-id="e5d55-125">個人用設定ツール バーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e5d55-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="e5d55-126">ツール バーで、**Power Apps からアプリを追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5d55-126">On the toolbar, select **Add an app from Power Apps**.</span></span>

    ![個人用設定ツールバーを使用して Power Apps からアプリを追加する](media/powerapp-bar.png)
