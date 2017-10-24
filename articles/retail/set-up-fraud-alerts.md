---
title: "詐欺警告の設定"
description: "このトピックでは、注文が処理されるとき、詐欺の可能性ある情報を顧客サービス担当者に警告するルールを設定する方法について説明します。 自動または手動で疑わしい注文を保留にするために使用する、特殊なコードを定義できます。"
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 09d80015298c3d0219b6ffb290dc456990536a62
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-fraud-alerts"></a><span data-ttu-id="a03b8-104">詐欺警告の設定</span><span class="sxs-lookup"><span data-stu-id="a03b8-104">Set up fraud alerts</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="a03b8-105">このトピックでは、注文が処理されるとき、詐欺の可能性ある情報を顧客サービス担当者に警告するルールを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a03b8-105">This topic explains how to set up rules to alert customer service representatives of potentially fraudulent information when orders are processed.</span></span> <span data-ttu-id="a03b8-106">自動または手動で疑わしい注文を保留にするために使用する、特殊なコードを定義できます。</span><span class="sxs-lookup"><span data-stu-id="a03b8-106">You can define specific codes to use to automatically or manually put suspicious orders on hold.</span></span> 

<span data-ttu-id="a03b8-107">詐欺チェックルールを設定および使用する前に、コール センター パラメーターで、詐欺チェック機能が有効で、基本的な詐欺チェック値が定義されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="a03b8-107">Before you set up and use fraud checking rules, you must enable fraud checking and define the basic fraud checking values in the call center parameters.</span></span> <span data-ttu-id="a03b8-108">詐欺警告には、次の 2 つのタイプがあります。</span><span class="sxs-lookup"><span data-stu-id="a03b8-108">There are two types of fraud rules:</span></span>

-   <span data-ttu-id="a03b8-109">**静的ルール** ブラックリストに載せられた電話番号など、特定の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="a03b8-109">**Static rules** use a specific value, such as a phone number that has been blacklisted.</span></span>
-   <span data-ttu-id="a03b8-110">**動的ルール** 変数と要件を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="a03b8-110">**Dynamic rules** can be composed from variables and conditions.</span></span>

<span data-ttu-id="a03b8-111">動的ルールを作成する前に、だれにルールを適用するか、またいつルールを適用するかを定義する変数と条件を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a03b8-111">Before you create a dynamic rule, you must create the variables and conditions that define who the rule applies to and when the rule should be applied.</span></span> <span data-ttu-id="a03b8-112">たとえば、顧客 1202 が 1,000.00 以上の注文をしたとき、顧客支払が確認できるまで販売注文を保留するルールを作成します。</span><span class="sxs-lookup"><span data-stu-id="a03b8-112">For example, you want to create a rule to require that any sales order that customer 1202 places that is worth 1,000.00 or more be put on hold until the customer payment can be verified.</span></span> <span data-ttu-id="a03b8-113">この場合、変数は顧客 1202 と注文合計 1,000.00 です。</span><span class="sxs-lookup"><span data-stu-id="a03b8-113">In this case, the variables are customer 1202 and an order total of 1,000.00.</span></span> <span data-ttu-id="a03b8-114">条件は、顧客 1202 が 1,000.00 以上の注文をしたとき、顧客支払が確定されるまで、販売注文が保留されることを指定します。</span><span class="sxs-lookup"><span data-stu-id="a03b8-114">The condition specifies that if customer 1202 places an order, and the total amount of the order is equal to or more than 1,000.00, the sales order must be put on hold until the customer payment can be verified.</span></span>




