---
title: チャネル データベースの事前拡張された列
description: このトピックでは、チャネル データベース内の事前拡張された列がどのように拡張に使用されるかについて説明します。
author: mugunthanm
manager: AnnBe
ms.date: 02/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2020-02-02
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 2961c6a0bf0c928b1804f06a6ab0b875b63b1757
ms.sourcegitcommit: 2464f371101ba616f472bab1631b0ecb863006ce
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/03/2020
ms.locfileid: "3095600"
---
# <a name="pre-extended-columns-in-the-channel-database"></a><span data-ttu-id="978bb-103">チャネル データベースの事前拡張された列</span><span class="sxs-lookup"><span data-stu-id="978bb-103">Pre-extended columns in the channel database</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="978bb-104">チャネル データベース内の一部の列は、*事前拡張* されています。</span><span class="sxs-lookup"><span data-stu-id="978bb-104">Some columns in the channel database are *pre-extended*.</span></span> <span data-ttu-id="978bb-105">つまり、チャンネルデータベースの列の長さが Microsoft Dynamics 365 Commerce 本体が規定する列の長さを超えています。</span><span class="sxs-lookup"><span data-stu-id="978bb-105">In other words, the column length in the channel database exceeds the column length in Microsoft Dynamics 365 Commerce Headquarters.</span></span> <span data-ttu-id="978bb-106">たとえば、**INVENTSERIALID** フィールドの長さは、Commerce 本体のデータベースでは 20 文字、チャネル データベースでは 50 文字です。</span><span class="sxs-lookup"><span data-stu-id="978bb-106">For example, the length of the **INVENTSERIALID** field is 20 characters in the Commerce Headquarters database but 50 characters in the channel database.</span></span>

<span data-ttu-id="978bb-107">チャネル データベースのフィールドは拡張されることは多いですが、フィールドの列の長さは拡張に対応していません。</span><span class="sxs-lookup"><span data-stu-id="978bb-107">Although fields in the channel database are often extended, column lengths for those fields aren't extensible.</span></span> <span data-ttu-id="978bb-108">したがって、拡張が必要となった場合にも対応できるよう、標準で列の長さが増設されています。</span><span class="sxs-lookup"><span data-stu-id="978bb-108">Therefore, out-of-box column lengths have been increased to support extension scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="978bb-109">事前拡張されていないフィールドを拡張する必要がある場合は、拡張リクエストまたはサポート チケットを提出する必要があります。</span><span class="sxs-lookup"><span data-stu-id="978bb-109">If you must extend a field that isn't already pre-extended, you must file an extension request or a support ticket.</span></span>

<span data-ttu-id="978bb-110">このフィールドは、チャネル データベースで拡張されますが、拡張データ型 (EDT) の拡張モデルを使用して、Commerce 本体のデータベースのフィールドも拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="978bb-110">Although the fields are extended in the channel database, your extension must also extend the field in the Commerce Headquarters database by using the extended data type (EDT) extension model.</span></span> <span data-ttu-id="978bb-111">さらに、これに対応する販売時点管理 (POS) 、または Commerce Runtime (CRT) ユーザー インターフェイス (UI) を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="978bb-111">Additionally, you must extend the corresponding point of sale (POS) or Commerce runtime (CRT) user interface (UI).</span></span>

<span data-ttu-id="978bb-112">Commerce 本体のデータベースが拡張されていない場合は、チャネル データベースと Commerce 本体のデータベース間の同期が、P-ジョブの実行中に失敗するか、または余分な文字が切り捨てられます。</span><span class="sxs-lookup"><span data-stu-id="978bb-112">If the Commerce Headquarters database isn't extended, either synchronization between the channel database and the Commerce Headquarters database will fail during the P-job or the extra characters will be truncated.</span></span> <span data-ttu-id="978bb-113">同様に、対応する販売時点管理 (POS) ユーザー インターフェイス (UI) または Commerce Runtime (CRT) が拡張されていない場合は、検証をすることで既定の文字長を超える文字の入力を防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="978bb-113">Likewise, if the corresponding point of sale (POS) user interface (UI) or the Commerce runtime (CRT) isn't extended, validation will prevent more than the default character length from being entered.</span></span> <span data-ttu-id="978bb-114">既定の長さは、Commerce 本体のデータベースにおける "基準" 列の長さによって決まります。</span><span class="sxs-lookup"><span data-stu-id="978bb-114">The default length is determined by the base column length in the Commerce Headquarters database.</span></span>

