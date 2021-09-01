---
title: 税エンジン インポート コンフィギュレーション
description: このトピックでは、輸入税エンジンのコンフィギュレーションについて説明します。
author: yijialuan
ms.date: 10/15/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, GTE
audience: IT Pro
ms.reviewer: roschlom
ms.search.region: India
ms.author: riluan
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: ec7db4caf10db2e33507d9692480b80f54d7ba36462c6255c51978c0c797e141
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758065"
---
# <a name="tax-engine-import-configuration"></a>税エンジン インポート コンフィギュレーション

[!include [banner](../includes/banner.md)]

このトピックでは、輸入税エンジンのコンフィギュレーションについて説明します。

### <a name="create-a-lifecycle-services-lcs-configuration-repository"></a>Lifecycle Services (LCS) のコンフィギュレーション リポジトリの作成
1. **組織管理** > **ワークスペース** > **電子申告** の順に移動します。
2. **コンフィギュレーション プロバイダー** セクションで、**Microsoft** プロバイダー タイルの **リポジトリ** をクリックします。

![コンフィギュレーションを読み込みます。](media/gte-extension-repositories.png)

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

![コンフィギュレーションを読み込みます。](media/gte-extension-import-configurations.png)

7. **はい** をクリックして、インポートを確認します。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]