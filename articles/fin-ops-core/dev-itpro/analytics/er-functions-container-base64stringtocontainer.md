---
title: Base64StringToContainer ER 関数
description: このトピックでは、Base64StringToContainer 電子申告 (ER) 関数の使用方法について説明します。
author: NickSelin
manager: kfend
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 0e92ae41a3e0f03cb14d4791ab768f096f2a0523
ms.sourcegitcommit: e8a46e127d70986539c138b27a641bff6f6874d0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/15/2020
ms.locfileid: "4739092"
---
# <a name="base64stringtocontainer-er-function"></a><span data-ttu-id="a87c3-103">Base64StringToContainer ER 関数</span><span class="sxs-lookup"><span data-stu-id="a87c3-103">Base64StringToContainer ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a87c3-104">`BASE64STRINGTOCONTAINER` [関数](er-formula-language.md#functions) は、指定された *文字列* 型の入力を *[コンテナー](er-functions-category-container.md)* 型のデータ項目に変換します。</span><span class="sxs-lookup"><span data-stu-id="a87c3-104">The `BASE64STRINGTOCONTAINER` [function](er-formula-language.md#functions) converts the specified input of the *String* type to a data item of the *[Container](er-functions-category-container.md)* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="a87c3-105">構文</span><span class="sxs-lookup"><span data-stu-id="a87c3-105">Syntax</span></span>

```vb
BASE64STRINGTOCONTAINER (input)
```

## <a name="arguments"></a><span data-ttu-id="a87c3-106">引数</span><span class="sxs-lookup"><span data-stu-id="a87c3-106">Arguments</span></span>

<span data-ttu-id="a87c3-107">`input`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="a87c3-107">`input`: *String*</span></span>

<span data-ttu-id="a87c3-108">*文字列* 型のデータ ソースの有効なパス。</span><span class="sxs-lookup"><span data-stu-id="a87c3-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="a87c3-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="a87c3-109">Return values</span></span>

<span data-ttu-id="a87c3-110">*コンテナー*</span><span class="sxs-lookup"><span data-stu-id="a87c3-110">*Container*</span></span>

<span data-ttu-id="a87c3-111">バイナリ ラージ オブジェクト (BLOB) 形式の結果バイナリ値。</span><span class="sxs-lookup"><span data-stu-id="a87c3-111">The resulting binary value in binary large object (BLOB) format.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a87c3-112">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="a87c3-112">Usage notes</span></span>

<span data-ttu-id="a87c3-113">入力文字列が、バイナリからテキストへのエンコード スキームの正しい Base64 グループを提供しない場合、"パラメーターが無効です" という例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="a87c3-113">The "Parameter is not valid" exception is thrown if the input string doesn't provide a correct Base64 group of binary-to-text encoding schemes.</span></span>

## <a name="example"></a><span data-ttu-id="a87c3-114">例</span><span class="sxs-lookup"><span data-stu-id="a87c3-114">Example</span></span>

<span data-ttu-id="a87c3-115">モデル マッピングでは、次のデータ ソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="a87c3-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="a87c3-116">**DocuTypeGroup** アプリケーションの列挙を参照する *Dynamics 365 for Operations / 列挙型* タイプのルート **DocuTypeGroupEnum** データ ソース</span><span class="sxs-lookup"><span data-stu-id="a87c3-116">The root **DocuTypeGroupEnum** data source of the *Dynamics 365 for Operations / Enumeration* type that refers to the **DocuTypeGroup** application enumeration</span></span>
- <span data-ttu-id="a87c3-117">**CustTable** アプリケーション テーブルを参照する *Dynamics 365 for Operations / テーブル レコード* タイプのルート **Customer** データ ソース</span><span class="sxs-lookup"><span data-stu-id="a87c3-117">The root **Customer** data source of the *Dynamics 365 for Operations / Table records* type that refers to the **CustTable** application table</span></span>
- <span data-ttu-id="a87c3-118">次のように構成された の 方法で構成 された *計算フィールド* 型の **\#Media** データ ソース:</span><span class="sxs-lookup"><span data-stu-id="a87c3-118">The **\#Media** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="a87c3-119">**Customer** データ ソースの子データ ソースとして追加されます。</span><span class="sxs-lookup"><span data-stu-id="a87c3-119">It's added as a child data source of the **Customer** data source.</span></span>
    - <span data-ttu-id="a87c3-120">式 `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)` を含みます。</span><span class="sxs-lookup"><span data-stu-id="a87c3-120">It contains the expression `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.</span></span>

- <span data-ttu-id="a87c3-121">次のように構成された *計算フィールド* 型の **\#MediaAsBase64String** データ ソース:</span><span class="sxs-lookup"><span data-stu-id="a87c3-121">The **\#MediaAsBase64String** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="a87c3-122">**Customer.'\#Media'** データ ソースの子データ ソースとして追加されます。</span><span class="sxs-lookup"><span data-stu-id="a87c3-122">It's added as a child data source of the **Customer.'\#Media'** data source.</span></span>
    - <span data-ttu-id="a87c3-123">式 `Customer.'#Media'.'getFileContentAsBase64String()'` を含みます。</span><span class="sxs-lookup"><span data-stu-id="a87c3-123">It contains the expression `Customer.'#Media'.'getFileContentAsBase64String()'`.</span></span>

- <span data-ttu-id="a87c3-124">次のように構成された *計算フィールド* 型の **\#BlobFomBase64** データ ソース:</span><span class="sxs-lookup"><span data-stu-id="a87c3-124">The **\#BlobFomBase64** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="a87c3-125">**Customer.'\#Media'** データ ソースの子データ ソースとして追加されます。</span><span class="sxs-lookup"><span data-stu-id="a87c3-125">It's added as a child data source of the **Customer.'\#Media'** data source.</span></span>
    - <span data-ttu-id="a87c3-126">式 `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'` を含みます。</span><span class="sxs-lookup"><span data-stu-id="a87c3-126">It contains the expression `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.</span></span>

<span data-ttu-id="a87c3-127">この例では、**\#MediaAsBase64String** データ ソースは、現在のメディア添付ファイルのバイナリ コンテンツを、バイナリからテキストへのエンコード スキームの Base64 グループを表すテキストとしてエンコードします。</span><span class="sxs-lookup"><span data-stu-id="a87c3-127">In this example, the **\#MediaAsBase64String** data source encodes the binary content of the current media attachment as text that represents a Base64 group of binary-to-text encoding schemes.</span></span> <span data-ttu-id="a87c3-128">**\#BlobFomBase64** データ ソースは、Base64 文字列をデコードし、BLOB 形式のバイナリ値を返します。</span><span class="sxs-lookup"><span data-stu-id="a87c3-128">The **\#BlobFomBase64** data source decodes the Base64 string and returns a binary value in BLOB format.</span></span>

![ER モデル マッピング デザイナー ページのサンプル データ ソース](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a><span data-ttu-id="a87c3-130">追加リソース</span><span class="sxs-lookup"><span data-stu-id="a87c3-130">Additional resources</span></span>

[<span data-ttu-id="a87c3-131">コンテナー関数</span><span class="sxs-lookup"><span data-stu-id="a87c3-131">Container functions</span></span>](er-functions-category-container.md)
