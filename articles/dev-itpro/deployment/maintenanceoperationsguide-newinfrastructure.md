---
title: "配置の保守操作"
description: "このトピックでは、セルフ サービス配置エクスペリエンスを使用して配置された環境の保守操作を実行する方法について説明します。"
author: manado
manager: AnnBe
ms.date: 12/14/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 24211
ms.search.region: Global
ms.author: manado
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: 8.1.1
ms.translationtype: HT
ms.sourcegitcommit: 96290e93b20af32d7103317d8fa8f041e599df96
ms.openlocfilehash: 55762be3e3481f1daa71c852a40657e0c8b05c1e
ms.contentlocale: ja-jp
ms.lasthandoff: 12/19/2018

---

# <a name="maintenance-operations-for-deployments"></a>配置の保守操作

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/limited-availability.md)]

このドキュメントでは、[セルフ サービス配置](infrastructure-stack.md)エクスペリエンスを使用して配置された Dynamics 365 for Finance and Operations 環境の保守操作を実行する方法について説明します。

## <a name="restart-services"></a>サービスをリセット
サービスの再開機能を使用すると、Microsoft サブスクリプションで展開された階層 2、階層 3、階層 4、または階層 5 の標準承認テスト (サンドボックス) 環境に関連付けられた個々のサービスを再開することができます。

サービスを再起動するには、サポート チケットを作成し、次の詳細を入力します。

- **プロジェクト ID**: LCS プロジェクトの ID。
- **環境 ID**: 環境の URL にある GUID (環境 ID)。
- **再起動するサービス**: AOS、DIXF、MR、バッチ。
- **ダウンタイム開始**: 協定世界時 (UTC) でダウンタイム開始を指定します。
- **ダウンタイム終了**: UTC でダウンタイム終了を指定します。

> [!NOTE]
> この機能は、2019 年早期に Lifecycle Services (LCS) を通じたセルフ サービスになります。

## <a name="maintenance-mode"></a>メンテナンス モード
Finance and Operations には、[メンテナンス モード](../sysadmin/maintenance-mode.md)という名前のシステム全体に適用される設定が含まれています。 メンテナンス モードを有効にすると、システム機能に影響を与える可能性のあるシステム変更を、システム管理者が安全に実行する方法が提供されます。 たとえば、コンフィギュレーション キーは、有効または無効にすることができます。 メンテナンス モードがオンのとき、システム管理者およびメンテナンス モード ユーザー ロールが割り当てられたユーザーのみがシステムにサインインすることができます。 既定では、メンテナンス モードがオフになっています。

メンテナンス モードを有効/無効にするには、サポート チケットを作成し、次の情報を入力します。

- **プロジェクト ID**: LCS プロジェクトの ID。
- **環境 ID**: 環境の URL にある GUID (環境 ID)。
- **メンテナンス モードを有効化する開始時刻**: メンテナンス モードを有効にする開始時刻を UTC で指定します。
- **メンテナンス モードを無効化する開始時刻**: メンテナンス モードを無効にする開始時刻を UTC で指定します。

> [!NOTE]
> この機能は、2019 年早期に Lifecycle Services (LCS) を通じたセルフ サービスになります。

## <a name="access-database"></a>データベースへのアクセス
[セルフサービス配置](infrastructure-stack.md)エクスペリエンスを使用して配置された環境では、リモート デスクトップ アクセスがオフになっています。 Finance and Operations の実装の一環として、トラブルシューティングのために標準受け入れテスト環境でデータベースに接続する必要がある場合、サポート チケットを作成し、次の情報を入力します。

- **プロジェクト ID**: LCS プロジェクトの ID。
- **環境 ID**: 環境の URL にある GUID (環境 ID)。
- **実行する必要があるクエリ**: 実行するクエリです。

> [!NOTE]
> この機能は、2019 年早期に Lifecycle Services (LCS) を通じたセルフ サービスになります。 Azure SQL データベースへのアクセスは永続的ではありません。ただし、Lifecycle Services 環境の詳細ページを使用して直接データベースへのアクセスを要求することができます。   アクセスを取得するプロセスは次のようになります。
>- SQL Management Studio を使用して Azure SQL データベースに接続するために使用するコンピューターの IP アドレスをホワイトリストに追加することで、LCS を通じて Azure SQL へのアクセスを有効にします。 
>- その後、アクセスを要求する理由を入力することにより、アクセスを要求して LCS を通じてデータベースの資格情報を参照できます。 
>- 要求を送信するとすぐに**自動承認**されます。 数分以内に LCS 環境の詳細ページでデータベース アクセスの資格情報を確認できるようになります。 
>- 資格情報は 8 時間有効であり、その期間の後に有効期限が切れることに注意してください。 8 時間の後、アクセス権が有効期限切れになり、もう一度アクセス権を要求する必要があります。 
> 上記の手順を実行する方法の詳細については、この機能が 1 月に Lifecycle Services から利用可能になるとすぐに公開されます。


