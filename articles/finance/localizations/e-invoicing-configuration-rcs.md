---
title: Regulatory Configuration Services (RCS) で電子請求アドオンを構成する
description: このトピックでは、Dynamics 365 Regulatory Configuration Services (RCS) で電子請求アドオンを構成する方法について説明します。
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: bb4a426bb54ee21197f9954d946d60ea55f5eb76
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104406"
---
# <a name="configure-the-electronic-invoicing-add-on-in-regulatory-configuration-services-rcs"></a>Regulatory Configuration Services (RCS) で電子請求アドオンを構成する

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/banner.md)]

このトピックでは、Dynamics 365 Regulatory Configuration Services (RCS) の電子請求アドオンの構成機能に関する情報を提供します。

この構成機能を通じて、電子請求書アドオンは、コーディングを行うことなく、電子請求書のビジネス要件および規制要件を満たすことができます。 また、Webサービスで電子請求書を電子的に承認する必要がある場合は、この構成機能を使用して、コードを実行せずに Web サービスとメッセージを交換する要件を満たすことができます。

## <a name="electronic-reporting"></a>電子申告

電子レポート (ER) は、電子請求アドオンに対応しています。

データモデルのマッピングと形式は、ER を通して作成・管理され、電子請求書作成アドオンで使用される構成可能なコンポーネントです。 ER 形式デザイナは、ファイルの形式を作成・管理するためのツールです。 これは、電子請求機能の構成に使用されます。

詳細については、[電子申告 (ER) の概要](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md) を参照してください。

## <a name="electronic-invoicing-features"></a>電子請求の機能

電子請求書機能は、電子請求書アドオンを介して電子請求書を生成する役割を担っています。 これらは構成ルールをカプセル化し、Microsoft Dynamics 365 Finance と Dynamics 365 Supply Chain Management が電子請求書アドオンや電子請求書に送信するデータを処理するために使用します。

この機能はまた、ファイル形式の仕様に準拠する必要があり、出力はスタンドアロンの電子ファイルのシナリオにも対応しています。 ほとんどの場合、指定のファイル形式は税務当局が公開しています。

また、税務当局や認定当事者によってホストされる外部の Web サービスとのメッセージ交換や、電子請求書での認証または承認スタンプの要求に対応しています。

### <a name="availability-of-electronic-invoicing-features"></a>電子請求機能の可用性

電子請求機能の可用性は、国または地域によって異なります。 一般公開されている機能もありますが、プレビュー段階の機能もあります。

#### <a name="preview-features"></a>プレビュー機能

次の表に、現在プレビュー中の電子請求機能をまとめています。

| 国/地域 | 機能名                         | ビジネス ドキュメント |
|----------------|--------------------------------------|-------------------|
| オーストリア        | オーストリア 顧客電子請求書 (AT)    | 売上請求書とプロジェクト請求書 |
| ベルギー        | ベルギー 電子請求書 (BE)      | 売上請求書とプロジェクト請求書 |
| ブラジル         | ブラジル NF-e (BR)                  | 財政文書モデル 55、督促状、取消書、廃棄物 |
| ブラジル         | ブラジル NFS-e ABRASF クリチバ (BR) | 会計ドキュメントのサービス |
| ブラジル         | ブラジル NFS-e サンパウロ (BR)       | 会計ドキュメントのサービス |
| デンマーク        | デンマーク 電子請求書 (DK)       | 売上請求書とプロジェクト請求書 |
| エジプト          | エジプト 電子請求書 (EG) | 売上請求書とプロジェクト請求書 |
| エストニア        | エストニア 電子請求書 (EE)     | 売上請求書とプロジェクト請求書 |
| フィンランド        | フィンランド 電子請求書 (FI)      | 売上請求書とプロジェクト請求書 |
| フランス         | フランス 電子請求書 (FR)       | 売上請求書とプロジェクト請求書 |
| ドイツ        | ドイツ 電子請求書 (DE)       | 売上請求書とプロジェクト請求書 |
| イタリア          | FatturaPA (IT)                       | 売上請求書とプロジェクト請求書 |
| メキシコ         | メキシコ CFDI (MX)                    | 売上請求書、梱包伝票、在庫振替、支払い補完、キャンセル |
| オランダ    | オランダ 電子請求書        | 売上請求書とプロジェクト請求書 |
| ノルウェー         | ノルウェー 電子請求書 (NO)    | 売上請求書とプロジェクト請求書 |
| スペイン          | スペイン 電子請求書 (ES)      | 売上請求書とプロジェクト請求書 |
| ヨーロッパ         | PEPPOL 電子請求書            | PEPPOL 営業の請求書とプロジェクトの請求書 |