<span data-ttu-id="978bb-115">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="978bb-115">Here are some examples:</span></span>

- <span data-ttu-id="978bb-116">チャネル データベースの **INVENTSERIALID** フィールドの長さは 50 文字ですが、POS UI では最大で 20 文字までのシリアル番号が入力できます。</span><span class="sxs-lookup"><span data-stu-id="978bb-116">The length of the **INVENTSERIALID** field in the channel database is 50 characters, but the POS UI accepts serial numbers that are a maximum of only 20 characters long.</span></span> <span data-ttu-id="978bb-117">この場合は、POS UI と Commerce 本体のデータベースの両方のフィールドを拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="978bb-117">In this case, you must extend the field in both the POS UI and the Commerce Headquarters database.</span></span>
- <span data-ttu-id="978bb-118">チャネルデータベースの **番地** フィールドの長さは、400文字まで拡張されますが、CRT の検証では Commerce 本体のデータベースの既定の長さを超えることは認められません。</span><span class="sxs-lookup"><span data-stu-id="978bb-118">The length of the **STREET** field in the channel database is extended to 400 characters, but validation in CRT prevents more than the default length in the Commerce Headquarters database from being accepted.</span></span> <span data-ttu-id="978bb-119">この場合は、CRT 要求ハンドラー (**ValidateAddressLengthServiceRequest**) と Commerce 本体のデータベースの両方を拡張して、**番地**フィールドで 400 文字を使用できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="978bb-119">In this case, you must extend both the CRT request handler (**ValidateAddressLengthServiceRequest**) and the Commerce Headquarters database, so that 400 characters are accepted for the **STREET** field.</span></span>

<span data-ttu-id="978bb-120">一部のフィールドは、POS 内の読み取り専用フィールドである可能性があるため、POS UI または CRT ハンドラーの拡張は不要です。</span><span class="sxs-lookup"><span data-stu-id="978bb-120">Extension of the POS UI or CRT handlers isn't required for some fields, because they might be read-only fields in POS.</span></span> <span data-ttu-id="978bb-121">たとえば、**ECORES** 製品に関連するフィールドは読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="978bb-121">For example, **ECORES** product-related fields are read-only.</span></span> <span data-ttu-id="978bb-122">POS では製品の作成に対応していないため、POS では製品の書き込みシナリオが存在しません。</span><span class="sxs-lookup"><span data-stu-id="978bb-122">Because product creation isn't supported in POS, there is no write scenario for products in POS.</span></span>

## <a name="sample-code-to-override-the-validateaddresslengthservicerequest-handler"></a><span data-ttu-id="978bb-123">ValidateAddressLengthServiceRequest ハンドラーをオーバーライドするサンプルコード</span><span class="sxs-lookup"><span data-stu-id="978bb-123">Sample code to override the ValidateAddressLengthServiceRequest handler</span></span>

<span data-ttu-id="978bb-124">次の例では、**ValidateAddressLengthServiceRequest** を上書きする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="978bb-124">The following example shows how to override the **ValidateAddressLengthServiceRequest** handler.</span></span>

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

## <a name="pre-extended-columns-in-the-channel-database"></a><span data-ttu-id="978bb-125">チャネル データベースの事前拡張された列</span><span class="sxs-lookup"><span data-stu-id="978bb-125">Pre-extended columns in the channel database</span></span>

<span data-ttu-id="978bb-126">次の表に、事前拡張されている列の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="978bb-126">The following table lists the columns that are pre-extended.</span></span>

