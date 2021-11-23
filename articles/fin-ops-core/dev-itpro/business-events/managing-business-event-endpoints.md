---
title: ビジネス イベント エンドポイントの管理
description: このトピックでは、Finance and Operations アプリのビジネス イベント用エンドポイントの管理法方法について説明します。
author: jaredha
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-11-03
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 4f0d03714fa0076081dd997d93a01c784b4acc8d
ms.sourcegitcommit: f4823a97c856e9a9b4ae14116a43c87f9482dd90
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/09/2021
ms.locfileid: "7779922"
---
# <a name="manage-business-event-endpoints"></a>ビジネス イベント エンドポイントの管理
[!include[banner](../includes/banner.md)]

エンドポイントを使用すると、ビジネス イベントの送信先を管理できます。 Finance and Operations アプリのビジネス イベントは、次のエンドポイント タイプをサポートします。

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

Finance and Operations アプリでは、エンドポイントを準備しません。 エンドポイントを個別に作成し、アプリに提供する必要があります。 その後、アプリは用意されているイベントをエンドポイントに送信するだけです。 顧客が Azure サブスクリプションでこれらのエンドポイントを使用している場合、追加費用が発生する可能性があります。

## <a name="subscribing-to-finance-and-operations-apps-events-from-dataverse"></a>Dataverse から Finance and Operations アプリを登録

> [!IMPORTANT]
> Finance and Operations アプリのビジネス イベントと Microsoft Dataverse のデータ イベントに登録する前に、Microsoft Power Platform 統合を有効にする必用があります。 Finance and Operations アプリ環境の Microsoft Power Platform 統合を有効にする方法の詳細については、[Microsoft Power Platform 統合の有効化](../power-platform/enable-power-platform-integration.md) を参照してください。

Microsoft Power Platform 統合が有効になった後、Finance and Operations アプリ ビジネス イベントとデータ イベントを Dataverse から登録できます。 サブスクリプションでは次の機能が有効です。

- Dataverse の複数のアプリケーションからのイベントにまたがる一貫した動作
- Finance and Operations アプリからコンスタントに消費するための Dataverse ソリューションに向けたアプリケーション ライフサイクル管理 (ALM)
- Dataverse の Finance and Operations アプリ イベント上におけるプラグインとソフトウェア開発キット手順 (SDK) の登録

Microsoft Power Platform 統合が Finance and Operations アプリ環境に対して有効になると、ビジネス イベント用に作成されるエンドポイントは Dataverse でサポートされたエンドポイント タイプのリンクされた Microsoft Power Platform 環境に同期されます。 その後、エンドポイントは Microsoft Power Platform で使用できます。 エンドポイントを同期すると、Finance and Operations アプリから送信されたビジネス イベントは Dataverse からエンドポイントにプロキシされます。

次の表では、エンドポイントの Finance and Operations アプリと Dataverse 実装の間にマッピングを表示します。

| Finance and Operations アプリ エンドポイント タイプ | Dataverse サービス エンドポイント タイプ    | 
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
> エンドポイント タイプが Dataverse でサポートされていない場合、または Microsoft Power Platform 統合が有効でない場合は、エンドポイントは Dataverse 経由で送信する代わりに Finance and Operations アプリから引き続きイベントを送信します。

### <a name="viewing-or-creating-mapped-endpoints-in-dataverse"></a>Dataverse でマップされたエンドポイントの表示または作成

新しいエンドポイントが Finance and Operations アプリに追加された場合、そのエンドポイントは Dataverse に同期されます。 **ServiceEndpoint** テーブルの Dataverse で使用できるようになります。 また、**ServiceEndpoint** テーブルの Dataverse にエンドポイントを直接作成できます。 サービス エンドポイントを Finance and Operations アプリ イベントに登録して作成する場合、自動的に Finance and Operations アプリが利用でき、**ビジネス イベント** ページの **エンドポイント** タブに表示されます。 この動作は、マップされているエンドポイントの次のタイプに適用できます。

- Azure Service Bus キュー
- Azure Service Bus トピック
- Azure Event Grid
- Azure イベント ハブ

**ServiceEndpoint** テーブルの詳細については、[ServiceEndpoint テーブル/エンティティの参照](/powerapps/developer/data-platform/reference/entities/serviceendpoint) を確認してください。

### <a name="microsoft-power-automate-endpoints"></a>Microsoft Power Automate エンドポイント

**Microsoft Power Automate** エンドポイント タイプは、Finance and Operations アプリの設定に直接使用できません。 このエンドポイント タイプは、Power Automate のフローから直接作成および送信されるサブスクリプションに使用されます。 

Finance and Operations アプリ ビジネス イベントまたは Power Automate のデータ イベントに登録する際は、エンドポイントは Finance and Operations の **ビジネス イベント** ページの **エンドポイント** タブで作成されます。 Power Automate のビジネス イベントとデータ イベントの登録方法については、[Microsoft Power Automate のビジネス イベント](business-events-flow.md) を参照してください。

### <a name="microsoft-dataverse-endpoints"></a>Microsoft Dataverse エンドポイント

また **Dataverse** エンドポイント タイプは、Finance and Operations アプリでの手動手順には使用できません。 エンドポイントは、プラグインまたは SDK 手順が Finance and Operations アプリ ビジネス イベントまたは Dataverse のデータ イベントに登録される際、作成されます。 手順が登録されると、Finance and Operations アプリの **ビジネス イベント** ページの **エンドポイント** タブ上リストにあるエンドポイントとして表示されます。 

![Finance and Operations アプリのビジネス イベント ページにある Dataverse タイプのエンドポイント。](../media/businessevents_DataverseEndpoint.png)

ビジネス イベント登録自体は、登録に応じて、Finance and Operations アプリの **ビジネス イベント** ページにある **ビジネス イベント カタログ** タブまたは **データ イベント カタログ** タブのどちらかにも表示されます。 これにより、Finance and Operations アプリ ユーザーは、ビジネス イベントかデータ イベントのどちらが Dataverse に登録されているプラグインまたは SDK 手順を所持してるか確認できます。 また、Finance and Operations アプリでイベントを有効にした理由も確認できます。

Finance and Operations アプリ イベントは、Visual Studio 用 Power Platform Tools 拡張機能などの Dataverse ツールセットのツールを使用して、Dataverse に直接登録できます。 この拡張機能の詳細については、[Power Platform Tools のインストール](/powerapps/developer/data-platform/tools/devtools-install)を参照してください。 これらのサブスクリプションは、Finance and Operations アプリの **ビジネス イベント** ページにある **ビジネス イベント カタログ** タブに表示されます。

名前や説明など、Dataverse のサービス エンドポイントの一部の属性を更新できます。 これらの更新は、Finance and Operations アプリにも反映されます。 ただし、サービス エンドポイントが Finance and Operations アプリ イベントで使用されている場合、サービス エンドポイント タイプを変更する更新は防止されます。 これらの更新には、Service Bus トピックから Service Bus キューへの変更が含まれます。通常 Dataverse は許可されます。 Finance and Operations アプリはエンドポイントの作成後にこれらの更新を行うことを許可しないので、この動作はデザインの動作と整合性を保証します。

サービス エンドポイントの作成後、使用されている場合は、Dataverse はサービス エンドポイントを削除できません。 この制限は、Finance and Operations アプリ イベントで使用されるサービス エンドポイントにも適用されます。 これらのエンドポイントのいずれかを削除しようとするとエラーが発生し、削除が防止されます。 

Dataverse の Finance and Operations アプリ ビジネス イベントの登録方法については、[イベントを Dataverse に登録](how-to/how-to-dataverse-events.md) を参照してください。
