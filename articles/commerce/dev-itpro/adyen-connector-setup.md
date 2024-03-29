---
title: Adyen 向け Dynamics 365 Payment Connector の設定
description: この記事では、Adyen にサインアップし、Adyen 向け Microsoft Dynamics 365 Payment Connector を設定する方法について説明します。
author: Reza-Assadi
ms.date: 11/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 7.0.1
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.industry: Retail
ms.openlocfilehash: a751cef639cd2212b3777c7cd2ff28da74163f85
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746129"
---
# <a name="set-up-dynamics-365-payment-connector-for-adyen"></a>Adyen 向け Dynamics 365 Payment Connector の設定

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

この記事では、Adyen にサインアップし、Adyen 向け Microsoft Dynamics 365 Payment Connector を設定する方法について説明します。 Adyen 向け Dynamics 365 Payment Connector の概要については [Adyen 向け Dynamics 365 Payment Connector の概要](adyen-connector.md)を参照してください。

## <a name="sign-up-with-adyen"></a>Adyen でサインアップ

Adyen 向け Dynamics 365 Payment Connector を使用するには、Adyen を使用する別の契約を保有している必要があります。 Adyen のサービスの詳細について、またはテスト商業アカウントを作成するには、[Adyen Web サイト](https://www.adyen.com/signup)を参照してください。

## <a name="setup-and-configuration"></a>設定およびコンフィギュレーション

> [!NOTE]
> これらの手順は、既に Adyen で商業口座にサインアップ済みで、Adyen 商業ダッシュ ボードへのアクセス権を保有していることを仮定しています。

> [!IMPORTANT]
> Adyen は、2022 年 10 月現在 [ホスト型決済ページ](https://docs.adyen.com/online-payments/classic-integrations/hosted-payment-pages) をサポートしていません。 Adyen 用 Dynamics 365 Payment Connector を構成する場合、バージョン V001 は、Adyen のホスト型決済ページを使用しているため、コール センターおよび eコマースではサポートされなくなります。 代わりに、V002 (オリジン キー付き) またはバージョン V003 (クライアント キー付き) を使用します。 バージョン V003 は Microsoft によって推奨され、Commerce バージョン 10.0.29 以上で使用できます。 また、サイト (e コマースの場合) または Commerce headquarters (コール センターの場合) に完全なURL (例: 'https://www.adventure-works.com') を追加して、Adyen のコンフィギュレーションで **Allowed Origins** が設定されていることを確認します。

### <a name="prerequisites"></a>必要条件

すべてのチャネルで支払を構成するには、次の前提条件を完了する必要があります。

#### <a name="configure-your-adyen-account-settings-for-dynamics-365-commerce"></a>Dynamics 365 Commerce の Adyen アカウント設定を構成する

次の手順に加えて、Dynamics 365 Commerce の Adyen アカウントの設定を構成する必要があります。 Dynamics 365 Commerce の Adyen の設定手順については、[Dynamics 365 の Adyen 支払コネクタの設定](https://docs.adyen.com/plugins/microsoft-dynamics)を参照してください。

#### <a name="set-up-a-processor-for-new-credit-cards"></a>新しいクレジット カードのプロセッサの設定

販売時点管理 (POS) 端末、コール センター、または Commerce で支払を処理するには、新しいクレジット カードに対して新しい既定の支払プロセッサを構成する必要があります。 次の手順に従って、既定の支払プロセッサを構成します。

1. Commerce 本社にサインインして、**売掛金勘定 \> 支払設定 \> 支払サービス** の順に移動します。
1. アクション ウィンドウで、**新規** を選択してから、**設定** タブに、以下の情報を入力します。

    | フィールド | 説明 | サンプル値 |
    |---|---|---|
    | 支払サービス | 構成する支払サービスの名前を入力します。 | Adyen Payment Service |
    | 支払コネクタ | 新しいクレジット カードの支払に使用する支払コネクタを選択します。 | Adyen 向け Dynamics 365 Payment Connector |
    | テスト モード | Adyen コネクタに関しては、運用環境とテスト環境でこのフィールドを **false** に設定する必要があります。 | false |
    | クレジット カードの既定のプロセッサ | この支払プロセッサが新しいクレジット カードで使用される既定のプロセッサであるかを指定します。 | 有 |
    | ゼロ トランザクションの支払プロセッサをバイパスする | この支払プロセッサが 0 (ゼロ) の量の取引でスキップする必要があるかを指定します。 | 有 |

1. **支払サービス アカウント** タブで、以下の情報を入力します。

    | フィールド | 説明 | 必須 | 自動セット | サンプル値 |
    |---|---|:-:|:-:|---|
    | アセンブリ名 | Adyen 向け Dynamics 365 Payment Connector の自動入力されたアセンブリ名。 | はい | はい | *バイナリ名* |
    | サービス アカウント ID | 商社のプロパティの設定のための自動入力された一意の識別子。 この識別子は支払トランザクションで記録され、下位のプロセス (請求など) が使用する商業プロパティを識別します。 | はい | はい | *Guid* |
    | バージョン | 使用する Adyen 向け Dynamics 365 Payment Connector のバージョンを入力します。 すべての新しい実装にはバージョン "V003" を使用する必要があります。 バージョン "V002" は使用可能で、オリジン キー機能は引き続き Adyen によってサポートされています。 バージョン "V001" はサポートされていません。  | 有効 | 有効 | "V002"/"V003" |
    | ゲートウェイ環境 | マップ対称の Adyen ゲートウェイ環境を入力します。 可能な値は **テスト** および **ライブ** です。 このフィールドは、生産デバイスおよびトランザクションでのみ **ライブ** にセットする必要があります。 | 有 | あり | ライブ |
    | オプション ドメイン | ライブ環境にはオプションのドメインが必要となります。これは、Adyen に連絡して取得する必要があります。 このドメインは、フォーム **[ランダム]-[会社名]** でライブ環境の一意識別子であり、Adyen Customer Area ポータル上の会社のライブ アカウントの **アカウント \> API URL** の下にある API URL 内の接頭語として存在します。 詳細については [ライブ エンドポイント](https://docs.adyen.com/development-resources/live-endpoints) を参照してください。 | ライブのみ | 無効 | Adyen に連絡する |
    | マーチャント口座 ID | 一意の Adyen 商業識別子を入力します。 この値は、[Adyen でサインアップ](#sign-up-with-adyen) セクションで説明されているように、Adyen でサインアップするときに提供されます。 | あり | なし | MerchantIdentifier |
    | ターミナル アーキテクチャ | このフィールドは、`Payment service account` 用 **クラウド** にセットする必要があります。 | 有 | 有 | クラウド |
    | ローカル パスワード フレーズ | このフィールドは、POS 支払端末統合に対してのみ使用され、空白のままにする必要があります。 | 無 | 有 | *このフィールドは空白のままにします。* |
    | ローカル キー識別子 | このフィールドは、POS 支払端末統合に対してのみ使用され、空白のままにする必要があります。 | 無 | 有 | *このフィールドは空白のままにします。* |
    | ローカル キー バージョン | このフィールドは、POS 支払端末統合に対してのみ使用され、空白のままにする必要があります。 | 無 | 有 | *このフィールドは空白のままにします。* |
    | ローカル Cryptor バージョン | Adyen ゲートウェイとやり取りするときに使用する Adyen cryptor バージョンを入力します。 このフィールドは **1** にセットする必要があります。 | 有 | 有 | 1 |
    | クラウド API キー | Adyen クラウド API キーを入力します。 このキーは Adyen Web サイトの [API キーを取得する方法](https://docs.adyen.com/developers/user-management/how-to-get-the-api-key)ページの指示に従い取得することができます。 | 有 | 無 | abcdefg |
    | サポートされている通貨 | コネクタが処理する必要がある通貨を入力します。 カードありのシナリオでは、トランザクション要求が支払端末に送信された後、Adyen は[動的通過換算](https://www.adyen.com/pos-payments/dynamic-currency-conversion) を使用した追加通過をすることができます。 サポートされている通貨の一覧を取得するには、Adyen サポートに問い合わせてください。 | 有 | 有 | USD;EUR |
    | サポートされている支払/入金タイプ | コネクタが処理する必要がある支払/入金タイプを入力します。 | 有 | 有 | Visa;MasterCard;Amex;Discover;Debit |
    | ギフト カード プロバイダー | ギフト カードの処理にコネクタが使用する必要があるギフト カード プロバイダーを入力します。 このフィールドは、大文字小文字を区別します。 | 番号 | 番号 | 「svs」 または 「givex」 |
    | ターミナル ギフト カード エントリ | (*POS のみ*) 顧客は **手動** または **機械に通す** のどちらかを選択できます。 | あり | あり | True/False |
    | E コマースでの支払情報の保存を許可します | (*電子商取引のみ*) サインインしたユーザーに、将来のオンライン購入の支払詳細を保存するためのオプションを提供します。  | あり | あり | True/False |
    | 承認失効期間 (日数) | (*POS のみ*) 承認が失効していると見なされ、取得のためにプロセッサにアクセスする前に拒否されるまでの日数。 | 有効 | 有効 | "7" |
    | オリジン キー ("V002") またはクライアント キー ("V003") | "V002" が指定されたバージョンの場合は、オリジン キーの値が必要です。 このキーを取得する手順については、[オリジン キーを取得する方法](https://docs.adyen.com/user-management/how-to-get-an-origin-key) を参照してください。 "V003" が指定されたバージョンの場合は、クライアント キーの値が必要です。 このキーを取得する手順については、[クライアント キーへの移行](https://docs.adyen.com/development-resources/client-side-authentication/migrate-from-origin-key-to-client-key#switch-to-using-the-client-key) を参照してください。| 有効 | 無効 | *完全なオリジン キーまたはクライアント キー* |
    | EnableRequestProtection | 「カードなし」支払呼び出しに再試行ロジックを追加し、相関する ID を使用した呼び出しの潜在的な重複を減少させます。 「True」の場合、プロバイダー要求に相関する ID が追加され、重複を防ぎます。 「False」の場合、呼び出しは相関する ID または重複保護ロジックなしでプロバイダーに送信されます。 | なし | なし | True/False |
    | 増分取得以外の支払方法 | 承認応答で増分取得をサポートしないカードの種類を識別するために Adyen が使用する支払方法バリアントまたはカードの種類の名前。 [Adyen PaymentMethodVariant](https://docs.adyen.com/development-resources/paymentmethodvariant) に記載されているように、入力された値は、Adyen で参照するために使用される支払方法バリアントまたはカードの種類の文字列と一致している必要があります 。  | なし | なし | "amexcommercial" |

1. **カードの検証値** タブで、**カードの検証値を行う** はそのままで、**カードの検証値を空白とする** を **いいえ** に設定します。 

### <a name="pos-payment-terminal"></a>POS 支払端末

#### <a name="onboard-and-configure-an-adyen-payment-terminal"></a>Adyen 支払端末のオンボードおよび構成

> [!NOTE]
> 次の手順では、Adyen 支払端末へのアクセス権を保持していると仮定します。

Adyen Web サイトの[販売時点管理](https://docs.adyen.com/developers/point-of-sale)ページに移動し、指示に従って Adyen 支払端末をオンボードします。 Adyen 固有のアプリのダウンロードを指示するステップをスキップします。 オンボード プロセス中、各支払端末のための以下の情報を書き留めてください。 この情報は、この記事の後半の [支払端末の IP アドレスおよび EFT POS 登録番号の構成](#configure-the-payment-terminal-ip-address-and-eft-pos-register-number) セクションで必要です。

- 支払端末の IP アドレス
- POIID (POIID はデバイスのシリアル番号およびモデル番号で構成されます。 これはデバイスを一意に識別するために使用されます。)

支払端末のオンボード後、[Adyen の顧客領域](https://ca-test.adyen.com/ca/ca/login.shtml)にサインインして、構成対称の端末に移動し、各支払端末のための以下の情報を書き留めてください。 この情報は、記事の後半の [ローカル ネットワーク通信用の EFT サービス](#eft-service-for-local-network-communication) セクションで必要になります。

- キー識別子
- キー パスフレーズ
- キー バージョン

#### <a name="set-up-a-dynamics-365-pos-hardware-profile"></a>Dynamics 365 POS ハードウェア プロファイルの設定

1. Commerce 本社にサインインして、**Retail と Commerce \> チャネル設定 \> POS 設定 \> POS プロファイル \> ハードウェア プロファイル** の順に移動します。
1. Adyen 向け Dynamics 365 Payment Connector を追加するためのハードウェア プロファイルを選択します。
1. [EFT サービス](#eft-service)、および続く [PIN パッド](#configure-the-pin-pad) セクションの手順に従います。

#### <a name="eft-service"></a>EFT サービス

Adyen 支払コネクタは、ローカル ネットワーク経由または Adyen のバックエンドのクラウドを介して、デバイスと通信するように構成できます。 インターネット サービスが依存しない環境またはオフライン モードが必要な環境では、**ローカル** 設定を使用する必要があります。 インターネット接続が強い環境や支払ターミナルに静的 IP アドレスを割り当てできない場合は、**クラウド** アーキテクチャが最適です。

##### <a name="eft-service-for-local-network-communication"></a>ローカル ネットワーク通信用の EFT サービス

1. **EFT サービス** クイックタブの、**EFT サービス** フィールドで、**支払コネクタ** を選択します。
1. **コネクタ** タブで、**新規** を選択してから、**コネクタ** フィールドで、**Adyen 向け Dynamics 365 Payment Connector** を選択します。 **順序番号** フィールドで内の値が他のコネクタの値より小さいことを確認してください。
1. **コネクタ プロパティ** セクションで、以下の情報を入力します。

    | フィールド | 説明 | 必須 | 自動セット | サンプル値 |
    |---|---|:-:|:-:|---|
    | アセンブリ名 | Adyen 向け Dynamics 365 Payment Connector の自動入力されたアセンブリ名。 | はい | はい | *バイナリ名* |
    | サービス アカウント ID | 商社のプロパティの設定のための自動入力された一意の識別子。 この識別子は支払トランザクションで記録され、下位のプロセス (請求など) が使用する商業プロパティを識別します。 | あり | あり | *Guid* |
    | バージョン | ハードウェア プロファイルの EFT 設定を、**V001** に設定します。 **V002** は、コール センターとストアフロントにのみ必要です。  | あり | あり | 「V001」 |
    | ゲートウェイ環境 | マップ対称の Adyen ゲートウェイ環境を入力します。 可能な値は **テスト** および **ライブ** です。 このフィールドは、生産デバイスおよびトランザクションでのみ **ライブ** にセットする必要があります。 | 有 | あり | ライブ |
    | オプション ドメイン | ライブ環境にはオプションのドメインが必要となります。これは、Adyen に連絡して取得する必要があります。 このドメインは、形式 **[ランダム]-[会社名]** でライブ環境の一意識別子であり、Adyen Customer Area ポータル上の会社のライブ アカウントの **アカウント \> API URL** の下にある API URL 内の接頭語として存在します。 詳細については [ライブ エンドポイント](https://docs.adyen.com/development-resources/live-endpoints) を参照してください。| ライブのみ | 無効 | Adyen に連絡する |
    | マーチャント口座 ID | 一意の Adyen 商業識別子を入力します。 この値は、[Adyen でサインアップ](#sign-up-with-adyen) セクションで説明されているように、Adyen でサインアップするときに提供されます。 | 有 | 無効 | MerchantIdenfier |
    | ターミナル アーキテクチャ | ローカル通信端末の場合、このフィールドは **ローカル** に設定する必要があります。 別のターミナル API アーキテクチャの詳細については、Adyen Web サイトの[ターミナル API の導入](https://www.adyen.com/blog/introducing-the-terminal-api)ページを参照してください。 | 有 | 有 | ローカル |
    | ローカル パスワード フレーズ | 支払端末の Adyen キー パスフレーズを入力します。 この値は、[Adyen でサインアップ](#sign-up-with-adyen) セクションで説明されているように、Adyen でサインアップするときに提供されます。 | 有 | 無 | keypassphrase123 |
    | ローカル キー識別子 | 支払端末の Adyen キー識別子を入力します。 この値は、[Adyen でサインアップ](#sign-up-with-adyen) セクションで説明されているように、Adyen でサインアップするときに提供されます。 | 有 | 無 | mykey |
    | ローカル キー バージョン | 支払端末の Adyen キー バージョンを入力します。 この値は、[Adyen でサインアップ](#sign-up-with-adyen) セクションで説明されているように、Adyen でサインアップするときに提供されます。 | 有 | 無 | 0 |
    | ローカル Cryptor バージョン | Adyen ゲートウェイとやり取りするときに使用する Adyen cryptor バージョンを入力します。 このフィールドは **1** にセットする必要があります。 | 有 | 有 | 1 |
    | クラウド API キー | Adyen クラウド API キーを入力します。 このキーは Adyen Web サイトの [API キーを取得する方法](https://docs.adyen.com/developers/user-management/how-to-get-the-api-key)ページの指示に従い取得することができます。 ローカル ターミナルの設定でも、このフィールドは必須です。 | 有効 | 無効 | abcdefg |
    | サポートされている通貨 | コネクタが処理する必要がある通貨を入力します。 カードありのシナリオでは、トランザクション要求が支払端末に送信された後、Adyen は[動的通過換算](https://www.adyen.com/pos-payments/dynamic-currency-conversion) を使用した追加通過をすることができます。 サポートされている通貨の一覧を取得するには、Adyen サポートに問い合わせてください。 | 有 | 有 | USD;EUR |
    | サポートされている支払/入金タイプ | コネクタが処理する必要がある支払/入金タイプを入力します。 これらの値は、大文字と小文字を区別します。 | あり | あり | Visa;MasterCard;Amex;Discover;Debit |
    | ギフト カード プロバイダー | ギフト カードの処理にコネクタが使用する必要があるギフト カード プロバイダーを入力します。 このフィールドは、大文字小文字を区別します。 | 番号 | 番号 | 「svs」 または 「givex」 |    
    | ターミナル ギフト カード エントリ | (*POS のみ*) 顧客は **手動** または **機械に通す** のどちらかを選択できます。 | あり | あり | True/False |
    | E コマースでの支払情報の保存を許可します | (*電子商取引のみ*) サインインしたユーザーに、将来のオンライン購入の支払詳細を保存するためのオプションを提供します。  | あり | あり | True/False |
    | 承認失効期間 (日数) | (*POS のみ*) 承認が失効していると見なされ、取得のためにプロセッサにアクセスする前に拒否されるまでの日数。 | あり | あり | "7" |
    | 元のキー | (*カードは存在しません*)  |
    | EnableRequestProtection | 「カードなし」支払呼び出しに再試行ロジックを追加し、相関する ID を使用した呼び出しの潜在的な重複を減少させます。 「True」の場合、プロバイダー要求に相関する ID が追加され、重複を防ぎます。 「False」の場合、呼び出しは相関する ID または重複保護ロジックなしでプロバイダーに送信されます。 | なし | なし | True/False |
    | 増分取得以外の支払方法 | 承認応答で増分取得をサポートしないカードの種類を識別するために Adyen が使用する支払方法バリアントまたはカードの種類の名前。 [Adyen PaymentMethodVariant](https://docs.adyen.com/development-resources/paymentmethodvariant) に記載されているように、入力された値は、Adyen で参照するために使用される支払方法バリアントまたはカードの種類の文字列と一致している必要があります 。  | 無効 | 無効 | "amexcommercial" |

1. アクション ウィンドウで、**保存** を選択します。

> [!NOTE]
> ローカル POS インスタンスを設定する場合、"カードなし" シナリオが機能するには、**クラウド API** キー フィールドが引き続き必要です。 このようなシナリオには、POS で作成されたオムニチャネル支払の顧客注文、リンクされた払戻、注文集荷での支払認証トークン参照などがあります。

##### <a name="eft-service-for-cloud-communication"></a>クラウド通信用 EFT サービス

1. **EFT サービス** クイックタブの、**EFT サービス** フィールドで、**支払コネクタ** を選択します。
1. **コネクタ** タブで、**新規** を選択してから、**コネクタ** フィールドで、**Adyen 向け Dynamics 365 Payment Connector** を選択します。 **順序番号** フィールドで内の値が他のコネクタの値より小さいことを確認してください。
1. **コネクタ プロパティ** セクションで、以下の情報を入力します。

    | フィールド | 説明 | 必須 | 自動セット | サンプル値 |
    |---|---|:-:|:-:|---|
    | アセンブリ名 | Adyen 向け Dynamics 365 Payment Connector の自動入力されたアセンブリ名。 | はい | はい | *バイナリ名* |
    | サービス アカウント ID | 商社のプロパティの設定のための自動入力された一意の識別子。 この識別子は支払トランザクションで記録され、下位のプロセス (請求など) が使用する商業プロパティを識別します。 | あり | あり | *Guid* |
    | バージョン | ハードウェア プロファイルの EFT 設定を、**V001** に設定します。 **V002** は、コール センターとストアフロントにのみ必要です。  | あり | あり | 「V001」 |
    | ゲートウェイ環境 | マップ対称の Adyen ゲートウェイ環境を入力します。 可能な値は **テスト** および **ライブ** です。 このフィールドは、生産デバイスおよびトランザクションでのみ **ライブ** にセットする必要があります。 | 有 | あり | ライブ |
    | オプション ドメイン | ライブ環境にはオプションのドメインが必要となります。これは、Adyen に連絡して取得する必要があります。 このドメインは、形式 **[ランダム]-[会社名]** でライブ環境の一意識別子であり、Adyen Customer Area ポータル上の会社のライブ アカウントの **アカウント \> API URL** の下にある API URL 内の接頭語として存在します。 詳細については [ライブ エンドポイント](https://docs.adyen.com/development-resources/live-endpoints) を参照してください。| ライブのみ | 無効 | Adyen に連絡する |
    | マーチャント口座 ID | 一意の Adyen 商業識別子を入力します。 この値は、[Adyen でサインアップ](#sign-up-with-adyen) セクションで説明されているように、Adyen でサインアップするときに提供されます。 | 有 | 無効 | MerchantIdenfier |
    | ターミナル アーキテクチャ | このフィールドは、支払端末とのクラウド通信用に、**クラウド** に設定する必要があります。 別のターミナル API アーキテクチャの詳細については、Adyen Web サイトの[ターミナル API の導入](https://www.adyen.com/blog/introducing-the-terminal-api) ページを参照してください。 | あり | あり | クラウド |
    | ローカル パスワード フレーズ | この設定は、ローカル支払ターミナル通信にのみ使用されます。 | なし | なし | *空白のまま* |
    | ローカル キー識別子 | この設定は、ローカル支払ターミナル通信にのみ使用されます。 | なし | なし | *空白のまま* |
    | ローカル キー バージョン | この設定は、ローカル支払ターミナル通信にのみ使用されます。 | なし | なし | *空白のまま* |
    | ローカル Cryptor バージョン | この設定は、ローカル支払ターミナル通信にのみ使用されます。 既定値は、**1** のままにできます。 | あり | あり | 1 |
    | クラウド API キー | Adyen クラウド API キーを入力します。 このキーは Adyen Web サイトの [API キーを取得する方法](https://docs.adyen.com/developers/user-management/how-to-get-the-api-key)ページの指示に従い取得することができます。 | 有 | 無 | abcdefg |
    | サポートされている通貨 | コネクタが処理する必要がある通貨を入力します。 カードありのシナリオでは、トランザクション要求が支払端末に送信された後、Adyen は[動的通過換算](https://www.adyen.com/pos-payments/dynamic-currency-conversion) を使用した追加通過をすることができます。 サポートされている通貨の一覧を取得するには、Adyen サポートに問い合わせてください。 | 有 | 有 | USD;EUR |
    | サポートされている支払/入金タイプ | コネクタが処理する必要がある支払/入金タイプを入力します。 これらの値は、大文字と小文字を区別します。 | あり | あり | Visa;MasterCard;Amex;Discover;Debit |
    | ギフト カード プロバイダー | ギフト カードの処理にコネクタが使用する必要があるギフト カード プロバイダーを入力します。 このフィールドは、大文字小文字を区別します。 | 番号 | 番号 | 「svs」 または 「givex」 |    
    | ターミナル ギフト カード エントリ | (*POS のみ*) 顧客は **手動** または **機械に通す** のどちらかを選択できます。 | あり | あり | True/False |
    | E コマースでの支払情報の保存を許可します | (*電子商取引のみ*) サインインしたユーザーに、将来のオンライン購入の支払詳細を保存するためのオプションを提供します。  | あり | あり | True/False |
    | 承認失効期間 (日数) | (*POS のみ*) 承認が失効していると見なされ、取得のためにプロセッサにアクセスする前に拒否されるまでの日数。 | あり | あり | "7" |
    | 元のキー | (*カードは存在しません*) |
    | EnableRequestProtection | 「カードなし」支払呼び出しに再試行ロジックを追加し、相関する ID を使用した呼び出しの潜在的な重複を減少させます。 「True」の場合、プロバイダー要求に相関する ID が追加され、重複を防ぎます。 「False」の場合、呼び出しは相関する ID または重複保護ロジックなしでプロバイダーに送信されます。 | なし | なし | True/False |
    | 増分取得以外の支払方法 | 承認応答で増分取得をサポートしないカードの種類を識別するために Adyen が使用する支払方法バリアントまたはカードの種類の名前。 [Adyen PaymentMethodVariant](https://docs.adyen.com/development-resources/paymentmethodvariant) に記載されているように、入力された値は、Adyen で参照するために使用される支払方法バリアントまたはカードの種類の文字列と一致している必要があります 。  | なし | なし | "amexcommercial" |

1. アクション ウィンドウで、**保存** を選択します。

##### <a name="configure-the-pin-pad"></a>PIN パッドの構成

1. **PIN パッド** クイックタブの、**PIN パッド** フィールドで、**ネットワーク** を選択します。
1. **デバイス名** フィールドに、**MicrosoftAdyenDeviceV001** と入力します。

#### <a name="set-up-a-dynamics-365-register"></a>Dynamics 365 レジスターの設定

> [!NOTE]
> 次の手順では、POS レジスターと Adyen 支払端末の間の専用マッピングがあることを前提としています。 Microsoft インターネット インフォメーション サービス (IIS) に基づくハードウェア ステーションの場合、**小売とコマース\>チャネル\>店舗\>すべての小売店舗** に移動して、設定対象の店舗を選択します。 次に、その店舗のページの、**ハードウェア ステーション** クイック タブで、同じ手順を実行します。

複数のハードウェア ステーションで支払端末を使用することはできません。 支払端末を複数の POS デバイスで共有する必要がある場合は、支払端末との通信を管理するために、IIS ハードウェア ステーションを配置する必要があります。 

##### <a name="configure-the-payment-terminal-ip-address-and-eft-pos-register-number"></a>支払端末の IP アドレスおよび EFT POS レジスター番号の構成

1. Commerce 本社で、**Retail と Commerce \> チャネル設定 \> POS 設定 \> レジスター** の順に移動します。
1. Adyen 支払端末にリンクするレジスターを選択します。
1. **POS レジスター** ページの、**一般** クイックタブの、**EFT** セクションの、**EFT POS レジスター番号** フィールドに、一意の番号を入力します。 
1. **プロファイル** セクションの **ハードウェア プロファイル** フィールドでは、以前構成したハードウェア プロファイルを選択します。
1. 変更を保存します。
1. アクション ウィンドウで、**レジスター** タブの、**ハードウェア** グループで、**IP アドレスのコンフィギュレーション** を選択します。
    1. **"ローカル" アーキテクチャを使用する場合:** **IP アドレス** フィールドの **PIN パッド** クイックタブの **IP アドレスのコンフィグレーション** ページで、次のフォーマットにあるターミナルの IP アドレスを入力します: `https://<IP address>:8443/nexo/<POIID>`。 **\<IP address\>** および **\<POIID\>** は、Adyen 支払端末をオンボードした際にメモした値です (例: `https://192.168.1.3:8443/nexo/MX925-123456789`)。 この URL の値は、大文字と小文字を区別します。
    1. **"クラウド" アーキテクチャを使用している場合:** **IP アドレス** フィールドの **PIN パッド** FastTab の **IP アドレス コンフィグレーション** ページで、Adyen 支払端末にオンボードした際にメモした **POIID** 値を入力します (例: `MX925-123456789`)。 このフィールドの値は、大文字と小文字を区別します。
1. 支払ターミナルにオンボード プリンターが用意され、そのプリンターを使用してプロセッサからのレシートを印刷する場合は、**PIN パッド** クイックタブの **IP アドレス** フィルダーとは別の **ポート** フィルダーに、**123** と入力します。

#### <a name="update-the-modern-pos-or-iis-hardware-station-configuration"></a>Modern POS または IIS ハードウェア ステーションのコンフィギュレーションの更新

Retail SDK を使用して Modern POS バージョンをパッキングする場合、インストーラーがパッケージ化される前に、SDK コードで 1 回のみこれらの手順を実行する必要があります。 それ以外の場合、標準 Modern POS または IIS ハードウェア ステーションがインストールされた後にこれらの手順を実行する必要があります。

1. **dllhost.exe.config** ファイル (Modern POS の場合) または **web.config** ファイル (IIS ハードウェア ステーションの場合) を開きます。
1. 個々に示すように、**PreloadedComposition** セクションを更新して、旧式の支払デバイス アダプターから標準支払デバイス アダプターに切替えます。

    ``` xml
    <PreloadedComposition>
        <composition>
            <add source="assembly" value="Microsoft.Dynamics.Commerce.HardwareStation.Peripherals.PaymentDeviceAdapter" />
            <!-- Switch from legacy to standard Payment Device Adapter.
            <add source="assembly" value="Microsoft.Dynamics.Commerce.HardwareStation.Peripherals.Legacy.PaymentDeviceAdapter" />
            -->
        </composition>
    </PreloadedComposition>
    ```
1. **appSettings** 変数の **"PrintReceiptsOnCardDeclineOrVoid"** 値を **True** に更新して、プロセッサからの応答を印刷拒否または印刷無効にします。 

### <a name="configure-the-connector-for-call-center-payments"></a>コール センター支払用のコネクタの構成

コール センターの支払のために Adyen 向け Dynamics 365 Payment Connector を構成するには、この記事の前半の[新しいクレジット カードのプロセッサの設定](#set-up-a-processor-for-new-credit-cards)セクションの指示に従います。

**売掛金勘定 \> 支払の設定 \> 支払サービス** での headquarters の構成は、コール センターで使用されるコネクタ構成です。 3D セキュア (3DS) 認証はコール センターでサポートされていません。 コール センターの担当者が顧客の代わりにユーザー パスワードを収集または使用することは禁止されているので、ユーザーにサインインを要求するデジタル ウォレットの最新の支払方法も、コール センターではサポートされていません。

### <a name="configure-additional-information-for-the-connector"></a>コネクタの追加情報を構成する

Commerce 本社でコネクタの追加情報を構成するには、次の手順を実行します。

1. **Retail と Commerce \> チャネル \> オンライン ストア** に移動します。
1. Adyen 向け Dynamics 365 Payment Connector を追加するオンライン店舗を選択します。
1. **オンライン店舗** ページの、**支払口座** クイック タブで、**追加** を選択します。
1. **コネクタ** フィールドで、**Adyen 向け Dynamics 365 Payment Connector** を選択します。
1. 以下の追加情報を入力します。

    | フィールド | 説明 | 必須 | 自動セット | サンプル値 |
    |---|---|:-:|:-:|---|
    | アセンブリ名 | Adyen 向け Dynamics 365 Payment Connector の自動入力されたアセンブリ名。 | はい | はい | *バイナリ名* |
    | サービス アカウント ID | 商社のプロパティの設定のための自動入力された一意の識別子。 この識別子は支払トランザクションで記録され、下位のプロセス (請求など) が使用する商業プロパティを識別します。 | はい | はい | *Guid* |
    | バージョン | 使用する Adyen 向け Dynamics 365 Payment Connector のバージョンを入力します。 すべての新しい実装にはバージョン "V003" を使用する必要があります。 バージョン "V002" は使用可能で、オリジン キー機能は引き続き Adyen によってサポートされています。 バージョン "V001" はサポートされていません。  | 有効 | 有効 | "V002"/"V003" |
    | ゲートウェイ環境 | マップ対称の Adyen ゲートウェイ環境を入力します。 可能な値は **テスト** および **ライブ** です。 | 有 | 有 | ライブ |
    | オプション ドメイン | 支払要求が Adyen に実行されるときに使用するドメインを入力します。 このドメインは、形式 **[ランダム]-[会社名]** でライブ環境の一意識別子であり、Adyen Customer Area ポータル上の会社のライブ アカウントの **アカウント \> API URL** の下にある API URL 内の接頭語として存在します。 詳細については [ライブ エンドポイント](https://docs.adyen.com/development-resources/live-endpoints) を参照してください。 | ライブのみ | 無効 | Adyen に連絡する |
    | マーチャント口座 ID | 一意の Adyen 商業識別子を入力します。 この値は、[Adyen でサインアップ](#sign-up-with-adyen) セクションで説明されているように、Adyen でサインアップするときに提供されます。 | 有 | 無 | MerchantIdenfier |
    | ターミナル アーキテクチャ | このフィールドは、POS 支払端末統合に対してのみ使用され、空白のままにする必要があります。 | 無 | 有 | *このフィールドは空白のままにします。* |
    | ローカル パスワード フレーズ | このフィールドは、POS 支払端末統合に対してのみ使用され、空白のままにする必要があります。 | 無 | 有 | *このフィールドは空白のままにします。* |
    | ローカル キー識別子 | このフィールドは、POS 支払端末統合に対してのみ使用され、空白のままにする必要があります。 | 無 | 有 | *このフィールドは空白のままにします。* |
    | ローカル キー バージョン | このフィールドは、POS 支払端末統合に対してのみ使用され、空白のままにする必要があります。 | 無 | 有 | *このフィールドは空白のままにします。* |
    | ローカル Cryptor バージョン | Adyen ゲートウェイとやり取りするときに使用する Adyen cryptor バージョンを入力します。 このフィールドは **1** にセットする必要があります。 | 有 | 無 | 1 |
    | クラウド API キー | Adyen クラウド API キーを入力します。 このキーは Adyen Web サイトの [API キーを取得する方法](https://docs.adyen.com/developers/user-management/how-to-get-the-api-key)ページの指示に従い取得することができます。 | 有 | 無 | *完全なクラウド API キー* |
    | サポートされている通貨 | コネクタが処理する必要がある通貨を入力します。 | 有 | 有 | USD;EUR |
    | サポートされている支払/入金タイプ | コネクタが処理する必要がある支払/入金タイプを入力します。 | 有 | 有 | Visa;MasterCard;Amex;Discover;Debit |
    | ギフト カード プロバイダー | ギフト カードの処理にコネクタが使用する必要があるギフト カード プロバイダーを入力します。 可能な値は **SVS** および **GIVEX** です。 | 番号 | 番号 | SVS |
    | ターミナル ギフト カード エントリ | (POS のみ*) 顧客は **手動** または **機械に通す** のどちらかを選択できます。 | あり | あり | True/False |
    | E コマースでの支払情報の保存を許可します | (*電子商取引のみ*) サインインしたユーザーに、将来のオンライン購入の支払詳細を保存するためのオプションを提供します。  | あり | あり | True/False |
    | 承認失効期間 (日数) | (*POS のみ*) 承認が失効していると見なされ、取得のためにプロセッサにアクセスする前に拒否されるまでの日数。 | 有効 | 有効 | "7" |
    | オリジン キー ("V002") またはクライアント キー ("V003") | (*eコマースのみ*) '"V002" が指定されたバージョンの場合は、オリジン キーの値が必要です。 このキーを取得する手順については、[オリジン キーを取得する方法](https://docs.adyen.com/user-management/how-to-get-an-origin-key) を参照してください。 "V003" が指定されたバージョンの場合は、クライアント キーの値が必要です。 このキーを取得する手順については、[クライアント キーへの移行](https://docs.adyen.com/development-resources/client-side-authentication/migrate-from-origin-key-to-client-key#switch-to-using-the-client-key) を参照してください。 | 有効 | 無効 | *完全なオリジン キーまたはクライアント キー* |
    | EnableRequestProtection | 「カードなし」支払呼び出しに再試行ロジックを追加し、相関する ID を使用した呼び出しの潜在的な重複を減少させます。 「True」の場合、プロバイダー要求に相関する ID が追加され、重複を防ぎます。 「False」の場合、呼び出しは相関する ID または重複保護ロジックなしでプロバイダーに送信されます。 | なし | なし | True/False |
    | 増分取得以外の支払方法 | 承認応答で増分取得をサポートしないカードの種類を識別するために Adyen が使用する支払方法バリアントまたはカードの種類の名前。 [Adyen PaymentMethodVariant](https://docs.adyen.com/development-resources/paymentmethodvariant) に記載されているように、入力された値は、Adyen で参照するために使用される支払方法バリアントまたはカードの種類の文字列と一致している必要があります 。  | なし | なし | "amexcommercial" |

1. アクション ウィンドウで、**保存** を選択します。

## <a name="next-steps"></a>次のステップ

Adyen 向け Dynamics 365 Payment Connector に関する、よくあるご質問への回答については [Adyen 向け Dynamics 365 Payment Connector の FAQ](adyen-connector-faq.md) を参照してください。

## <a name="additional-resources"></a>追加リソース

[Adyen 向け Dynamics 365 Payment Connector の概要](adyen-connector.md)

[Adyen 向け Dynamics 365 Payment Connector に関するよく寄せられる質問](adyen-connector-faq.md)

[Adyen 向け Dynamics 365 Payment Connector のトラブルシューティング](adyen-connector-troubleshoot.md)

[支払に関するよく寄せられる質問](/dynamics365/unified-operations/retail/dev-itpro/payments-retail)

[!INCLUDE [footer-include](../../includes/footer-banner.md)]
