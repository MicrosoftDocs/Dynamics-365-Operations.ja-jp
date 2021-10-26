---
title: 税エンジン インポート コンフィギュレーション
description: このトピックでは、輸入税エンジンのコンフィギュレーションについて説明します。
author: kailiang
ms.date: 10/15/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, GTE
audience: IT Pro
ms.reviewer: kfend
ms.search.region: India
ms.author: kailiang
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 49681ad5238e2a9f92fff149b4663f6d16673dcd
ms.sourcegitcommit: 25b3dd639e41d040c2714f56deadaa0906e4b493
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/06/2021
ms.locfileid: "7605144"
---
# <a name="tax-engine-import-configuration"></a>税エンジン インポート コンフィギュレーション

[!include [banner](../includes/banner.md)]

このトピックでは、輸入税エンジンのコンフィギュレーションについて説明します。

### <a name="create-a-lifecycle-services-lcs-configuration-repository"></a>Lifecycle Services (LCS) のコンフィギュレーション リポジトリの作成
1. **組織管理** > **ワークスペース** > **電子申告** の順に移動します。
2. **コンフィギュレーション プロバイダー** セクションで、**Microsoft** プロバイダー タイルの **リポジトリ** をクリックします。

![リポジトリ リンクが強調表示されたコンフィギュレーション プロバイダー タイル。](media/gte-extension-repositories.png)

3. **追加** をクリックします。 
4. **LCS** オプションを選択します。 
5. **リポジトリの作成** をクリックして、LCS コンフィギュレーション リポジトリを作成します。
6. リポジトリの名前と説明を入力し、**OK** をクリックします。

### <a name="import-configurations-from-lcs"></a>LCS からコンフィギュレーションをインポートする
1. **組織管理** > **ワークスペース** > **電子申告** の順に移動します。
2. **コンフィギュレーション プロバイダー** セクションで、**Microsoft** プロバイダー タイルの **リポジトリ** をクリックします。
3. 作成したコンフィギュレーション リポジトリを選択します。 
4. **開く** をクリックします。
5. ツリーで、最新の税務書類を選択します (たとえば、**税 (インド GST)** を選択)。
6. **バージョン** セクションで、**インポート** をクリックします。

![レポジトリ ページの構成](media/gte-extension-import-configurations.png)

7. **はい** をクリックして、インポートを確認します。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
