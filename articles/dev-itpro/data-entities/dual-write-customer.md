---
title: 統合済み顧客マスター
description: このトピックでは、Finance and Operations と Common Data Service 間の顧客データの統合について説明します。
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
ms.openlocfilehash: a8030d9d1f1f3636a679d334afddad0f573a824e
ms.sourcegitcommit: 02c223b44ac7196df675afac61c6783f467d1983
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/24/2019
ms.locfileid: "1789211"
---
## <a name="integrated-customer-master"></a>統合済み顧客マスター

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

顧客レコードは、複数のアプリケーションで習得するのが一般的です。 たとえば、営業活動は Microsoft Dynamics 365 for Sales アプリケーションを通じて商用顧客レコードを取り込むことができ、電子商取引や小売販売は、Dynamics 365 for Finance and Operations アプリケーションを通じて顧客レコードを取り込むことができます。 顧客レコードの発生元にかかわらず、アプリケーションの境界およびインフラストラクチャの違いを越えてバックグラウンドで統合されます。 統合された顧客マスタリングは、マルチ マスタリング シナリオの処理に役立ち、Dynamics 365 アプリケーション スイートに顧客の包括的な情報を提供します。

## <a name="customer-data-flow"></a>顧客データ フロー

*顧客*は、Finance and Operations と Common Data Service の両方で明確に定義された概念です。 したがって、顧客データの統合は、Finance and Operations と Common Data Service アプリケーションの間で顧客の概念を調和させるだけです。 次の図は、顧客データ フローを示します。

![顧客データ フロー](media/dual-write-customer-data-flow.png)

顧客は、商用 / 組織の顧客および消費者 / エンド ユーザーの 2 種類に大きく分類できます。 これら 2 種類の顧客は、Finance and Operations と Common Data Serviceにて、異なる方法で格納および処理されます。

Finance and Operations では、商用 / 組織の顧客および消費者 / エンド ユーザーの両方が、**CustTable** (CustomerCustomerV3Entity) という名前の単一のテーブルで習得され、**タイプ**属性に基づいて分類されます。 (**タイプ**が**組織**に設定されている場合、顧客は商用 / 組織の顧客であり、**タイプ**が**人材**に設定されている場合、顧客はコンシューマ / エンド ユーザーです。) 主な連絡担当者情報は、SMMContactPersonEntity エンティティを介して処理されます。

Common Data Serviceでは、商取引 / 組織の顧客は口座エンティティで習得され、**リレーションシップ タイプ**属性が**顧客**に設定されている場合、顧客として識別されます。 コンシューマ / エンド ユーザーと連絡担当者の両方が、連絡先エンティティによって表されます。 コンシューマー / エンド ユーザーおよび連絡担当者の間を明確に分離するために、**連絡先**エンティティには**販売可能**という名前のブール フラグがあります。 **販売可能**が **True** の場合、連絡先はコンシューマー / エンド ユーザーであり、その連絡先に対して見積と注文を作成できます。 **販売可能が**が **False** の場合、連絡先は顧客の主要な連絡担当者にすぎません。

販売不能な取引先担当者が見積または注文プロセスに参加する場合、**販売可能**が **True** に設定され、取引先担当者に販売可能な取引先担当者としてフラグが設定されます。 販売可能な取引先担当者になった連絡先は、引き続き販売可能な連絡先です。

## <a name="templates"></a>テンプレート

顧客データには、顧客グループ、住所、連絡先情報、支払プロファイル、請求書プロファイル、およびロイヤルティ ステータスなど、顧客に関するすべての情報が含まれます。 次の表に示すように、エンティティ マップのコレクションは、顧客データ操作中に連携して動作します。

