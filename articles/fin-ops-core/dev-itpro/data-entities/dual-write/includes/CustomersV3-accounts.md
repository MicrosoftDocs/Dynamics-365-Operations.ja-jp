## <a name="customers-v3-to-accounts"></a>顧客 V3 を アカウントへ

このテンプレートは、Finance and Operations アプリと Common Data Service 間でデータを同期します。

ソース フィルター: ((PartyType == "組織"))

取消済ソース フィルター: customertypecode eq 3

Finance and Operations フィールド | タイプのマッピング | その他の Dynamics 365 フィールド | 既定値
---|---|---|---
CUSTOMERACCOUNT | = | accountnumber | 
INVOICEADDRESSCITY | = | address2_city | 
INVOICEADDRESSCOUNTRYREGIONISOCODE | = | address2_country | 
INVOICEADDRESSCOUNTY | = | address2_county | 
INVOICEADDRESSLATITUDE | > | address2_latitude | 
INVOICEADDRESSLONGITUDE | > | address2_longitude | 
INVOICEADDRESSSTATE | = | address2_stateorprovince | 
INVOICEADDRESSSTREET | = | address2_line1 | 
INVOICEADDRESSZIPCODE | = | address2_postalcode | 
CREDITLIMIT | = | creditlimit | 
DELIVERYADDRESSCITY | = | address1_city | 
DELIVERYADDRESSCOUNTRYREGIONISOCODE | = | address1_country | 
DELIVERYADDRESSCOUNTY | = | address1_county | 
DELIVERYADDRESSLATITUDE | > | address1_latitude | 
DELIVERYADDRESSLONGITUDE | > | address1_longitude | 
DELIVERYADDRESSZIPCODE | = | address1_postalcode | 
ORGANIZATIONNAME | = | name | 
ORGANIZATIONNUMBEROFEMPLOYEES | = | numberofemployees | 
PRIMARYCONTACTEMAIL | = | emailaddress1 | 
PRIMARYCONTACTFAX | = | FAX | 
PRIMARYCONTACTPHONE | = | telephone1 | 
PRIMARYCONTACTTWITTER | = | primarytwitterid | 
PRIMARYCONTACTURL | = | websiteurl | 
SALESCURRENCYCODE | = | transactioncurrencyid.isocurrencycode | 
SALESMEMO | = | description | 
CREDITLIMITISMANDATORY | >< | msdyn_creditlimitismandatory | 
CREDITRATING | = | msdyn_creditrating | 
CUSTOMERGROUPID | = | msdyn_customergroupid.msdyn_groupid | 
IDENTIFICATIONNUMBER | = | msdyn_identificationnumber | 
INVOICEACCOUNT | = | msdyn_billingaccount.accountnumber | 
INVOICEADDRESS | >< | msdyn_invoiceaddress | 
ISONETIMECUSTOMER | >< | msdyn_onetimecustomer | 
ONHOLDSTATUS | >< | msdyn_onholdstatus | 
PARTYCOUNTRY | = | msdyn_partycountry | 
PARTYSTATE | = | msdyn_partystateprovince | 
PAYMENTDAY | = | msdyn_paymentday.msdyn_name | 
PAYMENTMETHOD | = | msdyn_customerpaymentmethod.msdyn_name | 
PAYMENTSCHEDULE | = | msdyn_paymentschedule.msdyn_name | 
PAYMENTTERMS | = | msdyn_paymentterm.msdyn_name | 
PAYMENTTERMSBASEDAYS | = | msdyn_paymenttermsbasedays | 
PRIMARYCONTACTFACEBOOK | = | msdyn_primaryfacebookid | 
PRIMARYCONTACTFAXEXTENSION | = | msdyn_faxextension | 
PRIMARYCONTACTLINKEDIN | = | msdyn_primarylinkedinid | 
TAXEXEMPTNUMBER | = | msdyn_taxexemptnumber | 
VENDORACCOUNT | = | msdyn_vendor.msdyn_vendoraccountnumber | 
PRIMARYCONTACTEMAILDESCRIPTION | = | msdyn_emailaddress1description | 
PRIMARYCONTACTFACEBOOKDESCRIPTION | = | msdyn_primaryfacebookdescription | 
PRIMARYCONTACTFAXDESCRIPTION | = | msdyn_faxdescription | 
PRIMARYCONTACTLINKEDINDESCRIPTION | = | msdyn_primarylinkedindescrption | 
PRIMARYCONTACTPHONEDESCRIPTION | = | msdyn_telephone1description | 
PRIMARYCONTACTPHONEEXTENSION | = | msdyn_telephone1extension | 
PRIMARYCONTACTTWITTERDESCRIPTION | = | msdyn_primarytwitteriddescription | 
PRIMARYCONTACTURLDESCRIPTION | = | msdyn_websiteurldescription | 
LANGUAGEID | << | なし | en-us
DELIVERYADDRESSSTREET | = | address1_line1 | 
DELIVERYADDRESSSTATE | = | address1_stateorprovince | 
なし | >> | address1_addresstypecode | 2
なし | >> | customertypecode | 3
PARTYTYPE | << | なし | 組織
PARTYNUMBER | = | msdyn_partynumber | 
CONTACTPERSONID | = | primarycontactid.msdyn_contactpersonid | 
