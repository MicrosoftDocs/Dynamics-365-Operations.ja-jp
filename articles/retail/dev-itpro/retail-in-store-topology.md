---
title: ストア内トポロジを選択します。
description: このトピックでは、様々な Dynamics 365 for Retail の実店舗構成図を提供します。
author: rassadi
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: Dynamics-365-retail
ms.technology: ''
ms.search.form: SysAADClientTable, RetailTransactionServiceProfile
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Operations, Retail, Core
ms.custom: 44351
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 062e4490306f09f11d7821f40044de3a901f4067
ms.sourcegitcommit: 308d116994e4a5a6e92750ed24b471c90b5f3cfc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/26/2019
ms.locfileid: "897888"
---
# <a name="select-an-in-store-topology"></a>ストア内トポロジを選択します。

[!include [banner](../../includes/banner.md)]

このトピックでは、様々な Dynamics 365 for Retail の実店舗構成図の概要を提供します。 

<a href="https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/dev-itpro/media/channel/instore/topology.jpg" rel="some text">![店舗の構成図で右の小売りを選択します。](media/CHANNEL/INSTORE/Topology.jpg)</a>

## <a name="supported-capabilities-when-connectivity-is-lost"></a>接続が失われたときにサポートしている機能
| 操作 | 小売りサーバーへの接続がされていないとき<br>MPOS オフライン モード | 本部への接続がされていないとき<br>(RSSUを使用) |
| --- | :-: | :-: |
| クロス ターミナル シフト (ビュー、中断、再開、切断など) | | ✔ | 
| クロス ターミナル トランザクション (ビュー、中断、再開など)  | | ✔ |

## <a name="supported-operations-when-connectivity-is-lost"></a>接続が失われたときにサポートしている操作
POSが本部との接続を失った場合にサポートしている宗さんの一覧については、 [オンラインおよびオフラインでの店頭(POS)操作](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/pos-operations) 参照してください。。

## <a name="supported-deployment-and-maintenance-capabilities"></a>サポートされている導入及びメンテナンスの機能
最新のPOSでは、大規模な一括配置をサポートしていますが、 Retail Store Scale Unit では未対応となっています。 詳細については、 [Retail セルフサービス コンポーネントの一括配置](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/dev-itpro/retail-mass-deployment) をご参照ください。

## <a name="deployed-components"></a>配置可能なコンポーネント
次に示すコンポーネントは、すべて1つのインストーラーを使って配置されます。 これらをそれぞれ個別でインストールする必要はありません。

### <a name="modern-pos"></a>Modern POS
| 配置可能なコンポーネント | コンポーネント タイプ | 摘要 |
| --- | --- | --- |
| 最新のPOSアプリケーション | ユニバーサル Windows プラットフォーム アプリケーション | レジで稼働する最新のPOSアプリケーションです。 |
| 最新のPOS クライアント ブローカー | 最新のPOSのネイティブ バイナリをホストしているCOM Surrogate | オフラインモードでの操作の実行をサポートする Commerce Runtime を提供します。また、最新のPOSと本部とデータを同期するにはAsync Clientライブラリも同様に必要となります。 | 
| チャンネル データベース | SQL データベース | レジのデータを提供している特定のチャンネル データベース インスタンスを登録します。

### <a name="retail-store-scale-unit"></a>Retail Store Scale Unit
| インストールされたコンポーネント | コンポーネント タイプ | 摘要 |
| --- | --- | --- |
| Retail サーバー | IIS Web サービス | 1つ以上の店舗で使用する小売 Serverのインスタンスの単位を計測します。 |
| チャンネル データベース | SQL データベース | 1つ以上の店舗で使用するデータを提供する、特定のチャンネルデータベースインスタンスの店舗単位を計測します。 |
| Async Client サービス | Windows サービス | マスター レコード データを本部から店舗へ、取引データを店舗から本部へと同期するためのコンポーネント |

## <a name="additional-resources"></a>追加リソース
### <a name="mpos-offline-mode"></a>MPOS オフライン モード
MPOS オフラインモードの詳細については、以下を参照してください。
- [オフライン販売時点管理 (POS) の機能](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/pos-offline-functionality)
- [オンラインおよびオフラインでの販売時点管理 (POS) の操作](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/pos-operations)
- [Retail セルフサービス コンポーネントの一括配置](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/dev-itpro/retail-mass-deployment)

### <a name="retail-store-scale-unit"></a>Retail Store Scale Unit 
Retail store scale unit は、実店舗などお客様の環境に配置することが可能な、バックオフィスや本部 (HQ) への通信が切断された場合でも継続して業務を行うことをサポートするコンポーネントです。 

詳細については、以下を参照してください。
- [Retail Store Scale Unit の設定とインストール](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/dev-itpro/retail-store-scale-unit-configuration-installation)
- [Retail Store Scale Unit](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/dev-itpro/retail-store-system-begin)
