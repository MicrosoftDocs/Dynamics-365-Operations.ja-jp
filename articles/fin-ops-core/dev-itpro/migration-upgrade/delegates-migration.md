---
title: コードの移行中にデリゲートを使用してモデル間の依存関係の解決
description: このトピックでは、デリゲート インスタンスとデリゲート ハンドラ間でコントラクトを定義する手段としてデリゲート メソッドがどのように機能するかについて説明します。
author: maertenm
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 27001
ms.assetid: 6640ae38-58f0-4a29-abca-5acd9489d45d
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41170e2bbbbbc716cdc1b5fea288c5680edcc0ad
ms.sourcegitcommit: d8a2301eda0e5d0a6244ebbbe4459ab6caa88a95
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029435"
---
# <a name="solve-dependencies-among-models-by-using-delegates-during-code-migration"></a>コードの移行中にデリゲートを使用してモデル間の依存関係の解決

[!include [banner](../includes/banner.md)]

このトピックでは、デリゲート インスタンスとデリゲート ハンドラ間でコントラクトを定義する手段としてデリゲート メソッドがどのように機能するかについて説明します。

<a name="overview"></a>概要
--------

Finance and Operations は、各モデルが個別のパッケージにある、複数のモデルに分割されます。 主要な 3 つのモデルは、アプリケーション プラットフォーム、アプリケーション基盤、アプリケーション スイートです。 モデル分割を使用して、階層が作成されました。ここで上位のモデルは依存関係を持つことができ、下位のモデル内の要素にアクセスできますが、上位のモデルにはアクセスできません。 たとえば、この設定では、アプリケーション スイートはその要素、アプリケーション基盤の要素およびアプリケーション プラットフォームの要素にフル アクセスできます。 アプリケーション基準は、独自の要素とアプリケーション プラットフォームの要素にアクセスできます。 最後に、アプリケーション プラットフォームは独自の要素にのみアクセスできます。 モデルとパッケージについては、 [モデル と パッケージ](../dev-tools/models.md) を参照してください。

[![Del1](./media/del1.jpg)](./media/del1.jpg) 

モデルの分割には多くの利点がありますが、上位モデルで定義された要素にアクセスするとき問題が発生します。 上位モデルの要素に下位モデルからアクセスするに、デリゲートが推奨されています。 デリゲートは、デリゲート インスタンスが呼び出されると、互換性のある署名コードを持つハンドラーが実行されるという点で、イベントと非常によく似ています。 これにより、ハンドラーである上位レイヤーコードが、デリゲート インスタンスである下位レイヤーコード (デリゲート インスタンス) によって呼び出されるようになります。

## <a name="create-delegates-and-handlers"></a>委任およびハンドラーを作成します
デリゲートの宣言には、次の 3 つが必要です。

-   委任キーワード
-   無効タイプ
-   空のメソッド

デリゲート メソッドは、デリゲート インスタンスとデリゲート ハンドラー間のコントラクトを定義する手段として機能します。 デリゲートは、アクション自体を行ないません。 これは、void 型を持ち、メソッドにコードがないことによって適用されます。 

```xpp
delegate void applyDiscountDelegate(real _receiptTotal, EventHandlerResult _result)
{
}
```

メソッドに **SubscribesTo** キーワードを追加して、静的委任ハンドラーを作成します。 **SubscribesTo** にはデリゲートのクラス名、およびデリゲート メソッドの文字列名が必要です。 

デリゲートが適切に処理されるには、デリゲート メソッドの宣言、デリゲート インスタンスおよびデリゲート ハンドラーに*同じ*メソッドの署名が必要です。 たとえば、次に示すデリゲート インスタンスには、2 つの入力が必要です。実数および EventHandlerResult で、上記のデリゲート宣言およびハンドラー署名と一致するものです。 

![static delegate ハンドラー](media/static-delegate-handler.png)

