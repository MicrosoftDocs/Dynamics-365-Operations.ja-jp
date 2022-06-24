---
title: 財務と運用アプリおよび Dataverse で二重書き込みの構成を確認する
description: この記事では、財務と運用アプリと Dataverse 間でデュアル書き込みが構成されているかどうかを確認する方法について説明します。
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 7131e6c2c4ca4d9c6bb84ad74bf425faf28bd92c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884462"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>財務と運用アプリおよび Dataverse で二重書き込みの構成を確認する

[!include [banner](../../includes/banner.md)]





この記事では、財務と運用アプリと Dataverse 間のデュアル書き込み統合に関するトラブル シューティングの情報を提供します。 このトピックでは、財務と運用アプリと Dataverse 間でデュアル書き込みの構成を確認する方法について説明します。

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>財務と運用アプリでデュアル書き込みが構成されていることを確認する

更新プログラムで行の保存時に発生したエラーがデュアル書き込みに起因するものであるかどうかを確認するには、まずデュアル書き込みが構成されていることを確認してください。

+ 財務と運用アプリで管理者権限が付与されている場合は、**ワークスペース \> データ管理** に移動して、**デュアル書き込み** のタイルを選択します。 リンクされた環境の詳細と実行中のテーブル マップの一覧が表示される場合は、デュアル書き込みが構成されています。

    ![管理者権限が付与されていない場合に財務と運用アプリの接続を確認します。](media/verify_fin_ops_1.png)

+ 管理者権限が付与されていない場合は、*エンティティ \<entity name\>にデータを書き込めません* というエラー メッセージが表示されます。 次の図に示す例では、財務と運用アプリで顧客行を作成することはできません。デュアル書き込みが構成されているものの、Dataverse に顧客グループおよび支払条件参照データがに存在しないことが原因です。

    ![管理者権限が付与されていない場合に財務と運用アプリの接続を確認します。](media/verify_fin_ops_2.png)

財務と運用アプリでデータを作成する際に発生する問題の修正方法については、[ライブ同期に関する問題のトラブルシューティング](dual-write-troubleshooting-live-sync.md) を参照してください。

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Dataverse アプリでデュアル書き込みが構成されていることを確認する

データの作成時に、Dataverse ページに **会社** 列が表示されている場合は、デュアル書き込みが構成されています。

![Dataverse の接続を確認します。](media/verify_cds.png)

Dataverse でデータの作成時に発生する問題の修正方法については、[ライブ同期に関する問題のトラブルシューティング](dual-write-troubleshooting-live-sync.md) を参照してください。

Dataverse でデータの作成時にエラーが発生した場合にエラーの詳細の確認する方法については、[ Dataverse でプラグイン追跡ログを有効化してエラーの詳細を確認する](dual-write-troubleshooting.md#enable-view-trace) を参照してください。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]