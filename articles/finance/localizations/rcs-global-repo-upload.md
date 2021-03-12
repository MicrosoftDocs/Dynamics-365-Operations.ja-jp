---
title: RCS で ER コンフィギュレーションを作成し、グローバル リポジトリにアップロードする
description: このトピックでは、Microsoft Regulatory Configuration Service (RCS) の電子レポート (ER) の構成を作成する方法と、グローバル レポジトリにアップロードする方法ついて説明します。
author: JaneA07
manager: AnnBe
ms.date: 09/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: ef12c911c8953b181db1c0eff0874a3d8cfcb3da
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005751"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a>Regulatory Configuration Services (RCS) で ER の構成を作成し、グローバル リポジトリにアップロードする

[!include [banner](../includes/banner.md)]

Microsoft Regulatory Configuration Service (RCS) を使用して電子レポート (ER) の構成を設計し、組織内で使えるように公開することができます。

以下の手順では、システム管理者 または電子レポートの開発者ロールを持つユーザーが、RCS インスタンスで構成された ER 構成の派生バージョンを作成し、派生する構成をグローバル リポジトリにアップロードする方法を説明します。 

この手順を完了する前に、まず以下の手順を完了する必要があります:

- RCS インスタンスへのアクセス権。
- 有効な構成プロバイダーを作成する。 詳細については、[構成プロバイダーを作成して、有効としてマークする](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md) を参照してください。

また、RCS 環境がプロビジョニングされていることを確認しておく必要があります。

1. Finance and Operations アプリで、**組織管理** \> **ワークスペース** \> **電子レポート** に移動します。
2. RCS 環境がご利用の会社にプロビジョニングされていない場合は、**Regulatory services – 外部の構成** を選択し、続いてプロビジョニングの指示に従います。

RCS 環境が既にプロビジョニングされている場合は、[サインイン] オプションを選択して、ページの URL を使用してこの機能にアクセスします。

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a>RCS で構成の派生バージョンを作成する

1. **電子レポート** ワークスペースで、ご利用の組織に対して有効な構成プロバイダーがあることを確認します。 
2. **コンフィギュレーションをレポートする** を選択します。
3. 新しいバージョンを派生させる構成を選択します。 ツリーの上にあるフィルターフィールドを使用して検索を絞り込むことができます。
4. **構成の作成** \> **名前から派生する** を選択します。
5. 名前と説明を入力し、**構成の作成** を選択して、新たな派生バージョンを作成します。
6. 新たに派生した構成を選択し、バージョンの説明を追加して、**OK** を選択します。 構成先のステータスが **完了** に変更されます。

![RCS における新たな構成のバージョン](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> 構成のステータスが変更されると、接続されているアプリケーションに関連した検証のエラーメッセージが表示される場合があります。 検証を無効にするには、**構成** タブのアクション ウィンドウで、**ユーザーパラメーター** を選択し、**設定のステータス変更時に検証をスキップしてリベースする** オプションを **はい** に設定します 

## <a name="upload-a-configuration-to-the-global-repository"></a>グローバル リポジトリに構成をアップロードする

新たな構成や派生した構成を組織と共有するには、グローバル リポジトリにアップロードします。

1. 構成の完成バージョンを選択し、**リポジトリにアップロード** を選択します。
2. **グローバル (Microsoft)** オプションを選択し、**アップロード** を選択します。

    ![リポジトリ オプションへのアップロード](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. 確認のメッセージ ボックスで、**はい** を選択します。 
4. 必要に応じてバージョンの説明を更新し、**OK** を選択します。 

構成のステータスが **共有** に更新され、構成がグローバル リポジトリにアップロードされます。 そこからは、次の方法で作業することができます:

- Dynamics 365 のインスタンスにインポートします。 詳細については、[(ER) RCS から構成をインポートする](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md) を参照してください。
- サード パーティや外部の組織と共有する場合は、[RCS 電子レポート (ER) の構成を外部組織と共有する](rcs-global-repo-share-configuration.md)を参照してください

    ![グローバル リポジトリの イントラスタット Contoso の構成バージョンが派生されました](media/RCS_Config_upload_GlobalRepo.JPG)

## <a name="delete-a-configuration-from-the-global-repository"></a>グローバル リポジトリから構成を削除する
組織で作成した構成を削除するには、次の手順を実行します。

1. **電子申告** ワークスペースで、構成プロバイダーが **アクティブ** であることを確認します。 詳細については、[構成プロバイダーを作成して、有効としてマークする](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md) を参照してください。
2. アクティブな構成プロバイダーで **リポジトリ** を選択します。
3. リポジトリ タイプ **グローバル** を選択し、**開く** を選択します。
4. **フィルター** クイック タブで、**フィルター** 機能を使用して削除する構成を見つけます。
5. **バージョン** クイック タブで、削除する構成のバージョンを選択し、**削除** を選択します。

    ![グローバル リポジトリから構成を削除する](media/RCS_Delete_from_GlobalRepo.JPG)

6. 確認のメッセージ ボックスで、**はい** を選択します。

    ![構成バージョン確認メッセージの削除](media/RCS_Delete_from_GlobalRepo_Msg.JPG)
 
構成バージョンが削除され、確認メッセージが表示されます。 

> [!NOTE]
> 構成は、作成した構成プロバイダーによってのみ削除できます。 構成が別の組織と共有されている場合、削除する前に構成の共有を解除する必要があります。
 
