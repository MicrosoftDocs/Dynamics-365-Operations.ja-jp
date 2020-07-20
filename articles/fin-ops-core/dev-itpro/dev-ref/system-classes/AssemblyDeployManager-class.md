---
title: AssemblyDeployManager クラス
description: このトピックでは、AssemblyDeployManager クラスについて説明します。
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
ms.openlocfilehash: d14751886e3ec17c02eec898927743bdcac281a7
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502724"
---
# <a name="class-assemblydeploymanager"></a>クラス AssemblyDeployManager

[!include [banner](../../includes/banner.md)]

```xpp
class AssemblyDeployManager extends Object
```

AssemblyDeployManager クラスを使用すると、.NET 呼び出し時に X++ ランタイムによって使用できる AOS VSAssemblies フォルダーに、AOT Visual Studio プロジェクトに格納されているアセンブリを展開することができます。

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>方法

| 方法                                                        | 説明                                                                                             |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| ::public static boolean isHotswappingEnabled()                | ホット スワップが有効かどうかを示すブール値を返します。                                 |
| ::public static void deployAssemblyFromPath(str assemblyPath) |                                                                                                         |
| ::public static void removeAssemblyFromPath(str assemblyPath) | サーバーへの配置用にマークされた特定のアセンブリを VSAssemblies フォルダーから削除します。 |
| ::public static void deployAssemblies()                       | サーバーへの配置用にマークされた特定のアセンブリを VSAssemblies フォルダーに展開します。       |

## <a name="method-ishotswappingenabled"></a>メソッド isHotswappingEnabled

ホット スワップが有効かどうかを示すブール値を返します。

```xpp
public static boolean isHotswappingEnabled()
```

### <a name="return-value---ishotswappingenabled"></a>戻り値 - isHotswappingEnabled

ホット スワップが有効かどうかを示すブール値。

## <a name="method-deployassemblyfrompath"></a>メソッド deployAssemblyFromPath

```xpp
public static void deployAssemblyFromPath(str assemblyPath)
```

### <a name="parameters---deployassemblyfrompath"></a>パラメーター - deployAssemblyFromPath

assemblyPath  

## <a name="method-removeassemblyfrompath"></a>メソッド removeAssemblyFromPath

サーバーへの配置用にマークされた特定のアセンブリを VSAssemblies フォルダーから削除します。

```xpp
public static void removeAssemblyFromPath(str assemblyPath)
```

### <a name="parameters---removeassemblyfrompath"></a>パラメーター - removeAssemblyFromPath

assemblyPath  
アセンブリが格納されている Visual Studio プロジェクト パス。

## <a name="method-deployassemblies"></a>メソッド deployAssemblies

サーバーへの配置用にマークされた特定のアセンブリを VSAssemblies フォルダーに展開します。

```xpp
public static void deployAssemblies()
```

