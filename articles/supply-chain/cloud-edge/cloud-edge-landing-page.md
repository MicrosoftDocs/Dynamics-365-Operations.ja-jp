---
title: 製造と倉庫管理ワークロードのためのクラウドおよびエッジのスケール ユニット
description: このトピックでは、製造および倉庫管理のワークロードのクラウドおよびエッジのスケール ユニットに関する情報を提供します。
author: cabeln
manager: ''
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 3a23ee452535423684c6d210a448ee768379fa08
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516824"
---
# <a name="cloud-and-edge-scale-units-for-manufacturing-and-warehouse-management-workloads"></a>製造と倉庫管理ワークロードのためのクラウドおよびエッジのスケール ユニット

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

クラウドおよびエッジのスケール ユニットによって、作業現場と倉庫の実行ワークロードを異なる環境間で配分できるようになります。 この機能は、パフォーマンスの向上、サービス中断の防止、アップタイムの最大化に役立ちます。 この情報は、次のアドインによって提供されます。

- Dynamics 365 Supply Chain Management のクラウド スケール ユニットのアドイン
- Dynamics 365 Supply Chain Management のエッジ スケール ユニットのアドイン

製造と流通が行われる会社は、重要な業務プロセスを年中無休 24 時間対応で実行でき、中断や規模の変更を行うことはできません。 クラウドおよびエッジのスケール ユニットを使用すると、ネットワーク接続や待機時間の問題が発生した場合でも、業務上不可欠な製造および倉庫の主要なプロセスを中断することなく実行できます。

## <a name="public-preview-information"></a>パブリック プレビュー情報

このプレビューでは、Dynamics 365 Supply Chain Management 環境のクラウドベースのハブとして機能する環境と、クラウド スケール ユニットとして機能する 1 つの環境を提供します。

<!-- You will also be able to use Local Business Data (LBD) to configure an on-premises environment as an edge scale unit for the hub you received as part of the preview program.-->

### <a name="preview-availability"></a>プレビューの可用性

クラウドおよびエッジのスケール ユニットのプレビューは、2020 年 10 月に Supply Chain Management の既存の顧客が使用できるようになります。

[Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/v2) 環境でデプロイ用に 10 月のプレビュー リリース 10.0.15/プラットフォーム アップデート 39 にアクセスするには、Supply Chain Management のプレビュー アーリー アクセス プログラム (PEAP とも呼ばれる) を持っている必要があります。 より広範な [Dynamics Insider Program](https://experience.dynamics.com/insider) のメンバーに既になっている場合は、PEAP に参加できます。 "Finance & Operations: Preview early access program (PEAP)" という名前の特定プログラムを選択するだけです。

> [!IMPORTANT]
> Supply Chain Management のスケール ユニット機能は、[Finance and Operations のクラウド + エッジ プレビューの条件](https://Aka.ms/SCMCnETerms) に合意した場合にのみ使用可能になります。

### <a name="data-processing-for-the-preview"></a>プレビューのデータ処理

パブリック プレビュー中に、一部の管理サービスは米国でのみでホストされます。 ただし、この機能を使用できるようになると、Supply Chain Management でサポートされているすべての地域で、この管理サービスを利用できるようになります。 これにより、スケール ユニット マネージャによって使用される管理情報の転送と保管に影響します。これには次のものが含まれています。

- テナント名と ID
- 自分の LCS プロジェクト ID
- ログインに使用する管理者のメール
- ハブとスケール ユニットの環境 ID
- ワークロードの構成
- [マップ分析] ページに表示される収集されたメトリック (遅延時間やスループットなど)

米国データ センターに転送および保存されたデータは、プレビュー環境をシャットダウンしたときに削除されます。

### <a name="sign-up-for-the-preview"></a>プレビューへのサインアップ

Supply Chain Management のためにクラウドとエッジのプレビューを登録するには、組織が既に Supply Chain Management のクラウド環境を所有している必要があります。

スケール ユニット機能は現在、パブリック プレビューにあります。 サインアップを行うときには、特定のテナントに対してユーザー アカウントを使用する必要があります。 また、プロジェクトの所有者やそのテナントの有効な Dynamics 365 LCS プロジェクトの環境管理者でもある必要があります。

プレビューにサインアップする際には、テナントを選択し、サインアップの手順に進みます。 Microsoft はプレビュー容量を割り当てるとすぐに、適切な LCS プロジェクトのための 2 つの環境 (ハブとスケール ユニット) の [プロビジョニングの詳細] や [プロモーション] コードを含む電子メールを送信します。 これにより、2 つの環境を、第 2 階層のサンドボックス環境として配置できるようになります。 これらの環境では、プロモーション コードの作成日からの有効期間は 60 日です。 次の段落で説明されている手順が完了するまでは、2 つの環境を使用しないでください。

2 つの環境がプロモーションコードを使用して配置されていることを確認した後、いずれかの環境がハブとして機能するように構成され、もう一方がスケール ユニットとして機能するように構成されます。 その後、スケール ユニットを構成したり、選択した倉庫管理と製造ワークロードを [スケール ユニット マネージャー ポータル](https://aka.ms/SCMSUM) を使用して配置したりできます。

プレビュー環境は、60 日後に自動的に削除されます。 ただし、使用されていない可能性がある場合は、すぐに削除されることがあります。 プレビュー環境を削除した後で、サインアップしてキューに追加し、新しいプレビューをデプロイすることができます。

プレビューにサインアップするには、[スケール ユニット マネージャー ポータル](https://aka.ms/SCMSUM) に移動します。

### <a name="limitations-that-apply-during-the-preview-period"></a>プレビュー期間中に適用される制限事項

> [!IMPORTANT]
> この機能のプレビュー プログラムの初期フェーズでは、Microsoft は、エッジ スケール ユニットを持つハブではなく、クラウド スケール ユニットが設定されたハブのみをサポートしています。 エッジ スケール ユニットはオンプレミスでインストールされており、プログラムの今後のフェーズで使用できるようになります。

クラウドおよびエッジのスケール ユニットはプレビュー機能であるため、これらに関連するサービスは現在、限定された国および地域で使用できます。 クラウドおよびエッジのスケール ユニットを有効にすることにより、クラウドおよびエッジのスケール ユニットの構成と処理に関連するデータが米国にあるデータ センターに保存されることを理解できることを確認してください。 クラウドおよびエッジのスケール ユニット を有効にすることにより、[Finance and Operations のクラウド + エッジ プレビューの条件](https://Aka.ms/SCMCnETerms) にも同意することになります。 クラウドおよびエッジのスケール ユニット の詳細については、[ドキュメント](https://aka.ms/scmcne) を参照してください。

Microsoft にとってお客様のプライバシーは重要です。 詳細については、Microsoft の [プライバシーに関する声明](https://aka.ms/privacy) をお読みください。

> [!IMPORTANT]
> ワークロードがスケール ユニットで使用されている場合は、すべてのビジネス機能がパブリック プレビューで完全にサポートされているわけではありません。 機能ワークロードの詳細については、このトピックで後述するセクションを参照してください。

## <a name="scale-units-and-dedicated-workloads"></a>スケール ユニットと専用ワークロード

:::image type="content" source="./media/cloud_edge-HeroDiagram.png" alt-text="スケール ユニット付き Dynamics 365":::

スケール ユニットは、専用の処理能力を追加することによって、Supply Chain Management の中央ハブ環境を拡張します。 スケール ユニットはクラウドで実行できます。 また、ローカル施設内のエッジで実行することもできます。 スケール ユニットは、ハブ環境から一時的に切断できます。 これらが接続されている場合、スケール ユニットでは、割り当てられたワークロードの専用処理を実行するために必要なすべての情報が表示されます。

:::image type="content" source="media/cloud_edge-previewoptions.png" alt-text="パブリック プレビューのスケール ユニット オプション":::

パブリック プレビューの場合は、スケール ユニット マネージャ ポータルを使用して、選択したワークロードを使用して、クラウド スケール単位でハブ環境を構成できます。 ローカル ビジネス データ (LBD) オンプレミス環境へのアクセス許可を持つ参加者は、LBD 環境をエッジ スケール ユニットとして構成することもできます。

ワークロードとは、定義された一連のビジネス機能であり、除外してスケール ユニットに委任することができます。 現在、プレビュー機能には次の 2 つのタイプのワークロードがあります。

- 製造実行
- 倉庫管理

スケール ユニットごとに、各タイプのワークロードのいずれかを割り当てることができます。 

### <a name="dedicated-manufacturing-execution-workload-capabilities-in-a-scale-unit"></a>スケール ユニットの専用の製造実行ワークロード機能

エッジ ユニットがクラウドに接続されていない場合でも、製造実行のために、クラウドおよびエッジのスケール ユニットには次の機能があります。

- 機械オペレーターと作業現場監督は、運用生産計画にアクセスできます。
- 機械オペレーターは、個々の製造ジョブを実行することによって、計画を最新の状態に保つことができます。
- 作業現場の監修者は、運用計画を調整できます。
- 作業者は、出勤と出勤の出勤と退勤をエッジで確認して、作業者の支払計算を正しく行うことができます。

詳細については、[製造スケール ユニットのワークロードの詳細](cloud-edge-workload-manufacturing.md) を参照してください。

### <a name="dedicated-warehouse-management-workload-capabilities-in-a-scale-unit"></a>スケール ユニットの専用の倉庫管理ワークロード機能

倉庫管理については、エッジ ユニットがクラウドに接続されていない場合でも、クラウドおよびエッジのスケール ユニットには次の機能があります。

- 選択されたウェーブ メソッドの処理は、販売注文と需要補充に対して有効化されています。
- 倉庫の作業者は、倉庫アプリを使用して販売と需要の補充倉庫作業を実行できます。
- 倉庫の作業者は、倉庫アプリを使用して手持在庫を照会できます。
- 倉庫の作業者は、倉庫アプリを使用して手持在庫の移動を作成および実行できます。
- 倉庫作業者は、倉庫アプリを使用した発注書の登録と、プットアウェイの実行をできます。

詳細については、[倉庫スケール ユニットのワークロードの詳細](cloud-edge-workload-warehousing.md) を参照してください。

## <a name="onboard-scale-units-for-your-supply-chain-management-environment"></a>Supply Chain Management 環境用のオンボードスケール ユニット

### <a name="deploy-the-preview-for-cloud-and-edge-scale-units"></a>クラウドおよびエッジのスケール ユニットのプレビューのデプロイ

次の図は、クラウド スケール ユニットのパブリック プレビューのサインアップとプロビジョニングの流れを示しています。

:::image type="content" source="media/cloud_edge-previewsignup.png" alt-text="サインアップ手順のプレビュー":::

### <a name="select-your-lcs-project-tenant-and-the-detailed-preview-process"></a>LCS プロジェクト テナントと詳細プレビュー プロセスの選択

パブリック プレビューでは、[スケール ユニット マネージャー ポータル](https://aka.ms/SCMSUM) は、自分のアカウントが含まれている、自分が LCS プロジェクトの所有者または環境管理者であるテナントの一覧が表示されます。

探しているテナントがこの一覧に含まれていない場合、[LCS](https://lcs.dynamics.com/v2) に移動して、環境管理者か、そのテナントの LCS プロジェクトのプロジェクト所有者かを確認してください。 選択したテナントの Azure Active Directory (Azure AD) アカウントのみが、サインアップのエクスペリエンスを完了することが許可されています。

> [!NOTE]
> LCS に変更を適用した後は、テナントの一覧に変更が反映されるまでに最大で 30 分かかる場合があります。

一覧には、テナントごとにサインアップのステータスが表示されます。

:::image type="content" source="media/cloud_edge-Signup1.png" alt-text="テナントのサインアップ オプション":::

**こちらをクリックしてサインアップ** リンクを選択して、自分の LCS テナントにサインアップして、プレビューに参加できます。 この条件は同意する必要があります。 また、Microsoft がプレビューのサインアップ処理に関連するメールアドレスを送信できるようにする必要があります。

:::image type="content" source="media/cloud_edge-Signup2.png" alt-text="テナントのサインアップ送信":::

Microsoft は、あなたの要求を確認し、サインアップ フォームに入力した住所にメールで次の手順を通知します。

プレビュー プログラムへのアクセス許可が付与されると、LCS プロジェクトに対して 2 つのプロモーション コードが提供されます。 これにより、これらのプロモーション コードを使用して LCS に 2 つの環境を配置することができます。 環境では、PEAP リリース 10.0.15 かそれ以降のバージョンを使用する必要があります。 プロモーション コードの適用が完了したら、(指示に従って) Microsoftに通知して、プレビュー機能のための環境の有効化を完了します。 この構成手順が完了したときには、Microsoft から通知をお伝えします。

プレビュー環境でのスケール ユニットとワークロードの構成を開始できるようになりました。

> [!IMPORTANT]
> Cloud Scale Unit を構成する際に、[スケール ユニット マネージャー ポータルで必要なステップをすべて実行](#scale-unit-manager-portal) できます。
<!-- >
> If want to use edge scale units with your preview deployment, you must do all scale unit configuration in the user interface on the hub as described in [Configure the hub environment for use with edge scale units](cloud-edge-edge-scale-units-lbd.md#configure-the-hub-environment). You can't use Scale Unit Manager portal if you include an edge scale unit. -->

### <a name="manage-cloud-scale-units-and-workloads-by-using-the-scale-unit-manager-portal"></a><a name="scale-unit-manager-portal"></a>スケール ユニット マネージャー ポータルを使用して、Cloud Scale Unit とワークロードを管理します

[スケール ユニット マネージャー ポータル](https://aka.ms/SCMSUM) に移動して、テナント アカウントを使用してログインします。 **スケール ユニットの構成** ページでは、ハブ環境がまだ一覧にない場合は追加できます。 次に、スケール ユニットとワークロードを構成するハブを選択できます。

:::image type="content" source="media/cloud_edge-Manage.png" alt-text="スケール ユニットとワークロードの管理体験":::

トポロジーで使用できる 1 つ以上のスケール ユニットを追加するには、**スケール ユニットを追加** を選択します。 このプレビューでは、プレビュー プログラムの一部として受け取ったいずれかのプロモーション コードから配置したクラウドのスケール ユニットが表示されます。

<!-- > [!IMPORTANT]
> In the public preview, the Scale Unit Manager portal shows the cloud scale unit that you received as part of the preview program. Any edge scale unit that you created based on an LBD configuration can't be managed in the Scale Unit Manager portal yet. For configuration details, see [Deploy custom edge scale units on custom hardware using LBD](cloud-edge-edge-scale-units-lbd.md) -->

**定義されたワークロード** タブで、**ワークロードの作成** ボタンを使用して、倉庫管理または製造実行ワークロードをスケール ユニットの 1 つに追加します。 各ワークロードに対して、ワークロードによって所有されるプロセスのコンテキストを指定する必要があります。 倉庫管理ワークロードの場合、コンテキストは特定のサイトおよび法人の特定の倉庫になります。 製造実行ワークロードの場合、そのコンテキストは法人内の特定のサイトです。

:::image type="content" source="media/cloud_edge-DefineWorkload.png" alt-text="ワークロードの作成":::

> [!IMPORTANT]
> プレビューのスケール ユニット マネージャー ポータルでは、割り当て後にスケール ユニットからワークロードを削除したり、割り当てが行われた後でハブからスケール ユニットを割り当て解除したりすることはできません。 割り当てを削除する必要がある場合は、連絡担当者に連絡して、プレビュー プログラムの管理を依頼してください。

<!-- ### Create an edge scale unit using your custom on-premises hardware appliance

In the public preview, you can create on-premises edge scale units on your custom hardware using the LBD environments. For details, see [Deploy custom edge scale units on custom hardware using LBD](cloud-edge-edge-scale-units-lbd.md). -->
