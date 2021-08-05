---
title: X++ 文字列ランタイム関数
description: このトピックでは、文字列ランタイム関数について説明します。
author: RobinARH
ms.date: 08/15/2019
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f8ed6d1d2c17f272b081f78f720b521aa4301ac9
ms.sourcegitcommit: ff5e892a91a1585472af2191ae45d6291cceb7f6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/24/2021
ms.locfileid: "6661344"
---
# <a name="x-string-runtime-functions"></a>X++ 文字列ランタイム関数

[!include [banner](../includes/banner.md)]

このトピックでは、文字列ランタイム関数について説明します。

## <a name="match"></a>照合

文字列や別の文字列内の式を検索します。

```xpp
int match(str pattern, str text)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                             |
|-----------|-----------------------------------------|
| pattern   | 検索する文字列または式。 |
| テキスト      | 検索する文字列。                   |

### <a name="return-value"></a>戻り値

パターンが文字列内にある場合は **1**、それ以外の場合は、**0** (ゼロ)。

### <a name="remarks"></a>備考

検索では大文字と小文字が区別されません。 次の特殊文字を使用して、*pattern* パラメーターのパターンを作成できます。

+ **\\** バックスラッシュ (**\\**) は、特殊文字の特別な扱いを無効にしたりエスケープしたりするため、特殊文字を通常の文字のように一致させることができます。 バックスラッシュのペアは、1 つの非特殊バックスラッシュに変換されます。 例

    + **照合("ab$cd","ab$cd");** は、**0** を返します。 
    + **照合("ab\\$cd","ab$cd");** は、**0** を返します。 バックスラッシュはエスケープされません。
    + **照合("ab\\\\$cd","ab$cd");** は、**1** を返します。 バックスラッシュとドル記号はエスケープされます。

+ **< または ^**: 式の先頭にある始め山かっこ (**<**) またはサーカムフレックス (**^**) は、明細行の始まりと照合するために使用します。 例

    + **照合("<abc","abcdef");** は、 **1** を返します。 
    + **照合("<abc","defabc");** は、**0** を返します。 
    + **照合("^abc","abcdef");** は、 **1** を返します。 
    + **照合("^abc","defabc");** は、**0** を返します。 

+ **> または $**: 式の最後の終わり山かっこ (**>**;) またはドル記号 (**$**) は、明細行の末尾と照合するために使用されます。 例

    + **照合("abc>","abcdef");** は、**0** を返します。 
    + **照合("abc>","defabc");** は、**1** を返します。 

+ **? または .**: 疑問符 (**?**) またはピリオド (**.**) は、同じ位置にある任意の 1 文字と一致します。 例

    + **照合("abc.def","abc#def");** は、**1** を返します。 
    + **照合("colou?r","colouXr");** は、**1** を返します。 

+ **:x**: コロン (**:**) は、直後の文字が示すように、一致する文字のグループを指定します。

+ **:a**: 文字に一致を設定します。 例

    + **照合("ab:acd","ab#cd");** は、**0** を返します。 
    + **照合("ab:acd","abxyzcd");** は、**0** を返します。 
    + **照合("ab:acd","abxcd");** は、**1** を返します。 

+ **:d**: 数字に一致を設定します。 例

    + **照合("ab:dcd","ab3cd");** は、**1** を返します。 
    + **照合("ab:dcd","ab123cd");** は、**0** を返します。 
    + **照合("ab:dcd","abcd");** は、**0** を返します。 

+ **:n**: 英数字に一致を設定します。 例

    + **照合("ab:ncd","ab%cd");** は、**0** を返します。 
    + **照合("ab:ncd","ab9cd");** は、**1** を返します。 
    + **照合("ab:ncd","abXcd");** は、**1** を返します。 

+ **:SPACE**: SPACE は、空白文字 ( ) です。 空白、タブ、および Enter (改行文字) などの制御文字を入力するには、一致を設定します。 例

    + **照合("ab: cd","ab cd");** は、**1** を返します。 
    + **照合("ab: cd","ab\ncd");** は、**1** を返します。 
    + **照合("ab: cd","ab\tcd");** は、**1** を返します。 
    + **照合("ab: cd","ab&nbsp;&nbsp;cd");** は、**0** を返します。 最初のスペースのみ一致します。 

+ **\** _: アスタリスク (「\_」) の後に続く式には、前の式に 0、1、またはそれ以上の一致が必要です。 例

    + **照合("abc\*d","abd");** は、**1** を返します。 
    + **照合("abc\*d","abcd");** は、**1** を返します。 
    + **照合("abc\*d","abcccd");** は、**1** を返します。 
    + **照合("abc\*d","abxd");** は、**0** を返します。 

+ **\+**: アスタリスクおよびプラス記号 ("**\+**) の後に続く式には、前の式に 1、またはそれ以上の一致が必要です。 例

    + **照合("abc+d","abd");** は、**0** を返します。 
    + **照合("abc+d","abcd");** は、**1** を返します。 
    + **照合("abc+d","abcccd");** は、**1** を返します。 
    + **照合("abc+d","abxd");** は、**0** を返します。 

+ **\-** アスタリスクおよびマイナス記号 (**\-**) の後に続く式には、前の式に 0 または 1 を一致させる必要があります。 つまり、前の式はオプションです。 例

    + **照合("colou-r","color");** は、**1** を返します。 
    + **照合("colou-r","colour");** は、**1** を返します。 

+ **[]**: かっこで囲まれた任意の文字と 1 つの文字を照合します。 文字の範囲は、マイナス記号 (**-**) で区切られた 2 つの文字で指定することができます。 たとえば、**[a-z]** は a ～ z のすべての文字に一致し、**[0-9]** は数字と一致し、さらに **[0-9a-f]** は 16 進数に一致します。 例

    + **照合("[abc]","apple");** は、"apple." の a が一致するので **1** を返します。 
    + **照合("[abc]","kiwi");** は、"kiwi" に a、b、または c が含まれていないため、**0** を返します。 
    + **照合("gr[ae]y","grey");** は、1 を返します。 この式は、”gray.” と一致します 
    + **照合("gr[ae]y","graey");** は、 "gr" and "y" の間で、1 つの文字だけが一致したため、**0** を返します。 

+ **[^]**: かっこで囲まれたテキスト内で最初の文字が曲折記号 (**^**) の場合は、かっこで囲まれた文字を除き、式はすべての文字と一致します。 例

    + **照合("[^bc]at","bat");** は、**0** を返します。 
    + **照合("[^bc]at","hat");** は、**1** を返します。 
    + **照合("[^abc]","bat");** は、**1** を返します。 a、b、または c 以外は一致します。 したがって、t が一致します。 

## <a name="stralpha"></a>strAlpha
文字列の英数字のみをコピーします。

```xpp
str strAlpha(str _text)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明              |
|-----------|--------------------------|
| \_テキスト    | コピー元の文字列。 |

