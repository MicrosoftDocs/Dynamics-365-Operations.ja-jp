---
title: X++ 文字列ランタイム関数
description: このトピックでは、文字列ランタイム関数について説明します。
author: RobinARH
ms.date: 08/15/2019
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.custom: 31401
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4cd0d6cc9bbafd960fbfb88848f16abd7a02abaa
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2021
ms.locfileid: "6190327"
---
# <a name="x-string-runtime-functions"></a><span data-ttu-id="0e6d7-103">X++ 文字列ランタイム関数</span><span class="sxs-lookup"><span data-stu-id="0e6d7-103">X++ string runtime functions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0e6d7-104">このトピックでは、文字列ランタイム関数について説明します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-104">This topic describes the string run-time functions.</span></span>

## <a name="match"></a><span data-ttu-id="0e6d7-105">照合</span><span class="sxs-lookup"><span data-stu-id="0e6d7-105">match</span></span>

<span data-ttu-id="0e6d7-106">文字列や別の文字列内の式を検索します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-106">Searches for a string or expression in another string.</span></span>

```xpp
int match(str pattern, str text)
```

### <a name="parameters"></a><span data-ttu-id="0e6d7-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-107">Parameters</span></span>

| <span data-ttu-id="0e6d7-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-108">Parameter</span></span> | <span data-ttu-id="0e6d7-109">説明</span><span class="sxs-lookup"><span data-stu-id="0e6d7-109">Description</span></span>                             |
|-----------|-----------------------------------------|
| <span data-ttu-id="0e6d7-110">pattern</span><span class="sxs-lookup"><span data-stu-id="0e6d7-110">pattern</span></span>   | <span data-ttu-id="0e6d7-111">検索する文字列または式。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-111">The string or expression to search for.</span></span> |
| <span data-ttu-id="0e6d7-112">テキスト</span><span class="sxs-lookup"><span data-stu-id="0e6d7-112">text</span></span>      | <span data-ttu-id="0e6d7-113">検索する文字列。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-113">The string to search.</span></span>                   |

### <a name="return-value"></a><span data-ttu-id="0e6d7-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="0e6d7-114">Return value</span></span>

