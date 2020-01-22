---
title: NUMSEQVALUE ER 機能
description: このトピックでは、NUMSEQVALUE 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: d68784524a5639d8d447daa2cda940680d795542
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915835"
---
# <span data-ttu-id="8d631-103"><a name="NUMSEQVALUE">NUMSEQVALUE ER 機能</a></span><span class="sxs-lookup"><span data-stu-id="8d631-103"><a name="NUMSEQVALUE">NUMSEQVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8d631-104">`NUMSEQVALUE` 関数は、指定された番号順序、範囲、およびスコープ ID に基づいて、番号順序の新しい生成値を表す*文字列*値を返します。</span><span class="sxs-lookup"><span data-stu-id="8d631-104">The `NUMSEQVALUE` function returns a *String* value that represents the new generated value of a number sequence, based on the specified number sequence, scope, and scope ID.</span></span> <span data-ttu-id="8d631-105">スコープ ID は、電子申告 (ER) 形式が実行されるコンテキストによって提供される会社コードと同じです。</span><span class="sxs-lookup"><span data-stu-id="8d631-105">The scope ID equals the company code that is supplied by the context that the Electronic reporting (ER) format is run under.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="8d631-106">構文 1</span><span class="sxs-lookup"><span data-stu-id="8d631-106">Syntax 1</span></span>

```
NUMSEQVALUE (number sequence code)
```

## <a name="syntax-2"></a><span data-ttu-id="8d631-107">構文 2</span><span class="sxs-lookup"><span data-stu-id="8d631-107">Syntax 2</span></span>

```
NUMSEQVALUE (number sequence record ID)
```

## <a name="syntax-3"></a><span data-ttu-id="8d631-108">構文 3</span><span class="sxs-lookup"><span data-stu-id="8d631-108">Syntax 3</span></span>

```
NUMSEQVALUE (number sequence code, scope type, scope ID)
```

## <a name="arguments"></a><span data-ttu-id="8d631-109">引数</span><span class="sxs-lookup"><span data-stu-id="8d631-109">Arguments</span></span>

<span data-ttu-id="8d631-110">`number sequence code`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="8d631-110">`number sequence code`: *String*</span></span>

<span data-ttu-id="8d631-111">新しい値で必要な番号順序のコードを表すテキスト値。</span><span class="sxs-lookup"><span data-stu-id="8d631-111">A text value that represents the code of the number sequence that a new value is required in.</span></span>

<span data-ttu-id="8d631-112">`number sequence record ID`: *Int64*</span><span class="sxs-lookup"><span data-stu-id="8d631-112">`number sequence record ID`: *Int64*</span></span>

<span data-ttu-id="8d631-113">新しい値で必要な番号順序の定義を含む、NumberSequenceTable テーブルの記録 ID を表す *Int64* 値。</span><span class="sxs-lookup"><span data-stu-id="8d631-113">An *Int64* value that represents the record ID of a record in the NumberSequenceTable table that contains the definition of the number sequence that a new value is required in.</span></span>

<span data-ttu-id="8d631-114">`scope type`: *列挙値*</span><span class="sxs-lookup"><span data-stu-id="8d631-114">`scope type`: *Enum value*</span></span>

<span data-ttu-id="8d631-115">新しい値が必要な番号順序のスコープを定義する **ERExpressionNumberSequenceScopeType** 列挙型の列挙値。</span><span class="sxs-lookup"><span data-stu-id="8d631-115">An enumeration value of the **ERExpressionNumberSequenceScopeType** enumeration that defines the scope of the number sequence that a new value is required in.</span></span> <span data-ttu-id="8d631-116">使用可能な範囲タイプは、**共有**、**法人**、および**会社**です。</span><span class="sxs-lookup"><span data-stu-id="8d631-116">The available scope types are **Shared**, **Legal entity**, and **Company**.</span></span>

<span data-ttu-id="8d631-117">`scope ID`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="8d631-117">`scope ID`: *String*</span></span>

