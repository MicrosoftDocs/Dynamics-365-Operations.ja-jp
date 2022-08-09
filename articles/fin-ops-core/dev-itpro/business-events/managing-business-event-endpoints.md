---
title: ビジネス イベント エンドポイントの管理
description: この記事では、財務と運用アプリのビジネス イベント用エンドポイントの管理方法について説明します。
author: jaredha
ms.date: 06/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-11-03
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 69aa947ad3a31be3187436e051e42f4a7f700dba
ms.sourcegitcommit: bba5ef41aeda7c0ef5a24bf38638126a8a62f23b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9080652"
---
# <a name="manage-business-event-endpoints"></a>ビジネス イベント エンドポイントの管理
[!include[banner](../includes/banner.md)]

エンドポイントを使用すると、ビジネス イベントの送信先を管理できます。 財務と運用アプリのビジネス イベントは、次のエンドポイント タイプをサポートします。

| エンドポイントの種類 | チュートリアル |
| ------------- | -------- |
| Azure Service Bus キュー | [ビジネス イベントおよび Azure Service Bus](how-to/how-to-servicebus-queue.md) |
| Azure Service Bus トピック | [ビジネス イベントおよび Azure Service Bus](how-to/how-to-servicebus.md) |
| Azure Event Grid | [ビジネス イベントおよび Azure Event Grid](how-to/how-to-eventgrid.md) |
| Azure イベント ハブ | [ビジネス イベント と Azure イベントのハブ](how-to/event-hub.md) |
| Azure Blob Storage | 該当なし |
| HTTPS | 該当なし |
| Microsoft Power Automate | [ビジネス イベントと Microsoft Power Automate](how-to/how-to-flow.md) |
| Dataverse | [Dataverse のイベントを登録](how-to/how-to-dataverse-events.md) |

直ちに、これらのメッセージングおよびイベント ブローカーのエンドポイントを作成できます。 消費者にビジネス イベントを組織化して配布するため、複数のエンドポイントが必要になる場合があります。 このようなシナリオをサポートするため、複数のエンドポイントを作成することができます。

Microsoft Azure ベースのエンドポイントは、顧客の Azure サブスクリプションに含まれている必要があります。 たとえば、イベント グリッドをエンドポイントとして使用する場合は、エンドポイントが顧客の Azure サブスクリプションに含まれている必要があります。

財務と運用アプリは、エンドポイントをプロビジョニングしません。 エンドポイントを個別に作成し、アプリに提供する必要があります。 その後、アプリは用意されているイベントをエンドポイントに送信するだけです。 顧客が Azure サブスクリプションでこれらのエンドポイントを使用している場合、追加費用が発生する可能性があります。

## <a name="subscribing-to-finance-and-operations-apps-events-from-dataverse"></a>Dataverse から財務と運用アプリ イベントへのサブスクライブ

> [!IMPORTANT]
> 財務と運用アプリのビジネス イベントと Microsoft Dataverse のデータ イベントに登録する前に、Microsoft Power Platform 統合を有効にする必用があります。 財務と運用アプリ環境の Microsoft Power Platform 統合を有効にする方法の詳細については、[Microsoft Power Platform 統合の有効化](../power-platform/enable-power-platform-integration.md)を参照してください。

Microsoft Power Platform 統合が有効になった後、財務と運用アプリ ビジネス イベントとデータ イベントを Dataverse から登録できます。 サブスクリプションでは次の機能が有効です。

- Dataverse の複数のアプリケーションからのイベントにまたがる一貫した動作
- 財務と運用アプリから一貫して消費するイベントヘの Dataverse ソリューション向けアプリケーション ライフサイクル管理 (ALM)
- Dataverse の財務と運用アプリ イベント上におけるプラグインとソフトウェア開発キット (SDK) 手順の登録

Microsoft Power Platform 統合が財務と運用アプリ環境に対して有効になると、ビジネス イベント用に作成されるエンドポイントは、Dataverse でサポートされたエンドポイント タイプのリンクされた Microsoft Power Platform 環境に同期されます。 その後、エンドポイントは Microsoft Power Platform で使用できます。 エンドポイントを同期すると、財務と運用アプリから送信されたビジネス イベントは Dataverse からエンドポイントにプロキシされます。

次の表では、エンドポイントの財務と運用アプリと Dataverse 実装間のマッピングを表示します。

| 財務と運用アプリのエンドポイント タイプ | Dataverse サービス エンドポイント タイプ    | 
| ----------------------------------------- | ---------------------------------- |
| Azure Service Bus キュー                   | タイプ Queue の Azure Service Bus    | 
| Azure Service Bus トピック                   | タイプ トピック の Azure Service Bus    |
| Azure Event Grid                          | Azure Event Grid                   |
| Azure イベント ハブ                           | Azure イベント ハブ                    |
| HTTPS                                     | Webhook                            |
| Azure Blob Storage                        | Dataverse ではサポートされていません         |
| Microsoft Power Automate                  | 非同期コールバックの登録 |
| Dataverse                                 | プラグインまたは SDK 手順の登録   |

