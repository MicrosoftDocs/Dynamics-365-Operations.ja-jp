---
title: "Modern POS およびクラウド POS かの選択をします"
description: "このトピックでは、Retail Modern POS およびクラウド POS の主な違いについて説明します。 Microsoft Dynamics 365 for Retail を実装する小売業者が、要件に対して最適な選択ができるよう考慮すべきさまざまな要因についても説明します。"
author: jblucher
manager: AnnBe
ms.date: 10/12/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-10-12
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 7eb15f9f73f4773d98160e1b0ec5ce74c159cdea
ms.contentlocale: ja-jp
ms.lasthandoff: 02/07/2018

---

# <a name="choose-between-modern-pos-and-cloud-pos"></a>Modern POS およびクラウド POS かの選択をします

[!include[banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Retail を配置する際に考慮すべき要因に対する追加のバック グラウンド、ヒント、およびガイダンスを実装者に与えます。 配置プロセスの一部としてこのガイドを確認し従うことにより、実装者は、ユーザーの満足度またはパフォーマンスに影響を与える可能性がある問題を回避することができます。

## <a name="insights"></a>インサイト
Retail は、幅広い配置とトポロジ オプションを提供します。 したがって、小売業者は、ビジネスおよび技術要件に合わせてコンポーネントおよびコンフィギュレーションを選択できます。 慎重に検討すべき実装の 1 つの側面は、販売時点管理 (POS) コンポーネントのプラットフォームおよびフォーム ファクターの選択です。

### <a name="pos-platform-and-form-factor-considerations"></a>POS プラットフォームおよびフォーム ファクターに関する考慮事項
Retail は、次の POS オプションをサポートします。

- Microsoft Windows の Retail Modern POS (MPOS)
- Microsoft Windows Phone の MPOS
- Apple iPad または Google Android タブレットの MPOS
- Microsoft Edge、Internet Explorer、および Google Chrome ブラウザをサポートするクラウド POS (CPOS)

いずれにしても、POS (MPOS および CPOS) は同じコア アプリケーション コードを共有します。 この点が重要なのは、以下の理由によります。

- ユーザー インターフェイス (UI) は、プラットフォームまたはフォーム ファクターに関係なく一貫しています。
- ほとんどの機能能力は、プラットフォームまたはフォーム ファクターに関係なく同じです。 ただし、重要な違いがいくつかあります。 これらの違いは、このトピックに記載されています。
- 特定の店舗では、POS バリエーションを組み合わせることができ、同時に実行できます。 たとえば、主要レジスターでは、小売業者は Windows を実行しているコンピューターで MPOS を使用できます。 ただし、小売業者は、ブラウザー ベースのターミナルまたはモバイル デバイスを持つレジスターを補うことができます。
- カスタマイズおよび拡張機能は、プラットフォームやフォーム ファクター間で容易に使用できます。 コア アプリケーション コードが共有されているため、ほとんどのカスタマイズが複数回ではなく 1 回で実装することができます。

### <a name="mpos-vs-cpos"></a>MPOS 対 CPOS
MPOS および CPOS は大部分は同じですが、理解しておくべき重要な違いがあります。

#### <a name="mpos"></a>MPOS

Windows、iOS、または Android デバイスの MPOSは、デバイスでパッケージ化され、インストールされ、およびサービス対象となるアプリケーションです。

- **Windows** – Windows アプリケーションの MPOS には、すべてのアプリケーション コードおよび埋め込み型 Commerce Runtime (CRT) が含まれています。 
- **iOS/Android** – これらのプラットフォームでは、アプリケーションが CPOS アプリケーション コードのホストとして機能します。 つまり、アプリケーション ードは Microsoft Azure または Retail Store スケール ユニット (RSSU) の CPOS サーバーから取得されます。 詳細については、[小売店舗スケール ユニットの概要](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/dev-itpro/retail-store-system-begin)を参照してください。

#### <a name="cpos"></a>CPOS

ブラウザーでの CPOS 実行により、アプリケーションはデバイスにインストールされていません。 代わりに、ブラウザーは CPOS サーバーからアプリケーション コードにアクセスします。 したがって、CPOS は POS ハードウェアに直接アクセスできませんし、またはオフライン状態での作業もできません。

### <a name="store-deployment-considerations"></a>店舗の配置に関する考慮事項
プラットフォームおよびフォーム ファクターに加えて、小売業者は、店舗での配置オプションを選択する必要もあります。 次の表に、各 POS オプションで使用可能なコンフィギュレーションを示します。

| POS アプリケーション         | Retail サーバー | オフラインで使用可 |
|-------------------------|---------------|-------------------|
| Windows 用 MPOS        | クラウドまたは RSSU | 有               |
| iOS または Android 用 MPOS | クラウドまたは RSSU | 無                |
| クラウド POS               | クラウドまたは RSSU | 無                |

#### <a name="retail-server"></a>Retail サーバー

Retail サーバーは、CRTをホストするコンポーネントです。 CRT は、POS が使用するすべてのビジネス ロジックを含み、チャネル データベースへのアクセスを提供します。 オンライン中、店舗内のすべての POS クライアントは Retail サーバーを使用します。 クラウドまたは店舗 (RSSU) 内のいずれかで、Retail サーバーを展開することができます。

#### <a name="offline-mode"></a>オフライン モード

Windows 用 MPOS は、オフライン モードをサポートします。 オフライン モードでは、Retail サーバーから非接続の状態でも、POS は処理中の販売を続行できます。 接続が復旧すると、チャネル データベースで同期できます。 MPOS は、独自の CRT の埋め込み型インスタンスを使用し、一時的に独自のローカル データ ソース (オフライン SQL Server データベース) を使用します。 オフライン機能の詳細については、「[POS オフライン機能](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/pos-offline-functionality)」を参照してください。

### <a name="pos-peripheralhardware-considerations"></a>POS 周辺機器/ハードウェアの考慮事項
小売業者は、POS がプリンター、キャッシュ ドロワー、および支払ターミナルなどのデバイスや周辺機器にどのようにアクセスするかを検討する必要もあります。 Windows 用 MPOS のみ、これらのデバイスでの直接通信をサポートしています。 Windows Phone、iOS、または Android 用の MPOS、およびクラウド POS は、これらのデバイスにアクセスするためハードウェア ステーションを必要とします。 ハードウェア ステーションは POS レジスター専用で、または店舗のレジスター間で共有できます。 ハードウェア ステーションの詳細については、[Retail ハードウェア ステーションのコンフィギュレーションとインストール](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/retail-hardware-station-configuration-installation) を参照してください。

## <a name="implementation-considerations"></a>実装の考慮事項
小売店舗で POS 実装を計画する際、以下の情報を考慮してください。

- **機能の要件** – プラットフォーム、フォーム ファクターまたは配置トポロジに関係なく、コア業務プロセスおよび機能は同じです。 したがって、ほとんどの小売業者は、実装を計画する場合に機能の要件を考慮する必要はありません。
- **接続** - ネットワーク機能 (ワイド エリア ネットワーク \[WAN\] およびローカル エリア ネットワーク \[LAN\]) は、慎重な検討を必要とする主要ファクターです。 ビジネスに重要なプロセスでシステムが使用できない場合、原価および簡略化に関するゼロ フットプリント、クラウド ホスト環境ソリューションがもたらす任意の利益は失われます。

    特定のデバイスの接続の信頼性および弾力性が非常に高くない限り、または一定のダウンタイムの量が小売業者に許容可能でない限り、次のオプションのいずれかをお勧めします。

    - Windows で MPOS を使用し、オフライン モードを有効にします。
    - オンプレミス RSSU の配置。

    これら 2 つのオプションは、相互に排他的ではありません。 最も信頼できるトポロジでは、小売業者はインターネット接続または Azure の可用性での依存関係を減らすためにローカル RSSU を配置でき、ローカル サーバーまたはネットワークに問題がある場合、オフライン モードが有効になっている POS レジスターを展開することもできます。

- **ハードウェア デバイス/周辺機器** – Retail POS システムの 1 つの重要な側面は、プリンター、キャッシュ ドロワー、および支払ターミナルなどの POS 周辺機器を使用する能力です。 使用可能なすべての POS オプションは周辺機器を使用できますが、Windows 用 MPOS のみそれらを直接サポートします。 その他のすべてのアプリケーションには、1 つまたは複数のハードウェア ステーションが必要です。 この方法により柔軟性が増しますが、追加コンポーネントは配置、コンフィギュレーション、およびサービスの対象となる必要があります。
- **システム要件** – POS アプリケーションのシステム要件が異なります。 選択を行う前に、最新の情報を確認してください。 たとえば、ブラウザーで CPOS が実行されるため、より広範囲のオペレーティング システムをサポートします。 システム要件に関する詳細については、「[クラウド配置のシステム要件](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/system-requirements)」を参照してください。
- **配置およびサービス** – アプリケーションおよび配置の選択に応じて、配置とサービス要件の複雑度が異なります。 たとえば、クラウド ホスト環境の CPOS 展開では、すべてのデバイスにインストールおよび更新は必要ありません。 したがって、この方法は、複雑度および原価を大幅に減少します。 ただし、オフライン モードを有効にしてすべてのレジスターに MPOS を配置する場合、共有ハードウェア ステーションも配置し、管理する必要があるエンドポイントの数が大幅に増加します。

