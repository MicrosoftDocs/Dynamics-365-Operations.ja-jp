---
title: B2B 向け Commerce カタログに関するよくあるご質問
description: この記事では、よく寄せられる Microsoft Dynamics 365 Commerce カタログに関する質問に対する回答を提供します。
author: ashishmsft
ms.date: 07/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 68c648c5caf2667f413b236dc437fc2c74c40d07
ms.sourcegitcommit: c271b2edc4bf777f7194b09139ccbd174a359c75
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/16/2022
ms.locfileid: "9168988"
---
# <a name="commerce-catalogs-for-b2b-faq"></a>B2B 向け Commerce カタログに関するよくあるご質問

[!include [banner](includes/banner.md)]

この記事では、よく寄せられる Microsoft Dynamics 365 Commerce [企業間 (B2B) カタログ](catalogs-b2b-sites.md) に関する質問に対する回答を提供します。

### <a name="why-cant-i-configure-a-catalog-specific-navigation-hierarchy-or-see-an-option-to-associate-a-customer-hierarchy"></a>カタログ固有のナビゲーション階層を構成したり、顧客階層を関連付けるオプションを表示したりできないのはなぜですか?

**小売チャネルでの複数のカタログの使用を有効にする** 機能が Commerce headquarters の **機能管理** ワークスペースで有効であること、および環境が Commerce version 10.0.27 以降であることを確認してください。 **カタログ タイプ** で **B2B** を選択したことを確認してください。

### <a name="can-i-view-the-catalog-specific-hierarchy-and-enrich-category-pages-in-commerce-site-builder"></a>Commerce サイト ビルダーでカタログ固有の階層を表示し、カテゴリ ページを拡充させることはできますか?

はい、サイト ビルダーの **製品** ページにアクセスできる Commerce サイト ビルダー ユーザーは、カタログを選択して、カタログ固有の階層を表示できます。 **製品** ページから、ユーザーはカタログ内の特定のカテゴリのカテゴリ ページを拡充させることもできます。 詳細については、[カテゴリ ランディング ページの拡充](enrich-category-page.md) を参照してください。 カタログに固有のエンリッチメントが必要な場合は、そのカタログに明確で一意のナビゲーション階層を設定することをお勧めします。

### <a name="can-a-b2b-shopper-purchase-from-multiple-catalogs-in-a-single-checkout"></a>B2B の買い物客は、1 回のチェックアウトで複数のカタログから購入できますか?

はい、1 回のチェックアウトで複数のカタログから購入できます。 B2B の買い物客は、カート ビューのカタログ インジケータを使用して、どの品目がどのカタログから追加されたかを判断できます。

### <a name="if-a-b2b-shopper-purchases-the-same-item-from-different-catalogs-what-is-the-expected-behavior"></a>B2B 買い物客が異なるカタログから同じ品目を購入した場合、予想される動作は何ですか?

特定のユーザーが特定の時間に複数のカタログにアクセスできる場合でも、それらのカタログ内の製品は相互に排他的であることが期待されます。 つまり、理想的には、同じ製品が特定のユーザーの複数のカタログの一部であってはなりません。

ただし、同じ商品が複数のカタログに属している状況が発生した場合、システムはその商品の複数のカート明細行を維持します。 カタログごとに個別の明細行があります。 2 つの異なるカタログの同じ商品は、チェックアウト時にマージされません。

### <a name="when-a-b2b-shopper-is-shopping-is-there-any-validation-for-catalog-availability"></a>B2B 買い物客が買い物をしているとき、カタログの使用可能性の検証はありますか?

はい。 B2B 買い物客は、カート内のすべての品目が有効なカタログからのものである場合にのみ、チェックアウトに進むことができます。 カート品目が期限切れまたは取り消されたカタログからのものである場合、それらは削除され、ユーザーに通知されます。

