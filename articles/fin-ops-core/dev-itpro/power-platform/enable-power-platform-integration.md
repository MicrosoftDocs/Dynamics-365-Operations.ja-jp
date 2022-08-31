---
title: Microsoft Power Platform 統合を有効にする
description: この記事では財務と運用アプリと Dataverse を Microsoft Dynamics Lifecycle Services (LCS) に使用して Microsoft Power Platform 統合を有効にする方法について説明します。
author: jaredha
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: intro-internal
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-10-13
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 7ed5217791d8c478e2c64820b63bed75d33972b0
ms.sourcegitcommit: e14648b01549bdc17998ffdef6cde273d4e78560
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/09/2022
ms.locfileid: "9242904"
---
# <a name="enable-the-microsoft-power-platform-integration"></a>Microsoft Power Platform 統合を有効にする

[!include[banner](../includes/banner.md)]

財務と運用アプリと Microsoft Power Platform の統合は Microsoft Dynamics Lifecycle Services (LCS) で新しい財務と運用アプリ環境を作成する時に有効にできます。 または、既存の財務と運用アプリ環境で Microsoft Power Platform を有効にすることもできます。 どちらのオプションでも、セットアップの前提条件を満たす必要があります。

Power Platform 統合では、次のタスクを完了することができます。

* 自動的に作成される新しい Power Platform 環境を使用して、アプリケーションとフローを作成します。
* 仮想テーブル、ビジネス イベント、および二重書き込み機能を使用して、財務と運用アプリのデータを Dataverse プラットフォームと統合します。
* 他の Dynamics 365 アプリケーションを財務と運用アプリにインストールして接続します。
* アドインをインストールし、財務と運用アプリに接続します。

## <a name="initial-power-platform-environment"></a>初期 Power Platform 環境

既定では、LCS によって管理されるすべての財務と運用アプリの環境 (サンドボックス環境および運用環境) は、初期 Power Platform 環境を、Dataverse **なし** で受け取ります。 次の図に示すように、この環境は財務と運用環境にリンクされています。 リレーションシップは一対一です。 時間の経過と共に、財務と運用アプリは Power Platform 管理センターのこの場所に移行されます。 Power Platform 管理センターの環境詳細ページにある財務と運用アプリの URL を参照して、Power Platform 管理センターの環境が LCS にリンクされているかどうかを判断します。

![Power Platform 管理センターの Power Platform 環境は、LCS の財務と運用の環境と同じ名前で作成されます。 財務と運用の URL には、財務と運用のインスタンスの URL が入力されます。](media/LinkedPowerPlatformEnvironment.png)

