---
title: 採用候補者
description: このトピックでは、Dynamics 365 Human Resources の採用候補者エンティティについて説明します。
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: aef9f4889d17811026fc36091bb98494412dacd898f847ac661333628e8e32e7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742827"
---
# <a name="candidate-to-hire"></a>採用候補者

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources の採用候補者エンティティについて説明します。

物理名 : mshr_hcmcandidatetohireentity

## <a name="description"></a>説明

このエンティティは、 Dynamics 365 Human Resources で従業員の作成に使用される候補者の詳細を提供します。 すべての候補者レコードを読み取り、内部および外部の候補者の記録の作成に使用され、新しい候補者の個人情報を作成できます。

システム内で新規人物レコードとなる外部の候補者レコードを作成する際には、新規候補者レコードを投稿する当事者 (人物) 番号を定義する必要があります。 新しい人物のエンティティ レコードは、新しい候補者レコードを使用して作成されます。

社内の候補者レコード (すでに社内で従業員レコードを持っている職位の候補者) を作成する場合は、新しい人物のレコードを作成する際に使用する個人情報 (名前、性別、生年月日など) を定義するのではなく、候補者レコードの mshr_partynumber プロパティに、すでに存在する人物レコードの当事者 (個人) 番号を定義してください。

## <a name="json-representation"></a>JSON 表記

```json
        {
            "mshr_candidateid": "String",
            "mshr_partynumber": "String",
            "mshr_partytype": "String",
            "mshr_recruitingrequestid": "String",
            "mshr_positionid": "String",
            "mshr_firstname": "String",
            "mshr_middlename": "String",
            "mshr_lastnameprefix": "String",
            "mshr_lastname": "String",
            "mshr_gender": Int,
            "mshr_birthdate": "Date",
            "mshr_citizenshipcountrycode": "String",
            "mshr_veteranstatusid": "String",
            "mshr_isdisabledveteran": Int,
            "mshr_availabilitydate": "Date",
            "mshr_iswillingtorelocate": Int,
            "mshr_comments": "String",
            "mshr_applicantintegrationresult": Int,
            "mshr_donothirereasoncodeid": "String",
            "mshr_dataareaid": "String",
            "_mshr_dataareaid_id_value": "Guid",
            "_mshr_fk_person_id_value": "Guid",
            "_mshr_fk_recruitingrequest_id_value": "Guid",
            "_mshr_fk_position_id_value": "Guid",
            "mshr_hcmcandidatetohireentityid": "Guid",
            "_mshr_fk_veteranstatus_id_value": "Guid",
            "_mshr_fk_reasoncode_id_value": "Guid",
            "mshr_militaryserviceenddate": "Guid",
            "mshr_militaryservicestartdate": "Guid"
        }
```

## <a name="properties"></a>プロパティ