<span data-ttu-id="8d631-118">指定したスコープ タイプに基づいて、スコープを識別する*文字列*値。</span><span class="sxs-lookup"><span data-stu-id="8d631-118">A *String* value that identifies the scope, based on the specified scope type.</span></span>

## <a name="return-values"></a><span data-ttu-id="8d631-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="8d631-119">Return values</span></span>

<span data-ttu-id="8d631-120">*文字列*</span><span class="sxs-lookup"><span data-stu-id="8d631-120">*String*</span></span>

<span data-ttu-id="8d631-121">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="8d631-121">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8d631-122">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="8d631-122">Usage notes</span></span>

<span data-ttu-id="8d631-123">**共有**スコープ タイプでは、スコープ ID として空の文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="8d631-123">For the **Shared** scope type, specify an empty string as the scope ID.</span></span>

<span data-ttu-id="8d631-124">**会社**および**法人**スコープ タイプでは、会社コードとスコープ ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="8d631-124">For the **Company** and **Legal entity** scope types, specify the company code as the scope ID.</span></span> <span data-ttu-id="8d631-125">これらのスコープ タイプのスコープ ID として空の文字列を指定した場合、現在の会社コードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="8d631-125">If you specify an empty string as the scope ID for these scope types, the current company code is used.</span></span>

<span data-ttu-id="8d631-126">構文 1 を使用すると、番号順序が**会社**スコープ タイプに対して要求され、会社コードが ER 形式を実行するコンテキストによって提供されます。</span><span class="sxs-lookup"><span data-stu-id="8d631-126">When syntax 1 is used, the number sequence is requested for the **Company** scope type, and the company code is supplied by the context that the ER format is run under.</span></span>

## <a name="example-1"></a><span data-ttu-id="8d631-127">例 1</span><span class="sxs-lookup"><span data-stu-id="8d631-127">Example 1</span></span>

<span data-ttu-id="8d631-128">ERフォーマットでは、*ユーザー入力パラメータ*タイプの **AskNumSeq** データ ソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="8d631-128">In your ER format, you define the **AskNumSeq** data source of the *User input parameter* type.</span></span> <span data-ttu-id="8d631-129">このデータ ソースは、**説明**の拡張データ型 (EDT) を参照しています。</span><span class="sxs-lookup"><span data-stu-id="8d631-129">This data source refers to the **Description** extended data type (EDT).</span></span> <span data-ttu-id="8d631-130">次に、*計算フィールド*タイプの **NumSeq** データ ソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="8d631-130">Next, you define the **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="8d631-131">このデータ ソースは、式 `NUMSEQVALUE (AskNumSeq)` が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8d631-131">This data source contains the expression `NUMSEQVALUE (AskNumSeq)`.</span></span> <span data-ttu-id="8d631-132">**NumSeq** データ ソースが呼び出されると、ダイアログ ボックスにコードを入力することにより、実行時に指定された番号順序の新しい生成値が返されます。</span><span class="sxs-lookup"><span data-stu-id="8d631-132">When the **NumSeq** data source is called, it returns the new generated value of the number sequence that was specified at runtime by entering its code in the dialog box.</span></span> <span data-ttu-id="8d631-133">**会社**スコープ タイプに対して番号順序が要求されます。</span><span class="sxs-lookup"><span data-stu-id="8d631-133">The number sequence is requested for the **Company** scope type.</span></span> <span data-ttu-id="8d631-134">会社コードは、ER 形式を実行するコンテキストによって提供されます。</span><span class="sxs-lookup"><span data-stu-id="8d631-134">The company code is supplied by the context that the ER format is run under.</span></span>

## <a name="example-2"></a><span data-ttu-id="8d631-135">例 2</span><span class="sxs-lookup"><span data-stu-id="8d631-135">Example 2</span></span>

