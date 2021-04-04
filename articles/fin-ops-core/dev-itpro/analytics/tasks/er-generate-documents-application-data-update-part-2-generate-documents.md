---
title: アプリケーション データを含むドキュメントを生成するためのコンフィギュレーションのデザイン
description: このトピックでは、電子ドキュメントを生成するために電子申告 (ER) コンフィギュレーションをデザインする方法について説明します。 (パート 1 - コンフィギュレーションのインポート)。
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 217eca9bd1502d4327857720fb2d32a3ec3508ef
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563177"
---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a><span data-ttu-id="17ca3-104">アプリケーション データを含むドキュメントを生成するためのコンフィギュレーションのデザイン</span><span class="sxs-lookup"><span data-stu-id="17ca3-104">Design configurations to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="17ca3-105">この手順のステップを完了するには、まず「ER アプリケーション データ更新と共にドキュメントを生成する (パート 1: コンフィギュレーションのインポート)」の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="17ca3-105">To complete the steps in this procedure, you must first complete the procedure, ER Generate documents with application data update (Part 1: Import configurations).</span></span>



<span data-ttu-id="17ca3-106">この手順のステップでは、電子ドキュメントを生成するために電子申告 (ER) コンフィギュレーションを設計する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="17ca3-106">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document.</span></span> <span data-ttu-id="17ca3-107">この手順では、サンプル会社 Litware, Inc. 用に作成された ER インポート済形式コンフィギュレーションを実行して、電子ドキュメントを生成します。</span><span class="sxs-lookup"><span data-stu-id="17ca3-107">In this procedure, you run the ER imported format configuration that has been created for the sample company, Litware, Inc. to generate electronic documents.</span></span>



<span data-ttu-id="17ca3-108">この手順は、「システム管理者」または「電子レポート開発者」ロールが割り当てられているユーザー用に作成されています。</span><span class="sxs-lookup"><span data-stu-id="17ca3-108">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="17ca3-109">これらのステップは、DEMF データ セットを使用して完了することができます。</span><span class="sxs-lookup"><span data-stu-id="17ca3-109">These steps can be completed using the DEMF dataset.</span></span> 



<span data-ttu-id="17ca3-110">開始する前に、DEMF 会社の国コンテキストを DEU (ドイツ) から BEL (ベルギー) に変更します。</span><span class="sxs-lookup"><span data-stu-id="17ca3-110">Before you begin, change the country context for the DEMF company from DEU (Germany) to BEL (Belgium).</span></span> <span data-ttu-id="17ca3-111">[組織管理] > [組織] > [法人] をクリックして、法人 DEMF の基本住所にある国コードを更新します。</span><span class="sxs-lookup"><span data-stu-id="17ca3-111">Click Organization administration > Organizations > Legal entities to update the country code in the primary address of the legal entity DEMF.</span></span> <span data-ttu-id="17ca3-112">アプリケーションを再起動します。</span><span class="sxs-lookup"><span data-stu-id="17ca3-112">Restart your application.</span></span>


## <a name="run-imported-er-format"></a><span data-ttu-id="17ca3-113">インポートされた ER 形式を実行する</span><span class="sxs-lookup"><span data-stu-id="17ca3-113">Run imported ER format</span></span>
1. <span data-ttu-id="17ca3-114">[組織管理] > [電子申告] > [コンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="17ca3-114">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="17ca3-115">ツリーで、「イントラスタット (モデル)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="17ca3-115">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="17ca3-116">ツリーで、「イントラスタット (モデル)\イントラスタット (形式)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="17ca3-116">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="17ca3-117">[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="17ca3-117">Click Run.</span></span>
    * <span data-ttu-id="17ca3-118">イントラスタット レポートを生成するために、ER 形式コンフィギュレーションのドラフト バージョンを実行します。</span><span class="sxs-lookup"><span data-stu-id="17ca3-118">Run the draft version of the ER format configuration to generate the Intrastat report.</span></span>  
5. <span data-ttu-id="17ca3-119">[ファイル名を入力] フィールドに、「intrastat.xml」と入力します。</span><span class="sxs-lookup"><span data-stu-id="17ca3-119">In the Enter file name field, type 'intrastat.xml'.</span></span>
    * <span data-ttu-id="17ca3-120">ファイルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="17ca3-120">Specify the name of the file.</span></span>  
6. <span data-ttu-id="17ca3-121">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="17ca3-121">Click OK.</span></span>
    * <span data-ttu-id="17ca3-122">生成した XML ファイルを確認します。</span><span class="sxs-lookup"><span data-stu-id="17ca3-122">Review the generated XML file.</span></span>  
7. <span data-ttu-id="17ca3-123">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="17ca3-123">Close the page.</span></span>
8. <span data-ttu-id="17ca3-124">[税] > [申告] > [対外貿易] > [イントラスタット] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="17ca3-124">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="17ca3-125">このフォームを開いて、生成した電子ドキュメントに含まれるイントラスタット トランザクションを表示します。</span><span class="sxs-lookup"><span data-stu-id="17ca3-125">Open this form to view the Intrastat transactions that are included in the generated electronic document.</span></span>  
9. <span data-ttu-id="17ca3-126">[イントラスタット アーカイブ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="17ca3-126">Click Intrastat archive.</span></span>
    * <span data-ttu-id="17ca3-127">実行した ER 形式にアプリケーション データ更新の設定が含まれていないため、完了したイントラスタット レポートの詳細はアーカイブされていません。</span><span class="sxs-lookup"><span data-stu-id="17ca3-127">Because the executed ER format does not contain any settings for application data update, the details of the completed Intrastat report have not been archived.</span></span>  
10. <span data-ttu-id="17ca3-128">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="17ca3-128">Close the page.</span></span>
11. <span data-ttu-id="17ca3-129">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="17ca3-129">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]