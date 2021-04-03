---
title: ALLITEMS ER 関数
description: このトピックでは、ALLITEMS 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 1eae005a71f50a08c1ef85a7a93c3b2c407c8848
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559227"
---
# <a name="allitems-er-function"></a><span data-ttu-id="2c111-103">ALLITEMS ER 関数</span><span class="sxs-lookup"><span data-stu-id="2c111-103">ALLITEMS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c111-104">`ALLITEMS` 関数は、メモリ内の選択範囲として実行され、指定したパスと一致するすべての品目を表すレコードの一覧として、新しいフラット化した *レコード リスト* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="2c111-104">The `ALLITEMS` function runs as an in-memory selection and returns a new flattened *Record list* value as a list of records that represents all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c111-105">構文</span><span class="sxs-lookup"><span data-stu-id="2c111-105">Syntax</span></span>

```vb
ALLITEMS (path)
```

## <a name="arguments"></a><span data-ttu-id="2c111-106">引数</span><span class="sxs-lookup"><span data-stu-id="2c111-106">Arguments</span></span>

<span data-ttu-id="2c111-107">`path`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="2c111-107">`path`: *Record list*</span></span>

<span data-ttu-id="2c111-108">*レコード リスト* データ型のデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="2c111-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="2c111-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="2c111-109">Return values</span></span>

<span data-ttu-id="2c111-110">*レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="2c111-110">*Record list*</span></span>

<span data-ttu-id="2c111-111">レコードの結果リスト。</span><span class="sxs-lookup"><span data-stu-id="2c111-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2c111-112">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="2c111-112">Usage notes</span></span>

<span data-ttu-id="2c111-113">パスは、*レコード リスト* データ型のデータ ソースの要素の有効なデータ ソース パスとして定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c111-113">The path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="2c111-114">パス文字列や日付などのデータ要素は、デザイン時に電子申告 (ER) 式ビルダーでエラーを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c111-114">Data elements such as the path string and date should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="2c111-115">大量のデータが含まれる可能性のあるトランザクション データ ソースには、この関数を使用しないことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="2c111-115">We don't recommend that you use this function for transactional data sources that might contain a large volume of data.</span></span> <span data-ttu-id="2c111-116">代わりに、[ALLTEMSQUERY](er-functions-list-allitemsquery.md) 関数の使用を検討してください。</span><span class="sxs-lookup"><span data-stu-id="2c111-116">Instead, consider using the [ALLTEMSQUERY](er-functions-list-allitemsquery.md) function.</span></span>

## <a name="example-1"></a><span data-ttu-id="2c111-117">例 1</span><span class="sxs-lookup"><span data-stu-id="2c111-117">Example 1</span></span>

<span data-ttu-id="2c111-118">データソース **DS** として `SPLIT("abcdef" , 2)` を入力すると、`COUNT( ALLITEMS (DS))` 式は **3** を返します。</span><span class="sxs-lookup"><span data-stu-id="2c111-118">If you enter `SPLIT("abcdef" , 2)` as data source **DS**, the expression `COUNT( ALLITEMS (DS))` returns **3**.</span></span>

## <a name="example-2"></a><span data-ttu-id="2c111-119">例 2</span><span class="sxs-lookup"><span data-stu-id="2c111-119">Example 2</span></span>

<span data-ttu-id="2c111-120">VendTable アプリケーション テーブルを参照する *レコード リスト* データ タイプのデータ ソースとして **Vend** を入力すると、`ALLITEMS (Vend.'<Relations'.ContactPerson)` 式は、**ContactPerson** テーブル構造を持ち、**ContactPerson.ContactForParty == VendTable.Party** 関係を使用してアクセスできるすべての連絡担当者を含み、参照された仕入先テーブルから仕入先に利用可能なレコードのフラット化されたリストを返します。</span><span class="sxs-lookup"><span data-stu-id="2c111-120">If you enter **Vend** as the data source of the *Record list* data type that refers to the VendTable application table, the expression `ALLITEMS (Vend.'<Relations'.ContactPerson)` returns a flattened list of records that has the **ContactPerson** table structure and contains all contact persons that can be accessed by using the **ContactPerson.ContactForParty == VendTable.Party** relation, and that is available for all vendors from the referenced vendor table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2c111-121">追加リソース</span><span class="sxs-lookup"><span data-stu-id="2c111-121">Additional resources</span></span>

[<span data-ttu-id="2c111-122">リスト機能</span><span class="sxs-lookup"><span data-stu-id="2c111-122">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]