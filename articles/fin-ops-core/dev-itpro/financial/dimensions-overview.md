---
title: Excel テンプレートへの分析コードの追加
description: このトピックでは、分析コード、エンティティを持つ分析コード、および使用できる分析コード コントロールについて説明します。
author: robinarh
manager: AnnBe
ms.date: 11/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 11314
ms.assetid: 20e6b97e-30ed-48d4-b63c-a073f80300b2
ms.search.region: Global
ms.author: rbrow
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e8340173a885ce1383fc2e89f0f3320b9c2495c7
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812014"
---
# <a name="add-dimensions-to-excel-templates"></a><span data-ttu-id="0af06-103">Excel テンプレートへの分析コードの追加</span><span class="sxs-lookup"><span data-stu-id="0af06-103">Add dimensions to Excel templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0af06-104">このトピックでは、分析コード、エンティティを持つ分析コード、および使用できる分析コード コントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="0af06-104">This topic provides information about dimensions, dimensions that have entities, and the dimension controls that are available.</span></span>

<span data-ttu-id="0af06-105">インストール後に Microsoft Excel テンプレートに存在する唯一の値は MainAccount です。</span><span class="sxs-lookup"><span data-stu-id="0af06-105">The only value that is present on Microsoft Excel templates after installation is the MainAccount.</span></span> <span data-ttu-id="0af06-106">これは、すべての顧客が持つ唯一の分析コード です。</span><span class="sxs-lookup"><span data-stu-id="0af06-106">This is the only dimension that all customers will have.</span></span> <span data-ttu-id="0af06-107">Microsoft Excel テンプレートに分析コードを追加するには、次の手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0af06-107">To add the dimensions to Microsoft Excel templates you need to complete the following steps:</span></span>

