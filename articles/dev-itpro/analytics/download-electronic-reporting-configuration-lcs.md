---
title: "Lifecycle Services の電子申告コンフィギュレーションのダウンロード"
description: "このトピックは、Microsoft Dynamics Lifecycle Services (LCS) から電子申告 (ER) のコンフィギュレーションをダウンロードする方法を説明します。"
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8fae33fbe2d1433e4263ed4087dad2bc894e0b84
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Lifecycle Services の電子申告コンフィギュレーションのダウンロード

[!include[banner](../includes/banner.md)]


このトピックは、Microsoft Dynamics Lifecycle Services (LCS) から電子申告 (ER) のコンフィギュレーションをダウンロードする方法を説明します。

このチュートリアル ガイドは Microsoft Dynamics Lifecycle Services (LCS) から Electronic reporting (ER) コンフィギュレーションの最新バージョンをダウンロードするプロセスを説明します。

1.  次のロールの 1 つを使用して Dynamics 365 for Finance and Operations にサインインします。
    -   電子申告開発者
    -   電子申告機能コンサルタント
    -   システム管理者

2.  [**組織管理**] &gt; [**電子申告**] の順に移動します。
3.  [**コンフィギュレーション プロバイダー**] セクションで、[**Microsoft**] タイルを選択します。
4.  [**Microsoft**] タイルで [**リポジトリ**] をクリックします。 [![MS オープン MS リポジトリ リスト用 LCS からの ER 更新](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)
5.  **コンフィギュレーション リポジトリ** ページのグリッドで、**LCS** タイプの既存のリポジトリを選択します。 このリポジトリがグリッドに表示されない場合は、次の手順に従います。
    1.  [**追加**] をクリックして新しいリポジトリを追加します。
    2.  リポジトリ タイプとして、[**LCS**] を選択します。
    3.  [**リポジトリの作成**] をクリックします。
    4. メッセージが表示されたら、承認の指示に従います。
    5.  リポジトリの名前と説明を入力します。
    6.  [**OK**] をクリックして、新しいリポジトリ エントリを確認します。
    7.  グリッドで、[**LCS**] タイプの新しいリポジトリを選択します。

6.  [**開く**] をクリックして、選択したリポジトリの ER コンフィギュレーションの一覧を表示します。 [![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)
7.  左ウィンドウのコンフィギュレーション ツリーで必要な ER コンフィギュレーションを選択します。
8.  [**バージョン**] クイック タブで、選択した ER コンフィギュレーションの必要なバージョンを選択します。
9.  [**インポート**] をクリックして、LCS から現在の Finance and Operations インスタンスに選択したバージョンをダウンロードします。 **注:** [**インポート**] ボタンは、現在の Finance and Operations インスタンスにある ER コンフィギュレーション バージョンでは使用できません。 [![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

**注:** ER の設定に応じて、コンフィギュレーションはインポートされた後に検証されます。 不整合の問題が検出されると、通知を受け取る場合があります。 インポートしたコンフィギュレーションのバージョンを使用する前に、それらの問題を解決する必要があります。 詳細については、このトピックの関連記事の一覧を参照してください。

<a name="see-also"></a>参照
--------

[電子申告の概要](general-electronic-reporting.md)




