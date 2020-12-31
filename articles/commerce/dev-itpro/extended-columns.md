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
# <a name="pre-extended-columns-in-the-channel-database"></a><span data-ttu-id="22d53-103">チャネル データベースの事前拡張された列</span><span class="sxs-lookup"><span data-stu-id="22d53-103">Pre-extended columns in the channel database</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="22d53-104">チャネル データベース内の一部の列は、*事前拡張* されています。</span><span class="sxs-lookup"><span data-stu-id="22d53-104">Some columns in the channel database are *pre-extended*.</span></span> <span data-ttu-id="22d53-105">つまり、チャンネルデータベースの列の長さが Microsoft Dynamics 365 Commerce 本体が規定する列の長さを超えています。</span><span class="sxs-lookup"><span data-stu-id="22d53-105">In other words, the column length in the channel database exceeds the column length in Microsoft Dynamics 365 Commerce Headquarters.</span></span> <span data-ttu-id="22d53-106">たとえば、**INVENTSERIALID** フィールドの長さは、Commerce 本体のデータベースでは 20 文字、チャネル データベースでは 50 文字です。</span><span class="sxs-lookup"><span data-stu-id="22d53-106">For example, the length of the **INVENTSERIALID** field is 20 characters in the Commerce Headquarters database but 50 characters in the channel database.</span></span>

<span data-ttu-id="22d53-107">チャネル データベースのフィールドは拡張されることは多いですが、フィールドの列の長さは拡張に対応していません。</span><span class="sxs-lookup"><span data-stu-id="22d53-107">Although fields in the channel database are often extended, column lengths for those fields aren't extensible.</span></span> <span data-ttu-id="22d53-108">したがって、拡張が必要となった場合にも対応できるよう、標準で列の長さが増設されています。</span><span class="sxs-lookup"><span data-stu-id="22d53-108">Therefore, out-of-box column lengths have been increased to support extension scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="22d53-109">事前拡張されていないフィールドを拡張する必要がある場合は、Lifecycle Services (LCS) で拡張リクエストを提出する必要があります。</span><span class="sxs-lookup"><span data-stu-id="22d53-109">If you must extend a field that isn't already pre-extended, you must file an extension request in Lifecycle Services (LCS).</span></span> <span data-ttu-id="22d53-110">詳細については、[拡張性要求](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/extensibility/extensibility-requests) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="22d53-110">For more information, see [Extensibility requests](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/extensibility/extensibility-requests).</span></span>

<span data-ttu-id="22d53-111">このフィールドは、チャネル データベースで拡張されますが、拡張データ型 (EDT) の拡張モデルを使用して、Commerce 本体のデータベースのフィールドも拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="22d53-111">Although the fields are extended in the channel database, your extension must also extend the field in the Commerce Headquarters database by using the extended data type (EDT) extension model.</span></span> <span data-ttu-id="22d53-112">さらに、これに対応する販売時点管理 (POS) 、または Commerce Runtime (CRT) ユーザー インターフェイス (UI) を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="22d53-112">Additionally, you must extend the corresponding point of sale (POS) or Commerce runtime (CRT) user interface (UI).</span></span>

<span data-ttu-id="22d53-113">Commerce 本体のデータベースが拡張されていない場合は、チャネル データベースと Commerce 本体のデータベース間の同期が、P-ジョブの実行中に失敗するか、または余分な文字が切り捨てられます。</span><span class="sxs-lookup"><span data-stu-id="22d53-113">If the Commerce Headquarters database isn't extended, either synchronization between the channel database and the Commerce Headquarters database will fail during the P-job or the extra characters will be truncated.</span></span> <span data-ttu-id="22d53-114">同様に、対応する販売時点管理 (POS) ユーザー インターフェイス (UI) または Commerce Runtime (CRT) が拡張されていない場合は、検証をすることで既定の文字長を超える文字の入力を防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="22d53-114">Likewise, if the corresponding point of sale (POS) user interface (UI) or the Commerce runtime (CRT) isn't extended, validation will prevent more than the default character length from being entered.</span></span> <span data-ttu-id="22d53-115">既定の長さは、Commerce 本体のデータベースにおける "基準" 列の長さによって決まります。</span><span class="sxs-lookup"><span data-stu-id="22d53-115">The default length is determined by the base column length in the Commerce Headquarters database.</span></span>

