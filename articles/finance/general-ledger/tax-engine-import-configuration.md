---
title: 税エンジン インポート コンフィギュレーション
description: この記事では、輸入税エンジン コンフィギュレーションについて説明します。
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
ms.openlocfilehash: 4f24ddedcfee32e071e61ec1ea09243c4fe8966b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899799"
---
# <a name="tax-engine-import-configuration"></a>税エンジン インポート コンフィギュレーション

[!include [banner](../includes/banner.md)]

この記事では、輸入税エンジン コンフィギュレーションについて説明します。

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
