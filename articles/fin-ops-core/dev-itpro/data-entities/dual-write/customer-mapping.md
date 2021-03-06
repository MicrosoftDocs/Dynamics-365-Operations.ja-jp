---
title: 統合済み顧客マスター
description: このトピックでは、Finance and Operations と Dataverse 間の顧客データの統合について説明します。
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 0015ca2ccbb0098a5a96bf56ff355fb2f9f8f626
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748926"
---
# <a name="integrated-customer-master"></a>統合された顧客マスター

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


顧客データは、複数の Dynamics 365 アプリケーションでマスターできます。 たとえば、顧客行は Dynamics 365 Sales (Dynamics 365のモデル駆動型アプリ) の営業活動から発生する場合があり、行は Dynamics 365 Commerce ( Finance and Operationsアプリの) 小売活動を通じて発生する場合があります。 顧客データの発生元の場所を問わず、バックグラウンドで統合されます。 統合された顧客マスターを使用すると、任意の Dynamics 365 アプリケーションに顧客データをマスタに分配することができ、Dynamics 365 application スイートを介して顧客の包括的なビューを表示できます。

## <a name="customer-data-flow"></a>顧客データ フロー

*顧客* は、アプリケーションで明確に定義された概念です。 したがって、顧客データの統合は、2 つのアプリケーションの間で顧客の概念を調和させるだけです。 次の図は、顧客データ フローを示します。

![顧客データ フロー](media/dual-write-customer-data-flow.png)

顧客は、商用 / 組織の顧客および消費者 / エンド ユーザーの 2 種類に大きく分類できます。 これら 2 種類の顧客は、Finance and Operations と Dataverse にて、異なる方法で格納および処理されます。

Finance and Operations では、商用 / 組織の顧客および消費者 / エンド ユーザーの両方が、**CustTable** (CustCustomerV3Entity) という名前の単一のテーブルでマスターされ、**タイプ** 属性に基づいて分類されます。 (**タイプ** が **組織** に設定されている場合、顧客は商用/組織の顧客であり、**タイプ** が **個人** に設定されている場合、顧客はコンシューマー/エンド ユーザーです。) 主な連絡担当者情報は、SMMContactPersonEntity テーブルを介して処理されます。

Dataverse では、商取引/組織の顧客はアカウント テーブルで習得され、**RelationshipType** 属性が **顧客** に設定されている場合、顧客として識別されます。 コンシューマ/エンド ユーザーと連絡担当者の両方が、連絡先テーブルによって表されます。 コンシューマー/エンド ユーザーと連絡担当者の間を明確に分離するために、**連絡先** テーブルには **販売可能** という名前のブール値フラグがあります。 **販売可能** が **True** の場合、連絡先はコンシューマー / エンド ユーザーであり、その連絡先に対して見積と注文を作成できます。 **販売可能が** が **False** の場合、連絡先は顧客の主要な連絡担当者にすぎません。

販売不能な取引先担当者が見積または注文プロセスに参加する場合、**販売可能** が **True** に設定され、取引先担当者に販売可能な取引先担当者としてフラグが設定されます。 販売可能な取引先担当者になった連絡先は、引き続き販売可能な連絡先です。

## <a name="templates"></a>テンプレート

顧客データには、顧客グループ、住所、連絡先情報、支払プロファイル、請求書プロファイル、およびロイヤルティ ステータスなど、顧客に関するすべての情報が含まれます。 次の表に示すように、テーブル マップのコレクションは、顧客データ操作中に連携して動作します。

Finance and Operations アプリ | その他の Dynamics 365 アプリ         | 説明
----------------------------|---------------------------------|------------
CDS 連絡先 V2             | 連絡先                        | このテンプレートでは、顧客と仕入先の両方について、基本、二次、三次の連絡先情報がすべて同期されます。
顧客グループ             | msdyn_customergroups            | このテンプレートは、顧客グループ情報を同期します。
顧客支払方法     | msdyn_customerpaymentmethods    | このテンプレートは、顧客支払方法に関する情報を同期します。
顧客 V3                | 勘定                        | このテンプレートは、商業および組織顧客の顧客マスター情報を同期します。
顧客 V3                | 連絡先                        | このテンプレートは、消費者およびエンド ユーザーの顧客マスター データを同期します。
名前の接辞                | msdyn_nameaffixes               | このテンプレートは、顧客および仕入先の名前の接辞に関する参照データを同期します。
支払期日明細行 CDS V2    | msdyn_paymentdaylines           | このテンプレートは、顧客および仕入先の支払期日明細行に関する参照データを同期します。
支払期日 CDS            | msdyn_paymentdays               | このテンプレートは、顧客および仕入先の支払期日に関する参照データを同期します。
支払スケジュール行      | msdyn_paymentschedulelines      | 顧客および仕入先の支払スケジュール明細行に関する参照データを同期します。
支払スケジュール            | msdyn_paymentschedules          | このテンプレートは、顧客および仕入先の支払スケジュールに関する参照データを同期します。
支払条件            | msdyn_paymentterms              | このテンプレートは、顧客および仕入先の支払条件 (支払に関する条件) に関する参照データを同期します。

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](includes/CDSContactsV2-contacts.md)]

[!include [mapping customer group](includes/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](includes/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](includes/CustomersV3-accounts.md)]

[!include [mapping customer contacts](includes/CustomersV3-contacts.md)]

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]