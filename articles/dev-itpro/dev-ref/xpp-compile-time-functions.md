---
title: X++ コンパイル時関数
description: このトピックでは、コンパイル時関数の一覧を示し、その構文、パラメーター、および戻り値について説明します。
author: RobinARH
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 29581
ms.assetid: fa6613a4-7d0b-40d3-be29-9d14c22c7d5b
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 34e9438ef0764399ac9de3444330d05a47e72e5f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369593"
---
# <a name="x-compile-time-functions"></a>X++ コンパイル時関数

[!include [banner](../includes/banner.md)]

このトピックでは、コンパイル時関数の一覧を示し、その構文、パラメーター、および戻り値について説明します。

<a name="overview"></a>概要
--------

コンパイル時関数は、X++ コードのコンパイル時に早期実行されます。 アプリケーション エクスプローラーに保存されているメタデータの変更に対してコードを復元するためには、可能な限り X++ で使用する必要があります。 コンパイル時関数は、コンパイラによって入力値が検証されます。 入力された値が見つからず、アプリケーション エクスプローラーの既存のオブジェクトが一致しない場合は、コンパイラーはエラーを発行します。 コンパイラは実行時に変数に含まれる値を判別できないため、これらの関数への入力はリテラルでなければなりません。 コンパイル時関数は、メタデータ アサーション関数です。 アプリケーション エクスプローラーでエンティティを表す引数を取得し、コンパイル時にその引数を検証します。 実行時に影響を与えません。 属性は **SysAttribute** クラスから継承するクラスです。 フォーム、レポート、クエリ、メニュー のメタデータの検証をサポートするには、コントロールの **AutoDeclaration** プロパティを使用します。 これらの機能のほとんどは、アプリケーション エクスプローラーにある項目に関するメタデータを取得します。 いくつかの一般的なコンパイル時機能は、次のとおりです。

-   `classNum` – クラスの ID を取得します。
-   `classStr` – コンパイル時に、その名前のクラスが存在することを確認します。 この方法は、実行時にエラーを後で発見するよりも優れています。
-   `evalBuf`– X++ コードの入力文字列を評価し、結果を文字列として返します。
-   `literalStr` – は、文字列 `"@SYS12345"` などのラベルの文字列表示が与えられたときにラベル ID を取得します。 たとえば、`myLabel.exists(literalStr("@SYS12345"));`。

| **メモ**                                                         |
|------------------------------------------------------------------|
| X++ コンパイル時関数は .NET プログラムから呼び出すことはできません。 |

### <a name="functions"></a>関数

## <a name="attributestr"></a>attributeStr
指定した属性クラスがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。

### <a name="syntax"></a>構文

    str classStr(class class)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                            |
|-----------|----------------------------------------|
| クラス     | 検証する属性の名前。 |

### <a name="return-value"></a>戻り値

属性の名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    static void attributeStrExample(Args _args)
    {
        str s;
        ;
        s = attributeStr(AifDocumentOperationAttribute);
        print s;
        pause;
    }

## <a name="classnum"></a>classNum
指定されたクラスの ID を取得します。

### <a name="syntax"></a>構文

    int classNum(class class)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                             |
|-----------|-----------------------------------------|
| クラス     | ID を取得するクラス。 |

### <a name="return-value"></a>戻り値

指定されたクラスの ID。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    static void classNumExample(Args _args)
    {
        int i;
        ;
        i = classNum(Global);
        print i;
        pause;
    }

## <a name="classstr"></a>classStr
文字列としてクラスの名前を取得します。

### <a name="syntax"></a>構文

    str classStr(class class)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                      |
|-----------|----------------------------------|
| クラス     | 返すクラスの名前。 |

### <a name="return-value"></a>戻り値

クラスの名前。

### <a name="remarks"></a>備考

リテラル テキストの代わりにこの関数を使用して、クラス名を含む文字列を取得します。 クラスが存在しない場合、関数は、コンパイル時に、構文エラーを生成します。 これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    static void clStrExample(Args _args)
    {
        str s;
        ;
        s = classStr(Global);
        print s;
        pause;
    }

## <a name="configurationkeynum"></a>configurationKeyNum
指定されたコンフィギュレーション キーの ID を取得します。

### <a name="syntax"></a>構文

    int configurationKeyNum(str keyname)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                       |
|-----------|---------------------------------------------------|
| keyname   | ID を返すコンフィギュレーション キー。 |

### <a name="return-value"></a>戻り値

指定されたコンフィギュレーション キーの ID。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    static void configurationKeyNum(Args _args)
    {
        int i;
        ;
        i = configurationKeyNum(AIF);
        print i;
        pause;
    }

## <a name="configurationkeystr"></a>configurationKeyStr
文字列としてコンフィギュレーション キーの名前を取得します。

### <a name="syntax"></a>構文

    str configurationKeyStr(str keyname)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                        |
|-----------|------------------------------------|
| keyname   | コンフィギュレーション キーの名前。 |

### <a name="return-value"></a>戻り値

コンフィギュレーション キーの名前。

### <a name="remarks"></a>備考

リテラル テキストの代わりにこの関数を使用して、構成キー名を含む文字列を取得します。 キーが存在しない場合、関数は、コンパイル時に、構文エラーを生成します。 これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    static void configurationKeyStrExample(Args _args)
    {
        str s;
        ;
        s = configurationKeyStr(AIF);
        print s;
        pause;
    }

## <a name="dataentitydatasourcestr"></a>dataEntityDataSourceStr
データ エンティティのデータ ソースの名前を取得します。

### <a name="syntax"></a>構文

    str dataEntityDataSourceStr(str dataEntity, str dataSource)

### <a name="parameters"></a>パラメーター

| パラメーター  | 説明                  |
|------------|------------------------------|
| dataEntity | データ エンティティの名前。 |
| dataSource | データ ソースの名前。 |

### <a name="return-value"></a>戻り値

データ ソースの名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    No example.

## <a name="delegatestr"></a>delegateStr
委任の名前を返します。

### <a name="syntax"></a>構文

    str delegateStr(str class, str instanceDelegate)

### <a name="parameters"></a>パラメーター

| パラメーター        | 説明                            |
|------------------|----------------------------------------|
| クラス            | クラス、テーブル、またはフォームの名前。 |
| instanceDelegate | インスタンス デリゲートの名前。     |

### <a name="return-value"></a>戻り値

委任の名前です。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    No example.

## <a name="dimensionhierarchylevelstr"></a>dimensionHierarchyLevelStr
分析コード階層レベルの名前を返します。

