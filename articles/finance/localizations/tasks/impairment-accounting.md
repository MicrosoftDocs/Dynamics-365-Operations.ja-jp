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
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 06bc9f2361010c2320f0bdda22a17a4a8668ff29
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140059"
---
# <a name="setup-impairment-accounting-common-parameters-and-posting-profile"></a><span data-ttu-id="83126-103">減損会計の共通パラメーターおよび転記プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="83126-103">Setup impairment accounting common parameters and posting profile</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="83126-104">このタスクでは、減損会計の共通パラメーターと転記プロファイルの定義方法が確認できます。</span><span class="sxs-lookup"><span data-stu-id="83126-104">Use this task to learn how to define impairment accounting common parameters and posting profiles.</span></span>



<span data-ttu-id="83126-105">このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="83126-105">To complete this task, the Fixed Assets configuration key must be selected.</span></span>



<span data-ttu-id="83126-106">この手順では、JPMF デモ会社のデータを使用します。</span><span class="sxs-lookup"><span data-stu-id="83126-106">This procedure uses the JPMF demo company data.</span></span>


## <a name="set-up-impairment-parameters"></a><span data-ttu-id="83126-107">減損パラメーターを設定</span><span class="sxs-lookup"><span data-stu-id="83126-107">Set up impairment parameters</span></span>
1. <span data-ttu-id="83126-108">[固定資産] > [設定] > [固定資産パラメーター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="83126-108">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="83126-109">[減損管理] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="83126-109">Expand the Impairment management section.</span></span>
3. <span data-ttu-id="83126-110">[警告期間 (月数) ] フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="83126-110">In the Warning period (in months) field, enter a number.</span></span>
    * <span data-ttu-id="83126-111">例: 6 か月</span><span class="sxs-lookup"><span data-stu-id="83126-111">Example: 6 months</span></span>  
4. <span data-ttu-id="83126-112">番号順序タブをクリックし、次の番号順序コードが設定されていることを確定します。</span><span class="sxs-lookup"><span data-stu-id="83126-112">Click the Number sequences tab. Confirm the following Number sequence codes are set up:</span></span>  
 - <span data-ttu-id="83126-113">減損のドキュメント ID</span><span class="sxs-lookup"><span data-stu-id="83126-113">Document ID for impairment</span></span>
 - <span data-ttu-id="83126-114">減損損失テスト ID</span><span class="sxs-lookup"><span data-stu-id="83126-114">Impairment test ID</span></span>
 - <span data-ttu-id="83126-115">資産グループ番号</span><span class="sxs-lookup"><span data-stu-id="83126-115">Cash generating unit number</span></span>        

## <a name="set-up-posting-profile"></a><span data-ttu-id="83126-116">転記プロファイルを設定</span><span class="sxs-lookup"><span data-stu-id="83126-116">Set up posting profile</span></span>
1. <span data-ttu-id="83126-117">[固定資産] > [設定] > [固定資産転記プロファイル] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="83126-117">Go to Fixed assets > Setup > Fixed asset posting profiles.</span></span>
2. <span data-ttu-id="83126-118">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="83126-118">Click Edit.</span></span>
3. <span data-ttu-id="83126-119">[減損管理] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="83126-119">Expand the Impairment management section.</span></span>
4. <span data-ttu-id="83126-120">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="83126-120">Click Add.</span></span>
5. <span data-ttu-id="83126-121">[帳簿] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="83126-121">In the Book field, type a value.</span></span>
6. <span data-ttu-id="83126-122">[グループ化] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="83126-122">In the Groupings field, select an option.</span></span>
7. <span data-ttu-id="83126-123">[固定資産番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="83126-123">In the Fixed asset number field, type a value.</span></span>
8. <span data-ttu-id="83126-124">[主勘定] フィールドに、目的の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="83126-124">In the Main account field, specify the desired values.</span></span>
9. <span data-ttu-id="83126-125">[相殺勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="83126-125">In the Offset account field, specify the desired values.</span></span>
10. <span data-ttu-id="83126-126">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="83126-126">Click Save.</span></span>

