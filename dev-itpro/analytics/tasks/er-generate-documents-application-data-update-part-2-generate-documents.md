--- 
title: "電子申告 (ER) のアプリケーション データ更新と共にドキュメントを生成する"
description: "この手順のステップを完了するには、まず「ER アプリケーション データ更新と共にドキュメントを生成する (パート 1 - コンフィギュレーションのインポート)」の手順を完了する必要があります。"
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: aa737abc9273e0068d864416ffb85302468088ed
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="generate-documents-with-application-data-update-for-electronic-reporting-er"></a><span data-ttu-id="52f3e-103">電子申告 (ER) のアプリケーション データ更新と共にドキュメントを生成する</span><span class="sxs-lookup"><span data-stu-id="52f3e-103">Generate documents with application data update for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="52f3e-104">この手順のステップを完了するには、まず「ER アプリケーション データ更新と共にドキュメントを生成する (パート 1: コンフィギュレーションのインポート)」の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="52f3e-104">To complete the steps in this procedure, you must first complete the procedure, ER Generate documents with application data update (Part 1: Import configurations).</span></span>



<span data-ttu-id="52f3e-105">この手順のステップでは、電子ドキュメントを生成するために電子申告 (ER) コンフィギュレーションを設計する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="52f3e-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document.</span></span> <span data-ttu-id="52f3e-106">この手順では、サンプル会社 Litware, Inc. 用に作成された ER インポート済形式コンフィギュレーションを実行して、電子ドキュメントを生成します。</span><span class="sxs-lookup"><span data-stu-id="52f3e-106">In this procedure, you run the ER imported format configuration that has been created for the sample company, Litware, Inc. to generate electronic documents.</span></span>



<span data-ttu-id="52f3e-107">この手順は、「システム管理者」または「電子レポート開発者」ロールが割り当てられているユーザー用に作成されています。</span><span class="sxs-lookup"><span data-stu-id="52f3e-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="52f3e-108">これらのステップは、DEMF データ セットを使用して完了することができます。</span><span class="sxs-lookup"><span data-stu-id="52f3e-108">These steps can be completed using the DEMF dataset.</span></span> 



<span data-ttu-id="52f3e-109">開始する前に、DEMF 会社の国コンテキストを DEU (ドイツ) から BEL (ベルギー) に変更します。</span><span class="sxs-lookup"><span data-stu-id="52f3e-109">Before you begin, change the country context for the DEMF company from DEU (Germany) to BEL (Belgium).</span></span> <span data-ttu-id="52f3e-110">[組織管理] > [組織] > [法人] をクリックして、法人 DEMF の基本住所にある国コードを更新します。</span><span class="sxs-lookup"><span data-stu-id="52f3e-110">Click Organization administration > Organizations > Legal entities to update the country code in the primary address of the legal entity DEMF.</span></span> <span data-ttu-id="52f3e-111">アプリケーションを再起動します。</span><span class="sxs-lookup"><span data-stu-id="52f3e-111">Restart your application.</span></span>


## <a name="run-imported-er-format"></a><span data-ttu-id="52f3e-112">インポートされた ER 形式を実行する</span><span class="sxs-lookup"><span data-stu-id="52f3e-112">Run imported ER format</span></span>
1. <span data-ttu-id="52f3e-113">[組織管理] > [電子申告] > [コンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="52f3e-113">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="52f3e-114">ツリーで、「イントラスタット (モデル)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="52f3e-114">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="52f3e-115">ツリーで、「イントラスタット (モデル)\イントラスタット (形式)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="52f3e-115">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="52f3e-116">[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="52f3e-116">Click Run.</span></span>
    * <span data-ttu-id="52f3e-117">イントラスタット レポートを生成するために、ER 形式コンフィギュレーションのドラフト バージョンを実行します。</span><span class="sxs-lookup"><span data-stu-id="52f3e-117">Run the draft version of the ER format configuration to generate the Intrastat report.</span></span>  
5. <span data-ttu-id="52f3e-118">[ファイル名を入力] フィールドに、「intrastat.xml」と入力します。</span><span class="sxs-lookup"><span data-stu-id="52f3e-118">In the Enter file name field, type 'intrastat.xml'.</span></span>
    * <span data-ttu-id="52f3e-119">ファイルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="52f3e-119">Specify the name of the file.</span></span>  
6. <span data-ttu-id="52f3e-120">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="52f3e-120">Click OK.</span></span>
    * <span data-ttu-id="52f3e-121">生成した XML ファイルを確認します。</span><span class="sxs-lookup"><span data-stu-id="52f3e-121">Review the generated XML file.</span></span>  
7. <span data-ttu-id="52f3e-122">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="52f3e-122">Close the page.</span></span>
8. <span data-ttu-id="52f3e-123">[税] > [申告] > [対外貿易] > [イントラスタット] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="52f3e-123">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="52f3e-124">このフォームを開いて、生成した電子ドキュメントに含まれるイントラスタット トランザクションを表示します。</span><span class="sxs-lookup"><span data-stu-id="52f3e-124">Open this form to view the Intrastat transactions that are included in the generated electronic document.</span></span>  
9. <span data-ttu-id="52f3e-125">[イントラスタット アーカイブ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="52f3e-125">Click Intrastat archive.</span></span>
    * <span data-ttu-id="52f3e-126">実行した ER 形式にアプリケーション データ更新の設定が含まれていないため、完了したイントラスタット レポートの詳細はアーカイブされていません。</span><span class="sxs-lookup"><span data-stu-id="52f3e-126">Because the executed ER format does not contain any settings for application data update, the details of the completed Intrastat report have not been archived.</span></span>  
10. <span data-ttu-id="52f3e-127">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="52f3e-127">Close the page.</span></span>
11. <span data-ttu-id="52f3e-128">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="52f3e-128">Close the page.</span></span>