### <a name="return-value"></a>戻り値

指定した文字列からのすべての英数字を含む新しい文字列。

### <a name="remarks"></a>備考

たとえば、**strAlpha(「2+2=5 これで正しいですか」)** は文字列 **225isthiscorrect** を返します。

### <a name="example"></a>例

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

## <a name="strcmp"></a>strCmp
2 つの文字列を比較します。

```xpp
int strCmp(str text1, str text2)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明        |
|-----------|--------------------|
| text1     | 最初の文字列。  |
| text2     | 2 番目の文字列。 |

### <a name="return-value"></a>戻り値

2 つの文字列が同じ場合は **0**、最初の文字列が以前に並べ替えられている場合は **1**、2 つ目の文字列が以前に並べ替えられている場合は **-1** です。

### <a name="remarks"></a>備考

このメソッドで実行される比較では、大文字と小文字が区別されます。

```xpp
print strCmp("abc", "abc"); //Returns the value 0.
print strCmp("abc", "ABC"); //Returns the value 1.
print strCmp("aaa", "bbb"); //Returns the value -1.
print strCmp("ccc", "bbb"); //Returns the value 1.
```

## <a name="strcolseq"></a>strColSeq
すべての大文字を小文字に変換し、アクセントのあるすべての文字を、対応するアクセントのない小文字に変換します。

```xpp
str strColSeq(str text)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                     |
|-----------|-------------------------------------------------|
| テキスト      | 文字をコピーして変換する文字列。 |

### <a name="return-value"></a>戻り値

変換されたテキスト文字列。

### <a name="remarks"></a>備考

**strColSeq** 関数は、下位互換性のために存在します。 この関数は、次の西ヨーロッパの文字のマッピングのみをサポートしています。

-   AàáâãäÀÁÂÃÄBCçÇDEèéêëÈÉÊËFGHIìíîïÌÍÎÏJKLMNñÑOòóôõöÒÓÔÕÖPQRSTUùúûüÙÚÛÜVWXYýÝZæøåÆØÅ
-   aaaaaaaaaaabcccdeeeeeeeeefghiiiiiiiiijklmnnnooooooooooopqrstuuuuuuuuuvwxyyyz~¦Ç~¦Ç

