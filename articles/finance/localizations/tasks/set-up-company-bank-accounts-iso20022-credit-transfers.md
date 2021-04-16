---
title: ISO20022 口座振替用の会社の銀行口座の設定
description: この手順では、支払ファイルの生成に必要な会社固有の銀行口座情報を設定する方法を示します。
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
ms.openlocfilehash: a3ddcae4a53fffa07bd386174811c12150f2f162
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819483"
---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="c5410-103">ISO20022 口座振替用の会社の銀行口座の設定</span><span class="sxs-lookup"><span data-stu-id="c5410-103">Set up company bank accounts for ISO20022 credit transfers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c5410-104">この手順では、支払ファイルの生成に必要な会社固有の銀行口座情報を設定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="c5410-104">This procedure shows how to set up company-specific bank account information that is required for payment file generation.</span></span> <span data-ttu-id="c5410-105">ISO 20022 口座振替形式を生成するために必要な情報を設定しますが、形式に応じて会社 ID または並べ替えコードなど、その他の情報が必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="c5410-105">You set up information required to generate ISO 20022 credit transfer format but depending on the format there might be other information required, such as the Company ID or the Sort code.</span></span> 

<span data-ttu-id="c5410-106">この手順の作成に使用するデモ データの会社は DEMF です。</span><span class="sxs-lookup"><span data-stu-id="c5410-106">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="c5410-107">これは、5 つのうち 2 つ目の手順で、電子レポートのコンフィギュレーションを使用する仕入先支払処理を説明しています。</span><span class="sxs-lookup"><span data-stu-id="c5410-107">This is the second procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="c5410-108">この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="c5410-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-iban-and-swift-code"></a><span data-ttu-id="c5410-109">IBAN および SWIFT コードの設定</span><span class="sxs-lookup"><span data-stu-id="c5410-109">Set up IBAN and SWIFT code</span></span>
1. <span data-ttu-id="c5410-110">[現金および銀行管理] > [銀行口座] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c5410-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="c5410-111">クイック フィルターを使用して、値が「DEMF OPER」である [銀行口座] フィールドをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="c5410-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="c5410-112">[DEMF OPER] をクリックして、銀行口座詳細を開きます。</span><span class="sxs-lookup"><span data-stu-id="c5410-112">Click DEMF OPER to open bank account details.</span></span>
4. <span data-ttu-id="c5410-113">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c5410-113">Click Edit.</span></span>
5. <span data-ttu-id="c5410-114">[追加 ID] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c5410-114">Expand the Additional identification section.</span></span>
6. <span data-ttu-id="c5410-115">[IBAN] フィールドに「DE89370400440532013000」と入力します。</span><span class="sxs-lookup"><span data-stu-id="c5410-115">In the IBAN field, type 'DE89370400440532013000'.</span></span>
7. <span data-ttu-id="c5410-116">[SWIFT コード] フィールドに、「DEUTDEFF」を入力します。</span><span class="sxs-lookup"><span data-stu-id="c5410-116">In the SWIFT code field, type 'DEUTDEFF'.</span></span>
    * <span data-ttu-id="c5410-117">SWIFT\BIC は多くの支払形式で必須ではありませんが、銀行口座への登録が推奨されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="c5410-117">Note that SWIFT\BIC is not required for many payment formats, however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="c5410-118">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c5410-118">Click Save.</span></span>

## <a name="set-up-bank-account-for-the-legal-entity"></a><span data-ttu-id="c5410-119">法人用の銀行口座の設定</span><span class="sxs-lookup"><span data-stu-id="c5410-119">Set up bank account for the legal entity</span></span>
1. <span data-ttu-id="c5410-120">[組織管理] > [組織] > [法人] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c5410-120">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="c5410-121">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c5410-121">Click Edit.</span></span>
3. <span data-ttu-id="c5410-122">[銀行口座情報] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c5410-122">Expand the Bank account information section.</span></span>
4. <span data-ttu-id="c5410-123">[銀行口座] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c5410-123">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="c5410-124">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c5410-124">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]