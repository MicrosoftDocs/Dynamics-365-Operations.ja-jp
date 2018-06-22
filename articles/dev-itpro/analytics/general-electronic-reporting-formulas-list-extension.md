---
title: "電子申告機能の一覧の拡張"
description: "テキスト、日時、算術、論理、情報、データ型変換、およびその他 (ビジネス ドメインの特定の関数) といったさまざまなタイプの関数がデータ変換のための電子報告式でサポートされています。 組み込み関数に加えて、電子申告により使用可能な関数の一覧を拡張できます。 この記事では、新しい機能を導入するために完了しなければならない重要なタスクの概要について説明します。"
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERExpressionDesignerFormula
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58911
ms.assetid: 62c740dc-6a88-4ded-9c41-6857b82b335e
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e36602baea698ab6915c28d2ab4b5f47dce20daa
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="extend-the-list-of-electronic-reporting-functions"></a><span data-ttu-id="07c2e-105">電子申告機能の一覧の拡張</span><span class="sxs-lookup"><span data-stu-id="07c2e-105">Extend the list of Electronic reporting functions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07c2e-106">テキスト、日時、算術、論理、情報、データ型変換、およびその他 (ビジネス ドメインの特定の関数) といったさまざまなタイプの関数がデータ変換のための電子報告式でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="07c2e-106">Various types of functions are supported in Electronic reporting expressions for data transformation -  text, date and time, mathematical logical, information, data type conversion, and other (business domain–specific functions).</span></span> <span data-ttu-id="07c2e-107">組み込み関数に加えて、電子申告により使用可能な関数の一覧を拡張できます。</span><span class="sxs-lookup"><span data-stu-id="07c2e-107">In addition to built-in functions, Electronic reporting lets you extend the list of available functions.</span></span> <span data-ttu-id="07c2e-108">この記事では、新しい機能を導入するために完了しなければならない重要なタスクの概要について説明します。</span><span class="sxs-lookup"><span data-stu-id="07c2e-108">This article includes an overview of key tasks that you must complete to introduce a new function.</span></span>

<span data-ttu-id="07c2e-109">Microsoft Dynamics 365 for Finance and Operations コードのすべての電子申告機能は、**ERExpression** クラスを拡張するクラスとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="07c2e-109">All Electronic reporting functions in Microsoft Dynamics 365 for Finance and Operations code are represented as classes that extend the **ERExpression** class.</span></span> <span data-ttu-id="07c2e-110">2 種類の関数が認識されます。</span><span class="sxs-lookup"><span data-stu-id="07c2e-110">Two types of functions are recognized:</span></span>

-   <span data-ttu-id="07c2e-111">**引数の数を固定** – これらの関数は、接頭語 **parm** (次のサンプルコードの **parmInput**、**parmStartNum**を参照してください) を持つメソッドを含むクラスで表されます。</span><span class="sxs-lookup"><span data-stu-id="07c2e-111">**Fixed number of arguments** – These functions are represented by classes that include methods that have the prefix **parm** (see **parmInput**, **parmStartNum** in the sample code the follows).</span></span> <span data-ttu-id="07c2e-112">引数の順序は、**SysOperationDisplayOrderAttribute** 属性によって設定されます。</span><span class="sxs-lookup"><span data-stu-id="07c2e-112">The order of arguments is set by the **SysOperationDisplayOrderAttribute** attribute.</span></span>
-   <span data-ttu-id="07c2e-113">**可変数の引数** – これらの機能は (**ERExpressionGenericCase** クラスを参照してください)**ERIObjectContainer** インターフェイスを実装するクラスで表されます。</span><span class="sxs-lookup"><span data-stu-id="07c2e-113">**Variable number of arguments** – These functions (see the **ERExpressionGenericCase** class) are represented by classes that implement the **ERIObjectContainer** interface.</span></span> <span data-ttu-id="07c2e-114">追加の**追加**メソッドを使用して関数を受け入れる型を宣言します。</span><span class="sxs-lookup"><span data-stu-id="07c2e-114">An additional **Add** method is used to declare the types that a function accepts.</span></span>

