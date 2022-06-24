---
title: Store Commerce または Cloud POS を選択する
description: この記事では、Store Commerce とクラウド POS の主な違いについて説明し、Dynamics 365 Commerce を実装する小売業者が要件を最適な方法で選択するために考慮すべきさまざまな要因について説明します。
author: jblucher
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-10-12
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 26f6e94b13b3058ac42c4c7b83dcf7179bae18e3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854009"
---
# <a name="choose-between-store-commerce-and-cloud-pos"></a>Store Commerce または Cloud POS を選択する

[!include [banner](includes/banner.md)]

この記事では、Store Commerce とクラウド POS の主な違いについて説明し、Dynamics 365 Commerce を実装する小売業者が要件を最適な方法で選択するために考慮すべきさまざまな要因について説明します。 このトピックでは、Dynamics 365 Commerce を配置する際に考慮すべき要因に対する追加のバックグラウンド、ヒント、およびガイダンスについても実装者に提供されます。 配置プロセスの一部としてこのガイドを確認し従うことにより、実装者は、ユーザーの満足度またはパフォーマンスに影響を与える可能性がある問題を回避することができます。

## <a name="insights"></a>インサイト

Commerce は、幅広い配置とトポロジ オプションを提供します。 したがって、小売業者は、ビジネスおよび技術要件に合わせてコンポーネントおよびコンフィギュレーションを選択できます。 慎重に検討すべき実装の 1 つの側面は、販売時点管理 (POS) コンポーネントのプラットフォームおよびフォーム ファクターの選択です。

### <a name="pos-platform-and-form-factor-considerations"></a>POS プラットフォームおよびフォーム ファクターに関する考慮事項

Commerce は、次の POS オプションをサポートします。

- Microsoft Windows の Store Commerce
- iOS および Android の Store Commerce
- Microsoft Edge および Google Chrome ブラウザーに対応しているクラウド POS (CPOS)
- Microsoft Windows の Modern POS (MPOS) (MPOSは 2023 年 10 月に非推奨になる予定です)。 

いずれにしても、POS (Store Commerce および CPOS) は同じコア アプリケーション コードを共有します。 この点が重要なのは、以下の理由によります。

- ユーザー インターフェイス (UI) は、プラットフォームまたはフォーム ファクターに関係なく一貫しています。
- ほとんどの機能能力は、プラットフォームまたはフォーム ファクターに関係なく同じです。 ただし、重要な違いがいくつかあります。 これらの違いは、この記事に記載されています。
- 各店舗では、POS バリエーションを組み合わせることができ、同時に実行できます。 たとえば、主要レジスターでは、小売業者は Windows を実行しているコンピューターで Store Commerce を使用できます。 ただし、小売業者は、ブラウザー ベースのターミナルまたはモバイル デバイスを持つレジスターを補うことができます。
- カスタマイズおよび拡張機能は、プラットフォームやフォーム ファクター間で容易に使用できます。 コア アプリケーション コードが共有されているため、ほとんどのカスタマイズが複数回ではなく 1 回で実装することができます。

### <a name="store-commerce-vs-cpos"></a>Store Commerce 対 CPOS

Store Commerce および CPOS は大部分は同じですが、理解しておくべき重要な違いがあります。

#### <a name="store-commerce"></a>Store Commerce

Store Commerce は、デバイスにインストールしてサービスを提供するデスクトップ アプリケーションです。

- **Windows** – Windows の Store Commerce アプリケーションには、すべてのアプリケーション コード、Commerce Runtime (CRT)、および ハードウェア ステーション (HWS) が含まれています。
- **iOS/Android** – これらのプラットフォームでは、アプリケーションが CPOS アプリケーション コードのホストとして機能します。 つまり、アプリケーション コードは Commerce Scale Unit でホストされている CPOS サーバーから取得されます。 詳細については、[Commerce Scale Unit の概要](dev-itpro/retail-store-system-begin.md) を参照してください。

#### <a name="cpos"></a>CPOS

ブラウザーでの CPOS 実行により、アプリケーションはデバイスにインストールされていません。 代わりに、ブラウザーは CPOS サーバーからアプリケーション コードにアクセスします。 したがって、CPOS は POS ハードウェアに直接アクセスできませんし、またはオフライン状態での作業もできません。

### <a name="store-deployment-considerations"></a>店舗の配置に関する考慮事項

プラットフォームおよびフォーム ファクターに加えて、小売業者は、店舗での配置オプションを選択する必要もあります。 次の表に、各 POS オプションで使用可能なコンフィギュレーションを示します。

| POS アプリケーション            | Commerce Scale Unit | オフラインで使用可 | ローカル HWS サポート |
|----------------------------|---------------------|-------------------|-------------------|
| Windows の Store Commerce | クラウドまたは RSSU       | 有効               | 有効               |
| Android の Store Commerce | クラウドまたは RSSU       | 無効                | 有効               |
| iOS の Store Commerce     | クラウドまたは RSSU       | 無効                | 無効                |
| クラウド POS                  | クラウドまたは RSSU       | 無効                | 無効                |

