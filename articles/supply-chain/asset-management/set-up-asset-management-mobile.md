---
title: 資産管理モバイル ワークスペースの設定
description: この記事では、作業者が資産管理タスクを実行するために使用できる資産管理モバイル ワークスペースを実行するための Microsoft Dynamics 365 Supply Chain Management と財務と運用 (Dynamics 365) モバイル アプリの設定方法について説明します。
author: johanhoffmann
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-22
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ef4e6bf2ae59adb05c7d4aacc3f5675a5adcafc9
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070056"
---
# <a name="set-up-the-asset-management-mobile-workspace"></a>資産管理モバイル ワークスペースの設定

[!include [banner](../includes/banner.md)]

この記事では、作業者が資産管理タスクを実行するために使用できる **資産管理** モバイル ワークスペースを実行するための Microsoft Dynamics 365 Supply Chain Management と財務と運用 (Dynamics 365) モバイル アプリの設定方法について説明します。

## <a name="set-up-maintenance-worker-users-in-supply-chain-management"></a>Supply Chain Management でのメンテナンス作業者ユーザーの設定

**資産管理** モバイル ワークスペースへのアクセスを必要とする 各ユーザーについて、次の手順に従います。

1. Supply Chain Management で、**人事管理 \>ワーカー** に移動し、設定するユーザーのワーカー レコードが存在することを確認します。 必要に応じて作業者レコードを作成します。
1. **資産管理 \> 設定 \> 作業者 \> 作業者** に移動し、前の手順で特定した (または作成された) 作業者レコードがメンテナンス作業者レコードにマップ されている事を確認します。 必要に応じて新しいメンテナンス作業者レコードを作成し、前の手順から作業者レコードに **作業者** フィールドを設定します。
1. **資産管理 \> 設定 \> 作業者 \> メンテナンス作業者グループ** に移動し、前の手順で特定した (または作成された) メンテナンス作業者レコードがメンテナンス作業者グループに属していることを確認します。
1. **システム管理 \> ユーザー** の順に移動します。
1. グリッドで関連ユーザーを選択します。
1. **ユーザーの詳細** クイック タブで、現在のユーザー アカウントに関連付ける作業者アカウントに **個人** フィールドを設定します。 この作業者アカウントは、手順 1 で特定した (または作成された) 作業者レコードで、手順2. でメンテナンス作業者レコードにマップされている必要があります。

> [!NOTE]
> ユーザーのアクセス許可とセキュリティ ロールは、Supply Chain Management のユーザー インターフェイスの機能と同様に、**資産管理** モバイル ワークスペースの機能に適用されます。 したがって、**資産管理** モバイル ワークスペースにアクセスするために設定したすべてのユーザーには、Supply Chain Management で同様の操作を直接実行するために必要なセキュリティ ロールが必要です。

## <a name="publish-the-asset-management-mobile-workspace"></a>資産管理モバイル ワークスペースの公開

財務と運用 (Dynamics 365) モバイル アプリで資産管理機能を使用するには、**資産管理** モバイル ワークスペースを公開する必要があります。

1. Supply Chain Management で、**設定** ボタン (右上隅のギア記号) を選択し、メニューの **モバイル アプリ** を選択します。
1. **モバイル アプリの管理** ダイアログ ボックスで、**資産管理** タイルを検索します。 "メタデータ内 - 未公開" というテキストが含まれている場合、ワークスペースはまだ公開されていません。 "メタデータ内 - 公開済" という文字列が含まれている場合、ワークスペースは既に発行済みで、この手順の残りを省略できます。

    ![モバイル アプリの管理ダイアログ ボックス。](media/mobile-workspaces.png "モバイル アプリの管理ダイアログ ボックス")

1. **資産管理** タイルを選択し、ツール バーの **発行** を選択します。 しばらくすると、ワークスペースが正常に発行されたことを示す通知が表示されます。 また、タイル上のテキストは "メタデータ内 - 公開済" に変更する必要があります。

## <a name="install-and-set-up-the-finance-and-operations-dynamics-365-mobile-app"></a>財務と運用 (Dynamics 365) モバイル アプリをインストールして設定する

1. 次のいずれかのアプリケーション店舗に移動して **Microsoft 財務と運用 (Dynamics 365)** アプリをモバイル デバイスにインストールします。

    - [Google Android デバイスの場合](https://go.microsoft.com/fwlink/?linkid=850662)
    - [Apple iOS デバイスの場合](https://go.microsoft.com/fwlink/?linkid=850663)

1. 財務と運用 (Dynamics 365) アプリを開きます。 サインイン ページが表示されます。 **サインイン** フィールドに Supply Chain Management の URL を入力するか、**最新の環境** ボックスの一覧で最近の URL を選択して、**接続** をクリックします。

    ![サインイン ページ。](media/mobile-app-sign-in.png "サインイン ページ")

1. 接続を確認するメッセージが表示された場合は、**了解します** チェック ボックスをオンにし、**接続** をクリックします。
1. **アカウントのピック** ページで、Microsoft アカウントを使用してモバイル アプリケーションにサインインします。

    **ワークスペース** ページが表示されます。 これには、Supply Chain Management インスタンスによって公開されたすべてのモバイル ワークスペースが一覧表示されます。

    ![ワークスペースのリスト。](media/mobile-app-workspaces.png "ワークスペースのリスト")

1. 法人 (会社) を変更する必要がある場合は、左上の角のメニュー ボタン (ハンバーガーまたはハンバーガー ボタンと呼ばれることもあります) をタップして、**会社の変更** をクリックします。

    ![法人の変更。](media/mobile-app-change-comp.png "法人の変更")

1. **ワークスペース** ページで、使用するワークスペースを選択して開きます。

    ![資産管理モバイル ワークスペース。](media/mobile-app-asset-workspace.png "資産管理モバイル ワークスペース")

## <a name="work-with-the-asset-management-mobile-workspace"></a>資産管理モバイル ワークスペースを使って作業する

**資産管理** モバイル ワークスペースの使用方法の詳細については、[資産管理モバイル ワークスペースの使用](asset-management-mobile-workspace.md) を参照してください。

財務と運用 (Dynamics 365) モバイル アプリの詳細については、[モバイル アプリ ホーム ページ](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md) を参照してください。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
