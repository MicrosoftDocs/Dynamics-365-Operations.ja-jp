---
title: 減損会計の共通パラメーターおよび転記プロファイルの設定
description: このタスクでは、減損会計の共通パラメーターと転記プロファイルの定義方法が確認できます。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, AssetPosting
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f5bf676d03d5561d26ce84bbf64010e321725a49
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "371034"
---
# <a name="setup-impairment-accounting-common-parameters-and-posting-profile"></a><span data-ttu-id="26281-103">減損会計の共通パラメーターおよび転記プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="26281-103">Setup impairment accounting common parameters and posting profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="26281-104">このタスクでは、減損会計の共通パラメーターと転記プロファイルの定義方法が確認できます。</span><span class="sxs-lookup"><span data-stu-id="26281-104">Use this task to learn how to define impairment accounting common parameters and posting profiles.</span></span>



<span data-ttu-id="26281-105">このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="26281-105">To complete this task, the Fixed Assets configuration key must be selected.</span></span>



<span data-ttu-id="26281-106">この手順では、JPMF デモ会社のデータを使用します。</span><span class="sxs-lookup"><span data-stu-id="26281-106">This procedure uses the JPMF demo company data.</span></span>


## <a name="set-up-impairment-parameters"></a><span data-ttu-id="26281-107">減損パラメーターを設定</span><span class="sxs-lookup"><span data-stu-id="26281-107">Set up impairment parameters</span></span>
1. <span data-ttu-id="26281-108">[固定資産] > [設定] > [固定資産パラメーター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="26281-108">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="26281-109">[減損管理] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="26281-109">Expand the Impairment management section.</span></span>
3. <span data-ttu-id="26281-110">[警告期間 (月数) ] フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="26281-110">In the Warning period (in months) field, enter a number.</span></span>
    * <span data-ttu-id="26281-111">例: 6 か月</span><span class="sxs-lookup"><span data-stu-id="26281-111">Example: 6 months</span></span>  
4. <span data-ttu-id="26281-112">[番号順序] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="26281-112">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="26281-113">次の番号順序コードが設定されていることを確認します: •減損のドキュメント ID •減損テスト ID •キャッシュ生成単位番号</span><span class="sxs-lookup"><span data-stu-id="26281-113">Confirm the following Number sequence codes are set up:  •Document ID for impairment  •Impairment test ID  •Cash generating unit number</span></span>        
    *   

## <a name="set-up-posting-profile"></a><span data-ttu-id="26281-114">転記プロファイルを設定</span><span class="sxs-lookup"><span data-stu-id="26281-114">Set up posting profile</span></span>
1. <span data-ttu-id="26281-115">[固定資産] > [設定] > [固定資産転記プロファイル] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="26281-115">Go to Fixed assets > Setup > Fixed asset posting profiles.</span></span>
2. <span data-ttu-id="26281-116">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="26281-116">Click Edit.</span></span>
3. <span data-ttu-id="26281-117">[減損管理] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="26281-117">Expand the Impairment management section.</span></span>
4. <span data-ttu-id="26281-118">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="26281-118">Click Add.</span></span>
5. <span data-ttu-id="26281-119">[帳簿] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="26281-119">In the Book field, type a value.</span></span>
6. <span data-ttu-id="26281-120">[グループ化] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="26281-120">In the Groupings field, select an option.</span></span>
7. <span data-ttu-id="26281-121">[固定資産番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="26281-121">In the Fixed asset number field, type a value.</span></span>
8. <span data-ttu-id="26281-122">[主勘定] フィールドに、目的の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="26281-122">In the Main account field, specify the desired values.</span></span>
9. <span data-ttu-id="26281-123">[相殺勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="26281-123">In the Offset account field, specify the desired values.</span></span>
10. <span data-ttu-id="26281-124">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="26281-124">Click Save.</span></span>