### <a name="syntax"></a>構文

    str dimensionHierarchyLevelStr(str dimensionHierarchyLevel)

### <a name="parameters"></a>パラメーター

| パラメーター               | 説明                                |
|-------------------------|--------------------------------------------|
| dimensionHierarchyLevel | 分析コード階層レベルの名前。 |

### <a name="return-value"></a>戻り値

分析コード階層レベルの名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    No example.

## <a name="dimensionhierarchystr"></a>dimensionHierarchyStr
分析コード階層の名前を返します。

### <a name="syntax"></a>構文

    str dimensionHierarchyStr(str dimensionHierarchy)

### <a name="parameters"></a>パラメーター

| パラメーター          | 説明                          |
|--------------------|--------------------------------------|
| dimensionHierarchy | 分析コード階層の名前。 |

### <a name="return-value"></a>戻り値

分析コード階層の名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    No example.

## <a name="dimensionreferencestr"></a>dimensionReferenceStr
分析コード参照の名前を返します。

### <a name="syntax"></a>構文

    str dimensionReferenceStr(str dimensionReference)

### <a name="parameters"></a>パラメーター

| パラメーター          | 説明                          |
|--------------------|--------------------------------------|
| dimensionReference | 分析コード参照の名前。 |

### <a name="return-value"></a>戻り値

分析コード参照の名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    No example.

## <a name="dutystr"></a>dutyStr
指定したセキュリティ職務権限の名前を表す文字列を取得します。

### <a name="syntax"></a>構文

    str dutyStr(str securityDuty)

### <a name="parameters"></a>パラメーター

| パラメーター    | 説明                    |
|--------------|--------------------------------|
| securityDuty | セキュリティ職務権限の名前です。 |

### <a name="return-value"></a>戻り値

文字列のセキュリティ職務の名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    No example.

## <a name="enumcnt"></a>enumCnt
指定された列挙型の要素数を取得します。

### <a name="syntax"></a>構文

    int enumCnt(enum enumtype)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明           |
|-----------|-----------------------|
| enumtype  | 列挙型タイプ。 |

### <a name="return-value"></a>戻り値

指定された列挙型の要素数。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    enumCnt(NoYes); //Returns 2, as the two elements are Yes and No.

## <a name="enumliteralstr"></a>enumLiteralStr
指定した文字列が指定した列挙型の要素であるかどうかを示します。

### <a name="syntax"></a>構文

    enumLiteralStr(enum enum, string str)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                                      |
|-----------|------------------------------------------------------------------|
| 列挙型      | 指定された値を取得する列挙型。 |

### <a name="return-value"></a>戻り値

指定された文字列が見つかった場合の *str* パラメーターの値。それ以外の場合は、コンパイル エラーです。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    static void getEnumValueAsString()
    {
        str i;
        i = enumLiteralStr(ABCEnum, "valueInABCEnum");
        print i;
        pause;
    }

## <a name="enumnum"></a>enumNum
指定された列挙型の ID を取得します。

### <a name="syntax"></a>構文

    int enumNum(enum enum)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                 |
|-----------|---------------------------------------------|
| 列挙型      | ID を返す列挙。 |

### <a name="return-value"></a>戻り値

指定された列挙型の ID。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    static void enumNum(Args _args)
    {
        int i;
        ;
        i = enumNum(ABC);
        print i;
        pause;
    }

## <a name="enumstr"></a>enumStr
文字列として列挙型の名前を取得します。

### <a name="syntax"></a>構文

    str enumStr(enum enum)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                  |
|-----------|------------------------------|
| 列挙型      | 列挙型の名前。 |

### <a name="return-value"></a>戻り値

列挙型の名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    static void enumStrExample(Args _args)
    {
        str s;
        ;
        s = enumStr(ABC);
        print s;
        pause;
    }

## <a name="extendedtypenum"></a>extendedTypeNum
指定された拡張データ型の ID を取得します。

### <a name="syntax"></a>構文

    int extendedTypeNum(int str)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                        |
|-----------|----------------------------------------------------|
| str       | ID を返す拡張データ型。 |

### <a name="return-value"></a>戻り値

指定された拡張データ型の ID。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    static void EDTNum(Args _args)
    {
        int i;
        str s;
        ;

        i = extendedTypeNum(AccountName);
        s = extendedTypeStr(AccountName);
        print  int2Str(i);
        print  s;
        pause;
    }

## <a name="extendedtypestr"></a>extendedTypeStr
文字列として拡張データ型の名前を取得します。

### <a name="syntax"></a>構文

    str extendedTypeStr(int str)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                         |
|-----------|-------------------------------------|
| str       | 拡張データ型の名前。 |

### <a name="return-value"></a>戻り値

拡張データ型の名前。

### <a name="remarks"></a>備考

リテラル テキストの代わりにこの関数を使用すると、拡張データ型名を含む文字列を返します。 データ タイプが存在しない場合、**extendedTypeStr** 関数は、コンパイル時に、構文エラーを生成します。 これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    static void EDTStr(Args _args)
    {
        int i;
        str s;
        ;

        i = extendedTypeNum(AccountName);
        s = extendedTypeStr(AccountName);
        print  int2Str(i);
        print  s;
        pause;
    }

## <a name="fieldnum"></a>fieldNum
指定したフィールドの ID 番号を返します。

### <a name="syntax"></a>構文

    int fieldNum(str tableName, str fieldName)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明            |
|-----------|------------------------|
| tableName | テーブルの名前。 |
| fieldName | フィールドの名前。 |

### <a name="return-value"></a>戻り値

指定されたフィールドの ID。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

次の例では、**CashDisc** フィールドの番号を **CustTable** テーブルに出力します。

    static void fieldNumExample(Args _args)
    {
        int myInt;
        ;

        myInt = fieldNum(CustTable, CashDisc);
        Global::info(strfmt("CashDisc has a field ID of %1 in the CustTable table.", myInt));
    }
    /****Infolog Display
    Message (10:40:00 am)
    CashDisc has a field ID of 10 in the CustTable table.
    ****/

## <a name="fieldpname"></a>fieldPName
指定されたフィールドのラベルを取得します。

### <a name="syntax"></a>構文

    str fieldPName(str tableid, str fieldid)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                  |
|-----------|----------------------------------------------|
| tableid   | 指定されたフィールドを含むテーブル。 |
| fieldid   | 変換するフィールド。                        |

### <a name="return-value"></a>戻り値

フィールドのラベル。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

