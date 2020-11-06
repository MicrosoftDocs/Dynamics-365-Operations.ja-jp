---
title: Finance and Operations アプリと Common Data Service でデュアル書き込みの構成を確認する
description: このトピックでは、Finance and Operations アプリと Common Data Service 間でデュアル書き込みが構成されているかどうかを確認する方法について説明します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 2ddac76871a3ac574a1edcb5446be6c64e5e4682
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997233"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-common-data-service"></a>Finance and Operations アプリと Common Data Service でデュアル書き込みの構成を確認する

[!include [banner](../../includes/banner.md)]



このトピックでは、Finance and Operations アプリと Common Data Service 間のデュアル書き込み統合に関するトラブルシューティングの情報を提供します。 このトピックでは、Finance and Operations アプリと Common Data Service 間でデュアル書き込みの構成を確認する方法について説明します。

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Finance and Operations アプリでデュアル書き込みが構成されていることを確認する

更新プログラムでレコードの保存時に発生したエラーがデュアル書き込みに起因するものであるかどうかを確認するには、まずデュアル書き込みが構成されていることを確認してください。

+ Finance and Operations アプリで管理者権限が付与されている場合は、 **ワークスペース \> データ管理** に移動して、 **デュアル書き込み** のタイルを選択します。 リンクされた環境の詳細と実行中のエンティティ マッピングの一覧が表示される場合は、デュアル書き込みが構成されています。

    ![管理者権限が付与されている場合に Finance and Operations アプリの接続を確認する](media/verify_fin_ops_1.png)

+ 管理者権限が付与されていない場合は、 *エンティティ \<entity name\>にデータを書き込めません* というエラー メッセージが表示されます。 次の図に示す例では、Finance and Operations アプリで顧客レコードを作成することはできません。デュアル書き込みが構成されているものの、Common Data Service に顧客グループおよび支払条件参照データがに存在しないことが原因です。

    ![管理者権限が付与されていない場合に Finance and Operations アプリの接続を確認する](media/verify_fin_ops_2.png)

Finance and Operations アプリでデータを作成する際に発生する問題の修正方法については、[ライブ同期に関する問題のトラブルシューティング](dual-write-troubleshooting-live-sync.md) を参照してください。

## <a name="verify-that-dual-write-is-configured-in-common-data-service"></a>Common Data Service アプリでデュアル書き込みが構成されていることを確認する

データの作成時に、Common Data Service ページに **会社** フィールドが表示されている場合は、デュアル書き込みが構成されています。

![Common Data Service の接続を確認します](media/verify_cds.png)

Common Data Service でデータの作成時に発生する問題の修正方法については、[ライブ同期に関する問題のトラブルシューティング](dual-write-troubleshooting-live-sync.md) を参照してください。

Common Data Service でデータの作成時にエラーが発生した場合にエラーの詳細の確認する方法については、[ Common Data Service でプラグイン追跡ログを有効化してエラーの詳細を確認する](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details) を参照してください。
