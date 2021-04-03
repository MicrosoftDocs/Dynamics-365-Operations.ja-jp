---
title: 修復管理
description: 過去に役立った解決策の提案により、問題を体系的にまとめます。
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAConditionTable, SMASymptomArea, SMADiagnosisArea, SMAResolutionTable, SMARepairStage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 265709f298d9310d5d647eaa029ece778d2e226e
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470644"
---
# <a name="repair-management"></a><span data-ttu-id="8fc63-103">修復管理</span><span class="sxs-lookup"><span data-stu-id="8fc63-103">Repair management</span></span>       

[!include [banner](../includes/banner.md)]


<span data-ttu-id="8fc63-104">修復管理のために、問題を体系的にグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="8fc63-104">For repair management you can group problems systematically.</span></span> <span data-ttu-id="8fc63-105">これは、過去に成功した解決策の提案を支援するためです。</span><span class="sxs-lookup"><span data-stu-id="8fc63-105">This is to help with the suggestion of solutions that have been successful in the past.</span></span>

<span data-ttu-id="8fc63-106">現象、診断、および解決策を設定します。</span><span class="sxs-lookup"><span data-stu-id="8fc63-106">You set up symptoms, diagnosis, and resolution settings.</span></span> <span data-ttu-id="8fc63-107">すべてこれらは、後で、修復のための同様の品目を受け取ったときに適用できます。</span><span class="sxs-lookup"><span data-stu-id="8fc63-107">All these can later be applied when you receive a similar item for repair.</span></span> <span data-ttu-id="8fc63-108">修復の問題の進捗を追跡できる修復ステージを設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="8fc63-108">You can also set up repair stages that can follow the progress of a repair issue.</span></span>

## <a name="setting-up-repair-management"></a><span data-ttu-id="8fc63-109">修理の管理の設定</span><span class="sxs-lookup"><span data-stu-id="8fc63-109">Setting up repair management</span></span>

<span data-ttu-id="8fc63-110">修復の現象、診断、および解決策を指定するために使用される情報を入力するには、次の設定フォームを使用します。</span><span class="sxs-lookup"><span data-stu-id="8fc63-110">Use the following setup forms to enter information that will be used to specify the symptoms, the diagnosis, and the resolution, of the repair.</span></span>

- <span data-ttu-id="8fc63-111">**サービス管理** \> **設定** \> **修復** \> **条件**。</span><span class="sxs-lookup"><span data-stu-id="8fc63-111">**Service management** \> **Setup** \> **Repair** \> **Conditions**.</span></span>
- <span data-ttu-id="8fc63-112">**サービス管理** \> **設定** \> **修復** \> **現象の範囲**。</span><span class="sxs-lookup"><span data-stu-id="8fc63-112">**Service management** \> **Setup** \> **Repair** \> **Symptom areas**.</span></span>
-  <span data-ttu-id="8fc63-113">**サービス管理** \> **設定** \> **修復** \> **診断の範囲**。</span><span class="sxs-lookup"><span data-stu-id="8fc63-113">**Service management** \> **Setup** \> **Repair** \> **Diagnosis areas**.</span></span>
- <span data-ttu-id="8fc63-114">**サービス管理** \> **設定** \> **修復** \> **解決策**。</span><span class="sxs-lookup"><span data-stu-id="8fc63-114">**Service management** \> **Setup** \> **Repair** \> **Resolutions**.</span></span>
- <span data-ttu-id="8fc63-115">**サービス管理** \> **設定** \> **修復** \> **修復ステージ**。</span><span class="sxs-lookup"><span data-stu-id="8fc63-115">**Service management** \> **Setup** \> **Repair** \> **Repair stages**.</span></span>

## <a name="symptoms-and-conditions"></a><span data-ttu-id="8fc63-116">現象と状態</span><span class="sxs-lookup"><span data-stu-id="8fc63-116">Symptoms and conditions</span></span>