Finance and Operations    | Customer Engagement アプリケーション
--------------------------|---------------------------------
顧客 V3               | 口座
顧客 V3               | 連絡
CDS 連絡先 V2           | 連絡
顧客グループ           | Msdyn\_customergroups
顧客支払方法   | Msdyn\_customerpaymentmethods
ロイヤルティ カード              | Msdyn\_loyaltycards
支払スケジュール          | Msdyn\_paymentschedules
支払スケジュール          | Msdyn\_paymentschedulelines
支払期日 CDS           | Msdyn\_paymentdays
支払期日明細行 CDS     | Msdyn\_paymentdaylines
支払条件          | Msdyn\_paymentterms
名前の接辞              | Msdyn\_nameaffixes

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="customer-v3-to-account"></a>口座に顧客 V3

このテンプレートは、Finance and Operations と Common Data Service 間で、商業および組織顧客の顧客マスター情報を同期します。

<!-- ![](media/dual-write-account-1.png) -->

<!-- ![](media/dual-write-account-2.png) -->

ソース フィールド | タイプのマッピング | 出力先フィールド
---|---|---
CUSTOMERACCOUNT | = | accountnumber
INVOICEADDRESSCITY | = | address2\_city
INVOICEADDRESSCOUNTRYREGIONISOCODE | = | address2\_country
INVOICEADDRESSCOUNTY | = | address2\_county
INVOICEADDRESSLATITUDE | \> | address2\_latitude
INVOICEADDRESSLONGITUDE | \> | address2\_longitude
INVOICEADDRESSSTATE | = | address2\_stateorprovince
INVOICEADDRESSSTREET | = | address2\_line1
INVOICEADDRESSZIPCODE | = | address2\_postalcode
CREDITLIMIT | = | creditlimit
DELIVERYADDRESSCITY | = | address1\_city
DELIVERYADDRESSCOUNTRYREGIONISOCODE | = | address1\_country
DELIVERYADDRESSCOUNTY | = | address1\_county
DELIVERYADDRESSLATITUDE | \> | address1\_latitude
DELIVERYADDRESSLONGITUDE | \> | address1\_longitude
DELIVERYADDRESSZIPCODE | = | address1\_postalcode
ORGANIZATIONNAME | = | name
ORGANIZATIONNUMBEROFEMPLOYEES | = | numberofemployees
PRIMARYCONTACTEMAIL | = | emailaddress1
PRIMARYCONTACTFAX | = | fax
PRIMARYCONTACTPHONE | = | telephone1
PRIMARYCONTACTTWITTER | = | primarytwitterid
PRIMARYCONTACTURL | = | websiteurl
SALESCURRENCYCODE | = | transactioncurrencyid.isocurrencycode
SALESMEMO | = | 説明
CREDITLIMITISMANDATORY | \>\< | msdyn\_creditlimitismandatory
CREDITRATING | = | msdyn\_creditrating
CUSTOMERGROUPID | = | msdyn\_customergroupid.msdyn\_groupid
IDENTIFICATIONNUMBER | = | msdyn\_identificationnumber
INVOICEACCOUNT | = | msdyn\_billingaccount.accountnumber
INVOICEADDRESS | \>\< | msdyn\_invoiceaddress
ISONETIMECUSTOMER | \>\< | msdyn\_onetimecustomer
ONHOLDSTATUS | \>\< | msdyn\_onholdstatus
PARTYCOUNTRY | = | msdyn\_partycountry
PARTYSTATE | = | msdyn\_partystateprovince
PAYMENTDAY | = | msdyn\_paymentday.msdyn\_name
PAYMENTMETHOD | = | msdyn\_customerpaymentmethod.msdyn\_name
PAYMENTSCHEDULE | = | msdyn\_paymentschedule.msdyn\_name
PAYMENTTERMS | = | msdyn\_paymentterm.msdyn\_name
PAYMENTTERMSBASEDAYS | = | msdyn\_paymenttermsbasedays
PRIMARYCONTACTFACEBOOK | = | msdyn\_primaryfacebookid
PRIMARYCONTACTFAXEXTENSION | = | msdyn\_faxextension
PRIMARYCONTACTLINKEDIN | = | msdyn\_primarylinkedinid
TAXEXEMPTNUMBER | = | msdyn\_taxexemptnumber
VENDORACCOUNT | = | msdyn\_vendor.msdyn\_vendoraccountnumber
PRIMARYCONTACTEMAILDESCRIPTION | = | msdyn\_emailaddress1description
PRIMARYCONTACTFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYCONTACTFAXDESCRIPTION | = | msdyn\_faxdescription
PRIMARYCONTACTLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescrption
PRIMARYCONTACTPHONEDESCRIPTION | = | msdyn\_telephone1description
PRIMARYCONTACTPHONEEXTENSION | = | msdyn\_telephone1extension
PRIMARYCONTACTTWITTERDESCRIPTION | = | msdyn\_primarytwitteriddescription
PRIMARYCONTACTURLDESCRIPTION | = | msdyn\_websiteurldescription
LANGUAGEID | \<\< | なし
DELIVERYADDRESSSTREET | = | address1\_line1
DELIVERYADDRESSSTATE | = | address1\_stateorprovince
なし | \>\> | address1\_addresstypecode
なし | \>\> | customertypecode
PARTYTYPE | \<\< | なし
PARTYNUMBER | = | msdyn\_partynumber