Unicode 互換機能は、**DLL** および **DLLFunc** クラスを通じて Win32 LCMapString アプリケーション プログラミング インターフェイス (API) を使用します。

### <a name="example"></a>例

次の例では、**abcdeabcde** を出力します。

```xpp
    static void strColSeqExample(Args _arg)
    {
            ;
            print strColSeq("");
            pause;
    }
```

## <a name="strdel"></a>strDel
指定されたサブ文字列が削除された文字列のコピーを作成します。

```xpp
str strDel(str _text, int _position, int _number)
```

### <a name="parameters"></a>パラメーター

| パラメーター  | 説明                                                                                                                                                                                                                      |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_テキスト     | コピー元の文字列。                                                                                                                                                                                                         |
| \_職位 | コピー操作時に文字の無視を開始する位置。                                                                                                                                                    |
| \_数値   | 無視する文字数。 *\_番号* パラメーターの前のマイナス記号は、*\_位置* にある文字の前の *\_番号*–1 文字が *\_位置* にある文字と一緒に削除される必要があることを示します。 |

### <a name="return-value"></a>戻り値

文字列からコピーされる残りの文字。

### <a name="remarks"></a>備考

**strDel** 関数は、**substr** 関数を補完します。

```xpp
strDel("ABCDEFGH",2,3); //Returns the string "AEFGH".
strDel("ABCDEFGH",4,3); //Returns the string "ABCGH".
```

## <a name="strfind"></a>strFind
指定された文字のいずれかの 1 番目の文字列を検索します。

```xpp
int strFind(str _text, str _characters, int _position, int _number)
```

### <a name="parameters"></a>パラメーター

| パラメーター    | 説明                                                                                                |
|--------------|------------------------------------------------------------------------------------------------------------|
| \_テキスト       | 検索する文字列。                                                                                      |
| \_文字 | 検索する文字。                                                                              |
| \_職位   | 検索を開始する文字列内の位置。                                                        |
| \_数値     | 検索の方向と文字列内で検索する位置の数を示す符号付き番号。 |

### <a name="return-value"></a>戻り値

指定された文字の 1 つが最初に現れる位置の値、また見つからない場合は 0。

### <a name="remarks"></a>備考

文字列の先頭から最後まで検索するには、*\_位置* パラメーターの値として **1** を使用します。 *\_番号* パラメーターの値がマイナスである場合、システムは指定された位置から後方に文字数を検索します。 検索では大文字と小文字が区別されません。 次に例を示します。

```xpp
strFind("ABCDEFGHIJ","KHD",1,10); //Returns the value 4 (the position where "D" was found).
strFind("ABCDEFGHIJ","KHD",10,-10); //Returns the value 8 (the position where "H" was found).
```

**strFind** 関数は、**strNFind** 関数を補完します。

## <a name="strfmt"></a>strFmt
指定された文字列を書式設定し、すべての n を n 番目の引数に置き換えます。

```xpp
str strFmt(str _string, ...)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明            |
|-----------|------------------------|
| \_文字列  | フォーマットする文字列。 |

### <a name="return-value"></a>戻り値

書式設定された文字列。

### <a name="remarks"></a>備考

パラメーターに引数が指定されない場合は、文字列内では "%n" として返されます。 **実数** 型の値の文字列変換では、小数点第 2 位に制限されます。 値は丸められ、切り捨てられません。 Microsoft .NET Framework の **System.String::Format** メソッドは、例に示すように、追加機能を取得するために使用できます。

### <a name="example"></a>例

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

## <a name="strins"></a>strIns
1 つの文字列を別の文字列に挿入して文字列を作成します。

```xpp
str strIns(str _text1, str _text2, int _position)
```

### <a name="parameters"></a>パラメーター

| パラメーター  | 説明                                                                                          |
|------------|------------------------------------------------------------------------------------------------------|
| \_text1    | 他の文字列を挿入する文字列。                                                          |
| \_text2    | 他の文字列に挿入する文字列。                                                          |
| \_職位 | 出力文字列内への *\_text2* パラメーターの最初の文字の配置位置。 |

### <a name="return-value"></a>戻り値

結合された。

### <a name="remarks"></a>備考

**strIns** 関数は、**strDel** 関数を補完します。 *\_位置* パラメーターの値が元の文字列より長くなる場合、挿入する文字列が元の文字列の末尾に追加されます。

```xpp
strIns("ABFGH","CDE",3); //Returns the string "ABCDEFGH".
strIns("ABCD","EFGH",10); //Returns the string "ABCDEFGH".
```

## <a name="strkeep"></a>strKeep
2 番目の入力文字列で指定する最初の入力文字列の文字のみを使用して文字列を作成します。

```xpp
str strKeep(str _text1, str _text2)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                                                         |
|-----------|-------------------------------------------------------------------------------------|
| \_text1   | 出力文字列を作成するために使用できる文字を含む文字列。 |
| \_text2   | 出力文字列に保持する文字を指定する文字列。           |

