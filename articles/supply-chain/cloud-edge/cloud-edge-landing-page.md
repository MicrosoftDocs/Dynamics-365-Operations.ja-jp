---
title: 分散ハイブリッド トポロジのスケール ユニット
description: このトピックでは、製造および倉庫管理のワークロードのクラウドおよびエッジのスケール ユニットに関する情報を提供します。
author: cabeln
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 59d246dd348bca6c00dc90b19353a382986841f2
ms.sourcegitcommit: a21166da59675e37890786ebf7e0f198507f7c9b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/03/2021
ms.locfileid: "7471743"
---
# <a name="scale-units-in-a-distributed-hybrid-topology"></a>分散ハイブリッド トポロジのスケール ユニット

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Microsoft Dynamics 365 Supply Chain Management のスケール ユニット機能は、サービスの使用を管理する条項に基づいて提供されます。 詳細については、[Microsoft Dynamics の法的情報](https://go.microsoft.com/fwlink/?LinkID=290927) を参照してください。
>
> クラウドおよびエッジのスケール ユニットを有効にする際、クラウドおよびエッジのスケール ユニットの構成と処理に関連するデータが米国にあるデータ センターに保存されることを理解できることを確認するよう求められます。 クラウドおよびエッジのスケール ユニットのデータ処理の詳細については、このトピックの後半の[スケール ユニットの管理中のデータ処理](#data-processing-management) セクションを参照してください。

## <a name="core-value-proposition-for-a-distributed-hybrid-topology"></a>分散ハイブリッド トポロジの主な価値提案

製造と流通が行われる会社は、重要な業務プロセスを年中無休 24 時間対応で実行でき、中断や規模の変更を行うことはできません。 分散ハイブリッド トポロジを使用すると、ネットワーク接続や待機時間の問題が発生した場合でも、業務上不可欠な製造および倉庫の主要なプロセスを中断することなく実行できます。

分散ハイブリッド トポロジでは *スケール ユニット* の概念が導入されており、作業現場と倉庫の実行ワークロードを異なる環境間で配分できるようになります。 この機能は、パフォーマンスの向上、サービス中断の防止、アップタイムの最大化に役立ちます。 スケール ユニットは、Supply Chain Management サブスクリプションの次のアドインを通じて提供されます。

- Dynamics 365 Supply Chain Management のクラウド スケール ユニットのアドイン (*2021 年 4 月より利用可能*)
- Dynamics 365 Supply Chain Management のエッジ スケール ユニットのアドイン (*まもなく利用できます*)

ワークロード機能は、段階的な拡張によって継続的にリリースされています。

## <a name="scale-units-and-dedicated-workloads"></a>スケール ユニットと専用ワークロード

スケール ユニットは、専用の処理能力を追加することによって、Supply Chain Management の中央ハブ環境を拡張します。 スケール ユニットはクラウドで実行できます。 また、ローカル施設のオンプレミスで、エッジで動作させることもできます。

:::image type="content" source="./media/cloud_edge-HeroDiagram.png" alt-text=" スケール ユニット付き Dynamics 365。":::

スケール ユニットは、割り当てられたワークロードに対して、弾力性、信頼性、およびスケールを提供します。 エッジ スケール ユニットはクラウド ハブ環境から一時的に切断でき、作業者はエッジ上の割り当てられたワークロードで作業を続行します。

*ワークロード* とは、定義された一連のビジネス機能であり、除外してスケール ユニットに委任することができます。 倉庫管理のワークロードはリリースされましたが、製造実行のワークロードは引き続きプレビュー段階にあります。

[スケール ユニット マネージャー ポータル](https://sum.dynamics.com) を使用して、選択したワークロードのハブ環境とクラウドのスケール ユニットを構成することができます。 スケール ユニットごとに複数のワークロードを割り当てることもできます。 現在のリリースでのクラウド スケール ユニットの前提条件と制限については、このトピックの後半の[クラウド スケール ユニットの前提条件と制限](#cloud-scale-unit-prerequisites) を参照してください。

### <a name="dedicated-warehouse-management-workload-capabilities-in-a-scale-unit"></a>スケール ユニットの専用の倉庫管理ワークロード機能

倉庫管理ワークロードは、一般提供のためにリリースされたスケール ユニットの最初の分散ワークロードです。

倉庫管理では、スケール ユニットは次の機能を提供します。

- システムでは、販売注文および需要補充のために選択したウェーブ メソッドを処理できます。
- 倉庫の作業者は、倉庫管理モバイル アプリを使用して販売と需要の補充倉庫作業を実行できます。
- 倉庫の作業者は、倉庫管理モバイル アプリを使用して手持在庫を照会できます。
- 倉庫の作業者は、倉庫管理アプリを使用して手持在庫の移動を作成・実行できます。
- 倉庫作業者は、倉庫管理モバイルアプリを使用した発注書の登録と、プットアウェイを実行できます。

詳細については、[クラウドおよびエッジのスケール ユニットに対する倉庫管理ワークロード](cloud-edge-workload-warehousing.md) を参照してください。

### <a name="dedicated-manufacturing-execution-workload-capabilities-in-a-scale-unit"></a>スケール ユニットの専用の製造実行ワークロード機能

製造ワークロードの最初のリリースは現在プレビュー段階にあり、以下の機能を提供します。

- 機械オペレーターと作業現場監督は、運用生産計画にアクセスできます。
- 機械オペレーターは、個々の製造ジョブを実行することによって、計画を最新の状態に保つことができます。
- 作業現場の監修者は、運用計画を調整できます。
- 作業者は、正しい作業者支払計算を確実に行うために、エッジでの出勤と退勤の時刻と出勤にアクセスできます。

詳細については、[クラウドおよびエッジのスケール ユニットの製造実行ワークロード](cloud-edge-workload-manufacturing.md) を参照してください。

## <a name="considerations-before-you-enable-the-distributed-hybrid-topology-for-supply-chain-management"></a>Supply Chain Management の分散されたハイブリッドのトポロジを有効にする前の考慮事項

分散ハイブリッド トポロジを有効にすることで、Supply Chain Management クラウド環境がハブとして機能するように移行します。 また、クラウドまたはエッジでスケール ユニットとして構成された追加の環境を関連付けることもできます。

### <a name="prerequisites-and-limitations-for-cloud-scale-units"></a><a name="cloud-scale-unit-prerequisites"></a>クラウド スケール ユニットの前提条件および制限

スケール ユニットの現在のリリースでは、一部の機能はまだ使用できませんが、今後の段階的なリリースによって追加される可能性があります。

#### <a name="you-must-be-a-licensed-customer-of-supply-chain-management"></a>Supply Chain Management のライセンスが必要

分散トポロジにオンボードするには、Supply Chain Management のライセンスが必要です。 既存のクラウド環境は、ハイブリッド トポロジのハブになります。 サンドボックス環境と運用環境の両方をハブ環境として宣言し、取得したアドインに応じてスケール ユニットを追加できます。

#### <a name="your-existing-project-must-be-administered-via-the-global-commercial-version-of-lcs"></a>既存のプロジェクトは LCS のグローバル商用バージョンを介して管理する必要がある

既存の Microsoft Dynamics Lifecyle Services (LCS) プロジェクトは、次のバージョン要件を満たす必要があります。

- プロジェクトは LCS のグローバル商用バージョンを介して、[lcs.dynamics.com](https://lcs.dynamics.com) で管理する必要があります。
- ローカル バージョンの LCS ([eu.lcs.dynamics.com](https://eu.lcs.dynamics.com) や [fr.lcs.dynamics.com](https://fr.lcs.dynamics.com)) はサポートされていません。
- LCS の政府クラウドのバージョンはサポートされていません。
- LCS の Mooncake バージョンはサポートされていません。

#### <a name="your-current-production-environment-must-be-of-the-self-service-type-in-lcs"></a>現在の運用環境が LCS のセルフサービス タイプである必要がある

現在の運用環境が LCS で **セルフサービス** タイプでタグ付けされている必要があります。 このタイプは、LCS プロジェクトのテナントが、Azure Service Fabric ホスティング モデルをサポートするように既に変換されていることを示します。

> [!IMPORTANT]
> サービスとしてのインフラストラクチャとして実行する環境タイプ (IaaS) はサポートされていません。 通常、これらの環境は、LCS で **Microsoft 管理** タイプでタグ付けされます。 このタイプの環境がある場合は、Microsoft の連絡先と連携して、**セルフサービス** タイプへの移行タイムラインについて把握する必要があります。

Microsoft では、Supply Chain Management のすべてのクラウド環境を IaaS モデルから Service Fabric でホストされているトポロジに移行しています。 この移行により、スケーラビリティが向上し、サービス管理が容易になります。 したがって、配置とメンテナンスの操作が迅速になります。 同様に、サービス コンポーネントをマイクロサービスの概念に移行すると、サービス ホスティング モデルは仮想マシン (VM) モデルから、コンテナ化された軽量アーキテクチャに[移行](/virtualization/windowscontainers/about/containers-vs-vm) します。

最終的には、Service Fabric ベースのコンテナ化されたサービス インフラストラクチャは、インスタンスがクラウドのハブであるか、クラウドのスケール ユニットであるか、エッジであるかにかかわらず、サービスのクラウドとエッジの両方のインスタンスに対応します。

スケール ユニットをサポートするハイブリッド トポロジにオンボードする前に、プロジェクト テナントを Service Fabric ホスト モデルに移行する必要があります。 また、ハブとなる環境はすべて変換する必要があります。

> [!TIP]
> LCS プロジェクト テナントのステータスを照会するには、[LCS](https://lcs.dynamics.com/) 内の環境のタイプを検索するか、パートナーまたは Microsoft の連絡先までお問い合わせください。

#### <a name="local-business-data-on-premises-environments-arent-supported-as-hubs-for-scale-units"></a>ローカル ビジネス データ (オンプレミス) 環境はスケール ユニットのハブとしてはサポートされない

オンプレミス環境は、スケール ユニットのハブとしては機能しません。 ハブ環境は常にクラウドでホストされている必要があります。

#### <a name="scale-unit-management-capabilities-are-limited"></a>スケール ユニット管理機能は限定的

ワークロードの移動に役立つ管理機能は限られています。 一部の管理操作はセルフサービス方式でサポートされていないので、パートナーまたは Microsoft の連絡先を通じてサポートを依頼する必要があります。 たとえば、スケール ユニット間でのワークロードの移動や、障害シナリオでの一時的なアドホック移動などがあります。

#### <a name="metrics-and-measurements-arent-yet-available"></a>指標と測定は現時点では利用できない

スケール ユニットに最適なアプリケーションを選択するのに役立つ指標および測定はまだ利用できません。 Microsoft の連絡先または実装パートナーと連携して、最も有益なアプリケーションを選択してください。

### <a name="data-processing-during-management-of-scale-units"></a><a name="data-processing-management"></a>スケール ユニットの管理中のデータ処理

Dynamics 365 環境を有効にして、クラウドおよびエッジ スケール ユニットの分散ハイブリッド トポロジをサポートすると、一部の管理サービスは LCS のように米国でのみホストされます。 この動作は、[スケール ユニット マネージャー ポータル](https://sum.dynamics.com) で使用される一部の管理情報および構成情報の転送と保存に影響します。 次にいくつか例を挙げます。

- テナント名と ID
- 自分の LCS プロジェクト ID
- サインインに使用する管理者およびプロジェクト所有者のメール アドレス
- ハブとスケール ユニットの環境 ID
- トポロジを地理的な地図上に表示するための、法人や施設の名前と物理的な住所を含むワークロードの構成
- マップ分析ページに表示される、スケール ユニットの最も有益な使用を選択するのに役立つ収集されたメトリック (待機時間やスループットなど)

転送され、米国のデータ センターに保存されているデータは、Microsoft データ保持ポリシーに従って削除されます。 Microsoft にとってお客様のプライバシーは重要です。 詳細については、Microsoft の [プライバシーに関する声明](https://go.microsoft.com/fwlink/?LinkId=521839) をお読みください。

## <a name="onboarding-in-two-stages"></a>2 つのステージでのオンボード

分散ハイブリッド トポロジにオンボードするプロセスには 2 つのステージがあります。 最初のステージでは、カスタマイズを検証して、スケール ユニットを含む分散トポロジで機能することを確認する必要があります。 サンドボックス環境及び運用環境は、2 つ目のステージでのみ移動されます。

### <a name="stage-1-evaluate-customizations-in-one-box-development-environments"></a>ステージ 1: 1 ボックス開発環境でのカスタマイズを評価する

サンドボックス環境や運用環境のオンボードを開始する前に、1 ボックス環境 (第 1 層環境とも呼ばれる) などの開発環境でスケール ユニットを検討し、プロセス、カスタマイズ、ソリューションを検証することをお勧めします。 このステージでは、データとカスタマイズが 1 ボックス環境に適用されます。 1 つの環境はハブのロールを持ち、もう一方の環境はスケール ユニットのロールを持ちます。 この設定によって、問題を特定して修正する最善の方法を提供します。 このステージを完了するために、最新の早期アクセス (PEAP) ビルドも使用できます。

ステージ 1 の場合は、[1 ボックス開発環境用のスケール ユニット配置ツール](https://github.com/microsoft/SCMScaleUnitDevTools) を使用する必要があります。 これらのツールを使用すると、1 つまたは 2 つの 1 ボックス環境で、ハブとスケール　ユニットを構成できます。 このツールは、GitHub 上でバイナリ リリースとしてソース コードで提供されています。 ツールの使用方法を説明した[ステップ バイ ステップの使用ガイド](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide) が掲載されているプロジェクト Wiki をご覧ください。

### <a name="stage-2-acquire-add-ins-and-deploy-in-your-sandbox-and-production-environments"></a>ステージ 2: アドインを入手し、サンドボックス環境と運用環境に配置する

サンドボックス環境または運用環境の 1 つを新しいトポロジにオンボードするには、1 つ以上のクラウド スケール ユニット (将来的にはエッジ スケール ユニット) のアドインを入手する必要があります。 このアドインにより、[LCS](https://lcs.dynamics.com/) の対応するプロジェクトおよび環境のスロットが付与され、スケール ユニット環境を配置できるようになります。

> [!NOTE]
> スケール ユニットのアドインは、限定されたユーザーに結合されているわけではなく、管理者が割り当てたロールに基づいて、既存のサブスクリプションのすべてのユーザーが使用することができます。

スケール ユニットは、複数の最小在庫管理単位 (SKU) および価格決定オプションで提供されます。 したがって、計画されている月々のトランザクションの量およびパフォーマンス要件を最も満たすオプションを選択できます。

エントリ レベルの SKUは *Basic*、より高いパフォーマンスの SKU は *Standard* と呼ばれています。 各 SKU には、特定の数の月々のトランザクションが事前に読み込まれます。 ただし、各 SKU に対して超過分のアドインを追加すると、月々のトランザクション予算を増やすことができます。

:::image type="content" source="media/SKUs-highlevel.png" alt-text=" クラウド スケール ユニットのアドイン。":::

> [!TIP]
> ニーズを最も満たすサイズ変更を見極めるためには、パートナーや Microsoft と連携して、必要な月々のトランザクション サイズについて把握する必要があります。

各スケール ユニットのアドインを購入すると、月々のトランザクションの量が増えるだけでなく、LCS で特定の数の環境スロットを利用する権利を得ることができます。 各クラウド スケール ユニットのアドインに対して、新しい運用スロットと新しいサンドボックス スロットを利用できます。 オンボード プロセスでは、これらのスロットを持つ新しい LCS プロジェクトが追加されます。 スロットの使用権は、クラウド ハブを持つスケール ユニットとして使用されなければならないように制限されています。

超過分のアドインでは、新しい環境のスロットを利用する権利は与えられません。

より多くのサンドボックス環境を取得する場合は、通常のサンドボックス スロットを追加で購入できます。 その後、Microsoft がこれらのスロットをハイブリッド トポロジのサンドボックス スケール ユニットとして有効にするようお手伝いします。

## <a name="onboard-to-the-distributed-hybrid-topology-for-supply-chain-management"></a>分散ハイブリッド トポロジにオンボードするには、Supply Chain Management のライセンスが必要

### <a name="select-your-lcs-project-tenant-and-the-detailed-onboarding-process"></a>LCS プロジェクト テナントと詳細オンボード プロセスの選択

Supply Chain Management の分散ハイブリッド トポロジへのオンボード方法の計画が完了したら、[スケール ユニット マネージャー ポータル](https://aka.ms/SCMSUM) を使用してオンボード プロセスを開始します。 ポータルでは、**Dynamics 365 テナント** タブを選択します。このタブには、自分のアカウントが含まれている、自分が LCS プロジェクトの所有者または環境管理者であるテナントの一覧が表示されます。

探しているテナントが一覧に含まれていない場合、[LCS](https://lcs.dynamics.com/v2) に移動して、環境管理者か、そのテナントの LCS プロジェクトのプロジェクト所有者かを確認してください。 選択したテナントの Azure Active Directory (Azure AD) アカウントのみが、サインアップのエクスペリエンスを完了することが許可されています。

> [!NOTE]
> LCS に変更を適用した後は、テナントの一覧に変更が反映されるまでに最大で 30 分かかる場合があります。

一覧には、テナントごとにオンボードのステータスが表示されます。

:::image type="content" source="media/cloud_edge-EnableHybrid1.png" alt-text=" Dynamics 365 テナント タブのテナントの一覧。":::

LCS テナントのプログラムのオンボードを要求するには、**ここをクリックして開始** を選択します。 この条件は同意する必要があります。 また、Microsoft がオンボード プロセスに関連する連絡を送信できるビジネス メール アドレスを指定する必要があります。

:::image type="content" source="media/cloud_edge-EnableHybrid2.png" alt-text=" テナントのサインアップ送信。":::

Microsoft は、お客様の要求を確認し、サインアップ フォームに入力したアドレスにメールで次の手順を通知します。 Microsoft は、お客様のビジネス シナリオにハイブリッド トポロジのスケール ユニットを有効にするために、お客様と緊密に連携していきます。

オンボードが完了した後、ポートを使用してスケール ユニットとワークロードを構成できます。

### <a name="manage-cloud-scale-units-and-workloads-by-using-the-scale-unit-manager-portal"></a><a name="scale-unit-manager-portal"></a>スケール ユニット マネージャー ポータルを使用して、Cloud Scale Unit とワークロードを管理します

[スケール ユニット マネージャー ポータル](https://aka.ms/SCMSUM) に移動して、テナント アカウントを使用してログインします。 **スケール ユニットの構成** ページでは、ハブ環境がまだ一覧にない場合は追加できます。 次に、スケール ユニットとワークロードを構成するハブを選択できます。

:::image type="content" source="media/cloud_edge-Manage.png" alt-text=" スケール ユニットとワークロードの管理体験。":::

サブスクリプションで使用できる 1 つ以上のスケール ユニットを追加するには、**スケール ユニットを追加** を選択します。

**定義されたワークロード** タブで、**ワークロードの作成** ボタンを使用して、倉庫管理ワークロードをスケール ユニットの 1 つに追加します。 各ワークロードに対して、ワークロードによって所有されるプロセスのコンテキストを指定する必要があります。 倉庫管理ワークロードの場合、コンテキストは特定のサイトおよび法人の特定の倉庫になります。

:::image type="content" source="media/cloud_edge-DefineWorkload.png" alt-text=" ワークロードの作成。":::

> [!TIP]
> 今後、スケール ユニット マネージャーの操作性を段階的に向上させ、ライフサイクル管理の操作を容易にしていく予定です。 今回のリリースの具体的な機能については、Supply Chain Management の分散ハイブリッド トポロジへのオンボードを進めているお客様に提供されるオンボード ハンドブックに記載されています。 <!-- KFM: Add a link to the handbook when it is published -->

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
