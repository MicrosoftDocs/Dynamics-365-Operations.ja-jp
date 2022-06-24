---
title: 外部組織で RCS/グローバル レポジトリの ER 構成を共有する
description: この記事では、Microsoft Regulatory Configuration Services (RCS) 、またはグローバル レポジトリの電子レポート (ER) の構成を外部組織と直接共有する方法について説明します。
author: JaneA07
ms.date: 05/04/2020
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
ms.openlocfilehash: 976a86aee75581d1afa764bea049b6c0eaecf9f3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888926"
---
# <a name="share-electronic-reporting-er-configurations-in-regulatory-configuration-services-rcs-global-repository-with-external-organizations"></a>Microsoft Regulatory Configuration Service (RCS) のグローバル レポジトリの電子レポート (ER) の構成を外部組織と共有する

[!include [banner](../includes/banner.md)]

Microsoft Regulatory Configuration Service (RCS) を使用すると、電子レポート (ER) の構成を共有して外部組織に公開することができます。

次の手順では、RCS のユーザーが RCS インスタンスで設定された ER 構成のバージョンを外部組織と共有する方法を説明します。 この手順を完了する前に、まず以下の手順を完了する必要があります:

- RCS インスタンスへのアクセス権。
- 有効な構成プロバイダーを作成する。 詳細については、[構成プロバイダーを作成して、有効としてマークする](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md) を参照してください。
- ER 構成の新しいバージョンを作成してアップロードします。 詳細については、[新しいバージョンの電子レポート (ER) 構成の作成とアップロード](rcs-global-repo-upload.md)を参照してください。

また、RCS 環境がプロビジョニングされていることを確認しておく必要があります。

1. Finance and Operations アプリで、**組織管理** \> **ワークスペース** \> **電子レポート** の順に移動します。
2. RCS 環境がご利用の会社にプロビジョニングされていない場合は、**Regulatory services – 外部の構成** を選択し、続いてプロビジョニングの指示に従います。

RCS 環境が既にプロビジョニングされている場合は、[サインイン] オプションを選択して、ページの URL を使用してこの機能にアクセスします。

## <a name="verify-the-configuration-that-you-want-to-share"></a>共有する構成を確認する

共有する構成が既にグローバル リポジトリにアップロードされていることを確認するには、次の手順に従います。

1. **電子レポート** ワークスペースで、超す営プロバイダーの **リポジトリ** を選択します。

    ![コンフィギュレーション提供者。](media/1_RCS_Repo_for_config_provider.JPG)

2. **グローバル リポジトリ** \>**開く** を選択します。
3. 共有する構成を検索します。 フィルターのフィールドを使用して検索を絞り込むことができます。 グローバル リポジトリに構成が見つからない場合は、[新しいバージョンの電子レポート (ER) 構成の作成とアップロード](rcs-global-repo-upload.md)に記載の手順に従ってください。

## <a name="share-er-configurations-with-external-organizations"></a>ER の構成を外部の組織と共有する

構成プロバイダーの配下に構成が作成された後は、**グローバル構成リポジトリ** ページの **共有** クイックタブを使用して外部組織と直接共有することができます。

1. **電子レポート** ワークスペースで、超す営プロバイダーの **リポジトリ** を選択します。
2. **グローバル リポジトリ** \>**開く** を選択します。 
3. 共有する構成を選択します。
4. **共有** クイック タブで、**組織** を選択します。

    ![クイック タブで共有する。](media/1_RCS_Repo_for_Share_with_org.JPG)

5. ダイアログ ボックスで、外部組織のドメイン名を入力し、**OK** を選択し ます。

    ![外部組織との構成バージョンを共有するダイアログ ボックス。](media/1_RCS_Repo_for_Share_with_form.JPG)

構成が外部組織と共有され、その組織ではグローバルリポジトリで利用できるようになります。 そこから RCS の組織のインスタンスにインポートをする、または組織の財務と運用アプリのインスタンスにインポートすることができます。

6. 外部組織と既に共有されている構成の共有を解除するには、構成を選択して **共有解除** をクリックし、**OK** をクリックします


[!INCLUDE[footer-include](../../includes/footer-banner.md)]