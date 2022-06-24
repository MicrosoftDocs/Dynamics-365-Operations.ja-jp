---
title: Lifecycle Services の電子申告コンフィギュレーションのダウンロード
description: この記事は、Microsoft Dynamics Lifecycle Services (LCS) から電子申告 (ER) のコンフィギュレーションをダウンロードする方法を説明します。
author: NickSelin
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8ba720f997981e85ea08d532f23341a838533ac4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885297"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Lifecycle Services の電子申告コンフィギュレーションのダウンロード

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics Lifecycle Services (LCS) の [共有アセット ライブラリ](../lifecycle-services/asset-library.md) から最新バージョンの [電子申告 (ER) コンフィギュレーション](general-electronic-reporting.md#Configuration) をダウンロードする方法について説明します。

> [!IMPORTANT]
> ER コンフィギュレーションの記憶域リポジトリとして LCS を使用することは[廃止される](../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release) 予定です。 詳細については、[Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) 記憶域の廃止](../../../finance/localizations/rcs-lcs-repo-dep-faq.md) を参照してください。

1. 次のロールの 1 つを使用してアプリケーションにサインインします。

    - 電子申告開発者
    - 電子申告機能コンサルタント
    - システム管理者

2. **組織管理** &gt; **ワークスペース** &gt; **電子申告** の順に移動します。
3. **コンフィギュレーション プロバイダー** セクションで、**Microsoft** タイルを選択します。
4. **Microsoft** タイルで **リポジトリ** を選択します。

    [![ローカライズ コンフィギュレーション ページ の Microsoft タイル。](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)

5. **コンフィギュレーション リポジトリ** ページのグリッドで、**LCS** タイプの既存のリポジトリを選択します。 このリポジトリがグリッドに表示されない場合は、次の手順に従います。

    1. **追加** を選択して、リポジトリを追加します。
    2. リポジトリ タイプとして、**LCS** を選択します。
    3. **レポジトリを作成** を選択します。
    4. 認証についてのメッセージが表示された場合は、画面の指示に従います。
    5. リポジトリの名前と説明を入力します。
    6. **OK** を選択して、新しいリポジトリ エントリを確認します。
    7. グリッドで、**LCS** タイプの新しいリポジトリを選択します。

6. **開く** を選択して、選択したリポジトリの ER コンフィギュレーションの一覧を表示します。

    [![コンフィギュレーション レポジトリ ページ。](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)

    > [!TIP]
    > LCS の共有アセット ライブラリからコンフィギュレーションをダウンロードするのに、LCS リポジトリへのアクセスに問題がある場合は、代わりに [グローバル リポジトリ](er-download-configurations-global-repo.md) からコンフィギュレーションをダウンロードできます。

7. 左側ペインのコンフィギュレーション ツリーで必要な ER コンフィギュレーションを選択します。
8. **バージョン** クイック タブで、選択した ER コンフィギュレーションの必要なバージョンを選択します。
9. **インポート** を選択して、LCS から現在のインスタンスに選択したバージョンをダウンロードします。

    > [!NOTE]
    > **インポート** ボタンは、現在のインスタンスにある ER コンフィギュレーション バージョンでは使用できません。

    [![コンフィギュレーション レポジトリ ページ。](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

> [!NOTE]
> ER の設定に応じて、コンフィギュレーションはインポートされた後に検証されます。 不整合の問題が検出されると、通知を受け取る場合があります。 インポートしたコンフィギュレーションのバージョンを使用する前に、それらの問題を解決する必要があります。 詳細については、この記事の関連トピックの一覧を参照してください。

## <a name="additional-resources"></a>追加リソース

[電子申告 (ER) の概要](general-electronic-reporting.md)

[ER コンフィギュレーションをコンフィギュレーション サービスのグローバル リポジトリからダウンロードする](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
