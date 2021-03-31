---
title: ISO20022 口座引落コンフィギュレーションのインポート
description: この手順では、顧客支払の電子レポートのコンフィギュレーションをインポートする方法を示します。
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 964f396625340d593a2fe3dd5be5a1b7da795e9a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218761"
---
# <a name="import-iso20022-direct-debit-configuration"></a><span data-ttu-id="3d04b-103">ISO20022 口座引落コンフィギュレーションのインポート</span><span class="sxs-lookup"><span data-stu-id="3d04b-103">Import ISO20022 direct debit configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3d04b-104">この手順では、顧客支払の電子レポートのコンフィギュレーションをインポートする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="3d04b-104">This procedure demonstrates how to import a customer payment electronic reporting configuration.</span></span> <span data-ttu-id="3d04b-105">この手順では、ISO 20022 口座引落形式を例として使用します。</span><span class="sxs-lookup"><span data-stu-id="3d04b-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> 



<span data-ttu-id="3d04b-106">この手順はデモ データの会社 DEMF を使用して作成されましたが、どのデモ データの会社もこの目的に使用できます。</span><span class="sxs-lookup"><span data-stu-id="3d04b-106">This procedure was created using the demo data company DEMF but you can use any demo data company for this purpose.</span></span>



<span data-ttu-id="3d04b-107">これは、5 つのうち 1 つ目の手順で、電子レポートのコンフィギュレーションを使用する顧客支払処理を説明しています。</span><span class="sxs-lookup"><span data-stu-id="3d04b-107">This is the first of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="3d04b-108">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3d04b-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="3d04b-109">使用できるコンフィギュレーション プロバイダーの一覧で、[Microsoft] を選択します。</span><span class="sxs-lookup"><span data-stu-id="3d04b-109">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="3d04b-110">[有効に設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d04b-110">Click Set active.</span></span>
4. <span data-ttu-id="3d04b-111">[リポジトリ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d04b-111">Click Repositories.</span></span>
5. <span data-ttu-id="3d04b-112">[開く] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d04b-112">Click Open.</span></span>
6. <span data-ttu-id="3d04b-113">[フィルターの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d04b-113">Click Show filters.</span></span>
7. <span data-ttu-id="3d04b-114">[コンフィギュレーション名] フィールドで "次の値で始まる" フィルター演算子を使用して、値 "ISO20022 口座引落 (DE)" でフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="3d04b-114">Apply the following filters: Enter a filter value of "ISO20022 Direct debit (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="3d04b-115">必要に応じて、一覧のコンフィギュレーションを検索して選択し、この手順を省略できます。</span><span class="sxs-lookup"><span data-stu-id="3d04b-115">Optionally, you can find the configuration in the list, select it, and skip this step.</span></span>  
8. <span data-ttu-id="3d04b-116">[インポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d04b-116">Click Import.</span></span>
    * <span data-ttu-id="3d04b-117">インポートのボタンを使用できない場合は、そのコンフィギュレーションは既にインポートされています。</span><span class="sxs-lookup"><span data-stu-id="3d04b-117">If the Import button is not available, it means that the configuration has been imported already.</span></span>  
9. <span data-ttu-id="3d04b-118">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d04b-118">Click Yes.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]