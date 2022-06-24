---
title: Dynamics 365 Commerce 評価環境のオプション機能のコンフィギュレーション
description: この記事では、Microsoft Dynamics 365 Commerce の評価環境のオプション機能を構成する方法について説明します。
author: psimolin
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 39d4784e21c4fb42ca218d507616d49eff309ee1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861917"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-evaluation-environment"></a>Dynamics 365 Commerce 評価環境のオプション機能のコンフィギュレーション

[!include [banner](includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce の評価環境のオプション機能を構成する方法について説明します。

## <a name="prerequisites"></a>必要条件

トランザクション電子メール機能を評価する場合、次の前提条件を満たす必要があります。

- 評価環境をプロビジョニングする Microsoft Azure のサブスクリプションから使用できるメールサーバー (シンプル メール トランスファー プロトコル \[SMTP\] サーバー) が使用可能です。
- サーバーの完全修飾ドメイン名 (FQDN)/IP アドレス、SMTP ポート番号、および認証の詳細が利用可能です。

## <a name="configure-the-image-back-end"></a>画像バックエンドのコンフィギュレーション

### <a name="find-your-media-base-url"></a>メディア ベース URL の検索

> [!NOTE]
> この手順を完了する前に、[コマースでサイトを設定する](cpe-post-provisioning.md#set-up-your-site-in-commerce) の手順を完了する必要があります。

1. プロビジョニングの実行時に eコマースを初期化した際に作成した URL を使用して、コマース サイトの管理ツールにサイン インします ([eコマースの初期化](provisioning-guide.md#initialize-e-commerce) を参照してください)。
1. **Fabrikam** サイトを開きます。
1. 左側のメニューで、**メディア ライブラリ** を選択します。
1. 1 つの画像資産を選択します。
1. 右側のプロパティ インスペクターで、**公開 URL** プロパティを検索します。 値は URL です。 次に例を示します。

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`。

1. URL の最後の識別子 (前の例では **MA1nQC**) を文字列 **search?fileName=** と置換します。 この変更を行った後の URL の例を次に示します。

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    この URL は、メディア ベース URL です。 記録しておいてください。

### <a name="update-the-media-base-url"></a>メディア ベース URL の更新

1. コマースの本部にサイン インします。
1. 左側のメニューを使用して、**モジュール \> 小売りとコマース \> チャネルの設定 \> チャネル プロファイル** の順に移動します。
1. **編集** を選択します。
1. **プロファイルのプロパティ** で、**メディア サーバー ベース URL** プロパティ値を、以前に作成したメディア ベース URL と置き換えます。
1. 使用可能な他のチャネル **scXXXXXXXXX** を選択します。
1. **プロファイル プロパティ** で、**追加** を選択します。
1. 追加されたプロパティに対して、**メディア サーバー ベース URL** をプロパティ キーとして選択します。 プロパティ値として、以前に作成したメディア ベース URL を入力します。
1. **保存** を選択します。

## <a name="configure-and-test-the-email-server"></a>電子メール サーバーの構成とテストを行います

> [!NOTE]
> ここで入力する SMTP サーバーまたは電子メール サービスは、環境に使用している Azure サブスクリプションからアクセスできる必要があります。

1. コマースの本部にサイン インします。
1. 左側のメニューを使用して、**モジュール  \>  小売とコマース \> 本部の設定 \> パラメーター \> 電子メールパラメーター** に移動します。
1. **SMTP 設定** タブの、**送信メール サーバー** フィールドで、SMTP サーバーまたは電子メールサービスの FQDN または IP アドレスを入力します。
1. **SMTP ポート番号** フィールドで、ポート番号を入力します。 (Secure Sockets Layer \[SSL\] を使用しない場合、既定のポート番号は **25** になります。)
1. 認証が必要な場合は、**ユーザー名** および **パスワード** フィールドに値を入力します。
1. **保存** を選択します。
1. **更新** を選択します。
1. **テスト電子メール** タブの、**電子メール プロバイダー** フィールドで、**SMTP** を選択します。
1. **送信先** フィールドで、テスト電子メールの送信先となる電子メール アドレスを入力します。
1. **テスト電子メールの送信** を選択します。

## <a name="configure-email-templates"></a>電子メール テンプレートのコンフィギュレーション

電子メールを送信する各トランザクション イベントに関しては、有効な送信者の電子メール アドレスで電子メール テンプレートを更新する必要があります。

1. コマースの本部にサイン インします。
1. 左側のメニューを使用して、**モジュール  \>  小売とコマース \> 本部の設定 \> パラメーター \> 組織のメール テンプレート** に移動します。
1. **リストを表示** を選択します。
1. リストの各テンプレートに関しては、次のステップを実行します。

    1. **送信者電子メール** フィールドに、送信者の電子メール アドレスを入力します。
    1. オプション: **送信者名** フィールドに、送信者名として使用する名前を入力します。

1. **保存** を選択します。

## <a name="customize-email-templates"></a>電子メール テンプレートのカスタマイズ

電子メール テンプレートをカスタマイズして、異なる画像を使用するようにできます。 またはテンプレートのリンクを更新して、評価環境に移動することも可能です。 この手順では、既定のテンプレートをダウンロードし、システムのテンプレートを更新する方法について説明します。

1. Web ブラウザーで、[Microsoft Dynamics 365 Commerce 評価版既定の電子メール アドレス テンプレート ZIP ファイル](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip)をローカル コンピューターにダウンロードします。 このファイルには、次の HTML ドキュメントが含まれます。

    - 注文確認モジュール テンプレート
    - ギフト カード テンプレートの発行
    - 新しい注文テンプレート
    - 注文テンプレートのパック
    - 注文テンプレートのピック

1. テキストまたは HTML エディターを使用してテンプレートをカスタマイズします。 この記事の後半にある、[サポートされているトークン](#supported-tokens-in-the-email-template) のリストを参照してください。
1. コマースにサインインします。
1. 左側にあるメニューを使用して、**モジュール \> 組織管理者 \> 設定 \> 組織の電子メール テンプレート** の順に移動します。
1. 左のリストを展開すると、すべてのテンプレートが表示されます。
1. カスタマイズする各テンプレートに関しては、次の手順を実行します。

    1. リストでテンプレートを選択します。
    1. **電子メール メッセージのコンテンツ** で、リストから適切な言語バージョンを選択します。 (既定の言語は **en-us** です。)
    1. **電子メール メッセージ コンテンツ** で、**編集** を選択します。 **電子メール テンプレートのアップロード** ウィンドウが表示されます。
    1. **参照** を選択し、カスタマイズされたコンテンツを含む HTML ファイルを検索します。
    1. **アップロード** を選択します。 テンプレートがシステムにアップロードされ、プレビューが表示されます。
    1. **OK** を選択します。
    1. オプション: テンプレートの **件名** プロパティをカスタマイズします。
    1. **保存** を選択します。

### <a name="supported-tokens-in-the-email-template"></a>電子メール テンプレートでサポートされているトークン

電子メールが表示されると、これらのトークンは顧客と顧客の注文に適用される実際の値に置換されます。

#### <a name="sales-order"></a>販売注文

次のトークンは、販売注文全体に適用されます。

| トークンの名前 | トークン |
|-------------------|-------|
| 注文番号      | %salesid% |
| 顧客の名前   | %customername% |
| 配送先住所  | %deliveryaddress% |
| 請求先住所   | %customeraddress% |
| 注文日付        | %shipdate% |
| 荷渡方法     | %modeofdelivery% |
| 割引          | %discount% |
| 売上税         | %tax% |
| 注文合計       | %total% |

#### <a name="sales-line"></a>販売明細行

次のトークンは、注文の各製品の値に置換されます。

> [!NOTE]
> **製品リスト - 開始** トークンを各製品に対して繰り返される HTML ブロックの先頭に、**製品リスト - 終了** トークンをブロックの末尾に配置します。

| トークンの名前      | トークン |
|------------------------|-------|
| 製品リスト - 開始   | \<!--%tablebegin.salesline% --\> |
| Product list - 終了     | \<!--%tableend.salesline%--\> |
| 製品名           | %lineproductname% |
| 説明            | %lineproductdescription% |
| 件数               | %linequantity% |
| 明細行の単価        | %lineprice% (確認) |
| 明細行の品目合計        | %linenetamount% |
| 明細行割引          | %linediscount% |
| 出荷日              | %lineshipdate% |
| 調達方法     | %linedeliverymode% |
| 配送先住所       | %linedeliveryaddress% |
| 明細行の販売単位 | %lineunit% |

## <a name="additional-resources"></a>追加リソース

[Dynamics 365 Commerce 評価環境の概要](cpe-overview.md)

[Dynamics 365 Commerce 評価環境をプロビジョニングする](provisioning-guide.md)

[Dynamics 365 Commerce の評価環境を構成する](cpe-post-provisioning.md)

[Dynamics 365 Commerce 評価環境で BOPIS を構成する](cpe-bopis.md)

[Dynamics 365 Commerce 評価環境に関するよく寄せられる質問](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure ポータル](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce Web サイト](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]