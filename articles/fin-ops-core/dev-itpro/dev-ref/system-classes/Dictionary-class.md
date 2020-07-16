---
title: ディクショナリ クラス
description: このトピックでは、ディクショナリ クラスについて説明します。
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
ms.openlocfilehash: d3b343d1fdafd695b3fea2d3febfbb2a9e3df2d7
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502673"
---
# <a name="class-dictionary"></a>クラス ディクショナリ

[!include [banner](../../includes/banner.md)]

```xpp
class Dictionary extends Object
```

ディクショナリ クラスは、テーブル、拡張データ型、クラス、およびアプリケーション オブジェクト ツリー (AOT) の他の品目に関する情報を提供します。

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                                                       | 説明                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| public int classCnt()                                                                                                                        | クラスの数を示します。                                                        |
| public ClassId classCnt2Id(int cnt)                                                                                                          | 指定されたクラスの ID を提供します。                                                                            |
| public str className(ClassId classId)                                                                                                        | 指定されたクラスの名前を提供します。                                                                          |
| public ClassId className2Id(str name)                                                                                                        | クラスの名前に基づいて、指定されたクラスの ID を提供します。                                                  |
| public ClassId classNext(ClassId classId)                                                                                                    | クラス ID に基づいて、指定されたクラスの後に続くクラスを示します。                                     |
| public DictClass classObject(ClassId classId)                                                                                                | DictClass オブジェクトを返すことで、指定されたクラスに関する情報を提供します。                                    |
| public int configurationKeyCnt()                                                                                                             | コンフィギュレーション キーの数を示します。                                             |
| public ConfigurationKeyId configurationKeyCnt2Id(int cnt)                                                                                    | 指定された構成キーの ID を提供します。                                                                |
| public str configurationKeyName(ConfigurationKeyId configurationKey)                                                                         | 指定された構成キーの名前を提供します。                                                              |
| public ConfigurationKeyId configurationKeyName2Id(str name)                                                                                  | 構成キー名に基づいて、指定された構成キーの ID を提供します。                          |
| public ConfigurationKeyId configurationKeyNext(ConfigurationKeyId configurationKey)                                                          | コンフィギュレーション キー ID に基づいて、指定されたコンフィギュレーション キーの後に続くコンフィギュレーション キーを示します。 |
| public DictConfigurationKey configurationKeyObject(ConfigurationKeyId configurationKey)                                                      | DictConfigurationKey オブジェクトを返すことで、指定された構成キーに関する情報を提供します。             |
| public SelectableDataArea currentCompany()                                                                                                   | データベースでデータを使用できる現在の会社を示します。                                       |
| public int enumCnt()                                                                                                                         | 列挙型の数を示します。                                              |
| public EnumId enumCnt2Id(int cnt)                                                                                                            | 指定された列挙型タイプの ID を提供します。                                                                 |
| public str enumName(EnumId typeId)                                                                                                           | 指定された列挙型の名前を指定します。                                                                   |
| public EnumId enumName2Id(str name)                                                                                                          | 名前に基づく、指定された列挙型の ID を提供します。                                                   |
| public EnumId enumNext(EnumId typeId)                                                                                                        | 列挙型 ID に基づいて、指定した列挙型の後に続く列挙型を示します。    |
| public DictEnum enumObject(EnumId typeId)                                                                                                    | DictEnum オブジェクトを返すことで、指定された列挙型に関する情報を提供します。                               |
| public int licenseCodeCnt()                                                                                                                  | ライセンス コードの数を示します。                                                  |
| public LicenseCodeId licenseCodeCnt2Id(int cnt)                                                                                              | 指定されたライセンス コードの ID を提供します。                                                                     |
| public str licenseCodeName(LicenseCodeId licenseCode)                                                                                        | 指定されたライセンス コードの名前を提供します。                                                                   |
| public LicenseCodeId licenseCodeName2Id(str name)                                                                                            | ライセンス コード名に基づいて、指定されたライセンス コードの ID を提供します。                                    |
| public LicenseCodeId licenseCodeNext(LicenseCodeId licenseCode)                                                                              | ライセンス コード ID に基づいて、指定したライセンス コードの後に続くライセンス コードを示します。                |
| public DictLicenseCode licenseCodeObject(LicenseCodeId licenseCode)                                                                          | DictLicenseCode オブジェクトを返すことで、指定されたライセンス コードに関する情報を提供します。                       |
| public int tableCnt()                                                                                                                        | テーブルの数を示します。                                                         |
| public TableId tableCnt2Id(int cnt)                                                                                                          | 指定されたテーブルの ID を提供します。                                                                            |
| public str tableName(TableId tableId)                                                                                                        | 指定されたテーブルの名前を提供します。                                                                          |
| public TableId tableName2Id(str name)                                                                                                        | テーブルの名前に基づいて、指定されたテーブルの ID を提供します。                                                  |
| public TableId tableNext(TableId tableId)                                                                                                    | テーブル ID に基づいて、指定されたテーブルの後に続くテーブルを示します。                                     |
| public DictTable tableObject(TableId tableId)                                                                                                | DictTable オブジェクトを返すことで、指定されたテーブルに関する情報を提供します。                                    |
| public boolean tableSql(TableId tableId)                                                                                                     | テーブルが SQL テーブルであるかどうかを示します。                                                                        |
| public boolean tableSystem(TableId tableId)                                                                                                  | テーブルがシステム テーブルであるかどうかを示します。                                                                     |
| public int testCode(int id, str value, str name, str serialno, str expiryDate, \[int userCount\], \[boolean verifyCert\], \[str timestamp\]) |                                                                                                                  |
| public int typeCnt()                                                                                                                         | 拡張データ型の数を示します。                                            |
| public ExtendedTypeId typeCnt2Id(int cnt)                                                                                                    | 指定された拡張データ型の ID を提供します。                                                               |
| public str typeName(ExtendedTypeId typeId)                                                                                                   | 指定された拡張データ型の名前を提供します。                                                             |
| public ExtendedTypeId typeName2Id(str name)                                                                                                  | 拡張データ型名に基づいて、指定された拡張データ型の ID を提供します。                        |
| public ExtendedTypeId typeNext(ExtendedTypeId typeId)                                                                                        | ID に基づいて、指定された拡張データ型の後に続く拡張データ型を示します。                 |
| public DictType typeObject(ExtendedTypeId typeId)                                                                                            | DictType オブジェクトを返すことで、指定された拡張データ型に関する情報を提供します。                        |
| ::public static boolean safeMode()                                                                                                           |                                                                                                                  |
| ::public static void loginSettingsFlush()                                                                                                    | ログオン設定を更新します。                                                          |
| ::public static void dataFlush(\[TableId tableId\])                                                                                          | テーブル データを更新します。                                                               |
| public void tableFlush()                                                                                                                     | テーブを更新します。                                                                   |
| public void enumFlush()                                                                                                                      | 列挙型を更新します。                                                        |
| public void new()                                                                                                                            | Dictionary クラスの新しいインスタンスを初期化します。                                                              |
| public void classFlush()                                                                                                                     | クラスを更新します。                                                                  |
| public void reloadSecurity(\[boolean reloadCodes\], \[boolean setSynchronizeRequired\], \[boolean flushTable\])                              | 機能キー システムを再読み込みします。                                                                                  |
| public void typeFlush()                                                                                                                      | 拡張データ型を更新します。                                                      |
| public void configurationKeyFlush()                                                                                                          | コンフィギュレーション キーを更新します。                                                       |
| public void licenseCodeFlush()                                                                                                               | ライセンス コードを更新します。                                                            |
| ::public static void aodFlush()                                                                                                              | .aod ファイルを更新します。                                                                                         |

