---
title: コンテナー カテゴリ内の ER 関数のリスト
description: このトピックでは、電子申告 (ER) でサポートされるコンテナー関数について説明します。
author: NickSelin
manager: kfend
ms.date: 12/14/2020
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
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: b7e7d770c334647f8f11338d49b39a2e9cb5c04c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561761"
---
# <a name="list-of-er-functions-in-the-container-category"></a><span data-ttu-id="a11bf-103">コンテナー カテゴリ内の ER 関数のリスト</span><span class="sxs-lookup"><span data-stu-id="a11bf-103">List of ER functions in the container category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a11bf-104">[電子申告 (ER)](general-electronic-reporting.md) コンテナー [関数](er-formula-language.md#functions) を使用して、*コンテナー* データ型のデータ ソースを含む操作を実行するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="a11bf-104">[Electronic reporting (ER)](general-electronic-reporting.md) container [functions](er-formula-language.md#functions) can be used to perform operations that involve data sources of the *Container* data type.</span></span> <span data-ttu-id="a11bf-105">これらの操作は、処理データがバイナリ ラージ オブジェクト (BLOB) 形式でバイナリ データのコレクションを表す場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="a11bf-105">These operations occur when the processing data represents a collection of binary data in binary large object (BLOB) format.</span></span> <span data-ttu-id="a11bf-106">このトピックでは、これらの関数の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="a11bf-106">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="a11bf-107">サポートされている関数のリスト</span><span class="sxs-lookup"><span data-stu-id="a11bf-107">List of supported functions</span></span>

| <span data-ttu-id="a11bf-108">関数</span><span class="sxs-lookup"><span data-stu-id="a11bf-108">Function</span></span> | <span data-ttu-id="a11bf-109">説明</span><span class="sxs-lookup"><span data-stu-id="a11bf-109">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="a11bf-110">Base64StringToContainer</span><span class="sxs-lookup"><span data-stu-id="a11bf-110">Base64StringToContainer</span></span>](er-functions-container-base64stringtocontainer.md) | <span data-ttu-id="a11bf-111">この関数は、バイナリからテキストへのエンコード スキームの Base64 グループを表す、指定された ASCII 文字列からデコードされるバイナリ コンテンツで構成される *コンテナー* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="a11bf-111">This function returns a *Container* value that consists of binary content that is decoded from the specified ASCII string that represents a Base64 group of binary-to-text encoding schemes.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="a11bf-112">追加リソース</span><span class="sxs-lookup"><span data-stu-id="a11bf-112">Additional resources</span></span>

[<span data-ttu-id="a11bf-113">電子申告の概要</span><span class="sxs-lookup"><span data-stu-id="a11bf-113">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="a11bf-114">電子申告のフォーミュラ デザイナー</span><span class="sxs-lookup"><span data-stu-id="a11bf-114">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="a11bf-115">電子報告のフォーミュラ言語</span><span class="sxs-lookup"><span data-stu-id="a11bf-115">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]