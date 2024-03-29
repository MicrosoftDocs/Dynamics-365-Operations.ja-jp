---
title: Lifecycle Services へのコンフィギュレーションのアップロード
description: この記事では、新しい電子申告 (ER) の構成を作成して、Microsoft Dynamics Lifecycle Services (LCS) にアップロードする方法について説明します。
author: kfend
ms.date: 06/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
ms.openlocfilehash: 28ad20956b4b621abdb74332187d8601c10ac164
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290067"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a>Lifecycle Services へのコンフィギュレーションのアップロード

[!include [banner](../../includes/banner.md)]

この記事では、システム管理者または電子申告開発者の役割のユーザーが、新しい [電子申告 (ER) 構成](../general-electronic-reporting.md#Configuration) を作成し、Microsoft Dynamics Lifecycle Services (LCS) の [プロジェクト レベルのアセット ライブラリ](../../lifecycle-services/asset-library.md) にアップロードする方法について説明します。

> [!IMPORTANT]
> ER コンフィギュレーションの記憶域リポジトリとして LCS を使用することは[廃止される](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release)予定です。 詳細については、[Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) 記憶域の廃止](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md)を参照してください。

この例では、コンフィギュレーションを作成し、それを Litware, Inc. という名前のサンプル会社の LCS にアップロードします。ER コンフィギュレーションはすべての会社間で共有されるため、これらの手順はどの企業でも完了できます。 これらの手順を完了するには、まず [コンフィギュレーション プロバイダーを作成し、有効としてマークする](er-configuration-provider-mark-it-active-2016-11.md) の手順を完了する必要があります。 LCS へのアクセスも必要です。

1. 次のロールの 1 つを使用してアプリケーションにサインインします。

    - 電子申告開発者
    - システム管理者

2. **組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。
3. **Litware, Inc.** を選択し、**アクティブ** としてマークします。
4. **コンフィギュレーション** を選択します。

<a name="accessconditions"></a>
> [!NOTE]
> 現在の Dynamics 365 Finance ユーザーが、ER 構成をインポートするために使用される [アセット ライブラリ](../../lifecycle-services/asset-library.md#asset-library-support) を含む LCS プロジェクトのメンバーであることを確認します。
>
> Finance で使用されているドメインとは異なるドメインを表す ER リポジトリから LCS プロジェクトにアクセスすることはできません。 試行すると、LCS プロジェクトの空の一覧が表示され、LCS のプロジェクト レベルのアセット ライブラリから ER コンフィギュレーションをインポートすることはできません。 ER コンフィギュレーションのインポートに使用される ER リポジトリからプロジェクト レベルのアセット ライブラリにアクセスするには、現在の Finance インスタンスがプロビジョニングされているテナント (ドメイン) に属するユーザーの資格情報を使用して Finance にサインインします。

## <a name="create-a-new-data-model-configuration"></a>新しいデータ モデル コンフィギュレーションの作成

1. **組織管理 \> 電子申告 \> コンフィギュレーション** の順に移動します。
2. **コンフィギュレーション** ページで、**コンフィギュレーションの作成** を選択して、ドロップ ダウンのダイアログ ボックスを開きます。

    この例では、電子ドキュメントのサンプル データ モデルを含むコンフィギュレーションを作成します。 このデータ モデルのコンフィギュレーションは、LCS に後でアップロードされます。

3. **名前** フィールドに、**サンプル モデル コンフィギュレーション** と入力します。
4. **説明** フィールドに、**サンプル モデル コンフィギュレーション** と入力します。
5. **構成の作成** を選択します。
6. **モデル デザイナー** を選択します。
7. **新規** を選択します。
8. **名前** フィールドに、**エントリ ポイント** を入力します。
9. **追加** を選択します。
10. **保存** を選択します。
11. ページを閉じます。
12. **ステータスの変更** を選択します。
13. **完了** を選択します。
14. **OK** を選択します。
15. ページを閉じます。

## <a name="register-a-new-repository"></a>新しいリポジトリの登録

1. **組織管理  \> ワークスペース \> 電子申告** の順に移動します。

2. **コンフィギュレーション プロバイダー** セクションで、**Litware, Inc.** タイルを選択します。

3. **Litware, Inc.** タイルで **リポジトリ** を選択します。

    これで、Litware, Inc. のコンフィギュレーション プロバイダーのリポジトリの一覧を開くことができます。

4. **追加** をクリックして、ドロップダウン ダイアログ ボックスを開きます。

    新しいリポジトリを追加できるようになりました。

5. **コンフィギュレーション リポジトリ入力** フィールドに、**LCS** を選択します。
6. **レポジトリを作成** を選択します。
7. **プロジェクト** フィールドで値を入力または選択します。

    この例の場合、目的の LCS プロジェクトを選択します。 プロジェクトに [アクセス](#accessconditions) できる必要があります。

8. **OK** を選択します。

    新しいリポジトリ エントリを完了します。

9. 一覧で、選択された行をマークします。

    この例の場合、**LCS** リポジトリ レコードを選択します。

    登録されているリポジトリが現在のプロバイダーによってマークされていることを確認します。 つまり、そのプロバイダーが所有するコンフィギュレーションのみをこのリポジトリに配置し、選択した LCS プロジェクトにアップロードできます。

10. **開く** を選択します。

    ER コンフィギュレーションの一覧を表示するためにリポジトリを開きます。 選択したプロジェクトが ER コンフィギュレーションの共有に使用されていない場合、一覧は空になります。

11. ページを閉じます。
12. ページを閉じます。

## <a name="upload-a-configuration-into-lcs"></a>LC へコンフィギュレーションをアップロードする

1. **組織管理 \> 電子申告 \> コンフィギュレーション** の順に移動します。
2. **コンフィギュレーション** ページのコンフィギュレーション ツリーで、**サンプル モデルのコンフィギュレーション** を選択します。

    すでに完了している作成済みのコンフィギュレーションを選択する必要があります。

3. 一覧で、目的のレコードを見つけ、選択します。

    この例の場合、状態が **完了** となっている選択したコンフィギュレーションのバージョンを選択します。

4. **ステータスの変更** を選択します。
5. **共有** を選択します。

    コンフィギュレーションが LCS で公開されると、コンフィギュレーションの状態が **完了** から **共有** に変更されます。

6. **OK** を選択します。
7. 一覧で、目的のレコードを見つけ、選択します。

    この例の場合、状態が **共有** となっているコンフィギュレーションのバージョンを選択します。

    選択したバージョンの状態が **完了** から **共有** に変更されたことに注意してください。

8. ページを閉じます。
9. **リポジトリ** を選択します。

    これで、Litware, Inc. のコンフィギュレーション プロバイダーのリポジトリの一覧を開くことができます。

10. **開く** を選択します。

    この例では、**LCS** リポジトリを選択して開きます。

    選択したコンフィギュレーションが、選択した LCS プロジェクトのアセットとして表示されることを確認します。

11. <https://lcs.dynamics.com> に移動して LCS を開きます。
12. 以前にリポジトリの登録に使用したプロジェクトを開きます。
13. プロジェクトのアセット ライブラリを開きます。
14. **GER コンフィギュレーション** アセット タイプを選択します。

    アップロードした ER コンフィギュレーションがリストされます。

    プロバイダーがこの LCS プロジェクトにアクセスできる場合に、アップロードされた LCS コンフィギュレーションは、別のインスタンスにインポートできることに注意してください。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
