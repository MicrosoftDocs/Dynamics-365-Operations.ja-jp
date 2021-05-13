---
title: 承認テスト ライブラリに関するよく寄せられる質問
description: このトピックでは、承認テスト ライブラリに関するよくある質問に対する回答を示します。
author: MichaelFruergaardPontoppidan
ms.date: 03/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2019-03-27
ms.dyn365.ops.version: App Update 10.0.2
ms.openlocfilehash: 7a809374d52ce106dad0223e5df8a050dbcfdbb5
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5865886"
---
# <a name="acceptance-test-library-faq"></a>承認テスト ライブラリに関するよく寄せられる質問

[!include [banner](../includes/banner.md)]

## <a name="which-fluent-prefix-should-i-use-set-for-or-with"></a>どの Fluent な接頭辞を使用しますか: set、for、with

Fluent メソッドを追加するクラスにより、異なるルールが適用されます:

- [エンティティ](concepts-entities.md)
- [作成者](concepts-creators.md)
- [[コマンド]](concepts-commands.md)
- [クエリ](concepts-queries.md)
- [詳細](concepts-specifications.md)

## <a name="should-i-implement-an-entity-or-a-creator-class"></a>エンティティまたは作成者クラスを実装する必要があるか

ほとんどのエンティティに対して、エンティティ クラスを作成する作業は作成者クラスを作成する作業と同じです。 したがって、エンティティ クラスを作成する必要があります。 ただし、場合によっては、エンティティを作成するプロセスは複雑な可能性があります。 良い例は品目エンティティです。 品目エンティティを構成する異なるテーブルは 10 以上あるため、エンティティ クラスを作成するのは困難です。 テスト ケースでは既存の品目を更新する必要がほとんどないため、作成者クラスがあれば問題ありません。その実装ははるかに簡単です。

## <a name="does-the-order-of-the-chained-fluent-setters-matter"></a>連鎖 Fluent セッターの順番は重要か

ほとんどの場合、連鎖 Fluent セッターの順番は問題になりません。 ただし、セッター メソッドの呼び出し時に既定値になることに注意してください。 したがって、メソッドの順序を変更すると、異なる結果になる場合があります。 これは販売明細行の例です。

### <a name="option-1"></a>オプション 1

```xpp
salesLine.setQuantity(10).setUnitPrice(100).setAmount(2000).save()
```

このオプションにより金額 == 2,000 の販売明細行が生成されます。これは金額が最後に設定されるためです。
    
### <a name="option-2"></a>オプション 2

```xpp
salesLine.setAmount(2000).setQuantity(10).setUnitPrice(100).save()
```

このオプションは 金額 == 1,000 の販売明細行を生成します。これは単価を設定した後、既定で金額は数量 × 価格に設定されるためです。

## <a name="can-i-use-atl-for-tests-that-run-on-the-empty-data-set"></a>空のデータセットで実行するテストに ATL を使用できるか

承認テスト ライブラリ (ATL) は空のデータ セットで問題なく使用できます。 前提条件の自動設定は必要に応じて行われます。 たとえば、請求書の転記に対する前提条件は、`salesOrder.postInvoice()` への最初の呼び出し時にのみ設定されます。 詳細については [確認](test-data-methods.md#ensure-methods) を参照してください。

テスト クラス内のひとつ以上のテストで請求書を転記する必要がある場合は、`setUpTestCase` メソッドで `Ensure` メソッドを呼び出してパフォーマンスを向上させることもできます。

## <a name="can-i-use-atl-for-unit-tests"></a>単体テストで ATL を使用できるか

ATL は主に統合やコンポーネント テストにおけるデータの設定と検証に使用する必要があります。 ただし、場合によっては、単体テストにも使用します。

### <a name="why-should-i-be-cautious-about-using-atl-in-unit-and-component-tests"></a>単体テストおよびコンポーネント テストで ATL を使用することに注意が必要な理由

販売注文など、より複雑なエンティティでは `modifiedField`、`insert`、`update` の各イベントに関連付けられたすべてのビジネス ロジックが呼び出されます。 たとえば、請求書トランザクションの作成は、実際の請求書転記ロジックの実行によっても行われます。 したがって、いくつかの操作でパフォーマンスが遅くなります。 ただし、これらの問題はマスター データを表すほとんどのエンティティで発生しません。 したがって、どんな種類のテストでもそれらのエンティティを使える必要があります。

詳細とクエリを使用して検証を行う場合、重大なオーバーヘッドは発生しません。 これらのコンポーネントは単体テストでも使用できます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]