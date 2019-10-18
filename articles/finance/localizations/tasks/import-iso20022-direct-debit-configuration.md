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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7eee00021f49ac0110d7bde07faba8095348e1b4
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185753"
---
# <a name="import-iso20022-direct-debit-configuration"></a><span data-ttu-id="7f51f-103">ISO20022 口座引落コンフィギュレーションのインポート</span><span class="sxs-lookup"><span data-stu-id="7f51f-103">Import ISO20022 direct debit configuration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7f51f-104">この手順では、顧客支払の電子レポートのコンフィギュレーションをインポートする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="7f51f-104">This procedure demonstrates how to import a customer payment electronic reporting configuration.</span></span> <span data-ttu-id="7f51f-105">この手順では、ISO 20022 口座引落形式を例として使用します。</span><span class="sxs-lookup"><span data-stu-id="7f51f-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> 



<span data-ttu-id="7f51f-106">この手順はデモ データの会社 DEMF を使用して作成されましたが、どのデモ データの会社もこの目的に使用できます。</span><span class="sxs-lookup"><span data-stu-id="7f51f-106">This procedure was created using the demo data company DEMF but you can use any demo data company for this purpose.</span></span>



<span data-ttu-id="7f51f-107">これは、5 つのうち 1 つ目の手順で、電子レポートのコンフィギュレーションを使用する顧客支払処理を説明しています。</span><span class="sxs-lookup"><span data-stu-id="7f51f-107">This is the first of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="7f51f-108">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f51f-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="7f51f-109">使用できるコンフィギュレーション プロバイダーの一覧で、[Microsoft] を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f51f-109">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="7f51f-110">[有効に設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f51f-110">Click Set active.</span></span>
4. <span data-ttu-id="7f51f-111">[リポジトリ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f51f-111">Click Repositories.</span></span>
5. <span data-ttu-id="7f51f-112">[開く] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f51f-112">Click Open.</span></span>
6. <span data-ttu-id="7f51f-113">[フィルターの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f51f-113">Click Show filters.</span></span>
7. <span data-ttu-id="7f51f-114">[コンフィギュレーション名] フィールドで "次の値で始まる" フィルター演算子を使用して、値 "ISO20022 口座引落 (DE)" でフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="7f51f-114">Apply the following filters: Enter a filter value of "ISO20022 Direct debit (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="7f51f-115">必要に応じて、一覧のコンフィギュレーションを検索して選択し、この手順を省略できます。</span><span class="sxs-lookup"><span data-stu-id="7f51f-115">Optionally, you can find the configuration in the list, select it, and skip this step.</span></span>  
8. <span data-ttu-id="7f51f-116">[インポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f51f-116">Click Import.</span></span>
    * <span data-ttu-id="7f51f-117">インポートのボタンを使用できない場合は、そのコンフィギュレーションは既にインポートされています。</span><span class="sxs-lookup"><span data-stu-id="7f51f-117">If the Import button is not available, it means that the configuration has been imported already.</span></span>  
9. <span data-ttu-id="7f51f-118">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f51f-118">Click Yes.</span></span>

