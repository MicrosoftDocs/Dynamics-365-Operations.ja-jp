---
title: イベントと代表者
description: この記事では、X++ のイベント用語とキーワードについて説明します。
author: tonyafehr
ms.date: 08/27/2021
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2adcf191a1d475989ccbb5c3a1529ce08b6e23de
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867171"
---
# <a name="events-and-delegates"></a>イベントと代表者

[!include [banner](../includes/banner.md)]

この記事では、X++ のイベント用語とキーワードについて説明します。

イベント設計パターンを使用すると、コードをさらにモジュール化して再使用可能にすることができます。 *イベント* という用語は、デリゲートの使用方法を説明するメタファです。 プログラム実行中に何か重要なことが発生したときは、他のモジュールがその発生を処理することが必要な場合があります。 これらの重要な出来事は *イベント* と呼ばれています。 イベントが発生すると、プログラムは、Notifier がイベントに関する通知を送信する必要があることを、そのイベントの Notifier に指示します。 通知は、通知のサブスクライバーであるすべてのイベント ハンドラーに送信する必要があります。 プログラムがその通知機能に通知を送信するように指示するとき、そのプロセスをイベントの *発生* と呼んでいます。

デリゲートはクラスにだけでなく、テーブル、フォーム、またはクエリで定義できます。

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
| デリゲート                                | `delegate myDelegate(str information) {}`                                | このコードは、コード エディターでのデリゲートの外観を示しています。 戻り値の型は常に **無効** なので、構文には示されていません。 かっこ ({}) 内にコードは使用できません。                                                               |
| eventHandler                            | `myClassInstance.myDelegate += eventHandler(otherClass.myInstanceMethod);` | **eventHandler** キーワードの構文は **eventHandler** X++ 関数であるという印象を与えますが、それは関数ではありません。 **eventHandler** キーワードは、メソッドがデリゲートにサブスクライブされることをコンパイラに伝えます。         |
| デリゲートにメソッドをサブスクライブまたは追加 | `myClassInstance.myDelegate += eventHandler(OtherClass::aStaticMethod);`   | コードでは、静的メソッド **OtherClass::aStaticMethod** がデリゲートにサブスクライブされます。              |
| デリゲートの呼び出し                         | `myClassInstance.myDelegate("Hello");`                                     | デリゲートへのこの呼び出しは、デリゲートにサブスクライブしている各メソッドを呼び出すようにデリゲートに要求します。 サブスクライブされたメソッドは、デリゲートに追加されたのと同じ順序で呼び出されます。 1 つのサブスクライブされたメソッドは、そのデリゲードが次のメソッドを呼び出す前に完了される必要があります。 |

## <a name="example"></a>例

次のコード例の 2 つのクラスは、イベントの定義方法、イベントのサブスクライブ方法、およびイベントを発生させる方法を示しています。 **PointWithEvent** クラスは、**移動** されたデリゲートを定義します。 **move** メソッドは **moved** デリゲートを呼び出し、イベントにサブスクライブした任意のオブジェクトに通知します。 **PointKeeper** クラスは、**writeMove** メソッドを定義し、そのメソッドを、**createandmove** メソッドで作成された **ポイント** インスタンスの **移動** されたデリゲートのイベント ハンドラーとして割り当てます。

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

## <a name="event-handlers-and-prepost-methods"></a>イベント ハンドラーおよび予備または転記メソッド

旧式 X++ では、特定のメソッドがメソッドの実行前後に実行されるようにメタデータで指定できました。 サブスクリプションが何を呼び出すかに関する情報は、パブリッシャーに記録されていますが、これは環境には役立ちません。 サブスクライバーに SubscribesTo 属性を指定することにより、コードを通じて前後のハンドラーを指定できるようになりました。

### <a name="example-of-pre-and-post-methods"></a>前後メソッドの例

```xpp
[PreHandlerFor(classStr(MyClass2), methodstr(MyClass2, publisher))]
public static void PreHandler(XppPrePostArgs arguments)
{
    int arg = arguments.getArg("i");
}

[PostHandlerFor(classStr(MyClass2), methodstr(MyClass2, publisher))]
public static void PostHandler(XppPrePostArgs arguments)
{
    int arg = arguments.getArg("i");
    int retvalFromMethod = arguments.getReturnValue();
}

public int Publisher(int i)
{
    return 1;
}
```

この例は、Publisher という公開メソッドを示しています。 2 人のサブスクライバーが PreHandlerFor と PostHandlerFor に登録されています。 このコードは、変数と戻り値にアクセスする方法を示しています。

この機能は、アプリケーションコードに代行機能が多くないことから、下位互換性を保つために提供されており、重要なアプリケーション イベントを発行する目的で提供されています。 前後のハンドラーは、パラメーターの追加または変更のため、パラメータータイプの変更ため、メソッドが呼び出されなくなったり、別の状況で呼び出されたりしたために容易に中断する可能があります。 属性はバインディング イベント ハンドラーをデリゲートするためにも使用されます。

```xpp
[SubscribesTo(
    classstr(FMRentalCheckoutProcessor),
    delegatestr(FMRentalCheckoutProcessor, RentalTransactionAboutTobeFinalizedEvent))]
public static void RentalFinalizedEventHandler(
    FMRental rentalrecord, Struct rentalConfirmation)
{
}

    delegate void RentalTransactionAboutTobeFinalizedEvent(
        FMRental fmrentalrecord, struct RentalConfirmation)
{
}
```

この場合、SubscribesTo 属性は、FmRentalCheckoutProcessor.RentalTransactionAboutToBeFinalizedEvent デリゲートが呼び出されたときにメソッド RentalFinalizedEventHandler を呼び出す必要があることを指定します。 パブリッシャーとサブスクライバーの間のバインディングは属性を通じて行われるため、サブスクライバーが呼び出される順序を指定する方法はありません。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
