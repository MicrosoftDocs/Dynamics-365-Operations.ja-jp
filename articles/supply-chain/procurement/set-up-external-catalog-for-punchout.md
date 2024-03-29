---
title: パンチアウト e-procurement の外部カタログの設定
description: この記事では、外部カタログまたは PunchOut カタログを使用して仕入先からの見積情報を収集し、要求に追加する方法について説明します。
author: GalynaFedorova
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchVendorPortalRequests, CatExternalCatalogConfiguration, CatCXMLCartLogList
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b109ec1db39240e6816d79092763b4686857676
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882492"
---
# <a name="set-up-an-external-catalog-for-punchout-e-procurement"></a>パンチアウト e-procurement の外部カタログの設定

[!include [banner](../includes/banner.md)]

外部カタログを使用することにより、Supply Chain Management で処理される製品および価格情報が、正確かつ最新のものであることを保証することができます。 要求は承認され、発注書に変換され、注文は仕入先に配置することができます。

外部カタログが設定され、従業員が依頼を準備しているときは、外部サイト、外部カタログにリダイレクトし、外部サイトで作成された買い物カゴを返すオプションがあります。 この通信は cXML プロトコルに基づいており、購買システムと販売組織の間で設定する必要があります。

コミュニケーションをセットアップするには、仕入先が ID や、購入者の会社のドメイン、例えば 「DUNS」 および 「DUNS 番号」 資格情報、および仕入先のカタログにアクセスするための URL など外部カタログの構成に使用する情報を提供する必要があります。

## <a name="setting-up-an-external-catalog"></a>外部カタログの設定

外部カタログにより、購買要求を入力した従業員は、製品を選択するために外部サイトにリダイレクトされます。 従業員が外部カタログから選択した製品は、最新の価格情報を使用して返され、ここから購買要求に追加することができます。 従業員による外部サイトからの注文を可能にすることは意図していません。 外部カタログを設定するときは、外部カタログがアクセスできるサイトの目的が見積もり情報を収集することであり、実際の注文を行わないことを確認する必要があります。

### <a name="to-set-up-an-external-vendor-catalog-complete-the-following-tasks"></a>外部仕入先カタログを設定するには、次の作業を行います。:

