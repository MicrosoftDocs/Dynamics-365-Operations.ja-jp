---
title: 減損会計の共通パラメーターおよび転記プロファイルの設定
description: このタスクでは、減損会計の共通パラメーターと転記プロファイルの定義方法が確認できます。
author: ShylaThompson
manager: AnnBe
ms.date: 02/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, AssetPosting
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4232f4ce055904e11239535facfed07dab6f1785
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3984849"
---
# <a name="setup-impairment-accounting-common-parameters-and-posting-profile"></a><span data-ttu-id="c96d0-103">減損会計の共通パラメーターおよび転記プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="c96d0-103">Setup impairment accounting common parameters and posting profile</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c96d0-104">このタスクでは、減損会計の共通パラメーターと転記プロファイルの定義方法が確認できます。</span><span class="sxs-lookup"><span data-stu-id="c96d0-104">Use this task to learn how to define impairment accounting common parameters and posting profiles.</span></span>



<span data-ttu-id="c96d0-105">このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c96d0-105">To complete this task, the Fixed Assets configuration key must be selected.</span></span>



<span data-ttu-id="c96d0-106">この手順では、JPMF デモ会社のデータを使用します。</span><span class="sxs-lookup"><span data-stu-id="c96d0-106">This procedure uses the JPMF demo company data.</span></span>


## <a name="set-up-impairment-parameters"></a><span data-ttu-id="c96d0-107">減損パラメーターを設定</span><span class="sxs-lookup"><span data-stu-id="c96d0-107">Set up impairment parameters</span></span>
1. <span data-ttu-id="c96d0-108">[固定資産] > [設定] > [固定資産パラメーター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c96d0-108">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="c96d0-109">[減損管理] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c96d0-109">Expand the Impairment management section.</span></span>
3. <span data-ttu-id="c96d0-110">[警告期間 (月数) ] フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c96d0-110">In the Warning period (in months) field, enter a number.</span></span>
    * <span data-ttu-id="c96d0-111">例: 6 か月</span><span class="sxs-lookup"><span data-stu-id="c96d0-111">Example: 6 months</span></span>  
4. <span data-ttu-id="c96d0-112">番号順序タブをクリックし、次の番号順序コードが設定されていることを確定します。</span><span class="sxs-lookup"><span data-stu-id="c96d0-112">Click the Number sequences tab. Confirm the following Number sequence codes are set up:</span></span>  
 - <span data-ttu-id="c96d0-113">減損のドキュメント ID</span><span class="sxs-lookup"><span data-stu-id="c96d0-113">Document ID for impairment</span></span>
 - <span data-ttu-id="c96d0-114">減損損失テスト ID</span><span class="sxs-lookup"><span data-stu-id="c96d0-114">Impairment test ID</span></span>
 - <span data-ttu-id="c96d0-115">資産グループ番号</span><span class="sxs-lookup"><span data-stu-id="c96d0-115">Cash generating unit number</span></span>        

## <a name="set-up-posting-profile"></a><span data-ttu-id="c96d0-116">転記プロファイルを設定</span><span class="sxs-lookup"><span data-stu-id="c96d0-116">Set up posting profile</span></span>
1. <span data-ttu-id="c96d0-117">[固定資産] > [設定] > [固定資産転記プロファイル] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c96d0-117">Go to Fixed assets > Setup > Fixed asset posting profiles.</span></span>
2. <span data-ttu-id="c96d0-118">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c96d0-118">Click Edit.</span></span>
3. <span data-ttu-id="c96d0-119">[減損管理] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c96d0-119">Expand the Impairment management section.</span></span>
4. <span data-ttu-id="c96d0-120">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c96d0-120">Click Add.</span></span>
5. <span data-ttu-id="c96d0-121">[帳簿] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c96d0-121">In the Book field, type a value.</span></span>
6. <span data-ttu-id="c96d0-122">[グループ化] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c96d0-122">In the Groupings field, select an option.</span></span>
7. <span data-ttu-id="c96d0-123">[固定資産番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c96d0-123">In the Fixed asset number field, type a value.</span></span>
8. <span data-ttu-id="c96d0-124">[主勘定] フィールドに、目的の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="c96d0-124">In the Main account field, specify the desired values.</span></span>
9. <span data-ttu-id="c96d0-125">[相殺勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="c96d0-125">In the Offset account field, specify the desired values.</span></span>
10. <span data-ttu-id="c96d0-126">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c96d0-126">Click Save.</span></span>