次の例では、**CashDisc** フィールドのラベルを出力します。

    static void fieldPNameExample(Args _arg)
    {
        str myText;
        ;

        myText = fieldPName(CustTable, CashDisc);
        Global::info(strfmt("%1 is the label of the CashDisc field.", myText));
    }
    /****Infolog Display
    Message (02:00:57 pm)
    Cash discount is the label of the CashDisc field.
    ****/

## <a name="fieldstr"></a>fieldStr
指定したフィールドのフィールド名を取得します。

### <a name="syntax"></a>構文

    str fieldStr(str tableid, str fieldid)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                        |
|-----------|------------------------------------|
| tableid   | フィールドを含むテーブル。 |
| fieldid   | 変換するフィールド。              |

### <a name="return-value"></a>戻り値

指定したフィールドのフィールド名。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

次の例では、**CashDisc** フィールドの名前を *myText* 変数に割り当てます。

    static void fieldStrExample(Args _arg)
    {
        str myText;
        ;

        myText = fieldStr(CustTable, CashDisc);
        Global::info(strfmt("%1 is the specified field.", myText));
    }
    /****Infolog Display
    Message (09:11:52 am)
    CashDisc is the specified field.
    ****/

## <a name="formcontrolstr"></a>formControlStr
X++ コンパイラは、コントロールがフォームに存在するかどうかをチェックし、関数呼び出しを有効なコントロール名の文字列で置き換えます。

### <a name="syntax"></a>構文

    str formControlStr(formName, controlName)

### <a name="parameters"></a>パラメーター

| パラメーター   | 説明                                                          |
|-------------|----------------------------------------------------------------------|
| formName    | 引用符ではなく、フォームの名前。                        |
| controlName | フォーム上のコントロールの名前で、引用符ではありません。 |

### <a name="return-value"></a>戻り値

アプリケーション エクスプローラーで表示されるコントロールの名前を含む文字列。

### <a name="remarks"></a>備考

コントロールがフォームに存在しないとコンパイラが判断した場合、コンパイル エラーが表示されます。 X++ コードが引用符が含まれる文字列を使用してコントロールの名前を入力する場合、実行時までエラーを検出できません。 この機能を使用すると、コンパイラはコンパイル時にエラーを早期に検出することができます。 コンパイラにより実行される **formControlStr** などの X++ 関数は、コンパイル時関数と呼ばれます。 入力パラメーターが引用符で囲まれた標準の文字列ではないのはそのためです。 コンパイル時関数は、コンパイラによって出力される P コードまたはその他の実行可能ファイルでは表現されません。 これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    No example.

## <a name="formdatafieldstr"></a>formDataFieldStr
フォームのデータ フィールドの名前を返します。

### <a name="syntax"></a>構文

    str formDataFieldStr(str formName, str dataSource, str dataField)

### <a name="parameters"></a>パラメーター

| パラメーター  | 説明                        |
|------------|------------------------------------|
| formName   | フォームの名前。              |
| dataSource | フォームのデータ ソース。       |
| dataField  | データ ソースのデータ フィールド。 |

### <a name="return-value"></a>戻り値

フォームのデータ フィールドの名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    str a = formDataFieldStr(FMVehicle, FMModelRate, RatePerDay);

## <a name="formdatasourcestr"></a>formDataSourceStr
フォームのデータ ソースの名前を返します。

### <a name="syntax"></a>構文

    str formDataSourceStr(str formName, str dataSource)

### <a name="parameters"></a>パラメーター

| パラメーター  | 説明                  |
|------------|------------------------------|
| formName   | フォームの名前。        |
| dataSource | フォームのデータ ソース。 |

### <a name="return-value"></a>戻り値

フォームのデータ ソースの名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    str b = formDataSourceStr(FMVehicle, FMModelRate);

## <a name="formmethodstr"></a>formMethodStr
フォームのメソッドの名前を返します。

### <a name="syntax"></a>構文

    str formMethodStr(str formName, str methodName)

### <a name="parameters"></a>パラメーター

| パラメーター  | 説明             |
|------------|-------------------------|
| formName   | フォームの名前。   |
| methodName | フォームのメソッド。 |

### <a name="return-value"></a>戻り値

フォームのメソッドの名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

次の例では、**showDialog** メソッドの名前を出力します。

    str c = formMethodStr(Batch,showDialog);

## <a name="formstr"></a>formStr
フォームの名前を取得します。

### <a name="syntax"></a>構文

    str formStr(str form)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明         |
|-----------|---------------------|
| フォーム      | フォームの名前。 |

### <a name="return-value"></a>戻り値

フォームの名前を表す文字列。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

次の例では、InventDim フォームの名前を出力します。

    static void formStrExample(Args _arg)
    {
        ;

        Global::info(formStr(InventDim));
    }
    /****Infolog Display
    Message (11:04:39 am)
    InventDim
    ****/

## <a name="identifierstr"></a>identifierStr
指定された識別子を文字列に変換します。

### <a name="syntax"></a>構文

    str identifierStr(str ident)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                |
|-----------|----------------------------|
| ident     | 変換する ID。 |

### <a name="return-value"></a>戻り値

指定した ID を表す文字列。

### <a name="remarks"></a>備考

**identifierStr** 関数使用する場合、ベスト プラクティス警告が表示されます。 これは、**identifierStr** に対して存在チェックが実行されたために発生します。 使用可能な場合は、より具体的なコンパイル時の関数を使用してください。 これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

次のコード例では、*myvar* 変数名を *thevar* 変数に割り当てています。

    static void indentifierStrExample(Args _args)
    {
        str myvar;
        str thevar
        ;

        thevar = "[" + identifierStr(myvar) + "]";
        Global::info(strfmt(thevar));
    }
    /****Infolog Display
    Message (09:19:49 am)
    [myvar]
    ****/

## <a name="indexnum"></a>indexNum
指定されたインデックスを数字に変換します。

### <a name="syntax"></a>構文

    int indexNum(str tableid, str indexid)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                        |
|-----------|------------------------------------|
| tableid   | フィールド インデックスを含むテーブル。 |
| indexid   | 変換するインデックス。              |

### <a name="return-value"></a>戻り値

指定されたインデックスを表すインデックス番号。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

次の例では、当事者インデックスのインデックス値を返します。

    static void indexNumExample(Args _arg)
    {
        ;

        Global::info(strfmt("%1 is the index number of Party.", indexNum(CustTable, Party)));
    }
    /****Infolog Display
    Message (11:28:03 am)
    3 is the index number of Party.
    ****/

## <a name="indexstr"></a>indexStr
指定されたインデックスを文字列に変換します。

### <a name="syntax"></a>構文

    str indexStr(str tableid, str indexid)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                        |
