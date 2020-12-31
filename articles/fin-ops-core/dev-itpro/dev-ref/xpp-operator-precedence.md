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
ms.custom: 6174
ms.assetid: dd4a4971-c35a-466d-9c24-244cd75f9020
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e3dac0a00a88c7460f821600840e29596f74ba4
ms.sourcegitcommit: 9e31a7347800d8d453d7be2c0f826010be946e95
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2020
ms.locfileid: "4409591"
---
# <a name="operator-precedence"></a><span data-ttu-id="1c69d-103">演算子の優先順位</span><span class="sxs-lookup"><span data-stu-id="1c69d-103">Operator precedence</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1c69d-104">このトピックでは、演算子の優先順位について説明します。</span><span class="sxs-lookup"><span data-stu-id="1c69d-104">This topic describes operator precedence.</span></span>

<span data-ttu-id="1c69d-105">複合式を評価する順番は重要です。</span><span class="sxs-lookup"><span data-stu-id="1c69d-105">The order in which a compound expression is evaluated is important.</span></span> <span data-ttu-id="1c69d-106">オペレーションを実行する順序をコンパイラに明示的に伝えていない場合、順序は演算子の優先順位に基づいています。</span><span class="sxs-lookup"><span data-stu-id="1c69d-106">If you do not explicitly tell the compiler the order that you want operations to be performed in, the order is based on operator precedence.</span></span> <span data-ttu-id="1c69d-107">かっこ `( )` を使用すると、式の評価方法を明示的に X++ コンパイラに指示することができます。</span><span class="sxs-lookup"><span data-stu-id="1c69d-107">You can use parentheses `( )` to explicitly tell the X++ compiler how you want an expression to be evaluated.</span></span>

<span data-ttu-id="1c69d-108">たとえば、式 `x + y / 100` では、追加または区分を最初に実行するかどうかによって、結果が異なります。</span><span class="sxs-lookup"><span data-stu-id="1c69d-108">Consider the expression `x + y / 100`, which gives a different result depending on whether the addition or the division is performed first.</span></span>  <span data-ttu-id="1c69d-109">除算演算子には、加算演算子より高い優先順位があるため、コンパイラはまず `y/100` を評価します。</span><span class="sxs-lookup"><span data-stu-id="1c69d-109">Because the division operator has a higher precedence than the addition operator, the compiler evaluates `y/100` first.</span></span> <span data-ttu-id="1c69d-110">つまり、`x + y / 100` は `x + (y / 100)` と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="1c69d-110">So, `x + y / 100` is equivalent to `x + (y / 100)`.</span></span> <span data-ttu-id="1c69d-111">式 `(x + y)/ 100` を作成するためにかっこを追加すると、`x + y` が最初に評価されます。</span><span class="sxs-lookup"><span data-stu-id="1c69d-111">If you add parentheses to make the expression `(x + y)/ 100`, then `x + y` is evaluated first.</span></span>

<span data-ttu-id="1c69d-112">コードを読みやすく管理しやすくするために、明示的にし、最初に評価すべき演算子をかっこで示します。</span><span class="sxs-lookup"><span data-stu-id="1c69d-112">To make your code easy to read and maintain, be explicit, and indicate with parentheses which operators should be evaluated first.</span></span>

## <a name="order-of-operator-precedence"></a><span data-ttu-id="1c69d-113">演算子の優先度順</span><span class="sxs-lookup"><span data-stu-id="1c69d-113">Order of operator precedence</span></span>

<span data-ttu-id="1c69d-114">次のテーブルの演算子は、優先順位の順に並べられています。</span><span class="sxs-lookup"><span data-stu-id="1c69d-114">The operators in the following table are listed in precedence order.</span></span> <span data-ttu-id="1c69d-115">テーブルの演算子は高いほど、その優先順位が高くなります。</span><span class="sxs-lookup"><span data-stu-id="1c69d-115">The higher in the table an operator appears, the higher precedence it has.</span></span> <span data-ttu-id="1c69d-116">高い優先順位がある演算子は、低い優先順位がある演算子より前に評価されます。</span><span class="sxs-lookup"><span data-stu-id="1c69d-116">Operators with higher precedence are evaluated before operators with a lower precedence.</span></span> <span data-ttu-id="1c69d-117">X++ の演算子の優先順位は、C# および Java などの他の言語と同じではありません。</span><span class="sxs-lookup"><span data-stu-id="1c69d-117">The operator precedence of X++ is not the same as other languages, for example C# and Java.</span></span>


|              <span data-ttu-id="1c69d-118">演算子 (優先順位)</span><span class="sxs-lookup"><span data-stu-id="1c69d-118">Operators in precedence order</span></span>               |                 <span data-ttu-id="1c69d-119">構文</span><span class="sxs-lookup"><span data-stu-id="1c69d-119">Syntax</span></span>                 |
|----------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="1c69d-120">単項演算子</span><span class="sxs-lookup"><span data-stu-id="1c69d-120">unary operators</span></span>                                          | `- ~ !`                  |
| <span data-ttu-id="1c69d-121">乗算、シフト、AND、ビット演算排他的 OR</span><span class="sxs-lookup"><span data-stu-id="1c69d-121">multiplicative, shift, bitwise AND, bitwise exclusive OR</span></span> | `* / % DIV << >> & ^`    |
| <span data-ttu-id="1c69d-122">加法、ビット演算包括的 OR</span><span class="sxs-lookup"><span data-stu-id="1c69d-122">additive, bitwise inclusive OR</span></span>                           | `+ -`                   |
| <span data-ttu-id="1c69d-123">リレーショナル、同等</span><span class="sxs-lookup"><span data-stu-id="1c69d-123">relational, equality</span></span>                                     | `< <= == != > >= like as is` |
| <span data-ttu-id="1c69d-124">論理演算子 (AND、OR)</span><span class="sxs-lookup"><span data-stu-id="1c69d-124">logical operators (AND, OR)</span></span>                              | `&& ||`             |
| <span data-ttu-id="1c69d-125">条件付</span><span class="sxs-lookup"><span data-stu-id="1c69d-125">conditional</span></span>                                              | `? :`                   |

<span data-ttu-id="1c69d-126">テーブルの同じ行の演算子には、同等な優先順位があります。</span><span class="sxs-lookup"><span data-stu-id="1c69d-126">Operators on the same line in the table have equal precedence.</span></span> <span data-ttu-id="1c69d-127">式にこれらの演算子が 1 つ以上ある場合、代入演算子が使用されていない限り、式は左から右に評価されます。</span><span class="sxs-lookup"><span data-stu-id="1c69d-127">If there are more than one of these operators in an expression, the expression is evaluated from left to right unless assignment operators are used.</span></span> <span data-ttu-id="1c69d-128">代入演算子は右から左に評価されます。</span><span class="sxs-lookup"><span data-stu-id="1c69d-128">Assignment operators are evaluated from right to left.</span></span> <span data-ttu-id="1c69d-129">たとえば、`&&` (論理的 AND) および `||` (論理的 OR) は、優先順位が等しく、左から右に評価されます。</span><span class="sxs-lookup"><span data-stu-id="1c69d-129">For example, `&&` (logical AND) and `||` (logical OR) have the same precedence and are evaluated from left to right.</span></span> <span data-ttu-id="1c69d-130">つまり、`0 && 0 || 1 == 1`、および `1 || 0 && 0 == 0` です</span><span class="sxs-lookup"><span data-stu-id="1c69d-130">This means that `0 && 0 || 1 == 1`, and `1 || 0 && 0 == 0`</span></span>
