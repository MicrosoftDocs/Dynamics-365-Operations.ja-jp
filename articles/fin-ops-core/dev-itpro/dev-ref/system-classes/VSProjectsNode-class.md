---
title: VSProjectsNode クラス
description: このトピックでは、VSProjectsNode クラスについて説明します。
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
ms.openlocfilehash: a736eab152ed5be142e9e8682cae584629fd2a3a
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502779"
---
# <a name="class-vsprojectsnode"></a>クラス VSProjectsNode

[!include [banner](../../includes/banner.md)]

```xpp
class VSProjectsNode extends xResourceNode
```

VSProjectNode クラスは、アプリケーション オブジェクト ツリー (AOT) 内の Microsoft Visual Studio プロジェクト ノードのルートです。

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                            | 説明                                                                                |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| public TreeNode AOTfindChild(str name, \[int nodeType\])                                          | このノードの指定した子ノードを検索します。                                               |
| public VSProjectNode createProjectNode(str name, str projectTypesString, \[boolean virtualNode\]) | VSProjectNode クラスの新しいインスタンスを作成します。                                         |
| public container getProjectsDeployingTo(DeployTo deployTo)                                        | 指定した deployToプ ロパティを持つ VSProjectNode オブジェクトの一覧を取得します。            |
| public container getProjectsModifiedAfter(DateTime timestamp)                                     | 指定された日時の後に変更された VSProjectNode オブジェクトの一覧を取得します。 |
| public VSProjectTypeNode getTypeNodeFromGuid(str projectTypesString)                              |                                                                                            |
| public Object getVSProjectNodeObservable()                                                        | VSProjectNodeObservable オブジェクトを取得します。                                                   |
| public void AOTrefresh()                                                                          | .aod ファイルを最新版に変更することによりノードを更新します。                                 |

## <a name="method-aotfindchild"></a>メソッド AOTfindChild

このノードの指定した子ノードを検索します。

```xpp
public TreeNode AOTfindChild(str name, [int nodeType])
```

### <a name="parameters---aotfindchild"></a>パラメーター - AOTfindChild

名前  

<!-- -->

nodeType  

### <a name="return-value---aotfindchild"></a>戻り値 - AOTfindChild

指定したツリー ノード。

## <a name="method-createprojectnode"></a>メソッド createProjectNode

VSProjectNode クラスの新しいインスタンスを作成します。

```xpp
public VSProjectNode createProjectNode(str name, str projectTypesString, [boolean virtualNode])
```

### <a name="parameters---createprojectnode"></a>パラメーター - createProjectNode

名前  
ノードがメモリ内でのみ作成されるかどうかを示すブール値。 この場合、ノードは Finance and Operations ストアで保持されません。

<!-- -->

projectTypesString  
ノードがメモリ内でのみ作成されるかどうかを示すブール値。 この場合、ノードは Finance and Operations ストアで保持されません。

<!-- -->

virtualNode  
ノードがメモリ内でのみ作成されるかどうかを示すブール値。 この場合、ノードは Finance and Operations ストアで保持されません。

### <a name="return-value---createprojectnode"></a>戻り値 - createProjectNode

作成された VSProjectNode オブジェクト。

## <a name="method-getprojectsdeployingto"></a>メソッド getProjectsDeployingTo

指定した deployToプ ロパティを持つ VSProjectNode オブジェクトの一覧を取得します。

```xpp
public container getProjectsDeployingTo(DeployTo deployTo)
```

### <a name="parameters---getprojectsdeployingto"></a>パラメーター - getProjectsDeployingTo

deployTo  
deployTo プロパティの値。

### <a name="return-value---getprojectsdeployingto"></a>戻り値 - getProjectsDeployingTo

VSProjectNode オブジェクトの一覧。

## <a name="method-getprojectsmodifiedafter"></a>メソッド getProjectsModifiedAfter

指定された日時の後に変更された VSProjectNode オブジェクトの一覧を取得します。

```xpp
public container getProjectsModifiedAfter(DateTime timestamp)
```

### <a name="parameters---getprojectsmodifiedafter"></a>パラメーター - getProjectsModifiedAfter

timestamp  
DB\_DATETIME\_TYPE 値としての日時。

### <a name="return-value---getprojectsmodifiedafter"></a>戻り値 - getProjectsModifiedAfter

VSProjectNode オブジェクトの一覧。

## <a name="method-gettypenodefromguid"></a>メソッド getTypeNodeFromGuid

```xpp
public VSProjectTypeNode getTypeNodeFromGuid(str projectTypesString)
```

### <a name="parameters---gettypenodefromguid"></a>パラメーター - getTypeNodeFromGuid

projectTypesString  

### <a name="return-value---gettypenodefromguid"></a>戻り値 - getTypeNodeFromGuid

## <a name="method-getvsprojectnodeobservable"></a>メソッド getVSProjectNodeObservable

VSProjectNodeObservable オブジェクトを取得します。

```xpp
public Object getVSProjectNodeObservable()
```

### <a name="return-value---getvsprojectnodeobservable"></a>戻り値 - getVSProjectNodeObservable

VSProjectNodeObservable オブジェクト。

### <a name="remarks---getvsprojectnodeobservable"></a>備考 - getVSProjectNodeObservable

オブザーバーはこれで登録でき、Visual Studio プロジェクトで CRUD 操作の通知を受け取ります。

## <a name="method-aotrefresh"></a>メソッド AOTrefresh

.aod ファイルを最新版に変更することによりノードを更新します。

```xpp
public void AOTrefresh()
```

