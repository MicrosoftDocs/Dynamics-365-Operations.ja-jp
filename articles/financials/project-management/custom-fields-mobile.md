---
title: iOS および Android 用 Microsoft Dynamics 365 Project Timesheet モバイル アプリのカスタム フィールドの実装
description: このトピックでは、拡張機能を使用してカスタム フィールドを実装するための共通のパターンを示します。
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 4343c875da05641c57b7784bf52f1c814dd26d20
ms.sourcegitcommit: 19859d8566a8c7840066b2c10c6b08b67f1b83f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2019
ms.locfileid: "1617999"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>iOS および Android 用 Microsoft Dynamics 365 Project Timesheet モバイル アプリのカスタム フィールドの実装

[!include [banner](../includes/banner.md)]

このトピックでは、拡張機能を使用してカスタム フィールドを実装するための共通のパターンを示します。 トピックの対象は次のとおりです。

- カスタム フィールド フレームワークでサポートされるさまざまなデータ型
- タイムシート エントリに読み取り専用または編集可能なフィールドを表示し、ユーザーが入力した値をデータベースに再保存する方法
- タイムシート ヘッダーに読み取り専用フィールドを表示する方法
- 他のカスタム ビジネス ロジックを統合して、フィールドに既定値を入力し、追加の検証を行う方法

## <a name="audience"></a>対象者

このトピックは、Apple iOS および Google Android で利用可能な Microsoft Dynamics 365 Project Timesheet モバイル アプリケーションにカスタムフィールドを統合する開発者を対象としています。 読者が X++ 開発とプロジェクト タイムシート機能をよく使用していることを前提としています。

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>データ契約 – TSTimesheetCustomField X++ クラス

**TSTimesheetCustomField** クラスは、X++ データ契約クラスで、タイムシート機能のカスタム フィールドに関する情報を表します。 モバイル アプリにカスタム フィールドを表示するために、TSTimesheetDetails データ契約と TSTimesheetEntry データ契約の両方にカスタム フィールド オブジェクトのリストが渡されます。

- **TSTimesheetDetails** - タイムシートのヘッダー契約。
- **TSTimesheetEntry** - タイムシートのトランザクション契約。 同じプロジェクト情報と **timesheetLineRecId** 値を持つオブジェクトのグループが 1 つの明細行を構成します。

### <a name="fieldbasetype-types"></a>fieldBaseType (タイプ)

**TsTimesheetCustom** オブジェクトの **FieldBaseType** プロパティによって、アプリに表示されるフィールドのタイプが決定されます。 次の**タイプ**の値がサポートされます。

| タイプの値 | 型              | 摘要 |
|-------------|-------------------|-------|
| 0           | 文字列 (および列挙) | このフィールドは、テキスト フィールドとして表示されます。 |
| 1           | 整数           | この値は、小数点以下を含まない数字として表示されます。 |
| 2           | 実績              | この値は、小数点以下を含む数字として表示されます。<p>アプリで通貨として実数値を表示するには、**fieldExtenededType** プロパティを使用します。 **numberOfDecimals** プロパティを使用し、表示される小数点以下の桁数を設定することができます。</p> |
| 3           | 日              | 日付の形式は、**ユーザー オプション**の**言語と国/地域の基本設定**の下で指定される、ユーザーの**日付、時刻、および数字の形式**の設定によって決定されます。 |
| 4           | ブール型           | |
| 15          | GUID              | |
| 16          | Int64             | |

- **stringOptions** プロパティが **TSTimesheetCustomField** オブジェクトで指定されていない場合、自由書式のフィールドがユーザーに提供されます。

    **stringLength** プロパティを使用し、ユーザーが入力できる最大文字列長を設定することができます。

