---
title: ISO20022 口座引落用の支払方法の設定
description: この手順では、ISO20022 口座振替の顧客の支払方法や電子レポートを使用したその他の支払タイプを設定する方法を示します。
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9c6a692553867d7e8679099210dc44b9d9e4d0f1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838685"
---
# <a name="setup-method-of-payment-for-iso20022-direct-debit"></a><span data-ttu-id="74aad-103">ISO20022 口座引落用の支払方法の設定</span><span class="sxs-lookup"><span data-stu-id="74aad-103">Setup method of payment for ISO20022 direct debit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="74aad-104">この手順では、ISO20022 口座振替の顧客の支払方法や電子レポートを使用したその他の支払タイプを設定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="74aad-104">This procedure shows how to set up the customer method of payment for ISO20022 direct debit or any other payment type using electronic reporting.</span></span> 



<span data-ttu-id="74aad-105">このタスクを完了する前に、エクスポート形式のコンフィギュレーションおよび支払口座を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="74aad-105">Before you complete this task, you must set up export format configurations and payment accounts.</span></span>



<span data-ttu-id="74aad-106">この手順は、デモ データ会社 DEMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="74aad-106">This procedure was created using the demo data company DEMF.</span></span>



<span data-ttu-id="74aad-107">これは、5 つのうち 3 つ目の手順で、電子レポートのコンフィギュレーションを使用する顧客支払処理を説明しています。</span><span class="sxs-lookup"><span data-stu-id="74aad-107">This is the third of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="74aad-108">[売掛金管理] > [支払設定] > [支払方法] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="74aad-108">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="74aad-109">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="74aad-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="74aad-110">たとえば、[支払い方法] フィールドに値「ELECTRONIC」でフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="74aad-110">For example, filter on the Method of payment field with a value of 'ELECTRONIC'.</span></span>
3. <span data-ttu-id="74aad-111">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="74aad-111">Click Edit.</span></span>
4. <span data-ttu-id="74aad-112">[支払勘定] フィールドで、値「DEMF OPER」を指定します。</span><span class="sxs-lookup"><span data-stu-id="74aad-112">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
5. <span data-ttu-id="74aad-113">[ファイル形式] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="74aad-113">Expand the File formats section.</span></span>
6. <span data-ttu-id="74aad-114">[一般的な電子申告] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="74aad-114">Select Yes in the Generic electronic reporting field.</span></span>
7. <span data-ttu-id="74aad-115">[エクスポート形式のコンフィギュレーション] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="74aad-115">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="74aad-116">一覧で、[ISO20022 口座引落 (DE)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="74aad-116">In the list, select ISO20022 Direct debit (DE).</span></span>  <span data-ttu-id="74aad-117">一覧が空の場合、顧客支払エクスポート形式のコンフィギュレーションはインポートされず有効になりません。</span><span class="sxs-lookup"><span data-stu-id="74aad-117">If the list is empty, the customer payment export format configuration has not been imported and active.</span></span>  
8. <span data-ttu-id="74aad-118">[委任状の要求] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="74aad-118">Select Yes in the Require mandate field.</span></span>
    * <span data-ttu-id="74aad-119">顧客支払形式の [委任状の要求] パラメーターを選択します。これには、SEPA 口座引落などの支払メッセージの委任状の情報が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="74aad-119">Select the Require mandate parameter for customer payment formats, which require including mandate information in the payment message, like SEPA direct debit.</span></span>  
9. <span data-ttu-id="74aad-120">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="74aad-120">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]