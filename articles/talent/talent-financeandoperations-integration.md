---
title: Dynamics 365 for Talent から Dynamics 365 for Finance and Operations への統合
description: このトピックでは、Talent と Finance and Operations の統合について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: IT Pro
ms.reviewer: anbichse
ms.search.scope: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-8
ms.dyn365.ops.version: ''
ms.openlocfilehash: fc4d6f88e54ebcdb9b82889c9315391eeee31d4d
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537614"
---
# <a name="integration-from-dynamics-365-for-talent-to-dynamics-365-for-finance-and-operations"></a>Dynamics 365 for Talent から Dynamics 365 for Finance and Operations への統合

[!include[banner](../includes/banner.md)]

このトピックでは、Dynamics 365 for Talent および Dynamics 365 for Finance and Operations から統合できる機能について説明します。 [データ インテグレーター](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator)と共に使用可能な Talent から Finance and Operations へのテンプレートにより、ジョブ、職位、および作業者のデータのフローが可能になります。 Talent から Finance and Operations へのデータ フロー。 テンプレートでは、Finance and Operations から Talent にデータを戻す機能は提供されません。 

![Talent のから Finance and Operations への統合フロー](./media/TalentFinOpsFlow.png)

Talent から Finance and Operations へのソリューションは、次のタイプのデータ同期を提供します。 

- Talent のジョブを管理し、Talent から Finance and Operations に同期します。
- Talent の職位と職位の割り当てを管理し、Talent から Finance and Operations に同期します。
- Talent の雇用を管理し、Talent から Finance and Operations に同期します。
- Talent の作業者と作業者住所を管理し、Talent から Finance and Operations に同期します。

## <a name="system-requirements-for-talent"></a>Talent のシステム要件
統合ソリューションには、次のバージョンの Talent および Finance and Operations アプリケーションが必要です。 
- Common Data Service 上の Dynamics 365 for Talent。
- Dynamics 365 for Finance and Operations バージョン 7.2 以降。

## <a name="template-and-tasks"></a>テンプレートおよびタスク