### <a name="return-value"></a>戻り値

保存されている文字の文字列。

### <a name="remarks"></a>備考

```xpp
strKeep("ABBCDDEFGHB","BCD"); //Returns the string "BBCDDB".
strKeep("abcZcba","bc") //Returns the string "bccb".
```

**strKeep** 関数は、**strRem** 関数を補完します。

## <a name="strlen"></a>strLen
指定した文字列の長さを計算します。

```xpp
int strLen(str text)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                            |
|-----------|----------------------------------------|
| テキスト      | 長さを計算する文字列。 |

### <a name="return-value"></a>戻り値

指定した文字列の長さ。

### <a name="remarks"></a>備考

```xpp
strLen("ABC"); //Returns the value 3.
strLen("ABCDEFGHIJ"); //Returns the value 10.
```

## <a name="strline"></a>strLine
複数の行にまたがる文字列から 1 つの行を取得します。

```xpp
str strLine(str string, int count)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                              |
|-----------|------------------------------------------|
| string    | 複数の明細行にまたがる文字列。 |
| カウント     | 返す線のオフセット。        |

### <a name="return-value"></a>戻り値

*文字列* パラメーターで指定された文字列のコピーされた明細行です。

### <a name="remarks"></a>備考

文字列の最初の行には 0 のオフセットがあります。 文字列に *\n* または *\r\n* 文字を埋め込むことにより、複数行を1 つの文字列に割り当てることができます。 また、開始引用符の直前にアット マーク (@) を使用することができ、Enter キーを使用して文字列値の一部を X++ コード エディタの複数の行に分散させることができます。

### <a name="example"></a>例

```xpp
str mytxt = "first-line\nsecond-line\nlast-line";
// Prints "second-line".
print strLine(mytxt,1);
// Prints "last-line".
print strLine(mytxt,2);            
```

## <a name="strltrim"></a>strLTrim
テキスト文字列から先行する空白を削除します。

```xpp
str strLTrim(str text)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                   |
|-----------|-----------------------------------------------|
| テキスト      | 先頭の空白を削除する文字列。 |

### <a name="return-value"></a>戻り値

先頭の空白が削除されたテキストに相当する文字列。

### <a name="remarks"></a>備考

**strLTrim** 関数は、**strRTrim** 関数を補完します。

### <a name="example"></a>例

```xpp
// Returns the text string "ABC-DEFG".
strLTrim("   ABC-DEFG");
```

## <a name="strlwr"></a>strLwr
指定された文字列のすべての文字を小文字に変換します。

```xpp
str strLwr(str _text)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                         |
|-----------|-------------------------------------|
| \_テキスト    | 小文字に変換する文字列。 |

### <a name="return-value"></a>戻り値

小文字のみを含んでいる指定された文字列のコピーです。

### <a name="remarks"></a>備考

**strLwr** 関数は、**strUpr** 関数を補完します。 **strLwr** 関数は、Win32 API で **LCMapString** 関数を使用します。

### <a name="example"></a>例

```xpp
static void strLwrExample(Args _args)
{
    // Returns the text string "abcdd55efghij".
    print strLwr("Abcdd55EFGHIJ");
    pause;
}
```
## <a name="strnfind"></a>strNFind
指定した文字リストに含まれていない文字の 1 番目の文字列の一部を検索します。

```xpp
int strNFind(str _text, str _characters, int _position, int _number)
```

### <a name="parameters"></a>パラメーター

| パラメーター    | 説明                                                                                                                                                                                                     |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_テキスト       | 検索するテキスト文字列。                                                                                                                                                                                      |
| \_文字 | 検索から除外する文字のリスト。                                                                                                                                                              |
| \_職位   | 検索を開始する文字列内の位置。                                                                                                                                                        |
| \_数値     | 検索の方向と検索する位置の数を示す符号付き番号。 マイナス記号が *\_番号* に先行する場合、システムでは *\_位置* の逆順で *\_番号* 文字が検索されます。 |