### <a name="configurable-components-of-electronic-invoicing-features"></a>電子請求機能のコ構成可能なコンポーネント

電子請求機能は、構成可能なコンポーネントの次のグループで構成されます。

- **形式** - 電子ドキュメントが電子請求書になった際に電子請求アドオンで生成する必要がある機能を構成できます。 形式には、電子請求書の形式構成や、外部の Web サービスとの通信が必要な場合にリクエストの送信やレスポンスの受信に使用するファイルやメッセージの形式設定などがあります。
- **アクション** - アクションを使用すると、Finance および Supply Chain Management が電子請求書に送信した電子ドキュメントの変換をどのように生成されるのかを構成できます。
- **適用ルール** - 適用ルールを使用すると、電子請求アドオンで電子請求機能を処理する際に考慮が必要となるコンテキストを構成できます。
- **変数** - 変数を使用すると、構成ロジックを構築するサポートを構成できます。 変数は、特定のアクションを実行する際の値の入力として機能します。 また、Finance および Supply Chain Management と電子請求アドオン間で値の変換として機能することもできます。
- **電子ドキュメント モデル マッピング** : 電子ドキュメント モデル マッピングを使用すると、ER モデル マッピングを構成できます。 モデル マッピングにより、電子ドキュメントの送信時に電子請求アドオンに統合される抽象請求書のデータ マッピングが定義されます。
- **請求書コンテキスト モデル** - 請求書コンテキスト モデルを使用すると、ER 請求書コンテキスト モデルを構成し、電子請求機能のコンテキストを定義できます。
- **応答タイプ** - 応答タイプを使用すると、電子請求処理の結果として Finance および Supply Chain Management で電子請求アドオンを更新する必要がある項目を設定できます。

### <a name="formats"></a>形式

次の一覧は、電子請求機能に使用可能な ER 形式の構成を示しています。

#### <a name="austrian-at-electronic-invoices-sales-and-project-invoices-for-austria"></a>オーストリア (AT) 電子請求書 : オーストリア向け、売上請求書とプロジェクト請求書

- OIOUBL 売上請求書
- OIOUBL プロジェクト請求書
- OIOUBL 売上訂正票
- OIOUBL プロジェクト訂正票

#### <a name="belgian-be-electronic-invoice-sales-and-project-invoices-for-belgium"></a>ベルギー (BE) 電子請求書 : ベルギー向け、売上請求書とプロジェクト請求書

- UBL 売上請求書 BE
- UBL プロジェクト請求書 BE
- UBL プロジェクト訂正票 BE
- UBL 売上訂正票 BE

#### <a name="brazilian-br-nf-e-nf-e-federal-brazil"></a>ブラジル (BR) NF-e: NF-e Federal (ブラジル)

- NF-e 送信エクスポートの形式 (BR)
- NF-e 督促状エクスポートの形式 (BR)
- NF-e キャンセル エクスポートの形式 (BR)
- NF-e 破棄エクスポートの形式 (BR)

#### <a name="brazilian-nfs-e-br-nfs-e-abrasf-curitiba-city"></a>ブラジル NFS-e (BR): NFS-e ABRASF クリチバ市

