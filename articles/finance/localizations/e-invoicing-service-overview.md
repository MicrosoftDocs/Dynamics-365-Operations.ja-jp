---
title: 電子請求書アドオン機能の概要
description: このトピックでは、Microsoft Dynamics 365 Finance および Dynamics 365 Supply Chain Management で電子請求のアドオンを設定する方法について説明します。
author: gionoder
manager: AnnBe
ms.date: 01/22/2021
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
ms.openlocfilehash: 2c35b810151349384f105d9ac1d93e1885031450
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104211"
---
# <a name="electronic-invoicing-add-on-overview"></a>電子請求書アドオン機能の概要

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Finance および、Dynamics 365 Supply Chain Management の電子請求書アドオンは、電子請求書ドキュメントの構成可能な処理と構成可能な訴求メント交換を可能にする高スケーラブルなマルチ テナントサービスです。 処理と統合のルールは完全に構成をすることが可能で、このロジックは財務と Supply Chain Management の外部で実行されます。 本サービスは、主に企業間の電子請求書の処理を対象としていますが、それ以外の用途にも独自の構成をすることが可能です。

電子請求のアドオンを使用すると、次のような目標の達成に役立ちます :

- 国/地域固有の要件を迅速かつ簡単に取り入れる
- 電子請求書のアドオン ソリューションの標準化された実装
- ドキュメント履歴の追跡機能の強化
- 短い実装サイクル
- 総保有コスト (TCO) を削減する
- コードの変更を必要としない構成を簡単に調整する
- 簡素化された構成のパッケージ化
- 組み込みのエクスポート、インポート、統合、および電子請求書ドキュメントの処理における容易な拡張性
- 複数の会社間で同一のエクスポート、インポート、統合の構成を簡単に再利用する

電子請求書のアドオンを使用するには、Microsoft Dynamics Lifecycle Services (LCS) のプロジェクトからインストールする必要があります。 次に、セットアップ手順に従って、財務または Supply Chain Management との統合を有効化します。 詳細情報については、[電子請求書アドオンの使用を開始する](e-invoicing-get-started.md)を参照してください。

## <a name="service-availability"></a><a name="availability"></a>サービスの可用性

現在、電子請求書アドオンはプレビュー プログラムご利用のお客様が利用いただけますが、次のフェーズでは一般のお客様にもご利用いただけるようになる予定です。 国/地域固有の要件に対応する機能は、リリースの段階によっては制限がされる場合があるため、サポートされている国/地域固有となるソリューションの範囲および、範囲を示す最新のドキュメントを常に確認する必要があります。

電子請求のアドオンは、次の Azure の地域で展開されます :

- 米国
- ヨーロッパ

> [!NOTE]
> 電子請求書のアドオンは、オンプレミスのデプロイに対応していません。

## <a name="extended-configurability"></a>拡張された設定可能性

電子請求のアドオンは、電子ドキュメントを作成して指定された当事者に送信する必要がある場合に使用できます。 受信したデータに基づいて、構成可能な処理の流れを実行する目的に特化しています。 財務および Supply Chain Management で使用できる構成のオプションは、ドキュメント変換に限定されます。 サービスは、その中で利用可能となる構成可能な統合を追加することで、これらのオプションを拡張します。 さらに、ブラジルの Nota fiscaleletrônica (NF-e) 、メキシコの Comprobante Fiscal por Internet (CFDI) 、または他の西ヨーロッパの Universal Business Language (UBL) /Pan-European Public Procurement OnLine (PEPPOL) 機能など、これまで利用可能であったすべての電子請求書機能は、エクスポートおよびインポート用の構成を使用して外部 Web サービスとの統合を可能にします。

## <a name="feature-highlights"></a>機能の特徴

