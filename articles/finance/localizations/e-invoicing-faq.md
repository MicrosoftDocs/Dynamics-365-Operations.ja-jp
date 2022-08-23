---
title: 電子請求に関する FAQ
description: この記事では、電子請求についてのよくある質問に関する情報を提供します。
author: gionoder
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.17
ms.custom: 97423
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: cf712c188e27deef4edfce7f5473fec4bb759bdf
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285820"
---
# <a name="electronic-invoicing-faq"></a>電子請求に関するよく寄せられる質問

[!include [banner](../includes/banner.md)]

この記事では、電子請求サービスについてよく寄せられる質問への回答を提供します。 電子請求は、Dynamics 365 Finance、Dynamics 365 Supply Chain Management および Dynamics 365 Project Operations に存在する電子請求機能を拡張したものです。 

## <a name="what-is-important-about-electronic-invoicing-and-why-should-it-matter-to-my-organization"></a>電子請求についての重要事項と、それが組織にとって重要な理由を教えてください。

企業がグローバルに成長し、リージョン全体で占有領域を拡大するにつれ、オペレーションの複雑性とリスクはますます高まっています。 コンプライアンスを維持し、頻繁に変更される規制に適応することは、ますます増え続ける課題であり、請求に関しては特に重要です。 請求書の発行は、従来紙の書類や手作業に頼っていたため、コストやミスが発生しがちでした。  

組織は、コスト削減とエンド ツー エンド プロセスの迅速化のために、紙の請求書からの移行を始めています。 各国政府は、税のデジタル化の重要な要素として、電子請求の導入を進めています。 組織がリアルタイムで税務情報を税務当局に提出するよう義務付けることで、政府は脱税や改ざんを最小限に抑え、不正を減らすことができます。 

世界は文書処理のペーパーレス化を進めており、電子請求を導入しないと、顧客がコンプライアンス上の問題や不必要なコストを抱え、競合他社に遅れをとる可能性があります。 

## <a name="doesnt-finance-supply-chain-management-and-project-operations-already-include-electronic-invoicing-functionality-what-value-does-this-provide-to-me-as-a-customer"></a>Finance および Supply Chain Management、および Project Operations には電子請求機能がすでにありませんでしたか? これは、顧客である私にどうのような価値を提供しますか? 

電子請求は、Finance、Supply Chain Management、および Project Operations に存在する電子請求機能を拡張したものです。 また、この機能により、最新の電子請求規格へ準拠しやすくなり、電子請求書の処理や交換において、異なる地域で一貫した体験を提供することができます。 電子請求により、以下のような様々なメリットが得られます。 

   - 国/リージョン固有の要件に、より早く、より簡単に対応することができる。
   - 電子請求ソリューション導入の標準化。 
   - 強化された電子請求書処理の追跡性。  
   - 変化する法的要件や現地の商習慣に対応するためのメンテナンスが簡単。 
   - 簡略化されたソリューションのパッケージ。
   - 大量に提出されたドキュメントに対応するスケーリング能力で、より早いターンアラウンドを実現。
   - ソリューションを他の会社と共有する機能。

## <a name="does-electronic-invoicing-service-support-the-on-premises-installations-of-finance-supply-chain-management-and-project-operations"></a>電子請求サービスは、Finance、Supply Chain Management、および Project Operations のオンプレミス インストールをサポートしていますか? 

現在のプラットフォームでは、オンプレミス バージョンを使用できず、将来的にもサポートする予定はありません。

## <a name="does-electronic-invoicing-service-interface-with-the-vendor-import-automation-feature"></a>電子請求サービスは、仕入先インポート自動化機能とインターフェイスを取っていますか?

いいえ。 このインターフェイスについては予定がありますが、計画されたタイムラインはありません。 予定されたら、[リリース計画](/dynamics365/release-plans/)で日付が発表されます。

## <a name="how-does-electronic-invoicing-service-handle-file-attachments-into-the-electronic-invoice-is-a-sharepoint-server-needed-when-embedding-pdf-files-into-the-xml-file"></a>電子請求サービスでは、電子請求書へのファイル添付をどのように処理しますか? PDF ファイルを XML ファイル埋め込む際に、SharePoint サーバーは必要ですか?

電子請求書へ添付されたファイルは、XML 要素に埋め込まれたバイナリ データとして処理されます。 PDF ファイルの埋め込みに SharePoint サーバーは必要ありませんが、添付ファイルは Finance、Supply Chain Management、および Project Operations のドキュメント管理システムに保存する必要があります。

## <a name="is-electronic-invoicing-service-available-according-to-the-regulations-of-my-countryregion"></a>電子請求サービスは、私の国/リージョンの規制に従って利用できますか?

電子請求サービスは、グローバルに利用可能なマイクロサービス プラットフォームです。

Microsoft では、Microsoft によって機能的にローカライズされている国の電子請求書フォーマットや統合機能を公開する予定です。 詳細については、[電子請求機能の利用可能性](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features)を参照してください。

