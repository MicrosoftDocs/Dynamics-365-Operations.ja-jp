---
title: xLanguage クラス
description: このトピックでは、xLanguage クラスについて説明します。
author: robinarh
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce023506b5de3395942eb8c8cc8551b2c2e294c2
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502679"
---
# <a name="class-xlanguage"></a><span data-ttu-id="01390-103">クラス xLanguage</span><span class="sxs-lookup"><span data-stu-id="01390-103">Class xLanguage</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class xLanguage extends Object
```

<span data-ttu-id="01390-104">xLanguage クラスは、言語 ID のリストと既存のラベル ファイルに関する情報へのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="01390-104">The xLanguage class provides access to a list of language IDs and information about existing label files.</span></span>

## <a name="remarks"></a><span data-ttu-id="01390-105">備考</span><span class="sxs-lookup"><span data-stu-id="01390-105">Remarks</span></span>

<span data-ttu-id="01390-106">ISO 639 は、英語の "en" などの言語の名前を定義します。</span><span class="sxs-lookup"><span data-stu-id="01390-106">ISO 639 defines the names of languages, such as "en" for English.</span></span> <span data-ttu-id="01390-107">Microsoft は、英語 (米国) の場合は「en-us」といった一連の言語コードをリストしました。</span><span class="sxs-lookup"><span data-stu-id="01390-107">Microsoft has listed a set of language codes, such "en-us" for English (United States).</span></span> <span data-ttu-id="01390-108">これらの言語コードは、言語 ID として参照されます。</span><span class="sxs-lookup"><span data-stu-id="01390-108">These language codes are referred to as Language IDs.</span></span> <span data-ttu-id="01390-109">韓国語 (Johab) の「ko-jo」が使用されます。</span><span class="sxs-lookup"><span data-stu-id="01390-109">"ko-jo" is used for Korean (Johab).</span></span> <span data-ttu-id="01390-110">Microsoft のリストで、「ko」は韓国語と韓国語 (Johab) の両方です。</span><span class="sxs-lookup"><span data-stu-id="01390-110">In the Microsoft list, "ko" is both Korean and Korean (Johab).</span></span> <span data-ttu-id="01390-111">ノルウェー語 (ニーノシュク) の「no-ny」が使用されます。</span><span class="sxs-lookup"><span data-stu-id="01390-111">"no-ny" is used for for Norwegian (Nynorsk).</span></span> <span data-ttu-id="01390-112">Microsoft のリストで、「no」はノルウェー語 (ブークモール) とノルウェー語 (ニーノシク) の両方です。</span><span class="sxs-lookup"><span data-stu-id="01390-112">In the Microsoft list, "no" is both Norwegian (Bokmal) and Norwegian (Nynorsk).</span></span> <span data-ttu-id="01390-113">スペイン語 (スペイン - トラディショナル ソート) を表す「es-tr」が使用されます。</span><span class="sxs-lookup"><span data-stu-id="01390-113">"es-tr" is used to represent Spanish (Spain - Traditional Sort).</span></span> <span data-ttu-id="01390-114">Microsoft のリストで、「es」はスペイン語 (スペイン - モダン ソート) とスペイン語 (スペイン - トラディショナル ソート) の両方です。</span><span class="sxs-lookup"><span data-stu-id="01390-114">In the Microsoft list, "es" is both Spanish (Spain - Modern Sort) and Spanish (Spain - Traditional Sort).</span></span> <span data-ttu-id="01390-115">「英語 (米国)」など、次の形式での言語名は、説明として参照されます。</span><span class="sxs-lookup"><span data-stu-id="01390-115">A language name in the following format, such as "English (United States)", is referred to as the description.</span></span>

## <a name="examples"></a><span data-ttu-id="01390-116">例</span><span class="sxs-lookup"><span data-stu-id="01390-116">Examples</span></span>

<span data-ttu-id="01390-117">次の例では、すべての言語 ID を Microsoft のリストと既存のラベル ファイルのリストから出力します。</span><span class="sxs-lookup"><span data-stu-id="01390-117">The following example prints all the language IDs from the Microsoft list and a list of existing label files.</span></span>

```xpp
static void aaaTestLanguage(args a) 
{ 
    int i; 
    int cnt; 
    str languageID; 
    str description; 
    str shortName; 
    cnt = xlanguage::languageCount(); 
    for (i = 0; i<=cnt; i++) 
    { 
        languageID =xLanguage::index2languageID(i); 
        print "Language ", i, ":", languageID, ":"; 
    } 
    cnt = xLanguage::labelFileCount(); 
    for (i = 0; i<=cnt; i++) 
    { 
        shortName =xLanguage::labelFileNumber2LanguageID(i); 
        languageID =xLanguage::index2languageID(i); 
        description = xLanguage::languageID2Description(languageID); 
        print i, ":", shortName, ":", description; 
    } 
    pause; 
}
```

## <a name="methods"></a><span data-ttu-id="01390-118">方法</span><span class="sxs-lookup"><span data-stu-id="01390-118">Methods</span></span>

| <span data-ttu-id="01390-119">方法</span><span class="sxs-lookup"><span data-stu-id="01390-119">Method</span></span>                                                     | <span data-ttu-id="01390-120">説明</span><span class="sxs-lookup"><span data-stu-id="01390-120">Description</span></span>                                                                                                 |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01390-121">::public static str index2languageID(int number)</span><span class="sxs-lookup"><span data-stu-id="01390-121">::public static str index2languageID(int number)</span></span>           | <span data-ttu-id="01390-122">指定された言語の言語 ID (たとえば、"en-us") を取得します。</span><span class="sxs-lookup"><span data-stu-id="01390-122">Retrieves the language ID (for example, "en-us") of the specified language.</span></span>                                 |
| <span data-ttu-id="01390-123">::public static int labelFileCount()</span><span class="sxs-lookup"><span data-stu-id="01390-123">::public static int labelFileCount()</span></span>                       | <span data-ttu-id="01390-124">ラベル ファイルの数を返します。</span><span class="sxs-lookup"><span data-stu-id="01390-124">Returns the number of label files.</span></span>                                                                          |
| <span data-ttu-id="01390-125">::public static str labelFileNumber2LanguageID(int number)</span><span class="sxs-lookup"><span data-stu-id="01390-125">::public static str labelFileNumber2LanguageID(int number)</span></span> |                                                                                                             |
| <span data-ttu-id="01390-126">::public static int languageCount()</span><span class="sxs-lookup"><span data-stu-id="01390-126">::public static int languageCount()</span></span>                        |                                                                                                             |
| <span data-ttu-id="01390-127">::public static str languageID2Description(str languageID)</span><span class="sxs-lookup"><span data-stu-id="01390-127">::public static str languageID2Description(str languageID)</span></span> | <span data-ttu-id="01390-128">言語 ID が付与された、指定された言語 ("英語 (米国)" など) の名前を返されます。</span><span class="sxs-lookup"><span data-stu-id="01390-128">Returns the name of the specified language (for example, "English (United States)"), given the language ID.</span></span> |
| <span data-ttu-id="01390-129">::public static int languageID2LCID(str languageID)</span><span class="sxs-lookup"><span data-stu-id="01390-129">::public static int languageID2LCID(str languageID)</span></span>        |                                                                                                             |
| <span data-ttu-id="01390-130">::public static str lcid2languageID(int lcid)</span><span class="sxs-lookup"><span data-stu-id="01390-130">::public static str lcid2languageID(int lcid)</span></span>              |                                                                                                             |

## <a name="method-index2languageid"></a><span data-ttu-id="01390-131">メソッド index2languageID</span><span class="sxs-lookup"><span data-stu-id="01390-131">Method index2languageID</span></span>

<span data-ttu-id="01390-132">指定された言語の言語 ID (たとえば、"en-us") を取得します。</span><span class="sxs-lookup"><span data-stu-id="01390-132">Retrieves the language ID (for example, "en-us") of the specified language.</span></span>

```xpp
public static str index2languageID(int number)
```

### <a name="parameters---index2languageid"></a><span data-ttu-id="01390-133">パラメーター - index2languageID</span><span class="sxs-lookup"><span data-stu-id="01390-133">Parameters - index2languageID</span></span>

<span data-ttu-id="01390-134">番号</span><span class="sxs-lookup"><span data-stu-id="01390-134">number</span></span>  
<span data-ttu-id="01390-135">1 と languageCount メソッドの戻り値の間での番号。</span><span class="sxs-lookup"><span data-stu-id="01390-135">A number between 1 and the return value of the languageCount method.</span></span>

### <a name="return-value---index2languageid"></a><span data-ttu-id="01390-136">戻り値 - index2languageID</span><span class="sxs-lookup"><span data-stu-id="01390-136">Return Value - index2languageID</span></span>

<span data-ttu-id="01390-137">言語 ID。</span><span class="sxs-lookup"><span data-stu-id="01390-137">The language ID.</span></span>

## <a name="method-labelfilecount"></a><span data-ttu-id="01390-138">メソッド labelFileCount</span><span class="sxs-lookup"><span data-stu-id="01390-138">Method labelFileCount</span></span>

<span data-ttu-id="01390-139">ラベル ファイルの数を返します。</span><span class="sxs-lookup"><span data-stu-id="01390-139">Returns the number of label files.</span></span>

```xpp
public static int labelFileCount()
```

### <a name="return-value---labelfilecount"></a><span data-ttu-id="01390-140">戻り値 - labelFileCount</span><span class="sxs-lookup"><span data-stu-id="01390-140">Return Value - labelFileCount</span></span>

<span data-ttu-id="01390-141">ラベル ファイルの数 (つまり、ax???\*.ald という形式の名前を持つファイルの数)。</span><span class="sxs-lookup"><span data-stu-id="01390-141">The number of label files (that is, the number of files that have names in the form ax???\*.ald).</span></span>

## <a name="method-labelfilenumber2languageid"></a><span data-ttu-id="01390-142">メソッド labelFileNumber2LanguageID</span><span class="sxs-lookup"><span data-stu-id="01390-142">Method labelFileNumber2LanguageID</span></span>

```xpp
public static str labelFileNumber2LanguageID(int number)
```

### <a name="parameters---labelfilenumber2languageid"></a><span data-ttu-id="01390-143">パラメーター - labelFileNumber2LanguageID</span><span class="sxs-lookup"><span data-stu-id="01390-143">Parameters - labelFileNumber2LanguageID</span></span>

<span data-ttu-id="01390-144">番号</span><span class="sxs-lookup"><span data-stu-id="01390-144">number</span></span>  

### <a name="return-value---labelfilenumber2languageid"></a><span data-ttu-id="01390-145">戻り値 - labelFileNumber2LanguageID</span><span class="sxs-lookup"><span data-stu-id="01390-145">Return Value - labelFileNumber2LanguageID</span></span>

## <a name="method-languagecount"></a><span data-ttu-id="01390-146">メソッド languageCount</span><span class="sxs-lookup"><span data-stu-id="01390-146">Method languageCount</span></span>

```xpp
public static int languageCount()
```

### <a name="return-value---languagecount"></a><span data-ttu-id="01390-147">戻り値 - languageCount</span><span class="sxs-lookup"><span data-stu-id="01390-147">Return Value - languageCount</span></span>

## <a name="method-languageid2description"></a><span data-ttu-id="01390-148">メソッド languageID2Description</span><span class="sxs-lookup"><span data-stu-id="01390-148">Method languageID2Description</span></span>

<span data-ttu-id="01390-149">言語 ID が付与された、指定された言語 ("英語 (米国)" など) の名前を返されます。</span><span class="sxs-lookup"><span data-stu-id="01390-149">Returns the name of the specified language (for example, "English (United States)"), given the language ID.</span></span>

```xpp
public static str languageID2Description(str languageID)
```

### <a name="parameters---languageid2description"></a><span data-ttu-id="01390-150">パラメーター - languageID2Description</span><span class="sxs-lookup"><span data-stu-id="01390-150">Parameters - languageID2Description</span></span>

<span data-ttu-id="01390-151">languageID</span><span class="sxs-lookup"><span data-stu-id="01390-151">languageID</span></span>  
<span data-ttu-id="01390-152">言語の ID (たとえば、"en-us")。</span><span class="sxs-lookup"><span data-stu-id="01390-152">The ID of the language (for example, "en-us").</span></span>

### <a name="return-value---languageid2description"></a><span data-ttu-id="01390-153">戻り値 - languageID2Description</span><span class="sxs-lookup"><span data-stu-id="01390-153">Return Value - languageID2Description</span></span>

<span data-ttu-id="01390-154">言語の説明を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="01390-154">A string that contains the description of a language.</span></span>

## <a name="method-languageid2lcid"></a><span data-ttu-id="01390-155">メソッド languageID2LCID</span><span class="sxs-lookup"><span data-stu-id="01390-155">Method languageID2LCID</span></span>

```xpp
public static int languageID2LCID(str languageID)
```

### <a name="parameters---languageid2lcid"></a><span data-ttu-id="01390-156">パラメーター - languageID2LCID</span><span class="sxs-lookup"><span data-stu-id="01390-156">Parameters - languageID2LCID</span></span>

<span data-ttu-id="01390-157">languageID</span><span class="sxs-lookup"><span data-stu-id="01390-157">languageID</span></span>  

### <a name="return-value---languageid2lcid"></a><span data-ttu-id="01390-158">戻り値 - languageID2LCID</span><span class="sxs-lookup"><span data-stu-id="01390-158">Return Value - languageID2LCID</span></span>

## <a name="method-lcid2languageid"></a><span data-ttu-id="01390-159">メソッド lcid2languageID</span><span class="sxs-lookup"><span data-stu-id="01390-159">Method lcid2languageID</span></span>

```xpp
public static str lcid2languageID(int lcid)
```

### <a name="parameters---lcid2languageid"></a><span data-ttu-id="01390-160">パラメーター - lcid2languageID</span><span class="sxs-lookup"><span data-stu-id="01390-160">Parameters - lcid2languageID</span></span>

<span data-ttu-id="01390-161">lcid</span><span class="sxs-lookup"><span data-stu-id="01390-161">lcid</span></span>  

### <a name="return-value---lcid2languageid"></a><span data-ttu-id="01390-162">戻り値 - lcid2languageID</span><span class="sxs-lookup"><span data-stu-id="01390-162">Return Value - lcid2languageID</span></span>