|-----------|------------------------------------|
| tableid   | フィールド インデックスを含むテーブル。 |
| indexid   | 変換するインデックス。              |

### <a name="return-value"></a>戻り値

指定インデックスを表す文字列。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

次の例では、**CashDisc** インデックス値を *myText* 変数に割り当てます。

    static void fieldStrExample(Args _arg)
    {
        str myText;
        ;

        myText = fieldStr(CustTable, CashDisc);
        Global::info(strfmt("%1 is the specified index.", myText));
    }
    /****Infolog Display
    Message (09:11:52 am)
    CashDisc is the specified index.
    ****/

## <a name="licensecodenum"></a>licenseCodeNum
指定したライセンス コードがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。

### <a name="syntax"></a>構文

    int licenseCodeNum(str codename)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                               |
|-----------|-------------------------------------------|
| codename  | 検証するライセンス コードの名前。 |

### <a name="return-value"></a>戻り値

指定されたライセンス コードの数。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    static void licenseCodeNumExample(Args args)
    {
        int i;
        ;

        i = licenseCodeNum(SysMorphX);
        Global::info(strfmt("%1 is the license code number for SysMorphX.", i));
    }
    /****Infolog Display
    Message (01:52:35 pm)
    24 is the license code number for SysMorphX.
    ****/

## <a name="licensecodestr"></a>licenseCodeStr
指定したライセンス コードがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。

### <a name="syntax"></a>構文

    str licenseCodeStr(str codename)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                               |
|-----------|-------------------------------------------|
| codename  | 検証するライセンス コードの名前。 |

### <a name="return-value"></a>戻り値

指定されたライセンス コードの名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    static void licenseCodeStrExample(Args _arg)
    {
        str s;
        ;

        s = licenseCodeStr(SysMorphX);
        Global::info(strfmt("%1 is the license code string for SysMorphX.", s));
    }
    /****Infolog Display
    Message (02:33:56 pm)
    SysMorphX is the license code string for SysMorphX.
    ****/

## <a name="literalstr"></a>literalStr
指定した文字列がリテラル文字列であることを検証します。そうでない場合は、コンパイラ エラーが発生します。

### <a name="syntax"></a>構文

    str literalStr(int str)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明             |
|-----------|-------------------------|
| codename  | 検証する文字列。 |

### <a name="return-value"></a>戻り値

有効な場合は、リテラル文字列。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    {
        str s;
        ;

        s = literalStr("This is a literal str");
        print s;
        pause;
    }

## <a name="maxdate"></a>maxDate
日付型の変数に使用できる最大値を取得します。

### <a name="syntax"></a>構文

    date maxDate()

### <a name="return-value"></a>戻り値

**日付** の変数に使用できる最大値は、**2154-12-31**です。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    static void maxDateExample(Args _arg)
    {
        date maximumDate;
        ;
        maximumDate = maxDate();
        print maximumDate;
        pause;
    }

## <a name="maxint"></a>maxInt
**int** 型に格納可能な最大符号付き値を取得します。

### <a name="syntax"></a>構文

    int maxInt()

### <a name="return-value"></a>戻り値

整数の許容値の最大値。

### <a name="remarks"></a>備考

その他の整数値は、戻り値以下になります。 これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    static void maxIntExample(Args _arg)
    {
        int i;
        ;
        print "The maximum value for type int is " + int2Str(maxInt());
        pause;
    }

## <a name="measurementstr"></a>measurementStr
測定の名前を返します。

### <a name="syntax"></a>構文

    str measurementStr(str measurement)

### <a name="parameters"></a>パラメーター

| パラメーター   | 説明                  |
|-------------|------------------------------|
| 測定値 | 測定の名前。 |

### <a name="return-value"></a>戻り値

測定の名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    No example.

## <a name="measurestr"></a>measureStr
メジャーの名前を返します。

### <a name="syntax"></a>構文

    str measureStr(str measure)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明              |
|-----------|--------------------------|
| 測定   | 測定の名前。 |

### <a name="return-value"></a>戻り値

測定の名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    No example.

## <a name="menuitemactionstr"></a>menuItemActionStr
指定したメニュー項目のアクションがアプリケーション オブジェクト ツリー (Application Explorer) に存在することを検証します。そうでなければ、コンパイラ エラーが発生します。

### <a name="syntax"></a>構文

    str menuItemActionStr(class menuitem)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                   |
|-----------|-----------------------------------------------|
| codename  | 検証するメニュー項目アクションの名前。 |

### <a name="return-value"></a>戻り値

有効な場合の、メニュー項目アクションの名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    {
        str s1, s2, s3, s4;
        ;

        s1 = menuItemActionStr(AssetCopy);
        s2 = menuItemDisplayStr(Address);
        s3 = menuItemOutputStr(AssetBarcode);
        s4 = menuStr(Administration);

        print "menuItemActionStr for AssetCopy is " + s1;
        print "menuItemDisplayStr for Address is " + s2;
        print "menuItemOutputStr for AssetBarcode is " + s3;
        print "menuStr for Administration is " + s4;

        pause;
    }

## <a name="menuitemdisplaystr"></a>menuItemDisplayStr
指定したメニュー項目の表示がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。

### <a name="syntax"></a>構文

    str menuitemdisplaystr(class menuItem)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                    |
|-----------|------------------------------------------------|
| codename  | 検証するメニュー項目nの表示の名前。 |

### <a name="return-value"></a>戻り値

有効な場合の、指定されたメニューの表示の名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    {
        str s1, s2, s3, s4;
        ;

        s1 = menuItemActionStr(AssetCopy);
        s2 = menuItemDisplayStr(Address);
        s3 = menuItemOutputStr(AssetBarcode);
        s4 = menuStr(Administration);

        print "menuItemActionStr for AssetCopy is " + s1;
        print "menuItemDisplayStr for Address is " + s2;
        print "menuItemOutputStr for AssetBarcode is " + s3;
        print "menuStr for Administration is " + s4;

        pause;
    }

## <a name="menuitemoutputstr"></a>menuItemOutputStr
指定したメニュー項目の出力がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。

### <a name="syntax"></a>構文

    str menuItemOutputStr(class menuitem)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                   |
|-----------|-----------------------------------------------|
| codename  | 検証するメニュー項目出力の名前。 |

### <a name="return-value"></a>戻り値

