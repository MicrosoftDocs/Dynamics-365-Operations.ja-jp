---
title: LISTOFFIELDS ER 関数
description: このトピックでは、LISTOFFIELDS 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 494dc347fadf44121c7eae0acf8c30768c58f035
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567667"
---
# <a name="listoffields-er-function"></a><span data-ttu-id="18161-103">LISTOFFIELDS ER 関数</span><span class="sxs-lookup"><span data-stu-id="18161-103">LISTOFFIELDS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="18161-104">`LISTOFFIELDS` 関数は、*列挙* または *コンテナー (レコード)* タイプの指定された引数の構造に基づいて作成された *レコード リスト* の値を返します。</span><span class="sxs-lookup"><span data-stu-id="18161-104">The `LISTOFFIELDS` function returns a *Record list* value that is created based on the structure of the specified argument of the *Enumeration* or *Container (record)* type.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="18161-105">構文 1</span><span class="sxs-lookup"><span data-stu-id="18161-105">Syntax 1</span></span>

```vb
LISTOFFIELDS (path)
```

## <a name="syntax-2"></a><span data-ttu-id="18161-106">構文 2</span><span class="sxs-lookup"><span data-stu-id="18161-106">Syntax 2</span></span>

```vb
LISTOFFIELDS (path, language)
```

## <a name="arguments"></a><span data-ttu-id="18161-107">引数</span><span class="sxs-lookup"><span data-stu-id="18161-107">Arguments</span></span>

<span data-ttu-id="18161-108">`path`: データ ソース参照</span><span class="sxs-lookup"><span data-stu-id="18161-108">`path`: Data source reference</span></span>

<span data-ttu-id="18161-109">次のいずれかのデータ型のデータ ソースの有効な参照パス。</span><span class="sxs-lookup"><span data-stu-id="18161-109">The valid reference path of a data source of one of the following data types:</span></span>

- <span data-ttu-id="18161-110">モデルの列挙</span><span class="sxs-lookup"><span data-stu-id="18161-110">Model enumeration</span></span>
- <span data-ttu-id="18161-111">形式列挙</span><span class="sxs-lookup"><span data-stu-id="18161-111">Format enumeration</span></span>
- <span data-ttu-id="18161-112">アプリケーションの列挙</span><span class="sxs-lookup"><span data-stu-id="18161-112">Application enumeration</span></span>
- <span data-ttu-id="18161-113">コンテナー (レコード)</span><span class="sxs-lookup"><span data-stu-id="18161-113">Container (record)</span></span>

<span data-ttu-id="18161-114">`language`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="18161-114">`language`: *String*</span></span>

<span data-ttu-id="18161-115">言語コードを表すテキスト。</span><span class="sxs-lookup"><span data-stu-id="18161-115">Text that represents a language code.</span></span>

## <a name="return-values"></a><span data-ttu-id="18161-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="18161-116">Return values</span></span>

<span data-ttu-id="18161-117">*レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="18161-117">*Record list*</span></span>

<span data-ttu-id="18161-118">レコードの結果リスト。</span><span class="sxs-lookup"><span data-stu-id="18161-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="18161-119">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="18161-119">Usage notes</span></span>

<span data-ttu-id="18161-120">作成するリストは、次のフィールドを持つレコードで構成されます。</span><span class="sxs-lookup"><span data-stu-id="18161-120">The list that is created consists of records that have the following fields:</span></span>

- <span data-ttu-id="18161-121">**名前** (*文字列* データ型)</span><span class="sxs-lookup"><span data-stu-id="18161-121">**Name** (*String* data type)</span></span>
- <span data-ttu-id="18161-122">**ラベル** (*文字列* データ型)</span><span class="sxs-lookup"><span data-stu-id="18161-122">**Label** (*String* data type)</span></span>
- <span data-ttu-id="18161-123">**説明** (*文字列* データ型)</span><span class="sxs-lookup"><span data-stu-id="18161-123">**Description** (*String* data type)</span></span>
- <span data-ttu-id="18161-124">**IsTranslated** (*ブール値* データ型)</span><span class="sxs-lookup"><span data-stu-id="18161-124">**IsTranslated** (*Boolean* data type)</span></span>