- **stringOptions** プロパティが **TSTimesheetCustomField** オブジェクトで指定された場合、これらのリスト要素が、ユーザーがオプション ボタン (ラジオ ボタン) を使用して選択できる唯一の値になります。

    この場合、文字列フィールドは、ユーザーの入力を目的とする列挙値として機能します。 データベースに値を列挙として保存するには、コマンド チェーンを使用してデータベースに保存する前に、手動で文字列値を列挙値にマップします (このトピックで後述する「TSTimesheetEntryService クラスでコマンド チェーンを使用し、アプリからデータベースにタイムシート エントリを再保存する」のセクションの例を参照してください)。

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

このプロパティを使用して、通貨として実数値の書式設定をすることができます。 この方法は、**fieldBaseType** の値が**実数**である場合にのみ適用されます。

- **TSCustomFieldExtendedType:None** – 書式設定は適用されません。
- **TSCustomFieldExtendedType::Currency** – 通貨として値の書式設定します。

    通貨の書式設定が有効な場合、**stringValue** フィールドを使用してアプリに表示する通貨コードを渡すことができます。 値は読み取り専用です。

    **realValue** フィールドには、データベースに保存する必要のある金額が含まれています。

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

このプロパティを使用して、カスタム フィールドを必要のあるアプリ内の場所を指定することができます。

- **TSCustomFieldSection::Header** – このフィールドはアプリの**詳細を表示**セクションに表示されます。 これらのフィールドは、常に読み取り専用です。
- **TSCustomFieldSection::Line** – このフィールドはタイムシート エントリで最初から用意されている明細行フィールドすべての後に表示されます。 これらのフィールドは、編集可能または読み取り専用のいずれかになります。

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

このプロパティにより、アプリによって指定される値がデータベースに再保存される時にフィールドを識別します。

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

このプロパティにより、アプリによって指定される値がデータベースに再保存される時にフィールドを識別します。

### <a name="iseditable-noyes"></a>isEditable (NoYes)

このプロパティを**はい**に設定し、ユーザーが編集可能なタイムシート エントリ セクションのフィールドを指定することができます。 このプロパティを**いいえ**に設定し、フィールドを読み取り専用にすることができます。

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

このプロパティを**はい**に設定し、タイムシート エントリ セクションの必須のフィールドを指定することができます。

### <a name="label-str"></a>label (str)

このプロパティにより、アプリのフィールドの次に表示されるラベルを指定します。

### <a name="stringoptions-list-of-strings"></a>stringOptions (文字列のリスト)

このプロパティは、**fieldBaseType** が**文字列**に設定されている場合にのみ適用されます。 **stringOptions** が設定されている場合、オプション ボタン (ラジオ ボタン) により選択可能な文字列値は、リストの文字列によって指定されます。 文字列が指定されなかった場合、文字列フィールドの自由書式のテキストが許可されます (このトピックで後述する「TSTimesheetEntryService クラスでコマンド チェーンを使用し、アプリからデータベースにタイムシート エントリを再保存する」のセクションの例を参照してください)。

### <a name="stringlength-int"></a>stringLength (int)

このプロパティにより、文字列フィールドの長さの最大値を指定します。 **fieldBaseType** が**文字列**に設定されている場合にのみ適用されます。

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

このプロパティにより、実数フィールドに表示される小数点以下の桁数を指定します。 **fieldBaseType** が**実数**に設定されている場合にのみ適用されます。

### <a name="ordersequence-int"></a>orderSequence (int)

このプロパティにより、複数のカスタム フィールドが指定された場合に、カスタム フィールドがアプリに表示される順序を制御します。 番号が小さいフィールドが最初に表示されます。

### <a name="booleanvalue-boolean"></a>booleanValue (ブール型)

**ブール型**のタイプのフィールドの場合、このプロパティはサーバーとアプリの間でフィールドのブール値を渡します。

### <a name="guidvalue-guid"></a>guidValue (guid)

**GUID** のタイプのフィールドの場合、このプロパティはサーバーとアプリの間でフィールドのグローバル一意識別子 (GUID) を渡します。

### <a name="int64value-int64"></a>int64Value (int64)

