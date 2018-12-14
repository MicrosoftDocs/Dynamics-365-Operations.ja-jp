---
title: "Core HR への PowerApps アプリの埋め込み"
description: "このトピックでは、PowerApps メニュー項目がシステム管理モジュールから消えてしまう問題を解決する方法について説明します。"
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 197b553f0b202ee29ad42274e2c0e03446ec782c
ms.contentlocale: ja-jp
ms.lasthandoff: 12/04/2018

---

# <a name="embed-powerapps-apps-in-core-hr"></a><span data-ttu-id="c18d7-103">Core HR への PowerApps アプリの埋め込み</span><span class="sxs-lookup"><span data-stu-id="c18d7-103">Embed PowerApps apps in Core HR</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c18d7-104">**払出**</span><span class="sxs-lookup"><span data-stu-id="c18d7-104">**Issue**</span></span>

<span data-ttu-id="c18d7-105">**PowerApps** メニュー項目が**システム管理**モジュールから消えました。</span><span class="sxs-lookup"><span data-stu-id="c18d7-105">The **PowerApps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="c18d7-106">**原因**</span><span class="sxs-lookup"><span data-stu-id="c18d7-106">**Cause**</span></span>

<span data-ttu-id="c18d7-107">ユーザー インターフェイス (UI) のデザインが変更され、Microsoft PowerApps が標準の個人用設定モデルに含まれるようになりました。</span><span class="sxs-lookup"><span data-stu-id="c18d7-107">The user interface (UI) design has been changed, and Microsoft PowerApps is now included in the standard personalization model.</span></span>

<span data-ttu-id="c18d7-108">**解像度**</span><span class="sxs-lookup"><span data-stu-id="c18d7-108">**Resolution**</span></span>

<span data-ttu-id="c18d7-109">PowerApps アプリが埋め込まれる方法が変更されました。</span><span class="sxs-lookup"><span data-stu-id="c18d7-109">The way that PowerApps apps are embedded has been changed.</span></span> <span data-ttu-id="c18d7-110">PowerApps アプリは個人用設定モデルによって追加されます。</span><span class="sxs-lookup"><span data-stu-id="c18d7-110">PowerApps apps are now added through the personalization model.</span></span> <span data-ttu-id="c18d7-111">PowerApps アプリは、Microsoft Dynamics 365 for Talent のほとんどすべてのページに追加できます。</span><span class="sxs-lookup"><span data-stu-id="c18d7-111">You can add PowerApps apps to almost all pages in Microsoft Dynamics 365 for Talent.</span></span>

<span data-ttu-id="c18d7-112">PowerApps アプリを Talent に埋め込む方法の詳細については、[PowerApps アプリの埋め込み](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c18d7-112">For information about how to embed PowerApps apps in Talent, see [Embed PowerApps apps](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="c18d7-113">変更前にアプリを埋め込んだ PowerApps の顧客は、新しいモデルにアップグレードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c18d7-113">Any PowerApps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="c18d7-114">**PowerApps** ボタンは、Talent のほとんどすべてのページの右上隅にあります。</span><span class="sxs-lookup"><span data-stu-id="c18d7-114">The **PowerApps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="c18d7-115">このボタンを使用して、PowerApps アプリを挿入することができます。</span><span class="sxs-lookup"><span data-stu-id="c18d7-115">You can use this button to insert a PowerApps app.</span></span>

<span data-ttu-id="c18d7-116">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="c18d7-116">Here is an example.</span></span>

1. <span data-ttu-id="c18d7-117">**人事管理\>リンク\>作業者\>従業員**に移動します。</span><span class="sxs-lookup"><span data-stu-id="c18d7-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="c18d7-118">**PowerApps** ボタンを選択してから、**PowerApp の挿入**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c18d7-118">Select the **PowerApps** button, and then select **Insert a PowerApp**.</span></span>

    ![PowerApps ボタン](media/png.png)

3. <span data-ttu-id="c18d7-120">**PowerApp の挿入**ダイアログ ボックスのフィールドを完了します。</span><span class="sxs-lookup"><span data-stu-id="c18d7-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![PowerApp の挿入ダイアログ ボックス](media/insert-powerapp.png)

<span data-ttu-id="c18d7-122">または、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c18d7-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="c18d7-123">ページのアクション ウィンドウの**オプション**タブ上の**個人用設定**グループで、**このフォームのパーソナライズ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c18d7-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![オプション タブのグループをパーソナライズする](media/options.png)

    <span data-ttu-id="c18d7-125">個人用設定ツール バーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c18d7-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="c18d7-126">ツール バーで、**挿入\>PowerApp** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c18d7-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![個人用設定ツール バーを使用して PowerApps アプリを挿入する](media/powerapp-bar.png)