<span data-ttu-id="07c2e-115">電子申告式の新しい機能を導入するのに推奨されている手順を次に示します。</span><span class="sxs-lookup"><span data-stu-id="07c2e-115">Here are the recommended steps for introducing a new function for Electronic reporting expressions:</span></span>

-   <span data-ttu-id="07c2e-116">戻り値の型に基づいて関数の基本クラスを選択します (以下のサンプル コードで **ERExpressionString** を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="07c2e-116">Select a base class for your function, based on the return value type (see **ERExpressionString** in the sample code that follows).</span></span>
    -   <span data-ttu-id="07c2e-117">選択したクラスを拡張する新しいクラスを作成します (サンプル コードの **ERExpressionStringMid** を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="07c2e-117">Create a new class that extends the selected class (see **ERExpressionStringMid** in the sample code the follows).</span></span>
        -   <span data-ttu-id="07c2e-118">必須属性を提供:</span><span class="sxs-lookup"><span data-stu-id="07c2e-118">Provide required attributes:</span></span>
            -   <span data-ttu-id="07c2e-119">**SysOperationLabelAttribute** – この属性は、関数の名前を定義します。</span><span class="sxs-lookup"><span data-stu-id="07c2e-119">**SysOperationLabelAttribute** – This attribute defines the function’s name.</span></span>
            -   <span data-ttu-id="07c2e-120">**SysOperationHelpTextAttribute** – この属性は、関数のヘルプ テキストを定義します。</span><span class="sxs-lookup"><span data-stu-id="07c2e-120">**SysOperationHelpTextAttribute** – This attribute defines the function’s Help text.</span></span>
            -   <span data-ttu-id="07c2e-121">**ERComponentGroupAttribute** - この属性は、この機能が属するグループを定義します。</span><span class="sxs-lookup"><span data-stu-id="07c2e-121">**ERComponentGroupAttribute** – This attribute defines the group that the function belongs to.</span></span> <span data-ttu-id="07c2e-122">(詳細については、「[電子申告のフォーミュラ デザイナー](general-electronic-reporting-formula-designer.md)」を参照してください。)</span><span class="sxs-lookup"><span data-stu-id="07c2e-122">(For more information, see [Formula designer in Electronic reporting](general-electronic-reporting-formula-designer.md).)</span></span>
        -   <span data-ttu-id="07c2e-123">引数を提供します。</span><span class="sxs-lookup"><span data-stu-id="07c2e-123">Provide arguments:</span></span>
            -   <span data-ttu-id="07c2e-124">引数関数の固定番号については、接頭語 **parm** を持つメソッドを提供し、**SysOperationDisplayOrderAttribute** 属性を使用して引数の順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="07c2e-124">For a fixed number of arguments function, provide methods that have the prefix **parm**, and use the **SysOperationDisplayOrderAttribute** attribute to set the order of the arguments.</span></span>
            -   <span data-ttu-id="07c2e-125">引数関数の変数番号で、**ERIObjectContainer** インターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="07c2e-125">For a variable number of argument function, implement the **ERIObjectContainer** interface.</span></span>
        -   <span data-ttu-id="07c2e-126">評価方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="07c2e-126">Provide an evaluation method.</span></span>

<span data-ttu-id="07c2e-127">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="07c2e-127">Here is an example.</span></span>

    /// <summary>
    /// Returns the characters from the middle of a text string, given a starting position and length.
    /// </summary>
    [
        SysOperationLabelAttribute ('MID'),
        SysOperationHelpTextAttribute ("@ElectronicReporting:ExpressionStringMidHelpText"),
        ERComponentGroupAttribute ("@ElectronicReporting:String")
    ]
    class ERExpressionStringMid extends ERExpressionString
    {
        ERExpressionString input;
        ERExpressionInt startNum;
        ERExpressionInt numChars;
        public str evaluateString(ERIDataContext _dataContext)
        {
            return subStr(
            this.parmInput().evaluateString(_dataContext),
            this.parmStartNum().evaluateInt(_dataContext),
            this.parmNumChars().evaluateInt(_dataContext));
        }
        [DataMemberAttribute, SysOperationLabelAttribute ("@ElectronicReporting:Input"), SysOperationDisplayOrderAttribute ("1")]
        public ERExpressionString parmInput(ERExpressionString _input = input)
        {
            input = _input;
            return input;
        }
        [DataMemberAttribute, SysOperationLabelAttribute ("@ElectronicReporting:NumChars"), SysOperationDisplayOrderAttribute ("3")]
        public ERExpressionInt parmNumChars(ERExpressionInt _numChars = numChars)
        {
            numChars = _numChars;
            return numChars;
        }
        [DataMemberAttribute, SysOperationLabelAttribute ("@ElectronicReporting:StartNum"), SysOperationDisplayOrderAttribute ("2")]
        public ERExpressionInt parmStartNum(ERExpressionInt _startNum = startNum)
        {
            startNum = _startNum;
            return startNum;
        }
        public str toString()
        {
            return ERExpressionStringPresenter::namedFunctionToStr(this);
        }
    }

## <a name="suggested-guidance"></a><span data-ttu-id="07c2e-128">推奨されるガイダンス</span><span class="sxs-lookup"><span data-stu-id="07c2e-128">Suggested guidance</span></span>
<span data-ttu-id="07c2e-129">次のガイダンスは、カスタム電子申告機能の設計を支援することを目的としています。</span><span class="sxs-lookup"><span data-stu-id="07c2e-129">The following guidance is intended to help you design your custom Electronic reporting functions:</span></span>

-   <span data-ttu-id="07c2e-130">電子レポート式が Excel と同様に維持されるようにため、可能な限り Microsoft Excel の関数名を再利用してください。</span><span class="sxs-lookup"><span data-stu-id="07c2e-130">Reuse the names of Microsoft Excel functions whenever you can, so that Electronic reporting formulas remain Excel-like.</span></span> <span data-ttu-id="07c2e-131">この方法で、電子申告のフォーミュラをエンド ユーザーにわかりやすく保持します。</span><span class="sxs-lookup"><span data-stu-id="07c2e-131">In this way, you will keep Electronic reporting formulas intelligible for end users.</span></span>
-   <span data-ttu-id="07c2e-132">電子申告では、プリミティブ データ型のリスト タイプがサポートされません。</span><span class="sxs-lookup"><span data-stu-id="07c2e-132">Electronic reporting doesn't support list types for primitive data types.</span></span> <span data-ttu-id="07c2e-133">したがって、単一の **Value** 項目を持つデータ コンテナー リストを使用することに決めました。</span><span class="sxs-lookup"><span data-stu-id="07c2e-133">Therefore, we have decided to use a data container list that has a single **Value** item in it.</span></span>
-   <span data-ttu-id="07c2e-134">新しい関数の一覧の拡張機能を新しい Finance and Operations の修正プログラムとしてリリースします。</span><span class="sxs-lookup"><span data-stu-id="07c2e-134">Release a new function's list extension as a new Finance and Operations hotfix.</span></span> <span data-ttu-id="07c2e-135">電子申告デザイナーは、新しいユーザー定義関数を使用する電子申告 コンフィギュレーションの修正プログラム番号を参照します。</span><span class="sxs-lookup"><span data-stu-id="07c2e-135">Electronic reporting designers will refer to the hotfix number in Electronic reporting configurations that use that new custom function.</span></span> <span data-ttu-id="07c2e-136">このタイプの構成が Finance and Operations の新しいインスタンスにインポートされるときはいつでも、必要な修正プログラムがインストールされたかどうかが電子申告によって評価されて、電子申告構成と、構成がインポートされる Finance and Operations のバージョンとの間のコンプライアンスを維持します。</span><span class="sxs-lookup"><span data-stu-id="07c2e-136">Whenever a configuration of this type is imported into a new instance of Finance and Operations, Electronic reporting will evaluate whether the required hotfix has been installed, to maintain compliance between the Electronic reporting configuration and the Finance and Operations version that configuration is imported into.</span></span>


<a name="additional-resources"></a><span data-ttu-id="07c2e-137">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="07c2e-137">Additional resources</span></span>
--------

[<span data-ttu-id="07c2e-138">電子申告の概要</span><span class="sxs-lookup"><span data-stu-id="07c2e-138">Electronic reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="07c2e-139">電子申告のフォーミュラ デザイナー</span><span class="sxs-lookup"><span data-stu-id="07c2e-139">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)




