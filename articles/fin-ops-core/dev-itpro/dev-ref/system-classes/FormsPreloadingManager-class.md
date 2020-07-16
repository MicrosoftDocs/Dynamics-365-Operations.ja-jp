---
title: FormsPreloadingManager クラス
description: このトピックでは、FormsPreloadingManager クラスについて説明します。
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
ms.openlocfilehash: 3aa69c2f21366d18c149773306807f96a7dcdd02
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502908"
---
# <a name="class-formspreloadingmanager"></a>クラス FormsPreloadingManager

[!include [banner](../../includes/banner.md)]

```xpp
class FormsPreloadingManager extends Object
```

FormsPreloadingManager クラスは、ワークスペースの関連付けとリソース負荷管理などのフォームのプリロードを管理します。

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>方法

| 方法                                              | 説明                                                                                  |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------|
| ::private static FormsPreloadingManager construct() |                                                                                              |
| public void workspaceActivated()                    | プリロード ワークスペース アフィニティを最後にアクティブ化されたワークスペースに設定します。                      |
| private void new()                                  | FormsPreloadingManager クラスの新しいインスタンスを初期化します。                              |
| public void updateState()                           | 読み込みのためにフォームを照会し、リソース使用率の負荷を処理し、その他の内部の状態を更新します。 |

## <a name="method-construct"></a>メソッド construct

```xpp
private static FormsPreloadingManager construct()
```

### <a name="return-value---construct"></a>戻り値 - construct

## <a name="method-workspaceactivated"></a>メソッド workspaceActivated

プリロード ワークスペース アフィニティを最後にアクティブ化されたワークスペースに設定します。

```xpp
public void workspaceActivated()
```

### <a name="remarks---workspaceactivated"></a>備考 - workspaceActivated

このメソッドは、通常、ワークスペースが有効にされた後にタイマーで呼び出されます。 ワークスペースを変更に対してすぐに親和させるには、このメソッドを直接呼び出します。

## <a name="method-new"></a>メソッド new

FormsPreloadingManager クラスの新しいインスタンスを初期化します。

```xpp
private void new()
```

## <a name="method-updatestate"></a>メソッド updateState

読み込みのためにフォームを照会し、リソース使用率の負荷を処理し、その他の内部の状態を更新します。

```xpp
public void updateState()
```

### <a name="remarks---updatestate"></a>備考 - updateState

このメソッドは、通常アイドル状態のときタイマーで呼び出されます。 実行時間の長い X++ コードが実行されている場合など、非アイドル時に状態を強制的に更新するには、このメソッドを直接呼び出します。

