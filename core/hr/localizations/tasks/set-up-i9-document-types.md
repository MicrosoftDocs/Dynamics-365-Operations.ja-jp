--- 
title: "I-9 ドキュメント タイプの設定"
description: "この手順では、I-9 の検証に使用するドキュメント タイプを表示および設定する方法を示します。"
author: ShielaSogge
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 3b0e7f09994367f5683ed5c6d1f3b3ba3d550cc7
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-i-9-document-types"></a><span data-ttu-id="785cc-103">I-9 ドキュメント タイプの設定</span><span class="sxs-lookup"><span data-stu-id="785cc-103">Set up I-9 document types</span></span>

[!include[task guide banner](../../../includes/task-guide-banner.md)]

<span data-ttu-id="785cc-104">この手順では、I-9 の検証に使用するドキュメント タイプを表示および設定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="785cc-104">This procedure shows how to view and set up document types that are used for I-9 verification.</span></span> <span data-ttu-id="785cc-105">I-9 ドキュメント タイプを設定する前に、発行機関と ID タイプも設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="785cc-105">Before you set up I-9 document types, you must also set up the issuing agencies and identification types.</span></span> <span data-ttu-id="785cc-106">この手順を作成するために使用するデモ データの会社は USMF です。ここには、手順を完了するために必要な発行機関および ID タイプの例が含まれます。</span><span class="sxs-lookup"><span data-stu-id="785cc-106">The demo data company used to create this procedure is USMF, which includes examples of the issue agencies and identification types that are needed to complete the procedure.</span></span>

1. <span data-ttu-id="785cc-107">[人事管理] > [作業者] > [I-9] > [I-9 ドキュメント タイプ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="785cc-107">Go to Human resources > Workers > I-9 > I-9 document types.</span></span>
2. <span data-ttu-id="785cc-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="785cc-108">Click New.</span></span>
3. <span data-ttu-id="785cc-109">[I-9 ドキュメント タイプ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="785cc-109">In the I-9 document type field, type a value.</span></span>
    * <span data-ttu-id="785cc-110">例: 学歴 ID。</span><span class="sxs-lookup"><span data-stu-id="785cc-110">Example: School ID.</span></span>  
4. <span data-ttu-id="785cc-111">ID のタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="785cc-111">Select the identification type.</span></span>  <span data-ttu-id="785cc-112">例: 学歴 ID</span><span class="sxs-lookup"><span data-stu-id="785cc-112">Example:  School ID</span></span>
    * <span data-ttu-id="785cc-113">ID タイプの例には、社会保障番号 (SSN)、ビザ番号、パスポート ID、または運転免許証があります。</span><span class="sxs-lookup"><span data-stu-id="785cc-113">Examples of identification types include a Social Security number (SSN), visa number, passport ID, or driver's licence.</span></span>  
5. <span data-ttu-id="785cc-114">ドキュメント タイプに使用される I-9 ドキュメントの一覧を選択します。</span><span class="sxs-lookup"><span data-stu-id="785cc-114">Select the I-9 document list that is used for the document type.</span></span>
    * <span data-ttu-id="785cc-115">I-9 プロセスの一部として、従業員が身分証明および労働許可証を雇用主に示すドキュメントを提出する必要があります。</span><span class="sxs-lookup"><span data-stu-id="785cc-115">As part of the I-9 process, employees must present documentation that shows the employer their identity and employment authorization.</span></span> <span data-ttu-id="785cc-116">米国市民権移民局サービス (US Citizenship and Immigration Services) Web サイトには、受入可能なドキュメントに関する情報、およびドキュメントが属するリストの情報があります。</span><span class="sxs-lookup"><span data-stu-id="785cc-116">The US Citizenship and Immigration Services website contains information about which documents are acceptable, and which list they belong to.</span></span>  <span data-ttu-id="785cc-117">http://www.uscis.gov</span><span class="sxs-lookup"><span data-stu-id="785cc-117">http://www.uscis.gov</span></span>  
6. <span data-ttu-id="785cc-118">[フォーム] フィールドに、ドキュメント タイプの正式なフォーム番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="785cc-118">In the Form field, Enter the official form number for the document type.</span></span> <span data-ttu-id="785cc-119">例: 学歴 ID。</span><span class="sxs-lookup"><span data-stu-id="785cc-119">Example: School ID.</span></span>
    * <span data-ttu-id="785cc-120">公式のフォーム番号は、米国市民権移民局サービス (US Citizenship and Immigration Services) Web サイトで表示できます。</span><span class="sxs-lookup"><span data-stu-id="785cc-120">The official form numbers can be found on the US Citizenship and Immigration Services website.</span></span>  <span data-ttu-id="785cc-121">http://www.uscis.gov</span><span class="sxs-lookup"><span data-stu-id="785cc-121">http://www.uscis.gov</span></span>  
7. <span data-ttu-id="785cc-122">[有効] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="785cc-122">Check or uncheck the Active checkbox.</span></span>
8. <span data-ttu-id="785cc-123">[期限切れ] フィールドで、日付を 2019 年 10 月 27 日に設定します。</span><span class="sxs-lookup"><span data-stu-id="785cc-123">In the Expire field, set the date to '2019-10-27'.</span></span>
    * <span data-ttu-id="785cc-124">有効期限はオプションです。</span><span class="sxs-lookup"><span data-stu-id="785cc-124">The expiration date is optional.</span></span>  
9. <span data-ttu-id="785cc-125">ドキュメント タイプを発行した機関を選択します。</span><span class="sxs-lookup"><span data-stu-id="785cc-125">Select the agency that issued the document type.</span></span> <span data-ttu-id="785cc-126">例: 都道府県 / 担当地域</span><span class="sxs-lookup"><span data-stu-id="785cc-126">Example: Province/territory</span></span>
10. <span data-ttu-id="785cc-127">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="785cc-127">Click Save.</span></span>


