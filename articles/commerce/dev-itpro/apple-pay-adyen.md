---
title: Dynamics 365 Commerce で Adyen を使用して Apple Pay を設定する
description: この記事では、Microsoft Dynamics 365 Commerce で Adyen を使用して Apple Pay を設定する方法について説明します。
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-06-20
ms.openlocfilehash: 896847cee696e221b2114f7f28a0b56e73fc911b
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838232"
---
# <a name="set-up-apple-pay-with-adyen-in-dynamics-365-commerce"></a>Dynamics 365 Commerce で Adyen を使用して Apple Pay を設定する

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

この記事では、Microsoft Dynamics 365 Commerce で Adyen を使用して Apple Pay を設定する方法について説明します。

## <a name="key-terms"></a>重要な用語

| 相談 | Description |
|---|---|
| Apple Pay | Apple Pay 「ボタン」とも呼ばれる Apple Pay は、Adyen コネクタでサポートされるウォレット決済として提供されます。 Microsoft Dynamics 365 Apple Connector でサポートされているカスタマー エクスペリエンスと統合を有効にします。 |
| ウォレット | 銀行識別番号 (BIN) の範囲や有効期限など、クレジット カード タイプとデビット カード タイプを区別するために使用される従来の支払特性を含まない支払タイプ。 |

Dynamics 365 Commerce は、Adyen 支払ゲートウェイ サービスを使用する場合の Apple Pay との統合を最初から提供しています。 Apple Pay は、Adyen 支払サービスと連携し、Apple Pay マーチャント アカウントを使用するデジタル ウォレットの決済方法です。 構成されている場合、Apple Pay ボタンは、オンライン ストアの注文のチェックアウト ページの一部として選択可能な決済方法になります。 Apple Pay ボタンは、サポートされている Apple Pay デバイスについてのみ決済オプションとして表示されます。 ユーザーがサポートされているブラウザーまたはデバイスで **Apple Pay** を選択すると、Apple Pay サービスに転送されて直接支払を完了することができます。 その後、注文完了のためにオンライン店舗に戻ります。

Apple Pay 向け Dynamics 365 Payment Connector のコネクタ参照は、サイトで Apple Pay とクレジット カード決済を有効にする Adyen 向け Dynamics 365 Payment Connector にも使用されます。 Apple Pay は、Commerce 販売時点管理 (POS) で Adyen 向け Dynamics 365 Payment Connector を使用する Adyen 支払端末を持つ店舗でも使用するように構成できます。 この場合、Adyen 向け Dynamics 365 Payment Connector は端末で Apple の決済デバイスのタップを処理します。

## <a name="prerequisites"></a>必要条件

