---
title: コード移行中の Azure DevOps マッピングのコンフィギュレーション
description: このチュートリアルでは、LCS コードのアップグレード サービスが完了した後、開発ボックスを Azure DevOps プロジェクトにマップする方法を示します。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 25951
ms.assetid: 60b8c895-0d5d-4d6b-8e32-e9c2f688ca69
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d5c2afd5868eeaffcae16a32e41017cb45278861
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683478"
---
# <a name="configure-the-azure-devops-mapping-during-code-migration"></a>コード移行中の Azure DevOps マッピングのコンフィギュレーション

[!include [banner](../includes/banner.md)]

このチュートリアルでは、Lifecycle Services (LCS) コードのアップグレード サービスが完了した後、開発ボックスを Azure DevOps プロジェクトにマップする方法を示します。 

LCS コードのアップグレード サービスでは、Azure DevOps にアップグレードされたコードが自動的に確認されます。 次に、 開発ボックスを、Azure DevOps プロジェクト内のアップグレード フォルダー/ブランチにマップする必要があります (アップグレード フォルダー/ブランチの名前は移行するバージョンによって異なります)。 アップグレードされたフォルダー内には、3 つのフォルダーが表示されます。

- 輸出
- メタデータ
- プロジェクト

## <a name="key-concepts"></a>重要な概念
- **Export** は、Microsoft Dynamics AX 2012 からのエクスポート後、XML ファイルを含んでいるプロジェクトです。 このプロジェクトは、アップグレード前の XML 形式のメタデータです。 このプロジェクトは、Dynamics AX 2012 からアップグレードする場合にのみ関係があります。
- **メタデータ** は、アップグレード済のコードです (メタデータ XML ファイル)。
- **プロジェクト** は、アップグレード中に使用できる 2 つのソリューションです。 1 つのソリューションである CodeMergeSolution は、競合し、また解決する必要がある要素を伴うプロジェクトを含むソリューションです。 もう 1 つのソリューション、UpgradedSolution には、アップグレードされたモデルごとに 1 つのプロジェクトのコレクションが含まれています。 たとえば、Azure DevOps で、以下の構造のようなものを表示します。 [![プロジェクト](./media/filestructure_configuringyourvsosolution.png)](./media/filestructure_configuringyourvsosolution.png)

## <a name="map-azure-devops-to-your-development-box"></a>Azure DevOps の開発ボックスへのマップ
1.  Visual Studio で、**チーム エクスプローラー &gt; チーム プロジェクトの選択 &gt; サーバー &gt; 追加** と進んでアカウントに接続します。
2.  チーム プロジェクトに URL を入力します。 **閉じる** を選択します。
3.  Azure DevOps アカウントが表示されることを確認します。 右側で、作業するプロジェクトを選択します。 **接続** を選択します。
4.  ここで、ワークスペースを Azure DevOps フォルダーにマップする必要があります。 **ソース コード エクスプ ローラ** に移動し、このマッピングを行います。
    1.  &gt; プロジェクト
        - **Visual Studio 2015** : C:\\ユーザー\\ &lt;ユーザー名&gt;\\ドキュメント\\Visual Studio 2015\\プロジェクト
        - **Visual Studio 2017** またはそれ以降 : C:\\ユーザー\\&lt;ユーザー名&gt;\\ソース\\リポジトリ
    2.  メタデータ &gt; C:\\AOSService\\PackagesLocalDirectory
        -   クラウド VMs で、このフォルダーは I:\\、J:\\または K:\\ ドライブにあります
        -   以前のバージョンで、このフォルダーは C:\\パッケージ
        -   **重要**:
            -   Dynamics AX 2012 R3 またはそれ以前のバージョンから移行する場合は、**メイン** 分岐の下のメタデータ フォルダにマッピングします。
            -   2 つの製品バージョン間で移行する場合は、**リリース** の分岐の下のメタデータ フォルダーにマッピングします。

[![vstsmapping](./media/vstsmapping.png)](./media/vstsmapping.png) 

これらのフォルダーをマップした後、ローカル ボックスにコードを同期させることができます。 **メタデータ** を右クリックし、**最新バージョンを取得** を選択します。 同様に、プロジェクト フォルダーを同期します。 メタデータ フォルダーを同期した後、**Finance and Operations** &gt; **モデル管理** &gt; **モデルの更新** から Visual Studio でモデルを更新します。 [![VSRefreshModels](./media/vsrefreshmodels.png)](./media/vsrefreshmodels.png) これで、プロジェクトを立ち上げ、競合を解決し、コードの移行を構築、テスト、および実行する準備が整いました。