テンプレートにアクセスするには、次の操作を行います。
1. [PowerApps 管理センター](https://admin.powerapps.com/)を開きます。 
1. **プロジェクト**を選択した後、右上隅にある **新しいプロジェクト** を選択してパブリック テンプレートを選択します。 新しいプロジェクトは、Finance and Operations に統合する法人ごとに作成する必要があります。

Talent から Finance and Operations にレコードを同期するには、次のテンプレートを使用します。

- **データ統合でのテンプレートの名前:** Core HR (Talent Common Data Service から Finance and Operations)

  > [!NOTE]
  > タスクの名前には、各アプリケーションで使用されるエンティティが含まれています。 ソース (Talent) は左にあり、ターゲット (Finance and Operations) は右にあります。

Talent から Finance and Operations にレコードを同期するには、次の基になるタスクを使用します。
- 職務権限から報酬職務権限
- 部門から作業単位
- ジョブ タイプから報酬ジョブ タイプ
- ジョブからジョブ
- ジョブからジョブ詳細
- 職位タイプから職位タイプ
- ジョブ職位から基本職位
- ジョブ職位から職位の詳細
- ジョブ職位から職位の期間
- ジョブ職位から職位の階層
- 作業者から作業者
- 雇用から雇用
- 雇用から雇用詳細
- 職位作業者割り当てから職位作業者割り当て
- 作業者住所から作業者の住所 V2

## <a name="template-mappings"></a>テンプレートのマッピング

### <a name="job-functions-to-compensation-job-function"></a>職務権限から報酬職務権限

| Common Data Service エンティティ (ソース)                 | Finance and Operations エンティティ (宛先) |
|-------------------------------------|---------------------------------------------|
| cdm_name (cdm_Job   関数名)  | JOBFUNCTIONID   (JOBFUNCTIONID)            |
| cdm_description   (cdm_description) | DESCRIPTION   (DESCRIPTION)                 |

### <a name="departments-to-operating-unit"></a>部門から作業単位

| Common Data Service エンティティ (ソース)                           | Finance and Operations エンティティ (宛先) |
|-----------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                           | NAME (NAME)                                 |
| cdm_departmentnumber   (cdm_departmentnumber) | OPERATINGUNITNUMBER   (OPERATINGUNITNUMBER) |
|                                               | OPERATINGUNITTYPE   (OPERATINGUNITTYPE)     |
| cdm_description   (cdm_description)           | NAMEALIAS   (NAMEALIAS)                     |

### <a name="job-types-to-compensation-job-type"></a>ジョブ タイプから報酬ジョブ タイプ

| Common Data Service エンティティ (ソース)                   | Finance and Operations エンティティ (宛先) |
|---------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                   | JOBTYPEID   (JOBTYPEID)                     |
| cdm_description   (cdm_description)   | DESCRIPTION   (DESCRIPTION)                 |
| cdm_exemptstatus   (cdm_exemptstatus) | EXEMPTSTATUS   (EXEMPTSTATUS)               |

### <a name="jobs-to-jobs"></a>ジョブからジョブ

| Common Data Service エンティティ (ソース)                                           | Finance and Operations エンティティ (宛先)           |
|---------------------------------------------------------------|-------------------------------------------------------|
| cdm_name (cdm_name)                                           | JOBID (JOBID)                                         |
| cdm_maximumnumberofpositions   (cdm_maximumnumberofpositions) | MAXIMUMNUMBEROFPOSITIONS   (MAXIMUMNUMBEROFPOSITIONS) |
| cdm_allowedunlimitedpositions   (cdm_allowunlimitedpositions) | ALLOWUNLIMITEDPOSITIONS   (ALLOWUNLIMITEDPOSITIONS)   |
| cdm_description   (cdm_description)                           | DESCRIPTION   (DESCRIPTION)                           |
| cdm_jobdescription   (cdm_jobdescription)                     | JOBDESCRIPTION   (JOBDESCRIPTIONS)                    |

### <a name="jobs-to-job-detail"></a>ジョブからジョブ詳細

| Common Data Service エンティティ (ソース)                                             | Finance and Operations エンティティ (宛先) |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                                             | JOBID (JOBID)                               |
| cdm_jobtypeid.cdm_name   (ジョブ タイプ (ジョブ タイプ名))             | JOBTYPEID   (JOBTYPEID)                     |
| cdm_jobfunctionid.cdm_name   (職務権限 (職務権限名)) | FUNCTIONID   (FUCNTIONID)                   |
| cdm_validfrom   (発効日)                                    | VALIDFROM   (VALIDFROM)                     |
| cdm_validto (失効日)                                        | VALIDTO (VALIDTO)                           |
| cdm_defaultfulltimeequivalent   (既定のフルタイム相当額)   | FULLTIMEEQUIVALENT   (FULLTIMEEQUIVALENT)   |

### <a name="position-types-to-position-type"></a>職位タイプから職位タイプ

| Common Data Service エンティティ (ソース)                       | Finance and Operations エンティティ (宛先) |
|-------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                       | POSITIONTYPEID   (POSITIONTYPEID)           |
| cdm_description   (cdm_description)       | DESCRIPTION   (DESCRIPTION)                 |
| cdm_classification   (cdm_classification) | CLASSIFICATION   (CLASSIFICATION)           |

### <a name="job-positions-to-base-position"></a>ジョブ職位から基本職位

| Common Data Service エンティティ (ソース)                           | Finance and Operations エンティティ (宛先) |
|-----------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (職位番号) | POSITIONID (POSITIONID)                      |

### <a name="job-positions-to-position-details"></a>ジョブ職位から職位の詳細

| Common Data Service エンティティ (ソース)                                                      | Finance and Operations エンティティ (宛先)       |
|--------------------------------------------------------------------------|---------------------------------------------------|
| cdm_jobpositionnumber  (職位番号)                            | POSITIONID (POSITIONID)                             |
| cdm_jobid.cdm_name   (職務 (名前))                                        | JOBID (JOBID)                                    |
| cdm_description   (cdm_description)                                        | DESCRIPTION   (DESCRIPTION)                       |
| cdm_departmentid.cdm_departmentnumber   (部門 (部門番号)) | DEPARTMENTNUMBER   (DEPARTMENTNUMBER)             |
| cdm_positiontypeid.cdm_name   (職位タイプ (名前))                     | POSITIONTYPEID   (POSITIONTYPEID)                 |
| cdm_avaialableforassignment   (割り当てに使用可能)                 | AVAILABLEFORASSIGNMENT   (AVAILABLEFORASSIGNMENT) |
| cdm_validfrom   (発効日)                                            | VALIDFROM   (VALIDFROM)                           |
| cdm_validto (失効日)                                                 | VALIDTO (VALIDTO)                               |
| cdm_fulltimeequivalent   (フルタイム相当)                           | FULLTIMEEQUIVALENT   (FULLTIMEEQUIVALENT)         |

### <a name="job-positions-to-position-durations"></a>ジョブ職位から職位の期間

| Common Data Service エンティティ (ソース)                             | Finance and Operations エンティティ (宛先) |
|-------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (職位番号)   | POSITIONID (POSITIONID)                      |
| 計算された有効化 (計算された有効化) | VALIDFROM (VALIDFROM)                        |
| 計算された退職 (計算された退職)  | VALIDTO (VALIDTO)                         |

### <a name="job-positions-to-position-hiearchies"></a>ジョブ職位から職位の階層

| Common Data Service エンティティ (ソース)                                                                           | Finance and Operations エンティティ (宛先) |
|-----------------------------------------------------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (職位番号)                                                 | POSITIONID(POSITIONID)                      |
| cdm_parentjobpositionid.cdmjobpositionnumber   (cdm_parentjobpositionid.cdmjobpositionnumber) | PARENTPOSITIONID (PARENTPOSITIONID)         |
| cdm_validfrom   (発効日)                                                                  | VALIDFROM   (VALIDFROM)                     |
| cdm_validto (失効日)                                                                      | VALIDTO (VALIDTO)                           |
| HIERARCHYTYPENAME   (HIERARCHYTYPENAME)                                                       | HIERARCHYTYPENAME   (HIERARCHYTYPENAME)     |


### <a name="workers-to-worker"></a>作業者から作業者
| Common Data Service エンティティ (ソース)                           | Finance and Operations エンティティ (宛先)       |
|-----------------------------------------------|---------------------------------------------------|
| cdm_birthdate   (cdm_birthdate)               | BIRTHDATE   (BIRTHDATE)                           |
| cdm_gender   (cdm_gender)                     | GENDER (GENDER)                                   |
| cdm_primaryaddress   (cdm_primaryaddress)     | PRIMARYCONTACTEMAIL   (PRIMARYCONTACTEMAIL )      |
| cdm_primarytelephone   (cdm_primarytelephone) | PRIMARYCONTACTPHONE   (PRIMARYCONTACTPHONE)       |
| cdm_facebookidentity   (cdm_facebookidentity) | PRIMARYCONTACTFACEBOOK   (PRIMARYCONTACTFACEBOOK) |
| cdm_twitteridentity   (cdm_twitteridentity)   | PRIMARYCONTACTTWITTER   (PRIMARYCONTACTTWITTER)   |
| cdm_linkedinIdentity   (cdm_linkedinIdentity) | PRIMARYCONTACTLINKEDIN   (PRIMARYCONTACTLINKEDIN) |
| cdm_websiteurl   (cdm_websiteurl)             | PRIMARYCONTACTURL   (PRIMARYCONTACTURL)           |
| cdm_firstname   (cdm_firstname)               | FIRSTNAME   (FIRSTNAME)                           |
| cdm_middlename   (cdm_middlename)             | MIDDLENAME   (MIDDLENAME)                         |
| cdm_lastname   (cdm_lastname)                 | LASTNAME (LASTNAME)                               |
| cdm_workernumber   (cdm_workernumber)         | PERSONNELNUMBER   (PERSONNELNUMBER)               |
| cdm_type (cdm_type)                           | WORKERTYPE   (WORKERTYPE)                         |
| cdm_state   (cdm_state)                       | WORKSTATUS   (WORKERSTATUS)                       |

### <a name="employments-to-employment"></a>雇用から雇用

| Common Data Service エンティティ (ソース)                                             | Finance and Operations エンティティ (宛先) |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_employmentstartdate   (cdm_employmentstartdate)             | EMPLOYMENTSTARTDATE   (EMPLOYMENTSTARTDATE) |
| cdm_employmentenddate   (cdm_employmentenddate)                 | EMPLOYMENTENDDATE   (EMPLOYMENTENDDATE)     |
| cdm_workertype   (cdm_workertype)                               | WORKERTYPE   (WORKERTYPE)                   |
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)         |
| cdm_companyid.cdm_companycode   (cdm_companyid.cdm_companycode) | LEGALENTITYID   (LEGALENTITYID)             |