1.  <span data-ttu-id="0af06-108">DimensionCombinationEntity または DimensionSet エンティティに分析コードを追加します。</span><span class="sxs-lookup"><span data-stu-id="0af06-108">Add dimensions to the DimensionCombinationEntity or the DimensionSet entity.</span></span>
2.  <span data-ttu-id="0af06-109">個々の列に分析コードを配置する各テンプレートに分析コードを追加します。</span><span class="sxs-lookup"><span data-stu-id="0af06-109">Add the dimensions to each template where you want dimensions in separate columns.</span></span> <span data-ttu-id="0af06-110">詳細については、[Excel で開くエクスペリエンスの作成](../office-integration/office-integration-edit-excel.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0af06-110">For more information, see [Create Open in Excel experiences](../office-integration/office-integration-edit-excel.md).</span></span>
3. <span data-ttu-id="0af06-111">[Excel で財務分析コード値の検索機能](add-dimensions-excel-templates.md) を追加します。</span><span class="sxs-lookup"><span data-stu-id="0af06-111">Add the [capability to look up financial dimension values in Excel](add-dimensions-excel-templates.md).</span></span>
3.  <span data-ttu-id="0af06-112">テンプレートを公開します。</span><span class="sxs-lookup"><span data-stu-id="0af06-112">Publish the template.</span></span>

<span data-ttu-id="0af06-113">このトピックでは、DimensionCombinationEntity を変更して Excel の列で分析コードを有効にする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="0af06-113">This topic shows how to modify DimensionCombinationEntity to enable the dimensions in columns for Excel.</span></span> <span data-ttu-id="0af06-114">同じ手順を使用して DimensionSet エンティティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="0af06-114">The same steps can be used to modify the DimensionSet entity.</span></span> 

> [!NOTE]
> <span data-ttu-id="0af06-115">この情報は、リリースごとに変更されることがあります。</span><span class="sxs-lookup"><span data-stu-id="0af06-115">This information is subject to change for each release.</span></span> <span data-ttu-id="0af06-116">したがって、頻繁に最新の情報を確認してください。</span><span class="sxs-lookup"><span data-stu-id="0af06-116">Therefore, be sure to check back frequently for the most up-to-date information.</span></span>

## <a name="add-dimensions--before-dynamics-365-for-finance-and-operations"></a><span data-ttu-id="0af06-117">Dynamics 365 for Finance and Operations の前に分析コードを追加します。</span><span class="sxs-lookup"><span data-stu-id="0af06-117">Add dimensions  before Dynamics 365 for Finance and Operations</span></span>
<span data-ttu-id="0af06-118">たとえば、Microsoft Excel との統合で、列に配置する分析コードとの相互作用をサポートするには、最初にカスタムを使用して分析コードの列を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0af06-118">To support interactions with dimensions as columns, for example, in the Microsoft Excel integration, you must first create the dimension columns through a customization.</span></span> 

1. <span data-ttu-id="0af06-119">Visual Studio で、アプリケーション エクスプローラーを開きます (**表示**&gt;**アプリケーション エクスプローラー**)。</span><span class="sxs-lookup"><span data-stu-id="0af06-119">Open the Application Explorer in Visual Studio (**View** &gt; **Application Explorer**).</span></span> 
2. <span data-ttu-id="0af06-120">DimensionCombinationEntity **(AOT** &gt; **データ モデル** &gt; **データ エンティティ**) に移動します。</span><span class="sxs-lookup"><span data-stu-id="0af06-120">Navigate to DimensionCombinationEntity **(AOT** &gt; **Data Model** &gt; **Data Entities**).</span></span> 
3. <span data-ttu-id="0af06-121">エンティティを右クリックし、**カスタマイズ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0af06-121">Right-click on the entity and choose **Customize**.</span></span> 

    <span data-ttu-id="0af06-122">[![5](./media/5-300x187.png)](./media/5.png)</span><span class="sxs-lookup"><span data-stu-id="0af06-122">[![5](./media/5-300x187.png)](./media/5.png)</span></span>

4. <span data-ttu-id="0af06-123">変更するエンティティのデザイナー、この例では **DimensionCombinationEntity** を開きます。</span><span class="sxs-lookup"><span data-stu-id="0af06-123">Open the designer for the entity that you want to modify, in this example **DimensionCombinationEntity**.</span></span> 
5. <span data-ttu-id="0af06-124">**departmentValue** という名前の str を返す新しいプライベート静的メソッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="0af06-124">Create a new private static method that returns a str named **departmentValue**.</span></span> 
6. <span data-ttu-id="0af06-125">この方法では、**DimensionAttributeValueCombination** から分析コードの値を取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0af06-125">In this method, you must get the dimension's value from **DimensionAttributeValueCombination**.</span></span> <span data-ttu-id="0af06-126">最終的な方法はこのようになります。</span><span class="sxs-lookup"><span data-stu-id="0af06-126">The final method will look something like this.</span></span>

    ```
    /// <summary>
    /// This method returns the value of Department.
    /// </summary>
    private static str departmentValue()
    {     
        Name dimensionName = 'Department';
        str sqlStatement;

        DimensionAttribute dimensionAttribute = DimensionAttribute::findByName(dimensionName);

        if (!dimensionAttribute)
        {
            sqlStatement = SysComputedColumn::returnLiteral('');
        }
        else
        {
            sqlStatement = strFmt('SELECT TOP 1 T1.%1 ', dimensionAttribute.DimensionValueColumnName);
        }

        return sqlStatement;
    }
    ```

7. <span data-ttu-id="0af06-127">エンティティに新しい「マップされていない文字列フィールド」を作成します。</span><span class="sxs-lookup"><span data-stu-id="0af06-127">Create a new "string unmapped field" on the entity:</span></span>

   - <span data-ttu-id="0af06-128">**名前** プロパティを分析コード名 **部門** に設定します。</span><span class="sxs-lookup"><span data-stu-id="0af06-128">Set the **Name** property to the dimension name, **Department**.</span></span>
   - <span data-ttu-id="0af06-129">**拡張データ型** プロパティを **DimensionValue** に設定します。</span><span class="sxs-lookup"><span data-stu-id="0af06-129">Set the **Extended Data Type** property to **DimensionValue**.</span></span>
   - <span data-ttu-id="0af06-130">**DataEntityView メソッド** プロパティを、前の手順で作成したメソッドに設定します (たとえば、**departmentValue**)。</span><span class="sxs-lookup"><span data-stu-id="0af06-130">Set the **DataEntityView Method** property to the method that you created earlier (for example, **departmentValue**).</span></span>
   - <span data-ttu-id="0af06-131">**ラベル** プロパティを分析コード名 **部門** に設定します。</span><span class="sxs-lookup"><span data-stu-id="0af06-131">Set the **Label** property to the dimension name **Department**.</span></span>

     <span data-ttu-id="0af06-132">[![6](./media/6-300x64.png)](./media/6.png)</span><span class="sxs-lookup"><span data-stu-id="0af06-132">[![6](./media/6-300x64.png)](./media/6.png)</span></span>

8. <span data-ttu-id="0af06-133">分析コードの名前を適切な分析コードに変更することで、追加する分析コードごとに手順 5 ～ 7 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="0af06-133">Repeat steps 5-7 for each dimension that you want to add, changing the dimension name to the appropriate dimension.</span></span> 
9. <span data-ttu-id="0af06-134">プロジェクトをコンパイルし、データベースと同期します。</span><span class="sxs-lookup"><span data-stu-id="0af06-134">Compile the project, and then synchronize it with the database.</span></span> 

    <span data-ttu-id="0af06-135">[![8](./media/8-300x260.png)](./media/8.png)</span><span class="sxs-lookup"><span data-stu-id="0af06-135">[![8](./media/8-300x260.png)](./media/8.png)</span></span>

10. <span data-ttu-id="0af06-136">これで、カスタマイズは完了です。</span><span class="sxs-lookup"><span data-stu-id="0af06-136">Your customization is now complete.</span></span> <span data-ttu-id="0af06-137">次のステートメントを使用して、SQL でテストすることができます。</span><span class="sxs-lookup"><span data-stu-id="0af06-137">You can test it in SQL using the following statement.</span></span>

    ```
    select * from DIMENSIONCOMBINATIONENTITY
    ```


## <a name="additional-resources"></a><span data-ttu-id="0af06-138">追加リソース</span><span class="sxs-lookup"><span data-stu-id="0af06-138">Additional resources</span></span>

[<span data-ttu-id="0af06-139">既定の分析コード コントロールの分析コード エントリ コントロールへの移行</span><span class="sxs-lookup"><span data-stu-id="0af06-139">Migrate default dimensions controls to Dimension Entry controls</span></span>](dimension-entry-control-migration.md)

[<span data-ttu-id="0af06-140">分析コード エントリ コントロールの取得</span><span class="sxs-lookup"><span data-stu-id="0af06-140">Uptake of Dimension Entry controls</span></span>](dimension-entry-control-uptake.md)

[<span data-ttu-id="0af06-141">拡張機能のホーム ページ</span><span class="sxs-lookup"><span data-stu-id="0af06-141">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)




