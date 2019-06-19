---
title: 拡張データ型
description: このトピックでは、拡張データ型 (EDT) について説明します。
author: MichaelFruergaardPontoppidan
manager: AnnBe
ms.date: 09/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2018-09-09
ms.dyn365.ops.version: Platform update 20
ms.openlocfilehash: 6f9b02081fdfdead8b9c26e43992fcbd4bc5b7d4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544114"
---
# <a name="extended-data-types"></a><span data-ttu-id="d968c-103">拡張データ型</span><span class="sxs-lookup"><span data-stu-id="d968c-103">Extended data types</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="d968c-104">拡張データ型 (EDT) には、拡張担当者が特定の動作を変更できる豊富な拡張モデルがあります。</span><span class="sxs-lookup"><span data-stu-id="d968c-104">Extended data types (EDTs) have a rich extension model that lets extenders change specific behaviors.</span></span>

<span data-ttu-id="d968c-105">拡張可能なソリューションを提供するには、EDT を操作する際に次のガイドラインに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d968c-105">To provide an extensible solution, keep the following guidelines in mind when you work with EDTs.</span></span>

## <a name="labelhelp-text"></a><span data-ttu-id="d968c-106">ラベル/ヘルプ テキスト</span><span class="sxs-lookup"><span data-stu-id="d968c-106">Label/Help text</span></span>
<span data-ttu-id="d968c-107">ラベルおよびヘルプ テキストのプロパティは、拡張によって変更できますが、値は 1 つだけ残すことができます。</span><span class="sxs-lookup"><span data-stu-id="d968c-107">Labels and Help text properties can be changed by an extension, but only one value can remain.</span></span> <span data-ttu-id="d968c-108">複数のソリューションで同じ EDT のラベルが変更される場合、機能の観点でさまざまなラベルが相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="d968c-108">If multiple solutions change the label of the same EDT, the various labels are, in functional terms, mutually exclusive.</span></span> <span data-ttu-id="d968c-109">したがって、それらのラベルをすべて同じシステムにインストールすることはできません。</span><span class="sxs-lookup"><span data-stu-id="d968c-109">Therefore, those labels can't all be installed on the same system.</span></span>

## <a name="string-size"></a><span data-ttu-id="d968c-110">文字列サイズ</span><span class="sxs-lookup"><span data-stu-id="d968c-110">String size</span></span>
<span data-ttu-id="d968c-111">文字列サイズは、ルート EDT でのみ定義できます。</span><span class="sxs-lookup"><span data-stu-id="d968c-111">String size can be defined only on root EDTs.</span></span> <span data-ttu-id="d968c-112">EDT とその拡張の間で定義されている最大値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="d968c-112">The system will use the largest value that is defined across the EDT and its extensions.</span></span>

<span data-ttu-id="d968c-113">派生 EDT の場合、EDT 間の IS-A 関係が壊れるため、文字列サイズを拡張によって変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="d968c-113">For derived EDTs, string size can't be changed by an extension, because the IS-A relationship between the EDTs will be broken.</span></span>

<span data-ttu-id="d968c-114">文字列 EDT への割り当てでは、定義されている文字列のサイズを照合するために文字列が切り捨てられます。</span><span class="sxs-lookup"><span data-stu-id="d968c-114">Assignments to string EDTs will truncate the string to match the defined string size.</span></span>

## <a name="extends"></a><span data-ttu-id="d968c-115">拡張</span><span class="sxs-lookup"><span data-stu-id="d968c-115">Extends</span></span>
<span data-ttu-id="d968c-116">拡張によって**拡張**プロパティを変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="d968c-116">The **extends** property can't be changed by an extension.</span></span> <span data-ttu-id="d968c-117">リリース後にこのプロパティに対して行った変更はすべて、重大な変更を引き起こします。</span><span class="sxs-lookup"><span data-stu-id="d968c-117">Any change that is made to this property after release will cause a breaking change.</span></span> <span data-ttu-id="d968c-118">したがって、リリース前に、プロパティが正しく設定されていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d968c-118">Therefore, you must make sure that the property is set correctly before release.</span></span>

<span data-ttu-id="d968c-119">このプロパティを設定した場合、自分も拡張担当者も後での文字列サイズを変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="d968c-119">If you set this property, neither you nor extenders will be able to make changes to the string size later.</span></span> 

<span data-ttu-id="d968c-120">不要な依存関係を回避してください。</span><span class="sxs-lookup"><span data-stu-id="d968c-120">Avoid unnecessary dependencies.</span></span> <span data-ttu-id="d968c-121">たとえば、名前や説明などの一般的な EDT を拡張しないでください。</span><span class="sxs-lookup"><span data-stu-id="d968c-121">For example, don't extend generic EDTs such as Name and Description.</span></span>

## <a name="number-of-decimals"></a><span data-ttu-id="d968c-122">小数点以下の桁数</span><span class="sxs-lookup"><span data-stu-id="d968c-122">Number of decimals</span></span>
<span data-ttu-id="d968c-123">拡張によって**拡張によって**プロパティを変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="d968c-123">The **Number of decimals** property can't be changed by an extension.</span></span>

<span data-ttu-id="d968c-124">このプロパティを **True** に設定した場合、拡張担当者は小数点以下桁数を変更できます。</span><span class="sxs-lookup"><span data-stu-id="d968c-124">If you set this property to **True**, extenders can change the number of decimal places.</span></span> 

<span data-ttu-id="d968c-125">このプロパティを **True** に設定した場合、以下の条件を満たすことを確認します。</span><span class="sxs-lookup"><span data-stu-id="d968c-125">If you set this property to **True**, make sure that the following conditions are met:</span></span>

+ <span data-ttu-id="d968c-126">暗黙的またはハードコードされた四捨五入が発生しないように、すべての切り捨てロジックでは、EDT で指定されている小数点以下の桁数が受け入れられます。</span><span class="sxs-lookup"><span data-stu-id="d968c-126">All truncation logic honors the number of decimal places that is specified on the EDT, so that no implicit or hardcoded rounding will occur.</span></span>
+ <span data-ttu-id="d968c-127">この値は、四捨五入が正しく処理されないその他の互換性のない EDT には割り当てられません。</span><span class="sxs-lookup"><span data-stu-id="d968c-127">The value isn't assigned to other incompatible EDTs that don't correctly handle rounding.</span></span>
