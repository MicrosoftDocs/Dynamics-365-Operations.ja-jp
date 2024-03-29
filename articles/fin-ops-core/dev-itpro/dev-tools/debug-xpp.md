---
title: Visual Studio で、デバッガーを使用して X++ コードをデバッグする
description: この記事では、Microsoft Visual Studio のデバッグ機能を使用して X++ コードをデバッグする方法について確認します。
author: gianugo
ms.date: 06/20/2017
ms.topic: article
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: gianura
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 23921
ms.assetid: 6be739c0-30da-4f91-97be-a8764fb8078c
ms.openlocfilehash: 84d9aafb553ac40a308ba7804b542399b4b10c36
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271191"
---
# <a name="debug-x-code-by-using-the-debugger-in-visual-studio"></a>Visual Studio で、デバッガーを使用して X++ コードをデバッグする

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Visual Studio のデバッグ機能を使用して X++ コードをデバッグする方法について確認します。

X++ コードをデバッグするには、Microsoft Visual Studio でデバッガを使用します。 このプロセスは、Visual Studio で作成される他のアプリケーションで使用されるプロセスに似ています。 たとえば、コードがブレークポイントで停止するときに、アプリケーションを検証する標準のツールを使用できます。

## <a name="debug-your-code"></a>コードのデバッグ

X++ コードをデバッグするには、次の手順を実行します。

1. Visual Studio で、デバッグする X++ コードを開きます。
2. 停止を実行する行または明細行を検索し、それらの明細行でブレークポイントを設定します。 行にブレークポイントを設定するには、コード エディターの左の列をクリックするか、カーソルがその行にある間に F9 を押します。 赤いドットは、ブレークポイントが設定されていることを示します。

   [![赤い丸。](./media/32_DevoToolsConcept.png)](./media/32_DevoToolsConcept.png)

3. スタートアップ プロジェクトおよびスタートアップ オブジェクトを設定します。 スタートアップ オブジェクトは、任意のフォーム、**main** メソッドを持つ任意のクラス、または任意のメニュー項目にすることができます。 スタートアップ オブジェクトはプロジェクトの **プロパティ** ウィンドウで設定することができます。 または、ソリューション エクスプローラーで要素を右クリックし、その後 **スタートアップ オブジェクトとして設定** をクリックします。

   ![スタートアップ オブジェクトとして設定します。](./media/setasstartupobject.jpg)

4. **デバッグ** メニューで、**デバッグの開始** をクリックします。
5. アプリケーションで、目的のコードを実行させるアクションを実行します。 標準的なアクションには、フォームを開くことが含まれます。 処理は、設定したブレークポイントで停止します。

   [![実行。](./media/33_DevoToolsConcept.png)](./media/33_devotoolsconcept.png)

6. Visual Studio のツールを使用して、アプリケーションを調べます。 たとえば、その値を表示するため、X++ コード内の変数をポイントします。 また、**デバッグ** メニュー上のコマンドを使用してコードを進めることができます。 また、Visual Studio の **Autos** ウィンドウのようなツールは、アプリケーションの状態に関する重要な情報を表示します。

   [![ホバー。](./media/34_DevoToolsConcept.png)](./media/34_devotoolsconcept.png)

   財務と運用アプリケーションに固有の、もう 1 つのツールは情報ログです。 多くの場合、**info()** ステートメントは、アプリケーションの実行中に、ログ ステータス メッセージのコードに追加されます。 これらの情報ログ メッセージは、Visual Studio で直接表示できます。 **表示** メニューで、**情報ログ** をクリックします。

   [![情報ログ。](./media/35_DevoToolsConcept.png)](./media/35_devotoolsconcept.png)

7. アプリケーションのデバッグが終了した後、アプリケーションは終了します。 Visual Studio はデバッグ モードを終了します。

## <a name="add-tostring-methods-to-your-classes"></a>クラスへの ToString メソッドの追加

多くの場合、**ToString** メソッドをクラスに追加することが利点となります。 これを行うのに費やした労力は何度も戻ってきます。それは簡単です。

> [!NOTE]
> ToString メソッドが予期しない時に呼び出されることがあるため、**ToString** メソッドでオブジェクトの状態を変更することはお勧めできません。

## <a name="identify-unselected-fields"></a>選択されていないフィールドの識別

フィールドが **選択** ステートメントのフィールドの一覧に表示されない場合に、テーブルのフィールドを使用することがバグの一般的な発生源となります。 このようなフィールドには、そのタイプに従って既定値が設定されます。 デバッガー ブレークポイントを使用して、値が選択されたかどうかを確認できます。

次のコードを考慮してください。

```xpp
class MyClass
{
    public static void Main(Args a)
    {
        FMRental rental;
        select EndMileage, RentalId from rental;
        rental.Comments = "Something";
    }
}
```

代入ステートメントにブレークポイントを設定します。 クラスをプロジェクトのスタートアップ オブジェクトにして、F5 キーを押して開始します。 ブレークポイントが検出されたときは、**ローカル** ウィンドウで `rental` 変数を展開して表示します。 選択されているフィールドである `EndMileage` と `RentalId` では、選択された値が表示され、選択されていないフィールドには `null` が表示されます。 これは、その値がデータベースからフェッチされなかったことを意味します。 当然、これはデバッグ コンポーネントです。 選択されていないフィールドの値は、フィールドのタイプの規定値になります。 これをステップオーバーし、デバッガーが実際の値のレンダリングをどのように変更するかを確認します。

