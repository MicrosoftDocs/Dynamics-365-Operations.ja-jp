---
title: JBA 形式で EFT 支払ファイルを生成
description: 日本では一般的に、銀行間の電子資金決済 (EFT) には全国銀行協会 (JBA) のファイル形式が使用されています。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 95cfffa5bac4c3483c54296c91ffe05f987bb34c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822617"
---
# <a name="generate-eft-payment-file-with-jba-format"></a><span data-ttu-id="01da9-103">JBA 形式で EFT 支払ファイルを生成</span><span class="sxs-lookup"><span data-stu-id="01da9-103">Generate EFT payment file with JBA format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="01da9-104">日本では一般的に、銀行間の電子資金決済 (EFT) には全国銀行協会 (JBA) のファイル形式が使用されています。</span><span class="sxs-lookup"><span data-stu-id="01da9-104">In Japan, the Japanese Bankers Association (JBA) file format is commonly used for Electronic Fund Transfer (EFT) among banks.</span></span> 



<span data-ttu-id="01da9-105">このタスクでは、JBA 形式を使用した EFT ファイルの生成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="01da9-105">Use this task to learn how to generate an EFT file with the JBA format.</span></span>



<span data-ttu-id="01da9-106">この手順では、JPMF デモ会社のデータを使用します。</span><span class="sxs-lookup"><span data-stu-id="01da9-106">This task uses the JPMF demo company data.</span></span>

1. <span data-ttu-id="01da9-107">[買掛金勘定] > [支払] > [支払仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="01da9-107">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="01da9-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="01da9-108">Click New.</span></span>
3. <span data-ttu-id="01da9-109">[名前] フィールドに、「VendaPay」と入力します。</span><span class="sxs-lookup"><span data-stu-id="01da9-109">In the Name field, type 'VendPay'.</span></span>
4. <span data-ttu-id="01da9-110">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="01da9-110">Click Lines.</span></span>
5. <span data-ttu-id="01da9-111">[口座] フィールドで、「JPMF-000001」という値を指定します。</span><span class="sxs-lookup"><span data-stu-id="01da9-111">In the Account field, specify the values 'JPMF-000001'.</span></span>
6. <span data-ttu-id="01da9-112">[借方] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="01da9-112">In the Debit field, enter a number.</span></span>
7. <span data-ttu-id="01da9-113">後で参照するために、[相手勘定] フィールドの値をメモします。</span><span class="sxs-lookup"><span data-stu-id="01da9-113">Note the value in the Offset account field to reference later</span></span>
8. <span data-ttu-id="01da9-114">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="01da9-114">Click Save.</span></span>
9. <span data-ttu-id="01da9-115">[支払の生成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="01da9-115">Click Generate payments.</span></span>
10. <span data-ttu-id="01da9-116">[支払方法] フィールドで、JBA のファイル形式に対して有効化されている支払方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="01da9-116">In the Method of payment field, select a method of payment that is enabled for the JBA file format..</span></span>
11. <span data-ttu-id="01da9-117">[名前] フィールドで、生成されたファイルのファイル名を指定します。</span><span class="sxs-lookup"><span data-stu-id="01da9-117">In the File name field, Specify a file name for the generated file..</span></span>
12. <span data-ttu-id="01da9-118">[銀行口座] フィールドで、前にメモした値を使用します。</span><span class="sxs-lookup"><span data-stu-id="01da9-118">Use the value noted previously in the Bank account field</span></span>
    * <span data-ttu-id="01da9-119">仕入先の仕訳帳明細行で [相殺銀行口座] を選択します。</span><span class="sxs-lookup"><span data-stu-id="01da9-119">Select a Offset bank account in the vendor journal lines.</span></span>  
13. <span data-ttu-id="01da9-120">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="01da9-120">Click OK.</span></span>
    * <span data-ttu-id="01da9-121">支払管理レポートを印刷する場合は、スライダーを切り替えます。</span><span class="sxs-lookup"><span data-stu-id="01da9-121">Toggle the slider if you want to print the payment control report.</span></span>  
14. <span data-ttu-id="01da9-122">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="01da9-122">Click OK.</span></span>
    * <span data-ttu-id="01da9-123">.zip ファイルが生成され、ファイルをダウンロードするように求めるメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="01da9-123">A .zip file will be generated and you will be prompted to download the file.</span></span>  
    * <span data-ttu-id="01da9-124">[支払ステータス] が、[送信済] に切り替わります。</span><span class="sxs-lookup"><span data-stu-id="01da9-124">The Payment status will now switch to be 'Sent'.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]