<span data-ttu-id="0e6d7-115">パターンが文字列内にある場合は **1**、それ以外の場合は、**0** (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-115">**1** if the pattern is located in the string; otherwise, **0** (zero).</span></span>

### <a name="remarks"></a><span data-ttu-id="0e6d7-116">備考</span><span class="sxs-lookup"><span data-stu-id="0e6d7-116">Remarks</span></span>

<span data-ttu-id="0e6d7-117">検索では大文字と小文字が区別されません。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-117">The search is case-insensitive.</span></span> <span data-ttu-id="0e6d7-118">次の特殊文字を使用して、*pattern* パラメーターのパターンを作成できます。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-118">The following special characters can be used to create the pattern for the *pattern* parameter.</span></span>

+ <span data-ttu-id="0e6d7-119">**\\** バックスラッシュ (**\\**) は、特殊文字の特別な扱いを無効にしたりエスケープしたりするため、特殊文字を通常の文字のように一致させることができます。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-119">**\\**: A backslash (**\\**) nullifies, or escapes, the special treatment of special characters, so that a special character can be matched like a normal letter.</span></span> <span data-ttu-id="0e6d7-120">バックスラッシュのペアは、1 つの非特殊バックスラッシュに変換されます。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-120">A pair of backslashes is translated into one non-special backslash.</span></span> <span data-ttu-id="0e6d7-121">例</span><span class="sxs-lookup"><span data-stu-id="0e6d7-121">Examples:</span></span>

    + <span data-ttu-id="0e6d7-122">**照合("ab$cd","ab$cd");** は、**0** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-122">**match("ab$cd","ab$cd");** returns **0**.</span></span> 
    + <span data-ttu-id="0e6d7-123">**照合("ab\\$cd","ab$cd");** は、**0** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-123">**match("ab\\$cd","ab$cd");** returns **0**.</span></span> <span data-ttu-id="0e6d7-124">バックスラッシュはエスケープされません。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-124">The backslash isn't escaped.</span></span>
    + <span data-ttu-id="0e6d7-125">**照合("ab\\\\$cd","ab$cd");** は、**1** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-125">**match("ab\\\\$cd","ab$cd");** returns **1**.</span></span> <span data-ttu-id="0e6d7-126">バックスラッシュとドル記号はエスケープされます。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-126">The backslash and dollar sign are escaped.</span></span>

+ <span data-ttu-id="0e6d7-127">**< または ^**: 式の先頭にある始め山かっこ (**<**) またはサーカムフレックス (**^**) は、明細行の始まりと照合するために使用します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-127">**< or ^**: A left angle bracket (**<**) or a circumflex (**^**) at the start of an expression is used to match the start of a line.</span></span> <span data-ttu-id="0e6d7-128">例</span><span class="sxs-lookup"><span data-stu-id="0e6d7-128">Examples:</span></span>

    + <span data-ttu-id="0e6d7-129">**照合("<abc","abcdef");** は、 **1** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-129">**match("<abc","abcdef");** returns **1**.</span></span> 
    + <span data-ttu-id="0e6d7-130">**照合("<abc","defabc");** は、**0** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-130">**match("<abc","defabc");** returns **0**.</span></span> 
    + <span data-ttu-id="0e6d7-131">**照合("^abc","abcdef");** は、 **1** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-131">**match("^abc","abcdef");** returns **1**.</span></span> 
    + <span data-ttu-id="0e6d7-132">**照合("^abc","defabc");** は、**0** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-132">**match("^abc","defabc");** returns **0**.</span></span> 

+ <span data-ttu-id="0e6d7-133">**> または $**: 式の最後の終わり山かっこ (**>**;) またはドル記号 (**$**) は、明細行の末尾と照合するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-133">**> or $**: A right angle bracket (**>**) or a dollar sign (**$**) at the end of the expression is used to match the end of a line.</span></span> <span data-ttu-id="0e6d7-134">例</span><span class="sxs-lookup"><span data-stu-id="0e6d7-134">Examples:</span></span>

    + <span data-ttu-id="0e6d7-135">**照合("abc>","abcdef");** は、**0** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-135">**match("abc>","abcdef");** returns **0**.</span></span> 
    + <span data-ttu-id="0e6d7-136">**照合("abc>","defabc");** は、**1** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-136">**match("abc>","defabc");** returns **1**.</span></span> 

+ <span data-ttu-id="0e6d7-137">**? または .**: 疑問符 (**?**) またはピリオド (**.**) は、同じ位置にある任意の 1 文字と一致します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-137">**? or .**: A question mark (**?**) or a period (**.**) matches any one character in the same position.</span></span> <span data-ttu-id="0e6d7-138">例</span><span class="sxs-lookup"><span data-stu-id="0e6d7-138">Examples:</span></span>

    + <span data-ttu-id="0e6d7-139">**照合("abc.def","abc#def");** は、**1** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-139">**match("abc.def","abc#def");** returns **1**.</span></span> 
    + <span data-ttu-id="0e6d7-140">**照合("colou?r","colouXr");** は、**1** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-140">**match("colou?r","colouXr");** returns **1**.</span></span> 

+ <span data-ttu-id="0e6d7-141">**:x**: コロン (**:**) は、直後の文字が示すように、一致する文字のグループを指定します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-141">**:x**: A colon (**:**) specifies a group of characters to match, as indicated by the character that immediately follows.</span></span>

+ <span data-ttu-id="0e6d7-142">**:a**: 文字に一致を設定します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-142">**:a**: Sets the match to letters.</span></span> <span data-ttu-id="0e6d7-143">例</span><span class="sxs-lookup"><span data-stu-id="0e6d7-143">Examples:</span></span>

    + <span data-ttu-id="0e6d7-144">**照合("ab:acd","ab#cd");** は、**0** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-144">**match("ab:acd","ab#cd");** returns **0**.</span></span> 
    + <span data-ttu-id="0e6d7-145">**照合("ab:acd","abxyzcd");** は、**0** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-145">**match("ab:acd","abxyzcd");** returns **0**.</span></span> 
    + <span data-ttu-id="0e6d7-146">**照合("ab:acd","abxcd");** は、**1** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-146">**match("ab:acd","abxcd");** returns **1**.</span></span> 

+ <span data-ttu-id="0e6d7-147">**:d**: 数字に一致を設定します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-147">**:d**: Sets the match to numeric characters.</span></span> <span data-ttu-id="0e6d7-148">例</span><span class="sxs-lookup"><span data-stu-id="0e6d7-148">Examples:</span></span>

    + <span data-ttu-id="0e6d7-149">**照合("ab:dcd","ab3cd");** は、**1** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-149">**match("ab:dcd","ab3cd");** returns **1**.</span></span> 
    + <span data-ttu-id="0e6d7-150">**照合("ab:dcd","ab123cd");** は、**0** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-150">**match("ab:dcd","ab123cd");** returns **0**.</span></span> 
    + <span data-ttu-id="0e6d7-151">**照合("ab:dcd","abcd");** は、**0** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-151">**match("ab:dcd","abcd");** returns **0**.</span></span> 

+ <span data-ttu-id="0e6d7-152">**:n**: 英数字に一致を設定します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-152">**:n**: Sets the match to alphanumeric characters.</span></span> <span data-ttu-id="0e6d7-153">例</span><span class="sxs-lookup"><span data-stu-id="0e6d7-153">Examples:</span></span>

    + <span data-ttu-id="0e6d7-154">**照合("ab:ncd","ab%cd");** は、**0** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-154">**match("ab:ncd","ab%cd");** returns **0**.</span></span> 
    + <span data-ttu-id="0e6d7-155">**照合("ab:ncd","ab9cd");** は、**1** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-155">**match("ab:ncd","ab9cd");** returns **1**.</span></span> 
    + <span data-ttu-id="0e6d7-156">**照合("ab:ncd","abXcd");** は、**1** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-156">**match("ab:ncd","abXcd");** returns **1**.</span></span> 

+ <span data-ttu-id="0e6d7-157">**:SPACE**: SPACE は、空白文字 ( ) です。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-157">**:SPACE**: SPACE is the space character (" ").</span></span> <span data-ttu-id="0e6d7-158">空白、タブ、および Enter (改行文字) などの制御文字を入力するには、一致を設定します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-158">Sets the match to blanks, tabulations, and control characters such as Enter (new line).</span></span> <span data-ttu-id="0e6d7-159">例</span><span class="sxs-lookup"><span data-stu-id="0e6d7-159">Examples:</span></span>

    + <span data-ttu-id="0e6d7-160">**照合("ab: cd","ab cd");** は、**1** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-160">**match("ab: cd","ab cd");** returns **1**.</span></span> 
    + <span data-ttu-id="0e6d7-161">**照合("ab: cd","ab\ncd");** は、**1** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-161">**match("ab: cd","ab\ncd");** returns **1**.</span></span> 
    + <span data-ttu-id="0e6d7-162">**照合("ab: cd","ab\tcd");** は、**1** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-162">**match("ab: cd","ab\tcd");** returns **1**.</span></span> 
    + <span data-ttu-id="0e6d7-163">**照合("ab: cd","ab&nbsp;&nbsp;cd");** は、**0** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-163">**match("ab: cd","ab&nbsp;&nbsp;cd");** returns **0**.</span></span> <span data-ttu-id="0e6d7-164">最初のスペースのみ一致します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-164">Only the first space is matched.</span></span> 

+ <span data-ttu-id="0e6d7-165">\**\** _: アスタリスク (「\_」) の後に続く式には、前の式に 0、1、またはそれ以上の一致が必要です。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-165">\**\** _: An expression that is followed by an asterisk ("\_") requires a match for zero, one, or more occurrences of the preceding expression.</span></span> <span data-ttu-id="0e6d7-166">例</span><span class="sxs-lookup"><span data-stu-id="0e6d7-166">Examples:</span></span>

    + <span data-ttu-id="0e6d7-167">**照合("abc\*d","abd");**  は、**1** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-167">**match("abc\*d","abd");** returns **1**.</span></span> 
    + <span data-ttu-id="0e6d7-168">**照合("abc\*d","abcd");** は、**1** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-168">**match("abc\*d","abcd");** returns **1**.</span></span> 
    + <span data-ttu-id="0e6d7-169">**照合("abc\*d","abcccd");** は、**1** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-169">**match("abc\*d","abcccd");** returns **1**.</span></span> 
    + <span data-ttu-id="0e6d7-170">**照合("abc\*d","abxd");** は、**0** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-170">**match("abc\*d","abxd");** returns **0**.</span></span> 

+ <span data-ttu-id="0e6d7-171">**\+**: アスタリスクおよびプラス記号 ("**\+**) の後に続く式には、前の式に 1、またはそれ以上の一致が必要です。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-171">**\+**: An expression that is followed by a plus sign (**\+**) requires a match for one or more occurrences of the preceding expression.</span></span> <span data-ttu-id="0e6d7-172">例</span><span class="sxs-lookup"><span data-stu-id="0e6d7-172">Examples:</span></span>

    + <span data-ttu-id="0e6d7-173">**照合("abc+d","abd");** は、**0** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-173">**match("abc+d","abd");** returns **0**.</span></span> 
    + <span data-ttu-id="0e6d7-174">**照合("abc+d","abcd");** は、**1** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-174">**match("abc+d","abcd");** returns **1**</span></span> 
    + <span data-ttu-id="0e6d7-175">**照合("abc+d","abcccd");** は、**1** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-175">**match("abc+d","abcccd");** returns **1**.</span></span> 
    + <span data-ttu-id="0e6d7-176">**照合("abc+d","abxd");** は、**0** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-176">**match("abc+d","abxd");** returns **0**.</span></span> 

+ <span data-ttu-id="0e6d7-177">**\-** アスタリスクおよびマイナス記号 (**\-**) の後に続く式には、前の式に 0 または 1 を一致させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-177">**\-**: An expression that is followed by a minus sign (**\-**) requires a match for zero or one occurrence of the preceding expression.</span></span> <span data-ttu-id="0e6d7-178">つまり、前の式はオプションです。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-178">In other words, the preceding expression is optional.</span></span> <span data-ttu-id="0e6d7-179">例</span><span class="sxs-lookup"><span data-stu-id="0e6d7-179">Examples:</span></span>

    + <span data-ttu-id="0e6d7-180">**照合("colou-r","color");** は、**1** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-180">**match("colou-r","color");** returns **1**.</span></span> 
    + <span data-ttu-id="0e6d7-181">**照合("colou-r","colour");** は、**1** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-181">**match("colou-r","colour");** returns **1**.</span></span> 

+ <span data-ttu-id="0e6d7-182">**[]**: かっこで囲まれた任意の文字と 1 つの文字を照合します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-182">**[]**: Matches a single character with any character that is enclosed in the brackets.</span></span> <span data-ttu-id="0e6d7-183">文字の範囲は、マイナス記号 (**-**) で区切られた 2 つの文字で指定することができます。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-183">A range of characters can be specified by two characters that are separated by a minus sign (**-**).</span></span> <span data-ttu-id="0e6d7-184">たとえば、**[a-z]** は a ～ z のすべての文字に一致し、**[0-9]** は数字と一致し、さらに **[0-9a-f]** は 16 進数に一致します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-184">For example, **[a-z]** matches all letters between a and z, **[0-9]** matches a digit, and **[0-9a-f]** matches a hexadecimal digit.</span></span> <span data-ttu-id="0e6d7-185">例</span><span class="sxs-lookup"><span data-stu-id="0e6d7-185">Examples:</span></span>

    + <span data-ttu-id="0e6d7-186">**照合("[abc]","apple");** は、"apple." の a が一致するので **1** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-186">**match("[abc]","apple");** returns **1**, because it matches the a in "apple."</span></span> 
    + <span data-ttu-id="0e6d7-187">**照合("[abc]","kiwi");** は、"kiwi" に a、b、または c が含まれていないため、**0** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-187">**match("[abc]","kiwi");** returns **0**, because "kiwi" doesn't contain an a, b, or c.</span></span> 
    + <span data-ttu-id="0e6d7-188">**照合("gr[ae]y","grey");** は、1 を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-188">**match("gr[ae]y","grey");** returns 1.</span></span> <span data-ttu-id="0e6d7-189">この式は、”gray.” と一致します</span><span class="sxs-lookup"><span data-stu-id="0e6d7-189">This expression also matches "gray."</span></span> 
    + <span data-ttu-id="0e6d7-190">**照合("gr[ae]y","graey");** は、 "gr" and "y" の間で、1 つの文字だけが一致したため、**0** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-190">**match("gr[ae]y","graey");** returns **0**, because only one character between "gr" and "y" is matched.</span></span> 

+ <span data-ttu-id="0e6d7-191">**[^]**: かっこで囲まれたテキスト内で最初の文字が曲折記号 (**^**) の場合は、かっこで囲まれた文字を除き、式はすべての文字と一致します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-191">**[^]**: If the first character in the text that is enclosed in brackets is a circumflex (**^**), the expression matches all characters except the characters that are enclosed in the brackets.</span></span> <span data-ttu-id="0e6d7-192">例</span><span class="sxs-lookup"><span data-stu-id="0e6d7-192">Examples:</span></span>

    + <span data-ttu-id="0e6d7-193">**照合("[^bc]at","bat");** は、**0** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-193">**match("[^bc]at","bat");** returns **0**.</span></span> 
    + <span data-ttu-id="0e6d7-194">**照合("[^bc]at","hat");** は、**1** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-194">**match("[^bc]at","hat");** returns **1**.</span></span> 
    + <span data-ttu-id="0e6d7-195">**照合("[^abc]","bat");** は、**1** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-195">**match("[^abc]","bat");** returns **1**.</span></span> <span data-ttu-id="0e6d7-196">a、b、または c 以外は一致します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-196">Anything except a, b, or c is matched.</span></span> <span data-ttu-id="0e6d7-197">したがって、t が一致します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-197">Therefore, the t is matched.</span></span> 

## <a name="stralpha"></a><span data-ttu-id="0e6d7-198">strAlpha</span><span class="sxs-lookup"><span data-stu-id="0e6d7-198">strAlpha</span></span>
<span data-ttu-id="0e6d7-199">文字列の英数字のみをコピーします。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-199">Copies only the alphanumeric characters from a string.</span></span>

```xpp
str strAlpha(str _text)
```

### <a name="parameters"></a><span data-ttu-id="0e6d7-200">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-200">Parameters</span></span>

| <span data-ttu-id="0e6d7-201">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-201">Parameter</span></span> | <span data-ttu-id="0e6d7-202">説明</span><span class="sxs-lookup"><span data-stu-id="0e6d7-202">Description</span></span>              |
|-----------|--------------------------|
| <span data-ttu-id="0e6d7-203">\_テキスト</span><span class="sxs-lookup"><span data-stu-id="0e6d7-203">\_text</span></span>    | <span data-ttu-id="0e6d7-204">コピー元の文字列。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-204">The string to copy from.</span></span> |

### <a name="return-value"></a><span data-ttu-id="0e6d7-205">戻り値</span><span class="sxs-lookup"><span data-stu-id="0e6d7-205">Return value</span></span>

<span data-ttu-id="0e6d7-206">指定した文字列からのすべての英数字を含む新しい文字列。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-206">A new string that contains all the alphanumeric characters from the specified string.</span></span>

### <a name="remarks"></a><span data-ttu-id="0e6d7-207">備考</span><span class="sxs-lookup"><span data-stu-id="0e6d7-207">Remarks</span></span>

<span data-ttu-id="0e6d7-208">たとえば、**strAlpha(「2+2=5 これで正しいですか」)** は文字列 **225isthiscorrect** を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-208">For example, **strAlpha("2+2=5 is this correct?")** returns the string **225isthiscorrect**.</span></span>

### <a name="example"></a><span data-ttu-id="0e6d7-209">例</span><span class="sxs-lookup"><span data-stu-id="0e6d7-209">Example</span></span>

```xpp
static void strAlphaExample(Args _arg)
{
    str s;
    ;
    s = strAlpha("?a*bc123.");
    print s;
    pause;
}
```

## <a name="strcmp"></a><span data-ttu-id="0e6d7-210">strCmp</span><span class="sxs-lookup"><span data-stu-id="0e6d7-210">strCmp</span></span>
<span data-ttu-id="0e6d7-211">2 つの文字列を比較します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-211">Compares two text strings.</span></span>

```xpp
int strCmp(str text1, str text2)
```

### <a name="parameters"></a><span data-ttu-id="0e6d7-212">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-212">Parameters</span></span>

| <span data-ttu-id="0e6d7-213">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-213">Parameter</span></span> | <span data-ttu-id="0e6d7-214">説明</span><span class="sxs-lookup"><span data-stu-id="0e6d7-214">Description</span></span>        |
|-----------|--------------------|
| <span data-ttu-id="0e6d7-215">text1</span><span class="sxs-lookup"><span data-stu-id="0e6d7-215">text1</span></span>     | <span data-ttu-id="0e6d7-216">最初の文字列。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-216">The first string.</span></span>  |
| <span data-ttu-id="0e6d7-217">text2</span><span class="sxs-lookup"><span data-stu-id="0e6d7-217">text2</span></span>     | <span data-ttu-id="0e6d7-218">2 番目の文字列。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-218">The second string.</span></span> |

### <a name="return-value"></a><span data-ttu-id="0e6d7-219">戻り値</span><span class="sxs-lookup"><span data-stu-id="0e6d7-219">Return value</span></span>

<span data-ttu-id="0e6d7-220">2 つの文字列が同じ場合は **0**、最初の文字列が以前に並べ替えられている場合は **1**、2 つ目の文字列が以前に並べ替えられている場合は **-1** です。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-220">**0** if the two strings are identical, **1** if the first string sorts earlier, or **-1** if the second string sorts earlier.</span></span>

### <a name="remarks"></a><span data-ttu-id="0e6d7-221">備考</span><span class="sxs-lookup"><span data-stu-id="0e6d7-221">Remarks</span></span>

<span data-ttu-id="0e6d7-222">このメソッドで実行される比較では、大文字と小文字が区別されます。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-222">The comparison performed by this method is case-sensitive.</span></span>

```xpp
print strCmp("abc", "abc"); //Returns the value 0.
print strCmp("abc", "ABC"); //Returns the value 1.
print strCmp("aaa", "bbb"); //Returns the value -1.
print strCmp("ccc", "bbb"); //Returns the value 1.
```

## <a name="strcolseq"></a><span data-ttu-id="0e6d7-223">strColSeq</span><span class="sxs-lookup"><span data-stu-id="0e6d7-223">strColSeq</span></span>
<span data-ttu-id="0e6d7-224">すべての大文字を小文字に変換し、アクセントのあるすべての文字を、対応するアクセントのない小文字に変換します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-224">Converts all uppercase characters to lowercase characters, and converts all characters that have accents to the corresponding unaccented lowercase characters.</span></span>

```xpp
str strColSeq(str text)
```

### <a name="parameters"></a><span data-ttu-id="0e6d7-225">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-225">Parameters</span></span>

| <span data-ttu-id="0e6d7-226">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-226">Parameter</span></span> | <span data-ttu-id="0e6d7-227">説明</span><span class="sxs-lookup"><span data-stu-id="0e6d7-227">Description</span></span>                                     |
|-----------|-------------------------------------------------|
| <span data-ttu-id="0e6d7-228">テキスト</span><span class="sxs-lookup"><span data-stu-id="0e6d7-228">text</span></span>      | <span data-ttu-id="0e6d7-229">文字をコピーして変換する文字列。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-229">The string to copy and convert characters from.</span></span> |

### <a name="return-value"></a><span data-ttu-id="0e6d7-230">戻り値</span><span class="sxs-lookup"><span data-stu-id="0e6d7-230">Return value</span></span>

<span data-ttu-id="0e6d7-231">変換されたテキスト文字列。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-231">The converted text string.</span></span>

### <a name="remarks"></a><span data-ttu-id="0e6d7-232">備考</span><span class="sxs-lookup"><span data-stu-id="0e6d7-232">Remarks</span></span>

<span data-ttu-id="0e6d7-233">**strColSeq** 関数は、下位互換性のために存在します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-233">The **strColSeq** function exists for backward-compatibility purposes.</span></span> <span data-ttu-id="0e6d7-234">この関数は、次の西ヨーロッパの文字のマッピングのみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-234">This function supports only the mapping for the following Western European characters:</span></span>

-   <span data-ttu-id="0e6d7-235">AàáâãäÀÁÂÃÄBCçÇDEèéêëÈÉÊËFGHIìíîïÌÍÎÏJKLMNñÑOòóôõöÒÓÔÕÖPQRSTUùúûüÙÚÛÜVWXYýÝZæøåÆØÅ</span><span class="sxs-lookup"><span data-stu-id="0e6d7-235">AàáâãäÀÁÂÃÄBCçÇDEèéêëÈÉÊËFGHIìíîïÌÍÎÏJKLMNñÑOòóôõöÒÓÔÕÖPQRSTUùúûüÙÚÛÜVWXYýÝZæøåÆØÅ</span></span>
-   <span data-ttu-id="0e6d7-236">aaaaaaaaaaabcccdeeeeeeeeefghiiiiiiiiijklmnnnooooooooooopqrstuuuuuuuuuvwxyyyz~¦Ç~¦Ç</span><span class="sxs-lookup"><span data-stu-id="0e6d7-236">aaaaaaaaaaabcccdeeeeeeeeefghiiiiiiiiijklmnnnooooooooooopqrstuuuuuuuuuvwxyyyz~¦Ç~¦Ç</span></span>

<span data-ttu-id="0e6d7-237">Unicode 互換機能は、**DLL** および **DLLFunc** クラスを通じて Win32 LCMapString アプリケーション プログラミング インターフェイス (API) を使用します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-237">For Unicode-compliant functionality, use the Win32 LCMapString application programming interface (API) via the **DLL** and **DLLFunc** classes.</span></span>

### <a name="example"></a><span data-ttu-id="0e6d7-238">例</span><span class="sxs-lookup"><span data-stu-id="0e6d7-238">Example</span></span>

<span data-ttu-id="0e6d7-239">次の例では、**abcdeabcde** を出力します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-239">The following example prints **abcdeabcde**.</span></span>

```xpp
    static void strColSeqExample(Args _arg)
    {
            ;
            print strColSeq("");
            pause;
    }
```

## <a name="strdel"></a><span data-ttu-id="0e6d7-240">strDel</span><span class="sxs-lookup"><span data-stu-id="0e6d7-240">strDel</span></span>
<span data-ttu-id="0e6d7-241">指定されたサブ文字列が削除された文字列のコピーを作成します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-241">Creates a copy of a string, from which the specified substring is removed.</span></span>

```xpp
str strDel(str _text, int _position, int _number)
```

### <a name="parameters"></a><span data-ttu-id="0e6d7-242">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-242">Parameters</span></span>

| <span data-ttu-id="0e6d7-243">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-243">Parameter</span></span>  | <span data-ttu-id="0e6d7-244">説明</span><span class="sxs-lookup"><span data-stu-id="0e6d7-244">Description</span></span>                                                                                                                                                                                                                      |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e6d7-245">\_テキスト</span><span class="sxs-lookup"><span data-stu-id="0e6d7-245">\_text</span></span>     | <span data-ttu-id="0e6d7-246">コピー元の文字列。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-246">The string to copy from.</span></span>                                                                                                                                                                                                         |
| <span data-ttu-id="0e6d7-247">\_職位</span><span class="sxs-lookup"><span data-stu-id="0e6d7-247">\_position</span></span> | <span data-ttu-id="0e6d7-248">コピー操作時に文字の無視を開始する位置。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-248">The position at which to begin ignoring characters during the copy operation.</span></span>                                                                                                                                                    |
| <span data-ttu-id="0e6d7-249">\_数値</span><span class="sxs-lookup"><span data-stu-id="0e6d7-249">\_number</span></span>   | <span data-ttu-id="0e6d7-250">無視する文字数。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-250">The number of characters to ignore.</span></span> <span data-ttu-id="0e6d7-251">*\_番号* パラメーターの前のマイナス記号は、*\_位置* にある文字の前の *\_番号*–1 文字が *\_位置* にある文字と一緒に削除される必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-251">A minus sign in front of the *\_number* parameter indicates that *\_number*–1 characters before the character at *\_position* should be removed together with the character at *\_position*.</span></span> |

### <a name="return-value"></a><span data-ttu-id="0e6d7-252">戻り値</span><span class="sxs-lookup"><span data-stu-id="0e6d7-252">Return value</span></span>

<span data-ttu-id="0e6d7-253">文字列からコピーされる残りの文字。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-253">The remaining characters that are copied from the string.</span></span>

### <a name="remarks"></a><span data-ttu-id="0e6d7-254">備考</span><span class="sxs-lookup"><span data-stu-id="0e6d7-254">Remarks</span></span>

<span data-ttu-id="0e6d7-255">**strDel** 関数は、**substr** 関数を補完します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-255">The **strDel** function is complementary to the **substr** function.</span></span>

```xpp
strDel("ABCDEFGH",2,3); //Returns the string "AEFGH".
strDel("ABCDEFGH",4,3); //Returns the string "ABCGH".
```

## <a name="strfind"></a><span data-ttu-id="0e6d7-256">strFind</span><span class="sxs-lookup"><span data-stu-id="0e6d7-256">strFind</span></span>
<span data-ttu-id="0e6d7-257">指定された文字のいずれかの 1 番目の文字列を検索します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-257">Searches a string for the first occurrence of one of the specified characters.</span></span>

```xpp
int strFind(str _text, str _characters, int _position, int _number)
```

### <a name="parameters"></a><span data-ttu-id="0e6d7-258">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-258">Parameters</span></span>

| <span data-ttu-id="0e6d7-259">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-259">Parameter</span></span>    | <span data-ttu-id="0e6d7-260">説明</span><span class="sxs-lookup"><span data-stu-id="0e6d7-260">Description</span></span>                                                                                                |
|--------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e6d7-261">\_テキスト</span><span class="sxs-lookup"><span data-stu-id="0e6d7-261">\_text</span></span>       | <span data-ttu-id="0e6d7-262">検索する文字列。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-262">The string to search.</span></span>                                                                                      |
| <span data-ttu-id="0e6d7-263">\_文字</span><span class="sxs-lookup"><span data-stu-id="0e6d7-263">\_characters</span></span> | <span data-ttu-id="0e6d7-264">検索する文字。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-264">The characters to search for.</span></span>                                                                              |
| <span data-ttu-id="0e6d7-265">\_職位</span><span class="sxs-lookup"><span data-stu-id="0e6d7-265">\_position</span></span>   | <span data-ttu-id="0e6d7-266">検索を開始する文字列内の位置。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-266">The position in the string where the search begins.</span></span>                                                        |
| <span data-ttu-id="0e6d7-267">\_数値</span><span class="sxs-lookup"><span data-stu-id="0e6d7-267">\_number</span></span>     | <span data-ttu-id="0e6d7-268">検索の方向と文字列内で検索する位置の数を示す符号付き番号。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-268">A signed number that indicates the direction of the search and how many positions to search in the string.</span></span> |

### <a name="return-value"></a><span data-ttu-id="0e6d7-269">戻り値</span><span class="sxs-lookup"><span data-stu-id="0e6d7-269">Return value</span></span>

<span data-ttu-id="0e6d7-270">指定された文字の 1 つが最初に現れる位置の値、また見つからない場合は 0。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-270">The value of the position of the first occurrence of one of the specified characters, or 0 when none found.</span></span>

### <a name="remarks"></a><span data-ttu-id="0e6d7-271">備考</span><span class="sxs-lookup"><span data-stu-id="0e6d7-271">Remarks</span></span>

<span data-ttu-id="0e6d7-272">文字列の先頭から最後まで検索するには、*\_位置* パラメーターの値として **1** を使用します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-272">To search from the beginning of the string to the end, use **1** as the value of the *\_position* parameter.</span></span> <span data-ttu-id="0e6d7-273">*\_番号* パラメーターの値がマイナスである場合、システムは指定された位置から後方に文字数を検索します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-273">If the value of the *\_number* parameter is negative, the system searches the number of characters backward from the specified position.</span></span> <span data-ttu-id="0e6d7-274">検索では大文字と小文字が区別されません。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-274">The search isn't case-sensitive.</span></span> <span data-ttu-id="0e6d7-275">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-275">Here is an example.</span></span>

```xpp
strFind("ABCDEFGHIJ","KHD",1,10); //Returns the value 4 (the position where "D" was found).
strFind("ABCDEFGHIJ","KHD",10,-10); //Returns the value 8 (the position where "H" was found).
```

<span data-ttu-id="0e6d7-276">**strFind** 関数は、**strNFind** 関数を補完します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-276">The **strFind** function is complementary to the **strNFind** function.</span></span>

## <a name="strfmt"></a><span data-ttu-id="0e6d7-277">strFmt</span><span class="sxs-lookup"><span data-stu-id="0e6d7-277">strFmt</span></span>
<span data-ttu-id="0e6d7-278">指定された文字列を書式設定し、すべての n を n 番目の引数に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-278">Formats the specified string and substitutes any occurrences of n with the nth argument.</span></span>

```xpp
str strFmt(str _string, ...)
```

### <a name="parameters"></a><span data-ttu-id="0e6d7-279">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-279">Parameters</span></span>

| <span data-ttu-id="0e6d7-280">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-280">Parameter</span></span> | <span data-ttu-id="0e6d7-281">説明</span><span class="sxs-lookup"><span data-stu-id="0e6d7-281">Description</span></span>            |
|-----------|------------------------|
| <span data-ttu-id="0e6d7-282">\_文字列</span><span class="sxs-lookup"><span data-stu-id="0e6d7-282">\_string</span></span>  | <span data-ttu-id="0e6d7-283">フォーマットする文字列。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-283">The strings to format.</span></span> |

### <a name="return-value"></a><span data-ttu-id="0e6d7-284">戻り値</span><span class="sxs-lookup"><span data-stu-id="0e6d7-284">Return value</span></span>

<span data-ttu-id="0e6d7-285">書式設定された文字列。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-285">The formatted string.</span></span>

### <a name="remarks"></a><span data-ttu-id="0e6d7-286">備考</span><span class="sxs-lookup"><span data-stu-id="0e6d7-286">Remarks</span></span>

<span data-ttu-id="0e6d7-287">パラメーターに引数が指定されない場合は、文字列内では "%n" として返されます。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-287">If an argument isn't provided for a parameter, the parameter will be returned as "%n" in the string.</span></span> <span data-ttu-id="0e6d7-288">**実数** 型の値の文字列変換では、小数点第 2 位に制限されます。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-288">The string conversion of values of the **real** type is limited to two decimal places.</span></span> <span data-ttu-id="0e6d7-289">値は丸められ、切り捨てられません。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-289">Values are rounded, not truncated.</span></span> <span data-ttu-id="0e6d7-290">Microsoft .NET Framework の **System.String::Format** メソッドは、例に示すように、追加機能を取得するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-290">The **System.String::Format** method from the Microsoft .NET Framework can be used to gain additional functionality, as shown in the example.</span></span>

### <a name="example"></a><span data-ttu-id="0e6d7-291">例</span><span class="sxs-lookup"><span data-stu-id="0e6d7-291">Example</span></span>

```xpp
static void strFmtExampleJob(Args _arg)
{
    System.Double sysDouble;
    real r = 8.3456789;
    int  i = 42;
    utcDateTime utc = str2DateTime("2008-01-16 13:44:55" ,321); // 321 == YMD.
    str  s;
    ;
    s = strFmt("real = %1, int = %2, utcDateTime = %3, [%4]", r, i, utc);
    info("X1:  " + s);
    //
    sysDouble = r;
    s = System.String::Format("{0:##.####}", sysDouble);
    info("N1:  " + s);
    //
    s = System.String::Format("{0,6:C}", sysDouble); // $
    info("N2:  " + s);
    /**********  Actual Infolog output
    Message (02:16:05 pm)
    X1:  real = 8.35, int = 42, utcDateTime = 1/16/2008 01:44:55 pm, [%4]
    N1:  8.3457
    N2:   $8.35
    **********/
}
```

## <a name="strins"></a><span data-ttu-id="0e6d7-292">strIns</span><span class="sxs-lookup"><span data-stu-id="0e6d7-292">strIns</span></span>
<span data-ttu-id="0e6d7-293">1 つの文字列を別の文字列に挿入して文字列を作成します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-293">Builds a string by inserting one string into another.</span></span>

```xpp
str strIns(str _text1, str _text2, int _position)
```

### <a name="parameters"></a><span data-ttu-id="0e6d7-294">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-294">Parameters</span></span>

| <span data-ttu-id="0e6d7-295">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-295">Parameter</span></span>  | <span data-ttu-id="0e6d7-296">説明</span><span class="sxs-lookup"><span data-stu-id="0e6d7-296">Description</span></span>                                                                                          |
|------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e6d7-297">\_text1</span><span class="sxs-lookup"><span data-stu-id="0e6d7-297">\_text1</span></span>    | <span data-ttu-id="0e6d7-298">他の文字列を挿入する文字列。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-298">The string to insert the other string into.</span></span>                                                          |
| <span data-ttu-id="0e6d7-299">\_text2</span><span class="sxs-lookup"><span data-stu-id="0e6d7-299">\_text2</span></span>    | <span data-ttu-id="0e6d7-300">他の文字列に挿入する文字列。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-300">The string to insert into the other string.</span></span>                                                          |
| <span data-ttu-id="0e6d7-301">\_職位</span><span class="sxs-lookup"><span data-stu-id="0e6d7-301">\_position</span></span> | <span data-ttu-id="0e6d7-302">出力文字列内への *\_text2* パラメーターの最初の文字の配置位置。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-302">The position where the first character of the *\_text2* parameter should occur in the output string.</span></span> |

### <a name="return-value"></a><span data-ttu-id="0e6d7-303">戻り値</span><span class="sxs-lookup"><span data-stu-id="0e6d7-303">Return value</span></span>

<span data-ttu-id="0e6d7-304">結合された。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-304">The combined text string.</span></span>

### <a name="remarks"></a><span data-ttu-id="0e6d7-305">備考</span><span class="sxs-lookup"><span data-stu-id="0e6d7-305">Remarks</span></span>

<span data-ttu-id="0e6d7-306">**strIns** 関数は、**strDel** 関数を補完します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-306">The **strIns** function is complementary to the **strDel** function.</span></span> <span data-ttu-id="0e6d7-307">*\_位置* パラメーターの値が元の文字列より長くなる場合、挿入する文字列が元の文字列の末尾に追加されます。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-307">If the value of the *\_position* parameter is more than the length of the original string, the string to insert is appended to the end of the original string.</span></span>

```xpp
strIns("ABFGH","CDE",3); //Returns the string "ABCDEFGH".
strIns("ABCD","EFGH",10); //Returns the string "ABCDEFGH".
```

## <a name="strkeep"></a><span data-ttu-id="0e6d7-308">strKeep</span><span class="sxs-lookup"><span data-stu-id="0e6d7-308">strKeep</span></span>
<span data-ttu-id="0e6d7-309">2 番目の入力文字列で指定する最初の入力文字列の文字のみを使用して文字列を作成します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-309">Builds a string by using only the characters from the first input string that the second input string specifies should be kept.</span></span>

```xpp
str strKeep(str _text1, str _text2)
```

### <a name="parameters"></a><span data-ttu-id="0e6d7-310">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-310">Parameters</span></span>

| <span data-ttu-id="0e6d7-311">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-311">Parameter</span></span> | <span data-ttu-id="0e6d7-312">説明</span><span class="sxs-lookup"><span data-stu-id="0e6d7-312">Description</span></span>                                                                         |
|-----------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0e6d7-313">\_text1</span><span class="sxs-lookup"><span data-stu-id="0e6d7-313">\_text1</span></span>   | <span data-ttu-id="0e6d7-314">出力文字列を作成するために使用できる文字を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-314">The string that contains the characters that can be used to build an output string.</span></span> |
| <span data-ttu-id="0e6d7-315">\_text2</span><span class="sxs-lookup"><span data-stu-id="0e6d7-315">\_text2</span></span>   | <span data-ttu-id="0e6d7-316">出力文字列に保持する文字を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-316">The string that specifies which characters to keep for the output string.</span></span>           |

### <a name="return-value"></a><span data-ttu-id="0e6d7-317">戻り値</span><span class="sxs-lookup"><span data-stu-id="0e6d7-317">Return value</span></span>

<span data-ttu-id="0e6d7-318">保存されている文字の文字列。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-318">A string of the characters that are kept.</span></span>

### <a name="remarks"></a><span data-ttu-id="0e6d7-319">備考</span><span class="sxs-lookup"><span data-stu-id="0e6d7-319">Remarks</span></span>

```xpp
strKeep("ABBCDDEFGHB","BCD"); //Returns the string "BBCDDB".
strKeep("abcZcba","bc") //Returns the string "bccb".
```

<span data-ttu-id="0e6d7-320">**strKeep** 関数は、**strRem** 関数を補完します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-320">The **strKeep** function is complementary to the **strRem** function.</span></span>

## <a name="strlen"></a><span data-ttu-id="0e6d7-321">strLen</span><span class="sxs-lookup"><span data-stu-id="0e6d7-321">strLen</span></span>
<span data-ttu-id="0e6d7-322">指定した文字列の長さを計算します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-322">Calculates the length of the specified string.</span></span>

```xpp
int strLen(str text)
```

### <a name="parameters"></a><span data-ttu-id="0e6d7-323">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-323">Parameters</span></span>

| <span data-ttu-id="0e6d7-324">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-324">Parameter</span></span> | <span data-ttu-id="0e6d7-325">説明</span><span class="sxs-lookup"><span data-stu-id="0e6d7-325">Description</span></span>                            |
|-----------|----------------------------------------|
| <span data-ttu-id="0e6d7-326">テキスト</span><span class="sxs-lookup"><span data-stu-id="0e6d7-326">text</span></span>      | <span data-ttu-id="0e6d7-327">長さを計算する文字列。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-327">The string to calculate the length of.</span></span> |

### <a name="return-value"></a><span data-ttu-id="0e6d7-328">戻り値</span><span class="sxs-lookup"><span data-stu-id="0e6d7-328">Return value</span></span>

<span data-ttu-id="0e6d7-329">指定した文字列の長さ。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-329">The length of the specified string.</span></span>

### <a name="remarks"></a><span data-ttu-id="0e6d7-330">備考</span><span class="sxs-lookup"><span data-stu-id="0e6d7-330">Remarks</span></span>

```xpp
strLen("ABC"); //Returns the value 3.
strLen("ABCDEFGHIJ"); //Returns the value 10.
```

## <a name="strline"></a><span data-ttu-id="0e6d7-331">strLine</span><span class="sxs-lookup"><span data-stu-id="0e6d7-331">strLine</span></span>
<span data-ttu-id="0e6d7-332">複数の行にまたがる文字列から 1 つの行を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-332">Retrieves a single line from a string that spans multiple lines.</span></span>

```xpp
str strLine(str string, int count)
```

### <a name="parameters"></a><span data-ttu-id="0e6d7-333">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-333">Parameters</span></span>

| <span data-ttu-id="0e6d7-334">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-334">Parameter</span></span> | <span data-ttu-id="0e6d7-335">説明</span><span class="sxs-lookup"><span data-stu-id="0e6d7-335">Description</span></span>                              |
|-----------|------------------------------------------|
| <span data-ttu-id="0e6d7-336">string</span><span class="sxs-lookup"><span data-stu-id="0e6d7-336">string</span></span>    | <span data-ttu-id="0e6d7-337">複数の明細行にまたがる文字列。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-337">A string that might span multiple lines.</span></span> |
| <span data-ttu-id="0e6d7-338">カウント</span><span class="sxs-lookup"><span data-stu-id="0e6d7-338">count</span></span>     | <span data-ttu-id="0e6d7-339">返す線のオフセット。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-339">The offset of the line to return.</span></span>        |

### <a name="return-value"></a><span data-ttu-id="0e6d7-340">戻り値</span><span class="sxs-lookup"><span data-stu-id="0e6d7-340">Return value</span></span>

<span data-ttu-id="0e6d7-341">*文字列* パラメーターで指定された文字列のコピーされた明細行です。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-341">A copied line of the string that is specified by the *string* parameter.</span></span>

### <a name="remarks"></a><span data-ttu-id="0e6d7-342">備考</span><span class="sxs-lookup"><span data-stu-id="0e6d7-342">Remarks</span></span>

<span data-ttu-id="0e6d7-343">文字列の最初の行には 0 のオフセットがあります。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-343">The first line of the string has an offset of 0.</span></span> <span data-ttu-id="0e6d7-344">文字列に *\n* または *\r\n* 文字を埋め込むことにより、複数行を1 つの文字列に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-344">You can assign multiple lines to one string by embedding the *\n* or *\r\n* characters in the string.</span></span> <span data-ttu-id="0e6d7-345">また、開始引用符の直前にアット マーク (@) を使用することができ、Enter キーを使用して文字列値の一部を X++ コード エディタの複数の行に分散させることができます。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-345">Additionally, you can use the at sign (@) immediately before the opening quotation mark and use the Enter key to spread parts of the string value over multiple lines in the X++ code editor.</span></span>

### <a name="example"></a><span data-ttu-id="0e6d7-346">例</span><span class="sxs-lookup"><span data-stu-id="0e6d7-346">Example</span></span>

```xpp
str mytxt = "first-line\nsecond-line\nlast-line";
// Prints "second-line".
print strLine(mytxt,1);
// Prints "last-line".
print strLine(mytxt,2);            
```

## <a name="strltrim"></a><span data-ttu-id="0e6d7-347">strLTrim</span><span class="sxs-lookup"><span data-stu-id="0e6d7-347">strLTrim</span></span>
<span data-ttu-id="0e6d7-348">テキスト文字列から先行する空白を削除します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-348">Removes leading blanks from a text string.</span></span>

```xpp
str strLTrim(str text)
```

### <a name="parameters"></a><span data-ttu-id="0e6d7-349">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-349">Parameters</span></span>

| <span data-ttu-id="0e6d7-350">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-350">Parameter</span></span> | <span data-ttu-id="0e6d7-351">説明</span><span class="sxs-lookup"><span data-stu-id="0e6d7-351">Description</span></span>                                   |
|-----------|-----------------------------------------------|
| <span data-ttu-id="0e6d7-352">テキスト</span><span class="sxs-lookup"><span data-stu-id="0e6d7-352">text</span></span>      | <span data-ttu-id="0e6d7-353">先頭の空白を削除する文字列。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-353">The string to delete the leading blanks from.</span></span> |

### <a name="return-value"></a><span data-ttu-id="0e6d7-354">戻り値</span><span class="sxs-lookup"><span data-stu-id="0e6d7-354">Return value</span></span>

<span data-ttu-id="0e6d7-355">先頭の空白が削除されたテキストに相当する文字列。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-355">The string equivalent for the text that leading blanks have been removed from.</span></span>

### <a name="remarks"></a><span data-ttu-id="0e6d7-356">備考</span><span class="sxs-lookup"><span data-stu-id="0e6d7-356">Remarks</span></span>

<span data-ttu-id="0e6d7-357">**strLTrim** 関数は、**strRTrim** 関数を補完します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-357">The **strLTrim** function is complementary to the **strRTrim** function.</span></span>

### <a name="example"></a><span data-ttu-id="0e6d7-358">例</span><span class="sxs-lookup"><span data-stu-id="0e6d7-358">Example</span></span>

```xpp
// Returns the text string "ABC-DEFG".
strLTrim("   ABC-DEFG");
```

## <a name="strlwr"></a><span data-ttu-id="0e6d7-359">strLwr</span><span class="sxs-lookup"><span data-stu-id="0e6d7-359">strLwr</span></span>
<span data-ttu-id="0e6d7-360">指定された文字列のすべての文字を小文字に変換します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-360">Converts all letters in the specified string to lowercase.</span></span>

```xpp
str strLwr(str _text)
```

### <a name="parameters"></a><span data-ttu-id="0e6d7-361">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-361">Parameters</span></span>

| <span data-ttu-id="0e6d7-362">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-362">Parameter</span></span> | <span data-ttu-id="0e6d7-363">説明</span><span class="sxs-lookup"><span data-stu-id="0e6d7-363">Description</span></span>                         |
|-----------|-------------------------------------|
| <span data-ttu-id="0e6d7-364">\_テキスト</span><span class="sxs-lookup"><span data-stu-id="0e6d7-364">\_text</span></span>    | <span data-ttu-id="0e6d7-365">小文字に変換する文字列。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-365">The string to convert to lowercase.</span></span> |

### <a name="return-value"></a><span data-ttu-id="0e6d7-366">戻り値</span><span class="sxs-lookup"><span data-stu-id="0e6d7-366">Return value</span></span>

<span data-ttu-id="0e6d7-367">小文字のみを含んでいる指定された文字列のコピーです。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-367">A copy of the specified string that contains only lowercase letter.</span></span>

### <a name="remarks"></a><span data-ttu-id="0e6d7-368">備考</span><span class="sxs-lookup"><span data-stu-id="0e6d7-368">Remarks</span></span>

<span data-ttu-id="0e6d7-369">**strLwr** 関数は、**strUpr** 関数を補完します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-369">The **strLwr** function is complementary to the **strUpr** function.</span></span> <span data-ttu-id="0e6d7-370">**strLwr** 関数は、Win32 API で **LCMapString** 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-370">The **strLwr** function uses the **LCMapString** function in the Win32 API.</span></span>

### <a name="example"></a><span data-ttu-id="0e6d7-371">例</span><span class="sxs-lookup"><span data-stu-id="0e6d7-371">Example</span></span>

```xpp
static void strLwrExample(Args _args)
{
    // Returns the text string "abcdd55efghij".
    print strLwr("Abcdd55EFGHIJ");
    pause;
}
```
## <a name="strnfind"></a><span data-ttu-id="0e6d7-372">strNFind</span><span class="sxs-lookup"><span data-stu-id="0e6d7-372">strNFind</span></span>
<span data-ttu-id="0e6d7-373">指定した文字リストに含まれていない文字の 1 番目の文字列の一部を検索します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-373">Searches part of a text string for the first occurrence of a character that isn't included in the specified list of characters.</span></span>

```xpp
int strNFind(str _text, str _characters, int _position, int _number)
```

### <a name="parameters"></a><span data-ttu-id="0e6d7-374">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-374">Parameters</span></span>

| <span data-ttu-id="0e6d7-375">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-375">Parameter</span></span>    | <span data-ttu-id="0e6d7-376">説明</span><span class="sxs-lookup"><span data-stu-id="0e6d7-376">Description</span></span>                                                                                                                                                                                                     |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e6d7-377">\_テキスト</span><span class="sxs-lookup"><span data-stu-id="0e6d7-377">\_text</span></span>       | <span data-ttu-id="0e6d7-378">検索するテキスト文字列。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-378">The text string to search.</span></span>                                                                                                                                                                                      |
| <span data-ttu-id="0e6d7-379">\_文字</span><span class="sxs-lookup"><span data-stu-id="0e6d7-379">\_characters</span></span> | <span data-ttu-id="0e6d7-380">検索から除外する文字のリスト。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-380">The list of characters to exclude from the search.</span></span>                                                                                                                                                              |
| <span data-ttu-id="0e6d7-381">\_職位</span><span class="sxs-lookup"><span data-stu-id="0e6d7-381">\_position</span></span>   | <span data-ttu-id="0e6d7-382">検索を開始する文字列内の位置。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-382">The position in the string at which to begin the search.</span></span>                                                                                                                                                        |
| <span data-ttu-id="0e6d7-383">\_数値</span><span class="sxs-lookup"><span data-stu-id="0e6d7-383">\_number</span></span>     | <span data-ttu-id="0e6d7-384">検索の方向と検索する位置の数を示す符号付き番号。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-384">A signed number that indicates the direction of the search and how many positions to search.</span></span> <span data-ttu-id="0e6d7-385">マイナス記号が *\_番号* に先行する場合、システムでは *\_位置* の逆順で *\_番号* 文字が検索されます。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-385">If a minus sign precedes *\_number*, the system searches *\_number* characters in reverse order from *\_position*.</span></span> |

### <a name="return-value"></a><span data-ttu-id="0e6d7-386">戻り値</span><span class="sxs-lookup"><span data-stu-id="0e6d7-386">Return value</span></span>

<span data-ttu-id="0e6d7-387">*\_characters* パラメーターによって指定されていない文字の 1 番目の位置、また見つからない場合は 0。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-387">The position of the first occurrence of a character that isn't specified by the *\_characters* parameter, or 0 when none found.</span></span>

### <a name="remarks"></a><span data-ttu-id="0e6d7-388">備考</span><span class="sxs-lookup"><span data-stu-id="0e6d7-388">Remarks</span></span>

<span data-ttu-id="0e6d7-389">検索では大文字と小文字が区別されません。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-389">The search isn't case-sensitive.</span></span> <span data-ttu-id="0e6d7-390">文字列の先頭から最後まで検索するには、*\_位置* パラメーターの値として **1** を使用します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-390">To search from the beginning of the string to the end, use a value of **1** for the *\_position* parameter.</span></span> <span data-ttu-id="0e6d7-391">マイナス記号が *\_番号* パラメーターの前にある場合、*\_位置* パラメーターで指定された位置から逆の順序で文字が検索されます。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-391">If a minus sign precedes the value of the *\_number* parameter, the characters will be searched in reverse order, starting from the position that is specified by the *\_position* parameter.</span></span>

```xpp
strNFind("ABCDEFGHIJ","ABCDHIJ",1,10); //Returns the value 5 (the position of "E");
strNFind("CDEFGHIJ","CDEFGIJ",10,-10); //Returns the value 6 (the position of "H").
strNFind("abcdef","abCdef",3,2) //Returns the value 0.
strNFind("abcdef", "abcef",3,2) //Returns the value 4.
```

<span data-ttu-id="0e6d7-392">**strNFind** 関数は、**strFind** 関数を補完します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-392">The **strNFind** function is complementary to the **strFind** function.</span></span>

## <a name="strpoke"></a><span data-ttu-id="0e6d7-393">strPoke</span><span class="sxs-lookup"><span data-stu-id="0e6d7-393">strPoke</span></span>
<span data-ttu-id="0e6d7-394">別の文字列で文字列の一部を上書きします。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-394">Overwrites part of a string with another string.</span></span>

```xpp
str strPoke(str _text1, str _text2, int _position)
```

### <a name="parameters"></a><span data-ttu-id="0e6d7-395">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-395">Parameters</span></span>

| <span data-ttu-id="0e6d7-396">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-396">Parameter</span></span>  | <span data-ttu-id="0e6d7-397">説明</span><span class="sxs-lookup"><span data-stu-id="0e6d7-397">Description</span></span>                                                                     |
|------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="0e6d7-398">\_text1</span><span class="sxs-lookup"><span data-stu-id="0e6d7-398">\_text1</span></span>    | <span data-ttu-id="0e6d7-399">元の文字列。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-399">The original string.</span></span>                                                            |
| <span data-ttu-id="0e6d7-400">\_text2</span><span class="sxs-lookup"><span data-stu-id="0e6d7-400">\_text2</span></span>    | <span data-ttu-id="0e6d7-401">元の文字列の一部を置き換える文字列。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-401">The string to replace part of the original string with.</span></span>                         |
| <span data-ttu-id="0e6d7-402">\_職位</span><span class="sxs-lookup"><span data-stu-id="0e6d7-402">\_position</span></span> | <span data-ttu-id="0e6d7-403">文字の置き換えを開始する元の文字列の位置。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-403">The position of the original string at which to begin replacing the characters.</span></span> |

### <a name="return-value"></a><span data-ttu-id="0e6d7-404">戻り値</span><span class="sxs-lookup"><span data-stu-id="0e6d7-404">Return value</span></span>

<span data-ttu-id="0e6d7-405">新しい文字列。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-405">The new string.</span></span>

### <a name="remarks"></a><span data-ttu-id="0e6d7-406">備考</span><span class="sxs-lookup"><span data-stu-id="0e6d7-406">Remarks</span></span>

<span data-ttu-id="0e6d7-407">新しい文字列は、元の文字列より長くすることができます。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-407">The new string can be longer than the original string.</span></span> <span data-ttu-id="0e6d7-408">ただし、*\_位置* パラメーターの値がを文字列の長さを超える場合、元の文字列が置換なしで返されます。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-408">However, if the value of the *\_position* parameter is more than the length of the string, the original string is returned without replacements.</span></span>

```xpp
strPoke("12345678","AAA",3); //Returns the string "12AAA678".
strPoke("abcde","4567",4); //Returns the string "abc4567".
strPoke("abcde", "4567", "10"); //Returns the string "abcde".
```

## <a name="strprompt"></a><span data-ttu-id="0e6d7-409">strPrompt</span><span class="sxs-lookup"><span data-stu-id="0e6d7-409">strPrompt</span></span>
<span data-ttu-id="0e6d7-410">指定されたピリオド文字数の後に、コロンと空白文字が続く文字列を追加します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-410">Appends a string with the specified number of period characters, followed by a colon and space character.</span></span>

```xpp
str strPrompt(str _string, _int len)
```

### <a name="parameters"></a><span data-ttu-id="0e6d7-411">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-411">Parameters</span></span>

| <span data-ttu-id="0e6d7-412">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-412">Parameter</span></span> | <span data-ttu-id="0e6d7-413">説明</span><span class="sxs-lookup"><span data-stu-id="0e6d7-413">Description</span></span>                             |
|-----------|-----------------------------------------|
| <span data-ttu-id="0e6d7-414">\_文字列</span><span class="sxs-lookup"><span data-stu-id="0e6d7-414">\_string</span></span>  | <span data-ttu-id="0e6d7-415">元の文字列。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-415">The original string.</span></span>                    |
| <span data-ttu-id="0e6d7-416">\_len</span><span class="sxs-lookup"><span data-stu-id="0e6d7-416">\_len</span></span>     | <span data-ttu-id="0e6d7-417">文字列の最終的な長さ。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-417">The desired final length of the string.</span></span> |

### <a name="return-value"></a><span data-ttu-id="0e6d7-418">戻り値</span><span class="sxs-lookup"><span data-stu-id="0e6d7-418">Return value</span></span>

<span data-ttu-id="0e6d7-419">ユーザー入力のプロンプトのように見える文字列。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-419">A string that looks like a prompt for user input.</span></span>

### <a name="remarks"></a><span data-ttu-id="0e6d7-420">備考</span><span class="sxs-lookup"><span data-stu-id="0e6d7-420">Remarks</span></span>

<span data-ttu-id="0e6d7-421">特別な場合では、*\_len* パラメーターの値が元の文字列の長さより少し大きい場合のみ、末尾へのスペース追加に最も高い優先順位が付与されます。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-421">In atypical cases, where the value of the *\_len* parameter is only slightly more than the length of the original string, the highest precedence is given to adding the trailing space.</span></span> <span data-ttu-id="0e6d7-422">次に、優先順位がコロンに指定されます。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-422">Next, precedence is given to the colon.</span></span> <span data-ttu-id="0e6d7-423">期間には、最下位の優先順位が付けられます。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-423">The lowest precedence is given to the periods.</span></span> <span data-ttu-id="0e6d7-424">*\_len* パラメーターの負の値は、後ろにスペースを付けた入力文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-424">Negative values for the *\_len* parameter return the input string appended with a trailing space.</span></span>

```xpp
strPrompt("ab",-1); //Returns "ab ".
strPrompt("ab",3); //Returns "ab ".
strPrompt("ab",4); //Returns "ab: ".
strPrompt("ab",5); //Returns "ab.: ".
strPrompt("ab",6); //Returns "ab..: ".
```

### <a name="example"></a><span data-ttu-id="0e6d7-425">例</span><span class="sxs-lookup"><span data-stu-id="0e6d7-425">Example</span></span>

```xpp
static void JobStrPromptDemo(Args _args)
{
    // Printed string is "[abc..: ]"
    print "[", strPrompt("abc", 7), "]";
    pause;
}
```

## <a name="strrem"></a><span data-ttu-id="0e6d7-426">strRem</span><span class="sxs-lookup"><span data-stu-id="0e6d7-426">strRem</span></span>
<span data-ttu-id="0e6d7-427">別の文字列から 1 つの文字列で指定されている文字を削除します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-427">Removes the characters that are specified in one string from another string.</span></span>

```xpp
str strRem(str text1, str text2)
```

### <a name="parameters"></a><span data-ttu-id="0e6d7-428">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-428">Parameters</span></span>

| <span data-ttu-id="0e6d7-429">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-429">Parameter</span></span> | <span data-ttu-id="0e6d7-430">説明</span><span class="sxs-lookup"><span data-stu-id="0e6d7-430">Description</span></span>                                       |
|-----------|---------------------------------------------------|
| <span data-ttu-id="0e6d7-431">text1</span><span class="sxs-lookup"><span data-stu-id="0e6d7-431">text1</span></span>     | <span data-ttu-id="0e6d7-432">文字を削除する文字列。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-432">The string to remove characters from.</span></span>             |
| <span data-ttu-id="0e6d7-433">text2</span><span class="sxs-lookup"><span data-stu-id="0e6d7-433">text2</span></span>     | <span data-ttu-id="0e6d7-434">出力文字列から除外する文字。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-434">The characters to exclude from the output string.</span></span> |

### <a name="return-value"></a><span data-ttu-id="0e6d7-435">戻り値</span><span class="sxs-lookup"><span data-stu-id="0e6d7-435">Return value</span></span>

<span data-ttu-id="0e6d7-436">元の文字列の残りのコンテンツ。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-436">The remaining content of the original string.</span></span>

### <a name="remarks"></a><span data-ttu-id="0e6d7-437">備考</span><span class="sxs-lookup"><span data-stu-id="0e6d7-437">Remarks</span></span>

<span data-ttu-id="0e6d7-438">この関数は、大文字小文字を区別します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-438">This function is case-sensitive.</span></span>

```xpp
strRem("abcd_abcd","Bc"); //Returns the string "abd_abd".
strRem("ABCDEFGABCDEFG","ACEG"); //Returns the string "BDFBDF".
```

<span data-ttu-id="0e6d7-439"> この関数は、**strKeep** 関数を補完します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-439">This function is complementary to the **strKeep** function.</span></span>

## <a name="strrep"></a><span data-ttu-id="0e6d7-440">strRep</span><span class="sxs-lookup"><span data-stu-id="0e6d7-440">strRep</span></span>
<span data-ttu-id="0e6d7-441">文字の文字列を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-441">Repeats a string of characters.</span></span>

```xpp
str strRep(str _text, str _number)
```

### <a name="parameters"></a><span data-ttu-id="0e6d7-442">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-442">Parameters</span></span>

| <span data-ttu-id="0e6d7-443">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-443">Parameter</span></span> | <span data-ttu-id="0e6d7-444">説明</span><span class="sxs-lookup"><span data-stu-id="0e6d7-444">Description</span></span>                               |
|-----------|-------------------------------------------|
| <span data-ttu-id="0e6d7-445">\_テキスト</span><span class="sxs-lookup"><span data-stu-id="0e6d7-445">\_text</span></span>    | <span data-ttu-id="0e6d7-446">クエリ返す文字列。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-446">The string to repeat.</span></span>                     |
| <span data-ttu-id="0e6d7-447">\_数値</span><span class="sxs-lookup"><span data-stu-id="0e6d7-447">\_number</span></span>  | <span data-ttu-id="0e6d7-448">文字列を繰り返す回数。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-448">The number of times to repeat the string.</span></span> |

### <a name="return-value"></a><span data-ttu-id="0e6d7-449">戻り値</span><span class="sxs-lookup"><span data-stu-id="0e6d7-449">Return value</span></span>

<span data-ttu-id="0e6d7-450">指定された回数が繰り返される元の文字列の内容を含む新しい文字列。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-450">A new string that contains the contents of the original string that are repeated the specified number of times.</span></span>

### <a name="example"></a><span data-ttu-id="0e6d7-451">例</span><span class="sxs-lookup"><span data-stu-id="0e6d7-451">Example</span></span>

<span data-ttu-id="0e6d7-452">次の例では、テキスト文字列 **ABABABABABAB** を出力します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-452">The following example prints the text string **ABABABABABAB**.</span></span>

```xpp
static void strRepExample(Args _arg)
{
    str strL;
    ;
    strL = strRep("AB",6);
    print strL;
    pause;
}
```

## <a name="strrtrim"></a><span data-ttu-id="0e6d7-453">strRTrim</span><span class="sxs-lookup"><span data-stu-id="0e6d7-453">strRTrim</span></span>
<span data-ttu-id="0e6d7-454">文字列の末尾から空白文字を削除します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-454">Removes the trailing space characters from the end of a string.</span></span>

```xpp
str strRTrim(str _text)
```

### <a name="parameters"></a><span data-ttu-id="0e6d7-455">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-455">Parameters</span></span>

| <span data-ttu-id="0e6d7-456">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-456">Parameter</span></span> | <span data-ttu-id="0e6d7-457">説明</span><span class="sxs-lookup"><span data-stu-id="0e6d7-457">Description</span></span>                                               |
|-----------|-----------------------------------------------------------|
| <span data-ttu-id="0e6d7-458">\_テキスト</span><span class="sxs-lookup"><span data-stu-id="0e6d7-458">\_text</span></span>    | <span data-ttu-id="0e6d7-459">末尾の空白文字を削除する文字列。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-459">The string to remove the trailing space characters from .</span></span> |

### <a name="return-value"></a><span data-ttu-id="0e6d7-460">戻り値</span><span class="sxs-lookup"><span data-stu-id="0e6d7-460">Return value</span></span>

<span data-ttu-id="0e6d7-461">末尾に空白文字が含まれていない指定の文字列のコピーです。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-461">A copy of the specified string that doesn't include trailing space characters.</span></span>

### <a name="remarks"></a><span data-ttu-id="0e6d7-462">備考</span><span class="sxs-lookup"><span data-stu-id="0e6d7-462">Remarks</span></span>

```xpp
strRTrim("ABC-DEFG- "); //Returns the string "ABC-DEFG-".
strRTrim(" CD "); //Returns " CD".
```

<span data-ttu-id="0e6d7-463">**strRTrim** 関数は、**strLTrim** 関数を補完します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-463">The **strRTrim** function is complementary to the **strLTrim** function.</span></span>

## <a name="strscan"></a><span data-ttu-id="0e6d7-464">strScan</span><span class="sxs-lookup"><span data-stu-id="0e6d7-464">strScan</span></span>
<span data-ttu-id="0e6d7-465">別の文字列と一致する文字列を検索します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-465">Searches a text string for an occurrence of another string.</span></span>

```xpp
int strScan(str _text1, str _text2, int _position, int _number)
```

### <a name="parameters"></a><span data-ttu-id="0e6d7-466">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-466">Parameters</span></span>

| <span data-ttu-id="0e6d7-467">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-467">Parameter</span></span>  | <span data-ttu-id="0e6d7-468">説明</span><span class="sxs-lookup"><span data-stu-id="0e6d7-468">Description</span></span>                                                                                                                                                                                                                   |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e6d7-469">\_text1</span><span class="sxs-lookup"><span data-stu-id="0e6d7-469">\_text1</span></span>    | <span data-ttu-id="0e6d7-470">検索する文字列。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-470">The string to search in.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="0e6d7-471">\_text2</span><span class="sxs-lookup"><span data-stu-id="0e6d7-471">\_text2</span></span>    | <span data-ttu-id="0e6d7-472">検索する文字列。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-472">The string to find.</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="0e6d7-473">\_職位</span><span class="sxs-lookup"><span data-stu-id="0e6d7-473">\_position</span></span> | <span data-ttu-id="0e6d7-474">比較を実行する *\_text1* パラメーターの最初の位置。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-474">The first position in the *\_text1* parameter at which to perform a comparison.</span></span>                                                                                                                                               |
| <span data-ttu-id="0e6d7-475">\_数値</span><span class="sxs-lookup"><span data-stu-id="0e6d7-475">\_number</span></span>   | <span data-ttu-id="0e6d7-476">比較を再試行する *\_text1* パラメーター内の位置の数。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-476">The number of positions in the *\_text1* parameter to retry the comparison for.</span></span> <span data-ttu-id="0e6d7-477">マイナス記号が *\_番号* パラメーターに先行する場合、システムでは特定位置の逆順で文字数が検索されます。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-477">If a minus sign precedes the *\_number* parameter, the system searches the number of characters in reverse order from the specified position.</span></span> |

### <a name="return-value"></a><span data-ttu-id="0e6d7-478">戻り値</span><span class="sxs-lookup"><span data-stu-id="0e6d7-478">Return value</span></span>

<span data-ttu-id="0e6d7-479">文字列内で指定した文字列が見つかった位置。それ以外の場合は **0** (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-479">The position at which the specified string was found in the string; otherwise, **0** (zero).</span></span>

### <a name="remarks"></a><span data-ttu-id="0e6d7-480">備考</span><span class="sxs-lookup"><span data-stu-id="0e6d7-480">Remarks</span></span>

<span data-ttu-id="0e6d7-481">この比較では大文字と小文字は区別されません。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-481">The comparisons aren't case-sensitive.</span></span> <span data-ttu-id="0e6d7-482">*\_位置* パラメーターが **1** 未満の値は **1** として扱われます。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-482">Values for the *\_position* parameter that are less than **1** are treated as **1**.</span></span> <span data-ttu-id="0e6d7-483">スキャンの方向は、*\_number* パラメーターで指定されている符号で制御されます。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-483">The direction of the scan is controlled by the sign that is specified in the *\_number* parameter.</span></span> <span data-ttu-id="0e6d7-484">プラス記号は、連続する各比較が文字列の末尾に 1 つ近い位置から開始することを示します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-484">A positive sign indicates that each successive comparison will start one position closer to the end of the string.</span></span> <span data-ttu-id="0e6d7-485">マイナス記号は、各比較が文字列の先頭に 1 つ近い位置から開始することを示します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-485">A negative sign indicates that each comparison will start one position closer to the start of the string.</span></span>

```xpp
strScan("ABCDEFGHIJ","DEF",1,10); //Returns the value 4.
strScan ("ABCDEFGHIJ","CDE",10,-10); //Returns the value 3.
```

## <a name="strupr"></a><span data-ttu-id="0e6d7-486">strUpr</span><span class="sxs-lookup"><span data-stu-id="0e6d7-486">strUpr</span></span>
<span data-ttu-id="0e6d7-487">文字列内のすべての文字を大文字に変換します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-487">Converts all the letters in a string to uppercase.</span></span>

```xpp
str strUpr(str _text)
```

### <a name="parameters"></a><span data-ttu-id="0e6d7-488">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-488">Parameters</span></span>

| <span data-ttu-id="0e6d7-489">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-489">Parameter</span></span> | <span data-ttu-id="0e6d7-490">説明</span><span class="sxs-lookup"><span data-stu-id="0e6d7-490">Description</span></span>                                 |
|-----------|---------------------------------------------|
| <span data-ttu-id="0e6d7-491">\_テキスト</span><span class="sxs-lookup"><span data-stu-id="0e6d7-491">\_text</span></span>    | <span data-ttu-id="0e6d7-492">大文字に変換する文字列。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-492">The string to convert to uppercase letters.</span></span> |

### <a name="return-value"></a><span data-ttu-id="0e6d7-493">戻り値</span><span class="sxs-lookup"><span data-stu-id="0e6d7-493">Return value</span></span>

<span data-ttu-id="0e6d7-494">小文字のみを含んでいる指定された文字列のコピーです。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-494">A copy of the specified string that contains only lowercase letters.</span></span>

### <a name="remarks"></a><span data-ttu-id="0e6d7-495">備考</span><span class="sxs-lookup"><span data-stu-id="0e6d7-495">Remarks</span></span>

<span data-ttu-id="0e6d7-496">**strUpr** 関数は、**strLwr** 関数を補完します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-496">The **strUpr** function is complementary to the **strLwr** function.</span></span> <span data-ttu-id="0e6d7-497">**strUpr** 関数は、Win32 API で **LCMapString()** 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-497">The **strUpr** function uses the **LCMapString()** function in the Win32 API.</span></span>

### <a name="example"></a><span data-ttu-id="0e6d7-498">例</span><span class="sxs-lookup"><span data-stu-id="0e6d7-498">Example</span></span>

<span data-ttu-id="0e6d7-499">次の例は **ABCDD55EFGHIJ** を出力します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-499">The following example will print **ABCDD55EFGHIJ**.</span></span>

```xpp
static void strUprExample(Args _args)
{
    print strUpr("Abcdd55EFGhiJ");
    pause;
}
```

## <a name="substr"></a><span data-ttu-id="0e6d7-500">subStr</span><span class="sxs-lookup"><span data-stu-id="0e6d7-500">subStr</span></span>
<span data-ttu-id="0e6d7-501">文字列の一部を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-501">Retrieves part of a string.</span></span>

```xpp
str subStr(str _text, int _position, int _number)
```

### <a name="parameters"></a><span data-ttu-id="0e6d7-502">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-502">Parameters</span></span>

| <span data-ttu-id="0e6d7-503">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e6d7-503">Parameter</span></span>  | <span data-ttu-id="0e6d7-504">説明</span><span class="sxs-lookup"><span data-stu-id="0e6d7-504">Description</span></span>                                                                                                                                                                                                             |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e6d7-505">\_テキスト</span><span class="sxs-lookup"><span data-stu-id="0e6d7-505">\_text</span></span>     | <span data-ttu-id="0e6d7-506">元の文字列。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-506">The original string.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="0e6d7-507">\_職位</span><span class="sxs-lookup"><span data-stu-id="0e6d7-507">\_position</span></span> | <span data-ttu-id="0e6d7-508">取得する部分が開始する元の文字列内の位置。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-508">The position in the original string where the part to retrieve begins.</span></span>                                                                                                                                                  |
| <span data-ttu-id="0e6d7-509">\_数値</span><span class="sxs-lookup"><span data-stu-id="0e6d7-509">\_number</span></span>   | <span data-ttu-id="0e6d7-510">元の文字列から取得する位置の方向と数を示す符号付き整数。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-510">A signed integer that indicates the direction and number of positions to retrieve from the original string.</span></span> <span data-ttu-id="0e6d7-511">マイナス記号が *\_番号* に先行する場合、システムでは指定された位置から後方に部分文字列を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-511">If a minus sign precedes *\_number*, the system selects the substring backward from the specified position.</span></span> |

### <a name="return-value"></a><span data-ttu-id="0e6d7-512">戻り値</span><span class="sxs-lookup"><span data-stu-id="0e6d7-512">Return value</span></span>

<span data-ttu-id="0e6d7-513">元の文字列のサブ文字列。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-513">A substring of the original string.</span></span>

### <a name="remarks"></a><span data-ttu-id="0e6d7-514">備考</span><span class="sxs-lookup"><span data-stu-id="0e6d7-514">Remarks</span></span>

<span data-ttu-id="0e6d7-515">マイナス記号が *\_番号* パラメーターの値より前にある場合、指定された位置から後方に部分文字列を選択します。</span><span class="sxs-lookup"><span data-stu-id="0e6d7-515">If a minus sign precedes the value of the *\_number* parameter, the substring will be selected backward from the specified position.</span></span>

```xpp
subStr("ABCDEFGHIJ",3,5); //Returns the string "CDEFG".
subStr("ABCDEFGHIJ",7,-4); //Returns the string "DEFG".
subStr("abcdef"),2,99) //Returns the string "cdef".
subStr("abcdef",2,3) //Returns the string "bcd".
subStr("abcdef",2,-3); //Returns the string "ab".
```




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
