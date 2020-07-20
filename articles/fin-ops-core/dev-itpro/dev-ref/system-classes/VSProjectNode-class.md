---
title: VSProjectNode クラス
description: このトピックでは、VSProjectNode クラスについて説明します。
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
ms.openlocfilehash: 5f80602b19a9cf2f2489000d8c2ee3bbf9d24cf8
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502693"
---
# <a name="class-vsprojectnode"></a>クラス VSProjectNode

[!include [banner](../../includes/banner.md)]

```xpp
class VSProjectNode extends xResourceNode
```

VSProjectNode クラスは、アプリケーション オブジェクト ツリー (AOT) 内の Microsoft Visual Studio プロジェクト ノードでプロジェクトを表します。

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                | 説明                                                                                       |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| public container extract(\[str path\], \[boolean extractReferenced\]) | ディスクにプロジェクト全体を展開します。                                                               |
| public VSProjectFolderNode getContentNode()                           | Visual Studio プロジェクト ファイルを含むコンテンツの VSProjectFolderNode オブジェクトを取得します。        |
| public DeployTo getDeployTo()                                         | deployTo プロパティの値を取得します。                                                              |
| public VSProjectFolderNode getOutputNode()                            | Visual Studio プロジェクト出力ファイルを含む、出力 VSProjectFolderNode オブジェクトを取得します。  |
| public VSProjectFileNode getPrimaryOutputNode()                       | Visual Studio プロジェクトの基本出力を表す VSProjectFileNode オブジェクトを取得します。 |
| public str getPrimaryTargetFileName()                                 | Visual Studio プロジェクトのプライマリ ターゲット ファイル名を取得します。                                   |
| public Map getProxies()                                               | このプロジェクトでのプロキシを取得します。                                                                 |
| public container getProxiesContainer()                                | このプロジェクトでのプロキシを取得します。                                                                 |
| public str getReferencedProjectsInAOT()                               | この Visual Studio プロジェクトで参照されているプロジェクトの AOT パスを取得します。             |
| public str referencedProjects(\[str value\])                          |                                                                                                   |
| public void setPrimaryTargetFileName(str targetFileName)              | Visual Studio プロジェクトのプライマリ ターゲット ファイル名を設定します。                                   |
| public void extractToSpecificDir(str directory)                       |                                                                                                   |
| public void setDeployTo(DeployTo deployTo)                            | deployTo プロパティの値を設定します。                                                          |

## <a name="method-extract"></a>メソッド extract

ディスクにプロジェクト全体を展開します。

```xpp
public container extract([str path], [boolean extractReferenced])
```

### <a name="parameters---extract"></a>パラメーター - extract

path  
参照されるプロジェクトを抽出するかどうかを決定するブール値。

<!-- -->

extractReferenced  
参照されるプロジェクトを抽出するかどうかを決定するブール値。

### <a name="return-value---extract"></a>戻り値 - extract

プロジェクトの展開先のパスの一覧。

## <a name="method-getcontentnode"></a>メソッド getContentNode

Visual Studio プロジェクト ファイルを含むコンテンツの VSProjectFolderNode オブジェクトを取得します。

```xpp
public VSProjectFolderNode getContentNode()
```

### <a name="return-value---getcontentnode"></a>戻り値 - getContentNode

Visual Studio プロジェクト ファイルを含むコンテンツの VSProjectFolderNode オブジェクト。

## <a name="method-getdeployto"></a>メソッド getDeployTo

deployTo プロパティの値を取得します。

```xpp
public DeployTo getDeployTo()
```

### <a name="return-value---getdeployto"></a>戻り値 - getDeployTo

deployTo プロパティ値。

## <a name="method-getoutputnode"></a>メソッド getOutputNode

Visual Studio プロジェクト出力ファイルを含む、出力 VSProjectFolderNode オブジェクトを取得します。

```xpp
public VSProjectFolderNode getOutputNode()
```

### <a name="return-value---getoutputnode"></a>戻り値 - getOutputNode

Visual Studio プロジェクト出力ファイルを含む、出力 VSProjectFolderNode オブジェクト。

## <a name="method-getprimaryoutputnode"></a>メソッド getPrimaryOutputNode

Visual Studio プロジェクトの基本出力を表す VSProjectFileNode オブジェクトを取得します。

```xpp
public VSProjectFileNode getPrimaryOutputNode()
```

### <a name="return-value---getprimaryoutputnode"></a>戻り値 - getPrimaryOutputNode

Visual Studio プロジェクトの基本出力を表す VSProjectFileNode オブジェクト。

## <a name="method-getprimarytargetfilename"></a>メソッド getPrimaryTargetFileName

Visual Studio プロジェクトのプライマリ ターゲット ファイル名を取得します。

```xpp
public str getPrimaryTargetFileName()
```

### <a name="return-value---getprimarytargetfilename"></a>戻り値 - getPrimaryTargetFileName

Visual Studio プロジェクトのプライマリ ターゲット ファイル名。

## <a name="method-getproxies"></a>メソッド getProxies

このプロジェクトでのプロキシを取得します。

```xpp
public Map getProxies()
```

### <a name="return-value---getproxies"></a>戻り値 - getProxies

クラス、列挙、およびテーブルのキーを含むマップ。 各キーには、プロキシのリストが含まれています。

## <a name="method-getproxiescontainer"></a>メソッド getProxiesContainer

このプロジェクトでのプロキシを取得します。

```xpp
public container getProxiesContainer()
```

### <a name="return-value---getproxiescontainer"></a>戻り値 - getProxiesContainer

マップの梱包済み表現を保持するコンテナーには、Class、Enum、Table のキーが含まれています。 各キーには、プロキシのリストが含まれています。

## <a name="method-getreferencedprojectsinaot"></a>メソッド getReferencedProjectsInAOT

この Visual Studio プロジェクトで参照されているプロジェクトの AOT パスを取得します。

```xpp
public str getReferencedProjectsInAOT()
```

### <a name="return-value---getreferencedprojectsinaot"></a>戻り値 - getReferencedProjectsInAOT

この Visual Studio プロジェクトで参照されているプロジェクトの AOT パスの一覧。

## <a name="method-referencedprojects"></a>メソッド referencedProjects

```xpp
public str referencedProjects([str value])
```

### <a name="parameters---referencedprojects"></a>パラメーター - referencedProjects

値  

### <a name="return-value---referencedprojects"></a>戻り値 - referencedProjects

## <a name="method-setprimarytargetfilename"></a>メソッド setPrimaryTargetFileName

Visual Studio プロジェクトのプライマリ ターゲット ファイル名を設定します。

```xpp
public void setPrimaryTargetFileName(str targetFileName)
```

### <a name="parameters---setprimarytargetfilename"></a>パラメーター - setPrimaryTargetFileName

targetFileName  
Visual Studio プロジェクトのプライマリ ターゲット ファイル名。

## <a name="method-extracttospecificdir"></a>メソッド extractToSpecificDir

```xpp
public void extractToSpecificDir(str directory)
```

### <a name="parameters---extracttospecificdir"></a>パラメーター - extractToSpecificDir

directory  

## <a name="method-setdeployto"></a>メソッド setDeployTo

deployTo プロパティの値を設定します。

```xpp
public void setDeployTo(DeployTo deployTo)
```

### <a name="parameters---setdeployto"></a>パラメーター - setDeployTo

deployTo  
deployTo プロパティ値。

