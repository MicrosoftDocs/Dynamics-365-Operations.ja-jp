---
title: バージョン管理で使用されるテーブル マップの拡張
description: このトピックでは、バージョン管理に使用できるテーブル マップを拡張する方法について説明します。
author: LarsBlaaberg
manager: AnnBe
ms.date: 12/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 89563
ms.assetid: ''
ms.search.region: Global
ms.author: lolsen
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 11
ms.openlocfilehash: f03c5b687504f81cb6c57927e68de5df1f6a0701
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408840"
---
# <a name="extend-table-maps-that-are-used-for-versioning"></a>バージョン管理で使用されるテーブル マップの拡張

[!include [banner](../includes/banner.md)]

## <a name="purchlinemap-table-map-logic"></a>PurchLineMap テーブル マップ ロジック

テーブル拡張機能を使用して新しいフィールドが **PurchLine** および **PurchLineHistory** テーブルに追加された場合、発注書のバージョンが更新されるときに、新しいフィールドをテーブル間でコピーする必要があります。 **PurchLineMap** テーブル マップは、新しい購買注文バージョンが作成または編集されたときに **PurchLine** テーブルおよび **PurchLineHistory** テーブルの間でコピーする必要があるフィールドを指定します。 これを行うためには、**PurchLineMap** マップ テーブルを拡張してフィールドを追加します。 また、**PurchLineMap** は、購買注文明細行をアーカイブするとき、**VersioningPurchaseOrder** によって使用されます。 このモデルを次の図に示します。

![VersioningPurchaseOrder](media/MapsWithVersioning1.png)

コピーする新しいフィールドを指定できるようにするため、**PurchLineMap** テーブル マップ ロジックとその使用がリファクタリングされています。 コピー ロジックが **PurchLineVersioning** 移動されているため、**VersioningPurchaseOrder** クラスは **PurchLineMap** テーブルマップの代わりに、**PurchLineVersioning** を参照します。 **PurchLineVersioning** クラスは、フィールドをコピーするロジックや、**PurchLineIVersioningFieldSet** インターフェイス を実行するクラスからの確認が必須かどうかを決定するロジックを委任します。 インターフェイスを実装する各クラスは、コピーするフィールドを指定するテーブル マップに関連付けられます。

**PurchLineDictVersioning** クラスは、リフレクションを使用して **PurchLineIVersioningFieldSet** オブジェクトをインスタンス化します。 **PurchLineDictVersioning** クラスは、コピーする必要があるフィールドのセット全体を収集します。 フィールドデータは、**PurchLineIVersioningFieldSet** を実装するクラスに関連付けられているすべてのテーブル マップに基づいて収集されます。 次の図は、新しいクラスとその依存関係を示しています。

![ソリューション](media/MapsWithVersioning2.png)

## <a name="how-to-extend-purchline-and-purchlinehistory-tables-with-new-fields"></a>新しいフィールドで PurchLine および PurchLineHistory テーブルを拡張する方法

発注書の新しいバージョンを作成するときにコピーする必要がある新しいフィールドを持つ **PurchLine** および **PurchLineHistory** テーブルを拡張するために、ISVModule2 モデルが必要であるとします。 

> [!NOTE] 
> ISVModule2 モデルに開発者がアクセスできる必要があります。 

このタスクを完了するには、次の手順を実行する必要があります。
1. **PurchLine** と **PurchLineHistory** テーブルへのテーブル拡張機能を使用して、フィールドを追加します。
2. コピーする必要があるフィールドを含む新しいテーブル マップを作成し、2 つの新しいテーブル拡張で新しいテーブル マップを実装します。
3. 新しいクラスを作成して **PurchLineIVersioningFieldSet** インターフェースを実装し、以下の必須メソッドを実装します。
    - **copyVersion** メソッド - 新しいテーブル マップの 2 つのレコード間でデータをコピーをします。
    - **fieldSetTableMapId** メソッド - は新しいテーブルマップの ID を返します。
    - **isChangeConfirmationRequired** メソッド - 新しく追加されたフィールド値が必要とする作成された確認への変更に基づいて、true または false を返します。

これらの手順で説明するクラス、インターフェイス、および拡張機能を次の図に示します。

![MapClassExtensions](media/TableMaps.png)

