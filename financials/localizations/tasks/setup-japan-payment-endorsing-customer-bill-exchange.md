--- 
title: "顧客受取手形の裏書による日本の支払の設定 (日本)"
description: "このタスクでは、日本での顧客の為替手形の裏書きによる支払いの設定について説明します。"
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 87841d708fc0aaceb3057eb37500ea8dfbc30ec2
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-japan-payment-by-endorsing-a-customer-bill-of-exchange-japan"></a><span data-ttu-id="78101-103">顧客受取手形の裏書による日本の支払の設定 (日本)</span><span class="sxs-lookup"><span data-stu-id="78101-103">Set up Japan payment by endorsing a customer bill of exchange (Japan)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="78101-104">このタスクでは、日本での顧客の為替手形の裏書きによる支払いの設定について説明します。</span><span class="sxs-lookup"><span data-stu-id="78101-104">This task walks you through setting up payments by endorsing a customer bills of exchange for Japan.</span></span>



<span data-ttu-id="78101-105">このタスクは デモ データ会社 JPMF を使用してレコードされました。</span><span class="sxs-lookup"><span data-stu-id="78101-105">This task was recorded using the demo data company JPMF.</span></span>


## <a name="set-up-a-posting-profile-for-endorsing-bills-of-exchange"></a><span data-ttu-id="78101-106">為替手形の転記プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="78101-106">Set up a posting profile for endorsing bills of exchange</span></span>
1. <span data-ttu-id="78101-107">[売掛金勘定] > [設定] > [顧客転記プロファイル] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="78101-107">Go to Accounts receivable > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="78101-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="78101-108">Click New.</span></span>
3. <span data-ttu-id="78101-109">[転記プロファイル] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="78101-109">In the Posting profile field, type a value.</span></span>
    * <span data-ttu-id="78101-110">例: 「新しい BoE」と入力します。</span><span class="sxs-lookup"><span data-stu-id="78101-110">For example:  enter 'New BoE'.</span></span>  
4. <span data-ttu-id="78101-111">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="78101-111">Click Add.</span></span>
5. <span data-ttu-id="78101-112">[会計コード] フィールドでオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="78101-112">In the Account code field, select an option.</span></span>
    * <span data-ttu-id="78101-113">例えば、「すべて」を選択します。</span><span class="sxs-lookup"><span data-stu-id="78101-113">For example, select "All".</span></span>  
6. <span data-ttu-id="78101-114">[裏書勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="78101-114">In the Endorse account field, specify the desired values.</span></span>
7. <span data-ttu-id="78101-115">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="78101-115">Click Save.</span></span>

## <a name="set-up-bills-of-exchange-information-in-accounts-receivable-parameters"></a><span data-ttu-id="78101-116">売掛金勘定パラメータでの為替手形情報の設定</span><span class="sxs-lookup"><span data-stu-id="78101-116">Set up bills of exchange information in accounts receivable parameters</span></span>
1. <span data-ttu-id="78101-117">[売掛金勘定] > [設定] > [売掛金勘定パラメーター] に移動します。</span><span class="sxs-lookup"><span data-stu-id="78101-117">Go to Accounts receivable > Setup > Accounts receivable parameters.</span></span>
2. <span data-ttu-id="78101-118">[元帳と売上税] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="78101-118">Click the Ledger and sales tax tab.</span></span>
3. <span data-ttu-id="78101-119">[為替手形] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="78101-119">Expand the Bill of exchange section.</span></span>
4. <span data-ttu-id="78101-120">[裏書為替手形] フィールドで、ドロップ ダウン ボタンをクリックしてルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="78101-120">In the Endorse Bill of Exchange field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="78101-121">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="78101-121">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="78101-122">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="78101-122">Click Save.</span></span>


