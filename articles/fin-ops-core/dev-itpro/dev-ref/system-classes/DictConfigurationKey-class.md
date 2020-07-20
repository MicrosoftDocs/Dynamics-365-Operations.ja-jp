---
title: DictConfigurationKey クラス
description: このトピックでは、DictConfigurationKey クラスについて説明します。
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
ms.openlocfilehash: 197a150a8076ed969254a23cca7e5edce56f9a52
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502993"
---
# <a name="class-dictconfigurationkey"></a>クラス DictConfigurationKey

[!include [banner](../../includes/banner.md)]

```xpp
class DictConfigurationKey extends Object
```

DictConfigurationKey クラスは、コンフィギュレーション キーの情報を提供します。

## <a name="remarks"></a>備考

DictConfigurationKey クラスを使用する例については、新しいメソッドを参照してください。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                     | 説明                                                               |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------|
| public boolean enabled()                                                   | 構成キーが有効かどうかを示す値を返します。  |
| public ConfigurationKeyId id()                                             | コンフィギュレーション キーの ID を返します。                                  |
| public str label()                                                         | コンフィギュレーション キーのラベルを返します。                                |
| public str labelId()                                                       |                                                                           |
| public LicenseCodeId licenseCode()                                         | コンフィギュレーション キーのライセンス コード ID を返します。                    |
| public str name()                                                          | コンフィギュレーション キーの名前を返します。                                |
| public ConfigurationKeyId parentConfigurationKeyId()                       | コンフィギュレーション キーの親コンフィギュレーション キーの ID を返します。 |
| ::public static boolean enabledById(ConfigurationKeyId configurationKeyId) |                                                                           |
| public boolean permanentlyDisabled()                                       |                                                                           |
| public void new(ConfigurationKeyId configurationKeyId)                     | Object クラスの新しいインスタンスを初期化します。                           |

## <a name="method-enabled"></a>メソッド enabled

構成キーが有効かどうかを示す値を返します。

```xpp
public boolean enabled()
```

### <a name="return-value---enabled"></a>戻り値 - enabled

コンフィギュレーション キーが有効である場合は true。それ以外の場合は、false。

### <a name="remarks---enabled"></a>備考 - enabled

このメソッドを使用する例については、新しいメソッドを参照してください。

## <a name="method-id"></a>メソッド id

コンフィギュレーション キーの ID を返します。

```xpp
public ConfigurationKeyId id()
```

### <a name="return-value---id"></a>戻り値 - id

コンフィギュレーション キーの ID。

## <a name="method-label"></a>メソッド label

コンフィギュレーション キーのラベルを返します。

```xpp
public str label()
```

### <a name="return-value---label"></a>戻り値 - label

コンフィギュレーション キーのラベル。コンフィギュレーション キーにラベル値がない場合は空の文字列。

## <a name="method-labelid"></a>メソッド labelId

```xpp
public str labelId()
```

### <a name="return-value---labelid"></a>戻り値 - LabelId

## <a name="method-licensecode"></a>メソッド licenseCode

コンフィギュレーション キーのライセンス コード ID を返します。

```xpp
public LicenseCodeId licenseCode()
```

### <a name="return-value---licensecode"></a>戻り値 - licenseCode

コンフィギュレーション キーのライセンス コード ID。コンフィギュレーション キーにライセンス コードがない場合は 0 (ゼロ)。

## <a name="method-name"></a>メソッド名

コンフィギュレーション キーの名前を返します。

```xpp
public str name()
```

### <a name="return-value---name"></a>戻り値 - name

コンフィギュレーション キーの名前。

### <a name="remarks---name"></a>備考 - name

このメソッドを使用する例については、新しいメソッドを参照してください。

## <a name="method-parentconfigurationkeyid"></a>メソッド parentConfigurationKeyId

コンフィギュレーション キーの親コンフィギュレーション キーの ID を返します。

```xpp
public ConfigurationKeyId parentConfigurationKeyId()
```

### <a name="return-value---parentconfigurationkeyid"></a>戻り値 - parentConfigurationKeyId

親コンフィギュレーション キーの ID。コンフィギュレーション キーに親コンフィギュレーション キーがない場合は 0 (ゼロ)。

## <a name="method-enabledbyid"></a>メソッド enabledById

```xpp
public static boolean enabledById(ConfigurationKeyId configurationKeyId)
```

### <a name="parameters---enabledbyid"></a>パラメーター - enabledById

configurationKeyId  

### <a name="return-value---enabledbyid"></a>戻り値 - enabledById

## <a name="method-permanentlydisabled"></a>メソッド permanentlyDisabled

```xpp
public boolean permanentlyDisabled()
```

### <a name="return-value---permanentlydisabled"></a>戻り値 - permanentlyDisabled

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(ConfigurationKeyId configurationKeyId)
```

### <a name="parameters---new"></a>パラメーター - new

configurationKeyId  
DictConfigurationKey クラスのインスタンスを作成するために使用されるコンフィギュレーション キーの ID。

### <a name="examples---new"></a>例 - new

次の例は、コンフィギュレーション キーの列挙中に DictConfigurationKey クラスの新しいインスタンスを作成する方法を示しています。

```xpp
ConfigurationKeySet configKeySet; 
DictConfigurationKey dictConfigKey; 
str strOutput; 
int i; 
configKeySet = new ConfigurationKeySet(); 
configKeySet.loadSystemSetup(); 
// Output the configuration key names and their enable state. 
for (i=1; i <= configKeySet.cnt(); i++) 
{ 
    dictConfigKey = new DictConfigurationKey(configKeySet.cnt2Id(i)); 
    strOutput = dictConfigKey.enabled() ? "enabled" : "disabled"; 
    strOutput += " " + dictConfigKey.name(); 
    print strOutput; 
}
```

