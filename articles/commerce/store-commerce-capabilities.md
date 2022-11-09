---
title: Store Commerce アプリの機能
description: この記事では、Microsoft Dynamics 365 Commerce 向け Store Commerce アプリで使用できる機能について説明します。
author: anupamar-ms
ms.date: 10/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2022-09-30
ms.openlocfilehash: d713cc0e9537ae20ffddee6e77779a16e74bd779
ms.sourcegitcommit: eb9a53d5cf10f1ada68757536d6a94b2cb00929d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2022
ms.locfileid: "9725638"
---
# <a name="store-commerce-app-capabilities"></a>Store Commerce アプリの機能

[!include [banner](includes/banner.md)]

Store Commerce アプリは Microsoft Dynamics 365 Commerce 向けの最新の販売時点管理 (POS) エクスペリエンスです。 このアプリを使用すると、店舗内のトランザクションを処理し、在庫や注文処理などのバックオフィス操作を管理することができます。 また、ロイヤルティとクライアンテリングを使用して顧客リレーションシップを管理できます。 

Commerce Scale Unit (CSU) を備えた Store Commerce アプリは、オムニチャネル ソリューションを提供します。 たとえば、顧客がオンラインで製品を購入し、それを近くの店舗で受け取ることで、データを失わずにチャネル全体で買い物を続けることができます。 

この記事では、Store Commerce アプリ機能の概要について説明します。

## <a name="platform"></a>プラットフォーム