## <a name="method-classcnt"></a>メソッド classCnt

クラスの数を示します。

```xpp
public int classCnt()
```

### <a name="return-value---classcnt"></a>戻り値 - classCnt

クラスの数を示す整数値。

## <a name="method-classcnt2id"></a>メソッド classCnt2Id

指定されたクラスの ID を提供します。

```xpp
public ClassId classCnt2Id(int cnt)
```

### <a name="parameters---classcnt2id"></a>パラメーター - classCnt2Id

cnt  
クラスの順序に基づいてクラスを指定する整数値。

### <a name="return-value---classcnt2id"></a>戻り値 - classCnt2Id

クラス ID を示す classId システム データ型値。Dictionary::classCnt メソッドによって返されるクラスの数より大きな cnt 値を渡すと 0 (ゼロ)。

## <a name="method-classname"></a>メソッド className

指定されたクラスの名前を提供します。

```xpp
public str className(ClassId classId)
```

### <a name="parameters---classname"></a>パラメーター - className

classId  
クラス ID を示す classId システム データ型。

### <a name="return-value---classname"></a>戻り値 - className

クラス名を示す文字列。

### <a name="remarks---classname"></a>備考 - className

クラス ID は、符号なし整数です。

## <a name="method-classname2id"></a>メソッド className2Id

