---
title: TaxTrans の正しくないフィールド値
description: このトピックでは、TaxTrans の正しくないフィールド値のトラブルシューティングに関する情報を提供します。
author: bijian
manager: beya
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 97f9bb24d32180f2fccb69c5a13e2aa0349c1ee4
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947666"
---
# <a name="incorrect-field-value-in-taxtrans"></a><span data-ttu-id="f5aa6-103">TaxTrans の正しくないフィールド値</span><span class="sxs-lookup"><span data-stu-id="f5aa6-103">Incorrect field value in TaxTrans</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f5aa6-104">**TaxTrans** のフィールド値が正しくない場合は、このトピックの情報を使用して問題を解決してください。</span><span class="sxs-lookup"><span data-stu-id="f5aa6-104">If a field value in **TaxTrans** is incorrect, use the information in this topic to try to resolve the issue.</span></span>

## <a name="overview-of-values"></a><span data-ttu-id="f5aa6-105">値の概要</span><span class="sxs-lookup"><span data-stu-id="f5aa6-105">Overview of values</span></span>
<span data-ttu-id="f5aa6-106">次のリストは、**TaxTrans**、**TaxUncommitted**、および **TmpTaxWorkTrans** がどのように類似したデータ セットであるかを示していますが、動作が異なります。</span><span class="sxs-lookup"><span data-stu-id="f5aa6-106">The following list shows how **TaxTrans**, **TaxUncommitted**, and **TmpTaxWorkTrans** are similar data sets, but in work differently.</span></span>

  - <span data-ttu-id="f5aa6-107">**TaxTrans** は、データベースに保持される最終的な転記された税トランザクションの結果です。</span><span class="sxs-lookup"><span data-stu-id="f5aa6-107">**TaxTrans** is the final posted tax transaction result persisted in the database.</span></span>
  - <span data-ttu-id="f5aa6-108">**TaxUncommitted** は、データベースに保持される中間計算税結果 (該当する場合) であり、後で転記に使用されます。</span><span class="sxs-lookup"><span data-stu-id="f5aa6-108">**TaxUncommitted** is the intermediate calculated tax result persisted in the database (if applicable), which will be used later in posting.</span></span>
  - <span data-ttu-id="f5aa6-109">**TmpTaxWorkTrans** は、メモリ内テーブル (テーブル タイプ = InMemory) で一時的に計算された税の結果です。</span><span class="sxs-lookup"><span data-stu-id="f5aa6-109">**TmpTaxWorkTrans** is the temporary calculated tax result in the in-memory table (Table Type = InMemory).</span></span>

<span data-ttu-id="f5aa6-110">正しくない **TaxTrans** 列の根本原因が見つかった場合は、正しくない **TaxUncommitted** 列または **TmpTaxWorkTrans** 列の根本原因も見つけました。</span><span class="sxs-lookup"><span data-stu-id="f5aa6-110">If you find the root cause of an incorrect **TaxTrans** column, you've also found the root cause of an incorrect **TaxUncommitted** or **TmpTaxWorkTrans** column.</span></span> <span data-ttu-id="f5aa6-111">これは、3 つの列が互いにコピーされているためです。</span><span class="sxs-lookup"><span data-stu-id="f5aa6-111">This is because the three columns are copied from each other.</span></span>

<span data-ttu-id="f5aa6-112">通常、税額計算時に **TmpTaxWorkTrans** が生成され、該当する場合は **TaxUncommitted** が生成されます。</span><span class="sxs-lookup"><span data-stu-id="f5aa6-112">Typically, during tax calculation, **TmpTaxWorkTrans** is generated, and then, if applicable, **TaxUncommitted** is generated.</span></span> <span data-ttu-id="f5aa6-113">税転記時に、**TaxTrans** が生成されます。</span><span class="sxs-lookup"><span data-stu-id="f5aa6-113">During tax posting, **TaxTrans** is generated.</span></span>


## <a name="add-breakpoints"></a><span data-ttu-id="f5aa6-114">ブレークポイントの追加</span><span class="sxs-lookup"><span data-stu-id="f5aa6-114">Add breakpoints</span></span>
<span data-ttu-id="f5aa6-115">ブレークポイントを追加するには、次の手順を完了してください。</span><span class="sxs-lookup"><span data-stu-id="f5aa6-115">To add breakpoints, complete the following steps:</span></span> 

