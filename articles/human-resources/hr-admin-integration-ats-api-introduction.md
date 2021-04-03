---
title: 申請者追跡システム統合APIの概要
description: このトピックでは、Dynamics 365 Human Resources 申請者追跡システム (ATS) 統合 API について説明します。
author: andreabichsel
manager: tfehr
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 61d8502a8f420d387b5b7f48fca2f8a680f6f3f8
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464035"
---
# <a name="applicant-tracking-system-integration-api-introduction"></a>申請者追跡システム統合APIの概要

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources 申請者追跡システム (ATS) 統合 API について説明します。 API の目的は、ATS 間およびパートナー間の合理化された Dynamics 365 Human Resources 統合を実現することです。

![ATS 統合のフロー](media/hr-admin-integration-ats-api-introduction-flow.png)

統合されたエクスペリエンスは、採用マネージャーが採用要求を作成する際に Human Resources で開始されます。 要求が有効化されると、ATS によって要求の詳細が引き出され、採用プロジェクトが作成されます。 その後、採用パイプラインに従ってポジションの候補者を選択・採用します。 ATSは最後に、選択した候補者のレコードを Human Resources に送信することで、ラウンド トリップの統合を完了します。 その後、その候補者レコードに対して、多くの修正の検証およびワークフローを実行して、従業員レコードを作成できます。

Human Resources では、統合を有効にするあたり、次のコンポーネントが追加されています。

1.  採用の要求を作成する機能。
2.  拡張された候補者プロファイルと関連するワークフロー。
3.  アプリケーションを統合する新機能をオープンにした統合 API。

採用要求と候補者の機能の設定と使用の詳細については、[採用ジョブ候補者](hr-personnel-recruit.md)を参照してください。

## <a name="microsoft-dataverse"></a>Microsoft Dataverse

この API は Microsoft Dataverse (旧 Common Data Service) に構築されています。 この API との RESTful の対話は、ODataを使用する Microsoft Dataverse Web API を介して行われます。 この API は Dataverse Web API のサブセットです。 Dataverse Web APIでは、認証、SLA、バッチ、同時実行制御、エラー処理などの特性が定義されます。

Microsoft Dataverse Web API の詳細については、次を参照してください :

