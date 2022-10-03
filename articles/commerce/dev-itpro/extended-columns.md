---
title: チャネル データベースの事前拡張された列
description: この記事では、チャネル データベース内の事前拡張された列がどのように拡張に使用されるかについて説明します。
author: josaw1
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-02-02
ms.dyn365.ops.version: 10.0.10
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 49fc02f3abbe512aad5224ad61f04cda19127745
ms.sourcegitcommit: 24673493d14f2045a08fe7240689bee34e099cb5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2022
ms.locfileid: "9589105"
---
# <a name="pre-extended-columns-in-the-channel-database"></a>チャネル データベースの事前拡張された列

[!include [banner](../../includes/banner.md)]

チャネル データベース内の一部の列は、*事前拡張* されています。 つまり、チャネル データベースの列の長さが Microsoft Dynamics 365 Commerce 本体が規定する列の長さを超えています。 たとえば、**INVENTSERIALID** フィールドの長さは、Commerce 本体のデータベースでは 20 文字、チャネル データベースでは 50 文字です。

チャネル データベースのフィールドは拡張されることは多いですが、フィールドの列の長さは拡張に対応していません。 したがって、拡張が必要となった場合にも対応できるよう、標準で列の長さが増設されています。

> [!NOTE]
> 事前拡張されていないフィールドを拡張する必要がある場合は、Lifecycle Services (LCS) で拡張リクエストを提出する必要があります。 詳細については、[拡張性要求](../../fin-ops-core/dev-itpro/extensibility/extensibility-requests.md) を参照してください。

このフィールドは、チャネル データベースで拡張されますが、拡張データ型 (EDT) の拡張モデルを使用して、Commerce 本体のデータベースのフィールドも拡張する必要があります。 さらに、これに対応する販売時点管理 (POS) 、または Commerce Runtime (CRT) ユーザー インターフェイス (UI) を拡張する必要があります。

Commerce 本体のデータベースが拡張されていない場合は、チャネル データベースと Commerce 本体のデータベース間の同期が、P-ジョブの実行中に失敗するか、または余分な文字が切り捨てられます。 同様に、対応する販売時点管理 (POS) ユーザー インターフェイス (UI) または Commerce Runtime (CRT) が拡張されていない場合は、検証をすることで既定の文字長を超える文字の入力を防ぐことができます。 既定の長さは、Commerce 本体のデータベースにおける "基準" 列の長さによって決まります。

次にいくつか例を挙げます。

- チャネル データベースの **INVENTSERIALID** フィールドの長さは 50 文字ですが、POS UI では最大で 20 文字までのシリアル番号が入力できます。 この場合は、POS UI と Commerce 本体のデータベースの両方のフィールドを拡張する必要があります。
- チャネルデータベースの **番地** フィールドの長さは、400文字まで拡張されますが、CRT の検証では Commerce 本体のデータベースの既定の長さを超えることは認められません。 この場合は、CRT 要求ハンドラー (**ValidateAddressLengthServiceRequest**) と Commerce 本体のデータベースの両方を拡張して、**番地** フィールドで 400 文字を使用できるようにする必要があります。

一部のフィールドは、POS 内の読み取り専用フィールドである可能性があるため、POS UI または CRT ハンドラーの拡張は不要です。 たとえば、**ECORES** 製品に関連するフィールドは読み取り専用です。 POS では製品の作成に対応していないため、POS では製品の書き込みシナリオが存在しません。

## <a name="sample-code-to-override-the-validateaddresslengthservicerequest-handler"></a>ValidateAddressLengthServiceRequest ハンドラーをオーバーライドするサンプルコード

次の例では、**ValidateAddressLengthServiceRequest** を上書きする方法を示しています。