ご自身の国/リージョンの電子請求書フォーマットがリストにない場合、プラットフォームは将来的にこのシナリオをサポートすることを目指しています。 それでも、電子請求が持つ設定機能を利用して、自分で電子請求のフォーマットを設定することもできますし、パートナー/ISV と協力して組織向けに設定することもできます。

## <a name="is-dynamics-365-for-regulatory-services-a-new-module-like-human-resources-or-project-operations-that-is-linked-to-finance-or-supply-chain-management-are-there-extra-costs-for-that"></a>Dynamics 365 for Regulatory Servicesは、Human Resources や Project Operations のように、Finance や Supply Chain Management と連携した新しいモジュールですか? 追加料金はかかりますか?

Dynamics 365 for Regulatory Services (RCS) は、グローバリゼーションのリソースを設定するためのクラウド サービスです。 Finance、Supply Chain Management および Project Operations ライセンスをお持ちの場合は、RCS が無料となります。

RCS に新規登録する場合は、<https://marketing.configure.global.dynamics.com/>にアクセスしてください。

詳細については、[Regulatory Configuration Services (RCS) - グローバリゼーション機能](rcs-globalization-feature.md)を参照してください。

## <a name="do-i-need-to-sign-up-to-get-electronic-invoicing-service-or-just-turn-it-on-in-feature-management"></a>電子請求サービスを利用するには登録が必要ですか、それとも機能管理でオンにするだけですか？

Finance、Supply Chain Management、および Project Operations のライセンスをお持ちの場合は、[電子請求アドオン サービス管理を開始する](e-invoicing-get-started-service-administration.md)を参照して、電子請求に登録します。

## <a name="does-electronic-invoicing-service-work-with-tier-1-virtual-machines-what-is-the-minimal-required-environment"></a>電子請求サービスは、第 1 層仮想マシンで機能しますか? 最小環境要件を教えてください。

電子請求サービスとの統合には、少なくとも Finance または Supply Chain Management をホストする第 2 層仮想マシンが必要です。 環境計画に関する詳細については、[環境計画](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)を参照してください。

## <a name="does-electronic-invoicing-service-have-a-test-mode-for-testing-invoice-submission"></a>電子請求サービスには、請求書の提出をテストするためのテスト モードがありますか?

これは、設定で実行できます。 請求書の提出をテストするには、ユーザー受け入れテスト (UAT) 環境から Finance または Supply Chain Management に接続し、テスト請求書を提出します。 電子請求では、テスト用電子証明書の設定や、電子承認が必要な電子請求書の場合には、税務当局が公開しているテスト用 Web サービスの URL の設定をサポートしています。

## <a name="is-there-any-documentation-about-the-out-of-box-country-specific-electronic-invoicing-features"></a>すぐに利用できる国別電子請求機能に関するドキュメントはありますか?

はい。 電子請求機能の可用性や対応フォーマットについては、[電子請求機能の可用性](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features) を参照してください。

## <a name="does-the-electronic-invoicing-service-allow-a-legal-entity-in-finance-or-supply-chain-management-that-is-configured-for-a-specific-country-to-consume-electronic-invoicing-features-from-different-countryregions"></a>電子請求サービスでは、特定の国に向けて構成された Finance または Supply Chain Management の法人が、異なる国/地域から電子請求機能を利用することはできますか?

はい。 次の条件に当てはまる場合、電子請求機能を使用して、法人の国に依存しないビジネス ドキュメントの提出を処理することができます。

   - 生成されるビジネス ドキュメントは、適切なドキュメント モデル マッピングを使用します。
   - 電子請求機能で設定されたビジネス ドキュメントと適合性ルールの間には一致があります。

## <a name="does-the-electronic-invoicing-service-use-the-same-configuration-and-design-experience-provided-by-the-electronic-reporting-module-in-finance-and-supply-chain-management"></a>電子請求サービスでは、Finance および Supply Chain Management の電子申告モジュールで提供されているのと同じ構成およびデザイン体験を使用していますか? 

はい。 Finance および Supply Chain Management の電子申告 (ER) モジュールで使用されるのと同じデザイナー ツールを使用して、データ モデル マッピングとファイル形式のコンフィギュレーションを作成および構成します。 これらのデザイナ ツールは、Regulatory Configuration Services (RCS) でも使用され、電子請求機能のコンフィギュレーションで使用されるデータ モデル マッピングおよびファイル形式コンフィギュレーションを作成および構成します。

## <a name="can-the-applicability-rules-be-extended-and-configured-so-that-they-arent-tied-to-any-specific-parameter-such-as-a-legal-entity"></a>適用ルールを拡張して、法人などの特定のパラメーターに関連付けられないように設定することはできますか?

