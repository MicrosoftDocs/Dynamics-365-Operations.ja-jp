---
title: ワンボックス開発環境のセキュリティ保護
description: この記事では、ワンボックス開発環境をセキュリティで保護する方法について説明します。
author: mnordick
ms.date: 09/15/2022
ms.topic: article
audience: Developer
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: mnordick
ms.search.validFrom: 2022-09-13
ms.openlocfilehash: c1f749085a635a8b640a8ea49a9f0ba434cedac8
ms.sourcegitcommit: d2046cad5de570e6302a4390b41881a7ecb12e26
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/15/2022
ms.locfileid: "9521879"
---
# <a name="secure-one-box-development-environments"></a>ワンボックス開発環境のセキュリティ保護

[!include [banner](../includes/banner.md)]

この記事では、ワンボックス開発環境をセキュリティで保護する方法について説明します。

ワンボックス開発環境は、ご利用の Azure サブスクリプションに配置された Microsoft Azure リソースで構成されます。

ワンボックス開発環境を配置すると、次の Azure リソースが配置されることが想定されます:

- 1 仮想マシン (VM)
- 5 ディスク
- 1 ロード バランサー
- 1 通常のネットワーク インターフェイス
- 1 ネットワーク セキュリティ グループ
- 1 仮想ネットワーク
- 1 パブリック IP アドレス
- 1 ストレージ アカウント
- 製品バイナリのストレージが「dyn」ではじまる 1 つ以上の追加ストレージ アカウント

これらの Azure リソースは独自に管理されるため、組織に固有のセキュリティおよびコンプライアンス要件に準拠する必要がある場合があります。 また、Microsoft Developer や Azure Well-Architected のセキュリティ評価などのソースからの推奨事項は、ワンボックス開発環境に適用される場合があります。 この記事では、ワンボックス環境を最適に保護するための判断に役立つ、これらの推奨事項について説明します。

## <a name="default-configuration"></a>既定コンフィギュレーション

初期状態では、ワンボックス開発環境には次の基本的なセキュリティ構成があります:

- VM の管理ポートは、Microsoft Dynamics Lifecycle Services の IP アドレスに制限されます。 このような制限は、環境のリソース グループ内のネットワーク セキュリティ グループで確認できます。 Lifecycle Services は、Windows Remote Management (WinRM) 管理ポート (5986) を使用して、環境の初期構成を行い、Lifecycle Services からパッケージを配置するなどの操作を可能にします。
- リモート デスクトップ プロトコル (RDP) は、ワンボックス環境にアクセスするための主要な方法の 1 つです。 したがって、RDP ポート (3389) は既定で許可されます。 RDP アクセスは、ネットワーク セキュリティ グループの独自のクライアント IP アドレスに制限することができます。 ベスト プラクティスとして、配置後はアクセスが必要なクライアントに対し、RDP アクセスを制限する必要があります。 顧客は、Azure Bastion などの他の Azure テクノロジを使用して、RDP アクセスを安全に取得することも検討できます。
- ポート 443 では、ワンボックス環境には、HTTPS トラフィック用に公開されているパブリック エンドポイントがあります。 このエンドポイントは環境 URL で使用され、VM で実行される製品自体へのアクセスを提供します。 既定では、エンドポイントはインターネットに公開されます。 サイトへのサインインには認証が必要ですが、ベスト プラクティスとして、それを必要とするクライアントにポート 443 へのアクセスを制限する必要があります。 この構成は組織に固有のものであり、環境の配置後に定義する必要があります。
- ストレージ アカウントは、ドキュメント添付ファイルなど、SQL 以外のデータを格納するための環境に関連付けられています。 VM の構成ファイルには、環境がストレージ アカウントにアクセスできるように、暗号化フィールドのストレージ キーが含まれています。 製品機能の一部には、ストレージ アカウントが外部からアクセス可能である必要があるため、ストレージ アカウントにはパブリックにアクセスできる IP アドレスがあります。
- サブスクリプションの追加のストレージ アカウント ("dyn" で始まる) を使用して、財務と運用コード パッケージをホストします。 また、このストレージ アカウントはパブリックにアドレス指定可能であり、Lifecycle Services が配置のためのコード パッケージにアクセスするために必要です。