### <a name="employments-to-employment-detail"></a>雇用から雇用詳細

| Common Data Service エンティティ (ソース)                                             | Finance and Operations エンティティ (宛先)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_employmentstartdate   (cdm_employmentstartdate)             | EMPLOYMENTSTARTDATE   (EMPLOYMENTSTARTDATE)   |
| cdm_employmentenddate   (cdm_employmentenddate)                 | EMPLOYMENTENDDATE   (EMPLOYMENTENDDATE)       |
| cdm_validfrom   (発効日)                                    | VALIDFROM   (VALIDFROM)                       |
| cdm_validto (失効日)                                        | VALIDTO (VALIDTO)                             |
| cdm_workerstartdate   (cdm_workerstartdate)                     | WORKERSTARTDATE   (WORKERSTARTDATE)           |
| cdm_lastdateworked   (cdm_lastdateworked)                       | LASTDATEWORKED   (LASTDATEWORKED)             |
| cdm_transitiondate   (cdm_transitiondate)                       | TRANSITIONDATE   (TRANSITIONDATE)             |
| cdm_employerunitofnotice   (cdm_employerunitofnotice)           | EMPLOYERUNITOFNOTICE   (EMPLOYERUNITOFNOTICE) |
| cdm_workerunitofnotice   (cdm_workerunitofnotice)               | WORKERUNITOFNOTICE   (WORKERUNITOFNOTICE)     |
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_companyid.cdm_companycode   (cdm_companyid.cdm_companycode) | LEGALENTITYID   (LEGALENTITYID)               |
| cdm_employernoticeamount   (cdm_employernoticeamount)           | EMPLOYERNOTICEAMOUNT   (EMPLOYERNOTICEAMOUNT) |
| cdm_workernoticeamount   (cdm_workernoticeamount )              | WORKERNOTICEAMOUNT   (WORKERNOTICEAMOUNT)     |

