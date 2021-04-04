---
title: 分析コードベースの製品マスターのリリース
description: この手順では、分析コード ベースのコンフィギュレーションに使用する製品マスターをリリースする方法を示します。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductRelease
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 786083e4befdb9ebe081b1238c5eb2179b32e01a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258617"
---
# <a name="release-a-dimension-based-product-master"></a><span data-ttu-id="222ec-103">分析コードベースの製品マスターのリリース</span><span class="sxs-lookup"><span data-stu-id="222ec-103">Release a dimension-based product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="222ec-104">この手順では、分析コード ベースのコンフィギュレーションに使用する製品マスターをリリースする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="222ec-104">This procedure shows how to release a product master, which will be used for the dimension-based configurations.</span></span> <span data-ttu-id="222ec-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="222ec-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="222ec-106">事前に分析コード ベースのコンフィギュレーション テクノロジで製品マスターを作成しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="222ec-106">It is a prerequisite that you have created a product master with the dimension-based configuration technology.</span></span> <span data-ttu-id="222ec-107">これは、分析コードベースのコンフィギュレーションでの組み合わせの作成方法を説明する 8 つの手順の 2 番目です。</span><span class="sxs-lookup"><span data-stu-id="222ec-107">This is the second procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span>

1. <span data-ttu-id="222ec-108">[製品情報管理] > [製品] > [製品マスター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="222ec-108">Go to Product information management > Products > Product masters.</span></span>
    * <span data-ttu-id="222ec-109">分析コード ベースのコンフィギュレーションだけが表示されるように [コンフィギュレーション テクノロジ] の列をフィルタ処理します。</span><span class="sxs-lookup"><span data-stu-id="222ec-109">Filter the Configuration technology column so that only the dimension-based configuration is displayed.</span></span> <span data-ttu-id="222ec-110">たとえば、「分析コード」と入力することによって、列をフィルタ処理できます。</span><span class="sxs-lookup"><span data-stu-id="222ec-110">For example, you can filter the column by typing Dimension.</span></span>    
2. <span data-ttu-id="222ec-111">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="222ec-111">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="222ec-112">[製品のリリース] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="222ec-112">Click Release products.</span></span>
4. <span data-ttu-id="222ec-113">[次へ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="222ec-113">Click Next.</span></span>
    * <span data-ttu-id="222ec-114">分析コード ベースのコンフィギュレーション テクノロジで作成された製品の製品バリアントは、部品表を作成した会社で作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="222ec-114">For products that are crated with the dimension-based configuration technology, the product variants must be created in the company where the bill of materials will be created.</span></span>  
5. <span data-ttu-id="222ec-115">[次へ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="222ec-115">Click Next.</span></span>
6. <span data-ttu-id="222ec-116">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="222ec-116">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="222ec-117">この手順のために、USMF 会社を選択します。</span><span class="sxs-lookup"><span data-stu-id="222ec-117">Select the company USMF for this procedure.</span></span>  
7. <span data-ttu-id="222ec-118">[次へ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="222ec-118">Click Next.</span></span>
8. <span data-ttu-id="222ec-119">[完了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="222ec-119">Click Finish.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]