- NFS-e ABRASF クリチバ (BR)
- NFS-e ABRASF 調査書 クリチバ (BR)

#### <a name="brazilian-br-nfs-e-nfs-e-so-paulo-city"></a>ブラジル (BR) NFS-e: NFS-e サンパウロ市

- NFS-e サンパウロ (BR)

#### <a name="danish-dk-electronic-invoice-sales-and-project-invoices-for-denmark"></a>デンマーク (BE) 電子請求書 : デンマーク向け、売上請求書とプロジェクト請求書

- OIOUBL 売上請求書
- OIOUBL プロジェクト請求書
- OIOUBL 売上訂正票
- OIOUBL プロジェクト訂正票

#### <a name="dutch-nl-electronic-invoice-sales-and-project-invoices-for-netherlands"></a>オランダ (NL) 電子請求書 : オランダ向け、売上請求書とプロジェクト請求書

- UBL 売上請求書 NL
- UBL プロジェクト請求書 NL
- UBL プロジェクト訂正票 NL
- UBL 売上訂正票 NL

#### <a name="egyptian-eg-electronic-invoice-sales-and-project-invoices-for-egypt"></a>エジプト (BE) 電子請求書 : エジプト向け、売上請求書とプロジェクト請求書

- 売上請求書(EG)(請求書)
- プロジェクト請求書(EG)(請求書)

#### <a name="estonian-ee-electronic-invoice-sales-and-project-invoices-for-estonia"></a>エストニア (BE) 電子請求書 : エストニア向け、売上請求書とプロジェクト請求書

- 売上請求書 (EE)
- プロジェクト請求書 (EE)

#### <a name="finnish-fi-electronic-invoice-sales-and-project-invoices-for-finland"></a>フィンランド (FI) 電子請求書 : フィンランド向け、売上請求書とプロジェクト請求書

- 売上請求書 (FI)
- プロジェクト請求書 (FI)

#### <a name="french-fr-electronic-invoice-sales-and-project-invoices-for-france"></a>フランス (FR) 電子請求書 : フランス向け、売上請求書とプロジェクト請求書

- UBL 売上請求書 FR
- UBL プロジェクト請求書 FR
- UBL プロジェクト訂正票 FR
- UBL 売上訂正票 FR

#### <a name="german-de-electronic-invoice-sales-and-project-invoices-for-germany"></a>ドイツ (DE) 電子請求書 : ドイツ向け、売上請求書とプロジェクト請求書

- 売上請求書 (DE)
- プロジェクト請求書 (DE)

#### <a name="italian-it-electronic-invoice-sales-and-project-invoices-for-italy"></a>イタリア (IT) 電子請求書 : イタリア向け、売上請求書とプロジェクト請求書

- 売上請求書 (IT)
- プロジェクト請求書 (IT)

#### <a name="mexican-mx-cfdi-cfdi-for-mexico"></a>メキシコ (MX) CFDI: メキシコ向け CFDI

- CFDI 請求書フォーマット (MX)
- CFDI 梱包明細 (MX)
- CFDI 在庫振替 (MX)
- CFDI 支払い形式 (MX)
- CFDI 請求書キャンセル形式 (MX)

#### <a name="norwegian-no-electronic-invoice-sales-and-project-invoices-for-norway"></a>ノルウェー (BE) 電子請求書 : ノルウェー向け、売上請求書とプロジェクト請求書

- OIOUBL 売上請求書
- OIOUBL プロジェクト請求書
- OIOUBL 売上訂正票
- OIOUBL プロジェクト訂正票

#### <a name="peppol-electronic-invoice-peppol-sales-and-project-invoices"></a>PEPPOL 電子請求書 :PEPPOL 売上とプロジェクト請求書

- PEPPOL 売上請求書
- PEPPOL プロジェクト請求書
- PEPPOL 売上訂正票
- PEPPOL プロジェクト訂正票

