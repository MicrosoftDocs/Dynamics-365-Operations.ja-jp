---
title: 受け入れテスト ライブラリ コード生成ウィザード
description: ここでは、受け入れテストライブラリのコード生成ウィザードに関する情報を提供します。
author: MichaelFruergaardPontoppidan
manager: AnnBe
ms.date: 03/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: RobinARH
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: MichaelFruergaardPontoppidan
ms.search.validFrom: 2018-XX-XX
ms.dyn365.ops.version: App Update 10.0.2
ms.openlocfilehash: 665d0b17a7e89f54cdb4c2d2ed38b384e9da9861
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537142"
---
# <a name="acceptance-test-library-code-generation-wizard"></a><span data-ttu-id="6fb5a-103">受け入れテスト ライブラリ コード生成ウィザード</span><span class="sxs-lookup"><span data-stu-id="6fb5a-103">Acceptance test library Code generation wizard</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="6fb5a-104">引受テスト ライブラリ (ATL) コード ジェネレーターはすばやくを生成し、新しいATLエンティティ、クエリ、およびテーブルとデータ エンティティに基づく仕様を更新します。</span><span class="sxs-lookup"><span data-stu-id="6fb5a-104">The Acceptance test library (ATL) code generator quickly generates and updates new ATL entities, queries, and specifications, based on tables and data entities.</span></span>

## <a name="create-the-atlentity-class-by-using-the-wizard"></a><span data-ttu-id="6fb5a-105">ウィザードを使用して、AtlEntityクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="6fb5a-105">Create the AtlEntity class by using the wizard</span></span>

<span data-ttu-id="6fb5a-106">`AtlEntity` クラスを作成するには、以下の手順に従って **コード生成** ウィザードを使用します。</span><span class="sxs-lookup"><span data-stu-id="6fb5a-106">Follow these steps to create the `AtlEntity` class by using the **Code generation** wizard.</span></span>

1. <span data-ttu-id="6fb5a-107">Microsoft Visual Studioを起動し、デザイナー ウィンドウで、テーブルを開きます。</span><span class="sxs-lookup"><span data-stu-id="6fb5a-107">In Microsoft Visual Studio, open the table in the designer window.</span></span>
2. <span data-ttu-id="6fb5a-108">テーブルの名前を右クリックし、 **アドイン** メニューで、 **ATLエンティティの生成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6fb5a-108">Right-click the name of the table, and then, on the **Add-ins** menu, select **Generate ATL Entity**.</span></span>
3. <span data-ttu-id="6fb5a-109">`AtlEntity` クラスに含めるフィールドを選択し、 **追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6fb5a-109">Select the fields that should be included in the `AtlEntity` class, and then select **Add**.</span></span>
4. <span data-ttu-id="6fb5a-110">必要に応じてエンティティとフィールド名称を変更します。</span><span class="sxs-lookup"><span data-stu-id="6fb5a-110">Rename the entity and the fields as you require.</span></span>
5. <span data-ttu-id="6fb5a-111">**生成** を選択してクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="6fb5a-111">Select **Generate** to create the class.</span></span>

### <a name="additional-optional-steps"></a><span data-ttu-id="6fb5a-112">追加オプション</span><span class="sxs-lookup"><span data-stu-id="6fb5a-112">Additional optional steps</span></span>

<span data-ttu-id="6fb5a-113">`AtlEntity` クラスを作成する際に、以下の作業を同時に実行するができます。</span><span class="sxs-lookup"><span data-stu-id="6fb5a-113">When you create the `AtlEntity` class, you can also complete these tasks:</span></span>

- <span data-ttu-id="6fb5a-114">シナリオに必要なアクションを追加します。</span><span class="sxs-lookup"><span data-stu-id="6fb5a-114">Add required actions for the scenario.</span></span>
- <span data-ttu-id="6fb5a-115">`default` メソッドを `AtlData` クラスに追加する。</span><span class="sxs-lookup"><span data-stu-id="6fb5a-115">Add a `default` method to `AtlData` classes.</span></span>
- <span data-ttu-id="6fb5a-116">`setMainRecordField` メソッドを上書きし、テーブル上の `modifiedField(_fieldId)` メソッドを呼び出す。</span><span class="sxs-lookup"><span data-stu-id="6fb5a-116">Override the `setMainRecordField` method to call the `modifiedField(_fieldId)` method on the table.</span></span>

    ```
    protected void setMainRecordField(FieldId _fieldId, anytype _value)
    {
        super(_fieldId, _value);
        common.modifiedField(_fieldId);
    }
    ```

