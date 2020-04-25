---
title: Azure Data Lake の Finance and Operations アプリ データ
description: このトピックでは、Data Lakeを実装した Finance and Operations アプリ環境の設定方法を説明します。
author: MilindaV2
manager: AnnBe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 96283
ms.assetid: ''
ms.search.region: Global
ms.author: milindav
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: Platform Update 34
ms.openlocfilehash: ee5ad6d1ed6820f9fa30ef7cf3f451ce3490eed6
ms.sourcegitcommit: 88347d0f0ac862a77f269a05f1801d30dc93586e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2020
ms.locfileid: "3260242"
---
# <a name="finance-and-operations-apps-data-in-azure-data-lake"></a>Azure Data Lake の Finance and Operations アプリ データ

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

**Azure Data Lake にエクスポート** 機能を使用すると、Finance and Operations アプリ環境で Data Lake を使用するように構成することができます。 構成が完了すると、Data Lake には Finance and Operations アプリのテーブルとエンティティが反映されます。

> [!NOTE]
> - **この機能は、すべての地域またはすべての環境で使用できるわけではありません。** この機能がご利用の環境で表示されない場合、当機能は未対応です。
> - Data Lakeで集計測定を使用できるようにするには、[エンティティ ストアを Data Lake として使用可能とする](entity-store-data-lake.md)で説明されている方法でこの機能を引き続き使用します。

## <a name="overview"></a>概要

このサービスを利用可能とするプロセスには、いくつかの手順があります。

1. サブスクリプションに Microsoft Azure Data Lake Storage Gen2 アカウント (ストレージアカウント) を作成します。
2. Azure Data Lake 統合を有効にするには、利用規約に同意してください。
3. **Azure Data Lake へのエクスポート** 機能を有効にします。
4. データ（Data Lake にステージングする必要のあるテーブルとエンティティ）を選択します 。
5. Data Lake のテーブルを監視します。

## <a name="create-a-data-lake-storage-gen2-account-in-your-subscription"></a>サブスクリプションに Data Lake ストレージ（Gen2）を作成します

ストレージ アカウントはデータの格納に使用されます。 ストレージ アカウントを手動で作成するには、Azure サブスクリプションに対して管理者権限を持つユーザーである必要があります。 （最終的には、システムがユーザーに代わって自身の Azure サブスクリプションにストレージ アカウントを作成することができます）

### <a name="manually-create-a-storage-account"></a>ストレージ アカウントの手動作成

ご利用の Azure サブスクリプションにストレージ アカウントを作成し、Key Vault を使用してそのアカウントをシステムに提供することができます。 続いて、ストレージ アカウントのルートへのアクセスを許可するAzure Active Directory (Azure AD) のアプリケーション ID を作成する必要があります。 システムでは、Azure AD アプリケーションを使用して、フォルダ構造の作成とデータの書き込みを行います。 最後に、サブスクリプションに Key Vault を作成し、ストレージ アカウントに関する情報と、Microsoft Dynamics Lifecycle Services (LCS) の Data Lake 条件に同意してください。

