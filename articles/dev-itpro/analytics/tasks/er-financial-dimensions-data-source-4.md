--- 
title: "データ ソースとして財務分析コードを使用するレポートの実行"
description: "次の手順では、システム管理者に指定されたユーザーまたは電子レポート開発者のロールが、電子レポート・データソースとしての財務分析コードを使用するために 電子レポート（ER）モデルをどのように環境設定しているのか説明します。"
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 6569f9b97d5d15bf74b8b3882bf4bab50970dd0f
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---
# <a name="run-reports-that-use-financial-dimensions-as-data-sources"></a><span data-ttu-id="f0245-103">データ ソースとして財務分析コードを使用するレポートの実行</span><span class="sxs-lookup"><span data-stu-id="f0245-103">Run reports that use financial dimensions as data sources</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f0245-104">次の手順では、システム管理者に指定されたユーザーまたは電子レポート開発者のロールが、電子レポート・データソースとしての財務分析コードを使用するために 電子レポート（ER）モデルをどのように環境設定しているのか説明します。</span><span class="sxs-lookup"><span data-stu-id="f0245-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="f0245-105">これらのステップは DEMF 会社で実行できます。</span><span class="sxs-lookup"><span data-stu-id="f0245-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="f0245-106">これらの手順を実施するには、まず「データ ソース (パート3：レポートのデザイン）手順としてのER使用・財務分析コード」にある手順を実施する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f0245-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 3: Design the report)” procedure.</span></span> <span data-ttu-id="f0245-107">また、電子レポート パラメーターのページで既定のドキュメント タイプを環境設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f0245-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="f0245-108">既定のドキュメントタイプは、ERのコンフィギュレーションがダウンロード、インポートされるときにも設定されます。</span><span class="sxs-lookup"><span data-stu-id="f0245-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="f0245-109">レポートを実行する</span><span class="sxs-lookup"><span data-stu-id="f0245-109">Run report</span></span>
1. <span data-ttu-id="f0245-110">[組織管理] > [電子申告] > [コンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="f0245-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="f0245-111">[ツリー] フィールドで、「Financial dimensions sample model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="f0245-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="f0245-112">ツリーで、「Financial dimensions sample model\Ledger journal report」を選択します。</span><span class="sxs-lookup"><span data-stu-id="f0245-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="f0245-113">[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f0245-113">Click Run.</span></span>
5. <span data-ttu-id="f0245-114">[ディメンション名] フィールドに値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="f0245-114">In the Dimension name field, In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="f0245-115">現在の会社のすべての分析コードを選択するには、次を入力します: 事業単位、コストセンター、部門、品目グループ、主勘定、プロジェクト</span><span class="sxs-lookup"><span data-stu-id="f0245-115">To select all dimensions in the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
6. <span data-ttu-id="f0245-116">[対象に含めるレコード] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="f0245-116">Expand the Records to include section.</span></span>
7. <span data-ttu-id="f0245-117">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f0245-117">Click Filter.</span></span>
8. <span data-ttu-id="f0245-118">仕訳元帳表および仕訳バッチ番号フィールドの行を選択します。</span><span class="sxs-lookup"><span data-stu-id="f0245-118">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="f0245-119">[基準] フィールドで、「00057」と入力します。</span><span class="sxs-lookup"><span data-stu-id="f0245-119">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="f0245-120">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f0245-120">Click OK.</span></span>
11. <span data-ttu-id="f0245-121">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f0245-121">Click OK.</span></span>
    * <span data-ttu-id="f0245-122">生成された出荷を確認します。</span><span class="sxs-lookup"><span data-stu-id="f0245-122">Review the generated output.</span></span> <span data-ttu-id="f0245-123">選択したバッチの各トランザクションについては、相当する分析コードの財務分析コードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f0245-123">Note that for each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="f0245-124">このレポートを実行し異なる分析コードを選択して、レポートが選択した分析コードの数または Dynamics 365 for Finance and Operations インスタンスに構成した分析コードの数に依存していないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="f0245-124">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations instance.</span></span>  


