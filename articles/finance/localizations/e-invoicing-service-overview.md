---
title: 電子請求の概要
description: この記事では、Microsoft Microsoft Dynamics 365 Finance および Dynamics 365 Supply Chain Management における電子請求の概要を示します。
author: gionoder
ms.date: 01/21/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 9d73b2dd7bf83c169aa776b41f962cc6addf5f19
ms.sourcegitcommit: a5a4c45bb265758c6e5c3483c8552503b1799a89
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524719"
---
# <a name="electronic-invoicing-overview"></a>電子請求の概要

[!include [banner](../includes/banner.md)]

Microsoft Microsoft Dynamics 365 Finance および Dynamics 365 Supply Chain Management の電子請求は、電子請求書の構成可能な処理と構成可能な電子ドキュメントの交換を可能にする高スケーラブルなマルチ テナントサービスです。 処理と統合のルールは完全に構成をすることが可能で、このロジックは財務と Supply Chain Management の外部で実行されます。 本サービスは、主に企業と政府間のシナリオにおける電子請求書ドキュメントの処理を対象としています。 ただし、さまざまなタイプのドキュメントに対する企業間シナリオなど、他の目的のためにカスタム構成することもできます。

電子請求を使用すると、次のような目標の達成に役立ちます :

- 国/地域固有の要件を迅速かつ簡単に取り入れる
- 電子請求ソリューションの標準化された実装
- ドキュメント履歴の追跡機能の強化
- 短い実装サイクル
- 総保有コスト (TCO) を削減する
- コードの変更を必要としない容易に調整可能な構成
- 簡素化された構成のパッケージ化
- 電子請求書ドキュメントの処理における組み込みのエクスポート、インポート、統合、容易な拡張性
- 複数の会社間で同一のエクスポート、インポート、統合の構成を簡単に再利用する

## <a name="service-availability"></a>サービスの可用性

現在、Finance および Supply Chain Management の顧客は、電子請求機能を使用できます。 詳細については、アプリケーションのライセンス条件を確認してください。

国/地域固有の要件に対応する機能は、リリースのさまざまな段階で制限される可能性があるため、サポートされている国/地域固有となるソリューションの範囲およびスコープを示す最新のドキュメントを常に確認する必要があります。

電子請求は、次の Azure の地域で展開されます :

- 米国
- ヨーロッパ
- イギリス
- アジア
- 日本
- スイス
- ブラジル
- アラブ首長国連邦
- オーストラリア
- カナダ
- フランス
- インド

> [!NOTE]
> 電子請求は、オンプレミスのデプロイに対応していません。

## <a name="feature-highlights"></a>機能の特徴

- Finance および Supply Chain Management との既成の統合
- すべての国と地域に対する電子請求書プロセスの構成と監視に使用する一貫したユーザー エクスペリエンス
- 新しい国や地域での電子請求ソリューションの導入をより早く、より簡単に、より低コストで行う
- Regulatory Configuration Service (RCS) およびグローバリゼーション機能の設定によるサービスの構成
- RCS で定義された構成を使用してビジネス データを複数の電子請求書フォーマット (XML、JavaScript Object Notation \[JSON\]、TXT、カンマ区切り値 \[CSV\]) に変換:

    - 電子請求書変換の構成が使用できない国や地域で利用可能な電子申告 (ER) 形式

- 外部 Web サービスへの電子請求書の構成可能な送信 (電子署名による認証処理を含む):

    - さまざまな国や地域の追加コンテンツとの組み込み型の、容易に拡張および構成可能な統合

- 例外メッセージの構成可能な処理を含む、Web サービスからの応答処理
- 電子署名への対応 (例えば、XMLDSig 署名アルゴリズムを使用する電子署名)
- メールにドキュメントを送信し、SharePoint に保存する機能
- 電子請求メッセージのバッチ処理
- Finance および Supply Chain Management での受信ドキュメントの構成可能な変換と処理
- メールや SharePoint などのチャネルから受信ドキュメントを受信する機能

## <a name="privacy-notice"></a>プライバシー通知

電子請求を有効にして使用するには、制限付きデータの送信が必要になる場合があります。 このデータは組織の税登録 ID を含みます。 このデータは、政府の web サービスとの統合に必要となる事前定義された形式で電子請求書を送信する目的で、税務当局によって認可された第三者機関に送信されます。 これらの外部システムから Dynamics 365 のオンライン サービスにインポートされたデータは、当社の [プライバシーに関する声明](https://go.microsoft.com/fwlink/?LinkId=512132) の対象となります。 詳細については、国/地域に固有の機能ドキュメントが含む "プライバシーに関する注意事項" セクションを参照してください。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