1. 調達カテゴリ階層を設定します。 詳細については、[調達カテゴリ階層に対するポリシーの設定](tasks/set-up-policies-procurement-category-hierarchies.md) を参照してください。
2. 仕入先を Supply Chain Management に登録します。 外部仕入先のカタログにアクセスするコンフィギュレーションを設定する前に、仕入先と仕入先の連絡先を Microsoft Dynamics 365 で設定する必要があります。 外部カタログの仕入先は、選択した調達カテゴリにも追加する必要があります。 仕入先を登録することに関する詳細については、[仕入先コラボレーション ユーザーの管理](manage-vendor-collaboration-users.md) を参照してください。 仕入先を調達カテゴリに割り当てる方法については、「[特定の調達カテゴリに対する仕入先の承認](tasks/approve-vendors-specific-procurement-categories.md)」を参照してください。
3. ベンダーが使用する測定単位と通貨が設定されていることを確認します。 測定単位を作成する方法の詳細については、[測定単位の管理](../pim/tasks/manage-unit-measure.md) を参照してください。
4. 仕入先の外部カタログ サイトの要件に基づいて、外部仕入先カタログをコンフィギュレーションします。 このタスクの詳細については、[外部仕入先カタログを構成する](#configure-the-external-vendor-catalog) を参照してください。
5. 仕入先の外部カタログのコンフィギュレーションをテストして、設定が有効であることと、仕入先の外部カタログにアクセスできることを確認します。 **設定の検証** アクションを使用して、定義した要求の設定メッセージを検証します。 このメッセージにより、仕入先の外部カタログ サイトがブラウザー ウィンドウで開かれるはずです。 検証中は、仕入先からアイテムやサービスを注文することはできません。 品目およびサービスを注文するには、購買要求を通じて仕入先のカタログにアクセスする必要があります。
6. 外部のカタログを有効化するには、**外部カタログ** ページの **カタログの有効化** ボタンを使用します。 外部カタログは、従業員が使用する前に有効にする必要があります。 外部カタログはいつでも無効にすることができます。


## <a name="configure-the-external-vendor-catalog"></a>外部仕入先カタログをコンフィギュレーションします

このセクションでは、前のセクションのタスク 4 の詳細について説明します。

1. 仕入先の外部カタログの名前と説明を入力します。 入力した名前は、購買依頼を作成した従業員に表示される外部カタログを表すカートに表示されます。 従業員はカートをクリックして、ベンダーの外部カタログ サイトでカタログを開くことができます。
2. **外部カタログ画像** アクションを使用して画像を追加します。 画像は、購買依頼を作成した従業員に表示される外部カタログを表すカートに表示されます。 画像の幅と高さは等しくなければならないことに注意してください。 それ以外の場合、画像が正しく表示されません。
3. 仕入先の外部カタログ Web サイトを、従業員が要求を作成したブラウザー ウィンドウと同じブラウザー ウィンドウに表示するか、新しいウィンドウで開くかを選択します。
4. カタログの仕入先を選択します。 **法人** リストでは、ベンダーが設定されている各法人の行があります。 ユーザーが一部の法人では仕入先カタログから直接製品を要求できるようし、他の法人ではできないようにするには、カタログを使用可能にするかどうかを決める法人ごとに **アクセス禁止** または **アクセス許可** ボタンを使用できます。
5. **既定の有効期限 (日数)** フィールドに、外部カタログから受け取った見積が有効であって、外部仕入先からの購入に使用できる日数を入力します。 見積が仕入先の外部カタログサイトで作成され、取得される場合、見積は現在のシステム日付で有効となり、このフィールドに入力した日数の間有効です。
6. **追加** ボタンをクリックして、調達カテゴリの外部カタログへのマッピングを開始します。 その後、カテゴリ名の一覧で、カテゴリを選択します。 カテゴリのリストは、仕入先に対して設定されたすべての法人で仕入先がマップされている調達カテゴリのスーパーセットです。

    > [!NOTE]
    > 調達方針は、購買組織と受取作業単位のためのカテゴリへのアクセスを許可または制限するために使用されます。 外部カタログへのパンチアウトでは、カタログにマッピングされている調達カテゴリの少なくとも 1 つにアクセスが許可されている必要があります。

7. 仕入先に送信される cXML セットアップ要求メッセージを設定します。 自動的に生成されるメッセージ形式は、セッションを開始するために必要な最小限のテンプレートです。 タグの値を入力します。

**メッセージ形式の復元** をクリックすると、いつでもシステム生成のメッセージ テンプレートを再ロードできます。 メッセージ形式を復元すると、現在のメッセージは空のタグを持つ自動的に生成されたメッセージ形式に置き換えられます。

### <a name="cxml-setup-message"></a>cXML セットアップ メッセージ
以下に、テンプレートに含まれるタグの説明があります。

| フィールド | 説明 | 
|---------|---------|
|< Header >< From >< Credential domain=”” >|購入者の会社のドメイン。|
|< Header >< From >< Credential>< Identity >< /Identity > | 購入者の会社の ID。|
|< Header >< To >< Credential domain=”” > | 仕入先の会社のドメイン。|
|< Header >< To >< Credential>< Identity >< /Identity> | 仕入先の会社の ID。|
|< Header >< Sender >< Credential domain=”” > | 購入者の会社のドメイン。|
|< Header >< Sender >< Credential >< Identity >< /Identity> | 購入者の会社の ID。|
|< Header >< Sender >< Credential >< SharedSecret >< /SharedSecret >|購入者の会社の共有機密情報。|
|< 要求 deploymentMode=”” >|テストまたは運用配置。|
|< Request >< PunchOutSetupRequest >< SupplierSetup >< URL >< /URL>|仕入先のパンチアウト エンドポイントの URL。|

### <a name="extrinsic-elements"></a>外部要素

外部要素とは、パンチアウトするユーザーに基づくユーザー名などの追加情報です。外部要素は、パンチアウトが発生したときに設定され、要求設定メッセージで送信されます。
仕入先は、セットアップ要求で外部要素を受け取る必要があります。 その場合は、**外部カタログ** ページの **メッセージ形式** セクションの外部要素のリストに外部要素を追加する必要があります。
仕入先が認識して値にマップできる外部要素の名前を指定します。 値のオプションは、ユーザー名、ユーザーの電子メール、またはランダム値です。
cXML プロトコルの詳細については、[cXML.org Web サイト](http://cxml.org/) を参照してください。

## <a name="post-back-message"></a>メッセージのポスト バック
ポスト バック メッセージは、ユーザーが外部サイトからチェックアウトし、Supply Chain Management に戻るときに仕入先から受け取ったメッセージです。 ポスト バック メッセージは構成できません。 メッセージは cXML プロトコル定義に基づいています。 要求明細行で受け取ったポスト バック メッセージの一部となる情報は次のとおりです。

| 仕入先から受け取ったメッセージ | 要求明細行にコピー済|
|------------------------------|----------------------------------------------------------|
|< ItemIn quantity=”” > |件数|
|< ItemIn>< ItemID >< SupplierPartID >< /SupplierPartID >|外部品目 ID|
|< ItemDetail>< UnitPrice >< Money currency=”” >| 通貨|
|< ItemDetail >< UnitPrice >< Money >< /Money >| 単価|
|< ItemDetail >< Description ShortName=”” >|製品名|
|< ItemDetail >< Description >< /Description >|商品説明に含まれています。ShortName が指定されていない場合の製品名。|
|< ItemDetail >< UnitOfMeasure >< /UnitOfMeasure >|単位|
|< ItemDetail >< Classification >< /Classification >|商品説明に含まれる|
|< ItemDetail >< Classification domain=”” >|商品説明に含まれる|

## <a name="delete-an-external-catalog"></a>外部カタログの削除
ページ上の [削除] アクションで外部カタログを削除します。

外部仕入先カタログの製品が要求されている場合、外部仕入先カタログを削除することはできません。 その代わりに、仕入先カタログを無効のステータスに設定されます。 外部仕入先のカタログ サイトへのアクセス許可を削除するが、外部カタログを削除しない場合は、外部カタログ ステータスを無効に変更します。

## <a name="additional-resources"></a>追加リソース

- [cXML の拡張機能の購入](purchasing-cxml-enhancements.md)
- [パンチアウト e-procurement の外部カタログの使用](use-external-catalogs-for-punchout.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]