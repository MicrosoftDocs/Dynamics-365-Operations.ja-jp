---
title: FORMAT ER 関数
description: このトピックでは、FORMAT 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df158e80bd1c11832376678a631a9e0e162534ad
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915720"
---
# <span data-ttu-id="fb8cd-103"><a name="FORMAT">FORMAT ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="fb8cd-103"><a name="FORMAT">FORMAT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fb8cd-104">`FORMAT` 関数は、*N* 番目の引数で **%N** の出現を置き換えることで書式設定した後に、*文字列*値として指定された文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="fb8cd-104">The `FORMAT` function returns the specified string as a *String* value after it has been formatted by substituting any occurrences of **%N** with the *N*th argument.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb8cd-105">構文</span><span class="sxs-lookup"><span data-stu-id="fb8cd-105">Syntax</span></span>

```
FORMAT (string, argument 1[, argument 2, …, argument N])
```

## <a name="arguments"></a><span data-ttu-id="fb8cd-106">引数</span><span class="sxs-lookup"><span data-stu-id="fb8cd-106">Arguments</span></span>

<span data-ttu-id="fb8cd-107">`string`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="fb8cd-107">`string`: *String*</span></span>

<span data-ttu-id="fb8cd-108">書式設定が必要な*文字列*タイプのデータ ソースを参照。</span><span class="sxs-lookup"><span data-stu-id="fb8cd-108">A reference to a data source of the *String* type that must be formatted.</span></span> <span data-ttu-id="fb8cd-109">この引数は必須です。</span><span class="sxs-lookup"><span data-stu-id="fb8cd-109">This argument is required.</span></span>

<span data-ttu-id="fb8cd-110">`argument 1`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="fb8cd-110">`argument 1`: *String*</span></span>

<span data-ttu-id="fb8cd-111">**%1** の出現に置き換えるために使用される最初の引数。</span><span class="sxs-lookup"><span data-stu-id="fb8cd-111">The first argument, which is used to replace occurrences of **%1**.</span></span> <span data-ttu-id="fb8cd-112">この引数は必須です。</span><span class="sxs-lookup"><span data-stu-id="fb8cd-112">This argument is required.</span></span>

<span data-ttu-id="fb8cd-113">`argument N`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="fb8cd-113">`argument N`: *String*</span></span>

<span data-ttu-id="fb8cd-114">**%2**、**%3** などの出現に置き換えるために使用される *N* 番目の引数。</span><span class="sxs-lookup"><span data-stu-id="fb8cd-114">The *N*th argument, which is used to replace occurrences of **%2**, **%3**, and so on.</span></span> <span data-ttu-id="fb8cd-115">これらの追加引数はオプションです。</span><span class="sxs-lookup"><span data-stu-id="fb8cd-115">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="fb8cd-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="fb8cd-116">Return values</span></span>

<span data-ttu-id="fb8cd-117">*文字列*</span><span class="sxs-lookup"><span data-stu-id="fb8cd-117">*String*</span></span>

<span data-ttu-id="fb8cd-118">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="fb8cd-118">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="fb8cd-119">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="fb8cd-119">Usage notes</span></span>

<span data-ttu-id="fb8cd-120">パラメーターに引数が指定されない場合は、文字列内では **"%N"** として返されます。</span><span class="sxs-lookup"><span data-stu-id="fb8cd-120">If an argument isn't provided for a parameter, the parameter is returned as **"%N"** in the string.</span></span> <span data-ttu-id="fb8cd-121">*実数*型の値では、既定の文字列変換が小数点第 2 位に制限されます。</span><span class="sxs-lookup"><span data-stu-id="fb8cd-121">For values of the *Real* type, the default string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="fb8cd-122">例</span><span class="sxs-lookup"><span data-stu-id="fb8cd-122">Example</span></span>

<span data-ttu-id="fb8cd-123">次の図では、**PaymentModel** データ ソースが**顧客**コンポーネントを使用して顧客レコードの一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="fb8cd-123">In the following illustration, the **PaymentModel** data source returns a list of customer records by using the **Customer** component.</span></span> <span data-ttu-id="fb8cd-124">**ProcessingDate** フィールドを使用して、処理日の値を返します。</span><span class="sxs-lookup"><span data-stu-id="fb8cd-124">It returns the processing date value by using the **ProcessingDate** field.</span></span>

<a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>

<span data-ttu-id="fb8cd-125">選択した顧客の電子ファイルを生成するよう設計されている電子申告 (ER) 形式では、**PaymentModel** がデータ ソースとして選択され、プロセス フローを制御します。</span><span class="sxs-lookup"><span data-stu-id="fb8cd-125">In the Electronic reporting (ER) format that is designed to generate an electronic file for selected customers, **PaymentModel** is selected as a data source, and it controls the process flow.</span></span> <span data-ttu-id="fb8cd-126">選択した顧客がレポートを処理される日付に停止されている場合、例外であることをユーザーに通知し、スローされます。</span><span class="sxs-lookup"><span data-stu-id="fb8cd-126">If a selected customer is stopped for the date when the report is processed, an exception is thrown to notify the user.</span></span> <span data-ttu-id="fb8cd-127">このタイプの処理制御のために設計された式は、次のリソースを使用できます。</span><span class="sxs-lookup"><span data-stu-id="fb8cd-127">The formula that is designed for this type of processing control can use the following resources:</span></span>

