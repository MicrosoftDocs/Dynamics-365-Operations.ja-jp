---
title: 製品コンフィギュレーション モデルの承認
description: この手順を実行するには、少なくとも 1 つの製品コンフィギュレーション モデルが必要です。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductModelVersion, PCApproveProductModelVersion, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c945756997b0580ac7ffb19261f9184e53a1c10
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920510"
---
# <a name="approve-a-product-configuration-model"></a><span data-ttu-id="4d48a-103">製品コンフィギュレーション モデルの承認</span><span class="sxs-lookup"><span data-stu-id="4d48a-103">Approve a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4d48a-104">この手順を実行するには、少なくとも 1 つの製品コンフィギュレーション モデルが必要です。</span><span class="sxs-lookup"><span data-stu-id="4d48a-104">Running this procedure requires that at least one product configuration model is available.</span></span> <span data-ttu-id="4d48a-105">この手順では、デモ データの会社 USMF の [ハイエンド スピーカー] モデルが使用されています。</span><span class="sxs-lookup"><span data-stu-id="4d48a-105">This procedure uses the High end speaker model in the demo data company USMF.</span></span> <span data-ttu-id="4d48a-106">このモデルは既に承認済ですが、手順は、プロセス全体について説明します。</span><span class="sxs-lookup"><span data-stu-id="4d48a-106">Note that this model has already been approved, but the procedure walks you through the entire process.</span></span>

1. <span data-ttu-id="4d48a-107">**製品情報管理\>製品\>製品コンフィギュレーション モデル** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d48a-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="4d48a-108">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="4d48a-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4d48a-109">この手順の [ハイエンド スピーカー] モデルを選択します。</span><span class="sxs-lookup"><span data-stu-id="4d48a-109">Select the High end speaker model for this procedure.</span></span>  
1. <span data-ttu-id="4d48a-110">**バージョン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4d48a-110">Select **Versions**.</span></span>
1. <span data-ttu-id="4d48a-111">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4d48a-111">Select **New**.</span></span>
1. <span data-ttu-id="4d48a-112">**製品番号** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="4d48a-112">In the **Product number** field, enter or select a value.</span></span>
    * <span data-ttu-id="4d48a-113">製品への参照は、製品コンフィギュレーション モデルのバージョンを表します。</span><span class="sxs-lookup"><span data-stu-id="4d48a-113">The reference to a product represents a version of a product configuration model.</span></span> <span data-ttu-id="4d48a-114">制約ベースのコンフィギュレーション テクノロジがある製品マスターのみこの一覧に表示されます。</span><span class="sxs-lookup"><span data-stu-id="4d48a-114">Only product masters which have the constraint-based configuration technology will appear in this list.</span></span>  
1. <span data-ttu-id="4d48a-115">**開始日** フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="4d48a-115">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="4d48a-116">製品モデル バージョンがある場合選択します。</span><span class="sxs-lookup"><span data-stu-id="4d48a-116">Select when the product model version will be available.</span></span>  
1. <span data-ttu-id="4d48a-117">**終了日** フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="4d48a-117">In the **To date** field, enter a date.</span></span>
    * <span data-ttu-id="4d48a-118">この製品モデル バージョンの有効期限が切れる場合は終了日を、または [なし] を選択します。</span><span class="sxs-lookup"><span data-stu-id="4d48a-118">Select an end date when this product model version will expire, or select Never.</span></span>  
1. <span data-ttu-id="4d48a-119">**承認** を選択してドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="4d48a-119">Select **Approve** to open the drop dialog.</span></span>
1. <span data-ttu-id="4d48a-120">**承認者** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="4d48a-120">In the **Approved by** field, enter or select a value.</span></span>
    * <span data-ttu-id="4d48a-121">工程の使用のために製品モデルの承認を担当する個人を選択します。</span><span class="sxs-lookup"><span data-stu-id="4d48a-121">Select the person who is responsible for approving product models for use in operations.</span></span>  
1. <span data-ttu-id="4d48a-122">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4d48a-122">Select **OK**.</span></span>
1. <span data-ttu-id="4d48a-123">**価格決定方法** フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="4d48a-123">In the **Pricing method** field, select an option.</span></span>
    * <span data-ttu-id="4d48a-124">製品モデルのバージョンを有効化します。</span><span class="sxs-lookup"><span data-stu-id="4d48a-124">Activate the product model version.</span></span> <span data-ttu-id="4d48a-125">1 度に、1 つの製品モデルに対して、1 つの製品のみ有効にできます。</span><span class="sxs-lookup"><span data-stu-id="4d48a-125">It is only possible to have one product active for one product model at a time.</span></span>  
1. <span data-ttu-id="4d48a-126">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4d48a-126">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]