<span data-ttu-id="8fc63-117">現象とは、顧客による問題の特徴づけの方法です。</span><span class="sxs-lookup"><span data-stu-id="8fc63-117">Symptoms are how the customer characterizes the problem.</span></span> <span data-ttu-id="8fc63-118">現象には、修復の必要性を示す顧客の観察が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8fc63-118">Symptoms include the customer observations that indicate the need for repair.</span></span>

<span data-ttu-id="8fc63-119">現象の範囲、現象コード、および条件を設定できます。</span><span class="sxs-lookup"><span data-stu-id="8fc63-119">You can set up symptom areas, symptom codes, and conditions.</span></span> <span data-ttu-id="8fc63-120">現象の範囲は障害の領域をカバーし、現象コードは障害の症状をカバーします。</span><span class="sxs-lookup"><span data-stu-id="8fc63-120">The symptom area covers the area of malfunction, and the symptom code covers the malfunction symptom.</span></span> <span data-ttu-id="8fc63-121">状態は、問題が発生したときに存在する状況または環境を説明します。</span><span class="sxs-lookup"><span data-stu-id="8fc63-121">The condition describes the situation or environment that is present when the problem occurs.</span></span>

<span data-ttu-id="8fc63-122">**例**</span><span class="sxs-lookup"><span data-stu-id="8fc63-122">**Example**</span></span>

<span data-ttu-id="8fc63-123">長期の使用の後、ハード ドライブが故障したので、コンピュータが修理に持ち込まれています。</span><span class="sxs-lookup"><span data-stu-id="8fc63-123">A computer is brought in for repair because the hard drive fails after an extended period of use.</span></span> <span data-ttu-id="8fc63-124">ハード ドライブの故障により、ブルー スクリーン エラーが発生しています。</span><span class="sxs-lookup"><span data-stu-id="8fc63-124">The hard drive failure causes a blue screen error.</span></span> <span data-ttu-id="8fc63-125">コンピュータを受け取る技術者は、次の症状や状態を入力します。</span><span class="sxs-lookup"><span data-stu-id="8fc63-125">The technician who receives the computer enters the following symptoms and conditions:</span></span>

1.  <span data-ttu-id="8fc63-126">現象の範囲はハード ドライブ。</span><span class="sxs-lookup"><span data-stu-id="8fc63-126">The symptom area is the hard drive</span></span>

2.  <span data-ttu-id="8fc63-127">現象コードはブルー スクリーンのエラー</span><span class="sxs-lookup"><span data-stu-id="8fc63-127">The symptom code is the blue screen error</span></span>

3.  <span data-ttu-id="8fc63-128">状態は、長期の使用後、ハード ドライブが故障</span><span class="sxs-lookup"><span data-stu-id="8fc63-128">The condition is that the hard drive fails after extended use</span></span>

## <a name="diagnosis-and-resolutions"></a><span data-ttu-id="8fc63-129">診断と解決策</span><span class="sxs-lookup"><span data-stu-id="8fc63-129">Diagnosis and resolutions</span></span>

<span data-ttu-id="8fc63-130">診断と解決策のフィールドは、修復の観点からの説明です。</span><span class="sxs-lookup"><span data-stu-id="8fc63-130">The diagnosis and resolution fields are statements from the repair perspective.</span></span> <span data-ttu-id="8fc63-131">これらは、技術者が問題を調査するために実行するステップです。</span><span class="sxs-lookup"><span data-stu-id="8fc63-131">These are the steps that a technician went through to investigate the problem.</span></span>

