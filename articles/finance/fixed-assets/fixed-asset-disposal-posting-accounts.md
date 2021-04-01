---
title: 固定資産の処分の転記勘定
description: このトピックは、資産の処分の総勘定元帳の転記勘定を設定する方法を説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 92b653d50744884d56c19601cff74c420eb1b397
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240973"
---
# <a name="fixed-asset-disposal-posting-accounts"></a><span data-ttu-id="412f5-103">固定資産の処分の転記勘定</span><span class="sxs-lookup"><span data-stu-id="412f5-103">Fixed asset disposal posting accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="412f5-104">このトピックは、資産の処分の総勘定元帳の転記勘定を設定する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="412f5-104">This topic explains how to set up general ledger posting accounts for disposing of assets.</span></span>

<span data-ttu-id="412f5-105">[勘定科目] クイック タブの [固定資産の転記プロファイル] のページで、[処分 - 売却] および [処分 - 仕損] を選択して、元帳への転記を設定します。</span><span class="sxs-lookup"><span data-stu-id="412f5-105">In the Fixed asset posting profiles page, on the Ledger accounts FastTab, select Disposal - sale and Disposal - scrap to set up postings to the ledger.</span></span>

<span data-ttu-id="412f5-106">どちらのトランザクション タイプの場合も、固定資産の処分金額は総勘定元帳の貸方に転記されます。</span><span class="sxs-lookup"><span data-stu-id="412f5-106">For both transaction types, the ledger account is credited for the disposal value of the fixed asset.</span></span> <span data-ttu-id="412f5-107">借方は銀行口座などの相手勘定に転記されます。</span><span class="sxs-lookup"><span data-stu-id="412f5-107">The debit is posted to an offset account, which might be, for example, a bank account.</span></span> <span data-ttu-id="412f5-108">固定資産を顧客に売却する場合は、相手勘定ではなく顧客勘定が使用されます。</span><span class="sxs-lookup"><span data-stu-id="412f5-108">If a fixed asset is sold to a customer, the customer account is used instead of the offset account.</span></span>

<span data-ttu-id="412f5-109">[処分] をクリックし、次に [売却] または [仕損] をクリックして、固定資産の正味簿価額を元に戻す具体的な勘定を設定します。</span><span class="sxs-lookup"><span data-stu-id="412f5-109">Click Disposal and then click Sale or Scrap, and then set up detailed accounts to reverse the net book value of the fixed asset.</span></span> <span data-ttu-id="412f5-110">また、[処分パラメーター] ページで、[転記金額] フィールドや [売却額のタイプ] フィールドに情報を入力できます。</span><span class="sxs-lookup"><span data-stu-id="412f5-110">You can also enter information in the Post value and Sales value type fields in the Disposal parameters page.</span></span> 

<span data-ttu-id="412f5-111">低価格プール内の資産に対する処分トランザクションは、低価格プールの正味簿価額を処分金額分だけ減額します。</span><span class="sxs-lookup"><span data-stu-id="412f5-111">The disposal transaction for an asset in a low-value pool reduces the net book value of the low-value pool by the disposed amount only.</span></span> <span data-ttu-id="412f5-112">ただし、資産の売却額が低価格プールの正味簿価額を超えた場合、正味簿価額はゼロに減額されます。</span><span class="sxs-lookup"><span data-stu-id="412f5-112">However, when the sale of an asset exceeds the net book value of the low-value pool, the net book value is reduced to zero.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]