<span data-ttu-id="22d53-116">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="22d53-116">Here are some examples:</span></span>

- <span data-ttu-id="22d53-117">チャネル データベースの **INVENTSERIALID** フィールドの長さは 50 文字ですが、POS UI では最大で 20 文字までのシリアル番号が入力できます。</span><span class="sxs-lookup"><span data-stu-id="22d53-117">The length of the **INVENTSERIALID** field in the channel database is 50 characters, but the POS UI accepts serial numbers that are a maximum of only 20 characters long.</span></span> <span data-ttu-id="22d53-118">この場合は、POS UI と Commerce 本体のデータベースの両方のフィールドを拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="22d53-118">In this case, you must extend the field in both the POS UI and the Commerce Headquarters database.</span></span>
- <span data-ttu-id="22d53-119">チャネルデータベースの **番地** フィールドの長さは、400文字まで拡張されますが、CRT の検証では Commerce 本体のデータベースの既定の長さを超えることは認められません。</span><span class="sxs-lookup"><span data-stu-id="22d53-119">The length of the **STREET** field in the channel database is extended to 400 characters, but validation in CRT prevents more than the default length in the Commerce Headquarters database from being accepted.</span></span> <span data-ttu-id="22d53-120">この場合は、CRT 要求ハンドラー (**ValidateAddressLengthServiceRequest**) と Commerce 本体のデータベースの両方を拡張して、**番地** フィールドで 400 文字を使用できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="22d53-120">In this case, you must extend both the CRT request handler (**ValidateAddressLengthServiceRequest**) and the Commerce Headquarters database, so that 400 characters are accepted for the **STREET** field.</span></span>

<span data-ttu-id="22d53-121">一部のフィールドは、POS 内の読み取り専用フィールドである可能性があるため、POS UI または CRT ハンドラーの拡張は不要です。</span><span class="sxs-lookup"><span data-stu-id="22d53-121">Extension of the POS UI or CRT handlers isn't required for some fields, because they might be read-only fields in POS.</span></span> <span data-ttu-id="22d53-122">たとえば、**ECORES** 製品に関連するフィールドは読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="22d53-122">For example, **ECORES** product-related fields are read-only.</span></span> <span data-ttu-id="22d53-123">POS では製品の作成に対応していないため、POS では製品の書き込みシナリオが存在しません。</span><span class="sxs-lookup"><span data-stu-id="22d53-123">Because product creation isn't supported in POS, there is no write scenario for products in POS.</span></span>

## <a name="sample-code-to-override-the-validateaddresslengthservicerequest-handler"></a><span data-ttu-id="22d53-124">ValidateAddressLengthServiceRequest ハンドラーをオーバーライドするサンプルコード</span><span class="sxs-lookup"><span data-stu-id="22d53-124">Sample code to override the ValidateAddressLengthServiceRequest handler</span></span>

<span data-ttu-id="22d53-125">次の例では、**ValidateAddressLengthServiceRequest** を上書きする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="22d53-125">The following example shows how to override the **ValidateAddressLengthServiceRequest** handler.</span></span>

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

## <a name="pre-extended-columns-in-the-channel-database"></a><span data-ttu-id="22d53-126">チャネル データベースの事前拡張された列</span><span class="sxs-lookup"><span data-stu-id="22d53-126">Pre-extended columns in the channel database</span></span>

<span data-ttu-id="22d53-127">次の表に、事前拡張されている列の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="22d53-127">The following table lists the columns that are pre-extended.</span></span>