<span data-ttu-id="8fc63-132">診断の範囲は、問題を解決するために行われる必要がある操作をカバーします。</span><span class="sxs-lookup"><span data-stu-id="8fc63-132">The diagnosis area covers the operation that must occur to solve the issue.</span></span> <span data-ttu-id="8fc63-133">診断コードは問題がどのように処理されたかを示し、解決策は、品目が修理された、交換された、顧客によって注文がキャンセルされた、などになります。</span><span class="sxs-lookup"><span data-stu-id="8fc63-133">The diagnosis code is how the problem was handled, and the resolution could be that the item was repaired, replaced, or the order was canceled by the customer.</span></span> <span data-ttu-id="8fc63-134">たとえば、コンピュータが修理された場合には、診断の範囲は "問題のある部品"、診断コードは "新しいビデオ カードの取り付け"、解決策は "交換" などになります。</span><span class="sxs-lookup"><span data-stu-id="8fc63-134">For example, if the computer is repaired, the diagnosis area could be "defective part," the diagnosis code could be "new video card installed," and the resolution could be "replaced."</span></span>

## <a name="repair-stages"></a><span data-ttu-id="8fc63-135">修復ステージ</span><span class="sxs-lookup"><span data-stu-id="8fc63-135">Repair stages</span></span>

<span data-ttu-id="8fc63-136">修復ステージは、修復プロセスの進捗を表します。</span><span class="sxs-lookup"><span data-stu-id="8fc63-136">Repair stages state the progress of the repair process.</span></span> <span data-ttu-id="8fc63-137">修復ステージには **完了** サインオフ パラメータがあります。これは、修復行が完了し、完了した日時が記録されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="8fc63-137">The repair stage has a **Finished** sign-off parameter that indicates that the repair line has been completed, and the finishing date and time has been recorded.</span></span>

## <a name="applying-repair-management"></a><span data-ttu-id="8fc63-138">修復管理の適用</span><span class="sxs-lookup"><span data-stu-id="8fc63-138">Applying repair management</span></span>

<span data-ttu-id="8fc63-139">品目に修復管理を適用するには、その品目が、サービス注文に対するサービス対象の関係で設定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="8fc63-139">To apply repair management to an item, the item must be set up with a service object relation on a service order.</span></span> <span data-ttu-id="8fc63-140">この条件が満たされている場合は、そのサービス注文から、現在の問題に関する情報を使用して修復行を作成できます。</span><span class="sxs-lookup"><span data-stu-id="8fc63-140">From the service order you can then create a repair line with information about the current issue.</span></span> <span data-ttu-id="8fc63-141">修復行では、修復の対象となるサービス対象と、現象、診断、および実行に関する情報を定義します。</span><span class="sxs-lookup"><span data-stu-id="8fc63-141">On the repair line you define the service object that is in repair and information about symptoms, diagnosis, and execution.</span></span> <span data-ttu-id="8fc63-142">修復行のメモを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="8fc63-142">You can also create a note for the repair line.</span></span>

<span data-ttu-id="8fc63-143">修復プロセスのステップごとに修復行を作成できます。</span><span class="sxs-lookup"><span data-stu-id="8fc63-143">You can create repair lines for each step in the repair process.</span></span>

## <a name="create-a-repair-line-on-a-service-order"></a><span data-ttu-id="8fc63-144">サービス注文の修復行の作成</span><span class="sxs-lookup"><span data-stu-id="8fc63-144">Create a repair line on a service order</span></span>

1.  <span data-ttu-id="8fc63-145">**サービス管理** \> **共通** \> **サービス注文** \> **サービス注文** に移動します。</span><span class="sxs-lookup"><span data-stu-id="8fc63-145">Go to **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="8fc63-146">修復が必要なサービス対象を含むサービス注文を選択します。</span><span class="sxs-lookup"><span data-stu-id="8fc63-146">Select the service order with the service object that needs repair.</span></span>

3.  <span data-ttu-id="8fc63-147">**修復** \> **修復行** をクリックして、**修復行** フォームを選択します。</span><span class="sxs-lookup"><span data-stu-id="8fc63-147">Select **Repair** \> **Repair lines** to open the **Repair lines** form.</span></span>

4.  <span data-ttu-id="8fc63-148">**新規作成** を選択して、新しい行を作成します。</span><span class="sxs-lookup"><span data-stu-id="8fc63-148">Select **New** to create a new line.</span></span>

