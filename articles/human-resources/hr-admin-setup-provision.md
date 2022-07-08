---
title: Human Resources のプロビジョニング
description: この記事では、Microsoft Dynamics 365 Human Resources の新しい運用環境のプロビジョニングについて説明します。
author: twheeloc
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9d13372d8cc1f1f0f1407ea69bee4f98ae5065c2
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015349"
---
# <a name="provision-human-resources"></a>Human Resources のプロビジョニング

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



この記事では、Microsoft Dynamics 365 Human Resources の新しい運用環境のプロビジョニングについて説明します。 

## <a name="prerequisites"></a>必要条件

新しい運用環境のプロビジョニングを始める前に、次の前提条件が満たされている必要があります:

- クラウド ソリューション プロバイダー (CSP) またはエンタープライズ アーキテクチャ (EA) 契約を通して Human Resources を購入しました。 Human Resources サービス プランがすでに含まれている既存の Microsoft Dynamics 365 ライセンスがあり、この記事の手順を完了できない場合は、サポートにお問い合わせください。

- グローバル管理者は [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) にサインインし、新しい Human Resources プロジェクトを作成しました。 

## <a name="provision-a-human-resources-trial-environment"></a>Human Resources 試用環境のプロビジョニング

>[!NOTE]
> 2022 年 4 月から、Human Resources 試用環境は、スタンドアロン アプリケーションでは使用できません。 財務と運用アプリ内の Human Resources 機能の評価に関心を持つ潜在顧客は、30 日間の無料試用版をデモ データと共に使用できます。 Dynamics 365 Finance には、スタンドアロン アプリケーションのマージを通じて Finance インフラストラクチャに提供される Human Resources 機能が含められます。 詳細については、[HR 製品のマージによる顧客向け機能の統合](https://cloudblogs.microsoft.com/dynamics365/it/2021/09/15/merging-of-hr-offerings-brings-capabilities-together-for-customers) を参照してください。Dynamics 365 Finance の試用の詳細については、ステップ バイ ステップ [ガイド](../fin-ops-core/fin-ops/get-started/before-you-buy.md) を参照してください。 


最初のサンドボックス環境または運用環境をプロビジョニングする前に、[Human Resources 試用環境](https://go.microsoft.com/fwlink/p/?LinkId=2115962)をプロビジョニングして、Human Resources の機能を検証することができます。 試用環境には、安全にプログラムを活用するために使用する架空のデータが含まれます。 試用環境は要求したユーザーにより所有されていますが、人事管理のシステム管理経験を通じて他のユーザーも招待できます。 

試用版環境では、人事管理環境へのアクセス権がまだないユーザーの人事管理機能を評価できます。 試用環境をプロビジョニングする際に、認証されたユーザーが既に 1 つ以上の既存の人事管理環境へのアクセス権がある場合、ユーザーは既存の環境または環境のリストにリダイレクトされます。

試用環境は運用環境として使用するものではありません。 30 日間のトライアル期間に限定されています。 試用期限が切れると、環境とその中にあるすべてのデータが削除されて、復元できないことに注意してください。 環境をサンドボックスや運用環境に変換することはできません。 既存の環境の期限が切れた後、新しい試用環境に登録することができます。

Human Resources 試用環境を作成すると、テナントに Power Apps 試用環境も作成され、Human Resources 環境にリンクされます。 「TestDrive」という名前の Power Apps 環境には、Human Resources 環境と同じ試用期間があります。

> [!NOTE]
> 認証されたユーザーに Power Apps 試用環境を作成するアクセス許可が与えられていない場合、Human Resources 試用環境のプロビジョニングは失敗します。 ユーザーは、Power Platform 管理センターで、試用環境を作成できるユーザー グループに含まれている必要があります。 詳細については、[Power Platform 管理センターでの環境の作成と管理を行うユーザーの制御](/power-platform/admin/control-environment-creation)を参照してください。

## <a name="plan-human-resources-environments"></a>Human Resources の環境を計画する

最初に Human Resources を作成する前に、プロジェクトに必要な環境を慎重に計画する必要があります。 人事管理への基本的なサブスクリプションには、2 つの環境 (運用環境とサンドボックス環境) が含まれます。 プロジェクトの複雑さに応じて、プロジェクト活動の対応するべく、サンドボックス環境を追加購入する必要がある場合があります。 

追加環境に関する考慮事項:

- **データ移行** : サンドボックス環境をプロジェクト全体でテストに使用できるようにするために、データ移行活動に使用する追加環境が必要となる場合があります。 環境を追加することにより、テストと構成の活動が別の環境で同時に行われている間も、データ移行活動を継続することができます。
- **統合** : 統合を構成してテストする際に、追加の環境が必要となる可能性があります。 これには、Ceridian Dayforce または LinkedIn Talent Integrations などのネイティブ統合や、給与、申請者追跡システム、福利厚生システムやプロバイダなどのカスタム統合が含まれます。
- **トレーニング** : 新しいシステムを使用して従業員をトレーニングする際に、一連のトレーニング データを使用して別の環境が必要となる場合があります。 
- **複数フェーズのプロジェクト** : プロジェクトの最初の移動後に計画されているプロジェクト フェーズで構成、データ移行、テスト、その他の活動に対応するにあたって、追加の環境が必要となる場合があります。

 > [!IMPORTANT]
 > 環境を考慮する場合は、次の点をお勧めします:
 > - プロジェクト全体で運用環境を GOLD 構成の環境として使用します。 サンドボックス環境は、運用環境にコピーできないため重要です。 そのため、GO-LIVE 時には GOLD 環境が運用環境となり、この環境でカットオーバー活動を完了させます。</br></br>
 > - サンドボックスまたは別の環境を使用して、切り替えをを実行します。 これを実行するには、GOLD 構成を使用して運用環境を最新の情報に更新します。</br></br>
 > - GO-LIVE のカットオーバー時には、最終データを運用環境に移行するために必要な各データ パッケージを含む、詳細なカットオーバー チェックリストを作成します。</br></br>
 > - プロジェクト全体でサンドボックス環境を TEST 構成の環境として使用します。 追加の環境が必要な場合は、組織が追加費用で購入することができます。</br></br>

## <a name="create-an-lcs-project"></a>LCS プロジェクトの作成

Human Resources 環境を管理するために LCS を使用するには、最初に LCS プロジェクトを作成する必要があります。

1. Human Resources をサブスクライブするために使用したアカウントを使用して [LCS](https://lcs.dynamics.com/Logon/Index) にサインインします。

   > [!NOTE]
   > プロビジョニングを成功させるためには、Human Resources 環境のプロビジョニングに使用するアカウントが、Human Resources 環境に関連する Power Apps 環境の **システム管理者** または **システム カスタマイザー** のいずれかのロールに割り当てられている必要があります。 Power Platform でユーザーにセキュリティ ロールを割り当てる方法の詳細については、[リソースに対するユーザー セキュリティの構成](/power-platform/admin/database-security)を参照してください。

2. プラス記号 (**+**) を選択してプロジェクトを作成します。

3. 製品名、製品バージョンとして **Microsoft Dynamics 365 Human Resources** を選択します。

4. **Dynamics 365 Human Resources** 方法を選択します。

5. **作成** を選択します。

Human Resources を使い始める方法については、新しいプロジェクトで作成した **Human Resources** の方法を参照してくだい。 プロジェクトの作成が終了したら、Human Resources 環境をプロビジョニングするために次の手順を完了してください。

## <a name="provision-a-human-resources-project"></a>Human Resources プロジェクトのプロビジョニング

LCS プロジェクトを作成した後は、環境に Human Resources をプロビジョニングすることができます。

1. LCS プロジェクトでは、**人事管理アプリの管理** タイルを選択します。

2. これ環境が Human Resources のサンドボックス、または実稼働インスタンスであるかどうかを示します。 初期のプレビュー機能をサンドボックス インスタンスで使用することにより、早期のフィードバックおよびテストを行うことができます。
   
    > [!NOTE]
    > Human Resources インスタンス タイプは、一度設定した後で変更することはできません。 続行する前に、正しいインスタンス タイプが選択されていることを確認します。</br></br>
    > Human Resources のインスタンス タイプは、Power Apps 管理センターで設定された Microsoft Power Apps 環境のインスタンス タイプとは異なります。
    
3. Human Resources 試用環境で使用される同じデモ データ セットを環境に含める場合は、**デモ データを含む** オプションをオンにします。 デモ データは長期的なデモまたはトレーニング環境に有用ですが、運用環境で使用するものではありません。 初期展開時にこのオプションを選択する必要があります。 既存の配置を後で更新することはできません。

4. Human Resources は、Microsoft Power Apps の環境に常にプロビジョニングされていて、これにより Power Apps の統合および拡張機能が有効になります。 続行する前に、この記事の「Power Apps 環境の選択」セクションを参照してください。 まだ Power Apps 環境を持っていない場合は、LCS で環境の管理を選択するか、または Power Apps 管理センターに移動します。 次に、以下の手順に従って、[Power Apps 環境を作成します](/powerapps/administrator/create-environment)。

5. Human Resources をプロビジョニングする環境を選択します。

6. 使用条件に同意、および展開を開始するために **はい** を選択します。

   新しい環境は、左のナビゲーション ウィンドウにある環境の一覧に表示されます。 ただし、配置状態が **配置済み** に更新されるまでは、環境の使用を開始できません。 このプロセスには通常、数分間かかります。 プロビジョニング プロセスに失敗する場合は、サポートに連絡する必要があります。

7. 新しい環境を使用するために **Human Resources にログオンする** を選択します。

    > [!NOTE]
    > 最終要件をまだサインオフしていない場合、プロジェクトに Human Resources のテスト インスタンスを配置することができます。 サインオフするまで、ソリューションをテストするためにこのインスタンスを使用することができます。 テストのために新しい環境を使用する場合は、運用環境を作成するためにこの手順を繰り返す必要があります。

## <a name="select-a-power-apps-environment"></a>Power Apps 環境の選択

Power Apps ツールを使用して、人事管理データの使用を統合、拡張することができます。 環境スコープ、環境アクセス、および環境の作成および選択を含む、Power Apps 環境の詳細については、[Power Apps 環境の発表](https://powerapps.microsoft.com/blog/powerapps-environments/) をご覧ください。 

Human Resources を配置する Power Apps 環境を決定する際には、次のガイダンスを参考にしてください。 

1. LCS で、**環境の管理** を選択します。 既存の環境の表示および新しい環境の作成ができる Power Apps 管理者センターに移動することも可能です。

2. 1 つの Human Resources 環境は、1 つの Power Apps 環境にマップされます。

3. Power Apps 環境には、対応する Power Apps、Power Automate、および Dataverse アプリケーションと共に、Human Resources が含まれています。 Power Apps 環境を削除すると、その中のアプリも削除されます。 Human Resources 環境をプロビジョニングする場合、**試用** または **実稼働** 環境のいずれかをプロビジョニングできます。 環境の使用方法に基づいて環境のタイプを選択します。 

4. サンドボックス、UAT、または生産などのデータの統合およびテスト戦略を考慮する必要があります。 Power Apps 環境にマッピングされている Human Resources 環境を後から変更することは容易ではないため、実装へのさまざまな影響について考慮することを推奨します。

5. 次の Power Apps 環境は Human Resources には使用できません。 これらは、LCS 内の選択リストからフィルタ処理されます：
 
    - **既定の Power Apps 環境** - 各テナントは既定の Power Apps 環境で自動的にプロビジョニングされますが、Human Resources での使用については推奨しません。 すべてのテナント ユーザーが Power Apps 環境にアクセスでき、テストや Power Apps、Power Automate 統合の際に、運用データの意図しない破損につながる可能性があります。
   
    - **評価版環境** - これらの環境には、有効期限が設定されています。 有効期限が切れると、環境とその中に含まれる Human Resources インスタンスが自動的に削除されます。
   
    - **サポート対象外の地域** - 環境はサポートされている地域に存在している必要があります。 詳細については、[サポートされている地域](hr-admin-setup-provision.md#supported-geographies) を参照してください。

6. 人事データを Power Apps 環境に統合するデュアル書き込み機能は、その環境で **Dynamics 365 アプリを有効にする** オプションが選択されている場合にのみ使用できます。 デュアル書き込みの詳細については、[デュアル書き込みのホームページ](../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)を参照してください。

    > [!NOTE]
    > **Dynamics 365アプリケーションを有効にする** オプションは、Power Apps 環境の作成時に選択する必要があります。 プロビジョニング時にこのオプションが選択されていない場合、デュアル書き込みを使用して Dynamics 365 Human Resources 環境と Power Apps 環境の間でデータを統合したり、Dynamics 365 Sales や Field Service などのDynamics 365 アプリを環境にインストールしたりすることができません。 このオプションは、元に戻すことはできません。 
    > -  Human Resources は、Human Resources を配置した後にリンクされた Dataverse インスタンスの変更はサポートしません。 </br></br>
    > 詳細については、Power Platform のドキュメント サイト、 [新しい環境を構築する際の重要な注意点](/power-platform/admin/create-environment#some-important-considerations-when-creating-a-new-environment)を参照してください。  

7. 使用する正しい環境の決定後、プロビジョニング プロセスを続行できます。 

### <a name="supported-geographies"></a>サポートされている地域

Human Resources では現在、次の場所がサポートされます。

- 米国
- ヨーロッパ
- 英国
- オーストラリア
- カナダ
- アジア 

Human Resources 環境を作成するときに、Human Resources 環境に関連付ける Power Apps 環境を選択します。 Human Resources 環境は、選択した Power Apps 環境と同じ Azure 地域にプロビジョニングされます。 Human Resources 環境に関連する Power Apps 環境を作成する際に、地理的な場所を選択することで、Human Resources 環境とデータベースが物理的に存在する場所を選択することができます。

環境がプロビジョニングされる Azure *地域* は選択できますが、特定の Azure *リージョン* は選択できません。 オートメーションでは、負荷分散とパフォーマンスを最適化するために、環境が作成される地域内の特定の地域を決定します。 Azure 地域とリージョンについては、[Azure 地域](https://azure.microsoft.com/global-infrastructure/geographies)についてのドキュメントを参照してください。

Human Resources 環境のデータは常に、Human Resources 環境が作成された Azure 地域内に含まれます。 ただし、常に同じ Azure リージョン内に含まれるわけではありません。 ディザスター リカバリーを目的として、データは主要な Azure リージョンと地域内のフェールオーバー リージョンの両方で複製されます。

 > [!NOTE]
 > Human Resources 環境を 1 つの Azure リージョンから別のリージョンに移行することはサポートされていません。

## <a name="grant-access-to-the-environment"></a>環境へのアクセスを付与

既定では、環境を作成したグローバル管理者がそこにアクセスできます。 追加のアプリケーション ユーザーに対するアクセス権を明示的に付与する必要があります。 Human Resources 環境では、ユーザーを追加し、適切な役割を割り当てる必要があります。 詳細については、[新規ユーザーの作成](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) および [ユーザーのセキュリティ ロールへの割り当て](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles) を参照してください。 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