**Int64** タイプのフィールドの場合、このプロパティはサーバーとアプリの間でフィールドの int64 値を渡します。

### <a name="intvalue-int"></a>intValue (int)

**Int** タイプのフィールドの場合、このプロパティはサーバーとアプリの間でフィールドの int 値を渡します。

### <a name="realvalue-real"></a>realValue (実数)

**実数**タイプのフィールドの場合、このプロパティはサーバーとアプリの間でフィールドの実数値を渡します。

### <a name="stringvalue-str"></a>stringValue (str)

**文字列**タイプのフィールドの場合、このプロパティはサーバーとアプリの間でフィールドの文字列値を渡します。 通貨として書式設定された**実数**タイプのフィールドにも使用されます。 これらのフィールドについて、このプロパティはアプリに通貨コードを渡すために使用されます。

### <a name="datevalue-date"></a>dateValue (日付)

**日付**タイプのフィールドの場合、このプロパティはサーバーとアプリの間でフィールドの日付値を渡します。

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>タイムシート エントリ セクションのカスタム フィールドの表示および保存

タイムシート エントリを作成するモバイル アプリのスクリーンショットを次に示します。 「テスト文字列」と呼ばれる「時間エントリ」に最初から用意されているフィールドとカスタム フィールドが、すでに設定されている「2 番目のオプション」の列挙値と共に表示されます。

![アプリのテスト文字列のカスタム フィールド](media/timesheet-entry.jpg)



「テスト文字列」のカスタム フィールドで使用可能な列挙オプションのいずれかを選択しているユーザーのモバイル アプリのスクリーンショットは次のとおりです。  ラジオ ボタンとして表示されている「1 番目のオプション」と「2 番目のオプション」の 2 つのオプションがあります。 現在、2 番目のオプションが選択されています。