1. ストレージ アカウントを作成する。 手順については、[ストレージ アカウントの作成](entity-store-data-lake.md#create-storage-accounts) を参照してください。
2. ご利用の Azure AD 環境のテナント ID を入力します。 Azure AD テナント ID は Azure ポータルで確認できます。 Azure portal にログインし、**Azure Active Directory** サービスを開きます。 **プロパティ** ページを開き、**ディレクトリ ID** フィールドの値をコピーします。
3. Key Vault とシークレットを作成します。 手順については、 [Key Vault とシークレットを作成する](entity-store-data-lake.md#create-a-key-vault-and-a-secret)。 Key Vault のドメイン名システム (DNS) 名と秘密名を入力する必要があります。

<!--### Let the system create a storage account -->

<!--Instead of manually creating a storage account, you can have the system create a storage account in your own subscription on your behalf. This option will be made available in a future release. -->

## <a name="accept-the-offer-and-terms-to-turn-on-the-data-lake-integration"></a>Data Lake 統合を有効にするには、利用規約に同意してください

Data Lake 統合を構成するには、LCS の Data Lake の規約に同意する必要があります。 このタスクを完了するには、Finance and Operations アプリの環境管理者である必要があります。また、LCS ポータルにアクセスできる必要があります。

1. [LCS](https://lcs.dynamics.com) にサインインします。
2. **環境** ページで、**環境のアドイン** クイック タブを選択します。 **Azure Data Lake** が一覧に表示されている場合は、Data Lake アドインが既にインストールされているため、この手順の残りの部分は省略できます。 それ以外の場合は、残りの手順に従って Data Lake アドインをインストールしてください。

    ![Data Lake アドインがインストールされていることを確認する](./media/LCS-EnvironmentPage-with-Addins.png)

3. **新しいアドインのインストール**を選択します。
4. **インストールするアドインの選択**ダイアログ ボックスで、一覧から **Azure Data lake** を選択します。 表示されない場合は、環境に対して当機能が未対応となっている可能性があります。

    ![Azure Data Lake のオプションを選択する](./media/LCS-EnvironmentPage-with-DataLake-Flyover.png)

5. **設定のアドイン** ダイアログ ボックスで、必要な情報を入力します。 質問に答えるには、既にストレージ アカウントが作成されている必要があります。 ストレージ アカウントをまだ持っていない場合は、作成するか、管理者にアカウントの作成代行を依頼してください。

    ![Data Lake アドインの詳細を入力する](./media/azure-data-lake-addin.png)

6. チェック ボックスをオンにしてサービス条件を承認し、**インストール** を選択します。

システムが、ご利用の環境に Data Lake をインストールし構成します。 インストールと構成が完了すると、 **環境** のページに **Azure Data Lake** の一覧が表示されます。

## <a name="turn-on-the-export-data-to-azure-data-lake-feature"></a>Azure Data Lake へのデータのエクスポート機能を有効にします

Finance and Operations アプリのすべての新機能については、管理者は事前に **Azure Data Lake へのエクスポート** 機能を有効化しておく必要があります。

- **機能の管理** ワークスペースにて、**Azure Data Lake にデータをエクスポート** 機能を選択し、**有効化** を選択します。

この機能を有効にすると、**システムの管理** の配下に **Azure Data Lake にエクスポートする** オプションが表示されます。

## <a name="select-data"></a>データの選択

Data Lake にステージングする必要のあるテーブルとエンティティを選択することができます 。

1. ご利用の環境で、**システム管理** \> **Azure Data Lake にエクスポートする** へと移動します。
2. **Data Lake にエクスポートするデータフィードの構成** を選択します。
3. **Data Lakeへのデータフィードの構成** ページの **テーブルの選択** ページで、Data Lake にステージングするデータ テーブルを選択します。 テーブルは、表示名またはシステム名で検索できます。 テーブルが既に同期されているかどうかを確認することもできます。 完了後に、**テーブルの追加** を選択し、選択したテーブルを Data Lake に追加します。

    ![テーブルの選択](./media/Export-Tables-toData-lake-unselected.png)

    また、必要な特定のテーブルについて詳しくない場合は、エンティティを使用してテーブルを選択できます。 エンティティはデータの抽象度が高く、複数のテーブルを含む場合があります。 エンティティを選択することで、それを構成するテーブルも選択することになります。
    
    - **使用するエンティティの選択** タブでエンティティを選択し、**エンティティを使用してテーブルを追加する** を選択します。

    ![エンティティを使用したテーブルの選択](./media/Export-Entities-toData-lake-unselected.png)

    テーブルを選択する方法を問わず、Data Lake ではテーブルがステージングされます。

## <a name="monitor-the-tables-in-data-lake"></a>Data Lake のテーブルを監視する

システムが Data Lake でデータの更新を維持しているため、データのエクスポートの監視や、スケジュールを設定する必要はありません。 ただし、**Data Lake へのデータフィードの設定** ページの **アクティブ** タブで、進行中のデータ エクスポートの状態を確認することができます。

![テーブルの監視の進行状況](./media/Export-Tables-toData-lake-monitor.png)
