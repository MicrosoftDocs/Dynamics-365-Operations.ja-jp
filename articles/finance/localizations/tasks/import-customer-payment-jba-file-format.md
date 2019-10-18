---
title: JBA のファイル形式の顧客支払のインポート
description: 日本では一般的に、銀行間の電子資金決済 (EFT) には全国銀行協会 (JBA) のファイル形式が使用されています。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, SrsReportViewerForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cf288eb46d07f38c4e882721a9b5e5fe8539f69f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174664"
---
# <a name="import-customer-payment-with-jba-file-format"></a><span data-ttu-id="07b49-103">JBA のファイル形式の顧客支払のインポート</span><span class="sxs-lookup"><span data-stu-id="07b49-103">Import customer payment with JBA file format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="07b49-104">日本では一般的に、銀行間の電子資金決済 (EFT) には全国銀行協会 (JBA) のファイル形式が使用されています。</span><span class="sxs-lookup"><span data-stu-id="07b49-104">In Japan, the Japanese Bankers Association (JBA) file format is commonly used for Electronic Fund Transfer (EFT) among banks.</span></span> 



<span data-ttu-id="07b49-105">このタスクは、JBA 形式での EFT ファイルのインポートについて説明します。</span><span class="sxs-lookup"><span data-stu-id="07b49-105">This task walks you through importing an EFT file with a JBA format.</span></span>



<span data-ttu-id="07b49-106">この手順は、デモ会社 JPMF のデータを使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="07b49-106">This procedure was created using the demo company data JPMF.</span></span>

1. <span data-ttu-id="07b49-107">[売掛金勘定] > [支払] > [支払仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="07b49-107">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="07b49-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="07b49-108">Click New.</span></span>
3. <span data-ttu-id="07b49-109">[名前] フィールドに、「CustPay」と入力します。</span><span class="sxs-lookup"><span data-stu-id="07b49-109">In the Name field, type 'CustPay'.</span></span>
4. <span data-ttu-id="07b49-110">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="07b49-110">Click Lines.</span></span>
5. <span data-ttu-id="07b49-111">[機能] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="07b49-111">Click Functions.</span></span>
6. <span data-ttu-id="07b49-112">[支払のインポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="07b49-112">Click Import payments.</span></span>
7. <span data-ttu-id="07b49-113">[支払方法] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="07b49-113">In the Method of payment field, type a value.</span></span>
    * <span data-ttu-id="07b49-114">たとえば、JBA (JP) の形式 A を使用する支払方法を入力します。</span><span class="sxs-lookup"><span data-stu-id="07b49-114">For example, enter the method of payment that uses JBA(JP) - Format A.</span></span>  
8. <span data-ttu-id="07b49-115">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="07b49-115">Click OK.</span></span>
    * <span data-ttu-id="07b49-116">アップロードするファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="07b49-116">Select the file to upload.</span></span>  
9. <span data-ttu-id="07b49-117">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="07b49-117">Click OK.</span></span>
10. <span data-ttu-id="07b49-118">レポートを閉じる</span><span class="sxs-lookup"><span data-stu-id="07b49-118">Close the report</span></span>
    * <span data-ttu-id="07b49-119">管理レポートが生成されます。</span><span class="sxs-lookup"><span data-stu-id="07b49-119">A control report is generated.</span></span>  
    * <span data-ttu-id="07b49-120">支払金額と説明がインポートされることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="07b49-120">Note that the payment amount and description are imported.</span></span>  
11. <span data-ttu-id="07b49-121">[口座] フィールドで、「JPMF-000001」という値を指定します。</span><span class="sxs-lookup"><span data-stu-id="07b49-121">In the Account field, specify the values 'JPMF-000001'.</span></span>
12. <span data-ttu-id="07b49-122">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="07b49-122">Click Post.</span></span>

