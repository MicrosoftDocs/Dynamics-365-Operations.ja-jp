---
title: Azure Data Lake へのエクスポートの構成
description: このトピックでは、Azure Data Lake へのエクスポートの構成に関する情報を説明します。
author: MilindaV2
ms.date: 09/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 96283
ms.assetid: ''
ms.search.region: Global
ms.author: milindav
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform Update 33
ms.openlocfilehash: 4a084049c77e56acc9b6e3536da672ae6b39be7d
ms.sourcegitcommit: 4fbf031319109660c0462a800f85848571eb040d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/02/2021
ms.locfileid: "7471349"
---
# <a name="configure-export-to-azure-data-lake"></a>Azure Data Lake へのエクスポートのコンフィギュレーション

[!include [banner](../includes/banner.md)]

> [!NOTE]
> **Data Lake へのエクスポート** 機能は、米国、カナダ、英国、ヨーロッパ、南アジア、東アジア、オーストラリア、および日本の地域でパブリック プレビューで表示されます。 Finance and Operations 環境がそれらの地域にある場合は、Microsoft Dynamics Lifecycle Services (LCS) を使用して、環境でこの機能を有効にできます。
>
> **環境のプレビュー期間中に機能が一時的に利用できない場合や、お客様の地域で利用できない場合があります。**
> 
> 数ヶ月後に、Microsoft は追加の地域および環境でこの機能を有効にします。 環境が以前にリストされた地域のひとつにない場合は、[アンケートを完了し、お知らせください](https://aka.ms/FnODataLakePreviewSurvey)。 [プレビュー Yammer グループ](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=32768909312&view=all)に参加することもできます。 Yammer グループを使用して、機能を理解するのに役立つ質問をお伝えすることができます。 
>
> **Data Lake へのエクスポート** 機能は、Tier 1 (開発者) 環境では使用できません。 この機能を有効化するには、クラウド ベースの Tier 2 またはそれ以上の環境が必要です。 
> 
> Tier 1 (開発者) 環境では、[GitHub ツール](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Analytics/AzureDataFactoryARMTemplates/SQLToADLSFullExport/ReadmeV2.md) を使用して機能の実装のプロトタイプを作成または計画できます。 このツールを使用すると、機能によってエクスポートされたのと同じ形式で、階層 1 またはサンドボックス環境のデータをストレージ アカウントにエクスポートすることができます。 
> 
> **プレビュー中は、運用環境ではこの機能がサポートされていません。** 運用環境では、この機能を有効にすることはできません。 サンドボックス (階層 2 以降) 環境でのみプレビューできます。

## <a name="create-service-principal-for-microsoft-dynamics-erp-microservices"></a><a name="createServicePrincipal"></a> Microsoft Dynamics ERP Microservices のサービス プリンシパルの作成

**Azure Data Lake へのエクスポート** 機能は、Finance and Operations アプリ データを Azure Data Lake へエクスポートしデータを最新の状態に維持するマイクロサービスを使用して構築されます。 マイクロサービスは、Azure サービス プリンシパル、**Microsoft Dynamics ERP Microservices** を使用して、Azure リソースに安全に接続します。 Data Lake にエクスポートする機能を構成する前に、**Microsoft Dynamics ERP マイクロサービス** サービス プリンシパルを Azure Active Directory (Azure AD) に追加します。 この手順により Azure AD を有効にしてマイクロサービスを認証できます。 

> [!NOTE]
> これらの手順を実行するには、**Azure Active Directory グローバル管理者** の権限が必要です。

サービス プリンシパルを追加するには、次の手順を実行します。

1. Azure portal を起動し、Azure Active Directory にアクセスします。
2. 左のメニューで、**管理** > **エンタープライズ アプリケーション** を選択し、以下のアプリケーションを検索します。

    | 申請書                          | アプリ ID |
    |--------------------------------------|--------|
    | Microsoft Dynamics ERP マイクロサービス | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |

    上記のアプリケーションが見つからない場合は、次の手順を完了してください。

3. ローカル コンピューターで、**スタート** メニューを開き、**PowerShell** を検索します。
4. **Windows PowerShell** を右クリックし、**管理者として実行** を選択します。
5. 以下のコマンドを実行して **AzureAD** モジュールをインストールします。

    ```powershell
    Install-Module -Name AzureAD
    ```

    - NuGet プロバイダーを続行する必要がある場合は、**Y** を選択してインストールします。
    - **信頼できないリポジトリ** のメッセージが表示された場合は、**Y** を選択して続行します。

6. Azure Active Directory へのアクセス許可を付与するには、次のコマンドを実行します。

    ```powershell
    Connect-AzureAD
    ```
    
    ```powershell
    New-AzureADServicePrincipal –AppId '0cdb527f-a8d1-4bf8-9436-b352c68682b2'
    ```

7. メッセージが表示されたら、管理者で Azure Active Directory にログインします。

## <a name="configure-azure-resources"></a><a name="ConfigureAzureResources"></a>Azure リソースの構成 

Data Lake へのエクスポートを構成するには、ご利用の Azure サブスクリプションにストレージ アカウントを作成します。 このストレージ アカウントはデータの格納に使用されます。 続いて、ストレージ アカウントのルートへのアクセスを許可する Azure AD のアプリケーション ID を作成します。 Finance or Operations アプリは、 Azure AD アプリケーションを使用してストレージへのアクセスや、フォルダ構造の作成や、データの書き込みを行います。 サブスクリプションにキー コンテナーを作成し、ストレージ アカウントの名前、アプリケーション ID、アプリケーションのシークレットを保存します。 Azure ポータルでリソースを作成するアクセス許可がない場合は、組織内でこのアクセス許可を持つユーザーの支援が必要となります。

Azure portal で行われる手順は次のとおりです。

> [!NOTE]
> Azure portal で作業する場合は、後続の手順に対して複数の値を保存するように指示されます。 また、これらの値の一部は、Lifecycle Services (LCS) を使用して Finance and Operations アプリに提供されます。 これを行うには、LCS への管理者アクセス権が必要です。

1. [Azure Active Directory でアプリケーションを作成する](#createapplication)
2. [サブスクリプションに Data Lake ストレージ (Gen2 アカウント) を作成します](#createsubscription)
3. [アプリケーションにアクセス制御ロールを付与する](#grantaccess)
4. [キー コンテナーの作成](#createkeyvault)
5. [キー コンテナーにシークレットを追加する](#addsecrets)
6. [キー コンテナーのシークレットを読み取るためにアプリケーションを許可する](#authorize)
7. [Power Platform 統合](#powerplatformintegration)
8. [LCS の Data Lake アドインへのエクスポートのインストール](#installaddin)

## <a name="create-an-application-in-azure-active-directory"></a><a name="createapplication"></a>Azure Active Directory でアプリケーションを作成する

1. Azure ポータルで、**Azure Active Directory** を選択し、**アプリケーション登録** を選択します。
2. **新しいアプリケーションの登録** を選択し、以下の情報を入力します。 

    - **名前:** アプリの名前を入力します。
    - **対応しているアカウントのタイプ** : 適切なオプションを選択します。

3. アプリケーションの作成後は、これを選択し、<a name="appid"></a> アプリケーション (クライアント) IDをページの先頭に保存します。 これは後で必要になります。
4. 左のナビゲーション ウィンドウで、**API のアクセス許可** を選択します。
5. **アクセス許可の追加** を選択し、**API アクセス許可の要求** ダイアログ ボックスで、**Azure キー コンテナー** を選択し ます。
6. **委任されたアクセス許可** を選択し 、**user_impersonation** を選択します。続いて **アクセス許可の追加** を選択します。
7. 左のナビゲーションウィンドウで、**証明書とシークレット** を選択し、 **新たなクライアント シークレット** を選択します。 
8. **説明** フィールドに名前を入力します。
9. **有効期限** フィールドで、オプションを選択し、**追加** を選択します。 システムがシークレットを生成し、グリッドの下に表示します。 
10. シークレット **値** をクリップボードにコピーします。 これは後でキー コンテナーを設定する際に、<a name="secret"></a> 値を提供する必要があります。

## <a name="create-a-data-lake-storage-gen2-account-in-your-subscription"></a><a name="createsubscription"></a>サブスクリプションに Data Lake ストレージ（Gen2）を作成します

Data Lake ストレージ アカウントは、Finance and Operations アプリのデータを格納する目的で使用されます。 ストレージ アカウントを手動で作成するには、Azure サブスクリプションへの管理者権限を持つユーザーである必要があります。 ストレージ アカウントを作成するには、次の手順を完了してください。

1. Azure portalで、**新しいリソースの作成** を選択し、**ストレージアカウント (blob、ファイル、テーブル、キュー)** を検索して選択し ます。
2. **ストレージ アカウントを作成** ダイアログ ボックスで、次のパラメーター フィールドの値を指定します。

    - **場所:** 環境があるデータ センターを選択します。 選択したデータ センターが異なる Azure リージョンにある場合は、データ移動コストが発生する場合があります。 Microsoft Power BI やデータ ウェアハウスが別の地域にある場合は、地域間でのストレージ移動にはレプリケーションを使用することができます。
    - **パフォーマンス**: **標準** を選択することを推奨します。
    - **アカウントの種類**: 必ず **Storage V2** を選択してください。 **詳細オプション** ダイアログ ボックスに、**Data Lake ストレージ Gen2** オプションが表示されます。

3. **詳細タブ** で、 **Data Lake storage Gen2** \> **階層の名前空間** を選択し、**有効化** を選択し ます。 このオプションを無効にすると、Power BI データフローや AI Builder などのサービスを使用して Finance and Operations アプリが書き込んだデータを使用できなくなる場合があります。
4. **確認して作成** を選択します。 デプロイの完了後は、新たなリソースが Azure ポータルに表示されます。
5. Azure portal で、作成したストレージ アカウントを選択します。 ストレージ<a name="storageaccount"></a>アカウント名をコピーして保存し ます。

## <a name="grant-access-control-roles-to-applications"></a><a name="grantaccess"></a>アプリケーションにアクセス制御ロールを付与する 

アプリケーションにストレージ アカウントの読み取り、書き込みのアクセス許可を付与する必要があります。 これらのアクセス許可は、Azure AD のロールを使用して付与されます。

1. **Azure ポータルl** で、作成済のストレージ アカウントを開きます。
2. 左側のナビゲーション ウィンドウで、**アクセス制御 (IAM)** を選択します。 
3. **アクセス制御** ページで、**ロールの割り当て** タブを選択します。
4. ページの上部の **追加** を選択し、**ロール割り当ての追加** を選択します。
5. **ロール割り当ての追加** ダイアログ ボックスで、**ロール** フィールドを選択し、**ストレージ BLOB データの共同作成者** を選択します。
6. **選択** フィールドで、前述の手順で登録したアプリケーションを選択します。

    > [!NOTE]
    > フィールド対する変更、**Azure AD ユーザー、グループ、サービス プリンシパル** への **アクセス権の割り当て** は行わないでください。

7. **保存** を選択します。
8. 手順 4 ~ 7 を繰り返して、次に示すように **ストレージ BLOB データの読み取り** ロールを追加します。
9. 先ほど作成した[アプリケーション](#appid) のストレージ アカウント ロール の割り当てを検証します。 

    | 申請書                                   | 役割 |
    |-----------------------------------------------|------|
    | 既に作成した[アプリケーション](#appid) | ストレージ BLOB データの共同作成者 |
    | 既に作成した[アプリケーション](#appid) | ストレージ BLOB データの読み取り権限を持つユーザー |

## <a name="create-a-key-vault"></a><a name="createkeyvault"></a> キー コンテナーの作成

キーボルトは、ストレージ アカウント名などの詳細情報を Finance and Operations アプリに共有する安全な手段です 。 キー コンテナーとシークレットを作成するには、次の手順を完了してください。

1. Azure portalで、**新しいリソースの作成** を選択し、**キー コンテナー** を検索して選択し ます。
2. **キー コンテナーの作成** ダイアログ ボックスの **場所** フィールドで、環境があるデータ センターを選択します。
3. キー コンテナーの作成後は、一覧から選択し、左側のナビゲーション ウィンドウで **概要** を選択します。 
4. <a name="dnsname"></a>**DNS名** フィールドに値を保存します。 後に、この値を使用します。

## <a name="add-secrets-to-the-key-vault"></a><a name="addsecrets"></a>キー コンテナーにシークレットを追加する

キーコンテナーに3つのシークレットを作成し、前述の手順で保存した値を追加します。 それぞれのシークレットに対して、前述の手順で保存したシークレット名を入力し、値を入力する必要があります。

| <a name="suggest"></a> 推奨されたシークレット名 | 前述の手順で保存したシークレット値 | シークレット値の例 |
|---------------------------------------------|-------------------------------------|----------------------|
| アプリ ID                                      | [作成済みの](#appid)アプリケーション オブジェクトの ID。 | 8936e905-197b-xxx-xxxx-xxxxxxxxx |
| アプリのシークレット                                  | 前述の手順で入力した[クライアント シークレット](#secret)です。 | NaeIxxxxxxx---xxxx7eixxx ~ 1g- |
| storage-account-name                        | 上記手順で作成した[ストレージアカウントの名前](#storageaccount)です。 | contosod365datalake |

それぞれのシークレットごとに 1 回ずつ、以下の手順を 3 回実行する必要があります。

1. Azure portalで、上記手順で作成したキー コンテナーに移動し、左側のナビゲーション ウィンドウで **シークレット** を選択し ます。
2. **生成/インポート** を選択し、**シークレットの作成** ダイアログ ボックスの、 **アップロード オプション** フィールドで **手動** を選択します。
3. シークレットの名前を入力します。 このセクション冒頭の「推奨される名前」の表を参照してください。
4. **値** フィールドに、対応するシークレットの値をコピーして貼り付け ます。
6. **有効** を選択し、**作成** を選択します。 

シークレットの一覧に作成されたシークレットが表示されます。

## <a name="authorize-the-application-to-read-secrets-in-the-key-vault"></a><a name="authorize"></a>キー コンテナーのシークレットを読み取るためにアプリケーションを許可する

1. **Azure ポータルl** で、作成済のキー コンテナーを開きます。
2. **アクセスポリシーの追加** ダイアログ ボックスで、**追加** を選択します。
3. 左のナビゲート ウィンドウ、**アクセス ポリシー > 新規ポリシーの追加** を選択して、新規ポリシーを作成します。 
4. **アクセス ポリシーの追加** ダイアログ ボックスの **プリンシパルの選択** フィールドで、**Microsoft Dynamics ERP マイクロサービス** を検索して選択し、**選択** をクリックします。 

    > [!NOTE]
    > **Microsoft Dynamics ERP Microservices** が見つからない場合は、このドキュメントの[サービス プリンシパルの作成](#createServicePrincipal) セクションを参照してください。

5. **シークレットのアクセス許可** フィールドで、**取得** と **リスト** を選択します。
6. **アクセスポリシー** ダイアログ ボックスで、**追加** を選択します。

    以下のように、キー コンテナーへのアクセス権を持つアプリケーションが表示されます。

    | 申請書                          | シークレットのアクセス許可 |
    |--------------------------------------|--------------------|
    | Microsoft Dynamics ERP マイクロサービス | 取得、リスト表示          |

7. **保存** を選択します。

## <a name="power-platform-integration"></a><a name="powerplatformintegration"></a>Power Platform 統合

この環境に初めてアドインをインストールする場合、この環境に対して **Power Platform 統合** を有効にする必要があるかもしれません。 Finance and Operations アプリケーション環境で Power Platform 統合を設定するには 2 つのオプションがあります。

### <a name="option-1-set-up-power-platform-integration-using-lcs"></a>オプション 1: LCS を使用して Power Platform 統合の設定

LCS から Power Platform 統合を設定するには、[アドインの概要](../power-platform/add-ins-overview.md) を参照してください。

### <a name="option-2-set-up-power-platform-integration-using-the-dual-write-wizard"></a>オプション 2: 二重書き込みウィザードを使用して Power Platform 統合の設定

**Power Platform 統合** を設定するもう 1 つの方法は、データベースで Power Platform 環境を作成し、二重書き込みの設定を使用します。 次の手順を実行して、Power Platform 環境を作成し、統合を完了します。 

1. [データベースを使用して環境を作成します](/power-platform/admin/create-environment#create-an-environment-with-a-database.md)。
2. [要件と前提条件を完了します](dual-write/requirements-and-prerequisites.md)。
3. [二重書き込みウィザードを使用して環境をリンクする](dual-write/link-your-environment.md) を使用します。
4. Power Platform 統合が設定され、LCS 環境ページに追加されていることを確認します。

> [!NOTE]
> このアプローチを使用する場合は、Finance and Operations 環境と同じリージョンにある Power Platform 環境を選択する必要があります。 別の地域の Power Platform 環境を選択した場合、アドインのインストールが失敗する場合があります。

## <a name="install-the-export-to-data-lake-add-in-in-lcs"></a><a name="installaddin"></a>LCS の Data Lake アドインへにエクスポート機能をインストールする 

Finance and Operations アプリからデータ レイクにデータをエクスポートするには、LCS の **Data Lake エクスポートする** アドインをインストールする必要があり ます。 このタスクを完了するには、使用する環境の LCS 環境管理者である必要があります。

これを開始する前に、次の情報を確認する必要があります。 作業の開始前に、情報を手元に保管しておいてください。

| Data lake アドインへのエクスポートに必要な情報       | 見つけられる場所 | 例 |
|-----------------------------------------------------------|-----------------------|---------|
| ご利用の Azure AD テナント ID                       | Azure AD テナント ID は Azure ポータルで確認できます。 **Azure ポータル** にログインし、**Azure Active Directory**  サービスを開きます。 **プロパティ** ページを開き、**ディレクトリ ID** フィールドの値をコピーします。 | 72f988bf-0000-0000-00000-2d7cd011db47 |
| キー コンテナーの DNS 名                                | この名前は、あらかじめ保存しておく必要があります。 キー コンテナーの [DNS 名](#dnsname) を入力します | `https://contosod365datafeedpoc.vault.azure.net/` |
| ストレージ アカウントの名前を含むシークレット | 提示された名前を使用した場合は、**storage-account-name** を入力します。 これを使用していない場合は、定義した[シークレット名](#suggest)を入力します。 | storage-account-name |
| アプリケーション ID を含むシークレット                   | 定時された名前を使用した場合は、**app id** を入力してください。これを使用していない場合は、定義した[シークレット名](#suggest)を入力します。 | アプリ ID |
| アプリケーションのシークレットを含むシークレット               | 提示された名前を使用した場合は、**app-secret** を入力します。 これを使用していない場合は、定義した[シークレット名](#suggest)を入力します。 | アプリのシークレット |

1. [LCS](https://lcs.dynamics.com) にログインし、ご利用の環境に移動します。
2. **環境** ページで、**環境アドイン** タブを選択します。**Data lakeの エクスポート** が一覧に表示される場合は、Data Lake アドインが既にインストールされているため、この手順の残りの部分は省略することができます。 これに該当しない場合は、残りの手順を実行してください。
3. **インストールするアドイン** を選択し、ダイアログ ボックスで、**Data lake にエクスポート** を選択します。 **Data lake にエクスポート** が表示されない場合は、この機能がご利用の環境で使用できない可能性があります。
4. **設定のアドイン** ダイアログ ボックスで、必要な情報を入力します。 質問に答えるには、既にストレージ アカウントが作成されている必要があります。 ストレージ アカウントをまだ持っていない場合は、作成するか、管理者にアカウントの作成代行を依頼してください。
5. チェック ボックスをオンにしてサービス条件を承認し、**インストール** を選択します。

システムが、ご利用の環境に Data Lake をインストールし構成します。 この操作には数分かかる場合があります。 インストールとコンフィギュレーションが完了したら、**Data Lake にエキスポート** は **環境** ページに記載され、ステータスは **インストール済** である必要があります。 別のステータスが表示される場合は、次の「トラブルシューティング」のセクションを参照してください。

## <a name="troubleshooting"></a><a name="troubleshooting"></a> トラブルシューティング

### <a name="add-in-installation-isnt-completed-within-a-few-minutes"></a>数分後にインストールしたアドインが完了しない

場合によっては、アドイン インストールのステータスが **インストール** または **コンフィグレーション** に、10 分以上表示される場合があります。 遅延の原因は、コンフィギュレーションの問題や不足しているパラメータによるものです。 この場合、**中止** オプションを選び、手順に従って再度[アドインをインストール](#installaddin) してください。 

### <a name="add-in-installation-fails"></a>アドインのインストールに失敗

場合によっては、アドイン インストールのステータスが **インストールに失敗** と表示されます。 インストールに失敗した場合は、エラー コードとエラー メッセージが表示されます。 次の表の「解決策」列に、失敗の理由の修正に役立つ候補が示されています。 この問題を修正するには、**中止** オプションを選び、手順に従って再度[アドインをインストール](#installaddin) してください。

| エラー コードとメッセージ | 解決策 |
|------------------------|------------|
| **AppidUserError**: Data Lake にアクセスするためのアプリケーション ID の検出に失敗しました。 指定されたアプリケーション ID が正しくない、または見つかりません。 | キー コンテナーで提供される申請 ID (**アプリ -ID**) は、Azure AD で見つかりません。 [Azure Data Lake へのエクスポートのコンフィギュレーション - 申請書の作成](#createapplication) の手順に従って、申請 ID を検証します。 システム管理者または Azure リソースを構成した管理者に連絡する必要があるかもしれません。 |
| **AppSecretUserError**: 指定されたアプリケーション ID とアプリケーション シークレットで Data Lake にアクセスできませんでした。 | 提供された申請 ID (**アプリ -ID**) と申請シークレット (**アプリ - シークレット**) は、ストレージ アカウントへのアクセスには使用できません。 [Azure Data Lake へのエクスポートのコンフィギュレーション - 申請書の作成](#createapplication) に記載の手順に従って、アプリケーション ID とアプリケーション シークレットを検証します。 次に、ストレージ アカウントに必要なアクセス権を持っているかどうかを確認します。 詳細については、[Azure Data Lake へのエクスポートのコンフィギュレーション - アクセス権の付与](#grantaccess)を参照してください。 システム管理者または Azure リソースを構成した管理者に連絡する必要があるかもしれません。 |
| **StorageNameUserError**: キー コンテナーで指定されているストレージ名を使用してストレージ アカウントにアクセスできませんでした。 | キー コンテナーで指定されているストレージ アカウントが見つからない、または無効です。 [Azure Data Lake へのエクスポートのコンフィギュレーション - シークレットの追加](#addsecrets) に記載の手順に従って、正しいストレージ アカウント名がキー コンテナーに入力されていることを確認します。 [Azure Data Lake へのエクスポートのコンフィギュレーション - シークレットの追加](#addsecrets) に記載の手順に従って、ストレージ アカウントに正しいシークレット名が指定されていることを確認します。 |
| **KeyVaultUserError**: キー コンテナーまたはキー コンテナーのシークレットにアクセスできませんでした。 | サービスが、キー コンテナーまたはキー コンテナーのシークレットにアクセスできません。 Azure サブスクリプションの有効期限が切れていないことを確認します。 [Azure Data Lake へのエクスポートのコンフィギュレーション - サービス プリンシパルの作成](#createServicePrincipal) に記載の手順に従って、サービス プリンシパルが作成されていることを確認します。 [Azure Data Lake へのエクスポートのコンフィギュレーション - シークレットの追加](#addsecrets)に記載の手順に従って、キー コンテナーに必要なシークレットがすべて含まれていることを確認します。 [Azure Data Lake へのエクスポートのコンフィギュレーション - アドインのインストール](#installaddin) の構成手順で、正しいキー コンテナー URI が指定されていることを確認します。 |
| **TenantIdUserError**: 環境の Azure テナント ID の検索に失敗しました。 | [Azure Data Lake へのエクスポートのコンフィギュレーション - アドインのインストール](#installaddin) に記載の手順に従って、正しい Azure テナント ID が指定されていることを確認します。 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
