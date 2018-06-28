---
title: "テーブルへのメソッドの追加"
description: "このトピックでは、拡張機能を使用してテーブルにメソッドを追加する方法について説明します。"
author: ivanv-microsoft
manager: AnnBe
ms.date: 07/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: 
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 4
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 8a0ecb9c6d7df5848bd6f489383be100adf69941
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="add-a-method-to-a-table"></a>テーブルへのメソッドの追加

[!include [banner](../includes/banner.md)]

テーブルに関連付けられているビジネス ロジックを拡張するとき、コードをクリーンに維持するために役立つ一般的なコーディング原則はまだ適用されます。 したがって、最終的にアクションをテーブルの別々のメソッドにカプセル化する必要があります。 Microsoft Dynamics AX 2012 では、オーバーレイ経由でテーブルに直接メソッドを追加することによってそのタスクを完了していました。 拡張を使用して同じタスクを完了するには、別の方法を使用します。 具体的には、拡張クラスを作成します。

たとえば、**MyInventLocationId** という名前新しいフィールドが、拡張機能によって InventTable テーブルに追加されました。 **挿入**イベント用のデータ イベント ハンドラーも作成されました。新しいフィールドに入力するロジックを実装する必要があります。 そのアクションをカプセル化するには、InventTable で新しいメソッドを作成し、そのメソッドに **defaultMyInventLocationId** という名前を付けます。

最初に、拡張モデルに新しいクラスを作成します。 このクラスは InventTable テーブルを拡張し、読みやすく理解しやすい方法でテーブルのフィールドとメソッドにアクセスできるようにします 強化クラスに正しい名前を選択することが重要です。 この名前は、展開されるすべてのモデルのすべてのタイプにわたって一意でなければなりません。 詳細については、[モデル拡張機能の名前付けガイドライン](naming-guidelines-extensions.md) を参照してください。

```
[ExtensionOf(tableStr(InventTable))]
final class MyInventTable_Extension
{
    [DataEventHandler(tableStr(InventTable), DataEventType::Inserting)]
    public static void InventTable_onInserting(Common sender, DataEventArgs e)
    {
        InventTable inventTable = sender as InventTable;
        // Call the method as if it was defined directly on InventTable.
        inventTable.defaultMyInventLocationId();
    }
    public void defaultMyInventLocationId()
    {
        // This would have partner specific logic to initialize the new field.
        this.MyInventLocationId = this.inventLocationId();
    }
}
```

新しいメソッドを強化クラスを追加することができるようになりました。 これらのメソッドは、テーブルに直接定義されているかのように、**InventTable** 型の変数の IntelliSense に表示されます。 この動作は、静的メソッドとインスタンス メソッドの両方に適用されます。

拡張クラスにはいくつかのルールがあります。

+ 最終である必要があります。
+ **\_拡張子**で接尾辞を付ける必要があります。
+ **[ExtensionOf()]** 属性で装飾されている必要があります。

> [!NOTE]
> この例では、データ イベント処理メソッドも強化クラスで定義されます。 実際の実装では、データ イベント処理メソッドを、InventTable テーブルのイベント ハンドラーを含む別のクラスに移動する場合があります。

