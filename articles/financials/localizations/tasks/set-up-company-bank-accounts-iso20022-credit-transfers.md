--- 
title: "ISO20022 口座振替用の会社の銀行口座の設定"
description: "この手順では、支払ファイルの生成に必要な会社固有の銀行口座情報を設定する方法を示します。"
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1d0eabdfdeb5ed7d0bdb6df87ebdfa0d41e87492
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="fb122-103">ISO20022 口座振替用の会社の銀行口座の設定</span><span class="sxs-lookup"><span data-stu-id="fb122-103">Set up company bank accounts for ISO20022 credit transfers</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fb122-104">この手順では、支払ファイルの生成に必要な会社固有の銀行口座情報を設定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="fb122-104">This procedure shows how to set up company-specific bank account information that is required for payment file generation.</span></span> <span data-ttu-id="fb122-105">ISO 20022 口座振替形式を生成するために必要な情報を設定しますが、形式に応じて会社 ID または並べ替えコードなど、その他の情報が必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="fb122-105">You set up information required to generate ISO 20022 credit transfer format but depending on the format there might be other information required, such as the Company ID or the Sort code.</span></span> 

<span data-ttu-id="fb122-106">この手順の作成に使用するデモ データの会社は DEMF です。</span><span class="sxs-lookup"><span data-stu-id="fb122-106">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="fb122-107">これは、5 つのうち 2 つ目の手順で、電子レポートのコンフィギュレーションを使用する仕入先支払処理を説明しています。</span><span class="sxs-lookup"><span data-stu-id="fb122-107">This is the second procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="fb122-108">この手順は、Dynamics 365 for Operations、バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="fb122-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-iban-and-swift-code"></a><span data-ttu-id="fb122-109">IBAN および SWIFT コードの設定</span><span class="sxs-lookup"><span data-stu-id="fb122-109">Set up IBAN and SWIFT code</span></span>
1. <span data-ttu-id="fb122-110">[現金および銀行管理] > [銀行口座] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="fb122-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="fb122-111">クイック フィルターを使用して、値が「DEMF OPER」である [銀行口座] フィールドをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="fb122-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="fb122-112">[DEMF OPER] をクリックして、銀行口座詳細を開きます。</span><span class="sxs-lookup"><span data-stu-id="fb122-112">Click DEMF OPER to open bank account details.</span></span>
4. <span data-ttu-id="fb122-113">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fb122-113">Click Edit.</span></span>
5. <span data-ttu-id="fb122-114">[追加 ID] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="fb122-114">Expand the Additional identification section.</span></span>
6. <span data-ttu-id="fb122-115">[IBAN] フィールドに「DE89370400440532013000」と入力します。</span><span class="sxs-lookup"><span data-stu-id="fb122-115">In the IBAN field, type 'DE89370400440532013000'.</span></span>
7. <span data-ttu-id="fb122-116">[SWIFT コード] フィールドに、「DEUTDEFF」を入力します。</span><span class="sxs-lookup"><span data-stu-id="fb122-116">In the SWIFT code field, type 'DEUTDEFF'.</span></span>
    * <span data-ttu-id="fb122-117">SWIFT\BIC は多くの支払形式で必須ではありませんが、銀行口座への登録が推奨されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="fb122-117">Note that SWIFT\BIC is not required for many payment formats, however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="fb122-118">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fb122-118">Click Save.</span></span>

## <a name="set-up-bank-account-for-the-legal-entity"></a><span data-ttu-id="fb122-119">法人用の銀行口座の設定</span><span class="sxs-lookup"><span data-stu-id="fb122-119">Set up bank account for the legal entity</span></span>
1. <span data-ttu-id="fb122-120">[組織管理] > [組織] > [法人] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="fb122-120">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="fb122-121">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fb122-121">Click Edit.</span></span>
3. <span data-ttu-id="fb122-122">[銀行口座情報] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="fb122-122">Expand the Bank account information section.</span></span>
4. <span data-ttu-id="fb122-123">[銀行口座] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="fb122-123">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="fb122-124">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fb122-124">Click Save.</span></span>