| <span data-ttu-id="978bb-127">テーブル</span><span class="sxs-lookup"><span data-stu-id="978bb-127">Table</span></span>                         | <span data-ttu-id="978bb-128">円柱</span><span class="sxs-lookup"><span data-stu-id="978bb-128">Column</span></span>                                                                        | <span data-ttu-id="978bb-129">期間</span><span class="sxs-lookup"><span data-stu-id="978bb-129">Length</span></span>        | <span data-ttu-id="978bb-130">CRT の拡張機能</span><span class="sxs-lookup"><span data-stu-id="978bb-130">Extension in CRT</span></span>      | <span data-ttu-id="978bb-131">POS の拡張機能</span><span class="sxs-lookup"><span data-stu-id="978bb-131">Extension in POS</span></span>                    |
|-------------------------------|-------------------------------------------------------------------------------|---------------|-----------------------|-------------------------------------|
| <span data-ttu-id="978bb-132">INVENTSERIAL</span><span class="sxs-lookup"><span data-stu-id="978bb-132">INVENTSERIAL</span></span>                  | <span data-ttu-id="978bb-133">INVENTSERIALID</span><span class="sxs-lookup"><span data-stu-id="978bb-133">INVENTSERIALID</span></span>                                                                | <span data-ttu-id="978bb-134">Nvarchar (50)</span><span class="sxs-lookup"><span data-stu-id="978bb-134">nvarchar(50)</span></span>  |                       | <span data-ttu-id="978bb-135">GetSerialNumberClientRequestHandler</span><span class="sxs-lookup"><span data-stu-id="978bb-135">GetSerialNumberClientRequestHandler</span></span> |
| <span data-ttu-id="978bb-136">LOGISTICSPOSTALADDRESS</span><span class="sxs-lookup"><span data-stu-id="978bb-136">LOGISTICSPOSTALADDRESS</span></span>        | <span data-ttu-id="978bb-137">住所</span><span class="sxs-lookup"><span data-stu-id="978bb-137">ADDRESS</span></span>                                                                       | <span data-ttu-id="978bb-138">Nvarchar (500)</span><span class="sxs-lookup"><span data-stu-id="978bb-138">nvarchar(500)</span></span> | <span data-ttu-id="978bb-139">ValidateAddressLength</span><span class="sxs-lookup"><span data-stu-id="978bb-139">ValidateAddressLength</span></span> |                                     |
| <span data-ttu-id="978bb-140">LOGISTICSPOSTALADDRESS</span><span class="sxs-lookup"><span data-stu-id="978bb-140">LOGISTICSPOSTALADDRESS</span></span>        | <span data-ttu-id="978bb-141">STREET</span><span class="sxs-lookup"><span data-stu-id="978bb-141">STREET</span></span>                                                                        | <span data-ttu-id="978bb-142">Nvarchar (400)</span><span class="sxs-lookup"><span data-stu-id="978bb-142">nvarchar(400)</span></span> | <span data-ttu-id="978bb-143">ValidateAddressLength</span><span class="sxs-lookup"><span data-stu-id="978bb-143">ValidateAddressLength</span></span> |                                     |
| <span data-ttu-id="978bb-144">LOGISTICSPOSTALADDRESS</span><span class="sxs-lookup"><span data-stu-id="978bb-144">LOGISTICSPOSTALADDRESS</span></span>        | <span data-ttu-id="978bb-145">COUNTY</span><span class="sxs-lookup"><span data-stu-id="978bb-145">COUNTY</span></span>                                                                        | <span data-ttu-id="978bb-146">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="978bb-146">nvarchar(60)</span></span>  | <span data-ttu-id="978bb-147">ValidateAddressLength</span><span class="sxs-lookup"><span data-stu-id="978bb-147">ValidateAddressLength</span></span> |                                     |
| <span data-ttu-id="978bb-148">LOGISTICSADDRESSCITY</span><span class="sxs-lookup"><span data-stu-id="978bb-148">LOGISTICSADDRESSCITY</span></span>          | <span data-ttu-id="978bb-149">COUNTYID</span><span class="sxs-lookup"><span data-stu-id="978bb-149">COUNTYID</span></span>                                                                      | <span data-ttu-id="978bb-150">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="978bb-150">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="978bb-151">LOGISTICSADDRESSCOUNTY</span><span class="sxs-lookup"><span data-stu-id="978bb-151">LOGISTICSADDRESSCOUNTY</span></span>        | <span data-ttu-id="978bb-152">COUNTYID</span><span class="sxs-lookup"><span data-stu-id="978bb-152">COUNTYID</span></span>                                                                      | <span data-ttu-id="978bb-153">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="978bb-153">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="978bb-154">LOGISTICSADDRESSDISTRICT</span><span class="sxs-lookup"><span data-stu-id="978bb-154">LOGISTICSADDRESSDISTRICT</span></span>      | <span data-ttu-id="978bb-155">COUNTYID\_RU</span><span class="sxs-lookup"><span data-stu-id="978bb-155">COUNTYID\_RU</span></span>                                                                  | <span data-ttu-id="978bb-156">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="978bb-156">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="978bb-157">LOGISTICSADDRESSZIPCODE</span><span class="sxs-lookup"><span data-stu-id="978bb-157">LOGISTICSADDRESSZIPCODE</span></span>       | <span data-ttu-id="978bb-158">STREETNAME</span><span class="sxs-lookup"><span data-stu-id="978bb-158">STREETNAME</span></span>                                                                    | <span data-ttu-id="978bb-159">Nvarchar (400)</span><span class="sxs-lookup"><span data-stu-id="978bb-159">nvarchar(400)</span></span> |                       |                                     |
| <span data-ttu-id="978bb-160">LOGISTICSADDRESSZIPCODE</span><span class="sxs-lookup"><span data-stu-id="978bb-160">LOGISTICSADDRESSZIPCODE</span></span>       | <span data-ttu-id="978bb-161">COUNTY</span><span class="sxs-lookup"><span data-stu-id="978bb-161">COUNTY</span></span>                                                                        | <span data-ttu-id="978bb-162">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="978bb-162">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="978bb-163">RETAILASYNCADDRESS</span><span class="sxs-lookup"><span data-stu-id="978bb-163">RETAILASYNCADDRESS</span></span>            | <span data-ttu-id="978bb-164">STREET</span><span class="sxs-lookup"><span data-stu-id="978bb-164">STREET</span></span>                                                                        | <span data-ttu-id="978bb-165">Nvarchar (400)</span><span class="sxs-lookup"><span data-stu-id="978bb-165">nvarchar(400)</span></span> |                       |                                     |
| <span data-ttu-id="978bb-166">RETAILASYNCADDRESS</span><span class="sxs-lookup"><span data-stu-id="978bb-166">RETAILASYNCADDRESS</span></span>            | <span data-ttu-id="978bb-167">COUNTY</span><span class="sxs-lookup"><span data-stu-id="978bb-167">COUNTY</span></span>                                                                        | <span data-ttu-id="978bb-168">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="978bb-168">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="978bb-169">RETAILASYNCCUSTOMER</span><span class="sxs-lookup"><span data-stu-id="978bb-169">RETAILASYNCCUSTOMER</span></span>           | <span data-ttu-id="978bb-170">STREET</span><span class="sxs-lookup"><span data-stu-id="978bb-170">STREET</span></span>                                                                        | <span data-ttu-id="978bb-171">Nvarchar (400)</span><span class="sxs-lookup"><span data-stu-id="978bb-171">nvarchar(400)</span></span> |                       |                                     |
| <span data-ttu-id="978bb-172">RETAILASYNCCUSTOMER</span><span class="sxs-lookup"><span data-stu-id="978bb-172">RETAILASYNCCUSTOMER</span></span>           | <span data-ttu-id="978bb-173">COUNTY</span><span class="sxs-lookup"><span data-stu-id="978bb-173">COUNTY</span></span>                                                                        | <span data-ttu-id="978bb-174">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="978bb-174">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="978bb-175">RETAILFISCALDOCUMENT\_BR</span><span class="sxs-lookup"><span data-stu-id="978bb-175">RETAILFISCALDOCUMENT\_BR</span></span>      | <span data-ttu-id="978bb-176">FEADDRESSSTREET</span><span class="sxs-lookup"><span data-stu-id="978bb-176">FEADDRESSSTREET</span></span>                                                               | <span data-ttu-id="978bb-177">Nvarchar (400)</span><span class="sxs-lookup"><span data-stu-id="978bb-177">nvarchar(400)</span></span> |                       |                                     |
| <span data-ttu-id="978bb-178">RETAILFISCALDOCUMENT\_BR</span><span class="sxs-lookup"><span data-stu-id="978bb-178">RETAILFISCALDOCUMENT\_BR</span></span>      | <span data-ttu-id="978bb-179">THIRDPARTYADDRESSSTREET</span><span class="sxs-lookup"><span data-stu-id="978bb-179">THIRDPARTYADDRESSSTREET</span></span>                                                       | <span data-ttu-id="978bb-180">Nvarchar (400)</span><span class="sxs-lookup"><span data-stu-id="978bb-180">nvarchar(400)</span></span> |                       |                                     |
| <span data-ttu-id="978bb-181">RETAILTAXFILTERS</span><span class="sxs-lookup"><span data-stu-id="978bb-181">RETAILTAXFILTERS</span></span>              | <span data-ttu-id="978bb-182">COUNTYID</span><span class="sxs-lookup"><span data-stu-id="978bb-182">COUNTYID</span></span>                                                                      | <span data-ttu-id="978bb-183">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="978bb-183">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="978bb-184">RETAILTRANSACTIONADDRESSTRANS</span><span class="sxs-lookup"><span data-stu-id="978bb-184">RETAILTRANSACTIONADDRESSTRANS</span></span> | <span data-ttu-id="978bb-185">STREET</span><span class="sxs-lookup"><span data-stu-id="978bb-185">STREET</span></span>                                                                        | <span data-ttu-id="978bb-186">Nvarchar (400)</span><span class="sxs-lookup"><span data-stu-id="978bb-186">nvarchar(400)</span></span> |                       |                                     |
| <span data-ttu-id="978bb-187">RETAILTRANSACTIONADDRESSTRANS</span><span class="sxs-lookup"><span data-stu-id="978bb-187">RETAILTRANSACTIONADDRESSTRANS</span></span> | <span data-ttu-id="978bb-188">COUNTY</span><span class="sxs-lookup"><span data-stu-id="978bb-188">COUNTY</span></span>                                                                        | <span data-ttu-id="978bb-189">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="978bb-189">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="978bb-190">RETAILTRANSACTIONSALESTRANS</span><span class="sxs-lookup"><span data-stu-id="978bb-190">RETAILTRANSACTIONSALESTRANS</span></span>   | <span data-ttu-id="978bb-191">INVENTBATCHID</span><span class="sxs-lookup"><span data-stu-id="978bb-191">INVENTBATCHID</span></span>                                                                 | <span data-ttu-id="978bb-192">Nvarchar (50)</span><span class="sxs-lookup"><span data-stu-id="978bb-192">nvarchar(50)</span></span>  |                       |                                     |
| <span data-ttu-id="978bb-193">RETAILTRANSACTIONSALESTRANS</span><span class="sxs-lookup"><span data-stu-id="978bb-193">RETAILTRANSACTIONSALESTRANS</span></span>   | <span data-ttu-id="978bb-194">INVENTSERIALID</span><span class="sxs-lookup"><span data-stu-id="978bb-194">INVENTSERIALID</span></span>                                                                | <span data-ttu-id="978bb-195">Nvarchar (50)</span><span class="sxs-lookup"><span data-stu-id="978bb-195">nvarchar(50)</span></span>  |                       |                                     |
| <span data-ttu-id="978bb-196">RETAILTRANSACTIONSALESTRANS</span><span class="sxs-lookup"><span data-stu-id="978bb-196">RETAILTRANSACTIONSALESTRANS</span></span>   | <span data-ttu-id="978bb-197">WAREHOUSELOCATION</span><span class="sxs-lookup"><span data-stu-id="978bb-197">WAREHOUSELOCATION</span></span>                                                             | <span data-ttu-id="978bb-198">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="978bb-198">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="978bb-199">INVENTDIM</span><span class="sxs-lookup"><span data-stu-id="978bb-199">INVENTDIM</span></span>                     | <span data-ttu-id="978bb-200">INVENTBATCHID</span><span class="sxs-lookup"><span data-stu-id="978bb-200">INVENTBATCHID</span></span>                                                                 | <span data-ttu-id="978bb-201">Nvarchar (50)</span><span class="sxs-lookup"><span data-stu-id="978bb-201">nvarchar(50)</span></span>  |                       |                                     |
| <span data-ttu-id="978bb-202">INVENTDIM</span><span class="sxs-lookup"><span data-stu-id="978bb-202">INVENTDIM</span></span>                     | <span data-ttu-id="978bb-203">INVENTSERIALID</span><span class="sxs-lookup"><span data-stu-id="978bb-203">INVENTSERIALID</span></span>                                                                | <span data-ttu-id="978bb-204">Nvarchar (50)</span><span class="sxs-lookup"><span data-stu-id="978bb-204">nvarchar(50)</span></span>  |                       |                                     |
| <span data-ttu-id="978bb-205">INVENTDIM</span><span class="sxs-lookup"><span data-stu-id="978bb-205">INVENTDIM</span></span>                     | <span data-ttu-id="978bb-206">CONFIGID</span><span class="sxs-lookup"><span data-stu-id="978bb-206">CONFIGID</span></span>                                                                      | <span data-ttu-id="978bb-207">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="978bb-207">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="978bb-208">INVENTDIM</span><span class="sxs-lookup"><span data-stu-id="978bb-208">INVENTDIM</span></span>                     | <span data-ttu-id="978bb-209">INVENTCOLORID</span><span class="sxs-lookup"><span data-stu-id="978bb-209">INVENTCOLORID</span></span>                                                                 | <span data-ttu-id="978bb-210">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="978bb-210">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="978bb-211">INVENTDIM</span><span class="sxs-lookup"><span data-stu-id="978bb-211">INVENTDIM</span></span>                     | <span data-ttu-id="978bb-212">INVENTSIZEID</span><span class="sxs-lookup"><span data-stu-id="978bb-212">INVENTSIZEID</span></span>                                                                  | <span data-ttu-id="978bb-213">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="978bb-213">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="978bb-214">INVENTDIM</span><span class="sxs-lookup"><span data-stu-id="978bb-214">INVENTDIM</span></span>                     | <span data-ttu-id="978bb-215">INVENTSTYLEID</span><span class="sxs-lookup"><span data-stu-id="978bb-215">INVENTSTYLEID</span></span>                                                                 | <span data-ttu-id="978bb-216">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="978bb-216">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="978bb-217">INVENTDIM</span><span class="sxs-lookup"><span data-stu-id="978bb-217">INVENTDIM</span></span>                     | <span data-ttu-id="978bb-218">WMSLOCATIONID</span><span class="sxs-lookup"><span data-stu-id="978bb-218">WMSLOCATIONID</span></span>                                                                 | <span data-ttu-id="978bb-219">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="978bb-219">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="978bb-220">ECORESCOLOR</span><span class="sxs-lookup"><span data-stu-id="978bb-220">ECORESCOLOR</span></span>                   | <span data-ttu-id="978bb-221">氏名</span><span class="sxs-lookup"><span data-stu-id="978bb-221">NAME</span></span>                                                                          | <span data-ttu-id="978bb-222">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="978bb-222">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="978bb-223">ECORESSTYLE</span><span class="sxs-lookup"><span data-stu-id="978bb-223">ECORESSTYLE</span></span>                   | <span data-ttu-id="978bb-224">氏名</span><span class="sxs-lookup"><span data-stu-id="978bb-224">NAME</span></span>                                                                          | <span data-ttu-id="978bb-225">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="978bb-225">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="978bb-226">ECORESCONFIGURATION</span><span class="sxs-lookup"><span data-stu-id="978bb-226">ECORESCONFIGURATION</span></span>           | <span data-ttu-id="978bb-227">氏名</span><span class="sxs-lookup"><span data-stu-id="978bb-227">NAME</span></span>                                                                          | <span data-ttu-id="978bb-228">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="978bb-228">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="978bb-229">ECORESSIZE</span><span class="sxs-lookup"><span data-stu-id="978bb-229">ECORESSIZE</span></span>                    | <span data-ttu-id="978bb-230">氏名</span><span class="sxs-lookup"><span data-stu-id="978bb-230">NAME</span></span>                                                                          | <span data-ttu-id="978bb-231">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="978bb-231">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="978bb-232">RETAILTABLEFIELDID</span><span class="sxs-lookup"><span data-stu-id="978bb-232">RETAILTABLEFIELDID</span></span>            | <span data-ttu-id="978bb-233">TABLENAME</span><span class="sxs-lookup"><span data-stu-id="978bb-233">TABLENAME</span></span>                                                                     | <span data-ttu-id="978bb-234">Nvarchar (81)</span><span class="sxs-lookup"><span data-stu-id="978bb-234">nvarchar(81)</span></span>  |                       |                                     |
|                               | <span data-ttu-id="978bb-235">FIELDNAME</span><span class="sxs-lookup"><span data-stu-id="978bb-235">FIELDNAME</span></span>                                                                     | <span data-ttu-id="978bb-236">Nvarchar (81)</span><span class="sxs-lookup"><span data-stu-id="978bb-236">nvarchar(81)</span></span>  |                       |                                     |
| <span data-ttu-id="978bb-237">RETAILTRANSACTIONTAXTRANSGTE</span><span class="sxs-lookup"><span data-stu-id="978bb-237">RETAILTRANSACTIONTAXTRANSGTE</span></span>  | <span data-ttu-id="978bb-238">TAXCOMPONENT</span><span class="sxs-lookup"><span data-stu-id="978bb-238">TAXCOMPONENT</span></span>                                                                  | <span data-ttu-id="978bb-239">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="978bb-239">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="978bb-240">TAXCOMPONENTTABLE\_IN</span><span class="sxs-lookup"><span data-stu-id="978bb-240">TAXCOMPONENTTABLE\_IN</span></span>         | <span data-ttu-id="978bb-241">COMPONENT</span><span class="sxs-lookup"><span data-stu-id="978bb-241">COMPONENT</span></span>                                                                     | <span data-ttu-id="978bb-242">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="978bb-242">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="978bb-243">WMSLOCATION</span><span class="sxs-lookup"><span data-stu-id="978bb-243">WMSLOCATION</span></span>                   | <span data-ttu-id="978bb-244">INPUTLOCATION</span><span class="sxs-lookup"><span data-stu-id="978bb-244">INPUTLOCATION</span></span>                                                                 | <span data-ttu-id="978bb-245">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="978bb-245">nvarchar(60)</span></span>  |                       |                                     |
|                               | <span data-ttu-id="978bb-246">WMSLOCATIONID</span><span class="sxs-lookup"><span data-stu-id="978bb-246">WMSLOCATIONID</span></span>                                                                 | <span data-ttu-id="978bb-247">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="978bb-247">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="978bb-248">INVENTLOCATION</span><span class="sxs-lookup"><span data-stu-id="978bb-248">INVENTLOCATION</span></span>                | <span data-ttu-id="978bb-249">RBODEFAULTWMSLOCATIONID</span><span class="sxs-lookup"><span data-stu-id="978bb-249">RBODEFAULTWMSLOCATIONID</span></span>                                                       | <span data-ttu-id="978bb-250">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="978bb-250">nvarchar(60)</span></span>  |                       |                                     |
|                               | <span data-ttu-id="978bb-251">WMSLOCATIONIDDEFAULTISSUE</span><span class="sxs-lookup"><span data-stu-id="978bb-251">WMSLOCATIONIDDEFAULTISSUE</span></span>                                                     | <span data-ttu-id="978bb-252">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="978bb-252">nvarchar(60)</span></span>  |                       |                                     |
|                               | <span data-ttu-id="978bb-253">WMSLOCATIONIDDEFAULTRECEIPT</span><span class="sxs-lookup"><span data-stu-id="978bb-253">WMSLOCATIONIDDEFAULTRECEIPT</span></span>                                                   | <span data-ttu-id="978bb-254">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="978bb-254">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="978bb-255">PRICEDISCTABLE</span><span class="sxs-lookup"><span data-stu-id="978bb-255">PRICEDISCTABLE</span></span>                | <span data-ttu-id="978bb-256">CONSTRAINT I\_137462222\_1904821809: { "action": "replace-line", "value": "CONSTRAINT \[I\_PRICEDISCTABLE\_RECID\] PRIMARY KEY CLUSTERED ( \[RECID\] ) "CONSTRAINT I\_PRICEDISCTABLE\_RECID": { "action": "remove-line" }</span><span class="sxs-lookup"><span data-stu-id="978bb-256">CONSTRAINT I\_137462222\_1904821809: { "action": "replace-line", "value": "CONSTRAINT \[I\_PRICEDISCTABLE\_RECID\] PRIMARY KEY CLUSTERED ( \[RECID\] ) "CONSTRAINT I\_PRICEDISCTABLE\_RECID": { "action": "remove-line" }</span></span> |               |                       |                                     |
| <span data-ttu-id="978bb-257">OMOPERATINGUNIT</span><span class="sxs-lookup"><span data-stu-id="978bb-257">OMOPERATINGUNIT</span></span>               | <span data-ttu-id="978bb-258">OMOPERATINGUNITNUMBER</span><span class="sxs-lookup"><span data-stu-id="978bb-258">OMOPERATINGUNITNUMBER</span></span>                                                         | <span data-ttu-id="978bb-259">Nvarchar (30)</span><span class="sxs-lookup"><span data-stu-id="978bb-259">nvarchar(30)</span></span>  |                       |                                     |
| <span data-ttu-id="978bb-260">RETAILPARAMETERS</span><span class="sxs-lookup"><span data-stu-id="978bb-260">RETAILPARAMETERS</span></span>              | <span data-ttu-id="978bb-261">USEADVANCEDAUTOCHARGE INT NULL DEFAULT(0)</span><span class="sxs-lookup"><span data-stu-id="978bb-261">USEADVANCEDAUTOCHARGE INT NULL DEFAULT(0)</span></span>                                     |               |                       |                                     |
|                               | <span data-ttu-id="978bb-262">GIFTCARDINQUIRYPRINTHISTORY INT NULL DEFAULT(0)</span><span class="sxs-lookup"><span data-stu-id="978bb-262">GIFTCARDINQUIRYPRINTHISTORY INT NULL DEFAULT(0)</span></span>                               |               |                       |                                     |
| <span data-ttu-id="978bb-263">RETAILINFOCODETABLE</span><span class="sxs-lookup"><span data-stu-id="978bb-263">RETAILINFOCODETABLE</span></span>           | <span data-ttu-id="978bb-264">PRINTINPUTONFISCALRECEIPT \[int\] NULL DEFAULT (0) PRINTTEXTONFISCALRECEIPT \[nvarchar\] (50) NULL DEFAULT('')</span><span class="sxs-lookup"><span data-stu-id="978bb-264">PRINTINPUTONFISCALRECEIPT \[int\] NULL DEFAULT (0) PRINTTEXTONFISCALRECEIPT \[nvarchar\] (50) NULL DEFAULT('')</span></span> |               |                       |                                     |
| <span data-ttu-id="978bb-265">RETAILINFORMATIONSUBCODETABLE</span><span class="sxs-lookup"><span data-stu-id="978bb-265">RETAILINFORMATIONSUBCODETABLE</span></span> | <span data-ttu-id="978bb-266">PRINTTEXTONFISCALRECEIPT \[nvarchar\](50) NULL DEFAULT('')</span><span class="sxs-lookup"><span data-stu-id="978bb-266">PRINTTEXTONFISCALRECEIPT \[nvarchar\](50) NULL DEFAULT('')</span></span>                    |               |                       |                                     |
