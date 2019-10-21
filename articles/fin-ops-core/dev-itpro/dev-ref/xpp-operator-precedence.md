---
title: 演算子の優先順位
description: このトピックでは、演算子の優先順位について説明します。
author: pvillads
manager: AnnBe
ms.date: 07/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 6174
ms.assetid: dd4a4971-c35a-466d-9c24-244cd75f9020
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 97d957d20d53e00ddfddaf24fe5e04f28034756e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191595"
---
# <a name="operator-precedence"></a><span data-ttu-id="d869a-103">演算子の優先順位</span><span class="sxs-lookup"><span data-stu-id="d869a-103">Operator precedence</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d869a-104">このトピックでは、演算子の優先順位について説明します。</span><span class="sxs-lookup"><span data-stu-id="d869a-104">This topic describes operator precedence.</span></span>

<span data-ttu-id="d869a-105">複合式を評価する順番は重要です。</span><span class="sxs-lookup"><span data-stu-id="d869a-105">The order in which a compound expression is evaluated is important.</span></span> <span data-ttu-id="d869a-106">たとえば、(x + y / 100) は追加または区分を最初に実行するかどうかによって、結果が異なります。</span><span class="sxs-lookup"><span data-stu-id="d869a-106">For example, (x + y / 100) gives a different result depending on whether the addition or the division is performed first.</span></span> <span data-ttu-id="d869a-107">かっこ () を使用すると、式の評価方法を明示的に X++ コンパイラに指示することができます。</span><span class="sxs-lookup"><span data-stu-id="d869a-107">You can use parentheses ( ) to explicitly tell the X++ compiler how you want an expression to be evaluated.</span></span> <span data-ttu-id="d869a-108">例えば、(x + y)/ 100。</span><span class="sxs-lookup"><span data-stu-id="d869a-108">For example, (x + y)/ 100.</span></span> <span data-ttu-id="d869a-109">オペレーションを実行する順序をコンパイラーに明示的に伝えていない場合、順序はオペレーターに割り当てられた優先順位に基づいています。</span><span class="sxs-lookup"><span data-stu-id="d869a-109">If you do not explicitly tell the compiler the order that you want operations to be performed in, the order is based on the precedence assigned to the operators.</span></span> <span data-ttu-id="d869a-110">たとえば、除算演算子には、加算演算子より高い優先順位があります。</span><span class="sxs-lookup"><span data-stu-id="d869a-110">For example, the division operator has a higher precedence than the addition operator.</span></span> <span data-ttu-id="d869a-111">x + y / 100 については、コンパイラは y/100 を最初に評価します。</span><span class="sxs-lookup"><span data-stu-id="d869a-111">For x + y / 100, the compiler would evaluate y/100 first.</span></span> <span data-ttu-id="d869a-112">つまり、x + y/100 は x + (y/100) と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="d869a-112">So, x + y / 100 is equivalent to x + (y / 100).</span></span> <span data-ttu-id="d869a-113">コードを読みやすく管理しやすくするために、明示的に記述します。</span><span class="sxs-lookup"><span data-stu-id="d869a-113">To make your code easy to read and maintain, be explicit.</span></span> <span data-ttu-id="d869a-114">最初に評価すべき演算子をかっこで示します。</span><span class="sxs-lookup"><span data-stu-id="d869a-114">Indicate with parentheses which operators should be evaluated first.</span></span>

## <a name="order-of-operator-precedence"></a><span data-ttu-id="d869a-115">演算子の優先度順</span><span class="sxs-lookup"><span data-stu-id="d869a-115">Order of operator precedence</span></span>
<span data-ttu-id="d869a-116">次のテーブルの演算子は、優先順位の順に並べられています。</span><span class="sxs-lookup"><span data-stu-id="d869a-116">The operators in the following table are listed in precedence order.</span></span> <span data-ttu-id="d869a-117">テーブルの演算子は高いほど、その優先順位が高くなります。</span><span class="sxs-lookup"><span data-stu-id="d869a-117">The higher in the table an operator appears, the higher precedence it has.</span></span> <span data-ttu-id="d869a-118">高い優先順位がある演算子は、低い優先順位がある演算子より前に評価されます。</span><span class="sxs-lookup"><span data-stu-id="d869a-118">Operators with higher precedence are evaluated before operators with a lower precedence.</span></span> <span data-ttu-id="d869a-119">X++ の演算子の優先順位は、C\# および Java などの他の言語と同じではないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d869a-119">Note that the operator precedence of X++ is not the same as other languages, for example C\# and Java.</span></span>


