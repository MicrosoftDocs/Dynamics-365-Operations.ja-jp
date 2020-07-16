---
title: SecureNode クラス
description: このトピックでは、SecureNode クラスについて説明します。
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
ms.openlocfilehash: 8b0f2f5afc8b1e892b7814460d19781191304006
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502815"
---
# <a name="class-securenode"></a>クラス SecureNode

[!include [banner](../../includes/banner.md)]

```xpp
class SecureNode extends TreeNode
```

SecureNode クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

## <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                          | 説明                                                             |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| public boolean checkAccessRights()                                              |                                                                         |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])        | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。     |
| public ConfigurationKeyId countryConfigurationkey(\[ConfigurationKeyId value\]) |                                                                         |
| public boolean extendedDataSecurity(\[boolean value\])                          |                                                                         |
| public boolean isWeb()                                                          |                                                                         |
| public int neededAccessLevel(\[int value\])                                     | MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。 |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                       |                                                                         |
| public ConfigurationKeyId webConfigurationkey(\[ConfigurationKeyId value\])     |                                                                         |

## <a name="method-checkaccessrights"></a>メソッド checkAccessRights

```xpp
public boolean checkAccessRights()
```

### <a name="return-value---checkaccessrights"></a>戻り値 - checkAccessRights

## <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a>パラメーター - configurationKey

値  

### <a name="return-value---configurationkey"></a>戻り値 - configurationKey

コントロールに割り当てられるコンフィギュレーションの ID。

### <a name="remarks---configurationkey"></a>備考 - configurationKey

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

## <a name="method-countryconfigurationkey"></a>メソッド countryConfigurationkey

```xpp
public ConfigurationKeyId countryConfigurationkey([ConfigurationKeyId value])
```

### <a name="parameters---countryconfigurationkey"></a>パラメーター - countryConfigurationkey

値  

### <a name="return-value---countryconfigurationkey"></a>戻り値 - countryConfigurationkey

## <a name="method-extendeddatasecurity"></a>メソッド extendedDataSecurity

```xpp
public boolean extendedDataSecurity([boolean value])
```

### <a name="parameters---extendeddatasecurity"></a>パラメーター - extendedDataSecurity

値  

### <a name="return-value---extendeddatasecurity"></a>戻り値 - extendedDataSecurity

## <a name="method-isweb"></a>メソッド isWeb

```xpp
public boolean isWeb()
```

### <a name="return-value---isweb"></a>戻り値 - isWeb

## <a name="method-neededaccesslevel"></a>メソッド neededAccessLevel

MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。

```xpp
public int neededAccessLevel([int value])
```

### <a name="parameters---neededaccesslevel"></a>パラメーター - neededAccessLevel

値  

### <a name="return-value---neededaccesslevel"></a>戻り値 - neededAccessLevel

neededAccessLevel プロパティの現在の値。

### <a name="remarks---neededaccesslevel"></a>備考 - neededAccessLevel

AccessType システム列挙値の使用可能な値は次のとおりです。

-   AccessType::NoAccess。
-   AccessType::View。
-   AccessType::Edit。
-   AccessType::Add。
-   AccessType::Delete。

## <a name="method-securitykey"></a>メソッド securityKey

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a>パラメーター - securityKey

値  

### <a name="return-value---securitykey"></a>戻り値 - securityKey

## <a name="method-webconfigurationkey"></a>メソッド webConfigurationkey

```xpp
public ConfigurationKeyId webConfigurationkey([ConfigurationKeyId value])
```

### <a name="parameters---webconfigurationkey"></a>パラメーター - webConfigurationkey

値  

### <a name="return-value---webconfigurationkey"></a>戻り値 - webConfigurationkey

