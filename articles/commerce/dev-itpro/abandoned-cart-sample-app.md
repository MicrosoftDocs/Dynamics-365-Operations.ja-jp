---
title: 破棄されたカートの検出と顧客への通知の送信
description: この記事では、Microsoft Dynamics 365 Commerce の破棄されたカート コネクタ サンプル アプリをカスタマイズして、破棄されたカートを検出し、アラームのメール通知を顧客に送信する方法について説明します。
author: bicyclingfool
ms.date: 02/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 707640ca211e997533d0f5a0b4e6d52cb5be9db4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899213"
---
# <a name="detect-abandoned-carts-and-send-notifications-to-customers"></a>破棄されたカートの検出と顧客への通知の送信

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce の破棄されたカート コネクタ サンプル アプリをカスタマイズして、破棄されたカートを検出し、アラームのメール通知を顧客に送信する方法について説明します。

放棄されたカートの通知によって収益を回復し、顧客を維持する機能は、Dynamics 365 Commerce がサポートする重要な機能です。 コマースの放棄されたカート コネクタのサンプル アプリをカスタマイズすることで、小売業者は小売サーバー上のショッピングカートのうち、小売業者が定義した時間内に変更されていないものにアクセスすることができます。 カートを回収し、商品と顧客のデータを追加して、第三者であるメールマーケティング プロバイダーに渡し、メール通知を作成して顧客に送信することができます。

顧客が受け取るカート放棄のメール通知には、以下の情報を含めることができます:

- 顧客の名前。
- 顧客の姓。
- 顧客のメールアドレス。
- 顧客をカートに戻す URL。
- 取引の通貨。
- 顧客のカートに入る製品のリスト。 各製品については、以下の情報が記載されています:

    - 製品の表示名
    - 商品 ID (商品説明ページへの URL の作成に使用します)
    - さまざまな大きさの大きさに対応するように自動的にサイズを変更できる商品イメージ
    - 商品画像の代替テキスト
    - 商品の単価

## <a name="abandoned-cart-connector-sample"></a>破棄されたカート コネクタのサンプル