![テスト文字列のカスタム フィールドのオプション ボタン (ラジオ ボタン)](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>カスタム フィールドが含まれるように TSTimesheetLine テーブルを拡張します。

一般的なシナリオでは、タイムシート エントリ セクションのカスタム フィールドのデータが TSTimesheetLine テーブルに保存されることがあります。 ただし、他のテーブルは、指定された TSTimesheetTrans レコードに基づいてデータが取得された場合、またはTSTimesheetTransレコードに基づいてデータを取得できる場合、または固有のレコード コンテキストを持たない場合に使用されます (たとえば、プロジェクト パラメーターでフィールドが読み取り専用として設定されている場合です)。

カスタム フィールドには、バッキングのデータベース レコードを持つ必要がないことに注意してください。 X++ ロジックに基づいて動的に生成することができます。 この方法は読み取り専用のシナリオで役に立ちます (動的に生成されたカスタム フィールド値の例については、「TSTimesheetDetails クラスでコマンド チェーンを使用し、buildCustomFieldListForHeader メソッドによりタイムシートの詳細を入力する」のセクションを参照してください。)

アプリケーション オブジェクト ツリーの Visual Studio のスクリーンショットを次に示します。 TSTimesheetLine テーブルの拡張機能とカスタム フィールドとして追加された TestLineString フィールドを表示します。

![行文字列](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>TSTimesheetSettings クラスの buildCustomFieldList メソッドのコマンド チェーンを使用して、タイムシート エントリ セクションにフィールドを表示します。

このコードにより、アプリのフィールドの表示設定を制御します。 たとえば、フィールドのタイプ、ラベル、フィールドが必須であるかどうか、またフィールドが表示されるセクションを制御します。

次の例は、時間入力の文字列フィールドを示します。 このフィールドには、**1 番目のオプション**と**2 番目のオプション**の 2 つのオプションがあり、オプション ボタン (ラジオ ボタン) を介して使用可能です。 アプリのフィールドは、TSTimesheetLine テーブルに追加される **TestLineString** フィールドに関連付けられています。

**TSTimesheetCustomField::newFromMetatdata()** メソッドを使用して、**fieldBaseType**、**tableName**、**fieldname**、**label**、**isEditable**、**isMandatory**、**stringLength**、および **numberOfDecimals** のカスタム フィールド プロパティの初期化を簡略化することに注意してください。 これらのパラメーターは、必要に応じて手動で設定することもできます。

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>TSTimesheetEntry クラスの buildCustomFieldListForEntry メソッドのコマンド チェーンを使用して、タイムシート エントリに値を入力します。

**buildCustomFieldListForEntry** メソッドは、モバイル アプリの保存されたタイムシートの明細行に値を入力するために使用されます。 TSTimesheetTrans レコードをパラメーターとして使用します。 レコードのフィールドを使用して、アプリのカスタム フィールドの値を入力することができます。

```
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>TSTimesheetEntryService クラスのコマンド チェーンを使用して、アプリからデータベースにタイムシートのエントリを再保存します。

通常の方法でデータベースにカスタム フィールドを再保存するには、複数のメソッドを拡張する必要があります。

- **timesheetLineNeedsUpdating** メソッドを使用して、明細行レコードがアプリでユーザーによって変更されたかどうか、およびデータベースに保存する必要があるかどうかを特定します。 パフォーマンスが問題にならない場合は、このメソッドを簡略化し、常に **True** を返すようにすることができます。
- **populateTimesheetLineFromEntryDuringCreate** および **populateTimesheetLineFromEntryDuringUpdate** メソッドを拡張し、指定された TSTimesheetEntry データ コントラクト レコードから TSTimesheetLine データベース レコードに値を入力できるようにすることができます。 次の例では、データベース フィールドと入力フィールドの間のマッピングが X++ コードを介して手動で行われる方法に注意してください。
- **TSTimesheetEntry** オブジェクトにマップされているカスタム フィールドを TSTimesheetLineweek データベース テーブル に再書き込みする必要がある場合、**populateTimesheetWeekFromEntry** メソッドは拡張することもできます。

> [!NOTE]
> 次の例では、ユーザーが未加工の文字列値としてデータベースに選択した **firstOption** または **secondOption** の値を保存します。 データベース フィールドが**列挙**タイプのフィールドである場合、これらの値を手動で列挙値にマップし、データベース テーブルの列挙フィールドに保存することができます。

```
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>タイムシート ヘッダー セクションのカスタム フィールドの表示

ユーザーがタイムシートを表示しているモバイル アプリのスクリーンショットを次に示します。 「詳細を表示」オプションを表示するために、右上隅にある「詳細情報」ボタンが選択されています。  

![詳細なコマンドを表示](media/show-more.png)



タイムシートの「詳細」セクションを表示しているモバイル アプリのスクリーンショットを次に示します。 「このタイムシートの稼動率 (計算されたカスタム フィールド)」と呼ばれるカスタム フィールドがタイムシートのヘッダー セクションに追加されました。 「0.667」の読み取り専用値がカスタム フィールドに設定されています。

![詳細セクション](media/more-section.jpg)



### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>カスタム フィールドが含まれるように TSTimesheetTable テーブルを拡張します。

一般的なシナリオでは、ヘッダー セクションのカスタム フィールドのデータが TSTimesheetHeader テーブルから引き出されることがあります。 ただし、他のテーブルは、指定された TSTimesheetTable のレコードに基づいてデータが取得された場合、またはTSTimesheetTransレコードに基づいてデータを取得できる場合、または固有のレコード コンテキストを持たない場合に使用されます (たとえば、プロジェクト パラメーターでフィールドが読み取り専用として設定されている場合です)。

カスタム フィールドには、バッキングのデータベース レコードを持つ必要がないことに注意してください。 X++ ロジックに基づいて動的に生成することができます。 次の例はこの方法を示しています。

ヘッダー セクションのフィールドは、アプリでは常に読み取り専用です。

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>TSTimesheetSettings クラスの buildCustomFieldList メソッドのコマンド チェーンを使用して、ヘッダー セクションにフィールドを表示します。

このコードにより、アプリのフィールドの表示設定を制御します。 たとえば、フィールドのタイプ、ラベル、フィールドが必須であるかどうか、またフィールドが表示されるセクションを制御します。

次の例では、アプリのヘッダー セクションに計算された値を表示します。

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>TSTimesheetDetails クラスの buildCustomFieldListForHeader メソッドのコマンド チェーンを使用して、タイムシートの詳細を記入します。

**buildCustomFieldListForHeader** メソッドは、モバイル アプリのタイムシート ヘッダーの詳細を記入するために使用されます。 TSTimesheetTable レコードをパラメーターとして使用します。 レコードのフィールドを使用して、アプリのカスタム フィールドの値を入力することができます。 次の例では、データベースから値を読み取ることができません。 代わりに、X++ ロジックを使用して、アプリに表示される計算値を生成します。


```
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>他のコンフィギュレーションの可能性または機能拡張の機会

### <a name="adding-additional-validation-for-the-app"></a>アプリへの追加検証の追加

タイムシート機能に対するデータベース レベルでの既存のロジックは、期待どおりに動作します。 保存または送信操作の完了を中断して特定のエラー メッセージを表示するために、コマンド チェーン拡張機能を介してコードに**エラーをスロー (「ユーザーへのメッセージ」)** を追加することができます。 便利で拡張可能なメソッドの 3 つの例を示します。

- タイムシートの明細行に対する保存操作中に TSTimesheetLine テーブルの **validateWrite** が **False** を返す場合、エラー メッセージがモバイル アプリに表示されます。
- アプリでタイムシートの送信中に TSTimesheetTable テーブルの **validateSubmit** が **False** を返す場合、エラー メッセージがユーザーに表示されます。
- TSTimesheetLine テーブルの**挿入**メソッドの実行中にフィールドを入力するロジック (たとえば、**明細行プロパティ**) も実行されます。

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>コンフィギュレーションにより、最初から用意されているフィールドを非表示また読み取り専用としてマーキング

プロジェクト パラメーターから、最初から用意されているフィールドをモバイル アプリで読み取り専用または非表示にすることができます。 **プロジェクト管理と会計パラメーター** ページの**タイムシート** タブで、**モバイル タイムシート** セクションのオプションを設定します。

![プロジェクト パラメーター](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>拡張機能を介して選択可能な活動の変更

プロジェクトに対して選択可能な活動は、**TsTimesheetProjectService** クラスの **getActivitiesForProject()** および **getActivityQuery()** メソッドを介して入力されます。 コマンド チェーンを使用してこの動作を変更し、特定のプロジェクトに対して選択可能な活動のビジネス シナリオに一致させることができます。

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>タイムシート エントリに既定のプロジェクト カテゴリを入力する

タイムシート エントリの既定のプロジェクト カテゴリの入力は、3 つのレベルで発生します。 コマンド チェーンを使用してこれらのレベルのいずれかまたはすべてにおける動作を拡張することにより、目的の動作を実現することができます。 次の階層が使用されます。

1. アプリは、プロジェクト リソースからの既定のカテゴリの配置を試みます。 この既定のカテゴリは、**TSTimesheetSettingsService** クラスの **getCurrentUserResource** および **getDelegatedResourcesForCurrentUser** メソッドで設定されます。
2. プロジェクト リソース レベルで既定のカテゴリが指定されていない場合、アプリはプロジェクト活動からの取得を試みます。 この既定のカテゴリは、**TSTimesheetProjectService** クラスの **getActivitiesForProject** メソッドで設定されます。
3. プロジェクト活動レベルで既定のカテゴリが指定されていない場合、既定のカテゴリはプロジェクトのパラメーターから取得されます。 この既定のカテゴリは、**TSTimesheetProjectService** クラスの **getProjectDetailsbyRule** メソッドで設定されます。
