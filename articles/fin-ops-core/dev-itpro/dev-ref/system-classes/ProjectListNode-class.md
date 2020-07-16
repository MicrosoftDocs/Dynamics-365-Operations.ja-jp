---
title: ProjectListNode クラス
description: このトピックでは、ProjectListNode クラスについて説明します。
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
ms.openlocfilehash: ae88f94543e15ebfba443cec30739dee8d86c53e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502870"
---
# <a name="class-projectlistnode"></a>クラス ProjectListNode

[!include [banner](../../includes/banner.md)]

```xpp
class ProjectListNode extends TreeNode
```

ProjectListNode クラスは、プロジェクトの概要ウィンドウ内のプロジェクトのプライベートと共有のリストに対応します。 X++ コードから新しいプロジェクトを追加するのにには、ProjectListNode.addProject メソッドを使用します。

## <a name="remarks"></a>備考

このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。 ユーザーがこの API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                               | 説明                     |
|----------------------------------------------------------------------|---------------------------------|
| public ProjectNode addProject(str projectName, \[str projectClass\]) | リストに新しいプロジェクトを追加します。 |

## <a name="method-addproject"></a>メソッド addProject

リストに新しいプロジェクトを追加します。

```xpp
public ProjectNode addProject(str projectName, [str projectClass])
```

### <a name="parameters---addproject"></a>パラメーター - addProject

projectName  
projecttype の名前 (オプション)。 これは、プロジェクトに関連付けられたクラスの名前でなければなりません (setProjectClass メソッドを参照)。 値が指定されていない場合は、標準のプロジェクトがプロジェクトになります。

<!-- -->

projectClass  
projecttype の名前 (オプション)。 これは、プロジェクトに関連付けられたクラスの名前でなければなりません (setProjectClass メソッドを参照)。 値が指定されていない場合は、標準のプロジェクトがプロジェクトになります。

### <a name="return-value---addproject"></a>戻り値 - addProject

新たに追加された projectNode。

