---
title: 詳細のクラス
description: このトピックでは、詳細のクラスに関する情報を提供します。
author: MichaelFruergaardPontoppidan
manager: AnnBe
ms.date: 03/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: MichaelFruergaardPontoppidan
ms.search.validFrom: 2018-XX-XX
ms.dyn365.ops.version: App Update 10.0.2
ms.openlocfilehash: 696834d934f10d9e9040466044d2692085dd729a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183094"
---
# <a name="specification-classes"></a>詳細のクラス

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

詳細のクラスはエンティティが満たすべき一連の条件の定義に使用される Fluent アプリケーション プログラミング インターフェイス (API) を提供します。 詳細は検証シナリオでよく使用されます。 通常それらはクエリ クラスと一緒に使用されます。

詳細のクラスの利点は、検証コードが非常に簡潔で表現的になることです。 基本的に 1 行のコードで複数の検証を行えます。

## <a name="naming-convention"></a>名前付け規則

`AtlSpec<ModuleName><#EntityName>`

この命名規則で:

- `<ModuleName>` はオプションで、メイン メニューのモジュール名に基づいています。 ただし、短いテスト コードをサポートするために、短いバージョンまたは省略形を使用する必要があります。
- `<#EntityName>` は承認テスト ライブラリ (ATL) 全体で使用されるエンティティ名を表します。

## <a name="examples"></a>例

```
AtlSpecWHSLoadLine

AtlSpecWHSWorkLine
```

## <a name="implementation"></a>実装

詳細のクラスは仕様のさまざまな条件を指定する Fluent セッター メソッドを提供する必要があります。

### <a name="example"></a>例

次のコードは、指定された条件を満たす 6 行が作業に含まれることを確認します。 たとえば、1 行目は **1** の行番号として **1** を、作業タイプとして **ピッキング** を、数量として **1** を、状態として **終了済み** を、場所として **一括** を持っている必要があります。

```
work.lines().assertExpectedLines(
    workLines.spec().withLineNum(1).withWorkType(WHSWorkType::Pick).setQuantity(1).setStatus(WHSWorkStatus::Closed).setLocation(locations.bulk()),
    workLines.spec().withLineNum(2).withWorkType(WHSWorkType::Pick).setQuantity(1).setStatus(WHSWorkStatus::Closed).setLocation(locations.floor()),
    workLines.spec().withLineNum(3).withWorkType(WHSWorkType::Put) .setQuantity(2).setStatus(WHSWorkStatus::Closed).setLocation(locations.stage()),
    workLines.spec().withLineNum(4).withWorkType(WHSWorkType::Pick).setQuantity(2).setStatus(WHSWorkStatus::Cancelled).setLocation(locations.stage()),
    workLines.spec().withLineNum(5).withWorkType(WHSWorkType::Put).setQuantity(2).setStatus(WHSWorkStatus::Cancelled)
);
```