<span data-ttu-id="18161-125">`path` 引数が *コンテナー (レコード)* タイプのデータ ソースを参照している場合、参照コンテナー レコードのすべてのフィールドに対して、作成されたリストに新しいレコードが追加されます。</span><span class="sxs-lookup"><span data-stu-id="18161-125">If the `path` argument refers to a data source of the *Container (Record)* type, for every field of the referenced container record, a new record is added to the list that is created.</span></span> <span data-ttu-id="18161-126">作成されるすべてのレコードについて、**名前** フィールドは、現在のレコードが作成された参照コンテナー レコードのフィールドの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="18161-126">For every record that is created, the **Name** field returns the name of the field of the referenced container record that the current record was created for.</span></span>

<span data-ttu-id="18161-127">`path` 引数が *列挙* 型のいずれかのデータ ソースを参照している場合、参照列挙の列挙値ごとに、作成されるリストに新しいレコードが追加されます。</span><span class="sxs-lookup"><span data-stu-id="18161-127">If the `path` argument refers to a data source of one of the *Enumeration* types, for every enumeration value of the referenced enumeration, a new record is added to the list that is created.</span></span> <span data-ttu-id="18161-128">作成されるすべてのレコードについて、**名前** フィールドは現在のレコードが作成された、参照列挙の値を返し、**説明** フィールドはその列挙の説明を返し、**ラベル** フィールドは、その列挙のラベルを返します。</span><span class="sxs-lookup"><span data-stu-id="18161-128">For every record that is created, the **Name** field returns the value of the referenced enumeration that the current record was created for, the **Description** field returns the description of that enumeration, and the **Label** field returns the label of that enumeration.</span></span>

<span data-ttu-id="18161-129">実行時に構文 1 を使用する場合、**ラベル** および **説明** フィールドは、実行中の電子申告 (ER) 形式の言語設定に基づく値を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="18161-129">At runtime, when syntax 1 is used, the **Label** and **Description** fields must return values that are based on the language settings of the Electronic reporting (ER) format that is running:</span></span>

- <span data-ttu-id="18161-130">要求された言語のラベルと説明が使用可能な場合、**ラベル** および **説明** フィールドはその言語に基づく値を返し、**IsTranslated** フィールドは **True** を返します。</span><span class="sxs-lookup"><span data-stu-id="18161-130">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="18161-131">要求された言語のラベルと説明が使用できない場合、**ラベル** および **説明** フィールドは既定の **EN-US** 言語に基づく値を返し、**IsTranslated** フィールドは **False** を返します。</span><span class="sxs-lookup"><span data-stu-id="18161-131">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the default **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

<span data-ttu-id="18161-132">実行時に構文 2 を使用する場合、**ラベル** および **説明** フィールドは、呼び出された関数の 2 番目の引数として定義されている言語に基づく値を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="18161-132">At runtime, when syntax 2 is used, the **Label** and **Description** fields must return values that are based on the language that is defined as the second argument of the called function:</span></span>

- <span data-ttu-id="18161-133">要求された言語のラベルと説明が使用可能な場合、**ラベル** および **説明** フィールドはその言語に基づく値を返し、**IsTranslated** フィールドは **True** を返します。</span><span class="sxs-lookup"><span data-stu-id="18161-133">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="18161-134">要求された言語のラベルと説明が使用できない場合、**ラベル** および **説明** フィールドは **EN-US** 言語に基づく値を返し、**IsTranslated** フィールドは **False** を返します。</span><span class="sxs-lookup"><span data-stu-id="18161-134">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

## <a name="example-1"></a><span data-ttu-id="18161-135">例 1</span><span class="sxs-lookup"><span data-stu-id="18161-135">Example 1</span></span>

