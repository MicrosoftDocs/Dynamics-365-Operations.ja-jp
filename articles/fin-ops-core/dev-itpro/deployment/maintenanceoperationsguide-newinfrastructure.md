---
title: 配置の保守操作
description: このトピックでは、セルフ サービス配置エクスペリエンスを使用して配置された環境の保守操作を実行する方法について説明します。
author: laneswenka
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 24211
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: c90c88fc35e36904b97fa5eb60bf6bfef4f6475a
ms.sourcegitcommit: 6fd739976b46122f9a9002309aba60edb89e5468
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/16/2022
ms.locfileid: "8453498"
---
# <a name="maintenance-operations-for-deployments"></a>配置の保守操作

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/limited-availability.md)]

このトピックでは、[セルフサービス配置](infrastructure-stack.md) エクスペリエンスを使用して、配置された環境の保守操作を実行する方法について説明します。

## <a name="restart-services"></a>サービスをリセット

サービスの再開機能を使用すると、Microsoft サブスクリプションで展開された階層 2、階層 3、階層 4、または階層 5 の標準承認テスト (サンドボックス) 環境に関連付けられた個々のサービスを再開することができます。 再起動できるサービスは、**財務と運用アプリ サービス**、**データ管理ワークスペース**、および **Financial Reporting サービス** です。

サービスを再起動するには、以下の手順を実行します。

1. Microsoft Dynamics Lifecycle Services (LCS) の環境の詳細ページで、**メンテナンス \> サービスの再起動** を選択します。
2. 再起動するサービスを選択し、**確認** を選択します。

    再起動時、環境のステータスが **サービスの再起動中** に更新されます。その他のメンテナンス操作を開始することはできません。 環境のステータスは、サービスの再起動後に、**展開済み** に戻ります。

## <a name="maintenance-mode"></a>メンテナンス モード

Finance and Operations アプリには、[メンテナンス モード](../sysadmin/maintenance-mode.md) という名前のシステム全体に適用される設定が含まれています。 メンテナンス モードでは、システム機能に影響を与える可能性のあるシステム変更を、システム管理者が安全に実行する方法が提供されます。 たとえば、コンフィギュレーション キーは、オンまたはオフにすることができます。 メンテナンス モードがオンのとき、システム管理者および **メンテナンス モード** ユーザー ロールが割り当てられたユーザーのみがシステムにサインインすることができます。 既定では、メンテナンス モードがオフになっています。

メンテナンス モードのオン/オフを切り替えるには、以下の手順に従います。

1. LCS の環境の詳細ページで、**メンテナンス \> メンテナンス モードを有効にする** を選択します。

    環境の状態は、**配置済み** から **サービス中** に変更されます。 メンテナンス モードがオンになると、環境のステータスが **メンテナンス中** に更新され、システム管理者のみがログインできます。

2. システム管理者が構成の変更を終了したら、環境の詳細ページで **メンテナンス \> メンテナンス モードを無効にする** を選択します。

    環境の状態は、**メンテナンス中** から **サービス中** に変更されます。 環境のステータスは、メンテナンス モードがオフになると、**展開済み** に戻ります。 環境の履歴が更新され、環境がメンテナンス モードに戻ったことが反映されます。

## <a name="access-database"></a>データベースへのアクセス

[セルフサービス配置](infrastructure-stack.md)エクスペリエンスを使用して配置された環境では、リモート アクセスがオフになっています。 実装時に、トラブルシューティング目的で階層 2、階層 3、階層 4、または階層 5 の標準受け入れテスト環境のデータベースに接続する必要がある場合、必要に応じてアクセスが許可されます。 アクセス権は永続的ではありません。

データベースに接続するには、[Just-In-Time のアクセスを有効にする](../database/database-just-in-time-jit-access.md)に従ってください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