## <a name="customer-v3-to-contact"></a>顧客 V3 から連絡先へ

このテンプレートは、Finance and Operations と Customer Engagement 間で、消費者およびエンド ユーザーの顧客マスターデータを同期します。

<!-- ![](media/dual-write-contact-1.png) -->
<!-- ![](media/dual-write-contact-2.png) -->

ソース フィールド | タイプのマッピング | 出力先フィールド
---|---|---
なし | \>\> | msdyn\_sellable
PARTYTYPE | \<\< | なし
PARTYNUMBER | = | msdyn\_partynumber
CUSTOMERACCOUNT | = | msdyn\_contactpersonid
CUSTOMERGROUPID | = | msdyn\_customergroupid.msdyn\_groupid
PERSONFIRSTNAME | = | 名
PERSONLASTNAME | = | 姓
PERSONMIDDLENAME | = | ミドル ネーム
PERSONPROFESSIONALTITLE | = | 職位
PERSONGENDER | \>\< | 性別コード
PERSONMARITALSTATUS | \>\< | familystatuscode
LANGUAGEID | \<\< | なし
ADDRESSCITY | = | address1\_city
ADDRESSCOUNTRYREGIONISOCODE | = | address1\_country
ADDRESSCOUNTY | = | address1\_county
ADDRESSLATITUDE | \> | address1\_latitude
ADDRESSLONGITUDE | \> | address1\_longitude
ADDRESSLOCATIONROLES | \<\< | なし
ADDRESSSTATE | = | address1\_stateorprovince
ADDRESSSTREET | = | address1\_line1
ADDRESSZIPCODE | = | address1\_postalcode
ADDRESSPOSTBOX | = | address1\_postofficebox
なし | \>\> | address1\_addresstypecode
INVOICEADDRESSCITY | = | address2\_city
INVOICEADDRESSCOUNTRYREGIONISOCODE | = | address2\_country
INVOICEADDRESSCOUNTY | = | address2\_county
INVOICEADDRESSLATITUDE | \> | address2\_latitude
INVOICEADDRESSLONGITUDE | \> | address2\_longitude
INVOICEADDRESSSTATE | = | address2\_stateorprovince
INVOICEADDRESSSTREET | = | address2\_line1
INVOICEADDRESSZIPCODE | = | address2\_postalcode
なし | \>\> | address2\_addresstypecode
DELIVERYADDRESSCITY | = | address3\_city
DELIVERYADDRESSCOUNTRYREGIONISOCODE | = | address3\_country
DELIVERYADDRESSCOUNTY | = | address3\_county
DELIVERYADDRESSLATITUDE | \> | address3\_latitude
DELIVERYADDRESSLONGITUDE | \>\> | address3\_longitude
DELIVERYADDRESSSTATE | = | address3\_stateorprovince
DELIVERYADDRESSSTREET | = | address3\_line1
DELIVERYADDRESSZIPCODE | = | address3\_postalcode
なし | \>\> | address3\_addresstypecode
PRIMARYCONTACTEMAIL | = | emailaddress1
PRIMARYCONTACTEMAILDESCRIPTION | = | msdyn\_emailaddress1description
PRIMARYCONTACTFAX | = | fax
PRIMARYCONTACTFAXDESCRIPTION | = | msdyn\_faxdescription
PRIMARYCONTACTFAXEXTENSION | = | msdyn\_faxextension
IDENTIFICATIONNUMBER | = | msdyn\_identificationnumber
PARTYCOUNTRY | = | msdyn\_partycountry
PARTYSTATE | = | msdyn\_partystateprovince
PRIMARYCONTACTFACEBOOK | = | msdyn\_primaryfacebookid
PRIMARYCONTACTFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYCONTACTLINKEDIN | = | msdyn\_primaryinkedinid
PRIMARYCONTACTLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescrption
PRIMARYCONTACTPHONE | = | 電話 1
PRIMARYCONTACTPHONEDESCRIPTION | = | msdyn\_telephone1description
PRIMARYCONTACTPHONEEXTENSION | = | msdyn\_telephone1extension
PRIMARYCONTACTTWITTER | = | msdyn\_primarytwitterid
PRIMARYCONTACTTWITTERDESCRIPTION | = | msdyn\_primarytwitteriddescription
PRIMARYCONTACTURL | = | Web サイト URL
PRIMARYCONTACTURLDESCRIPTION | = | msdyn\_websiteurldescription
SALESCURRENCYCODE | = | transactioncurrencyid.isocurrencycode
SALESMEMO | = | 説明

