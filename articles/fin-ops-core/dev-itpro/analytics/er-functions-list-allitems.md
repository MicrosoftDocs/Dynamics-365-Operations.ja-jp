---
title: ALLITEMS ER 関数
description: このトピックでは、ALLITEMS 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 79c43b6ecdb307433b0c2091840c21a5ada3a689
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917445"
---
# <span data-ttu-id="ee917-103"><a name="ALLITEMS">ALLITEMS ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="ee917-103"><a name="ALLITEMS">ALLITEMS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee917-104">`ALLITEMS` 関数は、メモリ内の選択範囲として実行され、指定したパスと一致するすべての品目を表すレコードの一覧として、新しいフラット化した*レコード リスト*値を返します。</span><span class="sxs-lookup"><span data-stu-id="ee917-104">The `ALLITEMS` function runs as an in-memory selection and returns a new flattened *Record list* value as a list of records that represents all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee917-105">構文</span><span class="sxs-lookup"><span data-stu-id="ee917-105">Syntax</span></span>

```
ALLITEMS (path)
```

## <a name="arguments"></a><span data-ttu-id="ee917-106">引数</span><span class="sxs-lookup"><span data-stu-id="ee917-106">Arguments</span></span>

<span data-ttu-id="ee917-107">`path`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="ee917-107">`path`: *Record list*</span></span>

<span data-ttu-id="ee917-108">*レコード リスト* データ型のデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="ee917-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="ee917-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="ee917-109">Return values</span></span>

<span data-ttu-id="ee917-110">*レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="ee917-110">*Record list*</span></span>

<span data-ttu-id="ee917-111">レコードの結果リスト。</span><span class="sxs-lookup"><span data-stu-id="ee917-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ee917-112">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="ee917-112">Usage notes</span></span>

<span data-ttu-id="ee917-113">パスは、*レコード リスト* データ型のデータ ソースの要素の有効なデータ ソース パスとして定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee917-113">The path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="ee917-114">パス文字列や日付などのデータ要素は、デザイン時に電子申告 (ER) 式ビルダーでエラーを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee917-114">Data elements such as the path string and date should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="ee917-115">大量のデータが含まれる可能性のあるトランザクション データ ソースには、この関数を使用しないことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ee917-115">We don't recommend that you use this function for transactional data sources that might contain a large volume of data.</span></span> <span data-ttu-id="ee917-116">代わりに、[ALLTEMSQUERY](er-functions-list-allitemsquery.md) 関数の使用を検討してください。</span><span class="sxs-lookup"><span data-stu-id="ee917-116">Instead, consider using the [ALLTEMSQUERY](er-functions-list-allitemsquery.md) function.</span></span>

## <a name="example-1"></a><span data-ttu-id="ee917-117">例 1</span><span class="sxs-lookup"><span data-stu-id="ee917-117">Example 1</span></span>

<span data-ttu-id="ee917-118">データソース **DS** として `SPLIT("abcdef" , 2)` を入力すると、`COUNT( ALLITEMS (DS))` 式は **3** を返します。</span><span class="sxs-lookup"><span data-stu-id="ee917-118">If you enter `SPLIT("abcdef" , 2)` as data source **DS**, the expression `COUNT( ALLITEMS (DS))` returns **3**.</span></span>

## <a name="example-2"></a><span data-ttu-id="ee917-119">例 2</span><span class="sxs-lookup"><span data-stu-id="ee917-119">Example 2</span></span>

<span data-ttu-id="ee917-120">VendTable アプリケーション テーブルを参照する*レコード リスト* データ タイプのデータ ソースとして **Vend** を入力すると、`ALLITEMS (Vend.'<Relations'.ContactPerson)` 式は、**ContactPerson**テーブル構造を持ち、**ContactPerson.ContactForParty == VendTable.Party** 関係を使用してアクセスできるすべての連絡担当者を含み、参照された仕入先テーブルから仕入先に利用可能なレコードのフラット化されたリストを返します。</span><span class="sxs-lookup"><span data-stu-id="ee917-120">If you enter **Vend** as the data source of the *Record list* data type that refers to the VendTable application table, the expression `ALLITEMS (Vend.'<Relations'.ContactPerson)` returns a flattened list of records that has the **ContactPerson** table structure and contains all contact persons that can be accessed by using the **ContactPerson.ContactForParty == VendTable.Party** relation, and that is available for all vendors from the referenced vendor table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ee917-121">追加リソース</span><span class="sxs-lookup"><span data-stu-id="ee917-121">Additional resources</span></span>

[<span data-ttu-id="ee917-122">リスト機能</span><span class="sxs-lookup"><span data-stu-id="ee917-122">List functions</span></span>](er-functions-category-list.md)