| プロパティ<br>**現物名**<br>**_種類_** | 使用 | 説明 |
| --- | --- | --- |
| **採用候補者のエンティティ ID**<br>mshr_hcmcandidatetohireentityid<br>GUID | 読み取り専用<br>必須<br>システム生成 | システムが生成した、エンティティ レコードの一意識別子です。 |
| **候補者 ID**<br>mshr_candidateid<br>文字列 | 読み取り専用<br>必須<br>システム生成 | エンティティの一意の識別子。 |
| **当事者番号**<br>mshr_partynumber<br>文字列 | 読み取り専用<br>必須 | 候補者の人物レコードの当事者 (個人) 番号。 |
| **個人 ID の値**<br>_mshr_fk_person_id_value<br>GUID | 読み取り専用<br>必須<br>外部キー : mshr_direpersonentity の mshr_dirpersonentityid | システムが生成する、候補者の当事者 (個人) レコードの一意識別子。 |
| **当事者 タイプ**<br>mshr_partytype<br>mshr_dirpartytype オプション セット | 読み取り専用<br>必須 | mshr_dirpartytype オプションセットに定義されている、当事者タイプのレコード。 このエンティティのタイプは常に "人" です。 |
| **採用要求 ID**<br>mshr_recruitingrequestid<br>文字列 | 1回書き込み<br>オプション | この候補者が履行する採用要求を参照します。 |
| **採用要求 ID 値**<br>_mshr_fk_recruitingrequest_id_value<br>GUID | 読み取り/書き込み<br>オプション<br>外部キー : mshr_hcmrecruitingrequestentity の mshr_hcmrecruitingrequestentityid | システムが生成する、候補者が履行する採用要求の一意識別子。 |
| **職位 ID**<br>mshr_positionid<br>文字列 | 読み取り/書き込み<br>オプション | 候補者が検討しているポジションの ID。 |
| **ポジション ID の値**<br>_mshr_fk_position_if_value<br>GUID | 読み取り専用<br>オプション<br>外部キー : mshr_hcmpositionv2entity の mshr_hcmpositionv2entityid | システムが生成する、 候補者が検討しているポジションの識別子。 |
| **名**<br>mshr_firstname<br>文字列 | 読み取り/書き込み<br>必須 | 候補者の名前。 |
| **ミドル ネーム**<br>mshr_middlename<br>文字列 | 読み取り/書き込み<br>オプション | 候補者のミドルネーム。 |
| **姓の接頭辞**<br>mshr_lastnameprefix<br>文字列 | 読み取り/書き込み<br>オプション | 候補者の姓の接頭辞です。 |
| **姓**<br>mshr_lastname<br>文字列 | 読み取り/書き込み<br>オプション | 候補者の名前。 |
| **種類**<br>mshr_gender<br>mshr_hcmpersongender オプション セット | 読み取り/書き込み<br>オプション | 候補者の性別。 |
| **生年月日**<br>mshr_birthdate<br>日時 | 読み取り/書き込み<br>オプション | 候補者の生年月日。 |
| **市民権のある国番号**<br>mshr_citizenshipcountrycode<br>文字列 | 読み取り/書き込み<br>オプション | 候補者が市民権を有する国を指定します。 有効な国番号は、mshr_logisticaddresscountryregionentity にあります。 |
| **ベテランの状態 ID**<br>mshr_veteranstatusid<br>文字列 | 読み取り/書き込み<br>オプション | 候補者の退役者状態を示します。 |
| **退役者の状態 ID 値**<br>_mshr_fk_veteranstatus_id_value<br>GUID | 読み取り専用<br>オプション<br>外部キー : mshr_hcmveteranstatusentity の mshr_hcmveteranstatusentityid | システムが生成した、退役者の状態エンティティ レコードの一意識別子。 |
| **兵役の開始日**<br>mshr_militaryservicestartdate<br>日時 | 読み取り/書き込み<br>オプション | 候補者の兵役開始日。 |
| **兵役の終了日**<br>mshr_militaryserviceenddate<br>日時 | 読み取り/書き込み<br>オプション | 候補者の兵役終了日。 |
| **退役傷病軍人かどうか**<br>mshr_isdisabledveteran<br>mshr_noyes オプション セット | 読み取り/書き込み<br>オプション | 候補者が退役者の資格を持っているかどうかを示します。 |
| **使用可能日**<br>mshr_availabilitydate<br>日時 | 読み取り/書き込み<br>オプション | 候補者が勤務可能な最も早い日付。 |
| **配置転換の意思あり**<br>mshr_iswillingtorelocate<br>mshr_noyes オプション セット | 読み取り/書き込み<br>オプション | 候補者がそのポジションのために転勤する意思があるかどうかを示します。 |
| **備考**<br>mshr_comments<br>文字列 | 読み取り/書き込み<br>オプション | 採用担当者、または採用マネージャが使用するコメント。 |
| **アプリケーションの統合結果**<br>mshr_applcantintegrationresult<br>mshr_applicantintegrationresult オプションセット | 読み取り/書き込み<br>必須 | 統合に関連する採用プロセスにおける候補者の状態。 |
| **不採用理由コード ID**<br>mshr_donothirereasoncodeid<br>文字列 | 読み取り/書き込み<br>オプション | 状態 (アプリケーション統合結果) が [採用されていない] に設定されている場合に、任意で指定される理由コードです。 |
| **理由コード ID の値**<br>_mshr_fk_reasoncode_id_value<br>GUID | 読み取り専用<br>オプション<br>外部キー : mshr_hcmreasoncodeentity entity の mshr_hcmreasoncodeentityid | **採用しない** 理由コードに対してシステムが生成する一意識別子。 |
| **データ領域 ID**<br>mshr_dataareaid<br>文字列 | 読み取り/書き込み<br>オプション |  法人 (会社) を指定します。 |
| **データ領域 ID 値**<br>_mshr_dataareaid_id_value<br>GUID | 読み取り専用<br>オプション<br>外部キー : cdm_companyid of cdm_company エンティティ | システムが生成する、法人 (会社) を識別する GUID 値です。 |

## <a name="see-also"></a>参照

[申請者追跡システム統合APIの概要](hr-admin-integration-ats-api-introduction.md)<br>
[採用する採用候補者に対するクエリの例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]