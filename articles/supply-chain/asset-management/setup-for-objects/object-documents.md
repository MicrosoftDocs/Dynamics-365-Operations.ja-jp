---
title: 資産ドキュメント
description: このトピックでは、資産管理の資産ドキュメントについて説明します。
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectDocument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8e93ae3a1170b2f8441d29090af7a5a91db94e8e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245398"
---
# <a name="asset-documents"></a><span data-ttu-id="15462-103">資産ドキュメント</span><span class="sxs-lookup"><span data-stu-id="15462-103">Asset documents</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="15462-104">このトピックでは、資産管理の資産ドキュメントについて説明します。</span><span class="sxs-lookup"><span data-stu-id="15462-104">This topic explains asset documents in Asset Management.</span></span>

<span data-ttu-id="15462-105">資産管理では、ジョブ タイプ、資産メーカー、資産タイプまたは資産などに自動的に関連付けるようドキュメントを設定できます。</span><span class="sxs-lookup"><span data-stu-id="15462-105">In Asset Management, you can set up documents so that they are automatically related to job types, asset manufacturers, asset types, or assets, for example.</span></span> <span data-ttu-id="15462-106">この機能は、更新されたドキュメント バージョンがリリースされた場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="15462-106">This functionality is useful when updated document versions are released.</span></span> <span data-ttu-id="15462-107">その場合、更新されたドキュメントを Supply Chain Management ドキュメントで使用する標準の場所に入れ、ドキュメントを作成した資産ドキュメント レコードに関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="15462-107">In that case, you just have to put the updated document in the standard location that you use for your Supply Chain Management documents, and attach the document to the asset document record that you've created.</span></span> <span data-ttu-id="15462-108">更新されたドキュメントは **全資産**、**有効な資産**、**個人用の有効な資産**、**すべてのワーク オーダー**、および **有効なワーク オーダー ジョブ** メニュー項目からアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="15462-108">The updated document can then be accessed from the **All assets**, **Active assets**, **My active assets**, **All work orders**, and **Active work order jobs** menu items.</span></span> <span data-ttu-id="15462-109">資産ドキュメント レコードにドキュメントを関連づけるプロセスでは、標準ドキュメント処理システムが使用されます。</span><span class="sxs-lookup"><span data-stu-id="15462-109">The process for attaching documents to an asset document record uses the standard document handling system.</span></span>

<span data-ttu-id="15462-110">**例 1:** ジョブ タイプに関連するドキュメントは、そのジョブ タイプの手順を説明する場合があります。</span><span class="sxs-lookup"><span data-stu-id="15462-110">**Example 1:** A document that is related to a job type might describe a procedure for that job type.</span></span>

<span data-ttu-id="15462-111">**例2 :** 資産タイプ、メーカー、モデルの組み合わせに関連するドキュメントは、選択した資産メーカー モデルの標準マニュアルである場合があります。</span><span class="sxs-lookup"><span data-stu-id="15462-111">**Example 2:** A document that is related to a combination of an asset type, manufacturer, and model might be the standard manual for the selected asset manufacturer model.</span></span>

## <a name="create-asset-document-relation"></a><span data-ttu-id="15462-112">資産ドキュメント関係の作成</span><span class="sxs-lookup"><span data-stu-id="15462-112">Create asset document relation</span></span>

