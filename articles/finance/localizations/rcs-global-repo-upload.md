---
title: RCS で ER コンフィギュレーションを作成し、グローバル リポジトリにアップロードする
description: この記事では、Microsoft Regulatory Configuration Services (RCS) の電子レポート (ER) の構成を作成する方法と、グローバル レポジトリにアップロードする方法ついて説明します。
author: JaneA07
ms.date: 01/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 8cfbcfea3c6056d87eb600c9a2f9e0d1727c30ff
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894746"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a>Regulatory Configuration Services (RCS) で ER の構成を作成し、グローバル リポジトリにアップロードする

[!include [banner](../includes/banner.md)]

Microsoft Regulatory Configuration Service (RCS) を使用して電子レポート (ER) の構成を設計し、組織内で使えるように公開することができます。

以下の手順では、システム管理者 または電子レポートの開発者ロールを持つユーザーが、RCS インスタンスで構成された ER 構成の派生バージョンを作成し、派生する構成をグローバル リポジトリにアップロードする方法を説明します。 

この手順を完了する前に、まず以下の手順を完了する必要があります:

- 組織の RCS環境 にアクセスできます。
- 有効な構成プロバイダーを作成し、アクティブにします。 詳細については、[構成プロバイダーを作成して、有効としてマークする](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md) を参照してください。

また、組織用に RCS 環境がプロビジョニングされていることを確認する必要があります。 組織用に RCS インスタンスがプロビジョニングされていない場合は、次の手順で行うことができます:

1. Finance and Operations アプリで、**組織管理** \> **ワークスペース** \> **電子レポート** の順に移動します。
2. **関連リンク / 外部リンク** で、**Regulatory services - 構成** を選択し、指示に従って **サインアップ** してプロビジョニングします。

RCS 環境が既に組織用にプロビジョニングされている場合は、ページの URL を使用してアクセスし、**サインイン** オプションを選択します。

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a>RCS で構成の派生バージョンを作成する

> [!NOTE]
> RCS を初めて使用する場合は、派生させるために使用できる構成はありません。 グローバル リポジトリから構成をインポートする必要があります。 詳細については、[ER コンフィギュレーションをコンフィギュレーション サービスのグローバル リポジトリからダウンロードする](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)を参照してください。

1. RCS に **サインイン** し、**電子レポート** ワークスペースを選択します。
2. 組織用の有効な構成プロバイダーがアクティブに設定されていることを確認します (前提条件を参照)。 
3. **コンフィギュレーションをレポートする** を選択します。
4. 新しいバージョンを派生させる構成を選択します。 ツリーの上にあるフィルターフィールドを使用して検索を絞り込むことができます。
5. **構成の作成** \> **名前から派生する** を選択します。
6. 名前と説明を入力し、**構成の作成** を選択して、'ドラフト' ステータスの新たな派生バージョンを作成します。
7. 新しく派生した構成を選択し、必要に応じて構成形式をさらに変更します。 
8. 変更が完了したら、構成の **ステータスの変更** を **完了** に設定して、リポジトリに公開できるようにする必要があります。  **OK** を選択します。

![RCS における新たな構成のバージョン。](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> 構成のステータスが変更されると、接続されているアプリケーションに関連した検証のエラーメッセージが表示される場合があります。 検証を無効にするには、**構成** タブのアクション ウィンドウで、**ユーザーパラメーター** を選択し、**設定のステータス変更時に検証をスキップしてリベースする** オプションを **はい** に設定します 

## <a name="upload-a-configuration-to-the-global-repository"></a>グローバル リポジトリに構成をアップロードする

新規または派生した構成を組織と共有するには、次の手順に従ってグローバル リポジトリにアップロードします:

1. 構成の完成バージョンを選択し、**リポジトリにアップロード** を選択します。
2. **グローバル (Microsoft)** オプションを選択し、**アップロード** を選択します。

    ![リポジトリ オプションへのアップロード。](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. 確認のメッセージ ボックスで、**はい** を選択します。 
4. 必要に応じてバージョンの説明を更新し、**OK** を選択します。 必要に応じて、接続されているアプリケーションまたは GIT リポジトリにバージョンをアップロードすることもできます。  

構成のステータスが **共有** に更新され、構成がグローバル リポジトリにアップロードされます。 アップロードした構成のドラフト バージョンも作成され、後続の変更が必要な場合に使用できます。

グローバル リポジトリに構成をアップロードした後、次の方法でその構成を使用できます:

- Dynamics 365 のインスタンスにインポートします。 詳細については、[(ER) RCS から構成をインポートする](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md) を参照してください。
- サード パーティや外部の組織と共有する場合は、[RCS 電子レポート (ER) の構成を外部組織と共有する](rcs-global-repo-share-configuration.md)を参照してください

    ![グローバル リポジトリの イントラスタット Contoso の構成バージョンが派生されました。](media/RCS_Config_upload_GlobalRepo.JPG)

## <a name="delete-a-configuration-from-the-global-repository"></a>グローバル リポジトリから構成を削除する
組織で作成した構成を削除するには、次の手順を実行します。

1. **電子申告** ワークスペースで、構成プロバイダーが **アクティブ** であることを確認します。 詳細については、[構成プロバイダーを作成して、有効としてマークする](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md) を参照してください。
2. アクティブな構成プロバイダーで **リポジトリ** を選択します。
3. リポジトリ タイプ **グローバル** を選択し、**開く** を選択します。
4. **フィルター** クイック タブで、**フィルター** 機能を使用して削除する構成を見つけます。
5. **バージョン** クイック タブで、削除する構成のバージョンを選択し、**削除** を選択します。

    ![グローバル リポジトリから構成を削除する。](media/RCS_Delete_from_GlobalRepo.JPG)

6. 確認のメッセージ ボックスで、**はい** を選択します。

    ![構成バージョン確認メッセージの削除。](media/RCS_Delete_from_GlobalRepo_Msg.JPG)
 
構成バージョンが削除され、確認メッセージが表示されます。 

> [!NOTE]
> 構成は、作成した構成プロバイダーによってのみ削除できます。 構成が別の組織と共有されている場合、削除する前に構成の共有を解除する必要があります。
 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