| 能力 | Description | ドキュメント | 追加コンテンツ |
|---|---|---|---|
| オムニチャネル | Dynamics 365 Commerce は、バックオフィス、店舗、コール センター、デジタル経験を統合する包括的なオムニチャネル ソリューションを提供します。 | [概要](index.md) | [技術解説](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/dynamics-365-commerce-overview-november-2-2020) |
| ヘッドレス コマース | Commerce Scale Unit は、ヘッドレス コマース エンジンをホストします。 すべてのコマース ビジネス ロジックの中心ポイントとして機能するヘッドレス コマース エンジンは、完全なオムニチャネル ソリューションを提供します。 | <p>[アーキテクチャの概要](commerce-architecture.md)</p><p>[ヘッドレス アーキテクチャ](dev-itpro/retail-server-architecture.md)</p> | [技術解説](https://community.dynamics.com/365/b/techtalks/posts/dynamics-365-commerce-architecture-overview-december-4-2020) |
| Commerce headquarters | Commerce headquarters は、業務に必要な製品、従業員、業務プロセス、価格、およびその他の機能の構成を可能とするバックオフィス機能を提供します。 | [アーキテクチャの概要](commerce-architecture.md) | |
| 販売時点管理 (POS) | Store Commerce アプリは、Dynamics 365 Commerce 向け POS エクスペリエンスです。 また、豊富な特徴を持ち合わせる包括的な POS 機能を利用することで、販売担当者、レジ担当者、マネージャーは優れた顧客サービスを提供することができます。 さらに、小売業者にはさまざまな配置オプションが用意されているため、パフォーマンスとアプリケーションのライフサイクル管理 (ALM) を向上させることができます。 | [Store Commerce アプリ](dev-itpro/store-commerce.md) | <p>[技術解説](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/modernize-the-dynamics-365-commerce-in-store-technology-using-the-new-store-commerce-app-march-30-2022)</p><p>[ビデオ](https://youtu.be/7B332XH_zfs)</p><p>[MPOS を Store Commerce に移行する](dev-itpro/pos-extension/migrate-mpos-store-commerce.md)</p> |
| クラウド配置 | Commerce Scale Unit の複数のインスタンスは、負荷配分と地理的な近接性で使用できるように配置できます。 | [クラウド配置](../fin-ops-core/dev-itpro/deployment/cloud-deployment-overview.md) | |
| オンプレミス配置 | ローカルのビジネス データ配置を使用すると、Commerce の顧客は Dynamics 365 環境の所有権と管理を向上することができます。 | [オンプレミス配置](../fin-ops-core/dev-itpro/deployment/deploy-retail-onprem.md) | |

## <a name="device-management"></a>デバイス管理

| 能力 | Description | ドキュメント | 追加コンテンツ |
|---|---|---|---|
| 複数のフォーム ファクター | Store Commerce アプリは、PC、タブレット、モバイル デバイスなどの複数のデバイス フォーム ファクターでサポートされています。 レスポンシブ ユーザー インターフェイス (UI) を使用すると、レイアウトのサイズを自動的に変更したり、画面サイズに調整することができます。 | [視覚化コンフィギュレーション](pos-screen-layouts.md) | |
| クロスプラットフォーム | Store Commerce アプリは、Web、Windows、iOS、および Android プラットフォームでサポートされています。 | [プラットフォーム](dev-itpro/hybridapp.md) | |
| ブランド | 画面デザイナーを使用すると、画面レイアウトをカスタマイズして業務要件を満たすことができます。 さらに、従業員の役割に基づいて、テーマ、レイアウト、色、画像を作成し、ユーザー間で共有してブランドの一貫性を保ち、使いやすくすることができます。 | [視覚化コンフィギュレーション](pos-screen-layouts.md) | [ビデオ](https://www.youtube.com/watch?v=ldqCw2wf5fY) |
| トポロジ | ネットワークの可用性に基づいて、店舗内の異なるトポロジがサポートされます。 | <p>[トポロジ](dev-itpro/retail-modern-pos-architecture.md)</p><p>[インフォグラフィック](dev-itpro/retail-in-store-topology.md)</p> | |
| マルチデバイス管理 | Commerce Headquarters で、複数のデバイスを店舗間で簡単に管理できます。 | [アクティブ化](set-up-activation-accounts-validate-devices-hq.md) | [技術解説](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/commerce-mass-deployment-with-sccm-system-center-configuration-manager-october-6-2022) |

## <a name="employee-management"></a>従業員の管理

| 能力 | Description | ドキュメント | 追加コンテンツ |
|---|---|---|---|
| サインイン | 店舗の各従業員は、専用のサインインを使用できます。 サインインのタイプには、ユーザー名、バーコード、磁気ストライプ リーダー (MSR)、生体認証、Azure Active Directory (Azure AD) があります。 | <p>[Azure AD](aad-pos-logon.md)</p><p>[拡張ログオン](extended-logon.md)</p> | |
| アクセス許可 | 従業員にはさまざまなレベルのアクセス許可 (注文を作成するためのアクセス許可、注文を編集するためのアクセス許可など) がサポートされます。 | [アクセス許可](tasks/create-pos-permission-groups.md) | |
| 時間と出勤管理 | 出勤は、タイム レコーダー機能を使用して管理できます。 Dynamics 365 Human Resources アプリを使用して出勤データを給与に処理できます。 | [時間管理](retail-time-attendance.md) | |
| 売上コミッション | 販売担当者が売上を追跡して、手数料やその他のインセンティブを計算することができます。 | [コミッション](pos-sales-groups-track-commissions.md) | |

## <a name="merchandising"></a>販売促進

| 能力 | Description | ドキュメント | 追加コンテンツ |
|---|---|---|---|
| 品揃え管理 | 販売促進マネージャーは、製品を分類して、特定のチャネルおよび特定の期間に販売できるようにできます。 | [品揃え](assortments.md) | |
| カタログ | 販売促進マネージャーは、カタログを管理して、カタログ特有の価格で提供する製品を識別できます。 | [カタログ](/dynamicsax-2012/appuser-itpro/about-retail-product-catalogs) | |
| 製品とカテゴリの管理 | 販売促進マネージャーは、Commerce headquarters で、バリアント、属性、測定単位などを含む製品を作成できます。 また、カテゴリ階層を定義して製品を整理することもできます。 | [品目](retail-hierarchies.md) | |
| バンドル | 販売促進マネージャーは、製品をグループ化して、バンドルまたはキットとして販売できます。 | [キット](/dynamicsax-2012/appuser-itpro/about-setting-up-retail-product-kits) | |
| 情報コード | 情報コードを使用して、品目の販売、品目の返品、または顧客の選択などの、POS でのさまざまなアクションをレジ担当者が行なう途中に、情報の入力を求めます。 | [情報コード](/dynamicsax-2012/appuser-itpro/about-info-codes-retail) | |
| リンク済品目 | リンク済品目を使用して、品目をトランザクションに追加するときに製品をアップセルします。 | [リンク済品目](/dynamicsax-2012/appuser-itpro/set-up-products-for-cross-selling-and-up-selling) | |
| 保証 | 保証期間の延長は、製品と一緒に販売できます。 | [保証](extended-warranty.md) | |
| ラベル印刷 | バッチ番号、シリアル番号、有効期限などの製品情報を含むラベルを生成することができます。 | [ラベル印刷](/dynamicsax-2012/appuser-itpro/create-and-print-labels-overview) | |

## <a name="assisted-selling"></a>支援販売

| 能力 | Description | ドキュメント | 追加コンテンツ |
|---|---|---|---|
| 製品の参照 | カテゴリ別製品を参照する。 | [製品階層](retail-hierarchies.md) | |
| 製品検索 | 製品を名前で検索し、ブランド、価格、材料などの製品属性を使用して検索を絞り込みます。 この機能は、Azure Cognitive Search が提供します。 | [クラウドを利用した検索](cloud-powered-search-overview.md) | |
| 製品の詳細ページ | 製品の豊富な詳細ページには、画像、説明、製品属性、おすすめ製品が含まれます。 おすすめ候補は、レコメンデーション サービスが提供します。 | | |
| 製品の比較 | 複数の製品を比較すると、顧客は製品を選択してトランザクションに追加しやすくなります。 | | |
| エンドレス アイル | 他の店舗の在庫を簡単に検索し、注文を作成します。 | [在庫検索](pos-inventory-lookup-operation.md) | [技術解説](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| レコメンデーション | レコメンデーション サービスを使用したアップセルおよびクロスセル製品 このサービスでは、特許を取得した技術を使用して、購入の傾向や、新着や類似品、ベストセラー商品などの特徴に基づいて、おすすめ品目を提案します。 これらのおすすめ候補は、製品の詳細ページ、**顧客の詳細** ページ、**トランザクション** ページで使用することができます。 | [おすすめ候補](product-recommendations.md) | [技術解説](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-recommendations-march-2-2021) |

## <a name="customer-relationship"></a>顧客リレーションシップ

| 能力 | Description | ドキュメント | 追加コンテンツ |
|---|---|---|---|
| 顧客管理 | 顧客のアカウントを作成、編集、管理します。 顧客アカウントは、リアルタイム処理を回避するために、非同期モードで管理できます。 | [管理](customer-mgmt-stores.md) | |
| 顧客の属性 | 顧客属性フレームワークを使用すると、業務要件に応じて他の顧客関連データを取得できます。 | [属性](dev-itpro/customer-attributes.md) | |
| 顧客の詳細ページ | 顧客の豊富な詳細ページでは、すべてのチャネル全体で行なわれている顧客のやりとりをオムニチャンネル ビューで表示することができます。 これらのやりとりには、購入、ウィッシュ リスト、ロイヤルティ ポイントが含まれます。 | | |
| クラウドを利用した顧客検索 | 顧客を名前、電話番号、メール アドレス、ロイヤルティ カード、住所などで検索します。 | [クラウドを利用した検索](pos-search-improvements.md#customer-search) | |
| ロイヤルティと報酬 | 顧客はロイヤルティ プログラムに登録し、チャネル全体でロイヤルティ ポイントを獲得し引き換えることができます。 | [ロイヤルティ](set-up-customer-loyalty-program.md) | |
| クライアンテリング | クライアント ブックを使用して主要顧客を管理し、顧客プロファイルに関する活動やメモを追跡します。 Dynamics 365 Customer Insights 統合を使用して、店舗の従業員に、各顧客の 2 番目に最適なアクションに関するヒントを与えます。 | [クライアンテリング](clienteling-overview.md#activities-and-notes) | |

## <a name="pricing-and-discounts"></a>価格決定と割引

| 能力 | Description | ドキュメント | 追加コンテンツ |
|---|---|---|---|
| 売買契約 | 価格決定マネージャーは、取引契約を使用して、特定の顧客の長期的な取引に応じて特別価格を定義できます。 | [価格](price-management.md)| [ビデオ](https://www.youtube.com/watch?v=r2VD8IxHesM) |
| 販売契約書 | 価格決定マネージャーは、販売契約書を使用して、企業間 (B2B) のコマース シナリオにおける契約ベースの価格を定義できます。 | [価格](price-management.md) | |
| 価格調整 | 価格設定マネージャーは、価格調節機能を使用して、長期にわたる自社製品の価格値下げの作成、追跡、管理することができます。 | [価格調整](price-adjustments-discounts.md) | |
| 割引 | 価格決定マネージャーは、さまざまなプロモーションを実行するために複数の割引タイプを設定できます。 割引には、シンプルな割引、数量割引、しきい値割引、組み合わせ割引、支払/入金ベースの割引、送料割引などを含みます。 | [割引](retail-discounts-overview.md) | |
| クーポン | 価格決定マネージャーは、クーポン コードやバーコードを設定し、それらを割引にリンクさせ、顧客に配布することができます。 販売担当者は、販売トランザクションにクーポンを追加したり、削除することができます。 | [クーポン](coupons.md) | |
| 価格グループ | 価格決定マネージャーは価格グループ機能を使用して、チャネル、カタログ、所属、またはロイヤルティ プログラムに基づいてコンテキスト価格を定義できます。 | [価格](price-management.md) | |
| 使用できるプロモーション | 販売担当者は、店舗内の製品、トランザクションに追加された製品など、利用できるプロモーションを簡単に参照できます。 | [価格関数](pos-pricing-functions.md) | |
| 価格の確認 | 販売担当者は、店舗にある製品の有効な販売価格をすばやく確認できます。 | [価格関数](pos-pricing-functions.md) | |
| 価格変更 | 必要なアクセス許可のある販売担当者は、システムで構成された価格または計算された価格を上書きできます。 | [価格関数](pos-pricing-functions.md) | |
| 手動割引 | 必要なアクセス許可のある販売担当者は、販売トランザクションか販売行に手動割引を適用できます。 | [価格関数](pos-pricing-functions.md) | |

## <a name="electronic-payments"></a>電子支払

| 能力 | Description | ドキュメント | 追加コンテンツ |
|---|---|---|---|
| 貸方と借方 | Store Commerce アプリは、Adyen Payment Gateway を使用した主要なクレジット カードやデビット カードでの支払、PayPal を使用した注文フルフィルメントをサポートします。 支払 SDK では、独立したソフトウェア仕入先 (ISV) の統合がサポートする外部ゲートウェイ接続が許可されています。 | <p>[Adyen](dev-itpro/adyen-connector.md?tabs=10-0-23)</p><p>[PayPal](paypal.md)</p><p>[支払利息](payment-methods.md)</p> | <p>[技術解説](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-omni-channel-payment-configuration-february-9-2021)</p><p>[技術解説](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-omni-channel-payment-overview-processing-february-4-2021)</p> |
| デジタル ウォレット サポート | Store Commerce アプリは、従来のクレジット カードやデビット カードとは違い、銀行 ID 番号 (BIN) の範囲を使用しないデジタル ウォレット支払方法を使用した支払をサポートします。 支払方法は、Adyen などデジタル ウォレットの支払にマップできます。 | [ウォレット](wallets.md) | |
| ギフト カード サポート | 銀行 ID 番号 Dynamics 365 ギフト カード、Stored Value Solutions (SVS)、および Givex ギフト カードの 3 つがあります。 ギフト カードは、注文の際に購入および引き換えができます。 | [ギフト カード](dev-itpro/gift-card.md) | [技術解説](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/d365-commerce-internal-gift-cards-november-16-2021) |
| 不正保護 | Dynamics 365 Fraud Protection を使用して、不正行為を妨げ、不正を通知しない可能性のある場所を特定することができます。 | [Fraud Protection](dev-itpro/dfp.md) | [ビデオ](https://www.youtube.com/watch?v=j_1nEiq3LfM) |

## <a name="taxes-and-charges"></a>税と費用

| 能力 | Description | ドキュメント | 追加コンテンツ |
|---|---|---|---|
| 税金 | Store Commerce は、消費税、付加価値税 (VAT)、商品及びサービス税 (GST)、単位あたりの費用、源泉徴収税など、さまざまな間接税のタイプをサポートします。 | [税金](/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json) | |
| 諸費用 | 費用は、行レベルやヘッダー レベル、自動請求として、チャンネル別などに構成できます。 | [諸掛](omni-auto-charges.md) | |

## <a name="order-processing-and-fulfillment"></a>注文の処理とフルフィルメント

| 能力 | Description | ドキュメント | 追加コンテンツ |
|---|---|---|---|
| 注文の作成 | 注文する際に、出荷か近くの店舗で受け取るかを選択できます。 店舗で受け取る場合は、時間帯が表示されます。 | [概要](customer-orders-overview.md) | |
| 注文の変更 | 注文は、変更、返品、キャンセルなどができます。 | <p>[キャンセル](customer-orders-overview.md#cancel-a-customer-order)</p><p>[返品](pos-returns.md)</p> | |
| 検索 | 注文固有の情報を使用して、注文を検索およびフィルター処理します。 | [検索](enhancedorderrecall.md) | |
| 注文属性 | 注文属性フレームワークを使用すると、業務要件に応じて他の注文関連情報を取得できます。 | [属性](dev-itpro/order-attributes.md) | |
| 直納 | 仕入先が顧客の住所に直納する場合、品目をマークできます。 直納は、直送と呼ばれることもあります。 | [直納](/dynamics365/supply-chain/sales-marketing/tasks/ship-orders-direct-deliveries) | |
| 見積書 | 店舗の従業員は顧客の見積を作成し、特別価格、手動割引、見積の有効期間を指定できます。 | [見積書](/dynamics365/supply-chain/sales-marketing/tasks/create-edit-sales-quotations) | |
| フルフィルメント | 店舗は、注文をピック、梱包、出荷することができます。 梱包明細は、出荷準備ができているパッケージに追加できます。 | [フルフィルメント](order-fulfillment-overview.md) | [技術解説](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-supporting-buy-online-pickup-in-store-curbside-with-dynamics-365-commerce-pos-february-3-2021) |
| 配分済み注文の管理 | Store Commerce アプリは、業務の性質、顧客のタイプ、注文元、注文の配送方法に基づいて業務戦略を構成できる、インテリジェント注文フルフィルメントの最適化をサポートしています。 | [DOM](dom.md) | |

## <a name="inventory-management"></a>在庫管理

| 能力 | Description | ドキュメント | 追加コンテンツ |
|---|---|---|---|
| 集中的購買 | 物流センターから複数の店舗や倉庫への利用可能な在庫の配分を合理化します。 | [集中的購買](tasks/set-up-rules-parameters-cross-docking-buyers-push.md) | [技術解説](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| クロスドッキング | 受信する発注書で、複数の店舗や倉庫への在庫配分を合理化します。 | [クロスドッキング](tasks/set-up-rules-parameters-cross-docking-buyers-push.md) | [技術解説](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| 入庫在庫 | 発注書を使用して仕入先から在庫を入庫するか、移動オーダーを使用して別の倉庫から在庫を入庫します。 発注書または移動オーダーの要求を作成します。 | [着信](pos-inbound-inventory-operation.md) | [技術解説](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| 出庫在庫 | 移動オーダーを使用して別の倉庫に在庫を出荷し、出庫移動オーダーの要求を作成します。 | [発信](pos-outbound-inventory-operation.md) | [技術解説](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| 在庫検索 | 店舗や倉庫全体にわたる製品の手持在庫と、将来の日付の納期回答可能在庫 (ATP) 在庫を確認します。 | [在庫検索](pos-inventory-lookup-operation.md) | [技術解説](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| 在庫調整 | 店舗倉庫に入庫/出庫される在庫を調整して、販売、受取、再カウントを使用せずに特定の業務要件を満たすことができます。 | [在庫調整](work-with-store-inventory.md) | [技術解説](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| 在庫数 | 物理在庫をカウントし、システムの簿記在庫を調節して一致させます。 | [棚卸](work-with-store-inventory.md) | [技術解説](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| 在庫移動 | 店舗内で在庫を移動します。 | [振替](work-with-store-inventory.md) | [技術解説](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |

## <a name="financials"></a>財務

| 能力 | Description | ドキュメント | 追加コンテンツ |
|---|---|---|---|
| 現金管理 | Store Commerce アプリは、店舗内の現金や特定の輸送業者の管理をサポートします。 また、店舗でのシフト調整は、高度な現金管理機能に対して有効にすることができます。 | [現金](cash-mgmt.md) | |
| 財務諸表と調整 | 店舗の現金や取引トランザクションは、明細書転記プロセスで Commerce headquarters に記録されます。 | [明細書](retail-statements.md) | |
| 収入と経費トランザクション | 店舗で小口現金トランザクションを処理し、失くしたり見つけたりした現金、ロビーにある喫茶店からの収益配分、カーペット クリーニング サービスなど、従来の方法では処理されない収入を記録します。 | [明細書](retail-statements.md) | |
| 請求書支払 | 請求書に対する支払をキャプチャする。 | [請求書](payinvoice.md) | |

## <a name="employee-productivity"></a>従業員の生産性

| 能力 | Description | ドキュメント | 追加コンテンツ |
|---|---|---|---|
| タスク管理 | タスク一覧とタスクを作成し、店舗と従業員に割り当てます。 店舗間でのタスクの状態を追跡します。 Microsoft Teams を使用してシームレスに統合できます。 | <p>[タスク管理](task-mgmt-overview.md)</p><p>[Microsoft Teams](commerce-teams-integration.md)</p> | [ビデオ](https://www.youtube.com/watch?v=ES1whB4C2lU) |

## <a name="hardware-and-peripherals"></a>ハードウェアおよび周辺機器

| 能力 | Description | ドキュメント | 追加コンテンツ |
|---|---|---|---|
| 周辺機器の接続 | プリンター、キャッシュ ドロワー、スキャナー、支払デバイスなどの周辺機器に POS 端末を接続します。 | [周辺機器](retail-peripherals-overview.md) ||
| 周辺機器の共有 | レシート プリンター、キャッシュ ドロワー、支払デバイスは、1 つの共有ハードウェア ステーションに接続して、多数の端末間で共有できます。 | <p>[ハードウェア ステーション](retail-peripherals-overview.md) ||
| POS と周辺機器シミュレーター | 周辺機器シミュレーターは、通常は物理的に POS 周辺機器が必要なシナリオのテストをサポートします。 また、POS シミュレーターでは、POS クライアントの配置を要求しなくても、物理的な周辺機器との互換性をテストするために使用されます。 | [シミュレーター](dev-itpro/retail-peripheral-simulator.md) | |

## <a name="receipts"></a>受領書

| 能力 | Description | ドキュメント | 追加コンテンツ |
|---|---|---|---|
| レシートの印刷 | 既定では、会計時にレジ担当者が確認した後に、販売レシート、クレジット カードレシート、ギフトレシート、請求書など、さまざまなタイプのレシートを印刷することができます。 仕訳帳から再印刷することもできます。 | [印刷](receipt-templates-printing.md) | |
| 電子メールの領収書 | 会計が完了した後に、POS からメールでレシートを送信できます。 | [メール](email-receipts.md) | |
| レシートのデザイン | 店舗のレシートは、小売業者とトランザクション タイプに適したデータやレイアウトを表示できるようカスタマイズできます。 レシートは、拡張して、小売業者が要求するカスタム データを表示することもできます。 | [デザイン](receipt-templates-printing.md) | |

## <a name="offline-support"></a>オフライン サポート

| 能力 | Description | ドキュメント | 追加コンテンツ |
|---|---|---|---|
| シームレス オフライン | シームレス オフラインを使用すると、インターネットへの接続が制限されている場合や利用できない場合でも処理を続行できます。 データを除外することで、オフライン データベースのデータ サイズを減らしパフォーマンスを最大限に高くすることができます。 | [オフライン](pos-operations.md) | |
| パフォーマンス ベースの切り替え | パフォーマンスの低下が検出された場合は、オフラインに切り替えます。 | [オフライン](dev-itpro/implementation-considerations-offline.md) | [ビデオ](https://youtu.be/sQU-2pgHToI) |
| オフライン ダッシュボード | **オフライン状態** のダッシュボードにオフライン状態が表示され、各デバイスのオフライン状態、エラー、データの詳細が表示されます。 そのため、多くのデバイスの状態を簡単に管理できます。 | [オフライン](dev-itpro/implementation-considerations-offline.md) | [ビデオ](https://youtu.be/sQU-2pgHToI)|

## <a name="extensibility"></a>拡張性

| 能力 | Description | ドキュメント | 追加コンテンツ |
|---|---|---|---|
| Commerce headquarters | Commerce headquarters ソリューションは、業務プロセスを追加や変更することでカスタマイズできます。 Commerce headquarters では、メタデータとコード駆動型拡張モデルを使用してカスタム機能を追加できます。 簡単に外部ソリューションに統合できます。 | [概要](dev-itpro/extend-customer-cdx-package.md) | [技術解説](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-unlock-the-power-of-dynamics-365-commerce-commerce-extensibility-overview-february-23-2021) |
| ヘッドレス コマース | 拡張できるオムニコマース API フレームワークは、ビジネス ロジックをカスタマイズおよび追加する場合に使用できます。 要求ハンドラーを含む API、トリガー前とトリガー後の拡張パターン。 | [CSU](dev-itpro/retail-server-customer-consumer-api.md) | [技術解説](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |
| Commerce SDK | Commerce SDK には、Dynamics 365 Commerce 機能を拡張やカスタマイズするために必要な、コード、コード サンプル、テンプレート、およびツールが含まれています。 SDK は、拡張コンポーネントに応じて、GitHub の異なるレポジトリ (Repos) で公開されます。 | [SDK](dev-itpro/retail-sdk/sdk-github.md) | [技術解説](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |
| 販売時点管理 | Commerce SDK の POS 拡張機能を使用して、Store Commerce を個別に拡張することができます。 フレームワークは、ユーザー エクスペリエンス (UX)、ワークフロー、ビジネス ロジックのカスタマイズをサポートします。 | [POS](dev-itpro/pos-extension/pos-extension-overview.md) | [技術解説](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |

## <a name="reporting"></a>レポート

| 能力 | Description | ドキュメント | 追加コンテンツ |
|---|---|---|---|
| 売上レポート | 店舗マネージャーは、スタッフが報告する売上、登録、支払タイプ、返品、製品などを使用できます。 マネージャーにレポートが表示され、コミッションの割り当てや製品トレンドの識別に使用できます。 | | |

## <a name="diagnostics"></a>診断

| 能力 | Description | ドキュメント | 追加コンテンツ |
|---|---|---|---|
| Operational Insights | 店舗が管理するサービス正常性への信頼性とパフォーマンスに関するメトリックは、顧客の Application Insights サブスクリプションで使用できます。 高度な警告機能や監視機能を利用できます。 | | |
| 正常性チェック | POS に接続されている周辺機器の使用可能状態は、正常性チェック操作を実行することで検証できます。 その後、個々の周辺機器の問題を解決して検証できます。 | [正常性チェック](pos-healthcheck.md) | [ビデオ](https://www.youtube.com/watch?v=RfPDNmnqYvY) |

## <a name="globalization"></a>グローバリゼーション

| 能力 | Description | ドキュメント | 追加コンテンツ |
|---|---|---|---|
| マルチ市場サポート | 会計統合、GST、高度な請求、前払などの市場固有の機能は、そのままサポートされます。 この機能は、ヨーロッパ、米州、ロシア、アジア、サウジアラビアなどの市場をカバーします。 | [グローバリゼーション](localizations/fiscal-integration-for-retail-channel.md) | |

## <a name="compliance"></a>コンプライアンス

| 能力 | Description | ドキュメント | 追加コンテンツ |
|---|---|---|---|
| マイクロソフト標準 | Store Commerce アプリは、セキュリティ、プライバシー、アクセシビリティ、一般データ保護規則 (GDPR)、欧州連合 (EU) データの境界などのマイクロソフト標準を満たしています。 | | |