LCS の環境に接続されている Power Platform 環境により、財務と運用アプリの顧客は Microsoft Power Platform を利用できます。 この Power Platform 環境は、削除またはリセットすることはできず、Dataverse データベースを手動で Power Platform 管理センターに追加することもできません。 Dataverse を追加して Microsoft Power Platform 統合機能を完全に有効にするには、この記事の[既存の Power Platform 環境との統合を有効にする](#connect-to-existing-dataverse) セクションの手順に従ってください。

または、財務と運用環境に接続する Dataverse を備えた Power Platform 環境が既に組織にある場合があります。 既存の Dataverse インスタンスを再利用するには、[既存の Power Platform 環境との統合を有効にする](#connect-to-existing-dataverse)の手順に従ってください。 この場合、財務と運用環境の作成時に作成された最初の Power Platform 環境は切断され、財務と運用アプリの URL は表示されなくなります。 その時点で、初期環境を削除したり、別の目的に使用したりすることができます。

## <a name="licensing-and-capacity-considerations"></a>ライセンスと容量に関する考慮事項

Dynamics 365 Finance または Dynamics 365 Supply Chain Management などの財務と運用アプリのライセンスを購入すると、テナントはさらに 10 ギガバイト (GB) の Dataverse データベース容量を利用できます。 さらに、Power Portal 管理センターの次の図に示すように、購入した各ユーザー ライセンスについて、データベースの容量が増量されます。

![Power Platform 管理センターの容量ビュー。](media/PPI-Capacity.png)

ライセンスを同じように購入すると、LCS の 1 つのセルフサービス サンドボックス環境と運用環境を利用できるようになります。 このため、すべての財務と運用アプリの環境に対して初期 Power Platform 環境が自動的に作成されます。 Power Platform 管理センターのすべての初期環境には、Dataverse がありません。 そのため、Power Apps を使用して作成されたアプリと、Power Automate を使用して作成されたフローをプロビジョニングするために、わずか 1 GB のデータベース容量しか使用されません。 Power Platform 統合を設定すると、Dataverse データベースが同じ環境に追加されます。 このデータベースは多くの場合、3 GB 以上消費します。

LCS で使用するために顧客が購入する追加のアドオン サンドボックス環境では、追加の Dataverse データベース容量を利用 **できません**。 Power Platform 統合機能を必要とする顧客は、アドオン Dataverse データベース ストレージを購入する必要があります。 Power Platform 管理センターの容量を管理する方法の詳細については、[ストレージ領域の解放](/power-platform/admin/free-storage-space)を参照してください。

## <a name="provisioning-templates"></a>プロビジョニング テンプレート

この記事で説明するシナリオのいくつかでは、Dataverse を使用して新しい Power Platform 環境を作成します。 新しいインスタンスに必要なすべてのアプリケーションをすばやく追加できるように、それらをまとめた複数のプロビジョニング テンプレートが用意されています。 次のテーブルは、それぞれのテンプレートに関する詳細を示します。

| テンプレート名 | Description | 含まれているアプリケーション |
|---------------|-------------|---------------|
| Dynamics 365 標準 | この基本テンプレートは、ビジネス イベント、仮想テーブル、二重書き込み機能、およびアドイン サポート用のすべてのプラットフォーム コンポーネントを準備します。 このテンプレートが選択されている場合は、二重書き込みは有効にならず、データも自動的に同期されません。 特定のテンプレートが必要ない場合、このテンプレートを選択します。 | MicrosoftOperationsVEAnchor、DualWriteCoreAnchor、MsDynCE_CRMHub、MsDyn_FnOIntegrationMDLApp_Anchor |
| Dynamics 365 標準 (二重書き込み付き) | このテンプレートは **Dynamics 365 標準** と同じですが、二重書き込みに必要なすべてのアプリケーションが含まれているので、環境を配置した後にこの機能をすぐに有効にできます。 | MicrosoftOperationsVEAnchor、DualWriteCoreAnchor、MsDynCE_CRMHub、MsDyn_FnOIntegrationMDLApp_Anchor、MsDyn_DualWriteAppCoreAnchor |
| Project Operations | このテンプレートは Dynamics 365 Project Operations シナリオに固有です。 テナントが Project Operations のライセンスと資格を持っている場合にのみ利用できます。 | MicrosoftOperationsVEAnchor、Dynamics365FinanceAndOperationsAnchor、ProjectOperations_Anchor |

## <a name="prerequisites-for-setting-up-the-microsoft-power-platform-integration"></a>Microsoft Power Platform 統合を設定するための前提条件

次のリストは、Microsoft Power Platform 統合を設定するための前提条件を示しています。

- テナントで少なくとも 1 GB の Microsoft Power Platform データベース ストレージ容量スペースが使用可能であることを確認してください。 この領域が利用できない場合、設定は失敗します。 [Power Platform 管理センター](https://admin.powerplatform.microsoft.com/resources/capacity)で、容量を表示できます。 

- 財務と運用アプリ環境管理者を識別します。 **環境の詳細** セクションにて、情報を確認できます。

    ![環境の詳細セクションの環境管理者情報。](media/EnvironmentDetails.png)

- Microsoft Power Platform 環境のガバナンス ポリシーを検証します。 この検証を行うには、**グローバル管理者** ロールまたは **Power Platform 管理者** ロールのいずれかが必要です。

    1. [Power Platform 管理センター](https://admin.powerplatform.microsoft.com) にサイン インします。
    2. ページの右上隅にある **設定** を選択して、**Power Platform 設定** ウィンドウを開きます。

        ![Power Platform 設定ウィンドウ。](media/PowerPlatformSettings.png)

- Microsoft Power Platform 環境の作成を **全員に許可しない** 組織の場合、使用中の環境の財務と運用アプリ環境管理者のアカウントを Azure Active Directory (Azure AD) 内の次の管理ロールのいずれかに追加する必要があります。 この変更を行うには、**グローバル管理者** ロールに割り当てられている必要があります。

    - Dynamics 365 サービス管理者
    - Power Platform 管理者


    > [!NOTE]
    > 上記のロールは、財務と運用アプリ環境管理者アカウントに必要なものより多くのアクセス許可を提供する場合があります。 したがって、この統合にさらに制限されたロールが最終的に Azure AD に追加されます。 新しいロールに上記のロールは必要ではありません。 最小限の特権の管理者を維持する場合、一時的に上記のロールの 1 つを付与できます。 Microsoft Power Platform 統合が設定された後、そのロールを削除します。

- Microsoft Power Platform 環境を作成するすべてのユーザーはライセンスが必要です。 Microsoft 365 管理センターを使用して **Dynamics 365 Unified Operations Plan** ライセンス、または **AX エンタープライズ** ライセンス、または **Dynamics 365 Finance** などのアプリケーション固有のライセンスを財務と運用アプリ環境の管理者アカウントに適用する必要があります。

## <a name="enable-integration-during-environment-deployment"></a><a name="enable-during-deploy"></a> 環境の配置中に統合を有効にする

> [!IMPORTANT]
> Power Platform 統合を有効にすると、前に説明した初期 Power Platform 環境に、新しい Dataverse データベースが追加されます。 組織に、財務と運用環境に接続する Dataverse インスタンスが既にある場合は、LCS での環境作成中に Power Platform 統合を **有効にしません**。 財務と運用環境の展開が完了すると、**設定** ボタンを使用して既存の Power Platform 環境に接続できるようになります。
>
> Power Platform 統合は **元に戻すことはできません**。また、リンクを変更または削除することもできません。 設定の一部として、財務と運用環境を Power Platform 環境に接続します。 仮想エンティティ、ビジネス イベント、および二重書き込みなどのランタイム機能はすべて、この接続に依存します。 したがって、財務と運用環境を削除するまで削除することはできません。 この動作は、Microsoft からのサービス更新プログラムを適用するときの動作に似ています。 このアクションをやり直す唯一の方法は、環境を再配置することです。

LCS に新しい財務と運用アプリ環境を設定する際、展開ウィザードには値を設定することができる複数のセクションがあります。 それらセクションの 1 つが **Power Platform 統合** という名前です 。

![配置ウィザードの Power Platform 統合セクション。](media/powerplat_integration_step0.png)

**Power Platform 統合** セクションを構成するには、次の手順に従います。

1. **Power Platform 環境の構成** オプションを **はい** に設定します。 複数の追加設定が使用可能になります。
2. **Power Platform テンプレート** フィールドで、テンプレートを選択します。 詳細については、この記事の[プロビジョニング テンプレート](#provisioning-templates) セクションを参照してください。
3. DevTest またはクラウド ホスト環境を配置する場合、**環境の種類** フィールドが使用可能です。 そこで、作成およびリンクされる Dataverse インスタンスのタイプを選択できます。 それ以外の場合、既定では、環境の種類はレベル 2 から 5 の承認テスト環境の場合は **サンドボックス** に、運用環境の場合は **運用** に設定されます。
4. **同意** を選択して、統合の使用条件に同意することを示します。

> [!IMPORTANT]
> 財務と運用アプリ環境に作成およびリンクされる Dataverse インスタンスの **言語** および **通貨** の値は、Azure AD テナントの物理的なアドレスに基づいて自動的に決定されます。 たとえば、住所が米国ワシントン州 Redmond である場合、既定では言語は英語で、通貨は米ドル (USD) になります。
>
> 既定値とは異なる値が必要な場合は、自分たちの仕様に対して、Dataverse で Power Platform 環境を作成できます。  財務と運用の作成中に Power Platform 統合を有効にしない限り、LCS の財務と運用環境から既存の環境にリンクできます。  既存の Dataverse インスタンスへのリンクは、以前に他の Dataverse インスタンスに関連付けされていない既存の財務と運用アプリ環境からのみ使用できます。

## <a name="enable-integration-after-environment-deployment"></a><a name="enable-after-deploy"></a> 環境の配置後に統合を有効にする

多くの場合、財務と運用アプリを配置した後に Power Platform 統合を有効にすることもできます。 たとえば、最初に財務と運用アプリを使用して、新しい Dataverse インスタンスを使用する場合や、次のセクションで説明するように、既存の Dataverse インスタンスに接続することを選択した場合です。

> [!IMPORTANT]
> Power Platform 統合は **元に戻すことはできません**。また、リンクを変更または削除することもできません。 設定の一部として、財務と運用環境を Power Platform 環境に接続します。 仮想エンティティ、ビジネス イベント、および二重書き込みなどのランタイム機能はすべて、この接続に依存します。 したがって、財務と運用環境を削除するまで削除することはできません。 この動作は、Microsoft からのサービス更新プログラムを適用するときの動作に似ています。 このアクションをやり直す唯一の方法は、環境を再配置することです。

1. 財務と運用アプリ環境が LCS を介して配置された後、LCS の **環境詳細** ページが開きます。
2. **Power Platform 統合** セクションで、**設定** を選択します。 *既存の Dataverse 組織に接続する場合は、この記事の次のセクションを参照してください。*

    ![Power Platform 統合セクションの設定ボタン。](media/powerplat_integration_step1.png) 

3. **Power Platform 環境設定** ダイアログ ボックスで契約条件に同意し、**設定** を選択します。

    > [!NOTE]
    > これで Dataverse ベースの環境が Power Platform 管理センターに準備されます。 この環境には通常 1 GB のデータベース ストレージ容量が必要で、財務と運用アプリ環境と同じ名前になります。 二重書き込みプラットフォーム レベルのコンポーネントはインストールされますが、二重書き込みアプリケーション コンポーネントは設定または有効化されません。 それらのアクションは別個のものです。

4. Microsoft Power Platform 環境が準備されているというメッセージが表示された場合は、**OK** を選択します。

    **環境詳細** ページの **Power Platform 統合** セクションに、Microsoft Power Platform 環境が準備されているというメッセージが表示されます。

5. 数分後、**環境の詳細** ページが更新されます。
6. **Power Platform 統合** セクションにおいて、**ステータス** フィールドの値が **環境設定が進行中** であることに注意してください。

    通常、設定は 60分 から 90分かかります。

    Dataverse インスタンスが準備された後、**新しいアドインのインストール** と **二重書き込みアプリケーション** ボタンが **Power Platform 統合** セクションで利用できるようになります。

    ![新しいアドイン ボタンをインストールします。](media/InstallANewAddIn.png)

    ![二重書き込みアプリケーション ボタン。](media/powerplat_integration_dwApp_button.png)

> [!IMPORTANT]
> 財務と運用アプリ環境に作成およびリンクされる Dataverse インスタンスの **言語** および **通貨** の値は、Azure AD テナントの物理的なアドレスに基づいて自動的に決定されます。 たとえば、住所が米国ワシントン州 Redmond である場合、既定では言語は英語で、通貨は USD になります。
>
> 既定値とは異なる値が必要な場合は、仕様を満たす新しい Power Platform 環境を手動で作成します。 次に、次のセクションの手順に従って、既存の Dataverse インスタンスを LCS を介して接続します。

設定が完了した後にアクションを取り消す唯一の方法は、LCS の環境を削除することです。 他の環境への再リンクやリンクはサポートされていません。

### <a name="enable-integration-with-an-existing-power-platform-environment"></a><a name="connect-to-existing-dataverse"></a>既存の Power Platform 環境との統合を有効にする

財務と運用環境に接続する Dataverse インスタンスが既にある場合は、以前に配置された財務と運用環境から Power Platform 統合の設定中に接続できます。 ただし、新しい財務と運用環境を配置する場合は、このオプションは使用できません。

![既存の Power Platform 環境に接続する。](media/PPI-ConnectToExisting.png)

Power Platform 環境 ID を取得するには、Power Platform 管理センターの環境にアクセスしてブラウザーのアドレス バーから環境 ID をコピーします。

![ブラウザーのアドレス バーから環境 ID を取得します。](media/PPI-ExistingEnvironmentID.png)

統合プロセス中に、Microsoft は **Dynamics 365 標準** のプロビジョニング テンプレートにパッケージを適用します。 他のテンプレートからパッケージを作成する必要がある場合は、手動でインストールする必要があります。 詳細については、この記事の[プロビジョニング テンプレート](#provisioning-templates) セクションを参照してください。

既に Power Platform 環境または他の Dynamics 365 アプリを使用していて、そのエコシステムに財務と運用アプリを追加したい顧客には、既存の Dataverse インスタンスを利用することが最も便利です。 統合については、初期環境の新しい Dataverse データベースに対して前に説明したのと同じ設定プロセスを使用します。 設定完了後に統合を取り消す唯一の方法は、LCS の環境を削除することです。 他の環境への再リンクやリンクはサポートされていません。

#### <a name="validations-for-bringing-your-existing-power-platform-environment"></a>既存の Power Platform 環境の使用に関する検証

既存の Power Platform 環境を接続する場合は、次の検証に合格する必要があります。 それ以外の場合、要求は続行できません。

1. Dataverse を Power Platform 環境に配置する場合は、**D365 アプリを有効にする** オプションを有効にする必要があります。 このタイプの Dataverse 展開は、財務と運用アプリへの接続を含め、Dynamics 365 アプリをサポートする唯一のタイプです。
2. Power Platform 環境は、財務と運用アプリと同じ地域にある必要があります。 たとえば、LCS では **West US 2** などの Azure リージョンが表示される場合があります。 Microsoft Power Platform では、この環境は **北米** に配置する必要があります。 パフォーマンスとデータ所在地の理由から、この要件が設定されています。
3. Power Platform 統合設定を実行している LCS のユーザーは、Dataverse 環境の管理者である必要があります。また、該当する Finance、Supply Chain Management、または Commerce ライセンスが割り当てられている必要があります。

### <a name="environments-that-already-use-dual-write-virtual-tables-business-events-or-add-ins-before-power-platform-integration-is-enabled"></a>Power Platform 統合を有効にする前に、二重書き込み、仮想テーブル、ビジネス イベント、またはアドインを既に使用している環境

Power Platform 統合機能が存在する前に二重書き込み、仮想テーブル、またはビジネス イベントを有効にしている場合は、LCS にない Dataverse を自動的に作成しています。

Microsoft Power Platform 統合が自動的に有効になったことを、LCS の財務と運用アプリ環境の **環境詳細** ページの **Power Platform 統合** セクションを表示することで確認できます。 統合が正常に有効化された場合、**環境名** フィールドには統合された Microsoft Power Platform 環境の名前が表示され、**状態** フィールドは **設定は正常に完了しました** に設定されます。

> [!NOTE]
> 単一の Microsoft Power Platform 環境にすでに接続されており、ビジネス イベント機能をすでに使用している財務と運用アプリ環境に対しては Microsoft Power Platform 統合は自動的に有効になります。 ただし、これらの環境では、リリース 10.0.22 以降の新しいビジネス イベントおよびデータ イベント機能を使用できなくなります。 これらの環境で既に使用されているビジネス イベントのエンドポイントは、バージョン 10.0.23 の Dataverse プラットフォームに移行されます。 その時点で、新しいビジネス イベントとデータ イベントの機能が環境で利用可能になります。 それまでは、ビジネス イベントは現在の環境で構成されている通りに引き続き機能します。
> 
> これらの環境で移行が完了するまで遅延される新しいビジネス イベントおよびデータ イベント機能の詳細については、2021 年リリース サイクル 2 プランの [Dataverse の財務と運用ビジネス イベント](/dynamics365-release-plan/2021wave2/finance-operations/finance-operations-crossapp-capabilities/new-scenarios-enabled-power-platform-convergence#finance-and-operations-business-events-in-dataverse)および [Dataverse の財務と運用 CUD イベント](/dynamics365-release-plan/2021wave2/finance-operations/finance-operations-crossapp-capabilities/new-scenarios-enabled-power-platform-convergence#finance-and-operations-cud-events-in-dataverse)を参照してください。 


## <a name="troubleshooting-the-setup"></a>設定のトラブルシューティング

設定は、Dataverse ベースの環境を配置するさまざまなステージで失敗する可能性があります。

設定が失敗するたびに、エラー メッセージが表示されます。 次の図は、二重書き込み設定に失敗した場合のエラー メッセージの例を示しています。

![二重書き込み設定に失敗した場合のエラー メッセージ。](media/Error.png)

エラー メッセージに基づいて、ライセンスや容量の問題への対処が必要となる場合があります。 これらの問題が修正されたら、LCS の **環境の詳細** ページの **Power Platform 統合** セクションにある **再開** を選択して設定を完了することができます。

## <a name="enable-the-integration-for-cloud-hosted-development-environments"></a>クラウド ホスト開発環境の統合を有効にする

このセクションの手順を完了することで、クラウド ホスト開発環境の Microsoft Power Platform 統合を手動で有効にできます。 クラウド開発環境の配置方法の詳細については、[開発環境の配置とアクセス](../dev-tools/access-instances.md)を参照してください。

### <a name="register-an-application-in-the-azure-portal"></a>Azure ポータルにアプリケーションを登録する

> [!IMPORTANT]
> Azure AD アプリケーションは、財務と運用アプリと同じテナントに作成する必要があります。

1. [Azure ポータル](https://portal.azure.com)を開きます。
2. **Azure Active Directory \> アプリの登録** に移動します。
3. **新しいアプリケーションの登録** を選択し、以下の情報を入力します。

    - **名前** – 一意の名前を入力します。
    - **勘定タイプ** – **任意の組織ディレクトリでのアカウント (任意の Azure AD ディレクトリ - マルチテナント)**。
    - **リダイレクト URI** – このフィールドは空白のままにします。

4. **登録** を選択します。
5. **アプリケーション (クライアント) ID** の値をメモします。 後に、この値を使用します。
6. アプリケーションの対称キーを作成します。

    1. 新しいアプリ登録の左側のナビゲーション ウィンドウで、**証明書とシークレット** を選択します。
    2. **新しいクライアント シークレット** を選択します。
    3. 説明と有効期限を入力します。
    4. **保存** を選択します。
    5. 作成された **値** フィールドにキーをコピーします。 このキー値は後で必要になります。
 
### <a name="add-the-azure-ad-application-as-a-microsoft-power-platform-user"></a>Microsoft Power Platform ユーザーとして Azure AD アプリケーションを追加する

Azure AD アプリケーションを Azure ポータルで作成した後、Microsoft Power Platform アプリケーション ユーザーとして追加する必要があります。 

1. Power Platform 管理センターで、[アプリケーション ユーザーの作成](/power-platform/admin/manage-application-users#create-an-application-user)の手順に従ってアプリケーション ユーザーを作成します。
2. アプリケーション ユーザーに追加するセキュリティ ロールを選択するステップで、**財務と運用の統合ユーザー** を選択します。

### <a name="grant-app-permissions-in-finance-and-operations-apps"></a>財務と運用アプリでアプリのアクセス許可を付与する

Dataverse は、財務と運用アプリを呼び出すために作成した Azure AD アプリケーションを使用します。 したがって、アプリケーションは財務と運用アプリによって信頼され、適切な権限を持つユーザー アカウントに関連付けられている必要があります。

1. 財務と運用アプリで、**システム管理 \> 設定 \> Azure Active Directory アプリケーション** に移動します。
2. **新規** を選択してグリッドに行を追加し、次の情報を入力します。

    - **クライアント ID** – 既に作成した Azure AD アプリケーションの **アプリケーション (クライアント) ID** の値を入力します。
    - **名前** – **Dataverse 統合** (または統合で認識する別の名前) を入力します。
    - **ユーザー ID** – **PowerPlatformApp** を選択します。

> [!NOTE]
> 利用可能な **PowerPlatformApp** ユーザーは、財務と運用アプリとの Dataverse 統合のための適切なアクセス許可を持っています。 ただし、このユーザーが存在しない場合、または別のアプリケーション ユーザー アカウントを使用する場合は、次のいずれかのロールを持つ他のユーザーを作成または使用できます。**ビジネス イベントのセキュリティ ロール**、**Dataverse 仮想エンティティ アプリケーション**、**Dataverse 仮想エンティティ匿名ユーザー**、および **Dataverse 仮想エンティティ認証ユーザー**。

### <a name="configure-finance-and-operations-apps-to-use-the-azure-ad-application-to-connect-to-dataverse"></a>財務と運用アプリを構成して、Dataverse に接続するための Azure AD アプリケーションを使用する 

1. リモート デスクトップ プロトコル (RDP) を使用して、財務と運用の環境にサインインします。
2. 次の Windows PowerShell スクリプトをコピーし、財務と運用環境の仮想マシン (VM) に .ps1 ファイルとして保存します。

    ```powershell
    param(
        [Parameter(Mandatory = $false)]
        [switch]$Relaunched
    )

    $isRelaunched = $false
    if ($PSBoundParameters.ContainsKey("Relaunched"))
    {
        $isRelaunched = $Relaunched.IsPresent
    }

    if (-not ([Security.Principal.WindowsPrincipal] [Security.Principal.WindowsIdentity]::GetCurrent()).IsInRole([Security.Principal.WindowsBuiltInRole]::Administrator))
    {
        # Relaunch as an elevated process:
        Start-Process powershell.exe "-File", ('"{0}"' -f $MyInvocation.MyCommand.Path), "-Relaunched" -Verb RunAs
        exit
    }

    $aosWebsiteName = "AOSService"

    function Get-AosWebSitePhysicalPath()
    {
        if (Get-Service W3SVC | Where-Object status -ne 'Running')
        {
            #IIS service is not running, starting IIS Service.
            Start-Service W3SVC
        }

        $webSitePhysicalPath = (Get-Website | Where-Object { $_.Name -eq $aosWebsiteName }).PhysicalPath

        return $webSitePhysicalPath
    }

    function Get-WebConfigValue($Key)
    {
        $webroot = Get-AosWebSitePhysicalPath
        $webConfigPath = Join-Path $webroot "web.config"
        if (-not (Test-Path $webConfigPath))
        {
            Throw "Unable to find web.config file at '$($webConfigPath)'..."
        }

        [xml]$webConfigDocument = Get-Content $webConfigPath -ErrorAction stop
        $appSettingNode = $webConfigDocument.SelectSingleNode("/configuration/appSettings/add[@key='$($Key)']")
        if ($appSettingNode)
        {
            return $appSettingNode.Value
        }

        return $null
    }

    function Set-WebConfigValue($Key, [string]$Value)
    {
        $webroot = Get-AosWebSitePhysicalPath
        $webConfigPath = Join-Path $webroot "web.config"
        if (-not (Test-Path $webConfigPath))
        {
            Throw "Unable to find web.config file at '$($webConfigPath)'..."
        }

        [xml]$webConfigDocument = Get-Content $webConfigPath -ErrorAction stop
        $appSettingNode = $webConfigDocument.SelectSingleNode("/configuration/appSettings/add[@key='$($Key)']")
        if ($null -ne $appSettingNode)
        {
            Write-Host "Updating key '$($Key)' to value '$($Value)'..."
            $appSettingNode.Value = [string]$Value
        }
        else
        {
            Write-Host "Inserting new key '$($Key)' with value '$($Value)'..."
            $ns = New-Object System.Xml.XmlNamespaceManager($webConfigDocument.NameTable)
            $ns.AddNamespace("ns", $webConfigDocument.DocumentElement.NamespaceURI)
            $addElement = $webConfigDocument.CreateElement("add")
            $addElement.SetAttribute("key", $Key)
            $addElement.SetAttribute("value", $Value)
            $appSettings = $webConfigDocument.SelectSingleNode("//ns:appSettings", $ns)
            $appSettings.AppendChild($addElement) | Out-Null
        }

        $webConfigDocument.Save($webConfigPath)
        Write-Host
    }

    function Confirm-ValueOfType($Value, $Type)
    {
        if ($Type -eq "Uri")
        {
            try
            {
                New-Object System.Uri $Value | Out-Null
            }
            catch
            {
                Throw "Cannot parse '$($Value)' as a URL: $($_)"
            }
        }
        elseif ($Type -eq "Guid")
        {
            try
            {
                [Guid]::Parse($Value) | Out-Null
            }
            catch
            {
                Throw "Cannot parse '$($Value)' as a guid: $($_)"
            }
        }
        elseif ($Type -eq "String")
        {
            if ([string]::IsNullOrEmpty($Value))
            {
                Throw "String value cannot be empty."
            }
        }
    }

    function Update-WebConfigValueFromHost($Key, $Prompt, $Type)
    {
        $shouldUpdate = $true
        $currentValue = Get-WebConfigValue -Key $Key
        if ($currentValue)
        {
            if ($Type -eq "Secret")
            {
                $currentValue = "<redacted>"
            }

            while ($true)
            {
                $yesNoResponse = Read-Host -Prompt "Value for '$($Prompt)' is already set to '$($currentValue)'. Do you want to overwrite it? (y/n)"
                if ($yesNoResponse -eq "y" -or $yesNoResponse -eq "yes")
                {
                    $shouldUpdate = $true
                    break
                }
                elseif ($yesNoResponse -eq "n" -or $yesNoResponse -eq "no")
                {
                    $shouldUpdate = $false
                    break
                }
                else
                {
                    Write-Host "Did not recognize input value '$($yesNoResponse)' - please try again."
                }
            }
        }

        if ($shouldUpdate)
        {
            $value = Read-Host -Prompt "Enter $($Prompt)"
            Confirm-ValueOfType -Value $value -Type $Type
            if ($Type -eq "Secret")
            {
                # If value is blank, assume we are trying to clear it
                $secretValue = ""
                if (-not [string]::IsNullOrEmpty($value))
                {
                    $webroot = Get-AosWebSitePhysicalPath -ErrorAction stop
                    $webrootBinPath = Join-Path $webroot "bin"
                    $b2bInvitationHelperDllPath = Join-Path $webrootBinPath "Microsoft.Dynamics.AX.Security.B2BInvitationHelper.dll"
                    Add-Type -Path $b2bInvitationHelperDllPath

                    $encryptionEngine = [Microsoft.Dynamics.AX.Security.B2BInvitationHelper.Cryptor]::GetEncryptionEngine()
                    $secretValue = [System.Convert]::ToBase64String($encryptionEngine.Encrypt($value))
                }

                $value = $secretValue
            }

            Set-WebConfigValue -Key $Key -Value $value
        }
    }

    function Enable-Flight($FlightName)
    {
        Write-Verbose "Enabling flight '$($FlightName)'..."
        $webroot = Get-AosWebSitePhysicalPath -ErrorAction stop
        $webrootBinPath = Join-Path $webroot "bin"
        $environmentDllPath = Join-Path $webrootBinPath 'Microsoft.Dynamics.ApplicationPlatform.Environment.dll'
        Add-Type -Path $environmentDllPath

        $config = [Microsoft.Dynamics.ApplicationPlatform.Environment.EnvironmentFactory]::GetApplicationEnvironment()

        $ServerName = $config.DataAccess.DbServer
        $DatabaseName = $config.DataAccess.Database
        $UserId = $config.DataAccess.SqlUser
        $Password = $config.DataAccess.SqlPwd
        $EnableFlightQuery = "DECLARE @flightName NVARCHAR(100) = '$($FlightName)';
        IF NOT EXISTS (SELECT TOP 1 1 FROM SysFlighting WHERE flightName = @flightName)
            INSERT INTO SYSFLIGHTING(FLIGHTNAME,ENABLED, FLIGHTSERVICEID, PARTITION)
            SELECT @flightName, 1, 12719367, RECID FROM DBO.[PARTITIONS];
        ELSE
            UPDATE SysFlighting SET enabled = 1, flightServiceId = 12719367 WHERE flightName = @flightName;"

        Invoke-Sqlcmd -ServerInstance $ServerName -Database $DatabaseName -Username $UserId -Password $Password -Query $EnableFlightQuery
        Write-Verbose "Flight '$($FlightName)' has been enabled."
    }

    function Test-Settings()
    {
        $cdsApiPath = "sdkmessages";
        Write-Host "Testing setup by calling API '$($cdsApiPath)'..."
        $webroot = Get-AosWebSitePhysicalPath -ErrorAction stop
        $webrootBinPath = Join-Path $webroot "bin"
        $httpCommunicationDllPath = Join-Path $webrootBinPath "Microsoft.Dynamics.HttpCommunication.dll"
        Add-Type -Path $httpCommunicationDllPath

        try
        {
            $assembly = [System.Reflection.Assembly]::LoadFile($httpCommunicationDllPath)
            $loggerType = $assembly.GetType("Microsoft.Dynamics.HttpCommunication.Logging.InMemoryLogger")
            $bindingFlags = [System.Reflection.BindingFlags]::Instance -bor [System.Reflection.BindingFlags]::Public
            $loggerConstructor = $loggerType.GetConstructor($bindingFlags, $null, [System.Type]::EmptyTypes, $null)
            $logger = $loggerConstructor.Invoke($null)

            $cdsWebApiClient = New-Object Microsoft.Dynamics.HttpCommunication.Cds.CdsWebApiClient $logger;
            $bindingFlags = [System.Reflection.BindingFlags]::Instance -bor [System.Reflection.BindingFlags]::NonPublic
            $method = [Microsoft.Dynamics.HttpCommunication.Cds.CdsWebApiClient].GetMethod("GetWithStringResponse", $bindingFlags, $null, @([string]), $null)
            $task = $method.Invoke($cdsWebApiClient, @($cdsApiPath))
            $response = $task.GetAwaiter().GetResult()

            Write-Host $logger.LogContent.ToString()
            Write-Host "Received response with length: $($response.Length)" 
            Write-Host "Test complete."
        }
        catch
        {
            Write-Verbose $logger.LogContent.ToString()
            Throw "Failed while testing the new settings: $($_)"
        }
    }

    try
    {
        Update-WebConfigValueFromHost -Key "Infrastructure.CdsOrganizationUrl" -Prompt "Dataverse Organization URL" -Type "Uri"
        Update-WebConfigValueFromHost -Key "Infrastructure.CdsOrganizationId" -Prompt "Dataverse Organization id" -Type "Guid"
        Update-WebConfigValueFromHost -Key "Infrastructure.DataverseCommunicationAadTenantId" -Prompt "Dataverse AAD Tenant domain (e.g. Contoso.OnMicrosoft.com)" -Type "String"
        Update-WebConfigValueFromHost -Key "Infrastructure.DataverseCommunicationAppId" -Prompt "Dataverse AAD App id" -Type "Guid"
        Update-WebConfigValueFromHost -Key "Infrastructure.DataverseCommunicationAppSecretEncrypted" -Prompt "Dataverse AAD App secret" -Type "Secret"

        Enable-Flight -FlightName "BusinessEventsCDSIntegration"

        Write-Host "Restarting AOS..."
        Stop-Website -Name $aosWebSiteName
        Start-Website -Name $aosWebSiteName
        Write-Host "AOS has been restarted."

        Test-Settings
    }
    catch
    {
        Write-Error $_
    }

    if ($isRelaunched)
    {
        Write-Host "Press any key to continue..."
        [System.Console]::ReadKey() | Out-Null
    }

    ```

3. 指示に従って Windows PowerShell スクリプトを実行します。 次の情報を入力します。

    - **Dataverse 組織 URL** – Dataverse へのアクセスに使用する URL を入力します。 たとえば、「`https://contoso.crm.dynamics.com`」を入力します。 この URL は、Power Platform 管理センターの環境詳細にある **詳細** セクションの **環境 URL** フィールドで見つけることができます。
    - **Dataverse 組織 ID** – この ID は、Power Platform 管理センターの環境詳細にある **詳細** セクションの **組織 ID** フィールドに見つけることができます。
    - **Dataverse AAD テナント ドメイン** – Dataverse で使用される Azure AD テナントのプライマリ ドメインを入力します。 このドメインは、[Asure ポータル](https://portal.azure.com)の **ポータル設定** ページのディレクトリにある **ドメイン** フィールドに見つけることができます。 通常、管理者の電子メール アドレスのドメイン セグメントです。 たとえば、電子メール アドレスが `admin@contoso.onmicrosoft.com` の場合、ドメインは `contoso.onmicrosoft.com` です。
    - **Dataverse AAD アプリ ID** – 既に作成した Azure AD アプリケーションの **アプリケーション (クライアント) ID** の値を入力します。
    - **Dataverse AAD アプリ シークレット** – Azure AD アプリのために既に作成したシークレット キーの値を入力します。

## <a name="verifying-power-platform-integration-status"></a>Power Platform の統合ステータスを検証する

```RetrieveFinanceAndOperationsIntegrationDetails``` API は、Power Platform 環境の Power Platform 統合のステータスを検証するために使用できます。 Power Platform 環境が Power Platform 統合を介して財務と運用アプリ環境にリンクされている場合、API は財務と運用アプリ環境の AAD テナントと環境の詳細を返します。

API をトラブルシューティングに使用して、Power Platform 統合が環境で有効になっていることを確認できます。 また、プラグイン、クライアント フォーム、または Power Platform 環境にリンクされた財務と運用アプリ環境を認識する必要があるその他のアプリケーションのコーディングに API を使用することもお勧めします。

**申請**
```http
GET [Organization URI]/api/data/v9.1/RetrieveFinanceAndOperationsIntegrationDetails
```

**応答**
```json
{
    "Url": "https://contoso.operations.dynamics.com",
    "TenantId": "72ad15fq-3m88-4e15-be25-8751c9bd0764",
    "Id": "b2106f5c-e218-4aac-841a-a59da4738eb4"
}
```

**プロパティ**

| プロパティ<br>**現物名**<br>**_種類_** | 使用 | Description |
| --- | --- | --- |
| 環境 URL<br>**URL**<br>**_文字列_** | 読み取り専用<br>必須 | Power Platform 統合を介して Power Platform 環境にリンクされた財務と運用アプリ環境の URL。 |
| テナント ID<br>**TenantId**<br>**_GUID_** | 読み取り専用<br>必須 | 財務と運用アプリ環境と Power Platform 環境の両方が配置されている Azure AD テナントの ID。 |
| 環境 ID<br>**ID**<br>**_GUID_** | 読み取り専用<br>必須 | Power Platform 統合を介して Power Platform 環境にリンクされた財務と運用アプリ環境の ID。 |

環境が Power Platform 統合を介して財務と運用アプリ環境にリンクされていない場合、API 応答で次のエラーが返されます:

| エラー コード | メッセージ |
| --- | --- |
| 0x80048d0b | Dataverse インスタンスは財務と運用と統合されていません。 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

