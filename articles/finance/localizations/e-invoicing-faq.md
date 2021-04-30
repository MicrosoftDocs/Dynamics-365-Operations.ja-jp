---
title: 電子請求に関する FAQ
description: このトピックでは、電子請求についてのよくある質問に関する情報を提供します。
author: gionoder
ms.date: 03/17/2021
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
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 1ba1a6c5542c10306d4b7494d33e7ff04504fa95
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893781"
---
# <a name="electronic-invoicing-faq"></a>電子請求に関する FAQ

[!include [banner](../includes/banner.md)]

このトピックでは、電子請求についてのよくある質問への回答を提供します。 電子請求は、Dynamics 365 Finance、Dynamics 365 Supply Chain Management、および Dynamics 365 Project Operations に存在する電子請求機能を拡張したものです。 

## <a name="what-is-important-about-electronic-invoicing-and-why-should-it-matter-to-my-organization"></a>電子請求についての重要事項と、それが組織にとって重要な理由を教えてください。

企業がグローバルに成長し、リージョン全体で占有領域を拡大するにつれ、オペレーションの複雑性とリスクはますます高まっています。 コンプライアンスを維持し、頻繁に変更される規制に適応することは、ますます増え続ける課題であり、請求に関しては特に重要です。 請求書の発行は、従来紙の書類や手作業に頼っていたため、コストやミスが発生しがちでした。  

組織は、コスト削減とエンド ツー エンド プロセスの迅速化のために、紙の請求書からの移行を始めています。 各国政府は、税のデジタル化の重要な要素として、電子請求の導入を進めています。 組織がリアルタイムで税務情報を税務当局に提出するよう義務付けることで、政府は脱税や改ざんを最小限に抑え、不正を減らすことができます。 

世界は文書処理のペーパーレス化を進めており、電子請求を導入しないと、顧客がコンプライアンス上の問題や不必要なコストを抱え、競合他社に遅れをとる可能性があります。 

## <a name="doesnt-finance-supply-chain-management-and-project-operations-already-include-electronic-invoicing-functionality-what-value-does-this-provide-to-me-as-a-customer"></a>Finance および Supply Chain Management、および Project Operations には電子請求機能がすでにありませんでしたか? これは、顧客である私にどうのような価値を提供しますか? 

電子請求は、Finance、Supply Chain Management、および Project Operations  に存在する電子請求機能を拡張したものです。 また、この機能により、最新の電子請求規格へ準拠しやすくなり、電子請求書の処理や交換において、異なる地域で一貫した体験を提供することができます。 電子請求により、以下のような様々なメリットが得られます。 

   - 国/リージョン固有の要件に、より早く、より簡単に対応することができる。
   - 電子請求ソリューション導入の標準化。 
   - 強化された電子請求書処理の追跡性。  
   - 変化する法的要件や現地の商習慣に対応するためのメンテナンスが簡単。 
   - 簡略化されたソリューションのパッケージ。
   - 大量に提出されたドキュメントに対応するスケーリング能力で、より早いターンアラウンドを実現。
   - ソリューションを他の会社と共有する機能。

## <a name="does-electronic-invoicing-support-the-on-premises-installations-of-finance-supply-chain-management-and-project-operations"></a>電子請求は、Finance および Supply Chain Management、および Project Operations のオンプレミス インストールをサポートしていますか? 

現在のプラットフォームでは、オンプレミス バージョンを使用できず、将来的にもサポートする予定はありません。

## <a name="does-electronic-invoicing-interface-with-the-vendor-import-automation-feature"></a>電子請求は、ベンダー インポート オートメーション機能とインターフェイスを取っていますか?

いいえ。 このインターフェイスについては予定がありますが、計画されたタイムラインはありません。 予定されたら、[リリース計画](/dynamics365/release-plans/)で日付が発表されます。

## <a name="how-does-electronic-invoicing-handle-file-attachments-into-the-electronic-invoice-is-a-sharepoint-server-needed-when-embedding-pdf-files-into-the-xml-file"></a>電子請求では、電子請求書へのファイル添付をどのように処理しますか? PDF ファイルを XML ファイル埋め込む際に、SharePoint サーバーは必要ですか?

