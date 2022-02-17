---
title: Finance との統合のコンフィギュレーション
description: このトピックでは、Dynamics 365 Human Resources と Dynamics 365 Finance 間の統合について説明します。
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0a2c5dd0ce97f33f5f8b65c801fbc15dfc65e8d4
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065019"
---
# <a name="configure-integration-with-finance"></a>Finance との統合のコンフィギュレーション


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Dynamics 365 Human Resources と Dynamics 365 Finance を統合するには、[データ インテグレーター](/powerapps/administrator/data-integrator)の 「Human Resources から Finance へ」 のテンプレートを使用します。 「Human Resources から Finance へ」 のテンプレートでは、職務、職位、および作業者のデータフローを使用できます。 このテンプレートを使用すると、データを Human Resources から Finance に転送できますが、Finance から Human Resources にデータを渡すことはできません。

![Human Resources から Finance への統合フロー。](./media/hr-admin-integration-finance-flow.png)

Human Resources から Finance へのソリューションは、次のタイプのデータ同期を提供します：

- Human Resources のジョブを管理し、Human Resources から Finance に同期する
- Human Resources の職位と職位の割り当てを管理し、Human Resources から Finance に同期する
- Human Resources の雇用を管理し、Human Resources から Finance に同期する
- Human Resources の作業者と作業者の住所を管理し、Human Resources から Finance に同期する

## <a name="system-requirements-for-human-resources"></a>Human Resources のシステム要件

統合ソリューションには、次のバージョンの Human Resources および Finance が必要です。 

- Dataverse の Dynamics 365 Human Resources
- Dynamics 365 Finance バージョン 7.2 およびそれ以降

## <a name="template-and-tasks"></a>テンプレートおよびタスク

Human Resources から Finance へのテンプレートにアクセスする方法。

1. [Power Apps 管理センター](https://admin.powerapps.com/) を開きます。 

2. **プロジェクト** を選択し、 右上隅の **新しいプロジェクト** を選択します。 新しいプロジェクトは、Finance に統合する法人ごとに作成してください。

3. **Human Resources（Human Resources Dataverse から Finance へ）** を選択し、Human Resources から Finance にレコードを同期します。

このテンプレートは、以下の基になるタスクを使用して、Human Resources から Finance にレコードを同期します。

- **職務権限から報酬職務権限**
- **部門から作業単位**
- **ジョブ タイプから報酬ジョブ タイプ**
- **ジョブからジョブ**
- **ジョブからジョブ詳細**
- **職位タイプから職位タイプ**
- **ジョブ職位から基本職位**
- **ジョブ職位から職位の詳細**
- **ジョブ職位から職位の期間**
- **ジョブの職位から職位の階層**
- **作業者から作業者**
- **雇用から雇用**
- **雇用から雇用詳細**
- **職位作業者割り当てから職位作業者割り当て**
- **作業者住所から作業者の住所 V2**

## <a name="template-mappings"></a>テンプレートのマッピング

次のテンプレートのマッピング テーブルでは、各アプリケーションで使用されるエンティティがタスクの名前に含まれています。 ソース（Human Resources）は左側にあり、ターゲット（Finance）は右側にあります。

### <a name="job-functions-to-compensation-job-function"></a>職務権限から報酬職務権限

| Dataverseテーブル (ソース) | Finance エンティティ（宛先） |
|-------------------------------------|---------------------------------------------|
| cdm_name (cdm_Job   関数名)  | JOBFUNCTIONID   (JOBFUNCTIONID)            |
| cdm_description   (cdm_description) | DESCRIPTION   (DESCRIPTION)                 |

### <a name="departments-to-operating-unit"></a>部門から作業単位

| Dataverseテーブル (ソース)           | Finance エンティティ（宛先） |
|-----------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                           | NAME (NAME)                                 |
| cdm_departmentnumber   (cdm_departmentnumber) | OPERATINGUNITNUMBER   (OPERATINGUNITNUMBER) |
|                                               | OPERATINGUNITTYPE   (OPERATINGUNITTYPE)     |
| cdm_description   (cdm_description)           | NAMEALIAS   (NAMEALIAS)                     |

### <a name="job-types-to-compensation-job-type"></a>ジョブ タイプから報酬ジョブ タイプ

| Dataverseテーブル (ソース)   | Finance エンティティ（宛先） |
|---------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                   | JOBTYPEID   (JOBTYPEID)                     |
| cdm_description   (cdm_description)   | DESCRIPTION   (DESCRIPTION)                 |
| cdm_exemptstatus   (cdm_exemptstatus) | EXEMPTSTATUS   (EXEMPTSTATUS)               |

### <a name="jobs-to-jobs"></a>ジョブからジョブ

| Dataverseテーブル (ソース)                           | Finance エンティティ（宛先）           |
|---------------------------------------------------------------|-------------------------------------------------------|
| cdm_name (cdm_name)                                           | JOBID (JOBID)                                         |
| cdm_maximumnumberofpositions   (cdm_maximumnumberofpositions) | MAXIMUMNUMBEROFPOSITIONS   (MAXIMUMNUMBEROFPOSITIONS) |
| cdm_allowedunlimitedpositions   (cdm_allowunlimitedpositions) | ALLOWUNLIMITEDPOSITIONS   (ALLOWUNLIMITEDPOSITIONS)   |
| cdm_description   (cdm_description)                           | DESCRIPTION   (DESCRIPTION)                           |
| cdm_jobdescription   (cdm_jobdescription)                     | JOBDESCRIPTION   (JOBDESCRIPTIONS)                    |

### <a name="jobs-to-job-detail"></a>ジョブからジョブ詳細

| Dataverseテーブル (ソース)                             | Finance エンティティ（宛先） |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                                             | JOBID (JOBID)                               |
| cdm_jobtypeid.cdm_name   (ジョブ タイプ (ジョブ タイプ名))             | JOBTYPEID   (JOBTYPEID)                     |
| cdm_jobfunctionid.cdm_name   (職務権限 (職務権限名)) | FUNCTIONID   (FUCNTIONID)                   |
| cdm_validfrom   (発効日)                                    | VALIDFROM   (VALIDFROM)                     |
| cdm_validto (失効日)                                        | VALIDTO (VALIDTO)                           |
| cdm_defaultfulltimeequivalent   (既定のフルタイム相当額)   | FULLTIMEEQUIVALENT   (FULLTIMEEQUIVALENT)   |

### <a name="position-types-to-position-type"></a>職位タイプから職位タイプ

| Dataverseテーブル (ソース)       | Finance エンティティ（宛先） |
|-------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                       | POSITIONTYPEID   (POSITIONTYPEID)           |
| cdm_description   (cdm_description)       | DESCRIPTION   (DESCRIPTION)                 |
| cdm_classification   (cdm_classification) | CLASSIFICATION   (CLASSIFICATION)           |

### <a name="job-positions-to-base-position"></a>ジョブ職位から基本職位

| Dataverseテーブル (ソース)           | Finance エンティティ（宛先） |
|-----------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (職位番号) | POSITIONID (POSITIONID)                      |

### <a name="job-positions-to-position-details"></a>ジョブ職位から職位の詳細

| Dataverseテーブル (ソース)              | Finance エンティティ（宛先）       |
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

| Dataverseテーブル (ソース)             | Finance エンティティ（宛先） |
|-------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (職位番号)   | POSITIONID (POSITIONID)                      |
| 計算された有効化 (計算された有効化) | VALIDFROM (VALIDFROM)                        |
| 計算された退職 (計算された退職)  | VALIDTO (VALIDTO)                         |

### <a name="job-positions-to-position-hierarchies"></a>ジョブの職位から職位の階層

| Dataverseテーブル (ソース)        | Finance エンティティ（宛先） |
|-----------------------------------------------------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (職位番号)                                                 | POSITIONID(POSITIONID)                      |
| cdm_parentjobpositionid.cdmjobpositionnumber   (cdm_parentjobpositionid.cdmjobpositionnumber) | PARENTPOSITIONID (PARENTPOSITIONID)         |
| cdm_validfrom   (発効日)                                                                  | VALIDFROM   (VALIDFROM)                     |
| cdm_validto (失効日)                                                                      | VALIDTO (VALIDTO)                           |
| HIERARCHYTYPENAME   (HIERARCHYTYPENAME)                                                       | HIERARCHYTYPENAME   (HIERARCHYTYPENAME)     |


### <a name="workers-to-worker"></a>作業者から作業者
| Dataverseテーブル (ソース)           | Finance エンティティ（宛先）       |
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

| Dataverseテーブル (ソース)                             | Finance エンティティ（宛先） |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_employmentstartdate   (cdm_employmentstartdate)             | EMPLOYMENTSTARTDATE   (EMPLOYMENTSTARTDATE) |
| cdm_employmentenddate   (cdm_employmentenddate)                 | EMPLOYMENTENDDATE   (EMPLOYMENTENDDATE)     |
| cdm_workertype   (cdm_workertype)                               | WORKERTYPE   (WORKERTYPE)                   |
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)         |
| cdm_companyid.cdm_companycode   (cdm_companyid.cdm_companycode) | LEGALENTITYID   (LEGALENTITYID)             |