- [Microsoft Dataverse とは](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)
- [Microsoft Dataverse Web API を使用する](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/overview)
- [Microsoft Dataverse 開発者ガイド](https://docs.microsoft.com/powerapps/developer/data-platform)

上記のドキュメントでは、[認証の管理](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/authenticate-web-api)、[操作の実行](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/perform-operations-web-api)、[API での Postman の使用](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/use-postman-web-api)、APIによる[変更追跡トークンまたはデルタ トークンの使用](https://docs.microsoft.com/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)などの、Dataverse Web API の使用に関する詳細なガイドと開発者ガイドが含まれています。

### <a name="option-sets"></a>オプション セット

このドキュメントで説明する ATS 統合 API のデータ モデルには、エンティティ プロパティに関連付けられた列挙値を提供するオプション セットが含まれています。 Dataverse Web API でのオプション セットの操作の詳細については、[Web APIを使用したオプション セットの作成と更新](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets)を参照してください。 オプション セットは各 Dataverse 環境ごとに定義されます。

### <a name="virtual-tables-for-human-resources-in-dataverse"></a>Dataverse における Human Resources の仮想テーブル

ATS 統合 API のエンドポイントは、Microsoft Dataverse の仮想テーブルプラットフォーム機能を使用します。 既定では、仮想テーブルと関連する API エンドポイントは人事環境には配置されていないため、組織は環境で公開される OData エンドポイントを決定することができます。 このAPIを使用するには、その環境に対して Human Resources エンティティの仮想テーブルを生成する必要があります。 

API 用の仮想テーブルの生成の詳細については、[Dataverse 仮想テーブルの構成](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities)を参照してください。

## <a name="data-model"></a>データ モデル

データ モデルは、次の2つの主要なエンティティの中央に位置しています。

- **RecruitingRequest** は、ATS に対して、ひとつまたは複数のオープンなポジションの募集を依頼していることを表しています。クエリの例については、[採用要求のクエリの例](hr-admin-integration-ats-api-recruiting-request-example-query.md)を参照してください。
- **CandidateToHire** は、ポジションのオファーを受けた候補者の詳細を表します。 **人物** は、採用候補者を表します。 候補者、労働者、社員、契約社員など、会社の中で複数の役割を割り当てることができます。 クエリの例については、[採用する候補者のクエリの例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)を参照してください。

次の図では、API 内の関係性を示しています。 Human Resources 内の既存のエンティティには、その他のエンティティに対する外部キーがあり、それについてはここでは示されていません。 このドキュメントでは、統合の採用のシナリオに固有のエンティティに関する情報を提供します。 しかし、Dynamics 365 Human Resources 向け Dataverse Web API には他にも多くのエンティティが存在しており、これらのエンティティも統合に関連している可能性があります。 たとえば、ここで定義していない作業者、ジョブ、職位、または他のエンティティの詳細が必要な場合があります。 これらのエンティティの多くは、外部キーとの関係性やナビゲーション プロパティで参照されます。

![ATS 統合の API データ モデル](media/hr-admin-integration-ats-api-data-model.png)

## <a name="recruiting-request-and-related-entities-and-option-sets"></a>採用要求と関連するエンティティとオプション セット

クエリの例 : 

- [採用要求のクエリの例](hr-admin-integration-ats-api-recruiting-request-example-query.md)

エンティティ:

- [採用要求](hr-admin-integration-ats-api-recruiting-request.md)
- [採用要求職位](hr-admin-integration-ats-api-recruiting-request-position.md)
- [採用で要求するスキル](hr-admin-integration-ats-api-recruiting-request-skill.md)
- [採用で要求する教育](hr-admin-integration-ats-api-recruiting-request-education.md)
- [採用要求場所](hr-admin-integration-ats-api-recruiting-request-location.md)

オプション セット :

- [ジョブ除外する状態](hr-admin-integration-ats-api-job-exempt-status.md)
- [採用で要求するポジションの状態](hr-admin-integration-ats-api-recruiting-request-position-status.md)
- [採用で要求する状態](hr-admin-integration-ats-api-recruiting-request-status.md)
- [規制のジョブ カテゴリ](hr-admin-integration-ats-api-regulatory-job-category.md)

## <a name="candidate-to-hire-and-related-entities-and-option-sets"></a>採用候補者と関連するエンティティおよびオプション セット

クエリの例 :

- [採用する採用候補者に対するクエリの例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

エンティティ:

- [採用候補者](hr-admin-integration-ats-api-candidate-to-hire.md)
- [名前](hr-admin-integration-ats-api-person.md)
- [人物の教育](hr-admin-integration-ats-api-person-education.md)
- [人物の職務経験](hr-admin-integration-ats-api-person-professional-experience.md)
- [人物の住所](hr-admin-integration-ats-api-person-address.md)
- [関係者の連絡先](hr-admin-integration-ats-api-party-contact.md)
- [人物のスキル](hr-admin-integration-ats-api-person-skill.md)
- [評価レベル](hr-admin-integration-ats-api-rating-level.md)
- [人物の証明書](hr-admin-integration-ats-api-person-certificate.md)
- [証明書タイプ](hr-admin-integration-ats-api-certificate-type.md)
- [個人の審査](hr-admin-integration-ats-api-person-screening.md)
- [審査タイプ](hr-admin-integration-ats-api-screening-types.md)
- [人物の ID 番号](hr-admin-integration-ats-api-person-identification-number.md)

オプション セット :

- [申請者の統合結果](hr-admin-integration-ats-api-applicant-integration-result.md)
- [空白の [はい] と [いいえ]](hr-admin-integration-ats-api-blank-yes-no.md)
- [完了の状態](hr-admin-integration-ats-api-completion-status.md)
- [連絡先タイプ](hr-admin-integration-ats-api-contact-type.md)
- [教育クレジット基準](hr-admin-integration-ats-api-education-credit-basis.md)
- [種類](hr-admin-integration-ats-api-gender.md)
- [配偶者の有無](hr-admin-integration-ats-api-marital-status.md)
- [月](hr-admin-integration-ats-api-months-of-year.md)
- [いいえ はい](hr-admin-integration-ats-api-no-yes.md)
- [期間の単位](hr-admin-integration-ats-api-period-unit.md)
- [審査の頻度](hr-admin-integration-ats-api-screening-frequency.md)
- [審査頻度の生成方法](hr-admin-integration-ats-api-screening-frequency-generate-from.md)
- [スキル レベル タイプ](hr-admin-integration-ats-api-skill-level-type.md)

## <a name="see-also"></a>参照

[職務候補者の採用](hr-personnel-recruit.md)<br>
[Microsoft Dataverse とは](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[Microsoft Dataverse Web API を使用する](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/overview)<br>
[Web API を使用したオプション セットの作成と更新](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]