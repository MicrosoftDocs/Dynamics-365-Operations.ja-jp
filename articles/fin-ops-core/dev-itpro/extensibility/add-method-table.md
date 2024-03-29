---
title: 拡張機能を使用してテーブルにメソッドを追加
description: この記事では、拡張機能を使用してテーブルにメソッドを追加する方法について説明します。
author: ivanv-microsoft
ms.date: 10/22/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 4
ms.custom: 268724
ms.assetid: ''
ms.openlocfilehash: 3c4728b8b00d09d8eefafd73d3fcdc60509004d5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270983"
---
# <a name="add-methods-to-tables-through-extension"></a>拡張機能を使用してテーブルにメソッドを追加

[!include [banner](../includes/banner.md)]

テーブルに関連付けられているビジネス ロジックを拡張するとき、コードをクリーンに維持するために役立つ一般的なコーディング原則はまだ適用されます。 したがって、最終的にアクションをテーブルの別々のメソッドにカプセル化する必要があります。 Microsoft Dynamics AX 2012 では、オーバーレイ経由でテーブルに直接メソッドを追加することによってそのタスクを完了していました。 拡張を使用して同じタスクを完了するには、別の方法を使用します。 具体的には、拡張クラスを作成します。

たとえば、**MyInventLocationId** という名前新しいフィールドが、拡張機能によって InventTable テーブルに追加されました。 **挿入** イベント用のデータ イベント ハンドラーも作成されました。新しいフィールドに入力するロジックを実装する必要があります。 そのアクションをカプセル化するには、InventTable で新しいメソッドを作成し、そのメソッドに **myDefaultInventLocationId** という名前を付けます。

最初に、拡張モデルに新しいクラスを作成します。 このクラスは InventTable テーブルを拡張し、読みやすく理解しやすい方法でテーブルのフィールドとメソッドにアクセスできるようにします 強化クラスに正しい名前を選択することが重要です。 この名前は、展開されるすべてのモデルのすべてのタイプにわたって一意でなければなりません。 詳細については、[拡張機能の名前付けのガイドライン](naming-guidelines-extensions.md) を参照してください。

```xpp
[ExtensionOf(tableStr(InventTable))]
final class InventTableMy_Extension
{
    public void myDefaultInventLocationId()
    {
        // This would have partner specific logic to initialize the new field.
        this.MyInventLocationId = this.inventLocationId();
    }
}
```

新しいメソッドを強化クラスを追加することができるようになりました。 これらのメソッドは、テーブルに直接定義されているかのように、**InventTable** 型の変数の IntelliSense に表示されます。 この動作は、静的メソッドとインスタンス メソッドの両方に適用されます。

拡張クラスにはいくつかのルールがあります。

+ 最終である必要があります。
+ **\_拡張子** で接尾辞を付ける必要があります。
+ **[ExtensionOf()]** 属性で装飾されている必要があります。

たとえば、イベント ハンドラーから新しいメソッドを使用できるようになります。

```xpp
class InventTableMy_EventHandler
{
    [DataEventHandler(tableStr(InventTable), DataEventType::Inserting)]
    public static void InventTable_onInserting(Common sender, DataEventArgs e)
    {
        InventTable inventTable = sender as InventTable;
        // Call the method as if it was defined directly on InventTable.
        inventTable.myDefaultInventLocationId();
    }
}

```

> [!NOTE]
> イベント ハンドラー クラスには任意の数のイベントのハンドラーが含まれるのが一般的です。 ただし、イベント ハンドラーを拡張クラスに入れるのは、良い方法では **ありません**。 そうすることで、イベント ハンドラー メソッドが拡張されたタイプのメソッドとして使用可能となります。 これは、イベント ハンドラーが、その型のメソッドとして明示的にではなく、イベントを通じて呼び出されることを意図しているので正しくありません。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