### <a name="return-value"></a>戻り値

*\_characters* パラメーターによって指定されていない文字の 1 番目の位置、また見つからない場合は 0。

### <a name="remarks"></a>備考

検索では大文字と小文字が区別されません。 文字列の先頭から最後まで検索するには、*\_位置* パラメーターの値として **1** を使用します。 マイナス記号が *\_番号* パラメーターの前にある場合、*\_位置* パラメーターで指定された位置から逆の順序で文字が検索されます。

```xpp
strNFind("ABCDEFGHIJ","ABCDHIJ",1,10); //Returns the value 5 (the position of "E");
strNFind("CDEFGHIJ","CDEFGIJ",10,-10); //Returns the value 6 (the position of "H").
strNFind("abcdef","abCdef",3,2) //Returns the value 0.
strNFind("abcdef", "abcef",3,2) //Returns the value 4.
```

**strNFind** 関数は、**strFind** 関数を補完します。

## <a name="strpoke"></a>strPoke
別の文字列で文字列の一部を上書きします。

```xpp
str strPoke(str _text1, str _text2, int _position)
```

### <a name="parameters"></a>パラメーター

| パラメーター  | 説明                                                                     |
|------------|---------------------------------------------------------------------------------|
| \_text1    | 元の文字列。                                                            |
| \_text2    | 元の文字列の一部を置き換える文字列。                         |
| \_職位 | 文字の置き換えを開始する元の文字列の位置。 |

### <a name="return-value"></a>戻り値

新しい文字列。

### <a name="remarks"></a>備考

新しい文字列は、元の文字列より長くすることができます。 ただし、*\_位置* パラメーターの値がを文字列の長さを超える場合、元の文字列が置換なしで返されます。

```xpp
strPoke("12345678","AAA",3); //Returns the string "12AAA678".
strPoke("abcde","4567",4); //Returns the string "abc4567".
strPoke("abcde", "4567", "10"); //Returns the string "abcde".
```

## <a name="strprompt"></a>strPrompt
指定されたピリオド文字数の後に、コロンと空白文字が続く文字列を追加します。

```xpp
str strPrompt(str _string, _int len)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                             |
|-----------|-----------------------------------------|
| \_文字列  | 元の文字列。                    |
| \_len     | 文字列の最終的な長さ。 |

### <a name="return-value"></a>戻り値

ユーザー入力のプロンプトのように見える文字列。

### <a name="remarks"></a>備考

特別な場合では、*\_len* パラメーターの値が元の文字列の長さより少し大きい場合のみ、末尾へのスペース追加に最も高い優先順位が付与されます。 次に、優先順位がコロンに指定されます。 期間には、最下位の優先順位が付けられます。 *\_len* パラメーターの負の値は、後ろにスペースを付けた入力文字列を返します。

```xpp
strPrompt("ab",-1); //Returns "ab ".
strPrompt("ab",3); //Returns "ab ".
strPrompt("ab",4); //Returns "ab: ".
strPrompt("ab",5); //Returns "ab.: ".
strPrompt("ab",6); //Returns "ab..: ".
```

### <a name="example"></a>例

```xpp
static void JobStrPromptDemo(Args _args)
{
    // Printed string is "[abc..: ]"
    print "[", strPrompt("abc", 7), "]";
    pause;
}
```

## <a name="strrem"></a>strRem
別の文字列から 1 つの文字列で指定されている文字を削除します。

```xpp
str strRem(str text1, str text2)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                       |
|-----------|---------------------------------------------------|
| text1     | 文字を削除する文字列。             |
| text2     | 出力文字列から除外する文字。 |

### <a name="return-value"></a>戻り値

元の文字列の残りのコンテンツ。

### <a name="remarks"></a>備考

この関数は、大文字小文字を区別します。

```xpp
strRem("abcd_abcd","Bc"); //Returns the string "abd_abd".
strRem("ABCDEFGABCDEFG","ACEG"); //Returns the string "BDFBDF".
```

 この関数は、**strKeep** 関数を補完します。

## <a name="strrep"></a>strRep
文字の文字列を繰り返します。