クラスの名前に基づいて、指定されたクラスの ID を提供します。

```xpp
public ClassId className2Id(str name)
```

### <a name="parameters---classname2id"></a>パラメーター - className2Id

名前  
クラス名を示す文字列。

### <a name="return-value---classname2id"></a>戻り値 - className2Id

クラス ID を示す classId システム データ型値; 存在しないクラスの名前値を渡すと 0 (ゼロ)。

## <a name="method-classnext"></a>メソッド classNext

クラス ID に基づいて、指定されたクラスの後に続くクラスを示します。

```xpp
public ClassId classNext(ClassId classId)
```

### <a name="parameters---classnext"></a>パラメーター - classNext

classId  
クラス ID を示す classId システム データ型。

### <a name="return-value---classnext"></a>戻り値 - classNext

指定されたクラスを継承するクラスを示す classId システム データ型値。

## <a name="method-classobject"></a>メソッド classObject

DictClass オブジェクトを返すことで、指定されたクラスに関する情報を提供します。

```xpp
public DictClass classObject(ClassId classId)
```

### <a name="parameters---classobject"></a>パラメーター - classObject

classId  
クラス ID を示す classId システム データ型。

### <a name="return-value---classobject"></a>戻り値 - classObject

指定されたクラスに関する情報を含む DictClass オブジェクト。

## <a name="method-configurationkeycnt"></a>メソッド configurationKeyCnt

コンフィギュレーション キーの数を示します。

```xpp
public int configurationKeyCnt()
```

### <a name="return-value---configurationkeycnt"></a>戻り値 - configurationKeyCnt

コンフィギュレーション キーの数を示す整数値。

## <a name="method-configurationkeycnt2id"></a>メソッド configurationKeyCnt2Id

指定された構成キーの ID を提供します。

```xpp
public ConfigurationKeyId configurationKeyCnt2Id(int cnt)
```

### <a name="parameters---configurationkeycnt2id"></a>パラメーター - configurationKeyCnt2Id

cnt  
コンフィギュレーション キーの順序に基づいてコンフィギュレーション キーを指定する整数。

### <a name="return-value---configurationkeycnt2id"></a>戻り値 - configurationKeyCnt2Id

コンフィギュレーション キー ID を示す configurationKeyId システム データ型値。Dictionary::configurationKeyCnt メソッドから返されるコンフィギュレーション キーの数よりも大きい cnt 値を渡すと、このデータ型値は 0 (ゼロ) になります。

## <a name="method-configurationkeyname"></a>メソッド configurationKeyName

指定された構成キーの名前を提供します。

```xpp
public str configurationKeyName(ConfigurationKeyId configurationKey)
```

### <a name="parameters---configurationkeyname"></a>パラメーター - configurationKeyName

configurationKey  
コンフィギュレーション キーの ID を示す configurationKeyId システム データ型。

### <a name="return-value---configurationkeyname"></a>戻り値 - configurationKeyName

コンフィギュレーション キーの名前を示す文字列。

## <a name="method-configurationkeyname2id"></a>メソッド configurationKeyName2Id

構成キー名に基づいて、指定された構成キーの ID を提供します。

```xpp
public ConfigurationKeyId configurationKeyName2Id(str name)
```

### <a name="parameters---configurationkeyname2id"></a>パラメーター - configurationKeyName2Id

名前  
コンフィギュレーション キーの名前を示す文字列。

### <a name="return-value---configurationkeyname2id"></a>戻り値 - configurationKeyName2Id

コンフィギュレーション キー ID を示す configurationKeyId システム データ型値; 存在しないコンフィギュレーション キー の名前の値を渡すと、0 (ゼロ) になります。

## <a name="method-configurationkeynext"></a>メソッド configurationKeyNext

コンフィギュレーション キー ID に基づいて、指定されたコンフィギュレーション キーの後に続くコンフィギュレーション キーを示します。

```xpp
public ConfigurationKeyId configurationKeyNext(ConfigurationKeyId configurationKey)
```

### <a name="parameters---configurationkeynext"></a>パラメーター - configurationKeyNext

