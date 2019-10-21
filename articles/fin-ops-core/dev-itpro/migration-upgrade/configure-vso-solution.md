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
ms.search.scope: Operations
ms.custom: 25951
ms.assetid: 60b8c895-0d5d-4d6b-8e32-e9c2f688ca69
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9dd8a69eac1ff986ec52c6d65250a84c2dc7e256
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183169"
---
# <a name="configure-the-azure-devops-mapping-during-code-migration"></a>コード移行中の Azure DevOps マッピングのコンフィギュレーション

[!include [banner](../includes/banner.md)]

このチュートリアルでは、Lifecycle Services (LCS) コードのアップグレード サービスが完了した後、開発ボックスを Azure DevOps プロジェクトにマップする方法を示します。 

LCS コードのアップグレード サービスでは、Azure DevOps (旧 Visual Studio Online) にアップグレードされたコードが自動的に確認されます。 次に、 開発ボックスを、Azure DevOps プロジェクト内のアップグレード フォルダー/ブランチにマップする必要があります (アップグレード フォルダー/ブランチの名前は移行するバージョンによって異なります)。 アップグレードされたフォルダー内には、3 つのフォルダーが表示されます。

-   輸出
-   メタデータ
-   プロジェクト

## <a name="key-concepts"></a>重要な概念
-   **Export** は、Microsoft Dynamics AX 2012 からのエクスポート後、XML ファイルを含んでいるプロジェクトです。 これはアップグレード前の XML 形式のメタデータです。 これは、Dynamics AX 2012 からアップグレードする場合にのみ関係があります。
-   **メタデータ**は、アップグレード済のコードです (メタデータ XML ファイル)。
-   **プロジェクト**は、アップグレード中に使用できる 2 つのソリューションです。 1 つのソリューションである CodeMergeSolution は、競合し、また解決する必要がある要素を伴うプロジェクトを含むソリューションです。 もう 1 つのソリューション、UpgradedSolution には、アップグレードされたモデルごとに 1 つのプロジェクトのコレクションが含まれています。 たとえば、Azure DevOps で、以下の構造のようなものを表示します。 [![プロジェクト](./media/filestructure_configuringyourvsosolution.png)](./media/filestructure_configuringyourvsosolution.png)

## <a name="map-azure-devops-to-your-development-box"></a>Azure DevOps の開発ボックスへのマップ
1.  Visual Studio で、**チーム エクスプローラー &gt; チーム プロジェクトの選択 &gt; サーバー &gt; 追加**と進んでアカウントに接続します。
2.  チーム プロジェクトに URL を入力します。 **閉じる**をクリックします。
3.  Azure DevOps アカウントが表示されることを確認します。 右側で、作業するプロジェクトを選択します。 **接続** をクリックします。
4.  ここで、ワークスペースを Azure DevOps フォルダーにマップする必要があります。 **ソース コード エクスプ ローラ**に移動し、このマッピングを行います。
    1.  プロジェクト &gt; C:\\Users\\&lt;username&gt;\\Documents\\Visual Studio 2015\\Projects
    2.  メタデータ &gt; C:\\AOSService\\PackagesLocalDirectory
        -   クラウド VMs で、このフォルダーは I:\\または J:\\ ドライブに保管
        -   以前のバージョンで、このフォルダーは C:\\パッケージ
        -   **重要**:
            -   Dynamics AX 2012 R3 またはそれ以前のバージョンから移行する場合は、**メイン**分岐の下のメタデータ フォルダにマッピングします。
            -   2 つの製品バージョン間で移行する場合は、**リリース**の分岐の下のメタデータ フォルダーにマッピングします。

[![vstsmapping](./media/vstsmapping.png)](./media/vstsmapping.png) 

これらのフォルダーをマップした後、ローカル ボックスにコードを同期させることができます。 **メタデータ**を右クリックし、**最新バージョンを取得**を選択します。 同様に、プロジェクト フォルダーを同期します。 メタデータ フォルダーを同期した後、**Finance and Operations** &gt; **モデル管理** &gt; **モデルの更新** から Visual Studio でモデルを更新します。 [![VSRefreshModels](./media/vsrefreshmodels.png)](./media/vsrefreshmodels.png) これで、プロジェクトを立ち上げ、競合を解決し、コードの移行を構築、テスト、および実行する準備が整いました。
