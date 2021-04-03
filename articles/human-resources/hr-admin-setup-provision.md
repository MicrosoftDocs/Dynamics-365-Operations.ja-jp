---
title: Human Resources のプロビジョニング
description: この記事では、Microsoft Dynamics 365 Human Resources の新しい実稼動環境のプロビジョニングのプロセスについて説明します。
author: andreabichsel
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 43aacf454d6a2c9eb8cda5bb54a2bf8e8965070d
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466883"
---
# <a name="provision-human-resources"></a>Human Resources のプロビジョニング

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

この記事では、Microsoft Dynamics 365 Human Resources の新しい実稼動環境のプロビジョニングのプロセスについて説明します。 この記事では、Human Resources をクラウド ソリューション プロバイダー (CSP) またはエンタープライズ アーキテクチャ (EA) 契約を通して購入したことを前提にしています。 Human Resources サービス プランがすでに含まれている既存の Microsoft Dynamics 365 ライセンスがあり、この記事の手順を完了できない場合は、サポートにお問い合わせください。

始めに、グローバル管理者は [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) にサインインし、新しい Human Resources プロジェクトを作成します。 ライセンスの問題で Human Resources プロビジョニングが妨げられない限り、サポートまたは Dynamics サービス エンジニアリング (DSE) の担当者に問い合わせる必要はありません。

## <a name="plan-human-resources-environments"></a>Human Resources の環境を計画する

最初に Human Resources を作成する前に、プロジェクトに必要な環境を慎重に計画する必要があります。 人事管理への基本的なサブスクリプションには、2 つの環境 (運用環境とサンドボックス環境) が含まれます。 プロジェクトの複雑さに応じて、プロジェクト活動の対応するべく、サンドボックス環境を追加購入する必要がある場合があります。 

追加の環境で考慮すべき点には、以下のようなものがありますが、これに限定されるものではありません。

- **データ移行** : サンドボックス環境をプロジェクト全体でテストに使用できるようにするために、データ移行活動に使用する追加環境が必要となる場合があります。 環境を追加することにより、テストと構成の活動が別の環境で同時に行われている間も、データ移行活動を継続することができます。
- **統合** : 統合を構成してテストする際に、追加の環境が必要となる可能性があります。 これには、Ceridian Dayforce LinkedIn Talent Integrations などのネイティブ統合や、給与、申請者追跡システム、福利厚生システムやプロバイダなどのカスタム統合が含まれます。
- **トレーニング** : 新しいシステムを使用して従業員をトレーニングする際に、一連のトレーニング データを使用して別の環境が必要となる場合があります。 
- **複数フェーズのプロジェクト** : プロジェクトの最初の移動後に計画されているプロジェクト フェーズで構成、データ移行、テスト、その他の活動に対応するにあたって、追加の環境が必要となる場合があります。

 > [!IMPORTANT]
 > 運用環境は、プロジェクト全体で GOLD 構成の環境として使用することをお勧めします。 サンドボックス環境は、運用環境にコピーできないため重要です。 そのため、GO-LIVE 時には GOLD 環境が運用環境となり、この環境でカットオーバー活動を完了させます。</br></br>
 > 移動前に、ひとつ以上の環境を使用して切り替えを実行しておくことをお勧めします。 これを実行するには、GOLD 構成を使用して運用環境を最新の情報に更新します。</br></br>
 > GO-LIVE のカットオーバー時には、最終データを運用環境に移行するために必要な各データ パッケージを含む、詳細なカットオーバー チェックリストを作成しておくことをお勧めします。</br></br>
 > また、プロジェクト全体でサンドボックス環境をテスト環境として使用することをお勧めします。 追加の環境が必要な場合は、組織が追加費用で購入することができます。</br></br>

## <a name="create-an-lcs-project"></a>LCS プロジェクトの作成

Human Resources 環境を管理するために LCS を使用するには、最初に LCS プロジェクトを作成する必要があります。