## <a name="contacts"></a>連絡先

このテンプレートは、Finance and Operations と Customer Engagement 間で、顧客および仕入先のすべての基本、二次、三次の連絡先情報を同期します。

<!-- ![](media/dual-write-contacts.png) -->

ソース フィールド | タイプのマッピング | 出力先フィールド
---|---|---
CONTACTPERSONPARTYNUMBER | = | msdyn\_partynumber
ASSOCIATEDCONTACTTYPE | \<\< | なし
FIRSTNAME | = | 名
MIDDLENAME | = | ミドル ネーム
LASTNAME | = | 姓
ASSOCIATEDCONTACTNUMBER | = | msdyn\_vendorcontactid.msdyn\_vendoraccountnumber
PRIMARYADDRESSCITY | = | address1\_city
PRIMARYADDRESSCOUNTRYREGIONID | = | address1\_country
PRIMARYADDRESSCOUNTYID | = | address1\_county
PRIMARYFAXNUMBER | = | fax
PRIMARYADDRESSSTATEID | = | address1\_stateorprovince
PRIMARYADDRESSSTREET | = | address1\_line1
PRIMARYADDRESSZIPCODE | = | address1\_postalcode
PRIMARYPHONENUMBER | = | 電話 1
PRIMARYEMAILADDRESS | = | 電子メール アドレス 1
EMPLOYMENTDEPARTMENT | = | 部門
メモ | = | 説明
GENDER | \>\< | 性別コード
GOVERNMENTIDENTIFICATIONNUMBER | = | governmentid
PRIMARYURL | = | Web サイト URL
MARITALSTATUS | \>\< | familystatuscode
ISRECEIVINGDIRECTMAIL | \>\< | donotemail
EMPLOYMENTPROFESSION | = | 職位
SPOUSENAME | = | spousesname
なし | \>\> | msdyn\_contactforvendor
なし | \>\> | msdyn\_contactpersonid

## <a name="customer-groups"></a>顧客グループ