## <a name="deploy-to-a-custom-virtual-network"></a>カスタム仮想ネットワークへの配置

Lifecycle Services を使用すると、配置時にカスタム仮想ネットワークを選択できます。 これにより、ワンボックス環境の VM を事前構成済みの仮想ネットワークに直接配置できます。 ただし、カスタム仮想ネットワークを使用する場合は、Lifecycle Services 機能の機能を継続させ、環境の配置が成功するように、いくつかの点を考慮する必要があります。

- Lifecycle Services からの IP アドレスは、VM のポート 5986 にアクセスできる必要があります。 このポートは、Lifecycle Services からの環境を配置および管理するために必要です。

### <a name="lifecycle-services-regional-instances-and-ips"></a>Lifecycle Services の地域インスタンス と IP

次の表に、Lifecycle Services の地域インスタンスを示します。

> [!IMPORTANT]
> これらの地域インスタンスは、プロジェクトと環境を管理するためにサインインする Lifecycle Services ポータルに対応します。 ポータルの場所は、開発環境を配置する地域とは異なる場合があります。

| 場所 | Lifecycle Services URL | Lifecycle Services IP アドレス |
|---|---|---|
| 米国/パブリック | lcs.dynamics.com | 191.239.20.104<br>40.76.5.241<br>40.112.209.123<br>40.121.208.21<br>40.118.145.241 |
| Azure Government | gov.lcs.microsoftdynamics.us | 52.227.70.23<br>13.72.15.62<br>23.97.12.187<br>13.72.20.213 |
| 中国 | lcs.dynamics.cn | 40.73.5.94<br>40.73.64.218<br>40.112.209.123<br>40.121.208.21 |
| ヨーロッパ | eu.lcs.dynamics.com | 40.114.140.114<br>40.115.104.173 |
| フランス | fr.lcs.dynamics.com | 40.89.132.81<br>40.89.155.166<br>40.89.130.72<br>52.136.130.60<br>52.136.130.76 |
| 南アフリカ | sa.lcs.dynamics.com | 102.133.165.35<br>102.133.67.149<br>40.127.1.92<br>102.133.67.146<br>40.127.4.34 |
| スイス | ch.lcs.dynamics.com | 51.103.133.142<br>51.103.146.43<br>51.103.138.255<br>51.107.226.123<br>51.107.224.152<br>51.107.224.175 |
| アラブ首長国連邦 | uae.lcs.dynamics.com | 20.45.79.158<br>40.123.207.67<br>20.45.64.174<br>40.123.217.56<br>20.45.79.195 |

- 仮想ネットワークのネットワーク セキュリティ グループの外部で上位レベルのファイアウォールを使用している場合は、Lifecycle Services のソース IP アドレスから、より広範な受信ポートを許可する必要があります。 この要件が存在するのは、ロード バランサーが 50000-65535 の範囲のランダム化されたポートを、WinRM や RDP のポートなどの既知のポートにマップするように構成されているからです。 Lifecycle Services からの配置では、この範囲のポートにアクセスできる必要があります。
- HTTPS ポート (443) は、外部に公開する必要はなく、配置操作や管理操作時に使用されません。
- 発信インターネット アクセスは、仮想ネットワークから開いたままにしておく必要があります。 財務と運用アプリでは、さまざまな製品機能にインターネット アクセスが必要です。 例えば、認証には Azure Active Directory (Azure AD) へのアクセスが必要です。

カスタム仮想ネットワークへの配置は、高度な構成です。 上記のガイダンスは、カスタム仮想ネットワークを正常に使用するために役立つ要件の概要として提供されます。 仮想ネットワークの構成が正しくない場合、Lifecycle Services からの配置または管理の操作ができない可能性があります。 したがって、カスタマイズが外部統合に与える影響を理解するようにしてください。