1. Human Resources をサブスクライブするために使用したアカウントを使用して [LCS](https://lcs.dynamics.com/Logon/Index) にサインインします。

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
    
3. Human Resources テスト ドライブ エクスペリエンスで使用される同じデモ データ セットを環境に含める場合は、**デモ データを含む** オプションをオンにします。 デモ データは長期的なデモまたはトレーニング環境に有用ですが、稼動環境で使用するものではありません。 初期展開時にこのオプションを選択する必要があります。 既存の配置を後で更新することはできません。

4. Human Resources は、Microsoft Power Apps の環境に常にプロビジョニングされていて、これにより Power Apps の統合および拡張機能が有効になります。 続行する前に、この記事の「Power Apps 環境の選択」セクションを参照してください。 まだ Power Apps 環境を持っていない場合は、LCS で環境の管理を選択するか、または Power Apps 管理センターに移動します。 次に、以下の手順に従って、[Power Apps 環境を作成します](https://docs.microsoft.com/powerapps/administrator/create-environment)。

5. Human Resources をプロビジョニングする環境を選択します。

6. 使用条件に同意、および展開を開始するために **はい** を選択します。

   新しい環境は、左のナビゲーション ウィンドウにある環境の一覧に表示されます。 ただし、配置状態が **配置済み** に更新されるまでは、環境の使用を開始できません。 このプロセスには通常、数分間かかります。 プロビジョニング プロセスに失敗する場合は、サポートに連絡する必要があります。

7. 新しい環境を使用するために **Human Resources にログオンする** を選択します。

    > [!NOTE]
    > 最終要件をまだサインオフしていない場合、プロジェクトに Human Resources のテスト インスタンスを配置することができます。 サインオフするまで、ソリューションをテストするためにこのインスタンスを使用することができます。 テストのために新しい環境を使用する場合は、実稼動環境を作成するためにこの手順を繰り返す必要があります。

    > この場合は、60日間の無料の [Human Resources 試用環境](https://go.microsoft.com/fwlink/p/?LinkId=2115962) を利用をご検討ください。 試用環境は要求したユーザーにより所有されていますが、人事管理のシステム管理経験を通じて他のユーザーも招待できます。 試用環境には、安全にプログラムを活用するために使用する架空のデータが含まれます。 これらは実稼動環境として使用するものではありません。 試用環境が 60 日後に期限が切れると、その中にあるすべてのデータが削除され復元できないことに注意してください。 既存の環境の期限が切れた後、新しい試用環境に登録することができます。

## <a name="select-a-power-apps-environment"></a>Power Apps 環境の選択

Power Apps ツールを使用して、人事管理データの使用を統合、拡張することができます。 環境スコープ、環境アクセス、および環境の作成および選択を含む、Power Apps 環境の詳細については、[Power Apps 環境の発表](https://powerapps.microsoft.com/blog/powerapps-environments/) をご覧ください。 

Human Resources を配置する Power Apps 環境を決定する際には、次のガイダンスを参考にしてください。 

1. LCS で、**環境の管理** を選択します。 既存の環境の表示および新しい環境の作成ができる Power Apps 管理者センターに移動することも可能です。

2. 1 つの Human Resources 環境は、1 つの Power Apps 環境にマップされます。

3. Power Apps 環境には、対応する Power Apps、Power Automate、および Dataverse アプリケーションと共に、Human Resources が含まれています。 Power Apps 環境を削除すると、その中のアプリも削除されます。 Human Resources 環境をプロビジョニングする場合、**試用** または **実稼働** 環境のいずれかをプロビジョニングできます。 環境の使用方法に基づいて環境のタイプを選択します。 

4. サンドボックス、UAT、または生産などのデータの統合およびテスト戦略を考慮する必要があります。 Power Apps 環境にマッピングされている Human Resources 環境を後から変更することは容易ではないため、実装へのさまざまな影響について考慮することを推奨します。

5. 次の Power Apps 環境を Human Resources に使用することはできません。 これらは、LCS 内の選択リストからフィルタ処理されます：
 
    - **既定の Power Apps 環境** - 各テナントは既定の Power Apps 環境で自動的にプロビジョニングされますが、Human Resources での使用については推奨しません。 すべてのテナント ユーザーが Power Apps 環境にアクセスでき、テストや Power Apps、Power Automate 統合の際に、本番データの意図しない破損につながる可能性があります。
   
    - **評価版環境** - これらの環境には、有効期限が設定されています。 有効期限が切れると、環境とその中に含まれる Human Resources インスタンスが自動的に削除されます。
   
    - **対応していない地域** - 現在の Human Resources は、次の地域でのみ対応しています：米国、ヨーロッパ、英国、オーストラリア、カナダ、アジア。

    > [!NOTE]
    > Human Resources 環境は、Power Apps 環境がプロビジョニングされたのと同じ領域でプロビジョニングされます。 Human Resources 環境の別の領域への移行には対応していません。

6. 使用する正しい環境の決定後、プロビジョニング プロセスを続行できます。 
 
## <a name="grant-access-to-the-environment"></a>環境へのアクセスを付与

既定では、環境を作成したグローバル管理者がそこにアクセスできます。 追加のアプリケーション ユーザーに対するアクセス権を明示的に付与する必要があります。 Human Resources 環境では、ユーザーを追加し、適切な役割を割り当てる必要があります。 Human Resources を展開するグローバル管理者は、初期化を完了して、他のテナント ユーザーのアクセスを有効にするため、Attract および Onboard の両方も起動する必要があります。 これが発生するまで、他のユーザーは Attract および Onboard にアクセスすることはできませんし、アクセス違反エラーが発生します。 詳細については、[新規ユーザーの作成](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) および [ユーザーのセキュリティ ロールへの割り当て](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles) を参照してください。 


[!INCLUDE[footer-include](../includes/footer-banner.md)]