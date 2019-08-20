---
title: AX 2009 の移行 － パッケージのインポート
description: このトピックは、Microsoft Dynamics AX 2009 から Microsoft Dynamics 365 for Finance and Operations に移行済みデータ パッケージをインポートする方法について説明します。
author: kfend
manager: AnnBe
ms.date: 09/13/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2018-06-21
ms.dyn365.ops.version: Platform update 17
ms.openlocfilehash: b8e0ba59688485c52a01e3265a767d4ddd327953
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851785"
---
# <a name="ax-2009-migration--import-packages"></a><span data-ttu-id="9a75e-103">AX 2009 の移行 - パッケージのインポート</span><span class="sxs-lookup"><span data-stu-id="9a75e-103">AX 2009 migration – Import packages</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9a75e-104">データは、正しい順序で配列された論理的に関連するエンティティのグループにインポートできます。</span><span class="sxs-lookup"><span data-stu-id="9a75e-104">Data can be imported for a group of logically related entities that are sequenced in the correct order.</span></span> <span data-ttu-id="9a75e-105">Microsoft Dynamics 365 for Finance and Operations に移行する Microsoft Dynamics AX 2009 データをインポートするための、以下の 3 つのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="9a75e-105">You have three options for importing Microsoft Dynamics AX 2009 data that you want to migrate to Microsoft Dynamics 365 for Finance and Operations:</span></span>

- <span data-ttu-id="9a75e-106">AX 2009</span><span class="sxs-lookup"><span data-stu-id="9a75e-106">AX 2009</span></span>
- <span data-ttu-id="9a75e-107">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9a75e-107">Finance and Operations</span></span>

## <a name="ax-2009"></a><span data-ttu-id="9a75e-108">AX 2009</span><span class="sxs-lookup"><span data-stu-id="9a75e-108">AX 2009</span></span>
<span data-ttu-id="9a75e-109">移行のデータは、ソース システムから直接インポートできます。</span><span class="sxs-lookup"><span data-stu-id="9a75e-109">You can import data for migration directly from the source system.</span></span> <span data-ttu-id="9a75e-110">以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="9a75e-110">Follow these steps.</span></span>

1. <span data-ttu-id="9a75e-111">AX 2009 の、ナビゲーション ウィンドウで、**データ移行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a75e-111">In AX 2009, in the navigation pane, click **Data migration**.</span></span>
2. <span data-ttu-id="9a75e-112">**共通** \> **移行グループの作成** に移動します。</span><span class="sxs-lookup"><span data-stu-id="9a75e-112">Go to **Common** \> **Create migration group**.</span></span>
3. <span data-ttu-id="9a75e-113">**移行グループ** フォームで、エクスポートする移行グループを選択し、**今すぐエクスポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a75e-113">In the **Migration group** form, select the migration group to export, and then click **Export now**.</span></span>
4. <span data-ttu-id="9a75e-114">**データのエクスポート** フォームで、**ターゲットにパッケージをインポートする** チェック ボックスをオンにし、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a75e-114">In the **Export data** form, select the **Import package in target** check box, and then click **OK**.</span></span>

## <a name="finance-and-operations"></a><span data-ttu-id="9a75e-115">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9a75e-115">Finance and Operations</span></span>
<span data-ttu-id="9a75e-116">Finance and Operations 環境を使用して、移行のデータをインポートできます。</span><span class="sxs-lookup"><span data-stu-id="9a75e-116">You can import data for migration by using your Finance and Operations environment.</span></span> <span data-ttu-id="9a75e-117">以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="9a75e-117">Follow these steps.</span></span>

1. <span data-ttu-id="9a75e-118">管理者ロールを使用して、Finance and Operations 環境にログインします。</span><span class="sxs-lookup"><span data-stu-id="9a75e-118">Sign in to your Finance and Operations environment by using an Administrator role.</span></span>
2. <span data-ttu-id="9a75e-119">ダッシュボードで、**データ管理**ワークスペースを選択します。</span><span class="sxs-lookup"><span data-stu-id="9a75e-119">On the dashboard, select the **Data Management** workspace.</span></span>
3. <span data-ttu-id="9a75e-120">**インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a75e-120">Select **Import**.</span></span>
4. <span data-ttu-id="9a75e-121">パッケージの名前を入力し、**ソースのデータ形式** フィールドで **パッケージ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a75e-121">Enter the name of the package, and then, in the **Source data format** field, select **Package**.</span></span>
5. <span data-ttu-id="9a75e-122">**アップロード** を選択し、インポートするデータの場所から適切なパッケージ ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="9a75e-122">Select **Upload**, and then select the appropriate package file from the location for the data that is being imported.</span></span> <span data-ttu-id="9a75e-123">パッケージからすべてのファイルがインポートされます。</span><span class="sxs-lookup"><span data-stu-id="9a75e-123">All the files from the package are imported.</span></span>