マイクロソフトがRetail Software Development Kit (SDK) を通じて提供するコネクタ モデルにより、放棄されたカート情報を取得し、サードパーティのメールマーケティング プロバイダーに送信することができます。 Retail Server との通信、Azure Key Vault によるセキュリティ、指定した時間帯のカート取得のスケジュール設定、注文と商品データの取得を行うコネクタです。 また、サードパーティのメールマーケティング プロバイダーとの統合のための実装例も提供しています。 コネクタは、[Emarsys](https://emarsys.com) とすぐに通信できるように作成されています。 しかし、Constant Contact、Mailchimp、SendGrid など、他のソリューションと統合するように簡単にカスタマイズすることができます。

以下の図は、破棄されたカートコネクタ サンプル アプリの構成要素を示しています。

![破棄されたカート コネクタ サンプル アプリケーションのコンポーネント](media/AbandonedCartConnector.png)

> [!IMPORTANT]
> 地域によっては、顧客がメール マーケティング プロバイダにカートのデータを渡すことを拒否したり、データの削除を要求したりできるようにすることを求めています。 しかし、マイクロソフトはこれらのオプションを顧客には提供していません。 したがって、それを義務付けている地域でビジネスを行う予定であれば、顧客の好みを追跡し、それに基づいて顧客データがメール プラットフォームに渡らないようにするために必要なインフラとカスタマイズを提供する必要があります。 また、顧客の要望に応じて、メールマーケティング プロバイダから顧客データを削除するプロセスを定義する必要があります。

## <a name="obtain-the-code-sample"></a>コード サンプルの入手

破棄されたカート コネクタのサンプル アプリは、バージョン 10.0.16 以降、Retail SDK に含まれています。 このコードは、**\\RetailSDK\\Code\\SampleExtensions\\RetailServer\\Extensions.AbandonedCartSample** にあります。 Retail SDK の詳細と入手先については、[小売 ソフトウェアの開発キット (SDK) のアーキテクチャ](retail-sdk/retail-sdk-overview.md) を参照してください。

> [!NOTE]
> このサンプルコードは、バージョン 10.0.16 のビルドで初めて利用可能になりましたが、バージョン 10.0.13 およびそれ以降の Retail Server のビルドと互換性があります。

## <a name="prerequisites-and-dependencies"></a>前提条件と依存関係

放棄されたカート コネクタのサンプル コードをデプロイして構成する前に、以下の前提条件を満たしている必要があります。

### <a name="access-to-commerce-resources"></a>Commerce リソースへのアクセス

放棄されたカート コネクタ アプリを設定およびデプロイするには、以下の Commerce リソースにアクセスできる必要があります。

- ご利用の環境に合わせた Commerce 本部への管理者アクセス権
- ご利用の環境に合わせた Microsoft Dynamics Lifecycle Services (LCS) プロジェクトにアクセスできます

### <a name="azure-cosmos-db"></a>Azure Cosmos DB

放棄されたカート コネクタ アプリは、Azure Cosmos DB を使用して、過去に取得されたカートの ID およびタイムスタンプを追跡します。 Azure Cosmos DB を使用してこのデータを永続化することもでき、またコードサンプルをカスタマイズして他のデータ ストレージのオプションと統合することもできます。 Azure Cosmos DB の詳細については、[Azure Cosmos DB にようこそ](/azure/cosmos-db/introduction) を参照してください。

Azure Cosmos DB を使用する場合、サンプルを実行する前に以下の前提条件を満たしている必要があります:

- Azure Cosmos DB のアカウントが有効であることが必要です。 アカウントを持っていない場合は、 [データベース アカウントの作成](/azure/cosmos-db/create-sql-api-dotnet#create-a-database-account)を参照してください。
- Azure Cosmos DB アカウントの **キー** ブレードから **URI** と **主キー** (または **セカンダリ キー** ) 値を Azure ポータルで取得する必要があります。 Azure Cosmos DBアカウントのエンドポイントおよびキー情報を取得する方法の詳細については、[アクセス キーと パスワードの表示、コピー、再生成](/azure/cosmos-db/manage-account#keys)を参照してください。

### <a name="azure-key-vault"></a>Azure Key Vault

放棄されたカートのコネクタ アプリは、安全なアクセスを必要とするさまざまなコンポーネントの名前と秘密を保存するためにキー コンテナーを使用しています。

キー コンテナーを設定するには、次の手順を実行します。

1. [ポータルを使用した Azure Stack Hub のキー コンテナーの管理](/azure-stack/user/azure-stack-key-vault-manage-portal?view=azs-2002&preserve-view=true)の手順に従います。
2. 以下の情報を使用して新しい情報を作成します:

    - Emarsys アプリケーション プログラミング インターフェース (API) のユーザー名と API シークレット
    - 放棄されたカートアプリケーションの ID とシークレット

放棄されたカート コネクタのサンプル コードでは、Azure の既定の認証情報を使用してキー コンテナーにアクセスします。 キー コンテナーへのアクセスに使用する予定の ID には、**リスト** 権限と **読み取り** 権限を付与する必要があります。

Azure の既定の資格情報の詳細については、[DefaultAzureCredential クラス](/dotnet/api/azure.identity.defaultazurecredential?view=azure-dotnet&preserve-view=true)を参照してください。

## <a name="create-an-abandoned-cart-connector-sample-app-application-id-for-the-azure-ad-tenant"></a>Azure AD テナントの破棄されたカート コネクタ サンプル アプリのアプリケーション ID を作成します

Azure Active Directory (AD) テナント用の放棄カートコネクタ サンプル アプリのアプリケーション ID を作成する必要があります。 アプリケーション ID の作成方法については、[ポータルを使用して、リソースにアクセスできる Azure AD アプリケーションとサービス プリンシパルを作成する](/azure/active-directory/develop/howto-create-service-principal-portal)を参照してください。

## <a name="add-the-abandoned-cart-connector-sample-app-application-id-to-the-allow-list-for-the-retail-server-api"></a>Retail Server API の許可リストに、放棄されたカート コネクタ サンプル アプリのアプリケーション ID を追加します

続いて、Retail Server API の許可リストに、放棄されたカート コネクタ サンプル アプリのアプリケーション ID を追加刷る必要があります。 Azure でアプリケーション ID を許可リストに追加する方法については、[Retail Server におけるサービス間認証のサポート](https://community.dynamics.com/ax/b/axforretail/posts/support-for-service-to-service-authentication-in-retail-server) を参照してください。

## <a name="configure-the-abandoned-cart-connector-sample-app"></a>破棄されたカート コネクタ サンプル アプリケーションの構成

破棄されたカート コネクタ サンプル アプリの設定は、**AbandonedCartDetectionSample** ディレクトリのルートにある **appSettings.json** 構成ファイルを変更することで行います。 次の表で、構成ファイルのプロパティについて説明します。

### <a name="keyvaultoptions"></a>KeyVaultOptions

| プロパティ    | Description |
| ----------- | ----------- |
| KeyVaultURI | Azure ポータルで使用しているキー ボルトのドメイン ネーム システム (DNS) 名です。 |

### <a name="retailserverclientoptions"></a>RetailServerClientOptions

| プロパティ                                      | Description |
| --------------------------------------------- | ----------- |
| TenantId                                      | ご利用の Azure テナントの Azure AD テナント ID です。 |
| RetailServerAudienceId                        | Retail Server のオーディエンス ID。 既定値のままでもかまいません。 |
| AppIdKeyVaultSecretName                       | 放棄されたカート コネクタ サンプル アプリのアプリケーション ID 用に作成したシークレットの名前です。 |
| AppSecretKeyVaultSecretName                   | 放棄されたカートコネクタ サンプル アプリのアプリ ID のアプリ シークレットを格納するシークレット名です。 |
| RetailServerUrl                               | Retail Server のインスタンスの URL。 この値は LCS で見つけることができます。 |
| オペレーティングユニットナンバー                           | 作業単位番号 (OUN)。 この値は Commerce 本部で見つけることができます。 |
| IncludeAbandonedCartsModifiedSinceLastMinutes | 取得する破棄されたカートの期間の開始時刻。 この値は、現在の時刻の数分前を表示します。 たとえば、このプロパティを **120** に設定すると、120 分前から **ExcludeAbandonedCartsModifiedSinceLastMinutes** プロパティで定義された期間の終わりまでの間に最終更新されたすべてのカートを取得することができます。 |
| ExcludeAbandonedCartsModifiedSinceLastMinutes | 取得する破棄されたカートの期間の終了時刻。 この値は、現在の時刻の数分前を表示します。 たとえば、**IncludeAbandonedCartsModifiedSinceLastMinutes** プロパティが **120** に設定されている場合、このプロパティを **30** に設定すると、120 分前から 30 分前までの間に変更されたすべてのカートを取得することができます。 実際には、このプロパティは、カートが破棄される前に待機する時間数を定義します。 |
| ReturnToCartUrl                               | eコマースサイトのカートの URL で、**app.config** ファイルで使用されている形式です。 |

### <a name="azurecosmosoptions"></a>AzureCosmosOptions

放棄されたカートの検索ジョブ ステータス、カート ID、および変更のタイムスタンプは、Azure Cosmos DB に格納されます。 既定では、構成ファイルの設定は、Azure Cosmos DB のローカル エミュレータのインスタンスを指します。 コネクタを本番環境に配置する際には、これらの設定を更新して、Azure サブスクリプション内の Azure Cosmos DB インスタンスを指す必要があります。 ローカルやサンドボックスでのテストには、[Azure Cosmos DB エミュレーター](/azure/cosmos-db/local-emulator) を使用できます。

| プロパティ    | Description |
| ----------- | ----------- |
| EndPointUri | Azure または Emulator から提供されるエンドポイントの URI。 |
| PrimaryKey  | Azure または Emulator から提供される主キー。 |
| DatabaseId  | データベースの ID。 既定値はそのままにするか、独自の値を指定できます。 |
| ContainerId | コンテナー ID。 既定値はそのままにするか、独自の値を指定できます。 |

### <a name="emarsysclientoptions"></a>EmarsysClientOptions

> [!NOTE]
> Emarsys 以外のメール マーケティング プロバイダと統合する場合は、そのプロバイダと通信するために、必要に応じて **IEmailProvider** インターフェイスを拡張する必要があります。

| プロパティ                      | Description |
| ----------------------------- | ----------- |
| ApiUrl                        | `https://api.emarsys.net/api/v2/event/{0}/trigger` |
| ExternalEventId               | Emarsys で作成される外部イベント レコードの ID です。 放棄されたカートのメール通知を送信するために作成したキャンペーンの **トリガーの設定** の下に値を見つけることができます。 |
| ApiUserNameKeyVaultSecretName | Emarsys API のユーザー名が格納されているキーの名前です。 |
| ApiSecretKeyVaultSecretName   | Emarsys API のシークレットが格納されているキーの名前です。 |
| EmarsysContactKeyId           | Emarsys 連絡先データベースのメールカラムの ID。 既定値は **3** で、変更する必要はありません。 |

### <a name="mediaoptions"></a>MediaOptions

Commerce の e コマース機能を利用している場合、Commerce のデジタル アセット マネジメントを利用して、商品画像を取得することができます。 デジタル資産管理の画像サイズ変更機能の詳細については、[ImageSettings のビューポートの構成](../e-commerce-extensibility/image-component.md#imagesettings-viewport-configuration)を参照してください。

| プロパティ                             | Description |
| ------------------------------------ | ----------- |
| ImageServerUrl                       | サイトのデジタル アセット マネージャーのルート URL。 この値は、Commerce 本部の **Retail と Commerce \> チャネル設定 \> チャネル プロファイル** にある **Media Server Base URL** プロパティ キーで確認することができます。 |
| ImageViewPorts                       | 個々のビューポート構成のためのコンテナ ノード。 |
| ImageViewPorts/viewport              | ビューポートの定義。 このプロパティを使用して、オブジェクトの幅の範囲をピクセル単位で指定します。 このプロパティの使用方法を示す例は、 **appSettings.json** 構成ファイルを参照してください。 |
| ImageViewPorts/imageWidth            | ビューポートの画像幅をピクセル単位で指定します。 |
| imageViewPorts/imageHeight           | ビューポートの画像の高さをピクセル単位で指定します。 |
| imageViewPorts/useForDefaultImageTag | Web ブラウザやメール クライアントで `<picture>`  HTMLタグがサポートされていない場合に、ビューポートで定義される画像の寸法を使用すべきかどうかを示す **true**/**false** の値。 |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