有効な場合、指定されたメニュー項目が出力されます。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    {
        str s1, s2, s3, s4;
        ;

        s1 = menuItemActionStr(AssetCopy);
        s2 = menuItemDisplayStr(Address);
        s3 = menuItemOutputStr(AssetBarcode);
        s4 = menuStr(Administration);

        print "menuItemActionStr for AssetCopy is " + s1;
        print "menuItemDisplayStr for Address is " + s2;
        print "menuItemOutputStr for AssetBarcode is " + s3;
        print "menuStr for Administration is " + s4;

        pause;
    }

## <a name="menustr"></a>menuStr
指定したメニューがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。

### <a name="syntax"></a>構文

    str menuStr(class menu)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                       |
|-----------|-----------------------------------|
| メニュー      | 検証するメニューの名前。 |

### <a name="return-value"></a>戻り値

有効な場合の指定されたメニュー項目の名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    {
        str s1, s2, s3, s4;
        ;

        s1 = menuItemActionStr(AssetCopy);
        s2 = menuItemDisplayStr(Address);
        s3 = menuItemOutputStr(AssetBarcode);
        s4 = menuStr(Administration);

        print "menuItemActionStr for AssetCopy is " + s1;
        print "menuItemDisplayStr for Address is " + s2;
        print "menuItemOutputStr for AssetBarcode is " + s3;
        print "menuStr for Administration is " + s4;

        pause;
    }

## <a name="methodstr"></a>methodStr
指定したメソッドが指定したクラスに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。

### <a name="syntax"></a>構文

    str methodStr(class class, int method)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                         |
|-----------|-------------------------------------|
| クラス     | クラスの名前。              |
| メソッド    | 検証するメソッドの名前。 |

### <a name="return-value"></a>戻り値

有効な場合の、指定されたメソッドの名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    {
        #define.timeout(50)
        str s;
        SysHelpInitTimeOut SysHelpInitTimeOut;
        ;

        s = methodStr(SysHelpInitTimeOut, timeout);
        print s;
        pause;
    }

## <a name="minint"></a>minInt
**int** 型に格納可能な最小符号付き値を取得します。

### <a name="syntax"></a>構文

    int minInt()

### <a name="return-value"></a>戻り値

**int** 型の最小値です。

### <a name="remarks"></a>備考

その他の整数値は、戻り値以上になります。 これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    static void minIntExample(Args _arg)
    {
        int i;
        ;
        i = minInt();
        print "minInt() is " + int2Str(i);    
        pause;
    }

## <a name="privilegestr"></a>privilegeStr
権限の名前を返します。

### <a name="syntax"></a>構文

    str privilegeStr(str privilege)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                 |
|-----------|---------------------------------------------|
| 権限 | 名前を返す対象の特権。 |

### <a name="return-value"></a>戻り値

権限の名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    No example.

## <a name="querydatasourcestr"></a>queryDatasourceStr
X++ コンパイラは、データ ソースがクエリに存在するかどうかをチェックし、関数呼び出しを有効なデータ ソース名の文字列で置き換えます。

### <a name="syntax"></a>構文

    str queryDataSourceStr(queryName, dataSourceName)

### <a name="parameters"></a>パラメーター

| パラメーター      | 説明                                                               |
|----------------|---------------------------------------------------------------------------|
| queryName      | 引用符ではなく、クエリの名前。                            |
| dataSourceName | クエリ上のデータ ソースの名前で、引用符ではありません。 |

### <a name="return-value"></a>戻り値

アプリケーション エクスプローラーで表示されるデータ ソースの名前を含む文字列。

### <a name="remarks"></a>備考

データ ソースがクエリに存在しないとコンパイラが判断した場合、コンパイル エラーが表示されます。 X++ コードが引用符が含まれる文字列を使用してデータ ソースの名前を入力する場合、実行時までエラーを検出できません。 この機能を使用すると、コンパイラはコンパイル時にエラーを早期に検出することができます。 コンパイラにより実行される **queryDataSourceStr** などの X++ 関数は、コンパイル時関数とみなされます。 入力パラメーターが引用符で囲まれた標準の文字列ではないのはそのためです。 コンパイル時関数は、コンパイラによって出力される P コードまたはその他の実行可能ファイルでは表現されません。 これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    No example.

## <a name="querymethodstr"></a>queryMethodStr
クエリのメソッドの名前を返します。

### <a name="syntax"></a>構文

    str queryMethodStr(str queryName, str methodName)

### <a name="parameters"></a>パラメーター

| パラメーター  | 説明             |
|------------|-------------------------|
| queryName  | クエリの名前。  |
| methodName | フォームのメソッド。 |

### <a name="return-value"></a>戻り値

クエリのメソッドの名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    No example.

## <a name="querystr"></a>queryStr
既存のクエリを表す文字列を取得します。

### <a name="syntax"></a>構文

    str queryStr(str query)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明            |
|-----------|------------------------|
| クエリ     | 取得するクエリ。 |

### <a name="return-value"></a>戻り値

クエリの名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    static void queryStrExample(Args _arg)
    {
        str myText;
        ;

        myText = queryStr(AssetTable);
        Global::info(strfmt("%1 is the name of the query.",myText));
    }
    /****Infolog Display
    Message (09:45:16 am)
    AssetTable is the name of the query.
    ****/

## <a name="reportstr"></a>reportStr
指定したレポートの名前を表す文字列を取得します。

### <a name="syntax"></a>構文

    str reportStr(str report)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                              |
|-----------|------------------------------------------|
| レポート    | 名前を返す対象のレポート。 |

### <a name="return-value"></a>戻り値

レポートの名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

次の例では、**AssetAddition** レポートの名前を *MyTxt* 変数に割り当てます。

    static void reportStrExample(Args _args)
    {
        str MyTxt;
        ;

        MyTxt = reportStr(AssetAddition);
        Global::info(strfmt("%1 is the name of the report.", MyTxt));
    }
    /****Infolog Display.
    Message (10:46:36 am)
    AssetAddition is the name of the report.
    ****/

## <a name="resourcestr"></a>resourceStr
指定したリソースがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。

### <a name="syntax"></a>構文

    str resourceStr(str resourcename)

### <a name="parameters"></a>パラメーター

| パラメーター    | 説明                           |
|--------------|---------------------------------------|
| resourcename | 検証するリソースの名前。 |

### <a name="return-value"></a>戻り値

有効な場合の、指定されたリソースの名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    {
        print "Str for resource StyleSheet_Help_Axapta is " 
            + resourceStr(StyleSheet_Help_Axapta);
        pause;
    }

## <a name="rolestr"></a>roleStr
指定したセキュリティ ロールの名前を表す文字列を取得します。

### <a name="syntax"></a>構文

    str roleStr(str securityRole)

### <a name="parameters"></a>パラメーター

