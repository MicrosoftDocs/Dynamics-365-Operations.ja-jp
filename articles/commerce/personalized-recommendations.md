---
title: パーソナライズされた製品推奨事項の有効化
description: この記事では、パーソナライズされた製品推奨事項を Microsoft Dynamics 365 Commerce の顧客に対して使用可能にする方法について説明します。
author: bebeale
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail, eCommerce
ms.search.form: ''
ms.openlocfilehash: f626704b41b9d22f6b2ff55dd4ffe1037559a83a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283617"
---
# <a name="enable-personalized-recommendations"></a>パーソナライズされた推奨事項の有効化

[!include [banner](includes/banner.md)]

この記事では、パーソナライズされた製品推奨事項を Microsoft Dynamics 365 Commerce の顧客に対して使用可能にする方法について説明します。

Dynamics 365 Commerce では、小売業者がパーソナライズされた製品推奨事項 (個人用設定とも呼ばれます) を使用可能にすることができます。 この方法で、パーソナライズされた推奨事項が顧客エクスペリエンス オンラインおよび販売時点管理 (POS) に組み込まれます。 個人用設定機能をオンにすると、システムはユーザーの購入情報と製品情報を関連付けて、個別の製品推奨事項を生成できます。

## <a name="personalization-prerequisites"></a>個人用設定の前提条件

パーソナライズされた製品推奨事項を顧客に対して利用可能にする前に、Azure Data Lake Store にストレージを移行したコマース ユーザーに対してのみ、製品推奨事項がサポートされることに注意してください。 顧客がパーソナライズした製品推奨事項を受信できるようにする前に、小売業者は [製品推奨事項を有効にする](enable-product-recommendations.md) 必要があります。

> [!NOTE]
> 製品推奨事項を有効にすることにより、個人用設定も有効になります。 ただし、個人用設定を無効にすると、他のタイプの製品推奨事項は無効になりません。

製品推奨事項の詳細については、[製品推奨事項の概要](product-recommendations.md) を参照してください。

## <a name="turn-on-personalization"></a>個人用設定を有効にする

個人用設定を有効にするには、次の手順に従います。

1. Commerce Headquarters で、**機能管理** を検索します。
1. **すべて** を選択して、使用可能な機能の一覧を表示します。 
1. 検索ボックスに、**推奨事項** を入力します。
1. **個人用設定がされた製品の推奨** 機能を選択します。
1. **個人用設定がされた製品の推奨** プロパティ ペインで、**すぐに有効化する** を選択します。

![個人用設定を有効にする。](./media/FeatureManagement_Personalized.PNG)

> [!NOTE]
> 個人用設定を有効にすると、パーソナライズされた製品推奨事項リストを生成するプロセスが開始します。 これらのリストを利用可能にし、オンラインおよび POS で表示するまでに、少なくとも 1 日必要な場合があります。

## <a name="personalized-lists"></a>パーソナライズされたリスト

推奨事項サービスでは、コンピューター生成された既存のリストの個人用設定を許可することに加え、オンラインと POS の両方で製品検索エクスペリエンスを個人用設定を許可することができます。

個人用設定を有効にした後、小売業者はパーソナライズされた "おすすめ" オンライン リストを、または POS 端末で "顧客への推奨" リストを買い物客に表示できます。 さらに、小売業者は既存の製品推奨事項リストに個人用設定を適用し、認証されたユーザーに対する一般データ保護規則 (GDPR) のオプトアウト エクスペリエンスを提供できます。 個人用設定を無効にすると、これらの機能も無効になります。

### <a name="online-picks-for-you-lists"></a>オンラインの "おすすめ" リスト

"おすすめ" リストは、認証されたユーザーが推奨製品の個人用設定リストを表示する、人為的知能の機械学習 (AI-ML) リストです。 このリストは、ユーザーのオムニチャネル購買履歴に基づいています。 ユーザーがより多くの購買を行うと、カスタマイズされた推奨が動的に更新されます。 このタイプのリストは、カテゴリのフィルター処理もサポートしているため、小売業者はナビゲーション階層に基づいておすすめの上位を表示できます。

E コマース ページに "おすすめ" リストが表示される前に、次のユーザー要件を満たす必要があります。

- ユーザーがサインインしている必要があります。 匿名ユーザーには、パーソナライズされた推奨事項は表示されません。
- ユーザーは、自分のアカウントで少なくとも 1 つ購入する必要があります。
- ユーザーは、パーソナライズされた推奨事項の受信をオプトインする必要があります。

次の図は、オンライン ストア ページの "おすすめ" リストの例を示します。

![オンラインのおすすめリスト。](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a>POS の "顧客への推奨" リスト

クライアンテリング エクスペリエンスを向上させるため、小売業者は、コンテキスト "顧客への推奨" リストを追加することにより、既存の顧客詳細ページをパーソナライズできます。

次の図は、POS 端末の "顧客への推奨" リストの例を示します。

![POS の顧客への推奨リスト。](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a>既存の推奨リストへの個人用設定の適用

小売業者は、既存の推奨リストに "新規"、"トレンド"、"ベスト セラー"、"人気製品"、"よく一緒に購入される製品" などの個人用設定を適用することができます。 既存のリストに対して個人用設定が適用されると、サインインしたユーザーが以前に購入した品目がそれらのリストから削除されます。 匿名ユーザーおよびパーソナライズされた推奨事項の受信をオプトアウトしたユーザーの両方については、既存のリストの既定バージョンが表示されます。 したがって、小売業者は個別のページ エクスペリエンスを手動で管理する必要はありません。

たとえば、サインインしたユーザーが、次の図にある "トレンド - 既定" のリストに表示されている黒色のウォッチと茶色の作業ブーツを既に購入しました。 したがって、"トレンド - 個人用設定" リストに示すように、ユーザーにはそれらの製品の代わりに新しい製品が表示されます。

![個人用設定の適用。](./media/applypersonalization.png)

コマース サイト ビルダーの既存の推奨リストに個人用設定を適用するには、次の手順を実行します。

1. 製品収集モジュールを含む既存のサイト ビルダー ページを開きます。
1. 左のナビゲーション ウィンドウで、製品収集モジュールを選択します。
1. 右のナビゲーション ウィンドウの、**製品** で、リストを選択します。
1. **製品リストのコンフィギュレーションの選** ダイアログ ボックスの、**タイプ** で、リスト タイプを選択します。
1. **個人用設定を適用** チェック ボックスを選択し、**OK** を選択します。

    ![トレンド リストへの個人用設定の適用。](./media/ApplyPersonalizationToTrending.PNG)

1. ページを保存し、編集を終了してから、公開します。 ページを公開した後、サインインしているユーザーにはパーソナライズされたトレンド リストが表示されます。

## <a name="additional-resources"></a>追加リソース

[製品推奨事項の概要](product-recommendations.md)

[Dynamics 365 Commerce 環境で Azure Data Lake Storage を有効化する](enable-adls-environment.md)

[製品推奨事項の有効化](enable-product-recommendations.md)

["類似したルックを買う" 推奨を有効にする](shop-similar-looks.md)

[カスタマイズされた推奨事項のオプト アウト](personalization-gdpr.md)

[POS での製品推奨事項の追加](product.md)

[トランザクション画面への推奨設定の追加](add-recommendations-control-pos-screen.md)

[AI-ML 推奨事項結果の調整](modify-product-recommendation-results.md)

[収集された推奨事項の手動作成](create-editorial-recommendation-lists.md)

[推奨事項とデモ データの作成](product-recommendations-demo-data.md)

[製品推奨事項に関するよく寄せられる質問](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
