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
# <a name="class-xlanguage"></a>クラス xLanguage

[!include [banner](../../includes/banner.md)]

```xpp
class xLanguage extends Object
```

xLanguage クラスは、言語 ID のリストと既存のラベル ファイルに関する情報へのアクセスを提供します。

## <a name="remarks"></a>備考

ISO 639 は、英語の "en" などの言語の名前を定義します。 Microsoft は、英語 (米国) の場合は「en-us」といった一連の言語コードをリストしました。 これらの言語コードは、言語 ID として参照されます。 韓国語 (Johab) の「ko-jo」が使用されます。 Microsoft のリストで、「ko」は韓国語と韓国語 (Johab) の両方です。 ノルウェー語 (ニーノシュク) の「no-ny」が使用されます。 Microsoft のリストで、「no」はノルウェー語 (ブークモール) とノルウェー語 (ニーノシク) の両方です。 スペイン語 (スペイン - トラディショナル ソート) を表す「es-tr」が使用されます。 Microsoft のリストで、「es」はスペイン語 (スペイン - モダン ソート) とスペイン語 (スペイン - トラディショナル ソート) の両方です。 「英語 (米国)」など、次の形式での言語名は、説明として参照されます。

## <a name="examples"></a>例

次の例では、すべての言語 ID を Microsoft のリストと既存のラベル ファイルのリストから出力します。

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

## <a name="methods"></a>方法

| 方法                                                     | 説明                                                                                                 |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| ::public static str index2languageID(int number)           | 指定された言語の言語 ID (たとえば、"en-us") を取得します。                                 |
| ::public static int labelFileCount()                       | ラベル ファイルの数を返します。                                                                          |
| ::public static str labelFileNumber2LanguageID(int number) |                                                                                                             |
| ::public static int languageCount()                        |                                                                                                             |
| ::public static str languageID2Description(str languageID) | 言語 ID が付与された、指定された言語 ("英語 (米国)" など) の名前を返されます。 |
| ::public static int languageID2LCID(str languageID)        |                                                                                                             |
| ::public static str lcid2languageID(int lcid)              |                                                                                                             |

## <a name="method-index2languageid"></a>メソッド index2languageID

指定された言語の言語 ID (たとえば、"en-us") を取得します。

```xpp
public static str index2languageID(int number)
```

### <a name="parameters---index2languageid"></a>パラメーター - index2languageID

番号  
1 と languageCount メソッドの戻り値の間での番号。

### <a name="return-value---index2languageid"></a>戻り値 - index2languageID

言語 ID。

## <a name="method-labelfilecount"></a>メソッド labelFileCount

ラベル ファイルの数を返します。

```xpp
public static int labelFileCount()
```

### <a name="return-value---labelfilecount"></a>戻り値 - labelFileCount

ラベル ファイルの数 (つまり、ax???\*.ald という形式の名前を持つファイルの数)。

## <a name="method-labelfilenumber2languageid"></a>メソッド labelFileNumber2LanguageID

```xpp
public static str labelFileNumber2LanguageID(int number)
```

### <a name="parameters---labelfilenumber2languageid"></a>パラメーター - labelFileNumber2LanguageID

番号  

### <a name="return-value---labelfilenumber2languageid"></a>戻り値 - labelFileNumber2LanguageID

## <a name="method-languagecount"></a>メソッド languageCount

```xpp
public static int languageCount()
```

### <a name="return-value---languagecount"></a>戻り値 - languageCount

## <a name="method-languageid2description"></a>メソッド languageID2Description

言語 ID が付与された、指定された言語 ("英語 (米国)" など) の名前を返されます。

```xpp
public static str languageID2Description(str languageID)
```

### <a name="parameters---languageid2description"></a>パラメーター - languageID2Description

languageID  
言語の ID (たとえば、"en-us")。

### <a name="return-value---languageid2description"></a>戻り値 - languageID2Description

言語の説明を含む文字列。

## <a name="method-languageid2lcid"></a>メソッド languageID2LCID

```xpp
public static int languageID2LCID(str languageID)
```

### <a name="parameters---languageid2lcid"></a>パラメーター - languageID2LCID

languageID  

### <a name="return-value---languageid2lcid"></a>戻り値 - languageID2LCID

## <a name="method-lcid2languageid"></a>メソッド lcid2languageID

```xpp
public static str lcid2languageID(int lcid)
```

### <a name="parameters---lcid2languageid"></a>パラメーター - lcid2languageID

lcid  

### <a name="return-value---lcid2languageid"></a>戻り値 - lcid2languageID