|              <span data-ttu-id="d869a-120">演算子 (優先順位)</span><span class="sxs-lookup"><span data-stu-id="d869a-120">Operators in precedence order</span></span>               |                 <span data-ttu-id="d869a-121">構文</span><span class="sxs-lookup"><span data-stu-id="d869a-121">Syntax</span></span>                 |
|----------------------------------------------------------|----------------------------------------|
|                     <span data-ttu-id="d869a-122">単項演算子</span><span class="sxs-lookup"><span data-stu-id="d869a-122">unary operators</span></span>                      |                 <span data-ttu-id="d869a-123">- ～ !</span><span class="sxs-lookup"><span data-stu-id="d869a-123">- ~ !</span></span>                  |
| <span data-ttu-id="d869a-124">乗算、シフト、AND、ビット演算排他的 OR</span><span class="sxs-lookup"><span data-stu-id="d869a-124">multiplicative, shift, bitwise AND, bitwise exclusive OR</span></span> |    <span data-ttu-id="d869a-125">\* / % DIV &lt;&lt; &gt;&gt; & ^</span><span class="sxs-lookup"><span data-stu-id="d869a-125">\* / % DIV &lt;&lt; &gt;&gt; & ^</span></span>    |
|              <span data-ttu-id="d869a-126">加法、ビット演算包括的 OR</span><span class="sxs-lookup"><span data-stu-id="d869a-126">additive, bitwise inclusive OR</span></span>              |                  <span data-ttu-id="d869a-127">+ -</span><span class="sxs-lookup"><span data-stu-id="d869a-127">+ -</span></span>                   |
|                   <span data-ttu-id="d869a-128">リレーショナル、同等</span><span class="sxs-lookup"><span data-stu-id="d869a-128">relational, equality</span></span>                   | <span data-ttu-id="d869a-129">&lt; &lt;= == != &gt; &gt;= 現状のとおり</span><span class="sxs-lookup"><span data-stu-id="d869a-129">&lt; &lt;= == != &gt; &gt;= like as is</span></span> |
|               <span data-ttu-id="d869a-130">論理演算子 (AND、OR)</span><span class="sxs-lookup"><span data-stu-id="d869a-130">logical operators (AND, OR)</span></span>                |            <span data-ttu-id="d869a-131">&& &#124;&#124;</span><span class="sxs-lookup"><span data-stu-id="d869a-131">&& &#124;&#124;</span></span>             |
|                       <span data-ttu-id="d869a-132">条件付</span><span class="sxs-lookup"><span data-stu-id="d869a-132">conditional</span></span>                        |                  <span data-ttu-id="d869a-133">?</span><span class="sxs-lookup"><span data-stu-id="d869a-133">?</span></span> <span data-ttu-id="d869a-134">:</span><span class="sxs-lookup"><span data-stu-id="d869a-134">:</span></span>                   |

<span data-ttu-id="d869a-135">同じ行の演算子には、同等な優先順位があります。</span><span class="sxs-lookup"><span data-stu-id="d869a-135">Operators on the same line have equal precedence.</span></span> <span data-ttu-id="d869a-136">式にあるこれらの演算子が 1 つ以上ある場合、代入演算子が使用されていない限り、式は左から右に評価されます (これらは右から左に評価されます)。</span><span class="sxs-lookup"><span data-stu-id="d869a-136">If there is more than one of these operators in an expression, the expression is evaluated from left to right unless assignment operators are used (these are evaluated from right to left).</span></span> <span data-ttu-id="d869a-137">たとえば、&& (論理的 AND) および || (論理的 OR) は、優先順位が等しく、左から右に評価されます。</span><span class="sxs-lookup"><span data-stu-id="d869a-137">For example, && (logical AND) and || (logical OR) have the same precedence and are evaluated from left to right.</span></span> <span data-ttu-id="d869a-138">つまり、0&&0||1 == 1、および 1||0&&0 == 0 です</span><span class="sxs-lookup"><span data-stu-id="d869a-138">This means that :0&&0||1 == 1, and 1||0&&0 == 0</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d869a-139">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="d869a-139">Additional resources</span></span>
<span data-ttu-id="d869a-140">[代入演算子](https://msdn.microsoft.com/library/d4e86b9c-be82-4f19-ad86-7722344a05f3(AX.60).aspx)</span><span class="sxs-lookup"><span data-stu-id="d869a-140">[Assignment Operators](https://msdn.microsoft.com/library/d4e86b9c-be82-4f19-ad86-7722344a05f3(AX.60).aspx)</span></span>

<span data-ttu-id="d869a-141">[算術演算子](https://msdn.microsoft.com/library/cffbc613-3875-4520-9dea-046dc99aab99(AX.60).aspx)</span><span class="sxs-lookup"><span data-stu-id="d869a-141">[Arithmetic Operators](https://msdn.microsoft.com/library/cffbc613-3875-4520-9dea-046dc99aab99(AX.60).aspx)</span></span>

<span data-ttu-id="d869a-142">[リレーショナル演算子](https://msdn.microsoft.com/library/702af366-4d46-445e-bd4b-722c9845199f(AX.60).aspx)</span><span class="sxs-lookup"><span data-stu-id="d869a-142">[Relational Operators](https://msdn.microsoft.com/library/702af366-4d46-445e-bd4b-722c9845199f(AX.60).aspx)</span></span>