configurationKey  
コンフィギュレーション キーの ID を示す configurationKeyId システム データ型。

### <a name="return-value---configurationkeynext"></a>戻り値 - configurationKeyNext

指定されたコンフィギュレーション キー の後に続くコンフィギュレーション キーの configurationKeyId システム データ型値。

## <a name="method-configurationkeyobject"></a>メソッド configurationKeyObject

DictConfigurationKey オブジェクトを返すことで、指定された構成キーに関する情報を提供します。

```xpp
public DictConfigurationKey configurationKeyObject(ConfigurationKeyId configurationKey)
```

### <a name="parameters---configurationkeyobject"></a>パラメーター - configurationKeyObject

configurationKey  
コンフィギュレーション キーの ID を示す configurationKeyId システム データ型。

### <a name="return-value---configurationkeyobject"></a>戻り値 - configurationKeyObject

指定されたコンフィギュレーション キーに関する情報を含む DictConfigurationKey オブジェクト。

## <a name="method-currentcompany"></a>メソッド currentCompany

データベースでデータを使用できる現在の会社を示します。

```xpp
public SelectableDataArea currentCompany()
```

### <a name="return-value---currentcompany"></a>戻り値 - currentCompany

現在の会社を示す SelectableDataArea システムのデータ型の値。

## <a name="method-enumcnt"></a>メソッド enumCnt

列挙型の数を示します。

```xpp
public int enumCnt()
```

### <a name="return-value---enumcnt"></a>戻り値 - enumCnt

列挙型の数を示す整数。

## <a name="method-enumcnt2id"></a>メソッド enumCnt2Id

指定された列挙型タイプの ID を提供します。

```xpp
public EnumId enumCnt2Id(int cnt)
```

### <a name="parameters---enumcnt2id"></a>パラメーター - enumCnt2Id

cnt  
列挙型の順序に基づいて列挙型を指定する整数。

### <a name="return-value---enumcnt2id"></a>戻り値 - enumCnt2Id

列挙型 ID を示す enumId システム データ型値です。Dictionary::enumCnt メソッドによって返されるクラスの数より大きな cnt 値を渡すと、このデータ型値は 0 (ゼロ) になります。

## <a name="method-enumname"></a>メソッド enumName

指定された列挙型の名前を指定します。

```xpp
public str enumName(EnumId typeId)
```

### <a name="parameters---enumname"></a>パラメーター - enumName

typeId  
列挙の enumId システム データ型です。

### <a name="return-value---enumname"></a>戻り値 - enumName

列挙の名前を示す文字列。

## <a name="method-enumname2id"></a>メソッド enumName2Id

名前に基づく、指定された列挙型の ID を提供します。

```xpp
public EnumId enumName2Id(str name)
```

### <a name="parameters---enumname2id"></a>パラメーター - enumName2Id

名前  
列挙の名前を示す文字列。

### <a name="return-value---enumname2id"></a>戻り値 - enumName2Id

列挙の ID を示す enumId システム データ型値です。

## <a name="method-enumnext"></a>メソッド enumNext

列挙型 ID に基づいて、指定した列挙型の後に続く列挙型を示します。

```xpp
public EnumId enumNext(EnumId typeId)
```

### <a name="parameters---enumnext"></a>パラメーター - enumNext

typeId  
列挙 ID を示す enumId システム データ型です。

### <a name="return-value---enumnext"></a>戻り値 - enumNext

指定された列挙を継承する列挙の enumId システム データ型値です。

## <a name="method-enumobject"></a>メソッド enumObject

DictEnum オブジェクトを返すことで、指定された列挙型に関する情報を提供します。

```xpp
public DictEnum enumObject(EnumId typeId)
```

### <a name="parameters---enumobject"></a>パラメーター - enumObject

typeId  
列挙 ID を示す enumId システム データ型です。

### <a name="return-value---enumobject"></a>戻り値 - enumObject

指定された列挙に関する情報を含む DictEnum オブジェクト。

## <a name="method-licensecodecnt"></a>メソッド licenseCodeCnt

ライセンス コードの数を示します。

```xpp
public int licenseCodeCnt()
```

### <a name="return-value---licensecodecnt"></a>戻り値 - licenseCodeCnt

ライセンス コードの数を示す整数。

## <a name="method-licensecodecnt2id"></a>メソッド licenseCodeCnt2Id

指定されたライセンス コードの ID を提供します。