## <a name="create-the-atlquery-class-by-using-the-wizard"></a><span data-ttu-id="6fb5a-117">ウィザードを使用して、AtlQueryクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="6fb5a-117">Create the AtlQuery class by using the wizard</span></span>

<span data-ttu-id="6fb5a-118">`AtlQuery` クラスを作成するには、以下の手順に従って **コード生成** ウィザードを使用します。</span><span class="sxs-lookup"><span data-stu-id="6fb5a-118">Follow these steps to create the `AtlQuery` class by using the **Code generation** wizard.</span></span>

1. <span data-ttu-id="6fb5a-119">Microsoft Visual Studioを起動し、デザイナー ウィンドウで、テーブルを開きます。</span><span class="sxs-lookup"><span data-stu-id="6fb5a-119">In Visual Studio, open the table in the designer window.</span></span>
2. <span data-ttu-id="6fb5a-120">テーブルの名前を右クリックし、 **アドイン** メニューで、 **ATLエンティティの生成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6fb5a-120">Right-click the name of the table, and then, on the **Add-ins** menu, select **Generate ATL Query**.</span></span>
3. <span data-ttu-id="6fb5a-121">`AtlQuery` クラスに含めるフィールドと関連付けを選択し、 **追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6fb5a-121">Select the fields and relations that should be included in the `AtlQuery` class, and then select **Add**.</span></span>
4. <span data-ttu-id="6fb5a-122">必要に応じてクエリ、フィールド名称、関連付けの名称を変更します。</span><span class="sxs-lookup"><span data-stu-id="6fb5a-122">Rename the query, the fields, and the relations as you require.</span></span>
5. <span data-ttu-id="6fb5a-123">**生成** を選択してクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="6fb5a-123">Select **Generate** to create the class.</span></span>

### <a name="additional-optional-steps"></a><span data-ttu-id="6fb5a-124">追加オプション</span><span class="sxs-lookup"><span data-stu-id="6fb5a-124">Additional optional steps</span></span>

<span data-ttu-id="6fb5a-125">`AtlQuery` クラスを作成する際に、 `query` のメソッドを `AtlData` のクラスに追加することが可能です。 これによりこのトピックの最初に作成した `AtlQuery` クラスのインスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="6fb5a-125">When you create the `AtlQuery` class, you can also add a `query` method to the `AtlData` class that returns an instance of the `AtlQuery` class that you created earlier in this topic.</span></span>

## <a name="create-the-atlspec-class-by-using-the-wizard"></a><span data-ttu-id="6fb5a-126">ウィザードを使用して、AtlSpecクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="6fb5a-126">Create the AtlSpec class by using the wizard</span></span>

<span data-ttu-id="6fb5a-127">`AtlSpec` クラスを作成するには、以下の手順に従って **コード生成** ウィザードを使用します。</span><span class="sxs-lookup"><span data-stu-id="6fb5a-127">Follow these steps to create the `AtlSpec` class by using the **Code generation** wizard.</span></span>

1. <span data-ttu-id="6fb5a-128">Microsoft Visual Studioを起動し、デザイナー ウィンドウで、テーブルを開きます。</span><span class="sxs-lookup"><span data-stu-id="6fb5a-128">In Visual Studio, open the table in the designer window.</span></span>
2. <span data-ttu-id="6fb5a-129">テーブルの名前を右クリックし、 **アドイン** メニューで、 **ATL Specificationの生成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6fb5a-129">Right-click the name of the table, and then, on the **Add-ins** menu, select **Generate ATL Specification**.</span></span>
3. <span data-ttu-id="6fb5a-130">`AtlSpec` クラスに含めるフィールドを選択し、 **追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6fb5a-130">Select the fields that should be included in the `AtlSpec` class, and then select **Add**.</span></span>
4. <span data-ttu-id="6fb5a-131">必要に応じてSpecificationとフィールド名称を変更します。</span><span class="sxs-lookup"><span data-stu-id="6fb5a-131">Rename the specification and the fields as you require.</span></span>
5. <span data-ttu-id="6fb5a-132">**生成** を選択してクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="6fb5a-132">Select **Generate** to create the class.</span></span>

### <a name="additional-optional-steps"></a><span data-ttu-id="6fb5a-133">追加オプション</span><span class="sxs-lookup"><span data-stu-id="6fb5a-133">Additional optional steps</span></span>

<span data-ttu-id="6fb5a-134">`spec` のメソッドをデータクラスに追加することにより、このトピックの最初に作成した `AtlSpec` クラスのインスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="6fb5a-134">Add a `spec` method to the data class that returns an instance of the `AtlSpec` class that you created earlier in this topic.</span></span>