1. <span data-ttu-id="15462-113">**資産管理** \> **設定** \> **資産ドキュメント** を選択します。</span><span class="sxs-lookup"><span data-stu-id="15462-113">Select **Asset management** \> **Setup** \> **Asset documents**.</span></span>
2. <span data-ttu-id="15462-114">**新規** を選択して資産ドキュメント レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="15462-114">Select **New** to create an asset document record.</span></span>
3. <span data-ttu-id="15462-115">ドキュメント関係をどの程度特定するかに応じて、次の 1 つ以上のフィールドで関連するセクションを選択します。**資産タイプ**、**メーカー**、**モデル**、**資産**、**ジョブ タイプ カテゴリ**、**ジョブ タイプ**、**ジョブ タイプ バリアント**、および **ジョブ要件**。</span><span class="sxs-lookup"><span data-stu-id="15462-115">Depending on how specific you want the document relation to be, make relevant selections in one or more of the following fields: **Asset type**, **Manufacturer**, **Model**, **Asset**, **Job type category**, **Job type**, **Job type variant**, and **Job requirement**.</span></span> <span data-ttu-id="15462-116">**ジョブ タイプ バリアント** および **ジョブ要件** フィールドで使用できるオプションは、**ジョブ タイプ** フィールドの選択によって異なります。</span><span class="sxs-lookup"><span data-stu-id="15462-116">The options that are available in the **Job type variant** and **Job requirement** fields depend on your selection in the **Job type** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="15462-117">システムが資産またはワーク オーダーに関連するドキュメントを検索すると、資産管理はすべての資産ドキュメント レコードを調べて、一致の可能性をチェックします。</span><span class="sxs-lookup"><span data-stu-id="15462-117">When the system searches for documents that should be related to an asset or a work order, Asset Management goes through all asset document records to check for a possible match.</span></span> <span data-ttu-id="15462-118">常に最も限定的な組み合わせを最初にチェックします。</span><span class="sxs-lookup"><span data-stu-id="15462-118">It always checks the most specific combination first.</span></span> <span data-ttu-id="15462-119">つまり、資産管理は、まず **ジョブ要件** フィールドの一致をチェックします。</span><span class="sxs-lookup"><span data-stu-id="15462-119">In other words, Asset Management first checks for a match for the **Job requirement** field.</span></span> <span data-ttu-id="15462-120">一致するものが見つからない場合は、**ジョブ タイプ バリアント** フィールドの一致がチェックされます。</span><span class="sxs-lookup"><span data-stu-id="15462-120">If no match is found, it checks for a match for the **Job type variant** field.</span></span> <span data-ttu-id="15462-121">一致するものが見つからない場合は、**ジョブ タイプ** フィールドなどの一致がチェックされます。</span><span class="sxs-lookup"><span data-stu-id="15462-121">If no match is found, it checks for a match for the **Job type** field, and so on.</span></span> <span data-ttu-id="15462-122">**資産ドキュメント** ページのレイアウトで分かるように、この動作は、最も限定的な組み合わせを見つけるために、資産管理が各レコードを右から左に一致をチェックすることを意味します。</span><span class="sxs-lookup"><span data-stu-id="15462-122">As you can see in the layout of the **Asset documents** page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="15462-123">複数のドキュメントが資産またはワーク オーダーに関連している場合があります。</span><span class="sxs-lookup"><span data-stu-id="15462-123">Several documents might be related to an asset or a work order.</span></span> <span data-ttu-id="15462-124">必要に応じて、メンテナンス要求またはワーク オーダーでサービス レベルを編集できます。</span><span class="sxs-lookup"><span data-stu-id="15462-124">You can edit the service level on a maintenance request or a work order as you require.</span></span>

4. <span data-ttu-id="15462-125">**添付ファイル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="15462-125">Select **Attachments**.</span></span> <span data-ttu-id="15462-126">標準の **ドキュメント処理** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="15462-126">The standard **Document handling** page appears.</span></span>
5. <span data-ttu-id="15462-127">資産ドキュメント レコードに関連付けるドキュメントまたはメモを設定します。</span><span class="sxs-lookup"><span data-stu-id="15462-127">Set up the documents or notes that should be attached to the asset document record.</span></span> <span data-ttu-id="15462-128">ドキュメントを関連付けると、**アタッチメント** フィールドにレコードに関連するドキュメントの数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="15462-128">After you attach documents, the **Attachments** field shows the number of documents that are related to the record.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]