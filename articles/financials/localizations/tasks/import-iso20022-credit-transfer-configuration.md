--- 
title: "ISO20022 口座振替コンフィギュレーションのインポート"
description: "この手順では、仕入先支払の電子レポートのコンフィギュレーションをインポートする方法を示します。"
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
ms.openlocfilehash: 71c0175178203006e297466c4a37cd3e6319b6ea
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="import-iso20022-credit-transfer-configuration"></a><span data-ttu-id="1a57e-103">ISO20022 口座振替コンフィギュレーションのインポート</span><span class="sxs-lookup"><span data-stu-id="1a57e-103">Import ISO20022 credit transfer configuration</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1a57e-104">この手順では、仕入先支払の電子レポートのコンフィギュレーションをインポートする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="1a57e-104">This procedure shows how to import a vendor payment electronic reporting configuration.</span></span> <span data-ttu-id="1a57e-105">ドイツの ISO 20022 口座振替形式が例として使用されます。</span><span class="sxs-lookup"><span data-stu-id="1a57e-105">The German ISO 20022 credit transfer format is used as an example.</span></span> <span data-ttu-id="1a57e-106">この手順は、使用可能なその他の電子申告フォーマットに使用できます。</span><span class="sxs-lookup"><span data-stu-id="1a57e-106">This procedure can be used for other available electronic reporting format.</span></span> 

<span data-ttu-id="1a57e-107">このタスクはデモ データの会社 DEMF を使用して作成されましたが、どのデモ データの会社を使用してもこのタスクを完了できます。</span><span class="sxs-lookup"><span data-stu-id="1a57e-107">This task was created using the demo data company DEMF but you can use any demo data company to complete this task.</span></span>

<span data-ttu-id="1a57e-108">これは、5 つのうち 1 つ目のタスクで、電子レポートのコンフィギュレーションを使用する仕入先支払処理を一緒に説明しています。</span><span class="sxs-lookup"><span data-stu-id="1a57e-108">This is the first of five tasks, that together illustrate the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="1a57e-109">この手順は、Dynamics 365 for Operations、バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="1a57e-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="1a57e-110">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1a57e-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="1a57e-111">使用できるコンフィギュレーション プロバイダーの一覧で、[Microsoft] を選択します。</span><span class="sxs-lookup"><span data-stu-id="1a57e-111">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="1a57e-112">[有効に設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1a57e-112">Click Set active.</span></span>
4. <span data-ttu-id="1a57e-113">[リポジトリ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1a57e-113">Click Repositories.</span></span>
5. <span data-ttu-id="1a57e-114">[開く] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1a57e-114">Click Open.</span></span>
6. <span data-ttu-id="1a57e-115">[フィルターの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1a57e-115">Click Show filters.</span></span>
7. <span data-ttu-id="1a57e-116">[コンフィギュレーション名] フィールドで "次の値で始まる" フィルター演算子を使用して、値 "ISO20022 口座振替 (DE)" でフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="1a57e-116">Apply the following filters: Enter a filter value of "ISO20022 Credit transfer (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="1a57e-117">または、一覧からコンフィギュレーションを見つけ、選択し、インポート タスクに移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="1a57e-117">Alternatively, you can find the configuration in the list, select it, and then move it to the Import task.</span></span>  
8. <span data-ttu-id="1a57e-118">[インポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1a57e-118">Click Import.</span></span>
    * <span data-ttu-id="1a57e-119">インポートのボタンを使用できない場合は、そのコンフィギュレーションは既にインポートされています。</span><span class="sxs-lookup"><span data-stu-id="1a57e-119">If the Import button is not available, it means that the configuration has  already been imported.</span></span>  
9. <span data-ttu-id="1a57e-120">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1a57e-120">Click Yes.</span></span>


