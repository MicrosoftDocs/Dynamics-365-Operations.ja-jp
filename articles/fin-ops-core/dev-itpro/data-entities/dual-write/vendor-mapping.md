---
title: 統合された仕入先マスター
description: この記事は、財務と運用アプリと Dataverse 間の仕入先データの統合について説明します。
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: a2c32ef546a5bc74e090591c0ac9d51529299041
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2022
ms.locfileid: "9112205"
---
# <a name="integrated-vendor-master"></a>統合された仕入先マスター

[!include [banner](../../includes/banner.md)]



*仕入先* という用語は、サプライヤー組織、または会社に商品やサービスを提供している唯一の個人事業主を指します。 *仕入先* は、Microsoft Dynamics 365 Supply Chain Management で確立されていますが、Customer Engagement アプリには仕入先の概念は存在しません。 ただし、**取引先企業/連絡先** テーブルをオーバーロードして、仕入先情報を格納することができます。 この統合型仕入先マスターは、Customer Engagement アプリで明示的なベンダー概念を導入します。 新しい仕入先設計を使用するか、仕入先データを **取引先企業/連絡先** テーブルに格納することができます。 デュアル書き込みでは、両方の手法がサポートされます。

どちらの手法でも、仕入先データは Dynamics 365 Supply Chain Management、Dynamics 365 Sales、Dynamics 365 Field Service、および Power Apps の各ポータル間で統合されます。 Supply Chain Management では、購買要求や発注書などのワークフローでデータを使用できます。

## <a name="vendor-data-flow"></a>仕入先データ フロー

仕入先データを Dataverse の **取引先企業/連絡先** テーブルに格納しない場合は、新規仕入先設計を使用できます。

![仕入先データ フロー。](media/dual-write-vendor-data-flow.png)

**取引先企業/連絡先** テーブルで仕入先データを格納し続ける場合は、この拡張仕入先設計を使用できます。 拡張仕入先設計を使用するには、デュアル書き込みソリューション パッケージで仕入先ワークフローをコンフィギュレーションする必要があります。 詳細については、[仕入先設計間での切り替え](vendor-switch.md) を参照してください。

![拡張された仕入先データ フロー。](media/dual-write-vendor-detail.jpg)

> [!TIP]
> セルフサービス仕入先の Power Apps ポータルを使用している場合は、その仕入先情報は財務と運用アプリに直接フローできます。

## <a name="templates"></a>テンプレート

仕入先データには、仕入先グループ、住所、連絡先情報、支払プロファイル、請求書プロファイル、およびロイヤルティ ステータスなど、仕入先に関するすべての情報が含まれます。 次の表に示すように、テーブル マップのコレクションは、仕入先データの操作中に連携して動作します。

財務と運用アプリ | Customer Engagement アプリ     | 説明
----------------------------|-----------------------------|------------
[CDS 連絡先 V2](mapping-reference.md#115) | 連絡先 | このテンプレートでは、顧客と仕入先の両方について、基本、二次、三次の連絡先情報がすべて同期されます。
[名前の接辞](mapping-reference.md#155) | msdyn_nameaffixes | このテンプレートは、顧客および仕入先の名前の接辞に関する参照データを同期します。
[支払期日明細行 CDS V2](mapping-reference.md#157) | msdyn_paymentdaylines | このテンプレートは、顧客および仕入先の支払期日明細行に関する参照データを同期します。
[支払期日 CDS](mapping-reference.md#158) | msdyn_paymentdays | このテンプレートは、顧客および仕入先の支払期日に関する参照データを同期します。
[支払スケジュール行](mapping-reference.md#159) | msdyn_paymentschedulelines | 顧客および仕入先の支払スケジュール明細行に関する参照データを同期します。
[支払スケジュール](mapping-reference.md#160) | msdyn_paymentschedules | このテンプレートは、顧客および仕入先の支払スケジュールに関する参照データを同期します。
[支払条件](mapping-reference.md#161) | msdyn_paymentterms | このテンプレートは、顧客および仕入先の支払条件 (支払に関する条件) に関する参照データを同期します。
[仕入先 V2](mapping-reference.md#202) | msdyn_vendors | 仕入先向けのカスタム ソリューションを使用する企業は、財務と運用アプリ統合の Dataverse により導入されている直定の仕入先概念を利用できます。
[仕入先グループ](mapping-reference.md#200) | msdyn_vendorgroups | このテンプレートは、仕入先グループ情報を同期します。
[仕入先支払方法](mapping-reference.md#201) | msdyn_vendorpaymentmethods | このテンプレートは、仕入先支払方法に関する情報を同期します。

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