```C#
namespace Contoso
{
    namespace Commerce.Runtime.ReceiptsSample
    {
        using System;
        using System.Collections.Generic;
        using Microsoft.Dynamics.Commerce.Runtime;
        using Microsoft.Dynamics.Commerce.Runtime.Messages;
        using Microsoft.Dynamics.Commerce.Runtime.Services.Messages;

        public class ValidateAddressLengthServiceRequestExt : IRequestHandler
        {
            private static int maxDefaultFullAddressColumnLength = 250;
            private static int maxDefaultStreetColumnLength = 250;
            private static int maxDefaultCountyColumnLength = 10;

            /// <summary>
            /// Gets the collection of supported request types by this handler.
            /// </summary>
            public IEnumerable<Type> SupportedRequestTypes
            {
                get
                {
                    return new[]
                    {
                        typeof(ValidateAddressLengthServiceRequest),
                    };
                }
            }

            public Response Execute(Request request)
            {
                if (request == null)
                {
                    return null;
                }

                ValidateAddressLengthServiceRequest validateAddressLengthServiceRequest = (ValidateAddressLengthServiceRequest)request;

                var validationFailures = new List<DataValidationFailure>();

                // Add custom logic to check your desired length.

                if (!string.IsNullOrEmpty(validateAddressLengthServiceRequest?.Address?.FullAddress) 
                && validateAddressLengthServiceRequest.Address.FullAddress.Length > maxDefaultFullAddressColumnLength)
                {
                    validationFailures.Add(new DataValidationFailure(
                        DataValidationErrors.Microsoft_Dynamics_Commerce_Runtime_AddressLengthExceeded,
                        string.Format("The full address exceeds the maximum number of {0} characters allowed.",
                        maxDefaultFullAddressColumnLength))
                    {
                        LocalizedMessageParameters = new object[] { maxDefaultFullAddressColumnLength }
                    });
                }

                // Add custom logic to check your desired length.

                if (!string.IsNullOrEmpty(validateAddressLengthServiceRequest?.Address?.Street) 
                && validateAddressLengthServiceRequest.Address.Street.Length > maxDefaultStreetColumnLength)
                {
                    validationFailures.Add(new DataValidationFailure(
                        DataValidationErrors.Microsoft_Dynamics_Commerce_Runtime_StreetLengthExceeded,
                        string.Format("The street exceeds the maximum number of {0} characters allowed.", maxDefaultStreetColumnLength))
                    {
                        LocalizedMessageParameters = new object[] { maxDefaultStreetColumnLength }
                    });
                }

                // Add custom logic to check your desired length.

                if (!string.IsNullOrEmpty(validateAddressLengthServiceRequest?.Address?.County) 
                && validateAddressLengthServiceRequest.Address.County.Length > maxDefaultCountyColumnLength)
                {
                    validationFailures.Add(new DataValidationFailure(
                        DataValidationErrors.Microsoft_Dynamics_Commerce_Runtime_CountyLengthExceeded,
                        string.Format("The county exceeds the maximum number of {0} characters allowed.", maxDefaultCountyColumnLength))
                    {
                        LocalizedMessageParameters = new object[] { maxDefaultCountyColumnLength }
                    });
                }

                if (validationFailures.Count > 0)
                {
                    throw new DataValidationException(DataValidationErrors.Microsoft_Dynamics_Commerce_Runtime_AggregateValidationError,
                    validationFailures, "An error occurred when validating the address.");
                }

                return new NullResponse();
            }
        }
    }
}
```

## <a name="pre-extended-columns-in-the-channel-database"></a>チャネル データベースの事前拡張された列

次の表に、事前拡張されている列の一覧を示します。