| パラメーター    | 説明                    |
|--------------|--------------------------------|
| securityRole | セキュリティ ロールの名前です。 |

### <a name="return-value"></a>戻り値

文字列のセキュリティ ロールの名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    No example.

## <a name="ssrsreportstr"></a>ssrsReportStr
指定したレポートの名前を表す文字列を取得します。 レポート コントローラー クラスで実行されるレポートを指定する場合は、この関数を使用します。

### <a name="syntax"></a>構文

    str ssrsReportStr(str report, str design)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                                |
|-----------|------------------------------------------------------------|
| レポート    | 名前を返す対象のレポート。                         |
| design    | レポートに関連付けられているデザインの名前。 |

### <a name="return-value"></a>戻り値

レポートの名前。

### <a name="remarks"></a>備考

**ssrsReportStr** 関数は、有効なレポートに属しているかどうかを検証するために、渡された 2 つの値を解析します。 コントローラーが、どのレポート デザインの組み合わせを呼び出す必要があるかを判断できるように、メニュー項目が controller() を指しているときは、レポート名を設定する必要があります。 **ssrsReportStr** 関数を使用すると、レポートおよびデザイン名のコンパイル時の検証で役立ちます。 これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    public static void main(Args _args)
    {
        // Initializing the object for a controller class, in this case, the class named AssetListingController.
        SrsReportRunController controller = new AssetListingController();

        // Getting the properties of the called object (in this case AssetListing MenuItem)
        controller.parmArgs(_args);
        // Setting the Report name for the controller.
        controller.parmReportName(ssrsReportStr(AssetListing, Report));

        // Initiate the report execution.
        controller.startOperation();
    }

## <a name="staticdelegatestr"></a>staticDelegateStr
静的デリゲートの名前を返します。

### <a name="syntax"></a>構文

    str staticDelegateStr(str class, str delegate)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                          |
|-----------|--------------------------------------|
| クラス     | クラス、テーブル、またはフォームの名前。 |
| デリゲート  | 委任の名前です。            |

### <a name="return-value"></a>戻り値

委任の名前です。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    No example.

## <a name="staticmethodstr"></a>staticMethodStr
指定した静的メソッドが指定したクラスに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。

### <a name="syntax"></a>構文

    str staticMethodStr(class class, int method)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                |
|-----------|--------------------------------------------|
| クラス     | クラスの名前。                     |
| メソッド    | 検証する静的メソッドの名前。 |

### <a name="return-value"></a>戻り値

有効な場合の、指定された静的メソッドの名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    No example.

## <a name="tablecollectionstr"></a>tableCollectionStr
指定したテーブル コレクションがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。

### <a name="syntax"></a>構文

    str tableCollectionStr(class tablecollection)

### <a name="parameters"></a>パラメーター

| パラメーター       | 説明                                   |
|-----------------|-----------------------------------------------|
| tablecollection | 検証するテーブル コレクションの名前。 |

### <a name="return-value"></a>戻り値

有効な場合の、指定されたテーブル コレクションの名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    No example.

## <a name="tablefieldgroupstr"></a>tableFieldGroupStr
文字列としてフィールド グループの名前を取得します。

### <a name="syntax"></a>構文

    str tableFieldGroupStr(str tableName, str fieldGroupName)

### <a name="parameters"></a>パラメーター

| パラメーター      | 説明                              |
|----------------|------------------------------------------|
| tableName      | フィールド グループを含むテーブル。 |
| fieldGroupName | テーブル内のフィールド グループ。            |

### <a name="return-value"></a>戻り値

文字列としてのフィールド グループの名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

次の例では、**編集** フィールド グループの名前を文字列として取得します。

    static void tableFieldGroupStrExample(Args _arg)
    {
        ;

        Global::info(tableFieldGroupStr(AccountingDistribution, Editing));
    }
    /****Infolog Display
    Message (03:14:54 pm)
    Editing
    ****/

## <a name="tablemethodstr"></a>tableMethodStr
指定したメソッドが指定したテーブルに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。

### <a name="syntax"></a>構文

    str tableMethodStr(int table, int method)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                         |
|-----------|-------------------------------------|
| テーブル     | テーブルの名前。              |
| メソッド    | 検証するメソッドの名前。 |

### <a name="return-value"></a>戻り値

有効な場合の、メソッドの名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    No example.

## <a name="tablenum"></a>tableNum
特定のテーブルのテーブル ID を取得します。

### <a name="syntax"></a>構文

    int tableNum(str table)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                             |
|-----------|-----------------------------------------|
| テーブル     | テーブル ID を取得するテーブル。 |

### <a name="return-value"></a>戻り値

特定のテーブルのテーブル ID

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

次の例では、**tableID** 変数を 77 に設定します。これは、**CustTable** テーブルの **ID** です。

    static void tableNumExample(Args _args)
    {
        int tableID;
        ;

        tableID = tableNum(CustTable);
        Global::info(strfmt("%1 is the table ID for the CustTable table.", tableID));

    }
    /****Infolog Display
    Message (11:15:54 am)
    77 is the table ID for the CustTable table.
    ****/

## <a name="tablepname"></a>tablePName
指定されたテーブルの出力可能な名前を含む文字列を取得します。

### <a name="syntax"></a>構文

    str tablePName(str table)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                   |
|-----------|-----------------------------------------------|
| テーブル     | 印刷可能な名前を取得するテーブル。 |

### <a name="return-value"></a>戻り値

指定されたテーブルの名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

次の例では、**CustTable** テーブルのラベルを *MyText* 変数に割り当てます。

    static void tablePNameExample(Args _args)
    {
        str MyText;
        ;

        MyText = tablePname(CustTable);
        Global::info(strfmt("%1 is the label of the CustTable table.", MyText));
    }
    /**** Infolog Display.
    Message (12:13:53 pm)
    Customers is the label of the CustTable table.
    ****/

## <a name="tablestaticmethodstr"></a>tableStaticMethodStr
指定した静的メソッドが指定したテーブルに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。

### <a name="syntax"></a>構文

    str tableStaticMethodStr(int table, int method)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                |
|-----------|--------------------------------------------|
| テーブル     | テーブルの名前。                     |
| メソッド    | 検証する静的メソッドの名前。 |

### <a name="return-value"></a>戻り値

指定された静的メソッドの名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    No example.

## <a name="tablestr"></a>tableStr
指定したテーブルの名前を含む文字列を取得します。

### <a name="syntax"></a>構文

    str tableStr(str table)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                         |
|-----------|-------------------------------------|
| テーブル     | 文字列を取得するテーブル。 |

