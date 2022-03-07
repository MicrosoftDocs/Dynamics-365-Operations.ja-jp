---
title: コード移行中の Azure DevOps マッピングのコンフィギュレーション
description: このチュートリアルでは、LCS コードのアップグレード サービスが完了した後、開発ボックスを Azure DevOps プロジェクトにマップする方法を示します。
author: jorisdg
ms.date: 01/10/2022
ms.topic: article
audience: Developer
ms.reviewer: sericks
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9fc37513d31da4a0b9a2a427cb39763fb664e7a1
ms.sourcegitcommit: 27475081f3d2d96cf655b6afdc97be9fb719c04d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/12/2022
ms.locfileid: "7964669"
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
- **プロジェクト** は、アップグレード中に使用できるソリューションです。 1 つのソリューションである CodeMergeSolution は、競合し、また解決する必要がある要素を伴うプロジェクトを含むソリューションです。 もう 1 つのソリューション、UpgradedSolution には、アップグレードされたモデルごとに 1 つのプロジェクトのコレクションが含まれています。

## <a name="map-azure-devops-to-your-development-box"></a>Azure DevOps の開発ボックスへのマップ
1.  Visual Studio でトップメニューから **表示 &gt; チーム エクスプローラー** を選択して **チーム エクスプローラー** ウィンドウを開きます。
2.  **チーム エクスプローラー** ウィンドウで **接続** を選択し、**接続の管理 > プロジェクトに接続** を選択します。
3.  プロンプトに従って接続します。 アカウントで使用できるプロジェクトの一覧から、作業するプロジェクトを選択します。 **接続** を選択します。
4.  ここで、ワークスペースを Azure DevOps フォルダーにマップする必要があります。 **ソース コード エクスプ ローラ** に移動し、このマッピングを行います。
    1.  &gt; プロジェクト
        - プロジェクトを保存するフォルダーを選択するか、既定の **Visual Studio** フォルダーを使用します: C:\\Users\\&lt;username&gt;\\source\\repos
    2.  メタデータ &gt; C:\\AOSService\\PackagesLocalDirectory
        -   クラウド VMs で、このフォルダーは I:\\、J:\\または K:\\ ドライブにあります
        -   **重要**:
            -   Dynamics AX 2012 R3 またはそれ以前のバージョンから移行する場合は、**メイン** 分岐の下のメタデータ フォルダにマッピングします。
            -   2 つの製品バージョン間で移行する場合は、**リリース** の分岐の下のメタデータ フォルダーにマッピングします。

[![vstsmapping。](./media/vstsmapping.png)](./media/vstsmapping.png) 

これらのフォルダーをマップした後、ローカル ボックスにコードを同期させることができます。 **メタデータ** を右クリックし、**最新バージョンを取得** を選択します。 同様に、プロジェクト フォルダーを同期します。 メタデータ フォルダーを同期した後、**Finance and Operations** &gt; **モデル管理** &gt; **モデルの更新** から Visual Studio でモデルを更新します。 [![VSRefreshModels。](./media/vsrefreshmodels.png)](./media/vsrefreshmodels.png) これで、プロジェクトの立ち上げ、競合の解決、コードの移行の構築、テスト、および実行を行う準備が整いました。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