> [!NOTE]
> エンドポイント タイプが Dataverse でサポートされていない場合、または Microsoft Power Platform 統合が有効でない場合は、エンドポイントは Dataverse 経由で送信する代わりに、財務と運用アプリから引き続きイベントを送信します。

### <a name="viewing-or-creating-mapped-endpoints-in-dataverse"></a>Dataverse でマップされたエンドポイントの表示または作成

財務と運用アプリに新しいエンドポイントが追加されると、そのエンドポイントは Dataverse に同期されます。 **ServiceEndpoint** テーブルの Dataverse で使用できるようになります。 また、**ServiceEndpoint** テーブルの Dataverse にエンドポイントを直接作成できます。 サービス エンドポイントを財務と運用アプリ イベントに登録して作成する場合、自動的に財務と運用アプリが利用できるようになり、**ビジネス イベント** ページの **エンドポイント** タブに表示されます。 この動作は、マップされているエンドポイントの次のタイプに適用できます。

- Azure Service Bus キュー
- Azure Service Bus トピック
- Azure Event Grid
- Azure イベント ハブ

**ServiceEndpoint** テーブルの詳細については、[ServiceEndpoint テーブル/エンティティの参照](/powerapps/developer/data-platform/reference/entities/serviceendpoint) を確認してください。

> [!NOTE]
> エンドポイントを Dataverse でマップする場合、Dataverse IP アドレスを、ビジネス イベントおよびデータ イベントに対するファイアウォール ポリシーの許可リストに追加する必要があります。 ファイアウォール ポリシーに必要な IP アドレスの詳細情報については、[必要な IP アドレス](/power-platform/admin/online-requirements#ip-addresses-required)を参照してください。

### <a name="microsoft-power-automate-endpoints"></a>Microsoft Power Automate エンドポイント

**Microsoft Power Automate** エンドポイント タイプは、財務と運用アプリに直接設定することはできません。 このエンドポイント タイプは、Power Automate のフローから直接作成および送信されるサブスクリプションに使用されます。 

Power Automate で財務と運用アプリ ビジネス イベントまたはデータ イベントに登録する際は、エンドポイントは財務と運用アプリの **ビジネス イベント** ページの **エンドポイント** タブで作成されます。 Power Automate のビジネス イベントとデータ イベントの登録方法については、[Microsoft Power Automate のビジネス イベント](business-events-flow.md) を参照してください。

### <a name="microsoft-dataverse-endpoints"></a>Microsoft Dataverse エンドポイント

**Dataverse** エンドポイント タイプも、財務と運用アプリに手動で設定することはできません。 エンドポイントは、プラグインまたは SDK 手順が、Dataverse の財務と運用アプリ ビジネス イベントまたはデータ イベントに登録される際に作成されます。 手順が登録されると、財務と運用アプリの **ビジネス イベント** ページの **エンドポイント** タブ上リストにあるエンドポイントとして表示されます。 

![財務と運用アプリのビジネス イベント ページにある Dataverse タイプのエンドポイント。](../media/businessevents_DataverseEndpoint.png)

ビジネス イベント登録自体は、登録に応じて、財務と運用アプリの **ビジネス イベント** ページにある **ビジネス イベント カタログ** タブまたは **データ イベント カタログ** タブのどちらかにも表示されます。 これにより、財務と運用アプリ ユーザーは、ビジネス イベントかデータ イベントのどちらが Dataverse に登録されているプラグインまたは SDK 手順を所持しているか確認できます。 また、財務と運用アプリでイベントを有効にした理由も確認できます。

財務と運用アプリ イベントは、Visual Studio 用 Power Platform Tools 拡張機能などの Dataverse ツールセットのツールを使用して、Dataverse に直接登録できます。 この拡張機能の詳細については、[Power Platform Tools のインストール](/powerapps/developer/data-platform/tools/devtools-install)を参照してください。 これらの登録は、財務と運用アプリの **ビジネス イベント** ページにある **ビジネス イベント カタログ** タブに表示されます。

名前や説明など、Dataverse のサービス エンドポイントの一部の属性を更新できます。 これらの更新は、財務と運用アプリにも反映されます。 ただし、サービス エンドポイントが財務と運用アプリ イベントで使用されている場合、サービス エンドポイント タイプを変更する更新は妨げられます。 これらの更新には、Service Bus 記事から Service Bus キューへの変更が含まれます。通常 Dataverse は許可されます。 財務と運用アプリはエンドポイントの作成後にこれらの更新を行うことを許可しないので、この動作はデザインの動作と整合性を保証します。

サービス エンドポイントの作成後、使用されている場合は、Dataverse はサービス エンドポイントを削除できません。 この制限は、財務と運用アプリ イベントで使用されるサービス エンドポイントにも適用されます。 これらのエンドポイントのいずれかを削除しようとするとエラーが発生し、削除が防止されます。 

Dataverse の財務と運用アプリ ビジネス イベントの登録方法については、[イベントを Dataverse に登録する](how-to/how-to-dataverse-events.md)を参照してください。