```xpp
str strRep(str _text, str _number)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                               |
|-----------|-------------------------------------------|
| \_テキスト    | クエリ返す文字列。                     |
| \_数値  | 文字列を繰り返す回数。 |

### <a name="return-value"></a>戻り値

指定された回数が繰り返される元の文字列の内容を含む新しい文字列。

### <a name="example"></a>例

次の例では、テキスト文字列 **ABABABABABAB** を出力します。

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

## <a name="strrtrim"></a>strRTrim
文字列の末尾から空白文字を削除します。

```xpp
str strRTrim(str _text)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                               |
|-----------|-----------------------------------------------------------|
| \_テキスト    | 末尾の空白文字を削除する文字列。 |

### <a name="return-value"></a>戻り値

末尾に空白文字が含まれていない指定の文字列のコピーです。

### <a name="remarks"></a>備考

```xpp
strRTrim("ABC-DEFG- "); //Returns the string "ABC-DEFG-".
strRTrim(" CD "); //Returns " CD".
```

**strRTrim** 関数は、**strLTrim** 関数を補完します。

## <a name="strscan"></a>strScan
別の文字列と一致する文字列を検索します。

```xpp
int strScan(str _text1, str _text2, int _position, int _number)
```

### <a name="parameters"></a>パラメーター

| パラメーター  | 説明                                                                                                                                                                                                                   |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_text1    | 検索する文字列。                                                                                                                                                                                                      |
| \_text2    | 検索する文字列。                                                                                                                                                                                                           |
| \_職位 | 比較を実行する *\_text1* パラメーターの最初の位置。                                                                                                                                               |
| \_数値   | 比較を再試行する *\_text1* パラメーター内の位置の数。 マイナス記号が *\_番号* パラメーターに先行する場合、システムでは特定位置の逆順で文字数が検索されます。 |

### <a name="return-value"></a>戻り値

文字列内で指定した文字列が見つかった位置。それ以外の場合は **0** (ゼロ)。

### <a name="remarks"></a>備考

この比較では大文字と小文字は区別されません。 *\_位置* パラメーターが **1** 未満の値は **1** として扱われます。 スキャンの方向は、*\_number* パラメーターで指定されている符号で制御されます。 プラス記号は、連続する各比較が文字列の末尾に 1 つ近い位置から開始することを示します。 マイナス記号は、各比較が文字列の先頭に 1 つ近い位置から開始することを示します。

```xpp
strScan("ABCDEFGHIJ","DEF",1,10); //Returns the value 4.
strScan ("ABCDEFGHIJ","CDE",10,-10); //Returns the value 3.
```

## <a name="strupr"></a>strUpr
文字列内のすべての文字を大文字に変換します。

```xpp
str strUpr(str _text)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                 |
|-----------|---------------------------------------------|
| \_テキスト    | 大文字に変換する文字列。 |

### <a name="return-value"></a>戻り値

小文字のみを含んでいる指定された文字列のコピーです。

### <a name="remarks"></a>備考

**strUpr** 関数は、**strLwr** 関数を補完します。 **strUpr** 関数は、Win32 API で **LCMapString()** 関数を使用します。

### <a name="example"></a>例

次の例は **ABCDD55EFGHIJ** を出力します。

```xpp
static void strUprExample(Args _args)
{
    print strUpr("Abcdd55EFGhiJ");
    pause;
}
```

## <a name="substr"></a>subStr
文字列の一部を取得します。

```xpp
str subStr(str _text, int _position, int _number)
```

### <a name="parameters"></a>パラメーター

| パラメーター  | 説明                                                                                                                                                                                                             |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_テキスト     | 元の文字列。                                                                                                                                                                                                    |
| \_職位 | 取得する部分が開始する元の文字列内の位置。                                                                                                                                                  |
| \_数値   | 元の文字列から取得する位置の方向と数を示す符号付き整数。 マイナス記号が *\_番号* に先行する場合、システムでは指定された位置から後方に部分文字列を選択します。 |

### <a name="return-value"></a>戻り値

元の文字列のサブ文字列。

### <a name="remarks"></a>備考

マイナス記号が *\_番号* パラメーターの値より前にある場合、指定された位置から後方に部分文字列を選択します。

```xpp
subStr("ABCDEFGHIJ",3,5); //Returns the string "CDEFG".
subStr("ABCDEFGHIJ",7,-4); //Returns the string "DEFG".
subStr("abcdef"),2,99) //Returns the string "cdef".
subStr("abcdef",2,3) //Returns the string "bcd".
subStr("abcdef",2,-3); //Returns the string "ab".
```




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
