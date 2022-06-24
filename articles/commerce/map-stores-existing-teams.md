---
title: Microsoft Teams に既存のチームがある場合は、店舗とチームをマッピングします
description: この記事では、Commerce の統合前に Microsoft Teams でチームを作成していた場合に、Dynamics 365 Commerce headquarters の店舗と対応するチームをマッピングする方法について説明します。
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 4cb18affd0df59dc986602a684a3fe3d418644fd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902740"
---
# <a name="map-stores-and-teams-if-there-are-pre-existing-teams-in-microsoft-teams"></a>Microsoft Teams に既存のチームがある場合は、店舗とチームをマッピングします

[!include [banner](includes/banner.md)]

この記事では、Commerce の統合前に Microsoft Teams でチームを作成していた場合に、Dynamics 365 Commerce headquarters の店舗と対応するチームをマッピングする方法について説明します。

組織では、Dynamics 365 Commerce と Microsoft Teams を統合する前に、一部またはすべてのストアにチームが作成されている場合もあるでしょう。 この場合、Commerce POSと Microsoft Teams の間でタスクの同期を確立するには、Commerce 本部で店舗と対応するチームのマッピングをする必要があります。

## <a name="map-stores-and-corresponding-teams-in-commerce-headquarters"></a>Commerce 本部の店舗と対応するチームをマッピングする 

Commerce 本部で店舗と対応するチームをマッピングするには、以下の手順で行います。

1. **システム管理 \> ワークスペース \> データ管理** の順に移動します。
1. **エクスポート** の選択 
1. アクション ウィンドウで、**新規** を選択します。
1. **グループ名** で、「Teams マッピングのエクスポート」と入力します。
1. **選択したエンティティ** クイックタブで、 **エンティティの追加** を選択します。 **エンティティの追加** ダイアログ ボックスが表示されます。  
1. **エンティティ名** ボックスの一覧で、**ソースとチームの間の Teams マッピング** を選択します 。
1. **ターゲットのデータ形式** ドロップダウン リスト一覧で、**CSV** を選択します。
1. **追加** を選択してから **閉じる** を選択します。
1. アクション ウィンドウの下の左上で、**今すぐエクスポート** を選択します。
1. **エンティティ 処理ステータス** で、**ファイルのダウンロード** を選択します。
1. エクスポートされた CSV ファイルで、 **SOURCETYPE**、**SOURCEID**、**TEAMID** の値を次のように入力します :
    - **SOURCETYPE** には、「RetailStore」と入力します。 
    - **SOURCEID** には、店舗番号を入力します (サンフランシスコ店舗の場合は  "000135" など)。 店舗番号は、**小売とコマース \> Channels \> Stores** で検索できます。
    - **TEAMID** には、Microsoft Teams から該当するチーム ID を入力してください (例 : "5f8bc92b-6aa8-451e-85d1-3949c01ddc6c")。 チーム ID の情報は、[admin.teams.microsoft.com](https://admin.teams.microsoft.com) で確認できます。
1. CSV ファイルをローカル コンピューターに保存します。
1. **システム管理 \> ワークスペース \> データ管理** にアクセスし、**インポート** を選択します。
1. **選択したエンティティ** クイックタブで、 **ファイルの追加** を選択します。 **ファイルの追加** ダイアログ ボックスが表示されます。
1. **エンティティ名** ボックスの一覧で、**ソースとチームの間の Teams マッピング** を選択します 。
1. **ソース データの形式** ドロップダウン リスト一覧で、**CSV** を選択します。
1. **アップロードして追加** を選択し、前に保存した CSV ファイルを選択して、**開く** を選択します。
1. **追加 ダイアログ** ボックスで、**閉じる** を選択します。
1. アクション ペインで、**保存** を選択し、**インポート** を選択します。

次のイメージ例では、Commerce の **チームのマッピングのエクスポート** グループで、**エンティティの追加** 要素とエクスポートされた CSV ファイルのヘッダーが強調表示されています。

![Commerce の チームのマッピングのエクスポート グループで、エンティティの追加 要素とエクスポートされた CSV ファイルのヘッダーが強調表示されている。](media/d365-commerce-data-mgmt-export-entity.png)

> [!NOTE]
> 上記手順の完了後は、[Microsoft Teams と POS 間のタスク管理を同期する](synchronize-tasks-teams-pos.md) に記載の手順に従い、タスク管理を同期します。 

## <a name="additional-resources"></a>追加リソース

[Dynamics 365 Commerce と Microsoft Teams データ統合の概要](commerce-teams-integration.md)

[Dynamics 365 Commerce と Microsoft Teams の統合を有効化する](enable-teams-integration.md)

[Dynamics 365 Commerce から Microsoft Teams へのプロビジョニング](provision-teams-from-commerce.md)

[Microsoft Teams と Dynamics 365 Commerce の POS 間でタスク管理を同期させる](synchronize-tasks-teams-pos.md)

[Microsoft Teams でユーザーとロールを管理する](manage-user-roles-teams.md)

[Dynamics 365 Commerce と Microsoft Teams の統合に関する FAQ](teams-integration-faq.md)