| テーブル                         | 円柱                                                                        | 期間        | CRT の拡張機能      | POS の拡張機能                    |
|-------------------------------|-------------------------------------------------------------------------------|---------------|-----------------------|-------------------------------------|
| INVENTSERIAL                  | INVENTSERIALID                                                                | Nvarchar (50)  |                       | GetSerialNumberClientRequestHandler |
| LOGISTICSPOSTALADDRESS        | 住所                                                                       | Nvarchar (500) | ValidateAddressLength |                                     |
| LOGISTICSPOSTALADDRESS        | STREET                                                                        | Nvarchar (400) | ValidateAddressLength |                                     |
| LOGISTICSPOSTALADDRESS        | COUNTY                                                                        | Nvarchar (60)  | ValidateAddressLength |                                     |
| LOGISTICSPOSTALADDRESS        | STATE                                                                         | Nvarchar (60)  | ValidateAddressLength |                                     |
| LOGISTICSPOSTALADDRESS        | ZIPCODE                                                                       | Nvarchar (60)  | ValidateAddressLength |                                     |
| LOGISTICSADDRESSCITY          | COUNTYID                                                                      | Nvarchar (60)  |                       |                                     |
| LOGISTICSADDRESSCITY          | STATEID                                                                      | Nvarchar (60)  |                       |                                     |
| LOGISTICSADDRESSCITY          | 名前                                                                         | Nvarchar (120)  |                       |                                     |
| LOGISTICSADDRESSCOUNTY        | COUNTYID                                                                     | Nvarchar (60)  |                       |                                     |
| LOGISTICSADDRESSCOUNTY        | 名前                                                                         | Nvarchar (120)  |                       |                                     |
| LOGISTICSADDRESSDISTRICT      | COUNTYID\_RU                                                                  | Nvarchar (60)  |                       |                                     |
| LOGISTICSADDRESSDISTRICT      | STATEID\_RU                                                                  | Nvarchar (60)  |                       |                                     |
| LOGISTICSADDRESSDISTRICT      | 名前                                                                          | Nvarchar (120)  |                       |                                     |
| LOGISTICSADDRESSZIPCODE       | STREETNAME                                                                    | Nvarchar (400) |                       |                                     |
| LOGISTICSADDRESSZIPCODE       | COUNTY                                                                        | Nvarchar (60)  |                       |                                     |
| LOGISTICSADDRESSZIPCODE       | STATE                                                                        | Nvarchar (60)  |                       |                                     |
| LOGISTICSADDRESSZIPCODE       | ZIPCODE                                                                        | Nvarchar (60)  |                       |                                     |
| LOGISTICSADDRESSSTATE        | STATEID                                                                        | Nvarchar (60)  |                       |                                     |
| LOGISTICSADDRESSSTATE        | 名前                                                                        | Nvarchar (120)  |                       |                                     |
| LOGISTICSELECTRONICADDRESS   | COUNTRYREGIONCODE                                                              | Nvarchar (10)  |   ValidateElectronicAdtronicServiceRequest                    |                                     |
| RETAILASYNCADDRESS            | STREET                                                                        | Nvarchar (400) |                       |                                     |
| RETAILASYNCADDRESS            | COUNTY                                                                        | Nvarchar (60)  |                       |                                     |
| RETAILASYNCADDRESS            | CUSTNAME                                                                        | Nvarchar (300)  |                       |                                     |
| RETAILASYNCADDRESS            | STATE                                                                        | Nvarchar (60)  |                       |                                     |
| RETAILASYNCADDRESS            | ZIP                                                                        | Nvarchar (60)  |                       |                                     |
| RETAILASYNCCUSTOMER           | STREET                                                                        | Nvarchar (400) |                       |                                     |
| RETAILASYNCCUSTOMER           | COUNTY                                                                        | Nvarchar (60)  |                       |                                     |
| RETAILASYNCCUSTOMER           | CUSTNAME                                                                        | Nvarchar (300)  |                       |                                     |
| RETAILASYNCCUSTOMER           | FIRSTNAME                                                                        | Nvarchar (100)  |                       |                                     |
| RETAILASYNCCUSTOMER           | LASTNAME                                                                        | Nvarchar (100)  |                       |                                     |
| RETAILASYNCCUSTOMER           | MIDDLENAME                                                                        | Nvarchar (100)  |                       |                                     |
| RETAILASYNCCUSTOMER           | CUSTGROUP                                                                        | Nvarchar (25)  |                       |                                     |
| CUSTTABLE           | CUSTGROUP                                                                        | Nvarchar (25) |                       |                                     |
| CUSTTABLE           | INVENTLOCATION                                                                        | Nvarchar (25) |                       |                                     |
| CUSTOMERTABLETYPE_V2           | FIRSTNAME                                                                        | Nvarchar (100)  | ValidateCustomerNameLengthServiceRequest                     |                                     |
| CUSTOMERTABLETYPE_V2          | MIDDLENAME                                                                        | Nvarchar (100)  | ValidateCustomerNameLengthServiceRequest                       |                                     |
| CUSTOMERTABLETYPE_V2           | LASTNAME                                                                        | Nvarchar (100)  |  ValidateCustomerNameLengthServiceRequest                      |                                     |
| RETAILFISCALDOCUMENT\_BR      | FEADDRESSSTREET                                                               | Nvarchar (400) |                       |                                     |
| RETAILFISCALDOCUMENT\_BR      | THIRDPARTYADDRESSSTREET                                                       | Nvarchar (400) |                       |                                     |
| RETAILTAXFILTERS              | COUNTYID                                                                      | Nvarchar (60)  |                       |                                     |
| RETAILTRANSACTIONADDRESSTRANS | STREET                                                                        | Nvarchar (400) |                       |                                     |
| RETAILTRANSACTIONADDRESSTRANS | STATE                                                                        | Nvarchar (60)  |                       |                                     |
| RETAILTRANSACTIONADDRESSTRANS | ZIPCODE                                                                        | Nvarchar (60) |                       |                                     |
| RETAILTRANSACTIONADDRESSTRANS | COUNTY                                                                        | Nvarchar (60)  |                       |                                     |
| RETAILTRANSACTIONSALESTRANS   | INVENTBATCHID                                                                 | Nvarchar (50)  |                       |                                     |
| RETAILTRANSACTIONSALESTRANS   | INVENTSERIALID                                                                | Nvarchar (50)  |                       |                                     |
| RETAILTRANSACTIONSALESTRANS   | WAREHOUSELOCATION                                                             | Nvarchar (60)  |                       |                                     |
| RETAILTRANSACTIONSALESTRANS   | ITEMID                                                                 | Nvarchar (100)  |                       |                                     |
| RETAILTRANSACTIONSALESTRANS   | INVENTLOCATIONID                                                                | Nvarchar (25)  |                       |                                     |
| RETAILTRANSACTIONSALESTRANS   | 単位                                                             | Nvarchar (20)  |                       |                                     |
| RETAILTRANSACTIONSALESTRANS   | ORIGINALTAXITEMGROUP                                                             | Nvarchar (100)  |                       |                                     |
| RETAILTRANSACTIONSALESTRANS   | TAXITEMGROUP                                                             | Nvarchar (100)  |                       |                                     |
| RETAILDLVMODEADDRESSEXPLODED   | STATE                                                                        | Nvarchar (60)  |                       |                                     |
| INVENTDIM                     | INVENTBATCHID                                                                 | Nvarchar (50)  |                       |                                     |
| INVENTDIM                     | INVENTSERIALID                                                                | Nvarchar (50)  |                       |                                     |
| INVENTDIM                     | CONFIGID                                                                      | Nvarchar (60)  |                       |                                     |
| INVENTDIM                     | INVENTCOLORID                                                                 | Nvarchar (60)  |                       |                                     |
| INVENTDIM                     | INVENTSIZEID                                                                  | Nvarchar (60)  |                       |                                     |
| INVENTDIM                     | INVENTSTYLEID                                                                 | Nvarchar (60)  |                       |                                     |
| INVENTDIM                     | WMSLOCATIONID                                                                 | Nvarchar (60)  |                       |                                     |
| INVENTDIM                     | INVENTLOCATIONID                                                                 | Nvarchar (25)  |                       |                                     |
| ECORESCOLOR                   | 名前                                                                          | Nvarchar (60)  |                       |                                     |
| ECORESSTYLE                   | 名前                                                                          | Nvarchar (60)  |                       |                                     |
| ECORESCONFIGURATION           | 氏名                                                                          | Nvarchar (60)  |                       |                                     |
| ECORESSIZE                    | 氏名                                                                          | Nvarchar (60)  |                       |                                     |
| RETAILTABLEFIELDID            | TABLENAME                                                                     | Nvarchar (81)  |                       |                                     |
| RETAILTABLEFIELDID            | FIELDNAME                                                                     | Nvarchar (81)  |                       |                                     |
| RETAILTRANSACTIONTAXTRANSGTE  | TAXCOMPONENT                                                                  | Nvarchar (60)  |                       |                                     |
| TAXCOMPONENTTABLE\_IN         | COMPONENT                                                                     | Nvarchar (60)  |                       |                                     |
| WMSLOCATION                   | INPUTLOCATION                                                                 | Nvarchar (60)  |                       |                                     |
| WMSLOCATION                 | WMSLOCATIONID                                                                 | Nvarchar (60)  |                       |                                     |
| WMSLOCATION                 | INVENTLOCATIONID                                                                 | Nvarchar (25)  |                       |                                     |
| INVENTLOCATION                | RBODEFAULTWMSLOCATIONID                                                       | Nvarchar (60)  |                       |                                     |
| INVENTLOCATION                               | WMSLOCATIONIDDEFAULTISSUE                                                     | Nvarchar (60)  |                       |                                     |
| INVENTLOCATION                            | WMSLOCATIONIDDEFAULTRECEIPT                                                   | Nvarchar (60)  |                       |                                     |
| INVENTLOCATION                            | 名前                                                   | Nvarchar (120)  |                       |                                     |
| INVENTLOCATION                            | INVENTLOCATIONID                                                   | Nvarchar (25)  |                       |                                     |
| PRICEDISCTABLE                | CONSTRAINT I\_137462222\_1904821809: { "action": "replace-line", "value": "CONSTRAINT \[I\_PRICEDISCTABLE\_RECID\] PRIMARY KEY CLUSTERED ( \[RECID\] ) "CONSTRAINT I\_PRICEDISCTABLE\_RECID": { "action": "remove-line" } |               |                       |                                     |
| PRICEDISCTABLE                            | UNITID                                                   | Nvarchar (20)  |                       |                                     |
| PRICEDISCTABLE                            | ITEMRELATION                                                   | Nvarchar (100)  |                       |                                     |
| OMOPERATINGUNIT               | OMOPERATINGUNITNUMBER                                                         | Nvarchar (30)  |                       |                                     |
| RETAILPARAMETERS              | USEADVANCEDAUTOCHARGE INT NULL DEFAULT(0)                                     |               |                       |                                     |
|                               | GIFTCARDINQUIRYPRINTHISTORY INT NULL DEFAULT(0)                               |               |                       |                                     |
| RETAILINFOCODETABLE           | PRINTINPUTONFISCALRECEIPT \[int\] NULL DEFAULT (0) PRINTTEXTONFISCALRECEIPT \[nvarchar\] (50) NULL DEFAULT('') |               |                       |    
| RETAILINFOCODETABLE           |PROMPT |  Nvarchar (350)              |                       |   |
| RETAILINFORMATIONSUBCODETABLE | PRINTTEXTONFISCALRECEIPT \[nvarchar\](50) NULL DEFAULT('')                    |               |                       |                                     |
| RETAILINFOCODETRANSLATION               | PROMPT                                                         | Nvarchar (350)  |                       |                                     |
| DIRPERSONNAME               | FIRSTNAME                                                         | Nvarchar (100)  |                       |                                     |
| DIRPERSONNAME               | LASTNAME                                                         | Nvarchar (100)  |                       |                                     |
| DIRPERSONNAME               | MIDDLENAME                                                         | Nvarchar (100)  |                       |                                     |
| DIRPARTYTABLE               | 名前                                                         | Nvarchar (300)  |                       |                                     |
| DIRPARTYTABLE               | NAMEALIAS                                                         | Nvarchar (150)  |                       |                                     |
| INVENTTABLE               | NAMEALIAS                                                         | Nvarchar (120)  |                       |                                     |
| INVENTTABLE               | ITEMID                                                         | Nvarchar (100)  |                       |                                     |
| INVENTTABLE               | ALTITEMID                                                         | Nvarchar (100)  |                       |                                     |
| ECORESPRODUCT               | SEARCHNAME                                                         | Nvarchar (150)  |                       |                                     |
| ECORESPRODUCT               | DISPLAYPRODUCTNUMBER                                                         | Nvarchar (190)  |                       |                                     |
| TAXSUBSTITUTIONCODETABLE\_BR               | ITEMID                                                         | Nvarchar (100)  |                       |                                     |
| INVENTITEMBARCODE               | ITEMID                                                         | Nvarchar (100)  |                       |                                     |
| INVENTTABLEMODULE               | ITEMID                                                         | Nvarchar (100)  |                       |                                     |
| INVENTTABLEMODULE               | UNITID                                                         | Nvarchar (20)  |                       |                                     |
| RETAILINVENTTABLE               | ITEMID                                                         | Nvarchar (100)  |                       |                                     |
| RETAILINVENTTABLE               | BASECOMPARISONUNITCODE                                                         | Nvarchar (20)  |                       |                                     |
| RETAILITEMONHANDQUANTITY               | ITEMID                                                         | Nvarchar (100)  |                       |                                     |
| TAXBENEFITCODESETUPDATA_BR               | ITEMRELATION                                                         | Nvarchar (100)  |                       |                                     |
| INVENTITEMGTIN               | ITEMID                                                         | Nvarchar (100)  |                       |                                     |
| INVENTITEMGTIN               | UNITID                                                         | Nvarchar (20)  |                       |                                     |
| INVENTITEMGTIN               | GLOBALTRADEITEMNUMBER                                                         | Nvarchar (16)  |                       |                                     |
| INVENTITEMGROUPITEM               | ITEMID                                                         | Nvarchar (100)  |                       |                                     |
| INVENTDIMCOMBINATION               | ITEMID                                                         | Nvarchar (100)  |                       |                                     |
| INVENTDIMCOMBINATION               | RETAILVARIANTID                                                         | Nvarchar (20)  |                       |                                     |
| TMPASSORTEDPRODUCTS               | ITEMID                                                         | Nvarchar (100)  |                       |                                     |
| INVENTORYINBOUNDOUTBOUNDSOURCEDOCUMENTLINE               | ITEMID                                                         | Nvarchar (100)  |                       |                                     |
| INVENTITEMSALESSETUP               | ITEMID                                                         | Nvarchar (100)  |                       |                                     |
| RETAILINVENTLINKEDITEM               | ITEMID                                                         | Nvarchar (100)  |                       |                                     |
| RETAILINVENTLINKEDITEM               | LINKEDITEMID                                                         | Nvarchar (100)  |                       |                                     |
| RETAILINVENTLINKEDITEM               | 単位                                                         | Nvarchar (20)  |                       |                                     |
| RETAILSTORETENDERTYPETABLE               | GIFTCARDITEMID                                                         | Nvarchar (100)  |                       |                                     |
| RETAILSTORETENDERTYPETABLE               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| WARRANTYINVENTTABLE               | ITEMID                                                         | Nvarchar (100)  |                       |                                     |
| INVENTORYINBOUNDOUTBOUNDDOCUMENTLINE               | ITEMID                                                         | Nvarchar (100)  |                       |                                     |
| TAXBURDEN\_BR               | ITEMID                                                         | Nvarchar (100)  |                       |                                     |
| RETAILFISCALDOCUMENTLINE_BR               | ITEMID                                                         | Nvarchar (100)  |                       |                                     |
| RETAILFISCALDOCUMENTLINE_BR               | 単位                                                         | Nvarchar (20)  |                       |                                     |
| RETAILFISCALDOCUMENTLINE_BR               | GLOBALTRADEITEMNUMBER                                                         | Nvarchar (16)  |                       |                                     |
| ECORESTRACKINGDIMENSIONGROUPITEM               | ITEMID                                                         | Nvarchar (100)  |                       |                                     |
| RETAILTRANSACTIONKITSDISASSEMBLYTRANS               | ITEMID                                                         | Nvarchar (100)  |                       |                                     |
| RETAILDLVMODEPRODUCTEXPLODED               | ITEMID                                                         | Nvarchar (100)  |                       |                                     |
| ECORESSTORAGEDIMENSIONGROUPITEM               | ITEMID                                                         | Nvarchar (100)  |                       |                                     |
| CUSTPACKINGSLIPTRANS               | ITEMID                                                         | Nvarchar (100)  |                       |                                     |
| ECORESPRODUCTTRANSLATION               | 名前                                                         | Nvarchar (250)  |                       |                                     |
| RETAILFISCALDOCUMENT\_BR                | FEADDRESSSTREET                                                       | Nvarchar (400)  |                       |                                     |
| RETAILFISCALDOCUMENT\_BR                | THIRDPARTYADDRESSSTREET                                                       | Nvarchar (400)  |                       |                                     |
| RETAILFISCALDOCUMENTREFERENCE\_BR                | REFRECEIPTNUMBER                                                       | Nvarchar (40)  |                       |                                     |
| RETAILFISCALDOCUMENT\_BR                | THIRDPARTYADDRESSSTREET                                                       | Nvarchar (400)  |                       |                                     |
| INVENTMODELGROUPITEM               | ITEMID                                                         | Nvarchar (100)  |                       |                                     |
| RETAILLABELCHANGEJOURNALTRANS               | ITEMID                                                         | Nvarchar (100)  |                       |                                     |
| RETAILFISCALDOCUMENTMODEL2LINE\_BR               | ITEMID                                                         | Nvarchar (100)  |                       |                                     |
| RETAILFISCALDOCUMENTMODEL2LINE\_BR                | 単位                                                         | Nvarchar (20)  |                       |                                     |
| RETAILFISCALRECEIPTLINE\_BR               | ITEMID                                                         | Nvarchar (100)  |                       |                                     |
| RETAILFISCALRECEIPTLINE\_BR               | 単位                                                         | Nvarchar (20)  |                       |                                     |
| RETAILINCOMEEXPENSEACCOUNTTABLE               | NAMEALIAS                                                         | Nvarchar (120)  |                       |                                     |
| RETAILINCOMEEXPENSEACCOUNTTABLE               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| ECORESATTRIBUTE               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| ECORESATTRIBUTETYPE               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| ERSOLUTIONVERSIONTABLE               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| RETAILTHEMEPALLET               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| KEYVAULTCERTIFICATETABLE               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| CUSTHIERARCHY               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| FISCALESTABLISHMENT_BR               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| INVENTITEMGROUP               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| LEDGER               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| INVENTSITE               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| TAXINFORMATION_IN               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| TAXRUNTIMEDOCMODELATTR               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| DOCUREF               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| ERTEXTFORMATVERSIONTABLE               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| FISCALESTABLISHMENTGROUP_BR               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| RETAILHARDWAREPROFILE               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| ACCOUNTANT_BR               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| RETAILCHANNELPROFILE               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| TAXRUNTIMEDOCCOMPONENTMEASURE               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| TAXRUNTIMEMODELATTR               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| TAXRATETYPE               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| ECORESTRACKINGDIMENSIONGROUP               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| RETAILUSERDEFINEDCERTIFICATEPROFILE               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| TAXRUNTIMECOMPONENT               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| RETAILSHAREDCONFIGURATIONPARAMETERS               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| TAXSOLUTIONSCOPE               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| TAXRUNTIMEREFERENCEMODELATTR               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| TAXRUNTIMELOOKUPSTRUCTURE               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| RETAILTILLLAYOUT               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| ECORESPRODUCTRELATIONTYPE               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| SYSTASKRECORDERFRAMEWORK               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| CUSTGROUP               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| CUSTGROUP               | CUSTGROUP                                                         | Nvarchar (25)  |                       |                                     |
| SYSTASKRECORDERINDUSTRY               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| FISCALDOCUMENTSOURCETEXT\_BR               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| RETAILTHEMEACCENT               | 名前                                                         | Nvarchar (120)  |                       |                                     |
| ECORESATTRIBUTEGROUP               | 名前                                                         | Nvarchar (120)  |                       |                                     |
|TAXRUNTIMELOOKUPSTRUCTUREFIELDBINDING  | 名前   | Nvarchar (120)  |          |           |  
|TAXRUNTIMEPOSTINGTYPE              | 名前   | Nvarchar (120)  |           |           |  
|RETAILVISUALPROFILE                    | 名前| Nvarchar (120)      |          |           |  
|TAXRUNTIMELOOKUP               | 名前| Nvarchar (120)      |          |          | 
|TAXRUNTIMEDOCMODELROWMEASURE          | 名前| Nvarchar (120)      |          |          |  
| TAXRUNTIMEMEASURE         | 名前| Nvarchar (120)      |          |          |  
| PRICEDISCGROUP            | 名前| Nvarchar (120)      |          |          |  
| SYSSERVICECONFIGURATIONSETTING | 名前| Nvarchar (120)      |          |          |  
| RETAILKEYBOARDBUTTONCONTROL    | 名前| Nvarchar (120)      |          |          |  
| RETAILDISCOUNTVALIDATIONPERIOD | 名前| Nvarchar (120)      |          |          |  
| ERFORMATMAPPINGVERSIONTABLE           | 名前| Nvarchar (120)      |          |          |  
| EXCHANGERATETYPE          | 名前| Nvarchar (120)      |          |          |  
| TAXRUNTIMEDOCCOMPONENT            | 名前| Nvarchar (120)      |          |          |  
| ERFORMATMAPPINGTABLE          | 名前| Nvarchar (120)      |          |          |  
| RETAILBUTTONGRID          | 名前| Nvarchar (120)      |          |          |  
| ERSOLUTIONTABLE           | 名前| Nvarchar (120)      |          |          |  
| RETAILTRANSACTIONATTRIBUTETRANS   | 名前| Nvarchar (120)      |          |          |  
| TAXRUNTIMEDOCCONTEXT          | 名前| Nvarchar (120)      |          |          |  
| TAXRUNTIMECOMPONENTMEASURE            | 名前| Nvarchar (120)      |          |          |  
| INVENTMODELGROUP          | 名前| Nvarchar (120)      |          |          |  
| RETAILPERIODICDISCOUNT            | 名前| Nvarchar (120)      |          |          |  
| DIRADDRESSBOOK            | 名前| Nvarchar (120)      |          |          |  
| RETAILFUNCTIONALITYPROFILE            | 名前| Nvarchar (120)      |          |          |  
| RETAILIDENTITYPROVIDER            | 名前| Nvarchar (120)      |          |          |  
| TAXRUNTIMEDOCTAXTYPE          | 名前| Nvarchar (120)      |          |          |  
| TAXRUNTIMEREFERENCEMODELROW           | 名前| Nvarchar (120)      |          |          |  
| RETAILPOSPERMISSIONGROUP          | 名前| Nvarchar (120)      |          |          |  
| TAXRUNTIMEDEFCONTEXT          | 名前| Nvarchar (120)      |          |          |  
| COMMISSIONSALESGROUP          | 名前| Nvarchar (120)      |          |          |  
| LOGISTICSLOCATIONROLE         | 名前| Nvarchar (120)      |          |          |  
| RETAILPOSTHEME            | 名前| Nvarchar (120)      |          |          |  
| TAXRUNTIMELOOKUPSTRUCTUREFIELD    | 名前| Nvarchar (120)      |          |          |  
| WHSINVENTSTATUS           | 名前| Nvarchar (120)      |          |          |  
| ERDATAMODELTABLE          | 名前| Nvarchar (120)      |          |          |  
| RETAILTERMINALTABLE           | 名前| Nvarchar (120)      |          |          |  
| RETAILFISCALINTEGRATIONDOCUMENTPROVIDERTABLE | 名前| Nvarchar (120)      |      |          |  
| TAXRUNTIMEMODEL           | 名前| Nvarchar (120)      |          |          |  
| TAXRUNTIMEDOCCOMPONENTPOSTINGPROFILEDET   | 名前| Nvarchar (120)      |          |          |  
| ERTEXTFORMATTABLE | 名前| Nvarchar (120)      |          |          |  
| RETAILTENDERTYPETABLE | 名前| Nvarchar (120)      |          |          |  
| TAXPERIODHEADER   | 名前| Nvarchar (120)      |          |          |  
| RETAILTABLEIDTABLE            | 名前| Nvarchar (120)      |          |          |  
| RETAILPERIODICDISCOUNTLINE            | 名前| Nvarchar (120)      |          |          |  
| RETAILCONNDATABASEPROFILE         | 名前| Nvarchar (120)      |          |          |  
| RETAILSTORETENDERTYPECARDTABLE    | 名前| Nvarchar (120)      |          |          |  
| RETAILAFFILIATION         | 名前| Nvarchar (120)      |          |          |  
| RETAILONLINECHANNELFUNCTIONALITYPROFILETABLE| 名前| Nvarchar (120)      |        |          |  
| TAXRUNTIMEREFERENCEMODEL          | 名前| Nvarchar (120)      |          |          |  
| RETAILTENDERTYPECARDTABLE         | 名前| Nvarchar (120)      |          |          |  
| ERVENDORTABLE         | 名前| Nvarchar (120)      |          |          |  
| ERMODELMAPPINGTABLE           | 名前| Nvarchar (120)      |          |          |  
| RETAILDRAWERPOOLDEVICE            | 名前| Nvarchar (120)      |          |          |  
| RETAILDRAWERPOOL          | 名前| Nvarchar (120)      |          |          |  
| RETAILCONFIGURATIONPARAMETERS | 名前| Nvarchar (120)      |          |          |  
| TAXENGINESQLDICTIONARY            | 名前| Nvarchar (120)      |          |          |  
| LOGISTICSADDRESSFORMATHEADING | 名前| Nvarchar (120)      |          |          |  
| TAXRUNTIMEDOCMODELROW         | 名前| Nvarchar (120)      |          |          |  
| RETAILCDXDATAGROUP            | 名前| Nvarchar (120)      |          |          |  
| ECORESPRODUCTMASTERDIMVALUETRANSLATION    | 名前| Nvarchar (120)      |          |          |  
| TAXRUNTIMELOOKUPSTRUCTUREBINDING  | 名前| Nvarchar (120)      |          |          |  
| RETAILTRANSACTIONSERVICEPROFILE   | 名前| Nvarchar (120)      |          |          |  
| RETAILSTORESAFE           | 名前| Nvarchar (120)      |          |          |  
| TAXRUNTIMETAXTYPE         | 名前| Nvarchar (120)      |          |          |  
| RETAILTERMINALCUSTOMFIELD         | 名前| Nvarchar (120)      |          |          |  
| RETAILFISCALINTEGRATIONCONNECTORTABLE | 名前| Nvarchar (120)      |          |          |  
| TAXRUNTIMEMODELROW            | 名前| Nvarchar (120)      |          |          |  
| ERDATAMODELVERSIONTABLE           | 名前| Nvarchar (120)      |          |          |  
| TAXRUNTIMEDOCCOMPONENTPOSTINGPROFILE | 名前| Nvarchar (120)      |          |          |  
| TAXRUNTIMEDOCMODEL            | 名前| Nvarchar (120)      |          |          |  
| RETAILPOSITIONPOSPERMISSION           | 名前| Nvarchar (120)      |          |          |  
| RETAILTENDERDISCOUNT          | 名前| Nvarchar (120)      |          |          |  
|RETAILDLVMODEADDRESSEXPLODED | STATE | Nvarchar (60)      |          |          |  
| INVENTLOCATIONDEFAULTLOCATION | INVENTLOCATIONID | Nvarchar (25)     |   |          |  
| RETAILRETURNPOLICYLINE    | INVENTLOCATIONID | Nvarchar (25)      |          |          |  
| RETAILRETURNINFOCODEPOLICYLINE        | INVENTLOCATIONID | Nvarchar (25)      |     |       |  
| RETAILRETURNREASONCODEPOLICYLINE |    INVENTLOCATIONID | Nvarchar (25)      |          |        |  
| RETAILPRODUCTWAREHOUSEINVENTORY   | INVENTLOCATIONID | Nvarchar (25)      |        |       |  
| RETAILPUBRETAILSTORETABLE | INVENTLOCATIONIDFORCUSTOMERORDER | Nvarchar (25)   |    |      |  
| RETAILSTORETABLE | INVENTLOCATIONIDFORCUSTOMERORDER | Nvarchar (25)      |      |          |  
| RETAILSTORELOCATORGROUPMEMBER | INVENTLOCATIONID | Nvarchar (25)      |          |          |  
| RETAILTRANSACTIONORDERINVOICETRANS       | INVOICEID | Nvarchar (40)      |          |          |  
| RETAILTRANSACTIONTABLE       | INVENTLOCATIONID | Nvarchar (25)      |          |          |  
| RETAILTRANSACTIONTABLE       | CUSTOMERNAME | Nvarchar (300)      |          |          |  
| RETAILCHANNELTABLE           | INVENTLOCATION | Nvarchar (25)      |          |          |  
| RETAILPUBRETAILCHANNELTABLE    | INVENTLOCATION | Nvarchar (25)      |          |          |  
| UNITOFMEASURE         | SYMBOL | Nvarchar (20)      |          |          |  
| RETAILPRODUCTLISTLINEUPDATE       | UNITOFMEASURE | Nvarchar (20)      |          |          |  
| RETAILUNIT            | UNITID | Nvarchar (20)      |          |          |  
| LOGISTICSELECTRONICADDRESS      | COUNTRYREGIONCODE | Nvarchar (10)      |          |          |  
| REQITEMTABLE          | ITEMID | Nvarchar (100)      |          |          |  
| GUPITEMBASEPRICE          | ITEMID | Nvarchar (100)      |          |          |  
| AGREEMENTLINE         | ITEMID | Nvarchar (100)      |          |          |  
| MARKUPAUTOTABLE           | ITEMRELATION | Nvarchar (100)      |          |          |  
| MARKUPAUTOLINE            | TAXITEMGROUP | Nvarchar (100)      |          |          |
| MARKUPTABLE           | TAXITEMGROUP | Nvarchar (100)      |          |          |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