1. <span data-ttu-id="f5aa6-116">次に示すように、拡張機能の *insert()* および *update()* に拡張機能とブレークポイントを追加します。</span><span class="sxs-lookup"><span data-stu-id="f5aa6-116">Add extensions and breakpoints in *insert()* and *update()* in the extensions as shown below.</span></span>

     - <span data-ttu-id="f5aa6-117">**TaxTrans**</span><span class="sxs-lookup"><span data-stu-id="f5aa6-117">**TaxTrans**</span></span>

        ```x++
        [ExtensionOf(tableStr(TaxTrans))]
        public final class TaxTrans_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - <span data-ttu-id="f5aa6-118">**TaxUncommitted**</span><span class="sxs-lookup"><span data-stu-id="f5aa6-118">**TaxUncommitted**</span></span>

        ```x++
        [ExtensionOf(tableStr(TaxUncommitted))]
        public final class TaxUncommitted_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - <span data-ttu-id="f5aa6-119">**TmpTaxWorkTrans**</span><span class="sxs-lookup"><span data-stu-id="f5aa6-119">**TmpTaxWorkTrans**</span></span>

        ```x++
        [ExtensionOf(tableStr(TmpTaxWorkTrans))]
        public final class TmpTaxWorkTrans_Extension
        {
            public void insert(boolean _ignoreCalculatedSalesTax)
            {
                next insert(_ignoreCalculatedSalesTax);
            }
        
            public void update(boolean _ignoreCalculatedSalesTax)
            {
                next update(_ignoreCalculatedSalesTax);
            }
        
        }
        
        ```

2. <span data-ttu-id="f5aa6-120">または、**TaxUncommitted** が含まれていない場合、ブレークポイントを直接追加できます。</span><span class="sxs-lookup"><span data-stu-id="f5aa6-120">Alternatively, you can add breakpoints directly when **TaxUncommitted** is not included.</span></span>

     - <span data-ttu-id="f5aa6-121">*TaxTrans.insert()*、*TaxTrans.update()*</span><span class="sxs-lookup"><span data-stu-id="f5aa6-121">*TaxTrans.insert()*, *TaxTrans.update()*</span></span>
     - <span data-ttu-id="f5aa6-122">*TmpTaxWorkTrans.insert()*、*TmpTaxWorkTrans.update()*</span><span class="sxs-lookup"><span data-stu-id="f5aa6-122">*TmpTaxWorkTrans.insert()*, *TmpTaxWorkTrans.update()*</span></span>

## <a name="reproduce-and-debug"></a><span data-ttu-id="f5aa6-123">再現とデバッグ</span><span class="sxs-lookup"><span data-stu-id="f5aa6-123">Reproduce and debug</span></span>

<span data-ttu-id="f5aa6-124">ブレークポイントが設定された後、デバッグ中にすべてのデータ持続性の変更が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f5aa6-124">After the breakpoints are set, every data persistency change is visible during debugging.</span></span> <span data-ttu-id="f5aa6-125">**TaxTrans**、**TaxUncommitted**、または **TmpTaxWorkTrans** の正しくない列の根本原因を見つけるには、次の項目を確認してメモします。</span><span class="sxs-lookup"><span data-stu-id="f5aa6-125">To find the root cause of an incorrect column of **TaxTrans**, **TaxUncommitted**, or **TmpTaxWorkTrans**, review and note the following items:</span></span>

- <span data-ttu-id="f5aa6-126">列が正しい最後のブレークポイント。</span><span class="sxs-lookup"><span data-stu-id="f5aa6-126">The last breakpoint where the column is correct.</span></span>
- <span data-ttu-id="f5aa6-127">列が正しくない最初のブレークポイント。</span><span class="sxs-lookup"><span data-stu-id="f5aa6-127">The first breakpoint where the column is incorrect.</span></span>
- <span data-ttu-id="f5aa6-128">これらの 2 つのポイントの間に何が起こるか。</span><span class="sxs-lookup"><span data-stu-id="f5aa6-128">What happens in between those two points.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="f5aa6-129">カスタマイズが存在するかどうかの確認</span><span class="sxs-lookup"><span data-stu-id="f5aa6-129">Determine whether customization exists</span></span>
<span data-ttu-id="f5aa6-130">前のセクションの手順を完了しても問題を解決できない場合は、カスタマイズが存在するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="f5aa6-130">If you've completed the steps in the previous sections but have not been able to resolve the issue, determine whether customization exists.</span></span> <span data-ttu-id="f5aa6-131">カスタマイズが存在しない場合は、Microsoft サポートに問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="f5aa6-131">If no customization exists, contact Microsoft Support for assistance.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