- 財務および Supply Chain Management との既成の統合
- べての国や地域の電子請求書プロセスの設定と監視に使用する一貫したユーザー エクスペリエンス
- 新しい国や地域での電子請求書アドオン ソリューションの導入をより早く、より簡単に、より低コストで行う
- Regulatory Configuration Services (規制構成サービス) およびグローバリゼーション機能の設定を通したサービスの構成
- RCS で定義されている構成を使用してビジネス データを複数の電子請求書フォーマット (XML、JavaScript Object Notation \[JSON\]、テキスト、カンマ区切り値\[CSV\]) に変換する :

    - 電子請求書の変換設定が使用できない国や地域で利用可能な電子レポートの形式

- 外部 Web サービスへの電子請求書の送信を構成可能 (電子署名による認証処理を含む):

    - 複数の国に対する追加コンテンツとの、組み込みの簡単で拡張性のある、構成可能な統合

    > [!NOTE]
    > 現時点では、対応している直接送信は限られています。 詳細については、前述の [サービスの可用性](#availability) セクションを参照してください。 対応範囲はは今後拡張する予定です。

- 構成可能な例外メッセージ処理を含む、Web サービスからのレスポンスの処理
- 電子署名への対応 (XMLDSig 署名アルゴリズムの使用など)
- 電子請求メッセージの一括処理

## <a name="architecture-and-data-flow"></a>アーキテクチャとデータ フロー

LCS から電子請求書アドオンをインストールし、必要となるアプリケーションでの必要な設定が完了すると、安全な接続が確立されます。 このサービスは現在、米国およびヨーロッパのデータ センターに配置されています。 したがって、サービスの場所は、関連する財務または、Supply Chain Management インスタンスの場所とは異なる場合があります。 電子請求書アドオンの設定を完了し、統合をオンにすると、電子請求書が送信されるたびに特定のドキュメントに関連するマスター データとトランザクション データが電子請求書アドオンに送信されます。

> [!NOTE]
> 電子請求書やその他のドキュメントに個人データが含まれている場合は、この機能を使用する際に一般データ保護規則 (GDPR) や個人データの転送に関するその他規制に準拠していることを確認してください。

### <a name="high-level-description-of-the-data-flow"></a>データ フローの高レベルな概要

1. クライアントは、標準的なビジネス ドキュメントをサービスに送信します。
2. サービスは、クライアントから受信したコンテキスト情報に基づいて、該当する処理フローを選択します。
3. サービスが処理アクションを実行します。 これらのアクションには、ビジネス ドキュメントを電子請求書に変換したり、電子署名を適用したり、外部の Web サービスにドキュメントを送信したりすることが含まれます。
4. 受信したドキュメントや処理したドキュメントは、顧客の Azure Blob Storage に保存されています。
5. 処理に使用したテナントのシークレットと証明書はすべて、顧客の Azure Key Vault に保存されています。
6. このサービスは、送信されたビジネス ドキュメントの処理状況をクライアントにオンデマンドで提供します。
7. クライアントは、処理の完了情報を受信し、すべてのログ情報を利用可能にします。 また、フローの処理中に作成、受信されたドキュメントを使用できます。

次の図は、電子請求書アドオンのデータの流れを示しています。

![電子請求書アドオン設定のデータ フロー](media/e-invoicing-service-data-flow-diagram-overview.png)

## <a name="privacy-notice"></a>プライバシー通知
電子請求書のアドオンを有効化して使用するには、税務登録 ID を含む一部のデータの送信が必要となる場合があります。 これは、政府の web サービスとの統合に必要となる事前定義された形式で電子請求書を送信する目的で、税務当局によって認可された第三者機関に送信されます。 これらの外部システムから Dynamics 365 のオンライン サービスにインポートされたデータは、当社の [プライバシー ステートメント](https://go.microsoft.com/fwlink/?LinkId=512132) の対象となります。 詳細については、各国固有の機能説明書のプライバシーに関する注意事項を参照してください。

## <a name="additional-resources"></a>追加リソース
- [サービス管理](e-invoicing-service-administration.md)
- [RCS で電子請求書を構成する](e-invoicing-configuration-rcs.md)
- [Finance および Supply Chain Management で電子請求書を発行する](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]