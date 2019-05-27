---
title: 電子署名の設定
description: 電子署名を設定するには、この手順を使用します。
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysConfiguration, SIGParameters, SIGReasonCode, SIGProcSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eb6bf529b1e94d598e219482f182140402f2928a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545525"
---
# <a name="set-up-electronic-signatures"></a><span data-ttu-id="bdc13-103">電子署名の設定</span><span class="sxs-lookup"><span data-stu-id="bdc13-103">Set up electronic signatures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bdc13-104">電子署名を設定するには、この手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="bdc13-104">Use this procedure to set up electronic signatures.</span></span> <span data-ttu-id="bdc13-105">電子署名は、コンピューティング プロセスの開始者または承認者を確認するための ID です。</span><span class="sxs-lookup"><span data-stu-id="bdc13-105">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="bdc13-106">この手順の作成に使用するデモ データの会社は DAT です。</span><span class="sxs-lookup"><span data-stu-id="bdc13-106">The demo data company used to create this procedure is DAT.</span></span>


## <a name="enable-the-electronic-signature-configuration-key"></a><span data-ttu-id="bdc13-107">電子署名コンフィギュレーション キーの有効化</span><span class="sxs-lookup"><span data-stu-id="bdc13-107">Enable the Electronic signature configuration key</span></span>
1. <span data-ttu-id="bdc13-108">[システム管理] > [設定] > [ライセンス コンフィギュレーション] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="bdc13-108">Go to System administration > Setup > License configuration.</span></span>
2. <span data-ttu-id="bdc13-109">ツリーで、[管理] を展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="bdc13-109">In the tree, expand 'Administration'.</span></span>
    * <span data-ttu-id="bdc13-110">[電子署名] チェック ボックスがオンになっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="bdc13-110">Verify that the Electronic signature check box is selected.</span></span>  
    * <span data-ttu-id="bdc13-111">[電子署名] チェック ボックスがオフの場合、メンテナンス モードを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="bdc13-111">If the Electronic signature check box is not selected, you must enable maintenance mode.</span></span> <span data-ttu-id="bdc13-112">この環境でメンテナンス モードを有効にするには、Lifecycle Services からメンテナンス ジョブを実行するか、ローカルから Deployment.Setup ツールを使用します。</span><span class="sxs-lookup"><span data-stu-id="bdc13-112">Maintenance mode can be enabled in this environment by running a maintenance job from Lifecycle Services, or by using the Deployment.Setup tool locally.</span></span>  
3. <span data-ttu-id="bdc13-113">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="bdc13-113">Close the page.</span></span>

