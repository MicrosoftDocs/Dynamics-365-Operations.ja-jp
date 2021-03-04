---
title: 統合された仕入先マスター
description: このトピックでは、Finance and Operations アプリと Dataverse 間の仕入先データの統合について説明します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
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
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 636bc57b5ef09d605744f4857fd5fbefceac4875
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685488"
---
# <a name="integrated-vendor-master"></a>統合された仕入先マスター

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



*仕入先* という用語は、サプライヤー組織、または会社に商品やサービスを提供している唯一の個人事業主を指します。 *仕入先* は、Microsoft Dynamics 365 Supply Chain Management で確立されていますが、Dynamics 365 のモデル駆動型アプリには仕入先の概念は存在しません。 ただし、**取引先企業 / 連絡先** エンティティをオーバーロードして、仕入先情報を格納することができます。 この統合型仕入先マスターは、Dynamics 365のモデル駆動アプリケーションで明示的なベンダー概念を導入します。 新しい仕入先設計を使用するか、仕入先データを **取引先企業 / 連絡先** エンティティに格納することができます。 デュアル書き込みでは、両方の手法がサポートされます。

どちらの手法でも、仕入先データは Dynamics 365 Supply Chain Management、Dynamics 365 Sales、Dynamics 365 Field Service、および Power Apps の各ポータル間で統合されます。 Supply Chain Management では、購買要求や発注書などのワークフローでデータを使用できます。

## <a name="vendor-data-flow"></a>仕入先データ フロー

仕入先データを Dataverse の **取引先企業 / 連絡先** エンティティに格納しない場合は、新規仕入先設計を使用できます。

![仕入先データ フロー](media/dual-write-vendor-data-flow.png)

**取引先企業 / 連絡先** で仕入先データを格納し続ける場合は、この拡張仕入先設計を使用できます。 拡張仕入先設計を使用するには、デュアル書き込みソリューション パッケージで仕入先ワークフローをコンフィギュレーションする必要があります。 詳細については、[仕入先設計間での切り替え](vendor-switch.md) を参照してください。

![拡張された仕入先データ フロー](media/dual-write-vendor-detail.jpg)

> [!TIP]
> セルフサービス仕入先の Power Apps ポータルを使用している場合は、その仕入先情報は Finance and Operations アプリに直接フローできます。

## <a name="templates"></a>テンプレート

仕入先データには、仕入先グループ、住所、連絡先情報、支払プロファイル、請求書プロファイル、およびロイヤルティ ステータスなど、仕入先に関するすべての情報が含まれます。 次の表に示すように、テーブル マップのコレクションは、仕入先データの操作中に連携して動作します。

Finance and Operations アプリ | その他の Dynamics 365 アプリ     | 説明
----------------------------|-----------------------------|------------
仕入先 V2                   | 口座                     | アカウント エンティティを使用して仕入先情報を格納する企業は、引き続き同じ方法で使用できます。 また、Finance and Operations アプリ統合により、明示的な仕入先機能を利用することもできます。
仕入先 V2                   | Msdyn\_vendors              | 仕入先向けのカスタム ソリューションを使用する企業は、Finance and Operations アプリ統合による Dataverse で導入されている直定の仕入先概念を利用できます。 
仕入先グループ               | msdyn\_vendorgroups         | このテンプレートは、仕入先グループ情報を同期します。
仕入先支払方法       | msdyn\_vendorpaymentmethods | このテンプレートは、仕入先支払方法に関する情報を同期します。
CDS 連絡先 V2             | 連絡先                    | [連絡先](customer-mapping.md#cds-contacts-v2-to-contacts) テンプレートでは、顧客と仕入先の両方について、基本、二次、三次の連絡先情報がすべて同期されます。
支払スケジュール行      | msdyn\_paymentschedulelines | [支払スケジュール行](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines) テンプレートは、顧客および仕入先の参照データを同期します。
支払スケジュール            | msdyn\_paymentschedules     | [支払スケジュール](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules) テンプレートは、顧客および仕入先の支払スケジュールに関する参照データを同期します。
支払期日明細行 CDS V2    | msdyn\_paymentdaylines      | [支払期日明細行](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) テンプレートは、顧客および仕入先の支払期日明細行に関する参照データを同期します。
支払期日 CDS            | msdyn\_paymentdays          | [支払期日](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays) テンプレートは、顧客および仕入先の支払期日に関する参照データを同期します。
支払条件            | msdyn\_paymentterms         | [支払条件](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms) テンプレートは、顧客および仕入先の支払条件に関する参照データを同期します。
名前の接辞                | msdyn\_nameaffixes          | [名前の接辞](customer-mapping.md#name-affixes-to-msdyn_nameaffixes) テンプレートは、顧客および仕入先の名前の接辞に関する参照データを同期します。

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [Vendors](includes/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](includes/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](includes/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]