> [!NOTE]
> Microsoft サポートでは、さまざまなカスタマイズが考えられるため、カスタム構成に関する問題をトラブルシューティングできません。 トラブルシューティングの推奨事項は、既定の構成を既知の正常な構成として使用することです。 その後、追加の制限を段階的に適用し、必要なカスタム コンフィギュレーションで問題を切り分けます。

## <a name="security-architecture-recommendations"></a>セキュリティ アーキテクチャの推奨事項

Microsoft Defender と Azure Well-Architected のセキュリティ評価は、ワンボックス開発環境リソースを含む、サブスクリプションでプロビジョニングする Azure リソースに適用される一般的なセキュリティ ガイダンスを提供します。

推奨事項がユーザーと組織のポリシーに適しているかどうかを検討する場合は、上記のガイダンスに従うことが重要です。 たとえば、セキュリティ評価がこれらのポートへのアクセスを閉じることを推奨している場合でも、Lifecycle Services が環境を管理するために管理ポートにアクセスできる必要があります。 別の例として、ガイダンスでは、環境のストレージ アカウントへのネットワーク アクセスを制限することをお勧めします。 ただし、このような制限は、ファイルをダウンロードするために外部からアクセスできる必要がある、Excel へのエクスポートなどの一部の統合シナリオを無効にします。 最後に、診断とテレメトリーのログに関する一部の推奨事項では、リソース 所有者がその推奨事項がニーズに適用できるかどうかを考慮する必要がある追加費用が発生する場合があります。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

### <a name="why-does-my-newly-provisioned-one-box-developer-environment-have-security-recommendations-from-microsoft-defender-and-other-security-assessments"></a>新たにプロビジョニングしたワンボックス開発環境では、Microsoft Defender と他のセキュリティ評価からのセキュリティ推奨事項があるのはなぜですか?

このような評価からの多くの推奨事項では、追加費用が発生するかどうかを判断するために、リソース所有者の関与が必要です。 セキュリティ推奨事項の実装を評価する際は、この記事のガイダンスを検討する必要があります。

### <a name="i-want-to-restrict-network-access-to-my-one-box-developer-environment-to-help-limit-my-security-exposure-how-can-i-block-network-access"></a>セキュリティ上のリスクを抑えるため、ワンボックス開発環境に対するネットワーク アクセスを制限する必要があります。 ネットワーク アクセスをブロックするにはどうすればよいですか? 

- VM アクセスを制限するには、環境のリソース グループ内のネットワーク セキュリティ グループを使用します。 WinRM 管理ポート (5986) は、Lifecycle Services でのみアクセスできるように既に制限されています。 既定では、RDP ポート (3389) と HTTPS ポート (443) のネットワーク セキュリティ グループ ルールは、制限されません。 ただし、選択したクライアント IP まで制限できます。
- 財務と運用アプリが機能するには、発信インターネット アクセスを利用できる状態にしておく必要があります。
- 環境の Azureストレージ アカウントはアクセスを制限できますが、VM のパブリック IP アドレスと承認されたクライアントの IP アドレスでアクセス可能な状態を維持する必要があります。 アクセスを正しく許可しないと、ストレージ機能に依存する財務と運用機能は失敗します。

### <a name="my-deployment-fails-when-i-try-to-provision-with-my-custom-virtual-network-can-microsoft-tell-me-what-is-wrong"></a>カスタム仮想ネットワークを使用してプロビジョニングしようとすると、配置が失敗します。 Microsoft は何が間違っているのかを教えてくれますか?

この記事の [カスタム仮想ネットワークへの配置](#deploy-to-a-custom-virtual-network) セクションでは、お使いの環境での Azure リソースのネットワーク アクセス要件の一覧が示されます。 残念ながら、Microsoft サポートでは、さまざまな構成が考えられるため、カスタム ネットワーク構成をトラブルシューティングできません。 トラブルシューティングの推奨事項は、既定の構成を既知の正常な構成として使用することです。 その後、追加の制限を段階的に適用し、必要なカスタム コンフィギュレーションで問題を切り分けます。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