### <a name="return-value"></a>戻り値

指定したテーブルの名前を含む文字列値。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

次の例では、**CustTable** テーブルの名前を *MyTxt* 変数に割り当てます。

    static void tableStrExample(Args _args)
    {
        str MyTxt;
        ;

        MyTxt = tableStr(CustTable);
        Global::info(strfmt("%1 is the str output of the input of CustTable.", MyTxt));
    }
    /**** Infolog Display. 
    Message (01:21:49 pm)
    CustTable is the str output of the input of CustTable.
    ****/

## <a name="tilestr"></a>tileStr
指定したタイルの名前を表す文字列を取得します。

### <a name="syntax"></a>構文

    str tileStr(str tile)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明           |
|-----------|-----------------------|
| tile      | タイルの名前。 |

### <a name="return-value"></a>戻り値

文字列のタイルの名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    No example.

## <a name="varstr"></a>varStr
指定した変数の名前を含む文字列を取得します。

### <a name="syntax"></a>構文

    str varStr(str var)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明               |
|-----------|---------------------------|
| var       | 変数の名前。 |

### <a name="return-value"></a>戻り値

指定した変数の名前を含む文字列。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    static void varStrExample(Args _arg)
    {
        str myString;
        anytype myVariable;
        ;

        myString = varStr(myVariable);
        Global::info(strfmt("%1 is the variable name.", myString));
    }
    /****Infolog Display.
    Message (02:26:56 pm)
    myVariable is the variable name.
    ****/

## <a name="webactionitemstr"></a>webActionItemStr
指定した Web アクション項目がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。

### <a name="syntax"></a>構文

    str webActionItemStr(class webactionitem)

### <a name="parameters"></a>パラメーター

| パラメーター     | 説明                                  |
|---------------|----------------------------------------------|
| webactionitem | 検証する Web アクション項目の名前。 |

### <a name="return-value"></a>戻り値

有効な場合の、指定された Web アクション項目の名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    {
        str s;
        ;
        s = webActionItemStr(EPFlushData);
        print "webactionitem str is " + s;
        pause;
    }

## <a name="webdisplaycontentitemstr"></a>webDisplayContentItemStr
指定したWeb 表示のコンテンツ項目がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。

### <a name="syntax"></a>構文

    str webDisplayContentItemStr(class webdisplaycontentitem)

### <a name="parameters"></a>パラメーター

| パラメーター             | 説明                                           |
|-----------------------|-------------------------------------------------------|
| webdisplaycontentitem | 検証する Web 表示コンテンツ項目の名前。 |

### <a name="return-value"></a>戻り値

有効な場合の、指定された Web 表示コンテンツ項目の名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    {
        str s;
        ;

        s = webDisplayContentItemStr(EPAdmin);
        print "string for webcontent display item EPAdmin is " + s;
        pause;
    }

## <a name="webformstr"></a>webFormStr
指定した Web フォームがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。

### <a name="syntax"></a>構文

    str webFormStr(str name)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                           |
|-----------|---------------------------------------|
| 名前      | 検証する Web フォームの名前。 |

### <a name="return-value"></a>戻り値

有効な場合の、指定された Web フォームの名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    {
        str s;
        ;
        s = webFormStr(EPAdmin);
        print "String for web form EPAdmin is " + s;
        pause;
    }

## <a name="webletitemstr"></a>webletItemStr
指定した Weblet 項目がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。

### <a name="syntax"></a>構文

    str webletItemStr(class webletitem)

### <a name="parameters"></a>パラメーター

| パラメーター  | 説明                              |
|------------|------------------------------------------|
| webletitem | 検証する Weblet 項目の名前。 |

### <a name="return-value"></a>戻り値

有効な場合の、指定された Weblet 項目の名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    {
        str s;
        ;
        s = webletItemStr(WebFormWeblet);
        print "String for WebFormWeblet is " + s;
        pause;
    }

## <a name="webmenustr"></a>webMenuStr
指定した Web メニューがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。

### <a name="syntax"></a>構文

    str webMenuStr(str name)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                           |
|-----------|---------------------------------------|
| 名前      | 検証する Web メニューの名前。 |

### <a name="return-value"></a>戻り値

有効な場合の、指定された Web メニューの名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    {
        str s;
        ;
        s = webMenuStr(ECPAdmin);
        print "String for web menu ECPAdmin is " + s;
        pause;
    }

## <a name="weboutputcontentitemstr"></a>webOutputContentItemStr
指定したWeb 出力のコンテンツ項目がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。

### <a name="syntax"></a>構文

    str webOutputContentItemStr(class weboutputcontentitem)

### <a name="parameters"></a>パラメーター

| パラメーター            | 説明                                          |
|----------------------|------------------------------------------------------|
| weboutputcontentitem | 検証する Web 出力コンテンツ項目の名前。 |

### <a name="return-value"></a>戻り値

有効な場合の、指定された Web 出力コンテンツ項目の名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    {
        str s;
        ;
        s = webOutputContentItemStr(EPPriceList);
        print "string for weboutput content item EPPriceList is " + s;
        pause;
    }

## <a name="webpagedefstr"></a>webpageDefStr
指定した Web ページ定義がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。

### <a name="syntax"></a>構文

    str webpageDefStr(str pagename)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                      |
|-----------|--------------------------------------------------|
| pagename  | 検証する Web ページ定義の名前。 |

### <a name="return-value"></a>戻り値

有効な場合の、指定された Web ページ定義の名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    No example.

## <a name="webreportstr"></a>webReportStr
指定した Web レポートがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。

### <a name="syntax"></a>構文

    str webReportStr(str name)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                             |
|-----------|-----------------------------------------|
| 名前      | 検証する Web レポートの名前。 |

### <a name="return-value"></a>戻り値

有効な場合の、指定された Web レポートの名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    {
        str s;
        ;
        s = webReportStr(EPCSSSalesConfirm);
        print "String for web report EPCSSalesConfirm is " + s;
        pause;
    }

## <a name="websitedefstr"></a>websiteDefStr
指定した Web サイトの定義がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。

### <a name="syntax"></a>構文

    str websiteDefStr(str resourcename)

### <a name="parameters"></a>パラメーター

| パラメーター    | 説明                                      |
|--------------|--------------------------------------------------|
| resourcename | 検証する Web サイト定義の名前。 |

### <a name="return-value"></a>戻り値

有効な場合の、指定された Web サイト定義の名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    {
        str s;
        ;

        s = websiteDefStr(AxSiteDef_1033_xip);
        print "string for web site definition AxSiteDef_1033_xip is " + s;
        pause;
    }

