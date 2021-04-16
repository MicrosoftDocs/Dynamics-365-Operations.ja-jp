---
title: ISO20022 口座引落用の会社の銀行口座の設定
description: このタスクでは、顧客支払ファイルを生成するのに必要な会社固有の銀行口座情報の設定について説明します。
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 319bf71982987296a8270f596f8d2bb518dd1790
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819459"
---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="7f8c2-103">ISO20022 口座引落用の会社の銀行口座の設定</span><span class="sxs-lookup"><span data-stu-id="7f8c2-103">Set up company bank accounts for ISO20022 direct debits</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7f8c2-104">このタスクでは、顧客支払ファイルを生成するのに必要な会社固有の銀行口座情報の設定について説明します。</span><span class="sxs-lookup"><span data-stu-id="7f8c2-104">This task walks you through setting up the company specific bank account information that is required for generating customer payment files.</span></span> <span data-ttu-id="7f8c2-105">この手順では、ISO 20022 口座引落形式を例として使用します。</span><span class="sxs-lookup"><span data-stu-id="7f8c2-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> <span data-ttu-id="7f8c2-106">他の形式では、会社 ID または並べ替えコードなどの情報の設定が必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="7f8c2-106">Other formats might require additional setup information like the Company ID or the Sort code.</span></span>



<span data-ttu-id="7f8c2-107">このタスクは デモ データ会社 DEMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="7f8c2-107">This task was created using the demo data company DEMF.</span></span>



<span data-ttu-id="7f8c2-108">これは、5 つのうち 2 つ目の手順で、電子レポートのコンフィギュレーションを使用する顧客支払処理を説明しています。</span><span class="sxs-lookup"><span data-stu-id="7f8c2-108">This is the second of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-the-iban-and-swift-codes"></a><span data-ttu-id="7f8c2-109">IBAN および SWIFT コードの設定</span><span class="sxs-lookup"><span data-stu-id="7f8c2-109">Set up the IBAN and SWIFT codes</span></span>
1. <span data-ttu-id="7f8c2-110">[現金および銀行管理] > [銀行口座] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f8c2-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="7f8c2-111">クイック フィルターを使用して、値が「DEMF OPER」である [銀行口座] フィールドをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="7f8c2-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="7f8c2-112">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f8c2-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7f8c2-113">たとえば、「DEMF OPER」をクリックして、銀行口座詳細を開きます。</span><span class="sxs-lookup"><span data-stu-id="7f8c2-113">For example, click 'DEMF OPER' to open the bank account details.</span></span>  
4. <span data-ttu-id="7f8c2-114">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f8c2-114">Click Edit.</span></span>
5. <span data-ttu-id="7f8c2-115">[追加 ID] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="7f8c2-115">Expand or collapse the Additional identification section.</span></span>
6. <span data-ttu-id="7f8c2-116">[IBAN] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7f8c2-116">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="7f8c2-117">たとえば、「DE89370400440532013000」を入力します。</span><span class="sxs-lookup"><span data-stu-id="7f8c2-117">For example, enter 'DE89370400440532013000'.</span></span>  
7. <span data-ttu-id="7f8c2-118">[SWIFT コード] フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7f8c2-118">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="7f8c2-119">たとえば、「DEUTDEFF」を入力します。</span><span class="sxs-lookup"><span data-stu-id="7f8c2-119">For example, enter 'DEUTDEFF'.</span></span>    <span data-ttu-id="7f8c2-120">SWIFT \ BIC は多くの支払形式で必須ではありませんが、銀行口座への登録が推奨されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="7f8c2-120">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="7f8c2-121">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f8c2-121">Click Save.</span></span>

## <a name="set-up-a-bank-account-for-the-legal-entity"></a><span data-ttu-id="7f8c2-122">法人用の銀行口座の設定</span><span class="sxs-lookup"><span data-stu-id="7f8c2-122">Set up a bank account for the legal entity</span></span>
1. <span data-ttu-id="7f8c2-123">[組織管理] > [組織] > [法人] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f8c2-123">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="7f8c2-124">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f8c2-124">Click Edit.</span></span>
3. <span data-ttu-id="7f8c2-125">[銀行口座情報] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="7f8c2-125">Expand or collapse the Bank account information section.</span></span>
4. <span data-ttu-id="7f8c2-126">[銀行口座] フィールドで、ドロップ ダウン ボタンをクリックしてルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="7f8c2-126">In the Bank account field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="7f8c2-127">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f8c2-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7f8c2-128">たとえば、「DEMF OPER」銀行口座を選択します。</span><span class="sxs-lookup"><span data-stu-id="7f8c2-128">For example, select the "DEMF OPER" bank account.</span></span>  
6. <span data-ttu-id="7f8c2-129">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f8c2-129">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]