デリゲートに戻り値がないため、EventHandlerResult がパラメーターとして渡され、デリゲートが返された後に必要な結果値にアクセスできるようになります。 このトピックでは、SubscribesTo を使用する静的委任ハンドラーについて説明します。 Dynamics AX 2012 からのデリゲート機能が保持されます。 [Dynamics AX 2012 で X++ デリゲートを使用する方法](https://blogs.msdn.com/b/x/archive/2011/08/02/how-to-use-x-delegates-in-dynamics-ax-2012.aspx) は Dynamics AX 2012 のデリゲートの概念について、Microsoft の開発者 Marcos Calderon が MSDN に投稿した素晴らしいブログです。 これらの概念が引き続き適用されます。

## <a name="example-scenarios"></a>シナリオ例
### <a name="overlaying-an-existing-delegate"></a>既存の委任のオーバーレイ

デリゲートが必要な多くの場合、以前にオーバーレイされたコードは既に Microsoft によってデリゲート ハンドラーに移動されています。 これらのインスタンスで、Microsoft は利用できるデリゲートを作成し、デリゲート ハンドラーで同様の方法でコードをオーバーレイできます。 このシナリオでは、独立系ソフトウェア ベンダー (ISV) が、LogisticsEntityPostalAddressFormHandler クラスで showSalesTax() メソッドをオーバーレイした Dynamics AX 2012 R3 からコードを移行しています。 移行後に、CodeUpgrade プロジェクトは、*Your Solution*、*Microsoft AX 2012*、*Microsoft AX* セクションを使用する LogisticsEntityPostalAddressFormHandler が含まれ、showSalesTax() メソッドを解決します。 コメントされた Your Solution セクションには、売上税の表示を承認するための追加のテーブルを追加することによって、showSalesTax() メソッドがオーバーレイされたことが示されています。 このオーバーレイは、赤で丸で囲まれた &lt;isv&gt; タグの間に表示されます。 

[![4](./media/41.png)](./media/41.png)

このオーバーレイを Dynamics AX 2012 のコードと比較するとき、これは単純な変更です。 オーバーレイによって、switch ステートメントに追加のテーブルが追加されました。 

[![5](./media/51.png)](./media/51.png) 

ただし、Finance and Operations のセクションでは、Dynamics AX 2012 コード スニペットのいずれかと同じようには表示されません。 

[![6](./media/61.png)](./media/61.png) 

詳細な点検を行う際、コードはデリゲート メソッド showSalesTax\_delegate() を呼び出します。 

[![this.showSalesTax\_delegate(this.getCallerRecord().TableId, result);](./media/showsalestax_delegate.png)](./media/showsalestax_delegate.png) 

デリゲートの使用は、コードが別の場所に移動されたことを意味します。 showSalesTax\_delegate() は、アプリケーション基準で宣言され、Application Suite で処理されました。 移動されたコードを表示するには、デリゲート ハンドラを探します。 **デリゲートとハンドラーの検索** セクションには、デリゲートとハンドラーを検索するメソッドがあります。 アプリケーション スイートでデリゲート ハンドラー メソッドを検索した後、showSalesTax() メソッドからから移動されたコードを参照します。 Dynamics AX 2012 で適用されているオーバーレイされた同じ変更を、デリゲート ハンドラーに適用できます。 

[![委任とハンドラーのコード サンプルの検索](./media/findingdelegatesandhandles.png)](./media/findingdelegatesandhandles.png) 

デリゲート ハンドラーで switch ステートメントに新しいテーブルを追加した後、コードは Dynamics AX 2012 の場合と同じように機能します。 

[![ShowSalesTax メソッド コード](./media/showsalestaxmethod.png)](./media/showsalestaxmethod.png)

### <a name="adding-a-new-delegate"></a>新しい委任の追加

このシナリオでは、アプリケーション スイートで作成された割引を考慮するために、アプリケーション基準に存在する既存の税計算方法を変更します。 Foundation レイヤーの次のクラスは、総額に基づいて税金を計算します。 

![SimpleTax クラス](media/simple-tax.png)

アプリケーション スイートでは、現在の割引を含む ProductDiscount クラスを追加することで割引の概念を導入しました。 

[![11](./media/112.png)](./media/112.png) 

Foundation レイヤー下部にある TaxCalculator クラスには、Suite レイヤーの DiscountRate へのアクセス権がないため、委任を使用して受領合計を更新し、税計算に使用する必要があります。 SimpleTax クラスでは、署名のハンドラーによって必要な状態情報とともにデリゲート メソッド applyDiscountDelegate を作成します。 デリゲート メソッドは、デリゲート インスタンスとハンドラー間のコントラクトを定義することが唯一の目的のため、常に空です。 

```xpp
delegate void applyDiscountDelegate(real _receiptTotal, EventHandlerResult _result)
{
} 
```

> [!NOTE]
> デリゲートの宣言、デリゲート インスタンスおよびデリゲート ハンドラーの署名は一致する必要があります。 デリゲート ハンドラーを実行するコード内の箇所に、デリゲートのインスタンスを作成することが必要になりました。 &lt;isv&gt; タグ間での変更は追加されたコードを表します。 

![calculateTotalTax method](media/calculate-total-tax.png)

デリゲートの環境が整い、割引情報へのアクセス権を持つアプリケーション スイート レイヤーに、ハンドラー メソッドを追加します。 

![applyDiscountDelegateHandler メソッド](media/apply-discount-delegate-handler.png)

SubscribesTo キーワードを使用して、applyDiscountDelegateHandler メソッドを applyDiscountDelegate デリゲートにハンドラーとして結合します。

> [!NOTE]
> デリゲートごとに複数のハンドラーが存在する可能性があります。 ハンドラー メソッドの処理には、定義された順序は**ありません**。 注文が重要な場合は、代行ハンドラーのペアは一緒に連鎖する必要があります。 以下の最終クラスでは、calculateTotalTax() メソッドが実行されるとき、applyDiscountDelegate が起動および処理され、receiptTotal が更新されて正確な税計算が提供されます。

#### <a name="full-code"></a>完全なコード

##### <a name="simpletax-class-in-the-application-foundation-layer"></a>Application Foundation Layer の SimpleTax クラス

![SimpleTax クラス](media/simple-tax-full-code.png)

##### <a name="productdiscount-class-in-the-application-suite-layer"></a>アプリケーション スイート レイヤーの ProductDiscount クラス

![ProductDiscount クラス](media/product-discount-full-code.png)

## <a name="find-delegates-and-handlers"></a>委任およびハンドラーを検索します
デリゲートとハンドラーを見つける主要な 3 つの方法があります

-   メタデータ検索
-   クラス参照
-   SubscribesTo 参照

[メタデータ検索と Visual Studio](../dev-tools/metadata-search-visual-studio.md) ページで説明されているメタデータ検索ツールは、デリゲート、またはそのハンドラーを検索するための優れた方法です。 Visual Studio で、 **Dynamics 365 &gt; メタデータ検索** に移動してメタデータ検索ツールを開きます。 

[![Del15](./media/del15.png)](./media/del15.png) 

検索フィールドに、「code:&lt;デリゲート名&gt;」を入力して検索をコードに制限し、デリゲート名の使用を見つけると、デリゲートとハンドラーの両方を返します。 メタデータ検索は全体のコード ベースを検索し、完了に時間がかかる場合がありますが、コードにあるすべての検索用語の使用を返します。 

[![Del16](./media/del16.png)](./media/del16.png) 

メソッド 2 および 3 はメタデータ検索に並行して使用できます。 デリゲートが定義されているクラスは、デリゲートまたはハンドラーの検索を絞り込む手段としても機能します。 SubscribesTo キーワードには、デリゲートが定義されているクラス名が必要です。 Visual Studio の 参照の検索 (クラス名の右クリック &gt; 参照の検索) により、クラスを参照するファイルの一覧が返されます。 このリストには、デリゲートが宣言されているクラス定義とそのクラスを参照するハンドラーの両方が含まれます。 クラス参照の検索は完全な方法ではなく、クラス参照によるいくつかの手動検索を必要とします。 ただし、少さいサブセットのファイルが生成され、メタデータ検索よりも早くなる可能性があります。 

[![Del17](./media/del17-1024x300.png)](./media/del17.png) 

クラス参照の検索と同様、すべての参照の検索は、SubscribesTo キーワードで行うことができます。 結果リストには、すべての静的デリゲート ハンドラーが含まれます。 この一覧を手動で移動することで、静的デリゲート ハンドラーを検索できます。 これは、SubscribesTo キーワードを使用しない動的に宣言された代理ハンドラを返しません。 

[![Del18](./media/del18-1024x328.png)](./media/del18.png)
