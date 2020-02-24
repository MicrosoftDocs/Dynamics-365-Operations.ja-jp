---
title: 統合された仕入先マスター
description: このトピックでは、Finance and Operations アプリと Common Data Service 間の仕入先データの統合について説明します。
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 2442a6869daac22a435c1a7504b93ea4b5c14747
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019874"
---
# <a name="integrated-vendor-master"></a>統合された仕入先マスター

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

*仕入先*という用語は、サプライ チェーン プロセスの一部で、ビジネスに商品を供給するサプライヤー組織または個人事業主を指します。 *仕入先*は、Finance and Operations アプリで確立された概念ですが、他の Dynamics 365 アプリには仕入先の概念は存在しません。 代わりに、一部の企業は顧客情報と仕入先情報の両方を格納するために、アカウント エンティティを過負荷にします。 他の企業では、カスタム ベンダーの概念を使用します。 Common Data Service 統合は、これらの設計の両方をサポートします。 したがって、ビジネス シナリオに応じて、いずれかの設計を有効にできます。

Finance and Operations アプリと他の Dynamics 365 アプリ間の仕入先データの統合により、データをマルチ マスターにできます。 仕入先データの発生元にかかわらず、アプリケーションの境界およびインフラストラクチャの違いを越えてバックグラウンドで統合されます。 

### <a name="vendor-data-flow"></a>仕入先データ フロー

仕入先のマスタリングにその他の Dynamics 365 アプリを使用し、顧客情報から仕入先情報を分離する場合は、新しい仕入先設計を使用できます。

![仕入先データ フロー](media/dual-write-vendor-data-flow.png)

仕入先のマスタリングにその他の Dynamics 365 アプリを使用し、仕入先情報を格納するためアカウント エンティティを使用し続ける場合は、新しく拡張された仕入先設計を使用できます。 この設計では、仕入先グループおよび仕入先転記プロファイルなどの拡張された仕入先情報が仕入先詳細に保存されます。

![拡張された仕入先データ フロー](media/dual-write-vendor-detail.jpg)

仕入先の連絡先情報は、顧客の連絡先情報に似ています。 その背後では、連絡担当者の情報が保存され、同じエンティティから取得されます。

## <a name="templates"></a>テンプレート

仕入先データには、仕入先グループ、住所、連絡先情報、支払プロファイル、請求書プロファイル、およびロイヤルティ ステータスなど、仕入先に関するすべての情報が含まれます。 次の表に示すように、エンティティ マップのコレクションは、仕入先データの操作中に連携して動作します。

Finance and Operations アプリ | その他の Dynamics 365 アプリ         | 説明
----------------------------|---------------------------------|------------
仕入先 V2               | 口座 | アカウント エンティティを使用して仕入先情報を格納する企業は、引き続き同じ方法で使用できます。 また、Finance and Operations アプリ統合により、明示的な仕入先機能を利用することもできます。
仕入先 V2               | Msdyn\_vendors | 仕入先向けのカスタム ソリューションを使用する企業は、Finance and Operations アプリ統合による Common Data Service で導入されている直定の仕入先概念を利用できます。 
仕入先グループ | msdyn_vendorgroups | このテンプレートは、仕入先グループ情報を同期します。
仕入先支払方法 | msdyn_vendorpaymentmethods | このテンプレートは、仕入先支払方法に関する情報を同期します。
CDS 連絡先 V2             | 連絡先                        | [連絡先](customer-mapping.md#cds-contacts-v2-to-contacts) テンプレートでは、顧客と仕入先の両方について、基本、二次、三次の連絡先情報がすべて同期されます。
支払スケジュール行      | msdyn_paymentschedulelines      | [支払スケジュール行](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines) テンプレートは、顧客および仕入先の参照データを同期します。
支払スケジュール            | msdyn_paymentschedules          | [支払スケジュール](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules) テンプレートは、顧客および仕入先の支払スケジュールに関する参照データを同期します。
支払期日明細行 CDS V2    | msdyn_paymentdaylines           | [支払期日明細行](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) テンプレートは、顧客および仕入先の支払期日明細行に関する参照データを同期します。
支払期日 CDS            | msdyn_paymentdays               | [支払期日](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays) テンプレートは、顧客および仕入先の支払期日に関する参照データを同期します。
支払条件            | msdyn_paymentterms              | [支払条件](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms) テンプレートは、顧客および仕入先の支払条件に関する参照データを同期します。
名前の接辞                | msdyn_nameaffixes               | [名前の接辞](customer-mapping.md#name-affixes-to-msdyn_nameaffixes) テンプレートは、顧客および仕入先の名前の接辞に関する参照データを同期します。

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [Vendors](includes/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](includes/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](includes/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]