このテンプレートは、Finance and Operations と Customer Engagement 間で、顧客グループ情報を同期します。

<!-- ![](media/dual-write-customer-groups.png) -->

ソース フィールド | タイプのマッピング | 出力先フィールド
---|---|---
CUSTOMERGROUPID | = | msdyn\_groupid
説明 | = | msdyn\_description
ISSALESTAXINCLUDEDINPRICE | \>\< | msdyn\_issalestaxincludedinprice
PAYMENTTERMID | = | msdyn\_paymenttermid.msdyn\_name
CLEARINGPERIODPAYMENTTERMNAME | = | msdyn\_clearingperiodpaymenttermname.msdyn\_name

## <a name="customer-payment-methods"></a>顧客支払方法

このテンプレートは、Finance and Operations と Customer Engagement 間で、顧客支払方法を同期します。

<!-- ![](media/dual-write-customer-payment-methods.png) -->

ソース フィールド | タイプのマッピング | 出力先フィールド
---|---|---
名前 | = | msdyn\_name
ACCOUNTTYPE | \>\< | msdyn\_accounttype
DISCOUNTGRACEPERIODDAYS | = | msdyn\_discountgraceperioddays
BRIDGINGPOSTINGENABLED | \>\< | msdyn\_bridgingpostingenabled
ISSEPA | \>\< | msdyn\_issepa
LASTFILENUMBER | = | msdyn\_lastfilenumber
LASTFILENUMBERTODAY | = | msdyn\_lastfilenumbertoday
説明 | = | msdyn\_description
PAYMENTTYPE | \>\< | msdyn\_paymenttype
CREATEANDDRAWBILLOFEXCHANGEDURINGINVOICEPOSTING | \>\< | msdyn\_invoiceupdate
PAYMENTSTATUS | \>\< | msdyn\_paymentstatus
SUMBYPERIOD | \>\< | msdyn\_sumbyperiod
ENABLEPOSTDATEDCHECKCLEARINGPOSTING | \>\< | msdyn\_enablepostdatescheckclearingposting
BILLOFEXCHANGEDRAFTTYPE | \>\< | msdyn\_billofexchangedrafttype
DIRECTDEBIT | \>\< | msdyn\_directdebit

## <a name="loyalty-cards"></a>ロイヤルティ カード (複数)

このテンプレートは、Finance and Operations と Customer Engagement 間で、顧客のロイヤリティ カード情報を同期します。

<!-- ![](media/dual-write-loyalty-cards.png) -->

ソース フィールド | タイプのマッピング | 出力先フィールド
---|---|---
CARDNUMBER | = | msdyn\_cardnumber
CARDTENDERTYPE | \>\< | msdyn\_cardtendertype
PARTYNUMBER | = | msdyn\_partynumber
REPLACEMENTCARDNUMBER | \> | msdyn\_replacementcardnumber
OMOPERATINGUNITNUMBER | = | msdyn\_operatingunitnumber
LOYALTYENROLLMENTDATE | = | msdyn\_enrollmentdate

## <a name="payment-schedules"></a>支払スケジュール

このテンプレートは、Finance and Operations と Customer Engagement 間で、顧客および仕入先の支払スケジュールに関する参照データを同期します。

<!-- ![](media/dual-write-payment-schedules.png) -->

ソース フィールド | タイプのマッピング | 出力先フィールド
---|---|---
名前 | = | msdyn\_name
説明 | = | msdyn\_description
ALLOCATIONMETHOD | \>\< | msdyn\_allocationmethod
PAYMENTFREQUENCYUNITS | \>\< | msdyn\_paymentfrequencyunit
PAYMENTFREQUENCY | = | msdyn\_paymentfrequency
NUMBEROFPAYMENTS | = | msdyn\_numberofpayments
FIXEDPAYMENTAMOUNT | = | msdyn\_fixedpaymentamount
MINIMUMPAYMENTAMOUNT | = | msdyn\_minimumpaymentamount
SALESTAXALLOCATIONMETHOD | \>\< | msdyn\_salestaxallocationmethod
摘要 | = | msdyn\_note