### <a name="employments-to-employment-detail"></a>雇用から雇用詳細

| Dataverseテーブル (ソース)                             | Finance エンティティ（宛先）   |
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

| Dataverseテーブル (ソース)                             | Finance エンティティ（宛先）   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_jobpositionnumber   (職位番号)                   | POSITIONID(POSITIONID)                        |
| cdm_validfrom   (発効日)                                    | VALIDFROM   (VALIDFROM)                       |
| cdm_validto (失効日)                                        | VALIDTO (VALIDTO)                             |

### <a name="worker-addresses-to-worker-postal-address-v2"></a>作業者住所から作業者の住所 V2

| Dataverseテーブル (ソース)                             | Finance エンティティ（宛先）   |
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

Human Resources から Finance にデータを統合する場合は、ID に基づいたレコードの一致を試行します。 一致がある場合、データ インテグレーターが Finance のデータを、Human Resources の値で上書きします。 ただし、論理的にさまざまなレコードが存在し、Human Resources または Finance のいずれかでそれぞれの番号順序に基づいて同一の ID が生成された場合に、問題が発生する場合があります。

これが発生する領域は、 **従業員番号** を使用した一致が実行される **作業者** と、**職位** です。 職務には、番号シーケンスは使用されません。 その結果、同一の職務ジョブ ID が Human Resources と Finance の両方に存在する場合は、Human Resources の情報で Dynamics 365 Finance の情報が上書きされます。 

重複する ID の問題を防ぐには、[番号順序](/dynamics365/unified-operations/fin-and-ops/organization-administration/number-sequence-overview?toc=%2fdynamics365%2funified-operations%2ftalent%2ftoc.json)に接頭語を追加するか、その他のシステムの範囲を超えている番号順序の開始番号を設定します。 

番号順序に含まれていない作業者住所に使用される場所 ID。 Human Resources から Finance に作業者住所を統合するとき、Finance に作業者の住所が既に存在する場合は、重複する住所レコードが作成される場合があります。 

次の図は、データ インテグレーターのテンプレート マッピングの例を示しています。 

![テンプレート マッピング。](./media/IntegrationMapping.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