### <a name="during-the-shopping-experience-are-search-and-product-discovery-including-related-and-recommended-product-collections-catalog-specific"></a>買い物体験中、検索と商品発見 (関連商品と推奨商品のコレクションを含む) はカタログ固有ですか?

はい。 ユーザーが特定のカタログを選択するとすぐに、買い物全体がカタログ固有になります。 この体験には、検索候補、検索結果、カテゴリ結果、絞り込み条件、価格、属性、推奨製品 (新製品、ベストセラー、トレンド、一緒に頻繁に購入される製品、関連製品など) の製品発見体験が含まれます。

### <a name="can-a-b2b-shopper-purchase-from-the-default-assortment-catalogid0"></a>B2B 買い物客は、既定の品揃え (catalogID=0) から購入できますか?

いいえ、B2B 買い物客は既定の品揃えから購入を許可されません。 その品揃えは、匿名の閲覧のみを目的としています。 B2B 買い物客にカタログの割り当てがない場合 (管理者からの更新が保留中)、選択できるカタログを表示できず、カテゴリ階層も表示されません。

### <a name="can-marketing-content-be-curated-for-a-product-that-is-specific-to-a-catalog"></a>カタログに固有の製品のマーケティング コンテンツをキュレーションできますか?

現在、製品のエンリッチメントはサイトおよびチャネル レベルでのみサポートされています。 つまり、製品が強化されその製品は複数のカタログ間で共有されている場合、その製品に対応する拡充製品の詳細ページ (PDP) は、特定のサイトのすべてのカタログ間で同じ方法でレンダリングされます。 

### <a name="is-catalog-support-available-for-both-b2b-and-business-to-consumer-b2c-online-channels"></a>カタログ サポートは、B2B と企業間 (B2C) の両方のオンライン チャネルで使用可能ですか?

現在、コマース カタログは B2B オンライン チャネルのみを使用することを意図しています。

### <a name="a-new-customer-was-added-to-the-customer-hierarchy-or-a-new-hierarchy-was-associated-with-the-catalog-but-the-catalog-is-not-available-to-the-user-why"></a>顧客階層に新しい顧客が追加または新しい階層がカタログに関連付けられましたが、そのカタログをユーザーが使用することはできません。 なぜですか。

新しい顧客を既存の顧客階層に関連付けた後、また新しい顧客階層を作成した際、**1010** ジョブを実行したことを確認してください。 顧客階層に関連付けられているカタログは、**1010** ジョブが正常に完了した後にのみ表示されます。 カタログも新しい場合は、**1150**(カタログ) ジョブおよび **1010** ジョブを実行したことを確認してください。 新しいカタログと同様に、データがチャンネルおよび検索インデックスと同期します。 ジョブのステータスが「適用済」である場合は、データをチャンネル データベースと同期中ですが、データを検索インデックスに同期化するために追加時間が必要です。 

### <a name="can-we-set-up-catalog-specific-upsellcross-sell-items"></a>カタログ固有のアップセル/クロスセル品目を設定できますか?

現在、関連製品の機能のみがサポートされています。 ただし、コール センターでは、アップセルおよびクロスセル品目構成を使用できます。

次の機能は、コール センターでのみサポートされています。

- カタログ ソース コード
- ソース ID を使用し、原価と反応率を追跡
- カタログに固有の注文および品目のスクリプト
- カタログ ページ分析
- カタログ要求
- 支払スケジュール
- ソース コードに基づく無料の製品

### <a name="can-we-use-catalog-source-codes-for-b2b-orders-through-the-e-commerce-portal"></a>e コマース ポータルを介して B2B 注文にカタログ ソース コードを使用できますか?

いいえ。 カタログ ソース コードは、コール センター チャネルでのみサポートされています。

## <a name="additional-resources"></a>追加リソース

[B2B サイトのコマース カタログの作成](catalogs-b2b-sites.md)

[カタログ ピッカー モジュール](catalog-picker.md)

[B2B カスタマイズ のためのコマース カタログの拡張性への影響](catalogs-b2b-sites-dev.md)
