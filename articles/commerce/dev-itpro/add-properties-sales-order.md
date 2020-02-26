---
title: プロパティを販売注文に追加
description: 販売注文のプロパティをカスタマイズすることにより、オンライン ストアから追加データを送信して業務プロセスの要件を満たすことができます。 この記事では、販売注文にプロパティを追加する方法について説明します。
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 44351
ms.assetid: dd9b86cb-630a-4429-9aea-8ba4c4723baa
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: aa92380b6ff5349c048608ce05c391dfd73c9a66
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004603"
---
# <a name="add-properties-to-sales-orders"></a>プロパティを販売注文に追加

[!include [banner](../includes/banner.md)]

販売注文のプロパティをカスタマイズすることにより、オンライン ストアから追加データを送信して業務プロセスの要件を満たすことができます。 この記事では、販売注文にプロパティを追加する方法について説明します。

スターター ストアには、注文トランザクション中にデータを取得するために使用できる販売注文プロパティがあります。 ただし、販売注文のプロパティを拡張し、注文トランザクション中に追加データを送信するすることができます。 たとえば、品目が贈物用に包装されるべきかを示す **GiftWrap** 属性を追加できます。 販売注文のプロパティをカスタマイズするには、次の作業を行う必要があります。

1.  属性を作成します。
2.  属性グループに属性を追加します。
3.  オンライン ストアに属性グループを割り当てます。
4.  販売注文書で属性を設定します。

## <a name="create-an-attribute"></a>属性を作成します
属性を作成するには、属性タイプを定義してから、新しい属性に属性タイプを割り当てる必要があります。 この例では、事前定義済みの属性タイプを使用します。

1.  クライアントで、**製品情報管理** &gt; **設定** &gt; **カテゴリと属性** &gt; **属性**の順にクリックします。
2.  **新規**をクリックし、次の値を入力します。

    | プロパティ       | 先頭値        |
    |----------------|--------------|
    | 氏名           | GiftWrap     |
    | フレンドリ名  | ギフト ラップ    |
    | 属性タイプ | StringDomain |

## <a name="add-the-attribute-to-an-attribute-group"></a>属性グループへの属性の追加
属性を定義した後は、属性グループを追加する事ができます。

1.  **製品情報管理** &gt; **設定** &gt; **カテゴリと属性** &gt; **属性グループ**の順にクリックします。
2.  **新規**をクリックし、次の値を入力します。

    | プロパティ      | 先頭値                       |
    |---------------|-----------------------------|
    | 氏名          | SalesOrderGroup             |
    | フレンドリ名 | 販売注文属性グループ |
    | 説明   | 販売注文属性グループ |

3.  **属性**クイック タブで、**追加**をクリックします。
4.  **GiftWrap** を選択し、**選択** をクリックします。
5.  **OK** をクリックします。

## <a name="assign-the-attribute-group-to-your-online-store"></a>オンライン ストアに属性グループを割り当てます
属性グループを作成した後は、オンライン ストアに割り当てることができます。

1.  **小売とコマース** &gt;**チャネル** &gt; **オンライン ストア**をクリックします。 
2.  **オンライン ストア** リストで、店舗をダブルクリックします。
3.  **設定**タブで、**販売注文属性**をクリックします。
4.  **チャネル属性グループ**ページで、**新規**をクリックします。
5.  **名前**フィールドで **SalesOrderGroup** を選択します。

## <a name="set-the-attribute-on-a-sales-order"></a>販売注文書で属性を設定
Commerce Runtime 内にビジネス ロジックを追加することにより属性を販売注文に追加することができます。 次のコードを追加して、カートに属性を追加し、カートを保存します。それから、カートから受注を作成します。

    var cart = orderManager.GetCart(cartId, accountNumber, false);
    cart.AttributeValues.Add(new AttributeTextValue { Name = "GiftWrap", TextValue = "Yes" });
    orderManager.SaveCart(cart);
    orderManager.CreateOrderFromCart(...);

## <a name="next-steps"></a>次のステップ
Commerce Runtime で販売注文を作成した後は、新しい属性を表示できます。

### <a name="view-the-attribute"></a>属性の表示

1.  クライアントで、**小売とコマース** &gt; **小売とコマース IT** &gt; **配布スケジュール**の順にクリックします。
2.  **P-0001\_OC** ジョブを実行し、オンライン チャネルとして POS トランザクションを実行します。
3.  **小売とコマース** &gt; **小売とコマース IT** &gt; **注文の同期**の順にクリックして販売注文を作成します。
4.  **小売とコマース** &gt; **照会およびレポート** &gt; **販売注文** &gt; **すべての販売注文**の順番にクリックします。
5.  **小売とコマース** タブで、**小売属性**をクリックします。 作成した属性を確認する必要があります。




