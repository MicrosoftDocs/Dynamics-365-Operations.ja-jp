---
title: TDS 特約証明書番号を記録する
description: このトピックでは、仕入先に発行された源泉徴収 (TDS) 特約証明書の番号を記録する方法について説明します。
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
ms.openlocfilehash: f543adc8bab5ca224bdb672d6b3c282c2d8531d8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023376"
---
# <a name="record-tds-concession-certificate-numbers"></a><span data-ttu-id="967f4-103">TDS 特約証明書番号を記録する</span><span class="sxs-lookup"><span data-stu-id="967f4-103">Record TDS concession certificate numbers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="967f4-104">このトピックでは、仕入先に発行された源泉徴収 (TDS) 特約証明書の番号を記録する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="967f4-104">This topic explains how to record the Tax Deducted at Source (TDS) concession certificate numbers that are issued to vendors.</span></span>

1. <span data-ttu-id="967f4-105">**税 \> 間接税 \> 源泉徴収税 \> 源泉徴収税特約** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="967f4-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax concessions**.</span></span>
2. <span data-ttu-id="967f4-106">**税タイプ** フィールドで、TDS 税タイプの特約証明書を記録する **TDS** を選択します。</span><span class="sxs-lookup"><span data-stu-id="967f4-106">In the **Tax type** field, select **TDS** to record concession certificates for the TDS tax type.</span></span>
3. <span data-ttu-id="967f4-107">**概要** タブ で 、**Alt+N** キーを押して明細行を作成します。</span><span class="sxs-lookup"><span data-stu-id="967f4-107">On the **Overview** tab, select **Alt+N** to create a line.</span></span>

    <span data-ttu-id="967f4-108">[![新しい明細行のヘッダー](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)</span><span class="sxs-lookup"><span data-stu-id="967f4-108">[![Header of the new line](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)</span></span>

4. <span data-ttu-id="967f4-109">**源泉徴収税コード** フィールドで、仕入先特約証明書の発行対象である TDS 税コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="967f4-109">In the **Withholding tax code** field, select the TDS tax code that the vendor concession certificates are issued for.</span></span> <span data-ttu-id="967f4-110">**源泉徴収税コード名** フィールドに、源泉徴収税コードの名前が表示されます。</span><span class="sxs-lookup"><span data-stu-id="967f4-110">The **Withholding tax code name** field shows the name of the TDS tax code.</span></span>
5. <span data-ttu-id="967f4-111">**開始日** フィールドと **終了日** フィールドで 、TDS税コードを使用して特約ベースで仕入先の TDS を計算する特約証明書の有効期間を定義します。</span><span class="sxs-lookup"><span data-stu-id="967f4-111">In the **From date** and **To date** fields, define the period of validity for the concession certificate that uses the TDS tax code to calculate TDS for the vendor on a concessional basis.</span></span>
6. <span data-ttu-id="967f4-112">**注釈** フィールド に、注釈を入力します。</span><span class="sxs-lookup"><span data-stu-id="967f4-112">In the **Remarks** field, enter any remarks.</span></span>
7. <span data-ttu-id="967f4-113">**セクション** フィールドに、TDS 特約証明書の使用を変更する法的セクション コードを入力します。</span><span class="sxs-lookup"><span data-stu-id="967f4-113">In the **Section** field, enter the legal section code that the TDS concession certificate is availed under.</span></span>

    <span data-ttu-id="967f4-114">セクション コードが 197 の場合、値 "A" は、フォーム 26Q の [非控除/控除の理由] 列とフォーム 27Q の [非控除/控除の理由/控除額の引き下げ/総額設定 (使用する場合)] 列の両方に表示されます。</span><span class="sxs-lookup"><span data-stu-id="967f4-114">If the section code is 197, the value "A" appears in both the "Reason for non-deduction/lower deduction" column in Form 26Q and the "Reason for non-deduction/lower deduction/grossing up (if any)" column in Form 27Q.</span></span> <span data-ttu-id="967f4-115">セクション コードが 197A の場合、両方の場所に値 "B" が表示されます。</span><span class="sxs-lookup"><span data-stu-id="967f4-115">If the section code is 197A, the value "B" appears in both those places.</span></span>

8. <span data-ttu-id="967f4-116">仕入先の TDS 特約証明書番号を記録する **証明書** クイック タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="967f4-116">Select the **Certificate** FastTab to record TDS concession certificate numbers for vendors.</span></span>
9. <span data-ttu-id="967f4-117">**仕入先アカウント** フィールドで、TDS 特約証明書を発行する仕入先を選択します。</span><span class="sxs-lookup"><span data-stu-id="967f4-117">In the **Vendor account** field, select the vendor account that the TDS concession certificate is issued for.</span></span>
10. <span data-ttu-id="967f4-118">**開始日** フィールドおよび **終了日** フィールドで 、TDS 特約証明書の有効期間を定義します。</span><span class="sxs-lookup"><span data-stu-id="967f4-118">In the **From date** and **To date** fields, define the period of validity for the TDS concession certificate.</span></span>

    <span data-ttu-id="967f4-119">特約ベースでの TDS の計算は、仕入先の証明書が作成された期間に基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="967f4-119">The calculation of TDS on a concessional basis is based on the period when the certificate is created for the vendor.</span></span>

11. <span data-ttu-id="967f4-120">**証明書** フィールドに、TDS特約証明書番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="967f4-120">In the **Certificate** field, enter the TDS concession certificate number.</span></span>

    <span data-ttu-id="967f4-121">[![証明書クイック タブ](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)</span><span class="sxs-lookup"><span data-stu-id="967f4-121">[![Certificate FastTab](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)</span></span>

12. <span data-ttu-id="967f4-122">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="967f4-122">Close the page.</span></span>
