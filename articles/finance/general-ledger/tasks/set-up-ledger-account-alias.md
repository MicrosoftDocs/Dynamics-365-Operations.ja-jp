---
title: 勘定科目のエイリアスの設定
description: この手順では、勘定番号を入力するショートカットを提供する勘定科目エイリアスを作成する方法について説明します。
author: aprilolson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAccountAlias
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cf5a0f233971fd7b84bb85c43bb0c0d585f0945a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838792"
---
# <a name="set-up-a-ledger-account-alias"></a><span data-ttu-id="90f38-103">勘定科目のエイリアスの設定</span><span class="sxs-lookup"><span data-stu-id="90f38-103">Set up a ledger account alias</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="90f38-104">この手順では、勘定番号を入力するショートカットを提供する勘定科目エイリアスを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="90f38-104">This procedure shows how to create an account alias that provides a shortcut for entering an account number.</span></span> <span data-ttu-id="90f38-105">この手順では、デモ データの会社 USMF を使用します。</span><span class="sxs-lookup"><span data-stu-id="90f38-105">This procedure uses demo data company USMF.</span></span>

1. <span data-ttu-id="90f38-106">[総勘定元帳] > [勘定科目表] > [勘定] > [勘定科目エイリアス] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="90f38-106">Go to General ledger > Chart of accounts > Accounts > Ledger account alias.</span></span>
2. <span data-ttu-id="90f38-107">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="90f38-107">Click New.</span></span>
3. <span data-ttu-id="90f38-108">[勘定科目エイリアス] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="90f38-108">In the Ledger account alias field, type a value.</span></span>
4. <span data-ttu-id="90f38-109">[勘定構造] フィールドで、勘定および分析コードが属する構造を選択します。</span><span class="sxs-lookup"><span data-stu-id="90f38-109">In the Account structure field, select the structure the account and dimensions belong to.</span></span>
5. <span data-ttu-id="90f38-110">[会社] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="90f38-110">In the Company field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="90f38-111">一覧で、エイリアスを適用する会社を検索し選択します。</span><span class="sxs-lookup"><span data-stu-id="90f38-111">In the list, find and select the company that the alias applies to.</span></span>
7. <span data-ttu-id="90f38-112">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="90f38-112">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="90f38-113">[勘定科目のエイリアス定義] フィールドで、勘定および分析コードを指定します。</span><span class="sxs-lookup"><span data-stu-id="90f38-113">In the Ledger account alias definition field, specify the account and dimensions.</span></span>
    * <span data-ttu-id="90f38-114">ショートカットを使用すると、勘定と分析コードが設定されます。</span><span class="sxs-lookup"><span data-stu-id="90f38-114">The account and dimensions will be populated when using the shortcut.</span></span>  
9. <span data-ttu-id="90f38-115">[初期フォーカス] フィールドで、エイリアスが使用された際にフォーカスされる分析コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="90f38-115">In the Initial focus field, select the dimension that will have focus when the alias is used.</span></span>
    * <span data-ttu-id="90f38-116">ショートカットの入力および勘定と分析コードの設定後、カーソルまたはフォーカスは [初期フォーカス] フィールドに移動します。</span><span class="sxs-lookup"><span data-stu-id="90f38-116">After you type the shortcut, and the account and dimensions are populated, the Initial focus field is where the cursor or focus will move to.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]