5.  <span data-ttu-id="8fc63-149">サービス対象を選択します。</span><span class="sxs-lookup"><span data-stu-id="8fc63-149">Select a service object.</span></span> <span data-ttu-id="8fc63-150">そのサービス注文に対するサービス対象の関係で設定されている任意のサービス対象を選択できます。</span><span class="sxs-lookup"><span data-stu-id="8fc63-150">You can select any service object that has been set up with an object relation on the service order.</span></span>

6.  <span data-ttu-id="8fc63-151">現象、診断、および実行の設定値から現在の修復行に関連する値を選択し、必要に応じて、**注記** タブを選択して修復行に関するメモを作成します。</span><span class="sxs-lookup"><span data-stu-id="8fc63-151">Select any of the preset symptoms, diagnosis, and execution values that are relevant in the repair line and then select the **Note** tab to create a note on the repair line, if needed.</span></span>

7.  <span data-ttu-id="8fc63-152">**保存** を選択して修復行を保存します。</span><span class="sxs-lookup"><span data-stu-id="8fc63-152">Select **Save** to save the new repair line.</span></span> <span data-ttu-id="8fc63-153">**修復行** フォームの **一般** タブで、**作成日時** フィールドが、保存の時刻で更新されます。</span><span class="sxs-lookup"><span data-stu-id="8fc63-153">The **Created date and time** field in the **General** tab of the **Repair lines** form is updated with the time of saving.</span></span>

## <a name="tracking-progress-and-resolving-a-repair-issue"></a><span data-ttu-id="8fc63-154">進捗の追跡と修復問題の解決</span><span class="sxs-lookup"><span data-stu-id="8fc63-154">Tracking progress and resolving a repair issue</span></span>

<span data-ttu-id="8fc63-155">修復の進捗を追跡するように、修復行の修復ステージを設定できます。</span><span class="sxs-lookup"><span data-stu-id="8fc63-155">You can set the repair stages of a repair line to track the progress of the repair.</span></span>

<span data-ttu-id="8fc63-156">修復の問題を解決したら、修復行をクローズできます。</span><span class="sxs-lookup"><span data-stu-id="8fc63-156">When a repair issue is resolved, you can close the repair line.</span></span> <span data-ttu-id="8fc63-157">修復ステージを **完了** プロパティが有効になったステージに設定します。</span><span class="sxs-lookup"><span data-stu-id="8fc63-157">Set the repair stage to a stage with a **Finished** property enabled.</span></span> <span data-ttu-id="8fc63-158">現在の日時が完了時刻として修復行に登録されます。</span><span class="sxs-lookup"><span data-stu-id="8fc63-158">The current date and time is registered as the finish time on the line.</span></span>

## <a name="close-a-repair-line-for-a-resolved-issue"></a><span data-ttu-id="8fc63-159">解決された問題の修復行のクローズ</span><span class="sxs-lookup"><span data-stu-id="8fc63-159">Close a repair line for a resolved issue</span></span>

1.  <span data-ttu-id="8fc63-160">**修復行** フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="8fc63-160">Open the **Repair lines** form.</span></span> <span data-ttu-id="8fc63-161">このトピックの前の手順に従って、修復行を作成します。</span><span class="sxs-lookup"><span data-stu-id="8fc63-161">Follow the procedure earlier in this topic to create a repair line.</span></span>

2.  <span data-ttu-id="8fc63-162">クローズする修復の問題を含む修復行を選択します。</span><span class="sxs-lookup"><span data-stu-id="8fc63-162">Select the repair line with the repair issue that you want to close.</span></span>

3.  <span data-ttu-id="8fc63-163">**修復ステージ** フィールドで、**完了済** プロパティが有効になっているステージを選択します。</span><span class="sxs-lookup"><span data-stu-id="8fc63-163">In the **Repair stage** field, select a stage with the **Finished** property enabled.</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]