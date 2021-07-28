---
title: 給与統合 API の概要
description: このトピックでは、Dynamics 365 Human Resources 給与統合 API について説明します。
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3b6b01053a043477521d7eb1a41bb9f6f51fc0e4
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6360571"
---
# <a name="payroll-integration-api-introduction"></a>給与統合 API の概要

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このドキュメントでは、Dynamics 365 Human Resources 給与統合 API について説明します。 API を使用すると、人事管理と給与システム パートナー間のエンド ツー エンドの統合を合理化できます。 統合された経験は、Human Resources で、従業員のプロファイル、給与と控除、および貢献度情報で始まります。 従業員を雇用し、必要なプロファイルと給与情報を Human Resources に入力すると、給与システムはこの情報を取得して、給与の処理時に使用します。 従業員に対して行われた更新や支払情報も、後で支払の実行で使用されます。

[![給与統合フロー。](media/hr-admin-integration-payroll-api-introduction-flow.png)](media/hr-admin-integration-payroll-api-introduction-flow-2.png#lightbox)

統合を有効にするため、Human Resources は、次のコンポーネントが含まれます。

- 従業員に支払準備完了をマークするための機能
- アプリケーションを統合する新機能をオープンにした統合 API

## <a name="microsoft-dataverse"></a>Microsoft Dataverse

この API は Microsoft Dataverse (旧 Common Data Service) に構築されています。 この API との RESTful の対話は、ODataを使用する Microsoft Dataverse Web API を介して行われます。 この API は Dataverse Web API のサブセットです。 Dataverse Web APIでは、認証、SLA、バッチ、同時実行制御、エラー処理などの特性が定義されます。

Microsoft Dataverse Web API の詳細については、次を参照してください :

- [Microsoft Dataverse とは](/powerapps/maker/data-platform/data-platform-intro)
- [Microsoft Dataverse Web API を使用する](/powerapps/developer/data-platform/webapi/overview)
- [Microsoft Dataverse 開発者ガイド](/powerapps/developer/data-platform)

このドキュメントには、次のトピックを含む、Dataverse Web API の使用に関する詳細と開発者ガイダンスが含まれています。

- [Web API で Microsoft Dataverse を認証](/powerapps/developer/data-platform/webapi/authenticate-web-api)
- [Web API を使用した操作の実行](/powerapps/developer/data-platform/webapi/perform-operations-web-api)
- [Web API で Postman を使用](/powerapps/developer/data-platform/webapi/use-postman-web-api)
- [変更追跡を使用した外部システムとのデータの同期](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)

### <a name="virtual-tables-for-human-resources-in-dataverse"></a>Dataverse における Human Resources の仮想テーブル

給与統合 API のエンドポイントは、Microsoft Dataverse の仮想テーブル プラットフォーム機能を使用します。 既定では、仮想テーブルと関連する API エンドポイントは人事環境には配置されていないため、組織は環境で公開される OData エンドポイントを決定することができます。 このAPIを使用するには、その環境に対して Human Resources エンティティの仮想テーブルを生成する必要があります。

API 用の仮想テーブルの生成の詳細については、[Dataverse 仮想テーブルの構成](./hr-admin-integration-common-data-service-virtual-entities.md)を参照してください。

## <a name="data-model"></a>データ モデル

次の図では、API 内の関係性を示しています。 Human Resources 内の既存のエンティティには、その他のエンティティに対する外部キーがあり、それについてはここでは示されていません。 このドキュメントでは、給与統合のシナリオに固有のエンティティに関する情報を提供します。 しかし、Human Resources 向け Dataverse Web API には他にも多くのエンティティが存在しており、これらのエンティティも統合に関連している可能性があります。 これらのエンティティの一部は、外部キーとの関係性やナビゲーション プロパティで参照されます。

[![給与統合の API データ モデル。](media/hr-admin-payroll-api-data-model.png)](media/hr-admin-payroll-api-data-model.png#lightbox)

## <a name="payroll-employee-and-related-entities"></a>給与従業員および関連エンティティ

エンティティ:

- [給与従業員](hr-admin-integration-payroll-api-payroll-employee.md)
- [給与作業者の住所](hr-admin-integration-payroll-api-payroll-worker-address.md)
- [固定報酬の報酬計画](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md)
- [固定報酬の報酬計画](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md)
- [給与職位職務](hr-admin-integration-payroll-api-payroll-position-job.md)
- [給与職位](hr-admin-integration-payroll-api-payroll-position.md)

## <a name="see-also"></a>参照

[給与エンティティの生成および確認](hr-admin-integration-payroll-api-generate-review-entities.md)<br>
[Human Resources パラメーターのコンフィギュレーション](hr-setup-parameters.md)<br>
[Human Resources 共有パラメーターのコンフィギュレーション](hr-setup-shared-parameters.md)<br>
[Microsoft Dataverse とは](/powerapps/maker/data-platform/data-platform-intro)<br>
[Microsoft Dataverse Web API を使用する](/powerapps/developer/data-platform/webapi/overview)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