```xpp
public LicenseCodeId licenseCodeCnt2Id(int cnt)
```

### <a name="parameters---licensecodecnt2id"></a>パラメーター - licenseCodeCnt2Id

cnt  
ライセンス コードの順序に基づいてライセンス コードを指定する整数。

### <a name="return-value---licensecodecnt2id"></a>戻り値 - licenseCodeCnt2Id

ライセンス コード ID を示す licenseCodeId システム データ型値。Dictionary::licenseCodeCnt メソッドによって返されるライセンス コードの数より大きな cnt 値を渡すと、このデータ型値は 0 (ゼロ) になります。

## <a name="method-licensecodename"></a>メソッド licenseCodeName

指定されたライセンス コードの名前を提供します。

```xpp
public str licenseCodeName(LicenseCodeId licenseCode)
```

### <a name="parameters---licensecodename"></a>パラメーター - licenseCodeName

licenseCode  
ライセンス コード ID を示す licenseCodeId システム データ型。

### <a name="return-value---licensecodename"></a>戻り値 - licenseCodeName

ライセンス コード名を示す文字列。

## <a name="method-licensecodename2id"></a>メソッド licenseCodeName2Id

ライセンス コード名に基づいて、指定されたライセンス コードの ID を提供します。

```xpp
public LicenseCodeId licenseCodeName2Id(str name)
```

### <a name="parameters---licensecodename2id"></a>パラメーター - licenseCodeName2Id

名前  
ライセンス コード名を示す文字列。

### <a name="return-value---licensecodename2id"></a>戻り値 - licenseCodeName2Id

ライセンス コード ID を示す licenseCodeId システム データ型の値、存在しないライセンス コード名の値を渡すと 0 (ゼロ)。

## <a name="method-licensecodenext"></a>メソッド licenseCodeNext

ライセンス コード ID に基づいて、指定したライセンス コードの後に続くライセンス コードを示します。

```xpp
public LicenseCodeId licenseCodeNext(LicenseCodeId licenseCode)
```

### <a name="parameters---licensecodenext"></a>パラメーター - licenseCodeNext

licenseCode  
ライセンス コード ID を示す licenseCodeId システム データ型。

### <a name="return-value---licensecodenext"></a>戻り値 - licenseCodeNext

指定したライセンス コードの後に続くライセンス コードの licenseCodeId システム データ型の値。

## <a name="method-licensecodeobject"></a>メソッド licenseCodeObject

DictLicenseCode オブジェクトを返すことで、指定されたライセンス コードに関する情報を提供します。

```xpp
public DictLicenseCode licenseCodeObject(LicenseCodeId licenseCode)
```

### <a name="parameters---licensecodeobject"></a>パラメーター - licenseCodeObject

licenseCode  
ライセンス コード ID を示す licenseCodeId システム データ。

### <a name="return-value---licensecodeobject"></a>戻り値 - licenseCodeObject

指定されたライセンス コードに関する情報を含む DictLicenseCode オブジェクト。

## <a name="method-tablecnt"></a>メソッド tableCnt

テーブルの数を示します。

```xpp
public int tableCnt()
```

### <a name="return-value---tablecnt"></a>戻り値 - tableCnt

テーブルの数を示す整数。

## <a name="method-tablecnt2id"></a>メソッド tableCnt2Id

指定されたテーブルの ID を提供します。

```xpp
public TableId tableCnt2Id(int cnt)
```

### <a name="parameters---tablecnt2id"></a>パラメーター - tableCnt2Id

cnt  
テーブルの順序に基づく、テーブルを指定する整数。

### <a name="return-value---tablecnt2id"></a>戻り値 - tableCnt2Id

テーブル ID を示す TableId システムのデータ型値。Dictionary::tableCnt メソッドによって返されるテーブル数より大きな cnt 値を渡すと、このデータ型値は 0 (ゼロ)。

## <a name="method-tablename"></a>メソッド tableName

指定されたテーブルの名前を提供します。

```xpp
public str tableName(TableId tableId)
```

### <a name="parameters---tablename"></a>パラメーター - tableName

tableId  
テーブル ID を示す tableId システムのデータ型。

### <a name="return-value---tablename"></a>戻り値 - tableName

テーブル名を示す文字列、存在しない tableId 値を渡すと UNKNOWN。

### <a name="remarks---tablename"></a>備考 - tableName

