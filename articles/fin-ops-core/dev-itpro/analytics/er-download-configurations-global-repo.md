---
title: ER コンフィギュレーションをコンフィギュレーション サービスのグローバル リポジトリからダウンロードする
description: この記事では、構成サービスのグローバル リポジトリから電子申告 (ER) 構成をダウンロードする方法について説明します。
author: NickSelin
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 4386e8fdbb2856d14d5b47ee5ab416c8d58b8d63
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891907"
---
# <a name="download-er-configurations-from-the-global-repository-of-configuration-service"></a>ER コンフィギュレーションをコンフィギュレーション サービスのグローバル リポジトリからダウンロードする

[!include [banner](../includes/banner.md)]

この記事では、構成サービスのグローバル リポジトリから [電子申告 (ER) 構成](general-electronic-reporting.md#Configuration) をダウンロードする方法について説明します。 詳細については、[Microsoft Dynamics 365 for Finance and Operations - Regulatory services、コンフィギュレーション サービス](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration) を参照してください。

## <a name="open-configurations-repository"></a>コンフィギュレーション リポジトリを開く

1. 次のロールの 1 つを使用して Dynamics 365 Finance アプリケーションにサインインします。

    - 電子申告開発者
    - 電子申告機能コンサルタント
    - システム管理者

2. **組織管理 > ワークスペース > 電子申告** の順に移動します。
3. **コンフィギュレーション プロバイダー** セクションで、**Microsoft** タイルを選択します。
3. **Microsoft** タイルで **リポジトリ** を選択します。

    ![電子申告ワークスペース。](./media/er-download-configurations-global-repo-er-workspace.png)

4. **コンフィギュレーション リポジトリ** ページのグリッドで、**グローバル** タイプの既存のリポジトリを選択します。 このリポジトリがグリッドに表示されない場合は、次の手順に従います。

    1. **追加** を選択して新しいリポジトリを追加します。
    2. リポジトリ タイプとして **グローバル** を選択し、**リポジトリの作成** を選択します。
    3. メッセージが表示されたら、承認の指示に従います。
    4. リポジトリの名前と説明を入力し、**OK** を選択して、新しいリポジトリのエントリを確認します。
    5. グリッドで、**グローバル** タイプの新しいリポジトリを選択します。

5. **開く** を選択して、選択したリポジトリの ER コンフィギュレーションの一覧を表示します。

    ![コンフィギュレーション レポジトリ ページ。](./media/er-download-configurations-global-repo-repositories-list.png)

## <a name="import-a-single-configuration"></a>単一のコンフィギュレーションをインポートする

1. **コンフィギュレーション リポジトリ** ページの コンフィギュレーション ツリーで、必要な ER コンフィギュレーションを選択します。
2. **バージョン** クイック タブで、選択した ER コンフィギュレーションの必要なバージョンを選択します。
3. **インポート** を選択して、グローバル リポジトリから現在の Finance インスタンスに選択したバージョンをダウンロードします。

    > [!NOTE]
    > **インポート** ボタンは、現在の Finance インスタンスにある ER コンフィギュレーション バージョンでは使用できません。

    ![構成リポジトリ ページ (構成 FastTab)。](./media/er-download-configurations-global-repo-repository-content.png)

## <a name="import-filtered-configurations"></a>フィルター処理されたコンフィギュレーションをインポートする

1. **コンフィギュレーション リポジトリ** ページの コンフィギュレーション ツリーで、**フィルター** クイック タブを展開します。
2. **タグ** グリッドで、必要なタグを追加します。
3. **国/地域の適用性** フィールドで、適切な国/地域コードを選択し、**フィルターの適用** を選択します。

    > [!NOTE]
    > **コンフィギュレーション** クイック タブには、指定した選択条件を満たすコンフィギュレーションがすべて表示されます。

4. **コンフィギュレーション** クイック タブで、**インポート** を選択し、フィルタ処理されたコンフィギュレーションをグローバル リポジトリから現在のインスタンスにダウンロードします。
5. **コンフィギュレーション** クイック タブで、**フィルタのリセット** を選択し、指定された選択条件をクリーンアップします。

    ![構成リポジトリ ページ (Versions FastTab、インポート ボタン)。](./media/er-download-configurations-global-repo-filtered-configurations.png)

> [!NOTE]
> ER の設定に応じて、コンフィギュレーションはインポートされた後に検証されます。 不整合の問題が検出されると、通知を受け取る場合があります。 インポートしたコンフィギュレーションのバージョンを使用する前に、問題を解決する必要があります。 詳細については、この記事の関連リソースの一覧を参照してください。

> [!NOTE]
> ER コンフィギュレーションは、他のコンフィギュレーションに依存するようにコンフィギュレーションできます。 したがって、選択したコンフィギュレーションに加えて、他のコンフィギュレーションが自動的にインポートされる場合があります。 コンフィギュレーションの依存関係の詳細については、[他のコンポーネントに対する ER コンフィギュレーションの依存関係を定義する](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md) を参照してください。

## <a name="additional-resources"></a>追加リソース

[電子申告 (ER) の概要](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