電子請求書へ添付されたファイルは、XML 要素に埋め込まれたバイナリ データとして処理されます。 PDF ファイルの埋め込みに SharePoint サーバーは必要ありませんが、添付ファイルは Finance、Supply Chain Management、および Project Operations のドキュメント管理システムに保存する必要があります。

## <a name="is-electronic-invoicing-available-according-to-the-regulations-of-my-countryregion"></a>電子請求は、私の国/リージョンの規制に従って利用できますか?

電子請求は、グローバルに利用可能なマイクロサービス プラットフォームです。

Microsoft では、Microsoft によって機能的にローカライズされている国の電子請求書フォーマットや統合機能を公開する予定です。 詳細については、[電子請求機能の利用可能性](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features)を参照してください。

ご自身の国/リージョンの電子請求書フォーマットがリストにない場合、プラットフォームは将来的にこのシナリオをサポートすることを目指しています。 それでも、電子請求が持つ設定機能を利用して、自分で電子請求のフォーマットを設定することもできますし、パートナー/ISV と協力して組織向けに設定することもできます。

## <a name="is-dynamics-365-for-regulatory-services-a-new-module-like-human-resources-or-project-operations-that-is-linked-to-finance-or-supply-chain-management-are-there-extra-costs-for-that"></a>Dynamics 365 for Regulatory Servicesは、Human Resources や Project Operations のように、Finance や Supply Chain Management と連携した新しいモジュールですか? 追加料金はかかりますか?

Dynamics 365 for Regulatory Services (RCS) は、グローバリゼーションのリソースを設定するためのクラウド サービスです。 Finance、Supply Chain Management および Project Operations ライセンスをお持ちの場合は、RCS が無料となります。

RCS に新規登録する場合は、<https://marketing.configure.global.dynamics.com/>にアクセスしてください。

詳細については、[Regulatory Configuration Services (RCS) - グローバリゼーション機能](rcs-globalization-feature.md)を参照してください。

## <a name="do-i-need-to-sign-up-to-get-electronic-invoicing--or-just-turn-it-on-in-feature-management"></a>電子請求を利用するには登録が必要ですか、それとも機能管理でオンにするだけですか？

Finance、Supply Chain Management、および Project Operations のライセンスをお持ちの場合は、[電子請求アドオン サービス管理を開始する](e-invoicing-get-started-service-administration.md)を参照して、電子請求に登録します。

## <a name="does-electronic-invoicing-work-with-tier-1-virtual-machines-what-is-the-minimal-required-environment"></a>電子請求は、第 1 層仮想マシンで機能しますか? 最小環境要件を教えてください。

電子請求を統合するには、少なくとも Finance または Supply Chain Management をホストする第 2 層仮想マシンが必要です。 環境計画に関する詳細については、[環境計画](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)を参照してください。

## <a name="does-electronic-invoicing-have-a-test-mode-for-testing-invoice-submission"></a>電子請求には、請求書の送信をテストするためのテスト モードがありますか?

これは、設定で実行できます。 請求書の提出をテストするには、ユーザー受け入れテスト (UAT) 環境から Finance または Supply Chain Management に接続し、テスト請求書を提出します。 電子請求では、テスト用電子証明書の設定や、電子承認が必要な電子請求書の場合には、税務当局が公開しているテスト用 Web サービスの URL の設定をサポートしています。

## <a name="is-there-any-documentation-about-the-out-of-box-country-specific-electronic-invoicing-features"></a>国別電子請求機能に関してすぐに使えるドキュメントはありますか?

はい。 電子請求機能の有無や対応フォーマットについては、[電子請求機能の利用可能性](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features)を参照してください。

> [!NOTE] 
> 求めている回答が得られない場合、製品開発チーム(<D365EInvoicePreview@microsoft.com>) までメールでお問い合わせください。 折り返し連絡を差し上げるか、または FAQ の取り扱い範囲を改善します。