存在しない tableId 値を渡すと、不明が返されます。

## <a name="method-tablename2id"></a>メソッド tableName2Id

テーブルの名前に基づいて、指定されたテーブルの ID を提供します。

```xpp
public TableId tableName2Id(str name)
```

### <a name="parameters---tablename2id"></a>パラメーター - tableName2Id

名前  
テーブル名を示す文字列。

### <a name="return-value---tablename2id"></a>戻り値 - tableName2Id

テーブル ID を示す TableId システムのデータ型値、存在しないテーブルの名前の値を渡すと 0 (ゼロ)。

## <a name="method-tablenext"></a>メソッド tableNext

テーブル ID に基づいて、指定されたテーブルの後に続くテーブルを示します。

```xpp
public TableId tableNext(TableId tableId)
```

### <a name="parameters---tablenext"></a>パラメーター - tableNext

tableId  
テーブル ID を示す tableId システムのデータ型。

### <a name="return-value---tablenext"></a>戻り値 - tableNext

指定されたテーブルの後に続くテーブルの TableId システムのデータ型値。

## <a name="method-tableobject"></a>メソッド tableObject

DictTable オブジェクトを返すことで、指定されたテーブルに関する情報を提供します。

```xpp
public DictTable tableObject(TableId tableId)
```

### <a name="parameters---tableobject"></a>パラメーター - tableObject

tableId  
テーブル ID を示す tableId システムのデータ型。

### <a name="return-value---tableobject"></a>戻り値 - tableObject

指定されたテーブルに関する情報を含む DictTable オブジェクト。

## <a name="method-tablesql"></a>メソッド tableSql

テーブルが SQL テーブルであるかどうかを示します。

```xpp
public boolean tableSql(TableId tableId)
```

### <a name="parameters---tablesql"></a>パラメーター - tableSql

tableId  
テーブル ID を示す tableId システムのデータ型。

### <a name="return-value---tablesql"></a>戻り値 - tableSql

テーブルが SQL テーブルである場合は true。それ以外の場合は false。

## <a name="method-tablesystem"></a>メソッド tableSystem

テーブルがシステム テーブルであるかどうかを示します。

```xpp
public boolean tableSystem(TableId tableId)
```

### <a name="parameters---tablesystem"></a>パラメーター - tableSystem

tableId  
テーブル ID を示す tableId システムのデータ型。

### <a name="return-value---tablesystem"></a>戻り値 - tableSystem

テーブルがシステム テーブルである場合は true。それ以外の場合は false。

### <a name="remarks---tablesystem"></a>備考 - tableSystem

tableNum 組み込み関数を使用して、テーブル ID の代わりにテーブル名をこのメソッドに渡すことができます。 この機能の詳細については、「組み込み関数」を参照してください。

## <a name="method-testcode"></a>メソッド testCode

```xpp
public int testCode(int id, str value, str name, str serialno, str expiryDate, [int userCount], [boolean verifyCert], [str timestamp])
```

### <a name="parameters---testcode"></a>パラメーター - testCode

id  

<!-- -->

値  

<!-- -->

名前  

<!-- -->

serialno  

<!-- -->

expiryDate  

<!-- -->

userCount  

<!-- -->

verifyCert  

<!-- -->

timestamp  

### <a name="return-value---testcode"></a>戻り値 - testCode

## <a name="method-typecnt"></a>メソッド typeCnt

拡張データ型の数を示します。

```xpp
public int typeCnt()
```

### <a name="return-value---typecnt"></a>戻り値 - typeCnt

拡張データ型の数を示す整数。

## <a name="method-typecnt2id"></a>メソッド typeCnt2Id

指定された拡張データ型の ID を提供します。

```xpp
public ExtendedTypeId typeCnt2Id(int cnt)
```

### <a name="parameters---typecnt2id"></a>パラメーター - typeCnt2Id

cnt  
拡張データ型の順序に基づいて拡張データ型を指定する整数。

### <a name="return-value---typecnt2id"></a>戻り値 - typeCnt2Id

拡張データ型の ID を示す extendedTypeId システム データ型値です。Dictionary::typeCnt メソッドによって返される拡張データ型の数より大きな cnt 値を渡すと、このデータ型値は 0 (ゼロ) になります。

## <a name="method-typename"></a>メソッド typeName

指定された拡張データ型の名前を提供します。

```xpp
public str typeName(ExtendedTypeId typeId)
```

