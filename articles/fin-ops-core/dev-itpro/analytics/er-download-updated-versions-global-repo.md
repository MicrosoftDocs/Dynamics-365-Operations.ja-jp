---
title: ER コンフィギュレーションの更新バージョンのインポート
description: この記事では、構成サービスのグローバル リポジトリから電子申告 (ER) 構成の更新済バージョンをインポートする方法について説明します。
author: NickSelin
ms.date: 06/09/2020
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
ms.openlocfilehash: 69eaa3e2ecfbd1e92f23725d97d7fa9f0abe1cea
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847549"
---
# <a name="import-updated-versions-of-er-configurations"></a>ER コンフィギュレーションの更新バージョンのインポート

[!include [banner](../includes/banner.md)]

電子レポート (ER) [リポジトリ](general-electronic-reporting.md#Repository) は、[ER コンフィギュレーション](general-electronic-reporting.md#Configuration) を共有するために使用されます。 異なるリポジトリから Microsoft Dynamics 365 Finance のインスタンスに ER 構成を [インポート](download-electronic-reporting-configuration-lcs.md) できます。 ER コンフィギュレーションをインポートする場合、[コンフィギュレーション プロバイダー](general-electronic-reporting.md#Provider) は、新しい[バージョン](general-electronic-reporting.md#component-versioning) のリポジトリを公開して共有できるようになります。

この記事では、構成サービスのグローバル リポジトリから ER 構成の更新済バージョンをインポートする方法について説明します。 詳細については、[Microsoft Dynamics 365 for Finance and Operations - Regulatory services、コンフィギュレーション サービス](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration) を参照してください。

## <a name="review-the-available-updated-versions"></a>利用可能な更新済バージョンを確認する

1. 次のロールの 1 つを使用して Finance にサイン インします:

    - 電子申告開発者
    - 電子申告機能コンサルタント
    - システム管理者

2. **組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。
3. **ローカライズ構成** ページの、**関連リンク** セクションで、**コンフィギュレーション バージョンの更新をインポート** を選択します。

    ![ローカライズ コンフィギュレーション ページ。](./media/er-download-updated-versions-global-repo1.png)

4. **電子レポート コンフィギュレーション バージョンの更新をインポート** ダイアログ ボックスの **実行モード** フィールドで、**使用可能な更新のみ表示** を選択します。 その後、**OK** を選択します。 

    ![実行モード フィールドを使用可能な更新のみに設定。](./media/er-download-updated-versions-global-repo2.png)

5. 受信したメッセージを確認します。 これらのメッセージは、現在の Finance インスタンス ER コンフィギュレーションに関する次の情報を提供し、それがグローバル リポジトリのコンテンツとどのように比較されるかを示します。

    - ER コンフィギュレーションの合計数
    - グローバル リポジトリに存在しない ER コンフィギュレーション
    - 現在の Finance インスタンスで最新バージョンが既に利用可能な ER コンフィギュレーション (これらの ER コンフィギュレーションの完全な一覧を表示するには、**メッセージの詳細** リンクを選択します。)

        ![「次のコンフィギュレーションの最新バージョンは既にインポートされています」というメッセージおよびメッセージの詳細](./media/er-download-updated-versions-global-repo3.png)

    - 最新バージョンがグローバル リポジトリで利用可能で、現在の Finance インスタンスにインポート可能な ER コンフィギュレーション (これらの ER コンフィギュレーションの完全な一覧を表示するには、**メッセージの詳細** リンクを選択します。)

        ![「使用可能な更新」というメッセージおよびメッセージの詳細](./media/er-download-updated-versions-global-repo4.png)

## <a name="import-available-updated-versions"></a>利用可能な更新済バージョンをインポートする

1. 次のロールの 1 つを使用して Finance にサイン インします:

    - 電子申告開発者
    - 電子申告機能コンサルタント
    - システム管理者

2. **組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。
3. **ローカライズ構成** ページの、**関連リンク** セクションで、**コンフィギュレーション バージョンの更新をインポート** を選択します。
4. **電子レポート コンフィギュレーションのバージョンをインポート** ダイアログ ボックスの **実行モード** フィールドで、**最新の更新プログラムをインポート** を選び、ER コンフィギュレーションの最新バージョンをグローバル リポジトリから現在の Finance インスタンスにインポートします。
5. インポートに対してバッチ ジョブをスケジュールするには、**バックグラウンドで実行** クイックタブで、**バッチ処理** オプションを **はい** に設定します。 定期的にインポートを繰り返したい場合は、必要な繰り返しをコンフィギュレーションします。

    ![最新の更新プログラムをインポートするように設定された実行モード フィールド。](./media/er-download-updated-versions-global-repo5.png)

6. **OK** を選択します。
7. インポートされたコンフィギュレーション バージョンを調べるには、次の手順のいずれかを実行します:

    - バッチ ジョブを使用する代わりにインポートを対話的に実行する場合は、受信したメッセージを確認します。

        ![対話型のインポート実行中に受信したメッセージ。](./media/er-download-updated-versions-global-repo6.png)

    - バッチ モードでインポートを実行する場合は、次の手順を実行します:

        1. **共通** \> **照会** \> **バッチ ジョブ** \> **私のバッチ ジョブ** の順に移動します。
        2. **電子レポート コンフィギュレーション バージョンのインポート** ジョブを検索および選択し、アクション ウィンドウの **バッチ ジョブ** タブで、**バッチ ジョブの履歴経歴** を選びジョブの履歴を表示します。
        3. **バッチ ジョブの履歴** ページで **ログ** を選択します。 次に、受信したメッセージで、**メッセージの詳細** リンクを選びジョブ ログを表示します。

        ![ジョブ ログ。](./media/er-download-updated-versions-global-repo7.png)

> [!IMPORTANT]
> 定期的なバッチ ジョブのスケジュールを設定して、更新されたバージョンの ER コンフィギュレーションを運用環境にインポートすることをお勧めします。この場合、インポートされたバージョンをすぐに使用できます。 代わりに、ER コンフィギュレーションのバージョンをサンドボックス環境に配置するには、この方法を使用します。 これにより、運用環境に配置する前に、サンドボックス環境で評価することができます。

## <a name="additional-resources"></a>追加リソース

- [電子申告 (ER) の概要](general-electronic-reporting.md)
- [ER コンフィギュレーションをコンフィギュレーション サービスのグローバル リポジトリからダウンロードする](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]