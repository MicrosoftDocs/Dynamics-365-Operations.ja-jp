---
title: Lifecycle Services からのコンフィギュレーションのインポート
description: この記事では、Microsoft Dynamics Lifecycle Services (LCS) から電子申告 (ER) 構成の新しいバージョンをインポートする方法について説明します。
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
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
ms.openlocfilehash: 92c5d010430b38cb6c11a87283a2f7d4c29484f8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290367"
---
# <a name="import-a-configuration-from-lifecycle-services"></a>Lifecycle Services からのコンフィギュレーションのインポート

[!include [banner](../../includes/banner.md)]

この記事では、システム管理者または電子申告開発者の役割のユーザーが、新しいバージョンの [電子申告 (ER) 構成](../general-electronic-reporting.md#Configuration) を Microsoft Dynamics Lifecycle Services (LCS) の [プロジェクト レベルのアセット ライブラリ](../../lifecycle-services/asset-library.md) からインポートする方法について説明します。

> [!IMPORTANT]
> ER コンフィギュレーションの記憶域リポジトリとして LCS を使用することは[廃止される](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release)予定です。 詳細については、[Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) 記憶域の廃止](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md)を参照してください。

この例では、ER コンフィギュレーションの目的のバージョンを選択し、Litware, Inc. という名前のサンプル会社にインポートします。ER コンフィギュレーションは会社間で共有されるため、これらの手順はどの企業でも完了できます。 これらの手順を完了するには、まず [Lifecycle Services へのコンフィギュレーションのアップロード](er-upload-configuration-into-lifecycle-services.md) の手順を完了する必要があります。 LCS へのアクセスも必要です。

1. 次のロールの 1 つを使用してアプリケーションにサインインします。

    - 電子申告開発者
    - システム管理者

2. **組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。
3. **コンフィギュレーション** を選択します。

<a name="accessconditions"></a>
> [!NOTE]
> 現在の Dynamics 365 Finance ユーザーが、ER 構成をインポートするために [アクセス](../../lifecycle-services/asset-library.md#asset-library-support) するアセット ライブラリを含む LCS プロジェクトのメンバーであることを確認します。
>
> Finance で使用されているドメインとは異なるドメインを表す ER リポジトリから LCS プロジェクトにアクセスすることはできません。 試行すると、LCS プロジェクトの空の一覧が表示され、LCS のプロジェクト レベルのアセット ライブラリから ER コンフィギュレーションをインポートすることはできません。 ER コンフィギュレーションのインポートに使用される ER リポジトリからプロジェクト レベルのアセット ライブラリにアクセスするには、現在の Finance インスタンスがプロビジョニングされているテナント (ドメイン) に属するユーザーの資格情報を使用して Finance にサインインします。

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a>データ モデル コンフィギュレーションの共有バージョンの削除

1. **コンフィギュレーション** ページのコンフィギュレーション ツリーで、**サンプル モデルのコンフィギュレーション** を選択します。

    サンプル データ モデル コンフィギュレーションの最初のバージョンを作成し、[Lifecycle Services へのコンフィギュレーションのアップロード](er-upload-configuration-into-lifecycle-services.md) の手順を完了したときに、LCS に公開しました。 この手順では、ER コンフィギュレーションのそのバージョンを削除します。 次に、この記事の後半でそのバージョンを LCS からインポートします。

2. 一覧で、目的のレコードを見つけ、選択します。

    この例では、状態が **共有** となっているコンフィギュレーションのバージョンを選択します。 この状態は、コンフィギュレーションが LCS に公開されていることを示します。

3. **ステータスの変更** を選択します。
4. **中止** を選択します。

    選択したバージョンの状態を **共有** から **中止** に変更することにより、バージョンを削除できるようにします。

5. **OK** を選択します。
6. 一覧で、目的のレコードを見つけ、選択します。

    この例では、状態が **中止** となっているコンフィギュレーションのバージョンを選択します。

7. **削除** を選択します。
8. **はい** を選択します。

    選択されたデータ モデル コンフィギュレーションのドラフト バージョン 2 だけが使用可能になっていることを確認します。

9. ページを閉じます。

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a>データ モデル コンフィギュレーションの共有バージョンを LCS からインポートする

1. **組織管理  \> ワークスペース \> 電子申告** の順に移動します。

2. **コンフィギュレーション プロバイダー** セクションで、**Litware, Inc.** タイルを選択します。

3. **Litware, Inc.** タイルで **リポジトリ** を選択します。

    これで、Litware, Inc. のコンフィギュレーション プロバイダーのリポジトリの一覧を開くことができます。

4. **開く** を選択します。

    この例では、**LCS** リポジトリを選択して開きます。 LCS プロジェクトと選択した ER リポジトリがアクセスするアセット ライブラリへの [アクセス権](#accessconditions) が必要です。

5. 一覧で、選択された行をマークします。

    この例では、バージョンの一覧の **サンプル モデル コンフィギュレーション** の最初のバージョンを選択します。

6. **インポート** を選択します。
7. **はい** を選択して、LCS からの選択したバージョンのインポートを確認します。

    選択したバージョンが正常にインポートされたことを確認するメッセージが表示されます。

8. ページを閉じます。
9. ページを閉じます。
10. **コンフィギュレーション** を選択します。
11. ツリーで、**サンプル モデル コンフィギュレーション** を選択します。
12. 一覧で、目的のレコードを見つけ、選択します。

    この例では、状態が **共有** となっているコンフィギュレーションのバージョンを選択します。

    選択したデータ モデル コンフィギュレーションの共有バージョン 1 も使用できるようになりました。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