#### <a name="spanish-es-electronic-invoice-sales-and-project-invoices-for-spain"></a>スペイン (ES) 電子請求書 : スペイン向け、売上請求書とプロジェクト請求書

- 売上請求書 (ES)
- プロジェクト請求書 (ES)

### <a name="actions"></a>アクション

次の表では、利用可能なアクションと、現在一般利用可能なのか、プレビュー段階であるのかを示しています。

| 操作                                        | 説明                                                                  | 適用の対象         |
|-----------------------------------------------|------------------------------------------------------------------------------|----------------------|
| ドキュメントの変換                            | 電子レポート形式を実行してドキュメントを変換します。                   | 一般に入手可能  |
| xml ドキュメントへの署名                             | デジタル署名を使用して XML ドキュメントに署名します。                                   | プレビュー           |
| エジプト税務当局に向けた json 文書に署名する | エジプト税務局の電子署名で json 文書に署名します。       | 一般に入手可能  |
| エジプト ETA サービスとの統合           | エジプト税務当局とのやりとりを行います。                                     | 一般に入手可能  |
| ブラジル SEFAZ サービスの呼び出し                  | ブラジルの SEFAZ サービスと統合して会計書類を提出します。       | プレビュー           |
| メキシコ PAC サービスの呼び出し                      | CFDI 提出に向けたメキシコ PAC サービスとの統合を行います。                      | プレビュー           |
| 応答の処理                              | Web サービス コールから受信した応答を分析します。                     | 一般に入手可能  |
| MS Power Automate を使用する                         | Microsoft Power Automate に組み込まれたフローとの統合をします。                       | プレビュー           |

## <a name="configuration-providers"></a>コンフィギュレーション提供者

構成プロバイダーは、電子請求書発行機能とその ER コンポーネント (モデル マッピング、フォーマット構成、コンテキスト モデルなど) を提供します。 関連するグローバル リポジトリで電子請求書発行機能と ER コンポーネントが公開されています。 そこから他の組織がダウンロードできるようになっています。

RCS を介した電子請求書発行機能の構成を行う前に、 **電子レポート** モジュールの構成プロバイダーに独自の組織を構成する必要があります。 構成プロバイダーを **有効化** に設定する方法については、[構成プロバイダーを作成して有効化としてマークする](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md) を参照してください。

## <a name="viewing-electronic-invoicing-features-in-the-global-repository"></a>グローバル リポジトリでの電子請求機能を表示する

特定の構成プロバイダのグローバル リポジトリで利用可能な電子請求書発行機能を閲覧するには、組織の RCS インスタンスを同期します。 同期が完了すると、使用可能な電子請求機能の一覧が更新されます。

## <a name="importing-electronic-invoicing-features"></a>電子請求書機能のインポート

電子請求機能を使用・構成する前に、組織の RCS インスタンスにインポートする必要があります。 インポート操作により、機能のローカル コピーが作成され、機能で使用する ER コンポーネント (構成やモデル構成の書式設定など) が組織の RCS インスタンスにコピーされます。

任意の構成プロバイダから電子請求機能をインポートできます。

## <a name="creating-electronic-invoicing-features"></a>電子請求書機能の作成

ゼロから電子請求書機能を作成することも、別の電子請求書機能から派生させることもできます。

電子請求機能を最初から作成する場合は、ER コンポーネントを手動で追加する必要があります (機能バージョンの構成や、機能バージョンの設定やアプリケーションの設定などのその他構成など)。 別の機能から派生させて機能を作成した場合、この新しい機能は元の機能からすべての構成を引き継ぎます。 

## <a name="electronic-invoicing-feature-version"></a>電子請求書機能のバージョン

電子請求書機能の機能はバージョン管理されています。 新しいバージョンを作成すると、バージョン番号が自動的に増番で付与されます。 新しいバージョンの"有効開始日" を定義できます。

電子請求機能のバージョンは、最大で 3 つのステータスを持つライフサイクルに従います。