#### <a name="commerce-scale-unit"></a>Commerce Scale Unit

Commerce Scale Unit は、CRT をホストするコンポーネントです。 CRT は、POS が使用するすべてのビジネス ロジックを含み、チャネル データベースへのアクセスを提供します。 オンライン中、店舗内のすべての POS クライアントは Commerce Scale Unit を使用します。 クラウドまたは店舗内のいずれかで、Commerce Scale Unit を展開することができます。

#### <a name="offline-mode"></a>オフライン モード

Windows の Store Commerce はオフライン モードでサポートされています。 オフライン モードでは、Commerce Scale Unit から非接続の状態でも、POS は処理中の販売を続行できます。 接続が復旧すると、チャネル データベースで同期できます。 Store Commerce は、独自の CRT の埋め込み型インスタンスを使用し、一時的に独自のローカル データ ソース (オフライン SQL Server データベース) を使用します。 オフライン機能の詳細については、「[POS オフライン機能](pos-offline-functionality.md)」を参照してください。

### <a name="pos-peripheralhardware-considerations"></a>POS 周辺機器/ハードウェアの考慮事項

小売業者は、POS がプリンター、キャッシュ ドロワー、および支払ターミナルなどのデバイスや周辺機器にどのようにアクセスするかを検討する必要もあります。 ハードウェア ステーションは POS レジスター専用で、または店舗のレジスター間で共有できます。

| POS アプリケーション            | ローカル HWS OPOS | ネットワーク周辺機器 | 共有済み HWS サポート |
|----------------------------|----------------|---------------------|--------------------|
| Windows の Store Commerce | 有効            | 有効                 | 有効                |
| Android の Store Commerce | 無効             | 有効                 | 有効                |
| iOS の Store Commerce     | 無効             | 無効                  | 有効                |
| クラウド POS                  | 無効             | 無効                  | 有効                |

ハードウェア ステーションの詳細については、[Retail ハードウェア ステーションのコンフィギュレーションとインストール](retail-hardware-station-configuration-installation.md) を参照してください。

## <a name="implementation-considerations"></a>実装の考慮事項

店舗で POS 実装を計画する際、以下の情報を考慮してください。

- **機能の要件** – プラットフォーム、フォーム ファクターまたは配置トポロジに関係なく、コア業務プロセスおよび機能は同じです。 したがって、ほとんどの小売業者は、実装を計画する場合に機能の要件を考慮する必要はありません。
- **接続** ー ネットワーク機能 (ワイド エリア ネットワーク \[WAN\] およびローカル エリア ネットワーク \[LAN\]) は、慎重な検討を必要とする主要ファクターです。 ビジネスに重要なプロセスでシステムが使用できない場合、原価および簡略化に関するゼロ フットプリント、クラウド ホスト環境ソリューションがもたらす任意の利益は失われます。

    特定のデバイスの接続の信頼性および弾力性が非常に高くない限り、または一定のダウンタイムの量が小売業者に許容可能でない限り、次のオプションのいずれかをお勧めします。

    - Windows で Store Commerce を使用し、オフライン モードを有効にします。
    - オンプレミスの Commerce Scale Unit を配置します。

    これら 2 つのオプションは、相互に排他的ではありません。 最も信頼できるトポロジでは、小売業者はインターネット接続または Azure の可用性での依存関係を減らすためにローカル RSSU を配置でき、ローカル サーバーまたはネットワークに問題がある場合、オフライン モードが有効になっている POS レジスターを展開することもできます。

- **ハードウェア デバイス/周辺機器** – Retail POS システムの 1 つの重要な側面は、プリンター、キャッシュ ドロワー、および支払ターミナルなどの POS 周辺機器を使用する能力です。 使用可能なすべての POS オプションは周辺機器を使用できますが、Windows の Store Commerce のみがそれらを直接サポートします。 その他のすべてのアプリケーションには、1 つまたは複数のハードウェア ステーションが必要です。 この方法により柔軟性が増しますが、追加コンポーネントは配置、コンフィギュレーション、およびサービスの対象となる必要があります。
- **システム要件** – POS アプリケーションのシステム要件が異なります。 選択を行う前に、最新の情報を確認してください。 たとえば、ブラウザーで CPOS が実行されるため、より広範囲のオペレーティング システムをサポートします。 システム要件に関する詳細については、「[クラウド配置のシステム要件](../fin-ops-core/fin-ops/get-started/system-requirements.md)」を参照してください。
- **配置およびサービス** – アプリケーションおよび配置の選択に応じて、配置とサービス要件の複雑度が異なります。 たとえば、クラウド ホスト環境の CPOS 展開では、すべてのデバイスにインストールおよび更新は必要ありません。 したがって、この方法は、複雑度および原価を大幅に減少します。 ただし、オフライン モードを有効にしてすべてのレジスターに Store Commerce を配置し、共有ハードウェア ステーションも配置すると、管理する必要があるエンドポイントの数が大幅に増加します。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
