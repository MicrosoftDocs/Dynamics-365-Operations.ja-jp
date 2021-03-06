---
title: Finance and Operations アプリと Dataverse でのデュアル書き込み構成の検証
description: このトピックでは、Finance and Operations アプリと Dataverse 間でデュアル書き込みが構成されているかどうかを確認する方法について説明します。
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: af746d1d20ddd1552bce797288c6d62d69d7bd16
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748852"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>Finance and Operations アプリと Dataverse でのデュアル書き込み構成の検証

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



このトピックでは、Finance and Operations アプリと Dataverse 間のデュアル書き込み統合に関するトラブルシューティングの情報を提供します。 このトピックでは、Finance and Operations アプリと Dataverse 間でデュアル書き込みの構成を確認する方法について説明します。

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Finance and Operations アプリでデュアル書き込みが構成されていることを確認する

更新プログラムで行の保存時に発生したエラーがデュアル書き込みに起因するものであるかどうかを確認するには、まずデュアル書き込みが構成されていることを確認してください。

+ Finance and Operations アプリで管理者権限が付与されている場合は、**ワークスペース \> データ管理** に移動して、**デュアル書き込み** のタイルを選択します。 リンクされた環境の詳細と実行中のテーブル マップの一覧が表示される場合は、デュアル書き込みが構成されています。

    ![管理者権限が付与されている場合に Finance and Operations アプリの接続を確認する](media/verify_fin_ops_1.png)

+ 管理者権限が付与されていない場合は、*エンティティ \<entity name\>にデータを書き込めません* というエラー メッセージが表示されます。 次の図に示す例では、Finance and Operations アプリで顧客行を作成することはできません。デュアル書き込みが構成されているものの、Dataverse に顧客グループおよび支払条件参照データがに存在しないことが原因です。

    ![管理者権限が付与されていない場合に Finance and Operations アプリの接続を確認する](media/verify_fin_ops_2.png)

Finance and Operations アプリでデータを作成する際に発生する問題の修正方法については、[ライブ同期に関する問題のトラブルシューティング](dual-write-troubleshooting-live-sync.md) を参照してください。

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Dataverse アプリでデュアル書き込みが構成されていることを確認する

データの作成時に、Dataverse ページに **会社** 列が表示されている場合は、デュアル書き込みが構成されています。

![Dataverse の接続を確認します](media/verify_cds.png)

Dataverse でデータの作成時に発生する問題の修正方法については、[ライブ同期に関する問題のトラブルシューティング](dual-write-troubleshooting-live-sync.md) を参照してください。

Dataverse でデータの作成時にエラーが発生した場合にエラーの詳細の確認する方法については、[ Dataverse でプラグイン追跡ログを有効化してエラーの詳細を確認する](dual-write-troubleshooting.md#enable-view-trace) を参照してください。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]