Commerce で Apple Pay と Adyen を使用するには、Apple マーチャント アカウントが必要です。 テスト顧客領域で Apple Pay を設定する方法の詳細については、[Apple Pay ドロップイン統合](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#set-up-apple-pay) を参照してください。 運用環境で運用する準備ができたときに行う操作については、[ライブに移行](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live) を参照してください。

Apple Pay の支払方法を、Adyen アカウントにも統合する必要があります。 Adyen は、支払方法の設定に役立ち、証明書を使用するドメインが証明書で使用するために割り当てられていることを確認するのにも役立ちます。

Commerce headquarters で拡張ウォレット機能のフラグを有効にするには、**ワークスペース \> 機能管理** に移動し、**拡張ウォレット サポートと支払の改善** 機能を検索します。 機能を選択し、**有効にする** を選択します。 機能を有効にした後 **1110** 配送スケジュールを実行して、すべてのチャンネルで変更を使用可能にします。

## <a name="map-the-apple-pay-payment-method"></a>Apple Pay の決済方法をマップする

Apple Pay はデジタル ウォレットの決済方法です。 Apple Pay の決済マッピングを設定する方法の詳細については、[ウォレット支払のサポート](../wallets.md) を参照してください。

Commerce headquarters で Apple Pay の決済方法をマップするには、次の手順に従います。

1. **Retail と Commerce \> チャネル設定 \> 決済方法 \> カード タイプ** に移動します。
1. **新規** を選択して Apple Pay の行を追加し、次の値を設定します:

    - **ID:** ApplePay
    - **電子決済名:** Apple Pay
    - **タイプ:** ウォレット
    - **発行者:** Apple

1. **プロセッサ マッピング** を選択し、**プロセッサ支払のマッピング方法** のダイアログ ボックスを開きます。 **マップされていないプロセッサ支払方法** 列には、使用可能な各コネクタ (Adyen、PayPal、Apple) でサポートされている決済方法の一覧が表示されます。
1. **Adyen 向け Dynamics 365 Payment Connector** コネクタ (POS で使用) と **Apple Pay 向け Dynamics 365 Payment Connector** コネクタ (オンライン チャネルで使用) の両方で必要なサポートされている決済方法をマップします。
1. マップの行ごとに **マップされていないプロセッサ支払方法** 列で、サポートする行を選択し、**追加** を選択して **マップされたプロセッサ支払方法** 列に選択を移動します。
1. **OK** を選択し、**カード タイプ** ページ で **保存** を選択します。

## <a name="set-up-the-apple-pay-certificate-for-your-site"></a>サイトに対する Apple Pay 証明書の設定

[Adyen Apple Pay ドキュメント](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live) で説明されているように、各サイトにドメイン関連ファイル (Apple Pay 証明書とも呼ばれる) をアップロードする必要があります。 Commerce サイト ビルダーを使用して、サイトのメディア ライブラリにドメイン関連ファイルをアップロードできます。

サイト ビルダーの Apple Pay 証明書を設定するには次の手順に従います。

1. [Adyen](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live) から証明書 (ドメイン関連ファイル) をダウンロードします。
1. .txt 拡張子をドメイン関連ファイルに追加します。
1. サイト ビルダーで、ドメイン関連ファイルをサイトのメディア ライブラリに [アップロード](../upload-serve-static-files.md) します。
1. **URL** に移動します。
1. **新規 \> 新しい URL** を選択します。
1. **新しい URL** ダイアログ ボックスで、**メディア ライブラリ アセット** を選択します。
1. **URL パス** フィールドに URL パスを入力します (入力されていない場合)。 ドメインのベース URL の後に、次の必要な Apple 文字列を入力します: `<domain>/.well-known/apple-developer-merchantid-domain-association.txt`。
1. **次へ** を選択します。 メディア ライブラリには、**ドキュメント** (.txt) タイプのアップロードされたすべてのメディア アセットが表示されます。
1. 先ほど定義した URL への要求に対して提供するドメイン関連ファイルを選択します。
1. **作成** を選択します。

この時点で、作成した URL はドラフト状態になっています。 プロセスを完了するには、URL を公開します。 URL をポイントしたファイルは、URL を発行するまで返されません。

## <a name="configure-a-commerce-online-store-for-apple-pay"></a>Apple Pay 用に Commerce オンライン ストアを構成する

Apple Pay 用に Commerce オンライン ストアを構成するには、次の手順に従います。

1. Commerce 本社で、**小売とコマース\>チャネル\>オンライン店舗** の順に移動します。
1. サイトのオンライン ストア チャネルの **小売チャネル ID** の値を選択します。
1. まだ設定されていない場合は [Adyen 向け Dynamics 365 Payment Connector の設定](adyen-connector-setup.md) の手順に従って、**支払口座** FastTab で、**Adyen 向け Dynamics 365 Payment Connector** を追加します。
1. Adyen コネクタを構成した後、**追加** を選択して **Apple Pay 向け Dynamics 365 Payment Connector** を追加します。
1. コネクタのマーチャント プロパティの値を入力します。

    | プロパティ               | Description | 必須 | 自動セット | サンプル値 |
    | ---------------------- | ----------- | -------- | ----------------- | ------------ |
    | アセンブリ名          | Apple Pay 向け Dynamics 365 Payment Connector のアセンブリ名。 | 有効 | 有効 | バイナリ名 |
    | サービス アカウント ID     | マーチャント プロパティ設定の一意識別子。 この識別子は支払トランザクションで記録され、下位のプロセス (請求など) が使用する商業プロパティを識別します。 | 有効 | 有効 | Guid |
    | マーチャント口座 ID    | 一意の Adyen 商業識別子を入力します。 この値は、[Adyen でサインアップ](adyen-connector-setup.md#sign-up-with-adyen)で説明されているように、Adyen でサインアップするときに提供されます。 | 有効 | 無効 | MerchantIdentifier |
    | クラウド API キー          | Adyen クラウド API キーを入力します。 このキーは、[API キーを取得する方法](https://docs.adyen.com/developers/user-management/how-to-get-the-api-key) の手順に従って取得できます。 | 有効 | 無効 | abcdefg |
    | ゲートウェイ環境    | マップ対称の Adyen ゲートウェイ環境を入力します。 可能な値は **テスト** および **ライブ** です。 このフィールドは、生産デバイスおよびトランザクションでのみ **ライブ** にセットする必要があります。 | 有効 | 有効 | ライブ |
    | サポートされている通貨   | コネクタが処理する必要がある通貨を入力します。 カードありのシナリオでは、Adyen は、トランザクション要求が支払端末に送信された後、[動的通過換算](https://www.adyen.com/pos-payments/dynamic-currency-conversion) により追加通貨をサポートすることができます。 サポートされている通貨の一覧を取得するには、Adyen サポートに問い合わせてください。 | 有効 | 有効 | USD;EUR |
    | サポートされている支払/入金タイプ | コネクタが処理する必要がある支払/入金タイプを入力します。 | 有効 | 有効 | ApplePay |

1. マーチャント情報を入力した後、**1070** チャネル コンフィギュレーション配送スケジュール ジョブを実行します。


### <a name="configure-content-security-policies-in-site-builder"></a>サイト ビルダーのコンテンツ セキュリティ ポリシーを構成する

Apple Pay を使用するフラグメントまたはページを構成する前に、コンテンツ セキュリティ ポリシー (CSPs) がサイトの Commerce サイト ビルダーで構成されていることを確認する必要があります。

コンテンツ セキュリティ ポリシーをサイト ビルダーで構成するには、次の手順に従います。

1. **サイト 設定 \> 拡張機能** に移動します。
1. **コンテンツ セキュリティ ポリシー** タブで **追加** を選択して、**child-src**、**connect-src**、**frame-src**、**img-src**、**script-src**、および **style-src** セクションに `https://applepay.cdn-apple.com/jsapi/v1/apple-pay-sdk.js` の行を追加します。
1. 完了したら、**保存して公開** を選択して、変更をコミットします。

### <a name="set-up-apple-pay-as-a-checkout-payment-option"></a>チェックアウトの決済オプションとして Apple Pay を設定する

サイトの (エクスプレスではない) チェックアウト ページで Apple Pay をチェックアウトの決済オプションとして設定するには、次の手順に従います。

1. サイト ビルダーで **フラグメント** に移動し、サイトのチェックアウト フラグメントを選択します。
1. **編集** を選択します。
1. **セクション コンテナーのチェックアウト** スロットで、省略記号 (**...**) を選択し、**モジュールの追加** を選択します。
1. **モジュールの選択** ダイアログ ボックスで **Apple Pay** モジュールを選択して、**OK** を選択します。
1. **保存** を選択します。
1. **編集の完了** を選択してフラグメントにチェックインし、 **発行** を選択して公開します。

**Apple Pay** モジュールの設定は、モジュールに組み込まれており、Commerce Headquarters のオンライン チャネルに対して設定されている、設定済みの Apple Pay 向け Dynamics 365 Payment Connector のコネクタと接続します。

### <a name="apple-pay-payment-behavior"></a>Apple Pay の支払動作

**Apple Pay** 決済ボタンは、サポートされている Apple Pay デバイス (iPhone、iPad、および Apple Pay をサポートする Safari ブラウザー) にのみ表示されます。 ユーザーがこれらのデバイスを使用していない場合は、**Apple Pay** の決済ボタンは表示されません。

ユーザーが **Apple Pay** 決済ボタンを選択すると、**Apple Pay** ダイアログ ボックスが表示されます。 そこで、ユーザーは Apple Pay デバイスまたはブラウザーに対して認証を行うことができます。 **Apple Pay** ダイアログ ボックスには、注文金額と、ユーザーが Apple Wallet に対して構成した決済方法の概要が表示されます。 ユーザーは、これらの詳細を確認し、**支払** を選択して支払を完了できます。 支払が完了すると、完了したトランザクションの注文の詳細な概要を示す **注文の完了** サイト ページが表示されます。

## <a name="configure-commerce-pos-for-apple-pay"></a>Apple Pay 向けの Commerce POS を構成する

POS 構成には、Adyen 向け Dynamics 365 Payment Connector に対してハードウェア プロファイルの **EFT サービス** フィールドの構成を使用します。 [Dynamics 365 POS ハードウェア プロファイルの設定](adyen-connector-setup.md#set-up-a-dynamics-365-pos-hardware-profile) で説明されているように、Commerce Headquarters で、Adyen 向け Dynamics 365 Payment Connector の EFT サービスを構成します。

**サポートされている支払/入金タイプ** フィールドの支払/入金タイプのリストに **ApplePay** を追加してください。 セミコロン (;) を使用して、一覧で支払/入金タイプを区切ります。

Adyen コネクタのプロセッサ マッピングは、Apple Pay が POS 端末で使用するウォレット カード タイプをキャプチャします。

## <a name="additional-resources"></a>追加リソース

[支払に関するよく寄せられる質問](payments-retail.md)

[チェックアウト モジュール](../add-checkout-module.md)

[支払モジュール](../payment-module.md)
