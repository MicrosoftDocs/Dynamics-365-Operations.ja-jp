---
title: X++ イベントの用語およびキーワード
description: このトピックでは、X++ のイベント用語とキーワードについて説明します。
author: robinarh
manager: AnnBe
ms.date: 06/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 150303
ms.assetid: 1b2d76d1-52d9-46b2-937f-5a3b62f2d516
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4c45b319504fcf68eff281e303464fab80f02f7c
ms.sourcegitcommit: 7eae20185944ff7394531173490a286a61092323
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/03/2019
ms.locfileid: "2872648"
---
# <a name="x-event-terminology-and-keywords"></a>X++ イベントの用語およびキーワード

[!include [banner](../includes/banner.md)]

このトピックでは、X++ のイベント用語とキーワードについて説明します。 

イベント設計パターンを使用すると、コードをさらにモジュール化して再使用可能にすることができます。 *イベント* という用語は、デリゲートの使用方法を説明するメタファです。 プログラム実行中に何か重要なことが発生したときは、他のモジュールがその発生を処理することが必要な場合があります。 これらの重要な出来事は*イベント*と呼ばれています。 イベントが発生すると、プログラムは、Notifier がイベントに関する通知を送信する必要があることを、そのイベントの Notifier に指示します。 通知は、通知のサブスクライバーであるすべてのイベント ハンドラーに送信する必要があります。 プログラムがその通知機能に通知を送信するように指示するとき、そのプロセスをイベントの *発生* と呼んでいます。 

次のテーブルは、イベント メタファを説明するために使用される用語を示しています。

| 期間          | 説明                                                 |
|---------------|-------------------------------------------------------------|
| イベント         | 追加モジュールは発生を処理するプログラム モジュールで重要な発生です。    |
| 通知機能      | 通知機能に登録されているすべてのイベント ハンドラーに、イベントに関する情報を送信するプログラム要素。 |
| サブスクライバー    | イベント通知機能を登録しているプログラム機能またはメソッド。                          |
| イベント ハンドラー | イベント通知を購読するメソッド。 適切な種類のメソッドのみ、イベント ハンドラーになることができます。  |

## <a name="keywords-that-are-used-for-programming-that-uses-delegates"></a>デリゲートを使用するプログラミングに使用されるキーワード

次のテーブルに、デリゲートの使用方法を説明するキーワードを示します。

| キーワードや用語           | 区分      | 説明           |
|---------------------------|-----------|-----------------------|
| デリゲート                                | `delegate myDelegate(str information) {}`                                | このコードは、コード エディターでのデリゲートの外観を示しています。 戻り値の型は常に**無効**なので、構文には示されていません。 かっこ ({}) 内にコードは使用できません。                                                               |
| eventHandler                            | `myClassInstance.myDelegate += eventHandler(otherClass.myInstanceMethod);` | **eventHandler** キーワードの構文は **eventHandler** X++ 関数であるという印象を与えますが、それは関数ではありません。 **eventHandler** キーワードは、メソッドがデリゲートにサブスクライブされることをコンパイラに伝えます。         |
| デリゲートにメソッドをサブスクライブまたは追加 | `myClassInstance.myDelegate += eventHandler(OtherClass::aStaticMethod);`   | コードでは、静的メソッド **OtherClass::aStaticMethod** がデリゲートにサブスクライブされます。              |
| デリゲートの呼び出し                         | `myClassInstance.myDelegate("Hello");`                                     | デリゲートへのこの呼び出しは、デリゲートにサブスクライブしている各メソッドを呼び出すようにデリゲートに要求します。 サブスクライブされたメソッドは、デリゲートに追加されたのと同じ順序で呼び出されます。 1 つのサブスクライブされたメソッドは、そのデリゲードが次のメソッドを呼び出す前に完了される必要があります。 |

## <a name="example"></a>例

次のコード例の 2 つのクラスは、イベントの定義方法、イベントのサブスクライブ方法、およびイベントを発生させる方法を示しています。 **PointWithEvent** クラスは、**移動** されたデリゲートを定義します。 **移動** メソッドは、**移動** されたデリゲートを呼び出し、その結果、イベントをサブスクライブしているすべてのオブジェクトに通知します。 **PointKeeper** クラスは、**writeMove** メソッドを定義し、そのメソッドを、**createandmove** メソッドで作成された **ポイント** インスタンスの **移動** されたデリゲートのイベント ハンドラーとして割り当てます。 

```xpp
class PointWithEvent
{
    // Instance fields.
    real x;
    real y;

    // Constructor to initialize fields x and y.
    void new(real _x, real _y)
    {
        x = _x;
        y = _y;
    }

    void move(real x_offset, real y_offset)
    {
        x += x_offset;
        y += y_offset;
        this.moved(abs(x_offset) + abs(y_offset));
    }

    delegate void moved(real distance)
    {
    }

}

class PointKeeper
{

    public void createAndMove()
    {
        PointWithEvent point = new PointWithEvent(1.0, 2.0);

        point.moved += eventhandler(this.writeMove);

        point.move(4.0, 5.0);
        // Output is "9.0".
    }

    public void writeMove(real distance)
    {
        info(any2Str(distance));
    }

}
```
