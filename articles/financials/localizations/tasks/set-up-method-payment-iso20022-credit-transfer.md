--- 
title: "ISO20022 口座振替用の支払方法の設定"
description: "この手順では、ISO20022 口座振替の仕入先の支払方法や電子レポートを使用してファイルを生成するその他の支払タイプを設定する方法を示します。"
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: bed51f8749dfa0264ad39f51f9ceb295ac46fe93
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a><span data-ttu-id="1a350-103">ISO20022 口座振替用の支払方法の設定</span><span class="sxs-lookup"><span data-stu-id="1a350-103">Set up method of payment for ISO20022 credit transfer</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1a350-104">この手順では、ISO20022 口座振替の仕入先の支払方法や電子レポートを使用してファイルを生成するその他の支払タイプを設定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="1a350-104">This procedure shows how to set up the vendor method of payment for ISO20022 credit transfer or any other payment type using electronic reporting to generate a file.</span></span> 

<span data-ttu-id="1a350-105">このタスクを完了する前に、書式設定のコンフィギュレーションをエクスポートして支払口座を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1a350-105">Before you complete this task, you must export format configurations and set up payment accounts.</span></span>

<span data-ttu-id="1a350-106">このタスクは、デモデータ会社 DEMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="1a350-106">This task was created using the DEMF demo data company.</span></span>

<span data-ttu-id="1a350-107">これは、5 つのうち 3 つ目の手順で、電子レポートのコンフィギュレーションを使用する仕入先支払処理を説明しています。</span><span class="sxs-lookup"><span data-stu-id="1a350-107">This is the third procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="1a350-108">この手順は、Dynamics 365 for Operations、バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="1a350-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="1a350-109">[買掛金勘定] > [支払設定] > [支払方法] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1a350-109">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="1a350-110">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="1a350-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="1a350-111">たとえば、値「SEPA CT」で [支払い方法] フィールドにフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="1a350-111">For example, filter on the Method of payment field with a value of 'SEPA CT'.</span></span>
3. <span data-ttu-id="1a350-112">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1a350-112">Click Edit.</span></span>
4. <span data-ttu-id="1a350-113">[期間] フィールドで、「合計」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1a350-113">In the Period field, select 'Total'.</span></span>
5. <span data-ttu-id="1a350-114">[支払タイプ] フィールドで、「電子支払」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1a350-114">In the Payment type field, select 'Electronic payment'.</span></span>
6. <span data-ttu-id="1a350-115">[ファイル形式] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="1a350-115">Expand the File formats section.</span></span>
7. <span data-ttu-id="1a350-116">[一般的な電子申告] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="1a350-116">Select Yes in the Generic electronic reporting field.</span></span>
8. <span data-ttu-id="1a350-117">[エクスポート形式のコンフィギュレーション] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="1a350-117">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="1a350-118">一覧で値「ISO20022 口座振替 (DE)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1a350-118">In the list, select the value ISO20022 Credit transfer (DE).</span></span> <span data-ttu-id="1a350-119">一覧が空の場合、仕入先支払エクスポート形式のコンフィギュレーションはインポートされず有効になりません。</span><span class="sxs-lookup"><span data-stu-id="1a350-119">If the list is empty, the vendor payment export format configuration is not imported and active.</span></span>  
9. <span data-ttu-id="1a350-120">[勘定タイプ] フィールドで、「銀行」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1a350-120">In the Account type field, select 'Bank'.</span></span>
10. <span data-ttu-id="1a350-121">[支払勘定] フィールドで、値「DEMF OPER」を指定します。</span><span class="sxs-lookup"><span data-stu-id="1a350-121">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
11. <span data-ttu-id="1a350-122">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1a350-122">Click Save.</span></span>