## <a name="payment-schedule-lines"></a>支払スケジュール明細行

Finance and Operations と Customer Engagement 間で、顧客および仕入先の支払スケジュール明細行に関する参照データを同期します。

<!-- ![](media/dual-write-payment-schedule-lines.png) -->

ソース フィールド | タイプのマッピング | 出力先フィールド
---|---|---
PAYMENTSCHEDULENAME | = | msdyn\_paymentschedule.msdyn\_name
PAYMENTSCHEDULENAME | \> | msdyn\_name
LINENUMBER | = | msdyn\_linenumber
PERIODSAFTERDUEDATE | = | msdyn\_periodsafterduedate
PERCENTORAMOUNT | \>\< | msdyn\_percentoramount
PERCENTORAMOUNTVALUE | = | msdyn\_percentoramountvalue

## <a name="payment-days"></a>支払期日

このテンプレートは、Finance and Operations と Customer Engagement 間で、顧客および仕入先の支払期日に関する参照データを同期します。

<!-- ![](media/dual-write-payment-days.png) -->

ソース フィールド | タイプのマッピング | 出力先フィールド
---|---|---
名前 | = | msdyn\_name
説明 | = | msdyn\_description

## <a name="payment-day-lines"></a>支払期日明細行

このテンプレートは、Finance and Operations と Customer Engagement 間で、顧客および仕入先の支払期日明細行に関する参照データを同期します。

<!-- ![](media/dual-write-payment-day-lines.png) -->

ソース フィールド | タイプのマッピング | 出力先フィールド
---|---|---
CDSINTEGRATIONKEY | = | msdyn\_paymentdaylineid
頻度 | \>\< | msdyn\_frequency
DAYOFWEEK | \>\< | msdyn\_dayofweek
DAYOFMONTH | = | msdyn\_dayofmonth
名前 | = | msdyn\_paymentday.msdyn\_name

## <a name="payment-terms"></a>支払条件

このテンプレートは、Finance and Operations と Customer Engagement 間で、顧客および仕入先の支払条件 (支払に関する条件) に関する参照データを同期します。

<!-- ![](media/dual-write-payment-terms.png) -->

ソース フィールド | タイプのマッピング | 出力先フィールド
---|---|---
説明 | = | msdyn\_description
名前 | = | msdyn\_name
NUMBEROFMONTHS | = | msdyn\_numberofmonth
CUTOFFDAYOFMONTH | = | msdyn\_cutoffdayofmonth
ISCASHPAYMENT | \>\< | msdyn\_iscashpayment
NUMBEROFDAYS | = | msdyn\_days
ISCERTIFIEDCOMPANYCHECK | \>\< | msdyn\_iscertifiedcompanycheck
ISDEFAULTPAYMENTTERM | \>\< | msdyn\_isdefaultpaymentterm
CREDITCARDPAYMENTTYPE | \>\< | msdyn\_creditcardpaymenttype
CREDITCARDCREDITCHECKTYPE | \>\< | msdyn\_creditcardcreditchecktype
PAYMENTDAYNAME | = | msdyn\_paymentdayname.msdyn\_name
PAYMENTMETHODTYPE | \>\< | msdyn\_paymentmethodtype
PAYMENTSCHEDULENAME | = | msdyn\_paymentschedulename.msdyn\_name

## <a name="name-affixes"></a>名前の接辞

このテンプレートは、Finance and Operations と Customer Engagement 間で、顧客および仕入先の名前の接辞に関する参照データを同期します。

<!-- ![](media/dual-write-name-affixes.png) -->

ソース フィールド | タイプのマッピング | 出力先フィールド
---|---|---
接辞 | = | msdyn\_affix
タイプ | \>\< | msdyn\_affixtype
説明 | = | msdyn\_description
