---
title: QRCODE ER 機能
description: このトピックでは、QRCODE 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 92665936decc87b29f2fabb346f4d16745d0a30b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562664"
---
# <a name="qrcode-er-function"></a><span data-ttu-id="2d800-103">QRCODE ER 機能</span><span class="sxs-lookup"><span data-stu-id="2d800-103">QRCODE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d800-104">`QRCODE` 関数は、バイナリ形式の指定された文字列に対して、クイック応答コード (QRコード) イメージを表示する *コンテナー* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="2d800-104">The `QRCODE` function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d800-105">構文</span><span class="sxs-lookup"><span data-stu-id="2d800-105">Syntax</span></span>

```vb
QRCODE (text)
```

## <a name="arguments"></a><span data-ttu-id="2d800-106">引数</span><span class="sxs-lookup"><span data-stu-id="2d800-106">Arguments</span></span>

<span data-ttu-id="2d800-107">`text`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="2d800-107">`text`: *String*</span></span>

<span data-ttu-id="2d800-108">オリジナルのテキストを表す *文字列* 値。</span><span class="sxs-lookup"><span data-stu-id="2d800-108">A *String* value that represents the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="2d800-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="2d800-109">Return values</span></span>

<span data-ttu-id="2d800-110">*コンテナー*</span><span class="sxs-lookup"><span data-stu-id="2d800-110">*Container*</span></span>

<span data-ttu-id="2d800-111">結果のバイナリ ストリーム。</span><span class="sxs-lookup"><span data-stu-id="2d800-111">The resulting binary stream.</span></span>

## <a name="example"></a><span data-ttu-id="2d800-112">例</span><span class="sxs-lookup"><span data-stu-id="2d800-112">Example</span></span>

<span data-ttu-id="2d800-113">定義済みのテンプレートを使用して、電子報告 (ER) 形式をコンフィギュレーションし、Microsoft Office 形式 (Excel ブックまたは Word 文書) の送信ドキュメントを生成することができます。</span><span class="sxs-lookup"><span data-stu-id="2d800-113">You can configure an Electronic reporting (ER) format to generate an outbound document in Microsoft Office format (Excel workbooks or Word documents) by using a predefined template.</span></span> <span data-ttu-id="2d800-114">このテンプレートには、QR コード画像のプレースホルダーとして **画像** オブジェクト (Excel ブック) または **画像コンテンツ コントロール** (Word 文書) を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="2d800-114">This template may contain a **Picture** object (Excel workbook) or a **Picture Content Control** (Word document) as a placeholder for a QR code image.</span></span> <span data-ttu-id="2d800-115">コンフィギュレーションされた ER 形式に、このプレースホルダーを塗りつぶすために使用する **セル** 要素を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2d800-115">You need to add to the configured ER format a **Cell** element that will be used to fill this placeholder in.</span></span> <span data-ttu-id="2d800-116">QR コードにどの情報を格納するかを指定するには、この **セル** 要素に対してバインドを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2d800-116">To specify what information will be stored in a QR code, you need to define a binding for this **Cell** element.</span></span> <span data-ttu-id="2d800-117">たとえば、次の式を含むようにバインドをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="2d800-117">For example, you can configure such binding as containing the following expression:</span></span>

```vb
QRCODE (model.ListOfShelfLabels.LabelText)`
```

<span data-ttu-id="2d800-118">コンフィギュレーションされた ER 形式を実行すると、**model.ListOfShelfLabels** データ ソースの **LabelText** フィールドは QR コード画像を生成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2d800-118">When you run the configured ER format, the text value of the **LabelText** field of the **model.ListOfShelfLabels** data source will be used to generate a QR code image.</span></span> <span data-ttu-id="2d800-119">この画像は、送信ドキュメントを生成するために使用するドキュメント テンプレートの QR コード画像のプレースホルダーを置き換えます。</span><span class="sxs-lookup"><span data-stu-id="2d800-119">This image will replace a QR code image placeholder in the document template using to generate an outbound document.</span></span> <span data-ttu-id="2d800-120">生成されたドキュメントの画像がスキャンされると、**model.ListOfShelfLabels** データ ソースの **LabelText** フィールドから取得されたテキストを返します。</span><span class="sxs-lookup"><span data-stu-id="2d800-120">When this image of the generated document is scanned, it returns the text that was taken from the **LabelText** field of the **model.ListOfShelfLabels** data source.</span></span> <span data-ttu-id="2d800-121">詳細については、[ER を使用して生成されるドキュメントへの画像や図形の埋め込み](electronic-reporting-embed-images-shapes.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2d800-121">For more information, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2d800-122">追加リソース</span><span class="sxs-lookup"><span data-stu-id="2d800-122">Additional resources</span></span>

[<span data-ttu-id="2d800-123">テキスト関数</span><span class="sxs-lookup"><span data-stu-id="2d800-123">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]