<span data-ttu-id="18161-136">次の図では、列挙は ER データ モデルで導入されます。</span><span class="sxs-lookup"><span data-stu-id="18161-136">In the following illustration, an enumeration is introduced in an ER data model.</span></span>

<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

<span data-ttu-id="18161-137">次の図は、これらの詳細について説明しています。</span><span class="sxs-lookup"><span data-stu-id="18161-137">The following illustration shows these details:</span></span>

- <span data-ttu-id="18161-138">モデル列挙はデータ ソースとしてレポートに挿入されます。</span><span class="sxs-lookup"><span data-stu-id="18161-138">The model enumeration is inserted into a report as a data source.</span></span>
- <span data-ttu-id="18161-139">ER の式は `LISTOFFIELDS` 関数のパラメーターとしてモデル列挙を使用します。</span><span class="sxs-lookup"><span data-stu-id="18161-139">An ER expression uses the model enumeration as a parameter of the `LISTOFFIELDS` function.</span></span>
- <span data-ttu-id="18161-140">*レコード リスト* タイプのデータ ソースは、作成された ER の式を使用してレポートに挿入されます。</span><span class="sxs-lookup"><span data-stu-id="18161-140">A data source of the *Record list* type is inserted into a report by using the ER expression that is created.</span></span>

<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>

<span data-ttu-id="18161-141">次の例では、`LISTOFFIELDS` 関数を使用して作成された *レコード リスト* タイプのデータ ソースにバインドされている ER 形式要素を示します。</span><span class="sxs-lookup"><span data-stu-id="18161-141">The following example shows the ER format elements that are bound to the data source of the *Record list* type that was created by using the `LISTOFFIELDS` function.</span></span>

<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

<span data-ttu-id="18161-142">次の図は、設計された形式が実行される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="18161-142">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a>

> [!NOTE] 
> <span data-ttu-id="18161-143">親 **FILE** および **FOLDER** 形式要素の言語設定に基づいて、ラベルと説明の翻訳文は、ER 形式出力に入力されます。</span><span class="sxs-lookup"><span data-stu-id="18161-143">Based on the language settings of the parent **FILE** and **FOLDER** format elements, translated text for labels and descriptions is entered in the output of the ER format.</span></span>

## <a name="example-2"></a><span data-ttu-id="18161-144">例 2</span><span class="sxs-lookup"><span data-stu-id="18161-144">Example 2</span></span>

<span data-ttu-id="18161-145">*計算済フィールド* データ ソース型を使用して、**enumType** データ モデル列挙に対して **enumType\_de** および **enumType\_deCH** データ ソースを構成します。</span><span class="sxs-lookup"><span data-stu-id="18161-145">You use the *Calculated field* data source type to configure **enumType\_de** and **enumType\_deCH** data sources for the **enumType** data model enumeration:</span></span>

- <span data-ttu-id="18161-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span><span class="sxs-lookup"><span data-stu-id="18161-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span></span>
- <span data-ttu-id="18161-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span><span class="sxs-lookup"><span data-stu-id="18161-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span></span>

<span data-ttu-id="18161-148">この場合、その翻訳が使用可能な場合は、スイス ドイツ語の列挙値のラベルを取得する次の式を使用できます。</span><span class="sxs-lookup"><span data-stu-id="18161-148">In this case, you can use the following expression to get the label of the enumeration value in Swiss German, if that translation is available.</span></span> <span data-ttu-id="18161-149">スイス ドイツ語翻訳を使用できない場合、ラベルはドイツ語になります。</span><span class="sxs-lookup"><span data-stu-id="18161-149">If the Swiss German translation isn't available, the label is in German.</span></span>

```vb
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
```

## <a name="additional-resources"></a><span data-ttu-id="18161-150">追加リソース</span><span class="sxs-lookup"><span data-stu-id="18161-150">Additional resources</span></span>

[<span data-ttu-id="18161-151">リスト機能</span><span class="sxs-lookup"><span data-stu-id="18161-151">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]