| <span data-ttu-id="22d53-128">テーブル</span><span class="sxs-lookup"><span data-stu-id="22d53-128">Table</span></span>                         | <span data-ttu-id="22d53-129">円柱</span><span class="sxs-lookup"><span data-stu-id="22d53-129">Column</span></span>                                                                        | <span data-ttu-id="22d53-130">期間</span><span class="sxs-lookup"><span data-stu-id="22d53-130">Length</span></span>        | <span data-ttu-id="22d53-131">CRT の拡張機能</span><span class="sxs-lookup"><span data-stu-id="22d53-131">Extension in CRT</span></span>      | <span data-ttu-id="22d53-132">POS の拡張機能</span><span class="sxs-lookup"><span data-stu-id="22d53-132">Extension in POS</span></span>                    |
|-------------------------------|-------------------------------------------------------------------------------|---------------|-----------------------|-------------------------------------|
| <span data-ttu-id="22d53-133">INVENTSERIAL</span><span class="sxs-lookup"><span data-stu-id="22d53-133">INVENTSERIAL</span></span>                  | <span data-ttu-id="22d53-134">INVENTSERIALID</span><span class="sxs-lookup"><span data-stu-id="22d53-134">INVENTSERIALID</span></span>                                                                | <span data-ttu-id="22d53-135">Nvarchar (50)</span><span class="sxs-lookup"><span data-stu-id="22d53-135">nvarchar(50)</span></span>  |                       | <span data-ttu-id="22d53-136">GetSerialNumberClientRequestHandler</span><span class="sxs-lookup"><span data-stu-id="22d53-136">GetSerialNumberClientRequestHandler</span></span> |
| <span data-ttu-id="22d53-137">LOGISTICSPOSTALADDRESS</span><span class="sxs-lookup"><span data-stu-id="22d53-137">LOGISTICSPOSTALADDRESS</span></span>        | <span data-ttu-id="22d53-138">住所</span><span class="sxs-lookup"><span data-stu-id="22d53-138">ADDRESS</span></span>                                                                       | <span data-ttu-id="22d53-139">Nvarchar (500)</span><span class="sxs-lookup"><span data-stu-id="22d53-139">nvarchar(500)</span></span> | <span data-ttu-id="22d53-140">ValidateAddressLength</span><span class="sxs-lookup"><span data-stu-id="22d53-140">ValidateAddressLength</span></span> |                                     |
| <span data-ttu-id="22d53-141">LOGISTICSPOSTALADDRESS</span><span class="sxs-lookup"><span data-stu-id="22d53-141">LOGISTICSPOSTALADDRESS</span></span>        | <span data-ttu-id="22d53-142">STREET</span><span class="sxs-lookup"><span data-stu-id="22d53-142">STREET</span></span>                                                                        | <span data-ttu-id="22d53-143">Nvarchar (400)</span><span class="sxs-lookup"><span data-stu-id="22d53-143">nvarchar(400)</span></span> | <span data-ttu-id="22d53-144">ValidateAddressLength</span><span class="sxs-lookup"><span data-stu-id="22d53-144">ValidateAddressLength</span></span> |                                     |
| <span data-ttu-id="22d53-145">LOGISTICSPOSTALADDRESS</span><span class="sxs-lookup"><span data-stu-id="22d53-145">LOGISTICSPOSTALADDRESS</span></span>        | <span data-ttu-id="22d53-146">COUNTY</span><span class="sxs-lookup"><span data-stu-id="22d53-146">COUNTY</span></span>                                                                        | <span data-ttu-id="22d53-147">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="22d53-147">nvarchar(60)</span></span>  | <span data-ttu-id="22d53-148">ValidateAddressLength</span><span class="sxs-lookup"><span data-stu-id="22d53-148">ValidateAddressLength</span></span> |                                     |
| <span data-ttu-id="22d53-149">LOGISTICSADDRESSCITY</span><span class="sxs-lookup"><span data-stu-id="22d53-149">LOGISTICSADDRESSCITY</span></span>          | <span data-ttu-id="22d53-150">COUNTYID</span><span class="sxs-lookup"><span data-stu-id="22d53-150">COUNTYID</span></span>                                                                      | <span data-ttu-id="22d53-151">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="22d53-151">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="22d53-152">LOGISTICSADDRESSCOUNTY</span><span class="sxs-lookup"><span data-stu-id="22d53-152">LOGISTICSADDRESSCOUNTY</span></span>        | <span data-ttu-id="22d53-153">COUNTYID</span><span class="sxs-lookup"><span data-stu-id="22d53-153">COUNTYID</span></span>                                                                      | <span data-ttu-id="22d53-154">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="22d53-154">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="22d53-155">LOGISTICSADDRESSDISTRICT</span><span class="sxs-lookup"><span data-stu-id="22d53-155">LOGISTICSADDRESSDISTRICT</span></span>      | <span data-ttu-id="22d53-156">COUNTYID\_RU</span><span class="sxs-lookup"><span data-stu-id="22d53-156">COUNTYID\_RU</span></span>                                                                  | <span data-ttu-id="22d53-157">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="22d53-157">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="22d53-158">LOGISTICSADDRESSZIPCODE</span><span class="sxs-lookup"><span data-stu-id="22d53-158">LOGISTICSADDRESSZIPCODE</span></span>       | <span data-ttu-id="22d53-159">STREETNAME</span><span class="sxs-lookup"><span data-stu-id="22d53-159">STREETNAME</span></span>                                                                    | <span data-ttu-id="22d53-160">Nvarchar (400)</span><span class="sxs-lookup"><span data-stu-id="22d53-160">nvarchar(400)</span></span> |                       |                                     |
| <span data-ttu-id="22d53-161">LOGISTICSADDRESSZIPCODE</span><span class="sxs-lookup"><span data-stu-id="22d53-161">LOGISTICSADDRESSZIPCODE</span></span>       | <span data-ttu-id="22d53-162">COUNTY</span><span class="sxs-lookup"><span data-stu-id="22d53-162">COUNTY</span></span>                                                                        | <span data-ttu-id="22d53-163">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="22d53-163">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="22d53-164">RETAILASYNCADDRESS</span><span class="sxs-lookup"><span data-stu-id="22d53-164">RETAILASYNCADDRESS</span></span>            | <span data-ttu-id="22d53-165">STREET</span><span class="sxs-lookup"><span data-stu-id="22d53-165">STREET</span></span>                                                                        | <span data-ttu-id="22d53-166">Nvarchar (400)</span><span class="sxs-lookup"><span data-stu-id="22d53-166">nvarchar(400)</span></span> |                       |                                     |
| <span data-ttu-id="22d53-167">RETAILASYNCADDRESS</span><span class="sxs-lookup"><span data-stu-id="22d53-167">RETAILASYNCADDRESS</span></span>            | <span data-ttu-id="22d53-168">COUNTY</span><span class="sxs-lookup"><span data-stu-id="22d53-168">COUNTY</span></span>                                                                        | <span data-ttu-id="22d53-169">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="22d53-169">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="22d53-170">RETAILASYNCCUSTOMER</span><span class="sxs-lookup"><span data-stu-id="22d53-170">RETAILASYNCCUSTOMER</span></span>           | <span data-ttu-id="22d53-171">STREET</span><span class="sxs-lookup"><span data-stu-id="22d53-171">STREET</span></span>                                                                        | <span data-ttu-id="22d53-172">Nvarchar (400)</span><span class="sxs-lookup"><span data-stu-id="22d53-172">nvarchar(400)</span></span> |                       |                                     |
| <span data-ttu-id="22d53-173">RETAILASYNCCUSTOMER</span><span class="sxs-lookup"><span data-stu-id="22d53-173">RETAILASYNCCUSTOMER</span></span>           | <span data-ttu-id="22d53-174">COUNTY</span><span class="sxs-lookup"><span data-stu-id="22d53-174">COUNTY</span></span>                                                                        | <span data-ttu-id="22d53-175">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="22d53-175">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="22d53-176">RETAILFISCALDOCUMENT\_BR</span><span class="sxs-lookup"><span data-stu-id="22d53-176">RETAILFISCALDOCUMENT\_BR</span></span>      | <span data-ttu-id="22d53-177">FEADDRESSSTREET</span><span class="sxs-lookup"><span data-stu-id="22d53-177">FEADDRESSSTREET</span></span>                                                               | <span data-ttu-id="22d53-178">Nvarchar (400)</span><span class="sxs-lookup"><span data-stu-id="22d53-178">nvarchar(400)</span></span> |                       |                                     |
| <span data-ttu-id="22d53-179">RETAILFISCALDOCUMENT\_BR</span><span class="sxs-lookup"><span data-stu-id="22d53-179">RETAILFISCALDOCUMENT\_BR</span></span>      | <span data-ttu-id="22d53-180">THIRDPARTYADDRESSSTREET</span><span class="sxs-lookup"><span data-stu-id="22d53-180">THIRDPARTYADDRESSSTREET</span></span>                                                       | <span data-ttu-id="22d53-181">Nvarchar (400)</span><span class="sxs-lookup"><span data-stu-id="22d53-181">nvarchar(400)</span></span> |                       |                                     |
| <span data-ttu-id="22d53-182">RETAILTAXFILTERS</span><span class="sxs-lookup"><span data-stu-id="22d53-182">RETAILTAXFILTERS</span></span>              | <span data-ttu-id="22d53-183">COUNTYID</span><span class="sxs-lookup"><span data-stu-id="22d53-183">COUNTYID</span></span>                                                                      | <span data-ttu-id="22d53-184">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="22d53-184">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="22d53-185">RETAILTRANSACTIONADDRESSTRANS</span><span class="sxs-lookup"><span data-stu-id="22d53-185">RETAILTRANSACTIONADDRESSTRANS</span></span> | <span data-ttu-id="22d53-186">STREET</span><span class="sxs-lookup"><span data-stu-id="22d53-186">STREET</span></span>                                                                        | <span data-ttu-id="22d53-187">Nvarchar (400)</span><span class="sxs-lookup"><span data-stu-id="22d53-187">nvarchar(400)</span></span> |                       |                                     |
| <span data-ttu-id="22d53-188">RETAILTRANSACTIONADDRESSTRANS</span><span class="sxs-lookup"><span data-stu-id="22d53-188">RETAILTRANSACTIONADDRESSTRANS</span></span> | <span data-ttu-id="22d53-189">COUNTY</span><span class="sxs-lookup"><span data-stu-id="22d53-189">COUNTY</span></span>                                                                        | <span data-ttu-id="22d53-190">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="22d53-190">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="22d53-191">RETAILTRANSACTIONSALESTRANS</span><span class="sxs-lookup"><span data-stu-id="22d53-191">RETAILTRANSACTIONSALESTRANS</span></span>   | <span data-ttu-id="22d53-192">INVENTBATCHID</span><span class="sxs-lookup"><span data-stu-id="22d53-192">INVENTBATCHID</span></span>                                                                 | <span data-ttu-id="22d53-193">Nvarchar (50)</span><span class="sxs-lookup"><span data-stu-id="22d53-193">nvarchar(50)</span></span>  |                       |                                     |
| <span data-ttu-id="22d53-194">RETAILTRANSACTIONSALESTRANS</span><span class="sxs-lookup"><span data-stu-id="22d53-194">RETAILTRANSACTIONSALESTRANS</span></span>   | <span data-ttu-id="22d53-195">INVENTSERIALID</span><span class="sxs-lookup"><span data-stu-id="22d53-195">INVENTSERIALID</span></span>                                                                | <span data-ttu-id="22d53-196">Nvarchar (50)</span><span class="sxs-lookup"><span data-stu-id="22d53-196">nvarchar(50)</span></span>  |                       |                                     |
| <span data-ttu-id="22d53-197">RETAILTRANSACTIONSALESTRANS</span><span class="sxs-lookup"><span data-stu-id="22d53-197">RETAILTRANSACTIONSALESTRANS</span></span>   | <span data-ttu-id="22d53-198">WAREHOUSELOCATION</span><span class="sxs-lookup"><span data-stu-id="22d53-198">WAREHOUSELOCATION</span></span>                                                             | <span data-ttu-id="22d53-199">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="22d53-199">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="22d53-200">INVENTDIM</span><span class="sxs-lookup"><span data-stu-id="22d53-200">INVENTDIM</span></span>                     | <span data-ttu-id="22d53-201">INVENTBATCHID</span><span class="sxs-lookup"><span data-stu-id="22d53-201">INVENTBATCHID</span></span>                                                                 | <span data-ttu-id="22d53-202">Nvarchar (50)</span><span class="sxs-lookup"><span data-stu-id="22d53-202">nvarchar(50)</span></span>  |                       |                                     |
| <span data-ttu-id="22d53-203">INVENTDIM</span><span class="sxs-lookup"><span data-stu-id="22d53-203">INVENTDIM</span></span>                     | <span data-ttu-id="22d53-204">INVENTSERIALID</span><span class="sxs-lookup"><span data-stu-id="22d53-204">INVENTSERIALID</span></span>                                                                | <span data-ttu-id="22d53-205">Nvarchar (50)</span><span class="sxs-lookup"><span data-stu-id="22d53-205">nvarchar(50)</span></span>  |                       |                                     |
| <span data-ttu-id="22d53-206">INVENTDIM</span><span class="sxs-lookup"><span data-stu-id="22d53-206">INVENTDIM</span></span>                     | <span data-ttu-id="22d53-207">CONFIGID</span><span class="sxs-lookup"><span data-stu-id="22d53-207">CONFIGID</span></span>                                                                      | <span data-ttu-id="22d53-208">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="22d53-208">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="22d53-209">INVENTDIM</span><span class="sxs-lookup"><span data-stu-id="22d53-209">INVENTDIM</span></span>                     | <span data-ttu-id="22d53-210">INVENTCOLORID</span><span class="sxs-lookup"><span data-stu-id="22d53-210">INVENTCOLORID</span></span>                                                                 | <span data-ttu-id="22d53-211">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="22d53-211">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="22d53-212">INVENTDIM</span><span class="sxs-lookup"><span data-stu-id="22d53-212">INVENTDIM</span></span>                     | <span data-ttu-id="22d53-213">INVENTSIZEID</span><span class="sxs-lookup"><span data-stu-id="22d53-213">INVENTSIZEID</span></span>                                                                  | <span data-ttu-id="22d53-214">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="22d53-214">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="22d53-215">INVENTDIM</span><span class="sxs-lookup"><span data-stu-id="22d53-215">INVENTDIM</span></span>                     | <span data-ttu-id="22d53-216">INVENTSTYLEID</span><span class="sxs-lookup"><span data-stu-id="22d53-216">INVENTSTYLEID</span></span>                                                                 | <span data-ttu-id="22d53-217">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="22d53-217">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="22d53-218">INVENTDIM</span><span class="sxs-lookup"><span data-stu-id="22d53-218">INVENTDIM</span></span>                     | <span data-ttu-id="22d53-219">WMSLOCATIONID</span><span class="sxs-lookup"><span data-stu-id="22d53-219">WMSLOCATIONID</span></span>                                                                 | <span data-ttu-id="22d53-220">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="22d53-220">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="22d53-221">ECORESCOLOR</span><span class="sxs-lookup"><span data-stu-id="22d53-221">ECORESCOLOR</span></span>                   | <span data-ttu-id="22d53-222">氏名</span><span class="sxs-lookup"><span data-stu-id="22d53-222">NAME</span></span>                                                                          | <span data-ttu-id="22d53-223">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="22d53-223">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="22d53-224">ECORESSTYLE</span><span class="sxs-lookup"><span data-stu-id="22d53-224">ECORESSTYLE</span></span>                   | <span data-ttu-id="22d53-225">氏名</span><span class="sxs-lookup"><span data-stu-id="22d53-225">NAME</span></span>                                                                          | <span data-ttu-id="22d53-226">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="22d53-226">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="22d53-227">ECORESCONFIGURATION</span><span class="sxs-lookup"><span data-stu-id="22d53-227">ECORESCONFIGURATION</span></span>           | <span data-ttu-id="22d53-228">氏名</span><span class="sxs-lookup"><span data-stu-id="22d53-228">NAME</span></span>                                                                          | <span data-ttu-id="22d53-229">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="22d53-229">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="22d53-230">ECORESSIZE</span><span class="sxs-lookup"><span data-stu-id="22d53-230">ECORESSIZE</span></span>                    | <span data-ttu-id="22d53-231">氏名</span><span class="sxs-lookup"><span data-stu-id="22d53-231">NAME</span></span>                                                                          | <span data-ttu-id="22d53-232">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="22d53-232">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="22d53-233">RETAILTABLEFIELDID</span><span class="sxs-lookup"><span data-stu-id="22d53-233">RETAILTABLEFIELDID</span></span>            | <span data-ttu-id="22d53-234">TABLENAME</span><span class="sxs-lookup"><span data-stu-id="22d53-234">TABLENAME</span></span>                                                                     | <span data-ttu-id="22d53-235">Nvarchar (81)</span><span class="sxs-lookup"><span data-stu-id="22d53-235">nvarchar(81)</span></span>  |                       |                                     |
|                               | <span data-ttu-id="22d53-236">FIELDNAME</span><span class="sxs-lookup"><span data-stu-id="22d53-236">FIELDNAME</span></span>                                                                     | <span data-ttu-id="22d53-237">Nvarchar (81)</span><span class="sxs-lookup"><span data-stu-id="22d53-237">nvarchar(81)</span></span>  |                       |                                     |
| <span data-ttu-id="22d53-238">RETAILTRANSACTIONTAXTRANSGTE</span><span class="sxs-lookup"><span data-stu-id="22d53-238">RETAILTRANSACTIONTAXTRANSGTE</span></span>  | <span data-ttu-id="22d53-239">TAXCOMPONENT</span><span class="sxs-lookup"><span data-stu-id="22d53-239">TAXCOMPONENT</span></span>                                                                  | <span data-ttu-id="22d53-240">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="22d53-240">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="22d53-241">TAXCOMPONENTTABLE\_IN</span><span class="sxs-lookup"><span data-stu-id="22d53-241">TAXCOMPONENTTABLE\_IN</span></span>         | <span data-ttu-id="22d53-242">COMPONENT</span><span class="sxs-lookup"><span data-stu-id="22d53-242">COMPONENT</span></span>                                                                     | <span data-ttu-id="22d53-243">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="22d53-243">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="22d53-244">WMSLOCATION</span><span class="sxs-lookup"><span data-stu-id="22d53-244">WMSLOCATION</span></span>                   | <span data-ttu-id="22d53-245">INPUTLOCATION</span><span class="sxs-lookup"><span data-stu-id="22d53-245">INPUTLOCATION</span></span>                                                                 | <span data-ttu-id="22d53-246">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="22d53-246">nvarchar(60)</span></span>  |                       |                                     |
|                               | <span data-ttu-id="22d53-247">WMSLOCATIONID</span><span class="sxs-lookup"><span data-stu-id="22d53-247">WMSLOCATIONID</span></span>                                                                 | <span data-ttu-id="22d53-248">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="22d53-248">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="22d53-249">INVENTLOCATION</span><span class="sxs-lookup"><span data-stu-id="22d53-249">INVENTLOCATION</span></span>                | <span data-ttu-id="22d53-250">RBODEFAULTWMSLOCATIONID</span><span class="sxs-lookup"><span data-stu-id="22d53-250">RBODEFAULTWMSLOCATIONID</span></span>                                                       | <span data-ttu-id="22d53-251">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="22d53-251">nvarchar(60)</span></span>  |                       |                                     |
|                               | <span data-ttu-id="22d53-252">WMSLOCATIONIDDEFAULTISSUE</span><span class="sxs-lookup"><span data-stu-id="22d53-252">WMSLOCATIONIDDEFAULTISSUE</span></span>                                                     | <span data-ttu-id="22d53-253">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="22d53-253">nvarchar(60)</span></span>  |                       |                                     |
|                               | <span data-ttu-id="22d53-254">WMSLOCATIONIDDEFAULTRECEIPT</span><span class="sxs-lookup"><span data-stu-id="22d53-254">WMSLOCATIONIDDEFAULTRECEIPT</span></span>                                                   | <span data-ttu-id="22d53-255">Nvarchar (60)</span><span class="sxs-lookup"><span data-stu-id="22d53-255">nvarchar(60)</span></span>  |                       |                                     |
| <span data-ttu-id="22d53-256">PRICEDISCTABLE</span><span class="sxs-lookup"><span data-stu-id="22d53-256">PRICEDISCTABLE</span></span>                | <span data-ttu-id="22d53-257">CONSTRAINT I\_137462222\_1904821809: { "action": "replace-line", "value": "CONSTRAINT \[I\_PRICEDISCTABLE\_RECID\] PRIMARY KEY CLUSTERED ( \[RECID\] ) "CONSTRAINT I\_PRICEDISCTABLE\_RECID": { "action": "remove-line" }</span><span class="sxs-lookup"><span data-stu-id="22d53-257">CONSTRAINT I\_137462222\_1904821809: { "action": "replace-line", "value": "CONSTRAINT \[I\_PRICEDISCTABLE\_RECID\] PRIMARY KEY CLUSTERED ( \[RECID\] ) "CONSTRAINT I\_PRICEDISCTABLE\_RECID": { "action": "remove-line" }</span></span> |               |                       |                                     |
| <span data-ttu-id="22d53-258">OMOPERATINGUNIT</span><span class="sxs-lookup"><span data-stu-id="22d53-258">OMOPERATINGUNIT</span></span>               | <span data-ttu-id="22d53-259">OMOPERATINGUNITNUMBER</span><span class="sxs-lookup"><span data-stu-id="22d53-259">OMOPERATINGUNITNUMBER</span></span>                                                         | <span data-ttu-id="22d53-260">Nvarchar (30)</span><span class="sxs-lookup"><span data-stu-id="22d53-260">nvarchar(30)</span></span>  |                       |                                     |
| <span data-ttu-id="22d53-261">RETAILPARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22d53-261">RETAILPARAMETERS</span></span>              | <span data-ttu-id="22d53-262">USEADVANCEDAUTOCHARGE INT NULL DEFAULT(0)</span><span class="sxs-lookup"><span data-stu-id="22d53-262">USEADVANCEDAUTOCHARGE INT NULL DEFAULT(0)</span></span>                                     |               |                       |                                     |
|                               | <span data-ttu-id="22d53-263">GIFTCARDINQUIRYPRINTHISTORY INT NULL DEFAULT(0)</span><span class="sxs-lookup"><span data-stu-id="22d53-263">GIFTCARDINQUIRYPRINTHISTORY INT NULL DEFAULT(0)</span></span>                               |               |                       |                                     |
| <span data-ttu-id="22d53-264">RETAILINFOCODETABLE</span><span class="sxs-lookup"><span data-stu-id="22d53-264">RETAILINFOCODETABLE</span></span>           | <span data-ttu-id="22d53-265">PRINTINPUTONFISCALRECEIPT \[int\] NULL DEFAULT (0) PRINTTEXTONFISCALRECEIPT \[nvarchar\] (50) NULL DEFAULT('')</span><span class="sxs-lookup"><span data-stu-id="22d53-265">PRINTINPUTONFISCALRECEIPT \[int\] NULL DEFAULT (0) PRINTTEXTONFISCALRECEIPT \[nvarchar\] (50) NULL DEFAULT('')</span></span> |               |                       |                                     |
| <span data-ttu-id="22d53-266">RETAILINFORMATIONSUBCODETABLE</span><span class="sxs-lookup"><span data-stu-id="22d53-266">RETAILINFORMATIONSUBCODETABLE</span></span> | <span data-ttu-id="22d53-267">PRINTTEXTONFISCALRECEIPT \[nvarchar\](50) NULL DEFAULT('')</span><span class="sxs-lookup"><span data-stu-id="22d53-267">PRINTTEXTONFISCALRECEIPT \[nvarchar\](50) NULL DEFAULT('')</span></span>                    |               |                       |                                     |
