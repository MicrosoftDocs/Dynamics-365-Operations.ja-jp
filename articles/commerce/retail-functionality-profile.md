---
title: 小売機能プロファイルの作成
description: このトピックでは、Microsoft Dynamics 365 Commerce に機能プロファイルを作成する方法について説明します。
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6bee51eb25b04eb65e588dd4cf54a0cef587aa15
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057351"
---
# <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="d8c8f-103">小売機能プロファイルの作成</span><span class="sxs-lookup"><span data-stu-id="d8c8f-103">Create a retail functionality profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d8c8f-104">このトピックでは、Microsoft Dynamics 365 Commerce に機能プロファイルを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d8c8f-104">This topic describes how to create a functionality profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d8c8f-105">概要</span><span class="sxs-lookup"><span data-stu-id="d8c8f-105">Overview</span></span>

<span data-ttu-id="d8c8f-106">コマース機能プロファイルは、オンライン チャネルに使用されるさまざまな設定を提供します。</span><span class="sxs-lookup"><span data-stu-id="d8c8f-106">The commerce functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="d8c8f-107">各チャネルでは、機能プロファイルを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8c8f-107">Each channel must specify a functionality profile.</span></span>

## <a name="create-a-functionality-profile"></a><span data-ttu-id="d8c8f-108">機能プロファイルの作成</span><span class="sxs-lookup"><span data-stu-id="d8c8f-108">Create a functionality profile</span></span>

<span data-ttu-id="d8c8f-109">機能プロファイルを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="d8c8f-109">To create a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="d8c8f-110">ナビゲーション ウィンドウで、**モジュール \> チャネル設定 \> POS プロファイル \> 機能プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d8c8f-110">In the navigation pane, go to **Modules \> Channel setup \> POS profiles \> Functionality profiles**.</span></span>
1. <span data-ttu-id="d8c8f-111">アクション ウィンドウで、**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d8c8f-111">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d8c8f-112">**プロファイル** フィールドで、プロファイルの ID を入力します (以下のサンプル画像の "FN006")。</span><span class="sxs-lookup"><span data-stu-id="d8c8f-112">In the **Profile** field, enter an ID for the profile ("FN006" in the example image below).</span></span>
1. <span data-ttu-id="d8c8f-113">**説明**フィールドに、値を入力します (以下のサンプル画像の "Adventure Works プロファイル")。</span><span class="sxs-lookup"><span data-stu-id="d8c8f-113">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="d8c8f-114">**全般**セクションで、**ISO** ロケールの国を選択します。</span><span class="sxs-lookup"><span data-stu-id="d8c8f-114">In the **General** section, select a country for the **ISO** locale.</span></span>
1. <span data-ttu-id="d8c8f-115">**全般**セクションで、必要に応じてその他の設定を変更します。</span><span class="sxs-lookup"><span data-stu-id="d8c8f-115">In the **General** section, modify other settings, as needed.</span></span>
1. <span data-ttu-id="d8c8f-116">**全般**セクションで、電子メール レシートの**レシート プロファイル ID** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d8c8f-116">In the **General** section, select a **Receipt profile ID** for email receipts.</span></span>
1. <span data-ttu-id="d8c8f-117">**機能**セクションで、必要に応じて設定を変更します。</span><span class="sxs-lookup"><span data-stu-id="d8c8f-117">In the **Functions** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="d8c8f-118">**金額**セクションで、必要に応じて設定を変更します。</span><span class="sxs-lookup"><span data-stu-id="d8c8f-118">In the **Amount** section, modify settings as, needed.</span></span>
1. <span data-ttu-id="d8c8f-119">**情報コード** セクションで、必要に応じて設定を変更します。</span><span class="sxs-lookup"><span data-stu-id="d8c8f-119">In the **Info Codes** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="d8c8f-120">**レシート番号**セクションで、必要に応じて設定を変更します。</span><span class="sxs-lookup"><span data-stu-id="d8c8f-120">In the **Receipt numbering** section, modify settings, as needed.</span></span> 
  
<span data-ttu-id="d8c8f-121">次の図は、機能プロファイルの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="d8c8f-121">The following image shows an example functionality profile.</span></span>
  
![機能プロファイルの例](media/retail-functionality-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="d8c8f-123">追加リソース</span><span class="sxs-lookup"><span data-stu-id="d8c8f-123">Additional resources</span></span>

[<span data-ttu-id="d8c8f-124">情報コードおよび情報コード グループ</span><span class="sxs-lookup"><span data-stu-id="d8c8f-124">Info codes and info code groups</span></span>](info-codes-retail.md)           

[<span data-ttu-id="d8c8f-125">新しいアドレス帳の作成</span><span class="sxs-lookup"><span data-stu-id="d8c8f-125">Create new address book</span></span>](new-address-book.md) 

[<span data-ttu-id="d8c8f-126">画面レイアウトの概要</span><span class="sxs-lookup"><span data-stu-id="d8c8f-126">Screen layout overview</span></span>](pos-screen-layouts.md)       

[<span data-ttu-id="d8c8f-127">Retail Hardware Station のコンフィギュレーションおよびインストール</span><span class="sxs-lookup"><span data-stu-id="d8c8f-127">Configure and install Retail hardware station</span></span>](retail-hardware-station-configuration-installation.md) 