## <a name="set-up-electronic-signature-parameters"></a><span data-ttu-id="bdc13-114">電子署名のパラメータの設定</span><span class="sxs-lookup"><span data-stu-id="bdc13-114">Set up electronic signature parameters</span></span>
1. <span data-ttu-id="bdc13-115">[組織管理] > [設定] > [電子署名] > [電子署名のパラメーター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bdc13-115">Go to Organization administration > Setup > Electronic signature > Electronic signature parameters.</span></span>
2. <span data-ttu-id="bdc13-116">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bdc13-116">Click Edit.</span></span>
3. <span data-ttu-id="bdc13-117">[通知] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="bdc13-117">In the Notice field, type a value.</span></span>
    * <span data-ttu-id="bdc13-118">署名が要求されている場合に署名者が受け取る通知を入力します。</span><span class="sxs-lookup"><span data-stu-id="bdc13-118">Enter the notice that signers will receive when a signature is requested.</span></span> <span data-ttu-id="bdc13-119">任意のテキストを入力できます。</span><span class="sxs-lookup"><span data-stu-id="bdc13-119">You can enter any text.</span></span> <span data-ttu-id="bdc13-120">通常、このテキストでは、ドキュメントに電子的に署名する意味をユーザーに説明します。</span><span class="sxs-lookup"><span data-stu-id="bdc13-120">Typically, this text tells the user what it means to sign a document electronically.</span></span>  
    * <span data-ttu-id="bdc13-121">追加の言語で通知テキストを入力する場合は、[翻訳] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="bdc13-121">If you want to enter the Notice text in additional languages, click the Translations button.</span></span>  
4. <span data-ttu-id="bdc13-122">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bdc13-122">Click Save.</span></span>
5. <span data-ttu-id="bdc13-123">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="bdc13-123">Close the page.</span></span>

## <a name="set-up-reason-codes-for-electronic-signatures"></a><span data-ttu-id="bdc13-124">電子署名の理由コードの設定</span><span class="sxs-lookup"><span data-stu-id="bdc13-124">Set up reason codes for electronic signatures</span></span>
1. <span data-ttu-id="bdc13-125">[組織管理] > [設定] > [電子署名] > [電子署名の理由コード] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bdc13-125">Go to Organization administration > Setup > Electronic signature > Electronic signature reason codes.</span></span>
2. <span data-ttu-id="bdc13-126">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bdc13-126">Click New.</span></span>
    * <span data-ttu-id="bdc13-127">電子署名を使用する前に理由コードを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bdc13-127">You must set up reason codes before using electronic signatures.</span></span> <span data-ttu-id="bdc13-128">ドキュメントに署名するとき、有効な理由コードが必要です。</span><span class="sxs-lookup"><span data-stu-id="bdc13-128">A valid reason code is required when signing a document.</span></span>     <span data-ttu-id="bdc13-129">署名者は、電子署名の目的を示す理由コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="bdc13-129">A signer selects a reason code to indicate the purpose of an electronic signature.</span></span> <span data-ttu-id="bdc13-130">たとえば、理由コードを使用して法的な承認を示すことができます。</span><span class="sxs-lookup"><span data-stu-id="bdc13-130">For example, a reason code could be used to indicate legal approval.</span></span>  
3. <span data-ttu-id="bdc13-131">[理由コード] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="bdc13-131">In the Reason code field, type a value.</span></span>
4. <span data-ttu-id="bdc13-132">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="bdc13-132">In the Description field, type a value.</span></span>
    * <span data-ttu-id="bdc13-133">必要に応じて、追加の理由コードを入力します。</span><span class="sxs-lookup"><span data-stu-id="bdc13-133">Enter additional reason codes, if needed.</span></span>  
5. <span data-ttu-id="bdc13-134">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bdc13-134">Click Save.</span></span>
6. <span data-ttu-id="bdc13-135">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="bdc13-135">Close the page.</span></span>

## <a name="require-electronic-signatures-for-existing-processes"></a><span data-ttu-id="bdc13-136">既存のプロセスに対する電子署名の要求</span><span class="sxs-lookup"><span data-stu-id="bdc13-136">Require electronic signatures for existing processes</span></span>
1. <span data-ttu-id="bdc13-137">[組織管理] > [設定] > [電子署名] > [電子署名要求] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bdc13-137">Go to Organization administration > Setup > Electronic signature > Electronic signature requirements.</span></span>
2. <span data-ttu-id="bdc13-138">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="bdc13-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="bdc13-139">電子署名を要求するプロセスを選択します。</span><span class="sxs-lookup"><span data-stu-id="bdc13-139">Select a process that requires electronic signatures.</span></span>  
3. <span data-ttu-id="bdc13-140">必要に応じて、[署名必須] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="bdc13-140">Select or clear the Signature required check box.</span></span>
    * <span data-ttu-id="bdc13-141">電子署名を要求する各プロセスで、これらの手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="bdc13-141">Repeat these steps for each process that requires electronic signatures.</span></span>  
4. <span data-ttu-id="bdc13-142">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bdc13-142">Click Save.</span></span>

## <a name="create-a-custom-requirement-for-electronic-signatures"></a><span data-ttu-id="bdc13-143">電子署名のカスタム要求の作成</span><span class="sxs-lookup"><span data-stu-id="bdc13-143">Create a custom requirement for electronic signatures</span></span>
1. <span data-ttu-id="bdc13-144">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bdc13-144">Click New.</span></span>
2. <span data-ttu-id="bdc13-145">必要に応じて、[署名必須] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="bdc13-145">Select or clear the Signature required check box.</span></span>
3. <span data-ttu-id="bdc13-146">[名前] フィールドに、電子署名を要求するプロセスの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="bdc13-146">In the Name field, enter a name for the process that requires electronic signatures.</span></span>
4. <span data-ttu-id="bdc13-147">[テーブル名] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="bdc13-147">In the Table name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="bdc13-148">リストで、署名を必要とするデータが保存されているテーブルを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="bdc13-148">In the list, find and select the table where the data that must be signed is stored.</span></span>
6. <span data-ttu-id="bdc13-149">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="bdc13-149">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="bdc13-150">[フィールド名] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="bdc13-150">In the Field name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="bdc13-151">リストで、テーブルの監視対象のフィールドを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="bdc13-151">In the list, find and select the field in the table that you want to monitor.</span></span>
9. <span data-ttu-id="bdc13-152">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="bdc13-152">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="bdc13-153">どのような場合に署名が必要かを指定します。</span><span class="sxs-lookup"><span data-stu-id="bdc13-153">Specify when a signature is required.</span></span>     <span data-ttu-id="bdc13-154">フィールドのデータが変更されるときに署名を要求する場合は、[常に] を選択します。</span><span class="sxs-lookup"><span data-stu-id="bdc13-154">Select Always if a signature is required when the data in the field changes.</span></span>     <span data-ttu-id="bdc13-155">署名が特定の条件下のみで必要な場合は、[1 回だけ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="bdc13-155">Select Only if a signature is required only under certain conditions.</span></span> <span data-ttu-id="bdc13-156">[1 回だけ] を選択する際、次のいすれかのオプションも選択する必要があります: レコードの挿入時、更新時、または削除時。</span><span class="sxs-lookup"><span data-stu-id="bdc13-156">If you select Only, you must also select one of the following options: When a record is inserted, When a record is updated, or When a record is deleted.</span></span>  
10. <span data-ttu-id="bdc13-157">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bdc13-157">Click Save.</span></span>
11. <span data-ttu-id="bdc13-158">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="bdc13-158">Close the page.</span></span>