### <a name="parameters---typename"></a>パラメーター - typeName

typeId  
拡張データ型の ID を示す extendedTypeId システム データ型です。

### <a name="return-value---typename"></a>戻り値 - typeName

拡張データ型の名前を示す文字列。

## <a name="method-typename2id"></a>メソッド typeName2Id

拡張データ型名に基づいて、指定された拡張データ型の ID を提供します。

```xpp
public ExtendedTypeId typeName2Id(str name)
```

### <a name="parameters---typename2id"></a>パラメーター - typeName2Id

名前  
拡張データ型の名前を示す文字列。

### <a name="return-value---typename2id"></a>戻り値 - typeName2Id

拡張データ型の ID を示す extendedTypeId システム データ型値です。存在しない拡張データ型の名前の値を渡した場合は 0 (ゼロ) になります。

## <a name="method-typenext"></a>メソッド typeNext

ID に基づいて、指定された拡張データ型の後に続く拡張データ型を示します。

```xpp
public ExtendedTypeId typeNext(ExtendedTypeId typeId)
```

### <a name="parameters---typenext"></a>パラメーター - typeNext

typeId  
拡張データ型の ID を示す extendedTypeId システム データ型です。

### <a name="return-value---typenext"></a>戻り値 - typeNext

指定された拡張データ型を継承する拡張データ型の extendedTypeId システム データ型値です。

## <a name="method-typeobject"></a>メソッド typeObject

DictType オブジェクトを返すことで、指定された拡張データ型に関する情報を提供します。

```xpp
public DictType typeObject(ExtendedTypeId typeId)
```

### <a name="parameters---typeobject"></a>パラメーター - typeObject

typeId  
拡張データ型の ID を示す extendedTypeId システム データ型です。

### <a name="return-value---typeobject"></a>戻り値 - typeObject

指定されてた拡張データ型に関する情報を含む DictType オブジェクト。

## <a name="method-safemode"></a>メソッド safeMode

```xpp
public static boolean safeMode()
```

### <a name="return-value---safemode"></a>戻り値 - safeMode

## <a name="method-loginsettingsflush"></a>メソッド loginSettingsFlush

ログオン設定を更新します。

```xpp
public static void loginSettingsFlush()
```

## <a name="method-dataflush"></a>メソッド dataFlush

テーブル データを更新します。

```xpp
public static void dataFlush([TableId tableId])
```

### <a name="parameters---dataflush"></a>パラメーター - dataFlush

tableId  
単一のテーブルまたはすべてのテーブルを示す tableId システムのデータ型。 既定値はすべてです。

### <a name="remarks---dataflush"></a>備考 - dataFlush

既定では、このメソッドはすべてのテーブルのデータを更新します。

## <a name="method-tableflush"></a>メソッド tableFlush

テーブを更新します。

```xpp
public void tableFlush()
```

## <a name="method-enumflush"></a>メソッド enumFlush

列挙型を更新します。

```xpp
public void enumFlush()
```

## <a name="method-new"></a>メソッド new

Dictionary クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

## <a name="method-classflush"></a>メソッド classFlush

クラスを更新します。

```xpp
public void classFlush()
```

## <a name="method-reloadsecurity"></a>メソッド reloadSecurity

機能キー システムを再読み込みします。

```xpp
public void reloadSecurity([boolean reloadCodes], [boolean setSynchronizeRequired], [boolean flushTable])
```

### <a name="parameters---reloadsecurity"></a>パラメーター - reloadSecurity

reloadCodes  

<!-- -->

setSynchronizeRequired  

<!-- -->

flushTable  

### <a name="remarks---reloadsecurity"></a>備考 - reloadSecurity

\_reloadCodes パラメーターの既定値は false です。 \_setSynchronizeRequired パラメーターの既定値は true です。

## <a name="method-typeflush"></a>メソッド typeFlush

拡張データ型を更新します。

```xpp
public void typeFlush()
```

## <a name="method-configurationkeyflush"></a>メソッド configurationKeyFlush

コンフィギュレーション キーを更新します。

```xpp
public void configurationKeyFlush()
```

## <a name="method-licensecodeflush"></a>メソッド licenseCodeFlush

ライセンス コードを更新します。

```xpp
public void licenseCodeFlush()
```

## <a name="method-aodflush"></a>メソッド aodFlush

.aod ファイルを更新します。

```xpp
public static void aodFlush()
```

