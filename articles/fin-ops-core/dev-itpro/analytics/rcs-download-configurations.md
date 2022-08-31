---
title: 規制コンフィギュレーション サービス (RCS) からの電子申告 (ER) 構成のインポート
description: この記事は、Regulatory Configuration Services (RCS) から電子申告 (ER) コンフィギュレーションをインポートする方法について説明します。
author: kfend
ms.date: 04/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.search.form: ERSolutionRepositoryTable
ms.openlocfilehash: 9edc76b13c69d89f3ee7bb4c4a8de60737367ec6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276644"
---
# <a name="import-electronic-reporting-er-configurations-from-regulatory-configuration-services-rcs"></a>規制コンフィギュレーション サービス (RCS) からの電子申告 (ER) 構成のインポート

[!include [banner](../includes/banner.md)]

規制コンフィギュレーション サービス (RCS) を使用すると電子申告 (ER) 構成をインポートできます。 ER ツールは、1 つの会社用にプロビジョニングされた RCS の各インスタンスで構成されているコンフィギュレーションの一覧へのアクセスを提供します。 この機能を使用して、現在のインスタンスに、RCS インスタンスで構成した構成をインポートできます。 コンフィギュレーションをインポートした後、受信ドキュメントの処理や、送信電子ドキュメントの生成に使用できます。

この機能の詳細を知るには、この記事の例を実行します。 または、7.5.4.3 IT サービス/ソリューション コンポーネントの取得/開発 (10677) 業務プロセスの一部である [RCS からの ER インポート構成](https://download.microsoft.com/download/0/4/e/04e13839-e423-442b-a6c2-dd35b1045c2d/Dynamics%20365%20for%20Finance%20and%20Operations%208.1%20Electronic%20reporting%20task%20guides.zip) タスク ガイドをダウンロードおよび再生します。 RCS インスタンスから現在のインスタンスに ER コンフィギュレーションをインポートするプロセスを示します。

## <a name="example-import-an-er-configuration-from-rcs"></a>例: RCS からの ER コンフィギュレーションのインポート

この例では、システム管理者または電子報告開発者ロールのユーザーが RCS から ER コンフィギュレーションの新しいバージョンをインポートする方法を示します。 この例では、RCS インスタンスで構成されている ER コンフィギュレーションの目的のバージョンを選択して、Litware, Inc. というサンプル企業の現在のインスタンスにそのバージョンをインポートします。ER コンフィギュレーションは会社間で共有されるため、すべての会社でこれらの手順を完了することができます。

この例の手順を完了するには、まず、[コンフィギュレーション プロバイダーを作成し、それを有効としてマークする](tasks/er-configuration-provider-mark-it-active-2016-11.md) にある手順を完了する必要があります。 **完了** または **共有** のステータスを持つ 1 つ以上の ER 構成を含む RCS インスタンスへのアクセスも必要です。

1. **組織管理  \> ワークスペース \> 電子申告** の順に移動します。
2. **ローカライズのコンフィギュレーション** ページの **構成プロバイダー** セクションで、Litware, Inc. サンプル会社のコンフィギュレーション プロバイダーが一覧に表示されていること、および **アクティブ** とマークされていることを確認します。 このコンフィギュレーション プロバイダーが表示されない場合は、[コンフィギュレーション プロバイダーを作成し、それを有効としてマークする](tasks/er-configuration-provider-mark-it-active-2016-11.md) の手順に従います。
3. RCS 環境が会社に対してプロビジョニングされていない場合、**外部リンク** セクションの **規制サービス - 構成** を選択します。 次に、RCS 環境をプロビジョニングする指示に従います。
4. **関連するリンク** セクションで、**電子申告のパラメーター** を選択します。
5. **電子申告のパラメーター** ページで、**RCS** タブを選択します。
6. 会社にプロビジョニングされた RCS 環境にアクセスするには、このタブの URL を使用します。
7. **電子申告のパラメーター** ページを閉じます。

### <a name="register-a-new-er-repository"></a>新しい ER リポジトリの登録

1. **ローカライズのコンフィギュレーション** ページの一覧で **Litware, Inc.** コンフィギュレーション プロバイダーを選択します。
2. **リポジトリ** を選択します。
3. **追加** をクリックして、ドロップダウン ダイアログ ボックスを開きます。
4. コンフィギュレーション リポジトリ タイプとして **RCS** を選択し、**リポジトリの作成** を選択します。
6. **RCS 環境の表示名** フィールドで、目的の RCS インスタンスを選択します。 複数のインスタンスがあることに注意してください。
7.  **OK** を選択します。

### <a name="import-er-configurations-from-an-rcs-based-repository"></a>RCS ベースのリポジトリからの ER コンフィギュレーションのインポート

1. **コンフィギュレーション リポジトリ** ページで、ウィンドウの左側にある **フィルターの表示** ボタンを選択します。
2. **名前** フィルターで、フィルター演算子として **次の値で始まる** を選択し、フィルター値として **RCS** と入力します。
3. リポジトリを選択し、開きます。
3. **規制コンフィギュレーション サービスに接続する** ページで、**規制コンフィギュレーション サービスに接続するには、ここをクリックしてください** リンクを選択します。
4. **開く** を選択します。
5. **閉じる** を選択します。
6. ER コンフィギュレーションの目的のバージョンを選択し、**インポート** を選択してそのバージョンをインポートします。

## <a name="additional-resource"></a>その他のリソース

- [電子申告 (ER) の概要](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
