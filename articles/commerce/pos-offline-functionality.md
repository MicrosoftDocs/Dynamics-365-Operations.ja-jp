---
title: オフライン販売時点管理 (POS) の機能
description: この記事では、Commerce Scale Unit が利用できない場合にチャンネルのデータベースからオフライン データベースに POS デバイスが自動的に切り替わる、Modern POS のオフライン モードについて説明します。 また、この記事ではオフライン モードの一般的な設定情報も含まれ、オフライン データベースとチャンネルのデータベース間で発生するデータ同期についても説明します。
author: josaw1
ms.date: 08/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTerminalTable
audience: IT Pro
ms.reviewer: josaw
ms.custom: 27041
ms.assetid: 20b51874-8912-40cf-9296-864df707315a
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a7b8480679509db7b4a9fa1d29d1ef871afa1db0
ms.sourcegitcommit: 09d4805aea6d148de47c8ca38d8244bbce9786ce
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/31/2022
ms.locfileid: "9386996"
---
# <a name="offline-point-of-sale-pos-functionality"></a>オフライン販売時点管理 (POS) の機能

[!include [banner](includes/banner.md)]

この記事では、Commerce Scale Unit が利用できない場合にチャンネルのデータベースからオフライン データベースに POS デバイスが自動的に切り替わる、Modern POS のオフライン モードについて説明します。 また、この記事ではオフライン モードの一般的な設定情報も含まれ、オフライン データベースとチャンネルのデータベース間で発生するデータ同期についても説明します。

Modern POS では、Commerce Scale Unit が利用できないときはいつでも 販売時点管理 (POS) デバイスがオフライン モードになります。 したがって、接続が失われると、POS はオフライン データベースに自動的に切り替わります。 

販売トランザクション中に、オフライン プロファイルでコンフィギュレーションされたタイムアウトの間隔内でデータの要求が成功しなかった場合、POS は自動的にオフライン データベースに切り替わり、販売トランザクションを続行します。 POS デバイスがオフライン モードの間に、Modern POS はオフライン プロファイルでコンフィギュレーションされた再接続試行間隔の後に Commerce Scale Unit との再接続を試みます。 この再接続試行は、トランザクションの先頭でのみ実行されます。

### <a name="determining-the-connection-mode-of-modern-pos"></a>Modern POS の接続モードの決定

Modern POS のステータス ヘッダーは現在の接続ステータスを表示し、**接続ステータス** ウィンドウはオフライン データベースと同期する最後の試行のステータスを表示します。

[![接続ステータス。](./media/status.png)](./media/status.png)

### <a name="creating-a-button-to-manually-switch-between-online-and-offline-modes"></a>手動でオンラインとオフライン モードを切り替えるためのボタンを作成

Modern POS にオンラインとオフライン モードを手動で切り替えるボタンを追加できます。 POS 操作 **917 – データベース接続ステータス** のボタンを作成します。 このボタンの名前は、POS が Commerce Scale Unit に接続されている場合は **接続解除** となり、接続解除されている場合は **接続** となります。 このボタンは接続の表示、Commerce Scale Unit との接続解除および接続に使用できます。

[![Retail Modern POS の接続解除ボタン。](./media/details-1024x537.png)](./media/details.png)

## <a name="setup"></a>段取り

POS のデバイス (登録) のオフライン サポートを有効にするには、**登録** ページで、**オフラインのサポート** オプションを **はい** に設定します。 新しいチャンネル データベース エンティティが作成され、店舗のチャンネル データ グループに追加されます。 その後、オフライン データベースのデータ パッケージを生成するためにすべての配送スケジュールを実行します。 次に、Modern POS のオフライン バージョンをインストールします。 インストール プロセスでは、オフライン データベースが作成されます。 必要に応じて、現在サポートされているバージョンの Microsoft SQL Server Express もインストールします。 (現在、SQL 2019 が最新バージョンです)。 Modern POS への最初のサインイン後にオフライン データの同期が開始されます。

## <a name="data-synchronization"></a>データ同期

コマース スケジューラはオフライン データベースにマスター データを送信するのに使用されます。 既定では、配送スケジュールの実行時に、データの変更がチャンネルのデータベースとオフライン データベースの両方に送信されます。 Modern POS には、使用可能なすべてのデータ パッケージをダウンロードし、オフライン データベースに挿入する async sync ライブラリが含まれます。 トランザクションがオフラインで作成された場合、POS はそれらを Commerce Scale Unit にアップロードし、チャンネル データベースに挿入できるようにします。 オフラインのデータ同期は、Modern POS の実行時にのみ実行できます。

[![オフライン同期。](./media/offline-sync-1024x521.png)](./media/offline-sync.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
