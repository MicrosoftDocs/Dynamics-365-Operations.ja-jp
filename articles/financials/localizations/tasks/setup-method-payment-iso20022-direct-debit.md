--- 
title: "ISO20022 口座引落用の支払方法の設定"
description: "この手順では、ISO20022 口座振替の顧客の支払方法や電子レポートを使用したその他の支払タイプを設定する方法を示します。"
author: mrolecki
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 3a884837ab0b5a1f4211532969619b54206bbef4
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-method-of-payment-for-iso20022-direct-debit"></a><span data-ttu-id="88ec7-103">ISO20022 口座引落用の支払方法の設定</span><span class="sxs-lookup"><span data-stu-id="88ec7-103">Set up method of payment for ISO20022 direct debit</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="88ec7-104">この手順では、ISO20022 口座振替の顧客の支払方法や電子レポートを使用したその他の支払タイプを設定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="88ec7-104">This procedure shows how to set up the customer method of payment for ISO20022 direct debit or any other payment type using electronic reporting.</span></span> 



<span data-ttu-id="88ec7-105">このタスクを完了する前に、エクスポート形式のコンフィギュレーションおよび支払口座を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="88ec7-105">Before you complete this task, you must set up export format configurations and payment accounts.</span></span>



<span data-ttu-id="88ec7-106">この手順は、デモ データ会社 DEMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="88ec7-106">This procedure was created using the demo data company DEMF.</span></span>



<span data-ttu-id="88ec7-107">これは、5 つのうち 3 つ目の手順で、電子レポートのコンフィギュレーションを使用する顧客支払処理を説明しています。</span><span class="sxs-lookup"><span data-stu-id="88ec7-107">This is the third of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="88ec7-108">[売掛金管理] > [支払設定] > [支払方法] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="88ec7-108">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="88ec7-109">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="88ec7-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="88ec7-110">たとえば、[支払い方法] フィールドに値「ELECTRONIC」でフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="88ec7-110">For example, filter on the Method of payment field with a value of 'ELECTRONIC'.</span></span>
3. <span data-ttu-id="88ec7-111">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88ec7-111">Click Edit.</span></span>
4. <span data-ttu-id="88ec7-112">[支払勘定] フィールドで、値「DEMF OPER」を指定します。</span><span class="sxs-lookup"><span data-stu-id="88ec7-112">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
5. <span data-ttu-id="88ec7-113">[ファイル形式] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="88ec7-113">Expand the File formats section.</span></span>
6. <span data-ttu-id="88ec7-114">[一般的な電子申告] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="88ec7-114">Select Yes in the Generic electronic reporting field.</span></span>
7. <span data-ttu-id="88ec7-115">[エクスポート形式のコンフィギュレーション] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="88ec7-115">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="88ec7-116">一覧で、[ISO20022 口座引落 (DE)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="88ec7-116">In the list, select ISO20022 Direct debit (DE).</span></span>  <span data-ttu-id="88ec7-117">一覧が空の場合、顧客支払エクスポート形式のコンフィギュレーションはインポートされず有効になりません。</span><span class="sxs-lookup"><span data-stu-id="88ec7-117">If the list is empty, the customer payment export format configuration has not been imported and active.</span></span>  
8. <span data-ttu-id="88ec7-118">[委任状の要求] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="88ec7-118">Select Yes in the Require mandate field.</span></span>
    * <span data-ttu-id="88ec7-119">顧客支払形式の [委任状の要求] パラメーターを選択します。これには、SEPA 口座引落などの支払メッセージの委任状の情報が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="88ec7-119">Select the Require mandate parameter for customer payment formats, which require including mandate information in the payment message, like SEPA direct debit.</span></span>  
9. <span data-ttu-id="88ec7-120">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88ec7-120">Click Save.</span></span>