> [!NOTE]
> テーブルにキャッシュが設定されている場合は、コードで指定されているフィールドリストに関係なく、常にテーブル全体からすべてのフィールドがフェッチされます。

## <a name="the-auto-and-infolog-windows"></a>自動および情報ログ ウィンドウ

デバッガーを使用すると、アプリケーションの状態の特定の部分に簡単にアクセスできます。 この情報は、現在の会社、パーティション、トランザクション レベル、および現在のユーザー ID が一覧表示される **自動** ウィンドウで使用できます。

![自動ウィンドウ。](./media/autos_debugfeatures.png)

また、Infolog に書き込まれるデータを表示するウィンドウもあります。

![情報ログ ウィンドウ。](./media/infolog_debugfeatures.png)

## <a name="breakpoint-features"></a>ブレークポイント機能

Visual Studio デバッガーでは、条件付きブレークポイントと、ヒット カウントによってトリガーされたブレークポイントをサポートします。 また、ブレークポイントをヒットするとき、ユーザーのためにシステムが特定のアクションを実行させることができます。

- **ヒット カウント** を使用することで、デバッガーが実行を中断する前にブレークポイントがヒットする回数を決定できます。 既定では、デバッガーはブレークポイントがヒットするたびに実行を中断します。 ブレークポイントが 2 回ヒットするたび、または 10 回ヒットするたび、または 512 回ヒットするたび、またはユーザーが選択した回数ヒットするたびにデバッガーが中断するよう、ヒット カウントを設定することができます。 一部のバグは、最初にユーザー プログラムがループを実行し、関数を呼び出し、または変数へアクセスする際に現れないため、ヒット数は役に立ちます。 場合によっては、100 回または 1000 回繰り返すまでバグが表示されない可能性があります、 このような問題をデバッグするには、ヒット数が 100 または 1000 のブレークポイントを設定します。
- **条件** は、ブレークポイントがヒットするかスキップするかを決定する式です。 デバッガーは、ブレークポイントに到達すると、条件を評価します。 条件が満たされた場合にのみ、ブレークポイントにヒットします。 場所ブレークポイントを持つ条件を使用して、特定の条件が true の時にのみ指定された場所で停止することができます。 たとえば、勘定残高がマイナスにならないように、銀行決済プログラムをデバッグしているとします。 コード内の特定の場所でブレークポイントを設定し、`balance < 0` 0 などの条件をそれぞれに添付する場合があります。 プログラムを実行するとき、残高が 0 より小さい場合にのみこれらの場所で実行が中断されます。 最初のブレークポイントの位置で変数およびプログラムの状態を調べ、2 つ目のブレークポイントの位置まで実行を続行、などを実行することができます。
- **アクション** は、ブレークポイントがヒットした場合に発生する必要のあるものを指定します。 既定では、デバッガーは実行を中断しますが、代わりにメッセージを印刷するか Visual Studio マクロを実行するかを選択できます。 中断するのではなく、メッセージを印刷する場合は、ブレークポイントは Trace ステートメントと非常に類似します。 このブレークポイントを使用するメソッドはトレース ポイントと呼ばれます。

### <a name="using-breakpoints-with-conditions"></a>条件を伴うブレークポイントの使用

次のコードを考慮してください。

```xpp
class PVsClass
{
    public static void Main(Args a)
    {
        int i;
        for (i = 0; i < 10; i++)
        {
            print i;
        }
    }
}
```

そのステートメントが選択されているときに F9 キーを押すことで、印刷明細書にブレークポイントを設定します。 これにより、通常の無条件ブレークポイントが作成されます。 ここで、マウスを使用して、ブレークポイントのコンテキスト メニューを開き、**条件** を選択します。 "i" 変数が 5 を超えたときにブレークポイントが発生することを示す条件を配置します。 スタートアップ プロジェクトとしてクラスを設定し、プロジェクト内のスタートアップ項目としてコードを含むクラスを設定します。 コードを実行します。 デバッガーを使用して「i」の値を自由に変更してください。 ここで、このブレークポイントを削除し、ヒット カウント機能を使用して同じことを実現します。

> [!NOTE]
> ブレークポイントには、いくつかの条件があります。 多くの場合、ブレークポイントにカーソルを置くと役立つツールヒントが表示されれば便利です。 トレース ポイントは、しばしばトレースの実行に役立ちます。 対象の行に追跡ポイントを挿入し、変数の値を記録します。 トレース出力がデバッガーの出力ウィンドウに表示されます。

## <a name="the-immediate-window"></a>即時ウィンドウ

**即時** ウィンドウは、式とステートメントに入力できるデバッカー機能で、任意の時点で評価できます。 この機能は、X++ stack に実装されません。 ただし、まだ即時ウィンドウから利益を得ることができます。 スニペットは、X++ ではなく、C\# で表示する必用があります。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