## <a name="websitetempstr"></a>webSiteTempStr
指定した Web サイトのテンプレートがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。

### <a name="syntax"></a>構文

    str websiteTempStr(str resourcename)

### <a name="parameters"></a>パラメーター

| パラメーター    | 説明                                    |
|--------------|------------------------------------------------|
| resourcename | 検証する Web サイト テンプレートの名前。 |

### <a name="return-value"></a>戻り値

有効な場合の、指定された Web テンプレートの名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    No example.

## <a name="webstaticfilestr"></a>webStaticFileStr
指定した Web 静的ファイルがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。

### <a name="syntax"></a>構文

    str webStaticFileStr(str pagename)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                  |
|-----------|----------------------------------------------|
| pagename  | 検証する Web 静的ファイル テンプレートの名前。 |

### <a name="return-value"></a>戻り値

有効な場合の、指定された Web 静的ファイルの名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    {
        str s;
        ;

        s = webStaticFileStr(AXEP);
        print "string for web static file AXEP is " + s;
        pause;
    }

## <a name="weburlitemstr"></a>webUrlItemStr
指定した Web URL 項目がアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。

### <a name="syntax"></a>構文

    str webUrlItemStr(class weburlitem)

### <a name="parameters"></a>パラメーター

| パラメーター  | 説明                               |
|------------|-------------------------------------------|
| weburlitem | 検証する Web URL 項目の名前。 |

### <a name="return-value"></a>戻り値

有効な場合の、指定された Web URL 項目の名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    {
        str s;
        ;

        s = webUrlItemStr(EPAdmin);
        print "string for web url item EPAdmin is " + s;
        pause;
    }

## <a name="webwebpartstr"></a>webWebPartStr
指定した Web パーツがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。

### <a name="syntax"></a>構文

    str webWebpartStr(str resourcename)

### <a name="parameters"></a>パラメーター

| パラメーター    | 説明                           |
|--------------|---------------------------------------|
| resourcename | 検証する Web パーツの名前。 |

### <a name="return-value"></a>戻り値

有効な場合の、指定された Web パーツの名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    {
        str s;
        ;

        s = webWebpartStr(AxWebParts_cab);
        print "string for web part AxWebParts_cab is " + s;
        pause;
    }

## <a name="workflowapprovalstr"></a>workflowApprovalStr
アプリケーション オブジェクト ツリー (アプリケーション エクスプローラー) でワークフロー承認の名前を文字列として取得します。

### <a name="syntax"></a>構文

    str workflowapprovalstr(approval approval)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                             |
|-----------|---------------------------------------------------------|
| 承認  | ワークフローの承認のアプリケーション エクスプローラーの名前。 |

### <a name="return-value"></a>戻り値

ワークフローの承認のアプリケーション エクスプローラーの名前を表す文字列。

### <a name="remarks"></a>備考

リテラル テキストの代わりにこの関数を使用して、ワークフロー承認名を含む文字列を取得します。 ワークフローの承認が存在しない場合、関数は、コンパイル時に、構文エラーを生成します。 これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

次のコード例では、変数 *str s* を **MyWorkflowApproval** に設定します。これは、アプリケーション エクスプローラーでのワークフロー承認の名前です。

    static void MyWorkflowApprovalStrExample(Args _args)
    {
        str s;
        ;
        s = workflowapprovalstr(MyWorkflowApproval);
        print s;
        pause;
    }

## <a name="workflowcategorystr"></a>workflowCategoryStr
アプリケーション オブジェクト ツリー (アプリケーション エクスプローラー) でワークフロー カテゴリの名前を文字列として取得します。

### <a name="syntax"></a>構文

    str workflowcategorystr(category category)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                             |
|-----------|---------------------------------------------------------|
| カテゴリ  | ワークフロー カテゴリーのアプリケーション エクスプローラーの名前。 |

### <a name="return-value"></a>戻り値

ワークフロー カテゴリのアプリケーション エクスプローラーの名前を表す文字列。

### <a name="remarks"></a>備考

リテラル テキストの代わりにこの関数を使用して、ワークフロー カテゴリ名を含む文字列を取得します。 ワークフローのカテゴリーが存在しない場合、関数は、コンパイル時に、構文エラーを生成します。 これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

次のコード例では、変数 *str s* を **MyWorkflowCategory** に設定します。これは、アプリケーション エクスプローラーでのワークフロー カテゴリの名前です。

    static void MyWorkflowCategoryStrExample(Args _args)
    {
        str s;
        ;
        s = workflowcategorystr(MyWorkflowCategory);
        print s;
        pause;
    }

## <a name="workflowtaskstr"></a>workflowTaskStr
アプリケーション オブジェクト ツリー (アプリケーション エクスプローラー) でワークフロー タスクの名前を文字列として取得します。

### <a name="syntax"></a>構文

    str workflowtaskstr(task task)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                         |
|-----------|-----------------------------------------------------|
| タスク      | ワークフロー タスクのアプリケーション エクスプローラーの名前。 |

### <a name="return-value"></a>戻り値

ワークフロー タスクのアプリケーション エクスプローラーの名前を表す文字列。

### <a name="remarks"></a>備考

リテラル テキストの代わりにこの関数を使用して、ワークフロー タスク名を含む文字列を取得します。 ワークフローのタスクーが存在しない場合、関数は、コンパイル時に、構文エラーを生成します。 これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

次のコード例では、変数 *str s* を **MyWorkflowTask** に設定します。これは、アプリケーション エクスプローラーでのワークフロー タスクの名前です。

    static void MyWorkflowTaskStrExample(Args _args)
    {
        str s;
        ;
        s = workflowtaskstr(MyWorkflowTask);
        print s;
        pause;
    }

## <a name="workflowtypestr"></a>workflowTypeStr
指定したワークフロー タイプがアプリケーション エクスプローラーに存在することを検証します。そうでなければ、コンパイラ エラーが発生します。

### <a name="syntax"></a>構文

    str workflowTypeStr(str workflow)

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                |
|-----------|--------------------------------------------|
| ワークフロー  | 検証するワークフロー タイプの名前。 |

### <a name="return-value"></a>戻り値

ワークフロー タイプの名前。

### <a name="remarks"></a>備考

これは、コンパイル時関数です。 詳細については、「[概要](#overview)」を参照してください。

### <a name="example"></a>例

    static void workFlowTypeStrExample(Args _args)
    {
        str s;
        ;
        s = workFlowTypeStr(BudgetAccountEntryType);
        print s;
        pause;
    }