はい。 適用ルールは完全に構成可能です。 句の追加と削除、ビルド ロジックの作成、句のグループ化とグループ解除を行えます。 詳細については、[適用ルール](e-invoicing-configuration-rcs.md?toc=/dynamics365/finance/toc.json#applicability-rules) を参照してください。

## <a name="does-the-electronic-invoicing-service-support-adding-other-er-format-configurations-to-generate-other-types-of-documents-does-it-support-sending-the-documents-electronically-to-customers-such-as-a-delivery-note"></a>電子請求サービスでは、他のタイプのドキュメントを生成するために、他の ER 形式コンフィギュレーションを追加することをサポートしていますか? 納品書などのドキュメントを顧客へ電子的に送信することサポートしていますか?

他の ER 形式コンフィギュレーションを使用して、必要な出力ファイルを生成できます。 ただし、ER 形式のコンフィギュレーションは、ビジネス ドキュメントを生成するために Finance または Supply Chain Management で構成したものと同じ ER 請求書モデル マッピングから派生する必要があります。 出力ファイルを EDI トランザクションとして顧客に直接送信することは、電子請求ではすぐにはサポートされていません。

## <a name="does-the-electronic-invoicing-service-support-exchanging-electronic-invoices-with-customers-does-it-support-configuring-different-invoice-formats-for-the-same-invoice"></a>電子請求サービスでは、顧客との電子請求書の交換をサポートしていますか? 同じ請求書に対する異なる請求書形式の構成をサポートしていますか?

仕入先の電子請求書を受信およびインポートする機能はロードマップ上にありますが、電子請求書を自動的に送信する機能は現在サポートされていません。

## <a name="does-the-electronic-invoicing-service-extend-to-support-exchanging-edi-messages-with-other-companies"></a>電子請求サービスは、他の会社との EDI メッセージの交換をサポートするように拡張されていますか?

電子請求サービスの焦点は、規制順守要件に基づいて電子請求書メッセージ タイプを交換することです。 仕入先の電子請求書の受信およびインポートはロードマップ上にありますが、顧客への電子請求書ファイルの送信は、規制上の要件である場合を除いて現在サポートされていません。

## <a name="does-the-electronic-invoicing-service-support-importing-or-merging-customizations-made-in-the-er-format-configurations-from-the-legacy-electronic-invoicing-feature"></a>電子請求サービスでは、従来の電子請求書発行機能から、ER 形式のコンフィギュレーションで行われたカスタマイズのインポートまたはマージをサポートしていますか?

電子請求サービスで、ER 形式のコンフィギュレーションを再利用できます。 ただし、ER 形式のコンフィギュレーションは、電子請求機能が使用するために設計され、ビジネス ドキュメントを生成するために Finance または Supply Chain Management で構成したものと同じ ER 請求書モデル マッピングから派生する必要があります。

## <a name="does-the-electronic-invoicing-service-support-issuing-electronic-invoices-from-custom-made-tables-if-so-how-do-you-create-the-er-data-model-configurations-for-these-new-tables-and-entities"></a>電子請求サービスでは、カスタム メイド テーブルからの電子請求書の発行をサポートしていますか? その場合、これらの新しいテーブルおよびエンティティの ER データ モデル コンフィギュレーションをどのように作成しますか?

はい。 ただし、請求書モデル マッピングをカスタマイズし、カスタム メイド テーブルに必要な参照を追加したり、複雑さによっては新しい請求書モデル マッピングを作成する必要があります。

## <a name="does-the-electronic-invoicing-service-support-different-web-service-endpoints"></a>電子請求サービスでは、異なる Web サービス エンドポイントをサポートしていますか?

電子請求サービスでは、異なる Web サービス エンドポイントをサポートしています。 コンフィギュレーション可能な REST Webサービスとの統合、または複数のパラメータ化された国固有の Web サービス統合を使用できます。 異なるバージョンのコンフィギュレーションを使用して、同じ Web サービスおよび API に対して異なるエンドポイントを構成できます。 詳細については、[アクション別パラメーター リスト](e-invoicing-setup.md#list-of-parameters-by-action) セクションを参照してください。

## <a name="is-electronic-invoicing-integrated-with-the-various-invoice-operators-apis-from-the-nordic-countries-or-should-that-be-handled-on-a-case-by-case-basis"></a>電子請求は、北欧諸国の様々な請求演算子の API と統合されていますか、それとも個別で処理される必要がありますか?

Microsoft は、電子請求機能を使用してすぐに統合できるよう、機能補充を継続的に拡張しています。 サポートされている形式と統合の詳細については、[電子請求機能の可用性](e-invoicing-configuration-rcs.md?toc=/dynamics365/finance/toc.json#availability-of-electronic-invoicing-features) を参照してください。

> [!NOTE] 
> 求めている回答が得られない場合、製品開発チーム(<D365EInvoicePreview@microsoft.com>) までメールでお問い合わせください。 折り返し連絡を差し上げるか、または FAQ の取り扱い範囲を改善します。