- <span data-ttu-id="fb8cd-128">次のテキストを含むラベル SYS70894:</span><span class="sxs-lookup"><span data-stu-id="fb8cd-128">Label SYS70894, which has the following text:</span></span>

    - <span data-ttu-id="fb8cd-129">**EN-US 言語の場合:** "Nothing to print"</span><span class="sxs-lookup"><span data-stu-id="fb8cd-129">**For the EN-US language:** "Nothing to print"</span></span>
    - <span data-ttu-id="fb8cd-130">**DE 言語の場合:** "Nichts zu drucken"</span><span class="sxs-lookup"><span data-stu-id="fb8cd-130">**For the DE language:** "Nichts zu drucken"</span></span>

- <span data-ttu-id="fb8cd-131">次のテキストを含むラベル SYS18389:</span><span class="sxs-lookup"><span data-stu-id="fb8cd-131">Label SYS18389, which has the following text:</span></span>

    - <span data-ttu-id="fb8cd-132">**EN-US 言語の場合:** "顧客 %1 は停止 %2。"</span><span class="sxs-lookup"><span data-stu-id="fb8cd-132">**For the EN-US language:** "Customer %1 is stopped for %2."</span></span>
    - <span data-ttu-id="fb8cd-133">**DE 言語の場合:** "Debitor '%1' wird für %2 gesperrt."</span><span class="sxs-lookup"><span data-stu-id="fb8cd-133">**For the DE language:** "Debitor '%1' wird für %2 gesperrt."</span></span>

<span data-ttu-id="fb8cd-134">設計できる式を次に示します。</span><span class="sxs-lookup"><span data-stu-id="fb8cd-134">Here is the expression that can be designed.</span></span>

```
FORMAT (CONCATENATE (@"SYS70894", ". ", @"SYS18389"), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, "d"))
```

<span data-ttu-id="fb8cd-135">レポートが 2015 年 12 月 17 日に **EN-US** カルチャおよび **EN-US** 言語で **Litware Retail** の顧客に対して処理される場合、この式は例外メッセージとしてユーザーに示すことができる次のテキストを返します:</span><span class="sxs-lookup"><span data-stu-id="fb8cd-135">If a report is processed for the **Litware Retail** customer on December 17, 2015, in the **EN-US** culture and the **EN-US** language, this formula returns the following text, which can be presented to the user as an exception message:</span></span>

<span data-ttu-id="fb8cd-136">*印刷するものはありません。顧客の Litware Retail は 12/17/2015 に停止されます。*</span><span class="sxs-lookup"><span data-stu-id="fb8cd-136">*Nothing to print. Customer Litware Retail is stopped for 12/17/2015.*</span></span>

<span data-ttu-id="fb8cd-137">同じレポートが 2015 年 12 月 17 日に **DE** カルチャおよび **DE** 言語で **Litware Retail** の顧客に対して処理される場合、この式は別の日付形式を使用する次のテキストを返します。</span><span class="sxs-lookup"><span data-stu-id="fb8cd-137">If the same report is processed for the **Litware Retail** customer on December 17, 2015, in the **DE** culture and the **DE** language, the formula returns the following text, which uses a different date format:</span></span>

<span data-ttu-id="fb8cd-138">*Nichts zu drucken。 Debitor 'Litware Retail' wird für 17.12.2015 gesperrt。*</span><span class="sxs-lookup"><span data-stu-id="fb8cd-138">*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*</span></span>

>[!NOTE]
> <span data-ttu-id="fb8cd-139">次の構文は ER の式でラベルに適用されます。</span><span class="sxs-lookup"><span data-stu-id="fb8cd-139">The following syntax is applied in ER formulas for labels:</span></span>
>
> - <span data-ttu-id="fb8cd-140">**Microsoft Dynamics 365 Finance アプリにあるリソースからのラベルの場合:** **X** がアプリケーション オブジェクト ツリー (AOT) のラベル ID にある **@X**</span><span class="sxs-lookup"><span data-stu-id="fb8cd-140">**For labels from resources in the Microsoft Dynamics 365 Finance app:** **@X**, where **X** is the label ID in the Application Object Tree (AOT)</span></span>
> - <span data-ttu-id="fb8cd-141">**ER コンフィギュレーションに存在するラベルの場合:** **X** が ER コンフィギュレーションのラベル ID にある **@"GER_LABEL:X"**</span><span class="sxs-lookup"><span data-stu-id="fb8cd-141">**For labels that reside in ER configurations:** **@"GER_LABEL:X"**, where **X** is the label ID in the ER configuration</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fb8cd-142">追加リソース</span><span class="sxs-lookup"><span data-stu-id="fb8cd-142">Additional resources</span></span>

[<span data-ttu-id="fb8cd-143">テキスト関数</span><span class="sxs-lookup"><span data-stu-id="fb8cd-143">Text functions</span></span>](er-functions-category-text.md)