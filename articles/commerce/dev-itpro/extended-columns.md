---
title: チャネル データベースの事前拡張された列
description: このトピックでは、チャネル データベース内の事前拡張された列がどのように拡張に使用されるかについて説明します。
author: mugunthanm
manager: AnnBe
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2020-02-02
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: b5af2ec35e8f359169e100547556f74454fe73ac
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681572"
---
# <a name="pre-extended-columns-in-the-channel-database"></a>チャネル データベースの事前拡張された列

[!include [banner](../../includes/banner.md)]

チャネル データベース内の一部の列は、*事前拡張* されています。 つまり、チャンネルデータベースの列の長さが Microsoft Dynamics 365 Commerce 本体が規定する列の長さを超えています。 たとえば、**INVENTSERIALID** フィールドの長さは、Commerce 本体のデータベースでは 20 文字、チャネル データベースでは 50 文字です。

チャネル データベースのフィールドは拡張されることは多いですが、フィールドの列の長さは拡張に対応していません。 したがって、拡張が必要となった場合にも対応できるよう、標準で列の長さが増設されています。

> [!NOTE]
> 事前拡張されていないフィールドを拡張する必要がある場合は、Lifecycle Services (LCS) で拡張リクエストを提出する必要があります。 詳細については、[拡張性要求](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/extensibility/extensibility-requests) を参照してください。

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
| LOGISTICSADDRESSCITY          | COUNTYID                                                                      | Nvarchar (60)  |                       |                                     |
| LOGISTICSADDRESSCOUNTY        | COUNTYID                                                                      | Nvarchar (60)  |                       |                                     |
| LOGISTICSADDRESSDISTRICT      | COUNTYID\_RU                                                                  | Nvarchar (60)  |                       |                                     |
| LOGISTICSADDRESSZIPCODE       | STREETNAME                                                                    | Nvarchar (400) |                       |                                     |
| LOGISTICSADDRESSZIPCODE       | COUNTY                                                                        | Nvarchar (60)  |                       |                                     |
| RETAILASYNCADDRESS            | STREET                                                                        | Nvarchar (400) |                       |                                     |
| RETAILASYNCADDRESS            | COUNTY                                                                        | Nvarchar (60)  |                       |                                     |
| RETAILASYNCCUSTOMER           | STREET                                                                        | Nvarchar (400) |                       |                                     |
| RETAILASYNCCUSTOMER           | COUNTY                                                                        | Nvarchar (60)  |                       |                                     |
| RETAILFISCALDOCUMENT\_BR      | FEADDRESSSTREET                                                               | Nvarchar (400) |                       |                                     |
| RETAILFISCALDOCUMENT\_BR      | THIRDPARTYADDRESSSTREET                                                       | Nvarchar (400) |                       |                                     |
| RETAILTAXFILTERS              | COUNTYID                                                                      | Nvarchar (60)  |                       |                                     |
| RETAILTRANSACTIONADDRESSTRANS | STREET                                                                        | Nvarchar (400) |                       |                                     |
| RETAILTRANSACTIONADDRESSTRANS | COUNTY                                                                        | Nvarchar (60)  |                       |                                     |
| RETAILTRANSACTIONSALESTRANS   | INVENTBATCHID                                                                 | Nvarchar (50)  |                       |                                     |
| RETAILTRANSACTIONSALESTRANS   | INVENTSERIALID                                                                | Nvarchar (50)  |                       |                                     |
| RETAILTRANSACTIONSALESTRANS   | WAREHOUSELOCATION                                                             | Nvarchar (60)  |                       |                                     |
| INVENTDIM                     | INVENTBATCHID                                                                 | Nvarchar (50)  |                       |                                     |
| INVENTDIM                     | INVENTSERIALID                                                                | Nvarchar (50)  |                       |                                     |
| INVENTDIM                     | CONFIGID                                                                      | Nvarchar (60)  |                       |                                     |
| INVENTDIM                     | INVENTCOLORID                                                                 | Nvarchar (60)  |                       |                                     |
| INVENTDIM                     | INVENTSIZEID                                                                  | Nvarchar (60)  |                       |                                     |
| INVENTDIM                     | INVENTSTYLEID                                                                 | Nvarchar (60)  |                       |                                     |
| INVENTDIM                     | WMSLOCATIONID                                                                 | Nvarchar (60)  |                       |                                     |
| ECORESCOLOR                   | 氏名                                                                          | Nvarchar (60)  |                       |                                     |
| ECORESSTYLE                   | 氏名                                                                          | Nvarchar (60)  |                       |                                     |
| ECORESCONFIGURATION           | 氏名                                                                          | Nvarchar (60)  |                       |                                     |
| ECORESSIZE                    | 氏名                                                                          | Nvarchar (60)  |                       |                                     |
| RETAILTABLEFIELDID            | TABLENAME                                                                     | Nvarchar (81)  |                       |                                     |
|                               | FIELDNAME                                                                     | Nvarchar (81)  |                       |                                     |
| RETAILTRANSACTIONTAXTRANSGTE  | TAXCOMPONENT                                                                  | Nvarchar (60)  |                       |                                     |
| TAXCOMPONENTTABLE\_IN         | COMPONENT                                                                     | Nvarchar (60)  |                       |                                     |
| WMSLOCATION                   | INPUTLOCATION                                                                 | Nvarchar (60)  |                       |                                     |
|                               | WMSLOCATIONID                                                                 | Nvarchar (60)  |                       |                                     |
| INVENTLOCATION                | RBODEFAULTWMSLOCATIONID                                                       | Nvarchar (60)  |                       |                                     |
|                               | WMSLOCATIONIDDEFAULTISSUE                                                     | Nvarchar (60)  |                       |                                     |
|                               | WMSLOCATIONIDDEFAULTRECEIPT                                                   | Nvarchar (60)  |                       |                                     |
| PRICEDISCTABLE                | CONSTRAINT I\_137462222\_1904821809: { "action": "replace-line", "value": "CONSTRAINT \[I\_PRICEDISCTABLE\_RECID\] PRIMARY KEY CLUSTERED ( \[RECID\] ) "CONSTRAINT I\_PRICEDISCTABLE\_RECID": { "action": "remove-line" } |               |                       |                                     |
| OMOPERATINGUNIT               | OMOPERATINGUNITNUMBER                                                         | Nvarchar (30)  |                       |                                     |
| RETAILPARAMETERS              | USEADVANCEDAUTOCHARGE INT NULL DEFAULT(0)                                     |               |                       |                                     |
|                               | GIFTCARDINQUIRYPRINTHISTORY INT NULL DEFAULT(0)                               |               |                       |                                     |
| RETAILINFOCODETABLE           | PRINTINPUTONFISCALRECEIPT \[int\] NULL DEFAULT (0) PRINTTEXTONFISCALRECEIPT \[nvarchar\] (50) NULL DEFAULT('') |               |                       |                                     |
| RETAILINFORMATIONSUBCODETABLE | PRINTTEXTONFISCALRECEIPT \[nvarchar\](50) NULL DEFAULT('')                    |               |                       |                                     |
