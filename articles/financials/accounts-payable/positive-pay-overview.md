---
title: 確認後支払の概要
description: この記事は確認後支払についての情報を提供し、銀行に提出する小切手の電子リストを生成するのに使用されます。
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankPositivePaySummary
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 88463
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 2ba23cf5afe9f007f5e32a75e918595929ad79a1
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834612"
---
# <a name="positive-pay-overview"></a><span data-ttu-id="52772-103">確認後支払の概要</span><span class="sxs-lookup"><span data-stu-id="52772-103">Positive pay overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="52772-104">この記事は確認後支払についての情報を提供し、銀行に提出する小切手の電子リストを生成するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="52772-104">This article provides information about positive pay, which is used to generate an electronic list of checks that can be presented to a bank.</span></span> 

<span data-ttu-id="52772-105">確認後支払を使用し、銀行に渡す小切手の電子リストを生成します。</span><span class="sxs-lookup"><span data-stu-id="52772-105">Positive pay is used to generate an electronic list of checks that can be presented to a bank.</span></span> <span data-ttu-id="52772-106">確認後支払ファイルは、銀行が小切手の不正を禁止するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="52772-106">Positive pay files can help banks prevent check fraud.</span></span> <span data-ttu-id="52772-107">小切手が印刷されるたびに、小切手の電子リストを生成するための確認後支払を設定します。</span><span class="sxs-lookup"><span data-stu-id="52772-107">You set up positive pay to generate an electronic list of checks every time that checks are printed.</span></span> <span data-ttu-id="52772-108">小切手が銀行に提出されるとき、銀行はその小切手を事前に提出された小切手のリストと比較します。</span><span class="sxs-lookup"><span data-stu-id="52772-108">Then, when a check is presented to the bank, the bank compares the check with the list of checks that you previously submitted.</span></span> <span data-ttu-id="52772-109">小切手がリストの小切手と一致する場合、銀行は小切手を決済します。</span><span class="sxs-lookup"><span data-stu-id="52772-109">If the check matches a check in the list, the bank clears it.</span></span> <span data-ttu-id="52772-110">小切手がリスト内の小切手と一致しない場合、銀行は確認のために小切手を保留にします。</span><span class="sxs-lookup"><span data-stu-id="52772-110">If the check doesn't match a check in the list, the bank holds it for review.</span></span>

<span data-ttu-id="52772-111">確認後支払は SafePay とも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="52772-111">Positive pay is also known as SafePay.</span></span> 

<span data-ttu-id="52772-112">確認後支払ファイルには、受取人と小切手金額に関する機密情報が含まれている場合があります。</span><span class="sxs-lookup"><span data-stu-id="52772-112">Positive pay files can contain sensitive information about payees and check amounts.</span></span> <span data-ttu-id="52772-113">したがって、ファイルを生成時から銀行がそのファイルを受領するまで、適切なセキュリティ対策をかならず使用します。</span><span class="sxs-lookup"><span data-stu-id="52772-113">Therefore, make sure that you use appropriate security measures from the time that the files are generated until they are received by the bank.</span></span> <span data-ttu-id="52772-114">確認後支払ファイルは、Web ブラウザのダウンロードの手順に従ってダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="52772-114">Positive pay files are downloaded according to the download instructions for the web browser.</span></span> 

<span data-ttu-id="52772-115">確認後支払ファイルは、データ エンティティを使用して作成されます。</span><span class="sxs-lookup"><span data-stu-id="52772-115">Positive pay files are created by using data entities.</span></span> <span data-ttu-id="52772-116">確認後支払ファイルを生成する前に、銀行が実行できる形式にデータを変換する XML の変換形式を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="52772-116">Before you generate a positive pay file, you must set up the transformation formats for the XML that translates the data into a format that the bank can consume.</span></span> 

<span data-ttu-id="52772-117">確認後支払情報を生成する銀行口座ごとに、確認後支払形式を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="52772-117">For each bank account that you want to generate positive pay information for, you must assign the positive pay format.</span></span> <span data-ttu-id="52772-118">確認後支払ファイルを生成した後に、一つの法人と一つの銀行口座に対する確認後支払ファイルを生成できます。</span><span class="sxs-lookup"><span data-stu-id="52772-118">After you generate payments, you can generate a positive pay file for a single legal entity and a single bank account.</span></span> <span data-ttu-id="52772-119">また、複数の法人と銀行口座の確認後支払ファイルを同時に生成することもできます。</span><span class="sxs-lookup"><span data-stu-id="52772-119">Alternatively, you can generate positive pay files for multiple legal entities and bank accounts at the same time.</span></span> 

<span data-ttu-id="52772-120">確認後支払ファイルに記載されている小切手が支払われた後、銀行から確認番号を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="52772-120">After the checks that are listed in a positive pay file have been paid, you receive a confirmation number from your bank.</span></span> <span data-ttu-id="52772-121">その後、Microsoft Dynamics 365 for Finance and Operations で確認後支払ファイルを確認できます。</span><span class="sxs-lookup"><span data-stu-id="52772-121">You can then confirm the positive pay file in Microsoft Dynamics 365 for Finance and Operations.</span></span> 

<span data-ttu-id="52772-122">確認後支払ファイルを変更する必要がある場合は、それを取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="52772-122">If you must change a positive pay file, you can recall it.</span></span> <span data-ttu-id="52772-123">その後、確認後支払ファイルの小切手ごとに、小切手が確認後支払ファイルに含まれているかどうかを示すフィールドがリセットされます。</span><span class="sxs-lookup"><span data-stu-id="52772-123">Then, for each check in the positive pay file, the field that indicates whether that check has been included in a positive pay file is reset.</span></span>

<span data-ttu-id="52772-124">詳細については、「[確認後支払ファイルの設定と生成](set-up-generate-positive-pay-files.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="52772-124">For more information, see [Set up and generate positive pay files](set-up-generate-positive-pay-files.md).</span></span>