- **下書き** - 機能バージョンがこのステータスにある場合、構成の属性とそのコンポーネント (ファイル形式の構成など)を編集できます。
- **完了** - 機能のバージョンがこのステータスの場合は、組織に関連付けられているグローバル リポジトリに公開されている状態を表わします。 機能のバージョン、または ER コンポーネントの編集はできなくなります。
- **公開済** - 機能のバージョンがこのステータスの場合は、電子請求アドオンに発行されています。 機能のバージョン、または ER コンポーネントの編集はできなくなります。

### <a name="feature-configurations"></a>機能の構成

機能の構成には、電子請求機能で使用する ER 形式のすべての構成が保持されます。 電子請求書発行機能が処理中に使用するすべての電子ファイルは、その機能の構成に追加されたフォーマット構成に由来します。

ER 形式デザイナには、機能の構成からアクセスできます。ER 形式デザイナは、形式の構成を作成するために使用する ER ツールです。

### <a name="feature-setup"></a>機能設定

機能の設定は、機能ノ構成と組み合わせて使用されます。 各機能設定は、電子請求書機能が電子請求書の特定の要件を満たせるように、期待される動作を提供するアクション、適用ルール、および変数のセットをカプセル化します。

### <a name="application-setup"></a>アプリケーションの設定

アプリケーションの設定は、既に作成した接続されたアプリケーションに関連付けられている必要があります。

アプリケーションの設定を通じて Finance と Supply Chain Management で行う必要がある電子請求機能の一部を構成できます。 構成可能なコンポーネントは、電子請求の機能を問わず、少なくとも 3 つ必要となります。

- **テーブル名** : 転記された請求書を保持している、Finance と Supply Chain Management のエンティティ、電子請求書機能がベースになっています。
- **コンテキスト** - ER を介して構成された請求書コンテキスト モデルの名前です。
- **ビジネス ドキュメント マッピング** - ER を介して構成された請求書マッピング モデルの名前です。

> [!IMPORTANT]
> アプリケーションの設定で入力された構成は、Finance と Supply Chain Management で表示できます。 **組織管理 \> 設定 \> 電子ドキュメント パラメーター** に移動します。 **電子ドキュメント** タブ で、**デプロイ** を選択し、**接続済みアプリケーション** オプションを選択します。

### <a name="deploying-feature-versions"></a>デプロイ機能のバージョン

RCS では、**デプロイ** コマンドを使用して電子請求機能のバージョンを target-publish します。 **デプロイ** を選択し、次のいずれかのオプションを選択して、デプロイするターゲットを定義します。 

- **サービス環境** - デプロイのターゲットがサービス環境の場合は、電子請求機能のバージョンをサービス環境に公開します。 以上で、電子請求アドオンが、Finance と Supply Chain Management から送信された電子ドキュメントの受信と処理をする準備が整います。
- **接続済アプリケーション** - デプロイのターゲットが接続されたアプリケーションである場合、アプリケーションの設定で提供される構成は、以前に関連付けらた Finance と Supply Chain Management のインスタンスに記述されます。

サービス環境や接続されたアプリケーションにデプロイできるバージョンは、ステータスが **完了** となっておる電子請求機能のバージョンのみです。

### <a name="removing-feature-versions"></a>機能のバージョンを削除する

RCS では、**アンデプロイ** コマンドを使用して、電子請求アドオンのサービス環境から特定の電子請求機能のバージョンを削除します。

> [!IMPORTANT]
> **アンデプロイ** コマンドは、サービス環境でのみ機能します。 接続されたアプリケーションからは、電子請求機能のバージョンは削除されません。

### <a name="rebasing-electronic-invoicing-features"></a>電子請求書発行機能をリベースする

電子請求書の作成機能が別の機能から派生したものである場合、**リベース** コマンドを使用すると、この派生した機能を元の機能に導入された変更を基に更新します。

## <a name="additional-resources"></a>追加リソース

- [Finance および Supply Chain Management で電子請求書を発行する](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]