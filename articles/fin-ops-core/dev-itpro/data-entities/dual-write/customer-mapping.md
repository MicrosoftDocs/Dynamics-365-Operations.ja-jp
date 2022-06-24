---
title: 統合された顧客マスター
description: この記事では、財務と運用と Dataverse 間の顧客データの統合について説明します。
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 042042bb19b32d3c96b4e0c8521a8b1d65e7ab22
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890459"
---
# <a name="integrated-customer-master"></a>統合された顧客マスター

[!include [banner](../../includes/banner.md)]



顧客データは、複数の Dynamics 365 アプリケーションでマスターできます。 たとえば、顧客行は Dynamics 365 sales (Customer Engagement アプリ) の営業活動から発生する場合があり、または行が Dynamics 365 Commerce (財務と運用アプリ) の小売活動を通じて発生する場合があります。 顧客データの発生元の場所を問わず、バックグラウンドで統合されます。 統合された顧客マスターを使用すると、任意の Dynamics 365 アプリケーションに顧客データをマスタに分配することができ、Dynamics 365 application スイートを介して顧客の包括的なビューを表示できます。

## <a name="customer-data-flow"></a>顧客データ フロー

*顧客* は、アプリケーションで明確に定義された概念です。 したがって、顧客データの統合は、2 つのアプリケーションの間で顧客の概念を調和させるだけです。 次の図は、顧客データ フローを示します。

![顧客データ フロー。](media/dual-write-customer-data-flow.png)

顧客は、商用 / 組織の顧客および消費者 / エンド ユーザーの 2 種類に大きく分類できます。 これら 2 種類の顧客は、Finance and Operations と Dataverseにて、異なる方法で格納および処理されます。

Finance and Operations では、商用 / 組織の顧客および消費者 / エンド ユーザーの両方が、**CustTable** (CustCustomerV3Entity) という名前の単一のテーブルで習得され、**タイプ** 属性に基づいて分類されます。 (**タイプ** が **組織** に設定されている場合、顧客は商用/組織の顧客であり、**タイプ** が **個人** に設定されている場合、顧客はコンシューマー/エンド ユーザーです。) 主な連絡担当者情報は、SMMContactPersonEntity テーブルを介して処理されます。

Dataverse では、商取引/組織の顧客はアカウント テーブルで習得され、**RelationshipType** 属性が **顧客** に設定されている場合、顧客として識別されます。 コンシューマ/エンド ユーザーと連絡担当者の両方が、連絡先テーブルによって表されます。 コンシューマー/エンド ユーザーと連絡担当者の間を明確に分離するために、**連絡先** テーブルには **販売可能** という名前のブール値フラグがあります。 **販売可能** が **True** の場合、連絡先はコンシューマー / エンド ユーザーであり、その連絡先に対して見積と注文を作成できます。 **販売可能が** が **False** の場合、連絡先は顧客の主要な連絡担当者にすぎません。

販売不能な取引先担当者が見積または注文プロセスに参加する場合、**販売可能** が **True** に設定され、取引先担当者に販売可能な取引先担当者としてフラグが設定されます。 販売可能な取引先担当者になった連絡先は、引き続き販売可能な連絡先です。

## <a name="templates"></a>テンプレート

顧客データには、顧客グループ、住所、連絡先情報、支払プロファイル、請求書プロファイル、およびロイヤルティ ステータスなど、顧客に関するすべての情報が含まれます。 次の表に示すように、テーブル マップのコレクションは、顧客データ操作中に連携して動作します。

財務と運用アプリ | Customer Engagement アプリ         | 説明
----------------------------|---------------------------------|------------
[CDS 連絡先 V2](mapping-reference.md#115) | 連絡先 | このテンプレートでは、顧客と仕入先の両方について、基本、二次、三次の連絡先情報がすべて同期されます。
[顧客グループ](mapping-reference.md#126) | msdyn_customergroups | このテンプレートは、顧客グループ情報を同期します。
[顧客支払方法](mapping-reference.md#127) | msdyn_customerpaymentmethods | このテンプレートは、顧客支払方法に関する情報を同期します。
[顧客 V3](mapping-reference.md#101) | 勘定 | このテンプレートは、商業および組織顧客の顧客マスター情報を同期します。
[顧客 V3](mapping-reference.md#116) | 連絡先 | このテンプレートは、消費者およびエンド ユーザーの顧客マスター データを同期します。
[名前の接辞](mapping-reference.md#155) | msdyn_nameaffixes | このテンプレートは、顧客および仕入先の名前の接辞に関する参照データを同期します。
[支払期日明細行 CDS V2](mapping-reference.md#157) | msdyn_paymentdaylines | このテンプレートは、顧客および仕入先の支払期日明細行に関する参照データを同期します。
[支払期日 CDS](mapping-reference.md#158) | msdyn_paymentdays | このテンプレートは、顧客および仕入先の支払期日に関する参照データを同期します。
[支払スケジュール行](mapping-reference.md#159) | msdyn_paymentschedulelines | 顧客および仕入先の支払スケジュール明細行に関する参照データを同期します。
[支払スケジュール](mapping-reference.md#160) | msdyn_paymentschedules | このテンプレートは、顧客および仕入先の支払スケジュールに関する参照データを同期します。
[支払条件](mapping-reference.md#161) | msdyn_paymentterms | このテンプレートは、顧客および仕入先の支払条件 (支払に関する条件) に関する参照データを同期します。

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