<span data-ttu-id="8d631-136">モデル マッピングでは、次のデータ ソースが定義されます。</span><span class="sxs-lookup"><span data-stu-id="8d631-136">The following data sources are defined in your model mapping:</span></span>

- <span data-ttu-id="8d631-137">*テーブル*タイプの **LedgerParms** データ ソース。</span><span class="sxs-lookup"><span data-stu-id="8d631-137">The **LedgerParms** data source of the *Table* type.</span></span> <span data-ttu-id="8d631-138">このデータ ソースは、LedgerParameters テーブルを指します。</span><span class="sxs-lookup"><span data-stu-id="8d631-138">This data source refers to the LedgerParameters table.</span></span>
- <span data-ttu-id="8d631-139">*計算フィールド*タイプの **NumSeq** データ ソース。</span><span class="sxs-lookup"><span data-stu-id="8d631-139">The **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="8d631-140">このデータ ソースは、式 `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)` が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8d631-140">This data source contains the expression `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.</span></span>

<span data-ttu-id="8d631-141">**NumSeq** データ ソースが呼び出されると、ER 形式が実行されているコンテキストを提供する会社用に一般会計パラメーターでコンフィギュレーションされた、番号順序の新しく生成された値を返します。</span><span class="sxs-lookup"><span data-stu-id="8d631-141">When the **NumSeq** data source is called, it returns the new generated value of the number sequence that has been configured in the General ledger parameters for the company that supplies the context that the ER format is run under.</span></span> <span data-ttu-id="8d631-142">この番号順序は、仕訳帳を一意に識別し、トランザクションをリンクするバッチ番号として機能します。</span><span class="sxs-lookup"><span data-stu-id="8d631-142">This number sequence uniquely identifies journals and acts as a batch number that links the transactions together.</span></span>

## <a name="example-3"></a><span data-ttu-id="8d631-143">例 3</span><span class="sxs-lookup"><span data-stu-id="8d631-143">Example 3</span></span>

<span data-ttu-id="8d631-144">モデル マッピングでは、次のデータ ソースが定義されます。</span><span class="sxs-lookup"><span data-stu-id="8d631-144">The following data sources are defined in your model mapping:</span></span>

- <span data-ttu-id="8d631-145">Microsoft Dynamics 365 Finance *列挙型* タイプの **enumScope** データ ソース。</span><span class="sxs-lookup"><span data-stu-id="8d631-145">The **enumScope** data source of the Microsoft Dynamics 365 Finance *enumeration* type.</span></span> <span data-ttu-id="8d631-146">このデータ ソースは、**ERExpressionNumberSequenceScopeType** 列挙型を参照しています。</span><span class="sxs-lookup"><span data-stu-id="8d631-146">This data source refers to the **ERExpressionNumberSequenceScopeType** enumeration.</span></span>
- <span data-ttu-id="8d631-147">*計算フィールド*タイプの **NumSeq** データ ソース。</span><span class="sxs-lookup"><span data-stu-id="8d631-147">The **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="8d631-148">このデータ ソースは、式 `NUMSEQVALUE ("Gene_1", enumScope.Company, "")` が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8d631-148">This data source contains the expression `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.</span></span>

<span data-ttu-id="8d631-149">**NumSeq** データ ソースが呼び出されると、ER 形式が実行されているコンテキストを提供する会社用にコンフィギュレーションされた **Gene\_1** 番号順序の新しく生成された値を返します。</span><span class="sxs-lookup"><span data-stu-id="8d631-149">When the **NumSeq** data source is called, it returns the new generated value of the **Gene\_1** number sequence that has been configured for the company that supplies the context that the ER format is run under.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8d631-150">追加リソース</span><span class="sxs-lookup"><span data-stu-id="8d631-150">Additional resources</span></span>

[<span data-ttu-id="8d631-151">その他 (ビジネス ドメインの特定の) 関数</span><span class="sxs-lookup"><span data-stu-id="8d631-151">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
