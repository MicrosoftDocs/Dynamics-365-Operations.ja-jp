---
title: ConfigurationKeySet クラス
description: このトピックでは、ConfigurationKeySet クラスについて説明します。
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
ms.openlocfilehash: 79c7c5942d3d2990bac8bd726981ea30884ab5b8
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502707"
---
# <a name="class-configurationkeyset"></a>クラス ConfigurationKeySet

[!include [banner](../../includes/banner.md)]

```xpp
class ConfigurationKeySet extends Object
```

ConfigurationKeySet クラスでは、コンフィギュレーション キーのツリーを操作できます。

## <a name="remarks"></a>備考

新しい ConfigurationKeySet が作成されるとき、コンフィギュレーション キーのツリーが作成されます。この場合、すべてのキーは既定では「有効」に設定されます。 cnt メソッドは、すべての設定キーをループしてカウントするために使用されます。 cntID メソッドは、設定キーの ID を取得するために使用されます。 コンフィギュレーション キーが削除され、キー ID が ID1、ID2、ID5 などである場合、このメソッドはそれらの ID と比較してコンフィギュレーション キーの数を区別します。 新しい ConfigurationKeySet が作成されるとき、すべてのコンフィギュレーション キーが有効になります。 システムは loadSystemSetup メソッドを呼び出し、構成タイプが格納されている SysConfig テーブルをスキャンします。 コンフィギュレーション キーの設定をループし、有効になっているものを識別します。 次に、有効なメソッドが呼び出されます。 構成キーが無効になるたびに、すべてのサブ構成キーも自動的に無効になります。 トップ ノードが有効でサブノードの 1 つが無効になっている場合、カーネルはトップ ノードが無効になったときに必ずどのコンフィギュレーション キー サブ ノードが以前に無効にされたかを記録します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                            | 説明                                                                                                             |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| public int cnt()                                                                  | アプリケーション オブジェクト ツリー (AOT) で定義されているコンフィギュレーション キーの数を取得します。 |
| public ConfigurationKeyId cnt2Id(int cnt)                                         | *n* 番目のコンフィギュレーション キーの ID を取得します。                                                                        |
| public boolean enabled(ConfigurationKeyId configurationKeyId, \[boolean enable\]) | オブジェクトを有効または無効にするかどうかを決定します。                                                                     |
| public container pack()                                                           | ConfigurationKeySet クラスの現在のインスタンスをシリアル化します。                                                       |
| public boolean touchedByUser(ConfigurationKeyId configurationKeyId)               |                                                                                                                         |
| public void new(\[container container\])                                          | Object クラスの新しいインスタンスを初期化します。                                                                         |
| public void loadSystemSetup()                                                     |                                                                                                                         |

## <a name="method-cnt"></a>メソッド cnt

アプリケーション オブジェクト ツリー (AOT) で定義されているコンフィギュレーション キーの数を取得します。

```xpp
public int cnt()
```

### <a name="return-value---cnt"></a>戻り値 -cnt

AOT で定義されているコンフィギュレーション キーの数。

## <a name="method-cnt2id"></a>メソッド cnt2Id

*n* 番目のコンフィギュレーション キーの ID を取得します。

```xpp
public ConfigurationKeyId cnt2Id(int cnt)
```

### <a name="parameters---cnt2id"></a>パラメーター - cnt2Id

cnt  
コンフィギュレーション キーのインデックス。1 とコンフィギュレーション キーの間でなければなりません。

### <a name="return-value---cnt2id"></a>戻り値 - cnt2Id

指定されたコンフィギュレーション キーの ID。

### <a name="remarks---cnt2id"></a>備考 - cnt2Id

構成キーの数を調べるには、cnt メソッドを使用します。 一般に、すべての ID が使用されているわけではないため、インデックスおよび ID は異なります。

### <a name="examples---cnt2id"></a>例 - cnt2Id

```xpp
ConfigurationKeySet configKeySet = new ConfigurationKeySet(); 
DictConfigurationKey dictConfigurationKey; 
int i; 
```

```xpp
configKeySet.loadSystemSetup(); 
for (i=1; i<= configKeySet.cnt(); i++) 
{ 
    setPrefix('Disabled configurationkeys'); 
    if (!configKeySet.enabled( configKeySet.cnt2Id(i) )) 
    { 
        dictConfigurationKey =  
            new DictConfigurationKey(configKeySet.cnt2id(i)); 
        info (dictConfigurationKey.name()); 
    } 
}
```

## <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

```xpp
public boolean enabled(ConfigurationKeyId configurationKeyId, [boolean enable])
```

### <a name="parameters---enabled"></a>パラメーター - enabled

configurationKeyId  
構成キーの状態を設定する値 (オプション)。

<!-- -->

enable  
構成キーの状態を設定する値 (オプション)。

### <a name="return-value---enabled"></a>戻り値 - enabled

オブジェクトが有効である場合は true。それ以外の場合は、false。

### <a name="remarks---enabled"></a>備考 - enabled

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

### <a name="examples---enabled"></a>例 - enabled

この例では、ConfigurationKeySet.enabled メソッドの使用方法を示します。

```xpp
static void testConfigKey(Args _args) 
{ 
    ConfigurationKeySet configKey = new ConfigurationKeySet(); 
```

```xpp
    configKey.loadSystemSetup(); 
```

```xpp
    // Set the enable value to false. 
    configKey.enabled(configurationkeynum(RouteApprove), false); 
    SysDictConfigurationKey::save(configKey.pack()); 
    SysSecurity::reload(true); 
    print isConfigurationkeyEnabled(configurationkeynum(RouteApprove)); 
```

```xpp
    // Set the enable value to true. 
    configKey.enabled(configurationkeynum(RouteApprove), true); 
    //Save the configuration key setup. 
    SysDictConfigurationKey::save(configKey.pack()); 
    SysSecurity::reload(true); 
```

```xpp
    print isConfigurationkeyEnabled(configurationkeynum(RouteApprove)); 
```

```xpp
    pause; 
}
```

## <a name="method-pack"></a>メソッド pack

ConfigurationKeySet クラスの現在のインスタンスをシリアル化します。

```xpp
public container pack()
```

### <a name="return-value---pack"></a>戻り値 - pack

ConfigurationKeySet クラスの現在のインスタンスを含むコンテナーです。

## <a name="method-touchedbyuser"></a>メソッド touchedByUser

```xpp
public boolean touchedByUser(ConfigurationKeyId configurationKeyId)
```

### <a name="parameters---touchedbyuser"></a>パラメーター - touchedByUser

configurationKeyId  

### <a name="return-value---touchedbyuser"></a>戻り値 - touchedByUser

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new([container container])
```

### <a name="parameters---new"></a>パラメーター - new

コンテナー  

## <a name="method-loadsystemsetup"></a>メソッド loadSystemSetup

```xpp
public void loadSystemSetup()
```

