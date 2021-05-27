---
title: 買掛金勘定および売掛金勘定の TDS パラメータの設定
description: このトピックでは、源泉徴収税 (TDS) 控除をサポートするために買掛金勘定と売掛金勘定のパラメータを設定する方法について説明します。
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 4540cdfff2362d8fb7cc2b4cccf9c340be9750ce
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023388"
---
# <a name="set-tds-parameters-in-accounts-payable-and-accounts-receivable"></a><span data-ttu-id="19eae-103">買掛金勘定および売掛金勘定の TDS パラメータの設定</span><span class="sxs-lookup"><span data-stu-id="19eae-103">Set TDS parameters in Accounts payable and Accounts receivable</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="19eae-104">このトピックでは、源泉徴収税 (TDS) 控除をサポートするために買掛金勘定と売掛金勘定のパラメータを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="19eae-104">This topic explains how to set parameters in Accounts payable and Accounts receivable to support Tax Deducted at Source (TDS) deductions.</span></span>

1. <span data-ttu-id="19eae-105">**税 \> 設定 \> パラメーター \> 売掛金勘定パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="19eae-105">Go to **Tax \> Setup \> Parameters \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="19eae-106">**更新** タブで **注文明細行の更新** を選択して **注文明細行の更新** ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="19eae-106">On the **Updates** tab, select **Update order lines** to open the **Update order lines** dialog box.</span></span>
3. <span data-ttu-id="19eae-107">**TDS グループ** セクションの **TDS グループの更新** フィールドで、TDS グループを明細行レベルで更新するために使用する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="19eae-107">In the **TDS group** section, in the **Updating TDS group** field, specify the method to use to update the TDS group at the line level.</span></span> <span data-ttu-id="19eae-108">この設定は、注文ヘッダーで TDS グループが更新される場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="19eae-108">This setting is used when the TDS group is updated on an order header.</span></span> <span data-ttu-id="19eae-109">次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="19eae-109">The following options are available:</span></span>

    - <span data-ttu-id="19eae-110">**許可しない** – 注文ヘッダーで TDS グループが更新されても、注文明細行の TDS グループは更新されません。</span><span class="sxs-lookup"><span data-stu-id="19eae-110">**Never** – The TDS group isn't updated on the order lines when it's updated on the order header.</span></span>
    - <span data-ttu-id="19eae-111">**常時** – 注文ヘッダーで TDS グループが更新されると、注文明細行の TDS グループは自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="19eae-111">**Always** – The TDS group is automatically updated on the order lines when it's updated on the order header.</span></span>
    - <span data-ttu-id="19eae-112">**プロンプト** – ユーザーは、注文明細行の TDS グループを更新するように求めるメッセージを受信します。</span><span class="sxs-lookup"><span data-stu-id="19eae-112">**Prompt** – Users receive a message that prompts them to update the TDS group on the order lines.</span></span>
4. <span data-ttu-id="19eae-113">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="19eae-113">Select **OK**.</span></span>

    <span data-ttu-id="19eae-114">[![注文明細行の更新ダイアログ ボックス](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)</span><span class="sxs-lookup"><span data-stu-id="19eae-114">[![Update order lines dialog box](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)</span></span>

5. <span data-ttu-id="19eae-115">**税 \> 設定 \> パラメーター \> 買掛金勘定パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="19eae-115">Go to **Tax \> Setup \> Parameters \> Accounts payable parameters**.</span></span>
6. <span data-ttu-id="19eae-116">**全般** タブの **配送情報に基づく分割** クイック タブで、**製品受領書** オプションを **はい** に設定して、異なる配送先住所および税勘定番号 (TAN) を持つ製品受領書を転記および分割します。</span><span class="sxs-lookup"><span data-stu-id="19eae-116">On the **General** tab, on the **Split based on delivery information** FastTab, set the **Product receipt** option to **Yes** to post and split a product receipt that has different delivery addresses and tax account numbers (TANs).</span></span> <span data-ttu-id="19eae-117">このオプションが **いいえ** に設定されている場合は、配送先住所と TAN が異なる購買梱包明細を転記できません。</span><span class="sxs-lookup"><span data-stu-id="19eae-117">If this option is set to **No**, you can't post a purchase packing slip that has different delivery addresses and TANs.</span></span>
7. <span data-ttu-id="19eae-118">**請求書** オプションを **はい** に設定し、異なる配送先住所と TAN を含む仕入請求書を転記および分割します。</span><span class="sxs-lookup"><span data-stu-id="19eae-118">Set the **Invoice** option to **Yes** to post and split a purchase invoice that has different delivery addresses and TANs.</span></span>

    <span data-ttu-id="19eae-119">[![配送情報に基づく分割クイック タブ](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)</span><span class="sxs-lookup"><span data-stu-id="19eae-119">[![Split based on delivery information FastTab](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)</span></span>

8. <span data-ttu-id="19eae-120">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="19eae-120">Close the page.</span></span>
