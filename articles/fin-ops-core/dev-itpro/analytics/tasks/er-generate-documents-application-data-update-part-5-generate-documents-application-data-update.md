---
title: アプリケーション データを含むドキュメントの生成
description: この手順のステップを完了するには、まず 「ER アプリケーション データ更新と共にドキュメントを生成する（パート 4 - 形式の変更）」 に記載の手順を完了する必要があります。
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a2643c85e64373e30aab16be686c50cd224490fe
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684478"
---
# <a name="generate-documents-that-have-application-data"></a><span data-ttu-id="3fe5d-103">アプリケーション データを含むドキュメントを生成する</span><span class="sxs-lookup"><span data-stu-id="3fe5d-103">Generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3fe5d-104">この手順のステップを完了するには、まず 「ER アプリケーション データ更新と共にドキュメントを生成する（パート 4：形式の変更）」 に記載の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3fe5d-104">To complete the steps in this procedure, you must first complete the procedure, "ER Generate documents with application data update (Part 4: Modify format)".</span></span>



<span data-ttu-id="3fe5d-105">この手順のステップでは、電子ドキュメントを生成してアプリケーション データを更新するために電子申告 (ER) コンフィギュレーションを設計する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3fe5d-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="3fe5d-106">この手順では、ER 形式コンフィギュレーションを実行して、イントラスタット レポートを生成し、レポート プロセスの詳細をアーカイブするためのアプリケーション データを更新します。</span><span class="sxs-lookup"><span data-stu-id="3fe5d-106">In this procedure, you execute the ER format configuration to generate the Intrastat report and update application data for archiving details of the reporting process.</span></span>



<span data-ttu-id="3fe5d-107">この手順は、「システム管理者」または「電子レポート開発者」ロールが割り当てられているユーザー用に作成されています。</span><span class="sxs-lookup"><span data-stu-id="3fe5d-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="3fe5d-108">これらのステップは、DEMF データ セットを使用して完了することができます。</span><span class="sxs-lookup"><span data-stu-id="3fe5d-108">These steps can be completed using the DEMF dataset.</span></span> <span data-ttu-id="3fe5d-109">開始する前に、DEMF 会社の国コンテキストが BEL (ベルギー) であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="3fe5d-109">Before you begin, make sure that the country context for the DEMF company is BEL (Belgium).</span></span>


## <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="3fe5d-110">対外貿易パラメーターの設定</span><span class="sxs-lookup"><span data-stu-id="3fe5d-110">Set up foreign trade parameters</span></span>
1. <span data-ttu-id="3fe5d-111">[税] > [設定] > [対外貿易] > [対外貿易パラメーター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3fe5d-111">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
2. <span data-ttu-id="3fe5d-112">[番号順序] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="3fe5d-112">Click the Number sequences tab.</span></span>

    <span data-ttu-id="3fe5d-113">イントラスタット レポート プロセスの詳細をアーカイブするのに、作成した各アーカイブのレコードを特定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3fe5d-113">Archiving details of Intrastat reporting process, we need to identify records of each archive we created.</span></span> <span data-ttu-id="3fe5d-114">そのためには特別な番号順序をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3fe5d-114">A special number sequence must be configured for that.</span></span>  

3. <span data-ttu-id="3fe5d-115">「イントラスタット アーカイブ ID」 の参照を選択します。</span><span class="sxs-lookup"><span data-stu-id="3fe5d-115">Select the 'Intrastat archive ID' reference.</span></span>
4. <span data-ttu-id="3fe5d-116">[番号順序コード] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3fe5d-116">In the Number sequence code field, type a value.</span></span>

    <span data-ttu-id="3fe5d-117">[番号シーケンス コード] フィールドに、 「Fore_2」 という値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="3fe5d-117">In the 'Number sequence code' field, enter or select the value 'Fore_2'.</span></span>  

5. <span data-ttu-id="3fe5d-118">ResolveChanges 番号順序コード。</span><span class="sxs-lookup"><span data-stu-id="3fe5d-118">ResolveChanges the Number sequence code.</span></span>
6. <span data-ttu-id="3fe5d-119">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3fe5d-119">Click Save.</span></span>
7. <span data-ttu-id="3fe5d-120">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3fe5d-120">Close the page.</span></span>

## <a name="run-modified-er-format"></a><span data-ttu-id="3fe5d-121">変更された ER 形式を実行する</span><span class="sxs-lookup"><span data-stu-id="3fe5d-121">Run modified ER format</span></span>
1. <span data-ttu-id="3fe5d-122">[組織管理] > [電子申告] > [コンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="3fe5d-122">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="3fe5d-123">ツリーで、「イントラスタット (モデル)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="3fe5d-123">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="3fe5d-124">ツリーで、「イントラスタット (モデル)\イントラスタット (形式)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="3fe5d-124">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="3fe5d-125">[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3fe5d-125">Click Run.</span></span>
5. <span data-ttu-id="3fe5d-126">[ファイル名を入力] フィールドに、「intrastat2.xml」と入力します。</span><span class="sxs-lookup"><span data-stu-id="3fe5d-126">In the Enter file name field, type 'intrastat2.xml'.</span></span>
6. <span data-ttu-id="3fe5d-127">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3fe5d-127">Click OK.</span></span>

## <a name="review-er-format-executions-results"></a><span data-ttu-id="3fe5d-128">ER 形式の実行結果を確認する</span><span class="sxs-lookup"><span data-stu-id="3fe5d-128">Review ER format execution's results</span></span>
<span data-ttu-id="3fe5d-129">生成した XML ファイルを確認します。</span><span class="sxs-lookup"><span data-stu-id="3fe5d-129">Review the generated XML file.</span></span>  
1. <span data-ttu-id="3fe5d-130">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3fe5d-130">Close the page.</span></span>
2. <span data-ttu-id="3fe5d-131">[税] > [申告] > [対外貿易] > [イントラスタット] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3fe5d-131">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>

    <span data-ttu-id="3fe5d-132">生成した電子ドキュメントに含まれているイントラスタット トランザクションを含むこのフォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="3fe5d-132">Open this form containing Intrastat transactions that have been included to the generated electronic document.</span></span>  

3. <span data-ttu-id="3fe5d-133">[イントラスタット アーカイブ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3fe5d-133">Click Intrastat archive.</span></span>

    <span data-ttu-id="3fe5d-134">実行された ER 形式にはアプリケーション データ更新の設定が含まれているので、完了したイントラスタット レポートの詳細はアーカイブされました。</span><span class="sxs-lookup"><span data-stu-id="3fe5d-134">Since the executed ER format contains now settings for application data update, the details of the completed Intrastat reporting have been archived.</span></span> <span data-ttu-id="3fe5d-135">このフォームでは、作成したアーカイブのヘッダー レコードを表示できます。</span><span class="sxs-lookup"><span data-stu-id="3fe5d-135">In this form, you can see the header record of the created archive.</span></span>  

4. <span data-ttu-id="3fe5d-136">[詳細] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3fe5d-136">Click Details.</span></span>

    <span data-ttu-id="3fe5d-137">このフォームでは、作成したアーカイブの詳細を表示できます。</span><span class="sxs-lookup"><span data-stu-id="3fe5d-137">In this form, you can see the details for the created archive.</span></span>  

5. <span data-ttu-id="3fe5d-138">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3fe5d-138">Close the page.</span></span>
6. <span data-ttu-id="3fe5d-139">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3fe5d-139">Close the page.</span></span>
7. <span data-ttu-id="3fe5d-140">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3fe5d-140">Close the page.</span></span>