### <a name="position-worker-assignment-to-position-worker-assignments"></a>職位作業者割り当てから職位作業者割り当て

| Common Data Service エンティティ (ソース)                                             | Finance and Operations エンティティ (宛先)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_jobpositionnumber   (職位番号)                   | POSITIONID(POSITIONID)                        |
| cdm_validfrom   (発効日)                                    | VALIDFROM   (VALIDFROM)                       |
| cdm_validto (失効日)                                        | VALIDTO (VALIDTO)                             |

### <a name="worker-addresses-to-worker-postal-address-v2"></a>作業者住所から作業者の住所 V2

| Common Data Service エンティティ (ソース)                                             | Finance and Operations エンティティ (宛先)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_addresstype   (cdm_addresstype)                             | ADDRESSLOCATIONROLES   (ADDRESSLOCATIONROLES) |
| cdm_line1   (cdm_line1)                                         | ADDRESSSTREET   (ADDRESSSTREET)               |
| cdm_city (cdm_city)                                             | ADDRESSCITY   (ADDRESSCITY)                   |
| cdm_stateorprovince   (cdm_stateorprovince)                     | ADDRESSSTATE   (ADDRESSSTATE)                 |
| cdm_postalcode   (cdm_postalcode)                               | ADDRESSZIPCODE(ADDRESSZIPCODE)                |
| cdm_countryregion   (cdm_countryregion)                         | ADDRESSCOUNTRYREGION(ADDRESSCOUNTRYREGION)    |
| cdm_addressnumber   (cdm_addressnumber)                         | ADDRESSLOCATIONID(ADDRESSLOCATIONID)          |
| cdm_ispreferred   (cdm_ispreferred)                             | ISPRIMARY   (ISPRIMARY)                       |
| cdm_county   (cdm_county)                                       | ADDRESSCOUNTYID(ADDRESSCOUNTYID)              |
| cdm_addresstype   (cdm_addresstype)                             | ADDRESSDESCRIPTION(ADDRESSDESCRIPTION)        |

## <a name="integration-considerations"></a>統合に関する考慮事項
Talent から Finance and Operations にデータを統合する場合は、統合が ID に基づいてレコードを一致させようとします。 一致が発生した場合、Finance and Operations のデータは、Talent の値で上書きされます。 ただし、論理的にさまざまなレコードが存在し、Talent または Finance and Operations のいずれかでそれぞれの番号順序に基づいて同一の ID が生成された場合に、問題が発生する場合があります。

これが発生する領域は、従業員番号を使用して一致が作成される作業者と、職位です。 職務には、番号順序は使用されません。 その結果、同一の職務ジョブ ID が Talent と Finance and Operations の両方で存在する場合は、Talent 情報により Finance and Operations 情報が上書きされます。 

重複する ID の問題を防ぐには、[番号順序](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/number-sequence-overview?toc=/dynamics365/unified-operations/talent/toc.json)に接頭語を追加するか、その他のシステムの範囲を超えている番号順序の開始番号を設定します。 

番号順序に含まれていない作業者住所に使用される場所 ID。 Talent から Finance and Operations に作業者住所を統合するとき、Finance and Operations に作業者の住所が既に存在する場合は、重複する住所レコードが作成される場合があります。 

次の図は、データ インテグレーターのテンプレート マッピングの例を示しています。 

![テンプレートのマッピング](./media/IntegrationMapping.png)




